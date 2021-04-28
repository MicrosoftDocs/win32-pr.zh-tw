---
description: Winsock 追蹤的控制權
ms.assetid: b079bdfc-b192-451c-967d-dcefa94b7ec7
title: Winsock 追蹤的控制權
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75f256c4e3927672bc13b14bfb72ca3b02c22bde
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110546"
---
# <a name="control-of-winsock-tracing"></a><span data-ttu-id="dc080-103">Winsock 追蹤的控制權</span><span class="sxs-lookup"><span data-stu-id="dc080-103">Control of Winsock Tracing</span></span>

<span data-ttu-id="dc080-104">您可以使用下列其中一種方法來控制 Winsock 追蹤：</span><span class="sxs-lookup"><span data-stu-id="dc080-104">Winsock tracing can be controlled by using either of the following methods:</span></span>

-   <span data-ttu-id="dc080-105">命令列工具</span><span class="sxs-lookup"><span data-stu-id="dc080-105">Command-line tools</span></span>

    <span data-ttu-id="dc080-106">Windows Vista 和 Windows Server 2008 中包含兩個命令列工具，可用來控制追蹤並將二進位追蹤記錄檔轉換為可讀取的文字。</span><span class="sxs-lookup"><span data-stu-id="dc080-106">Two command-line tools are included with Windows Vista and Windows Server 2008 that are used to control tracing and convert the binary trace log file to readable text.</span></span>

    <span data-ttu-id="dc080-107">**logman.exe** 工具是用來啟動或停止 Winsock 追蹤。</span><span class="sxs-lookup"><span data-stu-id="dc080-107">The **logman.exe** tool is used to start or stop Winsock tracing.</span></span>

    <span data-ttu-id="dc080-108">**tracerpt.exe** 工具是用來將二進位追蹤記錄檔轉換成可讀取的文字檔。</span><span class="sxs-lookup"><span data-stu-id="dc080-108">The **tracerpt.exe** tool is used to convert the binary trace log file to a readable text file.</span></span>

-   <span data-ttu-id="dc080-109">事件檢視器</span><span class="sxs-lookup"><span data-stu-id="dc080-109">Event Viewer</span></span>

    <span data-ttu-id="dc080-110">Windows Vista 和更新版本上的事件檢視器也可以用來啟用 Winsock 追蹤。</span><span class="sxs-lookup"><span data-stu-id="dc080-110">The Event Viewer on Windows Vista and later can also be used to enable Winsock tracing.</span></span> <span data-ttu-id="dc080-111">事件檢視器可從 [開始] 功能表的系統管理工具存取。</span><span class="sxs-lookup"><span data-stu-id="dc080-111">The Event Viewer is accessible under the Administrative Tools from the Start menu.</span></span>

## <a name="using-logman-and-tracert"></a><span data-ttu-id="dc080-112">使用 logman 和 tracert</span><span class="sxs-lookup"><span data-stu-id="dc080-112">Using logman and tracert</span></span>

<span data-ttu-id="dc080-113">在 Windows Vista 和更新版本上，預設會停用 Winsock 網路事件追蹤。</span><span class="sxs-lookup"><span data-stu-id="dc080-113">Winsock network event tracing is disabled by default on Windows Vista and later.</span></span>

<span data-ttu-id="dc080-114">下列命令會啟動電腦上的 Winsock 網路事件追蹤、將事件追蹤會話的名稱設定為 mywinsocksession，然後將輸出傳送至名為 winsocklogfile 的二進位記錄檔：</span><span class="sxs-lookup"><span data-stu-id="dc080-114">The following command starts Winsock network event tracing on a computer, sets the name of event trace session to mywinsocksession, and sends output to a binary log file called winsocklogfile.etl:</span></span>

<span data-ttu-id="dc080-115">**logman start-ets mywinsocksession-o winsocklogfile .etl-p Microsoft-Windows-Winsock-AFD**</span><span class="sxs-lookup"><span data-stu-id="dc080-115">**logman start -ets mywinsocksession -o winsocklogfile.etl -p Microsoft-Windows-Winsock-AFD**</span></span>

<span data-ttu-id="dc080-116">記錄檔是在目前的目錄中建立，其中包含 winsocklogfile 000001 格式的檔案名 \_ 。</span><span class="sxs-lookup"><span data-stu-id="dc080-116">Log files are created in the current directory with filenames of the form winsocklogfile\_000001.etl</span></span>

