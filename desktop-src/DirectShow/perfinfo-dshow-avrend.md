---
description: PERFINFO \_ DSHOW \_ AVREND 結構包含 GUID VIDEOREND 類型之追蹤事件的資料 \_ 。VMR 會在呈現框架之前立即記錄此事件。
ms.assetid: 95deda21-0ef4-4bf0-9fa3-826a813757b9
title: 'PERFINFO_DSHOW_AVREND 結構 (Perfstruct .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PERFINFO_DSHOW_AVREND
api_type:
- HeaderDef
api_location:
- Perfstruct.h
ms.openlocfilehash: 49cc76f4db1a5fae76678ee2d81f3e2fff0a6c5ca3d5c5532adebaec23f48215
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050708"
---
# <a name="perfinfo_dshow_avrend-structure"></a>PERFINFO \_ DSHOW \_ AVREND 結構

`PERFINFO_DSHOW_AVREND`結構包含 GUID VIDEOREND 類型之追蹤事件的資料 \_ 。

VMR 會在呈現框架之前立即記錄此事件。

## <a name="syntax"></a>語法


```C++
typedef struct PERFINFO_DSHOW_AVREND {
  ULONGLONG cycleCounter;
  ULONGLONG dshowClock;
  ULONGLONG sampleTime;
} PERFINFO_DSHOW_AVREND, *PPERFINFO_DSHOW_AVREND;
```



## <a name="members"></a>成員

<dl> <dt>

**cycleCounter**
</dt> <dd>

最新的頻率週期計數 (RDTSC 指令) 。

</dd> <dt>

**dshowClock**
</dt> <dd>

[**IReferenceClock：： GetTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime)方法所傳回的目前參考時間。

</dd> <dt>

**sampleTime**
</dt> <dd>

範例的開始時間。

</dd> </dl>

## <a name="remarks"></a>備註

若要啟用此事件，您必須在 \_ 呼叫 **EnableTrace** 時，在 *ENABLEFLAG* 參數中設定 DXMPERF VIDEOREND 旗標。 此旗標定義于標頭檔 Dxmperf 中，包含在 DirectShow 的基類中。

若要從 DirectShow 篩選記錄此事件，請使用 Dxmperf 中所定義的 **PERFLOG \_ VIDEOREND** 宏。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Perfstruct。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[DirectShow結構](directshow-structures.md)
</dt> <dt>

[DirectShow 中的事件追蹤](event-tracing-in-directshow.md)
</dt> <dt>

[追蹤事件 Guid](trace-guids.md)
</dt> </dl>

 

 




