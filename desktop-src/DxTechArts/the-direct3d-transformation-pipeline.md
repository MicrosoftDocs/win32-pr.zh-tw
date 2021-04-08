---
title: Direct3D 轉換管線
description: 本文提供 Direct3D 應用程式開發人員如何藉由直接操作 Direct3D 矩陣來設定 Direct3D 轉換管線參數的技術說明。
ms.assetid: 48ae49f0-1162-c292-4bd4-34da5aadd2df
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2b97a87293a840ccd9641b1418c2005cf73a855
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/04/2021
ms.locfileid: "103853208"
---
# <a name="the-direct3d-transformation-pipeline"></a><span data-ttu-id="24abc-103">Direct3D 轉換管線</span><span class="sxs-lookup"><span data-stu-id="24abc-103">The Direct3D Transformation Pipeline</span></span>

<span data-ttu-id="24abc-104">本文提供 Direct3D 應用程式開發人員如何藉由直接操作 Direct3D 矩陣來設定 Direct3D 轉換管線參數的技術說明。</span><span class="sxs-lookup"><span data-stu-id="24abc-104">This article provides a technical explanation for Direct3D application developers on how to set the parameters of the Direct3D Transformation Pipeline by the direct manipulation of Direct3D matrices.</span></span>

-   [<span data-ttu-id="24abc-105">概觀</span><span class="sxs-lookup"><span data-stu-id="24abc-105">Overview</span></span>](#overview)
-   [<span data-ttu-id="24abc-106">轉換管線</span><span class="sxs-lookup"><span data-stu-id="24abc-106">The Transformation Pipeline</span></span>](#the-transformation-pipeline)
-   [<span data-ttu-id="24abc-107">使用秘訣</span><span class="sxs-lookup"><span data-stu-id="24abc-107">Usage Tips</span></span>](#usage-tips)

## <a name="overview"></a><span data-ttu-id="24abc-108">概觀</span><span class="sxs-lookup"><span data-stu-id="24abc-108">Overview</span></span>

<span data-ttu-id="24abc-109">Direct3D 使用三個轉換在像素座標（螢幕空間）中變更您的 3D 模型座標。</span><span class="sxs-lookup"><span data-stu-id="24abc-109">Direct3D uses three transformations to change your 3D model coordinates into pixel coordinates (screen space).</span></span> <span data-ttu-id="24abc-110">這些轉換為世界轉換、檢視轉換和投影轉換。</span><span class="sxs-lookup"><span data-stu-id="24abc-110">These transformations are world transform, view transform, and projection transform.</span></span>

<span data-ttu-id="24abc-111">「世界轉換」可控制如何將模型座標轉換成全局座標。</span><span class="sxs-lookup"><span data-stu-id="24abc-111">World transform controls how model coordinates are transformed into world coordinates.</span></span> <span data-ttu-id="24abc-112">全球轉換可以包含翻譯、旋轉和 scalings，但不適用於燈光。</span><span class="sxs-lookup"><span data-stu-id="24abc-112">World transform can include translations, rotations, and scalings, but it does not apply to lights.</span></span> <span data-ttu-id="24abc-113">如需有關使用世界轉換的詳細資訊，請參閱「 [世界轉換](/windows/desktop/direct3d9/world-transform)」。</span><span class="sxs-lookup"><span data-stu-id="24abc-113">For more information on working with world transforms, see [World Transform](/windows/desktop/direct3d9/world-transform).</span></span>

<span data-ttu-id="24abc-114">View 轉換控制從全局座標轉換成「相機空間」，以決定世界中的相機位置。</span><span class="sxs-lookup"><span data-stu-id="24abc-114">View transform controls the transition from world coordinates into "camera space," determining camera position in the world.</span></span> <span data-ttu-id="24abc-115">如需使用 view 轉換的範例，請參閱 [視圖轉換](/windows/desktop/direct3d9/view-transform)。</span><span class="sxs-lookup"><span data-stu-id="24abc-115">For an example of working with view transforms, see [View Transform](/windows/desktop/direct3d9/view-transform).</span></span>

<span data-ttu-id="24abc-116">投影轉換會將幾何從相機空間變更為「剪輯空間」，並套用透視扭曲。</span><span class="sxs-lookup"><span data-stu-id="24abc-116">Projection transform changes the geometry from camera space into "clip space" and applies perspective distortion.</span></span> <span data-ttu-id="24abc-117">「剪輯空間」一詞是指在此轉換期間將幾何裁剪到視圖磁片區的方式。</span><span class="sxs-lookup"><span data-stu-id="24abc-117">The term "clip space" refers to how the geometry is clipped to the view volume during this transform.</span></span> <span data-ttu-id="24abc-118">如需使用投影轉換的範例，請參閱 [投射轉換](/windows/desktop/direct3d9/projection-transform)。</span><span class="sxs-lookup"><span data-stu-id="24abc-118">For an example of working with projection transforms, see [Projection Transform](/windows/desktop/direct3d9/projection-transform).</span></span>

<span data-ttu-id="24abc-119">最後，裁剪空間中的幾何會轉換成圖元座標， (螢幕空間) 。</span><span class="sxs-lookup"><span data-stu-id="24abc-119">Finally, the geometry in clip space is transformed into pixel coordinates (screen space).</span></span> <span data-ttu-id="24abc-120">這項轉換是由 [視口] 設定所控制。</span><span class="sxs-lookup"><span data-stu-id="24abc-120">This transformation is controlled by the viewport settings.</span></span>

<span data-ttu-id="24abc-121">剪切和轉換頂點必須在同質空間中進行 (單純放置的空間、座標系統) 包含第四個元素的空間，但大部分應用程式的最終結果都必須是「螢幕空間」中所定義的非同質三維 (3D) 座標。</span><span class="sxs-lookup"><span data-stu-id="24abc-121">Clipping and transforming vertices must take place in homogenous space (simply put, space in which the coordinate system includes a fourth element), but the final result for most applications needs to be non-homogenous three-dimensional (3D) coordinates defined in "screen space."</span></span> <span data-ttu-id="24abc-122">這表示輸入頂點和裁剪磁片區必須轉譯成同質空間，才能執行裁剪，然後轉譯回非同質空間來顯示。</span><span class="sxs-lookup"><span data-stu-id="24abc-122">This means that both the input vertices and the clipping volume must be translated into homogenous space to perform the clipping and then translated back into non-homogenous space to be displayed.</span></span>

<span data-ttu-id="24abc-123">這三個 Direct3D 轉換（世界、觀點和投射轉換）都是由 Direct3D 矩陣所定義。</span><span class="sxs-lookup"><span data-stu-id="24abc-123">The three Direct3D transformations-world, view, and projection transform-are defined by Direct3D matrices.</span></span> <span data-ttu-id="24abc-124">Direct3D 矩陣是 [**D3DMATRIX**](/windows/desktop/direct3d9/d3dmatrix) 結構所定義的4x4 同質矩陣。</span><span class="sxs-lookup"><span data-stu-id="24abc-124">A Direct3D matrix is a 4x4 homogenous matrix defined by a [**D3DMATRIX**](/windows/desktop/direct3d9/d3dmatrix) structure.</span></span> <span data-ttu-id="24abc-125">雖然 Direct3D 矩陣不是標準物件，但它們並不是由 COM 介面表示，您可以建立和設定它們，就像是任何其他 Direct3D 物件一樣。</span><span class="sxs-lookup"><span data-stu-id="24abc-125">Although Direct3D matrices are not standard objects-they are not represented by a COM interface-you can create and set them just as you would any other Direct3D object.</span></span> <span data-ttu-id="24abc-126">如需 Direct3D 矩陣的詳細資訊，請參閱 [轉換](/windows/desktop/direct3d9/transforms)。</span><span class="sxs-lookup"><span data-stu-id="24abc-126">For more information on Direct3D matrices, see [Transforms](/windows/desktop/direct3d9/transforms).</span></span>

## <a name="the-transformation-pipeline"></a><span data-ttu-id="24abc-127">轉換管線</span><span class="sxs-lookup"><span data-stu-id="24abc-127">The Transformation Pipeline</span></span>

<span data-ttu-id="24abc-128">如果模型座標中的頂點是由 Pm = (Xm、Ym、Zm、1) ，則下圖中顯示的轉換會套用到計算畫面座標 Ps = (Xs、Y) 、Zs、Ws) 。</span><span class="sxs-lookup"><span data-stu-id="24abc-128">If a vertex in the model coordinate is given by Pm = (Xm, Ym, Zm, 1), then the transformations shown in the following figure are applied to compute screen coordinates Ps = (Xs, Ys, Zs, Ws).</span></span>

![螢幕空間轉換的模型空間](images/d3dxfrm61.gif)

<span data-ttu-id="24abc-130">以下是上圖所示的階段說明：</span><span class="sxs-lookup"><span data-stu-id="24abc-130">Here are descriptions of the stages that are shown in the preceding figure:</span></span>

1.  <span data-ttu-id="24abc-131">世界矩陣 Mworld 會將頂點從模型空間轉換成世界空間。</span><span class="sxs-lookup"><span data-stu-id="24abc-131">World matrix Mworld transforms vertices from the model space to the world space.</span></span> <span data-ttu-id="24abc-132">此矩陣的設定方式如下：</span><span class="sxs-lookup"><span data-stu-id="24abc-132">This matrix is set by:</span></span>

    ``` syntax
        d3dDevice->SetTransform (D3DTRANSFORMSTATE_WORLD, matrix address) 
    ```

    <span data-ttu-id="24abc-133">Direct3D 的執行假設這個矩陣的最後一個資料行是 (0、0、0、1) 。</span><span class="sxs-lookup"><span data-stu-id="24abc-133">Direct3D implementation assumes that the last column of this matrix is (0, 0, 0, 1).</span></span> <span data-ttu-id="24abc-134">如果使用者指定的矩陣具有不同的最後一個資料行，但光源和模糊不正確，則不會傳回任何錯誤。</span><span class="sxs-lookup"><span data-stu-id="24abc-134">No error is returned if the user specifies a matrix with a different last column, but the lighting and fog will be incorrect.</span></span>

2.  <span data-ttu-id="24abc-135">視圖矩陣 Mview 會將頂點從世界空間轉換成相機空間。</span><span class="sxs-lookup"><span data-stu-id="24abc-135">View matrix Mview transforms vertices from the world space to the camera space.</span></span> <span data-ttu-id="24abc-136">此矩陣的設定方式如下：</span><span class="sxs-lookup"><span data-stu-id="24abc-136">This matrix is set by:</span></span>

    ``` syntax
        d3dDevice->SetTransform (D3DTRANSFORMSTATE_VIEW, matrix address) 
    ```

    <span data-ttu-id="24abc-137">Direct3D 的執行假設這個矩陣的最後一個資料行是 (0、0、0、1) 。</span><span class="sxs-lookup"><span data-stu-id="24abc-137">Direct3D implementation assumes that the last column of this matrix is (0, 0, 0, 1).</span></span> <span data-ttu-id="24abc-138">如果使用者指定的矩陣具有不同的最後一個資料行，但光源和模糊不正確，則不會傳回任何錯誤。</span><span class="sxs-lookup"><span data-stu-id="24abc-138">No error is returned if the user specifies a matrix with different last column, but the lighting and fog will be incorrect.</span></span>

3.  <span data-ttu-id="24abc-139">投射矩陣 Mproj 會將頂點從相機空間轉換成投射空間。</span><span class="sxs-lookup"><span data-stu-id="24abc-139">Projection matrix Mproj transforms vertices from the camera space to the projection space.</span></span> <span data-ttu-id="24abc-140">此矩陣的設定方式如下：</span><span class="sxs-lookup"><span data-stu-id="24abc-140">This matrix is set by:</span></span>

    ``` syntax
        d3dDevice->SetTransform (D3DTRANSFORMSTATE_PROJECTION, matrix address) 
    ```

    <span data-ttu-id="24abc-141">投射矩陣的最後一個資料行應該是 (0、0、1、0) 或 (0、0、a、0) ，以取得正確的霧化和光源效果;建議 (0、0、1、0) 表單。</span><span class="sxs-lookup"><span data-stu-id="24abc-141">The last column of the projection matrix should be (0, 0, 1, 0), or (0, 0, a, 0) for correct fog and lighting effects; (0, 0, 1, 0) form is preferred.</span></span>

    <span data-ttu-id="24abc-142">在投影空間中，所有點的剪輯磁片區都是 Xp = (Xp、Yp、Zp、Wp) 定義為：</span><span class="sxs-lookup"><span data-stu-id="24abc-142">Clipping volume for all points Xp = (Xp, Yp, Zp, Wp) in the projection space is defined as:</span></span>

    ``` syntax
        -Wp < Xp <= Wp 
        -Wp < Yp <= Wp 
        0 < Zp <= Wp 
    ```

    <span data-ttu-id="24abc-143">不滿足這些方程式的所有點都將會被裁剪。</span><span class="sxs-lookup"><span data-stu-id="24abc-143">All points that do not satisfy these equations will be clipped.</span></span>

    <span data-ttu-id="24abc-144">如果視圖磁片區定義為：</span><span class="sxs-lookup"><span data-stu-id="24abc-144">If a view volume is defined as:</span></span>

    -   <span data-ttu-id="24abc-145">在接近裁剪平面之相機空間中的 Sw 螢幕視窗寬度</span><span class="sxs-lookup"><span data-stu-id="24abc-145">Sw-screen window width in camera space in near clipping plane</span></span>
    -   <span data-ttu-id="24abc-146">Sh-接近裁剪平面之相機空間中的螢幕視窗高度</span><span class="sxs-lookup"><span data-stu-id="24abc-146">Sh-screen window height in camera space in near clipping plane</span></span>
    -   <span data-ttu-id="24abc-147">Zn-沿著相機空間中的 Z 軸距離接近裁剪平面的距離</span><span class="sxs-lookup"><span data-stu-id="24abc-147">Zn-distance to the near clipping plane along Z axes in camera space</span></span>
    -   <span data-ttu-id="24abc-148">Zf-沿著相機空間中的 Z 軸距離到最遠的裁剪平面</span><span class="sxs-lookup"><span data-stu-id="24abc-148">Zf-distance to the far clipping plane along Z axes in camera space</span></span>

    <span data-ttu-id="24abc-149">然後可以撰寫透視圖投影矩陣，如下所示：</span><span class="sxs-lookup"><span data-stu-id="24abc-149">then a perspective projection matrix could be written as follows:</span></span>

    ![顯示透視圖投影矩陣。](images/d3dxfrm62.gif)

    <span data-ttu-id="24abc-151">其中 Mij 是 Mproj 的成員。</span><span class="sxs-lookup"><span data-stu-id="24abc-151">where Mij are members of Mproj.</span></span>

    <span data-ttu-id="24abc-152">針對正向投射，我們有：</span><span class="sxs-lookup"><span data-stu-id="24abc-152">For the orthogonal projection we have:</span></span>

    ![正向投射](images/d3dxfrm63.gif)

    <span data-ttu-id="24abc-154">Direct3D 假設透視圖投影矩陣的形式如下：</span><span class="sxs-lookup"><span data-stu-id="24abc-154">Direct3D assumes that the perspective projection matrix has the form:</span></span>

    ![透視圖投影矩陣](images/d3dxfrm64.gif)

    <span data-ttu-id="24abc-156">如果透視圖投影矩陣沒有此表單，則會有一些成品。</span><span class="sxs-lookup"><span data-stu-id="24abc-156">If the perspective projection matrix does not have this form, there will be some artifacts.</span></span> <span data-ttu-id="24abc-157">例如，資料表霧化將無法運作。</span><span class="sxs-lookup"><span data-stu-id="24abc-157">For example, table fog will not work.</span></span>

4.  <span data-ttu-id="24abc-158">Direct3D 可讓使用者變更剪輯磁片區，如下所示：</span><span class="sxs-lookup"><span data-stu-id="24abc-158">Direct3D allows the user to change the clip volume as follows:</span></span>

    ![變更剪輯音量](images/d3dxfrm65.gif)

    <span data-ttu-id="24abc-160">這可以重寫為：</span><span class="sxs-lookup"><span data-stu-id="24abc-160">This can be rewritten as:</span></span>

    ![變更剪輯磁片區重寫](images/d3dxfrm66.gif)

    <span data-ttu-id="24abc-162">其中：</span><span class="sxs-lookup"><span data-stu-id="24abc-162">where:</span></span>

    ``` syntax
        Cx, Cy - dvClipX, dvClipY from D3DVIEWPORT9  
        Cw, Ch - dvClipWidth, dvClipHeight from D3DVIEWPORT9  
        Zmin, Zmax - dvMinZ, dvMaxZ from D3DVIEWPORT9  
    ```

    <span data-ttu-id="24abc-163">這項轉換可以提供更高的精確度，而且相當於調整和移動剪切的磁片區。</span><span class="sxs-lookup"><span data-stu-id="24abc-163">This transformation can provide increased precision and is equivalent to scaling and shifting the clipping volume.</span></span>

    <span data-ttu-id="24abc-164">對應的 Mclip 矩陣為：</span><span class="sxs-lookup"><span data-stu-id="24abc-164">The corresponding Mclip matrix is:</span></span>

    ![mclip 矩陣](images/d3dxfrm67.gif)

    <span data-ttu-id="24abc-166">頂點的轉換方式如下：</span><span class="sxs-lookup"><span data-stu-id="24abc-166">A vertex is transformed by:</span></span>

    ``` syntax
        dvClipWidth = 2   
        dvClipHeight = 2   
        dvClipX = -1   
        dvClipY = 1   
        dvMinZ = 0   
        dvMaxZ = 1   
    ```

    <span data-ttu-id="24abc-167">如果您不想要調整剪輯磁片區，您可以將資料區參數設定為預設值：</span><span class="sxs-lookup"><span data-stu-id="24abc-167">If you do not want to scale the clip volume, you can set viewport parameters to default values:</span></span>

    ``` syntax
        (Xc, Yc, Zc, Wc) = (Xp, Yp, Zp, Wp) * Mclip   
    ```

5.  <span data-ttu-id="24abc-168">如果使用者 \_ 在 DrawPrimitive 呼叫中指定 D3DDP DONOTCLIP 旗標，則裁剪階段是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="24abc-168">The clipping stage is optional if the user specifies the D3DDP\_DONOTCLIP flag in a DrawPrimitive call.</span></span> <span data-ttu-id="24abc-169">在此情況下，可以結合所有矩陣 (包括 Mvs) 。</span><span class="sxs-lookup"><span data-stu-id="24abc-169">In this case, all matrices (including Mvs) can be combined.</span></span>
6.  <span data-ttu-id="24abc-170">區形調整矩陣 Mvs 會將座標調整為位於 [視口] 視窗內，並將 Y 軸從最多向下翻轉：</span><span class="sxs-lookup"><span data-stu-id="24abc-170">The viewport scale matrix Mvs scales coordinates to be within the viewport window and flips the Y axis from up to down:</span></span>

    ![視口調整矩陣 mvs](images/d3dxfrm68.gif)

    <span data-ttu-id="24abc-172">其中：</span><span class="sxs-lookup"><span data-stu-id="24abc-172">where:</span></span>

    ``` syntax
        dwX, dwY - viewport offsets in pixels from D3DVIEWPORT9 
        dwWidth, dwHeight - viewport width and height in pixels from D3DVIEWPORT9    
    ```

7.  <span data-ttu-id="24abc-173">最後，會計算螢幕座標，並將其傳遞至轉譯器：</span><span class="sxs-lookup"><span data-stu-id="24abc-173">Finally, screen coordinates are computed and passed to the rasterizer:</span></span>

    ![計算並傳遞至轉譯器的螢幕座標](images/d3dxfrm69.gif)

## <a name="usage-tips"></a><span data-ttu-id="24abc-175">使用秘訣</span><span class="sxs-lookup"><span data-stu-id="24abc-175">Usage Tips</span></span>

<span data-ttu-id="24abc-176">以下是如何使用 Direct3D 轉換管線的一些秘訣：</span><span class="sxs-lookup"><span data-stu-id="24abc-176">Here are some tips for how to use the Direct3D Transformation Pipeline:</span></span>

-   <span data-ttu-id="24abc-177">世界上的最後一個資料行和視圖矩陣應該是 (0、0、0、1) ，否則光源將會不正確。</span><span class="sxs-lookup"><span data-stu-id="24abc-177">The last column of the world and view matrices should be (0, 0, 0, 1), or the lighting will be incorrect.</span></span>
-   <span data-ttu-id="24abc-178">除非您完全瞭解所需的內容，否則請將 [視口] 參數設定為 [建立身分識別 Mclip 矩陣]。</span><span class="sxs-lookup"><span data-stu-id="24abc-178">Set the viewport parameters to build an identity Mclip matrix, unless you understand exactly what it is needed for.</span></span>

    ``` syntax
        dvClipWidth = 2 
        dvClipHeight = 2
        dvClipX = -1
        dvClipY = 1
        dvMinZ = 0 
        dvMaxZ = 1
    ```

 

 