<span data-ttu-id="dc080-117">下列命令會針對名為 mywinsocksession 的會話，在電腦上停止上述的 Winsock 追蹤：</span><span class="sxs-lookup"><span data-stu-id="dc080-117">The following command stops the above Winsock tracing on a computer for the session named mywinsocksession:</span></span>

<span data-ttu-id="dc080-118">**logman stop-ets mywinsocksession**</span><span class="sxs-lookup"><span data-stu-id="dc080-118">**logman stop -ets mywinsocksession**</span></span>

<span data-ttu-id="dc080-119">二進位記錄檔將會寫入– o 參數所指定的位置。</span><span class="sxs-lookup"><span data-stu-id="dc080-119">A binary log file will be written to the location specified by the –o parameter.</span></span> <span data-ttu-id="dc080-120">若要將二進位檔案轉譯成可讀取的文字檔，請使用 **tracerpt.exe** ：</span><span class="sxs-lookup"><span data-stu-id="dc080-120">To translate the binary file into a readable text file, **tracerpt.exe** is used:</span></span>

<span data-ttu-id="dc080-121">**tracerpt.exe 的 .etl 檔案 <名稱> – o winsocktracelog.txt**</span><span class="sxs-lookup"><span data-stu-id="dc080-121">**tracerpt.exe <name of the .etl file> –o winsocktracelog.txt**</span></span>

<span data-ttu-id="dc080-122">如果偏好包含 xml 而非純文字的輸出檔，則會使用下列命令：</span><span class="sxs-lookup"><span data-stu-id="dc080-122">If an output file containing xml rather than plain text is preferred, the following command is used:</span></span>

<span data-ttu-id="dc080-123">**tracerpt.exe etl 檔的 <名稱> – o winsocktracelog.xml of xml**</span><span class="sxs-lookup"><span data-stu-id="dc080-123">**tracerpt.exe <name of the .etl file> –o winsocktracelog.xml –of xml**</span></span>

<span data-ttu-id="dc080-124">在 Windows Vista 和更新版本上，預設會啟用 Winsock 目錄變更追蹤。</span><span class="sxs-lookup"><span data-stu-id="dc080-124">Winsock catalog change tracing is enabled by default on Windows Vista and later.</span></span>

> [!Note]  
> <span data-ttu-id="dc080-125">已淘汰分層服務提供者。</span><span class="sxs-lookup"><span data-stu-id="dc080-125">Layered Service Providers are deprecated.</span></span> <span data-ttu-id="dc080-126">從 Windows 8 和 Windows Server 2012 開始，請使用 [Windows 篩選平台](../fwp/windows-filtering-platform-start-page.md)。</span><span class="sxs-lookup"><span data-stu-id="dc080-126">Starting with Windows 8 and Windows Server 2012, use [Windows Filtering Platform](../fwp/windows-filtering-platform-start-page.md).</span></span>

 

<span data-ttu-id="dc080-127">下列命令會針對在電腦上 (Lsp) 的多層式服務提供者啟動 Winsock 目錄變更追蹤、將事件追蹤會話的名稱設定為 mywinsockcatalogsession，然後將輸出傳送至名為 winsockcataloglogfile 的二進位記錄檔：</span><span class="sxs-lookup"><span data-stu-id="dc080-127">The following command starts Winsock Catalog Change tracing for layered service providers (LSPs) on a computer, sets the name of event trace session to mywinsockcatalogsession, and sends output to a binary log file called winsockcataloglogfile.etl:</span></span>

<span data-ttu-id="dc080-128">**logman start-ets mywinsockcatalogsession-o winsockcataloglogfile .etl-p Microsoft-Windows-Winsock-WS2HELP**</span><span class="sxs-lookup"><span data-stu-id="dc080-128">**logman start -ets mywinsockcatalogsession -o winsockcataloglogfile.etl -p Microsoft-Windows-Winsock-WS2HELP**</span></span>

<span data-ttu-id="dc080-129">記錄檔是在目前的目錄中建立，其中包含 winsockcataloglogfile 000001 格式的檔案名 \_ 。</span><span class="sxs-lookup"><span data-stu-id="dc080-129">Log files are created in the current directory with filenames of the form winsockcataloglogfile\_000001.etl</span></span>

