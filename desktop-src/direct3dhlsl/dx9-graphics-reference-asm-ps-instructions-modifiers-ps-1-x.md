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
ms.openlocfilehash: 6c97196040a8f5f9888cb2fb354dcc18ca3743c7
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/10/2021
ms.locfileid: "111988723"
---
# <a name="modifiers-for-ps_1_x"></a><span data-ttu-id="35677-104">Ps \_ 1 X 的修飾詞 \_</span><span class="sxs-lookup"><span data-stu-id="35677-104">Modifiers for ps\_1\_X</span></span>

<span data-ttu-id="35677-105">指令修飾詞會在將指令寫入目的地登錄之前，先影響指令的結果。</span><span class="sxs-lookup"><span data-stu-id="35677-105">Instruction modifiers affect the result of the instruction before it is written into the destination register.</span></span> <span data-ttu-id="35677-106">例如，您可以使用它們來將結果乘以或除以二的因數，或在零和1之間執行結果。</span><span class="sxs-lookup"><span data-stu-id="35677-106">For instance, use them to multiply or divide the result by a factor of two, or to clamp the result between zero and one.</span></span> <span data-ttu-id="35677-107">指令修飾詞會在執行指令之後，但在將結果寫入目的地登錄之前套用。</span><span class="sxs-lookup"><span data-stu-id="35677-107">Instruction modifiers are applied after the instruction runs but before writing the result to the destination register.</span></span>

<span data-ttu-id="35677-108">修改者清單如下所示。</span><span class="sxs-lookup"><span data-stu-id="35677-108">A list of the modifiers is shown below.</span></span>



