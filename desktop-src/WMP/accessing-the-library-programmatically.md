---
title: 以程式設計方式存取程式庫
description: 以程式設計方式存取程式庫
ms.assetid: f48fbb49-5b79-4a78-af72-8509c460a149
keywords:
- Windows Media Player，程式庫
- Windows Media Player 物件模型，程式庫
- 物件模型，程式庫
- Windows Media Player ActiveX 控制項，物件模型的程式庫
- ActiveX 控制項，物件模型的程式庫
- Windows Media Player 的行動 ActiveX 控制項、物件模型的程式庫
- Windows Media Player 行動裝置、物件模型的程式庫
- Windows Media Player 程式庫，以程式設計方式存取
- 程式庫，存取
- 以程式設計方式存取 Windows Media Player 程式庫
- Windows Media Player 程式庫，新增媒體專案
- 程式庫，新增媒體專案
- Windows Media Player 程式庫，正在抓取媒體專案
- 程式庫，正在抓取媒體專案
- Windows Media Player 程式庫，移除媒體專案
- 程式庫，移除媒體專案
- 將媒體專案新增至 Windows Media Player 程式庫
- 從 Windows Media Player 程式庫中取出媒體專案
- 從 Windows Media Player 程式庫移除媒體專案
- 擷取中繼資料
- Windows Media Player 程式庫，從媒體專案中取出中繼資料
- 程式庫，從媒體專案中取出中繼資料
- 中繼資料，正在抓取
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d40e03e91b2a67a24cb49b0ac1810ceb7b9544c9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372394"
---
# <a name="accessing-the-library-programmatically"></a><span data-ttu-id="1b123-126">以程式設計方式存取程式庫</span><span class="sxs-lookup"><span data-stu-id="1b123-126">Accessing the Library Programmatically</span></span>

<span data-ttu-id="1b123-127">在程式碼中，程式庫是以 **MediaCollection** 物件代表， (或 **IWMPMediaCollection** 介面) 。</span><span class="sxs-lookup"><span data-stu-id="1b123-127">In code, the library is represented by the **MediaCollection** object (or the **IWMPMediaCollection** interface).</span></span> <span data-ttu-id="1b123-128">媒體專案會以 **媒體** 物件 (或由 **IWMPMedia** 介面) 來表示。</span><span class="sxs-lookup"><span data-stu-id="1b123-128">Media items are represented as **Media** objects (or by the **IWMPMedia** interface).</span></span> <span data-ttu-id="1b123-129">播放清單專案會以 **播放清單** 物件 (或由 **IWMPPlaylist** 介面) 表示。</span><span class="sxs-lookup"><span data-stu-id="1b123-129">Playlist items are represented as **Playlist** objects (or by the **IWMPPlaylist** interface).</span></span> <span data-ttu-id="1b123-130">為了簡單起見，此區段只會參考物件名稱（如果可能的話）。</span><span class="sxs-lookup"><span data-stu-id="1b123-130">For simplicity, this section will simply refer to object names, when possible.</span></span>

<span data-ttu-id="1b123-131">您可以使用 **MediaCollection** 物件來處理媒體專案和播放清單。</span><span class="sxs-lookup"><span data-stu-id="1b123-131">By using the **MediaCollection** object, you can work with media items and playlists.</span></span> <span data-ttu-id="1b123-132">此程式庫也會公開 **PlaylistCollection** 物件 (或 **IWMPPlaylistCollection** 介面) ，其提供使用播放清單的特定功能。</span><span class="sxs-lookup"><span data-stu-id="1b123-132">The library also exposes the **PlaylistCollection** object (or the **IWMPPlaylistCollection** interface), which provides some functionality specific to working with playlists.</span></span> <span data-ttu-id="1b123-133">大部分的情況下， **MediaCollection** 物件會提供您所需的功能，即使使用播放清單也一樣。</span><span class="sxs-lookup"><span data-stu-id="1b123-133">Most of the time, the **MediaCollection** object will provide you with the functionality you need, even when working with playlists.</span></span> <span data-ttu-id="1b123-134">如需使用媒體專案的詳細資訊，請參閱 [管理媒體專案](managing-media-items.md)。</span><span class="sxs-lookup"><span data-stu-id="1b123-134">For more information about working with media items, see [Managing Media Items](managing-media-items.md).</span></span> <span data-ttu-id="1b123-135">如需使用播放清單的詳細資訊，請參閱 [管理播放清單](managing-playlists.md)。</span><span class="sxs-lookup"><span data-stu-id="1b123-135">For more information about working with playlists, see [Managing Playlists](managing-playlists.md).</span></span>

