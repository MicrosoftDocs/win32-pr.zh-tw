---
title: AxWindowsMediaPlayer 物件的 KeyDown 事件
description: 按下按鍵時，就會發生 KeyDown 事件。 |AxWindowsMediaPlayer 物件的 KeyDown 事件
ms.assetid: e67b9628-6c53-4893-921a-9487ebfc1cd5
keywords:
- AxWindowsMediaPlayer 物件的 KeyDown 事件 Windows Media Player
topic_type:
- apiref
api_name:
- KeyDown Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 054736007219021dbc0a4c1c968f61e1bbdb285fa416aae5f3c92c3880fb55de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119469718"
---
# <a name="keydown-event-of-the-axwindowsmediaplayer-object"></a>AxWindowsMediaPlayer 物件的 KeyDown 事件

按下按鍵時，就會發生 KeyDown 事件。

``` syntax
[C#]
private void player_KeyDownEvent(
  object sender,
  _WMPOCXEvents_KeyDownEvent e
)

[Visual Basic]
Private Sub player_KeyDownEvent(  
  sender As Object, 
  e As _WMPOCXEvents_KeyDownEvent
) Handles player.KeyDownEvent
```

## <a name="event-data"></a>事件資料

與這個事件相關聯的處理常式屬於 **AxWMPLib 型別。 \_WMPOCXEvents \_ KeyDownEventHandler**。 這個處理常式會接收 AxWMPLib 型別的引數 **。 \_WMPOCXEvents \_ KeyDownEvent**，其中包含與這個事件相關的下列屬性。



| 屬性    | 描述                                                                                                                                                                                                                                                                                                                                                                          |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| nKeyCode    | Int16Specifies 已按下的實體索引鍵。 如需可能的值，請參閱備註。<br/>                                                                                                                                                                                                                                                                                    |
| nShiftState | Int16A 位，具有與 SHIFT 鍵對應的最不重要位 (位 0) 、CTRL 鍵 (位 1) ，以及 ALT 鍵 (位 2) 。 這些位會分別對應至值1、2和4。 Shift 引數表示這些索引鍵的狀態。 您可以設定部分、全部或全部的位，表示未按下部分、全部或未按下任何鍵。<br/> |



 

## <a name="remarks"></a>備註

**NKeyCode** 屬性會指定實體索引鍵。 下表顯示標準鍵盤上主要索引鍵的可能值。

主要索引鍵的值。



| Key                     | 值   |
|-------------------------|---------|
| A-Z                     | 65-90   |
| 0-9                     | 48-56   |
| F1-F12                  | 112-123 |
| ESC                     | 27      |
| TAB                     | 9       |
| CAPS LOCK               | 20      |
| 向左或向右移動 ()    | 16      |
| CTRL (左或右)     | 17      |
| ALT (左或右)      | 18      |
| SPACE                   | 32      |
| 退格鍵               | 8       |
| ENTER                   | 13      |
| Windows 標誌鍵，左方  | 91      |
| Windows 標誌鍵，right | 92      |
| 應用程式金鑰         | 93      |



 

數位板索引鍵的值。



| Key               | 值  |
|-------------------|--------|
| 0-9               | 96-105 |
| NUM LOCK          | 144    |
| 除以 (/)         | 111    |
| 將 (乘以 \*)      | 106    |
| 減去 (-)       | 109    |
| 新增 (+)            | 107    |
|  (輸入) 的分隔符號 | 108    |
| DECIMAL (。 )        | 110    |



 

導覽鍵的值。



| Key         | 值 |
|-------------|-------|
| INSERT      | 45    |
| DELETE      | 46    |
| HOME        | 36    |
| END         | 35    |
| PAGE UP     | 33    |
| PAGE DOWN   | 34    |
| 向上鍵    | 38    |
| DOWN ARROW  | 40    |
| 向左鍵  | 37    |
| 向右鍵 | 39    |



 

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

 

 





