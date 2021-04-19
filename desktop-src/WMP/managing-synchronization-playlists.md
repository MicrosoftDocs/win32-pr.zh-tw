---
title: 管理同步播放清單
description: 管理同步播放清單
ms.assetid: 5891ada0-37a6-4256-9885-8aa9dbe98b7c
keywords:
- Windows Media Player，可攜式裝置
- Windows Media Player 物件模型，可攜式裝置
- 物件模型，可攜式裝置
- Windows Media Player 的 ActiveX 控制項、可攜式裝置
- ActiveX 控制項、可攜式裝置
- Windows Media Player Mobile ActiveX 控制項、可攜式裝置
- Windows Media Player Mobile、可攜式裝置
- 可攜式裝置，管理同步播放清單
- 裝置同步處理，播放清單
- 同步處理裝置、播放清單
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
- 同步播放清單，管理
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be0fe084918c0b69b827dbb941388246cbd177ee
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106968870"
---
# <a name="managing-synchronization-playlists"></a><span data-ttu-id="2d9f5-124">管理同步播放清單</span><span class="sxs-lookup"><span data-stu-id="2d9f5-124">Managing Synchronization Playlists</span></span>

<span data-ttu-id="2d9f5-125">Windows Media Player 10 或更新版本會使用播放清單來同步處理數位媒體檔案與可攜式裝置。</span><span class="sxs-lookup"><span data-stu-id="2d9f5-125">Windows Media Player 10 or later uses playlists to synchronize digital media files with portable devices.</span></span> <span data-ttu-id="2d9f5-126">本節說明如何使用同步播放清單。</span><span class="sxs-lookup"><span data-stu-id="2d9f5-126">This section explains how to work with synchronization playlists.</span></span>

<span data-ttu-id="2d9f5-127">本節中的範例程式碼會使用兩個 ListView 控制項來顯示資訊。</span><span class="sxs-lookup"><span data-stu-id="2d9f5-127">The example code in this section uses two ListView controls to display information.</span></span> <span data-ttu-id="2d9f5-128">第一個 ListView 控制項 (IDC \_ PLVIEW) 會顯示 Windows Media Player 文件庫中所有的播放清單，並先顯示同步播放清單。</span><span class="sxs-lookup"><span data-stu-id="2d9f5-128">The first ListView control (IDC\_PLVIEW) displays all of the playlists in the Windows Media Player library, with synchronization playlists appearing first.</span></span> <span data-ttu-id="2d9f5-129">目前所選裝置的同步播放清單會以核取記號標示，並以同步處理優先權順序排序。</span><span class="sxs-lookup"><span data-stu-id="2d9f5-129">Synchronization playlists for the currently selected device are marked with a check mark and are sorted in synchronization priority order.</span></span> <span data-ttu-id="2d9f5-130">所有其他播放清單都未核取。</span><span class="sxs-lookup"><span data-stu-id="2d9f5-130">All other playlists are unchecked.</span></span> <span data-ttu-id="2d9f5-131">ListView 控制項已設定為單一選取專案。</span><span class="sxs-lookup"><span data-stu-id="2d9f5-131">The ListView control was configured for single selection.</span></span> <span data-ttu-id="2d9f5-132">ListView 控制項中的播放清單順序決定了其同步處理優先權。</span><span class="sxs-lookup"><span data-stu-id="2d9f5-132">The order of playlists in the ListView control determines their synchronization priority.</span></span> <span data-ttu-id="2d9f5-133">個別播放清單的核取狀態會判斷它是否為目前所選裝置的同步播放清單。</span><span class="sxs-lookup"><span data-stu-id="2d9f5-133">The checked state of an individual playlist determines whether it is a synchronization playlist for the currently selected device.</span></span>

<span data-ttu-id="2d9f5-134">第二個 ListView 控制項 (IDC \_ MEDIAVIEW) 會顯示所選播放清單中的媒體專案。</span><span class="sxs-lookup"><span data-stu-id="2d9f5-134">The second ListView control (IDC\_MEDIAVIEW) displays the media items in the selected playlist.</span></span> <span data-ttu-id="2d9f5-135">有兩個額外的資料行會顯示文字，指出數位媒體檔案是否複製到裝置，並在發生失敗時，是否因為數位媒體檔案無法容納而導致複製失敗。</span><span class="sxs-lookup"><span data-stu-id="2d9f5-135">Two additional columns display text indicating whether the digital media file was copied to the device and, in the case of a failure, whether the copy failed because the digital media file did not fit.</span></span>

<span data-ttu-id="2d9f5-136">下列範例程式碼顯示如何初始化 ListView 控制項：</span><span class="sxs-lookup"><span data-stu-id="2d9f5-136">The following example code shows how the ListView controls are initialized:</span></span>


