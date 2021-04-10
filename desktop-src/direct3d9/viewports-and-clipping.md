---
description: 就概念而言，視口是投影出3D 場景的二維 (2D) 矩形。
ms.assetid: eddadaa1-9181-47fa-8530-44aa46fea286
title: " (Direct3D 9) 的區形和剪切"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d57f64d17f7abf4e370406f984fa50037be6d44e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108396"
---
# <a name="viewports-and-clipping-direct3d-9"></a><span data-ttu-id="d650e-103"> (Direct3D 9) 的區形和剪切</span><span class="sxs-lookup"><span data-stu-id="d650e-103">Viewports and Clipping (Direct3D 9)</span></span>

<span data-ttu-id="d650e-104">就概念而言，視口是投影出3D 場景的二維 (2D) 矩形。</span><span class="sxs-lookup"><span data-stu-id="d650e-104">Conceptually, a viewport is a two-dimensional (2D) rectangle into which a 3D scene is projected.</span></span> <span data-ttu-id="d650e-105">在 Direct3D 中，矩形在 Direct3D 表面中以座標的形式存在，系統會使用矩形作為轉譯目標。</span><span class="sxs-lookup"><span data-stu-id="d650e-105">In Direct3D, the rectangle exists as coordinates within a Direct3D surface that the system uses as a rendering target.</span></span> <span data-ttu-id="d650e-106">投影轉換將頂點轉換至用於檢視區的座標系統。</span><span class="sxs-lookup"><span data-stu-id="d650e-106">The projection transformation converts vertices into the coordinate system used for the viewport.</span></span> <span data-ttu-id="d650e-107">檢視區也用於指定轉譯目標表面 (場景轉譯目標) 上深度值的範圍 (通常是 0.0 到 1.0)。</span><span class="sxs-lookup"><span data-stu-id="d650e-107">A viewport is also used to specify the range of depth values on a render-target surface into which a scene will be rendered (usually 0.0 to 1.0).</span></span>

## <a name="the-viewing-frustum"></a><span data-ttu-id="d650e-108">檢視範圍</span><span class="sxs-lookup"><span data-stu-id="d650e-108">The Viewing Frustum</span></span>

<span data-ttu-id="d650e-109">檢視範圍是場景中相對於檢視區相機放置的 3D 體積。</span><span class="sxs-lookup"><span data-stu-id="d650e-109">A viewing frustum is 3D volume in a scene positioned relative to the viewport's camera.</span></span> <span data-ttu-id="d650e-110">體積形狀影響模型如何從相機空間投影到螢幕。</span><span class="sxs-lookup"><span data-stu-id="d650e-110">The shape of the volume affects how models are projected from camera space onto the screen.</span></span> <span data-ttu-id="d650e-111">最常見的投射類型，透視投影，負責讓靠近相機的物件看起來比遠方物件更大。</span><span class="sxs-lookup"><span data-stu-id="d650e-111">The most common type of projection, a perspective projection, is responsible for making objects near the camera appear bigger than objects in the distance.</span></span> <span data-ttu-id="d650e-112">針對透視檢視，檢視範圍可視為金字塔，相機位於塔頂，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="d650e-112">For perspective viewing, the viewing frustum can be visualized as a pyramid, with the camera positioned at the tip as shown in the following illustration.</span></span> <span data-ttu-id="d650e-113">此金字塔與前端和背景裁剪平面相交。</span><span class="sxs-lookup"><span data-stu-id="d650e-113">This pyramid is intersected by a front and back clipping plane.</span></span> <span data-ttu-id="d650e-114">金字塔內前端和背景裁剪平面之間的體積是檢視範圍。</span><span class="sxs-lookup"><span data-stu-id="d650e-114">The volume within the pyramid between the front and back clipping planes is the viewing frustum.</span></span> <span data-ttu-id="d650e-115">唯有在這個體積中，物件才會顯示。</span><span class="sxs-lookup"><span data-stu-id="d650e-115">Objects are visible only when they are in this volume.</span></span>

![前端和背景裁剪平面之間檢視範圍的圖例](images/frustum.png)

