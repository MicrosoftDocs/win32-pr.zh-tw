---
title: 'glLighti 函式 (Gl) '
description: GlLighti 函數會傳回燈光來源參數值。
ms.assetid: 4fa5e604-d45d-412e-a08c-c38e0836596f
keywords:
- glLighti 函式 OpenGL
topic_type:
- apiref
api_name:
- glLighti
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52225c4db8eaa31c17d12a25590b918cf94b4c3b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843740"
---
# <a name="gllighti-function"></a><span data-ttu-id="10d3f-104">glLighti 函式</span><span class="sxs-lookup"><span data-stu-id="10d3f-104">glLighti function</span></span>

<span data-ttu-id="10d3f-105">**GlLighti** 函數會傳回燈光來源參數值。</span><span class="sxs-lookup"><span data-stu-id="10d3f-105">The **glLighti** function returns light source parameter values.</span></span>

## <a name="syntax"></a><span data-ttu-id="10d3f-106">語法</span><span class="sxs-lookup"><span data-stu-id="10d3f-106">Syntax</span></span>


```C++
void WINAPI glLighti(
   GLenum light,
   GLenum pname,
   GLint  param
);
```



## <a name="parameters"></a><span data-ttu-id="10d3f-107">參數</span><span class="sxs-lookup"><span data-stu-id="10d3f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10d3f-108">*light*</span><span class="sxs-lookup"><span data-stu-id="10d3f-108">*light*</span></span> 
</dt> <dd>

<span data-ttu-id="10d3f-109">光線的識別碼。</span><span class="sxs-lookup"><span data-stu-id="10d3f-109">The identifier of a light.</span></span> <span data-ttu-id="10d3f-110">可能的燈光數目取決於執行，但至少有8個燈支援。</span><span class="sxs-lookup"><span data-stu-id="10d3f-110">The number of possible lights depends on the implementation, but at least eight lights are supported.</span></span> <span data-ttu-id="10d3f-111">其識別方式是以 GL 燈的符號名稱 \_ 來 *識別，* 其中 *i* 是值：0到 GL \_ 最大 \_ 燈光-1。</span><span class="sxs-lookup"><span data-stu-id="10d3f-111">They are identified by symbolic names of the form GL\_LIGHT *i* where *i* is a value: 0 to GL\_MAX\_LIGHTS - 1.</span></span>

</dd> <dt>

<span data-ttu-id="10d3f-112">*pname*</span><span class="sxs-lookup"><span data-stu-id="10d3f-112">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="10d3f-113">*Light* 的單一值光源參數。</span><span class="sxs-lookup"><span data-stu-id="10d3f-113">A single-valued light source parameter for *light*.</span></span> <span data-ttu-id="10d3f-114">接受下列符號名稱。</span><span class="sxs-lookup"><span data-stu-id="10d3f-114">The following symbolic names are accepted.</span></span>



