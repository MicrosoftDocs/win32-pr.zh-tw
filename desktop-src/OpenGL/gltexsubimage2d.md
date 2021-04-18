---
title: 'glTexSubImage2D 函式 (Gl) '
description: GlTexSubImage2D 函式會指定現有一維材質影像的一部分。 您無法使用 glTexSubImage2D 來定義新的材質。
ms.assetid: 2b6cb663-8e1d-4270-b8ba-5a8b43a2ece7
keywords:
- glTexSubImage2D 函式 OpenGL
topic_type:
- apiref
api_name:
- glTexSubImage2D
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7a0a59ae9e6724386cb2f7891a14e4bf9d4c1a6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965060"
---
# <a name="gltexsubimage2d-function"></a><span data-ttu-id="b3c02-105">glTexSubImage2D 函式</span><span class="sxs-lookup"><span data-stu-id="b3c02-105">glTexSubImage2D function</span></span>

<span data-ttu-id="b3c02-106">**GlTexSubImage2D** 函式會指定現有一維材質影像的一部分。</span><span class="sxs-lookup"><span data-stu-id="b3c02-106">The **glTexSubImage2D** function specifies a portion of an existing one-dimensional texture image.</span></span> <span data-ttu-id="b3c02-107">您無法使用 **glTexSubImage2D** 來定義新的材質。</span><span class="sxs-lookup"><span data-stu-id="b3c02-107">You cannot define a new texture with **glTexSubImage2D**.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3c02-108">語法</span><span class="sxs-lookup"><span data-stu-id="b3c02-108">Syntax</span></span>


```C++
void WINAPI glTexSubImage2D(
         GLenum  target,
         GLint   level,
         GLint   xoffset,
         GLint   yoffset,
         GLsizei width,
         GLsizei height,
         GLenum  format,
         GLenum  type,
   const GLvoid  *pixels
);
```



## <a name="parameters"></a><span data-ttu-id="b3c02-109">參數</span><span class="sxs-lookup"><span data-stu-id="b3c02-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3c02-110">*目標*</span><span class="sxs-lookup"><span data-stu-id="b3c02-110">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="b3c02-111">目標材質。</span><span class="sxs-lookup"><span data-stu-id="b3c02-111">The target texture.</span></span> <span data-ttu-id="b3c02-112">必須是 GL \_ 紋理 \_ 2d。</span><span class="sxs-lookup"><span data-stu-id="b3c02-112">Must be GL\_TEXTURE\_2D.</span></span>

</dd> <dt>

<span data-ttu-id="b3c02-113">*level*</span><span class="sxs-lookup"><span data-stu-id="b3c02-113">*level*</span></span> 
</dt> <dd>

<span data-ttu-id="b3c02-114">詳細資料層級數目。</span><span class="sxs-lookup"><span data-stu-id="b3c02-114">The level-of-detail number.</span></span> <span data-ttu-id="b3c02-115">層級0是基底映射。</span><span class="sxs-lookup"><span data-stu-id="b3c02-115">Level 0 is the base image.</span></span> <span data-ttu-id="b3c02-116">層級 *n* 是第 *n* 個 mipmap 縮減影像。</span><span class="sxs-lookup"><span data-stu-id="b3c02-116">Level *n* is the *n* th mipmap reduction image.</span></span>

</dd> <dt>

<span data-ttu-id="b3c02-117">*xoffset*</span><span class="sxs-lookup"><span data-stu-id="b3c02-117">*xoffset*</span></span> 
</dt> <dd>

<span data-ttu-id="b3c02-118">紋理陣列內 *x* 方向的材質位移。</span><span class="sxs-lookup"><span data-stu-id="b3c02-118">A texel offset in the *x* direction within the texture array.</span></span>

</dd> <dt>

<span data-ttu-id="b3c02-119">*yoffset*</span><span class="sxs-lookup"><span data-stu-id="b3c02-119">*yoffset*</span></span> 
</dt> <dd>

<span data-ttu-id="b3c02-120">紋理陣列中 *y* 方向的材質位移。</span><span class="sxs-lookup"><span data-stu-id="b3c02-120">A texel offset in the *y* direction within the texture array.</span></span>

</dd> <dt>

