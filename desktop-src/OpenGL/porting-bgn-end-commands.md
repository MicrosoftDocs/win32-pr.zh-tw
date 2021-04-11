---
title: 移植 bgn/end 命令
description: 鳶尾花 GL 使用 begin/end 範例，但每個圖形基本功能各有不同的函式。
ms.assetid: 4191344b-614a-42d6-8a31-7a708f17371e
keywords:
- 鳶尾花 GL 移植、bgn/結束命令
- 從鳶尾花 GL、bgn/end 命令移植
- 從鳶尾花 GL 移植至 OpenGL、bgn/end 命令
- 鳶尾花 GL、bgn/end 命令的 OpenGL 移植
- 繪圖函數、bgn/end 命令
- bgn/end 命令
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c25118d4e5050ea22d4b18fab596dfb9c92f562e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372512"
---
# <a name="porting-bgnend-commands"></a><span data-ttu-id="59691-109">移植 bgn/end 命令</span><span class="sxs-lookup"><span data-stu-id="59691-109">Porting bgn/end Commands</span></span>

<span data-ttu-id="59691-110">鳶尾花 GL 使用 begin/end 範例，但每個圖形基本功能各有不同的函式。</span><span class="sxs-lookup"><span data-stu-id="59691-110">IRIS GL uses the begin/end paradigm but has a different function for each graphics primitive.</span></span> <span data-ttu-id="59691-111">例如，您可能會使用 **bgnpolygon** 和 **endpolygon** 來繪製多邊形，並使用 **bgnline** 和 **endline** 來繪製線條。</span><span class="sxs-lookup"><span data-stu-id="59691-111">For example, you probably use **bgnpolygon** and **endpolygon** to draw polygons, and **bgnline** and **endline** to draw lines.</span></span> <span data-ttu-id="59691-112">在 OpenGL 中，您可以使用 [**glBegin**](glbegin.md)  /  [**glEnd**](glend.md)結構。</span><span class="sxs-lookup"><span data-stu-id="59691-112">In OpenGL, you use the [**glBegin**](glbegin.md) / [**glEnd**](glend.md) structure for both.</span></span> <span data-ttu-id="59691-113">在 OpenGL 中，您可以藉由封入一系列的函式來繪製大部分的幾何物件，這些函式會指定 **glBegin** 與 **glEnd** 呼叫配對之間的頂點、法線、材質和色彩。</span><span class="sxs-lookup"><span data-stu-id="59691-113">In OpenGL you draw most geometric objects by enclosing a series of functions that specify vertices, normals, textures, and colors between pairs of **glBegin** and **glEnd** calls.</span></span> <span data-ttu-id="59691-114">例如：</span><span class="sxs-lookup"><span data-stu-id="59691-114">For example:</span></span>

``` syntax
void glBegin( GLenum mode) ; 
   /* vertex list, colors, normals, textures, materials */ 
void glEnd( void );
```

<span data-ttu-id="59691-115">**GlBegin** 函式會採用指定繪圖模式的單一參數，也就是基本。</span><span class="sxs-lookup"><span data-stu-id="59691-115">The **glBegin** function takes a single parameter that specifies the drawing mode, and thus the primitive.</span></span> <span data-ttu-id="59691-116">以下是一個可繪製多邊形和一行的 OpenGL 程式碼範例：</span><span class="sxs-lookup"><span data-stu-id="59691-116">Here's an OpenGL code sample that draws a polygon and then a line:</span></span>

``` syntax
glBegin( GL_POLYGON ) ; 
   glVertex2f(20.0, 10.0); 
   glVertex2f(10.0, 30.0); 
   glVertex2f(20.0, 50.0); 
   glVertex2f(40.0, 50.0); 
   glVertex2f(50.0, 30.0); 
   glVertex2f(40.0, 10.0); 
glEnd(); 
glBegin( GL_LINES ) ; 
   glVertex2i(100,100); 
   glVertex2i(500,500); 
glEnd();
```

<span data-ttu-id="59691-117">使用 OpenGL，您可以藉由指定不同的 [**glBegin**](glbegin.md)參數來繪製不同的幾何物件。</span><span class="sxs-lookup"><span data-stu-id="59691-117">With OpenGL, you draw different geometric objects by specifying different parameters for [**glBegin**](glbegin.md).</span></span> <span data-ttu-id="59691-118">下表列出對應至相等鳶尾花 GL 函數的 OpenGL **glBegin** 參數。</span><span class="sxs-lookup"><span data-stu-id="59691-118">The following table lists the OpenGL **glBegin** parameters that correspond to equivalent IRIS GL functions.</span></span>



