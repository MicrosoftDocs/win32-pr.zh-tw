---
title: 'glReadPixels 函式 (Gl) '
description: GlReadPixels 函式會從畫面格緩衝區讀取圖元區塊。
ms.assetid: 41fbad5c-b8ca-456d-bbfc-b48c176e15b0
keywords:
- glReadPixels 函式 OpenGL
topic_type:
- apiref
api_name:
- glReadPixels
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a853d67be282227168da4b90f4fdd47a49d2d212
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104383913"
---
# <a name="glreadpixels-function"></a><span data-ttu-id="d444f-104">glReadPixels 函式</span><span class="sxs-lookup"><span data-stu-id="d444f-104">glReadPixels function</span></span>

<span data-ttu-id="d444f-105">**GlReadPixels** 函式會從畫面格緩衝區讀取圖元區塊。</span><span class="sxs-lookup"><span data-stu-id="d444f-105">The **glReadPixels** function reads a block of pixels from the framebuffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="d444f-106">語法</span><span class="sxs-lookup"><span data-stu-id="d444f-106">Syntax</span></span>


```C++
void WINAPI glReadPixels(
   GLint   x,
   GLint   y,
   GLsizei width,
   GLsizei height,
   GLenum  format,
   GLenum  type,
   GLvoid  *pixels
);
```



## <a name="parameters"></a><span data-ttu-id="d444f-107">參數</span><span class="sxs-lookup"><span data-stu-id="d444f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d444f-108">*x*</span><span class="sxs-lookup"><span data-stu-id="d444f-108">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="d444f-109">從畫面格緩衝區讀取之第一個圖元的視窗 *x* 座標。</span><span class="sxs-lookup"><span data-stu-id="d444f-109">The window *x* coordinate of the first pixel that is read from the framebuffer.</span></span> <span data-ttu-id="d444f-110">使用 *y* 座標，指定圖元矩形區塊的左下角位置。</span><span class="sxs-lookup"><span data-stu-id="d444f-110">Together with the *y* coordinate, specifies the location of the lower-left corner of a rectangular block of pixels.</span></span>

</dd> <dt>

<span data-ttu-id="d444f-111">*y*</span><span class="sxs-lookup"><span data-stu-id="d444f-111">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="d444f-112">從畫面格緩衝區讀取之第一個圖元的視窗 *y* 座標。</span><span class="sxs-lookup"><span data-stu-id="d444f-112">The window *y* coordinates of the first pixel that is read from the framebuffer.</span></span> <span data-ttu-id="d444f-113">搭配 *x* 座標，指定圖元矩形區塊的左下角位置。</span><span class="sxs-lookup"><span data-stu-id="d444f-113">Together with the *x* coordinate, specifies the location of the lower-left corner of a rectangular block of pixels.</span></span>

</dd> <dt>

<span data-ttu-id="d444f-114">*width* (寬度)</span><span class="sxs-lookup"><span data-stu-id="d444f-114">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="d444f-115">圖元矩形的寬度。</span><span class="sxs-lookup"><span data-stu-id="d444f-115">The width of the pixel rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="d444f-116">*height* (高度)</span><span class="sxs-lookup"><span data-stu-id="d444f-116">*height*</span></span> 
</dt> <dd>

<span data-ttu-id="d444f-117">圖元矩形的高度。</span><span class="sxs-lookup"><span data-stu-id="d444f-117">The height of the pixel rectangle.</span></span> <span data-ttu-id="d444f-118">值為 "1" 的 *寬度* 和 *高度* 參數對應到單一圖元。</span><span class="sxs-lookup"><span data-stu-id="d444f-118">*Width* and *height* parameters of value "1" correspond to a single pixel.</span></span>

</dd> <dt>

<span data-ttu-id="d444f-119">*format*</span><span class="sxs-lookup"><span data-stu-id="d444f-119">*format*</span></span> 
</dt> <dd>

<span data-ttu-id="d444f-120">圖元資料的格式。</span><span class="sxs-lookup"><span data-stu-id="d444f-120">The format of the pixel data.</span></span> <span data-ttu-id="d444f-121">接受下列符號值：</span><span class="sxs-lookup"><span data-stu-id="d444f-121">The following symbolic values are accepted:</span></span>



