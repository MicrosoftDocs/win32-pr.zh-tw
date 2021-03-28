---
description: 「自動記錄器」事件追蹤會話會記錄在作業系統開機程式初期發生的事件。
ms.assetid: df5a79f4-abbf-4b83-afc3-cbd14b166067
title: 設定和啟動自動記錄器會話
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b17e7e818193aa4fa316d17a0e4392e41b55dfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973849"
---
# <a name="configuring-and-starting-an-autologger-session"></a><span data-ttu-id="4c966-103">設定和啟動自動記錄器會話</span><span class="sxs-lookup"><span data-stu-id="4c966-103">Configuring and Starting an AutoLogger Session</span></span>

<span data-ttu-id="4c966-104">「自動記錄器」事件追蹤會話會記錄在作業系統開機程式初期發生的事件。</span><span class="sxs-lookup"><span data-stu-id="4c966-104">The AutoLogger event tracing session records events that occur early in the operating system boot process.</span></span> <span data-ttu-id="4c966-105">應用程式和設備磁碟機可以在使用者登入之前，使用「自動記錄器」會話來捕捉追蹤。</span><span class="sxs-lookup"><span data-stu-id="4c966-105">Applications and device drivers can use the AutoLogger session to capture traces before the user logs in.</span></span> <span data-ttu-id="4c966-106">請注意，某些設備磁碟機（例如磁片設備磁碟機）在自動記錄器會話開始時不會載入。</span><span class="sxs-lookup"><span data-stu-id="4c966-106">Note that some device drivers, such as disk device drivers, are not loaded at the time the AutoLogger session begins.</span></span>

<span data-ttu-id="4c966-107">自動記錄器與全域記錄器有下列不同之處：</span><span class="sxs-lookup"><span data-stu-id="4c966-107">The AutoLogger differs from the Global Logger in the following ways:</span></span>

-   <span data-ttu-id="4c966-108">您可以指定一或多個自動記錄器會話， (全域記錄器是每個人記錄事件) 的單一會話。</span><span class="sxs-lookup"><span data-stu-id="4c966-108">You can specify one or more AutoLogger sessions (the Global Logger was a single session to which everyone logged events).</span></span>
-   <span data-ttu-id="4c966-109">當會話啟動時，自動記錄器會將啟用通知傳送給提供者， (全域記錄器不會將啟用通知傳送給提供者，因此提供者必須依賴其他方法來知道是否啟動全域記錄器會話，才能開始) 記錄事件。</span><span class="sxs-lookup"><span data-stu-id="4c966-109">The AutoLogger sends an enable notification to the providers when the session starts (the Global Logger did not send an enable notification to the providers, so the providers had to rely on other means to know if the Global Logger session was started in order to begin logging events).</span></span>
-   <span data-ttu-id="4c966-110">自動記錄器不支援記錄 NT 核心記錄器事件 (請參閱 [**事件 \_ 追蹤 \_ 屬性**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)的 **EnableFlags** 成員) 。</span><span class="sxs-lookup"><span data-stu-id="4c966-110">The AutoLogger does not support logging NT Kernel Logger events (see the **EnableFlags** member of [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)).</span></span> <span data-ttu-id="4c966-111">若要記錄 NT 核心記錄器事件，您必須使用 [全域記錄器](configuring-and-starting-the-global-logger-session.md)。</span><span class="sxs-lookup"><span data-stu-id="4c966-111">To log NT Kernel Logger events, you must use the [Global Logger](configuring-and-starting-the-global-logger-session.md).</span></span>

<span data-ttu-id="4c966-112">如需全域記錄器 seesion 的詳細資訊，請參閱設定 [和啟動全域記錄器會話](configuring-and-starting-the-global-logger-session.md)。</span><span class="sxs-lookup"><span data-stu-id="4c966-112">For more information on the Global Logger seesion, see [Configuring and Starting the Global Logger Session](configuring-and-starting-the-global-logger-session.md).</span></span>

> [!Note]  
> <span data-ttu-id="4c966-113">ETW 支援 Windows Vista 和更新版本上的自動記錄器。</span><span class="sxs-lookup"><span data-stu-id="4c966-113">ETW supports the AutoLogger on Windows Vista and later.</span></span> <span data-ttu-id="4c966-114">使用舊版作業系統上的 [全域記錄器](configuring-and-starting-the-global-logger-session.md) 。</span><span class="sxs-lookup"><span data-stu-id="4c966-114">Use the [Global Logger](configuring-and-starting-the-global-logger-session.md) on earlier operating systems.</span></span>

 

<span data-ttu-id="4c966-115">您可以使用登錄來設定自動記錄器會話。</span><span class="sxs-lookup"><span data-stu-id="4c966-115">You use the registry to configure the AutoLogger session.</span></span> <span data-ttu-id="4c966-116">新增下列登錄機碼（如果尚未存在）：</span><span class="sxs-lookup"><span data-stu-id="4c966-116">Add the following registry key, if it is not already present:</span></span>

```
HKEY_LOCAL_MACHINE
   \SYSTEM
      \CurrentControlSet
         \Control
            \WMI
               \Autologger
```

<span data-ttu-id="4c966-117">在 [自動 **記錄器** ] 機碼底下，針對您想要設定的每個自動記錄器會話建立金鑰，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="4c966-117">Under the **Autologger** key create a key for each AutoLogger session that you want to configure as shown in the following example.</span></span>

```
HKEY_LOCAL_MACHINE
   \SYSTEM
      \CurrentControlSet
         \Control
            \WMI
               \Autologger
                  \Logger Session A
                  \Logger Session B
                  \Logger Session C
```

<span data-ttu-id="4c966-118">針對每個會話，為您想要啟用至會話的每個提供者建立金鑰。</span><span class="sxs-lookup"><span data-stu-id="4c966-118">For each session, create a key for each provider that you want to enable to the session.</span></span> <span data-ttu-id="4c966-119">使用提供者的 GUID 作為索引鍵。</span><span class="sxs-lookup"><span data-stu-id="4c966-119">Use the provider's GUID as the key.</span></span>

```
HKEY_LOCAL_MACHINE
   \SYSTEM
      \CurrentControlSet
         \Control
            \WMI
               \Autologger
                  \Logger Session A
                     \{ProviderGuid1}
                     \{ProviderGuid2}
                  \Logger Session B
                  \Logger Session C
```

