---
title: 'ishr (sm4-asm) '
description: '算術右移 (sign 擴充) 。 |ishr (sm4-asm) '
ms.assetid: AFE46BBA-A6B2-4691-A3F4-A4141F1578DB
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7516543c5501ed886c5c1fa98d093062e3099a0f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104992094"
---
# <a name="ishr-sm4---asm"></a><span data-ttu-id="42c25-104">ishr (sm4-asm) </span><span class="sxs-lookup"><span data-stu-id="42c25-104">ishr (sm4 - asm)</span></span>

<span data-ttu-id="42c25-105">算術右移 (sign 擴充) 。</span><span class="sxs-lookup"><span data-stu-id="42c25-105">Arithmetic shift right (sign extending).</span></span>



| <span data-ttu-id="42c25-106">ishr dest \[ . mask \] ，src0 \[ . swizzle \] ，src1. select \_ component</span><span class="sxs-lookup"><span data-stu-id="42c25-106">ishr dest\[.mask\], src0\[.swizzle\], src1.select\_component</span></span> |
|--------------------------------------------------------------|



 



| <span data-ttu-id="42c25-107">項目</span><span class="sxs-lookup"><span data-stu-id="42c25-107">Item</span></span>                                                            | <span data-ttu-id="42c25-108">描述</span><span class="sxs-lookup"><span data-stu-id="42c25-108">Description</span></span>                                             |
|-----------------------------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="42c25-109"><span id="dest"></span><span id="DEST"></span>*目標*</span><span class="sxs-lookup"><span data-stu-id="42c25-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="42c25-110">\[中的 \] 包含運算的結果。</span><span class="sxs-lookup"><span data-stu-id="42c25-110">\[in\] Contains the result of the operation.</span></span><br/> |
| <span data-ttu-id="42c25-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="42c25-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="42c25-112">\[in \] 包含要移位的值。</span><span class="sxs-lookup"><span data-stu-id="42c25-112">\[in\] Contains the value to be shifted.</span></span><br/>     |
| <span data-ttu-id="42c25-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="42c25-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="42c25-114">\[in \] 包含移位量。</span><span class="sxs-lookup"><span data-stu-id="42c25-114">\[in\] Contains the shift amount.</span></span><br/>            |



 

## <a name="remarks"></a><span data-ttu-id="42c25-115">備註</span><span class="sxs-lookup"><span data-stu-id="42c25-115">Remarks</span></span>

<span data-ttu-id="42c25-116">此指令會在 *src0* 中執行每個32位值的元件的算術移位，由 LSB 5 位所提供的不帶正負號整數位移， (0-31 範圍) 在 *src1 中。選取 [ \_ 元件*]，複寫位31的值。</span><span class="sxs-lookup"><span data-stu-id="42c25-116">This instruction performs a component-wise arithmetic shift of each 32-bit value in *src0* right by an unsigned integer bit count provided by the LSB 5 bits (0-31 range) in *src1.select\_component*, replicating the value of bit 31.</span></span> <span data-ttu-id="42c25-117">每個元件的32位結果都會放置在 *dest* 中。</span><span class="sxs-lookup"><span data-stu-id="42c25-117">The 32-bit per component result is placed in *dest*.</span></span> <span data-ttu-id="42c25-118">計數是套用至所有元件的純量值。</span><span class="sxs-lookup"><span data-stu-id="42c25-118">The count is a scalar value applied to all components.</span></span>

<span data-ttu-id="42c25-119">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="42c25-119">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="42c25-120">頂點著色器</span><span class="sxs-lookup"><span data-stu-id="42c25-120">Vertex Shader</span></span> | <span data-ttu-id="42c25-121">幾何著色器</span><span class="sxs-lookup"><span data-stu-id="42c25-121">Geometry Shader</span></span> | <span data-ttu-id="42c25-122">像素著色器</span><span class="sxs-lookup"><span data-stu-id="42c25-122">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="42c25-123">x</span><span class="sxs-lookup"><span data-stu-id="42c25-123">x</span></span>             | <span data-ttu-id="42c25-124">x</span><span class="sxs-lookup"><span data-stu-id="42c25-124">x</span></span>               | <span data-ttu-id="42c25-125">x</span><span class="sxs-lookup"><span data-stu-id="42c25-125">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="42c25-126">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="42c25-126">Minimum Shader Model</span></span>

<span data-ttu-id="42c25-127">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="42c25-127">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="42c25-128">著色器模型</span><span class="sxs-lookup"><span data-stu-id="42c25-128">Shader Model</span></span>                                              | <span data-ttu-id="42c25-129">支援</span><span class="sxs-lookup"><span data-stu-id="42c25-129">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="42c25-130">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="42c25-130">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="42c25-131">是</span><span class="sxs-lookup"><span data-stu-id="42c25-131">yes</span></span>       |
| [<span data-ttu-id="42c25-132">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="42c25-132">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="42c25-133">是</span><span class="sxs-lookup"><span data-stu-id="42c25-133">yes</span></span>       |
| [<span data-ttu-id="42c25-134">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="42c25-134">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="42c25-135">是</span><span class="sxs-lookup"><span data-stu-id="42c25-135">yes</span></span>       |
| [<span data-ttu-id="42c25-136">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="42c25-136">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="42c25-137">不可以</span><span class="sxs-lookup"><span data-stu-id="42c25-137">no</span></span>        |
| [<span data-ttu-id="42c25-138">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="42c25-138">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="42c25-139">不可以</span><span class="sxs-lookup"><span data-stu-id="42c25-139">no</span></span>        |
| [<span data-ttu-id="42c25-140">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="42c25-140">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="42c25-141">不可以</span><span class="sxs-lookup"><span data-stu-id="42c25-141">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="42c25-142">相關主題</span><span class="sxs-lookup"><span data-stu-id="42c25-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="42c25-143">著色器模型4元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="42c25-143">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