| <span data-ttu-id="10d3f-115">值</span><span class="sxs-lookup"><span data-stu-id="10d3f-115">Value</span></span>                                                                                                                                                                                                                                                                                                                                               | <span data-ttu-id="10d3f-116">意義</span><span class="sxs-lookup"><span data-stu-id="10d3f-116">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_SPOT_EXPONENT"></span><span id="gl_spot_exponent"></span><dl> <span data-ttu-id="10d3f-117"><dt>**GL \_ 點 \_ 指數**</dt></span><span class="sxs-lookup"><span data-stu-id="10d3f-117"><dt>**GL\_SPOT\_EXPONENT**</dt></span></span> </dl>                                                                                                                                                                             | <span data-ttu-id="10d3f-118">*Param* 參數是指定光線強度分佈的單一整數值。</span><span class="sxs-lookup"><span data-stu-id="10d3f-118">The *param* parameter is a single integer value that specifies the intensity distribution of the light.</span></span> <span data-ttu-id="10d3f-119">整數和浮點值會直接對應。</span><span class="sxs-lookup"><span data-stu-id="10d3f-119">Integer and floating-point values are mapped directly.</span></span> <span data-ttu-id="10d3f-120">只 \[ 接受範圍0，128中的值 \] 。</span><span class="sxs-lookup"><span data-stu-id="10d3f-120">Only values in the range \[0, 128\] are accepted.</span></span> <br/> <span data-ttu-id="10d3f-121">有效光線濃度的衰減方式是將光源的方向和光線方向之間的角度，以及光線之間的方向，提升為點指數的乘冪。</span><span class="sxs-lookup"><span data-stu-id="10d3f-121">Effective light intensity is attenuated by the cosine of the angle between the direction of the light and the direction from the light to the vertex being lighted, raised to the power of the spot exponent.</span></span> <span data-ttu-id="10d3f-122">因此，較高的點指數會產生更專注的燈光來源，不論是否有點截止角度。</span><span class="sxs-lookup"><span data-stu-id="10d3f-122">Thus, higher spot exponents result in a more focused light source, regardless of the spot cutoff angle.</span></span> <span data-ttu-id="10d3f-123">預設的點指數是0，會產生統一的光線分佈。</span><span class="sxs-lookup"><span data-stu-id="10d3f-123">The default spot exponent is 0, resulting in uniform light distribution.</span></span><br/> |
| <span id="GL_SPOT_CUTOFF"></span><span id="gl_spot_cutoff"></span><dl> <span data-ttu-id="10d3f-124"><dt>**GL \_ 點 \_ 截止**</dt></span><span class="sxs-lookup"><span data-stu-id="10d3f-124"><dt>**GL\_SPOT\_CUTOFF**</dt></span></span> </dl>                                                                                                                                                                                   | <span data-ttu-id="10d3f-125">*Param* 參數是單一整數值，可指定光線來源的最大散佈角度。</span><span class="sxs-lookup"><span data-stu-id="10d3f-125">The *param* parameter is a single integer value that specifies the maximum spread angle of a light source.</span></span> <span data-ttu-id="10d3f-126">整數和浮點值會直接對應。</span><span class="sxs-lookup"><span data-stu-id="10d3f-126">Integer and floating-point values are mapped directly.</span></span> <span data-ttu-id="10d3f-127">只 \[ 接受範圍0、90 \] 和特殊值180中的值。</span><span class="sxs-lookup"><span data-stu-id="10d3f-127">Only values in the range \[0, 90\], and the special value 180, are accepted.</span></span> <br/> <span data-ttu-id="10d3f-128">如果光源方向與光源方向之間的角度大於光源的方向，則光線會以完全遮罩的方向來表示。</span><span class="sxs-lookup"><span data-stu-id="10d3f-128">If the angle between the direction of the light and the direction from the light to the vertex being lighted is greater than the spot cutoff angle, then the light is completely masked.</span></span> <span data-ttu-id="10d3f-129">否則，其強度是由點指數和衰減因數所控制。</span><span class="sxs-lookup"><span data-stu-id="10d3f-129">Otherwise, its intensity is controlled by the spot exponent and the attenuation factors.</span></span> <span data-ttu-id="10d3f-130">預設的點截止是180，因此會產生一致的光線分佈。</span><span class="sxs-lookup"><span data-stu-id="10d3f-130">The default spot cutoff is 180, resulting in uniform light distribution.</span></span><br/>       |
| <span id="GL_CONSTANT_ATTENUATION__GL_LINEAR_ATTENUATION__GL_QUADRATIC_ATTENUATION"></span><span id="gl_constant_attenuation__gl_linear_attenuation__gl_quadratic_attenuation"></span><dl> <span data-ttu-id="10d3f-131"><dt>**GL \_ 固定 \_ 衰減、GL \_ 線性 \_ 衰減、GL \_ 二次 \_ 衰減**</dt></span><span class="sxs-lookup"><span data-stu-id="10d3f-131"><dt>**GL\_CONSTANT\_ATTENUATION, GL\_LINEAR\_ATTENUATION, GL\_QUADRATIC\_ATTENUATION**</dt></span></span> </dl> | <span data-ttu-id="10d3f-132">*Param* 參數是單一整數值，可指定三個光線衰減因數之一。</span><span class="sxs-lookup"><span data-stu-id="10d3f-132">The *param* parameter is a single integer value that specifies one of the three light attenuation factors.</span></span> <span data-ttu-id="10d3f-133">整數和浮點值會直接對應。</span><span class="sxs-lookup"><span data-stu-id="10d3f-133">Integer and floating-point values are mapped directly.</span></span> <span data-ttu-id="10d3f-134">只接受非負數值。</span><span class="sxs-lookup"><span data-stu-id="10d3f-134">Only nonnegative values are accepted.</span></span> <br/> <span data-ttu-id="10d3f-135">如果燈光是位置，而不是方向，則其濃度會衰減：常數因數的倒數、線性因數乘以光線和頂點之間的距離，以及乘以相同距離的平方。」的濃度。</span><span class="sxs-lookup"><span data-stu-id="10d3f-135">If the light is positional, rather than directional, its intensity is attenuated by the reciprocal of the sum of: the constant factor, the linear factor multiplied by the distance between the light and the vertex being lighted, and the quadratic factor multiplied by the square of the same distance.</span></span> <span data-ttu-id="10d3f-136">預設衰減因素是 (1，0，0) ，因此不會產生衰減。</span><span class="sxs-lookup"><span data-stu-id="10d3f-136">The default attenuation factors are (1,0,0), resulting in no attenuation.</span></span><br/>                   |



 

