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
# <a name="playlists-and-media-items"></a>播放清單和媒體專案

播放清單是一組媒體專案。 **播放清單** 物件可以操控代表這些專案的 **媒體** 物件。

## <a name="retrieving-media-items"></a>正在抓取媒體專案

若為現有的播放清單，您可以閱讀 *播放清單*。**count** 屬性可判斷播放清單中有多少媒體專案，而且您可以使用 *播放清單* 來取得對應至特定專案之 **媒體** 物件的參考。**item** 屬性。

下列 c # 範例會捕獲特定媒體專案的物件參考。  (在本主題中，變數 *pList* 是 **播放清單** 物件的參考。 ) 


```C++
currMedia = pList.Item(0);

```



下列 c # 範例會抓取播放清單中所有媒體專案的名稱，並將它們放在名為 lstOutput 的 ListBox 中。


```C++
for (j=0; j < pList.count; j++)
{
    strItemName = pList.get_Item(j).name;
    lstOutput.Items.Add(strItemName);
}

```



## <a name="adding-items-to-a-playlist"></a>將專案新增至播放清單

您可以使用 *播放清單*，將媒體專案新增至播放清單的結尾或播放清單中的特定位置。**appendItem** 和 *播放清單*。**insertItem** 方法。

在本主題中， **Player** 物件是以下列方式定義：


```C++
AxWMPLib.AxWindowsMediaPlayer Player;
using WMPLib;

```



下列 c # 範例會示範這兩種技術，方法是將目前的媒體專案新增至名為 "BluesTest" 的播放清單，先在結尾，然後在播放清單的開頭。


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



當您使用 *PlaylistCollection* 建立新的空白播放清單時。**[]** 方法，您可以重複呼叫 *播放清單* 來將媒體專案加入其中。**appendItem** 方法。

## <a name="manipulating-media-items-in-a-playlist"></a>操作播放清單中的媒體專案

您可以使用 *播放清單* 來變更媒體專案在播放清單中的位置。**moveItem** 方法。 您可以依目前的索引來指定專案，然後指定新的索引。 下列 c # 範例會在播放清單中將專案從索引5移至索引0。


```C++
// Move the 6th item to the beginning
// of the specified playlist.
pList.moveItem(5, 0);

```



您可以使用 **播放清單** 來移除播放清單中的媒體專案。**removeItem** 方法。 請注意，如果移除的專案不是播放清單中的最後一個專案，後續專案的索引值就會變更。 下列 c # 範例會移除指定的專案。


```C++
// Remove the currently playing item from the
// specified playlist.
pList.removeItem(currMedia);

```



> [!Note]  
> 使用者可以在您的應用程式之外變更播放清單的內容。 當您操作播放清單中的專案時，您應該監視和處理 Windows Media Player 控制項的播放清單相關事件，以確保您的程式碼正常運作。 這些事件是 *Player*。**CurrentPlaylistChange** 和 *Player*。**PlaylistChange**。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**管理播放清單**](managing-playlists.md)
</dt> <dt>

[**媒體物件**](media-object.md)
</dt> <dt>

[**播放清單物件**](playlist-object.md)
</dt> </dl>

 

 




