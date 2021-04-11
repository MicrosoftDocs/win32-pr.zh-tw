---
title: 'glTexParameteriv 函式 (Gl) '
description: '設定材質參數。 |glTexParameteriv 函式 (Gl) '
ms.assetid: c6381ee5-5323-4e11-9c32-bc70f25f8f4e
keywords:
- glTexParameterfv 函式 OpenGL
topic_type:
- apiref
api_name:
- glTexParameterfv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 315f9b447742cfe40219877bb947c7cc5584a3e7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "103945940"
---
# <a name="gltexparameteriv-function"></a><span data-ttu-id="6766d-105">glTexParameteriv 函式</span><span class="sxs-lookup"><span data-stu-id="6766d-105">glTexParameteriv function</span></span>

<span data-ttu-id="6766d-106">設定材質參數。</span><span class="sxs-lookup"><span data-stu-id="6766d-106">Sets texture parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="6766d-107">語法</span><span class="sxs-lookup"><span data-stu-id="6766d-107">Syntax</span></span>


```C++
void WINAPI glTexParameterfv(
         GLenum target,
         GLenum pname,
   const GLint  *params
);
```



## <a name="parameters"></a><span data-ttu-id="6766d-108">參數</span><span class="sxs-lookup"><span data-stu-id="6766d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6766d-109">*目標*</span><span class="sxs-lookup"><span data-stu-id="6766d-109">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="6766d-110">目標材質，必須是 GL \_ 材質 \_ 1D 或 gl \_ 紋理 \_ 2d。</span><span class="sxs-lookup"><span data-stu-id="6766d-110">The target texture, which must be either GL\_TEXTURE\_1D or GL\_TEXTURE\_2D.</span></span>

</dd> <dt>

<span data-ttu-id="6766d-111">*pname*</span><span class="sxs-lookup"><span data-stu-id="6766d-111">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="6766d-112">單一值材質參數的符號名稱。</span><span class="sxs-lookup"><span data-stu-id="6766d-112">The symbolic name of a single valued texture parameter.</span></span> <span data-ttu-id="6766d-113">*Pname* 接受下列符號。</span><span class="sxs-lookup"><span data-stu-id="6766d-113">The following symbols are accepted in *pname*.</span></span>



