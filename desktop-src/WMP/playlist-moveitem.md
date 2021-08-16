---
title: MoveItem 方法
description: MoveItem 方法會變更播放清單中專案的位置。
ms.assetid: 82a8de86-4419-48a7-89f8-f7b9084b51d4
keywords:
- moveItem 方法 Windows Media Player
- moveItem 方法 Windows Media Player，播放清單類別
- 播放清單類別 Windows Media Player，moveItem 方法
topic_type:
- apiref
api_name:
- Playlist.moveItem
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a725ae53e38d1903d31dc47a3362f90c29fb064e3a785b816de0d0b695998aee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117746849"
---
# <a name="playlistmoveitem-method"></a>MoveItem 方法

**MoveItem** 方法會變更播放清單中專案的位置。

## <a name="syntax"></a>語法


```JScript
Playlist.moveItem(
  oldIndex,
  newIndex
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*oldIndex* \[在\]
</dt> <dd>

包含舊索引的 (**長**) **數目**。

</dd> <dt>

*newIndex* \[在\]
</dt> <dd>

包含新索引的 (**長**) **數目**。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

儲存在程式庫中的播放清單可以在您的控制項之外變更。 請務必監視並處理所有適當的播放清單相關事件，讓播放清單中的專案順序不會意外變更。

若要使用此方法，需要有程式庫的完整存取權。 如需詳細資訊，請參閱連結 [庫存取](library-access.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本。<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**播放清單物件**](playlist-object.md)
</dt> <dt>

[**設定. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**設定. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





