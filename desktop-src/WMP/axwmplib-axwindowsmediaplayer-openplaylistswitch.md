---
title: AxWindowsMediaPlayer 物件的 OpenPlaylistSwitch 事件
description: 當 DVD 上的標題開始播放時，就會發生 OpenPlaylistSwitch 事件。 |AxWindowsMediaPlayer 物件的 OpenPlaylistSwitch 事件
ms.assetid: 0b9c37a3-1349-48bd-8e1a-aba286c82abf
keywords:
- AxWindowsMediaPlayer 物件的 OpenPlaylistSwitch 事件 Windows Media Player
topic_type:
- apiref
api_name:
- OpenPlaylistSwitch Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c57341488c385b159ce294626a79b7e22287bff83864f7273b0f4432c1db95ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764698"
---
# <a name="openplaylistswitch-event-of-the-axwindowsmediaplayer-object"></a>AxWindowsMediaPlayer 物件的 OpenPlaylistSwitch 事件

當 DVD 上的標題開始播放時，就會發生 OpenPlaylistSwitch 事件。

``` syntax
[C#]
private void player_OpenPlaylistSwitch(
  object sender,
  _WMPOCXEvents_OpenPlaylistSwitchEvent e
)

[Visual Basic]
Private Sub player_OpenPlaylistSwitch(
  sender As Object,
  e As _WMPOCXEvents_OpenPlaylistSwitchEvent
) Handles player.OpenPlaylistSwitch
```

## <a name="event-data"></a>事件資料

與這個事件相關聯的處理常式屬於 **AxWMPLib 型別。 \_WMPOCXEvents \_ OpenPlaylistSwitchEventHandler**。 這個處理常式會接收 AxWMPLib 型別的引數 **。 \_WMPOCXEvents \_ OpenPlaylistSwitchEvent**，其中包含與這個事件相關的下列屬性。



| 屬性  | 描述                                                                                                         |
|-----------|---------------------------------------------------------------------------------------------------------------------|
| **pItem** | 代表標題的 ObjectObject。 您可以將此轉換成 IWMPPlaylist 介面來存取它。<br/> |



 

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

 

 





