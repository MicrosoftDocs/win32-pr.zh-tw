---
title: 'exp (sm4-asm) '
description: 元件取向2exponent。
ms.assetid: 12EB865A-BF71-4B4B-854F-9DA056B18AE0
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b24c74394a5e8ac7a6c945e2c9b63e6f242daa1
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107999075"
---
# <a name="exp-sm4---asm"></a><span data-ttu-id="d6ecc-103">exp (sm4-asm) </span><span class="sxs-lookup"><span data-stu-id="d6ecc-103">exp (sm4 - asm)</span></span>

<span data-ttu-id="d6ecc-104">元件取向2exponent。</span><span class="sxs-lookup"><span data-stu-id="d6ecc-104">Component-wise 2exponent.</span></span>



| <span data-ttu-id="d6ecc-105">exp \[ \_ sat \] dest \[ . mask \] ， \[ - \] src0 \[ \_ abs \] \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="d6ecc-105">exp\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|------------------------------------------------------------|



 



| <span data-ttu-id="d6ecc-106">項目</span><span class="sxs-lookup"><span data-stu-id="d6ecc-106">Item</span></span>                                                            | <span data-ttu-id="d6ecc-107">描述</span><span class="sxs-lookup"><span data-stu-id="d6ecc-107">Description</span></span>                                                                |
|-----------------------------------------------------------------|----------------------------------------------------------------------------|
| <span data-ttu-id="d6ecc-108"><span id="dest"></span><span id="DEST"></span>*目標*</span><span class="sxs-lookup"><span data-stu-id="d6ecc-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="d6ecc-109">\[在作業的 \] 結果中。</span><span class="sxs-lookup"><span data-stu-id="d6ecc-109">\[in\] The result of the operation.</span></span><br/> <span data-ttu-id="d6ecc-110">*dest* = 2 *src0*</span><span class="sxs-lookup"><span data-stu-id="d6ecc-110">*dest* = 2 *src0*</span></span><br/> |
| <span data-ttu-id="d6ecc-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="d6ecc-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="d6ecc-112">\[在 \] 指數中。</span><span class="sxs-lookup"><span data-stu-id="d6ecc-112">\[in\] The exponent.</span></span><br/>                                            |



 

## <a name="remarks"></a><span data-ttu-id="d6ecc-113">備註</span><span class="sxs-lookup"><span data-stu-id="d6ecc-113">Remarks</span></span>

<span data-ttu-id="d6ecc-114">此指示遵循限制理論。</span><span class="sxs-lookup"><span data-stu-id="d6ecc-114">This instruction follows limit theory.</span></span> <span data-ttu-id="d6ecc-115">相對錯誤的最大值是2-21。</span><span class="sxs-lookup"><span data-stu-id="d6ecc-115">The maximum relative error is 2-21.</span></span>

<span data-ttu-id="d6ecc-116">下表顯示使用各種不同的數位類別來執行指令時所取得的結果，前提是不會發生溢位或下溢。</span><span class="sxs-lookup"><span data-stu-id="d6ecc-116">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span> <span data-ttu-id="d6ecc-117">在此表中，F 表示有限的實數。</span><span class="sxs-lookup"><span data-stu-id="d6ecc-117">In this table F means finite-real number.</span></span>



