---
title: 顯示同步處理進度
description: 顯示同步處理進度
ms.assetid: 5ca4d6ae-822e-4ddc-950d-cf7df6889108
keywords:
- Windows Media Player，可攜式裝置
- Windows Media Player 物件模型，可攜式裝置
- 物件模型，可攜式裝置
- Windows Media Player 的 ActiveX 控制項、可攜式裝置
- ActiveX 控制項、可攜式裝置
- Windows Media Player Mobile ActiveX 控制項、可攜式裝置
- Windows Media Player Mobile、可攜式裝置
- 可攜式裝置，同步處理進度
- 裝置同步處理，顯示進度
- 正在同步處理裝置，顯示進度
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3f109f09d4efacef620a2c21691f50cc0ac2143
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "103841896"
---
# <a name="showing-synchronization-progress"></a>顯示同步處理進度

您可以向使用者顯示同步處理進度。 下列範例程式碼示範如何使用 **IWMPSyncDevice：： get \_ 進度** 來建立計時器，以定期取出目前的進度值。 請注意，抓取的進度值代表每個裝置的整個同步處理作業的進度。 不支援取得個別媒體專案的同步處理進度。

若要判斷何時啟動或停止計時器，請處理 **DeviceSyncStateChange** 事件。 下列範例函數示範這類事件處理常式。 程式碼也會使用名為 IDC SYNCSTATE 的靜態文字控制項，將目前的同步處理狀態顯示為文字字串 \_ 。


```C++
void CMainDlg::DeviceSyncStateChange( IWMPSyncDevice * pDevice, WMPSyncState NewState )
{
    if(NULL == pDevice)
    {
        return;
    }

    HRESULT hr = E_POINTER;
    VARIANT_BOOL  vbIdentical = VARIANT_FALSE;
    // Window handle for static text control that shows the sync state.
    HWND hwndSyncStateText = GetDlgItem(IDC_SYNCSTATE); 

    // Strings to show sync state.
    const TCHAR *szSyncState[3] = {
    _T("Unknown"),
    _T("Synchronizing"),
    _T("Stopped")};

    // Get a pointer to the device the user selected in the list box.    
    CComPtr<IWMPSyncDevice> spDevice(m_ppWMPDevices[GetSelectedDeviceIndex()]); 
    // Cache the pointer to the device that raised the event.
    CComPtr<IWMPSyncDevice> spDeviceParam(pDevice); 

    if(spDevice.p)
    {
        // Test whether the device that raised the event is the same as 
        // the one the user selected.
        hr = spDevice->isIdentical(spDeviceParam, &vbIdentical);
    }

    if(SUCCEEDED(hr) &&
        vbIdentical == VARIANT_TRUE)
    {    
        // Display the sync state.
        SendMessage(hwndSyncStateText, WM_SETTEXT, 0, (LPARAM)szSyncState[NewState]);

        switch(NewState)
        {
        case wmpssSynchronizing:
            // Start the progress timer.
            SetTimer(1, 1000, NULL);
            SetUIState(Synchronizing, TRUE);
            break;
        case wmpssStopped:
            // Stop the progress timer.
            KillTimer(1);
            // Make sure the final progress is displayed.            
            ShowProgress(GetSelectedDeviceIndex());
            SetUIState(Partnership, TRUE);
            break;      
        default:
            break;
        }
    }    
}
```



當計時器正在執行時，它會 \_ 以一秒的間隔傳送 WM 計時器訊息。 應用程式會 \_ 在其訊息迴圈中處理 WM 計時器。

下列範例函式示範如何使用靜態文字控制項 (IDC PROGSTATIC) 來顯示進度 \_ ，以及 (idc SYNCPROG) 使用進度控制項 \_ 。 呼叫此函式以回應 WM \_ 計時器訊息，以及在同步處理常式完成時，如上述範例所示。


```C++
STDMETHODIMP CMainDlg::ShowProgress(long lIndex)
{  
    ATLASSERT(m_ppWMPDevices);

    long lProgress = 0;
    WCHAR buffer[10]; // Buffer larger than needed to hold progress string.
    ZeroMemory(buffer, sizeof WCHAR * 10);

    // Retrieve a handle to the progress control
    HWND  hwndSyncProgressCtl = GetDlgItem(IDC_SYNCPROG); 
    // Retrieve a handle to the static control that displays 
    // progress as text.
    HWND  hwndSyncProgressText = GetDlgItem(IDC_PROGSTATIC); 

    CComPtr<IWMPSyncDevice> spDevice(m_ppWMPDevices[lIndex]);
    
    HRESULT hr = spDevice->get_progress(&lProgress);

    // Convert progress to a string and add the percent character.
    _ltow(lProgress, buffer, 10);
    CComBSTR bstrProgress(buffer);
    bstrProgress += " %";

    // Display the text.
    ::SendMessage(hwndSyncProgressText, WM_SETTEXT, 0, (LPARAM)(LPCTSTR)COLE2T(bstrProgress));
    // Set the progress control position.
    ::SendMessage(hwndSyncProgressCtl, PBM_SETPOS, (WPARAM)(int)lProgress, 0);

    return hr;
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**列舉裝置**](enumerating-devices.md)
</dt> <dt>

[**IWMPSyncDevice 介面**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice)
</dt> <dt>

[**IWMPSyncDevice：：取得 \_ 進度**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_progress)
</dt> <dt>

[**IWMPSyncDevice：： isIdentical**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-isidentical)
</dt> <dt>

[**使用可攜式裝置**](working-with-portable-devices.md)
</dt> </dl>

 

 




