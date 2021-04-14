---
title: 追蹤
description: 追蹤會使用 Windows 事件追蹤 (ETW) 。
ms.assetid: b008bae2-9423-4e72-ae03-9cd50f73d812
keywords:
- 適用于 Windows 的追蹤 Web 服務
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82c660884667cefae8067376075a30cbc41f70d4
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "104383306"
---
# <a name="tracing"></a><span data-ttu-id="82b37-106">追蹤</span><span class="sxs-lookup"><span data-stu-id="82b37-106">Tracing</span></span>

<span data-ttu-id="82b37-107">追蹤會使用 Windows 事件追蹤 (ETW) 。</span><span class="sxs-lookup"><span data-stu-id="82b37-107">Tracing uses Event Tracing for Windows (ETW).</span></span> <span data-ttu-id="82b37-108">若要利用 Windows Server 2008 R2 提供的追蹤工具，請從 [MSDN 下載](https://www.microsoft.com/download/details.aspx?id=8279) 網站安裝 Microsoft Windows SDK。</span><span class="sxs-lookup"><span data-stu-id="82b37-108">To take advantage of the tracing tools available with Windows Server 2008 R2, install the Microsoft Windows SDK from the [MSDN Downloads](https://www.microsoft.com/download/details.aspx?id=8279) site.</span></span>


<span data-ttu-id="82b37-109">支援的追蹤層級有三種：</span><span class="sxs-lookup"><span data-stu-id="82b37-109">There are three tracing levels supported:</span></span>

-   <span data-ttu-id="82b37-110">詳細資訊 (所有可用的追蹤) 。</span><span class="sxs-lookup"><span data-stu-id="82b37-110">Verbose (all available traces).</span></span>
-   <span data-ttu-id="82b37-111">資訊 (資訊追蹤) 。</span><span class="sxs-lookup"><span data-stu-id="82b37-111">Info (informational traces).</span></span>
-   <span data-ttu-id="82b37-112">錯誤追蹤)  (錯誤。</span><span class="sxs-lookup"><span data-stu-id="82b37-112">Error (error traces).</span></span>

<span data-ttu-id="82b37-113">追蹤下列事件：</span><span class="sxs-lookup"><span data-stu-id="82b37-113">The following events are traced:</span></span>

-   <span data-ttu-id="82b37-114">任何錯誤 (層級 = 錯誤、層級 = 資訊或層級 = 詳細) 。</span><span class="sxs-lookup"><span data-stu-id="82b37-114">Any errors (Level=Error, Level=Info or Level=Verbose).</span></span>
-   <span data-ttu-id="82b37-115">API 的進入/離開 (Level = Info 或 Level = Verbose) 。</span><span class="sxs-lookup"><span data-stu-id="82b37-115">Entry/Exit of an API (Level=Info or Level=Verbose).</span></span>
-   <span data-ttu-id="82b37-116">開始及完成任何 IO (Level = Info 或 Level = Verbose) </span><span class="sxs-lookup"><span data-stu-id="82b37-116">Start and completion of any IO (Level=Info or Level=Verbose)</span></span>
-   <span data-ttu-id="82b37-117">交換的 SOAP 訊息 (Level = Verbose，可在 Windows 2003 SP1 和更新版本上使用) </span><span class="sxs-lookup"><span data-stu-id="82b37-117">Exchanged SOAP messages (Level=Verbose, available on Windows 2003 SP1 and later)</span></span>

## <a name="generating-and-viewing-wwsapi-traces"></a><span data-ttu-id="82b37-118">產生和查看 WWSAPI 追蹤</span><span class="sxs-lookup"><span data-stu-id="82b37-118">Generating and Viewing WWSAPI Traces</span></span>

<span data-ttu-id="82b37-119">WWSAPI 會使用 Windows Vista 和更新版本上以資訊清單為基礎的事件。</span><span class="sxs-lookup"><span data-stu-id="82b37-119">WWSAPI uses the manifest based events on Windows Vista and above.</span></span> <span data-ttu-id="82b37-120">因此，追蹤體驗會根據作業系統版本而有所差異。</span><span class="sxs-lookup"><span data-stu-id="82b37-120">As a result, the tracing experience has some differences based on the operating system version.</span></span> <span data-ttu-id="82b37-121">您可以在所有支援的平臺上使用內建的 ETW 工具來產生 ETW 追蹤。</span><span class="sxs-lookup"><span data-stu-id="82b37-121">Generating ETW traces can be done by using the in-box ETW tools on all supported platforms.</span></span> <span data-ttu-id="82b37-122">不過，以好用的格式來觀看 ETW 追蹤需要 Windows XP SP2 和 Windows 2003 SP1 上的自訂工具。</span><span class="sxs-lookup"><span data-stu-id="82b37-122">However viewing the ETW traces in a nice format requires custom tools on Windows XP SP2 and Windows 2003 SP1.</span></span> <span data-ttu-id="82b37-123">根據作業系統版本而定，有幾種不同的方式可以收集和查看 WWSAPI ETW 事件追蹤。</span><span class="sxs-lookup"><span data-stu-id="82b37-123">There are few different ways of collecting and viewing WWSAPI ETW event traces depending on the operating system version.</span></span>

## <a name="enabling-and-viewing-wwsapi-traces-in-event-viewer-works-on-windows-vista-and-above"></a><span data-ttu-id="82b37-124">在事件檢視器 (中啟用和觀看 WWSAPI 追蹤適用于 Windows Vista 和更新版本) </span><span class="sxs-lookup"><span data-stu-id="82b37-124">Enabling and Viewing WWSAPI traces in Event Viewer (works on Windows Vista and above)</span></span>

-   <span data-ttu-id="82b37-125">從命令列或 [執行] 功能表執行 eventvwr.msc。</span><span class="sxs-lookup"><span data-stu-id="82b37-125">Run eventvwr.msc from command line or run menu.</span></span>
-   <span data-ttu-id="82b37-126">在右側的 [動作] 窗格中，按一下 [view] 連結，然後啟用 [顯示分析和調試記錄] 選項。</span><span class="sxs-lookup"><span data-stu-id="82b37-126">Click the view link on the Actions pane on the right and enable Show Analytic and Debug logs option.</span></span>
-   <span data-ttu-id="82b37-127">流覽至左窗格中的 [應用程式及服務記錄檔] \\ Microsoft \\ Windows \\ WebServices 提供者。</span><span class="sxs-lookup"><span data-stu-id="82b37-127">Browse to Application and Service Logs\\Microsoft\\Windows\\WebServices providers on the left pane.</span></span>
-   <span data-ttu-id="82b37-128">以滑鼠右鍵按一下追蹤提供者，然後選取 [啟用記錄]。</span><span class="sxs-lookup"><span data-stu-id="82b37-128">Right click the Tracing provider and select Enable log.</span></span>
-   <span data-ttu-id="82b37-129">執行您的案例。</span><span class="sxs-lookup"><span data-stu-id="82b37-129">Run your scenario.</span></span>
-   <span data-ttu-id="82b37-130">重新整理 [事件檢視器] 頁面時，您應該會開始看到 WWSAPI 追蹤專案。</span><span class="sxs-lookup"><span data-stu-id="82b37-130">When you refresh the event viewer page, you should start seeing the WWSAPI tracing entries.</span></span>

## <a name="enabling-and-viewing-wwsapi-traces-using-wstracebat-script-works-on-xpsp2-and-above"></a><span data-ttu-id="82b37-131">使用 Wstrace.bat 腳本來啟用和觀看 WWSAPI 追蹤 (適用于 XPSP2 和更新版本) </span><span class="sxs-lookup"><span data-stu-id="82b37-131">Enabling and Viewing WWSAPI traces using Wstrace.bat Script (works on XPSP2 and above)</span></span>

<span data-ttu-id="82b37-132">wstrace.bat 批次檔提供便利的方式來執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="82b37-132">The wstrace.bat batch file provides a convenient way to:</span></span>

-   <span data-ttu-id="82b37-133">建立追蹤記錄</span><span class="sxs-lookup"><span data-stu-id="82b37-133">Create a trace log</span></span>
-   <span data-ttu-id="82b37-134">刪除追蹤記錄</span><span class="sxs-lookup"><span data-stu-id="82b37-134">Delete a trace log</span></span>
-   <span data-ttu-id="82b37-135">啟用和停用追蹤</span><span class="sxs-lookup"><span data-stu-id="82b37-135">Enable and disable tracing</span></span>
-   <span data-ttu-id="82b37-136">更新追蹤層級 (info/error/verbose) </span><span class="sxs-lookup"><span data-stu-id="82b37-136">Update the tracing level (info/error/verbose)</span></span>
-   <span data-ttu-id="82b37-137">將追蹤記錄轉換成 CSV 檔案</span><span class="sxs-lookup"><span data-stu-id="82b37-137">Converting trace logs to CSV files</span></span>

<span data-ttu-id="82b37-138">批次檔會針對所有命令使用 logman.exe，但將記錄檔轉換為 CSV 檔案（需要自訂工具 (wstracedump.exe) ）除外。</span><span class="sxs-lookup"><span data-stu-id="82b37-138">The batch file uses logman.exe for all commands, with the exception of converting the logs to CSV file, which requires a custom tool (wstracedump.exe).</span></span>

## <a name="using-tracing-commands"></a><span data-ttu-id="82b37-139">使用追蹤命令</span><span class="sxs-lookup"><span data-stu-id="82b37-139">Using tracing commands</span></span>

<span data-ttu-id="82b37-140">下列命令會建立使用資訊、錯誤或詳細資訊層級的記錄。</span><span class="sxs-lookup"><span data-stu-id="82b37-140">The following command creates a log that uses info, error or verbose level.</span></span> <span data-ttu-id="82b37-141">此命令需要較高的許可權。</span><span class="sxs-lookup"><span data-stu-id="82b37-141">This command requires elevated privileges.</span></span>

<span data-ttu-id="82b37-142">**wstrace.bat 建立 \[ 資訊 \| 錯誤 \| 詳細資訊\]**</span><span class="sxs-lookup"><span data-stu-id="82b37-142">**wstrace.bat create \[info \| error \| verbose\]**</span></span>

<span data-ttu-id="82b37-143">下列命令會刪除記錄檔。</span><span class="sxs-lookup"><span data-stu-id="82b37-143">The following command deletes the log.</span></span> <span data-ttu-id="82b37-144">此命令需要較高的許可權。</span><span class="sxs-lookup"><span data-stu-id="82b37-144">This command requires elevated privileges.</span></span>

<span data-ttu-id="82b37-145">**wstrace.bat 刪除**</span><span class="sxs-lookup"><span data-stu-id="82b37-145">**wstrace.bat delete**</span></span>

<span data-ttu-id="82b37-146">下列命令會啟用追蹤。</span><span class="sxs-lookup"><span data-stu-id="82b37-146">The following command enables tracing.</span></span> <span data-ttu-id="82b37-147">您必須先建立記錄檔。</span><span class="sxs-lookup"><span data-stu-id="82b37-147">You must first create a log.</span></span>

<span data-ttu-id="82b37-148">**wstrace.bat 開啟**</span><span class="sxs-lookup"><span data-stu-id="82b37-148">**wstrace.bat on**</span></span>

<span data-ttu-id="82b37-149">您可以依照下列方式修改 [資訊]、[錯誤] 或 [詳細資訊]) 的追蹤層級 (：</span><span class="sxs-lookup"><span data-stu-id="82b37-149">The tracing level (info, error or verbose) can be modified as follows:</span></span>

<span data-ttu-id="82b37-150">**wstrace.bat 更新 \[ 資訊 \| 錯誤 \| 詳細資訊\]**</span><span class="sxs-lookup"><span data-stu-id="82b37-150">**wstrace.bat update \[info \| error \| verbose\]**</span></span>

<span data-ttu-id="82b37-151">若要傾印追蹤輸出，請使用下列命令：</span><span class="sxs-lookup"><span data-stu-id="82b37-151">To dump the trace output, use the following command:</span></span>

<span data-ttu-id="82b37-152">**wstrace.bat 傾印 > temp.csv**</span><span class="sxs-lookup"><span data-stu-id="82b37-152">**wstrace.bat dump > temp.csv**</span></span>

<span data-ttu-id="82b37-153">事件會傾印至 CSV 檔案，直到按下 Ctrl + C 或停用追蹤為止。</span><span class="sxs-lookup"><span data-stu-id="82b37-153">The events will be dumped to the CSV file until Ctrl-C is pressed or tracing is disabled.</span></span>

## <a name="tracing-file-format"></a><span data-ttu-id="82b37-154">追蹤檔案格式</span><span class="sxs-lookup"><span data-stu-id="82b37-154">Tracing File format</span></span>

<span data-ttu-id="82b37-155">wstrace.bat 所建立的 CSV 檔案是簡單的逗號分隔變數文字檔。</span><span class="sxs-lookup"><span data-stu-id="82b37-155">The CSV files created by wstrace.bat are simple comma-separated-variable text files.</span></span> <span data-ttu-id="82b37-156">這些檔案可能會在 Excel、記事本等中開啟。</span><span class="sxs-lookup"><span data-stu-id="82b37-156">These files may be opened in Excel, Notepad, etc.</span></span>

<span data-ttu-id="82b37-157">檔案的資料行如下所示：</span><span class="sxs-lookup"><span data-stu-id="82b37-157">The columns of the file are as follows:</span></span>

-   <span data-ttu-id="82b37-158">記錄事件時的時間戳記時間戳記</span><span class="sxs-lookup"><span data-stu-id="82b37-158">TimeStamp - Time stamp of when the event was recorded</span></span>
-   <span data-ttu-id="82b37-159">ProcessID-記錄事件之進程的 ULONG 識別碼</span><span class="sxs-lookup"><span data-stu-id="82b37-159">ProcessID - ULONG ID of the process recording the event</span></span>
-   <span data-ttu-id="82b37-160">ThreadID-記錄事件之執行緒的 ULONG 識別碼</span><span class="sxs-lookup"><span data-stu-id="82b37-160">ThreadID - ULONG ID of the thread recording the event</span></span>
-   <span data-ttu-id="82b37-161">事件種類的事件列舉值可能 ( "api enter" \| "api pending" \| "api ExitSyncSuccess" \| "api ExitSyncFailure" \| "api ExitAsyncSuccess" \| "api ExitAsyncFailure" " \| io 已啟動" " \| io 已完成 \| 「io 失敗 \| \| 」「錯誤」「 \| \| \| \| \| 已收到訊息」「已收到訊息」「收到的訊息」「收到的訊息」「收到的訊息」「收到的訊息」「傳送訊息開始」」 ) </span><span class="sxs-lookup"><span data-stu-id="82b37-161">Event - Enumerated value of the event type may be ("api enter" \| "api pending" \| "api ExitSyncSuccess" \| "api ExitSyncFailure" \| "api ExitAsyncSuccess" \| "api ExitAsyncFailure" \| "io started" \| "io completed" \| "io failed" \| "error" \| "received message start" \| "received message" \| "received message stop" \| "sending message start" \| "sending message" \| "sending message stop")</span></span>
-   <span data-ttu-id="82b37-162">Operation-正在叫用的作業名稱。</span><span class="sxs-lookup"><span data-stu-id="82b37-162">Operation - The name of the operation being invoked.</span></span> <span data-ttu-id="82b37-163">這通常會對應至所呼叫的 API。</span><span class="sxs-lookup"><span data-stu-id="82b37-163">Typically this maps to the API being called.</span></span>
-   <span data-ttu-id="82b37-164">錯誤-選擇性的 HRESULT 錯誤號碼</span><span class="sxs-lookup"><span data-stu-id="82b37-164">Error - Optional HRESULT error number</span></span>
-   <span data-ttu-id="82b37-165">資訊-事件的選擇性資訊</span><span class="sxs-lookup"><span data-stu-id="82b37-165">Info - Optional information about the event</span></span>

## <a name="collecting-wwsapi-etw-trace-file-using-etw-tools-works-on-xpsp2-and-above"></a><span data-ttu-id="82b37-166">使用 ETW 工具收集 WWSAPI ETW 追蹤檔案 (可在 XPSP2 和更新版本上運作) </span><span class="sxs-lookup"><span data-stu-id="82b37-166">Collecting WWSAPI ETW Trace File using ETW tools (works on XPSP2 and above)</span></span>

<span data-ttu-id="82b37-167">啟用 WWSAPI 的 ETW 追蹤</span><span class="sxs-lookup"><span data-stu-id="82b37-167">Enabling ETW tracing for WWSAPI</span></span>

<span data-ttu-id="82b37-168">**logman start wstrace-bs 64-ft 1-rt-p Microsoft-Windows-WebServices \[ flags \[ level \] \] \[ -o <EtlLogFileName> \] -ets**</span><span class="sxs-lookup"><span data-stu-id="82b37-168">**logman start wstrace -bs 64 -ft 1 -rt -p Microsoft-Windows-WebServices \[flags \[level\]\] \[-o <EtlLogFileName>\] -ets**</span></span>

<span data-ttu-id="82b37-169">建立並啟動 ETW 追蹤會話。</span><span class="sxs-lookup"><span data-stu-id="82b37-169">to create and start the ETW tracing session.</span></span> <span data-ttu-id="82b37-170">Logman.exe 是可在所有支援的平臺上使用的內建 ETW 工具。</span><span class="sxs-lookup"><span data-stu-id="82b37-170">Logman.exe is an in-box ETW tool available on all supported platforms.</span></span> <span data-ttu-id="82b37-171">請注意，您必須 \_ \_ 在 XPSP2 和 W2K3 上使用 Microsoft Windows WebServices 作為提供者名稱。</span><span class="sxs-lookup"><span data-stu-id="82b37-171">Note that you need to use Microsoft\_Windows\_WebServices as the provider name on XPSP2 and W2K3.</span></span> <span data-ttu-id="82b37-172">您可以執行 logman 查詢提供者，以查看已註冊之提供者的清單。</span><span class="sxs-lookup"><span data-stu-id="82b37-172">You can run logman query providers to see the list of registered providers.</span></span> <span data-ttu-id="82b37-173">除非註冊 microsoft windows WebServices (或 Microsoft \_ windows \_ WebServices) 提供者，否則應予以列出。</span><span class="sxs-lookup"><span data-stu-id="82b37-173">Microsoft-Windows-WebServices (or Microsoft\_Windows\_WebServices) provider should be listed unless it is not registered.</span></span> <span data-ttu-id="82b37-174">提供者通常會在安裝期間註冊。</span><span class="sxs-lookup"><span data-stu-id="82b37-174">The provider is normally registered during setup.</span></span> <span data-ttu-id="82b37-175">不過，您也可以在 <ManifestFileName> Windows Vista 和更新) 版本上執行 wevtutil.exe im (，或 <MofFileName> 在 XPSP2 和 W2K3 (上 mofcomp.exe) ，以手動方式註冊。</span><span class="sxs-lookup"><span data-stu-id="82b37-175">However it can also be manually registered by running wevtutil.exe im <ManifestFileName> (on Windows Vista and Later) or mofcomp.exe <MofFileName> (on XPSP2 and W2K3).</span></span>

<span data-ttu-id="82b37-176">旗標可以用來依類別篩選追蹤。</span><span class="sxs-lookup"><span data-stu-id="82b37-176">Flags can be used to filter the traces by their kind.</span></span> <span data-ttu-id="82b37-177">它可以是或值下列追蹤種類。</span><span class="sxs-lookup"><span data-stu-id="82b37-177">It can be OR'd value of the following trace kinds.</span></span> <span data-ttu-id="82b37-178">如果未提供，則會啟用所有的追蹤類型。</span><span class="sxs-lookup"><span data-stu-id="82b37-178">If not supplied, all trace kinds are enabled.</span></span>

-   <span data-ttu-id="82b37-179">0x1-API 進入/離開追蹤。</span><span class="sxs-lookup"><span data-stu-id="82b37-179">0x1 - API entry/exit traces.</span></span>
-   <span data-ttu-id="82b37-180">0x2-錯誤追蹤。</span><span class="sxs-lookup"><span data-stu-id="82b37-180">0x2 - Error traces.</span></span>
-   <span data-ttu-id="82b37-181">0x4-IO 追蹤。</span><span class="sxs-lookup"><span data-stu-id="82b37-181">0x4 - IO traces.</span></span>
-   <span data-ttu-id="82b37-182">0x8-SOAP 訊息追蹤。</span><span class="sxs-lookup"><span data-stu-id="82b37-182">0x8 - SOAP message traces.</span></span>
-   <span data-ttu-id="82b37-183">0x10-二進位訊息追蹤。</span><span class="sxs-lookup"><span data-stu-id="82b37-183">0x10 - Binary message traces.</span></span>

<span data-ttu-id="82b37-184">層級可以用來依層級篩選追蹤。</span><span class="sxs-lookup"><span data-stu-id="82b37-184">Level can be used to filter the traces by their level.</span></span> <span data-ttu-id="82b37-185">它應該是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="82b37-185">It should be one of the following values.</span></span> <span data-ttu-id="82b37-186">如果未提供，則會啟用所有追蹤層級。</span><span class="sxs-lookup"><span data-stu-id="82b37-186">If not supplied, all trace levels are enabled.</span></span>

-   <span data-ttu-id="82b37-187">0x1-嚴重追蹤。</span><span class="sxs-lookup"><span data-stu-id="82b37-187">0x1 - Fatal traces.</span></span>
-   <span data-ttu-id="82b37-188">0x2-錯誤追蹤。</span><span class="sxs-lookup"><span data-stu-id="82b37-188">0x2 - Error traces.</span></span>
-   <span data-ttu-id="82b37-189">0x3-警告追蹤。</span><span class="sxs-lookup"><span data-stu-id="82b37-189">0x3 - Warning traces.</span></span>
-   <span data-ttu-id="82b37-190">0x4-資訊追蹤。</span><span class="sxs-lookup"><span data-stu-id="82b37-190">0x4 - Informational traces.</span></span>
-   <span data-ttu-id="82b37-191">0x5-詳細追蹤。</span><span class="sxs-lookup"><span data-stu-id="82b37-191">0x5 - Verbose traces.</span></span>

<span data-ttu-id="82b37-192">EtlLogFileName 是要建立之 ETW 事件記錄檔的路徑， (使用 etl 延伸模組) 。</span><span class="sxs-lookup"><span data-stu-id="82b37-192">EtlLogFileName is the path to the ETW event log file to be created (use .etl extension).</span></span> <span data-ttu-id="82b37-193">如果未提供，ETW 將會挑選可以稍後查詢的隨機名稱。</span><span class="sxs-lookup"><span data-stu-id="82b37-193">If not provided, ETW will pick a random name which can be queried later.</span></span> <span data-ttu-id="82b37-194">此檔案不應位於使用者的設定檔目錄中。</span><span class="sxs-lookup"><span data-stu-id="82b37-194">This file should not reside on user's profile directory.</span></span> <span data-ttu-id="82b37-195"> ( etl 檔案) 的 ETW 事件記錄檔是二進位格式。</span><span class="sxs-lookup"><span data-stu-id="82b37-195">ETW event log file (.etl file) is in binary format.</span></span> <span data-ttu-id="82b37-196">它可由 ETW 應用程式取用，但不是人類看得懂的格式。</span><span class="sxs-lookup"><span data-stu-id="82b37-196">It can be consumed by ETW applications, but it is not in human readable format.</span></span> <span data-ttu-id="82b37-197">下一步說明如何查看其內容。</span><span class="sxs-lookup"><span data-stu-id="82b37-197">Next step describes how to view its content.</span></span>

<span data-ttu-id="82b37-198">執行您的案例</span><span class="sxs-lookup"><span data-stu-id="82b37-198">Run your scenario</span></span>

<span data-ttu-id="82b37-199">正在收集 ETW 事件記錄檔。</span><span class="sxs-lookup"><span data-stu-id="82b37-199">Collecting ETW event log file.</span></span>

<span data-ttu-id="82b37-200">**logman stop wstrace-ets**</span><span class="sxs-lookup"><span data-stu-id="82b37-200">**logman stop wstrace -ets**</span></span>

<span data-ttu-id="82b37-201">停止 ETW 追蹤會話。</span><span class="sxs-lookup"><span data-stu-id="82b37-201">to stop the ETW tracing session.</span></span> <span data-ttu-id="82b37-202">這是 ETW 停止記錄事件的時間。</span><span class="sxs-lookup"><span data-stu-id="82b37-202">This is when ETW stops logging the events.</span></span> <span data-ttu-id="82b37-203">在 EtlLogFileName 參數中指定的 ETW 事件記錄檔 () 已準備好可供使用。</span><span class="sxs-lookup"><span data-stu-id="82b37-203">ETW event log file (specified in EtlLogFileName parameter) is ready to consume.</span></span> <span data-ttu-id="82b37-204">您可以在本機觀看 (指示) 或傳送至產品群組以進行調查。</span><span class="sxs-lookup"><span data-stu-id="82b37-204">It can either be viewed locally (instructions are given below) or sent to the product group for investigation.</span></span>

<span data-ttu-id="82b37-205">使用 ETW 工具的端對端範例：</span><span class="sxs-lookup"><span data-stu-id="82b37-205">End to end example using ETW tools:</span></span>

<span data-ttu-id="82b37-206">**logman start wstrace-bs 64-ft 1-rt-p Microsoft-Windows-WebServices-o mytrace .etl-ets**</span><span class="sxs-lookup"><span data-stu-id="82b37-206">**logman start wstrace -bs 64 -ft 1 -rt -p Microsoft-Windows-WebServices -o mytrace.etl -ets**</span></span>

<span data-ttu-id="82b37-207">**回波。。執行您的案例。**</span><span class="sxs-lookup"><span data-stu-id="82b37-207">**echo .. run your scenario..**</span></span>

<span data-ttu-id="82b37-208">**logman stop wstrace-ets**</span><span class="sxs-lookup"><span data-stu-id="82b37-208">**logman stop wstrace -ets**</span></span>

<span data-ttu-id="82b37-209">**tracerpt mytrace .etl-o mytrace.xml**</span><span class="sxs-lookup"><span data-stu-id="82b37-209">**tracerpt mytrace.etl -o mytrace.xml**</span></span>

<span data-ttu-id="82b37-210">**wstrace.htm**</span><span class="sxs-lookup"><span data-stu-id="82b37-210">**wstrace.htm**</span></span>

<span data-ttu-id="82b37-211">**回波。。在開啟的頁面中使用 mytrace.xml 和 wstrace。**</span><span class="sxs-lookup"><span data-stu-id="82b37-211">**echo .. use mytrace.xml and wstrace.xsl in the opened page ..**</span></span>

## <a name="viewing-wwsapi-etw-trace-file-traces-using-wstracedumpexe-tool-works-on-windows-xp-and-above"></a><span data-ttu-id="82b37-212">使用 wstracedump.exe tool (來觀看 WWSAPI ETW 追蹤檔案追蹤適用于 Windows XP 及更新版本) </span><span class="sxs-lookup"><span data-stu-id="82b37-212">Viewing WWSAPI ETW Trace File traces using wstracedump.exe tool (works on Windows XP and above)</span></span>

<span data-ttu-id="82b37-213">Wstracedump.exe 是自訂開發的 ETW 取用者工具，可處理 WWSAPI ETW 追蹤檔中的事件，並產生人類看得懂的輸出。</span><span class="sxs-lookup"><span data-stu-id="82b37-213">Wstracedump.exe is a custom developed ETW consumer tool which processes events in the WWSAPI ETW trace file and produces human readable output.</span></span> <span data-ttu-id="82b37-214">它可以從所有支援的平臺產生輸出。</span><span class="sxs-lookup"><span data-stu-id="82b37-214">It can produce output from all supported platforms.</span></span> <span data-ttu-id="82b37-215">如需詳細資訊，請參閱其使用方式 (wstracedump.exe-？ ) 。</span><span class="sxs-lookup"><span data-stu-id="82b37-215">See its usage (wstracedump.exe -?) for more information.</span></span>

## <a name="viewing-wwsapi-etw-trace-file-traces-using-etw-tools-works-on-windows-vista-and-above"></a><span data-ttu-id="82b37-216">使用 ETW 工具來觀看 WWSAPI ETW 追蹤檔案追蹤 (適用于 Windows Vista 和更新版本) </span><span class="sxs-lookup"><span data-stu-id="82b37-216">Viewing WWSAPI ETW Trace File traces using ETW tools (works on Windows Vista and above)</span></span>

<span data-ttu-id="82b37-217">Tracerpt.exe 是用來查看 ETW 事件記錄檔內容的工具，並可在所有支援的平臺上使用。</span><span class="sxs-lookup"><span data-stu-id="82b37-217">Tracerpt.exe is the tool to view the content of an ETW event log file and available on all supported platforms.</span></span> <span data-ttu-id="82b37-218">可以用來從 ETW 事件記錄檔產生 CSV、.EVTX 或 XML 傾印檔案。</span><span class="sxs-lookup"><span data-stu-id="82b37-218">It can be used to generate CSV, EVTX or XML dump files from an ETW event log file.</span></span> <span data-ttu-id="82b37-219">不過，產生的輸出檔只會在 Windows Vista 和更新版本上擁有人類可讀取的追蹤。</span><span class="sxs-lookup"><span data-stu-id="82b37-219">However the generated output file has human readable traces only on Windows Vista and later.</span></span> <span data-ttu-id="82b37-220">這些指示說明如何產生 XML 傾印檔案，並將它與 xsl 檔案一起使用，以美觀的格式顯示追蹤 (xsl 檔案非常簡單，而且如果需要) 不同的格式，則可能會改變。</span><span class="sxs-lookup"><span data-stu-id="82b37-220">These instructions describes how to generate the XML dump file and use it along with an xsl file to display the traces in a nice format (xsl file is very trivial and may be altered if different formats are desired).</span></span>

-   <span data-ttu-id="82b37-221">執行</span><span class="sxs-lookup"><span data-stu-id="82b37-221">Run</span></span>

    <span data-ttu-id="82b37-222">**tracerpt <EtlLogFileName> -o <OutputXMLFileName>**</span><span class="sxs-lookup"><span data-stu-id="82b37-222">**tracerpt <EtlLogFileName> -o <OutputXMLFileName>**</span></span>

    <span data-ttu-id="82b37-223">若要從二進位 ETL 檔案建立 XML 傾印 (tracerpt.exe 預設會建立 XML 格式的輸出檔。</span><span class="sxs-lookup"><span data-stu-id="82b37-223">to create an XML dump from the binary ETL file (tracerpt.exe creates the output file in XML format by default.</span></span> <span data-ttu-id="82b37-224">執行 tracerpt-？</span><span class="sxs-lookup"><span data-stu-id="82b37-224">Run tracerpt -?</span></span> <span data-ttu-id="82b37-225">可) 查看其他可用的格式。</span><span class="sxs-lookup"><span data-stu-id="82b37-225">To see other available formats).</span></span>

-   <span data-ttu-id="82b37-226">此時，您可以在 XML 檔案中看到追蹤資訊。</span><span class="sxs-lookup"><span data-stu-id="82b37-226">At this point, you can see the tracing information in the XML file.</span></span> <span data-ttu-id="82b37-227">此外，您還可以開啟 wstrace.htm 檔案，並使用 xml 傾印檔案和 wstrace xsl 檔案，以更好格式查看追蹤。</span><span class="sxs-lookup"><span data-stu-id="82b37-227">Additionally, you can open the wstrace.htm file and use the xml dump file and the wstrace.xsl file to see the traces in a nicer format.</span></span> <span data-ttu-id="82b37-228">請注意，檔案必須位於本機電腦上，才能在 IE 上使用此 html 檔案。</span><span class="sxs-lookup"><span data-stu-id="82b37-228">Note that the files need to be on the local machine to be able to use this html file on IE.</span></span>

## <a name="security"></a><span data-ttu-id="82b37-229">安全性</span><span class="sxs-lookup"><span data-stu-id="82b37-229">Security</span></span>

<span data-ttu-id="82b37-230">啟用追蹤時，系統管理員應該考慮它是否耗用額外的磁碟空間和計算能力。</span><span class="sxs-lookup"><span data-stu-id="82b37-230">When enabling tracing, administrators should take into account that it consumes additional disk space and computation power.</span></span> <span data-ttu-id="82b37-231">除非以合理的限制設定追蹤設定，否則惡意用戶端或應用程式可能會耗盡系統資源。</span><span class="sxs-lookup"><span data-stu-id="82b37-231">A malicious client or application may exhaust system resources unless tracing settings are configured with reasonable limits.</span></span> <span data-ttu-id="82b37-232">使用訊息追蹤功能時，攜帶機密資訊（例如認證、個人資訊等等）的訊息可能會保存到磁片中，或由可存取系統事件檢視器的任何人來查看。</span><span class="sxs-lookup"><span data-stu-id="82b37-232">When using message tracing feature, messages carrying sensitive information such as credentials, personal information, etc. may be persisted to the disk or be viewed by anyone who has access to the system event viewer.</span></span> <span data-ttu-id="82b37-233">基於這個問題的風險降低，Windows 2003 和更新版本上的系統或系統管理員使用者可以啟用追蹤。</span><span class="sxs-lookup"><span data-stu-id="82b37-233">As a mitigation to this issue, tracing can be enabled by System or Administrator users on Windows 2003 and later.</span></span> <span data-ttu-id="82b37-234">在 Windows XP 上，有任何使用者可以開啟追蹤的訊息追蹤功能已停用。</span><span class="sxs-lookup"><span data-stu-id="82b37-234">Message tracing is disabled on Windows XP on which any user can turn tracing on.</span></span>

<span data-ttu-id="82b37-235">下列列舉會搭配追蹤使用：</span><span class="sxs-lookup"><span data-stu-id="82b37-235">The following enumeration is used with tracing:</span></span>

-   [<span data-ttu-id="82b37-236">**WS \_ 追蹤 \_ API**</span><span class="sxs-lookup"><span data-stu-id="82b37-236">**WS\_TRACE\_API**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_trace_api)

 

 




