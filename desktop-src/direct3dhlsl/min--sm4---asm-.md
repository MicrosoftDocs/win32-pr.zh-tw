---
title: '最小 (sm4-asm) '
description: 元件的最小浮點數。
ms.assetid: 8EDD5503-76D5-4078-BFBA-1DA9260C6E68
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8791589b77edc66eeab4b48f10f4a9b16b5cb2d9
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107993895"
---
# <a name="min-sm4---asm"></a><span data-ttu-id="b206b-103">最小 (sm4-asm) </span><span class="sxs-lookup"><span data-stu-id="b206b-103">min (sm4 - asm)</span></span>

<span data-ttu-id="b206b-104">元件的最小浮點數。</span><span class="sxs-lookup"><span data-stu-id="b206b-104">Component-wise float minimum.</span></span>



| <span data-ttu-id="b206b-105">最小 \[ \_ \] 的 sat 目的地 \[ . mask \] 、 \[ - \] src0 \[ \_ abs \] \[ . swizzle \] 、 \[ - \] src1 \[ \_ abs \] \[ . swizzle \] 、</span><span class="sxs-lookup"><span data-stu-id="b206b-105">min\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\],</span></span> |
|---------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="b206b-106">項目</span><span class="sxs-lookup"><span data-stu-id="b206b-106">Item</span></span>                                                            | <span data-ttu-id="b206b-107">描述</span><span class="sxs-lookup"><span data-stu-id="b206b-107">Description</span></span>                                                                                             |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b206b-108"><span id="dest"></span><span id="DEST"></span>*目標*</span><span class="sxs-lookup"><span data-stu-id="b206b-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="b206b-109">\[在作業的 \] 結果中。</span><span class="sxs-lookup"><span data-stu-id="b206b-109">\[in\] The result of the operation.</span></span><br/> <span data-ttu-id="b206b-110">*目的地*  = *src0*  < *src1* 嗎？</span><span class="sxs-lookup"><span data-stu-id="b206b-110">*dest* = *src0* < *src1* ?</span></span> <span data-ttu-id="b206b-111">*src0* ： *src1*</span><span class="sxs-lookup"><span data-stu-id="b206b-111">*src0* : *src1*</span></span><br/> |
| <span data-ttu-id="b206b-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="b206b-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="b206b-113">\[在 \] [要與 *src1* 比較的元件] 中。</span><span class="sxs-lookup"><span data-stu-id="b206b-113">\[in\] The components to compare to *src1*.</span></span><br/>                                                  |
| <span data-ttu-id="b206b-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="b206b-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="b206b-115">\[在 \] [要與 *src0* 比較的元件] 中。</span><span class="sxs-lookup"><span data-stu-id="b206b-115">\[in\] The components to compare to *src0*.</span></span><br/>                                                  |



 

## <a name="remarks"></a><span data-ttu-id="b206b-116">備註</span><span class="sxs-lookup"><span data-stu-id="b206b-116">Remarks</span></span>

><span data-ttu-id="b206b-117">= 會用來取代 >，因此，如果 min (x、y) = x，則 (x，y) = y 的上限。</span><span class="sxs-lookup"><span data-stu-id="b206b-117">= is used instead of > so that if min(x,y) = x then max(x,y) = y.</span></span>

<span data-ttu-id="b206b-118">NaN 具有特殊處理。</span><span class="sxs-lookup"><span data-stu-id="b206b-118">NaN has special handling.</span></span> <span data-ttu-id="b206b-119">如果一個來源運算元為 NaN，則會傳回另一個來源運算元，並依元件進行選擇。</span><span class="sxs-lookup"><span data-stu-id="b206b-119">If one source operand is NaN, then the other source operand is returned and the choice is made per-component.</span></span> <span data-ttu-id="b206b-120">如果兩者都是 NaN，則會傳回任何 NaN 表示。</span><span class="sxs-lookup"><span data-stu-id="b206b-120">If both are NaN, any NaN representation is returned.</span></span> <span data-ttu-id="b206b-121">這符合新的 IEEE 754R 規則。</span><span class="sxs-lookup"><span data-stu-id="b206b-121">This conforms to new IEEE 754R rules.</span></span>

<span data-ttu-id="b206b-122">在比較之前，會先清除 Denorms 並保留正負號。</span><span class="sxs-lookup"><span data-stu-id="b206b-122">Denorms are flushed, with the sign preserved, before comparison.</span></span> <span data-ttu-id="b206b-123">不過，寫入至 *目的地* 的結果不一定會 denorm 排清。</span><span class="sxs-lookup"><span data-stu-id="b206b-123">However, the result written to *dest* may or may not be denorm flushed.</span></span>

<span data-ttu-id="b206b-124">下表顯示使用各種不同的數位類別來執行指令時所取得的結果，前提是不會發生溢位或下溢。</span><span class="sxs-lookup"><span data-stu-id="b206b-124">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span> <span data-ttu-id="b206b-125">F 表示有限的實數。</span><span class="sxs-lookup"><span data-stu-id="b206b-125">F means finite real number.</span></span>