<span data-ttu-id="b3c02-121">*width* (寬度)</span><span class="sxs-lookup"><span data-stu-id="b3c02-121">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="b3c02-122">材質子影像的寬度。</span><span class="sxs-lookup"><span data-stu-id="b3c02-122">The width of the texture sub-image.</span></span>

</dd> <dt>

<span data-ttu-id="b3c02-123">*height* (高度)</span><span class="sxs-lookup"><span data-stu-id="b3c02-123">*height*</span></span> 
</dt> <dd>

<span data-ttu-id="b3c02-124">材質子影像的高度。</span><span class="sxs-lookup"><span data-stu-id="b3c02-124">The height of the texture sub-image.</span></span>

</dd> <dt>

<span data-ttu-id="b3c02-125">*format*</span><span class="sxs-lookup"><span data-stu-id="b3c02-125">*format*</span></span> 
</dt> <dd>

<span data-ttu-id="b3c02-126">圖元資料的格式。</span><span class="sxs-lookup"><span data-stu-id="b3c02-126">The format of the pixel data.</span></span> <span data-ttu-id="b3c02-127">它可以採用下列其中一個符號值。</span><span class="sxs-lookup"><span data-stu-id="b3c02-127">It can assume one of the following symbolic values.</span></span>



| <span data-ttu-id="b3c02-128">值</span><span class="sxs-lookup"><span data-stu-id="b3c02-128">Value</span></span>                                                                                                                                                                         | <span data-ttu-id="b3c02-129">意義</span><span class="sxs-lookup"><span data-stu-id="b3c02-129">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_COLOR_INDEX"></span><span id="gl_color_index"></span><dl> <span data-ttu-id="b3c02-130"><dt>**GL \_ 色彩 \_ 索引**</dt></span><span class="sxs-lookup"><span data-stu-id="b3c02-130"><dt>**GL\_COLOR\_INDEX**</dt></span></span> </dl>             | <span data-ttu-id="b3c02-131">每個元素都是單一值，也就是色彩索引。</span><span class="sxs-lookup"><span data-stu-id="b3c02-131">Each element is a single value, a color index.</span></span> <span data-ttu-id="b3c02-132">它會轉換成固定點格式 (在二進位點的右邊有未指定的0位位數) 、向左或向右移動，視 GL 索引移位的值和正負號而定， \_ \_ 然後新增至 gl \_ 索引 \_ 位移 (查看 [**glPixelTransfer**](glpixeltransfer.md)) 。</span><span class="sxs-lookup"><span data-stu-id="b3c02-132">It is converted to fixed point format (with an unspecified number of 0 bits to the right of the binary point), shifted left or right, depending on the value and sign of GL\_INDEX\_SHIFT, and added to GL\_INDEX\_OFFSET (see [**glPixelTransfer**](glpixeltransfer.md)).</span></span> <span data-ttu-id="b3c02-133">產生的索引會使用 GL \_ 圖元 \_ 地圖 \_ i \_ 到 \_ R、gl \_ 圖元 \_ 地圖 \_ i \_ 到 \_ G、gl \_ 圖元 \_ 地圖 \_ i \_ 到 \_ B，以及 gl \_ 圖元 \_ 對應 \_ i 至 \_ \_ 資料表，並壓制至範圍 \[ 0，1 \] ，轉換成一組色彩元件。</span><span class="sxs-lookup"><span data-stu-id="b3c02-133">The resulting index is converted to a set of color components using the GL\_PIXEL\_MAP\_I\_TO\_R, GL\_PIXEL\_MAP\_I\_TO\_G, GL\_PIXEL\_MAP\_I\_TO\_B, and GL\_PIXEL\_MAP\_I\_TO\_A tables, and clamped to the range \[0,1\].</span></span><br/> |
| <span id="GL_RED"></span><span id="gl_red"></span><dl> <span data-ttu-id="b3c02-134"><dt>**GL \_ 紅色**</dt></span><span class="sxs-lookup"><span data-stu-id="b3c02-134"><dt>**GL\_RED**</dt></span></span> </dl>                                      | <span data-ttu-id="b3c02-135">每個元素都是單一的紅色元件。</span><span class="sxs-lookup"><span data-stu-id="b3c02-135">Each element is a single red component.</span></span> <span data-ttu-id="b3c02-136">它會轉換為浮點格式並組合成 RGBA 元素，方法是附加0.0 （適用于綠色和藍色）和1.0 （Alpha）。</span><span class="sxs-lookup"><span data-stu-id="b3c02-136">It is converted to floating point format and assembled into an RGBA element by attaching 0.0 for green and blue, and 1.0 for alpha.</span></span> <span data-ttu-id="b3c02-137">接著，每個元件會乘以已簽署的縮放比例 GL \_ c \_ 規模、新增至帶正負號偏差 gl \_ c \_ 偏差，然後壓制至範圍 \[ 0，1 \] (查看 **glPixelTransfer**) 。</span><span class="sxs-lookup"><span data-stu-id="b3c02-137">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see **glPixelTransfer**).</span></span><br/>                                                                                                                                                                                                |
| <span id="GL_GREEN"></span><span id="gl_green"></span><dl> <span data-ttu-id="b3c02-138"><dt>**GL \_ 綠**</dt></span><span class="sxs-lookup"><span data-stu-id="b3c02-138"><dt>**GL\_GREEN**</dt></span></span> </dl>                                | <span data-ttu-id="b3c02-139">每個元素都是一個綠色的元件。</span><span class="sxs-lookup"><span data-stu-id="b3c02-139">Each element is a single green component.</span></span> <span data-ttu-id="b3c02-140">它會轉換成浮點數格式並組合成 RGBA 元素，方法是附加0.0 （紅色和藍色）和1.0 （Alpha）。</span><span class="sxs-lookup"><span data-stu-id="b3c02-140">It is converted to floating point format and assembled into an RGBA element by attaching 0.0 for red and blue, and 1.0 for alpha.</span></span> <span data-ttu-id="b3c02-141">接著，每個元件會乘以已簽署的縮放比例 GL \_ c \_ 規模、新增至帶正負號偏差 gl \_ c \_ 偏差，然後壓制至範圍 \[ 0，1 \] (查看 [**glPixelTransfer**](glpixeltransfer.md)) 。</span><span class="sxs-lookup"><span data-stu-id="b3c02-141">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see [**glPixelTransfer**](glpixeltransfer.md)).</span></span><br/>                                                                                                                                                                         |
| <span id="GL_BLUE"></span><span id="gl_blue"></span><dl> <span data-ttu-id="b3c02-142"><dt>**GL \_ 藍色**</dt></span><span class="sxs-lookup"><span data-stu-id="b3c02-142"><dt>**GL\_BLUE**</dt></span></span> </dl>                                   | <span data-ttu-id="b3c02-143">每個元素都是單一藍色元件。</span><span class="sxs-lookup"><span data-stu-id="b3c02-143">Each element is a single blue component.</span></span> <span data-ttu-id="b3c02-144">它會轉換成浮點數格式並組合成 RGBA 元素，方法是附加0.0 （紅色和綠色）和1.0 （Alpha）。</span><span class="sxs-lookup"><span data-stu-id="b3c02-144">It is converted to floating point format and assembled into an RGBA element by attaching 0.0 for red and green, and 1.0 for alpha.</span></span> <span data-ttu-id="b3c02-145">接著，每個元件會乘以已簽署的縮放比例 GL \_ c \_ 規模、新增至帶正負號偏差 gl \_ c \_ 偏差，然後壓制至範圍 \[ 0，1 \] (查看 **glPixelTransfer**) 。</span><span class="sxs-lookup"><span data-stu-id="b3c02-145">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see **glPixelTransfer**).</span></span><br/>                                                                                                                                                                                                |
| <span id="GL_ALPHA"></span><span id="gl_alpha"></span><dl> <span data-ttu-id="b3c02-146"><dt>**GL \_ ALPHA**</dt></span><span class="sxs-lookup"><span data-stu-id="b3c02-146"><dt>**GL\_ALPHA**</dt></span></span> </dl>                                | <span data-ttu-id="b3c02-147">每個元素都是單一 Alpha 元件。</span><span class="sxs-lookup"><span data-stu-id="b3c02-147">Each element is a single alpha component.</span></span> <span data-ttu-id="b3c02-148">它會轉換成浮點數格式，並藉由附加0.0 的紅色、綠色和藍色來組合成 RGBA 元素。</span><span class="sxs-lookup"><span data-stu-id="b3c02-148">It is converted to floating point format and assembled into an RGBA element by attaching 0.0 for red, green, and blue.</span></span> <span data-ttu-id="b3c02-149">接著，每個元件會乘以已簽署的縮放比例 GL \_ c \_ 規模、新增至帶正負號偏差 gl \_ c \_ 偏差，然後壓制至範圍 \[ 0，1 \] (查看 [**glPixelTransfer**](glpixeltransfer.md)) 。</span><span class="sxs-lookup"><span data-stu-id="b3c02-149">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see [**glPixelTransfer**](glpixeltransfer.md)).</span></span><br/>                                                                                                                                                                                    |
| <span id="GL_RGB"></span><span id="gl_rgb"></span><dl> <span data-ttu-id="b3c02-150"><dt>**GL \_ RGB**</dt></span><span class="sxs-lookup"><span data-stu-id="b3c02-150"><dt>**GL\_RGB**</dt></span></span> </dl>                                      | <span data-ttu-id="b3c02-151">每個元素都是 RGB 三重。</span><span class="sxs-lookup"><span data-stu-id="b3c02-151">Each element is an RGB triple.</span></span> <span data-ttu-id="b3c02-152">它會轉換成浮點數格式，並藉由附加1.0 的 Alpha 來組合成 RGBA 元素。</span><span class="sxs-lookup"><span data-stu-id="b3c02-152">It is converted to floating point format and assembled into an RGBA element by attaching 1.0 for alpha.</span></span> <span data-ttu-id="b3c02-153">接著，每個元件會乘以已簽署的縮放比例 GL \_ c \_ 規模、新增至帶正負號偏差 gl \_ c \_ 偏差，然後壓制至範圍 \[ 0，1 \] (查看 **glPixelTransfer**) 。</span><span class="sxs-lookup"><span data-stu-id="b3c02-153">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see **glPixelTransfer**).</span></span><br/>                                                                                                                                                                                                                                     |
| <span id="GL_RGBA"></span><span id="gl_rgba"></span><dl> <span data-ttu-id="b3c02-154"><dt>**GL \_ RGBA**</dt></span><span class="sxs-lookup"><span data-stu-id="b3c02-154"><dt>**GL\_RGBA**</dt></span></span> </dl>                                   | <span data-ttu-id="b3c02-155">每個元素都是完整的 RGBA 元素。</span><span class="sxs-lookup"><span data-stu-id="b3c02-155">Each element is a complete RGBA element.</span></span> <span data-ttu-id="b3c02-156">它會轉換成浮點數。</span><span class="sxs-lookup"><span data-stu-id="b3c02-156">It is converted to floating point.</span></span> <span data-ttu-id="b3c02-157">接著，每個元件會乘以已簽署的縮放比例 GL \_ c \_ 規模、新增至帶正負號偏差 gl \_ c \_ 偏差，然後壓制至範圍 \[ 0，1 \] (查看 **glPixelTransfer**) 。</span><span class="sxs-lookup"><span data-stu-id="b3c02-157">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see **glPixelTransfer**).</span></span><br/>                                                                                                                                                                                                                                                                                                |
| <span id="GL_LUMINANCE"></span><span id="gl_luminance"></span><dl> <span data-ttu-id="b3c02-158"><dt>**GL \_ 亮度**</dt></span><span class="sxs-lookup"><span data-stu-id="b3c02-158"><dt>**GL\_LUMINANCE**</dt></span></span> </dl>                    | <span data-ttu-id="b3c02-159">每個元素都是單一的亮度值。</span><span class="sxs-lookup"><span data-stu-id="b3c02-159">Each element is a single luminance value.</span></span> <span data-ttu-id="b3c02-160">它會轉換成浮點數格式，然後將亮度值複寫三次（針對紅色、綠色和藍色），然後附加1.0 （Alpha），以組合成 RGBA 元素。</span><span class="sxs-lookup"><span data-stu-id="b3c02-160">It is converted to floating point format, and then assembled into an RGBA element by replicating the luminance value three times for red, green, and blue, and attaching 1.0 for alpha.</span></span> <span data-ttu-id="b3c02-161">接著，每個元件會乘以已簽署的縮放比例 GL \_ c \_ 規模、新增至帶正負號偏差 gl \_ c \_ 偏差，然後壓制至範圍 \[ 0，1 \] (查看 [**glPixelTransfer**](glpixeltransfer.md)) 。</span><span class="sxs-lookup"><span data-stu-id="b3c02-161">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see [**glPixelTransfer**](glpixeltransfer.md)).</span></span><br/>                                                                                                                   |
| <span id="GL_LUMINANCE_ALPHA"></span><span id="gl_luminance_alpha"></span><dl> <span data-ttu-id="b3c02-162"><dt>**GL \_ 亮度 \_ ALPHA**</dt></span><span class="sxs-lookup"><span data-stu-id="b3c02-162"><dt>**GL\_LUMINANCE\_ALPHA**</dt></span></span> </dl> | <span data-ttu-id="b3c02-163">每個元素都是一組明亮度/Alpha 配對。</span><span class="sxs-lookup"><span data-stu-id="b3c02-163">Each element is a luminance/alpha pair.</span></span> <span data-ttu-id="b3c02-164">它會轉換為浮點格式，然後藉由針對紅色、綠色和藍色複寫亮度值三次，來組合成 RGBA 元素。</span><span class="sxs-lookup"><span data-stu-id="b3c02-164">It is converted to floating point format, and then assembled into an RGBA element by replicating the luminance value three times for red, green, and blue.</span></span> <span data-ttu-id="b3c02-165">接著，每個元件會乘以已簽署的縮放比例 GL \_ c \_ 規模、新增至帶正負號偏差 gl \_ c \_ 偏差，然後壓制至範圍 \[ 0，1 \] (查看 **glPixelTransfer**) 。</span><span class="sxs-lookup"><span data-stu-id="b3c02-165">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see **glPixelTransfer**).</span></span><br/>                                                                                                                                                                         |



 

