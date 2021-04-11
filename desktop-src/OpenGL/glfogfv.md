---
title: 'glFogfv 函式 (Gl) '
description: 'GlFogfv 函數會指定霧化參數。 |glFogfv 函式 (Gl) '
ms.assetid: a2243ff4-4f3a-4b8c-b4fb-ce2cd74815e4
keywords:
- glFogfv 函式 OpenGL
topic_type:
- apiref
api_name:
- glFogfv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b407dd9b9c984a744e903a2c269d21028d32977a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104196136"
---
# <a name="glfogfv-function"></a><span data-ttu-id="c60ea-105">glFogfv 函式</span><span class="sxs-lookup"><span data-stu-id="c60ea-105">glFogfv function</span></span>

<span data-ttu-id="c60ea-106">**GlFogfv** 函數會指定霧化參數。</span><span class="sxs-lookup"><span data-stu-id="c60ea-106">The **glFogfv** function specifies fog parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="c60ea-107">語法</span><span class="sxs-lookup"><span data-stu-id="c60ea-107">Syntax</span></span>


```C++
void WINAPI glFogfv(
         GLenum  pname,
   const GLfloat *params
);
```



## <a name="parameters"></a><span data-ttu-id="c60ea-108">參數</span><span class="sxs-lookup"><span data-stu-id="c60ea-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c60ea-109">*pname*</span><span class="sxs-lookup"><span data-stu-id="c60ea-109">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="c60ea-110">指定霧化參數。</span><span class="sxs-lookup"><span data-stu-id="c60ea-110">Specifies a fog parameter.</span></span>

<span data-ttu-id="c60ea-111">接受下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="c60ea-111">Accepts one of the following values.</span></span>



