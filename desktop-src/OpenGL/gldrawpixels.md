---
title: 'glDrawPixels 函式 (Gl) '
description: GlDrawPixels 函式會將圖元區塊寫入至畫面格緩衝區。
ms.assetid: c4eda64f-a75e-4e6d-984d-af49414b94d8
keywords:
- glDrawPixels 函式 OpenGL
topic_type:
- apiref
api_name:
- glDrawPixels
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e25adc8ad28791086020a37d3a30651e169bfd07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094148"
---
# <a name="gldrawpixels-function"></a><span data-ttu-id="7b77a-104">glDrawPixels 函式</span><span class="sxs-lookup"><span data-stu-id="7b77a-104">glDrawPixels function</span></span>

<span data-ttu-id="7b77a-105">**GlDrawPixels** 函式會將圖元區塊寫入至畫面格緩衝區。</span><span class="sxs-lookup"><span data-stu-id="7b77a-105">The **glDrawPixels** function writes a block of pixels to the framebuffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b77a-106">語法</span><span class="sxs-lookup"><span data-stu-id="7b77a-106">Syntax</span></span>


```C++
void WINAPI glDrawPixels(
         GLsizei width,
         GLsizei height,
         GLenum  format,
         GLenum  type,
   const GLvoid  *pixels
);
```



## <a name="parameters"></a><span data-ttu-id="7b77a-107">參數</span><span class="sxs-lookup"><span data-stu-id="7b77a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b77a-108">*width* (寬度)</span><span class="sxs-lookup"><span data-stu-id="7b77a-108">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="7b77a-109">將寫入至畫面格緩衝區之圖元矩形的寬度維度。</span><span class="sxs-lookup"><span data-stu-id="7b77a-109">The width dimension of the pixel rectangle that will be written into the framebuffer.</span></span>

</dd> <dt>

<span data-ttu-id="7b77a-110">*height* (高度)</span><span class="sxs-lookup"><span data-stu-id="7b77a-110">*height*</span></span> 
</dt> <dd>

<span data-ttu-id="7b77a-111">將寫入至畫面格緩衝區之圖元矩形的高度維度。</span><span class="sxs-lookup"><span data-stu-id="7b77a-111">The height dimension of the pixel rectangle that will be written into the framebuffer.</span></span>

</dd> <dt>

<span data-ttu-id="7b77a-112">*format*</span><span class="sxs-lookup"><span data-stu-id="7b77a-112">*format*</span></span> 
</dt> <dd>

