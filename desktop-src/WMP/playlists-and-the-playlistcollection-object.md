---
title: 播放清單和 PlaylistCollection 物件
description: 播放清單和 PlaylistCollection 物件
ms.assetid: 63c8955b-34ad-447b-b734-657207bcecbb
keywords:
- Windows Media Player，播放清單
- Windows Media Player 物件模型，播放清單
- 物件模型，播放清單
- Windows Media Player行動裝置、播放清單
- Windows Media Player ActiveX 控制項、播放清單
- Windows Media Player行動 ActiveX 控制項、播放清單
- ActiveX 控制項，播放清單
- 播放清單，PlaylistCollection 物件
- 中繼檔播放清單，PlaylistCollection 物件
- Windows媒體中繼檔播放清單，PlaylistCollection 物件
- PlaylistCollection 物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82e57b11f29c259b3e4174f53fe4ef75d688475d8a42df595f89a0e72fe6f06b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119862028"
---
# <a name="playlists-and-the-playlistcollection-object"></a>播放清單和 PlaylistCollection 物件

**PlaylistCollection** 物件可讓您存取媒體櫃中的播放清單，並提供從中繼檔建立新的空白播放清單和新播放清單的方法。

## <a name="working-with-existing-playlists"></a>使用現有的播放清單

*PlaylistCollection*。**getAll** 和 *PlaylistCollection*。**getByName** 方法都會傳回 **PlaylistArray** 物件，其中可能包含多個播放清單。

*PlaylistCollection*。**getAll** 方法會傳回程式庫中所有現有的播放清單。 例如，您可以呼叫這個方法，然後取出 **PlaylistArray** 物件中的播放清單，以判斷是否已使用指定的播放清單名稱，或將所有的播放清單顯示給使用者。 [播放清單屬性](playlist-attributes.md)中的範例程式碼會使用 **getAll** 方法。

*PlaylistCollection*。**getByName** 方法會傳回具有指定名稱的所有播放清單。 您可以使用這個方法，分別處理每個播放清單。

您也可以使用 **getByName** 方法，依名稱抓取唯一的播放清單。 在此情況下， **PlaylistArray** 物件只有一個元素。 下列 c # 範例示範這項技巧。


```C++
IWMPPlaylistArray PlayListArray;
IWMPPlaylist Playlist;
// Store the playlist named "BluesTest" in the array
PlayListArray = Player.playlistCollection.getByName("BluesTest");
// Retrieve the first playlist in the collection.
Playlist = PlaylistArray.Item(0);

```



## <a name="working-with-new-playlists"></a>使用新的播放清單

您可以使用 *PlaylistCollection*。用來建立新的空白播放清單的 **[]** 方法。 方法會傳回新 **播放清單** 物件的參考。 然後您就可以呼叫 *播放清單*。將媒體專案新增至播放清單的 **appendItem** 方法。

您也可以根據播放清單中繼檔建立新的播放清單。 首先，將播放清單的名稱和中繼檔的路徑傳遞給 *播放機*。**[]** 方法。 該方法會傳回新 **播放清單** 物件的參考。 然後，將新的 **播放清單** 物件傳遞給 *PlaylistCollection*。**importPlaylist** 方法，將它新增至程式庫。

請注意 *PlaylistCollection* 之間的差異。**[]** 方法和 *播放機*。**[]** 方法。 **PlaylistCollection** 方法會建立新的空白播放清單，並將其新增至程式庫。 **Player** 方法會建立新填入的 **播放清單** 物件，但不會將它新增至程式庫。

在本主題中， **Player** 物件是以下列方式定義：


```C++
AxWMPLib.AxWindowsMediaPlayer Player;
using WMPLib;

```



下列 c # 範例示範如何從中繼檔匯入播放清單。 *StrPListName* 引數指定新播放清單的名稱。 *StrMetaFileName* 會指定要匯入播放清單的中繼檔名稱。


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



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**管理播放清單**](managing-playlists.md)
</dt> <dt>

[**[]**](player-newplaylist.md)
</dt> <dt>

[**播放清單。 appendItem**](playlist-appenditem.md)
</dt> <dt>

[**PlaylistArray 物件**](playlistarray-object.md)
</dt> <dt>

[**PlaylistCollection 物件**](playlistcollection-object.md)
</dt> <dt>

[**播放清單和媒體專案**](playlists-and-media-items.md)
</dt> </dl>

 

 