<span data-ttu-id="d650e-117">如果您想像站在暗房裡，並看出方窗外，就會視覺化檢視範圍。</span><span class="sxs-lookup"><span data-stu-id="d650e-117">If you imagine that you are standing in a dark room and looking through a square window, you are visualizing a viewing frustum.</span></span> <span data-ttu-id="d650e-118">在這個類比，近裁剪平面是窗戶，背景裁剪平面是最後中斷檢視的任何東西 - 對街的摩天大樓、遠方山脈，或空無一物。</span><span class="sxs-lookup"><span data-stu-id="d650e-118">In this analogy, the near clipping plane is the window, and the back clipping plane is whatever finally interrupts your view - the skyscraper across the street, the mountains in the distance, or nothing at all.</span></span> <span data-ttu-id="d650e-119">您可以看到被截斷金字塔內的所有東西，從窗戶開始到中斷檢視的任何東西結束，而且您看不到其他任何東西。</span><span class="sxs-lookup"><span data-stu-id="d650e-119">You can see everything inside the truncated pyramid that starts at the window and ends with whatever interrupts your view, and you can see nothing else.</span></span>

<span data-ttu-id="d650e-120">檢視範圍是由 fov（視野），以及前端和背景裁剪平面之間的距離 (在 z 座標中指定) 所定義，如下圖顯示。</span><span class="sxs-lookup"><span data-stu-id="d650e-120">The viewing frustum is defined by fov (field of view) and by the distances of the front and back clipping planes, specified in z-coordinates, as shown in the following diagram.</span></span>

![檢視範圍圖](images/fovdiag.png)

<span data-ttu-id="d650e-122">在這個圖，變數 D 是從相機到空間原點 (此空間定義在幾何管線最後一部分 - 檢視轉換) 之間的距離。</span><span class="sxs-lookup"><span data-stu-id="d650e-122">In this diagram, the variable D is the distance from the camera to the origin of the space that was defined in the last part of the geometry pipeline - the viewing transformation.</span></span> <span data-ttu-id="d650e-123">圍繞這個空間，您排列檢視範圍的限制。</span><span class="sxs-lookup"><span data-stu-id="d650e-123">This is the space around which you arrange the limits of your viewing frustum.</span></span> <span data-ttu-id="d650e-124">如需有關如何使用此 D 變數來建立投射矩陣的詳細資訊，請參閱 [ (Direct3D 9 的投射轉換) ](projection-transform.md)</span><span class="sxs-lookup"><span data-stu-id="d650e-124">For information about how this D variable is used to build the projection matrix, see the [Projection Transform (Direct3D 9)](projection-transform.md)</span></span>

## <a name="viewport-rectangle"></a><span data-ttu-id="d650e-125">檢視區矩形</span><span class="sxs-lookup"><span data-stu-id="d650e-125">Viewport Rectangle</span></span>

<span data-ttu-id="d650e-126">您可以使用 [**D3DVIEWPORT9**](d3dviewport9.md) 結構，在 c + + 中定義區的矩形。</span><span class="sxs-lookup"><span data-stu-id="d650e-126">You define the viewport rectangle in C++ by using the [**D3DVIEWPORT9**](d3dviewport9.md) structure.</span></span> <span data-ttu-id="d650e-127">D3DVIEWPORT9 結構會與 IDirect3DDevice9 介面所公開的下列視口操作方法搭配使用。</span><span class="sxs-lookup"><span data-stu-id="d650e-127">The D3DVIEWPORT9 structure is used with the following viewport manipulation methods exposed by the IDirect3DDevice9 interface.</span></span>

-   [<span data-ttu-id="d650e-128">**IDirect3DDevice9::GetViewport**</span><span class="sxs-lookup"><span data-stu-id="d650e-128">**IDirect3DDevice9::GetViewport**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getviewport)
-   [<span data-ttu-id="d650e-129">**IDirect3DDevice9::SetViewport**</span><span class="sxs-lookup"><span data-stu-id="d650e-129">**IDirect3DDevice9::SetViewport**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setviewport)

