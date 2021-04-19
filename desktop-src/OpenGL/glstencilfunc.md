---
title: 'glStencilFunc 函式 (Gl) '
description: GlStencilFunc 函數會設定樣板測試的函數和參考值。
ms.assetid: 6c84415b-4d22-494b-90f2-6243d1406725
keywords:
- glStencilFunc 函式 OpenGL
topic_type:
- apiref
api_name:
- glStencilFunc
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd4f9c0a5ec905ecb061ddb54984bf35ff8edc3d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966959"
---
# <a name="glstencilfunc-function"></a><span data-ttu-id="d8ad5-104">glStencilFunc 函式</span><span class="sxs-lookup"><span data-stu-id="d8ad5-104">glStencilFunc function</span></span>

<span data-ttu-id="d8ad5-105">**GlStencilFunc** 函數會設定樣板測試的函數和參考值。</span><span class="sxs-lookup"><span data-stu-id="d8ad5-105">The **glStencilFunc** function sets the function and reference value for stencil testing.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8ad5-106">語法</span><span class="sxs-lookup"><span data-stu-id="d8ad5-106">Syntax</span></span>


```C++
void WINAPI glStencilFunc(
   GLenum func,
   GLint  ref,
   GLuint mask
);
```



## <a name="parameters"></a><span data-ttu-id="d8ad5-107">參數</span><span class="sxs-lookup"><span data-stu-id="d8ad5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8ad5-108">*func*</span><span class="sxs-lookup"><span data-stu-id="d8ad5-108">*func*</span></span> 
</dt> <dd>

<span data-ttu-id="d8ad5-109">測試函數。</span><span class="sxs-lookup"><span data-stu-id="d8ad5-109">The test function.</span></span> <span data-ttu-id="d8ad5-110">下列八個權杖都有效。</span><span class="sxs-lookup"><span data-stu-id="d8ad5-110">The following eight tokens are valid.</span></span>



