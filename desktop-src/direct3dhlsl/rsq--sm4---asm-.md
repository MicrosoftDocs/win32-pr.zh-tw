---
title: 'rsq (sm4-asm) '
description: 元件的交互平方根。
ms.assetid: CDA3C2DF-2793-4CE3-87CE-4E0AA945A1BB
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc274f927151938be055150d5b17287f9be0004d
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104022844"
---
# <a name="rsq-sm4---asm"></a><span data-ttu-id="0cda7-103">rsq (sm4-asm) </span><span class="sxs-lookup"><span data-stu-id="0cda7-103">rsq (sm4 - asm)</span></span>

<span data-ttu-id="0cda7-104">元件的交互平方根。</span><span class="sxs-lookup"><span data-stu-id="0cda7-104">Component-wise reciprocal square root.</span></span>



| <span data-ttu-id="0cda7-105">rsq \[ \_ sat \] dest \[ . mask \] ， \[ - \] src0 \[ \_ abs \] \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="0cda7-105">rsq\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|------------------------------------------------------------|



 



| <span data-ttu-id="0cda7-106">項目</span><span class="sxs-lookup"><span data-stu-id="0cda7-106">Item</span></span>                                                            | <span data-ttu-id="0cda7-107">描述</span><span class="sxs-lookup"><span data-stu-id="0cda7-107">Description</span></span>                                                                                      |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0cda7-108"><span id="dest"></span><span id="DEST"></span>*目標*</span><span class="sxs-lookup"><span data-stu-id="0cda7-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="0cda7-109">\[中的包含作業的 \] 結果。</span><span class="sxs-lookup"><span data-stu-id="0cda7-109">\[in\] Contains the results of the operation.</span></span><br/> <span data-ttu-id="0cda7-110">*dest* = 1.0 f/sqrt (*src0*) </span><span class="sxs-lookup"><span data-stu-id="0cda7-110">*dest* = 1.0f / sqrt(*src0*)</span></span><br/> |
| <span data-ttu-id="0cda7-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="0cda7-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="0cda7-112">\[在 \] 操作的元件中。</span><span class="sxs-lookup"><span data-stu-id="0cda7-112">\[in\] The components for the operation.</span></span><br/>                                              |



 

## <a name="remarks"></a><span data-ttu-id="0cda7-113">備註</span><span class="sxs-lookup"><span data-stu-id="0cda7-113">Remarks</span></span>

<span data-ttu-id="0cda7-114">相對錯誤的最大值是2-21。</span><span class="sxs-lookup"><span data-stu-id="0cda7-114">The maximum relative error is 2-21.</span></span>

<span data-ttu-id="0cda7-115">下表顯示使用各種不同的數位類別來執行指令時所取得的結果，前提是不會發生溢位或下溢。</span><span class="sxs-lookup"><span data-stu-id="0cda7-115">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span>

<span data-ttu-id="0cda7-116">F 表示有限實數。</span><span class="sxs-lookup"><span data-stu-id="0cda7-116">F means finite-real number.</span></span>



