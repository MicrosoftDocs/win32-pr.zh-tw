---
description: 執行緒區域儲存 (TLS) 可讓相同進程的多個執行緒使用 TlsAlloc 函式所配置的索引，來儲存和取出執行緒的本機值。
ms.assetid: b7f5a206-a827-4b6b-86f6-5e3aea1246b7
title: 使用執行緒區域儲存體
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bdac1306a4a2da10e6a24ba2e1b2444f6215fdac39be7b41cc6850c1e5a683d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127988"
---
# <a name="using-thread-local-storage"></a>使用執行緒區域儲存體

[執行緒區域儲存](thread-local-storage.md) (TLS) 可讓相同進程的多個執行緒使用 [**TlsAlloc**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-tlsalloc) 函式所配置的索引，來儲存和取出執行緒的本機值。 在此範例中，會在處理常式啟動時配置索引。 當每個執行緒開始時，它會配置動態記憶體的區塊，並使用 [**TlsSetValue**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-tlssetvalue) 函式將指標儲存在 TLS 位置中。 CommonFunc 函式會使用 [**TlsGetValue**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-tlsgetvalue) 函數來存取與呼叫執行緒的本機索引相關聯的資料。 在每個執行緒終止之前，它會釋放其動態記憶體。 在進程終止之前，它會呼叫 [**TlsFree**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-tlsfree) 來釋放索引。


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



## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 Dynamic-Link 程式庫中的執行緒區域儲存體](../dlls/using-thread-local-storage-in-a-dynamic-link-library.md)
</dt> </dl>

 

 
