---
title: 'dmin (sm5-asm) '
description: 元件的雙精確度最小值。
ms.assetid: 77331B4D-C4B5-49B2-BB6A-77BD5050B575
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e199b01c68acca6609123425438f309af872fb4
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104022824"
---
# <a name="dmin-sm5---asm"></a><span data-ttu-id="9a150-103">dmin (sm5-asm) </span><span class="sxs-lookup"><span data-stu-id="9a150-103">dmin (sm5 - asm)</span></span>

<span data-ttu-id="9a150-104">元件的雙精確度最小值。</span><span class="sxs-lookup"><span data-stu-id="9a150-104">Component-wise double-precision minimum.</span></span>



| <span data-ttu-id="9a150-105">dmin \[ \_ sat \] dest \[ . mask \] 、 \[ - \] src0 \[ \_ abs \] \[ . swizzle \] 、 \[ - \] src1 \[ \_ abs \] \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="9a150-105">dmin\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\]</span></span> |
|---------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="9a150-106">項目</span><span class="sxs-lookup"><span data-stu-id="9a150-106">Item</span></span>                                                            | <span data-ttu-id="9a150-107">描述</span><span class="sxs-lookup"><span data-stu-id="9a150-107">Description</span></span>                                                                                                                                                                                                  |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a150-108"><span id="dest"></span><span id="DEST"></span>*目標*</span><span class="sxs-lookup"><span data-stu-id="9a150-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="9a150-109">\[在 \] 操作結果的位址中。</span><span class="sxs-lookup"><span data-stu-id="9a150-109">\[in\] The address of the results of the operation.</span></span><br/> <span data-ttu-id="9a150-110">*目的地*  = *src0*  < *src1* 嗎？</span><span class="sxs-lookup"><span data-stu-id="9a150-110">*dest* = *src0* < *src1* ?</span></span> <span data-ttu-id="9a150-111">*src0* ： *src1*</span><span class="sxs-lookup"><span data-stu-id="9a150-111">*src0* : *src1*</span></span><br/> <span data-ttu-id="9a150-112">< 是用來取代 <=，因此，如果 min (x，y) = x， (x，y) = y。</span><span class="sxs-lookup"><span data-stu-id="9a150-112">< is used instead of <= so that if min(x,y) = x then max(x,y) = y.</span></span> <br/> |
| <span data-ttu-id="9a150-113"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="9a150-113"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="9a150-114">\[在 \] 要與 *src1* 比較的元件中。</span><span class="sxs-lookup"><span data-stu-id="9a150-114">\[in\] The components to compare with *src1*.</span></span><br/>                                                                                                                                                     |
| <span data-ttu-id="9a150-115"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="9a150-115"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="9a150-116">\[在 \] 要與 *src0* 比較的元件中。</span><span class="sxs-lookup"><span data-stu-id="9a150-116">\[in\] The components to compare with *src0*.</span></span><br/>                                                                                                                                                     |



 

## <a name="remarks"></a><span data-ttu-id="9a150-117">備註</span><span class="sxs-lookup"><span data-stu-id="9a150-117">Remarks</span></span>

<span data-ttu-id="9a150-118">NaN 具有特殊處理。</span><span class="sxs-lookup"><span data-stu-id="9a150-118">NaN has special handling.</span></span> <span data-ttu-id="9a150-119">如果一個來源運算元為 NaN，則會傳回另一個來源運算元。</span><span class="sxs-lookup"><span data-stu-id="9a150-119">If one source operand is NaN, then the other source operand is returned.</span></span> <span data-ttu-id="9a150-120">選擇是依元件進行。</span><span class="sxs-lookup"><span data-stu-id="9a150-120">The choice is made per-component.</span></span> <span data-ttu-id="9a150-121">如果兩者都是 NaN，則會傳回任何 NaN 表示。</span><span class="sxs-lookup"><span data-stu-id="9a150-121">If both are NaN, any NaN representation is returned.</span></span>

<span data-ttu-id="9a150-122">來源參數的有效 swizzles 為. xyzw、. xyxy、. zwxy、. zwzw。</span><span class="sxs-lookup"><span data-stu-id="9a150-122">The valid swizzles for the source parameters are .xyzw, .xyxy, .zwxy, .zwzw.</span></span> <span data-ttu-id="9a150-123">有效的 *目的地* 遮罩是 xy、. zw 和. xyzw。</span><span class="sxs-lookup"><span data-stu-id="9a150-123">The valid *dest* masks are .xy, .zw, and .xyzw.</span></span> <span data-ttu-id="9a150-124">以下是 swizzle 後的 *src* 對應：</span><span class="sxs-lookup"><span data-stu-id="9a150-124">The following *src* mappings are post-swizzle:</span></span>

