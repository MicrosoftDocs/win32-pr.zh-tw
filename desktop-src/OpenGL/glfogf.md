---
title: 'glFogf 函式 (Gl) '
description: GlFogf 和函數會指定霧化參數。
ms.assetid: 69961d8f-385c-4353-aef3-38fb654c44f8
keywords:
- glFogf 函式 OpenGL
topic_type:
- apiref
api_name:
- glFogf
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfe0509b30e91797752604110068701fcedaa266
ms.sourcegitcommit: 7ef31bf778e76ce4196205d4c4c632fbdc649805
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/05/2021
ms.locfileid: "104027615"
---
# <a name="glfogf-function"></a><span data-ttu-id="d7793-104">glFogf 函式</span><span class="sxs-lookup"><span data-stu-id="d7793-104">glFogf function</span></span>

<span data-ttu-id="d7793-105">**GlFogf** 和函數會指定霧化參數。</span><span class="sxs-lookup"><span data-stu-id="d7793-105">The **glFogf** and function specifies fog parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7793-106">語法</span><span class="sxs-lookup"><span data-stu-id="d7793-106">Syntax</span></span>


```C++
void WINAPI glFogf(
   GLenum  pname,
   GLfloat param
);
```



## <a name="parameters"></a><span data-ttu-id="d7793-107">參數</span><span class="sxs-lookup"><span data-stu-id="d7793-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7793-108">*pname*</span><span class="sxs-lookup"><span data-stu-id="d7793-108">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="d7793-109">指定單一值的霧化參數。</span><span class="sxs-lookup"><span data-stu-id="d7793-109">Specifies a single-valued fog parameter.</span></span>

<span data-ttu-id="d7793-110">接受下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="d7793-110">Accepts one of the following values.</span></span>



