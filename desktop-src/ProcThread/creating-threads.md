---
description: 請參閱如何使用 CreateThread 函式來建立進程的新執行緒。 檢查顯示其使用方式的程式碼範例。
ms.assetid: eb0cc3c0-14f2-4913-a592-4ba3eaf67002
title: 建立執行緒
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5dee74cb81c886fe05d07a0970f7d8946d123d92810e6f22dd094e1d8d00466a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120081428"
---
# <a name="creating-threads"></a>建立執行緒

[**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread)函式會為進程建立新的執行緒。 建立執行緒必須指定新執行緒要執行之程式碼的起始位址。 一般而言，起始位址是程式碼中所定義的函式名稱 (如需詳細資訊，請參閱 [*ThreadProc*](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85))) 。 此函式會接受單一參數，並傳回 **DWORD** 值。 處理常式可以有多個執行緒同時執行相同的函式。

以下是一個簡單的範例，示範如何建立執行本機定義函數的新執行緒 `MyThreadFunction` 。

呼叫執行緒會使用 [**WaitForMultipleObjects**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjects) 函數來保存，直到所有背景工作執行緒終止為止。 呼叫執行緒在等候時封鎖;若要繼續處理，呼叫的執行緒會使用 [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) ，並等候每個背景工作執行緒來發出等候物件的信號。 請注意，如果您要在終止之前關閉工作者執行緒的控制碼，則不會終止背景工作執行緒。 不過，在後續的函式呼叫中無法使用控制碼。


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



函 `MyThreadFunction` 式可避免使用 C 執行時間程式庫 (CRT) ，因為它的許多函數都不是安全線程，特別是當您未使用多執行緒 CRT 時。 如果您想要在函式中使用 CRT `ThreadProc` ，請改用 **\_ beginthreadex** 函數。

如果建立執行緒在新執行緒之前結束，則傳遞區域變數的位址會有風險，因為指標變成無效。 相反地，請將指標傳遞至動態配置的記憶體，或讓建立執行緒等候新的執行緒終止。 您也可以使用全域變數，從建立執行緒將資料傳遞至新的執行緒。 使用全域變數時，通常需要同步處理多個執行緒的存取。 如需同步處理的詳細資訊，請參閱 [同步處理多執行緒的執行](synchronizing-execution-of-multiple-threads.md)。

建立執行緒可以使用 [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) 的引數來指定下列各項：

-   新執行緒之控制碼的安全性屬性。 這些安全性屬性包含繼承旗標，可決定子進程是否可以繼承控制碼。 安全性屬性也包含安全描述項，系統會在授與存取權之前，讓系統用來對執行緒控制碼的所有後續用途執行存取檢查。
-   新執行緒的初始堆疊大小。 執行緒的堆疊會在進程的記憶體空間中自動設定;系統會視需要增加堆疊，並線上程終止時釋出。 如需詳細資訊，請參閱 [執行緒堆疊大小](thread-stack-size.md)。
-   建立旗標，可讓您建立處於暫停狀態的執行緒。 暫止時，除非呼叫 [**ResumeThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-resumethread) 函數，否則執行緒不會執行。

您也可以藉由呼叫 [**CreateRemoteThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethread) 函數來建立執行緒。 偵錯工具進程會使用這個函式來建立執行緒，以在所要進行的進程的位址空間中執行。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[終止執行緒](terminating-a-thread.md)
</dt> </dl>

 

 
