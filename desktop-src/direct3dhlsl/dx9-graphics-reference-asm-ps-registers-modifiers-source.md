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
ms.openlocfilehash: a9dd4476dd7a1a885edb2e62a29b5127f5ff0a14
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/01/2021
ms.locfileid: "113129675"
---
# <a name="pixel-shader-source-register-modifiers"></a><span data-ttu-id="a281a-103">圖元著色器來源登錄修飾詞</span><span class="sxs-lookup"><span data-stu-id="a281a-103">Pixel Shader Source Register Modifiers</span></span>

<span data-ttu-id="a281a-104">在指令執行之前，請使用來源登錄修飾詞來變更從註冊程式讀取的值。</span><span class="sxs-lookup"><span data-stu-id="a281a-104">Use source register modifiers to change the value read from a register before an instruction runs.</span></span> <span data-ttu-id="a281a-105">來源暫存器的內容會保持不變。</span><span class="sxs-lookup"><span data-stu-id="a281a-105">The contents of a source register are left unchanged.</span></span> <span data-ttu-id="a281a-106">修飾詞可用來調整註冊資料的範圍，以準備進行指令。</span><span class="sxs-lookup"><span data-stu-id="a281a-106">Modifiers are useful for adjusting the range of register data in preparation for the instruction.</span></span> <span data-ttu-id="a281a-107">一組稱為選取器的修飾詞會從單一通道複製或複寫資料 (r、g、b、) 到其他通道。</span><span class="sxs-lookup"><span data-stu-id="a281a-107">A set of modifiers called selectors copies or replicates the data from a single channel (r,g,b,a) into the other channels.</span></span>

## <a name="ps_1_1---ps_1_4"></a><span data-ttu-id="a281a-108">ps \_ 1 \_ 1-ps \_ 1 \_ 4</span><span class="sxs-lookup"><span data-stu-id="a281a-108">ps\_1\_1 - ps\_1\_4</span></span>

<span data-ttu-id="a281a-109">下表列出支援每個修飾詞的版本：</span><span class="sxs-lookup"><span data-stu-id="a281a-109">This table identifies the versions that support each modifier:</span></span>



