---
title: 'glCopyPixels 函式 (Gl) '
description: GlCopyPixels 函式會複製畫面格緩衝區中的圖元。
ms.assetid: c4055928-7b8b-4d0f-94f3-e3b9c0503308
keywords:
- glCopyPixels 函式 OpenGL
topic_type:
- apiref
api_name:
- glCopyPixels
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a7ba0833534d21e48c251da6491fee2996c3ed9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934510"
---
# <a name="glcopypixels-function"></a><span data-ttu-id="d5f6c-104">glCopyPixels 函式</span><span class="sxs-lookup"><span data-stu-id="d5f6c-104">glCopyPixels function</span></span>

<span data-ttu-id="d5f6c-105">**GlCopyPixels** 函式會複製畫面格緩衝區中的圖元。</span><span class="sxs-lookup"><span data-stu-id="d5f6c-105">The **glCopyPixels** function copies pixels in the framebuffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5f6c-106">語法</span><span class="sxs-lookup"><span data-stu-id="d5f6c-106">Syntax</span></span>


```C++
void WINAPI glCopyPixels(
   GLint   x,
   GLint   y,
   GLsizei width,
   GLsizei height,
   GLenum  type
);
```



## <a name="parameters"></a><span data-ttu-id="d5f6c-107">參數</span><span class="sxs-lookup"><span data-stu-id="d5f6c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5f6c-108">*x*</span><span class="sxs-lookup"><span data-stu-id="d5f6c-108">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="d5f6c-109">要複製之圖元矩形區域左下角的視窗 x 平面座標。</span><span class="sxs-lookup"><span data-stu-id="d5f6c-109">The window x-plane coordinate of the lower-left corner of the rectangular region of pixels to be copied.</span></span>

</dd> <dt>

<span data-ttu-id="d5f6c-110">*y*</span><span class="sxs-lookup"><span data-stu-id="d5f6c-110">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="d5f6c-111">要複製之圖元矩形區域左下角的視窗 y 平面座標。</span><span class="sxs-lookup"><span data-stu-id="d5f6c-111">The window y-plane coordinate of the lower-left corner of the rectangular region of pixels to be copied.</span></span>

</dd> <dt>

<span data-ttu-id="d5f6c-112">*width* (寬度)</span><span class="sxs-lookup"><span data-stu-id="d5f6c-112">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="d5f6c-113">要複製之圖元矩形區域的寬度維度。</span><span class="sxs-lookup"><span data-stu-id="d5f6c-113">The width dimension of the rectangular region of pixels to be copied.</span></span> <span data-ttu-id="d5f6c-114">不可為負值。</span><span class="sxs-lookup"><span data-stu-id="d5f6c-114">Must be nonnegative.</span></span>

</dd> <dt>

<span data-ttu-id="d5f6c-115">*height* (高度)</span><span class="sxs-lookup"><span data-stu-id="d5f6c-115">*height*</span></span> 
</dt> <dd>

<span data-ttu-id="d5f6c-116">要複製之圖元矩形區域的高度維度。</span><span class="sxs-lookup"><span data-stu-id="d5f6c-116">The height dimension of the rectangular region of pixels to be copied.</span></span> <span data-ttu-id="d5f6c-117">不可為負值。</span><span class="sxs-lookup"><span data-stu-id="d5f6c-117">Must be nonnegative.</span></span>

</dd> <dt>

