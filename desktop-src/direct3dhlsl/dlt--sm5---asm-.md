---
title: 'dlt (sm5-asm) '
description: 元件的雙精確度雙精確度小於比較。
ms.assetid: A9DE5007-4ADD-403D-A2B7-EAE475E9DCCB
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88fd45ebde621ed2c5f5aafc013741d6ee34c318
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104971553"
---
# <a name="dlt-sm5---asm"></a><span data-ttu-id="1e453-103">dlt (sm5-asm) </span><span class="sxs-lookup"><span data-stu-id="1e453-103">dlt (sm5 - asm)</span></span>

<span data-ttu-id="1e453-104">元件的雙精確度雙精確度小於比較。</span><span class="sxs-lookup"><span data-stu-id="1e453-104">Component-wise double-precision less-than comparison.</span></span>



| <span data-ttu-id="1e453-105">dlt \[ \_ sat \] dest \[ . mask \] 、 \[ - \] src0 \[ \_ abs \] \[ . swizzle \] 、 \[ - \] src1 \[ \_ abs \] \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="1e453-105">dlt\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\]</span></span> |
|--------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="1e453-106">項目</span><span class="sxs-lookup"><span data-stu-id="1e453-106">Item</span></span>                                                            | <span data-ttu-id="1e453-107">描述</span><span class="sxs-lookup"><span data-stu-id="1e453-107">Description</span></span>                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="1e453-108"><span id="dest"></span><span id="DEST"></span>*目標*</span><span class="sxs-lookup"><span data-stu-id="1e453-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="1e453-109">\[在 \] 操作結果的位址中。</span><span class="sxs-lookup"><span data-stu-id="1e453-109">\[in\] The address of the results of the operation.</span></span><br/> |
| <span data-ttu-id="1e453-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="1e453-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="1e453-111">\[在 \] [要與 *src1* 比較的元件] 中。</span><span class="sxs-lookup"><span data-stu-id="1e453-111">\[in\] The components to compare to *src1*.</span></span><br/>         |
| <span data-ttu-id="1e453-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="1e453-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="1e453-113">\[在 \] [要與 *src0* 比較的元件] 中。</span><span class="sxs-lookup"><span data-stu-id="1e453-113">\[in\] The components to compare to *src0*.</span></span><br/>         |



 

## <a name="remarks"></a><span data-ttu-id="1e453-114">備註</span><span class="sxs-lookup"><span data-stu-id="1e453-114">Remarks</span></span>

<span data-ttu-id="1e453-115">此指令會針對每個元件執行雙精確度浮點數比較 (*src0*  <  *src1*) ，並將結果寫入至 *目的地*。</span><span class="sxs-lookup"><span data-stu-id="1e453-115">This instruction performs the double-precision floating-point comparison (*src0* < *src1*) for each component and writes the result to *dest*.</span></span>

<span data-ttu-id="1e453-116">如果比較結果為 true，則會傳回該元件的32位0xFFFFFFFF。</span><span class="sxs-lookup"><span data-stu-id="1e453-116">If the comparison is true, then 32-bit 0xFFFFFFFF is returned for that component.</span></span> <span data-ttu-id="1e453-117">否則會傳回32位0x00000000。</span><span class="sxs-lookup"><span data-stu-id="1e453-117">Otherwise 32-bit 0x00000000 is returned.</span></span>

<span data-ttu-id="1e453-118">與 NaN 的比較會傳回 false。</span><span class="sxs-lookup"><span data-stu-id="1e453-118">Comparison with NaN returns false.</span></span>

<span data-ttu-id="1e453-119">有效的 *目的地* 遮罩是任何一或兩個元件。</span><span class="sxs-lookup"><span data-stu-id="1e453-119">The valid *dest* masks are any one or two components.</span></span> <span data-ttu-id="1e453-120">亦即：. x、. y、. z、w、xy、xw、. yz、. yw、. zw 遮罩中的第一個 *目的地* 元件會收到第一個雙重比較的32位結果。</span><span class="sxs-lookup"><span data-stu-id="1e453-120">That is: .x, .y, .z, .w, .xy, .xz, .xw, .yz, .yw, .zw The first *dest* component in the mask receives the 32-bit result for the first double comparison.</span></span> <span data-ttu-id="1e453-121">遮罩 (中的第二個元件（如果有) 的話）會接收第二個雙重比較的32位結果。</span><span class="sxs-lookup"><span data-stu-id="1e453-121">The second component in the mask (if present) receives the 32-bit result for the second double comparison.</span></span>

