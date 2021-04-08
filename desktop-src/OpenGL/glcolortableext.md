---
title: 'glColorTableEXT 函式 (Gl) '
description: GlColorTableEXT 函式會指定適用于目標調色板材質之調色板的格式和大小。
ms.assetid: f3d7b1a1-97a5-47ef-a0ca-5e58acb86bb4
keywords:
- glColorTableEXT 函式 OpenGL
topic_type:
- apiref
api_name:
- glColorTableEXT
api_location:
- Gl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd0d5fd5c848e787f480e3e1893b9b25e4bbd3de
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686085"
---
# <a name="glcolortableext-function"></a><span data-ttu-id="c85fd-104">glColorTableEXT 函式</span><span class="sxs-lookup"><span data-stu-id="c85fd-104">glColorTableEXT function</span></span>

<span data-ttu-id="c85fd-105">**GlColorTableEXT** 函式會指定適用于目標調色板材質之調色板的格式和大小。</span><span class="sxs-lookup"><span data-stu-id="c85fd-105">The **glColorTableEXT** function specifies the format and size of a palette for targeted paletted textures.</span></span>

## <a name="syntax"></a><span data-ttu-id="c85fd-106">語法</span><span class="sxs-lookup"><span data-stu-id="c85fd-106">Syntax</span></span>


```C++
void WINAPI glColorTableEXT(
         GLenum  target,
         GLenum  internalFormat,
         GLsizei width,
         GLenum  format,
         GLenum  type,
   const GLvoid  *data
);
```



## <a name="parameters"></a><span data-ttu-id="c85fd-107">參數</span><span class="sxs-lookup"><span data-stu-id="c85fd-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c85fd-108">*目標*</span><span class="sxs-lookup"><span data-stu-id="c85fd-108">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="c85fd-109">要變更其調色板的目標材質。</span><span class="sxs-lookup"><span data-stu-id="c85fd-109">The target texture that is to have its palette changed.</span></span> <span data-ttu-id="c85fd-110">必須是材質 \_ 1d、材質 \_ 2D、proxy \_ 材質 \_ 1d 或 proxy \_ 材質 \_ 2d。</span><span class="sxs-lookup"><span data-stu-id="c85fd-110">Must be TEXTURE\_1D, TEXTURE\_2D, PROXY\_TEXTURE\_1D, or PROXY\_TEXTURE\_2D.</span></span>

</dd> <dt>

<span data-ttu-id="c85fd-111">*internalFormat*</span><span class="sxs-lookup"><span data-stu-id="c85fd-111">*internalFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="c85fd-112">調色板的內部格式和解析度。</span><span class="sxs-lookup"><span data-stu-id="c85fd-112">The internal format and resolution of the palette.</span></span> <span data-ttu-id="c85fd-113">這個參數可以採用下列其中一個符號值。</span><span class="sxs-lookup"><span data-stu-id="c85fd-113">This parameter can assume one of the following symbolic values.</span></span>