| <span data-ttu-id="6766d-114">值</span><span class="sxs-lookup"><span data-stu-id="6766d-114">Value</span></span>                                                                                                                                                                                         | <span data-ttu-id="6766d-115">意義</span><span class="sxs-lookup"><span data-stu-id="6766d-115">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_TEXTURE_MIN_FILTER"></span><span id="gl_texture_min_filter"></span><dl> <span data-ttu-id="6766d-116"><dt>**GL \_ 材質 \_ 最小 \_ 篩選**</dt></span><span class="sxs-lookup"><span data-stu-id="6766d-116"><dt>**GL\_TEXTURE\_MIN\_FILTER**</dt></span></span> </dl>       | <span data-ttu-id="6766d-117">紋理縮小函式會在每次有紋理的圖元對應到一個以上的材質專案區域時使用。</span><span class="sxs-lookup"><span data-stu-id="6766d-117">The texture minifying function is used whenever the pixel being textured maps to an area greater than one texture element.</span></span> <span data-ttu-id="6766d-118">有六個定義的縮小函數。</span><span class="sxs-lookup"><span data-stu-id="6766d-118">There are six defined minifying functions.</span></span> <span data-ttu-id="6766d-119">其中兩個會使用最接近的一個或最接近的四個材質元素來計算紋理值。</span><span class="sxs-lookup"><span data-stu-id="6766d-119">Two of them use the nearest one or nearest four texture elements to compute the texture value.</span></span> <span data-ttu-id="6766d-120">其他四個使用 mipmap。</span><span class="sxs-lookup"><span data-stu-id="6766d-120">The other four use mipmaps.</span></span> <br/> <span data-ttu-id="6766d-121">Mipmap 是一組已排序的陣列，代表以漸進較低解析度表示的相同影像。</span><span class="sxs-lookup"><span data-stu-id="6766d-121">A mipmap is an ordered set of arrays representing the same image at progressively lower resolutions.</span></span> <span data-ttu-id="6766d-122">如果材質的維度為 2nx2<sup>m</sup> ，則 (n，m) + 1 mipmap 的上限。</span><span class="sxs-lookup"><span data-stu-id="6766d-122">If the texture has dimensions 2nx2<sup>m</sup> there are max(n, m) + 1 mipmaps.</span></span> <span data-ttu-id="6766d-123">第一個 mipmap 是原始材質，維度為 2nx2<sup>m</sup>。</span><span class="sxs-lookup"><span data-stu-id="6766d-123">The first mipmap is the original texture, with dimensions 2nx2<sup>m</sup>.</span></span> <span data-ttu-id="6766d-124">每個後續的 mipmap 都有維度 2<sup>k</sup>1x2<sup>l</sup>1，其中 2<sup>k</sup>x2<sup>l</sup> 是前一個 mipmap 的維度，直到 k = 0 或 l = 0 為止。</span><span class="sxs-lookup"><span data-stu-id="6766d-124">Each subsequent mipmap has dimensions 2<sup>k</sup>1x2<sup>l</sup>1 where 2<sup>k</sup>x2<sup>l</sup> are the dimensions of the previous mipmap, until either k = 0 or l = 0.</span></span> <span data-ttu-id="6766d-125">屆時，後續的 mipmap 會有維度 1x2<sup>l</sup>1 或 2<sup>k</sup>1x1，直到最後一個 mipmap，其維度為1x1。</span><span class="sxs-lookup"><span data-stu-id="6766d-125">At that point, subsequent mipmaps have dimension 1x2<sup>l</sup>1 or 2<sup>k</sup>1x1 until the final mipmap, which has dimension 1x1.</span></span> <span data-ttu-id="6766d-126">Mipmap 是使用 [**glTexImage1D**](glteximage1d.md) 或 [**glTexImage2D**](glteximage2d.md) 來定義，並以詳細程度的引數來指出 mipmap 的順序。</span><span class="sxs-lookup"><span data-stu-id="6766d-126">Mipmaps are defined using [**glTexImage1D**](glteximage1d.md) or [**glTexImage2D**](glteximage2d.md) with the level-of-detail argument indicating the order of the mipmaps.</span></span> <span data-ttu-id="6766d-127">層級0是原始紋理;水準粗體最大 (n，m) 是最後 1x1 mipmap。</span><span class="sxs-lookup"><span data-stu-id="6766d-127">Level 0 is the original texture; level bold max(n, m) is the final 1x1 mipmap.</span></span><br/> |
| <span id="GL_TEXTURE_MAG_FILTER"></span><span id="gl_texture_mag_filter"></span><dl> <span data-ttu-id="6766d-128"><dt>**GL \_ 紋理 \_ MAG \_ 篩選**</dt></span><span class="sxs-lookup"><span data-stu-id="6766d-128"><dt>**GL\_TEXTURE\_MAG\_FILTER**</dt></span></span> </dl>       | <span data-ttu-id="6766d-129">當材質的圖元對應到小於或等於一個材質元素的區域時，就會使用材質放大功能。</span><span class="sxs-lookup"><span data-stu-id="6766d-129">The texture magnification function is used when the pixel being textured maps to an area less than or equal to one texture element.</span></span> <span data-ttu-id="6766d-130">它會將材質放大函式設定為 \_ 最接近的 gl 或 gl \_ 線性。</span><span class="sxs-lookup"><span data-stu-id="6766d-130">It sets the texture magnification function to either GL\_NEAREST or GL\_LINEAR.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="GL_TEXTURE_WRAP_S"></span><span id="gl_texture_wrap_s"></span><dl> <span data-ttu-id="6766d-131"><dt>**GL \_ 材質 \_ 換行 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6766d-131"><dt>**GL\_TEXTURE\_WRAP\_S**</dt></span></span> </dl>                   | <span data-ttu-id="6766d-132">將材質座標 s 的 wrap 參數設定為 GL \_ 夾具或 gl \_ 重複。</span><span class="sxs-lookup"><span data-stu-id="6766d-132">Sets the wrap parameter for texture coordinate s to either GL\_CLAMP or GL\_REPEAT.</span></span> <span data-ttu-id="6766d-133">GL \_ 夾具會將 s 座標壓制至範圍 \[ 0，1， \] 以便在將單一影像對應至物件時防止包裝成品。</span><span class="sxs-lookup"><span data-stu-id="6766d-133">GL\_CLAMP causes s coordinates to be clamped to the range \[0,1\] and is useful for preventing wrapping artifacts when mapping a single image onto an object.</span></span> <span data-ttu-id="6766d-134">GL \_ 重複會忽略 s 座標的整數部分。OpenGL 只會使用小數部分，藉此建立重複的模式。</span><span class="sxs-lookup"><span data-stu-id="6766d-134">GL\_REPEAT causes the integer part of the s coordinate to be ignored; OpenGL uses only the fractional part, thereby creating a repeating pattern.</span></span> <span data-ttu-id="6766d-135">只有當換行設定為 GL 夾具時，才會存取框線材質元素 \_ 。</span><span class="sxs-lookup"><span data-stu-id="6766d-135">Border texture elements are accessed only if wrapping is set to GL\_CLAMP.</span></span> <span data-ttu-id="6766d-136">一開始， \_ \_ 會將 gl 材質換行 \_ 設定為 gl \_ 重複。</span><span class="sxs-lookup"><span data-stu-id="6766d-136">Initially, GL\_TEXTURE\_WRAP\_S is set to GL\_REPEAT.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="GL_TEXTURE_WRAP_T"></span><span id="gl_texture_wrap_t"></span><dl> <span data-ttu-id="6766d-137"><dt>**GL \_ 紋理 \_ WRAP \_ T**</dt></span><span class="sxs-lookup"><span data-stu-id="6766d-137"><dt>**GL\_TEXTURE\_WRAP\_T**</dt></span></span> </dl>                   | <span data-ttu-id="6766d-138">將材質座標 t 的 wrap 參數設定為 GL \_ 夾具或 gl \_ 重複。</span><span class="sxs-lookup"><span data-stu-id="6766d-138">Sets the wrap parameter for texture coordinate t to either GL\_CLAMP or GL\_REPEAT.</span></span> <span data-ttu-id="6766d-139">請參閱 GL \_ 材質 WRAP S 下的討論 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="6766d-139">See the discussion under GL\_TEXTURE\_WRAP\_S.</span></span> <span data-ttu-id="6766d-140">一開始，GL \_ 紋理 \_ WRAP \_ T 會設定為 gl \_ 重複。</span><span class="sxs-lookup"><span data-stu-id="6766d-140">Initially, GL\_TEXTURE\_WRAP\_T is set to GL\_REPEAT.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span id="GL_TEXTURE_BORDER_COLOR"></span><span id="gl_texture_border_color"></span><dl> <span data-ttu-id="6766d-141"><dt>**GL \_ 紋理 \_ 框線 \_ 色彩**</dt></span><span class="sxs-lookup"><span data-stu-id="6766d-141"><dt>**GL\_TEXTURE\_BORDER\_COLOR**</dt></span></span> </dl> | <span data-ttu-id="6766d-142">設定框線色彩。</span><span class="sxs-lookup"><span data-stu-id="6766d-142">Sets a border color.</span></span> <span data-ttu-id="6766d-143">*Params* 參數包含四個值，這些值組成材質框線的 RGBA 色彩。</span><span class="sxs-lookup"><span data-stu-id="6766d-143">The *params* parameter contains four values that comprise the RGBA color of the texture border.</span></span> <span data-ttu-id="6766d-144">整數色彩元件會以線性方式轉譯，因此最多正整數會對應到1.0，而最大的負整數會對應到1.0。</span><span class="sxs-lookup"><span data-stu-id="6766d-144">Integer color components are interpreted linearly such that the most positive integer maps to 1.0, and the most negative integer maps to 1.0.</span></span> <span data-ttu-id="6766d-145">當指定值時，這些值會壓制至範圍 \[ 0、1 \] 。</span><span class="sxs-lookup"><span data-stu-id="6766d-145">The values are clamped to the range \[0,1\] when they are specified.</span></span> <span data-ttu-id="6766d-146">一開始，框線色彩是 (0、0、0、0) 。</span><span class="sxs-lookup"><span data-stu-id="6766d-146">Initially, the border color is (0, 0, 0, 0).</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="GL_TEXTURE_PRIORITY"></span><span id="gl_texture_priority"></span><dl> <span data-ttu-id="6766d-147"><dt>**GL \_ 材質 \_ 優先順序**</dt></span><span class="sxs-lookup"><span data-stu-id="6766d-147"><dt>**GL\_TEXTURE\_PRIORITY**</dt></span></span> </dl>              | <span data-ttu-id="6766d-148">指定目前系結材質的材質居住優先順序。</span><span class="sxs-lookup"><span data-stu-id="6766d-148">Specifies the texture residence priority of the currently bound texture.</span></span> <span data-ttu-id="6766d-149">允許的值在範圍 \[ 0，1之間 \] 。</span><span class="sxs-lookup"><span data-stu-id="6766d-149">Permissible values are in the range \[0, 1\].</span></span> <span data-ttu-id="6766d-150">如需詳細資訊，請參閱 [**glPrioritizeTextures**](glprioritizetextures.md) 和 [**glBindTexture**](glbindtexture.md) 。</span><span class="sxs-lookup"><span data-stu-id="6766d-150">See [**glPrioritizeTextures**](glprioritizetextures.md) and [**glBindTexture**](glbindtexture.md) for more information.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |



 

