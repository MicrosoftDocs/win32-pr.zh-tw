---
title: 'glStencilOp 函式 (Gl) '
description: GlStencilOp 函數會設定樣板測試動作。
ms.assetid: 16809735-5624-49cf-bfa5-9908d008b234
keywords:
- glStencilOp 函式 OpenGL
topic_type:
- apiref
api_name:
- glStencilOp
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b23162f8606ed68dc90a0cb6debdcc903e0ccd0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965511"
---
# <a name="glstencilop-function"></a><span data-ttu-id="df868-104">glStencilOp 函式</span><span class="sxs-lookup"><span data-stu-id="df868-104">glStencilOp function</span></span>

<span data-ttu-id="df868-105">**GlStencilOp** 函數會設定樣板測試動作。</span><span class="sxs-lookup"><span data-stu-id="df868-105">The **glStencilOp** function sets the stencil test actions.</span></span>

## <a name="syntax"></a><span data-ttu-id="df868-106">語法</span><span class="sxs-lookup"><span data-stu-id="df868-106">Syntax</span></span>


```C++
void WINAPI glStencilOp(
   GLenum fail,
   GLenum zfail,
   GLenum zpass
);
```



## <a name="parameters"></a><span data-ttu-id="df868-107">參數</span><span class="sxs-lookup"><span data-stu-id="df868-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df868-108">*失敗*</span><span class="sxs-lookup"><span data-stu-id="df868-108">*fail*</span></span> 
</dt> <dd>

<span data-ttu-id="df868-109">樣板測試失敗時所要採取的動作。</span><span class="sxs-lookup"><span data-stu-id="df868-109">The action to take when the stencil test fails.</span></span> <span data-ttu-id="df868-110">接受下列六個符號常數。</span><span class="sxs-lookup"><span data-stu-id="df868-110">The following six symbolic constants are accepted.</span></span>



| <span data-ttu-id="df868-111">值</span><span class="sxs-lookup"><span data-stu-id="df868-111">Value</span></span>                                                                                                                                                | <span data-ttu-id="df868-112">意義</span><span class="sxs-lookup"><span data-stu-id="df868-112">Meaning</span></span>                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span id="GL_KEEP"></span><span id="gl_keep"></span><dl> <span data-ttu-id="df868-113"><dt>**GL \_ 保留**</dt></span><span class="sxs-lookup"><span data-stu-id="df868-113"><dt>**GL\_KEEP**</dt></span></span> </dl>          | <span data-ttu-id="df868-114">保留目前的值。</span><span class="sxs-lookup"><span data-stu-id="df868-114">Keeps the current value.</span></span><br/>                                                                         |
| <span id="GL_ZERO"></span><span id="gl_zero"></span><dl> <span data-ttu-id="df868-115"><dt>**GL \_ 零**</dt></span><span class="sxs-lookup"><span data-stu-id="df868-115"><dt>**GL\_ZERO**</dt></span></span> </dl>          | <span data-ttu-id="df868-116">將樣板緩衝區值設定為零。</span><span class="sxs-lookup"><span data-stu-id="df868-116">Sets the stencil buffer value to zero.</span></span><br/>                                                           |
| <span id="GL_REPLACE"></span><span id="gl_replace"></span><dl> <span data-ttu-id="df868-117"><dt>**GL \_ 取代**</dt></span><span class="sxs-lookup"><span data-stu-id="df868-117"><dt>**GL\_REPLACE**</dt></span></span> </dl> | <span data-ttu-id="df868-118">將樣板緩衝區值設定為 *ref*（如 **glStencilFunc** 所指定）。</span><span class="sxs-lookup"><span data-stu-id="df868-118">Sets the stencil buffer value to *ref*, as specified by **glStencilFunc**.</span></span><br/>                       |
| <span id="GL_INCR"></span><span id="gl_incr"></span><dl> <span data-ttu-id="df868-119"><dt>**GL \_ 增量**</dt></span><span class="sxs-lookup"><span data-stu-id="df868-119"><dt>**GL\_INCR**</dt></span></span> </dl>          | <span data-ttu-id="df868-120">遞增目前的樣板緩衝區值。</span><span class="sxs-lookup"><span data-stu-id="df868-120">Increments the current stencil buffer value.</span></span> <span data-ttu-id="df868-121">個至可表示的最大不帶正負號值。</span><span class="sxs-lookup"><span data-stu-id="df868-121">Clamps to the maximum representable unsigned value.</span></span><br/> |
| <span id="GL_DECR"></span><span id="gl_decr"></span><dl> <span data-ttu-id="df868-122"><dt>**GL \_ OPERATORS.DECR**</dt></span><span class="sxs-lookup"><span data-stu-id="df868-122"><dt>**GL\_DECR**</dt></span></span> </dl>          | <span data-ttu-id="df868-123">遞減目前的樣板緩衝區值。</span><span class="sxs-lookup"><span data-stu-id="df868-123">Decrements the current stencil buffer value.</span></span> <span data-ttu-id="df868-124">個為零。</span><span class="sxs-lookup"><span data-stu-id="df868-124">Clamps to zero.</span></span><br/>                                     |
| <span id="GL_INVERT"></span><span id="gl_invert"></span><dl> <span data-ttu-id="df868-125"><dt>**GL \_ 反轉**</dt></span><span class="sxs-lookup"><span data-stu-id="df868-125"><dt>**GL\_INVERT**</dt></span></span> </dl>    | <span data-ttu-id="df868-126">以位反轉目前的樣板緩衝區值。</span><span class="sxs-lookup"><span data-stu-id="df868-126">Bitwise inverts the current stencil buffer value.</span></span><br/>                                                |



 

