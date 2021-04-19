---
title: AxWindowsMediaPlayer 物件的 PlaylistChange 事件
description: 當播放清單變更時，就會發生 PlaylistChange 事件。 |AxWindowsMediaPlayer 物件的 PlaylistChange 事件
ms.assetid: e4166d81-a205-401a-94c4-a1619e764647
keywords:
- AxWindowsMediaPlayer 物件的 PlaylistChange 事件 Windows Media Player
topic_type:
- apiref
api_name:
- PlaylistChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9989b303d8e9077c158fd844c93431100205d9f6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990800"
---
# <a name="playlistchange-event-of-the-axwindowsmediaplayer-object"></a>AxWindowsMediaPlayer 物件的 PlaylistChange 事件

當播放清單變更時，就會發生 PlaylistChange 事件。

``` syntax
[C#]
private void player_PlaylistChange(
  object sender,
  _WMPOCXEvents_PlaylistChangeEvent e
)

[Visual Basic]
Private Sub player_PlaylistChange(
  sender As Object,
  e As _WMPOCXEvents_PlaylistChangeEvent
) Handles player.PlaylistChange
```

## <a name="event-data"></a>事件資料

與這個事件相關聯的處理常式屬於 **AxWMPLib 型別。 \_WMPOCXEvents \_ PlaylistChangeEventHandler**。 這個處理常式會接收 AxWMPLib 型別的引數 **。 \_WMPOCXEvents \_ PlaylistChangeEvent**，其中包含與這個事件相關的下列屬性。



| 屬性     | 描述                                                                                                                   |
|--------------|-------------------------------------------------------------------------------------------------------------------------------|
| **播放清單** | 已變更的 ObjectThe 物件。 您可以將此轉換成 IWMPPlaylist 介面來存取它。<br/>                |
| **change**   | WMPLib. WMPPlaylistChangeEventTypeAn 列舉值，指出播放清單所發生的變更類型。<br/> |



 

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
</dt> </dl>

 

 





