---
title: 'dmov (sm5-asm) '
description: '元件取向的移動。 |dmov (sm5-asm) '
ms.assetid: 05DBB9E2-10EC-4324-BB8F-1A9E315DE90C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23b7d9c5ca0da1671ddf30fb9746333617f7688a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "103946022"
---
# <a name="dmov-sm5---asm"></a><span data-ttu-id="e881a-104">dmov (sm5-asm) </span><span class="sxs-lookup"><span data-stu-id="e881a-104">dmov (sm5 - asm)</span></span>

<span data-ttu-id="e881a-105">元件取向的移動。</span><span class="sxs-lookup"><span data-stu-id="e881a-105">Component-wise move.</span></span>



| <span data-ttu-id="e881a-106">dmov \[ \_ sat \] dest \[ . mask \] ， \[ - \] src0 \[ \_ abs \] \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="e881a-106">dmov\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|-------------------------------------------------------------|



 



| <span data-ttu-id="e881a-107">項目</span><span class="sxs-lookup"><span data-stu-id="e881a-107">Item</span></span>                                                            | <span data-ttu-id="e881a-108">描述</span><span class="sxs-lookup"><span data-stu-id="e881a-108">Description</span></span>                                              |
|-----------------------------------------------------------------|----------------------------------------------------------|
| <span data-ttu-id="e881a-109"><span id="dest"></span><span id="DEST"></span>*目標*</span><span class="sxs-lookup"><span data-stu-id="e881a-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="e881a-110">\[在 \] 移動目的地。</span><span class="sxs-lookup"><span data-stu-id="e881a-110">\[in\] The move destination.</span></span> <span data-ttu-id="e881a-111">*目的地*  = *src0*。</span><span class="sxs-lookup"><span data-stu-id="e881a-111">*dest* = *src0*.</span></span><br/> |
| <span data-ttu-id="e881a-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="e881a-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="e881a-113">\[在 \] 要移動的元件中。</span><span class="sxs-lookup"><span data-stu-id="e881a-113">\[in\] The components to be moved.</span></span><br/>            |



 

## <a name="remarks"></a><span data-ttu-id="e881a-114">備註</span><span class="sxs-lookup"><span data-stu-id="e881a-114">Remarks</span></span>

<span data-ttu-id="e881a-115">Swizzle 以外的修飾詞會假設資料是浮點。</span><span class="sxs-lookup"><span data-stu-id="e881a-115">The modifiers, other than swizzle, assume the data is floating point.</span></span> <span data-ttu-id="e881a-116">缺少修飾詞會移動資料，而不會改變位。</span><span class="sxs-lookup"><span data-stu-id="e881a-116">The absence of modifiers moves data without altering bits.</span></span>

<span data-ttu-id="e881a-117">來源參數的有效 swizzles 為. xyzw、. xyxy、. zwxy、. zwzw。</span><span class="sxs-lookup"><span data-stu-id="e881a-117">The valid swizzles for the source parameters are .xyzw, .xyxy, .zwxy, .zwzw.</span></span> <span data-ttu-id="e881a-118">以下是 swizzle 後的 *src* 對應：</span><span class="sxs-lookup"><span data-stu-id="e881a-118">The following *src* mappings are post-swizzle:</span></span>

-   <span data-ttu-id="e881a-119">*src0* 是跨 (x 32LSB、y 32MSB) 和 (z 32LSB、w 32MSB) 的雙重 vec2。</span><span class="sxs-lookup"><span data-stu-id="e881a-119">*src0* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>
-   <span data-ttu-id="e881a-120">*src1* 是跨 (x 32LSB、y 32MSB) 和 (z 32LSB、w 32MSB) 的雙重 vec2。</span><span class="sxs-lookup"><span data-stu-id="e881a-120">*src1* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>

<span data-ttu-id="e881a-121">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="e881a-121">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="e881a-122">頂點</span><span class="sxs-lookup"><span data-stu-id="e881a-122">Vertex</span></span> | <span data-ttu-id="e881a-123">船體</span><span class="sxs-lookup"><span data-stu-id="e881a-123">Hull</span></span> | <span data-ttu-id="e881a-124">網域</span><span class="sxs-lookup"><span data-stu-id="e881a-124">Domain</span></span> | <span data-ttu-id="e881a-125">幾何</span><span class="sxs-lookup"><span data-stu-id="e881a-125">Geometry</span></span> | <span data-ttu-id="e881a-126">像素</span><span class="sxs-lookup"><span data-stu-id="e881a-126">Pixel</span></span> | <span data-ttu-id="e881a-127">計算</span><span class="sxs-lookup"><span data-stu-id="e881a-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="e881a-128">X</span><span class="sxs-lookup"><span data-stu-id="e881a-128">X</span></span>      | <span data-ttu-id="e881a-129">X</span><span class="sxs-lookup"><span data-stu-id="e881a-129">X</span></span>    | <span data-ttu-id="e881a-130">X</span><span class="sxs-lookup"><span data-stu-id="e881a-130">X</span></span>      | <span data-ttu-id="e881a-131">X</span><span class="sxs-lookup"><span data-stu-id="e881a-131">X</span></span>        | <span data-ttu-id="e881a-132">X</span><span class="sxs-lookup"><span data-stu-id="e881a-132">X</span></span>     | <span data-ttu-id="e881a-133">X</span><span class="sxs-lookup"><span data-stu-id="e881a-133">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="e881a-134">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="e881a-134">Minimum Shader Model</span></span>

<span data-ttu-id="e881a-135">下列著色器模型支援此指令：</span><span class="sxs-lookup"><span data-stu-id="e881a-135">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="e881a-136">著色器模型</span><span class="sxs-lookup"><span data-stu-id="e881a-136">Shader Model</span></span>                                              | <span data-ttu-id="e881a-137">支援</span><span class="sxs-lookup"><span data-stu-id="e881a-137">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="e881a-138">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="e881a-138">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="e881a-139">是</span><span class="sxs-lookup"><span data-stu-id="e881a-139">yes</span></span>       |
| [<span data-ttu-id="e881a-140">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="e881a-140">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="e881a-141">不可以</span><span class="sxs-lookup"><span data-stu-id="e881a-141">no</span></span>        |
| [<span data-ttu-id="e881a-142">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="e881a-142">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="e881a-143">不可以</span><span class="sxs-lookup"><span data-stu-id="e881a-143">no</span></span>        |
| [<span data-ttu-id="e881a-144">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="e881a-144">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="e881a-145">不可以</span><span class="sxs-lookup"><span data-stu-id="e881a-145">no</span></span>        |
| [<span data-ttu-id="e881a-146">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="e881a-146">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="e881a-147">不可以</span><span class="sxs-lookup"><span data-stu-id="e881a-147">no</span></span>        |
| [<span data-ttu-id="e881a-148">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="e881a-148">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="e881a-149">不可以</span><span class="sxs-lookup"><span data-stu-id="e881a-149">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="e881a-150">相關主題</span><span class="sxs-lookup"><span data-stu-id="e881a-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e881a-151">著色器模型5元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="e881a-151">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





