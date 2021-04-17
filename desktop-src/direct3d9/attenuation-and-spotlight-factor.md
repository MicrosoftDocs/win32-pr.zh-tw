---
description: 全域照明方程式的擴散和聚光燈型光源元件內含描述光衰減及焦點圓錐的字詞。 以下將說明這些字詞。
ms.assetid: 960b5fc2-3074-4e51-b3de-5ed370379b01
title: " (Direct3D 9) 的衰減和焦點因素"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 623bb3cb2b1c2a3ee9e0e5d9419ff71dd9a303b6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104569705"
---
# <a name="attenuation-and-spotlight-factor-direct3d-9"></a><span data-ttu-id="4da5b-104"> (Direct3D 9) 的衰減和焦點因素</span><span class="sxs-lookup"><span data-stu-id="4da5b-104">Attenuation and Spotlight Factor (Direct3D 9)</span></span>

<span data-ttu-id="4da5b-105">全域照明方程式的擴散和聚光燈型光源元件內含描述光衰減及焦點圓錐的字詞。</span><span class="sxs-lookup"><span data-stu-id="4da5b-105">The diffuse and specular lighting components of the global illumination equation contain terms that describe light attenuation and the spotlight cone.</span></span> <span data-ttu-id="4da5b-106">以下將說明這些字詞。</span><span class="sxs-lookup"><span data-stu-id="4da5b-106">These terms are described below.</span></span>

## <a name="attenuation"></a><span data-ttu-id="4da5b-107">衰減</span><span class="sxs-lookup"><span data-stu-id="4da5b-107">Attenuation</span></span>

<span data-ttu-id="4da5b-108">光線的衰減取決於光線的類型以及光線與頂點位置之間的距離。</span><span class="sxs-lookup"><span data-stu-id="4da5b-108">The attenuation of a light depends on the type of light and the distance between the light and the vertex position.</span></span> <span data-ttu-id="4da5b-109">若要計算衰減，請使用下列其中一個方程式。</span><span class="sxs-lookup"><span data-stu-id="4da5b-109">To calculate attenuation, use one of the following equations.</span></span>

<span data-ttu-id="4da5b-110">Atten = 1/ ( att0<sub>i</sub> + att1<sub>i</sub> \* d + att2<sub>i</sub> \* d ²) </span><span class="sxs-lookup"><span data-stu-id="4da5b-110">Atten = 1/( att0<sub>i</sub> + att1<sub>i</sub> \* d + att2<sub>i</sub> \* d²)</span></span>

<span data-ttu-id="4da5b-111">其中：</span><span class="sxs-lookup"><span data-stu-id="4da5b-111">Where:</span></span>



