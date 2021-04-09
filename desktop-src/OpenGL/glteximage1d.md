---
title: 'glTexImage1D 函式 (Gl) '
description: GlTexImage1D 函式會指定一維紋理影像。
ms.assetid: 4f537b89-2ea2-4e2e-8c57-c372bf53f12c
keywords:
- glTexImage1D 函式 OpenGL
topic_type:
- apiref
api_name:
- glTexImage1D
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1865d19c54b9c59654f07162d2480aa5b29c47f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024965"
---
# <a name="glteximage1d-function"></a><span data-ttu-id="7e64c-104">glTexImage1D 函式</span><span class="sxs-lookup"><span data-stu-id="7e64c-104">glTexImage1D function</span></span>

<span data-ttu-id="7e64c-105">**GlTexImage1D** 函式會指定一維紋理影像。</span><span class="sxs-lookup"><span data-stu-id="7e64c-105">The **glTexImage1D** function specifies a one-dimensional texture image.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e64c-106">語法</span><span class="sxs-lookup"><span data-stu-id="7e64c-106">Syntax</span></span>


```C++
void WINAPI glTexImage1D(
         GLenum  target,
         GLint   level,
         GLint   internalformat,
         GLsizei width,
         GLint   border,
         GLint   format,
         GLenum  type,
   const GLvoid  *pixels
);
```



## <a name="parameters"></a><span data-ttu-id="7e64c-107">參數</span><span class="sxs-lookup"><span data-stu-id="7e64c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e64c-108">*目標*</span><span class="sxs-lookup"><span data-stu-id="7e64c-108">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="7e64c-109">目標材質。</span><span class="sxs-lookup"><span data-stu-id="7e64c-109">The target texture.</span></span> <span data-ttu-id="7e64c-110">必須是 GL \_ 紋理 \_ 1d。</span><span class="sxs-lookup"><span data-stu-id="7e64c-110">Must be GL\_TEXTURE\_1D.</span></span>

</dd> <dt>

<span data-ttu-id="7e64c-111">*level*</span><span class="sxs-lookup"><span data-stu-id="7e64c-111">*level*</span></span> 
</dt> <dd>

<span data-ttu-id="7e64c-112">詳細資料層級數目。</span><span class="sxs-lookup"><span data-stu-id="7e64c-112">The level-of-detail number.</span></span> <span data-ttu-id="7e64c-113">層級0是基底映射層級。</span><span class="sxs-lookup"><span data-stu-id="7e64c-113">Level 0 is the base image level.</span></span> <span data-ttu-id="7e64c-114">層級 *n* 是第 *n* 個 mipmap 縮減影像。</span><span class="sxs-lookup"><span data-stu-id="7e64c-114">Level *n* is the *n* Th mipmap reduction image.</span></span>

</dd> <dt>

<span data-ttu-id="7e64c-115">*internalformat*</span><span class="sxs-lookup"><span data-stu-id="7e64c-115">*internalformat*</span></span> 
</dt> <dd>

<span data-ttu-id="7e64c-116">指定材質中的色彩元件數目。</span><span class="sxs-lookup"><span data-stu-id="7e64c-116">Specifies the number of color components in the texture.</span></span> <span data-ttu-id="7e64c-117">必須是1、2、3或4，或下列其中一個符號常數： GL \_ ALPHA、gl \_ ALPHA4、gl \_ ALPHA8、GL \_ ALPHA12、gl \_ ALPHA16、gl \_ 亮度、gl \_ LUMINANCE4、gl LUMINANCE8、gl LUMINANCE12、GL LUMINANCE16、gl \_ \_ \_ \_ 亮度 \_ ALPHA、gl LUMINANCE4 ALPHA4、GL LUMINANCE6 ALPHA2 \_ \_ \_ \_ 、GL \_ LUMINANCE8 ALPHA8、gl LUMINANCE12 \_ \_ \_ ALPHA4、GL \_ LUMINANCE12 \_ ALPHA12、GL \_ LUMINANCE16 \_ ALPHA16、gl \_ 濃度、gl \_ INTENSITY4、gl \_ INTENSITY8、gl \_ INTENSITY12、gl \_ INTENSITY16、gl \_ RGB、gl \_ R3 G3 B2 \_ \_ 、 \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ gl RGB4、gl RGB5、gl RGB8、gl RGB10、gl RGB12、gl RGB16、gl RGBA、gl RGBA2、gl RGBA4、gl RGB5、gl RGBA8、gl RGB10、gl RGBA12 或 gl RGBA16。</span><span class="sxs-lookup"><span data-stu-id="7e64c-117">Must be 1, 2, 3, or 4, or one of the following symbolic constants: GL\_ALPHA, GL\_ALPHA4, GL\_ALPHA8, GL\_ALPHA12, GL\_ALPHA16, GL\_LUMINANCE, GL\_LUMINANCE4, GL\_LUMINANCE8, GL\_LUMINANCE12, GL\_LUMINANCE16, GL\_LUMINANCE\_ALPHA, GL\_LUMINANCE4\_ALPHA4, GL\_LUMINANCE6\_ALPHA2, GL\_LUMINANCE8\_ALPHA8, GL\_LUMINANCE12\_ALPHA4, GL\_LUMINANCE12\_ALPHA12, GL\_LUMINANCE16\_ALPHA16, GL\_INTENSITY, GL\_INTENSITY4, GL\_INTENSITY8, GL\_INTENSITY12, GL\_INTENSITY16, GL\_RGB, GL\_R3\_G3\_B2, GL\_RGB4, GL\_RGB5, GL\_RGB8, GL\_RGB10, GL\_RGB12, GL\_RGB16, GL\_RGBA, GL\_RGBA2, GL\_RGBA4, GL\_RGB5\_A1, GL\_RGBA8, GL\_RGB10\_A2, GL\_RGBA12, or GL\_RGBA16.</span></span>

