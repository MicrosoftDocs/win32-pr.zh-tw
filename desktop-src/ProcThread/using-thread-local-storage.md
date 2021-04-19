---
description: 執行緒區域儲存 (TLS) 可讓相同進程的多個執行緒使用 TlsAlloc 函式所配置的索引，來儲存和取出執行緒的本機值。
ms.assetid: b7f5a206-a827-4b6b-86f6-5e3aea1246b7
title: 使用執行緒區域儲存區
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e9221d4d0d68891ab8e2d0f2462b7c0aae307c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106992470"
---
# <a name="using-thread-local-storage"></a><span data-ttu-id="4ef93-103">使用執行緒區域儲存區</span><span class="sxs-lookup"><span data-stu-id="4ef93-103">Using Thread Local Storage</span></span>

<span data-ttu-id="4ef93-104">[執行緒區域儲存](thread-local-storage.md) (TLS) 可讓相同進程的多個執行緒使用 [**TlsAlloc**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-tlsalloc) 函式所配置的索引，來儲存和取出執行緒的本機值。</span><span class="sxs-lookup"><span data-stu-id="4ef93-104">[Thread local storage](thread-local-storage.md) (TLS) enables multiple threads of the same process to use an index allocated by the [**TlsAlloc**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-tlsalloc) function to store and retrieve a value that is local to the thread.</span></span> <span data-ttu-id="4ef93-105">在此範例中，會在處理常式啟動時配置索引。</span><span class="sxs-lookup"><span data-stu-id="4ef93-105">In this example, an index is allocated when the process starts.</span></span> <span data-ttu-id="4ef93-106">當每個執行緒開始時，它會配置動態記憶體的區塊，並使用 [**TlsSetValue**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-tlssetvalue) 函式將指標儲存在 TLS 位置中。</span><span class="sxs-lookup"><span data-stu-id="4ef93-106">When each thread starts, it allocates a block of dynamic memory and stores a pointer to this memory in the TLS slot using the [**TlsSetValue**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-tlssetvalue) function.</span></span> <span data-ttu-id="4ef93-107">CommonFunc 函式會使用 [**TlsGetValue**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-tlsgetvalue) 函數來存取與呼叫執行緒的本機索引相關聯的資料。</span><span class="sxs-lookup"><span data-stu-id="4ef93-107">The CommonFunc function uses the [**TlsGetValue**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-tlsgetvalue) function to access the data associated with the index that is local to the calling thread.</span></span> <span data-ttu-id="4ef93-108">在每個執行緒終止之前，它會釋放其動態記憶體。</span><span class="sxs-lookup"><span data-stu-id="4ef93-108">Before each thread terminates, it releases its dynamic memory.</span></span> <span data-ttu-id="4ef93-109">在進程終止之前，它會呼叫 [**TlsFree**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-tlsfree) 來釋放索引。</span><span class="sxs-lookup"><span data-stu-id="4ef93-109">Before the process terminates, it calls [**TlsFree**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-tlsfree) to release the index.</span></span>


```C++
#include <windows.h> 
#include <stdio.h> 
 
#define THREADCOUNT 4 
DWORD dwTlsIndex; 
 
VOID ErrorExit (LPCSTR message);
 
VOID CommonFunc(VOID) 
{ 
   LPVOID lpvData; 
 
// Retrieve a data pointer for the current thread. 
 
   lpvData = TlsGetValue(dwTlsIndex); 
   if ((lpvData == 0) && (GetLastError() != ERROR_SUCCESS)) 
      ErrorExit("TlsGetValue error"); 
 
// Use the data stored for the current thread. 
 
   printf("common: thread %d: lpvData=%lx\n", 
      GetCurrentThreadId(), lpvData); 
 
   Sleep(5000); 
} 
 
DWORD WINAPI ThreadFunc(VOID) 
{ 
   LPVOID lpvData; 
 
// Initialize the TLS index for this thread. 
 
   lpvData = (LPVOID) LocalAlloc(LPTR, 256); 
   if (! TlsSetValue(dwTlsIndex, lpvData)) 
      ErrorExit("TlsSetValue error"); 
 
   printf("thread %d: lpvData=%lx\n", GetCurrentThreadId(), lpvData); 
 
   CommonFunc(); 
 
// Release the dynamic memory before the thread returns. 
 
   lpvData = TlsGetValue(dwTlsIndex); 
   if (lpvData != 0) 
      LocalFree((HLOCAL) lpvData); 
 
   return 0; 
} 
 
int main(VOID) 
{ 
   DWORD IDThread; 
   HANDLE hThread[THREADCOUNT]; 
   int i; 
 
// Allocate a TLS index. 
 
   if ((dwTlsIndex = TlsAlloc()) == TLS_OUT_OF_INDEXES) 
      ErrorExit("TlsAlloc failed"); 
 
// Create multiple threads. 
 
   for (i = 0; i < THREADCOUNT; i++) 
   { 
      hThread[i] = CreateThread(NULL, // default security attributes 
         0,                           // use default stack size 
         (LPTHREAD_START_ROUTINE) ThreadFunc, // thread function 
         NULL,                    // no thread function argument 
         0,                       // use default creation flags 
         &IDThread);              // returns thread identifier 
 
   // Check the return value for success. 
      if (hThread[i] == NULL) 
         ErrorExit("CreateThread error\n"); 
   } 
 
   for (i = 0; i < THREADCOUNT; i++) 
      WaitForSingleObject(hThread[i], INFINITE); 
 
   TlsFree(dwTlsIndex);

   return 0; 
} 
 
VOID ErrorExit (LPCSTR message)
{ 
   fprintf(stderr, "%s\n", message); 
   ExitProcess(0); 
}
```



## <a name="related-topics"></a><span data-ttu-id="4ef93-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="4ef93-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4ef93-111">使用 Dynamic-Link 程式庫中的執行緒區域儲存區</span><span class="sxs-lookup"><span data-stu-id="4ef93-111">Using Thread Local Storage in a Dynamic-Link Library</span></span>](../dlls/using-thread-local-storage-in-a-dynamic-link-library.md)
</dt> </dl>

 

 
