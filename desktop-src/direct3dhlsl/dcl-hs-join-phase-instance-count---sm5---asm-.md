---
title: 'dcl_hs_join_phase_instance_count (sm5-asm) '
description: 在輪廓著色器聯結階段中宣告聯結階段實例計數。
ms.assetid: 9951B849-0537-4D08-9ADE-8CF6FF51A193
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34c3acc7074170ab4561a54e67668698d58b7ac1
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104373931"
---
# <a name="dcl_hs_join_phase_instance_count-sm5---asm"></a><span data-ttu-id="fa923-103">dcl \_ hs \_ 聯結 \_ 階段 \_ 實例 \_ 計數 (sm5-asm) </span><span class="sxs-lookup"><span data-stu-id="fa923-103">dcl\_hs\_join\_phase\_instance\_count (sm5 - asm)</span></span>

<span data-ttu-id="fa923-104">在輪廓著色器聯結階段中宣告聯結階段實例計數。</span><span class="sxs-lookup"><span data-stu-id="fa923-104">Declare the join phase instance count in a hull shader join phase.</span></span>



| <span data-ttu-id="fa923-105">dcl \_ hs \_ 聯結 \_ 階段 \_ 實例 \_ 計數 {1 ... 最大32位 UINT}</span><span class="sxs-lookup"><span data-stu-id="fa923-105">dcl\_hs\_join\_phase\_instance\_count {1... max 32-bit UINT}</span></span> |
|--------------------------------------------------------------|



 



| <span data-ttu-id="fa923-106">項目</span><span class="sxs-lookup"><span data-stu-id="fa923-106">Item</span></span>                                                   | <span data-ttu-id="fa923-107">描述</span><span class="sxs-lookup"><span data-stu-id="fa923-107">Description</span></span>                           |
|--------------------------------------------------------|---------------------------------------|
| <span data-ttu-id="fa923-108"><span id="N"></span><span id="n"></span>*N-1*</span><span class="sxs-lookup"><span data-stu-id="fa923-108"><span id="N"></span><span id="n"></span>*N*</span></span><br/> | <span data-ttu-id="fa923-109">\[在 \] 實例計數中。</span><span class="sxs-lookup"><span data-stu-id="fa923-109">\[in\] The instance count.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="fa923-110">備註</span><span class="sxs-lookup"><span data-stu-id="fa923-110">Remarks</span></span>

<span data-ttu-id="fa923-111">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="fa923-111">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="fa923-112">頂點</span><span class="sxs-lookup"><span data-stu-id="fa923-112">Vertex</span></span> | <span data-ttu-id="fa923-113">船體</span><span class="sxs-lookup"><span data-stu-id="fa923-113">Hull</span></span> | <span data-ttu-id="fa923-114">網域</span><span class="sxs-lookup"><span data-stu-id="fa923-114">Domain</span></span> | <span data-ttu-id="fa923-115">幾何</span><span class="sxs-lookup"><span data-stu-id="fa923-115">Geometry</span></span> | <span data-ttu-id="fa923-116">像素</span><span class="sxs-lookup"><span data-stu-id="fa923-116">Pixel</span></span> | <span data-ttu-id="fa923-117">計算</span><span class="sxs-lookup"><span data-stu-id="fa923-117">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="fa923-118">X</span><span class="sxs-lookup"><span data-stu-id="fa923-118">X</span></span>    |        |          |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="fa923-119">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="fa923-119">Minimum Shader Model</span></span>

<span data-ttu-id="fa923-120">下列著色器模型支援此指令：</span><span class="sxs-lookup"><span data-stu-id="fa923-120">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="fa923-121">著色器模型</span><span class="sxs-lookup"><span data-stu-id="fa923-121">Shader Model</span></span>                                              | <span data-ttu-id="fa923-122">支援</span><span class="sxs-lookup"><span data-stu-id="fa923-122">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="fa923-123">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="fa923-123">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="fa923-124">是</span><span class="sxs-lookup"><span data-stu-id="fa923-124">yes</span></span>       |
| [<span data-ttu-id="fa923-125">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="fa923-125">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="fa923-126">不可以</span><span class="sxs-lookup"><span data-stu-id="fa923-126">no</span></span>        |
| [<span data-ttu-id="fa923-127">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="fa923-127">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="fa923-128">不可以</span><span class="sxs-lookup"><span data-stu-id="fa923-128">no</span></span>        |
| [<span data-ttu-id="fa923-129">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="fa923-129">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="fa923-130">不可以</span><span class="sxs-lookup"><span data-stu-id="fa923-130">no</span></span>        |
| [<span data-ttu-id="fa923-131">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="fa923-131">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="fa923-132">不可以</span><span class="sxs-lookup"><span data-stu-id="fa923-132">no</span></span>        |
| [<span data-ttu-id="fa923-133">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="fa923-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="fa923-134">不可以</span><span class="sxs-lookup"><span data-stu-id="fa923-134">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="fa923-135">相關主題</span><span class="sxs-lookup"><span data-stu-id="fa923-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fa923-136">著色器模型5元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="fa923-136">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





