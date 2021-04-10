---
title: '轉換模式的旗標 (Ctffunc .h) '
description: 下列旗標可作為 GUID 區間 \_ \_ 鍵盤 \_ INPUTMODE 轉換的值 \_ 。 這相當於 IMM32 的輸入法 \_ CMODE 值。
ms.assetid: 6e545af5-5fdb-49de-b24e-aaee82b51326
keywords:
- 轉換模式文字服務架構的旗標
topic_type:
- apiref
api_name:
- Flags for Conversion Mode
api_location:
- Ctffunc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 022712ff45f213992bf3d40bd0149959e4864faa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104123"
---
# <a name="flags-for-conversion-mode"></a><span data-ttu-id="c7921-105">轉換模式的旗標</span><span class="sxs-lookup"><span data-stu-id="c7921-105">Flags for Conversion Mode</span></span>

<span data-ttu-id="c7921-106">下列旗標可作為 [GUID 區間 \_ \_ 鍵盤 \_ INPUTMODE \_ 轉換](predefined-compartments.md)的值。</span><span class="sxs-lookup"><span data-stu-id="c7921-106">The following flags are used as a value of [GUID\_COMPARTMENT\_KEYBOARD\_INPUTMODE\_CONVERSION](predefined-compartments.md).</span></span> <span data-ttu-id="c7921-107">這相當於 IMM32 的 [輸入法 \_ CMODE](../intl/ime-conversion-mode-values.md) 值。</span><span class="sxs-lookup"><span data-stu-id="c7921-107">This is equivalent with [IME\_CMODE](../intl/ime-conversion-mode-values.md) values for IMM32.</span></span>