<span data-ttu-id="4c966-120">下表描述您可以為每個自動記錄器會話定義的值。</span><span class="sxs-lookup"><span data-stu-id="4c966-120">The following table describes the values that you can define for each AutoLogger session.</span></span> <span data-ttu-id="4c966-121">您必須具有系統管理員許可權，才能指定這些登錄值。</span><span class="sxs-lookup"><span data-stu-id="4c966-121">You must have administrator privileges to specify these registry values.</span></span> <span data-ttu-id="4c966-122">**開始** 和 **Guid** 值是啟動自動記錄器會話所需的唯一值;如果登錄中沒有值，所有其他值都有預設的設定。</span><span class="sxs-lookup"><span data-stu-id="4c966-122">The **Start** and **Guid** value are the only values required to start the AutoLogger session; all other values have default settings that are used if the value is not present in the registry.</span></span> <span data-ttu-id="4c966-123">一般而言，您應該使用預設值。</span><span class="sxs-lookup"><span data-stu-id="4c966-123">Typically, you should use the default values.</span></span> <span data-ttu-id="4c966-124">如果您指定 ETW 無法支援的值，ETW 將會覆寫此值。</span><span class="sxs-lookup"><span data-stu-id="4c966-124">If you specify a value that ETW cannot support, ETW will override the value.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4c966-125">值</span><span class="sxs-lookup"><span data-stu-id="4c966-125">Value</span></span></th>
<th><span data-ttu-id="4c966-126">類型</span><span class="sxs-lookup"><span data-stu-id="4c966-126">Type</span></span></th>
<th><span data-ttu-id="4c966-127">Description</span><span class="sxs-lookup"><span data-stu-id="4c966-127">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4c966-128"><strong>BufferSize</strong></span><span class="sxs-lookup"><span data-stu-id="4c966-128"><strong>BufferSize</strong></span></span></td>
<td><span data-ttu-id="4c966-129"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="4c966-129"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="4c966-130">每個緩衝區的大小（以 kb 為單位）。</span><span class="sxs-lookup"><span data-stu-id="4c966-130">The size of each buffer, in kilobytes.</span></span> <span data-ttu-id="4c966-131">應小於 1 mb。</span><span class="sxs-lookup"><span data-stu-id="4c966-131">Should be less than one megabyte.</span></span> <span data-ttu-id="4c966-132">ETW 使用實體記憶體的大小來計算這個值。</span><span class="sxs-lookup"><span data-stu-id="4c966-132">ETW uses the size of physical memory to calculate this value.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4c966-133"><strong>ClockType</strong></span><span class="sxs-lookup"><span data-stu-id="4c966-133"><strong>ClockType</strong></span></span></td>
<td><span data-ttu-id="4c966-134"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="4c966-134"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="4c966-135">記錄每個事件的時間戳記時要使用的計時器。</span><span class="sxs-lookup"><span data-stu-id="4c966-135">The timer to use when logging the time stamp for each event.</span></span>
<ul>
<li><span data-ttu-id="4c966-136">1 = 效能計數器值 (高解析度) </span><span class="sxs-lookup"><span data-stu-id="4c966-136">1 = Performance counter value (high resolution)</span></span></li>
<li><span data-ttu-id="4c966-137">2 = 系統計時器</span><span class="sxs-lookup"><span data-stu-id="4c966-137">2 = System timer</span></span></li>
<li><span data-ttu-id="4c966-138">3 = CPU 週期計數器</span><span class="sxs-lookup"><span data-stu-id="4c966-138">3 = CPU cycle counter</span></span></li>
</ul>
<span data-ttu-id="4c966-139">如需每種頻率類型的描述，請參閱<a href="wnode-header.md"><strong>WNODE_HEADER</strong></a>的<strong>ClientCoNtext</strong>成員。</span><span class="sxs-lookup"><span data-stu-id="4c966-139">For a description of each clock type, see the <strong>ClientContext</strong> member of <a href="wnode-header.md"><strong>WNODE_HEADER</strong></a>.</span></span><br/> <span data-ttu-id="4c966-140">在 Windows Vista 和更新版本上，預設值為 1 (效能計數器值) 。</span><span class="sxs-lookup"><span data-stu-id="4c966-140">The default value is 1 (performance counter value) on Windows Vista and later.</span></span> <span data-ttu-id="4c966-141">在 Windows Vista 之前，預設值為 2 (系統計時器) 。</span><span class="sxs-lookup"><span data-stu-id="4c966-141">Prior to Windows Vista, the default value is 2 (system timer).</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4c966-142"><strong>DisableRealtimePersistence</strong></span><span class="sxs-lookup"><span data-stu-id="4c966-142"><strong>DisableRealtimePersistence</strong></span></span></td>
<td><span data-ttu-id="4c966-143"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="4c966-143"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="4c966-144">若要停用即時持續性，請將此值設定為1。</span><span class="sxs-lookup"><span data-stu-id="4c966-144">To disable real time persistence, set this value to 1.</span></span> <span data-ttu-id="4c966-145">預設值為 0 (啟用即時會話) 。</span><span class="sxs-lookup"><span data-stu-id="4c966-145">The default is 0 (enabled) for real time sessions.</span></span><br/> <span data-ttu-id="4c966-146">如果已啟用即時持續性，則在關閉電腦時未傳遞的即時事件將會被保存。</span><span class="sxs-lookup"><span data-stu-id="4c966-146">If real time persistence is enabled, real-time events that were not delivered by the time the computer was shutdown will be persisted.</span></span> <span data-ttu-id="4c966-147">然後，當取用者下次連接會話時，事件就會傳遞給取用者。</span><span class="sxs-lookup"><span data-stu-id="4c966-147">The events will then be delivered to the consumer the next time the consumer connects to the session.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4c966-148"><strong>FileCounter</strong></span><span class="sxs-lookup"><span data-stu-id="4c966-148"><strong>FileCounter</strong></span></span></td>
<td><span data-ttu-id="4c966-149"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="4c966-149"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="4c966-150">請勿設定或修改此值。</span><span class="sxs-lookup"><span data-stu-id="4c966-150">Do not set or modify this value.</span></span> <span data-ttu-id="4c966-151">如果指定 <strong>FileMax</strong> ，則這個值是用來遞增記錄檔名稱的序號。</span><span class="sxs-lookup"><span data-stu-id="4c966-151">This value is the serial number used to increment the log file name if <strong>FileMax</strong> is specified.</span></span> <span data-ttu-id="4c966-152">如果值無效，則會假設為1。</span><span class="sxs-lookup"><span data-stu-id="4c966-152">If the value is not valid, 1 will be assumed.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4c966-153"><strong>FileName</strong></span><span class="sxs-lookup"><span data-stu-id="4c966-153"><strong>FileName</strong></span></span></td>
<td><span data-ttu-id="4c966-154"><strong>REG_SZ</strong></span><span class="sxs-lookup"><span data-stu-id="4c966-154"><strong>REG_SZ</strong></span></span></td>
<td><span data-ttu-id="4c966-155">記錄檔的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="4c966-155">The fully qualified path of the log file.</span></span> <span data-ttu-id="4c966-156">這個檔案的路徑必須存在。</span><span class="sxs-lookup"><span data-stu-id="4c966-156">The path to this file must exist.</span></span> <span data-ttu-id="4c966-157">記錄檔是連續的記錄檔。</span><span class="sxs-lookup"><span data-stu-id="4c966-157">The log file is a sequential log file.</span></span> <span data-ttu-id="4c966-158">路徑的限制為1024個字元。</span><span class="sxs-lookup"><span data-stu-id="4c966-158">The path is limited to 1024 characters.</span></span><br/> <span data-ttu-id="4c966-159">如果未指定 <strong>FileName</strong> ，則會將事件寫入%SystemRoot%\System32\LogFiles\WMI\ <sessionname> 。</span><span class="sxs-lookup"><span data-stu-id="4c966-159">If <strong>FileName</strong> is not specified, events are written to %SystemRoot%\System32\LogFiles\WMI\<sessionname>.etl.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4c966-160"><strong>FileMax</strong></span><span class="sxs-lookup"><span data-stu-id="4c966-160"><strong>FileMax</strong></span></span></td>
<td><span data-ttu-id="4c966-161"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="4c966-161"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="4c966-162">ETW 所建立記錄檔的最大實例數目。</span><span class="sxs-lookup"><span data-stu-id="4c966-162">The maximum number of instances of the log file that ETW creates.</span></span> <span data-ttu-id="4c966-163">如果 <strong>檔案名</strong> 中指定的記錄檔存在，ETW 會將 <strong>FileCounter</strong> 值附加至檔案名。</span><span class="sxs-lookup"><span data-stu-id="4c966-163">If the log file specified in <strong>FileName</strong> exists, ETW appends the <strong>FileCounter</strong> value to the file name.</span></span> <span data-ttu-id="4c966-164">例如，如果使用預設的記錄檔名稱，則格式為%SystemRoot%\System32\LogFiles\WMI\ <sessionname> 。NNNN.</span><span class="sxs-lookup"><span data-stu-id="4c966-164">For example, if the default log file name is used, the form is %SystemRoot%\System32\LogFiles\WMI\<sessionname>.etl.NNNN.</span></span> <br/> <span data-ttu-id="4c966-165">電腦第一次啟動時，檔案名是 <sessionname> .etl，第二次檔案名是 <sessionname> .etl. 0002，依此類推。</span><span class="sxs-lookup"><span data-stu-id="4c966-165">The first time the computer is started, the file name is <sessionname>.etl.0001, the second time the file name is <sessionname>.etl.0002, and so on.</span></span> <span data-ttu-id="4c966-166">如果 <strong>FileMax</strong> 為3，則在第四次重新開機電腦時，ETW 會將計數器重設為1，並覆寫 <sessionname> .etl （如果存在的話）。</span><span class="sxs-lookup"><span data-stu-id="4c966-166">If <strong>FileMax</strong> is 3, on the fourth restart of the computer, ETW resets the counter to 1 and overwrites <sessionname>.etl.0001, if it exists.</span></span><br/> <span data-ttu-id="4c966-167">支援的記錄檔實例數目上限為16。</span><span class="sxs-lookup"><span data-stu-id="4c966-167">The maximum number of instances of the log file that are supported is 16.</span></span><br/> <span data-ttu-id="4c966-168">請勿將這項功能與 <a href="logging-mode-constants.md">EVENT_TRACE_FILE_MODE_NEWFILE</a> 記錄檔模式搭配使用。</span><span class="sxs-lookup"><span data-stu-id="4c966-168">Do not use this feature with the <a href="logging-mode-constants.md">EVENT_TRACE_FILE_MODE_NEWFILE</a> log file mode.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4c966-169"><strong>FlushTimer</strong></span><span class="sxs-lookup"><span data-stu-id="4c966-169"><strong>FlushTimer</strong></span></span></td>
<td><span data-ttu-id="4c966-170"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="4c966-170"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="4c966-171">強制排清追蹤緩衝區的頻率（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="4c966-171">How often, in seconds, the trace buffers are forcibly flushed.</span></span> <span data-ttu-id="4c966-172">最短排清時間為1秒。</span><span class="sxs-lookup"><span data-stu-id="4c966-172">The minimum flush time is 1 second.</span></span> <span data-ttu-id="4c966-173">這項強制排清是除了緩衝區已滿以及追蹤會話停止時所發生的自動排清之外。</span><span class="sxs-lookup"><span data-stu-id="4c966-173">This forced flush is in addition to the automatic flush that occurs when a buffer is full and when the trace session stops.</span></span> <br/> <span data-ttu-id="4c966-174">如果是即時記錄器， (預設值為零的值) 表示排清時間將會設定為1秒。</span><span class="sxs-lookup"><span data-stu-id="4c966-174">For the case of a real-time logger, a value of zero (the default value) means that the flush time will be set to 1 second.</span></span> <span data-ttu-id="4c966-175">當 <strong>LogFileMode</strong> 設定為 <strong>EVENT_TRACE_REAL_TIME_MODE</strong>時，即時記錄器就是。</span><span class="sxs-lookup"><span data-stu-id="4c966-175">A real-time logger is when <strong>LogFileMode</strong> is set to <strong>EVENT_TRACE_REAL_TIME_MODE</strong>.</span></span><br/> <span data-ttu-id="4c966-176">預設值為 0。</span><span class="sxs-lookup"><span data-stu-id="4c966-176">The default value is 0.</span></span> <span data-ttu-id="4c966-177">依預設，只有當緩衝區已滿時，才會排清緩衝區。</span><span class="sxs-lookup"><span data-stu-id="4c966-177">By default, buffers are flushed only when they are full.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4c966-178"><strong>Guid</strong></span><span class="sxs-lookup"><span data-stu-id="4c966-178"><strong>Guid</strong></span></span></td>
<td><span data-ttu-id="4c966-179"><strong>REG_SZ</strong></span><span class="sxs-lookup"><span data-stu-id="4c966-179"><strong>REG_SZ</strong></span></span></td>
<td><span data-ttu-id="4c966-180">字串，包含可唯一識別會話的 GUID。</span><span class="sxs-lookup"><span data-stu-id="4c966-180">A string that contains a GUID that uniquely identifies the session.</span></span> <span data-ttu-id="4c966-181">這是必要的值。</span><span class="sxs-lookup"><span data-stu-id="4c966-181">This value is required.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4c966-182"><strong>LogFileMode</strong></span><span class="sxs-lookup"><span data-stu-id="4c966-182"><strong>LogFileMode</strong></span></span></td>
<td><span data-ttu-id="4c966-183"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="4c966-183"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="4c966-184">指定一或多個記錄模式。</span><span class="sxs-lookup"><span data-stu-id="4c966-184">Specify one or more log modes.</span></span> <span data-ttu-id="4c966-185">如需可能的值，請參閱 <a href="logging-mode-constants.md">記錄模式常數</a>。</span><span class="sxs-lookup"><span data-stu-id="4c966-185">For possible values, see <a href="logging-mode-constants.md">Logging Mode Constants</a>.</span></span> <span data-ttu-id="4c966-186">預設值為 <strong>EVENT_TRACE_FILE_MODE_SEQUENTIAL</strong>。</span><span class="sxs-lookup"><span data-stu-id="4c966-186">The default is <strong>EVENT_TRACE_FILE_MODE_SEQUENTIAL</strong>.</span></span> <span data-ttu-id="4c966-187">您可以指定 <strong>EVENT_TRACE_BUFFERING_MODE</strong> 或 <strong>EVENT_TRACE_REAL_TIME_MODE</strong>，而不是寫入記錄檔。</span><span class="sxs-lookup"><span data-stu-id="4c966-187">Instead of writing to a log file, you can specify either <strong>EVENT_TRACE_BUFFERING_MODE</strong> or <strong>EVENT_TRACE_REAL_TIME_MODE</strong>.</span></span><br/> <span data-ttu-id="4c966-188">指定 <strong>EVENT_TRACE_BUFFERING_MODE</strong> 可避免在檔案系統變成可用時，將會話內容排清至磁片的成本。</span><span class="sxs-lookup"><span data-stu-id="4c966-188">Specifying <strong>EVENT_TRACE_BUFFERING_MODE</strong> avoids the cost of flushing the contents of the session to disk when the file system becomes available.</span></span> <br/> <span data-ttu-id="4c966-189">請注意，使用 <strong>EVENT_TRACE_BUFFERING_MODE</strong> 會導致系統忽略 <strong>MaximumBuffers</strong> 值，因為緩衝區大小是 <strong>MinimumBuffers</strong> 和 <strong>BufferSize</strong>的乘積。</span><span class="sxs-lookup"><span data-stu-id="4c966-189">Note that using <strong>EVENT_TRACE_BUFFERING_MODE</strong> will cause the system to ignore the <strong>MaximumBuffers</strong> value, as the buffer size is instead the product of <strong>MinimumBuffers</strong> and <strong>BufferSize</strong>.</span></span><br/> <span data-ttu-id="4c966-190">自動記錄器會話不支援 <strong>EVENT_TRACE_FILE_MODE_NEWFILE</strong> 記錄模式。</span><span class="sxs-lookup"><span data-stu-id="4c966-190">AutoLogger sessions do not support the <strong>EVENT_TRACE_FILE_MODE_NEWFILE</strong> logging mode.</span></span><br/> <span data-ttu-id="4c966-191">如果指定 <strong>EVENT_TRACE_FILE_MODE_APPEND</strong> ，則必須明確提供 <strong>BufferSize</strong> ，而且在記錄器和附加的檔案中都必須相同。</span><span class="sxs-lookup"><span data-stu-id="4c966-191">If <strong>EVENT_TRACE_FILE_MODE_APPEND</strong> is specified, <strong>BufferSize</strong> must be explicitly provided and must be the same in both the logger and the file being appended.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4c966-192"><strong>MaxFileSize</strong></span><span class="sxs-lookup"><span data-stu-id="4c966-192"><strong>MaxFileSize</strong></span></span></td>
<td><span data-ttu-id="4c966-193"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="4c966-193"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="4c966-194">記錄檔的檔案大小上限（以 mb 為單位）。</span><span class="sxs-lookup"><span data-stu-id="4c966-194">The maximum file size of the log file, in megabytes.</span></span> <span data-ttu-id="4c966-195">當到達大小上限時，會關閉會話，除非您處於迴圈記錄檔模式。</span><span class="sxs-lookup"><span data-stu-id="4c966-195">The session is closed when the maximum size is reached, unless you are in circular log file mode.</span></span> <span data-ttu-id="4c966-196">若要指定無限制，請將值設定為0。</span><span class="sxs-lookup"><span data-stu-id="4c966-196">To specify no limit, set value to 0.</span></span> <span data-ttu-id="4c966-197">如果未設定，預設值為 100 MB。</span><span class="sxs-lookup"><span data-stu-id="4c966-197">The default is 100 MB, if not set.</span></span> <span data-ttu-id="4c966-198">當達到檔案大小上限時所發生的行為，取決於 <strong>LogFileMode</strong>的值。</span><span class="sxs-lookup"><span data-stu-id="4c966-198">The behavior that occurs when the maximum file size is reached depends on the value of <strong>LogFileMode</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4c966-199"><strong>MaximumBuffers</strong></span><span class="sxs-lookup"><span data-stu-id="4c966-199"><strong>MaximumBuffers</strong></span></span></td>
<td><span data-ttu-id="4c966-200"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="4c966-200"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="4c966-201">要配置的緩衝區數目上限。</span><span class="sxs-lookup"><span data-stu-id="4c966-201">The maximum number of buffers to allocate.</span></span> <span data-ttu-id="4c966-202">一般來說，此值是緩衝區數目下限加上二十。</span><span class="sxs-lookup"><span data-stu-id="4c966-202">Typically, this value is the minimum number of buffers plus twenty.</span></span> <span data-ttu-id="4c966-203">ETW 使用緩衝區大小和實體記憶體的大小來計算這個值。</span><span class="sxs-lookup"><span data-stu-id="4c966-203">ETW uses the buffer size and the size of physical memory to calculate this value.</span></span> <span data-ttu-id="4c966-204">此值必須大於或等於 <strong>MinimumBuffers</strong>的值。</span><span class="sxs-lookup"><span data-stu-id="4c966-204">This value must be greater than or equal to the value for <strong>MinimumBuffers</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4c966-205"><strong>MinimumBuffers</strong></span><span class="sxs-lookup"><span data-stu-id="4c966-205"><strong>MinimumBuffers</strong></span></span></td>
<td><span data-ttu-id="4c966-206"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="4c966-206"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="4c966-207">啟動時要配置的緩衝區數目下限。</span><span class="sxs-lookup"><span data-stu-id="4c966-207">The minimum number of buffers to allocate at startup.</span></span> <span data-ttu-id="4c966-208">您可以指定的緩衝區數目下限為每個處理器兩個緩衝區。</span><span class="sxs-lookup"><span data-stu-id="4c966-208">The minimum number of buffers that you can specify is two buffers per processor.</span></span> <span data-ttu-id="4c966-209">例如，在單處理器電腦上，緩衝區的最小數目為二。</span><span class="sxs-lookup"><span data-stu-id="4c966-209">For example, on a single processor computer, the minimum number of buffers is two.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4c966-210"><strong>開始</strong></span><span class="sxs-lookup"><span data-stu-id="4c966-210"><strong>Start</strong></span></span></td>
<td><span data-ttu-id="4c966-211"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="4c966-211"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="4c966-212">若要在下次重新開機電腦時啟動重新開機記錄器會話，請將此值設為 1;否則，請將此值設定為0。</span><span class="sxs-lookup"><span data-stu-id="4c966-212">To have the AutoLogger session start the next time the computer is restarted, set this value to 1; otherwise, set this value to 0.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4c966-213"><strong>狀態</strong></span><span class="sxs-lookup"><span data-stu-id="4c966-213"><strong>Status</strong></span></span></td>
<td><span data-ttu-id="4c966-214"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="4c966-214"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="4c966-215">自動記錄器的啟動狀態。</span><span class="sxs-lookup"><span data-stu-id="4c966-215">The startup status of the AutoLogger.</span></span> <span data-ttu-id="4c966-216">如果無法啟動自動記錄器，此機碼的值會是適當的 Win32 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="4c966-216">If the AutoLogger failed to start, the value of this key is the appropriate Win32 error code.</span></span> <span data-ttu-id="4c966-217">如果自動記錄器成功啟動，則此機碼的值會 <strong>ERROR_SUCCESS</strong> (0) 。</span><span class="sxs-lookup"><span data-stu-id="4c966-217">If the AutoLogger successfully started, the value of this key is <strong>ERROR_SUCCESS</strong> (0).</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="4c966-218">下表描述您可以針對您想要啟用至會話的每個提供者定義的值。</span><span class="sxs-lookup"><span data-stu-id="4c966-218">The following table describes the values that you can define for each provider that you want to enable to your session.</span></span> <span data-ttu-id="4c966-219">您必須具有系統管理員許可權，才能指定這些登錄值。</span><span class="sxs-lookup"><span data-stu-id="4c966-219">You must have administrator privileges to specify these registry values.</span></span> <span data-ttu-id="4c966-220">如果您指定 ETW 無法支援的值，ETW 將會覆寫此值。</span><span class="sxs-lookup"><span data-stu-id="4c966-220">If you specify a value that ETW cannot support, ETW will override the value.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4c966-221">值</span><span class="sxs-lookup"><span data-stu-id="4c966-221">Value</span></span></th>
<th><span data-ttu-id="4c966-222">類型</span><span class="sxs-lookup"><span data-stu-id="4c966-222">Type</span></span></th>
<th><span data-ttu-id="4c966-223">Description</span><span class="sxs-lookup"><span data-stu-id="4c966-223">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4c966-224"><strong>Enabled</strong></span><span class="sxs-lookup"><span data-stu-id="4c966-224"><strong>Enabled</strong></span></span></td>
<td><span data-ttu-id="4c966-225"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="4c966-225"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="4c966-226">判斷是否已啟用提供者。</span><span class="sxs-lookup"><span data-stu-id="4c966-226">Determines if the provider is enabled.</span></span> <span data-ttu-id="4c966-227">若要啟用提供者，請將此值設定為1。</span><span class="sxs-lookup"><span data-stu-id="4c966-227">To enable the provider, set this value to 1.</span></span> <span data-ttu-id="4c966-228">若要停用提供者，請將此值設定為0。</span><span class="sxs-lookup"><span data-stu-id="4c966-228">To disable the provider, set this value to 0.</span></span> <span data-ttu-id="4c966-229">預設值是 0。</span><span class="sxs-lookup"><span data-stu-id="4c966-229">The default is 0.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4c966-230"><strong>EnableFlags</strong></span><span class="sxs-lookup"><span data-stu-id="4c966-230"><strong>EnableFlags</strong></span></span></td>
<td><span data-ttu-id="4c966-231"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="4c966-231"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="4c966-232">提供者定義的值，這個值會指定提供者產生事件的事件類別。</span><span class="sxs-lookup"><span data-stu-id="4c966-232">Provider-defined value that specifies the class of events for which the provider generates events.</span></span> <span data-ttu-id="4c966-233">如需詳細資訊，請參閱<a href="/windows/win32/api/evntrace/nf-evntrace-enabletrace"><strong>EnableTrace</strong></a>函數的<em>EnableFlags</em>參數。</span><span class="sxs-lookup"><span data-stu-id="4c966-233">For details, see the <em>EnableFlags</em> parameter of the <a href="/windows/win32/api/evntrace/nf-evntrace-enabletrace"><strong>EnableTrace</strong></a> function.</span></span> <span data-ttu-id="4c966-234">如果提供者不支援 <strong>MatchAnyKeyword</strong> 或 <strong>MatchAllKeyword</strong>，請指定此值名稱。</span><span class="sxs-lookup"><span data-stu-id="4c966-234">Specify this value name if the provider does not support <strong>MatchAnyKeyword</strong> or <strong>MatchAllKeyword</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4c966-235"><strong>EnableLevel</strong></span><span class="sxs-lookup"><span data-stu-id="4c966-235"><strong>EnableLevel</strong></span></span></td>
<td><span data-ttu-id="4c966-236"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="4c966-236"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="4c966-237">提供者定義的值，這個值會指定事件中包含的詳細層級。</span><span class="sxs-lookup"><span data-stu-id="4c966-237">Provider-defined value that specifies the level of detail included in the event.</span></span> <span data-ttu-id="4c966-238">例如，您可以使用這個值來指出事件的嚴重性層級 (提供者所產生的資訊、警告、錯誤) 。</span><span class="sxs-lookup"><span data-stu-id="4c966-238">For example, you can use this value to indicate the severity level of the events (informational, warning, error) that the provider generates.</span></span> <span data-ttu-id="4c966-239">如需預先定義的層級清單，請參閱<a href="/windows/win32/api/evntrace/nf-evntrace-enabletraceex"><strong>EnableTraceEx</strong></a>函數的<em>level</em>參數。</span><span class="sxs-lookup"><span data-stu-id="4c966-239">For a list of predefined levels, see the <em>level</em> parameter of the <a href="/windows/win32/api/evntrace/nf-evntrace-enabletraceex"><strong>EnableTraceEx</strong></a> function.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4c966-240"><strong>EnableProperty</strong></span><span class="sxs-lookup"><span data-stu-id="4c966-240"><strong>EnableProperty</strong></span></span></td>
<td><span data-ttu-id="4c966-241"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="4c966-241"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="4c966-242">使用此值可在記錄檔中包含下列一或多個專案：</span><span class="sxs-lookup"><span data-stu-id="4c966-242">Use this value to include one or more of the following items in the log file:</span></span>
<ul>
<li><span data-ttu-id="4c966-243"><strong>EVENT_ENABLE_PROPERTY_SID</strong> (0x00000001) = 在擴充的資料中包含使用者的安全識別碼 (SID) 。</span><span class="sxs-lookup"><span data-stu-id="4c966-243"><strong>EVENT_ENABLE_PROPERTY_SID</strong> (0x00000001) = Include in the extended data the security identifier (SID) of the user.</span></span></li>
<li><span data-ttu-id="4c966-244"><strong>EVENT_ENABLE_PROPERTY_TS_ID</strong> (0x00000002) = 將終端機會話識別碼包含在擴充的資料中。</span><span class="sxs-lookup"><span data-stu-id="4c966-244"><strong>EVENT_ENABLE_PROPERTY_TS_ID</strong> (0x00000002) = Include in the extended data the terminal session identifier.</span></span></li>
<li><span data-ttu-id="4c966-245"><strong>EVENT_ENABLE_PROPERTY_STACK_TRACE</strong> (0x00000004) = 包含在擴充的資料中，使用 <a href="/windows/desktop/api/Evntprov/nf-evntprov-eventwrite"><strong>EventWrite</strong></a>撰寫之事件的呼叫堆疊追蹤。</span><span class="sxs-lookup"><span data-stu-id="4c966-245"><strong>EVENT_ENABLE_PROPERTY_STACK_TRACE</strong> (0x00000004) = Include in the extended data a call stack trace for events written using <a href="/windows/desktop/api/Evntprov/nf-evntprov-eventwrite"><strong>EventWrite</strong></a>.</span></span></li>
<li><span data-ttu-id="4c966-246"><strong>EVENT_ENABLE_PROPERTY_IGNORE_KEYWORD_0</strong> (0x00000010) = 篩選出未指定非零關鍵字的所有事件。</span><span class="sxs-lookup"><span data-stu-id="4c966-246"><strong>EVENT_ENABLE_PROPERTY_IGNORE_KEYWORD_0</strong> (0x00000010) = Filters out all events that do not have a non-zero keyword specified.</span></span></li>
<li><span data-ttu-id="4c966-247"><strong>EVENT_ENABLE_PROPERTY_PROVIDER_GROUP</strong> (0x00000020) = 表示這個 <a href="/windows/win32/api/evntrace/nf-evntrace-enabletraceex2"><strong>EnableTraceEx2</strong></a> 呼叫應該啟用 <a href="provider-traits.md">提供者群組</a> ，而不是個別事件提供者。</span><span class="sxs-lookup"><span data-stu-id="4c966-247"><strong>EVENT_ENABLE_PROPERTY_PROVIDER_GROUP</strong> (0x00000020) = Indicates that this call to <a href="/windows/win32/api/evntrace/nf-evntrace-enabletraceex2"><strong>EnableTraceEx2</strong></a> should enable a <a href="provider-traits.md">Provider Group</a> rather than an individual Event Provider.</span></span></li>
<li><span data-ttu-id="4c966-248"><strong>EVENT_ENABLE_PROPERTY_PROCESS_START_KEY</strong> (0x00000080) = 在擴充的資料中包含處理常式啟動金鑰。</span><span class="sxs-lookup"><span data-stu-id="4c966-248"><strong>EVENT_ENABLE_PROPERTY_PROCESS_START_KEY</strong> (0x00000080) = Include the Process Start Key in the extended data.</span></span></li>
<li><span data-ttu-id="4c966-249"><strong>EVENT_ENABLE_PROPERTY_EVENT_KEY</strong> (0x00000100) = 在擴充的資料中包含事件索引鍵。</span><span class="sxs-lookup"><span data-stu-id="4c966-249"><strong>EVENT_ENABLE_PROPERTY_EVENT_KEY</strong> (0x00000100) = Include the Event Key in the extended data.</span></span></li>
<li><span data-ttu-id="4c966-250"><strong>EVENT_ENABLE_PROPERTY_EXCLUDE_INPRI加值稅E</strong> (0x00000200) = 篩選出標記為 inprivate 事件或來自標示為 inprivate 之進程的所有事件。</span><span class="sxs-lookup"><span data-stu-id="4c966-250"><strong>EVENT_ENABLE_PROPERTY_EXCLUDE_INPRIVATE</strong> (0x00000200) = Filters out all events that are either marked as an InPrivate event or come from a process that is marked as InPrivate.</span></span></li>
</ul>
<span data-ttu-id="4c966-251">如需這些專案的詳細資訊，請參閱<a href="/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters"><strong>ENABLE_TRACE_PARAMETERS</strong></a>結構的<strong>EnableProperty</strong> 。</span><span class="sxs-lookup"><span data-stu-id="4c966-251">For more information about these items, see the <strong>EnableProperty</strong> of the <a href="/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters"><strong>ENABLE_TRACE_PARAMETERS</strong></a> structure.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4c966-252"><strong>MatchAnyKeyword</strong></span><span class="sxs-lookup"><span data-stu-id="4c966-252"><strong>MatchAnyKeyword</strong></span></span></td>
<td><span data-ttu-id="4c966-253"><strong>REG_QWORD</strong></span><span class="sxs-lookup"><span data-stu-id="4c966-253"><strong>REG_QWORD</strong></span></span></td>
<td><span data-ttu-id="4c966-254">關鍵字的位元遮罩，可決定您想要提供者寫入的事件類別。</span><span class="sxs-lookup"><span data-stu-id="4c966-254">Bitmask of keywords that determine the category of events that you want the provider to write.</span></span> <span data-ttu-id="4c966-255">如果任何事件的關鍵字位符合此遮罩中設定的任何位，則提供者會寫入事件。</span><span class="sxs-lookup"><span data-stu-id="4c966-255">The provider writes the event if any of the event's keyword bits match any of the bits set in this mask.</span></span> <span data-ttu-id="4c966-256">若要指定提供者寫入所有事件，請將此值設定為零。</span><span class="sxs-lookup"><span data-stu-id="4c966-256">To specify that the provider write all events, set this value to zero.</span></span> <span data-ttu-id="4c966-257">如需範例，請參閱 <a href="/windows/win32/api/evntrace/nf-evntrace-enabletraceex"><strong>EnableTraceEx</strong></a> 函數的備註一節。</span><span class="sxs-lookup"><span data-stu-id="4c966-257">For an example, see the Remarks section of the <a href="/windows/win32/api/evntrace/nf-evntrace-enabletraceex"><strong>EnableTraceEx</strong></a> function.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4c966-258"><strong>MatchAllKeyword</strong></span><span class="sxs-lookup"><span data-stu-id="4c966-258"><strong>MatchAllKeyword</strong></span></span></td>
<td><span data-ttu-id="4c966-259"><strong>REG_QWORD</strong></span><span class="sxs-lookup"><span data-stu-id="4c966-259"><strong>REG_QWORD</strong></span></span></td>
<td><span data-ttu-id="4c966-260">此位元遮罩是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="4c966-260">This bitmask is optional.</span></span> <span data-ttu-id="4c966-261">這個遮罩會進一步限制您希望提供者寫入的事件類別。</span><span class="sxs-lookup"><span data-stu-id="4c966-261">This mask further restricts the category of events that you want the provider to write.</span></span> <span data-ttu-id="4c966-262">如果事件的關鍵字符合 <em>MatchAnyKeyword</em> 條件，則只有在這個遮罩中的所有位都存在於事件的關鍵字時，提供者才會寫入事件。</span><span class="sxs-lookup"><span data-stu-id="4c966-262">If the event's keyword meets the <em>MatchAnyKeyword</em> condition, the provider will write the event only if all of the bits in this mask exist in the event's keyword.</span></span> <span data-ttu-id="4c966-263">如果 <em>MatchAnyKeyword</em> 為零，則不會使用這個遮罩。</span><span class="sxs-lookup"><span data-stu-id="4c966-263">This mask is not used if <em>MatchAnyKeyword</em> is zero.</span></span> <span data-ttu-id="4c966-264">如需範例，請參閱 <a href="/windows/win32/api/evntrace/nf-evntrace-enabletraceex"><strong>EnableTraceEx</strong></a> 函數的備註一節。</span><span class="sxs-lookup"><span data-stu-id="4c966-264">For an example, see the Remarks section of the <a href="/windows/win32/api/evntrace/nf-evntrace-enabletraceex"><strong>EnableTraceEx</strong></a> function.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="4c966-265">在修改登錄之後，下次電腦重新開機時，就會啟動重新開機記錄器會話。</span><span class="sxs-lookup"><span data-stu-id="4c966-265">After the registry has been modified, the AutoLogger session is started the next time the computer is restarted.</span></span> <span data-ttu-id="4c966-266">自動記錄器會話會呼叫 [**EnableTraceEx**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex) 函式來啟用提供者。</span><span class="sxs-lookup"><span data-stu-id="4c966-266">The AutoLogger session calls the [**EnableTraceEx**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex) function to enable the providers.</span></span>

