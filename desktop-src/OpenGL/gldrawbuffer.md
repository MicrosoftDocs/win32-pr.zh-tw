---
title: 'glDrawBuffer 函式 (Gl) '
description: GlDrawBuffer 函式會指定要繪製的色彩緩衝區。
ms.assetid: ea625699-303b-4e60-b9aa-771949a8d52d
keywords:
- glDrawBuffer 函式 OpenGL
topic_type:
- apiref
api_name:
- glDrawBuffer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a99bd2b184766f1621d89b2c8d642902d300e14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968337"
---
# <a name="gldrawbuffer-function"></a><span data-ttu-id="79f8f-104">glDrawBuffer 函式</span><span class="sxs-lookup"><span data-stu-id="79f8f-104">glDrawBuffer function</span></span>

<span data-ttu-id="79f8f-105">**GlDrawBuffer** 函式會指定要繪製的色彩緩衝區。</span><span class="sxs-lookup"><span data-stu-id="79f8f-105">The **glDrawBuffer** function specifies which color buffers are to be drawn into.</span></span>

## <a name="syntax"></a><span data-ttu-id="79f8f-106">語法</span><span class="sxs-lookup"><span data-stu-id="79f8f-106">Syntax</span></span>


```C++
void WINAPI glDrawBuffer(
   GLenum mode
);
```



## <a name="parameters"></a><span data-ttu-id="79f8f-107">參數</span><span class="sxs-lookup"><span data-stu-id="79f8f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79f8f-108">*mode*</span><span class="sxs-lookup"><span data-stu-id="79f8f-108">*mode*</span></span> 
</dt> <dd>

<span data-ttu-id="79f8f-109">使用下列可接受的符號常數，指定要繪製的最多四個色彩緩衝區。</span><span class="sxs-lookup"><span data-stu-id="79f8f-109">Specifies up to four color buffers to be drawn into with the following acceptable symbolic constants.</span></span>



