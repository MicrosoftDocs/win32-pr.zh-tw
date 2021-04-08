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
# <a name="retrieving-the-rip-status"></a><span data-ttu-id="7410d-112">正在抓取 Rip 狀態</span><span class="sxs-lookup"><span data-stu-id="7410d-112">Retrieving the Rip Status</span></span>

<span data-ttu-id="7410d-113">您可以定期呼叫 [IWMPCdromRip：： get \_ ripProgress](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-get_ripprogress)來監視翻錄作業的進度。</span><span class="sxs-lookup"><span data-stu-id="7410d-113">You can monitor the progress of the ripping operation by periodically calling [IWMPCdromRip::get\_ripProgress](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-get_ripprogress).</span></span> <span data-ttu-id="7410d-114">這個方法會抓取整個翻錄作業的進度值。</span><span class="sxs-lookup"><span data-stu-id="7410d-114">This method retrieves a progress value for the entire ripping operation.</span></span> <span data-ttu-id="7410d-115">抓取的值是代表已完成的完成百分比的數位，從0到100。</span><span class="sxs-lookup"><span data-stu-id="7410d-115">The value retrieved is a number that represents the percentage of ripping completed, from 0 to 100.</span></span>

<span data-ttu-id="7410d-116">進度值代表整個翻錄進程的完成百分比。</span><span class="sxs-lookup"><span data-stu-id="7410d-116">The progress value represents the completed percentage of the entire ripping process.</span></span> <span data-ttu-id="7410d-117">若要判斷特定追蹤的進度，請使用 [IWMPMedia：： getItemInfo](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia-getiteminfo) 搭配 "RipProgress" 作為屬性名稱。</span><span class="sxs-lookup"><span data-stu-id="7410d-117">To determine the progress of a specific track, use [IWMPMedia::getItemInfo](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia-getiteminfo) with "RipProgress" as the attribute name.</span></span> <span data-ttu-id="7410d-118">若要判斷目前正在翻錄之追蹤的索引，請使用 "CurrentRipTrackIndex" 來呼叫 **IWMPPlaylist：： getItemInfo** 作為屬性名稱。</span><span class="sxs-lookup"><span data-stu-id="7410d-118">To determine the index of the track currently being ripped, call **IWMPPlaylist::getItemInfo** with "CurrentRipTrackIndex" as the attribute name.</span></span>