<span data-ttu-id="d5f6c-118">*type*</span><span class="sxs-lookup"><span data-stu-id="d5f6c-118">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="d5f6c-119">指定 **glCopyPixels** 是否要複製色彩值、深度值或樣板值。</span><span class="sxs-lookup"><span data-stu-id="d5f6c-119">Specifies whether **glCopyPixels** is to copy color values, depth values, or stencil values.</span></span> <span data-ttu-id="d5f6c-120">可接受的符號常數為。</span><span class="sxs-lookup"><span data-stu-id="d5f6c-120">The acceptable symbolic constants are.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d5f6c-121">值</span><span class="sxs-lookup"><span data-stu-id="d5f6c-121">Value</span></span></th>
<th><span data-ttu-id="d5f6c-122">意義</span><span class="sxs-lookup"><span data-stu-id="d5f6c-122">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="GL_COLOR"></span><span id="gl_color"></span><dl> <span data-ttu-id="d5f6c-123"><dt><strong>GL_COLOR</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="d5f6c-123"><dt><strong>GL_COLOR</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="d5f6c-124"><strong>GlCopyPixels</strong>函式會從目前指定為讀取來源緩衝區的緩衝區讀取索引或 RGBA 色彩 (查看<a href="glreadbuffer.md"><strong>glReadBuffer</strong></a>) 。</span><span class="sxs-lookup"><span data-stu-id="d5f6c-124">The <strong>glCopyPixels</strong> function reads indexes or RGBA colors from the buffer currently specified as the read source buffer (see <a href="glreadbuffer.md"><strong>glReadBuffer</strong></a>).</span></span> <br/> <span data-ttu-id="d5f6c-125">如果 OpenGL 處於色彩索引模式：</span><span class="sxs-lookup"><span data-stu-id="d5f6c-125">If OpenGL is in color-index mode:</span></span><br/>
<ol>
<li><span data-ttu-id="d5f6c-126">從這個緩衝區讀取的每個索引都會轉換成指向二進位點右邊未指定位數的固定點格式。</span><span class="sxs-lookup"><span data-stu-id="d5f6c-126">Each index that is read from this buffer is converted to a fixed-point format with an unspecified number of bits to the right of the binary point.</span></span></li>
<li><span data-ttu-id="d5f6c-127">每個索引都會 GL_INDEX_SHIFT 位左移，並新增至 GL_INDEX_OFFSET。如果 GL_INDEX_SHIFT 為負數，則向右移位。</span><span class="sxs-lookup"><span data-stu-id="d5f6c-127">Each index is shifted left by GL_INDEX_SHIFT bits, and added to GL_INDEX_OFFSET.If GL_INDEX_SHIFT is negative, the shift is to the right.</span></span> <span data-ttu-id="d5f6c-128">無論是哪一種情況，在結果中都不會以零位填滿指定的位位置。</span><span class="sxs-lookup"><span data-stu-id="d5f6c-128">In either case, zero bits fill otherwise unspecified bit locations in the result.</span></span><br/></li>
<li><span data-ttu-id="d5f6c-129">如果 GL_MAP_COLOR 為 true，就會將索引取代為它在查閱資料表 GL_PIXEL_MAP_I_TO_I 中所參考的值。</span><span class="sxs-lookup"><span data-stu-id="d5f6c-129">If GL_MAP_COLOR is true, the index is replaced with the value that it references in lookup table GL_PIXEL_MAP_I_TO_I.</span></span></li>
<li><span data-ttu-id="d5f6c-130">如果索引的查閱取代是否已完成，索引的整數部分就是， <strong>而</strong>ed 的整數部分是 2<em><sup>b</sup></em> 1，其中 <em>b</em> 是色彩索引緩衝區中的位數。</span><span class="sxs-lookup"><span data-stu-id="d5f6c-130">Whether the lookup replacement of the index is done or not, the integer part of the index is then <strong>AND</strong>ed with 2<em><sup>b</sup></em> 1, where <em>b</em> is the number of bits in a color-index buffer.</span></span></li>
</ol>
<span data-ttu-id="d5f6c-131">如果 OpenGL 處於 RGBA 模式：</span><span class="sxs-lookup"><span data-stu-id="d5f6c-131">If OpenGL is in RGBA mode:</span></span><br/>
<ol>
<li><span data-ttu-id="d5f6c-132">每個讀取之圖元的紅色、綠色、藍色和 Alpha 元件都會轉換成具有未指定精確度的內部浮點格式。</span><span class="sxs-lookup"><span data-stu-id="d5f6c-132">The red, green, blue, and alpha components of each pixel that is read are converted to an internal floating-point format with unspecified precision.</span></span></li>
<li><span data-ttu-id="d5f6c-133">轉換會將最大可表示的元件值對應至1.0，並將元件值0對應至0.0。</span><span class="sxs-lookup"><span data-stu-id="d5f6c-133">The conversion maps the largest representable component value to 1.0, and component value zero to 0.0.</span></span></li>
<li><span data-ttu-id="d5f6c-134">產生的浮點色彩值接著會乘以 GL_c_SCALE 並新增至 GL_c_BIAS，其中 <em>c</em> 是紅色、綠色、藍色和 ALPHA，適用于個別的色彩元件。</span><span class="sxs-lookup"><span data-stu-id="d5f6c-134">The resulting floating-point color values are then multiplied by GL_c_SCALE and added to GL_c_BIAS, where <em>c</em> is RED, GREEN, BLUE, and ALPHA for the respective color components.</span></span></li>
<li><span data-ttu-id="d5f6c-135">結果會壓制到 [0，1] 範圍內。</span><span class="sxs-lookup"><span data-stu-id="d5f6c-135">The results are clamped to the range [0,1].</span></span></li>
<li><span data-ttu-id="d5f6c-136">如果 GL_MAP_COLOR 為 true，則每個色彩元件都會依查閱資料表的大小進行調整 GL_PIXEL_MAP_c_TO_c，然後以它在該資料表中參考的值取代; <em>c</em> 分別為 R、G、B 或 A。</span><span class="sxs-lookup"><span data-stu-id="d5f6c-136">If GL_MAP_COLOR is true, each color component is scaled by the size of lookup table GL_PIXEL_MAP_c_TO_c, and then replaced by the value that it references in that table; <em>c</em> is R, G, B, or A, respectively.</span></span> <span data-ttu-id="d5f6c-137">接著，會將目前的點陣位置<em>z</em>座標和材質座標附加至每個圖元，然後指派視窗座標 (<em>x</em><sub>r</sub> + i、 <em>y</em><sub>r</sub> + <em>j</em>) ，其中 (<em>x</em><sub>r</sub> 、 <em>y</em><sub>r</sub> ) 是目前的點陣位置，而圖元是在<em>j</em>資料列中<em>i</em>位置的圖元，則會將結果的索引或 RGBA 色彩轉換成片段。</span><span class="sxs-lookup"><span data-stu-id="d5f6c-137">The resulting indexes or RGBA colors are then converted to fragments by attaching the current raster position <em>z</em>-coordinate and texture coordinates to each pixel, and then assigning window coordinates (<em>x</em><sub>r</sub> + i, <em>y</em><sub>r</sub> + <em>j</em>), where (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) is the current raster position, and the pixel was the pixel in the <em>i</em> position in the <em>j</em> row.</span></span> <span data-ttu-id="d5f6c-138">然後，這些圖元片段的處理方式就像是將點、線條或多邊形所產生的片段一樣。</span><span class="sxs-lookup"><span data-stu-id="d5f6c-138">These pixel fragments are then treated just like the fragments generated by rasterizing points, lines, or polygons.</span></span> <span data-ttu-id="d5f6c-139">材質對應、霧化和所有片段作業都是在片段寫入至畫面格緩衝區之前套用。</span><span class="sxs-lookup"><span data-stu-id="d5f6c-139">Texture mapping, fog, and all the fragment operations are applied before the fragments are written to the framebuffer.</span></span><br/></li>
</ol></td>
</tr>
<tr class="even">
<td><span id="GL_DEPTH"></span><span id="gl_depth"></span><dl> <span data-ttu-id="d5f6c-140"><dt><strong>GL_DEPTH</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="d5f6c-140"><dt><strong>GL_DEPTH</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="d5f6c-141">深度的值會從深度緩衝區讀取，並直接轉換成具有未指定精確度的內部浮點格式。</span><span class="sxs-lookup"><span data-stu-id="d5f6c-141">Depth values are read from the depth buffer and converted directly to an internal floating-point format with unspecified precision.</span></span> <span data-ttu-id="d5f6c-142">產生的浮點數深度值接著會乘以 GL_DEPTH_SCALE，並新增至 GL_DEPTH_BIAS。</span><span class="sxs-lookup"><span data-stu-id="d5f6c-142">The resulting floating-point depth value is then multiplied by GL_DEPTH_SCALE and added to GL_DEPTH_BIAS.</span></span> <span data-ttu-id="d5f6c-143">結果會壓制至範圍 [0，1]。</span><span class="sxs-lookup"><span data-stu-id="d5f6c-143">The result is clamped to the range [0,1].</span></span> <br/> <span data-ttu-id="d5f6c-144">然後，會將目前的點陣位置色彩或色彩索引和材質座標附加至每個圖元，然後指派視窗座標 (<em>x</em><sub>r</sub> + i、 <em>y</em><sub>r</sub> + <em>j</em>) ，其中 (<em>x</em><sub>r</sub> 、 <em>y</em><sub>r</sub> ) 是目前的點陣位置，而圖元是在<em>j</em>資料列中<em>i</em>位置的圖元，則會轉換成片段。</span><span class="sxs-lookup"><span data-stu-id="d5f6c-144">The resulting depth components are then converted to fragments by attaching the current raster position color or color index and texture coordinates to each pixel, then assigning window coordinates (<em>x</em><sub>r</sub> + i, <em>y</em><sub>r</sub> + <em>j</em>), where (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) is the current raster position, and the pixel was the pixel in the <em>i</em> position in the <em>j</em> row.</span></span> <span data-ttu-id="d5f6c-145">然後，這些圖元片段的處理方式就像是將點、線條或多邊形所產生的片段一樣。</span><span class="sxs-lookup"><span data-stu-id="d5f6c-145">These pixel fragments are then treated just like the fragments generated by rasterizing points, lines, or polygons.</span></span> <span data-ttu-id="d5f6c-146">材質對應、霧化和所有片段作業都是在片段寫入至畫面格緩衝區之前套用。</span><span class="sxs-lookup"><span data-stu-id="d5f6c-146">Texture mapping, fog, and all the fragment operations are applied before the fragments are written to the framebuffer.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="GL_STENCIL"></span><span id="gl_stencil"></span><dl> <span data-ttu-id="d5f6c-147"><dt><strong>GL_STENCIL</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="d5f6c-147"><dt><strong>GL_STENCIL</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="d5f6c-148">樣板索引會從樣板緩衝區中讀取，並轉換為內部的固定點格式，並在二進位點右邊有未指定的位數。</span><span class="sxs-lookup"><span data-stu-id="d5f6c-148">Stencil indexes are read from the stencil buffer and converted to an internal fixed-point format with an unspecified number of bits to the right of the binary point.</span></span> <span data-ttu-id="d5f6c-149">然後，每個固定點索引會依 GL_INDEX_SHIFT 位向左移，並新增至 GL_INDEX_OFFSET。</span><span class="sxs-lookup"><span data-stu-id="d5f6c-149">Each fixed-point index is then shifted left by GL_INDEX_SHIFT bits, and added to GL_INDEX_OFFSET.</span></span> <span data-ttu-id="d5f6c-150">如果 GL_INDEX_SHIFT 為負數，則向右移位。</span><span class="sxs-lookup"><span data-stu-id="d5f6c-150">If GL_INDEX_SHIFT is negative, the shift is to the right.</span></span> <span data-ttu-id="d5f6c-151">無論是哪一種情況，在結果中都不會以零位填滿指定的位位置。</span><span class="sxs-lookup"><span data-stu-id="d5f6c-151">In either case, zero bits fill otherwise unspecified bit locations in the result.</span></span> <span data-ttu-id="d5f6c-152">如果 GL_MAP_STENCIL 為 true，就會將索引取代為它在查閱資料表 GL_PIXEL_MAP_S_TO_S 中所參考的值。</span><span class="sxs-lookup"><span data-stu-id="d5f6c-152">If GL_MAP_STENCIL is true, the index is replaced with the value that it references in lookup table GL_PIXEL_MAP_S_TO_S.</span></span> <span data-ttu-id="d5f6c-153">如果索引的查閱取代是否已完成，索引的整數部分就是， <strong>而</strong>ed 的整數部分則是 2<sup>b</sup> - 1，其中 <em>b</em> 是樣板緩衝區中的位數。</span><span class="sxs-lookup"><span data-stu-id="d5f6c-153">Whether the lookup replacement of the index is done or not, the integer part of the index is then <strong>AND</strong>ed with 2<sup>b</sup> - 1, where <em>b</em> is the number of bits in the stencil buffer.</span></span> <span data-ttu-id="d5f6c-154">接著會將產生的樣板索引寫入至樣板緩衝區，以便從<em>j</em>資料列的<em>i</em>位置讀取的索引會寫入位置 (<em>x</em><sub>r</sub> + <em>i</em>， <em>y</em><sub>r</sub> + <em>j</em>) ，其中 (<em>x</em><sub>r</sub> ， <em>y</em><sub>r</sub> ) 是目前的點陣位置。</span><span class="sxs-lookup"><span data-stu-id="d5f6c-154">The resulting stencil indexes are then written to the stencil buffer such that the index read from the <em>i</em> location of the <em>j</em> row is written to location (<em>x</em><sub>r</sub> + <em>i</em>, <em>y</em><sub>r</sub> + <em>j</em>), where (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) is the current raster position.</span></span> <span data-ttu-id="d5f6c-155">只有圖元擁有權的測試、剪下測試和樣板 writemask 會影響這些寫入。</span><span class="sxs-lookup"><span data-stu-id="d5f6c-155">Only the pixel-ownership test, the scissor test, and the stencil writemask affect these writes.</span></span><br/></td>
</tr>
</tbody>
</table>



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5f6c-156">傳回值</span><span class="sxs-lookup"><span data-stu-id="d5f6c-156">Return value</span></span>

