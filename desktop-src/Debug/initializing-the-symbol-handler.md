---
description: 下列程式碼示範如何初始化符號處理常式。
ms.assetid: e8c8f648-c3b0-4595-ac07-f508dd576d9f
title: 初始化符號處理常式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d5a7ba79a71a389f185a5e18065af818223d4cb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936101"
---
# <a name="initializing-the-symbol-handler"></a><span data-ttu-id="1f0b8-103">初始化符號處理常式</span><span class="sxs-lookup"><span data-stu-id="1f0b8-103">Initializing the Symbol Handler</span></span>

<span data-ttu-id="1f0b8-104">下列程式碼示範如何初始化符號處理常式。</span><span class="sxs-lookup"><span data-stu-id="1f0b8-104">The following code demonstrates how to initialize the symbol handler.</span></span> <span data-ttu-id="1f0b8-105">[**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions)函式會延遲符號載入，直到要求符號資訊為止。</span><span class="sxs-lookup"><span data-stu-id="1f0b8-105">The [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) function defers symbol loading until symbol information is requested.</span></span> <span data-ttu-id="1f0b8-106">程式碼會針對 [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize)函式的 *BInvade* 參數傳遞 **TRUE** 值，以載入指定進程中每個模組的符號。</span><span class="sxs-lookup"><span data-stu-id="1f0b8-106">The code loads the symbols for each module in the specified process by passing a value of **TRUE** for the *bInvade* parameter of the [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) function.</span></span> <span data-ttu-id="1f0b8-107"> (此函式會針對進程已對應至其位址空間的每個模組，呼叫 [**SymLoadModule64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmodule) 函式。 ) </span><span class="sxs-lookup"><span data-stu-id="1f0b8-107">(This function calls the [**SymLoadModule64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmodule) function for each module the process has mapped into its address space.)</span></span>

<span data-ttu-id="1f0b8-108">如果指定的進程不是呼叫 [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize)的進程，則程式碼會傳遞處理序識別碼做為 **SymInitialize** 的第一個參數。</span><span class="sxs-lookup"><span data-stu-id="1f0b8-108">If the specified process is not the process that called [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize), the code passes a process identifier as the first parameter of **SymInitialize**.</span></span>

<span data-ttu-id="1f0b8-109">將 **Null** 指定為 [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) 的第二個參數，表示符號處理常式應該使用預設搜尋路徑來尋找符號檔。</span><span class="sxs-lookup"><span data-stu-id="1f0b8-109">Specifying **NULL** as the second parameter of [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) indicates that the symbol handler should use the default search path to locate symbol files.</span></span> <span data-ttu-id="1f0b8-110">如需有關符號處理常式如何尋找符號檔或應用程式如何指定符號搜尋路徑的詳細資訊，請參閱 [符號路徑](symbol-paths.md)。</span><span class="sxs-lookup"><span data-stu-id="1f0b8-110">For detailed information on how the symbol handler locates symbol files or how an application can specify a symbol search path, see [Symbol Paths](symbol-paths.md).</span></span>


```C++
DWORD  error;
HANDLE hProcess;

SymSetOptions(SYMOPT_UNDNAME | SYMOPT_DEFERRED_LOADS);

hProcess = GetCurrentProcess();

if (!SymInitialize(hProcess, NULL, TRUE))
{
    // SymInitialize failed
    error = GetLastError();
    printf("SymInitialize returned error : %d\n", error);
    return FALSE;
}
```



 

 



