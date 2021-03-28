---
title: 圖元著色器來源登錄修飾詞
description: 在指令執行之前，請使用來源登錄修飾詞來變更從註冊程式讀取的值。
ms.assetid: b45d0919-7878-4184-ad4a-5623aae9d1f1
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 12cfee533a71408a445d97a63bbd8b76b281236b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311492"
---
# <a name="pixel-shader-source-register-modifiers"></a><span data-ttu-id="9a74f-103">圖元著色器來源登錄修飾詞</span><span class="sxs-lookup"><span data-stu-id="9a74f-103">Pixel Shader Source Register Modifiers</span></span>

<span data-ttu-id="9a74f-104">在指令執行之前，請使用來源登錄修飾詞來變更從註冊程式讀取的值。</span><span class="sxs-lookup"><span data-stu-id="9a74f-104">Use source register modifiers to change the value read from a register before an instruction runs.</span></span> <span data-ttu-id="9a74f-105">來源暫存器的內容會保持不變。</span><span class="sxs-lookup"><span data-stu-id="9a74f-105">The contents of a source register are left unchanged.</span></span> <span data-ttu-id="9a74f-106">修飾詞可用來調整註冊資料的範圍，以準備進行指令。</span><span class="sxs-lookup"><span data-stu-id="9a74f-106">Modifiers are useful for adjusting the range of register data in preparation for the instruction.</span></span> <span data-ttu-id="9a74f-107">一組稱為選取器的修飾詞會從單一通道複製或複寫資料 (r、g、b、) 到其他通道。</span><span class="sxs-lookup"><span data-stu-id="9a74f-107">A set of modifiers called selectors copies or replicates the data from a single channel (r,g,b,a) into the other channels.</span></span>

## <a name="ps_1_1---ps_1_4"></a><span data-ttu-id="9a74f-108">ps \_ 1 \_ 1-ps \_ 1 \_ 4</span><span class="sxs-lookup"><span data-stu-id="9a74f-108">ps\_1\_1 - ps\_1\_4</span></span>

<span data-ttu-id="9a74f-109">下表列出支援每個修飾詞的版本：</span><span class="sxs-lookup"><span data-stu-id="9a74f-109">This table identifies the versions that support each modifier:</span></span>



