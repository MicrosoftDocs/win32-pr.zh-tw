---
title: 3D 轉換效果
description: 使用3D 轉換效果將任意4x4 轉換矩陣套用至影像。
ms.assetid: BC2F2837-40F0-4293-A190-8B5F81BB01B6
keywords:
- 3d 轉換效果
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fabe0c2c220038802b5218b54187a1ff89268bfa
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/28/2021
ms.locfileid: "104561958"
---
# <a name="3d-transform-effect"></a><span data-ttu-id="8d564-104">3D 轉換效果</span><span class="sxs-lookup"><span data-stu-id="8d564-104">3D transform effect</span></span>

<span data-ttu-id="8d564-105">使用3D 轉換效果將任意4x4 轉換矩陣套用至影像。</span><span class="sxs-lookup"><span data-stu-id="8d564-105">Use the 3D transform effect to apply an arbitrary 4x4 transform matrix to an image.</span></span>

<span data-ttu-id="8d564-106">此效果會將矩陣 (M？ ) 您提供給來源影像的邊角頂點 (\[ x y z 1 \]) 使用此計算：</span><span class="sxs-lookup"><span data-stu-id="8d564-106">This effect applies the matrix (M?) you provide to the corner vertices of the source image (\[ x y z 1 \]) using this calculation:</span></span>

<span data-ttu-id="8d564-107">\[x<sub>r</sub> y<sub>r</sub> z<sub>r</sub> 1 \] = \[ x y z 1 \] \* M？</span><span class="sxs-lookup"><span data-stu-id="8d564-107">\[ x<sub>r</sub> y<sub>r</sub> z<sub>r</sub> 1 \]=\[ x y z 1 \]\*M?</span></span>

<span data-ttu-id="8d564-108">這項效果的 CLSID 是 CLSID \_ D2D13DTransform。</span><span class="sxs-lookup"><span data-stu-id="8d564-108">The CLSID for this effect is CLSID\_D2D13DTransform.</span></span>

