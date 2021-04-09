---
description: 下列範例示範 DLL 進入點函式如何使用檔案對應物件來設定可由載入 DLL 之進程共用的記憶體。
ms.assetid: ab751ab1-3b40-4111-b724-9f8676b722a3
title: 使用 Dynamic-Link 程式庫中的共用記憶體
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 978a6fa77964c6404b3f85e9c9bcec6c3644f2ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848418"
---
# <a name="using-shared-memory-in-a-dynamic-link-library"></a><span data-ttu-id="f02f2-103">使用 Dynamic-Link 程式庫中的共用記憶體</span><span class="sxs-lookup"><span data-stu-id="f02f2-103">Using Shared Memory in a Dynamic-Link Library</span></span>

<span data-ttu-id="f02f2-104">下列範例示範 DLL 進入點函式如何使用檔案對應物件來設定可由載入 DLL 之進程共用的記憶體。</span><span class="sxs-lookup"><span data-stu-id="f02f2-104">The following example demonstrates how the DLL entry-point function can use a file-mapping object to set up memory that can be shared by processes that load the DLL.</span></span> <span data-ttu-id="f02f2-105">只要載入 DLL，共用 DLL 記憶體就會持續存在。</span><span class="sxs-lookup"><span data-stu-id="f02f2-105">The shared DLL memory persists only as long as the DLL is loaded.</span></span> <span data-ttu-id="f02f2-106">應用程式可以使用 SetSharedMem 和 GetSharedMem 函數來存取共用記憶體。</span><span class="sxs-lookup"><span data-stu-id="f02f2-106">Applications can use the SetSharedMem and GetSharedMem functions to access the shared memory.</span></span>

## <a name="dll-that-implements-the-shared-memory"></a><span data-ttu-id="f02f2-107">執行共用記憶體的 DLL</span><span class="sxs-lookup"><span data-stu-id="f02f2-107">DLL that Implements the Shared Memory</span></span>

<span data-ttu-id="f02f2-108">此範例使用檔案對應，將命名空間共用記憶體的區塊對應至載入 DLL 之每個進程的虛擬位址空間。</span><span class="sxs-lookup"><span data-stu-id="f02f2-108">The example uses file mapping to map a block of named shared memory into the virtual address space of each process that loads the DLL.</span></span> <span data-ttu-id="f02f2-109">若要這樣做，進入點函數必須：</span><span class="sxs-lookup"><span data-stu-id="f02f2-109">To do this, the entry-point function must:</span></span>

1.  <span data-ttu-id="f02f2-110">呼叫 [**CreateFileMapping**](/windows/desktop/api/winbase/nf-winbase-createfilemappinga) 函數，以取得檔案對應物件的控制碼。</span><span class="sxs-lookup"><span data-stu-id="f02f2-110">Call the [**CreateFileMapping**](/windows/desktop/api/winbase/nf-winbase-createfilemappinga) function to get a handle to a file-mapping object.</span></span> <span data-ttu-id="f02f2-111">載入 DLL 的第一個進程會建立檔案對應物件。</span><span class="sxs-lookup"><span data-stu-id="f02f2-111">The first process that loads the DLL creates the file-mapping object.</span></span> <span data-ttu-id="f02f2-112">後續的進程會開啟現有物件的控制碼。</span><span class="sxs-lookup"><span data-stu-id="f02f2-112">Subsequent processes open a handle to the existing object.</span></span> <span data-ttu-id="f02f2-113">如需詳細資訊，請參閱 [建立 File-Mapping 物件](/windows/desktop/Memory/creating-a-file-mapping-object)。</span><span class="sxs-lookup"><span data-stu-id="f02f2-113">For more information, see [Creating a File-Mapping Object](/windows/desktop/Memory/creating-a-file-mapping-object).</span></span>
2.  <span data-ttu-id="f02f2-114">呼叫 [**MapViewOfFile**](/windows/desktop/api/memoryapi/nf-memoryapi-mapviewoffile) 函式，將視圖對應至虛擬位址空間。</span><span class="sxs-lookup"><span data-stu-id="f02f2-114">Call the [**MapViewOfFile**](/windows/desktop/api/memoryapi/nf-memoryapi-mapviewoffile) function to map a view into the virtual address space.</span></span> <span data-ttu-id="f02f2-115">這可讓進程存取共用記憶體。</span><span class="sxs-lookup"><span data-stu-id="f02f2-115">This enables the process to access the shared memory.</span></span> <span data-ttu-id="f02f2-116">如需詳細資訊，請參閱 [建立檔案視圖](/windows/desktop/Memory/creating-a-file-view)。</span><span class="sxs-lookup"><span data-stu-id="f02f2-116">For more information, see [Creating a File View](/windows/desktop/Memory/creating-a-file-view).</span></span>

