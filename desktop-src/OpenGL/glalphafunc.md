---
title: 'glAlphaFunc 函式 (Gl) '
description: GlAlphaFunc 函式可讓您的應用程式設定 Alpha 測試函數。
ms.assetid: 6c0c06b5-1bad-4590-a262-f134f63f0936
keywords:
- glAlphaFunc 函式 OpenGL
topic_type:
- apiref
api_name:
- glAlphaFunc
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6cf96cfe2be0224c9c2e2409fc68805b530ae1f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968767"
---
# <a name="glalphafunc-function"></a><span data-ttu-id="42e17-104">glAlphaFunc 函式</span><span class="sxs-lookup"><span data-stu-id="42e17-104">glAlphaFunc function</span></span>

<span data-ttu-id="42e17-105">**GlAlphaFunc** 函式可讓您的應用程式設定 Alpha 測試函數。</span><span class="sxs-lookup"><span data-stu-id="42e17-105">The **glAlphaFunc** function enables your application to set the alpha test function.</span></span>

## <a name="syntax"></a><span data-ttu-id="42e17-106">語法</span><span class="sxs-lookup"><span data-stu-id="42e17-106">Syntax</span></span>


```C++
void WINAPI glAlphaFunc(
   GLenum   func,
   GLclampf ref
);
```



## <a name="parameters"></a><span data-ttu-id="42e17-107">參數</span><span class="sxs-lookup"><span data-stu-id="42e17-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42e17-108">*func*</span><span class="sxs-lookup"><span data-stu-id="42e17-108">*func*</span></span> 
</dt> <dd>

<span data-ttu-id="42e17-109">Alpha 比較函數。</span><span class="sxs-lookup"><span data-stu-id="42e17-109">The alpha comparison function.</span></span> <span data-ttu-id="42e17-110">以下是接受的符號常數及其意義。</span><span class="sxs-lookup"><span data-stu-id="42e17-110">The following are the accepted symbolic constants and their meanings.</span></span>