<span data-ttu-id="7b77a-113">圖元資料的格式。</span><span class="sxs-lookup"><span data-stu-id="7b77a-113">The format of the pixel data.</span></span> <span data-ttu-id="7b77a-114">可接受的符號常數如下所示。</span><span class="sxs-lookup"><span data-stu-id="7b77a-114">Acceptable symbolic constants are as follows.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7b77a-115">值</span><span class="sxs-lookup"><span data-stu-id="7b77a-115">Value</span></span></th>
<th><span data-ttu-id="7b77a-116">意義</span><span class="sxs-lookup"><span data-stu-id="7b77a-116">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="GL_COLOR_INDEX"></span><span id="gl_color_index"></span><dl> <span data-ttu-id="7b77a-117"><dt><strong>GL_COLOR_INDEX</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="7b77a-117"><dt><strong>GL_COLOR_INDEX</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="7b77a-118">每個圖元都是單一值，也就是色彩索引。</span><span class="sxs-lookup"><span data-stu-id="7b77a-118">Each pixel is a single value, a color index.</span></span> <br/>
<ol>
<li><span data-ttu-id="7b77a-119"><strong>GlDrawPixels</strong>函式會將每個圖元轉換成固定點格式，而不會有二進位點右邊未指定的位數數目，而不論記憶體資料類型為何。</span><span class="sxs-lookup"><span data-stu-id="7b77a-119">The <strong>glDrawPixels</strong> function converts each pixel to fixed-point format, with an unspecified number of bits to the right of the binary point, regardless of the memory data type.</span></span> <span data-ttu-id="7b77a-120">浮點值會轉換成真正的固定點值。</span><span class="sxs-lookup"><span data-stu-id="7b77a-120">Floating-point values convert to true fixed-point values.</span></span> <span data-ttu-id="7b77a-121"><strong>GlDrawPixels</strong>函式會將帶正負號和不帶正負號的整數資料轉換成設定為零的所有小數位。</span><span class="sxs-lookup"><span data-stu-id="7b77a-121">The <strong>glDrawPixels</strong> function converts signed and unsigned integer data with all fraction bits set to zero.</span></span> <span data-ttu-id="7b77a-122">函數會將點陣圖資料轉換為0.0 或1.0。</span><span class="sxs-lookup"><span data-stu-id="7b77a-122">The function converts bitmap data to either 0.0 or 1.0.</span></span></li>
<li><span data-ttu-id="7b77a-123"><strong>GlDrawPixels</strong>函式會將 GL_INDEX_SHIFT 位左方的每個固定點索引移至 GL_INDEX_OFFSET，並將它加入至。</span><span class="sxs-lookup"><span data-stu-id="7b77a-123">The <strong>glDrawPixels</strong> function shifts each fixed-point index left by GL_INDEX_SHIFT bits and adds it to GL_INDEX_OFFSET.</span></span> <span data-ttu-id="7b77a-124">如果 GL_INDEX_SHIFT 為負數，則向右移位。</span><span class="sxs-lookup"><span data-stu-id="7b77a-124">If GL_INDEX_SHIFT is negative, the shift is to the right.</span></span> <span data-ttu-id="7b77a-125">無論是哪一種情況，在結果中都不會以零位填滿指定的位位置。</span><span class="sxs-lookup"><span data-stu-id="7b77a-125">In either case, zero bits fill otherwise unspecified bit locations in the result.</span></span></li>
<li><span data-ttu-id="7b77a-126">在 RGBA 模式中， <strong>glDrawPixels</strong> 會使用 GL_PIXEL_MAP_I_TO_R、GL_PIXEL_MAP_I_TO_G、GL_PIXEL_MAP_I_TO_B 和 GL_PIXEL_MAP_I_TO_A 資料表，將產生的索引轉換成 RGBA 圖元。</span><span class="sxs-lookup"><span data-stu-id="7b77a-126">When in RGBA mode, <strong>glDrawPixels</strong> converts the resulting index to an RGBA pixel using the GL_PIXEL_MAP_I_TO_R, GL_PIXEL_MAP_I_TO_G, GL_PIXEL_MAP_I_TO_B, and GL_PIXEL_MAP_I_TO_A tables.</span></span> <span data-ttu-id="7b77a-127">當在色彩索引模式中，且 GL_MAP_COLOR 為 true 時，會將索引取代為查閱資料表中 <strong>glDrawPixels</strong> 參考的值 GL_PIXEL_MAP_I_TO_I。</span><span class="sxs-lookup"><span data-stu-id="7b77a-127">When in the color-index mode and GL_MAP_COLOR is true, the index is replaced with the value that <strong>glDrawPixels</strong> references in lookup table GL_PIXEL_MAP_I_TO_I.</span></span></li>
<li><span data-ttu-id="7b77a-128">如果索引的查閱取代是否已完成，索引的整數部分就是 <strong>和</strong>2<sup>b</sup> - 1 的 ed，其中 <em>b</em> 是色彩索引緩衝區中的位數。</span><span class="sxs-lookup"><span data-stu-id="7b77a-128">Whether the lookup replacement of the index is done or not, the integer part of the index is <strong>AND</strong>ed with 2<sup>b</sup> - 1, where <em>b</em> is the number of bits in a color-index buffer.</span></span></li>
<li><span data-ttu-id="7b77a-129">接著，會將目前的點陣位置 <em>z</em>座標和材質座標附加至每個圖元，然後將 <em>x</em> 和 <em>y</em> 視窗座標指派給 <em>n</em>個片段（例如 <em>x</em>），以將產生的索引或 RGBA 色彩轉換成片段：</span><span class="sxs-lookup"><span data-stu-id="7b77a-129">The resulting indexes or RGBA colors are then converted to fragments by attaching the current raster position <em>z</em>-coordinate and texture coordinates to each pixel, and then assigning <em>x</em> and <em>y</em> window coordinates to the <em>n</em>th fragment such that <em>x</em>?</span></span><span data-ttu-id="7b77a-130"> = <em>x</em><sub>r</sub> + <em>n</em> mod <em>寬度</em></span><span class="sxs-lookup"><span data-stu-id="7b77a-130"> = <em>x</em><sub>r</sub> + <em>n</em> mod <em>width</em></span></span><br/> <span data-ttu-id="7b77a-131"><em>y</em>？</span><span class="sxs-lookup"><span data-stu-id="7b77a-131"><em>y</em>?</span></span><span data-ttu-id="7b77a-132"> = <em>y</em><sub>r</sub> + <em>n/寬度</em></span><span class="sxs-lookup"><span data-stu-id="7b77a-132"> = <em>y</em><sub>r</sub> + <em>n/width</em></span></span><br/> <span data-ttu-id="7b77a-133">其中 (<em>x</em><sub>r</sub> ， <em>y</em><sub>r</sub> ) 是目前的點陣位置。</span><span class="sxs-lookup"><span data-stu-id="7b77a-133">where (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) is the current raster position.</span></span><br/></li>
<li><span data-ttu-id="7b77a-134"><strong>GlDrawPixels</strong>函式會將這些圖元片段視為與透過將點、線條或多邊形所產生的片段一樣。</span><span class="sxs-lookup"><span data-stu-id="7b77a-134">The <strong>glDrawPixels</strong> function treats these pixel fragments just like the fragments generated by rasterizing points, lines, or polygons.</span></span> <span data-ttu-id="7b77a-135">它會先套用材質對應、霧化和所有片段作業，然後再將片段寫入至畫面格緩衝區。</span><span class="sxs-lookup"><span data-stu-id="7b77a-135">It applies texture mapping, fog, and all the fragment operations before writing the fragments to the framebuffer.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span id="GL_STENCIL_INDEX"></span><span id="gl_stencil_index"></span><dl> <span data-ttu-id="7b77a-136"><dt><strong>GL_STENCIL_INDEX</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="7b77a-136"><dt><strong>GL_STENCIL_INDEX</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="7b77a-137">每個圖元都是單一值，也就是樣板索引。</span><span class="sxs-lookup"><span data-stu-id="7b77a-137">Each pixel is a single value, a stencil index.</span></span> <br/>
<ol>
<li><span data-ttu-id="7b77a-138"><strong>GlDrawPixels</strong>函式會將它轉換成固定點格式，而不指定二進位點右邊的位數（不論記憶體資料類型為何）。</span><span class="sxs-lookup"><span data-stu-id="7b77a-138">The <strong>glDrawPixels</strong> function converts it to fixed-point format, with an unspecified number of bits to the right of the binary point, regardless of the memory data type.</span></span> <span data-ttu-id="7b77a-139">浮點值會轉換成真正的固定點值。</span><span class="sxs-lookup"><span data-stu-id="7b77a-139">Floating-point values convert to true fixed-point values.</span></span> <span data-ttu-id="7b77a-140"><strong>GlDrawPixels</strong>函式會將帶正負號和不帶正負號的整數資料轉換成設定為零的所有小數位。</span><span class="sxs-lookup"><span data-stu-id="7b77a-140">The <strong>glDrawPixels</strong> function converts signed and unsigned integer data with all fraction bits set to zero.</span></span> <span data-ttu-id="7b77a-141">點陣圖資料會轉換為0.0 或1.0。</span><span class="sxs-lookup"><span data-stu-id="7b77a-141">Bitmap data converts to either 0.0 or 1.0.</span></span></li>
<li><span data-ttu-id="7b77a-142"><strong>GlDrawPixels</strong>函式會將每個固定點索引 GL_INDEX_SHIFT 位左移，並將其新增至 GL_INDEX_OFFSET。</span><span class="sxs-lookup"><span data-stu-id="7b77a-142">The <strong>glDrawPixels</strong> function shifts each fixed-point index left by GL_INDEX_SHIFT bits, and adds it to GL_INDEX_OFFSET.</span></span> <span data-ttu-id="7b77a-143">如果 GL_INDEX_SHIFT 為負數，則向右移位。</span><span class="sxs-lookup"><span data-stu-id="7b77a-143">If GL_INDEX_SHIFT is negative, the shift is to the right.</span></span> <span data-ttu-id="7b77a-144">無論是哪一種情況，在結果中都不會以零位填滿指定的位位置。</span><span class="sxs-lookup"><span data-stu-id="7b77a-144">In either case, zero bits fill otherwise unspecified bit locations in the result.</span></span></li>
<li><span data-ttu-id="7b77a-145">如果 GL_MAP_STENCIL 為 true，就會將索引取代為查閱資料表 GL_PIXEL_MAP_S_TO_S 中所參考的 <strong>glDrawPixels</strong> 值。</span><span class="sxs-lookup"><span data-stu-id="7b77a-145">If GL_MAP_STENCIL is true, the index is replaced with the value that <strong>glDrawPixels</strong> references in lookup table GL_PIXEL_MAP_S_TO_S.</span></span></li>
<li><span data-ttu-id="7b77a-146">如果索引的查閱取代是否已完成，索引的整數部分就是， <strong>而</strong>ed 的整數部分則是 2<sup>b</sup> - 1，其中 <em>b</em> 是樣板緩衝區中的位數。</span><span class="sxs-lookup"><span data-stu-id="7b77a-146">Whether the lookup replacement of the index is done or not, the integer part of the index is then <strong>AND</strong>ed with 2<sup>b</sup> - 1, where <em>b</em> is the number of bits in the stencil buffer.</span></span> <span data-ttu-id="7b77a-147">接著會將產生的樣板索引寫入至樣板緩衝區，以便將第 <em>n</em>個索引寫入至位置 <em>x</em>？</span><span class="sxs-lookup"><span data-stu-id="7b77a-147">The resulting stencil indexes are then written to the stencil buffer such that the <em>n</em>th index is written to location <em>x</em>?</span></span><span data-ttu-id="7b77a-148"> = <em>x</em><sub>r</sub> + <em>n</em> mod <em>寬度</em></span><span class="sxs-lookup"><span data-stu-id="7b77a-148"> = <em>x</em><sub>r</sub> + <em>n</em> mod <em>width</em></span></span><br/> <span data-ttu-id="7b77a-149"><em>y</em>？</span><span class="sxs-lookup"><span data-stu-id="7b77a-149"><em>y</em>?</span></span><span data-ttu-id="7b77a-150"> = <em>y</em><sub>r</sub> + <em>n/寬度</em></span><span class="sxs-lookup"><span data-stu-id="7b77a-150"> = <em>y</em><sub>r</sub> + <em>n/width</em></span></span><br/> <span data-ttu-id="7b77a-151">其中 (<em>x</em><sub>r</sub> ， <em></em> y<sub>r</sub> ) 是目前的點陣位置。</span><span class="sxs-lookup"><span data-stu-id="7b77a-151">where (<em>x</em><sub>r</sub> ,<em></em>y<sub>r</sub> ) is the current raster position.</span></span> <span data-ttu-id="7b77a-152">只有圖元擁有權測試、剪下測試和樣板 writemask 會影響這些寫入。</span><span class="sxs-lookup"><span data-stu-id="7b77a-152">Only the pixel ownership test, the scissor test, and the stencil writemask affect these writes.</span></span><br/></li>
</ol></td>
</tr>
<tr class="odd">
<td><span id="GL_DEPTH_COMPONENT"></span><span id="gl_depth_component"></span><dl> <span data-ttu-id="7b77a-153"><dt><strong>GL_DEPTH_COMPONENT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="7b77a-153"><dt><strong>GL_DEPTH_COMPONENT</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="7b77a-154">每個圖元都是一個深度的元件。</span><span class="sxs-lookup"><span data-stu-id="7b77a-154">Each pixel is a single-depth component.</span></span> <br/>
<ol>
<li><span data-ttu-id="7b77a-155"><strong>GlDrawPixels</strong>函式會將浮點數據直接轉換成具有未指定精確度的內部浮點格式。</span><span class="sxs-lookup"><span data-stu-id="7b77a-155">The <strong>glDrawPixels</strong> function converts floating-point data directly to an internal floating-point format with unspecified precision.</span></span> <span data-ttu-id="7b77a-156">帶正負號的整數資料會以線性方式對應至內部浮點格式，讓最正面可表示的整數值對應至1.0，而最大的可表示值會對應至-1.0。</span><span class="sxs-lookup"><span data-stu-id="7b77a-156">Signed integer data is mapped linearly to the internal floating-point format such that the most positive representable integer value maps to 1.0, and the most negative representable value maps to -1.0.</span></span> <span data-ttu-id="7b77a-157">不帶正負號的整數資料的對應方式如下：最大整數值對應至1.0，而零對應至0.0。</span><span class="sxs-lookup"><span data-stu-id="7b77a-157">Unsigned integer data is mapped similarly: the largest integer value maps to 1.0, and zero maps to 0.0.</span></span></li>
<li><span data-ttu-id="7b77a-158"><strong>GlDrawPixels</strong>函式會 GL_DEPTH_SCALE 將產生的浮點數深度值相乘，並將其新增至 GL_DEPTH_BIAS。</span><span class="sxs-lookup"><span data-stu-id="7b77a-158">The <strong>glDrawPixels</strong> function multiplies the resulting floating-point depth value by GL_DEPTH_SCALE and adds it to GL_DEPTH_BIAS.</span></span> <span data-ttu-id="7b77a-159">結果會壓制至範圍 [0，1]。</span><span class="sxs-lookup"><span data-stu-id="7b77a-159">The result is clamped to the range [0,1].</span></span></li>
<li><span data-ttu-id="7b77a-160"><strong>GlDrawPixels</strong>函式會將目前的點陣位置色彩或色彩索引和材質座標附加至每個圖元，然後將<em>x</em>和<em>y</em>視窗座標指派給<em>n</em>個片段（例如<em>x</em>），以將產生的深度元件轉換成片段：</span><span class="sxs-lookup"><span data-stu-id="7b77a-160">The <strong>glDrawPixels</strong> function converts the resulting depth components to fragments by attaching the current raster position color or color index and texture coordinates to each pixel, and then assigning <em>x</em> and <em>y</em> window coordinates to the <em>n</em> th fragment such that <em>x</em>?</span></span><span data-ttu-id="7b77a-161"> = <em></em>x<sub>r</sub> + <em>n</em> mod <em>寬度</em></span><span class="sxs-lookup"><span data-stu-id="7b77a-161"> = <em></em>x<sub>r</sub> + <em>n</em> mod <em>width</em></span></span><br/> <span data-ttu-id="7b77a-162"><em>y</em>？</span><span class="sxs-lookup"><span data-stu-id="7b77a-162"><em>y</em>?</span></span><span data-ttu-id="7b77a-163"> = <em>y</em><sub>r</sub> + <em>n/寬度</em></span><span class="sxs-lookup"><span data-stu-id="7b77a-163"> = <em>y</em><sub>r</sub> + <em>n/width</em></span></span><br/> <span data-ttu-id="7b77a-164">其中 (<em></em> x<sub>r</sub> ，<em>y</em><sub>r</sub> ) 是目前的點陣位置。</span><span class="sxs-lookup"><span data-stu-id="7b77a-164">where (<em></em>x<sub>r</sub> ,<em>y</em><sub>r</sub> ) is the current raster position.</span></span><br/></li>
<li><span data-ttu-id="7b77a-165">然後，這些圖元片段的處理方式就像是將點、線條或多邊形所產生的片段一樣。</span><span class="sxs-lookup"><span data-stu-id="7b77a-165">These pixel fragments are then treated just like the fragments generated by rasterizing points, lines, or polygons.</span></span> <span data-ttu-id="7b77a-166"><strong>GlDrawPixels</strong>函式會先套用材質對應、霧化和所有片段作業，然後再將片段寫入畫面格緩衝區。</span><span class="sxs-lookup"><span data-stu-id="7b77a-166">The <strong>glDrawPixels</strong> function applies texture mapping, fog, and all the fragment operations before writing the fragments to the framebuffer.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span id="GL_RGBA"></span><span id="gl_rgba"></span><dl> <span data-ttu-id="7b77a-167"><dt><strong>GL_RGBA</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="7b77a-167"><dt><strong>GL_RGBA</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="7b77a-168">每個圖元都是四個元件的群組，順序如下：紅色、綠色、藍色、Alpha。</span><span class="sxs-lookup"><span data-stu-id="7b77a-168">Each pixel is a four-component group in this order: red, green, blue, alpha.</span></span> <br/>
<ol>
<li><span data-ttu-id="7b77a-169"><strong>GlDrawPixels</strong>函式會將浮點值直接轉換成具有未指定精確度的內部浮點格式。</span><span class="sxs-lookup"><span data-stu-id="7b77a-169">The <strong>glDrawPixels</strong> function converts floating-point values directly to an internal floating-point format with unspecified precision.</span></span> <span data-ttu-id="7b77a-170">帶正負號的整數值會以線性方式對應至內部浮點格式，使最大的可表示整數值對應至1.0，而最大的可表示值會對應至-1.0。</span><span class="sxs-lookup"><span data-stu-id="7b77a-170">Signed integer values are mapped linearly to the internal floating-point format such that the most positive representable integer value maps to 1.0, and the most negative representable value maps to -1.0.</span></span> <span data-ttu-id="7b77a-171">不帶正負號的整數資料的對應方式如下：最大整數值對應至1.0，而零對應至0.0。</span><span class="sxs-lookup"><span data-stu-id="7b77a-171">Unsigned integer data is mapped similarly: the largest integer value maps to 1.0, and zero maps to 0.0.</span></span></li>
<li><span data-ttu-id="7b77a-172"><strong>GlDrawPixels</strong>函式會 GL_c_SCALE 來乘以產生的浮點色彩值，並將其新增至 GL_c_BIAS，其中<em>c</em>是紅色、綠色、藍色和 ALPHA （適用于個別色彩元件）。</span><span class="sxs-lookup"><span data-stu-id="7b77a-172">The <strong>glDrawPixels</strong> function multiplies the resulting floating-point color values by GL_c_SCALE and adds them to GL_c_BIAS, where <em>c</em> is RED, GREEN, BLUE, and ALPHA for the respective color components.</span></span> <span data-ttu-id="7b77a-173">結果會壓制到 [0，1] 範圍內。</span><span class="sxs-lookup"><span data-stu-id="7b77a-173">The results are clamped to the range [0,1].</span></span></li>
<li><span data-ttu-id="7b77a-174">如果 GL_MAP_COLOR 為 true， <strong>glDrawPixels</strong> 會依 GL_PIXEL_MAP_c_TO_c 的查閱資料表大小來調整每個色彩元件，然後以該資料表中參考的值取代該元件; <em>c</em> 分別為 R、G、B 或 A。</span><span class="sxs-lookup"><span data-stu-id="7b77a-174">If GL_MAP_COLOR is true, <strong>glDrawPixels</strong> scales each color component by the size of lookup table GL_PIXEL_MAP_c_TO_c, and then replaces the component by the value that it references in that table; <em>c</em> is R, G, B, or A, respectively.</span></span></li>
<li><span data-ttu-id="7b77a-175"><strong>GlDrawPixels</strong>函式會將目前的點陣位置<em>z</em>座標和材質座標附加至每個圖元，然後將<em>x</em>和<em>y</em>視窗座標指派給第<em>n</em>個片段（例如<em>x</em>），以將產生的 RGBA 色彩轉換成片段：</span><span class="sxs-lookup"><span data-stu-id="7b77a-175">The <strong>glDrawPixels</strong> function converts the resulting RGBA colors to fragments by attaching the current raster position <em>z</em>-coordinate and texture coordinates to each pixel, then assigning <em>x</em> and <em>y</em> window coordinates to the <em>n</em>th fragment such that <em>x</em>?</span></span><span data-ttu-id="7b77a-176"> = <em>x</em><sub>r</sub> + <em>n</em> mod <em>寬度</em></span><span class="sxs-lookup"><span data-stu-id="7b77a-176"> = <em>x</em><sub>r</sub> + <em>n</em> mod <em>width</em></span></span><br/> <span data-ttu-id="7b77a-177"><em>y</em>？</span><span class="sxs-lookup"><span data-stu-id="7b77a-177"><em>y</em>?</span></span><span data-ttu-id="7b77a-178"> = <em>y</em><sub>r</sub> + <em>n/width</em></span><span class="sxs-lookup"><span data-stu-id="7b77a-178"> = <em>y</em><sub>r</sub> + <em>n /width</em></span></span><br/> <span data-ttu-id="7b77a-179">其中 (<em>x</em><sub>r</sub> ，<em>y</em><sub>r</sub> ) 是目前的點陣位置。</span><span class="sxs-lookup"><span data-stu-id="7b77a-179">where (<em>x</em><sub>r</sub> ,<em>y</em><sub>r</sub> ) is the current raster position.</span></span><br/></li>
<li><span data-ttu-id="7b77a-180">然後，這些圖元片段的處理方式就像是將點、線條或多邊形所產生的片段一樣。</span><span class="sxs-lookup"><span data-stu-id="7b77a-180">These pixel fragments are then treated just like the fragments generated by rasterizing points, lines, or polygons.</span></span> <span data-ttu-id="7b77a-181"><strong>GlDrawPixels</strong>函式會先套用材質對應、霧化和所有片段作業，然後再將片段寫入畫面格緩衝區。</span><span class="sxs-lookup"><span data-stu-id="7b77a-181">The <strong>glDrawPixels</strong> function applies texture mapping, fog, and all the fragment operations before writing the fragments to the framebuffer.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span id="GL_RED"></span><span id="gl_red"></span><dl> <span data-ttu-id="7b77a-182"><dt><strong>GL_RED</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="7b77a-182"><dt><strong>GL_RED</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="7b77a-183">每個圖元都是單一的紅色元件。</span><span class="sxs-lookup"><span data-stu-id="7b77a-183">Each pixel is a single red component.</span></span><br/> <span data-ttu-id="7b77a-184"><strong>GlDrawPixels</strong>函式會以 RGBA 圖元的紅色元件相同的方式，將這個元件轉換成內部浮點格式，然後將其轉換為具有綠色和藍色設定為0.0 的 RGBA 圖元，並將 Alpha 設定為1.0。</span><span class="sxs-lookup"><span data-stu-id="7b77a-184">The <strong>glDrawPixels</strong> function converts this component to the internal floating-point format in the same way that the red component of an RGBA pixel is, and then converts it to an RGBA pixel with green and blue set to 0.0, and alpha set to 1.0.</span></span> <span data-ttu-id="7b77a-185">進行這項轉換之後，圖元的處理方式就像是將它當成 RGBA 圖元讀取一樣。</span><span class="sxs-lookup"><span data-stu-id="7b77a-185">After this conversion, the pixel is treated just as if it had been read as an RGBA pixel.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="GL_GREEN"></span><span id="gl_green"></span><dl> <span data-ttu-id="7b77a-186"><dt><strong>GL_GREEN</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="7b77a-186"><dt><strong>GL_GREEN</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="7b77a-187">每個圖元都是一個綠色的元件。</span><span class="sxs-lookup"><span data-stu-id="7b77a-187">Each pixel is a single green component.</span></span><br/> <span data-ttu-id="7b77a-188"><strong>GlDrawPixels</strong>函式會以 RGBA 圖元綠色元件的相同方式，將這個元件轉換成內部浮點格式，然後將其轉換為具有紅色和藍色設定為0.0 的 RGBA 圖元，然後將 Alpha 設定為1.0。</span><span class="sxs-lookup"><span data-stu-id="7b77a-188">The <strong>glDrawPixels</strong> function converts this component to the internal floating-point format in the same way that the green component of an RGBA pixel is, and then converts it to an RGBA pixel with red and blue set to 0.0, and alpha set to 1.0.</span></span> <span data-ttu-id="7b77a-189">進行這項轉換之後，圖元的處理方式就像是將它當成 RGBA 圖元讀取一樣。</span><span class="sxs-lookup"><span data-stu-id="7b77a-189">After this conversion, the pixel is treated just as if it had been read as an RGBA pixel.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="GL_BLUE"></span><span id="gl_blue"></span><dl> <span data-ttu-id="7b77a-190"><dt><strong>GL_BLUE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="7b77a-190"><dt><strong>GL_BLUE</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="7b77a-191">每個圖元都是單一藍色元件。</span><span class="sxs-lookup"><span data-stu-id="7b77a-191">Each pixel is a single blue component.</span></span><br/> <span data-ttu-id="7b77a-192"><strong>GlDrawPixels</strong>函式會以 rgba 圖元 blue 元件的相同方式，將這個元件轉換成內部浮點格式，然後將它轉換成具有紅色和綠色設定為0.0 的 RGBA 圖元，然後將 Alpha 設定為1.0。</span><span class="sxs-lookup"><span data-stu-id="7b77a-192">The <strong>glDrawPixels</strong> function converts this component to the internal floating-point format in the same way that the blue component of an RGBA pixel is, and then converts it to an RGBA pixel with red and green set to 0.0, and alpha set to 1.0.</span></span> <span data-ttu-id="7b77a-193">進行這項轉換之後，圖元的處理方式就像是將它當成 RGBA 圖元讀取一樣。</span><span class="sxs-lookup"><span data-stu-id="7b77a-193">After this conversion, the pixel is treated just as if it had been read as an RGBA pixel.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="GL_ALPHA"></span><span id="gl_alpha"></span><dl> <span data-ttu-id="7b77a-194"><dt><strong>GL_ALPHA</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="7b77a-194"><dt><strong>GL_ALPHA</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="7b77a-195">每個圖元都是單一 Alpha 元件。</span><span class="sxs-lookup"><span data-stu-id="7b77a-195">Each pixel is a single alpha component.</span></span><br/> <span data-ttu-id="7b77a-196"><strong>GlDrawPixels</strong>函式會以 RGBA 圖元 Alpha 元件的相同方式，將這個元件轉換成內部浮點格式，然後再將它轉換為紅色、綠色和藍色設定為0.0 的 RGBA 圖元。</span><span class="sxs-lookup"><span data-stu-id="7b77a-196">The <strong>glDrawPixels</strong> function converts this component to the internal floating-point format in the same way that the alpha component of an RGBA pixel is, and then converts it to an RGBA pixel with red, green, and blue set to 0.0.</span></span> <span data-ttu-id="7b77a-197">進行這項轉換之後，圖元的處理方式就像是將它當成 RGBA 圖元讀取一樣。</span><span class="sxs-lookup"><span data-stu-id="7b77a-197">After this conversion, the pixel is treated just as if it had been read as an RGBA pixel.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="GL_RGB"></span><span id="gl_rgb"></span><dl> <span data-ttu-id="7b77a-198"><dt><strong>GL_RGB</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="7b77a-198"><dt><strong>GL_RGB</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="7b77a-199">每個圖元都是三個元件的群組，順序如下：紅色、綠色、藍色。</span><span class="sxs-lookup"><span data-stu-id="7b77a-199">Each pixel is a group of three components in this order: red, green, blue.</span></span> <span data-ttu-id="7b77a-200"><strong>GlDrawPixels</strong>函式會以 RGBA 圖元的 red、綠和 blue 元件相同的方式，將每個元件轉換成內部浮點格式。</span><span class="sxs-lookup"><span data-stu-id="7b77a-200">The <strong>glDrawPixels</strong> function converts each component to the internal floating-point format in the same way that the red, green, and blue components of an RGBA pixel are.</span></span> <span data-ttu-id="7b77a-201">色彩三重轉換成將 Alpha 設定為1.0 的 RGBA 圖元。</span><span class="sxs-lookup"><span data-stu-id="7b77a-201">The color triple is converted to an RGBA pixel with alpha set to 1.0.</span></span> <span data-ttu-id="7b77a-202">進行這項轉換之後，圖元的處理方式就像是將它當成 RGBA 圖元讀取一樣。</span><span class="sxs-lookup"><span data-stu-id="7b77a-202">After this conversion, the pixel is treated just as if it had been read as an RGBA pixel.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="GL_LUMINANCE"></span><span id="gl_luminance"></span><dl> <span data-ttu-id="7b77a-203"><dt><strong>GL_LUMINANCE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="7b77a-203"><dt><strong>GL_LUMINANCE</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="7b77a-204">每個圖元都是單一亮度元件。</span><span class="sxs-lookup"><span data-stu-id="7b77a-204">Each pixel is a single luminance component.</span></span><br/> <span data-ttu-id="7b77a-205"><strong>GlDrawPixels</strong>函式會以 RGBA 圖元的紅色元件相同的方式，將這個元件轉換成內部浮點格式，然後將它轉換成具有紅色、綠色和藍色的 rgba 圖元（設定為已轉換的亮度值），並將 Alpha 設定為1.0。</span><span class="sxs-lookup"><span data-stu-id="7b77a-205">The <strong>glDrawPixels</strong> function converts this component to the internal floating-point format in the same way that the red component of an RGBA pixel is, and then converts it to an RGBA pixel with red, green, and blue set to the converted luminance value, and alpha set to 1.0.</span></span> <span data-ttu-id="7b77a-206">進行這項轉換之後，圖元的處理方式就像是將它當成 RGBA 圖元讀取一樣。</span><span class="sxs-lookup"><span data-stu-id="7b77a-206">After this conversion, the pixel is treated just as if it had been read as an RGBA pixel.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="GL_LUMINANCE_ALPHA"></span><span id="gl_luminance_alpha"></span><dl> <span data-ttu-id="7b77a-207"><dt><strong>GL_LUMINANCE_ALPHA</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="7b77a-207"><dt><strong>GL_LUMINANCE_ALPHA</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="7b77a-208">每個圖元都是以下列順序組成的兩個元件群組：亮度、Alpha。</span><span class="sxs-lookup"><span data-stu-id="7b77a-208">Each pixel is a group of two components in this order: luminance, alpha.</span></span><br/> <span data-ttu-id="7b77a-209"><strong>GlDrawPixels</strong>函式會以 RGBA 圖元的紅色元件相同的方式，將兩個元件轉換成內部浮點格式，然後將它們轉換成具有紅色、綠色和藍色的 rgba 圖元（設定為轉換的亮度值），並將 Alpha 設定為轉換的 Alpha 值。</span><span class="sxs-lookup"><span data-stu-id="7b77a-209">The <strong>glDrawPixels</strong> function converts the two components to the internal floating-point format in the same way that the red component of an RGBA pixel is, and then converts them to an RGBA pixel with red, green, and blue set to the converted luminance value, and alpha set to the converted alpha value.</span></span> <span data-ttu-id="7b77a-210">進行這項轉換之後，圖元的處理方式就像是將它當成 RGBA 圖元讀取一樣。</span><span class="sxs-lookup"><span data-stu-id="7b77a-210">After this conversion, the pixel is treated just as if it had been read as an RGBA pixel.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="GL_BGR_EXT"></span><span id="gl_bgr_ext"></span><dl> <span data-ttu-id="7b77a-211"><dt><strong>GL_BGR_EXT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="7b77a-211"><dt><strong>GL_BGR_EXT</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="7b77a-212">每個圖元都是三個元件的群組，順序如下：藍色、綠色、紅色。</span><span class="sxs-lookup"><span data-stu-id="7b77a-212">Each pixel is a group of three components in this order: blue, green, red.</span></span><br/> <span data-ttu-id="7b77a-213">GL_BGR_EXT 提供的格式符合 Windows 裝置獨立點陣圖 (Dib) 的記憶體配置。</span><span class="sxs-lookup"><span data-stu-id="7b77a-213">GL_BGR_EXT provides a format that matches the memory layout of Windows device-independent bitmaps (DIBs).</span></span> <span data-ttu-id="7b77a-214">因此，您的應用程式可以使用 Windows 函式呼叫和 OpenGL 圖元函式呼叫的相同資料。</span><span class="sxs-lookup"><span data-stu-id="7b77a-214">Thus, your applications can use the same data with Windows function calls and OpenGL pixel function calls.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="GL_BGRA_EXT"></span><span id="gl_bgra_ext"></span><dl> <span data-ttu-id="7b77a-215"><dt><strong>GL_BGRA_EXT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="7b77a-215"><dt><strong>GL_BGRA_EXT</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="7b77a-216">每個圖元都是四個元件的群組，順序如下： blue、綠、red、Alpha。</span><span class="sxs-lookup"><span data-stu-id="7b77a-216">Each pixel is a group of four components in this order: blue, green, red, alpha.</span></span><br/> <span data-ttu-id="7b77a-217">GL_BGRA_EXT 提供的格式符合 Windows 裝置獨立點陣圖 (Dib) 的記憶體配置。</span><span class="sxs-lookup"><span data-stu-id="7b77a-217">GL_BGRA_EXT provides a format that matches the memory layout of Windows device-independent bitmaps (DIBs).</span></span> <span data-ttu-id="7b77a-218">因此，您的應用程式可以使用 Windows 函式呼叫和 OpenGL 圖元函式呼叫的相同資料。</span><span class="sxs-lookup"><span data-stu-id="7b77a-218">Thus, your applications can use the same data with Windows function calls and OpenGL pixel function calls.</span></span><br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="7b77a-219">*type*</span><span class="sxs-lookup"><span data-stu-id="7b77a-219">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="7b77a-220">*圖元* 的資料類型。</span><span class="sxs-lookup"><span data-stu-id="7b77a-220">The data type for *pixels*.</span></span> <span data-ttu-id="7b77a-221">以下是接受的符號常數及其意義。</span><span class="sxs-lookup"><span data-stu-id="7b77a-221">The following are the accepted symbolic constants and their meanings.</span></span>



