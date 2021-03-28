---
title: 'mad (sm4-asm) '
description: 以元件為依據的乘法 add。
ms.assetid: 1C24AF49-AA32-4D3A-8478-C9BAC4FE7D77
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d34823cdb3545f29426117b35903c97c08c5807
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104022807"
---
# <a name="mad-sm4---asm"></a><span data-ttu-id="11354-103">mad (sm4-asm) </span><span class="sxs-lookup"><span data-stu-id="11354-103">mad (sm4 - asm)</span></span>

<span data-ttu-id="11354-104">& 新增的元件的乘積。</span><span class="sxs-lookup"><span data-stu-id="11354-104">Component-wise multiply & add.</span></span>



| <span data-ttu-id="11354-105">： mad \[ \_ sat \] dest \[ . mask \] 、 \[ - \] src0 \[ \_ abs \] \[ . swizzle \] 、 \[ - \] src1 \[ \_ abs \] \[ . swizzle \] 、 \[ - \] src2 收取 \[ \_ abs \] \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="11354-105">:mad\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\], \[-\]src2\[\_abs\]\[.swizzle\]</span></span> |
|-----------------------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="11354-106">項目</span><span class="sxs-lookup"><span data-stu-id="11354-106">Item</span></span>                                                            | <span data-ttu-id="11354-107">描述</span><span class="sxs-lookup"><span data-stu-id="11354-107">Description</span></span>                                                                                  |
|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="11354-108"><span id="dest"></span><span id="DEST"></span>*目標*</span><span class="sxs-lookup"><span data-stu-id="11354-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="11354-109">\[在作業的 \] 結果中。</span><span class="sxs-lookup"><span data-stu-id="11354-109">\[in\] The result of the operation.</span></span><br/> <span data-ttu-id="11354-110">*目的地*  = *src0* \**src1*  + *src2 收取*</span><span class="sxs-lookup"><span data-stu-id="11354-110">*dest* = *src0* \* *src1* + *src2*</span></span><br/> |
| <span data-ttu-id="11354-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="11354-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="11354-112">\[在 \] 被乘數中。</span><span class="sxs-lookup"><span data-stu-id="11354-112">\[in\] The multiplicand.</span></span><br/>                                                          |
| <span data-ttu-id="11354-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="11354-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="11354-114">\[在 \] 乘數中。</span><span class="sxs-lookup"><span data-stu-id="11354-114">\[in\] The multiplier.</span></span><br/>                                                            |
| <span data-ttu-id="11354-115"><span id="src2"></span><span id="SRC2"></span>*src2 收取*</span><span class="sxs-lookup"><span data-stu-id="11354-115"><span id="src2"></span><span id="SRC2"></span>*src2*</span></span><br/> | <span data-ttu-id="11354-116">\[在 \] 加數中。</span><span class="sxs-lookup"><span data-stu-id="11354-116">\[in\] The addend.</span></span><br/>                                                                |



 

## <a name="remarks"></a><span data-ttu-id="11354-117">備註</span><span class="sxs-lookup"><span data-stu-id="11354-117">Remarks</span></span>

<span data-ttu-id="11354-118">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="11354-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="11354-119">頂點著色器</span><span class="sxs-lookup"><span data-stu-id="11354-119">Vertex Shader</span></span> | <span data-ttu-id="11354-120">幾何著色器</span><span class="sxs-lookup"><span data-stu-id="11354-120">Geometry Shader</span></span> | <span data-ttu-id="11354-121">像素著色器</span><span class="sxs-lookup"><span data-stu-id="11354-121">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="11354-122">x</span><span class="sxs-lookup"><span data-stu-id="11354-122">x</span></span>             | <span data-ttu-id="11354-123">x</span><span class="sxs-lookup"><span data-stu-id="11354-123">x</span></span>               | <span data-ttu-id="11354-124">x</span><span class="sxs-lookup"><span data-stu-id="11354-124">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="11354-125">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="11354-125">Minimum Shader Model</span></span>

<span data-ttu-id="11354-126">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="11354-126">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="11354-127">著色器模型</span><span class="sxs-lookup"><span data-stu-id="11354-127">Shader Model</span></span>                                              | <span data-ttu-id="11354-128">支援</span><span class="sxs-lookup"><span data-stu-id="11354-128">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="11354-129">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="11354-129">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="11354-130">是</span><span class="sxs-lookup"><span data-stu-id="11354-130">yes</span></span>       |
| [<span data-ttu-id="11354-131">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="11354-131">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="11354-132">是</span><span class="sxs-lookup"><span data-stu-id="11354-132">yes</span></span>       |
| [<span data-ttu-id="11354-133">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="11354-133">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="11354-134">是</span><span class="sxs-lookup"><span data-stu-id="11354-134">yes</span></span>       |
| [<span data-ttu-id="11354-135">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="11354-135">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="11354-136">不可以</span><span class="sxs-lookup"><span data-stu-id="11354-136">no</span></span>        |
| [<span data-ttu-id="11354-137">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="11354-137">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="11354-138">不可以</span><span class="sxs-lookup"><span data-stu-id="11354-138">no</span></span>        |
| [<span data-ttu-id="11354-139">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="11354-139">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="11354-140">不可以</span><span class="sxs-lookup"><span data-stu-id="11354-140">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="11354-141">相關主題</span><span class="sxs-lookup"><span data-stu-id="11354-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="11354-142">著色器模型4元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="11354-142">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