|          |          |        |             |        |        |             |        |          |         |
|----------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| <span data-ttu-id="0cda7-117">**src**</span><span class="sxs-lookup"><span data-stu-id="0cda7-117">**src**</span></span>  | <span data-ttu-id="0cda7-118">**-inf**</span><span class="sxs-lookup"><span data-stu-id="0cda7-118">**-inf**</span></span> | <span data-ttu-id="0cda7-119">**-F**</span><span class="sxs-lookup"><span data-stu-id="0cda7-119">**-F**</span></span> | <span data-ttu-id="0cda7-120">**-denorm**</span><span class="sxs-lookup"><span data-stu-id="0cda7-120">**-denorm**</span></span> | <span data-ttu-id="0cda7-121">**-0**</span><span class="sxs-lookup"><span data-stu-id="0cda7-121">**-0**</span></span> | <span data-ttu-id="0cda7-122">**+0**</span><span class="sxs-lookup"><span data-stu-id="0cda7-122">**+0**</span></span> | <span data-ttu-id="0cda7-123">**+ denorm**</span><span class="sxs-lookup"><span data-stu-id="0cda7-123">**+denorm**</span></span> | <span data-ttu-id="0cda7-124">**+ F**</span><span class="sxs-lookup"><span data-stu-id="0cda7-124">**+F**</span></span> | <span data-ttu-id="0cda7-125">**+ inf**</span><span class="sxs-lookup"><span data-stu-id="0cda7-125">**+inf**</span></span> | <span data-ttu-id="0cda7-126">**NaN**</span><span class="sxs-lookup"><span data-stu-id="0cda7-126">**NaN**</span></span> |
| <span data-ttu-id="0cda7-127">**目標**</span><span class="sxs-lookup"><span data-stu-id="0cda7-127">**dest**</span></span> | <span data-ttu-id="0cda7-128">NaN</span><span class="sxs-lookup"><span data-stu-id="0cda7-128">NaN</span></span>      | <span data-ttu-id="0cda7-129">NaN</span><span class="sxs-lookup"><span data-stu-id="0cda7-129">NaN</span></span>    | <span data-ttu-id="0cda7-130">-inf</span><span class="sxs-lookup"><span data-stu-id="0cda7-130">-inf</span></span>        | <span data-ttu-id="0cda7-131">-inf</span><span class="sxs-lookup"><span data-stu-id="0cda7-131">-inf</span></span>   | <span data-ttu-id="0cda7-132">+inf</span><span class="sxs-lookup"><span data-stu-id="0cda7-132">+inf</span></span>   | <span data-ttu-id="0cda7-133">+inf</span><span class="sxs-lookup"><span data-stu-id="0cda7-133">+inf</span></span>        | <span data-ttu-id="0cda7-134">+F</span><span class="sxs-lookup"><span data-stu-id="0cda7-134">+F</span></span>     | <span data-ttu-id="0cda7-135">+0</span><span class="sxs-lookup"><span data-stu-id="0cda7-135">+0</span></span>       | <span data-ttu-id="0cda7-136">NaN</span><span class="sxs-lookup"><span data-stu-id="0cda7-136">NaN</span></span>     |



 

<span data-ttu-id="0cda7-137">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="0cda7-137">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="0cda7-138">頂點著色器</span><span class="sxs-lookup"><span data-stu-id="0cda7-138">Vertex Shader</span></span> | <span data-ttu-id="0cda7-139">幾何著色器</span><span class="sxs-lookup"><span data-stu-id="0cda7-139">Geometry Shader</span></span> | <span data-ttu-id="0cda7-140">像素著色器</span><span class="sxs-lookup"><span data-stu-id="0cda7-140">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="0cda7-141">x</span><span class="sxs-lookup"><span data-stu-id="0cda7-141">x</span></span>             | <span data-ttu-id="0cda7-142">x</span><span class="sxs-lookup"><span data-stu-id="0cda7-142">x</span></span>               | <span data-ttu-id="0cda7-143">x</span><span class="sxs-lookup"><span data-stu-id="0cda7-143">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="0cda7-144">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="0cda7-144">Minimum Shader Model</span></span>

<span data-ttu-id="0cda7-145">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="0cda7-145">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="0cda7-146">著色器模型</span><span class="sxs-lookup"><span data-stu-id="0cda7-146">Shader Model</span></span>                                              | <span data-ttu-id="0cda7-147">支援</span><span class="sxs-lookup"><span data-stu-id="0cda7-147">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="0cda7-148">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="0cda7-148">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="0cda7-149">是</span><span class="sxs-lookup"><span data-stu-id="0cda7-149">yes</span></span>       |
| [<span data-ttu-id="0cda7-150">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="0cda7-150">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="0cda7-151">是</span><span class="sxs-lookup"><span data-stu-id="0cda7-151">yes</span></span>       |
| [<span data-ttu-id="0cda7-152">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="0cda7-152">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="0cda7-153">是</span><span class="sxs-lookup"><span data-stu-id="0cda7-153">yes</span></span>       |
| [<span data-ttu-id="0cda7-154">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="0cda7-154">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="0cda7-155">不可以</span><span class="sxs-lookup"><span data-stu-id="0cda7-155">no</span></span>        |
| [<span data-ttu-id="0cda7-156">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="0cda7-156">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="0cda7-157">不可以</span><span class="sxs-lookup"><span data-stu-id="0cda7-157">no</span></span>        |
| [<span data-ttu-id="0cda7-158">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="0cda7-158">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="0cda7-159">不可以</span><span class="sxs-lookup"><span data-stu-id="0cda7-159">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="0cda7-160">相關主題</span><span class="sxs-lookup"><span data-stu-id="0cda7-160">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0cda7-161">著色器模型4元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="0cda7-161">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





