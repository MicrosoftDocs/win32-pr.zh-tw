---
title: 'ieq (sm4-asm) '
description: 元件的向量整數相等比較。
ms.assetid: AD010554-80DC-4D2D-B04C-2638276DDC34
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 579a47ffe38b8322b748f6ba64ce9bbbc26a5bd9
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104990810"
---
# <a name="ieq-sm4---asm"></a><span data-ttu-id="06dd7-103">ieq (sm4-asm) </span><span class="sxs-lookup"><span data-stu-id="06dd7-103">ieq (sm4 - asm)</span></span>

<span data-ttu-id="06dd7-104">元件的向量整數相等比較。</span><span class="sxs-lookup"><span data-stu-id="06dd7-104">Component-wise vector integer equality comparison.</span></span>



| <span data-ttu-id="06dd7-105">dest \[ . mask \] 、src0 \[ . swizzle \] 、src1 \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="06dd7-105">dest\[.mask\], src0\[.swizzle\], src1\[.swizzle\]</span></span> |
|---------------------------------------------------|



 



| <span data-ttu-id="06dd7-106">項目</span><span class="sxs-lookup"><span data-stu-id="06dd7-106">Item</span></span>                                                            | <span data-ttu-id="06dd7-107">描述</span><span class="sxs-lookup"><span data-stu-id="06dd7-107">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="06dd7-108"><span id="dest"></span><span id="DEST"></span>*目標*</span><span class="sxs-lookup"><span data-stu-id="06dd7-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="06dd7-109">\[在 \] 操作結果的位址中。</span><span class="sxs-lookup"><span data-stu-id="06dd7-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="06dd7-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="06dd7-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="06dd7-111">\[在 \] [要與 *src1* 比較的值] 中。</span><span class="sxs-lookup"><span data-stu-id="06dd7-111">\[in\] The value to compare with *src1*.</span></span><br/>           |
| <span data-ttu-id="06dd7-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="06dd7-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="06dd7-113">\[在 \] [要與 *src0* 比較的值] 中。</span><span class="sxs-lookup"><span data-stu-id="06dd7-113">\[in\] The value to compare with *src0*.</span></span><br/>           |



 

## <a name="remarks"></a><span data-ttu-id="06dd7-114">備註</span><span class="sxs-lookup"><span data-stu-id="06dd7-114">Remarks</span></span>

<span data-ttu-id="06dd7-115">此指令會針對每個元件執行整數比較 (*src0*  ==  *src1*) ，並將結果寫入至 *目的地*。</span><span class="sxs-lookup"><span data-stu-id="06dd7-115">This instruction performs the integer comparison (*src0* == *src1*) for each component, and writes the result to *dest*.</span></span>

<span data-ttu-id="06dd7-116">如果比較結果為 true，則會傳回該元件的0xFFFFFFFF。</span><span class="sxs-lookup"><span data-stu-id="06dd7-116">If the comparison is true, then 0xFFFFFFFF is returned for that component.</span></span> <span data-ttu-id="06dd7-117">否則會傳回0x0000000</span><span class="sxs-lookup"><span data-stu-id="06dd7-117">Otherwise 0x0000000 is returned</span></span>

<span data-ttu-id="06dd7-118">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="06dd7-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="06dd7-119">頂點著色器</span><span class="sxs-lookup"><span data-stu-id="06dd7-119">Vertex Shader</span></span> | <span data-ttu-id="06dd7-120">幾何著色器</span><span class="sxs-lookup"><span data-stu-id="06dd7-120">Geometry Shader</span></span> | <span data-ttu-id="06dd7-121">像素著色器</span><span class="sxs-lookup"><span data-stu-id="06dd7-121">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="06dd7-122">x</span><span class="sxs-lookup"><span data-stu-id="06dd7-122">x</span></span>             | <span data-ttu-id="06dd7-123">x</span><span class="sxs-lookup"><span data-stu-id="06dd7-123">x</span></span>               | <span data-ttu-id="06dd7-124">x</span><span class="sxs-lookup"><span data-stu-id="06dd7-124">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="06dd7-125">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="06dd7-125">Minimum Shader Model</span></span>

<span data-ttu-id="06dd7-126">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="06dd7-126">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="06dd7-127">著色器模型</span><span class="sxs-lookup"><span data-stu-id="06dd7-127">Shader Model</span></span>                                              | <span data-ttu-id="06dd7-128">支援</span><span class="sxs-lookup"><span data-stu-id="06dd7-128">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="06dd7-129">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="06dd7-129">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="06dd7-130">是</span><span class="sxs-lookup"><span data-stu-id="06dd7-130">yes</span></span>       |
| [<span data-ttu-id="06dd7-131">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="06dd7-131">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="06dd7-132">是</span><span class="sxs-lookup"><span data-stu-id="06dd7-132">yes</span></span>       |
| [<span data-ttu-id="06dd7-133">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="06dd7-133">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="06dd7-134">是</span><span class="sxs-lookup"><span data-stu-id="06dd7-134">yes</span></span>       |
| [<span data-ttu-id="06dd7-135">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="06dd7-135">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="06dd7-136">不可以</span><span class="sxs-lookup"><span data-stu-id="06dd7-136">no</span></span>        |
| [<span data-ttu-id="06dd7-137">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="06dd7-137">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="06dd7-138">不可以</span><span class="sxs-lookup"><span data-stu-id="06dd7-138">no</span></span>        |
| [<span data-ttu-id="06dd7-139">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="06dd7-139">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="06dd7-140">不可以</span><span class="sxs-lookup"><span data-stu-id="06dd7-140">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="06dd7-141">相關主題</span><span class="sxs-lookup"><span data-stu-id="06dd7-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="06dd7-142">著色器模型4元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="06dd7-142">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





