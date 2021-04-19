---
title: AxWindowsMediaPlayer 物件的 CdromRipStateChange 事件
description: 當 CD 翻錄操作變更狀態時，就會發生 CdromRipStateChange 事件。
ms.assetid: 0a0bd11f-a685-4c4e-8704-8eabe80d6f86
keywords:
- AxWindowsMediaPlayer 物件的 CdromRipStateChange 事件 Windows Media Player
topic_type:
- apiref
api_name:
- CdromRipStateChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20fae9eb1fa6d5f65876e3f6758a7594f0bdbb19
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106974905"
---
# <a name="cdromripstatechange-event-of-the-axwindowsmediaplayer-object"></a>AxWindowsMediaPlayer 物件的 CdromRipStateChange 事件

當 CD 翻錄操作變更狀態時，就會發生 CdromRipStateChange 事件。

``` syntax
[C#]
private void player_CdromRipStateChange(
  object sender,
  _WMPOCXEvents_CdromRipStateChangeEvent e
)

[Visual Basic]
Private Sub player_CdromRipStateChange(  
  sender As Object,
  e As _WMPOCXEvents_CdromRipStateChangeEvent
) Handles player.CdromRipStateChange
```

## <a name="event-data"></a>事件資料

與這個事件相關聯的處理常式屬於 **AxWMPLib 型別。 \_WMPOCXEvents \_ CdromRipStateChangeEventHandler**。 這個處理常式會接收 AxWMPLib 型別的引數 **。 \_WMPOCXEvents \_ CdromRipStateChangeEvent**，其中包含與這個事件相關的下列屬性。



| 屬性  | 描述                                                                                              |
|-----------|----------------------------------------------------------------------------------------------------------|
| pCdromRip | 代表引發錯誤之翻錄作業的 WMPLib IWMPCdromRipThe 介面。<br/> |
| wmprs     | WMPLib，表示新狀態的 WMPRipStateThe 列舉值。<br/>                         |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| 版本<br/>   | Windows Media Player 11<br/>                                                                                         |
| 命名空間<br/> | **AxWMPLib**<br/>                                                                                                    |
| 組件<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**AxWindowsMediaPlayer 物件 (VB 和 c # )**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**IWMPCdromRip 介面 (VB 和 c # )**](iwmpcdromrip--vb-and-c.md)
</dt> <dt>

[**WMPRipState**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpripstate)
</dt> </dl>

 

 