</dd> <dt>

<span data-ttu-id="b3c02-166">*type*</span><span class="sxs-lookup"><span data-stu-id="b3c02-166">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="b3c02-167">圖元資料的資料類型。</span><span class="sxs-lookup"><span data-stu-id="b3c02-167">The data type of the pixel data.</span></span> <span data-ttu-id="b3c02-168">接受下列符號值： GL \_ 未簽署 \_ 位元組、gl \_ 位元組、GL \_ 點陣圖、gl \_ 未簽署 \_ 短、gl \_ 簡短、GL 不 \_ 帶正負號 \_ int、GL \_ int 和 gl \_ FLOAT。</span><span class="sxs-lookup"><span data-stu-id="b3c02-168">The following symbolic values are accepted: GL\_UNSIGNED\_BYTE, GL\_BYTE, GL\_BITMAP, GL\_UNSIGNED\_SHORT, GL\_SHORT, GL\_UNSIGNED\_INT, GL\_INT, and GL\_FLOAT.</span></span>

</dd> <dt>

<span data-ttu-id="b3c02-169">*圖元*</span><span class="sxs-lookup"><span data-stu-id="b3c02-169">*pixels*</span></span> 
</dt> <dd>

<span data-ttu-id="b3c02-170">記憶體中影像資料的指標。</span><span class="sxs-lookup"><span data-stu-id="b3c02-170">A pointer to the image data in memory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3c02-171">傳回值</span><span class="sxs-lookup"><span data-stu-id="b3c02-171">Return value</span></span>