<span data-ttu-id="dc080-130">下列命令會針對名為 mysession 的會話，在電腦上停止上述的 Winsock 追蹤：</span><span class="sxs-lookup"><span data-stu-id="dc080-130">The following command stops the above Winsock tracing on a computer for the session named mysession:</span></span>

<span data-ttu-id="dc080-131">**logman stop-ets mywinsockcatalogsession**</span><span class="sxs-lookup"><span data-stu-id="dc080-131">**logman stop -ets mywinsockcatalogsession**</span></span>

<span data-ttu-id="dc080-132">二進位記錄檔將會寫入– o 參數所指定的位置。</span><span class="sxs-lookup"><span data-stu-id="dc080-132">A binary log file will be written to the location specified by the –o parameter.</span></span> <span data-ttu-id="dc080-133">若要將二進位檔案轉譯成可讀取的文字檔，請使用 **tracerpt.exe** ：</span><span class="sxs-lookup"><span data-stu-id="dc080-133">To translate the binary file into a readable text file, **tracerpt.exe** is used:</span></span>

<span data-ttu-id="dc080-134">**tracerpt.exe 的 .etl 檔案 <名稱> – o winsockcatalogtracelog.txt**</span><span class="sxs-lookup"><span data-stu-id="dc080-134">**tracerpt.exe <name of the .etl file> –o winsockcatalogtracelog.txt**</span></span>

<span data-ttu-id="dc080-135">如果偏好包含 xml 而非純文字的輸出檔，則會使用下列命令：</span><span class="sxs-lookup"><span data-stu-id="dc080-135">If an output file containing xml rather than plain text is preferred, the following command is used:</span></span>

<span data-ttu-id="dc080-136">**tracerpt.exe etl 檔的 <名稱> – o winsockcatalogtracelog.xml of xml**</span><span class="sxs-lookup"><span data-stu-id="dc080-136">**tracerpt.exe <name of the .etl file> –o winsockcatalogtracelog.xml –of xml**</span></span>

## <a name="using-event-viewer-to-start-winsock-network-event-tracing"></a><span data-ttu-id="dc080-137">使用事件檢視器啟動 Winsock 網路事件追蹤</span><span class="sxs-lookup"><span data-stu-id="dc080-137">Using Event Viewer to Start Winsock Network Event Tracing</span></span>

<span data-ttu-id="dc080-138">當您開啟事件檢視器時，左窗格會包含事件的清單。</span><span class="sxs-lookup"><span data-stu-id="dc080-138">When you open Event Viewer, the left pane contains the list of events.</span></span> <span data-ttu-id="dc080-139">開啟 [ **應用程式及服務記錄** 檔]，並流覽至 [ **Microsoft \\ Windows \\ Winsock 網路事件** ] 作為來源，然後選取 [ **操作**]。</span><span class="sxs-lookup"><span data-stu-id="dc080-139">Open **Applications and Services Logs** and navigate to **Microsoft\\Windows\\Winsock Network Event** as the source and select **Operational**.</span></span>

<span data-ttu-id="dc080-140">在 [動作] 窗格中，選取 [ **記錄** 內容]，然後選取 [ **啟用記錄** ] 核取方塊。</span><span class="sxs-lookup"><span data-stu-id="dc080-140">In the Action pane, select **Log Properties** and check the **Enable Logging** check box.</span></span> <span data-ttu-id="dc080-141">啟用記錄之後，您也可以變更記錄檔的大小（如果需要的話）。</span><span class="sxs-lookup"><span data-stu-id="dc080-141">Once logging is enabled, you can also change the size of the log file if this is needed.</span></span>

<span data-ttu-id="dc080-142">Winsock 網路事件追蹤現在已啟用，您只需要重新整理動作，即可更新已記錄的事件清單。</span><span class="sxs-lookup"><span data-stu-id="dc080-142">Winsock network event tracing is now enabled and all you need to do is hit the Refresh action to update the list of events that have been logged.</span></span> <span data-ttu-id="dc080-143">若要停止記錄，只要取消選取相同的選項按鈕即可。</span><span class="sxs-lookup"><span data-stu-id="dc080-143">To stop logging, simply uncheck the same radio button.</span></span>

