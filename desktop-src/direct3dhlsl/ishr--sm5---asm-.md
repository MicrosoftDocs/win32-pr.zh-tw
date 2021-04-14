---
title: 'ishr (sm5-asm) '
description: '算術右移 (sign 擴充) 。 |ishr (sm5-asm) '
ms.assetid: 8124B6C3-4576-4616-85A9-A2DD19EB6BB9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06df958b2e5c6e9cdd2a4dfb3d35c8112453ce9f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104992091"
---
# <a name="ishr-sm5---asm"></a><span data-ttu-id="584bf-104">ishr (sm5-asm) </span><span class="sxs-lookup"><span data-stu-id="584bf-104">ishr (sm5 - asm)</span></span>

<span data-ttu-id="584bf-105">算術右移 (sign 擴充) 。</span><span class="sxs-lookup"><span data-stu-id="584bf-105">Arithmetic shift right (sign extending).</span></span>



| <span data-ttu-id="584bf-106">ishl dest \[ . mask \] 、src0 \[ . swizzle \] 、src1 \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="584bf-106">ishl dest\[.mask\], src0\[.swizzle\], src1\[.swizzle\]</span></span> |
|--------------------------------------------------------|



 



| <span data-ttu-id="584bf-107">項目</span><span class="sxs-lookup"><span data-stu-id="584bf-107">Item</span></span>                                                            | <span data-ttu-id="584bf-108">描述</span><span class="sxs-lookup"><span data-stu-id="584bf-108">Description</span></span>                                          |
|-----------------------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="584bf-109"><span id="dest"></span><span id="DEST"></span>*目標*</span><span class="sxs-lookup"><span data-stu-id="584bf-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="584bf-110">\[中的 \] 包含 shift 的結果。</span><span class="sxs-lookup"><span data-stu-id="584bf-110">\[in\] Contains the results of the shift.</span></span><br/> |
| <span data-ttu-id="584bf-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="584bf-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="584bf-112">\[\]要移位的位數。</span><span class="sxs-lookup"><span data-stu-id="584bf-112">\[in\] The number of bits to shift.</span></span><br/>       |
| <span data-ttu-id="584bf-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="584bf-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="584bf-114">\[在 \] 要移位的32位值中。</span><span class="sxs-lookup"><span data-stu-id="584bf-114">\[in\] The 32-bit values to shift.</span></span><br/>        |



 

## <a name="remarks"></a><span data-ttu-id="584bf-115">備註</span><span class="sxs-lookup"><span data-stu-id="584bf-115">Remarks</span></span>

<span data-ttu-id="584bf-116">此指令會在 *src0* 中執行每個32位值的元件的算術移位，由 LSB 5 位所提供的不帶正負號的整數位計數 (0-31 範圍) 在 *src1* 中，複寫位31的值。</span><span class="sxs-lookup"><span data-stu-id="584bf-116">This instruction performs a component-wise arithmetic shift of each 32-bit value in *src0* right by an unsigned integer bit count provided by the LSB 5 bits (0-31 range) in *src1*, replicating the value of bit 31.</span></span> <span data-ttu-id="584bf-117">每個元件的32位結果都會放置在 *dest* 中。</span><span class="sxs-lookup"><span data-stu-id="584bf-117">The 32-bit per component result is placed in *dest*.</span></span>

<span data-ttu-id="584bf-118">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="584bf-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="584bf-119">頂點</span><span class="sxs-lookup"><span data-stu-id="584bf-119">Vertex</span></span> | <span data-ttu-id="584bf-120">船體</span><span class="sxs-lookup"><span data-stu-id="584bf-120">Hull</span></span> | <span data-ttu-id="584bf-121">網域</span><span class="sxs-lookup"><span data-stu-id="584bf-121">Domain</span></span> | <span data-ttu-id="584bf-122">幾何</span><span class="sxs-lookup"><span data-stu-id="584bf-122">Geometry</span></span> | <span data-ttu-id="584bf-123">像素</span><span class="sxs-lookup"><span data-stu-id="584bf-123">Pixel</span></span> | <span data-ttu-id="584bf-124">計算</span><span class="sxs-lookup"><span data-stu-id="584bf-124">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="584bf-125">X</span><span class="sxs-lookup"><span data-stu-id="584bf-125">X</span></span>      | <span data-ttu-id="584bf-126">X</span><span class="sxs-lookup"><span data-stu-id="584bf-126">X</span></span>    | <span data-ttu-id="584bf-127">X</span><span class="sxs-lookup"><span data-stu-id="584bf-127">X</span></span>      | <span data-ttu-id="584bf-128">X</span><span class="sxs-lookup"><span data-stu-id="584bf-128">X</span></span>        | <span data-ttu-id="584bf-129">X</span><span class="sxs-lookup"><span data-stu-id="584bf-129">X</span></span>     | <span data-ttu-id="584bf-130">X</span><span class="sxs-lookup"><span data-stu-id="584bf-130">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="584bf-131">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="584bf-131">Minimum Shader Model</span></span>

<span data-ttu-id="584bf-132">下列著色器模型支援此指令：</span><span class="sxs-lookup"><span data-stu-id="584bf-132">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="584bf-133">著色器模型</span><span class="sxs-lookup"><span data-stu-id="584bf-133">Shader Model</span></span>                                              | <span data-ttu-id="584bf-134">支援</span><span class="sxs-lookup"><span data-stu-id="584bf-134">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="584bf-135">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="584bf-135">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="584bf-136">是</span><span class="sxs-lookup"><span data-stu-id="584bf-136">yes</span></span>       |
| [<span data-ttu-id="584bf-137">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="584bf-137">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="584bf-138">不可以</span><span class="sxs-lookup"><span data-stu-id="584bf-138">no</span></span>        |
| [<span data-ttu-id="584bf-139">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="584bf-139">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="584bf-140">不可以</span><span class="sxs-lookup"><span data-stu-id="584bf-140">no</span></span>        |
| [<span data-ttu-id="584bf-141">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="584bf-141">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="584bf-142">不可以</span><span class="sxs-lookup"><span data-stu-id="584bf-142">no</span></span>        |
| [<span data-ttu-id="584bf-143">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="584bf-143">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="584bf-144">不可以</span><span class="sxs-lookup"><span data-stu-id="584bf-144">no</span></span>        |
| [<span data-ttu-id="584bf-145">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="584bf-145">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="584bf-146">不可以</span><span class="sxs-lookup"><span data-stu-id="584bf-146">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="584bf-147">相關主題</span><span class="sxs-lookup"><span data-stu-id="584bf-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="584bf-148">著色器模型5元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="584bf-148">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





