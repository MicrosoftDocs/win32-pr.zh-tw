---
description: 記錄檔標頭事件的事件種類類別。 此類別包含事件追蹤會話的相關資訊。
ms.assetid: 3d0c4044-da06-4850-95c4-99b4ea28fcd9
title: EventTrace_Header 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EventTrace_Header
- EventTrace_Header.BufferSize
- EventTrace_Header.Version
- EventTrace_Header.ProviderVersion
- EventTrace_Header.NumberOfProcessors
- EventTrace_Header.EndTime
- EventTrace_Header.TimerResolution
- EventTrace_Header.MaxFileSize
- EventTrace_Header.LogFileMode
- EventTrace_Header.BuffersWritten
- EventTrace_Header.StartBuffers
- EventTrace_Header.PointerSize
- EventTrace_Header.EventsLost
- EventTrace_Header.CPUSpeed
- EventTrace_Header.LoggerName
- EventTrace_Header.LogFileName
- EventTrace_Header.TimeZoneInformation
- EventTrace_Header.BootTime
- EventTrace_Header.PerfFreq
- EventTrace_Header.StartTime
- EventTrace_Header.ReservedFlags
- EventTrace_Header.BuffersLost
api_type:
- NA
api_location: ''
ms.openlocfilehash: dea803849d6aa15c2a3a14deb850d85ade569116
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511904"
---
# <a name="eventtrace_header-class"></a><span data-ttu-id="7fa54-104">EventTrace \_ 標頭類別</span><span class="sxs-lookup"><span data-stu-id="7fa54-104">EventTrace\_Header class</span></span>

<span data-ttu-id="7fa54-105">記錄檔標頭事件的事件種類類別。</span><span class="sxs-lookup"><span data-stu-id="7fa54-105">The event type class for the log file header event.</span></span> <span data-ttu-id="7fa54-106">此類別包含事件追蹤會話的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="7fa54-106">This class contains information about the event tracing session.</span></span>

<span data-ttu-id="7fa54-107">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="7fa54-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="7fa54-108">語法</span><span class="sxs-lookup"><span data-stu-id="7fa54-108">Syntax</span></span>

``` syntax
[EventType(0)]
class EventTrace_Header : EventTraceEvent
{
  uint32 BufferSize;
  uint32 Version;
  uint32 ProviderVersion;
  uint32 NumberOfProcessors;
  uint64 EndTime;
  uint32 TimerResolution;
  uint32 MaxFileSize;
  uint32 LogFileMode;
  uint32 BuffersWritten;
  uint32 StartBuffers;
  uint32 PointerSize;
  uint32 EventsLost;
  uint32 CPUSpeed;
  uint32 LoggerName;
  uint32 LogFileName;
  uint8  TimeZoneInformation[];
  uint64 BootTime;
  uint64 PerfFreq;
  uint64 StartTime;
  uint32 ReservedFlags;
  uint32 BuffersLost;
};
```

## <a name="members"></a><span data-ttu-id="7fa54-109">成員</span><span class="sxs-lookup"><span data-stu-id="7fa54-109">Members</span></span>

<span data-ttu-id="7fa54-110">**EventTrace \_ 標頭** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="7fa54-110">The **EventTrace\_Header** class has these types of members:</span></span>