-   <span data-ttu-id="9a150-125">*dest* 是跨 (x 32LSB、y 32MSB) 和 (z 32LSB、w 32MSB) 的雙 vec2。</span><span class="sxs-lookup"><span data-stu-id="9a150-125">*dest* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>
-   <span data-ttu-id="9a150-126">*src0* 是跨 (x 32LSB、y 32MSB) 和 (z 32LSB、w 32MSB) 的雙重 vec2。</span><span class="sxs-lookup"><span data-stu-id="9a150-126">*src0* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>
-   <span data-ttu-id="9a150-127">*src1* 是跨 (x 32LSB、y 32MSB) 和 (z 32LSB、w 32MSB) 的雙重 vec2。</span><span class="sxs-lookup"><span data-stu-id="9a150-127">*src1* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>

<span data-ttu-id="9a150-128">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="9a150-128">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="9a150-129">頂點</span><span class="sxs-lookup"><span data-stu-id="9a150-129">Vertex</span></span> | <span data-ttu-id="9a150-130">船體</span><span class="sxs-lookup"><span data-stu-id="9a150-130">Hull</span></span> | <span data-ttu-id="9a150-131">網域</span><span class="sxs-lookup"><span data-stu-id="9a150-131">Domain</span></span> | <span data-ttu-id="9a150-132">幾何</span><span class="sxs-lookup"><span data-stu-id="9a150-132">Geometry</span></span> | <span data-ttu-id="9a150-133">像素</span><span class="sxs-lookup"><span data-stu-id="9a150-133">Pixel</span></span> | <span data-ttu-id="9a150-134">計算</span><span class="sxs-lookup"><span data-stu-id="9a150-134">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="9a150-135">X</span><span class="sxs-lookup"><span data-stu-id="9a150-135">X</span></span>      | <span data-ttu-id="9a150-136">X</span><span class="sxs-lookup"><span data-stu-id="9a150-136">X</span></span>    | <span data-ttu-id="9a150-137">X</span><span class="sxs-lookup"><span data-stu-id="9a150-137">X</span></span>      | <span data-ttu-id="9a150-138">X</span><span class="sxs-lookup"><span data-stu-id="9a150-138">X</span></span>        | <span data-ttu-id="9a150-139">X</span><span class="sxs-lookup"><span data-stu-id="9a150-139">X</span></span>     | <span data-ttu-id="9a150-140">X</span><span class="sxs-lookup"><span data-stu-id="9a150-140">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="9a150-141">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="9a150-141">Minimum Shader Model</span></span>

<span data-ttu-id="9a150-142">下列著色器模型支援此指令：</span><span class="sxs-lookup"><span data-stu-id="9a150-142">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="9a150-143">著色器模型</span><span class="sxs-lookup"><span data-stu-id="9a150-143">Shader Model</span></span>                                              | <span data-ttu-id="9a150-144">支援</span><span class="sxs-lookup"><span data-stu-id="9a150-144">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="9a150-145">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="9a150-145">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="9a150-146">是</span><span class="sxs-lookup"><span data-stu-id="9a150-146">yes</span></span>       |
| [<span data-ttu-id="9a150-147">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="9a150-147">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="9a150-148">不可以</span><span class="sxs-lookup"><span data-stu-id="9a150-148">no</span></span>        |
| [<span data-ttu-id="9a150-149">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="9a150-149">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="9a150-150">不可以</span><span class="sxs-lookup"><span data-stu-id="9a150-150">no</span></span>        |
| [<span data-ttu-id="9a150-151">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="9a150-151">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="9a150-152">不可以</span><span class="sxs-lookup"><span data-stu-id="9a150-152">no</span></span>        |
| [<span data-ttu-id="9a150-153">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="9a150-153">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="9a150-154">不可以</span><span class="sxs-lookup"><span data-stu-id="9a150-154">no</span></span>        |
| [<span data-ttu-id="9a150-155">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="9a150-155">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="9a150-156">不可以</span><span class="sxs-lookup"><span data-stu-id="9a150-156">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="9a150-157">相關主題</span><span class="sxs-lookup"><span data-stu-id="9a150-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9a150-158">著色器模型5元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="9a150-158">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





