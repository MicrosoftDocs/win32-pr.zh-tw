---
title: 記錄和查看 TraceLogging 事件
description: 使用 Windows Performance Recorder (WPR 來記錄 TraceLogging 事件) 並使用 Windows Performance Analyzer (WPA) 加以查看。
ms.assetid: 906589FA-F48D-4105-9E56-1EC8B86542FB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09be054d274fc2c2c62635cc7bf12e8cf8acdef3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842684"
---
# <a name="record-and-view-tracelogging-events"></a><span data-ttu-id="ef972-103">記錄和查看 TraceLogging 事件</span><span class="sxs-lookup"><span data-stu-id="ef972-103">Record and View TraceLogging Events</span></span>

<span data-ttu-id="ef972-104">使用 Windows Performance Recorder (WPR 來記錄 TraceLogging 事件) 並使用 Windows Performance Analyzer (WPA) 加以查看。</span><span class="sxs-lookup"><span data-stu-id="ef972-104">Record TraceLogging events with the Windows Performance Recorder (WPR) and view them with the Windows Performance Analyzer (WPA).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="ef972-105">必要條件</span><span class="sxs-lookup"><span data-stu-id="ef972-105">Prerequisites</span></span>

-   <span data-ttu-id="ef972-106">Windows 10</span><span class="sxs-lookup"><span data-stu-id="ef972-106">Windows 10</span></span>
-   <span data-ttu-id="ef972-107">Windows 10 版的 Windows Performance Recorder (WPR) ，以及 Windows 10 Windows Performance Analyzer 的 (版本) WPA®，這是 Windows (評定及部署套件) Windows ADK 的一部分。</span><span class="sxs-lookup"><span data-stu-id="ef972-107">The Windows 10 version of Windows Performance Recorder (WPR), and the Windows 10 version of Windows Performance Analyzer (WPA) which is part of the Windows® Assessment and Deployment Kit (Windows ADK).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ef972-108">使用 TraceLogging 所捕捉的追蹤必須以 Windows Performance Recorder 的 Windows 10 版本來捕捉，並使用 Windows Performance Analyzer Windows 10 版本來查看。</span><span class="sxs-lookup"><span data-stu-id="ef972-108">Traces captured with TraceLogging must be captured with the Windows 10 version of Windows Performance Recorder and viewed with the Windows 10 version of Windows Performance Analyzer.</span></span> <span data-ttu-id="ef972-109">如果您無法捕捉或解碼您的事件，請確認您使用的是 Windows 10 版的工具。</span><span class="sxs-lookup"><span data-stu-id="ef972-109">If you are unable to capture or decode your events, verify that you are using the Windows 10 version of the tools.</span></span>

 

### <a name="1-capture-trace-data-with-wpr"></a><span data-ttu-id="ef972-110">1. 使用 WPR 來捕捉追蹤資料</span><span class="sxs-lookup"><span data-stu-id="ef972-110">1. Capture trace data with WPR</span></span>

<span data-ttu-id="ef972-111">若要在 Windows Phone 上捕捉追蹤，請參閱以下 Windows Phone 上的「捕捉 TraceLogging 事件」。</span><span class="sxs-lookup"><span data-stu-id="ef972-111">To capture a trace on Windows Phone, see Capture TraceLogging events on Windows Phone below.</span></span>

<span data-ttu-id="ef972-112">建立 Windows Performance Recorder 設定檔 (. wprp) 讓您可以使用 WPR 來捕捉 Tracelogging 事件。</span><span class="sxs-lookup"><span data-stu-id="ef972-112">Create a Windows Performance Recorder profile (.wprp) so that you can use WPR to capture your Tracelogging events.</span></span>

<span data-ttu-id="ef972-113">**建立。WPRP 檔案**</span><span class="sxs-lookup"><span data-stu-id="ef972-113">**Create a .WPRP file**</span></span>