| <span data-ttu-id="d7793-111">值</span><span class="sxs-lookup"><span data-stu-id="d7793-111">Value</span></span>                                                                                                                                                             | <span data-ttu-id="d7793-112">意義</span><span class="sxs-lookup"><span data-stu-id="d7793-112">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_FOG_MODE"></span><span id="gl_fog_mode"></span><dl> <span data-ttu-id="d7793-113"><dt>**GL \_ 霧化 \_ 模式**</dt></span><span class="sxs-lookup"><span data-stu-id="d7793-113"><dt>**GL\_FOG\_MODE**</dt></span></span> </dl>          | <span data-ttu-id="d7793-114">*Params* 參數是單一浮點值，可指定用來計算霧化 blend 因數 *f* 的方程式。</span><span class="sxs-lookup"><span data-stu-id="d7793-114">The *params* parameter is a single floating-point value that specifies the equation to be used to compute the fog blend factor, *f*.</span></span> <span data-ttu-id="d7793-115">接受三個符號常數： GL \_ 線性、gl \_ EXP 和 GL \_ EXP2。</span><span class="sxs-lookup"><span data-stu-id="d7793-115">Three symbolic constants are accepted: GL\_LINEAR, GL\_EXP, and GL\_EXP2.</span></span> <span data-ttu-id="d7793-116">對應到這些符號常數的方會定義于下列備註區段中。</span><span class="sxs-lookup"><span data-stu-id="d7793-116">The equations corresponding to these symbolic constants are defined in the following Remarks section.</span></span> <span data-ttu-id="d7793-117">預設的霧化模式為 GL \_ EXP。</span><span class="sxs-lookup"><span data-stu-id="d7793-117">The default fog mode is GL\_EXP.</span></span><br/> |
| <span id="GL_FOG_DENSITY"></span><span id="gl_fog_density"></span><dl> <span data-ttu-id="d7793-118"><dt>**GL \_ 霧化 \_ 密度**</dt></span><span class="sxs-lookup"><span data-stu-id="d7793-118"><dt>**GL\_FOG\_DENSITY**</dt></span></span> </dl> | <span data-ttu-id="d7793-119">*Params* 參數是單一浮點值，可指定 *密度*、兩個指數霧化方程式中所使用的霧化密度。</span><span class="sxs-lookup"><span data-stu-id="d7793-119">The *params* parameter is a single floating-point value that specifies *density*, the fog density used in both exponential fog equations.</span></span> <span data-ttu-id="d7793-120">只接受非負的密度。</span><span class="sxs-lookup"><span data-stu-id="d7793-120">Only nonnegative densities are accepted.</span></span> <span data-ttu-id="d7793-121">預設的霧化密度為1.0。</span><span class="sxs-lookup"><span data-stu-id="d7793-121">The default fog density is 1.0.</span></span><br/>                                                                                                                                    |
| <span id="GL_FOG_START"></span><span id="gl_fog_start"></span><dl> <span data-ttu-id="d7793-122"><dt>**GL \_ 霧化 \_ 開始**</dt></span><span class="sxs-lookup"><span data-stu-id="d7793-122"><dt>**GL\_FOG\_START**</dt></span></span> </dl>       | <span data-ttu-id="d7793-123">*Params* 參數是單一浮點數，用來指定線性霧化方程式中所使用的 *開始* 位置（接近距離）。</span><span class="sxs-lookup"><span data-stu-id="d7793-123">The *params* parameter is a single floating-point value that specifies *start*, the near distance used in the linear fog equation.</span></span> <span data-ttu-id="d7793-124">預設接近距離為0.0。</span><span class="sxs-lookup"><span data-stu-id="d7793-124">The default near distance is 0.0.</span></span><br/>                                                                                                                                                                                  |
| <span id="GL_FOG_END"></span><span id="gl_fog_end"></span><dl> <span data-ttu-id="d7793-125"><dt>**GL \_ 霧化 \_ 結束**</dt></span><span class="sxs-lookup"><span data-stu-id="d7793-125"><dt>**GL\_FOG\_END**</dt></span></span> </dl>             | <span data-ttu-id="d7793-126">*Params* 參數是單一浮點值，可指定線性霧化方程式中所使用的 *結束* 距離。</span><span class="sxs-lookup"><span data-stu-id="d7793-126">The *params* parameter is a single floating-point value that specifies *end*, the far distance used in the linear fog equation.</span></span> <span data-ttu-id="d7793-127">預設距離為1.0。</span><span class="sxs-lookup"><span data-stu-id="d7793-127">The default far distance is 1.0.</span></span><br/>                                                                                                                                                                                      |
| <span id="GL_FOG_INDEX"></span><span id="gl_fog_index"></span><dl> <span data-ttu-id="d7793-128"><dt>**GL \_ 霧化 \_ 索引**</dt></span><span class="sxs-lookup"><span data-stu-id="d7793-128"><dt>**GL\_FOG\_INDEX**</dt></span></span> </dl>       | <span data-ttu-id="d7793-129">*Params* 參數是指定 *i*<sub>f</sub> 、霧化色彩索引的單一浮點值。</span><span class="sxs-lookup"><span data-stu-id="d7793-129">The *params* parameter is a single floating-point value that specifies *i*<sub>f</sub> , the fog color index.</span></span> <span data-ttu-id="d7793-130">預設的霧化索引為0.0。</span><span class="sxs-lookup"><span data-stu-id="d7793-130">The default fog index is 0.0.</span></span><br/>                                                                                                                                                                                                           |



 

</dd> <dt>

<span data-ttu-id="d7793-131">*param*</span><span class="sxs-lookup"><span data-stu-id="d7793-131">*param*</span></span> 
</dt> <dd>

<span data-ttu-id="d7793-132">指定 *pname* 將設定為的值。</span><span class="sxs-lookup"><span data-stu-id="d7793-132">Specifies the value that *pname* will be set to.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7793-133">傳回值</span><span class="sxs-lookup"><span data-stu-id="d7793-133">Return value</span></span>

<span data-ttu-id="d7793-134">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="d7793-134">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="d7793-135">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="d7793-135">Error codes</span></span>

