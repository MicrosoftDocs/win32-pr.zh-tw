---
title: 'MM_MIM_DATA 訊息 (Mmsystem .h) '
description: '\_ \_ 當 midi 輸入裝置收到完整的 midi 訊息時，會將 MM MIM 的資料訊息傳送至視窗。'
ms.assetid: 9c580e48-78f3-4914-bdea-393823fb8482
keywords:
- MM_MIM_DATA 訊息 Windows 多媒體
topic_type:
- apiref
api_name:
- MM_MIM_DATA
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4309149c8b69fd4396de3a4e67ab18c49008dd7051ed52d4fe992867d1262fe4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807378"
---
# <a name="mm_mim_data-message"></a>MM \_ MIM \_ 資料訊息

當 midi 輸入裝置收到完整的 midi 訊息時，會將 **MM \_ MIM 的 \_ 資料** 訊息傳送至視窗。


```C++
MM_MIM_DATA 
wParam = (WPARAM) hInput 
lParam = (LPARAM) (DWORD) lMidiMessage 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*
</dt> <dd>

接收 MIDI 訊息之 MIDI 輸入裝置的控制碼。

</dd> <dt>

<span id="lMidiMessage"></span><span id="lmidimessage"></span><span id="LMIDIMESSAGE"></span>*lMidiMessage*
</dt> <dd>

收到的 MIDI 訊息。 訊息會封裝成雙字值，如下所示：



| 需求 | 值 | 描述 |
|-----------|-----------------|-----------------------------------------------------|
| 高單字 | 高序位位元組 | 未使用。                                           |
|           | 低序位位元組  | 視需要) ，包含第二個位元組的 MIDI 資料 (。  |
| 低字組  | 高序位位元組 | 當需要) 時，包含第一個 (的 MIDI 資料位元組。 |
|           | 低序位位元組  | 包含 MIDI 狀態。                           |



 

這兩個 MIDI 資料位元組是選擇性的，視 MIDI 狀態位元組而定。

</dd> </dl>

## <a name="return-value"></a>傳回值

此訊息不會傳回值。

## <a name="remarks"></a>備註

從 MIDI 輸入埠接收的 MIDI 訊息已停用執行中狀態;每個訊息都會展開以包含 MIDI 狀態位元組。

收到 MIDI 系統專屬訊息時，不會傳送此訊息。 此訊息沒有可用的時間戳記。 針對時間戳記的輸入資料，您必須使用傳送給回呼函式的訊息。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>Mmsystem (包含 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[樂器數位介面 (MIDI)](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[MIDI 訊息](midi-messages.md)
</dt> </dl>

 

 