1.  <span data-ttu-id="ef972-114">在 [TraceLogging C/c + + 快速入門](tracelogging-native-quick-start.md) 中使用原生程式碼範例，或 [TraceLogging managed 快速入門](tracelogging-managed-quick-start.md)中的 managed 範例，請使用下列 WPRP 範例。</span><span class="sxs-lookup"><span data-stu-id="ef972-114">Use the following WPRP example with the native code example in the [TraceLogging C/C++ Quick Start](tracelogging-native-quick-start.md) or the managed example in the [TraceLogging Managed Quick Start](tracelogging-managed-quick-start.md).</span></span> <span data-ttu-id="ef972-115">如果您是從自己的提供者記錄事件，請將 `TODO` 區段取代為提供者的適當值。</span><span class="sxs-lookup"><span data-stu-id="ef972-115">If you are logging events from your own provider, replace the `TODO` sections with the appropriate values for your provider.</span></span>

    > <span data-ttu-id="ef972-116">\[!重要\]</span><span class="sxs-lookup"><span data-stu-id="ef972-116">\[!Important\]</span></span>  

     

    <span data-ttu-id="ef972-117">如果您使用的是 TraceLogging C/c + + 快速入門，請在元素的屬性中指定提供者 GUID `Name` `<EventProvider>` 。</span><span class="sxs-lookup"><span data-stu-id="ef972-117">If you are using the TraceLogging C/C++ quick start, specify the provider GUID in the `Name` attribute of the `<EventProvider>` element.</span></span> <span data-ttu-id="ef972-118">例如：`<EventProvider Id="EventProvider_SimpleTraceLoggingProvider" Name="3970F9cf-2c0c-4f11-b1cc-e3a1e9958833" />`。</span><span class="sxs-lookup"><span data-stu-id="ef972-118">For example: `<EventProvider Id="EventProvider_SimpleTraceLoggingProvider" Name="3970F9cf-2c0c-4f11-b1cc-e3a1e9958833" />`.</span></span> <span data-ttu-id="ef972-119">如果您使用 managed TraceLogging 快速入門，請在專案的屬性中指定前面加上 ' ' 的提供者名稱 \* `Name` `<EventProvider />` 。</span><span class="sxs-lookup"><span data-stu-id="ef972-119">If you are using the managed TraceLogging quick start, specify the provider name prefaced by '\*' in the `Name` attribute of the `<EventProvider />` element.</span></span> <span data-ttu-id="ef972-120">例如： `<EventProvider Name="*SimpleTraceLoggingProvider" />` 。</span><span class="sxs-lookup"><span data-stu-id="ef972-120">For example, `<EventProvider Name="*SimpleTraceLoggingProvider" />`.</span></span>

    <span data-ttu-id="ef972-121">範例 WPRP 檔。</span><span class="sxs-lookup"><span data-stu-id="ef972-121">Sample WPRP file.</span></span>

    ```XML
    <?xml version="1.0" encoding="utf-8"?>
    <!-- TODO: 
    1. Find and replace "SimpleTraceLoggingProvider" with the name of your provider.
    2. See TODO below to update GUID for your event provider
    -->
    <WindowsPerformanceRecorder Version="1.0" Author="Microsoft Corporation" Copyright="Microsoft Corporation" Company="Microsoft Corporation">
      <Profiles>
        <EventCollector Id="EventCollector_SimpleTraceLoggingProvider" Name="SimpleTraceLoggingProvider">
          <BufferSize Value="64" />
          <Buffers Value="4" />
        </EventCollector>

        <!-- TODO: 
     1. Update Name attribute in EventProvider xml element with your provider GUID, eg: Name="3970F9cf-2c0c-4f11-b1cc-e3a1e9958833". Or
        if you specify an EventSource C# provider or call TraceLoggingRegister(...) without a GUID, use star (*) before your provider
        name, eg: Name="*MyEventSourceProvider" which will enable your provider appropriately.  
     2. This sample lists one EventProvider xml element and references it in a Profile with EventProviderId xml element. 
        For your component wprp, enable the required number of providers and fix the Profile xml element appropriately
    -->
        <EventProvider Id="EventProvider_SimpleTraceLoggingProvider" Name="*SimpleTraceLoggingProvider" />
        
        <Profile Id="SimpleTraceLoggingProvider.Verbose.File" Name="SimpleTraceLoggingProvider" Description="SimpleTraceLoggingProvider" LoggingMode="File" DetailLevel="Verbose">
          <Collectors>
            <EventCollectorId Value="EventCollector_SimpleTraceLoggingProvider">
              <EventProviders>
                <!-- TODO:
     1. Fix your EventProviderId with Value same as the Id attribute on EventProvider xml element above
    -->
                <EventProviderId Value="EventProvider_SimpleTraceLoggingProvider" />
              </EventProviders>
            </EventCollectorId>
          </Collectors>
        </Profile>

        <Profile Id="SimpleTraceLoggingProvider.Light.File" Name="SimpleTraceLoggingProvider" Description="SimpleTraceLoggingProvider" Base="SimpleTraceLoggingProvider.Verbose.File" LoggingMode="File" DetailLevel="Light" />
        <Profile Id="SimpleTraceLoggingProvider.Verbose.Memory" Name="SimpleTraceLoggingProvider" Description="SimpleTraceLoggingProvider" Base="SimpleTraceLoggingProvider.Verbose.File" LoggingMode="Memory" DetailLevel="Verbose" />
        <Profile Id="SimpleTraceLoggingProvider.Light.Memory" Name="SimpleTraceLoggingProvider" Description="SimpleTraceLoggingProvider" Base="SimpleTraceLoggingProvider.Verbose.File" LoggingMode="Memory" DetailLevel="Light" />

      </Profiles>
    </WindowsPerformanceRecorder>
    
    ```

    

