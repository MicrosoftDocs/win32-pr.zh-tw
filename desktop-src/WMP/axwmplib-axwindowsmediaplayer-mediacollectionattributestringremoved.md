---
title: AxWindowsMediaPlayer 物件的 MediaCollectionAttributeStringRemoved 事件
description: 從程式庫移除屬性值時，就會發生 MediaCollectionAttributeStringRemoved 事件。 |AxWindowsMediaPlayer 物件的 MediaCollectionAttributeStringRemoved 事件
ms.assetid: 2f264416-0bc5-41d0-8863-32c284393082
keywords:
- AxWindowsMediaPlayer 物件的 MediaCollectionAttributeStringRemoved 事件 Windows Media Player
topic_type:
- apiref
api_name:
- MediaCollectionAttributeStringRemoved Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f56a6e997ada3296a0ec1df841797c1495ccde0864495dcf77a0a0634ccde5fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118582074"
---
# <a name="mediacollectionattributestringremoved-event-of-the-axwindowsmediaplayer-object"></a>AxWindowsMediaPlayer 物件的 MediaCollectionAttributeStringRemoved 事件

從程式庫移除屬性值時，就會發生 MediaCollectionAttributeStringRemoved 事件。

``` syntax
[C#]
private void player_MediaCollectionAttributeStringRemoved(
  object sender,
  _WMPOCXEvents_MediaCollectionAttributeStringRemovedEvent e
)

[Visual Basic]
Private Sub player_MediaCollectionAttributeStringRemoved(
  sender As Object,
  e As _WMPOCXEvents_MediaCollectionAttributeStringRemovedEvent
) Handles player.MediaCollectionAttributeStringRemoved
```

## <a name="event-data"></a>事件資料

與這個事件相關聯的處理常式屬於 **AxWMPLib 型別。 \_WMPOCXEvents \_ MediaCollectionAttributeStringRemovedEventHandler**。 這個處理常式會接收 AxWMPLib 型別的引數 **。 \_WMPOCXEvents \_ MediaCollectionAttributeStringRemovedEvent**，其中包含與這個事件相關的下列屬性。



| 屬性           | 描述                                                                                                                                                                                  |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **bstrAttribName** | StringSpecifies 屬性的名稱。 如需 Windows Media Player 所支援之屬性的詳細資訊，請參閱[屬性參考](attribute-reference.md)。<br/> |
| bstrAttribVal      | StringSpecifies 屬性的值。<br/>                                                                                                                                |



 

## <a name="remarks"></a>備註

從程式庫中移除媒體專案時，會從 **MediaCollection** 中移除其中繼資料，並針對移除的每個屬性引發此事件。

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

 

 