</dd> <dt>

<span data-ttu-id="7e64c-118">*width* (寬度)</span><span class="sxs-lookup"><span data-stu-id="7e64c-118">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="7e64c-119">材質影像的寬度。</span><span class="sxs-lookup"><span data-stu-id="7e64c-119">The width of the texture image.</span></span> <span data-ttu-id="7e64c-120">必須為一個整數 *n* 的 2 *n* + 2 (*框線*) 。</span><span class="sxs-lookup"><span data-stu-id="7e64c-120">Must be 2 *n* + 2( *border* ) for some integer *n*.</span></span> <span data-ttu-id="7e64c-121">材質影像的高度為1。</span><span class="sxs-lookup"><span data-stu-id="7e64c-121">The height of the texture image is 1.</span></span>

</dd> <dt>

<span data-ttu-id="7e64c-122">*邊境*</span><span class="sxs-lookup"><span data-stu-id="7e64c-122">*border*</span></span> 
</dt> <dd>

<span data-ttu-id="7e64c-123">框線的寬度。</span><span class="sxs-lookup"><span data-stu-id="7e64c-123">The width of the border.</span></span> <span data-ttu-id="7e64c-124">必須是0或1。</span><span class="sxs-lookup"><span data-stu-id="7e64c-124">Must be either 0 or 1.</span></span>

</dd> <dt>

<span data-ttu-id="7e64c-125">*format*</span><span class="sxs-lookup"><span data-stu-id="7e64c-125">*format*</span></span> 
</dt> <dd>

<span data-ttu-id="7e64c-126">圖元資料的格式。</span><span class="sxs-lookup"><span data-stu-id="7e64c-126">The format of the pixel data.</span></span> <span data-ttu-id="7e64c-127">它可以假設有九個符號值的其中一個。</span><span class="sxs-lookup"><span data-stu-id="7e64c-127">It can assume one of nine symbolic values.</span></span>