2.  <span data-ttu-id="ef972-122">使用儲存檔案。WPRP 副檔名。</span><span class="sxs-lookup"><span data-stu-id="ef972-122">Save the file with a .WPRP file name extension.</span></span>
3.  <span data-ttu-id="ef972-123">從提高許可權的 ([以系統管理員身分執行]) 命令提示字元視窗中，使用 WPR 啟動 [捕獲]。</span><span class="sxs-lookup"><span data-stu-id="ef972-123">Start the capture using WPR from an elevated (run as Administrator) Command Prompt window.</span></span>

    <span data-ttu-id="ef972-124">**<path to wpr>\\wpr.exe-start GeneralProfile-start TraceLoggingProvider. wprp**</span><span class="sxs-lookup"><span data-stu-id="ef972-124">**<path to wpr>\\wpr.exe -start GeneralProfile -start TraceLoggingProvider.wprp**</span></span>

    > <span data-ttu-id="ef972-125">\[!提示\]</span><span class="sxs-lookup"><span data-stu-id="ef972-125">\[!Tip\]</span></span>  
    > <span data-ttu-id="ef972-126">針對一般分析用途，您也可以將 **– Start GeneralProfile** 新增至 wpr.exe 命令列，以捕捉系統事件以及來自提供者的事件。</span><span class="sxs-lookup"><span data-stu-id="ef972-126">For general profiling purposes, you can also add **–start GeneralProfile** to the wpr.exe command line to capture system events along with the events from your provider.</span></span> <span data-ttu-id="ef972-127">如果您只想要收集事件，請省略 **-Start GeneralProfile**。</span><span class="sxs-lookup"><span data-stu-id="ef972-127">If you only want to gather your events, omit **-start GeneralProfile**.</span></span>

     

4.  <span data-ttu-id="ef972-128">執行包含您事件的應用程式。</span><span class="sxs-lookup"><span data-stu-id="ef972-128">Run the application that contains your events.</span></span>
5.  <span data-ttu-id="ef972-129">停止追蹤捕捉。</span><span class="sxs-lookup"><span data-stu-id="ef972-129">Stop the trace capture.</span></span>

    <span data-ttu-id="ef972-130">**<path to wpr>\\wpr.exe-停止 TraceCaptureFile etl 描述**</span><span class="sxs-lookup"><span data-stu-id="ef972-130">**<path to wpr>\\wpr.exe -stop TraceCaptureFile.etl description**</span></span>

    > <span data-ttu-id="ef972-131">\[!提示\]</span><span class="sxs-lookup"><span data-stu-id="ef972-131">\[!Tip\]</span></span>  
    > <span data-ttu-id="ef972-132">如果您已新增 **–開始 GeneralProfile** 以收集系統事件，請將 **-stop GeneralProfile** 新增至上述 **wpr.exe** 命令列。</span><span class="sxs-lookup"><span data-stu-id="ef972-132">If you added **–start GeneralProfile** to gather system events, add **-stop GeneralProfile** to the **wpr.exe** command line above.</span></span>

     