| <span data-ttu-id="59691-119">鳶尾花 GL 函數</span><span class="sxs-lookup"><span data-stu-id="59691-119">IRIS GL function</span></span>  | <span data-ttu-id="59691-120">GlBegin 模式的值</span><span class="sxs-lookup"><span data-stu-id="59691-120">Value of glBegin mode</span></span> | <span data-ttu-id="59691-121">意義</span><span class="sxs-lookup"><span data-stu-id="59691-121">Meaning</span></span>                                                                                  |
|-------------------|-----------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="59691-122">**bgnpoint**</span><span class="sxs-lookup"><span data-stu-id="59691-122">**bgnpoint**</span></span>      | <span data-ttu-id="59691-123">GL \_ 點</span><span class="sxs-lookup"><span data-stu-id="59691-123">GL\_POINTS</span></span>            | <span data-ttu-id="59691-124">個別的點。</span><span class="sxs-lookup"><span data-stu-id="59691-124">Individual points.</span></span>                                                                       |
| <span data-ttu-id="59691-125">**bgnline**</span><span class="sxs-lookup"><span data-stu-id="59691-125">**bgnline**</span></span>       | <span data-ttu-id="59691-126">GL \_ 行 \_ 帶</span><span class="sxs-lookup"><span data-stu-id="59691-126">GL\_LINE\_STRIP</span></span>       | <span data-ttu-id="59691-127">一連串連接的線段。</span><span class="sxs-lookup"><span data-stu-id="59691-127">Series of connected line segments.</span></span>                                                       |
| <span data-ttu-id="59691-128">**bgnclosedline**</span><span class="sxs-lookup"><span data-stu-id="59691-128">**bgnclosedline**</span></span> | <span data-ttu-id="59691-129">GL \_ 線路 \_ 迴圈</span><span class="sxs-lookup"><span data-stu-id="59691-129">GL\_LINE\_LOOP</span></span>        | <span data-ttu-id="59691-130">一系列連接的直線線段，在第一個和最後一個頂點之間加入區段。</span><span class="sxs-lookup"><span data-stu-id="59691-130">Series of connected line segments, with a segment added between first and last vertices.</span></span> |
|                   | <span data-ttu-id="59691-131">GL \_ 行</span><span class="sxs-lookup"><span data-stu-id="59691-131">GL\_LINES</span></span>             | <span data-ttu-id="59691-132">成對的頂點，會轉譯為個別的線段。</span><span class="sxs-lookup"><span data-stu-id="59691-132">Pairs of vertices interpreted as individual line segments.</span></span>                               |
| <span data-ttu-id="59691-133">**bgnpolygon**</span><span class="sxs-lookup"><span data-stu-id="59691-133">**bgnpolygon**</span></span>    | <span data-ttu-id="59691-134">GL \_ 多邊形</span><span class="sxs-lookup"><span data-stu-id="59691-134">GL\_POLYGON</span></span>           | <span data-ttu-id="59691-135">簡單凸邊的界限。</span><span class="sxs-lookup"><span data-stu-id="59691-135">Boundary of a simple convex polygon.</span></span>                                                     |
|                   | <span data-ttu-id="59691-136">GL \_ 三角形</span><span class="sxs-lookup"><span data-stu-id="59691-136">GL\_TRIANGLES</span></span>         | <span data-ttu-id="59691-137">被解釋為三角形的三倍頂點。</span><span class="sxs-lookup"><span data-stu-id="59691-137">Triples of vertices interpreted as triangles.</span></span>                                            |
| <span data-ttu-id="59691-138">**bgntmesh**</span><span class="sxs-lookup"><span data-stu-id="59691-138">**bgntmesh**</span></span>      | <span data-ttu-id="59691-139">GL \_ 三角形 \_ 條紋</span><span class="sxs-lookup"><span data-stu-id="59691-139">GL\_TRIANGLE\_STRIP</span></span>   | <span data-ttu-id="59691-140">三角形的連結去除。</span><span class="sxs-lookup"><span data-stu-id="59691-140">Linked strips of triangles.</span></span>                                                              |
|                   | <span data-ttu-id="59691-141">GL \_ 三角形 \_ 風扇</span><span class="sxs-lookup"><span data-stu-id="59691-141">GL\_TRIANGLE\_FAN</span></span>     | <span data-ttu-id="59691-142">三角形的連結風扇。</span><span class="sxs-lookup"><span data-stu-id="59691-142">Linked fans of triangles.</span></span>                                                                |
|                   | <span data-ttu-id="59691-143">GL \_ 四邊形</span><span class="sxs-lookup"><span data-stu-id="59691-143">GL\_QUADS</span></span>             | <span data-ttu-id="59691-144">解釋為 quadrilaterals 的頂點時。</span><span class="sxs-lookup"><span data-stu-id="59691-144">Quadruples of vertices interpreted as quadrilaterals.</span></span>                                    |
| <span data-ttu-id="59691-145">**bgnqstrip**</span><span class="sxs-lookup"><span data-stu-id="59691-145">**bgnqstrip**</span></span>     | <span data-ttu-id="59691-146">GL \_ 四 \_ 條</span><span class="sxs-lookup"><span data-stu-id="59691-146">GL\_QUAD\_STRIP</span></span>       | <span data-ttu-id="59691-147">Quadrilaterals 的連結塊。</span><span class="sxs-lookup"><span data-stu-id="59691-147">Linked strips of quadrilaterals.</span></span>                                                         |



 

