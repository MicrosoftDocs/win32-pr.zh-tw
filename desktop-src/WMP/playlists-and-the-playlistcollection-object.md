---
title: 播放清單和 PlaylistCollection 物件
description: 播放清單和 PlaylistCollection 物件
ms.assetid: 63c8955b-34ad-447b-b734-657207bcecbb
keywords:
- Windows Media Player，播放清單
- Windows Media Player 物件模型，播放清單
- 物件模型，播放清單
- Windows Media Player 行動裝置、播放清單
- Windows Media Player ActiveX 控制項，播放清單
- Windows Media Player 的行動 ActiveX 控制項、播放清單
- ActiveX 控制項，播放清單
- 播放清單，PlaylistCollection 物件
- 中繼檔播放清單，PlaylistCollection 物件
- Windows Media 中繼檔播放清單，PlaylistCollection 物件
- PlaylistCollection 物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98744c2c5b97129db2824c42567802a374f90b6c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106968834"
---
# <a name="playlists-and-the-playlistcollection-object"></a><span data-ttu-id="d91e6-114">播放清單和 PlaylistCollection 物件</span><span class="sxs-lookup"><span data-stu-id="d91e6-114">Playlists and the PlaylistCollection Object</span></span>

<span data-ttu-id="d91e6-115">**PlaylistCollection** 物件可讓您存取媒體櫃中的播放清單，並提供從中繼檔建立新的空白播放清單和新播放清單的方法。</span><span class="sxs-lookup"><span data-stu-id="d91e6-115">The **PlaylistCollection** object gives you access to playlists in the library and has methods for creating new, empty playlists and new playlists from metafiles.</span></span>

## <a name="working-with-existing-playlists"></a><span data-ttu-id="d91e6-116">使用現有的播放清單</span><span class="sxs-lookup"><span data-stu-id="d91e6-116">Working with Existing Playlists</span></span>

<span data-ttu-id="d91e6-117">*PlaylistCollection*。**getAll** 和 *PlaylistCollection*。**getByName** 方法都會傳回 **PlaylistArray** 物件，其中可能包含多個播放清單。</span><span class="sxs-lookup"><span data-stu-id="d91e6-117">The *PlaylistCollection*.**getAll** and *PlaylistCollection*.**getByName** methods each return a **PlaylistArray** object, which can contain multiple playlists.</span></span>

<span data-ttu-id="d91e6-118">*PlaylistCollection*。**getAll** 方法會傳回程式庫中所有現有的播放清單。</span><span class="sxs-lookup"><span data-stu-id="d91e6-118">The *PlaylistCollection*.**getAll** method returns all of the existing playlists that are in the library.</span></span> <span data-ttu-id="d91e6-119">例如，您可以呼叫這個方法，然後取出 **PlaylistArray** 物件中的播放清單，以判斷是否已使用指定的播放清單名稱，或將所有的播放清單顯示給使用者。</span><span class="sxs-lookup"><span data-stu-id="d91e6-119">For example, you can call this method and then retrieve the playlists in the **PlaylistArray** object to determine whether a given playlist name has already been used, or to display all of the playlists to the user.</span></span> <span data-ttu-id="d91e6-120">[播放清單屬性](playlist-attributes.md)中的範例程式碼會使用 **getAll** 方法。</span><span class="sxs-lookup"><span data-stu-id="d91e6-120">The sample code in [Playlist Attributes](playlist-attributes.md) uses the **getAll** method.</span></span>

<span data-ttu-id="d91e6-121">*PlaylistCollection*。**getByName** 方法會傳回具有指定名稱的所有播放清單。</span><span class="sxs-lookup"><span data-stu-id="d91e6-121">The *PlaylistCollection*.**getByName** method returns all of the playlists with a given name.</span></span> <span data-ttu-id="d91e6-122">您可以使用這個方法，分別處理每個播放清單。</span><span class="sxs-lookup"><span data-stu-id="d91e6-122">You can use this method to handle each of those playlists separately.</span></span>

<span data-ttu-id="d91e6-123">您也可以使用 **getByName** 方法，依名稱抓取唯一的播放清單。</span><span class="sxs-lookup"><span data-stu-id="d91e6-123">You can also use the **getByName** method to retrieve a unique playlist by name.</span></span> <span data-ttu-id="d91e6-124">在此情況下， **PlaylistArray** 物件只有一個元素。</span><span class="sxs-lookup"><span data-stu-id="d91e6-124">In that case, the **PlaylistArray** object has only one element.</span></span> <span data-ttu-id="d91e6-125">下列 c # 範例示範這項技巧。</span><span class="sxs-lookup"><span data-stu-id="d91e6-125">The following C# example demonstrates this technique.</span></span>


```C++
IWMPPlaylistArray PlayListArray;
IWMPPlaylist Playlist;
// Store the playlist named "BluesTest" in the array
PlayListArray = Player.playlistCollection.getByName("BluesTest");
// Retrieve the first playlist in the collection.
Playlist = PlaylistArray.Item(0);

```



## <a name="working-with-new-playlists"></a><span data-ttu-id="d91e6-126">使用新的播放清單</span><span class="sxs-lookup"><span data-stu-id="d91e6-126">Working with New Playlists</span></span>

<span data-ttu-id="d91e6-127">您可以使用 *PlaylistCollection*。用來建立新的空白播放清單的 **[]** 方法。</span><span class="sxs-lookup"><span data-stu-id="d91e6-127">You can use the *PlaylistCollection*.**newPlaylist** method to create a new, empty playlist.</span></span> <span data-ttu-id="d91e6-128">方法會傳回新 **播放清單** 物件的參考。</span><span class="sxs-lookup"><span data-stu-id="d91e6-128">The method returns a reference to the new **Playlist** object.</span></span> <span data-ttu-id="d91e6-129">然後您就可以呼叫 *播放清單*。將媒體專案新增至播放清單的 **appendItem** 方法。</span><span class="sxs-lookup"><span data-stu-id="d91e6-129">You can then call the *Playlist*.**appendItem** method to add media items to the playlist.</span></span>

