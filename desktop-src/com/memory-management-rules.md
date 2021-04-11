---
title: 記憶體管理規則
description: 記憶體管理規則
ms.assetid: 769127a1-1a14-4ed4-9d38-7cf3e571b661
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56e7ad2483b794ec5c2e9c325bca8e469ff4ae0b
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104093399"
---
# <a name="memory-management-rules"></a><span data-ttu-id="2a3da-103">記憶體管理規則</span><span class="sxs-lookup"><span data-stu-id="2a3da-103">Memory Management Rules</span></span>

<span data-ttu-id="2a3da-104">介面指標的存留期一律是透過每個 COM 介面上的 [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) 和 [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) 方法來管理。</span><span class="sxs-lookup"><span data-stu-id="2a3da-104">The lifetime of pointers to interfaces is always managed through the [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) and [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) methods on every COM interface.</span></span> <span data-ttu-id="2a3da-105">如需詳細資訊，請參閱 [管理參考計數的規則](rules-for-managing-reference-counts.md)。</span><span class="sxs-lookup"><span data-stu-id="2a3da-105">For more information, see [Rules for Managing Reference Counts](rules-for-managing-reference-counts.md).</span></span>

<span data-ttu-id="2a3da-106">針對所有其他參數，請務必遵守管理記憶體的特定規則。</span><span class="sxs-lookup"><span data-stu-id="2a3da-106">For all other parameters, it is important to adhere to certain rules for managing memory.</span></span> <span data-ttu-id="2a3da-107">下列規則適用于介面 methodsâ中的所有參數（包括不以傳值方式傳遞的 return valueâ€）：</span><span class="sxs-lookup"><span data-stu-id="2a3da-107">The following rules apply to all parameters of interface methodsâ€”including the return valueâ€”that are not passed by value:</span></span>

-   <span data-ttu-id="2a3da-108">參數必須由呼叫端配置及釋放。</span><span class="sxs-lookup"><span data-stu-id="2a3da-108">In-parameters must be allocated and freed by the caller.</span></span>
-   <span data-ttu-id="2a3da-109">Out 參數必須由被呼叫的參數進行配置;呼叫端會使用標準 COM 工作記憶體配置器來釋放它們。</span><span class="sxs-lookup"><span data-stu-id="2a3da-109">Out-parameters must be allocated by the one called; they are freed by the caller using the standard COM task memory allocator.</span></span> <span data-ttu-id="2a3da-110">如需詳細資訊，請參閱 [OLE 記憶體](the-ole-memory-allocator.md) 配置器。</span><span class="sxs-lookup"><span data-stu-id="2a3da-110">See [The OLE Memory Allocator](the-ole-memory-allocator.md) for more information.</span></span>
-   <span data-ttu-id="2a3da-111">In/out-參數一開始是由呼叫端配置，然後在必要時由呼叫的參數釋放和重新配置。</span><span class="sxs-lookup"><span data-stu-id="2a3da-111">In/out-parameters are initially allocated by the caller, and then freed and reallocated by the one called, if necessary.</span></span> <span data-ttu-id="2a3da-112">如果是 out 參數，呼叫端會負責釋出最後傳回的值。</span><span class="sxs-lookup"><span data-stu-id="2a3da-112">As is true for out parameters, the caller is responsible for freeing the final returned value.</span></span> <span data-ttu-id="2a3da-113">必須使用標準 COM 記憶體配置器。</span><span class="sxs-lookup"><span data-stu-id="2a3da-113">The standard COM memory allocator must be used.</span></span>

<span data-ttu-id="2a3da-114">在後兩個案例中，其中一段程式碼會配置記憶體，而另一段程式碼會釋出記憶體，使用 COM 配置器可確保兩段程式碼使用相同的配置方法。</span><span class="sxs-lookup"><span data-stu-id="2a3da-114">In the latter two cases, where one piece of code allocates the memory and a different piece of code frees it, using the COM allocator ensures that the two pieces of code are using the same allocation methods.</span></span>

