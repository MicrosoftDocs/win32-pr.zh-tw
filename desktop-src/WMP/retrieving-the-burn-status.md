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
# <a name="retrieving-the-burn-status"></a><span data-ttu-id="8c375-112">正在取出燒錄狀態</span><span class="sxs-lookup"><span data-stu-id="8c375-112">Retrieving the Burn Status</span></span>

<span data-ttu-id="8c375-113">在接下來的程式碼範例中，會定義下列對話方塊控制項：</span><span class="sxs-lookup"><span data-stu-id="8c375-113">In the code example that follows, the following dialog controls are defined:</span></span>



| <span data-ttu-id="8c375-114">控制識別碼</span><span class="sxs-lookup"><span data-stu-id="8c375-114">Control ID</span></span>           | <span data-ttu-id="8c375-115">Description</span><span class="sxs-lookup"><span data-stu-id="8c375-115">Description</span></span>                                                                    |
|----------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="8c375-116">IDC \_ 燒錄 \_ 狀態</span><span class="sxs-lookup"><span data-stu-id="8c375-116">IDC\_BURN\_STATE</span></span>     | <span data-ttu-id="8c375-117">表示 CD 燒錄操作狀態的靜態文字。</span><span class="sxs-lookup"><span data-stu-id="8c375-117">Static text that represents the state of the CD burning operation.</span></span>             |
| <span data-ttu-id="8c375-118">IDC \_ 進度</span><span class="sxs-lookup"><span data-stu-id="8c375-118">IDC\_PROGRESS</span></span>        | <span data-ttu-id="8c375-119">範圍為0到100的進度列，表示總燒錄進度。</span><span class="sxs-lookup"><span data-stu-id="8c375-119">Progress bar with a range of 0 to 100 that represents the total burn progress.</span></span> |
| <span data-ttu-id="8c375-120">IDC \_ 進度 \_ 文字</span><span class="sxs-lookup"><span data-stu-id="8c375-120">IDC\_PROGRESS\_TEXT</span></span>  | <span data-ttu-id="8c375-121">以0到100的數位表示總燒錄進度的靜態文字。</span><span class="sxs-lookup"><span data-stu-id="8c375-121">Static text that represents the total burn progress as a number from 0 to 100.</span></span> |
| <span data-ttu-id="8c375-122">IDC \_ 可用 \_ 時間</span><span class="sxs-lookup"><span data-stu-id="8c375-122">IDC\_AVAILABLE\_TIME</span></span> | <span data-ttu-id="8c375-123">顯示 CD 可用時間的靜態文字（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="8c375-123">Static text to display the time available on the CD, in seconds.</span></span>               |
| <span data-ttu-id="8c375-124">IDC \_ 可用 \_ 空間</span><span class="sxs-lookup"><span data-stu-id="8c375-124">IDC\_FREE\_SPACE</span></span>     | <span data-ttu-id="8c375-125">靜態文字，用來顯示 CD 上的可用空間（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="8c375-125">Static text to display the free space on the CD, in bytes.</span></span>                     |
| <span data-ttu-id="8c375-126">IDC \_ 總 \_ 空間</span><span class="sxs-lookup"><span data-stu-id="8c375-126">IDC\_TOTAL\_SPACE</span></span>    | <span data-ttu-id="8c375-127">靜態文字，可顯示 CD 的總容量（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="8c375-127">Static text to display the total capacity of the CD, in bytes.</span></span>                 |



 

<span data-ttu-id="8c375-128">您可以在燒錄 CD 時，定期呼叫 [IWMPCdromBurn：： get \_ burnProgress](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-get_burnprogress) 來監視燒錄作業的進度。</span><span class="sxs-lookup"><span data-stu-id="8c375-128">You can monitor the progress of the burning operation by periodically calling [IWMPCdromBurn::get\_burnProgress](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-get_burnprogress) while the CD is being burned.</span></span> <span data-ttu-id="8c375-129">這個方法會抓取整個燒錄作業的進度值。</span><span class="sxs-lookup"><span data-stu-id="8c375-129">This method retrieves a progress value for the entire burning operation.</span></span> <span data-ttu-id="8c375-130">抓取的值是代表完成的燒錄百分比的數位，從0到100。</span><span class="sxs-lookup"><span data-stu-id="8c375-130">The value retrieved is a number that represents the percentage of burning completed, from 0 to 100.</span></span>


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



