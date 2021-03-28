---
title: 'dcl_uav_structured (sm5-asm) '
description: '宣告未排序的存取視圖 (UAV) 供著色器使用。 |dcl_uav_structured (sm5-asm) '
ms.assetid: 40D6B8F7-8A41-4EFE-A8A3-44A646B4D43B
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3dc02396f4837a095506e736d81ea8c00eb0669f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104195954"
---
# <a name="dcl_uav_structured-sm5---asm"></a><span data-ttu-id="654e1-104">dcl \_ uav \_ 結構化 (sm5-asm) </span><span class="sxs-lookup"><span data-stu-id="654e1-104">dcl\_uav\_structured (sm5 - asm)</span></span>

<span data-ttu-id="654e1-105">宣告未排序的存取視圖 (UAV) 供著色器使用。</span><span class="sxs-lookup"><span data-stu-id="654e1-105">Declare an unordered access view (UAV) for use by a shader.</span></span>



| <span data-ttu-id="654e1-106">dcl \_ uav \_ 結構化 \[ \_ glc \] dstUAV、structByteStride</span><span class="sxs-lookup"><span data-stu-id="654e1-106">dcl\_uav\_structured\[\_glc\] dstUAV, structByteStride</span></span> |
|--------------------------------------------------------|



 



| <span data-ttu-id="654e1-107">項目</span><span class="sxs-lookup"><span data-stu-id="654e1-107">Item</span></span>                                                                                                                                   | <span data-ttu-id="654e1-108">描述</span><span class="sxs-lookup"><span data-stu-id="654e1-108">Description</span></span>                                           |
|----------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <span data-ttu-id="654e1-109"><span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*</span><span class="sxs-lookup"><span data-stu-id="654e1-109"><span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*</span></span><br/>                                         | <span data-ttu-id="654e1-110">\[在 \] UAV 中。</span><span class="sxs-lookup"><span data-stu-id="654e1-110">\[in\] The UAV.</span></span><br/>                            |
| <span data-ttu-id="654e1-111"><span id="structByteStride"></span><span id="structbytestride"></span><span id="STRUCTBYTESTRIDE"></span>*structByteStride*</span><span class="sxs-lookup"><span data-stu-id="654e1-111"><span id="structByteStride"></span><span id="structbytestride"></span><span id="STRUCTBYTESTRIDE"></span>*structByteStride*</span></span><br/> | <span data-ttu-id="654e1-112">\[以 \] 位元組為單位的結構大小。</span><span class="sxs-lookup"><span data-stu-id="654e1-112">\[in\] The size of the structure in bytes.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="654e1-113">備註</span><span class="sxs-lookup"><span data-stu-id="654e1-113">Remarks</span></span>

<span data-ttu-id="654e1-114">*dstUAV* 是宣告 \# 為結構化緩衝區 UnorderedAccessView 參考的 u 暫存器，其指定的 stride 必須系結至 API 的 UAV \# 位置。</span><span class="sxs-lookup"><span data-stu-id="654e1-114">*dstUAV* is a u\# register declared as a reference to an UnorderedAccessView of a structured buffer with the specified stride that must be bound to UAV slot \# at the API.</span></span>

<span data-ttu-id="654e1-115">結構的內容沒有類型;在記憶體上執行的作業可能會隱含地將資料解讀為具有類型。</span><span class="sxs-lookup"><span data-stu-id="654e1-115">The contents of the structure have no type; operations performed on the memory may implicitly interpret the data as having a type.</span></span>

<span data-ttu-id="654e1-116">*structByteStride* 是要宣告的緩衝區中的結構大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="654e1-116">*structByteStride* is the size of the structure in bytes in the buffer being declared.</span></span> <span data-ttu-id="654e1-117">這個值必須大於零。</span><span class="sxs-lookup"><span data-stu-id="654e1-117">This value must be greater than zero.</span></span> <span data-ttu-id="654e1-118">*structByteStride* 是 uint 類型，而且必須是4的倍數。</span><span class="sxs-lookup"><span data-stu-id="654e1-118">*structByteStride* is of type uint, and must be a multiple of 4.</span></span>

<span data-ttu-id="654e1-119">參考結構化 u 的指示 \# 會採用2d 位址，其中第一個元件挑選 \[ 結構 \] ，而第二個元件則挑選 \[ 結構內的位移（以對齊的位元組為單位） \] 。</span><span class="sxs-lookup"><span data-stu-id="654e1-119">Instructions that reference a structured u\# take a 2D address, where the first component picks \[struct\], and the second component picks \[offset within struct, in aligned bytes\].</span></span>

