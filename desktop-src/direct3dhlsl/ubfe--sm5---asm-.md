---
title: 'ubfe (sm5-asm) '
description: 指定某個數位的位範圍時，請將這些位移至 LSB，並將其餘的位設定為0。
ms.assetid: CC6BE378-2726-47A2-8E23-B8151521F72D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43ebbe853ec1b53b452f32d79c9c2ec120e826b8
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "103841656"
---
# <a name="ubfe-sm5---asm"></a><span data-ttu-id="ac7ce-103">ubfe (sm5-asm) </span><span class="sxs-lookup"><span data-stu-id="ac7ce-103">ubfe (sm5 - asm)</span></span>

<span data-ttu-id="ac7ce-104">指定某個數位的位範圍時，請將這些位移至 LSB，並將其餘的位設定為0。</span><span class="sxs-lookup"><span data-stu-id="ac7ce-104">Given a range of bits in a number, shift those bits to the LSB and set remaining bits to 0.</span></span>



| <span data-ttu-id="ac7ce-105">ubfe dest \[ . mask \] 、src0 \[ . swizzle \] 、src1 \[ . swizzle \] 、src2 收取 \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="ac7ce-105">ubfe dest\[.mask\], src0\[.swizzle\], src1\[.swizzle\], src2\[.swizzle\]</span></span> |
|--------------------------------------------------------------------------|



 



| <span data-ttu-id="ac7ce-106">項目</span><span class="sxs-lookup"><span data-stu-id="ac7ce-106">Item</span></span>                                                            | <span data-ttu-id="ac7ce-107">描述</span><span class="sxs-lookup"><span data-stu-id="ac7ce-107">Description</span></span>                                                                    |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="ac7ce-108"><span id="dest"></span><span id="DEST"></span>*目標*</span><span class="sxs-lookup"><span data-stu-id="ac7ce-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="ac7ce-109">\[中的 \] 包含指令的結果。</span><span class="sxs-lookup"><span data-stu-id="ac7ce-109">\[in\] Contains the results of the instruction.</span></span><br/>                     |
| <span data-ttu-id="ac7ce-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="ac7ce-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="ac7ce-111">\[在 \] LSB 5 位中， (0-31) 提供位寬。</span><span class="sxs-lookup"><span data-stu-id="ac7ce-111">\[in\] The LSB 5 bits provide the bitfield width (0-31).</span></span><br/>            |
| <span data-ttu-id="ac7ce-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="ac7ce-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="ac7ce-113">\[在 \] *SRC1* 的 LSB 5 位中，提供位 (0-31) 的位位移。</span><span class="sxs-lookup"><span data-stu-id="ac7ce-113">\[in\] The LSB 5 bits of *src1* provide the bitfield offset (0-31).</span></span><br/> |
| <span data-ttu-id="ac7ce-114"><span id="src2"></span><span id="SRC2"></span>*src2 收取*</span><span class="sxs-lookup"><span data-stu-id="ac7ce-114"><span id="src2"></span><span id="SRC2"></span>*src2*</span></span><br/> | <span data-ttu-id="ac7ce-115">\[在 \] 要移位的數位中。</span><span class="sxs-lookup"><span data-stu-id="ac7ce-115">\[in\] The number to shift.</span></span><br/>                                         |



 

## <a name="remarks"></a><span data-ttu-id="ac7ce-116">備註</span><span class="sxs-lookup"><span data-stu-id="ac7ce-116">Remarks</span></span>

``` syntax
 
        Given width, offset:
                if( width == 0 )
                {
                    dest = 0
                }
                else if( width + offset < 32 )
                {
                    shl dest, src2, 32-(width+offset)
                    ushr dest, dest, 32-width
                }
                else
                {
                    ushr dest, src2, offset
                }
```

<span data-ttu-id="ac7ce-117">使用此指令來解除封裝不帶正負號的整數或旗標。</span><span class="sxs-lookup"><span data-stu-id="ac7ce-117">Use this instruction to unpack unsigned integers or flags.</span></span>

<span data-ttu-id="ac7ce-118">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="ac7ce-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="ac7ce-119">頂點</span><span class="sxs-lookup"><span data-stu-id="ac7ce-119">Vertex</span></span> | <span data-ttu-id="ac7ce-120">船體</span><span class="sxs-lookup"><span data-stu-id="ac7ce-120">Hull</span></span> | <span data-ttu-id="ac7ce-121">網域</span><span class="sxs-lookup"><span data-stu-id="ac7ce-121">Domain</span></span> | <span data-ttu-id="ac7ce-122">幾何</span><span class="sxs-lookup"><span data-stu-id="ac7ce-122">Geometry</span></span> | <span data-ttu-id="ac7ce-123">像素</span><span class="sxs-lookup"><span data-stu-id="ac7ce-123">Pixel</span></span> | <span data-ttu-id="ac7ce-124">計算</span><span class="sxs-lookup"><span data-stu-id="ac7ce-124">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="ac7ce-125">X</span><span class="sxs-lookup"><span data-stu-id="ac7ce-125">X</span></span>      | <span data-ttu-id="ac7ce-126">X</span><span class="sxs-lookup"><span data-stu-id="ac7ce-126">X</span></span>    | <span data-ttu-id="ac7ce-127">X</span><span class="sxs-lookup"><span data-stu-id="ac7ce-127">X</span></span>      | <span data-ttu-id="ac7ce-128">X</span><span class="sxs-lookup"><span data-stu-id="ac7ce-128">X</span></span>        | <span data-ttu-id="ac7ce-129">X</span><span class="sxs-lookup"><span data-stu-id="ac7ce-129">X</span></span>     | <span data-ttu-id="ac7ce-130">X</span><span class="sxs-lookup"><span data-stu-id="ac7ce-130">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="ac7ce-131">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="ac7ce-131">Minimum Shader Model</span></span>

<span data-ttu-id="ac7ce-132">下列著色器模型支援此指令：</span><span class="sxs-lookup"><span data-stu-id="ac7ce-132">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="ac7ce-133">著色器模型</span><span class="sxs-lookup"><span data-stu-id="ac7ce-133">Shader Model</span></span>                                              | <span data-ttu-id="ac7ce-134">支援</span><span class="sxs-lookup"><span data-stu-id="ac7ce-134">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="ac7ce-135">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="ac7ce-135">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="ac7ce-136">是</span><span class="sxs-lookup"><span data-stu-id="ac7ce-136">yes</span></span>       |
| [<span data-ttu-id="ac7ce-137">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="ac7ce-137">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="ac7ce-138">不可以</span><span class="sxs-lookup"><span data-stu-id="ac7ce-138">no</span></span>        |
| [<span data-ttu-id="ac7ce-139">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="ac7ce-139">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="ac7ce-140">不可以</span><span class="sxs-lookup"><span data-stu-id="ac7ce-140">no</span></span>        |
| [<span data-ttu-id="ac7ce-141">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="ac7ce-141">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="ac7ce-142">不可以</span><span class="sxs-lookup"><span data-stu-id="ac7ce-142">no</span></span>        |
| [<span data-ttu-id="ac7ce-143">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="ac7ce-143">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="ac7ce-144">不可以</span><span class="sxs-lookup"><span data-stu-id="ac7ce-144">no</span></span>        |
| [<span data-ttu-id="ac7ce-145">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="ac7ce-145">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="ac7ce-146">不可以</span><span class="sxs-lookup"><span data-stu-id="ac7ce-146">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="ac7ce-147">相關主題</span><span class="sxs-lookup"><span data-stu-id="ac7ce-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ac7ce-148">著色器模型5元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="ac7ce-148">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





