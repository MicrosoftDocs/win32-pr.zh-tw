---
title: 'max (sm4-asm) '
description: 元件的最大浮點數。
ms.assetid: 005468AA-577E-441F-ACD5-37A691E62CDD
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f24618897eacf250f2b924f6dde3745a32a7172
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104373722"
---
# <a name="max-sm4---asm"></a><span data-ttu-id="80a8b-103">max (sm4-asm) </span><span class="sxs-lookup"><span data-stu-id="80a8b-103">max (sm4 - asm)</span></span>

<span data-ttu-id="80a8b-104">元件的最大浮點數。</span><span class="sxs-lookup"><span data-stu-id="80a8b-104">Component-wise float maximum.</span></span>



| <span data-ttu-id="80a8b-105">最大 \[ \_ sat \] 目的地 \[ . mask \] 、 \[ - \] src0 \[ \_ abs \] \[ . swizzle \] 、 \[ - \] src1 \[ \_ abs \] \[ . swizzle \] 、</span><span class="sxs-lookup"><span data-stu-id="80a8b-105">max\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\],</span></span> |
|---------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="80a8b-106">項目</span><span class="sxs-lookup"><span data-stu-id="80a8b-106">Item</span></span>                                                            | <span data-ttu-id="80a8b-107">描述</span><span class="sxs-lookup"><span data-stu-id="80a8b-107">Description</span></span>                                                                                               |
|-----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80a8b-108"><span id="dest"></span><span id="DEST"></span>*目標*</span><span class="sxs-lookup"><span data-stu-id="80a8b-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="80a8b-109">\[在作業的 \] 結果中。</span><span class="sxs-lookup"><span data-stu-id="80a8b-109">\[in\] The result of the operation.</span></span> <br/> <span data-ttu-id="80a8b-110">*目的地*  = *src0*  >= *src1* 嗎？</span><span class="sxs-lookup"><span data-stu-id="80a8b-110">*dest* = *src0* >= *src1* ?</span></span> <span data-ttu-id="80a8b-111">*src0* ： *src1*</span><span class="sxs-lookup"><span data-stu-id="80a8b-111">*src0* : *src1*</span></span><br/> |
| <span data-ttu-id="80a8b-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="80a8b-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="80a8b-113">\[在 \] [要與 *src1* 比較的元件] 中。</span><span class="sxs-lookup"><span data-stu-id="80a8b-113">\[in\] The components to compare to *src1*.</span></span><br/>                                                    |
| <span data-ttu-id="80a8b-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="80a8b-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="80a8b-115">\[在 \] [要與 *src0* 比較的元件] 中。</span><span class="sxs-lookup"><span data-stu-id="80a8b-115">\[in\] The components to compare to *src0*.</span></span><br/>                                                    |



 

## <a name="remarks"></a><span data-ttu-id="80a8b-116">備註</span><span class="sxs-lookup"><span data-stu-id="80a8b-116">Remarks</span></span>

><span data-ttu-id="80a8b-117">= 會用來取代 >，因此，如果 min (x、y) = x，則 (x，y) = y 的上限。</span><span class="sxs-lookup"><span data-stu-id="80a8b-117">= is used instead of > so that if min(x,y) = x then max(x,y) = y.</span></span>

<span data-ttu-id="80a8b-118">NaN 具有特殊處理。</span><span class="sxs-lookup"><span data-stu-id="80a8b-118">NaN has special handling.</span></span> <span data-ttu-id="80a8b-119">如果一個來源運算元為 NaN，則會傳回另一個來源運算元，並依元件進行選擇。</span><span class="sxs-lookup"><span data-stu-id="80a8b-119">If one source operand is NaN, then the other source operand is returned and the choice is made per-component.</span></span> <span data-ttu-id="80a8b-120">如果兩者都是 NaN，則會傳回任何 NaN 表示。</span><span class="sxs-lookup"><span data-stu-id="80a8b-120">If both are NaN, any NaN representation is returned.</span></span>

<span data-ttu-id="80a8b-121">在進行比較之前，會先將 Denorms 排清並保留正負號。</span><span class="sxs-lookup"><span data-stu-id="80a8b-121">Denorms are flushed with sign preserved before the comparison.</span></span> <span data-ttu-id="80a8b-122">不過，寫入至 *目的地* 的結果不一定會 denorm 排清。</span><span class="sxs-lookup"><span data-stu-id="80a8b-122">However, the result written to *dest* may or may not be denorm flushed.</span></span>

<span data-ttu-id="80a8b-123">下表顯示使用各種不同的數位類別來執行指令時所取得的結果，前提是不會發生溢位或下溢。</span><span class="sxs-lookup"><span data-stu-id="80a8b-123">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span> <span data-ttu-id="80a8b-124">F 表示有限的實數。</span><span class="sxs-lookup"><span data-stu-id="80a8b-124">F means finite real number.</span></span>



