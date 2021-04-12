---
description: 在調整任何衰減效果的光線強度之後，光源引擎會計算從頂點反射的剩餘光線有多少，假設頂點角度為垂直，事件的方向為光源。
ms.assetid: 29280a02-1c26-4b54-8468-707dd96dea1d
title: " (Direct3D 9) 的擴散照明"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f51e45093786348aaa115ec38c420acec471f718
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108417"
---
# <a name="diffuse-lighting-direct3d-9"></a><span data-ttu-id="1ea0b-103"> (Direct3D 9) 的擴散照明</span><span class="sxs-lookup"><span data-stu-id="1ea0b-103">Diffuse Lighting (Direct3D 9)</span></span>

<span data-ttu-id="1ea0b-104">在調整任何衰減效果的光線強度之後，光源引擎會計算從頂點反射的剩餘光線有多少，假設頂點角度為垂直，事件的方向為光源。</span><span class="sxs-lookup"><span data-stu-id="1ea0b-104">After adjusting the light intensity for any attenuation effects, the lighting engine computes how much of the remaining light reflects from a vertex, given the angle of the vertex normal and the direction of the incident light.</span></span> <span data-ttu-id="1ea0b-105">光源引擎會針對方向光源跳至此步驟，因為它們不會因為距離而衰減。</span><span class="sxs-lookup"><span data-stu-id="1ea0b-105">The lighting engine skips to this step for directional lights because they do not attenuate over distance.</span></span> <span data-ttu-id="1ea0b-106">系統會考量兩種反射類型：擴散和反射，並使用不同的公式判斷分別反射的光線量。</span><span class="sxs-lookup"><span data-stu-id="1ea0b-106">The system considers two reflection types, diffuse and specular, and uses a different formula to determine how much light is reflected for each.</span></span> <span data-ttu-id="1ea0b-107">在計算反射光線量之後，Direct3D 會將這些新值套用至目前材質的擴散和反射的反射率屬性。</span><span class="sxs-lookup"><span data-stu-id="1ea0b-107">After calculating the amounts of light reflected, Direct3D applies these new values to the diffuse and specular reflectance properties of the current material.</span></span> <span data-ttu-id="1ea0b-108">產生的色彩值會是擴散和反射元件，點陣化用來產生 Gouraud Shading 和反射強光。</span><span class="sxs-lookup"><span data-stu-id="1ea0b-108">The resulting color values are the diffuse and specular components that the rasterizer uses to produce Gouraud shading and specular highlighting.</span></span>

<span data-ttu-id="1ea0b-109">擴散光源以下列方程式描述。</span><span class="sxs-lookup"><span data-stu-id="1ea0b-109">Diffuse lighting is described by the following equation.</span></span>

<span data-ttu-id="1ea0b-110">擴散光源 = 加總 \[ C<sub>d</sub> \* L<sub>d</sub> \* (N<sup>。</sup>L<sub>dir</sub>) \* Atten \* 位置\]</span><span class="sxs-lookup"><span data-stu-id="1ea0b-110">Diffuse Lighting = sum\[C<sub>d</sub>\*L<sub>d</sub>\*(N<sup>.</sup>L<sub>dir</sub>)\*Atten\*Spot\]</span></span>



