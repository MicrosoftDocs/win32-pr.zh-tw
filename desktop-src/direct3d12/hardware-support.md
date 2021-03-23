---
title: 硬體層
description: 第1層到第3層的硬體層級已增加管線的可用資源。
ms.assetid: 5A640BA9-3914-4481-9A0C-E18B52BD8AFE
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38773412d135aa4068f0f843c1a6ef64af06a841
ms.sourcegitcommit: 9d7585cb0b840d0d1a2b7fd02135181e69d0dc9d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/15/2020
ms.locfileid: "104548350"
---
# <a name="hardware-tiers"></a><span data-ttu-id="c33e0-103">硬體層</span><span class="sxs-lookup"><span data-stu-id="c33e0-103">Hardware Tiers</span></span>

<span data-ttu-id="c33e0-104">第1層到第3層的硬體層級已增加管線的可用資源。</span><span class="sxs-lookup"><span data-stu-id="c33e0-104">The levels of hardware from Tier 1 to Tier 3 have increasing resources available to the pipeline.</span></span>

-   [<span data-ttu-id="c33e0-105">依存于硬體的限制</span><span class="sxs-lookup"><span data-stu-id="c33e0-105">Limits dependant on hardware</span></span>](#limits-dependant-on-hardware)
-   [<span data-ttu-id="c33e0-106">變限制</span><span class="sxs-lookup"><span data-stu-id="c33e0-106">Invariable limits</span></span>](#invariable-limits)
-   [<span data-ttu-id="c33e0-107">相關主題</span><span class="sxs-lookup"><span data-stu-id="c33e0-107">Related topics</span></span>](#related-topics)

## <a name="limits-dependant-on-hardware"></a><span data-ttu-id="c33e0-108">依存于硬體的限制</span><span class="sxs-lookup"><span data-stu-id="c33e0-108">Limits dependant on hardware</span></span>



| <span data-ttu-id="c33e0-109">適用于管線的資源</span><span class="sxs-lookup"><span data-stu-id="c33e0-109">Resources Available to the Pipeline</span></span>                                                                                                              | <span data-ttu-id="c33e0-110">第 1 層</span><span class="sxs-lookup"><span data-stu-id="c33e0-110">Tier 1</span></span>                                                                   | <span data-ttu-id="c33e0-111">第 2 層</span><span class="sxs-lookup"><span data-stu-id="c33e0-111">Tier 2</span></span>        | <span data-ttu-id="c33e0-112">第 3 層</span><span class="sxs-lookup"><span data-stu-id="c33e0-112">Tier 3</span></span>        |
|--------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|---------------|---------------|
| <span data-ttu-id="c33e0-113">功能層級</span><span class="sxs-lookup"><span data-stu-id="c33e0-113">Feature levels</span></span>                                                                                                                                   | <span data-ttu-id="c33e0-114">11.0 +</span><span class="sxs-lookup"><span data-stu-id="c33e0-114">11.0+</span></span>                                                                    | <span data-ttu-id="c33e0-115">11.0 +</span><span class="sxs-lookup"><span data-stu-id="c33e0-115">11.0+</span></span>         | <span data-ttu-id="c33e0-116">11.1 +</span><span class="sxs-lookup"><span data-stu-id="c33e0-116">11.1+</span></span>         |
| <span data-ttu-id="c33e0-117">常數緩衝區視圖中最大的描述項數目 (CBV) 、著色器資源檢視 (SRV) 或未排序的存取視圖 (用於轉譯的 UAV) 堆積</span><span class="sxs-lookup"><span data-stu-id="c33e0-117">Maximum number of descriptors in a Constant Buffer View (CBV), Shader Resource View (SRV), or Unordered Access View(UAV) heap used for rendering</span></span> | <span data-ttu-id="c33e0-118">1,000,000</span><span class="sxs-lookup"><span data-stu-id="c33e0-118">1,000,000</span></span>                                                                | <span data-ttu-id="c33e0-119">1,000,000</span><span class="sxs-lookup"><span data-stu-id="c33e0-119">1,000,000</span></span>     | <span data-ttu-id="c33e0-120">1000000 +</span><span class="sxs-lookup"><span data-stu-id="c33e0-120">1,000,000+</span></span>    |
| <span data-ttu-id="c33e0-121">每個著色器階段在所有描述項資料表中的常數緩衝區視圖數目上限</span><span class="sxs-lookup"><span data-stu-id="c33e0-121">Maximum number of Constant Buffer Views in all descriptor tables per shader stage</span></span>                                                                | <span data-ttu-id="c33e0-122">14</span><span class="sxs-lookup"><span data-stu-id="c33e0-122">14</span></span>                                                                       | <span data-ttu-id="c33e0-123">14</span><span class="sxs-lookup"><span data-stu-id="c33e0-123">14</span></span>            | <span data-ttu-id="c33e0-124">**完整堆積**</span><span class="sxs-lookup"><span data-stu-id="c33e0-124">**full heap**</span></span> |
| <span data-ttu-id="c33e0-125">每個著色器階段在所有描述項資料表中的著色器資源瀏覽器數目上限</span><span class="sxs-lookup"><span data-stu-id="c33e0-125">Maximum number of Shader Resource Views in all descriptor tables per shader stage</span></span>                                                                | <span data-ttu-id="c33e0-126">128</span><span class="sxs-lookup"><span data-stu-id="c33e0-126">128</span></span>                                                                      | <span data-ttu-id="c33e0-127">**完整堆積**</span><span class="sxs-lookup"><span data-stu-id="c33e0-127">**full heap**</span></span> | <span data-ttu-id="c33e0-128">完整堆積</span><span class="sxs-lookup"><span data-stu-id="c33e0-128">full heap</span></span>     |
| <span data-ttu-id="c33e0-129">所有階段中所有描述中繼資料表的未排序存取視圖數目上限</span><span class="sxs-lookup"><span data-stu-id="c33e0-129">Maximum number of Unordered Access Views in all descriptor tables across all stages</span></span>                                                              | <span data-ttu-id="c33e0-130">64適用于功能等級 11.1 +</span><span class="sxs-lookup"><span data-stu-id="c33e0-130">64 for feature levels 11.1+</span></span><br/> <span data-ttu-id="c33e0-131">8（功能等級11）</span><span class="sxs-lookup"><span data-stu-id="c33e0-131">8 for feature level 11</span></span><br/> | <span data-ttu-id="c33e0-132">64</span><span class="sxs-lookup"><span data-stu-id="c33e0-132">64</span></span>            | <span data-ttu-id="c33e0-133">**完整堆積**</span><span class="sxs-lookup"><span data-stu-id="c33e0-133">**full heap**</span></span> |
| <span data-ttu-id="c33e0-134">每個著色器階段的所有描述項資料表中的取樣器數目上限</span><span class="sxs-lookup"><span data-stu-id="c33e0-134">Maximum number of Samplers in all descriptor tables per shader stage</span></span>                                                                             | <span data-ttu-id="c33e0-135">16</span><span class="sxs-lookup"><span data-stu-id="c33e0-135">16</span></span>                                                                       | <span data-ttu-id="c33e0-136">**2048**</span><span class="sxs-lookup"><span data-stu-id="c33e0-136">**2048**</span></span> | <span data-ttu-id="c33e0-137">2048</span><span class="sxs-lookup"><span data-stu-id="c33e0-137">2048</span></span>     |



 

<span data-ttu-id="c33e0-138">**粗體** 專案反白顯示前一層的重大改進。</span><span class="sxs-lookup"><span data-stu-id="c33e0-138">**Bold** entries highlight significant improvements over the previous tier.</span></span>

<span data-ttu-id="c33e0-139">適用于所有堆積的第1層硬體還有額外的限制，以及適用于 CBV 和 UAV 堆積的分層2硬體，根簽章中的描述項資料表所涵蓋的所有描述元堆積專案都 *必須* 在著色器執行時以描述項填入描述元，即使著色器 (可能是因為分支) 不需要描述項。</span><span class="sxs-lookup"><span data-stu-id="c33e0-139">There is an additional restriction for Tier 1 hardware that applies to all heaps, and to Tier 2 hardware that applies to CBV and UAV heaps, that all descriptor heap entries covered by descriptor tables in the root signature *must* be populated with descriptors by the time the shader executes, even if the shader (perhaps due to branching) does not need the descriptor.</span></span> <span data-ttu-id="c33e0-140">第3層硬體沒有這類限制。</span><span class="sxs-lookup"><span data-stu-id="c33e0-140">There is no such restriction for Tier 3 hardware.</span></span> <span data-ttu-id="c33e0-141">這項限制的一個緩和措施是 [Null 描述](descriptors.md)項的用心使用。</span><span class="sxs-lookup"><span data-stu-id="c33e0-141">One mitigation for this restriction is the diligent use of [Null descriptors](descriptors.md).</span></span>

## <a name="invariable-limits"></a><span data-ttu-id="c33e0-142">變限制</span><span class="sxs-lookup"><span data-stu-id="c33e0-142">Invariable limits</span></span>

<span data-ttu-id="c33e0-143">著色器可見描述項堆積中的取樣器數目上限為2048。</span><span class="sxs-lookup"><span data-stu-id="c33e0-143">The maximum number of samplers in a shader visible descriptor heap is 2048.</span></span>

<span data-ttu-id="c33e0-144">在即時根簽章之間唯一靜態取樣器的最大數目是 2032 (針對需要自己取樣器) 的驅動程式，則會保留16個。</span><span class="sxs-lookup"><span data-stu-id="c33e0-144">The maximum number of unique static samplers across live root signatures is 2032 (which leaves 16 for drivers that need their own samplers).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c33e0-145">相關主題</span><span class="sxs-lookup"><span data-stu-id="c33e0-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c33e0-146">描述元堆積</span><span class="sxs-lookup"><span data-stu-id="c33e0-146">Descriptor Heaps</span></span>](descriptor-heaps.md)
</dt> <dt>

[<span data-ttu-id="c33e0-147">硬體功能等級</span><span class="sxs-lookup"><span data-stu-id="c33e0-147">Hardware Feature Levels</span></span>](hardware-feature-levels.md)
</dt> </dl>

 

 





