---
description: 若要更新事件追蹤會話的屬性，請使用事件 \_ 追蹤 \_ 控制項 \_ 更新控制程式代碼來呼叫 ControlTrace 函數。
ms.assetid: 1496bf88-a989-4fa1-888a-90385c4ca8ee
title: 更新事件追蹤會話
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e580c2e84dec6682e5fad323fe0cad427300a21
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943616"
---
# <a name="updating-an-event-tracing-session"></a>更新事件追蹤會話

若要更新事件追蹤會話的屬性，請使用 **事件 \_ 追蹤 \_ 控制項 \_ 更新** 控制程式代碼來呼叫 [**ControlTrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea)函數。 您可以使用從先前呼叫 [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea)或會話名稱取得的會話控制碼，來指定要更新的會話。 事件追蹤會話的屬性會使用 [**事件 \_ 追蹤 \_ 屬性**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) 結構中指定的值來更新。 您只能更新屬性的子集。 如需可更新之屬性的清單，請參閱 **ControlTrace** 函數的 *properties* 參數。

如果 [**ControlTrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea) 呼叫成功， [**事件 \_ 追蹤 \_ 屬性**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) 結構就會更新，以反映新的屬性值。 此結構也會包含事件追蹤會話的新執行統計資料。

下列範例顯示如何更新核心事件追蹤會話。 此範例會查詢目前的屬性值，並在更新會話之前更新結構。


```C++
#include <windows.h>
#include <stdio.h>
#include <wmistr.h>
#include <evntrace.h>

#define MAX_SESSION_NAME_LEN 1024
#define MAX_LOGFILE_PATH_LEN 1024

void wmain(void)
{
    ULONG status = ERROR_SUCCESS;
    EVENT_TRACE_PROPERTIES* pSessionProperties = NULL;
    ULONG BufferSize = 0;

    // Allocate memory for the session properties. The memory must
    // be large enough to include the log file name and session name.
    // This example specifies the maximum size for the session name 
    // and log file name.
    
    BufferSize = sizeof(EVENT_TRACE_PROPERTIES) + 
        (MAX_SESSION_NAME_LEN * sizeof(WCHAR)) + 
        (MAX_LOGFILE_PATH_LEN * sizeof(WCHAR));

    pSessionProperties = (EVENT_TRACE_PROPERTIES*) malloc(BufferSize);    
    if (NULL == pSessionProperties)
    {
        wprintf(L"Unable to allocate %d bytes for properties structure.\n", BufferSize);
        goto cleanup;
    }
    
    ZeroMemory(pSessionProperties, BufferSize);
    pSessionProperties->Wnode.BufferSize = BufferSize;

    // Query for the kernel trace session's current property values.

    status = ControlTrace((TRACEHANDLE)NULL, KERNEL_LOGGER_NAME, pSessionProperties, EVENT_TRACE_CONTROL_QUERY);

    if (ERROR_SUCCESS != status)
    {
        if (ERROR_WMI_INSTANCE_NOT_FOUND == status)
        {
            wprintf(L"The Kernel Logger is not running.\n");
        }
        else
        {
            wprintf(L"ControlTrace(query) failed with %lu\n", status);
        }

        goto cleanup;
    }

    // Update the enable flags to also enable the Process and Thread providers.

    pSessionProperties->LogFileNameOffset = 0;  // Zero tells ETW not to update the file name
    pSessionProperties->Wnode.Flags = WNODE_FLAG_TRACED_GUID;
    pSessionProperties->EnableFlags |= EVENT_TRACE_FLAG_PROCESS | EVENT_TRACE_FLAG_THREAD;

    // Update the session's properties.

    status = ControlTrace((TRACEHANDLE)NULL, KERNEL_LOGGER_NAME, pSessionProperties, EVENT_TRACE_CONTROL_UPDATE);
    if (ERROR_SUCCESS != status)
    {
        wprintf(L"ControlTrace(update) failed with %lu.\n", status);
        goto cleanup;
    }

    wprintf(L"\nUpdated session");

cleanup:

    if (pSessionProperties)
    {
        free(pSessionProperties);
        pSessionProperties = NULL;
    }
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

[設定和啟動 NT Kernel 記錄器會話](configuring-and-starting-the-nt-kernel-logger-session.md)
</dt> </dl>

 

 
