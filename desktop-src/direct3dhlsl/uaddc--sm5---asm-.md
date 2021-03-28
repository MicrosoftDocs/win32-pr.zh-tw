---
title: 'uaddc (sm5-asm) '
description: 帶有 with 的不帶正負號的整數新增。
ms.assetid: 1007253C-F920-4003-B266-D124A255F731
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f57f75be617e32c15212207110851520a7a281e2
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104507712"
---
# <a name="uaddc-sm5---asm"></a><span data-ttu-id="6b25c-103">uaddc (sm5-asm) </span><span class="sxs-lookup"><span data-stu-id="6b25c-103">uaddc (sm5 - asm)</span></span>

<span data-ttu-id="6b25c-104">帶有 with 的不帶正負號的整數新增。</span><span class="sxs-lookup"><span data-stu-id="6b25c-104">Unsigned integer add with carry.</span></span>



| <span data-ttu-id="6b25c-105">uaddc dest0 \[ mask \] 、dest1 \[ mask \] 、src0 \[ . swizzle \] 、src1 \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="6b25c-105">uaddc dest0\[.mask\], dest1\[.mask\], src0\[.swizzle\], src1\[.swizzle\]</span></span> |
|--------------------------------------------------------------------------|



 



| <span data-ttu-id="6b25c-106">項目</span><span class="sxs-lookup"><span data-stu-id="6b25c-106">Item</span></span>                                                               | <span data-ttu-id="6b25c-107">描述</span><span class="sxs-lookup"><span data-stu-id="6b25c-107">Description</span></span>                                            |
|--------------------------------------------------------------------|--------------------------------------------------------|
| <span data-ttu-id="6b25c-108"><span id="dest0"></span><span id="DEST0"></span>*dest0*</span><span class="sxs-lookup"><span data-stu-id="6b25c-108"><span id="dest0"></span><span id="DEST0"></span>*dest0*</span></span><br/> | <span data-ttu-id="6b25c-109">\[在 \] 結果中的位址。</span><span class="sxs-lookup"><span data-stu-id="6b25c-109">\[in\] Address of the result.</span></span><br/>               |
| <span data-ttu-id="6b25c-110"><span id="dest1"></span><span id="DEST1"></span>*dest1*</span><span class="sxs-lookup"><span data-stu-id="6b25c-110"><span id="dest1"></span><span id="DEST1"></span>*dest1*</span></span><br/> | <span data-ttu-id="6b25c-111">\[\]如果產生，則為1。</span><span class="sxs-lookup"><span data-stu-id="6b25c-111">\[in\] 1 if carry is produced.</span></span> <span data-ttu-id="6b25c-112">否則為 0。</span><span class="sxs-lookup"><span data-stu-id="6b25c-112">Otherwise 0.</span></span><br/> |
| <span data-ttu-id="6b25c-113"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="6b25c-113"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>    | <span data-ttu-id="6b25c-114">\[在 \] 要加入的32位運算元中。</span><span class="sxs-lookup"><span data-stu-id="6b25c-114">\[in\] 32-bit operand to be added.</span></span><br/>          |
| <span data-ttu-id="6b25c-115"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="6b25c-115"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/>    | <span data-ttu-id="6b25c-116">\[在 \] 要加入的32位運算元中。</span><span class="sxs-lookup"><span data-stu-id="6b25c-116">\[in\] 32-bit operand to be added.</span></span><br/>          |



 

## <a name="remarks"></a><span data-ttu-id="6b25c-117">備註</span><span class="sxs-lookup"><span data-stu-id="6b25c-117">Remarks</span></span>

<span data-ttu-id="6b25c-118">如果不需要執行， *dest1* 可以是 Null。</span><span class="sxs-lookup"><span data-stu-id="6b25c-118">*dest1* can be NULL if the carry is not needed.</span></span>

<span data-ttu-id="6b25c-119">請使用此指示進行高精確度的算數運算。</span><span class="sxs-lookup"><span data-stu-id="6b25c-119">Use this instruction for high precision arithmetic.</span></span>

<span data-ttu-id="6b25c-120">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="6b25c-120">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="6b25c-121">頂點</span><span class="sxs-lookup"><span data-stu-id="6b25c-121">Vertex</span></span> | <span data-ttu-id="6b25c-122">船體</span><span class="sxs-lookup"><span data-stu-id="6b25c-122">Hull</span></span> | <span data-ttu-id="6b25c-123">網域</span><span class="sxs-lookup"><span data-stu-id="6b25c-123">Domain</span></span> | <span data-ttu-id="6b25c-124">幾何</span><span class="sxs-lookup"><span data-stu-id="6b25c-124">Geometry</span></span> | <span data-ttu-id="6b25c-125">像素</span><span class="sxs-lookup"><span data-stu-id="6b25c-125">Pixel</span></span> | <span data-ttu-id="6b25c-126">計算</span><span class="sxs-lookup"><span data-stu-id="6b25c-126">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="6b25c-127">X</span><span class="sxs-lookup"><span data-stu-id="6b25c-127">X</span></span>      | <span data-ttu-id="6b25c-128">X</span><span class="sxs-lookup"><span data-stu-id="6b25c-128">X</span></span>    | <span data-ttu-id="6b25c-129">X</span><span class="sxs-lookup"><span data-stu-id="6b25c-129">X</span></span>      | <span data-ttu-id="6b25c-130">X</span><span class="sxs-lookup"><span data-stu-id="6b25c-130">X</span></span>        | <span data-ttu-id="6b25c-131">X</span><span class="sxs-lookup"><span data-stu-id="6b25c-131">X</span></span>     | <span data-ttu-id="6b25c-132">X</span><span class="sxs-lookup"><span data-stu-id="6b25c-132">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="6b25c-133">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="6b25c-133">Minimum Shader Model</span></span>

<span data-ttu-id="6b25c-134">下列著色器模型支援此指令：</span><span class="sxs-lookup"><span data-stu-id="6b25c-134">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="6b25c-135">著色器模型</span><span class="sxs-lookup"><span data-stu-id="6b25c-135">Shader Model</span></span>                                              | <span data-ttu-id="6b25c-136">支援</span><span class="sxs-lookup"><span data-stu-id="6b25c-136">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="6b25c-137">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="6b25c-137">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="6b25c-138">是</span><span class="sxs-lookup"><span data-stu-id="6b25c-138">yes</span></span>       |
| [<span data-ttu-id="6b25c-139">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="6b25c-139">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="6b25c-140">不可以</span><span class="sxs-lookup"><span data-stu-id="6b25c-140">no</span></span>        |
| [<span data-ttu-id="6b25c-141">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="6b25c-141">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="6b25c-142">不可以</span><span class="sxs-lookup"><span data-stu-id="6b25c-142">no</span></span>        |
| [<span data-ttu-id="6b25c-143">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="6b25c-143">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="6b25c-144">不可以</span><span class="sxs-lookup"><span data-stu-id="6b25c-144">no</span></span>        |
| [<span data-ttu-id="6b25c-145">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="6b25c-145">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="6b25c-146">不可以</span><span class="sxs-lookup"><span data-stu-id="6b25c-146">no</span></span>        |
| [<span data-ttu-id="6b25c-147">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="6b25c-147">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="6b25c-148">不可以</span><span class="sxs-lookup"><span data-stu-id="6b25c-148">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="6b25c-149">相關主題</span><span class="sxs-lookup"><span data-stu-id="6b25c-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6b25c-150">著色器模型5元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="6b25c-150">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