<span data-ttu-id="d650e-130">D3DVIEWPORT9 結構包含四個成員（X、Y、寬度、高度），可定義要呈現場景的呈現目標介面區域。</span><span class="sxs-lookup"><span data-stu-id="d650e-130">The D3DVIEWPORT9 structure contains four members - X, Y, Width, Height - that define the area of the render-target surface into which a scene will be rendered.</span></span> <span data-ttu-id="d650e-131">這些值對應目的地矩形或檢視區矩形，如下圖顯示。</span><span class="sxs-lookup"><span data-stu-id="d650e-131">These values correspond to the destination rectangle, or viewport rectangle, as shown in the following diagram.</span></span>

![檢視區矩形圖](images/destrect.png)

<span data-ttu-id="d650e-133">指定的 X、Y、寬度、高度成員值是相對於轉譯目標表面左上角的螢幕座標。</span><span class="sxs-lookup"><span data-stu-id="d650e-133">The values you specify for the X, Y, Width, Height members are screen coordinates relative to the upper-left corner of the render-target surface.</span></span> <span data-ttu-id="d650e-134">結構定義兩個額外成員（MinZ 和 MaxZ），表示場景轉譯到的深度範圍。</span><span class="sxs-lookup"><span data-stu-id="d650e-134">The structure defines two additional members (MinZ and MaxZ) that indicate the depth-ranges into which the scene will be rendered.</span></span>

<span data-ttu-id="d650e-135">Direct3D 假設檢視區裁剪體積的範圍是從 -1.0 到 1.0 (在 X 中) 以及從 1.0 到 -1.0 (在 Y 中)。這些是應用程式過去最常使用的設定。</span><span class="sxs-lookup"><span data-stu-id="d650e-135">Direct3D assumes that the viewport clipping volume ranges from -1.0 to 1.0 in X, and from 1.0 to -1.0 in Y. These were the settings used most often by applications in the past.</span></span> <span data-ttu-id="d650e-136">裁剪之前，您可以使用[投影轉換](projection-transform.md)調整檢視區的長寬比例。</span><span class="sxs-lookup"><span data-stu-id="d650e-136">You can adjust the viewport aspect ratio before clipping using the [projection transform](projection-transform.md).</span></span>

> [!Note]  
> <span data-ttu-id="d650e-137">MinZ 和 MaxZ 指出將呈現場景的深度範圍，而不會用於剪切。</span><span class="sxs-lookup"><span data-stu-id="d650e-137">MinZ and MaxZ indicate the depth-ranges into which the scene will be rendered and are not used for clipping.</span></span> <span data-ttu-id="d650e-138">大部分的應用程式都會將這些成員設定為0.0 和1.0，讓系統能夠轉譯成深度緩衝區中的整個深度值範圍。</span><span class="sxs-lookup"><span data-stu-id="d650e-138">Most applications will set these members to 0.0 and 1.0 to enable the system to render to the entire range of depth values in the depth buffer.</span></span> <span data-ttu-id="d650e-139">有時候，您可以使用其他深度範圍達成特殊效果。</span><span class="sxs-lookup"><span data-stu-id="d650e-139">In some cases, you can achieve special effects by using other depth ranges.</span></span> <span data-ttu-id="d650e-140">例如，若要在遊戲中轉譯平視顯示器，您可以將這兩個值設定為 0.0，強迫在場景的前景中轉譯物件，或者您可以將這兩個值設定為 1.0，轉譯永遠應該會在背景中的物件。</span><span class="sxs-lookup"><span data-stu-id="d650e-140">For instance, to render a heads-up display in a game, you can set both values to 0.0 to force the system to render objects in a scene in the foreground, or you might set them both to 1.0 to render an object that should always be in the background.</span></span>

 

<span data-ttu-id="d650e-141">在 [**D3DVIEWPORT9**](d3dviewport9.md) 結構的 X、Y、Width、Height 成員中使用的維度，會定義呈現目標介面上的位置和大社區。</span><span class="sxs-lookup"><span data-stu-id="d650e-141">The dimensions used in the X, Y, Width, Height members of the [**D3DVIEWPORT9**](d3dviewport9.md) structure for a viewport define the location and dimensions of the viewport on the render-target surface.</span></span> <span data-ttu-id="d650e-142">這些值是在螢幕座標中，相對於表面左上角。</span><span class="sxs-lookup"><span data-stu-id="d650e-142">These values are in screen coordinates, relative to the upper-left corner of the surface.</span></span>