| <span data-ttu-id="4da5b-112">參數</span><span class="sxs-lookup"><span data-stu-id="4da5b-112">Parameter</span></span>        | <span data-ttu-id="4da5b-113">預設值</span><span class="sxs-lookup"><span data-stu-id="4da5b-113">Default value</span></span> | <span data-ttu-id="4da5b-114">類型</span><span class="sxs-lookup"><span data-stu-id="4da5b-114">Type</span></span>  | <span data-ttu-id="4da5b-115">描述</span><span class="sxs-lookup"><span data-stu-id="4da5b-115">Description</span></span>                                     | <span data-ttu-id="4da5b-116">範圍</span><span class="sxs-lookup"><span data-stu-id="4da5b-116">Range</span></span>          |
|------------------|---------------|-------|-------------------------------------------------|----------------|
| <span data-ttu-id="4da5b-117">att0<sub>i</sub></span><span class="sxs-lookup"><span data-stu-id="4da5b-117">att0<sub>i</sub></span></span> | <span data-ttu-id="4da5b-118">0.0</span><span class="sxs-lookup"><span data-stu-id="4da5b-118">0.0</span></span>           | <span data-ttu-id="4da5b-119">FLOAT</span><span class="sxs-lookup"><span data-stu-id="4da5b-119">FLOAT</span></span> | <span data-ttu-id="4da5b-120">定值衰減因數</span><span class="sxs-lookup"><span data-stu-id="4da5b-120">Constant attenuation factor</span></span>                     | <span data-ttu-id="4da5b-121">0 至 +infinity</span><span class="sxs-lookup"><span data-stu-id="4da5b-121">0 to +infinity</span></span> |
| <span data-ttu-id="4da5b-122">att1<sub>i</sub></span><span class="sxs-lookup"><span data-stu-id="4da5b-122">att1<sub>i</sub></span></span> | <span data-ttu-id="4da5b-123">0.0</span><span class="sxs-lookup"><span data-stu-id="4da5b-123">0.0</span></span>           | <span data-ttu-id="4da5b-124">FLOAT</span><span class="sxs-lookup"><span data-stu-id="4da5b-124">FLOAT</span></span> | <span data-ttu-id="4da5b-125">線性衰減因數</span><span class="sxs-lookup"><span data-stu-id="4da5b-125">Linear attenuation factor</span></span>                       | <span data-ttu-id="4da5b-126">0 至 +infinity</span><span class="sxs-lookup"><span data-stu-id="4da5b-126">0 to +infinity</span></span> |
| <span data-ttu-id="4da5b-127">att2<sub>i</sub></span><span class="sxs-lookup"><span data-stu-id="4da5b-127">att2<sub>i</sub></span></span> | <span data-ttu-id="4da5b-128">0.0</span><span class="sxs-lookup"><span data-stu-id="4da5b-128">0.0</span></span>           | <span data-ttu-id="4da5b-129">FLOAT</span><span class="sxs-lookup"><span data-stu-id="4da5b-129">FLOAT</span></span> | <span data-ttu-id="4da5b-130">二次方衰減因數</span><span class="sxs-lookup"><span data-stu-id="4da5b-130">Quadratic attenuation factor</span></span>                    | <span data-ttu-id="4da5b-131">0 至 +infinity</span><span class="sxs-lookup"><span data-stu-id="4da5b-131">0 to +infinity</span></span> |
| <span data-ttu-id="4da5b-132">d</span><span class="sxs-lookup"><span data-stu-id="4da5b-132">d</span></span>                | <span data-ttu-id="4da5b-133">N/A</span><span class="sxs-lookup"><span data-stu-id="4da5b-133">N/A</span></span>           | <span data-ttu-id="4da5b-134">FLOAT</span><span class="sxs-lookup"><span data-stu-id="4da5b-134">FLOAT</span></span> | <span data-ttu-id="4da5b-135">頂點位置至光源位置的距離</span><span class="sxs-lookup"><span data-stu-id="4da5b-135">Distance from vertex position to light position</span></span> | <span data-ttu-id="4da5b-136">N/A</span><span class="sxs-lookup"><span data-stu-id="4da5b-136">N/A</span></span>            |



 

-   <span data-ttu-id="4da5b-137">若光線為定向光線，則 Atten = 1。</span><span class="sxs-lookup"><span data-stu-id="4da5b-137">Atten = 1, if the light is a directional light.</span></span>
-   <span data-ttu-id="4da5b-138">若光線與頂點之間的距離超過光線範圍，則 Atten = 0。</span><span class="sxs-lookup"><span data-stu-id="4da5b-138">Atten = 0, if the distance between the light and the vertex exceeds the light's range.</span></span>

<span data-ttu-id="4da5b-139">Att0、att1、att2 值是由 [**Attenuation1**](d3dlight9.md)的 Attenuation0、Attenuation2 和 D3DLIGHT9 成員所指定。</span><span class="sxs-lookup"><span data-stu-id="4da5b-139">The att0, att1, att2 values are specified by the Attenuation0, Attenuation1, and Attenuation2 members of [**D3DLIGHT9**](d3dlight9.md).</span></span>

<span data-ttu-id="4da5b-140">光線與頂點位置之間的距離一律為正值。</span><span class="sxs-lookup"><span data-stu-id="4da5b-140">The distance between the light and the vertex position is always positive.</span></span>

<span data-ttu-id="4da5b-141">d = \| L<sub>dir</sub>\|</span><span class="sxs-lookup"><span data-stu-id="4da5b-141">d = \| L<sub>dir</sub> \|</span></span>