| <span data-ttu-id="7b77a-222">值</span><span class="sxs-lookup"><span data-stu-id="7b77a-222">Value</span></span>                                                                                                                                                                      | <span data-ttu-id="7b77a-223">意義</span><span class="sxs-lookup"><span data-stu-id="7b77a-223">Meaning</span></span>                                           |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| <span id="GL_UNSIGNED_BYTE"></span><span id="gl_unsigned_byte"></span><dl> <span data-ttu-id="7b77a-224"><dt>**GL 不 \_ 帶正負號的 \_ 位元組**</dt></span><span class="sxs-lookup"><span data-stu-id="7b77a-224"><dt>**GL\_UNSIGNED\_BYTE**</dt></span></span> </dl>    | <span data-ttu-id="7b77a-225">不帶正負號的 8 位元整數</span><span class="sxs-lookup"><span data-stu-id="7b77a-225">Unsigned 8-bit integer</span></span><br/>                 |
| <span id="GL_BYTE"></span><span id="gl_byte"></span><dl> <span data-ttu-id="7b77a-226"><dt>**GL \_ 位元組**</dt></span><span class="sxs-lookup"><span data-stu-id="7b77a-226"><dt>**GL\_BYTE**</dt></span></span> </dl>                                | <span data-ttu-id="7b77a-227">帶正負號的 8 位元整數</span><span class="sxs-lookup"><span data-stu-id="7b77a-227">Signed 8-bit integer</span></span><br/>                   |
| <span id="GL_BITMAP"></span><span id="gl_bitmap"></span><dl> <span data-ttu-id="7b77a-228"><dt>**GL \_ 點陣圖**</dt></span><span class="sxs-lookup"><span data-stu-id="7b77a-228"><dt>**GL\_BITMAP**</dt></span></span> </dl>                          | <span data-ttu-id="7b77a-229">不帶正負號的8位整數中的單一位</span><span class="sxs-lookup"><span data-stu-id="7b77a-229">Single bits in unsigned 8-bit integers</span></span><br/> |
| <span id="GL_UNSIGNED_SHORT"></span><span id="gl_unsigned_short"></span><dl> <span data-ttu-id="7b77a-230"><dt>**GL 不 \_ 帶正負號 \_ 簡短**</dt></span><span class="sxs-lookup"><span data-stu-id="7b77a-230"><dt>**GL\_UNSIGNED\_SHORT**</dt></span></span> </dl> | <span data-ttu-id="7b77a-231">不帶正負號的 16 位元整數</span><span class="sxs-lookup"><span data-stu-id="7b77a-231">Unsigned 16-bit integer</span></span><br/>                |
| <span id="GL_SHORT"></span><span id="gl_short"></span><dl> <span data-ttu-id="7b77a-232"><dt>**GL \_ 短期**</dt></span><span class="sxs-lookup"><span data-stu-id="7b77a-232"><dt>**GL\_SHORT**</dt></span></span> </dl>                             | <span data-ttu-id="7b77a-233">帶正負號的 16 位元整數</span><span class="sxs-lookup"><span data-stu-id="7b77a-233">Signed 16-bit integer</span></span><br/>                  |
| <span id="GL_UNSIGNED_INT"></span><span id="gl_unsigned_int"></span><dl> <span data-ttu-id="7b77a-234"><dt>**GL 不 \_ 帶正負號 \_ INT**</dt></span><span class="sxs-lookup"><span data-stu-id="7b77a-234"><dt>**GL\_UNSIGNED\_INT**</dt></span></span> </dl>       | <span data-ttu-id="7b77a-235">不帶正負號的 32 位元整數</span><span class="sxs-lookup"><span data-stu-id="7b77a-235">Unsigned 32-bit integer</span></span><br/>                |
| <span id="GL_INT"></span><span id="gl_int"></span><dl> <span data-ttu-id="7b77a-236"><dt>**GL \_ INT**</dt></span><span class="sxs-lookup"><span data-stu-id="7b77a-236"><dt>**GL\_INT**</dt></span></span> </dl>                                   | <span data-ttu-id="7b77a-237">32 位元整數</span><span class="sxs-lookup"><span data-stu-id="7b77a-237">32-bit integer</span></span><br/>                         |
| <span id="GL_FLOAT"></span><span id="gl_float"></span><dl> <span data-ttu-id="7b77a-238"><dt>**GL \_ FLOAT**</dt></span><span class="sxs-lookup"><span data-stu-id="7b77a-238"><dt>**GL\_FLOAT**</dt></span></span> </dl>                             | <span data-ttu-id="7b77a-239">單精確度浮點數</span><span class="sxs-lookup"><span data-stu-id="7b77a-239">Single-precision floating-point</span></span><br/>        |



 