<span data-ttu-id="7410d-119">您可以定期呼叫 [IWMPCdromRip：： get \_ ripState](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-get_ripstate)來監視翻錄作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="7410d-119">You can monitor the state of the ripping operation by periodically calling [IWMPCdromRip::get\_ripState](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-get_ripstate).</span></span> <span data-ttu-id="7410d-120">這個方法會抓取 [WMPRipState](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpripstate) 列舉值，這個值表示作業正在進行中或已停止。</span><span class="sxs-lookup"><span data-stu-id="7410d-120">This method retrieves a [WMPRipState](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpripstate) enumeration value that indicates whether the operation is in progress or stopped.</span></span> <span data-ttu-id="7410d-121">您也可以藉由處理 [IWMPEvents3：： CdromRipStateChange](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-cdromripstatechange) 事件，來監視「翻錄」作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="7410d-121">You can also monitor the state of the ripping operation by handling the [IWMPEvents3::CdromRipStateChange](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-cdromripstatechange) event.</span></span> <span data-ttu-id="7410d-122"> (參閱 [在 c + + 中處理事件](handling-events-in-c.md)。 ) 請小心將事件) 所提供的 **IWMPCdromRip** 指標 (，與代表您的翻錄作業的指標進行比較，以確保您的作業會引發事件。</span><span class="sxs-lookup"><span data-stu-id="7410d-122">(See [Handling Events in C++](handling-events-in-c.md).) Be careful to compare the **IWMPCdromRip** pointer (provided by the event) to the pointer that represents your ripping operation, to ensure that the event was raised by your operation.</span></span>

<span data-ttu-id="7410d-123">下列範例程式碼示範如何使用這些函式來取得「翻錄」作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="7410d-123">The following example code shows how to use these functions to retrieve the status of a ripping operation.</span></span>

<span data-ttu-id="7410d-124">下列是針對程式碼範例定義的對話方塊控制項。</span><span class="sxs-lookup"><span data-stu-id="7410d-124">The following dialog controls are defined for the code example.</span></span>



| <span data-ttu-id="7410d-125">控制識別碼</span><span class="sxs-lookup"><span data-stu-id="7410d-125">Control ID</span></span>                   | <span data-ttu-id="7410d-126">Description</span><span class="sxs-lookup"><span data-stu-id="7410d-126">Description</span></span>                                                                                                        |
|------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7410d-127">IDC \_ 目前的 \_ 追蹤</span><span class="sxs-lookup"><span data-stu-id="7410d-127">IDC\_CURRENT\_TRACK</span></span>          | <span data-ttu-id="7410d-128">靜態文字，代表目前正在進行翻錄的曲目索引。</span><span class="sxs-lookup"><span data-stu-id="7410d-128">Static text that represents the index of the track currently being ripped.</span></span>                                         |
| <span data-ttu-id="7410d-129">IDC \_ 追蹤 \_ 進度 \_ 文字</span><span class="sxs-lookup"><span data-stu-id="7410d-129">IDC\_TRACK\_PROGRESS\_TEXT</span></span>   | <span data-ttu-id="7410d-130">靜態文字，表示目前以百分比形式翻錄的曲目進度。</span><span class="sxs-lookup"><span data-stu-id="7410d-130">Static text that represents the progress of the track currently being ripped as a percentage.</span></span>                      |
| <span data-ttu-id="7410d-131">IDC \_ 進度 \_ 追蹤</span><span class="sxs-lookup"><span data-stu-id="7410d-131">IDC\_PROGRESS\_TRACK</span></span>         | <span data-ttu-id="7410d-132">範圍0到100的進度列，代表目前正在翻錄為百分比的曲目進度。</span><span class="sxs-lookup"><span data-stu-id="7410d-132">Progress bar with range 0 to 100 that represents the progress of the track currently being ripped as a percentage.</span></span> |
| <span data-ttu-id="7410d-133">IDC \_ 整體 \_ 進度 \_ 文字</span><span class="sxs-lookup"><span data-stu-id="7410d-133">IDC\_OVERALL\_PROGRESS\_TEXT</span></span> | <span data-ttu-id="7410d-134">表示以百分比表示之總翻錄進程進度的靜態文字。</span><span class="sxs-lookup"><span data-stu-id="7410d-134">Static text that represents the progress of the total ripping process as a percentage.</span></span>                             |
| <span data-ttu-id="7410d-135">IDC \_ \_ 整體進度</span><span class="sxs-lookup"><span data-stu-id="7410d-135">IDC\_PROGRESS\_OVERALL</span></span>       | <span data-ttu-id="7410d-136">範圍0到100的進度列，表示總翻錄進程的進度（以百分比表示）。</span><span class="sxs-lookup"><span data-stu-id="7410d-136">Progress bar with range 0 to 100 that represents the progress of the total ripping process as a percentage.</span></span>        |
| <span data-ttu-id="7410d-137">IDC \_ RIP \_ 狀態</span><span class="sxs-lookup"><span data-stu-id="7410d-137">IDC\_RIP\_STATE</span></span>              | <span data-ttu-id="7410d-138">顯示目前正在執行之作業 ( 「正在完成」、「已停止」或「未知」 ) 的靜態文字</span><span class="sxs-lookup"><span data-stu-id="7410d-138">Static text that displays the operation currently being performed ("Ripping", "Stopped", or "Unknown")</span></span>             |



 


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



## <a name="related-topics"></a><span data-ttu-id="7410d-139">相關主題</span><span class="sxs-lookup"><span data-stu-id="7410d-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7410d-140">**將 CD 翻錄**</span><span class="sxs-lookup"><span data-stu-id="7410d-140">**Ripping a CD**</span></span>](ripping-a-cd.md)
</dt> <dt>

[<span data-ttu-id="7410d-141">**擷取轉錄介面**</span><span class="sxs-lookup"><span data-stu-id="7410d-141">**Retrieving the Ripping Interface**</span></span>](retrieving-the-ripping-interface.md)
</dt> <dt>

[<span data-ttu-id="7410d-142">**啟動 Rip 進程**</span><span class="sxs-lookup"><span data-stu-id="7410d-142">**Starting the Rip Process**</span></span>](starting-the-rip-process.md)
</dt> <dt>

[<span data-ttu-id="7410d-143">**選取要進行翻錄的專案**</span><span class="sxs-lookup"><span data-stu-id="7410d-143">**Selecting Items for Ripping**</span></span>](selecting-items-for-ripping.md)
</dt> </dl>

 

 




