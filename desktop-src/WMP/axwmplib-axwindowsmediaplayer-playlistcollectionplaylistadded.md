---
title: AxWindowsMediaPlayer 物件的 PlaylistCollectionPlaylistAdded 事件
description: 當播放清單新增至播放清單集合時，就會發生 PlaylistCollectionPlaylistAdded 事件。 |AxWindowsMediaPlayer 物件的 PlaylistCollectionPlaylistAdded 事件
ms.assetid: 13d3bc86-6655-4536-a58f-327eabb2b8f9
keywords:
- AxWindowsMediaPlayer 物件的 PlaylistCollectionPlaylistAdded 事件 Windows Media Player
topic_type:
- apiref
api_name:
- PlaylistCollectionPlaylistAdded Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d5223d5864aa8be9019b2219ef09917a1c63cf16d87a48aef9543246d5197a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118581823"
---
# <a name="playlistcollectionplaylistadded-event-of-the-axwindowsmediaplayer-object"></a>AxWindowsMediaPlayer 物件的 PlaylistCollectionPlaylistAdded 事件

當播放清單新增至播放清單集合時，就會發生 PlaylistCollectionPlaylistAdded 事件。

``` syntax
[C#]
private void player_PlaylistCollectionPlaylistAdded(
  object sender,
  _WMPOCXEvents_PlaylistCollectionPlaylistAddedEvent e
)

[Visual Basic]
Private Sub player_PlaylistCollectionPlaylistAdded(
  sender As Object,
  e As _WMPOCXEvents_PlaylistCollectionPlaylistAddedEvent
) Handles player.PlaylistCollectionPlaylistAdded
```

## <a name="event-data"></a>事件資料

與這個事件相關聯的處理常式屬於 **AxWMPLib 型別。 \_WMPOCXEvents \_ PlaylistCollectionPlaylistAddedEventHandler**。 這個處理常式會接收 AxWMPLib 型別的引數 **。 \_WMPOCXEvents \_ PlaylistCollectionPlaylistAddedEvent**，其中包含與這個事件相關的下列屬性。



| 屬性             | 描述                                                                |
|----------------------|----------------------------------------------------------------------------|
| **bstrPlaylistName** | StringSpecifies 已新增的播放清單名稱。<br/> |



 

## <a name="remarks"></a>備註

已新增的播放清單名稱可用來使用 IWMPPlaylistCollection 來取出對應的播放清單。**getByName** 方法。

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

 

 