| <span data-ttu-id="1ea0b-111">參數</span><span class="sxs-lookup"><span data-stu-id="1ea0b-111">Parameter</span></span>       | <span data-ttu-id="1ea0b-112">預設值</span><span class="sxs-lookup"><span data-stu-id="1ea0b-112">Default value</span></span> | <span data-ttu-id="1ea0b-113">類型</span><span class="sxs-lookup"><span data-stu-id="1ea0b-113">Type</span></span>          | <span data-ttu-id="1ea0b-114">Description</span><span class="sxs-lookup"><span data-stu-id="1ea0b-114">Description</span></span>                                                                                                   |
|-----------------|---------------|---------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ea0b-115">Sum</span><span class="sxs-lookup"><span data-stu-id="1ea0b-115">sum</span></span>             | <span data-ttu-id="1ea0b-116">N/A</span><span class="sxs-lookup"><span data-stu-id="1ea0b-116">N/A</span></span>           | <span data-ttu-id="1ea0b-117">N/A</span><span class="sxs-lookup"><span data-stu-id="1ea0b-117">N/A</span></span>           | <span data-ttu-id="1ea0b-118">每道光的擴散元件的總和。</span><span class="sxs-lookup"><span data-stu-id="1ea0b-118">Summation of each light's diffuse component.</span></span>                                                                  |
| <span data-ttu-id="1ea0b-119">C<sub>d</sub></span><span class="sxs-lookup"><span data-stu-id="1ea0b-119">C<sub>d</sub></span></span>   | <span data-ttu-id="1ea0b-120">(0,0,0,0)</span><span class="sxs-lookup"><span data-stu-id="1ea0b-120">(0,0,0,0)</span></span>     | <span data-ttu-id="1ea0b-121">D3DCOLORVALUE</span><span class="sxs-lookup"><span data-stu-id="1ea0b-121">D3DCOLORVALUE</span></span> | <span data-ttu-id="1ea0b-122">擴散色彩。</span><span class="sxs-lookup"><span data-stu-id="1ea0b-122">Diffuse color.</span></span>                                                                                                |
| <span data-ttu-id="1ea0b-123">L<sub>d</sub></span><span class="sxs-lookup"><span data-stu-id="1ea0b-123">L<sub>d</sub></span></span>   | <span data-ttu-id="1ea0b-124">(0,0,0,0)</span><span class="sxs-lookup"><span data-stu-id="1ea0b-124">(0,0,0,0)</span></span>     | <span data-ttu-id="1ea0b-125">D3DCOLORVALUE</span><span class="sxs-lookup"><span data-stu-id="1ea0b-125">D3DCOLORVALUE</span></span> | <span data-ttu-id="1ea0b-126">光線擴散色彩。</span><span class="sxs-lookup"><span data-stu-id="1ea0b-126">Light diffuse color.</span></span>                                                                                          |
| <span data-ttu-id="1ea0b-127">N</span><span class="sxs-lookup"><span data-stu-id="1ea0b-127">N</span></span>               | <span data-ttu-id="1ea0b-128">N/A</span><span class="sxs-lookup"><span data-stu-id="1ea0b-128">N/A</span></span>           | <span data-ttu-id="1ea0b-129">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="1ea0b-129">D3DVECTOR</span></span>     | <span data-ttu-id="1ea0b-130">頂點垂直</span><span class="sxs-lookup"><span data-stu-id="1ea0b-130">Vertex normal</span></span>                                                                                                 |
| <span data-ttu-id="1ea0b-131">L<sub>dir</sub></span><span class="sxs-lookup"><span data-stu-id="1ea0b-131">L<sub>dir</sub></span></span> | <span data-ttu-id="1ea0b-132">N/A</span><span class="sxs-lookup"><span data-stu-id="1ea0b-132">N/A</span></span>           | <span data-ttu-id="1ea0b-133">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="1ea0b-133">D3DVECTOR</span></span>     | <span data-ttu-id="1ea0b-134">從物件頂點到光線的方向向量。</span><span class="sxs-lookup"><span data-stu-id="1ea0b-134">Direction vector from object vertex to the light.</span></span>                                                             |
| <span data-ttu-id="1ea0b-135">Atten</span><span class="sxs-lookup"><span data-stu-id="1ea0b-135">Atten</span></span>           | <span data-ttu-id="1ea0b-136">N/A</span><span class="sxs-lookup"><span data-stu-id="1ea0b-136">N/A</span></span>           | <span data-ttu-id="1ea0b-137">FLOAT</span><span class="sxs-lookup"><span data-stu-id="1ea0b-137">FLOAT</span></span>         | <span data-ttu-id="1ea0b-138">光線衰減。</span><span class="sxs-lookup"><span data-stu-id="1ea0b-138">Light attenuation.</span></span> <span data-ttu-id="1ea0b-139">請參閱 [ (Direct3D 9) 的衰減和焦點因素 ](attenuation-and-spotlight-factor.md)。</span><span class="sxs-lookup"><span data-stu-id="1ea0b-139">See [Attenuation and Spotlight Factor (Direct3D 9)](attenuation-and-spotlight-factor.md).</span></span> |
| <span data-ttu-id="1ea0b-140">付現</span><span class="sxs-lookup"><span data-stu-id="1ea0b-140">Spot</span></span>            | <span data-ttu-id="1ea0b-141">N/A</span><span class="sxs-lookup"><span data-stu-id="1ea0b-141">N/A</span></span>           | <span data-ttu-id="1ea0b-142">FLOAT</span><span class="sxs-lookup"><span data-stu-id="1ea0b-142">FLOAT</span></span>         | <span data-ttu-id="1ea0b-143">聚光燈係數。</span><span class="sxs-lookup"><span data-stu-id="1ea0b-143">Spotlight factor.</span></span> <span data-ttu-id="1ea0b-144">請參閱 [ (Direct3D 9) 的衰減和焦點因素 ](attenuation-and-spotlight-factor.md)。</span><span class="sxs-lookup"><span data-stu-id="1ea0b-144">See [Attenuation and Spotlight Factor (Direct3D 9)](attenuation-and-spotlight-factor.md).</span></span>  |



 

