---
description: 模型反射反映需要系統不僅知道光線的移動方向，也需要查看檢視器的眼睛方向。
ms.assetid: 35da0ac3-4e68-4d37-a987-405fc15d0cbf
title: " (Direct3D 9) 的反射光源"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b16d71bd8d814e104cf8a90d1d1fe9b15ba10f3
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343673"
---
# <a name="specular-lighting-direct3d-9"></a><span data-ttu-id="e1c79-103"> (Direct3D 9) 的反射光源</span><span class="sxs-lookup"><span data-stu-id="e1c79-103">Specular Lighting (Direct3D 9)</span></span>

<span data-ttu-id="e1c79-104">模型反射反映需要系統不僅知道光線的移動方向，也需要查看檢視器的眼睛方向。</span><span class="sxs-lookup"><span data-stu-id="e1c79-104">Modeling specular reflection requires that the system not only know in what direction light is traveling, but also the direction to the viewer's eye.</span></span> <span data-ttu-id="e1c79-105">系統使用簡化 Phong 鏡面反射模型的版本，運用半程向量來近似計算鏡面反射的強度。</span><span class="sxs-lookup"><span data-stu-id="e1c79-105">The system uses a simplified version of the Phong specular-reflection model, which employs a halfway vector to approximate the intensity of specular reflection.</span></span>

<span data-ttu-id="e1c79-106">預設光源狀態不計算反射強光。</span><span class="sxs-lookup"><span data-stu-id="e1c79-106">The default lighting state does not calculate specular highlights.</span></span> <span data-ttu-id="e1c79-107">若要啟用反射光源，請務必將 D3DRS \_ SPECULARENABLE 設定為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="e1c79-107">To enable specular lighting, be sure to set D3DRS\_SPECULARENABLE to **TRUE**.</span></span>

## <a name="specular-lighting-equation"></a><span data-ttu-id="e1c79-108">反射光源方程式</span><span class="sxs-lookup"><span data-stu-id="e1c79-108">Specular Lighting Equation</span></span>

<span data-ttu-id="e1c79-109">反射光源的描述如下方程式：</span><span class="sxs-lookup"><span data-stu-id="e1c79-109">Specular Lighting is described by the following equation:</span></span>

<span data-ttu-id="e1c79-110">**反射光源 = Cs \* 總和 \[ Ls \* (N ·H) <sup>P</sup> \* Atten \* 位置\]**</span><span class="sxs-lookup"><span data-stu-id="e1c79-110">**Specular Lighting = Cₛ \* sum\[Lₛ \* (N · H)<sup>P</sup> \* Atten \* Spot\]**</span></span>



 

<span data-ttu-id="e1c79-111">下表識別變數、其類型，以及其範圍。</span><span class="sxs-lookup"><span data-stu-id="e1c79-111">The following table identifies the variables, their types, and their ranges.</span></span>



