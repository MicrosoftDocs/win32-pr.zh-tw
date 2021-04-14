---
title: 使用 Netsh 來管理追蹤
description: 在 Windows 7 中，您可以從命令提示字元使用 netsh.exe 來啟用和設定網路追蹤。 本節說明一些可協助疑難排解追蹤問題的 netsh.exe 命令，包括新的 netsh 追蹤功能。
ms.assetid: f0f0fc7b-7cfa-43c7-89a3-3b80050875f8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1978345da984ac90699b5355b36af18b9b285d5c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372259"
---
# <a name="using-netsh-to-manage-traces"></a><span data-ttu-id="25d00-104">使用 Netsh 來管理追蹤</span><span class="sxs-lookup"><span data-stu-id="25d00-104">Using Netsh to Manage Traces</span></span>

<span data-ttu-id="25d00-105">在 Windows 7 中，您可以從命令提示字元使用 netsh.exe 來啟用和設定網路追蹤。</span><span class="sxs-lookup"><span data-stu-id="25d00-105">In Windows 7, netsh.exe can be used from a command prompt to enable and configure network traces.</span></span> <span data-ttu-id="25d00-106">本節說明一些可協助疑難排解追蹤問題的 netsh.exe 命令，包括新的 **netsh 追蹤** 功能。</span><span class="sxs-lookup"><span data-stu-id="25d00-106">This section describes some of the netsh.exe commands which can help in troubleshooting tracing issues, including the new **netsh trace** functionality.</span></span> <span data-ttu-id="25d00-107">請注意，您必須從提升許可權的命令提示字元執行 netsh 命令。</span><span class="sxs-lookup"><span data-stu-id="25d00-107">Note that the netsh commands must be run from an elevated command prompt.</span></span>

## <a name="collecting-traces"></a><span data-ttu-id="25d00-108">收集追蹤</span><span class="sxs-lookup"><span data-stu-id="25d00-108">Collecting traces</span></span>

<span data-ttu-id="25d00-109">案例是預先定義的追蹤提供者集合，可加以啟用以進行疑難排解。</span><span class="sxs-lookup"><span data-stu-id="25d00-109">Scenarios are predefined sets of trace providers which can be enabled for troubleshooting.</span></span> <span data-ttu-id="25d00-110">若要顯示可用的網路相關案例清單，請輸入 **netsh trace show 案例** (**netsh trace show provider** 會列出每一個可用的提供者，包括與網路) 無關的提供者。</span><span class="sxs-lookup"><span data-stu-id="25d00-110">To display the list of available network-related scenarios, type **netsh trace show scenarios** (**netsh trace show providers** lists every one of the available providers, including ones that are not relevant to networking).</span></span>

<span data-ttu-id="25d00-111">當您識別出與問題相關的案例時，您可以看到該案例中包含的所有提供者清單。</span><span class="sxs-lookup"><span data-stu-id="25d00-111">When you have identified a scenario that looks relevant to your issues, you can see a list of all of the providers included in that scenario.</span></span> <span data-ttu-id="25d00-112">例如，若要查看在 InternetClient 案例下啟用的所有提供者，請輸入 **netsh trace show 案例 InternetClient**。</span><span class="sxs-lookup"><span data-stu-id="25d00-112">For example, to see all of the providers enabled under the InternetClient scenario, type **netsh trace show scenario internetclient**.</span></span>

<span data-ttu-id="25d00-113">您可以針對指定案例或一組案例中的所有提供者啟動追蹤。</span><span class="sxs-lookup"><span data-stu-id="25d00-113">You can start a trace for all of the providers in a given scenario or set of scenarios.</span></span> <span data-ttu-id="25d00-114">例如，若要針對在 InternetClient 案例下啟用的所有提供者啟動追蹤，請輸入 **netsh trace start 情節 = InternetClient**。</span><span class="sxs-lookup"><span data-stu-id="25d00-114">For example, to start a trace for all of the providers enabled under the InternetClient scenario, type **netsh trace start scenario=internetclient**.</span></span> <span data-ttu-id="25d00-115">若要為多個案例捕捉提供者，您可以指定所有適當的案例，例如 **netsh trace start 情節 = 可共用的案例 = DirectAccess**。</span><span class="sxs-lookup"><span data-stu-id="25d00-115">To capture providers for more than one scenario, you can specify all of the appropriate scenarios, such as **netsh trace start scenario=FileSharing scenario=DirectAccess**.</span></span> <span data-ttu-id="25d00-116">請注意，一次只能啟用一個追蹤會話;在不同的檔案中，不可能同時從不同的提供者集合中捕捉追蹤資訊。</span><span class="sxs-lookup"><span data-stu-id="25d00-116">Note that only one tracing session may be enabled at a time; it is not possible to simultaneously capture trace information from different sets of providers in separate files.</span></span>

