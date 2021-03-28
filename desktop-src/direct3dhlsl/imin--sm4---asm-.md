---
title: 'imin (sm4-asm) '
description: 最小元件的整數。
ms.assetid: 8EDD5503-76D5-4078-BFBA-1DA9260C6E68
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 942384e7a988e4919a483e09c75e476d5a6917ba
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104373858"
---
# <a name="imin-sm4---asm"></a><span data-ttu-id="e1b1e-103">imin (sm4-asm) </span><span class="sxs-lookup"><span data-stu-id="e1b1e-103">imin (sm4 - asm)</span></span>

<span data-ttu-id="e1b1e-104">最小元件的整數。</span><span class="sxs-lookup"><span data-stu-id="e1b1e-104">Component-wise integer minimum.</span></span>



| <span data-ttu-id="e1b1e-105">imin dest \[ . mask \] 、 \[  - \] src0 \[ . swizzle \] 、 \[ - \] src1 \[ . swizzle \] 、</span><span class="sxs-lookup"><span data-stu-id="e1b1e-105">imin dest\[.mask\], \[ -\]src0\[.swizzle\], \[-\]src1\[.swizzle\],</span></span> |
|--------------------------------------------------------------------|



 



| <span data-ttu-id="e1b1e-106">項目</span><span class="sxs-lookup"><span data-stu-id="e1b1e-106">Item</span></span>                                                            | <span data-ttu-id="e1b1e-107">描述</span><span class="sxs-lookup"><span data-stu-id="e1b1e-107">Description</span></span>                                                                                             |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1b1e-108"><span id="dest"></span><span id="DEST"></span>*目標*</span><span class="sxs-lookup"><span data-stu-id="e1b1e-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="e1b1e-109">\[在作業的 \] 結果中。</span><span class="sxs-lookup"><span data-stu-id="e1b1e-109">\[in\] The result of the operation.</span></span><br/> <span data-ttu-id="e1b1e-110">*目的地*  = *src0*  < *src1* 嗎？</span><span class="sxs-lookup"><span data-stu-id="e1b1e-110">*dest* = *src0* < *src1* ?</span></span> <span data-ttu-id="e1b1e-111">*src0* ： *src1*</span><span class="sxs-lookup"><span data-stu-id="e1b1e-111">*src0* : *src1*</span></span><br/> |
| <span data-ttu-id="e1b1e-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="e1b1e-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="e1b1e-113">\[在 \] [要與 *src1* 比較的值] 中。</span><span class="sxs-lookup"><span data-stu-id="e1b1e-113">\[in\] The value to compare to *src1*.</span></span><br/>                                                       |
| <span data-ttu-id="e1b1e-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="e1b1e-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="e1b1e-115">\[在 \] [要與 *src0* 比較的值] 中。</span><span class="sxs-lookup"><span data-stu-id="e1b1e-115">\[in\] The value to compare to *src0*.</span></span><br/>                                                       |



 

## <a name="remarks"></a><span data-ttu-id="e1b1e-116">備註</span><span class="sxs-lookup"><span data-stu-id="e1b1e-116">Remarks</span></span>

<span data-ttu-id="e1b1e-117">在執行作業之前，來源運算元上的選擇性否定修飾詞會採用2的補數。</span><span class="sxs-lookup"><span data-stu-id="e1b1e-117">Optional negate modifier on source operands takes 2's complement before performing operation.</span></span>

<span data-ttu-id="e1b1e-118">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="e1b1e-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="e1b1e-119">頂點著色器</span><span class="sxs-lookup"><span data-stu-id="e1b1e-119">Vertex Shader</span></span> | <span data-ttu-id="e1b1e-120">幾何著色器</span><span class="sxs-lookup"><span data-stu-id="e1b1e-120">Geometry Shader</span></span> | <span data-ttu-id="e1b1e-121">像素著色器</span><span class="sxs-lookup"><span data-stu-id="e1b1e-121">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="e1b1e-122">x</span><span class="sxs-lookup"><span data-stu-id="e1b1e-122">x</span></span>             | <span data-ttu-id="e1b1e-123">x</span><span class="sxs-lookup"><span data-stu-id="e1b1e-123">x</span></span>               | <span data-ttu-id="e1b1e-124">x</span><span class="sxs-lookup"><span data-stu-id="e1b1e-124">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="e1b1e-125">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="e1b1e-125">Minimum Shader Model</span></span>

<span data-ttu-id="e1b1e-126">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="e1b1e-126">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="e1b1e-127">著色器模型</span><span class="sxs-lookup"><span data-stu-id="e1b1e-127">Shader Model</span></span>                                              | <span data-ttu-id="e1b1e-128">支援</span><span class="sxs-lookup"><span data-stu-id="e1b1e-128">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="e1b1e-129">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="e1b1e-129">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="e1b1e-130">是</span><span class="sxs-lookup"><span data-stu-id="e1b1e-130">yes</span></span>       |
| [<span data-ttu-id="e1b1e-131">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="e1b1e-131">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="e1b1e-132">是</span><span class="sxs-lookup"><span data-stu-id="e1b1e-132">yes</span></span>       |
| [<span data-ttu-id="e1b1e-133">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="e1b1e-133">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="e1b1e-134">是</span><span class="sxs-lookup"><span data-stu-id="e1b1e-134">yes</span></span>       |
| [<span data-ttu-id="e1b1e-135">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="e1b1e-135">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="e1b1e-136">不可以</span><span class="sxs-lookup"><span data-stu-id="e1b1e-136">no</span></span>        |
| [<span data-ttu-id="e1b1e-137">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="e1b1e-137">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="e1b1e-138">不可以</span><span class="sxs-lookup"><span data-stu-id="e1b1e-138">no</span></span>        |
| [<span data-ttu-id="e1b1e-139">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="e1b1e-139">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="e1b1e-140">不可以</span><span class="sxs-lookup"><span data-stu-id="e1b1e-140">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="e1b1e-141">相關主題</span><span class="sxs-lookup"><span data-stu-id="e1b1e-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e1b1e-142">著色器模型4元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="e1b1e-142">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





