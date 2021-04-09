---
description: 從 Windows Vista 開始，WMI 服務不會使用 WMI 記錄檔。 相反地，它會使用 Windows 的事件追蹤 (ETW) 而事件可透過事件檢視器或 Wevtutil 命令列工具取得。
ms.assetid: bb6401e8-caf7-4f39-ab64-b7532723ce9a
ms.tgt_platform: multiple
title: 追蹤 WMI 活動
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14371a4f18b81019073cd2b428500b12385719e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103693979"
---
# <a name="tracing-wmi-activity"></a><span data-ttu-id="03cb5-104">追蹤 WMI 活動</span><span class="sxs-lookup"><span data-stu-id="03cb5-104">Tracing WMI Activity</span></span>

<span data-ttu-id="03cb5-105">從 Windows Vista 開始，WMI 服務不會使用 [Wmi 記錄](wmi-log-files.md)檔。</span><span class="sxs-lookup"><span data-stu-id="03cb5-105">Starting with Windows Vista, the WMI service does not use the [WMI Log Files](wmi-log-files.md).</span></span> <span data-ttu-id="03cb5-106">相反地，它會使用 [Windows 的事件追蹤 (ETW)](/windows/desktop/ETW/event-tracing-portal) 而事件可透過 **事件檢視器** 或 Wevtutil 命令列工具取得。</span><span class="sxs-lookup"><span data-stu-id="03cb5-106">Instead, it uses [Event Tracing for Windows (ETW)](/windows/desktop/ETW/event-tracing-portal) and events are available through **Event Viewer** or the Wevtutil command-line tool.</span></span>

