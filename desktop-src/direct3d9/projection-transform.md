---
description: 您可以將投影轉換視為控制攝影機的內部;它類似于選擇相機的鏡頭。
ms.assetid: 09e6e887-7657-4654-be19-2e83dcbc91cf
title: " (Direct3D 9) 的投射轉換"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37b518583dd534bec9784590150233847274ca71
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104187496"
---
# <a name="projection-transform-direct3d-9"></a><span data-ttu-id="c0e5c-103"> (Direct3D 9) 的投射轉換</span><span class="sxs-lookup"><span data-stu-id="c0e5c-103">Projection Transform (Direct3D 9)</span></span>

<span data-ttu-id="c0e5c-104">您可以將投影轉換視為控制攝影機的內部;它類似于選擇相機的鏡頭。</span><span class="sxs-lookup"><span data-stu-id="c0e5c-104">You can think of the projection transformation as controlling the camera's internals; it is analogous to choosing a lens for the camera.</span></span> <span data-ttu-id="c0e5c-105">這是三種轉換類型中最複雜的轉換。</span><span class="sxs-lookup"><span data-stu-id="c0e5c-105">This is the most complicated of the three transformation types.</span></span> <span data-ttu-id="c0e5c-106">這項投射轉換的討論區分為下列主題。</span><span class="sxs-lookup"><span data-stu-id="c0e5c-106">This discussion of the projection transformation is organized into the following topics.</span></span>

<span data-ttu-id="c0e5c-107">投影矩陣通常是縮放和透視投影。</span><span class="sxs-lookup"><span data-stu-id="c0e5c-107">The projection matrix is typically a scale and perspective projection.</span></span> <span data-ttu-id="c0e5c-108">投影轉換會將檢視範圍轉換成立方體形狀。</span><span class="sxs-lookup"><span data-stu-id="c0e5c-108">The projection transformation converts the viewing frustum into a cuboid shape.</span></span> <span data-ttu-id="c0e5c-109">由於檢視範圍的近端小於遠端，這會影響靠近相機之物體的展開；這也是透視套用到場景的方式。</span><span class="sxs-lookup"><span data-stu-id="c0e5c-109">Because the near end of the viewing frustum is smaller than the far end, this has the effect of expanding objects that are near to the camera; this is how perspective is applied to the scene.</span></span>

<span data-ttu-id="c0e5c-110">在[檢視範圍](viewports-and-clipping.md)中，相機和檢視範圍空間的原點之間的距離隨意定義為 D，以便投影矩陣看起來如下圖。</span><span class="sxs-lookup"><span data-stu-id="c0e5c-110">In [the viewing frustum](viewports-and-clipping.md), the distance between the camera and the origin of the viewing transform space is defined arbitrarily as D, so the projection matrix looks like the following illustration.</span></span>

![投影矩陣的圖例](images/projmat1.png)

<span data-ttu-id="c0e5c-112">檢視矩陣會透過在 z 方向平移 - D 將相機轉移至原點，轉移矩陣就如下圖。</span><span class="sxs-lookup"><span data-stu-id="c0e5c-112">The viewing matrix translates the camera to the origin by translating in the z direction by - D. The translation matrix is like the following illustration.</span></span>

![轉移矩陣的圖例](images/projmat2.png)

<span data-ttu-id="c0e5c-114">將平移矩陣乘以投射矩陣 (T \* P) 會提供複合投射矩陣，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="c0e5c-114">Multiplying the translation matrix by the projection matrix (T\*P) gives the composite projection matrix, as shown in the following illustration.</span></span>

![複合投影矩陣的圖例](images/projmat3.png)

<span data-ttu-id="c0e5c-116">透視轉換會將檢視範圍轉換成新的座標空間。</span><span class="sxs-lookup"><span data-stu-id="c0e5c-116">The perspective transform converts a viewing frustum into a new coordinate space.</span></span> <span data-ttu-id="c0e5c-117">請注意，範圍會變成立方體，而原點也會從場景的右上角移到中心，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="c0e5c-117">Notice that the frustum becomes cuboid and also that the origin moves from the upper-right corner of the scene to the center, as shown in the following diagram.</span></span>

![透視轉換如何將檢視範圍變更為新的座標空間的圖表](images/cuboid.png)