| <span data-ttu-id="42e17-111">值</span><span class="sxs-lookup"><span data-stu-id="42e17-111">Value</span></span>                                                                                                                                                   | <span data-ttu-id="42e17-112">意義</span><span class="sxs-lookup"><span data-stu-id="42e17-112">Meaning</span></span>                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="GL_NEVER"></span><span id="gl_never"></span><dl> <span data-ttu-id="42e17-113"><dt>**GL \_ 永不**</dt></span><span class="sxs-lookup"><span data-stu-id="42e17-113"><dt>**GL\_NEVER**</dt></span></span> </dl>          | <span data-ttu-id="42e17-114">永遠不會通過。</span><span class="sxs-lookup"><span data-stu-id="42e17-114">Never passes.</span></span><br/>                                                                       |
| <span id="GL_LESS"></span><span id="gl_less"></span><dl> <span data-ttu-id="42e17-115"><dt>**GL \_ LESS**</dt></span><span class="sxs-lookup"><span data-stu-id="42e17-115"><dt>**GL\_LESS**</dt></span></span> </dl>             | <span data-ttu-id="42e17-116">如果傳入的 Alpha 值小於參考值，則會傳遞。</span><span class="sxs-lookup"><span data-stu-id="42e17-116">Passes if the incoming alpha value is less than the reference value.</span></span><br/>                |
| <span id="GL_EQUAL"></span><span id="gl_equal"></span><dl> <span data-ttu-id="42e17-117"><dt>**GL \_ 相等**</dt></span><span class="sxs-lookup"><span data-stu-id="42e17-117"><dt>**GL\_EQUAL**</dt></span></span> </dl>          | <span data-ttu-id="42e17-118">如果傳入的 Alpha 值等於參考值，則會傳遞。</span><span class="sxs-lookup"><span data-stu-id="42e17-118">Passes if the incoming alpha value is equal to the reference value.</span></span><br/>                 |
| <span id="GL_LEQUAL"></span><span id="gl_lequal"></span><dl> <span data-ttu-id="42e17-119"><dt>**GL \_ LEQUAL**</dt></span><span class="sxs-lookup"><span data-stu-id="42e17-119"><dt>**GL\_LEQUAL**</dt></span></span> </dl>       | <span data-ttu-id="42e17-120">如果傳入的 Alpha 值小於或等於參考值，則會傳遞。</span><span class="sxs-lookup"><span data-stu-id="42e17-120">Passes if the incoming alpha value is less than or equal to the reference value.</span></span><br/>    |
| <span id="GL_GREATER"></span><span id="gl_greater"></span><dl> <span data-ttu-id="42e17-121"><dt>**GL \_ 更高**</dt></span><span class="sxs-lookup"><span data-stu-id="42e17-121"><dt>**GL\_GREATER**</dt></span></span> </dl>    | <span data-ttu-id="42e17-122">傳入的 Alpha 值是否大於參考值時傳遞。</span><span class="sxs-lookup"><span data-stu-id="42e17-122">Passes if the incoming alpha value is greater than the reference value.</span></span><br/>             |
| <span id="GL_NOTEQUAL"></span><span id="gl_notequal"></span><dl> <span data-ttu-id="42e17-123"><dt>**GL \_ NOTEQUAL**</dt></span><span class="sxs-lookup"><span data-stu-id="42e17-123"><dt>**GL\_NOTEQUAL**</dt></span></span> </dl> | <span data-ttu-id="42e17-124">如果傳入的 Alpha 值不等於參考值，則會傳遞。</span><span class="sxs-lookup"><span data-stu-id="42e17-124">Passes if the incoming alpha value is not equal to the reference value.</span></span><br/>             |
| <span id="GL_GEQUAL"></span><span id="gl_gequal"></span><dl> <span data-ttu-id="42e17-125"><dt>**GL \_ GEQUAL**</dt></span><span class="sxs-lookup"><span data-stu-id="42e17-125"><dt>**GL\_GEQUAL**</dt></span></span> </dl>       | <span data-ttu-id="42e17-126">如果傳入的 Alpha 值大於或等於參考值，則會傳遞。</span><span class="sxs-lookup"><span data-stu-id="42e17-126">Passes if the incoming alpha value is greater than or equal to the reference value.</span></span><br/> |
| <span id="GL_ALWAYS"></span><span id="gl_always"></span><dl> <span data-ttu-id="42e17-127"><dt>**GL \_ 一律**</dt></span><span class="sxs-lookup"><span data-stu-id="42e17-127"><dt>**GL\_ALWAYS**</dt></span></span> </dl>       | <span data-ttu-id="42e17-128">一律傳遞。</span><span class="sxs-lookup"><span data-stu-id="42e17-128">Always passes.</span></span> <span data-ttu-id="42e17-129">此為預設值。</span><span class="sxs-lookup"><span data-stu-id="42e17-129">This is the default.</span></span><br/>                                                 |



 

</dd> <dt>

<span data-ttu-id="42e17-130">*ref*</span><span class="sxs-lookup"><span data-stu-id="42e17-130">*ref*</span></span> 
</dt> <dd>

<span data-ttu-id="42e17-131">要比較傳入 Alpha 值的參考值。</span><span class="sxs-lookup"><span data-stu-id="42e17-131">The reference value to which incoming alpha values are compared.</span></span> <span data-ttu-id="42e17-132">此值會壓制至範圍0到1，其中0代表可能的最小 Alpha 值和1個最高的可能值。</span><span class="sxs-lookup"><span data-stu-id="42e17-132">This value is clamped to the range 0 through 1, where 0 represents the lowest possible alpha value and 1 the highest possible value.</span></span> <span data-ttu-id="42e17-133">預設參考為0。</span><span class="sxs-lookup"><span data-stu-id="42e17-133">The default reference is 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42e17-134">傳回值</span><span class="sxs-lookup"><span data-stu-id="42e17-134">Return value</span></span>