### <a name="2-capture-tracelogging-events-on-windows-phone"></a><span data-ttu-id="ef972-133">2. 在 Windows Phone 上抓取 TraceLogging 事件</span><span class="sxs-lookup"><span data-stu-id="ef972-133">2. Capture TraceLogging events on Windows Phone</span></span>

<span id="capturephone"></span><span id="CAPTUREPHONE"></span>

1.  <span data-ttu-id="ef972-134">啟動 tracelog.exe 以從您的提供者捕獲事件。</span><span class="sxs-lookup"><span data-stu-id="ef972-134">Start tracelog to capture events from your provider.</span></span>

    <span data-ttu-id="ef972-135">**cmdd tracelog.exe-開始測試-f c： \\ test .etl-guid \# providerguid**</span><span class="sxs-lookup"><span data-stu-id="ef972-135">**cmdd tracelog -start test -f c:\\test.etl -guid \#providerguid**</span></span>

2.  <span data-ttu-id="ef972-136">執行您的測試案例以記錄事件。</span><span class="sxs-lookup"><span data-stu-id="ef972-136">Run your test scenario to log events.</span></span>
3.  <span data-ttu-id="ef972-137">停止追蹤捕捉。</span><span class="sxs-lookup"><span data-stu-id="ef972-137">Stop trace capture.</span></span>

    <span data-ttu-id="ef972-138">**cmdd tracelog.exe-停止測試**</span><span class="sxs-lookup"><span data-stu-id="ef972-138">**cmdd tracelog -stop test**</span></span>

4.  <span data-ttu-id="ef972-139">將系統追蹤結果與追蹤結果合併。</span><span class="sxs-lookup"><span data-stu-id="ef972-139">Merge the system trace results with your trace results.</span></span>

    <span data-ttu-id="ef972-140">**cmdd xperf-merge c： \\ test. etl c： \\ testmerged .etl**</span><span class="sxs-lookup"><span data-stu-id="ef972-140">**cmdd xperf -merge c:\\test.etl c:\\testmerged.etl**</span></span>

5.  <span data-ttu-id="ef972-141">取出合併的記錄檔。</span><span class="sxs-lookup"><span data-stu-id="ef972-141">Retrieve the merged log file.</span></span>

    <span data-ttu-id="ef972-142">**getd c： \\ testmerged .etl**</span><span class="sxs-lookup"><span data-stu-id="ef972-142">**getd c:\\testmerged.etl**</span></span>

### <a name="3-view-tracelogging-data-using-windows-performance-analyzer"></a><span data-ttu-id="ef972-143">3. 使用 Windows Performance Analyzer 來查看 TraceLogging 資料。</span><span class="sxs-lookup"><span data-stu-id="ef972-143">3. View TraceLogging data using Windows Performance Analyzer.</span></span>

<span data-ttu-id="ef972-144">WPA 目前是唯一可用來查看 TraceLogging 追蹤 ( etl) 檔案的檢視器。</span><span class="sxs-lookup"><span data-stu-id="ef972-144">WPA is currently the only viewer you can use to view TraceLogging trace (.etl) files.</span></span>

1.  <span data-ttu-id="ef972-145">啟動 WPA。</span><span class="sxs-lookup"><span data-stu-id="ef972-145">Start WPA.</span></span>

    <span data-ttu-id="ef972-146">**<path to wpr>\\wpa.exe traceLoggingResults**</span><span class="sxs-lookup"><span data-stu-id="ef972-146">**<path to wpr>\\wpa.exe traceLoggingResults.etl**</span></span>

