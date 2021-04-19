---
title: AxWindowsMediaPlayer 物件的警告事件
description: 警告事件已保留供日後使用。
ms.assetid: 3de63756-2726-4864-8988-fd614f23bcad
keywords:
- AxWindowsMediaPlayer 物件的警告事件 Windows Media Player
topic_type:
- apiref
api_name:
- Warning Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a868ba7f619287cd96929c62d89dee3555d908b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987878"
---
# <a name="warning-event-of-the-axwindowsmediaplayer-object"></a>AxWindowsMediaPlayer 物件的警告事件

警告事件已保留供日後使用。

``` syntax
[C#]
private void player_Warning(
  object sender,
  _WMPOCXEvents_WarningEvent e
)

[Visual Basic]
Private Sub player_Warning(
  sender As Object,
  e As _WMPOCXEvents_WarningEvent
) Handles player.Warning
```

## <a name="event-data"></a>事件資料

與這個事件相關聯的處理常式屬於 **AxWMPLib 型別。 \_WMPOCXEvents \_ WarningEventHandler**。 這個處理常式會接收 AxWMPLib 型別的引數 **。 \_WMPOCXEvents \_ WarningEvent**，其中包含與這個事件相關的下列屬性。



| 屬性    | 描述                                |
|-------------|--------------------------------------------|
| warningType | **System.object** 不支援。<br/>  |
| 參數       | **System.object** 不支援。<br/>  |
| description | **System.string** 不支援。<br/> |



 

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

 

 





