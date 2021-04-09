---
title: 'MIM_MOREDATA 訊息 (Mmsystem .h) '
description: '\_當 midi 輸入裝置收到 midi 訊息，但應用程式未及時處理 MIM \_ 資料訊息，以跟上輸入裝置磁碟機時，就會將 mim MOREDATA 訊息傳送至 midi 輸入回撥函式。'
ms.assetid: 74ed46ab-a18e-4df5-bf36-ab3dec7fafa5
keywords:
- MIM_MOREDATA message Windows 多媒體
topic_type:
- apiref
api_name:
- MIM_MOREDATA
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ececb41bc0f9dc0cef187c083afc72ba5fc899a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686643"
---
# <a name="mim_moredata-message"></a>MIM \_ MOREDATA 訊息

當 MIDI 輸入裝置收到 MIDI 訊息，但應用程式未及時處理 [**MIM \_ 資料**](mim-data.md)訊息，以跟上輸入裝置磁碟機時，就會將 **mim \_ MOREDATA** 訊息傳送至 midi 輸入回撥函式。 只有當應用程式在 MidiInOpen 函式 \_ \_ 的呼叫中指定 MIDI IO 狀態[](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen)時，回呼函式才會收到此訊息。


```C++
MIM_MOREDATA 
dwParam1 = dwMidiMessage 
dwParam2 = dwTimestamp 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="dwMidiMessage"></span><span id="dwmidimessage"></span><span id="DWMIDIMESSAGE"></span>*dwMidiMessage*
</dt> <dd>

指定收到的 MIDI 訊息。 訊息會封裝成 **DWORD** 值，如下所示：



| 需求 | 值 |
|-----------|-----------------|-----------------------------------------------------|
| 高單字 | 高序位位元組 | 未使用。                                           |
|           | 低序位位元組  | 視需要) ，包含第二個位元組的 MIDI 資料 (。  |
| 低字組  | 高序位位元組 | 當需要) 時，包含第一個 (的 MIDI 資料位元組。 |
|           | 低序位位元組  | 包含 MIDI 狀態。                           |



 

這兩個 MIDI 資料位元組是選擇性的，視 MIDI 狀態位元組而定。

</dd> <dt>

<span id="dwTimestamp"></span><span id="dwtimestamp"></span><span id="DWTIMESTAMP"></span>*dwTimestamp*
</dt> <dd>

指定輸入裝置磁碟機接收訊息的時間。 時間戳記是以毫秒為單位來指定，從0開始呼叫 [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) 函式。

</dd> </dl>

## <a name="return-value"></a>傳回值

此訊息不會傳回值。

## <a name="remarks"></a>備註

應用程式應該只進行最低限度的 MIM \_ MOREDATA 訊息處理。  (特別是，應用程式在處理 MIM MOREDATA 時不應呼叫 [PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea) 函式 \_ 。 ) 相反地，應用程式應該將事件資料放入緩衝區，然後再傳回。

當應用程式在一系列的 MIM MOREDATA 訊息之後收到 [**mim \_ 資料**](mim-data.md) 訊息時 \_ ，它會攔截傳入的 MIDI 事件，並且可以安全地呼叫需要大量時間的函式。

從 MIDI 輸入埠接收的 MIDI 訊息已停用執行中狀態;每個訊息都會展開以包含 MIDI 狀態位元組。

收到 MIDI 系統專屬訊息時，不會傳送此訊息。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>Mmsystem (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[樂器數位介面 (MIDI)](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[MIDI 訊息](midi-messages.md)
</dt> </dl>

 