| <span data-ttu-id="c60ea-112">值</span><span class="sxs-lookup"><span data-stu-id="c60ea-112">Value</span></span>                                                                                                                                                             | <span data-ttu-id="c60ea-113">意義</span><span class="sxs-lookup"><span data-stu-id="c60ea-113">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_FOG_MODE"></span><span id="gl_fog_mode"></span><dl> <span data-ttu-id="c60ea-114"><dt>**GL \_ 霧化 \_ 模式**</dt></span><span class="sxs-lookup"><span data-stu-id="c60ea-114"><dt>**GL\_FOG\_MODE**</dt></span></span> </dl>          | <span data-ttu-id="c60ea-115">*Params* 參數是浮點值，可指定用來計算霧化 blend 因數 *f* 的方程式。</span><span class="sxs-lookup"><span data-stu-id="c60ea-115">The *params* parameter is a floating-point value that specifies the equation to be used to compute the fog blend factor, *f*.</span></span> <span data-ttu-id="c60ea-116">接受三個符號常數： GL \_ 線性、gl \_ EXP 和 GL \_ EXP2。</span><span class="sxs-lookup"><span data-stu-id="c60ea-116">Three symbolic constants are accepted: GL\_LINEAR, GL\_EXP, and GL\_EXP2.</span></span> <span data-ttu-id="c60ea-117">對應到這些符號常數的方會定義于下列備註區段中。</span><span class="sxs-lookup"><span data-stu-id="c60ea-117">The equations corresponding to these symbolic constants are defined in the following Remarks section.</span></span> <span data-ttu-id="c60ea-118">預設的霧化模式為 GL \_ EXP。</span><span class="sxs-lookup"><span data-stu-id="c60ea-118">The default fog mode is GL\_EXP.</span></span><br/>                                                                           |
| <span id="GL_FOG_DENSITY"></span><span id="gl_fog_density"></span><dl> <span data-ttu-id="c60ea-119"><dt>**GL \_ 霧化 \_ 密度**</dt></span><span class="sxs-lookup"><span data-stu-id="c60ea-119"><dt>**GL\_FOG\_DENSITY**</dt></span></span> </dl> | <span data-ttu-id="c60ea-120">*Params* 參數是浮點值，可指定 *密度*、兩個指數霧化方程式中所使用的霧化密度。</span><span class="sxs-lookup"><span data-stu-id="c60ea-120">The *params* parameter is a floating-point value that specifies *density*, the fog density used in both exponential fog equations.</span></span> <span data-ttu-id="c60ea-121">只接受非負的密度。</span><span class="sxs-lookup"><span data-stu-id="c60ea-121">Only nonnegative densities are accepted.</span></span> <span data-ttu-id="c60ea-122">預設的霧化密度為1.0。</span><span class="sxs-lookup"><span data-stu-id="c60ea-122">The default fog density is 1.0.</span></span><br/>                                                                                                                                                                                                              |
| <span id="GL_FOG_START"></span><span id="gl_fog_start"></span><dl> <span data-ttu-id="c60ea-123"><dt>**GL \_ 霧化 \_ 開始**</dt></span><span class="sxs-lookup"><span data-stu-id="c60ea-123"><dt>**GL\_FOG\_START**</dt></span></span> </dl>       | <span data-ttu-id="c60ea-124">*Params* 參數是浮點值，可指定線性霧化方程式中所使用的 *開始* 和近距離。</span><span class="sxs-lookup"><span data-stu-id="c60ea-124">The *params* parameter is a floating-point value that specifies *start*, the near distance used in the linear fog equation.</span></span> <span data-ttu-id="c60ea-125">預設接近距離為0.0。</span><span class="sxs-lookup"><span data-stu-id="c60ea-125">The default near distance is 0.0.</span></span><br/>                                                                                                                                                                                                                                                            |
| <span id="GL_FOG_END"></span><span id="gl_fog_end"></span><dl> <span data-ttu-id="c60ea-126"><dt>**GL \_ 霧化 \_ 結束**</dt></span><span class="sxs-lookup"><span data-stu-id="c60ea-126"><dt>**GL\_FOG\_END**</dt></span></span> </dl>             | <span data-ttu-id="c60ea-127">*Params* 參數是浮點值，可指定線性霧化方程式中所使用的 *結束* 距離。</span><span class="sxs-lookup"><span data-stu-id="c60ea-127">The *params* parameter is a floating-point value that specifies *end*, the far distance used in the linear fog equation.</span></span> <span data-ttu-id="c60ea-128">預設距離為1.0。</span><span class="sxs-lookup"><span data-stu-id="c60ea-128">The default far distance is 1.0.</span></span><br/>                                                                                                                                                                                                                                                                |
| <span id="GL_FOG_INDEX"></span><span id="gl_fog_index"></span><dl> <span data-ttu-id="c60ea-129"><dt>**GL \_ 霧化 \_ 索引**</dt></span><span class="sxs-lookup"><span data-stu-id="c60ea-129"><dt>**GL\_FOG\_INDEX**</dt></span></span> </dl>       | <span data-ttu-id="c60ea-130">*Params* 參數是指定 *i*<sub>f</sub>的浮點數值（霧化色彩索引）。</span><span class="sxs-lookup"><span data-stu-id="c60ea-130">The *params* parameter is a floating-point value that specifies *i*<sub>f</sub> , the fog color index.</span></span> <span data-ttu-id="c60ea-131">預設的霧化索引為0.0。</span><span class="sxs-lookup"><span data-stu-id="c60ea-131">The default fog index is 0.0.</span></span><br/>                                                                                                                                                                                                                                                                                     |
| <span id="GL_FOG_COLOR"></span><span id="gl_fog_color"></span><dl> <span data-ttu-id="c60ea-132"><dt>**GL \_ 霧化 \_ 色彩**</dt></span><span class="sxs-lookup"><span data-stu-id="c60ea-132"><dt>**GL\_FOG\_COLOR**</dt></span></span> </dl>       | <span data-ttu-id="c60ea-133">*Params* 參數包含四個浮點值，可指定 *C*<sub>f</sub> （霧化色彩）。</span><span class="sxs-lookup"><span data-stu-id="c60ea-133">The *params* parameter contains four floating-point values that specify *C*<sub>f</sub> , the fog color.</span></span> <span data-ttu-id="c60ea-134">整數值會以線性方式對應，因此最正面的可表示值會對應至1.0，而最大的可表示值會對應至-1.0。</span><span class="sxs-lookup"><span data-stu-id="c60ea-134">Integer values are mapped linearly such that the most positive representable value maps to 1.0, and the most negative representable value maps to -1.0.</span></span> <span data-ttu-id="c60ea-135">浮點值會直接對應。</span><span class="sxs-lookup"><span data-stu-id="c60ea-135">Floating-point values are mapped directly.</span></span> <span data-ttu-id="c60ea-136">轉換之後，會將所有色彩元件壓制至範圍 \[ 0、1 \] 。</span><span class="sxs-lookup"><span data-stu-id="c60ea-136">After conversion, all color components are clamped to the range \[0,1\].</span></span> <span data-ttu-id="c60ea-137">預設的霧化色彩是 (0、0、0、0) 。</span><span class="sxs-lookup"><span data-stu-id="c60ea-137">The default fog color is (0,0,0,0).</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="c60ea-138">*params*</span><span class="sxs-lookup"><span data-stu-id="c60ea-138">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="c60ea-139">指定要指派給 *pname* 的值。</span><span class="sxs-lookup"><span data-stu-id="c60ea-139">Specifies the value or values to be assigned to *pname*.</span></span> <span data-ttu-id="c60ea-140">GL \_ 霧化 \_ 色彩需要四個值的陣列。</span><span class="sxs-lookup"><span data-stu-id="c60ea-140">GL\_FOG\_COLOR requires an array of four values.</span></span> <span data-ttu-id="c60ea-141">所有其他參數都接受僅包含單一值的陣列。</span><span class="sxs-lookup"><span data-stu-id="c60ea-141">All other parameters accept an array containing only a single value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c60ea-142">傳回值</span><span class="sxs-lookup"><span data-stu-id="c60ea-142">Return value</span></span>

