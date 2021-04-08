---
title: 正在抓取 Rip 狀態
description: 正在抓取 Rip 狀態
ms.assetid: 9907bfdd-eae7-4ca2-b488-5a6ad11416f5
keywords:
- Windows Media Player、CD 翻錄
- Windows Media Player 物件模型，CD 翻錄
- 物件模型、CD 翻錄
- Windows Media Player ActiveX 控制項、CD 翻錄
- ActiveX 控制項，CD 翻錄
- Windows Media Player 的行動 ActiveX 控制項、CD 翻錄
- Windows Media Player 行動電話、CD 翻錄
- CD 翻錄，正在抓取 rip 狀態
- 將 Cd 翻錄，正在抓取 rip 狀態
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3be1fce1a46f9cc2d8477cabcc12a3a1b5bd159d
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104023082"
---
# <a name="retrieving-the-rip-status"></a>正在抓取 Rip 狀態

您可以定期呼叫 [IWMPCdromRip：： get \_ ripProgress](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-get_ripprogress)來監視翻錄作業的進度。 這個方法會抓取整個翻錄作業的進度值。 抓取的值是代表已完成的完成百分比的數位，從0到100。

進度值代表整個翻錄進程的完成百分比。 若要判斷特定追蹤的進度，請使用 [IWMPMedia：： getItemInfo](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia-getiteminfo) 搭配 "RipProgress" 作為屬性名稱。 若要判斷目前正在翻錄之追蹤的索引，請使用 "CurrentRipTrackIndex" 來呼叫 **IWMPPlaylist：： getItemInfo** 作為屬性名稱。

您可以定期呼叫 [IWMPCdromRip：： get \_ ripState](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-get_ripstate)來監視翻錄作業的狀態。 這個方法會抓取 [WMPRipState](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpripstate) 列舉值，這個值表示作業正在進行中或已停止。 您也可以藉由處理 [IWMPEvents3：： CdromRipStateChange](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-cdromripstatechange) 事件，來監視「翻錄」作業的狀態。  (參閱 [在 c + + 中處理事件](handling-events-in-c.md)。 ) 請小心將事件) 所提供的 **IWMPCdromRip** 指標 (，與代表您的翻錄作業的指標進行比較，以確保您的作業會引發事件。

下列範例程式碼示範如何使用這些函式來取得「翻錄」作業的狀態。

下列是針對程式碼範例定義的對話方塊控制項。



| 控制識別碼                   | Description                                                                                                        |
|------------------------------|--------------------------------------------------------------------------------------------------------------------|
| IDC \_ 目前的 \_ 追蹤          | 靜態文字，代表目前正在進行翻錄的曲目索引。                                         |
| IDC \_ 追蹤 \_ 進度 \_ 文字   | 靜態文字，表示目前以百分比形式翻錄的曲目進度。                      |
| IDC \_ 進度 \_ 追蹤         | 範圍0到100的進度列，代表目前正在翻錄為百分比的曲目進度。 |
| IDC \_ 整體 \_ 進度 \_ 文字 | 表示以百分比表示之總翻錄進程進度的靜態文字。                             |
| IDC \_ \_ 整體進度       | 範圍0到100的進度列，表示總翻錄進程的進度（以百分比表示）。        |
| IDC \_ RIP \_ 狀態              | 顯示目前正在執行之作業 ( 「正在完成」、「已停止」或「未知」 ) 的靜態文字             |



 


```C++
HRESULT CMainDlg::UpdateStatus (void)
{
    // bstrItemName and bstrVal are used for getItemInfo.
    CComBSTR bstrItemName;
    CComBSTR bstrVal;

    // Get the current track index.
    HRESULT hr = bstrItemName.Append("CurrentRipTrackIndex");
    if (SUCCEEDED(hr))
    {
        hr = m_spPlaylist->getItemInfo(bstrItemName, &bstrVal);
    }

    // Update the dialog text with the track number.
    if (SUCCEEDED(hr))
    {
        SetDlgItemTextW(IDC_CURRENT_TRACK, bstrVal.m_str);
    }

    // Get an IWMPMedia interface from the Playlist.
    CComPtr<IWMPMedia> spMedia;
    if (SUCCEEDED(hr))
    {
        long lIndex = _wtol(bstrVal.m_str);
        hr = m_spPlaylist->get_item(lIndex, &spMedia);
    }

    // Update the current track progress bar and progress text.
    if (SUCCEEDED(hr))
    {
        bstrItemName.Empty();
        hr = bstrItemName.Append("RipProgress");
    }
    if (SUCCEEDED(hr))
    {
        hr = spMedia->getItemInfo(bstrItemName, &bstrVal);
    }

    if (SUCCEEDED(hr))
    {
        // Update the text corresponding to the percentage.
        SetDlgItemTextW(IDC_TRACK_PROGRESS_TEXT, bstrVal.m_str);

        // Obtain a numerical value from the progress string.
        long lTrackPosition = _wtol(bstrVal.m_str);

        // Update the progress bar showing the percentage.
        SendMessage(GetDlgItem(IDC_PROGRESS_TRACK),
            PBM_SETPOS, lTrackPosition, 0);
    }

    // Update the total progress bar and progress text.
    long lTotalPosition = 0;
    if (SUCCEEDED(hr))
    {
        hr = m_spCdromRip->get_ripProgress(&lTotalPosition);
    }
    if (SUCCEEDED(hr))
    {
        // Update the text corresponding to the percentage.
        SetDlgItemInt(IDC_OVERALL_PROGRESS_TEXT, lTotalPosition);

        // Update the progress bar showing the percentage.
        SendMessage(GetDlgItem(IDC_PROGRESS_OVERALL),
            PBM_SETPOS, lTotalPosition, 0);
    }

    // Update the ripping state.
    CComBSTR bstrState;
    WMPRipState wmprs = wmprsUnknown;
    if (SUCCEEDED(hr))
    {
        hr = m_spCdromRip->get_ripState(&wmprs);
    }
    if (SUCCEEDED(hr))
    {
        switch (wmprs)
        {
            case wmprsUnknown:
            default:
                hr = bstrState.Append("Unknown");
                break;
            case wmprsRipping:
                hr = bstrState.Append("Ripping");
                break;
            case wmprsStopped:
                hr = bstrState.Append("Stopped");
                break;
        }
    }
    if (SUCCEEDED(hr))
    {
        SetDlgItemTextW(IDC_RIP_STATE, bstrState.m_str);
    }

    return hr;
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**將 CD 翻錄**](ripping-a-cd.md)
</dt> <dt>

[**擷取轉錄介面**](retrieving-the-ripping-interface.md)
</dt> <dt>

[**啟動 Rip 進程**](starting-the-rip-process.md)
</dt> <dt>

[**選取要進行翻錄的專案**](selecting-items-for-ripping.md)
</dt> </dl>

 

 




