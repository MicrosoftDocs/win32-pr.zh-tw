---
title: 'glAccum 函式 (Gl) '
description: GlAccum 函數會在累積緩衝區上運作。
ms.assetid: 3ddd69fe-74fc-4ac0-be8d-bcaa71ac0292
keywords:
- glAccum 函式 OpenGL
topic_type:
- apiref
api_name:
- glAccum
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6d25e02971d07d54567c462708aa4efd87b2d32
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686019"
---
# <a name="glaccum-function"></a><span data-ttu-id="bd293-104">glAccum 函式</span><span class="sxs-lookup"><span data-stu-id="bd293-104">glAccum function</span></span>

<span data-ttu-id="bd293-105">**GlAccum** 函數會在累積緩衝區上運作。</span><span class="sxs-lookup"><span data-stu-id="bd293-105">The **glAccum** function operates on the accumulation buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd293-106">語法</span><span class="sxs-lookup"><span data-stu-id="bd293-106">Syntax</span></span>


```C++
void WINAPI glAccum(
   GLenum  op,
   GLfloat value
);
```



## <a name="parameters"></a><span data-ttu-id="bd293-107">參數</span><span class="sxs-lookup"><span data-stu-id="bd293-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd293-108">*op*</span><span class="sxs-lookup"><span data-stu-id="bd293-108">*op*</span></span> 
</dt> <dd>

<span data-ttu-id="bd293-109">累積緩衝區作業。</span><span class="sxs-lookup"><span data-stu-id="bd293-109">The accumulation buffer operation.</span></span> <span data-ttu-id="bd293-110">接受的符號常數如下所示。</span><span class="sxs-lookup"><span data-stu-id="bd293-110">The accepted symbolic constants are as follows.</span></span>



