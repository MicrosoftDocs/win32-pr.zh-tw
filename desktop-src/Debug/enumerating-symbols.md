---
description: 下列程式碼會顯示指定模組中每個已載入符號的名稱、位址和大小。
ms.assetid: 6ecdbd1e-406a-453e-9037-707ceb72074a
title: 列舉符號
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33f9a98f37ca5ef2249f68ffa9b8ef73198de242
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936043"
---
# <a name="enumerating-symbols"></a><span data-ttu-id="3ce3e-103">列舉符號</span><span class="sxs-lookup"><span data-stu-id="3ce3e-103">Enumerating Symbols</span></span>

<span data-ttu-id="3ce3e-104">下列程式碼會顯示指定模組中每個已載入符號的名稱、位址和大小。</span><span class="sxs-lookup"><span data-stu-id="3ce3e-104">The following code displays the name, address, and size of each loaded symbol in the specified module.</span></span> <span data-ttu-id="3ce3e-105">[**SymEnumSymbols**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumsymbols)函式需要回呼函式，此函式會針對每個已載入的模組呼叫一次。</span><span class="sxs-lookup"><span data-stu-id="3ce3e-105">The [**SymEnumSymbols**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumsymbols) function requires a callback function, which is called once for each module loaded.</span></span> <span data-ttu-id="3ce3e-106">在此範例中，EnumSymProc 是回呼函式的實作為。</span><span class="sxs-lookup"><span data-stu-id="3ce3e-106">In this example, EnumSymProc is an implementation of the callback function.</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#include <dbghelp.h>

BOOL CALLBACK EnumSymProc( 
    PSYMBOL_INFO pSymInfo,   
    ULONG SymbolSize,      
    PVOID UserContext)
{
    UNREFERENCED_PARAMETER(UserContext);
    
    printf("%08X %4u %s\n", 
           pSymInfo->Address, SymbolSize, pSymInfo->Name);
    return TRUE;
}

void main()
{
    HANDLE hProcess = GetCurrentProcess();
    DWORD64 BaseOfDll;
    char *Mask = "*";
    BOOL status;

    status = SymInitialize(hProcess, NULL, FALSE);
    if (status == FALSE)
    {
        return;
    }
    
    BaseOfDll = SymLoadModuleEx(hProcess,
                                NULL,
                                "foo.dll",
                                NULL,
                                0,
                                0,
                                NULL,
                                0);
                                
    if (BaseOfDll == 0)
    {
        SymCleanup(hProcess);
        return;
    }                                
        
    if (SymEnumSymbols(hProcess,     // Process handle from SymInitialize.
                        BaseOfDll,   // Base address of module.
                        Mask,        // Name of symbols to match.
                        EnumSymProc, // Symbol handler procedure.
                        NULL))       // User context.
    {
        // SymEnumSymbols succeeded
    }
    else
    {
        // SymEnumSymbols failed
        printf("SymEnumSymbols failed: %d\n", GetLastError());
    }
    
    SymCleanup(hProcess);
}
```



 

 



