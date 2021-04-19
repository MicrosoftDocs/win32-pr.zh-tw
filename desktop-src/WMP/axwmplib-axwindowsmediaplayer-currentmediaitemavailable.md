---
title: AxWindowsMediaPlayer 物件的 CurrentMediaItemAvailable 事件
description: 當目前媒體專案中的圖形中繼資料專案變成可用時，就會發生 CurrentMediaItemAvailable 事件。 |AxWindowsMediaPlayer 物件的 CurrentMediaItemAvailable 事件
ms.assetid: 7db62e6a-5f20-441a-801f-147ac386c5f8
keywords:
- AxWindowsMediaPlayer 物件的 CurrentMediaItemAvailable 事件 Windows Media Player
topic_type:
- apiref
api_name:
- CurrentMediaItemAvailable Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 547622424194e63733cec6166d813d42ebf577ee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995044"
---
# <a name="currentmediaitemavailable-event-of-the-axwindowsmediaplayer-object"></a>AxWindowsMediaPlayer 物件的 CurrentMediaItemAvailable 事件

當目前媒體專案中的圖形中繼資料專案變成可用時，就會發生 CurrentMediaItemAvailable 事件。

``` syntax
[C#]
private void player_CurrentMediaItemAvailable(
  object sender,
  _WMPOCXEvents_CurrentMediaItemAvailableEvent e
)

[Visual Basic]
Private Sub player_CurrentMediaItemAvailable(
  sender As Object,  
  e As _WMPOCXEvents_CurrentMediaItemAvailableEvent
) Handles player.CurrentMediaItemAvailable
```

## <a name="event-data"></a>事件資料

與這個事件相關聯的處理常式屬於 **AxWMPLib 型別。 \_WMPOCXEvents \_ CurrentMediaItemAvailableEventHandler**。 這個處理常式會接收 AxWMPLib 型別的引數 **。 \_WMPOCXEvents \_ CurrentMediaItemAvailableEvent**，其中包含與這個事件相關的下列屬性。



| 屬性     | 描述                                                 |
|--------------|-------------------------------------------------------------|
| bstrItemName | 目前媒體專案的 StringThe 名稱。<br/> |



 

## <a name="remarks"></a>備註

因為播放可以在媒體專案完全下載之前開始播放，所以媒體專案中包含的任何元資料圖形 (例如專輯封面) 在開始播放時可能無法使用。 此事件會在元資料圖形專案完成下載時發出警示。 然後，您可以藉由將 **bstrItemName** 的值傳遞給 *IWMPMediaCollection*，來取得 **IWMPMedia** 介面。**getByName** 方法，之後您就可以使用 *IWMPMedia3* 來存取元資料圖形專案。**getItemInfoByType** 並為屬性名稱指定 **WM/圖片**。

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

[**IWMPMedia 介面 (VB 和 c # )**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**IWMPMedia3. getItemInfoByType (VB 和 c # )**](wmplibiwmpmedia3-iwmpmedia3-getiteminfobytype--vb-and-c.md)
</dt> <dt>

[**IWMPMediaCollection. getByName (VB 和 c # )**](wmplibiwmpmediacollection-iwmpmediacollection-getbyname--vb-and-c.md)
</dt> </dl>

 

 





