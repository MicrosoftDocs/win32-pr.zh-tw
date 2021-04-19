---
title: 關於播放清單、PlaylistCollection 和 PlaylistArray 物件
description: 關於播放清單、PlaylistCollection 和 PlaylistArray 物件
ms.assetid: 19867944-c836-4b7e-ada3-f696905e6327
keywords:
- Windows Media Player，播放清單物件
- Windows Media Player 物件模型、播放清單物件
- 物件模型、播放清單物件
- Windows Media Player ActiveX 控制項、播放清單物件
- ActiveX 控制項、播放清單物件
- Windows Media Player 行動 ActiveX 控制項、播放清單物件
- Windows Media Player Mobile，播放清單物件
- 播放清單物件
- Windows Media Player，PlaylistCollection 物件
- Windows Media Player 物件模型，PlaylistCollection 物件
- 物件模型，PlaylistCollection 物件
- Windows Media Player ActiveX 控制項，PlaylistCollection 物件
- ActiveX 控制項，PlaylistCollection 物件
- Windows Media Player 行動 ActiveX 控制項，PlaylistCollection 物件
- Windows Media Player Mobile，PlaylistCollection 物件
- PlaylistCollection 物件
- Windows Media Player，PlaylistArray 物件
- Windows Media Player 物件模型，PlaylistArray 物件
- 物件模型，PlaylistArray 物件
- Windows Media Player ActiveX 控制項，PlaylistArray 物件
- ActiveX 控制項，PlaylistArray 物件
- Windows Media Player 行動 ActiveX 控制項，PlaylistArray 物件
- Windows Media Player Mobile，PlaylistArray 物件
- PlaylistArray 物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ee9d24f4f5decc28a369e44910990ff41b99e9e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106984505"
---
# <a name="about-the-playlist-playlistcollection-and-playlistarray-objects"></a><span data-ttu-id="bb5df-127">關於播放清單、PlaylistCollection 和 PlaylistArray 物件</span><span class="sxs-lookup"><span data-stu-id="bb5df-127">About the Playlist, PlaylistCollection, and PlaylistArray Objects</span></span>

<span data-ttu-id="bb5df-128">**播放清單**、 **PlaylistCollection** 和 **PlaylistArray** 物件會管理 Windows Media Player 可用來指定播放內容之順序的播放清單。</span><span class="sxs-lookup"><span data-stu-id="bb5df-128">The **Playlist**, **PlaylistCollection**, and **PlaylistArray** objects govern the playlists that Windows Media Player can use to specify the order in which content will be played.</span></span> <span data-ttu-id="bb5df-129">您可以從 **Player** 物件的 **PlaylistCollection** 屬性取得 **PlaylistCollection** 物件。</span><span class="sxs-lookup"><span data-stu-id="bb5df-129">You get the **PlaylistCollection** object from the **playlistCollection** property of the **Player** object.</span></span> <span data-ttu-id="bb5df-130">**PlaylistCollection** 屬性會傳回 **playlistCollection** 物件。</span><span class="sxs-lookup"><span data-stu-id="bb5df-130">The **playlistCollection** property returns the **PlaylistCollection** object.</span></span> <span data-ttu-id="bb5df-131">您只能在建立 **PlaylistCollection** 物件之後，存取其屬性。</span><span class="sxs-lookup"><span data-stu-id="bb5df-131">You can only access the properties of the **PlaylistCollection** object after you have created it.</span></span> <span data-ttu-id="bb5df-132">例如，若要建立新的播放清單，您必須先取得 **PlaylistCollection** 物件，然後在該物件上使用方法。</span><span class="sxs-lookup"><span data-stu-id="bb5df-132">For example, to create a new playlist, you must first get the **PlaylistCollection** object and then use a method on that object.</span></span>


```C++
player.playlistcollection.newplaylist('myplaylist');
```



<span data-ttu-id="bb5df-133">您可以使用 **currentPlaylist** 屬性來取得目前的播放清單。</span><span class="sxs-lookup"><span data-stu-id="bb5df-133">You can get the current playlist by using the **currentPlaylist** property.</span></span> <span data-ttu-id="bb5df-134">例如，若要取得目前播放清單的名稱，請使用下列程式碼：</span><span class="sxs-lookup"><span data-stu-id="bb5df-134">For example, to get the name of the current playlist, use the following code:</span></span>


```C++
myname = player.currentplaylist.name;
```



<span data-ttu-id="bb5df-135">**PlaylistArray** 物件是由 **PlaylistCollection** 物件的 **getAll** 和 **getByName** 方法所傳回。</span><span class="sxs-lookup"><span data-stu-id="bb5df-135">The **PlaylistArray** object is returned by the **getAll** and **getByName** methods of the **PlaylistCollection** object.</span></span> <span data-ttu-id="bb5df-136">例如，若要取得播放清單的數目，請使用下列程式碼：</span><span class="sxs-lookup"><span data-stu-id="bb5df-136">To get the number of playlists, for example, use the following code:</span></span>


```C++
howmany = player.playlistcollection.getAll().count;
```



<span data-ttu-id="bb5df-137">若要依名稱取得已知播放清單，請使用下列程式碼：</span><span class="sxs-lookup"><span data-stu-id="bb5df-137">To retrieve a known playlist by name, use the following code:</span></span>


```C++
if (player.playlistcollection.getbyname('myplaylist').count == 1) {
    pl = player.playlistcollection.getbyname('myplaylist').item(0);
}
```



## <a name="related-topics"></a><span data-ttu-id="bb5df-138">相關主題</span><span class="sxs-lookup"><span data-stu-id="bb5df-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bb5df-139">**指令碼語言的播放程式物件模型**</span><span class="sxs-lookup"><span data-stu-id="bb5df-139">**Player Object Model for Scripting Languages**</span></span>](player-object-model-for-scripting-languages.md)
</dt> <dt>

[<span data-ttu-id="bb5df-140">**播放清單物件**</span><span class="sxs-lookup"><span data-stu-id="bb5df-140">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="bb5df-141">**PlaylistArray 物件**</span><span class="sxs-lookup"><span data-stu-id="bb5df-141">**PlaylistArray Object**</span></span>](playlistarray-object.md)
</dt> <dt>

[<span data-ttu-id="bb5df-142">**PlaylistCollection 物件**</span><span class="sxs-lookup"><span data-stu-id="bb5df-142">**PlaylistCollection Object**</span></span>](playlistcollection-object.md)
</dt> </dl>

 

 




