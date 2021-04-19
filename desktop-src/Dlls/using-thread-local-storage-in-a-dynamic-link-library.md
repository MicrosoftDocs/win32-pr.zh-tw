---
description: 本節說明如何使用 DLL 進入點函數來設定執行緒區域儲存區 (TLS) 索引，為多執行緒處理的每個執行緒提供私用儲存。
ms.assetid: a300f223-b513-4a22-a7a4-5d98cf74d77d
title: 使用 Dynamic-Link 程式庫中的執行緒區域儲存區
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 261ef7482520b4cb6e6c7b630f10ebb456231283
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973907"
---
# <a name="using-thread-local-storage-in-a-dynamic-link-library"></a>使用 Dynamic-Link 程式庫中的執行緒區域儲存區

本節說明如何使用 DLL 進入點函數來設定執行緒區域儲存區 (TLS) 索引，為多執行緒處理的每個執行緒提供私用儲存。

TLS 索引會儲存在全域變數中，使其可供所有 DLL 函式使用。 此範例假設 DLL 的全域資料不是共用的，因為每個載入 DLL 的進程不一定會有相同的 TLS 索引。

當進程載入 DLL 時，進入點函數會使用 [**TlsAlloc**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsalloc) 函式來配置 TLS 索引。 接著，每個執行緒都可以使用這個索引，將指標儲存至它自己的記憶體區塊。

以 DLL 進程附加值呼叫進入點函數時 \_ ，程式 \_ 代碼會執行下列動作：

1.  使用 [**TlsAlloc**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsalloc) 函數來配置 TLS 索引。
2.  配置記憶體區塊，以供進程的初始執行緒專用。
3.  在 [**TlsSetValue**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlssetvalue) 函式的呼叫中使用 TLS 索引，以將記憶體區塊的位址儲存在與索引相關聯的 TLS 位置中。

每次程式建立新的執行緒時，就會以 DLL \_ 執行緒附加值來呼叫進入點函數 \_ 。 進入點函數接著會配置新執行緒的記憶體區塊，並使用 TLS 索引來儲存指標。

當函數需要存取與 TLS 索引相關聯的資料時，請在 [**TlsGetValue**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsgetvalue) 函式的呼叫中指定索引。 這會針對呼叫執行緒抓取 TLS 位置的內容，在此案例中為數據之記憶體區塊的指標。 當進程使用載入時間連結與此 DLL 時，進入點函數就足以管理執行緒區域儲存區。 使用執行時間連結的進程可能會發生問題，因為在呼叫 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 函式之前，不會針對存在的執行緒呼叫進入點函式，因此不會為這些執行緒配置 TLS 記憶體。 這個範例會藉由檢查 [**TlsGetValue**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsgetvalue) 函式所傳回的值，並在值指出未設定此執行緒的 TLS 位置時配置記憶體，藉此解決這個問題。

當每個執行緒不再需要使用 TLS 索引時，它必須釋放其指標儲存在 TLS 位置的記憶體。 當所有線程都已使用 TLS 索引完成時，請使用 [**TlsFree**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsfree) 函式來釋放索引。

當執行緒終止時，會以 DLL 執行緒卸離值呼叫進入點函式， \_ \_ 並釋放該執行緒的記憶體。 當進程終止時，會以 DLL 進程卸離值呼叫進入點函式， \_ \_ 而 TLS 索引中的指標所參考的記憶體則會釋放。


