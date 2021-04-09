---
title: 點狀反射光源效果
description: 使用點反射光源效果，建立看似反射表面的影像。
ms.assetid: 89E22FD0-BB7F-465F-A79C-056CA9F14F5D
keywords:
- 點反射光源效果
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 355c573888604af8dfac443f4f53554a8a780071
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934693"
---
# <a name="point-specular-lighting-effect"></a><span data-ttu-id="552f1-104">點狀反射光源效果</span><span class="sxs-lookup"><span data-stu-id="552f1-104">Point-specular lighting effect</span></span>

<span data-ttu-id="552f1-105">使用點反射光源效果，建立看似反射表面的影像。</span><span class="sxs-lookup"><span data-stu-id="552f1-105">Use the point-specular lighting effect to create an image that appears to be a reflective surface.</span></span> <span data-ttu-id="552f1-106">效果會使用影像的 Alpha 色板作為高度地圖和您放置的點光源，並根據 Phong 光源模型的反射部分計算反映和淺色。</span><span class="sxs-lookup"><span data-stu-id="552f1-106">The effect uses the alpha channel of the image as a height map and a point light source that you position, and calculates the reflection and light according to the specular portion of the Phong lighting model.</span></span>

<span data-ttu-id="552f1-107">輸出點陣圖的色彩是淺色、光線位置和表面幾何的結果。</span><span class="sxs-lookup"><span data-stu-id="552f1-107">The color of the output bitmap is a result of light color, light position, and the surface geometry.</span></span> <span data-ttu-id="552f1-108">每個圖元的 Alpha 通道輸出（具有反射光源）是該圖元的紅色、綠色和藍色通道輸出的最大值。</span><span class="sxs-lookup"><span data-stu-id="552f1-108">The alpha channel output for each pixel with specular lighting is the maximum of the red, green, and blue channel outputs for that pixel.</span></span>

<span data-ttu-id="552f1-109">這項效果的 CLSID 是 CLSID \_ D2D1PointSpecular。</span><span class="sxs-lookup"><span data-stu-id="552f1-109">The CLSID for this effect is CLSID\_D2D1PointSpecular.</span></span>

