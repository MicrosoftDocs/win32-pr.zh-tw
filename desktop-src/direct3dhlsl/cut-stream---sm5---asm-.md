---
title: 'cut_stream (sm5-asm) '
description: 幾何著色器指令，會在指定的資料流程上完成目前的基本拓撲，如果已發出任何頂點，並啟動該資料流程上幾何著色器所宣告類型的新拓撲。
ms.assetid: CEFDD13B-34FD-4E9C-94A0-CB8879A7DBDE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4650628d7f6b66130568f885e008a5163a9ee44f
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104373735"
---
# <a name="cut_stream-sm5---asm"></a><span data-ttu-id="19fde-103">剪下 \_ 資料流程 (sm5-asm) </span><span class="sxs-lookup"><span data-stu-id="19fde-103">cut\_stream (sm5 - asm)</span></span>

<span data-ttu-id="19fde-104">幾何著色器指令，會在指定的資料流程上完成目前的基本拓撲，如果已發出任何頂點，並啟動該資料流程上幾何著色器所宣告類型的新拓撲。</span><span class="sxs-lookup"><span data-stu-id="19fde-104">The geometry shader instruction that completes the current primitive topology at the specified stream, if any vertices have been emitted to it, and starts a new topology of the type declared by the geometry shader at that stream.</span></span>



| <span data-ttu-id="19fde-105">剪下 \_ 資料流程 streamIndex</span><span class="sxs-lookup"><span data-stu-id="19fde-105">cut\_stream streamIndex</span></span> |
|-------------------------|



 



| <span data-ttu-id="19fde-106">項目</span><span class="sxs-lookup"><span data-stu-id="19fde-106">Item</span></span>                                                                                                               | <span data-ttu-id="19fde-107">描述</span><span class="sxs-lookup"><span data-stu-id="19fde-107">Description</span></span>                         |
|--------------------------------------------------------------------------------------------------------------------|-------------------------------------|
| <span data-ttu-id="19fde-108"><span id="streamIndex"></span><span id="streamindex"></span><span id="STREAMINDEX"></span>*streamIndex*</span><span class="sxs-lookup"><span data-stu-id="19fde-108"><span id="streamIndex"></span><span id="streamindex"></span><span id="STREAMINDEX"></span>*streamIndex*</span></span><br/> | <span data-ttu-id="19fde-109">\[在 \] 資料流程索引中。</span><span class="sxs-lookup"><span data-stu-id="19fde-109">\[in\] The stream index.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="19fde-110">備註</span><span class="sxs-lookup"><span data-stu-id="19fde-110">Remarks</span></span>

<span data-ttu-id="19fde-111">當執行此指令時，會完成任何先前由幾何著色器調用發出的拓撲。</span><span class="sxs-lookup"><span data-stu-id="19fde-111">When this instruction is executed, any previously emitted topology by the geometry shader invocation is completed.</span></span> <span data-ttu-id="19fde-112">如果未針對先前的基本拓撲發出足夠的頂點，則會捨棄這些頂點。</span><span class="sxs-lookup"><span data-stu-id="19fde-112">If there are not enough vertices emitted for the previous primitive topology, then they are discarded.</span></span> <span data-ttu-id="19fde-113">因為幾何著色器的唯一可用輸出拓撲是 pointlist、linestrip 和 trianglestrip，所以永遠不會有任何剩餘的頂點。</span><span class="sxs-lookup"><span data-stu-id="19fde-113">Because the only available output topologies for the geometry shader are pointlist, linestrip and trianglestrip, there are never any leftover vertices.</span></span>

<span data-ttu-id="19fde-114">*streamIndex* 必須是宣告資料流程的立即值 \[ 0. 3。 \]</span><span class="sxs-lookup"><span data-stu-id="19fde-114">*streamIndex* must be an immediate value \[0..3\] for a declared stream.</span></span>

<span data-ttu-id="19fde-115">在先前的拓撲（如果有的話）完成之後，此指示會使用宣告為幾何著色器輸出的拓撲來開始新的拓撲。</span><span class="sxs-lookup"><span data-stu-id="19fde-115">After the previous topology, if any, is completed, this instruction causes a new topology to begin, using the topology declared as the output for the geometry shader.</span></span>

