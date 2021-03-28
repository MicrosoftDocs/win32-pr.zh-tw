---
title: 'umul (sm4-asm) '
description: 不帶正負號的整數相乘。
ms.assetid: C84AF349-32E6-40C4-9973-BCFA73EFBF0B
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 581696ef5aa7d027c30b4ae866d06401275ef4bc
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104373787"
---
# <a name="umul-sm4---asm"></a><span data-ttu-id="d9bd3-103">umul (sm4-asm) </span><span class="sxs-lookup"><span data-stu-id="d9bd3-103">umul (sm4 - asm)</span></span>

<span data-ttu-id="d9bd3-104">不帶正負號的整數相乘。</span><span class="sxs-lookup"><span data-stu-id="d9bd3-104">Unsigned integer multiply.</span></span>



| <span data-ttu-id="d9bd3-105">umul destHI \[ mask \] 、destLO \[ mask \] 、src0 \[ . swizzle \] 、src1 \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="d9bd3-105">umul destHI\[.mask\], destLO\[.mask\], src0\[.swizzle\], src1\[.swizzle\]</span></span> |
|---------------------------------------------------------------------------|



 



| <span data-ttu-id="d9bd3-106">項目</span><span class="sxs-lookup"><span data-stu-id="d9bd3-106">Item</span></span>                                                                                           | <span data-ttu-id="d9bd3-107">描述</span><span class="sxs-lookup"><span data-stu-id="d9bd3-107">Description</span></span>                                                      |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span data-ttu-id="d9bd3-108"><span id="destHI"></span><span id="desthi"></span><span id="DESTHI"></span>*destHI*</span><span class="sxs-lookup"><span data-stu-id="d9bd3-108"><span id="destHI"></span><span id="desthi"></span><span id="DESTHI"></span>*destHI*</span></span><br/> | <span data-ttu-id="d9bd3-109">\[在 \] 結果的高32位中，每個元件。</span><span class="sxs-lookup"><span data-stu-id="d9bd3-109">\[in\] The high 32 bits of the result, per component.</span></span><br/> |
| <span data-ttu-id="d9bd3-110"><span id="destLO"></span><span id="destlo"></span><span id="DESTLO"></span>*destLO*</span><span class="sxs-lookup"><span data-stu-id="d9bd3-110"><span id="destLO"></span><span id="destlo"></span><span id="DESTLO"></span>*destLO*</span></span><br/> | <span data-ttu-id="d9bd3-111">\[在 \] 結果的低32位中，每個元件。</span><span class="sxs-lookup"><span data-stu-id="d9bd3-111">\[in\] The low 32 bits of the result, per component.</span></span><br/>  |
| <span data-ttu-id="d9bd3-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="d9bd3-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                | <span data-ttu-id="d9bd3-113">\[用 \] 來乘以 *src1* 的元件。</span><span class="sxs-lookup"><span data-stu-id="d9bd3-113">\[in\] The components by which to multiply *src1*.</span></span><br/>    |
| <span data-ttu-id="d9bd3-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="d9bd3-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/>                                | <span data-ttu-id="d9bd3-115">\[用 \] 來乘以 *src0* 的元件。</span><span class="sxs-lookup"><span data-stu-id="d9bd3-115">\[in\] The components by which to multiply *src0*.</span></span><br/>    |



 

## <a name="remarks"></a><span data-ttu-id="d9bd3-116">備註</span><span class="sxs-lookup"><span data-stu-id="d9bd3-116">Remarks</span></span>

<span data-ttu-id="d9bd3-117">此指令會針對未簽署的32位運算元 *src0* 和 *src1* 執行元件的乘積，並為每個元件產生正確的完整64位結果。</span><span class="sxs-lookup"><span data-stu-id="d9bd3-117">This instruction performs a component-wise multiply of unsigned 32-bit operands *src0* and *src1*, producing the correct full 64-bit result per component.</span></span> <span data-ttu-id="d9bd3-118">每個元件的低32位都放在 *destLO* 中。</span><span class="sxs-lookup"><span data-stu-id="d9bd3-118">The low 32 bits per component are placed in *destLO*.</span></span> <span data-ttu-id="d9bd3-119">每個元件的高32位都放在 *destHI* 中。</span><span class="sxs-lookup"><span data-stu-id="d9bd3-119">The high 32 bits per component are placed in *destHI*.</span></span>

<span data-ttu-id="d9bd3-120">您可以指定 *destHI* 或 *DESTLO* 做為 Null，而不是在不需要64位結果的高或低32位時指定暫存器。</span><span class="sxs-lookup"><span data-stu-id="d9bd3-120">You can specify either *destHI* or *destLO* as NULL instead of specifying a register if the high or low 32 bits of the 64-bit result are not needed.</span></span>

<span data-ttu-id="d9bd3-121">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="d9bd3-121">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="d9bd3-122">頂點著色器</span><span class="sxs-lookup"><span data-stu-id="d9bd3-122">Vertex Shader</span></span> | <span data-ttu-id="d9bd3-123">幾何著色器</span><span class="sxs-lookup"><span data-stu-id="d9bd3-123">Geometry Shader</span></span> | <span data-ttu-id="d9bd3-124">像素著色器</span><span class="sxs-lookup"><span data-stu-id="d9bd3-124">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="d9bd3-125">x</span><span class="sxs-lookup"><span data-stu-id="d9bd3-125">x</span></span>             | <span data-ttu-id="d9bd3-126">x</span><span class="sxs-lookup"><span data-stu-id="d9bd3-126">x</span></span>               | <span data-ttu-id="d9bd3-127">x</span><span class="sxs-lookup"><span data-stu-id="d9bd3-127">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="d9bd3-128">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="d9bd3-128">Minimum Shader Model</span></span>

<span data-ttu-id="d9bd3-129">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="d9bd3-129">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="d9bd3-130">著色器模型</span><span class="sxs-lookup"><span data-stu-id="d9bd3-130">Shader Model</span></span>                                              | <span data-ttu-id="d9bd3-131">支援</span><span class="sxs-lookup"><span data-stu-id="d9bd3-131">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="d9bd3-132">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="d9bd3-132">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="d9bd3-133">是</span><span class="sxs-lookup"><span data-stu-id="d9bd3-133">yes</span></span>       |
| [<span data-ttu-id="d9bd3-134">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="d9bd3-134">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="d9bd3-135">是</span><span class="sxs-lookup"><span data-stu-id="d9bd3-135">yes</span></span>       |
| [<span data-ttu-id="d9bd3-136">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="d9bd3-136">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="d9bd3-137">是</span><span class="sxs-lookup"><span data-stu-id="d9bd3-137">yes</span></span>       |
| [<span data-ttu-id="d9bd3-138">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="d9bd3-138">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="d9bd3-139">不可以</span><span class="sxs-lookup"><span data-stu-id="d9bd3-139">no</span></span>        |
| [<span data-ttu-id="d9bd3-140">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="d9bd3-140">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="d9bd3-141">不可以</span><span class="sxs-lookup"><span data-stu-id="d9bd3-141">no</span></span>        |
| [<span data-ttu-id="d9bd3-142">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="d9bd3-142">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="d9bd3-143">不可以</span><span class="sxs-lookup"><span data-stu-id="d9bd3-143">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="d9bd3-144">相關主題</span><span class="sxs-lookup"><span data-stu-id="d9bd3-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d9bd3-145">著色器模型4元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="d9bd3-145">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





