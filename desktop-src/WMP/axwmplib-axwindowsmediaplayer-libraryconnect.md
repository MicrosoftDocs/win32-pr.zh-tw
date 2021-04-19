---
title: AxWindowsMediaPlayer 物件的 LibraryConnect 事件
description: 當程式庫變成可用時，就會發生 LibraryConnect 事件。
ms.assetid: f67243ce-0e25-43a7-b754-6b0e80d72055
keywords:
- AxWindowsMediaPlayer 物件的 LibraryConnect 事件 Windows Media Player
topic_type:
- apiref
api_name:
- LibraryConnect Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c33353b8438c61e28a3d52975fe90b06f14f03a4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993229"
---
# <a name="libraryconnect-event-of-the-axwindowsmediaplayer-object"></a>AxWindowsMediaPlayer 物件的 LibraryConnect 事件

當程式庫變成可用時，就會發生 LibraryConnect 事件。

``` syntax
[C#]
private void player_LibraryConnect(
  object sender,
  _WMPOCXEvents_LibraryConnectEvent e
)

[Visual Basic]
Private Sub player_LibraryConnect(  
  sender As Object,
  e As _WMPOCXEvents_LibraryConnectEvent
) Handles player.LibraryConnect
```

## <a name="event-data"></a>事件資料

與這個事件相關聯的處理常式屬於 **AxWMPLib 型別。 \_WMPOCXEvents \_ LibraryConnectEventHandler**。 這個處理常式會接收 AxWMPLib 型別的引數 **。 \_WMPOCXEvents \_ LibraryConnectEvent**，其中包含與這個事件相關的下列屬性。



| 屬性 | 描述                                                                                |
|----------|--------------------------------------------------------------------------------------------|
| pLibrary | **WMPLib. IWMPLibrary** 表示連接程式庫的介面。<br/> |



 

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

 

 





