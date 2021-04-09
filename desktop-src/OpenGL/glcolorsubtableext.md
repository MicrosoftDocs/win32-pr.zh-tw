---
title: 'glColorSubTableEXT 函式 (Gl) '
description: GlColorSubTableEXT 函式會指定要取代之目標材質調色板的一部分。
ms.assetid: 21430245-f837-4c7a-944f-b44482254b12
keywords:
- glColorSubTableEXT 函式 OpenGL
topic_type:
- apiref
api_name:
- glColorSubTableEXT
api_location:
- Gl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a0386bda82bf08ae778d20b1be69858698ac7bb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843747"
---
# <a name="glcolorsubtableext-function"></a><span data-ttu-id="843bd-104">glColorSubTableEXT 函式</span><span class="sxs-lookup"><span data-stu-id="843bd-104">glColorSubTableEXT function</span></span>

<span data-ttu-id="843bd-105">**GlColorSubTableEXT** 函式會指定要取代之目標材質調色板的一部分。</span><span class="sxs-lookup"><span data-stu-id="843bd-105">The **glColorSubTableEXT** function specifies a portion of the targeted texture's palette to be replaced.</span></span>

## <a name="syntax"></a><span data-ttu-id="843bd-106">語法</span><span class="sxs-lookup"><span data-stu-id="843bd-106">Syntax</span></span>


```C++
void WINAPI glColorSubTableEXT(
         GLenum  target,
         GLsizei start,
         GLsizei count,
         GLenum  format,
         GLenum  type,
   const GLvoid  *data
);
```



## <a name="parameters"></a><span data-ttu-id="843bd-107">參數</span><span class="sxs-lookup"><span data-stu-id="843bd-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="843bd-108">*目標*</span><span class="sxs-lookup"><span data-stu-id="843bd-108">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="843bd-109">要變更其調色板的目標調色板材質。</span><span class="sxs-lookup"><span data-stu-id="843bd-109">The target paletted texture that is to have its palette changed.</span></span> <span data-ttu-id="843bd-110">必須是材質 \_ 1d 或紋理 \_ 2d。</span><span class="sxs-lookup"><span data-stu-id="843bd-110">Must be TEXTURE\_1D or TEXTURE\_2D.</span></span>

</dd> <dt>

<span data-ttu-id="843bd-111">*開始*</span><span class="sxs-lookup"><span data-stu-id="843bd-111">*start*</span></span> 
</dt> <dd>

<span data-ttu-id="843bd-112">要變更之調色板的起始調色板索引項目。</span><span class="sxs-lookup"><span data-stu-id="843bd-112">The starting palette index entry of the palette to be changed.</span></span>

</dd> <dt>

<span data-ttu-id="843bd-113">*計數*</span><span class="sxs-lookup"><span data-stu-id="843bd-113">*count*</span></span> 
</dt> <dd>

<span data-ttu-id="843bd-114">*開始* 時要變更之調色板的調色板索引項目索引項目數目。</span><span class="sxs-lookup"><span data-stu-id="843bd-114">The number of palette index entries of the palette to be changed beginning at *start*.</span></span> <span data-ttu-id="843bd-115">*Count* 參數會決定變更的調色板索引項目範圍。</span><span class="sxs-lookup"><span data-stu-id="843bd-115">The *count* parameter determines the range of palette index entries that are changed.</span></span>

</dd> <dt>

<span data-ttu-id="843bd-116">*format*</span><span class="sxs-lookup"><span data-stu-id="843bd-116">*format*</span></span> 
</dt> <dd>

