---
description: 下列程式碼示範如何呼叫 SymFromAddr 函數。
ms.assetid: 63dfadea-b0c4-4050-add8-d1f3aef7a495
title: 依位址抓取符號資訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29ad9d2879dbfd5820c4aa6c2e7563a1575ebe1c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110456"
---
# <a name="retrieving-symbol-information-by-address"></a><span data-ttu-id="9f7d0-103">依位址抓取符號資訊</span><span class="sxs-lookup"><span data-stu-id="9f7d0-103">Retrieving Symbol Information by Address</span></span>

<span data-ttu-id="9f7d0-104">下列程式碼示範如何呼叫 [**SymFromAddr**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromaddr) 函數。</span><span class="sxs-lookup"><span data-stu-id="9f7d0-104">The following code demonstrates how to call the [**SymFromAddr**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromaddr) function.</span></span> <span data-ttu-id="9f7d0-105">此函數會填入 [**符號 \_ 資訊**](/windows/desktop/api/DbgHelp/ns-dbghelp-symbol_info) 結構。</span><span class="sxs-lookup"><span data-stu-id="9f7d0-105">This function fills in a [**SYMBOL\_INFO**](/windows/desktop/api/DbgHelp/ns-dbghelp-symbol_info) structure.</span></span> <span data-ttu-id="9f7d0-106">因為名稱是變數的長度，所以您必須提供夠大的緩衝區，以容納儲存在 **符號 \_ 資訊** 結構結尾的名稱。</span><span class="sxs-lookup"><span data-stu-id="9f7d0-106">Because the name is variable in length, you must supply a buffer that is large enough to hold the name stored at the end of the **SYMBOL\_INFO** structure.</span></span> <span data-ttu-id="9f7d0-107">此外， **MaxNameLen** 成員必須設定為名稱所保留的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="9f7d0-107">Also, the **MaxNameLen** member must be set to the number of bytes reserved for the name.</span></span> <span data-ttu-id="9f7d0-108">在此範例中， *dwAddress* 是要對應至符號的位址。</span><span class="sxs-lookup"><span data-stu-id="9f7d0-108">In this example, *dwAddress* is the address to be mapped to a symbol.</span></span> <span data-ttu-id="9f7d0-109">**SymFromAddr** 函數會將符號開頭的位移儲存至 *dwDisplacement* 中的位址。</span><span class="sxs-lookup"><span data-stu-id="9f7d0-109">The **SymFromAddr** function will store an offset to the beginning of the symbol to the address in *dwDisplacement*.</span></span> <span data-ttu-id="9f7d0-110">此範例假設您已使用 [初始化符號處理常式](initializing-the-symbol-handler.md)中的程式碼，初始化符號處理常式。</span><span class="sxs-lookup"><span data-stu-id="9f7d0-110">The example assumes you have initialized the symbol handler using the code in [Initializing the Symbol Handler](initializing-the-symbol-handler.md).</span></span>


```C++
DWORD64  dwDisplacement = 0;
DWORD64  dwAddress = SOME_ADDRESS;

char buffer[sizeof(SYMBOL_INFO) + MAX_SYM_NAME * sizeof(TCHAR)];
PSYMBOL_INFO pSymbol = (PSYMBOL_INFO)buffer;

pSymbol->SizeOfStruct = sizeof(SYMBOL_INFO);
pSymbol->MaxNameLen = MAX_SYM_NAME;

if (SymFromAddr(hProcess, dwAddress, &dwDisplacement, pSymbol))
{
    // SymFromAddr returned success
}
else
{
    // SymFromAddr failed
    DWORD error = GetLastError();
    printf("SymFromAddr returned error : %d\n", error);
}
```



<span data-ttu-id="9f7d0-111">若要取得指定位址的源程式碼號，應用程式可以使用 [**SymGetLineFromAddr64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromaddr)。</span><span class="sxs-lookup"><span data-stu-id="9f7d0-111">To retrieve the source code line number for a specified address, an application can use [**SymGetLineFromAddr64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromaddr).</span></span> <span data-ttu-id="9f7d0-112">此函式需要 [**Imagehlp.dll \_ LINE64**](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_line) 結構的指標，才能接收對應至指定之程式碼位址的原始程式檔名稱和行號。</span><span class="sxs-lookup"><span data-stu-id="9f7d0-112">This function requires a pointer to an [**IMAGEHLP\_LINE64**](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_line) structure to receive the source file name and line number corresponding to a specified code address.</span></span> <span data-ttu-id="9f7d0-113">請注意，只有在使用 [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions)函數設定 **SYMOPT \_ 載入 \_ 行** 時，符號處理常式才能取出行號資訊。</span><span class="sxs-lookup"><span data-stu-id="9f7d0-113">Note that the symbol handler can retrieve line number information only when **SYMOPT\_LOAD\_LINES** is set using the [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) function.</span></span> <span data-ttu-id="9f7d0-114">載入模組之前，必須先設定這個選項。</span><span class="sxs-lookup"><span data-stu-id="9f7d0-114">This option must be set before loading the module.</span></span> <span data-ttu-id="9f7d0-115">DwAddress 參數包含原始程式檔名稱和行號所在的程式碼位址。</span><span class="sxs-lookup"><span data-stu-id="9f7d0-115">The dwAddress parameter contains the code address for which the source file name and line number will be located.</span></span>


```C++
DWORD64  dwAddress;
DWORD  dwDisplacement;
IMAGEHLP_LINE64 line;

SymSetOptions(SYMOPT_LOAD_LINES);

line.SizeOfStruct = sizeof(IMAGEHLP_LINE64);
dwAddress = 0x1000000; // Address you want to check on.

if (SymGetLineFromAddr64(hProcess, dwAddress, &dwDisplacement, &line))
{
    // SymGetLineFromAddr64 returned success
}
else
{
    // SymGetLineFromAddr64 failed
    DWORD error = GetLastError();
    _tprintf(TEXT("SymGetLineFromAddr64 returned error : %d\n"), error);
}
```



 

 



