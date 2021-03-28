---
title: 'swapc (sm5-asm) '
description: 執行兩個輸入暫存器之間值的元件條件式交換。
ms.assetid: 3DFCEB82-076E-4AFA-915F-47390A355B7C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46d2ee674a1cb1067594b0e96c739ff8df73b152
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104990767"
---
# <a name="swapc-sm5---asm"></a><span data-ttu-id="6de85-103">swapc (sm5-asm) </span><span class="sxs-lookup"><span data-stu-id="6de85-103">swapc (sm5 - asm)</span></span>

<span data-ttu-id="6de85-104">執行兩個輸入暫存器之間值的元件條件式交換。</span><span class="sxs-lookup"><span data-stu-id="6de85-104">Performs a component-wise conditional swap of the values between two input registers.</span></span>



| <span data-ttu-id="6de85-105">swapc dest0 \[ mask \] 、dest1 \[ mask \] 、src0 \[ . swizzle \] 、src1. swizzle \[ \] 、src2 收取 \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="6de85-105">swapc dest0\[.mask\], dest1\[.mask\], src0\[.swizzle\], src1\[.swizzle\], src2\[.swizzle\]</span></span> |
|--------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="6de85-106">項目</span><span class="sxs-lookup"><span data-stu-id="6de85-106">Item</span></span>                                                               | <span data-ttu-id="6de85-107">描述</span><span class="sxs-lookup"><span data-stu-id="6de85-107">Description</span></span>                                                                                     |
|--------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6de85-108"><span id="dest0"></span><span id="DEST0"></span>*dest0*</span><span class="sxs-lookup"><span data-stu-id="6de85-108"><span id="dest0"></span><span id="DEST0"></span>*dest0*</span></span><br/> | <span data-ttu-id="6de85-109">\[以 \] 任意非空白寫入遮罩進行註冊。</span><span class="sxs-lookup"><span data-stu-id="6de85-109">\[in\] Register with arbitrary nonempty write masks.</span></span> <span data-ttu-id="6de85-110">必須不同于 *dest1*。</span><span class="sxs-lookup"><span data-stu-id="6de85-110">Must be different than *dest1*.</span></span><br/> |
| <span data-ttu-id="6de85-111"><span id="dest1"></span><span id="DEST1"></span>*dest1*</span><span class="sxs-lookup"><span data-stu-id="6de85-111"><span id="dest1"></span><span id="DEST1"></span>*dest1*</span></span><br/> | <span data-ttu-id="6de85-112">\[以 \] 任意非空白寫入遮罩進行註冊。</span><span class="sxs-lookup"><span data-stu-id="6de85-112">\[in\] Register with arbitrary nonempty write masks.</span></span> <span data-ttu-id="6de85-113">必須不同于 *dest0*。</span><span class="sxs-lookup"><span data-stu-id="6de85-113">Must be different than *dest0*.</span></span><br/> |
| <span data-ttu-id="6de85-114"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="6de85-114"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>    | <span data-ttu-id="6de85-115">\[中 \] 提供4個條件。</span><span class="sxs-lookup"><span data-stu-id="6de85-115">\[in\] Provides 4 conditions.</span></span> <span data-ttu-id="6de85-116">非零整數值表示 **true**。</span><span class="sxs-lookup"><span data-stu-id="6de85-116">A nonzero integer value means **true**.</span></span> <br/>               |
| <span data-ttu-id="6de85-117"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="6de85-117"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/>    | <span data-ttu-id="6de85-118">\[\]其中一個要交換的值。</span><span class="sxs-lookup"><span data-stu-id="6de85-118">\[in\] One of the values to be swapped.</span></span><br/>                                              |
| <span data-ttu-id="6de85-119"><span id="src2"></span><span id="SRC2"></span>*src2 收取*</span><span class="sxs-lookup"><span data-stu-id="6de85-119"><span id="src2"></span><span id="SRC2"></span>*src2*</span></span><br/>    | <span data-ttu-id="6de85-120">\[\]其中一個要交換的值。</span><span class="sxs-lookup"><span data-stu-id="6de85-120">\[in\] One of the values to be swapped.</span></span><br/>                                              |



 

## <a name="remarks"></a><span data-ttu-id="6de85-121">備註</span><span class="sxs-lookup"><span data-stu-id="6de85-121">Remarks</span></span>

<span data-ttu-id="6de85-122">此指示的編碼方式會嘗試在 2 4 元件暫存器中簡潔地多個純量的多重平行條件式交換，而且在結算所涉及的數位配對中，有些許的彈性。</span><span class="sxs-lookup"><span data-stu-id="6de85-122">The encoding of this instruction attempts to compactly express multiple parallel conditional swaps of scalars across two 4-component registers, with minor flexibility in the arrangement of the pairs of numbers involved in swapping.</span></span>

<span data-ttu-id="6de85-123">針對 *src0*、 *src1* 和 *src2 收取* 所選擇的 register 和 value，會以任何方式（例如 [movc](movc--sm4---asm-.md)）進行限制。</span><span class="sxs-lookup"><span data-stu-id="6de85-123">The choice of register and value for *src0*, *src1*, and *src2* are unconstrained in any way, like [movc](movc--sm4---asm-.md).</span></span>

