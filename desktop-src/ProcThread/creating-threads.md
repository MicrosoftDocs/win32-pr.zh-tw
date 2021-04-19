---
description: CreateThread 函式會為進程建立新的執行緒。
ms.assetid: eb0cc3c0-14f2-4913-a592-4ba3eaf67002
title: 建立執行緒
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 545088779bdaff665a8079296014535ab244e821
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106993128"
---
# <a name="creating-threads"></a><span data-ttu-id="97a54-103">建立執行緒</span><span class="sxs-lookup"><span data-stu-id="97a54-103">Creating Threads</span></span>

<span data-ttu-id="97a54-104">[**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread)函式會為進程建立新的執行緒。</span><span class="sxs-lookup"><span data-stu-id="97a54-104">The [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) function creates a new thread for a process.</span></span> <span data-ttu-id="97a54-105">建立執行緒必須指定新執行緒要執行之程式碼的起始位址。</span><span class="sxs-lookup"><span data-stu-id="97a54-105">The creating thread must specify the starting address of the code that the new thread is to execute.</span></span> <span data-ttu-id="97a54-106">一般而言，起始位址是程式碼中所定義的函式名稱 (如需詳細資訊，請參閱 [*ThreadProc*](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85))) 。</span><span class="sxs-lookup"><span data-stu-id="97a54-106">Typically, the starting address is the name of a function defined in the program code (for more information, see [*ThreadProc*](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85))).</span></span> <span data-ttu-id="97a54-107">此函式會接受單一參數，並傳回 **DWORD** 值。</span><span class="sxs-lookup"><span data-stu-id="97a54-107">This function takes a single parameter and returns a **DWORD** value.</span></span> <span data-ttu-id="97a54-108">處理常式可以有多個執行緒同時執行相同的函式。</span><span class="sxs-lookup"><span data-stu-id="97a54-108">A process can have multiple threads simultaneously executing the same function.</span></span>

<span data-ttu-id="97a54-109">以下是一個簡單的範例，示範如何建立執行本機定義函數的新執行緒 `MyThreadFunction` 。</span><span class="sxs-lookup"><span data-stu-id="97a54-109">The following is a simple example that demonstrates how to create a new thread that executes the locally defined function, `MyThreadFunction`.</span></span>

<span data-ttu-id="97a54-110">呼叫執行緒會使用 [**WaitForMultipleObjects**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjects) 函數來保存，直到所有背景工作執行緒終止為止。</span><span class="sxs-lookup"><span data-stu-id="97a54-110">The calling thread uses the [**WaitForMultipleObjects**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjects) function to persist until all worker threads have terminated.</span></span> <span data-ttu-id="97a54-111">呼叫執行緒在等候時封鎖;若要繼續處理，呼叫的執行緒會使用 [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) ，並等候每個背景工作執行緒來發出等候物件的信號。</span><span class="sxs-lookup"><span data-stu-id="97a54-111">The calling thread blocks while it is waiting; to continue processing, a calling thread would use [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) and wait for each worker thread to signal its wait object.</span></span> <span data-ttu-id="97a54-112">請注意，如果您要在終止之前關閉工作者執行緒的控制碼，則不會終止背景工作執行緒。</span><span class="sxs-lookup"><span data-stu-id="97a54-112">Note that if you were to close the handle to a worker thread before it terminated, this does not terminate the worker thread.</span></span> <span data-ttu-id="97a54-113">不過，在後續的函式呼叫中無法使用控制碼。</span><span class="sxs-lookup"><span data-stu-id="97a54-113">However, the handle will be unavailable for use in subsequent function calls.</span></span>


