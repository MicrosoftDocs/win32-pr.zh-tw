---
description: Direct3D 9 中點 sprite 的支援可讓您以高效能轉譯 (物件) 的點。 點 sprite 是泛用的泛用點，可讓任意圖形依照材質的定義來呈現。
ms.assetid: a9046c7e-779c-4f33-b8ff-f189da3dcfc5
title: '點 Sprite (Direct3D 9) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c988a104eb65b5e2d7e56ff2444e8d422c422df2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104510088"
---
# <a name="point-sprites-direct3d-9"></a><span data-ttu-id="baa25-104">點 Sprite (Direct3D 9) </span><span class="sxs-lookup"><span data-stu-id="baa25-104">Point Sprites (Direct3D 9)</span></span>

<span data-ttu-id="baa25-105">Direct3D 9 中點 sprite 的支援可讓您以高效能轉譯 (物件) 的點。</span><span class="sxs-lookup"><span data-stu-id="baa25-105">Support for point sprites in Direct3D 9 enables the high-performance rendering of points (particle systems).</span></span> <span data-ttu-id="baa25-106">點 sprite 是泛用的泛用點，可讓任意圖形依照材質的定義來呈現。</span><span class="sxs-lookup"><span data-stu-id="baa25-106">Point sprites are generalizations of generic points that enable arbitrary shapes to be rendered as defined by textures.</span></span>

