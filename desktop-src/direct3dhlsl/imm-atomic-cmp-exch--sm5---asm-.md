---
title: 'imm_atomic_cmp_exch (sm5-asm) '
description: 立即比較和交換至記憶體。
ms.assetid: 317A69E1-0E0A-45C8-8E0A-B88659ADBECC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f63e1be030d7cce0d6f0a581788db39a599272b2
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "103841684"
---
# <a name="imm_atomic_cmp_exch-sm5---asm"></a><span data-ttu-id="cd5d9-103">imm 不可部分完成的 \_ \_ cmp \_ ms-exch-assistant-name (sm5-asm) </span><span class="sxs-lookup"><span data-stu-id="cd5d9-103">imm\_atomic\_cmp\_exch (sm5 - asm)</span></span>

<span data-ttu-id="cd5d9-104">立即比較和交換至記憶體。</span><span class="sxs-lookup"><span data-stu-id="cd5d9-104">Immediate compare and exchange to memory.</span></span>



| <span data-ttu-id="cd5d9-105">imm 不可部分完成 \_ \_ \_ 的 cmp ms-exch-assistant-name dst0 \[ 。單一 \_ 元件 \_ 遮罩 \] 、dst1、dstAddress \[ . swizzle \] 、src0 \[ 。 select \_ component \] ，src1 \[ . select \_ component\]</span><span class="sxs-lookup"><span data-stu-id="cd5d9-105">imm\_atomic\_cmp\_exch dst0\[.single\_component\_mask\], dst1, dstAddress\[.swizzle\], src0\[.select\_component\], src1\[.select\_component\]</span></span> |
|-----------------------------------------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="cd5d9-106">項目</span><span class="sxs-lookup"><span data-stu-id="cd5d9-106">Item</span></span>                                                                                                           | <span data-ttu-id="cd5d9-107">描述</span><span class="sxs-lookup"><span data-stu-id="cd5d9-107">Description</span></span>                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd5d9-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span><span class="sxs-lookup"><span data-stu-id="cd5d9-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span></span><br/>                                                | <span data-ttu-id="cd5d9-109">\[out \] 在寫入之前包含 *dst1* 。</span><span class="sxs-lookup"><span data-stu-id="cd5d9-109">\[out\] Contains *dst1* before the write.</span></span><br/>                                                                              |
| <span data-ttu-id="cd5d9-110"><span id="dst1"></span><span id="DST1"></span>*dst1*</span><span class="sxs-lookup"><span data-stu-id="cd5d9-110"><span id="dst1"></span><span id="DST1"></span>*dst1*</span></span><br/>                                                | <span data-ttu-id="cd5d9-111">\[在 \] 未排序的存取視圖中 (UAV)  (u \#) 。</span><span class="sxs-lookup"><span data-stu-id="cd5d9-111">\[in\] An unordered access view (UAV) (u\#).</span></span> <span data-ttu-id="cd5d9-112">在計算著色器中，這也可以是執行緒群組的共用記憶體 (g \#) 。</span><span class="sxs-lookup"><span data-stu-id="cd5d9-112">In the compute shader this can also be thread group shared memory (g\#).</span></span> <br/> |
| <span data-ttu-id="cd5d9-113"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*</span><span class="sxs-lookup"><span data-stu-id="cd5d9-113"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*</span></span><br/> | <span data-ttu-id="cd5d9-114">\[在 \] 目的地記憶體中。</span><span class="sxs-lookup"><span data-stu-id="cd5d9-114">\[in\] The destination memory.</span></span><br/>                                                                                         |
| <span data-ttu-id="cd5d9-115"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="cd5d9-115"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                                | <span data-ttu-id="cd5d9-116">\[在 \] [要與 *dst1* 比較的值] 中。</span><span class="sxs-lookup"><span data-stu-id="cd5d9-116">\[in\] The value to compare to *dst1*.</span></span><br/>                                                                                 |
| <span data-ttu-id="cd5d9-117"><span id="scr1"></span><span id="SCR1"></span>*scr1*</span><span class="sxs-lookup"><span data-stu-id="cd5d9-117"><span id="scr1"></span><span id="SCR1"></span>*scr1*</span></span><br/>                                                | <span data-ttu-id="cd5d9-118">\[\]如果比較的值相同，則在寫入目的地記憶體的值中。</span><span class="sxs-lookup"><span data-stu-id="cd5d9-118">\[in\] The value written to the destination memory if the compared values are identical.</span></span><br/>                               |



 

<span data-ttu-id="cd5d9-119">此指令會在每個元件位址 *dstAddress* 的32位上執行運算元 *src0* 與 *dst1* 的單一元件32位值比較。</span><span class="sxs-lookup"><span data-stu-id="cd5d9-119">This instruction performs a single component 32-bit value compare of operand *src0* with *dst1* at 32-bit per component address *dstAddress*.</span></span>

<span data-ttu-id="cd5d9-120">如果 *dst1* 是 u \# ，則可能已宣告為 raw、具型別或結構化。</span><span class="sxs-lookup"><span data-stu-id="cd5d9-120">If *dst1* is a u\#, it may have been declared as raw, typed or structured.</span></span> <span data-ttu-id="cd5d9-121">如果具型別，則必須使用 R32 uint/聖的系結資源格式宣告為 UINT/聖 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="cd5d9-121">If typed, it must be declared as UINT/SINT with the bound resource format being R32\_UINT/\_SINT.</span></span>

<span data-ttu-id="cd5d9-122">如果 *dst1* 為 g \# ，則必須將它宣告為 raw 或結構化。</span><span class="sxs-lookup"><span data-stu-id="cd5d9-122">If *dst1* is g\#, it must be declared as raw or structured.</span></span>

<span data-ttu-id="cd5d9-123">如果比較的值相同， *src1* 中的單一元件32位值會寫入至目的地記憶體。</span><span class="sxs-lookup"><span data-stu-id="cd5d9-123">If the compared values are identical, the single-component 32-bit value in *src1* is written to the destination memory.</span></span> <span data-ttu-id="cd5d9-124">否則，不會變更目的地記憶體。</span><span class="sxs-lookup"><span data-stu-id="cd5d9-124">Otherwise, the destination memory is not changed.</span></span>

<span data-ttu-id="cd5d9-125">目的地記憶體中的原始32位值一律會寫入至 *dst0*。</span><span class="sxs-lookup"><span data-stu-id="cd5d9-125">The original 32-bit value in the destination memory is always written to *dst0*.</span></span>

<span data-ttu-id="cd5d9-126">整個作業會以不可部分完成的方式執行。</span><span class="sxs-lookup"><span data-stu-id="cd5d9-126">The entire operation is performed atomically.</span></span>

<span data-ttu-id="cd5d9-127">如果著色器調用處于非使用中狀態，例如，如果圖元先前在其執行過程中已捨棄，或圖元/樣本調用僅存在做為衍生的真實圖元/樣本的協助程式，則此指令完全不會改變 *dst1* 記憶體，且傳回的值為未定義。</span><span class="sxs-lookup"><span data-stu-id="cd5d9-127">If the shader invocation is inactive, for example if the pixel has been discarded earlier in its execution, or a pixel/sample invocation only exists to serve as a helper to a real pixel/sample for derivatives, this instruction does not alter the *dst1* memory at all, and the returned value is undefined.</span></span>

<span data-ttu-id="cd5d9-128">除了 u 的範圍外， \# 不會將任何內容寫入記憶體，除非 u \# 是結構化的，且在結構 (第二個元件) 的結構中的位元組位移會造成超出界限存取權，否則 UAV 的整個內容會變成未定義。</span><span class="sxs-lookup"><span data-stu-id="cd5d9-128">Out of bounds addressing on u\# causes nothing to be written to memory, except if the u\# is structured, and byte offset into the struct (second component of the address) is causing the out of bounds access, then the entire contents of the UAV become undefined.</span></span>

<span data-ttu-id="cd5d9-129">U 或 g 的超出範圍定址 \# \# 會導致未定義的結果傳回 *dst0* 中的著色器。</span><span class="sxs-lookup"><span data-stu-id="cd5d9-129">Out of bounds addressing on u\# or g\# causes an undefined result to be returned to the shader in *dst0*.</span></span>

<span data-ttu-id="cd5d9-130">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="cd5d9-130">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="cd5d9-131">頂點</span><span class="sxs-lookup"><span data-stu-id="cd5d9-131">Vertex</span></span> | <span data-ttu-id="cd5d9-132">船體</span><span class="sxs-lookup"><span data-stu-id="cd5d9-132">Hull</span></span> | <span data-ttu-id="cd5d9-133">網域</span><span class="sxs-lookup"><span data-stu-id="cd5d9-133">Domain</span></span> | <span data-ttu-id="cd5d9-134">幾何</span><span class="sxs-lookup"><span data-stu-id="cd5d9-134">Geometry</span></span> | <span data-ttu-id="cd5d9-135">像素</span><span class="sxs-lookup"><span data-stu-id="cd5d9-135">Pixel</span></span> | <span data-ttu-id="cd5d9-136">計算</span><span class="sxs-lookup"><span data-stu-id="cd5d9-136">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="cd5d9-137">X</span><span class="sxs-lookup"><span data-stu-id="cd5d9-137">X</span></span>     | <span data-ttu-id="cd5d9-138">X</span><span class="sxs-lookup"><span data-stu-id="cd5d9-138">X</span></span>       |



 

<span data-ttu-id="cd5d9-139">由於 UAVs 可在 Direct3D 11.1 的所有著色器階段使用，因此此指示適用于 Direct3D 11.1 執行時間的所有著色器階段，從 Windows 8 開始提供。</span><span class="sxs-lookup"><span data-stu-id="cd5d9-139">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="cd5d9-140">頂點</span><span class="sxs-lookup"><span data-stu-id="cd5d9-140">Vertex</span></span> | <span data-ttu-id="cd5d9-141">船體</span><span class="sxs-lookup"><span data-stu-id="cd5d9-141">Hull</span></span> | <span data-ttu-id="cd5d9-142">網域</span><span class="sxs-lookup"><span data-stu-id="cd5d9-142">Domain</span></span> | <span data-ttu-id="cd5d9-143">幾何</span><span class="sxs-lookup"><span data-stu-id="cd5d9-143">Geometry</span></span> | <span data-ttu-id="cd5d9-144">像素</span><span class="sxs-lookup"><span data-stu-id="cd5d9-144">Pixel</span></span> | <span data-ttu-id="cd5d9-145">計算</span><span class="sxs-lookup"><span data-stu-id="cd5d9-145">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="cd5d9-146">X</span><span class="sxs-lookup"><span data-stu-id="cd5d9-146">X</span></span>      | <span data-ttu-id="cd5d9-147">X</span><span class="sxs-lookup"><span data-stu-id="cd5d9-147">X</span></span>    | <span data-ttu-id="cd5d9-148">X</span><span class="sxs-lookup"><span data-stu-id="cd5d9-148">X</span></span>      | <span data-ttu-id="cd5d9-149">X</span><span class="sxs-lookup"><span data-stu-id="cd5d9-149">X</span></span>        | <span data-ttu-id="cd5d9-150">X</span><span class="sxs-lookup"><span data-stu-id="cd5d9-150">X</span></span>     | <span data-ttu-id="cd5d9-151">X</span><span class="sxs-lookup"><span data-stu-id="cd5d9-151">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="cd5d9-152">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="cd5d9-152">Minimum Shader Model</span></span>

<span data-ttu-id="cd5d9-153">下列著色器模型支援此指令：</span><span class="sxs-lookup"><span data-stu-id="cd5d9-153">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="cd5d9-154">著色器模型</span><span class="sxs-lookup"><span data-stu-id="cd5d9-154">Shader Model</span></span>                                              | <span data-ttu-id="cd5d9-155">支援</span><span class="sxs-lookup"><span data-stu-id="cd5d9-155">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="cd5d9-156">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="cd5d9-156">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="cd5d9-157">是</span><span class="sxs-lookup"><span data-stu-id="cd5d9-157">yes</span></span>       |
| [<span data-ttu-id="cd5d9-158">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="cd5d9-158">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="cd5d9-159">不可以</span><span class="sxs-lookup"><span data-stu-id="cd5d9-159">no</span></span>        |
| [<span data-ttu-id="cd5d9-160">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="cd5d9-160">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="cd5d9-161">不可以</span><span class="sxs-lookup"><span data-stu-id="cd5d9-161">no</span></span>        |
| [<span data-ttu-id="cd5d9-162">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="cd5d9-162">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="cd5d9-163">不可以</span><span class="sxs-lookup"><span data-stu-id="cd5d9-163">no</span></span>        |
| [<span data-ttu-id="cd5d9-164">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="cd5d9-164">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="cd5d9-165">不可以</span><span class="sxs-lookup"><span data-stu-id="cd5d9-165">no</span></span>        |
| [<span data-ttu-id="cd5d9-166">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="cd5d9-166">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="cd5d9-167">不可以</span><span class="sxs-lookup"><span data-stu-id="cd5d9-167">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="cd5d9-168">相關主題</span><span class="sxs-lookup"><span data-stu-id="cd5d9-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cd5d9-169">著色器模型5元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="cd5d9-169">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





