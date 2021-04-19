---
description: 您可以使用 mutex 物件來防止共用資源同時存取多個執行緒或進程。
ms.assetid: 0f69ba50-69ce-467a-b068-8fd8f07c6c78
title: 使用 Mutex 物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbd68f41319125613e8569e7b343c0b1601a7735
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106974295"
---
# <a name="using-mutex-objects"></a><span data-ttu-id="1bf99-103">使用 Mutex 物件</span><span class="sxs-lookup"><span data-stu-id="1bf99-103">Using Mutex Objects</span></span>

<span data-ttu-id="1bf99-104">您可以使用 [mutex 物件](mutex-objects.md) 來防止共用資源同時存取多個執行緒或進程。</span><span class="sxs-lookup"><span data-stu-id="1bf99-104">You can use a [mutex object](mutex-objects.md) to protect a shared resource from simultaneous access by multiple threads or processes.</span></span> <span data-ttu-id="1bf99-105">每個執行緒都必須等待 mutex 的擁有權，才能執行存取共用資源的程式碼。</span><span class="sxs-lookup"><span data-stu-id="1bf99-105">Each thread must wait for ownership of the mutex before it can execute the code that accesses the shared resource.</span></span> <span data-ttu-id="1bf99-106">例如，如果有數個執行緒共用資料庫的存取權，執行緒可以使用 mutex 物件一次只允許一個執行緒寫入資料庫。</span><span class="sxs-lookup"><span data-stu-id="1bf99-106">For example, if several threads share access to a database, the threads can use a mutex object to permit only one thread at a time to write to the database.</span></span>

<span data-ttu-id="1bf99-107">下列範例會使用 [**CreateMutex**](/windows/win32/api/synchapi/nf-synchapi-createmutexa) 函數來建立 mutex 物件，並使用 [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) 函數來建立背景工作執行緒。</span><span class="sxs-lookup"><span data-stu-id="1bf99-107">The following example uses the [**CreateMutex**](/windows/win32/api/synchapi/nf-synchapi-createmutexa) function to create a mutex object and the [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) function to create worker threads.</span></span>

<span data-ttu-id="1bf99-108">當這個進程的執行緒寫入資料庫時，它會先使用 [**WaitForSingleObject**](/windows/win32/api/winbase/nf-winbase-registerwaitforsingleobject) 函數要求 mutex 的擁有權。</span><span class="sxs-lookup"><span data-stu-id="1bf99-108">When a thread of this process writes to the database, it first requests ownership of the mutex using the [**WaitForSingleObject**](/windows/win32/api/winbase/nf-winbase-registerwaitforsingleobject) function.</span></span> <span data-ttu-id="1bf99-109">如果執行緒取得 mutex 的擁有權，則會寫入資料庫，然後使用 [**ReleaseMutex**](/windows/win32/api/synchapi/nf-synchapi-releasemutex) 函式釋放其 mutex 的擁有權。</span><span class="sxs-lookup"><span data-stu-id="1bf99-109">If the thread obtains ownership of the mutex, it writes to the database and then releases its ownership of the mutex using the [**ReleaseMutex**](/windows/win32/api/synchapi/nf-synchapi-releasemutex) function.</span></span>

<span data-ttu-id="1bf99-110">這個範例會使用結構化例外狀況處理，以確保執行緒能正確釋放 mutex 物件。</span><span class="sxs-lookup"><span data-stu-id="1bf99-110">This example uses structured exception handling to ensure that the thread properly releases the mutex object.</span></span> <span data-ttu-id="1bf99-111">無論 **\_ \_ try** 區塊如何終止 (，都會執行程式碼的 **\_ \_ finally** 區塊，除非 **\_ \_ try** 區塊包含對 [**TerminateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminatethread)函數) 的呼叫。</span><span class="sxs-lookup"><span data-stu-id="1bf99-111">The **\_\_finally** block of code is executed no matter how the **\_\_try** block terminates (unless the **\_\_try** block includes a call to the [**TerminateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminatethread) function).</span></span> <span data-ttu-id="1bf99-112">這可防止不小心放棄 mutex 物件。</span><span class="sxs-lookup"><span data-stu-id="1bf99-112">This prevents the mutex object from being abandoned inadvertently.</span></span>

<span data-ttu-id="1bf99-113">如果已放棄 mutex，則擁有 mutex 的執行緒不會在終止之前正確釋放它。</span><span class="sxs-lookup"><span data-stu-id="1bf99-113">If a mutex is abandoned, the thread that owned the mutex did not properly release it before terminating.</span></span> <span data-ttu-id="1bf99-114">在此情況下，共用資源的狀態是不定的，而且繼續使用 mutex 可能會混淆可能發生的嚴重錯誤。</span><span class="sxs-lookup"><span data-stu-id="1bf99-114">In this case, the status of the shared resource is indeterminate, and continuing to use the mutex can obscure a potentially serious error.</span></span> <span data-ttu-id="1bf99-115">有些應用程式可能會嘗試將資源還原為一致的狀態。此範例只會傳回錯誤並停止使用 mutex。</span><span class="sxs-lookup"><span data-stu-id="1bf99-115">Some applications might attempt to restore the resource to a consistent state; this example simply returns an error and stops using the mutex.</span></span> <span data-ttu-id="1bf99-116">如需詳細資訊，請參閱 [Mutex 物件](mutex-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="1bf99-116">For more information, see [Mutex Objects](mutex-objects.md).</span></span>


```C++
#include <windows.h>
#include <stdio.h>

#define THREADCOUNT 2

HANDLE ghMutex; 

DWORD WINAPI WriteToDatabase( LPVOID );

int main( void )
{
    HANDLE aThread[THREADCOUNT];
    DWORD ThreadID;
    int i;

    // Create a mutex with no initial owner

    ghMutex = CreateMutex( 
        NULL,              // default security attributes
        FALSE,             // initially not owned
        NULL);             // unnamed mutex

    if (ghMutex == NULL) 
    {
        printf("CreateMutex error: %d\n", GetLastError());
        return 1;
    }

    // Create worker threads

    for( i=0; i < THREADCOUNT; i++ )
    {
        aThread[i] = CreateThread( 
                     NULL,       // default security attributes
                     0,          // default stack size
                     (LPTHREAD_START_ROUTINE) WriteToDatabase, 
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

    // Close thread and mutex handles

    for( i=0; i < THREADCOUNT; i++ )
        CloseHandle(aThread[i]);

    CloseHandle(ghMutex);

    return 0;
}

DWORD WINAPI WriteToDatabase( LPVOID lpParam )
{ 
    // lpParam not used in this example
    UNREFERENCED_PARAMETER(lpParam);

    DWORD dwCount=0, dwWaitResult; 

    // Request ownership of mutex.

    while( dwCount < 20 )
    { 
        dwWaitResult = WaitForSingleObject( 
            ghMutex,    // handle to mutex
            INFINITE);  // no time-out interval
 
        switch (dwWaitResult) 
        {
            // The thread got ownership of the mutex
            case WAIT_OBJECT_0: 
                __try { 
                    // TODO: Write to the database
                    printf("Thread %d writing to database...\n", 
                            GetCurrentThreadId());
                    dwCount++;
                } 

                __finally { 
                    // Release ownership of the mutex object
                    if (! ReleaseMutex(ghMutex)) 
                    { 
                        // Handle error.
                    } 
                } 
                break; 

            // The thread got ownership of an abandoned mutex
            // The database is in an indeterminate state
            case WAIT_ABANDONED: 
                return FALSE; 
        }
    }
    return TRUE; 
}
```



 

 