| <span data-ttu-id="79f8f-110">值</span><span class="sxs-lookup"><span data-stu-id="79f8f-110">Value</span></span>                                                                                                                                                                       | <span data-ttu-id="79f8f-111">意義</span><span class="sxs-lookup"><span data-stu-id="79f8f-111">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_NONE"></span><span id="gl_none"></span><dl> <span data-ttu-id="79f8f-112"><dt>**GL \_ 無**</dt></span><span class="sxs-lookup"><span data-stu-id="79f8f-112"><dt>**GL\_NONE**</dt></span></span> </dl>                                 | <span data-ttu-id="79f8f-113">不會寫入任何色彩緩衝區。</span><span class="sxs-lookup"><span data-stu-id="79f8f-113">No color buffers are written.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="GL_FRONT_LEFT"></span><span id="gl_front_left"></span><dl> <span data-ttu-id="79f8f-114"><dt>**GL \_ FRONT \_ 左方**</dt></span><span class="sxs-lookup"><span data-stu-id="79f8f-114"><dt>**GL\_FRONT\_LEFT**</dt></span></span> </dl>              | <span data-ttu-id="79f8f-115">只會寫入 front 左色緩衝區。</span><span class="sxs-lookup"><span data-stu-id="79f8f-115">Only the front-left color buffer is written.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                      |
| <span id="GL_FRONT_RIGHT"></span><span id="gl_front_right"></span><dl> <span data-ttu-id="79f8f-116"><dt>**GL \_ 正面 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="79f8f-116"><dt>**GL\_FRONT\_RIGHT**</dt></span></span> </dl>           | <span data-ttu-id="79f8f-117">只會寫入右上方的色彩緩衝區。</span><span class="sxs-lookup"><span data-stu-id="79f8f-117">Only the front-right color buffer is written.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                     |
| <span id="GL_BACK_LEFT"></span><span id="gl_back_left"></span><dl> <span data-ttu-id="79f8f-118"><dt>**GL \_ 向 \_ 左復原**</dt></span><span class="sxs-lookup"><span data-stu-id="79f8f-118"><dt>**GL\_BACK\_LEFT**</dt></span></span> </dl>                 | <span data-ttu-id="79f8f-119">只會寫入向左色彩緩衝區。</span><span class="sxs-lookup"><span data-stu-id="79f8f-119">Only the back-left color buffer is written.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                       |
| <span id="GL_BACK_RIGHT"></span><span id="gl_back_right"></span><dl> <span data-ttu-id="79f8f-120"><dt>**GL \_ 向 \_ 右**</dt></span><span class="sxs-lookup"><span data-stu-id="79f8f-120"><dt>**GL\_BACK\_RIGHT**</dt></span></span> </dl>              | <span data-ttu-id="79f8f-121">只會寫入向右色彩緩衝區。</span><span class="sxs-lookup"><span data-stu-id="79f8f-121">Only the back-right color buffer is written.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                      |
| <span id="GL_FRONT"></span><span id="gl_front"></span><dl> <span data-ttu-id="79f8f-122"><dt>**GL \_ FRONT**</dt></span><span class="sxs-lookup"><span data-stu-id="79f8f-122"><dt>**GL\_FRONT**</dt></span></span> </dl>                              | <span data-ttu-id="79f8f-123">只會寫入左上角和右上角的色彩緩衝區。</span><span class="sxs-lookup"><span data-stu-id="79f8f-123">Only the front-left and front-right color buffers are written.</span></span> <span data-ttu-id="79f8f-124">如果沒有右邊的色彩緩衝區，則只會寫入 front 左色緩衝區。</span><span class="sxs-lookup"><span data-stu-id="79f8f-124">If there is no front-right color buffer, only the front left-color buffer is written.</span></span><br/>                                                                                                                                                                                                                                              |
| <span id="GL_BACK"></span><span id="gl_back"></span><dl> <span data-ttu-id="79f8f-125"><dt>**GL \_ 回**</dt></span><span class="sxs-lookup"><span data-stu-id="79f8f-125"><dt>**GL\_BACK**</dt></span></span> </dl>                                 | <span data-ttu-id="79f8f-126">只會寫入向左和向右色彩緩衝區。</span><span class="sxs-lookup"><span data-stu-id="79f8f-126">Only the back-left and back-right color buffers are written.</span></span> <span data-ttu-id="79f8f-127">如果沒有右邊的色彩緩衝區，則只會寫入向左色彩緩衝區。</span><span class="sxs-lookup"><span data-stu-id="79f8f-127">If there is no back-right color buffer, only the back-left color buffer is written.</span></span><br/>                                                                                                                                                                                                                                                  |
| <span id="GL_LEFT"></span><span id="gl_left"></span><dl> <span data-ttu-id="79f8f-128"><dt>**GL \_ 剩餘**</dt></span><span class="sxs-lookup"><span data-stu-id="79f8f-128"><dt>**GL\_LEFT**</dt></span></span> </dl>                                 | <span data-ttu-id="79f8f-129">只會寫入左上角和左邊的色彩緩衝區。</span><span class="sxs-lookup"><span data-stu-id="79f8f-129">Only the front-left and back-left color buffers are written.</span></span> <span data-ttu-id="79f8f-130">如果沒有上一頁的色彩緩衝區，則只會寫入左上角的色彩緩衝區。</span><span class="sxs-lookup"><span data-stu-id="79f8f-130">If there is no back-left color buffer, only the front-left color buffer is written.</span></span><br/>                                                                                                                                                                                                                                                  |
| <span id="GL_RIGHT"></span><span id="gl_right"></span><dl> <span data-ttu-id="79f8f-131"><dt>**GL \_ 右邊**</dt></span><span class="sxs-lookup"><span data-stu-id="79f8f-131"><dt>**GL\_RIGHT**</dt></span></span> </dl>                              | <span data-ttu-id="79f8f-132">只會寫入左右和右邊的色彩緩衝區。</span><span class="sxs-lookup"><span data-stu-id="79f8f-132">Only the front-right and back-right color buffers are written.</span></span> <span data-ttu-id="79f8f-133">如果沒有右邊的色彩緩衝區，則只會寫入右上方的色彩緩衝區。</span><span class="sxs-lookup"><span data-stu-id="79f8f-133">If there is no back-right color buffer, only the front-right color buffer is written.</span></span><br/>                                                                                                                                                                                                                                              |
| <span id="GL_FRONT_AND_BACK"></span><span id="gl_front_and_back"></span><dl> <span data-ttu-id="79f8f-134"><dt>**GL \_ 正面 \_ 和 \_ 背面**</dt></span><span class="sxs-lookup"><span data-stu-id="79f8f-134"><dt>**GL\_FRONT\_AND\_BACK**</dt></span></span> </dl> | <span data-ttu-id="79f8f-135">所有前端和背景色彩緩衝區都 (由左上角、右上角、左上角、右) 書寫。</span><span class="sxs-lookup"><span data-stu-id="79f8f-135">All the front and back color buffers (front-left, front-right, back-left, back-right) are written.</span></span> <span data-ttu-id="79f8f-136">如果沒有背面的色彩緩衝區，則只會寫入左上角和右上角的色彩緩衝區。</span><span class="sxs-lookup"><span data-stu-id="79f8f-136">If there are no back color buffers, only the front-left and front-right color buffers are written.</span></span> <span data-ttu-id="79f8f-137">如果沒有正確的色彩緩衝區，則只會寫入左上角和左邊的色彩緩衝區。</span><span class="sxs-lookup"><span data-stu-id="79f8f-137">If there are no right color buffers, only the front-left and back-left color buffers are written.</span></span> <span data-ttu-id="79f8f-138">如果沒有右邊或背面的色彩緩衝區，則只會寫入左上角的色彩緩衝區。</span><span class="sxs-lookup"><span data-stu-id="79f8f-138">If there are no right or back color buffers, only the front-left color buffer is written.</span></span><br/> |
| <span id="GL_AUXi"></span><span id="gl_auxi"></span><span id="GL_AUXI"></span><dl> <span data-ttu-id="79f8f-139"><dt>**GL \_ AUXi**</dt></span><span class="sxs-lookup"><span data-stu-id="79f8f-139"><dt>**GL\_AUXi**</dt></span></span> </dl>       | <span data-ttu-id="79f8f-140">只寫入輔助 *顏色緩衝區，\*\*i* 介於0和 GL \_ AUX \_ 的緩衝區-1 之間。</span><span class="sxs-lookup"><span data-stu-id="79f8f-140">Only the auxiliary color buffer *i* is written; *i* is between 0 and GL\_AUX\_BUFFERS - 1.</span></span> <span data-ttu-id="79f8f-141"> (GL \_ AUX \_ 緩衝區不是上限; 請使用 [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) 來查詢可用輔助緩衝區的數目。 ) </span><span class="sxs-lookup"><span data-stu-id="79f8f-141">(GL\_AUX\_BUFFERS is not the upper limit; use [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) to query the number of available auxiliary buffers.)</span></span><br/>                                                                                                                            |



 