<span data-ttu-id="42e17-135">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="42e17-135">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="42e17-136">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="42e17-136">Error codes</span></span>

<span data-ttu-id="42e17-137">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="42e17-137">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="42e17-138">Name</span><span class="sxs-lookup"><span data-stu-id="42e17-138">Name</span></span>                                                                                                  | <span data-ttu-id="42e17-139">意義</span><span class="sxs-lookup"><span data-stu-id="42e17-139">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="42e17-140"><dt>**GL \_ 無效 \_ 列舉**</dt></span><span class="sxs-lookup"><span data-stu-id="42e17-140"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="42e17-141">*func* 不是可接受的值。</span><span class="sxs-lookup"><span data-stu-id="42e17-141">*func* was not an accepted value.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="42e17-142"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="42e17-142"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="42e17-143">呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。</span><span class="sxs-lookup"><span data-stu-id="42e17-143">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="42e17-144">備註</span><span class="sxs-lookup"><span data-stu-id="42e17-144">Remarks</span></span>

<span data-ttu-id="42e17-145">Alpha 測試會根據傳入片段的 Alpha 值與常數參考值之間的比較結果，來捨棄片段。</span><span class="sxs-lookup"><span data-stu-id="42e17-145">The alpha test discards fragments depending on the outcome of a comparison between the incoming fragments' alpha values and a constant reference value.</span></span> <span data-ttu-id="42e17-146">**GlAlphaFunc** 函數會指定參考和比較函數。</span><span class="sxs-lookup"><span data-stu-id="42e17-146">The **glAlphaFunc** function specifies the reference and comparison function.</span></span> <span data-ttu-id="42e17-147">只有在啟用 Alpha 測試時，才會執行比較。</span><span class="sxs-lookup"><span data-stu-id="42e17-147">The comparison is performed only if alpha testing is enabled.</span></span> <span data-ttu-id="42e17-148"> (如需有關 GL ALPHA 測試的詳細資訊 \_ \_ ，請參閱 [**glEnable**](glenable.md)。 ) </span><span class="sxs-lookup"><span data-stu-id="42e17-148">(For more information on GL\_ALPHA\_TEST, see [**glEnable**](glenable.md).)</span></span>

<span data-ttu-id="42e17-149">*Func* 和 *ref* 參數指定圖元繪製時所依據的條件。</span><span class="sxs-lookup"><span data-stu-id="42e17-149">The *func* and *ref* parameters specify the conditions under which the pixel is drawn.</span></span> <span data-ttu-id="42e17-150">使用 *func* 指定的函式，將連入的 Alpha 值與 *ref* 進行比較。</span><span class="sxs-lookup"><span data-stu-id="42e17-150">The incoming alpha value is compared to *ref* using the function specified by *func*.</span></span> <span data-ttu-id="42e17-151">如果比較通過，則會繪製內送片段、後續樣板和深度緩衝區測試的條件。</span><span class="sxs-lookup"><span data-stu-id="42e17-151">If the comparison passes, the incoming fragment is drawn, conditional on subsequent stencil and depth-buffer tests.</span></span> <span data-ttu-id="42e17-152">如果比較失敗，則不會在該圖元位置對畫面格緩衝區進行任何變更。</span><span class="sxs-lookup"><span data-stu-id="42e17-152">If the comparison fails, no change is made to the framebuffer at that pixel location.</span></span>

<span data-ttu-id="42e17-153">**GlAlphaFunc** 函式會在所有圖元寫入上運作，包括從點、線條、多邊形和點陣圖的掃描轉換產生的結果，以及從圖元繪製和複製作業產生的結果。</span><span class="sxs-lookup"><span data-stu-id="42e17-153">The **glAlphaFunc** function operates on all pixel writes, including those resulting from the scan conversion of points, lines, polygons, and bitmaps, and from pixel draw and copy operations.</span></span> <span data-ttu-id="42e17-154">**GlAlphaFunc** 函數不會影響螢幕清除作業。</span><span class="sxs-lookup"><span data-stu-id="42e17-154">The **glAlphaFunc** function does not affect screen clear operations.</span></span>

