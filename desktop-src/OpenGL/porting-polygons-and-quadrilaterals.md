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
ms.openlocfilehash: 7900b44051cab9590be11198c8b01af0b7c10244
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908456"
---
# <a name="porting-polygons-and-quadrilaterals"></a><span data-ttu-id="6bf62-115">移植多邊形和 Quadrilaterals</span><span class="sxs-lookup"><span data-stu-id="6bf62-115">Porting Polygons and Quadrilaterals</span></span>

<span data-ttu-id="6bf62-116">移植多邊形和 quadrilaterals 時，請記住下列幾點：</span><span class="sxs-lookup"><span data-stu-id="6bf62-116">Keep the following points in mind when porting polygons and quadrilaterals:</span></span>

-   <span data-ttu-id="6bf62-117">**凹** (**TRUE**) 沒有直接對等專案。</span><span class="sxs-lookup"><span data-stu-id="6bf62-117">There is no direct equivalent for **concave**(**TRUE**).</span></span> <span data-ttu-id="6bf62-118">相反地，您可以使用 X.GLU 隊中的鑲嵌式常式，如 [鑲嵌多邊形](tessellating-polygons.md)所述。</span><span class="sxs-lookup"><span data-stu-id="6bf62-118">Instead you can use the tessellation routines in the GLU, described in [Tessellating Polygons](tessellating-polygons.md).</span></span>
-   <span data-ttu-id="6bf62-119">多邊形模式的設定方式不同。</span><span class="sxs-lookup"><span data-stu-id="6bf62-119">Polygon modes are set differently.</span></span>
-   <span data-ttu-id="6bf62-120">這些多邊形繪圖函式在 OpenGL 中沒有直接對等專案： **poly** 系列的常式; **polf** 系列的常式; **pmv**、 **寮國** 和 **pclos**; **rpmv** 和 **rpdr**; **splf**;和 **spclos**。</span><span class="sxs-lookup"><span data-stu-id="6bf62-120">These polygon drawing functions have no direct equivalents in OpenGL: the **poly** family of routines; the **polf** family of routines; **pmv**, **pdr**, and **pclos**; **rpmv** and **rpdr**; **splf**; and **spclos**.</span></span>

<span data-ttu-id="6bf62-121">如果您的鳶尾花 GL 程式碼使用這些功能，您必須使用 [**glBegin**](glbegin.md) ( GL 多邊形 ) 來重寫程式碼 \_ 。</span><span class="sxs-lookup"><span data-stu-id="6bf62-121">If your IRIS GL code uses these functions, you'll have to rewrite the code using [**glBegin**](glbegin.md)( GL\_POLYGON ).</span></span>

