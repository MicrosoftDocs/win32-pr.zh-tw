---
title: 'dcl_input vThread (sm5-asm) '
description: 宣告計算著色器輸入識別碼。
ms.assetid: C041863A-32B0-4588-A1A9-E416AF9B723C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbf6a7bb19feef95eae9cc153911407b206fde16
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "103679188"
---
# <a name="dcl_input-vthread-sm5---asm"></a><span data-ttu-id="a592d-103">dcl \_ 輸入 vThread (sm5-asm) </span><span class="sxs-lookup"><span data-stu-id="a592d-103">dcl\_input vThread (sm5 - asm)</span></span>

<span data-ttu-id="a592d-104">宣告計算著色器輸入識別碼。</span><span class="sxs-lookup"><span data-stu-id="a592d-104">Declare compute shader input IDs.</span></span>



| <span data-ttu-id="a592d-105">dcl \_ 輸入 {vThreadID.xyz </span><span class="sxs-lookup"><span data-stu-id="a592d-105">dcl\_input {vThreadID.xyz</span></span>\|<span data-ttu-id="a592d-106">vThreadGroupID.xyz </span><span class="sxs-lookup"><span data-stu-id="a592d-106">vThreadGroupID.xyz</span></span>\| <span data-ttu-id="a592d-107">vThreadIDInGroup.xyz </span><span class="sxs-lookup"><span data-stu-id="a592d-107">vThreadIDInGroup.xyz</span></span>\|<span data-ttu-id="a592d-108">vThreadIDInGroupFlattened}</span><span class="sxs-lookup"><span data-stu-id="a592d-108">vThreadIDInGroupFlattened}</span></span> |
|--------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="a592d-109">項目</span><span class="sxs-lookup"><span data-stu-id="a592d-109">Item</span></span>                                                                                                                                                                                                                                                                                                                                                                          | <span data-ttu-id="a592d-110">描述</span><span class="sxs-lookup"><span data-stu-id="a592d-110">Description</span></span>                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="a592d-111"><span id="vThreadID___vThreadGroupID___vThreadIDInGroup___vThreadIDInGroupFlattened"></span><span id="vthreadid___vthreadgroupid___vthreadidingroup___vthreadidingroupflattened"></span><span id="VTHREADID___VTHREADGROUPID___VTHREADIDINGROUP___VTHREADIDINGROUPFLATTENED"></span>*vThreadID \| vThreadGroupID \| vThreadIDInGroup \| vThreadIDInGroupFlattened*</span><span class="sxs-lookup"><span data-stu-id="a592d-111"><span id="vThreadID___vThreadGroupID___vThreadIDInGroup___vThreadIDInGroupFlattened"></span><span id="vthreadid___vthreadgroupid___vthreadidingroup___vthreadidingroupflattened"></span><span id="VTHREADID___VTHREADGROUPID___VTHREADIDINGROUP___VTHREADIDINGROUPFLATTENED"></span>*vThreadID \| vThreadGroupID \| vThreadIDInGroup \| vThreadIDInGroupFlattened*</span></span><br/> | <span data-ttu-id="a592d-112">\[在 \] 3 個元件的 [不帶正負號 32-位整數識別碼] 值。</span><span class="sxs-lookup"><span data-stu-id="a592d-112">\[in\] The 3-component unsigned 32-bit integer ID value.</span></span><br/> |



 

<span data-ttu-id="a592d-113">在其他著色器階段中， **dcl \_ 輸入** 是現有的宣告。</span><span class="sxs-lookup"><span data-stu-id="a592d-113">**dcl\_input** is an existing declaration in other shader stages.</span></span> <span data-ttu-id="a592d-114">它是在計算著色器中用來宣告不同于計算著色器的3個元件不帶正負號32位整數識別碼值。</span><span class="sxs-lookup"><span data-stu-id="a592d-114">It is used in the compute shader to declare the various 3-component unsigned 32-bit integer ID values unique to the compute shader.</span></span> <span data-ttu-id="a592d-115">這些包括：</span><span class="sxs-lookup"><span data-stu-id="a592d-115">They are:</span></span>

-   <span data-ttu-id="a592d-116">vThreadID.xyz</span><span class="sxs-lookup"><span data-stu-id="a592d-116">vThreadID.xyz</span></span>
-   <span data-ttu-id="a592d-117">vGroupID.xyz</span><span class="sxs-lookup"><span data-stu-id="a592d-117">vGroupID.xyz</span></span>
-   <span data-ttu-id="a592d-118">vThreadIDInGroup.xyz</span><span class="sxs-lookup"><span data-stu-id="a592d-118">vThreadIDInGroup.xyz</span></span>
-   <span data-ttu-id="a592d-119">vThreadIDInGroupFlattened (單一元件) </span><span class="sxs-lookup"><span data-stu-id="a592d-119">vThreadIDInGroupFlattened (single component)</span></span>

<span data-ttu-id="a592d-120">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="a592d-120">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="a592d-121">頂點</span><span class="sxs-lookup"><span data-stu-id="a592d-121">Vertex</span></span> | <span data-ttu-id="a592d-122">船體</span><span class="sxs-lookup"><span data-stu-id="a592d-122">Hull</span></span> | <span data-ttu-id="a592d-123">網域</span><span class="sxs-lookup"><span data-stu-id="a592d-123">Domain</span></span> | <span data-ttu-id="a592d-124">幾何</span><span class="sxs-lookup"><span data-stu-id="a592d-124">Geometry</span></span> | <span data-ttu-id="a592d-125">像素</span><span class="sxs-lookup"><span data-stu-id="a592d-125">Pixel</span></span> | <span data-ttu-id="a592d-126">計算</span><span class="sxs-lookup"><span data-stu-id="a592d-126">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | <span data-ttu-id="a592d-127">X</span><span class="sxs-lookup"><span data-stu-id="a592d-127">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="a592d-128">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="a592d-128">Minimum Shader Model</span></span>

<span data-ttu-id="a592d-129">下列著色器模型支援此指令：</span><span class="sxs-lookup"><span data-stu-id="a592d-129">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="a592d-130">著色器模型</span><span class="sxs-lookup"><span data-stu-id="a592d-130">Shader Model</span></span>                                              | <span data-ttu-id="a592d-131">支援</span><span class="sxs-lookup"><span data-stu-id="a592d-131">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="a592d-132">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="a592d-132">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="a592d-133">是</span><span class="sxs-lookup"><span data-stu-id="a592d-133">yes</span></span>       |
| [<span data-ttu-id="a592d-134">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="a592d-134">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="a592d-135">不可以</span><span class="sxs-lookup"><span data-stu-id="a592d-135">no</span></span>        |
| [<span data-ttu-id="a592d-136">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="a592d-136">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="a592d-137">不可以</span><span class="sxs-lookup"><span data-stu-id="a592d-137">no</span></span>        |
| [<span data-ttu-id="a592d-138">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="a592d-138">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="a592d-139">不可以</span><span class="sxs-lookup"><span data-stu-id="a592d-139">no</span></span>        |
| [<span data-ttu-id="a592d-140">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="a592d-140">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="a592d-141">不可以</span><span class="sxs-lookup"><span data-stu-id="a592d-141">no</span></span>        |
| [<span data-ttu-id="a592d-142">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="a592d-142">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="a592d-143">不可以</span><span class="sxs-lookup"><span data-stu-id="a592d-143">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="a592d-144">相關主題</span><span class="sxs-lookup"><span data-stu-id="a592d-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a592d-145">著色器模型5元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="a592d-145">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