</dd> <dt>

<span data-ttu-id="df868-127">*zfail*</span><span class="sxs-lookup"><span data-stu-id="df868-127">*zfail*</span></span> 
</dt> <dd>

<span data-ttu-id="df868-128">樣板測試通過時的樣板動作，但深度測試會失敗。</span><span class="sxs-lookup"><span data-stu-id="df868-128">Stencil action when the stencil test passes, but the depth test fails.</span></span> <span data-ttu-id="df868-129">接受與失敗相同的符號常數 *。*</span><span class="sxs-lookup"><span data-stu-id="df868-129">Accepts the same symbolic constants as *fail.*</span></span>

</dd> <dt>

<span data-ttu-id="df868-130">*zpass*</span><span class="sxs-lookup"><span data-stu-id="df868-130">*zpass*</span></span> 
</dt> <dd>

<span data-ttu-id="df868-131">樣板測試和深度測試成功時，或樣板測試通過，而且沒有啟用深度緩衝區或深度測試時的樣板動作。</span><span class="sxs-lookup"><span data-stu-id="df868-131">Stencil action when both the stencil test and the depth test pass, or when the stencil test passes and either there is no depth buffer or depth testing is not enabled.</span></span> <span data-ttu-id="df868-132">接受與 *失敗* 相同的符號常數。</span><span class="sxs-lookup"><span data-stu-id="df868-132">Accepts the same symbolic constants as *fail*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df868-133">傳回值</span><span class="sxs-lookup"><span data-stu-id="df868-133">Return value</span></span>

<span data-ttu-id="df868-134">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="df868-134">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="df868-135">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="df868-135">Error codes</span></span>

<span data-ttu-id="df868-136">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="df868-136">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="df868-137">Name</span><span class="sxs-lookup"><span data-stu-id="df868-137">Name</span></span>                                                                                                  | <span data-ttu-id="df868-138">意義</span><span class="sxs-lookup"><span data-stu-id="df868-138">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="df868-139"><dt>**GL \_ 無效 \_ 列舉**</dt></span><span class="sxs-lookup"><span data-stu-id="df868-139"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="df868-140">*fail*、 *zfail* 或 *zpass* 是六個定義常數值以外的任何值。</span><span class="sxs-lookup"><span data-stu-id="df868-140">*fail*, *zfail*, or *zpass* was any value other than the six defined constant values.</span></span><br/>                                      |
| <dl> <span data-ttu-id="df868-141"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="df868-141"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="df868-142">呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。</span><span class="sxs-lookup"><span data-stu-id="df868-142">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="df868-143">備註</span><span class="sxs-lookup"><span data-stu-id="df868-143">Remarks</span></span>

<span data-ttu-id="df868-144">Stenciling，例如 *z* 緩衝，可啟用和停用以每圖元為基礎的繪圖。</span><span class="sxs-lookup"><span data-stu-id="df868-144">Stenciling, like *z*-buffering, enables and disables drawing on a per-pixel basis.</span></span> <span data-ttu-id="df868-145">您可以使用 OpenGL 繪圖基本專案來繪製到樣板平面，然後轉譯幾何和影像，使用樣板平面來遮蔽畫面的部分。</span><span class="sxs-lookup"><span data-stu-id="df868-145">You draw into the stencil planes using OpenGL drawing primitives, then render geometry and images, using the stencil planes to mask out portions of the screen.</span></span> <span data-ttu-id="df868-146">Stenciling 通常用於 multipass 轉譯演算法，以達成特殊效果，例如 decals、大綱和具建設性的純幾何呈現。</span><span class="sxs-lookup"><span data-stu-id="df868-146">Stenciling is typically used in multipass rendering algorithms to achieve special effects, such as decals, outlining, and constructive solid geometry rendering.</span></span>