<span data-ttu-id="d7793-136">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="d7793-136">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="d7793-137">Name</span><span class="sxs-lookup"><span data-stu-id="d7793-137">Name</span></span>                                                                                                  | <span data-ttu-id="d7793-138">意義</span><span class="sxs-lookup"><span data-stu-id="d7793-138">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d7793-139"><dt>**GL \_ 無效 \_ 列舉**</dt></span><span class="sxs-lookup"><span data-stu-id="d7793-139"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="d7793-140">*pname* 不是可接受的值。</span><span class="sxs-lookup"><span data-stu-id="d7793-140">*pname* was not an accepted value.</span></span><br/>                                                                                         |
| <dl> <span data-ttu-id="d7793-141"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="d7793-141"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="d7793-142">呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。</span><span class="sxs-lookup"><span data-stu-id="d7793-142">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="d7793-143">備註</span><span class="sxs-lookup"><span data-stu-id="d7793-143">Remarks</span></span>

<span data-ttu-id="d7793-144">您可以使用引數 GL 霧化來啟用和停用 [**glEnable**](glenable.md) 和 [**glDisable**](gldisable.md)的霧化 \_ 。</span><span class="sxs-lookup"><span data-stu-id="d7793-144">You enable and disable fog with [**glEnable**](glenable.md) and [**glDisable**](gldisable.md), using the argument GL\_FOG.</span></span> <span data-ttu-id="d7793-145">啟用時，霧化會影響點陣化幾何、點陣圖和圖元區塊，但不會影響緩衝區清除作業。</span><span class="sxs-lookup"><span data-stu-id="d7793-145">While enabled, fog affects rasterized geometry, bitmaps, and pixel blocks, but not buffer-clear operations.</span></span>

<span data-ttu-id="d7793-146">**GlFogf** 函式會將 *params* 中的值或值指派給 *pname* 所指定的霧化參數。</span><span class="sxs-lookup"><span data-stu-id="d7793-146">The **glFogf** function assigns the value or values in *params* to the fog parameter specified by *pname*.</span></span>

<span data-ttu-id="d7793-147">霧化會使用混色因數 *f* 來混合霧化色彩與每個柵格化圖元片段的 posttexturing 色彩。</span><span class="sxs-lookup"><span data-stu-id="d7793-147">Fog blends a fog color with each rasterized pixel fragment's posttexturing color using a blending factor *f*.</span></span> <span data-ttu-id="d7793-148">第三種方式是以三種方式的其中一種來計算，視霧化 *模式而定* 。</span><span class="sxs-lookup"><span data-stu-id="d7793-148">Factor *f* is computed in one of three ways, depending on the fog mode.</span></span> <span data-ttu-id="d7793-149">讓 *z* 成為從原點到所 fogged 之片段的眼睛距離。</span><span class="sxs-lookup"><span data-stu-id="d7793-149">Let *z* be the distance in eye coordinates from the origin to the fragment being fogged.</span></span> <span data-ttu-id="d7793-150">GL \_ 線性模糊的方程式如下：</span><span class="sxs-lookup"><span data-stu-id="d7793-150">The equation for GL\_LINEAR fog is:</span></span>

![顯示 GL_LINEAR 霧化值的方程式。](images/fog01.png)

<span data-ttu-id="d7793-152">GL \_ EXP 霧化的方程式如下：</span><span class="sxs-lookup"><span data-stu-id="d7793-152">The equation for GL\_EXP fog is:</span></span>

![顯示 GL_EXP 霧化模式中混合因數值的方程式。](images/fog02.png)

<span data-ttu-id="d7793-154">GL \_ EXP2 霧化的方程式是：</span><span class="sxs-lookup"><span data-stu-id="d7793-154">The equation for GL\_EXP2 fog is:</span></span>

![顯示 GL_EXP2 霧化模式中混合因數值的方程式。](images/fog03.png)

<span data-ttu-id="d7793-156">不論霧化模式為何， *f* 都是在計算後壓制至範圍 \[ 0、1 \] 。</span><span class="sxs-lookup"><span data-stu-id="d7793-156">Regardless of the fog mode, *f* is clamped to the range \[0,1\] after it is computed.</span></span> <span data-ttu-id="d7793-157">然後，如果 OpenGL 處於 RGBA 色彩模式，則會將片段的色彩 *C*<sub>r</sub> 取代為</span><span class="sxs-lookup"><span data-stu-id="d7793-157">Then, if OpenGL is in RGBA color mode, the fragment's color *C*<sub>r</sub> is replaced by</span></span>

![顯示 fogged 片段色彩的方程式，做為混色因數和霧化色彩的函式。](images/fog04.png)

