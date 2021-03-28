---
title: 'dcl_thread_group (sm5-asm) '
description: 宣告執行緒群組大小。
ms.assetid: CB8192C4-100D-49B6-94E7-6CD3AEC28149
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8141c80e82f1dfd1ae5a4d360d04fac32ba5221
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104022846"
---
# <a name="dcl_thread_group-sm5---asm"></a><span data-ttu-id="a8025-103">dcl \_ 執行緒 \_ 群組 (sm5-asm) </span><span class="sxs-lookup"><span data-stu-id="a8025-103">dcl\_thread\_group (sm5 - asm)</span></span>

<span data-ttu-id="a8025-104">宣告執行緒群組大小。</span><span class="sxs-lookup"><span data-stu-id="a8025-104">Declare thread group size.</span></span>



| <span data-ttu-id="a8025-105">dcl \_ 執行緒 \_ 群組 x、y、z</span><span class="sxs-lookup"><span data-stu-id="a8025-105">dcl\_thread\_group x, y, z</span></span> |
|----------------------------|



 



| <span data-ttu-id="a8025-106">項目</span><span class="sxs-lookup"><span data-stu-id="a8025-106">Item</span></span>                                                   | <span data-ttu-id="a8025-107">描述</span><span class="sxs-lookup"><span data-stu-id="a8025-107">Description</span></span>                                                        |
|--------------------------------------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="a8025-108"><span id="x"></span><span id="X"></span>*X*</span><span class="sxs-lookup"><span data-stu-id="a8025-108"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="a8025-109">\[在 \] usigned 32 位整數中。</span><span class="sxs-lookup"><span data-stu-id="a8025-109">\[in\] An usigned 32-bit integer.</span></span> <span data-ttu-id="a8025-110">1 <= x <= 1024</span><span class="sxs-lookup"><span data-stu-id="a8025-110">1 <= x <= 1024</span></span> <br/> |
| <span data-ttu-id="a8025-111"><span id="y"></span><span id="Y"></span>*Y*</span><span class="sxs-lookup"><span data-stu-id="a8025-111"><span id="y"></span><span id="Y"></span>*y*</span></span><br/> | <span data-ttu-id="a8025-112">\[在 \] usigned 32 位整數中。</span><span class="sxs-lookup"><span data-stu-id="a8025-112">\[in\] An usigned 32-bit integer.</span></span> <span data-ttu-id="a8025-113">1 <= y <= 1024</span><span class="sxs-lookup"><span data-stu-id="a8025-113">1 <= y <= 1024</span></span><br/>  |
| <span data-ttu-id="a8025-114"><span id="z"></span><span id="Z"></span>*Z*</span><span class="sxs-lookup"><span data-stu-id="a8025-114"><span id="z"></span><span id="Z"></span>*z*</span></span><br/> | <span data-ttu-id="a8025-115">\[在 \] usigned 32 位整數中。</span><span class="sxs-lookup"><span data-stu-id="a8025-115">\[in\] An usigned 32-bit integer.</span></span> <span data-ttu-id="a8025-116">1 <= z <= 64</span><span class="sxs-lookup"><span data-stu-id="a8025-116">1 <= z <= 64</span></span><br/>    |



 

## <a name="remarks"></a><span data-ttu-id="a8025-117">備註</span><span class="sxs-lookup"><span data-stu-id="a8025-117">Remarks</span></span>

<span data-ttu-id="a8025-118">x \* y \* z <= 1024</span><span class="sxs-lookup"><span data-stu-id="a8025-118">x\*y\*z <= 1024</span></span>

<span data-ttu-id="a8025-119">此執行緒群組宣告必須在計算著色器中出現一次。</span><span class="sxs-lookup"><span data-stu-id="a8025-119">This thread group declaration must appear once in a compute shader.</span></span>

<span data-ttu-id="a8025-120">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="a8025-120">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="a8025-121">頂點</span><span class="sxs-lookup"><span data-stu-id="a8025-121">Vertex</span></span> | <span data-ttu-id="a8025-122">船體</span><span class="sxs-lookup"><span data-stu-id="a8025-122">Hull</span></span> | <span data-ttu-id="a8025-123">網域</span><span class="sxs-lookup"><span data-stu-id="a8025-123">Domain</span></span> | <span data-ttu-id="a8025-124">幾何</span><span class="sxs-lookup"><span data-stu-id="a8025-124">Geometry</span></span> | <span data-ttu-id="a8025-125">像素</span><span class="sxs-lookup"><span data-stu-id="a8025-125">Pixel</span></span> | <span data-ttu-id="a8025-126">計算</span><span class="sxs-lookup"><span data-stu-id="a8025-126">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | <span data-ttu-id="a8025-127">X</span><span class="sxs-lookup"><span data-stu-id="a8025-127">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="a8025-128">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="a8025-128">Minimum Shader Model</span></span>

<span data-ttu-id="a8025-129">下列著色器模型支援此指令：</span><span class="sxs-lookup"><span data-stu-id="a8025-129">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="a8025-130">著色器模型</span><span class="sxs-lookup"><span data-stu-id="a8025-130">Shader Model</span></span>                                              | <span data-ttu-id="a8025-131">支援</span><span class="sxs-lookup"><span data-stu-id="a8025-131">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="a8025-132">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="a8025-132">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="a8025-133">是</span><span class="sxs-lookup"><span data-stu-id="a8025-133">yes</span></span>       |
| [<span data-ttu-id="a8025-134">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="a8025-134">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="a8025-135">不可以</span><span class="sxs-lookup"><span data-stu-id="a8025-135">no</span></span>        |
| [<span data-ttu-id="a8025-136">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="a8025-136">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="a8025-137">不可以</span><span class="sxs-lookup"><span data-stu-id="a8025-137">no</span></span>        |
| [<span data-ttu-id="a8025-138">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="a8025-138">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="a8025-139">不可以</span><span class="sxs-lookup"><span data-stu-id="a8025-139">no</span></span>        |
| [<span data-ttu-id="a8025-140">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="a8025-140">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="a8025-141">不可以</span><span class="sxs-lookup"><span data-stu-id="a8025-141">no</span></span>        |
| [<span data-ttu-id="a8025-142">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="a8025-142">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="a8025-143">不可以</span><span class="sxs-lookup"><span data-stu-id="a8025-143">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="a8025-144">相關主題</span><span class="sxs-lookup"><span data-stu-id="a8025-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a8025-145">著色器模型5元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="a8025-145">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