## <a name="adding-media-items-to-the-library"></a><span data-ttu-id="1b123-136">將媒體專案新增至程式庫</span><span class="sxs-lookup"><span data-stu-id="1b123-136">Adding Media Items to the Library</span></span>

<span data-ttu-id="1b123-137">將數位媒體內容新增至媒體櫃很簡單。</span><span class="sxs-lookup"><span data-stu-id="1b123-137">Adding digital media content to the library is straightforward.</span></span> <span data-ttu-id="1b123-138">只要呼叫 MediaCollection，就可以 [將](mediacollection-add.md) 路徑當作引數提供給媒體檔案。</span><span class="sxs-lookup"><span data-stu-id="1b123-138">Simply call the [MediaCollection.add](mediacollection-add.md) method, providing the path to the media file as an argument.</span></span>

## <a name="retrieving-media-items-from-the-library"></a><span data-ttu-id="1b123-139">從程式庫中取出媒體專案</span><span class="sxs-lookup"><span data-stu-id="1b123-139">Retrieving Media Items from the Library</span></span>

<span data-ttu-id="1b123-140">當您從媒體櫃取出媒體專案時，您真正取得的是播放清單。</span><span class="sxs-lookup"><span data-stu-id="1b123-140">When you retrieve media items from the library, what you really retrieve is a playlist.</span></span> <span data-ttu-id="1b123-141">即使您預期只抓取一個媒體專案，您仍會收到包含單一專案的 **播放清單** 物件，該專案會與索引零相關聯。</span><span class="sxs-lookup"><span data-stu-id="1b123-141">Even if you expect to retrieve only one media item, you will get a **Playlist** object containing a single item, which will be associated with index zero.</span></span> <span data-ttu-id="1b123-142">例如，如果您想要取出代表名為 "Jeanne" 之歌曲的 **媒體** 物件，您可以使用下列 JScript 程式碼：</span><span class="sxs-lookup"><span data-stu-id="1b123-142">For example, if you want to retrieve a **Media** object that represents the song named "Jeanne", you could use the following JScript code:</span></span>


```C++
// Retrieve media named Jeanne from the library.
var playlist = player.mediaCollection.getByName("Jeanne");

```



<span data-ttu-id="1b123-143">上述程式碼會抓取播放清單，其中包含名稱為 "Jeanne" 的所有媒體專案作為標題。</span><span class="sxs-lookup"><span data-stu-id="1b123-143">The preceding code retrieves a playlist containing all the media items having the name "Jeanne" as the title.</span></span> <span data-ttu-id="1b123-144">在此範例中，假設您知道媒體櫃中只有一個該名稱的歌曲 (請注意，程式庫支援多個具有相同名稱) 的歌曲。</span><span class="sxs-lookup"><span data-stu-id="1b123-144">For this example, assume that you know there is only one song by that name in the library (note that the library supports multiple songs having the same name).</span></span> <span data-ttu-id="1b123-145">這表示您可以預期您抓取的播放清單中的專案計數等於1，而媒體專案會以索引零表示。</span><span class="sxs-lookup"><span data-stu-id="1b123-145">This means you could expect the count of items in the playlist you retrieved to equal one and the media item would be represented by index zero.</span></span> <span data-ttu-id="1b123-146">下列範例程式碼會繼續上一個範例，以示範如何使用 [播放清單專案](playlist-item.md) 方法，從播放清單取出媒體專案。</span><span class="sxs-lookup"><span data-stu-id="1b123-146">The following example code continues the previous example to demonstrate how you would retrieve the media item from the playlist by using the [Playlist.item](playlist-item.md) method.</span></span>


```C++
// Retrieve the individual media item from the playlist.
var media = playlist.item(0);

```



<span data-ttu-id="1b123-147">如需有關從播放清單中取得媒體專案的詳細資訊，請參閱《[播放程式控制指南》](player-control-guide.md)中的[播放清單和媒體專案](playlists-and-media-items.md)。</span><span class="sxs-lookup"><span data-stu-id="1b123-147">For more information about retrieving media items from playlists, see [Playlists and Media Items](playlists-and-media-items.md) in the [Player Control Guide](player-control-guide.md).</span></span>

## <a name="retrieving-metadata-from-a-media-item"></a><span data-ttu-id="1b123-148">從媒體專案中取出中繼資料</span><span class="sxs-lookup"><span data-stu-id="1b123-148">Retrieving Metadata from a Media Item</span></span>

