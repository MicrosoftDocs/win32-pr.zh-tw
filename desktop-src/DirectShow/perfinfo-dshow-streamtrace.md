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
# <a name="perfinfo_dshow_streamtrace-structure"></a><span data-ttu-id="ce47e-103">PERFINFO \_ DSHOW \_ STREAMTRACE 結構</span><span class="sxs-lookup"><span data-stu-id="ce47e-103">PERFINFO\_DSHOW\_STREAMTRACE structure</span></span>

<span data-ttu-id="ce47e-104">`PERFINFO_DSHOW_STREAMTRACE`結構包含 GUID STREAMTRACE 類型之 DirectShow 追蹤事件的資料 \_ 。</span><span class="sxs-lookup"><span data-stu-id="ce47e-104">The `PERFINFO_DSHOW_STREAMTRACE` structure contains data for a DirectShow trace event of type GUID\_STREAMTRACE.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce47e-105">語法</span><span class="sxs-lookup"><span data-stu-id="ce47e-105">Syntax</span></span>


```C++
typedef struct _PERFINFO_DSHOW_STREAMTRACE {
  ULONG     id;
  ULONG     reserved;
  ULONGLONG dshowClock;
  ULONGLONG data[4];
} PERFINFO_DSHOW_STREAMTRACE, *PPERFINFO_DSHOW_STREAMTRACE;
```



## <a name="members"></a><span data-ttu-id="ce47e-106">成員</span><span class="sxs-lookup"><span data-stu-id="ce47e-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="ce47e-107">**id**</span><span class="sxs-lookup"><span data-stu-id="ce47e-107">**id**</span></span>
</dt> <dd>

<span data-ttu-id="ce47e-108">事件識別碼。</span><span class="sxs-lookup"><span data-stu-id="ce47e-108">Event identifier.</span></span> <span data-ttu-id="ce47e-109">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="ce47e-109">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="ce47e-110">**保留**</span><span class="sxs-lookup"><span data-stu-id="ce47e-110">**reserved**</span></span>
</dt> <dd>

<span data-ttu-id="ce47e-111">保留的。</span><span class="sxs-lookup"><span data-stu-id="ce47e-111">Reserved.</span></span> <span data-ttu-id="ce47e-112">設定為零。</span><span class="sxs-lookup"><span data-stu-id="ce47e-112">Set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="ce47e-113">**dshowClock**</span><span class="sxs-lookup"><span data-stu-id="ce47e-113">**dshowClock**</span></span>
</dt> <dd>

<span data-ttu-id="ce47e-114">此事件的串流時間，以 100-毫微秒單位表示。</span><span class="sxs-lookup"><span data-stu-id="ce47e-114">Stream time for this event, in 100-nanosecond units.</span></span> <span data-ttu-id="ce47e-115">這個值是選擇性的，可以是零。</span><span class="sxs-lookup"><span data-stu-id="ce47e-115">This value is optional and can be zero.</span></span>

</dd> <dt>

<span data-ttu-id="ce47e-116">**data**</span><span class="sxs-lookup"><span data-stu-id="ce47e-116">**data**</span></span>
</dt> <dd>

<span data-ttu-id="ce47e-117">選擇性的事件資料，由四個 **ULONGLONG** 值組成。</span><span class="sxs-lookup"><span data-stu-id="ce47e-117">Optional event data consisting of four **ULONGLONG** values.</span></span> <span data-ttu-id="ce47e-118">這項資料的意義取決於事件識別碼。</span><span class="sxs-lookup"><span data-stu-id="ce47e-118">The meaning of this data depends on the event identifier.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ce47e-119">備註</span><span class="sxs-lookup"><span data-stu-id="ce47e-119">Remarks</span></span>

