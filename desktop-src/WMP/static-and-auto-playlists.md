---
title: 靜態和自動播放清單
description: 靜態和自動播放清單
ms.assetid: 708c236e-8f3c-4188-aefb-eda7da598944
keywords:
- Windows Media Player，播放清單
- Windows Media Player 物件模型，播放清單
- 物件模型，播放清單
- Windows Media Player 行動裝置、播放清單
- Windows Media Player ActiveX 控制項，播放清單
- Windows Media Player 的行動 ActiveX 控制項、播放清單
- ActiveX 控制項，播放清單
- 播放清單、靜態
- 中繼檔播放清單，靜態
- Windows Media 中繼檔播放清單、靜態
- 靜態播放清單
- 自動播放清單
- 播放清單、自動
- 中繼檔播放清單，自動
- Windows Media 中繼檔播放清單，自動
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 083ee2029eec2cfee7510766790f4ca7eb6468e5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104371935"
---
# <a name="static-and-auto-playlists"></a><span data-ttu-id="03c00-118">靜態和自動播放清單</span><span class="sxs-lookup"><span data-stu-id="03c00-118">Static and Auto Playlists</span></span>

<span data-ttu-id="03c00-119">有兩種類型的播放清單：</span><span class="sxs-lookup"><span data-stu-id="03c00-119">There are two types of playlists:</span></span>

-   <span data-ttu-id="03c00-120">包含特定媒體專案的靜態播放清單</span><span class="sxs-lookup"><span data-stu-id="03c00-120">Static playlists, which include specific media items</span></span>
-   <span data-ttu-id="03c00-121">自動播放清單，會在每次開啟程式庫時搜尋程式庫，而且可能會在不同的時間包含不同的媒體專案。</span><span class="sxs-lookup"><span data-stu-id="03c00-121">Auto playlists, which search the library every time they are opened and may contain different media items at different times.</span></span> <span data-ttu-id="03c00-122">自動播放清單是資料庫查詢的結果。</span><span class="sxs-lookup"><span data-stu-id="03c00-122">An auto playlist is the result of a database query.</span></span>

<span data-ttu-id="03c00-123">若要從中繼檔匯入靜態播放清單，請先呼叫 *Player*。**[]** 根據中繼檔中的資料建立 **播放清單** 物件，然後將該物件傳遞至 *PlaylistCollection*。**importPlaylist** ，將播放清單新增至程式庫。</span><span class="sxs-lookup"><span data-stu-id="03c00-123">To import a static playlist from a metafile, first call *Player*.**newPlaylist** to create a **Playlist** object based on the data in the metafile, and then pass that object to *PlaylistCollection*.**importPlaylist** to add the playlist to the library.</span></span>

<span data-ttu-id="03c00-124">若要從中繼檔匯入自動播放清單，請使用 *MediaCollection*。**加入**。</span><span class="sxs-lookup"><span data-stu-id="03c00-124">To import an auto playlist from a metafile, use *MediaCollection*.**add**.</span></span> <span data-ttu-id="03c00-125">如需詳細資訊，請參閱 [播放清單和 MediaCollection 物件](playlists-and-the-mediacollection-object.md)。</span><span class="sxs-lookup"><span data-stu-id="03c00-125">For more information, see [Playlists and the MediaCollection Object](playlists-and-the-mediacollection-object.md).</span></span>

<span data-ttu-id="03c00-126">若要從自動播放清單中繼檔匯入靜態播放清單，請使用 *Player*。**[]** 和 *PlaylistCollection*。如先前所述 **importPlaylist** 。</span><span class="sxs-lookup"><span data-stu-id="03c00-126">To import a static playlist from an auto playlist metafile, use *Player*.**newPlaylist** and *PlaylistCollection*.**importPlaylist** as described earlier.</span></span> <span data-ttu-id="03c00-127">自動播放清單會執行一次，而且會根據該執行的結果來建立靜態播放清單。</span><span class="sxs-lookup"><span data-stu-id="03c00-127">The auto playlist will be executed once and a static playlist will be created based on the result of that execution.</span></span>

<span data-ttu-id="03c00-128">使用者透過網際網路存取的網頁不支援使用自動播放清單來查詢使用者的程式庫。</span><span class="sxs-lookup"><span data-stu-id="03c00-128">Using an auto playlist to query the user's library is not supported for webpages that users access over the Internet.</span></span>

<span data-ttu-id="03c00-129">下列 c # 範例程式碼示範如何將自動播放清單中繼檔匯入為靜態播放清單。</span><span class="sxs-lookup"><span data-stu-id="03c00-129">The following C# example code demonstrates importing an auto playlist metafile as a static playlist.</span></span> <span data-ttu-id="03c00-130">若要執行此範例，請使用程式庫使用者介面建立自動播放清單，然後在此程式碼中包含自動播放清單中繼檔的正確路徑。</span><span class="sxs-lookup"><span data-stu-id="03c00-130">To run this sample, create an auto playlist by using the library user interface, and then include the correct path to the auto playlist metafile in this code.</span></span>


```C++
private void addStaticPlaylist()
{
    IWMPPlaylist pList;

    pList = Player.newPlaylist("NewImportedList", "\\\\myServer\\myPath\\artistcollection.wpl");
    if (pList.count == 0)
        MessageBox.Show("The specified playlist is empty.");
    else
        Player.playlistCollection.importPlaylist(pList);
}

```



## <a name="related-topics"></a><span data-ttu-id="03c00-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="03c00-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="03c00-132">**管理播放清單**</span><span class="sxs-lookup"><span data-stu-id="03c00-132">**Managing Playlists**</span></span>](managing-playlists.md)
</dt> </dl>

 

 




