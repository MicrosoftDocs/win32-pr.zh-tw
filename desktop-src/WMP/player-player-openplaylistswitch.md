---
title: OpenPlaylistSwitch 事件
description: 當 DVD 上的標題開始播放時，就會發生 OpenPlaylistSwitch 事件。 |OpenPlaylistSwitch 事件
ms.assetid: 97d69716-602f-4522-b743-83f2dbc852a2
keywords:
- OpenPlaylistSwitch 事件 Windows Media Player
- OpenPlaylistSwitch 事件 Windows Media Player，Player 類別
- Player 類別 Windows Media Player，OpenPlaylistSwitch 事件
topic_type:
- apiref
api_name:
- Player.OpenPlaylistSwitch
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d35d4568356365cc9276c13ea33f866e937da1a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992156"
---
# <a name="playeropenplaylistswitch-event"></a>OpenPlaylistSwitch 事件

當 DVD 上的標題開始播放時，就會發生 **OpenPlaylistSwitch** 事件。

## <a name="syntax"></a>語法


```JScript
Player.OpenPlaylistSwitch(
  pItem
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*pItem* 
</dt> <dd>

代表標題的 **播放清單** 物件。

</dd> </dl>

## <a name="return-value"></a>傳回值

此事件不會傳回值。

## <a name="remarks"></a>備註

事件參數的值是由 Windows Media Player 指定，而且可以使用指定的參數名稱，存取或傳遞至匯入之 JScript 檔案中的方法。 此參數名稱的類型必須完全如所示，包括大小寫。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | 適用于 Windows XP 或更新版本的 Windows Media Player。<br/>                           |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Player 物件**](player-object.md)
</dt> </dl>

 

 





