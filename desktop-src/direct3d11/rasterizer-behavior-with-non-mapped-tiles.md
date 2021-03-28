---
title: 非對應磚的轉譯器行為
description: 本節說明非對應磚的轉譯器行為。
ms.assetid: 3477A621-7051-4585-AB58-523EE64CDC5C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54230321f4286b92a3444e3f74167ee7b8711c3f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104990630"
---
# <a name="rasterizer-behavior-with-non-mapped-tiles"></a><span data-ttu-id="6cf71-103">非對應磚的轉譯器行為</span><span class="sxs-lookup"><span data-stu-id="6cf71-103">Rasterizer behavior with non-mapped tiles</span></span>

<span data-ttu-id="6cf71-104">本節說明非對應磚的轉譯器行為。</span><span class="sxs-lookup"><span data-stu-id="6cf71-104">This section describes rasterizer behavior with non-mapped tiles.</span></span>

## <a name="depthstencilview"></a><span data-ttu-id="6cf71-105">DepthStencilView</span><span class="sxs-lookup"><span data-stu-id="6cf71-105">DepthStencilView</span></span>

<span data-ttu-id="6cf71-106">深度樣板檢視 (DSV) 的行為會根據硬體支援程度讀取和寫入。</span><span class="sxs-lookup"><span data-stu-id="6cf71-106">Behavior of depth stencil view (DSV) reads and writes depends on the level of hardware support.</span></span> <span data-ttu-id="6cf71-107">如需要求的明細，請參閱並排顯示的 [資源功能層](tiled-resources-features-tiers.md)的整體讀取和寫入行為。</span><span class="sxs-lookup"><span data-stu-id="6cf71-107">For a breakdown of requirements, see overall read and write behavior for [Tiled resources features tiers](tiled-resources-features-tiers.md).</span></span>

<span data-ttu-id="6cf71-108">以下是理想的行為︰</span><span class="sxs-lookup"><span data-stu-id="6cf71-108">Here is the ideal behavior:</span></span>

<span data-ttu-id="6cf71-109">如果磚在 DepthStencilView 中未對應，讀取深度的傳回值為 0，然後饋入為深度讀取值設定的任何作業。</span><span class="sxs-lookup"><span data-stu-id="6cf71-109">If a tile isn't mapped in the DepthStencilView, the return value from reading depth is 0, which is then fed into whatever operations are configured for the depth read value.</span></span> <span data-ttu-id="6cf71-110">對遺失的深度磚的寫入會捨棄。</span><span class="sxs-lookup"><span data-stu-id="6cf71-110">Writes to the missing depth tile are dropped.</span></span> <span data-ttu-id="6cf71-111">[第 2 層](tier-2.md)不需要此寫入處理的理想定義；對非對應磚的寫入最後可能會在快取，後續讀取可能會收取此資料。</span><span class="sxs-lookup"><span data-stu-id="6cf71-111">This ideal definition for write handling is not required by [Tier 2](tier-2.md); writes to non-mapped tiles can end up in a cache that subsequent reads could pick up.</span></span>

## <a name="rendertargetview"></a><span data-ttu-id="6cf71-112">RenderTargetView</span><span class="sxs-lookup"><span data-stu-id="6cf71-112">RenderTargetView</span></span>

<span data-ttu-id="6cf71-113">轉譯目標檢視 (RTV) 的行為會根據硬體支援的層級讀取和寫入。</span><span class="sxs-lookup"><span data-stu-id="6cf71-113">Behavior of render target view (RTV) reads and writes depends on the level of hardware support.</span></span> <span data-ttu-id="6cf71-114">如需要求的明細，請參閱並排顯示的 [資源功能層](tiled-resources-features-tiers.md)的整體讀取和寫入行為。</span><span class="sxs-lookup"><span data-stu-id="6cf71-114">For a breakdown of requirements, see overall read and write behavior for [Tiled resources features tiers](tiled-resources-features-tiers.md).</span></span>

<span data-ttu-id="6cf71-115">在所有實作上，同時繫結的不同 RTV (和 DSV) 可能會有已對應和未對應的不同區域，也會有不同大小的表面格式 (亦即不同磚圖形)。</span><span class="sxs-lookup"><span data-stu-id="6cf71-115">On all implementations, different RTVs (and DSV) bound simultaneously can have different areas mapped versus non-mapped and can have different sized surface formats (which means different tile shapes).</span></span>

<span data-ttu-id="6cf71-116">以下是理想的行為︰</span><span class="sxs-lookup"><span data-stu-id="6cf71-116">Here is the ideal behavior:</span></span>

<span data-ttu-id="6cf71-117">在遺失磚中從 RTV 的讀取傳回 0，寫入會捨棄。</span><span class="sxs-lookup"><span data-stu-id="6cf71-117">Reads from RTVs return 0 in missing tiles and writes are dropped.</span></span> <span data-ttu-id="6cf71-118">[第 2 層](tier-2.md)不需要此寫入處理的理想定義；對非對應磚的寫入最後可能會在快取，後續讀取可能會收取此資料。</span><span class="sxs-lookup"><span data-stu-id="6cf71-118">This ideal definition for write handling is not required by [Tier 2](tier-2.md); writes to non-mapped tiles can end up in a cache that subsequent reads could pick up.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6cf71-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="6cf71-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6cf71-120">磚資源的管線存取</span><span class="sxs-lookup"><span data-stu-id="6cf71-120">Pipeline access to tiled resources</span></span>](pipeline-access-to-tiled-resources.md)
</dt> </dl>

 

 