| <span data-ttu-id="9a74f-110">來源暫存器修飾符</span><span class="sxs-lookup"><span data-stu-id="9a74f-110">Source register modifiers</span></span>                                                                                    | <span data-ttu-id="9a74f-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="9a74f-111">Syntax</span></span>         | <span data-ttu-id="9a74f-112">版本</span><span class="sxs-lookup"><span data-stu-id="9a74f-112">Version</span></span> |      |      |      |     |     |
|--------------------------------------------------------------------------------------------------------------|----------------|---------|------|------|------|-----|-----|
|                                                                                                              |                | <span data-ttu-id="9a74f-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="9a74f-113">1\_1</span></span>    | <span data-ttu-id="9a74f-114">1\_2</span><span class="sxs-lookup"><span data-stu-id="9a74f-114">1\_2</span></span> | <span data-ttu-id="9a74f-115">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="9a74f-115">1\_3</span></span> | <span data-ttu-id="9a74f-116">1\_4</span><span class="sxs-lookup"><span data-stu-id="9a74f-116">1\_4</span></span> |     |     |
| [<span data-ttu-id="9a74f-117">偏見</span><span class="sxs-lookup"><span data-stu-id="9a74f-117">bias</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-bias.md)                                           | <span data-ttu-id="9a74f-118">註冊 \_ 偏差</span><span class="sxs-lookup"><span data-stu-id="9a74f-118">register\_bias</span></span> | <span data-ttu-id="9a74f-119">X</span><span class="sxs-lookup"><span data-stu-id="9a74f-119">X</span></span>       | <span data-ttu-id="9a74f-120">X</span><span class="sxs-lookup"><span data-stu-id="9a74f-120">X</span></span>    | <span data-ttu-id="9a74f-121">X</span><span class="sxs-lookup"><span data-stu-id="9a74f-121">X</span></span>    | <span data-ttu-id="9a74f-122">X</span><span class="sxs-lookup"><span data-stu-id="9a74f-122">X</span></span>    |     |     |
| [<span data-ttu-id="9a74f-123">轉化</span><span class="sxs-lookup"><span data-stu-id="9a74f-123">invert</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-invert.md)                                       | <span data-ttu-id="9a74f-124">1-報名</span><span class="sxs-lookup"><span data-stu-id="9a74f-124">1 - register</span></span>   | <span data-ttu-id="9a74f-125">X</span><span class="sxs-lookup"><span data-stu-id="9a74f-125">X</span></span>       | <span data-ttu-id="9a74f-126">X</span><span class="sxs-lookup"><span data-stu-id="9a74f-126">X</span></span>    | <span data-ttu-id="9a74f-127">X</span><span class="sxs-lookup"><span data-stu-id="9a74f-127">X</span></span>    | <span data-ttu-id="9a74f-128">X</span><span class="sxs-lookup"><span data-stu-id="9a74f-128">X</span></span>    |     |     |
| [<span data-ttu-id="9a74f-129">negate</span><span class="sxs-lookup"><span data-stu-id="9a74f-129">negate</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-negate.md)                                       | <span data-ttu-id="9a74f-130">\- 註冊</span><span class="sxs-lookup"><span data-stu-id="9a74f-130">\- register</span></span>    | <span data-ttu-id="9a74f-131">X</span><span class="sxs-lookup"><span data-stu-id="9a74f-131">X</span></span>       | <span data-ttu-id="9a74f-132">X</span><span class="sxs-lookup"><span data-stu-id="9a74f-132">X</span></span>    | <span data-ttu-id="9a74f-133">X</span><span class="sxs-lookup"><span data-stu-id="9a74f-133">X</span></span>    | <span data-ttu-id="9a74f-134">X</span><span class="sxs-lookup"><span data-stu-id="9a74f-134">X</span></span>    |     |     |
| [<span data-ttu-id="9a74f-135">依2調整</span><span class="sxs-lookup"><span data-stu-id="9a74f-135">scale by 2</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-scale-x2.md)                                 | <span data-ttu-id="9a74f-136">註冊 \_ x2</span><span class="sxs-lookup"><span data-stu-id="9a74f-136">register\_x2</span></span>   |         |      |      | <span data-ttu-id="9a74f-137">X</span><span class="sxs-lookup"><span data-stu-id="9a74f-137">X</span></span>    |     |     |
| [<span data-ttu-id="9a74f-138">經過簽署的調整</span><span class="sxs-lookup"><span data-stu-id="9a74f-138">signed scaling</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-signed-scale.md)                         | <span data-ttu-id="9a74f-139">註冊 \_ bx2</span><span class="sxs-lookup"><span data-stu-id="9a74f-139">register\_bx2</span></span>  | <span data-ttu-id="9a74f-140">X</span><span class="sxs-lookup"><span data-stu-id="9a74f-140">X</span></span>       | <span data-ttu-id="9a74f-141">X</span><span class="sxs-lookup"><span data-stu-id="9a74f-141">X</span></span>    | <span data-ttu-id="9a74f-142">X</span><span class="sxs-lookup"><span data-stu-id="9a74f-142">X</span></span>    | <span data-ttu-id="9a74f-143">X</span><span class="sxs-lookup"><span data-stu-id="9a74f-143">X</span></span>    |     |     |
| [<span data-ttu-id="9a74f-144">texld 和 texcrd 修飾詞</span><span class="sxs-lookup"><span data-stu-id="9a74f-144">texld and texcrd modifiers</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-ps-1-4.md)                   | <span data-ttu-id="9a74f-145">註冊 \_ d\*</span><span class="sxs-lookup"><span data-stu-id="9a74f-145">register\_d\*</span></span>  | <span data-ttu-id="9a74f-146">X</span><span class="sxs-lookup"><span data-stu-id="9a74f-146">X</span></span>       | <span data-ttu-id="9a74f-147">X</span><span class="sxs-lookup"><span data-stu-id="9a74f-147">X</span></span>    | <span data-ttu-id="9a74f-148">X</span><span class="sxs-lookup"><span data-stu-id="9a74f-148">X</span></span>    | <span data-ttu-id="9a74f-149">X</span><span class="sxs-lookup"><span data-stu-id="9a74f-149">X</span></span>    |     |     |
| [<span data-ttu-id="9a74f-150">來源註冊 swizzling</span><span class="sxs-lookup"><span data-stu-id="9a74f-150">source register swizzling</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md) | <span data-ttu-id="9a74f-151">register. xyzw</span><span class="sxs-lookup"><span data-stu-id="9a74f-151">register.xyzw</span></span>  | <span data-ttu-id="9a74f-152">X</span><span class="sxs-lookup"><span data-stu-id="9a74f-152">X</span></span>       | <span data-ttu-id="9a74f-153">X</span><span class="sxs-lookup"><span data-stu-id="9a74f-153">X</span></span>    | <span data-ttu-id="9a74f-154">X</span><span class="sxs-lookup"><span data-stu-id="9a74f-154">X</span></span>    | <span data-ttu-id="9a74f-155">X</span><span class="sxs-lookup"><span data-stu-id="9a74f-155">X</span></span>    |     |     |



 