<span data-ttu-id="c0e5c-119">在透視轉換中，x 方向與 y 方向的限制是 -1 及 1。</span><span class="sxs-lookup"><span data-stu-id="c0e5c-119">In the perspective transform, the limits of the x- and y-directions are -1 and 1.</span></span> <span data-ttu-id="c0e5c-120">對於正面平面 z 方向的限制是 0 而對於後面平面是 1。</span><span class="sxs-lookup"><span data-stu-id="c0e5c-120">The limits of the z-direction are 0 for the front plane and 1 for the back plane.</span></span>

<span data-ttu-id="c0e5c-121">這個矩陣會根據從相機到近裁剪平面的指定距離平移和縮放物件，但是不會考慮視野 (fov)，而且在距離中對於物件產生的 z 值可能幾乎相同，使得難以比較深度。</span><span class="sxs-lookup"><span data-stu-id="c0e5c-121">This matrix translates and scales objects based on a specified distance from the camera to the near clipping plane, but it doesn't consider the field of view (fov), and the z-values that it produces for objects in the distance can be nearly identical, making depth comparisons difficult.</span></span> <span data-ttu-id="c0e5c-122">下列矩陣處理這些問題，並且調整頂點以考慮檢視區的長寬比，使其成為透視投影的不錯選擇。</span><span class="sxs-lookup"><span data-stu-id="c0e5c-122">The following matrix addresses these issues, and it adjusts vertices to account for the aspect ratio of the viewport, making it a good choice for the perspective projection.</span></span>

![透視投影的矩陣圖例](images/prjmatx1.png)

<span data-ttu-id="c0e5c-124">在這個矩陣中，Zₙ 是近裁剪平面的 z 值。</span><span class="sxs-lookup"><span data-stu-id="c0e5c-124">In this matrix, Zₙ is the z-value of the near clipping plane.</span></span> <span data-ttu-id="c0e5c-125">變數 w、h 和 Q 的意義如下。</span><span class="sxs-lookup"><span data-stu-id="c0e5c-125">The variables w, h, and Q have the following meanings.</span></span> <span data-ttu-id="c0e5c-126">請注意，fov<sub>w</sub>和 fovₖ 以弧度代表區檢視區的水平和垂直視野。</span><span class="sxs-lookup"><span data-stu-id="c0e5c-126">Note that fov<sub>w</sub> and fovₖ represent the viewport's horizontal and vertical fields of view, in radians.</span></span>

![變數的方程式意義](images/prjmatx2.png)

<span data-ttu-id="c0e5c-128">對於您的應用程式，使用視野角度來定義 x 和 y 縮放係數，可能不如使用檢視區的水平和垂直維度 (在相機空間中) 來得便利。</span><span class="sxs-lookup"><span data-stu-id="c0e5c-128">For your application, using field-of-view angles to define the x- and y-scaling coefficients might not be as convenient as using the viewport's horizontal and vertical dimensions (in camera space).</span></span> <span data-ttu-id="c0e5c-129">既然數學解出來，下列 w 和 h 的兩個方程式使用檢視區的維度，並且相當於前述方程式。</span><span class="sxs-lookup"><span data-stu-id="c0e5c-129">As the math works out, the following two equations for w and h use the viewport's dimensions, and are equivalent to the preceding equations.</span></span>

![W 和 h 變數的方程式意義](images/prjmatx3.png)

<span data-ttu-id="c0e5c-131">在這些公式中，Zₙ 代表近裁剪平面的位置，而 V<sub>w</sub>和 Vₕ 變數代表檢視區的寬度與高度 (照相機空間中)。</span><span class="sxs-lookup"><span data-stu-id="c0e5c-131">In these formulas, Zₙ represents the position of the near clipping plane, and the V<sub>w</sub> and Vₕ variables represent the width and height of the viewport, in camera space.</span></span>

<span data-ttu-id="c0e5c-132">若是 c + + 應用程式，這兩個維度會直接對應至 [**D3DVIEWPORT9**](d3dviewport9.md) 結構的寬度和高度成員。</span><span class="sxs-lookup"><span data-stu-id="c0e5c-132">For a C++ application, these two dimensions correspond directly to the Width and Height members of the [**D3DVIEWPORT9**](d3dviewport9.md) structure.</span></span>

<span data-ttu-id="c0e5c-133">不論您決定使用哪個公式，務必將 Zₙ 設定為越大值越好，因為 z 值非常接近相機，不會差太多。</span><span class="sxs-lookup"><span data-stu-id="c0e5c-133">Whatever formula you decide to use, be sure to set Zₙ to as large a value as possible, because z-values extremely close to the camera don't vary by much.</span></span> <span data-ttu-id="c0e5c-134">這會使得使用 16 位元 z 緩衝區的深度比較變得有些複雜。</span><span class="sxs-lookup"><span data-stu-id="c0e5c-134">This makes depth comparisons using 16-bit z-buffers somewhat complicated.</span></span>

