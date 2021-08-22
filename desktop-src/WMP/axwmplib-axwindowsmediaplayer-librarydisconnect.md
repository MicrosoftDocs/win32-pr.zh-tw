---
title: AxWindowsMediaPlayer 物件的 LibraryDisconnect 事件
description: 當程式庫不再可用時，就會發生 LibraryDisconnect 事件。
ms.assetid: 053d914a-dcd9-4fd6-a789-10c26147d08a
keywords:
- AxWindowsMediaPlayer 物件的 LibraryDisconnect 事件 Windows Media Player
topic_type:
- apiref
api_name:
- LibraryDisconnect Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a032dc95a68430768b0f2aa109a56dae80cdaecb14b67eb5dbf6b2657cdd5107
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136001"
---
# <a name="librarydisconnect-event-of-the-axwindowsmediaplayer-object"></a>AxWindowsMediaPlayer 物件的 LibraryDisconnect 事件

當程式庫不再可用時，就會發生 LibraryDisconnect 事件。

``` syntax
[C#]
private void player_LibraryDisconnect(
  object sender,
  _WMPOCXEvents_LibraryDisconnectEvent e
)

[Visual Basic]
Private Sub player_LibraryDisconnect(  
   sender As Object,  
   e As _WMPOCXEvents_LibraryDisconnectEvent
) Handles player.LibraryDisconnect
```

## <a name="event-data"></a>事件資料

與這個事件相關聯的處理常式屬於 **AxWMPLib 型別。 \_WMPOCXEvents \_ LibraryDisconnectEventHandler**。 這個處理常式會接收 AxWMPLib 型別的引數 **。 \_WMPOCXEvents \_ LibraryDisconnectEvent**，其中包含與這個事件相關的下列屬性。



| 屬性 | 描述                                                                                   |
|----------|-----------------------------------------------------------------------------------------------|
| pLibrary | **WMPLib. IWMPLibrary** 表示已中斷連結之程式庫的介面。<br/> |



 

## <a name="remarks"></a>備註

本機程式庫不會發生此事件。

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

[**IWMPLibrary 介面 (VB 和 c # )**](iwmplibrary--vb-and-c.md)
</dt> </dl>

 

 





