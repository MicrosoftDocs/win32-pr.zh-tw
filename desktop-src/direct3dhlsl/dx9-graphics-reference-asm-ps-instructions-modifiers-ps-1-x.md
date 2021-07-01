---
title: Ps_1_X 的修飾詞
description: 指令修飾詞會在將指令寫入目的地登錄之前，先影響指令的結果。 瞭解 ps_1_X 的修飾詞。
ms.assetid: 15b892da-b6fd-4bd5-8889-bc48035e7819
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b9291d818252c95bc11fae72bd3311ec733a45fa
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/01/2021
ms.locfileid: "113129937"
---
# <a name="modifiers-for-ps_1_x"></a><span data-ttu-id="4bd8a-104">Ps \_ 1 X 的修飾詞 \_</span><span class="sxs-lookup"><span data-stu-id="4bd8a-104">Modifiers for ps\_1\_X</span></span>

<span data-ttu-id="4bd8a-105">指令修飾詞會在將指令寫入目的地登錄之前，先影響指令的結果。</span><span class="sxs-lookup"><span data-stu-id="4bd8a-105">Instruction modifiers affect the result of the instruction before it is written into the destination register.</span></span> <span data-ttu-id="4bd8a-106">例如，您可以使用它們來將結果乘以或除以二的因數，或在零和1之間執行結果。</span><span class="sxs-lookup"><span data-stu-id="4bd8a-106">For instance, use them to multiply or divide the result by a factor of two, or to clamp the result between zero and one.</span></span> <span data-ttu-id="4bd8a-107">指令修飾詞會在執行指令之後，但在將結果寫入目的地登錄之前套用。</span><span class="sxs-lookup"><span data-stu-id="4bd8a-107">Instruction modifiers are applied after the instruction runs but before writing the result to the destination register.</span></span>

<span data-ttu-id="4bd8a-108">修改者清單如下所示。</span><span class="sxs-lookup"><span data-stu-id="4bd8a-108">A list of the modifiers is shown below.</span></span>



