---
title: 'MM_MIM_MOREDATA 訊息 (Mmsystem .h) '
description: '\_ \_ 當 midi 輸入裝置收到 midi 訊息時，會將 MM mim MOREDATA 訊息傳送至回呼視窗，但應用程式不會快速處理 MIM \_ 資料訊息，而足以跟上輸入裝置磁碟機。'
ms.assetid: 25d507f9-01d4-4a9a-afdd-693d74e3bd22
keywords:
- MM_MIM_MOREDATA message Windows 多媒體
topic_type:
- apiref
api_name:
- MM_MIM_MOREDATA
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b67835a67c957a250fe1ae6d391f5ebd56d5301b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025069"
---
# <a name="mm_mim_moredata-message"></a>MM \_ MIM \_ MOREDATA 訊息

當 MIDI 輸入裝置收到 MIDI 訊息時，會將 **MM \_ mim \_ MOREDATA** 訊息傳送至回呼視窗，但應用程式不會快速處理 [**MIM \_ 資料**](mim-data.md) 訊息，而足以跟上輸入裝置磁碟機。 只有當應用程式在 MidiInOpen 函式 \_ \_ 的呼叫中指定了 MIDI IO 狀態[](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen)時，此視窗才會收到此訊息。


```C++
MM_MIM_MOREDATA 
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

指定收到的 MIDI 訊息。 訊息會封裝成雙字值，如下所示：



| 需求 | 值 |
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

如果您的應用程式將會以更快的速度接收 MIDI 資料，則您不應該使用視窗回呼機制。 若要最大化速度，請使用回呼函式，並使用 [**mim \_ MOREDATA**](mim-moredata.md) 訊息，而不是使用 \_ mim \_ MOREDATA。

應用程式應該只對 MM \_ MIM MOREDATA 訊息進行最低限度的處理 \_ 。  (特別是，應用程式在處理 MM MIM MOREDATA 時不應呼叫 [PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea) 函式 \_ \_ 。 ) 相反地，應用程式應該將事件資料放入緩衝區，然後再傳回。

當應用程式在一系列的 MOREDATA 訊息之後收到 [**mm \_ mim \_ 資料**](mm-mim-data.md) 訊息時 \_ ，它會攔截 \_ 傳入的 MIDI 事件，並且可以安全地呼叫需要大量時間的函式。

從 MIDI 輸入埠接收的 MIDI 訊息已停用執行中狀態;每個訊息都會展開以包含 MIDI 狀態位元組。

收到 MIDI 系統專屬訊息時，不會傳送此訊息。 此訊息沒有可用的時間戳記。 針對時間戳記的輸入資料，您必須使用傳送給回呼函式的訊息。

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

 

