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
# <a name="using-shared-memory-in-a-dynamic-link-library"></a>使用 Dynamic-Link 程式庫中的共用記憶體

下列範例示範 DLL 進入點函式如何使用檔案對應物件來設定可由載入 DLL 之進程共用的記憶體。 只要載入 DLL，共用 DLL 記憶體就會持續存在。 應用程式可以使用 SetSharedMem 和 GetSharedMem 函數來存取共用記憶體。

## <a name="dll-that-implements-the-shared-memory"></a>執行共用記憶體的 DLL

此範例使用檔案對應，將命名空間共用記憶體的區塊對應至載入 DLL 之每個進程的虛擬位址空間。 若要這樣做，進入點函數必須：

1.  呼叫 [**CreateFileMapping**](/windows/desktop/api/winbase/nf-winbase-createfilemappinga) 函數，以取得檔案對應物件的控制碼。 載入 DLL 的第一個進程會建立檔案對應物件。 後續的進程會開啟現有物件的控制碼。 如需詳細資訊，請參閱 [建立 File-Mapping 物件](/windows/desktop/Memory/creating-a-file-mapping-object)。
2.  呼叫 [**MapViewOfFile**](/windows/desktop/api/memoryapi/nf-memoryapi-mapviewoffile) 函式，將視圖對應至虛擬位址空間。 這可讓進程存取共用記憶體。 如需詳細資訊，請參閱 [建立檔案視圖](/windows/desktop/Memory/creating-a-file-view)。

請注意，雖然您可以藉由針對 [**CreateFileMapping**](/windows/desktop/api/winbase/nf-winbase-createfilemappinga)的 *LPATTRIBUTES* 參數傳遞 Null 值來指定預設安全性屬性，但您可以選擇使用 [**安全性 \_ 屬性**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85))結構來提供額外的安全性。


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



共用記憶體可以對應到每個進程中的不同位址。 基於這個理由，每個進程都有自己的 lpvMem 實例，該實例宣告為全域變數，因此可供所有 DLL 函式使用。 此範例假設 DLL 全域資料不是共用的，因此載入 DLL 的每個進程都有自己的 lpvMem 實例。

請注意，當檔案對應物件的最後控制碼關閉時，就會釋放共用記憶體。 若要建立持續的共用記憶體，您必須確定某個進程一律具有檔案對應物件的開啟控制碼。

## <a name="processes-that-use-the-shared-memory"></a>使用共用記憶體的進程

下列進程會使用上面定義之 DLL 所提供的共用記憶體。 第一個進程會呼叫 SetSharedMem 來寫入字串，而第二個進程會呼叫 GetSharedMem 來取出這個字串。

此程式會使用 DLL 所執行的 SetSharedMem 函式，將字串「此為測試字串」寫入共用記憶體。 它也會啟動子進程，以從共用記憶體讀取字串。


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



此程式會使用 DLL 所執行的 GetSharedMem 函式，從共用記憶體讀取字串。 它是由上述父進程啟動。


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



## <a name="related-topics"></a>相關主題

<dl> <dt>

[動態連結程式庫資料](dynamic-link-library-data.md)
</dt> </dl>

 

 
