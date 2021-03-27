---
title: 'umad (sm4-asm) '
description: 不帶正負號的整數相乘和 add。
ms.assetid: C0BE31CA-E01D-42C0-A660-E63727CE344F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce52925622cb2f6f7cf53dec0e3f6f65d3fdcb58
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "103679128"
---
# <a name="umad-sm4---asm"></a><span data-ttu-id="ea5a3-103">umad (sm4-asm) </span><span class="sxs-lookup"><span data-stu-id="ea5a3-103">umad (sm4 - asm)</span></span>

<span data-ttu-id="ea5a3-104">不帶正負號的整數相乘和 add。</span><span class="sxs-lookup"><span data-stu-id="ea5a3-104">Unsigned integer multiply and add.</span></span>



| <span data-ttu-id="ea5a3-105">umad dest \[ . mask \] 、src0 \[ . swizzle \] 、src1 \[ . swizzle \] 、src2 收取 \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="ea5a3-105">umad dest\[.mask\], src0\[.swizzle\], src1\[.swizzle\], src2\[.swizzle\]</span></span> |
|--------------------------------------------------------------------------|



 



| <span data-ttu-id="ea5a3-106">項目</span><span class="sxs-lookup"><span data-stu-id="ea5a3-106">Item</span></span>                                                            | <span data-ttu-id="ea5a3-107">描述</span><span class="sxs-lookup"><span data-stu-id="ea5a3-107">Description</span></span>                                                             |
|-----------------------------------------------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="ea5a3-108"><span id="dest"></span><span id="DEST"></span>*目標*</span><span class="sxs-lookup"><span data-stu-id="ea5a3-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="ea5a3-109">\[在 \] 操作結果的位址中。</span><span class="sxs-lookup"><span data-stu-id="ea5a3-109">\[in\] The address of the result of the operation.</span></span><br/>           |
| <span data-ttu-id="ea5a3-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="ea5a3-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="ea5a3-111">\[在 \] 要乘以 *src1* 的值中。</span><span class="sxs-lookup"><span data-stu-id="ea5a3-111">\[in\] The value to multiply with *src1*.</span></span><br/>                    |
| <span data-ttu-id="ea5a3-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="ea5a3-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="ea5a3-113">\[在 \] 要乘以 *src1* 的值中。</span><span class="sxs-lookup"><span data-stu-id="ea5a3-113">\[in\] The value to multiply with *src1*.</span></span><br/>                     |
| <span data-ttu-id="ea5a3-114"><span id="src2"></span><span id="SRC2"></span>*src2 收取*</span><span class="sxs-lookup"><span data-stu-id="ea5a3-114"><span id="src2"></span><span id="SRC2"></span>*src2*</span></span><br/> | <span data-ttu-id="ea5a3-115">\[在 \] 要加入至 *src0* 和 *src1* 產品的值中。</span><span class="sxs-lookup"><span data-stu-id="ea5a3-115">\[in\] The value to add to the product of *src0* and *src1*.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ea5a3-116">備註</span><span class="sxs-lookup"><span data-stu-id="ea5a3-116">Remarks</span></span>

<span data-ttu-id="ea5a3-117">32位運算元的元件取向 [umul](umul--sm4---asm-.md) *src0* 和 *src1* 未簽署，並保留結果的低32位（每個元件）。</span><span class="sxs-lookup"><span data-stu-id="ea5a3-117">Component-wise [umul](umul--sm4---asm-.md) of 32-bit operands *src0* and *src1* unsigned, keeping the low 32-bits, per component, of the result.</span></span> <span data-ttu-id="ea5a3-118">此指令接著會執行 *src2 收取* 的 [iadd](iadd--sm4---asm-.md) ，) 結果產生每個元件的正確低32位 (。</span><span class="sxs-lookup"><span data-stu-id="ea5a3-118">This instruction then performs an [iadd](iadd--sm4---asm-.md) of *src2*, producing the correct low 32-bit (per component) result.</span></span> <span data-ttu-id="ea5a3-119">32位的結果會放在 *dest* 中。</span><span class="sxs-lookup"><span data-stu-id="ea5a3-119">The 32-bit results are placed in *dest*.</span></span>

<span data-ttu-id="ea5a3-120">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="ea5a3-120">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="ea5a3-121">頂點著色器</span><span class="sxs-lookup"><span data-stu-id="ea5a3-121">Vertex Shader</span></span> | <span data-ttu-id="ea5a3-122">幾何著色器</span><span class="sxs-lookup"><span data-stu-id="ea5a3-122">Geometry Shader</span></span> | <span data-ttu-id="ea5a3-123">像素著色器</span><span class="sxs-lookup"><span data-stu-id="ea5a3-123">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="ea5a3-124">x</span><span class="sxs-lookup"><span data-stu-id="ea5a3-124">x</span></span>             | <span data-ttu-id="ea5a3-125">x</span><span class="sxs-lookup"><span data-stu-id="ea5a3-125">x</span></span>               | <span data-ttu-id="ea5a3-126">x</span><span class="sxs-lookup"><span data-stu-id="ea5a3-126">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="ea5a3-127">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="ea5a3-127">Minimum Shader Model</span></span>

<span data-ttu-id="ea5a3-128">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="ea5a3-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="ea5a3-129">著色器模型</span><span class="sxs-lookup"><span data-stu-id="ea5a3-129">Shader Model</span></span>                                              | <span data-ttu-id="ea5a3-130">支援</span><span class="sxs-lookup"><span data-stu-id="ea5a3-130">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="ea5a3-131">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="ea5a3-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="ea5a3-132">是</span><span class="sxs-lookup"><span data-stu-id="ea5a3-132">yes</span></span>       |
| [<span data-ttu-id="ea5a3-133">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="ea5a3-133">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="ea5a3-134">是</span><span class="sxs-lookup"><span data-stu-id="ea5a3-134">yes</span></span>       |
| [<span data-ttu-id="ea5a3-135">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="ea5a3-135">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="ea5a3-136">是</span><span class="sxs-lookup"><span data-stu-id="ea5a3-136">yes</span></span>       |
| [<span data-ttu-id="ea5a3-137">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="ea5a3-137">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="ea5a3-138">不可以</span><span class="sxs-lookup"><span data-stu-id="ea5a3-138">no</span></span>        |
| [<span data-ttu-id="ea5a3-139">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="ea5a3-139">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="ea5a3-140">不可以</span><span class="sxs-lookup"><span data-stu-id="ea5a3-140">no</span></span>        |
| [<span data-ttu-id="ea5a3-141">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="ea5a3-141">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="ea5a3-142">不可以</span><span class="sxs-lookup"><span data-stu-id="ea5a3-142">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="ea5a3-143">相關主題</span><span class="sxs-lookup"><span data-stu-id="ea5a3-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ea5a3-144">著色器模型4元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="ea5a3-144">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





