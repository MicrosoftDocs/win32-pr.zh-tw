---
title: '來源註冊 swizzling (HLSL PS 參考) '
description: Swizzling 是指將任何來源暫存器元件複製到任何暫存登錄元件的能力。 Swizzling 不會影響來源註冊資料。 在執行指令之前，會將來源暫存器中的資料複製到臨時暫存器。
ms.assetid: 27aee6a8-5185-4236-b3e4-44addf230c34
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4ffc655129740f112a3ade9eb40c0bbe29dfc1fb
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/23/2019
ms.locfileid: "104313791"
---
# <a name="source-register-swizzling-hlsl-ps-reference"></a><span data-ttu-id="bbc9a-105">來源註冊 swizzling (HLSL PS 參考) </span><span class="sxs-lookup"><span data-stu-id="bbc9a-105">Source register swizzling (HLSL PS reference)</span></span>

<span data-ttu-id="bbc9a-106">Swizzling 是指將任何來源暫存器元件複製到任何暫存登錄元件的能力。</span><span class="sxs-lookup"><span data-stu-id="bbc9a-106">Swizzling refers to the ability to copy any source register component to any temporary register component.</span></span> <span data-ttu-id="bbc9a-107">Swizzling 不會影響來源註冊資料。</span><span class="sxs-lookup"><span data-stu-id="bbc9a-107">Swizzling does not affect the source register data.</span></span> <span data-ttu-id="bbc9a-108">在執行指令之前，會將來源暫存器中的資料複製到臨時暫存器。</span><span class="sxs-lookup"><span data-stu-id="bbc9a-108">Before an instruction runs, the data in a source register is copied to a temporary register.</span></span>

## <a name="source-swizzling"></a><span data-ttu-id="bbc9a-109">來源 Swizzling</span><span class="sxs-lookup"><span data-stu-id="bbc9a-109">Source Swizzling</span></span>

<span data-ttu-id="bbc9a-110">來源 swizzle 可讓來源暫存器的個別元件採用相同來源暫存器中任何四個元件的值，然後再讀取註冊來進行計算。</span><span class="sxs-lookup"><span data-stu-id="bbc9a-110">Source swizzle allows individual component of a source register to take on the value of any of the four components of the same source register before the register is read for computation.</span></span>

<span data-ttu-id="bbc9a-111">例如，zxxy swizzle 表示：</span><span class="sxs-lookup"><span data-stu-id="bbc9a-111">For example, the .zxxy swizzle means:</span></span>

-   <span data-ttu-id="bbc9a-112">. x 元件會取得. z 元件的值</span><span class="sxs-lookup"><span data-stu-id="bbc9a-112">.x component will take on the value of .z component</span></span>
-   <span data-ttu-id="bbc9a-113">. y 元件會取得. x 元件的值</span><span class="sxs-lookup"><span data-stu-id="bbc9a-113">.y component will take on the value of .x component</span></span>
-   <span data-ttu-id="bbc9a-114">. z 元件會取得. x 元件的值</span><span class="sxs-lookup"><span data-stu-id="bbc9a-114">.z component will take on the value of .x component</span></span>
-   <span data-ttu-id="bbc9a-115">。 w 元件會採用. y 元件的值</span><span class="sxs-lookup"><span data-stu-id="bbc9a-115">.w component will take on the value of .y component</span></span>

<span data-ttu-id="bbc9a-116">元件可以依任何順序顯示。</span><span class="sxs-lookup"><span data-stu-id="bbc9a-116">The components can appear in any order.</span></span> <span data-ttu-id="bbc9a-117">如果指定的元件少於四個，則會重複最後一個元件。</span><span class="sxs-lookup"><span data-stu-id="bbc9a-117">If fewer than four components are specified, the last component is repeated.</span></span> <span data-ttu-id="bbc9a-118">例如：</span><span class="sxs-lookup"><span data-stu-id="bbc9a-118">For example:</span></span>