| <span data-ttu-id="d444f-122">值</span><span class="sxs-lookup"><span data-stu-id="d444f-122">Value</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                           | <span data-ttu-id="d444f-123">意義</span><span class="sxs-lookup"><span data-stu-id="d444f-123">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_COLOR_INDEX"></span><span id="gl_color_index"></span><dl> <span data-ttu-id="d444f-124"><dt>**GL \_ 色彩 \_ 索引**</dt></span><span class="sxs-lookup"><span data-stu-id="d444f-124"><dt>**GL\_COLOR\_INDEX**</dt></span></span> </dl>                                                                                                                                                                                                                                                                                                               | <span data-ttu-id="d444f-125">色彩索引是從 [**glReadBuffer**](glreadbuffer.md)選取的色彩緩衝區中讀取。</span><span class="sxs-lookup"><span data-stu-id="d444f-125">Color indexes are read from the color buffer selected by [**glReadBuffer**](glreadbuffer.md).</span></span> <span data-ttu-id="d444f-126">每個索引都會轉換成固定點、向左或向右移動，取決於 GL 索引移位的值和正負號 \_ \_ ，並新增至 gl \_ 索引 \_ 位移。</span><span class="sxs-lookup"><span data-stu-id="d444f-126">Each index is converted to fixed point, shifted left or right, depending on the value and sign of GL\_INDEX\_SHIFT, and added to GL\_INDEX\_OFFSET.</span></span> <span data-ttu-id="d444f-127">如果 GL \_ 地圖 \_ 色彩為 gl \_ TRUE，則會將索引取代為數據表 GL \_ 圖元 \_ 地圖 \_ i \_ 到 \_ i 中的對應。</span><span class="sxs-lookup"><span data-stu-id="d444f-127">If GL\_MAP\_COLOR is GL\_TRUE, indexes are replaced by their mappings in the table GL\_PIXEL\_MAP\_I\_TO\_I.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="GL_STENCIL_INDEX"></span><span id="gl_stencil_index"></span><dl> <span data-ttu-id="d444f-128"><dt>**GL \_ 樣板 \_ 索引**</dt></span><span class="sxs-lookup"><span data-stu-id="d444f-128"><dt>**GL\_STENCIL\_INDEX**</dt></span></span> </dl>                                                                                                                                                                                                                                                                                                         | <span data-ttu-id="d444f-129">樣板值會從樣板緩衝區中讀取。</span><span class="sxs-lookup"><span data-stu-id="d444f-129">Stencil values are read from the stencil buffer.</span></span> <span data-ttu-id="d444f-130">每個索引都會轉換成固定點、向左或向右移動，取決於 GL 索引移位的值和正負號 \_ \_ ，並新增至 gl \_ 索引 \_ 位移。</span><span class="sxs-lookup"><span data-stu-id="d444f-130">Each index is converted to fixed point, shifted left or right, depending on the value and sign of GL\_INDEX\_SHIFT, and added to GL\_INDEX\_OFFSET.</span></span> <span data-ttu-id="d444f-131">如果 GL \_ 地圖樣板 \_ 為 gl \_ ，則會將索引取代為數據表 GL \_ 圖元 \_ 地圖 \_ s \_ 到 \_ s 中的對應。</span><span class="sxs-lookup"><span data-stu-id="d444f-131">If GL\_MAP\_STENCIL is GL\_TRUE, indexes are replaced by their mappings in the table GL\_PIXEL\_MAP\_S\_TO\_S.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="GL_DEPTH_COMPONENT"></span><span id="gl_depth_component"></span><dl> <span data-ttu-id="d444f-132"><dt>**GL \_ 深度 \_ 元件**</dt></span><span class="sxs-lookup"><span data-stu-id="d444f-132"><dt>**GL\_DEPTH\_COMPONENT**</dt></span></span> </dl>                                                                                                                                                                                                                                                                                                   | <span data-ttu-id="d444f-133">深度值是從深度緩衝區讀取的。</span><span class="sxs-lookup"><span data-stu-id="d444f-133">Depth values are read from the depth buffer.</span></span> <span data-ttu-id="d444f-134">每個元件都會轉換成浮點數，因此最小深度值會對應至0.0，而最大值會對應至1.0。</span><span class="sxs-lookup"><span data-stu-id="d444f-134">Each component is converted to floating point such that the minimum depth value maps to 0.0 and the maximum value maps to 1.0.</span></span> <span data-ttu-id="d444f-135">然後，每個元件會乘以 GL \_ 深度 \_ 比例、新增至 GL \_ 深度 \_ 偏差，最後壓制至範圍 \[ 0，1 \] 。</span><span class="sxs-lookup"><span data-stu-id="d444f-135">Each component is then multiplied by GL\_DEPTH\_SCALE, added to GL\_DEPTH\_BIAS, and finally clamped to the range \[0,1\].</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="GL_RED__GL_GREEN__GL_BLUE__GL_ALPHA__GL_RGB__GL_RGBA__GL_BGR_EXT__GL_BGRA_EXT__GL_LUMINANCE__GL_LUMINANCE_ALPHA"></span><span id="gl_red__gl_green__gl_blue__gl_alpha__gl_rgb__gl_rgba__gl_bgr_ext__gl_bgra_ext__gl_luminance__gl_luminance_alpha"></span><dl> <span data-ttu-id="d444f-136"><dt>**GL \_ RED、GL \_ 綠、GL \_ BLUE、GL \_ ALPHA、GL \_ RGB、GL \_ RGBA、GL \_ BGR \_ EXT、GL \_ BGRA \_ EXT、GL \_ 亮度、GL \_ 亮度 \_ ALPHA**</dt></span><span class="sxs-lookup"><span data-stu-id="d444f-136"><dt>**GL\_RED, GL\_GREEN, GL\_BLUE, GL\_ALPHA, GL\_RGB, GL\_RGBA, GL\_BGR\_EXT, GL\_BGRA\_EXT, GL\_LUMINANCE, GL\_LUMINANCE\_ALPHA**</dt></span></span> </dl> | <span data-ttu-id="d444f-137">處理會因色彩緩衝區儲存色彩索引或 RGBA 色彩元件而有所不同。</span><span class="sxs-lookup"><span data-stu-id="d444f-137">Processing differs depending on whether color buffers store color indexes or RGBA color components.</span></span> <span data-ttu-id="d444f-138">如果已儲存色彩索引，則會從 [**glReadBuffer**](glreadbuffer.md)所選取的色彩緩衝區讀取這些索引。</span><span class="sxs-lookup"><span data-stu-id="d444f-138">If color indexes are stored, they are read from the color buffer selected by [**glReadBuffer**](glreadbuffer.md).</span></span> <span data-ttu-id="d444f-139">每個索引都會轉換成固定點、向左或向右移動，取決於 GL 索引移位的值和正負號 \_ \_ ，並新增至 gl \_ 索引 \_ 位移。</span><span class="sxs-lookup"><span data-stu-id="d444f-139">Each index is converted to fixed point, shifted left or right, depending on the value and sign of GL\_INDEX\_SHIFT, and added to GL\_INDEX\_OFFSET.</span></span> <span data-ttu-id="d444f-140">然後，索引會由將 GL \_ 圖元 \_ 地圖 \_ i \_ 到 \_ R、gl \_ 圖元 \_ 地圖 \_ i \_ 到 \_ G、gl \_ 圖元 \_ 地圖 i \_ \_ 到 \_ B，以及 gl \_ 圖元 \_ 對應 \_ i \_ 到 \_ 資料表的紅色、綠色、藍色和 Alpha 值取代。</span><span class="sxs-lookup"><span data-stu-id="d444f-140">Indexes are then replaced by the red, green, blue, and alpha values obtained by indexing the GL\_PIXEL\_MAP\_I\_TO\_R, GL\_PIXEL\_MAP\_I\_TO\_G, GL\_PIXEL\_MAP\_I\_TO\_B, and GL\_PIXEL\_MAP\_I\_TO\_A tables.</span></span> <span data-ttu-id="d444f-141">如果 RGBA 色彩元件儲存在色彩緩衝區中，則會從 **glReadBuffer** 所選取的色彩緩衝區讀取它們。</span><span class="sxs-lookup"><span data-stu-id="d444f-141">If RGBA color components are stored in the color buffers, they are read from the color buffer selected by **glReadBuffer**.</span></span> <span data-ttu-id="d444f-142">每個色彩元件都會轉換成浮點數，如此一來，就會將零濃度對應到0.0，並將完整強度對應到1.0。</span><span class="sxs-lookup"><span data-stu-id="d444f-142">Each color component is converted to floating point such that zero intensity maps to 0.0 and full intensity maps to 1.0.</span></span> <span data-ttu-id="d444f-143">接著，每個元件會乘以 GL \_ c \_ 規模並新增至 gl \_ c \_ 偏差，其中 c 是 gl \_ RED、gl 綠、 \_ gl \_ BLUE 和 gl \_ ALPHA。</span><span class="sxs-lookup"><span data-stu-id="d444f-143">Each component is then multiplied by GL\_c\_SCALE and added to GL\_c\_BIAS, where c is GL\_RED, GL\_GREEN, GL\_BLUE, and GL\_ALPHA.</span></span> <span data-ttu-id="d444f-144">每個元件都會壓制至範圍 \[ 0、1 \] 。</span><span class="sxs-lookup"><span data-stu-id="d444f-144">Each component is clamped to the range \[0,1\].</span></span> <span data-ttu-id="d444f-145">最後，如果 GL \_ 對應 \_ 色彩為 gl \_ TRUE，則每個色彩元件 c 都會取代為數據表 GL \_ 圖元 \_ 地圖 \_ c 到 c 中的對應 \_ \_ ，其中 c 再次為 gl \_ RED、gl \_ 綠、gl \_ 藍色和 gl \_ ALPHA。</span><span class="sxs-lookup"><span data-stu-id="d444f-145">Finally, if GL\_MAP\_COLOR is GL\_TRUE, each color component c is replaced by its mapping in the table GL\_PIXEL\_MAP\_c\_TO\_c, where c again is GL\_RED, GL\_GREEN, GL\_BLUE, and GL\_ALPHA.</span></span> <span data-ttu-id="d444f-146">在執行查閱之前，每個元件都會調整為其對應資料表的大小。</span><span class="sxs-lookup"><span data-stu-id="d444f-146">Each component is scaled to the size of its corresponding table before the lookup is performed.</span></span> <span data-ttu-id="d444f-147">最後，會捨棄不必要的資料。</span><span class="sxs-lookup"><span data-stu-id="d444f-147">Finally, unneeded data is discarded.</span></span> <span data-ttu-id="d444f-148">例如，GL \_ RED 會捨棄綠色、藍色和 Alpha 元件，而 gl RGB 則 \_ 只捨棄 Alpha 元件。</span><span class="sxs-lookup"><span data-stu-id="d444f-148">For example, GL\_RED discards the green, blue, and alpha components, while GL\_RGB discards only the alpha component.</span></span> <span data-ttu-id="d444f-149">GL \_ 亮度會將單一元件值計算為紅色、綠色和藍色元件的總和，而 gl \_ 亮度 \_ ALPHA 會執行相同的工作，同時將 ALPHA 保持為第二個值。</span><span class="sxs-lookup"><span data-stu-id="d444f-149">GL\_LUMINANCE computes a single component value as the sum of the red, green, and blue components, and GL\_LUMINANCE\_ALPHA does the same, while keeping alpha as a second value.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="d444f-150">*type*</span><span class="sxs-lookup"><span data-stu-id="d444f-150">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="d444f-151">圖元資料的資料類型。</span><span class="sxs-lookup"><span data-stu-id="d444f-151">The data type of the pixel data.</span></span> <span data-ttu-id="d444f-152">必須是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="d444f-152">Must be one of the following values.</span></span>