<span data-ttu-id="843bd-117">圖元資料的格式。</span><span class="sxs-lookup"><span data-stu-id="843bd-117">The format of the pixel data.</span></span> <span data-ttu-id="843bd-118">接受下列符號常數。</span><span class="sxs-lookup"><span data-stu-id="843bd-118">The following symbolic constants are accepted.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="843bd-119">值</span><span class="sxs-lookup"><span data-stu-id="843bd-119">Value</span></span></th>
<th><span data-ttu-id="843bd-120">意義</span><span class="sxs-lookup"><span data-stu-id="843bd-120">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="GL_RGBA"></span><span id="gl_rgba"></span><dl> <span data-ttu-id="843bd-121"><dt><strong>GL_RGBA</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="843bd-121"><dt><strong>GL_RGBA</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="843bd-122">每個圖元都是四個元件的群組，順序如下：紅色、綠色、藍色、Alpha。</span><span class="sxs-lookup"><span data-stu-id="843bd-122">Each pixel is a group of four components in the following order: red, green, blue, alpha.</span></span> <span data-ttu-id="843bd-123">RGBA 格式的決定方式如下：</span><span class="sxs-lookup"><span data-stu-id="843bd-123">The RGBA format is determined in this way:</span></span> <br/>
<ol>
<li><span data-ttu-id="843bd-124"><strong>GlColorSubTableEXT</strong>函式會將浮點值直接轉換成具有未指定精確度的內部格式。</span><span class="sxs-lookup"><span data-stu-id="843bd-124">The <strong>glColorSubTableEXT</strong> function converts floating-point values directly to an internal format with unspecified precision.</span></span> <span data-ttu-id="843bd-125">帶正負號的整數值會以線性方式對應至內部格式，如此一來，最正面的可表示整數值會對應至1.0，而最大的可表示值會對應至-1.0。</span><span class="sxs-lookup"><span data-stu-id="843bd-125">Signed integer values are mapped linearly to the internal format such that the most positive representable integer value maps to 1.0, and the most negative representable value maps to -1.0.</span></span> <span data-ttu-id="843bd-126">不帶正負號的整數資料的對應方式如下：最大整數值對應至1.0，而零對應至0.0。</span><span class="sxs-lookup"><span data-stu-id="843bd-126">Unsigned integer data is mapped similarly: the largest integer value maps to 1.0, and zero maps to 0.0.</span></span></li>
<li><span data-ttu-id="843bd-127"><strong>GlColorSubTableEXT</strong>函式會 GL_c_SCALE 將產生的色彩值相乘，並將其新增至 GL_c_BIAS，其中<em>c</em>是紅色、綠色、藍色和 ALPHA，適用于個別的色彩元件。</span><span class="sxs-lookup"><span data-stu-id="843bd-127">The <strong>glColorSubTableEXT</strong> function multiplies the resulting color values by GL_c_SCALE and adds them to GL_c_BIAS, where <em>c</em> is RED, GREEN, BLUE, and ALPHA for the respective color components.</span></span> <span data-ttu-id="843bd-128">結果會壓制到 [0，1] 範圍內。</span><span class="sxs-lookup"><span data-stu-id="843bd-128">The results are clamped to the range [0,1].</span></span></li>
<li><span data-ttu-id="843bd-129">如果 GL_MAP_COLOR 為 <strong>TRUE</strong>， <strong>glColorSubTableEXT</strong> 會依 GL_PIXEL_MAP_c_TO_c 查閱資料表的大小來調整每個色彩元件，然後以資料表在該資料表中參考的值取代該元件; <em>c</em> 分別為 R、G、B 或 A。</span><span class="sxs-lookup"><span data-stu-id="843bd-129">If GL_MAP_COLOR is <strong>TRUE</strong>, <strong>glColorSubTableEXT</strong> scales each color component by the size of lookup table GL_PIXEL_MAP_c_TO_c, then replaces the component by the value that it references in that table; <em>c</em> is R, G, B, or A, respectively.</span></span></li>
<li><span data-ttu-id="843bd-130"><strong>GlColorSubTableEXT</strong>函式會將目前的點陣位置<em>z</em>座標和材質座標附加至每個圖元，然後將<em>x</em>和<em>y</em>視窗座標指派給第<em>n</em>個片段（例如<em>x</em>），以將產生的 RGBA 色彩轉換成片段：</span><span class="sxs-lookup"><span data-stu-id="843bd-130">The <strong>glColorSubTableEXT</strong> function converts the resulting RGBA colors to fragments by attaching the current raster position <em>z</em>-coordinate and texture coordinates to each pixel, then assigning <em>x</em> and <em>y</em> window coordinates to the <em>n</em>th fragment such that<em>x</em>?</span></span><span data-ttu-id="843bd-131"> = <em>x</em><sub>r</sub> + <em>n</em> mod <em>寬度</em></span><span class="sxs-lookup"><span data-stu-id="843bd-131"> = <em>x</em><sub>r</sub> + <em>n</em> mod <em>width</em></span></span><br/> <span data-ttu-id="843bd-132"><em>y</em>？</span><span class="sxs-lookup"><span data-stu-id="843bd-132"><em>y</em>?</span></span><span data-ttu-id="843bd-133"> = <em>y</em><sub>r</sub> +<em>n/寬度</em></span><span class="sxs-lookup"><span data-stu-id="843bd-133"> = <em>y</em><sub>r</sub> +<em>n / width</em></span></span><br/> <span data-ttu-id="843bd-134">其中 (<em>x</em><sub>r</sub> ， <em>y</em><sub>r</sub> ) 是目前的點陣位置。</span><span class="sxs-lookup"><span data-stu-id="843bd-134">where (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) is the current raster position.</span></span><br/></li>
<li><span data-ttu-id="843bd-135">然後，這些圖元片段的處理方式就像是將點、線條或多邊形所產生的片段一樣。</span><span class="sxs-lookup"><span data-stu-id="843bd-135">These pixel fragments are then treated just like the fragments generated by rasterizing points, lines, or polygons.</span></span> <span data-ttu-id="843bd-136"><strong>GlColorSubTableEXT</strong>函式會先套用材質對應、霧化和所有片段作業，然後再將片段寫入畫面格緩衝區。</span><span class="sxs-lookup"><span data-stu-id="843bd-136">The <strong>glColorSubTableEXT</strong> function applies texture mapping, fog, and all the fragment operations before writing the fragments to the framebuffer.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span id="GL_RED"></span><span id="gl_red"></span><dl> <span data-ttu-id="843bd-137"><dt><strong>GL_RED</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="843bd-137"><dt><strong>GL_RED</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="843bd-138">每個圖元都是單一的紅色元件。</span><span class="sxs-lookup"><span data-stu-id="843bd-138">Each pixel is a single red component.</span></span><br/> <span data-ttu-id="843bd-139"><strong>GlColorSubTableEXT</strong>函式會以 RGBA 圖元的紅色元件相同的方式，將這個元件轉換成內部格式，然後將其轉換為具有綠色和藍色的 rgba 圖元（設為0.0），並將 Alpha 設定為1.0。</span><span class="sxs-lookup"><span data-stu-id="843bd-139">The <strong>glColorSubTableEXT</strong> function converts this component to the internal format in the same way that the red component of an RGBA pixel is, then converts it to an RGBA pixel with green and blue set to 0.0, and alpha set to 1.0.</span></span> <span data-ttu-id="843bd-140">進行這項轉換之後，圖元的處理方式就像是將它當成 RGBA 圖元讀取一樣。</span><span class="sxs-lookup"><span data-stu-id="843bd-140">After this conversion, the pixel is treated just as if it had been read as an RGBA pixel.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="GL_GREEN"></span><span id="gl_green"></span><dl> <span data-ttu-id="843bd-141"><dt><strong>GL_GREEN</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="843bd-141"><dt><strong>GL_GREEN</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="843bd-142">每個圖元都是一個綠色的元件。</span><span class="sxs-lookup"><span data-stu-id="843bd-142">Each pixel is a single green component.</span></span><br/> <span data-ttu-id="843bd-143"><strong>GlColorSubTableEXT</strong>函式會以 RGBA 圖元的綠色元件相同的方式，將這個元件轉換成內部格式，然後將其轉換為具有紅色和藍色的 rgba 圖元（設為0.0），並將 Alpha 設定為1.0。</span><span class="sxs-lookup"><span data-stu-id="843bd-143">The <strong>glColorSubTableEXT</strong> function converts this component to the internal format in the same way that the green component of an RGBA pixel is, and then converts it to an RGBA pixel with red and blue set to 0.0, and alpha set to 1.0.</span></span> <span data-ttu-id="843bd-144">進行這項轉換之後，圖元的處理方式就像是將它當成 RGBA 圖元讀取一樣。</span><span class="sxs-lookup"><span data-stu-id="843bd-144">After this conversion, the pixel is treated just as if it had been read as an RGBA pixel.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="GL_BLUE"></span><span id="gl_blue"></span><dl> <span data-ttu-id="843bd-145"><dt><strong>GL_BLUE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="843bd-145"><dt><strong>GL_BLUE</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="843bd-146">每個圖元都是單一藍色元件。</span><span class="sxs-lookup"><span data-stu-id="843bd-146">Each pixel is a single blue component.</span></span><br/> <span data-ttu-id="843bd-147"><strong>GlColorSubTableEXT</strong>函式會以 RGBA 圖元 blue 元件的相同方式，將這個元件轉換成內部格式，然後將其轉換為具有紅色和綠色設定為0.0 的 RGBA 圖元，然後將 Alpha 設定為1.0。</span><span class="sxs-lookup"><span data-stu-id="843bd-147">The <strong>glColorSubTableEXT</strong> function converts this component to the internal format in the same way that the blue component of an RGBA pixel is, and then converts it to an RGBA pixel with red and green set to 0.0, and alpha set to 1.0.</span></span> <span data-ttu-id="843bd-148">進行這項轉換之後，圖元的處理方式就像是將它當成 RGBA 圖元讀取一樣。</span><span class="sxs-lookup"><span data-stu-id="843bd-148">After this conversion, the pixel is treated just as if it had been read as an RGBA pixel.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="GL_ALPHA"></span><span id="gl_alpha"></span><dl> <span data-ttu-id="843bd-149"><dt><strong>GL_ALPHA</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="843bd-149"><dt><strong>GL_ALPHA</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="843bd-150">每個圖元都是單一 Alpha 元件。</span><span class="sxs-lookup"><span data-stu-id="843bd-150">Each pixel is a single alpha component.</span></span><br/> <span data-ttu-id="843bd-151"><strong>GlColorSubTableEXT</strong>函式會以 RGBA 圖元 Alpha 元件的相同方式，將這個元件轉換成內部格式，然後將它轉換為紅色、綠色和藍色設定為0.0 的 RGBA 圖元。</span><span class="sxs-lookup"><span data-stu-id="843bd-151">The <strong>glColorSubTableEXT</strong> function converts this component to the internal format in the same way that the alpha component of an RGBA pixel is, and then converts it to an RGBA pixel with red, green, and blue set to 0.0.</span></span> <span data-ttu-id="843bd-152">進行這項轉換之後，圖元的處理方式就像是將它當成 RGBA 圖元讀取一樣。</span><span class="sxs-lookup"><span data-stu-id="843bd-152">After this conversion, the pixel is treated just as if it had been read as an RGBA pixel.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="GL_RGB"></span><span id="gl_rgb"></span><dl> <span data-ttu-id="843bd-153"><dt><strong>GL_RGB</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="843bd-153"><dt><strong>GL_RGB</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="843bd-154">每個圖元都是三個元件的群組，順序如下：紅色、綠色、藍色。</span><span class="sxs-lookup"><span data-stu-id="843bd-154">Each pixel is a group of three components in this order: red, green, blue.</span></span><br/> <span data-ttu-id="843bd-155"><strong>GlColorSubTableEXT</strong>函式會以 RGBA 圖元的 red、綠和 blue 元件的相同方式，將每個元件轉換成內部格式。</span><span class="sxs-lookup"><span data-stu-id="843bd-155">The <strong>glColorSubTableEXT</strong> function converts each component to the internal format in the same way that the red, green, and blue components of an RGBA pixel are.</span></span> <span data-ttu-id="843bd-156">色彩三重轉換成將 Alpha 設定為1.0 的 RGBA 圖元。</span><span class="sxs-lookup"><span data-stu-id="843bd-156">The color triple is converted to an RGBA pixel with alpha set to 1.0.</span></span> <span data-ttu-id="843bd-157">進行這項轉換之後，圖元的處理方式就像是將它當成 RGBA 圖元讀取一樣。</span><span class="sxs-lookup"><span data-stu-id="843bd-157">After this conversion, the pixel is treated just as if it had been read as an RGBA pixel.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="GL_BGR_EXT"></span><span id="gl_bgr_ext"></span><dl> <span data-ttu-id="843bd-158"><dt><strong>GL_BGR_EXT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="843bd-158"><dt><strong>GL_BGR_EXT</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="843bd-159">每個圖元都是三個元件的群組，順序如下：藍色、綠色、紅色。</span><span class="sxs-lookup"><span data-stu-id="843bd-159">Each pixel is a group of three components in this order: blue, green, red.</span></span><br/> <span data-ttu-id="843bd-160">GL_BGR_EXT 提供的格式符合 Windows 裝置獨立點陣圖 (Dib) 的記憶體配置。</span><span class="sxs-lookup"><span data-stu-id="843bd-160">GL_BGR_EXT provides a format that matches the memory layout of Windows device-independent bitmaps (DIBs).</span></span> <span data-ttu-id="843bd-161">因此，您的應用程式可以使用 Windows 函式呼叫和 OpenGL 圖元函式呼叫的相同資料。</span><span class="sxs-lookup"><span data-stu-id="843bd-161">Thus your applications can use the same data with Windows function calls and OpenGL pixel function calls.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="GL_BGRA_EXT"></span><span id="gl_bgra_ext"></span><dl> <span data-ttu-id="843bd-162"><dt><strong>GL_BGRA_EXT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="843bd-162"><dt><strong>GL_BGRA_EXT</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="843bd-163">每個圖元都是四個元件的群組，順序如下： blue、綠、red、Alpha。</span><span class="sxs-lookup"><span data-stu-id="843bd-163">Each pixel is a group of four components in this order: blue, green, red, alpha.</span></span><br/> <span data-ttu-id="843bd-164">GL_BGRA_EXT 提供的格式符合 Windows 裝置獨立點陣圖 (Dib) 的記憶體配置。</span><span class="sxs-lookup"><span data-stu-id="843bd-164">GL_BGRA_EXT provides a format that matches the memory layout of Windows device-independent bitmaps (DIBs).</span></span> <span data-ttu-id="843bd-165">因此，您的應用程式可以使用 Windows 函式呼叫和 OpenGL 圖元函式呼叫的相同資料。</span><span class="sxs-lookup"><span data-stu-id="843bd-165">Thus your applications can use the same data with Windows function calls and OpenGL pixel function calls.</span></span><br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="843bd-166">*type*</span><span class="sxs-lookup"><span data-stu-id="843bd-166">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="843bd-167">*資料* 的資料類型。</span><span class="sxs-lookup"><span data-stu-id="843bd-167">The data type for *data*.</span></span> <span data-ttu-id="843bd-168">接受下列符號常數： GL 不 \_ 帶正負號的 \_ 位元組、gl \_ 位元組、GL 不 \_ 帶正負號 \_ 的 SHORT、gl \_ short、gl 不 \_ 帶正負號 \_ int、gl \_ int 和 gl \_ FLOAT。</span><span class="sxs-lookup"><span data-stu-id="843bd-168">The following symbolic constants are accepted: GL\_UNSIGNED\_BYTE, GL\_BYTE, GL\_UNSIGNED\_SHORT, GL\_SHORT, GL\_UNSIGNED\_INT, GL\_INT, and GL\_FLOAT.</span></span>

