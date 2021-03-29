---
title: 'ushr (sm5-asm) '
description: '右移。 |ushr (sm5-asm) '
ms.assetid: C695CB6C-A6C9-4DC8-8EBE-70A0CFFC4981
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f33c627ec4aa985b5ac8a27cf0babd6219c9247c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104974216"
---
# <a name="ushr-sm5---asm"></a><span data-ttu-id="ac09f-104">ushr (sm5-asm) </span><span class="sxs-lookup"><span data-stu-id="ac09f-104">ushr (sm5 - asm)</span></span>

<span data-ttu-id="ac09f-105">右移。</span><span class="sxs-lookup"><span data-stu-id="ac09f-105">Shift right.</span></span>



| <span data-ttu-id="ac09f-106">ubfe dest \[ . mask \] 、src0 \[ . swizzle \] 、src1 \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="ac09f-106">ubfe dest\[.mask\], src0\[.swizzle\], src1\[.swizzle\]</span></span> |
|--------------------------------------------------------|



 



| <span data-ttu-id="ac09f-107">項目</span><span class="sxs-lookup"><span data-stu-id="ac09f-107">Item</span></span>                                                            | <span data-ttu-id="ac09f-108">描述</span><span class="sxs-lookup"><span data-stu-id="ac09f-108">Description</span></span>                                                                  |
|-----------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="ac09f-109"><span id="dest"></span><span id="DEST"></span>*目標*</span><span class="sxs-lookup"><span data-stu-id="ac09f-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="ac09f-110">\[中的 \] 包含指令的結果。</span><span class="sxs-lookup"><span data-stu-id="ac09f-110">\[in\] Contains the results of the instruction.</span></span><br/>                   |
| <span data-ttu-id="ac09f-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="ac09f-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="ac09f-112">\[在 \] 要移位的32位值中。</span><span class="sxs-lookup"><span data-stu-id="ac09f-112">\[in\] The 32-bit values to shift.</span></span><br/>                                |
| <span data-ttu-id="ac09f-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="ac09f-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="ac09f-114">\[在 \] LSB 5 位中，提供 (0-31) 移位的位數。</span><span class="sxs-lookup"><span data-stu-id="ac09f-114">\[in\] The LSB 5 bits provide the number of bits to shift (0-31).</span></span><br/> |



 

<span data-ttu-id="ac09f-115">此指令會在 src0 中，以 LSB 5) 0-31 (位所提供的不帶正負號的整數位元數目，在 *src1* 中插入0時，以元件的方式，在中執行每個32位值的元件轉移。</span><span class="sxs-lookup"><span data-stu-id="ac09f-115">This instruction performs a component-wise shift of each 32-bit value in *src0* right by an unsigned integer bit count provided by the LSB 5 bits (0-31 range) in *src1*, inserting 0.</span></span> <span data-ttu-id="ac09f-116">每個元件的32位結果都會放置在 *dest* 中。</span><span class="sxs-lookup"><span data-stu-id="ac09f-116">The 32-bit per component results is placed in *dest*.</span></span>

<span data-ttu-id="ac09f-117">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="ac09f-117">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="ac09f-118">頂點</span><span class="sxs-lookup"><span data-stu-id="ac09f-118">Vertex</span></span> | <span data-ttu-id="ac09f-119">船體</span><span class="sxs-lookup"><span data-stu-id="ac09f-119">Hull</span></span> | <span data-ttu-id="ac09f-120">網域</span><span class="sxs-lookup"><span data-stu-id="ac09f-120">Domain</span></span> | <span data-ttu-id="ac09f-121">幾何</span><span class="sxs-lookup"><span data-stu-id="ac09f-121">Geometry</span></span> | <span data-ttu-id="ac09f-122">像素</span><span class="sxs-lookup"><span data-stu-id="ac09f-122">Pixel</span></span> | <span data-ttu-id="ac09f-123">計算</span><span class="sxs-lookup"><span data-stu-id="ac09f-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="ac09f-124">X</span><span class="sxs-lookup"><span data-stu-id="ac09f-124">X</span></span>      | <span data-ttu-id="ac09f-125">X</span><span class="sxs-lookup"><span data-stu-id="ac09f-125">X</span></span>    | <span data-ttu-id="ac09f-126">X</span><span class="sxs-lookup"><span data-stu-id="ac09f-126">X</span></span>      | <span data-ttu-id="ac09f-127">X</span><span class="sxs-lookup"><span data-stu-id="ac09f-127">X</span></span>        | <span data-ttu-id="ac09f-128">X</span><span class="sxs-lookup"><span data-stu-id="ac09f-128">X</span></span>     | <span data-ttu-id="ac09f-129">X</span><span class="sxs-lookup"><span data-stu-id="ac09f-129">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="ac09f-130">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="ac09f-130">Minimum Shader Model</span></span>

<span data-ttu-id="ac09f-131">下列著色器模型支援此指令：</span><span class="sxs-lookup"><span data-stu-id="ac09f-131">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="ac09f-132">著色器模型</span><span class="sxs-lookup"><span data-stu-id="ac09f-132">Shader Model</span></span>                                              | <span data-ttu-id="ac09f-133">支援</span><span class="sxs-lookup"><span data-stu-id="ac09f-133">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="ac09f-134">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="ac09f-134">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="ac09f-135">是</span><span class="sxs-lookup"><span data-stu-id="ac09f-135">yes</span></span>       |
| [<span data-ttu-id="ac09f-136">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="ac09f-136">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="ac09f-137">不可以</span><span class="sxs-lookup"><span data-stu-id="ac09f-137">no</span></span>        |
| [<span data-ttu-id="ac09f-138">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="ac09f-138">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="ac09f-139">不可以</span><span class="sxs-lookup"><span data-stu-id="ac09f-139">no</span></span>        |
| [<span data-ttu-id="ac09f-140">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="ac09f-140">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="ac09f-141">不可以</span><span class="sxs-lookup"><span data-stu-id="ac09f-141">no</span></span>        |
| [<span data-ttu-id="ac09f-142">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="ac09f-142">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="ac09f-143">不可以</span><span class="sxs-lookup"><span data-stu-id="ac09f-143">no</span></span>        |
| [<span data-ttu-id="ac09f-144">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="ac09f-144">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="ac09f-145">不可以</span><span class="sxs-lookup"><span data-stu-id="ac09f-145">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="ac09f-146">相關主題</span><span class="sxs-lookup"><span data-stu-id="ac09f-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ac09f-147">著色器模型5元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="ac09f-147">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