| <span data-ttu-id="d8ad5-111">值</span><span class="sxs-lookup"><span data-stu-id="d8ad5-111">Value</span></span>                                                                                                                                                   | <span data-ttu-id="d8ad5-112">意義</span><span class="sxs-lookup"><span data-stu-id="d8ad5-112">Meaning</span></span>                                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="GL_NEVER"></span><span id="gl_never"></span><dl> <span data-ttu-id="d8ad5-113"><dt>**GL \_ 永不**</dt></span><span class="sxs-lookup"><span data-stu-id="d8ad5-113"><dt>**GL\_NEVER**</dt></span></span> </dl>          | <span data-ttu-id="d8ad5-114">一律會失敗。</span><span class="sxs-lookup"><span data-stu-id="d8ad5-114">Always fails.</span></span><br/>                                         |
| <span id="GL_LESS"></span><span id="gl_less"></span><dl> <span data-ttu-id="d8ad5-115"><dt>**GL \_ LESS**</dt></span><span class="sxs-lookup"><span data-stu-id="d8ad5-115"><dt>**GL\_LESS**</dt></span></span> </dl>             | <span data-ttu-id="d8ad5-116">如果 (*ref*  &  *mask*) < (樣板  &  *遮罩*) ，則傳遞。</span><span class="sxs-lookup"><span data-stu-id="d8ad5-116">Passes if (*ref* & *mask*) < (*stencil* & *mask*).</span></span><br/> |
| <span id="GL_LEQUAL"></span><span id="gl_lequal"></span><dl> <span data-ttu-id="d8ad5-117"><dt>**GL \_ LEQUAL**</dt></span><span class="sxs-lookup"><span data-stu-id="d8ad5-117"><dt>**GL\_LEQUAL**</dt></span></span> </dl>       | <span data-ttu-id="d8ad5-118">如果 (*ref*  &  *mask*) = (樣板  &  *遮罩*) ，則傳遞。</span><span class="sxs-lookup"><span data-stu-id="d8ad5-118">Passes if (*ref* & *mask*) = (*stencil* & *mask*).</span></span><br/>    |
| <span id="GL_GREATER"></span><span id="gl_greater"></span><dl> <span data-ttu-id="d8ad5-119"><dt>**GL \_ 更高**</dt></span><span class="sxs-lookup"><span data-stu-id="d8ad5-119"><dt>**GL\_GREATER**</dt></span></span> </dl>    | <span data-ttu-id="d8ad5-120">如果 (*ref*  &  *mask*) > (樣板  &  *遮罩*) ，則傳遞。</span><span class="sxs-lookup"><span data-stu-id="d8ad5-120">Passes if (*ref* & *mask*) > (*stencil* & *mask*).</span></span><br/> |
| <span id="GL_GEQUAL"></span><span id="gl_gequal"></span><dl> <span data-ttu-id="d8ad5-121"><dt>**GL \_ GEQUAL**</dt></span><span class="sxs-lookup"><span data-stu-id="d8ad5-121"><dt>**GL\_GEQUAL**</dt></span></span> </dl>       | <span data-ttu-id="d8ad5-122">如果 (*ref*  &  *mask*) = (樣板  &  *遮罩*) ，則傳遞。</span><span class="sxs-lookup"><span data-stu-id="d8ad5-122">Passes if (*ref* & *mask*) = (*stencil* & *mask*).</span></span><br/>    |
| <span id="GL_EQUAL"></span><span id="gl_equal"></span><dl> <span data-ttu-id="d8ad5-123"><dt>**GL \_ 相等**</dt></span><span class="sxs-lookup"><span data-stu-id="d8ad5-123"><dt>**GL\_EQUAL**</dt></span></span> </dl>          | <span data-ttu-id="d8ad5-124">如果 (*ref*  &  *mask*) = (樣板  &  *遮罩*) ，則傳遞。</span><span class="sxs-lookup"><span data-stu-id="d8ad5-124">Passes if (*ref* & *mask*) = (*stencil* & *mask*).</span></span><br/>    |
| <span id="GL_NOTEQUAL"></span><span id="gl_notequal"></span><dl> <span data-ttu-id="d8ad5-125"><dt>**GL \_ NOTEQUAL**</dt></span><span class="sxs-lookup"><span data-stu-id="d8ad5-125"><dt>**GL\_NOTEQUAL**</dt></span></span> </dl> | <span data-ttu-id="d8ad5-126">如果 (*ref*  &  *遮罩*) ，則傳遞？</span><span class="sxs-lookup"><span data-stu-id="d8ad5-126">Passes if (*ref* & *mask*) ?</span></span> <span data-ttu-id="d8ad5-127"> (*樣板*  &  *遮罩*) 。</span><span class="sxs-lookup"><span data-stu-id="d8ad5-127">(*stencil* & *mask*).</span></span><br/>    |
| <span id="GL_ALWAYS"></span><span id="gl_always"></span><dl> <span data-ttu-id="d8ad5-128"><dt>**GL \_ 一律**</dt></span><span class="sxs-lookup"><span data-stu-id="d8ad5-128"><dt>**GL\_ALWAYS**</dt></span></span> </dl>       | <span data-ttu-id="d8ad5-129">一律傳遞。</span><span class="sxs-lookup"><span data-stu-id="d8ad5-129">Always passes.</span></span><br/>                                        |



 

</dd> <dt>

<span data-ttu-id="d8ad5-130">*ref*</span><span class="sxs-lookup"><span data-stu-id="d8ad5-130">*ref*</span></span> 
</dt> <dd>

<span data-ttu-id="d8ad5-131">樣板測試的參考值。</span><span class="sxs-lookup"><span data-stu-id="d8ad5-131">The reference value for the stencil test.</span></span> <span data-ttu-id="d8ad5-132">*Ref* 參數壓制至範圍 \[ 0，2 *n* 1 \] ，其中 *n* 是樣板緩衝區中的 bitplanes 數目。</span><span class="sxs-lookup"><span data-stu-id="d8ad5-132">The *ref* parameter is clamped to the range \[0, 2 *n* 1\], where *n* is the number of bitplanes in the stencil buffer.</span></span>

