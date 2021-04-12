---
title: 'EM_SETFONTSIZE 訊息 (Richedit .h) '
description: 設定 rich edit 控制項中所選取文字的字型大小。
ms.assetid: 18d91370-12c0-4e5f-a0e9-ffde02abc966
keywords:
- EM_SETFONTSIZE message Windows 控制項
topic_type:
- apiref
api_name:
- EM_SETFONTSIZE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8eb75276acbb86cbd452a8ad97698f1cd7382bd2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465384"
---
# <a name="em_setfontsize-message"></a><span data-ttu-id="822df-104">EM \_ SETFONTSIZE 訊息</span><span class="sxs-lookup"><span data-stu-id="822df-104">EM\_SETFONTSIZE message</span></span>

<span data-ttu-id="822df-105">設定 rich edit 控制項中所選取文字的字型大小。</span><span class="sxs-lookup"><span data-stu-id="822df-105">Sets the font size for the selected text in a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="822df-106">參數</span><span class="sxs-lookup"><span data-stu-id="822df-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="822df-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="822df-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="822df-108">變更所選文字的點大小。</span><span class="sxs-lookup"><span data-stu-id="822df-108">Change in point size of the selected text.</span></span> <span data-ttu-id="822df-109">結果會根據下表所示的值進行四捨五入。</span><span class="sxs-lookup"><span data-stu-id="822df-109">The result will be rounded according to values shown in the following table.</span></span> <span data-ttu-id="822df-110">此參數的範圍應介於-1637 到1638之間。</span><span class="sxs-lookup"><span data-stu-id="822df-110">This parameter should be in the range of -1637 to 1638.</span></span> <span data-ttu-id="822df-111">產生的字型大小會在1到1638的範圍內。</span><span class="sxs-lookup"><span data-stu-id="822df-111">The resulting font size will be within the range of 1 to 1638.</span></span>

</dd> <dt>

<span data-ttu-id="822df-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="822df-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="822df-113">未使用此參數;它必須為零。</span><span class="sxs-lookup"><span data-stu-id="822df-113">This parameter is not used; it must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="822df-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="822df-114">Return value</span></span>

<span data-ttu-id="822df-115">如果未發生任何錯誤，則傳回值為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="822df-115">If no error occurred, the return value is **TRUE**.</span></span>

<span data-ttu-id="822df-116">如果發生錯誤，傳回值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="822df-116">If an error occurred, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="822df-117">備註</span><span class="sxs-lookup"><span data-stu-id="822df-117">Remarks</span></span>

<span data-ttu-id="822df-118">您可以藉由傳送 [**EM \_ GETCHARFORMAT**](em-getcharformat.md) 訊息來輕鬆取得字型大小。</span><span class="sxs-lookup"><span data-stu-id="822df-118">You can easily get the font size by sending the [**EM\_GETCHARFORMAT**](em-getcharformat.md) message.</span></span>

<span data-ttu-id="822df-119">Rich Edit 會先將 *wParam* 新增至目前的字型大小，然後使用產生的大小和下表來判斷舍入值。</span><span class="sxs-lookup"><span data-stu-id="822df-119">Rich Edit first adds *wParam* to the current font size and then uses the resulting size and the following table to determine the rounding value.</span></span>



| <span data-ttu-id="822df-120">樂隊</span><span class="sxs-lookup"><span data-stu-id="822df-120">Band</span></span>    | <span data-ttu-id="822df-121">舍入值</span><span class="sxs-lookup"><span data-stu-id="822df-121">Rounding value</span></span> |
|---------|----------------|
| <span data-ttu-id="822df-122"><= 12</span><span class="sxs-lookup"><span data-stu-id="822df-122"><=12</span></span> | <span data-ttu-id="822df-123">1</span><span class="sxs-lookup"><span data-stu-id="822df-123">1</span></span>              |
| <span data-ttu-id="822df-124">28</span><span class="sxs-lookup"><span data-stu-id="822df-124">28</span></span>      | <span data-ttu-id="822df-125">2</span><span class="sxs-lookup"><span data-stu-id="822df-125">2</span></span>              |
| <span data-ttu-id="822df-126">36</span><span class="sxs-lookup"><span data-stu-id="822df-126">36</span></span>      | <span data-ttu-id="822df-127">0</span><span class="sxs-lookup"><span data-stu-id="822df-127">0</span></span>              |
| <span data-ttu-id="822df-128">48</span><span class="sxs-lookup"><span data-stu-id="822df-128">48</span></span>      | <span data-ttu-id="822df-129">0</span><span class="sxs-lookup"><span data-stu-id="822df-129">0</span></span>              |
| <span data-ttu-id="822df-130">72</span><span class="sxs-lookup"><span data-stu-id="822df-130">72</span></span>      | <span data-ttu-id="822df-131">0</span><span class="sxs-lookup"><span data-stu-id="822df-131">0</span></span>              |
| <span data-ttu-id="822df-132">80</span><span class="sxs-lookup"><span data-stu-id="822df-132">80</span></span>      | <span data-ttu-id="822df-133">0</span><span class="sxs-lookup"><span data-stu-id="822df-133">0</span></span>              |
| <span data-ttu-id="822df-134">> 80</span><span class="sxs-lookup"><span data-stu-id="822df-134">> 80</span></span> | <span data-ttu-id="822df-135">10</span><span class="sxs-lookup"><span data-stu-id="822df-135">10</span></span>             |



 

