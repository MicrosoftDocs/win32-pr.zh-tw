---
title: 'glGetColorTableEXT 函式 (Gl) '
description: GlGetColorTableEXT 函式會取得目前目標材質調色板的色彩資料表資料。
ms.assetid: 9169c4e1-a22e-48fe-bd45-4549c1a10ff0
keywords:
- glGetColorTableEXT 函式 OpenGL
topic_type:
- apiref
api_name:
- glGetColorTableEXT
api_location:
- Gl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 811dc53b32c937970fbef8d87fa9a2ef4eb8b978
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966358"
---
# <a name="glgetcolortableext-function"></a><span data-ttu-id="7b3ba-104">glGetColorTableEXT 函式</span><span class="sxs-lookup"><span data-stu-id="7b3ba-104">glGetColorTableEXT function</span></span>

<span data-ttu-id="7b3ba-105">**GlGetColorTableEXT** 函式會取得目前目標材質調色板的色彩資料表資料。</span><span class="sxs-lookup"><span data-stu-id="7b3ba-105">The **glGetColorTableEXT** function gets the color table data of the current targeted texture palette.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b3ba-106">語法</span><span class="sxs-lookup"><span data-stu-id="7b3ba-106">Syntax</span></span>


```C++
void WINAPI glGetColorTableEXT(
         GLenum target,
         GLenum format,
         GLenum type,
   const GLvoid *data
);
```



## <a name="parameters"></a><span data-ttu-id="7b3ba-107">參數</span><span class="sxs-lookup"><span data-stu-id="7b3ba-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b3ba-108">*目標*</span><span class="sxs-lookup"><span data-stu-id="7b3ba-108">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="7b3ba-109">要變更其調色板的目標材質。</span><span class="sxs-lookup"><span data-stu-id="7b3ba-109">The target texture that is to have its palette changed.</span></span> <span data-ttu-id="7b3ba-110">必須是材質 \_ 1d 或紋理 \_ 2d。</span><span class="sxs-lookup"><span data-stu-id="7b3ba-110">Must be TEXTURE\_1D or TEXTURE\_2D.</span></span>

</dd> <dt>

<span data-ttu-id="7b3ba-111">*format*</span><span class="sxs-lookup"><span data-stu-id="7b3ba-111">*format*</span></span> 
</dt> <dd>

