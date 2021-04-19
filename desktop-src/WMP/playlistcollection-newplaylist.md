---
title: PlaylistCollection. [] 方法
description: '[] 方法會在文件庫中建立新的播放清單。'
ms.assetid: 428b5779-4dc0-466b-9834-6b2c43324013
keywords:
- '[] 方法 Windows Media Player'
- '[] 方法 Windows Media Player，PlaylistCollection 類別'
- PlaylistCollection 類別 Windows Media Player，[] 方法
topic_type:
- apiref
api_name:
- PlaylistCollection.newPlaylist
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d94c25a8dfe6f1eb7c4dac40dd644433a5f0d7e6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991156"
---
# <a name="playlistcollectionnewplaylist-method"></a>PlaylistCollection. [] 方法

**[]** 方法會在文件庫中建立新的播放清單。

## <a name="syntax"></a>語法


```JScript
retVal = PlaylistCollection.newPlaylist(
  name
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*名稱* \[在\]
</dt> <dd>

包含要建立之播放清單名稱的 **字串**。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會傳回 **播放清單** 物件。

## <a name="remarks"></a>備註

這個方法會在文件庫中建立空的播放清單。 若要以媒體專案填滿播放清單，請使用 *播放清單*。**appendItem** 或 *播放清單*。**insertItem**。

程式庫中允許有多個具有相同名稱的播放清單。 若要避免使用這個方法建立重複的播放清單名稱，請使用 **getByName** 和 *PlaylistArray*。**計數** ，以判斷具有特定名稱的播放清單是否已存在。

播放清單名稱中不允許前置和尾端空格，並且會自動從指定給 *name* 參數的值中移除。

若要使用此方法，需要有程式庫的完整存取權。 如需詳細資訊，請參閱連結 [庫存取](library-access.md)。

## <a name="examples"></a>範例

下列 JScript 範例會建立名為 "ThreeList" 的新空白播放清單。 使用 ID = "Player" 建立 **player** 物件。


```JScript
//Add a new empty playlist, named ThreeList, to the playlist collection.
var NewList = Player.playlistCollection.newPlaylist("ThreeList");

```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本。<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MediaCollection 新增**](mediacollection-add.md)
</dt> <dt>

[**播放清單。 appendItem**](playlist-appenditem.md)
</dt> <dt>

[**播放清單。 insertItem**](playlist-insertitem.md)
</dt> <dt>

[**PlaylistArray 計數**](playlistarray-count.md)
</dt> <dt>

[**PlaylistCollection 物件**](playlistcollection-object.md)
</dt> <dt>

[**PlaylistCollection.getByName**](playlistcollection-getbyname.md)
</dt> <dt>

[**PlaylistCollection.importPlaylist**](playlistcollection-importplaylist.md)
</dt> <dt>

[**PlaylistCollection。移除**](playlistcollection-remove.md)
</dt> <dt>

[**設定. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**設定. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





