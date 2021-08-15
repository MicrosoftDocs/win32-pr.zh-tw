---
title: Player. MouseMove 事件
description: 移動滑鼠指標時，就會發生 MouseMove 事件。 |Player. MouseMove 事件
ms.assetid: 026928a3-25a6-4e67-837a-df71c05e49ee
keywords:
- MouseMove 事件 Windows Media Player
- MouseMove 事件 Windows Media Player、Player 類別
- Player 類別 Windows Media Player，MouseMove 事件
topic_type:
- apiref
api_name:
- Player.MouseMove
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb864e2a8bf686bd39f2d44ba8f5558516d72034f606579a79c76a5d86ab3990
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118338095"
---
# <a name="playermousemove-event"></a>Player. MouseMove 事件

移動滑鼠指標時，就會發生 **MouseMove** 事件。

## <a name="syntax"></a>語法


```JScript
Player.MouseMove(
  nButton,
  nShiftState,
  fX,
  fY
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*nButton* 
</dt> <dd>

**Number** (**int**) 指定位的位位，其位對應于左按鈕 (位 0) ，右按鈕 (位 1) ，中間按鈕 (位 2) 。 這些位會分別對應至值1、2和4。 您可以設定部分、全部或全部的位，表示未按下部分、全部或所有按鈕。

</dd> <dt>

*nShiftState* 
</dt> <dd>

**Number** (**int**) 指定具有最少有效位數的位位（對應至 SHIFT 鍵 (BIT 0) 、CTRL 鍵 (位 1) ，以及 ALT 鍵 (位 2) ）。 這些位會分別對應至值1、2和4。 Shift 引數表示這些索引鍵的狀態。 您可以設定部分、全部或全部的位，表示未按下部分、全部或未按下任何鍵。

</dd> <dt>

*外匯* 
</dt> <dd>

**數值** (**long**) 指定滑鼠指標相對於控制項左上角的 x 座標。

</dd> <dt>

*財年* 
</dt> <dd>

**數值** (**long**) 指定滑鼠指標相對於控制項左上角的 y 座標。

</dd> </dl>

## <a name="return-value"></a>傳回值

此事件不會傳回值。

## <a name="remarks"></a>備註

事件參數的值是由 Windows Media Player 指定，而且可以使用指定的參數名稱，存取或傳遞至匯入 JScript 檔案中的方法。 此參數名稱的類型必須完全如所示，包括大小寫。

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

 

 