| <span data-ttu-id="c85fd-114">常數</span><span class="sxs-lookup"><span data-stu-id="c85fd-114">Constant</span></span>       | <span data-ttu-id="c85fd-115">基底格式</span><span class="sxs-lookup"><span data-stu-id="c85fd-115">Base Format</span></span> | <span data-ttu-id="c85fd-116">R 位</span><span class="sxs-lookup"><span data-stu-id="c85fd-116">R Bits</span></span> | <span data-ttu-id="c85fd-117">G 位</span><span class="sxs-lookup"><span data-stu-id="c85fd-117">G Bits</span></span> | <span data-ttu-id="c85fd-118">B 位</span><span class="sxs-lookup"><span data-stu-id="c85fd-118">B Bits</span></span> | <span data-ttu-id="c85fd-119">位</span><span class="sxs-lookup"><span data-stu-id="c85fd-119">A Bits</span></span> |
|----------------|-------------|--------|--------|--------|--------|
| <span data-ttu-id="c85fd-120">GL \_ R3 \_ G3 \_ B2</span><span class="sxs-lookup"><span data-stu-id="c85fd-120">GL\_R3\_G3\_B2</span></span> | <span data-ttu-id="c85fd-121">GL \_ RGB</span><span class="sxs-lookup"><span data-stu-id="c85fd-121">GL\_RGB</span></span>     | <span data-ttu-id="c85fd-122">3</span><span class="sxs-lookup"><span data-stu-id="c85fd-122">3</span></span>      | <span data-ttu-id="c85fd-123">3</span><span class="sxs-lookup"><span data-stu-id="c85fd-123">3</span></span>      | <span data-ttu-id="c85fd-124">2</span><span class="sxs-lookup"><span data-stu-id="c85fd-124">2</span></span>      |        |
| <span data-ttu-id="c85fd-125">GL \_ RGB4</span><span class="sxs-lookup"><span data-stu-id="c85fd-125">GL\_RGB4</span></span>       | <span data-ttu-id="c85fd-126">GL \_ RGB</span><span class="sxs-lookup"><span data-stu-id="c85fd-126">GL\_RGB</span></span>     | <span data-ttu-id="c85fd-127">4</span><span class="sxs-lookup"><span data-stu-id="c85fd-127">4</span></span>      | <span data-ttu-id="c85fd-128">4</span><span class="sxs-lookup"><span data-stu-id="c85fd-128">4</span></span>      | <span data-ttu-id="c85fd-129">4</span><span class="sxs-lookup"><span data-stu-id="c85fd-129">4</span></span>      |        |
| <span data-ttu-id="c85fd-130">GL \_ RGB5</span><span class="sxs-lookup"><span data-stu-id="c85fd-130">GL\_RGB5</span></span>       | <span data-ttu-id="c85fd-131">GL \_ RGB</span><span class="sxs-lookup"><span data-stu-id="c85fd-131">GL\_RGB</span></span>     | <span data-ttu-id="c85fd-132">5</span><span class="sxs-lookup"><span data-stu-id="c85fd-132">5</span></span>      | <span data-ttu-id="c85fd-133">5</span><span class="sxs-lookup"><span data-stu-id="c85fd-133">5</span></span>      | <span data-ttu-id="c85fd-134">5</span><span class="sxs-lookup"><span data-stu-id="c85fd-134">5</span></span>      |        |
| <span data-ttu-id="c85fd-135">GL \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="c85fd-135">GL\_RGB8</span></span>       | <span data-ttu-id="c85fd-136">GL \_ RGB</span><span class="sxs-lookup"><span data-stu-id="c85fd-136">GL\_RGB</span></span>     | <span data-ttu-id="c85fd-137">8</span><span class="sxs-lookup"><span data-stu-id="c85fd-137">8</span></span>      | <span data-ttu-id="c85fd-138">8</span><span class="sxs-lookup"><span data-stu-id="c85fd-138">8</span></span>      | <span data-ttu-id="c85fd-139">8</span><span class="sxs-lookup"><span data-stu-id="c85fd-139">8</span></span>      |        |
| <span data-ttu-id="c85fd-140">GL \_ RGB10</span><span class="sxs-lookup"><span data-stu-id="c85fd-140">GL\_RGB10</span></span>      | <span data-ttu-id="c85fd-141">GL \_ RGB</span><span class="sxs-lookup"><span data-stu-id="c85fd-141">GL\_RGB</span></span>     | <span data-ttu-id="c85fd-142">10</span><span class="sxs-lookup"><span data-stu-id="c85fd-142">10</span></span>     | <span data-ttu-id="c85fd-143">10</span><span class="sxs-lookup"><span data-stu-id="c85fd-143">10</span></span>     | <span data-ttu-id="c85fd-144">10</span><span class="sxs-lookup"><span data-stu-id="c85fd-144">10</span></span>     |        |
| <span data-ttu-id="c85fd-145">GL \_ RGB12</span><span class="sxs-lookup"><span data-stu-id="c85fd-145">GL\_RGB12</span></span>      | <span data-ttu-id="c85fd-146">GL \_ RGB</span><span class="sxs-lookup"><span data-stu-id="c85fd-146">GL\_RGB</span></span>     | <span data-ttu-id="c85fd-147">12</span><span class="sxs-lookup"><span data-stu-id="c85fd-147">12</span></span>     | <span data-ttu-id="c85fd-148">12</span><span class="sxs-lookup"><span data-stu-id="c85fd-148">12</span></span>     | <span data-ttu-id="c85fd-149">12</span><span class="sxs-lookup"><span data-stu-id="c85fd-149">12</span></span>     |        |
| <span data-ttu-id="c85fd-150">GL \_ RGB16</span><span class="sxs-lookup"><span data-stu-id="c85fd-150">GL\_RGB16</span></span>      | <span data-ttu-id="c85fd-151">GL \_ RGB</span><span class="sxs-lookup"><span data-stu-id="c85fd-151">GL\_RGB</span></span>     | <span data-ttu-id="c85fd-152">16</span><span class="sxs-lookup"><span data-stu-id="c85fd-152">16</span></span>     | <span data-ttu-id="c85fd-153">16</span><span class="sxs-lookup"><span data-stu-id="c85fd-153">16</span></span>     | <span data-ttu-id="c85fd-154">16</span><span class="sxs-lookup"><span data-stu-id="c85fd-154">16</span></span>     |        |
| <span data-ttu-id="c85fd-155">GL \_ RGBA2</span><span class="sxs-lookup"><span data-stu-id="c85fd-155">GL\_RGBA2</span></span>      | <span data-ttu-id="c85fd-156">GL \_ RGBA</span><span class="sxs-lookup"><span data-stu-id="c85fd-156">GL\_RGBA</span></span>    | <span data-ttu-id="c85fd-157">2</span><span class="sxs-lookup"><span data-stu-id="c85fd-157">2</span></span>      | <span data-ttu-id="c85fd-158">2</span><span class="sxs-lookup"><span data-stu-id="c85fd-158">2</span></span>      | <span data-ttu-id="c85fd-159">2</span><span class="sxs-lookup"><span data-stu-id="c85fd-159">2</span></span>      | <span data-ttu-id="c85fd-160">2</span><span class="sxs-lookup"><span data-stu-id="c85fd-160">2</span></span>      |
| <span data-ttu-id="c85fd-161">GL \_ RGBA4</span><span class="sxs-lookup"><span data-stu-id="c85fd-161">GL\_RGBA4</span></span>      | <span data-ttu-id="c85fd-162">GL \_ RGBA</span><span class="sxs-lookup"><span data-stu-id="c85fd-162">GL\_RGBA</span></span>    | <span data-ttu-id="c85fd-163">4</span><span class="sxs-lookup"><span data-stu-id="c85fd-163">4</span></span>      | <span data-ttu-id="c85fd-164">4</span><span class="sxs-lookup"><span data-stu-id="c85fd-164">4</span></span>      | <span data-ttu-id="c85fd-165">4</span><span class="sxs-lookup"><span data-stu-id="c85fd-165">4</span></span>      | <span data-ttu-id="c85fd-166">4</span><span class="sxs-lookup"><span data-stu-id="c85fd-166">4</span></span>      |
| <span data-ttu-id="c85fd-167">GL \_ RGB5 \_ A1</span><span class="sxs-lookup"><span data-stu-id="c85fd-167">GL\_RGB5\_A1</span></span>   | <span data-ttu-id="c85fd-168">GL \_ RGBA</span><span class="sxs-lookup"><span data-stu-id="c85fd-168">GL\_RGBA</span></span>    | <span data-ttu-id="c85fd-169">5</span><span class="sxs-lookup"><span data-stu-id="c85fd-169">5</span></span>      | <span data-ttu-id="c85fd-170">5</span><span class="sxs-lookup"><span data-stu-id="c85fd-170">5</span></span>      | <span data-ttu-id="c85fd-171">5</span><span class="sxs-lookup"><span data-stu-id="c85fd-171">5</span></span>      | <span data-ttu-id="c85fd-172">1</span><span class="sxs-lookup"><span data-stu-id="c85fd-172">1</span></span>      |
| <span data-ttu-id="c85fd-173">GL \_ RGBA8</span><span class="sxs-lookup"><span data-stu-id="c85fd-173">GL\_RGBA8</span></span>      | <span data-ttu-id="c85fd-174">GL \_ RGBA</span><span class="sxs-lookup"><span data-stu-id="c85fd-174">GL\_RGBA</span></span>    | <span data-ttu-id="c85fd-175">8</span><span class="sxs-lookup"><span data-stu-id="c85fd-175">8</span></span>      | <span data-ttu-id="c85fd-176">8</span><span class="sxs-lookup"><span data-stu-id="c85fd-176">8</span></span>      | <span data-ttu-id="c85fd-177">8</span><span class="sxs-lookup"><span data-stu-id="c85fd-177">8</span></span>      | <span data-ttu-id="c85fd-178">8</span><span class="sxs-lookup"><span data-stu-id="c85fd-178">8</span></span>      |
| <span data-ttu-id="c85fd-179">GL \_ RG10 \_ A2</span><span class="sxs-lookup"><span data-stu-id="c85fd-179">GL\_RG10\_A2</span></span>   | <span data-ttu-id="c85fd-180">GL \_ RGBA</span><span class="sxs-lookup"><span data-stu-id="c85fd-180">GL\_RGBA</span></span>    | <span data-ttu-id="c85fd-181">10</span><span class="sxs-lookup"><span data-stu-id="c85fd-181">10</span></span>     | <span data-ttu-id="c85fd-182">10</span><span class="sxs-lookup"><span data-stu-id="c85fd-182">10</span></span>     | <span data-ttu-id="c85fd-183">10</span><span class="sxs-lookup"><span data-stu-id="c85fd-183">10</span></span>     | <span data-ttu-id="c85fd-184">2</span><span class="sxs-lookup"><span data-stu-id="c85fd-184">2</span></span>      |
| <span data-ttu-id="c85fd-185">GL \_ RGB12</span><span class="sxs-lookup"><span data-stu-id="c85fd-185">GL\_RGB12</span></span>      | <span data-ttu-id="c85fd-186">GL \_ RGBA</span><span class="sxs-lookup"><span data-stu-id="c85fd-186">GL\_RGBA</span></span>    | <span data-ttu-id="c85fd-187">12</span><span class="sxs-lookup"><span data-stu-id="c85fd-187">12</span></span>     | <span data-ttu-id="c85fd-188">12</span><span class="sxs-lookup"><span data-stu-id="c85fd-188">12</span></span>     | <span data-ttu-id="c85fd-189">12</span><span class="sxs-lookup"><span data-stu-id="c85fd-189">12</span></span>     | <span data-ttu-id="c85fd-190">12</span><span class="sxs-lookup"><span data-stu-id="c85fd-190">12</span></span>     |
| <span data-ttu-id="c85fd-191">GL \_ RGBA16</span><span class="sxs-lookup"><span data-stu-id="c85fd-191">GL\_RGBA16</span></span>     | <span data-ttu-id="c85fd-192">GL \_ RGBA</span><span class="sxs-lookup"><span data-stu-id="c85fd-192">GL\_RGBA</span></span>    | <span data-ttu-id="c85fd-193">16</span><span class="sxs-lookup"><span data-stu-id="c85fd-193">16</span></span>     | <span data-ttu-id="c85fd-194">16</span><span class="sxs-lookup"><span data-stu-id="c85fd-194">16</span></span>     | <span data-ttu-id="c85fd-195">16</span><span class="sxs-lookup"><span data-stu-id="c85fd-195">16</span></span>     | <span data-ttu-id="c85fd-196">16</span><span class="sxs-lookup"><span data-stu-id="c85fd-196">16</span></span>     |



 

