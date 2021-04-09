---
title: 播放清單和媒體專案
description: 播放清單和媒體專案
ms.assetid: 281c744d-380e-4200-8585-a3f378bc1c36
keywords:
- Windows Media Player，播放清單
- Windows Media Player 物件模型，播放清單
- 物件模型，播放清單
- Windows Media Player 行動裝置、播放清單
- Windows Media Player ActiveX 控制項，播放清單
- Windows Media Player 的行動 ActiveX 控制項、播放清單
- ActiveX 控制項，播放清單
- 播放清單、媒體專案
- 中繼檔播放清單、媒體專案
- Windows Media 中繼檔播放清單、媒體專案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4716a8ce07e7b0ec8348ce1a6981e23291335e7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932069"
---
# <a name="playlists-and-media-items"></a><span data-ttu-id="1c36f-113">播放清單和媒體專案</span><span class="sxs-lookup"><span data-stu-id="1c36f-113">Playlists and Media Items</span></span>

<span data-ttu-id="1c36f-114">播放清單是一組媒體專案。</span><span class="sxs-lookup"><span data-stu-id="1c36f-114">A playlist is a set of media items.</span></span> <span data-ttu-id="1c36f-115">**播放清單** 物件可以操控代表這些專案的 **媒體** 物件。</span><span class="sxs-lookup"><span data-stu-id="1c36f-115">A **Playlist** object can manipulate the **Media** objects that represent those items.</span></span>

## <a name="retrieving-media-items"></a><span data-ttu-id="1c36f-116">正在抓取媒體專案</span><span class="sxs-lookup"><span data-stu-id="1c36f-116">Retrieving Media Items</span></span>

<span data-ttu-id="1c36f-117">若為現有的播放清單，您可以閱讀 *播放清單*。**count** 屬性可判斷播放清單中有多少媒體專案，而且您可以使用 *播放清單* 來取得對應至特定專案之 **媒體** 物件的參考。**item** 屬性。</span><span class="sxs-lookup"><span data-stu-id="1c36f-117">For an existing playlist, you can read the *Playlist*.**count** property to determine how many media items are in the playlist, and you can get a reference to the **Media** object corresponding to a specific item using the *Playlist*.**item** property.</span></span>

<span data-ttu-id="1c36f-118">下列 c # 範例會捕獲特定媒體專案的物件參考。</span><span class="sxs-lookup"><span data-stu-id="1c36f-118">The following C# example retrieves an object reference to a specific media item.</span></span> <span data-ttu-id="1c36f-119"> (在本主題中，變數 *pList* 是 **播放清單** 物件的參考。 ) </span><span class="sxs-lookup"><span data-stu-id="1c36f-119">(Throughout this topic, the variable *pList* is a reference to a **Playlist** object.)</span></span>


```C++
currMedia = pList.Item(0);

```



<span data-ttu-id="1c36f-120">下列 c # 範例會抓取播放清單中所有媒體專案的名稱，並將它們放在名為 lstOutput 的 ListBox 中。</span><span class="sxs-lookup"><span data-stu-id="1c36f-120">The following C# example retrieves the names of all the media items in a playlist and puts them in a ListBox named lstOutput.</span></span>


```C++
for (j=0; j < pList.count; j++)
{
    strItemName = pList.get_Item(j).name;
    lstOutput.Items.Add(strItemName);
}

```



## <a name="adding-items-to-a-playlist"></a><span data-ttu-id="1c36f-121">將專案新增至播放清單</span><span class="sxs-lookup"><span data-stu-id="1c36f-121">Adding Items to a Playlist</span></span>

<span data-ttu-id="1c36f-122">您可以使用 *播放清單*，將媒體專案新增至播放清單的結尾或播放清單中的特定位置。**appendItem** 和 *播放清單*。**insertItem** 方法。</span><span class="sxs-lookup"><span data-stu-id="1c36f-122">You can add a media item to the end of a playlist or at a specific position in a playlist, using the *Playlist*.**appendItem** and *Playlist*.**insertItem** methods.</span></span>

<span data-ttu-id="1c36f-123">在本主題中， **Player** 物件是以下列方式定義：</span><span class="sxs-lookup"><span data-stu-id="1c36f-123">Throughout this topic, the **Player** object was defined in the following manner:</span></span>


```C++
AxWMPLib.AxWindowsMediaPlayer Player;
using WMPLib;

```



<span data-ttu-id="1c36f-124">下列 c # 範例會示範這兩種技術，方法是將目前的媒體專案新增至名為 "BluesTest" 的播放清單，先在結尾，然後在播放清單的開頭。</span><span class="sxs-lookup"><span data-stu-id="1c36f-124">The following C# example demonstrates both techniques by adding the current media item to a playlist named "BluesTest", first at the end and then at the beginning of the playlist.</span></span>