<span data-ttu-id="f02f2-117">請注意，雖然您可以藉由針對 [**CreateFileMapping**](/windows/desktop/api/winbase/nf-winbase-createfilemappinga)的 *LPATTRIBUTES* 參數傳遞 Null 值來指定預設安全性屬性，但您可以選擇使用 [**安全性 \_ 屬性**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85))結構來提供額外的安全性。</span><span class="sxs-lookup"><span data-stu-id="f02f2-117">Note that while you can specify default security attributes by passing in a NULL value for the *lpAttributes* parameter of [**CreateFileMapping**](/windows/desktop/api/winbase/nf-winbase-createfilemappinga), you may choose to use a [**SECURITY\_ATTRIBUTES**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) structure to provide additional security.</span></span>


```C++
// The DLL code

#include <windows.h> 
#include <memory.h> 
 
#define SHMEMSIZE 4096 
 
static LPVOID lpvMem = NULL;      // pointer to shared memory
static HANDLE hMapObject = NULL;  // handle to file mapping

// The DLL entry-point function sets up shared memory using a 
// named file-mapping object. 
 
BOOL WINAPI DllMain(HINSTANCE hinstDLL,  // DLL module handle
    DWORD fdwReason,              // reason called 
    LPVOID lpvReserved)           // reserved 
{ 
    BOOL fInit, fIgnore; 
 
    switch (fdwReason) 
    { 
        // DLL load due to process initialization or LoadLibrary
 
          case DLL_PROCESS_ATTACH: 
 
            // Create a named file mapping object
 
            hMapObject = CreateFileMapping( 
                INVALID_HANDLE_VALUE,   // use paging file
                NULL,                   // default security attributes
                PAGE_READWRITE,         // read/write access
                0,                      // size: high 32-bits
                SHMEMSIZE,              // size: low 32-bits
                TEXT("dllmemfilemap")); // name of map object
            if (hMapObject == NULL) 
                return FALSE; 
 
            // The first process to attach initializes memory
 
            fInit = (GetLastError() != ERROR_ALREADY_EXISTS); 
 
            // Get a pointer to the file-mapped shared memory
 
            lpvMem = MapViewOfFile( 
                hMapObject,     // object to map view of
                FILE_MAP_WRITE, // read/write access
                0,              // high offset:  map from
                0,              // low offset:   beginning
                0);             // default: map entire file
            if (lpvMem == NULL) 
                return FALSE; 
 
            // Initialize memory if this is the first process
 
            if (fInit) 
                memset(lpvMem, '\0', SHMEMSIZE); 
 
            break; 
 
        // The attached process creates a new thread
 
        case DLL_THREAD_ATTACH: 
            break; 
 
        // The thread of the attached process terminates
 
        case DLL_THREAD_DETACH: 
            break; 
 
        // DLL unload due to process termination or FreeLibrary
 
        case DLL_PROCESS_DETACH: 
 
            // Unmap shared memory from the process's address space
 
            fIgnore = UnmapViewOfFile(lpvMem); 
 
            // Close the process's handle to the file-mapping object
 
            fIgnore = CloseHandle(hMapObject); 
 
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
 
// SetSharedMem sets the contents of the shared memory 
 
__declspec(dllexport) VOID __cdecl SetSharedMem(LPWSTR lpszBuf) 
{ 
    LPWSTR lpszTmp; 
    DWORD dwCount=1;
 
    // Get the address of the shared memory block
 
    lpszTmp = (LPWSTR) lpvMem; 
 
    // Copy the null-terminated string into shared memory
 
    while (*lpszBuf && dwCount<SHMEMSIZE) 
    {
        *lpszTmp++ = *lpszBuf++; 
        dwCount++;
    }
    *lpszTmp = '\0'; 
} 
 
// GetSharedMem gets the contents of the shared memory
 
__declspec(dllexport) VOID __cdecl GetSharedMem(LPWSTR lpszBuf, DWORD cchSize) 
{ 
    LPWSTR lpszTmp; 
 
    // Get the address of the shared memory block
 
    lpszTmp = (LPWSTR) lpvMem; 
 
    // Copy from shared memory into the caller's buffer
 
    while (*lpszTmp && --cchSize) 
        *lpszBuf++ = *lpszTmp++; 
    *lpszBuf = '\0'; 
}
#ifdef __cplusplus
}
#endif
```



