---
title: 'glGetTexLevelParameteriv 函式 (Gl) '
description: 'GlGetTexLevelParameterfv 和 glGetTexLevelParameteriv 函數會傳回特定詳細資料層級的材質參數值。 |glGetTexLevelParameteriv 函式 (Gl) '
ms.assetid: 536d7bc9-1599-47ff-8559-374f96f1d5f3
keywords:
- glGetTexLevelParameteriv 函式 OpenGL
topic_type:
- apiref
api_name:
- glGetTexLevelParameteriv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfc0fa167eae842784e967538ff1539e0b43a6a2
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "103945826"
---
# <a name="glgettexlevelparameteriv-function"></a><span data-ttu-id="12522-105">glGetTexLevelParameteriv 函式</span><span class="sxs-lookup"><span data-stu-id="12522-105">glGetTexLevelParameteriv function</span></span>

<span data-ttu-id="12522-106">[**GlGetTexLevelParameterfv**](glgettexlevelparameterfv.md)和 **glGetTexLevelParameteriv** 函數會傳回特定詳細資料層級的材質參數值。</span><span class="sxs-lookup"><span data-stu-id="12522-106">The [**glGetTexLevelParameterfv**](glgettexlevelparameterfv.md) and **glGetTexLevelParameteriv** functions return texture parameter values for a specific level of detail.</span></span>

## <a name="syntax"></a><span data-ttu-id="12522-107">語法</span><span class="sxs-lookup"><span data-stu-id="12522-107">Syntax</span></span>


```C++
void WINAPI glGetTexLevelParameteriv(
   GLenum target,
   GLint  level,
   GLenum pname,
   GLint  *params
);
```



## <a name="parameters"></a><span data-ttu-id="12522-108">參數</span><span class="sxs-lookup"><span data-stu-id="12522-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12522-109">*目標*</span><span class="sxs-lookup"><span data-stu-id="12522-109">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="12522-110">目標材質的符號名稱： GL \_ 紋理 \_ 1D、gl \_ 材質 \_ 2d、gl \_ proxy \_ 材質 \_ 1d 或 gl \_ proxy \_ 材質 \_ 2d。</span><span class="sxs-lookup"><span data-stu-id="12522-110">The symbolic name of the target texture: either GL\_TEXTURE\_1D, GL\_TEXTURE\_2D, GL\_PROXY\_TEXTURE\_1D, or GL\_PROXY\_TEXTURE\_2D.</span></span>

</dd> <dt>

<span data-ttu-id="12522-111">*level*</span><span class="sxs-lookup"><span data-stu-id="12522-111">*level*</span></span> 
</dt> <dd>

<span data-ttu-id="12522-112">所需影像的詳細層級編號。</span><span class="sxs-lookup"><span data-stu-id="12522-112">The level-of-detail number of the desired image.</span></span> <span data-ttu-id="12522-113">層級0是基底映射層級。</span><span class="sxs-lookup"><span data-stu-id="12522-113">Level 0 is the base image level.</span></span> <span data-ttu-id="12522-114">層級 *n* 是第 *n* 個 mipmap 縮減影像。</span><span class="sxs-lookup"><span data-stu-id="12522-114">Level *n* is the *n* th mipmap reduction image.</span></span>

</dd> <dt>

<span data-ttu-id="12522-115">*pname*</span><span class="sxs-lookup"><span data-stu-id="12522-115">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="12522-116">材質參數的符號名稱。</span><span class="sxs-lookup"><span data-stu-id="12522-116">The symbolic name of a texture parameter.</span></span> <span data-ttu-id="12522-117">接受下列參數名稱。</span><span class="sxs-lookup"><span data-stu-id="12522-117">The following parameter names are accepted.</span></span>