<span data-ttu-id="6de85-124">您可以使用 **movc** 指令，以對等的作業描述此指令的語法。</span><span class="sxs-lookup"><span data-stu-id="6de85-124">The semantics of this instruction can be described by the equivalent operations with the **movc** instruction.</span></span> <span data-ttu-id="6de85-125">最糟的情況會顯示在下列範例中，以確保目的地暫存器不會在結束之前更新。</span><span class="sxs-lookup"><span data-stu-id="6de85-125">The worst case is shown in the following example, making sure destination registers are not updated until the end.</span></span>

``` syntax
                swapc dest0[.mask], 
                      dest1[.mask],
                      src0[.swizzle],
                      src1[.swizzle],
                      src2[.swizzle]

                expands to:

                movc temp[dest0 s mask], 
                     src0[.swizzle], 
                     src2[.swizzle], src1[.swizzle]

                movc dest1[.mask], 
                     src0[.swizzle], 
                     src1[.swizzle], src2[.swizzle]

                mov  dest0.mask, temp
```

<span data-ttu-id="6de85-126">您可以選擇處理工作的方式（如果不是直接）。</span><span class="sxs-lookup"><span data-stu-id="6de85-126">You can choose how to tackle the task, if not directly.</span></span> <span data-ttu-id="6de85-127">例如，相同的效果可以透過一連串最多4個簡單純量條件交換的順序來達成，也可以在上述的兩個向量 **movc** 指令中完成，再加上任何額外負荷，以確保在展開的早期作業中不會事情來源值。</span><span class="sxs-lookup"><span data-stu-id="6de85-127">For example, the same effect can be achieved by a sequence of up to 4 simple scalar conditional swaps, or as above, two vector **movc** instructions, plus any overhead to make sure the source values are not clobbered by earlier operations in the midst of the expansion.</span></span>

<span data-ttu-id="6de85-128">使用此指令進行排序。</span><span class="sxs-lookup"><span data-stu-id="6de85-128">Use this instruction for sorting.</span></span>

<span data-ttu-id="6de85-129">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="6de85-129">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="6de85-130">頂點</span><span class="sxs-lookup"><span data-stu-id="6de85-130">Vertex</span></span> | <span data-ttu-id="6de85-131">船體</span><span class="sxs-lookup"><span data-stu-id="6de85-131">Hull</span></span> | <span data-ttu-id="6de85-132">網域</span><span class="sxs-lookup"><span data-stu-id="6de85-132">Domain</span></span> | <span data-ttu-id="6de85-133">幾何</span><span class="sxs-lookup"><span data-stu-id="6de85-133">Geometry</span></span> | <span data-ttu-id="6de85-134">像素</span><span class="sxs-lookup"><span data-stu-id="6de85-134">Pixel</span></span> | <span data-ttu-id="6de85-135">計算</span><span class="sxs-lookup"><span data-stu-id="6de85-135">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="6de85-136">X</span><span class="sxs-lookup"><span data-stu-id="6de85-136">X</span></span>      | <span data-ttu-id="6de85-137">X</span><span class="sxs-lookup"><span data-stu-id="6de85-137">X</span></span>    | <span data-ttu-id="6de85-138">X</span><span class="sxs-lookup"><span data-stu-id="6de85-138">X</span></span>      | <span data-ttu-id="6de85-139">X</span><span class="sxs-lookup"><span data-stu-id="6de85-139">X</span></span>        | <span data-ttu-id="6de85-140">X</span><span class="sxs-lookup"><span data-stu-id="6de85-140">X</span></span>     | <span data-ttu-id="6de85-141">X</span><span class="sxs-lookup"><span data-stu-id="6de85-141">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="6de85-142">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="6de85-142">Minimum Shader Model</span></span>

<span data-ttu-id="6de85-143">下列著色器模型支援此指令：</span><span class="sxs-lookup"><span data-stu-id="6de85-143">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="6de85-144">著色器模型</span><span class="sxs-lookup"><span data-stu-id="6de85-144">Shader Model</span></span>                                              | <span data-ttu-id="6de85-145">支援</span><span class="sxs-lookup"><span data-stu-id="6de85-145">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="6de85-146">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="6de85-146">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="6de85-147">是</span><span class="sxs-lookup"><span data-stu-id="6de85-147">yes</span></span>       |
| [<span data-ttu-id="6de85-148">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="6de85-148">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="6de85-149">不可以</span><span class="sxs-lookup"><span data-stu-id="6de85-149">no</span></span>        |
| [<span data-ttu-id="6de85-150">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="6de85-150">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="6de85-151">不可以</span><span class="sxs-lookup"><span data-stu-id="6de85-151">no</span></span>        |
| [<span data-ttu-id="6de85-152">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="6de85-152">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="6de85-153">不可以</span><span class="sxs-lookup"><span data-stu-id="6de85-153">no</span></span>        |
| [<span data-ttu-id="6de85-154">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="6de85-154">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="6de85-155">不可以</span><span class="sxs-lookup"><span data-stu-id="6de85-155">no</span></span>        |
| [<span data-ttu-id="6de85-156">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="6de85-156">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="6de85-157">不可以</span><span class="sxs-lookup"><span data-stu-id="6de85-157">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="6de85-158">相關主題</span><span class="sxs-lookup"><span data-stu-id="6de85-158">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6de85-159">著色器模型5元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="6de85-159">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





