---
Description: 以下是各種記憶體配置方法的簡短比較。
ms.assetid: b6101014-02d2-4b19-aec6-8772a2793d38
title: 比較記憶體配置方法
ms.topic: reference
ms.custom: snippet-project
ms.date: 05/31/2018
ms.openlocfilehash: 541b314c4ff0553ff8812e591c47c87962866bbe
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/10/2021
ms.locfileid: "103946031"
---
# <a name="comparing-memory-allocation-methods"></a><span data-ttu-id="69b21-103">比較記憶體配置方法</span><span class="sxs-lookup"><span data-stu-id="69b21-103">Comparing Memory Allocation Methods</span></span>

<span data-ttu-id="69b21-104">以下是各種記憶體配置方法的簡短比較：</span><span class="sxs-lookup"><span data-stu-id="69b21-104">The following is a brief comparison of the various memory allocation methods:</span></span>

-   [<span data-ttu-id="69b21-105">**CoTaskMemAlloc**</span><span class="sxs-lookup"><span data-stu-id="69b21-105">**CoTaskMemAlloc**</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemalloc)
-   [<span data-ttu-id="69b21-106">**GlobalAlloc**</span><span class="sxs-lookup"><span data-stu-id="69b21-106">**GlobalAlloc**</span></span>](/windows/desktop/api/WinBase/nf-winbase-globalalloc)
-   [<span data-ttu-id="69b21-107">**HeapAlloc**</span><span class="sxs-lookup"><span data-stu-id="69b21-107">**HeapAlloc**</span></span>](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc)
-   [<span data-ttu-id="69b21-108">**LocalAlloc**</span><span class="sxs-lookup"><span data-stu-id="69b21-108">**LocalAlloc**</span></span>](/windows/desktop/api/WinBase/nf-winbase-localalloc)
-   <span data-ttu-id="69b21-109">**malloc**</span><span class="sxs-lookup"><span data-stu-id="69b21-109">**malloc**</span></span>
-   <span data-ttu-id="69b21-110">**新增功能**</span><span class="sxs-lookup"><span data-stu-id="69b21-110">**new**</span></span>
-   [<span data-ttu-id="69b21-111">**VirtualAlloc**</span><span class="sxs-lookup"><span data-stu-id="69b21-111">**VirtualAlloc**</span></span>](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc)

<span data-ttu-id="69b21-112">雖然 [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc)、 [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc)和 [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) 函式最終會配置相同堆積的記憶體，但每個函數都提供稍微不同的功能集。</span><span class="sxs-lookup"><span data-stu-id="69b21-112">Although the [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc), [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc), and [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) functions ultimately allocate memory from the same heap, each provides a slightly different set of functionality.</span></span> <span data-ttu-id="69b21-113">例如，如果無法配置記憶體，則可指示 **HeapAlloc** 引發例外狀況，這是 **LocalAlloc** 無法使用的功能。</span><span class="sxs-lookup"><span data-stu-id="69b21-113">For example, **HeapAlloc** can be instructed to raise an exception if memory could not be allocated, a capability not available with **LocalAlloc**.</span></span> <span data-ttu-id="69b21-114">**LocalAlloc** 支援配置控制碼，以允許重新配置來移動基礎記憶體，而不變更控制碼值，也就是 **HeapAlloc** 無法使用的功能。</span><span class="sxs-lookup"><span data-stu-id="69b21-114">**LocalAlloc** supports allocation of handles which permit the underlying memory to be moved by a reallocation without changing the handle value, a capability not available with **HeapAlloc**.</span></span>

<span data-ttu-id="69b21-115">從32位 Windows 開始， [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc) 和 [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc) 會實作為包裝函式，以使用處理程式預設堆積的控制碼來呼叫 [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) 。</span><span class="sxs-lookup"><span data-stu-id="69b21-115">Starting with 32-bit Windows, [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc) and [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc) are implemented as wrapper functions that call [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) using a handle to the process's default heap.</span></span> <span data-ttu-id="69b21-116">因此， **GlobalAlloc** 和 **LocalAlloc** 的額外負荷高於 **HeapAlloc**。</span><span class="sxs-lookup"><span data-stu-id="69b21-116">Therefore, **GlobalAlloc** and **LocalAlloc** have greater overhead than **HeapAlloc**.</span></span>