2.  <span data-ttu-id="ef972-147">載入您在上述 wpa.exe 命令中指定的追蹤 ( .etl) 檔案，例如 traceLoggingResults。</span><span class="sxs-lookup"><span data-stu-id="ef972-147">Load the trace (.etl) file that you specified in the wpa.exe command above, e.g. traceLoggingResults.etl.</span></span>
3.  <span data-ttu-id="ef972-148">查看您的提供者事件。</span><span class="sxs-lookup"><span data-stu-id="ef972-148">View your provider events.</span></span> <span data-ttu-id="ef972-149">在 [WPA Graph Explorer] 中，展開 [ **系統活動**]。</span><span class="sxs-lookup"><span data-stu-id="ef972-149">In the WPA Graph Explorer, expand **System Activity**.</span></span>
4.  <span data-ttu-id="ef972-150">按兩下 [ **一般事件** ] 窗格，即可在 [ **分析** ] 窗格中查看事件。</span><span class="sxs-lookup"><span data-stu-id="ef972-150">Double-click in the **Generic Events** pane to view the events in the **Analysis** pane.</span></span>

    ![展開 [一般事件]](images/expandsystemactivity.png)

5.  <span data-ttu-id="ef972-152">在 [分析] 窗格中，找出提供者的事件，確認 TraceLogging 正常運作。</span><span class="sxs-lookup"><span data-stu-id="ef972-152">In the Analysis pane, locate the events from your provider to verify that TraceLogging is working.</span></span>

    <span data-ttu-id="ef972-153">在 [**一般事件**] 資料表的 [**提供者名稱**] 資料行中，尋找並選取具有提供者名稱的資料列。</span><span class="sxs-lookup"><span data-stu-id="ef972-153">In the **Provider Name** column of the **Generic Events** table, find and select the row with your provider name.</span></span>

    <span data-ttu-id="ef972-154">如果您有多個要排序的提供者，請按一下資料行標頭，依資料行名稱排序，這樣可讓您更輕鬆地尋找您的提供者。</span><span class="sxs-lookup"><span data-stu-id="ef972-154">If you have multiple providers to sort through, click the column header to sort by column name which may make it easier to find your provider.</span></span>

    <span data-ttu-id="ef972-155">當您找到您的提供者時，請在名稱上按一下滑鼠右鍵，然後選取 [ **篩選至選取專案**]。</span><span class="sxs-lookup"><span data-stu-id="ef972-155">When you find your provider, right click on the name and select **Filter to Selection**.</span></span>

    ![將選取範圍篩選至提供者](images/filtertoselection.png)

    <span data-ttu-id="ef972-157">SimpleTraceLoggingProvider 的事件和其值將會出現在 [分析] 視窗的下方窗格中。</span><span class="sxs-lookup"><span data-stu-id="ef972-157">The event for the SimpleTraceLoggingProvider and its value will appear in the bottom pane of the Analysis window.</span></span> <span data-ttu-id="ef972-158">展開 [提供者名稱] 以查看事件。</span><span class="sxs-lookup"><span data-stu-id="ef972-158">Expand the provider name to see the events.</span></span>

    ![從 simpletraceloggingprovider 查看活動](images/eventview.png)

    <span data-ttu-id="ef972-160">如需使用 WPA 的詳細資訊，請參閱 [Windows Performance Analyzer](/previous-versions/windows/it-pro/windows-8.1-and-8/hh448170(v=win.10))。</span><span class="sxs-lookup"><span data-stu-id="ef972-160">For more information about using WPA, see [Windows Performance Analyzer](/previous-versions/windows/it-pro/windows-8.1-and-8/hh448170(v=win.10)).</span></span>

## <a name="summary-and-next-steps"></a><span data-ttu-id="ef972-161">摘要和後續步驟</span><span class="sxs-lookup"><span data-stu-id="ef972-161">Summary and next steps</span></span>

<span data-ttu-id="ef972-162">使用 WPR 和 WPA 錄製和觀看 ETW 事件的程式同樣適用于 TraceLogging 事件。</span><span class="sxs-lookup"><span data-stu-id="ef972-162">The process for recording and viewing ETW events using WPR and WPA apply equally well to TraceLogging events.</span></span>

<span data-ttu-id="ef972-163">如需其他 TraceLogging 範例，請參閱 [c/c + + Tracelogging 範例](tracelogging-c-cpp-tracelogging-examples.md) 。</span><span class="sxs-lookup"><span data-stu-id="ef972-163">See [C/C++ Tracelogging Examples](tracelogging-c-cpp-tracelogging-examples.md) for additional TraceLogging examples.</span></span>

 

 