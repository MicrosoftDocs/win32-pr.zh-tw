---
description: Microsoft Windows HTTP Services (WinHTTP) 追蹤設定工具（WinHttpTraceCfg.exe）是用來設定偵錯工具和封包探查用途的追蹤功能。
ms.assetid: 744cae92-9c64-459e-96eb-eb609e62183c
title: WinHttpTraceCfg.exe，追蹤設定工具
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6c6423c581a51f0cf6b55856f2e8cd0ea670515
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973277"
---
# <a name="winhttptracecfgexe-a-trace-configuration-tool"></a><span data-ttu-id="0f3c5-103">WinHttpTraceCfg.exe，追蹤設定工具</span><span class="sxs-lookup"><span data-stu-id="0f3c5-103">WinHttpTraceCfg.exe, a Trace Configuration Tool</span></span>

<span data-ttu-id="0f3c5-104">[Microsoft WINDOWS HTTP Services (WinHTTP) ](about-winhttp.md)追蹤設定工具（WinHttpTraceCfg.exe）是用來設定偵錯工具和封包探查用途的追蹤功能。</span><span class="sxs-lookup"><span data-stu-id="0f3c5-104">The [Microsoft Windows HTTP Services (WinHTTP)](about-winhttp.md) trace configuration tool, WinHttpTraceCfg.exe, is used to configure trace capabilities for debugging and packet-sniffing purposes.</span></span> <span data-ttu-id="0f3c5-105">監視 WinHTTP 函式和其對應網路流量的能力很重要。</span><span class="sxs-lookup"><span data-stu-id="0f3c5-105">The ability to monitor WinHTTP functions and their corresponding network traffic is important.</span></span> <span data-ttu-id="0f3c5-106">將使用加密網路通訊協定的應用程式（例如安全通訊端層 (SSL) ）偵測到網路傳輸層上的探查封包，並在用戶端與伺服器解密之後，需要能夠攔截流量。</span><span class="sxs-lookup"><span data-stu-id="0f3c5-106">Debugging applications that utilize encrypted wire protocols, such as Secure Sockets Layer (SSL), preclude sniffing packets at the network transport layer and require the ability to intercept traffic between the client and server after it has been decrypted.</span></span> <span data-ttu-id="0f3c5-107">Microsoft Windows HTTP Services (WinHTTP) 提供的追蹤設備，有一系列的功能可攔截用戶端與伺服器之間的流量串流。</span><span class="sxs-lookup"><span data-stu-id="0f3c5-107">Microsoft Windows HTTP Services (WinHTTP) provides a trace facility that has a range of capabilities for intercepting the traffic stream between the client and server.</span></span>

<span data-ttu-id="0f3c5-108">此追蹤工具可以是很重要的偵錯工具。</span><span class="sxs-lookup"><span data-stu-id="0f3c5-108">This trace facility can be a valuable tool for debugging.</span></span> <span data-ttu-id="0f3c5-109">例如，您可以使用它來查看傳遞給各種函式呼叫的參數，以及查看 WinHTTP 應用程式傳送和接收的實際資料。</span><span class="sxs-lookup"><span data-stu-id="0f3c5-109">It can be used, for example, to view parameters passed to various function calls, as well as to view actual data sent and received by a WinHTTP application.</span></span>

