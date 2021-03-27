---
title: 非對應磚的 UAV 行為
description: 未排序存取檢視 (UAV) 讀取和寫入的行為取決於硬體支援程度。
ms.assetid: 26C40D1F-983B-4E5B-99F3-FD4E47BE1D7D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a9909f8faecd3345761ae26e60835c77aae9ab3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103931967"
---
# <a name="uav-behavior-with-non-mapped-tiles"></a><span data-ttu-id="11e12-103">非對應磚的 UAV 行為</span><span class="sxs-lookup"><span data-stu-id="11e12-103">UAV behavior with non-mapped tiles</span></span>

<span data-ttu-id="11e12-104">未排序存取檢視 (UAV) 讀取和寫入的行為取決於硬體支援程度。</span><span class="sxs-lookup"><span data-stu-id="11e12-104">Behavior of unordered access view (UAV) reads and writes depends on the level of hardware support.</span></span> <span data-ttu-id="11e12-105">如需要求的明細，請參閱並排顯示的 [資源功能層](tiled-resources-features-tiers.md)的整體讀取和寫入行為。</span><span class="sxs-lookup"><span data-stu-id="11e12-105">For a breakdown of requirements, see overall read and write behavior for [Tiled resources features tiers](tiled-resources-features-tiers.md).</span></span> <span data-ttu-id="11e12-106">本節摘要理想的行為。</span><span class="sxs-lookup"><span data-stu-id="11e12-106">This section summarizes the ideal behavior.</span></span>

<span data-ttu-id="11e12-107">讀取 UAV 非對應磚的著色器作業，對於格式的所有非遺失元件會傳回 0，對遺失元件則傳回預設值。</span><span class="sxs-lookup"><span data-stu-id="11e12-107">Shader operations that read from a non-mapped tile in a UAV return 0 in all non-missing components of the format, and the default for missing components.</span></span>

<span data-ttu-id="11e12-108">嘗試寫入到非對應磚的著色器作業，會導致無法寫入到非對應的區域（而繼續寫入到對應的區域）。</span><span class="sxs-lookup"><span data-stu-id="11e12-108">Shader operations that attempt to write to a non-mapped tile cause nothing to be written to the non-mapped area (while writes to a mapped area proceed).</span></span> <span data-ttu-id="11e12-109">[第 2 層](tier-2.md)不需要此寫入處理的理想定義；對非對應磚的寫入最後可能會在快取，後續讀取可能會收取此資料。</span><span class="sxs-lookup"><span data-stu-id="11e12-109">This ideal definition for write handling is not required by [Tier 2](tier-2.md); writes to non-mapped tiles can end up in a cache that subsequent reads could pick up.</span></span>

## <a name="related-topics"></a><span data-ttu-id="11e12-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="11e12-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="11e12-111">磚資源的管線存取</span><span class="sxs-lookup"><span data-stu-id="11e12-111">Pipeline access to tiled resources</span></span>](pipeline-access-to-tiled-resources.md)
</dt> </dl>

 

 