<span data-ttu-id="d650e-143">Direct3D 使用檢視區位置和維度來縮放頂點，讓轉譯的場景放在目標表面上的適當位置。</span><span class="sxs-lookup"><span data-stu-id="d650e-143">Direct3D uses the viewport location and dimensions to scale the vertices to fit a rendered scene into the appropriate location on the target surface.</span></span> <span data-ttu-id="d650e-144">內部，Direct3D 會將這些值插入下列套用到每個頂點的矩陣中。</span><span class="sxs-lookup"><span data-stu-id="d650e-144">Internally, Direct3D inserts these values into the following matrix that is applied to each vertex.</span></span>

![套用到每個頂點之矩陣的方程式](images/vpscale.png)

<span data-ttu-id="d650e-146">這個矩陣依據檢視區維度和您想要的深度範圍縮放頂點，並將它們轉移到轉譯目標表面上的適當位置。</span><span class="sxs-lookup"><span data-stu-id="d650e-146">This matrix scales vertices according to the viewport dimensions and desired depth range and translates them to the appropriate location on the render-target surface.</span></span> <span data-ttu-id="d650e-147">矩陣也翻轉 y 座標，隨著 y 向下漸增，以反映左上角的螢幕原點。</span><span class="sxs-lookup"><span data-stu-id="d650e-147">The matrix also flips the y-coordinate to reflect a screen origin at the top-left corner with y increasing downward.</span></span> <span data-ttu-id="d650e-148">套用這個矩陣之後，頂點仍是同質的，也就是說，它們仍會以 \[ x、y、z、w 頂點的形式存在， \] 而且必須先轉換成非同質座標，才能傳送到轉譯器。</span><span class="sxs-lookup"><span data-stu-id="d650e-148">After this matrix is applied, vertices are still homogeneous - that is, they still exist as \[x,y,z,w\] vertices - and they must be converted to non-homogeneous coordinates before being sent to the rasterizer.</span></span>

> [!Note]  
> <span data-ttu-id="d650e-149">區域調整矩陣會併入 [**D3DVIEWPORT9**](d3dviewport9.md) 結構的 MinZ 和 MaxZ 成員，以縮放頂點以符合深度範圍 \[ MinZ、MaxZ \] 。</span><span class="sxs-lookup"><span data-stu-id="d650e-149">The viewport scaling matrix incorporates the MinZ and MaxZ members of the [**D3DVIEWPORT9**](d3dviewport9.md) structure to scale vertices to fit the depth range \[MinZ, MaxZ\].</span></span> <span data-ttu-id="d650e-150">這代表舊版 DirectX 的不同語義，其中這些成員是用來剪切。</span><span class="sxs-lookup"><span data-stu-id="d650e-150">This represents different semantics from previous releases of DirectX, in which these members were used for clipping.</span></span>

 

> [!Note]  
> <span data-ttu-id="d650e-151">應用程式通常會分別將 MinZ 和 MaxZ 設定為0.0 和1.0，讓系統轉譯成整個深度範圍。</span><span class="sxs-lookup"><span data-stu-id="d650e-151">Applications typically set MinZ and MaxZ to 0.0 and 1.0 respectively to cause the system to render to the entire depth range.</span></span> <span data-ttu-id="d650e-152">不過，您可以使用其他值達到特定效果。</span><span class="sxs-lookup"><span data-stu-id="d650e-152">However, you can use other values to achieve certain affects.</span></span> <span data-ttu-id="d650e-153">例如，您可以將這兩個值設為 0.0，強制所有物件到前景，或都設為 1.0 將所有物件轉譯到背景。</span><span class="sxs-lookup"><span data-stu-id="d650e-153">For example, you might set both values to 0.0 to force all objects into the foreground, or set both to 1.0 to render all objects into the background.</span></span>

 

## <a name="clearing-a-viewport"></a><span data-ttu-id="d650e-154">清除檢視區</span><span class="sxs-lookup"><span data-stu-id="d650e-154">Clearing a Viewport</span></span>

<span data-ttu-id="d650e-155">清除檢視區會重設轉譯目標表面上檢視區矩形的內容。</span><span class="sxs-lookup"><span data-stu-id="d650e-155">Clearing the viewport resets the contents of the viewport rectangle on the render-target surface.</span></span> <span data-ttu-id="d650e-156">它也會清除深度和樣板緩衝區表面中的矩形。</span><span class="sxs-lookup"><span data-stu-id="d650e-156">It can also clear the rectangle in the depth and stencil buffer surfaces.</span></span>

