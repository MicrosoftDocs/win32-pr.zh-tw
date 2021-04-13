---
description: 環境光線為場景提供定值光線。
ms.assetid: 327095a7-f4e0-48c2-9e4d-bec8493fe37e
title: " (Direct3D 9) 的環境光源"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e991981a9c1d7d24714e7014d08cefeaa94fe20f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510621"
---
# <a name="ambient-lighting-direct3d-9"></a><span data-ttu-id="926e5-103"> (Direct3D 9) 的環境光源</span><span class="sxs-lookup"><span data-stu-id="926e5-103">Ambient Lighting (Direct3D 9)</span></span>

<span data-ttu-id="926e5-104">環境光線為場景提供定值光線。</span><span class="sxs-lookup"><span data-stu-id="926e5-104">Ambient lighting provides constant lighting for a scene.</span></span> <span data-ttu-id="926e5-105">它同等地照亮所有物件端點，因為其不取決於任何其他照明因素，例如頂點標準、光源方向、光源位置、範圍或衰減。</span><span class="sxs-lookup"><span data-stu-id="926e5-105">It lights all object vertices the same because it is not dependent on any other lighting factors such as vertex normals, light direction, light position, range, or attenuation.</span></span> <span data-ttu-id="926e5-106">這是最快速的照明類型，但會產生最不實際的結果。</span><span class="sxs-lookup"><span data-stu-id="926e5-106">It is the fastest type of lighting but it produces the least realistic results.</span></span> <span data-ttu-id="926e5-107">Direct3D 包含單一全域環境光線屬性，您可加以使用而不需建立任何光線。</span><span class="sxs-lookup"><span data-stu-id="926e5-107">Direct3D contains a single global ambient light property that you can use without creating any light.</span></span> <span data-ttu-id="926e5-108">或者，您可以將任何光線物件設為提供環境光線。</span><span class="sxs-lookup"><span data-stu-id="926e5-108">Alternatively, you can set any light object to provide ambient lighting.</span></span> <span data-ttu-id="926e5-109">場景的環境光線由下列方程式描述。</span><span class="sxs-lookup"><span data-stu-id="926e5-109">The ambient lighting for a scene is described by the following equation.</span></span>

<span data-ttu-id="926e5-110">環境光源 = C ₐ \* \[ g ₐ + Sum (Atten<sub>我</sub> \* 找<sub></sub>出 \* <sub>ai</sub>) \]</span><span class="sxs-lookup"><span data-stu-id="926e5-110">Ambient Lighting = Cₐ\*\[Gₐ + sum(Atten<sub>i</sub>\*Spot<sub>i</sub>\*L<sub>ai</sub>)\]</span></span>

<span data-ttu-id="926e5-111">其中：</span><span class="sxs-lookup"><span data-stu-id="926e5-111">Where:</span></span>



