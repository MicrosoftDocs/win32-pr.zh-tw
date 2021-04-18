---
title: 查詢事件
description: 您可以查詢來自通道或記錄檔的事件。
ms.assetid: 929bedbf-6dce-428e-b2c0-de9dcfe4531b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6fa69f9b1308cd7ebbc4e4510692bb25ab031ec
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106968717"
---
# <a name="querying-for-events"></a><span data-ttu-id="41109-103">查詢事件</span><span class="sxs-lookup"><span data-stu-id="41109-103">Querying for Events</span></span>

<span data-ttu-id="41109-104">您可以查詢來自通道或記錄檔的事件。</span><span class="sxs-lookup"><span data-stu-id="41109-104">You can query for events from a channel or a log file.</span></span> <span data-ttu-id="41109-105">通道或記錄檔可以存在於本機電腦或遠端電腦上。</span><span class="sxs-lookup"><span data-stu-id="41109-105">The channel or log file can exist on the local computer or a remote computer.</span></span> <span data-ttu-id="41109-106">若要指定您要從通道或記錄檔取得的事件，您可以使用 XPath 查詢或結構 XML 查詢。</span><span class="sxs-lookup"><span data-stu-id="41109-106">To specify the events that you want to get from the channel or log file, you use an XPath query or a structure XML query.</span></span> <span data-ttu-id="41109-107">如需撰寫查詢的詳細資訊，請參閱 [使用事件](consuming-events.md)。</span><span class="sxs-lookup"><span data-stu-id="41109-107">For details on writing the query, see [Consuming Events](consuming-events.md).</span></span>

<span data-ttu-id="41109-108">若要查詢事件，請呼叫 [**EvtQuery**](/windows/desktop/api/WinEvt/nf-winevt-evtquery) 函數。</span><span class="sxs-lookup"><span data-stu-id="41109-108">To query events, call the [**EvtQuery**](/windows/desktop/api/WinEvt/nf-winevt-evtquery) function.</span></span> <span data-ttu-id="41109-109">您可以指定傳回事件的順序 (最舊的 (預設) 或最新的) ，以及是否容許查詢中格式不正確的 XPath 運算式 (如需函式如何忽略格式不正確的運算式的詳細資訊，請參閱 [**EvtQueryTolerateQueryErrors**](/windows/desktop/api/WinEvt/ne-winevt-evt_query_flags) 旗標) 。</span><span class="sxs-lookup"><span data-stu-id="41109-109">You can specify the order in which the events are returned (oldest to newest (the default) or newest to oldest) and whether to tolerate malformed XPath expressions in the query (for details on how the function ignores the malformed expressions, see the [**EvtQueryTolerateQueryErrors**](/windows/desktop/api/WinEvt/ne-winevt-evt_query_flags) flag).</span></span>

<span data-ttu-id="41109-110">下列範例顯示如何使用 XPath 運算式從通道查詢事件。</span><span class="sxs-lookup"><span data-stu-id="41109-110">The following example shows how to query events from a channel using an XPath expression.</span></span>


```C++
#include <windows.h>
#include <sddl.h>
#include <stdio.h>
#include <winevt.h>

#pragma comment(lib, "wevtapi.lib")

#define ARRAY_SIZE 10
#define TIMEOUT 1000  // 1 second; Set and use in place of INFINITE in EvtNext call

DWORD PrintResults(EVT_HANDLE hResults);
DWORD PrintEvent(EVT_HANDLE hEvent); // Shown in the Rendering Events topic

void main(void)
{
    DWORD status = ERROR_SUCCESS;
    EVT_HANDLE hResults = NULL;
    LPWSTR pwsPath = L"<Name of the channel goes here>";
    LPWSTR pwsQuery = L"Event/System[EventID=4]";

    hResults = EvtQuery(NULL, pwsPath, pwsQuery, EvtQueryChannelPath | EvtQueryReverseDirection);
    if (NULL == hResults)
    {
        status = GetLastError();

        if (ERROR_EVT_CHANNEL_NOT_FOUND == status)
            wprintf(L"The channel was not found.\n");
        else if (ERROR_EVT_INVALID_QUERY == status)
            // You can call the EvtGetExtendedStatus function to try to get 
            // additional information as to what is wrong with the query.
            wprintf(L"The query is not valid.\n");
        else
            wprintf(L"EvtQuery failed with %lu.\n", status);

        goto cleanup;
    }

    PrintResults(hResults);

cleanup:

    if (hResults)
        EvtClose(hResults);

}
```



