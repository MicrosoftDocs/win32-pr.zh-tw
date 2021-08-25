---
title: IWMPControls currentPositionString 屬性
description: CurrentPositionString 屬性會取得媒體專案中的目前位置，作為格式化為 HH MM SS 的字串， (小時、分鐘和秒) 。
ms.assetid: cd28dafa-b6a4-4bed-aa5d-7e7be6af1426
keywords:
- currentPositionString 屬性 Windows Media Player
- currentPositionString 屬性 Windows Media Player，IWMPControls 介面
- IWMPControls 介面 Windows Media Player，currentPositionString 屬性
topic_type:
- apiref
api_name:
- IWMPControls.currentPositionString
- IWMPControls.get_currentPositionString
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61e3c98937a12c145742895979ccccb8118f8349f82b2840c902dfe625ad0472
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119861908"
---
# <a name="iwmpcontrolscurrentpositionstring-property"></a>IWMPControls：： currentPositionString 屬性

**CurrentPositionString** 屬性會取得媒體專案中的目前位置，作為格式化為 HH： MM： SS (時、分和秒) 的字串。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```CSharp
public System.String currentPositionString {get;}
```


```VB

Public ReadOnly Property currentPositionString As System.String
```





## <a name="property-value"></a>屬性值

已格式化的 **system.string** ，表示目前的位置。

## <a name="remarks"></a>備註

如果媒體專案的長度不到一小時，則目前的位置會格式化為 MM： SS (分鐘和秒) 。

## <a name="examples"></a>範例

下列範例會啟動一個以一秒為間隔觸發事件的計時器。 在計時器事件處理常式中，標籤會以 **currentPositionString** 進行更新。 **AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。


```CSharp
// Set the timer to fire an event every second and start the timer.
timer.Interval = 1000;
timer.Start();

// Note:  Use the AxWindowsMediaPlayer.PlayStateChange event with a switch statement to
// determine when to start and stop the timer. 
   
// Update the text of the label with the currentPositionString.
private void TimerEventProcessor(object sender, System.EventArgs e)
{
    currentPositionLabel.Text = player.Ctlcontrols.currentPositionString;
}
```


```VB

' Set the timer to fire an event every second and start the timer.
timer.Interval = 1000
timer.Start()

&#39; Note:  Use the AxWindowsMediaPlayer.PlayStateChange event with a switch statement to
&#39; determine when to start and stop the timer. 

&#39; Update the text of the label with the currentPositionString.
Public Sub TimerEventProcessor(ByVal sender As Object, ByVal e As System.EventArgs) Handles timer.Tick

    currentPositionLabel.Text = player.Ctlcontrols.currentPositionString

End Sub
```





## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| 版本<br/>   | Windows Media Player 9 系列或更新版本<br/>                                                                      |
| 命名空間<br/> | **WMPLib**<br/>                                                                                                  |
| 組件<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IWMPControls 介面 (VB 和 c # )**](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[**IWMPControls. currentPosition (VB 和 c # )**](wmplibiwmpcontrols-iwmpcontrols-currentposition--vb-and-c.md)
</dt> </dl>

 

 





