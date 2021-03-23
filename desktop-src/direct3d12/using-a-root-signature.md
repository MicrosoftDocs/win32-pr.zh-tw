---
title: 使用根簽章
description: 根簽章是描述項資料表的任意排列集合的定義， (包括其配置) 、根常數和根描述項。
ms.assetid: 0131CDE4-02DB-440A-92B8-B0933C6414B0
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3babe26dc06d4f85ce3d6fb771e18c78b54a3701
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104797"
---
# <a name="using-a-root-signature"></a><span data-ttu-id="d4621-103">使用根簽章</span><span class="sxs-lookup"><span data-stu-id="d4621-103">Using a Root Signature</span></span>

<span data-ttu-id="d4621-104">根簽章是描述項資料表的任意排列集合的定義， (包括其配置) 、根常數和根描述項。</span><span class="sxs-lookup"><span data-stu-id="d4621-104">The root signature is the definition of an arbitrarily arranged collection of descriptor tables (including their layout), root constants and root descriptors.</span></span> <span data-ttu-id="d4621-105">每個專案都有最大限制的成本，因此應用程式可以在根簽章將包含的每個專案類型的數目之間，權衡平衡。</span><span class="sxs-lookup"><span data-stu-id="d4621-105">Each entry has a cost towards a maximum limit, so the application can trade off the balance between how many of each type of entry the root signature will contain.</span></span>