<span data-ttu-id="41109-111">下列範例顯示如何使用結構化 XML 查詢從通道查詢事件。</span><span class="sxs-lookup"><span data-stu-id="41109-111">The following example shows how to query events from a channel using a structured XML query.</span></span> <span data-ttu-id="41109-112">從最新到最舊的順序傳回事件。</span><span class="sxs-lookup"><span data-stu-id="41109-112">The events are returned in order from newest to oldest.</span></span>


```C++
#include <windows.h>
#include <sddl.h>
#include <stdio.h>
#include <winevt.h>

#pragma comment(lib, "wevtapi.lib")

#define ARRAY_SIZE 10
#define TIMEOUT 1000  // 1 second; Set and use in place of INFINITE in EvtNext call

// The structured XML query.
#define QUERY \
    L"<QueryList>" \
    L"  <Query Path='Name of the channel goes here'>" \
    L"    <Select>Event/System[EventID=4]</Select>" \
    L"  </Query>" \
    L"</QueryList>"

DWORD PrintQueryStatuses(EVT_HANDLE hResults);
DWORD GetQueryStatusProperty(EVT_QUERY_PROPERTY_ID Id, EVT_HANDLE hResults, PEVT_VARIANT& pProperty);
DWORD PrintResults(EVT_HANDLE hResults);
DWORD PrintEvent(EVT_HANDLE hEvent);  // Shown in the Rendering Events topic

void main(void)
{
    DWORD status = ERROR_SUCCESS;
    EVT_HANDLE hResults = NULL;

    hResults = EvtQuery(NULL, NULL, QUERY, EvtQueryChannelPath | EvtQueryTolerateQueryErrors);
    if (NULL == hResults)
    {
        // Handle error.
        goto cleanup;
    }

    // Print the status of each query. If all the queries succeeded,
    // print the events in the result set. The status can be
    // ERROR_EVT_CHANNEL_NOT_FOUND or ERROR_EVT_INVALID_QUERY among others.
    if (ERROR_SUCCESS == PrintQueryStatuses(hResults))
        PrintResults(hResults);

cleanup:

    if (hResults)
        EvtClose(hResults);

}
```



<span data-ttu-id="41109-113">如果您使用結構化的 XML 查詢，並將 EvtQueryTolerateQueryErrors 旗標傳遞給 [**EvtQuery**](/windows/desktop/api/WinEvt/nf-winevt-evtquery)，即使結構化查詢中的一或多個查詢實際失敗，函式仍會成功。</span><span class="sxs-lookup"><span data-stu-id="41109-113">If you are using a structured XML query and pass the EvtQueryTolerateQueryErrors flag to [**EvtQuery**](/windows/desktop/api/WinEvt/nf-winevt-evtquery), the function succeeds even though one or more of the queries in the structured query may have actually failed.</span></span> <span data-ttu-id="41109-114">若要判斷結構化查詢中的哪些查詢成功或失敗，請呼叫 [**EvtGetQueryInfo**](/windows/desktop/api/WinEvt/nf-winevt-evtgetqueryinfo) 函數。</span><span class="sxs-lookup"><span data-stu-id="41109-114">To determine which queries in the structured query succeeded or failed, call the [**EvtGetQueryInfo**](/windows/desktop/api/WinEvt/nf-winevt-evtgetqueryinfo) function.</span></span> <span data-ttu-id="41109-115">如果您未傳遞 EvtQueryTolerateQueryErrors 旗標， **EvtQuery** 函式將會失敗，並出現在查詢中找到的第一個錯誤。</span><span class="sxs-lookup"><span data-stu-id="41109-115">If you do not pass the EvtQueryTolerateQueryErrors flag, the **EvtQuery** function will fail with the first error that it finds in the query.</span></span> <span data-ttu-id="41109-116">如果查詢失敗，並出現錯誤 \_ .Evt \_ 不正確 \_ 查詢，請呼叫 [**EvtGetExtendedStatus**](/windows/desktop/api/WinEvt/nf-winevt-evtgetextendedstatus) 函數來取得描述 XPath 錯誤的訊息字串。</span><span class="sxs-lookup"><span data-stu-id="41109-116">If the query fails with ERROR\_EVT\_INVALID\_QUERY, call the [**EvtGetExtendedStatus**](/windows/desktop/api/WinEvt/nf-winevt-evtgetextendedstatus) function to get a message string that describes the XPath error.</span></span>