<span data-ttu-id="7b3ba-112">圖元資料的格式。</span><span class="sxs-lookup"><span data-stu-id="7b3ba-112">The format of the pixel data.</span></span> <span data-ttu-id="7b3ba-113">接受下列符號常數。</span><span class="sxs-lookup"><span data-stu-id="7b3ba-113">The following symbolic constants are accepted.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7b3ba-114">值</span><span class="sxs-lookup"><span data-stu-id="7b3ba-114">Value</span></span></th>
<th><span data-ttu-id="7b3ba-115">意義</span><span class="sxs-lookup"><span data-stu-id="7b3ba-115">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="GL_RGBA"></span><span id="gl_rgba"></span><dl> <span data-ttu-id="7b3ba-116"><dt><strong>GL_RGBA</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="7b3ba-116"><dt><strong>GL_RGBA</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="7b3ba-117">每個圖元都是四個元件的群組，順序如下：紅色、綠色、藍色、Alpha。</span><span class="sxs-lookup"><span data-stu-id="7b3ba-117">Each pixel is a group of four components in the following order: red, green, blue, alpha.</span></span> <span data-ttu-id="7b3ba-118">RGBA 格式的決定方式如下：</span><span class="sxs-lookup"><span data-stu-id="7b3ba-118">The RGBA format is determined in this way:</span></span> <br/>
<ol>
<li><span data-ttu-id="7b3ba-119"><strong>GlGetColorTableEXT</strong>函式會將浮點值直接轉換成具有未指定精確度的內部格式。</span><span class="sxs-lookup"><span data-stu-id="7b3ba-119">The <strong>glGetColorTableEXT</strong> function converts floating-point values directly to an internal format with unspecified precision.</span></span> <span data-ttu-id="7b3ba-120">帶正負號的整數值會以線性方式對應至內部格式，如此一來，最正面的可表示整數值會對應至1.0，而最大的可表示整數值會對應至-1.0。</span><span class="sxs-lookup"><span data-stu-id="7b3ba-120">Signed integer values are mapped linearly to the internal format such that the most positive representable integer value maps to 1.0, and the most negative representable integer value maps to -1.0.</span></span> <span data-ttu-id="7b3ba-121">不帶正負號的整數資料的對應方式如下：最大整數值對應至1.0，而零對應至0.0。</span><span class="sxs-lookup"><span data-stu-id="7b3ba-121">Unsigned integer data is mapped similarly: the largest integer value maps to 1.0, and zero maps to 0.0.</span></span></li>
<li><span data-ttu-id="7b3ba-122"><strong>GlGetColorTableEXT</strong>函式會 GL_c_SCALE 將產生的色彩值相乘，並將其新增至 GL_c_BIAS，其中<em>c</em>是紅色、綠色、藍色和 ALPHA，適用于個別的色彩元件。</span><span class="sxs-lookup"><span data-stu-id="7b3ba-122">The <strong>glGetColorTableEXT</strong> function multiplies the resulting color values by GL_c_SCALE and adds them to GL_c_BIAS, where <em>c</em> is RED, GREEN, BLUE, and ALPHA for the respective color components.</span></span> <span data-ttu-id="7b3ba-123">結果會壓制到 [0，1] 範圍內。</span><span class="sxs-lookup"><span data-stu-id="7b3ba-123">The results are clamped to the range [0,1].</span></span></li>
<li><span data-ttu-id="7b3ba-124">如果 GL_MAP_COLOR 為 <strong>TRUE</strong>， <strong>glGetColorTableEXT</strong> 會依 GL_PIXEL_MAP_c_TO_c 查閱資料表的大小來調整每個色彩元件，然後以資料表在該資料表中參考的值取代該元件; <em>c</em> 分別為 R、G、B 或 A。</span><span class="sxs-lookup"><span data-stu-id="7b3ba-124">If GL_MAP_COLOR is <strong>TRUE</strong>, <strong>glGetColorTableEXT</strong> scales each color component by the size of lookup table GL_PIXEL_MAP_c_TO_c, then replaces the component by the value that it references in that table; <em>c</em> is R, G, B, or A, respectively.</span></span></li>
<li><span data-ttu-id="7b3ba-125"><strong>GlGetColorTableEXT</strong>函式會將目前的點陣位置 z 座標和材質座標附加至每個圖元，然後將<em>x</em>和<em>y</em>視窗座標指派給<em>n</em>個片段，以將產生的 RGBA 色彩轉換成片段，例如<em>x</em>？</span><span class="sxs-lookup"><span data-stu-id="7b3ba-125">The <strong>glGetColorTableEXT</strong> function converts the resulting RGBA colors to fragments by attaching the current raster position z-coordinate and texture coordinates to each pixel, then assigning <em>x</em> and <em>y</em> window coordinates to the <em>n</em>th fragment, such that <em>x</em>?</span></span><span data-ttu-id="7b3ba-126"> = <em>x</em><sub>r</sub> + <em>n</em> mod <em>寬度</em></span><span class="sxs-lookup"><span data-stu-id="7b3ba-126"> = <em>x</em><sub>r</sub> + <em>n</em> mod <em>width</em></span></span><br/> <span data-ttu-id="7b3ba-127"><em>y</em>？</span><span class="sxs-lookup"><span data-stu-id="7b3ba-127"><em>y</em>?</span></span><span data-ttu-id="7b3ba-128"> = <em>y</em><sub>r</sub> + <em>n/寬度</em></span><span class="sxs-lookup"><span data-stu-id="7b3ba-128"> = <em>y</em><sub>r</sub> + <em>n/width</em></span></span><br/> <span data-ttu-id="7b3ba-129">其中 (<em>x</em><sub>r</sub> ， <em>y</em><sub>r</sub> ) 是目前的點陣位置。</span><span class="sxs-lookup"><span data-stu-id="7b3ba-129">where (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) is the current raster position.</span></span><br/></li>
<li><span data-ttu-id="7b3ba-130">然後，這些圖元片段的處理方式就像是將點、線條或多邊形所產生的片段一樣。</span><span class="sxs-lookup"><span data-stu-id="7b3ba-130">These pixel fragments are then treated just like the fragments generated by rasterizing points, lines, or polygons.</span></span> <span data-ttu-id="7b3ba-131"><strong>GlGetColorTableEXT</strong>函式會先套用材質對應、霧化和所有片段作業，然後再將片段寫入畫面格緩衝區。</span><span class="sxs-lookup"><span data-stu-id="7b3ba-131">The <strong>glGetColorTableEXT</strong> function applies texture mapping, fog, and all the fragment operations before writing the fragments to the framebuffer.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span id="GL_RED"></span><span id="gl_red"></span><dl> <span data-ttu-id="7b3ba-132"><dt><strong>GL_RED</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="7b3ba-132"><dt><strong>GL_RED</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="7b3ba-133">每個圖元都是單一的紅色元件。</span><span class="sxs-lookup"><span data-stu-id="7b3ba-133">Each pixel is a single red component.</span></span><br/> <span data-ttu-id="7b3ba-134"><strong>GlGetColorTableEXT</strong>函式會以 RGBA 圖元的紅色元件相同的方式，將這個元件轉換成內部格式，然後將其轉換為具有綠色和藍色的 rgba 圖元（設為0.0），並將 Alpha 設定為1.0。</span><span class="sxs-lookup"><span data-stu-id="7b3ba-134">The <strong>glGetColorTableEXT</strong> function converts this component to the internal format in the same way that the red component of an RGBA pixel is, then converts it to an RGBA pixel with green and blue set to 0.0, and alpha set to 1.0.</span></span> <span data-ttu-id="7b3ba-135">進行這項轉換之後，圖元的處理方式就像是將它當成 RGBA 圖元讀取一樣。</span><span class="sxs-lookup"><span data-stu-id="7b3ba-135">After this conversion, the pixel is treated just as if it had been read as an RGBA pixel.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="GL_GREEN"></span><span id="gl_green"></span><dl> <span data-ttu-id="7b3ba-136"><dt><strong>GL_GREEN</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="7b3ba-136"><dt><strong>GL_GREEN</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="7b3ba-137">每個圖元都是一個綠色的元件。</span><span class="sxs-lookup"><span data-stu-id="7b3ba-137">Each pixel is a single green component.</span></span><br/> <span data-ttu-id="7b3ba-138"><strong>GlGetColorTableEXT</strong>函式會以 RGBA 圖元的綠色元件相同的方式，將這個元件轉換成內部格式，然後將其轉換為具有紅色和藍色的 rgba 圖元（設為0.0），並將 Alpha 設定為1.0。</span><span class="sxs-lookup"><span data-stu-id="7b3ba-138">The <strong>glGetColorTableEXT</strong> function converts this component to the internal format in the same way that the green component of an RGBA pixel is, and then converts it to an RGBA pixel with red and blue set to 0.0, and alpha set to 1.0.</span></span> <span data-ttu-id="7b3ba-139">進行這項轉換之後，圖元的處理方式就像是將它當成 RGBA 圖元讀取一樣。</span><span class="sxs-lookup"><span data-stu-id="7b3ba-139">After this conversion, the pixel is treated just as if it had been read as an RGBA pixel.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="GL_BLUE"></span><span id="gl_blue"></span><dl> <span data-ttu-id="7b3ba-140"><dt><strong>GL_BLUE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="7b3ba-140"><dt><strong>GL_BLUE</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="7b3ba-141">每個圖元都是單一藍色元件。</span><span class="sxs-lookup"><span data-stu-id="7b3ba-141">Each pixel is a single blue component.</span></span><br/> <span data-ttu-id="7b3ba-142"><strong>GlGetColorTableEXT</strong>函式會以 RGBA 圖元 blue 元件的相同方式，將這個元件轉換成內部格式，然後將其轉換為具有紅色和綠色設定為0.0 的 RGBA 圖元，然後將 Alpha 設定為1.0。</span><span class="sxs-lookup"><span data-stu-id="7b3ba-142">The <strong>glGetColorTableEXT</strong> function converts this component to the internal format in the same way that the blue component of an RGBA pixel is, and then converts it to an RGBA pixel with red and green set to 0.0, and alpha set to 1.0.</span></span> <span data-ttu-id="7b3ba-143">進行這項轉換之後，圖元的處理方式就像是將它當成 RGBA 圖元讀取一樣。</span><span class="sxs-lookup"><span data-stu-id="7b3ba-143">After this conversion, the pixel is treated just as if it had been read as an RGBA pixel.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="GL_ALPHA"></span><span id="gl_alpha"></span><dl> <span data-ttu-id="7b3ba-144"><dt><strong>GL_ALPHA</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="7b3ba-144"><dt><strong>GL_ALPHA</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="7b3ba-145">每個圖元都是單一 Alpha 元件。</span><span class="sxs-lookup"><span data-stu-id="7b3ba-145">Each pixel is a single alpha component.</span></span><br/> <span data-ttu-id="7b3ba-146"><strong>GlGetColorTableEXT</strong>函式會以 RGBA 圖元 Alpha 元件的相同方式，將這個元件轉換成內部格式，然後將它轉換為紅色、綠色和藍色設定為0.0 的 RGBA 圖元。</span><span class="sxs-lookup"><span data-stu-id="7b3ba-146">The <strong>glGetColorTableEXT</strong> function converts this component to the internal format in the same way that the alpha component of an RGBA pixel is, and then converts it to an RGBA pixel with red, green, and blue set to 0.0.</span></span> <span data-ttu-id="7b3ba-147">進行這項轉換之後，圖元的處理方式就像是將它當成 RGBA 圖元讀取一樣。</span><span class="sxs-lookup"><span data-stu-id="7b3ba-147">After this conversion, the pixel is treated just as if it had been read as an RGBA pixel.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="GL_RGB"></span><span id="gl_rgb"></span><dl> <span data-ttu-id="7b3ba-148"><dt><strong>GL_RGB</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="7b3ba-148"><dt><strong>GL_RGB</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="7b3ba-149">每個圖元都是三個元件的群組，順序如下：紅色、綠色、藍色。</span><span class="sxs-lookup"><span data-stu-id="7b3ba-149">Each pixel is a group of three components in this order: red, green, blue.</span></span><br/> <span data-ttu-id="7b3ba-150"><strong>GlGetColorTableEXT</strong>函式會以 RGBA 圖元的 red、綠和 blue 元件的相同方式，將每個元件轉換成內部格式。</span><span class="sxs-lookup"><span data-stu-id="7b3ba-150">The <strong>glGetColorTableEXT</strong> function converts each component to the internal format in the same way that the red, green, and blue components of an RGBA pixel are.</span></span> <span data-ttu-id="7b3ba-151">色彩三重轉換成將 Alpha 設定為1.0 的 RGBA 圖元。</span><span class="sxs-lookup"><span data-stu-id="7b3ba-151">The color triple is converted to an RGBA pixel with alpha set to 1.0.</span></span> <span data-ttu-id="7b3ba-152">進行這項轉換之後，圖元的處理方式就像是將它當成 RGBA 圖元讀取一樣。</span><span class="sxs-lookup"><span data-stu-id="7b3ba-152">After this conversion, the pixel is treated just as if it had been read as an RGBA pixel.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="GL_BGR_EXT"></span><span id="gl_bgr_ext"></span><dl> <span data-ttu-id="7b3ba-153"><dt><strong>GL_BGR_EXT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="7b3ba-153"><dt><strong>GL_BGR_EXT</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="7b3ba-154">每個圖元都是三個元件的群組，順序如下：藍色、綠色、紅色。</span><span class="sxs-lookup"><span data-stu-id="7b3ba-154">Each pixel is a group of three components in this order: blue, green, red.</span></span><br/> <span data-ttu-id="7b3ba-155">GL_BGR_EXT 提供的格式符合 Microsoft Windows 裝置獨立點陣圖 (Dib) 的記憶體配置。</span><span class="sxs-lookup"><span data-stu-id="7b3ba-155">GL_BGR_EXT provides a format that matches the memory layout of Microsoft Windows device-independent bitmaps (DIBs).</span></span> <span data-ttu-id="7b3ba-156">因此，您的應用程式可以使用 Windows 函式呼叫和 OpenGL 圖元函式呼叫的相同資料。</span><span class="sxs-lookup"><span data-stu-id="7b3ba-156">Thus, your applications can use the same data with Windows function calls and OpenGL pixel function calls.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="GL_BGRA_EXT"></span><span id="gl_bgra_ext"></span><dl> <span data-ttu-id="7b3ba-157"><dt><strong>GL_BGRA_EXT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="7b3ba-157"><dt><strong>GL_BGRA_EXT</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="7b3ba-158">每個圖元都是四個元件的群組，順序如下： blue、綠、red、Alpha。</span><span class="sxs-lookup"><span data-stu-id="7b3ba-158">Each pixel is a group of four components in this order: blue, green, red, alpha.</span></span><br/> <span data-ttu-id="7b3ba-159">GL_BGRA_EXT 提供的格式符合 Windows 裝置獨立點陣圖 (Dib) 的記憶體配置。</span><span class="sxs-lookup"><span data-stu-id="7b3ba-159">GL_BGRA_EXT provides a format that matches the memory layout of Windows device-independent bitmaps (DIBs).</span></span> <span data-ttu-id="7b3ba-160">因此，您的應用程式可以使用 Windows 函式呼叫和 OpenGL 圖元函式呼叫的相同資料。</span><span class="sxs-lookup"><span data-stu-id="7b3ba-160">Thus your applications can use the same data with Windows function calls and OpenGL pixel function calls.</span></span><br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="7b3ba-161">*type*</span><span class="sxs-lookup"><span data-stu-id="7b3ba-161">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="7b3ba-162">*資料* 的資料類型。</span><span class="sxs-lookup"><span data-stu-id="7b3ba-162">The data type for *data*.</span></span> <span data-ttu-id="7b3ba-163">以下是接受的符號常數及其意義。</span><span class="sxs-lookup"><span data-stu-id="7b3ba-163">The following are the accepted symbolic constants and their meanings.</span></span>