| <span data-ttu-id="bd293-111">值</span><span class="sxs-lookup"><span data-stu-id="bd293-111">Value</span></span>                                                                                                                                             | <span data-ttu-id="bd293-112">意義</span><span class="sxs-lookup"><span data-stu-id="bd293-112">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_ACCUM"></span><span id="gl_accum"></span><dl> <span data-ttu-id="bd293-113"><dt>**GL \_ ACCUM**</dt></span><span class="sxs-lookup"><span data-stu-id="bd293-113"><dt>**GL\_ACCUM**</dt></span></span> </dl>    | <span data-ttu-id="bd293-114">從目前選取要讀取的緩衝區取得 R、G、B 和值 (參閱 [**glReadBuffer**](glreadbuffer.md)) 。</span><span class="sxs-lookup"><span data-stu-id="bd293-114">Obtains R, G, B, and A values from the buffer currently selected for reading (see [**glReadBuffer**](glreadbuffer.md)).</span></span> <span data-ttu-id="bd293-115">每個元件值都除以 2 *n*  1，其中 *n* 是配置給目前所選緩衝區中每個色彩元件的位數。</span><span class="sxs-lookup"><span data-stu-id="bd293-115">Each component value is divided by 2 *n*  1, where *n* is the number of bits allocated to each color component in the currently selected buffer.</span></span> <span data-ttu-id="bd293-116">結果是範圍0，1的浮點值， \[ \] 會乘以 *值* 並加入至累積緩衝區中的對應圖元元件，藉此更新累積緩衝區。</span><span class="sxs-lookup"><span data-stu-id="bd293-116">The result is a floating-point value in the range \[0,1\], which is multiplied by *value* and added to the corresponding pixel component in the accumulation buffer, thereby updating the accumulation buffer.</span></span><br/> |
| <span id="GL_LOAD"></span><span id="gl_load"></span><dl> <span data-ttu-id="bd293-117"><dt>**GL \_ 負載**</dt></span><span class="sxs-lookup"><span data-stu-id="bd293-117"><dt>**GL\_LOAD**</dt></span></span> </dl>       | <span data-ttu-id="bd293-118">類似于 GL \_ ACCUM，不同之處在于累積緩衝區中的目前值不會用於計算新值。</span><span class="sxs-lookup"><span data-stu-id="bd293-118">Similar to GL\_ACCUM, except that the current value in the accumulation buffer is not used in the calculation of the new value.</span></span> <span data-ttu-id="bd293-119">也就是說，R、G、B 和目前所選緩衝區的值會除以 2 *n*  1、乘以 *值*，然後儲存在對應的累積緩衝區資料格中，以覆寫目前的值。</span><span class="sxs-lookup"><span data-stu-id="bd293-119">That is, the R, G, B, and A values from the currently selected buffer are divided by 2 *n*  1, multiplied by *value*, and then stored in the corresponding accumulation buffer cell, overwriting the current value.</span></span><br/>                                                                                                                                      |
| <span id="GL_ADD"></span><span id="gl_add"></span><dl> <span data-ttu-id="bd293-120"><dt>**GL \_ 新增**</dt></span><span class="sxs-lookup"><span data-stu-id="bd293-120"><dt>**GL\_ADD**</dt></span></span> </dl>          | <span data-ttu-id="bd293-121">將 *值* 加入至累積緩衝區中的每個 R、G、B 和 A。</span><span class="sxs-lookup"><span data-stu-id="bd293-121">Adds *value* to each R, G, B, and A in the accumulation buffer.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="GL_MULT"></span><span id="gl_mult"></span><dl> <span data-ttu-id="bd293-122"><dt>**GL \_ MULT**</dt></span><span class="sxs-lookup"><span data-stu-id="bd293-122"><dt>**GL\_MULT**</dt></span></span> </dl>       | <span data-ttu-id="bd293-123">以傳 *值* 方式將累積緩衝區中的每個 R、G、B 和 A 相乘，並將縮放的元件傳回至其對應的累積緩衝區位置。</span><span class="sxs-lookup"><span data-stu-id="bd293-123">Multiplies each R, G, B, and A in the accumulation buffer by *value* and returns the scaled component to its corresponding accumulation buffer location.</span></span><br/>                                                                                                                                                                                                                                                                                                                                |
| <span id="GL_RETURN"></span><span id="gl_return"></span><dl> <span data-ttu-id="bd293-124"><dt>**GL \_ 退貨**</dt></span><span class="sxs-lookup"><span data-stu-id="bd293-124"><dt>**GL\_RETURN**</dt></span></span> </dl> | <span data-ttu-id="bd293-125">將累積的緩衝區值傳輸到目前選取要寫入的色彩緩衝區或緩衝區。</span><span class="sxs-lookup"><span data-stu-id="bd293-125">Transfers accumulation buffer values to the color buffer or buffers currently selected for writing.</span></span> <span data-ttu-id="bd293-126">每個 R、G、B 和 A 元件都會乘以 *value*，然後乘以 2 *n*  1，壓制至範圍 \[ 0，2 *n*  1 \] ，並儲存在對應的顯示緩衝區資料格中。</span><span class="sxs-lookup"><span data-stu-id="bd293-126">Each R, G, B, and A component is multiplied by *value*, then multiplied by 2 *n*  1, clamped to the range \[0, 2 *n*  1 \], and stored in the corresponding display buffer cell.</span></span> <span data-ttu-id="bd293-127">套用到此傳輸的唯一片段作業是圖元擁有權、剪下、遞色和色彩 writemasks。</span><span class="sxs-lookup"><span data-stu-id="bd293-127">The only fragment operations that are applied to this transfer are pixel ownership, scissor, dithering, and color writemasks.</span></span><br/>                                                                        |



 

</dd> <dt>

<span data-ttu-id="bd293-128">*value*</span><span class="sxs-lookup"><span data-stu-id="bd293-128">*value*</span></span> 
</dt> <dd>

<span data-ttu-id="bd293-129">在累積緩衝區作業中使用的浮點值。</span><span class="sxs-lookup"><span data-stu-id="bd293-129">A floating-point value used in the accumulation buffer operation.</span></span> <span data-ttu-id="bd293-130">*Op* 參數會決定 *值* 的使用方式。</span><span class="sxs-lookup"><span data-stu-id="bd293-130">The *op* parameter determines how *value* is used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd293-131">傳回值</span><span class="sxs-lookup"><span data-stu-id="bd293-131">Return value</span></span>