</dd> <dt>

<span data-ttu-id="10d3f-137">*param*</span><span class="sxs-lookup"><span data-stu-id="10d3f-137">*param*</span></span> 
</dt> <dd>

<span data-ttu-id="10d3f-138">指定要將光源 *光源* 的參數 *pname* 設定為的值。</span><span class="sxs-lookup"><span data-stu-id="10d3f-138">Specifies the value that parameter *pname* of light source *light* will be set to.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10d3f-139">傳回值</span><span class="sxs-lookup"><span data-stu-id="10d3f-139">Return value</span></span>

<span data-ttu-id="10d3f-140">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="10d3f-140">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="10d3f-141">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="10d3f-141">Error codes</span></span>

<span data-ttu-id="10d3f-142">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="10d3f-142">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="10d3f-143">Name</span><span class="sxs-lookup"><span data-stu-id="10d3f-143">Name</span></span>                                                                                                  | <span data-ttu-id="10d3f-144">意義</span><span class="sxs-lookup"><span data-stu-id="10d3f-144">Meaning</span></span>                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="10d3f-145"><dt>**GL \_ 無效 \_ 列舉**</dt></span><span class="sxs-lookup"><span data-stu-id="10d3f-145"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="10d3f-146">*light* 或 *pname* 不是可接受的值。</span><span class="sxs-lookup"><span data-stu-id="10d3f-146">*light* or *pname* was not an accepted value.</span></span><br/>                                                                                                                                                                  |
| <dl> <span data-ttu-id="10d3f-147"><dt>**GL \_ 無效 \_ 值**</dt></span><span class="sxs-lookup"><span data-stu-id="10d3f-147"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="10d3f-148">指定的點指數值超出範圍0、 \[ 128 \] 或點截止值的範圍 \[ 0、90 (， \] 但特殊值 180) 或指定的負面衰減因數除外。</span><span class="sxs-lookup"><span data-stu-id="10d3f-148">A spot exponent value was specified outside the range \[0, 128\], or spot cutoff was specified outside the range \[0, 90\] (except for the special value 180), or a negative attenuation factor was specified.</span></span><br/> |
| <dl> <span data-ttu-id="10d3f-149"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="10d3f-149"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="10d3f-150">呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。</span><span class="sxs-lookup"><span data-stu-id="10d3f-150">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/>                                                                                     |



## <a name="remarks"></a><span data-ttu-id="10d3f-151">備註</span><span class="sxs-lookup"><span data-stu-id="10d3f-151">Remarks</span></span>

<span data-ttu-id="10d3f-152">**GlLighti** 函數會設定個別光源參數的值或值。</span><span class="sxs-lookup"><span data-stu-id="10d3f-152">The **glLighti** function sets the value or values of individual light source parameters.</span></span> <span data-ttu-id="10d3f-153">*Light* 參數會將燈光命名，而且是一個外型燈的符號名稱 \_ ，其中 0 = *i* < GL 的 \_ 最大 \_ 燈光。</span><span class="sxs-lookup"><span data-stu-id="10d3f-153">The *light* parameter names the light and is a symbolic name of the form GL\_LIGHT *i*, where 0 = *i* < GL\_MAX\_LIGHTS.</span></span>

<span data-ttu-id="10d3f-154">*Pname* 參數會以符號名稱再次指定其中一個燈光來源參數。</span><span class="sxs-lookup"><span data-stu-id="10d3f-154">The *pname* parameter specifies one of the light source parameters, again by symbolic name.</span></span> <span data-ttu-id="10d3f-155">*Param* 參數為單一值或陣列的指標，其中包含新的值。</span><span class="sxs-lookup"><span data-stu-id="10d3f-155">The *param* parameter is either a single value or a pointer to an array that contains the new values.</span></span>

