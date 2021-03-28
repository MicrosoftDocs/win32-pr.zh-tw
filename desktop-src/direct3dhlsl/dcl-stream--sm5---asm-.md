---
title: 'dcl_stream (sm5-asm) '
description: 宣告幾何著色器輸出資料流程。
ms.assetid: 0A8B8AB5-B7B0-46BB-91E8-B2E8E3D64B74
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f46903c3257c280788e91c25700743a23c146fe
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104373906"
---
# <a name="dcl_stream-sm5---asm"></a><span data-ttu-id="5f936-103">dcl \_ 資料流程 (sm5-asm) </span><span class="sxs-lookup"><span data-stu-id="5f936-103">dcl\_stream (sm5 - asm)</span></span>

<span data-ttu-id="5f936-104">宣告幾何著色器輸出資料流程。</span><span class="sxs-lookup"><span data-stu-id="5f936-104">Declare a geometry shader output stream.</span></span>



| <span data-ttu-id="5f936-105">dcl \_ 資料流程 m\#</span><span class="sxs-lookup"><span data-stu-id="5f936-105">dcl\_stream m\#</span></span> |
|-----------------|



 



| <span data-ttu-id="5f936-106">項目</span><span class="sxs-lookup"><span data-stu-id="5f936-106">Item</span></span>                                                       | <span data-ttu-id="5f936-107">描述</span><span class="sxs-lookup"><span data-stu-id="5f936-107">Description</span></span>                             |
|------------------------------------------------------------|-----------------------------------------|
| <span data-ttu-id="5f936-108"><span id="m_"></span><span id="M_"></span>*m\#*</span><span class="sxs-lookup"><span data-stu-id="5f936-108"><span id="m_"></span><span id="M_"></span>*m\#*</span></span><br/> | <span data-ttu-id="5f936-109">\[在 \] Stream 0 中 (m0。m3) 。</span><span class="sxs-lookup"><span data-stu-id="5f936-109">\[in\] Stream 0..3 (m0..m3).</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5f936-110">備註</span><span class="sxs-lookup"><span data-stu-id="5f936-110">Remarks</span></span>

<span data-ttu-id="5f936-111">給定的資料流程只能宣告一次。</span><span class="sxs-lookup"><span data-stu-id="5f936-111">A given stream can only be declared once.</span></span>

<span data-ttu-id="5f936-112">如果未宣告任何資料流程，則會假設資料流程0有輸出和輸出拓撲宣告。</span><span class="sxs-lookup"><span data-stu-id="5f936-112">If no streams are declared, output and output topology declarations are assumed to be for stream 0.</span></span>

<span data-ttu-id="5f936-113">第一個 **dcl \_ 資料流程** 不能出現在任何 **dcl \_ 輸出** 或 **dcl \_ outputTopology** 語句之後。</span><span class="sxs-lookup"><span data-stu-id="5f936-113">The first **dcl\_stream** cannot appear after any **dcl\_output** or **dcl\_outputTopology** statements.</span></span>

<span data-ttu-id="5f936-114">任何 **dcl \_ 資料流程** m 語句之後的任何 **dcl \_ 輸出** 或 **dcl \_ outputToplogy** 語句都會 \# 定義資料流程 m 的輸出 \# 。</span><span class="sxs-lookup"><span data-stu-id="5f936-114">Any **dcl\_output** or **dcl\_outputToplogy** statements after any **dcl\_stream** m\# statement define the outputs for stream m\#.</span></span>

<span data-ttu-id="5f936-115">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="5f936-115">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="5f936-116">頂點</span><span class="sxs-lookup"><span data-stu-id="5f936-116">Vertex</span></span> | <span data-ttu-id="5f936-117">船體</span><span class="sxs-lookup"><span data-stu-id="5f936-117">Hull</span></span> | <span data-ttu-id="5f936-118">網域</span><span class="sxs-lookup"><span data-stu-id="5f936-118">Domain</span></span> | <span data-ttu-id="5f936-119">幾何</span><span class="sxs-lookup"><span data-stu-id="5f936-119">Geometry</span></span> | <span data-ttu-id="5f936-120">像素</span><span class="sxs-lookup"><span data-stu-id="5f936-120">Pixel</span></span> | <span data-ttu-id="5f936-121">計算</span><span class="sxs-lookup"><span data-stu-id="5f936-121">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        | <span data-ttu-id="5f936-122">X</span><span class="sxs-lookup"><span data-stu-id="5f936-122">X</span></span>        |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="5f936-123">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="5f936-123">Minimum Shader Model</span></span>

<span data-ttu-id="5f936-124">下列著色器模型支援此指令：</span><span class="sxs-lookup"><span data-stu-id="5f936-124">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="5f936-125">著色器模型</span><span class="sxs-lookup"><span data-stu-id="5f936-125">Shader Model</span></span>                                              | <span data-ttu-id="5f936-126">支援</span><span class="sxs-lookup"><span data-stu-id="5f936-126">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="5f936-127">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="5f936-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="5f936-128">是</span><span class="sxs-lookup"><span data-stu-id="5f936-128">yes</span></span>       |
| [<span data-ttu-id="5f936-129">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="5f936-129">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="5f936-130">不可以</span><span class="sxs-lookup"><span data-stu-id="5f936-130">no</span></span>        |
| [<span data-ttu-id="5f936-131">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="5f936-131">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="5f936-132">不可以</span><span class="sxs-lookup"><span data-stu-id="5f936-132">no</span></span>        |
| [<span data-ttu-id="5f936-133">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="5f936-133">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="5f936-134">不可以</span><span class="sxs-lookup"><span data-stu-id="5f936-134">no</span></span>        |
| [<span data-ttu-id="5f936-135">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="5f936-135">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="5f936-136">不可以</span><span class="sxs-lookup"><span data-stu-id="5f936-136">no</span></span>        |
| [<span data-ttu-id="5f936-137">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="5f936-137">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="5f936-138">不可以</span><span class="sxs-lookup"><span data-stu-id="5f936-138">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="5f936-139">相關主題</span><span class="sxs-lookup"><span data-stu-id="5f936-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5f936-140">著色器模型5元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="5f936-140">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





