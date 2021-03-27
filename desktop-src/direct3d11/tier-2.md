---
title: 第 2 層
description: 本節說明第2層支援。
ms.assetid: 4A4AEF13-2F0F-482E-9262-256C257ED85A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58fa6e8ff3dba5780e3507bb2da5273e327a30e1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842495"
---
# <a name="tier-2"></a><span data-ttu-id="764b2-103">第 2 層</span><span class="sxs-lookup"><span data-stu-id="764b2-103">Tier 2</span></span>

<span data-ttu-id="764b2-104">本節說明第2層支援。</span><span class="sxs-lookup"><span data-stu-id="764b2-104">This section describes tier 2 support.</span></span>

-   <span data-ttu-id="764b2-105">硬體至少為功能層級 11.1。</span><span class="sxs-lookup"><span data-stu-id="764b2-105">Hardware at Feature Level 11.1 minimum.</span></span>
-   <span data-ttu-id="764b2-106">前一層的所有功能 (但沒有[第 1 層](tier-1.md)特定的限制) 以及新增的下列項目︰</span><span class="sxs-lookup"><span data-stu-id="764b2-106">All features of the previous tier (without [Tier 1](tier-1.md) specific limitations) plus the additions in these following items:</span></span>
-   <span data-ttu-id="764b2-107">有著色器指示可供鉗制 LOD 與對應狀態回應使用。</span><span class="sxs-lookup"><span data-stu-id="764b2-107">Shader instructions for clamping LOD and mapped status feedback are available.</span></span> <span data-ttu-id="764b2-108">如需詳細資訊，請參閱 HLSL 並排顯示 [資源暴露](hlsl-tiled-resources-exposure.md)。</span><span class="sxs-lookup"><span data-stu-id="764b2-108">For more info, see [HLSL tiled resources exposure](hlsl-tiled-resources-exposure.md).</span></span>
-   <span data-ttu-id="764b2-109">讀取非對應的磚時，會在格式的所有非遺漏元件以及遺失元件的預設值內傳回 0。</span><span class="sxs-lookup"><span data-stu-id="764b2-109">Reads from non-mapped tiles return 0 in all non-missing components of the format, and the default for missing components.</span></span>
-   <span data-ttu-id="764b2-110">非對應磚的寫入將停止移至記憶體，但最後可能會傳至快取，該快取後續會讀取同一個可能會被選取的位址。</span><span class="sxs-lookup"><span data-stu-id="764b2-110">Writes to non-mapped tiles are stopped from going to memory but might end up in caches that subsequent reads to the same address might or might not pick up.</span></span>
-   <span data-ttu-id="764b2-111">記憶體使用量供 **NULL** 與非 **NULL** 磚共用的紋理篩選，會為 **NULL** 磚上的材質，而將 0 (含遺失格式元件預設值) 提供至整體篩選作業。</span><span class="sxs-lookup"><span data-stu-id="764b2-111">Texture filtering with a footprint that straddles **NULL** and non-**NULL** tiles contributes 0 (with defaults for missing format components) for texels on **NULL** tiles into the overall filter operation.</span></span> <span data-ttu-id="764b2-112">如果任何材質 (含非零權數) 落在 **NULL** 磚上，某些舊版的硬體會不符合此需求，並讓完整篩選結果傳回 0 (含遺失格式元件預設值)。</span><span class="sxs-lookup"><span data-stu-id="764b2-112">Some early hardware don't meet this requirement and returns 0 (with defaults for missing format components) for the full filter result if any texels (with nonzero weight) fall on a **NULL** tile.</span></span> <span data-ttu-id="764b2-113">不允許任何其他硬體遺漏將所有 (非零權數) 材質包含在篩選作業中的需求。</span><span class="sxs-lookup"><span data-stu-id="764b2-113">No other hardware will be allowed to miss the requirement to include all (nonzero weighted) texels in the filter operation.</span></span>
-   <span data-ttu-id="764b2-114">存取 **NULL** 材質會造成狀態回應上 [**CheckAccessFullyMapped**](/windows/desktop/direct3dhlsl/checkaccessfullymapped) (英文) 作業的紋理讀取傳回 False。</span><span class="sxs-lookup"><span data-stu-id="764b2-114">**NULL** texel accesses cause the [**CheckAccessFullyMapped**](/windows/desktop/direct3dhlsl/checkaccessfullymapped) operation on the status feedback for a texture read to return false.</span></span> <span data-ttu-id="764b2-115">無論紋理存取結果如何在著色器內寫入遮罩，以及多少元件為紋理格式 (紋理格式的組合可能會造成不須存取其紋理的假象)，都會發生這項問題。</span><span class="sxs-lookup"><span data-stu-id="764b2-115">This is regardless of how the texture access result might get write masked in the shader and how many components are in the texture format (the combination of which might make it appear that the texture does not need to be accessed).</span></span>
-   <span data-ttu-id="764b2-116">標準磚圖形對齊限制︰在所有維度填滿至少一個標準磚的 Mipmap 一定會使用標準並排，餘數會視為 **單位** 而封裝至 N 磚 (將 N 回報至應用程式)。</span><span class="sxs-lookup"><span data-stu-id="764b2-116">Alignment constraints for standard tile shapes: Mipmaps that fill at least one standard tile in all dimensions are guaranteed to use the standard tiling, with the remainder considered packed as a **unit** into N tiles (N reported to the application).</span></span> <span data-ttu-id="764b2-117">應用程式可將 N 磚對應至磚集區中的任意斷續位置，但必須將所有的壓縮磚都對應，否則全都不對應。</span><span class="sxs-lookup"><span data-stu-id="764b2-117">The application can map the N tiles into arbitrarily disjoint locations in a tile pool, but must either map all or none of the packed tiles.</span></span> <span data-ttu-id="764b2-118">Mip 套件是每個陣列切割中的一組獨特壓縮磚。</span><span class="sxs-lookup"><span data-stu-id="764b2-118">The mip packing is a unique set of packed tiles per array slice.</span></span>
-   <span data-ttu-id="764b2-119">支援最小/最大削減篩選。</span><span class="sxs-lookup"><span data-stu-id="764b2-119">Min/Max reduction filtering is supported.</span></span> <span data-ttu-id="764b2-120">如需 Min/Max 縮減篩選的詳細資訊，請參閱並排顯示的 [資源紋理取樣功能](tiled-resources-texture-sampling-features.md)。</span><span class="sxs-lookup"><span data-stu-id="764b2-120">For info about Min/Max reduction filtering, see [Tiled resources texture sampling features](tiled-resources-texture-sampling-features.md).</span></span>
-   <span data-ttu-id="764b2-121">在任何維度中，將任何 mipmap 小於標準磚大小的資源，都不能有大於1的陣列大小。</span><span class="sxs-lookup"><span data-stu-id="764b2-121">Tiled resources with any mipmaps less than standard tile size in any dimension are not allowed to have an array size larger than 1.</span></span>
-   <span data-ttu-id="764b2-122">當有重複的對應時，可以存取磚的限制，如 [圖格存取限制](tile-access-limitations-with-duplicate-mappings-.md)中有重複對應的說明，請繼續套用。</span><span class="sxs-lookup"><span data-stu-id="764b2-122">Limitations on how tiles can be accessed when there are duplicate mappings, described in [Tile access limitations with duplicate mappings](tile-access-limitations-with-duplicate-mappings-.md), continue to apply.</span></span>

## <a name="related-topics"></a><span data-ttu-id="764b2-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="764b2-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="764b2-124">磚資源功能層級</span><span class="sxs-lookup"><span data-stu-id="764b2-124">Tiled resources features tiers</span></span>](tiled-resources-features-tiers.md)
</dt> </dl>

 

 