| <span data-ttu-id="d444f-153">類型</span><span class="sxs-lookup"><span data-stu-id="d444f-153">Type</span></span>                | <span data-ttu-id="d444f-154">索引遮罩</span><span class="sxs-lookup"><span data-stu-id="d444f-154">Index mask</span></span> | <span data-ttu-id="d444f-155">元件轉換</span><span class="sxs-lookup"><span data-stu-id="d444f-155">Component conversion</span></span> |
|---------------------|------------|----------------------|
| <span data-ttu-id="d444f-156">GL 不 \_ 帶正負號的 \_ 位元組</span><span class="sxs-lookup"><span data-stu-id="d444f-156">GL\_UNSIGNED\_BYTE</span></span>  | <span data-ttu-id="d444f-157">281</span><span class="sxs-lookup"><span data-stu-id="d444f-157">281</span></span>        | <span data-ttu-id="d444f-158"> (281) *c*</span><span class="sxs-lookup"><span data-stu-id="d444f-158">(281)*c*</span></span>             |
| <span data-ttu-id="d444f-159">GL \_ 位元組</span><span class="sxs-lookup"><span data-stu-id="d444f-159">GL\_BYTE</span></span>            | <span data-ttu-id="d444f-160">271</span><span class="sxs-lookup"><span data-stu-id="d444f-160">271</span></span>        | <span data-ttu-id="d444f-161">\[ (271) *c*-1 \] /2</span><span class="sxs-lookup"><span data-stu-id="d444f-161">\[(271)*c*-1\]/2</span></span>     |
| <span data-ttu-id="d444f-162">GL \_ 點陣圖</span><span class="sxs-lookup"><span data-stu-id="d444f-162">GL\_BITMAP</span></span>          | <span data-ttu-id="d444f-163">1</span><span class="sxs-lookup"><span data-stu-id="d444f-163">1</span></span>          | <span data-ttu-id="d444f-164">1</span><span class="sxs-lookup"><span data-stu-id="d444f-164">1</span></span>                    |
| <span data-ttu-id="d444f-165">GL 不 \_ 帶正負號 \_ 簡短</span><span class="sxs-lookup"><span data-stu-id="d444f-165">GL\_UNSIGNED\_SHORT</span></span> | <span data-ttu-id="d444f-166">2 61</span><span class="sxs-lookup"><span data-stu-id="d444f-166">2 61</span></span>       | <span data-ttu-id="d444f-167"> (2 61) *c*</span><span class="sxs-lookup"><span data-stu-id="d444f-167">(2 61)*c*</span></span>            |
| <span data-ttu-id="d444f-168">GL \_ 短期</span><span class="sxs-lookup"><span data-stu-id="d444f-168">GL\_SHORT</span></span>           | <span data-ttu-id="d444f-169">2 51</span><span class="sxs-lookup"><span data-stu-id="d444f-169">2 51</span></span>       | <span data-ttu-id="d444f-170">\[ (2 51) *c* 1 \] /2</span><span class="sxs-lookup"><span data-stu-id="d444f-170">\[(2 51)*c* 1\]/2</span></span>     |
| <span data-ttu-id="d444f-171">GL 不 \_ 帶正負號 \_ INT\_</span><span class="sxs-lookup"><span data-stu-id="d444f-171">GL\_UNSIGNED\_INT\_</span></span> | <span data-ttu-id="d444f-172">2 1</span><span class="sxs-lookup"><span data-stu-id="d444f-172">2  1</span></span>       | <span data-ttu-id="d444f-173"> (2 1) *c*</span><span class="sxs-lookup"><span data-stu-id="d444f-173">(2  1)*c*</span></span>            |
| <span data-ttu-id="d444f-174">GL \_ INT</span><span class="sxs-lookup"><span data-stu-id="d444f-174">GL\_INT</span></span>             | <span data-ttu-id="d444f-175">2 1</span><span class="sxs-lookup"><span data-stu-id="d444f-175">2   1</span></span>      | <span data-ttu-id="d444f-176">\[ (2 1) *c* 1 \] /2</span><span class="sxs-lookup"><span data-stu-id="d444f-176">\[(2  1)*c* 1\]/2</span></span>     |
| <span data-ttu-id="d444f-177">GL \_ FLOAT</span><span class="sxs-lookup"><span data-stu-id="d444f-177">GL\_FLOAT</span></span>           | <span data-ttu-id="d444f-178">無</span><span class="sxs-lookup"><span data-stu-id="d444f-178">none</span></span>       | <span data-ttu-id="d444f-179">*c*</span><span class="sxs-lookup"><span data-stu-id="d444f-179">*c*</span></span>                  |



 

