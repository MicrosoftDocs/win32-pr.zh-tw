---
title: AxWindowsMediaPlayer 物件的 MediaCollectionAttributeStringAdded 事件
description: 將屬性值新增至程式庫時，就會發生 MediaCollectionAttributeStringAdded 事件。 |AxWindowsMediaPlayer 物件的 MediaCollectionAttributeStringAdded 事件
ms.assetid: b14db0ce-bd78-4e28-a42c-1a231c29da2b
keywords:
- AxWindowsMediaPlayer 物件的 MediaCollectionAttributeStringAdded 事件 Windows Media Player
topic_type:
- apiref
api_name:
- MediaCollectionAttributeStringAdded Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6712b6caa8f014ec75bf2b031e2d3f6db429dbd2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999111"
---
# <a name="mediacollectionattributestringadded-event-of-the-axwindowsmediaplayer-object"></a>AxWindowsMediaPlayer 物件的 MediaCollectionAttributeStringAdded 事件

將屬性值新增至程式庫時，就會發生 MediaCollectionAttributeStringAdded 事件。

``` syntax
[C#]
private void player_MediaCollectionAttributeStringAdded(
  object sender,
  _WMPOCXEvents_MediaCollectionAttributeStringAddedEvent e
)

[Visual Basic]
Private Sub player_MediaCollectionAttributeStringAdded(
  sender As Object,
  e As _WMPOCXEvents_MediaCollectionAttributeStringAddedEvent
) Handles player.MediaCollectionAttributeStringAdded
```

## <a name="event-data"></a>事件資料

與這個事件相關聯的處理常式屬於 **AxWMPLib 型別。 \_WMPOCXEvents \_ MediaCollectionAttributeStringAddedEventHandler**。 這個處理常式會接收 AxWMPLib 型別的引數 **。 \_WMPOCXEvents \_ MediaCollectionAttributeStringAddedEvent**，其中包含與這個事件相關的下列屬性。



| 屬性           | 描述                                                                                                                                                                                  |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **bstrAttribName** | StringSpecifies 屬性的名稱。 如需 Windows Media Player 所支援之屬性的詳細資訊，請參閱 [屬性參考](attribute-reference.md)。<br/> |
| bstrAttribVal      | StringSpecifies 屬性的值。<br/>                                                                                                                                |



 

## <a name="remarks"></a>備註

當媒體專案加入至程式庫時，會將其中繼資料新增至媒體集合，並為每個新增的屬性引發此事件。

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

 

 





