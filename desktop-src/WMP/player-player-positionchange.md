---
title: PositionChange 事件
description: 當媒體專案目前的位置已變更時，就會發生 PositionChange 事件。
ms.assetid: 0561c58c-da5d-438e-adf8-2472405c6b9e
keywords:
- PositionChange 事件 Windows Media Player
- PositionChange 事件 Windows Media Player，Player 類別
- Player 類別 Windows Media Player，PositionChange 事件
topic_type:
- apiref
api_name:
- Player.PositionChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0ab7f64d6f5c4a081b8a81a14e3fcb353e1478e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999219"
---
# <a name="playerpositionchange-event"></a>PositionChange 事件

當媒體專案目前的位置已變更時，就會發生 **PositionChange** 事件。

## <a name="syntax"></a>語法


```JScript
Player.PositionChange(
  oldPosition,
  newPosition
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*oldPosition* 
</dt> <dd>

指定舊位置)  (**雙精度浮** 點數。

</dd> <dt>

*newPosition* 
</dt> <dd>

) 指定新位置 (**雙精度浮****點數**。

</dd> </dl>

## <a name="return-value"></a>傳回值

此事件不會傳回值。

## <a name="remarks"></a>備註

此事件不會在播放期間定期引發。 只有在主動變更播放媒體專案目前的位置，例如使用者移動搜尋控制碼或指定 *控制項* 值的程式碼時，才會發生此問題。**currentPosition**。

事件參數的值是由 Windows Media Player 指定，而且可以使用指定的參數名稱，存取或傳遞至匯入之 JScript 檔案中的方法。 此參數名稱的類型必須完全如所示，包括大小寫。

**Windows Media Player 10** 行動裝置版：不支援這個事件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本。<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Player 物件**](player-object.md)
</dt> </dl>

 

 