-   [<span data-ttu-id="0f3c5-110">使用追蹤設備</span><span class="sxs-lookup"><span data-stu-id="0f3c5-110">Using the Trace Facility</span></span>](#using-the-trace-facility)
-   [<span data-ttu-id="0f3c5-111">解讀追蹤資料</span><span class="sxs-lookup"><span data-stu-id="0f3c5-111">Interpreting Trace Data</span></span>](#interpreting-trace-data)

## <a name="using-the-trace-facility"></a><span data-ttu-id="0f3c5-112">使用追蹤設備</span><span class="sxs-lookup"><span data-stu-id="0f3c5-112">Using the Trace Facility</span></span>

<span data-ttu-id="0f3c5-113">WinHTTP 從登錄取得追蹤控制參數。</span><span class="sxs-lookup"><span data-stu-id="0f3c5-113">WinHTTP obtains tracing control parameters from the registry.</span></span> <span data-ttu-id="0f3c5-114">這些控制項參數會影響 WinHTTP 產生追蹤輸出的方式，以及該輸出的格式化方式。</span><span class="sxs-lookup"><span data-stu-id="0f3c5-114">These control parameters affect how WinHTTP produces trace output, and how that output is formatted.</span></span> <span data-ttu-id="0f3c5-115">使用 WinHTTP 的所有應用程式都會共用相同的設定。</span><span class="sxs-lookup"><span data-stu-id="0f3c5-115">All applications that use WinHTTP share the same settings.</span></span>

<span data-ttu-id="0f3c5-116">您可以從 [Windows Server 2003 資源套件工具](https://www.microsoft.com/downloads/details.aspx?familyid=9d467a69-57ff-4ae7-96ee-b18c4790cffd) 網站下載追蹤設備設定工具（WinHttpTraceCfg.exe）。</span><span class="sxs-lookup"><span data-stu-id="0f3c5-116">A trace facility configuration tool, WinHttpTraceCfg.exe, is available as a download on the [Windows Server 2003 Resource Kit Tools](https://www.microsoft.com/downloads/details.aspx?familyid=9d467a69-57ff-4ae7-96ee-b18c4790cffd) website.</span></span> <span data-ttu-id="0f3c5-117">Configuration tool 會根據指定的命令列參數，設定或抓取追蹤設備登錄設定。</span><span class="sxs-lookup"><span data-stu-id="0f3c5-117">The configuration tool sets or retrieves the trace facility registry settings based on the specified command line parameters.</span></span>

``` syntax
WinHttpTraceCfg [-e <0|1>] [-l [log-file]] [-d <0|1>] [-s <0|1|2>] 
                [-t <0|1>] [-?] [-m <file size>]
```

<span data-ttu-id="0f3c5-118">下表列出設定工具的可能參數。</span><span class="sxs-lookup"><span data-stu-id="0f3c5-118">The following table lists possible parameters for the configuration tool.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0f3c5-119">參數</span><span class="sxs-lookup"><span data-stu-id="0f3c5-119">Parameter</span></span></th>
<th><span data-ttu-id="0f3c5-120">Description</span><span class="sxs-lookup"><span data-stu-id="0f3c5-120">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0f3c5-121">-?</span><span class="sxs-lookup"><span data-stu-id="0f3c5-121">-?</span></span></td>
<td><span data-ttu-id="0f3c5-122">顯示語法資料。</span><span class="sxs-lookup"><span data-stu-id="0f3c5-122">Displays syntax data.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0f3c5-123">-E</span><span class="sxs-lookup"><span data-stu-id="0f3c5-123">-e</span></span></td>
<td><span data-ttu-id="0f3c5-124">指定是否啟用或停用追蹤工具。</span><span class="sxs-lookup"><span data-stu-id="0f3c5-124">Specifies whether the trace facility is enabled or disabled.</span></span> <br/> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0f3c5-125">0</span><span class="sxs-lookup"><span data-stu-id="0f3c5-125">0</span></span></td>
<td><span data-ttu-id="0f3c5-126">預設值，</span><span class="sxs-lookup"><span data-stu-id="0f3c5-126">Default setting.</span></span> <span data-ttu-id="0f3c5-127">停用追蹤。</span><span class="sxs-lookup"><span data-stu-id="0f3c5-127">Disables tracing.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0f3c5-128">1</span><span class="sxs-lookup"><span data-stu-id="0f3c5-128">1</span></span></td>
<td><span data-ttu-id="0f3c5-129">啟用追蹤。</span><span class="sxs-lookup"><span data-stu-id="0f3c5-129">Enables tracing.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0f3c5-130">-l</span><span class="sxs-lookup"><span data-stu-id="0f3c5-130">-l</span></span></td>
<td><p><span data-ttu-id="0f3c5-131">指定記錄檔的前置詞。</span><span class="sxs-lookup"><span data-stu-id="0f3c5-131">Specifies a prefix for the log file.</span></span> <span data-ttu-id="0f3c5-132">前置詞可以包含路徑。</span><span class="sxs-lookup"><span data-stu-id="0f3c5-132">The prefix can include a path.</span></span> <span data-ttu-id="0f3c5-133">記錄檔會寫入至目前的目錄或前置詞中指定的目錄，並具有下列格式。</span><span class="sxs-lookup"><span data-stu-id="0f3c5-133">The log file is written to the current directory or the directory specified in the prefix and has the following format.</span></span></p>
<p><span data-ttu-id="0f3c5-134"><<em>前置詞</em> > -<<em>應用程式名稱</em> > 。<<em>時間</em> > .log</span><span class="sxs-lookup"><span data-stu-id="0f3c5-134"><<em>prefix</em>>-<<em>application name</em>>.<<em>time</em>>.log</span></span></p>
<p><span data-ttu-id="0f3c5-135">如果未指定前置詞，則會使用空字串。</span><span class="sxs-lookup"><span data-stu-id="0f3c5-135">If a prefix is not specified, an empty string is used.</span></span> <span data-ttu-id="0f3c5-136">指定 &quot; \* &quot; 以刪除現有的前置詞。</span><span class="sxs-lookup"><span data-stu-id="0f3c5-136">Specify &quot;\*&quot; to delete an existing prefix.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0f3c5-137">-d</span><span class="sxs-lookup"><span data-stu-id="0f3c5-137">-d</span></span></td>
<td><p><span data-ttu-id="0f3c5-138">指定追蹤輸出是否顯示在偵錯工具中，或寫入檔案。</span><span class="sxs-lookup"><span data-stu-id="0f3c5-138">Specifies whether the trace output is displayed in a debugger or written to a file.</span></span></p>

<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0f3c5-139">0</span><span class="sxs-lookup"><span data-stu-id="0f3c5-139">0</span></span></td>
<td><span data-ttu-id="0f3c5-140">預設值，</span><span class="sxs-lookup"><span data-stu-id="0f3c5-140">Default setting.</span></span> <span data-ttu-id="0f3c5-141">寫入至記錄檔。</span><span class="sxs-lookup"><span data-stu-id="0f3c5-141">Writes to log file.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0f3c5-142">1</span><span class="sxs-lookup"><span data-stu-id="0f3c5-142">1</span></span></td>
<td><span data-ttu-id="0f3c5-143">在偵錯工具中顯示。</span><span class="sxs-lookup"><span data-stu-id="0f3c5-143">Displays in a debugger.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0f3c5-144">-S</span><span class="sxs-lookup"><span data-stu-id="0f3c5-144">-s</span></span></td>
<td><p><span data-ttu-id="0f3c5-145">指定如何) 顯示網路流量 (要求和回應。</span><span class="sxs-lookup"><span data-stu-id="0f3c5-145">Specifies how network traffic (requests and responses) is displayed.</span></span></p>

<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0f3c5-146">0</span><span class="sxs-lookup"><span data-stu-id="0f3c5-146">0</span></span></td>
<td><span data-ttu-id="0f3c5-147">只顯示 HTTP 標頭。</span><span class="sxs-lookup"><span data-stu-id="0f3c5-147">Only displays HTTP headers.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0f3c5-148">1</span><span class="sxs-lookup"><span data-stu-id="0f3c5-148">1</span></span></td>
<td><span data-ttu-id="0f3c5-149">預設值，</span><span class="sxs-lookup"><span data-stu-id="0f3c5-149">Default setting.</span></span> <span data-ttu-id="0f3c5-150">顯示美國國家標準局 (ANSI) 格式的網路流量。</span><span class="sxs-lookup"><span data-stu-id="0f3c5-150">Shows network traffic in American National Standards Institute (ANSI) format.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0f3c5-151">2</span><span class="sxs-lookup"><span data-stu-id="0f3c5-151">2</span></span></td>
<td><span data-ttu-id="0f3c5-152">以十六進位格式顯示網路流量。</span><span class="sxs-lookup"><span data-stu-id="0f3c5-152">Shows network traffic in hexadecimal format.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0f3c5-153">-t</span><span class="sxs-lookup"><span data-stu-id="0f3c5-153">-t</span></span></td>
<td><p><span data-ttu-id="0f3c5-154">指定追蹤中是否記錄最上層函式呼叫。</span><span class="sxs-lookup"><span data-stu-id="0f3c5-154">Specifies whether top-level function calls are recorded in the trace.</span></span></p>

<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0f3c5-155">0</span><span class="sxs-lookup"><span data-stu-id="0f3c5-155">0</span></span></td>
<td><span data-ttu-id="0f3c5-156">預設值，</span><span class="sxs-lookup"><span data-stu-id="0f3c5-156">Default setting.</span></span> <span data-ttu-id="0f3c5-157">不會記錄函式呼叫。</span><span class="sxs-lookup"><span data-stu-id="0f3c5-157">Function calls are not recorded.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0f3c5-158">1</span><span class="sxs-lookup"><span data-stu-id="0f3c5-158">1</span></span></td>
<td><span data-ttu-id="0f3c5-159">最上層函式呼叫會被記錄下來。</span><span class="sxs-lookup"><span data-stu-id="0f3c5-159">Top-level function calls are recorded.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0f3c5-160">-M</span><span class="sxs-lookup"><span data-stu-id="0f3c5-160">-m</span></span></td>
<td><p><span data-ttu-id="0f3c5-161">指定追蹤設備所產生之記錄檔的大小上限（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="0f3c5-161">Specifies the maximum size, in bytes, of a log file generated by the tracing facility.</span></span> <span data-ttu-id="0f3c5-162">如果指定這個選項但未指定大小，則最小值為65535個位元組。</span><span class="sxs-lookup"><span data-stu-id="0f3c5-162">If this option is specified without a size, the minimum value is 65,535 bytes.</span></span> <span data-ttu-id="0f3c5-163">如果記錄檔達到大小上限，則會清除檔案的內容。</span><span class="sxs-lookup"><span data-stu-id="0f3c5-163">If a log file reaches the maximum size, the contents of the file are erased.</span></span> <span data-ttu-id="0f3c5-164">追蹤資料會繼續寫入至記錄檔。</span><span class="sxs-lookup"><span data-stu-id="0f3c5-164">Trace data continues to be written to the log file.</span></span></p></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="0f3c5-165">執行追蹤設備設定工具並不指定參數，會抓取並顯示目前的登錄設定。</span><span class="sxs-lookup"><span data-stu-id="0f3c5-165">Running the trace facility configuration tool and specifying no parameters retrieves and displays the current registry settings.</span></span>

> [!Note]  
> <span data-ttu-id="0f3c5-166">記錄檔會快速成長並降低應用程式效能。</span><span class="sxs-lookup"><span data-stu-id="0f3c5-166">Log files grow rapidly and degrade application performance.</span></span> <span data-ttu-id="0f3c5-167">啟用追蹤設備之前，請確定所需的硬碟空間可用。</span><span class="sxs-lookup"><span data-stu-id="0f3c5-167">Ensure that the required hard disk drive space is available before enabling the trace facility.</span></span>

 

## <a name="interpreting-trace-data"></a><span data-ttu-id="0f3c5-168">解讀追蹤資料</span><span class="sxs-lookup"><span data-stu-id="0f3c5-168">Interpreting Trace Data</span></span>

<span data-ttu-id="0f3c5-169">追蹤設備資料流程會反映在應用程式中呼叫的 WinHTTP 函式，以及任何傳送或接收的 HTTP 資料。</span><span class="sxs-lookup"><span data-stu-id="0f3c5-169">The trace facility data stream reflects WinHTTP functions called in the application and any HTTP data sent or received.</span></span> <span data-ttu-id="0f3c5-170">在某些情況下，也會顯示 WinHTTP 內部呼叫的函式。</span><span class="sxs-lookup"><span data-stu-id="0f3c5-170">In some cases, functions called internally by WinHTTP are also shown.</span></span>

<span data-ttu-id="0f3c5-171">下圖顯示追蹤設備所產生的記錄檔部分。</span><span class="sxs-lookup"><span data-stu-id="0f3c5-171">The following image shows a portion of a log file generated by the trace facility.</span></span> <span data-ttu-id="0f3c5-172">已反白顯示並標示了數個專案。</span><span class="sxs-lookup"><span data-stu-id="0f3c5-172">Several items are highlighted and labeled.</span></span>

![範例追蹤](images/ss-tracer-wco.png)

<span data-ttu-id="0f3c5-174">追蹤輸出的每一行都包含三個數據行中的資訊。</span><span class="sxs-lookup"><span data-stu-id="0f3c5-174">Each line of trace output contains information in three columns.</span></span> <span data-ttu-id="0f3c5-175">第一個資料行顯示記錄專案的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="0f3c5-175">The first column shows the date and time when the entry was recorded.</span></span> <span data-ttu-id="0f3c5-176">第二個數據行會顯示 (識別碼) 的要求識別碼，可以用來區別多個要求。</span><span class="sxs-lookup"><span data-stu-id="0f3c5-176">The second column shows a request identifier (ID) that can be used to differentiate between multiple requests.</span></span> <span data-ttu-id="0f3c5-177">如果記錄專案未對應至特定的要求， \* \* 則會在此資料行中顯示「會話」。</span><span class="sxs-lookup"><span data-stu-id="0f3c5-177">If the log entry does not correspond to a specific request, "\*Session\*" is displayed in this column.</span></span> <span data-ttu-id="0f3c5-178">根據此識別碼排序記錄檔，以只查看針對單一要求所發生的事件，可能會很有用。</span><span class="sxs-lookup"><span data-stu-id="0f3c5-178">It can be useful to sort the log file based on this ID to see only events that occur for a single request.</span></span> <span data-ttu-id="0f3c5-179">下列範例顯示您可以用來排序記錄檔的命令。</span><span class="sxs-lookup"><span data-stu-id="0f3c5-179">The following example shows a command you can use to sort the log file.</span></span>

<span data-ttu-id="0f3c5-180">**findstr 00000001 LogFile 記錄檔**</span><span class="sxs-lookup"><span data-stu-id="0f3c5-180">**findstr 00000001 LogFile.log**</span></span>

<span data-ttu-id="0f3c5-181">第三個數據行會顯示函式呼叫、HTTP 流量或包含的狀態訊息，以協助解讀追蹤。</span><span class="sxs-lookup"><span data-stu-id="0f3c5-181">The third column shows a function call, HTTP traffic, or a status message included to help interpret the trace.</span></span>

<span data-ttu-id="0f3c5-182">當記錄專案對應至函式呼叫時，也會記錄函數的參數。</span><span class="sxs-lookup"><span data-stu-id="0f3c5-182">When a log entry corresponds to a function call, the parameters of the function are also recorded.</span></span> <span data-ttu-id="0f3c5-183">記憶體位址會以十六進位顯示，其他所有值則顯示為 ASCII 字串。</span><span class="sxs-lookup"><span data-stu-id="0f3c5-183">Memory addresses are displayed in hexadecimal while all other values are displayed as an ASCII string.</span></span> <span data-ttu-id="0f3c5-184">追蹤設備也會記錄每個函數的傳回時間和值。</span><span class="sxs-lookup"><span data-stu-id="0f3c5-184">The trace facility also records the return time and value for each function.</span></span>

<span data-ttu-id="0f3c5-185">HTTP 資料的格式取決於使用追蹤設備設定工具指定的登錄設定。</span><span class="sxs-lookup"><span data-stu-id="0f3c5-185">The format of HTTP data depends on the registry settings specified with the trace facility configuration tool.</span></span> <span data-ttu-id="0f3c5-186">加密 HTTP 資料時，解密的資料也會顯示在追蹤輸出中。</span><span class="sxs-lookup"><span data-stu-id="0f3c5-186">When HTTP data is encrypted, the decrypted data is also shown in the trace output.</span></span>

 

 




