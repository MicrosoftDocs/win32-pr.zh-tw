---
title: 列舉同步播放清單
description: 列舉同步播放清單
ms.assetid: 830c3ea5-2937-48b5-b89f-ef68a6649ca3
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
- 同步播放清單，列舉
- 可攜式裝置，列舉
- 列舉，同步播放清單
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29679380cec1844e9a790ac4ff047bfa4bf05288
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "106969691"
---
# <a name="enumerating-synchronization-playlists"></a><span data-ttu-id="81126-116">列舉同步播放清單</span><span class="sxs-lookup"><span data-stu-id="81126-116">Enumerating Synchronization Playlists</span></span>

<span data-ttu-id="81126-117">下列程式碼範例會建立一個函式，該函式會使用播放清單來填滿 ListView 控制項。</span><span class="sxs-lookup"><span data-stu-id="81126-117">The following example code creates a function that fills a ListView control with playlists.</span></span> <span data-ttu-id="81126-118">同步播放清單會先出現。</span><span class="sxs-lookup"><span data-stu-id="81126-118">Synchronization playlists appear first.</span></span> <span data-ttu-id="81126-119">目前所選裝置的同步播放清單會以核取記號標示，並以同步處理優先權順序排序。</span><span class="sxs-lookup"><span data-stu-id="81126-119">Synchronization playlists for the currently selected device are marked with a check mark and are sorted in synchronization priority order.</span></span> <span data-ttu-id="81126-120">所有其他播放清單都未核取。</span><span class="sxs-lookup"><span data-stu-id="81126-120">All other playlists are unchecked.</span></span>

<span data-ttu-id="81126-121">ListView 控制項已設定為單一選取專案。</span><span class="sxs-lookup"><span data-stu-id="81126-121">The ListView control was configured for single selection.</span></span> <span data-ttu-id="81126-122">ListView 控制項中的播放清單順序決定了其同步處理優先權。</span><span class="sxs-lookup"><span data-stu-id="81126-122">The order of playlists in the ListView control determines their synchronization priority.</span></span> <span data-ttu-id="81126-123">個別播放清單的核取狀態會判斷它是否為目前所選裝置的同步播放清單。</span><span class="sxs-lookup"><span data-stu-id="81126-123">The checked state of an individual playlist determines whether it is a synchronization playlist for the currently selected device.</span></span>

<span data-ttu-id="81126-124">參數 *lPSIndex* 為目前選取的可攜式裝置指定合作關係索引。</span><span class="sxs-lookup"><span data-stu-id="81126-124">The parameter *lPSIndex* specifies the partnership index for the currently selected portable device.</span></span>


```C++
STDMETHODIMP CSyncSettings::ShowPlaylists(long lPSIndex)
{ 
    HRESULT hr = S_OK; 
    ATLASSERT(m_pMainDlg);
   
    CComPtr<IWMPMediaCollection> spMediaCollection;
    CComPtr<IWMPPlaylist> spPlaylist; // Contains a playlist of all playlists.
    long lSyncItemCount= 0; // Count of items selected for synchronization. 

    ListView_DeleteAllItems(m_hPlView);

    m_spPlaylist.Release();
   
    if(lPSIndex == 0)
    {
        return S_OK;
    } 

    HCURSOR hCursor = LoadCursor(NULL, IDC_WAIT);
    HCURSOR hCursorOld = SetCursor(hCursor);

    if(SUCCEEDED(hr))
    {
        // Retrieve a pointer to IWMPMediaCollection.
        hr = m_spPlayer->get_mediaCollection(&spMediaCollection);
    }

    if(SUCCEEDED(hr) && spMediaCollection)
    {
        // Retrieve a playlist filled with IWMPMedia items.
        // Each IWMPMedia represents an individual playlist 
        // in the library.
        hr = spMediaCollection->getByAttribute(CComBSTR("MediaType"), CComBSTR("playlist"), &spPlaylist);
    }
 
    if(SUCCEEDED(hr) && spPlaylist)
    {  
        // Get the sync attribute name for the current device.
        CComBSTR bstrAttribute(g_szSyncAttributeNames[lPSIndex]);

        // Sort the playlist.
        // lSyncItemCount is the count of synchronization playlists.
        hr = SortPlaylist(spPlaylist, bstrAttribute, &lSyncItemCount);
     
        if(SUCCEEDED(hr))
        {
            m_spPlaylist = spPlaylist;  // Cache the playlist.

            long lCount = 0;
            spPlaylist->get_count(&lCount);
             
            // Fill the ListView control.
            for(long i = 0; i < lCount; i++)
            {
                CComPtr<IWMPMedia> spMedia;
                CComBSTR bstrPlaylistName;
                CComBSTR bstrVal; // Value of the SyncXX attribute.

                // Retrieve a playlist.
                hr = spPlaylist->get_item(i, &spMedia);

                if(SUCCEEDED(hr) && spMedia)
                {
                    // Get the name.
                    hr = spMedia->get_name(&bstrPlaylistName);
                }  
                if(SUCCEEDED(hr) && spMedia)
                {      
                    // Get the SyncXX attribute value.
                    hr = spMedia->getItemInfo(bstrAttribute, &bstrVal);
                }

                if(SUCCEEDED(hr) && bstrPlaylistName.Length())
                {
                    // Insert the item in the ListView control.
                    LVITEM lvI;
                    ZeroMemory(&lvI, sizeof(LVITEM));
                    lvI.mask = LVIF_TEXT; 
                    lvI.lParam = _wtol(bstrVal);
                    lvI.iItem = ListView_GetItemCount(m_hPlView);
                    lvI.pszText = "";
                    ListView_InsertItem(m_hPlView, &lvI);

                    // If this is a sync playlist, mark the check box.
                    if(i < lSyncItemCount)
                    {
                        ListView_SetCheckState(m_hPlView, i, TRUE);
                    }

                    // Display the playlist name.
                    lvI.iSubItem = 1;
                    lvI.pszText = COLE2T(bstrPlaylistName);
                    ListView_SetItem(m_hPlView, &lvI);
                }
            }
        }        
    }

    SetCursor(hCursorOld);
    return hr;
}
```



<span data-ttu-id="81126-125">如需 SortPlaylist 函式的執行，請參閱 [依同步處理優先權排序播放清單](sorting-playlists-by-synchronization-priority.md)。</span><span class="sxs-lookup"><span data-stu-id="81126-125">For the implementation of the SortPlaylist function, see [Sorting Playlists by Synchronization Priority](sorting-playlists-by-synchronization-priority.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="81126-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="81126-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="81126-127">**IWMPMedia：： getItemInfo**</span><span class="sxs-lookup"><span data-stu-id="81126-127">**IWMPMedia::getItemInfo**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia-getiteminfo)
</dt> <dt>

[<span data-ttu-id="81126-128">**IWMPMediaCollection::getByAttribute**</span><span class="sxs-lookup"><span data-stu-id="81126-128">**IWMPMediaCollection::getByAttribute**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmediacollection-getbyattribute)
</dt> <dt>

[<span data-ttu-id="81126-129">**管理同步播放清單**</span><span class="sxs-lookup"><span data-stu-id="81126-129">**Managing Synchronization Playlists**</span></span>](managing-synchronization-playlists.md)
</dt> <dt>

[<span data-ttu-id="81126-130">**同步屬性**</span><span class="sxs-lookup"><span data-stu-id="81126-130">**Sync Attributes**</span></span>](sync-attributes.md)
</dt> </dl>

 

 




