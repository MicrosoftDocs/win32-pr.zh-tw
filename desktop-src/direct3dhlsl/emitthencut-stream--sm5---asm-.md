---
title: 'emitThenCut_stream (sm5-asm) '
description: '相當於發出命令，後面接著剪下命令。 |emitThenCut_stream (sm5-asm) '
ms.assetid: E9D84647-E29B-4E31-9E95-9F7A173293D4
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ae3129f2a3fb50664a5dbf070c7a1dae9bf5d6e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104973977"
---
# <a name="emitthencut_stream-sm5---asm"></a><span data-ttu-id="a291f-104">emitThenCut \_ stream (sm5-asm) </span><span class="sxs-lookup"><span data-stu-id="a291f-104">emitThenCut\_stream (sm5 - asm)</span></span>

<span data-ttu-id="a291f-105">相當於 [發出](emit--sm4---asm-.md) 命令，後面接著 [剪](cut--sm4---asm-.md) 下命令。</span><span class="sxs-lookup"><span data-stu-id="a291f-105">Equivalent to an [emit](emit--sm4---asm-.md) command followed by a [cut](cut--sm4---asm-.md) command.</span></span>



| <span data-ttu-id="a291f-106">emitThenCut \_ 資料流程 streamIndex</span><span class="sxs-lookup"><span data-stu-id="a291f-106">emitThenCut\_stream streamIndex</span></span> |
|---------------------------------|



 



| <span data-ttu-id="a291f-107">項目</span><span class="sxs-lookup"><span data-stu-id="a291f-107">Item</span></span>                                                                                                               | <span data-ttu-id="a291f-108">描述</span><span class="sxs-lookup"><span data-stu-id="a291f-108">Description</span></span>                         |
|--------------------------------------------------------------------------------------------------------------------|-------------------------------------|
| <span data-ttu-id="a291f-109"><span id="streamIndex"></span><span id="streamindex"></span><span id="STREAMINDEX"></span>*streamIndex*</span><span class="sxs-lookup"><span data-stu-id="a291f-109"><span id="streamIndex"></span><span id="streamindex"></span><span id="STREAMINDEX"></span>*streamIndex*</span></span><br/> | <span data-ttu-id="a291f-110">\[在 \] 資料流程索引中。</span><span class="sxs-lookup"><span data-stu-id="a291f-110">\[in\] The stream index.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a291f-111">備註</span><span class="sxs-lookup"><span data-stu-id="a291f-111">Remarks</span></span>

<span data-ttu-id="a291f-112">當故意輸出拓撲中的最後一個頂點時，此作業會很有用。</span><span class="sxs-lookup"><span data-stu-id="a291f-112">This operation is useful when knowingly outputting the last vertex in a topology.</span></span>

<span data-ttu-id="a291f-113">如果尚未宣告資料流程，您必須使用 [emitThenCut](emitthencut--sm4---asm-.md) ，而不是 **emitThenCut \_ 資料流程**。</span><span class="sxs-lookup"><span data-stu-id="a291f-113">If streams have not been declared, then you must use [emitThenCut](emitthencut--sm4---asm-.md) instead of **emitThenCut\_stream**.</span></span>

<span data-ttu-id="a291f-114">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="a291f-114">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="a291f-115">頂點</span><span class="sxs-lookup"><span data-stu-id="a291f-115">Vertex</span></span> | <span data-ttu-id="a291f-116">船體</span><span class="sxs-lookup"><span data-stu-id="a291f-116">Hull</span></span> | <span data-ttu-id="a291f-117">網域</span><span class="sxs-lookup"><span data-stu-id="a291f-117">Domain</span></span> | <span data-ttu-id="a291f-118">幾何</span><span class="sxs-lookup"><span data-stu-id="a291f-118">Geometry</span></span> | <span data-ttu-id="a291f-119">像素</span><span class="sxs-lookup"><span data-stu-id="a291f-119">Pixel</span></span> | <span data-ttu-id="a291f-120">計算</span><span class="sxs-lookup"><span data-stu-id="a291f-120">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        | <span data-ttu-id="a291f-121">X</span><span class="sxs-lookup"><span data-stu-id="a291f-121">X</span></span>        |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="a291f-122">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="a291f-122">Minimum Shader Model</span></span>

<span data-ttu-id="a291f-123">下列著色器模型支援此指令：</span><span class="sxs-lookup"><span data-stu-id="a291f-123">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="a291f-124">著色器模型</span><span class="sxs-lookup"><span data-stu-id="a291f-124">Shader Model</span></span>                                              | <span data-ttu-id="a291f-125">支援</span><span class="sxs-lookup"><span data-stu-id="a291f-125">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="a291f-126">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="a291f-126">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="a291f-127">是</span><span class="sxs-lookup"><span data-stu-id="a291f-127">yes</span></span>       |
| [<span data-ttu-id="a291f-128">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="a291f-128">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="a291f-129">不可以</span><span class="sxs-lookup"><span data-stu-id="a291f-129">no</span></span>        |
| [<span data-ttu-id="a291f-130">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="a291f-130">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="a291f-131">不可以</span><span class="sxs-lookup"><span data-stu-id="a291f-131">no</span></span>        |
| [<span data-ttu-id="a291f-132">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="a291f-132">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="a291f-133">不可以</span><span class="sxs-lookup"><span data-stu-id="a291f-133">no</span></span>        |
| [<span data-ttu-id="a291f-134">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="a291f-134">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="a291f-135">不可以</span><span class="sxs-lookup"><span data-stu-id="a291f-135">no</span></span>        |
| [<span data-ttu-id="a291f-136">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="a291f-136">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="a291f-137">不可以</span><span class="sxs-lookup"><span data-stu-id="a291f-137">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="a291f-138">相關主題</span><span class="sxs-lookup"><span data-stu-id="a291f-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a291f-139">著色器模型5元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="a291f-139">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





