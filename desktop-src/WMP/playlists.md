---
title: 播放清單
description: 播放清單
ms.assetid: b1ac9208-33d1-448f-9e2e-920fad9c6add
keywords:
- Windows Media Player，播放清單
- Windows Media Player 物件模型，播放清單
- 物件模型，播放清單
- Windows Media Player ActiveX 控制項，播放清單
- ActiveX 控制項，播放清單
- Windows Media Player 的行動 ActiveX 控制項、播放清單
- Windows Media Player 行動裝置、播放清單
- 播放清單，遷移
- Windows Media 中繼檔播放清單，遷移
- 中繼檔播放清單，遷移
- 遷移指南，播放清單
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 124c07a6bd3aec0bebd235678e9fa8a5f069ec73
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021181"
---
# <a name="playlists"></a><span data-ttu-id="954a1-114">播放清單</span><span class="sxs-lookup"><span data-stu-id="954a1-114">Playlists</span></span>

<span data-ttu-id="954a1-115">Windows Media Player 6.4 ActiveX 控制項物件模型包含四種方法，以及一個用於處理 Windows Media 中繼檔播放清單的屬性：</span><span class="sxs-lookup"><span data-stu-id="954a1-115">The Windows Media Player 6.4 ActiveX control object model includes four methods and one property for working with Windows Media metafile playlists:</span></span>

-   <span data-ttu-id="954a1-116">*Player6*。**GetCurrentEntry**</span><span class="sxs-lookup"><span data-stu-id="954a1-116">*Player6*.**GetCurrentEntry**</span></span>
-   <span data-ttu-id="954a1-117">*Player6*。**SetCurrentEntry**</span><span class="sxs-lookup"><span data-stu-id="954a1-117">*Player6*.**SetCurrentEntry**</span></span>
-   <span data-ttu-id="954a1-118">*Player6*。**GetMediaParameter**</span><span class="sxs-lookup"><span data-stu-id="954a1-118">*Player6*.**GetMediaParameter**</span></span>
-   <span data-ttu-id="954a1-119">*Player6*。**GetMediaParameterName**</span><span class="sxs-lookup"><span data-stu-id="954a1-119">*Player6*.**GetMediaParameterName**</span></span>
-   <span data-ttu-id="954a1-120">*Player6*。**EntryCount**。</span><span class="sxs-lookup"><span data-stu-id="954a1-120">*Player6*.**EntryCount**.</span></span>

<span data-ttu-id="954a1-121">這些都提供有限的功能，可讓您流覽具有 .asx 副檔名的播放清單中繼檔，以及抓取播放清單中所包含專案的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="954a1-121">Together, these provide limited functionality for navigating a playlist metafile with an .asx file name extension and retrieving information about the entries contained in the playlist.</span></span>

<span data-ttu-id="954a1-122">Windows Media Player 7 引進了「媒體媒體櫃」。</span><span class="sxs-lookup"><span data-stu-id="954a1-122">Windows Media Player 7 introduced "Media Library."</span></span> <span data-ttu-id="954a1-123">程式庫可讓使用者組織其數位媒體內容，以及建立可從播放程式圖形化使用者介面管理的自訂播放清單。</span><span class="sxs-lookup"><span data-stu-id="954a1-123">The library allows users to organize their digital media content, as well as to create custom playlists that can be managed from the Player graphical user interface.</span></span> <span data-ttu-id="954a1-124">Windows Media Player 7 或更新版本的 ActiveX 控制項物件模型提供使用程式庫播放清單的支援，以及包含在副檔名為 .asx 之 Windows Media 中繼檔中的播放清單。</span><span class="sxs-lookup"><span data-stu-id="954a1-124">The Windows Media Player 7 or later ActiveX control object model provides support for working with library playlists, as well as playlists contained in Windows Media metafiles with an .asx file name extension.</span></span>