</dd> <dt>

<span data-ttu-id="7b77a-240">*圖元*</span><span class="sxs-lookup"><span data-stu-id="7b77a-240">*pixels*</span></span> 
</dt> <dd>

<span data-ttu-id="7b77a-241">圖元資料的指標。</span><span class="sxs-lookup"><span data-stu-id="7b77a-241">A pointer to the pixel data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b77a-242">傳回值</span><span class="sxs-lookup"><span data-stu-id="7b77a-242">Return value</span></span>

<span data-ttu-id="7b77a-243">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="7b77a-243">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="7b77a-244">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="7b77a-244">Error codes</span></span>

<span data-ttu-id="7b77a-245">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="7b77a-245">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="7b77a-246">Name</span><span class="sxs-lookup"><span data-stu-id="7b77a-246">Name</span></span>                                                                                                  | <span data-ttu-id="7b77a-247">意義</span><span class="sxs-lookup"><span data-stu-id="7b77a-247">Meaning</span></span>                                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7b77a-248"><dt>**GL \_ 無效 \_ 值**</dt></span><span class="sxs-lookup"><span data-stu-id="7b77a-248"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="7b77a-249">*寬度* 或 *高度* 都是負數。</span><span class="sxs-lookup"><span data-stu-id="7b77a-249">Either *width* or *height* was negative.</span></span><br/>                                                                                                                                          |
| <dl> <span data-ttu-id="7b77a-250"><dt>**GL \_ 無效 \_ 列舉**</dt></span><span class="sxs-lookup"><span data-stu-id="7b77a-250"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="7b77a-251">*格式* 或 *類型* 都不是可接受的值。</span><span class="sxs-lookup"><span data-stu-id="7b77a-251">Either *format* or *type* was not an accepted value.</span></span> <br/>                                                                                                                             |
| <dl> <span data-ttu-id="7b77a-252"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="7b77a-252"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="7b77a-253">*格式* 為 GL \_ RED、GL \_ 綠、gl \_ BLUE、gl \_ ALPHA、GL \_ RGB、GL \_ RGBA、GL \_ BGR \_ EXT、gl \_ BGRA \_ EXT、gl \_ 亮度或 gl \_ 亮度 \_ ALPHA，且 OpenGL 處於色彩索引模式。</span><span class="sxs-lookup"><span data-stu-id="7b77a-253">*format* was GL\_RED, GL\_GREEN, GL\_BLUE, GL\_ALPHA, GL\_RGB, GL\_RGBA, GL\_BGR\_EXT, GL\_BGRA\_EXT, GL\_LUMINANCE, or GL\_LUMINANCE\_ALPHA, and OpenGL was in color-index mode.</span></span><br/> |
| <dl> <span data-ttu-id="7b77a-254"><dt>**GL \_ 無效 \_ 列舉**</dt></span><span class="sxs-lookup"><span data-stu-id="7b77a-254"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="7b77a-255">*類型* 為 gl \_ 點陣圖， *格式* 不是 gl \_ 色彩 \_ 索引或 gl 樣板 \_ \_ 索引。</span><span class="sxs-lookup"><span data-stu-id="7b77a-255">*type* was GL\_BITMAP and *format* was not either GL\_COLOR\_INDEX or GL\_STENCIL\_INDEX.</span></span><br/>                                                                                         |
| <dl> <span data-ttu-id="7b77a-256"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="7b77a-256"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="7b77a-257">*格式* 為 GL 樣板索引，但沒有樣板 \_ \_ 緩衝區。</span><span class="sxs-lookup"><span data-stu-id="7b77a-257">*format* was GL\_STENCIL\_INDEX and there was no stencil buffer.</span></span><br/>                                                                                                                  |
| <dl> <span data-ttu-id="7b77a-258"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="7b77a-258"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="7b77a-259">呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。</span><span class="sxs-lookup"><span data-stu-id="7b77a-259">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/>                                                        |