<span data-ttu-id="6bf62-122">下表列出鳶尾花 GL 多邊形繪圖函式及其對等的 OpenGL 函數。</span><span class="sxs-lookup"><span data-stu-id="6bf62-122">The following table lists the IRIS GL polygon drawing functions and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="6bf62-123">鳶尾花 GL 函數</span><span class="sxs-lookup"><span data-stu-id="6bf62-123">IRIS GL function</span></span>         | <span data-ttu-id="6bf62-124">OpenGL 函數</span><span class="sxs-lookup"><span data-stu-id="6bf62-124">OpenGL function</span></span>                                                    | <span data-ttu-id="6bf62-125">意義</span><span class="sxs-lookup"><span data-stu-id="6bf62-125">Meaning</span></span>                                                 |
|--------------------------|--------------------------------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="6bf62-126">**bgnpolygonendpolygon**</span><span class="sxs-lookup"><span data-stu-id="6bf62-126">**bgnpolygonendpolygon**</span></span> | <span data-ttu-id="6bf62-127">[**glBegin**](glbegin.md) ( GL \_ 多邊形 ) [ **glEnd**](glend.md)</span><span class="sxs-lookup"><span data-stu-id="6bf62-127">[**glBegin**](glbegin.md) ( GL\_POLYGON )[**glEnd**](glend.md)</span></span>   | <span data-ttu-id="6bf62-128">頂點：定義簡單凸邊的界限。</span><span class="sxs-lookup"><span data-stu-id="6bf62-128">Vertices define boundary of a simple convex polygon.</span></span>    |
|                          | <span data-ttu-id="6bf62-129">**glBegin** ( GL \_ 四邊形 ) **glEnd**</span><span class="sxs-lookup"><span data-stu-id="6bf62-129">**glBegin**( GL\_QUADS )**glEnd**</span></span><br/>                       | <span data-ttu-id="6bf62-130">將頂點的時解讀為 quadrilaterals。</span><span class="sxs-lookup"><span data-stu-id="6bf62-130">Interprets quadruples of vertices as quadrilaterals.</span></span>    |
| <span data-ttu-id="6bf62-131">**bgnqstripendqstrip**</span><span class="sxs-lookup"><span data-stu-id="6bf62-131">**bgnqstripendqstrip**</span></span>   | <span data-ttu-id="6bf62-132">[**glBegin**](glbegin.md) ( GL \_ QUAD \_ ) **glEnd**</span><span class="sxs-lookup"><span data-stu-id="6bf62-132">[**glBegin**](glbegin.md) ( GL\_QUAD\_STRIP )**glEnd**</span></span><br/> | <span data-ttu-id="6bf62-133">將頂點解釋為 quadrilaterals 的連結塊。</span><span class="sxs-lookup"><span data-stu-id="6bf62-133">Interprets vertices as linked strips of quadrilaterals.</span></span> |
|                          | [<span data-ttu-id="6bf62-134">glEdgeFlag</span><span class="sxs-lookup"><span data-stu-id="6bf62-134">glEdgeFlag</span></span>](gledgeflag-functions.md)                             |                                                         |
| <span data-ttu-id="6bf62-135">**polymode**</span><span class="sxs-lookup"><span data-stu-id="6bf62-135">**polymode**</span></span>             | [<span data-ttu-id="6bf62-136">**glPolygonMode**</span><span class="sxs-lookup"><span data-stu-id="6bf62-136">**glPolygonMode**</span></span>](glpolygonmode.md)                             | <span data-ttu-id="6bf62-137">設定多邊形繪圖模式。</span><span class="sxs-lookup"><span data-stu-id="6bf62-137">Sets polygon drawing mode.</span></span>                              |
| <span data-ttu-id="6bf62-138">**rectrectf**</span><span class="sxs-lookup"><span data-stu-id="6bf62-138">**rectrectf**</span></span><br/> | [<span data-ttu-id="6bf62-139">glRect</span><span class="sxs-lookup"><span data-stu-id="6bf62-139">glRect</span></span>](glrect-functions.md)                                     | <span data-ttu-id="6bf62-140">繪製矩形。</span><span class="sxs-lookup"><span data-stu-id="6bf62-140">Draws a rectangle.</span></span>                                      |
| <span data-ttu-id="6bf62-141">**sboxsboxf**</span><span class="sxs-lookup"><span data-stu-id="6bf62-141">**sboxsboxf**</span></span><br/> |                                                                    | <span data-ttu-id="6bf62-142">繪製螢幕對齊的矩形。</span><span class="sxs-lookup"><span data-stu-id="6bf62-142">Draws a screen-aligned rectangle.</span></span>                       |



 

<span data-ttu-id="6bf62-143">??</span><span class="sxs-lookup"><span data-stu-id="6bf62-143">??</span></span>

## <a name="porting-polygon-modes"></a><span data-ttu-id="6bf62-144">移植多邊形模式</span><span class="sxs-lookup"><span data-stu-id="6bf62-144">Porting Polygon Modes</span></span>

<span data-ttu-id="6bf62-145">[OpenGL 函數 [**glPolygonMode**](glpolygonmode.md) ] 可讓您指定多邊形的哪一端 (要套用至哪一側的背景) 。</span><span class="sxs-lookup"><span data-stu-id="6bf62-145">The OpenGL function [**glPolygonMode**](glpolygonmode.md) lets you specify which side of a polygon (the back or the front) the mode applies to.</span></span> <span data-ttu-id="6bf62-146">其語法如下：</span><span class="sxs-lookup"><span data-stu-id="6bf62-146">Its syntax is:</span></span>