<span data-ttu-id="1ea0b-145">C<sub>d</sub> 的值可能是：</span><span class="sxs-lookup"><span data-stu-id="1ea0b-145">The value for C<sub>d</sub> is either:</span></span>

-   <span data-ttu-id="1ea0b-146">頂點 color1 （如果 DIFFUSEMATERIALSOURCE = D3DMCS \_ color1）和第一個頂點色彩是在頂點宣告中提供。</span><span class="sxs-lookup"><span data-stu-id="1ea0b-146">vertex color1, if DIFFUSEMATERIALSOURCE = D3DMCS\_COLOR1, and the first vertex color is supplied in the vertex declaration.</span></span>
-   <span data-ttu-id="1ea0b-147">頂點 color2 （如果 DIFFUSEMATERIALSOURCE = D3DMCS \_ color2），而第二個頂點色彩則是在頂點宣告中提供。</span><span class="sxs-lookup"><span data-stu-id="1ea0b-147">vertex color2, if DIFFUSEMATERIALSOURCE = D3DMCS\_COLOR2, and the second vertex color is supplied in the vertex declaration.</span></span>
-   <span data-ttu-id="1ea0b-148">材質擴散色彩</span><span class="sxs-lookup"><span data-stu-id="1ea0b-148">material diffuse color</span></span>

> [!Note]  
> <span data-ttu-id="1ea0b-149">如果使用任一個 DIFFUSEMATERIALSOURCE 選項，而且未提供頂點色彩，則會使用材質擴散色彩。</span><span class="sxs-lookup"><span data-stu-id="1ea0b-149">If either DIFFUSEMATERIALSOURCE option is used, and the vertex color is not provided, the material diffuse color is used.</span></span>

 

<span data-ttu-id="1ea0b-150">若要計算衰減 (Atten) 或焦點特性 (找出) ，請參閱 [ (Direct3D 9) 的衰減和焦點因素 ](attenuation-and-spotlight-factor.md)。</span><span class="sxs-lookup"><span data-stu-id="1ea0b-150">To calculate the attenuation (Atten) or the spotlight characteristics (Spot), see [Attenuation and Spotlight Factor (Direct3D 9)](attenuation-and-spotlight-factor.md).</span></span>

<span data-ttu-id="1ea0b-151">所有的光分開處理和插補之後，擴散元件會鉗制為從 0 到 255。</span><span class="sxs-lookup"><span data-stu-id="1ea0b-151">Diffuse components are clamped to be from 0 to 255, after all lights are processed and interpolated separately.</span></span> <span data-ttu-id="1ea0b-152">產生的擴散光源值是環境、擴散及發光值的組合。</span><span class="sxs-lookup"><span data-stu-id="1ea0b-152">The resulting diffuse lighting value is a combination of the ambient, diffuse and emissive light values.</span></span>

## <a name="example"></a><span data-ttu-id="1ea0b-153">範例</span><span class="sxs-lookup"><span data-stu-id="1ea0b-153">Example</span></span>

<span data-ttu-id="1ea0b-154">在這個範例中，物件是使用淺擴散色彩和材質擴散色彩著色。</span><span class="sxs-lookup"><span data-stu-id="1ea0b-154">In this example, the object is colored using the light diffuse color and a material diffuse color.</span></span> <span data-ttu-id="1ea0b-155">程式碼如下所示。</span><span class="sxs-lookup"><span data-stu-id="1ea0b-155">The code is shown below.</span></span>