| <span data-ttu-id="7e64c-128">值</span><span class="sxs-lookup"><span data-stu-id="7e64c-128">Value</span></span>                                                                                                                                                                         | <span data-ttu-id="7e64c-129">意義</span><span class="sxs-lookup"><span data-stu-id="7e64c-129">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_COLOR_INDEX"></span><span id="gl_color_index"></span><dl> <span data-ttu-id="7e64c-130"><dt>**GL \_ 色彩 \_ 索引**</dt></span><span class="sxs-lookup"><span data-stu-id="7e64c-130"><dt>**GL\_COLOR\_INDEX**</dt></span></span> </dl>             | <span data-ttu-id="7e64c-131">每個元素都是單一值，也就是色彩索引。</span><span class="sxs-lookup"><span data-stu-id="7e64c-131">Each element is a single value, a color index.</span></span> <span data-ttu-id="7e64c-132">它會轉換成固定點 (，並在二進位點的右邊指定0位不指定的位數) 、向左或向右移動，視 GL 索引移位的值和正負號而定， \_ \_ 然後新增至 gl \_ 索引 \_ 位移 (查看 [**glPixelTransfer**](glpixeltransfer.md)) 。</span><span class="sxs-lookup"><span data-stu-id="7e64c-132">It is converted to fixed point (with an unspecified number of 0 bits to the right of the binary point), shifted left or right, depending on the value and sign of GL\_INDEX\_SHIFT, and added to GL\_INDEX\_OFFSET (see [**glPixelTransfer**](glpixeltransfer.md)).</span></span> <span data-ttu-id="7e64c-133">產生的索引會使用 GL \_ 圖元 \_ 地圖 \_ i \_ 到 \_ R、gl \_ 圖元 \_ 地圖 \_ i \_ 到 \_ G、gl \_ 圖元 \_ 地圖 \_ i \_ 到 \_ B，以及 gl \_ 圖元 \_ 對應 \_ i 至 \_ \_ 資料表，並壓制至範圍 \[ 0，1 \] ，轉換成一組色彩元件。</span><span class="sxs-lookup"><span data-stu-id="7e64c-133">The resulting index is converted to a set of color components using the GL\_PIXEL\_MAP\_I\_TO\_R, GL\_PIXEL\_MAP\_I\_TO\_G, GL\_PIXEL\_MAP\_I\_TO\_B, and GL\_PIXEL\_MAP\_I\_TO\_A tables, and clamped to the range \[0,1\].</span></span><br/> |
| <span id="GL_RED"></span><span id="gl_red"></span><dl> <span data-ttu-id="7e64c-134"><dt>**GL \_ 紅色**</dt></span><span class="sxs-lookup"><span data-stu-id="7e64c-134"><dt>**GL\_RED**</dt></span></span> </dl>                                      | <span data-ttu-id="7e64c-135">每個元素都是單一的紅色元件。</span><span class="sxs-lookup"><span data-stu-id="7e64c-135">Each element is a single red component.</span></span> <span data-ttu-id="7e64c-136">它會轉換成浮點數，並藉由附加適用于綠色和藍色的0.0，以及適用于 Alpha 的1.0，組合成 RGBA 元素。</span><span class="sxs-lookup"><span data-stu-id="7e64c-136">It is converted to floating point and assembled into an RGBA element by attaching 0.0 for green and blue, and 1.0 for alpha.</span></span> <span data-ttu-id="7e64c-137">接著，每個元件會乘以已簽署的縮放比例 GL \_ c \_ 規模、新增至帶正負號偏差 gl \_ c \_ 偏差，然後壓制至範圍 \[ 0，1 \] (查看 **glPixelTransfer**) 。</span><span class="sxs-lookup"><span data-stu-id="7e64c-137">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see **glPixelTransfer**).</span></span><br/>                                                                                                                                                                                                |
| <span id="GL_GREEN"></span><span id="gl_green"></span><dl> <span data-ttu-id="7e64c-138"><dt>**GL \_ 綠**</dt></span><span class="sxs-lookup"><span data-stu-id="7e64c-138"><dt>**GL\_GREEN**</dt></span></span> </dl>                                | <span data-ttu-id="7e64c-139">每個元素都是一個綠色的元件。</span><span class="sxs-lookup"><span data-stu-id="7e64c-139">Each element is a single green component.</span></span> <span data-ttu-id="7e64c-140">它會轉換成浮點數，並藉由附加適用于紅色和藍色的0.0 和適用于 Alpha 的1.0，組合成 RGBA 元素。</span><span class="sxs-lookup"><span data-stu-id="7e64c-140">It is converted to floating point and assembled into an RGBA element by attaching 0.0 for red and blue, and 1.0 for alpha.</span></span> <span data-ttu-id="7e64c-141">接著，每個元件會乘以已簽署的縮放比例 GL \_ c \_ 規模、新增至帶正負號偏差 gl \_ c \_ 偏差，然後壓制至範圍 \[ 0，1 \] (查看 [**glPixelTransfer**](glpixeltransfer.md)) 。</span><span class="sxs-lookup"><span data-stu-id="7e64c-141">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see [**glPixelTransfer**](glpixeltransfer.md)).</span></span><br/>                                                                                                                                                                         |
| <span id="GL_BLUE"></span><span id="gl_blue"></span><dl> <span data-ttu-id="7e64c-142"><dt>**GL \_ 藍色**</dt></span><span class="sxs-lookup"><span data-stu-id="7e64c-142"><dt>**GL\_BLUE**</dt></span></span> </dl>                                   | <span data-ttu-id="7e64c-143">每個元素都是單一藍色元件。</span><span class="sxs-lookup"><span data-stu-id="7e64c-143">Each element is a single blue component.</span></span> <span data-ttu-id="7e64c-144">它會轉換成浮點數並組合成 RGBA 元素，方法是附加0.0 （紅色和綠色）和1.0 （適用于 Alpha）。</span><span class="sxs-lookup"><span data-stu-id="7e64c-144">It is converted to floating point and assembled into an RGBA element by attaching 0.0 for red and green, and 1.0 for alpha.</span></span> <span data-ttu-id="7e64c-145">接著，每個元件會乘以已簽署的縮放比例 GL \_ c \_ 規模、新增至帶正負號偏差 gl \_ c \_ 偏差，然後壓制至範圍 \[ 0，1 \] (查看 **glPixelTransfer**) 。</span><span class="sxs-lookup"><span data-stu-id="7e64c-145">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see **glPixelTransfer**).</span></span><br/>                                                                                                                                                                                                |
| <span id="GL_ALPHA"></span><span id="gl_alpha"></span><dl> <span data-ttu-id="7e64c-146"><dt>**GL \_ ALPHA**</dt></span><span class="sxs-lookup"><span data-stu-id="7e64c-146"><dt>**GL\_ALPHA**</dt></span></span> </dl>                                | <span data-ttu-id="7e64c-147">每個元素都是單一的紅色元件。</span><span class="sxs-lookup"><span data-stu-id="7e64c-147">Each element is a single red component.</span></span> <span data-ttu-id="7e64c-148">它會轉換成浮點數，並藉由附加0.0 的紅色、綠色和藍色來組合成 RGBA 元素。</span><span class="sxs-lookup"><span data-stu-id="7e64c-148">It is converted to floating point and assembled into an RGBA element by attaching 0.0 for red, green, and blue.</span></span> <span data-ttu-id="7e64c-149">接著，每個元件會乘以已簽署的縮放比例 GL \_ c \_ 規模、新增至帶正負號偏差 gl \_ c \_ 偏差，然後壓制至範圍 \[ 0，1 \] (查看 [**glPixelTransfer**](glpixeltransfer.md)) 。</span><span class="sxs-lookup"><span data-stu-id="7e64c-149">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see [**glPixelTransfer**](glpixeltransfer.md)).</span></span><br/>                                                                                                                                                                                      |
| <span id="GL_RGB"></span><span id="gl_rgb"></span><dl> <span data-ttu-id="7e64c-150"><dt>**GL \_ RGB**</dt></span><span class="sxs-lookup"><span data-stu-id="7e64c-150"><dt>**GL\_RGB**</dt></span></span> </dl>                                      | <span data-ttu-id="7e64c-151">每個元素都是 RGB 三重。</span><span class="sxs-lookup"><span data-stu-id="7e64c-151">Each element is an RGB triple.</span></span> <span data-ttu-id="7e64c-152">它會轉換成浮點數，並藉由附加1.0 的 Alpha 來組合成 RGBA 元素。</span><span class="sxs-lookup"><span data-stu-id="7e64c-152">It is converted to floating point and assembled into an RGBA element by attaching 1.0 for alpha.</span></span> <span data-ttu-id="7e64c-153">接著，每個元件會乘以已簽署的縮放比例 GL \_ c \_ 規模、新增至帶正負號偏差 gl \_ c \_ 偏差，然後壓制至範圍 \[ 0，1 \] (查看 **glPixelTransfer**) 。</span><span class="sxs-lookup"><span data-stu-id="7e64c-153">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see **glPixelTransfer**).</span></span><br/>                                                                                                                                                                                                                                     |
| <span id="GL_RGBA"></span><span id="gl_rgba"></span><dl> <span data-ttu-id="7e64c-154"><dt>**GL \_ RGBA**</dt></span><span class="sxs-lookup"><span data-stu-id="7e64c-154"><dt>**GL\_RGBA**</dt></span></span> </dl>                                   | <span data-ttu-id="7e64c-155">每個元素都是完整的 RGBA 元素。</span><span class="sxs-lookup"><span data-stu-id="7e64c-155">Each element is a complete RGBA element.</span></span> <span data-ttu-id="7e64c-156">它會轉換成浮點數。</span><span class="sxs-lookup"><span data-stu-id="7e64c-156">It is converted to floating point.</span></span> <span data-ttu-id="7e64c-157">接著，每個元件會乘以已簽署的縮放比例 GL \_ c \_ 規模、新增至帶正負號偏差 gl \_ c \_ 偏差，然後壓制至範圍 \[ 0，1 \] (查看 **glPixelTransfer**) 。</span><span class="sxs-lookup"><span data-stu-id="7e64c-157">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see **glPixelTransfer**).</span></span><br/>                                                                                                                                                                                                                                                                                         |
| <span id="GL_BGR_EXT"></span><span id="gl_bgr_ext"></span><dl> <span data-ttu-id="7e64c-158"><dt>**GL \_ BGR \_ EXT**</dt></span><span class="sxs-lookup"><span data-stu-id="7e64c-158"><dt>**GL\_BGR\_EXT**</dt></span></span> </dl>                         | <span data-ttu-id="7e64c-159">每個圖元都是三個元件的群組，順序如下：藍色、綠色、紅色。</span><span class="sxs-lookup"><span data-stu-id="7e64c-159">Each pixel is a group of three components in this order: blue, green, red.</span></span><br/> <span data-ttu-id="7e64c-160">GL \_ BGR \_ EXT 提供的格式符合 Windows 裝置獨立點陣圖 (dib) 的記憶體配置。</span><span class="sxs-lookup"><span data-stu-id="7e64c-160">GL\_BGR\_EXT provides a format that matches the memory layout of Windows device-independent bitmaps (DIBs).</span></span> <span data-ttu-id="7e64c-161">因此，您的應用程式可以使用 Windows 函式呼叫和 OpenGL 圖元函式呼叫的相同資料。</span><span class="sxs-lookup"><span data-stu-id="7e64c-161">Thus your applications can use the same data with Windows function calls and OpenGL pixel function calls.</span></span><br/>                                                                                                                                                                                                                                      |
| <span id="GL_BGRA_EXT"></span><span id="gl_bgra_ext"></span><dl> <span data-ttu-id="7e64c-162"><dt>**GL \_ BGRA \_ EXT**</dt></span><span class="sxs-lookup"><span data-stu-id="7e64c-162"><dt>**GL\_BGRA\_EXT**</dt></span></span> </dl>                      | <span data-ttu-id="7e64c-163">每個圖元都是四個元件的群組，順序如下： blue、綠、red、Alpha。</span><span class="sxs-lookup"><span data-stu-id="7e64c-163">Each pixel is a group of four components in this order: blue, green, red, alpha.</span></span><br/> <span data-ttu-id="7e64c-164">GL \_ BGRA \_ EXT 提供的格式符合 Windows 裝置獨立點陣圖 (dib) 的記憶體配置。</span><span class="sxs-lookup"><span data-stu-id="7e64c-164">GL\_BGRA\_EXT provides a format that matches the memory layout of Windows device-independent bitmaps (DIBs).</span></span> <span data-ttu-id="7e64c-165">因此，您的應用程式可以使用 Windows 函式呼叫和 OpenGL 圖元函式呼叫的相同資料。</span><span class="sxs-lookup"><span data-stu-id="7e64c-165">Thus your applications can use the same data with Windows function calls and OpenGL pixel function calls.</span></span><br/>                                                                                                                                                                                                                               |
| <span id="GL_LUMINANCE"></span><span id="gl_luminance"></span><dl> <span data-ttu-id="7e64c-166"><dt>**GL \_ 亮度**</dt></span><span class="sxs-lookup"><span data-stu-id="7e64c-166"><dt>**GL\_LUMINANCE**</dt></span></span> </dl>                    | <span data-ttu-id="7e64c-167">每個元素都是單一的亮度值。</span><span class="sxs-lookup"><span data-stu-id="7e64c-167">Each element is a single luminance value.</span></span> <span data-ttu-id="7e64c-168">它會轉換成浮點數，然後藉由針對紅色、綠色和藍色複寫亮度值三次，然後附加1.0 的 Alpha 元素組合成 RGBA 元素。</span><span class="sxs-lookup"><span data-stu-id="7e64c-168">It is converted to floating point, and then assembled into an RGBA element by replicating the luminance value three times for red, green, and blue, and attaching 1.0 for alpha.</span></span> <span data-ttu-id="7e64c-169">接著，每個元件會乘以已簽署的縮放比例 GL \_ c \_ 規模、新增至帶正負號偏差 gl \_ c \_ 偏差，然後壓制至範圍 \[ 0，1 \] (查看 [**glPixelTransfer**](glpixeltransfer.md)) 。</span><span class="sxs-lookup"><span data-stu-id="7e64c-169">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see [**glPixelTransfer**](glpixeltransfer.md)).</span></span><br/>                                                                                                                   |
| <span id="GL_LUMINANCE_ALPHA"></span><span id="gl_luminance_alpha"></span><dl> <span data-ttu-id="7e64c-170"><dt>**GL \_ 亮度 \_ ALPHA**</dt></span><span class="sxs-lookup"><span data-stu-id="7e64c-170"><dt>**GL\_LUMINANCE\_ALPHA**</dt></span></span> </dl> | <span data-ttu-id="7e64c-171">每個元素都是一組明亮度/Alpha 配對。</span><span class="sxs-lookup"><span data-stu-id="7e64c-171">Each element is a luminance/alpha pair.</span></span> <span data-ttu-id="7e64c-172">它會轉換成浮點數，然後藉由針對紅色、綠色和藍色複寫亮度值三次，來組合成 RGBA 元素。</span><span class="sxs-lookup"><span data-stu-id="7e64c-172">It is converted to floating point, and then assembled into an RGBA element by replicating the luminance value three times for red, green, and blue.</span></span> <span data-ttu-id="7e64c-173">接著，每個元件會乘以已簽署的縮放比例 GL \_ c \_ 規模、新增至帶正負號偏差 gl \_ c \_ 偏差，然後壓制至範圍 \[ 0，1 \] (查看 **glPixelTransfer**) 。</span><span class="sxs-lookup"><span data-stu-id="7e64c-173">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see **glPixelTransfer**).</span></span><br/>                                                                                                                                                                         |



 

