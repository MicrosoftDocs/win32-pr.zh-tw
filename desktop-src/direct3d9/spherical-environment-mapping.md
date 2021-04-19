---
description: 球形環境地圖（或球體圖）是特殊紋理，其中包含圍繞物件的場景影像，或物件周圍的光源效果。
ms.assetid: b4a8defc-876f-4a23-a12e-e7423a1e8f89
title: " (Direct3D 9) 的球面環境對應"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9b0e7aaa123478ecc7cc327dca0b13a8aae3d0c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106966611"
---
# <a name="spherical-environment-mapping-direct3d-9"></a><span data-ttu-id="db69f-103"> (Direct3D 9) 的球面環境對應</span><span class="sxs-lookup"><span data-stu-id="db69f-103">Spherical Environment Mapping (Direct3D 9)</span></span>

<span data-ttu-id="db69f-104">球形環境地圖（或球體圖）是特殊紋理，其中包含圍繞物件的場景影像，或物件周圍的光源效果。</span><span class="sxs-lookup"><span data-stu-id="db69f-104">Spherical environment maps, or sphere maps, are special textures that contain an image of the scene surrounding an object, or the lighting effects around the object.</span></span> <span data-ttu-id="db69f-105">不同于三次的環境對應，球體地圖不會直接代表物件的周圍。</span><span class="sxs-lookup"><span data-stu-id="db69f-105">Unlike cubic environment maps, sphere maps don't directly represent an object's surroundings.</span></span> <span data-ttu-id="db69f-106">[環境對應 (Direct3D 9) ](environment-mapping.md)主題中的茶壺映射會顯示您可以使用球體對應達成的反映效果。</span><span class="sxs-lookup"><span data-stu-id="db69f-106">The teapot image in [Environment Mapping (Direct3D 9)](environment-mapping.md) topic shows the reflection effects you can achieve with sphere mapping.</span></span> <span data-ttu-id="db69f-107">球體圖是一種2D 標記法，代表物件周圍場景的完整360度觀點，如同透過魚眼的鏡頭拍攝，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="db69f-107">A sphere map is a 2D representation of the full 360-degree view of the scene surrounding of an object, as if taken through a fish-eye lens, as shown in the following illustration.</span></span>

![建築物內部之球體圖的圖例](images/spheremap.png)

## <a name="texture-coordinates-for-spherical-environment-maps"></a><span data-ttu-id="db69f-109">球面環境對應的材質座標</span><span class="sxs-lookup"><span data-stu-id="db69f-109">Texture Coordinates for Spherical Environment Maps</span></span>

<span data-ttu-id="db69f-110">您為每個接收環境對應的頂點所指定的材質座標，應該將材質定址為表面曲率所建立之反射失真的函式。</span><span class="sxs-lookup"><span data-stu-id="db69f-110">The texture coordinates that you specify for each vertex receiving an environment mapping should address the texture as a function of the reflective distortion created by the curvature of the surface.</span></span> <span data-ttu-id="db69f-111">應用程式必須針對每個頂點計算這些材質座標，以達成所要的效果。</span><span class="sxs-lookup"><span data-stu-id="db69f-111">Applications must compute these texture coordinates for each vertex to achieve the desired effect.</span></span> <span data-ttu-id="db69f-112">產生材質座標的一個簡單且有效的方式，就是使用頂點 normal 做為輸入。</span><span class="sxs-lookup"><span data-stu-id="db69f-112">One simple and effective way to generate texture coordinates uses the vertex normal as input.</span></span> <span data-ttu-id="db69f-113">雖然有數種方法存在，但在使用球體對應執行環境對應的應用程式中，會共通下列方程式。</span><span class="sxs-lookup"><span data-stu-id="db69f-113">Although several methods exist, the following equation is common among applications that perform environment mapping with sphere maps.</span></span>

![球體圖的計算紋理座標方程式](images/spheremap-formula.png)