<span data-ttu-id="bd293-132">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="bd293-132">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="bd293-133">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="bd293-133">Error codes</span></span>

<span data-ttu-id="bd293-134">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="bd293-134">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="bd293-135">Name</span><span class="sxs-lookup"><span data-stu-id="bd293-135">Name</span></span>                                                                                                  | <span data-ttu-id="bd293-136">意義</span><span class="sxs-lookup"><span data-stu-id="bd293-136">Meaning</span></span>                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="bd293-137"><dt>**GL \_ 無效 \_ 列舉**</dt></span><span class="sxs-lookup"><span data-stu-id="bd293-137"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="bd293-138">*op* 不是可接受的值。</span><span class="sxs-lookup"><span data-stu-id="bd293-138">*op* was not an accepted value.</span></span><br/>                                                                                                                                            |
| <dl> <span data-ttu-id="bd293-139"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="bd293-139"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="bd293-140">沒有累積緩衝區，或呼叫 [**glBegin**](glbegin.md)和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數 **glAccum** 。</span><span class="sxs-lookup"><span data-stu-id="bd293-140">There was no accumulation buffer or the function **glAccum** was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="bd293-141">備註</span><span class="sxs-lookup"><span data-stu-id="bd293-141">Remarks</span></span>

<span data-ttu-id="bd293-142">累積緩衝區是延伸範圍的色彩緩衝區。</span><span class="sxs-lookup"><span data-stu-id="bd293-142">The accumulation buffer is an extended-range color buffer.</span></span> <span data-ttu-id="bd293-143">影像不會轉譯到其中。</span><span class="sxs-lookup"><span data-stu-id="bd293-143">Images are not rendered into it.</span></span> <span data-ttu-id="bd293-144">相反地，轉譯成其中一個色彩緩衝區的影像會在轉譯之後加入累積緩衝區的內容中。</span><span class="sxs-lookup"><span data-stu-id="bd293-144">Rather, images rendered into one of the color buffers are added to the contents of the accumulation buffer after rendering.</span></span> <span data-ttu-id="bd293-145">您可以藉由使用不同的轉換矩陣產生的影像累積，來建立點、線條和多邊形的消除鋸齒 (、曲線) 、運動模糊和欄位深度等效果。</span><span class="sxs-lookup"><span data-stu-id="bd293-145">You can create effects such as antialiasing (of points, lines, and polygons), motion blur, and depth of field by accumulating images generated with different transformation matrices.</span></span>

<span data-ttu-id="bd293-146">累積緩衝區中的每個圖元都是由紅色、綠色、藍色和 Alpha 值所組成。</span><span class="sxs-lookup"><span data-stu-id="bd293-146">Each pixel in the accumulation buffer consists of red, green, blue, and alpha values.</span></span> <span data-ttu-id="bd293-147">累積緩衝區中每個元件的位數取決於執行量。</span><span class="sxs-lookup"><span data-stu-id="bd293-147">The number of bits per component in the accumulation buffer depends on the implementation.</span></span> <span data-ttu-id="bd293-148">您可以藉由呼叫 [**glGetIntegerv**](glgetintegerv.md) 四次，分別使用引數 GL \_ ACCUM RED \_ bit \_ 、GL \_ ACCUM \_ 綠 BIT \_ 、gl \_ ACCUM \_ BLUE \_ bits 和 gl \_ ACCUM \_ ALPHA \_ bit 來檢查此數目。</span><span class="sxs-lookup"><span data-stu-id="bd293-148">You can examine this number by calling [**glGetIntegerv**](glgetintegerv.md) four times, with the arguments GL\_ACCUM\_RED\_BITS, GL\_ACCUM\_GREEN\_BITS, GL\_ACCUM\_BLUE\_BITS, and GL\_ACCUM\_ALPHA\_BITS, respectively.</span></span> <span data-ttu-id="bd293-149">但是，不論每個元件的位數為何，每個元件儲存的值範圍都是 \[ 1，？ 1 \] 。</span><span class="sxs-lookup"><span data-stu-id="bd293-149">Regardless of the number of bits per component, however, the range of values stored by each component is \[ 1,?1\].</span></span> <span data-ttu-id="bd293-150">累積的緩衝區圖元會以畫面格緩衝區圖元為一對一對應。</span><span class="sxs-lookup"><span data-stu-id="bd293-150">The accumulation buffer pixels are mapped one-to-one with framebuffer pixels.</span></span>