</dd> <dt>

<span data-ttu-id="7e64c-174">*type*</span><span class="sxs-lookup"><span data-stu-id="7e64c-174">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="7e64c-175">圖元資料的資料類型。</span><span class="sxs-lookup"><span data-stu-id="7e64c-175">The data type of the pixel data.</span></span> <span data-ttu-id="7e64c-176">接受下列符號值： GL \_ 未簽署 \_ 位元組、gl \_ 位元組、GL \_ 點陣圖、gl \_ 未簽署 \_ 短、gl \_ 簡短、GL 不 \_ 帶正負號 \_ int、GL \_ int 和 gl \_ FLOAT。</span><span class="sxs-lookup"><span data-stu-id="7e64c-176">The following symbolic values are accepted: GL\_UNSIGNED\_BYTE, GL\_BYTE, GL\_BITMAP, GL\_UNSIGNED\_SHORT, GL\_SHORT, GL\_UNSIGNED\_INT, GL\_INT, and GL\_FLOAT.</span></span>

</dd> <dt>

<span data-ttu-id="7e64c-177">*圖元*</span><span class="sxs-lookup"><span data-stu-id="7e64c-177">*pixels*</span></span> 
</dt> <dd>

<span data-ttu-id="7e64c-178">記憶體中影像資料的指標。</span><span class="sxs-lookup"><span data-stu-id="7e64c-178">A pointer to the image data in memory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7e64c-179">傳回值</span><span class="sxs-lookup"><span data-stu-id="7e64c-179">Return value</span></span>