</dd> <dt>

<span data-ttu-id="6766d-151">*params*</span><span class="sxs-lookup"><span data-stu-id="6766d-151">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="6766d-152">陣列的指標，其中儲存 pname 的值或值。</span><span class="sxs-lookup"><span data-stu-id="6766d-152">A pointer to an array where the value or values of pname are stored.</span></span> <span data-ttu-id="6766d-153">Params 參數提供一個函式，以縮小材質作為下列其中一項。</span><span class="sxs-lookup"><span data-stu-id="6766d-153">The params parameter supplies a function for minifying the texture as one of the following.</span></span>



| <span data-ttu-id="6766d-154">值</span><span class="sxs-lookup"><span data-stu-id="6766d-154">Value</span></span>                                                                                                                                                                                               | <span data-ttu-id="6766d-155">意義</span><span class="sxs-lookup"><span data-stu-id="6766d-155">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_NEAREST_"></span><span id="gl_nearest_"></span><dl> <span data-ttu-id="6766d-156"><dt>**GL \_最接近**</dt></span><span class="sxs-lookup"><span data-stu-id="6766d-156"><dt>**GL\_NEAREST** </dt></span></span> </dl>                                             | <span data-ttu-id="6766d-157">傳回材質專案的值，此值最接近 (在曼哈頓距離) 至要紋理的圖元中央。</span><span class="sxs-lookup"><span data-stu-id="6766d-157">Returns the value of the texture element that is nearest (in Manhattan distance) to the center of the pixel being textured.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="GL_LINEAR"></span><span id="gl_linear"></span><dl> <span data-ttu-id="6766d-158"><dt>**GL \_ 線性**</dt></span><span class="sxs-lookup"><span data-stu-id="6766d-158"><dt>**GL\_LINEAR**</dt></span></span> </dl>                                                   | <span data-ttu-id="6766d-159">傳回四個材質元素的加權平均值，最接近圖元的中央。</span><span class="sxs-lookup"><span data-stu-id="6766d-159">Returns the weighted average of the four texture elements that are closest to the center of the pixel being textured.</span></span> <span data-ttu-id="6766d-160">這些專案可以包含框線材質元素，視 GL \_ 紋理 \_ wrap S 的值 \_ 、GL \_ 材質 \_ 換行 \_ T，以及確切的對應而定。</span><span class="sxs-lookup"><span data-stu-id="6766d-160">These can include border texture elements, depending on the values of GL\_TEXTURE\_WRAP\_S, GL\_TEXTURE\_WRAP\_T, and on the exact mapping.</span></span> <span data-ttu-id="6766d-161">\_最接近的 gl 通常比 gl \_ 線性更快，但它可以產生具有更清晰邊緣的紋理影像，因為材質元素之間的轉換不會像是平滑。</span><span class="sxs-lookup"><span data-stu-id="6766d-161">GL\_NEAREST is generally faster than GL\_LINEAR, but it can produce textured images with sharper edges because the transition between texture elements is not as smooth.</span></span> <span data-ttu-id="6766d-162">GL \_ 紋理 MAG 濾波器的預設 \_ 值 \_ 為 gl \_ 線性。</span><span class="sxs-lookup"><span data-stu-id="6766d-162">The default value of GL\_TEXTURE\_MAG\_FILTER is GL\_LINEAR.</span></span><br/> |
| <span id="GL_NEAREST_MIPMAP_NEAREST"></span><span id="gl_nearest_mipmap_nearest"></span><dl> <span data-ttu-id="6766d-163"><dt>**最接近最接近 MIPMAP 的 GL \_ \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6766d-163"><dt>**GL\_NEAREST\_MIPMAP\_NEAREST**</dt></span></span> </dl> | <span data-ttu-id="6766d-164">選擇最符合所要材質之圖元大小的 mipmap，並使用最接近的 GL \_ 準則 (最接近圖元) 中心的材質元素，以產生材質值。</span><span class="sxs-lookup"><span data-stu-id="6766d-164">Chooses the mipmap that most closely matches the size of the pixel being textured and uses the GL\_NEAREST criterion (the texture element nearest to the center of the pixel) to produce a texture value.</span></span> <br/>                                                                                                                                                                                                                                                                                              |
| <span id="GL_LINEAR_MIPMAP_NEAREST"></span><span id="gl_linear_mipmap_nearest"></span><dl> <span data-ttu-id="6766d-165"><dt>**\_最接近的 GL 線性 \_ MIPMAP \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6766d-165"><dt>**GL\_LINEAR\_MIPMAP\_NEAREST**</dt></span></span> </dl>    | <span data-ttu-id="6766d-166">選擇最接近圖元大小的 mipmap，並使用 GL \_ 線性標準 (四個材質元素的加權平均值，最接近圖元) 的中心，以產生材質值。</span><span class="sxs-lookup"><span data-stu-id="6766d-166">Chooses the mipmap that most closely matches the size of the pixel being textured and uses the GL\_LINEAR criterion (a weighted average of the four texture elements that are closest to the center of the pixel) to produce a texture value.</span></span> <br/>                                                                                                                                                                                                                                                          |
| <span id="GL_NEAREST_MIPMAP_LINEAR"></span><span id="gl_nearest_mipmap_linear"></span><dl> <span data-ttu-id="6766d-167"><dt>**GL \_ 最接近 \_ MIPMAP \_ 線性**</dt></span><span class="sxs-lookup"><span data-stu-id="6766d-167"><dt>**GL\_NEAREST\_MIPMAP\_LINEAR**</dt></span></span> </dl>    | <span data-ttu-id="6766d-168">選擇最符合所要材質之圖元大小的兩個 mipmap，並使用最接近的 GL \_ 準則 (最接近圖元) 的材質元素，以產生每個 mipmap 的材質值。</span><span class="sxs-lookup"><span data-stu-id="6766d-168">Chooses the two mipmaps that most closely match the size of the pixel being textured and uses the GL\_NEAREST criterion (the texture element nearest to the center of the pixel) to produce a texture value from each mipmap.</span></span> <span data-ttu-id="6766d-169">最後的材質值是這兩個值的加權平均值。</span><span class="sxs-lookup"><span data-stu-id="6766d-169">The final texture value is a weighted average of those two values.</span></span> <br/>                                                                                                                                                                                                       |
| <span id="GL_LINEAR_MIPMAP_LINEAR"></span><span id="gl_linear_mipmap_linear"></span><dl> <span data-ttu-id="6766d-170"><dt>**GL \_ 線性 \_ MIPMAP \_ 線性**</dt></span><span class="sxs-lookup"><span data-stu-id="6766d-170"><dt>**GL\_LINEAR\_MIPMAP\_LINEAR**</dt></span></span> </dl>       | <span data-ttu-id="6766d-171">選擇最接近圖元大小的兩個 mipmap，並使用 GL \_ 線性標準 (四個材質元素的加權平均值，最接近圖元) 的中心，以產生每個 mipmap 的材質值。</span><span class="sxs-lookup"><span data-stu-id="6766d-171">Chooses the two mipmaps that most closely match the size of the pixel being textured and uses the GL\_LINEAR criterion (a weighted average of the four texture elements that are closest to the center of the pixel) to produce a texture value from each mipmap.</span></span> <span data-ttu-id="6766d-172">最後的材質值是這兩個值的加權平均值。</span><span class="sxs-lookup"><span data-stu-id="6766d-172">The final texture value is a weighted average of those two values.</span></span><br/>                                                                                                                                                                    |



 

