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
# <a name="playlists"></a>播放清單

Windows Media Player 6.4 ActiveX 控制項物件模型包含四種方法，以及一個用於處理 Windows Media 中繼檔播放清單的屬性：

-   *Player6*。**GetCurrentEntry**
-   *Player6*。**SetCurrentEntry**
-   *Player6*。**GetMediaParameter**
-   *Player6*。**GetMediaParameterName**
-   *Player6*。**EntryCount**。

這些都提供有限的功能，可讓您流覽具有 .asx 副檔名的播放清單中繼檔，以及抓取播放清單中所包含專案的相關資訊。

Windows Media Player 7 引進了「媒體媒體櫃」。 程式庫可讓使用者組織其數位媒體內容，以及建立可從播放程式圖形化使用者介面管理的自訂播放清單。 Windows Media Player 7 或更新版本的 ActiveX 控制項物件模型提供使用程式庫播放清單的支援，以及包含在副檔名為 .asx 之 Windows Media 中繼檔中的播放清單。

> [!Note]  
> 基於安全性理由，使用者必須先授與程式庫的存取權限，您的程式才能操作其內容。 只能透過 Windows Media Player 9 系列或更新版本的物件模型來要求和授與存取權限。 如需存取權限的詳細資訊，請參閱連結 [庫存取](library-access.md)。

 

Windows Media Player 7 或更新版本的物件模型包含處理播放清單的三個物件。 **PlaylistCollection** 物件提供組織播放清單的功能;它代表使用者程式庫中的整個播放清單集合。 **PlaylistArray** 物件提供一種方式，可讓您使用索引編號從 **PlaylistCollection** 物件取出特定播放清單;其中兩個 **PlaylistCollection** 物件方法會取出 **PlaylistArray** 物件。 **播放清單** 物件提供操作單一播放清單中包含之媒體專案所需的屬性和方法。

例如，因為媒體櫃中的每個播放清單都有唯一的名稱，所以您可以使用 *PlaylistCollection* 從程式庫取出播放清單。**getByName** 方法：


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



您經常會想要使用目前的播放清單。 雖然您可以使用數個播放清單物件，但 *播放* 程式只能抓取一個物件。**currentPlaylist** 屬性（在任何指定時間）： Windows Media Player 正在處理的屬性。

當 Windows Media Player 7 或更新版本播放副檔名為 .asx 的 Windows Media 中繼檔時，它會先建立 **播放清單** 物件。 接下來，它會以 .asx 播放清單中的資訊來填滿物件，然後將該 **播放** 清單物件放在目前的播放清單中。 這表示您可以使用與 **播放清單** 物件相關聯的屬性和方法來操作 .asx 播放清單，就像處理文件庫中的播放清單一樣。 例如，若要使用6.4 版物件模型取出 .asx 播放清單中的專案數，您可以使用 *Player6*。**EntryCount** 屬性：


```C++
var entrycount = WMP64.EntryCount;

```



使用 Windows Media Player 7 或更新版本的物件模型時，您會使用 *播放清單*。**count** 屬性：


```C++
var entrycount = WMP9.currentPlaylist.count;

```



使用6.4 版的控制項時，您可以使用 *Player6*。**GetCurrentEntry** 方法，以取得 .asx 播放清單中目前專案的索引：


```C++
var entrynum = WMP64.GetCurrentEntry();

```



您可以在腳本中使用 Windows Media Player 7 或更新版本的物件模型，來達到相同的結果。 下列 JScript 範例會比較目前媒體物件與播放清單中的每個專案。 *媒體*。**isIdentical** 會傳回 true，訊息方塊會顯示目前媒體專案的索引。


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



若要指定 .asx 播放清單中目前專案的索引，請使用 *Player6*。**SetCurrentEntry**。 版本6.4 中的播放清單專案索引從1開始，因此若要讓中繼檔播放清單中的第二個專案成為目前的專案，請使用下列語法：


```C++
WMP6.SetCurrentEntry(2);

```



播放清單專案索引在 Windows Media Player 7 或更新版本中是以零為基礎;若要讓中繼檔播放清單中的第二個專案成為目前的專案，使用 Windows Media Player 7 或更新版本的物件模型時，請使用下列語法：


```C++
WMP9.controls.currentItem = WMP9.currentPlaylist.item(1);

```



下列 JScript 範例會示範接受索引編號做為參數的函式，然後將對應至索引的播放清單專案設為目前的媒體專案：


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



Windows Media 中繼檔可以包含自訂參數元素，您可以使用標記來指定這些專案 **<PARAM>** 。 使用6.4 版物件模型時，您可以使用 *Player6* 來取出特定參數的名稱。**GetMediaParameterName** 方法。 下列 JScript 範例會在 .asx 播放清單的第一個專案中，捕獲第一個參數的名稱：


```C++
var paramname = WMP6.GetMediaParameterName(1,1);

```



同樣地，您可以使用 *Player6* 來取出與參數相關聯的值。**GetMediaParameter**：


```C++
var paramvalue = WMP6.GetMediaParameter(1, paramname);

```



下列 JScript 範例會使用 Windows Media Player 7 或更新版本的物件模型，從 .asx 播放清單中的第一個專案取出參數名稱和值：


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



您可以使用 *PlaylistCollection*。將 .asx 播放清單新增至程式庫的 **importPlaylist** 方法。 匯入之後，中繼檔播放清單會變成程式庫播放清單，因此您可以使用所有屬性和方法來操作。 使用者必須授與程式庫的完整存取權限，您的應用程式才能使用 **importPlaylist** 方法。

您可以使用 *PlaylistCollection*。**getByName** 以測試播放清單是否存在。 這個方法一律會傳回有效的 **PlaylistArray** 物件。 如果取出的播放清單陣列只包含一個播放清單，則程式庫中會有該名稱的播放清單。 否則播放清單陣列將不會包含播放清單物件;這表示媒體櫃中沒有播放清單，並將名稱做為引數傳遞至 **getByName** 方法。 下列 JScript 範例會示範：


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



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**管理播放清單**](managing-playlists.md)
</dt> <dt>

[**物件模型遷移指南**](object-model-migration-guide.md)
</dt> <dt>

[**播放清單物件**](playlist-object.md)
</dt> </dl>

 

 




