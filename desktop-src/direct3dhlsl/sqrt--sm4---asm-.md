---
title: 'sqrt (sm4-asm) '
description: 以元件為依據的平方根。
ms.assetid: B860D656-7F01-484F-909F-A5C9A61C52C3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 628601e0a3a78784a5fd1a089ef7608a0cf9ca05
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996605"
---
# <a name="sqrt-sm4---asm"></a><span data-ttu-id="bff14-103">sqrt (sm4-asm) </span><span class="sxs-lookup"><span data-stu-id="bff14-103">sqrt (sm4 - asm)</span></span>

<span data-ttu-id="bff14-104">以元件為依據的平方根。</span><span class="sxs-lookup"><span data-stu-id="bff14-104">Component-wise square root.</span></span>



| <span data-ttu-id="bff14-105">sqrt \[ \_ sat \] dest \[ . mask \] ， \[ - \] src0 \[ \_ abs \] \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="bff14-105">sqrt\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|-------------------------------------------------------------|



 



| <span data-ttu-id="bff14-106">項目</span><span class="sxs-lookup"><span data-stu-id="bff14-106">Item</span></span>                                                            | <span data-ttu-id="bff14-107">描述</span><span class="sxs-lookup"><span data-stu-id="bff14-107">Description</span></span>                                                                     |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="bff14-108"><span id="dest"></span><span id="DEST"></span>*目標*</span><span class="sxs-lookup"><span data-stu-id="bff14-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="bff14-109">\[在作業的 \] 結果中。</span><span class="sxs-lookup"><span data-stu-id="bff14-109">\[in\] The result of the operation.</span></span><br/> <span data-ttu-id="bff14-110">*dest* = sqrt (*src0*) </span><span class="sxs-lookup"><span data-stu-id="bff14-110">*dest* = sqrt(*src0*)</span></span><br/> |
| <span data-ttu-id="bff14-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="bff14-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="bff14-112">\[在 \] 要採用平方根的元件中。</span><span class="sxs-lookup"><span data-stu-id="bff14-112">\[in\] The components for which to take the square root.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="bff14-113">備註</span><span class="sxs-lookup"><span data-stu-id="bff14-113">Remarks</span></span>

<span data-ttu-id="bff14-114">有效位數為 1 ulp。</span><span class="sxs-lookup"><span data-stu-id="bff14-114">Precision is 1 ulp.</span></span>

<span data-ttu-id="bff14-115">下表顯示使用各種不同的數位類別來執行指令時所取得的結果，前提是不會發生溢位或下溢。</span><span class="sxs-lookup"><span data-stu-id="bff14-115">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span>

<span data-ttu-id="bff14-116">F 表示有限實數。</span><span class="sxs-lookup"><span data-stu-id="bff14-116">F means finite-real number.</span></span>



