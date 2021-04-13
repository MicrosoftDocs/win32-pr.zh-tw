---
title: 移植矩陣和轉換函數
description: 鳶尾花 GL 和 OpenGL 以類似的方式處理矩陣和轉換。
ms.assetid: 732ba65a-d776-43ea-a605-0f59209c9a46
keywords:
- 鳶尾花 GL 移植，矩陣
- 從鳶尾花 GL （矩陣）移植
- 從鳶尾花 GL （矩陣）移植至 OpenGL
- 從鳶尾花 GL （矩陣）進行 OpenGL 移植
- 矩陣
- 鳶尾花 GL 移植，轉換
- 從鳶尾花 GL 進行移植，轉換
- 從鳶尾花 GL 移植至 OpenGL，轉換
- 從鳶尾花 GL 的 OpenGL 移植，轉換
- 轉換
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1c6219640085370202b8dbebad9a2e9d4992b4f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301387"
---
# <a name="porting-matrix-and-transformation-functions"></a><span data-ttu-id="79afd-113">移植矩陣和轉換函數</span><span class="sxs-lookup"><span data-stu-id="79afd-113">Porting Matrix and Transformation Functions</span></span>

<span data-ttu-id="79afd-114">鳶尾花 GL 和 OpenGL 以類似的方式處理矩陣和轉換。</span><span class="sxs-lookup"><span data-stu-id="79afd-114">IRIS GL and OpenGL handle matrices and transformations in a similar manner.</span></span> <span data-ttu-id="79afd-115">但是從鳶尾花 GL 移植程式碼時，有幾個差異要記住：</span><span class="sxs-lookup"><span data-stu-id="79afd-115">But there are several differences to keep in mind when porting code from IRIS GL:</span></span>

-   <span data-ttu-id="79afd-116">在 OpenGL 中，一律採用雙矩陣模式;沒有單一矩陣模式。</span><span class="sxs-lookup"><span data-stu-id="79afd-116">In OpenGL you are always in double-matrix mode; there is no single-matrix mode.</span></span>
-   <span data-ttu-id="79afd-117">角度是以度為單位，而不是十分之一度。</span><span class="sxs-lookup"><span data-stu-id="79afd-117">Angles are measured in degrees, instead of tenths of degrees.</span></span>
-   <span data-ttu-id="79afd-118">投射矩陣呼叫（例如 [**glFrustum**](glfrustum.md) 和 [**glOrtho**](glortho.md)）現在會乘以目前的矩陣，而不是載入到目前的矩陣上。</span><span class="sxs-lookup"><span data-stu-id="79afd-118">Projection matrix calls, like [**glFrustum**](glfrustum.md) and [**glOrtho**](glortho.md), now multiply onto the current matrix, instead of being loaded onto the current matrix.</span></span>
-   <span data-ttu-id="79afd-119">OpenGL 函數 [**glRotate**](glrotate.md)與 **旋轉** 非常不同。</span><span class="sxs-lookup"><span data-stu-id="79afd-119">The OpenGL function, [**glRotate**](glrotate.md), is very different from **rotate**.</span></span> <span data-ttu-id="79afd-120">您可以繞著任意軸旋轉，而不是限制為 X 軸、y 軸和 Z 軸。</span><span class="sxs-lookup"><span data-stu-id="79afd-120">You can rotate around any arbitrary axis, instead of being confined to the x-, y-, and z- axes.</span></span> <span data-ttu-id="79afd-121">例如，您可以翻譯：</span><span class="sxs-lookup"><span data-stu-id="79afd-121">For example, you can translate:</span></span>

    ```C++
    rotate(200*(i+1), 'z');
    ```

    

    <span data-ttu-id="79afd-122">變更為：</span><span class="sxs-lookup"><span data-stu-id="79afd-122">to:</span></span>

    ```C++
    glRotate(.1*(200*(i+1), 0.0, 0.0, 1.0);
    ```

    

    <span data-ttu-id="79afd-123">從 **旋轉** 轉譯為 **glRotate** 時，您會切換至十分之一度的角度，並以 Z 軸的向量取代 ' z '。</span><span class="sxs-lookup"><span data-stu-id="79afd-123">When translating from **rotate** to **glRotate** you switch to degrees from tenths of degrees and replace 'z' with a vector for the z-axis.</span></span>

