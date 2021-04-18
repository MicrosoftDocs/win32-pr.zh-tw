---
title: PlaylistCollection 物件
description: PlaylistCollection 物件提供一種方式來組織播放清單。
ms.assetid: 9ea61954-d185-4a77-9016-4d58340a96fc
keywords:
- PlaylistCollection 物件 Windows Media Player
topic_type:
- apiref
api_name:
- PlaylistCollection Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2266537e0df9fc0ba5527784c254b27313d636d3
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "106965615"
---
# <a name="playlistcollection-object"></a>PlaylistCollection 物件

**PlaylistCollection** 物件提供一種方式來組織播放清單。

**PlaylistCollection** 物件支援下列方法。



| 方法                                                  | 描述                                                                                                              |
|---------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [getAll](playlistcollection-getall.md)                 | 抓取 [PlaylistArray](playlistarray-object.md) 物件，其中包含文件庫中的所有播放清單。                |
| [getByName](playlistcollection-getbyname.md)           | 抓取 [PlaylistArray](playlistarray-object.md) 物件，其中包含具有指定名稱的播放清單（如果有的話）。 |
| [importPlaylist](playlistcollection-importplaylist.md) | 將靜態播放清單新增至程式庫。                                                                                   |
| [isDeleted](playlistcollection-isdeleted.md)           | 抓取值，指出指定的播放清單是否在 [刪除的專案] 資料夾中。                              |
| [[]](playlistcollection-newplaylist.md)       | 在文件庫中建立新的播放清單。                                                                                   |
| [remove](playlistcollection-remove.md)                 | 從媒體櫃移除播放清單。                                                                                     |
| [setDeleted](playlistcollection-setdeleted.md)         | 移動播放清單至 [刪除的專案] 資料夾。                                                                            |



 

**PlaylistCollection** 物件是透過下列屬性來存取。



| Object                      | 屬性                                            |
|-----------------------------|-----------------------------------------------------|
| [球員](player-object.md) | [playlistCollection](player-playlistcollection.md) |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**腳本的物件模型參考**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