-   [<span data-ttu-id="baa25-107">點基本呈現控制項</span><span class="sxs-lookup"><span data-stu-id="baa25-107">Point Primitive Rendering Controls</span></span>](#point-primitive-rendering-controls)
-   [<span data-ttu-id="baa25-108">點大小計算</span><span class="sxs-lookup"><span data-stu-id="baa25-108">Point Size Computations</span></span>](#point-size-computations)
-   [<span data-ttu-id="baa25-109">點轉譯</span><span class="sxs-lookup"><span data-stu-id="baa25-109">Point Rendering</span></span>](#point-rendering)

## <a name="point-primitive-rendering-controls"></a><span data-ttu-id="baa25-110">點基本呈現控制項</span><span class="sxs-lookup"><span data-stu-id="baa25-110">Point Primitive Rendering Controls</span></span>

<span data-ttu-id="baa25-111">Direct3D 9 支援其他參數，以控制點 sprite (點基本) 的呈現。</span><span class="sxs-lookup"><span data-stu-id="baa25-111">Direct3D 9 supports additional parameters to control the rendering of point sprites (point primitives).</span></span> <span data-ttu-id="baa25-112">這些參數可讓點成為變數大小，並套用完整紋理對應。</span><span class="sxs-lookup"><span data-stu-id="baa25-112">These parameters enable points to be of variable size and have a full texture map applied.</span></span> <span data-ttu-id="baa25-113">每個點的大小是由應用程式指定的大小所決定，並結合 Direct3D 所計算的以距離為基礎的函式。</span><span class="sxs-lookup"><span data-stu-id="baa25-113">The size of each point is determined by an application-specified size combined with a distance-based function computed by Direct3D.</span></span> <span data-ttu-id="baa25-114">應用程式可以將點大小指定為每個頂點，或設定 D3DRS \_ dialog，以套用至沒有每個頂點大小的點。</span><span class="sxs-lookup"><span data-stu-id="baa25-114">The application can specify point size either as per-vertex or by setting D3DRS\_POINTSIZE, which applies to points without a per-vertex size.</span></span> <span data-ttu-id="baa25-115">點大小是以相機空間單位來表示，但應用程式在將轉換後的彈性頂點格式傳遞 (FVF) 頂點時除外。</span><span class="sxs-lookup"><span data-stu-id="baa25-115">The point size is expressed in camera space units, with the exception of when the application is passing post-transformed flexible vertex format (FVF) vertices.</span></span> <span data-ttu-id="baa25-116">在此情況下，不會套用以距離為基礎的函式，而且點大小會以轉譯目標的圖元單位表示。</span><span class="sxs-lookup"><span data-stu-id="baa25-116">In this case, the distance-based function is not applied and the point size is expressed in units of pixels on the render target.</span></span>

<span data-ttu-id="baa25-117">當轉譯點取決於 D3DRS POINTSPRITEENABLE 的設定時，會計算並使用材質座標 \_ 。</span><span class="sxs-lookup"><span data-stu-id="baa25-117">The texture coordinates computed and used when rendering points depends on the setting of D3DRS\_POINTSPRITEENABLE.</span></span> <span data-ttu-id="baa25-118">當此值設定為 **TRUE** 時，會設定材質座標，讓每個點都顯示完整紋理。</span><span class="sxs-lookup"><span data-stu-id="baa25-118">When this value is set to **TRUE**, the texture coordinates are set so that each point displays the full texture.</span></span> <span data-ttu-id="baa25-119">一般來說，這只適用于點明顯大於一個圖元時。</span><span class="sxs-lookup"><span data-stu-id="baa25-119">In general, this is only useful when points are significantly larger than one pixel.</span></span> <span data-ttu-id="baa25-120">當 D3DRS \_ POINTSPRITEENABLE 設定為 **FALSE** 時，每個點的頂點材質座標都會用於整個點。</span><span class="sxs-lookup"><span data-stu-id="baa25-120">When D3DRS\_POINTSPRITEENABLE is set to **FALSE**, each point's vertex texture coordinate is used for the entire point.</span></span>

## <a name="point-size-computations"></a><span data-ttu-id="baa25-121">點大小計算</span><span class="sxs-lookup"><span data-stu-id="baa25-121">Point Size Computations</span></span>

<span data-ttu-id="baa25-122">點大小取決於 D3DRS \_ POINTSCALEENABLE。</span><span class="sxs-lookup"><span data-stu-id="baa25-122">Point size is determined by D3DRS\_POINTSCALEENABLE.</span></span> <span data-ttu-id="baa25-123">如果此值設定為 **FALSE**，則會使用應用程式指定的點大小做為螢幕空間 (轉換後的) 大小。</span><span class="sxs-lookup"><span data-stu-id="baa25-123">If this value is set to **FALSE**, the application-specified point size is used as the screen-space (post-transformed) size.</span></span> <span data-ttu-id="baa25-124">在螢幕空間中傳遞給 Direct3D 的頂點沒有計算的點大小;指定的點大小會轉譯為螢幕空間大小。</span><span class="sxs-lookup"><span data-stu-id="baa25-124">Vertices that are passed to Direct3D in screen space do not have point sizes computed; the specified point size is interpreted as screen-space size.</span></span>

<span data-ttu-id="baa25-125">如果 D3DRS \_ POINTSCALEENABLE 為 **TRUE**，Direct3D 會根據下列公式計算螢幕空間點大小。</span><span class="sxs-lookup"><span data-stu-id="baa25-125">If D3DRS\_POINTSCALEENABLE is **TRUE**, Direct3D computes the screen-space point size according to the following formula.</span></span> <span data-ttu-id="baa25-126">應用程式指定的點大小以相機空間單位表示。</span><span class="sxs-lookup"><span data-stu-id="baa25-126">The application-specified point size is expressed in camera space units.</span></span>

<span data-ttu-id="baa25-127">S = Vh \* s <sub>i</sub> \* (1/ (A + B \* D ₑ + C \* ( D ₑ² ) ) ) </span><span class="sxs-lookup"><span data-stu-id="baa25-127">S ₛ = Vₕ \* S <sub>i</sub> \* sqrt(1/(A + B \* D ₑ + C \*( D ₑ² )))</span></span>

<span data-ttu-id="baa25-128">在此公式中，輸入點大小（ <sub>i</sub>）是每個頂點或 D3DRS dialog 轉譯狀態的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="baa25-128">In this formula, the input point size, S <sub>i</sub>, is either per-vertex or the value of the D3DRS\_POINTSIZE render state.</span></span> <span data-ttu-id="baa25-129">點縮放因數、D3DRS \_ POINTSCALE \_ A、D3DRS \_ POINTSCALE \_ B 和 D3DRS \_ POINTSCALE \_ C 會以點 A、B 和 c 表示。視口的高度（V h）是代表視口的 [**D3DVIEWPORT9**](d3dviewport9.md) 結構高度成員。</span><span class="sxs-lookup"><span data-stu-id="baa25-129">The point scale factors, D3DRS\_POINTSCALE\_A, D3DRS\_POINTSCALE\_B, and D3DRS\_POINTSCALE\_C, are represented by the points A, B, and C. The height of the viewport, V ₕ, is the [**D3DVIEWPORT9**](d3dviewport9.md) structure's Height member representing the viewport.</span></span> <span data-ttu-id="baa25-130">D ₑ，從眼睛到) 原點 (眼睛的距離，會以點的眼睛空間位置 (X ₑ、Y ₑ、Z ₑ) ，然後執行下列作業來計算。</span><span class="sxs-lookup"><span data-stu-id="baa25-130">D ₑ, the distance from the eye to the position (the eye at the origin), is computed by taking the eye space position of the point (Xₑ, Yₑ, Zₑ) and performing the following operation.</span></span>

<span data-ttu-id="baa25-131">D ₑ = sqrt (X ₑ² + Y ₑ² + Z ₑ²) </span><span class="sxs-lookup"><span data-stu-id="baa25-131">D ₑ = sqrt (Xₑ² + Y ₑ² + Z ₑ²)</span></span>

<span data-ttu-id="baa25-132">最大點數大小（Pm ₐₓ）是以 [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) 結構的 MaxPointSize 成員或 D3DRS \_ dialog 最大轉譯狀態的較小者來決定 \_ 。</span><span class="sxs-lookup"><span data-stu-id="baa25-132">The maximum point size, Pₘₐₓ, is determined by taking the smaller of either the [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure's MaxPointSize member or the D3DRS\_POINTSIZE\_MAX render state.</span></span> <span data-ttu-id="baa25-133">最小的點大小（P<sub>分鐘</sub>）是藉由查詢 D3DRS dialog min 的值來決定 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="baa25-133">The minimum point size, P<sub>min</sub>, is determined by querying the value of D3DRS\_POINTSIZE\_MIN.</span></span> <span data-ttu-id="baa25-134">因此，最後的畫面空間點大小是以下列方式決定。</span><span class="sxs-lookup"><span data-stu-id="baa25-134">Thus the final screen-space point size, S, is determined in the following manner.</span></span>

-   <span data-ttu-id="baa25-135">如果 Ss > Pm ₐₓ，則 S = P m ₐₓ</span><span class="sxs-lookup"><span data-stu-id="baa25-135">If Sₛ > Pₘₐₓ, then S = P ₘₐₓ</span></span>
-   <span data-ttu-id="baa25-136">如果 S < P<sub>分鐘</sub>，則 s = p <sub>分鐘</sub></span><span class="sxs-lookup"><span data-stu-id="baa25-136">if S < P<sub>min</sub>, then S = P <sub>min</sub></span></span>
-   <span data-ttu-id="baa25-137">否則，S = S</span><span class="sxs-lookup"><span data-stu-id="baa25-137">Otherwise, S = S ₛ</span></span>

## <a name="point-rendering"></a><span data-ttu-id="baa25-138">點轉譯</span><span class="sxs-lookup"><span data-stu-id="baa25-138">Point Rendering</span></span>

<span data-ttu-id="baa25-139">螢幕空間大小 S 的螢幕空間點、P = ( X、Y、Z、W) ，會以下列四個頂點的四邊形來進行柵格化。</span><span class="sxs-lookup"><span data-stu-id="baa25-139">A screen-space point, P = ( X, Y, Z, W), of screen-space size S is rasterized as a quadrilateral of the following four vertices.</span></span>

<span data-ttu-id="baa25-140"> ( ( X + S/2、Y + S/2、Z、W) 、 ( X + S/2、Y-S/2、Z、W) 、 ( X-S/2、Y-S/2、Z、W) 、 ( X-S/2、Y + S/2、Z、W) ) </span><span class="sxs-lookup"><span data-stu-id="baa25-140">(( X + S/2, Y + S/2, Z, W), ( X + S/2, Y - S/2, Z, W), ( X - S/2, Y- S/2, Z, W), ( X - S/2, Y + S/2, Z, W))</span></span>

<span data-ttu-id="baa25-141">頂點色彩屬性會在每個頂點複製;因此，每個點一律會以固定色彩呈現。</span><span class="sxs-lookup"><span data-stu-id="baa25-141">The vertex color attributes are duplicated at each vertex; thus each point is always rendered with constant colors.</span></span>

<span data-ttu-id="baa25-142">紋理索引的指派是由 [D3DRS POINTSPRITEENABLE 轉譯 \_ 狀態] 設定所控制。</span><span class="sxs-lookup"><span data-stu-id="baa25-142">The assignment of texture indices is controlled by the D3DRS\_POINTSPRITEENABLE render state setting.</span></span> <span data-ttu-id="baa25-143">如果 D3DRS \_ POINTSPRITEENABLE 設定為 **FALSE**，則頂點材質座標會在每個頂點上重複。</span><span class="sxs-lookup"><span data-stu-id="baa25-143">If D3DRS\_POINTSPRITEENABLE is set to **FALSE**, then the vertex texture coordinates are duplicated at each vertex.</span></span> <span data-ttu-id="baa25-144">如果 D3DRS \_ POINTSPRITEENABLE 設定為 **TRUE**，則四個頂點上的材質座標會設定為下列值。</span><span class="sxs-lookup"><span data-stu-id="baa25-144">If D3DRS\_POINTSPRITEENABLE is set to **TRUE**, then the texture coordinates at the four vertices are set to the following values.</span></span>

<span data-ttu-id="baa25-145"> (0. F、0 F) 、 (0 F.、1. F) 、 (1. F、0 F) 、 (1. F、1. F) </span><span class="sxs-lookup"><span data-stu-id="baa25-145">(0.F, 0.F), (0.F, 1.F), (1.F, 0.F), (1.F, 1.F)</span></span>

<span data-ttu-id="baa25-146">如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="baa25-146">This is shown in the following diagram.</span></span>

![正方形的圖表，其中包含 (u、v) 和 (x、y) 座標值的標記頂點](images/spritepoint.png)

<span data-ttu-id="baa25-148">啟用裁剪時，會以下列方式裁剪點點。</span><span class="sxs-lookup"><span data-stu-id="baa25-148">When clipping is enabled, points are clipped in the following manner.</span></span> <span data-ttu-id="baa25-149">如果頂點超過深度值的範圍（ [**D3DVIEWPORT9**](d3dviewport9.md) 結構的 MinZ 和 MaxZ），將會在其中呈現場景，則點會存在於視圖的分割區之外，而且不會呈現。</span><span class="sxs-lookup"><span data-stu-id="baa25-149">If the vertex exceeds the range of depth values - MinZ and MaxZ of the [**D3DVIEWPORT9**](d3dviewport9.md) structure - into which a scene is to be rendered, the point exists outside of the view frustum and is not rendered.</span></span> <span data-ttu-id="baa25-150">如果考慮點大小的點是完全在 X 和 Y 的視口之外，則不會呈現點;其餘的點都會呈現。</span><span class="sxs-lookup"><span data-stu-id="baa25-150">If the point, taking into account the point size, is completely outside the viewport in X and Y, then the point is not rendered; the remaining points are rendered.</span></span> <span data-ttu-id="baa25-151">點位置可能會位於 X 或 Y 的視口之外，而且仍然是部分可見的。</span><span class="sxs-lookup"><span data-stu-id="baa25-151">It is possible for the point position to be outside the viewport in X or Y and still be partially visible.</span></span>

<span data-ttu-id="baa25-152">點可能會或可能不會正確地裁剪到使用者定義的剪輯平面。</span><span class="sxs-lookup"><span data-stu-id="baa25-152">Points may or may not be correctly clipped to user-defined clip planes.</span></span> <span data-ttu-id="baa25-153">如果 \_ 未在 [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) 結構的 PrimitiveMiscCaps 成員中設定 D3DPMISCCAPS CLIPPLANESCALEDPOINTS，則只會根據頂點位置將點裁剪到使用者定義的剪輯平面，以忽略點大小。</span><span class="sxs-lookup"><span data-stu-id="baa25-153">If D3DPMISCCAPS\_CLIPPLANESCALEDPOINTS is not set in the [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure's PrimitiveMiscCaps member, points are clipped to user-defined clip planes based only on the vertex position, ignoring the point size.</span></span> <span data-ttu-id="baa25-154">在此情況下，當頂點位置位於剪輯平面內時，會完全轉譯縮放點，並在頂點位置超出剪輯平面時捨棄。</span><span class="sxs-lookup"><span data-stu-id="baa25-154">In this case, scaled points are fully rendered when the vertex position is inside the clip planes, and discarded when the vertex position is outside a clip plane.</span></span> <span data-ttu-id="baa25-155">應用程式可以藉由將框線幾何新增至與最大點數大小相同的剪輯平面，來防止可能的成品。</span><span class="sxs-lookup"><span data-stu-id="baa25-155">Applications can prevent potential artifacts by adding a border geometry to clip planes that is as large as the maximum point size.</span></span>

<span data-ttu-id="baa25-156">如果 \_ 已設定 D3DPMISCCAPS CLIPPLANESCALEDPOINTS 位，則會將縮放點正確地裁剪到使用者定義的剪輯平面。</span><span class="sxs-lookup"><span data-stu-id="baa25-156">If the D3DPMISCCAPS\_CLIPPLANESCALEDPOINTS bit is set, then the scaled points are correctly clipped to user-defined clip planes.</span></span>

<span data-ttu-id="baa25-157">硬體頂點處理不一定會支援點大小。</span><span class="sxs-lookup"><span data-stu-id="baa25-157">Hardware vertex processing may or may not support point size.</span></span> <span data-ttu-id="baa25-158">例如，如果在 \_ \_ 硬體抽象層上使用 D3DCREATE 硬體 VERTEXPROCESSING 建立裝置 (HAL) 裝置 (D3DDEVTYPE \_ Hal) 將 [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) 結構的 MaxPointSize 成員設定為1.0 或0.0，則所有點都是單一圖元。</span><span class="sxs-lookup"><span data-stu-id="baa25-158">For example, if a device is created with D3DCREATE\_HARDWARE\_VERTEXPROCESSING on a hardware abstraction layer (HAL) device (D3DDEVTYPE\_HAL) that has the [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure's MaxPointSize member set to 1.0 or 0.0, then all points are a single pixel.</span></span> <span data-ttu-id="baa25-159">若要轉譯小於1.0 的圖元點 sprite，您必須使用 FVF TL (轉換和亮) 頂點或軟體頂點處理 (D3DCREATE \_ software \_ VERTEXPROCESSING) ，在這種情況下，Direct3D 執行時間會模擬點 sprite 轉譯。</span><span class="sxs-lookup"><span data-stu-id="baa25-159">To render pixel point sprites less than 1.0, you must use either FVF TL (transformed and lit) vertices or software vertex processing (D3DCREATE\_SOFTWARE\_VERTEXPROCESSING), in which case the Direct3D run time emulates the point sprite rendering.</span></span>

<span data-ttu-id="baa25-160">執行頂點處理並支援點 sprite-MaxPointSize 設定為大於 1.0 f-的硬體裝置必須執行 nontransformed sprite 的大小計算，而且必須正確設定 TL 頂點的每個頂點或 D3DRS \_ POINTSIZED3DRS \_ dialog。</span><span class="sxs-lookup"><span data-stu-id="baa25-160">A hardware device that does vertex processing and supports point sprites - MaxPointSize set to greater than 1.0f - is required to perform the size computation for nontransformed sprites and is required to properly set the per-vertex or D3DRS\_POINTSIZED3DRS\_POINTSIZE for TL vertices.</span></span>

<span data-ttu-id="baa25-161">如需有關點、線條和三角形之轉譯規則的詳細資訊，請參閱 [ (Direct3D 9) 的點陣化規則 ](rasterization-rules.md)。</span><span class="sxs-lookup"><span data-stu-id="baa25-161">For information about rendering rules for points, lines, and triangles, see [Rasterization Rules (Direct3D 9)](rasterization-rules.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="baa25-162">相關主題</span><span class="sxs-lookup"><span data-stu-id="baa25-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="baa25-163">頂點管線</span><span class="sxs-lookup"><span data-stu-id="baa25-163">Vertex Pipeline</span></span>](vertex-pipeline.md)
</dt> </dl>

 

 



