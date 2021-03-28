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
# <a name="updating-an-event-tracing-session"></a><span data-ttu-id="e557b-103">更新事件追蹤會話</span><span class="sxs-lookup"><span data-stu-id="e557b-103">Updating an Event Tracing Session</span></span>

<span data-ttu-id="e557b-104">若要更新事件追蹤會話的屬性，請使用 **事件 \_ 追蹤 \_ 控制項 \_ 更新** 控制程式代碼來呼叫 [**ControlTrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea)函數。</span><span class="sxs-lookup"><span data-stu-id="e557b-104">To update the properties of an event tracing session, call the [**ControlTrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea) function using the **EVENT\_TRACE\_CONTROL\_UPDATE** control code.</span></span> <span data-ttu-id="e557b-105">您可以使用從先前呼叫 [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea)或會話名稱取得的會話控制碼，來指定要更新的會話。</span><span class="sxs-lookup"><span data-stu-id="e557b-105">You can specify the session to update using a session handle obtained from an earlier call to [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea), or a session name.</span></span> <span data-ttu-id="e557b-106">事件追蹤會話的屬性會使用 [**事件 \_ 追蹤 \_ 屬性**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) 結構中指定的值來更新。</span><span class="sxs-lookup"><span data-stu-id="e557b-106">The properties of the event tracing session are updated using the values specified in the [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure.</span></span> <span data-ttu-id="e557b-107">您只能更新屬性的子集。</span><span class="sxs-lookup"><span data-stu-id="e557b-107">You can update only a subset of the properties.</span></span> <span data-ttu-id="e557b-108">如需可更新之屬性的清單，請參閱 **ControlTrace** 函數的 *properties* 參數。</span><span class="sxs-lookup"><span data-stu-id="e557b-108">For a list of the properties you can update, see the *Properties* parameter of the **ControlTrace** function.</span></span>

<span data-ttu-id="e557b-109">如果 [**ControlTrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea) 呼叫成功， [**事件 \_ 追蹤 \_ 屬性**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) 結構就會更新，以反映新的屬性值。</span><span class="sxs-lookup"><span data-stu-id="e557b-109">If the [**ControlTrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea) call is successful, the [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure is updated to reflect the new property values.</span></span> <span data-ttu-id="e557b-110">此結構也會包含事件追蹤會話的新執行統計資料。</span><span class="sxs-lookup"><span data-stu-id="e557b-110">The structure will also contain the new run statistics for the event tracing session.</span></span>

<span data-ttu-id="e557b-111">下列範例顯示如何更新核心事件追蹤會話。</span><span class="sxs-lookup"><span data-stu-id="e557b-111">The following example shows how to update the kernel event tracing session.</span></span> <span data-ttu-id="e557b-112">此範例會查詢目前的屬性值，並在更新會話之前更新結構。</span><span class="sxs-lookup"><span data-stu-id="e557b-112">The example queries for the current property values and updates the structure before updating the session.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="e557b-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="e557b-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e557b-114">設定和啟動私用記錄器會話</span><span class="sxs-lookup"><span data-stu-id="e557b-114">Configuring and Starting a Private Logger Session</span></span>](configuring-and-starting-a-private-logger-session.md)
</dt> <dt>

[<span data-ttu-id="e557b-115">設定並啟動 SystemTraceProvider 會話</span><span class="sxs-lookup"><span data-stu-id="e557b-115">Configuring and Starting a SystemTraceProvider Session</span></span>](configuring-and-starting-a-systemtraceprovider-session.md)
</dt> <dt>

[<span data-ttu-id="e557b-116">設定和啟動自動記錄器會話</span><span class="sxs-lookup"><span data-stu-id="e557b-116">Configuring and Starting an AutoLogger Session</span></span>](configuring-and-starting-an-autologger-session.md)
</dt> <dt>

[<span data-ttu-id="e557b-117">設定和啟動事件追蹤會話</span><span class="sxs-lookup"><span data-stu-id="e557b-117">Configuring and Starting an Event Tracing Session</span></span>](configuring-and-starting-an-event-tracing-session.md)
</dt> <dt>

[<span data-ttu-id="e557b-118">設定和啟動 NT Kernel 記錄器會話</span><span class="sxs-lookup"><span data-stu-id="e557b-118">Configuring and Starting the NT Kernel Logger Session</span></span>](configuring-and-starting-the-nt-kernel-logger-session.md)
</dt> </dl>

 

 
