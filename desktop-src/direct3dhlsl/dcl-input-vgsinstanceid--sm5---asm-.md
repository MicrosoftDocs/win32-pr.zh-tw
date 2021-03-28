---
title: 'dcl_input vGSInstanceID (sm5-asm) '
description: 啟用幾何著色器實例。
ms.assetid: 47B9BAD5-0FFF-4DB7-B34A-7811B8A4F792
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3134a9d372f1fde5457f26235fe9a6a5439c58c1
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104313761"
---
# <a name="dcl_input-vgsinstanceid-sm5---asm"></a><span data-ttu-id="16e6c-103">dcl \_ 輸入 vGSInstanceID (sm5-asm) </span><span class="sxs-lookup"><span data-stu-id="16e6c-103">dcl\_input vGSInstanceID (sm5 - asm)</span></span>

<span data-ttu-id="16e6c-104">啟用幾何著色器實例。</span><span class="sxs-lookup"><span data-stu-id="16e6c-104">Enable geometry shader instancing.</span></span>



| <span data-ttu-id="16e6c-105">dcl \_ 輸入 vGSInstanceID、instanceCount</span><span class="sxs-lookup"><span data-stu-id="16e6c-105">dcl\_input vGSInstanceID, instanceCount</span></span> |
|-----------------------------------------|



 



| <span data-ttu-id="16e6c-106">項目</span><span class="sxs-lookup"><span data-stu-id="16e6c-106">Item</span></span>                                                                                                                       | <span data-ttu-id="16e6c-107">描述</span><span class="sxs-lookup"><span data-stu-id="16e6c-107">Description</span></span>                           |
|----------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <span data-ttu-id="16e6c-108"><span id="vGSInstanceID"></span><span id="vgsinstanceid"></span><span id="VGSINSTANCEID"></span>*vGSInstanceID*</span><span class="sxs-lookup"><span data-stu-id="16e6c-108"><span id="vGSInstanceID"></span><span id="vgsinstanceid"></span><span id="VGSINSTANCEID"></span>*vGSInstanceID*</span></span><br/> | <span data-ttu-id="16e6c-109">\[在 \] 實例識別碼中。</span><span class="sxs-lookup"><span data-stu-id="16e6c-109">\[in\] The instance ID.</span></span><br/>    |
| <span data-ttu-id="16e6c-110"><span id="instanceCount"></span><span id="instancecount"></span><span id="INSTANCECOUNT"></span>*instanceCount*</span><span class="sxs-lookup"><span data-stu-id="16e6c-110"><span id="instanceCount"></span><span id="instancecount"></span><span id="INSTANCECOUNT"></span>*instanceCount*</span></span><br/> | <span data-ttu-id="16e6c-111">\[在 \] 實例計數中。</span><span class="sxs-lookup"><span data-stu-id="16e6c-111">\[in\] The instance count.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="16e6c-112">備註</span><span class="sxs-lookup"><span data-stu-id="16e6c-112">Remarks</span></span>

<span data-ttu-id="16e6c-113">宣告的 *instanceCount* 參數會指定幾何著色器應該針對每個輸入基本類型執行多少個實例。</span><span class="sxs-lookup"><span data-stu-id="16e6c-113">The *instanceCount* parameter of the declaration specifies how many instances the geometry shader should execute for each input primitive.</span></span> <span data-ttu-id="16e6c-114">*InstanceCount* 的最大值是32。</span><span class="sxs-lookup"><span data-stu-id="16e6c-114">The maximum value for *instanceCount* is 32.</span></span>

<span data-ttu-id="16e6c-115">透過 [**dcl \_ maxOutputVertexCount**](dcl-maxoutputvertexcount.md)針對輸出宣告的最大頂點數目，會個別套用至每個實例。</span><span class="sxs-lookup"><span data-stu-id="16e6c-115">The maximum number of vertices declared for output, via [**dcl\_maxOutputVertexCount**](dcl-maxoutputvertexcount.md), applies individually to each instance.</span></span>