<span data-ttu-id="6766d-173">*Params* 參數提供一個函式，可將材質放大為下列其中一項。</span><span class="sxs-lookup"><span data-stu-id="6766d-173">The *params* parameter supplies a function for magnifying the texture as one of the following.</span></span>



| <span data-ttu-id="6766d-174">值</span><span class="sxs-lookup"><span data-stu-id="6766d-174">Value</span></span>                                                                                                                                                   | <span data-ttu-id="6766d-175">意義</span><span class="sxs-lookup"><span data-stu-id="6766d-175">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_NEAREST_"></span><span id="gl_nearest_"></span><dl> <span data-ttu-id="6766d-176"><dt>**GL \_最接近**</dt></span><span class="sxs-lookup"><span data-stu-id="6766d-176"><dt>**GL\_NEAREST** </dt></span></span> </dl> | <span data-ttu-id="6766d-177">傳回材質專案的值，此值最接近 (在曼哈頓距離) 至要紋理的圖元中央。</span><span class="sxs-lookup"><span data-stu-id="6766d-177">Returns the value of the texture element that is nearest (in Manhattan distance) to the center of the pixel being textured.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="GL_LINEAR"></span><span id="gl_linear"></span><dl> <span data-ttu-id="6766d-178"><dt>**GL \_ 線性**</dt></span><span class="sxs-lookup"><span data-stu-id="6766d-178"><dt>**GL\_LINEAR**</dt></span></span> </dl>       | <span data-ttu-id="6766d-179">傳回四個材質元素的加權平均值，最接近圖元的中央。</span><span class="sxs-lookup"><span data-stu-id="6766d-179">Returns the weighted average of the four texture elements that are closest to the center of the pixel being textured.</span></span> <span data-ttu-id="6766d-180">這些專案可以包含框線材質元素，視 GL \_ 紋理 \_ wrap S 的值 \_ 、GL \_ 材質 \_ 換行 \_ T，以及確切的對應而定。</span><span class="sxs-lookup"><span data-stu-id="6766d-180">These can include border texture elements, depending on the values of GL\_TEXTURE\_WRAP\_S, GL\_TEXTURE\_WRAP\_T, and on the exact mapping.</span></span> <span data-ttu-id="6766d-181">\_最接近的 gl 通常比 gl \_ 線性更快，但它可以產生具有更清晰邊緣的紋理影像，因為材質元素之間的轉換不會像是平滑。</span><span class="sxs-lookup"><span data-stu-id="6766d-181">GL\_NEAREST is generally faster than GL\_LINEAR, but it can produce textured images with sharper edges because the transition between texture elements is not as smooth.</span></span> <span data-ttu-id="6766d-182">GL \_ 紋理 MAG 濾波器的預設 \_ 值 \_ 為 gl \_ 線性。</span><span class="sxs-lookup"><span data-stu-id="6766d-182">The default value of GL\_TEXTURE\_MAG\_FILTER is GL\_LINEAR.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6766d-183">傳回值</span><span class="sxs-lookup"><span data-stu-id="6766d-183">Return value</span></span>

