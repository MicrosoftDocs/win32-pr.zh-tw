---
title: 'deq (sm5-asm) '
description: 元件的雙精確度相等比較。
ms.assetid: 99806989-D3A0-43F4-832A-5F1BD9C59A11
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0ed263deec975815f29050d2de0a877a312258c
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104507716"
---
# <a name="deq-sm5---asm"></a><span data-ttu-id="d60a6-103">deq (sm5-asm) </span><span class="sxs-lookup"><span data-stu-id="d60a6-103">deq (sm5 - asm)</span></span>

<span data-ttu-id="d60a6-104">元件的雙精確度相等比較。</span><span class="sxs-lookup"><span data-stu-id="d60a6-104">Component-wise double-precision equality comparison.</span></span>



| <span data-ttu-id="d60a6-105">deq \[ \_ sat \] dest \[ . mask \] ， \[ - \] src0 \[ \_ abs \] \[ . swizzle \] ， \[ - \] src1 \[ \_ abs \] \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="d60a6-105">deq\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\]</span></span> |
|--------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="d60a6-106">項目</span><span class="sxs-lookup"><span data-stu-id="d60a6-106">Item</span></span>                                                            | <span data-ttu-id="d60a6-107">描述</span><span class="sxs-lookup"><span data-stu-id="d60a6-107">Description</span></span>                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="d60a6-108"><span id="dest"></span><span id="DEST"></span>*目標*</span><span class="sxs-lookup"><span data-stu-id="d60a6-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="d60a6-109">\[在 \] 操作結果的位址中。</span><span class="sxs-lookup"><span data-stu-id="d60a6-109">\[in\] The address of the results of the operation.</span></span><br/> |
| <span data-ttu-id="d60a6-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="d60a6-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="d60a6-111">\[在 \] [要與 *src1* 比較的元件] 中。</span><span class="sxs-lookup"><span data-stu-id="d60a6-111">\[in\] The components to compare to *src1*.</span></span><br/>         |
| <span data-ttu-id="d60a6-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="d60a6-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="d60a6-113">\[在 \] [要與 *src0* 比較的元件] 中。</span><span class="sxs-lookup"><span data-stu-id="d60a6-113">\[in\] The components to compare to *src0*.</span></span><br/>         |



 

## <a name="remarks"></a><span data-ttu-id="d60a6-114">備註</span><span class="sxs-lookup"><span data-stu-id="d60a6-114">Remarks</span></span>

<span data-ttu-id="d60a6-115">此指令會針對每個元件執行雙精確度浮點數比較 (*src0*  ==  *src1*) ，並將結果寫入至 *目的地*。</span><span class="sxs-lookup"><span data-stu-id="d60a6-115">This instruction performs the double-precision floating-point comparison (*src0* == *src1*) for each component and writes the result to *dest*.</span></span>

<span data-ttu-id="d60a6-116">如果比較結果為 true，則會傳回該元件的32位0xFFFFFFFF。</span><span class="sxs-lookup"><span data-stu-id="d60a6-116">If the comparison is true, then 32-bit 0xFFFFFFFF is returned for that component.</span></span> <span data-ttu-id="d60a6-117">否則會傳回32位0x00000000。</span><span class="sxs-lookup"><span data-stu-id="d60a6-117">Otherwise 32-bit 0x00000000 is returned.</span></span>

<span data-ttu-id="d60a6-118">與 NaN 的比較會傳回 false。</span><span class="sxs-lookup"><span data-stu-id="d60a6-118">Comparison with NaN returns false.</span></span>

<span data-ttu-id="d60a6-119">有效的 *目的地* 遮罩是任何一或兩個元件。</span><span class="sxs-lookup"><span data-stu-id="d60a6-119">The valid *dest* masks are any one or 2 components.</span></span> <span data-ttu-id="d60a6-120">亦即：. x、. y、. z、w、xy、xw、. yz、. yw、. zw 遮罩中的第一個 *目的地* 元件會收到第一個雙重比較的32位結果。</span><span class="sxs-lookup"><span data-stu-id="d60a6-120">That is: .x, .y, .z, .w, .xy, .xz, .xw, .yz, .yw, .zw The first *dest* component in the mask receives the 32-bit result for the first double comparison.</span></span> <span data-ttu-id="d60a6-121">遮罩中的第二個元件（如果有的話）會接收第二個雙重比較的32位結果。</span><span class="sxs-lookup"><span data-stu-id="d60a6-121">The second component in the mask, if present, receives the 32-bit result for the second double comparison.</span></span>