<span data-ttu-id="843bd-169">下表摘要說明 *型* 別參數之有效常數的意義。</span><span class="sxs-lookup"><span data-stu-id="843bd-169">The following table summarizes the meaning of the valid constants for the *type* parameter.</span></span>



| <span data-ttu-id="843bd-170">值</span><span class="sxs-lookup"><span data-stu-id="843bd-170">Value</span></span>                                                                                                                                                                      | <span data-ttu-id="843bd-171">意義</span><span class="sxs-lookup"><span data-stu-id="843bd-171">Meaning</span></span>                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="GL_UNSIGNED_BYTE"></span><span id="gl_unsigned_byte"></span><dl> <span data-ttu-id="843bd-172"><dt>**GL 不 \_ 帶正負號的 \_ 位元組**</dt></span><span class="sxs-lookup"><span data-stu-id="843bd-172"><dt>**GL\_UNSIGNED\_BYTE**</dt></span></span> </dl>    | <span data-ttu-id="843bd-173">不帶正負號的 8 位元整數</span><span class="sxs-lookup"><span data-stu-id="843bd-173">Unsigned 8-bit integer</span></span><br/>                |
| <span id="GL_BYTE"></span><span id="gl_byte"></span><dl> <span data-ttu-id="843bd-174"><dt>**GL \_ 位元組**</dt></span><span class="sxs-lookup"><span data-stu-id="843bd-174"><dt>**GL\_BYTE**</dt></span></span> </dl>                                | <span data-ttu-id="843bd-175">帶正負號的 8 位元整數</span><span class="sxs-lookup"><span data-stu-id="843bd-175">Signed 8-bit integer</span></span><br/>                  |
| <span id="GL_UNSIGNED_SHORT"></span><span id="gl_unsigned_short"></span><dl> <span data-ttu-id="843bd-176"><dt>**GL 不 \_ 帶正負號 \_ 簡短**</dt></span><span class="sxs-lookup"><span data-stu-id="843bd-176"><dt>**GL\_UNSIGNED\_SHORT**</dt></span></span> </dl> | <span data-ttu-id="843bd-177">不帶正負號的 16 位元整數</span><span class="sxs-lookup"><span data-stu-id="843bd-177">Unsigned 16-bit integer</span></span><br/>               |
| <span id="GL_SHORT"></span><span id="gl_short"></span><dl> <span data-ttu-id="843bd-178"><dt>**GL \_ 短期**</dt></span><span class="sxs-lookup"><span data-stu-id="843bd-178"><dt>**GL\_SHORT**</dt></span></span> </dl>                             | <span data-ttu-id="843bd-179">帶正負號的 16 位元整數</span><span class="sxs-lookup"><span data-stu-id="843bd-179">Signed 16-bit integer</span></span><br/>                 |
| <span id="GL_UNSIGNED_INT"></span><span id="gl_unsigned_int"></span><dl> <span data-ttu-id="843bd-180"><dt>**GL 不 \_ 帶正負號 \_ INT**</dt></span><span class="sxs-lookup"><span data-stu-id="843bd-180"><dt>**GL\_UNSIGNED\_INT**</dt></span></span> </dl>       | <span data-ttu-id="843bd-181">不帶正負號的 32 位元整數</span><span class="sxs-lookup"><span data-stu-id="843bd-181">Unsigned 32-bit integer</span></span><br/>               |
| <span id="GL_INT"></span><span id="gl_int"></span><dl> <span data-ttu-id="843bd-182"><dt>**GL \_ INT**</dt></span><span class="sxs-lookup"><span data-stu-id="843bd-182"><dt>**GL\_INT**</dt></span></span> </dl>                                   | <span data-ttu-id="843bd-183">32 位元整數</span><span class="sxs-lookup"><span data-stu-id="843bd-183">32-bit integer</span></span><br/>                        |
| <span id="GL_FLOAT"></span><span id="gl_float"></span><dl> <span data-ttu-id="843bd-184"><dt>**GL \_ FLOAT**</dt></span><span class="sxs-lookup"><span data-stu-id="843bd-184"><dt>**GL\_FLOAT**</dt></span></span> </dl>                             | <span data-ttu-id="843bd-185">單精確度浮點值</span><span class="sxs-lookup"><span data-stu-id="843bd-185">Single-precision floating-point value</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="843bd-186">*data*</span><span class="sxs-lookup"><span data-stu-id="843bd-186">*data*</span></span> 
</dt> <dd>