```C++
IWMPPlaylistCollection pListColl;
IWMPPlaylistArray pListArray;
IWMPPlaylist pList;

// Initialize the Media object
IWMPMedia currMedia = Player.currentMedia;

if(currMedia != null)
{
    // Retrieve the playlist collection
    pListColl = Player.playlistCollection;

    // Retrieve a playlist array containing
    // playlists named BluesTest
    pListArray = pListColl.getByName("BluesTest");

    // Retrieve the first element with this name from the
    // array.
    pList = pListArray.Item(0);

    // Add the current item to the end, and then, the beginning
    // of the specified playlist.
    pList.appendItem(currMedia);
    pList.insertItem(0, currMedia);
}

```



<span data-ttu-id="1c36f-125">當您使用 *PlaylistCollection* 建立新的空白播放清單時。**[]** 方法，您可以重複呼叫 *播放清單* 來將媒體專案加入其中。**appendItem** 方法。</span><span class="sxs-lookup"><span data-stu-id="1c36f-125">When you create a new, empty playlist by using the *PlaylistCollection*.**newPlaylist** method, you can add media items to it by repeatedly calling the *Playlist*.**appendItem** method.</span></span>

## <a name="manipulating-media-items-in-a-playlist"></a><span data-ttu-id="1c36f-126">操作播放清單中的媒體專案</span><span class="sxs-lookup"><span data-stu-id="1c36f-126">Manipulating Media Items in a Playlist</span></span>

<span data-ttu-id="1c36f-127">您可以使用 *播放清單* 來變更媒體專案在播放清單中的位置。**moveItem** 方法。</span><span class="sxs-lookup"><span data-stu-id="1c36f-127">You can change the position of a media item in the playlist by using the *Playlist*.**moveItem** method.</span></span> <span data-ttu-id="1c36f-128">您可以依目前的索引來指定專案，然後指定新的索引。</span><span class="sxs-lookup"><span data-stu-id="1c36f-128">You specify the item by its current index, and then you specify the new index.</span></span> <span data-ttu-id="1c36f-129">下列 c # 範例會在播放清單中將專案從索引5移至索引0。</span><span class="sxs-lookup"><span data-stu-id="1c36f-129">The following C# example moves an item from index 5 to index 0 within a playlist.</span></span>


```C++
// Move the 6th item to the beginning
// of the specified playlist.
pList.moveItem(5, 0);

```



<span data-ttu-id="1c36f-130">您可以使用 **播放清單** 來移除播放清單中的媒體專案。**removeItem** 方法。</span><span class="sxs-lookup"><span data-stu-id="1c36f-130">You can remove a media item from the playlist by using the **Playlist**.**removeItem** method.</span></span> <span data-ttu-id="1c36f-131">請注意，如果移除的專案不是播放清單中的最後一個專案，後續專案的索引值就會變更。</span><span class="sxs-lookup"><span data-stu-id="1c36f-131">Note that if the removed item was not the final item in the playlist, the index values of the subsequent items change.</span></span> <span data-ttu-id="1c36f-132">下列 c # 範例會移除指定的專案。</span><span class="sxs-lookup"><span data-stu-id="1c36f-132">The following C# example removes the specified item.</span></span>


```C++
// Remove the currently playing item from the
// specified playlist.
pList.removeItem(currMedia);

```



> [!Note]  
> <span data-ttu-id="1c36f-133">使用者可以在您的應用程式之外變更播放清單的內容。</span><span class="sxs-lookup"><span data-stu-id="1c36f-133">Users can change the contents of a playlist outside of your application.</span></span> <span data-ttu-id="1c36f-134">當您操作播放清單中的專案時，您應該監視和處理 Windows Media Player 控制項的播放清單相關事件，以確保您的程式碼正常運作。</span><span class="sxs-lookup"><span data-stu-id="1c36f-134">Whenever you manipulate the items in a playlist, you should monitor and handle the playlist-related events of the Windows Media Player control to ensure that your code works correctly.</span></span> <span data-ttu-id="1c36f-135">這些事件是 *Player*。**CurrentPlaylistChange** 和 *Player*。**PlaylistChange**。</span><span class="sxs-lookup"><span data-stu-id="1c36f-135">These events are *Player*.**CurrentPlaylistChange** and *Player*.**PlaylistChange**.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="1c36f-136">相關主題</span><span class="sxs-lookup"><span data-stu-id="1c36f-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1c36f-137">**管理播放清單**</span><span class="sxs-lookup"><span data-stu-id="1c36f-137">**Managing Playlists**</span></span>](managing-playlists.md)
</dt> <dt>

[<span data-ttu-id="1c36f-138">**媒體物件**</span><span class="sxs-lookup"><span data-stu-id="1c36f-138">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="1c36f-139">**播放清單物件**</span><span class="sxs-lookup"><span data-stu-id="1c36f-139">**Playlist Object**</span></span>](playlist-object.md)
</dt> </dl>

 

 