| <span data-ttu-id="12522-118">值</span><span class="sxs-lookup"><span data-stu-id="12522-118">Value</span></span>                                                                                                                                                                                                  | <span data-ttu-id="12522-119">意義</span><span class="sxs-lookup"><span data-stu-id="12522-119">Meaning</span></span>                                                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_TEXTURE_WIDTH"></span><span id="gl_texture_width"></span><dl> <span data-ttu-id="12522-120"><dt>**GL \_ 材質 \_ 寬度**</dt></span><span class="sxs-lookup"><span data-stu-id="12522-120"><dt>**GL\_TEXTURE\_WIDTH**</dt></span></span> </dl>                                | <span data-ttu-id="12522-121">*Params* 參數會傳回包含紋理影像寬度的單一值。</span><span class="sxs-lookup"><span data-stu-id="12522-121">The *params* parameter returns a single value containing the width of the texture image.</span></span> <span data-ttu-id="12522-122">此值包含紋理影像的框線。</span><span class="sxs-lookup"><span data-stu-id="12522-122">This value includes the border of the texture image.</span></span><br/>                                                                                                                                          |
| <span id="GL_TEXTURE_HEIGHT"></span><span id="gl_texture_height"></span><dl> <span data-ttu-id="12522-123"><dt>**GL \_ 材質 \_ 高度**</dt></span><span class="sxs-lookup"><span data-stu-id="12522-123"><dt>**GL\_TEXTURE\_HEIGHT**</dt></span></span> </dl>                             | <span data-ttu-id="12522-124">*Params* 參數會傳回單一值，其中包含紋理影像的高度。</span><span class="sxs-lookup"><span data-stu-id="12522-124">The *params* parameter returns a single value containing the height of the texture image.</span></span> <span data-ttu-id="12522-125">此值包含紋理影像的框線。</span><span class="sxs-lookup"><span data-stu-id="12522-125">This value includes the border of the texture image.</span></span><br/>                                                                                                                                         |
| <span id="GL_TEXTURE_INTERNAL_FORMAT"></span><span id="gl_texture_internal_format"></span><dl> <span data-ttu-id="12522-126"><dt>**GL \_ 材質 \_ 內部 \_ 格式**</dt></span><span class="sxs-lookup"><span data-stu-id="12522-126"><dt>**GL\_TEXTURE\_INTERNAL\_FORMAT**</dt></span></span> </dl> | <span data-ttu-id="12522-127">*Params* 參數會傳回單一值，以描述材質的材質格式。</span><span class="sxs-lookup"><span data-stu-id="12522-127">The *params* parameter returns a single value which describes the texel format of the texture.</span></span><br/>                                                                                                                                                                                         |
| <span id="GL_TEXTURE_BORDER"></span><span id="gl_texture_border"></span><dl> <span data-ttu-id="12522-128"><dt>**GL \_ 材質 \_ 框線**</dt></span><span class="sxs-lookup"><span data-stu-id="12522-128"><dt>**GL\_TEXTURE\_BORDER**</dt></span></span> </dl>                             | <span data-ttu-id="12522-129">*Params* 參數會傳回單一值：紋理影像框線的寬度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="12522-129">The *params* parameter returns a single value: the width in pixels of the border of the texture image.</span></span><br/>                                                                                                                                                                                 |
| <span id="GL_TEXTURE_RED_SIZE"></span><span id="gl_texture_red_size"></span><dl> <span data-ttu-id="12522-130"><dt>**GL \_ 材質 \_ 紅色 \_ 大小**</dt></span><span class="sxs-lookup"><span data-stu-id="12522-130"><dt>**GL\_TEXTURE\_RED\_SIZE**</dt></span></span> </dl>                      | <span data-ttu-id="12522-131">材質 red 元件的內部儲存體解析。</span><span class="sxs-lookup"><span data-stu-id="12522-131">The internal storage resolution of the red component of a texel.</span></span> <span data-ttu-id="12522-132">OpenGL 所選擇的解析度將會與使用者使用 [**glTexImage1D**](glteximage1d.md) 或 [**glTexImage2D**](glteximage2d.md)的元件引數所要求的解析度相符。</span><span class="sxs-lookup"><span data-stu-id="12522-132">The resolution chosen by the OpenGL will be a close match for the resolution requested by the user with the component argument of [**glTexImage1D**](glteximage1d.md) or [**glTexImage2D**](glteximage2d.md).</span></span><br/>       |
| <span id="GL_TEXTURE_GREEN_SIZE"></span><span id="gl_texture_green_size"></span><dl> <span data-ttu-id="12522-133"><dt>**GL \_ 材質 \_ 綠 \_ 尺寸**</dt></span><span class="sxs-lookup"><span data-stu-id="12522-133"><dt>**GL\_TEXTURE\_GREEN\_SIZE**</dt></span></span> </dl>                | <span data-ttu-id="12522-134">材質綠色元件的內部儲存體解析。</span><span class="sxs-lookup"><span data-stu-id="12522-134">The internal storage resolution of the green component of a texel.</span></span> <span data-ttu-id="12522-135">OpenGL 所選擇的解析度將會與使用者使用 [**glTexImage1D**](glteximage1d.md) 或 [**glTexImage2D**](glteximage2d.md)的元件引數所要求的解析度相符。</span><span class="sxs-lookup"><span data-stu-id="12522-135">The resolution chosen by the OpenGL will be a close match for the resolution requested by the user with the component argument of [**glTexImage1D**](glteximage1d.md) or [**glTexImage2D**](glteximage2d.md).</span></span><br/>     |
| <span id="GL_TEXTURE_BLUE_SIZE"></span><span id="gl_texture_blue_size"></span><dl> <span data-ttu-id="12522-136"><dt>**GL \_ 材質 \_ 藍色 \_ 大小**</dt></span><span class="sxs-lookup"><span data-stu-id="12522-136"><dt>**GL\_TEXTURE\_BLUE\_SIZE**</dt></span></span> </dl>                   | <span data-ttu-id="12522-137">材質藍色元件的內部儲存體解析。</span><span class="sxs-lookup"><span data-stu-id="12522-137">The internal storage resolution of the blue component of a texel.</span></span> <span data-ttu-id="12522-138">OpenGL 所選擇的解析度將會與使用者使用 [**glTexImage1D**](glteximage1d.md) 或 [**glTexImage2D**](glteximage2d.md)的元件引數所要求的解析度相符。</span><span class="sxs-lookup"><span data-stu-id="12522-138">The resolution chosen by the OpenGL will be a close match for the resolution requested by the user with the component argument of [**glTexImage1D**](glteximage1d.md) or [**glTexImage2D**](glteximage2d.md).</span></span><br/>      |
| <span id="GL_TEXTURE_ALPHA_SIZE"></span><span id="gl_texture_alpha_size"></span><dl> <span data-ttu-id="12522-139"><dt>**GL \_ 紋理 \_ ALPHA \_ 大小**</dt></span><span class="sxs-lookup"><span data-stu-id="12522-139"><dt>**GL\_TEXTURE\_ALPHA\_SIZE**</dt></span></span> </dl>                | <span data-ttu-id="12522-140">材質 Alpha 元件的內部儲存體解析。</span><span class="sxs-lookup"><span data-stu-id="12522-140">The internal storage resolution of the alpha component of a texel.</span></span> <span data-ttu-id="12522-141">OpenGL 所選擇的解析度將會與使用者使用 [**glTexImage1D**](glteximage1d.md) 或 [**glTexImage2D**](glteximage2d.md)的元件引數所要求的解析度相符。</span><span class="sxs-lookup"><span data-stu-id="12522-141">The resolution chosen by the OpenGL will be a close match for the resolution requested by the user with the component argument of [**glTexImage1D**](glteximage1d.md) or [**glTexImage2D**](glteximage2d.md).</span></span><br/>     |
| <span id="GL_TEXTURE_LUMINANCE_SIZE"></span><span id="gl_texture_luminance_size"></span><dl> <span data-ttu-id="12522-142"><dt>**GL \_ 紋理 \_ 亮度 \_ 大小**</dt></span><span class="sxs-lookup"><span data-stu-id="12522-142"><dt>**GL\_TEXTURE\_LUMINANCE\_SIZE**</dt></span></span> </dl>    | <span data-ttu-id="12522-143">材質之明亮元件的內部儲存體解析。</span><span class="sxs-lookup"><span data-stu-id="12522-143">The internal storage resolution of the luminance component of a texel.</span></span> <span data-ttu-id="12522-144">OpenGL 所選擇的解析度將會與使用者使用 [**glTexImage1D**](glteximage1d.md) 或 [**glTexImage2D**](glteximage2d.md)的元件引數所要求的解析度相符。</span><span class="sxs-lookup"><span data-stu-id="12522-144">The resolution chosen by the OpenGL will be a close match for the resolution requested by the user with the component argument of [**glTexImage1D**](glteximage1d.md) or [**glTexImage2D**](glteximage2d.md).</span></span><br/> |
| <span id="GL_TEXTURE_INTENSITY_SIZE"></span><span id="gl_texture_intensity_size"></span><dl> <span data-ttu-id="12522-145"><dt>**GL \_ 材質 \_ 濃度 \_ 大小**</dt></span><span class="sxs-lookup"><span data-stu-id="12522-145"><dt>**GL\_TEXTURE\_INTENSITY\_SIZE**</dt></span></span> </dl>    | <span data-ttu-id="12522-146">材質濃度元件的內部儲存體解析。</span><span class="sxs-lookup"><span data-stu-id="12522-146">The internal storage resolution of the intensity component of a texel.</span></span> <span data-ttu-id="12522-147">OpenGL 所選擇的解析度將會與使用者使用 [**glTexImage1D**](glteximage1d.md) 或 [**glTexImage2D**](glteximage2d.md)的元件引數所要求的解析度相符。</span><span class="sxs-lookup"><span data-stu-id="12522-147">The resolution chosen by the OpenGL will be a close match for the resolution requested by the user with the component argument of [**glTexImage1D**](glteximage1d.md) or [**glTexImage2D**](glteximage2d.md).</span></span><br/> |
| <span id="GL_TEXTURE_COMPONENTS"></span><span id="gl_texture_components"></span><dl> <span data-ttu-id="12522-148"><dt>**GL \_ 材質 \_ 元件**</dt></span><span class="sxs-lookup"><span data-stu-id="12522-148"><dt>**GL\_TEXTURE\_COMPONENTS**</dt></span></span> </dl>                 | <span data-ttu-id="12522-149">*Params* 參數會傳回單一值：材質影像中的元件數目。</span><span class="sxs-lookup"><span data-stu-id="12522-149">The *params* parameter returns a single value: the number of components in the texture image.</span></span><br/>                                                                                                                                                                                          |



 