<span data-ttu-id="9a74f-156">來源暫存器修飾詞只能用於算術指令。</span><span class="sxs-lookup"><span data-stu-id="9a74f-156">Source register modifiers can be used only on arithmetic instructions.</span></span> <span data-ttu-id="9a74f-157">它們不能用於紋理位址指令。</span><span class="sxs-lookup"><span data-stu-id="9a74f-157">They cannot be used on texture address instructions.</span></span> <span data-ttu-id="9a74f-158">例外狀況是 [由 2](dx9-graphics-reference-asm-ps-registers-modifiers-scale-x2.md) 個修飾詞所調整。</span><span class="sxs-lookup"><span data-stu-id="9a74f-158">The exception to this is the [scale by 2](dx9-graphics-reference-asm-ps-registers-modifiers-scale-x2.md) modifier.</span></span> <span data-ttu-id="9a74f-159">針對第1版 \_ ，已簽署的小數位數可用於任何 texm 指令的來源引數 \* 。</span><span class="sxs-lookup"><span data-stu-id="9a74f-159">For version 1\_1, signed scale can be used on the source argument of any texm\* instruction.</span></span> <span data-ttu-id="9a74f-160">在第1版 \_ 或第1版 \_ 中，已簽署的小數位數可用於任何材質位址指令的來源引數。</span><span class="sxs-lookup"><span data-stu-id="9a74f-160">For version 1\_2 or 1\_3, signed scale can be used on the source argument of any texture address instruction.</span></span>

<span data-ttu-id="9a74f-161">部分修飾詞的特定限制：</span><span class="sxs-lookup"><span data-stu-id="9a74f-161">Some modifier specific restrictions:</span></span>

-   <span data-ttu-id="9a74f-162">您可以利用偏差、帶正負號的調整或 scalex2 修飾詞，將否定的符號結合在一起。</span><span class="sxs-lookup"><span data-stu-id="9a74f-162">Negate can be combined with either the bias, signed scaling, or scalex2 modifier.</span></span> <span data-ttu-id="9a74f-163">如果結合，則會最後執行否定。</span><span class="sxs-lookup"><span data-stu-id="9a74f-163">When combined, negate is run last.</span></span>
-   <span data-ttu-id="9a74f-164">反轉無法與任何其他修飾詞結合。</span><span class="sxs-lookup"><span data-stu-id="9a74f-164">Invert cannot be combined with any other modifier.</span></span>
-   <span data-ttu-id="9a74f-165">反轉、否定、偏差、帶正負號的調整和 scalex2 可以與任何選取器結合。</span><span class="sxs-lookup"><span data-stu-id="9a74f-165">Invert, negate, bias, signed scaling, and scalex2 can be combined with any of the selectors.</span></span>
-   <span data-ttu-id="9a74f-166">來源登錄修飾詞不應該用於常數暫存器，因為它們會導致未定義的結果。</span><span class="sxs-lookup"><span data-stu-id="9a74f-166">Source register modifiers should not be used on constant registers because they will cause undefined results.</span></span> <span data-ttu-id="9a74f-167">在第1版 \_ 中，不允許常數的修飾詞，而且驗證將會失敗。</span><span class="sxs-lookup"><span data-stu-id="9a74f-167">For version 1\_4, modifiers on constants are not allowed and will fail validation.</span></span>

## <a name="ps_2_0-and-above"></a><span data-ttu-id="9a74f-168">ps \_ 2 \_ 0 和更新版本</span><span class="sxs-lookup"><span data-stu-id="9a74f-168">ps\_2\_0 and Above</span></span>

<span data-ttu-id="9a74f-169">針對 ps \_ 2 \_ 0 和更新版本，修飾詞的數目已經過簡化。</span><span class="sxs-lookup"><span data-stu-id="9a74f-169">For version ps\_2\_0 and up, the number of modifiers has been simplified.</span></span>

### <a name="negate"></a><span data-ttu-id="9a74f-170">Negate</span><span class="sxs-lookup"><span data-stu-id="9a74f-170">Negate</span></span>

<span data-ttu-id="9a74f-171">否定來源暫存器的內容。</span><span class="sxs-lookup"><span data-stu-id="9a74f-171">Negate the contents of the source register.</span></span>



| <span data-ttu-id="9a74f-172">元件修飾詞</span><span class="sxs-lookup"><span data-stu-id="9a74f-172">Component modifier</span></span> | <span data-ttu-id="9a74f-173">Description</span><span class="sxs-lookup"><span data-stu-id="9a74f-173">Description</span></span>     |
|--------------------|-----------------|
| <span data-ttu-id="9a74f-174">\- R</span><span class="sxs-lookup"><span data-stu-id="9a74f-174">\- r</span></span>               | <span data-ttu-id="9a74f-175">來源否定</span><span class="sxs-lookup"><span data-stu-id="9a74f-175">Source negation</span></span> |



 