```C++
// The DLL code

#include <windows.h>

static DWORD dwTlsIndex; // address of shared memory
 
// DllMain() is the entry-point function for this DLL. 
 
BOOL WINAPI DllMain(HINSTANCE hinstDLL, // DLL module handle
    DWORD fdwReason,                    // reason called
    LPVOID lpvReserved)                 // reserved
{ 
    LPVOID lpvData; 
    BOOL fIgnore; 
 
    switch (fdwReason) 
    { 
        // The DLL is loading due to process 
        // initialization or a call to LoadLibrary. 
 
        case DLL_PROCESS_ATTACH: 
 
            // Allocate a TLS index.
 
            if ((dwTlsIndex = TlsAlloc()) == TLS_OUT_OF_INDEXES) 
                return FALSE; 
 
            // No break: Initialize the index for first thread.
 
        // The attached process creates a new thread. 
 
        case DLL_THREAD_ATTACH: 
 
            // Initialize the TLS index for this thread.
 
            lpvData = (LPVOID) LocalAlloc(LPTR, 256); 
            if (lpvData != NULL) 
                fIgnore = TlsSetValue(dwTlsIndex, lpvData); 
 
            break; 
 
        // The thread of the attached process terminates.
 
        case DLL_THREAD_DETACH: 
 
            // Release the allocated memory for this thread.
 
            lpvData = TlsGetValue(dwTlsIndex); 
            if (lpvData != NULL) 
                LocalFree((HLOCAL) lpvData); 
 
            break; 
 
        // DLL unload due to process termination or FreeLibrary. 
 
        case DLL_PROCESS_DETACH: 
 
            // Release the allocated memory for this thread.
 
            lpvData = TlsGetValue(dwTlsIndex); 
            if (lpvData != NULL) 
                LocalFree((HLOCAL) lpvData); 
 
            // Release the TLS index.
 
            TlsFree(dwTlsIndex); 
            break; 
 
        default: 
            break; 
    } 
 
    return TRUE; 
    UNREFERENCED_PARAMETER(hinstDLL); 
    UNREFERENCED_PARAMETER(lpvReserved); 
}

// The export mechanism used here is the __declspec(export)
// method supported by Microsoft Visual Studio, but any
// other export method supported by your development
// environment may be substituted.

#ifdef __cplusplus    // If used by C++ code, 
extern "C" {          // we need to export the C interface
#endif

__declspec(dllexport)
BOOL WINAPI StoreData(DWORD dw)
{
   LPVOID lpvData; 
   DWORD * pData;  // The stored memory pointer 

   lpvData = TlsGetValue(dwTlsIndex); 
   if (lpvData == NULL)
   {
      lpvData = (LPVOID) LocalAlloc(LPTR, 256); 
      if (lpvData == NULL) 
         return FALSE;
      if (!TlsSetValue(dwTlsIndex, lpvData))
         return FALSE;
   }

   pData = (DWORD *) lpvData; // Cast to my data type.
   // In this example, it is only a pointer to a DWORD
   // but it can be a structure pointer to contain more complicated data.

   (*pData) = dw;
   return TRUE;
}

__declspec(dllexport)
BOOL WINAPI GetData(DWORD *pdw)
{
   LPVOID lpvData; 
   DWORD * pData;  // The stored memory pointer 

   lpvData = TlsGetValue(dwTlsIndex); 
   if (lpvData == NULL)
      return FALSE;

   pData = (DWORD *) lpvData;
   (*pdw) = (*pData);
   return TRUE;
}
#ifdef __cplusplus
}
#endif
```



下列程式碼示範如何使用在前一個範例中定義的 DLL 函式。


```C++
#include <windows.h> 
#include <stdio.h> 
 
#define THREADCOUNT 4 
#define DLL_NAME TEXT("testdll")

VOID ErrorExit(LPSTR); 

extern "C" BOOL WINAPI StoreData(DWORD dw);
extern "C" BOOL WINAPI GetData(DWORD *pdw);
 
DWORD WINAPI ThreadFunc(VOID) 
{   
   int i;

   if(!StoreData(GetCurrentThreadId()))
      ErrorExit("StoreData error");

   for(i=0; i<THREADCOUNT; i++)
   {
      DWORD dwOut;
      if(!GetData(&dwOut))
         ErrorExit("GetData error");
      if( dwOut != GetCurrentThreadId())
         printf("thread %d: data is incorrect (%d)\n", GetCurrentThreadId(), dwOut);
      else printf("thread %d: data is correct\n", GetCurrentThreadId());
      Sleep(0);
   }
   return 0; 
} 
 
int main(VOID) 
{ 
   DWORD IDThread; 
   HANDLE hThread[THREADCOUNT]; 
   int i; 
   HMODULE hm;
 
// Load the DLL

   hm = LoadLibrary(DLL_NAME);
   if(!hm)
   {
      ErrorExit("DLL failed to load");
   }

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
 
   WaitForMultipleObjects(THREADCOUNT, hThread, TRUE, INFINITE); 

   FreeLibrary(hm);
 
   return 0; 
} 
 
VOID ErrorExit (LPSTR lpszMessage) 
{ 
   fprintf(stderr, "%s\n", lpszMessage); 
   ExitProcess(0); 
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[動態連結程式庫資料](dynamic-link-library-data.md)
</dt> <dt>

[使用執行緒區域儲存區](/windows/desktop/ProcThread/using-thread-local-storage)
</dt> </dl>

 

 
