---
title: 訂閱事件
description: 若要訂閱事件，請呼叫 EvtSubscribe 函數。
ms.assetid: 1e86deeb-fc59-4658-9353-e4ced7ace89a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0889c4ff440a17696fe6d908ff98d632ff7058ca
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106968702"
---
# <a name="subscribing-to-events"></a><span data-ttu-id="87bad-103">訂閱事件</span><span class="sxs-lookup"><span data-stu-id="87bad-103">Subscribing to Events</span></span>

<span data-ttu-id="87bad-104">若要訂閱事件，請呼叫 [**EvtSubscribe**](/windows/desktop/api/WinEvt/nf-winevt-evtsubscribe) 函數。</span><span class="sxs-lookup"><span data-stu-id="87bad-104">To subscribe to events, call the [**EvtSubscribe**](/windows/desktop/api/WinEvt/nf-winevt-evtsubscribe) function.</span></span> <span data-ttu-id="87bad-105">您可以從一或多個系統管理員或操作通道訂閱事件。</span><span class="sxs-lookup"><span data-stu-id="87bad-105">You can subscribe to events from one or more Admin or Operational channels.</span></span> <span data-ttu-id="87bad-106">通道可以存在於本機電腦或遠端電腦上。</span><span class="sxs-lookup"><span data-stu-id="87bad-106">The channel can exist on the local computer or a remote computer.</span></span> <span data-ttu-id="87bad-107">若要指定您要訂閱的事件，您可以使用 XPath 查詢或結構 XML 查詢。</span><span class="sxs-lookup"><span data-stu-id="87bad-107">To specify the events that you want to subscribe to, you can use an XPath query or a structure XML query.</span></span> <span data-ttu-id="87bad-108">如需撰寫查詢的詳細資訊，請參閱 [使用事件](consuming-events.md)。</span><span class="sxs-lookup"><span data-stu-id="87bad-108">For details on writing the query, see [Consuming Events](consuming-events.md).</span></span>

<span data-ttu-id="87bad-109">Windows 事件記錄檔為事件訂閱提供兩種模型：</span><span class="sxs-lookup"><span data-stu-id="87bad-109">Windows Event Log provides two models for event subscription:</span></span>

-   <span data-ttu-id="87bad-110">推送模型會以非同步方式將事件推送至您所執行的回呼。</span><span class="sxs-lookup"><span data-stu-id="87bad-110">The push model pushes events asynchronously to a callback that you implement.</span></span>
-   <span data-ttu-id="87bad-111">提取模型會使用您所建立的事件控制碼，在有符合您的查詢準則的事件可用時通知您。</span><span class="sxs-lookup"><span data-stu-id="87bad-111">The pull model uses an event handle that you create to signal you when there are events available that match your query criteria.</span></span> <span data-ttu-id="87bad-112">然後，您可以列舉結果集中的事件。</span><span class="sxs-lookup"><span data-stu-id="87bad-112">You then enumerate the events in the result set.</span></span>

<span data-ttu-id="87bad-113">您可以訂閱過去和未來的事件、僅限未來的事件，或是在加上書簽的事件之後的過去和未來事件。</span><span class="sxs-lookup"><span data-stu-id="87bad-113">You can subscribe to past and future events, future events only, or past and future events beginning after the bookmarked event.</span></span>

