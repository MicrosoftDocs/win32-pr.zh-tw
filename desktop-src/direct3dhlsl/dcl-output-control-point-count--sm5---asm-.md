---
title: 'dcl_output_control_point_count (sm5-asm) '
description: 宣告輪廓著色器輸出控制點計數。
ms.assetid: 51E8117F-1802-413B-9820-04D5CEBE2DB6
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 147f8f7021252f07cdb6dd0f225555ff0f23d54b
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104022858"
---
# <a name="dcl_output_control_point_count-sm5---asm"></a><span data-ttu-id="d8b3b-103">dcl \_ 輸出 \_ 控制 \_ 點 \_ 計數 (sm5-asm) </span><span class="sxs-lookup"><span data-stu-id="d8b3b-103">dcl\_output\_control\_point\_count (sm5 - asm)</span></span>

<span data-ttu-id="d8b3b-104">宣告輪廓著色器輸出控制點計數。</span><span class="sxs-lookup"><span data-stu-id="d8b3b-104">Declares the hull shader output control point count.</span></span>



| <span data-ttu-id="d8b3b-105">dcl \_ 輸出 \_ 控制 \_ 點 \_ 計數 N</span><span class="sxs-lookup"><span data-stu-id="d8b3b-105">dcl\_output\_control\_point\_count N</span></span> |
|--------------------------------------|



 



| <span data-ttu-id="d8b3b-106">項目</span><span class="sxs-lookup"><span data-stu-id="d8b3b-106">Item</span></span>                                                   | <span data-ttu-id="d8b3b-107">描述</span><span class="sxs-lookup"><span data-stu-id="d8b3b-107">Description</span></span>                                                                                    |
|--------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8b3b-108"><span id="N"></span><span id="n"></span>*N-1*</span><span class="sxs-lookup"><span data-stu-id="d8b3b-108"><span id="N"></span><span id="n"></span>*N*</span></span><br/> | <span data-ttu-id="d8b3b-109">\[\]從0到32的整數值，指定輸出控制點計數。</span><span class="sxs-lookup"><span data-stu-id="d8b3b-109">\[in\] An integer value from 0 to 32 that specifies the output control point count.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d8b3b-110">備註</span><span class="sxs-lookup"><span data-stu-id="d8b3b-110">Remarks</span></span>

<span data-ttu-id="d8b3b-111">如果不需要，輪廓著色器可以輸出0個控制點。</span><span class="sxs-lookup"><span data-stu-id="d8b3b-111">The hull shader can output 0 control points if they are not needed.</span></span>

<span data-ttu-id="d8b3b-112">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="d8b3b-112">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="d8b3b-113">頂點</span><span class="sxs-lookup"><span data-stu-id="d8b3b-113">Vertex</span></span> | <span data-ttu-id="d8b3b-114">船體</span><span class="sxs-lookup"><span data-stu-id="d8b3b-114">Hull</span></span>                 | <span data-ttu-id="d8b3b-115">網域</span><span class="sxs-lookup"><span data-stu-id="d8b3b-115">Domain</span></span> | <span data-ttu-id="d8b3b-116">幾何</span><span class="sxs-lookup"><span data-stu-id="d8b3b-116">Geometry</span></span> | <span data-ttu-id="d8b3b-117">像素</span><span class="sxs-lookup"><span data-stu-id="d8b3b-117">Pixel</span></span> | <span data-ttu-id="d8b3b-118">計算</span><span class="sxs-lookup"><span data-stu-id="d8b3b-118">Compute</span></span> |
|--------|----------------------|--------|----------|-------|---------|
|        | <span data-ttu-id="d8b3b-119">宣告區段</span><span class="sxs-lookup"><span data-stu-id="d8b3b-119">Declarations Section</span></span> |        |          |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="d8b3b-120">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="d8b3b-120">Minimum Shader Model</span></span>

<span data-ttu-id="d8b3b-121">下列著色器模型支援此指令：</span><span class="sxs-lookup"><span data-stu-id="d8b3b-121">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="d8b3b-122">著色器模型</span><span class="sxs-lookup"><span data-stu-id="d8b3b-122">Shader Model</span></span>                                              | <span data-ttu-id="d8b3b-123">支援</span><span class="sxs-lookup"><span data-stu-id="d8b3b-123">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="d8b3b-124">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="d8b3b-124">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="d8b3b-125">是</span><span class="sxs-lookup"><span data-stu-id="d8b3b-125">yes</span></span>       |
| [<span data-ttu-id="d8b3b-126">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="d8b3b-126">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="d8b3b-127">不可以</span><span class="sxs-lookup"><span data-stu-id="d8b3b-127">no</span></span>        |
| [<span data-ttu-id="d8b3b-128">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="d8b3b-128">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="d8b3b-129">不可以</span><span class="sxs-lookup"><span data-stu-id="d8b3b-129">no</span></span>        |
| [<span data-ttu-id="d8b3b-130">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="d8b3b-130">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="d8b3b-131">不可以</span><span class="sxs-lookup"><span data-stu-id="d8b3b-131">no</span></span>        |
| [<span data-ttu-id="d8b3b-132">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="d8b3b-132">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="d8b3b-133">不可以</span><span class="sxs-lookup"><span data-stu-id="d8b3b-133">no</span></span>        |
| [<span data-ttu-id="d8b3b-134">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="d8b3b-134">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="d8b3b-135">不可以</span><span class="sxs-lookup"><span data-stu-id="d8b3b-135">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="d8b3b-136">相關主題</span><span class="sxs-lookup"><span data-stu-id="d8b3b-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d8b3b-137">著色器模型5元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="d8b3b-137">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