> [!Note]  
> <span data-ttu-id="954a1-125">基於安全性理由，使用者必須先授與程式庫的存取權限，您的程式才能操作其內容。</span><span class="sxs-lookup"><span data-stu-id="954a1-125">For security reasons, the user must grant access rights to the library before your program can manipulate its content.</span></span> <span data-ttu-id="954a1-126">只能透過 Windows Media Player 9 系列或更新版本的物件模型來要求和授與存取權限。</span><span class="sxs-lookup"><span data-stu-id="954a1-126">Access rights can only be requested and granted through the Windows Media Player 9 Series or later object model.</span></span> <span data-ttu-id="954a1-127">如需存取權限的詳細資訊，請參閱連結 [庫存取](library-access.md)。</span><span class="sxs-lookup"><span data-stu-id="954a1-127">For details about access rights, see [Library Access](library-access.md).</span></span>

 

<span data-ttu-id="954a1-128">Windows Media Player 7 或更新版本的物件模型包含處理播放清單的三個物件。</span><span class="sxs-lookup"><span data-stu-id="954a1-128">The Windows Media Player 7 or later object model includes three objects for handling playlists.</span></span> <span data-ttu-id="954a1-129">**PlaylistCollection** 物件提供組織播放清單的功能;它代表使用者程式庫中的整個播放清單集合。</span><span class="sxs-lookup"><span data-stu-id="954a1-129">The **PlaylistCollection** object provides functionality for organizing playlists; it represents the entire collection of playlists in the user's library.</span></span> <span data-ttu-id="954a1-130">**PlaylistArray** 物件提供一種方式，可讓您使用索引編號從 **PlaylistCollection** 物件取出特定播放清單;其中兩個 **PlaylistCollection** 物件方法會取出 **PlaylistArray** 物件。</span><span class="sxs-lookup"><span data-stu-id="954a1-130">The **PlaylistArray** object provides a way to retrieve a specific playlist from the **PlaylistCollection** object by using an index number; two of the **PlaylistCollection** object methods retrieve a **PlaylistArray** object.</span></span> <span data-ttu-id="954a1-131">**播放清單** 物件提供操作單一播放清單中包含之媒體專案所需的屬性和方法。</span><span class="sxs-lookup"><span data-stu-id="954a1-131">The **Playlist** object provides the properties and methods necessary to manipulate media items contained in a single playlist.</span></span>

<span data-ttu-id="954a1-132">例如，因為媒體櫃中的每個播放清單都有唯一的名稱，所以您可以使用 *PlaylistCollection* 從程式庫取出播放清單。**getByName** 方法：</span><span class="sxs-lookup"><span data-stu-id="954a1-132">As an example, since each playlist in the library has a unique name, you can retrieve a playlist from the library using the *PlaylistCollection*.**getByName** method:</span></span>


```C++
// Retrieve a PlaylistArray object that contains 
// exactly one Playlist object.
var plarray = WMP9.playlistCollection.getByName("MyPlaylist");

// Get the Playlist object from the PlaylistArray object.
// The Playlist object has index number zero.
var pl = plarray.item(0);

// Make the retrieved playlist the current playlist.
WMP9.currentPlaylist = pl;

```



<span data-ttu-id="954a1-133">您經常會想要使用目前的播放清單。</span><span class="sxs-lookup"><span data-stu-id="954a1-133">You will most frequently want to work with the current playlist.</span></span> <span data-ttu-id="954a1-134">雖然您可以使用數個播放清單物件，但 *播放* 程式只能抓取一個物件。**currentPlaylist** 屬性（在任何指定時間）： Windows Media Player 正在處理的屬性。</span><span class="sxs-lookup"><span data-stu-id="954a1-134">While it is possible to use several playlist objects, only one can be retrieved by the *Player*.**currentPlaylist** property at any given time: the one that Windows Media Player is processing at that moment.</span></span>