<span data-ttu-id="6766d-184">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="6766d-184">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="6766d-185">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="6766d-185">Error codes</span></span>

<span data-ttu-id="6766d-186">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="6766d-186">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="6766d-187">Name</span><span class="sxs-lookup"><span data-stu-id="6766d-187">Name</span></span>                                                                                                  | <span data-ttu-id="6766d-188">意義</span><span class="sxs-lookup"><span data-stu-id="6766d-188">Meaning</span></span>                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6766d-189"><dt>**GL \_不正確 \_ 列舉**</dt></span><span class="sxs-lookup"><span data-stu-id="6766d-189"><dt>**GL\_INVALID\_ENUM** </dt></span></span> </dl>     | <span data-ttu-id="6766d-190">*target* 或 *pname* 不是其中一個接受的定義值，或是當 *param* 應該有定義的常數值 (根據 *pname*) 的值而不是時。</span><span class="sxs-lookup"><span data-stu-id="6766d-190">*target* or *pname* was not one of the accepted defined values, or when *param* should have had a defined constant value (based on the value of *pname*) and did not.</span></span><br/> |
| <dl> <span data-ttu-id="6766d-191"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="6766d-191"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="6766d-192">呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。</span><span class="sxs-lookup"><span data-stu-id="6766d-192">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/>                                            |



