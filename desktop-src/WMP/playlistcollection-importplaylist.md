---
title: PlaylistCollection. importPlaylist 方法
description: ImportPlaylist 方法會將靜態播放清單新增至程式庫。 |PlaylistCollection. importPlaylist 方法
ms.assetid: 0611ba42-fd8f-4fb9-9fbb-809a82775c2a
keywords:
- importPlaylist 方法 Windows Media Player
- importPlaylist 方法 Windows Media Player，PlaylistCollection 類別
- PlaylistCollection 類別 Windows Media Player，importPlaylist 方法
topic_type:
- apiref
api_name:
- PlaylistCollection.importPlaylist
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 736e9afa17f571428fada48660726b606268796a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984112"
---
# <a name="playlistcollectionimportplaylist-method"></a>PlaylistCollection. importPlaylist 方法

**ImportPlaylist** 方法會將靜態播放清單新增至程式庫。

## <a name="syntax"></a>語法


```JScript
retVal = PlaylistCollection.importPlaylist(
  playlist
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*播放清單* \[在\]
</dt> <dd>

要加入的 **播放清單** 物件。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會傳回已加入的 **播放清單** 物件。

## <a name="remarks"></a>備註

未包含任何媒體專案的播放清單，無法使用此方法新增至程式庫。 若要在程式庫中建立空的播放清單，請使用 **[]** 方法。 然後，您可以使用 *播放清單* 來填滿媒體專案所產生的播放清單。**appendItem** 或 *播放清單*。**insertItem**。

如果您將此方法傳遞給自動播放清單，則查詢會執行一次，並將結果以靜態播放清單的形式新增至程式庫。 若要將自動播放清單新增至程式庫並保留其自動行為，請使用 *MediaCollection*。**加入**。 如需詳細資訊，請參閱 [靜態和自動播放清單](static-and-auto-playlists.md)。

若要使用此方法，需要有程式庫的完整存取權。 如需詳細資訊，請參閱連結 [庫存取](library-access.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本。<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**管理播放清單**](managing-playlists.md)
</dt> <dt>

[**MediaCollection 物件**](mediacollection-object.md)
</dt> <dt>

[**MediaCollection 新增**](mediacollection-add.md)
</dt> <dt>

[**播放清單。 appendItem**](playlist-appenditem.md)
</dt> <dt>

[**播放清單。 insertItem**](playlist-insertitem.md)
</dt> <dt>

[**PlaylistCollection 物件**](playlistcollection-object.md)
</dt> <dt>

[**PlaylistCollection. []**](playlistcollection-newplaylist.md)
</dt> <dt>

[**PlaylistCollection。移除**](playlistcollection-remove.md)
</dt> <dt>

[**設定. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**設定. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





