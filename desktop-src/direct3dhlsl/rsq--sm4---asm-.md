---
title: 'rsq (sm4-asm) '
description: 元件的交互平方根。
ms.assetid: CDA3C2DF-2793-4CE3-87CE-4E0AA945A1BB
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1528e9f187ff7d4fb6074d42a1c574686f3b22f
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998165"
---
# <a name="rsq-sm4---asm"></a><span data-ttu-id="907ac-103">rsq (sm4-asm) </span><span class="sxs-lookup"><span data-stu-id="907ac-103">rsq (sm4 - asm)</span></span>

<span data-ttu-id="907ac-104">元件的交互平方根。</span><span class="sxs-lookup"><span data-stu-id="907ac-104">Component-wise reciprocal square root.</span></span>



| <span data-ttu-id="907ac-105">rsq \[ \_ sat \] dest \[ . mask \] ， \[ - \] src0 \[ \_ abs \] \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="907ac-105">rsq\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|------------------------------------------------------------|



 



| <span data-ttu-id="907ac-106">項目</span><span class="sxs-lookup"><span data-stu-id="907ac-106">Item</span></span>                                                            | <span data-ttu-id="907ac-107">描述</span><span class="sxs-lookup"><span data-stu-id="907ac-107">Description</span></span>                                                                                      |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="907ac-108"><span id="dest"></span><span id="DEST"></span>*目標*</span><span class="sxs-lookup"><span data-stu-id="907ac-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="907ac-109">\[中的包含作業的 \] 結果。</span><span class="sxs-lookup"><span data-stu-id="907ac-109">\[in\] Contains the results of the operation.</span></span><br/> <span data-ttu-id="907ac-110">*dest* = 1.0 f/sqrt (*src0*) </span><span class="sxs-lookup"><span data-stu-id="907ac-110">*dest* = 1.0f / sqrt(*src0*)</span></span><br/> |
| <span data-ttu-id="907ac-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="907ac-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="907ac-112">\[在 \] 操作的元件中。</span><span class="sxs-lookup"><span data-stu-id="907ac-112">\[in\] The components for the operation.</span></span><br/>                                              |



 

## <a name="remarks"></a><span data-ttu-id="907ac-113">備註</span><span class="sxs-lookup"><span data-stu-id="907ac-113">Remarks</span></span>

<span data-ttu-id="907ac-114">相對錯誤的最大值是2-21。</span><span class="sxs-lookup"><span data-stu-id="907ac-114">The maximum relative error is 2-21.</span></span>

<span data-ttu-id="907ac-115">下表顯示使用各種不同的數位類別來執行指令時所取得的結果，前提是不會發生溢位或下溢。</span><span class="sxs-lookup"><span data-stu-id="907ac-115">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span>

<span data-ttu-id="907ac-116">F 表示有限實數。</span><span class="sxs-lookup"><span data-stu-id="907ac-116">F means finite-real number.</span></span>



