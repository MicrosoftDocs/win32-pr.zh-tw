---
title: 'dcl_hs_max_tessfactor (sm5-asm) '
description: 宣告修補程式的 maxTessFactor。
ms.assetid: 7EF0FD81-69FE-49F6-95DF-0C452A90A713
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69bd20fc8f4a3687988e8b100975f74016a45ae6
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104990846"
---
# <a name="dcl_hs_max_tessfactor-sm5---asm"></a><span data-ttu-id="5e6b3-103">dcl \_ hs \_ max \_ tessfactor (sm5-asm) </span><span class="sxs-lookup"><span data-stu-id="5e6b3-103">dcl\_hs\_max\_tessfactor (sm5 - asm)</span></span>

<span data-ttu-id="5e6b3-104">宣告修補程式的 maxTessFactor。</span><span class="sxs-lookup"><span data-stu-id="5e6b3-104">Declare the maxTessFactor for the patch.</span></span>



| <span data-ttu-id="5e6b3-105">dcl \_ hs \_ 最大 \_ tessfactor n</span><span class="sxs-lookup"><span data-stu-id="5e6b3-105">dcl\_hs\_max\_tessfactor n</span></span> |
|----------------------------|



 



| <span data-ttu-id="5e6b3-106">項目</span><span class="sxs-lookup"><span data-stu-id="5e6b3-106">Item</span></span>                                                   | <span data-ttu-id="5e6b3-107">描述</span><span class="sxs-lookup"><span data-stu-id="5e6b3-107">Description</span></span>                          |
|--------------------------------------------------------|--------------------------------------|
| <span data-ttu-id="5e6b3-108"><span id="n"></span><span id="N"></span>*n-1*</span><span class="sxs-lookup"><span data-stu-id="5e6b3-108"><span id="n"></span><span id="N"></span>*n*</span></span><br/> | <span data-ttu-id="5e6b3-109">\[在 \] maxTessFactor 中。</span><span class="sxs-lookup"><span data-stu-id="5e6b3-109">\[in\] The maxTessFactor.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5e6b3-110">備註</span><span class="sxs-lookup"><span data-stu-id="5e6b3-110">Remarks</span></span>

<span data-ttu-id="5e6b3-111">MaxTessFactor 是範圍 {1.0 ... 中的 float32 值64.0}。</span><span class="sxs-lookup"><span data-stu-id="5e6b3-111">The maxTessFactor is a float32 value in the range {1.0 ... 64.0}.</span></span>

<span data-ttu-id="5e6b3-112">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="5e6b3-112">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="5e6b3-113">頂點</span><span class="sxs-lookup"><span data-stu-id="5e6b3-113">Vertex</span></span> | <span data-ttu-id="5e6b3-114">船體</span><span class="sxs-lookup"><span data-stu-id="5e6b3-114">Hull</span></span> | <span data-ttu-id="5e6b3-115">網域</span><span class="sxs-lookup"><span data-stu-id="5e6b3-115">Domain</span></span> | <span data-ttu-id="5e6b3-116">幾何</span><span class="sxs-lookup"><span data-stu-id="5e6b3-116">Geometry</span></span> | <span data-ttu-id="5e6b3-117">像素</span><span class="sxs-lookup"><span data-stu-id="5e6b3-117">Pixel</span></span> | <span data-ttu-id="5e6b3-118">計算</span><span class="sxs-lookup"><span data-stu-id="5e6b3-118">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="5e6b3-119">X</span><span class="sxs-lookup"><span data-stu-id="5e6b3-119">X</span></span>    |        |          |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="5e6b3-120">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="5e6b3-120">Minimum Shader Model</span></span>

<span data-ttu-id="5e6b3-121">下列著色器模型支援此指令：</span><span class="sxs-lookup"><span data-stu-id="5e6b3-121">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="5e6b3-122">著色器模型</span><span class="sxs-lookup"><span data-stu-id="5e6b3-122">Shader Model</span></span>                                              | <span data-ttu-id="5e6b3-123">支援</span><span class="sxs-lookup"><span data-stu-id="5e6b3-123">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="5e6b3-124">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="5e6b3-124">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="5e6b3-125">是</span><span class="sxs-lookup"><span data-stu-id="5e6b3-125">yes</span></span>       |
| [<span data-ttu-id="5e6b3-126">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="5e6b3-126">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="5e6b3-127">不可以</span><span class="sxs-lookup"><span data-stu-id="5e6b3-127">no</span></span>        |
| [<span data-ttu-id="5e6b3-128">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="5e6b3-128">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="5e6b3-129">不可以</span><span class="sxs-lookup"><span data-stu-id="5e6b3-129">no</span></span>        |
| [<span data-ttu-id="5e6b3-130">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="5e6b3-130">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="5e6b3-131">不可以</span><span class="sxs-lookup"><span data-stu-id="5e6b3-131">no</span></span>        |
| [<span data-ttu-id="5e6b3-132">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="5e6b3-132">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="5e6b3-133">不可以</span><span class="sxs-lookup"><span data-stu-id="5e6b3-133">no</span></span>        |
| [<span data-ttu-id="5e6b3-134">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="5e6b3-134">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="5e6b3-135">不可以</span><span class="sxs-lookup"><span data-stu-id="5e6b3-135">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="5e6b3-136">相關主題</span><span class="sxs-lookup"><span data-stu-id="5e6b3-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5e6b3-137">著色器模型5元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="5e6b3-137">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