<span data-ttu-id="03cb5-107">本主題將討論下列各節：</span><span class="sxs-lookup"><span data-stu-id="03cb5-107">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="03cb5-108">透過事件檢視器取得 WMI 事件</span><span class="sxs-lookup"><span data-stu-id="03cb5-108">Obtaining WMI Events Through Event Viewer</span></span>](#obtaining-wmi-events-through-event-viewer)
-   [<span data-ttu-id="03cb5-109">在命令提示字元中啟用 WMI 追蹤</span><span class="sxs-lookup"><span data-stu-id="03cb5-109">Enabling WMI Tracing at Command Prompt</span></span>](#enabling-wmi-tracing-at-command-prompt)
-   [<span data-ttu-id="03cb5-110">使用以 WPP 為基礎的 WMI 追蹤</span><span class="sxs-lookup"><span data-stu-id="03cb5-110">Using WPP-based WMI Tracing</span></span>](#using-wpp-based-wmi-tracing)
-   [<span data-ttu-id="03cb5-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="03cb5-111">Related topics</span></span>](#related-topics)

## <a name="obtaining-wmi-events-through-event-viewer"></a><span data-ttu-id="03cb5-112">透過事件檢視器取得 WMI 事件</span><span class="sxs-lookup"><span data-stu-id="03cb5-112">Obtaining WMI Events Through Event Viewer</span></span>

<span data-ttu-id="03cb5-113">WMITracing 記錄檔包含 WMI 追蹤的事件。</span><span class="sxs-lookup"><span data-stu-id="03cb5-113">The WMITracing.log file contains the events that WMI traces.</span></span> <span data-ttu-id="03cb5-114">不過，這是二進位檔案。</span><span class="sxs-lookup"><span data-stu-id="03cb5-114">However, this is a binary file.</span></span> <span data-ttu-id="03cb5-115">若要以人類可讀取的格式查看這些事件，請使用 **事件檢視器**。</span><span class="sxs-lookup"><span data-stu-id="03cb5-115">To see these events in a format readable by humans, use the **Event Viewer**.</span></span>

<span data-ttu-id="03cb5-116">根據預設，不會追蹤 WMI 事件。</span><span class="sxs-lookup"><span data-stu-id="03cb5-116">By default, WMI events are not traced.</span></span> <span data-ttu-id="03cb5-117">此程式描述如何使用 **事件檢視器** 來啟用 wmi 事件追蹤和尋找 wmi 事件。</span><span class="sxs-lookup"><span data-stu-id="03cb5-117">This procedure describes how to use **Event Viewer** to enable WMI event tracing and locate WMI events.</span></span> <span data-ttu-id="03cb5-118">您可以透過 wevtutil 命令列工具執行相同的作業。</span><span class="sxs-lookup"><span data-stu-id="03cb5-118">You can do the same operations through the wevtutil command-line tool.</span></span>

<span data-ttu-id="03cb5-119">**若要在事件檢視器中查看 WMI 事件**</span><span class="sxs-lookup"><span data-stu-id="03cb5-119">**To view WMI Events in Event Viewer**</span></span>

1.  <span data-ttu-id="03cb5-120">開啟 [事件檢視器]。</span><span class="sxs-lookup"><span data-stu-id="03cb5-120">Open **Event Viewer**.</span></span> <span data-ttu-id="03cb5-121">在 [ **View** ] 功能表上，按一下 [ **顯示分析和調試記錄**]。</span><span class="sxs-lookup"><span data-stu-id="03cb5-121">On the **View** menu, click **Show Analytic and Debug Logs**.</span></span> <span data-ttu-id="03cb5-122">在 [ 應用程式和服務記錄檔 \| Microsoft \| Windows WMI 活動] 下找出 WMI 的追蹤通道記錄檔 \| 。</span><span class="sxs-lookup"><span data-stu-id="03cb5-122">Locate the **Trace** channel log for WMI under Applications and Service Logs \| Microsoft \| Windows \| WMI Activity.</span></span>
2.  <span data-ttu-id="03cb5-123">以滑鼠右鍵按一下 **追蹤** 記錄檔，然後選取 [ **記錄檔屬性**]。</span><span class="sxs-lookup"><span data-stu-id="03cb5-123">Right-click the **Trace** log and select **Log Properties**.</span></span> <span data-ttu-id="03cb5-124">按一下 [ **啟用記錄** ] 核取方塊，以啟動 WMI 事件追蹤。</span><span class="sxs-lookup"><span data-stu-id="03cb5-124">Click the **Enable Logging** check box to start the WMI event tracing.</span></span> <span data-ttu-id="03cb5-125">如需通道的詳細資訊，請參閱 [Windows 事件記錄檔中的事件記錄檔和通道](/previous-versions//aa385225(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="03cb5-125">For more information about channels, see [Event Logs and Channels in Windows Event Log](/previous-versions//aa385225(v=vs.85)).</span></span>
3.  <span data-ttu-id="03cb5-126">Wmi 事件會顯示在 **Wmi 活動** 的事件視窗中。</span><span class="sxs-lookup"><span data-stu-id="03cb5-126">WMI events appear in the event window for **WMI-Activity**.</span></span> <span data-ttu-id="03cb5-127">按兩下清單中的事件以查看詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="03cb5-127">Double-click an event in the list to see the detailed information.</span></span> <span data-ttu-id="03cb5-128">您可以使用 **XML 視圖** 或 **易記的視圖** 格式來查看事件。</span><span class="sxs-lookup"><span data-stu-id="03cb5-128">You can view an event in **XML View** or in **Friendly View** format.</span></span>

<span data-ttu-id="03cb5-129">[ **事件識別碼** ] 欄位會顯示包含下列資訊的值。</span><span class="sxs-lookup"><span data-stu-id="03cb5-129">The **Event ID** field displays a value that contains the following information.</span></span>

<dl> <dt>

<span data-ttu-id="03cb5-130"><span id="Event_1"></span><span id="event_1"></span><span id="EVENT_1"></span>事件1</span><span class="sxs-lookup"><span data-stu-id="03cb5-130"><span id="Event_1"></span><span id="event_1"></span><span id="EVENT_1"></span>Event 1</span></span>
</dt> <dd>

<span data-ttu-id="03cb5-131">特定作業的事件順序開始。</span><span class="sxs-lookup"><span data-stu-id="03cb5-131">Start of the event sequence for a specific operation.</span></span> <span data-ttu-id="03cb5-132">每個序列都會出現一次。</span><span class="sxs-lookup"><span data-stu-id="03cb5-132">One occurrence for each sequence.</span></span>

<span data-ttu-id="03cb5-133">事件1的事件欄位如下：</span><span class="sxs-lookup"><span data-stu-id="03cb5-133">The event fields for an Event 1 are:</span></span>

-   <span data-ttu-id="03cb5-134">**GroupOperationID** 是唯一的識別碼，用於針對特定用戶端回報的所有事件。</span><span class="sxs-lookup"><span data-stu-id="03cb5-134">**GroupOperationID** is a unique identifier that is used for all events reported for a specific client.</span></span>
-   <span data-ttu-id="03cb5-135">**OperationId** 表示作業順序。</span><span class="sxs-lookup"><span data-stu-id="03cb5-135">**OperationId** indicates the operation sequence.</span></span>
-   <span data-ttu-id="03cb5-136">作業 **會指定對** WMI 的連接或要求。</span><span class="sxs-lookup"><span data-stu-id="03cb5-136">**Operation** specifies the connection or request to WMI.</span></span>
-   <span data-ttu-id="03cb5-137">**使用者** 指出透過執行腳本或透過 CIM STUDIO 對 WMI 提出要求的帳戶。</span><span class="sxs-lookup"><span data-stu-id="03cb5-137">**User** indicates the account that makes a request to WMI by running a script or through CIM Studio.</span></span>
-   <span data-ttu-id="03cb5-138">**命名空間** 會顯示連接的目標 WMI 命名空間。</span><span class="sxs-lookup"><span data-stu-id="03cb5-138">**Namespace** shows the WMI namespace to which the connection is made.</span></span>

<span data-ttu-id="03cb5-139">例如，腳本可能會要求 WMI 類別的所有實例，例如 [**Win32 \_ 服務**](/windows/desktop/CIMWin32Prov/win32-service)。</span><span class="sxs-lookup"><span data-stu-id="03cb5-139">For example, a script may request all the instances of a WMI class, such as [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service).</span></span> <span data-ttu-id="03cb5-140">第一個作業可能是與 WMI 的連接。</span><span class="sxs-lookup"><span data-stu-id="03cb5-140">The first operation may be a connection to WMI.</span></span>

</dd> <dt>

<span data-ttu-id="03cb5-141"><span id="Event_2"></span><span id="event_2"></span><span id="EVENT_2"></span>事件2</span><span class="sxs-lookup"><span data-stu-id="03cb5-141"><span id="Event_2"></span><span id="event_2"></span><span id="EVENT_2"></span>Event 2</span></span>
</dt> <dd>

<span data-ttu-id="03cb5-142">組成作業的事件。</span><span class="sxs-lookup"><span data-stu-id="03cb5-142">Events that make up the operation.</span></span> <span data-ttu-id="03cb5-143">順序中的一或多個出現次數。</span><span class="sxs-lookup"><span data-stu-id="03cb5-143">One or more occurrences in the sequence.</span></span>

<span data-ttu-id="03cb5-144">事件2的事件欄位如下：</span><span class="sxs-lookup"><span data-stu-id="03cb5-144">The event fields for an Event 2 are:</span></span>

-   <span data-ttu-id="03cb5-145">**GroupOperationID** 指出事件發生的順序。</span><span class="sxs-lookup"><span data-stu-id="03cb5-145">**GroupOperationID** indicates the sequence in which the event occurs.</span></span>
-   <span data-ttu-id="03cb5-146">**GroupOperationID** 指出事件發生的順序。</span><span class="sxs-lookup"><span data-stu-id="03cb5-146">**GroupOperationID** indicates the sequence in which the event occurs.</span></span>
-   <span data-ttu-id="03cb5-147">**ProviderName** 表示提供資料的提供者名稱。</span><span class="sxs-lookup"><span data-stu-id="03cb5-147">**ProviderName** indicates the name of the provider which supplies the data.</span></span>
-   <span data-ttu-id="03cb5-148">**Path** 是物件的 WMI 路徑。</span><span class="sxs-lookup"><span data-stu-id="03cb5-148">**Path** is the WMI path to the object.</span></span>

<span data-ttu-id="03cb5-149">例如，作業可能是 [**Win32 \_ 服務**](/windows/desktop/CIMWin32Prov/win32-service)的列舉。</span><span class="sxs-lookup"><span data-stu-id="03cb5-149">For example, the operation may be an enumeration of [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service).</span></span>

</dd> <dt>

<span data-ttu-id="03cb5-150"><span id="Event_3"></span><span id="event_3"></span><span id="EVENT_3"></span>事件3</span><span class="sxs-lookup"><span data-stu-id="03cb5-150"><span id="Event_3"></span><span id="event_3"></span><span id="EVENT_3"></span>Event 3</span></span>
</dt> <dd>

<span data-ttu-id="03cb5-151">特定作業的事件序列結尾。</span><span class="sxs-lookup"><span data-stu-id="03cb5-151">End of the event sequence for a specific operation.</span></span> <span data-ttu-id="03cb5-152">每個序列都會出現一次。</span><span class="sxs-lookup"><span data-stu-id="03cb5-152">One occurrence for each sequence.</span></span>

<span data-ttu-id="03cb5-153">只會顯示 **GroupOperationID** 。</span><span class="sxs-lookup"><span data-stu-id="03cb5-153">Only the **GroupOperationID** is shown.</span></span>

</dd> </dl>

## <a name="enabling-wmi-tracing-at-command-prompt"></a><span data-ttu-id="03cb5-154">在命令提示字元中啟用 WMI 追蹤</span><span class="sxs-lookup"><span data-stu-id="03cb5-154">Enabling WMI Tracing at Command Prompt</span></span>

<span data-ttu-id="03cb5-155">您也可以透過 Wevtutil 命令列工具啟用 WMI 事件追蹤。</span><span class="sxs-lookup"><span data-stu-id="03cb5-155">You can also enable WMI event tracing through the Wevtutil command-line tool.</span></span> <span data-ttu-id="03cb5-156">使用下列命令： **Wevtutil.exe Sl Microsoft-Windows-WMI-活動/追蹤/e： true**。</span><span class="sxs-lookup"><span data-stu-id="03cb5-156">Use the following command: **Wevtutil.exe sl Microsoft-Windows-WMI-Activity/Trace /e:true**.</span></span> <span data-ttu-id="03cb5-157">WMI 事件來源是 Microsoft Windows-WMI。</span><span class="sxs-lookup"><span data-stu-id="03cb5-157">The WMI event source is Microsoft-Windows-WMI.</span></span> <span data-ttu-id="03cb5-158">如需 Wevtutil.exe 的詳細資訊，請參閱 [關於 Windows 事件記錄](/previous-versions//aa382610(v=vs.85))檔。</span><span class="sxs-lookup"><span data-stu-id="03cb5-158">For more information about Wevtutil.exe, see [About Windows Event Log](/previous-versions//aa382610(v=vs.85)).</span></span>

## <a name="using-wpp-based-wmi-tracing"></a><span data-ttu-id="03cb5-159">使用以 WPP 為基礎的 WMI 追蹤</span><span class="sxs-lookup"><span data-stu-id="03cb5-159">Using WPP-based WMI Tracing</span></span>

<span data-ttu-id="03cb5-160">從 Windows Vista 開始，在 Windows 作業系統中，WMI 會在開機程式期間建立作用中的追蹤通道。</span><span class="sxs-lookup"><span data-stu-id="03cb5-160">In Windows operating systems starting with Windows Vista, WMI creates an active trace channel during the boot process.</span></span> <span data-ttu-id="03cb5-161">通道的名稱是 WMI \_ 追蹤 \_ 會話。</span><span class="sxs-lookup"><span data-stu-id="03cb5-161">The name of the channel is WMI\_Trace\_Session.</span></span> <span data-ttu-id="03cb5-162">只有錯誤會記錄到通道。</span><span class="sxs-lookup"><span data-stu-id="03cb5-162">Only errors are logged to the channel.</span></span>

<span data-ttu-id="03cb5-163">Windows 軟體追蹤預處理器 (WPP) 會在二進位檔案中記錄資訊。</span><span class="sxs-lookup"><span data-stu-id="03cb5-163">The Windows software trace preprocessor (WPP) records information in a binary file.</span></span> <span data-ttu-id="03cb5-164">若要讀取檔案，您必須先將它轉譯成可讀取的文字格式。</span><span class="sxs-lookup"><span data-stu-id="03cb5-164">To read the file, you must first translate it into a readable, text format.</span></span> <span data-ttu-id="03cb5-165">您可以使用稱為 tracefmt.exe 的工具（ [Windows 驅動程式套件 (WDK) ](https://www.microsoft.com/whdc/DevTools/WDK/WDKpkg.mspx) ）來進行轉譯。</span><span class="sxs-lookup"><span data-stu-id="03cb5-165">You use a tool called tracefmt.exe from the [Windows Driver Kit (WDK)](https://www.microsoft.com/whdc/DevTools/WDK/WDKpkg.mspx) to do the translation.</span></span> <span data-ttu-id="03cb5-166">此工具需要儲存在某些相關檔案中的資訊。</span><span class="sxs-lookup"><span data-stu-id="03cb5-166">The tool requires information stored in some associated files.</span></span> <span data-ttu-id="03cb5-167">這些檔案位於% SystemRoot% \\ System32 \\ wbem \\ tmf 目錄中，而且副檔名為 tmf。</span><span class="sxs-lookup"><span data-stu-id="03cb5-167">The files are located in the %SystemRoot%\\System32\\wbem\\tmf directory and have a .tmf file name extension.</span></span> <span data-ttu-id="03cb5-168">此工具實際上需要單一 tmf 檔案。</span><span class="sxs-lookup"><span data-stu-id="03cb5-168">The tool actually requires a single .tmf file .</span></span> <span data-ttu-id="03cb5-169">您可以藉由將所有的 tmf 檔案串連至另一個 tmf 檔案，來建立該單一檔案。</span><span class="sxs-lookup"><span data-stu-id="03cb5-169">You make that single file by concatenating all of the .tmf files into another .tmf file.</span></span> <span data-ttu-id="03cb5-170">如需 tmf 檔案的詳細資訊，請參閱 [追蹤訊息格式](/windows-hardware/drivers/devtest/trace-message-format-file)檔案。</span><span class="sxs-lookup"><span data-stu-id="03cb5-170">For more information about .tmf files, see [Trace Message Format File](/windows-hardware/drivers/devtest/trace-message-format-file).</span></span>

<span data-ttu-id="03cb5-171">安裝 [Windows 驅動程式套件 (WDK) ](https://www.microsoft.com/whdc/DevTools/WDK/WDKpkg.mspx) 以取得 tracelog.exe 和 tracefmt.exe 命令列工具之後，請執行下列步驟來收集以 WPP 為基礎的 WMI 追蹤。</span><span class="sxs-lookup"><span data-stu-id="03cb5-171">After installing the [Windows Driver Kit (WDK)](https://www.microsoft.com/whdc/DevTools/WDK/WDKpkg.mspx) to get the tracelog.exe and tracefmt.exe command-line tools, perform the following steps to collect a WPP-based WMI trace.</span></span>

<span data-ttu-id="03cb5-172">**若要查看以 WPP 為基礎的 WMI 追蹤**</span><span class="sxs-lookup"><span data-stu-id="03cb5-172">**To view a WPP-based WMI trace**</span></span>

1.  <span data-ttu-id="03cb5-173">若要建立單一 tmf 檔案，請開啟提升許可權的命令提示字元視窗，然後流覽至% SystemRoot% \\ System32 \\ wbem \\ tmf 目錄。</span><span class="sxs-lookup"><span data-stu-id="03cb5-173">To create the single .tmf file, open an elevated Command Prompt window and navigate to the %SystemRoot%\\System32\\wbem\\tmf directory.</span></span>

2.  <span data-ttu-id="03cb5-174">輸入 **copy/y% SystemRoot% \\ system32 \\ wbem \\ Tmf \\ \* . tmf% systemroot% \\ system32 \\ wbem \\ tmf \\ wmi. tmf**。</span><span class="sxs-lookup"><span data-stu-id="03cb5-174">Type **copy /y %SystemRoot%\\System32\\wbem\\tmf\\\*.tmf %SystemRoot%\\System32\\wbem\\tmf\\wmi.tmf**.</span></span> <span data-ttu-id="03cb5-175">這會建立名為 tmf 的檔案，其中包含所有 tmf 檔案的內容。</span><span class="sxs-lookup"><span data-stu-id="03cb5-175">This will create a file named wmi.tmf that includes the contents of all of the other .tmf files.</span></span>

3.  <span data-ttu-id="03cb5-176">輸入 **tracelog.exe-FLUSH WMI \_ Trace \_ Session**。</span><span class="sxs-lookup"><span data-stu-id="03cb5-176">Type **tracelog -flush WMI\_Trace\_Session**.</span></span> <span data-ttu-id="03cb5-177">這會清除磁片上的 WPP 緩衝區。</span><span class="sxs-lookup"><span data-stu-id="03cb5-177">This will flush the WPP buffers on the disk.</span></span>
4.  <span data-ttu-id="03cb5-178">輸入 **集追蹤 \_ 格式 \_ 前置詞 \[ = %9！ d！ \]%8！04X！。%3！04X！。%3！04X！：： %4！ s！ \[%1！ s！ \] (%！COMPNAME!:%!FUNC！： %2！ s！ )**。</span><span class="sxs-lookup"><span data-stu-id="03cb5-178">Type **set TRACE\_FORMAT\_PREFIX = \[%9!d!\]%8!04X!.%3!04X!.%3!04X!::%4!s!\[%1!s!\](%!COMPNAME!:%!FUNC !:%2!s!)**.</span></span> <span data-ttu-id="03cb5-179">Tracefmt 工具會在每個追蹤訊息中加入一些預設資訊。</span><span class="sxs-lookup"><span data-stu-id="03cb5-179">The tracefmt tool adds some default information to each trace message.</span></span> <span data-ttu-id="03cb5-180">您可以設定追蹤 \_ 格式前置詞環境變數來設定所包含的資訊 \_ 。</span><span class="sxs-lookup"><span data-stu-id="03cb5-180">You can configure what information is included by setting the TRACE\_FORMAT\_PREFIX environment variable.</span></span> <span data-ttu-id="03cb5-181">若要瞭解所使用的語法，請參閱 [追蹤訊息前置](https://msdn.microsoft.com/library/aa139695.aspx)詞。</span><span class="sxs-lookup"><span data-stu-id="03cb5-181">To learn about the syntax used, see [Trace Message Prefix](https://msdn.microsoft.com/library/aa139695.aspx).</span></span>
5.  <span data-ttu-id="03cb5-182">輸入 **tracefmt-tmf% systemroot% \\ system32 \\ wbem \\ tmf \\ wmi. tmf-o OUTPUT.TXT% systemroot% \\ system32 \\ wbem \\ 記錄 \\ WMITracing .log**。</span><span class="sxs-lookup"><span data-stu-id="03cb5-182">Type **tracefmt -tmf %systemroot%\\system32\\wbem\\tmf\\wmi.tmf -o OUTPUT.TXT %systemroot%\\system32\\wbem\\logs\\WMITracing.log**.</span></span> <span data-ttu-id="03cb5-183">這會執行從二進位格式到可讀取文字格式的轉譯。</span><span class="sxs-lookup"><span data-stu-id="03cb5-183">This performs the translation from binary format to readable text format.</span></span>
6.  <span data-ttu-id="03cb5-184">輸入 **notepad% systemroot% \\ system32 \\ wbem \\ tmf \\OUTPUT.TXT**。</span><span class="sxs-lookup"><span data-stu-id="03cb5-184">Type **notepad %systemroot%\\system32\\wbem\\tmf\\OUTPUT.TXT**.</span></span> <span data-ttu-id="03cb5-185">這將會在 [記事本] 中開啟追蹤檔案。</span><span class="sxs-lookup"><span data-stu-id="03cb5-185">This will open the trace file in Notepad.</span></span>

<span data-ttu-id="03cb5-186">以下是一些您可能需要執行的其他 WPP 相關工作。</span><span class="sxs-lookup"><span data-stu-id="03cb5-186">The following are some other WPP-related tasks you might need to perform.</span></span>

<span data-ttu-id="03cb5-187">**停止以 WPP 為基礎的 WMI 追蹤**</span><span class="sxs-lookup"><span data-stu-id="03cb5-187">**To stop WPP-based WMI tracing**</span></span>

-   <span data-ttu-id="03cb5-188">輸入 **tracelog.exe-STOP WMI \_ Trace \_ Session**。</span><span class="sxs-lookup"><span data-stu-id="03cb5-188">Type **tracelog -stop WMI\_Trace\_Session**.</span></span>

<span data-ttu-id="03cb5-189">**啟動以 WPP 為基礎的 WMI 追蹤**</span><span class="sxs-lookup"><span data-stu-id="03cb5-189">**To start WPP-based WMI tracing**</span></span>

-   <span data-ttu-id="03cb5-190">輸入 **tracelog.exe-啟動 WMI \_ 追蹤 \_ 會話-guid \# 1FF6B227-2CA7-40f9-9A66-980EADAA602E-rt-層級 5-旗標 0x7-f MYTRACE。BIN**</span><span class="sxs-lookup"><span data-stu-id="03cb5-190">Type **tracelog -start WMI\_Trace\_Session -guid \#1FF6B227-2CA7-40f9-9A66-980EADAA602E -rt -level 5 -flag 0x7 -f MYTRACE.BIN**</span></span>

<span data-ttu-id="03cb5-191">**Windows Vista：** 根據預設，會將以 WPP 為基礎的 WMI 追蹤設定為層級2，其中只包含錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="03cb5-191">**Windows Vista:** By default, WPP-based WMI tracing is set to level 2 which includes only error messages.</span></span> <span data-ttu-id="03cb5-192">若要同時包含資訊訊息，請將層級設定為4。</span><span class="sxs-lookup"><span data-stu-id="03cb5-192">To include informational messages as well, set the level to 4.</span></span> <span data-ttu-id="03cb5-193">預設會追蹤 WMI 的所有區域。</span><span class="sxs-lookup"><span data-stu-id="03cb5-193">All areas of WMI are traced by default.</span></span> <span data-ttu-id="03cb5-194">有三個可追蹤的不同區域： Core (旗標 = 0x1) 、ESS (旗標 = 0x2) 和 >prov (旗標 = 0x4) 。</span><span class="sxs-lookup"><span data-stu-id="03cb5-194">There are three distinct areas that can be traced: Core (flag=0x1), ESS (flag=0x2) and Prov (flag=0x4).</span></span> <span data-ttu-id="03cb5-195">在上述的 start 命令中， **旗標 0x7** 會追蹤所有三個區域。</span><span class="sxs-lookup"><span data-stu-id="03cb5-195">In the start command above, **flag 0x7** causes all three areas to be traced.</span></span>

<span data-ttu-id="03cb5-196">**Windows 7：** 根據預設，會停用以 WPP 為基礎的 WMI 追蹤，並將其設定為層級0。</span><span class="sxs-lookup"><span data-stu-id="03cb5-196">**Windows 7:** By default, WPP-based WMI tracing is disabled and set to level 0.</span></span> <span data-ttu-id="03cb5-197">若要使用以 WPP 為基礎的 WMI 追蹤，必須啟用這項功能，並將錯誤訊息的層級2設為，並將錯誤和參考用訊息設定為層級4。</span><span class="sxs-lookup"><span data-stu-id="03cb5-197">To use WPP-based WMI tracing, this feature must be enabled and set to either level 2 for error messages or level 4 for both error and informational messages.</span></span>

<span data-ttu-id="03cb5-198">**列出所有的 WPP 追蹤會話**</span><span class="sxs-lookup"><span data-stu-id="03cb5-198">**To list all WPP trace sessions**</span></span>

-   <span data-ttu-id="03cb5-199">輸入 **tracelog.exe-l**。</span><span class="sxs-lookup"><span data-stu-id="03cb5-199">Type **tracelog -l**.</span></span>

<span data-ttu-id="03cb5-200">**列出 WMI WPP 追蹤會話的相關資訊**</span><span class="sxs-lookup"><span data-stu-id="03cb5-200">**To list info about the WMI WPP trace session**</span></span>

-   <span data-ttu-id="03cb5-201">輸入 **tracelog.exe-l \| findstr/i "wmi \_ trace"**。</span><span class="sxs-lookup"><span data-stu-id="03cb5-201">Type **tracelog -l \| findstr /i "wmi\_trace"**.</span></span>

<span data-ttu-id="03cb5-202">**若要查看 WMI WPP 追蹤會話參數**</span><span class="sxs-lookup"><span data-stu-id="03cb5-202">**To view the WMI WPP trace session parameters**</span></span>

-   <span data-ttu-id="03cb5-203">輸入 **tracelog.exe-q WMI \_ Trace \_ Session**。</span><span class="sxs-lookup"><span data-stu-id="03cb5-203">Type **tracelog -q WMI\_Trace\_Session**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="03cb5-204">相關主題</span><span class="sxs-lookup"><span data-stu-id="03cb5-204">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="03cb5-205">[WMI 疑難排解](wmi-troubleshooting.md) \(英文\)</span><span class="sxs-lookup"><span data-stu-id="03cb5-205">[WMI Troubleshooting](wmi-troubleshooting.md)</span></span>
</dt> <dt>

[<span data-ttu-id="03cb5-206">WMI 記錄檔</span><span class="sxs-lookup"><span data-stu-id="03cb5-206">WMI Log Files</span></span>](wmi-log-files.md)
</dt> </dl>

 

 