|          | <span data-ttu-id="bff14-117">**-inf**</span><span class="sxs-lookup"><span data-stu-id="bff14-117">**-inf**</span></span> | <span data-ttu-id="bff14-118">**-F**</span><span class="sxs-lookup"><span data-stu-id="bff14-118">**-F**</span></span> | <span data-ttu-id="bff14-119">**-denorm**</span><span class="sxs-lookup"><span data-stu-id="bff14-119">**-denorm**</span></span> | <span data-ttu-id="bff14-120">**-0**</span><span class="sxs-lookup"><span data-stu-id="bff14-120">**-0**</span></span> | <span data-ttu-id="bff14-121">**+0**</span><span class="sxs-lookup"><span data-stu-id="bff14-121">**+0**</span></span> | <span data-ttu-id="bff14-122">**+ denorm**</span><span class="sxs-lookup"><span data-stu-id="bff14-122">**+denorm**</span></span> | <span data-ttu-id="bff14-123">**+ F**</span><span class="sxs-lookup"><span data-stu-id="bff14-123">**+F**</span></span> | <span data-ttu-id="bff14-124">**+ inf**</span><span class="sxs-lookup"><span data-stu-id="bff14-124">**+inf**</span></span> | <span data-ttu-id="bff14-125">**NaN**</span><span class="sxs-lookup"><span data-stu-id="bff14-125">**NaN**</span></span> |
|----------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| <span data-ttu-id="bff14-126">**目標**</span><span class="sxs-lookup"><span data-stu-id="bff14-126">**dest**</span></span> | <span data-ttu-id="bff14-127">NaN</span><span class="sxs-lookup"><span data-stu-id="bff14-127">NaN</span></span>      | <span data-ttu-id="bff14-128">NaN</span><span class="sxs-lookup"><span data-stu-id="bff14-128">NaN</span></span>    | <span data-ttu-id="bff14-129">-0</span><span class="sxs-lookup"><span data-stu-id="bff14-129">-0</span></span>          | <span data-ttu-id="bff14-130">-0</span><span class="sxs-lookup"><span data-stu-id="bff14-130">-0</span></span>     | <span data-ttu-id="bff14-131">+0</span><span class="sxs-lookup"><span data-stu-id="bff14-131">+0</span></span>     | <span data-ttu-id="bff14-132">+0</span><span class="sxs-lookup"><span data-stu-id="bff14-132">+0</span></span>          | <span data-ttu-id="bff14-133">+F</span><span class="sxs-lookup"><span data-stu-id="bff14-133">+F</span></span>     | <span data-ttu-id="bff14-134">+inf</span><span class="sxs-lookup"><span data-stu-id="bff14-134">+inf</span></span>     | <span data-ttu-id="bff14-135">NaN</span><span class="sxs-lookup"><span data-stu-id="bff14-135">NaN</span></span>     |



 

<span data-ttu-id="bff14-136">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="bff14-136">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="bff14-137">頂點著色器</span><span class="sxs-lookup"><span data-stu-id="bff14-137">Vertex Shader</span></span> | <span data-ttu-id="bff14-138">幾何著色器</span><span class="sxs-lookup"><span data-stu-id="bff14-138">Geometry Shader</span></span> | <span data-ttu-id="bff14-139">像素著色器</span><span class="sxs-lookup"><span data-stu-id="bff14-139">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="bff14-140">x</span><span class="sxs-lookup"><span data-stu-id="bff14-140">x</span></span>             | <span data-ttu-id="bff14-141">x</span><span class="sxs-lookup"><span data-stu-id="bff14-141">x</span></span>               | <span data-ttu-id="bff14-142">x</span><span class="sxs-lookup"><span data-stu-id="bff14-142">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="bff14-143">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="bff14-143">Minimum Shader Model</span></span>

<span data-ttu-id="bff14-144">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="bff14-144">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="bff14-145">著色器模型</span><span class="sxs-lookup"><span data-stu-id="bff14-145">Shader Model</span></span>                                              | <span data-ttu-id="bff14-146">支援</span><span class="sxs-lookup"><span data-stu-id="bff14-146">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="bff14-147">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="bff14-147">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="bff14-148">是</span><span class="sxs-lookup"><span data-stu-id="bff14-148">yes</span></span>       |
| [<span data-ttu-id="bff14-149">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="bff14-149">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="bff14-150">是</span><span class="sxs-lookup"><span data-stu-id="bff14-150">yes</span></span>       |
| [<span data-ttu-id="bff14-151">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="bff14-151">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="bff14-152">是</span><span class="sxs-lookup"><span data-stu-id="bff14-152">yes</span></span>       |
| [<span data-ttu-id="bff14-153">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="bff14-153">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="bff14-154">否</span><span class="sxs-lookup"><span data-stu-id="bff14-154">no</span></span>        |
| [<span data-ttu-id="bff14-155">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="bff14-155">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="bff14-156">否</span><span class="sxs-lookup"><span data-stu-id="bff14-156">no</span></span>        |
| [<span data-ttu-id="bff14-157">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="bff14-157">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="bff14-158">否</span><span class="sxs-lookup"><span data-stu-id="bff14-158">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="bff14-159">相關主題</span><span class="sxs-lookup"><span data-stu-id="bff14-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bff14-160">著色器模型4元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="bff14-160">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





