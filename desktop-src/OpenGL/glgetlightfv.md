---
title: 'glGetLightfv 函式 (Gl) '
description: 'GlGetLightfv 和 glGetLightiv 函數會傳回燈光來源參數值。 |glGetLightfv 函式 (Gl) '
ms.assetid: 81049726-426e-4f90-bb8e-e5d467870260
keywords:
- glGetLightfv 函式 OpenGL
topic_type:
- apiref
api_name:
- glGetLightfv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: faf90cb9567822ef578bdf01805648a2dabd02db
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "103853668"
---
# <a name="glgetlightfv-function"></a><span data-ttu-id="b7303-105">glGetLightfv 函式</span><span class="sxs-lookup"><span data-stu-id="b7303-105">glGetLightfv function</span></span>

<span data-ttu-id="b7303-106">**GlGetLightfv** 和 [**glGetLightiv**](glgetlightiv.md)函數會傳回燈光來源參數值。</span><span class="sxs-lookup"><span data-stu-id="b7303-106">The **glGetLightfv** and [**glGetLightiv**](glgetlightiv.md) functions return light source parameter values.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7303-107">語法</span><span class="sxs-lookup"><span data-stu-id="b7303-107">Syntax</span></span>


```C++
void WINAPI glGetLightfv(
   GLenum  light,
   GLenum  pname,
   GLfloat *params
);
```



## <a name="parameters"></a><span data-ttu-id="b7303-108">參數</span><span class="sxs-lookup"><span data-stu-id="b7303-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7303-109">*light*</span><span class="sxs-lookup"><span data-stu-id="b7303-109">*light*</span></span> 
</dt> <dd>

<span data-ttu-id="b7303-110">燈光來源。</span><span class="sxs-lookup"><span data-stu-id="b7303-110">A light source.</span></span> <span data-ttu-id="b7303-111">可能的燈光數目取決於執行，但至少有8個燈支援。</span><span class="sxs-lookup"><span data-stu-id="b7303-111">The number of possible lights depends on the implementation, but at least eight lights are supported.</span></span> <span data-ttu-id="b7303-112">其識別方式是以 GL 燈的符號名稱 \_ 來 *識別，* 其中 0 = *i* < GL \_ 最大 \_ 燈。</span><span class="sxs-lookup"><span data-stu-id="b7303-112">They are identified by symbolic names of the form GL\_LIGHT *i* where 0 = *i* < GL\_MAX\_LIGHTS.</span></span>

</dd> <dt>

<span data-ttu-id="b7303-113">*pname*</span><span class="sxs-lookup"><span data-stu-id="b7303-113">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="b7303-114">*Light* 的光源參數。</span><span class="sxs-lookup"><span data-stu-id="b7303-114">A light source parameter for *light*.</span></span> <span data-ttu-id="b7303-115">接受下列符號名稱。</span><span class="sxs-lookup"><span data-stu-id="b7303-115">The following symbolic names are accepted.</span></span>



