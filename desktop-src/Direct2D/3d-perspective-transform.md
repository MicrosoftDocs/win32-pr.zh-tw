---
title: 3D 透視轉換效果
description: 使用3D 透視轉換效果，將影像旋轉為3個尺寸，就像從距離觀看一樣。
ms.assetid: 0E1A940E-2DCA-4772-BB68-7E5EF5CEF833
keywords:
- 3d 透視轉換效果
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ed2b1c5131319dd711d2c7802a0bfabceaaa32e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844427"
---
# <a name="3d-perspective-transform-effect"></a><span data-ttu-id="e4af5-104">3D 透視轉換效果</span><span class="sxs-lookup"><span data-stu-id="e4af5-104">3D perspective transform effect</span></span>

<span data-ttu-id="e4af5-105">使用3D 透視轉換效果，將影像旋轉為3個尺寸，就像從距離觀看一樣。</span><span class="sxs-lookup"><span data-stu-id="e4af5-105">Use the 3D perspective transform effect to rotate the image in 3 dimensions as if viewed from a distance.</span></span>

<span data-ttu-id="e4af5-106">3D 的觀點轉換比3D 轉換效果更為方便，但只會公開功能的子集。</span><span class="sxs-lookup"><span data-stu-id="e4af5-106">The 3D perspective transform is more convenient than the 3D transform effect, but only exposes a subset of the functionality.</span></span> <span data-ttu-id="e4af5-107">您可以計算完整的3D 轉換矩陣，並使用 [3d 轉換](3d-transform.md) 效果將更多任意的轉換矩陣套用至影像。</span><span class="sxs-lookup"><span data-stu-id="e4af5-107">You can compute a full 3D transformation matrix and apply a more arbitrary transform matrix to an image using the [3D transform](3d-transform.md) effect.</span></span>

<span data-ttu-id="e4af5-108">這項效果的 CLSID 是 CLSID \_ D2D13DPerspectiveTransform。</span><span class="sxs-lookup"><span data-stu-id="e4af5-108">The CLSID for this effect is CLSID\_D2D13DPerspectiveTransform.</span></span>

