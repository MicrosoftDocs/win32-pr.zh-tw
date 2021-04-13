---
title: .NET Tracelogging 範例
description: 本主題包含 managed 程式碼 Tracelogging 範例，說明如何只在會話詳細資訊層級為詳細資訊時記錄事件，以及如何記錄結構化的事件資料。
ms.assetid: 156016FE-FDC7-4361-BFD0-5F41254FE14D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8064f2ce139b5fd07bc74b3de6e107abeb958530
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311210"
---
# <a name="net-tracelogging-examples"></a><span data-ttu-id="b77d1-103">.NET Tracelogging 範例</span><span class="sxs-lookup"><span data-stu-id="b77d1-103">.NET Tracelogging Examples</span></span>

<span data-ttu-id="b77d1-104">本主題包含 managed 程式碼 Tracelogging 範例，說明如何只在會話詳細資訊層級為詳細資訊時記錄事件，以及如何記錄結構化的事件資料。</span><span class="sxs-lookup"><span data-stu-id="b77d1-104">This topic contains a managed code Tracelogging example that illustrates how to log an event only when the session verbosity level is verbose, and how to log structured event data.</span></span>


```CSharp
using System;
using System.Text;
using System.Diagnostics.Tracing;

namespace MoreSimpleTraceLoggingExamples
{
    class Program
    {
        private static EventSource log = new EventSource("SimpleTraceLoggingProvider", EventSourceSettings.EtwSelfDescribingEventFormat);

        static void Main(string[] args)
        {
            StringBuilder cmdLine = new StringBuilder();
            foreach (string arg in args)
            {
                cmdLine.AppendFormat("{0} ", arg);
            }

            // Log event verbosity level and opcode
            // This event is only logged when the session verbosity level is verbose.
            log.Write("CmdLine", new EventSourceOptions {Level=EventLevel.Verbose, Opcode=EventOpcode.Info }, 
                                 new { Args = cmdLine.ToString().TrimEnd() });

            try
            {
                int j = 0;
                int i = 1 / j;
            }
            catch (Exception e)
            {
                var error = new Error { ErrorTitle = e.Message, CallStack = e.StackTrace, ErrType = ErrorType.Exception };
                log.Write("Error", new { Error = error, ErrorType = e.ToString() });
            }
        }
    }

    [EventData] // [EventData] makes it possible to pass an instance of the class as an argument to EventSource.Write()
    public class Error
    {
        public string ErrorTitle { get; set; }
        public string CallStack { get; set; }
        public ErrorType ErrType { get; set; }
    }

    public enum ErrorType
    {
        Exception,
        UserError,
        ProgramError
    }
}
```



 

 