```C++
#include <windows.h>
#include <tchar.h>
#include <strsafe.h>

#define MAX_THREADS 3
#define BUF_SIZE 255

DWORD WINAPI MyThreadFunction( LPVOID lpParam );
void ErrorHandler(LPTSTR lpszFunction);

// Sample custom data structure for threads to use.
// This is passed by void pointer so it can be any data type
// that can be passed using a single void pointer (LPVOID).
typedef struct MyData {
    int val1;
    int val2;
} MYDATA, *PMYDATA;


int _tmain()
{
    PMYDATA pDataArray[MAX_THREADS];
    DWORD   dwThreadIdArray[MAX_THREADS];
    HANDLE  hThreadArray[MAX_THREADS]; 

    // Create MAX_THREADS worker threads.

    for( int i=0; i<MAX_THREADS; i++ )
    {
        // Allocate memory for thread data.

        pDataArray[i] = (PMYDATA) HeapAlloc(GetProcessHeap(), HEAP_ZERO_MEMORY,
                sizeof(MYDATA));

        if( pDataArray[i] == NULL )
        {
           // If the array allocation fails, the system is out of memory
           // so there is no point in trying to print an error message.
           // Just terminate execution.
            ExitProcess(2);
        }

        // Generate unique data for each thread to work with.

        pDataArray[i]->val1 = i;
        pDataArray[i]->val2 = i+100;

        // Create the thread to begin execution on its own.

        hThreadArray[i] = CreateThread( 
            NULL,                   // default security attributes
            0,                      // use default stack size  
            MyThreadFunction,       // thread function name
            pDataArray[i],          // argument to thread function 
            0,                      // use default creation flags 
            &dwThreadIdArray[i]);   // returns the thread identifier 


        // Check the return value for success.
        // If CreateThread fails, terminate execution. 
        // This will automatically clean up threads and memory. 

        if (hThreadArray[i] == NULL) 
        {
           ErrorHandler(TEXT("CreateThread"));
           ExitProcess(3);
        }
    } // End of main thread creation loop.

    // Wait until all threads have terminated.

    WaitForMultipleObjects(MAX_THREADS, hThreadArray, TRUE, INFINITE);

    // Close all thread handles and free memory allocations.

    for(int i=0; i<MAX_THREADS; i++)
    {
        CloseHandle(hThreadArray[i]);
        if(pDataArray[i] != NULL)
        {
            HeapFree(GetProcessHeap(), 0, pDataArray[i]);
            pDataArray[i] = NULL;    // Ensure address is not reused.
        }
    }

    return 0;
}


DWORD WINAPI MyThreadFunction( LPVOID lpParam ) 
{ 
    HANDLE hStdout;
    PMYDATA pDataArray;

    TCHAR msgBuf[BUF_SIZE];
    size_t cchStringSize;
    DWORD dwChars;

    // Make sure there is a console to receive output results. 

    hStdout = GetStdHandle(STD_OUTPUT_HANDLE);
    if( hStdout == INVALID_HANDLE_VALUE )
        return 1;

    // Cast the parameter to the correct data type.
    // The pointer is known to be valid because 
    // it was checked for NULL before the thread was created.
 
    pDataArray = (PMYDATA)lpParam;

    // Print the parameter values using thread-safe functions.

    StringCchPrintf(msgBuf, BUF_SIZE, TEXT("Parameters = %d, %d\n"), 
        pDataArray->val1, pDataArray->val2); 
    StringCchLength(msgBuf, BUF_SIZE, &cchStringSize);
    WriteConsole(hStdout, msgBuf, (DWORD)cchStringSize, &dwChars, NULL);

    return 0; 
} 



void ErrorHandler(LPTSTR lpszFunction) 
{ 
    // Retrieve the system error message for the last-error code.

    LPVOID lpMsgBuf;
    LPVOID lpDisplayBuf;
    DWORD dw = GetLastError(); 

    FormatMessage(
        FORMAT_MESSAGE_ALLOCATE_BUFFER | 
        FORMAT_MESSAGE_FROM_SYSTEM |
        FORMAT_MESSAGE_IGNORE_INSERTS,
        NULL,
        dw,
        MAKELANGID(LANG_NEUTRAL, SUBLANG_DEFAULT),
        (LPTSTR) &lpMsgBuf,
        0, NULL );

    // Display the error message.

    lpDisplayBuf = (LPVOID)LocalAlloc(LMEM_ZEROINIT, 
        (lstrlen((LPCTSTR) lpMsgBuf) + lstrlen((LPCTSTR) lpszFunction) + 40) * sizeof(TCHAR)); 
    StringCchPrintf((LPTSTR)lpDisplayBuf, 
        LocalSize(lpDisplayBuf) / sizeof(TCHAR),
        TEXT("%s failed with error %d: %s"), 
        lpszFunction, dw, lpMsgBuf); 
    MessageBox(NULL, (LPCTSTR) lpDisplayBuf, TEXT("Error"), MB_OK); 

    // Free error-handling buffer allocations.

    LocalFree(lpMsgBuf);
    LocalFree(lpDisplayBuf);
}
```



<span data-ttu-id="97a54-114">函 `MyThreadFunction` 式可避免使用 C 執行時間程式庫 (CRT) ，因為它的許多函數都不是安全線程，特別是當您未使用多執行緒 CRT 時。</span><span class="sxs-lookup"><span data-stu-id="97a54-114">The `MyThreadFunction` function avoids the use of the C run-time library (CRT), as many of its functions are not thread-safe, particularly if you are not using the multithreaded CRT.</span></span> <span data-ttu-id="97a54-115">如果您想要在函式中使用 CRT `ThreadProc` ，請改用 **\_ beginthreadex** 函數。</span><span class="sxs-lookup"><span data-stu-id="97a54-115">If you would like to use the CRT in a `ThreadProc` function, use the **\_beginthreadex** function instead.</span></span>

