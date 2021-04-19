---
title: 'glGetTexParameteriv 函式 (Gl) '
description: 'GlGetTexParameterfv 和 glGetTexParameteriv 函數會傳回材質參數值。 |glGetTexParameteriv 函式 (Gl) '
ms.assetid: b89d10f1-5e30-4d25-8953-fbd59781fdac
keywords:
- glGetTexParameteriv 函式 OpenGL
topic_type:
- apiref
api_name:
- glGetTexParameteriv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ca78983594487fd22917c15a5b211c529b6b14d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106981241"
---
# <a name="glgettexparameteriv-function"></a><span data-ttu-id="bc2e4-105">glGetTexParameteriv 函式</span><span class="sxs-lookup"><span data-stu-id="bc2e4-105">glGetTexParameteriv function</span></span>

<span data-ttu-id="bc2e4-106">[**GlGetTexParameterfv**](glgettexparameterfv.md)和 **glGetTexParameteriv** 函數會傳回材質參數值。</span><span class="sxs-lookup"><span data-stu-id="bc2e4-106">The [**glGetTexParameterfv**](glgettexparameterfv.md) and **glGetTexParameteriv** functions return texture parameter values.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc2e4-107">語法</span><span class="sxs-lookup"><span data-stu-id="bc2e4-107">Syntax</span></span>


```C++
void WINAPI glGetTexParameteriv(
   GLenum target,
   GLenum pname,
   GLint  *params
);
```



## <a name="parameters"></a><span data-ttu-id="bc2e4-108">參數</span><span class="sxs-lookup"><span data-stu-id="bc2e4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc2e4-109">*目標*</span><span class="sxs-lookup"><span data-stu-id="bc2e4-109">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="bc2e4-110">目標材質的符號名稱。</span><span class="sxs-lookup"><span data-stu-id="bc2e4-110">The symbolic name of the target texture.</span></span> <span data-ttu-id="bc2e4-111">\_ \_ 已接受 gl 材質1D 和 gl \_ 材質 \_ 2d。</span><span class="sxs-lookup"><span data-stu-id="bc2e4-111">GL\_TEXTURE\_1D and GL\_TEXTURE\_2D are accepted.</span></span>

</dd> <dt>

<span data-ttu-id="bc2e4-112">*pname*</span><span class="sxs-lookup"><span data-stu-id="bc2e4-112">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="bc2e4-113">材質參數的符號名稱。</span><span class="sxs-lookup"><span data-stu-id="bc2e4-113">The symbolic name of a texture parameter.</span></span> <span data-ttu-id="bc2e4-114">接受下列值。</span><span class="sxs-lookup"><span data-stu-id="bc2e4-114">The following values are accepted.</span></span>