| <span data-ttu-id="926e5-112">參數</span><span class="sxs-lookup"><span data-stu-id="926e5-112">Parameter</span></span>         | <span data-ttu-id="926e5-113">預設值</span><span class="sxs-lookup"><span data-stu-id="926e5-113">Default value</span></span> | <span data-ttu-id="926e5-114">類型</span><span class="sxs-lookup"><span data-stu-id="926e5-114">Type</span></span>          | <span data-ttu-id="926e5-115">Description</span><span class="sxs-lookup"><span data-stu-id="926e5-115">Description</span></span>                                                                                                                    |
|-------------------|---------------|---------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="926e5-116">Cₐ</span><span class="sxs-lookup"><span data-stu-id="926e5-116">Cₐ</span></span>                | <span data-ttu-id="926e5-117">(0,0,0,0)</span><span class="sxs-lookup"><span data-stu-id="926e5-117">(0,0,0,0)</span></span>     | <span data-ttu-id="926e5-118">D3DCOLORVALUE</span><span class="sxs-lookup"><span data-stu-id="926e5-118">D3DCOLORVALUE</span></span> | <span data-ttu-id="926e5-119">材料環境色彩</span><span class="sxs-lookup"><span data-stu-id="926e5-119">Material ambient color</span></span>                                                                                                         |
| <span data-ttu-id="926e5-120">Gₐ</span><span class="sxs-lookup"><span data-stu-id="926e5-120">Gₐ</span></span>                | <span data-ttu-id="926e5-121">(0,0,0,0)</span><span class="sxs-lookup"><span data-stu-id="926e5-121">(0,0,0,0)</span></span>     | <span data-ttu-id="926e5-122">D3DCOLORVALUE</span><span class="sxs-lookup"><span data-stu-id="926e5-122">D3DCOLORVALUE</span></span> | <span data-ttu-id="926e5-123">全域環境色彩</span><span class="sxs-lookup"><span data-stu-id="926e5-123">Global ambient color</span></span>                                                                                                           |
| <span data-ttu-id="926e5-124">Atten<sub>i</sub></span><span class="sxs-lookup"><span data-stu-id="926e5-124">Atten<sub>i</sub></span></span> | <span data-ttu-id="926e5-125">(0,0,0,0)</span><span class="sxs-lookup"><span data-stu-id="926e5-125">(0,0,0,0)</span></span>     | <span data-ttu-id="926e5-126">D3DCOLORVALUE</span><span class="sxs-lookup"><span data-stu-id="926e5-126">D3DCOLORVALUE</span></span> | <span data-ttu-id="926e5-127">第 i 個光線的光衰減。</span><span class="sxs-lookup"><span data-stu-id="926e5-127">Light attenuation of the ith light.</span></span> <span data-ttu-id="926e5-128">請參閱 [ (Direct3D 9) 的衰減和焦點因素 ](attenuation-and-spotlight-factor.md)。</span><span class="sxs-lookup"><span data-stu-id="926e5-128">See [Attenuation and Spotlight Factor (Direct3D 9)](attenuation-and-spotlight-factor.md).</span></span> |
| <span data-ttu-id="926e5-129">找<sub>我</sub></span><span class="sxs-lookup"><span data-stu-id="926e5-129">Spot<sub>i</sub></span></span>  | <span data-ttu-id="926e5-130">(0,0,0,0)</span><span class="sxs-lookup"><span data-stu-id="926e5-130">(0,0,0,0)</span></span>     | <span data-ttu-id="926e5-131">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="926e5-131">D3DVECTOR</span></span>     | <span data-ttu-id="926e5-132">第 i 個光線的聚光燈係數。</span><span class="sxs-lookup"><span data-stu-id="926e5-132">Spotlight factor of the ith light.</span></span> <span data-ttu-id="926e5-133">請參閱 [ (Direct3D 9) 的衰減和焦點因素 ](attenuation-and-spotlight-factor.md)。</span><span class="sxs-lookup"><span data-stu-id="926e5-133">See [Attenuation and Spotlight Factor (Direct3D 9)](attenuation-and-spotlight-factor.md).</span></span>  |
| <span data-ttu-id="926e5-134">Sum</span><span class="sxs-lookup"><span data-stu-id="926e5-134">sum</span></span>               | <span data-ttu-id="926e5-135">N/A</span><span class="sxs-lookup"><span data-stu-id="926e5-135">N/A</span></span>           | <span data-ttu-id="926e5-136">N/A</span><span class="sxs-lookup"><span data-stu-id="926e5-136">N/A</span></span>           | <span data-ttu-id="926e5-137">環境光線的加總</span><span class="sxs-lookup"><span data-stu-id="926e5-137">Sum of the ambient light</span></span>                                                                                                       |
| <span data-ttu-id="926e5-138">L<sub>ai</sub></span><span class="sxs-lookup"><span data-stu-id="926e5-138">L<sub>ai</sub></span></span>    | <span data-ttu-id="926e5-139">(0,0,0,0)</span><span class="sxs-lookup"><span data-stu-id="926e5-139">(0,0,0,0)</span></span>     | <span data-ttu-id="926e5-140">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="926e5-140">D3DVECTOR</span></span>     | <span data-ttu-id="926e5-141">第 i 個光線的環境光線色彩</span><span class="sxs-lookup"><span data-stu-id="926e5-141">Light ambient color of the ith light</span></span>                                                                                           |



 

<span data-ttu-id="926e5-142">Cₐ 的值為︰</span><span class="sxs-lookup"><span data-stu-id="926e5-142">The value for Cₐ is either:</span></span>

-   <span data-ttu-id="926e5-143">頂點 color1 （如果 AMBIENTMATERIALSOURCE = D3DMCS \_ color1）和第一個頂點色彩是在頂點宣告中提供。</span><span class="sxs-lookup"><span data-stu-id="926e5-143">vertex color1, if AMBIENTMATERIALSOURCE = D3DMCS\_COLOR1, and the first vertex color is supplied in the vertex declaration.</span></span>
-   <span data-ttu-id="926e5-144">頂點 color2 （如果 AMBIENTMATERIALSOURCE = D3DMCS \_ color2），而第二個頂點色彩則是在頂點宣告中提供。</span><span class="sxs-lookup"><span data-stu-id="926e5-144">vertex color2, if AMBIENTMATERIALSOURCE = D3DMCS\_COLOR2, and the second vertex color is supplied in vertex declaration.</span></span>
-   <span data-ttu-id="926e5-145">材料環境色彩。</span><span class="sxs-lookup"><span data-stu-id="926e5-145">material ambient color.</span></span>

> [!Note]  
> <span data-ttu-id="926e5-146">如果使用任一個 AMBIENTMATERIALSOURCE 選項，而且未提供頂點色彩，則會使用材質環境色彩。</span><span class="sxs-lookup"><span data-stu-id="926e5-146">If either AMBIENTMATERIALSOURCE option is used, and the vertex color is not provided, then the material ambient color is used.</span></span>

 

<span data-ttu-id="926e5-147">若要使用材料環境色彩，請使用下方範例程式碼所示的 SetMaterial。</span><span class="sxs-lookup"><span data-stu-id="926e5-147">To use the material ambient color, use SetMaterial as shown in the example code below.</span></span>