-   [<span data-ttu-id="7fa54-111">屬性</span><span class="sxs-lookup"><span data-stu-id="7fa54-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7fa54-112">屬性</span><span class="sxs-lookup"><span data-stu-id="7fa54-112">Properties</span></span>

<span data-ttu-id="7fa54-113">**EventTrace \_ 標頭** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="7fa54-113">The **EventTrace\_Header** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7fa54-114">**BootTime**</span><span class="sxs-lookup"><span data-stu-id="7fa54-114">**BootTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fa54-115">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="7fa54-115">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="7fa54-116">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7fa54-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7fa54-117">限定詞： **WmiDataId** (17) </span><span class="sxs-lookup"><span data-stu-id="7fa54-117">Qualifiers: **WmiDataId** (17)</span></span>
</dt> </dl>

<span data-ttu-id="7fa54-118">系統啟動的時間，從1601年1月1日午夜起算的 100-毫微秒間隔。</span><span class="sxs-lookup"><span data-stu-id="7fa54-118">Time at which the system was started, in 100-nanosecond intervals since midnight, January 1, 1601.</span></span>

</dd> <dt>

<span data-ttu-id="7fa54-119">**BufferSize**</span><span class="sxs-lookup"><span data-stu-id="7fa54-119">**BufferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fa54-120">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="7fa54-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7fa54-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7fa54-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7fa54-122">限定詞： **WmiDataId** (1) </span><span class="sxs-lookup"><span data-stu-id="7fa54-122">Qualifiers: **WmiDataId** (1)</span></span>
</dt> </dl>

<span data-ttu-id="7fa54-123">事件追蹤會話的緩衝區大小（以 kb 為單位）。</span><span class="sxs-lookup"><span data-stu-id="7fa54-123">Size of the event tracing session's buffers, in kilobytes.</span></span>

</dd> <dt>

<span data-ttu-id="7fa54-124">**BuffersLost**</span><span class="sxs-lookup"><span data-stu-id="7fa54-124">**BuffersLost**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fa54-125">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="7fa54-125">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7fa54-126">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7fa54-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7fa54-127">限定詞： **WmiDataId** (21) </span><span class="sxs-lookup"><span data-stu-id="7fa54-127">Qualifiers: **WmiDataId** (21)</span></span>
</dt> </dl>

<span data-ttu-id="7fa54-128">遺失的緩衝區總數。</span><span class="sxs-lookup"><span data-stu-id="7fa54-128">Total number of buffers lost.</span></span>

</dd> <dt>

<span data-ttu-id="7fa54-129">**BuffersWritten**</span><span class="sxs-lookup"><span data-stu-id="7fa54-129">**BuffersWritten**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fa54-130">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="7fa54-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7fa54-131">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7fa54-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7fa54-132">限定詞： **WmiDataId** (9) </span><span class="sxs-lookup"><span data-stu-id="7fa54-132">Qualifiers: **WmiDataId** (9)</span></span>
</dt> </dl>

<span data-ttu-id="7fa54-133">事件追蹤會話所寫入的緩衝區總數。</span><span class="sxs-lookup"><span data-stu-id="7fa54-133">Total number of buffers written by the event tracing session.</span></span>

</dd> <dt>

<span data-ttu-id="7fa54-134">**CPUSpeed**</span><span class="sxs-lookup"><span data-stu-id="7fa54-134">**CPUSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fa54-135">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="7fa54-135">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7fa54-136">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7fa54-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7fa54-137">限定詞： **WmiDataId** (13) </span><span class="sxs-lookup"><span data-stu-id="7fa54-137">Qualifiers: **WmiDataId** (13)</span></span>
</dt> </dl>

<span data-ttu-id="7fa54-138">CPU 速度（以 mhz 為單位）。</span><span class="sxs-lookup"><span data-stu-id="7fa54-138">CPU speed, in megahertz.</span></span>

<span data-ttu-id="7fa54-139">**Windows 2000：** 不支援。</span><span class="sxs-lookup"><span data-stu-id="7fa54-139">**Windows 2000:** Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="7fa54-140">**EndTime**</span><span class="sxs-lookup"><span data-stu-id="7fa54-140">**EndTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fa54-141">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="7fa54-141">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="7fa54-142">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7fa54-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7fa54-143">限定詞： **WmiDataId** (5) </span><span class="sxs-lookup"><span data-stu-id="7fa54-143">Qualifiers: **WmiDataId** (5)</span></span>
</dt> </dl>

<span data-ttu-id="7fa54-144">事件追蹤會話停止的時間，從1601年1月1日午夜起算的 100-毫微秒間隔時間。</span><span class="sxs-lookup"><span data-stu-id="7fa54-144">Time at which the event tracing session stopped, in 100-nanosecond intervals since midnight, January 1, 1601.</span></span> <span data-ttu-id="7fa54-145">如果您正在使用事件，或從提供仍在記錄事件的記錄檔中，則此值可能是0。</span><span class="sxs-lookup"><span data-stu-id="7fa54-145">This value may be 0 if you are consuming events in real time or from a log file to which the provide is still logging events.</span></span>

</dd> <dt>

<span data-ttu-id="7fa54-146">**EventsLost**</span><span class="sxs-lookup"><span data-stu-id="7fa54-146">**EventsLost**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fa54-147">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="7fa54-147">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7fa54-148">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7fa54-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7fa54-149">限定詞： **WmiDataId** (12) </span><span class="sxs-lookup"><span data-stu-id="7fa54-149">Qualifiers: **WmiDataId** (12)</span></span>
</dt> </dl>

<span data-ttu-id="7fa54-150">事件追蹤會話期間遺失的事件數。</span><span class="sxs-lookup"><span data-stu-id="7fa54-150">Number of events lost during the event tracing session.</span></span>

</dd> <dt>

<span data-ttu-id="7fa54-151">**LogFileMode**</span><span class="sxs-lookup"><span data-stu-id="7fa54-151">**LogFileMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fa54-152">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="7fa54-152">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7fa54-153">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7fa54-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7fa54-154">限定詞： **WmiDataId** (8) ， **格式 ( "x" )**</span><span class="sxs-lookup"><span data-stu-id="7fa54-154">Qualifiers: **WmiDataId** (8), **Format("x")**</span></span>
</dt> </dl>

<span data-ttu-id="7fa54-155">事件追蹤會話目前的記錄模式。</span><span class="sxs-lookup"><span data-stu-id="7fa54-155">Current logging mode for the event tracing session.</span></span> <span data-ttu-id="7fa54-156">如需值的清單，請參閱記錄模式常數。</span><span class="sxs-lookup"><span data-stu-id="7fa54-156">For a list of values, see Logging Mode Constants.</span></span>

</dd> <dt>

<span data-ttu-id="7fa54-157">**LogFileName**</span><span class="sxs-lookup"><span data-stu-id="7fa54-157">**LogFileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fa54-158">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="7fa54-158">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7fa54-159">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7fa54-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7fa54-160">限定詞： **WmiDataId** (15) ， **指標**</span><span class="sxs-lookup"><span data-stu-id="7fa54-160">Qualifiers: **WmiDataId** (15), **Pointer**</span></span>
</dt> </dl>

<span data-ttu-id="7fa54-161">包含事件的事件追蹤記錄檔名稱。</span><span class="sxs-lookup"><span data-stu-id="7fa54-161">Name of the event tracing log file that contains the events.</span></span>

</dd> <dt>

<span data-ttu-id="7fa54-162">**LoggerName**</span><span class="sxs-lookup"><span data-stu-id="7fa54-162">**LoggerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fa54-163">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="7fa54-163">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7fa54-164">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7fa54-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7fa54-165">限定詞： **WmiDataId** (14) ， **指標**</span><span class="sxs-lookup"><span data-stu-id="7fa54-165">Qualifiers: **WmiDataId** (14), **Pointer**</span></span>
</dt> </dl>

<span data-ttu-id="7fa54-166">事件追蹤會話的名稱。</span><span class="sxs-lookup"><span data-stu-id="7fa54-166">Name of the event tracing session.</span></span>

</dd> <dt>

<span data-ttu-id="7fa54-167">**MaxFileSize**</span><span class="sxs-lookup"><span data-stu-id="7fa54-167">**MaxFileSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fa54-168">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="7fa54-168">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7fa54-169">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7fa54-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7fa54-170">限定詞： **WmiDataId** (7) </span><span class="sxs-lookup"><span data-stu-id="7fa54-170">Qualifiers: **WmiDataId** (7)</span></span>
</dt> </dl>

<span data-ttu-id="7fa54-171">記錄檔的大小上限（以 mb 為單位）。</span><span class="sxs-lookup"><span data-stu-id="7fa54-171">Maximum size of the log file, in megabytes.</span></span>

</dd> <dt>

<span data-ttu-id="7fa54-172">**NumberOfProcessors**</span><span class="sxs-lookup"><span data-stu-id="7fa54-172">**NumberOfProcessors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fa54-173">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="7fa54-173">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7fa54-174">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7fa54-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7fa54-175">限定詞： **WmiDataId** (4) </span><span class="sxs-lookup"><span data-stu-id="7fa54-175">Qualifiers: **WmiDataId** (4)</span></span>
</dt> </dl>

<span data-ttu-id="7fa54-176">系統上的處理器數目。</span><span class="sxs-lookup"><span data-stu-id="7fa54-176">Number of processors on the system.</span></span>

</dd> <dt>

<span data-ttu-id="7fa54-177">**PerfFreq**</span><span class="sxs-lookup"><span data-stu-id="7fa54-177">**PerfFreq**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fa54-178">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="7fa54-178">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="7fa54-179">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7fa54-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7fa54-180">限定詞： **WmiDataId** (18) </span><span class="sxs-lookup"><span data-stu-id="7fa54-180">Qualifiers: **WmiDataId** (18)</span></span>
</dt> </dl>

<span data-ttu-id="7fa54-181">高解析度效能計數器的頻率（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="7fa54-181">Frequency of the high-resolution performance counter, if one exists.</span></span>

</dd> <dt>

<span data-ttu-id="7fa54-182">**PointerSize**</span><span class="sxs-lookup"><span data-stu-id="7fa54-182">**PointerSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fa54-183">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="7fa54-183">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7fa54-184">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7fa54-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7fa54-185">限定詞： **WmiDataId** (11) </span><span class="sxs-lookup"><span data-stu-id="7fa54-185">Qualifiers: **WmiDataId** (11)</span></span>
</dt> </dl>

<span data-ttu-id="7fa54-186">指標資料類型的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="7fa54-186">Size of a pointer data type, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="7fa54-187">**ProviderVersion**</span><span class="sxs-lookup"><span data-stu-id="7fa54-187">**ProviderVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fa54-188">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="7fa54-188">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7fa54-189">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7fa54-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7fa54-190">限定詞： **WmiDataId** (3) </span><span class="sxs-lookup"><span data-stu-id="7fa54-190">Qualifiers: **WmiDataId** (3)</span></span>
</dt> </dl>

<span data-ttu-id="7fa54-191">作業系統的組建編號。</span><span class="sxs-lookup"><span data-stu-id="7fa54-191">Build number of the operating system.</span></span>

</dd> <dt>

<span data-ttu-id="7fa54-192">**ReservedFlags**</span><span class="sxs-lookup"><span data-stu-id="7fa54-192">**ReservedFlags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fa54-193">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="7fa54-193">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7fa54-194">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7fa54-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7fa54-195">限定詞： **WmiDataId** (20) </span><span class="sxs-lookup"><span data-stu-id="7fa54-195">Qualifiers: **WmiDataId** (20)</span></span>
</dt> </dl>

<span data-ttu-id="7fa54-196">保留的。</span><span class="sxs-lookup"><span data-stu-id="7fa54-196">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="7fa54-197">**StartBuffers**</span><span class="sxs-lookup"><span data-stu-id="7fa54-197">**StartBuffers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fa54-198">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="7fa54-198">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7fa54-199">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7fa54-199">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7fa54-200">限定詞： **WmiDataId** (10) </span><span class="sxs-lookup"><span data-stu-id="7fa54-200">Qualifiers: **WmiDataId** (10)</span></span>
</dt> </dl>

<span data-ttu-id="7fa54-201">保留的。</span><span class="sxs-lookup"><span data-stu-id="7fa54-201">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="7fa54-202">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="7fa54-202">**StartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fa54-203">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="7fa54-203">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="7fa54-204">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7fa54-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7fa54-205">限定詞： **WmiDataId** (19) </span><span class="sxs-lookup"><span data-stu-id="7fa54-205">Qualifiers: **WmiDataId** (19)</span></span>
</dt> </dl>

<span data-ttu-id="7fa54-206">事件追蹤會話開始的時間，從1601年1月1日午夜起算的 100-毫微秒間隔。</span><span class="sxs-lookup"><span data-stu-id="7fa54-206">Time at which the event tracing session started, in 100-nanosecond intervals since midnight, January 1, 1601.</span></span>

</dd> <dt>

<span data-ttu-id="7fa54-207">**TimerResolution**</span><span class="sxs-lookup"><span data-stu-id="7fa54-207">**TimerResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fa54-208">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="7fa54-208">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7fa54-209">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7fa54-209">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7fa54-210">限定詞： **WmiDataId** (6) </span><span class="sxs-lookup"><span data-stu-id="7fa54-210">Qualifiers: **WmiDataId** (6)</span></span>
</dt> </dl>

<span data-ttu-id="7fa54-211">硬體計時器的解析度（以100毫微秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="7fa54-211">Resolution of the hardware timer, in units of 100 nanoseconds.</span></span>

</dd> <dt>

<span data-ttu-id="7fa54-212">**TimeZoneInformation**</span><span class="sxs-lookup"><span data-stu-id="7fa54-212">**TimeZoneInformation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fa54-213">資料類型： **uint8** 陣列</span><span class="sxs-lookup"><span data-stu-id="7fa54-213">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="7fa54-214">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7fa54-214">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7fa54-215">限定詞： **WmiDataId** (16) 、 **延伸 ( "NoPrint" )**、 **最大** (176) </span><span class="sxs-lookup"><span data-stu-id="7fa54-215">Qualifiers: **WmiDataId** (16), **Extension("NoPrint")**, **Max** (176)</span></span>
</dt> </dl>

<span data-ttu-id="7fa54-216">[**時區 \_ \_ 資訊**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)結構，其中包含 **BootTime**、 **EndTime** 和 **StartTime** 成員的時區。</span><span class="sxs-lookup"><span data-stu-id="7fa54-216">A [**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) structure that contains the time zone for the **BootTime**, **EndTime** and **StartTime** members.</span></span>

</dd> <dt>

<span data-ttu-id="7fa54-217">**版本**</span><span class="sxs-lookup"><span data-stu-id="7fa54-217">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fa54-218">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="7fa54-218">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7fa54-219">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7fa54-219">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7fa54-220">限定詞： **WmiDataId** (2) </span><span class="sxs-lookup"><span data-stu-id="7fa54-220">Qualifiers: **WmiDataId** (2)</span></span>
</dt> </dl>

<span data-ttu-id="7fa54-221">作業系統的版本號碼。</span><span class="sxs-lookup"><span data-stu-id="7fa54-221">Version number of the operating system.</span></span> <span data-ttu-id="7fa54-222">從低序位位元組開始，前兩個位元組包含主要版本，接下來的兩個位元組包含次要版本，接下來的兩個位元組包含 service pack 的主要版本，而最後兩個位元組包含 service pack 次要版本。</span><span class="sxs-lookup"><span data-stu-id="7fa54-222">Starting with the low-order bytes, the first two bytes contain major version, the next two bytes contain minor version, the next two bytes contain service pack major version, and the last two bytes contain service pack minor version.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7fa54-223">備註</span><span class="sxs-lookup"><span data-stu-id="7fa54-223">Remarks</span></span>

<span data-ttu-id="7fa54-224">一般來說，您會想要儲存下列屬性的值，以便稍後在處理記錄檔中的事件時使用。</span><span class="sxs-lookup"><span data-stu-id="7fa54-224">Typically, you want to save the values for the following properties for use later when processing events from the log file.</span></span>

-   <span data-ttu-id="7fa54-225">**TimerResolution**-與 [**事件 \_ 追蹤 \_ 標頭**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header)結構的 **KernelTime** 和 **UserTime** 成員一起使用，以判斷一組指示的 CPU 成本。</span><span class="sxs-lookup"><span data-stu-id="7fa54-225">**TimerResolution**—use with the **KernelTime** and **UserTime** members of the [**EVENT\_TRACE\_HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) structure to determine the CPU cost for a set of instructions.</span></span> <span data-ttu-id="7fa54-226">如需詳細資訊，請參閱 [**事件 \_ 追蹤 \_ 標頭**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header)的備註一節。</span><span class="sxs-lookup"><span data-stu-id="7fa54-226">For details, see the Remarks section of [**EVENT\_TRACE\_HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header).</span></span>
-   <span data-ttu-id="7fa54-227">**PointerSize**：對於包含 **指標** 辨識符號的屬性，請使用此值來判斷指標的大小。</span><span class="sxs-lookup"><span data-stu-id="7fa54-227">**PointerSize**—for properties that contain the **Pointer** qualifier, use this value to determine the size of the pointer.</span></span> <span data-ttu-id="7fa54-228">請注意，這個值可能不正確。</span><span class="sxs-lookup"><span data-stu-id="7fa54-228">Note that this value may not be accurate.</span></span> <span data-ttu-id="7fa54-229">例如，在64位的電腦上，32位應用程式將會記錄4位元組指標;不過，會話會將 **PointerSize** 設定為8。</span><span class="sxs-lookup"><span data-stu-id="7fa54-229">For example, on a 64-bit computer, a 32-bit application will log 4-byte pointers; however, the session will set **PointerSize** to 8.</span></span>
-   <span data-ttu-id="7fa54-230">**LogFileMode**：用來判斷此會話是否為私用記錄器會話。</span><span class="sxs-lookup"><span data-stu-id="7fa54-230">**LogFileMode**—use to determine if this session is a private logger session.</span></span> <span data-ttu-id="7fa54-231">有些屬性不包含私用記錄器會話的資料。</span><span class="sxs-lookup"><span data-stu-id="7fa54-231">There are some properties that do not contain data for private logger sessions.</span></span> <span data-ttu-id="7fa54-232">例如，[**事件 \_ 追蹤 \_ 標頭**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header)結構的 **KernelTime** 和 **UserTime** 成員。</span><span class="sxs-lookup"><span data-stu-id="7fa54-232">For example, the **KernelTime** and **UserTime** members of the [**EVENT\_TRACE\_HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="7fa54-233">規格需求</span><span class="sxs-lookup"><span data-stu-id="7fa54-233">Requirements</span></span>



| <span data-ttu-id="7fa54-234">需求</span><span class="sxs-lookup"><span data-stu-id="7fa54-234">Requirement</span></span> | <span data-ttu-id="7fa54-235">值</span><span class="sxs-lookup"><span data-stu-id="7fa54-235">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="7fa54-236">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7fa54-236">Minimum supported client</span></span><br/> | <span data-ttu-id="7fa54-237">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7fa54-237">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="7fa54-238">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7fa54-238">Minimum supported server</span></span><br/> | <span data-ttu-id="7fa54-239">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7fa54-239">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="7fa54-240">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7fa54-240">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7fa54-241">**EventTraceEvent**</span><span class="sxs-lookup"><span data-stu-id="7fa54-241">**EventTraceEvent**</span></span>](eventtraceevent.md)
</dt> <dt>

[<span data-ttu-id="7fa54-242">**TRACE \_ LOGFILE \_ 標頭**</span><span class="sxs-lookup"><span data-stu-id="7fa54-242">**TRACE\_LOGFILE\_HEADER**</span></span>](/windows/win32/api/evntrace/ns-evntrace-trace_logfile_header)
</dt> </dl>

 

 