<span data-ttu-id="df868-147">樣板測試會根據樣板緩衝區中的值與參考值之間的比較結果，有條件地消除圖元。</span><span class="sxs-lookup"><span data-stu-id="df868-147">The stencil test conditionally eliminates a pixel based on the outcome of a comparison between the value in the stencil buffer and a reference value.</span></span> <span data-ttu-id="df868-148">測試會以具有引數 GL 樣板測試的 [**glEnable**](glenable.md) 和 [**glDisable**](gldisable.md) 呼叫來啟用 \_ \_ ，並使用 [**glStencilFunc**](glstencilfunc.md)來控制。</span><span class="sxs-lookup"><span data-stu-id="df868-148">The test is enabled with [**glEnable**](glenable.md) and [**glDisable**](gldisable.md) calls with argument GL\_STENCIL\_TEST, and controlled with [**glStencilFunc**](glstencilfunc.md).</span></span>

<span data-ttu-id="df868-149">**GlStencilOp** 函式會採用三個引數，指出啟用 stenciling 時，儲存的樣板值會發生什麼事。</span><span class="sxs-lookup"><span data-stu-id="df868-149">The **glStencilOp** function takes three arguments that indicate what happens to the stored stencil value while stenciling is enabled.</span></span> <span data-ttu-id="df868-150">如果樣板測試失敗，則不會對圖元的色彩或深度緩衝區進行任何變更，而且 *會* 指定樣板緩衝區內容會發生什麼事。</span><span class="sxs-lookup"><span data-stu-id="df868-150">If the stencil test fails, no change is made to the pixel's color or depth buffers, and *fail* specifies what happens to the stencil buffer contents.</span></span>

<span data-ttu-id="df868-151">樣板緩衝區值會被視為不帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="df868-151">Stencil buffer values are treated as unsigned integers.</span></span> <span data-ttu-id="df868-152">遞增和遞減時，值會壓制為0和 2 *n* 1，其中 *n* 是查詢 GL 樣板位所傳回的值 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="df868-152">When incremented and decremented, values are clamped to 0 and 2 *n* 1, where *n* is the value returned by querying GL\_STENCIL\_BITS.</span></span>

<span data-ttu-id="df868-153">**GlStencilOp** 指定樣板緩衝區動作的其他兩個引數，應該 (*zpass*) 或 (*zfail*) 失敗，才能執行後續深度緩衝區測試。</span><span class="sxs-lookup"><span data-stu-id="df868-153">The other two arguments to **glStencilOp** specify stencil buffer actions should subsequent depth buffer tests succeed (*zpass*) or fail (*zfail*).</span></span> <span data-ttu-id="df868-154"> (請參閱 [**glDepthFunc**](gldepthfunc.md)。 ) 使用相同的六個符號常數來指定 *失敗*。</span><span class="sxs-lookup"><span data-stu-id="df868-154">(See [**glDepthFunc**](gldepthfunc.md).) They are specified using the same six symbolic constants as *fail*.</span></span> <span data-ttu-id="df868-155">請注意，當沒有深度緩衝區或未啟用深度緩衝區時，就會忽略 *zfail* 。</span><span class="sxs-lookup"><span data-stu-id="df868-155">Note that *zfail* is ignored when there is no depth buffer, or when the depth buffer is not enabled.</span></span> <span data-ttu-id="df868-156">在這些情況下，當樣板測試失敗並分別傳遞時，fail 和 *zpass* *會* 指定樣板動作。</span><span class="sxs-lookup"><span data-stu-id="df868-156">In these cases, *fail* and *zpass* specify stencil action when the stencil test fails and passes, respectively.</span></span>

<span data-ttu-id="df868-157">範本測試一開始會停用。</span><span class="sxs-lookup"><span data-stu-id="df868-157">Initially the stencil test is disabled.</span></span> <span data-ttu-id="df868-158">如果沒有任何樣板緩衝區，則不會發生任何樣板修改，也就像樣板測試一律通過，而不考慮任何 **glStencilOp** 呼叫。</span><span class="sxs-lookup"><span data-stu-id="df868-158">If there is no stencil buffer, no stencil modification can occur and it is as if the stencil tests always pass, regardless of any call to **glStencilOp**.</span></span>