<span data-ttu-id="25d00-117">您也可以針對未包含在該特定案例中的其他提供者啟動追蹤。</span><span class="sxs-lookup"><span data-stu-id="25d00-117">You can also start a trace for additional providers not included in that particular scenario.</span></span> <span data-ttu-id="25d00-118">例如，您可能想要針對在 WLAN 案例和 DHCP 提供者下啟用的所有提供者啟動追蹤。</span><span class="sxs-lookup"><span data-stu-id="25d00-118">For example, you might want to start traces for all of the providers enabled under the WLAN scenario and also the DHCP provider.</span></span> <span data-ttu-id="25d00-119">若要這樣做，請輸入 **netsh trace start 情節 = wlan 提供者 = Microsoft-Windows-Dhcp-Client**。</span><span class="sxs-lookup"><span data-stu-id="25d00-119">To do this, type **netsh trace start scenario=wlan provider=Microsoft-Windows-Dhcp-Client**.</span></span>

<span data-ttu-id="25d00-120">您也可以輸入 **netsh trace show provider** ，後面接著提供者名稱，以查看特定提供者的更多詳細資料。</span><span class="sxs-lookup"><span data-stu-id="25d00-120">You can also see more details about a specific provider by typing **netsh trace show provider** followed by the provider name.</span></span>

<span data-ttu-id="25d00-121">若要查看所有可用的選項和篩選，您可以輸入 **netsh trace start/？**。</span><span class="sxs-lookup"><span data-stu-id="25d00-121">To see all of the options and filters available you can type **netsh trace start /?**.</span></span>

<span data-ttu-id="25d00-122">若要停止追蹤，請輸入 **netsh trace stop**。</span><span class="sxs-lookup"><span data-stu-id="25d00-122">To stop tracing, type **netsh trace stop**.</span></span>

## <a name="using-the-output-files"></a><span data-ttu-id="25d00-123">使用輸出檔案</span><span class="sxs-lookup"><span data-stu-id="25d00-123">Using the output files</span></span>

<span data-ttu-id="25d00-124">停止追蹤時，預設會產生兩個檔案：「事件追蹤」記錄檔 (ETL) 檔和 .cab 檔。</span><span class="sxs-lookup"><span data-stu-id="25d00-124">When tracing is stopped, two files are generated by default: an Event Trace Log (ETL) file and a .cab file.</span></span>

<span data-ttu-id="25d00-125">追蹤事件會收集在 ETL 檔案中，您可以使用網路監視器之類的工具來查看這些事件。</span><span class="sxs-lookup"><span data-stu-id="25d00-125">Trace events are collected in the ETL file, which can be viewed using tools such as Network Monitor.</span></span> <span data-ttu-id="25d00-126">ETL 檔案預設會命名為 nettrace，或者，您可以在啟動追蹤時包含 **tracefile = filename** ，以指定不同的名稱。</span><span class="sxs-lookup"><span data-stu-id="25d00-126">The ETL file will be named nettrace.etl by default, or you can specify a different name by including **tracefile=filename.etl** when starting the trace.</span></span>

<span data-ttu-id="25d00-127">.Cab 檔案包含有關系統上的軟體和硬體的豐富資訊，例如介面卡資訊、組建、作業系統和無線設定。</span><span class="sxs-lookup"><span data-stu-id="25d00-127">The .cab file contains rich information about the software and hardware on the system such as the adapter information, build, operating system, and wireless settings.</span></span> <span data-ttu-id="25d00-128">預設會將 .cab 檔案命名為 nettrace.cab，除非指定了其他名稱，如上所示。</span><span class="sxs-lookup"><span data-stu-id="25d00-128">The .cab file will be named nettrace.cab by default, unless another name was specified as indicated above.</span></span>

<span data-ttu-id="25d00-129">這個 .cab 檔將包含兩個檔案，這些檔案一律會有相同的名稱。</span><span class="sxs-lookup"><span data-stu-id="25d00-129">This .cab file will contain two files, which will always have the same name.</span></span> <span data-ttu-id="25d00-130">.Etl 是 nettrace 中所含相同資訊的另一份複本。</span><span class="sxs-lookup"><span data-stu-id="25d00-130">Report.etl is another copy of the same information included in nettrace.etl.</span></span> <span data-ttu-id="25d00-131">report.html 檔案包含追蹤事件和所收集其他資訊的其他資訊。</span><span class="sxs-lookup"><span data-stu-id="25d00-131">The report.html file includes additional information about the trace events and the other information collected.</span></span> <span data-ttu-id="25d00-132">若要接收最多可用的詳細資料，請在啟動追蹤時，包含命令 **report = yes** 。</span><span class="sxs-lookup"><span data-stu-id="25d00-132">To receive the most details available, include the command **report = yes** when starting a trace.</span></span>