<span data-ttu-id="843bd-187">指向調色板材質資料的指標。</span><span class="sxs-lookup"><span data-stu-id="843bd-187">A pointer to the paletted texture data.</span></span> <span data-ttu-id="843bd-188">資料會被視為一個調色板專案的立體材質調色板專案的單一圖元。</span><span class="sxs-lookup"><span data-stu-id="843bd-188">The data is treated as single pixels of a 1-D texture palette entry for a palette entry.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="843bd-189">傳回值</span><span class="sxs-lookup"><span data-stu-id="843bd-189">Return value</span></span>

<span data-ttu-id="843bd-190">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="843bd-190">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="843bd-191">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="843bd-191">Error codes</span></span>

<span data-ttu-id="843bd-192">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="843bd-192">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="843bd-193">Name</span><span class="sxs-lookup"><span data-stu-id="843bd-193">Name</span></span>                                                                                              | <span data-ttu-id="843bd-194">意義</span><span class="sxs-lookup"><span data-stu-id="843bd-194">Meaning</span></span>                                                                                                                               |
|---------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="843bd-195"><dt>**GL \_ 無效 \_ 值**</dt></span><span class="sxs-lookup"><span data-stu-id="843bd-195"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl> | <span data-ttu-id="843bd-196">*開始* 或 *計數* 是不正確整數。</span><span class="sxs-lookup"><span data-stu-id="843bd-196">*start* or *count* was an invalid integer.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="843bd-197"><dt>**GL \_ 無效 \_ 列舉**</dt></span><span class="sxs-lookup"><span data-stu-id="843bd-197"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>  | <span data-ttu-id="843bd-198">*目標*、 *格式* 或 *類型* 不是可接受的值。</span><span class="sxs-lookup"><span data-stu-id="843bd-198">*target*, *format*,or *type* was not an accepted value.</span></span><br/>                                                                    |
| <dl> <span data-ttu-id="843bd-199"><dt>**GL \_ 無效 \_ 值**</dt></span><span class="sxs-lookup"><span data-stu-id="843bd-199"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl> | <span data-ttu-id="843bd-200">呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。</span><span class="sxs-lookup"><span data-stu-id="843bd-200">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="843bd-201">備註</span><span class="sxs-lookup"><span data-stu-id="843bd-201">Remarks</span></span>