| <span data-ttu-id="b7303-116">值</span><span class="sxs-lookup"><span data-stu-id="b7303-116">Value</span></span>                                                                                                                                                                                           | <span data-ttu-id="b7303-117">意義</span><span class="sxs-lookup"><span data-stu-id="b7303-117">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_AMBIENT"></span><span id="gl_ambient"></span><dl> <span data-ttu-id="b7303-118"><dt>**GL \_ 環境**</dt></span><span class="sxs-lookup"><span data-stu-id="b7303-118"><dt>**GL\_AMBIENT**</dt></span></span> </dl>                                            | <span data-ttu-id="b7303-119">*Params* 參數會傳回四個整數或浮點值，代表光線來源的環境濃度。</span><span class="sxs-lookup"><span data-stu-id="b7303-119">The *params* parameter returns four integer or floating-point values representing the ambient intensity of the light source.</span></span> <span data-ttu-id="b7303-120">在要求時，整數值會以線性方式從內部浮點表示對應，因此，1.0 對應到最大的可表示整數值，而-1.0 則對應至最大的可表示整數值。</span><span class="sxs-lookup"><span data-stu-id="b7303-120">Integer values, when requested, are linearly mapped from the internal floating-point representation such that 1.0 maps to the most positive representable integer value, and -1.0 maps to the most negative representable integer value.</span></span> <span data-ttu-id="b7303-121">如果內部值超出範圍 \[ -1、1 \] ，則對應的整數傳回值為未定義。</span><span class="sxs-lookup"><span data-stu-id="b7303-121">If the internal value is outside the range \[-1,1\], the corresponding integer return value is undefined.</span></span><br/>                                                                                                                                                                  |
| <span id="GL_DIFFUSE"></span><span id="gl_diffuse"></span><dl> <span data-ttu-id="b7303-122"><dt>**GL \_ 擴散**</dt></span><span class="sxs-lookup"><span data-stu-id="b7303-122"><dt>**GL\_DIFFUSE**</dt></span></span> </dl>                                            | <span data-ttu-id="b7303-123">*Params* 參數會傳回四個整數或浮點值，代表光線來源的擴散濃度。</span><span class="sxs-lookup"><span data-stu-id="b7303-123">The *params* parameter returns four integer or floating-point values representing the diffuse intensity of the light source.</span></span> <span data-ttu-id="b7303-124">在要求時，整數值會以線性方式從內部浮點表示對應，因此，1.0 對應到最大的可表示整數值，而-1.0 則對應至最大的可表示整數值。</span><span class="sxs-lookup"><span data-stu-id="b7303-124">Integer values, when requested, are linearly mapped from the internal floating-point representation such that 1.0 maps to the most positive representable integer value, and -1.0 maps to the most negative representable integer value.</span></span> <span data-ttu-id="b7303-125">如果內部值超出範圍 \[ -1、1 \] ，則對應的整數傳回值為未定義。</span><span class="sxs-lookup"><span data-stu-id="b7303-125">If the internal value is outside the range \[-1,1\], the corresponding integer return value is undefined.</span></span><br/>                                                                                                                                                                  |
| <span id="GL_SPECULAR"></span><span id="gl_specular"></span><dl> <span data-ttu-id="b7303-126"><dt>**GL \_ 反射**</dt></span><span class="sxs-lookup"><span data-stu-id="b7303-126"><dt>**GL\_SPECULAR**</dt></span></span> </dl>                                         | <span data-ttu-id="b7303-127">*Params* 參數會傳回四個整數或浮點值，代表光線來源的反射濃度。</span><span class="sxs-lookup"><span data-stu-id="b7303-127">The *params* parameter returns four integer or floating-point values representing the specular intensity of the light source.</span></span> <span data-ttu-id="b7303-128">在要求時，整數值會以線性方式從內部浮點表示對應，因此，1.0 對應到最大的可表示整數值，而-1.0 則對應至最大的可表示整數值。</span><span class="sxs-lookup"><span data-stu-id="b7303-128">Integer values, when requested, are linearly mapped from the internal floating-point representation such that 1.0 maps to the most positive representable integer value, and -1.0 maps to the most negative representable integer value.</span></span> <span data-ttu-id="b7303-129">如果內部值超出範圍 \[ -1、1 \] ，則對應的整數傳回值為未定義。</span><span class="sxs-lookup"><span data-stu-id="b7303-129">If the internal value is outside the range \[-1,1\], the corresponding integer return value is undefined.</span></span><br/>                                                                                                                                                                 |
| <span id="GL_POSITION"></span><span id="gl_position"></span><dl> <span data-ttu-id="b7303-130"><dt>**GL \_ 位置**</dt></span><span class="sxs-lookup"><span data-stu-id="b7303-130"><dt>**GL\_POSITION**</dt></span></span> </dl>                                         | <span data-ttu-id="b7303-131">*Params* 參數會傳回四個整數或浮點值，代表光線來源的位置。</span><span class="sxs-lookup"><span data-stu-id="b7303-131">The *params* parameter returns four integer or floating-point values representing the position of the light source.</span></span> <span data-ttu-id="b7303-132">在要求時，整數值會藉由將內部浮點值四捨五入為最接近的整數值來計算。</span><span class="sxs-lookup"><span data-stu-id="b7303-132">Integer values, when requested, are computed by rounding the internal floating-point values to the nearest integer value.</span></span> <span data-ttu-id="b7303-133">傳回的值是以眼睛座標維持的值。</span><span class="sxs-lookup"><span data-stu-id="b7303-133">The returned values are those maintained in eye coordinates.</span></span> <span data-ttu-id="b7303-134">除非模型矩陣是在呼叫 **glLight** 時所識別，否則它們不會等於使用 [**glLight**](gllight-functions.md)所指定的值。</span><span class="sxs-lookup"><span data-stu-id="b7303-134">They will not be equal to the values specified using [**glLight**](gllight-functions.md), unless the modelview matrix was identified at the time **glLight** was called.</span></span><br/>                                                                                                                                                             |
| <span id="GL_SPOT_DIRECTION"></span><span id="gl_spot_direction"></span><dl> <span data-ttu-id="b7303-135"><dt>**GL \_ 點 \_ 方向**</dt></span><span class="sxs-lookup"><span data-stu-id="b7303-135"><dt>**GL\_SPOT\_DIRECTION**</dt></span></span> </dl>                      | <span data-ttu-id="b7303-136">*Params* 參數會傳回三個整數或浮點值，代表光線來源的方向。</span><span class="sxs-lookup"><span data-stu-id="b7303-136">The *params* parameter returns three integer or floating-point values representing the direction of the light source.</span></span> <span data-ttu-id="b7303-137">在要求時，整數值會藉由將內部浮點值四捨五入為最接近的整數值來計算。</span><span class="sxs-lookup"><span data-stu-id="b7303-137">Integer values, when requested, are computed by rounding the internal floating-point values to the nearest integer value.</span></span> <span data-ttu-id="b7303-138">傳回的值是以眼睛座標維持的值。</span><span class="sxs-lookup"><span data-stu-id="b7303-138">The returned values are those maintained in eye coordinates.</span></span> <span data-ttu-id="b7303-139">除非模型矩陣是在呼叫 **glLight** 時所識別，否則它們不會等於使用 **glLight** 所指定的值。</span><span class="sxs-lookup"><span data-stu-id="b7303-139">They will not be equal to the values specified using **glLight**, unless the modelview matrix was identified at the time **glLight** was called.</span></span> <span data-ttu-id="b7303-140">雖然在光源方向會在使用於光源方程式之前正規化，但傳回的值是正規化之前所指定值的轉換版本。</span><span class="sxs-lookup"><span data-stu-id="b7303-140">Although spot direction is normalized before being used in the lighting equation, the returned values are the transformed versions of the specified values prior to normalization.</span></span><br/> |
| <span id="GL_SPOT_EXPONENT"></span><span id="gl_spot_exponent"></span><dl> <span data-ttu-id="b7303-141"><dt>**GL \_ 點 \_ 指數**</dt></span><span class="sxs-lookup"><span data-stu-id="b7303-141"><dt>**GL\_SPOT\_EXPONENT**</dt></span></span> </dl>                         | <span data-ttu-id="b7303-142">*Params* 參數會傳回代表光線點指數的單一整數或浮點值。</span><span class="sxs-lookup"><span data-stu-id="b7303-142">The *params* parameter returns a single integer or floating-point value representing the spot exponent of the light.</span></span> <span data-ttu-id="b7303-143">當要求時，整數值會藉由將內部浮點表示四捨五入至最接近的整數來計算。</span><span class="sxs-lookup"><span data-stu-id="b7303-143">An integer value, when requested, is computed by rounding the internal floating-point representation to the nearest integer.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                |
| <span id="GL_SPOT_CUTOFF"></span><span id="gl_spot_cutoff"></span><dl> <span data-ttu-id="b7303-144"><dt>**GL \_ 點 \_ 截止**</dt></span><span class="sxs-lookup"><span data-stu-id="b7303-144"><dt>**GL\_SPOT\_CUTOFF**</dt></span></span> </dl>                               | <span data-ttu-id="b7303-145">*Params* 參數會傳回單一整數或浮點值，代表光線的點截止角度。</span><span class="sxs-lookup"><span data-stu-id="b7303-145">The *params* parameter returns a single integer or floating-point value representing the spot cutoff angle of the light.</span></span> <span data-ttu-id="b7303-146">當要求時，整數值會藉由將內部浮點表示四捨五入至最接近的整數來計算。</span><span class="sxs-lookup"><span data-stu-id="b7303-146">An integer value, when requested, is computed by rounding the internal floating-point representation to the nearest integer.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="GL_CONSTANT_ATTENUATION"></span><span id="gl_constant_attenuation"></span><dl> <span data-ttu-id="b7303-147"><dt>**GL \_ 常數 \_ 衰減**</dt></span><span class="sxs-lookup"><span data-stu-id="b7303-147"><dt>**GL\_CONSTANT\_ATTENUATION**</dt></span></span> </dl>    | <span data-ttu-id="b7303-148">*Params* 參數會傳回單一整數或浮點值，表示光源的常數 (非距離相關的) 衰減。</span><span class="sxs-lookup"><span data-stu-id="b7303-148">The *params* parameter returns a single integer or floating-point value representing the constant (not distance-related) attenuation of the light.</span></span> <span data-ttu-id="b7303-149">當要求時，整數值會藉由將內部浮點表示四捨五入至最接近的整數來計算。</span><span class="sxs-lookup"><span data-stu-id="b7303-149">An integer value, when requested, is computed by rounding the internal floating-point representation to the nearest integer.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                  |
| <span id="GL_LINEAR_ATTENUATION"></span><span id="gl_linear_attenuation"></span><dl> <span data-ttu-id="b7303-150"><dt>**GL \_ 線性 \_ 衰減**</dt></span><span class="sxs-lookup"><span data-stu-id="b7303-150"><dt>**GL\_LINEAR\_ATTENUATION**</dt></span></span> </dl>          | <span data-ttu-id="b7303-151">*Params* 參數會傳回單一整數或浮點值，代表光線的線性衰減。</span><span class="sxs-lookup"><span data-stu-id="b7303-151">The *params* parameter returns a single integer or floating-point value representing the linear attenuation of the light.</span></span> <span data-ttu-id="b7303-152">當要求時，整數值會藉由將內部浮點表示四捨五入至最接近的整數來計算。</span><span class="sxs-lookup"><span data-stu-id="b7303-152">An integer value, when requested, is computed by rounding the internal floating-point representation to the nearest integer.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="GL_QUADRATIC_ATTENUATION"></span><span id="gl_quadratic_attenuation"></span><dl> <span data-ttu-id="b7303-153"><dt>**GL \_ 二次 \_ 衰減**</dt></span><span class="sxs-lookup"><span data-stu-id="b7303-153"><dt>**GL\_QUADRATIC\_ATTENUATION**</dt></span></span> </dl> | <span data-ttu-id="b7303-154">*Params* 參數會傳回單一整數或浮點值，代表光線的二次衰減。</span><span class="sxs-lookup"><span data-stu-id="b7303-154">The *params* parameter returns a single integer or floating-point value representing the quadratic attenuation of the light.</span></span> <span data-ttu-id="b7303-155">當要求時，整數值會藉由將內部浮點表示四捨五入至最接近的整數來計算。</span><span class="sxs-lookup"><span data-stu-id="b7303-155">An integer value, when requested, is computed by rounding the internal floating-point representation to the nearest integer.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                        |



 