<span data-ttu-id="654e1-120">\_Glc 旗標表示「全域一致」。</span><span class="sxs-lookup"><span data-stu-id="654e1-120">The \_glc flag means for"globally coherent".</span></span> <span data-ttu-id="654e1-121">缺少 \_ glc 表示 UAV 在計算著色器中宣告為「群組一致」，或在單一圖元著色器調用中宣告為「本機一致」。</span><span class="sxs-lookup"><span data-stu-id="654e1-121">The absence of \_glc means the UAV is being declared only as "group coherent" in the compute shader, or "locally coherent" in a single pixel shader invocation.</span></span>

<span data-ttu-id="654e1-122">\_Opc 旗標是「訂單保留」計數器。</span><span class="sxs-lookup"><span data-stu-id="654e1-122">The \_opc flag is the order preserving counter.</span></span> <span data-ttu-id="654e1-123">這表示，如果 UAV 系結至 \# (u) 的位置 \# ，則必須使用計數器旗標來建立它。</span><span class="sxs-lookup"><span data-stu-id="654e1-123">It indicates that if a UAV is bound to slot \# (u\#), it must have been created with the COUNTER flag.</span></span> <span data-ttu-id="654e1-124">這表示，在著色器中的 imm 不可部分完成配置或 imm 不可部分完成取用作業會操作一個計數器，其值可以在著色器中當做 UAV 中位置的永久參考[ \_ \_ ](imm-atomic-alloc--sm5---asm-.md)使用。 [ \_ \_ ](imm-atomic-consume--sm5---asm-.md)</span><span class="sxs-lookup"><span data-stu-id="654e1-124">This means that [imm\_atomic\_alloc](imm-atomic-alloc--sm5---asm-.md) or [imm\_atomic\_consume](imm-atomic-consume--sm5---asm-.md) operations in the shader manipulate a counter whose values can be used in the shader as a permanent reference to a location in the UAV.</span></span> <span data-ttu-id="654e1-125">在著色器結束之後，資料無法重新排序。</span><span class="sxs-lookup"><span data-stu-id="654e1-125">Data cannot be reordered after the shader is over.</span></span>

<span data-ttu-id="654e1-126">缺少 \_ opc 旗標表示如果著色器使用了 imm 不可部分完成配置或 imm 不可部分完成的[ \_ \_ 使用](imm-atomic-consume--sm5---asm-.md)指示，且 UAV 系結至 (u) 的位置[ \_ \_ ](imm-atomic-alloc--sm5---asm-.md) \# ，則必須已使用 APPEND 旗標建立此旗標，此旗標提供的計數器不保證會在著色器調用之後保留順序。</span><span class="sxs-lookup"><span data-stu-id="654e1-126">The absence of the \_opc flag means that if the shader uses[imm\_atomic\_alloc](imm-atomic-alloc--sm5---asm-.md) or [imm\_atomic\_consume](imm-atomic-consume--sm5---asm-.md) instructions and a UAV is bound to slot \# (u), it must have been created with the APPEND flag, which provides a counter that does not guarantee order is preserved after the shader invocation.</span></span>

<span data-ttu-id="654e1-127">如果不 \_ 存在 opc 旗標，且著色器未包含 [imm \_ \_ ](imm-atomic-alloc--sm5---asm-.md) 不可部分完成配置或 imm 不可部分完成的 [ \_ \_ 使用](imm-atomic-consume--sm5---asm-.md) 指示，則 \# 會允許使用計數器旗標來建立系結至插槽 (u) 的 UAV， (計數器將不會被此著色器) 、不 (任何旗標) ，但不會使用附加旗標。</span><span class="sxs-lookup"><span data-stu-id="654e1-127">If the \_opc flag is absent and the shader does not contain [imm\_atomic\_alloc](imm-atomic-alloc--sm5---asm-.md) or [imm\_atomic\_consume](imm-atomic-consume--sm5---asm-.md) instructions, a UAV bound to slot \# (u) is permitted to have been created with the COUNTER flag (the counter will go unused by this shader), no flag (no counter), but not with the APPEND flag.</span></span>

> [!Note]  
> <span data-ttu-id="654e1-128">cs \_ 4 \_ 0 和 cs \_ 4 \_ 1 支援 **\_ tgsm \_ 結構化**，但不 [支援 \_ tgsm \_ 原始](dcl-tgsm-raw--sm5---asm-.md)的 dcl。</span><span class="sxs-lookup"><span data-stu-id="654e1-128">cs\_4\_0 and cs\_4\_1 supports **dcl\_tgsm\_structured**, but not [dcl\_tgsm\_raw](dcl-tgsm-raw--sm5---asm-.md).</span></span>

 

