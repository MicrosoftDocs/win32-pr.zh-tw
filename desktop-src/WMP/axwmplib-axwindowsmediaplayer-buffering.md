---
title: AxWindowsMediaPlayer 物件的緩衝事件
description: 當 Windows Media Player 控制項開始或結束緩衝或下載時，就會發生緩衝事件。 |AxWindowsMediaPlayer 物件的緩衝事件
ms.assetid: ad152c4d-1c91-4da1-bec0-46f89f3b8c79
keywords:
- AxWindowsMediaPlayer 物件的緩衝事件 Windows Media Player
topic_type:
- apiref
api_name:
- Buffering Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af595443d78a311510df6a7e06b2e716da22ecae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106986141"
---
# <a name="buffering-event-of-the-axwindowsmediaplayer-object"></a>AxWindowsMediaPlayer 物件的緩衝事件

當 Windows Media Player 控制項開始或結束緩衝或下載時，就會發生緩衝事件。

``` syntax
[C#]
private void player_Buffering(
  object sender,
  _WMPOCXEvents_BufferingEvent e
)

[Visual Basic]
Private Sub player_Buffering(
  sender As Object,
  e As _WMPOCXEvents_BufferingEvent
) Handles player.Buffering
```

## <a name="event-data"></a>事件資料

與這個事件相關聯的處理常式屬於 **AxWMPLib 型別。 \_WMPOCXEvents \_ BufferingEventHandler**。 這個處理常式會接收 AxWMPLib 型別的引數 **。 \_WMPOCXEvents \_ BufferingEvent**，其中包含與這個事件相關的下列屬性。



| 屬性 | 描述                                                                                                                                                         |
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Start    | BooleanSpecifies，表示緩衝是否已開始或結束。 True 值表示它已開始;值為 false 表示它已結束。<br/> |



 

## <a name="remarks"></a>備註

您可以使用此事件來判斷何時啟動或停止緩衝或下載。 您可以針對這兩種案例和測試 *IWMPNetwork* 使用相同的事件區塊。**bufferingProgress** 和 *IWMPNetwork*。**downloadProgress** ，以判斷 Windows Media Player 目前是否正在緩衝或正在下載內容。

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

[**IWMPNetwork. bufferingProgress (VB 和 c # )**](wmplibiwmpnetwork-iwmpnetwork-bufferingprogress--vb-and-c.md)
</dt> <dt>

[**IWMPNetwork. downloadProgress (VB 和 c # )**](wmplibiwmpnetwork-iwmpnetwork-downloadprogress--vb-and-c.md)
</dt> </dl>

 

 





