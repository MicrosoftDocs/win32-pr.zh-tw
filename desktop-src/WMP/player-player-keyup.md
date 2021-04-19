---
title: Player. KeyUp 事件
description: 當釋放索引鍵時，就會發生 KeyUp 事件。 |Player. KeyUp 事件
ms.assetid: 8b624374-403f-4d41-8481-5e94cee70861
keywords:
- KeyUp 事件 Windows Media Player
- KeyUp 事件 Windows Media Player、Player 類別
- Player 類別 Windows Media Player、KeyUp 事件
topic_type:
- apiref
api_name:
- Player.KeyUp
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f06e9b77871e9f62d46bdfa223bfa40b87feaf06
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994633"
---
# <a name="playerkeyup-event"></a>Player. KeyUp 事件

當釋放索引鍵時，就會發生 **KeyUp** 事件。

## <a name="syntax"></a>語法


```JScript
Player.KeyUp(
  nKeyCode,
  nShiftState
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*nKeyCode* 
</dt> <dd>

 (**int**) 指定按下哪個實體索引鍵的 **數目**。 如需可能的值，請參閱 [Player. KeyDown 事件](player-player-keydown.md)。

</dd> <dt>

*nShiftState* 
</dt> <dd>

**Number** (**int**) 指定具有最少有效位數的位位（對應至 SHIFT 鍵 (BIT 0) 、CTRL 鍵 (位 1) ，以及 ALT 鍵 (位 2) ）。 這些位會分別對應至值1、2和4。 Shift 引數表示這些索引鍵的狀態。 您可以設定部分、全部或全部的位，表示未按下部分、全部或未按下任何鍵。

</dd> </dl>

## <a name="return-value"></a>傳回值

此事件不會傳回值。

## <a name="remarks"></a>備註

事件參數的值是由 Windows Media Player 指定，而且可以使用指定的參數名稱，存取或傳遞至匯入之 JScript 檔案中的方法。 此參數名稱的類型必須完全如所示，包括大小寫。

**Windows Media Player 10** 行動裝置版：不支援這個事件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player  9  系列或更新的版本。<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Player 物件**](player-object.md)
</dt> </dl>

 

 