</dd> <dt>

<span data-ttu-id="d444f-180">*圖元*</span><span class="sxs-lookup"><span data-stu-id="d444f-180">*pixels*</span></span> 
</dt> <dd>

<span data-ttu-id="d444f-181">傳回圖元資料。</span><span class="sxs-lookup"><span data-stu-id="d444f-181">Returns the pixel data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d444f-182">傳回值</span><span class="sxs-lookup"><span data-stu-id="d444f-182">Return value</span></span>

<span data-ttu-id="d444f-183">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="d444f-183">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="d444f-184">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="d444f-184">Error codes</span></span>

<span data-ttu-id="d444f-185">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="d444f-185">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="d444f-186">Name</span><span class="sxs-lookup"><span data-stu-id="d444f-186">Name</span></span>                                                                                                  | <span data-ttu-id="d444f-187">意義</span><span class="sxs-lookup"><span data-stu-id="d444f-187">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d444f-188"><dt>**GL \_ 無效 \_ 列舉**</dt></span><span class="sxs-lookup"><span data-stu-id="d444f-188"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="d444f-189">*格式* 或 *類型* 不是可接受的值。</span><span class="sxs-lookup"><span data-stu-id="d444f-189">*format* or *type* was not an accepted value.</span></span><br/>                                                                              |
| <dl> <span data-ttu-id="d444f-190"><dt>**GL \_ 無效 \_ 值**</dt></span><span class="sxs-lookup"><span data-stu-id="d444f-190"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="d444f-191">*寬度* 或 *高度* 都是負數。</span><span class="sxs-lookup"><span data-stu-id="d444f-191">Either *width* or *height* was negative.</span></span><br/>                                                                                   |
| <dl> <span data-ttu-id="d444f-192"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="d444f-192"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="d444f-193">*格式* 為 GL \_ 色彩 \_ 索引，以及儲存 RGBA 或 BGRA 色彩元件的色彩緩衝區。</span><span class="sxs-lookup"><span data-stu-id="d444f-193">*format* was GL\_COLOR\_INDEX, and the color buffers stored RGBA or BGRA color components.</span></span><br/>                                 |
| <dl> <span data-ttu-id="d444f-194"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="d444f-194"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="d444f-195">*格式* 為 GL 樣板索引，但沒有樣板 \_ \_ 緩衝區。</span><span class="sxs-lookup"><span data-stu-id="d444f-195">*format* was GL\_STENCIL\_INDEX, and there was no stencil buffer.</span></span><br/>                                                          |
| <dl> <span data-ttu-id="d444f-196"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="d444f-196"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="d444f-197">*格式* 為 GL \_ 深度 \_ 元件，但沒有深度緩衝區。</span><span class="sxs-lookup"><span data-stu-id="d444f-197">*format* was GL\_DEPTH\_COMPONENT, and there was no depth buffer.</span></span><br/>                                                          |
| <dl> <span data-ttu-id="d444f-198"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="d444f-198"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="d444f-199">呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。</span><span class="sxs-lookup"><span data-stu-id="d444f-199">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |

## <a name="remarks"></a><span data-ttu-id="d444f-200">備註</span><span class="sxs-lookup"><span data-stu-id="d444f-200">Remarks</span></span>

<span data-ttu-id="d444f-201">**GlReadPixels** 函式會從畫面格緩衝區傳回圖元資料，從左下角位置 (*x*， *y*) 的圖元開始，到以位置 *圖元* 開始的用戶端記憶體。</span><span class="sxs-lookup"><span data-stu-id="d444f-201">The **glReadPixels** function returns pixel data from the framebuffer, starting with the pixel whose lower-left corner is at location (*x*, *y*), into client memory starting at location *pixels*.</span></span> <span data-ttu-id="d444f-202">有幾個參數會控制將圖元資料放入用戶端記憶體之前的處理。</span><span class="sxs-lookup"><span data-stu-id="d444f-202">Several parameters control the processing of the pixel data before it is placed into client memory.</span></span> <span data-ttu-id="d444f-203">這些參數會以三個命令設定： [**glPixelStore**](glpixelstore-functions.md)、 [**glPixelTransfer**](glpixeltransfer.md)和 [**glPixelMap**](glpixelmap.md)。</span><span class="sxs-lookup"><span data-stu-id="d444f-203">These parameters are set with three commands: [**glPixelStore**](glpixelstore-functions.md), [**glPixelTransfer**](glpixeltransfer.md), and [**glPixelMap**](glpixelmap.md).</span></span> <span data-ttu-id="d444f-204">本主題說明大部分（但不是這三個命令所指定的所有參數）對 **glReadPixels** 的影響。</span><span class="sxs-lookup"><span data-stu-id="d444f-204">This topic describes the effects on **glReadPixels** of most, but not all of the parameters specified by these three commands.</span></span>

