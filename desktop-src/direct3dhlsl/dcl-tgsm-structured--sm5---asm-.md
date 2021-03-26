---
title: 'dcl_tgsm_structured (sm5-asm) '
description: 宣告可供計算著色器執行緒群組使用之共用記憶體空間區域的參考。 記憶體會被視為結構的陣列。
ms.assetid: C42CD506-58EB-4740-8403-3F9BF29F0CAE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a639d31c4449a0dfeb152c06b35cfb86c5cc30a
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104990743"
---
# <a name="dcl_tgsm_structured-sm5---asm"></a><span data-ttu-id="3b156-104">dcl \_ tgsm \_ 結構化 (sm5-asm) </span><span class="sxs-lookup"><span data-stu-id="3b156-104">dcl\_tgsm\_structured (sm5 - asm)</span></span>

<span data-ttu-id="3b156-105">宣告可供計算著色器執行緒群組使用之共用記憶體空間區域的參考。</span><span class="sxs-lookup"><span data-stu-id="3b156-105">Declare a reference to a region of shared memory space available to the compute shader s thread group.</span></span> <span data-ttu-id="3b156-106">記憶體會被視為結構的陣列。</span><span class="sxs-lookup"><span data-stu-id="3b156-106">The memory is viewed as an array of structures.</span></span>



| <span data-ttu-id="3b156-107">dcl \_ tgsm \_ 結構化 g \# 、structByteStride、structCount</span><span class="sxs-lookup"><span data-stu-id="3b156-107">dcl\_tgsm\_structured g\#, structByteStride, structCount</span></span> |
|----------------------------------------------------------|



 



| <span data-ttu-id="3b156-108">項目</span><span class="sxs-lookup"><span data-stu-id="3b156-108">Item</span></span>                                                                                                                                   | <span data-ttu-id="3b156-109">描述</span><span class="sxs-lookup"><span data-stu-id="3b156-109">Description</span></span>                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b156-110"><span id="g_"></span><span id="G_"></span>*G\#*</span><span class="sxs-lookup"><span data-stu-id="3b156-110"><span id="g_"></span><span id="G_"></span>*g\#*</span></span><br/>                                                                             | <span data-ttu-id="3b156-111">\[在 \] *structByteStride* \* *structCount* 位元組大小之共用記憶體區塊的參考中。</span><span class="sxs-lookup"><span data-stu-id="3b156-111">\[in\] A reference to a block of shared memory of size *structByteStride* \* *structCount* bytes.</span></span> <br/> |
| <span data-ttu-id="3b156-112"><span id="structByteStride"></span><span id="structbytestride"></span><span id="STRUCTBYTESTRIDE"></span>*structByteStride*</span><span class="sxs-lookup"><span data-stu-id="3b156-112"><span id="structByteStride"></span><span id="structbytestride"></span><span id="STRUCTBYTESTRIDE"></span>*structByteStride*</span></span><br/> | <span data-ttu-id="3b156-113">\[在 \] 結構 stride 中。</span><span class="sxs-lookup"><span data-stu-id="3b156-113">\[in\] The structure stride.</span></span> <span data-ttu-id="3b156-114">這個值是以位元組為單位的單位，而且必須是4的倍數。</span><span class="sxs-lookup"><span data-stu-id="3b156-114">This value is a uint in bytes and must be a multiple of 4.</span></span> <br/>           |
| <span data-ttu-id="3b156-115"><span id="structCount"></span><span id="structcount"></span><span id="STRUCTCOUNT"></span>*structCount*</span><span class="sxs-lookup"><span data-stu-id="3b156-115"><span id="structCount"></span><span id="structcount"></span><span id="STRUCTCOUNT"></span>*structCount*</span></span><br/>                     | <span data-ttu-id="3b156-116">\[\]結構的數目。</span><span class="sxs-lookup"><span data-stu-id="3b156-116">\[in\] The number of structures.</span></span><br/>                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="3b156-117">備註</span><span class="sxs-lookup"><span data-stu-id="3b156-117">Remarks</span></span>