<span data-ttu-id="ce47e-120">系統會定義下列事件識別碼。</span><span class="sxs-lookup"><span data-stu-id="ce47e-120">The following event identifiers are defined.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ce47e-121">事件識別碼</span><span class="sxs-lookup"><span data-stu-id="ce47e-121">Event identifier</span></span></th>
<th><span data-ttu-id="ce47e-122">Description</span><span class="sxs-lookup"><span data-stu-id="ce47e-122">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ce47e-123">PERFINFO_STREAMTRACE_MPEG2DEMUX_PTS_TRANSLATION</span><span class="sxs-lookup"><span data-stu-id="ce47e-123">PERFINFO_STREAMTRACE_MPEG2DEMUX_PTS_TRANSLATION</span></span></td>
<td><span data-ttu-id="ce47e-124">當 <a href="mpeg-2-demultiplexer.md">Mpeg-2 信號</a> 標記篩選將呈現時間戳記（ (pt) 轉換為數據流時間）時記錄。</span><span class="sxs-lookup"><span data-stu-id="ce47e-124">Logged when the <a href="mpeg-2-demultiplexer.md">MPEG-2 Demultiplexer</a> filter converts a presentation time stamp (PTS) to stream time.</span></span>
<ul>
<li><span data-ttu-id="ce47e-125"><strong>資料</strong>[0]: Converted start time.</span><span class="sxs-lookup"><span data-stu-id="ce47e-125"><strong>data</strong>[0]: Converted start time.</span></span></li>
<li><span data-ttu-id="ce47e-126"><strong>資料</strong>[1]: Converted stop time.</span><span class="sxs-lookup"><span data-stu-id="ce47e-126"><strong>data</strong>[1]: Converted stop time.</span></span></li>
<li><span data-ttu-id="ce47e-127"><strong>資料</strong>[2]。</span><span class="sxs-lookup"><span data-stu-id="ce47e-127"><strong>data</strong>[2].</span></span> <span data-ttu-id="ce47e-128">輸入 pin 的資料流程識別碼。</span><span class="sxs-lookup"><span data-stu-id="ce47e-128">Stream identifier for the input pin.</span></span></li>
<li><span data-ttu-id="ce47e-129"><strong>資料</strong>[3]: PTS that was converted.</span><span class="sxs-lookup"><span data-stu-id="ce47e-129"><strong>data</strong>[3]: PTS that was converted.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ce47e-130">PERFINFO_STREAMTRACE_MPEG2DEMUX_SAMPLE_RECEIVE</span><span class="sxs-lookup"><span data-stu-id="ce47e-130">PERFINFO_STREAMTRACE_MPEG2DEMUX_SAMPLE_RECEIVE</span></span></td>
<td><span data-ttu-id="ce47e-131">當 MPEG 2 信號接收到範例時記錄。</span><span class="sxs-lookup"><span data-stu-id="ce47e-131">Logged when MPEG-2 Demultiplexer receives a sample.</span></span>
<ul>
<li><span data-ttu-id="ce47e-132"><strong>資料</strong> [0]: Current time returned by <a href="/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter"><strong>QueryPerformanceCounter</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="ce47e-132"><strong>data</strong>[0]: Current time returned by <a href="/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter"><strong>QueryPerformanceCounter</strong></a>.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ce47e-133">PERFINFO_STREAMTRACE_VMR_BEGIN_ADVISE</span><span class="sxs-lookup"><span data-stu-id="ce47e-133">PERFINFO_STREAMTRACE_VMR_BEGIN_ADVISE</span></span></td>
<td><span data-ttu-id="ce47e-134">當 VMR 排程轉譯的範例時，緊接在 VMR 呼叫 <a href="/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime"><strong>IReferenceClock：： AdviseTime</strong></a>之前所記錄的範例。</span><span class="sxs-lookup"><span data-stu-id="ce47e-134">Logged when the VMR schedules a sample for rendering, immediately before the VMR calls <a href="/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime"><strong>IReferenceClock::AdviseTime</strong></a>.</span></span>
<ul>
<li><span data-ttu-id="ce47e-135"><strong>資料</strong>[0]: Reference time when streaming began, which corresponds to stream time zero.</span><span class="sxs-lookup"><span data-stu-id="ce47e-135"><strong>data</strong>[0]: Reference time when streaming began, which corresponds to stream time zero.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ce47e-136">PERFINFO_STREAMTRACE_VMR_BEGIN_DECODE</span><span class="sxs-lookup"><span data-stu-id="ce47e-136">PERFINFO_STREAMTRACE_VMR_BEGIN_DECODE</span></span></td>
<td><span data-ttu-id="ce47e-137">當 VMR 開始解碼作業時記錄，也就是當解碼器呼叫 <a href="/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-beginframe"><strong>IAMVideoAccelerator：： BeginFrame</strong></a>時。</span><span class="sxs-lookup"><span data-stu-id="ce47e-137">Logged when the VMR begins a decoding operation—that is, when the decoder calls <a href="/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-beginframe"><strong>IAMVideoAccelerator::BeginFrame</strong></a>.</span></span> <span data-ttu-id="ce47e-138">沒有事件資料。</span><span class="sxs-lookup"><span data-stu-id="ce47e-138">No event data.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ce47e-139">PERFINFO_STREAMTRACE_VMR_BEGIN_DEINTERLACE</span><span class="sxs-lookup"><span data-stu-id="ce47e-139">PERFINFO_STREAMTRACE_VMR_BEGIN_DEINTERLACE</span></span></td>
<td><span data-ttu-id="ce47e-140">在 VMR 開始去交錯或影片合成作業時記錄。</span><span class="sxs-lookup"><span data-stu-id="ce47e-140">Logged when the VMR begins a deinterlacing or video compositing operation.</span></span> <span data-ttu-id="ce47e-141">沒有事件資料。</span><span class="sxs-lookup"><span data-stu-id="ce47e-141">No event data.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ce47e-142">PERFINFO_STREAMTRACE_VMR_DROPPED_FRAME</span><span class="sxs-lookup"><span data-stu-id="ce47e-142">PERFINFO_STREAMTRACE_VMR_DROPPED_FRAME</span></span></td>
<td><span data-ttu-id="ce47e-143">在 VMR 卸載框架時記錄;例如，如果範例已延遲。</span><span class="sxs-lookup"><span data-stu-id="ce47e-143">Logged when the VMR drops a frame; for example, if a sample was late.</span></span>
<ul>
<li><span data-ttu-id="ce47e-144"><strong>資料</strong>[0]: Sample start time.</span><span class="sxs-lookup"><span data-stu-id="ce47e-144"><strong>data</strong>[0]: Sample start time.</span></span></li>
<li><span data-ttu-id="ce47e-145"><strong>資料</strong>[1]: Sample end time.</span><span class="sxs-lookup"><span data-stu-id="ce47e-145"><strong>data</strong>[1]: Sample end time.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ce47e-146">PERFINFO_STREAMTRACE_VMR_END_ADVISE</span><span class="sxs-lookup"><span data-stu-id="ce47e-146">PERFINFO_STREAMTRACE_VMR_END_ADVISE</span></span></td>
<td><span data-ttu-id="ce47e-147">當 VMR 收到來自參考時鐘的建議通知時記錄。</span><span class="sxs-lookup"><span data-stu-id="ce47e-147">Logged when the VMR receives an advise notification from the reference clock.</span></span> <span data-ttu-id="ce47e-148">沒有事件資料。</span><span class="sxs-lookup"><span data-stu-id="ce47e-148">No event data.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ce47e-149">PERFINFO_STREAMTRACE_VMR_END_DECODE</span><span class="sxs-lookup"><span data-stu-id="ce47e-149">PERFINFO_STREAMTRACE_VMR_END_DECODE</span></span></td>
<td><span data-ttu-id="ce47e-150">當 VMR 結束解碼作業（亦即，當解碼器呼叫 <a href="/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-endframe"><strong>IAMVideoAccelerator：： EndFrame</strong></a>時）時記錄。</span><span class="sxs-lookup"><span data-stu-id="ce47e-150">Logged when the VMR ends a decoding operation—that is, when the decoder calls <a href="/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-endframe"><strong>IAMVideoAccelerator::EndFrame</strong></a>.</span></span> <span data-ttu-id="ce47e-151">沒有事件資料。</span><span class="sxs-lookup"><span data-stu-id="ce47e-151">No event data.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ce47e-152">PERFINFO_STREAMTRACE_VMR_END_DEINTERLACE</span><span class="sxs-lookup"><span data-stu-id="ce47e-152">PERFINFO_STREAMTRACE_VMR_END_DEINTERLACE</span></span></td>
<td><span data-ttu-id="ce47e-153">在 VMR 完成去交錯或影片合成作業時記錄。</span><span class="sxs-lookup"><span data-stu-id="ce47e-153">Logged when the VMR completes a deinterlacing or video compositing operation.</span></span> <span data-ttu-id="ce47e-154">沒有事件資料。</span><span class="sxs-lookup"><span data-stu-id="ce47e-154">No event data.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ce47e-155">PERFINFO_STREAMTRACE_VMR_RECEIVE</span><span class="sxs-lookup"><span data-stu-id="ce47e-155">PERFINFO_STREAMTRACE_VMR_RECEIVE</span></span></td>
<td><span data-ttu-id="ce47e-156">在 VMR 收到新的範例時記錄。</span><span class="sxs-lookup"><span data-stu-id="ce47e-156">Logged when the VMR receives a new sample.</span></span> <span data-ttu-id="ce47e-157">沒有事件資料。</span><span class="sxs-lookup"><span data-stu-id="ce47e-157">No event data.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ce47e-158">PERFINFO_STREAMTRACE_VMR_RENDER_TIME</span><span class="sxs-lookup"><span data-stu-id="ce47e-158">PERFINFO_STREAMTRACE_VMR_RENDER_TIME</span></span></td>
<td><span data-ttu-id="ce47e-159">在 VMR 完成呈現框架時記錄。</span><span class="sxs-lookup"><span data-stu-id="ce47e-159">Logged when the VMR finishes rendering a frame.</span></span>
<ul>
<li><span data-ttu-id="ce47e-160"><strong>資料</strong>[0]: Time that it took to render this frame.</span><span class="sxs-lookup"><span data-stu-id="ce47e-160"><strong>data</strong>[0]: Time that it took to render this frame.</span></span></li>
<li><span data-ttu-id="ce47e-161"><strong>資料</strong>[1]: Running average of frame rendering times.</span><span class="sxs-lookup"><span data-stu-id="ce47e-161"><strong>data</strong>[1]: Running average of frame rendering times.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="ce47e-162">若要從 DirectShow 篩選記錄此事件，請使用 **PERFLOG \_ STREAMTRACE** 函式，該函式定義于標頭檔 Dxmperf 中。</span><span class="sxs-lookup"><span data-stu-id="ce47e-162">To log this event from a DirectShow filter, use the **PERFLOG\_STREAMTRACE** function, which is defined in the header file Dxmperf.h.</span></span> <span data-ttu-id="ce47e-163">此標頭包含在 DirectShow 基類中。</span><span class="sxs-lookup"><span data-stu-id="ce47e-163">This header is included in the DirectShow base classes.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce47e-164">規格需求</span><span class="sxs-lookup"><span data-stu-id="ce47e-164">Requirements</span></span>



| <span data-ttu-id="ce47e-165">需求</span><span class="sxs-lookup"><span data-stu-id="ce47e-165">Requirement</span></span> | <span data-ttu-id="ce47e-166">值</span><span class="sxs-lookup"><span data-stu-id="ce47e-166">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ce47e-167">標頭</span><span class="sxs-lookup"><span data-stu-id="ce47e-167">Header</span></span><br/> | <dl> <span data-ttu-id="ce47e-168"><dt>Perfstruct。h</dt></span><span class="sxs-lookup"><span data-stu-id="ce47e-168"><dt>Perfstruct.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce47e-169">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ce47e-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce47e-170">DirectShow 結構</span><span class="sxs-lookup"><span data-stu-id="ce47e-170">DirectShow Structures</span></span>](directshow-structures.md)
</dt> <dt>

[<span data-ttu-id="ce47e-171">DirectShow 中的事件追蹤</span><span class="sxs-lookup"><span data-stu-id="ce47e-171">Event Tracing in DirectShow</span></span>](event-tracing-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="ce47e-172">追蹤事件 Guid</span><span class="sxs-lookup"><span data-stu-id="ce47e-172">Trace Event GUIDs</span></span>](trace-guids.md)
</dt> </dl>

 

 
