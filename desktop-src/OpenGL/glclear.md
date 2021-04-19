---
title: 'glClear 函式 (Gl) '
description: GlClear 函式會清除緩衝區來設定預設值。
ms.assetid: 9818f969-3145-45ea-aa9c-2abed953a8e0
keywords:
- glClear 函式 OpenGL
topic_type:
- apiref
api_name:
- glClear
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0db935e46c65c42976024a8afbb98028294710c7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968355"
---
# <a name="glclear-function"></a><span data-ttu-id="06367-104">glClear 函式</span><span class="sxs-lookup"><span data-stu-id="06367-104">glClear function</span></span>

<span data-ttu-id="06367-105">**GlClear** 函式會清除緩衝區來設定預設值。</span><span class="sxs-lookup"><span data-stu-id="06367-105">The **glClear** function clears buffers to preset values.</span></span>

## <a name="syntax"></a><span data-ttu-id="06367-106">語法</span><span class="sxs-lookup"><span data-stu-id="06367-106">Syntax</span></span>


```C++
void WINAPI glClear(
   GLbitfield mask
);
```



## <a name="parameters"></a><span data-ttu-id="06367-107">參數</span><span class="sxs-lookup"><span data-stu-id="06367-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06367-108">*面具*</span><span class="sxs-lookup"><span data-stu-id="06367-108">*mask*</span></span> 
</dt> <dd>

<span data-ttu-id="06367-109">遮罩的位 OR 運算子，表示要清除的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="06367-109">Bitwise OR operators of masks that indicate the buffers to be cleared.</span></span> <span data-ttu-id="06367-110">四個遮罩如下所示。</span><span class="sxs-lookup"><span data-stu-id="06367-110">The four masks are as follows.</span></span>



| <span data-ttu-id="06367-111">值</span><span class="sxs-lookup"><span data-stu-id="06367-111">Value</span></span>                                                                                                                                                                                   | <span data-ttu-id="06367-112">意義</span><span class="sxs-lookup"><span data-stu-id="06367-112">Meaning</span></span>                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <span id="GL_COLOR_BUFFER_BIT"></span><span id="gl_color_buffer_bit"></span><dl> <span data-ttu-id="06367-113"><dt>**GL \_ 色彩 \_ 緩衝區 \_ 位**</dt></span><span class="sxs-lookup"><span data-stu-id="06367-113"><dt>**GL\_COLOR\_BUFFER\_BIT**</dt></span></span> </dl>       | <span data-ttu-id="06367-114">目前已啟用色彩寫入的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="06367-114">The buffers currently enabled for color writing.</span></span><br/> |
| <span id="GL_DEPTH_BUFFER_BIT"></span><span id="gl_depth_buffer_bit"></span><dl> <span data-ttu-id="06367-115"><dt>**GL \_ 深度 \_ 緩衝區 \_ 位**</dt></span><span class="sxs-lookup"><span data-stu-id="06367-115"><dt>**GL\_DEPTH\_BUFFER\_BIT**</dt></span></span> </dl>       | <span data-ttu-id="06367-116">深度緩衝區。</span><span class="sxs-lookup"><span data-stu-id="06367-116">The depth buffer.</span></span><br/>                                |
| <span id="GL_ACCUM_BUFFER_BIT"></span><span id="gl_accum_buffer_bit"></span><dl> <span data-ttu-id="06367-117"><dt>**GL \_ ACCUM \_ 緩衝區 \_ 位**</dt></span><span class="sxs-lookup"><span data-stu-id="06367-117"><dt>**GL\_ACCUM\_BUFFER\_BIT**</dt></span></span> </dl>       | <span data-ttu-id="06367-118">累積緩衝區。</span><span class="sxs-lookup"><span data-stu-id="06367-118">The accumulation buffer.</span></span><br/>                         |
| <span id="GL_STENCIL_BUFFER_BIT"></span><span id="gl_stencil_buffer_bit"></span><dl> <span data-ttu-id="06367-119"><dt>**GL \_ 樣板 \_ 緩衝區 \_ 位**</dt></span><span class="sxs-lookup"><span data-stu-id="06367-119"><dt>**GL\_STENCIL\_BUFFER\_BIT**</dt></span></span> </dl> | <span data-ttu-id="06367-120">樣板緩衝區。</span><span class="sxs-lookup"><span data-stu-id="06367-120">The stencil buffer.</span></span><br/>                              |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06367-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="06367-121">Return value</span></span>

