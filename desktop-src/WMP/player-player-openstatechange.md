---
title: OpenStateChange 事件
description: 當 openState 屬性變更值時，就會發生 OpenStateChange 事件。 |OpenStateChange 事件
ms.assetid: b6b840ab-72c7-4150-a259-1e7d8afcec81
keywords:
- OpenStateChange 事件 Windows Media Player
- OpenStateChange 事件 Windows Media Player，Player 類別
- Player 類別 Windows Media Player，OpenStateChange 事件
topic_type:
- apiref
api_name:
- Player.OpenStateChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b65436dee60a5207e09a57a39c32dc479ce110e1dafb07a7dbd7cab86e4f0a92
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120003218"
---
# <a name="playeropenstatechange-event"></a>OpenStateChange 事件

當 **openState** 屬性變更值時，就會發生 **OpenStateChange** 事件。

## <a name="syntax"></a>語法


```JScript
Player.OpenStateChange(
  NewState
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*NewState* 
</dt> <dd>

指定新的開啟狀態 (**長**) **數目**。 如需值的表格，請參閱 [openState](player-openstate.md) 。

</dd> </dl>

## <a name="return-value"></a>傳回值

此事件不會傳回值。

## <a name="remarks"></a>備註

Windows Media Player 可以在嘗試開啟網路檔案（例如找出伺服器、連線到伺服器，最後開啟檔案）時，經歷數個開啟的狀態。 每次開啟狀態變更時，就會引發此事件。

事件參數的值是由 Windows Media Player 指定，而且可以使用指定的參數名稱，存取或傳遞至匯入 JScript 檔案中的方法。 此參數名稱的類型必須完全如所示，包括大小寫。

Windows Media Player 狀態不保證會以任何特定順序發生。 此外，並非每個狀態都一定會在一連串的事件期間發生。 您不應該撰寫依賴狀態順序的程式碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本。<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Player 物件**](player-object.md)
</dt> <dt>

[**OpenState**](player-openstate.md)
</dt> </dl>

 

 