-   [<span data-ttu-id="e4af5-109">範例影像</span><span class="sxs-lookup"><span data-stu-id="e4af5-109">Example image</span></span>](#example-image)
-   [<span data-ttu-id="e4af5-110">效果屬性</span><span class="sxs-lookup"><span data-stu-id="e4af5-110">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="e4af5-111">插補模式</span><span class="sxs-lookup"><span data-stu-id="e4af5-111">Interpolation modes</span></span>](#interpolation-modes)
-   [<span data-ttu-id="e4af5-112">框線模式</span><span class="sxs-lookup"><span data-stu-id="e4af5-112">Border modes</span></span>](#border-modes)
-   [<span data-ttu-id="e4af5-113">輸出點陣圖</span><span class="sxs-lookup"><span data-stu-id="e4af5-113">Output bitmap</span></span>](#output-bitmap)
-   [<span data-ttu-id="e4af5-114">需求</span><span class="sxs-lookup"><span data-stu-id="e4af5-114">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="e4af5-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="e4af5-115">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="e4af5-116">範例影像</span><span class="sxs-lookup"><span data-stu-id="e4af5-116">Example image</span></span>



| <span data-ttu-id="e4af5-117">之前</span><span class="sxs-lookup"><span data-stu-id="e4af5-117">Before</span></span>                                                               |
|----------------------------------------------------------------------|
| ![效果之前的影像。](images/default-before.jpg)           |
| <span data-ttu-id="e4af5-119">After</span><span class="sxs-lookup"><span data-stu-id="e4af5-119">After</span></span>                                                                |
| ![效果之後的影像。](images/23-3dperspectivetransform.png) |



 


```C++
ComPtr<ID2D1Effect> perspectiveTransformEffect;
m_d2dContext->CreateEffect(CLSID_D2D13DPerspectiveTransform, &perspectiveTransformEffect);

perspectiveTransformEffect->SetInput(0, bitmap);

perspectiveTransformEffect->SetValue(D2D1_3DPERSPECTIVETRANSFORM_PROP_PERSPECTIVE_ORIGIN, D2D1::Vector3F(0.0f, 192.0f, 0.0f));
perspectiveTransformEffect->SetValue(D2D1_3DPERSPECTIVETRANSFORM_PROP_ROTATION, D2D1::Vector3F(0.0f, 30.0f, 0.0f));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(perspectiveTransformEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a><span data-ttu-id="e4af5-121">效果屬性</span><span class="sxs-lookup"><span data-stu-id="e4af5-121">Effect properties</span></span>



| <span data-ttu-id="e4af5-122">顯示名稱和索引列舉</span><span class="sxs-lookup"><span data-stu-id="e4af5-122">Display name and index enumeration</span></span>                                                              | <span data-ttu-id="e4af5-123">Description</span><span class="sxs-lookup"><span data-stu-id="e4af5-123">Description</span></span>                                                                                                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4af5-124">InterpolationMode</span><span class="sxs-lookup"><span data-stu-id="e4af5-124">InterpolationMode</span></span><br/> <span data-ttu-id="e4af5-125">D2D1 \_ 3DPERSPECTIVETRANSFORM \_ 的 \_ 內插補點 \_ 模式</span><span class="sxs-lookup"><span data-stu-id="e4af5-125">D2D1\_3DPERSPECTIVETRANSFORM\_PROP\_INTERPOLATION\_MODE</span></span><br/> | <span data-ttu-id="e4af5-126">效果在影像上使用的插補模式。</span><span class="sxs-lookup"><span data-stu-id="e4af5-126">The interpolation mode the effect uses on the image.</span></span> <span data-ttu-id="e4af5-127">有5種調整模式的品質和速度。</span><span class="sxs-lookup"><span data-stu-id="e4af5-127">There are 5 scale modes that range in quality and speed.</span></span><br/> <span data-ttu-id="e4af5-128">類型為 D2D1 \_ 3DPERSPECTIVETRANSFORM \_ 插補 \_ 模式。</span><span class="sxs-lookup"><span data-stu-id="e4af5-128">Type is D2D1\_3DPERSPECTIVETRANSFORM\_INTERPOLATION\_MODE.</span></span><br/> <span data-ttu-id="e4af5-129">預設值為 D2D1 \_ 3DPERSPECTIVETRANSFORM \_ 插補 \_ 模式 \_ 線性。</span><span class="sxs-lookup"><span data-stu-id="e4af5-129">Default value is D2D1\_3DPERSPECTIVETRANSFORM\_INTERPOLATION\_MODE\_LINEAR.</span></span><br/>              |
| <span data-ttu-id="e4af5-130">BorderMode</span><span class="sxs-lookup"><span data-stu-id="e4af5-130">BorderMode</span></span><br/> <span data-ttu-id="e4af5-131">D2D1 \_ 3DPERSPECTIVETRANSFORM \_ 的 \_ 樣式框線 \_ 模式</span><span class="sxs-lookup"><span data-stu-id="e4af5-131">D2D1\_3DPERSPECTIVETRANSFORM\_PROP\_BORDER\_MODE</span></span><br/>               | <span data-ttu-id="e4af5-132">用來計算影像（軟或硬）框線的模式。</span><span class="sxs-lookup"><span data-stu-id="e4af5-132">The mode used to calculate the border of the image, soft or hard.</span></span> <span data-ttu-id="e4af5-133">如需詳細資訊，請參閱 [框線模式](https://www.bing.com/search?q=Border+modes) 。</span><span class="sxs-lookup"><span data-stu-id="e4af5-133">See [Border modes](https://www.bing.com/search?q=Border+modes) for more info.</span></span><br/> <span data-ttu-id="e4af5-134">類型為 D2D1 \_ 框線 \_ 模式。</span><span class="sxs-lookup"><span data-stu-id="e4af5-134">Type is D2D1\_BORDER\_MODE.</span></span><br/> <span data-ttu-id="e4af5-135">預設值為 [D2D1 \_ 框線 \_ 模式] \_ 。</span><span class="sxs-lookup"><span data-stu-id="e4af5-135">Default value is D2D1\_BORDER\_MODE\_SOFT.</span></span><br/>                                                              |
| <span data-ttu-id="e4af5-136">深度</span><span class="sxs-lookup"><span data-stu-id="e4af5-136">Depth</span></span><br/> <span data-ttu-id="e4af5-137">D2D1 \_ 3DPERSPECTIVETRANSFORM \_ 的 \_ 深度</span><span class="sxs-lookup"><span data-stu-id="e4af5-137">D2D1\_3DPERSPECTIVETRANSFORM\_PROP\_DEPTH</span></span><br/>                           | <span data-ttu-id="e4af5-138">從 *PerspectiveOrigin* 到投射平面的距離。</span><span class="sxs-lookup"><span data-stu-id="e4af5-138">The distance from the *PerspectiveOrigin* to the projection plane.</span></span> <span data-ttu-id="e4af5-139">在 Dip 中指定的值必須大於0。</span><span class="sxs-lookup"><span data-stu-id="e4af5-139">The value specified in DIPs and must be greater than 0.</span></span><br/> <span data-ttu-id="e4af5-140">類型為 FLOAT。</span><span class="sxs-lookup"><span data-stu-id="e4af5-140">Type is FLOAT.</span></span><br/> <span data-ttu-id="e4af5-141">預設值為 1000.0 f。</span><span class="sxs-lookup"><span data-stu-id="e4af5-141">Default value is 1000.0f.</span></span><br/>                                                                                               |
| <span data-ttu-id="e4af5-142">PerspectiveOrigin</span><span class="sxs-lookup"><span data-stu-id="e4af5-142">PerspectiveOrigin</span></span><br/> <span data-ttu-id="e4af5-143">D2D1 \_ 3DPERSPECTIVETRANSFORM \_ 的 \_ 觀點 \_ 來源</span><span class="sxs-lookup"><span data-stu-id="e4af5-143">D2D1\_3DPERSPECTIVETRANSFORM\_PROP\_PERSPECTIVE\_ORIGIN</span></span><br/> | <span data-ttu-id="e4af5-144">3D 場景中檢視器的 X 和 Y 位置。</span><span class="sxs-lookup"><span data-stu-id="e4af5-144">The X and Y location of the viewer in the 3D scene.</span></span> <span data-ttu-id="e4af5-145">這個屬性是 \_ \_ 定義為： (point X，point Y) 的 D2D1 向量2f。</span><span class="sxs-lookup"><span data-stu-id="e4af5-145">This property is a D2D1\_VECTOR\_2F defined as: (point X, point Y).</span></span> <span data-ttu-id="e4af5-146">單位為 Dip。</span><span class="sxs-lookup"><span data-stu-id="e4af5-146">The units are in DIPs.</span></span><br/> <span data-ttu-id="e4af5-147">您可以使用 *Depth* 屬性來設定 Z 值。</span><span class="sxs-lookup"><span data-stu-id="e4af5-147">You set the Z value with the *Depth* property.</span></span><br/> <span data-ttu-id="e4af5-148">類型為 D2D1 \_ VECTOR \_ 2f。</span><span class="sxs-lookup"><span data-stu-id="e4af5-148">Type is D2D1\_VECTOR\_2F.</span></span><br/> <span data-ttu-id="e4af5-149">預設值為 {0.0 f，0.0 f}。</span><span class="sxs-lookup"><span data-stu-id="e4af5-149">Default value is {0.0f, 0.0f}.</span></span><br/> |
| <span data-ttu-id="e4af5-150">LocalOffset</span><span class="sxs-lookup"><span data-stu-id="e4af5-150">LocalOffset</span></span><br/> <span data-ttu-id="e4af5-151">D2D1 \_ 3DPERSPECTIVETRANSFORM \_ 的 \_ 局部 \_ 位移</span><span class="sxs-lookup"><span data-stu-id="e4af5-151">D2D1\_3DPERSPECTIVETRANSFORM\_PROP\_LOCAL\_OFFSET</span></span><br/>             | <span data-ttu-id="e4af5-152">效果在旋轉投射平面之前所執行的轉譯。</span><span class="sxs-lookup"><span data-stu-id="e4af5-152">A translation the effect performs before it rotates the projection plane.</span></span> <span data-ttu-id="e4af5-153">這個屬性是 \_ \_ 定義為： (X、Y、Z) 的 D2D1 向量3F。</span><span class="sxs-lookup"><span data-stu-id="e4af5-153">This property is a D2D1\_VECTOR\_3F defined as: (X, Y, Z).</span></span> <span data-ttu-id="e4af5-154">單位為 Dip。</span><span class="sxs-lookup"><span data-stu-id="e4af5-154">The units are in DIPs.</span></span><br/> <span data-ttu-id="e4af5-155">類型為 D2D1 \_ VECTOR \_ 3F。</span><span class="sxs-lookup"><span data-stu-id="e4af5-155">Type is D2D1\_VECTOR\_3F.</span></span><br/> <span data-ttu-id="e4af5-156">預設值為 {0.0 f、0.0 f、0.0 f}。</span><span class="sxs-lookup"><span data-stu-id="e4af5-156">Default value is {0.0f, 0.0f, 0.0f}.</span></span><br/>                                        |
| <span data-ttu-id="e4af5-157">GlobalOffset</span><span class="sxs-lookup"><span data-stu-id="e4af5-157">GlobalOffset</span></span><br/> <span data-ttu-id="e4af5-158">D2D1 \_ 3DPERSPECTIVETRANSFORM \_ 的 \_ 通用 \_ 位移</span><span class="sxs-lookup"><span data-stu-id="e4af5-158">D2D1\_3DPERSPECTIVETRANSFORM\_PROP\_GLOBAL\_OFFSET</span></span><br/>           | <span data-ttu-id="e4af5-159">效果在旋轉投射平面之後所執行的轉譯。</span><span class="sxs-lookup"><span data-stu-id="e4af5-159">A translation the effect performs after it rotates the projection plane.</span></span> <span data-ttu-id="e4af5-160">這個屬性是 \_ \_ 定義為： (X、Y、Z) 的 D2D1 向量3F。</span><span class="sxs-lookup"><span data-stu-id="e4af5-160">This property is a D2D1\_VECTOR\_3F defined as: (X, Y, Z).</span></span> <span data-ttu-id="e4af5-161">單位為 Dip。</span><span class="sxs-lookup"><span data-stu-id="e4af5-161">The units are in DIPs.</span></span><br/> <span data-ttu-id="e4af5-162">類型為 D2D1 \_ VECTOR \_ 3F。</span><span class="sxs-lookup"><span data-stu-id="e4af5-162">Type is D2D1\_VECTOR\_3F.</span></span><br/> <span data-ttu-id="e4af5-163">預設值為 {0.0 f、0.0 f、0.0 f}。</span><span class="sxs-lookup"><span data-stu-id="e4af5-163">Default value is {0.0f, 0.0f, 0.0f}.</span></span><br/>                                         |
| <span data-ttu-id="e4af5-164">RotationOrigin</span><span class="sxs-lookup"><span data-stu-id="e4af5-164">RotationOrigin</span></span><br/> <span data-ttu-id="e4af5-165">D2D1 \_ 3DPERSPECTIVETRANSFORM 的型 \_ \_ 旋轉 \_ 來源</span><span class="sxs-lookup"><span data-stu-id="e4af5-165">D2D1\_3DPERSPECTIVETRANSFORM\_PROP\_ROTATION\_ORIGIN</span></span><br/>       | <span data-ttu-id="e4af5-166">效果所執行之旋轉的中心點。</span><span class="sxs-lookup"><span data-stu-id="e4af5-166">The center point of the rotation the effect performs.</span></span> <span data-ttu-id="e4af5-167">這個屬性是 \_ \_ 定義為： (X、Y、Z) 的 D2D1 向量3F。</span><span class="sxs-lookup"><span data-stu-id="e4af5-167">This property is a D2D1\_VECTOR\_3F defined as: (X, Y, Z).</span></span> <span data-ttu-id="e4af5-168">單位為 Dip。</span><span class="sxs-lookup"><span data-stu-id="e4af5-168">The units are in DIPs.</span></span><br/> <span data-ttu-id="e4af5-169">類型為 D2D1 \_ VECTOR \_ 3F。</span><span class="sxs-lookup"><span data-stu-id="e4af5-169">Type is D2D1\_VECTOR\_3F.</span></span><br/> <span data-ttu-id="e4af5-170">預設值為 {0.0 f、0.0 f、0.0 f}。</span><span class="sxs-lookup"><span data-stu-id="e4af5-170">Default value is {0.0f, 0.0f, 0.0f}.</span></span><br/>                                                            |
| <span data-ttu-id="e4af5-171">旋轉</span><span class="sxs-lookup"><span data-stu-id="e4af5-171">Rotation</span></span><br/> <span data-ttu-id="e4af5-172">D2D1 \_ 3DPERSPECTIVETRANSFORM 的型 \_ \_ 旋轉</span><span class="sxs-lookup"><span data-stu-id="e4af5-172">D2D1\_3DPERSPECTIVETRANSFORM\_PROP\_ROTATION</span></span><br/>                     | <span data-ttu-id="e4af5-173">每個軸的旋轉角度。</span><span class="sxs-lookup"><span data-stu-id="e4af5-173">The angles of rotation for each axis.</span></span> <span data-ttu-id="e4af5-174">這個屬性是 \_ \_ 定義為： (X、Y、Z) 的 D2D1 向量3F。</span><span class="sxs-lookup"><span data-stu-id="e4af5-174">This property is a D2D1\_VECTOR\_3F defined as: (X, Y, Z).</span></span> <span data-ttu-id="e4af5-175">單位是以度為單位。</span><span class="sxs-lookup"><span data-stu-id="e4af5-175">The units are in degrees.</span></span><br/> <span data-ttu-id="e4af5-176">類型為 D2D1 \_ VECTOR \_ 3F。</span><span class="sxs-lookup"><span data-stu-id="e4af5-176">Type is D2D1\_VECTOR\_3F.</span></span><br/> <span data-ttu-id="e4af5-177">預設值為 {0.0 f、0.0 f、0.0 f}。</span><span class="sxs-lookup"><span data-stu-id="e4af5-177">Default value is {0.0f, 0.0f, 0.0f}.</span></span><br/>                                                                         |



 

## <a name="interpolation-modes"></a><span data-ttu-id="e4af5-178">插補模式</span><span class="sxs-lookup"><span data-stu-id="e4af5-178">Interpolation modes</span></span>



| <span data-ttu-id="e4af5-179">列舉型別</span><span class="sxs-lookup"><span data-stu-id="e4af5-179">Enumeration</span></span>                                                              | <span data-ttu-id="e4af5-180">描述</span><span class="sxs-lookup"><span data-stu-id="e4af5-180">Description</span></span>                                                                                                                                                |
|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4af5-181">\_ \_ \_ \_ 最接近 \_ 鄰近的 D2D1 3DPERSPECTIVETRANSFORM 插補模式</span><span class="sxs-lookup"><span data-stu-id="e4af5-181">D2D1\_3DPERSPECTIVETRANSFORM\_INTERPOLATION\_MODE\_NEAREST\_NEIGHBOR</span></span>     | <span data-ttu-id="e4af5-182">範例最接近的單一點，並使用該點。</span><span class="sxs-lookup"><span data-stu-id="e4af5-182">Samples the nearest single point and uses that.</span></span> <span data-ttu-id="e4af5-183">這個模式會使用較少的處理時間，但會輸出最低品質的影像。</span><span class="sxs-lookup"><span data-stu-id="e4af5-183">This mode uses less processing time, but outputs the lowest quality image.</span></span>                                 |
| <span data-ttu-id="e4af5-184">D2D1 \_ 3DPERSPECTIVETRANSFORM \_ 插補 \_ 模式 \_ 線性</span><span class="sxs-lookup"><span data-stu-id="e4af5-184">D2D1\_3DPERSPECTIVETRANSFORM\_INTERPOLATION\_MODE\_LINEAR</span></span>                | <span data-ttu-id="e4af5-185">使用四個點取樣和線性插補。</span><span class="sxs-lookup"><span data-stu-id="e4af5-185">Uses a four point sample and linear interpolation.</span></span> <span data-ttu-id="e4af5-186">這個模式所使用的處理時間比最近的鄰近模式更多，但會輸出較高品質的影像。</span><span class="sxs-lookup"><span data-stu-id="e4af5-186">This mode uses more processing time than the nearest neighbor mode, but outputs a higher quality image.</span></span> |
| <span data-ttu-id="e4af5-187">D2D1 \_ 3DPERSPECTIVETRANSFORM \_ 插補 \_ 模式 \_ 立方</span><span class="sxs-lookup"><span data-stu-id="e4af5-187">D2D1\_3DPERSPECTIVETRANSFORM\_INTERPOLATION\_MODE\_CUBIC</span></span>                 | <span data-ttu-id="e4af5-188">使用16個範例三核心來進行插補。</span><span class="sxs-lookup"><span data-stu-id="e4af5-188">Uses a 16 sample cubic kernel for interpolation.</span></span> <span data-ttu-id="e4af5-189">這個模式會使用大部分的處理時間，但會輸出較高品質的影像。</span><span class="sxs-lookup"><span data-stu-id="e4af5-189">This mode uses the most processing time, but outputs a higher quality image.</span></span>                              |
| <span data-ttu-id="e4af5-190">D2D1 \_ 3DPERSPECTIVETRANSFORM \_ 插補 \_ 模式 \_ 多 \_ 樣本 \_ 線性</span><span class="sxs-lookup"><span data-stu-id="e4af5-190">D2D1\_3DPERSPECTIVETRANSFORM\_INTERPOLATION\_MODE\_MULTI\_SAMPLE\_LINEAR</span></span> | <span data-ttu-id="e4af5-191">使用單一圖元內的4個線性樣本來取得良好的邊緣消除鋸齒。</span><span class="sxs-lookup"><span data-stu-id="e4af5-191">Uses 4 linear samples within a single pixel for good edge anti-aliasing.</span></span> <span data-ttu-id="e4af5-192">這種模式適合用來在具有少量圖元的影像上相應減少量。</span><span class="sxs-lookup"><span data-stu-id="e4af5-192">This mode is good for scaling down by small amounts on images with few pixels.</span></span>    |
| <span data-ttu-id="e4af5-193">D2D1 \_ 3DPERSPECTIVETRANSFORM \_ 插補 \_ 模式 \_ 各向異性</span><span class="sxs-lookup"><span data-stu-id="e4af5-193">D2D1\_3DPERSPECTIVETRANSFORM\_INTERPOLATION\_MODE\_ANISOTROPIC</span></span>           | <span data-ttu-id="e4af5-194">根據點陣圖的轉換圖形，使用非等向篩選來取樣模式。</span><span class="sxs-lookup"><span data-stu-id="e4af5-194">Uses anisotropic filtering to sample a pattern according to the transformed shape of the bitmap.</span></span>                                                           |



 

> [!Note]  
> <span data-ttu-id="e4af5-195">如果您未選取模式，效果會預設為 D2D1 \_ 3DPERSPECTIVETRANSFORM \_ 插補 \_ 模式 \_ 線性。</span><span class="sxs-lookup"><span data-stu-id="e4af5-195">If you don't select a mode, the effect defaults to D2D1\_3DPERSPECTIVETRANSFORM\_INTERPOLATION\_MODE\_LINEAR.</span></span>

 

> [!Note]  
> <span data-ttu-id="e4af5-196">當調整時，非等向模式會產生 mipmap，不過，如果您在輸入至此效果的效果上將快取 **的屬性設** 為 true，則每次都不會針對足夠的小型影像產生 mipmap。</span><span class="sxs-lookup"><span data-stu-id="e4af5-196">Anisotropic mode generates mipmaps when scaling, however, if you set the **Cached** property to true on the effects that are input to this effect, the mipmaps won't be generated every time for sufficiently small images.</span></span>

 

## <a name="border-modes"></a><span data-ttu-id="e4af5-197">框線模式</span><span class="sxs-lookup"><span data-stu-id="e4af5-197">Border modes</span></span>



| <span data-ttu-id="e4af5-198">Name</span><span class="sxs-lookup"><span data-stu-id="e4af5-198">Name</span></span>                     | <span data-ttu-id="e4af5-199">描述</span><span class="sxs-lookup"><span data-stu-id="e4af5-199">Description</span></span>                                                                                                      |
|--------------------------|------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4af5-200">D2D1 \_ 框線 \_ 模式 \_ 軟</span><span class="sxs-lookup"><span data-stu-id="e4af5-200">D2D1\_BORDER\_MODE\_SOFT</span></span> | <span data-ttu-id="e4af5-201">效果會在插補時以透明黑色圖元來填補影像，進而產生軟邊緣。</span><span class="sxs-lookup"><span data-stu-id="e4af5-201">The effect pads the image with transparent black pixels as it interpolates, resulting in a soft edge.</span></span><br/> |
| <span data-ttu-id="e4af5-202">D2D1 \_ 框線 \_ 模式 \_ 硬性</span><span class="sxs-lookup"><span data-stu-id="e4af5-202">D2D1\_BORDER\_MODE\_HARD</span></span> | <span data-ttu-id="e4af5-203">效果會將輸出個至輸入影像的大小。</span><span class="sxs-lookup"><span data-stu-id="e4af5-203">The effect clamps the output to the size of the input image.</span></span> <br/>                                         |



 

## <a name="output-bitmap"></a><span data-ttu-id="e4af5-204">輸出點陣圖</span><span class="sxs-lookup"><span data-stu-id="e4af5-204">Output bitmap</span></span>

<span data-ttu-id="e4af5-205">輸出點陣圖的大小取決於套用至影像的轉換矩陣。</span><span class="sxs-lookup"><span data-stu-id="e4af5-205">The size of the output bitmap depends on the transform matrix that is applied to the image.</span></span>

<span data-ttu-id="e4af5-206">效果會執行轉換作業，然後在結果周圍套用周框方塊。</span><span class="sxs-lookup"><span data-stu-id="e4af5-206">The effect performs the transform operation and then applies a bounding box around the result.</span></span> <span data-ttu-id="e4af5-207">輸出點陣圖是周框方塊的大小。</span><span class="sxs-lookup"><span data-stu-id="e4af5-207">The output bitmap is the size of the bounding box.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4af5-208">規格需求</span><span class="sxs-lookup"><span data-stu-id="e4af5-208">Requirements</span></span>



| <span data-ttu-id="e4af5-209">需求</span><span class="sxs-lookup"><span data-stu-id="e4af5-209">Requirement</span></span> | <span data-ttu-id="e4af5-210">值</span><span class="sxs-lookup"><span data-stu-id="e4af5-210">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e4af5-211">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e4af5-211">Minimum supported client</span></span> | <span data-ttu-id="e4af5-212">適用于 Windows 7 desktop app 的 Windows 8 和平臺更新 \[ \| windows Store 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e4af5-212">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="e4af5-213">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e4af5-213">Minimum supported server</span></span> | <span data-ttu-id="e4af5-214">適用于 Windows 7 desktop app 的 Windows 8 和平臺更新 \[ \| windows Store 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e4af5-214">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="e4af5-215">標頭</span><span class="sxs-lookup"><span data-stu-id="e4af5-215">Header</span></span>                   | <span data-ttu-id="e4af5-216">d2d1effects。h</span><span class="sxs-lookup"><span data-stu-id="e4af5-216">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="e4af5-217">程式庫</span><span class="sxs-lookup"><span data-stu-id="e4af5-217">Library</span></span>                  | <span data-ttu-id="e4af5-218">d2d1 .lib，dxguid .lib</span><span class="sxs-lookup"><span data-stu-id="e4af5-218">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="e4af5-219">相關主題</span><span class="sxs-lookup"><span data-stu-id="e4af5-219">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e4af5-220">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="e4af5-220">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