<span data-ttu-id="4c966-267">自動記錄器會話會增加系統開機時間，並應謹慎使用。</span><span class="sxs-lookup"><span data-stu-id="4c966-267">The AutoLogger sessions increase the system boot time and should be used sparingly.</span></span> <span data-ttu-id="4c966-268">想要在開機過程中捕獲資訊的服務，應該考慮將控制器邏輯新增到本身，而不是使用自動記錄器會話。</span><span class="sxs-lookup"><span data-stu-id="4c966-268">Services that want to capture information during the boot process should consider adding controller logic to itself instead of using the AutoLogger session.</span></span>

<span data-ttu-id="4c966-269">若要停止自動記錄器會話，請呼叫 [**ControlTrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea) 函數。</span><span class="sxs-lookup"><span data-stu-id="4c966-269">To stop an AutoLogger session, call the [**ControlTrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea) function.</span></span> <span data-ttu-id="4c966-270">您傳遞給函式的會話名稱就是您在登錄中用來定義會話的登錄機碼名稱。</span><span class="sxs-lookup"><span data-stu-id="4c966-270">The session name that you pass to the function is the name of the registry key that you used to define the session in the registry.</span></span>

<span data-ttu-id="4c966-271">在 Windows 8.1、Windows Server 2012 R2 和更新版本上， [**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2) 函式可以使用事件承載、範圍和堆疊逐步篩選，以及 [**啟用 \_ 追蹤 \_ 參數**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters) 和 [**事件 \_ 篩選 \_ 描述**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor) 項結構，以篩選記錄器會話中的特定條件。</span><span class="sxs-lookup"><span data-stu-id="4c966-271">On Windows 8.1,Windows Server 2012 R2, and later, event payload , scope, and stack walk filters can be used by the [**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2) function and the [**ENABLE\_TRACE\_PARAMETERS**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters) and [**EVENT\_FILTER\_DESCRIPTOR**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor) structures to filter on specific conditions in a logger session.</span></span> <span data-ttu-id="4c966-272">如需事件裝載篩選準則的詳細資訊，請參閱 [**TdhCreatePayloadFilter**](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter)和 [**TdhAggregatePayloadFilters**](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters) 函式以及 **啟用 \_ 追蹤 \_ 參數**、 **事件 \_ 篩選器 \_ 描述** 元和承載 [**\_ 篩選 \_**](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate) 述詞結構。</span><span class="sxs-lookup"><span data-stu-id="4c966-272">For more information on event payload filters, see the [**TdhCreatePayloadFilter**](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter), and [**TdhAggregatePayloadFilters**](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters) functions and the **ENABLE\_TRACE\_PARAMETERS**, **EVENT\_FILTER\_DESCRIPTOR**, and [**PAYLOAD\_FILTER\_PREDICATE**](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate) structures.</span></span>

