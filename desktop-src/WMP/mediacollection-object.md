---
title: MediaCollection 物件
description: MediaCollection 物件提供一種方式來組織大型的媒體專案集合。 您可以查詢它，以自動產生播放清單。
ms.assetid: afcb2c51-3ecb-4529-8f3e-56aa6d0ec2b4
keywords:
- MediaCollection 物件 Windows Media Player
topic_type:
- apiref
api_name:
- MediaCollection Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8e529bec203b836f1f1022793a18320a7612cb242de58407ddb998c7410a47cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996248"
---
# <a name="mediacollection-object"></a>MediaCollection 物件

**MediaCollection** 物件提供一種方式來組織大型的媒體專案集合。 您可以查詢它，以自動產生播放清單。

**MediaCollection** 物件支援下列方法。



| 方法                                                                           | 描述                                                                                                                                                    |
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [add](mediacollection-add.md)                                                   | 將新的媒體專案或播放清單新增至程式庫。                                                                                                              |
| [createQuery](mediacollection-createquery.md)                                   | 建立新的 [查詢](query-object.md) 物件。                                                                                                                |
| [getAll](mediacollection-getall.md)                                             | 抓取包含媒體櫃中所有媒體專案的 [播放清單](playlist-object.md) 物件。                                                                  |
| [getAttributeStringCollection](mediacollection-getattributestringcollection.md) | 抓取 [StringCollection](stringcollection-object.md) 物件，代表指定之媒體類型內指定之屬性的所有值集。 |
| [getByAlbum](mediacollection-getbyalbum.md)                                     | 從指定的專輯抓取包含媒體專案的 [播放清單](playlist-object.md) 物件。                                                            |
| [getByAttribute](mediacollection-getbyattribute.md)                             | 抓取 [播放清單](playlist-object.md) 物件，其中包含具有指定之屬性的媒體專案具有指定的值。                             |
| [getByAttributeAndMediaType](mediacollection-getbyattributeandmediatype.md)     | 抓取包含具有指定屬性和媒體類型之[媒體](media-object.md)物件的[播放清單](playlist-object.md)物件。                 |
| [getByAuthor](mediacollection-getbyauthor.md)                                   | 依指定的作者，抓取包含媒體專案的 [播放清單](playlist-object.md) 物件。                                                             |
| [getByGenre](mediacollection-getbygenre.md)                                     | 抓取包含具有指定類型之媒體專案的 [播放清單](playlist-object.md) 物件。                                                            |
| [getByName](mediacollection-getbyname.md)                                       | 抓取包含具有指定名稱之媒體專案的 [播放清單](playlist-object.md) 物件。                                                             |
| [getMediaAtom](mediacollection-getmediaatom.md)                                 | 抓取可用屬性集合中指定的屬性所在的索引。                                                              |
| [getPlaylistByQuery](mediacollection-getplaylistbyquery.md)                     | 抓取包含符合查詢準則之[媒體](media-object.md)物件的[播放清單](playlist-object.md)物件。                               |
| [getStringCollectionByQuery](mediacollection-getstringcollectionbyquery.md)     | 抓取 [StringCollection](stringcollection-object.md) 物件，其中包含符合查詢準則的字串。                                         |
| [isDeleted](mediacollection-isdeleted.md)                                       | 抓取值，指出指定的媒體專案是否在 [刪除的專案] 資料夾中。                                                                  |
| [remove](mediacollection-remove.md)                                             | 從媒體集合中移除專案。                                                                                                                     |
| [setDeleted](mediacollection-setdeleted.md)                                     | 將指定的媒體專案移到 [刪除的專案] 資料夾。                                                                                                    |



 

**MediaCollection** 物件是透過下列屬性來存取。



| Object                      | 屬性                                      |
|-----------------------------|-----------------------------------------------|
| [球員](player-object.md) | [mediaCollection](player-mediacollection.md) |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**腳本的物件模型參考**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




