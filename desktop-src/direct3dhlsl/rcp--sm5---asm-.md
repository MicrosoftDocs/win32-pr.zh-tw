---
title: 'rcp (sm5-asm) '
description: 元件的相互比較。
ms.assetid: 499A14D6-36DB-4860-94D1-887D931E60D4
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abbaa2ffc29a4c3373009d9dec1b895710186e67
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104507732"
---
# <a name="rcp-sm5---asm"></a><span data-ttu-id="4f29e-103">rcp (sm5-asm) </span><span class="sxs-lookup"><span data-stu-id="4f29e-103">rcp (sm5 - asm)</span></span>

<span data-ttu-id="4f29e-104">元件的相互比較。</span><span class="sxs-lookup"><span data-stu-id="4f29e-104">Component-wise reciprocal.</span></span>



| <span data-ttu-id="4f29e-105">rcp \[ \_ sat \] dest \[ \] 、 \[ - \] src0 \[ \_ abs \] \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="4f29e-105">rcp\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|------------------------------------------------------------|



 



| <span data-ttu-id="4f29e-106">項目</span><span class="sxs-lookup"><span data-stu-id="4f29e-106">Item</span></span>                                                            | <span data-ttu-id="4f29e-107">描述</span><span class="sxs-lookup"><span data-stu-id="4f29e-107">Description</span></span>                                                                         |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="4f29e-108"><span id="dest"></span><span id="DEST"></span>*目標*</span><span class="sxs-lookup"><span data-stu-id="4f29e-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="4f29e-109">\[在 \] 結果的位址中</span><span class="sxs-lookup"><span data-stu-id="4f29e-109">\[in\] The address of the results</span></span><br/> <span data-ttu-id="4f29e-110">*目的地*  = **1.0 f**  / *src0*。</span><span class="sxs-lookup"><span data-stu-id="4f29e-110">*dest* = **1.0f** / *src0*.</span></span><br/> |
| <span data-ttu-id="4f29e-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="4f29e-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="4f29e-112">\[\]要採用的數位。</span><span class="sxs-lookup"><span data-stu-id="4f29e-112">\[in\] The number to take the reciprocal of.</span></span><br/>                             |



 

## <a name="remarks"></a><span data-ttu-id="4f29e-113">備註</span><span class="sxs-lookup"><span data-stu-id="4f29e-113">Remarks</span></span>

<span data-ttu-id="4f29e-114">請使用此指令來取得較低的精確度，而不受限於除的嚴格需求。</span><span class="sxs-lookup"><span data-stu-id="4f29e-114">Use this instruction for reduced precision reciprocal, independent of the strict requirements for divide.</span></span>

<span data-ttu-id="4f29e-115">相對錯誤的最大值是2-21。</span><span class="sxs-lookup"><span data-stu-id="4f29e-115">Maximum relative error is 2-21.</span></span> <span data-ttu-id="4f29e-116"> (容錯功能只符合 rsq) </span><span class="sxs-lookup"><span data-stu-id="4f29e-116">(The error tolerance just matches rsq)</span></span>

<span data-ttu-id="4f29e-117">下表顯示使用各種不同的數位類別來執行指令時所取得的結果。</span><span class="sxs-lookup"><span data-stu-id="4f29e-117">The following table shows the results obtained when executing the instruction with various classes of numbers.</span></span>



|        |          |        |             |        |        |             |        |          |         |
|--------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| <span data-ttu-id="4f29e-118">*src*</span><span class="sxs-lookup"><span data-stu-id="4f29e-118">*src*</span></span>  | <span data-ttu-id="4f29e-119">**-inf**</span><span class="sxs-lookup"><span data-stu-id="4f29e-119">**-inf**</span></span> | <span data-ttu-id="4f29e-120">**-F**</span><span class="sxs-lookup"><span data-stu-id="4f29e-120">**-F**</span></span> | <span data-ttu-id="4f29e-121">**-denorm**</span><span class="sxs-lookup"><span data-stu-id="4f29e-121">**-denorm**</span></span> | <span data-ttu-id="4f29e-122">**-0**</span><span class="sxs-lookup"><span data-stu-id="4f29e-122">**-0**</span></span> | <span data-ttu-id="4f29e-123">**+0**</span><span class="sxs-lookup"><span data-stu-id="4f29e-123">**+0**</span></span> | <span data-ttu-id="4f29e-124">**+ denorm**</span><span class="sxs-lookup"><span data-stu-id="4f29e-124">**+denorm**</span></span> | <span data-ttu-id="4f29e-125">**+ F**</span><span class="sxs-lookup"><span data-stu-id="4f29e-125">**+F**</span></span> | <span data-ttu-id="4f29e-126">**+ inf**</span><span class="sxs-lookup"><span data-stu-id="4f29e-126">**+inf**</span></span> | <span data-ttu-id="4f29e-127">**NaN**</span><span class="sxs-lookup"><span data-stu-id="4f29e-127">**NaN**</span></span> |
| <span data-ttu-id="4f29e-128">*目標*</span><span class="sxs-lookup"><span data-stu-id="4f29e-128">*dest*</span></span> | <span data-ttu-id="4f29e-129">-0</span><span class="sxs-lookup"><span data-stu-id="4f29e-129">-0</span></span>       | <span data-ttu-id="4f29e-130">-F</span><span class="sxs-lookup"><span data-stu-id="4f29e-130">-F</span></span>     | <span data-ttu-id="4f29e-131">-inf</span><span class="sxs-lookup"><span data-stu-id="4f29e-131">-inf</span></span>        | <span data-ttu-id="4f29e-132">-inf</span><span class="sxs-lookup"><span data-stu-id="4f29e-132">-inf</span></span>   | <span data-ttu-id="4f29e-133">+inf</span><span class="sxs-lookup"><span data-stu-id="4f29e-133">+inf</span></span>   | <span data-ttu-id="4f29e-134">+inf</span><span class="sxs-lookup"><span data-stu-id="4f29e-134">+inf</span></span>        | <span data-ttu-id="4f29e-135">+F</span><span class="sxs-lookup"><span data-stu-id="4f29e-135">+F</span></span>     | <span data-ttu-id="4f29e-136">+0</span><span class="sxs-lookup"><span data-stu-id="4f29e-136">+0</span></span>       | <span data-ttu-id="4f29e-137">NaN</span><span class="sxs-lookup"><span data-stu-id="4f29e-137">NaN</span></span>     |



 

