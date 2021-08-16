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
ms.openlocfilehash: be29e4a1bd6721b8f53dbe2394be3552ca4845143cf948f130ef55e11881b518
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119589238"
---
# <a name="tracelogging-managed-quick-start"></a>TraceLogging 受控快速入門

下一節說明將 TraceLogging 新增至 managed 程式碼所需的基本步驟。

## <a name="prerequisites"></a>必要條件

-   Windows 10

### <a name="simpletraceloggingexamplecs"></a>SimpleTraceLoggingExample .cs

此範例示範如何記錄 Tracelogging 事件，而不需要手動建立個別的檢測資訊清單 XML 檔案。


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



### <a name="create-the-eventsource"></a>建立 EventSource

在您可以記錄事件之前，您必須先建立 EventSource 類別的實例。 第一個函式參數會識別此提供者的名稱。 系統會自動為您註冊提供者，如範例中所示。


```CSharp
        private static EventSource log = new EventSource("SimpleTraceLoggingProvider");
```



實例是靜態的，因為您的應用程式中一次只能有一個特定提供者的實例。

### <a name="log-tracelogging-events"></a>記錄 Tracelogging 事件

建立提供者之後，上述範例中的下列程式碼會記錄簡單事件。


```CSharp
            log.Write("Event 1"); // write an event with no fields
```



### <a name="log-structured-event-payload-data"></a>記錄結構化事件承載資料

您可以定義隨事件記錄的結構化承載資料。 以匿名型別的形式提供結構化承載資料，或以已標注屬性的類別實例形式提供， `[EventData]` 如下列範例所示。


```CSharp
            log.Write("Event 2", new { someEventData = DateTime.Now }); // Sending an anonymous type as event data

            ExampleStructuredData EventData = new ExampleStructuredData() { TransactionID = 1234, TransactionDate = DateTime.Now };
            log.Write("Event 3", EventData); // Sending a class decorated with [EventData] as event data
```



您必須將 `[EventData]` 屬性加入至您定義的事件裝載類別，如下所示。


```CSharp
    [EventData] // [EventData] makes it possible to pass an instance of the class as an argument to EventSource.Write()
    public sealed class ExampleStructuredData
    {
        public int TransactionID { get; set; }
        public DateTime TransactionDate { get; set; }
    }
```



屬性取代了手動建立資訊清單檔案以描述事件資料的需求。 現在您只需要將類別的實例傳遞給 EventSource。寫入 () 方法來記錄事件和對應的裝載資料。

## <a name="summary-and-next-steps"></a>摘要和後續步驟

如需如何使用 Windows 效能工具 (WPT) 的最新內部版本來捕捉和查看 TraceLogging 資料的相關資訊，請參閱[記錄和顯示 TraceLogging 事件](tracelogging-record-and-display-tracelogging-events.md)。

如需更多受控 TraceLogging 範例，請參閱 [.Net Tracelogging 範例](tracelogging-net-examples.md) 。

 

 




