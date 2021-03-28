---
title: 'umax (sm4-asm) '
description: 元件的不帶正負號的整數最大值。
ms.assetid: 86BCF7A7-99CA-481B-82B4-E0BA30963344
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ceb1fda620facce31132f56ed888d18022ca27ec
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104373790"
---
# <a name="umax-sm4---asm"></a><span data-ttu-id="2588f-103">umax (sm4-asm) </span><span class="sxs-lookup"><span data-stu-id="2588f-103">umax (sm4 - asm)</span></span>

<span data-ttu-id="2588f-104">元件的不帶正負號的整數最大值。</span><span class="sxs-lookup"><span data-stu-id="2588f-104">Component-wise unsigned integer maximum.</span></span>



| <span data-ttu-id="2588f-105">umax dest \[ . mask \] 、src0 \[ . swizzle \] 、src1 \[ . swizzle \] 、</span><span class="sxs-lookup"><span data-stu-id="2588f-105">umax dest\[.mask\], src0\[.swizzle\], src1\[.swizzle\],</span></span> |
|---------------------------------------------------------|



 



| <span data-ttu-id="2588f-106">項目</span><span class="sxs-lookup"><span data-stu-id="2588f-106">Item</span></span>                                                            | <span data-ttu-id="2588f-107">描述</span><span class="sxs-lookup"><span data-stu-id="2588f-107">Description</span></span>                                                                                                            |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2588f-108"><span id="dest"></span><span id="DEST"></span>*目標*</span><span class="sxs-lookup"><span data-stu-id="2588f-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="2588f-109">\[在 \] 操作結果的位址中。</span><span class="sxs-lookup"><span data-stu-id="2588f-109">\[in\] The address of the result of the operation.</span></span><br/> <span data-ttu-id="2588f-110">*目的地*  = *src0*  > *src1* 嗎？</span><span class="sxs-lookup"><span data-stu-id="2588f-110">*dest* = *src0* > *src1* ?</span></span> <span data-ttu-id="2588f-111">*src0* ： *src1*</span><span class="sxs-lookup"><span data-stu-id="2588f-111">*src0* : *src1*</span></span><br/> |
| <span data-ttu-id="2588f-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="2588f-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="2588f-113">\[在 \] [要與 *src1* 比較的值] 中。</span><span class="sxs-lookup"><span data-stu-id="2588f-113">\[in\] The value to compare to *src1*.</span></span><br/>                                                                      |
| <span data-ttu-id="2588f-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="2588f-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="2588f-115">\[在 \] [要與 *src0* 比較的值] 中。</span><span class="sxs-lookup"><span data-stu-id="2588f-115">\[in\] The value to compare to *src0*.</span></span><br/>                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="2588f-116">備註</span><span class="sxs-lookup"><span data-stu-id="2588f-116">Remarks</span></span>

<span data-ttu-id="2588f-117">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="2588f-117">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="2588f-118">頂點著色器</span><span class="sxs-lookup"><span data-stu-id="2588f-118">Vertex Shader</span></span> | <span data-ttu-id="2588f-119">幾何著色器</span><span class="sxs-lookup"><span data-stu-id="2588f-119">Geometry Shader</span></span> | <span data-ttu-id="2588f-120">像素著色器</span><span class="sxs-lookup"><span data-stu-id="2588f-120">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="2588f-121">x</span><span class="sxs-lookup"><span data-stu-id="2588f-121">x</span></span>             | <span data-ttu-id="2588f-122">x</span><span class="sxs-lookup"><span data-stu-id="2588f-122">x</span></span>               | <span data-ttu-id="2588f-123">x</span><span class="sxs-lookup"><span data-stu-id="2588f-123">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="2588f-124">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="2588f-124">Minimum Shader Model</span></span>

<span data-ttu-id="2588f-125">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="2588f-125">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="2588f-126">著色器模型</span><span class="sxs-lookup"><span data-stu-id="2588f-126">Shader Model</span></span>                                              | <span data-ttu-id="2588f-127">支援</span><span class="sxs-lookup"><span data-stu-id="2588f-127">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="2588f-128">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="2588f-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="2588f-129">是</span><span class="sxs-lookup"><span data-stu-id="2588f-129">yes</span></span>       |
| [<span data-ttu-id="2588f-130">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="2588f-130">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="2588f-131">是</span><span class="sxs-lookup"><span data-stu-id="2588f-131">yes</span></span>       |
| [<span data-ttu-id="2588f-132">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="2588f-132">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="2588f-133">是</span><span class="sxs-lookup"><span data-stu-id="2588f-133">yes</span></span>       |
| [<span data-ttu-id="2588f-134">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="2588f-134">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="2588f-135">不可以</span><span class="sxs-lookup"><span data-stu-id="2588f-135">no</span></span>        |
| [<span data-ttu-id="2588f-136">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="2588f-136">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="2588f-137">不可以</span><span class="sxs-lookup"><span data-stu-id="2588f-137">no</span></span>        |
| [<span data-ttu-id="2588f-138">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="2588f-138">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="2588f-139">不可以</span><span class="sxs-lookup"><span data-stu-id="2588f-139">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="2588f-140">相關主題</span><span class="sxs-lookup"><span data-stu-id="2588f-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2588f-141">著色器模型4元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="2588f-141">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





