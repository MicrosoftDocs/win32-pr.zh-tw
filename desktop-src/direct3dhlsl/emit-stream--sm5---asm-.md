---
title: 'emit_stream (sm5-asm) '
description: 將頂點發出至指定的資料流程。
ms.assetid: 5DBB0BEC-6EA4-4C04-A3D2-853E48260226
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f56c2582453d18120e3e95b27af9c7613728fa62
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104373770"
---
# <a name="emit_stream-sm5---asm"></a><span data-ttu-id="d546d-103">發出 \_ stream (sm5-asm) </span><span class="sxs-lookup"><span data-stu-id="d546d-103">emit\_stream (sm5 - asm)</span></span>

<span data-ttu-id="d546d-104">將頂點發出至指定的資料流程。</span><span class="sxs-lookup"><span data-stu-id="d546d-104">Emit a vertex to a given stream.</span></span>



| <span data-ttu-id="d546d-105">發出 \_ 資料流程 streamIndex</span><span class="sxs-lookup"><span data-stu-id="d546d-105">emit\_stream streamIndex</span></span> |
|--------------------------|



 



| <span data-ttu-id="d546d-106">項目</span><span class="sxs-lookup"><span data-stu-id="d546d-106">Item</span></span>                                                                                                               | <span data-ttu-id="d546d-107">描述</span><span class="sxs-lookup"><span data-stu-id="d546d-107">Description</span></span>                         |
|--------------------------------------------------------------------------------------------------------------------|-------------------------------------|
| <span data-ttu-id="d546d-108"><span id="streamIndex"></span><span id="streamindex"></span><span id="STREAMINDEX"></span>*streamIndex*</span><span class="sxs-lookup"><span data-stu-id="d546d-108"><span id="streamIndex"></span><span id="streamindex"></span><span id="STREAMINDEX"></span>*streamIndex*</span></span><br/> | <span data-ttu-id="d546d-109">\[在 \] 資料流程索引中。</span><span class="sxs-lookup"><span data-stu-id="d546d-109">\[in\] The stream index.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d546d-110">備註</span><span class="sxs-lookup"><span data-stu-id="d546d-110">Remarks</span></span>

<span data-ttu-id="d546d-111">這個指令會讓指定資料流程的所有宣告的 o 緩存 \# 器從幾何著色器中讀出，以產生頂點。</span><span class="sxs-lookup"><span data-stu-id="d546d-111">This instruction causes all declared o\# registers for the given stream to be read out of the geometry shader to generate a vertex.</span></span> <span data-ttu-id="d546d-112">Afer 發出，所有資料流程所有輸出暫存器中的所有資料都會變成未初始化，而不只是發出至的資料流程。</span><span class="sxs-lookup"><span data-stu-id="d546d-112">Afer the emit, all data in all output registers for all streams become uninitialized, not just the stream emitted to.</span></span>

<span data-ttu-id="d546d-113">*streamIndex* 必須是宣告資料流程的立即值 \[ 0. 3。 \]</span><span class="sxs-lookup"><span data-stu-id="d546d-113">*streamIndex* must be an immediate value \[0..3\] for a declared stream.</span></span>

<span data-ttu-id="d546d-114">發出多個 **發出的 \_ 資料流程** 呼叫時，會產生基本專案。</span><span class="sxs-lookup"><span data-stu-id="d546d-114">As multiple **emit\_stream** calls are issued, primitives are generated.</span></span>

### <a name="restrictions"></a><span data-ttu-id="d546d-115">限制</span><span class="sxs-lookup"><span data-stu-id="d546d-115">Restrictions</span></span>

-   <span data-ttu-id="d546d-116">**發出 \_ 資料流程** 可能會在幾何著色器中出現任何次數，包括 flow 控制項。</span><span class="sxs-lookup"><span data-stu-id="d546d-116">**emit\_stream** can appear any number of times in a geometry shader, including within flow control.</span></span>
-   <span data-ttu-id="d546d-117">如果尚未宣告資料流程，您必須使用 [發出](emit--sm4---asm-.md) ，而不是 **發出 \_ 資料流程**。</span><span class="sxs-lookup"><span data-stu-id="d546d-117">If streams have not been declared, then you must use [emit](emit--sm4---asm-.md) instead of **emit\_stream**.</span></span>

<span data-ttu-id="d546d-118">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="d546d-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="d546d-119">頂點</span><span class="sxs-lookup"><span data-stu-id="d546d-119">Vertex</span></span> | <span data-ttu-id="d546d-120">船體</span><span class="sxs-lookup"><span data-stu-id="d546d-120">Hull</span></span> | <span data-ttu-id="d546d-121">網域</span><span class="sxs-lookup"><span data-stu-id="d546d-121">Domain</span></span> | <span data-ttu-id="d546d-122">幾何</span><span class="sxs-lookup"><span data-stu-id="d546d-122">Geometry</span></span> | <span data-ttu-id="d546d-123">像素</span><span class="sxs-lookup"><span data-stu-id="d546d-123">Pixel</span></span> | <span data-ttu-id="d546d-124">計算</span><span class="sxs-lookup"><span data-stu-id="d546d-124">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        | <span data-ttu-id="d546d-125">X</span><span class="sxs-lookup"><span data-stu-id="d546d-125">X</span></span>        |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="d546d-126">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="d546d-126">Minimum Shader Model</span></span>

<span data-ttu-id="d546d-127">下列著色器模型支援此指令：</span><span class="sxs-lookup"><span data-stu-id="d546d-127">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="d546d-128">著色器模型</span><span class="sxs-lookup"><span data-stu-id="d546d-128">Shader Model</span></span>                                              | <span data-ttu-id="d546d-129">支援</span><span class="sxs-lookup"><span data-stu-id="d546d-129">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="d546d-130">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="d546d-130">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="d546d-131">是</span><span class="sxs-lookup"><span data-stu-id="d546d-131">yes</span></span>       |
| [<span data-ttu-id="d546d-132">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="d546d-132">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="d546d-133">不可以</span><span class="sxs-lookup"><span data-stu-id="d546d-133">no</span></span>        |
| [<span data-ttu-id="d546d-134">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="d546d-134">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="d546d-135">不可以</span><span class="sxs-lookup"><span data-stu-id="d546d-135">no</span></span>        |
| [<span data-ttu-id="d546d-136">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="d546d-136">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="d546d-137">不可以</span><span class="sxs-lookup"><span data-stu-id="d546d-137">no</span></span>        |
| [<span data-ttu-id="d546d-138">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="d546d-138">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="d546d-139">不可以</span><span class="sxs-lookup"><span data-stu-id="d546d-139">no</span></span>        |
| [<span data-ttu-id="d546d-140">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="d546d-140">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="d546d-141">不可以</span><span class="sxs-lookup"><span data-stu-id="d546d-141">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="d546d-142">相關主題</span><span class="sxs-lookup"><span data-stu-id="d546d-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d546d-143">著色器模型5元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="d546d-143">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





