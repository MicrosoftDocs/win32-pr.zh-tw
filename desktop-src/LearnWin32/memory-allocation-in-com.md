---
title: COM 中的記憶體配置
description: COM 中的記憶體配置
ms.assetid: b3c318d2-1273-430e-8aca-5bd5c95c138e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82cb9913da55fab82f699ac05dae3998f7582224
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103886"
---
# <a name="memory-allocation-in-com"></a><span data-ttu-id="3ea75-103">COM 中的記憶體配置</span><span class="sxs-lookup"><span data-stu-id="3ea75-103">Memory Allocation in COM</span></span>

<span data-ttu-id="3ea75-104">有時候，方法會在堆積上配置記憶體緩衝區，並將緩衝區的位址傳回給呼叫端。</span><span class="sxs-lookup"><span data-stu-id="3ea75-104">Sometimes a method allocates a memory buffer on the heap and returns the address of the buffer to the caller.</span></span> <span data-ttu-id="3ea75-105">COM 會定義一組函數來配置和釋放堆積上的記憶體。</span><span class="sxs-lookup"><span data-stu-id="3ea75-105">COM defines a pair of functions for allocating and freeing memory on the heap.</span></span>

-   <span data-ttu-id="3ea75-106">[**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc)函數會配置記憶體區塊。</span><span class="sxs-lookup"><span data-stu-id="3ea75-106">The [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) function allocates a block of memory.</span></span>
-   <span data-ttu-id="3ea75-107">[**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)函式會釋放以 [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc)配置的記憶體區塊。</span><span class="sxs-lookup"><span data-stu-id="3ea75-107">The [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) function frees a block of memory that was allocated with [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc).</span></span>

<span data-ttu-id="3ea75-108">在 [ [開啟] 對話方塊範例](example--the-open-dialog-box.md)中，我們看到這個模式的範例：</span><span class="sxs-lookup"><span data-stu-id="3ea75-108">We saw an example of this pattern in the [Open dialog box example](example--the-open-dialog-box.md):</span></span>


```C++
PWSTR pszFilePath;
hr = pItem->GetDisplayName(SIGDN_FILESYSPATH, &pszFilePath);
if (SUCCEEDED(hr))
{
    // ...
    CoTaskMemFree(pszFilePath);
}
```



<span data-ttu-id="3ea75-109">[**GetDisplayName**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-getdisplayname)方法會配置字串的記憶體。</span><span class="sxs-lookup"><span data-stu-id="3ea75-109">The [**GetDisplayName**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-getdisplayname) method allocates memory for a string.</span></span> <span data-ttu-id="3ea75-110">方法會在內部呼叫 [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) 來配置字串。</span><span class="sxs-lookup"><span data-stu-id="3ea75-110">Internally, the method calls [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) to allocate the string.</span></span> <span data-ttu-id="3ea75-111">當方法傳回時， *pszFilePath* 會指向新緩衝區的記憶體位置。</span><span class="sxs-lookup"><span data-stu-id="3ea75-111">When the method returns, *pszFilePath* points to the memory location of the new buffer.</span></span> <span data-ttu-id="3ea75-112">呼叫端會負責呼叫 [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) 來釋放記憶體。</span><span class="sxs-lookup"><span data-stu-id="3ea75-112">The caller is responsible for calling [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to free the memory.</span></span>

<span data-ttu-id="3ea75-113">為什麼 COM 會定義自己的記憶體配置函數？</span><span class="sxs-lookup"><span data-stu-id="3ea75-113">Why does COM define its own memory allocation functions?</span></span> <span data-ttu-id="3ea75-114">其中一個原因是要在堆積配置器上提供抽象層。</span><span class="sxs-lookup"><span data-stu-id="3ea75-114">One reason is to provide an abstraction layer over the heap allocator.</span></span> <span data-ttu-id="3ea75-115">否則，某些方法可能會呼叫 **malloc** ，而其他方法則稱為 **new**。</span><span class="sxs-lookup"><span data-stu-id="3ea75-115">Otherwise, some methods might call **malloc** while others called **new**.</span></span> <span data-ttu-id="3ea75-116">然後，在某些情況下，您的程式需要 **免費** 通話，並在其他情況下 **刪除** ，並持續追蹤所有的情況。</span><span class="sxs-lookup"><span data-stu-id="3ea75-116">Then your program would need to call **free** in some cases and **delete** in others, and keeping track of it all would quickly become impossible.</span></span> <span data-ttu-id="3ea75-117">COM 配置函數會建立一致的方法。</span><span class="sxs-lookup"><span data-stu-id="3ea75-117">The COM allocation functions create a uniform approach.</span></span>

<span data-ttu-id="3ea75-118">另一個考慮是 COM 是 *二進位* 標準，因此不會系結至特定的程式設計語言。</span><span class="sxs-lookup"><span data-stu-id="3ea75-118">Another consideration is the fact that COM is a *binary* standard, so it is not tied to a particular programming language.</span></span> <span data-ttu-id="3ea75-119">因此，COM 無法依賴任何特定語言的記憶體配置形式。</span><span class="sxs-lookup"><span data-stu-id="3ea75-119">Therefore, COM cannot rely on any language-specific form of memory allocation.</span></span>

## <a name="next"></a><span data-ttu-id="3ea75-120">下一個</span><span class="sxs-lookup"><span data-stu-id="3ea75-120">Next</span></span>

[<span data-ttu-id="3ea75-121">COM 編碼作法</span><span class="sxs-lookup"><span data-stu-id="3ea75-121">COM Coding Practices</span></span>](com-coding-practices.md)

 

 
