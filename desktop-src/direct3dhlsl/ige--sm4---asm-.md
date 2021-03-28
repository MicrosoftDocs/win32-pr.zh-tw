---
title: 'ige (sm4-asm) '
description: 以元件為依據的向量整數大於或等於比較。
ms.assetid: 3A3225D1-9A3D-4928-9041-38CB6DE16E2A
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8709ebedb054dffe227340f2ccd3de572d92ffce
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104092448"
---
# <a name="ige-sm4---asm"></a><span data-ttu-id="55536-103">ige (sm4-asm) </span><span class="sxs-lookup"><span data-stu-id="55536-103">ige (sm4 - asm)</span></span>

<span data-ttu-id="55536-104">以元件為依據的向量整數大於或等於比較。</span><span class="sxs-lookup"><span data-stu-id="55536-104">Component-wise vector integer greater-than-or-equal comparison.</span></span>



| <span data-ttu-id="55536-105">ige dest \[ . mask \] 、src0 \[ . swizzle \] 、src1 \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="55536-105">ige dest\[.mask\], src0\[.swizzle\], src1\[.swizzle\]</span></span> |
|-------------------------------------------------------|



 



| <span data-ttu-id="55536-106">項目</span><span class="sxs-lookup"><span data-stu-id="55536-106">Item</span></span>                                                            | <span data-ttu-id="55536-107">描述</span><span class="sxs-lookup"><span data-stu-id="55536-107">Description</span></span>                                           |
|-----------------------------------------------------------------|-------------------------------------------------------|
| <span data-ttu-id="55536-108"><span id="dest"></span><span id="DEST"></span>*目標*</span><span class="sxs-lookup"><span data-stu-id="55536-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="55536-109">\[在作業的 \] 結果中。</span><span class="sxs-lookup"><span data-stu-id="55536-109">\[in\] The result of the operation.</span></span><br/>        |
| <span data-ttu-id="55536-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="55536-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="55536-111">\[在 \] 要與 *src1* 比較的元件中。</span><span class="sxs-lookup"><span data-stu-id="55536-111">\[in\] The component to compare to *src1*.</span></span><br/> |
| <span data-ttu-id="55536-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="55536-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="55536-113">\[在 \] 要與 *src0* 比較的元件中。</span><span class="sxs-lookup"><span data-stu-id="55536-113">\[in\] The component to compare to *src0*.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="55536-114">備註</span><span class="sxs-lookup"><span data-stu-id="55536-114">Remarks</span></span>

<span data-ttu-id="55536-115">針對每個元件執行整數比較 (*src0*  >=  *src1*) ，然後將結果寫入至 *目的地*。</span><span class="sxs-lookup"><span data-stu-id="55536-115">Performs the integer comparison (*src0* >= *src1*) for each component, and writes the result to *dest*.</span></span>

<span data-ttu-id="55536-116">如果比較結果為 true，則會傳回該元件的0xFFFFFFFF。</span><span class="sxs-lookup"><span data-stu-id="55536-116">If the comparison is true, then 0xFFFFFFFF is returned for that component.</span></span> <span data-ttu-id="55536-117">否則會傳回0x0000000。</span><span class="sxs-lookup"><span data-stu-id="55536-117">Otherwise 0x0000000 is returned.</span></span>

<span data-ttu-id="55536-118">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="55536-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="55536-119">頂點著色器</span><span class="sxs-lookup"><span data-stu-id="55536-119">Vertex Shader</span></span> | <span data-ttu-id="55536-120">幾何著色器</span><span class="sxs-lookup"><span data-stu-id="55536-120">Geometry Shader</span></span> | <span data-ttu-id="55536-121">像素著色器</span><span class="sxs-lookup"><span data-stu-id="55536-121">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="55536-122">x</span><span class="sxs-lookup"><span data-stu-id="55536-122">x</span></span>             | <span data-ttu-id="55536-123">x</span><span class="sxs-lookup"><span data-stu-id="55536-123">x</span></span>               | <span data-ttu-id="55536-124">x</span><span class="sxs-lookup"><span data-stu-id="55536-124">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="55536-125">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="55536-125">Minimum Shader Model</span></span>

<span data-ttu-id="55536-126">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="55536-126">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="55536-127">著色器模型</span><span class="sxs-lookup"><span data-stu-id="55536-127">Shader Model</span></span>                                              | <span data-ttu-id="55536-128">支援</span><span class="sxs-lookup"><span data-stu-id="55536-128">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="55536-129">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="55536-129">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="55536-130">是</span><span class="sxs-lookup"><span data-stu-id="55536-130">yes</span></span>       |
| [<span data-ttu-id="55536-131">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="55536-131">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="55536-132">是</span><span class="sxs-lookup"><span data-stu-id="55536-132">yes</span></span>       |
| [<span data-ttu-id="55536-133">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="55536-133">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="55536-134">是</span><span class="sxs-lookup"><span data-stu-id="55536-134">yes</span></span>       |
| [<span data-ttu-id="55536-135">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="55536-135">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="55536-136">不可以</span><span class="sxs-lookup"><span data-stu-id="55536-136">no</span></span>        |
| [<span data-ttu-id="55536-137">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="55536-137">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="55536-138">不可以</span><span class="sxs-lookup"><span data-stu-id="55536-138">no</span></span>        |
| [<span data-ttu-id="55536-139">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="55536-139">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="55536-140">不可以</span><span class="sxs-lookup"><span data-stu-id="55536-140">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="55536-141">相關主題</span><span class="sxs-lookup"><span data-stu-id="55536-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="55536-142">著色器模型4元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="55536-142">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