<span data-ttu-id="41109-117">下列範例示範如何在將 EvtQueryTolerateQueryErrors 旗標傳遞給 [**EvtQuery**](/windows/desktop/api/WinEvt/nf-winevt-evtquery)時，判斷結構化查詢中每個查詢的成功或失敗。</span><span class="sxs-lookup"><span data-stu-id="41109-117">The following example shows how to determine the success or failure of each query in a structured query when passing the EvtQueryTolerateQueryErrors flag to [**EvtQuery**](/windows/desktop/api/WinEvt/nf-winevt-evtquery).</span></span>


```C++
// Get the list of paths in the query and the status for each path. Return
// the sum of the statuses, so the caller can decide whether to enumerate 
// the results.
DWORD PrintQueryStatuses(EVT_HANDLE hResults)
{
    DWORD status = ERROR_SUCCESS;
    PEVT_VARIANT pPaths = NULL;
    PEVT_VARIANT pStatuses = NULL;

    wprintf(L"List of channels/logs that were queried and their status\n\n");

    if (status = GetQueryStatusProperty(EvtQueryNames, hResults, pPaths))
        goto cleanup;

    if (status = GetQueryStatusProperty(EvtQueryStatuses, hResults, pStatuses))
        goto cleanup;

    for (DWORD i = 0; i < pPaths->Count; i++)
    {
        wprintf(L"%s (%lu)\n", pPaths->StringArr[i], pStatuses->UInt32Arr[i]);
        status += pStatuses->UInt32Arr[i];
    }

cleanup:

    if (pPaths)
        free(pPaths);

    if (pStatuses)
        free(pStatuses);

    return status;
}


// Get the list of paths specified in the query or the list of status values 
// for each path.
DWORD GetQueryStatusProperty(EVT_QUERY_PROPERTY_ID Id, EVT_HANDLE hResults, PEVT_VARIANT& pProperty)
{
    DWORD status = ERROR_SUCCESS;
    DWORD dwBufferSize = 0;
    DWORD dwBufferUsed = 0;

    if  (!EvtGetQueryInfo(hResults, Id, dwBufferSize, pProperty, &dwBufferUsed))
    {
        status = GetLastError();
        if (ERROR_INSUFFICIENT_BUFFER == status)
        {
            dwBufferSize = dwBufferUsed;
            pProperty = (PEVT_VARIANT)malloc(dwBufferSize);
            if (pProperty)
            {
                EvtGetQueryInfo(hResults, Id, dwBufferSize, pProperty, &dwBufferUsed);
            }
            else
            {
                wprintf(L"realloc failed\n");
                status = ERROR_OUTOFMEMORY;
                goto cleanup;
            }
        }

        if (ERROR_SUCCESS != (status = GetLastError()))
        {
            wprintf(L"EvtGetQueryInfo failed with %d\n", GetLastError());
            goto cleanup;
        }
    }

cleanup:

    return status;
}
```