<span data-ttu-id="4f29e-138">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="4f29e-138">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="4f29e-139">頂點</span><span class="sxs-lookup"><span data-stu-id="4f29e-139">Vertex</span></span> | <span data-ttu-id="4f29e-140">船體</span><span class="sxs-lookup"><span data-stu-id="4f29e-140">Hull</span></span> | <span data-ttu-id="4f29e-141">網域</span><span class="sxs-lookup"><span data-stu-id="4f29e-141">Domain</span></span> | <span data-ttu-id="4f29e-142">幾何</span><span class="sxs-lookup"><span data-stu-id="4f29e-142">Geometry</span></span> | <span data-ttu-id="4f29e-143">像素</span><span class="sxs-lookup"><span data-stu-id="4f29e-143">Pixel</span></span> | <span data-ttu-id="4f29e-144">計算</span><span class="sxs-lookup"><span data-stu-id="4f29e-144">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="4f29e-145">X</span><span class="sxs-lookup"><span data-stu-id="4f29e-145">X</span></span>      | <span data-ttu-id="4f29e-146">X</span><span class="sxs-lookup"><span data-stu-id="4f29e-146">X</span></span>    | <span data-ttu-id="4f29e-147">X</span><span class="sxs-lookup"><span data-stu-id="4f29e-147">X</span></span>      | <span data-ttu-id="4f29e-148">X</span><span class="sxs-lookup"><span data-stu-id="4f29e-148">X</span></span>        | <span data-ttu-id="4f29e-149">X</span><span class="sxs-lookup"><span data-stu-id="4f29e-149">X</span></span>     | <span data-ttu-id="4f29e-150">X</span><span class="sxs-lookup"><span data-stu-id="4f29e-150">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="4f29e-151">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="4f29e-151">Minimum Shader Model</span></span>

<span data-ttu-id="4f29e-152">下列著色器模型支援此指令：</span><span class="sxs-lookup"><span data-stu-id="4f29e-152">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="4f29e-153">著色器模型</span><span class="sxs-lookup"><span data-stu-id="4f29e-153">Shader Model</span></span>                                              | <span data-ttu-id="4f29e-154">支援</span><span class="sxs-lookup"><span data-stu-id="4f29e-154">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="4f29e-155">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="4f29e-155">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="4f29e-156">是</span><span class="sxs-lookup"><span data-stu-id="4f29e-156">yes</span></span>       |
| [<span data-ttu-id="4f29e-157">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="4f29e-157">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="4f29e-158">不可以</span><span class="sxs-lookup"><span data-stu-id="4f29e-158">no</span></span>        |
| [<span data-ttu-id="4f29e-159">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="4f29e-159">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="4f29e-160">不可以</span><span class="sxs-lookup"><span data-stu-id="4f29e-160">no</span></span>        |
| [<span data-ttu-id="4f29e-161">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="4f29e-161">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="4f29e-162">不可以</span><span class="sxs-lookup"><span data-stu-id="4f29e-162">no</span></span>        |
| [<span data-ttu-id="4f29e-163">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="4f29e-163">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="4f29e-164">不可以</span><span class="sxs-lookup"><span data-stu-id="4f29e-164">no</span></span>        |
| [<span data-ttu-id="4f29e-165">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="4f29e-165">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="4f29e-166">不可以</span><span class="sxs-lookup"><span data-stu-id="4f29e-166">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="4f29e-167">相關主題</span><span class="sxs-lookup"><span data-stu-id="4f29e-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4f29e-168">著色器模型5元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="4f29e-168">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





