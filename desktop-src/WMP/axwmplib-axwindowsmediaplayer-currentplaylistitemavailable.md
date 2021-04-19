---
title: AxWindowsMediaPlayer 物件的 CurrentPlaylistItemAvailable 事件
description: 當目前的播放清單變成可用時，就會發生 CurrentPlaylistItemAvailable 事件。 |AxWindowsMediaPlayer 物件的 CurrentPlaylistItemAvailable 事件
ms.assetid: 101807c9-b00f-4351-a9a3-5413a52496f4
keywords:
- AxWindowsMediaPlayer 物件的 CurrentPlaylistItemAvailable 事件 Windows Media Player
topic_type:
- apiref
api_name:
- CurrentPlaylistItemAvailable Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be9362a569fe8296284d92204628627c74ae3b44
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997662"
---
# <a name="currentplaylistitemavailable-event-of-the-axwindowsmediaplayer-object"></a>AxWindowsMediaPlayer 物件的 CurrentPlaylistItemAvailable 事件

當目前的播放清單變成可用時，就會發生 CurrentPlaylistItemAvailable 事件。

``` syntax
[C#]
private void player_CurrentPlaylistItemAvailable(
  object sender,
  _WMPOCXEvents_CurrentPlaylistItemAvailableEvent e
)

[Visual Basic]
Private Sub player_CurrentPlaylistItemAvailable(  
  sender As Object,
  e As _WMPOCXEvents_CurrentPlaylistItemAvailableEvent
) Handles player.CurrentPlaylistItemAvailable
```

## <a name="event-data"></a>事件資料

與這個事件相關聯的處理常式屬於 **AxWMPLib 型別。 \_WMPOCXEvents \_ CurrentPlaylistItemAvailableEventHandler**。 這個處理常式會接收 AxWMPLib 型別的引數 **。 \_WMPOCXEvents \_ CurrentPlaylistItemAvailableEvent**，其中包含與這個事件相關的下列屬性。



| 屬性         | 描述                                                    |
|------------------|----------------------------------------------------------------|
| **bstrItemName** | 目前播放清單專案的 StringThe 名稱。<br/> |



 

## <a name="remarks"></a>備註

目前播放清單的名稱可以用來從 IWMPPlaylistCollection. getByName 方法所傳回的 IWMPPlaylistArray 介面取出對應的 **IWMPPlaylist** 介面。

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

[**IWMPPlaylist 介面 (VB 和 c # )**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylistArray 介面 (VB 和 c # )**](iwmpplaylistarray--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylistCollection. getByName (VB 和 c # )**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getbyname--vb-and-c.md)
</dt> </dl>

 

 