| <span data-ttu-id="bc2e4-115">值</span><span class="sxs-lookup"><span data-stu-id="bc2e4-115">Value</span></span>                                                                                                                                                                                         | <span data-ttu-id="bc2e4-116">意義</span><span class="sxs-lookup"><span data-stu-id="bc2e4-116">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_TEXTURE_MAG_FILTER"></span><span id="gl_texture_mag_filter"></span><dl> <span data-ttu-id="bc2e4-117"><dt>**GL \_ 紋理 \_ MAG \_ 篩選**</dt></span><span class="sxs-lookup"><span data-stu-id="bc2e4-117"><dt>**GL\_TEXTURE\_MAG\_FILTER**</dt></span></span> </dl>       | <span data-ttu-id="bc2e4-118">傳回單一值材質放大篩選準則（符號常數）。</span><span class="sxs-lookup"><span data-stu-id="bc2e4-118">Returns the single-valued texture magnification filter, a symbolic constant.</span></span><br/>                                                                                                                                                                                                                                                                                                      |
| <span id="GL_TEXTURE_MIN_FILTER"></span><span id="gl_texture_min_filter"></span><dl> <span data-ttu-id="bc2e4-119"><dt>**GL \_ 材質 \_ 最小 \_ 篩選**</dt></span><span class="sxs-lookup"><span data-stu-id="bc2e4-119"><dt>**GL\_TEXTURE\_MIN\_FILTER**</dt></span></span> </dl>       | <span data-ttu-id="bc2e4-120">傳回單一值紋理縮制篩選（符號常數）。</span><span class="sxs-lookup"><span data-stu-id="bc2e4-120">Returns the single-valued texture minification filter, a symbolic constant.</span></span><br/>                                                                                                                                                                                                                                                                                                       |
| <span id="GL_TEXTURE_WRAP_S"></span><span id="gl_texture_wrap_s"></span><dl> <span data-ttu-id="bc2e4-121"><dt>**GL \_ 材質 \_ 換行 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="bc2e4-121"><dt>**GL\_TEXTURE\_WRAP\_S**</dt></span></span> </dl>                   | <span data-ttu-id="bc2e4-122">傳回紋理座標 *s* 的單一值換行函式，這是一個符號常數。</span><span class="sxs-lookup"><span data-stu-id="bc2e4-122">Returns the single-valued wrapping function for texture coordinate *s*, a symbolic constant.</span></span><br/>                                                                                                                                                                                                                                                                                      |
| <span id="GL_TEXTURE_WRAP_T"></span><span id="gl_texture_wrap_t"></span><dl> <span data-ttu-id="bc2e4-123"><dt>**GL \_ 紋理 \_ WRAP \_ T**</dt></span><span class="sxs-lookup"><span data-stu-id="bc2e4-123"><dt>**GL\_TEXTURE\_WRAP\_T**</dt></span></span> </dl>                   | <span data-ttu-id="bc2e4-124">傳回紋理座標 *t*（符號常數）的單一值包裝函式。</span><span class="sxs-lookup"><span data-stu-id="bc2e4-124">Returns the single-valued wrapping function for texture coordinate *t*, a symbolic constant.</span></span><br/>                                                                                                                                                                                                                                                                                      |
| <span id="GL_TEXTURE_BORDER_COLOR"></span><span id="gl_texture_border_color"></span><dl> <span data-ttu-id="bc2e4-125"><dt>**GL \_ 紋理 \_ 框線 \_ 色彩**</dt></span><span class="sxs-lookup"><span data-stu-id="bc2e4-125"><dt>**GL\_TEXTURE\_BORDER\_COLOR**</dt></span></span> </dl> | <span data-ttu-id="bc2e4-126">傳回四個整數或浮點數，這些數位組成材質框線的 RGBA 色彩。</span><span class="sxs-lookup"><span data-stu-id="bc2e4-126">Returns four integer or floating-point numbers that comprise the RGBA color of the texture border.</span></span> <span data-ttu-id="bc2e4-127">浮點值會傳回範圍 \[ 0，1 \] 。</span><span class="sxs-lookup"><span data-stu-id="bc2e4-127">Floating-point values are returned in the range \[0,1\].</span></span> <span data-ttu-id="bc2e4-128">整數值會傳回為內部浮點表示的線性對應，因此，1.0 對應至最正面的可表示整數，而-1.0 對應至最大的可表示整數。</span><span class="sxs-lookup"><span data-stu-id="bc2e4-128">Integer values are returned as a linear mapping of the internal floating-point representation such that 1.0 maps to the most positive representable integer and -1.0 maps to the most negative representable integer.</span></span><br/> |
| <span id="GL_TEXTURE_PRIORITY"></span><span id="gl_texture_priority"></span><dl> <span data-ttu-id="bc2e4-129"><dt>**GL \_ 材質 \_ 優先順序**</dt></span><span class="sxs-lookup"><span data-stu-id="bc2e4-129"><dt>**GL\_TEXTURE\_PRIORITY**</dt></span></span> </dl>              | <span data-ttu-id="bc2e4-130">傳回目標材質 (的居住優先權，或系結至它) 的命名材質。</span><span class="sxs-lookup"><span data-stu-id="bc2e4-130">Returns the residence priority of the target texture (or the named texture bound to it).</span></span> <span data-ttu-id="bc2e4-131">初始值為1。</span><span class="sxs-lookup"><span data-stu-id="bc2e4-131">The initial value is 1.</span></span> <span data-ttu-id="bc2e4-132">請參閱 [**glPrioritizeTextures**](glprioritizetextures.md)。</span><span class="sxs-lookup"><span data-stu-id="bc2e4-132">See [**glPrioritizeTextures**](glprioritizetextures.md).</span></span><br/>                                                                                                                                                                                                        |
| <span id="GL_TEXTURE_RESIDENT"></span><span id="gl_texture_resident"></span><dl> <span data-ttu-id="bc2e4-133"><dt>**GL \_ 材質 \_ 常駐**</dt></span><span class="sxs-lookup"><span data-stu-id="bc2e4-133"><dt>**GL\_TEXTURE\_RESIDENT**</dt></span></span> </dl>              | <span data-ttu-id="bc2e4-134">傳回目標材質的居住狀態。</span><span class="sxs-lookup"><span data-stu-id="bc2e4-134">Returns the residence status of the target texture.</span></span> <span data-ttu-id="bc2e4-135">如果在 params 中傳回的值為 GL \_ ，則紋理會在材質記憶體中。</span><span class="sxs-lookup"><span data-stu-id="bc2e4-135">If the value returned in params is GL\_TRUE, the texture is resident in texture memory.</span></span> <span data-ttu-id="bc2e4-136">請參閱 [**glAreTexturesResident**](glaretexturesresident.md)。</span><span class="sxs-lookup"><span data-stu-id="bc2e4-136">See [**glAreTexturesResident**](glaretexturesresident.md).</span></span><br/>                                                                                                                                                                           |



 