<span data-ttu-id="654e1-129">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="654e1-129">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="654e1-130">頂點</span><span class="sxs-lookup"><span data-stu-id="654e1-130">Vertex</span></span> | <span data-ttu-id="654e1-131">船體</span><span class="sxs-lookup"><span data-stu-id="654e1-131">Hull</span></span> | <span data-ttu-id="654e1-132">網域</span><span class="sxs-lookup"><span data-stu-id="654e1-132">Domain</span></span> | <span data-ttu-id="654e1-133">幾何</span><span class="sxs-lookup"><span data-stu-id="654e1-133">Geometry</span></span> | <span data-ttu-id="654e1-134">像素</span><span class="sxs-lookup"><span data-stu-id="654e1-134">Pixel</span></span> | <span data-ttu-id="654e1-135">計算</span><span class="sxs-lookup"><span data-stu-id="654e1-135">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="654e1-136">X</span><span class="sxs-lookup"><span data-stu-id="654e1-136">X</span></span>     | <span data-ttu-id="654e1-137">X</span><span class="sxs-lookup"><span data-stu-id="654e1-137">X</span></span>       |



 

<span data-ttu-id="654e1-138">由於 UAVs 可在 Direct3D 11.1 的所有著色器階段使用，因此此指示適用于 Direct3D 11.1 執行時間的所有著色器階段，從 Windows 8 開始提供。</span><span class="sxs-lookup"><span data-stu-id="654e1-138">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="654e1-139">頂點</span><span class="sxs-lookup"><span data-stu-id="654e1-139">Vertex</span></span> | <span data-ttu-id="654e1-140">船體</span><span class="sxs-lookup"><span data-stu-id="654e1-140">Hull</span></span> | <span data-ttu-id="654e1-141">網域</span><span class="sxs-lookup"><span data-stu-id="654e1-141">Domain</span></span> | <span data-ttu-id="654e1-142">幾何</span><span class="sxs-lookup"><span data-stu-id="654e1-142">Geometry</span></span> | <span data-ttu-id="654e1-143">像素</span><span class="sxs-lookup"><span data-stu-id="654e1-143">Pixel</span></span> | <span data-ttu-id="654e1-144">計算</span><span class="sxs-lookup"><span data-stu-id="654e1-144">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="654e1-145">X</span><span class="sxs-lookup"><span data-stu-id="654e1-145">X</span></span>      | <span data-ttu-id="654e1-146">X</span><span class="sxs-lookup"><span data-stu-id="654e1-146">X</span></span>    | <span data-ttu-id="654e1-147">X</span><span class="sxs-lookup"><span data-stu-id="654e1-147">X</span></span>      | <span data-ttu-id="654e1-148">X</span><span class="sxs-lookup"><span data-stu-id="654e1-148">X</span></span>        | <span data-ttu-id="654e1-149">X</span><span class="sxs-lookup"><span data-stu-id="654e1-149">X</span></span>     | <span data-ttu-id="654e1-150">X</span><span class="sxs-lookup"><span data-stu-id="654e1-150">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="654e1-151">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="654e1-151">Minimum Shader Model</span></span>

<span data-ttu-id="654e1-152">下列著色器模型支援此指令：</span><span class="sxs-lookup"><span data-stu-id="654e1-152">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="654e1-153">著色器模型</span><span class="sxs-lookup"><span data-stu-id="654e1-153">Shader Model</span></span>                                              | <span data-ttu-id="654e1-154">支援</span><span class="sxs-lookup"><span data-stu-id="654e1-154">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="654e1-155">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="654e1-155">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="654e1-156">是</span><span class="sxs-lookup"><span data-stu-id="654e1-156">yes</span></span>       |
| [<span data-ttu-id="654e1-157">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="654e1-157">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="654e1-158">不可以</span><span class="sxs-lookup"><span data-stu-id="654e1-158">no</span></span>        |
| [<span data-ttu-id="654e1-159">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="654e1-159">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="654e1-160">不可以</span><span class="sxs-lookup"><span data-stu-id="654e1-160">no</span></span>        |
| [<span data-ttu-id="654e1-161">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="654e1-161">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="654e1-162">不可以</span><span class="sxs-lookup"><span data-stu-id="654e1-162">no</span></span>        |
| [<span data-ttu-id="654e1-163">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="654e1-163">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="654e1-164">不可以</span><span class="sxs-lookup"><span data-stu-id="654e1-164">no</span></span>        |
| [<span data-ttu-id="654e1-165">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="654e1-165">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="654e1-166">不可以</span><span class="sxs-lookup"><span data-stu-id="654e1-166">no</span></span>        |



 

> [!Note]  
> <span data-ttu-id="654e1-167">Cs \_ 4 \_ 0 和 cs \_ 4 1 支援這個指令 \_ 。</span><span class="sxs-lookup"><span data-stu-id="654e1-167">This instruction is supported in cs\_4\_0 and cs\_4\_1.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="654e1-168">相關主題</span><span class="sxs-lookup"><span data-stu-id="654e1-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="654e1-169">著色器模型5元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="654e1-169">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





