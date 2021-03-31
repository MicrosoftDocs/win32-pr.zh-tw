---
title: 'sqrt (sm4-asm) '
description: 以元件為依據的平方根。
ms.assetid: B860D656-7F01-484F-909F-A5C9A61C52C3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0a12afaf5b2366dac15c953d509a6814b48a6b9
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104373803"
---
# <a name="sqrt-sm4---asm"></a><span data-ttu-id="9a223-103">sqrt (sm4-asm) </span><span class="sxs-lookup"><span data-stu-id="9a223-103">sqrt (sm4 - asm)</span></span>

<span data-ttu-id="9a223-104">以元件為依據的平方根。</span><span class="sxs-lookup"><span data-stu-id="9a223-104">Component-wise square root.</span></span>



| <span data-ttu-id="9a223-105">sqrt \[ \_ sat \] dest \[ . mask \] ， \[ - \] src0 \[ \_ abs \] \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="9a223-105">sqrt\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|-------------------------------------------------------------|



 



| <span data-ttu-id="9a223-106">項目</span><span class="sxs-lookup"><span data-stu-id="9a223-106">Item</span></span>                                                            | <span data-ttu-id="9a223-107">描述</span><span class="sxs-lookup"><span data-stu-id="9a223-107">Description</span></span>                                                                     |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="9a223-108"><span id="dest"></span><span id="DEST"></span>*目標*</span><span class="sxs-lookup"><span data-stu-id="9a223-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="9a223-109">\[在作業的 \] 結果中。</span><span class="sxs-lookup"><span data-stu-id="9a223-109">\[in\] The result of the operation.</span></span><br/> <span data-ttu-id="9a223-110">*dest* = sqrt (*src0*) </span><span class="sxs-lookup"><span data-stu-id="9a223-110">*dest* = sqrt(*src0*)</span></span><br/> |
| <span data-ttu-id="9a223-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="9a223-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="9a223-112">\[在 \] 要採用平方根的元件中。</span><span class="sxs-lookup"><span data-stu-id="9a223-112">\[in\] The components for which to take the square root.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="9a223-113">備註</span><span class="sxs-lookup"><span data-stu-id="9a223-113">Remarks</span></span>

<span data-ttu-id="9a223-114">有效位數為 1 ulp。</span><span class="sxs-lookup"><span data-stu-id="9a223-114">Precision is 1 ulp.</span></span>

<span data-ttu-id="9a223-115">下表顯示使用各種不同的數位類別來執行指令時所取得的結果，前提是不會發生溢位或下溢。</span><span class="sxs-lookup"><span data-stu-id="9a223-115">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span>

<span data-ttu-id="9a223-116">F 表示有限實數。</span><span class="sxs-lookup"><span data-stu-id="9a223-116">F means finite-real number.</span></span>