<span data-ttu-id="d650e-157">使用 [**IDirect3DDevice9：： clear**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-clear) 可清除此區。</span><span class="sxs-lookup"><span data-stu-id="d650e-157">Use [**IDirect3DDevice9::Clear**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-clear) to clear the viewport.</span></span> <span data-ttu-id="d650e-158">方法會接受一個或多個矩形，以定義要清除之介面上的區域。</span><span class="sxs-lookup"><span data-stu-id="d650e-158">The method accepts one or more rectangles that define the areas on the surface being cleared.</span></span> <span data-ttu-id="d650e-159">將 Count 參數設定為1，而將 pRects 參數設定為單一矩形的位址（涵蓋整個視窗區區域）將會清除整個視表單。</span><span class="sxs-lookup"><span data-stu-id="d650e-159">Setting the Count parameter to 1, and the pRects parameter to the address of a single rectangle that covers the entire viewport area will clear the entire viewport.</span></span> <span data-ttu-id="d650e-160">清除整個視口的另一種方式是將 pRects 參數設定為 **Null** ，並將 Count 參數設定為0。</span><span class="sxs-lookup"><span data-stu-id="d650e-160">Another way to clear the entire viewport is to set the pRects parameter to **NULL** and the Count parameter to 0.</span></span>

<span data-ttu-id="d650e-161">[**IDirect3DDevice9：： Clear**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-clear)可以用來清除深度緩衝區內的樣板位。</span><span class="sxs-lookup"><span data-stu-id="d650e-161">The [**IDirect3DDevice9::Clear**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-clear) can be used for clearing stencil bits within a depth buffer.</span></span> <span data-ttu-id="d650e-162">只要設定 Flags 參數，即可決定 **IDirect3DDevice9：： Clear** 如何搭配轉譯目標和任何相關聯的深度或樣板緩衝區。</span><span class="sxs-lookup"><span data-stu-id="d650e-162">Simply set the Flags parameter to determine how **IDirect3DDevice9::Clear** works with the render target and any associated depth or stencil buffers.</span></span> <span data-ttu-id="d650e-163">D3DCLEAR \_ 目標旗標將會使用您在 color 引數中提供的任意 RGBA 色彩來清除此區， (這不是材質色彩) 。</span><span class="sxs-lookup"><span data-stu-id="d650e-163">The D3DCLEAR\_TARGET flag will clear the viewport using an arbitrary RGBA color that you provide in the Color argument (this is not the material color).</span></span> <span data-ttu-id="d650e-164">D3DCLEAR \_ ZBUFFER 旗標會將深度緩衝區清除為您在 Z：0.0 中指定的任意深度最接近的距離，而1.0 是最遠的。</span><span class="sxs-lookup"><span data-stu-id="d650e-164">The D3DCLEAR\_ZBUFFER flag will clear the depth buffer to an arbitrary depth you specify in Z: 0.0 is the closest distance, and 1.0 is the farthest.</span></span> <span data-ttu-id="d650e-165">D3DCLEAR 樣板 \_ 旗標會將樣板位重設為您在樣板引數中提供的值。</span><span class="sxs-lookup"><span data-stu-id="d650e-165">The D3DCLEAR\_STENCIL flag will reset the stencil bits to the value you provide in the Stencil argument.</span></span> <span data-ttu-id="d650e-166">您可以使用範圍從0到 2n-1 的整數，其中 n 是樣板緩衝區位深度。</span><span class="sxs-lookup"><span data-stu-id="d650e-166">You can use integers that range from 0 to 2n-1, where n is the stencil buffer bit depth.</span></span>