<span data-ttu-id="d5f6c-157">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="d5f6c-157">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="d5f6c-158">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="d5f6c-158">Error codes</span></span>

<span data-ttu-id="d5f6c-159">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="d5f6c-159">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="d5f6c-160">Name</span><span class="sxs-lookup"><span data-stu-id="d5f6c-160">Name</span></span>                                                                                                  | <span data-ttu-id="d5f6c-161">意義</span><span class="sxs-lookup"><span data-stu-id="d5f6c-161">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d5f6c-162"><dt>**GL \_ 無效 \_ 列舉**</dt></span><span class="sxs-lookup"><span data-stu-id="d5f6c-162"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="d5f6c-163">*類型* 不是可接受的值。</span><span class="sxs-lookup"><span data-stu-id="d5f6c-163">*type* was not an accepted value.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="d5f6c-164"><dt>**GL \_ 無效 \_ 值**</dt></span><span class="sxs-lookup"><span data-stu-id="d5f6c-164"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="d5f6c-165">*寬度* 或高度都是負數。</span><span class="sxs-lookup"><span data-stu-id="d5f6c-165">Either *width* or height was negative.</span></span><br/>                                                                                     |
| <dl> <span data-ttu-id="d5f6c-166"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="d5f6c-166"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="d5f6c-167">*類型* 為 GL \_ 深度且沒有深度緩衝區。</span><span class="sxs-lookup"><span data-stu-id="d5f6c-167">*type* was GL\_DEPTH and there was no depth buffer.</span></span><br/>                                                                        |
| <dl> <span data-ttu-id="d5f6c-168"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="d5f6c-168"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="d5f6c-169">*類型* 為 GL 樣板，但沒有 \_ 任何樣板緩衝區。</span><span class="sxs-lookup"><span data-stu-id="d5f6c-169">*type* was GL\_STENCIL and there was no stencil buffer.</span></span><br/>                                                                    |
| <dl> <span data-ttu-id="d5f6c-170"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="d5f6c-170"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="d5f6c-171">呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。</span><span class="sxs-lookup"><span data-stu-id="d5f6c-171">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="d5f6c-172">備註</span><span class="sxs-lookup"><span data-stu-id="d5f6c-172">Remarks</span></span>

