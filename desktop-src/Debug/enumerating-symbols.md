---
description: 下列程式碼會顯示指定模組中每個已載入符號的名稱、位址和大小。
ms.assetid: 6ecdbd1e-406a-453e-9037-707ceb72074a
title: 列舉符號
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 041768d46fec2aada74ebef37fdf5ffbb719b7c691a5e037a0f2f0532390d54e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119692028"
---
# <a name="enumerating-symbols"></a>列舉符號

下列程式碼會顯示指定模組中每個已載入符號的名稱、位址和大小。 [**SymEnumSymbols**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumsymbols)函式需要回呼函式，此函式會針對每個已載入的模組呼叫一次。 在此範例中，EnumSymProc 是回呼函式的實作為。


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



 

 



