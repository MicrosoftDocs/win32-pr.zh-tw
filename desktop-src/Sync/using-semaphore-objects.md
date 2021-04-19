---
description: 下列範例會使用信號物件來限制可執行特定工作的執行緒數目。
ms.assetid: 24a5c13c-573a-4fc2-ac19-98188c9eb68a
title: 使用信號物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ded28014c7e832ab5bdc96d724d57e314d0cc857
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/19/2021
ms.locfileid: "106999312"
---
# <a name="using-semaphore-objects"></a><span data-ttu-id="3f321-103">使用信號物件</span><span class="sxs-lookup"><span data-stu-id="3f321-103">Using Semaphore Objects</span></span>

<span data-ttu-id="3f321-104">下列範例會使用 [信號物件](semaphore-objects.md) 來限制可執行特定工作的執行緒數目。</span><span class="sxs-lookup"><span data-stu-id="3f321-104">The following example uses a [semaphore object](semaphore-objects.md) to limit the number of threads that can perform a particular task.</span></span> <span data-ttu-id="3f321-105">首先，它會使用 [**CreateSemaphore**](/windows/desktop/api/WinBase/nf-winbase-createsemaphorea) 函數來建立信號，並指定初始和最大計數，然後使用 [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) 函數來建立執行緒。</span><span class="sxs-lookup"><span data-stu-id="3f321-105">First, it uses the [**CreateSemaphore**](/windows/desktop/api/WinBase/nf-winbase-createsemaphorea) function to create the semaphore and to specify initial and maximum counts, then it uses the [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) function to create the threads.</span></span>

<span data-ttu-id="3f321-106">線上程嘗試執行工作之前，它會使用 [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) 函數來判斷信號的目前計數是否允許它執行這項作業。</span><span class="sxs-lookup"><span data-stu-id="3f321-106">Before a thread attempts to perform the task, it uses the [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) function to determine whether the semaphore's current count permits it to do so.</span></span> <span data-ttu-id="3f321-107">Wait 函式的超時參數設定為零，因此，如果信號處於未收到信號狀態，函式就會立即傳回。</span><span class="sxs-lookup"><span data-stu-id="3f321-107">The wait function's time-out parameter is set to zero, so the function returns immediately if the semaphore is in the nonsignaled state.</span></span> <span data-ttu-id="3f321-108">**WaitForSingleObject** 會將信號的計數遞減一。</span><span class="sxs-lookup"><span data-stu-id="3f321-108">**WaitForSingleObject** decrements the semaphore's count by one.</span></span>

<span data-ttu-id="3f321-109">當執行緒完成工作時，它會使用 [**ReleaseSemaphore**](/windows/win32/api/synchapi/nf-synchapi-releasesemaphore) 函式來遞增信號的計數，進而讓另一個等候執行緒執行工作。</span><span class="sxs-lookup"><span data-stu-id="3f321-109">When a thread completes the task, it uses the [**ReleaseSemaphore**](/windows/win32/api/synchapi/nf-synchapi-releasesemaphore) function to increment the semaphore's count, thus enabling another waiting thread to perform the task.</span></span>


```C++
#include <windows.h>
#include <stdio.h>

#define MAX_SEM_COUNT 10
#define THREADCOUNT 12

HANDLE ghSemaphore;

DWORD WINAPI ThreadProc( LPVOID );

int main( void )
{
    HANDLE aThread[THREADCOUNT];
    DWORD ThreadID;
    int i;

    // Create a semaphore with initial and max counts of MAX_SEM_COUNT

    ghSemaphore = CreateSemaphore( 
        NULL,           // default security attributes
        MAX_SEM_COUNT,  // initial count
        MAX_SEM_COUNT,  // maximum count
        NULL);          // unnamed semaphore

    if (ghSemaphore == NULL) 
    {
        printf("CreateSemaphore error: %d\n", GetLastError());
        return 1;
    }

    // Create worker threads

    for( i=0; i < THREADCOUNT; i++ )
    {
        aThread[i] = CreateThread( 
                     NULL,       // default security attributes
                     0,          // default stack size
                     (LPTHREAD_START_ROUTINE) ThreadProc, 
                     NULL,       // no thread function arguments
                     0,          // default creation flags
                     &ThreadID); // receive thread identifier

        if( aThread[i] == NULL )
        {
            printf("CreateThread error: %d\n", GetLastError());
            return 1;
        }
    }

    // Wait for all threads to terminate

    WaitForMultipleObjects(THREADCOUNT, aThread, TRUE, INFINITE);

    // Close thread and semaphore handles

    for( i=0; i < THREADCOUNT; i++ )
        CloseHandle(aThread[i]);

    CloseHandle(ghSemaphore);

    return 0;
}

DWORD WINAPI ThreadProc( LPVOID lpParam )
{

    // lpParam not used in this example
    UNREFERENCED_PARAMETER(lpParam);

    DWORD dwWaitResult; 
    BOOL bContinue=TRUE;

    while(bContinue)
    {
        // Try to enter the semaphore gate.

        dwWaitResult = WaitForSingleObject( 
            ghSemaphore,   // handle to semaphore
            0L);           // zero-second time-out interval

        switch (dwWaitResult) 
        { 
            // The semaphore object was signaled.
            case WAIT_OBJECT_0: 
                // TODO: Perform task
                printf("Thread %d: wait succeeded\n", GetCurrentThreadId());
                bContinue=FALSE;            

                // Simulate thread spending time on task
                Sleep(5);

                // Release the semaphore when task is finished

                if (!ReleaseSemaphore( 
                        ghSemaphore,  // handle to semaphore
                        1,            // increase count by one
                        NULL) )       // not interested in previous count
                {
                    printf("ReleaseSemaphore error: %d\n", GetLastError());
                }
                break; 

            // The semaphore was nonsignaled, so a time-out occurred.
            case WAIT_TIMEOUT: 
                printf("Thread %d: wait timed out\n", GetCurrentThreadId());
                break; 
        }
    }
    return TRUE;
}
```



 

 