<span data-ttu-id="4da5b-142">其中：</span><span class="sxs-lookup"><span data-stu-id="4da5b-142">Where:</span></span>



| <span data-ttu-id="4da5b-143">參數</span><span class="sxs-lookup"><span data-stu-id="4da5b-143">Parameter</span></span>       | <span data-ttu-id="4da5b-144">預設值</span><span class="sxs-lookup"><span data-stu-id="4da5b-144">Default value</span></span> | <span data-ttu-id="4da5b-145">類型</span><span class="sxs-lookup"><span data-stu-id="4da5b-145">Type</span></span>      | <span data-ttu-id="4da5b-146">Description</span><span class="sxs-lookup"><span data-stu-id="4da5b-146">Description</span></span>                                                 |
|-----------------|---------------|-----------|-------------------------------------------------------------|
| <span data-ttu-id="4da5b-147">L<sub>dir</sub></span><span class="sxs-lookup"><span data-stu-id="4da5b-147">L<sub>dir</sub></span></span> | <span data-ttu-id="4da5b-148">N/A</span><span class="sxs-lookup"><span data-stu-id="4da5b-148">N/A</span></span>           | <span data-ttu-id="4da5b-149">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="4da5b-149">D3DVECTOR</span></span> | <span data-ttu-id="4da5b-150">從頂點位置至光線位置的方向向量</span><span class="sxs-lookup"><span data-stu-id="4da5b-150">Direction vector from vertex position to the light position</span></span> |



 

<span data-ttu-id="4da5b-151">如果 d 大於光的範圍，也就是 [**D3DLIGHT9**](d3dlight9.md) 結構的範圍成員，Direct3D 不會進行進一步的衰減計算，也不會對頂點套用任何效果。</span><span class="sxs-lookup"><span data-stu-id="4da5b-151">If d is greater than the light's range, that is, the Range member of a [**D3DLIGHT9**](d3dlight9.md) structure, Direct3D makes no further attenuation calculations and applies no effects from the light to the vertex.</span></span>

<span data-ttu-id="4da5b-152">衰減定值作為公式中的係數，您可對其進行簡單的調整來產生多種出現衰減曲線。</span><span class="sxs-lookup"><span data-stu-id="4da5b-152">The attenuation constants act as coefficients in the formula - you can produce a variety of attenuation curves by making simple adjustments to them.</span></span> <span data-ttu-id="4da5b-153">您可將 Attenuation1 設為 1.0，以建立不會衰減但仍受限於範圍的光線，或您可以嘗試使用不同的值，以取得各種衰減效果。</span><span class="sxs-lookup"><span data-stu-id="4da5b-153">You can set Attenuation1 to 1.0 to create a light that doesn't attenuate but is still limited by range, or you can experiment with different values to achieve various attenuation effects.</span></span>

<span data-ttu-id="4da5b-154">衰減的光線範圍上限不是 0.0。</span><span class="sxs-lookup"><span data-stu-id="4da5b-154">The attenuation at the maximum range of the light is not 0.0.</span></span> <span data-ttu-id="4da5b-155">若要防止光線在光線範圍時突然出現，應用程式可以增加光線範圍。</span><span class="sxs-lookup"><span data-stu-id="4da5b-155">To prevent lights from suddenly appearing when they are at the light range, an application can increase the light range.</span></span> <span data-ttu-id="4da5b-156">或者，應用程式可以設定衰減定值，使衰減因數的光線範圍接近 0.0。</span><span class="sxs-lookup"><span data-stu-id="4da5b-156">Or, the application can set up attenuation constants so that the attenuation factor is close to 0.0 at the light range.</span></span> <span data-ttu-id="4da5b-157">衰減值會乘以光線色彩的紅、綠及藍元件，以將光線的強度擴充作為光線傳輸至頂點之距離的因數。</span><span class="sxs-lookup"><span data-stu-id="4da5b-157">The attenuation value is multiplied by the red, green, and blue components of the light's color to scale the light's intensity as a factor of the distance light travels to a vertex.</span></span>

## <a name="spotlight-factor"></a><span data-ttu-id="4da5b-158">焦點因數</span><span class="sxs-lookup"><span data-stu-id="4da5b-158">Spotlight Factor</span></span>

