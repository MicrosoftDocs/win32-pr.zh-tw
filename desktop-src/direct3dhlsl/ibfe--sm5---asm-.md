---
title: 'ibfe (sm5-asm) '
description: 指定某個數位的位範圍時，請將這些位移至 LSB，並將其符號延伸至範圍的 MSB。
ms.assetid: 1ED39812-A89F-4325-82A0-DA2CCC55A99A
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 805d5c1137e25d8b8fa560588b9e876ccc5c8748
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "103679112"
---
# <a name="ibfe-sm5---asm"></a><span data-ttu-id="84398-103">ibfe (sm5-asm) </span><span class="sxs-lookup"><span data-stu-id="84398-103">ibfe (sm5 - asm)</span></span>

<span data-ttu-id="84398-104">指定某個數位的位範圍時，請將這些位移至 LSB，並將其符號延伸至範圍的 MSB。</span><span class="sxs-lookup"><span data-stu-id="84398-104">Given a range of bits in a number, shift those bits to the LSB and sign extend the MSB of the range.</span></span>



| <span data-ttu-id="84398-105">ibfe dest \[ . mask \] 、src0 \[ . swizzle \] 、src1 \[ . swizzle \] 、src2 收取 \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="84398-105">ibfe dest\[.mask\], src0\[.swizzle\], src1\[.swizzle\], src2\[.swizzle\]</span></span> |
|--------------------------------------------------------------------------|



 



| <span data-ttu-id="84398-106">項目</span><span class="sxs-lookup"><span data-stu-id="84398-106">Item</span></span>                                                            | <span data-ttu-id="84398-107">描述</span><span class="sxs-lookup"><span data-stu-id="84398-107">Description</span></span>                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="84398-108"><span id="dest"></span><span id="DEST"></span>*目標*</span><span class="sxs-lookup"><span data-stu-id="84398-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="84398-109">\[在 \] 操作結果的位址中。</span><span class="sxs-lookup"><span data-stu-id="84398-109">\[in\] The address of the results of the operation.</span></span><br/> |
| <span data-ttu-id="84398-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="84398-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="84398-111">\[在 [位位寬度] 中 \] 。</span><span class="sxs-lookup"><span data-stu-id="84398-111">\[in\] The bitfield width.</span></span><br/>                          |
| <span data-ttu-id="84398-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="84398-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="84398-113">\[在欄位 \] 位移中。</span><span class="sxs-lookup"><span data-stu-id="84398-113">\[in\] The bitfield offset.</span></span><br/>                         |
| <span data-ttu-id="84398-114"><span id="src2"></span><span id="SRC2"></span>*src2 收取*</span><span class="sxs-lookup"><span data-stu-id="84398-114"><span id="src2"></span><span id="SRC2"></span>*src2*</span></span><br/> | <span data-ttu-id="84398-115">\[在 \] [要移位的值] 中。</span><span class="sxs-lookup"><span data-stu-id="84398-115">\[in\] The value to shift.</span></span><br/>                          |



 

## <a name="remarks"></a><span data-ttu-id="84398-116">備註</span><span class="sxs-lookup"><span data-stu-id="84398-116">Remarks</span></span>

<span data-ttu-id="84398-117">LSB 5 位的 src0 會提供位寬度 (0-31) 。</span><span class="sxs-lookup"><span data-stu-id="84398-117">The LSB 5 bits of src0 provide the bitfield width (0-31).</span></span>

<span data-ttu-id="84398-118">LSB 5 位的 src1 會提供位 (0-31) 的位位移。</span><span class="sxs-lookup"><span data-stu-id="84398-118">The LSB 5 bits of src1 provide the bitfield offset (0-31).</span></span>

<span data-ttu-id="84398-119">下列範例示範如何使用此指令。</span><span class="sxs-lookup"><span data-stu-id="84398-119">The following example shows how to use this instruction.</span></span>

``` syntax
        Given width, offset:
                if( width == 0 )
                {
                    dest = 0
                }
                else if( width + offset < 32 )
                {
                    shl dest, src2, 32-(width+offset)
                    ishr dest, dest, 32-width
                }
                else
                {
                    ishr dest, src2, offset
                }
```

<span data-ttu-id="84398-120">使用此指令來將帶正負號的整數或旗標解壓縮。</span><span class="sxs-lookup"><span data-stu-id="84398-120">Use this instruction to unpack signed integers or flags.</span></span>

<span data-ttu-id="84398-121">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="84398-121">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="84398-122">頂點</span><span class="sxs-lookup"><span data-stu-id="84398-122">Vertex</span></span> | <span data-ttu-id="84398-123">船體</span><span class="sxs-lookup"><span data-stu-id="84398-123">Hull</span></span> | <span data-ttu-id="84398-124">網域</span><span class="sxs-lookup"><span data-stu-id="84398-124">Domain</span></span> | <span data-ttu-id="84398-125">幾何</span><span class="sxs-lookup"><span data-stu-id="84398-125">Geometry</span></span> | <span data-ttu-id="84398-126">像素</span><span class="sxs-lookup"><span data-stu-id="84398-126">Pixel</span></span> | <span data-ttu-id="84398-127">計算</span><span class="sxs-lookup"><span data-stu-id="84398-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="84398-128">X</span><span class="sxs-lookup"><span data-stu-id="84398-128">X</span></span>      | <span data-ttu-id="84398-129">X</span><span class="sxs-lookup"><span data-stu-id="84398-129">X</span></span>    | <span data-ttu-id="84398-130">X</span><span class="sxs-lookup"><span data-stu-id="84398-130">X</span></span>      | <span data-ttu-id="84398-131">X</span><span class="sxs-lookup"><span data-stu-id="84398-131">X</span></span>        | <span data-ttu-id="84398-132">X</span><span class="sxs-lookup"><span data-stu-id="84398-132">X</span></span>     | <span data-ttu-id="84398-133">X</span><span class="sxs-lookup"><span data-stu-id="84398-133">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="84398-134">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="84398-134">Minimum Shader Model</span></span>

<span data-ttu-id="84398-135">下列著色器模型支援此指令：</span><span class="sxs-lookup"><span data-stu-id="84398-135">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="84398-136">著色器模型</span><span class="sxs-lookup"><span data-stu-id="84398-136">Shader Model</span></span>                                              | <span data-ttu-id="84398-137">支援</span><span class="sxs-lookup"><span data-stu-id="84398-137">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="84398-138">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="84398-138">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="84398-139">是</span><span class="sxs-lookup"><span data-stu-id="84398-139">yes</span></span>       |
| [<span data-ttu-id="84398-140">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="84398-140">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="84398-141">不可以</span><span class="sxs-lookup"><span data-stu-id="84398-141">no</span></span>        |
| [<span data-ttu-id="84398-142">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="84398-142">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="84398-143">不可以</span><span class="sxs-lookup"><span data-stu-id="84398-143">no</span></span>        |
| [<span data-ttu-id="84398-144">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="84398-144">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="84398-145">不可以</span><span class="sxs-lookup"><span data-stu-id="84398-145">no</span></span>        |
| [<span data-ttu-id="84398-146">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="84398-146">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="84398-147">不可以</span><span class="sxs-lookup"><span data-stu-id="84398-147">no</span></span>        |
| [<span data-ttu-id="84398-148">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="84398-148">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="84398-149">不可以</span><span class="sxs-lookup"><span data-stu-id="84398-149">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="84398-150">相關主題</span><span class="sxs-lookup"><span data-stu-id="84398-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="84398-151">著色器模型5元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="84398-151">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