<span data-ttu-id="06367-122">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="06367-122">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="06367-123">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="06367-123">Error codes</span></span>

<span data-ttu-id="06367-124">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="06367-124">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="06367-125">Name</span><span class="sxs-lookup"><span data-stu-id="06367-125">Name</span></span>                                                                                                  | <span data-ttu-id="06367-126">意義</span><span class="sxs-lookup"><span data-stu-id="06367-126">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="06367-127"><dt>**GL \_ 無效 \_ 值**</dt></span><span class="sxs-lookup"><span data-stu-id="06367-127"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="06367-128">在 *遮罩* 中設定四個定義位以外的任何位。</span><span class="sxs-lookup"><span data-stu-id="06367-128">Any bit other than the four defined bits was set in *mask*.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="06367-129"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="06367-129"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="06367-130">呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。</span><span class="sxs-lookup"><span data-stu-id="06367-130">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="06367-131">備註</span><span class="sxs-lookup"><span data-stu-id="06367-131">Remarks</span></span>

<span data-ttu-id="06367-132">**GlClear** 函式會將視窗的 bitplane 區域設定為先前由 [**glClearColor**](glclearcolor.md)、 [**glClearIndex**](glclearindex.md)、 [**glClearDepth**](glcleardepth.md)、 [**glClearStencil**](glclearstencil.md)和 [**glClearAccum**](glclearaccum.md)所選取的值。</span><span class="sxs-lookup"><span data-stu-id="06367-132">The **glClear** function sets the bitplane area of the window to values previously selected by [**glClearColor**](glclearcolor.md), [**glClearIndex**](glclearindex.md), [**glClearDepth**](glcleardepth.md), [**glClearStencil**](glclearstencil.md), and [**glClearAccum**](glclearaccum.md).</span></span> <span data-ttu-id="06367-133">您可以使用 [**glDrawBuffer**](gldrawbuffer.md)一次選取一個以上的緩衝區，以同時清除多個色彩緩衝區。</span><span class="sxs-lookup"><span data-stu-id="06367-133">You can clear multiple color buffers simultaneously by selecting more than one buffer at a time using [**glDrawBuffer**](gldrawbuffer.md).</span></span>

<span data-ttu-id="06367-134">圖元擁有權測試、剪下測試、遞色和緩衝區 writemasks 都會影響 **glClear** 的作業。</span><span class="sxs-lookup"><span data-stu-id="06367-134">The pixel-ownership test, the scissor test, dithering, and the buffer writemasks affect the operation of **glClear**.</span></span> <span data-ttu-id="06367-135">剪式方塊會將已清除的區域界限。</span><span class="sxs-lookup"><span data-stu-id="06367-135">The scissor box bounds the cleared region.</span></span> <span data-ttu-id="06367-136">**GlClear** 函式會忽略 Alpha 函數、blend 函式、邏輯運算、stenciling、材質對應和 *z* 緩衝。</span><span class="sxs-lookup"><span data-stu-id="06367-136">The **glClear** function ignores the alpha function, blend function, logical operation, stenciling, texture mapping, and *z*-buffering.</span></span>

<span data-ttu-id="06367-137">**GlClear** 函式會採用單一引數 (*mask*) 這是數個值的位 or，表示要清除的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="06367-137">The **glClear** function takes a single argument (*mask*) that is the bitwise OR of several values indicating which buffer is to be cleared.</span></span>

<span data-ttu-id="06367-138">每個緩衝區清除的值取決於該緩衝區的清除值設定。</span><span class="sxs-lookup"><span data-stu-id="06367-138">The value to which each buffer is cleared depends on the setting of the clear value for that buffer.</span></span>

<span data-ttu-id="06367-139">如果緩衝區不存在，則在該緩衝區導向的 **glClear** 呼叫不會有任何作用。</span><span class="sxs-lookup"><span data-stu-id="06367-139">If a buffer is not present, a **glClear** call directed at that buffer has no effect.</span></span>

<span data-ttu-id="06367-140">下列函式會取出與 **glClear** 相關的資訊：</span><span class="sxs-lookup"><span data-stu-id="06367-140">The following functions retrieve information related to **glClear**:</span></span>