<span data-ttu-id="4da5b-159">以下方程式指定焦點因數。</span><span class="sxs-lookup"><span data-stu-id="4da5b-159">The following equation specifies the spotlight factor.</span></span>

![焦點因數的方程式](images/dx8light9.png)



| <span data-ttu-id="4da5b-161">參數</span><span class="sxs-lookup"><span data-stu-id="4da5b-161">Parameter</span></span>         | <span data-ttu-id="4da5b-162">預設值</span><span class="sxs-lookup"><span data-stu-id="4da5b-162">Default value</span></span> | <span data-ttu-id="4da5b-163">類型</span><span class="sxs-lookup"><span data-stu-id="4da5b-163">Type</span></span>  | <span data-ttu-id="4da5b-164">描述</span><span class="sxs-lookup"><span data-stu-id="4da5b-164">Description</span></span>                              | <span data-ttu-id="4da5b-165">範圍</span><span class="sxs-lookup"><span data-stu-id="4da5b-165">Range</span></span>                    |
|-------------------|---------------|-------|------------------------------------------|--------------------------|
| <span data-ttu-id="4da5b-166">rho<sub>i</sub></span><span class="sxs-lookup"><span data-stu-id="4da5b-166">rho<sub>i</sub></span></span>   | <span data-ttu-id="4da5b-167">N/A</span><span class="sxs-lookup"><span data-stu-id="4da5b-167">N/A</span></span>           | <span data-ttu-id="4da5b-168">FLOAT</span><span class="sxs-lookup"><span data-stu-id="4da5b-168">FLOAT</span></span> | <span data-ttu-id="4da5b-169">spotlight i 的 cosine(angle)</span><span class="sxs-lookup"><span data-stu-id="4da5b-169">cosine(angle) for spotlight i</span></span>            | <span data-ttu-id="4da5b-170">N/A</span><span class="sxs-lookup"><span data-stu-id="4da5b-170">N/A</span></span>                      |
| <span data-ttu-id="4da5b-171">phi<sub>i</sub></span><span class="sxs-lookup"><span data-stu-id="4da5b-171">phi<sub>i</sub></span></span>   | <span data-ttu-id="4da5b-172">0.0</span><span class="sxs-lookup"><span data-stu-id="4da5b-172">0.0</span></span>           | <span data-ttu-id="4da5b-173">FLOAT</span><span class="sxs-lookup"><span data-stu-id="4da5b-173">FLOAT</span></span> | <span data-ttu-id="4da5b-174">焦點 i 在弧度的半影角度</span><span class="sxs-lookup"><span data-stu-id="4da5b-174">Penumbra angle of spotlight i in radians</span></span> | <span data-ttu-id="4da5b-175">\[theta<sub>i</sub>、pi) </span><span class="sxs-lookup"><span data-stu-id="4da5b-175">\[theta<sub>i</sub>, pi)</span></span> |
| <span data-ttu-id="4da5b-176">theta<sub>i</sub></span><span class="sxs-lookup"><span data-stu-id="4da5b-176">theta<sub>i</sub></span></span> | <span data-ttu-id="4da5b-177">0.0</span><span class="sxs-lookup"><span data-stu-id="4da5b-177">0.0</span></span>           | <span data-ttu-id="4da5b-178">FLOAT</span><span class="sxs-lookup"><span data-stu-id="4da5b-178">FLOAT</span></span> | <span data-ttu-id="4da5b-179">焦點 i 在弧度的本影角度</span><span class="sxs-lookup"><span data-stu-id="4da5b-179">Umbra angle of spotlight i in radians</span></span>    | <span data-ttu-id="4da5b-180">\[0、pi) </span><span class="sxs-lookup"><span data-stu-id="4da5b-180">\[0, pi)</span></span>                 |
| <span data-ttu-id="4da5b-181">falloff</span><span class="sxs-lookup"><span data-stu-id="4da5b-181">falloff</span></span>           | <span data-ttu-id="4da5b-182">0.0</span><span class="sxs-lookup"><span data-stu-id="4da5b-182">0.0</span></span>           | <span data-ttu-id="4da5b-183">FLOAT</span><span class="sxs-lookup"><span data-stu-id="4da5b-183">FLOAT</span></span> | <span data-ttu-id="4da5b-184">Falloff 因數</span><span class="sxs-lookup"><span data-stu-id="4da5b-184">Falloff factor</span></span>                           | <span data-ttu-id="4da5b-185">(-infinity, +infinity)</span><span class="sxs-lookup"><span data-stu-id="4da5b-185">(-infinity, +infinity)</span></span>   |



 