``` syntax
void glPolygonMode( GLenum face, GLenum mode ); 
 
```

<span data-ttu-id="6bf62-147">其中的臉部是下列其中一項：</span><span class="sxs-lookup"><span data-stu-id="6bf62-147">where face is one of:</span></span>



|<span data-ttu-id="6bf62-148">GLenum 值</span><span class="sxs-lookup"><span data-stu-id="6bf62-148">GLenum value</span></span>                      |  <span data-ttu-id="6bf62-149">意義</span><span class="sxs-lookup"><span data-stu-id="6bf62-149">Meaning</span></span>                                                          |
|----------------------|------------------------------------------------------------|
| <span data-ttu-id="6bf62-150">GL \_ FRONT</span><span class="sxs-lookup"><span data-stu-id="6bf62-150">GL\_FRONT</span></span>            | <span data-ttu-id="6bf62-151">適用于正面多邊形的模式</span><span class="sxs-lookup"><span data-stu-id="6bf62-151">mode which applies to front-facing polygons</span></span>                |
| <span data-ttu-id="6bf62-152">GL \_ 回</span><span class="sxs-lookup"><span data-stu-id="6bf62-152">GL\_BACK</span></span>             | <span data-ttu-id="6bf62-153">適用于後置多邊形的模式</span><span class="sxs-lookup"><span data-stu-id="6bf62-153">mode which applies to back-facing polygons</span></span>                 |
| <span data-ttu-id="6bf62-154">GL \_ 正面 \_ 和 \_ 背面</span><span class="sxs-lookup"><span data-stu-id="6bf62-154">GL\_FRONT\_AND\_BACK</span></span> | <span data-ttu-id="6bf62-155">適用于 front 和 back 多邊形的模式</span><span class="sxs-lookup"><span data-stu-id="6bf62-155">mode which applies to both front- and back-facing polygons</span></span> |



 

<span data-ttu-id="6bf62-156">GL \_ 前端 \_ 和 \_ 後端模式相當於鳶尾花 GL **polymode** 函數。</span><span class="sxs-lookup"><span data-stu-id="6bf62-156">The GL\_FRONT\_AND\_BACK mode is equivalent to the IRIS GL **polymode** function.</span></span> <span data-ttu-id="6bf62-157">下表列出鳶尾花 GL 多邊形模式及其對等的 OpenGL 模式。</span><span class="sxs-lookup"><span data-stu-id="6bf62-157">The following table lists IRIS GL polygon modes and their equivalent OpenGL modes.</span></span>