<span data-ttu-id="4c966-273">如需啟動事件追蹤會話的詳細資訊，請參閱設定 [和啟動事件追蹤會話](configuring-and-starting-an-event-tracing-session.md)。</span><span class="sxs-lookup"><span data-stu-id="4c966-273">For details on starting an event tracing session, see [Configuring and Starting an Event Tracing Session](configuring-and-starting-an-event-tracing-session.md).</span></span>

<span data-ttu-id="4c966-274">如需啟動私用記錄器會話的詳細資訊，請參閱設定 [和啟動私用記錄器會話](configuring-and-starting-a-private-logger-session.md)。</span><span class="sxs-lookup"><span data-stu-id="4c966-274">For details on starting a private logger session, see [Configuring and Starting a Private Logger Session](configuring-and-starting-a-private-logger-session.md).</span></span>

<span data-ttu-id="4c966-275">如需啟動 NT Kernel 記錄器會話的詳細資訊，請參閱設定 [和啟動 Nt Kernel 記錄器會話](configuring-and-starting-the-nt-kernel-logger-session.md)。</span><span class="sxs-lookup"><span data-stu-id="4c966-275">For details on starting an NT Kernel Logger session, see [Configuring and Starting the NT Kernel Logger Session](configuring-and-starting-the-nt-kernel-logger-session.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4c966-276">相關主題</span><span class="sxs-lookup"><span data-stu-id="4c966-276">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4c966-277">設定和啟動私用記錄器會話</span><span class="sxs-lookup"><span data-stu-id="4c966-277">Configuring and Starting a Private Logger Session</span></span>](configuring-and-starting-a-private-logger-session.md)
</dt> <dt>