<span data-ttu-id="954a1-135">當 Windows Media Player 7 或更新版本播放副檔名為 .asx 的 Windows Media 中繼檔時，它會先建立 **播放清單** 物件。</span><span class="sxs-lookup"><span data-stu-id="954a1-135">When Windows Media Player 7 or later plays a Windows Media metafile with an .asx file name extension, it first creates a **Playlist** object.</span></span> <span data-ttu-id="954a1-136">接下來，它會以 .asx 播放清單中的資訊來填滿物件，然後將該 **播放** 清單物件放在目前的播放清單中。</span><span class="sxs-lookup"><span data-stu-id="954a1-136">Next, it fills the object with the information from the .asx playlist, and then makes that **Playlist** object the current playlist.</span></span> <span data-ttu-id="954a1-137">這表示您可以使用與 **播放清單** 物件相關聯的屬性和方法來操作 .asx 播放清單，就像處理文件庫中的播放清單一樣。</span><span class="sxs-lookup"><span data-stu-id="954a1-137">This means that you can use the properties and methods associated with the **Playlist** object to manipulate .asx playlists exactly as you would handle playlists in the library.</span></span> <span data-ttu-id="954a1-138">例如，若要使用6.4 版物件模型取出 .asx 播放清單中的專案數，您可以使用 *Player6*。**EntryCount** 屬性：</span><span class="sxs-lookup"><span data-stu-id="954a1-138">For instance, to retrieve the number of entries in an .asx playlist using the version 6.4 object model, you use the *Player6*.**EntryCount** property:</span></span>


```C++
var entrycount = WMP64.EntryCount;

```



<span data-ttu-id="954a1-139">使用 Windows Media Player 7 或更新版本的物件模型時，您會使用 *播放清單*。**count** 屬性：</span><span class="sxs-lookup"><span data-stu-id="954a1-139">When using the Windows Media Player 7 or later object model, you use the *Playlist*.**count** property:</span></span>


```C++
var entrycount = WMP9.currentPlaylist.count;

```



<span data-ttu-id="954a1-140">使用6.4 版的控制項時，您可以使用 *Player6*。**GetCurrentEntry** 方法，以取得 .asx 播放清單中目前專案的索引：</span><span class="sxs-lookup"><span data-stu-id="954a1-140">When using the version 6.4 control, you can use the *Player6*.**GetCurrentEntry** method to retrieve the index of the current entry in an .asx playlist:</span></span>


```C++
var entrynum = WMP64.GetCurrentEntry();

```



<span data-ttu-id="954a1-141">您可以在腳本中使用 Windows Media Player 7 或更新版本的物件模型，來達到相同的結果。</span><span class="sxs-lookup"><span data-stu-id="954a1-141">You can achieve the same result by using the Windows Media Player 7 or later object model in script.</span></span> <span data-ttu-id="954a1-142">下列 JScript 範例會比較目前媒體物件與播放清單中的每個專案。</span><span class="sxs-lookup"><span data-stu-id="954a1-142">The following JScript example compares the current media object to each item in the playlist.</span></span> <span data-ttu-id="954a1-143">*媒體*。**isIdentical** 會傳回 true，訊息方塊會顯示目前媒體專案的索引。</span><span class="sxs-lookup"><span data-stu-id="954a1-143">When *Media*.**isIdentical** returns true, a message box displays the index of the current media item.</span></span>


```C++
function matchit(){
// Store the current playlist object in a variable.
var pl = WMP9.currentPlaylist;

// Loop through the playlist one entry at a time.
  for (var i = 0; i < pl.count; i++){

   // Test whether the current media item matches 
   // the item in the playlist at the current loop index.
   if (WMP9.currentmedia.isIdentical(pl.item(i))){

       // They match, display the index.
       var message = "Current media at index: " + i;
       alert(message);

       // Exit the function, don't continue looping!
       return;
      }
  }
}

```



<span data-ttu-id="954a1-144">若要指定 .asx 播放清單中目前專案的索引，請使用 *Player6*。**SetCurrentEntry**。</span><span class="sxs-lookup"><span data-stu-id="954a1-144">To specify the index of the current entry in an .asx playlist, you use *Player6*.**SetCurrentEntry**.</span></span> <span data-ttu-id="954a1-145">版本6.4 中的播放清單專案索引從1開始，因此若要讓中繼檔播放清單中的第二個專案成為目前的專案，請使用下列語法：</span><span class="sxs-lookup"><span data-stu-id="954a1-145">Playlist entry indexes in version 6.4 start with 1, so to make the second entry in a metafile playlist the current one, use the following syntax:</span></span>


