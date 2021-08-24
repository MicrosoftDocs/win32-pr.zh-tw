---
title: AxWindowsMediaPlayer 物件的 ModeChange 事件
description: 當 Windows Media Player 的模式變更時，就會發生 ModeChange 事件。 |AxWindowsMediaPlayer 物件的 ModeChange 事件
ms.assetid: 56308425-dce5-4691-8970-c0807744abef
keywords:
- AxWindowsMediaPlayer 物件的 ModeChange 事件 Windows Media Player
topic_type:
- apiref
api_name:
- ModeChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa3b81ce7c48fd34f03131c7ed3f6cafed1029b103f218842a70ecaade08f1af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764838"
---
# <a name="modechange-event-of-the-axwindowsmediaplayer-object"></a>AxWindowsMediaPlayer 物件的 ModeChange 事件

當 Windows Media Player 的模式變更時，就會發生 ModeChange 事件。

``` syntax
[C#]
private void player_ModeChange(
  object sender,
  _WMPOCXEvents_ModeChangeEvent e
)

[Visual Basic]
Private Sub player_ModeChange( 
  sender As Object,
  e As _WMPOCXEvents_ModeChangeEvent
) Handles player.ModeChange
```

## <a name="event-data"></a>事件資料

與這個事件相關聯的處理常式屬於 **AxWMPLib 型別。 \_WMPOCXEvents \_ ModeChangeEventHandler**。 這個處理常式會接收 AxWMPLib 型別的引數 **。 \_WMPOCXEvents \_ ModeChangeEvent**，其中包含與這個事件相關的下列屬性。



| 屬性 | 描述                                                                                    |
|----------|------------------------------------------------------------------------------------------------|
| modeName | StringIndicates 已變更的模式。 如需可能的值，請參閱備註。<br/> |
| newValue | BooleanIndicates 指定模式的新狀態。<br/>                        |



 

## <a name="remarks"></a>備註

下表顯示 modeName 屬性的可能值。



| String  | 描述                                         |
|---------|-----------------------------------------------------|
| 隨機播放 | 曲目會以隨機順序播放。                  |
| loop    | 整個播放曲目順序都會重複播放。 |



 

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

[**IWMPSettings. getMode (VB 和 c # )**](wmplibiwmpsettings-iwmpsettings-getmode--vb-and-c.md)
</dt> <dt>

[**IWMPSettings. setMode (VB 和 c # )**](wmplibiwmpsettings-iwmpsettings-setmode--vb-and-c.md)
</dt> </dl>

 

 