<span data-ttu-id="bd293-151">**GlAccum** 函數會在累積緩衝區上運作。</span><span class="sxs-lookup"><span data-stu-id="bd293-151">The **glAccum** function operates on the accumulation buffer.</span></span> <span data-ttu-id="bd293-152">第一個引數 *op* 是選取累積緩衝區作業的符號常數。</span><span class="sxs-lookup"><span data-stu-id="bd293-152">The first argument, *op*, is a symbolic constant that selects an accumulation buffer operation.</span></span> <span data-ttu-id="bd293-153">第二個引數（ *value*）是要在該作業中使用的浮點值。</span><span class="sxs-lookup"><span data-stu-id="bd293-153">The second argument, *value*, is a floating-point value to be used in that operation.</span></span> <span data-ttu-id="bd293-154">指定了五個作業： GL \_ ACCUM、gl \_ LOAD、gl \_ ADD、GL \_ MULT 和 gl \_ 退回。</span><span class="sxs-lookup"><span data-stu-id="bd293-154">Five operations are specified: GL\_ACCUM, GL\_LOAD, GL\_ADD, GL\_MULT, and GL\_RETURN.</span></span>

<span data-ttu-id="bd293-155">所有累積的緩衝區作業僅限於目前剪下方塊的區域，並與每個圖元的紅色、綠色、藍色和 Alpha 元件相同套用。</span><span class="sxs-lookup"><span data-stu-id="bd293-155">All accumulation buffer operations are limited to the area of the current scissor box and are applied identically to the red, green, blue, and alpha components of each pixel.</span></span> <span data-ttu-id="bd293-156">如果 **glAccum** 作業產生的值超出範圍 \[ 1，1，則會定義累積緩衝區圖元元件的內容 \] 。</span><span class="sxs-lookup"><span data-stu-id="bd293-156">The contents of an accumulation buffer pixel component are undefined if the **glAccum** operation results in a value outside the range \[ 1,1\].</span></span>

<span data-ttu-id="bd293-157">若要清除累積緩衝區，請使用 [**glClearAccum**](glclearaccum.md) 函式來指定 R、G、B 和值，以將其設定為，併發出 [**glClear**](glclear.md) 函數並啟用累積緩衝區。</span><span class="sxs-lookup"><span data-stu-id="bd293-157">To clear the accumulation buffer, use the [**glClearAccum**](glclearaccum.md) function to specify R, G, B, and A values to set it to, and issue a [**glClear**](glclear.md) function with the accumulation buffer enabled.</span></span>

<span data-ttu-id="bd293-158">任何 **glAccum** 作業都只會更新目前剪式方塊內的圖元。</span><span class="sxs-lookup"><span data-stu-id="bd293-158">Only those pixels within the current scissor box are updated by any **glAccum** operation.</span></span>

<span data-ttu-id="bd293-159">下列函式會取出與 **glAccum** 函數相關的資訊：</span><span class="sxs-lookup"><span data-stu-id="bd293-159">The following functions retrieve information related to the **glAccum** function:</span></span>

<span data-ttu-id="bd293-160">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)與引數 GL \_ ACCUM \_ RED bit \_</span><span class="sxs-lookup"><span data-stu-id="bd293-160">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_ACCUM\_RED\_BITS</span></span>

<span data-ttu-id="bd293-161">**glGet** 與引數 GL \_ ACCUM \_ 綠 \_ 位</span><span class="sxs-lookup"><span data-stu-id="bd293-161">**glGet** with argument GL\_ACCUM\_GREEN\_BITS</span></span>

<span data-ttu-id="bd293-162">**glGet** 與引數 GL \_ ACCUM \_ BLUE \_ BITS</span><span class="sxs-lookup"><span data-stu-id="bd293-162">**glGet** with argument GL\_ACCUM\_BLUE\_BITS</span></span>