| <span data-ttu-id="e1c79-112">參數</span><span class="sxs-lookup"><span data-stu-id="e1c79-112">Parameter</span></span>    | <span data-ttu-id="e1c79-113">預設值</span><span class="sxs-lookup"><span data-stu-id="e1c79-113">Default value</span></span> | <span data-ttu-id="e1c79-114">類型</span><span class="sxs-lookup"><span data-stu-id="e1c79-114">Type</span></span>          | <span data-ttu-id="e1c79-115">Description</span><span class="sxs-lookup"><span data-stu-id="e1c79-115">Description</span></span>                                                                                                         |
|--------------|---------------|---------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1c79-116">Cₛ</span><span class="sxs-lookup"><span data-stu-id="e1c79-116">Cₛ</span></span>           | <span data-ttu-id="e1c79-117">(0,0,0,0)</span><span class="sxs-lookup"><span data-stu-id="e1c79-117">(0,0,0,0)</span></span>     | <span data-ttu-id="e1c79-118">D3DCOLORVALUE</span><span class="sxs-lookup"><span data-stu-id="e1c79-118">D3DCOLORVALUE</span></span> | <span data-ttu-id="e1c79-119">反射色彩。</span><span class="sxs-lookup"><span data-stu-id="e1c79-119">Specular color.</span></span>                                                                                                     |
| <span data-ttu-id="e1c79-120">Sum</span><span class="sxs-lookup"><span data-stu-id="e1c79-120">sum</span></span>          | <span data-ttu-id="e1c79-121">N/A</span><span class="sxs-lookup"><span data-stu-id="e1c79-121">N/A</span></span>           | <span data-ttu-id="e1c79-122">N/A</span><span class="sxs-lookup"><span data-stu-id="e1c79-122">N/A</span></span>           | <span data-ttu-id="e1c79-123">每道光的反射元件的總和。</span><span class="sxs-lookup"><span data-stu-id="e1c79-123">Summation of each light's specular component.</span></span>                                                                       |
| <span data-ttu-id="e1c79-124">N</span><span class="sxs-lookup"><span data-stu-id="e1c79-124">N</span></span>            | <span data-ttu-id="e1c79-125">N/A</span><span class="sxs-lookup"><span data-stu-id="e1c79-125">N/A</span></span>           | <span data-ttu-id="e1c79-126">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="e1c79-126">D3DVECTOR</span></span>     | <span data-ttu-id="e1c79-127">頂點標準。</span><span class="sxs-lookup"><span data-stu-id="e1c79-127">Vertex normal.</span></span>                                                                                                      |
| <span data-ttu-id="e1c79-128">H</span><span class="sxs-lookup"><span data-stu-id="e1c79-128">H</span></span>            | <span data-ttu-id="e1c79-129">N/A</span><span class="sxs-lookup"><span data-stu-id="e1c79-129">N/A</span></span>           | <span data-ttu-id="e1c79-130">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="e1c79-130">D3DVECTOR</span></span>     | <span data-ttu-id="e1c79-131">半程向量。</span><span class="sxs-lookup"><span data-stu-id="e1c79-131">Half way vector.</span></span> <span data-ttu-id="e1c79-132">請參閱有關半程向量的一節。</span><span class="sxs-lookup"><span data-stu-id="e1c79-132">See the section on the halfway vector.</span></span>                                                             |
| <span data-ttu-id="e1c79-133"><sup>P</sup></span><span class="sxs-lookup"><span data-stu-id="e1c79-133"><sup>P</sup></span></span> | <span data-ttu-id="e1c79-134">0.0</span><span class="sxs-lookup"><span data-stu-id="e1c79-134">0.0</span></span>           | <span data-ttu-id="e1c79-135">FLOAT</span><span class="sxs-lookup"><span data-stu-id="e1c79-135">FLOAT</span></span>         | <span data-ttu-id="e1c79-136">鏡面反射力。</span><span class="sxs-lookup"><span data-stu-id="e1c79-136">Specular reflection power.</span></span> <span data-ttu-id="e1c79-137">範圍是 0 到 + 無限大</span><span class="sxs-lookup"><span data-stu-id="e1c79-137">Range is 0 to +infinity</span></span>                                                                  |
| <span data-ttu-id="e1c79-138">Lₛ</span><span class="sxs-lookup"><span data-stu-id="e1c79-138">Lₛ</span></span>           | <span data-ttu-id="e1c79-139">(0,0,0,0)</span><span class="sxs-lookup"><span data-stu-id="e1c79-139">(0,0,0,0)</span></span>     | <span data-ttu-id="e1c79-140">D3DCOLORVALUE</span><span class="sxs-lookup"><span data-stu-id="e1c79-140">D3DCOLORVALUE</span></span> | <span data-ttu-id="e1c79-141">淺色反射。</span><span class="sxs-lookup"><span data-stu-id="e1c79-141">Light specular color.</span></span>                                                                                               |
| <span data-ttu-id="e1c79-142">Atten</span><span class="sxs-lookup"><span data-stu-id="e1c79-142">Atten</span></span>        | <span data-ttu-id="e1c79-143">N/A</span><span class="sxs-lookup"><span data-stu-id="e1c79-143">N/A</span></span>           | <span data-ttu-id="e1c79-144">FLOAT</span><span class="sxs-lookup"><span data-stu-id="e1c79-144">FLOAT</span></span>         | <span data-ttu-id="e1c79-145">光衰減值。</span><span class="sxs-lookup"><span data-stu-id="e1c79-145">Light attenuation value.</span></span> <span data-ttu-id="e1c79-146">請參閱 [ (Direct3D 9) 的衰減和焦點因素 ](attenuation-and-spotlight-factor.md)。</span><span class="sxs-lookup"><span data-stu-id="e1c79-146">See [Attenuation and Spotlight Factor (Direct3D 9)](attenuation-and-spotlight-factor.md).</span></span> |
| <span data-ttu-id="e1c79-147">付現</span><span class="sxs-lookup"><span data-stu-id="e1c79-147">Spot</span></span>         | <span data-ttu-id="e1c79-148">N/A</span><span class="sxs-lookup"><span data-stu-id="e1c79-148">N/A</span></span>           | <span data-ttu-id="e1c79-149">FLOAT</span><span class="sxs-lookup"><span data-stu-id="e1c79-149">FLOAT</span></span>         | <span data-ttu-id="e1c79-150">聚光燈係數。</span><span class="sxs-lookup"><span data-stu-id="e1c79-150">Spotlight factor.</span></span> <span data-ttu-id="e1c79-151">請參閱 [ (Direct3D 9) 的衰減和焦點因素 ](attenuation-and-spotlight-factor.md)。</span><span class="sxs-lookup"><span data-stu-id="e1c79-151">See [Attenuation and Spotlight Factor (Direct3D 9)](attenuation-and-spotlight-factor.md).</span></span>        |



 