<span data-ttu-id="d5f6c-173">**GlCopyPixels** 函式會從指定的畫面格緩衝區位置將螢幕對齊的圖元矩形複製到相對於目前點陣位置的區域。</span><span class="sxs-lookup"><span data-stu-id="d5f6c-173">The **glCopyPixels** function copies a screen-aligned rectangle of pixels from the specified framebuffer location to a region relative to the current raster position.</span></span> <span data-ttu-id="d5f6c-174">只有在整個圖元來源區域都在視窗的公開部分內時，才會妥善定義其作業。</span><span class="sxs-lookup"><span data-stu-id="d5f6c-174">Its operation is well defined only if the entire pixel source region is within the exposed portion of the window.</span></span> <span data-ttu-id="d5f6c-175">從視窗外部或未公開之視窗的區域產生的複本結果，會與硬體相依或未定義。</span><span class="sxs-lookup"><span data-stu-id="d5f6c-175">Results of copies from outside the window, or from regions of the window that are not exposed, are hardware dependent and undefined.</span></span>

<span data-ttu-id="d5f6c-176">*X* 和 *y* 參數指定要複製之矩形區域左下角的視窗座標。</span><span class="sxs-lookup"><span data-stu-id="d5f6c-176">The *x* and *y* parameters specify the window coordinates of the lower-left corner of the rectangular region to be copied.</span></span> <span data-ttu-id="d5f6c-177">*寬度* 和 *高度* 參數指定要複製之矩形區域的維度。</span><span class="sxs-lookup"><span data-stu-id="d5f6c-177">The *width* and *height* parameters specify the dimensions of the rectangular region to be copied.</span></span> <span data-ttu-id="d5f6c-178">*寬度* 和 *高度* 都必須是非負值。</span><span class="sxs-lookup"><span data-stu-id="d5f6c-178">Both *width* and *height* must be nonnegative.</span></span>