<span data-ttu-id="3b156-118">所有 g 的總儲存空間 \# 必須 <= 每個執行緒群組可用的共用記憶體量（32kB）或 8192 32 位的純量。</span><span class="sxs-lookup"><span data-stu-id="3b156-118">The total storage for all g\# must be <= the amount of shared memory available per thread group, which is 32kB, or 8192 32-bit scalars.</span></span>

<span data-ttu-id="3b156-119">在極端情況下， \# 如果每個 g s 的 *structByteStride* 為4，而 *structCount* 為1，則您可以宣告 8192 total g s。</span><span class="sxs-lookup"><span data-stu-id="3b156-119">In an extreme case, you can declare 8192 total g\# s, if each has a *structByteStride* of 4 and a *structCount* of 1.</span></span>

<span data-ttu-id="3b156-120">相反地，您可以 \# 使用32kB 的結構 stride 和結構計數1來宣告單一 g。</span><span class="sxs-lookup"><span data-stu-id="3b156-120">In the opposite extreme, you can declare a single g\# with a structure stride of 32kB and a structure count of 1.</span></span>

<span data-ttu-id="3b156-121">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="3b156-121">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="3b156-122">頂點</span><span class="sxs-lookup"><span data-stu-id="3b156-122">Vertex</span></span> | <span data-ttu-id="3b156-123">船體</span><span class="sxs-lookup"><span data-stu-id="3b156-123">Hull</span></span> | <span data-ttu-id="3b156-124">網域</span><span class="sxs-lookup"><span data-stu-id="3b156-124">Domain</span></span> | <span data-ttu-id="3b156-125">幾何</span><span class="sxs-lookup"><span data-stu-id="3b156-125">Geometry</span></span> | <span data-ttu-id="3b156-126">像素</span><span class="sxs-lookup"><span data-stu-id="3b156-126">Pixel</span></span> | <span data-ttu-id="3b156-127">計算</span><span class="sxs-lookup"><span data-stu-id="3b156-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | <span data-ttu-id="3b156-128">X</span><span class="sxs-lookup"><span data-stu-id="3b156-128">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="3b156-129">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="3b156-129">Minimum Shader Model</span></span>

<span data-ttu-id="3b156-130">下列著色器模型支援此指令：</span><span class="sxs-lookup"><span data-stu-id="3b156-130">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="3b156-131">著色器模型</span><span class="sxs-lookup"><span data-stu-id="3b156-131">Shader Model</span></span>                                              | <span data-ttu-id="3b156-132">支援</span><span class="sxs-lookup"><span data-stu-id="3b156-132">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="3b156-133">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="3b156-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="3b156-134">是</span><span class="sxs-lookup"><span data-stu-id="3b156-134">yes</span></span>       |
| [<span data-ttu-id="3b156-135">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="3b156-135">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="3b156-136">不可以</span><span class="sxs-lookup"><span data-stu-id="3b156-136">no</span></span>        |
| [<span data-ttu-id="3b156-137">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="3b156-137">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="3b156-138">不可以</span><span class="sxs-lookup"><span data-stu-id="3b156-138">no</span></span>        |
| [<span data-ttu-id="3b156-139">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="3b156-139">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="3b156-140">不可以</span><span class="sxs-lookup"><span data-stu-id="3b156-140">no</span></span>        |
| [<span data-ttu-id="3b156-141">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="3b156-141">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="3b156-142">不可以</span><span class="sxs-lookup"><span data-stu-id="3b156-142">no</span></span>        |
| [<span data-ttu-id="3b156-143">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="3b156-143">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="3b156-144">不可以</span><span class="sxs-lookup"><span data-stu-id="3b156-144">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="3b156-145">相關主題</span><span class="sxs-lookup"><span data-stu-id="3b156-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3b156-146">著色器模型5元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="3b156-146">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





