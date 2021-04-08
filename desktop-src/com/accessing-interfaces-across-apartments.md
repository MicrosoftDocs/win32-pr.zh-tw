---
title: 跨單元存取介面
description: 跨單元存取介面
ms.assetid: 4e0467b9-bbf1-410c-8aab-40450a7f963a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 626707daf721aee3b440bb79ba2d1e084d154a98
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672372"
---
# <a name="accessing-interfaces-across-apartments"></a><span data-ttu-id="dc5c9-103">跨單元存取介面</span><span class="sxs-lookup"><span data-stu-id="dc5c9-103">Accessing Interfaces Across Apartments</span></span>

<span data-ttu-id="dc5c9-104">COM 提供一種方法，讓進程中的任何一個單元都能存取在進程中任何其他單元之物件上所執行的介面。</span><span class="sxs-lookup"><span data-stu-id="dc5c9-104">COM provides a way for any apartment in a process to get access to an interface implemented on an object in any other apartment in the process.</span></span> <span data-ttu-id="dc5c9-105">這是透過 [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) 介面完成的。</span><span class="sxs-lookup"><span data-stu-id="dc5c9-105">This is done through the [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) interface.</span></span> <span data-ttu-id="dc5c9-106">這個介面有三個方法，可讓您執行下列作業：</span><span class="sxs-lookup"><span data-stu-id="dc5c9-106">This interface has three methods, which allow you to do the following:</span></span>

-   <span data-ttu-id="dc5c9-107">將介面註冊為 *全域* (processwide) 介面。</span><span class="sxs-lookup"><span data-stu-id="dc5c9-107">Register an interface as a *global* (processwide) interface.</span></span>
-   <span data-ttu-id="dc5c9-108">透過 cookie 從任何其他的單元取得該介面的指標。</span><span class="sxs-lookup"><span data-stu-id="dc5c9-108">Get a pointer to that interface from any other apartment through a cookie.</span></span>
-   <span data-ttu-id="dc5c9-109">撤銷介面的全域註冊。</span><span class="sxs-lookup"><span data-stu-id="dc5c9-109">Revoke the global registration of an interface.</span></span>

<span data-ttu-id="dc5c9-110">[**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable)介面是一個有效率的方法，可讓您將介面指標儲存在記憶體位置，以便從進程內的多個單元存取，例如整個進程的變數和 *agile* 物件 (自由執行緒、封送處理的物件) 包含指向其他物件的介面指標。</span><span class="sxs-lookup"><span data-stu-id="dc5c9-110">The [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) interface is an efficient way for a process to store an interface pointer in a memory location that can be accessed from multiple apartments within the process, such as process-wide variables and *agile* objects (free-threaded, marshaled objects) containing interface pointers to other objects.</span></span>

<span data-ttu-id="dc5c9-111">Agile 物件不知道其執行所在的基礎 COM 基礎結構;換句話說，它正在執行的是哪一個單元、內容和執行緒。</span><span class="sxs-lookup"><span data-stu-id="dc5c9-111">An agile object is unaware of the underlying COM infrastructure in which it runs; in other words, what apartment, context, and thread it is executing on.</span></span> <span data-ttu-id="dc5c9-112">物件可能會保存在某個單元或內容特定的介面上。</span><span class="sxs-lookup"><span data-stu-id="dc5c9-112">The object may be holding on to interfaces that are specific to an apartment or context.</span></span> <span data-ttu-id="dc5c9-113">基於這個理由，從 agile 元件執行的任何位置呼叫這些介面，可能不一定會正常運作。</span><span class="sxs-lookup"><span data-stu-id="dc5c9-113">For this reason, calling these interfaces from wherever the agile component is executing might not always work properly.</span></span> <span data-ttu-id="dc5c9-114">全域介面表會根據 agile 物件執行所在的位置，確保使用有效的 proxy (或指向物件的直接指標) ，藉以避免這個問題。</span><span class="sxs-lookup"><span data-stu-id="dc5c9-114">The global interface table avoids this problem by guaranteeing that a valid proxy (or direct pointer) to the object is used, based on where the agile object is executing.</span></span>

> [!Note]  
> <span data-ttu-id="dc5c9-115">全域介面資料表無法跨進程或電腦界限進行移植，因此不能用來取代正常的參數傳遞機制。</span><span class="sxs-lookup"><span data-stu-id="dc5c9-115">The global interface table is not portable across process or machine boundaries, so it cannot be used in place of the normal parameter-passing mechanism.</span></span>

 

<span data-ttu-id="dc5c9-116">如需有關建立和使用全域介面表的詳細資訊，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="dc5c9-116">For information about creating and using a global interface table, see the following topics:</span></span>

-   [<span data-ttu-id="dc5c9-117">建立全域介面資料表</span><span class="sxs-lookup"><span data-stu-id="dc5c9-117">Creating the Global Interface Table</span></span>](creating-the-global-interface-table.md)
-   [<span data-ttu-id="dc5c9-118">使用全域介面資料表的時機</span><span class="sxs-lookup"><span data-stu-id="dc5c9-118">When to Use the Global Interface Table</span></span>](when-to-use-the-global-interface-table.md)

## <a name="related-topics"></a><span data-ttu-id="dc5c9-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="dc5c9-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dc5c9-120">選擇執行緒模型</span><span class="sxs-lookup"><span data-stu-id="dc5c9-120">Choosing the Threading Model</span></span>](choosing-the-threading-model.md)
</dt> <dt>

[<span data-ttu-id="dc5c9-121">多執行緒單元</span><span class="sxs-lookup"><span data-stu-id="dc5c9-121">Multithreaded Apartments</span></span>](multithreaded-apartments.md)
</dt> <dt>

[<span data-ttu-id="dc5c9-122">同進程伺服器執行緒問題</span><span class="sxs-lookup"><span data-stu-id="dc5c9-122">In-Process Server Threading Issues</span></span>](in-process-server-threading-issues.md)
</dt> <dt>

[<span data-ttu-id="dc5c9-123">進程、執行緒和單元</span><span class="sxs-lookup"><span data-stu-id="dc5c9-123">Processes, Threads, and Apartments</span></span>](processes--threads--and-apartments.md)
</dt> <dt>

[<span data-ttu-id="dc5c9-124">單一執行緒和多執行緒通訊</span><span class="sxs-lookup"><span data-stu-id="dc5c9-124">Single-Threaded and Multithreaded Communication</span></span>](single-threaded-and-multithreaded-communication.md)
</dt> <dt>

[<span data-ttu-id="dc5c9-125">單一執行緒單元</span><span class="sxs-lookup"><span data-stu-id="dc5c9-125">Single-Threaded Apartments</span></span>](single-threaded-apartments.md)
</dt> </dl>

 

 