<span data-ttu-id="59691-148">如需三角形網格、條紋和風扇之間差異的詳細討論，請參閱 [移植三角形](porting-triangles.md)。</span><span class="sxs-lookup"><span data-stu-id="59691-148">For a detailed discussion of the differences between triangle meshes, strips, and fans, see [Porting Triangles](porting-triangles.md).</span></span>

<span data-ttu-id="59691-149">您可以在 [**glBegin**](glbegin.md)  /  [**glEnd**](glend.md)配對之間指定的頂點數目沒有任何限制。</span><span class="sxs-lookup"><span data-stu-id="59691-149">There is no limit to the number of vertices you can specify between a [**glBegin**](glbegin.md) / [**glEnd**](glend.md) pair.</span></span>

<span data-ttu-id="59691-150">除了在 **glBegin**  /  **glEnd** 配對內指定頂點之外，您還可以指定目前的一般材質和目前的材質座標，以及目前的色彩。</span><span class="sxs-lookup"><span data-stu-id="59691-150">In addition to specifying vertices inside a **glBegin** / **glEnd** pair, you can specify a current normal, current texture coordinates, and a current color.</span></span> <span data-ttu-id="59691-151">下表列出 **glBegin**  /  **glEnd** 配對內的有效命令。</span><span class="sxs-lookup"><span data-stu-id="59691-151">The following table lists the commands valid inside a **glBegin** / **glEnd** pair.</span></span>