<span data-ttu-id="bd293-163">**glGet** 與引數 GL \_ ACCUM \_ ALPHA \_ 位</span><span class="sxs-lookup"><span data-stu-id="bd293-163">**glGet** with argument GL\_ACCUM\_ALPHA\_BITS</span></span>

## <a name="requirements"></a><span data-ttu-id="bd293-164">規格需求</span><span class="sxs-lookup"><span data-stu-id="bd293-164">Requirements</span></span>



| <span data-ttu-id="bd293-165">需求</span><span class="sxs-lookup"><span data-stu-id="bd293-165">Requirement</span></span> | <span data-ttu-id="bd293-166">值</span><span class="sxs-lookup"><span data-stu-id="bd293-166">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bd293-167">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bd293-167">Minimum supported client</span></span><br/> | <span data-ttu-id="bd293-168">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bd293-168">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="bd293-169">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bd293-169">Minimum supported server</span></span><br/> | <span data-ttu-id="bd293-170">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bd293-170">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="bd293-171">標頭</span><span class="sxs-lookup"><span data-stu-id="bd293-171">Header</span></span><br/>                   | <dl> <span data-ttu-id="bd293-172"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="bd293-172"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="bd293-173">程式庫</span><span class="sxs-lookup"><span data-stu-id="bd293-173">Library</span></span><br/>                  | <dl> <span data-ttu-id="bd293-174"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="bd293-174"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="bd293-175">DLL</span><span class="sxs-lookup"><span data-stu-id="bd293-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bd293-176"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bd293-176"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd293-177">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bd293-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd293-178">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="bd293-178">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="bd293-179">**glBlendFunc**</span><span class="sxs-lookup"><span data-stu-id="bd293-179">**glBlendFunc**</span></span>](glblendfunc.md)
</dt> <dt>

[<span data-ttu-id="bd293-180">**glClear**</span><span class="sxs-lookup"><span data-stu-id="bd293-180">**glClear**</span></span>](glclear.md)
</dt> <dt>

[<span data-ttu-id="bd293-181">**glClearAccum**</span><span class="sxs-lookup"><span data-stu-id="bd293-181">**glClearAccum**</span></span>](glclearaccum.md)
</dt> <dt>

[<span data-ttu-id="bd293-182">**glCopyPixels**</span><span class="sxs-lookup"><span data-stu-id="bd293-182">**glCopyPixels**</span></span>](glcopypixels.md)
</dt> <dt>

[<span data-ttu-id="bd293-183">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="bd293-183">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="bd293-184">**glGet**</span><span class="sxs-lookup"><span data-stu-id="bd293-184">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="bd293-185">**glLogicOp**</span><span class="sxs-lookup"><span data-stu-id="bd293-185">**glLogicOp**</span></span>](gllogicop.md)
</dt> <dt>

[<span data-ttu-id="bd293-186">**glPixelStore**</span><span class="sxs-lookup"><span data-stu-id="bd293-186">**glPixelStore**</span></span>](glpixelstore-functions.md)
</dt> <dt>

[<span data-ttu-id="bd293-187">**glPixelTransfer**</span><span class="sxs-lookup"><span data-stu-id="bd293-187">**glPixelTransfer**</span></span>](glpixeltransfer.md)
</dt> <dt>

[<span data-ttu-id="bd293-188">**glReadBuffer**</span><span class="sxs-lookup"><span data-stu-id="bd293-188">**glReadBuffer**</span></span>](glreadbuffer.md)
</dt> <dt>

[<span data-ttu-id="bd293-189">**glReadPixels**</span><span class="sxs-lookup"><span data-stu-id="bd293-189">**glReadPixels**</span></span>](glreadpixels.md)
</dt> <dt>

[<span data-ttu-id="bd293-190">**glScissor**</span><span class="sxs-lookup"><span data-stu-id="bd293-190">**glScissor**</span></span>](glscissor.md)
</dt> <dt>

[<span data-ttu-id="bd293-191">**glStencilOp**</span><span class="sxs-lookup"><span data-stu-id="bd293-191">**glStencilOp**</span></span>](glstencilop.md)
</dt> </dl>

 

 





