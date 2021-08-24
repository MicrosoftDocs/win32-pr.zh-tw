---
title: AxWindowsMediaPlayer 物件的 MouseDown 事件
description: 當使用者按下滑鼠按鍵時，就會發生 MouseDown 事件。 |AxWindowsMediaPlayer 物件的 MouseDown 事件
ms.assetid: 3dfbd034-67d4-4b7e-88d8-a77d301c5df7
keywords:
- AxWindowsMediaPlayer 物件的 MouseDown 事件 Windows Media Player
topic_type:
- apiref
api_name:
- MouseDown Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73259fab6ffd268e1c9a581a4b7ba18fdfba6c1647b57ef12bcae1c3ab8c04a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119509448"
---
# <a name="mousedown-event-of-the-axwindowsmediaplayer-object"></a>AxWindowsMediaPlayer 物件的 MouseDown 事件

當使用者按下滑鼠按鍵時，就會發生 MouseDown 事件。

``` syntax
[C#]
private void player_MouseDownEvent(
  object sender,
  _WMPOCXEvents_MouseDownEvent e
)

[Visual Basic]
Private Sub player_MouseDownEvent(  
  sender As Object,
  e As _WMPOCXEvents_MouseDownEvent
) Handles player.MouseDownEvent
```

## <a name="event-data"></a>事件資料

與這個事件相關聯的處理常式屬於 **AxWMPLib 型別。 \_WMPOCXEvents \_ MouseDownEventHandler**。 這個處理常式會接收 AxWMPLib 型別的引數 **。 \_WMPOCXEvents \_ MouseDownEvent**，其中包含與這個事件相關的下列屬性。



| 屬性    | 描述                                                                                                                                                                                                                                                                                                                    |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| nButton     | Int16A 位的位，其中位對應至左按鈕 (位 0) ，右鍵 (位 1) ，中間按鈕 (位 2) 。 這些位會分別對應至值1、2和4。 只會設定其中一個位，表示造成事件的按鈕。<br/>                                                |
| nShiftState | Int16A 位，具有與 SHIFT 鍵對應的最不重要位 (位 0) 、CTRL 鍵 (位 1) ，以及 ALT 鍵 (位 2) 。 這些位會分別對應至值1、2和4。 您可以設定部分、全部或全部的位，表示未按下部分、全部或未按下任何鍵。<br/> |
| 外匯          | 滑鼠指標相對於控制項左上角的 Int32The X 軸座標。<br/>                                                                                                                                                                                                                 |
| 財年          | 滑鼠指標的 Int32The y 座標，相對於控制項的左上角。<br/>                                                                                                                                                                                                                 |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| 版本<br/>   | Windows Media Player 9 系列或更新版本<br/>                                                                          |
| 命名空間<br/> | **AxWMPLib**<br/>                                                                                                    |
| 組件<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**AxWindowsMediaPlayer 物件 (VB 和 c # )**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