<span data-ttu-id="d650e-167">在某些情況下，您可能只會轉譯成轉譯目標和深度緩衝區表面的小部分。</span><span class="sxs-lookup"><span data-stu-id="d650e-167">In some situations, you might be rendering only to small portions of the render target and depth buffer surfaces.</span></span> <span data-ttu-id="d650e-168">Clear 方法也可讓您在單一呼叫中清除介面的多個區域。</span><span class="sxs-lookup"><span data-stu-id="d650e-168">The clear methods also enable you to clear multiple areas of your surfaces in a single call.</span></span> <span data-ttu-id="d650e-169">若要這麼做，請將 Count 參數設定為您想要清除的矩形數目，並在 pRects 參數中指定矩形陣列中第一個矩形的位址。</span><span class="sxs-lookup"><span data-stu-id="d650e-169">Do this by setting the Count parameter to the number of rectangles you want cleared, and specify the address of the first rectangle in an array of rectangles in the pRects parameter.</span></span>

## <a name="set-up-the-viewport-for-clipping"></a><span data-ttu-id="d650e-170">設定裁剪的檢視區</span><span class="sxs-lookup"><span data-stu-id="d650e-170">Set Up the Viewport for Clipping</span></span>

<span data-ttu-id="d650e-171">投影矩陣的結果決定投影空間中的裁剪體積為：</span><span class="sxs-lookup"><span data-stu-id="d650e-171">The results of the projection matrix determine the clipping volume in projection space as:</span></span>

<span data-ttu-id="d650e-172">-w<sub>c</sub><= x<sub>c</sub><= w<sub>c</sub></span><span class="sxs-lookup"><span data-stu-id="d650e-172">-w<sub>c</sub><= x<sub>c</sub><= w<sub>c</sub></span></span>

<span data-ttu-id="d650e-173">-w<sub>c</sub><= y<sub>c</sub><= w<sub>c</sub></span><span class="sxs-lookup"><span data-stu-id="d650e-173">-w<sub>c</sub><= y<sub>c</sub><= w<sub>c</sub></span></span>

<span data-ttu-id="d650e-174">0 <= z<sub>c</sub><= w<sub>c</sub></span><span class="sxs-lookup"><span data-stu-id="d650e-174">0 <= z<sub>c</sub><= w<sub>c</sub></span></span>

<span data-ttu-id="d650e-175">其中：x、y 和 w 代表套用投影轉換後的頂點座標。</span><span class="sxs-lookup"><span data-stu-id="d650e-175">Where: x, y, z, and w represent the vertex coordinates after the projection transformation is applied.</span></span> <span data-ttu-id="d650e-176">x、y 或 z 元件在這些範圍外的任何頂點都會被裁剪，如果裁剪已啟用（預設行為）。</span><span class="sxs-lookup"><span data-stu-id="d650e-176">Any vertices that have an x-, y-, or z-component outside these ranges are clipped, if clipping is enabled (the default behavior).</span></span>

<span data-ttu-id="d650e-177">除了頂點緩衝區例外之外，應用程式也會透過 [**D3DRS \_ 剪切**](./d3drenderstatetype.md) 轉譯狀態來啟用或停用裁剪。</span><span class="sxs-lookup"><span data-stu-id="d650e-177">With the exception of vertex buffers, applications enable or disable clipping by way of the [**D3DRS\_CLIPPING**](./d3drenderstatetype.md) render state.</span></span> <span data-ttu-id="d650e-178">在處理期間，會產生頂點緩衝區的剪輯資訊。</span><span class="sxs-lookup"><span data-stu-id="d650e-178">Clipping information for vertex buffers is generated during processing.</span></span> <span data-ttu-id="d650e-179">如需詳細資訊，請參閱 [ (direct3d 9 的固定函式頂點處理) ](fixed-function-vertex-processing.md) 和可程式化的 [頂點處理 (direct3d 9) ](programmable-vertex-processing.md)。</span><span class="sxs-lookup"><span data-stu-id="d650e-179">For more information, see [Fixed Function Vertex Processing (Direct3D 9)](fixed-function-vertex-processing.md) and [Programmable Vertex Processing (Direct3D 9)](programmable-vertex-processing.md).</span></span>