| <span data-ttu-id="6bf62-158">鳶尾花 GL 模式</span><span class="sxs-lookup"><span data-stu-id="6bf62-158">IRIS GL mode</span></span> | <span data-ttu-id="6bf62-159">OpenGL 模式</span><span class="sxs-lookup"><span data-stu-id="6bf62-159">OpenGL mode</span></span> | <span data-ttu-id="6bf62-160">意義</span><span class="sxs-lookup"><span data-stu-id="6bf62-160">Meaning</span></span>                                       |
|--------------|-------------|-----------------------------------------------|
| <span data-ttu-id="6bf62-161">PYM \_ 點</span><span class="sxs-lookup"><span data-stu-id="6bf62-161">PYM\_POINT</span></span>   | <span data-ttu-id="6bf62-162">GL \_ 點</span><span class="sxs-lookup"><span data-stu-id="6bf62-162">GL\_POINT</span></span>   | <span data-ttu-id="6bf62-163">將頂點繪製成點。</span><span class="sxs-lookup"><span data-stu-id="6bf62-163">Draws vertices as points.</span></span>                     |
| <span data-ttu-id="6bf62-164">PYM \_ 行</span><span class="sxs-lookup"><span data-stu-id="6bf62-164">PYM\_LINE</span></span>    | <span data-ttu-id="6bf62-165">GL \_ 線</span><span class="sxs-lookup"><span data-stu-id="6bf62-165">GL\_LINE</span></span>    | <span data-ttu-id="6bf62-166">將邊界邊緣繪製為線段。</span><span class="sxs-lookup"><span data-stu-id="6bf62-166">Draws boundary edges as line segments.</span></span>        |
| <span data-ttu-id="6bf62-167">PYM \_ 填滿</span><span class="sxs-lookup"><span data-stu-id="6bf62-167">PYM\_FILL</span></span>    | <span data-ttu-id="6bf62-168">GL \_ 填滿</span><span class="sxs-lookup"><span data-stu-id="6bf62-168">GL\_FILL</span></span>    | <span data-ttu-id="6bf62-169">繪製填滿的多邊形內部。</span><span class="sxs-lookup"><span data-stu-id="6bf62-169">Draws polygon interior filled.</span></span>                |
| <span data-ttu-id="6bf62-170">PYM \_ 空心</span><span class="sxs-lookup"><span data-stu-id="6bf62-170">PYM\_HOLLOW</span></span>  |             | <span data-ttu-id="6bf62-171">只填滿界限的內部圖元。</span><span class="sxs-lookup"><span data-stu-id="6bf62-171">Fills only interior pixels at the boundaries.</span></span> |



 

## <a name="porting-polygon-stipples"></a><span data-ttu-id="6bf62-172">移植多邊形 Stipples</span><span class="sxs-lookup"><span data-stu-id="6bf62-172">Porting Polygon Stipples</span></span>

<span data-ttu-id="6bf62-173">移植鳶尾花 GL 多邊形 stipples 時，請記住下列幾點：</span><span class="sxs-lookup"><span data-stu-id="6bf62-173">When porting IRIS GL polygon stipples, keep the following points in mind:</span></span>

-   <span data-ttu-id="6bf62-174">OpenGL 不會使用資料表進行多邊形 stipples;只保留一個 stipple 模式。</span><span class="sxs-lookup"><span data-stu-id="6bf62-174">OpenGL doesn't use tables for polygon stipples; only one stipple pattern is kept.</span></span> <span data-ttu-id="6bf62-175">您可以使用顯示清單來儲存不同的 stipple 模式。</span><span class="sxs-lookup"><span data-stu-id="6bf62-175">You can use display lists to store different stipple patterns.</span></span>
-   <span data-ttu-id="6bf62-176">OpenGL 多邊形 stipple 點陣圖大小一律為32x32 位模式。</span><span class="sxs-lookup"><span data-stu-id="6bf62-176">The OpenGL polygon stipple bitmap size is always a 32x32 bit pattern.</span></span>
-   <span data-ttu-id="6bf62-177">Stipple 編碼會受到 [**glPixelStore**](glpixelstore-functions.md)的影響。</span><span class="sxs-lookup"><span data-stu-id="6bf62-177">Stipple encoding is affected by [**glPixelStore**](glpixelstore-functions.md).</span></span>

<span data-ttu-id="6bf62-178">如需移植多邊形 stipples 的詳細資訊，請參閱 [移植圖元作業](porting-pixel-operations.md)。</span><span class="sxs-lookup"><span data-stu-id="6bf62-178">For more information on porting polygon stipples, see [Porting Pixel Operations](porting-pixel-operations.md).</span></span>

