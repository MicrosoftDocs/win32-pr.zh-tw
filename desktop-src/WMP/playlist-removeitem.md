---
title: RemoveItem 方法
description: RemoveItem 方法會從播放清單中移除指定的專案。
ms.assetid: 294ba4fb-967b-4a03-b0c5-6e9c15db3bff
keywords:
- removeItem 方法 Windows Media Player
- removeItem 方法 Windows Media Player，播放清單類別
- 播放清單類別 Windows Media Player，removeItem 方法
topic_type:
- apiref
api_name:
- Playlist.removeItem
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8a55fb45fa7ea8d172d76321d7c907fbedfd3f868448f1ad63e220ff8e69f9a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118336589"
---
# <a name="playlistremoveitem-method"></a>RemoveItem 方法

**RemoveItem** 方法會從播放清單中移除指定的專案。

## <a name="syntax"></a>語法


```JScript
Playlist.removeItem(
  item
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*專案* \[在\]
</dt> <dd>

要移除的 **媒體** 物件。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

如果移除的專案是目前播放的曲目 (*播放機*。**currentMedia**) ，播放會停止，且播放清單中的下一個專案會變成目前的播放清單。 如果沒有下一個專案，則會使用前一個專案，如果沒有其他專案，則會使用 [ *播放* 程式]。**currentMedia** 設定為 **Null**。

若要使用此方法，需要有程式庫的完整存取權。 如需詳細資訊，請參閱連結 [庫存取](library-access.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本。<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CurrentMedia**](player-currentmedia.md)
</dt> <dt>

[**播放清單物件**](playlist-object.md)
</dt> <dt>

[**播放清單。 insertItem**](playlist-insertitem.md)
</dt> <dt>

[**播放清單。專案**](playlist-item.md)
</dt> <dt>

[**設定. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**設定. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





