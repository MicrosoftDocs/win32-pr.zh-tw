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
# <a name="record-and-view-tracelogging-events"></a>記錄和查看 TraceLogging 事件

使用 Windows Performance Recorder (WPR 來記錄 TraceLogging 事件) 並使用 Windows Performance Analyzer (WPA) 加以查看。

## <a name="prerequisites"></a>必要條件

-   Windows 10
-   Windows 10 版的 Windows Performance Recorder (WPR) ，以及 Windows 10 Windows Performance Analyzer 的 (版本) WPA®，這是 Windows (評定及部署套件) Windows ADK 的一部分。

> [!IMPORTANT]
> 使用 TraceLogging 所捕捉的追蹤必須以 Windows Performance Recorder 的 Windows 10 版本來捕捉，並使用 Windows Performance Analyzer Windows 10 版本來查看。 如果您無法捕捉或解碼您的事件，請確認您使用的是 Windows 10 版的工具。

 

### <a name="1-capture-trace-data-with-wpr"></a>1. 使用 WPR 來捕捉追蹤資料

若要在 Windows Phone 上捕捉追蹤，請參閱以下 Windows Phone 上的「捕捉 TraceLogging 事件」。

建立 Windows Performance Recorder 設定檔 (. wprp) 讓您可以使用 WPR 來捕捉 Tracelogging 事件。

**建立。WPRP 檔案**

1.  在 [TraceLogging C/c + + 快速入門](tracelogging-native-quick-start.md) 中使用原生程式碼範例，或 [TraceLogging managed 快速入門](tracelogging-managed-quick-start.md)中的 managed 範例，請使用下列 WPRP 範例。 如果您是從自己的提供者記錄事件，請將 `TODO` 區段取代為提供者的適當值。

    > \[!重要\]  

     

    如果您使用的是 TraceLogging C/c + + 快速入門，請在元素的屬性中指定提供者 GUID `Name` `<EventProvider>` 。 例如：`<EventProvider Id="EventProvider_SimpleTraceLoggingProvider" Name="3970F9cf-2c0c-4f11-b1cc-e3a1e9958833" />`。 如果您使用 managed TraceLogging 快速入門，請在專案的屬性中指定前面加上 ' ' 的提供者名稱 \* `Name` `<EventProvider />` 。 例如： `<EventProvider Name="*SimpleTraceLoggingProvider" />` 。

    範例 WPRP 檔。

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

    

2.  使用儲存檔案。WPRP 副檔名。
3.  從提高許可權的 ([以系統管理員身分執行]) 命令提示字元視窗中，使用 WPR 啟動 [捕獲]。

    **<path to wpr>\\wpr.exe-start GeneralProfile-start TraceLoggingProvider. wprp**

    > \[!提示\]  
    > 針對一般分析用途，您也可以將 **– Start GeneralProfile** 新增至 wpr.exe 命令列，以捕捉系統事件以及來自提供者的事件。 如果您只想要收集事件，請省略 **-Start GeneralProfile**。

     

4.  執行包含您事件的應用程式。
5.  停止追蹤捕捉。

    **<path to wpr>\\wpr.exe-停止 TraceCaptureFile etl 描述**

    > \[!提示\]  
    > 如果您已新增 **–開始 GeneralProfile** 以收集系統事件，請將 **-stop GeneralProfile** 新增至上述 **wpr.exe** 命令列。

     

### <a name="2-capture-tracelogging-events-on-windows-phone"></a>2. 在 Windows Phone 上抓取 TraceLogging 事件

<span id="capturephone"></span><span id="CAPTUREPHONE"></span>

1.  啟動 tracelog.exe 以從您的提供者捕獲事件。

    **cmdd tracelog.exe-開始測試-f c： \\ test .etl-guid \# providerguid**

2.  執行您的測試案例以記錄事件。
3.  停止追蹤捕捉。

    **cmdd tracelog.exe-停止測試**

4.  將系統追蹤結果與追蹤結果合併。

    **cmdd xperf-merge c： \\ test. etl c： \\ testmerged .etl**

5.  取出合併的記錄檔。

    **getd c： \\ testmerged .etl**

### <a name="3-view-tracelogging-data-using-windows-performance-analyzer"></a>3. 使用 Windows Performance Analyzer 來查看 TraceLogging 資料。

WPA 目前是唯一可用來查看 TraceLogging 追蹤 ( etl) 檔案的檢視器。

1.  啟動 WPA。

    **<path to wpr>\\wpa.exe traceLoggingResults**

2.  載入您在上述 wpa.exe 命令中指定的追蹤 ( .etl) 檔案，例如 traceLoggingResults。
3.  查看您的提供者事件。 在 [WPA Graph Explorer] 中，展開 [ **系統活動**]。
4.  按兩下 [ **一般事件** ] 窗格，即可在 [ **分析** ] 窗格中查看事件。

    ![展開 [一般事件]](images/expandsystemactivity.png)

5.  在 [分析] 窗格中，找出提供者的事件，確認 TraceLogging 正常運作。

    在 [**一般事件**] 資料表的 [**提供者名稱**] 資料行中，尋找並選取具有提供者名稱的資料列。

    如果您有多個要排序的提供者，請按一下資料行標頭，依資料行名稱排序，這樣可讓您更輕鬆地尋找您的提供者。

    當您找到您的提供者時，請在名稱上按一下滑鼠右鍵，然後選取 [ **篩選至選取專案**]。

    ![將選取範圍篩選至提供者](images/filtertoselection.png)

    SimpleTraceLoggingProvider 的事件和其值將會出現在 [分析] 視窗的下方窗格中。 展開 [提供者名稱] 以查看事件。

    ![從 simpletraceloggingprovider 查看活動](images/eventview.png)

    如需使用 WPA 的詳細資訊，請參閱 [Windows Performance Analyzer](/previous-versions/windows/it-pro/windows-8.1-and-8/hh448170(v=win.10))。

## <a name="summary-and-next-steps"></a>摘要和後續步驟

使用 WPR 和 WPA 錄製和觀看 ETW 事件的程式同樣適用于 TraceLogging 事件。

如需其他 TraceLogging 範例，請參閱 [c/c + + Tracelogging 範例](tracelogging-c-cpp-tracelogging-examples.md) 。

 

 