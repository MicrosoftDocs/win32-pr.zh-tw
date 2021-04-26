---
title: 'rcp (sm5-asm) '
description: 元件的相互比較。
ms.assetid: 499A14D6-36DB-4860-94D1-887D931E60D4
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa37499a981bae86333b071c2e96a37ccb8ac1a6
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998245"
---
# <a name="rcp-sm5---asm"></a><span data-ttu-id="fdfe4-103">rcp (sm5-asm) </span><span class="sxs-lookup"><span data-stu-id="fdfe4-103">rcp (sm5 - asm)</span></span>

<span data-ttu-id="fdfe4-104">元件的相互比較。</span><span class="sxs-lookup"><span data-stu-id="fdfe4-104">Component-wise reciprocal.</span></span>



| <span data-ttu-id="fdfe4-105">rcp \[ \_ sat \] dest \[ \] 、 \[ - \] src0 \[ \_ abs \] \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="fdfe4-105">rcp\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|------------------------------------------------------------|



 



| <span data-ttu-id="fdfe4-106">項目</span><span class="sxs-lookup"><span data-stu-id="fdfe4-106">Item</span></span>                                                            | <span data-ttu-id="fdfe4-107">描述</span><span class="sxs-lookup"><span data-stu-id="fdfe4-107">Description</span></span>                                                                         |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="fdfe4-108"><span id="dest"></span><span id="DEST"></span>*目標*</span><span class="sxs-lookup"><span data-stu-id="fdfe4-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="fdfe4-109">\[在 \] 結果的位址中</span><span class="sxs-lookup"><span data-stu-id="fdfe4-109">\[in\] The address of the results</span></span><br/> <span data-ttu-id="fdfe4-110">*目的地*  = **1.0 f**  / *src0*。</span><span class="sxs-lookup"><span data-stu-id="fdfe4-110">*dest* = **1.0f** / *src0*.</span></span><br/> |
| <span data-ttu-id="fdfe4-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="fdfe4-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="fdfe4-112">\[\]要採用的數位。</span><span class="sxs-lookup"><span data-stu-id="fdfe4-112">\[in\] The number to take the reciprocal of.</span></span><br/>                             |



 

## <a name="remarks"></a><span data-ttu-id="fdfe4-113">備註</span><span class="sxs-lookup"><span data-stu-id="fdfe4-113">Remarks</span></span>

<span data-ttu-id="fdfe4-114">請使用此指令來取得較低的精確度，而不受限於除的嚴格需求。</span><span class="sxs-lookup"><span data-stu-id="fdfe4-114">Use this instruction for reduced precision reciprocal, independent of the strict requirements for divide.</span></span>

<span data-ttu-id="fdfe4-115">相對錯誤的最大值是2-21。</span><span class="sxs-lookup"><span data-stu-id="fdfe4-115">Maximum relative error is 2-21.</span></span> <span data-ttu-id="fdfe4-116"> (容錯功能只符合 rsq) </span><span class="sxs-lookup"><span data-stu-id="fdfe4-116">(The error tolerance just matches rsq)</span></span>

<span data-ttu-id="fdfe4-117">下表顯示使用各種不同的數位類別來執行指令時所取得的結果。</span><span class="sxs-lookup"><span data-stu-id="fdfe4-117">The following table shows the results obtained when executing the instruction with various classes of numbers.</span></span>



| <span data-ttu-id="fdfe4-118">*src*</span><span class="sxs-lookup"><span data-stu-id="fdfe4-118">*src*</span></span>  | <span data-ttu-id="fdfe4-119">**-inf**</span><span class="sxs-lookup"><span data-stu-id="fdfe4-119">**-inf**</span></span> | <span data-ttu-id="fdfe4-120">**-F**</span><span class="sxs-lookup"><span data-stu-id="fdfe4-120">**-F**</span></span> | <span data-ttu-id="fdfe4-121">**-denorm**</span><span class="sxs-lookup"><span data-stu-id="fdfe4-121">**-denorm**</span></span> | <span data-ttu-id="fdfe4-122">**-0**</span><span class="sxs-lookup"><span data-stu-id="fdfe4-122">**-0**</span></span> | <span data-ttu-id="fdfe4-123">**+0**</span><span class="sxs-lookup"><span data-stu-id="fdfe4-123">**+0**</span></span> | <span data-ttu-id="fdfe4-124">**+ denorm**</span><span class="sxs-lookup"><span data-stu-id="fdfe4-124">**+denorm**</span></span> | <span data-ttu-id="fdfe4-125">**+ F**</span><span class="sxs-lookup"><span data-stu-id="fdfe4-125">**+F**</span></span> | <span data-ttu-id="fdfe4-126">**+ inf**</span><span class="sxs-lookup"><span data-stu-id="fdfe4-126">**+inf**</span></span> | <span data-ttu-id="fdfe4-127">**NaN**</span><span class="sxs-lookup"><span data-stu-id="fdfe4-127">**NaN**</span></span> |
|--------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| <span data-ttu-id="fdfe4-128">*目標*</span><span class="sxs-lookup"><span data-stu-id="fdfe4-128">*dest*</span></span> | <span data-ttu-id="fdfe4-129">-0</span><span class="sxs-lookup"><span data-stu-id="fdfe4-129">-0</span></span>       | <span data-ttu-id="fdfe4-130">-F</span><span class="sxs-lookup"><span data-stu-id="fdfe4-130">-F</span></span>     | <span data-ttu-id="fdfe4-131">-inf</span><span class="sxs-lookup"><span data-stu-id="fdfe4-131">-inf</span></span>        | <span data-ttu-id="fdfe4-132">-inf</span><span class="sxs-lookup"><span data-stu-id="fdfe4-132">-inf</span></span>   | <span data-ttu-id="fdfe4-133">+inf</span><span class="sxs-lookup"><span data-stu-id="fdfe4-133">+inf</span></span>   | <span data-ttu-id="fdfe4-134">+inf</span><span class="sxs-lookup"><span data-stu-id="fdfe4-134">+inf</span></span>        | <span data-ttu-id="fdfe4-135">+F</span><span class="sxs-lookup"><span data-stu-id="fdfe4-135">+F</span></span>     | <span data-ttu-id="fdfe4-136">+0</span><span class="sxs-lookup"><span data-stu-id="fdfe4-136">+0</span></span>       | <span data-ttu-id="fdfe4-137">NaN</span><span class="sxs-lookup"><span data-stu-id="fdfe4-137">NaN</span></span>     |



 