<span data-ttu-id="79f8f-142">預設值為單一緩衝內容的 GL \_ 前端，而 \_ 針對雙重緩衝的內容則會傳回 gl。</span><span class="sxs-lookup"><span data-stu-id="79f8f-142">The default value is GL\_FRONT for single-buffered contexts, and GL\_BACK for double-buffered contexts.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79f8f-143">傳回值</span><span class="sxs-lookup"><span data-stu-id="79f8f-143">Return value</span></span>

<span data-ttu-id="79f8f-144">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="79f8f-144">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="79f8f-145">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="79f8f-145">Error codes</span></span>

<span data-ttu-id="79f8f-146">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="79f8f-146">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="79f8f-147">Name</span><span class="sxs-lookup"><span data-stu-id="79f8f-147">Name</span></span>                                                                                                  | <span data-ttu-id="79f8f-148">意義</span><span class="sxs-lookup"><span data-stu-id="79f8f-148">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="79f8f-149"><dt>**GL \_ 無效 \_ 列舉**</dt></span><span class="sxs-lookup"><span data-stu-id="79f8f-149"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="79f8f-150">*模式* 不是可接受的值。</span><span class="sxs-lookup"><span data-stu-id="79f8f-150">*mode* was not an accepted value.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="79f8f-151"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="79f8f-151"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="79f8f-152">*模式* 所指出的緩衝區都不存在。</span><span class="sxs-lookup"><span data-stu-id="79f8f-152">None of the buffers indicated by *mode* existed.</span></span><br/>                                                                           |
| <dl> <span data-ttu-id="79f8f-153"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="79f8f-153"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="79f8f-154">呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。</span><span class="sxs-lookup"><span data-stu-id="79f8f-154">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |


## <a name="remarks"></a><span data-ttu-id="79f8f-155">備註</span><span class="sxs-lookup"><span data-stu-id="79f8f-155">Remarks</span></span>

<span data-ttu-id="79f8f-156">當色彩寫入至畫面格緩衝區時，會將其寫入至 **glDrawBuffer** 所指定的色彩緩衝區。</span><span class="sxs-lookup"><span data-stu-id="79f8f-156">When colors are written to the framebuffer, they are written into the color buffers specified by **glDrawBuffer**.</span></span>

<span data-ttu-id="79f8f-157">如果選取了一個以上的色彩緩衝區來進行繪製，則會針對每個顏色緩衝區個別計算並套用混合或邏輯運算，而且可能會在每個緩衝區中產生不同的結果。</span><span class="sxs-lookup"><span data-stu-id="79f8f-157">If more than one color buffer is selected for drawing, then blending or logical operations are computed and applied independently for each color buffer and can produce different results in each buffer.</span></span>