<span data-ttu-id="d444f-205">**GlReadPixels** 函式會從左下角 (*x* + i、 *y* + j) 的每個圖元傳回值，0 = i <*寬度* 和 0 = j <*高度*。</span><span class="sxs-lookup"><span data-stu-id="d444f-205">The **glReadPixels** function returns values from each pixel with lower-left corner at (*x* + i, *y* + j) for 0 = i < *width* and 0 = j < *height*.</span></span> <span data-ttu-id="d444f-206">這個圖元就是第一個 *j*# 資料列中的第 *i* 個圖元。</span><span class="sxs-lookup"><span data-stu-id="d444f-206">This pixel is said to be the *i* th pixel in the *j* th row.</span></span> <span data-ttu-id="d444f-207">在每個資料列中，從最小到最高的資料列，以左至右的順序傳回圖元。</span><span class="sxs-lookup"><span data-stu-id="d444f-207">Pixels are returned in row order from the lowest to the highest row, left to right in each row.</span></span>

<span data-ttu-id="d444f-208">上述的 shift、scale、偏差和 lookup 因數都是由 [**glPixelTransfer**](glpixeltransfer.md)所指定。</span><span class="sxs-lookup"><span data-stu-id="d444f-208">The shift, scale, bias, and lookup factors described above are all specified by [**glPixelTransfer**](glpixeltransfer.md).</span></span> <span data-ttu-id="d444f-209">查閱資料表內容是由 [**glPixelMap**](glpixelmap.md)所指定。</span><span class="sxs-lookup"><span data-stu-id="d444f-209">The lookup table contents are specified by [**glPixelMap**](glpixelmap.md).</span></span>

