---
title: 'frc (sm4-asm) '
description: 元件的 [解壓縮小數] 元件。
ms.assetid: 17C88BCE-7F2F-446C-9BB4-860098B5E42A
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4abcfd56e7d6051e9c476097b3e5eef4d97563e
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104971588"
---
# <a name="frc-sm4---asm"></a><span data-ttu-id="dc206-103">frc (sm4-asm) </span><span class="sxs-lookup"><span data-stu-id="dc206-103">frc (sm4 - asm)</span></span>

<span data-ttu-id="dc206-104">元件的 [解壓縮小數] 元件。</span><span class="sxs-lookup"><span data-stu-id="dc206-104">Component-wise, extract fractional component.</span></span>



| <span data-ttu-id="dc206-105">frc \[ \_ sat \] dest \[ . mask \] ， \[ - \] src0 \[ \_ abs \] \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="dc206-105">frc\[\_sat\] dest\[.mask\], \[-\] src0\[\_abs\]\[.swizzle\]</span></span> |
|-------------------------------------------------------------|



 



| <span data-ttu-id="dc206-106">項目</span><span class="sxs-lookup"><span data-stu-id="dc206-106">Item</span></span>                                                            | <span data-ttu-id="dc206-107">描述</span><span class="sxs-lookup"><span data-stu-id="dc206-107">Description</span></span>                                                                                                                              |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc206-108"><span id="dest"></span><span id="DEST"></span>*目標*</span><span class="sxs-lookup"><span data-stu-id="dc206-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="dc206-109">\[在 \] 操作結果的位址中。</span><span class="sxs-lookup"><span data-stu-id="dc206-109">\[in\] The address of the result of the operation.</span></span><br/> <span data-ttu-id="dc206-110">*目的地*  = *src0*  -  (*src0*) 的 [回合 \_ ni](round-ni--sm4---asm-.md)</span><span class="sxs-lookup"><span data-stu-id="dc206-110">*dest* = *src0* - [round\_ni](round-ni--sm4---asm-.md)(*src0*)</span></span><br/> |
| <span data-ttu-id="dc206-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="dc206-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="dc206-112">\[在作業 \] 的元件中。</span><span class="sxs-lookup"><span data-stu-id="dc206-112">\[in\] The component in the operation.</span></span><br/>                                                                                        |



 

## <a name="remarks"></a><span data-ttu-id="dc206-113">備註</span><span class="sxs-lookup"><span data-stu-id="dc206-113">Remarks</span></span>

<span data-ttu-id="dc206-114">下表顯示使用各種不同的數位類別來執行指令時所取得的結果。</span><span class="sxs-lookup"><span data-stu-id="dc206-114">The following table shows the results obtained when executing the instruction with various classes of numbers.</span></span>