<span data-ttu-id="97a54-116">如果建立執行緒在新執行緒之前結束，則傳遞區域變數的位址會有風險，因為指標變成無效。</span><span class="sxs-lookup"><span data-stu-id="97a54-116">It is risky to pass the address of a local variable if the creating thread exits before the new thread, because the pointer becomes invalid.</span></span> <span data-ttu-id="97a54-117">相反地，請將指標傳遞至動態配置的記憶體，或讓建立執行緒等候新的執行緒終止。</span><span class="sxs-lookup"><span data-stu-id="97a54-117">Instead, either pass a pointer to dynamically allocated memory or make the creating thread wait for the new thread to terminate.</span></span> <span data-ttu-id="97a54-118">您也可以使用全域變數，從建立執行緒將資料傳遞至新的執行緒。</span><span class="sxs-lookup"><span data-stu-id="97a54-118">Data can also be passed from the creating thread to the new thread using global variables.</span></span> <span data-ttu-id="97a54-119">使用全域變數時，通常需要同步處理多個執行緒的存取。</span><span class="sxs-lookup"><span data-stu-id="97a54-119">With global variables, it is usually necessary to synchronize access by multiple threads.</span></span> <span data-ttu-id="97a54-120">如需同步處理的詳細資訊，請參閱 [同步處理多執行緒的執行](synchronizing-execution-of-multiple-threads.md)。</span><span class="sxs-lookup"><span data-stu-id="97a54-120">For more information about synchronization, see [Synchronizing Execution of Multiple Threads](synchronizing-execution-of-multiple-threads.md).</span></span>

<span data-ttu-id="97a54-121">建立執行緒可以使用 [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) 的引數來指定下列各項：</span><span class="sxs-lookup"><span data-stu-id="97a54-121">The creating thread can use the arguments to [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) to specify the following:</span></span>

-   <span data-ttu-id="97a54-122">新執行緒之控制碼的安全性屬性。</span><span class="sxs-lookup"><span data-stu-id="97a54-122">The security attributes for the handle to the new thread.</span></span> <span data-ttu-id="97a54-123">這些安全性屬性包含繼承旗標，可決定子進程是否可以繼承控制碼。</span><span class="sxs-lookup"><span data-stu-id="97a54-123">These security attributes include an inheritance flag that determines whether the handle can be inherited by child processes.</span></span> <span data-ttu-id="97a54-124">安全性屬性也包含安全描述項，系統會在授與存取權之前，讓系統用來對執行緒控制碼的所有後續用途執行存取檢查。</span><span class="sxs-lookup"><span data-stu-id="97a54-124">The security attributes also include a security descriptor, which the system uses to perform access checks on all subsequent uses of the thread's handle before access is granted.</span></span>
-   <span data-ttu-id="97a54-125">新執行緒的初始堆疊大小。</span><span class="sxs-lookup"><span data-stu-id="97a54-125">The initial stack size of the new thread.</span></span> <span data-ttu-id="97a54-126">執行緒的堆疊會在進程的記憶體空間中自動設定;系統會視需要增加堆疊，並線上程終止時釋出。</span><span class="sxs-lookup"><span data-stu-id="97a54-126">The thread's stack is allocated automatically in the memory space of the process; the system increases the stack as needed and frees it when the thread terminates.</span></span> <span data-ttu-id="97a54-127">如需詳細資訊，請參閱 [執行緒堆疊大小](thread-stack-size.md)。</span><span class="sxs-lookup"><span data-stu-id="97a54-127">For more information, see [Thread Stack Size](thread-stack-size.md).</span></span>
-   <span data-ttu-id="97a54-128">建立旗標，可讓您建立處於暫停狀態的執行緒。</span><span class="sxs-lookup"><span data-stu-id="97a54-128">A creation flag that enables you to create the thread in a suspended state.</span></span> <span data-ttu-id="97a54-129">暫止時，除非呼叫 [**ResumeThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-resumethread) 函數，否則執行緒不會執行。</span><span class="sxs-lookup"><span data-stu-id="97a54-129">When suspended, the thread does not run until the [**ResumeThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-resumethread) function is called.</span></span>

<span data-ttu-id="97a54-130">您也可以藉由呼叫 [**CreateRemoteThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethread) 函數來建立執行緒。</span><span class="sxs-lookup"><span data-stu-id="97a54-130">You can also create a thread by calling the [**CreateRemoteThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethread) function.</span></span> <span data-ttu-id="97a54-131">偵錯工具進程會使用這個函式來建立執行緒，以在所要進行的進程的位址空間中執行。</span><span class="sxs-lookup"><span data-stu-id="97a54-131">This function is used by debugger processes to create a thread that runs in the address space of the process being debugged.</span></span>

## <a name="related-topics"></a><span data-ttu-id="97a54-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="97a54-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="97a54-133">終止執行緒</span><span class="sxs-lookup"><span data-stu-id="97a54-133">Terminating a Thread</span></span>](terminating-a-thread.md)
</dt> </dl>

 

 
