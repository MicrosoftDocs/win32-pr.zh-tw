---
title: Single-Threaded 和多執行緒通訊
description: Single-Threaded 和多執行緒通訊
ms.assetid: 8d3a855c-b52d-48bb-9fdf-efbf8005c374
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6470ac398e6ae1c8a645fb076fbbf509d58b579
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300531"
---
# <a name="single-threaded-and-multithreaded-communication"></a><span data-ttu-id="b05ae-103">Single-Threaded 和多執行緒通訊</span><span class="sxs-lookup"><span data-stu-id="b05ae-103">Single-Threaded and Multithreaded Communication</span></span>

<span data-ttu-id="b05ae-104">支援單一執行緒和多執行緒單元的用戶端或伺服器會有一個多執行緒單元，其中包含所有初始化為自由執行緒的執行緒，以及一或多個單一執行緒單元。</span><span class="sxs-lookup"><span data-stu-id="b05ae-104">A client or server that supports both single-threaded and multithreaded apartments will have one multithreaded apartment, containing all threads initialized as free-threaded, and one or more single-threaded apartments.</span></span> <span data-ttu-id="b05ae-105">介面指標必須在單元之間進行封送處理，但可以在不需要封送處理的情況下使用。</span><span class="sxs-lookup"><span data-stu-id="b05ae-105">Interface pointers must be marshaled between apartments but can be used without marshaling within an apartment.</span></span> <span data-ttu-id="b05ae-106">對單一執行緒單元中的物件呼叫會由 COM 進行同步處理。</span><span class="sxs-lookup"><span data-stu-id="b05ae-106">Calls to objects in a single-threaded apartment will be synchronized by COM.</span></span> <span data-ttu-id="b05ae-107">COM 將不會同步處理多執行緒單元中的物件呼叫。</span><span class="sxs-lookup"><span data-stu-id="b05ae-107">Calls to objects in the multithreaded apartment will not be synchronized by COM.</span></span>

<span data-ttu-id="b05ae-108">單一執行緒單元上的所有資訊都會套用至標示為「單元模型」的執行緒，而多執行緒單元上的所有資訊則適用于所有標記為自由執行緒的執行緒。</span><span class="sxs-lookup"><span data-stu-id="b05ae-108">All of the information on single-threaded apartments applies to the threads marked as apartment model, and all of the information on multithreaded apartments applies to all of the threads marked as free-threaded.</span></span> <span data-ttu-id="b05ae-109">單元執行緒規則適用于進行內部通訊，需要在具有 [**CoMarshalInterThreadInterfaceInStream**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterthreadinterfaceinstream) 和 [**CoGetInterfaceAndReleaseStream**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetinterfaceandreleasestream)呼叫的單元之間封送處理介面指標，如 [單一執行緒單元](single-threaded-apartments.md)中所述。</span><span class="sxs-lookup"><span data-stu-id="b05ae-109">Apartment threading rules apply to inter-apartment communication, requiring that interface pointers be marshaled between apartments with calls to [**CoMarshalInterThreadInterfaceInStream**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterthreadinterfaceinstream) and [**CoGetInterfaceAndReleaseStream**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetinterfaceandreleasestream), as described in [Single-Threaded Apartments](single-threaded-apartments.md).</span></span>

> [!Note]  
> <span data-ttu-id="b05ae-110">處理同進程伺服器時，有一些特殊考慮。</span><span class="sxs-lookup"><span data-stu-id="b05ae-110">Some special considerations apply when dealing with in-process servers.</span></span> <span data-ttu-id="b05ae-111">如需詳細資訊，請參閱同 [進程伺服器執行緒問題](in-process-server-threading-issues.md)。</span><span class="sxs-lookup"><span data-stu-id="b05ae-111">For more information, see [In-Process Server Threading Issues](in-process-server-threading-issues.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="b05ae-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="b05ae-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b05ae-113">跨單元存取介面</span><span class="sxs-lookup"><span data-stu-id="b05ae-113">Accessing Interfaces Across Apartments</span></span>](accessing-interfaces-across-apartments.md)
</dt> <dt>

[<span data-ttu-id="b05ae-114">選擇執行緒模型</span><span class="sxs-lookup"><span data-stu-id="b05ae-114">Choosing the Threading Model</span></span>](choosing-the-threading-model.md)
</dt> <dt>

[<span data-ttu-id="b05ae-115">多執行緒單元</span><span class="sxs-lookup"><span data-stu-id="b05ae-115">Multithreaded Apartments</span></span>](multithreaded-apartments.md)
</dt> <dt>

[<span data-ttu-id="b05ae-116">同進程伺服器執行緒問題</span><span class="sxs-lookup"><span data-stu-id="b05ae-116">In-Process Server Threading Issues</span></span>](in-process-server-threading-issues.md)
</dt> <dt>

[<span data-ttu-id="b05ae-117">進程、執行緒和單元</span><span class="sxs-lookup"><span data-stu-id="b05ae-117">Processes, Threads, and Apartments</span></span>](processes--threads--and-apartments.md)
</dt> <dt>

[<span data-ttu-id="b05ae-118">單一執行緒單元</span><span class="sxs-lookup"><span data-stu-id="b05ae-118">Single-Threaded Apartments</span></span>](single-threaded-apartments.md)
</dt> </dl>

 

 




