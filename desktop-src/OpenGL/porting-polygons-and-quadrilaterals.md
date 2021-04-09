---
title: 移植多邊形和 Quadrilaterals
description: 移植多邊形和 quadrilaterals 時，請記住下列幾點
ms.assetid: 2b752437-caf9-4336-a906-d06b2aa8bb04
keywords:
- 鳶尾花 GL 移植，quadrilaterals
- 從鳶尾花 GL、quadrilaterals 移植
- 從鳶尾花 GL （quadrilaterals）移植至 OpenGL
- 從鳶尾花 GL quadrilaterals 的 OpenGL 移植
- 繪圖函數，quadrilaterals
- quadrilaterals
- 鳶尾花 GL 移植，多邊形
- 從鳶尾花 GL、多邊形進行移植
- 從鳶尾花 GL、多邊形移植至 OpenGL
- 從鳶尾花 GL、多邊形的 OpenGL 移植
- 繪圖函數、多邊形
- 多邊形，從鳶尾花 GL 進行移植
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c95d654b101c5eeb86cfcc4ea342e8196b8749e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674535"
---
# <a name="porting-polygons-and-quadrilaterals"></a><span data-ttu-id="0ad15-115">移植多邊形和 Quadrilaterals</span><span class="sxs-lookup"><span data-stu-id="0ad15-115">Porting Polygons and Quadrilaterals</span></span>

<span data-ttu-id="0ad15-116">移植多邊形和 quadrilaterals 時，請記住下列幾點：</span><span class="sxs-lookup"><span data-stu-id="0ad15-116">Keep the following points in mind when porting polygons and quadrilaterals:</span></span>

-   <span data-ttu-id="0ad15-117">**凹** (**TRUE**) 沒有直接對等專案。</span><span class="sxs-lookup"><span data-stu-id="0ad15-117">There is no direct equivalent for **concave**(**TRUE**).</span></span> <span data-ttu-id="0ad15-118">相反地，您可以使用 X.GLU 隊中的鑲嵌式常式，如 [鑲嵌多邊形](tessellating-polygons.md)所述。</span><span class="sxs-lookup"><span data-stu-id="0ad15-118">Instead you can use the tessellation routines in the GLU, described in [Tessellating Polygons](tessellating-polygons.md).</span></span>
-   <span data-ttu-id="0ad15-119">多邊形模式的設定方式不同。</span><span class="sxs-lookup"><span data-stu-id="0ad15-119">Polygon modes are set differently.</span></span>
-   <span data-ttu-id="0ad15-120">這些多邊形繪圖函式在 OpenGL 中沒有直接對等專案： **poly** 系列的常式; **polf** 系列的常式; **pmv**、 **寮國** 和 **pclos**; **rpmv** 和 **rpdr**; **splf**;和 **spclos**。</span><span class="sxs-lookup"><span data-stu-id="0ad15-120">These polygon drawing functions have no direct equivalents in OpenGL: the **poly** family of routines; the **polf** family of routines; **pmv**, **pdr**, and **pclos**; **rpmv** and **rpdr**; **splf**; and **spclos**.</span></span>

<span data-ttu-id="0ad15-121">如果您的鳶尾花 GL 程式碼使用這些功能，您必須使用 [**glBegin**](glbegin.md) ( GL 多邊形 ) 來重寫程式碼 \_ 。</span><span class="sxs-lookup"><span data-stu-id="0ad15-121">If your IRIS GL code uses these functions, you'll have to rewrite the code using [**glBegin**](glbegin.md)( GL\_POLYGON ).</span></span>