<span data-ttu-id="9a74f-176">否定修飾詞不能用在這些指示的第二個來源登錄上： [m3x2-ps](m3x2---ps.md)、 [m3x3-ps](m3x3---ps.md)、 [m3x4-ps](m3x4---ps.md)、 [m4x3-ps](m4x3---ps.md)和 [m4x4-ps](m4x4---ps.md)。</span><span class="sxs-lookup"><span data-stu-id="9a74f-176">The negate modifier cannot be used on second source register of these instructions: [m3x2 - ps](m3x2---ps.md), [m3x3 - ps](m3x3---ps.md), [m3x4 - ps](m3x4---ps.md), [m4x3 - ps](m4x3---ps.md), and [m4x4 - ps](m4x4---ps.md).</span></span>



| <span data-ttu-id="9a74f-177">圖元著色器版本</span><span class="sxs-lookup"><span data-stu-id="9a74f-177">Pixel shader versions</span></span> | <span data-ttu-id="9a74f-178">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="9a74f-178">2\_0</span></span> | <span data-ttu-id="9a74f-179">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="9a74f-179">2\_x</span></span> | <span data-ttu-id="9a74f-180">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="9a74f-180">2\_sw</span></span> | <span data-ttu-id="9a74f-181">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="9a74f-181">3\_0</span></span> | <span data-ttu-id="9a74f-182">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="9a74f-182">3\_sw</span></span> |
|-----------------------|------|------|-------|------|-------|
| \-                    | <span data-ttu-id="9a74f-183">x</span><span class="sxs-lookup"><span data-stu-id="9a74f-183">x</span></span>    | <span data-ttu-id="9a74f-184">x</span><span class="sxs-lookup"><span data-stu-id="9a74f-184">x</span></span>    | <span data-ttu-id="9a74f-185">x</span><span class="sxs-lookup"><span data-stu-id="9a74f-185">x</span></span>     | <span data-ttu-id="9a74f-186">x</span><span class="sxs-lookup"><span data-stu-id="9a74f-186">x</span></span>    | <span data-ttu-id="9a74f-187">x</span><span class="sxs-lookup"><span data-stu-id="9a74f-187">x</span></span>     |



 

### <a name="absolute-value"></a><span data-ttu-id="9a74f-188">絕對值</span><span class="sxs-lookup"><span data-stu-id="9a74f-188">Absolute Value</span></span>

<span data-ttu-id="9a74f-189">取得註冊的絕對值。</span><span class="sxs-lookup"><span data-stu-id="9a74f-189">Take the absolute value of the register.</span></span>



| <span data-ttu-id="9a74f-190">圖元著色器版本</span><span class="sxs-lookup"><span data-stu-id="9a74f-190">Pixel shader versions</span></span> | <span data-ttu-id="9a74f-191">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="9a74f-191">2\_0</span></span> | <span data-ttu-id="9a74f-192">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="9a74f-192">2\_x</span></span> | <span data-ttu-id="9a74f-193">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="9a74f-193">2\_sw</span></span> | <span data-ttu-id="9a74f-194">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="9a74f-194">3\_0</span></span> | <span data-ttu-id="9a74f-195">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="9a74f-195">3\_sw</span></span> |
|-----------------------|------|------|-------|------|-------|
| <span data-ttu-id="9a74f-196">abs</span><span class="sxs-lookup"><span data-stu-id="9a74f-196">abs</span></span>                   |      |      |       | <span data-ttu-id="9a74f-197">x</span><span class="sxs-lookup"><span data-stu-id="9a74f-197">x</span></span>    | <span data-ttu-id="9a74f-198">x</span><span class="sxs-lookup"><span data-stu-id="9a74f-198">x</span></span>     |



 

<span data-ttu-id="9a74f-199">如果任何第3版著色器從一或多個常數浮點數暫存器 (c \#) 讀取，下列其中一個條件必須為 true。</span><span class="sxs-lookup"><span data-stu-id="9a74f-199">If any version 3 shader reads from one or more constant float registers (c\#), one of the following must be true.</span></span>

-   <span data-ttu-id="9a74f-200">所有常數浮點數暫存器都必須使用 abs 修飾詞。</span><span class="sxs-lookup"><span data-stu-id="9a74f-200">All of the constant floating-point registers must use the abs modifier.</span></span>
-   <span data-ttu-id="9a74f-201">沒有常數浮點數暫存器可以使用 abs 修飾詞。</span><span class="sxs-lookup"><span data-stu-id="9a74f-201">None of the constant floating-point registers can use the abs modifier.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9a74f-202">相關主題</span><span class="sxs-lookup"><span data-stu-id="9a74f-202">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9a74f-203">圖元著色器暫存器修飾詞</span><span class="sxs-lookup"><span data-stu-id="9a74f-203">Pixel Shader Register Modifiers</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers.md)
</dt> </dl>

 

 




