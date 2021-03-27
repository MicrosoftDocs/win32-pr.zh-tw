---
title: 'imm_atomic_alloc (sm5-asm) '
description: 以不可部分完成的方式遞增以計數儲存的隱藏32位計數器，或附加未排序的存取視圖 (UAV) ，傳回原始值。
ms.assetid: 534FA3C3-6FAC-41DC-AC07-0E53FEED000C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28a97709629497bae9af0298789453ef1d1172b7
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "103679151"
---
# <a name="imm_atomic_alloc-sm5---asm"></a><span data-ttu-id="8d88f-103">imm 不可部分完成配置 \_ \_ (sm5-asm) </span><span class="sxs-lookup"><span data-stu-id="8d88f-103">imm\_atomic\_alloc (sm5 - asm)</span></span>

<span data-ttu-id="8d88f-104">以不可部分完成的方式遞增以計數儲存的隱藏32位計數器，或附加未排序的存取視圖 (UAV) ，傳回原始值。</span><span class="sxs-lookup"><span data-stu-id="8d88f-104">Atomically increment the hidden 32-bit counter stored with a Count or Append unordered access view (UAV), returning the original value.</span></span>



| <span data-ttu-id="8d88f-105">imm 不可部分完成配置 \_ \_ dst0 \[ 。單一 \_ 元件 \_ 遮罩 \] ，dstUAV</span><span class="sxs-lookup"><span data-stu-id="8d88f-105">imm\_atomic\_alloc dst0\[.single\_component\_mask\], dstUAV</span></span> |
|-------------------------------------------------------------|



 



| <span data-ttu-id="8d88f-106">項目</span><span class="sxs-lookup"><span data-stu-id="8d88f-106">Item</span></span>                                                                                           | <span data-ttu-id="8d88f-107">描述</span><span class="sxs-lookup"><span data-stu-id="8d88f-107">Description</span></span>                                                               |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <span data-ttu-id="8d88f-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span><span class="sxs-lookup"><span data-stu-id="8d88f-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span></span><br/>                                | <span data-ttu-id="8d88f-109">\[中 \] 的包含傳回的計數器值。</span><span class="sxs-lookup"><span data-stu-id="8d88f-109">\[in\] Contains the returned counter value.</span></span><br/>                    |
| <span data-ttu-id="8d88f-110"><span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*</span><span class="sxs-lookup"><span data-stu-id="8d88f-110"><span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*</span></span><br/> | <span data-ttu-id="8d88f-111">\[在 \] 具有 Count 或 Append 旗標的結構化緩衝區 UAV 中。</span><span class="sxs-lookup"><span data-stu-id="8d88f-111">\[in\] A Structured Buffer UAV with the Count or Append flag.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="8d88f-112">備註</span><span class="sxs-lookup"><span data-stu-id="8d88f-112">Remarks</span></span>

<span data-ttu-id="8d88f-113">有一個隱藏的不帶正負號32位整數計數器值與每個計數或附加緩衝區視圖相關聯，此值會在 view 系結至管線時初始化，包括保留先前值的選項。</span><span class="sxs-lookup"><span data-stu-id="8d88f-113">There is a hidden unsigned 32-bit integer counter value associated with each Count or Append Buffer view which is initialized when the view is bound to the pipeline, including the option to keep the previous value.</span></span>

<span data-ttu-id="8d88f-114">此指令會執行計數器值的不可部分完成遞增，並將原始值傳回給 *dst0*。</span><span class="sxs-lookup"><span data-stu-id="8d88f-114">This instruction does an atomic increment of the counter value, returning the original to *dst0*.</span></span>

<span data-ttu-id="8d88f-115">針對附加 UAV，傳回的值僅適用于著色器調用的持續時間。</span><span class="sxs-lookup"><span data-stu-id="8d88f-115">For an Append UAV, the returned value is only valid for the duration of the shader invocation.</span></span> <span data-ttu-id="8d88f-116">之後，執行可能會重新排列記憶體配置。</span><span class="sxs-lookup"><span data-stu-id="8d88f-116">after that the implementation may rearrange the memory layout.</span></span> <span data-ttu-id="8d88f-117">任何以傳回值為基礎的記憶體定址都必須限制為著色器調用。</span><span class="sxs-lookup"><span data-stu-id="8d88f-117">Any memory addressing based on the returned value must be limited to the shader invocation.</span></span>

