---
title: 'glLogicOp 函式 (Gl) '
description: GlLogicOp 函式會指定色彩索引呈現的邏輯圖元運算。
ms.assetid: 29edf9bd-f3b8-4de7-9afb-07714f4efd92
keywords:
- glLogicOp 函式 OpenGL
topic_type:
- apiref
api_name:
- glLogicOp
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb29e8f845e99f6d3c988dfd0c0201de129bee69
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509450"
---
# <a name="gllogicop-function"></a><span data-ttu-id="9c11f-104">glLogicOp 函式</span><span class="sxs-lookup"><span data-stu-id="9c11f-104">glLogicOp function</span></span>

<span data-ttu-id="9c11f-105">**GlLogicOp** 函式會指定色彩索引呈現的邏輯圖元運算。</span><span class="sxs-lookup"><span data-stu-id="9c11f-105">The **glLogicOp** function specifies a logical pixel operation for color index rendering.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c11f-106">語法</span><span class="sxs-lookup"><span data-stu-id="9c11f-106">Syntax</span></span>


```C++
void WINAPI glLogicOp(
   GLenum opcode
);
```



## <a name="parameters"></a><span data-ttu-id="9c11f-107">參數</span><span class="sxs-lookup"><span data-stu-id="9c11f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c11f-108">*opcode*</span><span class="sxs-lookup"><span data-stu-id="9c11f-108">*opcode*</span></span> 
</dt> <dd>

<span data-ttu-id="9c11f-109">選取邏輯運算的符號常數。</span><span class="sxs-lookup"><span data-stu-id="9c11f-109">A symbolic constant that selects a logical operation.</span></span> <span data-ttu-id="9c11f-110">接受下列符號，其中 s 等於來源位的值，而 d 是目的地位的值。</span><span class="sxs-lookup"><span data-stu-id="9c11f-110">The following symbols are accepted where s equals the value of the source bit and d is the value of the destination bit.</span></span>