<span data-ttu-id="e1c79-152">Cₛ 的值為：</span><span class="sxs-lookup"><span data-stu-id="e1c79-152">The value for Cₛ is either:</span></span>


```
if(SPECULARMATERIALSOURCE == D3DMCS_COLOR1)
  C = color1;
```



-   <span data-ttu-id="e1c79-153">頂點 color1，如果反射材質來源為 D3DMCS \_ color1，且頂點宣告中提供第一個頂點色彩。</span><span class="sxs-lookup"><span data-stu-id="e1c79-153">vertex color1, if the specular material source is D3DMCS\_COLOR1, and the first vertex color is supplied in the vertex declaration.</span></span>
-   <span data-ttu-id="e1c79-154">頂點 color2，如果反射材質來源為 D3DMCS \_ color2，且頂點宣告中提供第二個頂點色彩。</span><span class="sxs-lookup"><span data-stu-id="e1c79-154">vertex color2, if specular material source is D3DMCS\_COLOR2, and the second vertex color is supplied in the vertex declaration.</span></span>
-   <span data-ttu-id="e1c79-155">材料反射色彩</span><span class="sxs-lookup"><span data-stu-id="e1c79-155">material specular color</span></span>

> [!Note]  
> <span data-ttu-id="e1c79-156">如果使用任一種 [反射材質來源] 選項，而且未提供頂點色彩，則會使用材質反射色彩。</span><span class="sxs-lookup"><span data-stu-id="e1c79-156">If either specular material source option is used and the vertex color is not provided, then the material specular color is used.</span></span>

 

<span data-ttu-id="e1c79-157">所有的光分開處理和插補之後，反射元件會鉗制為從 0 到 255。</span><span class="sxs-lookup"><span data-stu-id="e1c79-157">Specular components are clamped to be from 0 to 255, after all lights are processed and interpolated separately.</span></span>

## <a name="the-halfway-vector"></a><span data-ttu-id="e1c79-158">半程向量</span><span class="sxs-lookup"><span data-stu-id="e1c79-158">The Halfway Vector</span></span>

<span data-ttu-id="e1c79-159">半程向量 (H) 存在於兩個向量之間路程的一半：從物件頂點到光源的向量，以及從物件頂點到相機位置的向量。</span><span class="sxs-lookup"><span data-stu-id="e1c79-159">The halfway vector (H) exists midway between two vectors: the vector from an object vertex to the light source, and the vector from an object vertex to the camera position.</span></span> <span data-ttu-id="e1c79-160">Direct3D 提供兩種方式來計算半程向量。</span><span class="sxs-lookup"><span data-stu-id="e1c79-160">Direct3D provides two ways to compute the halfway vector.</span></span> <span data-ttu-id="e1c79-161">當 D3DRS \_ LOCALVIEWER 設定為 **TRUE** 時，系統會使用相機的位置和頂點的位置，以及光線的方向向量來計算中間向量。</span><span class="sxs-lookup"><span data-stu-id="e1c79-161">When D3DRS\_LOCALVIEWER is set to **TRUE**, the system calculates the halfway vector using the position of the camera and the position of the vertex, along with the light's direction vector.</span></span> <span data-ttu-id="e1c79-162">下列公式說明這點。</span><span class="sxs-lookup"><span data-stu-id="e1c79-162">The following formula illustrates this.</span></span>