<span data-ttu-id="b3c02-172">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="b3c02-172">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b3c02-173">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="b3c02-173">Error codes</span></span>

<span data-ttu-id="b3c02-174">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="b3c02-174">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="b3c02-175">Name</span><span class="sxs-lookup"><span data-stu-id="b3c02-175">Name</span></span>                                                                                                  | <span data-ttu-id="b3c02-176">意義</span><span class="sxs-lookup"><span data-stu-id="b3c02-176">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b3c02-177"><dt>**GL \_ 無效 \_ 列舉**</dt></span><span class="sxs-lookup"><span data-stu-id="b3c02-177"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="b3c02-178">*目標* 不是 GL \_ 紋理 \_ 2d。</span><span class="sxs-lookup"><span data-stu-id="b3c02-178">*target* was not GL\_TEXTURE\_2D.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                 |
| <dl> <span data-ttu-id="b3c02-179"><dt>**GL \_ 無效 \_ 列舉**</dt></span><span class="sxs-lookup"><span data-stu-id="b3c02-179"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="b3c02-180">*格式* 不是可接受的常數。</span><span class="sxs-lookup"><span data-stu-id="b3c02-180">*format* was not an accepted constant.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <span data-ttu-id="b3c02-181"><dt>**GL \_ 無效 \_ 列舉**</dt></span><span class="sxs-lookup"><span data-stu-id="b3c02-181"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="b3c02-182">*類型* 不是可接受的常數。</span><span class="sxs-lookup"><span data-stu-id="b3c02-182">*type* was not an accepted constant.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                              |
| <dl> <span data-ttu-id="b3c02-183"><dt>**GL \_ 無效 \_ 列舉**</dt></span><span class="sxs-lookup"><span data-stu-id="b3c02-183"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="b3c02-184">*類型* 為 gl \_ 點陣圖， *格式* 不是 gl \_ 色彩 \_ 索引。</span><span class="sxs-lookup"><span data-stu-id="b3c02-184">*type* was GL\_BITMAP and *format* was not GL\_COLOR\_INDEX.</span></span><br/>                                                                                                                                                                                                                                                                                                                                      |
| <dl> <span data-ttu-id="b3c02-185"><dt>**GL \_ 無效 \_ 值**</dt></span><span class="sxs-lookup"><span data-stu-id="b3c02-185"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="b3c02-186">*層級* 小於零或大於 log2 *max*，其中 *max* 是 GL \_ 最大紋理大小的傳回值 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="b3c02-186">*level* was less than zero or greater than log2 *max*, where *max* was the returned value of GL\_MAX\_TEXTURE\_SIZE.</span></span><br/>                                                                                                                                                                                                                                                                              |
| <dl> <span data-ttu-id="b3c02-187"><dt>**GL \_ 無效 \_ 值**</dt></span><span class="sxs-lookup"><span data-stu-id="b3c02-187"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="b3c02-188">*xoffset* 小於-*b*;或 *xoffset*  +  *寬度* 大於 *w*  -  *b*; 或 *yoffset* 小於-*b*; 或 *yoffset*  +  *高度* 大於 *h*  -  *b*，其中 *w* 是 gl \_ 材質 \_ 寬度， *h* 是 gl \_ 材質 \_ 高度，而 *b* 則是 \_ \_ 要修改之紋理影像的 GL 紋理框線寬度。</span><span class="sxs-lookup"><span data-stu-id="b3c02-188">*xoffset* was less than -*b*; or *xoffset* + *width* was greater than *w* - *b*; or *yoffset* was less than -*b*; or *yoffset* + *height* was greater than *h* - *b*, where *w* is the GL\_TEXTURE\_WIDTH, *h* is the GL\_TEXTURE\_HEIGHT, and *b* is the width of the GL\_TEXTURE\_BORDER of the texture image being modified.</span></span> <br/> <span data-ttu-id="b3c02-189">請注意， *w* 和 *h* 包含框線寬度的兩倍。</span><span class="sxs-lookup"><span data-stu-id="b3c02-189">Note that *w* and *h* include twice the border width.</span></span><br/> |
| <dl> <span data-ttu-id="b3c02-190"><dt>**GL \_ 無效 \_ 值**</dt></span><span class="sxs-lookup"><span data-stu-id="b3c02-190"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="b3c02-191">*寬度* 小於 *b*，其中 *b* 是材質陣列的框線寬度。</span><span class="sxs-lookup"><span data-stu-id="b3c02-191">*width* was was less than *b*, where *b* is the border width of the texture array.</span></span><br/>                                                                                                                                                                                                                                                                                                                |
| <dl> <span data-ttu-id="b3c02-192"><dt>**GL \_ 無效 \_ 值**</dt></span><span class="sxs-lookup"><span data-stu-id="b3c02-192"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="b3c02-193">*框線* 不是零或1。</span><span class="sxs-lookup"><span data-stu-id="b3c02-193">*border* was not zero or 1.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                       |
| <dl> <span data-ttu-id="b3c02-194"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="b3c02-194"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="b3c02-195">材質陣列未由先前的 **glTexImage2D** 作業定義。</span><span class="sxs-lookup"><span data-stu-id="b3c02-195">The texture array was not defined by a previous **glTexImage2D** operation.</span></span><br/>                                                                                                                                                                                                                                                                                                                       |
| <dl> <span data-ttu-id="b3c02-196"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="b3c02-196"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="b3c02-197">呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。</span><span class="sxs-lookup"><span data-stu-id="b3c02-197">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/>                                                                                                                                                                                                                                                                        |