| <span data-ttu-id="907ac-117">**src**</span><span class="sxs-lookup"><span data-stu-id="907ac-117">**src**</span></span>  | <span data-ttu-id="907ac-118">**-inf**</span><span class="sxs-lookup"><span data-stu-id="907ac-118">**-inf**</span></span> | <span data-ttu-id="907ac-119">**-F**</span><span class="sxs-lookup"><span data-stu-id="907ac-119">**-F**</span></span> | <span data-ttu-id="907ac-120">**-denorm**</span><span class="sxs-lookup"><span data-stu-id="907ac-120">**-denorm**</span></span> | <span data-ttu-id="907ac-121">**-0**</span><span class="sxs-lookup"><span data-stu-id="907ac-121">**-0**</span></span> | <span data-ttu-id="907ac-122">**+0**</span><span class="sxs-lookup"><span data-stu-id="907ac-122">**+0**</span></span> | <span data-ttu-id="907ac-123">**+ denorm**</span><span class="sxs-lookup"><span data-stu-id="907ac-123">**+denorm**</span></span> | <span data-ttu-id="907ac-124">**+ F**</span><span class="sxs-lookup"><span data-stu-id="907ac-124">**+F**</span></span> | <span data-ttu-id="907ac-125">**+ inf**</span><span class="sxs-lookup"><span data-stu-id="907ac-125">**+inf**</span></span> | <span data-ttu-id="907ac-126">**NaN**</span><span class="sxs-lookup"><span data-stu-id="907ac-126">**NaN**</span></span> |
|----------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| <span data-ttu-id="907ac-127">**目標**</span><span class="sxs-lookup"><span data-stu-id="907ac-127">**dest**</span></span> | <span data-ttu-id="907ac-128">NaN</span><span class="sxs-lookup"><span data-stu-id="907ac-128">NaN</span></span>      | <span data-ttu-id="907ac-129">NaN</span><span class="sxs-lookup"><span data-stu-id="907ac-129">NaN</span></span>    | <span data-ttu-id="907ac-130">-inf</span><span class="sxs-lookup"><span data-stu-id="907ac-130">-inf</span></span>        | <span data-ttu-id="907ac-131">-inf</span><span class="sxs-lookup"><span data-stu-id="907ac-131">-inf</span></span>   | <span data-ttu-id="907ac-132">+inf</span><span class="sxs-lookup"><span data-stu-id="907ac-132">+inf</span></span>   | <span data-ttu-id="907ac-133">+inf</span><span class="sxs-lookup"><span data-stu-id="907ac-133">+inf</span></span>        | <span data-ttu-id="907ac-134">+F</span><span class="sxs-lookup"><span data-stu-id="907ac-134">+F</span></span>     | <span data-ttu-id="907ac-135">+0</span><span class="sxs-lookup"><span data-stu-id="907ac-135">+0</span></span>       | <span data-ttu-id="907ac-136">NaN</span><span class="sxs-lookup"><span data-stu-id="907ac-136">NaN</span></span>     |



 

<span data-ttu-id="907ac-137">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="907ac-137">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="907ac-138">頂點著色器</span><span class="sxs-lookup"><span data-stu-id="907ac-138">Vertex Shader</span></span> | <span data-ttu-id="907ac-139">幾何著色器</span><span class="sxs-lookup"><span data-stu-id="907ac-139">Geometry Shader</span></span> | <span data-ttu-id="907ac-140">像素著色器</span><span class="sxs-lookup"><span data-stu-id="907ac-140">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="907ac-141">x</span><span class="sxs-lookup"><span data-stu-id="907ac-141">x</span></span>             | <span data-ttu-id="907ac-142">x</span><span class="sxs-lookup"><span data-stu-id="907ac-142">x</span></span>               | <span data-ttu-id="907ac-143">x</span><span class="sxs-lookup"><span data-stu-id="907ac-143">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="907ac-144">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="907ac-144">Minimum Shader Model</span></span>

<span data-ttu-id="907ac-145">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="907ac-145">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="907ac-146">著色器模型</span><span class="sxs-lookup"><span data-stu-id="907ac-146">Shader Model</span></span>                                              | <span data-ttu-id="907ac-147">支援</span><span class="sxs-lookup"><span data-stu-id="907ac-147">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="907ac-148">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="907ac-148">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="907ac-149">是</span><span class="sxs-lookup"><span data-stu-id="907ac-149">yes</span></span>       |
| [<span data-ttu-id="907ac-150">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="907ac-150">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="907ac-151">是</span><span class="sxs-lookup"><span data-stu-id="907ac-151">yes</span></span>       |
| [<span data-ttu-id="907ac-152">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="907ac-152">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="907ac-153">是</span><span class="sxs-lookup"><span data-stu-id="907ac-153">yes</span></span>       |
| [<span data-ttu-id="907ac-154">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="907ac-154">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="907ac-155">否</span><span class="sxs-lookup"><span data-stu-id="907ac-155">no</span></span>        |
| [<span data-ttu-id="907ac-156">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="907ac-156">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="907ac-157">否</span><span class="sxs-lookup"><span data-stu-id="907ac-157">no</span></span>        |
| [<span data-ttu-id="907ac-158">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="907ac-158">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="907ac-159">否</span><span class="sxs-lookup"><span data-stu-id="907ac-159">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="907ac-160">相關主題</span><span class="sxs-lookup"><span data-stu-id="907ac-160">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="907ac-161">著色器模型4元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="907ac-161">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