| <span data-ttu-id="c7921-108">旗標</span><span class="sxs-lookup"><span data-stu-id="c7921-108">Flag</span></span>                             | <span data-ttu-id="c7921-109">值</span><span class="sxs-lookup"><span data-stu-id="c7921-109">Value</span></span>  | <span data-ttu-id="c7921-110">描述</span><span class="sxs-lookup"><span data-stu-id="c7921-110">Description</span></span>                                                     |
|----------------------------------|--------|-----------------------------------------------------------------|
| <span data-ttu-id="c7921-111">TF \_ CONVERSIONMODE 英 \_ 數位元</span><span class="sxs-lookup"><span data-stu-id="c7921-111">TF\_CONVERSIONMODE\_ALPHANUMERIC</span></span> | <span data-ttu-id="c7921-112">0x0000</span><span class="sxs-lookup"><span data-stu-id="c7921-112">0x0000</span></span> | <span data-ttu-id="c7921-113">如果是英數位元模式，則設為1。</span><span class="sxs-lookup"><span data-stu-id="c7921-113">Set to 1 if ALPHANUMERIC mode.</span></span>                                  |
| <span data-ttu-id="c7921-114">TF \_ CONVERSIONMODE \_ NATIVE</span><span class="sxs-lookup"><span data-stu-id="c7921-114">TF\_CONVERSIONMODE\_NATIVE</span></span>       | <span data-ttu-id="c7921-115">0x0001</span><span class="sxs-lookup"><span data-stu-id="c7921-115">0x0001</span></span> | <span data-ttu-id="c7921-116">如果原生模式，則設定為 1;若為英數位元模式，則為0。</span><span class="sxs-lookup"><span data-stu-id="c7921-116">Set to 1 if NATIVE mode; 0 if ALPHANUMERIC mode.</span></span>                |
| <span data-ttu-id="c7921-117">TF \_ CONVERSIONMODE \_ 片假名</span><span class="sxs-lookup"><span data-stu-id="c7921-117">TF\_CONVERSIONMODE\_KATAKANA</span></span>     | <span data-ttu-id="c7921-118">0x0002</span><span class="sxs-lookup"><span data-stu-id="c7921-118">0x0002</span></span> | <span data-ttu-id="c7921-119">若為片假名模式，則設定為 1;若為平假名模式，則為0。</span><span class="sxs-lookup"><span data-stu-id="c7921-119">Set to 1 if KATAKANA mode; 0 if HIRAGANA mode.</span></span>                  |
| <span data-ttu-id="c7921-120">TF \_ CONVERSIONMODE \_ FULLSHAPE</span><span class="sxs-lookup"><span data-stu-id="c7921-120">TF\_CONVERSIONMODE\_FULLSHAPE</span></span>    | <span data-ttu-id="c7921-121">0x0008</span><span class="sxs-lookup"><span data-stu-id="c7921-121">0x0008</span></span> | <span data-ttu-id="c7921-122">如果全圖形模式，則設定為 1;如果為半形狀模式，則為0。</span><span class="sxs-lookup"><span data-stu-id="c7921-122">Set to 1 if full shape mode; 0 if half shape mode.</span></span>              |
| <span data-ttu-id="c7921-123">TF \_ CONVERSIONMODE \_ 羅馬</span><span class="sxs-lookup"><span data-stu-id="c7921-123">TF\_CONVERSIONMODE\_ROMAN</span></span>        | <span data-ttu-id="c7921-124">0x0010</span><span class="sxs-lookup"><span data-stu-id="c7921-124">0x0010</span></span> | <span data-ttu-id="c7921-125">設定為1以防止依 IME 處理轉換;如果沒有，則為0。</span><span class="sxs-lookup"><span data-stu-id="c7921-125">Set to 1 to prevent processing of conversions by IME; 0 if not.</span></span> |
| <span data-ttu-id="c7921-126">TF \_ CONVERSIONMODE \_ CHARCODE</span><span class="sxs-lookup"><span data-stu-id="c7921-126">TF\_CONVERSIONMODE\_CHARCODE</span></span>     | <span data-ttu-id="c7921-127">0x0020</span><span class="sxs-lookup"><span data-stu-id="c7921-127">0x0020</span></span> | <span data-ttu-id="c7921-128">如果字元碼輸入模式，則設定為 1;如果沒有，則為0。</span><span class="sxs-lookup"><span data-stu-id="c7921-128">Set to 1 if character code input mode; 0 if not.</span></span>                |
| <span data-ttu-id="c7921-129">TF \_ CONVERSIONMODE \_ SOFTKEYBOARD</span><span class="sxs-lookup"><span data-stu-id="c7921-129">TF\_CONVERSIONMODE\_SOFTKEYBOARD</span></span> | <span data-ttu-id="c7921-130">0x0080</span><span class="sxs-lookup"><span data-stu-id="c7921-130">0x0080</span></span> | <span data-ttu-id="c7921-131">如果軟鍵盤模式，則設定為 1;如果沒有，則為0。</span><span class="sxs-lookup"><span data-stu-id="c7921-131">Set to 1 if Soft Keyboard mode; 0 if not.</span></span>                       |
| <span data-ttu-id="c7921-132">TF \_ CONVERSIONMODE \_ NOCONVERSION</span><span class="sxs-lookup"><span data-stu-id="c7921-132">TF\_CONVERSIONMODE\_NOCONVERSION</span></span> | <span data-ttu-id="c7921-133">0x0100</span><span class="sxs-lookup"><span data-stu-id="c7921-133">0x0100</span></span> | <span data-ttu-id="c7921-134">設定為1以防止依 IME 處理轉換;如果沒有，則為0。</span><span class="sxs-lookup"><span data-stu-id="c7921-134">Set to 1 to prevent processing of conversions by IME; 0 if not.</span></span> |
| <span data-ttu-id="c7921-135">TF \_ CONVERSIONMODE \_ 符號</span><span class="sxs-lookup"><span data-stu-id="c7921-135">TF\_CONVERSIONMODE\_SYMBOL</span></span>       | <span data-ttu-id="c7921-136">0x0400</span><span class="sxs-lookup"><span data-stu-id="c7921-136">0x0400</span></span> | <span data-ttu-id="c7921-137">如果符號轉換模式，則設定為 1;如果沒有，則為0。</span><span class="sxs-lookup"><span data-stu-id="c7921-137">Set to 1 if SYMBOL conversion mode; 0 if not.</span></span>                   |
| <span data-ttu-id="c7921-138">TF \_ CONVERSIONMODE 已 \_ 修正</span><span class="sxs-lookup"><span data-stu-id="c7921-138">TF\_CONVERSIONMODE\_FIXED</span></span>        | <span data-ttu-id="c7921-139">0x0800</span><span class="sxs-lookup"><span data-stu-id="c7921-139">0x0800</span></span> | <span data-ttu-id="c7921-140">如果固定的轉換模式，則設定為 1;如果沒有，則為0。</span><span class="sxs-lookup"><span data-stu-id="c7921-140">Set to 1 if fixed conversion mode; 0 if not.</span></span>                    |



 