## <a name="using-filters-to-reduce-the-amount-of-data-in-the-etl-trace-file"></a><span data-ttu-id="25d00-133">使用篩選器減少 ETL 追蹤檔中的資料量</span><span class="sxs-lookup"><span data-stu-id="25d00-133">Using filters to reduce the amount of data in the ETL trace file</span></span>

<span data-ttu-id="25d00-134">當捕捉經過很長一段時間時，ETL 追蹤檔案可能會變得非常大。</span><span class="sxs-lookup"><span data-stu-id="25d00-134">When captures happen over a long period of time, the ETL trace file can become very large.</span></span> <span data-ttu-id="25d00-135">在啟用多個提供者的情況下，會產生高流量，ETW 緩衝區條件約束可能會導致某些追蹤被捨棄。</span><span class="sxs-lookup"><span data-stu-id="25d00-135">In scenarios where multiple providers are enabled, resulting in high traffic, ETW buffer constraints may cause some traces to be dropped.</span></span> <span data-ttu-id="25d00-136">除了這項考慮之外，減少 ETL 追蹤檔中的資料量可讓您藉由減少要檢查的資料量來更輕鬆進行疑難排解。</span><span class="sxs-lookup"><span data-stu-id="25d00-136">Aside from this consideration, reducing the amount of data in the ETL trace file can help make troubleshooting easier by reducing the amount of data to review.</span></span>

<span data-ttu-id="25d00-137">您可以使用 Netsh 追蹤篩選器來減少 ETL 追蹤檔案的大小。</span><span class="sxs-lookup"><span data-stu-id="25d00-137">Netsh trace filters can be used to reduce the ETL trace file size.</span></span> <span data-ttu-id="25d00-138">這些追蹤篩選器是可套用至個別提供者的 ETW 層級和關鍵字。</span><span class="sxs-lookup"><span data-stu-id="25d00-138">These trace filters are ETW levels and keywords that can be applied to individual providers.</span></span>

<span data-ttu-id="25d00-139">若要查看可以套用的篩選器清單，請輸入 **netsh trace start/？**</span><span class="sxs-lookup"><span data-stu-id="25d00-139">To see a list of filters which can be applied, type **netsh trace start /?**</span></span>

<span data-ttu-id="25d00-140">以下是一個篩選準則的範例 **： netsh trace Start InternetClient provider = Microsoft-Windows-TCPIP level = 5 關鍵字 =： ReceivePath，ui： SendPath**。</span><span class="sxs-lookup"><span data-stu-id="25d00-140">An example of a filter is **netsh trace start InternetClient provider=Microsoft-Windows-TCPIP level=5 keywords=ut:ReceivePath,ut:SendPath**.</span></span>

<span data-ttu-id="25d00-141">在此範例中，層級會設為5，這表示會顯示最大事件數目。</span><span class="sxs-lookup"><span data-stu-id="25d00-141">In this example, the level is set to 5, which means that the maximum number of events will be shown.</span></span> <span data-ttu-id="25d00-142">下表顯示可用的設定：</span><span class="sxs-lookup"><span data-stu-id="25d00-142">The following table shows the settings available:</span></span>