<span data-ttu-id="0ad15-122">下表列出鳶尾花 GL 多邊形繪圖函式及其對等的 OpenGL 函數。</span><span class="sxs-lookup"><span data-stu-id="0ad15-122">The following table lists the IRIS GL polygon drawing functions and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="0ad15-123">鳶尾花 GL 函數</span><span class="sxs-lookup"><span data-stu-id="0ad15-123">IRIS GL function</span></span>         | <span data-ttu-id="0ad15-124">OpenGL 函數</span><span class="sxs-lookup"><span data-stu-id="0ad15-124">OpenGL function</span></span>                                                    | <span data-ttu-id="0ad15-125">意義</span><span class="sxs-lookup"><span data-stu-id="0ad15-125">Meaning</span></span>                                                 |
|--------------------------|--------------------------------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="0ad15-126">**bgnpolygonendpolygon**</span><span class="sxs-lookup"><span data-stu-id="0ad15-126">**bgnpolygonendpolygon**</span></span> | <span data-ttu-id="0ad15-127">[**glBegin**](glbegin.md) ( GL \_ 多邊形 ) [ **glEnd**](glend.md)</span><span class="sxs-lookup"><span data-stu-id="0ad15-127">[**glBegin**](glbegin.md) ( GL\_POLYGON )[**glEnd**](glend.md)</span></span>   | <span data-ttu-id="0ad15-128">頂點：定義簡單凸邊的界限。</span><span class="sxs-lookup"><span data-stu-id="0ad15-128">Vertices define boundary of a simple convex polygon.</span></span>    |
|                          | <span data-ttu-id="0ad15-129">**glBegin** ( GL \_ 四邊形 ) **glEnd**</span><span class="sxs-lookup"><span data-stu-id="0ad15-129">**glBegin**( GL\_QUADS )**glEnd**</span></span><br/>                       | <span data-ttu-id="0ad15-130">將頂點的時解讀為 quadrilaterals。</span><span class="sxs-lookup"><span data-stu-id="0ad15-130">Interprets quadruples of vertices as quadrilaterals.</span></span>    |
| <span data-ttu-id="0ad15-131">**bgnqstripendqstrip**</span><span class="sxs-lookup"><span data-stu-id="0ad15-131">**bgnqstripendqstrip**</span></span>   | <span data-ttu-id="0ad15-132">[**glBegin**](glbegin.md) ( GL \_ QUAD \_ ) **glEnd**</span><span class="sxs-lookup"><span data-stu-id="0ad15-132">[**glBegin**](glbegin.md) ( GL\_QUAD\_STRIP )**glEnd**</span></span><br/> | <span data-ttu-id="0ad15-133">將頂點解釋為 quadrilaterals 的連結塊。</span><span class="sxs-lookup"><span data-stu-id="0ad15-133">Interprets vertices as linked strips of quadrilaterals.</span></span> |
|                          | [<span data-ttu-id="0ad15-134">glEdgeFlag</span><span class="sxs-lookup"><span data-stu-id="0ad15-134">glEdgeFlag</span></span>](gledgeflag-functions.md)                             |                                                         |
| <span data-ttu-id="0ad15-135">**polymode**</span><span class="sxs-lookup"><span data-stu-id="0ad15-135">**polymode**</span></span>             | [<span data-ttu-id="0ad15-136">**glPolygonMode**</span><span class="sxs-lookup"><span data-stu-id="0ad15-136">**glPolygonMode**</span></span>](glpolygonmode.md)                             | <span data-ttu-id="0ad15-137">設定多邊形繪圖模式。</span><span class="sxs-lookup"><span data-stu-id="0ad15-137">Sets polygon drawing mode.</span></span>                              |
| <span data-ttu-id="0ad15-138">**rectrectf**</span><span class="sxs-lookup"><span data-stu-id="0ad15-138">**rectrectf**</span></span><br/> | [<span data-ttu-id="0ad15-139">glRect</span><span class="sxs-lookup"><span data-stu-id="0ad15-139">glRect</span></span>](glrect-functions.md)                                     | <span data-ttu-id="0ad15-140">繪製矩形。</span><span class="sxs-lookup"><span data-stu-id="0ad15-140">Draws a rectangle.</span></span>                                      |
| <span data-ttu-id="0ad15-141">**sboxsboxf**</span><span class="sxs-lookup"><span data-stu-id="0ad15-141">**sboxsboxf**</span></span><br/> |                                                                    | <span data-ttu-id="0ad15-142">繪製螢幕對齊的矩形。</span><span class="sxs-lookup"><span data-stu-id="0ad15-142">Draws a screen-aligned rectangle.</span></span>                       |



 