| <span data-ttu-id="35677-109">修飾詞</span><span class="sxs-lookup"><span data-stu-id="35677-109">Modifier</span></span> | <span data-ttu-id="35677-110">描述</span><span class="sxs-lookup"><span data-stu-id="35677-110">Description</span></span>                   | <span data-ttu-id="35677-111">語法</span><span class="sxs-lookup"><span data-stu-id="35677-111">Syntax</span></span>           | <span data-ttu-id="35677-112">版本</span><span class="sxs-lookup"><span data-stu-id="35677-112">Version</span></span> |      |      |      |
|----------|-------------------------------|------------------|---------|------|------|------|
|          |                               |                  | <span data-ttu-id="35677-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="35677-113">1\_1</span></span>    | <span data-ttu-id="35677-114">1\_2</span><span class="sxs-lookup"><span data-stu-id="35677-114">1\_2</span></span> | <span data-ttu-id="35677-115">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="35677-115">1\_3</span></span> | <span data-ttu-id="35677-116">1\_4</span><span class="sxs-lookup"><span data-stu-id="35677-116">1\_4</span></span> |
| <span data-ttu-id="35677-117">\_x2</span><span class="sxs-lookup"><span data-stu-id="35677-117">\_x2</span></span>     | <span data-ttu-id="35677-118">乘以2</span><span class="sxs-lookup"><span data-stu-id="35677-118">Multiply by 2</span></span>                 | <span data-ttu-id="35677-119">指令 \_ x2</span><span class="sxs-lookup"><span data-stu-id="35677-119">instruction\_x2</span></span>  | <span data-ttu-id="35677-120">X</span><span class="sxs-lookup"><span data-stu-id="35677-120">X</span></span>       | <span data-ttu-id="35677-121">X</span><span class="sxs-lookup"><span data-stu-id="35677-121">X</span></span>    | <span data-ttu-id="35677-122">X</span><span class="sxs-lookup"><span data-stu-id="35677-122">X</span></span>    | <span data-ttu-id="35677-123">X</span><span class="sxs-lookup"><span data-stu-id="35677-123">X</span></span>    |
| <span data-ttu-id="35677-124">\_四</span><span class="sxs-lookup"><span data-stu-id="35677-124">\_x4</span></span>     | <span data-ttu-id="35677-125">乘以4</span><span class="sxs-lookup"><span data-stu-id="35677-125">Multiply by 4</span></span>                 | <span data-ttu-id="35677-126">指示 \_ x4</span><span class="sxs-lookup"><span data-stu-id="35677-126">instruction\_x4</span></span>  | <span data-ttu-id="35677-127">X</span><span class="sxs-lookup"><span data-stu-id="35677-127">X</span></span>       | <span data-ttu-id="35677-128">X</span><span class="sxs-lookup"><span data-stu-id="35677-128">X</span></span>    | <span data-ttu-id="35677-129">X</span><span class="sxs-lookup"><span data-stu-id="35677-129">X</span></span>    | <span data-ttu-id="35677-130">X</span><span class="sxs-lookup"><span data-stu-id="35677-130">X</span></span>    |
| <span data-ttu-id="35677-131">\_x8</span><span class="sxs-lookup"><span data-stu-id="35677-131">\_x8</span></span>     | <span data-ttu-id="35677-132">乘以8</span><span class="sxs-lookup"><span data-stu-id="35677-132">Multiply by 8</span></span>                 | <span data-ttu-id="35677-133">指令 \_ x8</span><span class="sxs-lookup"><span data-stu-id="35677-133">instruction\_x8</span></span>  |         |      |      | <span data-ttu-id="35677-134">X</span><span class="sxs-lookup"><span data-stu-id="35677-134">X</span></span>    |
| <span data-ttu-id="35677-135">\_d2</span><span class="sxs-lookup"><span data-stu-id="35677-135">\_d2</span></span>     | <span data-ttu-id="35677-136">除以2</span><span class="sxs-lookup"><span data-stu-id="35677-136">Divide by 2</span></span>                   | <span data-ttu-id="35677-137">指令 \_ d2</span><span class="sxs-lookup"><span data-stu-id="35677-137">instruction\_d2</span></span>  | <span data-ttu-id="35677-138">X</span><span class="sxs-lookup"><span data-stu-id="35677-138">X</span></span>       | <span data-ttu-id="35677-139">X</span><span class="sxs-lookup"><span data-stu-id="35677-139">X</span></span>    | <span data-ttu-id="35677-140">X</span><span class="sxs-lookup"><span data-stu-id="35677-140">X</span></span>    | <span data-ttu-id="35677-141">X</span><span class="sxs-lookup"><span data-stu-id="35677-141">X</span></span>    |
| <span data-ttu-id="35677-142">\_d4</span><span class="sxs-lookup"><span data-stu-id="35677-142">\_d4</span></span>     | <span data-ttu-id="35677-143">除以4</span><span class="sxs-lookup"><span data-stu-id="35677-143">Divide by 4</span></span>                   | <span data-ttu-id="35677-144">指示 \_ d4</span><span class="sxs-lookup"><span data-stu-id="35677-144">instruction\_d4</span></span>  |         |      |      | <span data-ttu-id="35677-145">X</span><span class="sxs-lookup"><span data-stu-id="35677-145">X</span></span>    |
| <span data-ttu-id="35677-146">\_d8</span><span class="sxs-lookup"><span data-stu-id="35677-146">\_d8</span></span>     | <span data-ttu-id="35677-147">除以8</span><span class="sxs-lookup"><span data-stu-id="35677-147">Divide by 8</span></span>                   | <span data-ttu-id="35677-148">d8 的指令 \_</span><span class="sxs-lookup"><span data-stu-id="35677-148">instruction\_d8</span></span>  |         |      |      | <span data-ttu-id="35677-149">X</span><span class="sxs-lookup"><span data-stu-id="35677-149">X</span></span>    |
| <span data-ttu-id="35677-150">\_坐</span><span class="sxs-lookup"><span data-stu-id="35677-150">\_sat</span></span>    | <span data-ttu-id="35677-151">從0和 1)  (夾具飽和</span><span class="sxs-lookup"><span data-stu-id="35677-151">Saturate (clamp from 0 and 1)</span></span> | <span data-ttu-id="35677-152">指示 \_ sat</span><span class="sxs-lookup"><span data-stu-id="35677-152">instruction\_sat</span></span> | <span data-ttu-id="35677-153">X</span><span class="sxs-lookup"><span data-stu-id="35677-153">X</span></span>       | <span data-ttu-id="35677-154">X</span><span class="sxs-lookup"><span data-stu-id="35677-154">X</span></span>    | <span data-ttu-id="35677-155">X</span><span class="sxs-lookup"><span data-stu-id="35677-155">X</span></span>    | <span data-ttu-id="35677-156">X</span><span class="sxs-lookup"><span data-stu-id="35677-156">X</span></span>    |



 

-   <span data-ttu-id="35677-157">乘數修飾詞會將暫存器資料乘以讀取後的兩次乘冪。</span><span class="sxs-lookup"><span data-stu-id="35677-157">The multiply modifier multiplies the register data by a power of two after it is read.</span></span> <span data-ttu-id="35677-158">這與左移時相同。</span><span class="sxs-lookup"><span data-stu-id="35677-158">This is the same as a shift left.</span></span>
-   <span data-ttu-id="35677-159">除法修飾詞會將暫存器資料除以兩次讀取後的乘冪。</span><span class="sxs-lookup"><span data-stu-id="35677-159">The divide modifier divides the register data by a power of two after it is read.</span></span> <span data-ttu-id="35677-160">這與 shift 許可權相同。</span><span class="sxs-lookup"><span data-stu-id="35677-160">This is the same as a shift right.</span></span>
-   <span data-ttu-id="35677-161">飽和修飾詞會個從零到1的暫存器值範圍。</span><span class="sxs-lookup"><span data-stu-id="35677-161">The saturate modifier clamps the range of register values from zero to one.</span></span>

<span data-ttu-id="35677-162">指令修飾詞可用於算術指令。</span><span class="sxs-lookup"><span data-stu-id="35677-162">Instruction modifiers can be used on arithmetic instructions.</span></span> <span data-ttu-id="35677-163">它們不能用於紋理位址指示。</span><span class="sxs-lookup"><span data-stu-id="35677-163">They may not be used on texture address instructions.</span></span>

<span data-ttu-id="35677-164">乘修飾詞</span><span class="sxs-lookup"><span data-stu-id="35677-164">Multiply modifier</span></span>

<span data-ttu-id="35677-165">此範例會使用來源運算元中兩個色彩的總和來載入目的地登錄 (dest)  (src0 和 src1) ，並將結果乘以二。</span><span class="sxs-lookup"><span data-stu-id="35677-165">This example loads the destination register (dest) with the sum of the two colors in the source operands (src0 and src1) and multiplies the result by two.</span></span>


```
add_x2 dest, src0, src1
```



<span data-ttu-id="35677-166">此範例結合兩個指令修飾詞。</span><span class="sxs-lookup"><span data-stu-id="35677-166">This example combines two instruction modifiers.</span></span> <span data-ttu-id="35677-167">首先，來源運算元中的兩個色彩 (src0 和 src1) 都會加入。</span><span class="sxs-lookup"><span data-stu-id="35677-167">First, two colors in the source operands (src0 and src1) are added.</span></span> <span data-ttu-id="35677-168">然後，結果會乘以2，並在0.0 到1.0 之間壓制每個元件。</span><span class="sxs-lookup"><span data-stu-id="35677-168">The result is then multiplied by two, and clamped between 0.0 to 1.0 for each component.</span></span> <span data-ttu-id="35677-169">結果會儲存在目的地註冊中。</span><span class="sxs-lookup"><span data-stu-id="35677-169">The result is saved in the destination register.</span></span>


```
add_x2_sat dest, src0, src1
```



<span data-ttu-id="35677-170">除法修飾詞</span><span class="sxs-lookup"><span data-stu-id="35677-170">Divide modifier</span></span>

<span data-ttu-id="35677-171">此範例會使用來源運算元中兩個色彩的總和來載入目的地登錄 (dest)  (src0 和 src1) ，並將結果除以二。</span><span class="sxs-lookup"><span data-stu-id="35677-171">This example loads the destination register (dest) with the sum of the two colors in the source operands (src0 and src1) and divides the result by two.</span></span>


```
add_d2 dest, src0, src1
```



<span data-ttu-id="35677-172">飽和修飾詞</span><span class="sxs-lookup"><span data-stu-id="35677-172">Saturate modifier</span></span>

<span data-ttu-id="35677-173">針對算術指令，飽和度修飾詞會將此指令的結果個至每個元件的0.0 至1.0 範圍內。</span><span class="sxs-lookup"><span data-stu-id="35677-173">For arithmetic instructions, the saturation modifier clamps the result of this instruction into the range 0.0 to 1.0 for each component.</span></span> <span data-ttu-id="35677-174">下列範例顯示如何使用此指令修飾詞。</span><span class="sxs-lookup"><span data-stu-id="35677-174">The following example shows how to use this instruction modifier.</span></span>


```
dp3_sat r0, t0_bx2, v0_bx2    ; t0 is bump, v0 is light direction
```



<span data-ttu-id="35677-175">此作業會在任何乘法或除法指令修飾詞之後發生。</span><span class="sxs-lookup"><span data-stu-id="35677-175">This operation occurs after any multiply or divide instruction modifier.</span></span> <span data-ttu-id="35677-176">\_sat 最常用來夾具點積結果。</span><span class="sxs-lookup"><span data-stu-id="35677-176">\_sat is most often used to clamp dot product results.</span></span> <span data-ttu-id="35677-177">不過，它也可以一致地模擬 multipass 方法，其中的框架緩衝區一律在0到1的範圍內，以及 DirectX 6 和7.0 多紋理語法，其中的飽和度定義為在每個階段發生。</span><span class="sxs-lookup"><span data-stu-id="35677-177">However, it also enables consistent emulation of multipass methods where the frame buffer is always in the range 0 to 1, and of DirectX 6 and 7.0 multitexture syntax, in which saturation is defined to occur at every stage.</span></span>

<span data-ttu-id="35677-178">這個範例會使用來源運算元中兩個色彩的總和 (src0 和 src1) ，將目的地登錄載入 (dest) ，然後將每個元件的結果個為0.0 到1.0 的範圍。</span><span class="sxs-lookup"><span data-stu-id="35677-178">This example loads the destination register (dest) with the sum of the two colors in the source operands (src0 and src1), and clamps the result into the range 0.0 to 1.0 for each component.</span></span>


```
add_sat dest, src0, src1
```



<span data-ttu-id="35677-179">此範例結合兩個指令修飾詞。</span><span class="sxs-lookup"><span data-stu-id="35677-179">This example combines two instruction modifiers.</span></span> <span data-ttu-id="35677-180">首先，來源運算元中的兩個色彩 (src0 和 src1) 都會加入。</span><span class="sxs-lookup"><span data-stu-id="35677-180">First, two colors in the source operands (src0 and src1) are added.</span></span> <span data-ttu-id="35677-181">每個元件的結果會乘以2，並在0.0 到1.0 之間壓制。</span><span class="sxs-lookup"><span data-stu-id="35677-181">The result is multiplied by two and clamped between 0.0 to 1.0 for each component.</span></span> <span data-ttu-id="35677-182">結果會儲存在目的地註冊中。</span><span class="sxs-lookup"><span data-stu-id="35677-182">The result is saved in the destination register.</span></span>


```
add_x2_sat dest, src0, src1
```



## <a name="related-topics"></a><span data-ttu-id="35677-183">相關主題</span><span class="sxs-lookup"><span data-stu-id="35677-183">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="35677-184">圖元著色器指示</span><span class="sxs-lookup"><span data-stu-id="35677-184">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




