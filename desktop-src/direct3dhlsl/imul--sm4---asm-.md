---
title: 'imul (sm4-asm) '
description: 帶正負號的整數相乘。
ms.assetid: DB95A38F-54E4-4BB6-81DF-CFFEBB4D425B
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 997f62fc389ad1e0fb6b23dd6c419ff8b3933b41
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "103679148"
---
# <a name="imul-sm4---asm"></a><span data-ttu-id="366ee-103">imul (sm4-asm) </span><span class="sxs-lookup"><span data-stu-id="366ee-103">imul (sm4 - asm)</span></span>

<span data-ttu-id="366ee-104">帶正負號的整數相乘。</span><span class="sxs-lookup"><span data-stu-id="366ee-104">Signed integer multiply.</span></span>



| <span data-ttu-id="366ee-105">imul destHI \[ mask \] 、destLO \[ mask \] 、 \[ - \] src0 \[ . swizzle \] 、 \[ - \] src1 \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="366ee-105">imul destHI\[.mask\], destLO\[.mask\], \[-\]src0\[.swizzle\], \[-\]src1\[.swizzle\]</span></span> |
|-------------------------------------------------------------------------------------|



 



| <span data-ttu-id="366ee-106">項目</span><span class="sxs-lookup"><span data-stu-id="366ee-106">Item</span></span>                                                                                           | <span data-ttu-id="366ee-107">描述</span><span class="sxs-lookup"><span data-stu-id="366ee-107">Description</span></span>                                                      |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span data-ttu-id="366ee-108"><span id="destHI"></span><span id="desthi"></span><span id="DESTHI"></span>*destHI*</span><span class="sxs-lookup"><span data-stu-id="366ee-108"><span id="destHI"></span><span id="desthi"></span><span id="DESTHI"></span>*destHI*</span></span><br/> | <span data-ttu-id="366ee-109">\[在 \] 結果的高32位位址中。</span><span class="sxs-lookup"><span data-stu-id="366ee-109">\[in\] The address of the high 32 bits of the result.</span></span><br/> |
| <span data-ttu-id="366ee-110"><span id="destLO"></span><span id="destlo"></span><span id="DESTLO"></span>*destLO*</span><span class="sxs-lookup"><span data-stu-id="366ee-110"><span id="destLO"></span><span id="destlo"></span><span id="DESTLO"></span>*destLO*</span></span><br/> | <span data-ttu-id="366ee-111">\[在 \] 結果的低32位位址中。</span><span class="sxs-lookup"><span data-stu-id="366ee-111">\[in\] The address of the low 32 bits of the result.</span></span><br/>  |
| <span data-ttu-id="366ee-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="366ee-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                | <span data-ttu-id="366ee-113">\[在 \] 要乘以 *src1* 的值中。</span><span class="sxs-lookup"><span data-stu-id="366ee-113">\[in\] The value to multiply with *src1*.</span></span><br/>             |
| <span data-ttu-id="366ee-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="366ee-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/>                                | <span data-ttu-id="366ee-115">\[在 \] 要乘以 *src0* 的值中。</span><span class="sxs-lookup"><span data-stu-id="366ee-115">\[in\] The value to multiply with *src0*.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="366ee-116">備註</span><span class="sxs-lookup"><span data-stu-id="366ee-116">Remarks</span></span>

<span data-ttu-id="366ee-117">32位運算元的元件取向乘以 *src0* 和 *src1* (兩者皆已簽署) ，會產生每個元件的正確完整64位 () 結果。</span><span class="sxs-lookup"><span data-stu-id="366ee-117">Component-wise multiply of 32-bit operands *src0* and *src1* (both are signed), producing the correct full 64-bit (per component) result.</span></span> <span data-ttu-id="366ee-118">每個元件) 的低32位 (放在 *destLO* 中。</span><span class="sxs-lookup"><span data-stu-id="366ee-118">The low 32 bits (per component) are placed in *destLO*.</span></span> <span data-ttu-id="366ee-119">每個元件) 的高32位 (放在 *destHI* 中。</span><span class="sxs-lookup"><span data-stu-id="366ee-119">The high 32 bits (per component) are placed in *destHI*.</span></span>

<span data-ttu-id="366ee-120">如果不需要64位結果的高或低32位，則可以將 *destHI* 或 *DESTLO* 指定為 Null，而不是指定暫存器。</span><span class="sxs-lookup"><span data-stu-id="366ee-120">Either *destHI* or *destLO* may be specified as NULL instead of specifying a register, if the high or low 32 bits of the 64-bit result are not needed.</span></span>

<span data-ttu-id="366ee-121">在執行算數運算之前，來源運算元上的選擇性否定修飾詞會採用2的補數。</span><span class="sxs-lookup"><span data-stu-id="366ee-121">Optional negate modifier on source operands takes 2's complement before performing arithmetic operation.</span></span>

<span data-ttu-id="366ee-122">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="366ee-122">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="366ee-123">頂點著色器</span><span class="sxs-lookup"><span data-stu-id="366ee-123">Vertex Shader</span></span> | <span data-ttu-id="366ee-124">幾何著色器</span><span class="sxs-lookup"><span data-stu-id="366ee-124">Geometry Shader</span></span> | <span data-ttu-id="366ee-125">像素著色器</span><span class="sxs-lookup"><span data-stu-id="366ee-125">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="366ee-126">x</span><span class="sxs-lookup"><span data-stu-id="366ee-126">x</span></span>             | <span data-ttu-id="366ee-127">x</span><span class="sxs-lookup"><span data-stu-id="366ee-127">x</span></span>               | <span data-ttu-id="366ee-128">x</span><span class="sxs-lookup"><span data-stu-id="366ee-128">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="366ee-129">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="366ee-129">Minimum Shader Model</span></span>

<span data-ttu-id="366ee-130">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="366ee-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="366ee-131">著色器模型</span><span class="sxs-lookup"><span data-stu-id="366ee-131">Shader Model</span></span>                                              | <span data-ttu-id="366ee-132">支援</span><span class="sxs-lookup"><span data-stu-id="366ee-132">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="366ee-133">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="366ee-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="366ee-134">是</span><span class="sxs-lookup"><span data-stu-id="366ee-134">yes</span></span>       |
| [<span data-ttu-id="366ee-135">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="366ee-135">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="366ee-136">是</span><span class="sxs-lookup"><span data-stu-id="366ee-136">yes</span></span>       |
| [<span data-ttu-id="366ee-137">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="366ee-137">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="366ee-138">是</span><span class="sxs-lookup"><span data-stu-id="366ee-138">yes</span></span>       |
| [<span data-ttu-id="366ee-139">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="366ee-139">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="366ee-140">不可以</span><span class="sxs-lookup"><span data-stu-id="366ee-140">no</span></span>        |
| [<span data-ttu-id="366ee-141">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="366ee-141">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="366ee-142">不可以</span><span class="sxs-lookup"><span data-stu-id="366ee-142">no</span></span>        |
| [<span data-ttu-id="366ee-143">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="366ee-143">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="366ee-144">不可以</span><span class="sxs-lookup"><span data-stu-id="366ee-144">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="366ee-145">相關主題</span><span class="sxs-lookup"><span data-stu-id="366ee-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="366ee-146">著色器模型4元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="366ee-146">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