<span data-ttu-id="822df-136">如果產生的字型大小未以舍入值來平均整除，則會將字型大小舍入成可平均除以舍入值的數位。</span><span class="sxs-lookup"><span data-stu-id="822df-136">If the resulting font size is not evenly divisible by the rounding value, the font size is then rounded to a number evenly divisible by the rounding value.</span></span> <span data-ttu-id="822df-137">因此，如果字型大小小於或等於12，則舍入值會是1。</span><span class="sxs-lookup"><span data-stu-id="822df-137">So if the font size is less than or equal to 12, the rounding value will be 1.</span></span> <span data-ttu-id="822df-138">同樣地，如果字型大小小於或等於28，則舍入值為2。</span><span class="sxs-lookup"><span data-stu-id="822df-138">Similarly, if the font size is less than or equal to 28, the rounding value is 2.</span></span> <span data-ttu-id="822df-139">針對大於28的值，字型大小會四捨五入至下一個頻外。</span><span class="sxs-lookup"><span data-stu-id="822df-139">For values greater than 28, font sizes are rounded to the next band.</span></span> <span data-ttu-id="822df-140">因此，字型大小會跳到36、48、72、80。</span><span class="sxs-lookup"><span data-stu-id="822df-140">So, the font size jumps to 36, 48, 72, 80.</span></span> <span data-ttu-id="822df-141">80之後，會以十個點遞增的方式來完成所有四捨五入。</span><span class="sxs-lookup"><span data-stu-id="822df-141">After 80, all rounding is done in increments of ten points.</span></span>

<span data-ttu-id="822df-142">字型大小會根據 *wParam* 的正負號進位或下移。</span><span class="sxs-lookup"><span data-stu-id="822df-142">The font size is rounded up or down depending on the sign of *wParam*.</span></span> <span data-ttu-id="822df-143">如果 *wParam* 是正數，則四捨五入一律為向上。</span><span class="sxs-lookup"><span data-stu-id="822df-143">If *wParam* is positive, the rounding is always up.</span></span> <span data-ttu-id="822df-144">否則，舍入一律會關閉。</span><span class="sxs-lookup"><span data-stu-id="822df-144">Otherwise, rounding is always down.</span></span> <span data-ttu-id="822df-145">因此，如果目前的字型大小為10，而 *wParam* 為3，則產生的字型大小會是 14 (10 + 3 = 13，其不能被2整除，因此大小會四捨五入為 14) 。</span><span class="sxs-lookup"><span data-stu-id="822df-145">So, if the current font size is 10 and *wParam* is 3, the resulting font size would be 14 (10 + 3 = 13, which is not divisible by 2, so the size rounds up to 14).</span></span> <span data-ttu-id="822df-146">相反地，如果目前的字型大小為14，而 *wParam* 為-3，則產生的字型大小會是 10 (14-3 = 11，而不是由2整除，因此大小會四捨五入為 10) 。</span><span class="sxs-lookup"><span data-stu-id="822df-146">Conversely, if the current font size is 14 and *wParam* is -3, the resulting font size would be 10 (14 - 3 = 11, which is not divisible by 2, so the size rounds down to 10).</span></span>

<span data-ttu-id="822df-147">這項變更會套用至選取專案的每個部分。</span><span class="sxs-lookup"><span data-stu-id="822df-147">The change is applied to each part of the selection.</span></span> <span data-ttu-id="822df-148">因此，如果部分文字是10pt 和某些20pt，在 *wParam* 設定為1的呼叫之後，字型大小會分別變成11pt 和22pt。</span><span class="sxs-lookup"><span data-stu-id="822df-148">So, if some of the text is 10pt and some 20pt, after a call with *wParam* set to 1, the font sizes become 11pt and 22pt, respectively.</span></span>

<span data-ttu-id="822df-149">下表顯示其他範例。</span><span class="sxs-lookup"><span data-stu-id="822df-149">Additional examples are shown in the following table.</span></span>