<span data-ttu-id="c0e5c-135">如同「世界」和「視圖」轉換，您可以呼叫 [**IDirect3DDevice9：： SetTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform) 方法來設定投影轉換。</span><span class="sxs-lookup"><span data-stu-id="c0e5c-135">As with the world and view transformations, you call the [**IDirect3DDevice9::SetTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform) method to set the projection transform.</span></span>

## <a name="setting-up-a-projection-matrix"></a><span data-ttu-id="c0e5c-136">設定投射矩陣</span><span class="sxs-lookup"><span data-stu-id="c0e5c-136">Setting Up a Projection Matrix</span></span>

<span data-ttu-id="c0e5c-137">下列 ProjectionMatrix 範例函式會設定 front 和 back 裁剪平面，以及視角的水準和垂直欄位。</span><span class="sxs-lookup"><span data-stu-id="c0e5c-137">The following ProjectionMatrix sample function sets the front and back clipping planes, as well as the horizontal and vertical field of view angles.</span></span> <span data-ttu-id="c0e5c-138">View 的欄位應小於 pi 弧度。</span><span class="sxs-lookup"><span data-stu-id="c0e5c-138">The fields of view should be less than pi radians.</span></span>


```
D3DXMATRIX 
ProjectionMatrix(const float near_plane, // Distance to near clipping 
                                         // plane
                 const float far_plane,  // Distance to far clipping 
                                         // plane
                 const float fov_horiz,  // Horizontal field of view 
                                         // angle, in radians
                 const float fov_vert)   // Vertical field of view 
                                         // angle, in radians
{
    float    h, w, Q;

    w = (float)1/tan(fov_horiz*0.5);  // 1/tan(x) == cot(x)
    h = (float)1/tan(fov_vert*0.5);   // 1/tan(x) == cot(x)
    Q = far_plane/(far_plane - near_plane);

    D3DXMATRIX ret;
    ZeroMemory(&ret, sizeof(ret));

    ret(0, 0) = w;
    ret(1, 1) = h;
    ret(2, 2) = Q;
    ret(3, 2) = -Q*near_plane;
    ret(2, 3) = 1;
    return ret;
}   // End of ProjectionMatrix
```



<span data-ttu-id="c0e5c-139">建立矩陣之後，請使用 [**IDirect3DDevice9：： SetTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform) 指定 D3DTS 投射來設定它 \_ 。</span><span class="sxs-lookup"><span data-stu-id="c0e5c-139">After creating the matrix, set it with [**IDirect3DDevice9::SetTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform) specifying D3DTS\_PROJECTION.</span></span>

<span data-ttu-id="c0e5c-140">D3DX 公用程式程式庫提供下列功能，協助您設定投影矩陣。</span><span class="sxs-lookup"><span data-stu-id="c0e5c-140">The D3DX utility library provides the following functions to help you set up your projection matrix.</span></span>

-   [<span data-ttu-id="c0e5c-141">**D3DXMatrixPerspectiveLH**</span><span class="sxs-lookup"><span data-stu-id="c0e5c-141">**D3DXMatrixPerspectiveLH**</span></span>](d3dxmatrixperspectivelh.md)
-   [<span data-ttu-id="c0e5c-142">**D3DXMatrixPerspectiveRH**</span><span class="sxs-lookup"><span data-stu-id="c0e5c-142">**D3DXMatrixPerspectiveRH**</span></span>](d3dxmatrixperspectiverh.md)
-   [<span data-ttu-id="c0e5c-143">**D3DXMatrixPerspectiveFovLH**</span><span class="sxs-lookup"><span data-stu-id="c0e5c-143">**D3DXMatrixPerspectiveFovLH**</span></span>](d3dxmatrixperspectivefovlh.md)
-   [<span data-ttu-id="c0e5c-144">**D3DXMatrixPerspectiveFovRH**</span><span class="sxs-lookup"><span data-stu-id="c0e5c-144">**D3DXMatrixPerspectiveFovRH**</span></span>](d3dxmatrixperspectivefovrh.md)
-   [<span data-ttu-id="c0e5c-145">**D3DXMatrixPerspectiveOffCenterLH**</span><span class="sxs-lookup"><span data-stu-id="c0e5c-145">**D3DXMatrixPerspectiveOffCenterLH**</span></span>](d3dxmatrixperspectiveoffcenterlh.md)
-   [<span data-ttu-id="c0e5c-146">**D3DXMatrixPerspectiveOffCenterRH**</span><span class="sxs-lookup"><span data-stu-id="c0e5c-146">**D3DXMatrixPerspectiveOffCenterRH**</span></span>](d3dxmatrixperspectiveoffcenterrh.md)

