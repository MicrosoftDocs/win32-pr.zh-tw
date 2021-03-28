---
title: 'dcl_input_control_point_count (sm5-asm) '
description: 在 [輪廓著色器宣告] 區段中宣告輪廓著色器輸入控制點計數。
ms.assetid: 2E524BF0-3DD0-446A-8437-0CF17B348D83
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f0a674a05bfd66b4c1d94da73958dc68f00fe21
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104373923"
---
# <a name="dcl_input_control_point_count-sm5---asm"></a><span data-ttu-id="ffa62-103">dcl \_ 輸入 \_ 控制 \_ 點 \_ 計數 (sm5-asm) </span><span class="sxs-lookup"><span data-stu-id="ffa62-103">dcl\_input\_control\_point\_count (sm5 - asm)</span></span>

<span data-ttu-id="ffa62-104">在 [輪廓著色器宣告] 區段中宣告輪廓著色器輸入控制點計數。</span><span class="sxs-lookup"><span data-stu-id="ffa62-104">Declare the hull shader input control point count in the hull shader declaration section.</span></span>



| <span data-ttu-id="ffa62-105">dcl \_ 輸入 \_ 控制 \_ 點 \_ 計數 {1 ... 32}</span><span class="sxs-lookup"><span data-stu-id="ffa62-105">dcl\_input\_control\_point\_count {1..32}</span></span> |
|-------------------------------------------|



 



| <span data-ttu-id="ffa62-106">項目</span><span class="sxs-lookup"><span data-stu-id="ffa62-106">Item</span></span>                                                   | <span data-ttu-id="ffa62-107">描述</span><span class="sxs-lookup"><span data-stu-id="ffa62-107">Description</span></span>                                      |
|--------------------------------------------------------|--------------------------------------------------|
| <span data-ttu-id="ffa62-108"><span id="N"></span><span id="n"></span>*N-1*</span><span class="sxs-lookup"><span data-stu-id="ffa62-108"><span id="N"></span><span id="n"></span>*N*</span></span><br/> | <span data-ttu-id="ffa62-109">\[在 \] 輸入控制點計數中。</span><span class="sxs-lookup"><span data-stu-id="ffa62-109">\[in\] The input control point count.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ffa62-110">備註</span><span class="sxs-lookup"><span data-stu-id="ffa62-110">Remarks</span></span>

<span data-ttu-id="ffa62-111">至少需要1個輸入控制點;如果不需要，它可以是空的。</span><span class="sxs-lookup"><span data-stu-id="ffa62-111">At least 1 input control point is required; it can be empty if it is not needed.</span></span>

<span data-ttu-id="ffa62-112">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="ffa62-112">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="ffa62-113">頂點</span><span class="sxs-lookup"><span data-stu-id="ffa62-113">Vertex</span></span> | <span data-ttu-id="ffa62-114">船體</span><span class="sxs-lookup"><span data-stu-id="ffa62-114">Hull</span></span> | <span data-ttu-id="ffa62-115">網域</span><span class="sxs-lookup"><span data-stu-id="ffa62-115">Domain</span></span> | <span data-ttu-id="ffa62-116">幾何</span><span class="sxs-lookup"><span data-stu-id="ffa62-116">Geometry</span></span> | <span data-ttu-id="ffa62-117">像素</span><span class="sxs-lookup"><span data-stu-id="ffa62-117">Pixel</span></span> | <span data-ttu-id="ffa62-118">計算</span><span class="sxs-lookup"><span data-stu-id="ffa62-118">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="ffa62-119">X</span><span class="sxs-lookup"><span data-stu-id="ffa62-119">X</span></span>    |        |          |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="ffa62-120">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="ffa62-120">Minimum Shader Model</span></span>

<span data-ttu-id="ffa62-121">下列著色器模型支援此指令：</span><span class="sxs-lookup"><span data-stu-id="ffa62-121">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="ffa62-122">著色器模型</span><span class="sxs-lookup"><span data-stu-id="ffa62-122">Shader Model</span></span>                                              | <span data-ttu-id="ffa62-123">支援</span><span class="sxs-lookup"><span data-stu-id="ffa62-123">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="ffa62-124">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="ffa62-124">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="ffa62-125">是</span><span class="sxs-lookup"><span data-stu-id="ffa62-125">yes</span></span>       |
| [<span data-ttu-id="ffa62-126">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="ffa62-126">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="ffa62-127">不可以</span><span class="sxs-lookup"><span data-stu-id="ffa62-127">no</span></span>        |
| [<span data-ttu-id="ffa62-128">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="ffa62-128">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="ffa62-129">不可以</span><span class="sxs-lookup"><span data-stu-id="ffa62-129">no</span></span>        |
| [<span data-ttu-id="ffa62-130">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="ffa62-130">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="ffa62-131">不可以</span><span class="sxs-lookup"><span data-stu-id="ffa62-131">no</span></span>        |
| [<span data-ttu-id="ffa62-132">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="ffa62-132">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="ffa62-133">不可以</span><span class="sxs-lookup"><span data-stu-id="ffa62-133">no</span></span>        |
| [<span data-ttu-id="ffa62-134">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="ffa62-134">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="ffa62-135">不可以</span><span class="sxs-lookup"><span data-stu-id="ffa62-135">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="ffa62-136">相關主題</span><span class="sxs-lookup"><span data-stu-id="ffa62-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ffa62-137">著色器模型5元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="ffa62-137">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





