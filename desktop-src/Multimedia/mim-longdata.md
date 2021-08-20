---
title: 'MIM_LONGDATA 訊息 (Mmsystem .h) '
description: '\_當系統專屬的緩衝區已填滿資料，並傳回給應用程式時，會將 MIM LONGDATA 訊息傳送至 MIDI 輸入回撥函數。'
ms.assetid: 3a11ed21-e7c5-4b78-9536-f0d862e26a02
keywords:
- MIM_LONGDATA 訊息 Windows 多媒體
topic_type:
- apiref
api_name:
- MIM_LONGDATA
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82605835ce8ac231346014215c854abfe9ae7a55fd81e81b8d6214fb8a230327
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118137209"
---
# <a name="mim_longdata-message"></a>MIM \_LONGDATA 訊息

當系統專屬的緩衝區已填滿資料，並傳回給應用程式時，會將 **MIM \_ LONGDATA** 訊息傳送至 MIDI 輸入回撥函數。


```C++
MIM_LONGDATA 
dwParam1 = (DWORD) lpMidiHdr 
dwParam2 = dwTimestamp 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*lpMidiHdr*
</dt> <dd>

識別輸入緩衝區之 [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) 結構的指標。

</dd> <dt>

<span id="dwTimestamp"></span><span id="dwtimestamp"></span><span id="DWTIMESTAMP"></span>*dwTimestamp*
</dt> <dd>

輸入裝置磁碟機收到資料的時間。 時間戳記是以毫秒為單位來指定，在呼叫 [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) 函式時從零開始。

</dd> </dl>

## <a name="return-value"></a>傳回值

此訊息不會傳回值。

## <a name="remarks"></a>備註

傳回的緩衝區可能不完整。 若要判斷記錄到傳回緩衝區的位元組數目，請使用 *lpMidiHdr* 所指定之 [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr)結構的 **dwBytesRecorded** 成員。

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

 

