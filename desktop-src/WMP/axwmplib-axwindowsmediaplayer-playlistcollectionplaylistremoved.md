---
title: AxWindowsMediaPlayer 物件的 PlaylistCollectionPlaylistRemoved 事件
description: 從播放清單集合中移除播放清單時，就會發生 PlaylistCollectionPlaylistRemoved 事件。 |AxWindowsMediaPlayer 物件的 PlaylistCollectionPlaylistRemoved 事件
ms.assetid: 96935a9e-4c08-42e9-a63f-7b6cda41b243
keywords:
- AxWindowsMediaPlayer 物件的 PlaylistCollectionPlaylistRemoved 事件 Windows Media Player
topic_type:
- apiref
api_name:
- PlaylistCollectionPlaylistRemoved Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b982ff566380a7aa5bf4d0b1a1219739b52dd35
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993539"
---
# <a name="playlistcollectionplaylistremoved-event-of-the-axwindowsmediaplayer-object"></a>AxWindowsMediaPlayer 物件的 PlaylistCollectionPlaylistRemoved 事件

從播放清單集合中移除播放清單時，就會發生 PlaylistCollectionPlaylistRemoved 事件。

``` syntax
[C#]
private void player_PlaylistCollectionPlaylistRemoved(
  object sender,
  _WMPOCXEvents_PlaylistCollectionPlaylistRemovedEvent e
)

[Visual Basic]
Private Sub player_PlaylistCollectionPlaylistRemoved(  
  sender As Object,
  e As _WMPOCXEvents_PlaylistCollectionPlaylistRemovedEvent
) Handles player.PlaylistCollectionPlaylistRemoved
```

## <a name="event-data"></a>事件資料

與這個事件相關聯的處理常式屬於 **AxWMPLib 型別。 \_WMPOCXEvents \_ PlaylistCollectionPlaylistRemovedEventHandler**。 這個處理常式會接收 AxWMPLib 型別的引數 **。 \_WMPOCXEvents \_ PlaylistCollectionPlaylistRemovedEvent**，其中包含與這個事件相關的下列屬性。



| 屬性             | 描述                                                                  |
|----------------------|------------------------------------------------------------------------------|
| **bstrPlaylistName** | StringSpecifies 已移除的播放清單名稱。<br/> |



 

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

[**IWMPPlaylistCollection. getByName (VB 和 c # )**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getbyname--vb-and-c.md)
</dt> </dl>

 

 





