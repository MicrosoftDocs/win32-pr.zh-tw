---
title: AxWindowsMediaPlayer 物件的 MediaCollectionMediaRemoved 事件
description: 從本機程式庫移除媒體專案時，就會發生 MediaCollectionMediaRemoved 事件。 |AxWindowsMediaPlayer 物件的 MediaCollectionMediaRemoved 事件
ms.assetid: 66dae2be-2a71-4d53-b2e2-f106426d4eea
keywords:
- AxWindowsMediaPlayer 物件的 MediaCollectionMediaRemoved 事件 Windows Media Player
topic_type:
- apiref
api_name:
- MediaCollectionMediaRemoved Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cea15ff63fb913cd399a152913a27ffda1090d9a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987911"
---
# <a name="mediacollectionmediaremoved-event-of-the-axwindowsmediaplayer-object"></a>AxWindowsMediaPlayer 物件的 MediaCollectionMediaRemoved 事件

從本機程式庫移除媒體專案時，就會發生 MediaCollectionMediaRemoved 事件。

``` syntax
[C#]
private void player_MediaCollectionMediaRemoved(
  object sender,
  _WMPOCXEvents_MediaCollectionMediaRemovedEvent e
)
        
[Visual Basic]
Private Sub player_MediaCollectionMediaRemoved(
  sender As Object,
  e As _WMPOCXEvents_MediaCollectionMediaRemovedEvent
) Handles player.MediaCollectionMediaRemoved
```

## <a name="event-data"></a>事件資料

與這個事件相關聯的處理常式屬於 **AxWMPLib 型別。 \_WMPOCXEvents \_ MediaCollectionMediaRemovedEventHandler**。 這個處理常式會接收 AxWMPLib 型別的引數 **。 \_WMPOCXEvents \_ MediaCollectionMediaRemovedEvent**，其中包含與這個事件相關的下列屬性。



| 屬性 | 描述                                                                                                                      |
|----------|----------------------------------------------------------------------------------------------------------------------------------|
| pMedia   | 從本機程式庫移除的 ObjectThe 媒體專案。 您可以將此轉換成 IWMPMedia 介面來存取它。<br/> |



 

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

[**IWMPMedia 介面 (VB 和 c # )**](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