## <a name="reading-events-from-the-result-set"></a><span data-ttu-id="41109-118">從結果集讀取事件</span><span class="sxs-lookup"><span data-stu-id="41109-118">Reading events from the result set</span></span>

<span data-ttu-id="41109-119">若要列舉結果集內的事件，請在迴圈中呼叫 [**EvtNext**](/windows/desktop/api/WinEvt/nf-winevt-evtnext) 函式，直到函數傳回 **FALSE** ，而 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 函式傳回錯誤的 \_ \_ \_ 專案。</span><span class="sxs-lookup"><span data-stu-id="41109-119">To enumerate the events in the result set, call the [**EvtNext**](/windows/desktop/api/WinEvt/nf-winevt-evtnext) function in a loop until the function returns **FALSE** and the [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function returns ERROR\_NO\_MORE\_ITEMS.</span></span> <span data-ttu-id="41109-120">結果集內的事件不是靜態的;寫入至通道的新事件會包含在結果集中，直到錯誤 \_ 未 \_ 設定任何專案為止 \_ 。</span><span class="sxs-lookup"><span data-stu-id="41109-120">The events in the result set are not static; new events that are written to the channel will be included in the result set until ERROR\_NO\_MORE\_ITEMS is set.</span></span> <span data-ttu-id="41109-121">為了改善效能，會以批次方式提取結果集的事件， (在判斷要提取) 的事件數目時，考慮每個事件的大小。</span><span class="sxs-lookup"><span data-stu-id="41109-121">To improve performance, fetch events from the result set in batches (taking into account the size of each event when determining the number of events to fetch).</span></span>

<span data-ttu-id="41109-122">下列範例顯示如何列舉結果集內的事件。</span><span class="sxs-lookup"><span data-stu-id="41109-122">The following example shows how to enumerate the events in a result set.</span></span>


```C++
// Enumerate all the events in the result set. 
DWORD PrintResults(EVT_HANDLE hResults)
{
    DWORD status = ERROR_SUCCESS;
    EVT_HANDLE hEvents[ARRAY_SIZE];
    DWORD dwReturned = 0;

    while (true)
    {
        // Get a block of events from the result set.
        if (!EvtNext(hResults, ARRAY_SIZE, hEvents, INFINITE, 0, &dwReturned))
        {
            if (ERROR_NO_MORE_ITEMS != (status = GetLastError()))
            {
                wprintf(L"EvtNext failed with %lu\n", status);
            }

            goto cleanup;
        }

        // For each event, call the PrintEvent function which renders the
        // event for display. PrintEvent is shown in RenderingEvents.
        for (DWORD i = 0; i < dwReturned; i++)
        {
            if (ERROR_SUCCESS == (status = PrintEvent(hEvents[i])))
            {
                EvtClose(hEvents[i]);
                hEvents[i] = NULL;
            }
            else
            {
                goto cleanup;
            }
        }
    }

cleanup:

    for (DWORD i = 0; i < dwReturned; i++)
    {
        if (NULL != hEvents[i])
            EvtClose(hEvents[i]);
    }

    return status;
}
```



<span data-ttu-id="41109-123">如需呈現從結果集取得之事件的詳細資訊，請參閱轉譯 [事件](rendering-events.md)。</span><span class="sxs-lookup"><span data-stu-id="41109-123">For details on rendering the events that you get from the result set, see [Rendering Events](rendering-events.md).</span></span>

<span data-ttu-id="41109-124">如果您想要從離開的地方查詢事件，請建立最後一個事件的書簽，並在下次執行查詢時使用它。</span><span class="sxs-lookup"><span data-stu-id="41109-124">If you want to query for events from where you left off, create a bookmark of the last event that you read and use it the next time you run your query.</span></span> <span data-ttu-id="41109-125">如需詳細資訊，請參閱將事件加上 [書簽](bookmarking-events.md)。</span><span class="sxs-lookup"><span data-stu-id="41109-125">For details, see [Bookmarking Events](bookmarking-events.md).</span></span>

 

 