## <a name="remarks"></a><span data-ttu-id="6766d-193">備註</span><span class="sxs-lookup"><span data-stu-id="6766d-193">Remarks</span></span>

<span data-ttu-id="6766d-194">材質對應是一種技術，可將影像套用至物件的介面，就像影像是 decal 或 cellophane 壓縮包裝一樣。</span><span class="sxs-lookup"><span data-stu-id="6766d-194">Texture mapping is a technique that applies an image onto an object's surface as if the image were a decal or cellophane shrink-wrap.</span></span> <span data-ttu-id="6766d-195">影像會在材質空間中建立，其中包含 (*s*， *t*) 座標系統。</span><span class="sxs-lookup"><span data-stu-id="6766d-195">The image is created in texture space, with an (*s*, *t*) coordinate system.</span></span> <span data-ttu-id="6766d-196">材質是一或兩維度的影像，而一組參數會決定如何從影像衍生樣本。</span><span class="sxs-lookup"><span data-stu-id="6766d-196">A texture is a one- or two-dimensional image and a set of parameters that determine how samples are derived from the image.</span></span>

<span data-ttu-id="6766d-197">**GlTexParameter** 函式會將 params 中的值或值指派給指定為 pname 的材質參數。</span><span class="sxs-lookup"><span data-stu-id="6766d-197">The **glTexParameter** function assigns the value or values in params to the texture parameter specified as pname.</span></span> <span data-ttu-id="6766d-198">目標參數會定義目標材質，也就是 GL \_ 材質 \_ 1D 或 gl \_ 材質 \_ 2d。</span><span class="sxs-lookup"><span data-stu-id="6766d-198">The target parameter defines the target texture, either GL\_TEXTURE\_1D or GL\_TEXTURE\_2D.</span></span>

