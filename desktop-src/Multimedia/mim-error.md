---
title: 'MIM_ERROR 訊息 (Mmsystem .h) '
description: '\_收到不正確 midi 訊息時，會將 MIM 錯誤訊息傳送至 MIDI 輸入回撥函式。'
ms.assetid: ea720da5-1f18-4d0d-ac9d-45cd1c3219d6
keywords:
- MIM_ERROR 訊息 Windows 多媒體
topic_type:
- apiref
api_name:
- MIM_ERROR
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44793587b35c5d3e614c6a52f0cc9299e899b5feb4154f21b1ff278b96afde9d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119525058"
---
# <a name="mim_error-message"></a>MIM \_錯誤訊息

收到不正確 midi 訊息時，會將 **MIM \_ 錯誤** 訊息傳送至 MIDI 輸入回撥函式。


```C++
MIM_ERROR 
dwParam1 = dwMidiMessage 
dwParam2 = dwTimestamp 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="dwMidiMessage"></span><span id="dwmidimessage"></span><span id="DWMIDIMESSAGE"></span>*dwMidiMessage*
</dt> <dd>

收到的 MIDI 訊息無效。 訊息會以低序位位元組中訊息的第一個位元組，封裝成雙位元組值。

</dd> <dt>

<span id="dwTimestamp"></span><span id="dwtimestamp"></span><span id="DWTIMESTAMP"></span>*dwTimestamp*
</dt> <dd>

輸入裝置磁碟機收到訊息的時間。 時間戳記是以毫秒為單位來指定，在呼叫 [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) 函式時從零開始。

</dd> </dl>

## <a name="return-value"></a>傳回值

此訊息不會傳回值。

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

 