<span data-ttu-id="f02f2-118">共用記憶體可以對應到每個進程中的不同位址。</span><span class="sxs-lookup"><span data-stu-id="f02f2-118">Shared memory can be mapped to a different address in each process.</span></span> <span data-ttu-id="f02f2-119">基於這個理由，每個進程都有自己的 lpvMem 實例，該實例宣告為全域變數，因此可供所有 DLL 函式使用。</span><span class="sxs-lookup"><span data-stu-id="f02f2-119">For this reason, each process has its own instance of lpvMem, which is declared as a global variable so that it is available to all DLL functions.</span></span> <span data-ttu-id="f02f2-120">此範例假設 DLL 全域資料不是共用的，因此載入 DLL 的每個進程都有自己的 lpvMem 實例。</span><span class="sxs-lookup"><span data-stu-id="f02f2-120">The example assumes that the DLL global data is not shared, so each process that loads the DLL has its own instance of lpvMem.</span></span>

<span data-ttu-id="f02f2-121">請注意，當檔案對應物件的最後控制碼關閉時，就會釋放共用記憶體。</span><span class="sxs-lookup"><span data-stu-id="f02f2-121">Note that the shared memory is released when the last handle to the file-mapping object is closed.</span></span> <span data-ttu-id="f02f2-122">若要建立持續的共用記憶體，您必須確定某個進程一律具有檔案對應物件的開啟控制碼。</span><span class="sxs-lookup"><span data-stu-id="f02f2-122">To create persistent shared memory, you would need to ensure that some process always has an open handle to the file-mapping object.</span></span>

## <a name="processes-that-use-the-shared-memory"></a><span data-ttu-id="f02f2-123">使用共用記憶體的進程</span><span class="sxs-lookup"><span data-stu-id="f02f2-123">Processes that Use the Shared Memory</span></span>

<span data-ttu-id="f02f2-124">下列進程會使用上面定義之 DLL 所提供的共用記憶體。</span><span class="sxs-lookup"><span data-stu-id="f02f2-124">The following processes use the shared memory provided by the DLL defined above.</span></span> <span data-ttu-id="f02f2-125">第一個進程會呼叫 SetSharedMem 來寫入字串，而第二個進程會呼叫 GetSharedMem 來取出這個字串。</span><span class="sxs-lookup"><span data-stu-id="f02f2-125">The first process calls SetSharedMem to write a string while the second process calls GetSharedMem to retrieve this string.</span></span>