<span data-ttu-id="d5f6c-179">有幾個參數會控制正在複製的圖元資料處理。</span><span class="sxs-lookup"><span data-stu-id="d5f6c-179">Several parameters control the processing of the pixel data while it is being copied.</span></span> <span data-ttu-id="d5f6c-180">這些參數會以三個函式設定： [**glPixelTransfer**](glpixeltransfer.md)、 [**glPixelMap**](glpixelmap.md)和 [**glPixelZoom**](glpixelzoom.md)。</span><span class="sxs-lookup"><span data-stu-id="d5f6c-180">These parameters are set with three functions: [**glPixelTransfer**](glpixeltransfer.md), [**glPixelMap**](glpixelmap.md), and [**glPixelZoom**](glpixelzoom.md).</span></span> <span data-ttu-id="d5f6c-181">本主題說明 **glCopyPixels** 這三個函式所指定的大部分（但非全部）參數的效果。</span><span class="sxs-lookup"><span data-stu-id="d5f6c-181">This topic describes the effects on **glCopyPixels** of most, but not all, of the parameters specified by these three functions.</span></span>

<span data-ttu-id="d5f6c-182">**GlCopyPixels** 函式會在 (*x* i、y j) 的左下角，將每個圖元的值複製到  +     +   0 = *i* 的  <  *寬度* 和 0 = *j*  <  *高度*。</span><span class="sxs-lookup"><span data-stu-id="d5f6c-182">The **glCopyPixels** function copies values from each pixel with the lower-left corner at (*x* + *i*, *y* + *j*) for 0 = *i* < *width* and 0 = *j* < *height*.</span></span> <span data-ttu-id="d5f6c-183">這個圖元稱為 *j* 資料列中的 *i* 圖元。</span><span class="sxs-lookup"><span data-stu-id="d5f6c-183">This pixel is said to be the *i* pixel in the *j* row.</span></span> <span data-ttu-id="d5f6c-184">在每個資料列中，會以資料列順序從最小到最高的資料列複製圖元。</span><span class="sxs-lookup"><span data-stu-id="d5f6c-184">Pixels are copied in row order from the lowest to the highest row, left to right in each row.</span></span>

