---
description: 全域記錄器事件追蹤會話會記錄在作業系統開機程式初期發生的事件。
ms.assetid: 1462bbef-ef32-4053-9930-5b4a0ab46b47
title: 設定和啟動全域記錄器會話
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8692e1f7321acc163e48cda7e3323f3d24adc1c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973433"
---
# <a name="configuring-and-starting-the-global-logger-session"></a><span data-ttu-id="f339f-103">設定和啟動全域記錄器會話</span><span class="sxs-lookup"><span data-stu-id="f339f-103">Configuring and Starting the Global Logger Session</span></span>

<span data-ttu-id="f339f-104">全域記錄器事件追蹤會話會記錄在作業系統開機程式初期發生的事件。</span><span class="sxs-lookup"><span data-stu-id="f339f-104">The Global Logger event tracing session records events that occur early in the operating system boot process.</span></span> <span data-ttu-id="f339f-105">在使用者登入之前，應用程式和設備磁碟機可以使用全域記錄器會話來捕捉追蹤。</span><span class="sxs-lookup"><span data-stu-id="f339f-105">Applications and device drivers can use the Global Logger session to capture traces before the user logs in.</span></span> <span data-ttu-id="f339f-106">請注意，某些設備磁碟機（例如磁片設備磁碟機）在全域記錄器會話開始時不會載入。</span><span class="sxs-lookup"><span data-stu-id="f339f-106">Note that some device drivers, such as disk device drivers, are not loaded at the time the Global Logger session begins.</span></span>

> [!Note]  
> <span data-ttu-id="f339f-107">如果您要在 Windows Vista 上建立全域記錄器會話，您應該考慮改為建立自動記錄器 [會話](configuring-and-starting-an-autologger-session.md) 。</span><span class="sxs-lookup"><span data-stu-id="f339f-107">If you are creating a Global Logger session on Windows Vista, you should consider creating an [AutoLogger session](configuring-and-starting-an-autologger-session.md) instead.</span></span>

 

<span data-ttu-id="f339f-108">您可以使用登錄來設定全域記錄器會話。</span><span class="sxs-lookup"><span data-stu-id="f339f-108">You use the registry to configure the Global Logger session.</span></span> <span data-ttu-id="f339f-109">如果下列登錄機碼尚未存在，請將其新增至 **GlobalLogger** 機碼：</span><span class="sxs-lookup"><span data-stu-id="f339f-109">Add the **GlobalLogger** key to the following registry key, if it is not already present:</span></span>

```
HKEY_LOCAL_MACHINE
   \SYSTEM
      \CurrentControlSet
         \Control
            \WMI
```

