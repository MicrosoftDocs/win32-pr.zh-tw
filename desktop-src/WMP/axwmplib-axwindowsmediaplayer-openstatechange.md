---
title: AxWindowsMediaPlayer 物件的 OpenStateChange 事件
description: 當 openState 屬性變更值時，就會發生 OpenStateChange 事件。 |AxWindowsMediaPlayer 物件的 OpenStateChange 事件
ms.assetid: 0229f8b4-7216-44f6-9838-a640b99bd9f3
keywords:
- AxWindowsMediaPlayer 物件的 OpenStateChange 事件 Windows Media Player
topic_type:
- apiref
api_name:
- OpenStateChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ccf7619e86268fe6b465d2a64ca00d650a7a7051b3aa4f44e2a73a98929be13
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120003978"
---
# <a name="openstatechange-event-of-the-axwindowsmediaplayer-object"></a>AxWindowsMediaPlayer 物件的 OpenStateChange 事件

當 **openState** 屬性變更值時，就會發生 OpenStateChange 事件。

``` syntax
[C#]
private void player_OpenStateChange(
  object sender,
  _WMPOCXEvents_OpenStateChangeEvent e
)

[Visual Basic]
Private Sub player_OpenStateChange(
  sender As Object,
  e As _WMPOCXEvents_OpenStateChangeEvent
) Handles player.OpenStateChange
```

## <a name="event-data"></a>事件資料

與這個事件相關聯的處理常式屬於 **AxWMPLib 型別。 \_WMPOCXEvents \_ OpenStateChangeEventHandler**。 這個處理常式會接收 AxWMPLib 型別的引數 **。 \_WMPOCXEvents \_ OpenStateChangeEvent**，其中包含與這個事件相關的下列屬性。



| 屬性 | 描述                                                                                                                                         |
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| NewState | Int32Specifies 新的開啟狀態。 如需值的表格，請參閱 [openState](axwmplib-axwindowsmediaplayer-openstate--vb-and-c.md)。<br/> |



 

## <a name="remarks"></a>備註

Windows Media Player 可以在嘗試開啟網路檔案（例如找出伺服器、連線到伺服器，最後開啟檔案）時，經歷數個開啟的狀態。 每次開啟狀態變更時，就會引發此事件。

Windows Media Player 狀態不保證會以任何特定順序發生。 此外，並非每個狀態都一定會在一連串的事件期間發生。 您不應該撰寫依賴狀態順序的程式碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| 版本<br/>   | Windows Media Player 9 系列或更新版本<br/>                                                                          |
| 命名空間<br/> | **AxWMPLib**<br/>                                                                                                    |
| 組件<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**AxWindowsMediaPlayer 物件 (VB 和 c # )**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**AxWindowsMediaPlayer. openState (VB 和 c # )**](axwmplib-axwindowsmediaplayer-openstate--vb-and-c.md)
</dt> </dl>

 

 