<span data-ttu-id="d650e-180">除非來自 [**IDirect3DDevice9：:P rocessvertices**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-processvertices)，否則 Direct3D 不會從頂點緩衝區裁剪基本的已轉換頂點。</span><span class="sxs-lookup"><span data-stu-id="d650e-180">Direct3D does not clip transformed vertices of a primitive from a vertex buffer unless it comes from [**IDirect3DDevice9::ProcessVertices**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-processvertices).</span></span> <span data-ttu-id="d650e-181">如果您要執行自己的轉換，而且需要 Direct3D 進行裁剪，則不應使用頂點緩衝區。</span><span class="sxs-lookup"><span data-stu-id="d650e-181">If you are doing your own transforms and need Direct3D to do the clipping, you should not use vertex buffers.</span></span> <span data-ttu-id="d650e-182">在此情況下，應用程式會將資料進行轉換。</span><span class="sxs-lookup"><span data-stu-id="d650e-182">In this case, the application traverses the data to transform it.</span></span> <span data-ttu-id="d650e-183">Direct3D 會第二次流經資料來裁剪資料，然後驅動程式會轉譯資料，而這種情況沒有效率。</span><span class="sxs-lookup"><span data-stu-id="d650e-183">Direct3D traverses the data a second time to clip it, and then the driver renders the data, which is inefficient.</span></span> <span data-ttu-id="d650e-184">因此，如果應用程式轉換資料，也應該要裁剪資料。</span><span class="sxs-lookup"><span data-stu-id="d650e-184">So, if the application transforms the data, is should also clip the data.</span></span>

<span data-ttu-id="d650e-185">當裝置接收到預先轉換和亮頂點 (T&需要裁剪的頂點) 時，為了執行裁剪作業，頂點會使用頂點的交互同質 w (RHW) 和資料格資訊，重新轉換成剪切空間。</span><span class="sxs-lookup"><span data-stu-id="d650e-185">When the device receives pre-transformed and lit vertices (T&L vertices) that need to be clipped, in order to perform the clipping operation the vertices are back-transformed to the clipping space using the vertex's reciprocal homogeneous w (RHW) and the viewport information.</span></span> <span data-ttu-id="d650e-186">然後會執行剪切。</span><span class="sxs-lookup"><span data-stu-id="d650e-186">Clipping is then performed.</span></span> <span data-ttu-id="d650e-187">並非所有裝置都能夠執行此反向轉換，以裁剪 T&L 頂點。</span><span class="sxs-lookup"><span data-stu-id="d650e-187">Not all devices are capable of performing this back-transform in order to clip T&L vertices.</span></span>

