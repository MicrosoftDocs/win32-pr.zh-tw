---
title: 'ilt (sm4-asm) '
description: 以元件為依據的向量整數小於比較。
ms.assetid: 5F06E568-6234-4778-8169-D8352FAB5297
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2c2e5e47272412bb483e4782e9a6c35e971293c
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104313634"
---
# <a name="ilt-sm4---asm"></a><span data-ttu-id="4b8be-103">ilt (sm4-asm) </span><span class="sxs-lookup"><span data-stu-id="4b8be-103">ilt (sm4 - asm)</span></span>

<span data-ttu-id="4b8be-104">以元件為依據的向量整數小於比較。</span><span class="sxs-lookup"><span data-stu-id="4b8be-104">Component-wise vector integer less-than comparison.</span></span>



| <span data-ttu-id="4b8be-105">ilt dest \[ . mask \] 、src0 \[ . swizzle \] 、src1 \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="4b8be-105">ilt dest\[.mask\], src0\[.swizzle\], src1\[.swizzle\]</span></span> |
|-------------------------------------------------------|



 



| <span data-ttu-id="4b8be-106">項目</span><span class="sxs-lookup"><span data-stu-id="4b8be-106">Item</span></span>                                                            | <span data-ttu-id="4b8be-107">描述</span><span class="sxs-lookup"><span data-stu-id="4b8be-107">Description</span></span>                                       |
|-----------------------------------------------------------------|---------------------------------------------------|
| <span data-ttu-id="4b8be-108"><span id="dest"></span><span id="DEST"></span>*目標*</span><span class="sxs-lookup"><span data-stu-id="4b8be-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="4b8be-109">運算的結果。</span><span class="sxs-lookup"><span data-stu-id="4b8be-109">The result of the operation.</span></span><br/>           |
| <span data-ttu-id="4b8be-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="4b8be-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="4b8be-111">\[在 \] [要與 *src1* 比較的值] 中。</span><span class="sxs-lookup"><span data-stu-id="4b8be-111">\[in\] The value to compare to *src1*.</span></span><br/> |
| <span data-ttu-id="4b8be-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="4b8be-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="4b8be-113">\[在 \] [要與 *src0* 比較的值] 中。</span><span class="sxs-lookup"><span data-stu-id="4b8be-113">\[in\] The value to compare to *src0*.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4b8be-114">備註</span><span class="sxs-lookup"><span data-stu-id="4b8be-114">Remarks</span></span>

<span data-ttu-id="4b8be-115">針對每個元件執行整數比較 *(src0*  <  *src1*) ，然後將結果寫入至 *目的地*。</span><span class="sxs-lookup"><span data-stu-id="4b8be-115">Performs the integer comparison *(src0* < *src1*) for each component, and writes the result to *dest*.</span></span>

<span data-ttu-id="4b8be-116">如果比較結果為 true，則會傳回該元件的0xFFFFFFFF。</span><span class="sxs-lookup"><span data-stu-id="4b8be-116">If the comparison is true, then 0xFFFFFFFF is returned for that component.</span></span> <span data-ttu-id="4b8be-117">否則會傳回0x0000000。</span><span class="sxs-lookup"><span data-stu-id="4b8be-117">Otherwise 0x0000000 is returned.</span></span>

<span data-ttu-id="4b8be-118">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="4b8be-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="4b8be-119">頂點著色器</span><span class="sxs-lookup"><span data-stu-id="4b8be-119">Vertex Shader</span></span> | <span data-ttu-id="4b8be-120">幾何著色器</span><span class="sxs-lookup"><span data-stu-id="4b8be-120">Geometry Shader</span></span> | <span data-ttu-id="4b8be-121">像素著色器</span><span class="sxs-lookup"><span data-stu-id="4b8be-121">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="4b8be-122">x</span><span class="sxs-lookup"><span data-stu-id="4b8be-122">x</span></span>             | <span data-ttu-id="4b8be-123">x</span><span class="sxs-lookup"><span data-stu-id="4b8be-123">x</span></span>               | <span data-ttu-id="4b8be-124">x</span><span class="sxs-lookup"><span data-stu-id="4b8be-124">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="4b8be-125">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="4b8be-125">Minimum Shader Model</span></span>



| <span data-ttu-id="4b8be-126">著色器模型</span><span class="sxs-lookup"><span data-stu-id="4b8be-126">Shader Model</span></span>                                              | <span data-ttu-id="4b8be-127">支援</span><span class="sxs-lookup"><span data-stu-id="4b8be-127">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="4b8be-128">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="4b8be-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="4b8be-129">是</span><span class="sxs-lookup"><span data-stu-id="4b8be-129">yes</span></span>       |
| [<span data-ttu-id="4b8be-130">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="4b8be-130">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="4b8be-131">是</span><span class="sxs-lookup"><span data-stu-id="4b8be-131">yes</span></span>       |
| [<span data-ttu-id="4b8be-132">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="4b8be-132">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="4b8be-133">是</span><span class="sxs-lookup"><span data-stu-id="4b8be-133">yes</span></span>       |
| [<span data-ttu-id="4b8be-134">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="4b8be-134">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="4b8be-135">不可以</span><span class="sxs-lookup"><span data-stu-id="4b8be-135">no</span></span>        |
| [<span data-ttu-id="4b8be-136">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="4b8be-136">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="4b8be-137">不可以</span><span class="sxs-lookup"><span data-stu-id="4b8be-137">no</span></span>        |
| [<span data-ttu-id="4b8be-138">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="4b8be-138">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="4b8be-139">不可以</span><span class="sxs-lookup"><span data-stu-id="4b8be-139">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="4b8be-140">相關主題</span><span class="sxs-lookup"><span data-stu-id="4b8be-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4b8be-141">著色器模型4元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="4b8be-141">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