</dd> <dt>

<span data-ttu-id="c85fd-197">*width* (寬度)</span><span class="sxs-lookup"><span data-stu-id="c85fd-197">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="c85fd-198">調色板的大小。</span><span class="sxs-lookup"><span data-stu-id="c85fd-198">The size of the palette.</span></span> <span data-ttu-id="c85fd-199">某些整數 *n* 必須是 2n = 1。</span><span class="sxs-lookup"><span data-stu-id="c85fd-199">Must be 2n = 1 for some integer *n*.</span></span>

</dd> <dt>

<span data-ttu-id="c85fd-200">*format*</span><span class="sxs-lookup"><span data-stu-id="c85fd-200">*format*</span></span> 
</dt> <dd>

<span data-ttu-id="c85fd-201">圖元資料的格式。</span><span class="sxs-lookup"><span data-stu-id="c85fd-201">The format of the pixel data.</span></span> <span data-ttu-id="c85fd-202">接受下列符號常數。</span><span class="sxs-lookup"><span data-stu-id="c85fd-202">The following symbolic constants are accepted.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c85fd-203">值</span><span class="sxs-lookup"><span data-stu-id="c85fd-203">Value</span></span></th>
<th><span data-ttu-id="c85fd-204">意義</span><span class="sxs-lookup"><span data-stu-id="c85fd-204">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="GL_RGBA"></span><span id="gl_rgba"></span><dl> <span data-ttu-id="c85fd-205"><dt><strong>GL_RGBA</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="c85fd-205"><dt><strong>GL_RGBA</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="c85fd-206">每個圖元都是四個元件的群組，順序如下：紅色、綠色、藍色、Alpha。</span><span class="sxs-lookup"><span data-stu-id="c85fd-206">Each pixel is a group of four components in this order: red, green, blue, alpha.</span></span> <span data-ttu-id="c85fd-207">RGBA 格式的決定方式如下：</span><span class="sxs-lookup"><span data-stu-id="c85fd-207">The RGBA format is determined in this way:</span></span> <br/>
<ol>
<li><span data-ttu-id="c85fd-208"><strong>GlColorTableEXT</strong>函式會將浮點值直接轉換成具有未指定精確度的內部格式。</span><span class="sxs-lookup"><span data-stu-id="c85fd-208">The <strong>glColorTableEXT</strong> function converts floating-point values directly to an internal format with unspecified precision.</span></span> <span data-ttu-id="c85fd-209">帶正負號的整數值會以線性方式對應至內部格式，如此一來，最正面的可表示整數值會對應至1.0，而最大的可表示整數值會對應至-1.0。</span><span class="sxs-lookup"><span data-stu-id="c85fd-209">Signed integer values are mapped linearly to the internal format such that the most positive representable integer value maps to 1.0, and the most negative representable integer value maps to -1.0.</span></span> <span data-ttu-id="c85fd-210">不帶正負號的整數資料的對應方式如下：最大整數值對應至1.0，而零對應至0.0。</span><span class="sxs-lookup"><span data-stu-id="c85fd-210">Unsigned integer data is mapped similarly: the largest integer value maps to 1.0, and zero maps to 0.0.</span></span></li>
<li><span data-ttu-id="c85fd-211"><strong>GlColorTableEXT</strong>函式會 GL_c_SCALE 將產生的色彩值相乘，並將其新增至 GL_c_BIAS，其中<em>c</em>是紅色、綠色、藍色和 ALPHA，適用于個別的色彩元件。</span><span class="sxs-lookup"><span data-stu-id="c85fd-211">The <strong>glColorTableEXT</strong> function multiplies the resulting color values by GL_c_SCALE and adds them to GL_c_BIAS, where <em>c</em> is RED, GREEN, BLUE, and ALPHA for the respective color components.</span></span> <span data-ttu-id="c85fd-212">結果會壓制到 [0，1] 範圍內。</span><span class="sxs-lookup"><span data-stu-id="c85fd-212">The results are clamped to the range [0,1].</span></span></li>
<li><span data-ttu-id="c85fd-213">如果 GL_MAP_COLOR 為 <strong>TRUE</strong>， <strong>glColorTableEXT</strong> 會依 GL_PIXEL_MAP_c_TO_c 查閱資料表的大小來調整每個色彩元件，然後以資料表在該資料表中參考的值取代該元件; <em>c</em> 分別為 R、G、B 或 A。</span><span class="sxs-lookup"><span data-stu-id="c85fd-213">If GL_MAP_COLOR is <strong>TRUE</strong>, <strong>glColorTableEXT</strong> scales each color component by the size of lookup table GL_PIXEL_MAP_c_TO_c, then replaces the component by the value that it references in that table; <em>c</em> is R, G, B, or A, respectively.</span></span></li>
<li><span data-ttu-id="c85fd-214"><strong>GlColorTableEXT</strong>函式會將目前的點陣位置<em>z</em>座標和材質座標附加至每個圖元，然後將<em>x</em>和<em>y</em>視窗座標指派給第<em>n</em>個片段（例如<em>x</em>），以將產生的 RGBA 色彩轉換成片段：</span><span class="sxs-lookup"><span data-stu-id="c85fd-214">The <strong>glColorTableEXT</strong> function converts the resulting RGBA colors to fragments by attaching the current raster position <em>z</em>-coordinate and texture coordinates to each pixel, then assigning <em>x</em> and <em>y</em> window coordinates to the <em>n</em>th fragment such that<em>x</em>?</span></span><span data-ttu-id="c85fd-215"> = <em>x</em><sub>r</sub> + <em>n</em> mod <em>寬度</em></span><span class="sxs-lookup"><span data-stu-id="c85fd-215"> = <em>x</em><sub>r</sub> + <em>n</em> mod <em>width</em></span></span><br/> <span data-ttu-id="c85fd-216"><em></em>Y？</span><span class="sxs-lookup"><span data-stu-id="c85fd-216"><em></em>y?</span></span><span data-ttu-id="c85fd-217"> = <em>y</em><sub>r</sub> +<em>n/寬度</em></span><span class="sxs-lookup"><span data-stu-id="c85fd-217"> = <em>y</em><sub>r</sub> +<em>n / width</em></span></span><br/> <span data-ttu-id="c85fd-218">其中 (<em>x</em><sub>r</sub> ， <em>y</em><sub>r</sub> ) 是目前的點陣位置。</span><span class="sxs-lookup"><span data-stu-id="c85fd-218">where (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) is the current raster position.</span></span><br/></li>
<li><span data-ttu-id="c85fd-219">然後，這些圖元片段的處理方式就像是將點、線條或多邊形所產生的片段一樣。</span><span class="sxs-lookup"><span data-stu-id="c85fd-219">These pixel fragments are then treated just like the fragments generated by rasterizing points, lines, or polygons.</span></span> <span data-ttu-id="c85fd-220"><strong>GlColorTableEXT</strong>函式會先套用材質對應、霧化和所有片段作業，然後再將片段寫入畫面格緩衝區。</span><span class="sxs-lookup"><span data-stu-id="c85fd-220">The <strong>glColorTableEXT</strong> function applies texture mapping, fog, and all the fragment operations before writing the fragments to the framebuffer.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span id="GL_RED"></span><span id="gl_red"></span><dl> <span data-ttu-id="c85fd-221"><dt><strong>GL_RED</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="c85fd-221"><dt><strong>GL_RED</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="c85fd-222">每個圖元都是單一的紅色元件。</span><span class="sxs-lookup"><span data-stu-id="c85fd-222">Each pixel is a single red component.</span></span><br/> <span data-ttu-id="c85fd-223"><strong>GlColorTableEXT</strong>函式會以 RGBA 圖元的紅色元件相同的方式，將這個元件轉換成內部格式，然後將其轉換為具有綠色和藍色的 rgba 圖元（設為0.0），並將 Alpha 設定為1.0。</span><span class="sxs-lookup"><span data-stu-id="c85fd-223">The <strong>glColorTableEXT</strong> function converts this component to the internal format in the same way that the red component of an RGBA pixel is, then converts it to an RGBA pixel with green and blue set to 0.0, and alpha set to 1.0.</span></span> <span data-ttu-id="c85fd-224">進行這項轉換之後，圖元的處理方式就像是將它當成 RGBA 圖元讀取一樣。</span><span class="sxs-lookup"><span data-stu-id="c85fd-224">After this conversion, the pixel is treated just as if it had been read as an RGBA pixel.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="GL_GREEN"></span><span id="gl_green"></span><dl> <span data-ttu-id="c85fd-225"><dt><strong>GL_GREEN</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="c85fd-225"><dt><strong>GL_GREEN</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="c85fd-226">每個圖元都是一個綠色的元件。</span><span class="sxs-lookup"><span data-stu-id="c85fd-226">Each pixel is a single green component.</span></span><br/> <span data-ttu-id="c85fd-227"><strong>GlColorTableEXT</strong>函式會以 RGBA 圖元的綠色元件相同的方式，將這個元件轉換成內部格式，然後將其轉換為具有紅色和藍色的 rgba 圖元（設為0.0），並將 Alpha 設定為1.0。</span><span class="sxs-lookup"><span data-stu-id="c85fd-227">The <strong>glColorTableEXT</strong> function converts this component to the internal format in the same way that the green component of an RGBA pixel is, and then converts it to an RGBA pixel with red and blue set to 0.0, and alpha set to 1.0.</span></span> <span data-ttu-id="c85fd-228">進行這項轉換之後，圖元的處理方式就像是將它當成 RGBA 圖元讀取一樣。</span><span class="sxs-lookup"><span data-stu-id="c85fd-228">After this conversion, the pixel is treated just as if it had been read as an RGBA pixel.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="GL_BLUE"></span><span id="gl_blue"></span><dl> <span data-ttu-id="c85fd-229"><dt><strong>GL_BLUE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="c85fd-229"><dt><strong>GL_BLUE</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="c85fd-230">每個圖元都是單一藍色元件。</span><span class="sxs-lookup"><span data-stu-id="c85fd-230">Each pixel is a single blue component.</span></span><br/> <span data-ttu-id="c85fd-231"><strong>GlColorTableEXT</strong>函式會以 RGBA 圖元 blue 元件的相同方式，將這個元件轉換成內部格式，然後將其轉換為具有紅色和綠色設定為0.0 的 RGBA 圖元，然後將 Alpha 設定為1.0。</span><span class="sxs-lookup"><span data-stu-id="c85fd-231">The <strong>glColorTableEXT</strong> function converts this component to the internal format in the same way that the blue component of an RGBA pixel is, and then converts it to an RGBA pixel with red and green set to 0.0, and alpha set to 1.0.</span></span> <span data-ttu-id="c85fd-232">進行這項轉換之後，圖元的處理方式就像是將它當成 RGBA 圖元讀取一樣。</span><span class="sxs-lookup"><span data-stu-id="c85fd-232">After this conversion, the pixel is treated just as if it had been read as an RGBA pixel.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="GL_ALPHA"></span><span id="gl_alpha"></span><dl> <span data-ttu-id="c85fd-233"><dt><strong>GL_ALPHA</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="c85fd-233"><dt><strong>GL_ALPHA</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="c85fd-234">每個圖元都是單一 Alpha 元件。</span><span class="sxs-lookup"><span data-stu-id="c85fd-234">Each pixel is a single alpha component.</span></span><br/> <span data-ttu-id="c85fd-235"><strong>GlColorTableEXT</strong>函式會以 RGBA 圖元 Alpha 元件的相同方式，將這個元件轉換成內部格式，然後將它轉換為紅色、綠色和藍色設定為0.0 的 RGBA 圖元。</span><span class="sxs-lookup"><span data-stu-id="c85fd-235">The <strong>glColorTableEXT</strong> function converts this component to the internal format in the same way that the alpha component of an RGBA pixel is, and then converts it to an RGBA pixel with red, green, and blue set to 0.0.</span></span> <span data-ttu-id="c85fd-236">進行這項轉換之後，圖元的處理方式就像是將它當成 RGBA 圖元讀取一樣。</span><span class="sxs-lookup"><span data-stu-id="c85fd-236">After this conversion, the pixel is treated just as if it had been read as an RGBA pixel.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="GL_RGB"></span><span id="gl_rgb"></span><dl> <span data-ttu-id="c85fd-237"><dt><strong>GL_RGB</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="c85fd-237"><dt><strong>GL_RGB</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="c85fd-238">每個圖元都是三個元件的群組，順序如下：紅色、綠色、藍色。</span><span class="sxs-lookup"><span data-stu-id="c85fd-238">Each pixel is a group of three components in this order: red, green, blue.</span></span><br/> <span data-ttu-id="c85fd-239"><strong>GlColorTableEXT</strong>函式會以 RGBA 圖元的 red、綠和 blue 元件的相同方式，將每個元件轉換成內部格式。</span><span class="sxs-lookup"><span data-stu-id="c85fd-239">The <strong>glColorTableEXT</strong> function converts each component to the internal format in the same way that the red, green, and blue components of an RGBA pixel are.</span></span> <span data-ttu-id="c85fd-240">色彩三重轉換成將 Alpha 設定為1.0 的 RGBA 圖元。</span><span class="sxs-lookup"><span data-stu-id="c85fd-240">The color triple is converted to an RGBA pixel with alpha set to 1.0.</span></span> <span data-ttu-id="c85fd-241">進行這項轉換之後，圖元的處理方式就像是將它當成 RGBA 圖元讀取一樣。</span><span class="sxs-lookup"><span data-stu-id="c85fd-241">After this conversion, the pixel is treated just as if it had been read as an RGBA pixel.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="GL_BGR_EXT"></span><span id="gl_bgr_ext"></span><dl> <span data-ttu-id="c85fd-242"><dt><strong>GL_BGR_EXT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="c85fd-242"><dt><strong>GL_BGR_EXT</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="c85fd-243">每個圖元都是三個元件的群組，順序如下：藍色、綠色、紅色。</span><span class="sxs-lookup"><span data-stu-id="c85fd-243">Each pixel is a group of three components in this order: blue, green, red.</span></span><br/> <span data-ttu-id="c85fd-244">GL_BGR_EXT 提供的格式符合 Windows 裝置獨立點陣圖 (Dib) 的記憶體配置。</span><span class="sxs-lookup"><span data-stu-id="c85fd-244">GL_BGR_EXT provides a format that matches the memory layout of Windows device-independent bitmaps (DIBs).</span></span> <span data-ttu-id="c85fd-245">因此，您的應用程式可以使用 Windows 函式呼叫和 OpenGL 圖元函式呼叫的相同資料。</span><span class="sxs-lookup"><span data-stu-id="c85fd-245">Thus your applications can use the same data with Windows function calls and OpenGL pixel function calls.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="GL_BGRA_EXT"></span><span id="gl_bgra_ext"></span><dl> <span data-ttu-id="c85fd-246"><dt><strong>GL_BGRA_EXT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="c85fd-246"><dt><strong>GL_BGRA_EXT</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="c85fd-247">每個圖元都是四個元件的群組，順序如下： blue、綠、red、Alpha。</span><span class="sxs-lookup"><span data-stu-id="c85fd-247">Each pixel is a group of four components in this order: blue, green, red, alpha.</span></span><br/> <span data-ttu-id="c85fd-248">GL_BGRA_EXT 提供的格式符合 Windows 裝置獨立點陣圖 (Dib) 的記憶體配置。</span><span class="sxs-lookup"><span data-stu-id="c85fd-248">GL_BGRA_EXT provides a format that matches the memory layout of Windows device-independent bitmaps (DIBs).</span></span> <span data-ttu-id="c85fd-249">因此，您的應用程式可以使用 Windows 函式呼叫和 OpenGL 圖元函式呼叫的相同資料。</span><span class="sxs-lookup"><span data-stu-id="c85fd-249">Thus your applications can use the same data with Windows function calls and OpenGL pixel function calls.</span></span><br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="c85fd-250">*type*</span><span class="sxs-lookup"><span data-stu-id="c85fd-250">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="c85fd-251">*資料* 的資料類型。</span><span class="sxs-lookup"><span data-stu-id="c85fd-251">The data type for *data*.</span></span> <span data-ttu-id="c85fd-252">接受下列符號常數： GL 不 \_ 帶正負號的 \_ 位元組、gl \_ 位元組、GL 不 \_ 帶正負號 \_ 的 SHORT、gl \_ short、gl 不 \_ 帶正負號 \_ int、gl \_ int 和 gl \_ FLOAT。</span><span class="sxs-lookup"><span data-stu-id="c85fd-252">The following symbolic constants are accepted: GL\_UNSIGNED\_BYTE, GL\_BYTE, GL\_UNSIGNED\_SHORT, GL\_SHORT, GL\_UNSIGNED\_INT, GL\_INT, and GL\_FLOAT.</span></span>