<span data-ttu-id="926e5-148">Gₐ 是全域環境色彩。</span><span class="sxs-lookup"><span data-stu-id="926e5-148">Gₐ is the global ambient color.</span></span> <span data-ttu-id="926e5-149">它是使用 Graphicsdevice (D3DRS \_ 環境) 來設定。</span><span class="sxs-lookup"><span data-stu-id="926e5-149">It is set using SetRenderState(D3DRS\_AMBIENT).</span></span> <span data-ttu-id="926e5-150">Direct3D 場景中有一個全域環境色彩。</span><span class="sxs-lookup"><span data-stu-id="926e5-150">There is one global ambient color in a Direct3D scene.</span></span> <span data-ttu-id="926e5-151">此參數與 Direct3D 光線物件無關聯。</span><span class="sxs-lookup"><span data-stu-id="926e5-151">This parameter is not associated with a Direct3D light object.</span></span>

<span data-ttu-id="926e5-152">L<sub>ai</sub> 是場景中第 i 個光線的環境色彩。</span><span class="sxs-lookup"><span data-stu-id="926e5-152">L<sub>ai</sub> is the ambient color of the ith light in the scene.</span></span> <span data-ttu-id="926e5-153">每個 Direct3D 光線都有一組屬性，其中一項是環境色彩。</span><span class="sxs-lookup"><span data-stu-id="926e5-153">Each Direct3D light has a set of properties, one of which is the ambient color.</span></span> <span data-ttu-id="926e5-154">sum(L<sub>ai</sub>) 這項字詞是場景中所有環境色彩的加總。</span><span class="sxs-lookup"><span data-stu-id="926e5-154">The term, sum(L<sub>ai</sub>) is a sum of all the ambient colors in the scene.</span></span>

## <a name="example"></a><span data-ttu-id="926e5-155">範例</span><span class="sxs-lookup"><span data-stu-id="926e5-155">Example</span></span>

<span data-ttu-id="926e5-156">在此範例中，物件使用場景環境光線和材料環境色彩上色。</span><span class="sxs-lookup"><span data-stu-id="926e5-156">In this example, the object is colored using the scene ambient light and a material ambient color.</span></span>


```
#define GRAY_COLOR  0x00bfbfbf

// create material
D3DMATERIAL9 mtrl;
ZeroMemory(&mtrl, sizeof(mtrl));
mtrl.Ambient.r = 0.75f;
mtrl.Ambient.g = 0.0f;
mtrl.Ambient.b = 0.0f;
mtrl.Ambient.a = 0.0f;
m_pd3dDevice->SetMaterial(&mtrl);
m_pd3dDevice->SetRenderState(D3DRS_AMBIENT, GRAY_COLOR);
```



<span data-ttu-id="926e5-157">根據方程式，為物件端點產生的色彩是材質色彩和淺色的組合。</span><span class="sxs-lookup"><span data-stu-id="926e5-157">According to the equation, the resulting color for the object vertices is a combination of the material color and the light color.</span></span>

<span data-ttu-id="926e5-158">下方兩個圖例顯示材質色彩 (灰色)，以及淺色 (鮮紅)。</span><span class="sxs-lookup"><span data-stu-id="926e5-158">The following two illustrations show the material color, which is gray, and the light color, which is bright red.</span></span>

![灰球體圖例](images/amb1.jpg)![紅色球體圖例](images/lightred.jpg)

<span data-ttu-id="926e5-161">下圖顯示產生的場景。</span><span class="sxs-lookup"><span data-stu-id="926e5-161">The resulting scene is shown in the following illustration.</span></span> <span data-ttu-id="926e5-162">場景中唯一的物件為球體。</span><span class="sxs-lookup"><span data-stu-id="926e5-162">The only object in the scene is a sphere.</span></span> <span data-ttu-id="926e5-163">環境光線使用相同色彩照亮所有物件端點。</span><span class="sxs-lookup"><span data-stu-id="926e5-163">Ambient light lights all object vertices with the same color.</span></span> <span data-ttu-id="926e5-164">其不取決於頂點標準或光線方向。</span><span class="sxs-lookup"><span data-stu-id="926e5-164">It is not dependent on the vertex normal or the light direction.</span></span> <span data-ttu-id="926e5-165">如此一來，球體看起來像是 2D 圓形，因為物件表面周圍的陰影並無差別。</span><span class="sxs-lookup"><span data-stu-id="926e5-165">As a result, the sphere looks like a 2D circle because there is no difference in shading around the surface of the object.</span></span>

![使用環境光線的球體圖例](images/lighta.jpg)

<span data-ttu-id="926e5-167">若要讓物件看起來更逼真，請在環境光線之外套用光源擴散或反射光源。</span><span class="sxs-lookup"><span data-stu-id="926e5-167">To give objects a more realistic look, apply diffuse or specular lighting in addition to ambient lighting.</span></span>

## <a name="related-topics"></a><span data-ttu-id="926e5-168">相關主題</span><span class="sxs-lookup"><span data-stu-id="926e5-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="926e5-169">燈光數學</span><span class="sxs-lookup"><span data-stu-id="926e5-169">Mathematics of Lighting</span></span>](mathematics-of-lighting.md)
</dt> </dl>

 

 



