---
description: PERFINFO \_ DSHOW \_ STREAMTRACE 結構包含 GUID STREAMTRACE 類型之 DirectShow 追蹤事件的資料 \_ 。
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
ms.openlocfilehash: 2bee4f3c11cf8462c8292cc412a6da5d9f9bfa78
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978632"
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



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>事件識別碼</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>PERFINFO_STREAMTRACE_MPEG2DEMUX_PTS_TRANSLATION</td>
<td>當 <a href="mpeg-2-demultiplexer.md">Mpeg-2 信號</a> 標記篩選將呈現時間戳記（ (pt) 轉換為數據流時間）時記錄。
<ul>
<li><strong>資料</strong>[0]: Converted start time.</li>
<li><strong>資料</strong>[1]: Converted stop time.</li>
<li><strong>資料</strong>[2]。 輸入 pin 的資料流程識別碼。</li>
<li><strong>資料</strong>[3]: PTS that was converted.</li>
</ul></td>
</tr>
<tr class="even">
<td>PERFINFO_STREAMTRACE_MPEG2DEMUX_SAMPLE_RECEIVE</td>
<td>當 MPEG 2 信號接收到範例時記錄。
<ul>
<li><strong>資料</strong> [0]: Current time returned by <a href="/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter"><strong>QueryPerformanceCounter</strong></a>。</li>
</ul></td>
</tr>
<tr class="odd">
<td>PERFINFO_STREAMTRACE_VMR_BEGIN_ADVISE</td>
<td>當 VMR 排程轉譯的範例時，緊接在 VMR 呼叫 <a href="/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime"><strong>IReferenceClock：： AdviseTime</strong></a>之前所記錄的範例。
<ul>
<li><strong>資料</strong>[0]: Reference time when streaming began, which corresponds to stream time zero.</li>
</ul></td>
</tr>
<tr class="even">
<td>PERFINFO_STREAMTRACE_VMR_BEGIN_DECODE</td>
<td>當 VMR 開始解碼作業時記錄，也就是當解碼器呼叫 <a href="/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-beginframe"><strong>IAMVideoAccelerator：： BeginFrame</strong></a>時。 沒有事件資料。</td>
</tr>
<tr class="odd">
<td>PERFINFO_STREAMTRACE_VMR_BEGIN_DEINTERLACE</td>
<td>在 VMR 開始去交錯或影片合成作業時記錄。 沒有事件資料。</td>
</tr>
<tr class="even">
<td>PERFINFO_STREAMTRACE_VMR_DROPPED_FRAME</td>
<td>在 VMR 卸載框架時記錄;例如，如果範例已延遲。
<ul>
<li><strong>資料</strong>[0]: Sample start time.</li>
<li><strong>資料</strong>[1]: Sample end time.</li>
</ul></td>
</tr>
<tr class="odd">
<td>PERFINFO_STREAMTRACE_VMR_END_ADVISE</td>
<td>當 VMR 收到來自參考時鐘的建議通知時記錄。 沒有事件資料。</td>
</tr>
<tr class="even">
<td>PERFINFO_STREAMTRACE_VMR_END_DECODE</td>
<td>當 VMR 結束解碼作業（亦即，當解碼器呼叫 <a href="/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-endframe"><strong>IAMVideoAccelerator：： EndFrame</strong></a>時）時記錄。 沒有事件資料。</td>
</tr>
<tr class="odd">
<td>PERFINFO_STREAMTRACE_VMR_END_DEINTERLACE</td>
<td>在 VMR 完成去交錯或影片合成作業時記錄。 沒有事件資料。</td>
</tr>
<tr class="even">
<td>PERFINFO_STREAMTRACE_VMR_RECEIVE</td>
<td>在 VMR 收到新的範例時記錄。 沒有事件資料。</td>
</tr>
<tr class="odd">
<td>PERFINFO_STREAMTRACE_VMR_RENDER_TIME</td>
<td>在 VMR 完成呈現框架時記錄。
<ul>
<li><strong>資料</strong>[0]: Time that it took to render this frame.</li>
<li><strong>資料</strong>[1]: Running average of frame rendering times.</li>
</ul></td>
</tr>
</tbody>
</table>



 

若要從 DirectShow 篩選記錄此事件，請使用 **PERFLOG \_ STREAMTRACE** 函式，該函式定義于標頭檔 Dxmperf 中。 此標頭包含在 DirectShow 基類中。

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

 

 
