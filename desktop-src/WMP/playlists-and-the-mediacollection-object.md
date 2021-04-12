---
title: 播放清單和 MediaCollection 物件
description: 播放清單和 MediaCollection 物件
ms.assetid: 3c98ceed-2545-4774-998b-c1db0d172a81
keywords:
- Windows Media Player，播放清單
- Windows Media Player 物件模型，播放清單
- 物件模型，播放清單
- Windows Media Player 行動裝置、播放清單
- Windows Media Player ActiveX 控制項，播放清單
- Windows Media Player 的行動 ActiveX 控制項、播放清單
- ActiveX 控制項，播放清單
- 播放清單，MediaCollection 物件
- 中繼檔播放清單，MediaCollection 物件
- Windows Media 中繼檔播放清單，MediaCollection 物件
- MediaCollection 物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 334b693046e6c78e92a4af901816b57bb9c4cddc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372029"
---
# <a name="playlists-and-the-mediacollection-object"></a><span data-ttu-id="047a1-114">播放清單和 MediaCollection 物件</span><span class="sxs-lookup"><span data-stu-id="047a1-114">Playlists and the MediaCollection Object</span></span>

<span data-ttu-id="047a1-115">**MediaCollection** 物件可讓您存取各種特殊的播放清單，並包含從中繼檔建立新播放清單的方法。</span><span class="sxs-lookup"><span data-stu-id="047a1-115">The **MediaCollection** object gives you access to a variety of special playlists, and includes a method for creating a new playlist from a metafile.</span></span>

<span data-ttu-id="047a1-116">下列方法會取出特殊的播放清單：</span><span class="sxs-lookup"><span data-stu-id="047a1-116">The following methods retrieve special playlists:</span></span>

-   <span data-ttu-id="047a1-117">**getAll**</span><span class="sxs-lookup"><span data-stu-id="047a1-117">**getAll**</span></span>
-   <span data-ttu-id="047a1-118">**getByAlbum**</span><span class="sxs-lookup"><span data-stu-id="047a1-118">**getByAlbum**</span></span>
-   <span data-ttu-id="047a1-119">**getByAttribute**</span><span class="sxs-lookup"><span data-stu-id="047a1-119">**getByAttribute**</span></span>
-   <span data-ttu-id="047a1-120">**getByAuthor**</span><span class="sxs-lookup"><span data-stu-id="047a1-120">**getByAuthor**</span></span>
-   <span data-ttu-id="047a1-121">**getByGenre**</span><span class="sxs-lookup"><span data-stu-id="047a1-121">**getByGenre**</span></span>
-   <span data-ttu-id="047a1-122">**getByName**</span><span class="sxs-lookup"><span data-stu-id="047a1-122">**getByName**</span></span>

<span data-ttu-id="047a1-123">顧名思義，這些方法會取出包含媒體櫃中符合特定準則之所有媒體專案的播放清單。</span><span class="sxs-lookup"><span data-stu-id="047a1-123">As their names suggest, these methods retrieve playlists containing all of the media items in the library that match certain criteria.</span></span>

<span data-ttu-id="047a1-124">請小心不要混淆 *MediaCollection*。具有 *PlaylistCollection* 的 **getByName** 方法。**getByName** 方法。</span><span class="sxs-lookup"><span data-stu-id="047a1-124">Be careful not to confuse the *MediaCollection*.**getByName** method with the *PlaylistCollection*.**getByName** method.</span></span> <span data-ttu-id="047a1-125">**MediaCollection** 方法會傳回包含所有具有指定名稱之媒體專案的 **播放清單** 物件。</span><span class="sxs-lookup"><span data-stu-id="047a1-125">The **MediaCollection** method returns a **Playlist** object containing all of the media items that have the specified name.</span></span> <span data-ttu-id="047a1-126">**PlaylistCollection** 方法會傳回 **PlaylistArray** 物件，其中包含所有具有指定名稱的播放清單。</span><span class="sxs-lookup"><span data-stu-id="047a1-126">The **PlaylistCollection** method returns a **PlaylistArray** object containing all of the playlists that have the specified name.</span></span>

<span data-ttu-id="047a1-127">您可以使用 *MediaCollection*。**新增** 方法，以將播放清單以及媒體專案新增至程式庫。</span><span class="sxs-lookup"><span data-stu-id="047a1-127">You can use the *MediaCollection*.**add** method to add playlists as well as media items to the library.</span></span> <span data-ttu-id="047a1-128">若要加入播放清單，請將路徑傳遞給定義播放清單的中繼檔。</span><span class="sxs-lookup"><span data-stu-id="047a1-128">To add a playlist, you pass the method the path to the metafile that defines the playlist.</span></span> <span data-ttu-id="047a1-129">方法一律會傳回 **媒體** 物件。</span><span class="sxs-lookup"><span data-stu-id="047a1-129">The method always returns a **Media** object.</span></span> <span data-ttu-id="047a1-130">您無法在 **媒體** 與 **播放清單** 物件之間轉換。</span><span class="sxs-lookup"><span data-stu-id="047a1-130">You cannot cast between **Media** and **Playlist** objects.</span></span> <span data-ttu-id="047a1-131">若要使用您新增的播放清單，請取得與 **媒體** 物件同名的 **播放清單** 物件。</span><span class="sxs-lookup"><span data-stu-id="047a1-131">To work with the playlist that you added, retrieve the **Playlist** object that has the same name as the **Media** object.</span></span>