## <a name="a-w-friendly-projection-matrix"></a><span data-ttu-id="c0e5c-147">易記投影矩陣</span><span class="sxs-lookup"><span data-stu-id="c0e5c-147">A W-Friendly Projection Matrix</span></span>

<span data-ttu-id="c0e5c-148">Direct3D 可使用已被世界、檢視和投影矩陣轉換的 w 元件頂點，來執行深度緩衝區的深度計算或霧的效果。</span><span class="sxs-lookup"><span data-stu-id="c0e5c-148">Direct3D can use the w-component of a vertex that has been transformed by the world, view, and projection matrices to perform depth-based calculations in depth-buffer or fog effects.</span></span> <span data-ttu-id="c0e5c-149">這類運算需要投影矩陣將 w 標準化為等於世界空間 z。</span><span class="sxs-lookup"><span data-stu-id="c0e5c-149">Computations such as these require that your projection matrix normalize w to be equivalent to world-space z.</span></span> <span data-ttu-id="c0e5c-150">簡言之，如果您的投影矩陣包含不是 1 的 (3,4) 係數，您必須透過反轉 (3,4) 係數來縮放所有係數以製作適當的矩陣。</span><span class="sxs-lookup"><span data-stu-id="c0e5c-150">In short, if your projection matrix includes a (3,4) coefficient that is not 1, you must scale all the coefficients by the inverse of the (3,4) coefficient to make a proper matrix.</span></span> <span data-ttu-id="c0e5c-151">如果您不提供相符的矩陣，霧效果和深度緩衝區就不會正確套用。</span><span class="sxs-lookup"><span data-stu-id="c0e5c-151">If you don't provide a compliant matrix, fog effects and depth buffering are not applied correctly.</span></span>

<span data-ttu-id="c0e5c-152">下圖顯示不相符的投影矩陣和縮放的矩陣，所以將會啟用眼睛相關的霧化。</span><span class="sxs-lookup"><span data-stu-id="c0e5c-152">The following illustration shows a noncompliant projection matrix, and the same matrix scaled so that eye-relative fog will be enabled.</span></span>

![不相符投影矩陣及具有眼睛相關霧化的矩陣圖例](images/eyerlmx.png)

<span data-ttu-id="c0e5c-154">在前述矩陣中，所有變數都假設為非零。</span><span class="sxs-lookup"><span data-stu-id="c0e5c-154">In the preceding matrices, all variables are assumed to be nonzero.</span></span> <span data-ttu-id="c0e5c-155">如需眼睛相關模糊的詳細資訊，請參閱 [眼睛相關與以 Z 為基礎的深度](pixel-fog.md)。</span><span class="sxs-lookup"><span data-stu-id="c0e5c-155">For more information about eye-relative fog, see [Eye-Relative vs. Z-Based Depth](pixel-fog.md).</span></span> <span data-ttu-id="c0e5c-156">如需以 w 為基礎深度緩衝的詳細資訊，請參閱 [ (Direct3D 9) 的深度緩衝區 ](depth-buffers.md)。</span><span class="sxs-lookup"><span data-stu-id="c0e5c-156">For information about w-based depth buffering, see [Depth Buffers (Direct3D 9)](depth-buffers.md).</span></span>

<span data-ttu-id="c0e5c-157">Direct3D 使用目前以 w 型深度計算的投影矩陣。</span><span class="sxs-lookup"><span data-stu-id="c0e5c-157">Direct3D uses the currently set projection matrix in its w-based depth calculations.</span></span> <span data-ttu-id="c0e5c-158">如此一來，應用程式必須設定相符的投影矩陣，才能接收所要的 w 型功能，即使它們不使用 Direct3D 進行轉換。</span><span class="sxs-lookup"><span data-stu-id="c0e5c-158">As a result, applications must set a compliant projection matrix to receive the desired w-based features, even if they do not use Direct3D for transforms.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c0e5c-159">相關主題</span><span class="sxs-lookup"><span data-stu-id="c0e5c-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c0e5c-160">轉換</span><span class="sxs-lookup"><span data-stu-id="c0e5c-160">Transforms</span></span>](transforms.md)
</dt> </dl>

 

 
