---
title: TraceLogging 受控快速入門
description: 下一節說明將 TraceLogging 新增至 managed 程式碼所需的基本步驟。
ms.assetid: E144214D-8DCC-4263-8232-9F468C1A3CC0
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7108dfc094f3183950dd94e5398263f4bf7cfd5c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300667"
---
# <a name="tracelogging-managed-quick-start"></a><span data-ttu-id="3c3f0-103">TraceLogging 受控快速入門</span><span class="sxs-lookup"><span data-stu-id="3c3f0-103">TraceLogging Managed Quick Start</span></span>

<span data-ttu-id="3c3f0-104">下一節說明將 TraceLogging 新增至 managed 程式碼所需的基本步驟。</span><span class="sxs-lookup"><span data-stu-id="3c3f0-104">The following section describes the basic steps required to add TraceLogging to managed code.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="3c3f0-105">必要條件</span><span class="sxs-lookup"><span data-stu-id="3c3f0-105">Prerequisites</span></span>

-   <span data-ttu-id="3c3f0-106">Windows 10</span><span class="sxs-lookup"><span data-stu-id="3c3f0-106">Windows 10</span></span>

### <a name="simpletraceloggingexamplecs"></a><span data-ttu-id="3c3f0-107">SimpleTraceLoggingExample .cs</span><span class="sxs-lookup"><span data-stu-id="3c3f0-107">SimpleTraceLoggingExample.cs</span></span>

<span data-ttu-id="3c3f0-108">此範例示範如何記錄 Tracelogging 事件，而不需要手動建立個別的檢測資訊清單 XML 檔案。</span><span class="sxs-lookup"><span data-stu-id="3c3f0-108">This example demonstrates how to log Tracelogging events without the need to manually create a separate instrumentation manifest XML file.</span></span>


```CSharp
using System;
using System.Diagnostics.Tracing;

namespace SimpleTraceLoggingExample
{
    class Program
    {
        private static EventSource log = new EventSource("SimpleTraceLoggingProvider");
        static void Main(string[] args)
        {
            log.Write("Event 1"); // write an event with no fields
            log.Write("Event 2", new { someEventData = DateTime.Now }); // Sending an anonymous type as event data

            ExampleStructuredData EventData = new ExampleStructuredData() { TransactionID = 1234, TransactionDate = DateTime.Now };
            log.Write("Event 3", EventData); // Sending a class decorated with [EventData] as event data
        }
    }

    [EventData] // [EventData] makes it possible to pass an instance of the class as an argument to EventSource.Write()
    public sealed class ExampleStructuredData
    {
        public int TransactionID { get; set; }
        public DateTime TransactionDate { get; set; }
    }
}
```



### <a name="create-the-eventsource"></a><span data-ttu-id="3c3f0-109">建立 EventSource</span><span class="sxs-lookup"><span data-stu-id="3c3f0-109">Create the EventSource</span></span>

<span data-ttu-id="3c3f0-110">在您可以記錄事件之前，您必須先建立 EventSource 類別的實例。</span><span class="sxs-lookup"><span data-stu-id="3c3f0-110">Before you can log events you must create an instance of the EventSource class.</span></span> <span data-ttu-id="3c3f0-111">第一個函式參數會識別此提供者的名稱。</span><span class="sxs-lookup"><span data-stu-id="3c3f0-111">The first constructor parameter identifies the name of this provider.</span></span> <span data-ttu-id="3c3f0-112">系統會自動為您註冊提供者，如範例中所示。</span><span class="sxs-lookup"><span data-stu-id="3c3f0-112">The provider is automatically registered for you as illustrated in the example.</span></span>


```CSharp
        private static EventSource log = new EventSource("SimpleTraceLoggingProvider");
```



<span data-ttu-id="3c3f0-113">實例是靜態的，因為您的應用程式中一次只能有一個特定提供者的實例。</span><span class="sxs-lookup"><span data-stu-id="3c3f0-113">The instance is static because there should only be one instance of a specific provider in your application at a time.</span></span>

