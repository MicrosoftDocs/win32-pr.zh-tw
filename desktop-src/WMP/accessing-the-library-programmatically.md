---
title: 以程式設計方式存取程式庫
description: 以程式設計方式存取程式庫
ms.assetid: f48fbb49-5b79-4a78-af72-8509c460a149
keywords:
- Windows Media Player，程式庫
- Windows Media Player 物件模型，程式庫
- 物件模型，程式庫
- Windows Media Player ActiveX 控制項、物件模型的程式庫
- ActiveX 控制項，物件模型的程式庫
- Windows Media PlayerMobile ActiveX 控制項，物件模型的程式庫
- Windows Media Player適用于物件模型的 Mobile、library
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
ms.openlocfilehash: 6b575d1ed265d5c8e65beab9cc8e937b3639d8547867dacf473b2db21fe99198
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119619428"
---
# <a name="accessing-the-library-programmatically"></a>以程式設計方式存取程式庫

在程式碼中，程式庫是以 **MediaCollection** 物件代表， (或 **IWMPMediaCollection** 介面) 。 媒體專案會以 **媒體** 物件 (或由 **IWMPMedia** 介面) 來表示。 播放清單專案會以 **播放清單** 物件 (或由 **IWMPPlaylist** 介面) 表示。 為了簡單起見，此區段只會參考物件名稱（如果可能的話）。

您可以使用 **MediaCollection** 物件來處理媒體專案和播放清單。 此程式庫也會公開 **PlaylistCollection** 物件 (或 **IWMPPlaylistCollection** 介面) ，其提供使用播放清單的特定功能。 大部分的情況下， **MediaCollection** 物件會提供您所需的功能，即使使用播放清單也一樣。 如需使用媒體專案的詳細資訊，請參閱 [管理媒體專案](managing-media-items.md)。 如需使用播放清單的詳細資訊，請參閱 [管理播放清單](managing-playlists.md)。

## <a name="adding-media-items-to-the-library"></a>將媒體專案新增至程式庫

將數位媒體內容新增至媒體櫃很簡單。 只要呼叫 MediaCollection，就可以 [將](mediacollection-add.md) 路徑當作引數提供給媒體檔案。

## <a name="retrieving-media-items-from-the-library"></a>從程式庫中取出媒體專案

當您從媒體櫃取出媒體專案時，您真正取得的是播放清單。 即使您預期只抓取一個媒體專案，您仍會收到包含單一專案的 **播放清單** 物件，該專案會與索引零相關聯。 例如，如果您想要取出代表名為 "Jeanne" 之歌曲的 **媒體** 物件，您可以使用下列 JScript 程式碼：


```C++
// Retrieve media named Jeanne from the library.
var playlist = player.mediaCollection.getByName("Jeanne");

```



上述程式碼會抓取播放清單，其中包含名稱為 "Jeanne" 的所有媒體專案作為標題。 在此範例中，假設您知道媒體櫃中只有一個該名稱的歌曲 (請注意，程式庫支援多個具有相同名稱) 的歌曲。 這表示您可以預期您抓取的播放清單中的專案計數等於1，而媒體專案會以索引零表示。 下列範例程式碼會繼續上一個範例，以示範如何使用 [播放清單專案](playlist-item.md) 方法，從播放清單取出媒體專案。


```C++
// Retrieve the individual media item from the playlist.
var media = playlist.item(0);

```



如需有關從播放清單中取得媒體專案的詳細資訊，請參閱《[播放程式控制指南》](player-control-guide.md)中的[播放清單和媒體專案](playlists-and-media-items.md)。

## <a name="retrieving-metadata-from-a-media-item"></a>從媒體專案中取出中繼資料

取得 **媒體** 物件之後，您可以讀取與內容相關聯的屬性值。 在最簡單的情況下，您可能只想要知道單一值，例如執行音樂播放軌的演出者名稱。下列 JScript 範例示範如何使用[getItemInfo](media-getiteminfo.md)方法，從上一個範例中取出的媒體取出演出者的名稱：


```C++
// Retrieve the artist name string.
var author = media.getItemInfo("Artist");

```



媒體專案可以有許多不同的屬性，而且使用中繼資料並不一定像前一個範例所示的簡單案例一樣簡單。 例如，某些屬性可包含多個值，或具有多個語言的值。 如需使用中繼資料的詳細資訊，請參閱 [媒體專案屬性](media-item-attributes.md)。 如需各種屬性、其意義及檔案類型支援的詳細資訊，請參閱 [屬性參考](attribute-reference.md)。

## <a name="removing-media-items-from-the-library"></a>從媒體櫃移除媒體專案

從媒體櫃移除數位媒體內容也很簡單。 只要呼叫 **MediaCollection**，就會提供代表專案的 **媒體** 物件做為第一個引數，並將值 **true** 做為第二個引數。 下列 JScript 範例會從程式庫移除先前範例) 中所抓取的名為 Jeanne 的檔案 (：


```C++
// Remove Jeanne from the library.
playst.mediaCollection.remove(media, true);

```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**關於程式庫**](about-the-library.md)
</dt> <dt>

[**關於 MediaCollection 和 Media 物件**](about-the-mediacollection-and-media-objects.md)
</dt> <dt>

[**關於播放清單、PlaylistCollection 和 PlaylistArray 物件**](about-the-playlist--playlistcollection--and-playlistarray-objects.md)
</dt> <dt>

[**使用程式庫**](working-with-the-library.md)
</dt> </dl>

 

 