<span data-ttu-id="7e64c-180">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="7e64c-180">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="7e64c-181">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="7e64c-181">Error codes</span></span>

<span data-ttu-id="7e64c-182">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="7e64c-182">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="7e64c-183">Name</span><span class="sxs-lookup"><span data-stu-id="7e64c-183">Name</span></span>                                                                                                  | <span data-ttu-id="7e64c-184">意義</span><span class="sxs-lookup"><span data-stu-id="7e64c-184">Meaning</span></span>                                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7e64c-185"><dt>**GL \_ 無效 \_ 列舉**</dt></span><span class="sxs-lookup"><span data-stu-id="7e64c-185"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="7e64c-186">*目標* 不是 GL \_ 紋理。</span><span class="sxs-lookup"><span data-stu-id="7e64c-186">*target* was not an GL\_TEXTURE.</span></span><br/>                                                                                                                                                                                    |
| <dl> <span data-ttu-id="7e64c-187"><dt>**GL \_ 無效 \_ 列舉**</dt></span><span class="sxs-lookup"><span data-stu-id="7e64c-187"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="7e64c-188">*格式* 不是接受的 *格式* 常數。</span><span class="sxs-lookup"><span data-stu-id="7e64c-188">*format* was not an accepted *format* constant.</span></span> <span data-ttu-id="7e64c-189">只接受 GL 樣板 \_ \_ 索引和 gl \_ 深度 \_ 元件以外的格式常數。</span><span class="sxs-lookup"><span data-stu-id="7e64c-189">Only format constants other than GL\_STENCIL\_INDEX and GL\_DEPTH\_COMPONENT are accepted.</span></span> <span data-ttu-id="7e64c-190">如需可能值的清單，請參閱 *格式* 的參數描述。</span><span class="sxs-lookup"><span data-stu-id="7e64c-190">See the parameter description of *format* for a list of possible values.</span></span><br/> |
| <dl> <span data-ttu-id="7e64c-191"><dt>**GL \_ 無效 \_ 列舉**</dt></span><span class="sxs-lookup"><span data-stu-id="7e64c-191"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="7e64c-192">*類型* 不是 *類型* 常數。</span><span class="sxs-lookup"><span data-stu-id="7e64c-192">*type* was not a *type* constant.</span></span><br/>                                                                                                                                                                                   |
| <dl> <span data-ttu-id="7e64c-193"><dt>**GL \_ 無效 \_ 列舉**</dt></span><span class="sxs-lookup"><span data-stu-id="7e64c-193"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="7e64c-194">*類型* 為 gl \_ 點陣圖， *格式* 不是 gl \_ 色彩 \_ 索引。</span><span class="sxs-lookup"><span data-stu-id="7e64c-194">*type* was GL\_BITMAP and *format* was not GL\_COLOR\_INDEX.</span></span><br/>                                                                                                                                                        |
| <dl> <span data-ttu-id="7e64c-195"><dt>**GL \_ 無效 \_ 值**</dt></span><span class="sxs-lookup"><span data-stu-id="7e64c-195"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="7e64c-196">*層級* 小於零或大於 log2 *max*，其中 *max* 是 GL \_ 最大紋理大小的傳回值 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="7e64c-196">*level* was less than zero or greater than log2 *max*, where *max* was the returned value of GL\_MAX\_TEXTURE\_SIZE.</span></span><br/>                                                                                                 |
| <dl> <span data-ttu-id="7e64c-197"><dt>**GL \_ 無效 \_ 值**</dt></span><span class="sxs-lookup"><span data-stu-id="7e64c-197"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="7e64c-198">*internalformat* 不是1、2、3或4。</span><span class="sxs-lookup"><span data-stu-id="7e64c-198">*internalformat* was was not 1, 2, 3, or 4.</span></span><br/>                                                                                                                                                                         |
| <dl> <span data-ttu-id="7e64c-199"><dt>**GL \_ 無效 \_ 值**</dt></span><span class="sxs-lookup"><span data-stu-id="7e64c-199"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="7e64c-200">*寬度* 小於零或大於 2 + GL \_ 的最大 \_ 紋理 \_ 大小，或無法表示為某個整數值 *n* 的 2 *n* + 2 (框線) 。</span><span class="sxs-lookup"><span data-stu-id="7e64c-200">*width* was less than zero or greater than 2 + GL\_MAX\_TEXTURE\_SIZE, or it could not be represented as 2 *n* + 2(border) for some integer value of *n*.</span></span><br/>                                                            |
| <dl> <span data-ttu-id="7e64c-201"><dt>**GL \_ 無效 \_ 值**</dt></span><span class="sxs-lookup"><span data-stu-id="7e64c-201"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="7e64c-202">*框線* 不是0或1。</span><span class="sxs-lookup"><span data-stu-id="7e64c-202">*border* was not 0 or 1.</span></span><br/>                                                                                                                                                                                            |
| <dl> <span data-ttu-id="7e64c-203"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="7e64c-203"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="7e64c-204">呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。</span><span class="sxs-lookup"><span data-stu-id="7e64c-204">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/>                                                                                          |