| <span data-ttu-id="7b3ba-164">值</span><span class="sxs-lookup"><span data-stu-id="7b3ba-164">Value</span></span>                                                                                                                                                                      | <span data-ttu-id="7b3ba-165">意義</span><span class="sxs-lookup"><span data-stu-id="7b3ba-165">Meaning</span></span>                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="GL_UNSIGNED_BYTE"></span><span id="gl_unsigned_byte"></span><dl> <span data-ttu-id="7b3ba-166"><dt>**GL 不 \_ 帶正負號的 \_ 位元組**</dt></span><span class="sxs-lookup"><span data-stu-id="7b3ba-166"><dt>**GL\_UNSIGNED\_BYTE**</dt></span></span> </dl>    | <span data-ttu-id="7b3ba-167">不帶正負號的 8 位元整數</span><span class="sxs-lookup"><span data-stu-id="7b3ba-167">Unsigned 8-bit integer</span></span><br/>                |
| <span id="GL_BYTE"></span><span id="gl_byte"></span><dl> <span data-ttu-id="7b3ba-168"><dt>**GL \_ 位元組**</dt></span><span class="sxs-lookup"><span data-stu-id="7b3ba-168"><dt>**GL\_BYTE**</dt></span></span> </dl>                                | <span data-ttu-id="7b3ba-169">帶正負號的 8 位元整數</span><span class="sxs-lookup"><span data-stu-id="7b3ba-169">Signed 8-bit integer</span></span><br/>                  |
| <span id="GL_UNSIGNED_SHORT"></span><span id="gl_unsigned_short"></span><dl> <span data-ttu-id="7b3ba-170"><dt>**GL 不 \_ 帶正負號 \_ 簡短**</dt></span><span class="sxs-lookup"><span data-stu-id="7b3ba-170"><dt>**GL\_UNSIGNED\_SHORT**</dt></span></span> </dl> | <span data-ttu-id="7b3ba-171">不帶正負號的 16 位元整數</span><span class="sxs-lookup"><span data-stu-id="7b3ba-171">Unsigned 16-bit integer</span></span><br/>               |
| <span id="GL_SHORT"></span><span id="gl_short"></span><dl> <span data-ttu-id="7b3ba-172"><dt>**GL \_ 短期**</dt></span><span class="sxs-lookup"><span data-stu-id="7b3ba-172"><dt>**GL\_SHORT**</dt></span></span> </dl>                             | <span data-ttu-id="7b3ba-173">帶正負號的 16 位元整數</span><span class="sxs-lookup"><span data-stu-id="7b3ba-173">Signed 16-bit integer</span></span><br/>                 |
| <span id="GL_UNSIGNED_INT"></span><span id="gl_unsigned_int"></span><dl> <span data-ttu-id="7b3ba-174"><dt>**GL 不 \_ 帶正負號 \_ INT**</dt></span><span class="sxs-lookup"><span data-stu-id="7b3ba-174"><dt>**GL\_UNSIGNED\_INT**</dt></span></span> </dl>       | <span data-ttu-id="7b3ba-175">不帶正負號的 32 位元整數</span><span class="sxs-lookup"><span data-stu-id="7b3ba-175">Unsigned 32-bit integer</span></span><br/>               |
| <span id="GL_INT"></span><span id="gl_int"></span><dl> <span data-ttu-id="7b3ba-176"><dt>**GL \_ INT**</dt></span><span class="sxs-lookup"><span data-stu-id="7b3ba-176"><dt>**GL\_INT**</dt></span></span> </dl>                                   | <span data-ttu-id="7b3ba-177">32 位元整數</span><span class="sxs-lookup"><span data-stu-id="7b3ba-177">32-bit integer</span></span><br/>                        |
| <span id="GL_FLOAT"></span><span id="gl_float"></span><dl> <span data-ttu-id="7b3ba-178"><dt>**GL \_ FLOAT**</dt></span><span class="sxs-lookup"><span data-stu-id="7b3ba-178"><dt>**GL\_FLOAT**</dt></span></span> </dl>                             | <span data-ttu-id="7b3ba-179">單精確度浮點值</span><span class="sxs-lookup"><span data-stu-id="7b3ba-179">Single-precision floating-point value</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="7b3ba-180">*data*</span><span class="sxs-lookup"><span data-stu-id="7b3ba-180">*data*</span></span> 
</dt> <dd>