| <span data-ttu-id="d6ecc-118">**src**</span><span class="sxs-lookup"><span data-stu-id="d6ecc-118">**src**</span></span>  | <span data-ttu-id="d6ecc-119">**-inf**</span><span class="sxs-lookup"><span data-stu-id="d6ecc-119">**-inf**</span></span> | <span data-ttu-id="d6ecc-120">**-F**</span><span class="sxs-lookup"><span data-stu-id="d6ecc-120">**-F**</span></span> | <span data-ttu-id="d6ecc-121">**-denorm**</span><span class="sxs-lookup"><span data-stu-id="d6ecc-121">**-denorm**</span></span> | <span data-ttu-id="d6ecc-122">**-0**</span><span class="sxs-lookup"><span data-stu-id="d6ecc-122">**-0**</span></span> | <span data-ttu-id="d6ecc-123">**+0**</span><span class="sxs-lookup"><span data-stu-id="d6ecc-123">**+0**</span></span> | <span data-ttu-id="d6ecc-124">**+ denorm**</span><span class="sxs-lookup"><span data-stu-id="d6ecc-124">**+denorm**</span></span> | <span data-ttu-id="d6ecc-125">**+ F**</span><span class="sxs-lookup"><span data-stu-id="d6ecc-125">**+F**</span></span> | <span data-ttu-id="d6ecc-126">**+ inf**</span><span class="sxs-lookup"><span data-stu-id="d6ecc-126">**+inf**</span></span> | <span data-ttu-id="d6ecc-127">**NaN**</span><span class="sxs-lookup"><span data-stu-id="d6ecc-127">**NaN**</span></span> |
|----------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| <span data-ttu-id="d6ecc-128">**目標**</span><span class="sxs-lookup"><span data-stu-id="d6ecc-128">**dest**</span></span> | <span data-ttu-id="d6ecc-129">0</span><span class="sxs-lookup"><span data-stu-id="d6ecc-129">0</span></span>        | <span data-ttu-id="d6ecc-130">+F</span><span class="sxs-lookup"><span data-stu-id="d6ecc-130">+F</span></span>     | <span data-ttu-id="d6ecc-131">1</span><span class="sxs-lookup"><span data-stu-id="d6ecc-131">1</span></span>           | <span data-ttu-id="d6ecc-132">1</span><span class="sxs-lookup"><span data-stu-id="d6ecc-132">1</span></span>      | <span data-ttu-id="d6ecc-133">1</span><span class="sxs-lookup"><span data-stu-id="d6ecc-133">1</span></span>      | <span data-ttu-id="d6ecc-134">1</span><span class="sxs-lookup"><span data-stu-id="d6ecc-134">1</span></span>           | <span data-ttu-id="d6ecc-135">+F</span><span class="sxs-lookup"><span data-stu-id="d6ecc-135">+F</span></span>     | <span data-ttu-id="d6ecc-136">+inf</span><span class="sxs-lookup"><span data-stu-id="d6ecc-136">+inf</span></span>     | <span data-ttu-id="d6ecc-137">NaN</span><span class="sxs-lookup"><span data-stu-id="d6ecc-137">NaN</span></span>     |



 

<span data-ttu-id="d6ecc-138">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="d6ecc-138">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="d6ecc-139">頂點著色器</span><span class="sxs-lookup"><span data-stu-id="d6ecc-139">Vertex Shader</span></span> | <span data-ttu-id="d6ecc-140">幾何著色器</span><span class="sxs-lookup"><span data-stu-id="d6ecc-140">Geometry Shader</span></span> | <span data-ttu-id="d6ecc-141">像素著色器</span><span class="sxs-lookup"><span data-stu-id="d6ecc-141">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="d6ecc-142">x</span><span class="sxs-lookup"><span data-stu-id="d6ecc-142">x</span></span>             | <span data-ttu-id="d6ecc-143">x</span><span class="sxs-lookup"><span data-stu-id="d6ecc-143">x</span></span>               | <span data-ttu-id="d6ecc-144">x</span><span class="sxs-lookup"><span data-stu-id="d6ecc-144">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="d6ecc-145">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="d6ecc-145">Minimum Shader Model</span></span>

<span data-ttu-id="d6ecc-146">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="d6ecc-146">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="d6ecc-147">著色器模型</span><span class="sxs-lookup"><span data-stu-id="d6ecc-147">Shader Model</span></span>                                              | <span data-ttu-id="d6ecc-148">支援</span><span class="sxs-lookup"><span data-stu-id="d6ecc-148">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="d6ecc-149">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="d6ecc-149">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="d6ecc-150">是</span><span class="sxs-lookup"><span data-stu-id="d6ecc-150">yes</span></span>       |
| [<span data-ttu-id="d6ecc-151">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="d6ecc-151">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="d6ecc-152">是</span><span class="sxs-lookup"><span data-stu-id="d6ecc-152">yes</span></span>       |
| [<span data-ttu-id="d6ecc-153">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="d6ecc-153">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="d6ecc-154">是</span><span class="sxs-lookup"><span data-stu-id="d6ecc-154">yes</span></span>       |
| [<span data-ttu-id="d6ecc-155">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="d6ecc-155">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="d6ecc-156">否</span><span class="sxs-lookup"><span data-stu-id="d6ecc-156">no</span></span>        |
| [<span data-ttu-id="d6ecc-157">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="d6ecc-157">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="d6ecc-158">否</span><span class="sxs-lookup"><span data-stu-id="d6ecc-158">no</span></span>        |
| [<span data-ttu-id="d6ecc-159">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="d6ecc-159">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="d6ecc-160">否</span><span class="sxs-lookup"><span data-stu-id="d6ecc-160">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="d6ecc-161">相關主題</span><span class="sxs-lookup"><span data-stu-id="d6ecc-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d6ecc-162">著色器模型4元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="d6ecc-162">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





