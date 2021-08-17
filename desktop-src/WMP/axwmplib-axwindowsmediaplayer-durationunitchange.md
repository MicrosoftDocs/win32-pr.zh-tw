---
title: AxWindowsMediaPlayer 物件的 DurationUnitChange 事件
description: DurationUnitChange 事件已保留供日後使用。
ms.assetid: d8d7da21-bc61-49f8-91bd-4c232295c1ac
keywords:
- AxWindowsMediaPlayer 物件的 DurationUnitChange 事件 Windows Media Player
topic_type:
- apiref
api_name:
- DurationUnitChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1efa872389ad88a236808de64ed299dd3afc123cee59f39f1215f7a16bcb589f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136041"
---
# <a name="durationunitchange-event-of-the-axwindowsmediaplayer-object"></a>AxWindowsMediaPlayer 物件的 DurationUnitChange 事件

DurationUnitChange 事件已保留供日後使用。

``` syntax
[C#]
private void player_DurationUnitChange(
  object sender,
  _WMPOCXEvents_DurationUnitChangeEvent e
)

[Visual Basic]
Private Sub player_DurationUnitChange(  
  sender As Object,  
  e As _WMPOCXEvents_DurationUnitChangeEvent
) Handles player.DurationUnitChange
```

## <a name="event-data"></a>事件資料

與這個事件相關聯的處理常式屬於 **AxWMPLib 型別。 \_WMPOCXEvents \_ DurationUnitChangeEventHandler**。 這個處理常式會接收 AxWMPLib 型別的引數 **。 \_WMPOCXEvents \_ DurationUnitChangeEvent**，其中包含與這個事件相關的下列屬性。



| 屬性        | 描述                               |
|-----------------|-------------------------------------------|
| newDurationUnit | **System.object** 不支援。<br/> |



 

## <a name="remarks"></a>備註

此事件已保留供日後使用。

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

 

 





