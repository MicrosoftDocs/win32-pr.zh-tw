---
title: 'countbits (sm5-asm) '
description: 計算數位中設定的位數數目。
ms.assetid: ED75487F-46FF-45F5-BEAA-7A32BEFB0571
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55d46fe9c750790d65630a743dd9ddc347fea50e
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "103841660"
---
# <a name="countbits-sm5---asm"></a><span data-ttu-id="b990e-103">countbits (sm5-asm) </span><span class="sxs-lookup"><span data-stu-id="b990e-103">countbits (sm5 - asm)</span></span>

<span data-ttu-id="b990e-104">計算數位中設定的位數數目。</span><span class="sxs-lookup"><span data-stu-id="b990e-104">Counts the number of bits set in a number.</span></span>



| <span data-ttu-id="b990e-105">countbits dest \[ . mask \] ，src0 \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="b990e-105">countbits dest\[.mask\], src0\[.swizzle\]</span></span> |
|-------------------------------------------|



 



| <span data-ttu-id="b990e-106">項目</span><span class="sxs-lookup"><span data-stu-id="b990e-106">Item</span></span>                                                            | <span data-ttu-id="b990e-107">描述</span><span class="sxs-lookup"><span data-stu-id="b990e-107">Description</span></span>                                   |
|-----------------------------------------------------------------|-----------------------------------------------|
| <span data-ttu-id="b990e-108"><span id="dest"></span><span id="DEST"></span>*目標*</span><span class="sxs-lookup"><span data-stu-id="b990e-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="b990e-109">\[在 \] 結果的位址中。</span><span class="sxs-lookup"><span data-stu-id="b990e-109">\[in\] The address of the results.</span></span><br/> |
| <span data-ttu-id="b990e-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="b990e-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="b990e-111">\[在 \] 輸入32位數位中。</span><span class="sxs-lookup"><span data-stu-id="b990e-111">\[in\] The input 32-bit number.</span></span><br/>    |



 

## <a name="remarks"></a><span data-ttu-id="b990e-112">備註</span><span class="sxs-lookup"><span data-stu-id="b990e-112">Remarks</span></span>

<span data-ttu-id="b990e-113">此指令可以用來計算著色器輸入涵蓋範圍百分比。</span><span class="sxs-lookup"><span data-stu-id="b990e-113">This instruction can be used to compute shader input coverage percentage.</span></span>

<span data-ttu-id="b990e-114">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="b990e-114">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="b990e-115">頂點</span><span class="sxs-lookup"><span data-stu-id="b990e-115">Vertex</span></span> | <span data-ttu-id="b990e-116">船體</span><span class="sxs-lookup"><span data-stu-id="b990e-116">Hull</span></span> | <span data-ttu-id="b990e-117">網域</span><span class="sxs-lookup"><span data-stu-id="b990e-117">Domain</span></span> | <span data-ttu-id="b990e-118">幾何</span><span class="sxs-lookup"><span data-stu-id="b990e-118">Geometry</span></span> | <span data-ttu-id="b990e-119">像素</span><span class="sxs-lookup"><span data-stu-id="b990e-119">Pixel</span></span> | <span data-ttu-id="b990e-120">計算</span><span class="sxs-lookup"><span data-stu-id="b990e-120">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="b990e-121">X</span><span class="sxs-lookup"><span data-stu-id="b990e-121">X</span></span>      | <span data-ttu-id="b990e-122">X</span><span class="sxs-lookup"><span data-stu-id="b990e-122">X</span></span>    | <span data-ttu-id="b990e-123">X</span><span class="sxs-lookup"><span data-stu-id="b990e-123">X</span></span>      | <span data-ttu-id="b990e-124">X</span><span class="sxs-lookup"><span data-stu-id="b990e-124">X</span></span>        | <span data-ttu-id="b990e-125">X</span><span class="sxs-lookup"><span data-stu-id="b990e-125">X</span></span>     | <span data-ttu-id="b990e-126">X</span><span class="sxs-lookup"><span data-stu-id="b990e-126">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="b990e-127">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="b990e-127">Minimum Shader Model</span></span>

<span data-ttu-id="b990e-128">下列著色器模型支援此指令：</span><span class="sxs-lookup"><span data-stu-id="b990e-128">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="b990e-129">著色器模型</span><span class="sxs-lookup"><span data-stu-id="b990e-129">Shader Model</span></span>                                              | <span data-ttu-id="b990e-130">支援</span><span class="sxs-lookup"><span data-stu-id="b990e-130">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="b990e-131">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="b990e-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="b990e-132">是</span><span class="sxs-lookup"><span data-stu-id="b990e-132">yes</span></span>       |
| [<span data-ttu-id="b990e-133">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="b990e-133">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="b990e-134">不可以</span><span class="sxs-lookup"><span data-stu-id="b990e-134">no</span></span>        |
| [<span data-ttu-id="b990e-135">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="b990e-135">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="b990e-136">不可以</span><span class="sxs-lookup"><span data-stu-id="b990e-136">no</span></span>        |
| [<span data-ttu-id="b990e-137">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="b990e-137">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="b990e-138">不可以</span><span class="sxs-lookup"><span data-stu-id="b990e-138">no</span></span>        |
| [<span data-ttu-id="b990e-139">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="b990e-139">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="b990e-140">不可以</span><span class="sxs-lookup"><span data-stu-id="b990e-140">no</span></span>        |
| [<span data-ttu-id="b990e-141">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="b990e-141">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="b990e-142">不可以</span><span class="sxs-lookup"><span data-stu-id="b990e-142">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="b990e-143">相關主題</span><span class="sxs-lookup"><span data-stu-id="b990e-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b990e-144">著色器模型5元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="b990e-144">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