-   <span data-ttu-id="79afd-124">OpenGL 沒有 **polarview** 函式的相等專案。</span><span class="sxs-lookup"><span data-stu-id="79afd-124">OpenGL has no equivalent to the **polarview** function.</span></span> <span data-ttu-id="79afd-125">您可以輕鬆地使用轉譯和三個旋轉來取代它。</span><span class="sxs-lookup"><span data-stu-id="79afd-125">You can replace it easily with a translation and three rotations.</span></span> <span data-ttu-id="79afd-126">例如，您可以翻譯：</span><span class="sxs-lookup"><span data-stu-id="79afd-126">For example, you can translate:</span></span>

    ```C++
    polarview(distance, azimuth, incidence, twist);
     
    ```

    

    <span data-ttu-id="79afd-127">變更為：</span><span class="sxs-lookup"><span data-stu-id="79afd-127">to:</span></span>

    ```C++
    glTranslatef( 0.0, 0.0, -distance); 
    glRotatef( -twist * 10.0, 0.0, 0.0, 1.0); 
    glRotatef( -incidence * 10.0, 1.0, 0.0, 0.0); 
    glRotatef( -azimuth * 10.0, 0.0, 0.0, 1.0);
    ```

    

<span data-ttu-id="79afd-128">下表列出 OpenGL 矩陣函數及其對等的鳶尾花 GL 函數。</span><span class="sxs-lookup"><span data-stu-id="79afd-128">The following table lists the OpenGL matrix functions and their equivalent IRIS GL functions.</span></span>