## <a name="remarks"></a><span data-ttu-id="b3c02-198">備註</span><span class="sxs-lookup"><span data-stu-id="b3c02-198">Remarks</span></span>

<span data-ttu-id="b3c02-199">使用 [**glEnable**](glenable.md) 和 **glDisable** 搭配引數 GL 材質2d，可啟用基本的二維紋理 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="b3c02-199">Two-dimensional texturing for a primitive is enabled using [**glEnable**](glenable.md) and **glDisable** with the argument GL\_TEXTURE\_2D.</span></span> <span data-ttu-id="b3c02-200">在紋理期間，指定之材質影像的一部分會對應到每個已啟用的基本類型。</span><span class="sxs-lookup"><span data-stu-id="b3c02-200">During texturing, part of a specified texture image is mapped into each enabled primitive.</span></span> <span data-ttu-id="b3c02-201">您可以使用 **glTexSubImage2D** 函式來指定用於紋理的現有二維紋理影像的連續子影像。</span><span class="sxs-lookup"><span data-stu-id="b3c02-201">You use the **glTexSubImage2D** function to specify a contiguous sub-image of an existing two-dimensional texture image for texturing.</span></span>

<span data-ttu-id="b3c02-202">*圖元* 所參考的材質會將現有材質陣列的區域 *取代為* *xoffset* 和 *xoffset* + (*寬度* 1) 內含和 *y* 索引（ *yoffset* 和 *yoffset* + (*高度* 1) 包含）。</span><span class="sxs-lookup"><span data-stu-id="b3c02-202">The texels referenced by *pixels* replace a region of the existing texture array with *x* indexes of *xoffset* and *xoffset* + (*width* 1) inclusive and *y* indexes of *yoffset* and *yoffset* + (*height* 1) inclusive.</span></span> <span data-ttu-id="b3c02-203">此區域無法在原始指定的材質陣列範圍之外包含任何材質。</span><span class="sxs-lookup"><span data-stu-id="b3c02-203">This region cannot include any texels outside the range of the originally specified texture array.</span></span>

