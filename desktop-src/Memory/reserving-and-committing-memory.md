---
description: 下列範例說明如何使用 VirtualAlloc 和 VirtualFree 函式，根據動態陣列的需要來保留和認可記憶體。
ms.assetid: f46bd57d-7684-4a08-8ac7-de204aecb207
title: 保留和認可記憶體
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 615f3c4321dc432b5ef83a841cea12215563e7d103443512a4d3b2c553849540
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118386276"
---
# <a name="reserving-and-committing-memory"></a>保留和認可記憶體

下列範例說明如何使用 [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) 和 [**VirtualFree**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfree) 函式，根據動態陣列的需要來保留和認可記憶體。 首先，呼叫 **VirtualAlloc** 以保留一組頁面，並將 **Null** 指定為基底位址參數，強制系統判斷區塊的位置。 之後，每當需要從這個保留區域認可頁面，並指定下一個要認可的頁面基底位址時，就會呼叫 **VirtualAlloc** 。

此範例會使用結構化例外狀況處理語法來認可保留區域中的頁面。 每當在執行 **\_ \_ try** 區塊期間發生分頁錯誤例外狀況時，就會執行 **\_ \_ except** 區塊前面的運算式中的篩選函數。 如果篩選函式可以配置另一個頁面，在發生例外狀況的位置，會在 **\_ \_ try** 區塊中繼續執行。 否則，會執行 **\_ \_ except** 區塊中的例外狀況處理常式。 如需詳細資訊，請參閱 [結構化例外狀況處理](../debug/structured-exception-handling.md)。

作為動態配置的替代方式，程式可以直接認可整個區域，而不是只保留它。 這兩種方法都會產生相同的實體記憶體使用量，因為在第一次存取之前，認可的頁面不會使用任何實體儲存體。 動態配置的優點是它可將系統上的已認可頁面總數降至最低。 針對非常大的配置，預先認可整個配置可能會導致系統用盡可認可的頁面，導致虛擬記憶體配置失敗。

**\_ \_ Except** 區塊中的 [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess)函式會自動釋放虛擬記憶體配置，因此不需要在程式終止此執行路徑時明確地釋放頁面。 如果程式是以停用例外狀況處理建立的， [**VirtualFree**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfree) 函式會釋出保留和認可的頁面。 此函式會使用 **記憶體 \_ 釋放** 來取消認可和釋放保留和認可頁面的整個區域。

下列 c + + 範例示範使用結構化例外狀況處理常式的動態記憶體配置。


```C++
// A short program to demonstrate dynamic memory allocation
// using a structured exception handler.

#include <windows.h>
#include <tchar.h>
#include <stdio.h>
#include <stdlib.h>             // For exit

#define PAGELIMIT 80            // Number of pages to ask for

LPTSTR lpNxtPage;               // Address of the next page to ask for
DWORD dwPages = 0;              // Count of pages gotten so far
DWORD dwPageSize;               // Page size on this computer

INT PageFaultExceptionFilter(DWORD dwCode)
{
    LPVOID lpvResult;

    // If the exception is not a page fault, exit.

    if (dwCode != EXCEPTION_ACCESS_VIOLATION)
    {
        _tprintf(TEXT("Exception code = %d.\n"), dwCode);
        return EXCEPTION_EXECUTE_HANDLER;
    }

    _tprintf(TEXT("Exception is a page fault.\n"));

    // If the reserved pages are used up, exit.

    if (dwPages >= PAGELIMIT)
    {
        _tprintf(TEXT("Exception: out of pages.\n"));
        return EXCEPTION_EXECUTE_HANDLER;
    }

    // Otherwise, commit another page.

    lpvResult = VirtualAlloc(
                     (LPVOID) lpNxtPage, // Next page to commit
                     dwPageSize,         // Page size, in bytes
                     MEM_COMMIT,         // Allocate a committed page
                     PAGE_READWRITE);    // Read/write access
    if (lpvResult == NULL )
    {
        _tprintf(TEXT("VirtualAlloc failed.\n"));
        return EXCEPTION_EXECUTE_HANDLER;
    }
    else
    {
        _tprintf(TEXT("Allocating another page.\n"));
    }

    // Increment the page count, and advance lpNxtPage to the next page.

    dwPages++;
    lpNxtPage = (LPTSTR) ((PCHAR) lpNxtPage + dwPageSize);

    // Continue execution where the page fault occurred.

    return EXCEPTION_CONTINUE_EXECUTION;
}

VOID ErrorExit(LPTSTR lpMsg)
{
    _tprintf(TEXT("Error! %s with error code of %ld.\n"),
             lpMsg, GetLastError ());
    exit (0);
}

VOID _tmain(VOID)
{
    LPVOID lpvBase;               // Base address of the test memory
    LPTSTR lpPtr;                 // Generic character pointer
    BOOL bSuccess;                // Flag
    DWORD i;                      // Generic counter
    SYSTEM_INFO sSysInfo;         // Useful information about the system

    GetSystemInfo(&sSysInfo);     // Initialize the structure.

    _tprintf (TEXT("This computer has page size %d.\n"), sSysInfo.dwPageSize);

    dwPageSize = sSysInfo.dwPageSize;

    // Reserve pages in the virtual address space of the process.

    lpvBase = VirtualAlloc(
                     NULL,                 // System selects address
                     PAGELIMIT*dwPageSize, // Size of allocation
                     MEM_RESERVE,          // Allocate reserved pages
                     PAGE_NOACCESS);       // Protection = no access
    if (lpvBase == NULL )
        ErrorExit(TEXT("VirtualAlloc reserve failed."));

    lpPtr = lpNxtPage = (LPTSTR) lpvBase;

    // Use structured exception handling when accessing the pages.
    // If a page fault occurs, the exception filter is executed to
    // commit another page from the reserved block of pages.

    for (i=0; i < PAGELIMIT*dwPageSize; i++)
    {
        __try
        {
            // Write to memory.

            lpPtr[i] = 'a';
        }

        // If there's a page fault, commit another page and try again.

        __except ( PageFaultExceptionFilter( GetExceptionCode() ) )
        {

            // This code is executed only if the filter function
            // is unsuccessful in committing the next page.

            _tprintf (TEXT("Exiting process.\n"));

            ExitProcess( GetLastError() );

        }

    }

    // Release the block of pages when you are finished using them.

    bSuccess = VirtualFree(
                       lpvBase,       // Base address of block
                       0,             // Bytes of committed pages
                       MEM_RELEASE);  // Decommit the pages

    _tprintf (TEXT("Release %s.\n"), bSuccess ? TEXT("succeeded") : TEXT("failed") );

}
```



 

 
