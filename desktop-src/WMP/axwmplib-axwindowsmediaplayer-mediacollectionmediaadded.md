---
title: AxWindowsMediaPlayer 物件的 MediaCollectionMediaAdded 事件
description: 當媒體專案加入至本機程式庫時，就會發生 MediaCollectionMediaAdded 事件。 |AxWindowsMediaPlayer 物件的 MediaCollectionMediaAdded 事件
ms.assetid: ba1779f6-a212-44f4-b52a-c88e22aebcce
keywords:
- AxWindowsMediaPlayer 物件的 MediaCollectionMediaAdded 事件 Windows Media Player
topic_type:
- apiref
api_name:
- MediaCollectionMediaAdded Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbb839fccf9a5048b5647480eca36fcfcaeb904e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984400"
---
# <a name="mediacollectionmediaadded-event-of-the-axwindowsmediaplayer-object"></a>AxWindowsMediaPlayer 物件的 MediaCollectionMediaAdded 事件

當媒體專案加入至本機程式庫時，就會發生 MediaCollectionMediaAdded 事件。

``` syntax
[C#]
private void player_MediaCollectionMediaAdded(
  object sender,
  _WMPOCXEvents_MediaCollectionMediaAddedEvent e
)

[Visual Basic]
Private Sub player_MediaCollectionMediaAdded(
  sender As Object,
  e As _WMPOCXEvents_MediaCollectionMediaAddedEvent
) Handles player.MediaCollectionMediaAdded
```

## <a name="event-data"></a>事件資料

與這個事件相關聯的處理常式屬於 **AxWMPLib 型別。 \_WMPOCXEvents \_ MediaCollectionMediaAddedEventHandler**。 這個處理常式會接收 AxWMPLib 型別的引數 **。 \_WMPOCXEvents \_ MediaCollectionMediaAddedEvent**，其中包含與這個事件相關的下列屬性。



| 屬性 | 描述                                                                                                                  |
|----------|------------------------------------------------------------------------------------------------------------------------------|
| pMedia   | ObjectThe 媒體專案已新增至本機程式庫。 您可以將此轉換成 IWMPMedia 介面來存取它。<br/> |



 

## <a name="remarks"></a>備註

只有本機程式庫才會發生此事件。

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

[**AxWindowsMediaPlayer. mediaCollection (VB 和 c # )**](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md)
</dt> <dt>

[**IWMPMedia 介面 (VB 和 c # )**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**IWMPMediaCollection 介面 (VB 和 c # )**](iwmpmediacollection--vb-and-c.md)
</dt> </dl>

 

 





