---
title: AxWindowsMediaPlayer 物件的 MouseUp 事件
description: 當使用者放開滑鼠按鍵時，就會發生 MouseUp 事件。 |AxWindowsMediaPlayer 物件的 MouseUp 事件
ms.assetid: 26bb6e82-d744-4770-b4de-07c9f52b76ec
keywords:
- AxWindowsMediaPlayer 物件的 MouseUp 事件 Windows Media Player
topic_type:
- apiref
api_name:
- MouseUp Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2bf9c209b4fa263eb0a6cbcba2a32b0b1c46fa9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001588"
---
# <a name="mouseup-event-of-the-axwindowsmediaplayer-object"></a>AxWindowsMediaPlayer 物件的 MouseUp 事件

當使用者放開滑鼠按鍵時，就會發生 MouseUp 事件。

``` syntax
[C#]
private void player_MouseUpEvent(
  object sender,
  _WMPOCXEvents_MouseUpEvent e
)

[Visual Basic]
Private Sub player_MouseUpEvent(  
  sender As Object,
  e As _WMPOCXEvents_MouseUpEvent
) Handles player.MouseUpEvent
```

## <a name="event-data"></a>事件資料

與這個事件相關聯的處理常式屬於 **AxWMPLib 型別。 \_WMPOCXEvents \_ MouseUpEventHandler**。 這個處理常式會接收 AxWMPLib 型別的引數 **。 \_WMPOCXEvents \_ MouseUpEvent**，其中包含與這個事件相關的下列屬性。



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

 

 