<span data-ttu-id="843bd-202">**GlColorSubTableEXT** 函式會指定要取代之目前目標材質調色板的部分。</span><span class="sxs-lookup"><span data-stu-id="843bd-202">The **glColorSubTableEXT** function specifies portions of the current targeted texture's palette to be replaced.</span></span> <span data-ttu-id="843bd-203">不同于 [**glColorTableEXT**](glcolortableext.md)，您無法將 *目標* 參數指定為 proxy 材質選擇區。</span><span class="sxs-lookup"><span data-stu-id="843bd-203">Unlike [**glColorTableEXT**](glcolortableext.md), you cannot specify the *target* parameter to be a proxy texture palette.</span></span>

> [!Note]  
> <span data-ttu-id="843bd-204">**GlColorSubTableEXT** 函式是延伸模組函式，不是標準 OpenGL 程式庫的一部分，而是 GL \_ EXT \_ \_ 材質擴充功能的一部分。</span><span class="sxs-lookup"><span data-stu-id="843bd-204">The **glColorSubTableEXT** function is an extension function that is not part of the standard OpenGL library but is part of the GL\_EXT\_paletted\_texture extension.</span></span> <span data-ttu-id="843bd-205">若要檢查您的 OpenGL 執行是否支援 **glColorSubTableEXT**，請) 呼叫 [**glGetString**](glgetstring.md) (GL \_ 延伸模組。</span><span class="sxs-lookup"><span data-stu-id="843bd-205">To check whether your implementation of OpenGL supports **glColorSubTableEXT**, call [**glGetString**](glgetstring.md)(GL\_EXTENSIONS).</span></span> <span data-ttu-id="843bd-206">如果它傳回 GL \_ EXT \_ \_ （調色板）材質，則會支援 **glColorSubTableEXT** 。</span><span class="sxs-lookup"><span data-stu-id="843bd-206">If it returns GL\_EXT\_paletted\_texture, **glColorSubTableEXT** is supported.</span></span> <span data-ttu-id="843bd-207">若要取得擴充函數的函式位址，請呼叫 [**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress)。</span><span class="sxs-lookup"><span data-stu-id="843bd-207">To obtain the function address of an extension function, call [**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="843bd-208">規格需求</span><span class="sxs-lookup"><span data-stu-id="843bd-208">Requirements</span></span>



| <span data-ttu-id="843bd-209">需求</span><span class="sxs-lookup"><span data-stu-id="843bd-209">Requirement</span></span> | <span data-ttu-id="843bd-210">值</span><span class="sxs-lookup"><span data-stu-id="843bd-210">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="843bd-211">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="843bd-211">Minimum supported client</span></span><br/> | <span data-ttu-id="843bd-212">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="843bd-212">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                      |
| <span data-ttu-id="843bd-213">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="843bd-213">Minimum supported server</span></span><br/> | <span data-ttu-id="843bd-214">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="843bd-214">Windows 2000 Server \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="843bd-215">標頭</span><span class="sxs-lookup"><span data-stu-id="843bd-215">Header</span></span><br/>                   | <dl> <span data-ttu-id="843bd-216"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="843bd-216"><dt>Gl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="843bd-217">另請參閱</span><span class="sxs-lookup"><span data-stu-id="843bd-217">See also</span></span>

<dl> <dt>

[<span data-ttu-id="843bd-218">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="843bd-218">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="843bd-219">**glColorTableEXT**</span><span class="sxs-lookup"><span data-stu-id="843bd-219">**glColorTableEXT**</span></span>](glcolortableext.md)
</dt> <dt>

[<span data-ttu-id="843bd-220">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="843bd-220">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="843bd-221">**glGetColorTableEXT**</span><span class="sxs-lookup"><span data-stu-id="843bd-221">**glGetColorTableEXT**</span></span>](glgetcolortableext.md)
</dt> <dt>

[<span data-ttu-id="843bd-222">**glGetColorTableParameterfvEXT**</span><span class="sxs-lookup"><span data-stu-id="843bd-222">**glGetColorTableParameterfvEXT**</span></span>](glgetcolortableparameterfvext.md)
</dt> <dt>

[<span data-ttu-id="843bd-223">**glGetColorTableParameterivEXT**</span><span class="sxs-lookup"><span data-stu-id="843bd-223">**glGetColorTableParameterivEXT**</span></span>](glgetcolortableparameterivext.md)
</dt> <dt>

[<span data-ttu-id="843bd-224">**glGetString**</span><span class="sxs-lookup"><span data-stu-id="843bd-224">**glGetString**</span></span>](glgetstring.md)
</dt> <dt>

[<span data-ttu-id="843bd-225">**wglGetProcAddress**</span><span class="sxs-lookup"><span data-stu-id="843bd-225">**wglGetProcAddress**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress)
</dt> </dl>

 

 