| <span data-ttu-id="9c11f-111">值</span><span class="sxs-lookup"><span data-stu-id="9c11f-111">Value</span></span>                                                                                                                                                                   | <span data-ttu-id="9c11f-112">意義</span><span class="sxs-lookup"><span data-stu-id="9c11f-112">Meaning</span></span>              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|
| <span id="GL_CLEAR"></span><span id="gl_clear"></span><dl> <span data-ttu-id="9c11f-113"><dt>**GL \_ 清除**</dt></span><span class="sxs-lookup"><span data-stu-id="9c11f-113"><dt>**GL\_CLEAR**</dt></span></span> </dl>                          | <span data-ttu-id="9c11f-114">0</span><span class="sxs-lookup"><span data-stu-id="9c11f-114">0</span></span><br/>         |
| <span id="GL_SET"></span><span id="gl_set"></span><dl> <span data-ttu-id="9c11f-115"><dt>**GL \_ 設定**</dt></span><span class="sxs-lookup"><span data-stu-id="9c11f-115"><dt>**GL\_SET**</dt></span></span> </dl>                                | <span data-ttu-id="9c11f-116">1</span><span class="sxs-lookup"><span data-stu-id="9c11f-116">1</span></span><br/>         |
| <span id="GL_COPY"></span><span id="gl_copy"></span><dl> <span data-ttu-id="9c11f-117"><dt>**GL \_ 複製**</dt></span><span class="sxs-lookup"><span data-stu-id="9c11f-117"><dt>**GL\_COPY**</dt></span></span> </dl>                             | <span data-ttu-id="9c11f-118">s</span><span class="sxs-lookup"><span data-stu-id="9c11f-118">s</span></span><br/>         |
| <span id="GL_COPY_INVERTED"></span><span id="gl_copy_inverted"></span><dl> <span data-ttu-id="9c11f-119"><dt>**GL \_ 複製 \_ 反轉**</dt></span><span class="sxs-lookup"><span data-stu-id="9c11f-119"><dt>**GL\_COPY\_INVERTED**</dt></span></span> </dl> | <span data-ttu-id="9c11f-120">！ s</span><span class="sxs-lookup"><span data-stu-id="9c11f-120">!s</span></span><br/>        |
| <span id="GL_NOOP"></span><span id="gl_noop"></span><dl> <span data-ttu-id="9c11f-121"><dt>**GL \_ NOOP**</dt></span><span class="sxs-lookup"><span data-stu-id="9c11f-121"><dt>**GL\_NOOP**</dt></span></span> </dl>                             | <span data-ttu-id="9c11f-122">d</span><span class="sxs-lookup"><span data-stu-id="9c11f-122">d</span></span><br/>         |
| <span id="GL_INVERT"></span><span id="gl_invert"></span><dl> <span data-ttu-id="9c11f-123"><dt>**GL \_ 反轉**</dt></span><span class="sxs-lookup"><span data-stu-id="9c11f-123"><dt>**GL\_INVERT**</dt></span></span> </dl>                       | <span data-ttu-id="9c11f-124">！ d</span><span class="sxs-lookup"><span data-stu-id="9c11f-124">!d</span></span><br/>        |
| <span id="GL_AND"></span><span id="gl_and"></span><dl> <span data-ttu-id="9c11f-125"><dt>**GL \_ 和**</dt></span><span class="sxs-lookup"><span data-stu-id="9c11f-125"><dt>**GL\_AND**</dt></span></span> </dl>                                | <span data-ttu-id="9c11f-126">s & d</span><span class="sxs-lookup"><span data-stu-id="9c11f-126">s & d</span></span><br/>     |
| <span id="GL_NAND"></span><span id="gl_nand"></span><dl> <span data-ttu-id="9c11f-127"><dt>**GL \_ N**</dt></span><span class="sxs-lookup"><span data-stu-id="9c11f-127"><dt>**GL\_NAND**</dt></span></span> </dl>                             | <span data-ttu-id="9c11f-128">！ (s & d) </span><span class="sxs-lookup"><span data-stu-id="9c11f-128">!(s & d)</span></span><br/>  |
| <span id="GL_OR"></span><span id="gl_or"></span><dl> <span data-ttu-id="9c11f-129"><dt>**GL \_ 或**</dt></span><span class="sxs-lookup"><span data-stu-id="9c11f-129"><dt>**GL\_OR**</dt></span></span> </dl>                                   | <span data-ttu-id="9c11f-130">s \| d</span><span class="sxs-lookup"><span data-stu-id="9c11f-130">s \| d</span></span><br/>    |
| <span id="GL_NOR"></span><span id="gl_nor"></span><dl> <span data-ttu-id="9c11f-131"><dt>**GL \_ 或**</dt></span><span class="sxs-lookup"><span data-stu-id="9c11f-131"><dt>**GL\_NOR**</dt></span></span> </dl>                                | <span data-ttu-id="9c11f-132">！ (s \| d) </span><span class="sxs-lookup"><span data-stu-id="9c11f-132">!(s \| d)</span></span><br/> |
| <span id="GL_XOR"></span><span id="gl_xor"></span><dl> <span data-ttu-id="9c11f-133"><dt>**GL \_ XOR**</dt></span><span class="sxs-lookup"><span data-stu-id="9c11f-133"><dt>**GL\_XOR**</dt></span></span> </dl>                                | <span data-ttu-id="9c11f-134">s ^ d</span><span class="sxs-lookup"><span data-stu-id="9c11f-134">s ^ d</span></span><br/>     |
| <span id="GL_EQUIV"></span><span id="gl_equiv"></span><dl> <span data-ttu-id="9c11f-135"><dt>**GL \_ HTTP-EQUIV**</dt></span><span class="sxs-lookup"><span data-stu-id="9c11f-135"><dt>**GL\_EQUIV**</dt></span></span> </dl>                          | <span data-ttu-id="9c11f-136">！ (s ^ d) </span><span class="sxs-lookup"><span data-stu-id="9c11f-136">!(s ^ d)</span></span><br/>  |
| <span id="GL_AND_REVERSE"></span><span id="gl_and_reverse"></span><dl> <span data-ttu-id="9c11f-137"><dt>**GL \_ 和 \_ 反向**</dt></span><span class="sxs-lookup"><span data-stu-id="9c11f-137"><dt>**GL\_AND\_REVERSE**</dt></span></span> </dl>       | <span data-ttu-id="9c11f-138">s &！ d</span><span class="sxs-lookup"><span data-stu-id="9c11f-138">s & !d</span></span><br/>    |
| <span id="GL_AND_INVERTED"></span><span id="gl_and_inverted"></span><dl> <span data-ttu-id="9c11f-139"><dt>**GL \_ 和 \_ 倒轉**</dt></span><span class="sxs-lookup"><span data-stu-id="9c11f-139"><dt>**GL\_AND\_INVERTED**</dt></span></span> </dl>    | <span data-ttu-id="9c11f-140">！ s & d</span><span class="sxs-lookup"><span data-stu-id="9c11f-140">!s & d</span></span><br/>    |
| <span id="GL_OR_REVERSE"></span><span id="gl_or_reverse"></span><dl> <span data-ttu-id="9c11f-141"><dt>**GL \_ 或 \_ 反轉**</dt></span><span class="sxs-lookup"><span data-stu-id="9c11f-141"><dt>**GL\_OR\_REVERSE**</dt></span></span> </dl>          | <span data-ttu-id="9c11f-142">s \| ！ d</span><span class="sxs-lookup"><span data-stu-id="9c11f-142">s \| !d</span></span><br/>   |
| <span id="GL_OR_INVERTED"></span><span id="gl_or_inverted"></span><dl> <span data-ttu-id="9c11f-143"><dt>**GL \_ 或 \_ 反轉**</dt></span><span class="sxs-lookup"><span data-stu-id="9c11f-143"><dt>**GL\_OR\_INVERTED**</dt></span></span> </dl>       | <span data-ttu-id="9c11f-144">！ s \| d</span><span class="sxs-lookup"><span data-stu-id="9c11f-144">!s \| d</span></span><br/>   |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c11f-145">傳回值</span><span class="sxs-lookup"><span data-stu-id="9c11f-145">Return value</span></span>

