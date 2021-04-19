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
# <a name="using-thread-local-storage-in-a-dynamic-link-library"></a><span data-ttu-id="58675-103">使用 Dynamic-Link 程式庫中的執行緒區域儲存區</span><span class="sxs-lookup"><span data-stu-id="58675-103">Using Thread Local Storage in a Dynamic-Link Library</span></span>

<span data-ttu-id="58675-104">本節說明如何使用 DLL 進入點函數來設定執行緒區域儲存區 (TLS) 索引，為多執行緒處理的每個執行緒提供私用儲存。</span><span class="sxs-lookup"><span data-stu-id="58675-104">This section shows the use of a DLL entry-point function to set up a thread local storage (TLS) index to provide private storage for each thread of a multithreaded process.</span></span>

<span data-ttu-id="58675-105">TLS 索引會儲存在全域變數中，使其可供所有 DLL 函式使用。</span><span class="sxs-lookup"><span data-stu-id="58675-105">The TLS index is stored in a global variable, making it available to all of the DLL functions.</span></span> <span data-ttu-id="58675-106">此範例假設 DLL 的全域資料不是共用的，因為每個載入 DLL 的進程不一定會有相同的 TLS 索引。</span><span class="sxs-lookup"><span data-stu-id="58675-106">This example assumes that the DLL's global data is not shared, because the TLS index is not necessarily the same for each process that loads the DLL.</span></span>

<span data-ttu-id="58675-107">當進程載入 DLL 時，進入點函數會使用 [**TlsAlloc**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsalloc) 函式來配置 TLS 索引。</span><span class="sxs-lookup"><span data-stu-id="58675-107">The entry-point function uses the [**TlsAlloc**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsalloc) function to allocate a TLS index whenever a process loads the DLL.</span></span> <span data-ttu-id="58675-108">接著，每個執行緒都可以使用這個索引，將指標儲存至它自己的記憶體區塊。</span><span class="sxs-lookup"><span data-stu-id="58675-108">Each thread can then use this index to store a pointer to its own block of memory.</span></span>

<span data-ttu-id="58675-109">以 DLL 進程附加值呼叫進入點函數時 \_ ，程式 \_ 代碼會執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="58675-109">When the entry-point function is called with the DLL\_PROCESS\_ATTACH value, the code performs the following actions:</span></span>

1.  <span data-ttu-id="58675-110">使用 [**TlsAlloc**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsalloc) 函數來配置 TLS 索引。</span><span class="sxs-lookup"><span data-stu-id="58675-110">Uses the [**TlsAlloc**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsalloc) function to allocate a TLS index.</span></span>
2.  <span data-ttu-id="58675-111">配置記憶體區塊，以供進程的初始執行緒專用。</span><span class="sxs-lookup"><span data-stu-id="58675-111">Allocates a block of memory to be used exclusively by the initial thread of the process.</span></span>
3.  <span data-ttu-id="58675-112">在 [**TlsSetValue**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlssetvalue) 函式的呼叫中使用 TLS 索引，以將記憶體區塊的位址儲存在與索引相關聯的 TLS 位置中。</span><span class="sxs-lookup"><span data-stu-id="58675-112">Uses the TLS index in a call to the [**TlsSetValue**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlssetvalue) function to store the address of the memory block in the TLS slot associated with the index.</span></span>

<span data-ttu-id="58675-113">每次程式建立新的執行緒時，就會以 DLL \_ 執行緒附加值來呼叫進入點函數 \_ 。</span><span class="sxs-lookup"><span data-stu-id="58675-113">Each time the process creates a new thread, the entry-point function is called with the DLL\_THREAD\_ATTACH value.</span></span> <span data-ttu-id="58675-114">進入點函數接著會配置新執行緒的記憶體區塊，並使用 TLS 索引來儲存指標。</span><span class="sxs-lookup"><span data-stu-id="58675-114">The entry-point function then allocates a block of memory for the new thread and stores a pointer to it by using the TLS index.</span></span>