```
.xy  = .xyyy
.wzx = .wzxx
.z   = .zzzz
```



<span data-ttu-id="bbc9a-119">如果未指定任何元件，則不會套用任何 swizzling。</span><span class="sxs-lookup"><span data-stu-id="bbc9a-119">If no component is specified, no swizzling is applied.</span></span>

<span data-ttu-id="bbc9a-120">某些指示對於來源 swizzle 有一些限制。</span><span class="sxs-lookup"><span data-stu-id="bbc9a-120">Some instructions have restrictions for source swizzle.</span></span> <span data-ttu-id="bbc9a-121">它們列在 [遵守的指令參考] 頁面中。</span><span class="sxs-lookup"><span data-stu-id="bbc9a-121">They are listed in the respected instruction reference pages.</span></span>



| <span data-ttu-id="bbc9a-122">圖元著色器版本</span><span class="sxs-lookup"><span data-stu-id="bbc9a-122">Pixel shader versions</span></span> | <span data-ttu-id="bbc9a-123">1\_1</span><span class="sxs-lookup"><span data-stu-id="bbc9a-123">1\_1</span></span> | <span data-ttu-id="bbc9a-124">1\_2</span><span class="sxs-lookup"><span data-stu-id="bbc9a-124">1\_2</span></span> | <span data-ttu-id="bbc9a-125">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="bbc9a-125">1\_3</span></span> | <span data-ttu-id="bbc9a-126">1\_4</span><span class="sxs-lookup"><span data-stu-id="bbc9a-126">1\_4</span></span> | <span data-ttu-id="bbc9a-127">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="bbc9a-127">2\_0</span></span> | <span data-ttu-id="bbc9a-128">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="bbc9a-128">2\_x</span></span> | <span data-ttu-id="bbc9a-129">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="bbc9a-129">2\_sw</span></span> | <span data-ttu-id="bbc9a-130">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="bbc9a-130">3\_0</span></span> | <span data-ttu-id="bbc9a-131">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="bbc9a-131">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="bbc9a-132">.x</span><span class="sxs-lookup"><span data-stu-id="bbc9a-132">.x</span></span>                    |      |      |      | <span data-ttu-id="bbc9a-133">x</span><span class="sxs-lookup"><span data-stu-id="bbc9a-133">x</span></span>    | <span data-ttu-id="bbc9a-134">x</span><span class="sxs-lookup"><span data-stu-id="bbc9a-134">x</span></span>    | <span data-ttu-id="bbc9a-135">x</span><span class="sxs-lookup"><span data-stu-id="bbc9a-135">x</span></span>    | <span data-ttu-id="bbc9a-136">x</span><span class="sxs-lookup"><span data-stu-id="bbc9a-136">x</span></span>     | <span data-ttu-id="bbc9a-137">x</span><span class="sxs-lookup"><span data-stu-id="bbc9a-137">x</span></span>    | <span data-ttu-id="bbc9a-138">x</span><span class="sxs-lookup"><span data-stu-id="bbc9a-138">x</span></span>     |
| <span data-ttu-id="bbc9a-139">. y</span><span class="sxs-lookup"><span data-stu-id="bbc9a-139">.y</span></span>                    |      |      |      | <span data-ttu-id="bbc9a-140">x</span><span class="sxs-lookup"><span data-stu-id="bbc9a-140">x</span></span>    | <span data-ttu-id="bbc9a-141">x</span><span class="sxs-lookup"><span data-stu-id="bbc9a-141">x</span></span>    | <span data-ttu-id="bbc9a-142">x</span><span class="sxs-lookup"><span data-stu-id="bbc9a-142">x</span></span>    | <span data-ttu-id="bbc9a-143">x</span><span class="sxs-lookup"><span data-stu-id="bbc9a-143">x</span></span>     | <span data-ttu-id="bbc9a-144">x</span><span class="sxs-lookup"><span data-stu-id="bbc9a-144">x</span></span>    | <span data-ttu-id="bbc9a-145">x</span><span class="sxs-lookup"><span data-stu-id="bbc9a-145">x</span></span>     |
| <span data-ttu-id="bbc9a-146">. z</span><span class="sxs-lookup"><span data-stu-id="bbc9a-146">.z</span></span>                    | <span data-ttu-id="bbc9a-147">X\*</span><span class="sxs-lookup"><span data-stu-id="bbc9a-147">x\*</span></span>  | <span data-ttu-id="bbc9a-148">X\*</span><span class="sxs-lookup"><span data-stu-id="bbc9a-148">x\*</span></span>  | <span data-ttu-id="bbc9a-149">x\*</span><span class="sxs-lookup"><span data-stu-id="bbc9a-149">x\*</span></span>  | <span data-ttu-id="bbc9a-150">x</span><span class="sxs-lookup"><span data-stu-id="bbc9a-150">x</span></span>    | <span data-ttu-id="bbc9a-151">x</span><span class="sxs-lookup"><span data-stu-id="bbc9a-151">x</span></span>    | <span data-ttu-id="bbc9a-152">x</span><span class="sxs-lookup"><span data-stu-id="bbc9a-152">x</span></span>    | <span data-ttu-id="bbc9a-153">x</span><span class="sxs-lookup"><span data-stu-id="bbc9a-153">x</span></span>     | <span data-ttu-id="bbc9a-154">x</span><span class="sxs-lookup"><span data-stu-id="bbc9a-154">x</span></span>    | <span data-ttu-id="bbc9a-155">x</span><span class="sxs-lookup"><span data-stu-id="bbc9a-155">x</span></span>     |
| <span data-ttu-id="bbc9a-156">w</span><span class="sxs-lookup"><span data-stu-id="bbc9a-156">.w</span></span>                    | <span data-ttu-id="bbc9a-157">x</span><span class="sxs-lookup"><span data-stu-id="bbc9a-157">x</span></span>    | <span data-ttu-id="bbc9a-158">x</span><span class="sxs-lookup"><span data-stu-id="bbc9a-158">x</span></span>    | <span data-ttu-id="bbc9a-159">x</span><span class="sxs-lookup"><span data-stu-id="bbc9a-159">x</span></span>    | <span data-ttu-id="bbc9a-160">x</span><span class="sxs-lookup"><span data-stu-id="bbc9a-160">x</span></span>    | <span data-ttu-id="bbc9a-161">x</span><span class="sxs-lookup"><span data-stu-id="bbc9a-161">x</span></span>    | <span data-ttu-id="bbc9a-162">x</span><span class="sxs-lookup"><span data-stu-id="bbc9a-162">x</span></span>    | <span data-ttu-id="bbc9a-163">x</span><span class="sxs-lookup"><span data-stu-id="bbc9a-163">x</span></span>     | <span data-ttu-id="bbc9a-164">x</span><span class="sxs-lookup"><span data-stu-id="bbc9a-164">x</span></span>    | <span data-ttu-id="bbc9a-165">x</span><span class="sxs-lookup"><span data-stu-id="bbc9a-165">x</span></span>     |
| <span data-ttu-id="bbc9a-166">xyzw (預設) </span><span class="sxs-lookup"><span data-stu-id="bbc9a-166">.xyzw (default)</span></span>       | <span data-ttu-id="bbc9a-167">x</span><span class="sxs-lookup"><span data-stu-id="bbc9a-167">x</span></span>    | <span data-ttu-id="bbc9a-168">x</span><span class="sxs-lookup"><span data-stu-id="bbc9a-168">x</span></span>    | <span data-ttu-id="bbc9a-169">x</span><span class="sxs-lookup"><span data-stu-id="bbc9a-169">x</span></span>    | <span data-ttu-id="bbc9a-170">x</span><span class="sxs-lookup"><span data-stu-id="bbc9a-170">x</span></span>    | <span data-ttu-id="bbc9a-171">x</span><span class="sxs-lookup"><span data-stu-id="bbc9a-171">x</span></span>    | <span data-ttu-id="bbc9a-172">x</span><span class="sxs-lookup"><span data-stu-id="bbc9a-172">x</span></span>    | <span data-ttu-id="bbc9a-173">x</span><span class="sxs-lookup"><span data-stu-id="bbc9a-173">x</span></span>     | <span data-ttu-id="bbc9a-174">x</span><span class="sxs-lookup"><span data-stu-id="bbc9a-174">x</span></span>    | <span data-ttu-id="bbc9a-175">x</span><span class="sxs-lookup"><span data-stu-id="bbc9a-175">x</span></span>     |
| <span data-ttu-id="bbc9a-176">.yzxw</span><span class="sxs-lookup"><span data-stu-id="bbc9a-176">.yzxw</span></span>                 |      |      |      |      | <span data-ttu-id="bbc9a-177">x</span><span class="sxs-lookup"><span data-stu-id="bbc9a-177">x</span></span>    | <span data-ttu-id="bbc9a-178">x</span><span class="sxs-lookup"><span data-stu-id="bbc9a-178">x</span></span>    | <span data-ttu-id="bbc9a-179">x</span><span class="sxs-lookup"><span data-stu-id="bbc9a-179">x</span></span>     | <span data-ttu-id="bbc9a-180">x</span><span class="sxs-lookup"><span data-stu-id="bbc9a-180">x</span></span>    | <span data-ttu-id="bbc9a-181">x</span><span class="sxs-lookup"><span data-stu-id="bbc9a-181">x</span></span>     |
| <span data-ttu-id="bbc9a-182">.zxyw</span><span class="sxs-lookup"><span data-stu-id="bbc9a-182">.zxyw</span></span>                 |      |      |      |      | <span data-ttu-id="bbc9a-183">x</span><span class="sxs-lookup"><span data-stu-id="bbc9a-183">x</span></span>    | <span data-ttu-id="bbc9a-184">x</span><span class="sxs-lookup"><span data-stu-id="bbc9a-184">x</span></span>    | <span data-ttu-id="bbc9a-185">x</span><span class="sxs-lookup"><span data-stu-id="bbc9a-185">x</span></span>     | <span data-ttu-id="bbc9a-186">x</span><span class="sxs-lookup"><span data-stu-id="bbc9a-186">x</span></span>    | <span data-ttu-id="bbc9a-187">x</span><span class="sxs-lookup"><span data-stu-id="bbc9a-187">x</span></span>     |
| <span data-ttu-id="bbc9a-188">.wzyx</span><span class="sxs-lookup"><span data-stu-id="bbc9a-188">.wzyx</span></span>                 |      |      |      |      | <span data-ttu-id="bbc9a-189">x</span><span class="sxs-lookup"><span data-stu-id="bbc9a-189">x</span></span>    | <span data-ttu-id="bbc9a-190">x</span><span class="sxs-lookup"><span data-stu-id="bbc9a-190">x</span></span>    | <span data-ttu-id="bbc9a-191">x</span><span class="sxs-lookup"><span data-stu-id="bbc9a-191">x</span></span>     | <span data-ttu-id="bbc9a-192">x</span><span class="sxs-lookup"><span data-stu-id="bbc9a-192">x</span></span>    | <span data-ttu-id="bbc9a-193">x</span><span class="sxs-lookup"><span data-stu-id="bbc9a-193">x</span></span>     |
| <span data-ttu-id="bbc9a-194">任意 swizzle</span><span class="sxs-lookup"><span data-stu-id="bbc9a-194">arbitrary swizzle</span></span>     |      |      |      |      |      | <span data-ttu-id="bbc9a-195">x</span><span class="sxs-lookup"><span data-stu-id="bbc9a-195">x</span></span>    | <span data-ttu-id="bbc9a-196">x</span><span class="sxs-lookup"><span data-stu-id="bbc9a-196">x</span></span>     | <span data-ttu-id="bbc9a-197">x</span><span class="sxs-lookup"><span data-stu-id="bbc9a-197">x</span></span>    | <span data-ttu-id="bbc9a-198">x</span><span class="sxs-lookup"><span data-stu-id="bbc9a-198">x</span></span>     |



 