<span data-ttu-id="dc080-144">您可能需要根據您想要查看的事件數目來增加記錄檔大小。</span><span class="sxs-lookup"><span data-stu-id="dc080-144">You may need to increase the log size depending on how many events you want to see.</span></span> <span data-ttu-id="dc080-145">使用事件檢視器進行 Winsock 追蹤的一個缺點是，它不會載入所有字串資源，因此在您選取事件) 時，[描述] 欄位中所顯示的訊息 (，有時很難讀取 (必須格式化為十六進位的引數會以十進位顯示，例如) 。</span><span class="sxs-lookup"><span data-stu-id="dc080-145">One drawback to using the Event Viewer for Winsock tracing is that it does not load all the string resources so the messages displayed in the Description field (once you select an event) is sometimes hard to read (an argument that should be formatted as hex will be displayed in decimal, for example).</span></span> <span data-ttu-id="dc080-146">不過，您可以在 [事件描述] 中選取 [ **詳細資料** ] 索引標籤，以顯示原始 XML 記錄專案，這通常會更容易瞭解引數。</span><span class="sxs-lookup"><span data-stu-id="dc080-146">However, you can select the **Details** tab in the event description which shows the raw XML log entry which usually has easier to understand arguments.</span></span>

## <a name="using-event-viewer-to-start-winsock-catalog-change-tracing"></a><span data-ttu-id="dc080-147">使用事件檢視器啟動 Winsock 類別目錄變更追蹤</span><span class="sxs-lookup"><span data-stu-id="dc080-147">Using Event Viewer to Start Winsock Catalog Change Tracing</span></span>

<span data-ttu-id="dc080-148">當您開啟事件檢視器時，左窗格會包含事件的清單。</span><span class="sxs-lookup"><span data-stu-id="dc080-148">When you open Event Viewer, the left pane contains the list of events.</span></span> <span data-ttu-id="dc080-149">開啟 [ **應用程式及服務記錄** 檔]，並流覽至 [ **Microsoft \\ Windows \\ Winsock 目錄變更** ] 作為來源，然後選取 [ **操作**]。</span><span class="sxs-lookup"><span data-stu-id="dc080-149">Open **Applications and Services Logs** and navigate to **Microsoft\\Windows\\Winsock Catalog Change** as the source and select **Operational**.</span></span>

<span data-ttu-id="dc080-150">在 [動作] 窗格中，選取 [ **記錄** 內容]，然後選取 [ **啟用記錄** ] 核取方塊。</span><span class="sxs-lookup"><span data-stu-id="dc080-150">In the Action pane, select **Log Properties** and check the **Enable Logging** check box.</span></span> <span data-ttu-id="dc080-151">啟用記錄之後，您也可以變更記錄檔的大小（如果需要的話）。</span><span class="sxs-lookup"><span data-stu-id="dc080-151">Once logging is enabled, you can also change the size of the log file if this is needed.</span></span>

<span data-ttu-id="dc080-152">Winsock 目錄變更追蹤現在已啟用，您只需要重新整理動作，即可更新已記錄的事件清單。</span><span class="sxs-lookup"><span data-stu-id="dc080-152">Winsock catalog change tracing is now enabled and all you need to do is hit the Refresh action to update the list of events that have been logged.</span></span> <span data-ttu-id="dc080-153">若要停止記錄，只要取消選取相同的選項按鈕即可。</span><span class="sxs-lookup"><span data-stu-id="dc080-153">To stop logging, simply uncheck the same radio button.</span></span>

<span data-ttu-id="dc080-154">您可能需要根據您想要查看的事件數目來增加記錄檔大小。</span><span class="sxs-lookup"><span data-stu-id="dc080-154">You may need to increase the log size depending on how many events you want to see.</span></span> <span data-ttu-id="dc080-155">使用事件檢視器進行 Winsock 追蹤的一個缺點是，它不會載入所有字串資源，因此在您選取事件) 時，[描述] 欄位中所顯示的訊息 (，有時很難讀取 (必須格式化為十六進位的引數會以十進位顯示，例如) 。</span><span class="sxs-lookup"><span data-stu-id="dc080-155">One drawback to using the Event Viewer for Winsock tracing is that it does not load all the string resources so the messages displayed in the Description field (once you select an event) is sometimes hard to read (an argument that should be formatted as hex will be displayed in decimal, for example).</span></span> <span data-ttu-id="dc080-156">不過，您可以在 [事件描述] 中選取 [ **詳細資料** ] 索引標籤，以顯示原始 XML 記錄專案，這通常會更容易瞭解引數。</span><span class="sxs-lookup"><span data-stu-id="dc080-156">However, you can select the **Details** tab in the event description which shows the raw XML log entry which usually has easier to understand arguments.</span></span>

## <a name="interpreting-winsock-tracing-logs"></a><span data-ttu-id="dc080-157">解讀 Winsock 追蹤記錄</span><span class="sxs-lookup"><span data-stu-id="dc080-157">Interpreting Winsock Tracing Logs</span></span>

<span data-ttu-id="dc080-158">記錄檔中的所有 Winsock 追蹤事件都包含兩種類型的資訊：</span><span class="sxs-lookup"><span data-stu-id="dc080-158">All Winsock tracing events in a log contain two types of information:</span></span>

-   <span data-ttu-id="dc080-159">系統</span><span class="sxs-lookup"><span data-stu-id="dc080-159">System</span></span>
-   <span data-ttu-id="dc080-160">EventData</span><span class="sxs-lookup"><span data-stu-id="dc080-160">EventData</span></span>

<span data-ttu-id="dc080-161">系統資訊包含記錄層級、記錄專案的建立時間、代表事件種類的事件識別碼、執行處理常式識別碼、執行執行緒識別碼，以及其他系統資訊。</span><span class="sxs-lookup"><span data-stu-id="dc080-161">The system information contains the logging level, the time the log entry was created, the event ID that represents the event type, the execution Process ID, the execution Thread ID, and other system information.</span></span> <span data-ttu-id="dc080-162">Winsock 追蹤中的記錄層級4表示資訊事件記錄。</span><span class="sxs-lookup"><span data-stu-id="dc080-162">A log level of 4 in Winsock tracing represents information event logging.</span></span> <span data-ttu-id="dc080-163">Winsock 追蹤中的記錄層級5表示詳細的事件記錄。</span><span class="sxs-lookup"><span data-stu-id="dc080-163">A log level of 5 in Winsock tracing represents verbose event logging.</span></span>

<span data-ttu-id="dc080-164">系統資訊中的執行程式識別碼和執行緒識別碼，表示發生事件時正在執行的進程和執行緒。</span><span class="sxs-lookup"><span data-stu-id="dc080-164">The execution process ID and thread ID in the system information indicates the process and thread that was running when the event occurred.</span></span> <span data-ttu-id="dc080-165">在許多情況下，這將代表核心或背景工作執行緒和進程，而不是使用者模式執行緒和或應用程式的處理常式。</span><span class="sxs-lookup"><span data-stu-id="dc080-165">In many cases, this will represent a kernel or worker thread and process, not a user-mode thread and or the process of the application.</span></span> <span data-ttu-id="dc080-166">因此，此欄位通常不太實用。</span><span class="sxs-lookup"><span data-stu-id="dc080-166">So this field is normally not very useful.</span></span>

<span data-ttu-id="dc080-167">每個 Winsock 追蹤事件種類在記錄資料的系統區段中都有唯一的事件識別碼。</span><span class="sxs-lookup"><span data-stu-id="dc080-167">Each Winsock tracing event type has a unique event ID in the system section of the logged data.</span></span> <span data-ttu-id="dc080-168">這些事件識別碼很容易用來篩選特定 Winsock 追蹤事件的記錄檔。</span><span class="sxs-lookup"><span data-stu-id="dc080-168">These event IDs can easily be used to filter a log file for specific Winsock tracing events.</span></span>

<span data-ttu-id="dc080-169">Eventdata 包含事件種類的特定資訊。</span><span class="sxs-lookup"><span data-stu-id="dc080-169">The eventdata contains information specific to the event type.</span></span>

<span data-ttu-id="dc080-170">Eventdata 資訊中的 Process 參數是進程的核心 EPROCESS 結構位址，而不是實際的 PID。</span><span class="sxs-lookup"><span data-stu-id="dc080-170">The Process parameter in the eventdata information is the kernel EPROCESS structure address for the process, not the actual PID.</span></span> <span data-ttu-id="dc080-171">若要比對事件與使用者模式 PID，請從任何記錄專案的 eventdata 資訊中取得處理常式值，然後在記錄檔中查看具有處理常式值的通訊端建立事件。</span><span class="sxs-lookup"><span data-stu-id="dc080-171">To match an event to the user mode PID, take the Process value from the eventdata information from any log entry and look earlier in the log for a socket creation event with the Process value.</span></span> <span data-ttu-id="dc080-172">找到相符專案之後，通訊端建立事件資料中的最後一個參數就是建立通訊端的使用者模式處理序識別碼。</span><span class="sxs-lookup"><span data-stu-id="dc080-172">Once a match is found, the last parameter in the socket creation event data is the user-mode Process ID that created the socket.</span></span>

<span data-ttu-id="dc080-173">在某些 Winsock 追蹤事件中，會傳回 eventdata 資訊中的位址參數。</span><span class="sxs-lookup"><span data-stu-id="dc080-173">An Address parameter in the eventdata information is returned in some Winsock tracing events.</span></span> <span data-ttu-id="dc080-174">Address 參數代表 IP 位址，但會顯示在 **tracerpt.exe** 工具所建立的文字檔中，或是以原始位元組或數位事件檢視器。</span><span class="sxs-lookup"><span data-stu-id="dc080-174">An Address parameter represents an IP address, but it is displayed in the text file created by the **tracerpt.exe** tool or in Event Viewer as raw bytes or a number.</span></span> <span data-ttu-id="dc080-175">IPv6 位址會以十六進位顯示，因此更容易瞭解。</span><span class="sxs-lookup"><span data-stu-id="dc080-175">IPv6 addresses are displayed in hexadecimal, so they are more easily understood.</span></span> <span data-ttu-id="dc080-176">IPv4 位址會顯示為大十進位數。</span><span class="sxs-lookup"><span data-stu-id="dc080-176">IPv4 addresses are displayed as a large decimal number.</span></span> <span data-ttu-id="dc080-177">開發人員必須以手動方式將 IPv4 位址的未經處理位元組轉換成較熟悉的 IPv4 小數點位址標記法，以便更容易解讀此值。</span><span class="sxs-lookup"><span data-stu-id="dc080-177">Developers will need to manually convert the raw bytes of an IPv4 address to the more familiar IPv4 dotted-decimal address notation to be better able to interpret the value.</span></span>

<span data-ttu-id="dc080-178">在某些 Winsock 追蹤事件中，會傳回 eventdata 中的錯誤參數。</span><span class="sxs-lookup"><span data-stu-id="dc080-178">An Error parameter in the eventdata is returned in some Winsock tracing events.</span></span> <span data-ttu-id="dc080-179">錯誤參數的格式為 NTSTATUS 或 HRESULT 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="dc080-179">An Error parameter is of the form of an NTSTATUS or HRESULT error code.</span></span> <span data-ttu-id="dc080-180">這個錯誤參數會顯示在 **tracerpt.exe** 工具所建立的文字檔中，或事件檢視器為十進位數。</span><span class="sxs-lookup"><span data-stu-id="dc080-180">This error parameter is displayed in the text file created by the **tracerpt.exe** tool or in Event Viewer as a decimal number.</span></span> <span data-ttu-id="dc080-181">開發人員必須手動將十進位數轉換成十六進位數位，以便在某些情況下更清楚地解讀錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="dc080-181">Developers will need to manually convert the decimal number to a hex number in order to better interpret the error code in some cases.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dc080-182">相關主題</span><span class="sxs-lookup"><span data-stu-id="dc080-182">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dc080-183">Winsock 追蹤</span><span class="sxs-lookup"><span data-stu-id="dc080-183">Winsock Tracing</span></span>](winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="dc080-184">Winsock 目錄變更追蹤詳細資料</span><span class="sxs-lookup"><span data-stu-id="dc080-184">Winsock Catalog Change Tracing Details</span></span>](winsock-layered-service-provider-tracing-event-details.md)
</dt> <dt>

[<span data-ttu-id="dc080-185">Winsock 網路事件追蹤詳細資料</span><span class="sxs-lookup"><span data-stu-id="dc080-185">Winsock Network Event Tracing Details</span></span>](winsock-tracing-event-details.md)
</dt> <dt>

[<span data-ttu-id="dc080-186">Winsock 追蹤層級</span><span class="sxs-lookup"><span data-stu-id="dc080-186">Winsock Tracing Levels</span></span>](winsock-tracing-levels.md)
</dt> </dl>

 

 