</dd> <dt>

<span data-ttu-id="b7303-156">*params*</span><span class="sxs-lookup"><span data-stu-id="b7303-156">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="b7303-157">傳回要求的資料。</span><span class="sxs-lookup"><span data-stu-id="b7303-157">Returns the requested data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7303-158">傳回值</span><span class="sxs-lookup"><span data-stu-id="b7303-158">Return value</span></span>

<span data-ttu-id="b7303-159">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="b7303-159">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b7303-160">備註</span><span class="sxs-lookup"><span data-stu-id="b7303-160">Remarks</span></span>

<span data-ttu-id="b7303-161">**GlGetLight** 函式會以 *參數* 值傳回 light 來源參數的值或值。</span><span class="sxs-lookup"><span data-stu-id="b7303-161">The **glGetLight** function returns in *params* the value or values of a light source parameter.</span></span> <span data-ttu-id="b7303-162">*Light* 參數會將燈光命名，而且是一種形式的符號名稱，也就是 gl light i 的符號名稱 \_ ，0 = *i* < gl \*\* \_ 最大光線 \_ ，其中 gl \_ 最大 \_ 光線是大於或等於八的實值相依常數。</span><span class="sxs-lookup"><span data-stu-id="b7303-162">The *light* parameter names the light and is a symbolic name of the form GL\_LIGHT *i* for 0 = *i* < GL\_MAX\_LIGHTS, where GL\_MAX\_LIGHTS is an implementation-dependent constant that is greater than or equal to eight.</span></span> <span data-ttu-id="b7303-163">*Pname* 參數會以符號名稱再次指定十個光源來源參數的其中一個。</span><span class="sxs-lookup"><span data-stu-id="b7303-163">The *pname* parameter specifies one of ten light source parameters, again by symbolic name.</span></span>