<span data-ttu-id="bbc9a-199">\* 只有當目的地寫入遮罩是. w ( 時，才可使用。) 。</span><span class="sxs-lookup"><span data-stu-id="bbc9a-199">\* Only available if destination write mask is .w (.a).</span></span>

## <a name="arbitrary-swizzle"></a><span data-ttu-id="bbc9a-200">任意 Swizzle</span><span class="sxs-lookup"><span data-stu-id="bbc9a-200">Arbitrary Swizzle</span></span>

<span data-ttu-id="bbc9a-201">Swizzles 可依任意順序套用至來源暫存器;也就是說，任何來源暫存器都可以採用任何順序的元件遮罩。</span><span class="sxs-lookup"><span data-stu-id="bbc9a-201">Swizzles can be applied to source registers in an arbitrary order; that is, any source register can take any component mask, in any order.</span></span>

## <a name="replicate-swizzle"></a><span data-ttu-id="bbc9a-202">複寫 Swizzle</span><span class="sxs-lookup"><span data-stu-id="bbc9a-202">Replicate Swizzle</span></span>

<span data-ttu-id="bbc9a-203">複寫 swizzle 會將一個元件複製到另一個元件。</span><span class="sxs-lookup"><span data-stu-id="bbc9a-203">Replicate swizzle copies one component to another.</span></span> <span data-ttu-id="bbc9a-204">這就是其中一個. x、. y、z、w swizzle 元件 (或 r、g.、b.。必須指定對應的) 。</span><span class="sxs-lookup"><span data-stu-id="bbc9a-204">This is, exactly one of the .x, .y, .z, .w swizzle components (or the .r, .g, .b, .a equivalents) must be specified.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bbc9a-205">相關主題</span><span class="sxs-lookup"><span data-stu-id="bbc9a-205">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bbc9a-206">圖元著色器來源登錄修飾詞</span><span class="sxs-lookup"><span data-stu-id="bbc9a-206">Pixel Shader Source Register Modifiers</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-source.md)
</dt> <dt>

