---
title: 'imax (sm4-asm) '
description: 元件的最大整數。
ms.assetid: 005468AA-577E-441F-ACD5-37A691E62CDD
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc1bc6311573b1e7b39fbeaa93904203e7aae2ae
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104092445"
---
# <a name="imax-sm4---asm"></a><span data-ttu-id="a51f4-103">imax (sm4-asm) </span><span class="sxs-lookup"><span data-stu-id="a51f4-103">imax (sm4 - asm)</span></span>

<span data-ttu-id="a51f4-104">元件的最大整數。</span><span class="sxs-lookup"><span data-stu-id="a51f4-104">Component-wise integer maximum.</span></span>



| <span data-ttu-id="a51f4-105">imax dest \[ . mask \] 、 \[  - \] src0 \[ . swizzle \] 、 \[ - \] src1 \[ . swizzle \] 、</span><span class="sxs-lookup"><span data-stu-id="a51f4-105">imax dest\[.mask\], \[ -\]src0\[.swizzle\], \[-\]src1\[.swizzle\],</span></span> |
|--------------------------------------------------------------------|



 



| <span data-ttu-id="a51f4-106">項目</span><span class="sxs-lookup"><span data-stu-id="a51f4-106">Item</span></span>                                                            | <span data-ttu-id="a51f4-107">描述</span><span class="sxs-lookup"><span data-stu-id="a51f4-107">Description</span></span>                                                                                             |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a51f4-108"><span id="dest"></span><span id="DEST"></span>*目標*</span><span class="sxs-lookup"><span data-stu-id="a51f4-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="a51f4-109">\[在作業的 \] 結果中。</span><span class="sxs-lookup"><span data-stu-id="a51f4-109">\[in\] The result of the operation.</span></span><br/> <span data-ttu-id="a51f4-110">*目的地*  = *src0*  > *src1* 嗎？</span><span class="sxs-lookup"><span data-stu-id="a51f4-110">*dest* = *src0* > *src1* ?</span></span> <span data-ttu-id="a51f4-111">*src0* ： *src1*</span><span class="sxs-lookup"><span data-stu-id="a51f4-111">*src0* : *src1*</span></span><br/> |
| <span data-ttu-id="a51f4-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="a51f4-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="a51f4-113">\[在 \] [要與 *src1* 比較的值] 中。</span><span class="sxs-lookup"><span data-stu-id="a51f4-113">\[in\] The value to compare to *src1*.</span></span><br/>                                                       |
| <span data-ttu-id="a51f4-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="a51f4-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="a51f4-115">\[在 \] [要與 *src0* 比較的值] 中。</span><span class="sxs-lookup"><span data-stu-id="a51f4-115">\[in\] The value to compare to *src0*.</span></span><br/>                                                       |



 

## <a name="remarks"></a><span data-ttu-id="a51f4-116">備註</span><span class="sxs-lookup"><span data-stu-id="a51f4-116">Remarks</span></span>

<span data-ttu-id="a51f4-117">在執行作業之前，來源運算元上的選擇性否定修飾詞會採用2的補數。</span><span class="sxs-lookup"><span data-stu-id="a51f4-117">Optional negate modifier on source operands takes 2's complement before performing operation.</span></span>

<span data-ttu-id="a51f4-118">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="a51f4-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="a51f4-119">頂點著色器</span><span class="sxs-lookup"><span data-stu-id="a51f4-119">Vertex Shader</span></span> | <span data-ttu-id="a51f4-120">幾何著色器</span><span class="sxs-lookup"><span data-stu-id="a51f4-120">Geometry Shader</span></span> | <span data-ttu-id="a51f4-121">像素著色器</span><span class="sxs-lookup"><span data-stu-id="a51f4-121">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="a51f4-122">x</span><span class="sxs-lookup"><span data-stu-id="a51f4-122">x</span></span>             | <span data-ttu-id="a51f4-123">x</span><span class="sxs-lookup"><span data-stu-id="a51f4-123">x</span></span>               | <span data-ttu-id="a51f4-124">x</span><span class="sxs-lookup"><span data-stu-id="a51f4-124">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="a51f4-125">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="a51f4-125">Minimum Shader Model</span></span>

<span data-ttu-id="a51f4-126">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="a51f4-126">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="a51f4-127">著色器模型</span><span class="sxs-lookup"><span data-stu-id="a51f4-127">Shader Model</span></span>                                              | <span data-ttu-id="a51f4-128">支援</span><span class="sxs-lookup"><span data-stu-id="a51f4-128">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="a51f4-129">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="a51f4-129">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="a51f4-130">是</span><span class="sxs-lookup"><span data-stu-id="a51f4-130">yes</span></span>       |
| [<span data-ttu-id="a51f4-131">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="a51f4-131">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="a51f4-132">是</span><span class="sxs-lookup"><span data-stu-id="a51f4-132">yes</span></span>       |
| [<span data-ttu-id="a51f4-133">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="a51f4-133">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="a51f4-134">是</span><span class="sxs-lookup"><span data-stu-id="a51f4-134">yes</span></span>       |
| [<span data-ttu-id="a51f4-135">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="a51f4-135">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="a51f4-136">不可以</span><span class="sxs-lookup"><span data-stu-id="a51f4-136">no</span></span>        |
| [<span data-ttu-id="a51f4-137">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="a51f4-137">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="a51f4-138">不可以</span><span class="sxs-lookup"><span data-stu-id="a51f4-138">no</span></span>        |
| [<span data-ttu-id="a51f4-139">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="a51f4-139">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="a51f4-140">不可以</span><span class="sxs-lookup"><span data-stu-id="a51f4-140">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="a51f4-141">相關主題</span><span class="sxs-lookup"><span data-stu-id="a51f4-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a51f4-142">著色器模型4元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="a51f4-142">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