<span data-ttu-id="b7303-164">這一律是 GL \_ 燈 = gl \*\* \_ LIGHT0 + *i* 的情況。</span><span class="sxs-lookup"><span data-stu-id="b7303-164">It is always the case that GL\_LIGHT *i* = GL\_LIGHT0 + *i*.</span></span>

<span data-ttu-id="b7303-165">如果產生錯誤，則不會對 *參數* 的內容進行任何變更。</span><span class="sxs-lookup"><span data-stu-id="b7303-165">If an error is generated, no change is made to the contents of *params*.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7303-166">規格需求</span><span class="sxs-lookup"><span data-stu-id="b7303-166">Requirements</span></span>



| <span data-ttu-id="b7303-167">需求</span><span class="sxs-lookup"><span data-stu-id="b7303-167">Requirement</span></span> | <span data-ttu-id="b7303-168">值</span><span class="sxs-lookup"><span data-stu-id="b7303-168">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b7303-169">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b7303-169">Minimum supported client</span></span><br/> | <span data-ttu-id="b7303-170">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b7303-170">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="b7303-171">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b7303-171">Minimum supported server</span></span><br/> | <span data-ttu-id="b7303-172">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b7303-172">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b7303-173">標頭</span><span class="sxs-lookup"><span data-stu-id="b7303-173">Header</span></span><br/>                   | <dl> <span data-ttu-id="b7303-174"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="b7303-174"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="b7303-175">程式庫</span><span class="sxs-lookup"><span data-stu-id="b7303-175">Library</span></span><br/>                  | <dl> <span data-ttu-id="b7303-176"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="b7303-176"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="b7303-177">DLL</span><span class="sxs-lookup"><span data-stu-id="b7303-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b7303-178"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b7303-178"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7303-179">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b7303-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7303-180">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="b7303-180">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="b7303-181">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="b7303-181">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="b7303-182">**glLight**</span><span class="sxs-lookup"><span data-stu-id="b7303-182">**glLight**</span></span>](gllight-functions.md)
</dt> </dl>

 

 





