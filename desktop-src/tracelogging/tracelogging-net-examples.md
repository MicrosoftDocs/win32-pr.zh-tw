---
title: .NET Tracelogging 範例
description: 本主題包含 managed 程式碼 Tracelogging 範例，說明如何只在會話詳細資訊層級為詳細資訊時記錄事件，以及如何記錄結構化的事件資料。
ms.assetid: 156016FE-FDC7-4361-BFD0-5F41254FE14D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4346374974f450f11382f46f28ab1eda6c9ac891391ec0a565942e7918966c84
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118966517"
---
# <a name="net-tracelogging-examples"></a>.NET Tracelogging 範例

本主題包含 managed 程式碼 Tracelogging 範例，說明如何只在會話詳細資訊層級為詳細資訊時記錄事件，以及如何記錄結構化的事件資料。


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



 

 