| <span data-ttu-id="a281a-110">來源暫存器修飾符</span><span class="sxs-lookup"><span data-stu-id="a281a-110">Source register modifiers</span></span>                                                                                    | <span data-ttu-id="a281a-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="a281a-111">Syntax</span></span>         | <span data-ttu-id="a281a-112">\_第1版</span><span class="sxs-lookup"><span data-stu-id="a281a-112">Version 1\_1</span></span> | <span data-ttu-id="a281a-113">\_第1版</span><span class="sxs-lookup"><span data-stu-id="a281a-113">Version 1\_2</span></span>     | <span data-ttu-id="a281a-114">第1版 \_</span><span class="sxs-lookup"><span data-stu-id="a281a-114">Version 1\_3</span></span>     | <span data-ttu-id="a281a-115">\_第1版</span><span class="sxs-lookup"><span data-stu-id="a281a-115">Version 1\_4</span></span>     |
|--------------------------------------------------------------------------------------------------------------|----------------|---------|------|------|------|
| [<span data-ttu-id="a281a-116">偏見</span><span class="sxs-lookup"><span data-stu-id="a281a-116">bias</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-bias.md)                                           | <span data-ttu-id="a281a-117">註冊 \_ 偏差</span><span class="sxs-lookup"><span data-stu-id="a281a-117">register\_bias</span></span> | <span data-ttu-id="a281a-118">X</span><span class="sxs-lookup"><span data-stu-id="a281a-118">X</span></span>       | <span data-ttu-id="a281a-119">X</span><span class="sxs-lookup"><span data-stu-id="a281a-119">X</span></span>    | <span data-ttu-id="a281a-120">X</span><span class="sxs-lookup"><span data-stu-id="a281a-120">X</span></span>    | <span data-ttu-id="a281a-121">X</span><span class="sxs-lookup"><span data-stu-id="a281a-121">X</span></span>    |
| [<span data-ttu-id="a281a-122">轉化</span><span class="sxs-lookup"><span data-stu-id="a281a-122">invert</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-invert.md)                                       | <span data-ttu-id="a281a-123">1-報名</span><span class="sxs-lookup"><span data-stu-id="a281a-123">1 - register</span></span>   | <span data-ttu-id="a281a-124">X</span><span class="sxs-lookup"><span data-stu-id="a281a-124">X</span></span>       | <span data-ttu-id="a281a-125">X</span><span class="sxs-lookup"><span data-stu-id="a281a-125">X</span></span>    | <span data-ttu-id="a281a-126">X</span><span class="sxs-lookup"><span data-stu-id="a281a-126">X</span></span>    | <span data-ttu-id="a281a-127">X</span><span class="sxs-lookup"><span data-stu-id="a281a-127">X</span></span>    |
| [<span data-ttu-id="a281a-128">negate</span><span class="sxs-lookup"><span data-stu-id="a281a-128">negate</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-negate.md)                                       | <span data-ttu-id="a281a-129">\- 註冊</span><span class="sxs-lookup"><span data-stu-id="a281a-129">\- register</span></span>    | <span data-ttu-id="a281a-130">X</span><span class="sxs-lookup"><span data-stu-id="a281a-130">X</span></span>       | <span data-ttu-id="a281a-131">X</span><span class="sxs-lookup"><span data-stu-id="a281a-131">X</span></span>    | <span data-ttu-id="a281a-132">X</span><span class="sxs-lookup"><span data-stu-id="a281a-132">X</span></span>    | <span data-ttu-id="a281a-133">X</span><span class="sxs-lookup"><span data-stu-id="a281a-133">X</span></span>    |
| [<span data-ttu-id="a281a-134">依2調整</span><span class="sxs-lookup"><span data-stu-id="a281a-134">scale by 2</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-scale-x2.md)                                 | <span data-ttu-id="a281a-135">註冊 \_ x2</span><span class="sxs-lookup"><span data-stu-id="a281a-135">register\_x2</span></span>   |         |      |      | <span data-ttu-id="a281a-136">X</span><span class="sxs-lookup"><span data-stu-id="a281a-136">X</span></span>    |
| [<span data-ttu-id="a281a-137">經過簽署的調整</span><span class="sxs-lookup"><span data-stu-id="a281a-137">signed scaling</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-signed-scale.md)                         | <span data-ttu-id="a281a-138">註冊 \_ bx2</span><span class="sxs-lookup"><span data-stu-id="a281a-138">register\_bx2</span></span>  | <span data-ttu-id="a281a-139">X</span><span class="sxs-lookup"><span data-stu-id="a281a-139">X</span></span>       | <span data-ttu-id="a281a-140">X</span><span class="sxs-lookup"><span data-stu-id="a281a-140">X</span></span>    | <span data-ttu-id="a281a-141">X</span><span class="sxs-lookup"><span data-stu-id="a281a-141">X</span></span>    | <span data-ttu-id="a281a-142">X</span><span class="sxs-lookup"><span data-stu-id="a281a-142">X</span></span>    |
| [<span data-ttu-id="a281a-143">texld 和 texcrd 修飾詞</span><span class="sxs-lookup"><span data-stu-id="a281a-143">texld and texcrd modifiers</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-ps-1-4.md)                   | <span data-ttu-id="a281a-144">註冊 \_ d\*</span><span class="sxs-lookup"><span data-stu-id="a281a-144">register\_d\*</span></span>  | <span data-ttu-id="a281a-145">X</span><span class="sxs-lookup"><span data-stu-id="a281a-145">X</span></span>       | <span data-ttu-id="a281a-146">X</span><span class="sxs-lookup"><span data-stu-id="a281a-146">X</span></span>    | <span data-ttu-id="a281a-147">X</span><span class="sxs-lookup"><span data-stu-id="a281a-147">X</span></span>    | <span data-ttu-id="a281a-148">X</span><span class="sxs-lookup"><span data-stu-id="a281a-148">X</span></span>    |
| [<span data-ttu-id="a281a-149">來源註冊 swizzling</span><span class="sxs-lookup"><span data-stu-id="a281a-149">source register swizzling</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md) | <span data-ttu-id="a281a-150">register. xyzw</span><span class="sxs-lookup"><span data-stu-id="a281a-150">register.xyzw</span></span>  | <span data-ttu-id="a281a-151">X</span><span class="sxs-lookup"><span data-stu-id="a281a-151">X</span></span>       | <span data-ttu-id="a281a-152">X</span><span class="sxs-lookup"><span data-stu-id="a281a-152">X</span></span>    | <span data-ttu-id="a281a-153">X</span><span class="sxs-lookup"><span data-stu-id="a281a-153">X</span></span>    | <span data-ttu-id="a281a-154">X</span><span class="sxs-lookup"><span data-stu-id="a281a-154">X</span></span>    |



 