<span data-ttu-id="8d88f-118">針對附加 UAV，在著色器調用中，HLSL 編譯器可以使用傳回的值做為用來存取結構化緩衝區的結構索引。</span><span class="sxs-lookup"><span data-stu-id="8d88f-118">For an Append UAV, within the shader invocation the HLSL compiler can use the returned value as the struct index to use for accessing the structured buffer.</span></span> <span data-ttu-id="8d88f-119">存取由呼叫 (s 所傳回的任何結構索引，) 至 imm 不可部分完成的配置或 [ \_ 使用](imm-atomic-consume--sm5---asm-.md)會產生未定義的結果，即表示正在存取 UAV 中的記憶體位置是隨機的，而且只會在著色器調用的存留期內修正。 **\_ \_**</span><span class="sxs-lookup"><span data-stu-id="8d88f-119">Accessing any struct index other than those locations returned by call(s) to **imm\_atomic\_alloc** or [\_consume](imm-atomic-consume--sm5---asm-.md) produce undefined results in that exactly which memory location within the UAV is being accessed is random and only fixed for the lifetime of the shader invocation.</span></span>

<span data-ttu-id="8d88f-120">針對計數 UAV，應用程式可以將傳回的值儲存為 UAV 內的固定位置參考，而該位置在著色器調用結束後有意義。</span><span class="sxs-lookup"><span data-stu-id="8d88f-120">For a Count UAV, the returned value can be saved by the application as a reference to a fixed location within the UAV that is meaningful after the shader invocation is over.</span></span> <span data-ttu-id="8d88f-121">計數 UAV 中的任何位置，都可以永遠存取，而不受 count 值的影響。</span><span class="sxs-lookup"><span data-stu-id="8d88f-121">Any location in a Count UAV may always be accessed independent of what the count value is.</span></span>

<span data-ttu-id="8d88f-122">沒有計數的固定，所以它會在溢位時換行。</span><span class="sxs-lookup"><span data-stu-id="8d88f-122">There is no clamping of the count, so it wraps on overflow.</span></span>

<span data-ttu-id="8d88f-123">相同的著色器無法在相同的 UAV 上 **嘗試 \_ \_ 使用** imm 不可部分完成配置和 imm 不可部分完成。 **\_ \_**</span><span class="sxs-lookup"><span data-stu-id="8d88f-123">The same shader cannot attempt both **imm\_atomic\_alloc** and **imm\_atomic\_consume** on the same UAV.</span></span> <span data-ttu-id="8d88f-124">此外，GPU 無法允許多個著色器調用在相同的 UAV 上混合使用 imm 不可部分完成配置和 imm 不可部分完成。 **\_ \_** **\_ \_**</span><span class="sxs-lookup"><span data-stu-id="8d88f-124">Further, the GPU cannot allow multiple shader invocations to mix **imm\_atomic\_alloc** and **imm\_atomic\_consume** on the same UAV.</span></span>

<span data-ttu-id="8d88f-125">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="8d88f-125">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="8d88f-126">頂點</span><span class="sxs-lookup"><span data-stu-id="8d88f-126">Vertex</span></span> | <span data-ttu-id="8d88f-127">船體</span><span class="sxs-lookup"><span data-stu-id="8d88f-127">Hull</span></span> | <span data-ttu-id="8d88f-128">網域</span><span class="sxs-lookup"><span data-stu-id="8d88f-128">Domain</span></span> | <span data-ttu-id="8d88f-129">幾何</span><span class="sxs-lookup"><span data-stu-id="8d88f-129">Geometry</span></span> | <span data-ttu-id="8d88f-130">像素</span><span class="sxs-lookup"><span data-stu-id="8d88f-130">Pixel</span></span> | <span data-ttu-id="8d88f-131">計算</span><span class="sxs-lookup"><span data-stu-id="8d88f-131">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="8d88f-132">X</span><span class="sxs-lookup"><span data-stu-id="8d88f-132">X</span></span>     | <span data-ttu-id="8d88f-133">X</span><span class="sxs-lookup"><span data-stu-id="8d88f-133">X</span></span>       |



 

