---
title: 'dmax (sm5-asm) '
description: 元件的雙精確度最大值。
ms.assetid: 34ED8B34-2592-4BBB-BCF0-F2222E4D51D9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 703b277a98b16570de6f5ab7e0e7643ddfdcc705
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104373739"
---
# <a name="dmax-sm5---asm"></a><span data-ttu-id="a1aa9-103">dmax (sm5-asm) </span><span class="sxs-lookup"><span data-stu-id="a1aa9-103">dmax (sm5 - asm)</span></span>

<span data-ttu-id="a1aa9-104">元件的雙精確度最大值。</span><span class="sxs-lookup"><span data-stu-id="a1aa9-104">Component-wise double-precision maximum.</span></span>



| <span data-ttu-id="a1aa9-105">dmax \[ \_ sat \] dest \[ . mask \] 、 \[ - \] src0 \[ \_ abs \] \[ . swizzle \] 、 \[ - \] src1 \[ \_ abs \] \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="a1aa9-105">dmax\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\]</span></span> |
|---------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="a1aa9-106">項目</span><span class="sxs-lookup"><span data-stu-id="a1aa9-106">Item</span></span>                                                            | <span data-ttu-id="a1aa9-107">描述</span><span class="sxs-lookup"><span data-stu-id="a1aa9-107">Description</span></span>                                                                                                                                                                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1aa9-108"><span id="dest"></span><span id="DEST"></span>*目標*</span><span class="sxs-lookup"><span data-stu-id="a1aa9-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="a1aa9-109">\[在 \] 操作結果的位址中。</span><span class="sxs-lookup"><span data-stu-id="a1aa9-109">\[in\] The address of the results of the operation.</span></span><br/> <span data-ttu-id="a1aa9-110">*目的地*  = *src0*  >= *src1* 嗎？</span><span class="sxs-lookup"><span data-stu-id="a1aa9-110">*dest* = *src0* >= *src1* ?</span></span> <span data-ttu-id="a1aa9-111">*src0* ： *src1*</span><span class="sxs-lookup"><span data-stu-id="a1aa9-111">*src0* : *src1*</span></span><br/> <span data-ttu-id="a1aa9-112">>= 會用來取代 >，因此，如果 min (x，y) = x， (x，y) = y 的上限。</span><span class="sxs-lookup"><span data-stu-id="a1aa9-112">>= is used instead of > so that if min(x,y) = x then max(x,y) = y.</span></span> <br/> |
| <span data-ttu-id="a1aa9-113"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="a1aa9-113"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="a1aa9-114">\[在 \] [要與 *src1* 比較的值] 中。</span><span class="sxs-lookup"><span data-stu-id="a1aa9-114">\[in\] The value to compare with *src1*.</span></span><br/>                                                                                                                                                           |
| <span data-ttu-id="a1aa9-115"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="a1aa9-115"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="a1aa9-116">\[在 \] [要與 *src0* 比較的值] 中。</span><span class="sxs-lookup"><span data-stu-id="a1aa9-116">\[in\] The value to compare with *src0*.</span></span><br/>                                                                                                                                                           |



 

## <a name="remarks"></a><span data-ttu-id="a1aa9-117">備註</span><span class="sxs-lookup"><span data-stu-id="a1aa9-117">Remarks</span></span>

<span data-ttu-id="a1aa9-118">NaN 具有特殊處理。</span><span class="sxs-lookup"><span data-stu-id="a1aa9-118">NaN has special handling.</span></span> <span data-ttu-id="a1aa9-119">如果一個來源運算元為 NaN，則會傳回另一個來源運算元。</span><span class="sxs-lookup"><span data-stu-id="a1aa9-119">If one source operand is NaN, then the other source operand is returned.</span></span> <span data-ttu-id="a1aa9-120">選擇是依元件進行。</span><span class="sxs-lookup"><span data-stu-id="a1aa9-120">The choice is made per-component.</span></span> <span data-ttu-id="a1aa9-121">如果兩者都是 NaN，則會傳回任何 NaN 表示。</span><span class="sxs-lookup"><span data-stu-id="a1aa9-121">If both are NaN, any NaN representation is returned.</span></span>

<span data-ttu-id="a1aa9-122">來源參數的有效 swizzles 為. xyzw、. xyxy、. zwxy、. zwzw。</span><span class="sxs-lookup"><span data-stu-id="a1aa9-122">The valid swizzles for the source parameters are .xyzw, .xyxy, .zwxy, .zwzw.</span></span> <span data-ttu-id="a1aa9-123">有效的 *目的地* 遮罩是 xy、. zw 和. xyzw。</span><span class="sxs-lookup"><span data-stu-id="a1aa9-123">The valid *dest* masks are .xy, .zw, and .xyzw.</span></span> <span data-ttu-id="a1aa9-124">以下是 swizzle 後的 *src* 對應：</span><span class="sxs-lookup"><span data-stu-id="a1aa9-124">The following *src* mappings are post-swizzle:</span></span>