<span data-ttu-id="79f8f-158">Monoscopic 內容只會包含左邊的緩衝區，而 stereoscopic 內容則包含左邊和右邊的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="79f8f-158">Monoscopic contexts include only left buffers, and stereoscopic contexts include both left and right buffers.</span></span> <span data-ttu-id="79f8f-159">同樣地，單一緩衝的內容只會包含前端緩衝區，而雙重緩衝的內容則包含前端和後端緩衝區。</span><span class="sxs-lookup"><span data-stu-id="79f8f-159">Likewise, single-buffered contexts include only front buffers, and double-buffered contexts include both front and back buffers.</span></span> <span data-ttu-id="79f8f-160">內容會在 OpenGL 初始化時選取。</span><span class="sxs-lookup"><span data-stu-id="79f8f-160">The context is selected at OpenGL initialization.</span></span>

<span data-ttu-id="79f8f-161">這一律是 GL \_ AUX *i* = gl \_ AUX0 + *i*。</span><span class="sxs-lookup"><span data-stu-id="79f8f-161">It is always the case that GL\_AUX *i* = GL\_AUX0 + *i*.</span></span>

<span data-ttu-id="79f8f-162">下列函式會取出與 **glDrawBuffer** 函數相關的資訊：</span><span class="sxs-lookup"><span data-stu-id="79f8f-162">The following functions retrieve information related to the **glDrawBuffer** function:</span></span>

<span data-ttu-id="79f8f-163">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) 與引數 GL \_ 繪圖 \_ 緩衝區</span><span class="sxs-lookup"><span data-stu-id="79f8f-163">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_DRAW\_BUFFER</span></span>

<span data-ttu-id="79f8f-164">具有引數 GL \_ AUX \_ 緩衝區的 glGet</span><span class="sxs-lookup"><span data-stu-id="79f8f-164">**glGet** with argument GL\_AUX\_BUFFERS</span></span>

## <a name="requirements"></a><span data-ttu-id="79f8f-165">規格需求</span><span class="sxs-lookup"><span data-stu-id="79f8f-165">Requirements</span></span>



| <span data-ttu-id="79f8f-166">需求</span><span class="sxs-lookup"><span data-stu-id="79f8f-166">Requirement</span></span> | <span data-ttu-id="79f8f-167">值</span><span class="sxs-lookup"><span data-stu-id="79f8f-167">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="79f8f-168">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="79f8f-168">Minimum supported client</span></span><br/> | <span data-ttu-id="79f8f-169">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="79f8f-169">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="79f8f-170">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="79f8f-170">Minimum supported server</span></span><br/> | <span data-ttu-id="79f8f-171">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="79f8f-171">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="79f8f-172">標頭</span><span class="sxs-lookup"><span data-stu-id="79f8f-172">Header</span></span><br/>                   | <dl> <span data-ttu-id="79f8f-173"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="79f8f-173"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="79f8f-174">程式庫</span><span class="sxs-lookup"><span data-stu-id="79f8f-174">Library</span></span><br/>                  | <dl> <span data-ttu-id="79f8f-175"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="79f8f-175"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="79f8f-176">DLL</span><span class="sxs-lookup"><span data-stu-id="79f8f-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="79f8f-177"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="79f8f-177"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79f8f-178">另請參閱</span><span class="sxs-lookup"><span data-stu-id="79f8f-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79f8f-179">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="79f8f-179">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="79f8f-180">**glBlendFunc**</span><span class="sxs-lookup"><span data-stu-id="79f8f-180">**glBlendFunc**</span></span>](glblendfunc.md)
</dt> <dt>

[<span data-ttu-id="79f8f-181">**glColorMask**</span><span class="sxs-lookup"><span data-stu-id="79f8f-181">**glColorMask**</span></span>](glcolormask.md)
</dt> <dt>

[<span data-ttu-id="79f8f-182">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="79f8f-182">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="79f8f-183">**glGet**</span><span class="sxs-lookup"><span data-stu-id="79f8f-183">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="79f8f-184">**glIndexMask**</span><span class="sxs-lookup"><span data-stu-id="79f8f-184">**glIndexMask**</span></span>](glindexmask.md)
</dt> <dt>

[<span data-ttu-id="79f8f-185">**glLogicOp**</span><span class="sxs-lookup"><span data-stu-id="79f8f-185">**glLogicOp**</span></span>](gllogicop.md)
</dt> <dt>

[<span data-ttu-id="79f8f-186">**glReadBuffer**</span><span class="sxs-lookup"><span data-stu-id="79f8f-186">**glReadBuffer**</span></span>](glreadbuffer.md)
</dt> </dl>

 

 