### <a name="restrictions"></a><span data-ttu-id="19fde-116">限制</span><span class="sxs-lookup"><span data-stu-id="19fde-116">Restrictions</span></span>

-   <span data-ttu-id="19fde-117">此指令僅適用于幾何著色器。</span><span class="sxs-lookup"><span data-stu-id="19fde-117">This instruction applies to the geometry shader only.</span></span>
-   <span data-ttu-id="19fde-118">**剪下 \_ 資料流程** 可能會在幾何著色器中出現任何次數，包括在流程式控制制內。</span><span class="sxs-lookup"><span data-stu-id="19fde-118">**cut\_stream** can appear any number of times in the geometry shader, including within flow control.</span></span>
-   <span data-ttu-id="19fde-119">如果幾何著色器結束且頂點已發出，則會完成其所建立的拓撲，如同剪下 **\_ 資料流程** 指令做為最後一個指令執行一樣。</span><span class="sxs-lookup"><span data-stu-id="19fde-119">If the geometry shader ends and vertices have been emitted, the topology they are building is completed, as if a **cut\_stream** instruction was executed as the last instruction.</span></span>
-   <span data-ttu-id="19fde-120">如果尚未宣告資料流程，您必須使用 [剪](cut--sm4---asm-.md) 下，而不是 **剪下 \_ 資料流程**。</span><span class="sxs-lookup"><span data-stu-id="19fde-120">If streams have not been declared, you must use [cut](cut--sm4---asm-.md) instead of **cut\_stream**.</span></span>

<span data-ttu-id="19fde-121">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="19fde-121">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="19fde-122">頂點</span><span class="sxs-lookup"><span data-stu-id="19fde-122">Vertex</span></span> | <span data-ttu-id="19fde-123">船體</span><span class="sxs-lookup"><span data-stu-id="19fde-123">Hull</span></span> | <span data-ttu-id="19fde-124">網域</span><span class="sxs-lookup"><span data-stu-id="19fde-124">Domain</span></span> | <span data-ttu-id="19fde-125">幾何</span><span class="sxs-lookup"><span data-stu-id="19fde-125">Geometry</span></span> | <span data-ttu-id="19fde-126">像素</span><span class="sxs-lookup"><span data-stu-id="19fde-126">Pixel</span></span> | <span data-ttu-id="19fde-127">計算</span><span class="sxs-lookup"><span data-stu-id="19fde-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        | <span data-ttu-id="19fde-128">X</span><span class="sxs-lookup"><span data-stu-id="19fde-128">X</span></span>        |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="19fde-129">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="19fde-129">Minimum Shader Model</span></span>

<span data-ttu-id="19fde-130">下列著色器模型支援此指令：</span><span class="sxs-lookup"><span data-stu-id="19fde-130">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="19fde-131">著色器模型</span><span class="sxs-lookup"><span data-stu-id="19fde-131">Shader Model</span></span>                                              | <span data-ttu-id="19fde-132">支援</span><span class="sxs-lookup"><span data-stu-id="19fde-132">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="19fde-133">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="19fde-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="19fde-134">是</span><span class="sxs-lookup"><span data-stu-id="19fde-134">yes</span></span>       |
| [<span data-ttu-id="19fde-135">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="19fde-135">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="19fde-136">不可以</span><span class="sxs-lookup"><span data-stu-id="19fde-136">no</span></span>        |
| [<span data-ttu-id="19fde-137">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="19fde-137">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="19fde-138">不可以</span><span class="sxs-lookup"><span data-stu-id="19fde-138">no</span></span>        |
| [<span data-ttu-id="19fde-139">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="19fde-139">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="19fde-140">不可以</span><span class="sxs-lookup"><span data-stu-id="19fde-140">no</span></span>        |
| [<span data-ttu-id="19fde-141">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="19fde-141">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="19fde-142">不可以</span><span class="sxs-lookup"><span data-stu-id="19fde-142">no</span></span>        |
| [<span data-ttu-id="19fde-143">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="19fde-143">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="19fde-144">不可以</span><span class="sxs-lookup"><span data-stu-id="19fde-144">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="19fde-145">相關主題</span><span class="sxs-lookup"><span data-stu-id="19fde-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="19fde-146">著色器模型5元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="19fde-146">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





