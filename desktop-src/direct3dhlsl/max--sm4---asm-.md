---
title: 'max (sm4-asm) '
description: 元件的最大浮點數。
ms.assetid: 005468AA-577E-441F-ACD5-37A691E62CDD
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f64d88c581828f2563f6d5d8a6c57de6400f9bbf
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994725"
---
# <a name="max-sm4---asm"></a><span data-ttu-id="60467-103">max (sm4-asm) </span><span class="sxs-lookup"><span data-stu-id="60467-103">max (sm4 - asm)</span></span>

<span data-ttu-id="60467-104">元件的最大浮點數。</span><span class="sxs-lookup"><span data-stu-id="60467-104">Component-wise float maximum.</span></span>



| <span data-ttu-id="60467-105">最大 \[ \_ sat \] 目的地 \[ . mask \] 、 \[ - \] src0 \[ \_ abs \] \[ . swizzle \] 、 \[ - \] src1 \[ \_ abs \] \[ . swizzle \] 、</span><span class="sxs-lookup"><span data-stu-id="60467-105">max\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\],</span></span> |
|---------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="60467-106">項目</span><span class="sxs-lookup"><span data-stu-id="60467-106">Item</span></span>                                                            | <span data-ttu-id="60467-107">描述</span><span class="sxs-lookup"><span data-stu-id="60467-107">Description</span></span>                                                                                               |
|-----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60467-108"><span id="dest"></span><span id="DEST"></span>*目標*</span><span class="sxs-lookup"><span data-stu-id="60467-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="60467-109">\[在作業的 \] 結果中。</span><span class="sxs-lookup"><span data-stu-id="60467-109">\[in\] The result of the operation.</span></span> <br/> <span data-ttu-id="60467-110">*目的地*  = *src0*  >= *src1* 嗎？</span><span class="sxs-lookup"><span data-stu-id="60467-110">*dest* = *src0* >= *src1* ?</span></span> <span data-ttu-id="60467-111">*src0* ： *src1*</span><span class="sxs-lookup"><span data-stu-id="60467-111">*src0* : *src1*</span></span><br/> |
| <span data-ttu-id="60467-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="60467-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="60467-113">\[在 \] [要與 *src1* 比較的元件] 中。</span><span class="sxs-lookup"><span data-stu-id="60467-113">\[in\] The components to compare to *src1*.</span></span><br/>                                                    |
| <span data-ttu-id="60467-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="60467-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="60467-115">\[在 \] [要與 *src0* 比較的元件] 中。</span><span class="sxs-lookup"><span data-stu-id="60467-115">\[in\] The components to compare to *src0*.</span></span><br/>                                                    |



 

## <a name="remarks"></a><span data-ttu-id="60467-116">備註</span><span class="sxs-lookup"><span data-stu-id="60467-116">Remarks</span></span>

><span data-ttu-id="60467-117">= 會用來取代 >，因此，如果 min (x、y) = x，則 (x，y) = y 的上限。</span><span class="sxs-lookup"><span data-stu-id="60467-117">= is used instead of > so that if min(x,y) = x then max(x,y) = y.</span></span>

<span data-ttu-id="60467-118">NaN 具有特殊處理。</span><span class="sxs-lookup"><span data-stu-id="60467-118">NaN has special handling.</span></span> <span data-ttu-id="60467-119">如果一個來源運算元為 NaN，則會傳回另一個來源運算元，並依元件進行選擇。</span><span class="sxs-lookup"><span data-stu-id="60467-119">If one source operand is NaN, then the other source operand is returned and the choice is made per-component.</span></span> <span data-ttu-id="60467-120">如果兩者都是 NaN，則會傳回任何 NaN 表示。</span><span class="sxs-lookup"><span data-stu-id="60467-120">If both are NaN, any NaN representation is returned.</span></span>

<span data-ttu-id="60467-121">在進行比較之前，會先將 Denorms 排清並保留正負號。</span><span class="sxs-lookup"><span data-stu-id="60467-121">Denorms are flushed with sign preserved before the comparison.</span></span> <span data-ttu-id="60467-122">不過，寫入至 *目的地* 的結果不一定會 denorm 排清。</span><span class="sxs-lookup"><span data-stu-id="60467-122">However, the result written to *dest* may or may not be denorm flushed.</span></span>

<span data-ttu-id="60467-123">下表顯示使用各種不同的數位類別來執行指令時所取得的結果，前提是不會發生溢位或下溢。</span><span class="sxs-lookup"><span data-stu-id="60467-123">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span> <span data-ttu-id="60467-124">F 表示有限的實數。</span><span class="sxs-lookup"><span data-stu-id="60467-124">F means finite real number.</span></span>