<span data-ttu-id="0ad15-143">??</span><span class="sxs-lookup"><span data-stu-id="0ad15-143">??</span></span>

## <a name="porting-polygon-modes"></a><span data-ttu-id="0ad15-144">移植多邊形模式</span><span class="sxs-lookup"><span data-stu-id="0ad15-144">Porting Polygon Modes</span></span>

<span data-ttu-id="0ad15-145">[OpenGL 函數 [**glPolygonMode**](glpolygonmode.md) ] 可讓您指定多邊形的哪一端 (要套用至哪一側的背景) 。</span><span class="sxs-lookup"><span data-stu-id="0ad15-145">The OpenGL function [**glPolygonMode**](glpolygonmode.md) lets you specify which side of a polygon (the back or the front) the mode applies to.</span></span> <span data-ttu-id="0ad15-146">其語法如下：</span><span class="sxs-lookup"><span data-stu-id="0ad15-146">Its syntax is:</span></span>

``` syntax
void glPolygonMode( GLenum face, GLenum mode ); 
 
```

<span data-ttu-id="0ad15-147">其中的臉部是下列其中一項：</span><span class="sxs-lookup"><span data-stu-id="0ad15-147">where face is one of:</span></span>



|                      |                                                            |
|----------------------|------------------------------------------------------------|
| <span data-ttu-id="0ad15-148">GL \_ FRONT</span><span class="sxs-lookup"><span data-stu-id="0ad15-148">GL\_FRONT</span></span>            | <span data-ttu-id="0ad15-149">適用于正面多邊形的模式</span><span class="sxs-lookup"><span data-stu-id="0ad15-149">mode which applies to front-facing polygons</span></span>                |
| <span data-ttu-id="0ad15-150">GL \_ 回</span><span class="sxs-lookup"><span data-stu-id="0ad15-150">GL\_BACK</span></span>             | <span data-ttu-id="0ad15-151">適用于後置多邊形的模式</span><span class="sxs-lookup"><span data-stu-id="0ad15-151">mode which applies to back-facing polygons</span></span>                 |
| <span data-ttu-id="0ad15-152">GL \_ 正面 \_ 和 \_ 背面</span><span class="sxs-lookup"><span data-stu-id="0ad15-152">GL\_FRONT\_AND\_BACK</span></span> | <span data-ttu-id="0ad15-153">適用于 front 和 back 多邊形的模式</span><span class="sxs-lookup"><span data-stu-id="0ad15-153">mode which applies to both front- and back-facing polygons</span></span> |



 

<span data-ttu-id="0ad15-154">GL \_ 前端 \_ 和 \_ 後端模式相當於鳶尾花 GL **polymode** 函數。</span><span class="sxs-lookup"><span data-stu-id="0ad15-154">The GL\_FRONT\_AND\_BACK mode is equivalent to the IRIS GL **polymode** function.</span></span> <span data-ttu-id="0ad15-155">下表列出鳶尾花 GL 多邊形模式及其對等的 OpenGL 模式。</span><span class="sxs-lookup"><span data-stu-id="0ad15-155">The following table lists IRIS GL polygon modes and their equivalent OpenGL modes.</span></span>



