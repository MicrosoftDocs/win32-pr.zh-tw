---
title: 非對應磚的 SRV 行為
description: 著色器資源檢視 (SRV) 涉及非對應磚的讀取行為取決於硬體支援程度。
ms.assetid: 9B720BEE-AB0C-4B75-92AD-3F382A107D48
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e086a4db869c3204fc560e64002ba04e8bd8ba9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104182974"
---
# <a name="srv-behavior-with-non-mapped-tiles"></a><span data-ttu-id="42c34-103">非對應磚的 SRV 行為</span><span class="sxs-lookup"><span data-stu-id="42c34-103">SRV behavior with non-mapped tiles</span></span>

<span data-ttu-id="42c34-104">著色器資源檢視 (SRV) 涉及非對應磚的讀取行為取決於硬體支援程度。</span><span class="sxs-lookup"><span data-stu-id="42c34-104">Behavior of shader resource view (SRV) reads that involve non-mapped tiles depends on the level of hardware support.</span></span> <span data-ttu-id="42c34-105">如需要求的明細，請參閱並排顯示 [資源功能層](tiled-resources-features-tiers.md)的讀取行為。</span><span class="sxs-lookup"><span data-stu-id="42c34-105">For a breakdown of requirements, see read behavior for [Tiled resources features tiers](tiled-resources-features-tiers.md).</span></span> <span data-ttu-id="42c34-106">本節摘要[第 2 層](tier-2.md)需要的理想行為。</span><span class="sxs-lookup"><span data-stu-id="42c34-106">This section summarizes the ideal behavior, which [Tier 2](tier-2.md) requires.</span></span>

<span data-ttu-id="42c34-107">請考慮可讀取 SRV 中的一組紋素的紋理篩選操作。</span><span class="sxs-lookup"><span data-stu-id="42c34-107">Consider a texture filter operation that reads from a set of texels in an SRV.</span></span> <span data-ttu-id="42c34-108">在格式的所有非遺失元件中，落在非對應磚的紋素貢獻 0（如果是遺失元件則為預設值）到整體篩選作業，對應紋素的貢獻在旁邊。</span><span class="sxs-lookup"><span data-stu-id="42c34-108">Texels that fall on non-mapped tiles contribute 0 in all non-missing components of the format (and the default for missing components) into the overall filter operation alongside contributions from mapped texels.</span></span> <span data-ttu-id="42c34-109">紋素全部都會加權和結合在一起，不受資料是來自對應或非對應磚的影響。</span><span class="sxs-lookup"><span data-stu-id="42c34-109">The texels are all weighted and combined together independent of whether the data came from mapped or non-mapped tiles.</span></span>

<span data-ttu-id="42c34-110">某些第一 [層層](tier-2.md) 級的硬體不符合這項規格需求，如果任何材質 (的非零權數) 落在非對應的磚上，則會傳回0，並以上述的預設值作為整體篩選結果。</span><span class="sxs-lookup"><span data-stu-id="42c34-110">Some first generation [Tier 2](tier-2.md) level hardware does not meet this spec requirement and returns the 0 with defaults described preceding as the overall filter result if any texels (with nonzero weight) fall on non-mapped tiles.</span></span> <span data-ttu-id="42c34-111">不允許任何其他硬體錯過將所有（非零加權）紋素包含在篩選中的需求。</span><span class="sxs-lookup"><span data-stu-id="42c34-111">No other hardware will be allowed to miss the requirement to include all (nonzero weight) texels in the filter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="42c34-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="42c34-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="42c34-113">磚資源的管線存取</span><span class="sxs-lookup"><span data-stu-id="42c34-113">Pipeline access to tiled resources</span></span>](pipeline-access-to-tiled-resources.md)
</dt> </dl>

 

 