| <span data-ttu-id="59691-152">鳶尾花 GL 函數</span><span class="sxs-lookup"><span data-stu-id="59691-152">IRIS GL function</span></span>        | <span data-ttu-id="59691-153">OpenGL 函數</span><span class="sxs-lookup"><span data-stu-id="59691-153">OpenGL function</span></span>                                                      | <span data-ttu-id="59691-154">意義</span><span class="sxs-lookup"><span data-stu-id="59691-154">Meaning</span></span>                                          |
|-------------------------|----------------------------------------------------------------------|--------------------------------------------------|
| <span data-ttu-id="59691-155">**v2**、 **v3**、 **v4**</span><span class="sxs-lookup"><span data-stu-id="59691-155">**v2**, **v3**, **v4**</span></span>  | [<span data-ttu-id="59691-156">glVertex</span><span class="sxs-lookup"><span data-stu-id="59691-156">glVertex</span></span>](glvertex-functions.md)                                   | <span data-ttu-id="59691-157">設定頂點座標。</span><span class="sxs-lookup"><span data-stu-id="59691-157">Sets vertex coordinates.</span></span>                         |
| <span data-ttu-id="59691-158">**RGBcolor**、 **cpack**</span><span class="sxs-lookup"><span data-stu-id="59691-158">**RGBcolor**, **cpack**</span></span> | [<span data-ttu-id="59691-159">glColor</span><span class="sxs-lookup"><span data-stu-id="59691-159">glColor</span></span>](glcolor-functions.md)                                     | <span data-ttu-id="59691-160">設定目前的色彩。</span><span class="sxs-lookup"><span data-stu-id="59691-160">Sets current color.</span></span>                              |
| <span data-ttu-id="59691-161">**color**</span><span class="sxs-lookup"><span data-stu-id="59691-161">**color**</span></span>               | [<span data-ttu-id="59691-162">glIndex</span><span class="sxs-lookup"><span data-stu-id="59691-162">glIndex</span></span>](glindex-functions.md)                                     | <span data-ttu-id="59691-163">設定目前的色彩索引。</span><span class="sxs-lookup"><span data-stu-id="59691-163">Sets current color index.</span></span>                        |
| <span data-ttu-id="59691-164">**n3f**</span><span class="sxs-lookup"><span data-stu-id="59691-164">**n3f**</span></span>                 | [<span data-ttu-id="59691-165">glNormal</span><span class="sxs-lookup"><span data-stu-id="59691-165">glNormal</span></span>](glnormal-functions.md)                                   | <span data-ttu-id="59691-166">設定一般向量座標。</span><span class="sxs-lookup"><span data-stu-id="59691-166">Sets normal vector coordinates.</span></span>                  |
|                         | [<span data-ttu-id="59691-167">glEvalCoord</span><span class="sxs-lookup"><span data-stu-id="59691-167">glEvalCoord</span></span>](glevalcoord-functions.md)                             | <span data-ttu-id="59691-168">評估已啟用一維和二維的地圖。</span><span class="sxs-lookup"><span data-stu-id="59691-168">Evaluates enabled one- and two-dimensional maps.</span></span> |
| <span data-ttu-id="59691-169">**callobj**</span><span class="sxs-lookup"><span data-stu-id="59691-169">**callobj**</span></span>             | <span data-ttu-id="59691-170">[**glCallList**](glcalllist.md)、 [ **glCallLists**](glcalllists.md)</span><span class="sxs-lookup"><span data-stu-id="59691-170">[**glCallList**](glcalllist.md), [**glCallLists**](glcalllists.md)</span></span> | <span data-ttu-id="59691-171"> (s) 執行顯示清單。</span><span class="sxs-lookup"><span data-stu-id="59691-171">Executes display list(s).</span></span>                        |
| <bpt id="p1">**</bpt>t2<ept id="p1">**</ept>                  | [<span data-ttu-id="59691-173">glTexCoord</span><span class="sxs-lookup"><span data-stu-id="59691-173">glTexCoord</span></span>](gltexcoord-functions.md)                               | <span data-ttu-id="59691-174">設定材質座標。</span><span class="sxs-lookup"><span data-stu-id="59691-174">Sets texture coordinates.</span></span>                        |
|                         | [<span data-ttu-id="59691-175">glEdgeFlag</span><span class="sxs-lookup"><span data-stu-id="59691-175">glEdgeFlag</span></span>](gledgeflag-functions.md)                               | <span data-ttu-id="59691-176">控制繪圖邊緣。</span><span class="sxs-lookup"><span data-stu-id="59691-176">Controls drawing edges.</span></span>                          |
| <span data-ttu-id="59691-177">**lmbind**</span><span class="sxs-lookup"><span data-stu-id="59691-177">**lmbind**</span></span>              | [<span data-ttu-id="59691-178">glMaterial</span><span class="sxs-lookup"><span data-stu-id="59691-178">glMaterial</span></span>](glmaterial-functions.md)                               | <span data-ttu-id="59691-179">設定材質屬性。</span><span class="sxs-lookup"><span data-stu-id="59691-179">Sets material properties.</span></span>                        |



 

> [!Note]
>
> <span data-ttu-id="59691-180">如果您使用上述表格中所列的任何 OpenGL 函式，而不是在 [**glBegin**](glbegin.md)  /  [**glEnd**](glend.md)組內，您將會得到無法預期的結果，或可能發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="59691-180">If you use any OpenGL function other than those listed in the preceding table inside a [**glBegin**](glbegin.md) / [**glEnd**](glend.md) pair, you'll get unpredictable results, or possibly an error.</span></span>

 

 

 