| <span data-ttu-id="0ad15-156">鳶尾花 GL 模式</span><span class="sxs-lookup"><span data-stu-id="0ad15-156">IRIS GL mode</span></span> | <span data-ttu-id="0ad15-157">OpenGL 模式</span><span class="sxs-lookup"><span data-stu-id="0ad15-157">OpenGL mode</span></span> | <span data-ttu-id="0ad15-158">意義</span><span class="sxs-lookup"><span data-stu-id="0ad15-158">Meaning</span></span>                                       |
|--------------|-------------|-----------------------------------------------|
| <span data-ttu-id="0ad15-159">PYM \_ 點</span><span class="sxs-lookup"><span data-stu-id="0ad15-159">PYM\_POINT</span></span>   | <span data-ttu-id="0ad15-160">GL \_ 點</span><span class="sxs-lookup"><span data-stu-id="0ad15-160">GL\_POINT</span></span>   | <span data-ttu-id="0ad15-161">將頂點繪製成點。</span><span class="sxs-lookup"><span data-stu-id="0ad15-161">Draws vertices as points.</span></span>                     |
| <span data-ttu-id="0ad15-162">PYM \_ 行</span><span class="sxs-lookup"><span data-stu-id="0ad15-162">PYM\_LINE</span></span>    | <span data-ttu-id="0ad15-163">GL \_ 線</span><span class="sxs-lookup"><span data-stu-id="0ad15-163">GL\_LINE</span></span>    | <span data-ttu-id="0ad15-164">將邊界邊緣繪製為線段。</span><span class="sxs-lookup"><span data-stu-id="0ad15-164">Draws boundary edges as line segments.</span></span>        |
| <span data-ttu-id="0ad15-165">PYM \_ 填滿</span><span class="sxs-lookup"><span data-stu-id="0ad15-165">PYM\_FILL</span></span>    | <span data-ttu-id="0ad15-166">GL \_ 填滿</span><span class="sxs-lookup"><span data-stu-id="0ad15-166">GL\_FILL</span></span>    | <span data-ttu-id="0ad15-167">繪製填滿的多邊形內部。</span><span class="sxs-lookup"><span data-stu-id="0ad15-167">Draws polygon interior filled.</span></span>                |
| <span data-ttu-id="0ad15-168">PYM \_ 空心</span><span class="sxs-lookup"><span data-stu-id="0ad15-168">PYM\_HOLLOW</span></span>  |             | <span data-ttu-id="0ad15-169">只填滿界限的內部圖元。</span><span class="sxs-lookup"><span data-stu-id="0ad15-169">Fills only interior pixels at the boundaries.</span></span> |



 

## <a name="porting-polygon-stipples"></a><span data-ttu-id="0ad15-170">移植多邊形 Stipples</span><span class="sxs-lookup"><span data-stu-id="0ad15-170">Porting Polygon Stipples</span></span>

<span data-ttu-id="0ad15-171">移植鳶尾花 GL 多邊形 stipples 時，請記住下列幾點：</span><span class="sxs-lookup"><span data-stu-id="0ad15-171">When porting IRIS GL polygon stipples, keep the following points in mind:</span></span>

-   <span data-ttu-id="0ad15-172">OpenGL 不會使用資料表進行多邊形 stipples;只保留一個 stipple 模式。</span><span class="sxs-lookup"><span data-stu-id="0ad15-172">OpenGL doesn't use tables for polygon stipples; only one stipple pattern is kept.</span></span> <span data-ttu-id="0ad15-173">您可以使用顯示清單來儲存不同的 stipple 模式。</span><span class="sxs-lookup"><span data-stu-id="0ad15-173">You can use display lists to store different stipple patterns.</span></span>
-   <span data-ttu-id="0ad15-174">OpenGL 多邊形 stipple 點陣圖大小一律為32x32 位模式。</span><span class="sxs-lookup"><span data-stu-id="0ad15-174">The OpenGL polygon stipple bitmap size is always a 32x32 bit pattern.</span></span>
-   <span data-ttu-id="0ad15-175">Stipple 編碼會受到 [**glPixelStore**](glpixelstore-functions.md)的影響。</span><span class="sxs-lookup"><span data-stu-id="0ad15-175">Stipple encoding is affected by [**glPixelStore**](glpixelstore-functions.md).</span></span>