### <a name="log-tracelogging-events"></a><span data-ttu-id="3c3f0-114">記錄 Tracelogging 事件</span><span class="sxs-lookup"><span data-stu-id="3c3f0-114">Log Tracelogging events</span></span>

<span data-ttu-id="3c3f0-115">建立提供者之後，上述範例中的下列程式碼會記錄簡單事件。</span><span class="sxs-lookup"><span data-stu-id="3c3f0-115">After the provider is created, the following code from the example above logs a simple event.</span></span>


```CSharp
            log.Write("Event 1"); // write an event with no fields
```



### <a name="log-structured-event-payload-data"></a><span data-ttu-id="3c3f0-116">記錄結構化事件承載資料</span><span class="sxs-lookup"><span data-stu-id="3c3f0-116">Log structured event payload data</span></span>

<span data-ttu-id="3c3f0-117">您可以定義隨事件記錄的結構化承載資料。</span><span class="sxs-lookup"><span data-stu-id="3c3f0-117">You can define structured payload data that is logged with the event.</span></span> <span data-ttu-id="3c3f0-118">以匿名型別的形式提供結構化承載資料，或以已標注屬性的類別實例形式提供， `[EventData]` 如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="3c3f0-118">Provide structured payload data either as an anonymous type or as an instance of a class that has been annotated with the `[EventData]` attribute as shown in the following example.</span></span>


```CSharp
            log.Write("Event 2", new { someEventData = DateTime.Now }); // Sending an anonymous type as event data

            ExampleStructuredData EventData = new ExampleStructuredData() { TransactionID = 1234, TransactionDate = DateTime.Now };
            log.Write("Event 3", EventData); // Sending a class decorated with [EventData] as event data
```



<span data-ttu-id="3c3f0-119">您必須將 `[EventData]` 屬性加入至您定義的事件裝載類別，如下所示。</span><span class="sxs-lookup"><span data-stu-id="3c3f0-119">You must add the `[EventData]` attribute to event payload classes that you define as shown below.</span></span>


```CSharp
    [EventData] // [EventData] makes it possible to pass an instance of the class as an argument to EventSource.Write()
    public sealed class ExampleStructuredData
    {
        public int TransactionID { get; set; }
        public DateTime TransactionDate { get; set; }
    }
```



<span data-ttu-id="3c3f0-120">屬性取代了手動建立資訊清單檔案以描述事件資料的需求。</span><span class="sxs-lookup"><span data-stu-id="3c3f0-120">The attribute replaces the need to manually create a manifest file to describe the event data.</span></span> <span data-ttu-id="3c3f0-121">現在您只需要將類別的實例傳遞給 EventSource。寫入 () 方法來記錄事件和對應的裝載資料。</span><span class="sxs-lookup"><span data-stu-id="3c3f0-121">Now all you have to do is pass an instance of the class to the EventSource.Write() method to log the event and corresponding payload data.</span></span>

## <a name="summary-and-next-steps"></a><span data-ttu-id="3c3f0-122">摘要和後續步驟</span><span class="sxs-lookup"><span data-stu-id="3c3f0-122">Summary and next steps</span></span>

<span data-ttu-id="3c3f0-123">如需有關如何使用 Windows 效能工具 (WPT) 的最新內部版本來捕捉和查看 TraceLogging 資料的詳細資訊，請參閱 [記錄和顯示 TraceLogging 事件](tracelogging-record-and-display-tracelogging-events.md) 。</span><span class="sxs-lookup"><span data-stu-id="3c3f0-123">See [Record and Display TraceLogging Events](tracelogging-record-and-display-tracelogging-events.md) for information about how to capture and view TraceLogging data using the latest internal versions of the Windows Performance Tools (WPT).</span></span>

<span data-ttu-id="3c3f0-124">如需更多受控 TraceLogging 範例，請參閱 [.Net Tracelogging 範例](tracelogging-net-examples.md) 。</span><span class="sxs-lookup"><span data-stu-id="3c3f0-124">See [.NET Tracelogging Examples](tracelogging-net-examples.md) for more managed TraceLogging examples.</span></span>

 

 




