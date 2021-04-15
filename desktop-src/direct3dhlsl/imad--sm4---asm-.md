---
title: 'imad (sm4-asm) '
description: 帶正負號的整數乘以並加入。
ms.assetid: 1C24AF49-AA32-4D3A-8478-C9BAC4FE7D77
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90db4cb0a36b0d3951e8b0490bb3ca08db8d5354
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104990715"
---
# <a name="imad-sm4---asm"></a><span data-ttu-id="ed1ee-103">imad (sm4-asm) </span><span class="sxs-lookup"><span data-stu-id="ed1ee-103">imad (sm4 - asm)</span></span>

<span data-ttu-id="ed1ee-104">帶正負號的整數乘以並加入。</span><span class="sxs-lookup"><span data-stu-id="ed1ee-104">Signed integer multiply and add.</span></span>



| <span data-ttu-id="ed1ee-105">imad dest \[ . mask \] 、 \[ - \] src0 \[ . swizzle \] 、 \[ - \] src1 \[ . swizzle \] 、 \[ - \] src2 收取 \[ . swizzle</span><span class="sxs-lookup"><span data-stu-id="ed1ee-105">imad dest\[.mask\], \[-\]src0\[.swizzle\], \[-\]src1\[.swizzle\], \[-\]src2\[.swizzle</span></span> |
|---------------------------------------------------------------------------------------|



 



| <span data-ttu-id="ed1ee-106">項目</span><span class="sxs-lookup"><span data-stu-id="ed1ee-106">Item</span></span>                                                            | <span data-ttu-id="ed1ee-107">描述</span><span class="sxs-lookup"><span data-stu-id="ed1ee-107">Description</span></span>                                                         |
|-----------------------------------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="ed1ee-108"><span id="dest"></span><span id="DEST"></span>*目標*</span><span class="sxs-lookup"><span data-stu-id="ed1ee-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="ed1ee-109">\[在作業的 \] 結果中。</span><span class="sxs-lookup"><span data-stu-id="ed1ee-109">\[in\] The result of the operation.</span></span><br/>                      |
| <span data-ttu-id="ed1ee-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="ed1ee-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="ed1ee-111">\[\]要乘以 *src1* 的值。</span><span class="sxs-lookup"><span data-stu-id="ed1ee-111">\[in\] Value to multiply with *src1*.</span></span><br/>                    |
| <span data-ttu-id="ed1ee-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="ed1ee-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="ed1ee-113">\[\]要乘以 *src0* 的值。</span><span class="sxs-lookup"><span data-stu-id="ed1ee-113">\[in\] Value to multiply with *src0*.</span></span><br/>                    |
| <span data-ttu-id="ed1ee-114"><span id="src2"></span><span id="SRC2"></span>*src2 收取*</span><span class="sxs-lookup"><span data-stu-id="ed1ee-114"><span id="src2"></span><span id="SRC2"></span>*src2*</span></span><br/> | <span data-ttu-id="ed1ee-115">\[\]要加入 *src0* 和 *src1* 產品的值。</span><span class="sxs-lookup"><span data-stu-id="ed1ee-115">\[in\] Value to add to the product of *src0* and *src1*.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ed1ee-116">備註</span><span class="sxs-lookup"><span data-stu-id="ed1ee-116">Remarks</span></span>

<span data-ttu-id="ed1ee-117">32位運算元的元件取向 [imul](imul--sm4---asm-.md) *src0* 和 *src1* (簽署的) 、保留低32位 (每個元件) 結果，接著 [iadd](iadd--sm4---asm-.md) *src2 收取*，產生每個元件的正確低32位 () 結果。</span><span class="sxs-lookup"><span data-stu-id="ed1ee-117">Component-wise [imul](imul--sm4---asm-.md) of 32-bit operands *src0* and *src1* (signed), keeping low 32-bits (per component) of the result, followed by an [iadd](iadd--sm4---asm-.md) of *src2*, producing the correct low 32-bit (per component) result.</span></span> <span data-ttu-id="ed1ee-118">32位的結果會放在 *dest* 中。</span><span class="sxs-lookup"><span data-stu-id="ed1ee-118">The 32-bit results are placed in *dest*.</span></span>

<span data-ttu-id="ed1ee-119">在執行算數運算之前，來源運算元上的選擇性否定修飾詞會採用2的補數。</span><span class="sxs-lookup"><span data-stu-id="ed1ee-119">Optional negate modifier on source operands takes 2's complement before performing arithmetic operation.</span></span>

<span data-ttu-id="ed1ee-120">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="ed1ee-120">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="ed1ee-121">頂點著色器</span><span class="sxs-lookup"><span data-stu-id="ed1ee-121">Vertex Shader</span></span> | <span data-ttu-id="ed1ee-122">幾何著色器</span><span class="sxs-lookup"><span data-stu-id="ed1ee-122">Geometry Shader</span></span> | <span data-ttu-id="ed1ee-123">像素著色器</span><span class="sxs-lookup"><span data-stu-id="ed1ee-123">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="ed1ee-124">x</span><span class="sxs-lookup"><span data-stu-id="ed1ee-124">x</span></span>             | <span data-ttu-id="ed1ee-125">x</span><span class="sxs-lookup"><span data-stu-id="ed1ee-125">x</span></span>               | <span data-ttu-id="ed1ee-126">x</span><span class="sxs-lookup"><span data-stu-id="ed1ee-126">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="ed1ee-127">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="ed1ee-127">Minimum Shader Model</span></span>

<span data-ttu-id="ed1ee-128">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="ed1ee-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="ed1ee-129">著色器模型</span><span class="sxs-lookup"><span data-stu-id="ed1ee-129">Shader Model</span></span>                                              | <span data-ttu-id="ed1ee-130">支援</span><span class="sxs-lookup"><span data-stu-id="ed1ee-130">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="ed1ee-131">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="ed1ee-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="ed1ee-132">是</span><span class="sxs-lookup"><span data-stu-id="ed1ee-132">yes</span></span>       |
| [<span data-ttu-id="ed1ee-133">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="ed1ee-133">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="ed1ee-134">是</span><span class="sxs-lookup"><span data-stu-id="ed1ee-134">yes</span></span>       |
| [<span data-ttu-id="ed1ee-135">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="ed1ee-135">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="ed1ee-136">是</span><span class="sxs-lookup"><span data-stu-id="ed1ee-136">yes</span></span>       |
| [<span data-ttu-id="ed1ee-137">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="ed1ee-137">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="ed1ee-138">不可以</span><span class="sxs-lookup"><span data-stu-id="ed1ee-138">no</span></span>        |
| [<span data-ttu-id="ed1ee-139">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="ed1ee-139">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="ed1ee-140">不可以</span><span class="sxs-lookup"><span data-stu-id="ed1ee-140">no</span></span>        |
| [<span data-ttu-id="ed1ee-141">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="ed1ee-141">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="ed1ee-142">不可以</span><span class="sxs-lookup"><span data-stu-id="ed1ee-142">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="ed1ee-143">相關主題</span><span class="sxs-lookup"><span data-stu-id="ed1ee-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ed1ee-144">著色器模型4元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="ed1ee-144">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