<span data-ttu-id="d5f6c-185">*Type* 參數會指定是否要複製 color、depth 或樣板資料。</span><span class="sxs-lookup"><span data-stu-id="d5f6c-185">The *type* parameter specifies whether color, depth, or stencil data is to be copied.</span></span>

<span data-ttu-id="d5f6c-186">目前為止所描述的點陣化會假設圖元縮放因數為1.0。</span><span class="sxs-lookup"><span data-stu-id="d5f6c-186">The rasterization described thus far assumes pixel zoom factors of 1.0.</span></span> <span data-ttu-id="d5f6c-187">如果您使用 [**glPixelZoom**](glpixelzoom.md) 來變更 *x* 和 *y* 圖元縮放因數，圖元會轉換成片段，如下所示。</span><span class="sxs-lookup"><span data-stu-id="d5f6c-187">If you use [**glPixelZoom**](glpixelzoom.md) to change the *x* and *y* pixel zoom factors, pixels are converted to fragments as follows.</span></span> <span data-ttu-id="d5f6c-188">如果 (*x*<sub>r</sub> ， *y*<sub>r</sub> ) 是目前的點陣位置，而指定的圖元位於來源圖元矩形的 *j* 資料列中的 *i* 個位置，則會為其中心位於矩形中邊角為矩形的圖元產生片段。</span><span class="sxs-lookup"><span data-stu-id="d5f6c-188">If (*x*<sub>r</sub> , *y*<sub>r</sub> ) is the current raster position, and a given pixel is in the *i* location in the *j* row of the source pixel rectangle, then fragments are generated for pixels whose centers are in the rectangle with corners at</span></span>