<span data-ttu-id="b3c02-204">指定 *寬度* 為零的子影像沒有任何作用，也不會產生錯誤。</span><span class="sxs-lookup"><span data-stu-id="b3c02-204">Specifying a sub-image with a *width* of zero has no effect and does not generate an error.</span></span>

<span data-ttu-id="b3c02-205">紋理在色彩索引模式中沒有任何作用。</span><span class="sxs-lookup"><span data-stu-id="b3c02-205">Texturing has no effect in color-index mode.</span></span>

<span data-ttu-id="b3c02-206">一般而言，材質影像可以用與 [**glDrawPixels**](gldrawpixels.md) 命令中的圖元相同的資料格式表示，但 \_ 無法使用 gl 樣板 \_ 索引和 gl \_ 深度 \_ 元件。</span><span class="sxs-lookup"><span data-stu-id="b3c02-206">In general, texture images can be represented by the same data formats as the pixels in a [**glDrawPixels**](gldrawpixels.md) command, except that GL\_STENCIL\_INDEX and GL\_DEPTH\_COMPONENT cannot be used.</span></span> <span data-ttu-id="b3c02-207">[**GlPixelStore**](glpixelstore-functions.md)和 [**glPixelTransfer**](glpixeltransfer.md)模式會以其影響 **glDrawPixels** 的確切方式來影響紋理影像。</span><span class="sxs-lookup"><span data-stu-id="b3c02-207">The [**glPixelStore**](glpixelstore-functions.md) and [**glPixelTransfer**](glpixeltransfer.md) modes affect texture images in exactly the way they affect **glDrawPixels**.</span></span>

