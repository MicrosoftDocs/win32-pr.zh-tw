---
description: Direct3D 10 的座標系統是針對圖元和材質所定義。
ms.assetid: c8c269e7-6e2a-4b5d-847c-6779e276b9af
title: " (Direct3D 10) 協調系統"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ba84cd7d807474a1ff41f873d16cbd7eee07224
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689163"
---
# <a name="coordinate-systems-direct3d-10"></a><span data-ttu-id="904c0-103"> (Direct3D 10) 協調系統</span><span class="sxs-lookup"><span data-stu-id="904c0-103">Coordinate Systems (Direct3D 10)</span></span>

<span data-ttu-id="904c0-104">Direct3D 10 的座標系統是針對圖元和材質所定義。</span><span class="sxs-lookup"><span data-stu-id="904c0-104">Coordinate systems for Direct3D 10 are defined for pixels and texels.</span></span>



|                                                                                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="904c0-105">Direct3D 9 與 Direct3D 10 之間的差異：</span><span class="sxs-lookup"><span data-stu-id="904c0-105">Differences between Direct3D 9 and Direct3D 10:</span></span><br/> <span data-ttu-id="904c0-106">Direct3D 10 會將左上角的左上角定義為呈現目標的原點。</span><span class="sxs-lookup"><span data-stu-id="904c0-106">Direct3D 10 defines the upper-left corner of the upper-left pixel as the origin of a render target.</span></span><br/> <span data-ttu-id="904c0-107">Direct3D 9 會將左上圖元的中央定義為呈現目標的原點。</span><span class="sxs-lookup"><span data-stu-id="904c0-107">Direct3D 9 defines the center of the upper-left pixel as the origin of a render target.</span></span><br/> |



 