```C++
STDMETHODIMP CSyncSettings::InitListView()
{
    m_hPlView = GetDlgItem(IDC_PLVIEW);
    m_hMediaView = GetDlgItem(IDC_MEDIAVIEW); 

    ATLASSERT(m_hPlView);
    ATLASSERT(m_hMediaView);

    // Sync playlist information.
    // Selection highlights all rows.
    // Show checkboxes.
    ListView_SetExtendedListViewStyleEx(m_hPlView, 0, LVS_EX_CHECKBOXES | LVS_EX_FULLROWSELECT);
   
    // Add headers.
    LVCOLUMN lvc;
    ZeroMemory(&lvc, sizeof(LVCOLUMN));
    lvc.mask = LVCF_WIDTH | LVCF_TEXT | LVCF_SUBITEM; 
    lvc.iSubItem = 0;
    
    lvc.pszText = _T("Sync");
    lvc.cx = 40;
    ListView_InsertColumn(m_hPlView, lvc.iSubItem, &lvc);

    lvc.iSubItem++;
    lvc.pszText = _T("Playlist Name");
    lvc.cx = 300;
    ListView_InsertColumn(m_hPlView, lvc.iSubItem, &lvc); 

    // Media information.
    // Selection highlights all rows.
    ListView_SetExtendedListViewStyleEx(m_hMediaView, 0, LVS_EX_FULLROWSELECT);

    // Add headers
    ZeroMemory(&lvc, sizeof(LVCOLUMN));
    lvc.mask = LVCF_WIDTH | LVCF_TEXT | LVCF_SUBITEM; 
    lvc.iSubItem = 0;
    
    lvc.pszText = _T("Media name");
    lvc.cx = 150;
    ListView_InsertColumn(m_hMediaView, lvc.iSubItem, &lvc);

    lvc.iSubItem++;
    lvc.pszText = _T("On Device");
    lvc.cx = 69;
    ListView_InsertColumn(m_hMediaView, lvc.iSubItem, &lvc);  

    lvc.iSubItem++;
    lvc.pszText = _T("Fit?");
    lvc.cx = 40;
    ListView_InsertColumn(m_hMediaView, lvc.iSubItem, &lvc);  
   
    return S_OK;
}
```



<span data-ttu-id="2d9f5-137">下列字串陣列包含範例中所使用之同步處理屬性的名稱：</span><span class="sxs-lookup"><span data-stu-id="2d9f5-137">The following array of strings contains the names of the synchronization attributes used in the examples:</span></span>


```C++
static const TCHAR *g_szSyncAttributeNames[17] = {
        _T("Not used"), // Do not access this one.
        _T("Sync01"),
        _T("Sync02"),
        _T("Sync03"),
        _T("Sync04"),
        _T("Sync05"),
        _T("Sync06"),
        _T("Sync07"),
        _T("Sync08"),
        _T("Sync09"),
        _T("Sync10"),
        _T("Sync11"),
        _T("Sync12"),
        _T("Sync13"),
        _T("Sync14"),
        _T("Sync15"),
        _T("Sync16")};
```



<span data-ttu-id="2d9f5-138">下列成員變數包含包含 Windows Media Player 文件庫中所有播放清單的播放清單。</span><span class="sxs-lookup"><span data-stu-id="2d9f5-138">The following member variable contains a playlist containing all playlists in the Windows Media Player library.</span></span> <span data-ttu-id="2d9f5-139">每個播放清單都會以媒體專案表示。</span><span class="sxs-lookup"><span data-stu-id="2d9f5-139">Each playlist is represented as a media item.</span></span>


```C++
CComPtr<IWMPPlaylist> m_spPlaylist;
```



<span data-ttu-id="2d9f5-140">下列各節提供範例程式碼：</span><span class="sxs-lookup"><span data-stu-id="2d9f5-140">The following sections provide example code:</span></span>

-   [<span data-ttu-id="2d9f5-141">列舉同步播放清單</span><span class="sxs-lookup"><span data-stu-id="2d9f5-141">Enumerating Synchronization Playlists</span></span>](enumerating-synchronization-playlists.md)
-   [<span data-ttu-id="2d9f5-142">依同步處理優先順序排序播放清單</span><span class="sxs-lookup"><span data-stu-id="2d9f5-142">Sorting Playlists by Synchronization Priority</span></span>](sorting-playlists-by-synchronization-priority.md)
-   [<span data-ttu-id="2d9f5-143">列舉媒體專案</span><span class="sxs-lookup"><span data-stu-id="2d9f5-143">Enumerating the Media Items</span></span>](enumerating-the-media-items.md)
-   [<span data-ttu-id="2d9f5-144">判斷播放清單同步處理狀態</span><span class="sxs-lookup"><span data-stu-id="2d9f5-144">Determining Playlist Synchronization State</span></span>](determining-playlist-synchronization-state.md)
-   [<span data-ttu-id="2d9f5-145">變更同步處理優先權</span><span class="sxs-lookup"><span data-stu-id="2d9f5-145">Changing Synchronization Priority</span></span>](changing-synchronization-priority.md)

## <a name="related-topics"></a><span data-ttu-id="2d9f5-146">相關主題</span><span class="sxs-lookup"><span data-stu-id="2d9f5-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2d9f5-147">**使用可攜式裝置**</span><span class="sxs-lookup"><span data-stu-id="2d9f5-147">**Working with Portable Devices**</span></span>](working-with-portable-devices.md)
</dt> </dl>

 

 




