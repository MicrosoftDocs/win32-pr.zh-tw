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
# <a name="using-mutex-objects"></a>使用 Mutex 物件

您可以使用 [mutex 物件](mutex-objects.md) 來防止共用資源同時存取多個執行緒或進程。 每個執行緒都必須等待 mutex 的擁有權，才能執行存取共用資源的程式碼。 例如，如果有數個執行緒共用資料庫的存取權，執行緒可以使用 mutex 物件一次只允許一個執行緒寫入資料庫。

下列範例會使用 [**CreateMutex**](/windows/win32/api/synchapi/nf-synchapi-createmutexa) 函數來建立 mutex 物件，並使用 [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) 函數來建立背景工作執行緒。

當這個進程的執行緒寫入資料庫時，它會先使用 [**WaitForSingleObject**](/windows/win32/api/winbase/nf-winbase-registerwaitforsingleobject) 函數要求 mutex 的擁有權。 如果執行緒取得 mutex 的擁有權，則會寫入資料庫，然後使用 [**ReleaseMutex**](/windows/win32/api/synchapi/nf-synchapi-releasemutex) 函式釋放其 mutex 的擁有權。

這個範例會使用結構化例外狀況處理，以確保執行緒能正確釋放 mutex 物件。 無論 **\_ \_ try** 區塊如何終止 (，都會執行程式碼的 **\_ \_ finally** 區塊，除非 **\_ \_ try** 區塊包含對 [**TerminateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminatethread)函數) 的呼叫。 這可防止不小心放棄 mutex 物件。

如果已放棄 mutex，則擁有 mutex 的執行緒不會在終止之前正確釋放它。 在此情況下，共用資源的狀態是不定的，而且繼續使用 mutex 可能會混淆可能發生的嚴重錯誤。 有些應用程式可能會嘗試將資源還原為一致的狀態。此範例只會傳回錯誤並停止使用 mutex。 如需詳細資訊，請參閱 [Mutex 物件](mutex-objects.md)。


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



 

 