| <span data-ttu-id="60467-125">**src0 src1->**</span><span class="sxs-lookup"><span data-stu-id="60467-125">**src0 src1->**</span></span> | <span data-ttu-id="60467-126">**-inf**</span><span class="sxs-lookup"><span data-stu-id="60467-126">**-inf**</span></span> | <span data-ttu-id="60467-127">**F**</span><span class="sxs-lookup"><span data-stu-id="60467-127">**F**</span></span>        | <span data-ttu-id="60467-128">**+ inf**</span><span class="sxs-lookup"><span data-stu-id="60467-128">**+inf**</span></span> | <span data-ttu-id="60467-129">**NaN**</span><span class="sxs-lookup"><span data-stu-id="60467-129">**NaN**</span></span> |
|--------------------|----------|--------------|----------|---------|
| <span data-ttu-id="60467-130">**-inf**</span><span class="sxs-lookup"><span data-stu-id="60467-130">**-inf**</span></span>           | <span data-ttu-id="60467-131">-inf</span><span class="sxs-lookup"><span data-stu-id="60467-131">-inf</span></span>     | <span data-ttu-id="60467-132">src1</span><span class="sxs-lookup"><span data-stu-id="60467-132">src1</span></span>         | <span data-ttu-id="60467-133">+inf</span><span class="sxs-lookup"><span data-stu-id="60467-133">+inf</span></span>     | <span data-ttu-id="60467-134">-inf</span><span class="sxs-lookup"><span data-stu-id="60467-134">-inf</span></span>    |
| <span data-ttu-id="60467-135">**F**</span><span class="sxs-lookup"><span data-stu-id="60467-135">**F**</span></span>              | <span data-ttu-id="60467-136">src0</span><span class="sxs-lookup"><span data-stu-id="60467-136">src0</span></span>     | <span data-ttu-id="60467-137">src0 或 src1</span><span class="sxs-lookup"><span data-stu-id="60467-137">src0 or src1</span></span> | <span data-ttu-id="60467-138">+inf</span><span class="sxs-lookup"><span data-stu-id="60467-138">+inf</span></span>     | <span data-ttu-id="60467-139">src0</span><span class="sxs-lookup"><span data-stu-id="60467-139">src0</span></span>    |
| <span data-ttu-id="60467-140">**+ inf**</span><span class="sxs-lookup"><span data-stu-id="60467-140">**+inf**</span></span>           | <span data-ttu-id="60467-141">+inf</span><span class="sxs-lookup"><span data-stu-id="60467-141">+inf</span></span>     | <span data-ttu-id="60467-142">+inf</span><span class="sxs-lookup"><span data-stu-id="60467-142">+inf</span></span>         | <span data-ttu-id="60467-143">+inf</span><span class="sxs-lookup"><span data-stu-id="60467-143">+inf</span></span>     | <span data-ttu-id="60467-144">+inf</span><span class="sxs-lookup"><span data-stu-id="60467-144">+inf</span></span>    |
| <span data-ttu-id="60467-145">**NaN**</span><span class="sxs-lookup"><span data-stu-id="60467-145">**NaN**</span></span>            | <span data-ttu-id="60467-146">-inf</span><span class="sxs-lookup"><span data-stu-id="60467-146">-inf</span></span>     | <span data-ttu-id="60467-147">src1</span><span class="sxs-lookup"><span data-stu-id="60467-147">src1</span></span>         | <span data-ttu-id="60467-148">+inf</span><span class="sxs-lookup"><span data-stu-id="60467-148">+inf</span></span>     | <span data-ttu-id="60467-149">NaN</span><span class="sxs-lookup"><span data-stu-id="60467-149">NaN</span></span>     |



 

<span data-ttu-id="60467-150">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="60467-150">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="60467-151">頂點著色器</span><span class="sxs-lookup"><span data-stu-id="60467-151">Vertex Shader</span></span> | <span data-ttu-id="60467-152">幾何著色器</span><span class="sxs-lookup"><span data-stu-id="60467-152">Geometry Shader</span></span> | <span data-ttu-id="60467-153">像素著色器</span><span class="sxs-lookup"><span data-stu-id="60467-153">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="60467-154">x</span><span class="sxs-lookup"><span data-stu-id="60467-154">x</span></span>             | <span data-ttu-id="60467-155">x</span><span class="sxs-lookup"><span data-stu-id="60467-155">x</span></span>               | <span data-ttu-id="60467-156">x</span><span class="sxs-lookup"><span data-stu-id="60467-156">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="60467-157">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="60467-157">Minimum Shader Model</span></span>

<span data-ttu-id="60467-158">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="60467-158">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="60467-159">著色器模型</span><span class="sxs-lookup"><span data-stu-id="60467-159">Shader Model</span></span>                                              | <span data-ttu-id="60467-160">支援</span><span class="sxs-lookup"><span data-stu-id="60467-160">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="60467-161">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="60467-161">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="60467-162">是</span><span class="sxs-lookup"><span data-stu-id="60467-162">yes</span></span>       |
| [<span data-ttu-id="60467-163">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="60467-163">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="60467-164">是</span><span class="sxs-lookup"><span data-stu-id="60467-164">yes</span></span>       |
| [<span data-ttu-id="60467-165">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="60467-165">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="60467-166">是</span><span class="sxs-lookup"><span data-stu-id="60467-166">yes</span></span>       |
| [<span data-ttu-id="60467-167">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="60467-167">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="60467-168">否</span><span class="sxs-lookup"><span data-stu-id="60467-168">no</span></span>        |
| [<span data-ttu-id="60467-169">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="60467-169">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="60467-170">否</span><span class="sxs-lookup"><span data-stu-id="60467-170">no</span></span>        |
| [<span data-ttu-id="60467-171">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="60467-171">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="60467-172">否</span><span class="sxs-lookup"><span data-stu-id="60467-172">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="60467-173">相關主題</span><span class="sxs-lookup"><span data-stu-id="60467-173">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="60467-174">著色器模型4元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="60467-174">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