<span data-ttu-id="4da5b-186">其中：</span><span class="sxs-lookup"><span data-stu-id="4da5b-186">Where:</span></span>

<span data-ttu-id="4da5b-187">rho = norm(L<sub>dcs</sub>)<sup>.</sup>norm(L<sub>dir</sub>)</span><span class="sxs-lookup"><span data-stu-id="4da5b-187">rho = norm(L<sub>dcs</sub>)<sup>.</sup>norm(L<sub>dir</sub>)</span></span>

<span data-ttu-id="4da5b-188">以及：</span><span class="sxs-lookup"><span data-stu-id="4da5b-188">and:</span></span>



| <span data-ttu-id="4da5b-189">參數</span><span class="sxs-lookup"><span data-stu-id="4da5b-189">Parameter</span></span>       | <span data-ttu-id="4da5b-190">預設值</span><span class="sxs-lookup"><span data-stu-id="4da5b-190">Default value</span></span> | <span data-ttu-id="4da5b-191">類型</span><span class="sxs-lookup"><span data-stu-id="4da5b-191">Type</span></span>      | <span data-ttu-id="4da5b-192">Description</span><span class="sxs-lookup"><span data-stu-id="4da5b-192">Description</span></span>                                                 |
|-----------------|---------------|-----------|-------------------------------------------------------------|
| <span data-ttu-id="4da5b-193">L<sub>dc</sub></span><span class="sxs-lookup"><span data-stu-id="4da5b-193">L<sub>dcs</sub></span></span> | <span data-ttu-id="4da5b-194">N/A</span><span class="sxs-lookup"><span data-stu-id="4da5b-194">N/A</span></span>           | <span data-ttu-id="4da5b-195">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="4da5b-195">D3DVECTOR</span></span> | <span data-ttu-id="4da5b-196">相機空間光線方向的負值</span><span class="sxs-lookup"><span data-stu-id="4da5b-196">The negative of the light direction in camera space</span></span>         |
| <span data-ttu-id="4da5b-197">L<sub>dir</sub></span><span class="sxs-lookup"><span data-stu-id="4da5b-197">L<sub>dir</sub></span></span> | <span data-ttu-id="4da5b-198">N/A</span><span class="sxs-lookup"><span data-stu-id="4da5b-198">N/A</span></span>           | <span data-ttu-id="4da5b-199">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="4da5b-199">D3DVECTOR</span></span> | <span data-ttu-id="4da5b-200">從頂點位置至光線位置的方向向量</span><span class="sxs-lookup"><span data-stu-id="4da5b-200">Direction vector from vertex position to the light position</span></span> |



 

<span data-ttu-id="4da5b-201">在計算光線衰減之後，Direct3D 也會考慮焦點效果（如果適用的話）、光線從介面反映的角度，以及目前材質的反射率來計算該頂點的擴散和反射元件。</span><span class="sxs-lookup"><span data-stu-id="4da5b-201">After computing the light attenuation, Direct3D also considers spotlight effects if applicable, the angle that the light reflects from a surface, and the reflectance of the current material to calculate the diffuse and specular components for that vertex.</span></span> <span data-ttu-id="4da5b-202">如需詳細資訊，請參閱 [焦點](light-types.md)。</span><span class="sxs-lookup"><span data-stu-id="4da5b-202">For more information, see [SpotLight](light-types.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4da5b-203">相關主題</span><span class="sxs-lookup"><span data-stu-id="4da5b-203">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4da5b-204">燈光數學</span><span class="sxs-lookup"><span data-stu-id="4da5b-204">Mathematics of Lighting</span></span>](mathematics-of-lighting.md)
</dt> </dl>

 

 