<span data-ttu-id="d7793-159">在色彩索引模式中，片段的色彩索引 *i*<sub>r</sub> 會取代為</span><span class="sxs-lookup"><span data-stu-id="d7793-159">In color-index mode, the fragment's color index *i*<sub>r</sub> is replaced by</span></span>

![顯示 fogged 片段之色彩索引的方程式，做為混合因數和索引色彩的函式。](images/fog05.png)

<span data-ttu-id="d7793-161">下列函式會取出與 **glFog** 函數相關的資訊：</span><span class="sxs-lookup"><span data-stu-id="d7793-161">The following functions retrieve information related to the **glFog** functions:</span></span>

<span data-ttu-id="d7793-162">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 霧化 \_ 色彩的 glGet</span><span class="sxs-lookup"><span data-stu-id="d7793-162">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_FOG\_COLOR</span></span>

<span data-ttu-id="d7793-163">具有引數 GL \_ 霧化 \_ 索引的 glGet</span><span class="sxs-lookup"><span data-stu-id="d7793-163">**glGet** with argument GL\_FOG\_INDEX</span></span>

<span data-ttu-id="d7793-164">具有引數 GL \_ 霧化 \_ 密度的 glGet</span><span class="sxs-lookup"><span data-stu-id="d7793-164">**glGet** with argument GL\_FOG\_DENSITY</span></span>

<span data-ttu-id="d7793-165">具有引數 GL \_ 霧化 \_ 開始的 glGet</span><span class="sxs-lookup"><span data-stu-id="d7793-165">**glGet** with argument GL\_FOG\_START</span></span>

<span data-ttu-id="d7793-166">具有引數 GL \_ 霧化 \_ END 的 glGet</span><span class="sxs-lookup"><span data-stu-id="d7793-166">**glGet** with argument GL\_FOG\_END</span></span>

<span data-ttu-id="d7793-167">具有引數 GL \_ 霧化 \_ 模式的 glGet</span><span class="sxs-lookup"><span data-stu-id="d7793-167">**glGet** with argument GL\_FOG\_MODE</span></span>

<span data-ttu-id="d7793-168">[](glisenabled.md)具有引數 GL \_ 霧化的 glIsEnabled</span><span class="sxs-lookup"><span data-stu-id="d7793-168">[**glIsEnabled**](glisenabled.md) with argument GL\_FOG</span></span>

## <a name="requirements"></a><span data-ttu-id="d7793-169">規格需求</span><span class="sxs-lookup"><span data-stu-id="d7793-169">Requirements</span></span>



| <span data-ttu-id="d7793-170">需求</span><span class="sxs-lookup"><span data-stu-id="d7793-170">Requirement</span></span> | <span data-ttu-id="d7793-171">值</span><span class="sxs-lookup"><span data-stu-id="d7793-171">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d7793-172">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d7793-172">Minimum supported client</span></span><br/> | <span data-ttu-id="d7793-173">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d7793-173">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="d7793-174">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d7793-174">Minimum supported server</span></span><br/> | <span data-ttu-id="d7793-175">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d7793-175">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d7793-176">標頭</span><span class="sxs-lookup"><span data-stu-id="d7793-176">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7793-177"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="d7793-177"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="d7793-178">程式庫</span><span class="sxs-lookup"><span data-stu-id="d7793-178">Library</span></span><br/>                  | <dl> <span data-ttu-id="d7793-179"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="d7793-179"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="d7793-180">DLL</span><span class="sxs-lookup"><span data-stu-id="d7793-180">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d7793-181"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d7793-181"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7793-182">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d7793-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7793-183">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="d7793-183">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="d7793-184">**glDisable**</span><span class="sxs-lookup"><span data-stu-id="d7793-184">**glDisable**</span></span>](gldisable.md)
</dt> <dt>

[<span data-ttu-id="d7793-185">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="d7793-185">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="d7793-186">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="d7793-186">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="d7793-187">**glGet**</span><span class="sxs-lookup"><span data-stu-id="d7793-187">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="d7793-188">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="d7793-188">**glIsEnabled**</span></span>](glisenabled.md)
</dt> </dl>

 

 





