---
title: AxWindowsMediaPlayer 物件的按鍵事件
description: 按下並釋放按鍵時，就會發生 KeyPress 事件。 |AxWindowsMediaPlayer 物件的按鍵事件
ms.assetid: 73ecd6f9-1b58-4e28-ad1b-2d930a235e1d
keywords:
- AxWindowsMediaPlayer 物件的按鍵事件 Windows Media Player
topic_type:
- apiref
api_name:
- KeyPress Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4a01e84b8f765d024c753d08211f3bb84e7f011
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995043"
---
# <a name="keypress-event-of-the-axwindowsmediaplayer-object"></a>AxWindowsMediaPlayer 物件的按鍵事件

按下並釋放按鍵時，就會發生 KeyPress 事件。

``` syntax
[C#]
private void player_KeyPressEvent(
  object sender,
  _WMPOCXEvents_KeyPressEvent e
)

[Visual Basic]
Private Sub player_KeyPressEvent(  
  sender As Object,  
  e As _WMPOCXEvents_KeyPressEvent
) Handles player.KeyPressEvent
```

## <a name="event-data"></a>事件資料

與這個事件相關聯的處理常式屬於 **AxWMPLib 型別。 \_WMPOCXEvents \_ KeyPressEventHandler**。 這個處理常式會接收 AxWMPLib 型別的引數 **。 \_WMPOCXEvents \_ KeyPressEvent**，其中包含與這個事件相關的下列屬性。



| 屬性      | 描述                                                                        |
|---------------|------------------------------------------------------------------------------------|
| **nKeyAscii** | Int16Specifies 字元的標準數值 ANSI 代碼。<br/> |



 

## <a name="remarks"></a>備註

當擊鍵產生任何可列印的鍵盤字元、CTRL 鍵與標準字母中的字元或一些特殊字元的其中一個字元，以及 ENTER 鍵或倒退鍵時，就會發生此事件。

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

 

 