```C++
WMP6.SetCurrentEntry(2);

```



<span data-ttu-id="954a1-146">播放清單專案索引在 Windows Media Player 7 或更新版本中是以零為基礎;若要讓中繼檔播放清單中的第二個專案成為目前的專案，使用 Windows Media Player 7 或更新版本的物件模型時，請使用下列語法：</span><span class="sxs-lookup"><span data-stu-id="954a1-146">Playlist entry indexes are zero-based in Windows Media Player 7 or later; to make the second entry in a metafile playlist the current one, when using the Windows Media Player 7 or later object model, use the following syntax:</span></span>


```C++
WMP9.controls.currentItem = WMP9.currentPlaylist.item(1);

```



<span data-ttu-id="954a1-147">下列 JScript 範例會示範接受索引編號做為參數的函式，然後將對應至索引的播放清單專案設為目前的媒體專案：</span><span class="sxs-lookup"><span data-stu-id="954a1-147">The following JScript example demonstrates a function that accepts an index number as a parameter, and then makes the playlist entry that corresponds to the index the current media item:</span></span>


```C++
function setindex(idx){
// Store the current playlist in a variable.
var pl = WMP9.currentPlaylist;

// Get the first playlist entry.
var firstmedia = pl.item(0);

// Start the Player to allow navigation within the playlist.
WMP9.controls.playItem(firstmedia);

// Test whether idx is within a valid range.
   if (idx < pl.count && idx >= 0){

     // Set the currentItem to the desired playlist item.
     WMP9.controls.currentItem = pl.item(idx);

     // Display the name of the media item.
     alert(WMP9.currentMedia.name);
     return true;
 }

// The index is out of range, stop the Player, alert the user.
WMP9.controls.stop();
alert("Index out of range");
return false;
}

```



<span data-ttu-id="954a1-148">Windows Media 中繼檔可以包含自訂參數元素，您可以使用標記來指定這些專案 **<PARAM>** 。</span><span class="sxs-lookup"><span data-stu-id="954a1-148">Windows Media metafiles can contain custom parameter elements, which you specify by using the **<PARAM>** tag.</span></span> <span data-ttu-id="954a1-149">使用6.4 版物件模型時，您可以使用 *Player6* 來取出特定參數的名稱。**GetMediaParameterName** 方法。</span><span class="sxs-lookup"><span data-stu-id="954a1-149">When using the version 6.4 object model, you can retrieve the name of a particular parameter with the *Player6*.**GetMediaParameterName** method.</span></span> <span data-ttu-id="954a1-150">下列 JScript 範例會在 .asx 播放清單的第一個專案中，捕獲第一個參數的名稱：</span><span class="sxs-lookup"><span data-stu-id="954a1-150">The following JScript example retrieves the name of the first parameter in the first entry of an .asx playlist:</span></span>


```C++
var paramname = WMP6.GetMediaParameterName(1,1);

```



<span data-ttu-id="954a1-151">同樣地，您可以使用 *Player6* 來取出與參數相關聯的值。**GetMediaParameter**：</span><span class="sxs-lookup"><span data-stu-id="954a1-151">Similarly, you can retrieve the value associated with the parameter using *Player6*.**GetMediaParameter**:</span></span>


```C++
var paramvalue = WMP6.GetMediaParameter(1, paramname);

```



<span data-ttu-id="954a1-152">下列 JScript 範例會使用 Windows Media Player 7 或更新版本的物件模型，從 .asx 播放清單中的第一個專案取出參數名稱和值：</span><span class="sxs-lookup"><span data-stu-id="954a1-152">The following JScript example uses the Windows Media Player 7 or later object model to retrieve the parameter name and value from the first entry in an .asx playlist:</span></span>


```C++
function getattribute(){
// Store the first playlist entry as a Media object.
var firstmedia = WMP9.currentplaylist.item(0);

// Get the name of the first parameter in the object named firstmedia.
var attname = firstmedia.getAttributeName(0);

// Get the value of the first parameter in the object named firstmedia.
var attval = firstmedia.getItemInfo(attname);

// Display the information.
alert(attname + ": " + attval);
}

```