## <a name="remarks"></a><span data-ttu-id="7e64c-205">備註</span><span class="sxs-lookup"><span data-stu-id="7e64c-205">Remarks</span></span>

<span data-ttu-id="7e64c-206">**GlTexImage1D** 函式會指定一維紋理影像。</span><span class="sxs-lookup"><span data-stu-id="7e64c-206">The **glTexImage1D** function specifies a one-dimensional texture image.</span></span> <span data-ttu-id="7e64c-207">紋理會將指定之 *材質影像* 的一部分對應到已啟用紋理的每個圖形化基本物件。</span><span class="sxs-lookup"><span data-stu-id="7e64c-207">Texturing maps a portion of a specified *texture image* onto each graphical primitive for which texturing is enabled.</span></span> <span data-ttu-id="7e64c-208">使用 [**glEnable**](glenable.md) 和 **glDisable** 搭配引數 GL 紋理1d 來啟用和停用一維紋理 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="7e64c-208">One-dimensional texturing is enabled and disabled using [**glEnable**](glenable.md) and **glDisable** with argument GL\_TEXTURE\_1D.</span></span>

<span data-ttu-id="7e64c-209">材質影像會以 **glTexImage1D** 定義。</span><span class="sxs-lookup"><span data-stu-id="7e64c-209">Texture images are defined with **glTexImage1D**.</span></span> <span data-ttu-id="7e64c-210">引數描述紋理影像的參數，例如框線寬度、框線寬度、詳細資料層級 (查看 [**glTexParameter**](gltexparameter-functions.md)) ，以及所提供的色彩元件數目。</span><span class="sxs-lookup"><span data-stu-id="7e64c-210">The arguments describe the parameters of the texture image, such as width, width of the border, level-of-detail number (see [**glTexParameter**](gltexparameter-functions.md)), and number of color components provided.</span></span> <span data-ttu-id="7e64c-211">最後三個引數說明影像在記憶體中的呈現方式。</span><span class="sxs-lookup"><span data-stu-id="7e64c-211">The last three arguments describe the way the image is represented in memory.</span></span> <span data-ttu-id="7e64c-212">這些引數等同于用於 [**glDrawPixels**](gldrawpixels.md)的像素格式。</span><span class="sxs-lookup"><span data-stu-id="7e64c-212">These arguments are identical to the pixel formats used for [**glDrawPixels**](gldrawpixels.md).</span></span>