<span data-ttu-id="b3c02-208">下列函式會取出與 **glTexSubImage2D** 相關的資訊：</span><span class="sxs-lookup"><span data-stu-id="b3c02-208">The following functions retrieve information related to **glTexSubImage2D**:</span></span>

[<span data-ttu-id="b3c02-209">**glGetTexImage**</span><span class="sxs-lookup"><span data-stu-id="b3c02-209">**glGetTexImage**</span></span>](glgetteximage.md)

<span data-ttu-id="b3c02-210">[](glisenabled.md)具有引數 GL \_ 材質 \_ 2d 的 glIsEnabled</span><span class="sxs-lookup"><span data-stu-id="b3c02-210">[**glIsEnabled**](glisenabled.md) with argument GL\_TEXTURE\_2D</span></span>

## <a name="requirements"></a><span data-ttu-id="b3c02-211">規格需求</span><span class="sxs-lookup"><span data-stu-id="b3c02-211">Requirements</span></span>



| <span data-ttu-id="b3c02-212">需求</span><span class="sxs-lookup"><span data-stu-id="b3c02-212">Requirement</span></span> | <span data-ttu-id="b3c02-213">值</span><span class="sxs-lookup"><span data-stu-id="b3c02-213">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b3c02-214">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b3c02-214">Minimum supported client</span></span><br/> | <span data-ttu-id="b3c02-215">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b3c02-215">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="b3c02-216">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b3c02-216">Minimum supported server</span></span><br/> | <span data-ttu-id="b3c02-217">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b3c02-217">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b3c02-218">標頭</span><span class="sxs-lookup"><span data-stu-id="b3c02-218">Header</span></span><br/>                   | <dl> <span data-ttu-id="b3c02-219"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="b3c02-219"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="b3c02-220">程式庫</span><span class="sxs-lookup"><span data-stu-id="b3c02-220">Library</span></span><br/>                  | <dl> <span data-ttu-id="b3c02-221"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="b3c02-221"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="b3c02-222">DLL</span><span class="sxs-lookup"><span data-stu-id="b3c02-222">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b3c02-223"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b3c02-223"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3c02-224">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b3c02-224">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3c02-225">**glCopyTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="b3c02-225">**glCopyTexImage1D**</span></span>](glcopyteximage1d.md)
</dt> <dt>

