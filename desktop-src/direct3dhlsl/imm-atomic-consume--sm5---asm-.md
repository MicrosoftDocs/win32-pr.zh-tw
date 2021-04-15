---
title: 'imm_atomic_consume (sm5-asm) '
description: 以不可部分完成的方式遞減以計數儲存的隱藏32位計數器，或附加未排序的存取視圖 (UAV) ，傳回新的值。
ms.assetid: 1115C318-2F86-4161-AC5C-2A61A262DC28
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a1c6fe01ddb92b2ce870b16254f75c52cadd341
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104990787"
---
# <a name="imm_atomic_consume-sm5---asm"></a><span data-ttu-id="41377-103">imm 不可部分完成 \_ \_ 的使用 (sm5-asm) </span><span class="sxs-lookup"><span data-stu-id="41377-103">imm\_atomic\_consume (sm5 - asm)</span></span>

<span data-ttu-id="41377-104">以不可部分完成的方式遞減以計數儲存的隱藏32位計數器，或附加未排序的存取視圖 (UAV) ，傳回新的值。</span><span class="sxs-lookup"><span data-stu-id="41377-104">Atomically decrement the hidden 32-bit counter stored with a Count or Append unordered access view (UAV), returning the new value.</span></span>



| <span data-ttu-id="41377-105">imm 不可部分完成的 \_ \_ 使用 dst0 \[ 。單一 \_ 元件 \_ 遮罩 \] ，dstUAV</span><span class="sxs-lookup"><span data-stu-id="41377-105">imm\_atomic\_consume dst0\[.single\_component\_mask\], dstUAV</span></span> |
|---------------------------------------------------------------|



 



| <span data-ttu-id="41377-106">項目</span><span class="sxs-lookup"><span data-stu-id="41377-106">Item</span></span>                                                                                           | <span data-ttu-id="41377-107">描述</span><span class="sxs-lookup"><span data-stu-id="41377-107">Description</span></span>                                                               |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <span data-ttu-id="41377-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span><span class="sxs-lookup"><span data-stu-id="41377-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span></span><br/>                                | <span data-ttu-id="41377-109">\[中 \] 的包含傳回的原始計數器值。</span><span class="sxs-lookup"><span data-stu-id="41377-109">\[in\] Contains the returned original counter value.</span></span><br/>           |
| <span data-ttu-id="41377-110"><span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*</span><span class="sxs-lookup"><span data-stu-id="41377-110"><span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*</span></span><br/> | <span data-ttu-id="41377-111">\[在 \] 具有 Count 或 Append 旗標的結構化緩衝區 UAV 中。</span><span class="sxs-lookup"><span data-stu-id="41377-111">\[in\] A structured buffer UAV with the Count or Append flag.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="41377-112">備註</span><span class="sxs-lookup"><span data-stu-id="41377-112">Remarks</span></span>

<span data-ttu-id="41377-113">請參閱「imm 不可部分完成」配置，以瞭解傳回的計數值是否有效，取決於 UAV 是 Count 或 Append。 [ \_ \_ ](imm-atomic-alloc--sm5---asm-.md)</span><span class="sxs-lookup"><span data-stu-id="41377-113">See [imm\_atomic\_alloc](imm-atomic-alloc--sm5---asm-.md) for a discussion about the validity of the returned count value depending on whether the UAV is Count or Append.</span></span> <span data-ttu-id="41377-114">這同樣適用于 imm 不可部分完成的 **\_ \_ 使用**。</span><span class="sxs-lookup"><span data-stu-id="41377-114">The same applies for **imm\_atomic\_consume**.</span></span>

<span data-ttu-id="41377-115">imm 不可部分完成的 **\_ \_ 使用** 會執行計數器值的不可部分完成遞減，並將新值傳回給 *dst0*。</span><span class="sxs-lookup"><span data-stu-id="41377-115">**imm\_atomic\_consume** does an atomic decrement of the counter value, returning the new value to *dst0*.</span></span>

<span data-ttu-id="41377-116">沒有計數的固定，所以它會在下溢處進行換行。</span><span class="sxs-lookup"><span data-stu-id="41377-116">There is no clamping of the count, so it wraps on underflow.</span></span>

<span data-ttu-id="41377-117">相同的著色器無法在相同的 UAV 上 **嘗試 \_ \_ 使用** imm 不可部分完成配置和 imm 不可部分完成。 **\_ \_**</span><span class="sxs-lookup"><span data-stu-id="41377-117">The same shader cannot attempt both **imm\_atomic\_alloc** and **imm\_atomic\_consume** on the same UAV.</span></span> <span data-ttu-id="41377-118">此外，GPU 無法允許多個著色器調用在相同的 UAV 上混合使用 imm 不可部分完成配置和 imm 不可部分完成。 **\_ \_** **\_ \_**</span><span class="sxs-lookup"><span data-stu-id="41377-118">Further, the GPU cannot allow multiple shader invocations to mix **imm\_atomic\_alloc** and **imm\_atomic\_consume** on the same UAV.</span></span>

