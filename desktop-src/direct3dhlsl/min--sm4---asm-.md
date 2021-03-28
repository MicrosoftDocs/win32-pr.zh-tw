---
title: '最小 (sm4-asm) '
description: 元件的最小浮點數。
ms.assetid: 8EDD5503-76D5-4078-BFBA-1DA9260C6E68
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e584aee077735b717bf76d148d4d0db4357a7d95
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104092465"
---
# <a name="min-sm4---asm"></a><span data-ttu-id="414b7-103">最小 (sm4-asm) </span><span class="sxs-lookup"><span data-stu-id="414b7-103">min (sm4 - asm)</span></span>

<span data-ttu-id="414b7-104">元件的最小浮點數。</span><span class="sxs-lookup"><span data-stu-id="414b7-104">Component-wise float minimum.</span></span>



| <span data-ttu-id="414b7-105">最小 \[ \_ \] 的 sat 目的地 \[ . mask \] 、 \[ - \] src0 \[ \_ abs \] \[ . swizzle \] 、 \[ - \] src1 \[ \_ abs \] \[ . swizzle \] 、</span><span class="sxs-lookup"><span data-stu-id="414b7-105">min\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\],</span></span> |
|---------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="414b7-106">項目</span><span class="sxs-lookup"><span data-stu-id="414b7-106">Item</span></span>                                                            | <span data-ttu-id="414b7-107">描述</span><span class="sxs-lookup"><span data-stu-id="414b7-107">Description</span></span>                                                                                             |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="414b7-108"><span id="dest"></span><span id="DEST"></span>*目標*</span><span class="sxs-lookup"><span data-stu-id="414b7-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="414b7-109">\[在作業的 \] 結果中。</span><span class="sxs-lookup"><span data-stu-id="414b7-109">\[in\] The result of the operation.</span></span><br/> <span data-ttu-id="414b7-110">*目的地*  = *src0*  < *src1* 嗎？</span><span class="sxs-lookup"><span data-stu-id="414b7-110">*dest* = *src0* < *src1* ?</span></span> <span data-ttu-id="414b7-111">*src0* ： *src1*</span><span class="sxs-lookup"><span data-stu-id="414b7-111">*src0* : *src1*</span></span><br/> |
| <span data-ttu-id="414b7-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="414b7-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="414b7-113">\[在 \] [要與 *src1* 比較的元件] 中。</span><span class="sxs-lookup"><span data-stu-id="414b7-113">\[in\] The components to compare to *src1*.</span></span><br/>                                                  |
| <span data-ttu-id="414b7-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="414b7-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="414b7-115">\[在 \] [要與 *src0* 比較的元件] 中。</span><span class="sxs-lookup"><span data-stu-id="414b7-115">\[in\] The components to compare to *src0*.</span></span><br/>                                                  |



 

## <a name="remarks"></a><span data-ttu-id="414b7-116">備註</span><span class="sxs-lookup"><span data-stu-id="414b7-116">Remarks</span></span>

><span data-ttu-id="414b7-117">= 會用來取代 >，因此，如果 min (x、y) = x，則 (x，y) = y 的上限。</span><span class="sxs-lookup"><span data-stu-id="414b7-117">= is used instead of > so that if min(x,y) = x then max(x,y) = y.</span></span>

<span data-ttu-id="414b7-118">NaN 具有特殊處理。</span><span class="sxs-lookup"><span data-stu-id="414b7-118">NaN has special handling.</span></span> <span data-ttu-id="414b7-119">如果一個來源運算元為 NaN，則會傳回另一個來源運算元，並依元件進行選擇。</span><span class="sxs-lookup"><span data-stu-id="414b7-119">If one source operand is NaN, then the other source operand is returned and the choice is made per-component.</span></span> <span data-ttu-id="414b7-120">如果兩者都是 NaN，則會傳回任何 NaN 表示。</span><span class="sxs-lookup"><span data-stu-id="414b7-120">If both are NaN, any NaN representation is returned.</span></span> <span data-ttu-id="414b7-121">這符合新的 IEEE 754R 規則。</span><span class="sxs-lookup"><span data-stu-id="414b7-121">This conforms to new IEEE 754R rules.</span></span>

<span data-ttu-id="414b7-122">在比較之前，會先清除 Denorms 並保留正負號。</span><span class="sxs-lookup"><span data-stu-id="414b7-122">Denorms are flushed, with the sign preserved, before comparison.</span></span> <span data-ttu-id="414b7-123">不過，寫入至 *目的地* 的結果不一定會 denorm 排清。</span><span class="sxs-lookup"><span data-stu-id="414b7-123">However, the result written to *dest* may or may not be denorm flushed.</span></span>

<span data-ttu-id="414b7-124">下表顯示使用各種不同的數位類別來執行指令時所取得的結果，前提是不會發生溢位或下溢。</span><span class="sxs-lookup"><span data-stu-id="414b7-124">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span> <span data-ttu-id="414b7-125">F 表示有限的實數。</span><span class="sxs-lookup"><span data-stu-id="414b7-125">F means finite real number.</span></span>



