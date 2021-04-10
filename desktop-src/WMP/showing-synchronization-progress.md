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
# <a name="showing-synchronization-progress"></a><span data-ttu-id="c1fb8-113">顯示同步處理進度</span><span class="sxs-lookup"><span data-stu-id="c1fb8-113">Showing Synchronization Progress</span></span>

<span data-ttu-id="c1fb8-114">您可以向使用者顯示同步處理進度。</span><span class="sxs-lookup"><span data-stu-id="c1fb8-114">You can display synchronization progress to the user.</span></span> <span data-ttu-id="c1fb8-115">下列範例程式碼示範如何使用 **IWMPSyncDevice：： get \_ 進度** 來建立計時器，以定期取出目前的進度值。</span><span class="sxs-lookup"><span data-stu-id="c1fb8-115">The following example code shows how to create a timer to periodically retrieve the current progress value by using **IWMPSyncDevice::get\_progress**.</span></span> <span data-ttu-id="c1fb8-116">請注意，抓取的進度值代表每個裝置的整個同步處理作業的進度。</span><span class="sxs-lookup"><span data-stu-id="c1fb8-116">Note that the progress value retrieved represents the progress for the entire synchronization operation for each device.</span></span> <span data-ttu-id="c1fb8-117">不支援取得個別媒體專案的同步處理進度。</span><span class="sxs-lookup"><span data-stu-id="c1fb8-117">Retrieving synchronization progress for individual media items is not supported.</span></span>

<span data-ttu-id="c1fb8-118">若要判斷何時啟動或停止計時器，請處理 **DeviceSyncStateChange** 事件。</span><span class="sxs-lookup"><span data-stu-id="c1fb8-118">To determine when to start or stop the timer, handle the **DeviceSyncStateChange** event.</span></span> <span data-ttu-id="c1fb8-119">下列範例函數示範這類事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="c1fb8-119">The following example function demonstrates such an event handler.</span></span> <span data-ttu-id="c1fb8-120">程式碼也會使用名為 IDC SYNCSTATE 的靜態文字控制項，將目前的同步處理狀態顯示為文字字串 \_ 。</span><span class="sxs-lookup"><span data-stu-id="c1fb8-120">The code also displays the current synchronization state as a text string using a static text control, named IDC\_SYNCSTATE.</span></span>


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



<span data-ttu-id="c1fb8-121">當計時器正在執行時，它會 \_ 以一秒的間隔傳送 WM 計時器訊息。</span><span class="sxs-lookup"><span data-stu-id="c1fb8-121">When the timer is running, it sends a WM\_TIMER message at one-second intervals.</span></span> <span data-ttu-id="c1fb8-122">應用程式會 \_ 在其訊息迴圈中處理 WM 計時器。</span><span class="sxs-lookup"><span data-stu-id="c1fb8-122">The application handles WM\_TIMER in its message loop.</span></span>

<span data-ttu-id="c1fb8-123">下列範例函式示範如何使用靜態文字控制項 (IDC PROGSTATIC) 來顯示進度 \_ ，以及 (idc SYNCPROG) 使用進度控制項 \_ 。</span><span class="sxs-lookup"><span data-stu-id="c1fb8-123">The following example function demonstrates how to show progress by using both a static text control (IDC\_PROGSTATIC), and using a progress control (IDC\_SYNCPROG).</span></span> <span data-ttu-id="c1fb8-124">呼叫此函式以回應 WM \_ 計時器訊息，以及在同步處理常式完成時，如上述範例所示。</span><span class="sxs-lookup"><span data-stu-id="c1fb8-124">Call this function in response to the WM\_TIMER message and upon completion of the synchronization process, as shown in the preceding example.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="c1fb8-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="c1fb8-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c1fb8-126">**列舉裝置**</span><span class="sxs-lookup"><span data-stu-id="c1fb8-126">**Enumerating Devices**</span></span>](enumerating-devices.md)
</dt> <dt>

[<span data-ttu-id="c1fb8-127">**IWMPSyncDevice 介面**</span><span class="sxs-lookup"><span data-stu-id="c1fb8-127">**IWMPSyncDevice Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice)
</dt> <dt>

[<span data-ttu-id="c1fb8-128">**IWMPSyncDevice：：取得 \_ 進度**</span><span class="sxs-lookup"><span data-stu-id="c1fb8-128">**IWMPSyncDevice::get\_progress**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_progress)
</dt> <dt>

[<span data-ttu-id="c1fb8-129">**IWMPSyncDevice：： isIdentical**</span><span class="sxs-lookup"><span data-stu-id="c1fb8-129">**IWMPSyncDevice::isIdentical**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-isidentical)
</dt> <dt>

[<span data-ttu-id="c1fb8-130">**使用可攜式裝置**</span><span class="sxs-lookup"><span data-stu-id="c1fb8-130">**Working with Portable Devices**</span></span>](working-with-portable-devices.md)
</dt> </dl>

 

 




