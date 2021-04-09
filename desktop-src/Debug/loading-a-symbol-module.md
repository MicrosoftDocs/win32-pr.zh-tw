---
description: 如果應用程式未呼叫 SymInitialize 函式，並將 fInvadeProcess 參數設為 TRUE，它就必須在需要時載入模組的符號。
ms.assetid: 01cee812-d1f2-4459-acee-bce8719a85b2
title: 載入符號模組
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5182322e62b450333a064069ea5f5de2aa95e912
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110149"
---
# <a name="loading-a-symbol-module"></a><span data-ttu-id="aa59d-103">載入符號模組</span><span class="sxs-lookup"><span data-stu-id="aa59d-103">Loading a Symbol Module</span></span>

<span data-ttu-id="aa59d-104">如果應用程式未呼叫 [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) 函式，並將 *fInvadeProcess* 參數設為 **TRUE**，它就必須在需要時載入模組的符號。</span><span class="sxs-lookup"><span data-stu-id="aa59d-104">If an application does not call the [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) function with the *fInvadeProcess* parameter set to **TRUE**, it must load symbols for a module when they are required.</span></span> <span data-ttu-id="aa59d-105">若要視需要載入符號模組，應用程式可以使用模組名稱的完整路徑來呼叫 [**SymLoadModuleEx**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmoduleex) 函數。</span><span class="sxs-lookup"><span data-stu-id="aa59d-105">To load a symbol module on demand, the application can call the [**SymLoadModuleEx**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmoduleex) function with a full path to a module name.</span></span> <span data-ttu-id="aa59d-106">載入模組時，符號處理常式會立即載入符號或延遲載入，視使用 [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) 函式所設定的選項而定。</span><span class="sxs-lookup"><span data-stu-id="aa59d-106">When the module is loaded, the symbol handler will either load the symbols immediately or defer the load, depending on the options set using the [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) function.</span></span>

<span data-ttu-id="aa59d-107">下列程式碼會載入符號模組。</span><span class="sxs-lookup"><span data-stu-id="aa59d-107">The following code loads a symbol module.</span></span> <span data-ttu-id="aa59d-108">請注意，它會假設您已使用 [初始化符號處理常式](initializing-the-symbol-handler.md)中的程式碼來初始化符號處理常式。</span><span class="sxs-lookup"><span data-stu-id="aa59d-108">Note that it assumes you have initialized the symbol handler using the code in [Initializing the Symbol Handler](initializing-the-symbol-handler.md).</span></span>


```C++
TCHAR  szImageName[MAX_PATH] = TEXT("foo.dll");
DWORD64 dwBaseAddr = 0;

if (SymLoadModuleEx(hProcess,    // target process 
                    NULL,        // handle to image - not used
                    szImageName, // name of image file
                    NULL,        // name of module - not required
                    dwBaseAddr,  // base address - not required
                    0,           // size of image - not required
                    NULL,        // MODLOAD_DATA used for special cases 
                    0))          // flags - not required
{
    // SymLoadModuleEx returned success
}
else
{
    // SymLoadModuleEx failed
    DWORD error = GetLastError();
    printf("SymLoadModuleEx returned error : %d\n", error);
}
```



<span data-ttu-id="aa59d-109">請注意， *szImageName* 可以是任何 ( .exe、.dll、. winspool.drv、sys、.scr、cpl、.com) 的可執行模組的路徑。</span><span class="sxs-lookup"><span data-stu-id="aa59d-109">Note that *szImageName* can be a path to any executable module that has debugging information (.exe, .dll, .drv, .sys, .scr, .cpl, .com).</span></span> <span data-ttu-id="aa59d-110">此外， *dwBaseAddr* 是要載入之符號模組的基底位址。</span><span class="sxs-lookup"><span data-stu-id="aa59d-110">Also, *dwBaseAddr* is the base address of the symbol module to be loaded.</span></span> <span data-ttu-id="aa59d-111">如果這個值為0，符號處理常式將會從指定的符號模組取得基底位址。</span><span class="sxs-lookup"><span data-stu-id="aa59d-111">If this value is 0, the symbol handler will obtain the base address from the specified symbol module.</span></span>

## <a name="related-topics"></a><span data-ttu-id="aa59d-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="aa59d-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aa59d-113">卸載符號模組</span><span class="sxs-lookup"><span data-stu-id="aa59d-113">Unloading a Symbol Module</span></span>](unloading-a-symbol-module.md)
</dt> </dl>

 

 