|                    |          |              |          |         |
|--------------------|----------|--------------|----------|---------|
| <span data-ttu-id="414b7-126">**src0 src1->**</span><span class="sxs-lookup"><span data-stu-id="414b7-126">**src0 src1->**</span></span> | <span data-ttu-id="414b7-127">**-inf**</span><span class="sxs-lookup"><span data-stu-id="414b7-127">**-inf**</span></span> | <span data-ttu-id="414b7-128">**F**</span><span class="sxs-lookup"><span data-stu-id="414b7-128">**F**</span></span>        | <span data-ttu-id="414b7-129">**+ inf**</span><span class="sxs-lookup"><span data-stu-id="414b7-129">**+inf**</span></span> | <span data-ttu-id="414b7-130">**NaN**</span><span class="sxs-lookup"><span data-stu-id="414b7-130">**NaN**</span></span> |
| <span data-ttu-id="414b7-131">**-inf**</span><span class="sxs-lookup"><span data-stu-id="414b7-131">**-inf**</span></span>           | <span data-ttu-id="414b7-132">-inf</span><span class="sxs-lookup"><span data-stu-id="414b7-132">-inf</span></span>     | <span data-ttu-id="414b7-133">-inf</span><span class="sxs-lookup"><span data-stu-id="414b7-133">-inf</span></span>         | <span data-ttu-id="414b7-134">-inf</span><span class="sxs-lookup"><span data-stu-id="414b7-134">-inf</span></span>     | <span data-ttu-id="414b7-135">-inf</span><span class="sxs-lookup"><span data-stu-id="414b7-135">-inf</span></span>    |
| <span data-ttu-id="414b7-136">**F**</span><span class="sxs-lookup"><span data-stu-id="414b7-136">**F**</span></span>              | <span data-ttu-id="414b7-137">-inf</span><span class="sxs-lookup"><span data-stu-id="414b7-137">-inf</span></span>     | <span data-ttu-id="414b7-138">src0 或 src1</span><span class="sxs-lookup"><span data-stu-id="414b7-138">src0 or src1</span></span> | <span data-ttu-id="414b7-139">src0</span><span class="sxs-lookup"><span data-stu-id="414b7-139">src0</span></span>     | <span data-ttu-id="414b7-140">src0</span><span class="sxs-lookup"><span data-stu-id="414b7-140">src0</span></span>    |
| <span data-ttu-id="414b7-141">**-inf**</span><span class="sxs-lookup"><span data-stu-id="414b7-141">**-inf**</span></span>           | <span data-ttu-id="414b7-142">-inf</span><span class="sxs-lookup"><span data-stu-id="414b7-142">-inf</span></span>     | <span data-ttu-id="414b7-143">src1</span><span class="sxs-lookup"><span data-stu-id="414b7-143">src1</span></span>         | <span data-ttu-id="414b7-144">+inf</span><span class="sxs-lookup"><span data-stu-id="414b7-144">+inf</span></span>     | <span data-ttu-id="414b7-145">+inf</span><span class="sxs-lookup"><span data-stu-id="414b7-145">+inf</span></span>    |
| <span data-ttu-id="414b7-146">**NaN**</span><span class="sxs-lookup"><span data-stu-id="414b7-146">**NaN**</span></span>            | <span data-ttu-id="414b7-147">-inf</span><span class="sxs-lookup"><span data-stu-id="414b7-147">-inf</span></span>     | <span data-ttu-id="414b7-148">src1</span><span class="sxs-lookup"><span data-stu-id="414b7-148">src1</span></span>         | <span data-ttu-id="414b7-149">+inf</span><span class="sxs-lookup"><span data-stu-id="414b7-149">+inf</span></span>     | <span data-ttu-id="414b7-150">NaN</span><span class="sxs-lookup"><span data-stu-id="414b7-150">NaN</span></span>     |



 

<span data-ttu-id="414b7-151">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="414b7-151">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="414b7-152">頂點著色器</span><span class="sxs-lookup"><span data-stu-id="414b7-152">Vertex Shader</span></span> | <span data-ttu-id="414b7-153">幾何著色器</span><span class="sxs-lookup"><span data-stu-id="414b7-153">Geometry Shader</span></span> | <span data-ttu-id="414b7-154">像素著色器</span><span class="sxs-lookup"><span data-stu-id="414b7-154">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="414b7-155">x</span><span class="sxs-lookup"><span data-stu-id="414b7-155">x</span></span>             | <span data-ttu-id="414b7-156">x</span><span class="sxs-lookup"><span data-stu-id="414b7-156">x</span></span>               | <span data-ttu-id="414b7-157">x</span><span class="sxs-lookup"><span data-stu-id="414b7-157">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="414b7-158">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="414b7-158">Minimum Shader Model</span></span>

<span data-ttu-id="414b7-159">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="414b7-159">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="414b7-160">著色器模型</span><span class="sxs-lookup"><span data-stu-id="414b7-160">Shader Model</span></span>                                              | <span data-ttu-id="414b7-161">支援</span><span class="sxs-lookup"><span data-stu-id="414b7-161">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="414b7-162">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="414b7-162">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="414b7-163">是</span><span class="sxs-lookup"><span data-stu-id="414b7-163">yes</span></span>       |
| [<span data-ttu-id="414b7-164">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="414b7-164">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="414b7-165">是</span><span class="sxs-lookup"><span data-stu-id="414b7-165">yes</span></span>       |
| [<span data-ttu-id="414b7-166">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="414b7-166">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="414b7-167">是</span><span class="sxs-lookup"><span data-stu-id="414b7-167">yes</span></span>       |
| [<span data-ttu-id="414b7-168">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="414b7-168">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="414b7-169">不可以</span><span class="sxs-lookup"><span data-stu-id="414b7-169">no</span></span>        |
| [<span data-ttu-id="414b7-170">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="414b7-170">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="414b7-171">不可以</span><span class="sxs-lookup"><span data-stu-id="414b7-171">no</span></span>        |
| [<span data-ttu-id="414b7-172">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="414b7-172">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="414b7-173">不可以</span><span class="sxs-lookup"><span data-stu-id="414b7-173">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="414b7-174">相關主題</span><span class="sxs-lookup"><span data-stu-id="414b7-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="414b7-175">著色器模型4元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="414b7-175">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





