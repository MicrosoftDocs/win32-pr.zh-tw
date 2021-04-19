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
ms.openlocfilehash: ee2d944d086f9c1a4ea7944f023321dfbc06d547
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999687"
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

若要啟用此事件，您必須在 \_ 呼叫 **EnableTrace** 時，在 *ENABLEFLAG* 參數中設定 DXMPERF VIDEOREND 旗標。 此旗標定義于 Dxmperf 標頭檔中，並包含在 DirectShow 基類中。

若要從 DirectShow 篩選記錄此事件，請使用 **PERFLOG \_ VIDEOREND** 宏（定義于 Dxmperf 中）。

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

 

 