<span data-ttu-id="c60ea-143">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="c60ea-143">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c60ea-144">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="c60ea-144">Error codes</span></span>

<span data-ttu-id="c60ea-145">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="c60ea-145">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="c60ea-146">Name</span><span class="sxs-lookup"><span data-stu-id="c60ea-146">Name</span></span>                                                                                                  | <span data-ttu-id="c60ea-147">意義</span><span class="sxs-lookup"><span data-stu-id="c60ea-147">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c60ea-148"><dt>**GL \_ 無效 \_ 列舉**</dt></span><span class="sxs-lookup"><span data-stu-id="c60ea-148"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="c60ea-149">*pname* 不是可接受的值。</span><span class="sxs-lookup"><span data-stu-id="c60ea-149">*pname* was not an accepted value.</span></span><br/>                                                                                         |
| <dl> <span data-ttu-id="c60ea-150"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="c60ea-150"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="c60ea-151">呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。</span><span class="sxs-lookup"><span data-stu-id="c60ea-151">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="c60ea-152">備註</span><span class="sxs-lookup"><span data-stu-id="c60ea-152">Remarks</span></span>

<span data-ttu-id="c60ea-153">您可以使用引數 GL 霧化來啟用和停用 [**glEnable**](glenable.md) 和 [**glDisable**](gldisable.md)的霧化 \_ 。</span><span class="sxs-lookup"><span data-stu-id="c60ea-153">You enable and disable fog with [**glEnable**](glenable.md) and [**glDisable**](gldisable.md), using the argument GL\_FOG.</span></span> <span data-ttu-id="c60ea-154">啟用時，霧化會影響點陣化幾何、點陣圖和圖元區塊，但不會影響緩衝區清除作業。</span><span class="sxs-lookup"><span data-stu-id="c60ea-154">While enabled, fog affects rasterized geometry, bitmaps, and pixel blocks, but not buffer-clear operations.</span></span>

<span data-ttu-id="c60ea-155">**GlFogfv** 函式會將 *params* 中的值或值指派給 *pname* 所指定的霧化參數。</span><span class="sxs-lookup"><span data-stu-id="c60ea-155">The **glFogfv** function assigns the value or values in *params* to the fog parameter specified by *pname*.</span></span>

<span data-ttu-id="c60ea-156">霧化會使用混色因數 *f* 來混合霧化色彩與每個柵格化圖元片段的 posttexturing 色彩。</span><span class="sxs-lookup"><span data-stu-id="c60ea-156">Fog blends a fog color with each rasterized pixel fragment's posttexturing color using a blending factor *f*.</span></span> <span data-ttu-id="c60ea-157">第三種方式是以三種方式的其中一種來計算，視霧化 *模式而定* 。</span><span class="sxs-lookup"><span data-stu-id="c60ea-157">Factor *f* is computed in one of three ways, depending on the fog mode.</span></span> <span data-ttu-id="c60ea-158">讓 *z* 成為從原點到所 fogged 之片段的眼睛距離。</span><span class="sxs-lookup"><span data-stu-id="c60ea-158">Let *z* be the distance in eye coordinates from the origin to the fragment being fogged.</span></span> <span data-ttu-id="c60ea-159">GL \_ 線性模糊的方程式如下：</span><span class="sxs-lookup"><span data-stu-id="c60ea-159">The equation for GL\_LINEAR fog is:</span></span>

![顯示 GL_LINEAR 霧化值的方程式。](images/fog01.png)

<span data-ttu-id="c60ea-161">GL \_ EXP 霧化的方程式如下：</span><span class="sxs-lookup"><span data-stu-id="c60ea-161">The equation for GL\_EXP fog is:</span></span>

![顯示 GL_EXP 霧化模式中混合因數值的方程式。](images/fog02.png)

<span data-ttu-id="c60ea-163">GL \_ EXP2 霧化的方程式是：</span><span class="sxs-lookup"><span data-stu-id="c60ea-163">The equation for GL\_EXP2 fog is:</span></span>

![顯示 GL_EXP2 霧化模式中混合因數值的方程式。](images/fog03.png)

<span data-ttu-id="c60ea-165">不論霧化模式為何， *f* 都是在計算後壓制至範圍 \[ 0、1 \] 。</span><span class="sxs-lookup"><span data-stu-id="c60ea-165">Regardless of the fog mode, *f* is clamped to the range \[0,1\] after it is computed.</span></span> <span data-ttu-id="c60ea-166">然後，如果 OpenGL 處於 RGBA 色彩模式，則會將片段的色彩 *C*<sub>r</sub> 取代為</span><span class="sxs-lookup"><span data-stu-id="c60ea-166">Then, if OpenGL is in RGBA color mode, the fragment's color *C*<sub>r</sub> is replaced by</span></span>

