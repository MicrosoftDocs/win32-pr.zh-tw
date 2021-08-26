---
description: PERFINFO \_ DSHOW \_ STREAMTRACE 結構包含 GUID STREAMTRACE 類型 DirectShow 追蹤事件的資料 \_ 。
ms.assetid: 41fbf95c-e86c-4c64-898f-01fbf5f8839c
title: 'PERFINFO_DSHOW_STREAMTRACE 結構 (Perfstruct .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PERFINFO_DSHOW_STREAMTRACE
api_type:
- HeaderDef
api_location:
- Perfstruct.h
ms.openlocfilehash: e17d013d90b133f9c6819b8d9ddf4b5970582cae
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477003"
---
# <a name="perfinfo_dshow_streamtrace-structure"></a>PERFINFO \_ DSHOW \_ STREAMTRACE 結構

`PERFINFO_DSHOW_STREAMTRACE`結構包含 GUID STREAMTRACE 類型之 DirectShow 追蹤事件的資料 \_ 。

## <a name="syntax"></a>語法


```C++
typedef struct _PERFINFO_DSHOW_STREAMTRACE {
  ULONG     id;
  ULONG     reserved;
  ULONGLONG dshowClock;
  ULONGLONG data[4];
} PERFINFO_DSHOW_STREAMTRACE, *PPERFINFO_DSHOW_STREAMTRACE;
```



## <a name="members"></a>成員

<dl> <dt>

**id**
</dt> <dd>

事件識別碼。 請參閱＜備註＞。

</dd> <dt>

**保留**
</dt> <dd>

保留的。 設定為零。

</dd> <dt>

**dshowClock**
</dt> <dd>

此事件的串流時間，以 100-毫微秒單位表示。 這個值是選擇性的，可以是零。

</dd> <dt>

**data**
</dt> <dd>

選擇性的事件資料，由四個 **ULONGLONG** 值組成。 這項資料的意義取決於事件識別碼。

</dd> </dl>

## <a name="remarks"></a>備註

系統會定義下列事件識別碼。




| 事件識別碼 | Description | 
|------------------|-------------|
| PERFINFO_STREAMTRACE_MPEG2DEMUX_PTS_TRANSLATION | 當 <a href="mpeg-2-demultiplexer.md">Mpeg-2 信號</a> 標記篩選將呈現時間戳記（ (pt) 轉換為數據流時間）時記錄。<ul><li><strong>資料</strong>[0]：已轉換的開始時間。</li><li><strong>資料</strong>[1]：已轉換的停止時間。</li><li><strong>資料</strong>[2]。 輸入 pin 的資料流程識別碼。</li><li><strong>資料</strong>[3]：已轉換的 pt。</li></ul> | 
| PERFINFO_STREAMTRACE_MPEG2DEMUX_SAMPLE_RECEIVE | 當 MPEG 2 信號接收到範例時記錄。<ul><li><strong>資料</strong>[0]： <a href="/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter"><strong>QueryPerformanceCounter</strong></a>傳回的目前時間。</li></ul> | 
| PERFINFO_STREAMTRACE_VMR_BEGIN_ADVISE | 當 VMR 排程轉譯的範例時，緊接在 VMR 呼叫 <a href="/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime"><strong>IReferenceClock：： AdviseTime</strong></a>之前所記錄的範例。<ul><li><strong>資料</strong>[0]：資料流程開始時的參考時間，對應于資料流程時間零。</li></ul> | 
| PERFINFO_STREAMTRACE_VMR_BEGIN_DECODE | 當 VMR 開始解碼作業時記錄，也就是當解碼器呼叫 <a href="/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-beginframe"><strong>IAMVideoAccelerator：： BeginFrame</strong></a>時。 沒有事件資料。 | 
| PERFINFO_STREAMTRACE_VMR_BEGIN_DEINTERLACE | 在 VMR 開始去交錯或影片合成作業時記錄。 沒有事件資料。 | 
| PERFINFO_STREAMTRACE_VMR_DROPPED_FRAME | 在 VMR 卸載框架時記錄;例如，如果範例已延遲。<ul><li><strong>資料</strong>[0]：取樣開始時間。</li><li><strong>資料</strong>[1]：範例結束時間。</li></ul> | 
| PERFINFO_STREAMTRACE_VMR_END_ADVISE | 當 VMR 收到來自參考時鐘的建議通知時記錄。 沒有事件資料。 | 
| PERFINFO_STREAMTRACE_VMR_END_DECODE | 當 VMR 結束解碼作業（亦即，當解碼器呼叫 <a href="/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-endframe"><strong>IAMVideoAccelerator：： EndFrame</strong></a>時）時記錄。 沒有事件資料。 | 
| PERFINFO_STREAMTRACE_VMR_END_DEINTERLACE | 在 VMR 完成去交錯或影片合成作業時記錄。 沒有事件資料。 | 
| PERFINFO_STREAMTRACE_VMR_RECEIVE | 在 VMR 收到新的範例時記錄。 沒有事件資料。 | 
| PERFINFO_STREAMTRACE_VMR_RENDER_TIME | 在 VMR 完成呈現框架時記錄。<ul><li><strong>資料</strong>[0]：轉譯此框架所花費的時間。</li><li><strong>資料</strong>[1]：平均顯示畫面格轉譯時間。</li></ul> | 




 

若要從 DirectShow 篩選準則記錄此事件，請使用 **PERFLOG \_ STREAMTRACE** 函式，該函式定義于標頭檔 Dxmperf 中。 此標頭包含在 DirectShow 的基類中。

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

 

 