</dd> <dt>

<span data-ttu-id="12522-150">*params*</span><span class="sxs-lookup"><span data-stu-id="12522-150">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="12522-151">傳回要求的資料。</span><span class="sxs-lookup"><span data-stu-id="12522-151">Returns the requested data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12522-152">傳回值</span><span class="sxs-lookup"><span data-stu-id="12522-152">Return value</span></span>

<span data-ttu-id="12522-153">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="12522-153">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="12522-154">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="12522-154">Error codes</span></span>

<span data-ttu-id="12522-155">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="12522-155">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="12522-156">Name</span><span class="sxs-lookup"><span data-stu-id="12522-156">Name</span></span>                                                                                                  | <span data-ttu-id="12522-157">意義</span><span class="sxs-lookup"><span data-stu-id="12522-157">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="12522-158"><dt>**GL \_ 無效 \_ 列舉**</dt></span><span class="sxs-lookup"><span data-stu-id="12522-158"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="12522-159">*target* 或 *pname* 不是可接受的值。</span><span class="sxs-lookup"><span data-stu-id="12522-159">*target* or *pname* was not an accepted value.</span></span><br/>                                                                             |
| <dl> <span data-ttu-id="12522-160"><dt>**GL \_ 無效 \_ 值**</dt></span><span class="sxs-lookup"><span data-stu-id="12522-160"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="12522-161">*層級* 小於零或大於 *log* 2 *(max)*，其中 *max* 是 GL \_ 最大 \_ 紋理大小的傳回值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="12522-161">*level* is less than zero or greater than *log* 2 *(max)*, where *max* is the returned value of GL\_MAX\_TEXTURE\_SIZE.</span></span><br/>      |
| <dl> <span data-ttu-id="12522-162"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="12522-162"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="12522-163">呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。</span><span class="sxs-lookup"><span data-stu-id="12522-163">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="12522-164">備註</span><span class="sxs-lookup"><span data-stu-id="12522-164">Remarks</span></span>

