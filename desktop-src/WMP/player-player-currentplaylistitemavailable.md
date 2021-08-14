---
title: CurrentPlaylistItemAvailable 事件
description: 當目前的播放清單變成可用時，就會發生 CurrentPlaylistItemAvailable 事件。 |CurrentPlaylistItemAvailable 事件
ms.assetid: 4894e2fc-3464-413f-8abf-8b5e91899946
keywords:
- CurrentPlaylistItemAvailable 事件 Windows Media Player
- CurrentPlaylistItemAvailable 事件 Windows Media Player，Player 類別
- Player 類別 Windows Media Player，CurrentPlaylistItemAvailable 事件
topic_type:
- apiref
api_name:
- Player.CurrentPlaylistItemAvailable
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c4c2543f99d9bc645fa021d7dc5c94f66369b3c3151647dc4d575aab0a32f62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118338134"
---
# <a name="playercurrentplaylistitemavailable-event"></a>CurrentPlaylistItemAvailable 事件

當目前的播放清單變成可用時，就會發生 **CurrentPlaylistItemAvailable** 事件。

## <a name="syntax"></a>語法


```JScript
Player.CurrentPlaylistItemAvailable(
  bstrItemName
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*bstrItemName* 
</dt> <dd>

包含目前播放清單專案名稱的 **字串**。

</dd> </dl>

## <a name="return-value"></a>傳回值

此事件不會傳回值。

## <a name="remarks"></a>備註

目前播放清單的名稱可以用來使用 *PlaylistCollection* 來取出對應的 **播放清單** 物件。**getByName** 方法。

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

[**播放清單物件**](playlist-object.md)
</dt> <dt>

[**PlaylistCollection.getByName**](playlistcollection-getbyname.md)
</dt> </dl>

 

 