<span data-ttu-id="954a1-153">您可以使用 *PlaylistCollection*。將 .asx 播放清單新增至程式庫的 **importPlaylist** 方法。</span><span class="sxs-lookup"><span data-stu-id="954a1-153">You can use the *PlaylistCollection*.**importPlaylist** method to add an .asx playlist to the library.</span></span> <span data-ttu-id="954a1-154">匯入之後，中繼檔播放清單會變成程式庫播放清單，因此您可以使用所有屬性和方法來操作。</span><span class="sxs-lookup"><span data-stu-id="954a1-154">Once imported, the metafile playlist becomes a library playlist, so you can manipulate it using all the properties and methods at your disposal.</span></span> <span data-ttu-id="954a1-155">使用者必須授與程式庫的完整存取權限，您的應用程式才能使用 **importPlaylist** 方法。</span><span class="sxs-lookup"><span data-stu-id="954a1-155">The user must grant full access rights to the library for your application to be able to use the **importPlaylist** method.</span></span>

<span data-ttu-id="954a1-156">您可以使用 *PlaylistCollection*。**getByName** 以測試播放清單是否存在。</span><span class="sxs-lookup"><span data-stu-id="954a1-156">You can use *PlaylistCollection*.**getByName** to test whether a playlist exists.</span></span> <span data-ttu-id="954a1-157">這個方法一律會傳回有效的 **PlaylistArray** 物件。</span><span class="sxs-lookup"><span data-stu-id="954a1-157">This method always returns a valid **PlaylistArray** object.</span></span> <span data-ttu-id="954a1-158">如果取出的播放清單陣列只包含一個播放清單，則程式庫中會有該名稱的播放清單。</span><span class="sxs-lookup"><span data-stu-id="954a1-158">If the playlist array retrieved contains exactly one playlist, then there exists a playlist with that name in the library.</span></span> <span data-ttu-id="954a1-159">否則播放清單陣列將不會包含播放清單物件;這表示媒體櫃中沒有播放清單，並將名稱做為引數傳遞至 **getByName** 方法。</span><span class="sxs-lookup"><span data-stu-id="954a1-159">Otherwise, the playlist array will contain no playlist object; this means there is no playlist in the library with the name passed as an argument to the **getByName** method.</span></span> <span data-ttu-id="954a1-160">下列 JScript 範例會示範：</span><span class="sxs-lookup"><span data-stu-id="954a1-160">The following JScript example demonstrates this:</span></span>


```C++
// Specify an .asx playlist file.
WMP9.URL = "https://www.microsoft.com/someplaylist.asx";

// Open the playlist and start playing the content.
WMP9.controls.play();

// Store the current playlist object.
var pl = WMP9.currentPlaylist;

// Attempt to retrieve from the library 
// a playlist having the same name as the current playlist.
var plarray = WMP9.playlistCollection.getByName(pl.name);

// Test whether the PlaylistArray object, plarray, contains
// a Playlist object.
if (!plarray.count)
   
   // If plarray contains no playlist, then import 
   // the current one.
   WMP9.playlistCollection.importPlaylist(pl);
}

```



## <a name="related-topics"></a><span data-ttu-id="954a1-161">相關主題</span><span class="sxs-lookup"><span data-stu-id="954a1-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="954a1-162">**管理播放清單**</span><span class="sxs-lookup"><span data-stu-id="954a1-162">**Managing Playlists**</span></span>](managing-playlists.md)
</dt> <dt>

[<span data-ttu-id="954a1-163">**物件模型遷移指南**</span><span class="sxs-lookup"><span data-stu-id="954a1-163">**Object Model Migration Guide**</span></span>](object-model-migration-guide.md)
</dt> <dt>

[<span data-ttu-id="954a1-164">**播放清單物件**</span><span class="sxs-lookup"><span data-stu-id="954a1-164">**Playlist Object**</span></span>](playlist-object.md)
</dt> </dl>

 

 