<span data-ttu-id="d60a6-122">來源參數的有效 swizzles 為. xyzw、. xyxy、. zwxy、. zwzw。</span><span class="sxs-lookup"><span data-stu-id="d60a6-122">The valid swizzles for the source parameters are .xyzw, .xyxy, .zwxy, .zwzw.</span></span> <span data-ttu-id="d60a6-123">以下是 swizzle 後的 *src* 對應：</span><span class="sxs-lookup"><span data-stu-id="d60a6-123">The following *src* mappings are post-swizzle:</span></span>

-   <span data-ttu-id="d60a6-124">*src0* 是跨 (x 32LSB、y 32MSB) 和 (z 32LSB、w 32MSB) 的雙重 vec2。</span><span class="sxs-lookup"><span data-stu-id="d60a6-124">*src0* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>
-   <span data-ttu-id="d60a6-125">*src1* 是跨 (x 32LSB、y 32MSB) 和 (z 32LSB、w 32MSB) 的雙重 vec2。</span><span class="sxs-lookup"><span data-stu-id="d60a6-125">*src1* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>

<span data-ttu-id="d60a6-126">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="d60a6-126">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="d60a6-127">頂點</span><span class="sxs-lookup"><span data-stu-id="d60a6-127">Vertex</span></span> | <span data-ttu-id="d60a6-128">船體</span><span class="sxs-lookup"><span data-stu-id="d60a6-128">Hull</span></span> | <span data-ttu-id="d60a6-129">網域</span><span class="sxs-lookup"><span data-stu-id="d60a6-129">Domain</span></span> | <span data-ttu-id="d60a6-130">幾何</span><span class="sxs-lookup"><span data-stu-id="d60a6-130">Geometry</span></span> | <span data-ttu-id="d60a6-131">像素</span><span class="sxs-lookup"><span data-stu-id="d60a6-131">Pixel</span></span> | <span data-ttu-id="d60a6-132">計算</span><span class="sxs-lookup"><span data-stu-id="d60a6-132">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="d60a6-133">X</span><span class="sxs-lookup"><span data-stu-id="d60a6-133">X</span></span>      | <span data-ttu-id="d60a6-134">X</span><span class="sxs-lookup"><span data-stu-id="d60a6-134">X</span></span>    | <span data-ttu-id="d60a6-135">X</span><span class="sxs-lookup"><span data-stu-id="d60a6-135">X</span></span>      | <span data-ttu-id="d60a6-136">X</span><span class="sxs-lookup"><span data-stu-id="d60a6-136">X</span></span>        | <span data-ttu-id="d60a6-137">X</span><span class="sxs-lookup"><span data-stu-id="d60a6-137">X</span></span>     | <span data-ttu-id="d60a6-138">X</span><span class="sxs-lookup"><span data-stu-id="d60a6-138">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="d60a6-139">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="d60a6-139">Minimum Shader Model</span></span>

<span data-ttu-id="d60a6-140">下列著色器模型支援此指令：</span><span class="sxs-lookup"><span data-stu-id="d60a6-140">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="d60a6-141">著色器模型</span><span class="sxs-lookup"><span data-stu-id="d60a6-141">Shader Model</span></span>                                              | <span data-ttu-id="d60a6-142">支援</span><span class="sxs-lookup"><span data-stu-id="d60a6-142">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="d60a6-143">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="d60a6-143">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="d60a6-144">是</span><span class="sxs-lookup"><span data-stu-id="d60a6-144">yes</span></span>       |
| [<span data-ttu-id="d60a6-145">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="d60a6-145">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="d60a6-146">不可以</span><span class="sxs-lookup"><span data-stu-id="d60a6-146">no</span></span>        |
| [<span data-ttu-id="d60a6-147">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="d60a6-147">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="d60a6-148">不可以</span><span class="sxs-lookup"><span data-stu-id="d60a6-148">no</span></span>        |
| [<span data-ttu-id="d60a6-149">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="d60a6-149">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="d60a6-150">不可以</span><span class="sxs-lookup"><span data-stu-id="d60a6-150">no</span></span>        |
| [<span data-ttu-id="d60a6-151">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="d60a6-151">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="d60a6-152">不可以</span><span class="sxs-lookup"><span data-stu-id="d60a6-152">no</span></span>        |
| [<span data-ttu-id="d60a6-153">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="d60a6-153">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="d60a6-154">不可以</span><span class="sxs-lookup"><span data-stu-id="d60a6-154">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="d60a6-155">相關主題</span><span class="sxs-lookup"><span data-stu-id="d60a6-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d60a6-156">著色器模型5元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="d60a6-156">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