|                    |          |              |          |         |
|--------------------|----------|--------------|----------|---------|
| <span data-ttu-id="80a8b-125">**src0 src1->**</span><span class="sxs-lookup"><span data-stu-id="80a8b-125">**src0 src1->**</span></span> | <span data-ttu-id="80a8b-126">**-inf**</span><span class="sxs-lookup"><span data-stu-id="80a8b-126">**-inf**</span></span> | <span data-ttu-id="80a8b-127">**F**</span><span class="sxs-lookup"><span data-stu-id="80a8b-127">**F**</span></span>        | <span data-ttu-id="80a8b-128">**+ inf**</span><span class="sxs-lookup"><span data-stu-id="80a8b-128">**+inf**</span></span> | <span data-ttu-id="80a8b-129">**NaN**</span><span class="sxs-lookup"><span data-stu-id="80a8b-129">**NaN**</span></span> |
| <span data-ttu-id="80a8b-130">**-inf**</span><span class="sxs-lookup"><span data-stu-id="80a8b-130">**-inf**</span></span>           | <span data-ttu-id="80a8b-131">-inf</span><span class="sxs-lookup"><span data-stu-id="80a8b-131">-inf</span></span>     | <span data-ttu-id="80a8b-132">src1</span><span class="sxs-lookup"><span data-stu-id="80a8b-132">src1</span></span>         | <span data-ttu-id="80a8b-133">+inf</span><span class="sxs-lookup"><span data-stu-id="80a8b-133">+inf</span></span>     | <span data-ttu-id="80a8b-134">-inf</span><span class="sxs-lookup"><span data-stu-id="80a8b-134">-inf</span></span>    |
| <span data-ttu-id="80a8b-135">**F**</span><span class="sxs-lookup"><span data-stu-id="80a8b-135">**F**</span></span>              | <span data-ttu-id="80a8b-136">src0</span><span class="sxs-lookup"><span data-stu-id="80a8b-136">src0</span></span>     | <span data-ttu-id="80a8b-137">src0 或 src1</span><span class="sxs-lookup"><span data-stu-id="80a8b-137">src0 or src1</span></span> | <span data-ttu-id="80a8b-138">+inf</span><span class="sxs-lookup"><span data-stu-id="80a8b-138">+inf</span></span>     | <span data-ttu-id="80a8b-139">src0</span><span class="sxs-lookup"><span data-stu-id="80a8b-139">src0</span></span>    |
| <span data-ttu-id="80a8b-140">**+ inf**</span><span class="sxs-lookup"><span data-stu-id="80a8b-140">**+inf**</span></span>           | <span data-ttu-id="80a8b-141">+inf</span><span class="sxs-lookup"><span data-stu-id="80a8b-141">+inf</span></span>     | <span data-ttu-id="80a8b-142">+inf</span><span class="sxs-lookup"><span data-stu-id="80a8b-142">+inf</span></span>         | <span data-ttu-id="80a8b-143">+inf</span><span class="sxs-lookup"><span data-stu-id="80a8b-143">+inf</span></span>     | <span data-ttu-id="80a8b-144">+inf</span><span class="sxs-lookup"><span data-stu-id="80a8b-144">+inf</span></span>    |
| <span data-ttu-id="80a8b-145">**NaN**</span><span class="sxs-lookup"><span data-stu-id="80a8b-145">**NaN**</span></span>            | <span data-ttu-id="80a8b-146">-inf</span><span class="sxs-lookup"><span data-stu-id="80a8b-146">-inf</span></span>     | <span data-ttu-id="80a8b-147">src1</span><span class="sxs-lookup"><span data-stu-id="80a8b-147">src1</span></span>         | <span data-ttu-id="80a8b-148">+inf</span><span class="sxs-lookup"><span data-stu-id="80a8b-148">+inf</span></span>     | <span data-ttu-id="80a8b-149">NaN</span><span class="sxs-lookup"><span data-stu-id="80a8b-149">NaN</span></span>     |



 

<span data-ttu-id="80a8b-150">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="80a8b-150">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="80a8b-151">頂點著色器</span><span class="sxs-lookup"><span data-stu-id="80a8b-151">Vertex Shader</span></span> | <span data-ttu-id="80a8b-152">幾何著色器</span><span class="sxs-lookup"><span data-stu-id="80a8b-152">Geometry Shader</span></span> | <span data-ttu-id="80a8b-153">像素著色器</span><span class="sxs-lookup"><span data-stu-id="80a8b-153">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="80a8b-154">x</span><span class="sxs-lookup"><span data-stu-id="80a8b-154">x</span></span>             | <span data-ttu-id="80a8b-155">x</span><span class="sxs-lookup"><span data-stu-id="80a8b-155">x</span></span>               | <span data-ttu-id="80a8b-156">x</span><span class="sxs-lookup"><span data-stu-id="80a8b-156">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="80a8b-157">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="80a8b-157">Minimum Shader Model</span></span>

<span data-ttu-id="80a8b-158">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="80a8b-158">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="80a8b-159">著色器模型</span><span class="sxs-lookup"><span data-stu-id="80a8b-159">Shader Model</span></span>                                              | <span data-ttu-id="80a8b-160">支援</span><span class="sxs-lookup"><span data-stu-id="80a8b-160">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="80a8b-161">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="80a8b-161">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="80a8b-162">是</span><span class="sxs-lookup"><span data-stu-id="80a8b-162">yes</span></span>       |
| [<span data-ttu-id="80a8b-163">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="80a8b-163">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="80a8b-164">是</span><span class="sxs-lookup"><span data-stu-id="80a8b-164">yes</span></span>       |
| [<span data-ttu-id="80a8b-165">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="80a8b-165">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="80a8b-166">是</span><span class="sxs-lookup"><span data-stu-id="80a8b-166">yes</span></span>       |
| [<span data-ttu-id="80a8b-167">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="80a8b-167">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="80a8b-168">不可以</span><span class="sxs-lookup"><span data-stu-id="80a8b-168">no</span></span>        |
| [<span data-ttu-id="80a8b-169">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="80a8b-169">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="80a8b-170">不可以</span><span class="sxs-lookup"><span data-stu-id="80a8b-170">no</span></span>        |
| [<span data-ttu-id="80a8b-171">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="80a8b-171">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="80a8b-172">不可以</span><span class="sxs-lookup"><span data-stu-id="80a8b-172">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="80a8b-173">相關主題</span><span class="sxs-lookup"><span data-stu-id="80a8b-173">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="80a8b-174">著色器模型4元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="80a8b-174">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