<span data-ttu-id="f339f-110">下表描述您可以為 **GlobalLogger** 索引鍵定義的值。</span><span class="sxs-lookup"><span data-stu-id="f339f-110">The following table describes the values that you can define for the **GlobalLogger** key.</span></span> <span data-ttu-id="f339f-111">您必須具有系統管理員許可權，才能指定這些登錄值。</span><span class="sxs-lookup"><span data-stu-id="f339f-111">You must have administrator privileges to specify these registry values.</span></span> <span data-ttu-id="f339f-112">登錄值會影響將事件記錄到全域記錄器會話的所有提供者。</span><span class="sxs-lookup"><span data-stu-id="f339f-112">The registry values affect all providers that log events to the Global Logger session.</span></span> <span data-ttu-id="f339f-113">**開始** 值是啟動全域記錄器會話所需的唯一值;如果登錄中沒有值，所有其他值都有預設的設定。</span><span class="sxs-lookup"><span data-stu-id="f339f-113">The **Start** value is the only value required to start the Global Logger session; all other values have default settings that are used if the value is not present in the registry.</span></span> <span data-ttu-id="f339f-114">一般而言，您應該使用預設值。</span><span class="sxs-lookup"><span data-stu-id="f339f-114">Typically, you should use the default values.</span></span> <span data-ttu-id="f339f-115">如果您指定 ETW 無法支援的值，ETW 將會覆寫此值。</span><span class="sxs-lookup"><span data-stu-id="f339f-115">If you specify a value that ETW cannot support, ETW will override the value.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f339f-116">值</span><span class="sxs-lookup"><span data-stu-id="f339f-116">Value</span></span></th>
<th><span data-ttu-id="f339f-117">類型</span><span class="sxs-lookup"><span data-stu-id="f339f-117">Type</span></span></th>
<th><span data-ttu-id="f339f-118">Description</span><span class="sxs-lookup"><span data-stu-id="f339f-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f339f-119"><strong>開始</strong></span><span class="sxs-lookup"><span data-stu-id="f339f-119"><strong>Start</strong></span></span></td>
<td><span data-ttu-id="f339f-120"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="f339f-120"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="f339f-121">在) 上將此值設定為 1 (，以在下次系統啟動時啟動全域記錄器會話。</span><span class="sxs-lookup"><span data-stu-id="f339f-121">Set this value to 1 (on) to start the Global Logger session the next time the system starts.</span></span> <span data-ttu-id="f339f-122">若要停止會話開始，請將此值設定為 0 (off) 。</span><span class="sxs-lookup"><span data-stu-id="f339f-122">To stop the session from starting, set this value to 0 (off).</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f339f-123"><strong>BufferSize</strong></span><span class="sxs-lookup"><span data-stu-id="f339f-123"><strong>BufferSize</strong></span></span></td>
<td><span data-ttu-id="f339f-124"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="f339f-124"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="f339f-125">每個緩衝區的大小（以 kb 為單位）。</span><span class="sxs-lookup"><span data-stu-id="f339f-125">The size of each buffer, in kilobytes.</span></span> <span data-ttu-id="f339f-126">此值應小於 1 mb。</span><span class="sxs-lookup"><span data-stu-id="f339f-126">This value should be less than one megabyte.</span></span> <span data-ttu-id="f339f-127">ETW 使用實體記憶體的大小來計算這個值。</span><span class="sxs-lookup"><span data-stu-id="f339f-127">ETW uses the size of physical memory to calculate this value.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f339f-128"><strong>ClockType</strong></span><span class="sxs-lookup"><span data-stu-id="f339f-128"><strong>ClockType</strong></span></span></td>
<td><span data-ttu-id="f339f-129"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="f339f-129"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="f339f-130">記錄每個事件的時間戳記時要使用的計時器。</span><span class="sxs-lookup"><span data-stu-id="f339f-130">The timer to use when logging the time stamp for each event.</span></span>
<ul>
<li><span data-ttu-id="f339f-131">1 = 效能計數器值 (高解析度) </span><span class="sxs-lookup"><span data-stu-id="f339f-131">1 = Performance counter value (high resolution)</span></span></li>
<li><span data-ttu-id="f339f-132">2 = 系統計時器</span><span class="sxs-lookup"><span data-stu-id="f339f-132">2 = System timer</span></span></li>
<li><span data-ttu-id="f339f-133">3 = CPU 週期計數器</span><span class="sxs-lookup"><span data-stu-id="f339f-133">3 = CPU cycle counter</span></span></li>
</ul>
<span data-ttu-id="f339f-134">如需每種頻率類型的描述，請參閱<a href="wnode-header.md"><strong>WNODE_HEADER</strong></a>的<strong>ClientCoNtext</strong>成員。</span><span class="sxs-lookup"><span data-stu-id="f339f-134">For a description of each clock type, see the <strong>ClientContext</strong> member of <a href="wnode-header.md"><strong>WNODE_HEADER</strong></a>.</span></span><br/> <span data-ttu-id="f339f-135">在 Windows Vista 和更新版本上，預設值為 1 (效能計數器值) 。</span><span class="sxs-lookup"><span data-stu-id="f339f-135">The default value is 1 (performance counter value) on Windows Vista and later.</span></span> <span data-ttu-id="f339f-136">在 Windows Vista 之前，預設值為 2 (系統計時器) 。</span><span class="sxs-lookup"><span data-stu-id="f339f-136">Prior to Windows Vista, the default value is 2 (system timer).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f339f-137"><strong>EnableKernelFlags</strong></span><span class="sxs-lookup"><span data-stu-id="f339f-137"><strong>EnableKernelFlags</strong></span></span></td>
<td><span data-ttu-id="f339f-138"><strong>REG_BINARY</strong></span><span class="sxs-lookup"><span data-stu-id="f339f-138"><strong>REG_BINARY</strong></span></span></td>
<td><span data-ttu-id="f339f-139">使用此值可啟用一或多個核心提供者。</span><span class="sxs-lookup"><span data-stu-id="f339f-139">Use this value to enable one or more kernel providers.</span></span> <span data-ttu-id="f339f-140">如果您啟用核心提供者，全域記錄器會話就會在啟動時將本身重新命名為 NT Kernel 記錄器。</span><span class="sxs-lookup"><span data-stu-id="f339f-140">If you enable kernel providers, the Global Logger session will rename itself to NT Kernel Logger when it starts.</span></span> <span data-ttu-id="f339f-141">如需可能的值，請參閱<a href="/windows/win32/api/evntrace/ns-evntrace-event_trace_properties"><strong>EVENT_TRACE_PROPERTIES</strong></a>的<strong>EnableFlags</strong>成員。</span><span class="sxs-lookup"><span data-stu-id="f339f-141">For possible values, see the <strong>EnableFlags</strong> member of <a href="/windows/win32/api/evntrace/ns-evntrace-event_trace_properties"><strong>EVENT_TRACE_PROPERTIES</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f339f-142"><strong>FileCounter</strong></span><span class="sxs-lookup"><span data-stu-id="f339f-142"><strong>FileCounter</strong></span></span></td>
<td><span data-ttu-id="f339f-143"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="f339f-143"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="f339f-144">全域記錄器會話所產生的事件追蹤記錄檔數目。</span><span class="sxs-lookup"><span data-stu-id="f339f-144">The number of event trace log files generated by Global Logger sessions.</span></span> <span data-ttu-id="f339f-145">系統會遞增此值，直到達到 <strong>FileMax</strong>的值為止。</span><span class="sxs-lookup"><span data-stu-id="f339f-145">The system increments this value until it reaches the value of <strong>FileMax</strong>.</span></span> <span data-ttu-id="f339f-146">然後，它會將值重設為0。</span><span class="sxs-lookup"><span data-stu-id="f339f-146">Then, it resets the value to 0.</span></span> <span data-ttu-id="f339f-147">此計數器可防止系統覆寫全域記錄器追蹤記錄檔。</span><span class="sxs-lookup"><span data-stu-id="f339f-147">This counter prevents the system from overwriting a Global Logger trace log file.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f339f-148"><strong>FileMax</strong></span><span class="sxs-lookup"><span data-stu-id="f339f-148"><strong>FileMax</strong></span></span></td>
<td><span data-ttu-id="f339f-149"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="f339f-149"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="f339f-150">系統上允許的事件追蹤記錄檔數目上限。</span><span class="sxs-lookup"><span data-stu-id="f339f-150">The maximum number of event trace log files permitted on the system.</span></span> <span data-ttu-id="f339f-151">當追蹤記錄檔的數目達到指定的最大值時，系統就會開始覆寫記錄，從最舊的開始。</span><span class="sxs-lookup"><span data-stu-id="f339f-151">When the number of trace logs reaches the specified maximum, the system begins to overwrite the logs, beginning with the oldest.</span></span> <br/> <span data-ttu-id="f339f-152">如果 <strong>檔案名</strong> 中指定的記錄檔存在，ETW 會將 <strong>FileCounter</strong> 值附加至檔案名。</span><span class="sxs-lookup"><span data-stu-id="f339f-152">If the log file specified in <strong>FileName</strong> exists, ETW appends the <strong>FileCounter</strong> value to the file name.</span></span> <span data-ttu-id="f339f-153">例如，如果使用預設記錄檔名稱，則表單為%SystemRoot%\System32\LogFiles\WMI\GlobalLogger.etl.NNNN。</span><span class="sxs-lookup"><span data-stu-id="f339f-153">For example, if the default log file name is used, the form is %SystemRoot%\System32\LogFiles\WMI\GlobalLogger.etl.NNNN.</span></span> <br/> <span data-ttu-id="f339f-154">預設值為0，表示沒有最大值。</span><span class="sxs-lookup"><span data-stu-id="f339f-154">The default value is 0, meaning that there is no maximum.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f339f-155"><strong>FileName</strong></span><span class="sxs-lookup"><span data-stu-id="f339f-155"><strong>FileName</strong></span></span></td>
<td><span data-ttu-id="f339f-156"><strong>REG_SZ</strong></span><span class="sxs-lookup"><span data-stu-id="f339f-156"><strong>REG_SZ</strong></span></span></td>
<td><span data-ttu-id="f339f-157">記錄檔的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="f339f-157">Fully qualified path of the log file.</span></span> <span data-ttu-id="f339f-158">這個檔案的路徑必須存在。</span><span class="sxs-lookup"><span data-stu-id="f339f-158">The path to this file must exist.</span></span> <span data-ttu-id="f339f-159">記錄檔是連續的記錄檔。</span><span class="sxs-lookup"><span data-stu-id="f339f-159">The log file is a sequential log file.</span></span> <span data-ttu-id="f339f-160">請注意，所有提供者將事件寫入全域記錄器會話的提供者都會將事件寫入此記錄檔。</span><span class="sxs-lookup"><span data-stu-id="f339f-160">Note that all providers writing events to the Global Logger session write events to this log file.</span></span> <span data-ttu-id="f339f-161">路徑的限制為1024個字元。如果未指定 <strong>FileName</strong> ，則會將事件寫入至%SystemRoot%\System32\LogFiles\WMI\GlobalLogger.etl。</span><span class="sxs-lookup"><span data-stu-id="f339f-161">The path is limited to 1024 characters.If <strong>FileName</strong> is not specified, events are written to %SystemRoot%\System32\LogFiles\WMI\GlobalLogger.etl.</span></span> <span data-ttu-id="f339f-162"><strong>在 Windows Vista 之前：</strong> 預設檔案為%SystemRoot%\System32\LogFiles\WMI\Trace.log。</span><span class="sxs-lookup"><span data-stu-id="f339f-162"><strong>Prior to Windows Vista:</strong> The default file is %SystemRoot%\System32\LogFiles\WMI\Trace.log.</span></span><br/> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f339f-163"><strong>FlushTimer</strong></span><span class="sxs-lookup"><span data-stu-id="f339f-163"><strong>FlushTimer</strong></span></span></td>
<td><span data-ttu-id="f339f-164"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="f339f-164"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="f339f-165">強制排清追蹤緩衝區的頻率（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="f339f-165">How often, in seconds, the trace buffers are forcibly flushed.</span></span> <span data-ttu-id="f339f-166">最短排清時間為1秒。</span><span class="sxs-lookup"><span data-stu-id="f339f-166">The minimum flush time is 1 second.</span></span> <span data-ttu-id="f339f-167">這項強制排清是除了緩衝區已滿以及追蹤會話停止時所發生的自動排清之外。</span><span class="sxs-lookup"><span data-stu-id="f339f-167">This forced flush is in addition to the automatic flush that occurs when a buffer is full and when the trace session stops.</span></span> <br/> <span data-ttu-id="f339f-168">如果是即時記錄器， (預設值為零的值) 表示排清時間將會設定為1秒。</span><span class="sxs-lookup"><span data-stu-id="f339f-168">For the case of a real-time logger, a value of zero (the default value) means that the flush time will be set to 1 second.</span></span> <span data-ttu-id="f339f-169">當 <strong>LogFileMode</strong> 設定為 <strong>EVENT_TRACE_REAL_TIME_MODE</strong>時，即時記錄器就是。</span><span class="sxs-lookup"><span data-stu-id="f339f-169">A real-time logger is when <strong>LogFileMode</strong> is set to <strong>EVENT_TRACE_REAL_TIME_MODE</strong>.</span></span><br/> <span data-ttu-id="f339f-170">預設值為 0。</span><span class="sxs-lookup"><span data-stu-id="f339f-170">The default value is 0.</span></span> <span data-ttu-id="f339f-171">依預設，只有當緩衝區已滿時，才會排清緩衝區。</span><span class="sxs-lookup"><span data-stu-id="f339f-171">By default, buffers are flushed only when they are full.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f339f-172"><strong>LogFileMode</strong></span><span class="sxs-lookup"><span data-stu-id="f339f-172"><strong>LogFileMode</strong></span></span></td>
<td><span data-ttu-id="f339f-173"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="f339f-173"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="f339f-174">指定記錄會話選項。</span><span class="sxs-lookup"><span data-stu-id="f339f-174">Specifies log session options.</span></span> <span data-ttu-id="f339f-175">如需值，請參閱 <a href="logging-mode-constants.md">記錄模式常數</a>。</span><span class="sxs-lookup"><span data-stu-id="f339f-175">For values, see <a href="logging-mode-constants.md">Logging Mode Constants</a>.</span></span> <span data-ttu-id="f339f-176">Windows Vista 及更新版本支援此值。</span><span class="sxs-lookup"><span data-stu-id="f339f-176">This values is supported on Windows Vista and later.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f339f-177"><strong>MaximumBuffers</strong></span><span class="sxs-lookup"><span data-stu-id="f339f-177"><strong>MaximumBuffers</strong></span></span></td>
<td><span data-ttu-id="f339f-178"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="f339f-178"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="f339f-179">要配置的緩衝區數目上限。</span><span class="sxs-lookup"><span data-stu-id="f339f-179">The maximum number of buffers to allocate.</span></span> <span data-ttu-id="f339f-180">一般來說，此值是緩衝區數目下限加上二十。</span><span class="sxs-lookup"><span data-stu-id="f339f-180">Typically, this value is the minimum number of buffers plus twenty.</span></span> <span data-ttu-id="f339f-181">ETW 使用緩衝區大小和實體記憶體的大小來計算這個值。</span><span class="sxs-lookup"><span data-stu-id="f339f-181">ETW uses the buffer size and the size of physical memory to calculate this value.</span></span> <span data-ttu-id="f339f-182">此值必須大於或等於 <strong>MinimumBuffers</strong>的值。</span><span class="sxs-lookup"><span data-stu-id="f339f-182">This value must be greater than or equal to the value for <strong>MinimumBuffers</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f339f-183"><strong>MaxFileSize</strong></span><span class="sxs-lookup"><span data-stu-id="f339f-183"><strong>MaxFileSize</strong></span></span></td>
<td><span data-ttu-id="f339f-184"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="f339f-184"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="f339f-185">事件追蹤記錄檔的大小上限（以 mb 為單位）。</span><span class="sxs-lookup"><span data-stu-id="f339f-185">The maximum size, in megabytes, of the event trace log file.</span></span> <span data-ttu-id="f339f-186">根據預設值，沒有檔案大小限制。</span><span class="sxs-lookup"><span data-stu-id="f339f-186">By default, there is no maximum file size.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f339f-187"><strong>MinimumBuffers</strong></span><span class="sxs-lookup"><span data-stu-id="f339f-187"><strong>MinimumBuffers</strong></span></span></td>
<td><span data-ttu-id="f339f-188"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="f339f-188"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="f339f-189">全域記錄器會話啟動時要配置的緩衝區數目下限。</span><span class="sxs-lookup"><span data-stu-id="f339f-189">The minimum number of buffers to allocate when the Global Logger session starts.</span></span> <span data-ttu-id="f339f-190">您可以指定的緩衝區數目下限為每個處理器兩個緩衝區。</span><span class="sxs-lookup"><span data-stu-id="f339f-190">The minimum number of buffers that you can specify is two buffers per processor.</span></span> <span data-ttu-id="f339f-191">例如，在單處理器電腦上，緩衝區的最小數目為二。</span><span class="sxs-lookup"><span data-stu-id="f339f-191">For example, on a single processor computer, the minimum number of buffers is two.</span></span> <br/> <span data-ttu-id="f339f-192">單處理器系統上的預設值為0x3。</span><span class="sxs-lookup"><span data-stu-id="f339f-192">The default value on a single-processor system is 0x3.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f339f-193"><strong>狀態</strong></span><span class="sxs-lookup"><span data-stu-id="f339f-193"><strong>Status</strong></span></span></td>
<td><span data-ttu-id="f339f-194"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="f339f-194"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="f339f-195">全域記錄器的啟動狀態。</span><span class="sxs-lookup"><span data-stu-id="f339f-195">The startup status of the Global Logger.</span></span> <span data-ttu-id="f339f-196">如果全域記錄器無法啟動，則此機碼的值會是適當的 Win32 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="f339f-196">If the Global Logger failed to start, the value of this key is the appropriate Win32 error code.</span></span> <span data-ttu-id="f339f-197">如果全域記錄器成功啟動，則此索引鍵的值為 ERROR_SUCCESS (0) 。</span><span class="sxs-lookup"><span data-stu-id="f339f-197">If the Global Logger successfully started, the value of this key is ERROR_SUCCESS (0).</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="f339f-198">在修改登錄並重新啟動電腦之後，全域記錄器會話就會自動啟動，並且與任何其他會話一樣使用，但有一個例外狀況：您 \_ 使用 \_ \_) Wmistr 中定義的 WMI 全域記錄器識別碼常數控制碼 (，以參考全域記錄器會話。</span><span class="sxs-lookup"><span data-stu-id="f339f-198">After the registry has been modified and the computer restarted, the Global Logger session starts automatically and is used like any other session with one exception: You use the WMI\_GLOBAL\_LOGGER\_ID constant handle (defined in Wmistr.h) to reference the Global Logger session.</span></span> <span data-ttu-id="f339f-199">這個常數可用來當做接受會話控制碼之任何事件追蹤函數的引數。</span><span class="sxs-lookup"><span data-stu-id="f339f-199">This constant may be used as an argument to any event tracing function that accepts a session handle.</span></span> <span data-ttu-id="f339f-200">在接受會話名稱的函式中，使用全域 \_ 記錄器 \_ 名稱。</span><span class="sxs-lookup"><span data-stu-id="f339f-200">In functions that accept a session name, use GLOBAL\_LOGGER\_NAME.</span></span>

<span data-ttu-id="f339f-201">全域記錄器控制器不會呼叫 [**EnableTrace**](/windows/win32/api/evntrace/nf-evntrace-enabletrace) 函數來啟用提供者。</span><span class="sxs-lookup"><span data-stu-id="f339f-201">The Global Logger controller does not call the [**EnableTrace**](/windows/win32/api/evntrace/nf-evntrace-enabletrace) function to enable providers.</span></span> <span data-ttu-id="f339f-202">提供者負責判斷全域記錄器會話是否已啟動，然後再啟用它本身。</span><span class="sxs-lookup"><span data-stu-id="f339f-202">The provider is responsible for determining if the Global Logger session is started and then enabling itself.</span></span>

<span data-ttu-id="f339f-203">若要判斷全域記錄器會話是否已啟動，您可以呼叫 [**ControlTrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea) 函式，將 *SESSIONHANDLE* 設定為 WMI \_ 全域 \_ 記錄器識別碼， \_ 並 *ControlCode* 至 **事件 \_ 追蹤 \_ 控制 \_ 查詢**。</span><span class="sxs-lookup"><span data-stu-id="f339f-203">To determine if the Global Logger session is started, you can call the [**ControlTrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea) function, setting *SessionHandle* to WMI\_GLOBAL\_LOGGER\_ID and *ControlCode* to **EVENT\_TRACE\_CONTROL\_QUERY**.</span></span> <span data-ttu-id="f339f-204">如果 **ControlTrace** 呼叫成功，全域記錄器會話就會存在，而提供者可以啟用本身，並將事件記錄到全域記錄器會話 (**ControlTrace** 函式會 \_ 在 \_ \_ \_ 全域記錄器) 不是使用中時，傳回錯誤的 WMI 實例。</span><span class="sxs-lookup"><span data-stu-id="f339f-204">If the **ControlTrace** call is successful, the Global Logger session exists and the provider can enable itself and log events to the Global Logger session (the **ControlTrace** function returns ERROR\_WMI\_INSTANCE\_NOT\_FOUND if the Global Logger is not active).</span></span>

<span data-ttu-id="f339f-205">一般而言，控制器會負責在啟用提供者時，將啟用旗標和層級傳遞給提供者，但由於全域記錄器控制器未啟用提供者，因此，提供者會負責在需要時將這項資訊傳遞給本身。</span><span class="sxs-lookup"><span data-stu-id="f339f-205">Typically, the controller is responsible for passing the enable flags and level to the provider when it enables the provider, but because the Global Logger controller does not enable the provider, it is the provider's responsibility to pass this information to itself, if needed.</span></span>

<span data-ttu-id="f339f-206">全域記錄器會話是受限的資源，應謹慎使用。</span><span class="sxs-lookup"><span data-stu-id="f339f-206">The Global Logger session is a limited resource and should be used sparingly.</span></span> <span data-ttu-id="f339f-207">想要在開機過程中捕獲資訊的服務，應該考慮將控制器邏輯新增到本身，而不是使用全域記錄器會話。</span><span class="sxs-lookup"><span data-stu-id="f339f-207">Services that want to capture information during the boot process should consider adding controller logic to itself instead of using the Global Logger session.</span></span>

<span data-ttu-id="f339f-208">如需啟動事件追蹤會話的詳細資訊，請參閱設定 [和啟動事件追蹤會話](configuring-and-starting-an-event-tracing-session.md)。</span><span class="sxs-lookup"><span data-stu-id="f339f-208">For details on starting an event tracing session, see [Configuring and Starting an Event Tracing Session](configuring-and-starting-an-event-tracing-session.md).</span></span>

<span data-ttu-id="f339f-209">如需啟動私用記錄器會話的詳細資訊，請參閱設定 [和啟動私用記錄器會話](configuring-and-starting-a-private-logger-session.md)。</span><span class="sxs-lookup"><span data-stu-id="f339f-209">For details on starting a private logger session, see [Configuring and Starting a Private Logger Session](configuring-and-starting-a-private-logger-session.md).</span></span>

<span data-ttu-id="f339f-210">如需啟動 NT Kernel 記錄器會話的詳細資訊，請參閱設定 [和啟動 Nt Kernel 記錄器會話](configuring-and-starting-the-nt-kernel-logger-session.md)。</span><span class="sxs-lookup"><span data-stu-id="f339f-210">For details on starting an NT Kernel Logger session, see [Configuring and Starting the NT Kernel Logger Session](configuring-and-starting-the-nt-kernel-logger-session.md).</span></span>