<span data-ttu-id="6bf62-179">下表列出鳶尾花 GL 多邊形 stipple 函數及其對等的 OpenGL 函數。</span><span class="sxs-lookup"><span data-stu-id="6bf62-179">The following table lists IRIS GL polygon stipple functions and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="6bf62-180">鳶尾花 GL 函數</span><span class="sxs-lookup"><span data-stu-id="6bf62-180">IRIS GL function</span></span> | <span data-ttu-id="6bf62-181">OpenGL 函數</span><span class="sxs-lookup"><span data-stu-id="6bf62-181">OpenGL function</span></span>                                    | <span data-ttu-id="6bf62-182">意義</span><span class="sxs-lookup"><span data-stu-id="6bf62-182">Meaning</span></span>                                               |
|------------------|----------------------------------------------------|-------------------------------------------------------|
| <span data-ttu-id="6bf62-183">**defpattern**</span><span class="sxs-lookup"><span data-stu-id="6bf62-183">**defpattern**</span></span>   | [<span data-ttu-id="6bf62-184">**glPolygonStipple**</span><span class="sxs-lookup"><span data-stu-id="6bf62-184">**glPolygonStipple**</span></span>](glpolygonstipple.md)       | <span data-ttu-id="6bf62-185">設定 stipple 模式。</span><span class="sxs-lookup"><span data-stu-id="6bf62-185">Sets the stipple pattern.</span></span>                             |
| <span data-ttu-id="6bf62-186">**setpattern**</span><span class="sxs-lookup"><span data-stu-id="6bf62-186">**setpattern**</span></span>   |                                                    | <span data-ttu-id="6bf62-187">OpenGL 只保留一個多邊形 stipple 模式。</span><span class="sxs-lookup"><span data-stu-id="6bf62-187">OpenGL keeps only one polygon stipple pattern.</span></span>        |
| <span data-ttu-id="6bf62-188">**system.windows.automation.peers.uielementautomationpeer.getpattern**</span><span class="sxs-lookup"><span data-stu-id="6bf62-188">**getpattern**</span></span>   | [<span data-ttu-id="6bf62-189">**glGetPolygonStipple**</span><span class="sxs-lookup"><span data-stu-id="6bf62-189">**glGetPolygonStipple**</span></span>](glgetpolygonstipple.md) | <span data-ttu-id="6bf62-190">傳回 stipple 點陣圖 (用來傳回索引) 。</span><span class="sxs-lookup"><span data-stu-id="6bf62-190">Returns the stipple bitmap (used to return an index).</span></span> |



 

<span data-ttu-id="6bf62-191">在 OpenGL 中，您可以藉由 \_ 將 GL 多邊形 STIPPLE 傳遞 \_ 為 [**glEnable**](glenable.md) 和 [**glDisable**](gldisable.md)的參數，來啟用和停用多邊形 stippling。</span><span class="sxs-lookup"><span data-stu-id="6bf62-191">In OpenGL, you enable and disable polygon stippling by passing GL\_POLYGON\_STIPPLE as a parameter for [**glEnable**](glenable.md) and [**glDisable**](gldisable.md).</span></span>

<span data-ttu-id="6bf62-192">下列 OpenGL 程式碼範例示範多邊形 stippling：</span><span class="sxs-lookup"><span data-stu-id="6bf62-192">The following OpenGL code sample demonstrates polygon stippling:</span></span>


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



## <a name="porting-tessellated-polygons"></a><span data-ttu-id="6bf62-193">移植鑲嵌多邊形</span><span class="sxs-lookup"><span data-stu-id="6bf62-193">Porting Tessellated Polygons</span></span>

<span data-ttu-id="6bf62-194">在鳶尾花 GL 中，您會使用 **凹** (**TRUE**) 然後 **bgnpolygon** 來繪製凹形多邊形。</span><span class="sxs-lookup"><span data-stu-id="6bf62-194">In IRIS GL, you use **concave**(**TRUE**) and then **bgnpolygon** to draw concave polygons.</span></span> <span data-ttu-id="6bf62-195">OpenGL X.GLU 隊包含您可以用來繪製凹形多邊形的函式。</span><span class="sxs-lookup"><span data-stu-id="6bf62-195">The OpenGL GLU includes functions you can use to draw concave polygons.</span></span>

<span data-ttu-id="6bf62-196">**使用 OpenGL 繪製凹形多邊形**</span><span class="sxs-lookup"><span data-stu-id="6bf62-196">**To draw a concave polygon with OpenGL**</span></span>

