---
description: NT Kernel 記錄器會話是一種事件追蹤會話，可記錄一組預先定義的核心事件。
ms.assetid: 3c4258d8-8073-4cc5-a29d-ce485a3fdc14
title: 設定和啟動 NT Kernel 記錄器會話
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a41398c9caac3ecd090af68a18bfb148095632d96b8c75eaaee7f04a551360fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119901218"
---
# <a name="configuring-and-starting-the-nt-kernel-logger-session"></a>設定和啟動 NT Kernel 記錄器會話

NT Kernel 記錄器會話是一種事件追蹤會話，可記錄一組預先定義的核心事件。 您不會呼叫 [**EnableTrace**](/windows/win32/api/evntrace/nf-evntrace-enabletrace) 函數來啟用核心提供者。 相反地，您可以使用 [**事件 \_ 追蹤 \_ 屬性**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)結構的 **EnableFlags** 成員來指定您要接收的核心事件。 [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea)函式會使用您指定的啟用旗標來啟用核心提供者。

只有一個 NT Kernel 記錄器會話。 如果會話已在使用中， [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) 函數會傳回錯誤 \_ \_ 。

如需啟動事件追蹤會話的詳細資訊，請參閱設定 [和啟動事件追蹤會話](configuring-and-starting-an-event-tracing-session.md)。

如需啟動私用記錄器會話的詳細資訊，請參閱設定 [和啟動私用記錄器會話](configuring-and-starting-a-private-logger-session.md)。

如需啟動全域記錄器會話的詳細資訊，請參閱設定 [和啟動全域記錄器會話](configuring-and-starting-the-global-logger-session.md)。

如需啟動自動記錄器會話的詳細資訊，請參閱設定 [和啟動自動記錄器會話](configuring-and-starting-an-autologger-session.md)。

下列範例示範如何設定和啟動 NT Kernel 記錄器會話，以收集網路 TCP/IP 核心事件，並將它們寫入至5MB 的迴圈檔案。


```C++
#define INITGUID  // Include this #define to use SystemTraceControlGuid in Evntrace.h.

#include <windows.h>
#include <stdio.h>
#include <conio.h>
#include <strsafe.h>
#include <wmistr.h>
#include <evntrace.h>

#define LOGFILE_PATH L"<FULLPATHTOTHELOGFILE.etl>"

void wmain(void)
{
    ULONG status = ERROR_SUCCESS;
    TRACEHANDLE SessionHandle = 0;
    EVENT_TRACE_PROPERTIES* pSessionProperties = NULL;
    ULONG BufferSize = 0;

    // Allocate memory for the session properties. The memory must
    // be large enough to include the log file name and session name,
    // which get appended to the end of the session properties structure.
    
    BufferSize = sizeof(EVENT_TRACE_PROPERTIES) + sizeof(LOGFILE_PATH) + sizeof(KERNEL_LOGGER_NAME);
    pSessionProperties = (EVENT_TRACE_PROPERTIES*) malloc(BufferSize);    
    if (NULL == pSessionProperties)
    {
        wprintf(L"Unable to allocate %d bytes for properties structure.\n", BufferSize);
        goto cleanup;
    }
    
    // Set the session properties. You only append the log file name
    // to the properties structure; the StartTrace function appends
    // the session name for you.

    ZeroMemory(pSessionProperties, BufferSize);
    pSessionProperties->Wnode.BufferSize = BufferSize;
    pSessionProperties->Wnode.Flags = WNODE_FLAG_TRACED_GUID;
    pSessionProperties->Wnode.ClientContext = 1; //QPC clock resolution
    pSessionProperties->Wnode.Guid = SystemTraceControlGuid; 
    pSessionProperties->EnableFlags = EVENT_TRACE_FLAG_NETWORK_TCPIP;
    pSessionProperties->LogFileMode = EVENT_TRACE_FILE_MODE_CIRCULAR;
    pSessionProperties->MaximumFileSize = 5;  // 5 MB
    pSessionProperties->LoggerNameOffset = sizeof(EVENT_TRACE_PROPERTIES);
    pSessionProperties->LogFileNameOffset = sizeof(EVENT_TRACE_PROPERTIES) + sizeof(KERNEL_LOGGER_NAME); 
    StringCbCopy((LPWSTR)((char*)pSessionProperties + pSessionProperties->LogFileNameOffset), sizeof(LOGFILE_PATH), LOGFILE_PATH);

    // Create the trace session.

    status = StartTrace((PTRACEHANDLE)&SessionHandle, KERNEL_LOGGER_NAME, pSessionProperties);

    if (ERROR_SUCCESS != status)
    {
        if (ERROR_ALREADY_EXISTS == status)
        {
            wprintf(L"The NT Kernel Logger session is already in use.\n");
        }
        else
        {
            wprintf(L"EnableTrace() failed with %lu\n", status);
        }

        goto cleanup;
    }

    wprintf(L"Press any key to end trace session ");
    _getch();

cleanup:

    if (SessionHandle)
    {
        status = ControlTrace(SessionHandle, KERNEL_LOGGER_NAME, pSessionProperties, EVENT_TRACE_CONTROL_STOP);

        if (ERROR_SUCCESS != status)
        {
            wprintf(L"ControlTrace(stop) failed with %lu\n", status);
        }
    }

    if (pSessionProperties)
        free(pSessionProperties);
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[設定和啟動私用記錄器會話](configuring-and-starting-a-private-logger-session.md)
</dt> <dt>

[設定並啟動 SystemTraceProvider 會話](configuring-and-starting-a-systemtraceprovider-session.md)
</dt> <dt>

[設定和啟動自動記錄器會話](configuring-and-starting-an-autologger-session.md)
</dt> <dt>

[設定和啟動事件追蹤會話](configuring-and-starting-an-event-tracing-session.md)
</dt> <dt>

[更新事件追蹤會話](updating-an-event-tracing-session.md)
</dt> </dl>

 

 