<span data-ttu-id="0ad15-176">如需移植多邊形 stipples 的詳細資訊，請參閱 [移植圖元作業](porting-pixel-operations.md)。</span><span class="sxs-lookup"><span data-stu-id="0ad15-176">For more information on porting polygon stipples, see [Porting Pixel Operations](porting-pixel-operations.md).</span></span>

<span data-ttu-id="0ad15-177">下表列出鳶尾花 GL 多邊形 stipple 函數及其對等的 OpenGL 函數。</span><span class="sxs-lookup"><span data-stu-id="0ad15-177">The following table lists IRIS GL polygon stipple functions and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="0ad15-178">鳶尾花 GL 函數</span><span class="sxs-lookup"><span data-stu-id="0ad15-178">IRIS GL function</span></span> | <span data-ttu-id="0ad15-179">OpenGL 函數</span><span class="sxs-lookup"><span data-stu-id="0ad15-179">OpenGL function</span></span>                                    | <span data-ttu-id="0ad15-180">意義</span><span class="sxs-lookup"><span data-stu-id="0ad15-180">Meaning</span></span>                                               |
|------------------|----------------------------------------------------|-------------------------------------------------------|
| <span data-ttu-id="0ad15-181">**defpattern**</span><span class="sxs-lookup"><span data-stu-id="0ad15-181">**defpattern**</span></span>   | [<span data-ttu-id="0ad15-182">**glPolygonStipple**</span><span class="sxs-lookup"><span data-stu-id="0ad15-182">**glPolygonStipple**</span></span>](glpolygonstipple.md)       | <span data-ttu-id="0ad15-183">設定 stipple 模式。</span><span class="sxs-lookup"><span data-stu-id="0ad15-183">Sets the stipple pattern.</span></span>                             |
| <span data-ttu-id="0ad15-184">**setpattern**</span><span class="sxs-lookup"><span data-stu-id="0ad15-184">**setpattern**</span></span>   |                                                    | <span data-ttu-id="0ad15-185">OpenGL 只保留一個多邊形 stipple 模式。</span><span class="sxs-lookup"><span data-stu-id="0ad15-185">OpenGL keeps only one polygon stipple pattern.</span></span>        |
| <span data-ttu-id="0ad15-186">**system.windows.automation.peers.uielementautomationpeer.getpattern**</span><span class="sxs-lookup"><span data-stu-id="0ad15-186">**getpattern**</span></span>   | [<span data-ttu-id="0ad15-187">**glGetPolygonStipple**</span><span class="sxs-lookup"><span data-stu-id="0ad15-187">**glGetPolygonStipple**</span></span>](glgetpolygonstipple.md) | <span data-ttu-id="0ad15-188">傳回 stipple 點陣圖 (用來傳回索引) 。</span><span class="sxs-lookup"><span data-stu-id="0ad15-188">Returns the stipple bitmap (used to return an index).</span></span> |



 

<span data-ttu-id="0ad15-189">在 OpenGL 中，您可以藉由 \_ 將 GL 多邊形 STIPPLE 傳遞 \_ 為 [**glEnable**](glenable.md) 和 [**glDisable**](gldisable.md)的參數，來啟用和停用多邊形 stippling。</span><span class="sxs-lookup"><span data-stu-id="0ad15-189">In OpenGL, you enable and disable polygon stippling by passing GL\_POLYGON\_STIPPLE as a parameter for [**glEnable**](glenable.md) and [**glDisable**](gldisable.md).</span></span>

<span data-ttu-id="0ad15-190">下列 OpenGL 程式碼範例示範多邊形 stippling：</span><span class="sxs-lookup"><span data-stu-id="0ad15-190">The following OpenGL code sample demonstrates polygon stippling:</span></span>