[<span data-ttu-id="4c966-278">設定並啟動 SystemTraceProvider 會話</span><span class="sxs-lookup"><span data-stu-id="4c966-278">Configuring and Starting a SystemTraceProvider Session</span></span>](configuring-and-starting-a-systemtraceprovider-session.md)
</dt> <dt>

[<span data-ttu-id="4c966-279">設定和啟動事件追蹤會話</span><span class="sxs-lookup"><span data-stu-id="4c966-279">Configuring and Starting an Event Tracing Session</span></span>](configuring-and-starting-an-event-tracing-session.md)
</dt> <dt>

[<span data-ttu-id="4c966-280">設定和啟動 NT Kernel 記錄器會話</span><span class="sxs-lookup"><span data-stu-id="4c966-280">Configuring and Starting the NT Kernel Logger Session</span></span>](configuring-and-starting-the-nt-kernel-logger-session.md)
</dt> <dt>

[<span data-ttu-id="4c966-281">**EnableTraceEx2**</span><span class="sxs-lookup"><span data-stu-id="4c966-281">**EnableTraceEx2**</span></span>](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2)
</dt> <dt>

[<span data-ttu-id="4c966-282">**啟用 \_ 追蹤 \_ 參數**</span><span class="sxs-lookup"><span data-stu-id="4c966-282">**ENABLE\_TRACE\_PARAMETERS**</span></span>](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters)
</dt> <dt>

[<span data-ttu-id="4c966-283">**事件 \_ 篩選器 \_ 描述項**</span><span class="sxs-lookup"><span data-stu-id="4c966-283">**EVENT\_FILTER\_DESCRIPTOR**</span></span>](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor)
</dt> <dt>

[<span data-ttu-id="4c966-284">**裝載 \_ 篩選述詞 \_**</span><span class="sxs-lookup"><span data-stu-id="4c966-284">**PAYLOAD\_FILTER\_PREDICATE**</span></span>](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate)
</dt> <dt>

[<span data-ttu-id="4c966-285">**TdhAggregatePayloadFilters**</span><span class="sxs-lookup"><span data-stu-id="4c966-285">**TdhAggregatePayloadFilters**</span></span>](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters)
</dt> <dt>

[<span data-ttu-id="4c966-286">**TdhCreatePayloadFilter**</span><span class="sxs-lookup"><span data-stu-id="4c966-286">**TdhCreatePayloadFilter**</span></span>](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter)
</dt> <dt>

[<span data-ttu-id="4c966-287">更新事件追蹤會話</span><span class="sxs-lookup"><span data-stu-id="4c966-287">Updating an Event Tracing Session</span></span>](updating-an-event-tracing-session.md)
</dt> </dl>