<span data-ttu-id="d5f6c-189"> (*x*<sub>r</sub>  +  *zoom*？ i，y <sub>r</sub>  +  *zoom*<sub>y</sub> *j*) </span><span class="sxs-lookup"><span data-stu-id="d5f6c-189">(*x*<sub>r</sub> + *zoom*? i, y <sub>r</sub> + *zoom*<sub>y</sub> *j*)</span></span>

<span data-ttu-id="d5f6c-190">及</span><span class="sxs-lookup"><span data-stu-id="d5f6c-190">and</span></span>

<span data-ttu-id="d5f6c-191"> (*x*<sub>r</sub>  +  *縮放比例*？</span><span class="sxs-lookup"><span data-stu-id="d5f6c-191">(*x*<sub>r</sub> + *zoom*?</span></span> <span data-ttu-id="d5f6c-192"> (*i* + 1) ， *y*<sub>r</sub>  +  *zoom*<sub>y</sub> (*j* + 1) ) </span><span class="sxs-lookup"><span data-stu-id="d5f6c-192">(*i* + 1), *y*<sub>r</sub> + *zoom*<sub>y</sub> (*j* + 1))</span></span>

<span data-ttu-id="d5f6c-193">哪裡 *縮放*？是 gl zoom \_ \_ X 和 *ZOOM*<sub>y</sub> 的值是 gl zoom y 的值 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="d5f6c-193">where *zoom*? is the value of GL\_ZOOM\_X and *zoom*<sub>y</sub> is the value of GL\_ZOOM\_Y.</span></span>

<span data-ttu-id="d5f6c-194">[**GlPixelStore**](glpixelstore-functions.md)指定的模式不會影響 **glCopyPixels** 的操作。</span><span class="sxs-lookup"><span data-stu-id="d5f6c-194">Modes specified by [**glPixelStore**](glpixelstore-functions.md) have no effect on the operation of **glCopyPixels**.</span></span>

<span data-ttu-id="d5f6c-195">下列函式會取出與 **glCopyPixels** 相關的資訊：</span><span class="sxs-lookup"><span data-stu-id="d5f6c-195">The following functions retrieve information related to **glCopyPixels**:</span></span>

<span data-ttu-id="d5f6c-196">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 目前 \_ 點陣 \_ 位置的 glGet</span><span class="sxs-lookup"><span data-stu-id="d5f6c-196">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_RASTER\_POSITION</span></span>

<span data-ttu-id="d5f6c-197">具有引數 GL \_ 目前 \_ 點陣 \_ 位置 \_ 有效的 glGet</span><span class="sxs-lookup"><span data-stu-id="d5f6c-197">**glGet** with argument GL\_CURRENT\_RASTER\_POSITION\_VALID</span></span>

<span data-ttu-id="d5f6c-198">若要將視窗左下角的色彩圖元複製到目前的點陣位置，請使用</span><span class="sxs-lookup"><span data-stu-id="d5f6c-198">To copy the color pixel in the lower-left corner of the window to the current raster position, use</span></span>

<span data-ttu-id="d5f6c-199">**glCopyPixels** ( 0、0、1、1、GL \_ 色彩 ) ;</span><span class="sxs-lookup"><span data-stu-id="d5f6c-199">**glCopyPixels**( 0, 0, 1, 1, GL\_COLOR );</span></span>