<span data-ttu-id="69b21-117">因為不同的堆積配置器會使用不同的機制來提供獨特的功能，所以您必須使用正確的函式來釋放記憶體。</span><span class="sxs-lookup"><span data-stu-id="69b21-117">Because the different heap allocators provide distinctive functionality by using different mechanisms, you must free memory with the correct function.</span></span> <span data-ttu-id="69b21-118">例如，使用 [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) 配置的記憶體必須使用 [**HeapFree**](/windows/desktop/api/HeapApi/nf-heapapi-heapfree) 來釋放，而不是 [**>localfree**](/windows/desktop/api/WinBase/nf-winbase-localfree) 或 [**GlobalFree**](/windows/desktop/api/WinBase/nf-winbase-globalfree)。</span><span class="sxs-lookup"><span data-stu-id="69b21-118">For example, memory allocated with [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) must be freed with [**HeapFree**](/windows/desktop/api/HeapApi/nf-heapapi-heapfree) and not [**LocalFree**](/windows/desktop/api/WinBase/nf-winbase-localfree) or [**GlobalFree**](/windows/desktop/api/WinBase/nf-winbase-globalfree).</span></span> <span data-ttu-id="69b21-119">使用 [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc) 或 [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc) 所配置的記憶體必須使用對應的全域或區域函數進行查詢、驗證和發行。</span><span class="sxs-lookup"><span data-stu-id="69b21-119">Memory allocated with [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc) or [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc) must be queried, validated, and released with the corresponding global or local function.</span></span>

<span data-ttu-id="69b21-120">[**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc)函式可讓您指定額外的記憶體配置選項。</span><span class="sxs-lookup"><span data-stu-id="69b21-120">The [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) function allows you to specify additional options for memory allocation.</span></span> <span data-ttu-id="69b21-121">不過，其配置會使用頁面細微性，因此使用 **VirtualAlloc** 可能會導致更高的記憶體使用量。</span><span class="sxs-lookup"><span data-stu-id="69b21-121">However, its allocations use a page granularity, so using **VirtualAlloc** can result in higher memory usage.</span></span>

<span data-ttu-id="69b21-122">**Malloc** 函數具有與執行時間相依的缺點。</span><span class="sxs-lookup"><span data-stu-id="69b21-122">The **malloc** function has the disadvantage of being run-time dependent.</span></span> <span data-ttu-id="69b21-123">**New** 運算子的缺點是編譯器相依和語言相依。</span><span class="sxs-lookup"><span data-stu-id="69b21-123">The **new** operator has the disadvantage of being compiler dependent and language dependent.</span></span>

<span data-ttu-id="69b21-124">[**CoTaskMemAlloc**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemalloc)函式的優點是在 c、c + + 或 Visual Basic 中都能正常運作。</span><span class="sxs-lookup"><span data-stu-id="69b21-124">The [**CoTaskMemAlloc**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemalloc) function has the advantage of working well in either C, C++, or Visual Basic.</span></span> <span data-ttu-id="69b21-125">它也是在以 COM 為基礎的應用程式中共用記憶體的唯一方式，因為 MIDL 會使用 **CoTaskMemAlloc** 和 [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) 來封送處理記憶體。</span><span class="sxs-lookup"><span data-stu-id="69b21-125">It is also the only way to share memory in a COM-based application, since MIDL uses **CoTaskMemAlloc** and [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) to marshal memory.</span></span>


## <a name="examples"></a><span data-ttu-id="69b21-126">範例</span><span class="sxs-lookup"><span data-stu-id="69b21-126">Examples</span></span>

* [<span data-ttu-id="69b21-127">保留和認可記憶體</span><span class="sxs-lookup"><span data-stu-id="69b21-127">Reserving and Committing Memory</span></span>](./reserving-and-committing-memory.md)

* [<span data-ttu-id="69b21-128">AWE 範例</span><span class="sxs-lookup"><span data-stu-id="69b21-128">AWE Example</span></span>](./awe-example.md)

## <a name="related-topics"></a><span data-ttu-id="69b21-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="69b21-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="69b21-130">全域和區域函數</span><span class="sxs-lookup"><span data-stu-id="69b21-130">Global and Local Functions</span></span>](global-and-local-functions.md)
</dt> <dt>

[<span data-ttu-id="69b21-131">堆積函數</span><span class="sxs-lookup"><span data-stu-id="69b21-131">Heap Functions</span></span>](heap-functions.md)
</dt> <dt>

[<span data-ttu-id="69b21-132">虛擬記憶體函數</span><span class="sxs-lookup"><span data-stu-id="69b21-132">Virtual Memory Functions</span></span>](virtual-memory-functions.md)
</dt> </dl>

 

 