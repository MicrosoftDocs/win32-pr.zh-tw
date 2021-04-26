---
title: '記錄 (sm4-asm) '
description: 以元件為基礎的記錄基底2。
ms.assetid: 6D28864A-C2BA-44AF-9E78-7C2B34F5E462
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88e4b89b4dcc085cf4fd4fda762d96fb71271af2
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998315"
---
# <a name="log-sm4---asm"></a><span data-ttu-id="6bfbc-103">記錄 (sm4-asm) </span><span class="sxs-lookup"><span data-stu-id="6bfbc-103">log (sm4 - asm)</span></span>

<span data-ttu-id="6bfbc-104">以元件為基礎的記錄基底2。</span><span class="sxs-lookup"><span data-stu-id="6bfbc-104">Component-wise log base 2.</span></span>



| <span data-ttu-id="6bfbc-105">記錄 \[ \_ sat \] dest \[ . mask \] ， \[ - \] src0 \[ \_ abs \] \[ . swizzle</span><span class="sxs-lookup"><span data-stu-id="6bfbc-105">log\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle</span></span> |
|----------------------------------------------------------|



 



| <span data-ttu-id="6bfbc-106">項目</span><span class="sxs-lookup"><span data-stu-id="6bfbc-106">Item</span></span>                                                            | <span data-ttu-id="6bfbc-107">描述</span><span class="sxs-lookup"><span data-stu-id="6bfbc-107">Description</span></span>                                                                                |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="6bfbc-108"><span id="dest"></span><span id="DEST"></span>*目標*</span><span class="sxs-lookup"><span data-stu-id="6bfbc-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="6bfbc-109">\[在 \] 操作結果的位址中。</span><span class="sxs-lookup"><span data-stu-id="6bfbc-109">\[in\] The address of the result of the operation.</span></span><br/> <span data-ttu-id="6bfbc-110">dest = log2 (src0) </span><span class="sxs-lookup"><span data-stu-id="6bfbc-110">dest = log2(src0)</span></span><br/> |
| <span data-ttu-id="6bfbc-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="6bfbc-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="6bfbc-112">\[在作業 \] 的值中。</span><span class="sxs-lookup"><span data-stu-id="6bfbc-112">\[in\] The value for the operation.</span></span><br/>                                             |



 

## <a name="remarks"></a><span data-ttu-id="6bfbc-113">備註</span><span class="sxs-lookup"><span data-stu-id="6bfbc-113">Remarks</span></span>

### <a name="restrictions"></a><span data-ttu-id="6bfbc-114">限制</span><span class="sxs-lookup"><span data-stu-id="6bfbc-114">Restrictions</span></span>

-   <span data-ttu-id="6bfbc-115">遵循限制理論。</span><span class="sxs-lookup"><span data-stu-id="6bfbc-115">Follows limit theory.</span></span>
-   <span data-ttu-id="6bfbc-116">容錯：如果 *src0* 為 \[ 0.5，則 \] absolue 錯誤必須不超過2-21。</span><span class="sxs-lookup"><span data-stu-id="6bfbc-116">Error tolerance: If *src0* is \[0.5..2\], absolue error must be no more than 2-21.</span></span> <span data-ttu-id="6bfbc-117">如果 *src0* 是 (0. 0.5) 或 (2. + INF，則 \] 相對錯誤不能超過2-21。</span><span class="sxs-lookup"><span data-stu-id="6bfbc-117">If *src0* is (0..0.5) or (2..+INF\], relative error must be no more than 2-21.</span></span>

<span data-ttu-id="6bfbc-118">下表顯示使用各種不同的數位類別來執行指令時所取得的結果，前提是不會發生溢位或下溢。</span><span class="sxs-lookup"><span data-stu-id="6bfbc-118">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span> <span data-ttu-id="6bfbc-119">F 表示有限實數。</span><span class="sxs-lookup"><span data-stu-id="6bfbc-119">F means finite-real number.</span></span>



| <span data-ttu-id="6bfbc-120">**src**</span><span class="sxs-lookup"><span data-stu-id="6bfbc-120">**src**</span></span>  | <span data-ttu-id="6bfbc-121">**-inf**</span><span class="sxs-lookup"><span data-stu-id="6bfbc-121">**-inf**</span></span> | <span data-ttu-id="6bfbc-122">**-F**</span><span class="sxs-lookup"><span data-stu-id="6bfbc-122">**-F**</span></span> | <span data-ttu-id="6bfbc-123">**-denorm**</span><span class="sxs-lookup"><span data-stu-id="6bfbc-123">**-denorm**</span></span> | <span data-ttu-id="6bfbc-124">**-0**</span><span class="sxs-lookup"><span data-stu-id="6bfbc-124">**-0**</span></span> | <span data-ttu-id="6bfbc-125">**+0**</span><span class="sxs-lookup"><span data-stu-id="6bfbc-125">**+0**</span></span> | <span data-ttu-id="6bfbc-126">**+ denorm**</span><span class="sxs-lookup"><span data-stu-id="6bfbc-126">**+denorm**</span></span> | <span data-ttu-id="6bfbc-127">**+ F**</span><span class="sxs-lookup"><span data-stu-id="6bfbc-127">**+F**</span></span> | <span data-ttu-id="6bfbc-128">**+ inf**</span><span class="sxs-lookup"><span data-stu-id="6bfbc-128">**+inf**</span></span> | <span data-ttu-id="6bfbc-129">**NaN**</span><span class="sxs-lookup"><span data-stu-id="6bfbc-129">**NaN**</span></span> |
|----------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| <span data-ttu-id="6bfbc-130">**目標**</span><span class="sxs-lookup"><span data-stu-id="6bfbc-130">**dest**</span></span> | <span data-ttu-id="6bfbc-131">NaN</span><span class="sxs-lookup"><span data-stu-id="6bfbc-131">NaN</span></span>      | <span data-ttu-id="6bfbc-132">NaN</span><span class="sxs-lookup"><span data-stu-id="6bfbc-132">NaN</span></span>    | <span data-ttu-id="6bfbc-133">-inf</span><span class="sxs-lookup"><span data-stu-id="6bfbc-133">-inf</span></span>        | <span data-ttu-id="6bfbc-134">-inf</span><span class="sxs-lookup"><span data-stu-id="6bfbc-134">-inf</span></span>   | <span data-ttu-id="6bfbc-135">-inf</span><span class="sxs-lookup"><span data-stu-id="6bfbc-135">-inf</span></span>   | <span data-ttu-id="6bfbc-136">-inf</span><span class="sxs-lookup"><span data-stu-id="6bfbc-136">-inf</span></span>        | <span data-ttu-id="6bfbc-137">F</span><span class="sxs-lookup"><span data-stu-id="6bfbc-137">F</span></span>      | <span data-ttu-id="6bfbc-138">+inf</span><span class="sxs-lookup"><span data-stu-id="6bfbc-138">+inf</span></span>     | <span data-ttu-id="6bfbc-139">NaN</span><span class="sxs-lookup"><span data-stu-id="6bfbc-139">NaN</span></span>     |



 

<span data-ttu-id="6bfbc-140">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="6bfbc-140">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="6bfbc-141">頂點著色器</span><span class="sxs-lookup"><span data-stu-id="6bfbc-141">Vertex Shader</span></span> | <span data-ttu-id="6bfbc-142">幾何著色器</span><span class="sxs-lookup"><span data-stu-id="6bfbc-142">Geometry Shader</span></span> | <span data-ttu-id="6bfbc-143">像素著色器</span><span class="sxs-lookup"><span data-stu-id="6bfbc-143">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="6bfbc-144">x</span><span class="sxs-lookup"><span data-stu-id="6bfbc-144">x</span></span>             | <span data-ttu-id="6bfbc-145">x</span><span class="sxs-lookup"><span data-stu-id="6bfbc-145">x</span></span>               | <span data-ttu-id="6bfbc-146">x</span><span class="sxs-lookup"><span data-stu-id="6bfbc-146">x</span></span>            |



 

### <a name="minimum-shader-model"></a><span data-ttu-id="6bfbc-147">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="6bfbc-147">Minimum Shader Model</span></span>

<span data-ttu-id="6bfbc-148">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="6bfbc-148">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="6bfbc-149">著色器模型</span><span class="sxs-lookup"><span data-stu-id="6bfbc-149">Shader Model</span></span>                                              | <span data-ttu-id="6bfbc-150">支援</span><span class="sxs-lookup"><span data-stu-id="6bfbc-150">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="6bfbc-151">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="6bfbc-151">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="6bfbc-152">是</span><span class="sxs-lookup"><span data-stu-id="6bfbc-152">yes</span></span>       |
| [<span data-ttu-id="6bfbc-153">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="6bfbc-153">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="6bfbc-154">是</span><span class="sxs-lookup"><span data-stu-id="6bfbc-154">yes</span></span>       |
| [<span data-ttu-id="6bfbc-155">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="6bfbc-155">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="6bfbc-156">是</span><span class="sxs-lookup"><span data-stu-id="6bfbc-156">yes</span></span>       |
| [<span data-ttu-id="6bfbc-157">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="6bfbc-157">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="6bfbc-158">否</span><span class="sxs-lookup"><span data-stu-id="6bfbc-158">no</span></span>        |
| [<span data-ttu-id="6bfbc-159">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="6bfbc-159">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="6bfbc-160">否</span><span class="sxs-lookup"><span data-stu-id="6bfbc-160">no</span></span>        |
| [<span data-ttu-id="6bfbc-161">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="6bfbc-161">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="6bfbc-162">否</span><span class="sxs-lookup"><span data-stu-id="6bfbc-162">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="6bfbc-163">相關主題</span><span class="sxs-lookup"><span data-stu-id="6bfbc-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6bfbc-164">著色器模型4元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="6bfbc-164">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