-   [<span data-ttu-id="d4621-106">命令清單語義</span><span class="sxs-lookup"><span data-stu-id="d4621-106">Command List Semantic</span></span>](#command-list-semantic)
-   [<span data-ttu-id="d4621-107">組合語義</span><span class="sxs-lookup"><span data-stu-id="d4621-107">Bundle Semantics</span></span>](#bundle-semantics)
-   [<span data-ttu-id="d4621-108">相關主題</span><span class="sxs-lookup"><span data-stu-id="d4621-108">Related topics</span></span>](#related-topics)

<span data-ttu-id="d4621-109">根簽章是可由 API 手動規格建立的物件。</span><span class="sxs-lookup"><span data-stu-id="d4621-109">The root signature is an object that can be created by manual specification at the API.</span></span> <span data-ttu-id="d4621-110">PSO 中的所有著色器都必須與 PSO 所指定的根配置相容，否則個別的著色器必須包含彼此相符的內嵌根配置;否則，PSO 建立將會失敗。</span><span class="sxs-lookup"><span data-stu-id="d4621-110">All shaders in a PSO must be compatible with the root layout specified with the PSO, or else the individual shaders must include embedded root layouts that match each other; otherwise, PSO creation will fail.</span></span> <span data-ttu-id="d4621-111">根簽章的一個屬性，就是在撰寫時，著色器不需要知道它，雖然根簽章也可以直接在著色器中撰寫（如有需要）。</span><span class="sxs-lookup"><span data-stu-id="d4621-111">One property of the root signature is that shaders don't have to know about it when authored, although root signatures can also be authored directly in shaders if desired.</span></span> <span data-ttu-id="d4621-112">現有的著色器資產不需要任何變更，即可與根簽章相容。</span><span class="sxs-lookup"><span data-stu-id="d4621-112">Existing shader assets do not require any changes to be compatible with root signatures.</span></span> <span data-ttu-id="d4621-113">引進著色器模型5.1，以提供一些額外的彈性 (從著色器) 內動態編制描述項的索引，並可依需要從現有的著色器資產開始逐漸採用。</span><span class="sxs-lookup"><span data-stu-id="d4621-113">Shader Model 5.1 is introduced to provide some extra flexibility (dynamic indexing of descriptors from within shaders), and can be incrementally adopted starting from existing shader assets as desired.</span></span>

## <a name="command-list-semantic"></a><span data-ttu-id="d4621-114">命令清單語義</span><span class="sxs-lookup"><span data-stu-id="d4621-114">Command List Semantic</span></span>

<span data-ttu-id="d4621-115">在命令清單的開頭，未定義根簽章。</span><span class="sxs-lookup"><span data-stu-id="d4621-115">At the beginning of a command list, the root signature is undefined.</span></span> <span data-ttu-id="d4621-116">圖形著色器的計算著色器會有不同的根簽章，每個都是在命令清單上個別指派。</span><span class="sxs-lookup"><span data-stu-id="d4621-116">Graphics shaders have a separate root signature from the compute shader, each independently assigned on a command list.</span></span> <span data-ttu-id="d4621-117">命令清單或套件組合上設定的根簽章，也必須符合 Draw/分派目前設定的 PSO;否則，行為會是未定義的。</span><span class="sxs-lookup"><span data-stu-id="d4621-117">The root signature set on a command list or bundle must also match the currently set PSO at Draw/Dispatch; otherwise, the behavior is undefined.</span></span> <span data-ttu-id="d4621-118">繪製/分派之前的暫時性根簽章不相符，例如在切換到相容的根簽章之前，先設定不相容的 PSO，然後再切換到相容的根簽章 (，只要這些都是由稱為「繪製/分派」) 。</span><span class="sxs-lookup"><span data-stu-id="d4621-118">Transient root signature mismatches before Draw/Dispatch are fine - such as setting an incompatible PSO before switching to a compatible root signature (as long as these are compatible by the time Draw/Dispatch is called).</span></span> <span data-ttu-id="d4621-119">設定 PSO 並不會變更根簽章。</span><span class="sxs-lookup"><span data-stu-id="d4621-119">Setting a PSO does not change the root signature.</span></span> <span data-ttu-id="d4621-120">應用程式必須呼叫專用的 API 來設定根簽章。</span><span class="sxs-lookup"><span data-stu-id="d4621-120">The application must call a dedicated API for setting the root signature.</span></span>

<span data-ttu-id="d4621-121">在命令清單上設定根簽章之後，配置會定義應用程式預期要提供的一組系結，以及哪些 Pso 可 (用於使用相同配置) 進行下一個繪製/分派呼叫的編譯。</span><span class="sxs-lookup"><span data-stu-id="d4621-121">Once a root signature has been set on a command list, the layout defines the set of bindings that the application is expected to provide, and which PSOs can be used (those compiled with the same layout) for the next draw/dispatch calls.</span></span> <span data-ttu-id="d4621-122">例如，應用程式可能會定義根簽章，以提供下列專案。</span><span class="sxs-lookup"><span data-stu-id="d4621-122">For example, a root signature could be defined by the application to have the following entries.</span></span> <span data-ttu-id="d4621-123">每個專案都稱為「位置」。</span><span class="sxs-lookup"><span data-stu-id="d4621-123">Each entry is referred to as a "slot".</span></span>

-   <span data-ttu-id="d4621-124">\[0 \] CBV 描述項內嵌 (根描述元) </span><span class="sxs-lookup"><span data-stu-id="d4621-124">\[0\] A CBV descriptor inline (root descriptors)</span></span>
-   <span data-ttu-id="d4621-125">\[1 \] 包含 2 SRVs、1 CBVs 和 1 UAV 的描述中繼資料表</span><span class="sxs-lookup"><span data-stu-id="d4621-125">\[1\] A descriptor table containing 2 SRVs, 1 CBVs, and 1 UAV</span></span>
-   <span data-ttu-id="d4621-126">\[2 \] 包含1個取樣器的描述項資料表</span><span class="sxs-lookup"><span data-stu-id="d4621-126">\[2\] A descriptor table containing 1 sampler</span></span>
-   <span data-ttu-id="d4621-127">\[3 \] 根常數的4x32 位集合</span><span class="sxs-lookup"><span data-stu-id="d4621-127">\[3\] A 4x32-bit collection of root constants</span></span>
-   <span data-ttu-id="d4621-128">\[4 \] 包含未指定 SRVs 數目的描述中繼資料表</span><span class="sxs-lookup"><span data-stu-id="d4621-128">\[4\] A descriptor table containing an unspecified number of SRVs</span></span>

<span data-ttu-id="d4621-129">在此情況下，在能夠發出繪製/分派之前，應用程式應該將適當的系結設定為每個位置 \[ 0 \] 和4，應用程式是以其目前的根簽章來定義。</span><span class="sxs-lookup"><span data-stu-id="d4621-129">In this case, before being able to issue a Draw/Dispatch, the application is expected to set the appropriate binding to each of the slots \[0..4\] that the application defined with its current root signature.</span></span> <span data-ttu-id="d4621-130">例如，在位置 \[ 1 \] ，必須系結描述中繼資料表，這是描述項堆積中的連續區域，其中包含 (或將在執行時包含) 2 SRVs、1 CBVs 和 1 UAV。</span><span class="sxs-lookup"><span data-stu-id="d4621-130">For instance, at slot \[1\], a descriptor table must be bound, which is a contiguous region in a descriptor heap that contains (or will contain at execution) 2 SRVs, 1 CBVs, and 1 UAV.</span></span> <span data-ttu-id="d4621-131">同樣地，描述項資料表必須設定在插槽 \[ 2 \] 和 \[ 4 \] 。</span><span class="sxs-lookup"><span data-stu-id="d4621-131">Similarly, descriptor tables must be set at slots \[2\] and \[4\].</span></span>

<span data-ttu-id="d4621-132">應用程式一次可以變更根簽章系結的一部分， (其餘部分會維持不變) 。</span><span class="sxs-lookup"><span data-stu-id="d4621-132">The application can change part of the root signature bindings at a time (the rest remain unchanged).</span></span> <span data-ttu-id="d4621-133">例如，如果只需要在繪圖之間變更的唯一一件事是位置2的其中一個常數，則必須重新系結 \[ \] 應用程式。</span><span class="sxs-lookup"><span data-stu-id="d4621-133">For example, if the only thing that needs to change between draws is one of the constants at slot \[2\], that is all the application needs to rebind.</span></span> <span data-ttu-id="d4621-134">如先前所述，驅動程式/硬體會在自動修改時的所有根簽章系結狀態。</span><span class="sxs-lookup"><span data-stu-id="d4621-134">As discussed previously, the driver/hardware versions all root signature bind state as it is modified automatically.</span></span> <span data-ttu-id="d4621-135">如果命令清單上的根簽章已變更，則所有先前的根簽章系結都會變成過時，而且必須先設定所有新的預期系結，才能進行繪製/分派;否則，行為會是未定義的。</span><span class="sxs-lookup"><span data-stu-id="d4621-135">If a root signature is changed on a command list, all previous root signature bindings become stale and all newly expected bindings must be set before Draw/Dispatch; otherwise, the behavior is undefined.</span></span> <span data-ttu-id="d4621-136">如果根簽章重複設定為目前設定的相同，則現有的根簽章系結不會變成過時。</span><span class="sxs-lookup"><span data-stu-id="d4621-136">If the root signature is redundantly set to the same one currently set, existing root signature bindings do not become stale.</span></span>

## <a name="bundle-semantics"></a><span data-ttu-id="d4621-137">組合語義</span><span class="sxs-lookup"><span data-stu-id="d4621-137">Bundle Semantics</span></span>

<span data-ttu-id="d4621-138">組合會將命令清單的根簽章系結 (系結至上述) 的命令清單範例中的不同位置。</span><span class="sxs-lookup"><span data-stu-id="d4621-138">Bundles inherit the command list's root signature bindings (the bindings to the various slots in the Command List example above).</span></span> <span data-ttu-id="d4621-139">如果套件組合需要變更部分繼承的根簽章系結，則必須先將根簽章設定為與呼叫命令清單相同， (繼承的系結不會變成過時) 。</span><span class="sxs-lookup"><span data-stu-id="d4621-139">If a bundle needs to change some of the inherited root signature bindings, it must first set the root signature to be the same as the calling command list (the inherited bindings do not become stale).</span></span> <span data-ttu-id="d4621-140">如果套件組合將根簽章設定為與呼叫的命令清單不同，則其效果與變更上述命令清單上的根簽章相同：所有先前的根簽章系結都已過時，而且必須在繪製/分派之前設定新的預期系結;否則，行為會是未定義的。</span><span class="sxs-lookup"><span data-stu-id="d4621-140">If the bundle sets the root signature to be different than the calling command list, that has the same effect as changing the root signature on the command list described above: all previous root signature bindings are stale and newly expected bindings must be set before Draw/Dispatch; otherwise, the behavior is undefined.</span></span> <span data-ttu-id="d4621-141">如果組合不需要變更任何根簽章系結，就不需要設定根簽章。</span><span class="sxs-lookup"><span data-stu-id="d4621-141">If a bundle does not need to change any root signature bindings, it does not need to set the root signature.</span></span>

<span data-ttu-id="d4621-142">下列程式碼顯示組合中的範例呼叫流程。</span><span class="sxs-lookup"><span data-stu-id="d4621-142">The following code shows an example call flow into a bundle.</span></span>

``` syntax
// Command List
...
pCmdList->SetGraphicsRootSignature(pRootSig); // new parameter space
MyEngine_SetTextures(); // bundle inherits descriptor table setting
MyEngine_SetAnimationFactor(fTime); // bundle inherits root constant
pCmdList->ExecuteBundle(...);
...
// Bundle
pBundle->SetGraphicsRootSignature(pRootSig); // same as caller, in order to inherits bindings
pBundle->SetPipelineState(pPS); 
pBundle->SetGraphicsRoot32BitConstant(drawConstantsSlot,0,drawIDOffset);
pBundle->Draw(...); // using inherited textures / animation factor
pBundle->SetGraphicsRoot32BitConstant(drawConstantsSlot,1,drawIDOffset);
pBundle->Draw(...);
...
```

<span data-ttu-id="d4621-143">當套件組合完成執行時，套件組合的任何根配置變更和/或系結變更都將會被繼承回呼叫的命令清單。</span><span class="sxs-lookup"><span data-stu-id="d4621-143">Coming out of a bundle, any root layout changes and/or binding changes a bundle makes are inherited back to the calling command list when a bundle finishes executing.</span></span>

<span data-ttu-id="d4621-144">如需有關繼承的詳細資訊，請參閱在 [Direct3D 12 中管理圖形管線狀態](managing-graphics-pipeline-state-in-direct3d-12.md)的「**圖形管線狀態繼承**」一節。</span><span class="sxs-lookup"><span data-stu-id="d4621-144">For more information on inheritance, refer to the **Graphics pipeline state inheritance** section of [Managing Graphics Pipeline State in Direct3D 12](managing-graphics-pipeline-state-in-direct3d-12.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d4621-145">相關主題</span><span class="sxs-lookup"><span data-stu-id="d4621-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d4621-146">根簽章</span><span class="sxs-lookup"><span data-stu-id="d4621-146">Root Signatures</span></span>](root-signatures.md)
</dt> </dl>

 

 