<span data-ttu-id="12522-165">**GlGetTexLevelParameter** 函式會針對特定的詳細層級值（指定為 *層級*），傳回 *params* 材質參數值。</span><span class="sxs-lookup"><span data-stu-id="12522-165">The **glGetTexLevelParameter** function returns in *params* texture parameter values for a specific level-of-detail value, specified as *level*.</span></span> <span data-ttu-id="12522-166">*目標* 參數會定義目標材質，也就是 gl \_ 紋理 \_ 1d、GL \_ 材質 \_ 2d、gl \_ proxy \_ 材質 \_ 1d 或 gl \_ proxy \_ 材質 \_ 2d，以指定一維或二維紋理。</span><span class="sxs-lookup"><span data-stu-id="12522-166">The *target* parameter defines the target texture, either GL\_TEXTURE\_1D, GL\_TEXTURE\_2D, GL\_PROXY\_TEXTURE\_1D, or GL\_PROXY\_TEXTURE\_2D to specify one-dimensional or two-dimensional texturing.</span></span> <span data-ttu-id="12522-167">*Pname* 參數會指定將傳回其值的材質參數。</span><span class="sxs-lookup"><span data-stu-id="12522-167">The *pname* parameter specifies the texture parameter whose value or values will be returned.</span></span>

<span data-ttu-id="12522-168">如果產生錯誤，則不會對 *參數* 的內容進行任何變更。</span><span class="sxs-lookup"><span data-stu-id="12522-168">If an error is generated, no change is made to the contents of *params*.</span></span>

