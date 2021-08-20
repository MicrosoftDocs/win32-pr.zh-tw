---
title: 'MIM_DATA 訊息 (Mmsystem .h) '
description: '\_當 midi 輸入裝置收到 midi 訊息時，會將 MIM 的資料訊息傳送至 midi 輸入回撥函式。'
ms.assetid: 966aab84-420a-42ce-9989-da5910ced9c0
keywords:
- MIM_DATA 訊息 Windows 多媒體
topic_type:
- apiref
api_name:
- MIM_DATA
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bebbb9ca6016706605de8fed29e5fa5ebaf6055f4a730fb563323f306606b866
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118137287"
---
# <a name="mim_data-message"></a>MIM \_資料訊息

當 midi 輸入裝置收到 midi 訊息時，會將 **MIM 的 \_ 資料** 訊息傳送至 midi 輸入回撥函式。


```C++
MIM_DATA 
dwParam1 = dwMidiMessage 
dwParam2 = dwTimestamp 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="dwMidiMessage"></span><span id="dwmidimessage"></span><span id="DWMIDIMESSAGE"></span>*dwMidiMessage*
</dt> <dd>

收到的 MIDI 訊息。 訊息會封裝成雙字值，如下所示：



| 需求 | 值 | 描述 |
|-----------|-----------------|-----------------------------------------------------|
| 高單字 | 高序位位元組 | 未使用。                                           |
|           | 低序位位元組  | 視需要) ，包含第二個位元組的 MIDI 資料 (。  |
| 低字組  | 高序位位元組 | 當需要) 時，包含第一個 (的 MIDI 資料位元組。 |
|           | 低序位位元組  | 包含 MIDI 狀態。                           |



 

這兩個 MIDI 資料位元組是選擇性的，視 MIDI 狀態位元組而定。

</dd> <dt>

<span id="dwTimestamp"></span><span id="dwtimestamp"></span><span id="DWTIMESTAMP"></span>*dwTimestamp*
</dt> <dd>

輸入裝置磁碟機收到訊息的時間。 時間戳記是以毫秒為單位來指定，在呼叫 [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) 函式時從零開始。

</dd> </dl>

## <a name="return-value"></a>傳回值

此訊息不會傳回值。

## <a name="remarks"></a>備註

從 MIDI 輸入埠接收的 MIDI 訊息已停用執行中狀態;每個訊息都會展開以包含 MIDI 狀態位元組。

收到 MIDI 系統專屬訊息時，不會傳送此訊息。

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

 