</dd> <dt>

<span data-ttu-id="bc2e4-137">*params*</span><span class="sxs-lookup"><span data-stu-id="bc2e4-137">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="bc2e4-138">傳回材質參數。</span><span class="sxs-lookup"><span data-stu-id="bc2e4-138">Returns the texture parameters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc2e4-139">傳回值</span><span class="sxs-lookup"><span data-stu-id="bc2e4-139">Return value</span></span>

<span data-ttu-id="bc2e4-140">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="bc2e4-140">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="bc2e4-141">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="bc2e4-141">Error codes</span></span>

<span data-ttu-id="bc2e4-142">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="bc2e4-142">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="bc2e4-143">Name</span><span class="sxs-lookup"><span data-stu-id="bc2e4-143">Name</span></span>                                                                                                  | <span data-ttu-id="bc2e4-144">意義</span><span class="sxs-lookup"><span data-stu-id="bc2e4-144">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="bc2e4-145"><dt>**GL \_ 無效 \_ 列舉**</dt></span><span class="sxs-lookup"><span data-stu-id="bc2e4-145"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="bc2e4-146">*目標* 或 *名稱* 不是可接受的值。</span><span class="sxs-lookup"><span data-stu-id="bc2e4-146">*target* or *name* was not an accepted value.</span></span><br/>                                                                              |
| <dl> <span data-ttu-id="bc2e4-147"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="bc2e4-147"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="bc2e4-148">呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。</span><span class="sxs-lookup"><span data-stu-id="bc2e4-148">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="bc2e4-149">備註</span><span class="sxs-lookup"><span data-stu-id="bc2e4-149">Remarks</span></span>

<span data-ttu-id="bc2e4-150">**GlGetTexParameter** 函式會以 *params* 傳回指定為 *pname* 的材質參數值或值。</span><span class="sxs-lookup"><span data-stu-id="bc2e4-150">The **glGetTexParameter** function returns in *params* the value or values of the texture parameter specified as *pname*.</span></span> <span data-ttu-id="bc2e4-151">*目標* 參數會定義目標材質，也就是 gl \_ 材質 \_ 1d 或 gl \_ 材質 \_ 2d，以指定一維或二維紋理。</span><span class="sxs-lookup"><span data-stu-id="bc2e4-151">The *target* parameter defines the target texture, either GL\_TEXTURE\_1D or GL\_TEXTURE\_2D, to specify one-dimensional or two-dimensional texturing.</span></span> <span data-ttu-id="bc2e4-152">*Pname* 參數會接受與 [**glTexParameter**](gltexparameter-functions.md)相同的符號，並具有相同的解釋。</span><span class="sxs-lookup"><span data-stu-id="bc2e4-152">The *pname* parameter accepts the same symbols as [**glTexParameter**](gltexparameter-functions.md), with the same interpretations.</span></span>

<span data-ttu-id="bc2e4-153">如果產生錯誤，則不會對 *參數* 的內容進行任何變更。</span><span class="sxs-lookup"><span data-stu-id="bc2e4-153">If an error is generated, no change is made to the contents of *params*.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc2e4-154">規格需求</span><span class="sxs-lookup"><span data-stu-id="bc2e4-154">Requirements</span></span>



| <span data-ttu-id="bc2e4-155">需求</span><span class="sxs-lookup"><span data-stu-id="bc2e4-155">Requirement</span></span> | <span data-ttu-id="bc2e4-156">值</span><span class="sxs-lookup"><span data-stu-id="bc2e4-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bc2e4-157">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bc2e4-157">Minimum supported client</span></span><br/> | <span data-ttu-id="bc2e4-158">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bc2e4-158">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="bc2e4-159">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bc2e4-159">Minimum supported server</span></span><br/> | <span data-ttu-id="bc2e4-160">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bc2e4-160">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="bc2e4-161">標頭</span><span class="sxs-lookup"><span data-stu-id="bc2e4-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="bc2e4-162"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="bc2e4-162"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="bc2e4-163">程式庫</span><span class="sxs-lookup"><span data-stu-id="bc2e4-163">Library</span></span><br/>                  | <dl> <span data-ttu-id="bc2e4-164"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="bc2e4-164"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="bc2e4-165">DLL</span><span class="sxs-lookup"><span data-stu-id="bc2e4-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bc2e4-166"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bc2e4-166"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc2e4-167">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bc2e4-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc2e4-168">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="bc2e4-168">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="bc2e4-169">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="bc2e4-169">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="bc2e4-170">**glTexParameter**</span><span class="sxs-lookup"><span data-stu-id="bc2e4-170">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> </dl>

 

 