<span data-ttu-id="1e453-122">來源參數的有效 swizzles 為. xyzw、. xyxy、. zwxy、. zwzw。</span><span class="sxs-lookup"><span data-stu-id="1e453-122">The valid swizzles for the source parameters are .xyzw, .xyxy, .zwxy, .zwzw.</span></span> <span data-ttu-id="1e453-123">以下是 swizzle 後的 *src* 對應：</span><span class="sxs-lookup"><span data-stu-id="1e453-123">The following *src* mappings are post-swizzle:</span></span>

-   <span data-ttu-id="1e453-124">*src0* 是跨 (x 32LSB、y 32MSB) 和 (z 32LSB、w 32MSB) 的雙重 vec2。</span><span class="sxs-lookup"><span data-stu-id="1e453-124">*src0* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>
-   <span data-ttu-id="1e453-125">*src1* 是跨 (x 32LSB、y 32MSB) 和 (z 32LSB、w 32MSB) 的雙重 vec2。</span><span class="sxs-lookup"><span data-stu-id="1e453-125">*src1* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>

<span data-ttu-id="1e453-126">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="1e453-126">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="1e453-127">頂點</span><span class="sxs-lookup"><span data-stu-id="1e453-127">Vertex</span></span> | <span data-ttu-id="1e453-128">船體</span><span class="sxs-lookup"><span data-stu-id="1e453-128">Hull</span></span> | <span data-ttu-id="1e453-129">網域</span><span class="sxs-lookup"><span data-stu-id="1e453-129">Domain</span></span> | <span data-ttu-id="1e453-130">幾何</span><span class="sxs-lookup"><span data-stu-id="1e453-130">Geometry</span></span> | <span data-ttu-id="1e453-131">像素</span><span class="sxs-lookup"><span data-stu-id="1e453-131">Pixel</span></span> | <span data-ttu-id="1e453-132">計算</span><span class="sxs-lookup"><span data-stu-id="1e453-132">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="1e453-133">X</span><span class="sxs-lookup"><span data-stu-id="1e453-133">X</span></span>      | <span data-ttu-id="1e453-134">X</span><span class="sxs-lookup"><span data-stu-id="1e453-134">X</span></span>    | <span data-ttu-id="1e453-135">X</span><span class="sxs-lookup"><span data-stu-id="1e453-135">X</span></span>      | <span data-ttu-id="1e453-136">X</span><span class="sxs-lookup"><span data-stu-id="1e453-136">X</span></span>        | <span data-ttu-id="1e453-137">X</span><span class="sxs-lookup"><span data-stu-id="1e453-137">X</span></span>     | <span data-ttu-id="1e453-138">X</span><span class="sxs-lookup"><span data-stu-id="1e453-138">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="1e453-139">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="1e453-139">Minimum Shader Model</span></span>

<span data-ttu-id="1e453-140">下列著色器模型支援此指令：</span><span class="sxs-lookup"><span data-stu-id="1e453-140">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="1e453-141">著色器模型</span><span class="sxs-lookup"><span data-stu-id="1e453-141">Shader Model</span></span>                                              | <span data-ttu-id="1e453-142">支援</span><span class="sxs-lookup"><span data-stu-id="1e453-142">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="1e453-143">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="1e453-143">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="1e453-144">是</span><span class="sxs-lookup"><span data-stu-id="1e453-144">yes</span></span>       |
| [<span data-ttu-id="1e453-145">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="1e453-145">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="1e453-146">不可以</span><span class="sxs-lookup"><span data-stu-id="1e453-146">no</span></span>        |
| [<span data-ttu-id="1e453-147">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="1e453-147">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="1e453-148">不可以</span><span class="sxs-lookup"><span data-stu-id="1e453-148">no</span></span>        |
| [<span data-ttu-id="1e453-149">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="1e453-149">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="1e453-150">不可以</span><span class="sxs-lookup"><span data-stu-id="1e453-150">no</span></span>        |
| [<span data-ttu-id="1e453-151">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="1e453-151">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="1e453-152">不可以</span><span class="sxs-lookup"><span data-stu-id="1e453-152">no</span></span>        |
| [<span data-ttu-id="1e453-153">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="1e453-153">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="1e453-154">不可以</span><span class="sxs-lookup"><span data-stu-id="1e453-154">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="1e453-155">相關主題</span><span class="sxs-lookup"><span data-stu-id="1e453-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1e453-156">著色器模型5元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="1e453-156">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