<span data-ttu-id="16e6c-116">此宣告中的實例計數（乘以透過 [**\_ maxOutputVertexCount**](dcl-maxoutputvertexcount.md)的每個實例最大頂點計數）必須是 <= 1024。</span><span class="sxs-lookup"><span data-stu-id="16e6c-116">The instance count in this declaration, multiplied by the maximum vertex count per instance via [**dcl\_maxOutputVertexCount**](dcl-maxoutputvertexcount.md), must be <= 1024.</span></span>

<span data-ttu-id="16e6c-117">給定幾何著色器實例可以發出的資料量是1024的最大值，並藉由計算針對輸入所宣告的所有純量，並乘以宣告的輸出頂點計數來進行驗證。</span><span class="sxs-lookup"><span data-stu-id="16e6c-117">The amount of data that a given geometry shader instance can emit is 1024 scalars maximum, validated by counting up all scalars declared for input and multiplying by the declared output vertex count.</span></span>

<span data-ttu-id="16e6c-118">使用幾何著色器實例，可有效地增加每個輸入基本資料可發出的總數據量。</span><span class="sxs-lookup"><span data-stu-id="16e6c-118">Use of geometry shader instancing effectively increases the total amount of data that can be emitted per input primitive.</span></span> <span data-ttu-id="16e6c-119">針對單一實例的1024純量，會產生 \* 單一輸入基本的所有幾何著色器實例之輸出資料的最高 1024 32 純量。</span><span class="sxs-lookup"><span data-stu-id="16e6c-119">1024 scalars for a single instance yields up to 1024\*32 scalars of output data across all geometry shader instances for a single input primitive.</span></span> <span data-ttu-id="16e6c-120">不過，實例越多，每個實例可以發出的頂點就越少。</span><span class="sxs-lookup"><span data-stu-id="16e6c-120">However the more instances, the fewer vertices each instance can emit.</span></span> <span data-ttu-id="16e6c-121">單一實例 (沒有可發出1024頂點的實例) 。</span><span class="sxs-lookup"><span data-stu-id="16e6c-121">A single instance (no instancing) can emit 1024 vertices.</span></span> <span data-ttu-id="16e6c-122">如果您宣告 \* 32 實例，表示每個實例只能輸出 1024/32 = 32 頂點。</span><span class="sxs-lookup"><span data-stu-id="16e6c-122">If you declare \*32 instances it means each instance can only output 1024/32 = 32 vertices.</span></span>

<span data-ttu-id="16e6c-123">幾何著色器實例宣告可讓程式使用獨立的32位整數輸入暫存器 *vGSInstanceID*。</span><span class="sxs-lookup"><span data-stu-id="16e6c-123">The geometry shader instancing declaration makes available to the program a standalone 32-bit integer input register, *vGSInstanceID*.</span></span> <span data-ttu-id="16e6c-124">每個幾何著色器實例都是以 *vGSInstanceID* \[ 0，1，2中包含的值來 \] 識別。</span><span class="sxs-lookup"><span data-stu-id="16e6c-124">Each geometry shader instance is identified by the value contained in *vGSInstanceID* \[0,1,2...\].</span></span>

<span data-ttu-id="16e6c-125">*vGSInstanceID* 不是幾何著色器輸入頂點陣列的一部分 (例如，在輸入三角形) 時，會有3個頂點。</span><span class="sxs-lookup"><span data-stu-id="16e6c-125">*vGSInstanceID* is not part of the geometry shader input vertex array (e.g. 3 vertices when inputting a triangle).</span></span> <span data-ttu-id="16e6c-126">*VGSInstanceID* 註冊本身會有其本身，例如 vPrimitiveID。</span><span class="sxs-lookup"><span data-stu-id="16e6c-126">The *vGSInstanceID* register stands on its own, like vPrimitiveID.</span></span>