<span data-ttu-id="8d88f-134">由於 UAVs 可在 Direct3D 11.1 的所有著色器階段使用，因此此指示適用于 Direct3D 11.1 執行時間的所有著色器階段，從 Windows 8 開始提供。</span><span class="sxs-lookup"><span data-stu-id="8d88f-134">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="8d88f-135">頂點</span><span class="sxs-lookup"><span data-stu-id="8d88f-135">Vertex</span></span> | <span data-ttu-id="8d88f-136">船體</span><span class="sxs-lookup"><span data-stu-id="8d88f-136">Hull</span></span> | <span data-ttu-id="8d88f-137">網域</span><span class="sxs-lookup"><span data-stu-id="8d88f-137">Domain</span></span> | <span data-ttu-id="8d88f-138">幾何</span><span class="sxs-lookup"><span data-stu-id="8d88f-138">Geometry</span></span> | <span data-ttu-id="8d88f-139">像素</span><span class="sxs-lookup"><span data-stu-id="8d88f-139">Pixel</span></span> | <span data-ttu-id="8d88f-140">計算</span><span class="sxs-lookup"><span data-stu-id="8d88f-140">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="8d88f-141">X</span><span class="sxs-lookup"><span data-stu-id="8d88f-141">X</span></span>      | <span data-ttu-id="8d88f-142">X</span><span class="sxs-lookup"><span data-stu-id="8d88f-142">X</span></span>    | <span data-ttu-id="8d88f-143">X</span><span class="sxs-lookup"><span data-stu-id="8d88f-143">X</span></span>      | <span data-ttu-id="8d88f-144">X</span><span class="sxs-lookup"><span data-stu-id="8d88f-144">X</span></span>        | <span data-ttu-id="8d88f-145">X</span><span class="sxs-lookup"><span data-stu-id="8d88f-145">X</span></span>     | <span data-ttu-id="8d88f-146">X</span><span class="sxs-lookup"><span data-stu-id="8d88f-146">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="8d88f-147">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="8d88f-147">Minimum Shader Model</span></span>

<span data-ttu-id="8d88f-148">下列著色器模型支援此指令：</span><span class="sxs-lookup"><span data-stu-id="8d88f-148">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="8d88f-149">著色器模型</span><span class="sxs-lookup"><span data-stu-id="8d88f-149">Shader Model</span></span>                                              | <span data-ttu-id="8d88f-150">支援</span><span class="sxs-lookup"><span data-stu-id="8d88f-150">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="8d88f-151">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="8d88f-151">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="8d88f-152">是</span><span class="sxs-lookup"><span data-stu-id="8d88f-152">yes</span></span>       |
| [<span data-ttu-id="8d88f-153">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="8d88f-153">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="8d88f-154">不可以</span><span class="sxs-lookup"><span data-stu-id="8d88f-154">no</span></span>        |
| [<span data-ttu-id="8d88f-155">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="8d88f-155">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="8d88f-156">不可以</span><span class="sxs-lookup"><span data-stu-id="8d88f-156">no</span></span>        |
| [<span data-ttu-id="8d88f-157">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="8d88f-157">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="8d88f-158">不可以</span><span class="sxs-lookup"><span data-stu-id="8d88f-158">no</span></span>        |
| [<span data-ttu-id="8d88f-159">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="8d88f-159">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="8d88f-160">不可以</span><span class="sxs-lookup"><span data-stu-id="8d88f-160">no</span></span>        |
| [<span data-ttu-id="8d88f-161">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="8d88f-161">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="8d88f-162">不可以</span><span class="sxs-lookup"><span data-stu-id="8d88f-162">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="8d88f-163">相關主題</span><span class="sxs-lookup"><span data-stu-id="8d88f-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8d88f-164">著色器模型5元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="8d88f-164">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





