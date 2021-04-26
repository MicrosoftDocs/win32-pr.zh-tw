---
title: 'frc (sm4-asm) '
description: 元件的 [解壓縮小數] 元件。
ms.assetid: 17C88BCE-7F2F-446C-9BB4-860098B5E42A
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f59b747f38fb970b92b5e48610873efe781d63d
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107993915"
---
# <a name="frc-sm4---asm"></a><span data-ttu-id="ca205-103">frc (sm4-asm) </span><span class="sxs-lookup"><span data-stu-id="ca205-103">frc (sm4 - asm)</span></span>

<span data-ttu-id="ca205-104">元件的 [解壓縮小數] 元件。</span><span class="sxs-lookup"><span data-stu-id="ca205-104">Component-wise, extract fractional component.</span></span>



| <span data-ttu-id="ca205-105">frc \[ \_ sat \] dest \[ . mask \] ， \[ - \] src0 \[ \_ abs \] \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="ca205-105">frc\[\_sat\] dest\[.mask\], \[-\] src0\[\_abs\]\[.swizzle\]</span></span> |
|-------------------------------------------------------------|



 



| <span data-ttu-id="ca205-106">項目</span><span class="sxs-lookup"><span data-stu-id="ca205-106">Item</span></span>                                                            | <span data-ttu-id="ca205-107">描述</span><span class="sxs-lookup"><span data-stu-id="ca205-107">Description</span></span>                                                                                                                              |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca205-108"><span id="dest"></span><span id="DEST"></span>*目標*</span><span class="sxs-lookup"><span data-stu-id="ca205-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="ca205-109">\[在 \] 操作結果的位址中。</span><span class="sxs-lookup"><span data-stu-id="ca205-109">\[in\] The address of the result of the operation.</span></span><br/> <span data-ttu-id="ca205-110">*目的地*  = *src0*  -  (*src0*) 的 [回合 \_ ni](round-ni--sm4---asm-.md)</span><span class="sxs-lookup"><span data-stu-id="ca205-110">*dest* = *src0* - [round\_ni](round-ni--sm4---asm-.md)(*src0*)</span></span><br/> |
| <span data-ttu-id="ca205-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="ca205-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="ca205-112">\[在作業 \] 的元件中。</span><span class="sxs-lookup"><span data-stu-id="ca205-112">\[in\] The component in the operation.</span></span><br/>                                                                                        |



 

## <a name="remarks"></a><span data-ttu-id="ca205-113">備註</span><span class="sxs-lookup"><span data-stu-id="ca205-113">Remarks</span></span>

<span data-ttu-id="ca205-114">下表顯示使用各種不同的數位類別來執行指令時所取得的結果。</span><span class="sxs-lookup"><span data-stu-id="ca205-114">The following table shows the results obtained when executing the instruction with various classes of numbers.</span></span>