<span data-ttu-id="d444f-210">最後一個步驟牽涉到將索引或元件轉換成正確的格式，如 *類型* 所指定。</span><span class="sxs-lookup"><span data-stu-id="d444f-210">The final step involves converting the indexes or components to the proper format, as specified by *type*.</span></span> <span data-ttu-id="d444f-211">如果 *格式* 為 gl \_ 色彩 \_ 索引或 gl \_ 樣板 \_ 索引，且 *類型* 不是 gl \_ FLOAT，則會使用下表中提供的遮罩值來遮罩每個索引。</span><span class="sxs-lookup"><span data-stu-id="d444f-211">If *format* is GL\_COLOR\_INDEX or GL\_STENCIL\_INDEX and *type* is not GL\_FLOAT, each index is masked with the mask value given in the following table.</span></span> <span data-ttu-id="d444f-212">如果 *type* 是 GL \_ FLOAT，則每個整數索引都會轉換成單精確度浮點數格式。</span><span class="sxs-lookup"><span data-stu-id="d444f-212">If *type* is GL\_FLOAT, then each integer index is converted to single-precision floating-point format.</span></span>

<span data-ttu-id="d444f-213">如果 *格式* 為 gl \_ RED、GL \_ 綠、gl \_ BLUE、gl \_ ALPHA、GL \_ RGB、GL \_ RGBA、GL \_ BGR \_ EXT、gl \_ BGRA \_ EXT、gl \_ 亮度或 gl \_ 亮度 \_ ALPHA，而 *類型* 不是 gl \_ FLOAT，則每個元件都會乘以上表所示的乘數。</span><span class="sxs-lookup"><span data-stu-id="d444f-213">If *format* is GL\_RED, GL\_GREEN, GL\_BLUE, GL\_ALPHA, GL\_RGB, GL\_RGBA, GL\_BGR\_EXT, GL\_BGRA\_EXT, GL\_LUMINANCE, or GL\_LUMINANCE\_ALPHA and *type* is not GL\_FLOAT, each component is multiplied by the multiplier shown in the preceding table.</span></span> <span data-ttu-id="d444f-214">如果 type 是 GL \_ FLOAT，則會將每個元件當做 (傳遞，或轉換成用戶端的單精確度浮點數格式（如果不同于 OpenGL) 所使用的格式）。</span><span class="sxs-lookup"><span data-stu-id="d444f-214">If type is GL\_FLOAT, then each component is passed as is (or converted to the client's single-precision floating-point format if it is different from the one used by OpenGL).</span></span>

<span data-ttu-id="d444f-215">傳回值會放在記憶體中，如下所示。</span><span class="sxs-lookup"><span data-stu-id="d444f-215">Return values are placed in memory as follows.</span></span> <span data-ttu-id="d444f-216">如果 *格式* 為 gl \_ 色彩 \_ 索引、gl \_ 樣板 \_ 索引、gl \_ 深度 \_ 元件、gl \_ 紅色、gl \_ 綠色、gl \_ 藍色、gl \_ ALPHA 或 gl \_ 亮度，則會傳回單一值，而 *j*# 第一個資料列的第 *i* 圖元資料會放在位置 (*j* ) *寬度*  +  *i*。</span><span class="sxs-lookup"><span data-stu-id="d444f-216">If *format* is GL\_COLOR\_INDEX, GL\_STENCIL\_INDEX, GL\_DEPTH\_COMPONENT, GL\_RED, GL\_GREEN, GL\_BLUE, GL\_ALPHA, or GL\_LUMINANCE, a single value is returned and the data for the *i* th pixel in the *j* th row is placed in location (*j* )*width* + *i*.</span></span> <span data-ttu-id="d444f-217">GL \_ RGB 和 gl \_ BGR \_ ext 會傳回三個值、GL \_ RGBA 和 gl BGRA EXT 會傳回四個值 \_ \_ ，而 gl \_ 亮度 ALPHA 會 \_ 針對每個圖元傳回兩個值，並將所有值對應至佔用連續空間的單一圖元（以 *圖元為單位）*。</span><span class="sxs-lookup"><span data-stu-id="d444f-217">GL\_RGB and GL\_BGR\_EXT return three values, GL\_RGBA and GL\_BGRA\_EXT return four values, and GL\_LUMINANCE\_ALPHA returns two values for each pixel, with all values corresponding to a single pixel occupying contiguous space in *pixels*.</span></span> <span data-ttu-id="d444f-218">[**GlPixelStore**](glpixelstore-functions.md)所設定的儲存體參數（例如 GL \_ 套件 \_ 交換 \_ 位元組和 gl \_ 套件 \_ LSB \_ ）會先影響資料寫入記憶體的方式。</span><span class="sxs-lookup"><span data-stu-id="d444f-218">Storage parameters set by [**glPixelStore**](glpixelstore-functions.md), such as GL\_PACK\_SWAP\_BYTES and GL\_PACK\_LSB\_FIRST, affect the way that data is written into memory.</span></span> <span data-ttu-id="d444f-219">如需描述，請參閱 [**glPixelStore**](glpixelstore-functions.md) 。</span><span class="sxs-lookup"><span data-stu-id="d444f-219">See [**glPixelStore**](glpixelstore-functions.md) for a description.</span></span>

<span data-ttu-id="d444f-220">在連接到目前 OpenGL 內容的視窗外的圖元值未定義。</span><span class="sxs-lookup"><span data-stu-id="d444f-220">Values for pixels that lie outside the window connected to the current OpenGL context are undefined.</span></span>

<span data-ttu-id="d444f-221">如果產生錯誤，則不會對 *圖元* 的內容進行任何變更。</span><span class="sxs-lookup"><span data-stu-id="d444f-221">If an error is generated, no change is made to the contents of *pixels*.</span></span>

<span data-ttu-id="d444f-222">下列函式會抓取 **glReadPixels** 的相關資訊：</span><span class="sxs-lookup"><span data-stu-id="d444f-222">The following function retrieves information related to **glReadPixels**:</span></span>

<span data-ttu-id="d444f-223">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 索引 \_ 模式的 glGet</span><span class="sxs-lookup"><span data-stu-id="d444f-223">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_INDEX\_MODE</span></span>

## <a name="requirements"></a><span data-ttu-id="d444f-224">規格需求</span><span class="sxs-lookup"><span data-stu-id="d444f-224">Requirements</span></span>



| <span data-ttu-id="d444f-225">需求</span><span class="sxs-lookup"><span data-stu-id="d444f-225">Requirement</span></span> | <span data-ttu-id="d444f-226">值</span><span class="sxs-lookup"><span data-stu-id="d444f-226">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d444f-227">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d444f-227">Minimum supported client</span></span><br/> | <span data-ttu-id="d444f-228">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d444f-228">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="d444f-229">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d444f-229">Minimum supported server</span></span><br/> | <span data-ttu-id="d444f-230">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d444f-230">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d444f-231">標頭</span><span class="sxs-lookup"><span data-stu-id="d444f-231">Header</span></span><br/>                   | <dl> <span data-ttu-id="d444f-232"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="d444f-232"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="d444f-233">程式庫</span><span class="sxs-lookup"><span data-stu-id="d444f-233">Library</span></span><br/>                  | <dl> <span data-ttu-id="d444f-234"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="d444f-234"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="d444f-235">DLL</span><span class="sxs-lookup"><span data-stu-id="d444f-235">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d444f-236"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d444f-236"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d444f-237">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d444f-237">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d444f-238">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="d444f-238">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="d444f-239">**glCopyPixels**</span><span class="sxs-lookup"><span data-stu-id="d444f-239">**glCopyPixels**</span></span>](glcopypixels.md)
</dt> <dt>

[<span data-ttu-id="d444f-240">**glDrawPixels**</span><span class="sxs-lookup"><span data-stu-id="d444f-240">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="d444f-241">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="d444f-241">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="d444f-242">**glPixelMap**</span><span class="sxs-lookup"><span data-stu-id="d444f-242">**glPixelMap**</span></span>](glpixelmap.md)
</dt> <dt>

[<span data-ttu-id="d444f-243">**glPixelStore**</span><span class="sxs-lookup"><span data-stu-id="d444f-243">**glPixelStore**</span></span>](glpixelstore-functions.md)
</dt> <dt>

[<span data-ttu-id="d444f-244">**glPixelTransfer**</span><span class="sxs-lookup"><span data-stu-id="d444f-244">**glPixelTransfer**</span></span>](glpixeltransfer.md)
</dt> <dt>

[<span data-ttu-id="d444f-245">**glReadBuffer**</span><span class="sxs-lookup"><span data-stu-id="d444f-245">**glReadBuffer**</span></span>](glreadbuffer.md)
</dt> </dl>

 

 