[<span data-ttu-id="bbc9a-207">ps \_ 1 \_ 1 \_ \_ ps \_ 1 \_ 2 \_ \_ ps \_ 1 \_ 3 \_ \_ ps \_ 1 \_ 4 註冊</span><span class="sxs-lookup"><span data-stu-id="bbc9a-207">ps\_1\_1\_\_ps\_1\_2\_\_ps\_1\_3\_\_ps\_1\_4 Registers</span></span>](dx9-graphics-reference-asm-ps-registers-ps-1-x.md)
</dt> <dt>

[<span data-ttu-id="bbc9a-208">ps \_ 2 \_ 0 註冊</span><span class="sxs-lookup"><span data-stu-id="bbc9a-208">ps\_2\_0 Registers</span></span>](dx9-graphics-reference-asm-ps-registers-ps-2-0.md)
</dt> <dt>

[<span data-ttu-id="bbc9a-209">ps \_ 2 \_ x 註冊</span><span class="sxs-lookup"><span data-stu-id="bbc9a-209">ps\_2\_x Registers</span></span>](dx9-graphics-reference-asm-ps-registers-ps-2-x.md)
</dt> <dt>

[<span data-ttu-id="bbc9a-210">ps \_ 3 \_ 0 註冊</span><span class="sxs-lookup"><span data-stu-id="bbc9a-210">ps\_3\_0 Registers</span></span>](dx9-graphics-reference-asm-ps-registers-ps-3-0.md)
</dt> </dl>

 

 