<span data-ttu-id="a281a-155">來源暫存器修飾詞只能用於算術指令。</span><span class="sxs-lookup"><span data-stu-id="a281a-155">Source register modifiers can be used only on arithmetic instructions.</span></span> <span data-ttu-id="a281a-156">它們不能用於紋理位址指令。</span><span class="sxs-lookup"><span data-stu-id="a281a-156">They cannot be used on texture address instructions.</span></span> <span data-ttu-id="a281a-157">例外狀況是 [由 2](dx9-graphics-reference-asm-ps-registers-modifiers-scale-x2.md) 個修飾詞所調整。</span><span class="sxs-lookup"><span data-stu-id="a281a-157">The exception to this is the [scale by 2](dx9-graphics-reference-asm-ps-registers-modifiers-scale-x2.md) modifier.</span></span> <span data-ttu-id="a281a-158">針對第1版 \_ ，已簽署的小數位數可用於任何 texm 指令的來源引數 \* 。</span><span class="sxs-lookup"><span data-stu-id="a281a-158">For version 1\_1, signed scale can be used on the source argument of any texm\* instruction.</span></span> <span data-ttu-id="a281a-159">在第1版 \_ 或第1版 \_ 中，已簽署的小數位數可用於任何材質位址指令的來源引數。</span><span class="sxs-lookup"><span data-stu-id="a281a-159">For version 1\_2 or 1\_3, signed scale can be used on the source argument of any texture address instruction.</span></span>

<span data-ttu-id="a281a-160">部分修飾詞的特定限制：</span><span class="sxs-lookup"><span data-stu-id="a281a-160">Some modifier specific restrictions:</span></span>

-   <span data-ttu-id="a281a-161">您可以利用偏差、帶正負號的調整或 scalex2 修飾詞，將否定的符號結合在一起。</span><span class="sxs-lookup"><span data-stu-id="a281a-161">Negate can be combined with either the bias, signed scaling, or scalex2 modifier.</span></span> <span data-ttu-id="a281a-162">如果結合，則會最後執行否定。</span><span class="sxs-lookup"><span data-stu-id="a281a-162">When combined, negate is run last.</span></span>
-   <span data-ttu-id="a281a-163">反轉無法與任何其他修飾詞結合。</span><span class="sxs-lookup"><span data-stu-id="a281a-163">Invert cannot be combined with any other modifier.</span></span>
-   <span data-ttu-id="a281a-164">反轉、否定、偏差、帶正負號的調整和 scalex2 可以與任何選取器結合。</span><span class="sxs-lookup"><span data-stu-id="a281a-164">Invert, negate, bias, signed scaling, and scalex2 can be combined with any of the selectors.</span></span>
-   <span data-ttu-id="a281a-165">來源登錄修飾詞不應該用於常數暫存器，因為它們會導致未定義的結果。</span><span class="sxs-lookup"><span data-stu-id="a281a-165">Source register modifiers should not be used on constant registers because they will cause undefined results.</span></span> <span data-ttu-id="a281a-166">在第1版 \_ 中，不允許常數的修飾詞，而且驗證將會失敗。</span><span class="sxs-lookup"><span data-stu-id="a281a-166">For version 1\_4, modifiers on constants are not allowed and will fail validation.</span></span>

## <a name="ps_2_0-and-above"></a><span data-ttu-id="a281a-167">ps \_ 2 \_ 0 和更新版本</span><span class="sxs-lookup"><span data-stu-id="a281a-167">ps\_2\_0 and Above</span></span>

<span data-ttu-id="a281a-168">針對 ps \_ 2 \_ 0 和更新版本，修飾詞的數目已經過簡化。</span><span class="sxs-lookup"><span data-stu-id="a281a-168">For version ps\_2\_0 and up, the number of modifiers has been simplified.</span></span>

### <a name="negate"></a><span data-ttu-id="a281a-169">Negate</span><span class="sxs-lookup"><span data-stu-id="a281a-169">Negate</span></span>

<span data-ttu-id="a281a-170">否定來源暫存器的內容。</span><span class="sxs-lookup"><span data-stu-id="a281a-170">Negate the contents of the source register.</span></span>



| <span data-ttu-id="a281a-171">元件修飾詞</span><span class="sxs-lookup"><span data-stu-id="a281a-171">Component modifier</span></span> | <span data-ttu-id="a281a-172">描述</span><span class="sxs-lookup"><span data-stu-id="a281a-172">Description</span></span>     |
|--------------------|-----------------|
| <span data-ttu-id="a281a-173">\- R</span><span class="sxs-lookup"><span data-stu-id="a281a-173">\- r</span></span>               | <span data-ttu-id="a281a-174">來源否定</span><span class="sxs-lookup"><span data-stu-id="a281a-174">Source negation</span></span> |



 

