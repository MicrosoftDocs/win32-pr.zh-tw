---
title: 'usubb (sm5-asm) '
description: 不帶正負號的整數減去借用。
ms.assetid: 6D42E3CA-5A37-4194-AB42-7A2337C5AB9D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 111ffd134a75b8cfe19f63597cd80655201359c4
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104373715"
---
# <a name="usubb-sm5---asm"></a><span data-ttu-id="11e21-103">usubb (sm5-asm) </span><span class="sxs-lookup"><span data-stu-id="11e21-103">usubb (sm5 - asm)</span></span>

<span data-ttu-id="11e21-104">不帶正負號的整數減去借用。</span><span class="sxs-lookup"><span data-stu-id="11e21-104">Unsigned integer subtract with borrow.</span></span>



| <span data-ttu-id="11e21-105">usubb dest0 \[ mask \] 、dest1 \[ mask \] 、src0 \[ . swizzle \] 、src1 \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="11e21-105">usubb dest0\[.mask\], dest1\[.mask\], src0\[.swizzle\], src1\[.swizzle\]</span></span> |
|--------------------------------------------------------------------------|



 



| <span data-ttu-id="11e21-106">項目</span><span class="sxs-lookup"><span data-stu-id="11e21-106">Item</span></span>                                                               | <span data-ttu-id="11e21-107">描述</span><span class="sxs-lookup"><span data-stu-id="11e21-107">Description</span></span>                                                                                       |
|--------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11e21-108"><span id="dest0"></span><span id="DEST0"></span>*dest0*</span><span class="sxs-lookup"><span data-stu-id="11e21-108"><span id="dest0"></span><span id="DEST0"></span>*dest0*</span></span><br/> | <span data-ttu-id="11e21-109">\[中的 \] 包含指令的 LSAB 結果。</span><span class="sxs-lookup"><span data-stu-id="11e21-109">\[in\] Contains the LSAB results of the instruction.</span></span><br/>                                   |
| <span data-ttu-id="11e21-110"><span id="dest1"></span><span id="DEST1"></span>*dest1*</span><span class="sxs-lookup"><span data-stu-id="11e21-110"><span id="dest1"></span><span id="DEST1"></span>*dest1*</span></span><br/> | <span data-ttu-id="11e21-111">\[在 \] 指定是否產生借用的對應 *dest0* 元件中。</span><span class="sxs-lookup"><span data-stu-id="11e21-111">\[in\] The corresponding component of *dest0* that specifies if a borrow was produced.</span></span><br/> |
| <span data-ttu-id="11e21-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="11e21-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>    | <span data-ttu-id="11e21-113">\[\]要從中減去的值。</span><span class="sxs-lookup"><span data-stu-id="11e21-113">\[in\] The value from which to subtract.</span></span><br/>                                               |
| <span data-ttu-id="11e21-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="11e21-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/>    | <span data-ttu-id="11e21-115">\[\]從 *src0* 減去的數量。</span><span class="sxs-lookup"><span data-stu-id="11e21-115">\[in\] The amount to subtract from *src0*.</span></span><br/>                                             |



 

## <a name="remarks"></a><span data-ttu-id="11e21-116">備註</span><span class="sxs-lookup"><span data-stu-id="11e21-116">Remarks</span></span>

<span data-ttu-id="11e21-117">此指令會執行從 *src0* *src1* 的元件的不帶正負號減去32位運算元，將32位結果的 LSB 部分放在 *dest0* 中。</span><span class="sxs-lookup"><span data-stu-id="11e21-117">This instruction performs a component-wise unsigned subtract of 32-bit operands *src1* from *src0*, placing the LSB part of the 32-bit result in *dest0*.</span></span>

<span data-ttu-id="11e21-118">如果產生借用， *dest1* 中對應的元件會以1寫入，否則為0。</span><span class="sxs-lookup"><span data-stu-id="11e21-118">The corresponding component in *dest1* is written with 1 if a borrow is produced, 0 otherwise.</span></span>

<span data-ttu-id="11e21-119">如果不需要借用， *dest1* 可以是 Null。</span><span class="sxs-lookup"><span data-stu-id="11e21-119">*dest1* can be NULL if the borrow is not needed.</span></span>

<span data-ttu-id="11e21-120">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="11e21-120">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="11e21-121">頂點</span><span class="sxs-lookup"><span data-stu-id="11e21-121">Vertex</span></span> | <span data-ttu-id="11e21-122">船體</span><span class="sxs-lookup"><span data-stu-id="11e21-122">Hull</span></span> | <span data-ttu-id="11e21-123">網域</span><span class="sxs-lookup"><span data-stu-id="11e21-123">Domain</span></span> | <span data-ttu-id="11e21-124">幾何</span><span class="sxs-lookup"><span data-stu-id="11e21-124">Geometry</span></span> | <span data-ttu-id="11e21-125">像素</span><span class="sxs-lookup"><span data-stu-id="11e21-125">Pixel</span></span> | <span data-ttu-id="11e21-126">計算</span><span class="sxs-lookup"><span data-stu-id="11e21-126">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="11e21-127">X</span><span class="sxs-lookup"><span data-stu-id="11e21-127">X</span></span>      | <span data-ttu-id="11e21-128">X</span><span class="sxs-lookup"><span data-stu-id="11e21-128">X</span></span>    | <span data-ttu-id="11e21-129">X</span><span class="sxs-lookup"><span data-stu-id="11e21-129">X</span></span>      | <span data-ttu-id="11e21-130">X</span><span class="sxs-lookup"><span data-stu-id="11e21-130">X</span></span>        | <span data-ttu-id="11e21-131">X</span><span class="sxs-lookup"><span data-stu-id="11e21-131">X</span></span>     | <span data-ttu-id="11e21-132">X</span><span class="sxs-lookup"><span data-stu-id="11e21-132">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="11e21-133">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="11e21-133">Minimum Shader Model</span></span>

<span data-ttu-id="11e21-134">下列著色器模型支援此指令：</span><span class="sxs-lookup"><span data-stu-id="11e21-134">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="11e21-135">著色器模型</span><span class="sxs-lookup"><span data-stu-id="11e21-135">Shader Model</span></span>                                              | <span data-ttu-id="11e21-136">支援</span><span class="sxs-lookup"><span data-stu-id="11e21-136">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="11e21-137">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="11e21-137">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="11e21-138">是</span><span class="sxs-lookup"><span data-stu-id="11e21-138">yes</span></span>       |
| [<span data-ttu-id="11e21-139">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="11e21-139">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="11e21-140">不可以</span><span class="sxs-lookup"><span data-stu-id="11e21-140">no</span></span>        |
| [<span data-ttu-id="11e21-141">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="11e21-141">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="11e21-142">不可以</span><span class="sxs-lookup"><span data-stu-id="11e21-142">no</span></span>        |
| [<span data-ttu-id="11e21-143">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="11e21-143">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="11e21-144">不可以</span><span class="sxs-lookup"><span data-stu-id="11e21-144">no</span></span>        |
| [<span data-ttu-id="11e21-145">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="11e21-145">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="11e21-146">不可以</span><span class="sxs-lookup"><span data-stu-id="11e21-146">no</span></span>        |
| [<span data-ttu-id="11e21-147">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="11e21-147">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="11e21-148">不可以</span><span class="sxs-lookup"><span data-stu-id="11e21-148">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="11e21-149">相關主題</span><span class="sxs-lookup"><span data-stu-id="11e21-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="11e21-150">著色器模型5元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="11e21-150">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