<span data-ttu-id="e1c79-163">**H = 標準 (標準 (Cp-Vp) + L <sub>dir</sub>)**</span><span class="sxs-lookup"><span data-stu-id="e1c79-163">**H = norm(norm(Cₚ - Vₚ) + L<sub>dir</sub>)**</span></span>



 



| <span data-ttu-id="e1c79-164">參數</span><span class="sxs-lookup"><span data-stu-id="e1c79-164">Parameter</span></span>       | <span data-ttu-id="e1c79-165">預設值</span><span class="sxs-lookup"><span data-stu-id="e1c79-165">Default value</span></span> | <span data-ttu-id="e1c79-166">類型</span><span class="sxs-lookup"><span data-stu-id="e1c79-166">Type</span></span>      | <span data-ttu-id="e1c79-167">Description</span><span class="sxs-lookup"><span data-stu-id="e1c79-167">Description</span></span>                                                  |
|-----------------|---------------|-----------|--------------------------------------------------------------|
| <span data-ttu-id="e1c79-168">Cₚ</span><span class="sxs-lookup"><span data-stu-id="e1c79-168">Cₚ</span></span>              | <span data-ttu-id="e1c79-169">N/A</span><span class="sxs-lookup"><span data-stu-id="e1c79-169">N/A</span></span>           | <span data-ttu-id="e1c79-170">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="e1c79-170">D3DVECTOR</span></span> | <span data-ttu-id="e1c79-171">相機位置。</span><span class="sxs-lookup"><span data-stu-id="e1c79-171">Camera position.</span></span>                                             |
| <span data-ttu-id="e1c79-172">Vₚ</span><span class="sxs-lookup"><span data-stu-id="e1c79-172">Vₚ</span></span>              | <span data-ttu-id="e1c79-173">N/A</span><span class="sxs-lookup"><span data-stu-id="e1c79-173">N/A</span></span>           | <span data-ttu-id="e1c79-174">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="e1c79-174">D3DVECTOR</span></span> | <span data-ttu-id="e1c79-175">頂點位置。</span><span class="sxs-lookup"><span data-stu-id="e1c79-175">Vertex position.</span></span>                                             |
| <span data-ttu-id="e1c79-176">L<sub>dir</sub></span><span class="sxs-lookup"><span data-stu-id="e1c79-176">L<sub>dir</sub></span></span> | <span data-ttu-id="e1c79-177">N/A</span><span class="sxs-lookup"><span data-stu-id="e1c79-177">N/A</span></span>           | <span data-ttu-id="e1c79-178">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="e1c79-178">D3DVECTOR</span></span> | <span data-ttu-id="e1c79-179">從頂點位置至光線位置的方向向量。</span><span class="sxs-lookup"><span data-stu-id="e1c79-179">Direction vector from vertex position to the light position.</span></span> |



 

<span data-ttu-id="e1c79-180">以這種方式判斷半程向量可能會需要大量運算資源。</span><span class="sxs-lookup"><span data-stu-id="e1c79-180">Determining the halfway vector in this manner can be computationally intensive.</span></span> <span data-ttu-id="e1c79-181">另一種方式是設定 D3DRS \_ LOCALVIEWER = **FALSE** ，指示系統在 Z 軸上有無限遠的角度時，採取行動。</span><span class="sxs-lookup"><span data-stu-id="e1c79-181">As an alternative, setting D3DRS\_LOCALVIEWER = **FALSE** instructs the system to act as though the viewpoint is infinitely distant on the z-axis.</span></span> <span data-ttu-id="e1c79-182">其計算公式如下。</span><span class="sxs-lookup"><span data-stu-id="e1c79-182">This is reflected in the following formula.</span></span>

<span data-ttu-id="e1c79-183">**H = 標準 ( (0、0、1) + L <sub>dir</sub>)**</span><span class="sxs-lookup"><span data-stu-id="e1c79-183">**H = norm((0,0,1) + L<sub>dir</sub>)**</span></span>



 

<span data-ttu-id="e1c79-184">此設定比較不需要大量運算資源，但比較不精確，因此最適合供使用正交投影的應用程式使用。</span><span class="sxs-lookup"><span data-stu-id="e1c79-184">This setting is less computationally intensive, but much less accurate, so it is best used by applications that use orthogonal projection.</span></span>

## <a name="example"></a><span data-ttu-id="e1c79-185">範例</span><span class="sxs-lookup"><span data-stu-id="e1c79-185">Example</span></span>

