---
title: 'bfi (sm5-asm) '
description: 從數位的 LSB 中指定位範圍，並將該位數的數位放在其他數位的任何位移。
ms.assetid: BA84C882-A141-4AD2-8FD9-C60F1483FC65
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a14f8b9f6ef126ec3c6a31bf330dfd89cf0770c4
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104022832"
---
# <a name="bfi-sm5---asm"></a><span data-ttu-id="23223-103">bfi (sm5-asm) </span><span class="sxs-lookup"><span data-stu-id="23223-103">bfi (sm5 - asm)</span></span>

<span data-ttu-id="23223-104">從數位的 LSB 中指定位範圍，並將該位數的數位放在其他數位的任何位移。</span><span class="sxs-lookup"><span data-stu-id="23223-104">Given a bit range from the LSB of a number, place that number of bits in another number at any offset.</span></span>



| <span data-ttu-id="23223-105">bfi dest \[ . mask \] 、src0 \[ . swizzle \] 、src1 \[ . swizzle \] 、src2 收取 \[ . swizzle \] 、src3 \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="23223-105">bfi dest\[.mask\], src0\[.swizzle\], src1\[.swizzle\], src2\[.swizzle\], src3\[.swizzle\]</span></span> |
|-------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="23223-106">項目</span><span class="sxs-lookup"><span data-stu-id="23223-106">Item</span></span>                                                            | <span data-ttu-id="23223-107">描述</span><span class="sxs-lookup"><span data-stu-id="23223-107">Description</span></span>                                                         |
|-----------------------------------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="23223-108"><span id="dest"></span><span id="DEST"></span>*目標*</span><span class="sxs-lookup"><span data-stu-id="23223-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="23223-109">\[在 \] 結果的位址中。</span><span class="sxs-lookup"><span data-stu-id="23223-109">\[in\] The address of the results.</span></span><br/>                       |
| <span data-ttu-id="23223-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="23223-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="23223-111">\[\]要從 *src2 收取* 取得的位位寬度。</span><span class="sxs-lookup"><span data-stu-id="23223-111">\[in\] The bitfield width to take from *src2*.</span></span><br/>           |
| <span data-ttu-id="23223-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="23223-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="23223-113">\[用 \] 來取代 *src3* 中之位的位位位移。</span><span class="sxs-lookup"><span data-stu-id="23223-113">\[in\] The bitfield offset for replacing bits in *src3*.</span></span><br/> |
| <span data-ttu-id="23223-114"><span id="src2"></span><span id="SRC2"></span>*src2 收取*</span><span class="sxs-lookup"><span data-stu-id="23223-114"><span id="src2"></span><span id="SRC2"></span>*src2*</span></span><br/> | <span data-ttu-id="23223-115">\[\]從取得位數的數位。</span><span class="sxs-lookup"><span data-stu-id="23223-115">\[in\] The number the bits are taken from.</span></span> <br/>              |
| <span data-ttu-id="23223-116"><span id="src3"></span><span id="SRC3"></span>*src3*</span><span class="sxs-lookup"><span data-stu-id="23223-116"><span id="src3"></span><span id="SRC3"></span>*src3*</span></span><br/> | <span data-ttu-id="23223-117">\[， \] 包含要取代的位數。</span><span class="sxs-lookup"><span data-stu-id="23223-117">\[in\] The number with bits to be replaced.</span></span><br/>              |



 

## <a name="remarks"></a><span data-ttu-id="23223-118">備註</span><span class="sxs-lookup"><span data-stu-id="23223-118">Remarks</span></span>

<span data-ttu-id="23223-119">LSB 5 位的 *src0* 會提供位寬度 (0-31) 要從 *src2 收取* 中取得。</span><span class="sxs-lookup"><span data-stu-id="23223-119">The LSB 5 bits of *src0* provide the bitfield width (0-31) to take from *src2*.</span></span>