-   [<span data-ttu-id="8d564-109">範例影像</span><span class="sxs-lookup"><span data-stu-id="8d564-109">Example image</span></span>](#example-image)
-   [<span data-ttu-id="8d564-110">效果屬性</span><span class="sxs-lookup"><span data-stu-id="8d564-110">Effect properties</span></span>](#effect-properties)
    -   [<span data-ttu-id="8d564-111">插補模式</span><span class="sxs-lookup"><span data-stu-id="8d564-111">Interpolation modes</span></span>](#interpolation-modes)
    -   [<span data-ttu-id="8d564-112">框線模式</span><span class="sxs-lookup"><span data-stu-id="8d564-112">Border modes</span></span>](#border-modes)
-   [<span data-ttu-id="8d564-113">4x4 轉換矩陣類別</span><span class="sxs-lookup"><span data-stu-id="8d564-113">4x4 Transform Matrix Class</span></span>](#4x4-transform-matrix-class)
-   [<span data-ttu-id="8d564-114">需求</span><span class="sxs-lookup"><span data-stu-id="8d564-114">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="8d564-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="8d564-115">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="8d564-116">範例影像</span><span class="sxs-lookup"><span data-stu-id="8d564-116">Example image</span></span>



| <span data-ttu-id="8d564-117">之前</span><span class="sxs-lookup"><span data-stu-id="8d564-117">Before</span></span>                                                        |
|---------------------------------------------------------------|
| ![轉換之前的影像。](images/default-before.jpg) |
| <span data-ttu-id="8d564-119">After</span><span class="sxs-lookup"><span data-stu-id="8d564-119">After</span></span>                                                         |
| ![轉換後的影像。](images/24-3dtransform.png)  |



 


```C++
ComPtr<ID2D1Effect> D2D13DTransformEffect;
m_d2dContext->CreateEffect(CLSID_D2D13DTransform, &D2D13DTransformEffect);

D2D13DTransformEffect->SetInput(0, bitmap);

// You can use the helper methods in D2D1::Matrix4x4F to create common matrix transformations.
D2D1_MATRIX_4X4_F matrix = 
    D2D1::Matrix4x4F::Translation(0.0f, -192.0f, 0.0f) *
    D2D1::Matrix4x4F::RotationY(30.0f) *
    D2D1::Matrix4x4F::Translation(0.0f, 192.0f, 0.0f);

D2D13DTransformEffect->SetValue(D2D1_3DTRANSFORM_PROP_TRANSFORM_MATRIX, matrix);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(D2D13DTransformEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a><span data-ttu-id="8d564-121">效果屬性</span><span class="sxs-lookup"><span data-stu-id="8d564-121">Effect properties</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="8d564-122">顯示名稱和索引列舉</span><span class="sxs-lookup"><span data-stu-id="8d564-122">Display name and index enumeration</span></span></th>
<th><span data-ttu-id="8d564-123">Description</span><span class="sxs-lookup"><span data-stu-id="8d564-123">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8d564-124">InterpolationMode</span><span class="sxs-lookup"><span data-stu-id="8d564-124">InterpolationMode</span></span><br/> <span data-ttu-id="8d564-125">D2D1_3DTRANSFORM_PROP_INTERPOLATION_MODE</span><span class="sxs-lookup"><span data-stu-id="8d564-125">D2D1_3DTRANSFORM_PROP_INTERPOLATION_MODE</span></span><br/></td>
<td><span data-ttu-id="8d564-126">效果在影像上使用的插補模式。</span><span class="sxs-lookup"><span data-stu-id="8d564-126">The interpolation mode the effect uses on the image.</span></span> <span data-ttu-id="8d564-127">有5種調整模式的品質和速度。</span><span class="sxs-lookup"><span data-stu-id="8d564-127">There are 5 scale modes that range in quality and speed.</span></span><br/> <span data-ttu-id="8d564-128">類型為 D2D1_3DTRANSFORM_INTERPOLATION_MODE。</span><span class="sxs-lookup"><span data-stu-id="8d564-128">Type is D2D1_3DTRANSFORM_INTERPOLATION_MODE.</span></span><br/> <span data-ttu-id="8d564-129">預設值為 D2D1_3DTRANSFORM_INTERPOLATION_MODE_LINEAR。</span><span class="sxs-lookup"><span data-stu-id="8d564-129">Default value is D2D1_3DTRANSFORM_INTERPOLATION_MODE_LINEAR.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8d564-130">BorderMode</span><span class="sxs-lookup"><span data-stu-id="8d564-130">BorderMode</span></span><br/> <span data-ttu-id="8d564-131">D2D1_3DTRANSFORM_PROP_BORDER_MODE</span><span class="sxs-lookup"><span data-stu-id="8d564-131">D2D1_3DTRANSFORM_PROP_BORDER_MODE</span></span><br/></td>
<td><span data-ttu-id="8d564-132">用來計算影像（軟或硬）框線的模式。</span><span class="sxs-lookup"><span data-stu-id="8d564-132">The mode used to calculate the border of the image, soft or hard.</span></span> <span data-ttu-id="8d564-133">如需詳細資訊，請參閱 <a href="https://www.bing.com/search?q=Border+modes">框線模式</a> 。</span><span class="sxs-lookup"><span data-stu-id="8d564-133">See <a href="https://www.bing.com/search?q=Border+modes">Border modes</a> for more info.</span></span><br/> <span data-ttu-id="8d564-134">類型為 D2D1_BORDER_MODE。</span><span class="sxs-lookup"><span data-stu-id="8d564-134">Type is D2D1_BORDER_MODE.</span></span><br/> <span data-ttu-id="8d564-135">預設值為 D2D1_BORDER_MODE_SOFT。</span><span class="sxs-lookup"><span data-stu-id="8d564-135">Default value is D2D1_BORDER_MODE_SOFT.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8d564-136">TransformMatrix</span><span class="sxs-lookup"><span data-stu-id="8d564-136">TransformMatrix</span></span><br/> <span data-ttu-id="8d564-137">D2D1_3DTRANSFORM_PROP_TRANSFORM_MATRIX</span><span class="sxs-lookup"><span data-stu-id="8d564-137">D2D1_3DTRANSFORM_PROP_TRANSFORM_MATRIX</span></span><br/></td>
<td><span data-ttu-id="8d564-138">套用至投射平面的4x4 轉換矩陣。</span><span class="sxs-lookup"><span data-stu-id="8d564-138">A 4x4 transform matrix applied to the projection plane.</span></span> <span data-ttu-id="8d564-139">下列矩陣計算可用來將某個3D 座標系統的點對應到轉換的2D 座標系統。</span><span class="sxs-lookup"><span data-stu-id="8d564-139">The following matrix calculation is used to map points from one 3D coordinate system to the transformed 2D coordinate system.</span></span> <br/><img src="images/3d-transform-matrix1.png" alt="3D Depth Matrix" /><span data-ttu-id="8d564-140">其中：</span><span class="sxs-lookup"><span data-stu-id="8d564-140">Where:</span></span><dl> <span data-ttu-id="8d564-141">X、Y、Z = 輸入投射平面座標</span><span class="sxs-lookup"><span data-stu-id="8d564-141">X, Y, Z = Input projection plane coordinates</span></span><br />
<span data-ttu-id="8d564-142">M<sub>x、y</sub> = 轉換矩陣元素</span><span class="sxs-lookup"><span data-stu-id="8d564-142">M<sub>x,y</sub> = Transform Matrix elements</span></span><br />
<span data-ttu-id="8d564-143">X、Y、Z = 輸出投射平面座標</span><span class="sxs-lookup"><span data-stu-id="8d564-143">X , Y , Z  =Output projection plane coordinates</span></span><br />
</dl> <br/> <span data-ttu-id="8d564-144">個別的矩陣元素未系結，而且沒有單位。</span><span class="sxs-lookup"><span data-stu-id="8d564-144">The individual matrix elements are not bounded and are unitless.</span></span> <br/> <span data-ttu-id="8d564-145">類型為 D2D1_MATRIX_4X4_F。</span><span class="sxs-lookup"><span data-stu-id="8d564-145">Type is D2D1_MATRIX_4X4_F.</span></span><br/> <span data-ttu-id="8d564-146">預設值為 Matrix4x4F (1、0、0、0、0、1、0、0、0、0、1、0、0、0、0、1) 。</span><span class="sxs-lookup"><span data-stu-id="8d564-146">Default value is Matrix4x4F(1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1).</span></span><br/></td>
</tr>
</tbody>
</table>



 

### <a name="interpolation-modes"></a><span data-ttu-id="8d564-147">插補模式</span><span class="sxs-lookup"><span data-stu-id="8d564-147">Interpolation modes</span></span>



| <span data-ttu-id="8d564-148">列舉型別</span><span class="sxs-lookup"><span data-stu-id="8d564-148">Enumeration</span></span>                                                   | <span data-ttu-id="8d564-149">描述</span><span class="sxs-lookup"><span data-stu-id="8d564-149">Description</span></span>                                                                                                                                                |
|---------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d564-150">\_ \_ \_ \_ 最接近 \_ 鄰近的 D2D1 3DTRANSFORM 插補模式</span><span class="sxs-lookup"><span data-stu-id="8d564-150">D2D1\_3DTRANSFORM\_INTERPOLATION\_MODE\_NEAREST\_NEIGHBOR</span></span>     | <span data-ttu-id="8d564-151">範例最接近的單一點，並使用該點。</span><span class="sxs-lookup"><span data-stu-id="8d564-151">Samples the nearest single point and uses that.</span></span> <span data-ttu-id="8d564-152">這個模式會使用較少的處理時間，但會輸出最低品質的影像。</span><span class="sxs-lookup"><span data-stu-id="8d564-152">This mode uses less processing time, but outputs the lowest quality image.</span></span>                                 |
| <span data-ttu-id="8d564-153">D2D1 \_ 3DTRANSFORM \_ 插補 \_ 模式 \_ 線性</span><span class="sxs-lookup"><span data-stu-id="8d564-153">D2D1\_3DTRANSFORM\_INTERPOLATION\_MODE\_LINEAR</span></span>                | <span data-ttu-id="8d564-154">使用四個點取樣和線性插補。</span><span class="sxs-lookup"><span data-stu-id="8d564-154">Uses a four point sample and linear interpolation.</span></span> <span data-ttu-id="8d564-155">這個模式所使用的處理時間比最近的鄰近模式更多，但會輸出較高品質的影像。</span><span class="sxs-lookup"><span data-stu-id="8d564-155">This mode uses more processing time than the nearest neighbor mode, but outputs a higher quality image.</span></span> |
| <span data-ttu-id="8d564-156">D2D1 \_ 3DTRANSFORM \_ 插補 \_ 模式 \_ 立方</span><span class="sxs-lookup"><span data-stu-id="8d564-156">D2D1\_3DTRANSFORM\_INTERPOLATION\_MODE\_CUBIC</span></span>                 | <span data-ttu-id="8d564-157">使用16個範例三核心來進行插補。</span><span class="sxs-lookup"><span data-stu-id="8d564-157">Uses a 16 sample cubic kernel for interpolation.</span></span> <span data-ttu-id="8d564-158">這個模式會使用大部分的處理時間，但會輸出較高品質的影像。</span><span class="sxs-lookup"><span data-stu-id="8d564-158">This mode uses the most processing time, but outputs a higher quality image.</span></span>                              |
| <span data-ttu-id="8d564-159">D2D1 \_ 3DTRANSFORM \_ 插補 \_ 模式 \_ 多 \_ 樣本 \_ 線性</span><span class="sxs-lookup"><span data-stu-id="8d564-159">D2D1\_3DTRANSFORM\_INTERPOLATION\_MODE\_MULTI\_SAMPLE\_LINEAR</span></span> | <span data-ttu-id="8d564-160">使用單一圖元內的4個線性樣本來取得良好的邊緣消除鋸齒。</span><span class="sxs-lookup"><span data-stu-id="8d564-160">Uses 4 linear samples within a single pixel for good edge anti-aliasing.</span></span> <span data-ttu-id="8d564-161">這種模式適合用來在具有少量圖元的影像上相應減少量。</span><span class="sxs-lookup"><span data-stu-id="8d564-161">This mode is good for scaling down by small amounts on images with few pixels.</span></span>    |
| <span data-ttu-id="8d564-162">D2D1 \_ 3DTRANSFORM \_ 插補 \_ 模式 \_ 各向異性</span><span class="sxs-lookup"><span data-stu-id="8d564-162">D2D1\_3DTRANSFORM\_INTERPOLATION\_MODE\_ANISOTROPIC</span></span>           | <span data-ttu-id="8d564-163">根據點陣圖的轉換圖形，使用非等向篩選來取樣模式。</span><span class="sxs-lookup"><span data-stu-id="8d564-163">Uses anisotropic filtering to sample a pattern according to the transformed shape of the bitmap.</span></span>                                                           |



 

> [!Note]  
> <span data-ttu-id="8d564-164">如果您未選取模式，效果會預設為 D2D1 \_ 3DTRANSFORM \_ 插補 \_ 模式 \_ 線性。</span><span class="sxs-lookup"><span data-stu-id="8d564-164">If you don't select a mode, the effect defaults to D2D1\_3DTRANSFORM\_INTERPOLATION\_MODE\_LINEAR.</span></span>

 

> [!Note]  
> <span data-ttu-id="8d564-165">當調整時，非等向模式會產生 mipmap，不過，如果您在輸入至此效果的效果上將快取 **的屬性設** 為 true，則每次都不會針對足夠的小型影像產生 mipmap。</span><span class="sxs-lookup"><span data-stu-id="8d564-165">Anisotropic mode generates mipmaps when scaling, however, if you set the **Cached** property to true on the effects that are input to this effect, the mipmaps won't be generated every time for sufficiently small images.</span></span>

 

### <a name="border-modes"></a><span data-ttu-id="8d564-166">框線模式</span><span class="sxs-lookup"><span data-stu-id="8d564-166">Border modes</span></span>



| <span data-ttu-id="8d564-167">Name</span><span class="sxs-lookup"><span data-stu-id="8d564-167">Name</span></span>                     | <span data-ttu-id="8d564-168">描述</span><span class="sxs-lookup"><span data-stu-id="8d564-168">Description</span></span>                                                                                                      |
|--------------------------|------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d564-169">D2D1 \_ 框線 \_ 模式 \_ 軟</span><span class="sxs-lookup"><span data-stu-id="8d564-169">D2D1\_BORDER\_MODE\_SOFT</span></span> | <span data-ttu-id="8d564-170">效果會在插補時以透明黑色圖元來填補影像，進而產生軟邊緣。</span><span class="sxs-lookup"><span data-stu-id="8d564-170">The effect pads the image with transparent black pixels as it interpolates, resulting in a soft edge.</span></span><br/> |
| <span data-ttu-id="8d564-171">D2D1 \_ 框線 \_ 模式 \_ 硬性</span><span class="sxs-lookup"><span data-stu-id="8d564-171">D2D1\_BORDER\_MODE\_HARD</span></span> | <span data-ttu-id="8d564-172">效果會將輸出個至輸入影像的大小。</span><span class="sxs-lookup"><span data-stu-id="8d564-172">The effect clamps the output to the size of the input image.</span></span> <br/>                                         |



 

## <a name="4x4-transform-matrix-class"></a><span data-ttu-id="8d564-173">4x4 轉換矩陣類別</span><span class="sxs-lookup"><span data-stu-id="8d564-173">4x4 Transform Matrix Class</span></span>

<span data-ttu-id="8d564-174">Direct2D 提供4x4 矩陣類別，以提供協助程式函式來轉換3個維度中的影像。</span><span class="sxs-lookup"><span data-stu-id="8d564-174">Direct2D provides a 4x4 matrix class to provide helper functions for transforming the image in 3 dimensions.</span></span> <span data-ttu-id="8d564-175">如需詳細資訊和所有類別成員的描述，請參閱 [**Matrix4x4F**](/windows/desktop/api/d2d1_1helper/nl-d2d1_1helper-matrix4x4f) 主題。</span><span class="sxs-lookup"><span data-stu-id="8d564-175">See the [**Matrix4x4F**](/windows/desktop/api/d2d1_1helper/nl-d2d1_1helper-matrix4x4f) topic for more info and a description of all the class members.</span></span>



| <span data-ttu-id="8d564-176">函式</span><span class="sxs-lookup"><span data-stu-id="8d564-176">Function</span></span>                                | <span data-ttu-id="8d564-177">描述</span><span class="sxs-lookup"><span data-stu-id="8d564-177">Description</span></span>                                                                                    | <span data-ttu-id="8d564-178">Matrix</span><span class="sxs-lookup"><span data-stu-id="8d564-178">Matrix</span></span>                                                 |
|-----------------------------------------|------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span data-ttu-id="8d564-179">Matrix4x4F：： Scale (X、Y、Z) </span><span class="sxs-lookup"><span data-stu-id="8d564-179">Matrix4x4F::Scale(X, Y, Z)</span></span>              | <span data-ttu-id="8d564-180">產生會以 X、Y 和/或 Z 方向調整投射平面的轉換矩陣。</span><span class="sxs-lookup"><span data-stu-id="8d564-180">Generates a transform matrix that scales the projection plane in the X, Y, and/or Z direction.</span></span> | ![scale3d 矩陣](images/3d-transform-matrix2.png)     |
| <span data-ttu-id="8d564-182">SkewX (X) </span><span class="sxs-lookup"><span data-stu-id="8d564-182">SkewX(X)</span></span>                                | <span data-ttu-id="8d564-183">產生會以 X 方向扭曲投射平面的轉換矩陣。</span><span class="sxs-lookup"><span data-stu-id="8d564-183">Generates a transform matrix that skews the projection plane in the X direction.</span></span>               | ![顯示 X 方向的扭曲矩陣。](images/matrix4x4-skewx.png)             |
| <span data-ttu-id="8d564-185">SkewY (Y) </span><span class="sxs-lookup"><span data-stu-id="8d564-185">SkewY(Y)</span></span>                                | <span data-ttu-id="8d564-186">產生會在 Y 方向扭曲投射平面的轉換矩陣。</span><span class="sxs-lookup"><span data-stu-id="8d564-186">Generates a transform matrix that skews the projection plane in the Y direction.</span></span>               | ![扭曲矩陣](images/matrix4x4-skewy.png)             |
| <span data-ttu-id="8d564-188">轉譯 (X、Y、Z) </span><span class="sxs-lookup"><span data-stu-id="8d564-188">Translation(X, Y, Z)</span></span>                    | <span data-ttu-id="8d564-189">產生會以 X、Y 或 Z 方向轉譯投射平面的轉換矩陣。</span><span class="sxs-lookup"><span data-stu-id="8d564-189">Generates a transform matrix that translates the projection plane in the X, Y, or Z direction.</span></span> | ![轉譯矩陣](images/3d-transform-matrix4.png)   |
| <span data-ttu-id="8d564-191">RotationX (X) </span><span class="sxs-lookup"><span data-stu-id="8d564-191">RotationX(X)</span></span>                            | <span data-ttu-id="8d564-192">產生會旋轉 X 軸之投射平面的轉換矩陣。</span><span class="sxs-lookup"><span data-stu-id="8d564-192">Generates a transform matrix that rotates the projection plane about the X axis.</span></span>               | ![旋轉 x 矩陣](images/3d-transform-matrix5.png)    |
| <span data-ttu-id="8d564-194">RotationY (Y) </span><span class="sxs-lookup"><span data-stu-id="8d564-194">RotationY(Y)</span></span>                            | <span data-ttu-id="8d564-195">產生會旋轉 Y 軸的投射平面的轉換矩陣。</span><span class="sxs-lookup"><span data-stu-id="8d564-195">Generates a transform matrix that rotates the projection plane about the Y axis.</span></span>               | ![旋轉 y 矩陣](images/3d-transform-matrix6.png)    |
| <span data-ttu-id="8d564-197">RotationZ (Z) </span><span class="sxs-lookup"><span data-stu-id="8d564-197">RotationZ(Z)</span></span>                            | <span data-ttu-id="8d564-198">產生會旋轉 Z 軸的投射平面的轉換矩陣。</span><span class="sxs-lookup"><span data-stu-id="8d564-198">Generates a transform matrix that rotates the projection plane about the Z axis.</span></span>               | ![旋轉 z 矩陣](images/3d-transform-matrix7.png)    |
| <span data-ttu-id="8d564-200">PerspectiveProjection (D) </span><span class="sxs-lookup"><span data-stu-id="8d564-200">PerspectiveProjection(D)</span></span>                | <span data-ttu-id="8d564-201">深度值為 D 的透視圖轉換。</span><span class="sxs-lookup"><span data-stu-id="8d564-201">A perspective transformation with a depth value of D.</span></span>                                          | ![透視圖矩陣](images/3d-transform-matrix8.png) |
| <span data-ttu-id="8d564-203">RotationArbitraryAxis (X、Y、Z、度數) </span><span class="sxs-lookup"><span data-stu-id="8d564-203">RotationArbitraryAxis(X, Y, Z, degrees)</span></span> | <span data-ttu-id="8d564-204">針對您指定的軸旋轉投射平面。</span><span class="sxs-lookup"><span data-stu-id="8d564-204">Rotates the projection plane about the axis you specify.</span></span>                                       |                                                        |



 

## <a name="requirements"></a><span data-ttu-id="8d564-205">規格需求</span><span class="sxs-lookup"><span data-stu-id="8d564-205">Requirements</span></span>



| <span data-ttu-id="8d564-206">需求</span><span class="sxs-lookup"><span data-stu-id="8d564-206">Requirement</span></span> | <span data-ttu-id="8d564-207">值</span><span class="sxs-lookup"><span data-stu-id="8d564-207">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8d564-208">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8d564-208">Minimum supported client</span></span> | <span data-ttu-id="8d564-209">適用于 Windows 7 desktop app 的 Windows 8 和平臺更新 \[ \| windows Store 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8d564-209">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="8d564-210">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8d564-210">Minimum supported server</span></span> | <span data-ttu-id="8d564-211">適用于 Windows 7 desktop app 的 Windows 8 和平臺更新 \[ \| windows Store 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8d564-211">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="8d564-212">標頭</span><span class="sxs-lookup"><span data-stu-id="8d564-212">Header</span></span>                   | <span data-ttu-id="8d564-213">d2d1effects。h</span><span class="sxs-lookup"><span data-stu-id="8d564-213">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="8d564-214">程式庫</span><span class="sxs-lookup"><span data-stu-id="8d564-214">Library</span></span>                  | <span data-ttu-id="8d564-215">d2d1 .lib，dxguid .lib</span><span class="sxs-lookup"><span data-stu-id="8d564-215">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="8d564-216">相關主題</span><span class="sxs-lookup"><span data-stu-id="8d564-216">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8d564-217">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="8d564-217">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