## <a name="remarks"></a><span data-ttu-id="7b77a-260">備註</span><span class="sxs-lookup"><span data-stu-id="7b77a-260">Remarks</span></span>

<span data-ttu-id="7b77a-261">**GlDrawPixels** 函式會從記憶體讀取圖元資料，並將其寫入相對於目前點陣位置的畫面格緩衝區。</span><span class="sxs-lookup"><span data-stu-id="7b77a-261">The **glDrawPixels** function reads pixel data from memory and writes it into the framebuffer relative to the current raster position.</span></span> <span data-ttu-id="7b77a-262">使用 [**glRasterPos**](glrasterpos-functions.md) 來設定目前的點陣位置，並使用 [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) 搭配引數 GL \_ 目前的 \_ 點陣 \_ 位置來查詢點陣位置。</span><span class="sxs-lookup"><span data-stu-id="7b77a-262">Use [**glRasterPos**](glrasterpos-functions.md) to set the current raster position, and use [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_RASTER\_POSITION to query the raster position.</span></span>

<span data-ttu-id="7b77a-263">有幾個參數會定義記憶體中圖元資料的編碼，並控制圖元資料在放置於畫面格緩衝區之前的處理。</span><span class="sxs-lookup"><span data-stu-id="7b77a-263">Several parameters define the encoding of pixel data in memory and control the processing of the pixel data before it is placed in the framebuffer.</span></span> <span data-ttu-id="7b77a-264">這些參數設定有四個函數： [**glPixelStore**](glpixelstore-functions.md)、 [**glPixelTransfer**](glpixeltransfer.md)、 [**glPixelMap**](glpixelmap.md)和 [**glPixelZoom**](glpixelzoom.md)。</span><span class="sxs-lookup"><span data-stu-id="7b77a-264">These parameters are set with four functions: [**glPixelStore**](glpixelstore-functions.md), [**glPixelTransfer**](glpixeltransfer.md), [**glPixelMap**](glpixelmap.md), and [**glPixelZoom**](glpixelzoom.md).</span></span> <span data-ttu-id="7b77a-265">本主題說明 **glDrawPixels** 這四個函式所指定之許多（但不是全部）參數的影響。</span><span class="sxs-lookup"><span data-stu-id="7b77a-265">This topic describes the effects on **glDrawPixels** of many, but not all, of the parameters specified by these four functions.</span></span>

<span data-ttu-id="7b77a-266">資料是從 *圖元* 讀取為帶正負號或不帶正負號的位元組序列、帶正負號或不帶正負號的短整數、帶正負號或不帶正負號的整數，或是單精確度浮點值（視 *類型* 而定）。</span><span class="sxs-lookup"><span data-stu-id="7b77a-266">Data is read from *pixels* as a sequence of signed or unsigned bytes, signed or unsigned shorts, signed or unsigned integers, or single-precision floating-point values, depending on *type*.</span></span> <span data-ttu-id="7b77a-267">這些位元組、短、整數或浮點數值都會被視為一個色彩或深度元件，或一個索引（視 *格式* 而定）。</span><span class="sxs-lookup"><span data-stu-id="7b77a-267">Each of these bytes, shorts, integers, or floating-point values is interpreted as one color or depth component, or one index, depending on *format*.</span></span> <span data-ttu-id="7b77a-268">索引一律會個別處理。</span><span class="sxs-lookup"><span data-stu-id="7b77a-268">Indexes are always treated individually.</span></span> <span data-ttu-id="7b77a-269">色彩元件會根據 *格式*，再次視為一、二、三或四個值的群組。</span><span class="sxs-lookup"><span data-stu-id="7b77a-269">Color components are treated as groups of one, two, three, or four values, again based on *format*.</span></span> <span data-ttu-id="7b77a-270">個別的索引和元件群組都稱為圖元。</span><span class="sxs-lookup"><span data-stu-id="7b77a-270">Both individual indexes and groups of components are referred to as pixels.</span></span> <span data-ttu-id="7b77a-271">如果 *type* 是 gl \_ BITMAP，則資料必須為不帶正負號的位元組，且 *格式* 必須是 gl \_ 色彩 \_ 索引或 gl 樣板 \_ \_ 索引。</span><span class="sxs-lookup"><span data-stu-id="7b77a-271">If *type* is GL\_BITMAP, the data must be unsigned bytes, and *format* must be either GL\_COLOR\_INDEX or GL\_STENCIL\_INDEX.</span></span> <span data-ttu-id="7b77a-272">每個不帶正負號的位元組都會被視為 8 1 位圖元，而依 GL 解壓縮 LSB 的位排序會 \_ \_ \_ 先 (請參閱 [**glPixelStore**](glpixelstore-functions.md)) 。</span><span class="sxs-lookup"><span data-stu-id="7b77a-272">Each unsigned byte is treated as eight 1-bit pixels, with bit ordering determined by GL\_UNPACK\_LSB\_FIRST (see [**glPixelStore**](glpixelstore-functions.md)).</span></span>

<span data-ttu-id="7b77a-273">*寬度*（依 *高度* 圖元）會從記憶體讀取，從位置 *圖元* 開始。</span><span class="sxs-lookup"><span data-stu-id="7b77a-273">The *width* by *height* pixels are read from memory, starting at location *pixels*.</span></span> <span data-ttu-id="7b77a-274">根據預設，這些圖元取自連續的記憶體位置，但在讀取所有 *寬度* 的圖元之後，讀取指標會前進到下一個4位元組的界限。</span><span class="sxs-lookup"><span data-stu-id="7b77a-274">By default, these pixels are taken from adjacent memory locations, except that after all *width* pixels are read, the read pointer is advanced to the next 4-byte boundary.</span></span> <span data-ttu-id="7b77a-275">**GlPixelStore** 函式會指定與引數 GL 解除封裝對齊的4位元組資料列對齊 \_ \_ ，而且您可以將它設定為1、2、4或8個位元組。</span><span class="sxs-lookup"><span data-stu-id="7b77a-275">The **glPixelStore** function specifies the 4-byte row alignment with argument GL\_UNPACK\_ALIGNMENT, and you can set it to 1, 2, 4, or 8 bytes.</span></span> <span data-ttu-id="7b77a-276">其他圖元存放區參數會在讀取第一個圖元之前，以及讀取所有 *寬度* 圖元之後，指定不同的讀取指標的進展。</span><span class="sxs-lookup"><span data-stu-id="7b77a-276">Other pixel store parameters specify different read pointer advancements, both before the first pixel is read, and after all *width* pixels are read.</span></span> <span data-ttu-id="7b77a-277">**GlPixelStore** 函式會根據 [**glPixelTransfer**](glpixeltransfer.md)和 [**glPixelMap**](glpixelmap.md)所指定數個參數的值，以相同的方式在每個 *高度寬度* 的圖元上運作。</span><span class="sxs-lookup"><span data-stu-id="7b77a-277">The **glPixelStore** function operates on each of the *width-by-height* pixels that it reads from memory in the same way, based on the values of several parameters specified by [**glPixelTransfer**](glpixeltransfer.md) and [**glPixelMap**](glpixelmap.md).</span></span> <span data-ttu-id="7b77a-278">這些作業的詳細資料，以及圖元繪製所在的目標緩衝區，是依 *格式* 指定的像素格式所特有。</span><span class="sxs-lookup"><span data-stu-id="7b77a-278">The details of these operations, as well as the target buffer into which the pixels are drawn, are specific to the format of the pixels, as specified by *format*.</span></span>

<span data-ttu-id="7b77a-279">目前為止所描述的點陣化會假設圖元縮放因數為1.0。</span><span class="sxs-lookup"><span data-stu-id="7b77a-279">The rasterization described thus far assumes pixel zoom factors of 1.0.</span></span> <span data-ttu-id="7b77a-280">如果您使用 [**glPixelZoom**](glpixelzoom.md) 來變更 *x* 和 *y* 圖元縮放因數，圖元會轉換成片段，如下所示。</span><span class="sxs-lookup"><span data-stu-id="7b77a-280">If you use [**glPixelZoom**](glpixelzoom.md) to change the *x* and *y* pixel zoom factors, pixels are converted to fragments as follows.</span></span> <span data-ttu-id="7b77a-281">如果 (*xr，年*) 是目前的點陣位置，而指定的圖元是在第 *n* 個數據行和第 *m* 個圖元的資料列中，則會為其中心位於矩形中，有邊角的圖元產生片段</span><span class="sxs-lookup"><span data-stu-id="7b77a-281">If (*xr,yr*) is the current raster position, and a given pixel is in the *n* th column and *m* th row of the pixel rectangle, then fragments are generated for pixels whose centers are in the rectangle with corners at</span></span>

<span data-ttu-id="7b77a-282"> (*x*<sub>r</sub>  +  *縮放比例*？*n*、 *y*<sub>r</sub>  +  *縮放*<sub>y</sub> *m*) </span><span class="sxs-lookup"><span data-stu-id="7b77a-282">(*x*<sub>r</sub> + *zoom*? *n*, *y*<sub>r</sub> + *zoom*<sub>y</sub> *m*)</span></span>

<span data-ttu-id="7b77a-283"> (*x*<sub>r</sub>  +  *縮放比例*？</span><span class="sxs-lookup"><span data-stu-id="7b77a-283">(*x*<sub>r</sub> + *zoom*?</span></span> <span data-ttu-id="7b77a-284"> (*n* + 1) ， *y*<sub>r</sub>  +  *縮放*<sub>y</sub> (*m* + 1) ) </span><span class="sxs-lookup"><span data-stu-id="7b77a-284">(*n* + 1), *y*<sub>r</sub> + *zoom*<sub>y</sub> (*m* + 1))</span></span>

<span data-ttu-id="7b77a-285">哪裡 *縮放*？是 gl zoom \_ \_ X 和 *ZOOM*<sub>y</sub> 的值是 gl zoom y 的值 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="7b77a-285">where *zoom*? is the value of GL\_ZOOM\_X and *zoom*<sub>y</sub> is the value of GL\_ZOOM\_Y.</span></span>

<span data-ttu-id="7b77a-286">下列函式會取出與 **glDrawPixels** 相關的資訊：</span><span class="sxs-lookup"><span data-stu-id="7b77a-286">The following functions retrieve information related to **glDrawPixels**:</span></span>

<span data-ttu-id="7b77a-287">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 目前 \_ 點陣 \_ 位置的 glGet</span><span class="sxs-lookup"><span data-stu-id="7b77a-287">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_RASTER\_POSITION</span></span>

<span data-ttu-id="7b77a-288">具有引數 GL \_ 目前 \_ 點陣 \_ 位置 \_ 有效的 glGet</span><span class="sxs-lookup"><span data-stu-id="7b77a-288">**glGet** with argument GL\_CURRENT\_RASTER\_POSITION\_VALID</span></span>

## <a name="requirements"></a><span data-ttu-id="7b77a-289">規格需求</span><span class="sxs-lookup"><span data-stu-id="7b77a-289">Requirements</span></span>



| <span data-ttu-id="7b77a-290">需求</span><span class="sxs-lookup"><span data-stu-id="7b77a-290">Requirement</span></span> | <span data-ttu-id="7b77a-291">值</span><span class="sxs-lookup"><span data-stu-id="7b77a-291">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7b77a-292">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7b77a-292">Minimum supported client</span></span><br/> | <span data-ttu-id="7b77a-293">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7b77a-293">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="7b77a-294">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7b77a-294">Minimum supported server</span></span><br/> | <span data-ttu-id="7b77a-295">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7b77a-295">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7b77a-296">標頭</span><span class="sxs-lookup"><span data-stu-id="7b77a-296">Header</span></span><br/>                   | <dl> <span data-ttu-id="7b77a-297"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="7b77a-297"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="7b77a-298">程式庫</span><span class="sxs-lookup"><span data-stu-id="7b77a-298">Library</span></span><br/>                  | <dl> <span data-ttu-id="7b77a-299"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="7b77a-299"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="7b77a-300">DLL</span><span class="sxs-lookup"><span data-stu-id="7b77a-300">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7b77a-301"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7b77a-301"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b77a-302">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7b77a-302">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b77a-303">**glAlphaFunc**</span><span class="sxs-lookup"><span data-stu-id="7b77a-303">**glAlphaFunc**</span></span>](glalphafunc.md)
</dt> <dt>

[<span data-ttu-id="7b77a-304">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="7b77a-304">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="7b77a-305">**glBlendFunc**</span><span class="sxs-lookup"><span data-stu-id="7b77a-305">**glBlendFunc**</span></span>](glblendfunc.md)
</dt> <dt>

[<span data-ttu-id="7b77a-306">**glCopyPixels**</span><span class="sxs-lookup"><span data-stu-id="7b77a-306">**glCopyPixels**</span></span>](glcopypixels.md)
</dt> <dt>

[<span data-ttu-id="7b77a-307">**glDepthFunc**</span><span class="sxs-lookup"><span data-stu-id="7b77a-307">**glDepthFunc**</span></span>](gldepthfunc.md)
</dt> <dt>

[<span data-ttu-id="7b77a-308">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="7b77a-308">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="7b77a-309">**glGet**</span><span class="sxs-lookup"><span data-stu-id="7b77a-309">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="7b77a-310">**glLogicOp**</span><span class="sxs-lookup"><span data-stu-id="7b77a-310">**glLogicOp**</span></span>](gllogicop.md)
</dt> <dt>

[<span data-ttu-id="7b77a-311">**glPixelMap**</span><span class="sxs-lookup"><span data-stu-id="7b77a-311">**glPixelMap**</span></span>](glpixelmap.md)
</dt> <dt>

[<span data-ttu-id="7b77a-312">**glPixelStore**</span><span class="sxs-lookup"><span data-stu-id="7b77a-312">**glPixelStore**</span></span>](glpixelstore-functions.md)
</dt> <dt>

[<span data-ttu-id="7b77a-313">**glPixelTransfer**</span><span class="sxs-lookup"><span data-stu-id="7b77a-313">**glPixelTransfer**</span></span>](glpixeltransfer.md)
</dt> <dt>

[<span data-ttu-id="7b77a-314">**glPixelZoom**</span><span class="sxs-lookup"><span data-stu-id="7b77a-314">**glPixelZoom**</span></span>](glpixelzoom.md)
</dt> <dt>

[<span data-ttu-id="7b77a-315">**glRasterPos**</span><span class="sxs-lookup"><span data-stu-id="7b77a-315">**glRasterPos**</span></span>](glrasterpos-functions.md)
</dt> <dt>

[<span data-ttu-id="7b77a-316">**glReadPixels**</span><span class="sxs-lookup"><span data-stu-id="7b77a-316">**glReadPixels**</span></span>](glreadpixels.md)
</dt> <dt>

[<span data-ttu-id="7b77a-317">**glScissor**</span><span class="sxs-lookup"><span data-stu-id="7b77a-317">**glScissor**</span></span>](glscissor.md)
</dt> <dt>

[<span data-ttu-id="7b77a-318">**glStencilFunc**</span><span class="sxs-lookup"><span data-stu-id="7b77a-318">**glStencilFunc**</span></span>](glstencilfunc.md)
</dt> </dl>

 

 





