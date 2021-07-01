---
title: '轉換 (DirectComposition) '
description: 本主題討論 Microsoft DirectComposition 對二維 (2D) 仿射 (線性) 轉換的支援，並說明 DirectComposition 支援的轉換類型。
ms.assetid: a0f41cc6-e848-4831-8063-609e17d9b4c6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 991e1205422864efdec82bbd4067b9c7662aaf29
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118653"
---
# <a name="transforms-directcomposition"></a><span data-ttu-id="542d2-103">轉換 (DirectComposition) </span><span class="sxs-lookup"><span data-stu-id="542d2-103">Transforms (DirectComposition)</span></span>

> [!NOTE]
> <span data-ttu-id="542d2-104">針對 Windows 10 上的應用程式，我們建議使用 DirectComposition，而不是使用。</span><span class="sxs-lookup"><span data-stu-id="542d2-104">For apps on Windows 10, we recommend using Windows.UI.Composition APIs instead of DirectComposition.</span></span> <span data-ttu-id="542d2-105">如需詳細資訊，請參閱 [使用視覺分層將您的桌面應用程式現代化](/windows/uwp/composition/visual-layer-in-desktop-apps)。</span><span class="sxs-lookup"><span data-stu-id="542d2-105">For more info, see [Modernize your desktop app using the Visual layer](/windows/uwp/composition/visual-layer-in-desktop-apps).</span></span>

<span data-ttu-id="542d2-106">本主題討論 Microsoft DirectComposition 對二維 (2D) 仿射 (線性) 轉換的支援，並說明 DirectComposition 支援的轉換類型。</span><span class="sxs-lookup"><span data-stu-id="542d2-106">This topic discusses Microsoft DirectComposition support for two-dimensional (2D) affine (linear) transforms, and describes the types of transforms that DirectComposition supports.</span></span>

<span data-ttu-id="542d2-107">DirectComposition 也支援3D 的觀點轉換，但因為它們需要建立中繼點陣圖，所以 DirectComposition 會將它們視為效果，而不是轉換。</span><span class="sxs-lookup"><span data-stu-id="542d2-107">DirectComposition also supports 3D perspective transforms, but because they require the creation of an intermediate bitmap, DirectComposition considers them to be effects rather than transforms.</span></span> <span data-ttu-id="542d2-108">如需3D 透視圖轉換效果的詳細資訊，請參閱 [效果](effects.md)。</span><span class="sxs-lookup"><span data-stu-id="542d2-108">For information about 3D perspective transform effects, see [Effects](effects.md).</span></span>

<span data-ttu-id="542d2-109">本主題包含下列章節：</span><span class="sxs-lookup"><span data-stu-id="542d2-109">This topic includes the following sections:</span></span>