| <span data-ttu-id="79afd-129">鳶尾花 GL 函數</span><span class="sxs-lookup"><span data-stu-id="79afd-129">IRIS GL function</span></span>              | <span data-ttu-id="79afd-130">OpenGL 函數</span><span class="sxs-lookup"><span data-stu-id="79afd-130">OpenGL function</span></span>                                                                        | <span data-ttu-id="79afd-131">意義</span><span class="sxs-lookup"><span data-stu-id="79afd-131">Meaning</span></span>                                                                                                                                                                        |
|-------------------------------|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="79afd-132">**mmode**</span><span class="sxs-lookup"><span data-stu-id="79afd-132">**mmode**</span></span>                     | [<span data-ttu-id="79afd-133">**glMatrixMode**</span><span class="sxs-lookup"><span data-stu-id="79afd-133">**glMatrixMode**</span></span>](glmatrixmode.md)                                                   | <span data-ttu-id="79afd-134">設定目前的矩陣模式。</span><span class="sxs-lookup"><span data-stu-id="79afd-134">Sets current matrix mode.</span></span>                                                                                                                                                      |
|                               | [<span data-ttu-id="79afd-135">**glLoadIdentity**</span><span class="sxs-lookup"><span data-stu-id="79afd-135">**glLoadIdentity**</span></span>](glloadidentity.md)                                               | <span data-ttu-id="79afd-136">將目前的矩陣取代為識別矩陣。</span><span class="sxs-lookup"><span data-stu-id="79afd-136">Replaces current matrix with the identity matrix.</span></span>                                                                                                                              |
| <span data-ttu-id="79afd-137">**loadmatrix**</span><span class="sxs-lookup"><span data-stu-id="79afd-137">**loadmatrix**</span></span>                | <span data-ttu-id="79afd-138">[**glLoadMatrixf**](glloadmatrix.md)、[**glLoadMatrixd**](glloadmatrix.md)</span><span class="sxs-lookup"><span data-stu-id="79afd-138">[**glLoadMatrixf**](glloadmatrix.md),[**glLoadMatrixd**](glloadmatrix.md)</span></span><br/> | <span data-ttu-id="79afd-139">以指定的矩陣取代目前的矩陣。</span><span class="sxs-lookup"><span data-stu-id="79afd-139">Replaces current matrix with the specified matrix.</span></span>                                                                                                                             |
| <span data-ttu-id="79afd-140">**multmatrix**</span><span class="sxs-lookup"><span data-stu-id="79afd-140">**multmatrix**</span></span>                | <span data-ttu-id="79afd-141">[**glMultMatrixf**](glmultmatrix.md)、[**glMultMatrixd**](glmultmatrix.md)</span><span class="sxs-lookup"><span data-stu-id="79afd-141">[**glMultMatrixf**](glmultmatrix.md),[**glMultMatrixd**](glmultmatrix.md)</span></span><br/> | <span data-ttu-id="79afd-142">將目前的矩陣與指定的矩陣相乘 (請注意， **multmatrix** 會預先相乘) 。</span><span class="sxs-lookup"><span data-stu-id="79afd-142">Post-multiplies current matrix with the specified matrix (note that **multmatrix** pre-multiplied).</span></span>                                                                            |
| <span data-ttu-id="79afd-143">**mapw**、 **mapw2**</span><span class="sxs-lookup"><span data-stu-id="79afd-143">**mapw**, **mapw2**</span></span>           | [<span data-ttu-id="79afd-144">**gluUnProject**</span><span class="sxs-lookup"><span data-stu-id="79afd-144">**gluUnProject**</span></span>](gluunproject.md)                                                   | <span data-ttu-id="79afd-145">專案世界-空間與物件空間的座標 (另請參閱 [**gluProject**](gluproject.md)) 。</span><span class="sxs-lookup"><span data-stu-id="79afd-145">Projects world-space coordinates to object space (see also [**gluProject**](gluproject.md)).</span></span>                                                                                  |
| <span data-ttu-id="79afd-146">**鄰**</span><span class="sxs-lookup"><span data-stu-id="79afd-146">**ortho**</span></span>                     | [<span data-ttu-id="79afd-147">**glOrtho**</span><span class="sxs-lookup"><span data-stu-id="79afd-147">**glOrtho**</span></span>](glortho.md)                                                             | <span data-ttu-id="79afd-148">將目前的矩陣與正向投射矩陣相乘。</span><span class="sxs-lookup"><span data-stu-id="79afd-148">Multiplies current matrix by an orthographic projection matrix.</span></span>                                                                                                                |
| <span data-ttu-id="79afd-149">**ortho2**</span><span class="sxs-lookup"><span data-stu-id="79afd-149">**ortho2**</span></span>                    | [<span data-ttu-id="79afd-150">**gluOrtho2D**</span><span class="sxs-lookup"><span data-stu-id="79afd-150">**gluOrtho2D**</span></span>](gluortho2d.md)                                                       | <span data-ttu-id="79afd-151">定義二維正射投射矩陣。</span><span class="sxs-lookup"><span data-stu-id="79afd-151">Defines a two-dimensional orthographic projection matrix.</span></span>                                                                                                                      |
| <span data-ttu-id="79afd-152">**視角**</span><span class="sxs-lookup"><span data-stu-id="79afd-152">**perspective**</span></span>               | [<span data-ttu-id="79afd-153">**gluPerspective**</span><span class="sxs-lookup"><span data-stu-id="79afd-153">**gluPerspective**</span></span>](gluperspective.md)                                               | <span data-ttu-id="79afd-154">定義透視圖投影矩陣。</span><span class="sxs-lookup"><span data-stu-id="79afd-154">Defines a perspective projection matrix.</span></span>                                                                                                                                       |
| <span data-ttu-id="79afd-155">**picksize**</span><span class="sxs-lookup"><span data-stu-id="79afd-155">**picksize**</span></span>                  | [<span data-ttu-id="79afd-156">**gluPickMatrix**</span><span class="sxs-lookup"><span data-stu-id="79afd-156">**gluPickMatrix**</span></span>](glupickmatrix.md)                                                 | <span data-ttu-id="79afd-157">定義挑選區域。</span><span class="sxs-lookup"><span data-stu-id="79afd-157">Defines a picking region.</span></span>                                                                                                                                                      |
| <span data-ttu-id="79afd-158">**popmatrix**</span><span class="sxs-lookup"><span data-stu-id="79afd-158">**popmatrix**</span></span>                 | [<span data-ttu-id="79afd-159">**glPopMatrix**</span><span class="sxs-lookup"><span data-stu-id="79afd-159">**glPopMatrix**</span></span>](glpopmatrix.md)                                                     | <span data-ttu-id="79afd-160">Pop 目前的矩陣堆疊，以其下的矩陣來取代目前的矩陣。</span><span class="sxs-lookup"><span data-stu-id="79afd-160">Pops current matrix stack, replacing the current matrix with the one below it.</span></span>                                                                                                 |
| <span data-ttu-id="79afd-161">**pushmatrix**</span><span class="sxs-lookup"><span data-stu-id="79afd-161">**pushmatrix**</span></span>                | [<span data-ttu-id="79afd-162">**glPushMatrix**</span><span class="sxs-lookup"><span data-stu-id="79afd-162">**glPushMatrix**</span></span>](glpushmatrix.md)                                                   | <span data-ttu-id="79afd-163">將目前的矩陣堆疊向下推一，以複製目前的矩陣。</span><span class="sxs-lookup"><span data-stu-id="79afd-163">Pushes current matrix stack down by one, duplicating the current matrix.</span></span>                                                                                                       |
| <span data-ttu-id="79afd-164">**旋轉**，**rot**</span><span class="sxs-lookup"><span data-stu-id="79afd-164">**rotate**,**rot**</span></span><br/> | <span data-ttu-id="79afd-165">[**glRotated**](glrotate.md)、[**glRotatef**](glrotate.md)</span><span class="sxs-lookup"><span data-stu-id="79afd-165">[**glRotated**](glrotate.md),[**glRotatef**](glrotate.md)</span></span><br/>                 | <span data-ttu-id="79afd-166">透過指定的點，將目前座標系統與原點的向量旋轉。</span><span class="sxs-lookup"><span data-stu-id="79afd-166">Rotates current coordinate system by the given angle about the vector from the origin through the given point.</span></span> <span data-ttu-id="79afd-167">請注意，只 **旋轉** X 軸、y 軸和 Z 軸的旋轉。</span><span class="sxs-lookup"><span data-stu-id="79afd-167">Note that **rotate** rotated only about the x-, y-, and z-axes.</span></span> |
| <span data-ttu-id="79afd-168">**scale**</span><span class="sxs-lookup"><span data-stu-id="79afd-168">**scale**</span></span>                     | <span data-ttu-id="79afd-169">[**glScaled**](glscale.md)、[**glScalef**](glscale.md)</span><span class="sxs-lookup"><span data-stu-id="79afd-169">[**glScaled**](glscale.md),[**glScalef**](glscale.md)</span></span><br/>                     | <span data-ttu-id="79afd-170">將目前的矩陣乘以縮放矩陣。</span><span class="sxs-lookup"><span data-stu-id="79afd-170">Multiplies current matrix by a scaling matrix.</span></span>                                                                                                                                 |
| <span data-ttu-id="79afd-171">**翻譯**</span><span class="sxs-lookup"><span data-stu-id="79afd-171">**translate**</span></span>                 | <span data-ttu-id="79afd-172">[**glTranslatef**](gltranslate.md)、[**glTranslated**](gltranslate.md)</span><span class="sxs-lookup"><span data-stu-id="79afd-172">[**glTranslatef**](gltranslate.md),[**glTranslated**](gltranslate.md)</span></span><br/>     | <span data-ttu-id="79afd-173">將目前的矩陣乘以平移矩陣，將座標系統原點移至指定的點。</span><span class="sxs-lookup"><span data-stu-id="79afd-173">Moves coordinate-system origin to the point specified, by multiplying the current matrix by a translation matrix.</span></span>                                                              |
| <span data-ttu-id="79afd-174">**視窗**</span><span class="sxs-lookup"><span data-stu-id="79afd-174">**window**</span></span>                    | [<span data-ttu-id="79afd-175">**glFrustum**</span><span class="sxs-lookup"><span data-stu-id="79afd-175">**glFrustum**</span></span>](glfrustum.md)                                                         | <span data-ttu-id="79afd-176">指定裁剪平面的座標，將目前的矩陣乘以透視圖矩陣。</span><span class="sxs-lookup"><span data-stu-id="79afd-176">Given coordinates for clipping planes, multiplies the current matrix by a perspective matrix.</span></span>                                                                                  |



 