<span data-ttu-id="9c11f-146">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="9c11f-146">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="9c11f-147">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="9c11f-147">Error codes</span></span>

<span data-ttu-id="9c11f-148">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="9c11f-148">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="9c11f-149">Name</span><span class="sxs-lookup"><span data-stu-id="9c11f-149">Name</span></span>                                                                                                  | <span data-ttu-id="9c11f-150">意義</span><span class="sxs-lookup"><span data-stu-id="9c11f-150">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9c11f-151"><dt>**GL \_ 無效 \_ 列舉**</dt></span><span class="sxs-lookup"><span data-stu-id="9c11f-151"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="9c11f-152">*opcode* 不是可接受的值。</span><span class="sxs-lookup"><span data-stu-id="9c11f-152">*opcode* was not an accepted value.</span></span><br/>                                                                                        |
| <dl> <span data-ttu-id="9c11f-153"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="9c11f-153"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="9c11f-154">呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。</span><span class="sxs-lookup"><span data-stu-id="9c11f-154">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="9c11f-155">備註</span><span class="sxs-lookup"><span data-stu-id="9c11f-155">Remarks</span></span>

<span data-ttu-id="9c11f-156">**GlLogicOp** 函式會指定在已啟用時，于畫面格緩衝區中對應位置的內送色彩索引和色彩索引之間套用的邏輯運算。</span><span class="sxs-lookup"><span data-stu-id="9c11f-156">The **glLogicOp** function specifies a logical operation that, when enabled, is applied between the incoming color index and the color index at the corresponding location in the framebuffer.</span></span> <span data-ttu-id="9c11f-157">使用符號常數 GL 邏輯 OP 來啟用或停用 [**glEnable**](glenable.md) 和 **glDisable** 的邏輯 \_ 作業 \_ 。</span><span class="sxs-lookup"><span data-stu-id="9c11f-157">The logical operation is enabled or disabled with [**glEnable**](glenable.md) and **glDisable** using the symbolic constant GL\_LOGIC\_OP.</span></span>

<span data-ttu-id="9c11f-158">*Opcode* 參數是從下列清單中選擇的符號常數。</span><span class="sxs-lookup"><span data-stu-id="9c11f-158">The *opcode* parameter is a symbolic constant chosen from the list below.</span></span> <span data-ttu-id="9c11f-159">在邏輯作業的說明中， *s* 代表傳入的色彩索引，而 *d* 代表畫面格緩衝區中的索引。</span><span class="sxs-lookup"><span data-stu-id="9c11f-159">In the explanation of the logical operations, *s* represents the incoming color index and *d* represents the index in the framebuffer.</span></span> <span data-ttu-id="9c11f-160">使用標準 C 語言運算子。</span><span class="sxs-lookup"><span data-stu-id="9c11f-160">Standard C-language operators are used.</span></span> <span data-ttu-id="9c11f-161">如同這些位運算子的建議，邏輯作業會獨立套用至來源和目的地索引的每個位配對。</span><span class="sxs-lookup"><span data-stu-id="9c11f-161">As these bitwise operators suggest, the logical operation is applied independently to each bit pair of the source and destination indexes.</span></span>

