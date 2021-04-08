---
title: 依同步處理優先順序排序播放清單
description: 依同步處理優先順序排序播放清單
ms.assetid: 0f7f1ed3-0639-47bf-bf8e-52ae0a1d7ab2
keywords:
- Windows Media Player，同步播放清單
- Windows Media Player 物件模型，同步播放清單
- 物件模型，同步處理播放清單
- Windows Media Player 行動裝置、同步播放清單
- Windows Media Player ActiveX 控制項，同步播放清單
- Windows Media Player 的行動 ActiveX 控制項、同步播放清單
- ActiveX 控制項，同步播放清單
- 播放清單，同步處理
- 中繼檔播放清單，同步處理
- Windows Media 中繼檔播放清單，同步處理
- 可攜式裝置，排序同步播放清單
- 同步播放清單，排序
- 同步播放清單，優先順序
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90624e8e1cab715e8a26e33f40a444d53ab35def
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "103841904"
---
# <a name="sorting-playlists-by-synchronization-priority"></a><span data-ttu-id="ace0d-116">依同步處理優先順序排序播放清單</span><span class="sxs-lookup"><span data-stu-id="ace0d-116">Sorting Playlists by Synchronization Priority</span></span>

<span data-ttu-id="ace0d-117">下列程式碼會執行簡單排序的播放清單。</span><span class="sxs-lookup"><span data-stu-id="ace0d-117">The following code performs a simple sort of playlists.</span></span> <span data-ttu-id="ace0d-118">您可以在 [列舉同步播放清單](enumerating-synchronization-playlists.md)的範例程式碼中，看到此函式的使用方式。</span><span class="sxs-lookup"><span data-stu-id="ace0d-118">You can see how this function is used in the example code in [Enumerating Synchronization Playlists](enumerating-synchronization-playlists.md).</span></span> <span data-ttu-id="ace0d-119">函數會採用下列參數：</span><span class="sxs-lookup"><span data-stu-id="ace0d-119">The function takes the following parameters:</span></span>

-   <span data-ttu-id="ace0d-120">*pPlaylist*。</span><span class="sxs-lookup"><span data-stu-id="ace0d-120">*pPlaylist*.</span></span> <span data-ttu-id="ace0d-121">要排序之 Windows Media Player 播放清單的指標。</span><span class="sxs-lookup"><span data-stu-id="ace0d-121">The pointer to the Windows Media Player playlist to sort.</span></span> <span data-ttu-id="ace0d-122">播放清單中的媒體專案必須指向其他播放清單，而不是個別的數位媒體檔案。</span><span class="sxs-lookup"><span data-stu-id="ace0d-122">The media items in the playlist must point to other playlists, not individual digital media files.</span></span>
-   <span data-ttu-id="ace0d-123">*bstrSyncAttribute*。</span><span class="sxs-lookup"><span data-stu-id="ace0d-123">*bstrSyncAttribute*.</span></span> <span data-ttu-id="ace0d-124">包含目前裝置之同步合作關係屬性名稱的 BSTR ( "Sync01"、"Sync02" 等等) 。</span><span class="sxs-lookup"><span data-stu-id="ace0d-124">A BSTR containing the name of the synchronization partnership attribute for the current device ("Sync01", "Sync02", and so on).</span></span>
-   <span data-ttu-id="ace0d-125">*plSelected*。</span><span class="sxs-lookup"><span data-stu-id="ace0d-125">*plSelected*.</span></span> <span data-ttu-id="ace0d-126">**長** 變數的指標，此變數會接收同步播放清單的計數。</span><span class="sxs-lookup"><span data-stu-id="ace0d-126">Pointer to a **long** variable that receives the count of synchronization playlists.</span></span>

<span data-ttu-id="ace0d-127">此函式會檢查每個媒體專案的同步合作關係屬性 (代表 *pPlaylist* 所指定播放清單中的播放清單) 。</span><span class="sxs-lookup"><span data-stu-id="ace0d-127">The function inspects the synchronization partnership attribute for each media item (representing a playlist) in the playlist specified by *pPlaylist*.</span></span> <span data-ttu-id="ace0d-128">如果屬性具有非零值，則程式碼會將媒體專案移至播放清單的開頭，並依優先權順序插入。</span><span class="sxs-lookup"><span data-stu-id="ace0d-128">If the attribute has a nonzero value, the code moves the media item to the beginning of the playlist and inserts it in priority order.</span></span>