<span data-ttu-id="7e64c-213">資料會以一系列的帶正負號或不帶正負號的位元組、短路或長，或單精確度浮點值（視 *類型* 而 *定）來* 讀取。</span><span class="sxs-lookup"><span data-stu-id="7e64c-213">Data is read from *pixels* as a sequence of signed or unsigned bytes, shorts or longs, or single-precision floating-point values, depending on *type*.</span></span> <span data-ttu-id="7e64c-214">這些值會依 *格式* 組成一組、二、三或四個值，以形成元素。</span><span class="sxs-lookup"><span data-stu-id="7e64c-214">These values are grouped into sets of one, two, three, or four values, depending on *format*, to form elements.</span></span> <span data-ttu-id="7e64c-215">如果 *type* 是 GL \_ BITMAP，資料會被視為不帶正負號的位元組字串 (且 *格式* 必須是 GL \_ 色彩 \_ 索引) 。</span><span class="sxs-lookup"><span data-stu-id="7e64c-215">If *type* is GL\_BITMAP, the data is considered as a string of unsigned bytes (and *format* must be GL\_COLOR\_INDEX).</span></span> <span data-ttu-id="7e64c-216">每個資料位元組都會被視為 8 1 位元素，並以 GL 解壓縮 LSB 先決定的位順序， \_ \_ \_ (請參閱 [**glPixelStore**](glpixelstore-functions.md)) 。</span><span class="sxs-lookup"><span data-stu-id="7e64c-216">Each data byte is treated as eight 1-bit elements, with bit ordering determined by GL\_UNPACK\_LSB\_FIRST (see [**glPixelStore**](glpixelstore-functions.md)).</span></span>

<span data-ttu-id="7e64c-217">材質影像的每個材質元素最多可有四個元件，視 *元件* 而定。</span><span class="sxs-lookup"><span data-stu-id="7e64c-217">A texture image can have up to four components per texture element, depending on *components*.</span></span> <span data-ttu-id="7e64c-218">單一元件紋理影像只會使用從 *圖元* 解壓縮之 RGBA 色彩的紅色元件。</span><span class="sxs-lookup"><span data-stu-id="7e64c-218">A one-component texture image uses only the red component of the RGBA color extracted from *pixels*.</span></span> <span data-ttu-id="7e64c-219">雙元件映射會使用 R 和值。</span><span class="sxs-lookup"><span data-stu-id="7e64c-219">A two-component image uses the R and A values.</span></span> <span data-ttu-id="7e64c-220">三個元件的影像使用 R、G 和 B 值。</span><span class="sxs-lookup"><span data-stu-id="7e64c-220">A three-component image uses the R, G, and B values.</span></span> <span data-ttu-id="7e64c-221">四個元件的映射會使用所有的 RGBA 元件。</span><span class="sxs-lookup"><span data-stu-id="7e64c-221">A four-component image uses all of the RGBA components.</span></span>

<span data-ttu-id="7e64c-222">紋理在色彩索引模式中沒有任何作用。</span><span class="sxs-lookup"><span data-stu-id="7e64c-222">Texturing has no effect in color-index mode.</span></span>

<span data-ttu-id="7e64c-223">材質影像可以用與 [**glDrawPixels**](gldrawpixels.md) 命令中的圖元相同的資料格式表示，但 \_ 無法使用 gl 樣板 \_ 索引和 gl \_ 深度 \_ 元件。</span><span class="sxs-lookup"><span data-stu-id="7e64c-223">The texture image can be represented by the same data formats as the pixels in a [**glDrawPixels**](gldrawpixels.md) command, except that GL\_STENCIL\_INDEX and GL\_DEPTH\_COMPONENT cannot be used.</span></span> <span data-ttu-id="7e64c-224">[**GlPixelStore**](glpixelstore-functions.md)和 [**glPixelTransfer**](glpixeltransfer.md)模式會以其影響 **glDrawPixels** 的確切方式來影響紋理影像。</span><span class="sxs-lookup"><span data-stu-id="7e64c-224">The [**glPixelStore**](glpixelstore-functions.md) and [**glPixelTransfer**](glpixeltransfer.md) modes affect texture images in exactly the way they affect **glDrawPixels**.</span></span>

<span data-ttu-id="7e64c-225">寬度為零的材質影像表示 null 材質。</span><span class="sxs-lookup"><span data-stu-id="7e64c-225">A texture image with zero width indicates the null texture.</span></span> <span data-ttu-id="7e64c-226">如果針對詳細資料0指定了 null 材質，就如同已停用紋理一樣。</span><span class="sxs-lookup"><span data-stu-id="7e64c-226">If the null texture is specified for level-of-detail 0, it is as if texturing were disabled.</span></span>

<span data-ttu-id="7e64c-227">下列函式會取出與 **glTexImageID** 相關的資訊：</span><span class="sxs-lookup"><span data-stu-id="7e64c-227">The following functions retrieve information related to **glTexImageID**:</span></span>