<span data-ttu-id="a281a-175">否定修飾詞不能用在這些指示的第二個來源登錄上： [m3x2-ps](m3x2---ps.md)、 [m3x3-ps](m3x3---ps.md)、 [m3x4-ps](m3x4---ps.md)、 [m4x3-ps](m4x3---ps.md)和 [m4x4-ps](m4x4---ps.md)。</span><span class="sxs-lookup"><span data-stu-id="a281a-175">The negate modifier cannot be used on second source register of these instructions: [m3x2 - ps](m3x2---ps.md), [m3x3 - ps](m3x3---ps.md), [m3x4 - ps](m3x4---ps.md), [m4x3 - ps](m4x3---ps.md), and [m4x4 - ps](m4x4---ps.md).</span></span>



| <span data-ttu-id="a281a-176">圖元著色器版本</span><span class="sxs-lookup"><span data-stu-id="a281a-176">Pixel shader versions</span></span> | <span data-ttu-id="a281a-177">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a281a-177">2\_0</span></span> | <span data-ttu-id="a281a-178">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="a281a-178">2\_x</span></span> | <span data-ttu-id="a281a-179">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="a281a-179">2\_sw</span></span> | <span data-ttu-id="a281a-180">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a281a-180">3\_0</span></span> | <span data-ttu-id="a281a-181">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="a281a-181">3\_sw</span></span> |
|-----------------------|------|------|-------|------|-------|
| \-                    | <span data-ttu-id="a281a-182">x</span><span class="sxs-lookup"><span data-stu-id="a281a-182">x</span></span>    | <span data-ttu-id="a281a-183">x</span><span class="sxs-lookup"><span data-stu-id="a281a-183">x</span></span>    | <span data-ttu-id="a281a-184">x</span><span class="sxs-lookup"><span data-stu-id="a281a-184">x</span></span>     | <span data-ttu-id="a281a-185">x</span><span class="sxs-lookup"><span data-stu-id="a281a-185">x</span></span>    | <span data-ttu-id="a281a-186">x</span><span class="sxs-lookup"><span data-stu-id="a281a-186">x</span></span>     |



 

### <a name="absolute-value"></a><span data-ttu-id="a281a-187">絕對值</span><span class="sxs-lookup"><span data-stu-id="a281a-187">Absolute Value</span></span>

<span data-ttu-id="a281a-188">取得註冊的絕對值。</span><span class="sxs-lookup"><span data-stu-id="a281a-188">Take the absolute value of the register.</span></span>



| <span data-ttu-id="a281a-189">圖元著色器版本</span><span class="sxs-lookup"><span data-stu-id="a281a-189">Pixel shader versions</span></span> | <span data-ttu-id="a281a-190">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a281a-190">2\_0</span></span> | <span data-ttu-id="a281a-191">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="a281a-191">2\_x</span></span> | <span data-ttu-id="a281a-192">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="a281a-192">2\_sw</span></span> | <span data-ttu-id="a281a-193">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a281a-193">3\_0</span></span> | <span data-ttu-id="a281a-194">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="a281a-194">3\_sw</span></span> |
|-----------------------|------|------|-------|------|-------|
| <span data-ttu-id="a281a-195">abs</span><span class="sxs-lookup"><span data-stu-id="a281a-195">abs</span></span>                   |      |      |       | <span data-ttu-id="a281a-196">x</span><span class="sxs-lookup"><span data-stu-id="a281a-196">x</span></span>    | <span data-ttu-id="a281a-197">x</span><span class="sxs-lookup"><span data-stu-id="a281a-197">x</span></span>     |



 

<span data-ttu-id="a281a-198">如果任何第3版著色器從一或多個常數浮點數暫存器 (c \#) 讀取，下列其中一個條件必須為 true。</span><span class="sxs-lookup"><span data-stu-id="a281a-198">If any version 3 shader reads from one or more constant float registers (c\#), one of the following must be true.</span></span>

-   <span data-ttu-id="a281a-199">所有常數浮點數暫存器都必須使用 abs 修飾詞。</span><span class="sxs-lookup"><span data-stu-id="a281a-199">All of the constant floating-point registers must use the abs modifier.</span></span>
-   <span data-ttu-id="a281a-200">沒有常數浮點數暫存器可以使用 abs 修飾詞。</span><span class="sxs-lookup"><span data-stu-id="a281a-200">None of the constant floating-point registers can use the abs modifier.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a281a-201">相關主題</span><span class="sxs-lookup"><span data-stu-id="a281a-201">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a281a-202">圖元著色器暫存器修飾詞</span><span class="sxs-lookup"><span data-stu-id="a281a-202">Pixel Shader Register Modifiers</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers.md)
</dt> </dl>

 

 