<span data-ttu-id="f02f2-126">此程式會使用 DLL 所執行的 SetSharedMem 函式，將字串「此為測試字串」寫入共用記憶體。</span><span class="sxs-lookup"><span data-stu-id="f02f2-126">This process uses the SetSharedMem function implemented by the DLL to write the string "This is a test string" to the shared memory.</span></span> <span data-ttu-id="f02f2-127">它也會啟動子進程，以從共用記憶體讀取字串。</span><span class="sxs-lookup"><span data-stu-id="f02f2-127">It also starts a child process that will read the string from the shared memory.</span></span>


```C++
// Parent process

#include <windows.h>
#include <tchar.h>
#include <stdio.h>

extern "C" VOID __cdecl SetSharedMem(LPWSTR lpszBuf);

HANDLE CreateChildProcess(LPTSTR szCmdline) 
{ 
   PROCESS_INFORMATION piProcInfo; 
   STARTUPINFO siStartInfo;
   BOOL bFuncRetn = FALSE; 
 
// Set up members of the PROCESS_INFORMATION structure. 
 
   ZeroMemory( &piProcInfo, sizeof(PROCESS_INFORMATION) );
 
// Set up members of the STARTUPINFO structure. 
 
   ZeroMemory( &siStartInfo, sizeof(STARTUPINFO) );
   siStartInfo.cb = sizeof(STARTUPINFO); 
 
// Create the child process. 
    
   bFuncRetn = CreateProcess(NULL, 
      szCmdline,     // command line 
      NULL,          // process security attributes 
      NULL,          // primary thread security attributes 
      TRUE,          // handles are inherited 
      0,             // creation flags 
      NULL,          // use parent's environment 
      NULL,          // use parent's current directory 
      &siStartInfo,  // STARTUPINFO pointer 
      &piProcInfo);  // receives PROCESS_INFORMATION 
   
   if (bFuncRetn == 0) 
   {
      printf("CreateProcess failed (%)\n", GetLastError());
      return INVALID_HANDLE_VALUE;
   }
   else 
   {
      CloseHandle(piProcInfo.hThread);
      return piProcInfo.hProcess;
   }
}

int _tmain(int argc, TCHAR *argv[])
{
   HANDLE hProcess;

   if (argc == 1) 
   {
      printf("Please specify an input file");
      ExitProcess(0);
   }

   // Call the DLL function
   printf("\nProcess is writing to shared memory...\n\n");
   SetSharedMem(L"This is a test string");

   // Start the child process that will read the memory
   hProcess = CreateChildProcess(argv[1]);

   // Ensure this process is around until the child process terminates
   if (INVALID_HANDLE_VALUE != hProcess) 
   {
      WaitForSingleObject(hProcess, INFINITE);
      CloseHandle(hProcess);
   }
   return 0;
}

```



<span data-ttu-id="f02f2-128">此程式會使用 DLL 所執行的 GetSharedMem 函式，從共用記憶體讀取字串。</span><span class="sxs-lookup"><span data-stu-id="f02f2-128">This process uses the GetSharedMem function implemented by the DLL to read a string from the shared memory.</span></span> <span data-ttu-id="f02f2-129">它是由上述父進程啟動。</span><span class="sxs-lookup"><span data-stu-id="f02f2-129">It is started by the parent process above.</span></span>


```C++
// Child process

#include <windows.h>
#include <tchar.h>
#include <stdio.h>

extern "C" VOID __cdecl GetSharedMem(LPWSTR lpszBuf, DWORD cchSize);

int _tmain( void )
{
    WCHAR cBuf[MAX_PATH];

    GetSharedMem(cBuf, MAX_PATH);
 
    printf("Child process read from shared memory: %S\n", cBuf);
    
    return 0;
}
```



## <a name="related-topics"></a><span data-ttu-id="f02f2-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="f02f2-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f02f2-131">動態連結程式庫資料</span><span class="sxs-lookup"><span data-stu-id="f02f2-131">Dynamic-Link Library Data</span></span>](dynamic-link-library-data.md)
</dt> </dl>

 

 
