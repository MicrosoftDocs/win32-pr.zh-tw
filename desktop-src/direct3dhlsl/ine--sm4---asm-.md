---
title: '視窗 (sm4-asm) '
description: 元件的向量整數不等於比較。
ms.assetid: 5BED97D3-8FF6-4F1C-819B-DC8B4A4F2CCA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b74a68cf4b1b3c7473f8264e8b83910f4cb0677
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104990807"
---
# <a name="ine-sm4---asm"></a><span data-ttu-id="5a964-103">視窗 (sm4-asm) </span><span class="sxs-lookup"><span data-stu-id="5a964-103">ine (sm4 - asm)</span></span>

<span data-ttu-id="5a964-104">元件的向量整數不等於比較。</span><span class="sxs-lookup"><span data-stu-id="5a964-104">Component-wise vector integer not-equal comparison.</span></span>



| <span data-ttu-id="5a964-105">視窗 dest \[ . mask \] 、src0 \[ . swizzle \] 、src1 \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="5a964-105">ine dest\[.mask\], src0\[.swizzle\], src1\[.swizzle\]</span></span> |
|-------------------------------------------------------|



 



| <span data-ttu-id="5a964-106">項目</span><span class="sxs-lookup"><span data-stu-id="5a964-106">Item</span></span>                                                            | <span data-ttu-id="5a964-107">描述</span><span class="sxs-lookup"><span data-stu-id="5a964-107">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="5a964-108"><span id="dest"></span><span id="DEST"></span>*目標*</span><span class="sxs-lookup"><span data-stu-id="5a964-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="5a964-109">\[在 \] 操作結果的位址中。</span><span class="sxs-lookup"><span data-stu-id="5a964-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="5a964-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="5a964-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="5a964-111">\[in \] 包含要與 *src1* 比較的值。</span><span class="sxs-lookup"><span data-stu-id="5a964-111">\[in\] Contains the value to compare to *src1*.</span></span><br/>    |
| <span data-ttu-id="5a964-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="5a964-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="5a964-113">\[in \] 包含要與 *src0* 比較的值。</span><span class="sxs-lookup"><span data-stu-id="5a964-113">\[in\] Contains the value to compare to *src0*.</span></span><br/>    |



 

## <a name="remarks"></a><span data-ttu-id="5a964-114">備註</span><span class="sxs-lookup"><span data-stu-id="5a964-114">Remarks</span></span>

<span data-ttu-id="5a964-115">針對每個元件執行整數比較 (*src0* ！ = *src1*) ，並將結果寫入至 *目的地*。</span><span class="sxs-lookup"><span data-stu-id="5a964-115">Performs the integer comparison (*src0* != *src1*) for each component, and writes the result to *dest*.</span></span>

<span data-ttu-id="5a964-116">如果比較結果為 true，則會傳回該元件的0xFFFFFFFF。</span><span class="sxs-lookup"><span data-stu-id="5a964-116">If the comparison is true, then 0xFFFFFFFF is returned for that component.</span></span> <span data-ttu-id="5a964-117">否則會傳回0x0000000</span><span class="sxs-lookup"><span data-stu-id="5a964-117">Otherwise 0x0000000 is returned</span></span>

<span data-ttu-id="5a964-118">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="5a964-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="5a964-119">頂點著色器</span><span class="sxs-lookup"><span data-stu-id="5a964-119">Vertex Shader</span></span> | <span data-ttu-id="5a964-120">幾何著色器</span><span class="sxs-lookup"><span data-stu-id="5a964-120">Geometry Shader</span></span> | <span data-ttu-id="5a964-121">像素著色器</span><span class="sxs-lookup"><span data-stu-id="5a964-121">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="5a964-122">x</span><span class="sxs-lookup"><span data-stu-id="5a964-122">x</span></span>             | <span data-ttu-id="5a964-123">x</span><span class="sxs-lookup"><span data-stu-id="5a964-123">x</span></span>               | <span data-ttu-id="5a964-124">x</span><span class="sxs-lookup"><span data-stu-id="5a964-124">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="5a964-125">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="5a964-125">Minimum Shader Model</span></span>

<span data-ttu-id="5a964-126">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="5a964-126">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="5a964-127">著色器模型</span><span class="sxs-lookup"><span data-stu-id="5a964-127">Shader Model</span></span>                                              | <span data-ttu-id="5a964-128">支援</span><span class="sxs-lookup"><span data-stu-id="5a964-128">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="5a964-129">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="5a964-129">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="5a964-130">是</span><span class="sxs-lookup"><span data-stu-id="5a964-130">yes</span></span>       |
| [<span data-ttu-id="5a964-131">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="5a964-131">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="5a964-132">是</span><span class="sxs-lookup"><span data-stu-id="5a964-132">yes</span></span>       |
| [<span data-ttu-id="5a964-133">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="5a964-133">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="5a964-134">是</span><span class="sxs-lookup"><span data-stu-id="5a964-134">yes</span></span>       |
| [<span data-ttu-id="5a964-135">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="5a964-135">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="5a964-136">不可以</span><span class="sxs-lookup"><span data-stu-id="5a964-136">no</span></span>        |
| [<span data-ttu-id="5a964-137">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="5a964-137">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="5a964-138">不可以</span><span class="sxs-lookup"><span data-stu-id="5a964-138">no</span></span>        |
| [<span data-ttu-id="5a964-139">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="5a964-139">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="5a964-140">不可以</span><span class="sxs-lookup"><span data-stu-id="5a964-140">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="5a964-141">相關主題</span><span class="sxs-lookup"><span data-stu-id="5a964-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5a964-142">著色器模型4元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="5a964-142">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