<span data-ttu-id="1b123-149">取得 **媒體** 物件之後，您可以讀取與內容相關聯的屬性值。</span><span class="sxs-lookup"><span data-stu-id="1b123-149">After you retrieve a **Media** object, you can read the attribute values associated with the content.</span></span> <span data-ttu-id="1b123-150">在最簡單的情況下，您可能只想要知道單一值，例如執行音樂播放軌的演出者名稱。下列 JScript 範例示範如何使用 [getItemInfo](media-getiteminfo.md) 方法，從上一個範例中取出的媒體取出演出者的名稱：</span><span class="sxs-lookup"><span data-stu-id="1b123-150">In the simplest case, you might simply want to know a single value, such as the name of the artist who performed a music track. The following JScript example shows how to use the [Media.getItemInfo](media-getiteminfo.md) method to retrieve the name of the artist from the media retrieved in the previous example:</span></span>


```C++
// Retrieve the artist name string.
var author = media.getItemInfo("Artist");

```



<span data-ttu-id="1b123-151">媒體專案可以有許多不同的屬性，而且使用中繼資料並不一定像前一個範例所示的簡單案例一樣簡單。</span><span class="sxs-lookup"><span data-stu-id="1b123-151">A media item can have many different attributes, and working with metadata is not always as straightforward as the simple case shown in the previous example.</span></span> <span data-ttu-id="1b123-152">例如，某些屬性可包含多個值，或具有多個語言的值。</span><span class="sxs-lookup"><span data-stu-id="1b123-152">For instance, some attributes can contain multiple values or have values in more than one language.</span></span> <span data-ttu-id="1b123-153">如需使用中繼資料的詳細資訊，請參閱 [媒體專案屬性](media-item-attributes.md)。</span><span class="sxs-lookup"><span data-stu-id="1b123-153">For more information about working with metadata, see [Media Item Attributes](media-item-attributes.md).</span></span> <span data-ttu-id="1b123-154">如需各種屬性、其意義及檔案類型支援的詳細資訊，請參閱 [屬性參考](attribute-reference.md)。</span><span class="sxs-lookup"><span data-stu-id="1b123-154">For more information about the various attributes, their meanings, and file type support, see the [Attribute Reference](attribute-reference.md).</span></span>

## <a name="removing-media-items-from-the-library"></a><span data-ttu-id="1b123-155">從媒體櫃移除媒體專案</span><span class="sxs-lookup"><span data-stu-id="1b123-155">Removing Media Items from the Library</span></span>

<span data-ttu-id="1b123-156">從媒體櫃移除數位媒體內容也很簡單。</span><span class="sxs-lookup"><span data-stu-id="1b123-156">Removing digital media content from the library is also straightforward.</span></span> <span data-ttu-id="1b123-157">只要呼叫 **MediaCollection**，就會提供代表專案的 **媒體** 物件做為第一個引數，並將值 **true** 做為第二個引數。</span><span class="sxs-lookup"><span data-stu-id="1b123-157">Simply call **MediaCollection.remove**, providing the **Media** object that represents the item as the first argument and the value **true** as the second.</span></span> <span data-ttu-id="1b123-158">下列 JScript 範例會從程式庫移除先前範例) 中， (抓取名為 Jeanne 的檔案：</span><span class="sxs-lookup"><span data-stu-id="1b123-158">The following JScript example removes the file named Jeanne (retrieved in the previous example) from the library:</span></span>


```C++
// Remove Jeanne from the library.
playst.mediaCollection.remove(media, true);

```



## <a name="related-topics"></a><span data-ttu-id="1b123-159">相關主題</span><span class="sxs-lookup"><span data-stu-id="1b123-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1b123-160">**關於程式庫**</span><span class="sxs-lookup"><span data-stu-id="1b123-160">**About the Library**</span></span>](about-the-library.md)
</dt> <dt>

[<span data-ttu-id="1b123-161">**關於 MediaCollection 和 Media 物件**</span><span class="sxs-lookup"><span data-stu-id="1b123-161">**About the MediaCollection and Media Objects**</span></span>](about-the-mediacollection-and-media-objects.md)
</dt> <dt>

[<span data-ttu-id="1b123-162">**關於播放清單、PlaylistCollection 和 PlaylistArray 物件**</span><span class="sxs-lookup"><span data-stu-id="1b123-162">**About the Playlist, PlaylistCollection, and PlaylistArray Objects**</span></span>](about-the-playlist--playlistcollection--and-playlistarray-objects.md)
</dt> <dt>

[<span data-ttu-id="1b123-163">**使用程式庫**</span><span class="sxs-lookup"><span data-stu-id="1b123-163">**Working with the Library**</span></span>](working-with-the-library.md)
</dt> </dl>

 

 