1.  <span data-ttu-id="6bf62-197">建立鑲嵌式物件。</span><span class="sxs-lookup"><span data-stu-id="6bf62-197">Create a tessellation object.</span></span>
2.  <span data-ttu-id="6bf62-198">定義將用來處理鑲嵌所產生之三角形的回呼。</span><span class="sxs-lookup"><span data-stu-id="6bf62-198">Define callbacks that will be used to process the triangles generated by the tessellator.</span></span>
3.  <span data-ttu-id="6bf62-199">指定要鑲嵌的凹陷多邊形。</span><span class="sxs-lookup"><span data-stu-id="6bf62-199">Specify the concave polygon to be tessellated.</span></span>

<span data-ttu-id="6bf62-200">下表列出繪圖鑲嵌多邊形的 OpenGL 函數。</span><span class="sxs-lookup"><span data-stu-id="6bf62-200">The following table lists the OpenGL functions for drawing tessellated polygons.</span></span>



| <span data-ttu-id="6bf62-201">OpenGL X.GLU 隊函式</span><span class="sxs-lookup"><span data-stu-id="6bf62-201">OpenGL GLU function</span></span>                        | <span data-ttu-id="6bf62-202">意義</span><span class="sxs-lookup"><span data-stu-id="6bf62-202">Meaning</span></span>                                                            |
|--------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="6bf62-203">**gluNewTess**</span><span class="sxs-lookup"><span data-stu-id="6bf62-203">**gluNewTess**</span></span>](glunewtess.md)           | <span data-ttu-id="6bf62-204">建立新的鑲嵌式物件。</span><span class="sxs-lookup"><span data-stu-id="6bf62-204">Creates a new tessellation object.</span></span>                                 |
| [<span data-ttu-id="6bf62-205">**gluDeleteTess**</span><span class="sxs-lookup"><span data-stu-id="6bf62-205">**gluDeleteTess**</span></span>](gludeletetess.md)     | <span data-ttu-id="6bf62-206">刪除鑲嵌式物件。</span><span class="sxs-lookup"><span data-stu-id="6bf62-206">Deletes a tessellation object.</span></span>                                     |
| [<span data-ttu-id="6bf62-207">*gluTessCallback*</span><span class="sxs-lookup"><span data-stu-id="6bf62-207">*gluTessCallback*</span></span>](glutess.md)           |                                                                    |
| [<span data-ttu-id="6bf62-208">**gluBeginPolygon**</span><span class="sxs-lookup"><span data-stu-id="6bf62-208">**gluBeginPolygon**</span></span>](glubeginpolygon.md) | <span data-ttu-id="6bf62-209">開始多邊形規格。</span><span class="sxs-lookup"><span data-stu-id="6bf62-209">Begins the polygon specification.</span></span>                                  |
| [<span data-ttu-id="6bf62-210">**gluTessVertex**</span><span class="sxs-lookup"><span data-stu-id="6bf62-210">**gluTessVertex**</span></span>](glutessvertex.md)     | <span data-ttu-id="6bf62-211">指定輪廓中的多邊形頂點。</span><span class="sxs-lookup"><span data-stu-id="6bf62-211">Specifies a polygon vertex in a contour.</span></span>                           |
| [<span data-ttu-id="6bf62-212">**gluNextContour**</span><span class="sxs-lookup"><span data-stu-id="6bf62-212">**gluNextContour**</span></span>](glunextcontour.md)   | <span data-ttu-id="6bf62-213">表示下一系列頂點描述新的輪廓。</span><span class="sxs-lookup"><span data-stu-id="6bf62-213">Indicates that the next series of vertices describe a new contour.</span></span> |
| [<span data-ttu-id="6bf62-214">**gluEndPolygon**</span><span class="sxs-lookup"><span data-stu-id="6bf62-214">**gluEndPolygon**</span></span>](gluendpolygon.md)     | <span data-ttu-id="6bf62-215">結束多邊形規格。</span><span class="sxs-lookup"><span data-stu-id="6bf62-215">Ends the polygon specification.</span></span>                                    |



 

 

 





