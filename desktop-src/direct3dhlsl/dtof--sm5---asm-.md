---
title: 'dtof (sm5-asm) '
description: 從雙精確度浮點數轉換成單精確度浮點數據的元件取向轉換。
ms.assetid: 1D2EF05C-06EF-44F0-AA0F-22D3057FF43E
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a66e72cf4c2cb1ac49adc492a586b4cbb9eef3b4
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104313628"
---
# <a name="dtof-sm5---asm"></a><span data-ttu-id="34ce6-103">dtof (sm5-asm) </span><span class="sxs-lookup"><span data-stu-id="34ce6-103">dtof (sm5 - asm)</span></span>

<span data-ttu-id="34ce6-104">從雙精確度浮點數轉換成單精確度浮點數據的元件取向轉換。</span><span class="sxs-lookup"><span data-stu-id="34ce6-104">Component-wise conversion from double-precision floating-point data to single-precision floating-point data.</span></span>



| <span data-ttu-id="34ce6-105">dtof dest \[ . mask \] 、 \[ - \] src \[ . swizzle \] 、</span><span class="sxs-lookup"><span data-stu-id="34ce6-105">dtof dest\[.mask\], \[-\]src\[.swizzle\],</span></span> |
|-------------------------------------------|



 



| <span data-ttu-id="34ce6-106">項目</span><span class="sxs-lookup"><span data-stu-id="34ce6-106">Item</span></span>                                                            | <span data-ttu-id="34ce6-107">描述</span><span class="sxs-lookup"><span data-stu-id="34ce6-107">Description</span></span>                                          |
|-----------------------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="34ce6-108"><span id="dest"></span><span id="DEST"></span>*目標*</span><span class="sxs-lookup"><span data-stu-id="34ce6-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="34ce6-109">\[已 \] 轉換資料的位址。</span><span class="sxs-lookup"><span data-stu-id="34ce6-109">\[in\] The address of the converted data.</span></span><br/> |
| <span data-ttu-id="34ce6-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="34ce6-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="34ce6-111">\[在 \] 要轉換的資料中。</span><span class="sxs-lookup"><span data-stu-id="34ce6-111">\[in\] The data to be converted.</span></span><br/>          |



 

## <a name="remarks"></a><span data-ttu-id="34ce6-112">備註</span><span class="sxs-lookup"><span data-stu-id="34ce6-112">Remarks</span></span>

<span data-ttu-id="34ce6-113">來源的每個元件都會使用四捨五入到最接近的舍入，從雙精確度表示轉換成單精確度標記法。</span><span class="sxs-lookup"><span data-stu-id="34ce6-113">Each component of the source is converted from the double-precision representation to the single-precision representation using round-to-nearest-even rounding.</span></span>

<span data-ttu-id="34ce6-114">來源參數的有效 swizzles 為. xyzw、. xyxy、. zwxy、. zwzw。</span><span class="sxs-lookup"><span data-stu-id="34ce6-114">The valid swizzles for the source parameter are .xyzw, .xyxy, .zwxy, .zwzw.</span></span>

<span data-ttu-id="34ce6-115">有效的 *目的地* 遮罩是任何一或兩個元件。</span><span class="sxs-lookup"><span data-stu-id="34ce6-115">The valid *dest* masks are any one or two components.</span></span> <span data-ttu-id="34ce6-116">亦即：. x、. y、. z、w、xy、. xw、. yz、. yw、. zw 第一個轉換的結果會移至遮罩中的第一個元件，而第二個元件的結果會移至遮罩中的第二個元件（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="34ce6-116">That is: .x, .y, .z, .w, .xy, .xz, .xw, .yz, .yw, .zw The result of the first conversion goes to the first component in the mask, and the result of the second component goes in the second component in the mask, if present.</span></span>

<span data-ttu-id="34ce6-117">*dest* 元件是 float32。</span><span class="sxs-lookup"><span data-stu-id="34ce6-117">*dest* components are float32.</span></span>