</dd> <dt>

<span data-ttu-id="d8ad5-133">*面具*</span><span class="sxs-lookup"><span data-stu-id="d8ad5-133">*mask*</span></span> 
</dt> <dd>

<span data-ttu-id="d8ad5-134">當測試完成時 **，同時** 具有參考值和儲存的樣板值的遮罩。</span><span class="sxs-lookup"><span data-stu-id="d8ad5-134">A mask that is **AND** ed with both the reference value and the stored stencil value when the test is done.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8ad5-135">傳回值</span><span class="sxs-lookup"><span data-stu-id="d8ad5-135">Return value</span></span>

<span data-ttu-id="d8ad5-136">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="d8ad5-136">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="d8ad5-137">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="d8ad5-137">Error codes</span></span>

<span data-ttu-id="d8ad5-138">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="d8ad5-138">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="d8ad5-139">Name</span><span class="sxs-lookup"><span data-stu-id="d8ad5-139">Name</span></span>                                                                                                  | <span data-ttu-id="d8ad5-140">意義</span><span class="sxs-lookup"><span data-stu-id="d8ad5-140">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d8ad5-141"><dt>**GL \_ 無效 \_ 列舉**</dt></span><span class="sxs-lookup"><span data-stu-id="d8ad5-141"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="d8ad5-142">*func* 不是八個接受值的其中一個。</span><span class="sxs-lookup"><span data-stu-id="d8ad5-142">*func* was not one of the eight accepted values.</span></span><br/>                                                                           |
| <dl> <span data-ttu-id="d8ad5-143"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="d8ad5-143"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="d8ad5-144">呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。</span><span class="sxs-lookup"><span data-stu-id="d8ad5-144">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="d8ad5-145">備註</span><span class="sxs-lookup"><span data-stu-id="d8ad5-145">Remarks</span></span>

<span data-ttu-id="d8ad5-146">Stenciling，例如 *z* 緩衝，可啟用和停用以每圖元為基礎的繪圖。</span><span class="sxs-lookup"><span data-stu-id="d8ad5-146">Stenciling, like *z*-buffering, enables and disables drawing on a per-pixel basis.</span></span> <span data-ttu-id="d8ad5-147">您可以使用 OpenGL 繪圖基本專案來繪製到樣板平面，然後轉譯幾何和影像，使用樣板平面來遮蔽畫面的部分。</span><span class="sxs-lookup"><span data-stu-id="d8ad5-147">You draw into the stencil planes using OpenGL drawing primitives, then render geometry and images, using the stencil planes to mask out portions of the screen.</span></span> <span data-ttu-id="d8ad5-148">Stenciling 通常用於 multipass 轉譯演算法，以達成特殊效果，例如 decals、大綱和具建設性的純幾何呈現。</span><span class="sxs-lookup"><span data-stu-id="d8ad5-148">Stenciling is typically used in multipass rendering algorithms to achieve special effects, such as decals, outlining, and constructive solid geometry rendering.</span></span>

<span data-ttu-id="d8ad5-149">樣板測試會根據參考值與樣板緩衝區中的值之間的比較結果，有條件地排除圖元。</span><span class="sxs-lookup"><span data-stu-id="d8ad5-149">The stencil test conditionally eliminates a pixel based on the outcome of a comparison between the reference value and the value in the stencil buffer.</span></span> <span data-ttu-id="d8ad5-150">[**GlEnable**](glenable.md)和 [**glDisable**](gldisable.md)會使用引數 GL 樣板測試來啟用測試 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="d8ad5-150">The test is enabled by [**glEnable**](glenable.md) and [**glDisable**](gldisable.md) with argument GL\_STENCIL\_TEST.</span></span> <span data-ttu-id="d8ad5-151">根據樣板測試結果所採取的動作會以 [**glStencilOp**](glstencilop.md)指定。</span><span class="sxs-lookup"><span data-stu-id="d8ad5-151">Actions taken based on the outcome of the stencil test are specified with [**glStencilOp**](glstencilop.md).</span></span>