-   [<span data-ttu-id="542d2-110">什麼是 DirectComposition 2D 轉換？</span><span class="sxs-lookup"><span data-stu-id="542d2-110">What is a DirectComposition 2D transform?</span></span>](#what-is-a-directcomposition-2d-transform)
-   [<span data-ttu-id="542d2-111">DirectComposition 2D 座標空間</span><span class="sxs-lookup"><span data-stu-id="542d2-111">The DirectComposition 2D coordinate space</span></span>](#the-directcomposition-2d-coordinate-space)
-   [<span data-ttu-id="542d2-112">支援仿射2D 轉換</span><span class="sxs-lookup"><span data-stu-id="542d2-112">Support for affine 2D transforms</span></span>](#support-for-affine-2d-transforms)
-   [<span data-ttu-id="542d2-113">矩陣2D 轉換</span><span class="sxs-lookup"><span data-stu-id="542d2-113">Matrix 2D transforms</span></span>](#matrix-2d-transforms)
-   [<span data-ttu-id="542d2-114">轉換群組</span><span class="sxs-lookup"><span data-stu-id="542d2-114">Transform Groups</span></span>](#transform-groups)
-   [<span data-ttu-id="542d2-115">轉換動畫</span><span class="sxs-lookup"><span data-stu-id="542d2-115">Transform animation</span></span>](#transform-animation)
-   [<span data-ttu-id="542d2-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="542d2-116">Related topics</span></span>](#related-topics)

## <a name="what-is-a-directcomposition-2d-transform"></a><span data-ttu-id="542d2-117">什麼是 DirectComposition 2D 轉換？</span><span class="sxs-lookup"><span data-stu-id="542d2-117">What is a DirectComposition 2D transform?</span></span>

<span data-ttu-id="542d2-118">2D 轉換可讓您藉由將視覺效果移至另一個位置 (轉譯) ，讓它變得更大或更小 (調整) 、將它 (旋轉) ，或扭曲其形狀 (扭曲) 。</span><span class="sxs-lookup"><span data-stu-id="542d2-118">A 2D transform enables you to alter the position, size, or nature of a visual in two dimensions by moving the visual to another location (translation), making it larger or smaller (scaling), turning it (rotation), or distorting its shape (skewing).</span></span>

<span data-ttu-id="542d2-119">2D 轉換的達成方式是將視覺效果的點從某個位置對應到相同座標空間內的另一個位置，或從某個座標空間對應到另一個位置。</span><span class="sxs-lookup"><span data-stu-id="542d2-119">A 2D transform is achieved by mapping the points of a visual from one position to another within the same coordinate space, or from one coordinate space to another.</span></span> <span data-ttu-id="542d2-120">這項對應是由稱為轉換矩陣的值表所描述，定義為三個數據列的集合，其中有三個浮點值的資料行，如下表所示。</span><span class="sxs-lookup"><span data-stu-id="542d2-120">This mapping is described by a table of values called a transformation matrix, defined as a collection of three rows with three columns of floating-point values as shown in the following table.</span></span>

:::row:::
    :::column:::
        <span data-ttu-id="542d2-121">M11Default：1。0</span><span class="sxs-lookup"><span data-stu-id="542d2-121">M11Default: 1.0</span></span><br/>
        <span data-ttu-id="542d2-122">M21Default：0。0</span><span class="sxs-lookup"><span data-stu-id="542d2-122">M21Default: 0.0</span></span><br/>
        <span data-ttu-id="542d2-123">M31OffsetX：0。0</span><span class="sxs-lookup"><span data-stu-id="542d2-123">M31OffsetX: 0.0</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="542d2-124">M12Default：0。0</span><span class="sxs-lookup"><span data-stu-id="542d2-124">M12Default: 0.0</span></span><br/>
        <span data-ttu-id="542d2-125">M22Default：1。0</span><span class="sxs-lookup"><span data-stu-id="542d2-125">M22Default: 1.0</span></span><br/>
        <span data-ttu-id="542d2-126">M32OffsetY：0。0</span><span class="sxs-lookup"><span data-stu-id="542d2-126">M32OffsetY: 0.0</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="542d2-127">0.0</span><span class="sxs-lookup"><span data-stu-id="542d2-127">0.0</span></span><br/>
        <span data-ttu-id="542d2-128">0.0</span><span class="sxs-lookup"><span data-stu-id="542d2-128">0.0</span></span><br/>
        <span data-ttu-id="542d2-129">1.0</span><span class="sxs-lookup"><span data-stu-id="542d2-129">1.0</span></span>
    :::column-end:::
:::row-end:::

<span data-ttu-id="542d2-130">仿射2D 轉換的轉換矩陣是從上一個轉換矩陣省略第三個數據行的3到2個矩陣。</span><span class="sxs-lookup"><span data-stu-id="542d2-130">The transformation matrix for affine 2D transforms is a 3-by-2 matrix that omits the third column from the previous transformation matrix.</span></span> <span data-ttu-id="542d2-131">下表顯示此矩陣的版面配置。</span><span class="sxs-lookup"><span data-stu-id="542d2-131">The following table shows the layout of this matrix.</span></span>

:::row:::
    :::column:::
        <span data-ttu-id="542d2-132">M11Default：1。0</span><span class="sxs-lookup"><span data-stu-id="542d2-132">M11Default: 1.0</span></span><br/>
        <span data-ttu-id="542d2-133">M21Default：0。0</span><span class="sxs-lookup"><span data-stu-id="542d2-133">M21Default: 0.0</span></span><br/>
        <span data-ttu-id="542d2-134">M31OffsetX：0。0</span><span class="sxs-lookup"><span data-stu-id="542d2-134">M31OffsetX: 0.0</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="542d2-135">M12Default：0。0</span><span class="sxs-lookup"><span data-stu-id="542d2-135">M12Default: 0.0</span></span><br/>
        <span data-ttu-id="542d2-136">M22Default：1。0</span><span class="sxs-lookup"><span data-stu-id="542d2-136">M22Default: 1.0</span></span><br/>
        <span data-ttu-id="542d2-137">M32OffsetY：0。0</span><span class="sxs-lookup"><span data-stu-id="542d2-137">M32OffsetY: 0.0</span></span>
    :::column-end:::
:::row-end:::

> [!Note]  
> <span data-ttu-id="542d2-138">將2D 轉換套用至身歷聲內容時，DirectComposition 不會執行任何特殊處理。</span><span class="sxs-lookup"><span data-stu-id="542d2-138">DirectComposition does no special processing when applying 2D transforms to stereo content.</span></span> <span data-ttu-id="542d2-139">這表示在套用2D 轉換時，3D 內容可能會失真。</span><span class="sxs-lookup"><span data-stu-id="542d2-139">This means the 3D content might appear distorted when a 2D transform is applied to it.</span></span>

 

## <a name="the-directcomposition-2d-coordinate-space"></a><span data-ttu-id="542d2-140">DirectComposition 2D 座標空間</span><span class="sxs-lookup"><span data-stu-id="542d2-140">The DirectComposition 2D coordinate space</span></span>

<span data-ttu-id="542d2-141">DirectComposition 會使用左手式2D 座標空間;也就是說，正 X 軸的值會增加到右邊，且 y 軸值會向下增加。</span><span class="sxs-lookup"><span data-stu-id="542d2-141">DirectComposition uses a left-handed 2D coordinate space; that is, positive x-axis values increase to the right and positive y-axis values increase downward.</span></span> <span data-ttu-id="542d2-142">視覺效果的位置相對於原點，也就是 X 軸和 y 軸相交 (0，0) 的點，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="542d2-142">Visuals are positioned relative to the origin, which is the point where the x-axis and y-axis intersect (0, 0), as shown in the following illustration.</span></span>

![左手座標空間的 X 軸和 y 軸](images/coordinatespace.png)

<span data-ttu-id="542d2-144">藉由在 3 x 2 轉換矩陣中操作值，您可以旋轉、縮放、扭曲和轉譯兩個維度中的物件。</span><span class="sxs-lookup"><span data-stu-id="542d2-144">By manipulating values in a 3-by-2 transformation matrix, you can rotate, scale, skew, and translate an object in two dimensions.</span></span> <span data-ttu-id="542d2-145">例如，如果您將 OffsetX 設定為100，並將 OffsetY 設為200，則會將物件移至右邊的100圖元和下200圖元。</span><span class="sxs-lookup"><span data-stu-id="542d2-145">For example, if you set OffsetX to 100 and OffsetY to 200, you move the object to the right 100 pixels and down 200 pixels.</span></span>

## <a name="support-for-affine-2d-transforms"></a><span data-ttu-id="542d2-146">支援仿射2D 轉換</span><span class="sxs-lookup"><span data-stu-id="542d2-146">Support for affine 2D transforms</span></span>

<span data-ttu-id="542d2-147">下表說明 DirectComposition 所支援的仿射2D 轉換類型，並列出您可以用來執行各種類型轉換的介面。</span><span class="sxs-lookup"><span data-stu-id="542d2-147">The following table describes the types of affine 2D transforms supported by DirectComposition, and lists the interfaces that you can use to perform the various types of transformations.</span></span>



| <span data-ttu-id="542d2-148">轉換/介面</span><span class="sxs-lookup"><span data-stu-id="542d2-148">Transform/interface</span></span>                                                                               | <span data-ttu-id="542d2-149">描述</span><span class="sxs-lookup"><span data-stu-id="542d2-149">Description</span></span>                                                                                              | <span data-ttu-id="542d2-150">圖例</span><span class="sxs-lookup"><span data-stu-id="542d2-150">Illustration</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="542d2-151">輪替 2D [**idcompositionrotatetransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionrotatetransform) \[ 換行\]</span><span class="sxs-lookup"><span data-stu-id="542d2-151">Rotate 2D [**idcompositionrotatetransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionrotatetransform)\[newline\]</span></span>          | <span data-ttu-id="542d2-152">依據指定的中心點，以指定的角度旋轉視覺效果。</span><span class="sxs-lookup"><span data-stu-id="542d2-152">rotate a visual by the specified angle about the specified center point.</span></span>                                 | ![以順時針方向與原始正方形中央旋轉45度的圖例](images/rotate.png)               |
| <span data-ttu-id="542d2-154">調整 2D [**idcompositionscaletransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionscaletransform)的 \[ 新行\]</span><span class="sxs-lookup"><span data-stu-id="542d2-154">Scale 2D [**idcompositionscaletransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionscaletransform)\[newline\]</span></span>             | <span data-ttu-id="542d2-155">依指定的中心點依指定的因素調整視覺效果。</span><span class="sxs-lookup"><span data-stu-id="542d2-155">scale a visual by the specified factor about the specified center point.</span></span>                                 | ![調整130% 的正方形圖例](images/scale.png)                                                                  |
| <span data-ttu-id="542d2-157">扭曲 2D [**idcompositionskewtransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionskewtransform) \[ 換行\]</span><span class="sxs-lookup"><span data-stu-id="542d2-157">Skew 2D [**idcompositionskewtransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionskewtransform)\[newline\]</span></span>                | <span data-ttu-id="542d2-158">沿著 X 軸和 y 軸上的指定角度扭曲視覺效果，以及圍繞指定的中心點。</span><span class="sxs-lookup"><span data-stu-id="542d2-158">skew a visual by the specified angle along the x-axis and y-axis, and around the specified center point.</span></span> | ![從 y 軸逆時針算起30度的正方形圖例](images/skew.png)                                   |
| <span data-ttu-id="542d2-160">轉譯 2D [**idcompositiontranslatetransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositiontranslatetransform) \[ 換行\]</span><span class="sxs-lookup"><span data-stu-id="542d2-160">Translate 2D [**idcompositiontranslatetransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositiontranslatetransform)\[newline\]</span></span> | <span data-ttu-id="542d2-161">以 X 軸和 y 軸的方向變更視覺效果的位置。</span><span class="sxs-lookup"><span data-stu-id="542d2-161">change the position of a visual in the direction of the x-axis and y-axis.</span></span>                               | ![正方形的圖，沿著正 X 軸移動20個單位，沿著正 y 軸移動10個單位](images/translate.png) |



 

## <a name="matrix-2d-transforms"></a><span data-ttu-id="542d2-163">矩陣2D 轉換</span><span class="sxs-lookup"><span data-stu-id="542d2-163">Matrix 2D transforms</span></span>

<span data-ttu-id="542d2-164">[**IDCompositionMatrixTransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionmatrixtransform)介面可讓您定義自己的三2仿射2d 轉換矩陣，並將其套用至視覺效果。</span><span class="sxs-lookup"><span data-stu-id="542d2-164">The [**IDCompositionMatrixTransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionmatrixtransform) interface enables you to define your own 3-by-2 affine 2D transform matrix and apply it to a visual.</span></span> <span data-ttu-id="542d2-165">如果您需要套用無法透過其他 DirectComposition 轉換介面使用的仿射2D 轉換類型，這個介面會很有用。</span><span class="sxs-lookup"><span data-stu-id="542d2-165">This interface is useful if you need to apply a type of affine 2D transform that is not available through the other DirectComposition transform interfaces.</span></span> <span data-ttu-id="542d2-166">您可以藉由填妥 [**D2D \_ 矩陣 \_ 3X2 \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f) 結構，並將它傳遞至 [**IDCompositionMatrixTransform：： SetMatrix**](/windows/win32/api/dcomp/nf-dcomp-idcompositionmatrixtransform-setmatrix) 方法，來定義矩陣。</span><span class="sxs-lookup"><span data-stu-id="542d2-166">You define the matrix by filling a [**D2D\_MATRIX\_3X2\_F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f) structure and passing it to the [**IDCompositionMatrixTransform::SetMatrix**](/windows/win32/api/dcomp/nf-dcomp-idcompositionmatrixtransform-setmatrix) method.</span></span>

## <a name="transform-groups"></a><span data-ttu-id="542d2-167">轉換群組</span><span class="sxs-lookup"><span data-stu-id="542d2-167">Transform Groups</span></span>

<span data-ttu-id="542d2-168">您可以使用轉換群組，將多個轉換合併成一個。</span><span class="sxs-lookup"><span data-stu-id="542d2-168">You can use transform groups to combine multiple transforms into one.</span></span> <span data-ttu-id="542d2-169">轉換群組定義的轉換物件集合，其矩陣會以集合中指定的順序相乘。</span><span class="sxs-lookup"><span data-stu-id="542d2-169">A transform group defines a collection of transform objects whose matrices are multiplied together in the order in which they are specified in the collection.</span></span> <span data-ttu-id="542d2-170">接著會將產生的轉換矩陣套用至視覺效果。</span><span class="sxs-lookup"><span data-stu-id="542d2-170">The resulting transform matrix is then applied to the visual.</span></span> <span data-ttu-id="542d2-171">轉換群組會產生與個別套用每個轉換相同的結果。</span><span class="sxs-lookup"><span data-stu-id="542d2-171">A transform group produces the same result as applying each transform separately.</span></span>

<span data-ttu-id="542d2-172">請記住，轉換群組中的轉換物件順序很重要。</span><span class="sxs-lookup"><span data-stu-id="542d2-172">Keep in mind that the order of the transform objects in a transform group is important.</span></span> <span data-ttu-id="542d2-173">例如，如果先旋轉視覺效果，然後進行縮放，然後轉譯，結果會與第一次轉譯視覺效果，然後旋轉然後縮放的結果不同。</span><span class="sxs-lookup"><span data-stu-id="542d2-173">For example, if a visual is first rotated, then scaled, and then translated, the result is different than if the visual is first translated, then rotated, and then scaled.</span></span> <span data-ttu-id="542d2-174">DirectComposition 一律會依照在集合中指定的順序，將轉換套用至視覺效果。</span><span class="sxs-lookup"><span data-stu-id="542d2-174">DirectComposition always applies the transforms to a visual in the order in which they are specified in the collection.</span></span>

<span data-ttu-id="542d2-175">若要建立轉換群組，請先建立要包含在群組中的轉換物件，然後將轉換物件指標的陣列傳遞至 [**IDCompositionDevice：： CreateTransformGroup**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtransformgroup) 方法。</span><span class="sxs-lookup"><span data-stu-id="542d2-175">To create a transform group, first create the transform objects that you want to include in the group, and then pass an array of transform object pointers to the [**IDCompositionDevice::CreateTransformGroup**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtransformgroup) method.</span></span> <span data-ttu-id="542d2-176">建立轉換群組之後，您無法新增或移除任何轉換物件。</span><span class="sxs-lookup"><span data-stu-id="542d2-176">After you create a transform group, you cannot add or remove any transform objects.</span></span> <span data-ttu-id="542d2-177">不過，您可以修改集合中個別轉換物件的屬性，而變更將會反映在產生的轉換矩陣中。</span><span class="sxs-lookup"><span data-stu-id="542d2-177">However, you can modify the properties of the individual transform objects in the collection, and the changes will be reflected in the resulting transform matrix.</span></span>

## <a name="transform-animation"></a><span data-ttu-id="542d2-178">轉換動畫</span><span class="sxs-lookup"><span data-stu-id="542d2-178">Transform animation</span></span>

<span data-ttu-id="542d2-179">轉換的屬性可進行動畫。</span><span class="sxs-lookup"><span data-stu-id="542d2-179">The properties of a transform can be animated.</span></span> <span data-ttu-id="542d2-180">當屬性有動畫時，DirectComposition 會變更一段時間的屬性值，而不是一次全部變更。</span><span class="sxs-lookup"><span data-stu-id="542d2-180">When a property is animated, DirectComposition changes the value of the property over time, rather than all at once.</span></span> <span data-ttu-id="542d2-181">這在建立轉換時特別有用。</span><span class="sxs-lookup"><span data-stu-id="542d2-181">This is particularly useful when creating transitions.</span></span> <span data-ttu-id="542d2-182">如需詳細資訊，請參閱 [動畫](animation.md)。</span><span class="sxs-lookup"><span data-stu-id="542d2-182">For more information, see [Animation](animation.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="542d2-183">相關主題</span><span class="sxs-lookup"><span data-stu-id="542d2-183">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="542d2-184">DirectComposition 概念</span><span class="sxs-lookup"><span data-stu-id="542d2-184">DirectComposition Concepts</span></span>](directcomposition-concepts.md)
</dt> </dl>

 

 