<span data-ttu-id="58675-115">當函數需要存取與 TLS 索引相關聯的資料時，請在 [**TlsGetValue**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsgetvalue) 函式的呼叫中指定索引。</span><span class="sxs-lookup"><span data-stu-id="58675-115">When a function requires access to the data associated with a TLS index, specify the index in a call to the [**TlsGetValue**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsgetvalue) function.</span></span> <span data-ttu-id="58675-116">這會針對呼叫執行緒抓取 TLS 位置的內容，在此案例中為數據之記憶體區塊的指標。</span><span class="sxs-lookup"><span data-stu-id="58675-116">This retrieves the contents of the TLS slot for the calling thread, which in this case is a pointer to the memory block for the data.</span></span> <span data-ttu-id="58675-117">當進程使用載入時間連結與此 DLL 時，進入點函數就足以管理執行緒區域儲存區。</span><span class="sxs-lookup"><span data-stu-id="58675-117">When a process uses load-time linking with this DLL, the entry-point function is sufficient to manage the thread local storage.</span></span> <span data-ttu-id="58675-118">使用執行時間連結的進程可能會發生問題，因為在呼叫 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 函式之前，不會針對存在的執行緒呼叫進入點函式，因此不會為這些執行緒配置 TLS 記憶體。</span><span class="sxs-lookup"><span data-stu-id="58675-118">Problems can occur with a process that uses run-time linking because the entry-point function is not called for threads that exist before the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) function is called, so TLS memory is not allocated for these threads.</span></span> <span data-ttu-id="58675-119">這個範例會藉由檢查 [**TlsGetValue**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsgetvalue) 函式所傳回的值，並在值指出未設定此執行緒的 TLS 位置時配置記憶體，藉此解決這個問題。</span><span class="sxs-lookup"><span data-stu-id="58675-119">This example solves this problem by checking the value returned by the [**TlsGetValue**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsgetvalue) function and allocating memory if the value indicates that the TLS slot for this thread is not set.</span></span>

<span data-ttu-id="58675-120">當每個執行緒不再需要使用 TLS 索引時，它必須釋放其指標儲存在 TLS 位置的記憶體。</span><span class="sxs-lookup"><span data-stu-id="58675-120">When each thread no longer needs to use a TLS index, it must free the memory whose pointer is stored in the TLS slot.</span></span> <span data-ttu-id="58675-121">當所有線程都已使用 TLS 索引完成時，請使用 [**TlsFree**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsfree) 函式來釋放索引。</span><span class="sxs-lookup"><span data-stu-id="58675-121">When all threads have finished using a TLS index, use the [**TlsFree**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsfree) function to release the index.</span></span>

<span data-ttu-id="58675-122">當執行緒終止時，會以 DLL 執行緒卸離值呼叫進入點函式， \_ \_ 並釋放該執行緒的記憶體。</span><span class="sxs-lookup"><span data-stu-id="58675-122">When a thread terminates, the entry-point function is called with the DLL\_THREAD\_DETACH value and the memory for that thread is freed.</span></span> <span data-ttu-id="58675-123">當進程終止時，會以 DLL 進程卸離值呼叫進入點函式， \_ \_ 而 TLS 索引中的指標所參考的記憶體則會釋放。</span><span class="sxs-lookup"><span data-stu-id="58675-123">When a process terminates, the entry-point function is called with the DLL\_PROCESS\_DETACH value and the memory referenced by the pointer in the TLS index is freed.</span></span>


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



<span data-ttu-id="58675-124">下列程式碼示範如何使用在前一個範例中定義的 DLL 函式。</span><span class="sxs-lookup"><span data-stu-id="58675-124">The following code demonstrates the use of the DLL functions defined in the previous example.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="58675-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="58675-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="58675-126">動態連結程式庫資料</span><span class="sxs-lookup"><span data-stu-id="58675-126">Dynamic-Link Library Data</span></span>](dynamic-link-library-data.md)
</dt> <dt>

[<span data-ttu-id="58675-127">使用執行緒區域儲存區</span><span class="sxs-lookup"><span data-stu-id="58675-127">Using Thread Local Storage</span></span>](/windows/desktop/ProcThread/using-thread-local-storage)
</dt> </dl>

 

 