<span data-ttu-id="6766d-199">在縮制程式中取樣更多紋理專案時，會有較少的別名成品。</span><span class="sxs-lookup"><span data-stu-id="6766d-199">As more texture elements are sampled in the minification process, fewer aliasing artifacts will be apparent.</span></span> <span data-ttu-id="6766d-200">雖然 \_ 最接近的 gl 和 gl \_ 線性縮制函式可以比其他四個函式更快，但它們只會取樣一或四個材質元素，以判斷所轉譯圖元的材質值，而且可以產生 moire 模式或不完全的轉換。</span><span class="sxs-lookup"><span data-stu-id="6766d-200">While the GL\_NEAREST and GL\_LINEAR minification functions can be faster than the other four, they sample only one or four texture elements to determine the texture value of the pixel being rendered and can produce moire patterns or ragged transitions.</span></span> <span data-ttu-id="6766d-201">GL \_ 紋理 \_ 最小篩選的預設值 \_ 為 gl \_ 最接近 \_ MIPMAP 的 \_ 線性。</span><span class="sxs-lookup"><span data-stu-id="6766d-201">The default value of GL\_TEXTURE\_MIN\_FILTER is GL\_NEAREST\_MIPMAP\_LINEAR.</span></span>

<span data-ttu-id="6766d-202">假設 (藉由使用引數 GL [](glenable.md) \_ 紋理 \_ 1d 或 gl \_ 材質 2d) 來呼叫 glEnable \_ ，並 \_ 將 gl 材質 \_ MIN \_ 篩選設定為需要 mipmap 的其中一個函式，以啟用紋理。</span><span class="sxs-lookup"><span data-stu-id="6766d-202">Suppose that texturing is enabled (by calling [**glEnable**](glenable.md) with argument GL\_TEXTURE\_1D or GL\_TEXTURE\_2D) and GL\_TEXTURE\_MIN\_FILTER is set to one of the functions that requires a mipmap.</span></span> <span data-ttu-id="6766d-203">如果目前定義的材質影像維度 (與先前對 [**glTexImage1D**](glteximage1d.md) 或) [**glTexImage2D**](glteximage2d.md) 的呼叫不遵循正確的 mipmap 順序，或者定義的材質影像數目小於所需的材質影像，或紋理影像集合的材質元件數目不同，則會如同材質對應已停用一樣。</span><span class="sxs-lookup"><span data-stu-id="6766d-203">If either the dimensions of the texture images currently defined (with previous calls to [**glTexImage1D**](glteximage1d.md) or [**glTexImage2D**](glteximage2d.md)) do not follow the proper sequence for mipmaps, or there are fewer texture images defined than are needed, or the set of texture images have differing numbers of texture components, then it is as if texture mapping were disabled.</span></span> <span data-ttu-id="6766d-204">線性篩選只會存取2D 材質中四個最接近的材質元素。</span><span class="sxs-lookup"><span data-stu-id="6766d-204">Linear filtering accesses the four nearest texture elements only in 2-D textures.</span></span> <span data-ttu-id="6766d-205">在立體材質中，線性篩選會存取兩個最接近的材質元素。</span><span class="sxs-lookup"><span data-stu-id="6766d-205">In 1-D textures, linear filtering accesses the two nearest texture elements.</span></span> <span data-ttu-id="6766d-206">下列函式會抓取 **glTexParameterf**、 **glTexParameteri**、 **glTexParameterfv** 和 **glTexParameteriv** 的相關資訊：</span><span class="sxs-lookup"><span data-stu-id="6766d-206">The following function retrieves information related to **glTexParameterf**, **glTexParameteri**, **glTexParameterfv**, and **glTexParameteriv**:</span></span>

[<span data-ttu-id="6766d-207">**glGetTexParameter**</span><span class="sxs-lookup"><span data-stu-id="6766d-207">**glGetTexParameter**</span></span>](glgettexparameter.md)

