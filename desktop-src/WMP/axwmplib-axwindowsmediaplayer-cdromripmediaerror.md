---
title: AxWindowsMediaPlayer 物件的 CdromRipMediaError 事件
description: 從 CD 翻錄個別播放軌時發生錯誤，就會發生 CdromRipMediaError 事件。
ms.assetid: 542d0184-d893-4b98-903e-339909276fd6
keywords:
- AxWindowsMediaPlayer 物件的 CdromRipMediaError 事件 Windows Media Player
topic_type:
- apiref
api_name:
- CdromRipMediaError Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39b429505996cd5e85bc1e0e2e85c3f47103d244
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981088"
---
# <a name="cdromripmediaerror-event-of-the-axwindowsmediaplayer-object"></a>AxWindowsMediaPlayer 物件的 CdromRipMediaError 事件

從 CD 翻錄個別播放軌時發生錯誤，就會發生 CdromRipMediaError 事件。

``` syntax
[C#]
private void player_CdromRipMediaError(
  object sender,
  _WMPOCXEvents_CdromRipMediaErrorEvent e
)

[Visual Basic]
Private Sub player_CdromRipMediaError( 
  sender As Object,
  e As _WMPOCXEvents_CdromRipMediaErrorEvent
) Handles player.CdromRipMediaError
```

## <a name="event-data"></a>事件資料

與這個事件相關聯的處理常式屬於 **AxWMPLib 型別。 \_WMPOCXEvents \_ CdromRipMediaErrorEventHandler**。 這個處理常式會接收 AxWMPLib 型別的引數 **。 \_WMPOCXEvents \_ CdromRipMediaErrorEvent**，其中包含與這個事件相關的下列屬性。



| 屬性  | 描述                                                                                                             |
|-----------|-------------------------------------------------------------------------------------------------------------------------|
| pCdromRip | 代表引發錯誤之翻錄作業的 WMPLib IWMPCdromRipThe 介面。<br/>                |
| pMedia    | 引發錯誤的 ObjectThe 媒體專案。 您可以將此轉換成 IWMPMedia 介面來存取它。<br/> |



 

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

[**IWMPMedia 介面 (VB 和 c # )**](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