| <span data-ttu-id="4bd8a-109">修飾詞</span><span class="sxs-lookup"><span data-stu-id="4bd8a-109">Modifier</span></span> | <span data-ttu-id="4bd8a-110">描述</span><span class="sxs-lookup"><span data-stu-id="4bd8a-110">Description</span></span>                   | <span data-ttu-id="4bd8a-111">語法</span><span class="sxs-lookup"><span data-stu-id="4bd8a-111">Syntax</span></span>           | <span data-ttu-id="4bd8a-112">\_第1版</span><span class="sxs-lookup"><span data-stu-id="4bd8a-112">Version 1\_1</span></span> | <span data-ttu-id="4bd8a-113">\_第1版</span><span class="sxs-lookup"><span data-stu-id="4bd8a-113">Version 1\_2</span></span>     |<span data-ttu-id="4bd8a-114">第1版 \_</span><span class="sxs-lookup"><span data-stu-id="4bd8a-114">Version  1\_3</span></span>    | <span data-ttu-id="4bd8a-115">\_第1版</span><span class="sxs-lookup"><span data-stu-id="4bd8a-115">Version 1\_4</span></span>    |
|----------|-------------------------------|------------------|---------|------|------|------|
| <span data-ttu-id="4bd8a-116">\_x2</span><span class="sxs-lookup"><span data-stu-id="4bd8a-116">\_x2</span></span>     | <span data-ttu-id="4bd8a-117">乘以2</span><span class="sxs-lookup"><span data-stu-id="4bd8a-117">Multiply by 2</span></span>                 | <span data-ttu-id="4bd8a-118">指令 \_ x2</span><span class="sxs-lookup"><span data-stu-id="4bd8a-118">instruction\_x2</span></span>  | <span data-ttu-id="4bd8a-119">X</span><span class="sxs-lookup"><span data-stu-id="4bd8a-119">X</span></span>       | <span data-ttu-id="4bd8a-120">X</span><span class="sxs-lookup"><span data-stu-id="4bd8a-120">X</span></span>    | <span data-ttu-id="4bd8a-121">X</span><span class="sxs-lookup"><span data-stu-id="4bd8a-121">X</span></span>    | <span data-ttu-id="4bd8a-122">X</span><span class="sxs-lookup"><span data-stu-id="4bd8a-122">X</span></span>    |
| <span data-ttu-id="4bd8a-123">\_四</span><span class="sxs-lookup"><span data-stu-id="4bd8a-123">\_x4</span></span>     | <span data-ttu-id="4bd8a-124">乘以4</span><span class="sxs-lookup"><span data-stu-id="4bd8a-124">Multiply by 4</span></span>                 | <span data-ttu-id="4bd8a-125">指示 \_ x4</span><span class="sxs-lookup"><span data-stu-id="4bd8a-125">instruction\_x4</span></span>  | <span data-ttu-id="4bd8a-126">X</span><span class="sxs-lookup"><span data-stu-id="4bd8a-126">X</span></span>       | <span data-ttu-id="4bd8a-127">X</span><span class="sxs-lookup"><span data-stu-id="4bd8a-127">X</span></span>    | <span data-ttu-id="4bd8a-128">X</span><span class="sxs-lookup"><span data-stu-id="4bd8a-128">X</span></span>    | <span data-ttu-id="4bd8a-129">X</span><span class="sxs-lookup"><span data-stu-id="4bd8a-129">X</span></span>    |
| <span data-ttu-id="4bd8a-130">\_x8</span><span class="sxs-lookup"><span data-stu-id="4bd8a-130">\_x8</span></span>     | <span data-ttu-id="4bd8a-131">乘以8</span><span class="sxs-lookup"><span data-stu-id="4bd8a-131">Multiply by 8</span></span>                 | <span data-ttu-id="4bd8a-132">指令 \_ x8</span><span class="sxs-lookup"><span data-stu-id="4bd8a-132">instruction\_x8</span></span>  |         |      |      | <span data-ttu-id="4bd8a-133">X</span><span class="sxs-lookup"><span data-stu-id="4bd8a-133">X</span></span>    |
| <span data-ttu-id="4bd8a-134">\_d2</span><span class="sxs-lookup"><span data-stu-id="4bd8a-134">\_d2</span></span>     | <span data-ttu-id="4bd8a-135">除以2</span><span class="sxs-lookup"><span data-stu-id="4bd8a-135">Divide by 2</span></span>                   | <span data-ttu-id="4bd8a-136">指令 \_ d2</span><span class="sxs-lookup"><span data-stu-id="4bd8a-136">instruction\_d2</span></span>  | <span data-ttu-id="4bd8a-137">X</span><span class="sxs-lookup"><span data-stu-id="4bd8a-137">X</span></span>       | <span data-ttu-id="4bd8a-138">X</span><span class="sxs-lookup"><span data-stu-id="4bd8a-138">X</span></span>    | <span data-ttu-id="4bd8a-139">X</span><span class="sxs-lookup"><span data-stu-id="4bd8a-139">X</span></span>    | <span data-ttu-id="4bd8a-140">X</span><span class="sxs-lookup"><span data-stu-id="4bd8a-140">X</span></span>    |
| <span data-ttu-id="4bd8a-141">\_d4</span><span class="sxs-lookup"><span data-stu-id="4bd8a-141">\_d4</span></span>     | <span data-ttu-id="4bd8a-142">除以4</span><span class="sxs-lookup"><span data-stu-id="4bd8a-142">Divide by 4</span></span>                   | <span data-ttu-id="4bd8a-143">指示 \_ d4</span><span class="sxs-lookup"><span data-stu-id="4bd8a-143">instruction\_d4</span></span>  |         |      |      | <span data-ttu-id="4bd8a-144">X</span><span class="sxs-lookup"><span data-stu-id="4bd8a-144">X</span></span>    |
| <span data-ttu-id="4bd8a-145">\_d8</span><span class="sxs-lookup"><span data-stu-id="4bd8a-145">\_d8</span></span>     | <span data-ttu-id="4bd8a-146">除以8</span><span class="sxs-lookup"><span data-stu-id="4bd8a-146">Divide by 8</span></span>                   | <span data-ttu-id="4bd8a-147">d8 的指令 \_</span><span class="sxs-lookup"><span data-stu-id="4bd8a-147">instruction\_d8</span></span>  |         |      |      | <span data-ttu-id="4bd8a-148">X</span><span class="sxs-lookup"><span data-stu-id="4bd8a-148">X</span></span>    |
| <span data-ttu-id="4bd8a-149">\_坐</span><span class="sxs-lookup"><span data-stu-id="4bd8a-149">\_sat</span></span>    | <span data-ttu-id="4bd8a-150">從0和 1)  (夾具飽和</span><span class="sxs-lookup"><span data-stu-id="4bd8a-150">Saturate (clamp from 0 and 1)</span></span> | <span data-ttu-id="4bd8a-151">指示 \_ sat</span><span class="sxs-lookup"><span data-stu-id="4bd8a-151">instruction\_sat</span></span> | <span data-ttu-id="4bd8a-152">X</span><span class="sxs-lookup"><span data-stu-id="4bd8a-152">X</span></span>       | <span data-ttu-id="4bd8a-153">X</span><span class="sxs-lookup"><span data-stu-id="4bd8a-153">X</span></span>    | <span data-ttu-id="4bd8a-154">X</span><span class="sxs-lookup"><span data-stu-id="4bd8a-154">X</span></span>    | <span data-ttu-id="4bd8a-155">X</span><span class="sxs-lookup"><span data-stu-id="4bd8a-155">X</span></span>    |



 

-   <span data-ttu-id="4bd8a-156">乘數修飾詞會將暫存器資料乘以讀取後的兩次乘冪。</span><span class="sxs-lookup"><span data-stu-id="4bd8a-156">The multiply modifier multiplies the register data by a power of two after it is read.</span></span> <span data-ttu-id="4bd8a-157">這與左移時相同。</span><span class="sxs-lookup"><span data-stu-id="4bd8a-157">This is the same as a shift left.</span></span>
-   <span data-ttu-id="4bd8a-158">除法修飾詞會將暫存器資料除以兩次讀取後的乘冪。</span><span class="sxs-lookup"><span data-stu-id="4bd8a-158">The divide modifier divides the register data by a power of two after it is read.</span></span> <span data-ttu-id="4bd8a-159">這與 shift 許可權相同。</span><span class="sxs-lookup"><span data-stu-id="4bd8a-159">This is the same as a shift right.</span></span>
-   <span data-ttu-id="4bd8a-160">飽和修飾詞會個從零到1的暫存器值範圍。</span><span class="sxs-lookup"><span data-stu-id="4bd8a-160">The saturate modifier clamps the range of register values from zero to one.</span></span>

<span data-ttu-id="4bd8a-161">指令修飾詞可用於算術指令。</span><span class="sxs-lookup"><span data-stu-id="4bd8a-161">Instruction modifiers can be used on arithmetic instructions.</span></span> <span data-ttu-id="4bd8a-162">它們不能用於紋理位址指示。</span><span class="sxs-lookup"><span data-stu-id="4bd8a-162">They may not be used on texture address instructions.</span></span>

<span data-ttu-id="4bd8a-163">乘修飾詞</span><span class="sxs-lookup"><span data-stu-id="4bd8a-163">Multiply modifier</span></span>

<span data-ttu-id="4bd8a-164">此範例會使用來源運算元中兩個色彩的總和來載入目的地登錄 (dest)  (src0 和 src1) ，並將結果乘以二。</span><span class="sxs-lookup"><span data-stu-id="4bd8a-164">This example loads the destination register (dest) with the sum of the two colors in the source operands (src0 and src1) and multiplies the result by two.</span></span>


```
add_x2 dest, src0, src1
```



<span data-ttu-id="4bd8a-165">此範例結合兩個指令修飾詞。</span><span class="sxs-lookup"><span data-stu-id="4bd8a-165">This example combines two instruction modifiers.</span></span> <span data-ttu-id="4bd8a-166">首先，來源運算元中的兩個色彩 (src0 和 src1) 都會加入。</span><span class="sxs-lookup"><span data-stu-id="4bd8a-166">First, two colors in the source operands (src0 and src1) are added.</span></span> <span data-ttu-id="4bd8a-167">然後，結果會乘以2，並在0.0 到1.0 之間壓制每個元件。</span><span class="sxs-lookup"><span data-stu-id="4bd8a-167">The result is then multiplied by two, and clamped between 0.0 to 1.0 for each component.</span></span> <span data-ttu-id="4bd8a-168">結果會儲存在目的地註冊中。</span><span class="sxs-lookup"><span data-stu-id="4bd8a-168">The result is saved in the destination register.</span></span>


```
add_x2_sat dest, src0, src1
```



<span data-ttu-id="4bd8a-169">除法修飾詞</span><span class="sxs-lookup"><span data-stu-id="4bd8a-169">Divide modifier</span></span>

<span data-ttu-id="4bd8a-170">此範例會使用來源運算元中兩個色彩的總和來載入目的地登錄 (dest)  (src0 和 src1) ，並將結果除以二。</span><span class="sxs-lookup"><span data-stu-id="4bd8a-170">This example loads the destination register (dest) with the sum of the two colors in the source operands (src0 and src1) and divides the result by two.</span></span>


```
add_d2 dest, src0, src1
```



<span data-ttu-id="4bd8a-171">飽和修飾詞</span><span class="sxs-lookup"><span data-stu-id="4bd8a-171">Saturate modifier</span></span>

<span data-ttu-id="4bd8a-172">針對算術指令，飽和度修飾詞會將此指令的結果個至每個元件的0.0 至1.0 範圍內。</span><span class="sxs-lookup"><span data-stu-id="4bd8a-172">For arithmetic instructions, the saturation modifier clamps the result of this instruction into the range 0.0 to 1.0 for each component.</span></span> <span data-ttu-id="4bd8a-173">下列範例顯示如何使用此指令修飾詞。</span><span class="sxs-lookup"><span data-stu-id="4bd8a-173">The following example shows how to use this instruction modifier.</span></span>


```
dp3_sat r0, t0_bx2, v0_bx2    ; t0 is bump, v0 is light direction
```



<span data-ttu-id="4bd8a-174">此作業會在任何乘法或除法指令修飾詞之後發生。</span><span class="sxs-lookup"><span data-stu-id="4bd8a-174">This operation occurs after any multiply or divide instruction modifier.</span></span> <span data-ttu-id="4bd8a-175">\_sat 最常用來夾具點積結果。</span><span class="sxs-lookup"><span data-stu-id="4bd8a-175">\_sat is most often used to clamp dot product results.</span></span> <span data-ttu-id="4bd8a-176">不過，它也可以一致地模擬 multipass 方法，其中的框架緩衝區一律在0到1的範圍內，以及 DirectX 6 和7.0 多紋理語法，其中的飽和度定義為在每個階段發生。</span><span class="sxs-lookup"><span data-stu-id="4bd8a-176">However, it also enables consistent emulation of multipass methods where the frame buffer is always in the range 0 to 1, and of DirectX 6 and 7.0 multitexture syntax, in which saturation is defined to occur at every stage.</span></span>

<span data-ttu-id="4bd8a-177">這個範例會使用來源運算元中兩個色彩的總和 (src0 和 src1) ，將目的地登錄載入 (dest) ，然後將每個元件的結果個為0.0 到1.0 的範圍。</span><span class="sxs-lookup"><span data-stu-id="4bd8a-177">This example loads the destination register (dest) with the sum of the two colors in the source operands (src0 and src1), and clamps the result into the range 0.0 to 1.0 for each component.</span></span>


```
add_sat dest, src0, src1
```



<span data-ttu-id="4bd8a-178">此範例結合兩個指令修飾詞。</span><span class="sxs-lookup"><span data-stu-id="4bd8a-178">This example combines two instruction modifiers.</span></span> <span data-ttu-id="4bd8a-179">首先，來源運算元中的兩個色彩 (src0 和 src1) 都會加入。</span><span class="sxs-lookup"><span data-stu-id="4bd8a-179">First, two colors in the source operands (src0 and src1) are added.</span></span> <span data-ttu-id="4bd8a-180">每個元件的結果會乘以2，並在0.0 到1.0 之間壓制。</span><span class="sxs-lookup"><span data-stu-id="4bd8a-180">The result is multiplied by two and clamped between 0.0 to 1.0 for each component.</span></span> <span data-ttu-id="4bd8a-181">結果會儲存在目的地註冊中。</span><span class="sxs-lookup"><span data-stu-id="4bd8a-181">The result is saved in the destination register.</span></span>


```
add_x2_sat dest, src0, src1
```



## <a name="related-topics"></a><span data-ttu-id="4bd8a-182">相關主題</span><span class="sxs-lookup"><span data-stu-id="4bd8a-182">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4bd8a-183">圖元著色器指示</span><span class="sxs-lookup"><span data-stu-id="4bd8a-183">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