```
D3DMATERIAL9 mtrl;
ZeroMemory( &mtrl, sizeof(mtrl) );

D3DLIGHT9 light;
ZeroMemory( &light, sizeof(light) );
light.Type = D3DLIGHT_DIRECTIONAL;

D3DXVECTOR3 vecDir;
vecDir = D3DXVECTOR3(0.5f, 0.0f, -0.5f);
D3DXVec3Normalize( (D3DXVECTOR3*)&light.Direction, &vecDir );

// set directional light diffuse color
light.Diffuse.r = 1.0f;
light.Diffuse.g = 1.0f;
light.Diffuse.b = 1.0f;
light.Diffuse.a = 1.0f;
m_pd3dDevice->SetLight( 0, &light );
m_pd3dDevice->LightEnable( 0, TRUE );

// if a material is used, SetRenderState must be used
// vertex color = light diffuse color * material diffuse color
mtrl.Diffuse.r = 0.75f;
mtrl.Diffuse.g = 0.0f;
mtrl.Diffuse.b = 0.0f;
mtrl.Diffuse.a = 0.0f;
m_pd3dDevice->SetMaterial( &mtrl );
m_pd3dDevice->SetRenderState(D3DRS_DIFFUSEMATERIALSOURCE, D3DMCS_MATERIAL);
```



<span data-ttu-id="1ea0b-156">根據方程式，為物件端點產生的色彩是材質色彩和淺色的組合。</span><span class="sxs-lookup"><span data-stu-id="1ea0b-156">According to the equation, the resulting color for the object vertices is a combination of the material color and the light color.</span></span>

<span data-ttu-id="1ea0b-157">下方兩個圖例顯示材質色彩 (灰色)，以及淺色 (鮮紅)。</span><span class="sxs-lookup"><span data-stu-id="1ea0b-157">The following two illustrations show the material color, which is gray, and the light color, which is bright red.</span></span>

![灰球體圖例](images/amb1.jpg)![紅色球體圖例](images/lightred.jpg)

<span data-ttu-id="1ea0b-160">下圖顯示產生的場景。</span><span class="sxs-lookup"><span data-stu-id="1ea0b-160">The resulting scene is shown in the following illustration.</span></span> <span data-ttu-id="1ea0b-161">場景中唯一的物件為球體。</span><span class="sxs-lookup"><span data-stu-id="1ea0b-161">The only object in the scene is a sphere.</span></span> <span data-ttu-id="1ea0b-162">擴散光線計算會採用材質和淺擴散色彩，並使用內積修改光線方向和頂點直角之間的角度。</span><span class="sxs-lookup"><span data-stu-id="1ea0b-162">The diffuse lighting calculation takes the material and light diffuse color and modifies it by the angle between the light direction and the vertex normal using the dot product.</span></span> <span data-ttu-id="1ea0b-163">如此一來，球體的背面會隨著球體表面曲線遠離光源而變暗。</span><span class="sxs-lookup"><span data-stu-id="1ea0b-163">As a result, the backside of the sphere gets darker as the surface of the sphere curves away from the light.</span></span>

![使用擴散光源的球體圖例](images/lightd.jpg)

<span data-ttu-id="1ea0b-165">結合前一個範例的擴散光源與環境光源形成物體表面的整體色調。</span><span class="sxs-lookup"><span data-stu-id="1ea0b-165">Combining the diffuse lighting with the ambient lighting from the previous example shades the entire surface of the object.</span></span> <span data-ttu-id="1ea0b-166">環境光源形成整個表面的色調，擴散光源則幫助顯現物體的 3D 形狀，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="1ea0b-166">The ambient light shades the entire surface and the diffuse light helps reveal the object's 3D shape, as shown in the following illustration.</span></span>

![擴散光源與環境光源的球體圖例](images/lightad.jpg)

<span data-ttu-id="1ea0b-168">擴散光源比環境光源需要較多運算資源。</span><span class="sxs-lookup"><span data-stu-id="1ea0b-168">Diffuse lighting is more intensive to calculate than ambient lighting.</span></span> <span data-ttu-id="1ea0b-169">因為它取決於頂點直角和光線方向，因此您可以看到 3D 空間的物體幾何，它會產生比環境光源更真實的光源。</span><span class="sxs-lookup"><span data-stu-id="1ea0b-169">Because it depends on the vertex normals and light direction, you can see the objects geometry in 3D space, which produces a more realistic lighting than ambient lighting.</span></span> <span data-ttu-id="1ea0b-170">您可以使用反射強光達到更真實的外觀。</span><span class="sxs-lookup"><span data-stu-id="1ea0b-170">You can use specular highlights to achieve a more realistic look.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1ea0b-171">相關主題</span><span class="sxs-lookup"><span data-stu-id="1ea0b-171">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1ea0b-172">燈光數學</span><span class="sxs-lookup"><span data-stu-id="1ea0b-172">Mathematics of Lighting</span></span>](mathematics-of-lighting.md)
</dt> </dl>

 

 