<span data-ttu-id="34ce6-118">*src* 是跨 (x 32LSB、y 32MSB) 和 (z 32LSB、w 32MSB) post swizzle 的雙 vec2。</span><span class="sxs-lookup"><span data-stu-id="34ce6-118">*src* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB) post swizzle.</span></span>

<span data-ttu-id="34ce6-119">針對 float32<->雙精度浮點數轉換，執行可能會接受 denorms 或清除它們。</span><span class="sxs-lookup"><span data-stu-id="34ce6-119">For float32<->double conversions, implementations may either honor float32 denorms or may flush them.</span></span>

<span data-ttu-id="34ce6-120">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="34ce6-120">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="34ce6-121">頂點</span><span class="sxs-lookup"><span data-stu-id="34ce6-121">Vertex</span></span> | <span data-ttu-id="34ce6-122">船體</span><span class="sxs-lookup"><span data-stu-id="34ce6-122">Hull</span></span> | <span data-ttu-id="34ce6-123">網域</span><span class="sxs-lookup"><span data-stu-id="34ce6-123">Domain</span></span> | <span data-ttu-id="34ce6-124">幾何</span><span class="sxs-lookup"><span data-stu-id="34ce6-124">Geometry</span></span> | <span data-ttu-id="34ce6-125">像素</span><span class="sxs-lookup"><span data-stu-id="34ce6-125">Pixel</span></span> | <span data-ttu-id="34ce6-126">計算</span><span class="sxs-lookup"><span data-stu-id="34ce6-126">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="34ce6-127">X</span><span class="sxs-lookup"><span data-stu-id="34ce6-127">X</span></span>      | <span data-ttu-id="34ce6-128">X</span><span class="sxs-lookup"><span data-stu-id="34ce6-128">X</span></span>    | <span data-ttu-id="34ce6-129">X</span><span class="sxs-lookup"><span data-stu-id="34ce6-129">X</span></span>      | <span data-ttu-id="34ce6-130">X</span><span class="sxs-lookup"><span data-stu-id="34ce6-130">X</span></span>        | <span data-ttu-id="34ce6-131">X</span><span class="sxs-lookup"><span data-stu-id="34ce6-131">X</span></span>     | <span data-ttu-id="34ce6-132">X</span><span class="sxs-lookup"><span data-stu-id="34ce6-132">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="34ce6-133">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="34ce6-133">Minimum Shader Model</span></span>

<span data-ttu-id="34ce6-134">下列著色器模型支援此指令：</span><span class="sxs-lookup"><span data-stu-id="34ce6-134">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="34ce6-135">著色器模型</span><span class="sxs-lookup"><span data-stu-id="34ce6-135">Shader Model</span></span>                                              | <span data-ttu-id="34ce6-136">支援</span><span class="sxs-lookup"><span data-stu-id="34ce6-136">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="34ce6-137">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="34ce6-137">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="34ce6-138">是</span><span class="sxs-lookup"><span data-stu-id="34ce6-138">yes</span></span>       |
| [<span data-ttu-id="34ce6-139">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="34ce6-139">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="34ce6-140">不可以</span><span class="sxs-lookup"><span data-stu-id="34ce6-140">no</span></span>        |
| [<span data-ttu-id="34ce6-141">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="34ce6-141">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="34ce6-142">不可以</span><span class="sxs-lookup"><span data-stu-id="34ce6-142">no</span></span>        |
| [<span data-ttu-id="34ce6-143">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="34ce6-143">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="34ce6-144">不可以</span><span class="sxs-lookup"><span data-stu-id="34ce6-144">no</span></span>        |
| [<span data-ttu-id="34ce6-145">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="34ce6-145">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="34ce6-146">不可以</span><span class="sxs-lookup"><span data-stu-id="34ce6-146">no</span></span>        |
| [<span data-ttu-id="34ce6-147">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="34ce6-147">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="34ce6-148">不可以</span><span class="sxs-lookup"><span data-stu-id="34ce6-148">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="34ce6-149">相關主題</span><span class="sxs-lookup"><span data-stu-id="34ce6-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="34ce6-150">著色器模型5元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="34ce6-150">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