<span data-ttu-id="c85fd-253">下表摘要說明 *型* 別參數之有效常數的意義。</span><span class="sxs-lookup"><span data-stu-id="c85fd-253">The following table summarizes the meaning of the valid constants for the *type* parameter.</span></span>



| <span data-ttu-id="c85fd-254">值</span><span class="sxs-lookup"><span data-stu-id="c85fd-254">Value</span></span>                                                                                                                                                                      | <span data-ttu-id="c85fd-255">意義</span><span class="sxs-lookup"><span data-stu-id="c85fd-255">Meaning</span></span>                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="GL_UNSIGNED_BYTE"></span><span id="gl_unsigned_byte"></span><dl> <span data-ttu-id="c85fd-256"><dt>**GL 不 \_ 帶正負號的 \_ 位元組**</dt></span><span class="sxs-lookup"><span data-stu-id="c85fd-256"><dt>**GL\_UNSIGNED\_BYTE**</dt></span></span> </dl>    | <span data-ttu-id="c85fd-257">不帶正負號的 8 位元整數</span><span class="sxs-lookup"><span data-stu-id="c85fd-257">Unsigned 8-bit integer</span></span><br/>                |
| <span id="GL_BYTE"></span><span id="gl_byte"></span><dl> <span data-ttu-id="c85fd-258"><dt>**GL \_ 位元組**</dt></span><span class="sxs-lookup"><span data-stu-id="c85fd-258"><dt>**GL\_BYTE**</dt></span></span> </dl>                                | <span data-ttu-id="c85fd-259">帶正負號的 8 位元整數</span><span class="sxs-lookup"><span data-stu-id="c85fd-259">Signed 8-bit integer</span></span><br/>                  |
| <span id="GL_UNSIGNED_SHORT"></span><span id="gl_unsigned_short"></span><dl> <span data-ttu-id="c85fd-260"><dt>**GL 不 \_ 帶正負號 \_ 簡短**</dt></span><span class="sxs-lookup"><span data-stu-id="c85fd-260"><dt>**GL\_UNSIGNED\_SHORT**</dt></span></span> </dl> | <span data-ttu-id="c85fd-261">不帶正負號的 16 位元整數</span><span class="sxs-lookup"><span data-stu-id="c85fd-261">Unsigned 16-bit integer</span></span><br/>               |
| <span id="GL_SHORT"></span><span id="gl_short"></span><dl> <span data-ttu-id="c85fd-262"><dt>**GL \_ 短期**</dt></span><span class="sxs-lookup"><span data-stu-id="c85fd-262"><dt>**GL\_SHORT**</dt></span></span> </dl>                             | <span data-ttu-id="c85fd-263">帶正負號的 16 位元整數</span><span class="sxs-lookup"><span data-stu-id="c85fd-263">Signed 16-bit integer</span></span><br/>                 |
| <span id="GL_UNSIGNED_INT"></span><span id="gl_unsigned_int"></span><dl> <span data-ttu-id="c85fd-264"><dt>**GL 不 \_ 帶正負號 \_ INT**</dt></span><span class="sxs-lookup"><span data-stu-id="c85fd-264"><dt>**GL\_UNSIGNED\_INT**</dt></span></span> </dl>       | <span data-ttu-id="c85fd-265">不帶正負號的 32 位元整數</span><span class="sxs-lookup"><span data-stu-id="c85fd-265">Unsigned 32-bit integer</span></span><br/>               |
| <span id="GL_INT"></span><span id="gl_int"></span><dl> <span data-ttu-id="c85fd-266"><dt>**GL \_ INT**</dt></span><span class="sxs-lookup"><span data-stu-id="c85fd-266"><dt>**GL\_INT**</dt></span></span> </dl>                                   | <span data-ttu-id="c85fd-267">32 位元整數</span><span class="sxs-lookup"><span data-stu-id="c85fd-267">32-bit integer</span></span><br/>                        |
| <span id="GL_FLOAT"></span><span id="gl_float"></span><dl> <span data-ttu-id="c85fd-268"><dt>**GL \_ FLOAT**</dt></span><span class="sxs-lookup"><span data-stu-id="c85fd-268"><dt>**GL\_FLOAT**</dt></span></span> </dl>                             | <span data-ttu-id="c85fd-269">單精確度浮點值</span><span class="sxs-lookup"><span data-stu-id="c85fd-269">Single-precision floating-point value</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="c85fd-270">*data*</span><span class="sxs-lookup"><span data-stu-id="c85fd-270">*data*</span></span> 
</dt> <dd>