<span data-ttu-id="db69f-115">在這些公式中，您和 v 是要計算的材質座標，而 N<sub>X</sub> 和 n<sub>Y</sub> 是相機空間頂點標準的 X 和 Y 元件。</span><span class="sxs-lookup"><span data-stu-id="db69f-115">In these formulas, u and v are the texture coordinates being computed, and N<sub>X</sub> and N<sub>Y</sub> are the x and y components of the camera-space vertex normal.</span></span> <span data-ttu-id="db69f-116">公式很簡單但有效。</span><span class="sxs-lookup"><span data-stu-id="db69f-116">The formula is simple but effective.</span></span> <span data-ttu-id="db69f-117">如果正常的 x 元件是正數，則會將法線指向右邊，並調整 u 座標以適當地定址紋理。</span><span class="sxs-lookup"><span data-stu-id="db69f-117">If the normal has a positive x component, the normal points to the right, and the u coordinate is adjusted to address the texture appropriately.</span></span> <span data-ttu-id="db69f-118">同樣地，v 座標：正面 y 表示正常的點。</span><span class="sxs-lookup"><span data-stu-id="db69f-118">Likewise for the v coordinate: positive y indicates that the normal points up.</span></span> <span data-ttu-id="db69f-119">對每個元件中的負數值而言，相反的情況。</span><span class="sxs-lookup"><span data-stu-id="db69f-119">The opposite is true for negative values in each component.</span></span>

<span data-ttu-id="db69f-120">如果直接在相機上的點，則產生的座標應該不會失真。</span><span class="sxs-lookup"><span data-stu-id="db69f-120">If the normal points directly at the camera, the resulting coordinates should receive no distortion.</span></span> <span data-ttu-id="db69f-121">這兩個座標的 + 0.5 偏差會在球體圖的中央放置零扭曲點，而 (0、0、z) 的頂點法線則會解決此點。</span><span class="sxs-lookup"><span data-stu-id="db69f-121">The +0.5 bias to both coordinates places the point of zero-distortion at the center of the sphere map, and a vertex normal of (0, 0, z) addresses this point.</span></span> <span data-ttu-id="db69f-122">此公式不會考慮一般的 z 元件，但使用公式的應用程式可以略過具有正 z 元素的垂直頂點，以優化計算。</span><span class="sxs-lookup"><span data-stu-id="db69f-122">This formula doesn't account for the z component of the normal, but applications that use the formula can optimize computations by skipping vertices with a normal that has a positive z element.</span></span> <span data-ttu-id="db69f-123">這適用于平面陰影物件，因為在相機空間中，如果正常點離相機 (正 z) ，則在呈現物件時，會挑選頂點。</span><span class="sxs-lookup"><span data-stu-id="db69f-123">This works for flat-shaded objects because, in camera space, if the normal points away from the camera (positive z), the vertex is culled when the object is rendered.</span></span> <span data-ttu-id="db69f-124">針對 Gouraud 陰影的物件，一般可以從相機指向相機 (正 x) ，而包含頂點的三角形仍然可以顯示。</span><span class="sxs-lookup"><span data-stu-id="db69f-124">For Gouraud-shaded objects, a normal can point away from the camera (positive x), and the triangle containing the vertex can still be visible.</span></span> <span data-ttu-id="db69f-125">如果您沒有為此頂點計算您和 v，可能仍會使用臉部，導致非預期的行為。</span><span class="sxs-lookup"><span data-stu-id="db69f-125">If you don't compute u and v for this vertex, the face might still be used, resulting in unexpected behavior.</span></span>

## <a name="applying-spherical-environment-maps"></a><span data-ttu-id="db69f-126">套用球形環境對應</span><span class="sxs-lookup"><span data-stu-id="db69f-126">Applying Spherical Environment Maps</span></span>

<span data-ttu-id="db69f-127">您可以使用 [**IDirect3DDevice9：： SetTexture**](/windows/desktop/api) 方法將材質設定為適當的材質階段，將環境對應套用至任何其他材質的相同方式。</span><span class="sxs-lookup"><span data-stu-id="db69f-127">You apply an environment map to objects in the same manner as for any other texture, by setting the texture to the appropriate texture stage with the [**IDirect3DDevice9::SetTexture**](/windows/desktop/api) method.</span></span> <span data-ttu-id="db69f-128">將第一個參數設定為所需紋理階段的索引，並將第二個參數設定為您為環境對應建立紋理時所傳回之 [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) 介面的位址。</span><span class="sxs-lookup"><span data-stu-id="db69f-128">Set the first parameter to the index for the desired texture stage, and set the second parameter to the address of the [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface returned when you created the texture for the environment map.</span></span> <span data-ttu-id="db69f-129">您可以視需要設定色彩和 Alpha 混合作業和引數，以達成所需的材質混合效果。</span><span class="sxs-lookup"><span data-stu-id="db69f-129">You can set the color and alpha blending operations and arguments as needed to achieve the desired texture blending effects.</span></span>

## <a name="related-topics"></a><span data-ttu-id="db69f-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="db69f-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="db69f-131">環境對應</span><span class="sxs-lookup"><span data-stu-id="db69f-131">Environment Mapping</span></span>](environment-mapping.md)
</dt> </dl>

 

 