## <a name="requirements"></a><span data-ttu-id="6766d-208">規格需求</span><span class="sxs-lookup"><span data-stu-id="6766d-208">Requirements</span></span>



| <span data-ttu-id="6766d-209">需求</span><span class="sxs-lookup"><span data-stu-id="6766d-209">Requirement</span></span> | <span data-ttu-id="6766d-210">值</span><span class="sxs-lookup"><span data-stu-id="6766d-210">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6766d-211">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6766d-211">Minimum supported client</span></span><br/> | <span data-ttu-id="6766d-212">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6766d-212">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="6766d-213">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6766d-213">Minimum supported server</span></span><br/> | <span data-ttu-id="6766d-214">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6766d-214">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6766d-215">標頭</span><span class="sxs-lookup"><span data-stu-id="6766d-215">Header</span></span><br/>                   | <dl> <span data-ttu-id="6766d-216"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="6766d-216"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="6766d-217">程式庫</span><span class="sxs-lookup"><span data-stu-id="6766d-217">Library</span></span><br/>                  | <dl> <span data-ttu-id="6766d-218"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="6766d-218"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="6766d-219">DLL</span><span class="sxs-lookup"><span data-stu-id="6766d-219">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6766d-220"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6766d-220"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6766d-221">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6766d-221">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6766d-222">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="6766d-222">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="6766d-223">**glBindTexture**</span><span class="sxs-lookup"><span data-stu-id="6766d-223">**glBindTexture**</span></span>](glbindtexture.md)
</dt> <dt>

[<span data-ttu-id="6766d-224">**glCopyPixels**</span><span class="sxs-lookup"><span data-stu-id="6766d-224">**glCopyPixels**</span></span>](glcopypixels.md)
</dt> <dt>

[<span data-ttu-id="6766d-225">**glCopyTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="6766d-225">**glCopyTexImage1D**</span></span>](glcopyteximage1d.md)
</dt> <dt>

[<span data-ttu-id="6766d-226">**glCopyTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="6766d-226">**glCopyTexImage2D**</span></span>](glcopyteximage2d.md)
</dt> <dt>

[<span data-ttu-id="6766d-227">**glCopyTexSubImage2D**</span><span class="sxs-lookup"><span data-stu-id="6766d-227">**glCopyTexSubImage2D**</span></span>](glcopytexsubimage2d.md)
</dt> <dt>

[<span data-ttu-id="6766d-228">**glDrawPixels**</span><span class="sxs-lookup"><span data-stu-id="6766d-228">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="6766d-229">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="6766d-229">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="6766d-230">**glGetTexParameter**</span><span class="sxs-lookup"><span data-stu-id="6766d-230">**glGetTexParameter**</span></span>](glgettexparameter.md)
</dt> <dt>

[<span data-ttu-id="6766d-231">**glPixelStore**</span><span class="sxs-lookup"><span data-stu-id="6766d-231">**glPixelStore**</span></span>](glpixelstore-functions.md)
</dt> <dt>

[<span data-ttu-id="6766d-232">**glPixelTransfer**</span><span class="sxs-lookup"><span data-stu-id="6766d-232">**glPixelTransfer**</span></span>](glpixeltransfer.md)
</dt> <dt>

[<span data-ttu-id="6766d-233">**glPrioritizeTextures**</span><span class="sxs-lookup"><span data-stu-id="6766d-233">**glPrioritizeTextures**</span></span>](glprioritizetextures.md)
</dt> <dt>

[<span data-ttu-id="6766d-234">glTexEnv</span><span class="sxs-lookup"><span data-stu-id="6766d-234">glTexEnv</span></span>](gltexenv-functions.md)
</dt> <dt>

[<span data-ttu-id="6766d-235">glTexGen</span><span class="sxs-lookup"><span data-stu-id="6766d-235">glTexGen</span></span>](gltexgen-functions.md)
</dt> <dt>

[<span data-ttu-id="6766d-236">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="6766d-236">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="6766d-237">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="6766d-237">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="6766d-238">**glTexSubImage1D**</span><span class="sxs-lookup"><span data-stu-id="6766d-238">**glTexSubImage1D**</span></span>](gltexsubimage1d.md)
</dt> <dt>

[<span data-ttu-id="6766d-239">**glTexSubImage2D**</span><span class="sxs-lookup"><span data-stu-id="6766d-239">**glTexSubImage2D**</span></span>](gltexsubimage2d.md)
</dt> </dl>

 

 