## <a name="requirements"></a><span data-ttu-id="12522-169">規格需求</span><span class="sxs-lookup"><span data-stu-id="12522-169">Requirements</span></span>



| <span data-ttu-id="12522-170">需求</span><span class="sxs-lookup"><span data-stu-id="12522-170">Requirement</span></span> | <span data-ttu-id="12522-171">值</span><span class="sxs-lookup"><span data-stu-id="12522-171">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="12522-172">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="12522-172">Minimum supported client</span></span><br/> | <span data-ttu-id="12522-173">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="12522-173">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="12522-174">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="12522-174">Minimum supported server</span></span><br/> | <span data-ttu-id="12522-175">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="12522-175">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="12522-176">標頭</span><span class="sxs-lookup"><span data-stu-id="12522-176">Header</span></span><br/>                   | <dl> <span data-ttu-id="12522-177"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="12522-177"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="12522-178">程式庫</span><span class="sxs-lookup"><span data-stu-id="12522-178">Library</span></span><br/>                  | <dl> <span data-ttu-id="12522-179"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="12522-179"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="12522-180">DLL</span><span class="sxs-lookup"><span data-stu-id="12522-180">DLL</span></span><br/>                      | <dl> <span data-ttu-id="12522-181"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="12522-181"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12522-182">另請參閱</span><span class="sxs-lookup"><span data-stu-id="12522-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12522-183">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="12522-183">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="12522-184">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="12522-184">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="12522-185">**glGetTexParameter**</span><span class="sxs-lookup"><span data-stu-id="12522-185">**glGetTexParameter**</span></span>](glgettexparameter.md)
</dt> <dt>

[<span data-ttu-id="12522-186">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="12522-186">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="12522-187">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="12522-187">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="12522-188">**glTexParameter**</span><span class="sxs-lookup"><span data-stu-id="12522-188">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> </dl>

 

 