<span data-ttu-id="c85fd-271">指向調色板材質資料的指標。</span><span class="sxs-lookup"><span data-stu-id="c85fd-271">A pointer to the paletted texture data.</span></span> <span data-ttu-id="c85fd-272">資料會被視為一個調色板專案的立體材質調色板專案的單一圖元。</span><span class="sxs-lookup"><span data-stu-id="c85fd-272">The data is treated as single pixels of a 1-D texture palette entry for a palette entry.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c85fd-273">傳回值</span><span class="sxs-lookup"><span data-stu-id="c85fd-273">Return value</span></span>

<span data-ttu-id="c85fd-274">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="c85fd-274">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c85fd-275">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="c85fd-275">Error codes</span></span>

<span data-ttu-id="c85fd-276">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="c85fd-276">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="c85fd-277">Name</span><span class="sxs-lookup"><span data-stu-id="c85fd-277">Name</span></span>                                                                                                  | <span data-ttu-id="c85fd-278">意義</span><span class="sxs-lookup"><span data-stu-id="c85fd-278">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c85fd-279"><dt>**GL \_ 無效 \_ 值**</dt></span><span class="sxs-lookup"><span data-stu-id="c85fd-279"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="c85fd-280">*寬度* 是不正確整數。</span><span class="sxs-lookup"><span data-stu-id="c85fd-280">*width* was an invalid integer.</span></span><br/>                                                                                            |
| <dl> <span data-ttu-id="c85fd-281"><dt>**GL \_ 無效 \_ 列舉**</dt></span><span class="sxs-lookup"><span data-stu-id="c85fd-281"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="c85fd-282">*target*、 *internalFormat*、 *format* 或 *type* 不是可接受的值。</span><span class="sxs-lookup"><span data-stu-id="c85fd-282">*target*, *internalFormat*, *format*, or *type* was not an accepted value.</span></span><br/>                                                 |
| <dl> <span data-ttu-id="c85fd-283"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="c85fd-283"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="c85fd-284">呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。</span><span class="sxs-lookup"><span data-stu-id="c85fd-284">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="c85fd-285">備註</span><span class="sxs-lookup"><span data-stu-id="c85fd-285">Remarks</span></span>