<span data-ttu-id="9c11f-162">邏輯圖元作業不會套用到 RGBA 色彩緩衝區。</span><span class="sxs-lookup"><span data-stu-id="9c11f-162">Logical pixel operations are not applied to RGBA color buffers.</span></span>

<span data-ttu-id="9c11f-163">當有一個以上的色彩索引緩衝區啟用繪圖時，會針對每個啟用的緩衝區個別完成邏輯作業，使用目的地索引的緩衝區內容 (查看 [**glDrawBuffer**](gldrawbuffer.md)) 。</span><span class="sxs-lookup"><span data-stu-id="9c11f-163">When more than one color-index buffer is enabled for drawing, logical operations are done separately for each enabled buffer, using the contents of that buffer for the destination index (see [**glDrawBuffer**](gldrawbuffer.md)).</span></span>

<span data-ttu-id="9c11f-164">*Opcode* 參數必須是16個接受值的其中一個。</span><span class="sxs-lookup"><span data-stu-id="9c11f-164">The *opcode* parameter must be one of the 16 accepted values.</span></span> <span data-ttu-id="9c11f-165">其他值會導致錯誤。</span><span class="sxs-lookup"><span data-stu-id="9c11f-165">Other values result in an error.</span></span>

<span data-ttu-id="9c11f-166">下列函式會取出與 **glLogicOp** 相關的資訊：</span><span class="sxs-lookup"><span data-stu-id="9c11f-166">The following functions retrieve information related to **glLogicOp**:</span></span>

<span data-ttu-id="9c11f-167">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 邏輯 \_ OP \_ 模式的 glGet</span><span class="sxs-lookup"><span data-stu-id="9c11f-167">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_LOGIC\_OP\_MODE</span></span>

<span data-ttu-id="9c11f-168">[](glisenabled.md)具有引數 GL \_ 邏輯 \_ OP 的 glIsEnabled</span><span class="sxs-lookup"><span data-stu-id="9c11f-168">[**glIsEnabled**](glisenabled.md) with argument GL\_LOGIC\_OP</span></span>

## <a name="requirements"></a><span data-ttu-id="9c11f-169">規格需求</span><span class="sxs-lookup"><span data-stu-id="9c11f-169">Requirements</span></span>



| <span data-ttu-id="9c11f-170">需求</span><span class="sxs-lookup"><span data-stu-id="9c11f-170">Requirement</span></span> | <span data-ttu-id="9c11f-171">值</span><span class="sxs-lookup"><span data-stu-id="9c11f-171">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9c11f-172">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9c11f-172">Minimum supported client</span></span><br/> | <span data-ttu-id="9c11f-173">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9c11f-173">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="9c11f-174">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9c11f-174">Minimum supported server</span></span><br/> | <span data-ttu-id="9c11f-175">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9c11f-175">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9c11f-176">標頭</span><span class="sxs-lookup"><span data-stu-id="9c11f-176">Header</span></span><br/>                   | <dl> <span data-ttu-id="9c11f-177"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="9c11f-177"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="9c11f-178">程式庫</span><span class="sxs-lookup"><span data-stu-id="9c11f-178">Library</span></span><br/>                  | <dl> <span data-ttu-id="9c11f-179"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="9c11f-179"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="9c11f-180">DLL</span><span class="sxs-lookup"><span data-stu-id="9c11f-180">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9c11f-181"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9c11f-181"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9c11f-182">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9c11f-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c11f-183">**glAlphaFunc**</span><span class="sxs-lookup"><span data-stu-id="9c11f-183">**glAlphaFunc**</span></span>](glalphafunc.md)
</dt> <dt>

[<span data-ttu-id="9c11f-184">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="9c11f-184">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="9c11f-185">**glBlendFunc**</span><span class="sxs-lookup"><span data-stu-id="9c11f-185">**glBlendFunc**</span></span>](glblendfunc.md)
</dt> <dt>

[<span data-ttu-id="9c11f-186">**glDrawBuffer**</span><span class="sxs-lookup"><span data-stu-id="9c11f-186">**glDrawBuffer**</span></span>](gldrawbuffer.md)
</dt> <dt>

[<span data-ttu-id="9c11f-187">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="9c11f-187">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="9c11f-188">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="9c11f-188">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="9c11f-189">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="9c11f-189">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="9c11f-190">**glStencilOp**</span><span class="sxs-lookup"><span data-stu-id="9c11f-190">**glStencilOp**</span></span>](glstencilop.md)
</dt> </dl>

 

 