-   [<span data-ttu-id="552f1-110">範例影像</span><span class="sxs-lookup"><span data-stu-id="552f1-110">Example image</span></span>](#example-image)
-   [<span data-ttu-id="552f1-111">點燈來源</span><span class="sxs-lookup"><span data-stu-id="552f1-111">Point light source</span></span>](#point-light-source)
-   [<span data-ttu-id="552f1-112">高度地圖和一般向量</span><span class="sxs-lookup"><span data-stu-id="552f1-112">Height map and normal vector</span></span>](#height-map-and-normal-vector)
-   [<span data-ttu-id="552f1-113">反射光源常數和指數</span><span class="sxs-lookup"><span data-stu-id="552f1-113">Specular lighting constant and exponent</span></span>](#specular-lighting-constant-and-exponent)
-   [<span data-ttu-id="552f1-114">效果屬性</span><span class="sxs-lookup"><span data-stu-id="552f1-114">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="552f1-115">縮放模式</span><span class="sxs-lookup"><span data-stu-id="552f1-115">Scales modes</span></span>](#scales-modes)
-   [<span data-ttu-id="552f1-116">需求</span><span class="sxs-lookup"><span data-stu-id="552f1-116">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="552f1-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="552f1-117">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="552f1-118">範例影像</span><span class="sxs-lookup"><span data-stu-id="552f1-118">Example image</span></span>

<span data-ttu-id="552f1-119">此處的範例會顯示點反射光源效果的輸入和輸出影像。</span><span class="sxs-lookup"><span data-stu-id="552f1-119">The example here shows the input and output images of the point-specular lighting effect.</span></span>

![顯示點反射光源效果之輸入和輸出影像的效果範例螢幕擷取畫面。](images/point-spec-example.png)

<span data-ttu-id="552f1-121">反射光源指的是根據 Phong 光源模型反映在特定方向的燈光。</span><span class="sxs-lookup"><span data-stu-id="552f1-121">Specular light refers to light that is reflected in a specific direction according to the Phong lighting model.</span></span>

![用來 cacluate 點陣圖反射光源輸出的向量圖。](images/point-spec-reflected1.png)

<span data-ttu-id="552f1-123">效果會使用以下的方公式來計算最終輸出圖元值：</span><span class="sxs-lookup"><span data-stu-id="552f1-123">The effect calculates the final output pixel values using the equations here:</span></span>

![<span data-ttu-id="552f1-124">用於計算最終圖元值的方程式。</span><span class="sxs-lookup"><span data-stu-id="552f1-124">the equations for calculating the final pixel values.</span></span> ](images/point-spec-formula-output.png)

<span data-ttu-id="552f1-125">其中</span><span class="sxs-lookup"><span data-stu-id="552f1-125">where</span></span><dl> <span data-ttu-id="552f1-126">K？</span><span class="sxs-lookup"><span data-stu-id="552f1-126">k?</span></span> <span data-ttu-id="552f1-127">= 反射光源常數。</span><span class="sxs-lookup"><span data-stu-id="552f1-127">= specular lighting constant.</span></span>  
<span data-ttu-id="552f1-128">![表面標準單元向量符號。 ](images/point-spec-mathchar-n.png)= surface 一般單位向量，也就是 x 和 y 的函式。</span><span class="sxs-lookup"><span data-stu-id="552f1-128">![the surface normal unit vector symbol.](images/point-spec-mathchar-n.png)= surface normal unit vector which is a function of x and y.</span></span> <span data-ttu-id="552f1-129">請參閱計算的 [高度地圖和一般向量](#height-map-and-normal-vector) 。</span><span class="sxs-lookup"><span data-stu-id="552f1-129">See [Height map and normal vector](#height-map-and-normal-vector) for the calculations.</span></span>  
<span data-ttu-id="552f1-130">![中間的單位向量符號。 ](images/point-spec-mathchar-h.png)= 紅眼單位向量和淺色單位向量之間的「半」單位向量。</span><span class="sxs-lookup"><span data-stu-id="552f1-130">![the halfway unit vector symbol.](images/point-spec-mathchar-h.png)= "halfway" unit vector between eye unit vector and light unit vector.</span></span> <span data-ttu-id="552f1-131">請參閱計算的 [Point light 來源](#point-light-source) 。</span><span class="sxs-lookup"><span data-stu-id="552f1-131">See [Point light source](#point-light-source) for the calculations.</span></span>  
<span data-ttu-id="552f1-132">L<sub>r</sub>、l<sub>g</sub>、l<sub>b</sub> = RGB 元件中的淺色。</span><span class="sxs-lookup"><span data-stu-id="552f1-132">L<sub>r</sub>, L<sub>g</sub>, L<sub>b</sub> = the light color in RGB components.</span></span>  
</dl>

<span data-ttu-id="552f1-133">您將反射光源常數設定為 [ *SpecularConstant* ] 屬性，並將 [淺色] 色彩設定為 [ *色彩* ] 屬性。</span><span class="sxs-lookup"><span data-stu-id="552f1-133">You set the specular lighting constant as the *SpecularConstant* property and the light color as the *Color* property.</span></span>

## <a name="point-light-source"></a><span data-ttu-id="552f1-134">點燈來源</span><span class="sxs-lookup"><span data-stu-id="552f1-134">Point light source</span></span>

<span data-ttu-id="552f1-135">點燈光來源會以所有方向發出燈光，例如影像中的影像。</span><span class="sxs-lookup"><span data-stu-id="552f1-135">A point light source emits light in all directions like in the image here.</span></span>

![點燈會以所有方向發出燈光。](images/point-spec-light.png)

<span data-ttu-id="552f1-137">您可以使用 *LightPosition* 屬性設定光源來源的位置。</span><span class="sxs-lookup"><span data-stu-id="552f1-137">You set the position of the light source using the *LightPosition* property.</span></span> <span data-ttu-id="552f1-138">效果會使用此處的方程式，計算點光源的燈光向量 L：</span><span class="sxs-lookup"><span data-stu-id="552f1-138">The effect calculates the light vector, L   , for a point light source using the equations here:</span></span>

![淺向量方程式。](images/point-spec-formula3.png)

<span data-ttu-id="552f1-140">光在哪裡？、Light<sub>y</sub>和淺色<sub>z</sub> 是輸入光線位置。</span><span class="sxs-lookup"><span data-stu-id="552f1-140">where Light?, Light<sub>y</sub>, and Light<sub>z</sub> are the input light position.</span></span> <span data-ttu-id="552f1-141">效果會計算中間向量的中向量 ![ 符號。](images/point-spec-mathchar-h.png)</span><span class="sxs-lookup"><span data-stu-id="552f1-141">The effect calculates the halfway vector, ![halfway vector symbol.](images/point-spec-mathchar-h.png)</span></span> <span data-ttu-id="552f1-142">如 Phong 光源模型中所定義，在這裡使用方程式。</span><span class="sxs-lookup"><span data-stu-id="552f1-142">as defined in the Phong lighting model, using the equation here.</span></span> <span data-ttu-id="552f1-143">光源模型假設眼睛向量（ ![ 眼睛向量符號 ](images/point-spec-mathchar-e.png) ）位於 (0、0、1) 。</span><span class="sxs-lookup"><span data-stu-id="552f1-143">The lighting model assumes that the eye vector, ![the eye vector symbol](images/point-spec-mathchar-e.png), is located at (0,0,1).</span></span>

![中間向量方程式。](images/point-spec-formula4.png)

<span data-ttu-id="552f1-145">L 和 H 都會正規化為單位長度向量。</span><span class="sxs-lookup"><span data-stu-id="552f1-145">Both L and H are normalized to unit-length vectors.</span></span>

## <a name="height-map-and-normal-vector"></a><span data-ttu-id="552f1-146">高度地圖和一般向量</span><span class="sxs-lookup"><span data-stu-id="552f1-146">Height map and normal vector</span></span>

<span data-ttu-id="552f1-147">效果會根據其 Alpha 色板產生輸入影像的高度地圖。</span><span class="sxs-lookup"><span data-stu-id="552f1-147">The effect generates a height map for the input image based on its alpha channel.</span></span>

<span data-ttu-id="552f1-148">高度 (Z) 元件會使用方程式來計算：</span><span class="sxs-lookup"><span data-stu-id="552f1-148">The height (Z) component is calculated using the equation:</span></span>

![用來計算介面高度 (z) 的方程式。](images/point-spec-formula6.png)

<span data-ttu-id="552f1-150">效果會計算 surface normal，</span><span class="sxs-lookup"><span data-stu-id="552f1-150">The effect calculates the surface normal,</span></span> ![一般向量符號。](images/point-spec-mathchar-n.png)<span data-ttu-id="552f1-152">，適用于使用 Sobel 漸層的輸入點陣圖。</span><span class="sxs-lookup"><span data-stu-id="552f1-152">, for the input bitmap using a Sobel gradient.</span></span>

## <a name="specular-lighting-constant-and-exponent"></a><span data-ttu-id="552f1-153">反射光源常數和指數</span><span class="sxs-lookup"><span data-stu-id="552f1-153">Specular lighting constant and exponent</span></span>

<span data-ttu-id="552f1-154">反射光線代表從影像高度地圖的表面反映出來的光線。</span><span class="sxs-lookup"><span data-stu-id="552f1-154">Specular light represents the light that is reflected from the surface of the of the image height map.</span></span> <span data-ttu-id="552f1-155">您可以指定 *SpecularExponent* 屬性，以判斷來自點陣圖的反射反映數量。</span><span class="sxs-lookup"><span data-stu-id="552f1-155">You specify the *SpecularExponent* property that determines the amount of specular reflection from the bitmap.</span></span>

<span data-ttu-id="552f1-156">較大的指數代表 shinier 物件，並以更具焦點的形狀來反映淺色。</span><span class="sxs-lookup"><span data-stu-id="552f1-156">Larger exponents represent shinier objects and reflect light in a more focused shape.</span></span>

<span data-ttu-id="552f1-157">*SpecularConstant* 屬性 K？將反映的燈光數量定義為連入燈光的比率。</span><span class="sxs-lookup"><span data-stu-id="552f1-157">The *SpecularConstant* property K? defines the amount of reflected light as a ratio of the incoming light.</span></span>

## <a name="effect-properties"></a><span data-ttu-id="552f1-158">效果屬性</span><span class="sxs-lookup"><span data-stu-id="552f1-158">Effect properties</span></span>



| <span data-ttu-id="552f1-159">顯示名稱和索引列舉</span><span class="sxs-lookup"><span data-stu-id="552f1-159">Display name and index enumeration</span></span>                                                     | <span data-ttu-id="552f1-160">Description</span><span class="sxs-lookup"><span data-stu-id="552f1-160">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="552f1-161">LightPosition</span><span class="sxs-lookup"><span data-stu-id="552f1-161">LightPosition</span></span><br/> <span data-ttu-id="552f1-162">D2D1 \_ POINTSPECULAR \_ 的 \_ 照明 \_ 位置</span><span class="sxs-lookup"><span data-stu-id="552f1-162">D2D1\_POINTSPECULAR\_PROP\_LIGHT\_POSITION</span></span><br/>         | <span data-ttu-id="552f1-163">點燈來源的光線位置。</span><span class="sxs-lookup"><span data-stu-id="552f1-163">The light position of the point light source.</span></span> <span data-ttu-id="552f1-164">屬性是 \_ \_ 定義為 (x、y、z) 的 D2D1 向量3F。</span><span class="sxs-lookup"><span data-stu-id="552f1-164">The property is a D2D1\_VECTOR\_3F defined as (x, y, z).</span></span> <span data-ttu-id="552f1-165">單位是以與裝置無關的圖元為單位， (Dip) 且值沒有單位或未系結。</span><span class="sxs-lookup"><span data-stu-id="552f1-165">The units are in device-independent pixels (DIPs) and the values are unitless and unbounded.</span></span> <span data-ttu-id="552f1-166">此類型為 D2D1 \_ VECTOR \_ 3F。</span><span class="sxs-lookup"><span data-stu-id="552f1-166">The type is D2D1\_VECTOR\_3F.</span></span><br/> <span data-ttu-id="552f1-167">預設值為 {0.0 f、0.0 f、0.0 f}。</span><span class="sxs-lookup"><span data-stu-id="552f1-167">The default value is {0.0f, 0.0f, 0.0f}.</span></span><br/>                                                                                                                                                                                      |
| <span data-ttu-id="552f1-168">SpecularExponent</span><span class="sxs-lookup"><span data-stu-id="552f1-168">SpecularExponent</span></span><br/> <span data-ttu-id="552f1-169">D2D1 \_ POINTSPECULAR 的 \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="552f1-169">D2D1\_POINTSPECULAR\_PROP\_SPECULAR\_EXPONENT</span></span><br/>   | <span data-ttu-id="552f1-170">Phong 光源方程式中反射詞彙的指數。</span><span class="sxs-lookup"><span data-stu-id="552f1-170">The exponent for the specular term in the Phong lighting equation.</span></span> <span data-ttu-id="552f1-171">較大的值會對應至更反射的介面。</span><span class="sxs-lookup"><span data-stu-id="552f1-171">A larger value corresponds to a more reflective surface.</span></span> <span data-ttu-id="552f1-172">此值沒有單位，而且必須介於1.0 到128之間。</span><span class="sxs-lookup"><span data-stu-id="552f1-172">This value is unitless and must be between 1.0 and 128.</span></span> <span data-ttu-id="552f1-173">此類型為 FLOAT。</span><span class="sxs-lookup"><span data-stu-id="552f1-173">The type is FLOAT.</span></span><br/> <span data-ttu-id="552f1-174">預設值為 1.0 f。</span><span class="sxs-lookup"><span data-stu-id="552f1-174">The default value is 1.0f.</span></span><br/>                                                                                                                                                                                                                               |
| <span data-ttu-id="552f1-175">SpecularConstant</span><span class="sxs-lookup"><span data-stu-id="552f1-175">SpecularConstant</span></span><br/> <span data-ttu-id="552f1-176">D2D1 \_ POINTSPECULAR \_ 的 \_ 反射 \_ 常數</span><span class="sxs-lookup"><span data-stu-id="552f1-176">D2D1\_POINTSPECULAR\_PROP\_SPECULAR\_CONSTANT</span></span><br/>   | <span data-ttu-id="552f1-177">反射反映與連入燈光的比率。</span><span class="sxs-lookup"><span data-stu-id="552f1-177">The ratio of specular reflection to the incoming light.</span></span> <span data-ttu-id="552f1-178">值沒有單位，而且必須介於0到10000之間。</span><span class="sxs-lookup"><span data-stu-id="552f1-178">The value is unitless and must be between 0 and 10,000.</span></span> <span data-ttu-id="552f1-179">此類型為 FLOAT。</span><span class="sxs-lookup"><span data-stu-id="552f1-179">The type is FLOAT.</span></span><br/> <span data-ttu-id="552f1-180">預設值為 1.0 f。</span><span class="sxs-lookup"><span data-stu-id="552f1-180">The default value is 1.0f.</span></span><br/>                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="552f1-181">SurfaceScale</span><span class="sxs-lookup"><span data-stu-id="552f1-181">SurfaceScale</span></span><br/> <span data-ttu-id="552f1-182">D2D1 \_ POINTSPECULAR \_ 的 \_ 平面 \_ 縮放比例</span><span class="sxs-lookup"><span data-stu-id="552f1-182">D2D1\_POINTSPECULAR\_PROP\_SURFACE\_SCALE</span></span><br/>           | <span data-ttu-id="552f1-183">用來產生高度地圖之 Z 方向的縮放比例。</span><span class="sxs-lookup"><span data-stu-id="552f1-183">The scale factor in the Z direction for generating a height map.</span></span> <span data-ttu-id="552f1-184">值沒有單位，而且必須介於0到10000之間。</span><span class="sxs-lookup"><span data-stu-id="552f1-184">The value is unitless and must be between 0 and 10,000.</span></span> <span data-ttu-id="552f1-185">此類型為 FLOAT。</span><span class="sxs-lookup"><span data-stu-id="552f1-185">The type is FLOAT.</span></span><br/> <span data-ttu-id="552f1-186">預設值為 1.0 f。</span><span class="sxs-lookup"><span data-stu-id="552f1-186">The default value is 1.0f.</span></span><br/>                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="552f1-187">Color</span><span class="sxs-lookup"><span data-stu-id="552f1-187">Color</span></span><br/> <span data-ttu-id="552f1-188">D2D1 \_ POINTSPECULAR \_ 的 \_ 色彩</span><span class="sxs-lookup"><span data-stu-id="552f1-188">D2D1\_POINTSPECULAR\_PROP\_COLOR</span></span><br/>                           | <span data-ttu-id="552f1-189">傳入光線的色彩。</span><span class="sxs-lookup"><span data-stu-id="552f1-189">The color of the incoming light.</span></span> <span data-ttu-id="552f1-190">這個屬性會公開為 D2D1 \_ 向量 \_ 3F (R、G、B) ，用來計算 L<sub>R</sub>、L<sub>G</sub>、l<sub>b</sub>。</span><span class="sxs-lookup"><span data-stu-id="552f1-190">This property is exposed as a D2D1\_VECTOR\_3F   (R, G, B) and used to compute L<sub>R</sub>, L<sub>G</sub>, L<sub>B</sub>.</span></span> <span data-ttu-id="552f1-191">此類型為 D2D1 \_ VECTOR \_ 3F。</span><span class="sxs-lookup"><span data-stu-id="552f1-191">The type is D2D1\_VECTOR\_3F.</span></span><br/> <span data-ttu-id="552f1-192">預設值為 {1.0 f、1.0 f、1.0 f}。</span><span class="sxs-lookup"><span data-stu-id="552f1-192">The default value is {1.0f, 1.0f, 1.0f}.</span></span><br/>                                                                                                                                                                                                                             |
| <span data-ttu-id="552f1-193">KernelUnitLength</span><span class="sxs-lookup"><span data-stu-id="552f1-193">KernelUnitLength</span></span><br/> <span data-ttu-id="552f1-194">D2D1 \_ POINTSPECULAR \_ 的 \_ 核心 \_ 單位 \_ 長度</span><span class="sxs-lookup"><span data-stu-id="552f1-194">D2D1\_POINTSPECULAR\_PROP\_KERNEL\_UNIT\_LENGTH</span></span><br/> | <span data-ttu-id="552f1-195">Sobel 核心中用來以 X 和 Y 方向產生表面法線的元素大小。</span><span class="sxs-lookup"><span data-stu-id="552f1-195">The size of an element in the Sobel kernel used to generate the surface normal in the X and Y directions.</span></span> <span data-ttu-id="552f1-196">這個屬性會對應至 Sobel 漸層中的 dx 和 dy 值。</span><span class="sxs-lookup"><span data-stu-id="552f1-196">This property maps to the dx and dy values in the Sobel gradient.</span></span> <span data-ttu-id="552f1-197">這個屬性是 D2D1 \_ 向量 \_ 2F (核心單位長度 X、核心單位長度 Y) ，而且是在 (Dip/核心單位) 中定義。</span><span class="sxs-lookup"><span data-stu-id="552f1-197">This property is a D2D1\_VECTOR\_2F(Kernel Unit Length X, Kernel Unit Length Y) and is defined in (DIPs/Kernel Unit).</span></span> <span data-ttu-id="552f1-198">效果會使用雙線性插補來調整點陣圖，以符合核心元素的大小。</span><span class="sxs-lookup"><span data-stu-id="552f1-198">The effect uses bilinear interpolation to scale the bitmap to match size of kernel elements.</span></span> <span data-ttu-id="552f1-199">此類型為 D2D1 \_ VECTOR \_ 2f。</span><span class="sxs-lookup"><span data-stu-id="552f1-199">The type is D2D1\_VECTOR\_2F.</span></span><br/> <span data-ttu-id="552f1-200">預設值為 {1.0 f、1.0 f}。</span><span class="sxs-lookup"><span data-stu-id="552f1-200">The default value is {1.0f, 1.0f}.</span></span><br/> |
| <span data-ttu-id="552f1-201">ScaleMode</span><span class="sxs-lookup"><span data-stu-id="552f1-201">ScaleMode</span></span><br/> <span data-ttu-id="552f1-202">D2D1 \_ POINTSPECULAR \_ 的 \_ 範圍調整 \_ 模式</span><span class="sxs-lookup"><span data-stu-id="552f1-202">D2D1\_POINTSPECULAR\_PROP\_SCALE\_MODE</span></span><br/>                 | <span data-ttu-id="552f1-203">效果用來將影像調整為對應核心單位長度的插補模式。</span><span class="sxs-lookup"><span data-stu-id="552f1-203">The interpolation mode the effect uses to scale the image to the corresponding kernel unit length.</span></span> <span data-ttu-id="552f1-204">有六個調整模式的品質和速度。</span><span class="sxs-lookup"><span data-stu-id="552f1-204">There are six scale modes that range in quality and speed.</span></span> <span data-ttu-id="552f1-205">如需詳細資訊，請參閱 [調整模式](#scales-modes) 。</span><span class="sxs-lookup"><span data-stu-id="552f1-205">See [Scale modes](#scales-modes) for more info.</span></span> <br/> <span data-ttu-id="552f1-206">此類型為 D2D1 \_ POINTSPECULAR \_ SCALE \_ 模式。</span><span class="sxs-lookup"><span data-stu-id="552f1-206">The type is D2D1\_POINTSPECULAR\_SCALE\_MODE.</span></span><br/> <span data-ttu-id="552f1-207">預設值為 D2D1 \_ POINTSPECULAR \_ SCALE \_ MODE \_ 線性。</span><span class="sxs-lookup"><span data-stu-id="552f1-207">The default value is D2D1\_POINTSPECULAR\_SCALE\_MODE\_LINEAR.</span></span><br/>                                                                                                                          |



 

## <a name="scales-modes"></a><span data-ttu-id="552f1-208">縮放模式</span><span class="sxs-lookup"><span data-stu-id="552f1-208">Scales modes</span></span>



| <span data-ttu-id="552f1-209">列舉型別</span><span class="sxs-lookup"><span data-stu-id="552f1-209">Enumeration</span></span>                                             | <span data-ttu-id="552f1-210">描述</span><span class="sxs-lookup"><span data-stu-id="552f1-210">Description</span></span>                                                                                                                                                                                          |
|---------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="552f1-211">\_ \_ \_ \_ 最接近 \_ 鄰近的 D2D1 POINTSPECULAR 調整模式</span><span class="sxs-lookup"><span data-stu-id="552f1-211">D2D1\_POINTSPECULAR\_SCALE\_MODE\_NEAREST\_NEIGHBOR</span></span>     | <span data-ttu-id="552f1-212">範例最接近的單一點，並使用該點。</span><span class="sxs-lookup"><span data-stu-id="552f1-212">Samples the nearest single point and uses that.</span></span> <span data-ttu-id="552f1-213">這個模式會使用較少的處理時間，但會輸出最低品質的影像。</span><span class="sxs-lookup"><span data-stu-id="552f1-213">This mode uses less processing time, but outputs the lowest quality image.</span></span>                                                                           |
| <span data-ttu-id="552f1-214">D2D1 \_ POINTSPECULAR \_ SCALE \_ 模式 \_ 線性</span><span class="sxs-lookup"><span data-stu-id="552f1-214">D2D1\_POINTSPECULAR\_SCALE\_MODE\_LINEAR</span></span>                | <span data-ttu-id="552f1-215">使用四個點取樣和線性插補。</span><span class="sxs-lookup"><span data-stu-id="552f1-215">Uses a four point sample and linear interpolation.</span></span> <span data-ttu-id="552f1-216">此模式會輸出比最接近的鄰近程度更高的品質影像。</span><span class="sxs-lookup"><span data-stu-id="552f1-216">This mode outputs a higher quality image than nearest neighbor.</span></span>                                                                                   |
| <span data-ttu-id="552f1-217">D2D1 \_ POINTSPECULAR \_ SCALE \_ 模式 \_ 立方</span><span class="sxs-lookup"><span data-stu-id="552f1-217">D2D1\_POINTSPECULAR\_SCALE\_MODE\_CUBIC</span></span>                 | <span data-ttu-id="552f1-218">使用16個範例三核心來進行插補。</span><span class="sxs-lookup"><span data-stu-id="552f1-218">Uses a 16 sample cubic kernel for interpolation.</span></span> <span data-ttu-id="552f1-219">這個模式會使用大部分的處理時間，但會輸出較高品質的影像。</span><span class="sxs-lookup"><span data-stu-id="552f1-219">This mode uses the most processing time, but outputs a higher quality image.</span></span>                                                                        |
| <span data-ttu-id="552f1-220">D2D1 \_ POINTSPECULAR \_ SCALE \_ MODE \_ 多重 \_ 範例 \_ 線性</span><span class="sxs-lookup"><span data-stu-id="552f1-220">D2D1\_POINTSPECULAR\_SCALE\_MODE\_MULTI\_SAMPLE\_LINEAR</span></span> | <span data-ttu-id="552f1-221">使用單一圖元內的4個線性樣本來取得良好的邊緣消除鋸齒。</span><span class="sxs-lookup"><span data-stu-id="552f1-221">Uses 4 linear samples within a single pixel for good edge anti-aliasing.</span></span> <span data-ttu-id="552f1-222">這種模式適合用來在具有少量圖元的影像上相應減少量。</span><span class="sxs-lookup"><span data-stu-id="552f1-222">This mode is good for scaling down by small amounts on images with few pixels.</span></span>                                              |
| <span data-ttu-id="552f1-223">D2D1 \_ POINTSPECULAR \_ SCALE \_ 模式 \_ 非等</span><span class="sxs-lookup"><span data-stu-id="552f1-223">D2D1\_POINTSPECULAR\_SCALE\_MODE\_ANISOTROPIC</span></span>           | <span data-ttu-id="552f1-224">根據點陣圖的轉換圖形，使用非等向篩選來取樣模式。</span><span class="sxs-lookup"><span data-stu-id="552f1-224">Uses anisotropic filtering to sample a pattern according to the transformed shape of the bitmap.</span></span>                                                                                                     |
| <span data-ttu-id="552f1-225">D2D1 \_ POINTSPECULAR \_ 調整 \_ 模式 \_ 高 \_ 品質 \_ 三階</span><span class="sxs-lookup"><span data-stu-id="552f1-225">D2D1\_POINTSPECULAR\_SCALE\_MODE\_HIGH\_QUALITY\_CUBIC</span></span>  | <span data-ttu-id="552f1-226">如果 downscaling 與轉換矩陣有關，則使用可變大小的高品質三核心來執行預先縮小的影像。</span><span class="sxs-lookup"><span data-stu-id="552f1-226">Uses a variable size high quality cubic kernel to perform a pre-downscale the image if downscaling is involved in the transform matrix.</span></span> <span data-ttu-id="552f1-227">然後使用三次插補模式來進行最終輸出。</span><span class="sxs-lookup"><span data-stu-id="552f1-227">Then uses the cubic interpolation mode for the final output.</span></span> |



 

> [!Note]  
> <span data-ttu-id="552f1-228">如果您未選取模式，效果會預設為 D2D1 \_ POINTSPECULAR \_ 縮放 \_ 模式 \_ 線性。</span><span class="sxs-lookup"><span data-stu-id="552f1-228">If you don't select a mode, the effect defaults to D2D1\_POINTSPECULAR\_SCALE\_MODE\_LINEAR.</span></span>

## <a name="requirements"></a><span data-ttu-id="552f1-229">規格需求</span><span class="sxs-lookup"><span data-stu-id="552f1-229">Requirements</span></span>



| <span data-ttu-id="552f1-230">需求</span><span class="sxs-lookup"><span data-stu-id="552f1-230">Requirement</span></span> | <span data-ttu-id="552f1-231">值</span><span class="sxs-lookup"><span data-stu-id="552f1-231">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="552f1-232">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="552f1-232">Minimum supported client</span></span> | <span data-ttu-id="552f1-233">適用于 Windows 7 desktop app 的 Windows 8 和平臺更新 \[ \| windows Store 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="552f1-233">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="552f1-234">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="552f1-234">Minimum supported server</span></span> | <span data-ttu-id="552f1-235">適用于 Windows 7 desktop app 的 Windows 8 和平臺更新 \[ \| windows Store 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="552f1-235">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="552f1-236">標頭</span><span class="sxs-lookup"><span data-stu-id="552f1-236">Header</span></span>                   | <span data-ttu-id="552f1-237">d2d1effects。h</span><span class="sxs-lookup"><span data-stu-id="552f1-237">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="552f1-238">程式庫</span><span class="sxs-lookup"><span data-stu-id="552f1-238">Library</span></span>                  | <span data-ttu-id="552f1-239">d2d1 .lib，dxguid .lib</span><span class="sxs-lookup"><span data-stu-id="552f1-239">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="552f1-240">相關主題</span><span class="sxs-lookup"><span data-stu-id="552f1-240">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="552f1-241">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="552f1-241">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

