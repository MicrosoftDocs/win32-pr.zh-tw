---
description: 用來呈現多邊形的陰影模式對其外觀有深遠的影響。 陰影模式會決定多邊形臉部上任何點的色彩和光源濃度。 Direct3D 支援兩種網底模式。
ms.assetid: vs|directx_sdk|~\shading_modes.htm
title: " (Direct3D 9) 的陰影模式"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f84e791bed0098838760f10f6605f716444e7688
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104553173"
---
# <a name="shading-modes-direct3d-9"></a><span data-ttu-id="42f7e-105"> (Direct3D 9) 的陰影模式</span><span class="sxs-lookup"><span data-stu-id="42f7e-105">Shading Modes (Direct3D 9)</span></span>

<span data-ttu-id="42f7e-106">用來呈現多邊形的陰影模式對其外觀有深遠的影響。</span><span class="sxs-lookup"><span data-stu-id="42f7e-106">The shading mode used to render a polygon has a profound effect on its appearance.</span></span> <span data-ttu-id="42f7e-107">陰影模式會決定多邊形臉部上任何點的色彩和光源濃度。</span><span class="sxs-lookup"><span data-stu-id="42f7e-107">Shading modes determine the intensity of color and lighting at any point on a polygon face.</span></span> <span data-ttu-id="42f7e-108">Direct3D 支援兩種網底模式。</span><span class="sxs-lookup"><span data-stu-id="42f7e-108">Direct3D supports two shading modes.</span></span>

-   [<span data-ttu-id="42f7e-109">平面網底</span><span class="sxs-lookup"><span data-stu-id="42f7e-109">Flat Shading</span></span>](#flat-shading)
-   [<span data-ttu-id="42f7e-110">Gouraud 網底</span><span class="sxs-lookup"><span data-stu-id="42f7e-110">Gouraud Shading</span></span>](#gouraud-shading)

## <a name="flat-shading"></a><span data-ttu-id="42f7e-111">平面網底</span><span class="sxs-lookup"><span data-stu-id="42f7e-111">Flat Shading</span></span>

<span data-ttu-id="42f7e-112">在平面陰影模式中，Direct3D 轉譯管線會使用多邊形材質的色彩，將多邊形材質的色彩轉譯成整個多邊形的色彩。</span><span class="sxs-lookup"><span data-stu-id="42f7e-112">In the flat shading mode, the Direct3D rendering pipeline renders a polygon, using the color of the polygon material at its first vertex as the color for the entire polygon.</span></span> <span data-ttu-id="42f7e-113">以平面陰影轉譯的3D 物件如果不是共面，則會在多邊形之間呈現明顯的邊緣。</span><span class="sxs-lookup"><span data-stu-id="42f7e-113">3D objects that are rendered with flat shading have visibly sharp edges between polygons if they are not coplanar.</span></span>

<span data-ttu-id="42f7e-114">下圖顯示以平面陰影呈現的茶壺。</span><span class="sxs-lookup"><span data-stu-id="42f7e-114">The following illustration shows a teapot rendered with flat shading.</span></span> <span data-ttu-id="42f7e-115">每個多邊形的外框都清楚可見。</span><span class="sxs-lookup"><span data-stu-id="42f7e-115">The outline of each polygon is clearly visible.</span></span> <span data-ttu-id="42f7e-116">平面陰影是最快速的陰影形式。</span><span class="sxs-lookup"><span data-stu-id="42f7e-116">Flat shading is the fastest form of shading.</span></span>

![使用平面陰影的茶壺圖例](images/flattea.png)

## <a name="gouraud-shading"></a><span data-ttu-id="42f7e-118">Gouraud 網底</span><span class="sxs-lookup"><span data-stu-id="42f7e-118">Gouraud Shading</span></span>

<span data-ttu-id="42f7e-119">當 Direct3D 使用 Gouraud 陰影轉譯多邊形時，會使用頂點 normal 和光源參數來計算每個頂點的色彩。</span><span class="sxs-lookup"><span data-stu-id="42f7e-119">When Direct3D renders a polygon using Gouraud shading, it computes a color for each vertex by using the vertex normal and lighting parameters.</span></span> <span data-ttu-id="42f7e-120">然後，它會將色彩插到多邊形的臉部上，並以線性方式進行插補。</span><span class="sxs-lookup"><span data-stu-id="42f7e-120">Then, it interpolates the color across the face of the polygons The interpolation is done linearly.</span></span> <span data-ttu-id="42f7e-121">例如，如果頂點1的紅色元件是0.8，而頂點2的紅色元件是0.4，則使用 Gouraud 網底模式和 RGB 色彩模型，Direct3D 照明模組會將紅色的0.6 元件指派給這些頂點之間線條中間點的圖元。</span><span class="sxs-lookup"><span data-stu-id="42f7e-121">For example, if the red component of the color of vertex 1 is 0.8 and the red component of vertex 2 is 0.4, using the Gouraud shading mode and the RGB color model, the Direct3D lighting module assigns a red component of 0.6 to the pixel at the midpoint of the line between these vertices.</span></span>

<span data-ttu-id="42f7e-122">下圖將示範 Gouraud 陰影。</span><span class="sxs-lookup"><span data-stu-id="42f7e-122">The following illustration demonstrates Gouraud shading.</span></span> <span data-ttu-id="42f7e-123">這個茶壺是由許多平面的三角形多邊形所組成。</span><span class="sxs-lookup"><span data-stu-id="42f7e-123">This teapot is composed of many flat, triangular polygons.</span></span> <span data-ttu-id="42f7e-124">不過，Gouraud 陰影會讓物件的表面顯示為曲線且平滑。</span><span class="sxs-lookup"><span data-stu-id="42f7e-124">However, Gouraud shading makes the surface of the object appear curved and smooth.</span></span>

![使用 gouraud 網底的茶壺圖例](images/gourtea.png)

<span data-ttu-id="42f7e-126">Gouraud 陰影也可以用來顯示具有尖邊緣的物件。</span><span class="sxs-lookup"><span data-stu-id="42f7e-126">Gouraud shading can also be used to display objects with sharp edges.</span></span>

<span data-ttu-id="42f7e-127">如需詳細資訊，請參閱 [ (Direct3D 9) 的臉部和頂點一般向量 ](face-and-vertex-normal-vectors.md)。</span><span class="sxs-lookup"><span data-stu-id="42f7e-127">For more information, see [Face and Vertex Normal Vectors (Direct3D 9)](face-and-vertex-normal-vectors.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="42f7e-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="42f7e-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="42f7e-129">陰影</span><span class="sxs-lookup"><span data-stu-id="42f7e-129">Shading</span></span>](shading.md)
</dt> </dl>

 

 