| <span data-ttu-id="ca205-115">**src**</span><span class="sxs-lookup"><span data-stu-id="ca205-115">**src**</span></span>  | <span data-ttu-id="ca205-116">**-inf**</span><span class="sxs-lookup"><span data-stu-id="ca205-116">**-inf**</span></span> | <span data-ttu-id="ca205-117">**-F**</span><span class="sxs-lookup"><span data-stu-id="ca205-117">**-F**</span></span>     | <span data-ttu-id="ca205-118">**-denorm**</span><span class="sxs-lookup"><span data-stu-id="ca205-118">**-denorm**</span></span> | <span data-ttu-id="ca205-119">**-0**</span><span class="sxs-lookup"><span data-stu-id="ca205-119">**-0**</span></span> | <span data-ttu-id="ca205-120">**+0**</span><span class="sxs-lookup"><span data-stu-id="ca205-120">**+0**</span></span> | <span data-ttu-id="ca205-121">**+ denorm**</span><span class="sxs-lookup"><span data-stu-id="ca205-121">**+denorm**</span></span> | <span data-ttu-id="ca205-122">**+ F**</span><span class="sxs-lookup"><span data-stu-id="ca205-122">**+F**</span></span>     | <span data-ttu-id="ca205-123">**+ inf**</span><span class="sxs-lookup"><span data-stu-id="ca205-123">**+inf**</span></span> | <span data-ttu-id="ca205-124">**NaN**</span><span class="sxs-lookup"><span data-stu-id="ca205-124">**NaN**</span></span> |
|----------|----------|------------|-------------|--------|--------|-------------|------------|----------|---------|
| <span data-ttu-id="ca205-125">**目標**</span><span class="sxs-lookup"><span data-stu-id="ca205-125">**dest**</span></span> | <span data-ttu-id="ca205-126">NaN</span><span class="sxs-lookup"><span data-stu-id="ca205-126">NaN</span></span>      | <span data-ttu-id="ca205-127">\[+ 0 至 1) </span><span class="sxs-lookup"><span data-stu-id="ca205-127">\[+0 to 1)</span></span> | <span data-ttu-id="ca205-128">+0</span><span class="sxs-lookup"><span data-stu-id="ca205-128">+0</span></span>          | <span data-ttu-id="ca205-129">+0</span><span class="sxs-lookup"><span data-stu-id="ca205-129">+0</span></span>     | <span data-ttu-id="ca205-130">+0</span><span class="sxs-lookup"><span data-stu-id="ca205-130">+0</span></span>     | <span data-ttu-id="ca205-131">+0</span><span class="sxs-lookup"><span data-stu-id="ca205-131">+0</span></span>          | <span data-ttu-id="ca205-132">\[+ 0 至 1) </span><span class="sxs-lookup"><span data-stu-id="ca205-132">\[+0 to 1)</span></span> | <span data-ttu-id="ca205-133">NaN</span><span class="sxs-lookup"><span data-stu-id="ca205-133">NaN</span></span>      | <span data-ttu-id="ca205-134">NaN</span><span class="sxs-lookup"><span data-stu-id="ca205-134">NaN</span></span>     |



 

<span data-ttu-id="ca205-135">F 表示有限實數。</span><span class="sxs-lookup"><span data-stu-id="ca205-135">F means finite-real number.</span></span>

<span data-ttu-id="ca205-136">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="ca205-136">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="ca205-137">頂點著色器</span><span class="sxs-lookup"><span data-stu-id="ca205-137">Vertex Shader</span></span> | <span data-ttu-id="ca205-138">幾何著色器</span><span class="sxs-lookup"><span data-stu-id="ca205-138">Geometry Shader</span></span> | <span data-ttu-id="ca205-139">像素著色器</span><span class="sxs-lookup"><span data-stu-id="ca205-139">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="ca205-140">x</span><span class="sxs-lookup"><span data-stu-id="ca205-140">x</span></span>             | <span data-ttu-id="ca205-141">x</span><span class="sxs-lookup"><span data-stu-id="ca205-141">x</span></span>               | <span data-ttu-id="ca205-142">x</span><span class="sxs-lookup"><span data-stu-id="ca205-142">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="ca205-143">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="ca205-143">Minimum Shader Model</span></span>

<span data-ttu-id="ca205-144">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="ca205-144">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="ca205-145">著色器模型</span><span class="sxs-lookup"><span data-stu-id="ca205-145">Shader Model</span></span>                                              | <span data-ttu-id="ca205-146">支援</span><span class="sxs-lookup"><span data-stu-id="ca205-146">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="ca205-147">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="ca205-147">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="ca205-148">是</span><span class="sxs-lookup"><span data-stu-id="ca205-148">yes</span></span>       |
| [<span data-ttu-id="ca205-149">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="ca205-149">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="ca205-150">是</span><span class="sxs-lookup"><span data-stu-id="ca205-150">yes</span></span>       |
| [<span data-ttu-id="ca205-151">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="ca205-151">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="ca205-152">是</span><span class="sxs-lookup"><span data-stu-id="ca205-152">yes</span></span>       |
| [<span data-ttu-id="ca205-153">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="ca205-153">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="ca205-154">否</span><span class="sxs-lookup"><span data-stu-id="ca205-154">no</span></span>        |
| [<span data-ttu-id="ca205-155">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="ca205-155">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="ca205-156">否</span><span class="sxs-lookup"><span data-stu-id="ca205-156">no</span></span>        |
| [<span data-ttu-id="ca205-157">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="ca205-157">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="ca205-158">否</span><span class="sxs-lookup"><span data-stu-id="ca205-158">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="ca205-159">相關主題</span><span class="sxs-lookup"><span data-stu-id="ca205-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ca205-160">著色器模型4元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="ca205-160">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