| <span data-ttu-id="822df-150">原始字型大小</span><span class="sxs-lookup"><span data-stu-id="822df-150">Original font size</span></span> | <span data-ttu-id="822df-151">*wParam*</span><span class="sxs-lookup"><span data-stu-id="822df-151">*wParam*</span></span> | <span data-ttu-id="822df-152">產生的字型大小</span><span class="sxs-lookup"><span data-stu-id="822df-152">Resulting font size</span></span> |
|--------------------|----------|---------------------|
| <span data-ttu-id="822df-153">7</span><span class="sxs-lookup"><span data-stu-id="822df-153">7</span></span>                  | <span data-ttu-id="822df-154">1</span><span class="sxs-lookup"><span data-stu-id="822df-154">1</span></span>        | <span data-ttu-id="822df-155">8</span><span class="sxs-lookup"><span data-stu-id="822df-155">8</span></span>                   |
| <span data-ttu-id="822df-156">7</span><span class="sxs-lookup"><span data-stu-id="822df-156">7</span></span>                  | <span data-ttu-id="822df-157">3</span><span class="sxs-lookup"><span data-stu-id="822df-157">3</span></span>        | <span data-ttu-id="822df-158">10</span><span class="sxs-lookup"><span data-stu-id="822df-158">10</span></span>                  |
| <span data-ttu-id="822df-159">10</span><span class="sxs-lookup"><span data-stu-id="822df-159">10</span></span>                 | <span data-ttu-id="822df-160">3</span><span class="sxs-lookup"><span data-stu-id="822df-160">3</span></span>        | <span data-ttu-id="822df-161">14</span><span class="sxs-lookup"><span data-stu-id="822df-161">14</span></span>                  |
| <span data-ttu-id="822df-162">14</span><span class="sxs-lookup"><span data-stu-id="822df-162">14</span></span>                 | <span data-ttu-id="822df-163">-3</span><span class="sxs-lookup"><span data-stu-id="822df-163">-3</span></span>       | <span data-ttu-id="822df-164">10</span><span class="sxs-lookup"><span data-stu-id="822df-164">10</span></span>                  |
| <span data-ttu-id="822df-165">28</span><span class="sxs-lookup"><span data-stu-id="822df-165">28</span></span>                 | <span data-ttu-id="822df-166">1</span><span class="sxs-lookup"><span data-stu-id="822df-166">1</span></span>        | <span data-ttu-id="822df-167">36</span><span class="sxs-lookup"><span data-stu-id="822df-167">36</span></span>                  |
| <span data-ttu-id="822df-168">28</span><span class="sxs-lookup"><span data-stu-id="822df-168">28</span></span>                 | <span data-ttu-id="822df-169">3</span><span class="sxs-lookup"><span data-stu-id="822df-169">3</span></span>        | <span data-ttu-id="822df-170">36</span><span class="sxs-lookup"><span data-stu-id="822df-170">36</span></span>                  |
| <span data-ttu-id="822df-171">80</span><span class="sxs-lookup"><span data-stu-id="822df-171">80</span></span>                 | <span data-ttu-id="822df-172">1</span><span class="sxs-lookup"><span data-stu-id="822df-172">1</span></span>        | <span data-ttu-id="822df-173">90</span><span class="sxs-lookup"><span data-stu-id="822df-173">90</span></span>                  |
| <span data-ttu-id="822df-174">80</span><span class="sxs-lookup"><span data-stu-id="822df-174">80</span></span>                 | <span data-ttu-id="822df-175">-1</span><span class="sxs-lookup"><span data-stu-id="822df-175">-1</span></span>       | <span data-ttu-id="822df-176">72</span><span class="sxs-lookup"><span data-stu-id="822df-176">72</span></span>                  |



 

## <a name="requirements"></a><span data-ttu-id="822df-177">規格需求</span><span class="sxs-lookup"><span data-stu-id="822df-177">Requirements</span></span>



| <span data-ttu-id="822df-178">需求</span><span class="sxs-lookup"><span data-stu-id="822df-178">Requirement</span></span> | <span data-ttu-id="822df-179">值</span><span class="sxs-lookup"><span data-stu-id="822df-179">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="822df-180">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="822df-180">Minimum supported client</span></span><br/> | <span data-ttu-id="822df-181">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="822df-181">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="822df-182">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="822df-182">Minimum supported server</span></span><br/> | <span data-ttu-id="822df-183">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="822df-183">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="822df-184">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="822df-184">Redistributable</span></span><br/>          | <span data-ttu-id="822df-185">Rich Edit 3。0</span><span class="sxs-lookup"><span data-stu-id="822df-185">Rich Edit 3.0</span></span><br/>                                                              |
| <span data-ttu-id="822df-186">標頭</span><span class="sxs-lookup"><span data-stu-id="822df-186">Header</span></span><br/>                   | <dl> <span data-ttu-id="822df-187"><dt>Richedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="822df-187"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="822df-188">另請參閱</span><span class="sxs-lookup"><span data-stu-id="822df-188">See also</span></span>

<dl> <dt>

<span data-ttu-id="822df-189">**參考**</span><span class="sxs-lookup"><span data-stu-id="822df-189">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="822df-190">**EM \_ GETCHARFORMAT**</span><span class="sxs-lookup"><span data-stu-id="822df-190">**EM\_GETCHARFORMAT**</span></span>](em-getcharformat.md)
</dt> <dt>

[<span data-ttu-id="822df-191">**CHARFORMAT2**</span><span class="sxs-lookup"><span data-stu-id="822df-191">**CHARFORMAT2**</span></span>](/windows/desktop/api/Richedit/ns-richedit-charformat2a)
</dt> <dt>

<span data-ttu-id="822df-192">**概念**</span><span class="sxs-lookup"><span data-stu-id="822df-192">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="822df-193">關於 Rich Edit 控制項</span><span class="sxs-lookup"><span data-stu-id="822df-193">About Rich Edit Controls</span></span>](about-rich-edit-controls.md)
</dt> </dl>

 

 





