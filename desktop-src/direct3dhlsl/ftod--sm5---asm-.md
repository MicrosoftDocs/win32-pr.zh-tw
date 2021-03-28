---
title: 'ftod (sm5-asm) '
description: 從單精確度浮點數到雙精確度浮點數據的元件取向轉換。
ms.assetid: 95297556-41ED-4ED0-8F9A-16B7A440AF25
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6790735745805426d32aefcc5d5d771ade644e43
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104313706"
---
# <a name="ftod-sm5---asm"></a><span data-ttu-id="d080e-103">ftod (sm5-asm) </span><span class="sxs-lookup"><span data-stu-id="d080e-103">ftod (sm5 - asm)</span></span>

<span data-ttu-id="d080e-104">從單精確度浮點數到雙精確度浮點數據的元件取向轉換。</span><span class="sxs-lookup"><span data-stu-id="d080e-104">Component-wise conversion from single-precision floating-point data to double-precision floating-point data.</span></span>



| <span data-ttu-id="d080e-105">ftod dest \[ . mask \] 、 \[ - \] src \[ . swizzle \] 、</span><span class="sxs-lookup"><span data-stu-id="d080e-105">ftod dest\[.mask\], \[-\]src\[.swizzle\],</span></span> |
|-------------------------------------------|



 



| <span data-ttu-id="d080e-106">項目</span><span class="sxs-lookup"><span data-stu-id="d080e-106">Item</span></span>                                                            | <span data-ttu-id="d080e-107">描述</span><span class="sxs-lookup"><span data-stu-id="d080e-107">Description</span></span>                                          |
|-----------------------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d080e-108"><span id="dest"></span><span id="DEST"></span>*目標*</span><span class="sxs-lookup"><span data-stu-id="d080e-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="d080e-109">\[已 \] 轉換資料的位址。</span><span class="sxs-lookup"><span data-stu-id="d080e-109">\[in\] The address of the converted data.</span></span><br/> |
| <span data-ttu-id="d080e-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="d080e-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="d080e-111">\[在 \] 要轉換的資料中。</span><span class="sxs-lookup"><span data-stu-id="d080e-111">\[in\] The data to be converted.</span></span><br/>          |



 

## <a name="remarks"></a><span data-ttu-id="d080e-112">備註</span><span class="sxs-lookup"><span data-stu-id="d080e-112">Remarks</span></span>

<span data-ttu-id="d080e-113">來源的每個元件都會從單精確度表示轉換為雙精確度標記法。</span><span class="sxs-lookup"><span data-stu-id="d080e-113">Each component of the source is converted from the single-precision representation to the double-precision representation.</span></span>

<span data-ttu-id="d080e-114">有效的 *目的地* 遮罩是 xy、. zw 和. xyzw。</span><span class="sxs-lookup"><span data-stu-id="d080e-114">The valid *dest* masks are .xy, .zw, and .xyzw.</span></span> <span data-ttu-id="d080e-115">xy 接收第一個轉換的結果，而. zw 會接收第二個轉換的結果。</span><span class="sxs-lookup"><span data-stu-id="d080e-115">.xy receives the result of the first conversion, and .zw receives the result of the second conversion.</span></span>

<span data-ttu-id="d080e-116">*dest* 是跨 (x 32LSB、y 32MSB) 和 (z 32LSB、w 32MSB) 的雙 vec2。</span><span class="sxs-lookup"><span data-stu-id="d080e-116">*dest* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>

<span data-ttu-id="d080e-117">*src* 是跨 x 和 y 的 float vec2 (zw 會) 忽略 (swizzle 後) 。</span><span class="sxs-lookup"><span data-stu-id="d080e-117">*src* is a float vec2 across x and y (zw ignored) (post swizzle).</span></span>

<span data-ttu-id="d080e-118">針對 float32<->雙精度浮點數轉換，執行可能會接受 denorms 或清除它們。</span><span class="sxs-lookup"><span data-stu-id="d080e-118">For float32<->double conversions, implementations may either honor float32 denorms or may flush them.</span></span>

<span data-ttu-id="d080e-119">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="d080e-119">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="d080e-120">頂點</span><span class="sxs-lookup"><span data-stu-id="d080e-120">Vertex</span></span> | <span data-ttu-id="d080e-121">船體</span><span class="sxs-lookup"><span data-stu-id="d080e-121">Hull</span></span> | <span data-ttu-id="d080e-122">網域</span><span class="sxs-lookup"><span data-stu-id="d080e-122">Domain</span></span> | <span data-ttu-id="d080e-123">幾何</span><span class="sxs-lookup"><span data-stu-id="d080e-123">Geometry</span></span> | <span data-ttu-id="d080e-124">像素</span><span class="sxs-lookup"><span data-stu-id="d080e-124">Pixel</span></span> | <span data-ttu-id="d080e-125">計算</span><span class="sxs-lookup"><span data-stu-id="d080e-125">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="d080e-126">X</span><span class="sxs-lookup"><span data-stu-id="d080e-126">X</span></span>      | <span data-ttu-id="d080e-127">X</span><span class="sxs-lookup"><span data-stu-id="d080e-127">X</span></span>    | <span data-ttu-id="d080e-128">X</span><span class="sxs-lookup"><span data-stu-id="d080e-128">X</span></span>      | <span data-ttu-id="d080e-129">X</span><span class="sxs-lookup"><span data-stu-id="d080e-129">X</span></span>        | <span data-ttu-id="d080e-130">X</span><span class="sxs-lookup"><span data-stu-id="d080e-130">X</span></span>     | <span data-ttu-id="d080e-131">X</span><span class="sxs-lookup"><span data-stu-id="d080e-131">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="d080e-132">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="d080e-132">Minimum Shader Model</span></span>

<span data-ttu-id="d080e-133">下列著色器模型支援此指令：</span><span class="sxs-lookup"><span data-stu-id="d080e-133">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="d080e-134">著色器模型</span><span class="sxs-lookup"><span data-stu-id="d080e-134">Shader Model</span></span>                                              | <span data-ttu-id="d080e-135">支援</span><span class="sxs-lookup"><span data-stu-id="d080e-135">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="d080e-136">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="d080e-136">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="d080e-137">是</span><span class="sxs-lookup"><span data-stu-id="d080e-137">yes</span></span>       |
| [<span data-ttu-id="d080e-138">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="d080e-138">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="d080e-139">不可以</span><span class="sxs-lookup"><span data-stu-id="d080e-139">no</span></span>        |
| [<span data-ttu-id="d080e-140">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="d080e-140">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="d080e-141">不可以</span><span class="sxs-lookup"><span data-stu-id="d080e-141">no</span></span>        |
| [<span data-ttu-id="d080e-142">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="d080e-142">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="d080e-143">不可以</span><span class="sxs-lookup"><span data-stu-id="d080e-143">no</span></span>        |
| [<span data-ttu-id="d080e-144">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="d080e-144">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="d080e-145">不可以</span><span class="sxs-lookup"><span data-stu-id="d080e-145">no</span></span>        |
| [<span data-ttu-id="d080e-146">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="d080e-146">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="d080e-147">不可以</span><span class="sxs-lookup"><span data-stu-id="d080e-147">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="d080e-148">相關主題</span><span class="sxs-lookup"><span data-stu-id="d080e-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d080e-149">著色器模型5元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="d080e-149">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





