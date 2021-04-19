---
description: PERFINFO \_ DSHOW \_ AUDIOBREAK 結構包含 GUID AUDIOBREAK 類型之追蹤事件的資料 \_ 。當音訊資料流程中出現中斷時，DirectSound 轉譯器篩選器會記錄此事件。
ms.assetid: 9e7abdca-7d4c-4006-997f-9605f8d18e1d
title: 'PERFINFO_DSHOW_AUDIOBREAK 結構 (Perfstruct .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PERFINFO_DSHOW_AUDIOBREAK
api_type:
- HeaderDef
api_location:
- Perfstruct.h
ms.openlocfilehash: 599befea67b28acbedffd5c98ebce84aadf70838
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991198"
---
# <a name="perfinfo_dshow_audiobreak-structure"></a>PERFINFO \_ DSHOW \_ AUDIOBREAK 結構

`PERFINFO_DSHOW_AUDIOBREAK`結構包含 GUID AUDIOBREAK 類型之追蹤事件的資料 \_ 。

當音訊資料流程中出現中斷時， [DirectSound](directsound-renderer-filter.md) 轉譯器篩選器會記錄此事件。

## <a name="syntax"></a>語法


```C++
typedef struct PERFINFO_DSHOW_AUDIOBREAK {
  ULONGLONG cycleCounter;
  ULONGLONG dshowClock;
  ULONGLONG sampleTime;
  ULONGLONG sampleDuration;
} PERFINFO_DSHOW_AUDIOBREAK, *PPERFINFO_DSHOW_AUDIOBREAK;
```



## <a name="members"></a>成員

<dl> <dt>

**cycleCounter**
</dt> <dd>

最新的頻率週期計數 (RDTSC 指令) 。

</dd> <dt>

**dshowClock**
</dt> <dd>

DirectSound 緩衝區中的目前寫入位置。

</dd> <dt>

**sampleTime**
</dt> <dd>

DirectSound 緩衝區中的音訊中斷開頭。

</dd> <dt>

**sampleDuration**
</dt> <dd>

中斷的持續時間（以毫秒為單位）。

</dd> </dl>

## <a name="remarks"></a>備註

若要啟用此事件，您必須在 \_ 呼叫 **EnableTrace** 時，在 *ENABLEFLAG* 參數中設定 AUDIOBREAK 位旗標。 此旗標定義于 Dxmperf 標頭檔中，並包含在 DirectShow 基類中。

若要從 DirectShow 篩選記錄此事件，請使用 **PERFLOG \_ AUDIOBREAK** 宏（定義于 Dxmperf 中）。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Perfstruct。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[DirectShow 結構](directshow-structures.md)
</dt> <dt>

[DirectShow 中的事件追蹤](event-tracing-in-directshow.md)
</dt> <dt>

[追蹤事件 Guid](trace-guids.md)
</dt> </dl>

 

 