<span data-ttu-id="79afd-177">OpenGL 有三個矩陣模式，以 [**glMatrixMode**](glmatrixmode.md)設定。</span><span class="sxs-lookup"><span data-stu-id="79afd-177">OpenGL has three matrix modes, which are set with [**glMatrixMode**](glmatrixmode.md).</span></span> <span data-ttu-id="79afd-178">下表列出可做為 **glMatrixMode** 參數的模式。</span><span class="sxs-lookup"><span data-stu-id="79afd-178">The following table lists the modes available as parameters for **glMatrixMode**.</span></span>



| <span data-ttu-id="79afd-179">鳶尾花 GL 矩陣模式</span><span class="sxs-lookup"><span data-stu-id="79afd-179">IRIS GL matrix mode</span></span> | <span data-ttu-id="79afd-180">OpenGL 模式</span><span class="sxs-lookup"><span data-stu-id="79afd-180">OpenGL mode</span></span>    | <span data-ttu-id="79afd-181">意義</span><span class="sxs-lookup"><span data-stu-id="79afd-181">Meaning</span></span>                                  | <span data-ttu-id="79afd-182">最小堆疊深度</span><span class="sxs-lookup"><span data-stu-id="79afd-182">Min stack depth</span></span> |
|---------------------|----------------|------------------------------------------|-----------------|
| <span data-ttu-id="79afd-183">**MTEXTURE**</span><span class="sxs-lookup"><span data-stu-id="79afd-183">**MTEXTURE**</span></span>        | <span data-ttu-id="79afd-184">GL \_ 材質</span><span class="sxs-lookup"><span data-stu-id="79afd-184">GL\_TEXTURE</span></span>    | <span data-ttu-id="79afd-185">在紋理矩陣堆疊上運作。</span><span class="sxs-lookup"><span data-stu-id="79afd-185">Operates on the texture matrix stack.</span></span>    | <span data-ttu-id="79afd-186">2</span><span class="sxs-lookup"><span data-stu-id="79afd-186">2</span></span>               |
| <span data-ttu-id="79afd-187">**MVIEWING**</span><span class="sxs-lookup"><span data-stu-id="79afd-187">**MVIEWING**</span></span>        | <span data-ttu-id="79afd-188">GL \_ 模型</span><span class="sxs-lookup"><span data-stu-id="79afd-188">GL\_MODELVIEW</span></span>  | <span data-ttu-id="79afd-189">在模型視圖矩陣堆疊上運作。</span><span class="sxs-lookup"><span data-stu-id="79afd-189">Operates on the model view matrix stack.</span></span> | <span data-ttu-id="79afd-190">32</span><span class="sxs-lookup"><span data-stu-id="79afd-190">32</span></span>              |
| <span data-ttu-id="79afd-191">**MPROJECTION**</span><span class="sxs-lookup"><span data-stu-id="79afd-191">**MPROJECTION**</span></span>     | <span data-ttu-id="79afd-192">GL \_ 投射</span><span class="sxs-lookup"><span data-stu-id="79afd-192">GL\_PROJECTION</span></span> | <span data-ttu-id="79afd-193">在投射矩陣堆疊上運作。</span><span class="sxs-lookup"><span data-stu-id="79afd-193">Operates on the projection matrix stack.</span></span> | <span data-ttu-id="79afd-194">2</span><span class="sxs-lookup"><span data-stu-id="79afd-194">2</span></span>               |



 

 

 