<span data-ttu-id="d8ad5-152">*Func* 參數是決定樣板比較函數的符號常數。</span><span class="sxs-lookup"><span data-stu-id="d8ad5-152">The *func* parameter is a symbolic constant that determines the stencil comparison function.</span></span> <span data-ttu-id="d8ad5-153">它會接受上面所示的八個值之一。</span><span class="sxs-lookup"><span data-stu-id="d8ad5-153">It accepts one of the eight values shown above.</span></span> <span data-ttu-id="d8ad5-154">*Ref* 參數是用於樣板比較的整數參考值。</span><span class="sxs-lookup"><span data-stu-id="d8ad5-154">The *ref* parameter is an integer reference value that is used in the stencil comparison.</span></span> <span data-ttu-id="d8ad5-155">它會壓制至範圍 \[ 0，2 *n* 1 \] ，其中 *n* 是樣板緩衝區中的 bitplanes 數目。</span><span class="sxs-lookup"><span data-stu-id="d8ad5-155">It is clamped to the range \[0, 2 *n* 1\], where *n* is the number of bitplanes in the stencil buffer.</span></span> <span data-ttu-id="d8ad5-156">*Mask* 參數是使用參考值和預存樣板值的位 **And** ed，並參與比較的 **和** ed 值。</span><span class="sxs-lookup"><span data-stu-id="d8ad5-156">The *mask* parameter is bitwise **AND** ed with both the reference value and the stored stencil value, with the **AND** ed values participating in the comparison.</span></span>

<span data-ttu-id="d8ad5-157">如果樣板表示儲存在對應之樣板緩衝區位置的值 *，則上述* 清單會顯示 *func* 可指定之每個比較函式的效果。</span><span class="sxs-lookup"><span data-stu-id="d8ad5-157">If *stencil* represents the value stored in the corresponding stencil buffer location, the preceding list shows the effect of each comparison function that can be specified by *func*.</span></span> <span data-ttu-id="d8ad5-158">只有在比較成功時，才會將圖元傳遞給點陣化進程中的下一個階段 (請參閱 [**glStencilOp**](glstencilop.md)) 。</span><span class="sxs-lookup"><span data-stu-id="d8ad5-158">Only if the comparison succeeds is the pixel passed through to the next stage in the rasterization process (see [**glStencilOp**](glstencilop.md)).</span></span> <span data-ttu-id="d8ad5-159">所有測試都會將 *樣板值視為* 範圍 \[ 0，2 *n* 1 的不帶正負號的整數， \] 其中 *n* 是樣板緩衝區中的 bitplanes 數目。</span><span class="sxs-lookup"><span data-stu-id="d8ad5-159">All tests treat *stencil* values as unsigned integers in the range \[0, 2 *n* 1\], where *n* is the number of bitplanes in the stencil buffer.</span></span>

<span data-ttu-id="d8ad5-160">一開始，樣板測試已停用。</span><span class="sxs-lookup"><span data-stu-id="d8ad5-160">Initially, the stencil test is disabled.</span></span> <span data-ttu-id="d8ad5-161">如果沒有樣板緩衝區，則不會進行任何樣板修改，如同樣板測試一律會通過。</span><span class="sxs-lookup"><span data-stu-id="d8ad5-161">If there is no stencil buffer, no stencil modification can occur and it is as if the stencil test always passes.</span></span>

<span data-ttu-id="d8ad5-162">下列函式會取出與 **glStencilFunc** 相關的資訊：</span><span class="sxs-lookup"><span data-stu-id="d8ad5-162">The following functions retrieve information related to **glStencilFunc**:</span></span>

<span data-ttu-id="d8ad5-163">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 樣板 \_ FUNC 的 glGet</span><span class="sxs-lookup"><span data-stu-id="d8ad5-163">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_STENCIL\_FUNC</span></span>