<span data-ttu-id="c85fd-286">調色板紋理是以色彩的調色板和一組影像資料所定義，而這組影像資料是由色彩表 (色彩表) 的色彩專案的索引組成。</span><span class="sxs-lookup"><span data-stu-id="c85fd-286">Paletted textures are defined with a palette of colors and a set of image data that is composed of indexes to color entries of a palette (a color table).</span></span>

<span data-ttu-id="c85fd-287">**GlColorTableEXT** 函式會指定目標材質的材質調色板。</span><span class="sxs-lookup"><span data-stu-id="c85fd-287">The **glColorTableEXT** function specifies the texture palette of a targeted texture.</span></span> <span data-ttu-id="c85fd-288">它會取得記憶體中的 *資料* ，並將資料轉換成每個調色板專案都是立體材質的單一圖元。</span><span class="sxs-lookup"><span data-stu-id="c85fd-288">It takes the *data* from memory and converts the data as if each palette entry is a single pixel of a 1-D texture.</span></span> <span data-ttu-id="c85fd-289">**GlColorTableEXT** 函式會解壓縮和轉換資料，並將其轉譯成符合指定格式的內部格式（最接近指定 *格式*）。</span><span class="sxs-lookup"><span data-stu-id="c85fd-289">The **glColorTableEXT** function unpacks and converts the data and translates it into an internal format that matches the given *format* as closely as possible.</span></span>