<span data-ttu-id="10d3f-156">您可以使用 [**glEnable**](glenable.md) 和 [**glDisable**](gldisable.md) 搭配引數 GL 光源來啟用和停用光源計算 \_ 。</span><span class="sxs-lookup"><span data-stu-id="10d3f-156">Lighting calculation is enabled and disabled using [**glEnable**](glenable.md) and [**glDisable**](gldisable.md) with argument GL\_LIGHTING.</span></span> <span data-ttu-id="10d3f-157">當光源啟用時，已啟用的燈光來源會對光源計算造成影響。</span><span class="sxs-lookup"><span data-stu-id="10d3f-157">When lighting is enabled, light sources that are enabled contribute to the lighting calculation.</span></span> <span data-ttu-id="10d3f-158">您可以使用 **glEnable** 和 **glDisable** 搭配引數 GL 燈來啟用和停用燈光來源 *i* \_ 。\*\*</span><span class="sxs-lookup"><span data-stu-id="10d3f-158">Light source *i* is enabled and disabled using **glEnable** and **glDisable** with argument GL\_LIGHT *i*.</span></span>

<span data-ttu-id="10d3f-159">這一律是 GL \_ 燈 = gl \*\* \_ LIGHT0 + *i* 的情況。</span><span class="sxs-lookup"><span data-stu-id="10d3f-159">It is always the case that GL\_LIGHT *i* = GL\_LIGHT0 + *i*.</span></span>

<span data-ttu-id="10d3f-160">下列函式會取出與 **glLighti** 函數相關的資訊：</span><span class="sxs-lookup"><span data-stu-id="10d3f-160">The following functions retrieve information related to the **glLighti** function:</span></span>

[<span data-ttu-id="10d3f-161">**glGetLight**</span><span class="sxs-lookup"><span data-stu-id="10d3f-161">**glGetLight**</span></span>](glgetlight.md)

<span data-ttu-id="10d3f-162">[](glisenabled.md)具有引數 GL \_ 光源的 glIsEnabled</span><span class="sxs-lookup"><span data-stu-id="10d3f-162">[**glIsEnabled**](glisenabled.md) with argument GL\_LIGHTING</span></span>

## <a name="requirements"></a><span data-ttu-id="10d3f-163">規格需求</span><span class="sxs-lookup"><span data-stu-id="10d3f-163">Requirements</span></span>



| <span data-ttu-id="10d3f-164">需求</span><span class="sxs-lookup"><span data-stu-id="10d3f-164">Requirement</span></span> | <span data-ttu-id="10d3f-165">值</span><span class="sxs-lookup"><span data-stu-id="10d3f-165">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="10d3f-166">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="10d3f-166">Minimum supported client</span></span><br/> | <span data-ttu-id="10d3f-167">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="10d3f-167">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="10d3f-168">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="10d3f-168">Minimum supported server</span></span><br/> | <span data-ttu-id="10d3f-169">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="10d3f-169">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="10d3f-170">標頭</span><span class="sxs-lookup"><span data-stu-id="10d3f-170">Header</span></span><br/>                   | <dl> <span data-ttu-id="10d3f-171"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="10d3f-171"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="10d3f-172">程式庫</span><span class="sxs-lookup"><span data-stu-id="10d3f-172">Library</span></span><br/>                  | <dl> <span data-ttu-id="10d3f-173"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="10d3f-173"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="10d3f-174">DLL</span><span class="sxs-lookup"><span data-stu-id="10d3f-174">DLL</span></span><br/>                      | <dl> <span data-ttu-id="10d3f-175"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="10d3f-175"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10d3f-176">另請參閱</span><span class="sxs-lookup"><span data-stu-id="10d3f-176">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10d3f-177">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="10d3f-177">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="10d3f-178">**glColorMaterial**</span><span class="sxs-lookup"><span data-stu-id="10d3f-178">**glColorMaterial**</span></span>](glcolormaterial.md)
</dt> <dt>

[<span data-ttu-id="10d3f-179">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="10d3f-179">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="10d3f-180">**glLightModel**</span><span class="sxs-lookup"><span data-stu-id="10d3f-180">**glLightModel**</span></span>](gllightmodel-functions.md)
</dt> <dt>

[<span data-ttu-id="10d3f-181">**glMaterial**</span><span class="sxs-lookup"><span data-stu-id="10d3f-181">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> </dl>

 

 





