---
title: 正在取出燒錄狀態
description: 正在取出燒錄狀態
ms.assetid: 63b6525d-00be-4c68-8473-3bc1a58fde15
keywords:
- Windows Media Player、CD 燒錄
- Windows Media Player 物件模型，CD 燒錄
- 物件模型，CD 燒錄
- Windows Media Player ActiveX 控制項、CD 燒錄
- ActiveX 控制項，CD 燒錄
- Windows Media Player 的行動 ActiveX 控制項、CD 燒錄
- Windows Media Player Mobile、CD 燒錄
- CD 燒錄，正在取出燒錄狀態
- 燒錄 Cd，正在取出燒錄狀態
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e9b9ab1d865b728c3a23b9b77f45ab022226605
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "103932947"
---
# <a name="retrieving-the-burn-status"></a>正在取出燒錄狀態

在接下來的程式碼範例中，會定義下列對話方塊控制項：



| 控制識別碼           | Description                                                                    |
|----------------------|--------------------------------------------------------------------------------|
| IDC \_ 燒錄 \_ 狀態     | 表示 CD 燒錄操作狀態的靜態文字。             |
| IDC \_ 進度        | 範圍為0到100的進度列，表示總燒錄進度。 |
| IDC \_ 進度 \_ 文字  | 以0到100的數位表示總燒錄進度的靜態文字。 |
| IDC \_ 可用 \_ 時間 | 顯示 CD 可用時間的靜態文字（以秒為單位）。               |
| IDC \_ 可用 \_ 空間     | 靜態文字，用來顯示 CD 上的可用空間（以位元組為單位）。                     |
| IDC \_ 總 \_ 空間    | 靜態文字，可顯示 CD 的總容量（以位元組為單位）。                 |



 

您可以在燒錄 CD 時，定期呼叫 [IWMPCdromBurn：： get \_ burnProgress](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-get_burnprogress) 來監視燒錄作業的進度。 這個方法會抓取整個燒錄作業的進度值。 抓取的值是代表完成的燒錄百分比的數位，從0到100。


```C++
// Update the progress bar IDC_PROGRESS
// and the corresponding text string IDC_PROGRESS_TEXT.
long lProgress = 0;
hr = m_spCdromBurn->get_burnProgress(&lProgress);
if (SUCCEEDED(hr))
{
    SendMessage(GetDlgItem(IDC_PROGRESS),
        PBM_SETPOS, lProgress, 0);
    SetDlgItemInt(IDC_PROGRESS_TEXT, lProgress);
}

```



您可以藉由呼叫 [IWMPCdromBurn：： get \_ burnState](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-get_burnstate)取得燒錄作業的目前狀態。 這個方法會抓取指定目前正在執行之作業的列舉。


```C++
// Retrieve the burn state.
WMPBurnState wmpbs = wmpbsUnknown;
HRESULT hr = m_spCdromBurn->get_burnState(&wmpbs);

if (SUCCEEDED(hr))
{
    // Set the burn state string.
    CComBSTR bstrState;
    switch (wmpbs)
    {
        case wmpbsUnknown:
        default:
            hr = bstrState.Append("Unknown state.");
            break;
        case wmpbsBusy:
            hr = bstrState.Append("Windows Media Player is Busy.");
            break;
        case wmpbsReady:
            hr = bstrState.Append("Ready to begin burning.");
            break;
        case wmpbsWaitingForDisc:
            hr = bstrState.Append("Waiting for disc.");
            break;
        case wmpbsRefreshStatusPending:
            hr = bstrState.Append("The burn playlist has changed.");
            m_spCdromBurn->refreshStatus();
            break;
        case wmpbsPreparingToBurn:
            hr = bstrState.Append("Preparing to burn the CD.");
            break;
        case wmpbsBurning:
            hr = bstrState.Append("The CD is being burned.");
            break;
        case wmpbsStopped:
            hr = bstrState.Append("The burning operation is stopped.");
            break;
        case wmpbsErasing:
            hr = bstrState.Append("Erasing the CD.");
            break;
    }
    if (SUCCEEDED(hr))
    {
        SetDlgItemTextW(IDC_BURN_STATE, bstrState.m_str);
    }
}

```



若要抓取 CD 可保存的音訊秒數，請使用 "AvailableTime" 作為第一個參數來呼叫 [IWMPCdromBurn：： getItemInfo](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-getiteminfo) 。 這個函式所抓取的值是以字串表示。


```C++
// Set "AvailableTime" string
CComBSTR bstrTime;
CComBSTR bstrItem;
HRESULT hr = bstrItem.Append("AvailableTime");
if (SUCCEEDED(hr))
{
    hr = m_spCdromBurn->getItemInfo(bstrItem, &bstrTime);
}
if (SUCCEEDED(hr))
{
    hr = bstrTime.Append(" seconds");
}
if (SUCCEEDED(hr))
{
    SetDlgItemTextW(IDC_AVAILABLE_TIME, bstrTime.m_str);
}

```



若要取出光碟上的可用空間量，請使用 "可空間" 來呼叫 **IWMPCdromBurn：： getItemInfo** 作為第一個參數。 此函式所抓取的值是表示光碟上可用位元組數的字串。


```C++
// Set "FreeSpace" string
CComBSTR bstrFreeSpace;
CComBSTR bstrItem;
HRESULT hr = bstrItem.Append("FreeSpace");
if (SUCCEEDED(hr))
{
    hr = m_spCdromBurn->getItemInfo(bstrItem, &bstrFreeSpace);
}
if (SUCCEEDED(hr))
{
    hr = bstrFreeSpace.Append(" bytes");
}
if (SUCCEEDED(hr))
{
    SetDlgItemTextW(IDC_FREE_SPACE, bstrFreeSpace.m_str);
}

```



若要取出磁片的總容量，請以 "TotalSpace" 作為第一個參數來呼叫 **IWMPCdromBurn：： getItemInfo** 。 此函式所抓取的值是對應到光碟上的總位元組數的字串。


```C++
// Set "TotalSpace" string.
CComBSTR bstrTotalSpace;
CComBSTR bstrItem;
HRESULT hr = bstrItem.Append("TotalSpace");
if (SUCCEEDED(hr))
{
    hr = m_spCdromBurn->getItemInfo(bstrItem, &bstrTotalSpace);
}
if (SUCCEEDED(hr))
{
    hr = bstrTotalSpace.Append(" bytes");
}
if (SUCCEEDED(hr))
{
    SetDlgItemTextW(IDC_TOTAL_SPACE, bstrTotalSpace.m_str);
}

```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**燒錄 CD**](burning-a-cd.md)
</dt> <dt>

[**擷取 CD 燒錄介面**](retrieving-the-cd-burning-interface.md)
</dt> <dt>

[**啟動燒錄流程**](starting-the-burn-process.md)
</dt> <dt>

[**清除可讀寫 CD**](erasing-a-rewritable-cd.md)
</dt> <dt>

[**正在抓取磁片磁碟機和光碟狀態**](retrieving-the-drive-and-disc-status.md)
</dt> </dl>

 

 