<span data-ttu-id="ace0d-129">完成時，此函式會傳回 (同步處理的播放清單) 之媒體專案的計數，這是同步合作關係屬性的非零值。</span><span class="sxs-lookup"><span data-stu-id="ace0d-129">When finished, the function returns the count of media items (synchronization playlists) that had a nonzero value for the synchronization partnership attribute.</span></span>


```C++
STDMETHODIMP CSyncSettings::SortPlaylist(IWMPPlaylist *pPlaylist, BSTR bstrSyncAttribute, long *plSelected)
{
    HRESULT hr = S_OK;
    long lSyncItemCount = 0;

    ATLASSERT (pPlaylist);
    ATLASSERT (plSelected);

    // Local copies of the parameters.
    CComPtr<IWMPPlaylist> spPlaylist(pPlaylist);
    CComBSTR bstrAttribute(bstrSyncAttribute);

    ATLASSERT (bstrAttribute.Length());

    // Get the count of playlist media items.
    long lCount = 0;
    spPlaylist->get_count(&lCount);

    // Walk the playlist.
    for(long i = 0; i < lCount; i++)
    {
        CComPtr<IWMPMedia> spMedia;                 
        CComBSTR bstrVal;            
        long lPriority = 0;
        
        hr = spPlaylist->get_item(i, &spMedia);

        if(SUCCEEDED(hr) && spMedia)
        {      
            // Get the sync priority value as a string.
            hr = spMedia->getItemInfo(bstrAttribute, &bstrVal);
        }

        if(SUCCEEDED(hr) && spMedia)
        {
            // Convert sync priority to a long number.
            lPriority = _wtol(bstrVal);
        }

        // Sort the playlist.
        // Only move the current item if it has a
        // sync priority value.
        if(lPriority > 0)
        {
            lSyncItemCount++;

            // Walk down the list and insert the item
            // in ascending order.
            for(long j = 0; j < lCount; j++)
            {
                CComPtr<IWMPMedia> spMediaCompare;
                CComBSTR bstrValCompare;
                long lPriorityTest = 0;

                hr = spPlaylist->get_item(j, &spMediaCompare);

                if(SUCCEEDED(hr) && spMediaCompare.p)
                {
                    hr = spMediaCompare->getItemInfo(bstrAttribute, &bstrValCompare);
                }
                if(SUCCEEDED(hr) && spMediaCompare.p)
                {
                    lPriorityTest = _wtol(bstrValCompare);
                    
                    if(lPriority <= lPriorityTest || 
                        0 == lPriorityTest)
                    {
                        hr = spPlaylist->moveItem(i, j);
                        break;                            
                    }                        
                } 
            } // for j                       
        } // if(lPriority > 0)          
    } // for i  
  
    // Return the sync item count.
    *plSelected = lSyncItemCount;

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="ace0d-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="ace0d-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ace0d-131">**IWMPMedia：： getItemInfo**</span><span class="sxs-lookup"><span data-stu-id="ace0d-131">**IWMPMedia::getItemInfo**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia-getiteminfo)
</dt> <dt>

[<span data-ttu-id="ace0d-132">**IWMPPlaylist：： get \_ 專案**</span><span class="sxs-lookup"><span data-stu-id="ace0d-132">**IWMPPlaylist::get\_item**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplaylist-get_item)
</dt> <dt>

[<span data-ttu-id="ace0d-133">**IWMPPlaylist：： moveItem**</span><span class="sxs-lookup"><span data-stu-id="ace0d-133">**IWMPPlaylist::moveItem**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplaylist-moveitem)
</dt> <dt>

[<span data-ttu-id="ace0d-134">**管理同步播放清單**</span><span class="sxs-lookup"><span data-stu-id="ace0d-134">**Managing Synchronization Playlists**</span></span>](managing-synchronization-playlists.md)
</dt> <dt>

[<span data-ttu-id="ace0d-135">**同步屬性**</span><span class="sxs-lookup"><span data-stu-id="ace0d-135">**Sync Attributes**</span></span>](sync-attributes.md)
</dt> </dl>

 

 




