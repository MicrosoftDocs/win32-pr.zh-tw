---
description: 下列程式碼會列出 SymLoadModule64 或 SymInitialize 函數所載入的模組。
ms.assetid: 8c7fdfaa-d4d3-42d6-ad19-23e8ffda7bf4
title: 列舉符號模組
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43623a7409116450fccc822bbc0bef1a309fbd2a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104467949"
---
# <a name="enumerating-symbol-modules"></a><span data-ttu-id="27bb7-103">列舉符號模組</span><span class="sxs-lookup"><span data-stu-id="27bb7-103">Enumerating Symbol Modules</span></span>

<span data-ttu-id="27bb7-104">下列程式碼會列出 [**SymLoadModule64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmodule) 或 [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) 函數所載入的模組。</span><span class="sxs-lookup"><span data-stu-id="27bb7-104">The following code lists the modules that have been loaded by the [**SymLoadModule64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmodule) or [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) function.</span></span> <span data-ttu-id="27bb7-105">[**SymEnumerateModules64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumeratemodules)函式需要回呼函式，每個載入的模組會呼叫一次。</span><span class="sxs-lookup"><span data-stu-id="27bb7-105">The [**SymEnumerateModules64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumeratemodules) function requires a callback function, which will be called once for each module loaded.</span></span> <span data-ttu-id="27bb7-106">在此範例中，EnumModules 是回呼函式的實作為。</span><span class="sxs-lookup"><span data-stu-id="27bb7-106">In this example, EnumModules is an implementation of the callback function.</span></span> <span data-ttu-id="27bb7-107">此範例假設您已使用 [初始化符號處理常式](initializing-the-symbol-handler.md)中的程式碼，初始化符號處理常式。</span><span class="sxs-lookup"><span data-stu-id="27bb7-107">The example assumes you have initialized the symbol handler using the code in [Initializing the Symbol Handler](initializing-the-symbol-handler.md).</span></span>


```C++
BOOL CALLBACK EnumModules(
    PCTSTR  ModuleName, 
    DWORD64 BaseOfDll,  
    PVOID   UserContext )
{
    UNREFERENCED_PARAMETER(UserContext);
    
    _tprintf(TEXT("%08X %s\n"), BaseOfDll, ModuleName);
    return TRUE;
}


if (SymEnumerateModules64(hProcess, EnumModules, NULL))
{
    // SymEnumerateModules64 returned success
}
else
{
    // SymEnumerateModules64 failed
    error = GetLastError();
    _tprintf(TEXT("SymEnumerateModules64 returned error : %d\n"), error);
}
```



 

 



