---
title: AxWindowsMediaPlayer 物件的 MediaCollectionAttributeStringChanged 事件
description: 當程式庫中的屬性值變更時，就會發生 MediaCollectionAttributeStringChanged 事件。 |AxWindowsMediaPlayer 物件的 MediaCollectionAttributeStringChanged 事件
ms.assetid: f5b91399-42b7-4202-9b65-caa9b15847b9
keywords:
- AxWindowsMediaPlayer 物件的 MediaCollectionAttributeStringChanged 事件 Windows Media Player
topic_type:
- apiref
api_name:
- MediaCollectionAttributeStringChanged Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5dcc755d1a183525923b91ce2de7937860582c3cf795d13cbf4a8c22d7c9c37f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119618778"
---
# <a name="mediacollectionattributestringchanged-event-of-the-axwindowsmediaplayer-object"></a>AxWindowsMediaPlayer 物件的 MediaCollectionAttributeStringChanged 事件

當程式庫中的屬性值變更時，就會發生 MediaCollectionAttributeStringChanged 事件。

``` syntax
[C#]
private void player_MediaCollectionAttributeStringChanged(
  object sender,
  _WMPOCXEvents_MediaCollectionAttributeStringChangedEvent e
)

[Visual Basic]
Private Sub player_MediaCollectionAttributeStringChanged(
  sender As Object,
  e As _WMPOCXEvents_MediaCollectionAttributeStringChangedEvent
) Handles player.MediaCollectionAttributeStringChanged
```

## <a name="event-data"></a>事件資料

與這個事件相關聯的處理常式屬於 **AxWMPLib 型別。 \_WMPOCXEvents \_ MediaCollectionAttributeStringChangedEventHandler**。 這個處理常式會接收 AxWMPLib 型別的引數 **。 \_WMPOCXEvents \_ MediaCollectionAttributeStringChangedEvent**，其中包含與這個事件相關的下列屬性。



| 屬性         | 描述                                                                                                                                                                                  |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| bstrAttribName   | StringSpecifies 屬性的名稱。 如需 Windows Media Player 所支援之屬性的詳細資訊，請參閱[屬性參考](attribute-reference.md)。<br/> |
| bstrOldAttribVal | StringSpecifies 屬性的舊值。<br/>                                                                                                                            |
| bstrNewAttribVal | StringSpecifies 屬性的新值。<br/>                                                                                                                            |



 

## <a name="remarks"></a>備註

當使用者修改程式庫中繼資料時，會更新媒體集合，並針對每個屬性變更引發此事件。

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

[**AxWindowsMediaPlayer. mediaCollection (VB 和 c # )**](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md)
</dt> <dt>

[**IWMPMediaCollection 介面 (VB 和 c # )**](iwmpmediacollection--vb-and-c.md)
</dt> </dl>

 

 