<span data-ttu-id="2a3da-115">另一個需要特別注意的地方，就是在失敗狀況中處理 out 和 out 參數。</span><span class="sxs-lookup"><span data-stu-id="2a3da-115">Another area that needs special attention is the treatment of out and in-out parameters in failure conditions.</span></span> <span data-ttu-id="2a3da-116">如果函式傳回失敗碼，呼叫端通常無法清除 out 或 out 參數。</span><span class="sxs-lookup"><span data-stu-id="2a3da-116">If a function returns a failure code, the caller typically has no way to clean up the out or in-out parameters.</span></span> <span data-ttu-id="2a3da-117">這會導致下列其他規則：</span><span class="sxs-lookup"><span data-stu-id="2a3da-117">This leads to the following additional rules:</span></span>

-   <span data-ttu-id="2a3da-118">如果發生錯誤情況，參數必須一律可靠地設定為將會清除的值，而不會由呼叫端執行任何動作。</span><span class="sxs-lookup"><span data-stu-id="2a3da-118">In case of an error condition, parameters must always be reliably set to a value that will be cleaned up without any action by the caller.</span></span>
-   <span data-ttu-id="2a3da-119">所有 out 指標參數都必須明確設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="2a3da-119">All out pointer parameters must explicitly be set to **NULL**.</span></span> <span data-ttu-id="2a3da-120">這些通常會以指標對指標參數的形式傳遞，但也可以做為呼叫端所配置之結構的成員，以及呼叫的程式碼填滿。</span><span class="sxs-lookup"><span data-stu-id="2a3da-120">These are usually passed in a pointer-to-pointer parameter but can also be passed as members of a structure that the caller allocates and the called code fills.</span></span> <span data-ttu-id="2a3da-121">確保這一點的最直接方式 (是在部分) 中，將這些值設定為函式專案的 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="2a3da-121">The most straightforward way to ensure this is (in part) to set these values to **NULL** on function entry.</span></span> <span data-ttu-id="2a3da-122">這項規則很重要，因為它可提升更健全的應用程式互通性。</span><span class="sxs-lookup"><span data-stu-id="2a3da-122">This rule is important because it promotes more robust application interoperability.</span></span>
-   <span data-ttu-id="2a3da-123">在錯誤情況下，所有的 out 參數都必須由稱為 (的程式碼保持不變，因此會在呼叫端初始化它們) 或明確設定的值（如同 out 參數錯誤傳回案例中）。</span><span class="sxs-lookup"><span data-stu-id="2a3da-123">Under error conditions, all in-out parameters must either be left alone by the code called (thus remaining at the value to which they were initialized by the caller) or be explicitly set, as in the out parameter error return case.</span></span>

<span data-ttu-id="2a3da-124">請記住，這些適用于 COM 應用程式的記憶體管理慣例只適用于公用介面，而 APIsâ則是「COM 應用程式必須嚴格地內部進行記憶體配置，因此必須使用這些機制來完成。</span><span class="sxs-lookup"><span data-stu-id="2a3da-124">Remember that these memory management conventions for COM applications apply only across public interfaces and APIsâ€”there is no requirement at all that memory allocation strictly internal to a COM application need be done using these mechanisms.</span></span>

<span data-ttu-id="2a3da-125">COM 會在內部使用遠端程序呼叫， (RPC) 在用戶端與伺服器之間進行通訊。</span><span class="sxs-lookup"><span data-stu-id="2a3da-125">COM internally uses Remote Procedure Calls (RPC) to communicate between clients and servers.</span></span> <span data-ttu-id="2a3da-126">如需在 RPC 伺服器 stub 中管理記憶體的詳細資訊，請參閱 [伺服器 Stub 記憶體管理](../rpc/server-stub-memory-management.md) 主題。</span><span class="sxs-lookup"><span data-stu-id="2a3da-126">For more information about managing memory in RPC server stubs, see the [Server-stub Memory Management](../rpc/server-stub-memory-management.md) topic.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2a3da-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="2a3da-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2a3da-128">管理記憶體配置</span><span class="sxs-lookup"><span data-stu-id="2a3da-128">Managing Memory Allocation</span></span>](managing-memory-allocation.md)
</dt> </dl>

 

 