<span data-ttu-id="42e17-155">Alpha 測試只會在 RGBA 模式中完成。</span><span class="sxs-lookup"><span data-stu-id="42e17-155">Alpha testing is done only in RGBA mode.</span></span>

<span data-ttu-id="42e17-156">下列函式會取出與 **glAlphaFunc** 函數相關的資訊：</span><span class="sxs-lookup"><span data-stu-id="42e17-156">The following functions retrieve information related to the **glAlphaFunc** function:</span></span>

<span data-ttu-id="42e17-157">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ ALPHA \_ TEST \_ FUNC 的 glGet</span><span class="sxs-lookup"><span data-stu-id="42e17-157">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_ALPHA\_TEST\_FUNC</span></span>

<span data-ttu-id="42e17-158">具有引數 GL \_ ALPHA \_ TEST \_ REF 的 glGet</span><span class="sxs-lookup"><span data-stu-id="42e17-158">**glGet** with argument GL\_ALPHA\_TEST\_REF</span></span>

<span data-ttu-id="42e17-159">[](glisenabled.md)具有引數 GL \_ ALPHA \_ 測試的 glIsEnabled</span><span class="sxs-lookup"><span data-stu-id="42e17-159">[**glIsEnabled**](glisenabled.md) with argument GL\_ALPHA\_TEST</span></span>

## <a name="requirements"></a><span data-ttu-id="42e17-160">規格需求</span><span class="sxs-lookup"><span data-stu-id="42e17-160">Requirements</span></span>



| <span data-ttu-id="42e17-161">需求</span><span class="sxs-lookup"><span data-stu-id="42e17-161">Requirement</span></span> | <span data-ttu-id="42e17-162">值</span><span class="sxs-lookup"><span data-stu-id="42e17-162">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="42e17-163">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="42e17-163">Minimum supported client</span></span><br/> | <span data-ttu-id="42e17-164">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="42e17-164">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="42e17-165">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="42e17-165">Minimum supported server</span></span><br/> | <span data-ttu-id="42e17-166">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="42e17-166">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="42e17-167">標頭</span><span class="sxs-lookup"><span data-stu-id="42e17-167">Header</span></span><br/>                   | <dl> <span data-ttu-id="42e17-168"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="42e17-168"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="42e17-169">程式庫</span><span class="sxs-lookup"><span data-stu-id="42e17-169">Library</span></span><br/>                  | <dl> <span data-ttu-id="42e17-170"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="42e17-170"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="42e17-171">DLL</span><span class="sxs-lookup"><span data-stu-id="42e17-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="42e17-172"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="42e17-172"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42e17-173">另請參閱</span><span class="sxs-lookup"><span data-stu-id="42e17-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42e17-174">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="42e17-174">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="42e17-175">**glBlendFunc**</span><span class="sxs-lookup"><span data-stu-id="42e17-175">**glBlendFunc**</span></span>](glblendfunc.md)
</dt> <dt>

[<span data-ttu-id="42e17-176">**glClear**</span><span class="sxs-lookup"><span data-stu-id="42e17-176">**glClear**</span></span>](glclear.md)
</dt> <dt>

[<span data-ttu-id="42e17-177">**glDepthFunc**</span><span class="sxs-lookup"><span data-stu-id="42e17-177">**glDepthFunc**</span></span>](gldepthfunc.md)
</dt> <dt>

[<span data-ttu-id="42e17-178">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="42e17-178">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="42e17-179">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="42e17-179">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="42e17-180">**glGet**</span><span class="sxs-lookup"><span data-stu-id="42e17-180">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="42e17-181">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="42e17-181">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="42e17-182">**glStencilFunc**</span><span class="sxs-lookup"><span data-stu-id="42e17-182">**glStencilFunc**</span></span>](glstencilfunc.md)
</dt> </dl>

 

 