<span data-ttu-id="8c375-131">您可以藉由呼叫 [IWMPCdromBurn：： get \_ burnState](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-get_burnstate)取得燒錄作業的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="8c375-131">You can get the current state of the burning operation by calling [IWMPCdromBurn::get\_burnState](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-get_burnstate).</span></span> <span data-ttu-id="8c375-132">這個方法會抓取指定目前正在執行之作業的列舉。</span><span class="sxs-lookup"><span data-stu-id="8c375-132">This method retrieves an enumeration specifying the current operation being performed.</span></span>


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



<span data-ttu-id="8c375-133">若要抓取 CD 可保存的音訊秒數，請使用 "AvailableTime" 作為第一個參數來呼叫 [IWMPCdromBurn：： getItemInfo](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-getiteminfo) 。</span><span class="sxs-lookup"><span data-stu-id="8c375-133">To retrieve the number of seconds of audio the CD can hold, call [IWMPCdromBurn::getItemInfo](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-getiteminfo) with "AvailableTime" as the first parameter.</span></span> <span data-ttu-id="8c375-134">這個函式所抓取的值是以字串表示。</span><span class="sxs-lookup"><span data-stu-id="8c375-134">The value retrieved by this function is represented by a string.</span></span>


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



<span data-ttu-id="8c375-135">若要取出光碟上的可用空間量，請使用 "可空間" 來呼叫 **IWMPCdromBurn：： getItemInfo** 作為第一個參數。</span><span class="sxs-lookup"><span data-stu-id="8c375-135">To retrieve the amount of free space on a disc, call **IWMPCdromBurn::getItemInfo** with "FreeSpace" as the first parameter.</span></span> <span data-ttu-id="8c375-136">此函式所抓取的值是表示光碟上可用位元組數的字串。</span><span class="sxs-lookup"><span data-stu-id="8c375-136">The value retrieved by this function is a string that represents the number of free bytes available on the disc.</span></span>


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



<span data-ttu-id="8c375-137">若要取出磁片的總容量，請以 "TotalSpace" 作為第一個參數來呼叫 **IWMPCdromBurn：： getItemInfo** 。</span><span class="sxs-lookup"><span data-stu-id="8c375-137">To retrieve the total capacity of a disc, call **IWMPCdromBurn::getItemInfo** with "TotalSpace" as the first parameter.</span></span> <span data-ttu-id="8c375-138">此函式所抓取的值是對應到光碟上的總位元組數的字串。</span><span class="sxs-lookup"><span data-stu-id="8c375-138">The value retrieved by this function is a string that corresponds to the total number of bytes on the disc.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="8c375-139">相關主題</span><span class="sxs-lookup"><span data-stu-id="8c375-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8c375-140">**燒錄 CD**</span><span class="sxs-lookup"><span data-stu-id="8c375-140">**Burning a CD**</span></span>](burning-a-cd.md)
</dt> <dt>

[<span data-ttu-id="8c375-141">**擷取 CD 燒錄介面**</span><span class="sxs-lookup"><span data-stu-id="8c375-141">**Retrieving the CD Burning Interface**</span></span>](retrieving-the-cd-burning-interface.md)
</dt> <dt>

[<span data-ttu-id="8c375-142">**啟動燒錄流程**</span><span class="sxs-lookup"><span data-stu-id="8c375-142">**Starting the Burn Process**</span></span>](starting-the-burn-process.md)
</dt> <dt>

[<span data-ttu-id="8c375-143">**清除可讀寫 CD**</span><span class="sxs-lookup"><span data-stu-id="8c375-143">**Erasing a Rewritable CD**</span></span>](erasing-a-rewritable-cd.md)
</dt> <dt>

[<span data-ttu-id="8c375-144">**正在抓取磁片磁碟機和光碟狀態**</span><span class="sxs-lookup"><span data-stu-id="8c375-144">**Retrieving the Drive and Disc Status**</span></span>](retrieving-the-drive-and-disc-status.md)
</dt> </dl>

 

 