![顯示 fogged 片段色彩的方程式，做為混色因數和霧化色彩的函式。](images/fog04.png)

<span data-ttu-id="c60ea-168">在色彩索引模式中，片段的色彩索引 *i*<sub>r</sub> 會取代為</span><span class="sxs-lookup"><span data-stu-id="c60ea-168">In color-index mode, the fragment's color index *i*<sub>r</sub> is replaced by</span></span>

![顯示 fogged 片段之色彩索引的方程式，做為混合因數和索引色彩的函式。](images/fog05.png)

<span data-ttu-id="c60ea-170">下列函式會取出與 **glFog** 函數相關的資訊：</span><span class="sxs-lookup"><span data-stu-id="c60ea-170">The following functions retrieve information related to the **glFog** functions:</span></span>

<span data-ttu-id="c60ea-171">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 霧化 \_ 色彩的 glGet</span><span class="sxs-lookup"><span data-stu-id="c60ea-171">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_FOG\_COLOR</span></span>

<span data-ttu-id="c60ea-172">具有引數 GL \_ 霧化 \_ 索引的 glGet</span><span class="sxs-lookup"><span data-stu-id="c60ea-172">**glGet** with argument GL\_FOG\_INDEX</span></span>

<span data-ttu-id="c60ea-173">具有引數 GL \_ 霧化 \_ 密度的 glGet</span><span class="sxs-lookup"><span data-stu-id="c60ea-173">**glGet** with argument GL\_FOG\_DENSITY</span></span>

<span data-ttu-id="c60ea-174">具有引數 GL \_ 霧化 \_ 開始的 glGet</span><span class="sxs-lookup"><span data-stu-id="c60ea-174">**glGet** with argument GL\_FOG\_START</span></span>

<span data-ttu-id="c60ea-175">具有引數 GL \_ 霧化 \_ END 的 glGet</span><span class="sxs-lookup"><span data-stu-id="c60ea-175">**glGet** with argument GL\_FOG\_END</span></span>

<span data-ttu-id="c60ea-176">具有引數 GL \_ 霧化 \_ 模式的 glGet</span><span class="sxs-lookup"><span data-stu-id="c60ea-176">**glGet** with argument GL\_FOG\_MODE</span></span>

<span data-ttu-id="c60ea-177">[](glisenabled.md)具有引數 GL \_ 霧化的 glIsEnabled</span><span class="sxs-lookup"><span data-stu-id="c60ea-177">[**glIsEnabled**](glisenabled.md) with argument GL\_FOG</span></span>

## <a name="requirements"></a><span data-ttu-id="c60ea-178">規格需求</span><span class="sxs-lookup"><span data-stu-id="c60ea-178">Requirements</span></span>



| <span data-ttu-id="c60ea-179">需求</span><span class="sxs-lookup"><span data-stu-id="c60ea-179">Requirement</span></span> | <span data-ttu-id="c60ea-180">值</span><span class="sxs-lookup"><span data-stu-id="c60ea-180">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c60ea-181">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c60ea-181">Minimum supported client</span></span><br/> | <span data-ttu-id="c60ea-182">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c60ea-182">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="c60ea-183">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c60ea-183">Minimum supported server</span></span><br/> | <span data-ttu-id="c60ea-184">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c60ea-184">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c60ea-185">標頭</span><span class="sxs-lookup"><span data-stu-id="c60ea-185">Header</span></span><br/>                   | <dl> <span data-ttu-id="c60ea-186"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="c60ea-186"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="c60ea-187">程式庫</span><span class="sxs-lookup"><span data-stu-id="c60ea-187">Library</span></span><br/>                  | <dl> <span data-ttu-id="c60ea-188"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="c60ea-188"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="c60ea-189">DLL</span><span class="sxs-lookup"><span data-stu-id="c60ea-189">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c60ea-190"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c60ea-190"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c60ea-191">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c60ea-191">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c60ea-192">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="c60ea-192">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="c60ea-193">**glDisable**</span><span class="sxs-lookup"><span data-stu-id="c60ea-193">**glDisable**</span></span>](gldisable.md)
</dt> <dt>

[<span data-ttu-id="c60ea-194">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="c60ea-194">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="c60ea-195">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="c60ea-195">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="c60ea-196">**glGet**</span><span class="sxs-lookup"><span data-stu-id="c60ea-196">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="c60ea-197">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="c60ea-197">**glIsEnabled**</span></span>](glisenabled.md)
</dt> </dl>

 

 