```C++
void display(void) 
{ 
    GLubyte fly[] = { 
      0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 
      0x03, 0x80, 0x01, 0xC0, 0x06, 0xC0, 0x03, 0x60, 
      0x04, 0x60, 0x06, 0x20, 0x04, 0x30, 0x0C, 0x20, 
      0x04, 0x18, 0x18, 0x20, 0x04, 0x0C, 0x30, 0x20, 
      0x04, 0x06, 0x60, 0x20, 0x44, 0x03, 0xC0, 0x22, 
      0x44, 0x01, 0x80, 0x22, 0x44, 0x01, 0x80, 0x22, 
      0x44, 0x01, 0x80, 0x22, 0x44, 0x01, 0x80, 0x22, 
      0x44, 0x01, 0x80, 0x22, 0x44, 0x01, 0x80, 0x22, 
      0x66, 0x01, 0x80, 0x66, 0x33, 0x01, 0x80, 0xCC, 
      0x19, 0x81, 0x81, 0x98, 0x0C, 0xC1, 0x83, 0x30, 
      0x07, 0xe1, 0x87, 0xe0, 0x03, 0x3f, 0xfc, 0xc0, 
      0x03, 0x31, 0x8c, 0xc0, 0x03, 0x33, 0xcc, 0xc0, 
      0x06, 0x64, 0x26, 0x60, 0x0c, 0xcc, 0x33, 0x30, 
      0x18, 0xcc, 0x33, 0x18, 0x10, 0xc4, 0x23, 0x08, 
      0x10, 0x63, 0xC6, 0x08, 0x10, 0x30, 0x0c, 0x08, 
      0x10, 0x18, 0x18, 0x08, 0x10, 0x00, 0x00, 0x08 
    }; 
    GLubyte halftone[] = { 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55 
    }; 
 
    glClear (GL_COLOR_BUFFER_BIT); 
 
/*  draw all polygons in white*/ 
    glColor3f (1.0, 1.0, 1.0); 
 
/*  draw one solid, unstippled rectangle,*/ 
/*  then two stippled rectangles*/ 
    glRectf (25.0, 25.0, 125.0, 125.0); 
    glEnable (GL_POLYGON_STIPPLE); 
    glPolygonStipple (fly); 
    glRectf (125.0, 25.0, 225.0, 125.0); 
    glPolygonStipple (halftone); 
    glRectf (225.0, 25.0, 325.0, 125.0); 
    glDisable (GL_POLYGON_STIPPLE); 
 
    glFlush (); 
}
```



## <a name="porting-tessellated-polygons"></a><span data-ttu-id="0ad15-191">移植鑲嵌多邊形</span><span class="sxs-lookup"><span data-stu-id="0ad15-191">Porting Tessellated Polygons</span></span>

<span data-ttu-id="0ad15-192">在鳶尾花 GL 中，您會使用 **凹** (**TRUE**) 然後 **bgnpolygon** 來繪製凹形多邊形。</span><span class="sxs-lookup"><span data-stu-id="0ad15-192">In IRIS GL, you use **concave**(**TRUE**) and then **bgnpolygon** to draw concave polygons.</span></span> <span data-ttu-id="0ad15-193">OpenGL X.GLU 隊包含您可以用來繪製凹形多邊形的函式。</span><span class="sxs-lookup"><span data-stu-id="0ad15-193">The OpenGL GLU includes functions you can use to draw concave polygons.</span></span>

<span data-ttu-id="0ad15-194">**使用 OpenGL 繪製凹形多邊形**</span><span class="sxs-lookup"><span data-stu-id="0ad15-194">**To draw a concave polygon with OpenGL**</span></span>

