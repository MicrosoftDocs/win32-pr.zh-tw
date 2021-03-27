---
description: WNODE \_ 標頭結構是事件 \_ 追蹤屬性結構的成員 \_ 。
ms.assetid: 862a8f46-a326-48c6-92b7-8bb667837bb7
title: 'WNODE_HEADER 結構 (Wmistr .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WNODE_HEADER
api_type:
- HeaderDef
api_location:
- Wmistr.h
ms.openlocfilehash: 6a2ed615d2b67cbd47a817234a14b7cf1221f601
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/19/2021
ms.locfileid: "104974789"
---
# <a name="wnode_header-structure"></a><span data-ttu-id="b041f-103">WNODE \_ 標頭結構</span><span class="sxs-lookup"><span data-stu-id="b041f-103">WNODE\_HEADER structure</span></span>

<span data-ttu-id="b041f-104">**WNODE \_ 標頭** 結構是 [**事件 \_ 追蹤 \_ 屬性**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)結構的成員。</span><span class="sxs-lookup"><span data-stu-id="b041f-104">The **WNODE\_HEADER** structure is a member of the [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="b041f-105">語法</span><span class="sxs-lookup"><span data-stu-id="b041f-105">Syntax</span></span>


```C++
typedef struct _WNODE_HEADER {
  ULONG BufferSize;
  ULONG ProviderId;
  union {
    ULONG64 HistoricalContext;
    struct {
      ULONG Version;
      ULONG Linkage;
    };
  };
  union {
    HANDLE        KernelHandle;
    LARGE_INTEGER TimeStamp;
  };
  GUID  Guid;
  ULONG ClientContext;
  ULONG Flags;
} WNODE_HEADER, *PWNODE_HEADER;
```



## <a name="members"></a><span data-ttu-id="b041f-106">成員</span><span class="sxs-lookup"><span data-stu-id="b041f-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="b041f-107">**BufferSize**</span><span class="sxs-lookup"><span data-stu-id="b041f-107">**BufferSize**</span></span>
</dt> <dd>

<span data-ttu-id="b041f-108">事件追蹤會話屬性配置的記憶體大小總計（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="b041f-108">Total size of memory allocated, in bytes, for the event tracing session properties.</span></span> <span data-ttu-id="b041f-109">記憶體的大小必須包含 [**事件 \_ 追蹤 \_ 屬性**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) 結構的空間，以及在記憶體中結構後面的會話名稱字串和記錄檔名稱字串。</span><span class="sxs-lookup"><span data-stu-id="b041f-109">The size of memory must include the room for the [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure plus the session name string and log file name string that follow the structure in memory.</span></span>

</dd> <dt>

<span data-ttu-id="b041f-110">**ProviderId**</span><span class="sxs-lookup"><span data-stu-id="b041f-110">**ProviderId**</span></span>
</dt> <dd>

<span data-ttu-id="b041f-111">保留供內部使用。</span><span class="sxs-lookup"><span data-stu-id="b041f-111">Reserved for internal use.</span></span>

</dd> <dt>

<span data-ttu-id="b041f-112">**HistoricalCoNtext**</span><span class="sxs-lookup"><span data-stu-id="b041f-112">**HistoricalContext**</span></span>
</dt> <dd>

<span data-ttu-id="b041f-113">在輸出時，事件追蹤會話的控制碼。</span><span class="sxs-lookup"><span data-stu-id="b041f-113">On output, the handle to the event tracing session.</span></span>

</dd> <dt>

<span data-ttu-id="b041f-114">**版本**</span><span class="sxs-lookup"><span data-stu-id="b041f-114">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="b041f-115">保留供內部使用。</span><span class="sxs-lookup"><span data-stu-id="b041f-115">Reserved for internal use.</span></span>

</dd> <dt>

<span data-ttu-id="b041f-116">**連結**</span><span class="sxs-lookup"><span data-stu-id="b041f-116">**Linkage**</span></span>
</dt> <dd>

<span data-ttu-id="b041f-117">保留供內部使用。</span><span class="sxs-lookup"><span data-stu-id="b041f-117">Reserved for internal use.</span></span>

</dd> <dt>

<span data-ttu-id="b041f-118">**KernelHandle**</span><span class="sxs-lookup"><span data-stu-id="b041f-118">**KernelHandle**</span></span>
</dt> <dd>

<span data-ttu-id="b041f-119">保留供內部使用。</span><span class="sxs-lookup"><span data-stu-id="b041f-119">Reserved for internal use.</span></span>

</dd> <dt>

<span data-ttu-id="b041f-120">**時間 戳**</span><span class="sxs-lookup"><span data-stu-id="b041f-120">**TimeStamp**</span></span>
</dt> <dd>

<span data-ttu-id="b041f-121">此結構中資訊的更新時間，自1601年1月1日午夜起的 100-毫微秒間隔時間。</span><span class="sxs-lookup"><span data-stu-id="b041f-121">Time at which the information in this structure was updated, in 100-nanosecond intervals since midnight, January 1, 1601.</span></span>

</dd> <dt>

<span data-ttu-id="b041f-122">**Guid**</span><span class="sxs-lookup"><span data-stu-id="b041f-122">**Guid**</span></span>
</dt> <dd>

<span data-ttu-id="b041f-123">您為會話定義的 GUID。</span><span class="sxs-lookup"><span data-stu-id="b041f-123">The GUID that you define for the session.</span></span>

<span data-ttu-id="b041f-124">若為 NT Kernel 記錄器會話，請將這個成員設定為 **SystemTraceControlGuid**。</span><span class="sxs-lookup"><span data-stu-id="b041f-124">For an NT Kernel Logger session, set this member to **SystemTraceControlGuid**.</span></span>

<span data-ttu-id="b041f-125">如果這個成員設定為 **SystemTraceControlGuid** 或 **GlobalLoggerGuid**，記錄器將會是系統記錄器。</span><span class="sxs-lookup"><span data-stu-id="b041f-125">If this member is set to **SystemTraceControlGuid** or **GlobalLoggerGuid**, the logger will be a system logger.</span></span>

<span data-ttu-id="b041f-126">若為私用記錄器會話，請將這個成員設定為您要為會話啟用的提供者 GUID。</span><span class="sxs-lookup"><span data-stu-id="b041f-126">For a private logger session, set this member to the provider's GUID that you are going to enable for the session.</span></span>

<span data-ttu-id="b041f-127">如果您啟動不是核心記錄器或私用記錄器會話的會話，就不需要指定會話 GUID。</span><span class="sxs-lookup"><span data-stu-id="b041f-127">If you start a session that is not a kernel logger or private logger session, you do not have to specify a session GUID.</span></span> <span data-ttu-id="b041f-128">如果您未指定 GUID，ETW 會為您建立一個 GUID。</span><span class="sxs-lookup"><span data-stu-id="b041f-128">If you do not specify a GUID, ETW creates one for you.</span></span> <span data-ttu-id="b041f-129">只有當您想要變更與特定會話相關聯的預設許可權時，才需要指定會話 GUID。</span><span class="sxs-lookup"><span data-stu-id="b041f-129">You need to specify a session GUID only if you want to change the default permissions associated with a specific session.</span></span> <span data-ttu-id="b041f-130">如需詳細資訊，請參閱 EventAccessControl 函數。</span><span class="sxs-lookup"><span data-stu-id="b041f-130">For details, see the EventAccessControl function.</span></span>

<span data-ttu-id="b041f-131">您無法以相同的會話 GUID 啟動多個會話。</span><span class="sxs-lookup"><span data-stu-id="b041f-131">You cannot start more than one session with the same session GUID.</span></span>

<span data-ttu-id="b041f-132">**在 Windows Vista 之前：** 您可以使用相同的會話 GUID 來啟動一個以上的會話。</span><span class="sxs-lookup"><span data-stu-id="b041f-132">**Prior to Windows Vista:** You can start more than one session with the same session GUID.</span></span>

</dd> <dt>

<span data-ttu-id="b041f-133">**ClientContext**</span><span class="sxs-lookup"><span data-stu-id="b041f-133">**ClientContext**</span></span>
</dt> <dd>

<span data-ttu-id="b041f-134">記錄每個事件的時間戳記時所要使用的時鐘解析。</span><span class="sxs-lookup"><span data-stu-id="b041f-134">Clock resolution to use when logging the time stamp for each event.</span></span> <span data-ttu-id="b041f-135">預設值是 (QPC) 的 Query 效能計數器。</span><span class="sxs-lookup"><span data-stu-id="b041f-135">The default is Query performance counter (QPC).</span></span>

<span data-ttu-id="b041f-136">**在 Windows Vista 之前：** 預設值為系統時間。</span><span class="sxs-lookup"><span data-stu-id="b041f-136">**Prior to Windows Vista:** The default is system time.</span></span>

<span data-ttu-id="b041f-137">**在 Windows 10 之前，版本1703：** 任何系統記錄器都不能同時使用2個以上的不同時鐘類型。</span><span class="sxs-lookup"><span data-stu-id="b041f-137">**Prior to Windows 10, version 1703:** No more than 2 distinct clock types can be used simultaneously by any system loggers.</span></span>

<span data-ttu-id="b041f-138">**從 Windows 10 開始，版本1703：** 已移除時鐘類型限制。</span><span class="sxs-lookup"><span data-stu-id="b041f-138">**Starting with Windows 10, version 1703:** The clock type restriction has been removed.</span></span> <span data-ttu-id="b041f-139">所有三種時鐘類型現在都可以由系統記錄器同時使用。</span><span class="sxs-lookup"><span data-stu-id="b041f-139">All three clock types can now be used simultaneously by system loggers.</span></span>

<span data-ttu-id="b041f-140">您可以指定下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="b041f-140">You can specify one of the following values.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b041f-141">值</span><span class="sxs-lookup"><span data-stu-id="b041f-141">Value</span></span></th>
<th><span data-ttu-id="b041f-142">意義</span><span class="sxs-lookup"><span data-stu-id="b041f-142">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <span data-ttu-id="b041f-143"><dt>1</dt> </span><span class="sxs-lookup"><span data-stu-id="b041f-143"><dt>1</dt> </span></span></dl></td>
<td><span data-ttu-id="b041f-144"> (QPC) 的 Query 效能計數器。</span><span class="sxs-lookup"><span data-stu-id="b041f-144">Query performance counter (QPC).</span></span> <span data-ttu-id="b041f-145">QPC 計數器會提供高解析度的時間戳記，而不會受到系統時鐘的調整影響。</span><span class="sxs-lookup"><span data-stu-id="b041f-145">The QPC counter provides a high-resolution time stamp that is not affected by adjustments to the system clock.</span></span> <span data-ttu-id="b041f-146">事件中儲存的時間戳記相當於從 QueryPerformanceCounter API 傳回的值。</span><span class="sxs-lookup"><span data-stu-id="b041f-146">The time stamp stored in the event is equivalent to the value returned from the QueryPerformanceCounter API.</span></span> <span data-ttu-id="b041f-147">如需此時間戳記特性的詳細資訊，請參閱取得 <a href="/windows/win32/sysinfo/acquiring-high-resolution-time-stamps">高解析度的時間戳記</a>。</span><span class="sxs-lookup"><span data-stu-id="b041f-147">For more information on the characteristics of this time stamp, see <a href="/windows/win32/sysinfo/acquiring-high-resolution-time-stamps">Acquiring high-resolution time stamps</a>.</span></span><br/> <span data-ttu-id="b041f-148">如果您有高事件率，或取用者合併來自不同緩衝區的事件，則應該使用此解析。</span><span class="sxs-lookup"><span data-stu-id="b041f-148">You should use this resolution if you have high event rates or if the consumer merges events from different buffers.</span></span> <span data-ttu-id="b041f-149">在這些情況下，QPC 時間戳記的精確度和穩定性可讓您更精確地從不同的緩衝區排序事件。</span><span class="sxs-lookup"><span data-stu-id="b041f-149">In these cases, the precision and stability of the QPC time stamp allows for better accuracy in ordering the events from different buffers.</span></span> <span data-ttu-id="b041f-150">不過，QPC 時間戳記並不會反映系統時鐘的更新，例如，如果系統時鐘因為與 NTP 伺服器同步處理而在追蹤進行中進行同步處理，則追蹤中的 QPC 時間戳記會繼續反映時間，就像未發生任何更新一樣。</span><span class="sxs-lookup"><span data-stu-id="b041f-150">However, the QPC time stamp will not reflect updates to the system clock, e.g. if the system clock is adjusted forward due to synchronization with an NTP server while the trace is in progress, the QPC time stamps in the trace will continue to reflect time as if no update had occurred.</span></span><br/> <span data-ttu-id="b041f-151">若要判斷解決方式，請在取用事件時使用<a href="/windows/win32/api/evntrace/ns-evntrace-trace_logfile_header"><strong>TRACE_LOGFILE_HEADER</strong></a>的<strong>PerfFreq</strong>成員。</span><span class="sxs-lookup"><span data-stu-id="b041f-151">To determine the resolution, use the <strong>PerfFreq</strong> member of <a href="/windows/win32/api/evntrace/ns-evntrace-trace_logfile_header"><strong>TRACE_LOGFILE_HEADER</strong></a> when consuming the event.</span></span><br/> <span data-ttu-id="b041f-152">若要將事件的時間戳記轉換為 100-ns 單位，請使用下列轉換公式：</span><span class="sxs-lookup"><span data-stu-id="b041f-152">To convert an event’s time stamp into 100-ns units, use the following conversion formula:</span></span> <br/> <span data-ttu-id="b041f-153">scaledTimestamp = eventRecord. EventHeader. QuadPart \* 10000000.0/logfileHeader. PerfFreq</span><span class="sxs-lookup"><span data-stu-id="b041f-153">scaledTimestamp = eventRecord.EventHeader.TimeStamp.QuadPart \* 10000000.0 / logfileHeader.PerfFreq.QuadPart</span></span><br/> <span data-ttu-id="b041f-154">請注意，在較舊的電腦上，時間戳記可能不准確，因為由於硬體錯誤，計數器有時會向前跳過。</span><span class="sxs-lookup"><span data-stu-id="b041f-154">Note that on older computers, the time stamp may not be accurate because the counter sometimes skips forward due to hardware errors.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="b041f-155"><dt>2</dt> </span><span class="sxs-lookup"><span data-stu-id="b041f-155"><dt>2</dt> </span></span></dl></td>
<td><span data-ttu-id="b041f-156">系統時間。</span><span class="sxs-lookup"><span data-stu-id="b041f-156">System time.</span></span> <span data-ttu-id="b041f-157">系統時間會提供時間戳記來追蹤系統時鐘的變更，例如，如果系統時鐘因為與 NTP 伺服器同步處理而在追蹤進行中進行同步處理，則追蹤中的系統時間戳記也會向前跳到符合系統時鐘的新設定。</span><span class="sxs-lookup"><span data-stu-id="b041f-157">The system time provides a time stamp that tracks changes to the system’s clock, e.g. if the system clock is adjusted forward due to synchronization with an NTP server while the trace is in progress, the System Time time stamps in the trace will also jump forward to match the new setting of the system clock.</span></span> <br/>
<ul>
<li><span data-ttu-id="b041f-158">在 Windows 10 之前的系統上，儲存在事件中的時間戳記相當於 GetSystemTimeAsFileTime API 所傳回的值。</span><span class="sxs-lookup"><span data-stu-id="b041f-158">On systems prior to Windows 10, the time stamp stored in the event is equivalent to the value returned from the GetSystemTimeAsFileTime API.</span></span></li>
<li><span data-ttu-id="b041f-159">在 Windows 10 或更新版本上，儲存在事件中的時間戳記相當於 GetSystemTimePreciseAsFileTime API 所傳回的值。</span><span class="sxs-lookup"><span data-stu-id="b041f-159">On Windows 10 or later, the time stamp stored in the event is equivalent to the value returned from the GetSystemTimePreciseAsFileTime API.</span></span></li>
</ul>
<span data-ttu-id="b041f-160">在 Windows 10 之前，此時間戳記的解決方式是系統時鐘滴答的解析度，如 TRACE_LOGFILE_HEADER 的 TimerResolution 成員所表示。</span><span class="sxs-lookup"><span data-stu-id="b041f-160">Prior to Windows 10, the resolution of this time stamp was the resolution of a system clock tick, as indicated by the TimerResolution member of TRACE_LOGFILE_HEADER.</span></span> <span data-ttu-id="b041f-161">從 Windows 10 開始，這個時間戳記的解決方法是效能計數器解析度，如 TRACE_LOGFILE_HEADER 的 PerfFreq 成員所示。</span><span class="sxs-lookup"><span data-stu-id="b041f-161">Starting with Windows 10, the resolution of this time stamp is the performance counter resolution, as indicated by the PerfFreq member of TRACE_LOGFILE_HEADER.</span></span><br/> <span data-ttu-id="b041f-162">若要將事件的時間戳記轉換為 100-ns 單位，請使用下列轉換公式：</span><span class="sxs-lookup"><span data-stu-id="b041f-162">To convert an event’s time stamp into 100-ns units, use the following conversion formula:</span></span> <br/> <span data-ttu-id="b041f-163">scaledTimestamp = eventRecord. EventHeader. QuadPart</span><span class="sxs-lookup"><span data-stu-id="b041f-163">scaledTimestamp = eventRecord.EventHeader.TimeStamp.QuadPart</span></span><br/> <span data-ttu-id="b041f-164">請注意，在 Windows 10 之前，在執行作業系統的系統上捕捉到事件時，如果事件的數量很高，則系統時間的解析可能不夠好，無法判斷事件的順序。</span><span class="sxs-lookup"><span data-stu-id="b041f-164">Note that when events are captured on a system running an OS prior to Windows 10, if the volume of events is high, the resolution for system time may not be fine enough to determine the sequence of events.</span></span> <span data-ttu-id="b041f-165">在此情況下，一組事件將會有相同的時間戳記，但 ETW 傳遞事件的順序可能不正確。</span><span class="sxs-lookup"><span data-stu-id="b041f-165">In this case, a set of events will have the same time stamp, but the order in which ETW delivers the events may not be correct.</span></span> <span data-ttu-id="b041f-166">從 Windows 10 開始，系統會以額外的精確度來捕捉時間戳記，但在捕捉追蹤時，系統時鐘已調整的情況下，可能仍會發生某些不穩定的情況。</span><span class="sxs-lookup"><span data-stu-id="b041f-166">Starting with Windows 10, the time stamp is captured with additional precision, though some instability may still occur in cases where the system clock was adjusted while the trace was being captured.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="b041f-167"><dt>3</dt> </span><span class="sxs-lookup"><span data-stu-id="b041f-167"><dt>3</dt> </span></span></dl></td>
<td><span data-ttu-id="b041f-168">CPU 週期計數器。</span><span class="sxs-lookup"><span data-stu-id="b041f-168">CPU cycle counter.</span></span> <span data-ttu-id="b041f-169">CPU 計數器提供最高的解析時間戳記，而且是要抓取的最不耗用資源。</span><span class="sxs-lookup"><span data-stu-id="b041f-169">The CPU counter provides the highest resolution time stamp and is the least resource-intensive to retrieve.</span></span> <span data-ttu-id="b041f-170">不過，CPU 計數器不可靠，不應該用於生產環境。</span><span class="sxs-lookup"><span data-stu-id="b041f-170">However, the CPU counter is unreliable and should not be used in production.</span></span> <span data-ttu-id="b041f-171">例如，在某些電腦上，計時器將會因為溫度和電源變更而變更頻率，除了在某些狀態下停止。</span><span class="sxs-lookup"><span data-stu-id="b041f-171">For example, on some computers, the timers will change frequency due to thermal and power changes, in addition to stopping in some states.</span></span><br/> <span data-ttu-id="b041f-172">若要判斷解決方式，請在取用事件時使用<a href="/windows/win32/api/evntrace/ns-evntrace-trace_logfile_header"><strong>TRACE_LOGFILE_HEADER</strong></a>的<strong>CpuSpeedInMHz</strong>成員。</span><span class="sxs-lookup"><span data-stu-id="b041f-172">To determine the resolution, use the <strong>CpuSpeedInMHz</strong> member of <a href="/windows/win32/api/evntrace/ns-evntrace-trace_logfile_header"><strong>TRACE_LOGFILE_HEADER</strong></a> when consuming the event.</span></span><br/> <span data-ttu-id="b041f-173">如果您的硬體不支援此時鐘類型，ETW 會使用系統時間。</span><span class="sxs-lookup"><span data-stu-id="b041f-173">If your hardware does not support this clock type, ETW uses system time.</span></span><br/> <span data-ttu-id="b041f-174"><strong>Windows Server 2003、WINDOWS xp 加裝 SP1 和 WINDOWS xp：</strong> 此值不受支援，它是在 Windows Server 2003 SP1 和 Windows XP （含 SP2）中引進。</span><span class="sxs-lookup"><span data-stu-id="b041f-174"><strong>Windows Server 2003, Windows XP with SP1 and Windows XP:</strong> This value is not supported, it was introduced in Windows Server 2003 with SP1 and Windows XP with SP2.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="b041f-175">**Windows 2000：** 不支援 **ClientCoNtext** 成員。</span><span class="sxs-lookup"><span data-stu-id="b041f-175">**Windows 2000:** The **ClientContext** member is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="b041f-176">**旗標**</span><span class="sxs-lookup"><span data-stu-id="b041f-176">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="b041f-177">必須包含 **WNODE \_ 旗標 \_ 追蹤 \_ GUID** ，以指出此結構包含事件追蹤資訊。</span><span class="sxs-lookup"><span data-stu-id="b041f-177">Must contain **WNODE\_FLAG\_TRACED\_GUID** to indicate that the structure contains event tracing information.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b041f-178">備註</span><span class="sxs-lookup"><span data-stu-id="b041f-178">Remarks</span></span>

<span data-ttu-id="b041f-179">設定任何成員之前，請務必將此結構的記憶體初始化為零。</span><span class="sxs-lookup"><span data-stu-id="b041f-179">Be sure to initialize the memory for this structure to zero before setting any members.</span></span>

<span data-ttu-id="b041f-180">若要將 ETW 時間戳記轉換成 FILETIME，請使用下列程式：</span><span class="sxs-lookup"><span data-stu-id="b041f-180">To convert an ETW timestamp into a FILETIME, use the following procedure:</span></span>

<dl> 1. <span data-ttu-id="b041f-181">針對每個要處理的會話或記錄檔 (也就是針對每個事件追蹤記錄檔 \_ \_) ，請檢查 ProcessTraceMode 欄位，以判斷是否 \_ \_ 已設定進程追蹤模式 \_ 原始 \_ 時間戳記旗標。</span><span class="sxs-lookup"><span data-stu-id="b041f-181">For each session or log file being processed (i.e. for each EVENT\_TRACE\_LOGFILE), check the logFile.ProcessTraceMode field to determine whether the PROCESS\_TRACE\_MODE\_RAW\_TIMESTAMP flag is set.</span></span> <span data-ttu-id="b041f-182">依預設，不會設定此旗標。</span><span class="sxs-lookup"><span data-stu-id="b041f-182">By default, this flag is not set.</span></span> <span data-ttu-id="b041f-183">如果未設定此旗標，ETW 執行時間會在將事件記錄傳送至您的 EventRecordCallback 函式之前，自動將每個事件記錄的時間戳記轉換 \_ 成 FILETIME \_ ，因此不需要額外的處理。</span><span class="sxs-lookup"><span data-stu-id="b041f-183">If this flag is not set, the ETW runtime will automatically convert the timestamp of each EVENT\_RECORD into a FILETIME before sending the EVENT\_RECORD to your EventRecordCallback function, so no additional processing is needed.</span></span> <span data-ttu-id="b041f-184">只有在使用處理程式 \_ 追蹤 \_ 模式的 \_ 原始 \_ 時間戳記旗標設定來處理追蹤時，才應該使用下列步驟。</span><span class="sxs-lookup"><span data-stu-id="b041f-184">The following steps should only be used if the trace is being processed with the PROCESS\_TRACE\_MODE\_RAW\_TIMESTAMP flag set.</span></span>  
2. <span data-ttu-id="b041f-185">針對每個要處理的會話或記錄檔 (也就是針對每個事件追蹤記錄檔 \_ \_) ，請檢查 LogfileHeader ReservedFlags 欄位，以判斷記錄檔的時間戳記規模。</span><span class="sxs-lookup"><span data-stu-id="b041f-185">For each session or log file being processed (i.e. for each EVENT\_TRACE\_LOGFILE), check the logFile.LogfileHeader.ReservedFlags field to determine the time stamp scale for the log file.</span></span> <span data-ttu-id="b041f-186">根據 ReservedFlags 的值，遵循下列其中一個步驟來決定要在其餘步驟中用於 timeStampScale 的值：</span><span class="sxs-lookup"><span data-stu-id="b041f-186">Based on the value of ReservedFlags, follow one of these steps to determine the value to use for timeStampScale in the remaining steps:</span></span> <dl> <span data-ttu-id="b041f-187">a.</span><span class="sxs-lookup"><span data-stu-id="b041f-187">a.</span></span> <span data-ttu-id="b041f-188">If ReservedFlags = = 1 (QPC) ： DOUBLE timeStampScale = 10000000.0/logFile. LogfileHeader. PerfFreq;</span><span class="sxs-lookup"><span data-stu-id="b041f-188">If ReservedFlags == 1 (QPC): DOUBLE timeStampScale = 10000000.0 / logFile.LogfileHeader.PerfFreq.QuadPart;</span></span>  
<span data-ttu-id="b041f-189">b.</span><span class="sxs-lookup"><span data-stu-id="b041f-189">b.</span></span> <span data-ttu-id="b041f-190">If ReservedFlags = = 2 (系統時間) ： DOUBLE timeStampScale = 1.0;</span><span class="sxs-lookup"><span data-stu-id="b041f-190">If ReservedFlags == 2 (System time): DOUBLE timeStampScale = 1.0;</span></span>  
<span data-ttu-id="b041f-191">請注意，對於使用系統時間的事件，其餘步驟是不必要的，因為事件已經以 FILETIME 單位提供時間戳記。</span><span class="sxs-lookup"><span data-stu-id="b041f-191">Note that the remaining steps are unnecessary for events using system time, since the events already provide their time stamps in FILETIME units.</span></span> <span data-ttu-id="b041f-192">其餘步驟可以運作，但不是必要的，而且會引入較小的舍入錯誤。</span><span class="sxs-lookup"><span data-stu-id="b041f-192">The remaining steps will work but are unnecessary and will introduce a small rounding error.</span></span>  
<span data-ttu-id="b041f-193">c.</span><span class="sxs-lookup"><span data-stu-id="b041f-193">c.</span></span> <span data-ttu-id="b041f-194">如果 ReservedFlags = = 3 (CPU 週期計數器) ： DOUBLE timeStampScale = 10.0/logFile. LogfileHeader. CpuSpeedInMHz;</span><span class="sxs-lookup"><span data-stu-id="b041f-194">If ReservedFlags == 3 (CPU cycle counter): DOUBLE timeStampScale = 10.0 / logFile.LogfileHeader.CpuSpeedInMHz;</span></span>  
</dl> </dd> 3. On the FIRST call to your EventRecordCallback function for a particular log file, use data from the logFile (EVENT\_TRACE\_LOGFILE) and from the eventRecord (EVENT\_RECORD) to compute the timeStampBase that will be used for the remaining events in the log file: INT64 timeStampBase = logFile.LogfileHeader.StartTime.QuadPart - (INT64)(timeStampScale \* eventRecord.EventHeader.TimeStamp.QuadPart);  
4. For each eventRecord (EVENT\_RECORD), convert the event’s timestamp into FILETIME as follows, using the timeStampScale and timeStampBase values calculated in steps 2 and 3: INT64 timeStampInFileTime = timeStampBase + (INT64)(timeStampScale \* eventRecord.EventHeader.TimeStamp.QuadPart);  
</dl>

## <a name="requirements"></a><span data-ttu-id="b041f-195">規格需求</span><span class="sxs-lookup"><span data-stu-id="b041f-195">Requirements</span></span>



| <span data-ttu-id="b041f-196">需求</span><span class="sxs-lookup"><span data-stu-id="b041f-196">Requirement</span></span> | <span data-ttu-id="b041f-197">值</span><span class="sxs-lookup"><span data-stu-id="b041f-197">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b041f-198">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b041f-198">Minimum supported client</span></span><br/> | <span data-ttu-id="b041f-199">Windows 2000 專業版傳統型 \[ 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b041f-199">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                   |
| <span data-ttu-id="b041f-200">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b041f-200">Minimum supported server</span></span><br/> | <span data-ttu-id="b041f-201">Windows 2000 Server \[ desktop 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b041f-201">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                         |
| <span data-ttu-id="b041f-202">標頭</span><span class="sxs-lookup"><span data-stu-id="b041f-202">Header</span></span><br/>                   | <dl> <span data-ttu-id="b041f-203"><dt>Wmistr。h</dt></span><span class="sxs-lookup"><span data-stu-id="b041f-203"><dt>Wmistr.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b041f-204">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b041f-204">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b041f-205">*ControlCallback*</span><span class="sxs-lookup"><span data-stu-id="b041f-205">*ControlCallback*</span></span>](/windows/win32/api/evntrace/nc-evntrace-wmidprequest)
</dt> <dt>

[<span data-ttu-id="b041f-206">**事件 \_ 追蹤 \_ 屬性**</span><span class="sxs-lookup"><span data-stu-id="b041f-206">**EVENT\_TRACE\_PROPERTIES**</span></span>](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)
</dt> <dt>

[<span data-ttu-id="b041f-207">**GetTraceLoggerHandle**</span><span class="sxs-lookup"><span data-stu-id="b041f-207">**GetTraceLoggerHandle**</span></span>](/windows/win32/api/evntrace/nf-evntrace-gettraceloggerhandle)
</dt> <dt>

[<span data-ttu-id="b041f-208">**大型 \_ 整數**</span><span class="sxs-lookup"><span data-stu-id="b041f-208">**LARGE\_INTEGER**</span></span>](/windows/win32/api/winnt/ns-winnt-large_integer-r1)
</dt> </dl>

 

 
