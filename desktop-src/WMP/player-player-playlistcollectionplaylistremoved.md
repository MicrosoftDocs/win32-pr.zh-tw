---
title: PlaylistCollectionPlaylistRemoved 事件
description: 從播放清單集合中移除播放清單時，就會發生 PlaylistCollectionPlaylistRemoved 事件。 |PlaylistCollectionPlaylistRemoved 事件
ms.assetid: 2405be98-b4c2-4b4e-bea6-0c48a3e26f18
keywords:
- PlaylistCollectionPlaylistRemoved 事件 Windows Media Player
- PlaylistCollectionPlaylistRemoved 事件 Windows Media Player，Player 類別
- Player 類別 Windows Media Player，PlaylistCollectionPlaylistRemoved 事件
topic_type:
- apiref
api_name:
- Player.PlaylistCollectionPlaylistRemoved
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 456f7598b9e1f1d2c2a6e76e58a0b06142980835c3c6d71d9ab10c2230ac386f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118337972"
---
# <a name="playerplaylistcollectionplaylistremoved-event"></a>PlaylistCollectionPlaylistRemoved 事件

從播放清單集合中移除播放清單時，就會發生 **PlaylistCollectionPlaylistRemoved** 事件。

## <a name="syntax"></a>語法


```JScript
Player.PlaylistCollectionPlaylistRemoved(
  bstrPlaylistName
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*bstrPlaylistName* 
</dt> <dd>

**字串** ，指定已移除之播放清單的名稱。

</dd> </dl>

## <a name="return-value"></a>傳回值

此事件不會傳回值。

## <a name="remarks"></a>備註

事件參數的值是由 Windows Media Player 指定，而且可以使用指定的參數名稱，存取或傳遞至匯入 JScript 檔案中的方法。 此參數名稱的類型必須完全如所示，包括大小寫。

**Windows Media Player 10** 行動裝置版：不支援這個事件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本。<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Player 物件**](player-object.md)
</dt> <dt>

[**PlaylistCollection.getByName**](playlistcollection-getbyname.md)
</dt> </dl>

 

 