<span data-ttu-id="c85fd-290">如果調色板的 *寬度* 大於材質資料中的色彩索引範圍，部分調色板專案就不會使用。</span><span class="sxs-lookup"><span data-stu-id="c85fd-290">If a palette's *width* is greater than the range of the color indexes in the texture data, some of the palette entries are unused.</span></span> <span data-ttu-id="c85fd-291">如果調色板的 *寬度* 小於紋理資料中的色彩索引範圍，則會忽略紋理資料的最高有效位，而且在存取調色板時只會使用索引中適當的位數。</span><span class="sxs-lookup"><span data-stu-id="c85fd-291">If a palette's *width* is less than the range of the color indexes in the texture data, the most significant bits of the texture data are ignored and only the appropriate number of bits in the index are used when accessing the palette.</span></span> <span data-ttu-id="c85fd-292">當您使用 PROXY  \_ 材質 \_ 1d 或 proxy 材質2d 指定 proxy 目標時 \_ \_ ，會重設 proxy 材質的選擇區，並設定其參數，但不會傳送或存取任何資料。</span><span class="sxs-lookup"><span data-stu-id="c85fd-292">When you specify a proxy *target* using PROXY\_TEXTURE\_1D or PROXY\_TEXTURE\_2D, the palette of the proxy texture is resized and its parameters are set but no data is transferred or accessed.</span></span>

