---
title: 轉譯簡單的表面
description: X.GLU 隊程式庫包含一組用來繪製各種簡單表面的函式， (球體、圓柱圖、磁片和部分磁片) 以各種樣式和方向呈現。 這些函數會在 OpenGL 參考手冊中詳細說明。
ms.assetid: 403bdf8d-de4c-49e2-87d0-11109061b4c2
keywords:
- OpenGL 公用程式 (X.GLU 隊) 、簡單表面
- X.GLU 隊 (OpenGL 公用程式) ，簡單表面
- 簡單表面 OpenGL
- OpenGL 公用程式 (X.GLU 隊) 、球體
- X.GLU 隊 (OpenGL 公用程式) 、球體
- 球體 OpenGL
- OpenGL 公用程式 (X.GLU 隊) 、圓柱
- X.GLU 隊 (OpenGL 公用程式) 、圓柱
- 圓柱的 OpenGL
- OpenGL 公用程式 (X.GLU 隊) 、磁片
- X.GLU 隊 (OpenGL 公用程式) ，磁片
- 磁片 OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab766c661f89cbdec30b3295dfef8dc85b59f7fe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372665"
---
# <a name="rendering-simple-surfaces"></a><span data-ttu-id="53537-116">轉譯簡單的表面</span><span class="sxs-lookup"><span data-stu-id="53537-116">Rendering Simple Surfaces</span></span>

<span data-ttu-id="53537-117">X.GLU 隊程式庫包含一組用來繪製各種簡單表面的函式， (球體、圓柱圖、磁片和部分磁片) 以各種樣式和方向呈現。</span><span class="sxs-lookup"><span data-stu-id="53537-117">The GLU library includes a set of functions for drawing various simple surfaces (spheres, cylinders, disks, and parts of disks) in a variety of styles and orientations.</span></span> <span data-ttu-id="53537-118">這些函數會在 *OpenGL 參考手冊* 中詳細說明。</span><span class="sxs-lookup"><span data-stu-id="53537-118">These functions are described in detail in the *OpenGL Reference Manual*.</span></span>

<span data-ttu-id="53537-119">**轉譯簡單的表面**</span><span class="sxs-lookup"><span data-stu-id="53537-119">**To render simple surfaces**</span></span>

1.  <span data-ttu-id="53537-120">使用 [**gluNewQuadric**](glunewquadric.md)建立 quadric 物件。</span><span class="sxs-lookup"><span data-stu-id="53537-120">Create a quadric object with [**gluNewQuadric**](glunewquadric.md).</span></span>

    <span data-ttu-id="53537-121">若要在完成時終結這個物件，請使用 [**gluDeleteQuadric**](gludeletequadric.md)。</span><span class="sxs-lookup"><span data-stu-id="53537-121">To destroy this object when you're finished with it, use [**gluDeleteQuadric**](gludeletequadric.md).</span></span>

2.  <span data-ttu-id="53537-122">指定所需的轉譯樣式（如下所示），並使用適當的函式 (除非您滿意) 的預設值：</span><span class="sxs-lookup"><span data-stu-id="53537-122">Specify the desired rendering style, as listed below, with the appropriate function (unless you're satisfied with the default values):</span></span>
    -   <span data-ttu-id="53537-123">是否應該產生介面法線，若是如此，每個頂點上是否應該有一個法線，或每個臉部的一個法線： [ **gluQuadricNormals**](gluquadricnormals.md)</span><span class="sxs-lookup"><span data-stu-id="53537-123">Whether surface normals should be generated, and if so, whether there should be one normal per vertex or one normal per face: [**gluQuadricNormals**](gluquadricnormals.md)</span></span>
    -   <span data-ttu-id="53537-124">是否應該產生材質座標： [ **gluQuadricTexture**](gluquadrictexture.md)</span><span class="sxs-lookup"><span data-stu-id="53537-124">Whether texture coordinates should be generated: [**gluQuadricTexture**](gluquadrictexture.md)</span></span>
    -   <span data-ttu-id="53537-125">應將 quadric 的哪個端視為外部，並將其置於： [ **gluQuadricOrientation**](gluquadricorientation.md)</span><span class="sxs-lookup"><span data-stu-id="53537-125">Which side of the quadric should be considered the outside and which the inside: [**gluQuadricOrientation**](gluquadricorientation.md)</span></span>
    -   <span data-ttu-id="53537-126">是否應將 quadric 繪製成一組多邊形、線條或點： [ **gluQuadricDrawStyle**](gluquadricdrawstyle.md)</span><span class="sxs-lookup"><span data-stu-id="53537-126">Whether the quadric should be drawn as a set of polygons, lines, or points: [**gluQuadricDrawStyle**](gluquadricdrawstyle.md)</span></span>
3.  <span data-ttu-id="53537-127">指定轉譯樣式之後，針對所需的 quadric 物件類型叫用轉譯函數： [**gluSphere**](glusphere.md)、 [**gluCylinder**](glucylinder.md)、 [**gluDisk**](gludisk.md)或 [**gluPartialDisk**](glupartialdisk.md)。</span><span class="sxs-lookup"><span data-stu-id="53537-127">After specifying the rendering style, invoke the rendering function for the desired type of quadric object: [**gluSphere**](glusphere.md), [**gluCylinder**](glucylinder.md), [**gluDisk**](gludisk.md), or [**gluPartialDisk**](glupartialdisk.md).</span></span>

    <span data-ttu-id="53537-128">如果在轉譯期間發生錯誤，則會叫用您以 [*gluQuadricCallBack*](gluquadric.md) 指定的錯誤處理函式。</span><span class="sxs-lookup"><span data-stu-id="53537-128">If an error occurs during rendering, the error-handling function you've specified with [*gluQuadricCallBack*](gluquadric.md) is invoked.</span></span>

<span data-ttu-id="53537-129">使用 *\* 半徑*、*高度* 和類似的引數（而不是 [**glScale**](glscale.md)函式）來調整 quadrics，如此您就不需要重新標準化為產生的任何單位長度法線。</span><span class="sxs-lookup"><span data-stu-id="53537-129">Use the *\*Radius*, *height*, and similar arguments, rather than the [**glScale**](glscale.md) function, to scale the quadrics, so that you don't have to renormalize any unit-length normals that are generated.</span></span> <span data-ttu-id="53537-130">若要以更精細的細微性來強制執行光源計算，尤其是當材質 specularity 很高時，請將 *迴圈* 和 *堆疊* 引數設定為1以外的值。</span><span class="sxs-lookup"><span data-stu-id="53537-130">To force lighting calculations at a finer granularity, especially if the material specularity is high, set the *loops* and *stacks* arguments to values other than 1.</span></span>

 

 