|       |               |                                                                            |
|-------|---------------|----------------------------------------------------------------------------|
| <span data-ttu-id="25d00-143">層級</span><span class="sxs-lookup"><span data-stu-id="25d00-143">Level</span></span> | <span data-ttu-id="25d00-144">設定</span><span class="sxs-lookup"><span data-stu-id="25d00-144">Setting</span></span>       | <span data-ttu-id="25d00-145">描述</span><span class="sxs-lookup"><span data-stu-id="25d00-145">Description</span></span>                                                                |
| <span data-ttu-id="25d00-146">1</span><span class="sxs-lookup"><span data-stu-id="25d00-146">1</span></span>     | <span data-ttu-id="25d00-147">重大</span><span class="sxs-lookup"><span data-stu-id="25d00-147">Critical</span></span>      | <span data-ttu-id="25d00-148">只會顯示重大事件。</span><span class="sxs-lookup"><span data-stu-id="25d00-148">Only critical events will be shown.</span></span>                                        |
| <span data-ttu-id="25d00-149">2</span><span class="sxs-lookup"><span data-stu-id="25d00-149">2</span></span>     | <span data-ttu-id="25d00-150">Errors</span><span class="sxs-lookup"><span data-stu-id="25d00-150">Errors</span></span>        | <span data-ttu-id="25d00-151">將會顯示重大事件和錯誤。</span><span class="sxs-lookup"><span data-stu-id="25d00-151">Critical events and errors will be shown.</span></span>                                  |
| <span data-ttu-id="25d00-152">3</span><span class="sxs-lookup"><span data-stu-id="25d00-152">3</span></span>     | <span data-ttu-id="25d00-153">警告</span><span class="sxs-lookup"><span data-stu-id="25d00-153">Warnings</span></span>      | <span data-ttu-id="25d00-154">將會顯示重大事件、錯誤和警告。</span><span class="sxs-lookup"><span data-stu-id="25d00-154">Critical events, errors, and warnings will be shown.</span></span>                       |
| <span data-ttu-id="25d00-155">4</span><span class="sxs-lookup"><span data-stu-id="25d00-155">4</span></span>     | <span data-ttu-id="25d00-156">資訊</span><span class="sxs-lookup"><span data-stu-id="25d00-156">Informational</span></span> | <span data-ttu-id="25d00-157">將會顯示重大事件、錯誤、警告和資訊事件。</span><span class="sxs-lookup"><span data-stu-id="25d00-157">Critical events, errors, warnings, and informational events will be shown.</span></span> |
| <span data-ttu-id="25d00-158">5</span><span class="sxs-lookup"><span data-stu-id="25d00-158">5</span></span>     | <span data-ttu-id="25d00-159">「詳細資訊」</span><span class="sxs-lookup"><span data-stu-id="25d00-159">Verbose</span></span>       | <span data-ttu-id="25d00-160">將會顯示所有事件。</span><span class="sxs-lookup"><span data-stu-id="25d00-160">All events will be shown.</span></span>                                                  |



 

<span data-ttu-id="25d00-161">關鍵字 **ReceivePath** 和 Ui **： SentPath** 會篩選事件，只顯示在接收或傳送路徑上追蹤的事件。</span><span class="sxs-lookup"><span data-stu-id="25d00-161">The keywords **ut:ReceivePath** and **ut:SentPath** filters the events to show only those events traced on the receive or send path.</span></span> <span data-ttu-id="25d00-162">輸入 **netsh trace show provider** ，後面接著提供者名稱，即可找到特定提供者的關鍵字完整清單。</span><span class="sxs-lookup"><span data-stu-id="25d00-162">A complete list of keywords for a specific provider can be found by typing **netsh trace show provider** followed by the provider name.</span></span> <span data-ttu-id="25d00-163">例如，輸入 **netsh trace show Provider microsoft-windows-tcpip** 將會顯示有關 MICROSOFT windows tcpip 提供者的資訊，包括關鍵字清單。</span><span class="sxs-lookup"><span data-stu-id="25d00-163">For example, typing **netsh trace show provider Microsoft-Windows-TCPIP** will display information about the Microsoft-Windows-TCPIP provider, including a list of keywords.</span></span>

<span data-ttu-id="25d00-164">Netsh 也支援封包篩選功能 (類似于網路監視器) 當封包捕捉開啟 (時，請設定 **[capture = yes]**) 。</span><span class="sxs-lookup"><span data-stu-id="25d00-164">Netsh also supports packet filtering capability (similar to Network Monitor) when packet capturing is turned on (by setting **capture = yes**).</span></span> <span data-ttu-id="25d00-165">您可以使用封包篩選，在追蹤檔案中捕捉有限數量的封包。</span><span class="sxs-lookup"><span data-stu-id="25d00-165">Packet filtering can be used to capture a limited number of packets in a trace file.</span></span> <span data-ttu-id="25d00-166">例如， **netsh trace start capture = yes ipv4. address = = x** . x. x，其中 X.X.X.X 是 IP 位址，只會以具有該特定來源或目的地位址的 ipv4 流量來捕捉封包。</span><span class="sxs-lookup"><span data-stu-id="25d00-166">For example, **netsh trace start capture = yes ipv4.address == x.x.x.x** , where x.x.x.x is the IP address, will only capture packets with ipv4 traffic with that specific source or destination address.</span></span>

<span data-ttu-id="25d00-167">如需有關如何使用封包篩選的詳細資訊，您可以輸入 **netsh trace Show capturefilterHelp**。</span><span class="sxs-lookup"><span data-stu-id="25d00-167">For additional information about how to use packet filtering, you can type **netsh trace show capturefilterHelp**.</span></span>

 

 




