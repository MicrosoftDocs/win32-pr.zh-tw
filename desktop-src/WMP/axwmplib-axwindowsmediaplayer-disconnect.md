---
title: AxWindowsMediaPlayer 物件的中斷線上活動
description: 中斷線上活動是保留供日後使用。
ms.assetid: 3baecc6c-e772-4269-96c1-900be270543e
keywords:
- AxWindowsMediaPlayer 物件的中斷線上活動 Windows Media Player
topic_type:
- apiref
api_name:
- Disconnect Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89dffe3191efeddba74eb22c7c5c72b8c52bc095
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001504"
---
# <a name="disconnect-event-of-the-axwindowsmediaplayer-object"></a>AxWindowsMediaPlayer 物件的中斷線上活動

中斷線上活動是保留供日後使用。

``` syntax
[C#]
private void player_Disconnect(
  object sender,
  _WMPOCXEvents_DisconnectEvent e
)

[Visual Basic]
Private Sub player_Disconnect(  
  sender As Object,
  e As _WMPOCXEvents_DisconnectEvent
) Handles player.Disconnect
```

## <a name="event-data"></a>事件資料

與這個事件相關聯的處理常式屬於 **AxWMPLib 型別。 \_WMPOCXEvents \_ DisconnectEventHandler**。 這個處理常式會接收 AxWMPLib 型別的引數 **。 \_WMPOCXEvents \_ DisconnectEvent**，其中包含與這個事件相關的下列屬性。



| 屬性 | 描述                               |
|----------|-------------------------------------------|
| result   | **System.object** 不支援。<br/> |



 

## <a name="remarks"></a>備註

此事件已保留供日後使用。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| 版本<br/>   | Windows Media Player 9 系列或更新版本<br/>                                                                          |
| 命名空間<br/> | **AxWMPLib**<br/>                                                                                                    |
| 組件<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**AxWindowsMediaPlayer 物件 (VB 和 c # )**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