<span data-ttu-id="c7921-141">下列值會當做 [GUID 區間 \_ \_ 鍵盤 \_ INPUTMODE \_ 句子](predefined-compartments.md)的值使用。</span><span class="sxs-lookup"><span data-stu-id="c7921-141">The following values are used as a value of [GUID\_COMPARTMENT\_KEYBOARD\_INPUTMODE\_SENTENCE](predefined-compartments.md).</span></span> <span data-ttu-id="c7921-142">這相當於 IMM32 的 [輸入法 \_ SMODE](../intl/ime-composition-string-values.md) 值。</span><span class="sxs-lookup"><span data-stu-id="c7921-142">This is equivalent with [IME\_SMODE](../intl/ime-composition-string-values.md) values for IMM32.</span></span>



| <span data-ttu-id="c7921-143">旗標</span><span class="sxs-lookup"><span data-stu-id="c7921-143">Flag</span></span>                            | <span data-ttu-id="c7921-144">值</span><span class="sxs-lookup"><span data-stu-id="c7921-144">Value</span></span>  | <span data-ttu-id="c7921-145">描述</span><span class="sxs-lookup"><span data-stu-id="c7921-145">Description</span></span>                                                                |
|---------------------------------|--------|----------------------------------------------------------------------------|
| <span data-ttu-id="c7921-146">TF \_ SENTENCEMODE \_ NONE</span><span class="sxs-lookup"><span data-stu-id="c7921-146">TF\_SENTENCEMODE\_NONE</span></span>          | <span data-ttu-id="c7921-147">0x0000</span><span class="sxs-lookup"><span data-stu-id="c7921-147">0x0000</span></span> | <span data-ttu-id="c7921-148">沒有句子的資訊。</span><span class="sxs-lookup"><span data-stu-id="c7921-148">No information for sentence.</span></span>                                               |
| <span data-ttu-id="c7921-149">TF \_ SENTENCEMODE \_ PLAURALCLAUSE</span><span class="sxs-lookup"><span data-stu-id="c7921-149">TF\_SENTENCEMODE\_PLAURALCLAUSE</span></span> | <span data-ttu-id="c7921-150">0x0001</span><span class="sxs-lookup"><span data-stu-id="c7921-150">0x0001</span></span> | <span data-ttu-id="c7921-151">IME 使用複數子句資訊來執行轉換處理。</span><span class="sxs-lookup"><span data-stu-id="c7921-151">The IME uses plural clause information to carry out conversion processing.</span></span> |
| <span data-ttu-id="c7921-152">TF \_ SENTENCEMODE \_ SINGLECONVERT</span><span class="sxs-lookup"><span data-stu-id="c7921-152">TF\_SENTENCEMODE\_SINGLECONVERT</span></span> | <span data-ttu-id="c7921-153">0x0002</span><span class="sxs-lookup"><span data-stu-id="c7921-153">0x0002</span></span> | <span data-ttu-id="c7921-154">IME 會以單一字元模式執行轉換處理。</span><span class="sxs-lookup"><span data-stu-id="c7921-154">The IME carries out conversion processing in single-character mode.</span></span>        |
| <span data-ttu-id="c7921-155">TF \_ SENTENCEMODE \_ 自動</span><span class="sxs-lookup"><span data-stu-id="c7921-155">TF\_SENTENCEMODE\_AUTOMATIC</span></span>     | <span data-ttu-id="c7921-156">0x0004</span><span class="sxs-lookup"><span data-stu-id="c7921-156">0x0004</span></span> | <span data-ttu-id="c7921-157">IME 會在自動模式中執行轉換處理。</span><span class="sxs-lookup"><span data-stu-id="c7921-157">The IME carries out conversion processing in automatic mode.</span></span>               |
| <span data-ttu-id="c7921-158">TF \_ SENTENCEMODE \_ PHRASEPREDICT</span><span class="sxs-lookup"><span data-stu-id="c7921-158">TF\_SENTENCEMODE\_PHRASEPREDICT</span></span> | <span data-ttu-id="c7921-159">0x0008</span><span class="sxs-lookup"><span data-stu-id="c7921-159">0x0008</span></span> | <span data-ttu-id="c7921-160">IME 會使用片語資訊來預測下一個字元。</span><span class="sxs-lookup"><span data-stu-id="c7921-160">The IME uses phrase information to predict the next character.</span></span>             |
| <span data-ttu-id="c7921-161">TF \_ SENTENCEMODE \_ 對話</span><span class="sxs-lookup"><span data-stu-id="c7921-161">TF\_SENTENCEMODE\_CONVERSATION</span></span>  | <span data-ttu-id="c7921-162">0x0010</span><span class="sxs-lookup"><span data-stu-id="c7921-162">0x0010</span></span> | <span data-ttu-id="c7921-163">IME 使用交談模式。</span><span class="sxs-lookup"><span data-stu-id="c7921-163">The IME uses conversation mode.</span></span> <span data-ttu-id="c7921-164">這對聊天應用程式很有用。</span><span class="sxs-lookup"><span data-stu-id="c7921-164">This is useful for chat applications.</span></span>      |



 