|          |          |        |             |        |        |             |        |          |         |
|----------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
|          | <span data-ttu-id="9a223-117">**-inf**</span><span class="sxs-lookup"><span data-stu-id="9a223-117">**-inf**</span></span> | <span data-ttu-id="9a223-118">**-F**</span><span class="sxs-lookup"><span data-stu-id="9a223-118">**-F**</span></span> | <span data-ttu-id="9a223-119">**-denorm**</span><span class="sxs-lookup"><span data-stu-id="9a223-119">**-denorm**</span></span> | <span data-ttu-id="9a223-120">**-0**</span><span class="sxs-lookup"><span data-stu-id="9a223-120">**-0**</span></span> | <span data-ttu-id="9a223-121">**+0**</span><span class="sxs-lookup"><span data-stu-id="9a223-121">**+0**</span></span> | <span data-ttu-id="9a223-122">**+ denorm**</span><span class="sxs-lookup"><span data-stu-id="9a223-122">**+denorm**</span></span> | <span data-ttu-id="9a223-123">**+ F**</span><span class="sxs-lookup"><span data-stu-id="9a223-123">**+F**</span></span> | <span data-ttu-id="9a223-124">**+ inf**</span><span class="sxs-lookup"><span data-stu-id="9a223-124">**+inf**</span></span> | <span data-ttu-id="9a223-125">**NaN**</span><span class="sxs-lookup"><span data-stu-id="9a223-125">**NaN**</span></span> |
| <span data-ttu-id="9a223-126">**目標**</span><span class="sxs-lookup"><span data-stu-id="9a223-126">**dest**</span></span> | <span data-ttu-id="9a223-127">NaN</span><span class="sxs-lookup"><span data-stu-id="9a223-127">NaN</span></span>      | <span data-ttu-id="9a223-128">NaN</span><span class="sxs-lookup"><span data-stu-id="9a223-128">NaN</span></span>    | <span data-ttu-id="9a223-129">-0</span><span class="sxs-lookup"><span data-stu-id="9a223-129">-0</span></span>          | <span data-ttu-id="9a223-130">-0</span><span class="sxs-lookup"><span data-stu-id="9a223-130">-0</span></span>     | <span data-ttu-id="9a223-131">+0</span><span class="sxs-lookup"><span data-stu-id="9a223-131">+0</span></span>     | <span data-ttu-id="9a223-132">+0</span><span class="sxs-lookup"><span data-stu-id="9a223-132">+0</span></span>          | <span data-ttu-id="9a223-133">+F</span><span class="sxs-lookup"><span data-stu-id="9a223-133">+F</span></span>     | <span data-ttu-id="9a223-134">+inf</span><span class="sxs-lookup"><span data-stu-id="9a223-134">+inf</span></span>     | <span data-ttu-id="9a223-135">NaN</span><span class="sxs-lookup"><span data-stu-id="9a223-135">NaN</span></span>     |



 

<span data-ttu-id="9a223-136">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="9a223-136">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="9a223-137">頂點著色器</span><span class="sxs-lookup"><span data-stu-id="9a223-137">Vertex Shader</span></span> | <span data-ttu-id="9a223-138">幾何著色器</span><span class="sxs-lookup"><span data-stu-id="9a223-138">Geometry Shader</span></span> | <span data-ttu-id="9a223-139">像素著色器</span><span class="sxs-lookup"><span data-stu-id="9a223-139">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="9a223-140">x</span><span class="sxs-lookup"><span data-stu-id="9a223-140">x</span></span>             | <span data-ttu-id="9a223-141">x</span><span class="sxs-lookup"><span data-stu-id="9a223-141">x</span></span>               | <span data-ttu-id="9a223-142">x</span><span class="sxs-lookup"><span data-stu-id="9a223-142">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="9a223-143">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="9a223-143">Minimum Shader Model</span></span>

<span data-ttu-id="9a223-144">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="9a223-144">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="9a223-145">著色器模型</span><span class="sxs-lookup"><span data-stu-id="9a223-145">Shader Model</span></span>                                              | <span data-ttu-id="9a223-146">支援</span><span class="sxs-lookup"><span data-stu-id="9a223-146">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="9a223-147">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="9a223-147">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="9a223-148">是</span><span class="sxs-lookup"><span data-stu-id="9a223-148">yes</span></span>       |
| [<span data-ttu-id="9a223-149">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="9a223-149">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="9a223-150">是</span><span class="sxs-lookup"><span data-stu-id="9a223-150">yes</span></span>       |
| [<span data-ttu-id="9a223-151">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="9a223-151">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="9a223-152">是</span><span class="sxs-lookup"><span data-stu-id="9a223-152">yes</span></span>       |
| [<span data-ttu-id="9a223-153">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="9a223-153">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="9a223-154">不可以</span><span class="sxs-lookup"><span data-stu-id="9a223-154">no</span></span>        |
| [<span data-ttu-id="9a223-155">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="9a223-155">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="9a223-156">不可以</span><span class="sxs-lookup"><span data-stu-id="9a223-156">no</span></span>        |
| [<span data-ttu-id="9a223-157">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="9a223-157">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="9a223-158">不可以</span><span class="sxs-lookup"><span data-stu-id="9a223-158">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="9a223-159">相關主題</span><span class="sxs-lookup"><span data-stu-id="9a223-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9a223-160">著色器模型4元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="9a223-160">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