## <a name="requirements"></a><span data-ttu-id="d5f6c-200">規格需求</span><span class="sxs-lookup"><span data-stu-id="d5f6c-200">Requirements</span></span>



| <span data-ttu-id="d5f6c-201">需求</span><span class="sxs-lookup"><span data-stu-id="d5f6c-201">Requirement</span></span> | <span data-ttu-id="d5f6c-202">值</span><span class="sxs-lookup"><span data-stu-id="d5f6c-202">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d5f6c-203">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d5f6c-203">Minimum supported client</span></span><br/> | <span data-ttu-id="d5f6c-204">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d5f6c-204">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="d5f6c-205">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d5f6c-205">Minimum supported server</span></span><br/> | <span data-ttu-id="d5f6c-206">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d5f6c-206">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d5f6c-207">標頭</span><span class="sxs-lookup"><span data-stu-id="d5f6c-207">Header</span></span><br/>                   | <dl> <span data-ttu-id="d5f6c-208"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="d5f6c-208"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="d5f6c-209">程式庫</span><span class="sxs-lookup"><span data-stu-id="d5f6c-209">Library</span></span><br/>                  | <dl> <span data-ttu-id="d5f6c-210"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="d5f6c-210"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="d5f6c-211">DLL</span><span class="sxs-lookup"><span data-stu-id="d5f6c-211">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d5f6c-212"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d5f6c-212"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5f6c-213">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d5f6c-213">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5f6c-214">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="d5f6c-214">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="d5f6c-215">**glDepthFunc**</span><span class="sxs-lookup"><span data-stu-id="d5f6c-215">**glDepthFunc**</span></span>](gldepthfunc.md)
</dt> <dt>

[<span data-ttu-id="d5f6c-216">**glDrawBuffer**</span><span class="sxs-lookup"><span data-stu-id="d5f6c-216">**glDrawBuffer**</span></span>](gldrawbuffer.md)
</dt> <dt>

[<span data-ttu-id="d5f6c-217">**glDrawPixels**</span><span class="sxs-lookup"><span data-stu-id="d5f6c-217">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="d5f6c-218">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="d5f6c-218">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="d5f6c-219">**glGet**</span><span class="sxs-lookup"><span data-stu-id="d5f6c-219">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="d5f6c-220">**glPixelMap**</span><span class="sxs-lookup"><span data-stu-id="d5f6c-220">**glPixelMap**</span></span>](glpixelmap.md)
</dt> <dt>

[<span data-ttu-id="d5f6c-221">**glPixelStore**</span><span class="sxs-lookup"><span data-stu-id="d5f6c-221">**glPixelStore**</span></span>](glpixelstore-functions.md)
</dt> <dt>

[<span data-ttu-id="d5f6c-222">**glPixelTransfer**</span><span class="sxs-lookup"><span data-stu-id="d5f6c-222">**glPixelTransfer**</span></span>](glpixeltransfer.md)
</dt> <dt>

[<span data-ttu-id="d5f6c-223">**glPixelZoom**</span><span class="sxs-lookup"><span data-stu-id="d5f6c-223">**glPixelZoom**</span></span>](glpixelzoom.md)
</dt> <dt>

[<span data-ttu-id="d5f6c-224">**glRasterPos**</span><span class="sxs-lookup"><span data-stu-id="d5f6c-224">**glRasterPos**</span></span>](glrasterpos-functions.md)
</dt> <dt>

[<span data-ttu-id="d5f6c-225">**glReadBuffer**</span><span class="sxs-lookup"><span data-stu-id="d5f6c-225">**glReadBuffer**</span></span>](glreadbuffer.md)
</dt> <dt>

[<span data-ttu-id="d5f6c-226">**glReadPixels**</span><span class="sxs-lookup"><span data-stu-id="d5f6c-226">**glReadPixels**</span></span>](glreadpixels.md)
</dt> <dt>

[<span data-ttu-id="d5f6c-227">**glStencilFunc**</span><span class="sxs-lookup"><span data-stu-id="d5f6c-227">**glStencilFunc**</span></span>](glstencilfunc.md)
</dt> </dl>

 

 