-   [<span data-ttu-id="904c0-108">圖元座標系統</span><span class="sxs-lookup"><span data-stu-id="904c0-108">Pixel Coordinate System</span></span>](#pixel-coordinate-system)
    -   [<span data-ttu-id="904c0-109">Direct3D 9 的圖元座標系統</span><span class="sxs-lookup"><span data-stu-id="904c0-109">Pixel Coordinate System for Direct3D 9</span></span>](#pixel-coordinate-system-for-direct3d-9)
-   [<span data-ttu-id="904c0-110">材質座標系統</span><span class="sxs-lookup"><span data-stu-id="904c0-110">Texel Coordinate System</span></span>](#texel-coordinate-system)
    -   [<span data-ttu-id="904c0-111">材質座標系統</span><span class="sxs-lookup"><span data-stu-id="904c0-111">Texel Coordinate System</span></span>](#texel-coordinate-system)
-   [<span data-ttu-id="904c0-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="904c0-112">Related topics</span></span>](#related-topics)

## <a name="pixel-coordinate-system"></a><span data-ttu-id="904c0-113">像素座標系統</span><span class="sxs-lookup"><span data-stu-id="904c0-113">Pixel Coordinate System</span></span>

<span data-ttu-id="904c0-114">Direct3D 10 中的圖元座標系統會定義位於左上角之呈現目標的原點。</span><span class="sxs-lookup"><span data-stu-id="904c0-114">The pixel coordinate system in Direct3D 10 defines the origin of a render target at the upper-left corner.</span></span> <span data-ttu-id="904c0-115">如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="904c0-115">as shown in the following diagram.</span></span> <span data-ttu-id="904c0-116">像素中心離整數位置偏移 (0.5f, 0.5f)。</span><span class="sxs-lookup"><span data-stu-id="904c0-116">Pixel centers are offset by (0.5f,0.5f) from integer locations.</span></span>

![direct3d 10 中的像素座標系統圖表](images/d3d10-coordspix10.png)

### <a name="pixel-coordinate-system-for-direct3d-9"></a><span data-ttu-id="904c0-118">Direct3D 9 的圖元座標系統</span><span class="sxs-lookup"><span data-stu-id="904c0-118">Pixel Coordinate System for Direct3D 9</span></span>

<span data-ttu-id="904c0-119">以下是 Direct3D 9 的圖元座標系統，其定義原點或轉譯目標作為左上角圖元的中心， (0.5，0.5) 遠離左上角，如下列圖表所示。</span><span class="sxs-lookup"><span data-stu-id="904c0-119">For reference, here is the pixel coordinate system for Direct3D 9, which defined the origin or a render target as the center of the upper-left pixel, (0.5,0.5) away from the upper left corner, as shown in the following diagram.</span></span> <span data-ttu-id="904c0-120">在 Direct3D 9 中，圖元中心位於整數位置。</span><span class="sxs-lookup"><span data-stu-id="904c0-120">In Direct3D 9, pixel centers are at integer locations.</span></span>

![direct3d 9 中圖元座標系統的圖表](images/d3d10-coordspix9.png)

## <a name="texel-coordinate-system"></a><span data-ttu-id="904c0-122">紋素座標系統</span><span class="sxs-lookup"><span data-stu-id="904c0-122">Texel Coordinate System</span></span>

<span data-ttu-id="904c0-123">紋素座標系統在紋理左上角的原點，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="904c0-123">The texel coordinate system has its origin at the top-left corner of the texture, as shown in the following diagram.</span></span> <span data-ttu-id="904c0-124">這使得在 Direct3D 10) 中呈現螢幕對齊的材質很簡單 (，因為圖元座標系統與材質座標系統對齊。</span><span class="sxs-lookup"><span data-stu-id="904c0-124">This makes rendering screen-aligned textures trivial (in Direct3D 10), as the pixel coordinate system is aligned with the texel coordinate system.</span></span>

![紋理座標系統的圖表](images/d3d10-coordstex10.png)

### <a name="texel-coordinate-system"></a><span data-ttu-id="904c0-126">紋素座標系統</span><span class="sxs-lookup"><span data-stu-id="904c0-126">Texel Coordinate System</span></span>

<span data-ttu-id="904c0-127">紋理座標以標準化或按比例調整之數字表示。每個紋理座標對應特定紋素，如下所示︰</span><span class="sxs-lookup"><span data-stu-id="904c0-127">Texture coordinates are represented with either a normalized or a scaled number; each texture coordinate is mapped to a specific texel as follows:</span></span>

<span data-ttu-id="904c0-128">對於標準座標︰</span><span class="sxs-lookup"><span data-stu-id="904c0-128">For a normalized coordinate:</span></span>

-   <span data-ttu-id="904c0-129">點取樣：材質 \# = floor (U \* 寬度) </span><span class="sxs-lookup"><span data-stu-id="904c0-129">Point sampling: Texel \# = floor(U \* Width)</span></span>
-   <span data-ttu-id="904c0-130">線性取樣：左方材質 \# = floor (U \* 寬度) ，Right 材質 \# = 左方材質 \# + 1</span><span class="sxs-lookup"><span data-stu-id="904c0-130">Linear sampling: Left Texel \# = floor(U \* Width), Right Texel \# = Left Texel \# + 1</span></span>

<span data-ttu-id="904c0-131">對於按比例調整座標︰</span><span class="sxs-lookup"><span data-stu-id="904c0-131">For a scaled coordinate:</span></span>

-   <span data-ttu-id="904c0-132">點取樣：材質 \# = floor (U) </span><span class="sxs-lookup"><span data-stu-id="904c0-132">Point sampling: Texel \# = floor(U)</span></span>
-   <span data-ttu-id="904c0-133">線性取樣：左方材質 \# = floor (U-0.5) ，Right 材質 \# = Left 材質 \# + 1</span><span class="sxs-lookup"><span data-stu-id="904c0-133">Linear sampling: Left Texel \# = floor(U - 0.5), Right Texel \# = Left Texel \# + 1</span></span>

<span data-ttu-id="904c0-134">寬度是紋理的寬度 (以紋素為單位)。</span><span class="sxs-lookup"><span data-stu-id="904c0-134">Where the width, is the width of the texture (in texels).</span></span>

<span data-ttu-id="904c0-135">計算紋素位置之後，就會紋理尋址環繞。</span><span class="sxs-lookup"><span data-stu-id="904c0-135">Texture address wrapping occurs after the texel location is computed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="904c0-136">相關主題</span><span class="sxs-lookup"><span data-stu-id="904c0-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="904c0-137"> (Direct3D 10) 的資源 </span><span class="sxs-lookup"><span data-stu-id="904c0-137">Resources (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 