| <span data-ttu-id="b206b-126">**src0 src1->**</span><span class="sxs-lookup"><span data-stu-id="b206b-126">**src0 src1->**</span></span> | <span data-ttu-id="b206b-127">**-inf**</span><span class="sxs-lookup"><span data-stu-id="b206b-127">**-inf**</span></span> | <span data-ttu-id="b206b-128">**F**</span><span class="sxs-lookup"><span data-stu-id="b206b-128">**F**</span></span>        | <span data-ttu-id="b206b-129">**+ inf**</span><span class="sxs-lookup"><span data-stu-id="b206b-129">**+inf**</span></span> | <span data-ttu-id="b206b-130">**NaN**</span><span class="sxs-lookup"><span data-stu-id="b206b-130">**NaN**</span></span> |
|--------------------|----------|--------------|----------|---------|
| <span data-ttu-id="b206b-131">**-inf**</span><span class="sxs-lookup"><span data-stu-id="b206b-131">**-inf**</span></span>           | <span data-ttu-id="b206b-132">-inf</span><span class="sxs-lookup"><span data-stu-id="b206b-132">-inf</span></span>     | <span data-ttu-id="b206b-133">-inf</span><span class="sxs-lookup"><span data-stu-id="b206b-133">-inf</span></span>         | <span data-ttu-id="b206b-134">-inf</span><span class="sxs-lookup"><span data-stu-id="b206b-134">-inf</span></span>     | <span data-ttu-id="b206b-135">-inf</span><span class="sxs-lookup"><span data-stu-id="b206b-135">-inf</span></span>    |
| <span data-ttu-id="b206b-136">**F**</span><span class="sxs-lookup"><span data-stu-id="b206b-136">**F**</span></span>              | <span data-ttu-id="b206b-137">-inf</span><span class="sxs-lookup"><span data-stu-id="b206b-137">-inf</span></span>     | <span data-ttu-id="b206b-138">src0 或 src1</span><span class="sxs-lookup"><span data-stu-id="b206b-138">src0 or src1</span></span> | <span data-ttu-id="b206b-139">src0</span><span class="sxs-lookup"><span data-stu-id="b206b-139">src0</span></span>     | <span data-ttu-id="b206b-140">src0</span><span class="sxs-lookup"><span data-stu-id="b206b-140">src0</span></span>    |
| <span data-ttu-id="b206b-141">**-inf**</span><span class="sxs-lookup"><span data-stu-id="b206b-141">**-inf**</span></span>           | <span data-ttu-id="b206b-142">-inf</span><span class="sxs-lookup"><span data-stu-id="b206b-142">-inf</span></span>     | <span data-ttu-id="b206b-143">src1</span><span class="sxs-lookup"><span data-stu-id="b206b-143">src1</span></span>         | <span data-ttu-id="b206b-144">+inf</span><span class="sxs-lookup"><span data-stu-id="b206b-144">+inf</span></span>     | <span data-ttu-id="b206b-145">+inf</span><span class="sxs-lookup"><span data-stu-id="b206b-145">+inf</span></span>    |
| <span data-ttu-id="b206b-146">**NaN**</span><span class="sxs-lookup"><span data-stu-id="b206b-146">**NaN**</span></span>            | <span data-ttu-id="b206b-147">-inf</span><span class="sxs-lookup"><span data-stu-id="b206b-147">-inf</span></span>     | <span data-ttu-id="b206b-148">src1</span><span class="sxs-lookup"><span data-stu-id="b206b-148">src1</span></span>         | <span data-ttu-id="b206b-149">+inf</span><span class="sxs-lookup"><span data-stu-id="b206b-149">+inf</span></span>     | <span data-ttu-id="b206b-150">NaN</span><span class="sxs-lookup"><span data-stu-id="b206b-150">NaN</span></span>     |



 

<span data-ttu-id="b206b-151">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="b206b-151">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="b206b-152">頂點著色器</span><span class="sxs-lookup"><span data-stu-id="b206b-152">Vertex Shader</span></span> | <span data-ttu-id="b206b-153">幾何著色器</span><span class="sxs-lookup"><span data-stu-id="b206b-153">Geometry Shader</span></span> | <span data-ttu-id="b206b-154">像素著色器</span><span class="sxs-lookup"><span data-stu-id="b206b-154">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="b206b-155">x</span><span class="sxs-lookup"><span data-stu-id="b206b-155">x</span></span>             | <span data-ttu-id="b206b-156">x</span><span class="sxs-lookup"><span data-stu-id="b206b-156">x</span></span>               | <span data-ttu-id="b206b-157">x</span><span class="sxs-lookup"><span data-stu-id="b206b-157">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="b206b-158">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="b206b-158">Minimum Shader Model</span></span>

<span data-ttu-id="b206b-159">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="b206b-159">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="b206b-160">著色器模型</span><span class="sxs-lookup"><span data-stu-id="b206b-160">Shader Model</span></span>                                              | <span data-ttu-id="b206b-161">支援</span><span class="sxs-lookup"><span data-stu-id="b206b-161">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="b206b-162">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="b206b-162">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="b206b-163">是</span><span class="sxs-lookup"><span data-stu-id="b206b-163">yes</span></span>       |
| [<span data-ttu-id="b206b-164">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="b206b-164">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="b206b-165">是</span><span class="sxs-lookup"><span data-stu-id="b206b-165">yes</span></span>       |
| [<span data-ttu-id="b206b-166">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="b206b-166">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="b206b-167">是</span><span class="sxs-lookup"><span data-stu-id="b206b-167">yes</span></span>       |
| [<span data-ttu-id="b206b-168">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="b206b-168">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="b206b-169">否</span><span class="sxs-lookup"><span data-stu-id="b206b-169">no</span></span>        |
| [<span data-ttu-id="b206b-170">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="b206b-170">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="b206b-171">否</span><span class="sxs-lookup"><span data-stu-id="b206b-171">no</span></span>        |
| [<span data-ttu-id="b206b-172">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="b206b-172">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="b206b-173">否</span><span class="sxs-lookup"><span data-stu-id="b206b-173">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="b206b-174">相關主題</span><span class="sxs-lookup"><span data-stu-id="b206b-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b206b-175">著色器模型4元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="b206b-175">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