<span data-ttu-id="fdfe4-138">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="fdfe4-138">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="fdfe4-139">頂點</span><span class="sxs-lookup"><span data-stu-id="fdfe4-139">Vertex</span></span> | <span data-ttu-id="fdfe4-140">船體</span><span class="sxs-lookup"><span data-stu-id="fdfe4-140">Hull</span></span> | <span data-ttu-id="fdfe4-141">網域</span><span class="sxs-lookup"><span data-stu-id="fdfe4-141">Domain</span></span> | <span data-ttu-id="fdfe4-142">幾何</span><span class="sxs-lookup"><span data-stu-id="fdfe4-142">Geometry</span></span> | <span data-ttu-id="fdfe4-143">像素</span><span class="sxs-lookup"><span data-stu-id="fdfe4-143">Pixel</span></span> | <span data-ttu-id="fdfe4-144">計算</span><span class="sxs-lookup"><span data-stu-id="fdfe4-144">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="fdfe4-145">X</span><span class="sxs-lookup"><span data-stu-id="fdfe4-145">X</span></span>      | <span data-ttu-id="fdfe4-146">X</span><span class="sxs-lookup"><span data-stu-id="fdfe4-146">X</span></span>    | <span data-ttu-id="fdfe4-147">X</span><span class="sxs-lookup"><span data-stu-id="fdfe4-147">X</span></span>      | <span data-ttu-id="fdfe4-148">X</span><span class="sxs-lookup"><span data-stu-id="fdfe4-148">X</span></span>        | <span data-ttu-id="fdfe4-149">X</span><span class="sxs-lookup"><span data-stu-id="fdfe4-149">X</span></span>     | <span data-ttu-id="fdfe4-150">X</span><span class="sxs-lookup"><span data-stu-id="fdfe4-150">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="fdfe4-151">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="fdfe4-151">Minimum Shader Model</span></span>

<span data-ttu-id="fdfe4-152">下列著色器模型支援此指令：</span><span class="sxs-lookup"><span data-stu-id="fdfe4-152">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="fdfe4-153">著色器模型</span><span class="sxs-lookup"><span data-stu-id="fdfe4-153">Shader Model</span></span>                                              | <span data-ttu-id="fdfe4-154">支援</span><span class="sxs-lookup"><span data-stu-id="fdfe4-154">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="fdfe4-155">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="fdfe4-155">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="fdfe4-156">是</span><span class="sxs-lookup"><span data-stu-id="fdfe4-156">yes</span></span>       |
| [<span data-ttu-id="fdfe4-157">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="fdfe4-157">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="fdfe4-158">否</span><span class="sxs-lookup"><span data-stu-id="fdfe4-158">no</span></span>        |
| [<span data-ttu-id="fdfe4-159">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="fdfe4-159">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="fdfe4-160">否</span><span class="sxs-lookup"><span data-stu-id="fdfe4-160">no</span></span>        |
| [<span data-ttu-id="fdfe4-161">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="fdfe4-161">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="fdfe4-162">否</span><span class="sxs-lookup"><span data-stu-id="fdfe4-162">no</span></span>        |
| [<span data-ttu-id="fdfe4-163">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="fdfe4-163">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="fdfe4-164">否</span><span class="sxs-lookup"><span data-stu-id="fdfe4-164">no</span></span>        |
| [<span data-ttu-id="fdfe4-165">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="fdfe4-165">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="fdfe4-166">否</span><span class="sxs-lookup"><span data-stu-id="fdfe4-166">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="fdfe4-167">相關主題</span><span class="sxs-lookup"><span data-stu-id="fdfe4-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fdfe4-168">著色器模型5元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="fdfe4-168">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