<span data-ttu-id="16e6c-127">當每個幾何著色器實例結束時，輸出拓撲中會有隱含的剪下，因此連續的實例不會彼此相依。</span><span class="sxs-lookup"><span data-stu-id="16e6c-127">When each geometry shader instance ends, there is an implicit cut in the output topology, so consecutive instances do not depend on each other.</span></span>

<span data-ttu-id="16e6c-128">雖然硬體可能會以平行方式執行每個幾何著色器實例，但最後的所有實例的輸出會序列化，就像是將 *vGSInstanceID* 從0逐一查看到 *instanceCount*-1 的迴圈中，會在每個實例結束時，將隱含的輸出拓朴剪下。</span><span class="sxs-lookup"><span data-stu-id="16e6c-128">Although hardware may execute each geometry shader instance in parallel, the output of all instances at the end is serialized as if all the instanced geometry shader invocations ran sequentially in a loop iterating *vGSInstanceID* from 0 to *instanceCount*-1, with implicit output topology cuts at the end of each instance.</span></span>

<span data-ttu-id="16e6c-129">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="16e6c-129">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="16e6c-130">頂點</span><span class="sxs-lookup"><span data-stu-id="16e6c-130">Vertex</span></span> | <span data-ttu-id="16e6c-131">船體</span><span class="sxs-lookup"><span data-stu-id="16e6c-131">Hull</span></span> | <span data-ttu-id="16e6c-132">網域</span><span class="sxs-lookup"><span data-stu-id="16e6c-132">Domain</span></span> | <span data-ttu-id="16e6c-133">幾何</span><span class="sxs-lookup"><span data-stu-id="16e6c-133">Geometry</span></span> | <span data-ttu-id="16e6c-134">像素</span><span class="sxs-lookup"><span data-stu-id="16e6c-134">Pixel</span></span> | <span data-ttu-id="16e6c-135">計算</span><span class="sxs-lookup"><span data-stu-id="16e6c-135">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        | <span data-ttu-id="16e6c-136">X</span><span class="sxs-lookup"><span data-stu-id="16e6c-136">X</span></span>        |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="16e6c-137">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="16e6c-137">Minimum Shader Model</span></span>

<span data-ttu-id="16e6c-138">下列著色器模型支援此指令：</span><span class="sxs-lookup"><span data-stu-id="16e6c-138">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="16e6c-139">著色器模型</span><span class="sxs-lookup"><span data-stu-id="16e6c-139">Shader Model</span></span>                                              | <span data-ttu-id="16e6c-140">支援</span><span class="sxs-lookup"><span data-stu-id="16e6c-140">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="16e6c-141">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="16e6c-141">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="16e6c-142">是</span><span class="sxs-lookup"><span data-stu-id="16e6c-142">yes</span></span>       |
| [<span data-ttu-id="16e6c-143">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="16e6c-143">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="16e6c-144">不可以</span><span class="sxs-lookup"><span data-stu-id="16e6c-144">no</span></span>        |
| [<span data-ttu-id="16e6c-145">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="16e6c-145">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="16e6c-146">不可以</span><span class="sxs-lookup"><span data-stu-id="16e6c-146">no</span></span>        |
| [<span data-ttu-id="16e6c-147">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="16e6c-147">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="16e6c-148">不可以</span><span class="sxs-lookup"><span data-stu-id="16e6c-148">no</span></span>        |
| [<span data-ttu-id="16e6c-149">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="16e6c-149">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="16e6c-150">不可以</span><span class="sxs-lookup"><span data-stu-id="16e6c-150">no</span></span>        |
| [<span data-ttu-id="16e6c-151">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="16e6c-151">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="16e6c-152">不可以</span><span class="sxs-lookup"><span data-stu-id="16e6c-152">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="16e6c-153">相關主題</span><span class="sxs-lookup"><span data-stu-id="16e6c-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="16e6c-154">著色器模型5元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="16e6c-154">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