<span data-ttu-id="e1c79-186">在這個範例，物件使用場景反射淺色和材料反射色彩來著色。</span><span class="sxs-lookup"><span data-stu-id="e1c79-186">In this example, the object is colored using the scene specular light color and a material specular color.</span></span> <span data-ttu-id="e1c79-187">程式碼如下所示。</span><span class="sxs-lookup"><span data-stu-id="e1c79-187">The code is shown below.</span></span>


```
D3DMATERIAL9 mtrl;
ZeroMemory( &mtrl, sizeof(mtrl) );

D3DLIGHT9 light;
ZeroMemory( &light, sizeof(light) );
light.Type = D3DLIGHT_DIRECTIONAL;

D3DXVECTOR3 vecDir;
vecDir = D3DXVECTOR3(0.5f, 0.0f, -0.5f);
D3DXVec3Normalize( (D3DXVECTOR3*)&light.Direction, &vecDir );

light.Specular.r = 1.0f;
light.Specular.g = 1.0f;
light.Specular.b = 1.0f;
light.Specular.a = 1.0f;

light.Range = 1000;
light.Falloff = 0;
light.Attenuation0 = 1;
light.Attenuation1 = 0;
light.Attenuation2 = 0;
m_pd3dDevice->SetLight( 0, &light );
m_pd3dDevice->LightEnable( 0, TRUE );
m_pd3dDevice->SetRenderState( D3DRS_SPECULARENABLE, TRUE );

mtrl.Specular.r = 0.5f;
mtrl.Specular.g = 0.5f;
mtrl.Specular.b = 0.5f;
mtrl.Specular.a = 0.5f;
mtrl.Power = 20;
m_pd3dDevice->SetMaterial( &mtrl );
m_pd3dDevice->SetRenderState(D3DRS_SPECULARMATERIALSOURCE, D3DMCS_MATERIAL);
```



<span data-ttu-id="e1c79-188">根據方程式，為物件端點產生的色彩是材質色彩和淺色的組合。</span><span class="sxs-lookup"><span data-stu-id="e1c79-188">According to the equation, the resulting color for the object vertices is a combination of the material color and the light color.</span></span>

<span data-ttu-id="e1c79-189">下列兩圖顯示反射材料色彩 (灰色)，以及反射淺色 (白色)。</span><span class="sxs-lookup"><span data-stu-id="e1c79-189">The following two illustration show the specular material color, which is gray, and the specular light color, which is white.</span></span>

![灰球體圖例](images/amb1.jpg)![白色球體的圖例](images/lightwhite.jpg)

<span data-ttu-id="e1c79-192">下圖顯示結果反射強光。</span><span class="sxs-lookup"><span data-stu-id="e1c79-192">The resulting specular highlight is shown in the following illustration.</span></span>

![反射強光的圖例](images/lights.jpg)

<span data-ttu-id="e1c79-194">結合反射強光與周遭環境和擴散光源會產生下圖。</span><span class="sxs-lookup"><span data-stu-id="e1c79-194">Combining the specular highlight with the ambient and diffuse lighting produces the following illustration.</span></span> <span data-ttu-id="e1c79-195">在套用所有三種光源類型時，這更加清楚地類似寫實物件。</span><span class="sxs-lookup"><span data-stu-id="e1c79-195">With all three types of lighting applied, this more clearly resembles a realistic object.</span></span>

![結合反射強光、周遭環境光源和擴散光源的圖例](images/lightads.jpg)

<span data-ttu-id="e1c79-197">反射光源比擴散光源需要較多運算資源。</span><span class="sxs-lookup"><span data-stu-id="e1c79-197">Specular lighting is more intensive to calculate than diffuse lighting.</span></span> <span data-ttu-id="e1c79-198">這通常用來提供表面材料的視覺線索。</span><span class="sxs-lookup"><span data-stu-id="e1c79-198">It is typically used to provide visual clues about the surface material.</span></span> <span data-ttu-id="e1c79-199">根據表面材料，反射強光在大小和色彩上不同。</span><span class="sxs-lookup"><span data-stu-id="e1c79-199">The specular highlight varies in size and color with the material of the surface.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e1c79-200">相關主題</span><span class="sxs-lookup"><span data-stu-id="e1c79-200">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e1c79-201">燈光數學</span><span class="sxs-lookup"><span data-stu-id="e1c79-201">Mathematics of Lighting</span></span>](mathematics-of-lighting.md)
</dt> </dl>

 

 