|          |          |            |             |        |        |             |            |          |         |
|----------|----------|------------|-------------|--------|--------|-------------|------------|----------|---------|
| <span data-ttu-id="dc206-115">**src**</span><span class="sxs-lookup"><span data-stu-id="dc206-115">**src**</span></span>  | <span data-ttu-id="dc206-116">**-inf**</span><span class="sxs-lookup"><span data-stu-id="dc206-116">**-inf**</span></span> | <span data-ttu-id="dc206-117">**-F**</span><span class="sxs-lookup"><span data-stu-id="dc206-117">**-F**</span></span>     | <span data-ttu-id="dc206-118">**-denorm**</span><span class="sxs-lookup"><span data-stu-id="dc206-118">**-denorm**</span></span> | <span data-ttu-id="dc206-119">**-0**</span><span class="sxs-lookup"><span data-stu-id="dc206-119">**-0**</span></span> | <span data-ttu-id="dc206-120">**+0**</span><span class="sxs-lookup"><span data-stu-id="dc206-120">**+0**</span></span> | <span data-ttu-id="dc206-121">**+ denorm**</span><span class="sxs-lookup"><span data-stu-id="dc206-121">**+denorm**</span></span> | <span data-ttu-id="dc206-122">**+ F**</span><span class="sxs-lookup"><span data-stu-id="dc206-122">**+F**</span></span>     | <span data-ttu-id="dc206-123">**+ inf**</span><span class="sxs-lookup"><span data-stu-id="dc206-123">**+inf**</span></span> | <span data-ttu-id="dc206-124">**NaN**</span><span class="sxs-lookup"><span data-stu-id="dc206-124">**NaN**</span></span> |
| <span data-ttu-id="dc206-125">**目標**</span><span class="sxs-lookup"><span data-stu-id="dc206-125">**dest**</span></span> | <span data-ttu-id="dc206-126">NaN</span><span class="sxs-lookup"><span data-stu-id="dc206-126">NaN</span></span>      | <span data-ttu-id="dc206-127">\[+ 0 至 1) </span><span class="sxs-lookup"><span data-stu-id="dc206-127">\[+0 to 1)</span></span> | <span data-ttu-id="dc206-128">+0</span><span class="sxs-lookup"><span data-stu-id="dc206-128">+0</span></span>          | <span data-ttu-id="dc206-129">+0</span><span class="sxs-lookup"><span data-stu-id="dc206-129">+0</span></span>     | <span data-ttu-id="dc206-130">+0</span><span class="sxs-lookup"><span data-stu-id="dc206-130">+0</span></span>     | <span data-ttu-id="dc206-131">+0</span><span class="sxs-lookup"><span data-stu-id="dc206-131">+0</span></span>          | <span data-ttu-id="dc206-132">\[+ 0 至 1) </span><span class="sxs-lookup"><span data-stu-id="dc206-132">\[+0 to 1)</span></span> | <span data-ttu-id="dc206-133">NaN</span><span class="sxs-lookup"><span data-stu-id="dc206-133">NaN</span></span>      | <span data-ttu-id="dc206-134">NaN</span><span class="sxs-lookup"><span data-stu-id="dc206-134">NaN</span></span>     |



 

<span data-ttu-id="dc206-135">F 表示有限實數。</span><span class="sxs-lookup"><span data-stu-id="dc206-135">F means finite-real number.</span></span>

<span data-ttu-id="dc206-136">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="dc206-136">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="dc206-137">頂點著色器</span><span class="sxs-lookup"><span data-stu-id="dc206-137">Vertex Shader</span></span> | <span data-ttu-id="dc206-138">幾何著色器</span><span class="sxs-lookup"><span data-stu-id="dc206-138">Geometry Shader</span></span> | <span data-ttu-id="dc206-139">像素著色器</span><span class="sxs-lookup"><span data-stu-id="dc206-139">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="dc206-140">x</span><span class="sxs-lookup"><span data-stu-id="dc206-140">x</span></span>             | <span data-ttu-id="dc206-141">x</span><span class="sxs-lookup"><span data-stu-id="dc206-141">x</span></span>               | <span data-ttu-id="dc206-142">x</span><span class="sxs-lookup"><span data-stu-id="dc206-142">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="dc206-143">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="dc206-143">Minimum Shader Model</span></span>

<span data-ttu-id="dc206-144">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="dc206-144">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="dc206-145">著色器模型</span><span class="sxs-lookup"><span data-stu-id="dc206-145">Shader Model</span></span>                                              | <span data-ttu-id="dc206-146">支援</span><span class="sxs-lookup"><span data-stu-id="dc206-146">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="dc206-147">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="dc206-147">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="dc206-148">是</span><span class="sxs-lookup"><span data-stu-id="dc206-148">yes</span></span>       |
| [<span data-ttu-id="dc206-149">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="dc206-149">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="dc206-150">是</span><span class="sxs-lookup"><span data-stu-id="dc206-150">yes</span></span>       |
| [<span data-ttu-id="dc206-151">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="dc206-151">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="dc206-152">是</span><span class="sxs-lookup"><span data-stu-id="dc206-152">yes</span></span>       |
| [<span data-ttu-id="dc206-153">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="dc206-153">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="dc206-154">不可以</span><span class="sxs-lookup"><span data-stu-id="dc206-154">no</span></span>        |
| [<span data-ttu-id="dc206-155">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="dc206-155">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="dc206-156">不可以</span><span class="sxs-lookup"><span data-stu-id="dc206-156">no</span></span>        |
| [<span data-ttu-id="dc206-157">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="dc206-157">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="dc206-158">不可以</span><span class="sxs-lookup"><span data-stu-id="dc206-158">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="dc206-159">相關主題</span><span class="sxs-lookup"><span data-stu-id="dc206-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dc206-160">著色器模型4元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="dc206-160">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