<span data-ttu-id="7b3ba-181">指向要儲存傳回之色彩資料表資訊的位置。</span><span class="sxs-lookup"><span data-stu-id="7b3ba-181">Points to the location where returned color table information is to be stored.</span></span> <span data-ttu-id="7b3ba-182">每個色彩資料表專案都會儲存為立體材質的單一圖元。</span><span class="sxs-lookup"><span data-stu-id="7b3ba-182">Each color table entry is stored as if it was a single pixel of a 1-D texture.</span></span> <span data-ttu-id="7b3ba-183">因為所有紋理都有預設的調色板，所以即使紋理資料不是調色板格式， **glGetColorTableEXT** 一律會傳回檔色板資訊。</span><span class="sxs-lookup"><span data-stu-id="7b3ba-183">Because all textures have a default palette, **glGetColorTableEXT** always returns palette information even if the texture data is not in a paletted format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b3ba-184">傳回值</span><span class="sxs-lookup"><span data-stu-id="7b3ba-184">Return value</span></span>

<span data-ttu-id="7b3ba-185">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="7b3ba-185">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="7b3ba-186">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="7b3ba-186">Error codes</span></span>

<span data-ttu-id="7b3ba-187">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="7b3ba-187">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="7b3ba-188">Name</span><span class="sxs-lookup"><span data-stu-id="7b3ba-188">Name</span></span>                                                                                                  | <span data-ttu-id="7b3ba-189">意義</span><span class="sxs-lookup"><span data-stu-id="7b3ba-189">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7b3ba-190"><dt>**GL \_ 無效 \_ 列舉**</dt></span><span class="sxs-lookup"><span data-stu-id="7b3ba-190"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="7b3ba-191">*目標*、 *格式* 或 *類型* 不是可接受的值。</span><span class="sxs-lookup"><span data-stu-id="7b3ba-191">*target*, *format*, or *type* was not an accepted value.</span></span><br/>                                                                   |
| <dl> <span data-ttu-id="7b3ba-192"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="7b3ba-192"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="7b3ba-193">呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。</span><span class="sxs-lookup"><span data-stu-id="7b3ba-193">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="7b3ba-194">備註</span><span class="sxs-lookup"><span data-stu-id="7b3ba-194">Remarks</span></span>

