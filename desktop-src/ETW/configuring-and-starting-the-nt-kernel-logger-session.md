---
description: NT Kernel 記錄器會話是一種事件追蹤會話，可記錄一組預先定義的核心事件。
ms.assetid: 3c4258d8-8073-4cc5-a29d-ce485a3fdc14
title: 設定和啟動 NT Kernel 記錄器會話
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d13cb0d429bc4b0e01e02c33e2686040f0b7454b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973845"
---
# <a name="configuring-and-starting-the-nt-kernel-logger-session"></a><span data-ttu-id="1b178-103">設定和啟動 NT Kernel 記錄器會話</span><span class="sxs-lookup"><span data-stu-id="1b178-103">Configuring and Starting the NT Kernel Logger Session</span></span>

<span data-ttu-id="1b178-104">NT Kernel 記錄器會話是一種事件追蹤會話，可記錄一組預先定義的核心事件。</span><span class="sxs-lookup"><span data-stu-id="1b178-104">The NT Kernel Logger session is an event tracing session that records a predefined set of kernel events.</span></span> <span data-ttu-id="1b178-105">您不會呼叫 [**EnableTrace**](/windows/win32/api/evntrace/nf-evntrace-enabletrace) 函數來啟用核心提供者。</span><span class="sxs-lookup"><span data-stu-id="1b178-105">You do not call the [**EnableTrace**](/windows/win32/api/evntrace/nf-evntrace-enabletrace) function to enable the kernel providers.</span></span> <span data-ttu-id="1b178-106">相反地，您可以使用 [**事件 \_ 追蹤 \_ 屬性**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)結構的 **EnableFlags** 成員來指定您要接收的核心事件。</span><span class="sxs-lookup"><span data-stu-id="1b178-106">Instead, you use the **EnableFlags** member of [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure to specify the kernel events that you want to receive.</span></span> <span data-ttu-id="1b178-107">[**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea)函式會使用您指定的啟用旗標來啟用核心提供者。</span><span class="sxs-lookup"><span data-stu-id="1b178-107">The [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) function uses the enable flags that you specify to enable the kernel providers.</span></span>

<span data-ttu-id="1b178-108">只有一個 NT Kernel 記錄器會話。</span><span class="sxs-lookup"><span data-stu-id="1b178-108">There is only one NT Kernel Logger session.</span></span> <span data-ttu-id="1b178-109">如果會話已在使用中， [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) 函數會傳回錯誤 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="1b178-109">If the session is already in use, the [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) function returns ERROR\_ALREADY\_EXISTS.</span></span>

<span data-ttu-id="1b178-110">如需啟動事件追蹤會話的詳細資訊，請參閱設定 [和啟動事件追蹤會話](configuring-and-starting-an-event-tracing-session.md)。</span><span class="sxs-lookup"><span data-stu-id="1b178-110">For details on starting an event tracing session, see [Configuring and Starting an Event Tracing Session](configuring-and-starting-an-event-tracing-session.md).</span></span>

<span data-ttu-id="1b178-111">如需啟動私用記錄器會話的詳細資訊，請參閱設定 [和啟動私用記錄器會話](configuring-and-starting-a-private-logger-session.md)。</span><span class="sxs-lookup"><span data-stu-id="1b178-111">For details on starting a private logger session, see [Configuring and Starting a Private Logger Session](configuring-and-starting-a-private-logger-session.md).</span></span>

<span data-ttu-id="1b178-112">如需啟動全域記錄器會話的詳細資訊，請參閱設定 [和啟動全域記錄器會話](configuring-and-starting-the-global-logger-session.md)。</span><span class="sxs-lookup"><span data-stu-id="1b178-112">For details on starting a Global Logger session, see [Configuring and Starting the Global Logger Session](configuring-and-starting-the-global-logger-session.md).</span></span>

<span data-ttu-id="1b178-113">如需啟動自動記錄器會話的詳細資訊，請參閱設定 [和啟動自動記錄器會話](configuring-and-starting-an-autologger-session.md)。</span><span class="sxs-lookup"><span data-stu-id="1b178-113">For details on starting an AutoLogger session, see [Configuring and Starting an AutoLogger Session](configuring-and-starting-an-autologger-session.md).</span></span>

<span data-ttu-id="1b178-114">下列範例示範如何設定和啟動 NT Kernel 記錄器會話，以收集網路 TCP/IP 核心事件，並將它們寫入至5MB 的迴圈檔案。</span><span class="sxs-lookup"><span data-stu-id="1b178-114">The following example shows how to configure and start an NT Kernel Logger session that collects network TCP/IP kernel events and writes them to a 5MB circular file.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="1b178-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="1b178-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1b178-116">設定和啟動私用記錄器會話</span><span class="sxs-lookup"><span data-stu-id="1b178-116">Configuring and Starting a Private Logger Session</span></span>](configuring-and-starting-a-private-logger-session.md)
</dt> <dt>

[<span data-ttu-id="1b178-117">設定並啟動 SystemTraceProvider 會話</span><span class="sxs-lookup"><span data-stu-id="1b178-117">Configuring and Starting a SystemTraceProvider Session</span></span>](configuring-and-starting-a-systemtraceprovider-session.md)
</dt> <dt>

[<span data-ttu-id="1b178-118">設定和啟動自動記錄器會話</span><span class="sxs-lookup"><span data-stu-id="1b178-118">Configuring and Starting an AutoLogger Session</span></span>](configuring-and-starting-an-autologger-session.md)
</dt> <dt>

[<span data-ttu-id="1b178-119">設定和啟動事件追蹤會話</span><span class="sxs-lookup"><span data-stu-id="1b178-119">Configuring and Starting an Event Tracing Session</span></span>](configuring-and-starting-an-event-tracing-session.md)
</dt> <dt>

[<span data-ttu-id="1b178-120">更新事件追蹤會話</span><span class="sxs-lookup"><span data-stu-id="1b178-120">Updating an Event Tracing Session</span></span>](updating-an-event-tracing-session.md)
</dt> </dl>

 

 
