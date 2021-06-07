---
description: 下列範例會建立一個計時器常式，此常式會在10秒延遲之後，由計時器佇列中的執行緒執行。
ms.assetid: 779156fe-f825-452b-acbe-e2cb189e24d2
title: 使用計時器佇列
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d084a03eb25301f94361c1e7ca6b76dd9fee269
ms.sourcegitcommit: b01ad017c152c6756f3638623fe335877644d414
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/06/2021
ms.locfileid: "111549930"
---
# <a name="using-timer-queues"></a><span data-ttu-id="03855-103">使用計時器佇列</span><span class="sxs-lookup"><span data-stu-id="03855-103">Using Timer Queues</span></span>

<span data-ttu-id="03855-104">下列範例會建立一個計時器常式，此常式會在10秒延遲之後，由 [計時器佇列](timer-queues.md) 中的執行緒執行。</span><span class="sxs-lookup"><span data-stu-id="03855-104">The following example creates a timer routine that will be executed by a thread from a [timer queue](timer-queues.md) after a 10 second delay.</span></span> <span data-ttu-id="03855-105">首先，程式碼會使用 [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) 函式來建立計時器佇列執行緒完成時發出信號的事件物件。</span><span class="sxs-lookup"><span data-stu-id="03855-105">First, the code uses the [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) function to create an event object that is signaled when the timer-queue thread completes.</span></span> <span data-ttu-id="03855-106">然後，它會分別使用 [**CreateTimerQueue**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueue) 和 [**CreateTimerQueueTimer**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer) 函數來建立計時器佇列和計時器佇列計時器。</span><span class="sxs-lookup"><span data-stu-id="03855-106">Then it creates a timer queue and a timer-queue timer, using the [**CreateTimerQueue**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueue) and [**CreateTimerQueueTimer**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer) functions, respectively.</span></span> <span data-ttu-id="03855-107">程式碼會使用 [**WaitForSingleObject**](/windows/win32/api/winbase/nf-winbase-registerwaitforsingleobject) 函數來判斷計時器常式何時完成。</span><span class="sxs-lookup"><span data-stu-id="03855-107">The code uses the [**WaitForSingleObject**](/windows/win32/api/winbase/nf-winbase-registerwaitforsingleobject) function to determine when the timer routine has completed.</span></span> <span data-ttu-id="03855-108">最後，程式碼會呼叫 [**DeleteTimerQueue**](/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-deletetimerqueue) 來進行清除。</span><span class="sxs-lookup"><span data-stu-id="03855-108">Finally, the code calls [**DeleteTimerQueue**](/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-deletetimerqueue) to clean up.</span></span>

<span data-ttu-id="03855-109">如需計時器常式的詳細資訊，請參閱 [**WaitOrTimerCallback**](/previous-versions/windows/desktop/legacy/ms687066(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="03855-109">For more information on the timer routine, see [**WaitOrTimerCallback**](/previous-versions/windows/desktop/legacy/ms687066(v=vs.85)).</span></span>


```C++
#include <windows.h>
#include <stdio.h>

HANDLE gDoneEvent;

VOID CALLBACK TimerRoutine(PVOID lpParam, BOOLEAN TimerOrWaitFired)
{
    if (lpParam == NULL)
    {
        printf("TimerRoutine lpParam is NULL\n");
    }
    else
    {
        // lpParam points to the argument; in this case it is an int

        printf("Timer routine called. Parameter is %d.\n", 
                *(int*)lpParam);
        if(TimerOrWaitFired)
        {
            printf("The wait timed out.\n");
        }
        else
        {
            printf("The wait event was signaled.\n");
        }
    }

    SetEvent(gDoneEvent);
}

int main()
{
    HANDLE hTimer = NULL;
    HANDLE hTimerQueue = NULL;
    int arg = 123;

    // Use an event object to track the TimerRoutine execution
    gDoneEvent = CreateEvent(NULL, TRUE, FALSE, NULL);
    if (NULL == gDoneEvent)
    {
        printf("CreateEvent failed (%d)\n", GetLastError());
        return 1;
    }

    // Create the timer queue.
    hTimerQueue = CreateTimerQueue();
    if (NULL == hTimerQueue)
    {
        printf("CreateTimerQueue failed (%d)\n", GetLastError());
        return 2;
    }

    // Set a timer to call the timer routine in 10 seconds.
    if (!CreateTimerQueueTimer( &hTimer, hTimerQueue, 
            (WAITORTIMERCALLBACK)TimerRoutine, &arg , 10000, 0, 0))
    {
        printf("CreateTimerQueueTimer failed (%d)\n", GetLastError());
        return 3;
    }

    // TODO: Do other useful work here 

    printf("Call timer routine in 10 seconds...\n");

    // Wait for the timer-queue thread to complete using an event 
    // object. The thread will signal the event at that time.

    if (WaitForSingleObject(gDoneEvent, INFINITE) != WAIT_OBJECT_0)
        printf("WaitForSingleObject failed (%d)\n", GetLastError());

    CloseHandle(gDoneEvent);

    // Delete all timers in the timer queue.
    if (!DeleteTimerQueue(hTimerQueue))
        printf("DeleteTimerQueue failed (%d)\n", GetLastError());

    return 0;
}
```



 

 