<span data-ttu-id="d91e6-130">您也可以根據播放清單中繼檔建立新的播放清單。</span><span class="sxs-lookup"><span data-stu-id="d91e6-130">You can also create a new playlist based on a playlist metafile.</span></span> <span data-ttu-id="d91e6-131">首先，將播放清單的名稱和中繼檔的路徑傳遞給 *播放機*。**[]** 方法。</span><span class="sxs-lookup"><span data-stu-id="d91e6-131">First, pass the name of the playlist and the path to the metafile to the *Player*.**newPlaylist** method.</span></span> <span data-ttu-id="d91e6-132">該方法會傳回新 **播放清單** 物件的參考。</span><span class="sxs-lookup"><span data-stu-id="d91e6-132">That method returns a reference to the new **Playlist** object.</span></span> <span data-ttu-id="d91e6-133">然後，將新的 **播放清單** 物件傳遞給 *PlaylistCollection*。**importPlaylist** 方法，將它新增至程式庫。</span><span class="sxs-lookup"><span data-stu-id="d91e6-133">Then, pass the new **Playlist** object to the *PlaylistCollection*.**importPlaylist** method to add it to the library.</span></span>

<span data-ttu-id="d91e6-134">請注意 *PlaylistCollection* 之間的差異。**[]** 方法和 *播放機*。**[]** 方法。</span><span class="sxs-lookup"><span data-stu-id="d91e6-134">Notice the difference between the *PlaylistCollection*.**newPlaylist** method and the *Player*.**newPlaylist** method.</span></span> <span data-ttu-id="d91e6-135">**PlaylistCollection** 方法會建立新的空白播放清單，並將其新增至程式庫。</span><span class="sxs-lookup"><span data-stu-id="d91e6-135">The **PlaylistCollection** method creates a new, empty playlist and adds it to the library.</span></span> <span data-ttu-id="d91e6-136">**Player** 方法會建立新填入的 **播放清單** 物件，但不會將它新增至程式庫。</span><span class="sxs-lookup"><span data-stu-id="d91e6-136">The **Player** method creates a new, populated **Playlist** object but does not add it to the library.</span></span>

<span data-ttu-id="d91e6-137">在本主題中， **Player** 物件是以下列方式定義：</span><span class="sxs-lookup"><span data-stu-id="d91e6-137">Throughout this topic, the **Player** object was defined in the following manner:</span></span>


```C++
AxWMPLib.AxWindowsMediaPlayer Player;
using WMPLib;

```



<span data-ttu-id="d91e6-138">下列 c # 範例示範如何從中繼檔匯入播放清單。</span><span class="sxs-lookup"><span data-stu-id="d91e6-138">The following C# example demonstrates importing a playlist from a metafile.</span></span> <span data-ttu-id="d91e6-139">*StrPListName* 引數指定新播放清單的名稱。</span><span class="sxs-lookup"><span data-stu-id="d91e6-139">The *strPListName* argument specifies the name of the new playlist.</span></span> <span data-ttu-id="d91e6-140">*StrMetaFileName* 會指定要匯入播放清單的中繼檔名稱。</span><span class="sxs-lookup"><span data-stu-id="d91e6-140">The *strMetaFileName* specifies the name of the metafile from which the playlist is imported.</span></span>


```C++
private IWMPPlaylist importPlaylist(string strPlaylistName, string strMetaFileName)
{
    IWMPPlaylist  NewPlaylist;
    IWMPPlaylist  ImportPlaylist;

    NewPlaylist = Player.newPlaylist(strPlaylistName, strMetaFileName);
    ImportPlaylist = Player.playlistCollection.importPlaylist(NewPlaylist);

    return ImportPlaylist;
}

```



## <a name="related-topics"></a><span data-ttu-id="d91e6-141">相關主題</span><span class="sxs-lookup"><span data-stu-id="d91e6-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d91e6-142">**管理播放清單**</span><span class="sxs-lookup"><span data-stu-id="d91e6-142">**Managing Playlists**</span></span>](managing-playlists.md)
</dt> <dt>

<span data-ttu-id="d91e6-143">[**[]**](player-newplaylist.md)</span><span class="sxs-lookup"><span data-stu-id="d91e6-143">[**Player.newPlaylist**](player-newplaylist.md)</span></span>
</dt> <dt>

[<span data-ttu-id="d91e6-144">**播放清單。 appendItem**</span><span class="sxs-lookup"><span data-stu-id="d91e6-144">**Playlist.appendItem**</span></span>](playlist-appenditem.md)
</dt> <dt>

[<span data-ttu-id="d91e6-145">**PlaylistArray 物件**</span><span class="sxs-lookup"><span data-stu-id="d91e6-145">**PlaylistArray Object**</span></span>](playlistarray-object.md)
</dt> <dt>

[<span data-ttu-id="d91e6-146">**PlaylistCollection 物件**</span><span class="sxs-lookup"><span data-stu-id="d91e6-146">**PlaylistCollection Object**</span></span>](playlistcollection-object.md)
</dt> <dt>

[<span data-ttu-id="d91e6-147">**播放清單和媒體專案**</span><span class="sxs-lookup"><span data-stu-id="d91e6-147">**Playlists and Media Items**</span></span>](playlists-and-media-items.md)
</dt> </dl>

 

 