## <a name="requirements"></a><span data-ttu-id="c7921-165">規格需求</span><span class="sxs-lookup"><span data-stu-id="c7921-165">Requirements</span></span>



| <span data-ttu-id="c7921-166">需求</span><span class="sxs-lookup"><span data-stu-id="c7921-166">Requirement</span></span> | <span data-ttu-id="c7921-167">值</span><span class="sxs-lookup"><span data-stu-id="c7921-167">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c7921-168">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c7921-168">Minimum supported client</span></span><br/> | <span data-ttu-id="c7921-169">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c7921-169">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="c7921-170">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c7921-170">Minimum supported server</span></span><br/> | <span data-ttu-id="c7921-171">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c7921-171">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="c7921-172">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="c7921-172">Redistributable</span></span><br/>          | <span data-ttu-id="c7921-173">TSF 1.0 于 windows NT 4.0、Windows 2000 ProfessionalandWindows MeWindows 98</span><span class="sxs-lookup"><span data-stu-id="c7921-173">TSF 1.0 onWindows NT 4.0,Windows 2000 ProfessionalandWindows MeWindows 98</span></span><br/>   |
| <span data-ttu-id="c7921-174">標頭</span><span class="sxs-lookup"><span data-stu-id="c7921-174">Header</span></span><br/>                   | <dl> <span data-ttu-id="c7921-175"><dt>Ctffunc。h</dt></span><span class="sxs-lookup"><span data-stu-id="c7921-175"><dt>Ctffunc.h</dt></span></span> </dl>   |
| <span data-ttu-id="c7921-176">Idl</span><span class="sxs-lookup"><span data-stu-id="c7921-176">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c7921-177"><dt>Ctffunc .idl</dt></span><span class="sxs-lookup"><span data-stu-id="c7921-177"><dt>Ctffunc.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7921-178">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c7921-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7921-179">預先定義的區間</span><span class="sxs-lookup"><span data-stu-id="c7921-179">Predefined Compartments</span></span>](predefined-compartments.md)
</dt> </dl>

 

