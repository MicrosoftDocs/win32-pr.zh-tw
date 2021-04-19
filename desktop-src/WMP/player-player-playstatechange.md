---
title: PlayStateChange 事件
description: 當 playState 屬性中有變更時，就會發生 PlayStateChange 事件。
ms.assetid: d4c4b114-04b6-4079-b6a2-52b336fc6dc1
keywords:
- PlayStateChange 事件 Windows Media Player
- PlayStateChange 事件 Windows Media Player，Player 類別
- Player 類別 Windows Media Player，PlayStateChange 事件
topic_type:
- apiref
api_name:
- Player.PlayStateChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e621d8698a5379b0d39a55db141fc0012f6ef969
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993268"
---
# <a name="playerplaystatechange-event"></a>PlayStateChange 事件

當 **playState** 屬性中有變更時，就會發生 **PlayStateChange** 事件。

## <a name="syntax"></a>語法


```JScript
Player.PlayStateChange(
  NewState
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*NewState* 
</dt> <dd>

指定新 **playState** 的數位 (**long**) 。 如需可能值的表格，請參閱 [playState](player-playstate.md) 。

</dd> </dl>

## <a name="return-value"></a>傳回值

此事件不會傳回值。

## <a name="remarks"></a>備註

事件參數的值是由 Windows Media Player 指定，而且可以使用指定的參數名稱，存取或傳遞至匯入之 JScript 檔案中的方法。 此參數名稱的類型必須完全如所示，包括大小寫。

Windows Media Player 狀態不保證會以任何特定順序發生。 此外，並非每個狀態都一定會在一連串的事件期間發生。 您不應該撰寫依賴狀態順序的程式碼。

## <a name="examples"></a>範例

下列範例示範 *播放* 程式的事件處理常式。**playStateChange** 事件。 名為 "myText" 的 HTML 文字元素會顯示新的播放狀態。 使用 ID = "Player" 建立 player 物件。


```JScript
<SCRIPT LANGUAGE = "JScript"  FOR = Player EVENT = playStateChange(NewState)>

// Test for the player current state, display a message for each.
switch (NewState){
    case 1:
        myText.value = "Stopped";
        break;

    case 2:
        myText.value = "Paused";
        break;

    case 3:
        myText.value = "Playing";
        break;

    // Other cases go here.

    default:
        myText.value = "";
}
</SCRIPT>
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本。<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Player 物件**](player-object.md)
</dt> <dt>

[**PlayState**](player-playstate.md)
</dt> </dl>

 

 