<span data-ttu-id="d650e-188">D3DPMISCCAPS \_ CLIPTLVERTS 裝置功能指出裝置是否能夠裁剪 T&L 頂點。</span><span class="sxs-lookup"><span data-stu-id="d650e-188">The D3DPMISCCAPS\_CLIPTLVERTS device capability indicates whether the device is capable of clipping T&L vertices.</span></span> <span data-ttu-id="d650e-189">如果未設定這項功能，應用程式會負責將它要向下傳送至要轉譯之裝置的 T&L 頂點。</span><span class="sxs-lookup"><span data-stu-id="d650e-189">If this capability is not set, the application is responsible for clipping the T&L vertices that it intends to send down to the device to be rendered.</span></span> <span data-ttu-id="d650e-190">無論裝置是在軟體頂點處理模式中建立，還是切換至軟體頂點處理模式) ，裝置一律都能在軟體頂點處理模式中裁剪 T&L 頂點 (。</span><span class="sxs-lookup"><span data-stu-id="d650e-190">The device is always capable of clipping T&L vertices in the software vertex processing mode (regardless of whether the device is created in the software vertex processing mode, or switched to the software vertex processing mode).</span></span>

<span data-ttu-id="d650e-191">設定轉譯裝置之視口參數的唯一需求是設定視口的剪切量。</span><span class="sxs-lookup"><span data-stu-id="d650e-191">The only requirement for configuring the viewport parameters for a rendering device is to set the viewport's clipping volume.</span></span> <span data-ttu-id="d650e-192">若要這樣做，您可以針對裁剪磁片區和轉譯目標介面，初始化並設定裁剪值。</span><span class="sxs-lookup"><span data-stu-id="d650e-192">To do this, you initialize and set clipping values for the clipping volume and for the render-target surface.</span></span> <span data-ttu-id="d650e-193">您通常會將多個區域設定為轉譯為轉譯目標表面的完整區域，但這不是必要條件。</span><span class="sxs-lookup"><span data-stu-id="d650e-193">Viewports are commonly set up to render to the full area of the render-target surface, but this isn't a requirement.</span></span>

<span data-ttu-id="d650e-194">您可以針對 [**D3DVIEWPORT9**](d3dviewport9.md) 結構的成員使用下列設定，以在 c + + 中達成這個目的。</span><span class="sxs-lookup"><span data-stu-id="d650e-194">You can use the following settings for the members of the [**D3DVIEWPORT9**](d3dviewport9.md) structure to achieve this in C++.</span></span>


```
D3DVIEWPORT9 viewData = { 0, 0, width, height, 0.0f, 1.0f };
```



<span data-ttu-id="d650e-195">設定 [**D3DVIEWPORT9**](d3dviewport9.md) 結構中的值之後，請呼叫其 [**IDirect3DDevice9：： SetViewport**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setviewport) 方法，將資料區參數套用至裝置。</span><span class="sxs-lookup"><span data-stu-id="d650e-195">After setting values in the [**D3DVIEWPORT9**](d3dviewport9.md) structure, apply the viewport parameters to the device by calling its [**IDirect3DDevice9::SetViewport**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setviewport) method.</span></span> <span data-ttu-id="d650e-196">下列程式碼範例會顯示這個呼叫的外觀。</span><span class="sxs-lookup"><span data-stu-id="d650e-196">The following code example shows what this call might look like.</span></span>


```
HRESULT hr;

hr = pd3dDevice->SetViewport(&viewData);
if(FAILED(hr))
    return hr;
```



<span data-ttu-id="d650e-197">如果呼叫成功，則會設定視口參數，並且會在下次呼叫轉譯方法時生效。</span><span class="sxs-lookup"><span data-stu-id="d650e-197">If the call succeeds, the viewport parameters are set and will take effect the next time a rendering method is called.</span></span> <span data-ttu-id="d650e-198">若要變更視口參數，請只更新 [**D3DVIEWPORT9**](d3dviewport9.md) 結構中的值，然後再次呼叫 [**IDirect3DDevice9：： SetViewport**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setviewport) 。</span><span class="sxs-lookup"><span data-stu-id="d650e-198">To make changes to the viewport parameters, just update the values in the [**D3DVIEWPORT9**](d3dviewport9.md) structure and call [**IDirect3DDevice9::SetViewport**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setviewport) again.</span></span>

> [!Note]  
> <span data-ttu-id="d650e-199">[**D3DVIEWPORT9**](d3dviewport9.md)結構成員 MinZ 和 MaxZ 指出將呈現場景的深度範圍，而不會用於裁剪。</span><span class="sxs-lookup"><span data-stu-id="d650e-199">The [**D3DVIEWPORT9**](d3dviewport9.md) structure members MinZ and MaxZ indicate the depth-ranges into which the scene will be rendered and are not used for clipping.</span></span> <span data-ttu-id="d650e-200">大部分的應用程式都會將這些成員設定為0.0 和1.0，讓系統能夠轉譯成深度緩衝區中的整個深度值範圍。</span><span class="sxs-lookup"><span data-stu-id="d650e-200">Most applications set these members to 0.0 and 1.0 to enable the system to render to the entire range of depth values in the depth buffer.</span></span> <span data-ttu-id="d650e-201">有時候，您可以使用其他深度範圍達成特殊效果。</span><span class="sxs-lookup"><span data-stu-id="d650e-201">In some cases, you can achieve special effects by using other depth ranges.</span></span> <span data-ttu-id="d650e-202">例如，若要在遊戲中轉譯平視顯示器，您可以將這兩個值設定為 0.0，強迫在場景的前景中轉譯物件，或者您可以將這兩個值設定為 1.0，轉譯永遠應該會在背景中的物件。</span><span class="sxs-lookup"><span data-stu-id="d650e-202">For instance, to render a heads-up display in a game, you can set both values to 0.0 to force the system to render objects in a scene in the foreground, or you might set them both to 1.0 to render an object that should always be in the background.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="d650e-203">相關主題</span><span class="sxs-lookup"><span data-stu-id="d650e-203">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d650e-204">快速入門</span><span class="sxs-lookup"><span data-stu-id="d650e-204">Getting Started</span></span>](getting-started.md)
</dt> </dl>

 

 