<span data-ttu-id="23223-120">*Src1* 的 LSB 5 位會提供位位移 (0-31) 來開始取代從 *src3* 讀取的位數。</span><span class="sxs-lookup"><span data-stu-id="23223-120">The LSB 5 bits of *src1* provide the bitfield offset (0-31) to start replacing bits in the number read from *src3*.</span></span>

``` syntax
Given width, offset:
                bitmask = (((1 << width)-1) << offset) & 0xffffffff
                dest = ((src2 << offset) & bitmask) | (src3 & ~bitmask)
```

<span data-ttu-id="23223-121">此指令用於封裝整數或旗標。</span><span class="sxs-lookup"><span data-stu-id="23223-121">This instruction is used for packing integers or flags.</span></span>

<span data-ttu-id="23223-122">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="23223-122">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="23223-123">頂點</span><span class="sxs-lookup"><span data-stu-id="23223-123">Vertex</span></span> | <span data-ttu-id="23223-124">船體</span><span class="sxs-lookup"><span data-stu-id="23223-124">Hull</span></span> | <span data-ttu-id="23223-125">網域</span><span class="sxs-lookup"><span data-stu-id="23223-125">Domain</span></span> | <span data-ttu-id="23223-126">幾何</span><span class="sxs-lookup"><span data-stu-id="23223-126">Geometry</span></span> | <span data-ttu-id="23223-127">像素</span><span class="sxs-lookup"><span data-stu-id="23223-127">Pixel</span></span> | <span data-ttu-id="23223-128">計算</span><span class="sxs-lookup"><span data-stu-id="23223-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="23223-129">X</span><span class="sxs-lookup"><span data-stu-id="23223-129">X</span></span>      | <span data-ttu-id="23223-130">X</span><span class="sxs-lookup"><span data-stu-id="23223-130">X</span></span>    | <span data-ttu-id="23223-131">X</span><span class="sxs-lookup"><span data-stu-id="23223-131">X</span></span>      | <span data-ttu-id="23223-132">X</span><span class="sxs-lookup"><span data-stu-id="23223-132">X</span></span>        | <span data-ttu-id="23223-133">X</span><span class="sxs-lookup"><span data-stu-id="23223-133">X</span></span>     | <span data-ttu-id="23223-134">X</span><span class="sxs-lookup"><span data-stu-id="23223-134">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="23223-135">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="23223-135">Minimum Shader Model</span></span>

<span data-ttu-id="23223-136">下列著色器模型支援此指令：</span><span class="sxs-lookup"><span data-stu-id="23223-136">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="23223-137">著色器模型</span><span class="sxs-lookup"><span data-stu-id="23223-137">Shader Model</span></span>                                              | <span data-ttu-id="23223-138">支援</span><span class="sxs-lookup"><span data-stu-id="23223-138">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="23223-139">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="23223-139">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="23223-140">是</span><span class="sxs-lookup"><span data-stu-id="23223-140">yes</span></span>       |
| [<span data-ttu-id="23223-141">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="23223-141">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="23223-142">不可以</span><span class="sxs-lookup"><span data-stu-id="23223-142">no</span></span>        |
| [<span data-ttu-id="23223-143">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="23223-143">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="23223-144">不可以</span><span class="sxs-lookup"><span data-stu-id="23223-144">no</span></span>        |
| [<span data-ttu-id="23223-145">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="23223-145">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="23223-146">不可以</span><span class="sxs-lookup"><span data-stu-id="23223-146">no</span></span>        |
| [<span data-ttu-id="23223-147">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="23223-147">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="23223-148">不可以</span><span class="sxs-lookup"><span data-stu-id="23223-148">no</span></span>        |
| [<span data-ttu-id="23223-149">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="23223-149">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="23223-150">不可以</span><span class="sxs-lookup"><span data-stu-id="23223-150">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="23223-151">相關主題</span><span class="sxs-lookup"><span data-stu-id="23223-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="23223-152">著色器模型5元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="23223-152">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