[<span data-ttu-id="7e64c-228">**glGetTexImage**</span><span class="sxs-lookup"><span data-stu-id="7e64c-228">**glGetTexImage**</span></span>](glgetteximage.md)

<span data-ttu-id="7e64c-229">[](glisenabled.md)具有引數 GL \_ 材質 \_ 1d 的 glIsEnabled</span><span class="sxs-lookup"><span data-stu-id="7e64c-229">[**glIsEnabled**](glisenabled.md) with argument GL\_TEXTURE\_1D</span></span>

## <a name="requirements"></a><span data-ttu-id="7e64c-230">規格需求</span><span class="sxs-lookup"><span data-stu-id="7e64c-230">Requirements</span></span>



| <span data-ttu-id="7e64c-231">需求</span><span class="sxs-lookup"><span data-stu-id="7e64c-231">Requirement</span></span> | <span data-ttu-id="7e64c-232">值</span><span class="sxs-lookup"><span data-stu-id="7e64c-232">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7e64c-233">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7e64c-233">Minimum supported client</span></span><br/> | <span data-ttu-id="7e64c-234">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7e64c-234">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="7e64c-235">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7e64c-235">Minimum supported server</span></span><br/> | <span data-ttu-id="7e64c-236">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7e64c-236">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7e64c-237">標頭</span><span class="sxs-lookup"><span data-stu-id="7e64c-237">Header</span></span><br/>                   | <dl> <span data-ttu-id="7e64c-238"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="7e64c-238"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="7e64c-239">程式庫</span><span class="sxs-lookup"><span data-stu-id="7e64c-239">Library</span></span><br/>                  | <dl> <span data-ttu-id="7e64c-240"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="7e64c-240"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="7e64c-241">DLL</span><span class="sxs-lookup"><span data-stu-id="7e64c-241">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7e64c-242"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7e64c-242"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e64c-243">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7e64c-243">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e64c-244">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="7e64c-244">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="7e64c-245">**glCopyPixels**</span><span class="sxs-lookup"><span data-stu-id="7e64c-245">**glCopyPixels**</span></span>](glcopypixels.md)
</dt> <dt>

[<span data-ttu-id="7e64c-246">**glCopyTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="7e64c-246">**glCopyTexImage1D**</span></span>](glcopyteximage1d.md)
</dt> <dt>

[<span data-ttu-id="7e64c-247">**glCopyTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="7e64c-247">**glCopyTexImage2D**</span></span>](glcopyteximage2d.md)
</dt> <dt>

[<span data-ttu-id="7e64c-248">**glCopyTexSubImage1D**</span><span class="sxs-lookup"><span data-stu-id="7e64c-248">**glCopyTexSubImage1D**</span></span>](glcopytexsubimage1d.md)
</dt> <dt>

[<span data-ttu-id="7e64c-249">**glCopyTexSubImage2D**</span><span class="sxs-lookup"><span data-stu-id="7e64c-249">**glCopyTexSubImage2D**</span></span>](glcopytexsubimage2d.md)
</dt> <dt>

[<span data-ttu-id="7e64c-250">**glDrawPixels**</span><span class="sxs-lookup"><span data-stu-id="7e64c-250">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="7e64c-251">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="7e64c-251">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="7e64c-252">**glFog**</span><span class="sxs-lookup"><span data-stu-id="7e64c-252">**glFog**</span></span>](glfog.md)
</dt> <dt>

[<span data-ttu-id="7e64c-253">**glGetTexImage**</span><span class="sxs-lookup"><span data-stu-id="7e64c-253">**glGetTexImage**</span></span>](glgetteximage.md)
</dt> <dt>

[<span data-ttu-id="7e64c-254">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="7e64c-254">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="7e64c-255">**glPixelStore**</span><span class="sxs-lookup"><span data-stu-id="7e64c-255">**glPixelStore**</span></span>](glpixelstore-functions.md)
</dt> <dt>

[<span data-ttu-id="7e64c-256">**glPixelTransfer**</span><span class="sxs-lookup"><span data-stu-id="7e64c-256">**glPixelTransfer**</span></span>](glpixeltransfer.md)
</dt> <dt>

[<span data-ttu-id="7e64c-257">**glTexEnv**</span><span class="sxs-lookup"><span data-stu-id="7e64c-257">**glTexEnv**</span></span>](gltexenv-functions.md)
</dt> <dt>

[<span data-ttu-id="7e64c-258">**glTexGen**</span><span class="sxs-lookup"><span data-stu-id="7e64c-258">**glTexGen**</span></span>](gltexgen-functions.md)
</dt> <dt>

[<span data-ttu-id="7e64c-259">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="7e64c-259">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="7e64c-260">**glTexSubImage1D**</span><span class="sxs-lookup"><span data-stu-id="7e64c-260">**glTexSubImage1D**</span></span>](gltexsubimage1d.md)
</dt> <dt>

[<span data-ttu-id="7e64c-261">**glTexSubImage2D**</span><span class="sxs-lookup"><span data-stu-id="7e64c-261">**glTexSubImage2D**</span></span>](gltexsubimage2d.md)
</dt> <dt>

[<span data-ttu-id="7e64c-262">**glTexParameter**</span><span class="sxs-lookup"><span data-stu-id="7e64c-262">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> </dl>

 

 





