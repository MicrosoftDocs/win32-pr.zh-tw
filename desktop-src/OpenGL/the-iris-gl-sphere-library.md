---
title: 鳶尾花 GL 球體程式庫
description: OpenGL 不支援鳶尾花 GL 球體程式庫。 您可以使用 X.GLU 隊程式庫中的 quadrics 常式來取代球體程式庫呼叫。 如需 X.GLU 隊程式庫的詳細資訊，請參閱 Open GL 程式設計指南和 OpenGL 公用程式程式庫。
ms.assetid: 2b7e6a3d-d2d0-4b54-8dff-8c4d6b113007
keywords:
- 鳶尾花 GL 移植，球體程式庫
- 從鳶尾花 GL、球體程式庫移植
- 從鳶尾花 GL、球體程式庫移植至 OpenGL
- 從鳶尾花 GL、球體程式庫移植的 OpenGL
- 繪圖函數、球體程式庫
- 球體程式庫
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 586974c5874aee73121e536cbadca4564a18c250
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301199"
---
# <a name="the-iris-gl-sphere-library"></a><span data-ttu-id="678f5-111">鳶尾花 GL 球體程式庫</span><span class="sxs-lookup"><span data-stu-id="678f5-111">The IRIS GL Sphere Library</span></span>

<span data-ttu-id="678f5-112">OpenGL 不支援鳶尾花 GL 球體程式庫。</span><span class="sxs-lookup"><span data-stu-id="678f5-112">OpenGL does not support the IRIS GL sphere library.</span></span> <span data-ttu-id="678f5-113">您可以使用 X.GLU 隊程式庫中的 quadrics 常式來取代球體程式庫呼叫。</span><span class="sxs-lookup"><span data-stu-id="678f5-113">You can replace your sphere library calls with quadrics routines from the GLU library.</span></span> <span data-ttu-id="678f5-114">如需 X.GLU 隊程式庫的詳細資訊，請參閱 *OPEN GL 程式設計指南* 和 [OpenGL 公用程式程式庫](opengl-utility-library.md)。</span><span class="sxs-lookup"><span data-stu-id="678f5-114">For more information about the GLU library, see the *Open GL Programming Guide* and [OpenGL Utility Library](opengl-utility-library.md).</span></span>

<span data-ttu-id="678f5-115">下表列出 OpenGL quadrics 函數。</span><span class="sxs-lookup"><span data-stu-id="678f5-115">The following table lists the OpenGL quadrics functions.</span></span>