-   <span data-ttu-id="a1aa9-125">*dest* 是跨 (x 32LSB、y 32MSB) 和 (z 32LSB、w 32MSB) 的雙 vec2。</span><span class="sxs-lookup"><span data-stu-id="a1aa9-125">*dest* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>
-   <span data-ttu-id="a1aa9-126">*src0* 是跨 (x 32LSB、y 32MSB) 和 (z 32LSB、w 32MSB) 的雙重 vec2。</span><span class="sxs-lookup"><span data-stu-id="a1aa9-126">*src0* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>
-   <span data-ttu-id="a1aa9-127">*src1* 是跨 (x 32LSB、y 32MSB) 和 (z 32LSB、w 32MSB) 的雙重 vec2。</span><span class="sxs-lookup"><span data-stu-id="a1aa9-127">*src1* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>

<span data-ttu-id="a1aa9-128">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="a1aa9-128">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="a1aa9-129">頂點</span><span class="sxs-lookup"><span data-stu-id="a1aa9-129">Vertex</span></span> | <span data-ttu-id="a1aa9-130">船體</span><span class="sxs-lookup"><span data-stu-id="a1aa9-130">Hull</span></span> | <span data-ttu-id="a1aa9-131">網域</span><span class="sxs-lookup"><span data-stu-id="a1aa9-131">Domain</span></span> | <span data-ttu-id="a1aa9-132">幾何</span><span class="sxs-lookup"><span data-stu-id="a1aa9-132">Geometry</span></span> | <span data-ttu-id="a1aa9-133">像素</span><span class="sxs-lookup"><span data-stu-id="a1aa9-133">Pixel</span></span> | <span data-ttu-id="a1aa9-134">計算</span><span class="sxs-lookup"><span data-stu-id="a1aa9-134">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="a1aa9-135">X</span><span class="sxs-lookup"><span data-stu-id="a1aa9-135">X</span></span>      | <span data-ttu-id="a1aa9-136">X</span><span class="sxs-lookup"><span data-stu-id="a1aa9-136">X</span></span>    | <span data-ttu-id="a1aa9-137">X</span><span class="sxs-lookup"><span data-stu-id="a1aa9-137">X</span></span>      | <span data-ttu-id="a1aa9-138">X</span><span class="sxs-lookup"><span data-stu-id="a1aa9-138">X</span></span>        | <span data-ttu-id="a1aa9-139">X</span><span class="sxs-lookup"><span data-stu-id="a1aa9-139">X</span></span>     | <span data-ttu-id="a1aa9-140">X</span><span class="sxs-lookup"><span data-stu-id="a1aa9-140">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="a1aa9-141">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="a1aa9-141">Minimum Shader Model</span></span>

<span data-ttu-id="a1aa9-142">下列著色器模型支援此指令：</span><span class="sxs-lookup"><span data-stu-id="a1aa9-142">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="a1aa9-143">著色器模型</span><span class="sxs-lookup"><span data-stu-id="a1aa9-143">Shader Model</span></span>                                              | <span data-ttu-id="a1aa9-144">支援</span><span class="sxs-lookup"><span data-stu-id="a1aa9-144">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="a1aa9-145">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="a1aa9-145">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="a1aa9-146">是</span><span class="sxs-lookup"><span data-stu-id="a1aa9-146">yes</span></span>       |
| [<span data-ttu-id="a1aa9-147">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="a1aa9-147">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="a1aa9-148">不可以</span><span class="sxs-lookup"><span data-stu-id="a1aa9-148">no</span></span>        |
| [<span data-ttu-id="a1aa9-149">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="a1aa9-149">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="a1aa9-150">不可以</span><span class="sxs-lookup"><span data-stu-id="a1aa9-150">no</span></span>        |
| [<span data-ttu-id="a1aa9-151">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="a1aa9-151">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="a1aa9-152">不可以</span><span class="sxs-lookup"><span data-stu-id="a1aa9-152">no</span></span>        |
| [<span data-ttu-id="a1aa9-153">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="a1aa9-153">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="a1aa9-154">不可以</span><span class="sxs-lookup"><span data-stu-id="a1aa9-154">no</span></span>        |
| [<span data-ttu-id="a1aa9-155">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="a1aa9-155">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="a1aa9-156">不可以</span><span class="sxs-lookup"><span data-stu-id="a1aa9-156">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="a1aa9-157">相關主題</span><span class="sxs-lookup"><span data-stu-id="a1aa9-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a1aa9-158">著色器模型5元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="a1aa9-158">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