<span data-ttu-id="c85fd-293">當 *目標* 參數為 GL \_ proxy \_ 材質 \_ 1d 或 GL \_ proxy \_ 材質 \_ 2d，且執行不支援針對 *格式* 或 *寬度* 指定的值時， **glColorTableEXT** 可能無法建立要求的色彩表。</span><span class="sxs-lookup"><span data-stu-id="c85fd-293">When the *target* parameter is GL\_PROXY\_TEXTURE\_1D or GL\_PROXY\_TEXTURE\_2D, and the implementation does not support the values specified for either *format* or *width*, **glColorTableEXT** can fail to create the requested color table.</span></span> <span data-ttu-id="c85fd-294">在此情況下，color 資料表是空的，而且所有取出的參數都是零。</span><span class="sxs-lookup"><span data-stu-id="c85fd-294">In this case, the color table is empty and all parameters retrieved will be zero.</span></span> <span data-ttu-id="c85fd-295">您可以藉由使用 proxy 目標呼叫 **glColorTableEXT** ，然後呼叫 [**glGetColorTableParameterivEXT**](glgetcolortableparameterivext.md) 或 [**glGetColorTableParameterfvEXT**](glgetcolortableparameterfvext.md) 來判斷 width 參數是否符合 **GlColorTableEXT** 所設定的，來判斷 OpenGL 是否支援特定的色彩表格式和大小。</span><span class="sxs-lookup"><span data-stu-id="c85fd-295">You can determine whether OpenGL supports a particular color table format and size by calling **glColorTableEXT** with a proxy target, and then calling [**glGetColorTableParameterivEXT**](glgetcolortableparameterivext.md) or [**glGetColorTableParameterfvEXT**](glgetcolortableparameterfvext.md) to determine whether the width parameter matches that set by **glColorTableEXT**.</span></span> <span data-ttu-id="c85fd-296">如果取出的寬度為零，則 **glColorTable** 的色彩表格要求會失敗。</span><span class="sxs-lookup"><span data-stu-id="c85fd-296">If the retrieved width is zero, the color table request by **glColorTable** failed.</span></span> <span data-ttu-id="c85fd-297">如果取出的寬度不是零，您可以使用紋理1d 或材質2d 的真實目標來呼叫 **glColorTable** ， \_ \_ 以設定色彩表。</span><span class="sxs-lookup"><span data-stu-id="c85fd-297">If the retrieved width is not zero, you can call **glColorTable** with the real target with TEXTURE\_1D or TEXTURE\_2D to set the color table.</span></span>

> [!Note]  
> <span data-ttu-id="c85fd-298">**GlColorTableEXT** 函式是延伸模組函式，不是標準 OpenGL 程式庫的一部分，而是 GL \_ EXT \_ \_ 材質擴充功能的一部分。</span><span class="sxs-lookup"><span data-stu-id="c85fd-298">The **glColorTableEXT** function is an extension function that is not part of the standard OpenGL library but is part of the GL\_EXT\_paletted\_texture extension.</span></span> <span data-ttu-id="c85fd-299">若要檢查您的 OpenGL 執行是否支援 **glColorTableEXT**，請) 呼叫 [**glGetString**](glgetstring.md) (GL \_ 延伸模組。</span><span class="sxs-lookup"><span data-stu-id="c85fd-299">To check whether your implementation of OpenGL supports **glColorTableEXT**, call [**glGetString**](glgetstring.md)(GL\_EXTENSIONS).</span></span> <span data-ttu-id="c85fd-300">如果它傳回 GL \_ EXT \_ \_ （調色板）材質，則會支援 **glColorTableEXT** 。</span><span class="sxs-lookup"><span data-stu-id="c85fd-300">If it returns GL\_EXT\_paletted\_texture, **glColorTableEXT** is supported.</span></span> <span data-ttu-id="c85fd-301">若要取得擴充函數的函式位址，請呼叫 [**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress)。</span><span class="sxs-lookup"><span data-stu-id="c85fd-301">To obtain the function address of an extension function, call [**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress).</span></span>

 

<span data-ttu-id="c85fd-302">若要取出 **glColorTableEXT** 函數所指定的實際色彩資料表資料，請呼叫 [**glGetColorTableEXT**](glgetcolortableext.md)。</span><span class="sxs-lookup"><span data-stu-id="c85fd-302">To retrieve the actual color table data specified by the **glColorTableEXT** function, call [**glGetColorTableEXT**](glgetcolortableext.md).</span></span> <span data-ttu-id="c85fd-303">若要抓取 **glColorTableEXT** 函式所指定之色彩表的參數（例如 *寬度* 和 *格式*），請呼叫 **glGetColorTableParameterivEXT** 或 **glGetColorTableParameterfvEXT** 函數。</span><span class="sxs-lookup"><span data-stu-id="c85fd-303">To retrieve the parameters, such as *width* and *format*, of the color table specified by the **glColorTableEXT** function, call the **glGetColorTableParameterivEXT** or **glGetColorTableParameterfvEXT** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="c85fd-304">規格需求</span><span class="sxs-lookup"><span data-stu-id="c85fd-304">Requirements</span></span>



| <span data-ttu-id="c85fd-305">需求</span><span class="sxs-lookup"><span data-stu-id="c85fd-305">Requirement</span></span> | <span data-ttu-id="c85fd-306">值</span><span class="sxs-lookup"><span data-stu-id="c85fd-306">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="c85fd-307">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c85fd-307">Minimum supported client</span></span><br/> | <span data-ttu-id="c85fd-308">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c85fd-308">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                      |
| <span data-ttu-id="c85fd-309">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c85fd-309">Minimum supported server</span></span><br/> | <span data-ttu-id="c85fd-310">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c85fd-310">Windows 2000 Server \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="c85fd-311">標頭</span><span class="sxs-lookup"><span data-stu-id="c85fd-311">Header</span></span><br/>                   | <dl> <span data-ttu-id="c85fd-312"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="c85fd-312"><dt>Gl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c85fd-313">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c85fd-313">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c85fd-314">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="c85fd-314">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="c85fd-315">**glColorSubTableEXT**</span><span class="sxs-lookup"><span data-stu-id="c85fd-315">**glColorSubTableEXT**</span></span>](glcolorsubtableext.md)
</dt> <dt>

[<span data-ttu-id="c85fd-316">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="c85fd-316">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="c85fd-317">**glGetColorTableEXT**</span><span class="sxs-lookup"><span data-stu-id="c85fd-317">**glGetColorTableEXT**</span></span>](glgetcolortableext.md)
</dt> <dt>

[<span data-ttu-id="c85fd-318">**glGetColorTableParameterfvEXT**</span><span class="sxs-lookup"><span data-stu-id="c85fd-318">**glGetColorTableParameterfvEXT**</span></span>](glgetcolortableparameterfvext.md)
</dt> <dt>

[<span data-ttu-id="c85fd-319">**glGetColorTableParameterivEXT**</span><span class="sxs-lookup"><span data-stu-id="c85fd-319">**glGetColorTableParameterivEXT**</span></span>](glgetcolortableparameterivext.md)
</dt> <dt>

[<span data-ttu-id="c85fd-320">**wglGetProcAddress**</span><span class="sxs-lookup"><span data-stu-id="c85fd-320">**wglGetProcAddress**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress)
</dt> </dl>

 

 