[<span data-ttu-id="b3c02-226">**glCopyTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="b3c02-226">**glCopyTexImage2D**</span></span>](glcopyteximage2d.md)
</dt> <dt>

[<span data-ttu-id="b3c02-227">**glCopyTexSubImage1D**</span><span class="sxs-lookup"><span data-stu-id="b3c02-227">**glCopyTexSubImage1D**</span></span>](glcopytexsubimage1d.md)
</dt> <dt>

[<span data-ttu-id="b3c02-228">**glCopyTexSubImage2D**</span><span class="sxs-lookup"><span data-stu-id="b3c02-228">**glCopyTexSubImage2D**</span></span>](glcopytexsubimage2d.md)
</dt> <dt>

[<span data-ttu-id="b3c02-229">**glDrawPixels**</span><span class="sxs-lookup"><span data-stu-id="b3c02-229">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="b3c02-230">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="b3c02-230">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="b3c02-231">**glFog**</span><span class="sxs-lookup"><span data-stu-id="b3c02-231">**glFog**</span></span>](glfog.md)
</dt> <dt>

[<span data-ttu-id="b3c02-232">**glGetTexImage**</span><span class="sxs-lookup"><span data-stu-id="b3c02-232">**glGetTexImage**</span></span>](glgetteximage.md)
</dt> <dt>

[<span data-ttu-id="b3c02-233">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="b3c02-233">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="b3c02-234">**glPixelStore**</span><span class="sxs-lookup"><span data-stu-id="b3c02-234">**glPixelStore**</span></span>](glpixelstore-functions.md)
</dt> <dt>

[<span data-ttu-id="b3c02-235">**glPixelTransfer**</span><span class="sxs-lookup"><span data-stu-id="b3c02-235">**glPixelTransfer**</span></span>](glpixeltransfer.md)
</dt> <dt>

[<span data-ttu-id="b3c02-236">**glTexEnv**</span><span class="sxs-lookup"><span data-stu-id="b3c02-236">**glTexEnv**</span></span>](gltexenv-functions.md)
</dt> <dt>

[<span data-ttu-id="b3c02-237">**glTexGen**</span><span class="sxs-lookup"><span data-stu-id="b3c02-237">**glTexGen**</span></span>](gltexgen-functions.md)
</dt> <dt>

[<span data-ttu-id="b3c02-238">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="b3c02-238">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="b3c02-239">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="b3c02-239">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="b3c02-240">**glTexSubImage1D**</span><span class="sxs-lookup"><span data-stu-id="b3c02-240">**glTexSubImage1D**</span></span>](gltexsubimage1d.md)
</dt> <dt>

[<span data-ttu-id="b3c02-241">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="b3c02-241">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="b3c02-242">**glTexParameter**</span><span class="sxs-lookup"><span data-stu-id="b3c02-242">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> </dl>

 

 





