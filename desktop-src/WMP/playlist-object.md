---
title: 播放清單物件
description: 播放清單物件提供一種方式，可讓您使用下列屬性和方法，在清單中組織媒體專案以方便操作。
ms.assetid: c2d2f265-b207-4b82-bb76-aee467f00659
keywords:
- 播放清單物件 Windows Media Player
topic_type:
- apiref
api_name:
- Playlist Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d517e13f8da103b1f9cee9498cce58a62eaf6462
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104022248"
---
# <a name="playlist-object"></a>播放清單物件

**播放** 清單物件提供一種方式，可讓您使用下列屬性和方法，在清單中組織媒體專案以方便操作。

**播放清單** 物件支援下列屬性。



| 屬性                                      | 描述                                                      |
|-----------------------------------------------|------------------------------------------------------------------|
| [attributeCount](playlist-attributecount.md) | 捕獲與播放清單相關聯的屬性數目。 |
| [attributeName](playlist-attributename.md)   | 抓取索引所指定之屬性的名稱。        |
| [計數](playlist-count.md)                   | 捕獲播放清單中的專案數。                   |
| [name](playlist-name.md)                     | 指定或抓取播放清單的名稱。                 |



 

**播放清單** 物件支援下列方法。



| 方法                                  | 描述                                                                                            |
|-----------------------------------------|--------------------------------------------------------------------------------------------------------|
| [appendItem](playlist-appenditem.md)   | 將媒體專案加入至播放清單的結尾。                                                          |
| **清除**                               | 保留供未來使用。                                                                               |
| [getItemInfo](playlist-getiteminfo.md) | 捕獲播放清單屬性的值。                                                           |
| [insertItem](playlist-insertitem.md)   | 將媒體專案插入播放清單中指定的位置。                                      |
| [isIdentical](playlist-isidentical.md) | 抓取值，指出提供的播放清單物件是否與目前的 **播放清單** 物件相同。 |
| [item](playlist-item.md)               | 抓取位於指定之索引處的媒體專案。                                                       |
| [moveItem](playlist-moveitem.md)       | 變更播放清單中專案的位置。                                                       |
| [removeItem](playlist-removeitem.md)   | 從播放清單中移除指定的專案。                                                          |
| [setItemInfo](playlist-setiteminfo.md) | 指定播放清單屬性的值。                                                           |



 

**播放清單** 物件是透過下列屬性和方法來存取。



| Object                                              | 屬性或方法                                                                                                                                                                                                                                                                 |
|-----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [光碟](cdrom-object.md)                           | [播放清單](cdrom-playlist.md)                                                                                                                                                                                                                                                     |
| [MediaCollection](mediacollection-object.md)       | [getAll](mediacollection-getall.md)、 [getByAlbum](mediacollection-getbyalbum.md)、 [getByAttribute](mediacollection-getbyattribute.md)、 [getByAuthor](mediacollection-getbyauthor.md)、 [getByGenre](mediacollection-getbygenre.md)、 [getByName](mediacollection-getbyname.md) |
| [球員](player-object.md)                         | [currentPlaylist](player-currentplaylist.md)、 [[]](player-newplaylist.md)                                                                                                                                                                                               |
| [PlaylistArray](playlistarray-object.md)           | [item](playlistarray-item.md)                                                                                                                                                                                                                                                     |
| [PlaylistCollection](playlistcollection-object.md) | [[]](playlistcollection-newplaylist.md)                                                                                                                                                                                                                                  |



 

因為這是最常見的存取方式，也就是 *播放機*。**currentPlaylist** 是用於參考語法區段中的說明用途。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**腳本的物件模型參考**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