<span data-ttu-id="87bad-114">如需訂閱事件的詳細資訊，請參閱發送 [訂閱](#push-subscriptions) 或 [提取訂閱](#pull-subscriptions)。</span><span class="sxs-lookup"><span data-stu-id="87bad-114">For details on subscribing to events, see [Push Subscriptions](#push-subscriptions) or [Pull Subscriptions](#pull-subscriptions).</span></span>

<span data-ttu-id="87bad-115">如需呈現事件的詳細資訊，請參閱轉譯 [事件](rendering-events.md)。</span><span class="sxs-lookup"><span data-stu-id="87bad-115">For details on rendering the events, see [Rendering Events](rendering-events.md).</span></span>

<span data-ttu-id="87bad-116">如果您想要從您離開的地方訂閱事件，請在結束訂用帳戶之前建立書簽，然後在您下一次訂閱事件時使用它。</span><span class="sxs-lookup"><span data-stu-id="87bad-116">If you want to subscribe to events from where you left off, create a bookmark before ending your subscription and use it the next time you subscribe to events.</span></span> <span data-ttu-id="87bad-117">如需詳細資訊，請參閱將事件加上 [書簽](bookmarking-events.md)。</span><span class="sxs-lookup"><span data-stu-id="87bad-117">For details, see [Bookmarking Events](bookmarking-events.md).</span></span>

## <a name="push-subscriptions"></a><span data-ttu-id="87bad-118">發送訂閱</span><span class="sxs-lookup"><span data-stu-id="87bad-118">Push Subscriptions</span></span>

<span data-ttu-id="87bad-119">下列範例示範如何訂閱事件、執行訂用帳戶回呼，以及呈現事件。</span><span class="sxs-lookup"><span data-stu-id="87bad-119">The following example shows how to subscribe to events, implement the subscription callback, and render the events.</span></span>


```C++
#include <windows.h>
#include <conio.h>
#include <stdio.h>
#include <winevt.h>

#pragma comment(lib, "wevtapi.lib")

DWORD WINAPI SubscriptionCallback(EVT_SUBSCRIBE_NOTIFY_ACTION action, PVOID pContext, EVT_HANDLE hEvent);
DWORD PrintEvent(EVT_HANDLE hEvent);


void main(void)
{
    DWORD status = ERROR_SUCCESS;
    EVT_HANDLE hSubscription = NULL;
    LPWSTR pwsPath = L"<channel name goes here>";
    LPWSTR pwsQuery = L"<xpath query goes here>";

    // Subscribe to events beginning with the oldest event in the channel. The subscription
    // will return all current events in the channel and any future events that are raised
    // while the application is active.
    hSubscription = EvtSubscribe(NULL, NULL, pwsPath, pwsQuery, NULL, NULL, 
                                 (EVT_SUBSCRIBE_CALLBACK)SubscriptionCallback, EvtSubscribeStartAtOldestRecord);
    if (NULL == hSubscription)
    {
        status = GetLastError();

        if (ERROR_EVT_CHANNEL_NOT_FOUND == status)
            wprintf(L"Channel %s was not found.\n", pwsPath);
        else if (ERROR_EVT_INVALID_QUERY == status)
            // You can call EvtGetExtendedStatus to get information as to why the query is not valid.
            wprintf(L"The query \"%s\" is not valid.\n", pwsQuery);
        else
            wprintf(L"EvtSubscribe failed with %lu.\n", status);

        goto cleanup;
    }

    wprintf(L"Hit any key to quit\n\n");
    while (!_kbhit())
        Sleep(10);

cleanup:

    if (hSubscription)
        EvtClose(hSubscription);
}

// The callback that receives the events that match the query criteria. 
DWORD WINAPI SubscriptionCallback(EVT_SUBSCRIBE_NOTIFY_ACTION action, PVOID pContext, EVT_HANDLE hEvent)
{
    UNREFERENCED_PARAMETER(pContext);
    
    DWORD status = ERROR_SUCCESS;

    switch(action)
    {
        // You should only get the EvtSubscribeActionError action if your subscription flags 
        // includes EvtSubscribeStrict and the channel contains missing event records.
        case EvtSubscribeActionError:
            if (ERROR_EVT_QUERY_RESULT_STALE == (DWORD)hEvent)
            {
                wprintf(L"The subscription callback was notified that event records are missing.\n");
                // Handle if this is an issue for your application.
            }
            else
            {
                wprintf(L"The subscription callback received the following Win32 error: %lu\n", (DWORD)hEvent);
            }
            break;

        case EvtSubscribeActionDeliver:
            if (ERROR_SUCCESS != (status = PrintEvent(hEvent)))
            {
                goto cleanup;
            }
            break;

        default:
            wprintf(L"SubscriptionCallback: Unknown action.\n");
    }

cleanup:

    if (ERROR_SUCCESS != status)
    {
        // End subscription - Use some kind of IPC mechanism to signal
        // your application to close the subscription handle.
    }

    return status; // The service ignores the returned status.
}

// Render the event as an XML string and print it.
DWORD PrintEvent(EVT_HANDLE hEvent)
{
    DWORD status = ERROR_SUCCESS;
    DWORD dwBufferSize = 0;
    DWORD dwBufferUsed = 0;
    DWORD dwPropertyCount = 0;
    LPWSTR pRenderedContent = NULL;

    if (!EvtRender(NULL, hEvent, EvtRenderEventXml, dwBufferSize, pRenderedContent, &dwBufferUsed, &dwPropertyCount))
    {
        if (ERROR_INSUFFICIENT_BUFFER == (status = GetLastError()))
        {
            dwBufferSize = dwBufferUsed;
            pRenderedContent = (LPWSTR)malloc(dwBufferSize);
            if (pRenderedContent)
            {
                EvtRender(NULL, hEvent, EvtRenderEventXml, dwBufferSize, pRenderedContent, &dwBufferUsed, &dwPropertyCount);
            }
            else
            {
                wprintf(L"malloc failed\n");
                status = ERROR_OUTOFMEMORY;
                goto cleanup;
            }
        }

        if (ERROR_SUCCESS != (status = GetLastError()))
        {
            wprintf(L"EvtRender failed with %d\n", status);
            goto cleanup;
        }
    }

    wprintf(L"%s\n\n", pRenderedContent);

cleanup:

    if (pRenderedContent)
        free(pRenderedContent);

    return status;
}
```



## <a name="pull-subscriptions"></a><span data-ttu-id="87bad-120">提取訂閱</span><span class="sxs-lookup"><span data-stu-id="87bad-120">Pull Subscriptions</span></span>

<span data-ttu-id="87bad-121">提取訂閱模型會使用事件物件 (請參閱 [**CreateEventEx**](/windows/desktop/api/synchapi/nf-synchapi-createeventexa) 函式) ，以指示應用程式在結果集中有符合查詢準則的事件。</span><span class="sxs-lookup"><span data-stu-id="87bad-121">The pull subscription model uses an event object (see the [**CreateEventEx**](/windows/desktop/api/synchapi/nf-synchapi-createeventexa) function) to signal the application that there are events in the result set that match the query criteria.</span></span> <span data-ttu-id="87bad-122">建立可等候事件物件的迴圈結構，直到事件收到信號為止。</span><span class="sxs-lookup"><span data-stu-id="87bad-122">Create a loop construct that waits on the event object until the event is signaled.</span></span> <span data-ttu-id="87bad-123">然後，在迴圈中呼叫 [**EvtNext**](/windows/desktop/api/WinEvt/nf-winevt-evtnext) 函數，以列舉結果集中的事件。</span><span class="sxs-lookup"><span data-stu-id="87bad-123">Then, call the [**EvtNext**](/windows/desktop/api/WinEvt/nf-winevt-evtnext) function in a loop to enumerate the events in the result set.</span></span> <span data-ttu-id="87bad-124">當 **EvtNext** 函式失敗，並將最後一個錯誤設定為 [錯誤] 的 \_ 專案時 \_ \_ ，請重設事件物件，並等候服務在結果集中有事件時再次通知物件。</span><span class="sxs-lookup"><span data-stu-id="87bad-124">When the **EvtNext** function fails and sets the last error to ERROR\_NO\_MORE\_ITEMS, reset the event object and wait for the service to signal the object again when there are events in the result set.</span></span>

<span data-ttu-id="87bad-125">下列範例顯示如何使用提取訂閱模型。</span><span class="sxs-lookup"><span data-stu-id="87bad-125">The following example shows how to use the pull subscription model.</span></span>


```C++
#include <windows.h>
#include <conio.h>
#include <stdio.h>
#include <winevt.h>

#pragma comment(lib, "wevtapi.lib")

#define ARRAY_SIZE 10

DWORD EnumerateResults(EVT_HANDLE hResults);
DWORD PrintEvent(EVT_HANDLE hEvent);
BOOL IsKeyEvent(HANDLE hStdIn);

void __cdecl wmain()
{
    DWORD status = ERROR_SUCCESS;
    EVT_HANDLE hSubscription = NULL;
    LPWSTR pwsPath = L"<channel name goes here>";
    LPWSTR pwsQuery = L"*";
    HANDLE aWaitHandles[2];
    DWORD dwWait = 0;

    // Get a handle for console input, so you can break out of the loop.
    aWaitHandles[0] = GetStdHandle(STD_INPUT_HANDLE);
    if (INVALID_HANDLE_VALUE == aWaitHandles[0])
    {
        wprintf(L"GetStdHandle failed with %lu.\n", GetLastError());
        goto cleanup;
    }

    // Get a handle to a manual reset event object that the subscription will signal
    // when events become available that match your query criteria.
    aWaitHandles[1] = CreateEvent(NULL, TRUE, TRUE, NULL);
    if (NULL == aWaitHandles[1])
    {
        wprintf(L"CreateEvent failed with %lu.\n", GetLastError());
        goto cleanup;
    }

    // Subscribe to events.
    hSubscription = EvtSubscribe(NULL, aWaitHandles[1], pwsPath, pwsQuery, NULL, NULL, NULL, EvtSubscribeStartAtOldestRecord);
    if (NULL == hSubscription)
    {
        status = GetLastError();

        if (ERROR_EVT_CHANNEL_NOT_FOUND == status)
            wprintf(L"Channel %s was not found.\n", pwsPath);
        else if (ERROR_EVT_INVALID_QUERY == status)
            wprintf(L"The query %s was not found.\n", pwsQuery);
        else
            wprintf(L"EvtSubscribe failed with %lu.\n", status);

        goto cleanup;
    }

    wprintf(L"Press any key to quit.\n");

    // Loop until the user presses a key or there is an error.
    while (true)
    {
        dwWait = WaitForMultipleObjects(sizeof(aWaitHandles)/sizeof(HANDLE), aWaitHandles, FALSE, INFINITE);

        if (0 == dwWait - WAIT_OBJECT_0)  // Console input
        {
            if (IsKeyEvent(aWaitHandles[0]))
                break;
        }
        else if (1 == dwWait - WAIT_OBJECT_0) // Query results
        {
            if (ERROR_NO_MORE_ITEMS != (status = EnumerateResults(hSubscription)))
            {
                break;
            }

            ResetEvent(aWaitHandles[1]);
        }
        else
        {
            if (WAIT_FAILED == dwWait)
            {
                wprintf(L"WaitForSingleObject failed with %lu\n", GetLastError());
            }
            break;
        }
    }

cleanup:

    if (hSubscription)
        EvtClose(hSubscription);

    if (aWaitHandles[0])
        CloseHandle(aWaitHandles[0]);

    if (aWaitHandles[1])
        CloseHandle(aWaitHandles[1]);
}

// Enumerate the events in the result set.
DWORD EnumerateResults(EVT_HANDLE hResults)
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
        // event for display.
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

    // Closes any events in case an error occurred above.
    for (DWORD i = 0; i < dwReturned; i++)
    {
        if (NULL != hEvents[i])
            EvtClose(hEvents[i]);
    }

    return status;
}

// Render the event as an XML string and print it.
DWORD PrintEvent(EVT_HANDLE hEvent)
{
    DWORD status = ERROR_SUCCESS;
    DWORD dwBufferSize = 0;
    DWORD dwBufferUsed = 0;
    DWORD dwPropertyCount = 0;
    LPWSTR pRenderedContent = NULL;

    // The EvtRenderEventXml flag tells EvtRender to render the event as an XML string.
    if (!EvtRender(NULL, hEvent, EvtRenderEventXml, dwBufferSize, pRenderedContent, &dwBufferUsed, &dwPropertyCount))
    {
        if (ERROR_INSUFFICIENT_BUFFER == (status = GetLastError()))
        {
            dwBufferSize = dwBufferUsed;
            pRenderedContent = (LPWSTR)malloc(dwBufferSize);
            if (pRenderedContent)
            {
                EvtRender(NULL, hEvent, EvtRenderEventXml, dwBufferSize, pRenderedContent, &dwBufferUsed, &dwPropertyCount);
            }
            else
            {
                wprintf(L"malloc failed\n");
                status = ERROR_OUTOFMEMORY;
                goto cleanup;
            }
        }

        if (ERROR_SUCCESS != (status = GetLastError()))
        {
            wprintf(L"EvtRender failed with %d\n", GetLastError());
            goto cleanup;
        }
    }

    wprintf(L"\n\n%s", pRenderedContent);

cleanup:

    if (pRenderedContent)
        free(pRenderedContent);

    return status;
}

// Determines whether the console input was a key event.
BOOL IsKeyEvent(HANDLE hStdIn)
{
    INPUT_RECORD Record[128];
    DWORD dwRecordsRead = 0;
    BOOL fKeyPress = FALSE;

    if (ReadConsoleInput(hStdIn, Record, 128, &dwRecordsRead))
    {
        for (DWORD i = 0; i < dwRecordsRead; i++)
        {
            if (KEY_EVENT == Record[i].EventType)
            {
                fKeyPress = TRUE;
                break;
            }
        }
    }

    return fKeyPress;
}
```



 

 