<span data-ttu-id="d8ad5-164">具有引數 GL \_ 範本 \_ 值 \_ 遮罩的 glGet</span><span class="sxs-lookup"><span data-stu-id="d8ad5-164">**glGet** with argument GL\_STENCIL\_VALUE\_MASK</span></span>

<span data-ttu-id="d8ad5-165">具有引數 GL \_ 樣板 \_ REF 的 glGet</span><span class="sxs-lookup"><span data-stu-id="d8ad5-165">**glGet** with argument GL\_STENCIL\_REF</span></span>

<span data-ttu-id="d8ad5-166">具有引數 GL \_ 樣板 \_ 位的 glGet</span><span class="sxs-lookup"><span data-stu-id="d8ad5-166">**glGet** with argument GL\_STENCIL\_BITS</span></span>

<span data-ttu-id="d8ad5-167">[](glisenabled.md)具有引數 GL \_ 樣板 \_ 測試的 glIsEnabled</span><span class="sxs-lookup"><span data-stu-id="d8ad5-167">[**glIsEnabled**](glisenabled.md) with argument GL\_STENCIL\_TEST</span></span>

## <a name="requirements"></a><span data-ttu-id="d8ad5-168">規格需求</span><span class="sxs-lookup"><span data-stu-id="d8ad5-168">Requirements</span></span>



| <span data-ttu-id="d8ad5-169">需求</span><span class="sxs-lookup"><span data-stu-id="d8ad5-169">Requirement</span></span> | <span data-ttu-id="d8ad5-170">值</span><span class="sxs-lookup"><span data-stu-id="d8ad5-170">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d8ad5-171">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d8ad5-171">Minimum supported client</span></span><br/> | <span data-ttu-id="d8ad5-172">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d8ad5-172">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="d8ad5-173">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d8ad5-173">Minimum supported server</span></span><br/> | <span data-ttu-id="d8ad5-174">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d8ad5-174">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d8ad5-175">標頭</span><span class="sxs-lookup"><span data-stu-id="d8ad5-175">Header</span></span><br/>                   | <dl> <span data-ttu-id="d8ad5-176"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="d8ad5-176"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="d8ad5-177">程式庫</span><span class="sxs-lookup"><span data-stu-id="d8ad5-177">Library</span></span><br/>                  | <dl> <span data-ttu-id="d8ad5-178"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="d8ad5-178"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="d8ad5-179">DLL</span><span class="sxs-lookup"><span data-stu-id="d8ad5-179">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d8ad5-180"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d8ad5-180"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8ad5-181">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d8ad5-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8ad5-182">**glAlphaFunc**</span><span class="sxs-lookup"><span data-stu-id="d8ad5-182">**glAlphaFunc**</span></span>](glalphafunc.md)
</dt> <dt>

[<span data-ttu-id="d8ad5-183">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="d8ad5-183">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="d8ad5-184">**glBlendFunc**</span><span class="sxs-lookup"><span data-stu-id="d8ad5-184">**glBlendFunc**</span></span>](glblendfunc.md)
</dt> <dt>

[<span data-ttu-id="d8ad5-185">**glDepthFunc**</span><span class="sxs-lookup"><span data-stu-id="d8ad5-185">**glDepthFunc**</span></span>](gldepthfunc.md)
</dt> <dt>

[<span data-ttu-id="d8ad5-186">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="d8ad5-186">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="d8ad5-187">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="d8ad5-187">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="d8ad5-188">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="d8ad5-188">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="d8ad5-189">**glLogicOp**</span><span class="sxs-lookup"><span data-stu-id="d8ad5-189">**glLogicOp**</span></span>](gllogicop.md)
</dt> <dt>

[<span data-ttu-id="d8ad5-190">**glStencilOp**</span><span class="sxs-lookup"><span data-stu-id="d8ad5-190">**glStencilOp**</span></span>](glstencilop.md)
</dt> </dl>

 

 