<span data-ttu-id="41377-119">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="41377-119">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="41377-120">頂點</span><span class="sxs-lookup"><span data-stu-id="41377-120">Vertex</span></span> | <span data-ttu-id="41377-121">船體</span><span class="sxs-lookup"><span data-stu-id="41377-121">Hull</span></span> | <span data-ttu-id="41377-122">網域</span><span class="sxs-lookup"><span data-stu-id="41377-122">Domain</span></span> | <span data-ttu-id="41377-123">幾何</span><span class="sxs-lookup"><span data-stu-id="41377-123">Geometry</span></span> | <span data-ttu-id="41377-124">像素</span><span class="sxs-lookup"><span data-stu-id="41377-124">Pixel</span></span> | <span data-ttu-id="41377-125">計算</span><span class="sxs-lookup"><span data-stu-id="41377-125">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="41377-126">X</span><span class="sxs-lookup"><span data-stu-id="41377-126">X</span></span>     | <span data-ttu-id="41377-127">X</span><span class="sxs-lookup"><span data-stu-id="41377-127">X</span></span>       |



 

<span data-ttu-id="41377-128">由於 UAVs 可在 Direct3D 11.1 的所有著色器階段使用，因此此指示適用于 Direct3D 11.1 執行時間的所有著色器階段，從 Windows 8 開始提供。</span><span class="sxs-lookup"><span data-stu-id="41377-128">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="41377-129">頂點</span><span class="sxs-lookup"><span data-stu-id="41377-129">Vertex</span></span> | <span data-ttu-id="41377-130">船體</span><span class="sxs-lookup"><span data-stu-id="41377-130">Hull</span></span> | <span data-ttu-id="41377-131">網域</span><span class="sxs-lookup"><span data-stu-id="41377-131">Domain</span></span> | <span data-ttu-id="41377-132">幾何</span><span class="sxs-lookup"><span data-stu-id="41377-132">Geometry</span></span> | <span data-ttu-id="41377-133">像素</span><span class="sxs-lookup"><span data-stu-id="41377-133">Pixel</span></span> | <span data-ttu-id="41377-134">計算</span><span class="sxs-lookup"><span data-stu-id="41377-134">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="41377-135">X</span><span class="sxs-lookup"><span data-stu-id="41377-135">X</span></span>      | <span data-ttu-id="41377-136">X</span><span class="sxs-lookup"><span data-stu-id="41377-136">X</span></span>    | <span data-ttu-id="41377-137">X</span><span class="sxs-lookup"><span data-stu-id="41377-137">X</span></span>      | <span data-ttu-id="41377-138">X</span><span class="sxs-lookup"><span data-stu-id="41377-138">X</span></span>        | <span data-ttu-id="41377-139">X</span><span class="sxs-lookup"><span data-stu-id="41377-139">X</span></span>     | <span data-ttu-id="41377-140">X</span><span class="sxs-lookup"><span data-stu-id="41377-140">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="41377-141">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="41377-141">Minimum Shader Model</span></span>

<span data-ttu-id="41377-142">下列著色器模型支援此指令：</span><span class="sxs-lookup"><span data-stu-id="41377-142">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="41377-143">著色器模型</span><span class="sxs-lookup"><span data-stu-id="41377-143">Shader Model</span></span>                                              | <span data-ttu-id="41377-144">支援</span><span class="sxs-lookup"><span data-stu-id="41377-144">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="41377-145">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="41377-145">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="41377-146">是</span><span class="sxs-lookup"><span data-stu-id="41377-146">yes</span></span>       |
| [<span data-ttu-id="41377-147">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="41377-147">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="41377-148">不可以</span><span class="sxs-lookup"><span data-stu-id="41377-148">no</span></span>        |
| [<span data-ttu-id="41377-149">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="41377-149">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="41377-150">不可以</span><span class="sxs-lookup"><span data-stu-id="41377-150">no</span></span>        |
| [<span data-ttu-id="41377-151">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="41377-151">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="41377-152">不可以</span><span class="sxs-lookup"><span data-stu-id="41377-152">no</span></span>        |
| [<span data-ttu-id="41377-153">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="41377-153">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="41377-154">不可以</span><span class="sxs-lookup"><span data-stu-id="41377-154">no</span></span>        |
| [<span data-ttu-id="41377-155">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="41377-155">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="41377-156">不可以</span><span class="sxs-lookup"><span data-stu-id="41377-156">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="41377-157">相關主題</span><span class="sxs-lookup"><span data-stu-id="41377-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="41377-158">著色器模型5元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="41377-158">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





