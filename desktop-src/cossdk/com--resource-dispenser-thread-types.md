---
description: COM + 資源配置器執行緒類型
ms.assetid: 3ab67adb-311f-404c-a3ca-d274af53f91c
title: COM + 資源配置器執行緒類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 761d85edc3105785ded904fd2dc6083a9aea30cd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104385899"
---
# <a name="com-resource-dispenser-thread-types"></a><span data-ttu-id="6baa1-103">COM + 資源配置器執行緒類型</span><span class="sxs-lookup"><span data-stu-id="6baa1-103">COM+ Resource Dispenser Thread Types</span></span>

<span data-ttu-id="6baa1-104">COM + 資源配置器的呼叫可能源自下列其中一種執行緒類型：</span><span class="sxs-lookup"><span data-stu-id="6baa1-104">Calls into a COM+ resource dispenser may originate in one of the following thread types:</span></span>

-   <span data-ttu-id="6baa1-105"> (STA) 的單元執行緒</span><span class="sxs-lookup"><span data-stu-id="6baa1-105">Apartment thread (STA)</span></span>
-   <span data-ttu-id="6baa1-106"> (MTA) 的自由執行緒</span><span class="sxs-lookup"><span data-stu-id="6baa1-106">Free thread (MTA)</span></span>
-   <span data-ttu-id="6baa1-107">非 COM 執行緒 (應用程式或分配 [器管理員](com--dispenser-manager.md) 垃圾收集器執行緒) </span><span class="sxs-lookup"><span data-stu-id="6baa1-107">Non-COM thread (application or the [dispenser manager](com--dispenser-manager.md) garbage-collector thread)</span></span>

<span data-ttu-id="6baa1-108">如果資源配置器不是 COM 物件，它就必須能夠隨時處理來自任何執行緒的呼叫。</span><span class="sxs-lookup"><span data-stu-id="6baa1-108">If a resource dispenser is not a COM object, it must be able to handle calls arriving from any thread at any time.</span></span> <span data-ttu-id="6baa1-109">如果資源配置器是 COM 物件，則應該使用 **兩者** 的執行緒模型來註冊 com 物件。</span><span class="sxs-lookup"><span data-stu-id="6baa1-109">If a resource dispenser is a COM object, the COM object should be registered with a threading model of **Both**.</span></span> <span data-ttu-id="6baa1-110">這可讓 STA 或 MTA 執行緒在沒有線程切換的情況下，建立及使用資源配置器。</span><span class="sxs-lookup"><span data-stu-id="6baa1-110">This allows STA or MTA threads to create and use the resource dispenser without a thread switch.</span></span>

<span data-ttu-id="6baa1-111">如果資源配置器建立並使用另一個 COM 物件 (例如，跨進程的 resource manager) ，資源配置器可能需要維護此其他 COM 物件的多個 proxy，並確保對呼叫執行緒使用適當的 proxy 來呼叫物件。</span><span class="sxs-lookup"><span data-stu-id="6baa1-111">If a resource dispenser creates and uses another COM object (for example, an out-of-process resource manager), the resource dispenser might need to maintain multiple proxies to this other COM object and ensure that calls to the object are made using the appropriate proxy for the calling thread.</span></span> <span data-ttu-id="6baa1-112">當資源配置器建立這個物件時，它會封送處理並儲存參考。</span><span class="sxs-lookup"><span data-stu-id="6baa1-112">When the resource dispenser creates this object, it marshals and saves the reference.</span></span> <span data-ttu-id="6baa1-113">再次呼叫物件之前，必須先 unmarshal 來建立呼叫執行緒的 proxy。</span><span class="sxs-lookup"><span data-stu-id="6baa1-113">Before calling the object again, it must unmarshal to create a proxy for the calling thread.</span></span>

<span data-ttu-id="6baa1-114">快取這些每個執行緒的 proxy 可能更有效率，方法是將對應從執行緒識別碼保留至 proxy 指標。</span><span class="sxs-lookup"><span data-stu-id="6baa1-114">It might be more efficient to cache these per-thread proxies by keeping a map from the thread ID to a proxy pointer.</span></span> <span data-ttu-id="6baa1-115">此對應會在進程中使用新的執行緒時展開。</span><span class="sxs-lookup"><span data-stu-id="6baa1-115">This map expands as new threads are used in the process.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6baa1-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="6baa1-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6baa1-117">COM + 資源配置器概念</span><span class="sxs-lookup"><span data-stu-id="6baa1-117">COM+ Resource Dispenser Concepts</span></span>](com--resource-dispenser-concepts.md)
</dt> </dl>

 

 