<span data-ttu-id="047a1-132">下列 c # 範例示範如何使用 **MediaCollection** 依類型取得媒體。**getByAttribute** 方法。</span><span class="sxs-lookup"><span data-stu-id="047a1-132">The following C# example demonstrates how to retrieve media by type using the **MediaCollection**.**getByAttribute** method.</span></span> <span data-ttu-id="047a1-133">此程式碼會抓取與指定類型相關聯之所有屬性的名稱，以及這些屬性的讀/寫或唯讀狀態。</span><span class="sxs-lookup"><span data-stu-id="047a1-133">This code retrieves the names of all attributes associated with a given type as well as the read/write or read-only status of those attributes.</span></span> <span data-ttu-id="047a1-134">它會產生單一檔案，其中包含音訊、影片、廣播、播放清單、其他、音樂和相片類型的屬性清單。</span><span class="sxs-lookup"><span data-stu-id="047a1-134">It generates a single file that contains lists of attributes for the Audio, Video, Radio, Playlist, Other, Music, and Photo types.</span></span>


```C++
string strOutFile = "AttribList.txt";    // Name of the output file
...
StreamWriter sw = new StreamWriter(strOutFile, true);

sw.Write(getMediaCollectionNames("Audio"));
sw.Write(getMediaCollectionNames("Video"));
sw.Write(getMediaCollectionNames("Radio"));
sw.Write(getMediaCollectionNames("Playlist"));
sw.Write(getMediaCollectionNames("Other"));
sw.Write(getMediaCollectionNames("Music"));
sw.Write(getMediaCollectionNames("Photo"));
sw.Close();
...
// The getMediaCollection method retrieves the names of
// all attributes for a specified type.
private string getMediaCollectionNames(string sSchema)
{
IWMPPlaylist playlist;
IWMPMedia media;
string strResult = "";    // Cumulative list of attributes
string strAttrName = "";  // Attribute name
string strReadWrite = ""; // Read/Write status of attribute
int iAttrCount = 0;       // Count of playlist attributes

// Retrieve a playlist corresponding to the requested type.
playlist = Player.mediaCollection.getByAttribute("MediaType", sSchema);

// Initialize the result string
strResult += "\n" + sSchema.ToString() + " Schema: \n";

// Retrieve the attributes for the playlist
if (playlist.count != 0)
{
    media = playlist.get_Item(0);
    iAttrCount = media.attributeCount;
    for (int i = 0; i < iAttrCount; i++)
    {
        strAttrName = media.getAttributeName(i);
        strResult += "   " + strAttrName  +"\n";
        if (media.isReadOnlyItem(strAttrName))
            strReadWrite = "Read Only";
        else
            strReadWrite = "Read/Write";
        strResult += "         " + strReadWrite + "\n";
    }
}

return strResult;
}

```



<span data-ttu-id="047a1-135">下列 c # 範例示範如何從中繼檔將播放清單新增至程式庫。</span><span class="sxs-lookup"><span data-stu-id="047a1-135">The following C# example demonstrates how to add a playlist from a metafile to the library.</span></span>


```C++
// Add a playlist as a media item
IWMPMedia Media = Player.mediaCollection.add("c:\\testPlayList.asx");

```



<span data-ttu-id="047a1-136">靜態播放清單包含特定媒體專案。</span><span class="sxs-lookup"><span data-stu-id="047a1-136">Static playlists include specific media items.</span></span> <span data-ttu-id="047a1-137">自動播放清單會在每次開啟程式庫時搜尋程式庫，而且可能會在不同時間包含不同的媒體專案。</span><span class="sxs-lookup"><span data-stu-id="047a1-137">Auto playlists search the library every time they are opened and may contain different media items at different times.</span></span> <span data-ttu-id="047a1-138">您可以使用 *MediaCollection*，將靜態和自動播放清單新增至程式庫。**add** 方法。</span><span class="sxs-lookup"><span data-stu-id="047a1-138">You can add both static and auto playlists to the library by using the *MediaCollection*.**add** method.</span></span> <span data-ttu-id="047a1-139">您也可以使用 *PlaylistCollection* 來新增靜態播放清單。**importPlaylist** 方法。</span><span class="sxs-lookup"><span data-stu-id="047a1-139">You can also add static playlists by using the *PlaylistCollection*.**importPlaylist** method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="047a1-140">相關主題</span><span class="sxs-lookup"><span data-stu-id="047a1-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="047a1-141">**管理播放清單**</span><span class="sxs-lookup"><span data-stu-id="047a1-141">**Managing Playlists**</span></span>](managing-playlists.md)
</dt> <dt>

[<span data-ttu-id="047a1-142">**MediaCollection 物件**</span><span class="sxs-lookup"><span data-stu-id="047a1-142">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="047a1-143">**播放清單物件**</span><span class="sxs-lookup"><span data-stu-id="047a1-143">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="047a1-144">**PlaylistCollection 物件**</span><span class="sxs-lookup"><span data-stu-id="047a1-144">**PlaylistCollection Object**</span></span>](playlistcollection-object.md)
</dt> <dt>

[<span data-ttu-id="047a1-145">**播放清單和 PlaylistCollection 物件**</span><span class="sxs-lookup"><span data-stu-id="047a1-145">**Playlists and the PlaylistCollection Object**</span></span>](playlists-and-the-playlistcollection-object.md)
</dt> <dt>

[<span data-ttu-id="047a1-146">**靜態和自動播放清單**</span><span class="sxs-lookup"><span data-stu-id="047a1-146">**Static and Auto Playlists**</span></span>](static-and-auto-playlists.md)
</dt> </dl>

 

 




