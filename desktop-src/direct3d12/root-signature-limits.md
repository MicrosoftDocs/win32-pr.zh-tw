---
title: 根簽章限制
description: 根簽章是主要房地產，而且需要考慮嚴格的限制和成本。
ms.assetid: 01121D3A-1926-4246-9C20-5E11F2E0B092
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25986da72cfcad7b714031e063341e1832d6ae68
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "74103695"
---
# <a name="root-signature-limits"></a><span data-ttu-id="d0252-103">根簽章限制</span><span class="sxs-lookup"><span data-stu-id="d0252-103">Root Signature Limits</span></span>

<span data-ttu-id="d0252-104">根簽章是主要房地產，而且需要考慮嚴格的限制和成本。</span><span class="sxs-lookup"><span data-stu-id="d0252-104">The root signature is prime real estate, and there are strict limits and costs to consider.</span></span>

-   [<span data-ttu-id="d0252-105">記憶體限制和成本</span><span class="sxs-lookup"><span data-stu-id="d0252-105">Memory limits and costs</span></span>](#memory-limits-and-costs)
-   [<span data-ttu-id="d0252-106">效能成本</span><span class="sxs-lookup"><span data-stu-id="d0252-106">Performance costs</span></span>](#performance-costs)
-   [<span data-ttu-id="d0252-107">靜態取樣器</span><span class="sxs-lookup"><span data-stu-id="d0252-107">Static samplers</span></span>](#static-samplers)
-   [<span data-ttu-id="d0252-108">相關主題</span><span class="sxs-lookup"><span data-stu-id="d0252-108">Related topics</span></span>](#related-topics)

## <a name="memory-limits-and-costs"></a><span data-ttu-id="d0252-109">記憶體限制和成本</span><span class="sxs-lookup"><span data-stu-id="d0252-109">Memory limits and costs</span></span>

<span data-ttu-id="d0252-110">根簽章的大小上限為64的 Dword。</span><span class="sxs-lookup"><span data-stu-id="d0252-110">The maximum size of a root signature is 64 DWORDs.</span></span>

<span data-ttu-id="d0252-111">選擇這個大小上限，以防止將根簽章視為儲存大量資料的方式。</span><span class="sxs-lookup"><span data-stu-id="d0252-111">This maximum size is chosen to prevent abuse of the root signature as a way of storing bulk data.</span></span> <span data-ttu-id="d0252-112">根簽章中的每個專案都有此 64 DWORD 限制的成本：</span><span class="sxs-lookup"><span data-stu-id="d0252-112">Each entry in the root signature has a cost towards this 64 DWORD limit:</span></span>

-   <span data-ttu-id="d0252-113">描述項資料表每個都有成本1的 DWORD。</span><span class="sxs-lookup"><span data-stu-id="d0252-113">Descriptor tables cost 1 DWORD each.</span></span>
-   <span data-ttu-id="d0252-114">根常數的成本為 1 DWORD，因為它們是32位的值。</span><span class="sxs-lookup"><span data-stu-id="d0252-114">Root constants cost 1 DWORD each, since they are 32-bit values.</span></span>
-   <span data-ttu-id="d0252-115">根描述項 (64 位 GPU 虛擬位址) 每個成本2的 Dword。</span><span class="sxs-lookup"><span data-stu-id="d0252-115">Root descriptors (64-bit GPU virtual addresses) cost 2 DWORDs each.</span></span>

<span data-ttu-id="d0252-116">靜態取樣器的根簽章大小沒有任何費用。</span><span class="sxs-lookup"><span data-stu-id="d0252-116">Static samplers do not have any cost in the size of the root signature.</span></span>

## <a name="performance-costs"></a><span data-ttu-id="d0252-117">效能成本</span><span class="sxs-lookup"><span data-stu-id="d0252-117">Performance costs</span></span>

<span data-ttu-id="d0252-118">以) 間接取值層級為零的效能成本 (為零，代表根常數，1代表根描述項，2表示描述中繼資料表。</span><span class="sxs-lookup"><span data-stu-id="d0252-118">The performance cost (in terms of levels of indirection) are zero for a root constant, 1 for a root descriptor, and 2 for a descriptor table.</span></span> <span data-ttu-id="d0252-119">如果根簽章很大，而從最快的記憶體中溢位為稍微緩慢的記憶體 (可能會發生在某些硬體) 上，則在根簽章結尾的溢位專案的效能成本加1。</span><span class="sxs-lookup"><span data-stu-id="d0252-119">If a root signature is large and overflows out of the fastest memory into slightly slower memory (which can happen on some hardware), then add 1 to the performance cost for the overflowing items at the end of the root signature.</span></span>

<span data-ttu-id="d0252-120">可能會發生溢位，例如，在根引數空間中有固定大小的16個 Dword。</span><span class="sxs-lookup"><span data-stu-id="d0252-120">An overflow can occur on hardware that might have, for example, a fixed size of 16 DWORDs for root argument space.</span></span> <span data-ttu-id="d0252-121">如果使用輸入組合語言，此限制可能會進一步減少一次。</span><span class="sxs-lookup"><span data-stu-id="d0252-121">This limit might be further reduced by one if the Input Assembler is used.</span></span> <span data-ttu-id="d0252-122">在此情況下，如果根簽章對15或16個 DWORD 原生記憶體而言太大，就會造成溢位的記憶體溢位。</span><span class="sxs-lookup"><span data-stu-id="d0252-122">In this case there is overflow into slightly slower memory if the root signature is too large for the 15 or 16 DWORD native memory.</span></span> <span data-ttu-id="d0252-123">在其他硬體中，沒有固定的原生根目錄引數記憶體 (因此) 不會發生溢位狀況。</span><span class="sxs-lookup"><span data-stu-id="d0252-123">In other hardware there is no fixed native root argument memory (so the overflow situation never occurs).</span></span>

<span data-ttu-id="d0252-124">針對所有的硬體，如果任何根引數變更，驅動程式必須維護所有根引數的版本 (與其他儲存體（例如描述元堆積和緩衝區資源）不同，但驅動程式) 不會建立版本。</span><span class="sxs-lookup"><span data-stu-id="d0252-124">For all hardware, if any root argument changes, the driver must maintain a version of all the root arguments (unlike other storage such as descriptor heaps and buffer resources, which are not versioned by the driver).</span></span> <span data-ttu-id="d0252-125">在發生溢位情況的硬體中，只有原生或溢位區域需要進行版本設定，視發生變更的位置而定。</span><span class="sxs-lookup"><span data-stu-id="d0252-125">In hardware that an overflow situation occurs, only the native or overflow area needs to be versioned, depending on where the change occurred.</span></span> <span data-ttu-id="d0252-126">您應該將版本設定的數量明顯保留在必要的最小值。</span><span class="sxs-lookup"><span data-stu-id="d0252-126">The amount of versioning should obviously be kept to the necessary minimum.</span></span>

<span data-ttu-id="d0252-127">一般來說，請考慮下列指導方針：</span><span class="sxs-lookup"><span data-stu-id="d0252-127">Generally, consider the following guidelines:</span></span>

-   <span data-ttu-id="d0252-128">視需要使用小型的根簽章，但以較大的根簽章彈性來平衡。</span><span class="sxs-lookup"><span data-stu-id="d0252-128">Use a small a root signature as necessary, though balance this with the flexibility of a larger root signature.</span></span>
-   <span data-ttu-id="d0252-129">在大型根簽章中排列參數，讓最可能經常變更的參數，或如果指定參數的低存取延遲很重要，則會先發生。</span><span class="sxs-lookup"><span data-stu-id="d0252-129">Arrange parameters in a large root signature so that the parameters most likely to change often, or if low access latency for a given parameter is important, occur first.</span></span>
-   <span data-ttu-id="d0252-130">如果方便，請使用根常數或根常數緩衝區，將常數緩衝區查看放在描述元堆積中。</span><span class="sxs-lookup"><span data-stu-id="d0252-130">If convenient, use root constants or root constant buffer views over putting constant buffer views in a descriptor heap.</span></span>

## <a name="static-samplers"></a><span data-ttu-id="d0252-131">靜態取樣器</span><span class="sxs-lookup"><span data-stu-id="d0252-131">Static samplers</span></span>

<span data-ttu-id="d0252-132">靜態取樣器 (取樣器，其中狀態已完整定義且不可變) 是根簽章的一部分，但不會計入 64 DWORD 限制。</span><span class="sxs-lookup"><span data-stu-id="d0252-132">Static samplers (samplers where the state is fully defined and immutable) are part of root signatures, but do not count towards the 64 DWORD limit.</span></span> <span data-ttu-id="d0252-133">如果取樣器可以定義為靜態，則取樣器不需要是描述項堆積的一部分。</span><span class="sxs-lookup"><span data-stu-id="d0252-133">If a sampler can be defined as static, there is no need for the sampler to be part of a descriptor heap.</span></span>

<span data-ttu-id="d0252-134">使用靜態取樣器並不會產生任何效能成本，而且根簽章可以混合使用靜態取樣器 (儲存在根簽章中，或儲存在部分硬體) 和動態取樣器 (儲存在取樣器描述項堆積) 中。</span><span class="sxs-lookup"><span data-stu-id="d0252-134">There is no performance cost to using static samplers, and a root signature can contain a mix of static samplers (stored in the root signature, or in reserved space on some hardware) and dynamic samplers (stored in a sampler descriptor heap).</span></span> <span data-ttu-id="d0252-135">描述元堆積中的取樣器可以動態指派並編制索引，而無法使用靜態取樣器。</span><span class="sxs-lookup"><span data-stu-id="d0252-135">Samplers in a descriptor heap can be dynamically assigned and indexed, which static samplers cannot.</span></span>

<span data-ttu-id="d0252-136">您可以在 HLSL 著色器中將靜態取樣器撰寫為根簽章的一部分 (請參閱 [在 HLSL) 中指定根](specifying-root-signatures-in-hlsl.md) 簽章。</span><span class="sxs-lookup"><span data-stu-id="d0252-136">Static samplers can be written as part of the root signature in HLSL shaders (refer to [Specifying Root Signatures in HLSL](specifying-root-signatures-in-hlsl.md)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d0252-137">相關主題</span><span class="sxs-lookup"><span data-stu-id="d0252-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d0252-138">根簽章</span><span class="sxs-lookup"><span data-stu-id="d0252-138">Root Signatures</span></span>](root-signatures.md)
</dt> </dl>

 

 