<span data-ttu-id="df868-159">下列函式會取出與 **glStencilOp** 相關的資訊：</span><span class="sxs-lookup"><span data-stu-id="df868-159">The following functions retrieve information related to **glStencilOp**:</span></span>

<span data-ttu-id="df868-160">具有引數 GL 樣板的 [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) \_ \_ 失敗</span><span class="sxs-lookup"><span data-stu-id="df868-160">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_STENCIL\_FAIL</span></span>

<span data-ttu-id="df868-161">具有引數 GL \_ 樣板 \_ 通過 \_ 深度 \_ 傳遞的 glGet</span><span class="sxs-lookup"><span data-stu-id="df868-161">**glGet** with argument GL\_STENCIL\_PASS\_DEPTH\_PASS</span></span>

<span data-ttu-id="df868-162">具有引數 GL \_ 樣板 \_ 通過 \_ 深度 \_ 失敗的 glGet</span><span class="sxs-lookup"><span data-stu-id="df868-162">**glGet** with argument GL\_STENCIL\_PASS\_DEPTH\_FAIL</span></span>

<span data-ttu-id="df868-163">具有引數 GL \_ 樣板 \_ 位的 glGet</span><span class="sxs-lookup"><span data-stu-id="df868-163">**glGet** with argument GL\_STENCIL\_BITS</span></span>

<span data-ttu-id="df868-164">[](glisenabled.md)具有引數 GL \_ 樣板 \_ 測試的 glIsEnabled</span><span class="sxs-lookup"><span data-stu-id="df868-164">[**glIsEnabled**](glisenabled.md) with argument GL\_STENCIL\_TEST</span></span>

## <a name="requirements"></a><span data-ttu-id="df868-165">規格需求</span><span class="sxs-lookup"><span data-stu-id="df868-165">Requirements</span></span>



| <span data-ttu-id="df868-166">需求</span><span class="sxs-lookup"><span data-stu-id="df868-166">Requirement</span></span> | <span data-ttu-id="df868-167">值</span><span class="sxs-lookup"><span data-stu-id="df868-167">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="df868-168">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="df868-168">Minimum supported client</span></span><br/> | <span data-ttu-id="df868-169">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="df868-169">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="df868-170">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="df868-170">Minimum supported server</span></span><br/> | <span data-ttu-id="df868-171">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="df868-171">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="df868-172">標頭</span><span class="sxs-lookup"><span data-stu-id="df868-172">Header</span></span><br/>                   | <dl> <span data-ttu-id="df868-173"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="df868-173"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="df868-174">程式庫</span><span class="sxs-lookup"><span data-stu-id="df868-174">Library</span></span><br/>                  | <dl> <span data-ttu-id="df868-175"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="df868-175"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="df868-176">DLL</span><span class="sxs-lookup"><span data-stu-id="df868-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="df868-177"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="df868-177"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df868-178">另請參閱</span><span class="sxs-lookup"><span data-stu-id="df868-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df868-179">**glAlphaFunc**</span><span class="sxs-lookup"><span data-stu-id="df868-179">**glAlphaFunc**</span></span>](glalphafunc.md)
</dt> <dt>

[<span data-ttu-id="df868-180">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="df868-180">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="df868-181">**glBlendFunc**</span><span class="sxs-lookup"><span data-stu-id="df868-181">**glBlendFunc**</span></span>](glblendfunc.md)
</dt> <dt>

[<span data-ttu-id="df868-182">**glDepthFunc**</span><span class="sxs-lookup"><span data-stu-id="df868-182">**glDepthFunc**</span></span>](gldepthfunc.md)
</dt> <dt>

[<span data-ttu-id="df868-183">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="df868-183">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="df868-184">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="df868-184">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="df868-185">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="df868-185">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="df868-186">**glLogicOp**</span><span class="sxs-lookup"><span data-stu-id="df868-186">**glLogicOp**</span></span>](gllogicop.md)
</dt> <dt>

[<span data-ttu-id="df868-187">**glStencilFunc**</span><span class="sxs-lookup"><span data-stu-id="df868-187">**glStencilFunc**</span></span>](glstencilfunc.md)
</dt> </dl>

 

 