<span data-ttu-id="7b3ba-195">**GlGetColorTableEXT** 函數會取得 [**glColorTableEXT**](glcolortableext.md)和 [**glColorSubTableEXT**](glcolorsubtableext.md)所指定的實際色彩資料表資料。</span><span class="sxs-lookup"><span data-stu-id="7b3ba-195">The **glGetColorTableEXT** function gets the actual color table data specified by [**glColorTableEXT**](glcolortableext.md) and [**glColorSubTableEXT**](glcolorsubtableext.md).</span></span>

<span data-ttu-id="7b3ba-196">**GlGetColorTableEXT** 函式是延伸模組函式，不是標準 OpenGL 程式庫的一部分，而是 GL \_ EXT \_ \_ 材質擴充功能的一部分。</span><span class="sxs-lookup"><span data-stu-id="7b3ba-196">The **glGetColorTableEXT** function is an extension function that is not part of the standard OpenGL library but is part of the GL\_EXT\_paletted\_texture extension.</span></span> <span data-ttu-id="7b3ba-197">若要檢查您的 OpenGL 執行是否支援 **glGetColorTableEXT**，請) 呼叫 [**glGetString**](glgetstring.md) (GL \_ 延伸模組。</span><span class="sxs-lookup"><span data-stu-id="7b3ba-197">To check whether your implementation of OpenGL supports **glGetColorTableEXT**, call [**glGetString**](glgetstring.md)(GL\_EXTENSIONS).</span></span> <span data-ttu-id="7b3ba-198">如果它傳回 GL \_ EXT \_ \_ （調色板）材質，則會支援 **glGetColorTableEXT** 。</span><span class="sxs-lookup"><span data-stu-id="7b3ba-198">If it returns GL\_EXT\_paletted\_texture, **glGetColorTableEXT** is supported.</span></span> <span data-ttu-id="7b3ba-199">若要取得擴充函數的函式位址，請呼叫 [**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress)。</span><span class="sxs-lookup"><span data-stu-id="7b3ba-199">To obtain the function address of an extension function, call [**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress).</span></span>

## <a name="requirements"></a><span data-ttu-id="7b3ba-200">規格需求</span><span class="sxs-lookup"><span data-stu-id="7b3ba-200">Requirements</span></span>



| <span data-ttu-id="7b3ba-201">需求</span><span class="sxs-lookup"><span data-stu-id="7b3ba-201">Requirement</span></span> | <span data-ttu-id="7b3ba-202">值</span><span class="sxs-lookup"><span data-stu-id="7b3ba-202">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="7b3ba-203">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7b3ba-203">Minimum supported client</span></span><br/> | <span data-ttu-id="7b3ba-204">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7b3ba-204">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                      |
| <span data-ttu-id="7b3ba-205">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7b3ba-205">Minimum supported server</span></span><br/> | <span data-ttu-id="7b3ba-206">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7b3ba-206">Windows 2000 Server \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="7b3ba-207">標頭</span><span class="sxs-lookup"><span data-stu-id="7b3ba-207">Header</span></span><br/>                   | <dl> <span data-ttu-id="7b3ba-208"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="7b3ba-208"><dt>Gl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b3ba-209">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7b3ba-209">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b3ba-210">**glColorSubTableEXT**</span><span class="sxs-lookup"><span data-stu-id="7b3ba-210">**glColorSubTableEXT**</span></span>](glcolorsubtableext.md)
</dt> <dt>

[<span data-ttu-id="7b3ba-211">**glColorTableEXT**</span><span class="sxs-lookup"><span data-stu-id="7b3ba-211">**glColorTableEXT**</span></span>](glcolortableext.md)
</dt> <dt>

[<span data-ttu-id="7b3ba-212">**glGetColorTableParameterfvEXT**</span><span class="sxs-lookup"><span data-stu-id="7b3ba-212">**glGetColorTableParameterfvEXT**</span></span>](glgetcolortableparameterfvext.md)
</dt> <dt>

[<span data-ttu-id="7b3ba-213">**glGetColorTableParameterivEXT**</span><span class="sxs-lookup"><span data-stu-id="7b3ba-213">**glGetColorTableParameterivEXT**</span></span>](glgetcolortableparameterivext.md)
</dt> <dt>

[<span data-ttu-id="7b3ba-214">**wglGetProcAddress**</span><span class="sxs-lookup"><span data-stu-id="7b3ba-214">**wglGetProcAddress**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress)
</dt> </dl>

 

 





