---
title: 'dp2 (sm4-asm) '
description: 二維向量點-元件 rg、POS swizzle 的乘積。
ms.assetid: E35F6A8B-6D8E-4660-B0F3-95B76BC19229
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4073def6cb315dc0268d1ce8e3f28039b9b2a69
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104373742"
---
# <a name="dp2-sm4---asm"></a><span data-ttu-id="76feb-103">dp2 (sm4-asm) </span><span class="sxs-lookup"><span data-stu-id="76feb-103">dp2 (sm4 - asm)</span></span>

<span data-ttu-id="76feb-104">二維向量點-元件 rg、POS swizzle 的乘積。</span><span class="sxs-lookup"><span data-stu-id="76feb-104">2-dimensional vector dot-product of components rg, POS-swizzle.</span></span>



| <span data-ttu-id="76feb-105">dp2 \[ \_ sat \] dest \[ . mask \] ， \[ - \] src0 \[ \_ abs \] \[ . swizzle \] ， \[ - \] src1 \[ \_ abs \] \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="76feb-105">dp2\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\]</span></span> |
|--------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="76feb-106">項目</span><span class="sxs-lookup"><span data-stu-id="76feb-106">Item</span></span>                                                            | <span data-ttu-id="76feb-107">描述</span><span class="sxs-lookup"><span data-stu-id="76feb-107">Description</span></span>                                                                                                                    |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="76feb-108"><span id="dest"></span><span id="DEST"></span>*目標*</span><span class="sxs-lookup"><span data-stu-id="76feb-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="76feb-109">\[在 \] 操作結果的位址中。</span><span class="sxs-lookup"><span data-stu-id="76feb-109">\[in\] The address of the result of the operation.</span></span> <br/> <span data-ttu-id="76feb-110">*目的地*  = *src0. r* \* *src1. r*  +  *src0.* g \* *src1. g*</span><span class="sxs-lookup"><span data-stu-id="76feb-110">*dest* = *src0.r* \* *src1.r* + *src0.g* \* *src1.g*</span></span><br/> |
| <span data-ttu-id="76feb-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="76feb-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="76feb-112">\[在作業 \] 的元件中。</span><span class="sxs-lookup"><span data-stu-id="76feb-112">\[in\] The components in the operation.</span></span><br/>                                                                             |
| <span data-ttu-id="76feb-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="76feb-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="76feb-114">\[在作業 \] 的元件中。</span><span class="sxs-lookup"><span data-stu-id="76feb-114">\[in\] The components in the operation.</span></span><br/>                                                                             |



 

## <a name="remarks"></a><span data-ttu-id="76feb-115">備註</span><span class="sxs-lookup"><span data-stu-id="76feb-115">Remarks</span></span>

<span data-ttu-id="76feb-116">純量結果已複寫至寫入遮罩中的元件。</span><span class="sxs-lookup"><span data-stu-id="76feb-116">Scalar result replicated to components in write mask.</span></span>

<span data-ttu-id="76feb-117">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="76feb-117">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="76feb-118">頂點著色器</span><span class="sxs-lookup"><span data-stu-id="76feb-118">Vertex Shader</span></span> | <span data-ttu-id="76feb-119">幾何著色器</span><span class="sxs-lookup"><span data-stu-id="76feb-119">Geometry Shader</span></span> | <span data-ttu-id="76feb-120">像素著色器</span><span class="sxs-lookup"><span data-stu-id="76feb-120">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="76feb-121">x</span><span class="sxs-lookup"><span data-stu-id="76feb-121">x</span></span>             | <span data-ttu-id="76feb-122">x</span><span class="sxs-lookup"><span data-stu-id="76feb-122">x</span></span>               | <span data-ttu-id="76feb-123">x</span><span class="sxs-lookup"><span data-stu-id="76feb-123">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="76feb-124">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="76feb-124">Minimum Shader Model</span></span>

<span data-ttu-id="76feb-125">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="76feb-125">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="76feb-126">著色器模型</span><span class="sxs-lookup"><span data-stu-id="76feb-126">Shader Model</span></span>                                              | <span data-ttu-id="76feb-127">支援</span><span class="sxs-lookup"><span data-stu-id="76feb-127">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="76feb-128">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="76feb-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="76feb-129">是</span><span class="sxs-lookup"><span data-stu-id="76feb-129">yes</span></span>       |
| [<span data-ttu-id="76feb-130">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="76feb-130">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="76feb-131">是</span><span class="sxs-lookup"><span data-stu-id="76feb-131">yes</span></span>       |
| [<span data-ttu-id="76feb-132">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="76feb-132">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="76feb-133">是</span><span class="sxs-lookup"><span data-stu-id="76feb-133">yes</span></span>       |
| [<span data-ttu-id="76feb-134">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="76feb-134">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="76feb-135">不可以</span><span class="sxs-lookup"><span data-stu-id="76feb-135">no</span></span>        |
| [<span data-ttu-id="76feb-136">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="76feb-136">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="76feb-137">不可以</span><span class="sxs-lookup"><span data-stu-id="76feb-137">no</span></span>        |
| [<span data-ttu-id="76feb-138">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="76feb-138">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="76feb-139">不可以</span><span class="sxs-lookup"><span data-stu-id="76feb-139">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="76feb-140">相關主題</span><span class="sxs-lookup"><span data-stu-id="76feb-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="76feb-141">著色器模型4元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="76feb-141">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