<span data-ttu-id="06367-141">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) 與引數 GL \_ ACCUM \_ CLEAR \_ 值</span><span class="sxs-lookup"><span data-stu-id="06367-141">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_ACCUM\_CLEAR\_VALUE</span></span>

<span data-ttu-id="06367-142">具有引數 GL \_ 深度 \_ 清除 \_ 值的 glGet</span><span class="sxs-lookup"><span data-stu-id="06367-142">**glGet** with argument GL\_DEPTH\_CLEAR\_VALUE</span></span>

<span data-ttu-id="06367-143">具有引數 GL \_ 索引 \_ 清除 \_ 值的 glGet</span><span class="sxs-lookup"><span data-stu-id="06367-143">**glGet** with argument GL\_INDEX\_CLEAR\_VALUE</span></span>

<span data-ttu-id="06367-144">具有引數 GL \_ 色彩 \_ 清除 \_ 值的 glGet</span><span class="sxs-lookup"><span data-stu-id="06367-144">**glGet** with argument GL\_COLOR\_CLEAR\_VALUE</span></span>

<span data-ttu-id="06367-145">具有引數 GL \_ 樣板 \_ CLEAR \_ 值的 glGet</span><span class="sxs-lookup"><span data-stu-id="06367-145">**glGet** with argument GL\_STENCIL\_CLEAR\_VALUE</span></span>

## <a name="requirements"></a><span data-ttu-id="06367-146">規格需求</span><span class="sxs-lookup"><span data-stu-id="06367-146">Requirements</span></span>



| <span data-ttu-id="06367-147">需求</span><span class="sxs-lookup"><span data-stu-id="06367-147">Requirement</span></span> | <span data-ttu-id="06367-148">值</span><span class="sxs-lookup"><span data-stu-id="06367-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="06367-149">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="06367-149">Minimum supported client</span></span><br/> | <span data-ttu-id="06367-150">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="06367-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="06367-151">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="06367-151">Minimum supported server</span></span><br/> | <span data-ttu-id="06367-152">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="06367-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="06367-153">標頭</span><span class="sxs-lookup"><span data-stu-id="06367-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="06367-154"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="06367-154"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="06367-155">程式庫</span><span class="sxs-lookup"><span data-stu-id="06367-155">Library</span></span><br/>                  | <dl> <span data-ttu-id="06367-156"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="06367-156"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="06367-157">DLL</span><span class="sxs-lookup"><span data-stu-id="06367-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="06367-158"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="06367-158"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06367-159">另請參閱</span><span class="sxs-lookup"><span data-stu-id="06367-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06367-160">**glClearAccum**</span><span class="sxs-lookup"><span data-stu-id="06367-160">**glClearAccum**</span></span>](glclearaccum.md)
</dt> <dt>

[<span data-ttu-id="06367-161">**glClearColor**</span><span class="sxs-lookup"><span data-stu-id="06367-161">**glClearColor**</span></span>](glclearcolor.md)
</dt> <dt>

[<span data-ttu-id="06367-162">**glClearDepth**</span><span class="sxs-lookup"><span data-stu-id="06367-162">**glClearDepth**</span></span>](glcleardepth.md)
</dt> <dt>

[<span data-ttu-id="06367-163">**glClearIndex**</span><span class="sxs-lookup"><span data-stu-id="06367-163">**glClearIndex**</span></span>](glclearindex.md)
</dt> <dt>

[<span data-ttu-id="06367-164">**glClearStencil**</span><span class="sxs-lookup"><span data-stu-id="06367-164">**glClearStencil**</span></span>](glclearstencil.md)
</dt> <dt>

[<span data-ttu-id="06367-165">**glDrawBuffer**</span><span class="sxs-lookup"><span data-stu-id="06367-165">**glDrawBuffer**</span></span>](gldrawbuffer.md)
</dt> <dt>

[<span data-ttu-id="06367-166">**glGet**</span><span class="sxs-lookup"><span data-stu-id="06367-166">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="06367-167">**glScissor**</span><span class="sxs-lookup"><span data-stu-id="06367-167">**glScissor**</span></span>](glscissor.md)
</dt> </dl>

 

 