| <span data-ttu-id="678f5-116">OpenGL 函數</span><span class="sxs-lookup"><span data-stu-id="678f5-116">OpenGL function</span></span>                                        | <span data-ttu-id="678f5-117">意義</span><span class="sxs-lookup"><span data-stu-id="678f5-117">Meaning</span></span>                                                          |
|--------------------------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="678f5-118">**gluNewQuadric**</span><span class="sxs-lookup"><span data-stu-id="678f5-118">**gluNewQuadric**</span></span>](glunewquadric.md)                 | <span data-ttu-id="678f5-119">建立新的 quadric 物件。</span><span class="sxs-lookup"><span data-stu-id="678f5-119">Creates a new quadric object.</span></span>                                    |
| [<span data-ttu-id="678f5-120">**gluDeleteQuadric**</span><span class="sxs-lookup"><span data-stu-id="678f5-120">**gluDeleteQuadric**</span></span>](gludeletequadric.md)           | <span data-ttu-id="678f5-121">刪除 quadric 物件。</span><span class="sxs-lookup"><span data-stu-id="678f5-121">Deletes a quadric object.</span></span>                                        |
| [<span data-ttu-id="678f5-122">*gluQuadricCallback*</span><span class="sxs-lookup"><span data-stu-id="678f5-122">*gluQuadricCallback*</span></span>](gluquadric.md)                 | <span data-ttu-id="678f5-123">將回呼與 quadric 物件產生關聯，以進行錯誤處理。</span><span class="sxs-lookup"><span data-stu-id="678f5-123">Associates a callback with a quadric object, for error handling.</span></span> |
| [<span data-ttu-id="678f5-124">**gluQuadricNormals**</span><span class="sxs-lookup"><span data-stu-id="678f5-124">**gluQuadricNormals**</span></span>](gluquadricnormals.md)         | <span data-ttu-id="678f5-125">指定法線：無法線，每個臉部各一個，或每個頂點一個。</span><span class="sxs-lookup"><span data-stu-id="678f5-125">Specifies normals: no normals, one per face, or one per vertex.</span></span>  |
| [<span data-ttu-id="678f5-126">**gluQuadricOrientation**</span><span class="sxs-lookup"><span data-stu-id="678f5-126">**gluQuadricOrientation**</span></span>](gluquadricorientation.md) | <span data-ttu-id="678f5-127">指定法線的方向：向外或向外。</span><span class="sxs-lookup"><span data-stu-id="678f5-127">Specifies direction of normals: outward or inward.</span></span>               |
| [<span data-ttu-id="678f5-128">**gluQuadricTexture**</span><span class="sxs-lookup"><span data-stu-id="678f5-128">**gluQuadricTexture**</span></span>](gluquadrictexture.md)         | <span data-ttu-id="678f5-129">開啟或關閉材質座標產生。</span><span class="sxs-lookup"><span data-stu-id="678f5-129">Turns texture-coordinate generation on or off.</span></span>                   |
| [<span data-ttu-id="678f5-130">**gluQuadricDrawstyle**</span><span class="sxs-lookup"><span data-stu-id="678f5-130">**gluQuadricDrawstyle**</span></span>](gluquadricdrawstyle.md)     | <span data-ttu-id="678f5-131">指定繪製樣式：多邊形、線條、點等等。</span><span class="sxs-lookup"><span data-stu-id="678f5-131">Specifies drawing style: polygons, lines, points, and so on.</span></span>     |
| [<span data-ttu-id="678f5-132">**gluSphere**</span><span class="sxs-lookup"><span data-stu-id="678f5-132">**gluSphere**</span></span>](glusphere.md)                         | <span data-ttu-id="678f5-133">繪製球體。</span><span class="sxs-lookup"><span data-stu-id="678f5-133">Draws a sphere.</span></span>                                                  |
| [<span data-ttu-id="678f5-134">**gluCylinder**</span><span class="sxs-lookup"><span data-stu-id="678f5-134">**gluCylinder**</span></span>](glucylinder.md)                     | <span data-ttu-id="678f5-135">繪製圓柱圖或圓錐圖。</span><span class="sxs-lookup"><span data-stu-id="678f5-135">Draws a cylinder or cone.</span></span>                                        |
| [<span data-ttu-id="678f5-136">**gluPartialDisk**</span><span class="sxs-lookup"><span data-stu-id="678f5-136">**gluPartialDisk**</span></span>](glupartialdisk.md)               | <span data-ttu-id="678f5-137">繪製弧形。</span><span class="sxs-lookup"><span data-stu-id="678f5-137">Draws an arc.</span></span>                                                    |
| [<span data-ttu-id="678f5-138">**gluDisk**</span><span class="sxs-lookup"><span data-stu-id="678f5-138">**gluDisk**</span></span>](gludisk.md)                             | <span data-ttu-id="678f5-139">繪製圓形或磁片。</span><span class="sxs-lookup"><span data-stu-id="678f5-139">Draws a circle or disk.</span></span>                                          |



 

<span data-ttu-id="678f5-140">您可以針對想要以類似方式轉譯的所有 quadrics 使用一個 quadric 物件。</span><span class="sxs-lookup"><span data-stu-id="678f5-140">You can use one quadric object for all quadrics you want to render in similar ways.</span></span> <span data-ttu-id="678f5-141">下列程式碼範例會使用兩個 quadric 物件來繪製四個 quadrics，兩個都有紋理。</span><span class="sxs-lookup"><span data-stu-id="678f5-141">The following code sample uses two quadric objects to draw four quadrics, two of them textured.</span></span>


```C++
GLUquadricObj    *texturedQuad, *plainQuad; 
 
texturedQuad = gluNewQuadric(void); 
gluQuadricTexture(texturedQuad, GL_TRUE); 
gluQuadricOrientation(texturedQuad, GLU_OUTSIDE); 
gluQuadricDrawStyle(texturedQuad, GLU_FILL); 
 
plainQuad = gluNewQuadric(void); 
gluQuadricDrawStyle(plainQuad, GLU_LINE); 
 
glColor3f (1.0, 1.0, 1.0); 
 
gluSphere(texturedQuad, 5.0, 20, 20); 
glTranslatef(10.0, 10.0, 0.0); 
gluCylinder(texturedQuad, 2.5, 5, 5, 10, 10); 
glTranslatef(10.0, 10.0, 0.0); 
gluDisk(plainQuad, 2.0, 5.0, 10, 10); 
glTranslatef(10.0, 10.0, 0.0); 
gluSphere(plainQuad, 5.0, 20, 20);
```



 

 