1.  <span data-ttu-id="0ad15-195">建立鑲嵌式物件。</span><span class="sxs-lookup"><span data-stu-id="0ad15-195">Create a tessellation object.</span></span>
2.  <span data-ttu-id="0ad15-196">定義將用來處理鑲嵌所產生之三角形的回呼。</span><span class="sxs-lookup"><span data-stu-id="0ad15-196">Define callbacks that will be used to process the triangles generated by the tessellator.</span></span>
3.  <span data-ttu-id="0ad15-197">指定要鑲嵌的凹陷多邊形。</span><span class="sxs-lookup"><span data-stu-id="0ad15-197">Specify the concave polygon to be tessellated.</span></span>

<span data-ttu-id="0ad15-198">下表列出繪圖鑲嵌多邊形的 OpenGL 函數。</span><span class="sxs-lookup"><span data-stu-id="0ad15-198">The following table lists the OpenGL functions for drawing tessellated polygons.</span></span>



| <span data-ttu-id="0ad15-199">OpenGL X.GLU 隊函式</span><span class="sxs-lookup"><span data-stu-id="0ad15-199">OpenGL GLU function</span></span>                        | <span data-ttu-id="0ad15-200">意義</span><span class="sxs-lookup"><span data-stu-id="0ad15-200">Meaning</span></span>                                                            |
|--------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="0ad15-201">**gluNewTess**</span><span class="sxs-lookup"><span data-stu-id="0ad15-201">**gluNewTess**</span></span>](glunewtess.md)           | <span data-ttu-id="0ad15-202">建立新的鑲嵌式物件。</span><span class="sxs-lookup"><span data-stu-id="0ad15-202">Creates a new tessellation object.</span></span>                                 |
| [<span data-ttu-id="0ad15-203">**gluDeleteTess**</span><span class="sxs-lookup"><span data-stu-id="0ad15-203">**gluDeleteTess**</span></span>](gludeletetess.md)     | <span data-ttu-id="0ad15-204">刪除鑲嵌式物件。</span><span class="sxs-lookup"><span data-stu-id="0ad15-204">Deletes a tessellation object.</span></span>                                     |
| [<span data-ttu-id="0ad15-205">*gluTessCallback*</span><span class="sxs-lookup"><span data-stu-id="0ad15-205">*gluTessCallback*</span></span>](glutess.md)           |                                                                    |
| [<span data-ttu-id="0ad15-206">**gluBeginPolygon**</span><span class="sxs-lookup"><span data-stu-id="0ad15-206">**gluBeginPolygon**</span></span>](glubeginpolygon.md) | <span data-ttu-id="0ad15-207">開始多邊形規格。</span><span class="sxs-lookup"><span data-stu-id="0ad15-207">Begins the polygon specification.</span></span>                                  |
| [<span data-ttu-id="0ad15-208">**gluTessVertex**</span><span class="sxs-lookup"><span data-stu-id="0ad15-208">**gluTessVertex**</span></span>](glutessvertex.md)     | <span data-ttu-id="0ad15-209">指定輪廓中的多邊形頂點。</span><span class="sxs-lookup"><span data-stu-id="0ad15-209">Specifies a polygon vertex in a contour.</span></span>                           |
| [<span data-ttu-id="0ad15-210">**gluNextContour**</span><span class="sxs-lookup"><span data-stu-id="0ad15-210">**gluNextContour**</span></span>](glunextcontour.md)   | <span data-ttu-id="0ad15-211">表示下一系列頂點描述新的輪廓。</span><span class="sxs-lookup"><span data-stu-id="0ad15-211">Indicates that the next series of vertices describe a new contour.</span></span> |
| [<span data-ttu-id="0ad15-212">**gluEndPolygon**</span><span class="sxs-lookup"><span data-stu-id="0ad15-212">**gluEndPolygon**</span></span>](gluendpolygon.md)     | <span data-ttu-id="0ad15-213">結束多邊形規格。</span><span class="sxs-lookup"><span data-stu-id="0ad15-213">Ends the polygon specification.</span></span>                                    |



 

 

 





