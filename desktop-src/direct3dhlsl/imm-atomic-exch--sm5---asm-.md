---
title: 'imm_atomic_exch (sm5-asm) '
description: 立即不可部分完成的 exchange 到記憶體。
ms.assetid: D06AE57E-52A4-4579-84FF-7DE9E713A5E3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb38cd696af079c5ae7dc896db619b95dd1d1d6c
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104092461"
---
# <a name="imm_atomic_exch-sm5---asm"></a><span data-ttu-id="f0a08-103">imm 不可部分完成 \_ \_ ms-exch-assistant-name (sm5-asm) </span><span class="sxs-lookup"><span data-stu-id="f0a08-103">imm\_atomic\_exch (sm5 - asm)</span></span>

<span data-ttu-id="f0a08-104">立即不可部分完成的 exchange 到記憶體。</span><span class="sxs-lookup"><span data-stu-id="f0a08-104">Immediate atomic exchange to memory.</span></span>



| <span data-ttu-id="f0a08-105">imm \_ 不可 \_ 部分完成 ms-exch-assistant-name dst0 \[ 。單一 \_ 元件 \_ 遮罩 \] 、dst1、dstAddress \[ . swizzle \] 、src0 \[ 。選取 \_ 元件\]</span><span class="sxs-lookup"><span data-stu-id="f0a08-105">imm\_atomic\_exch dst0\[.single\_component\_mask\], dst1, dstAddress\[.swizzle\], src0\[.select\_component\]</span></span> |
|--------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="f0a08-106">項目</span><span class="sxs-lookup"><span data-stu-id="f0a08-106">Item</span></span>                                                                                                           | <span data-ttu-id="f0a08-107">描述</span><span class="sxs-lookup"><span data-stu-id="f0a08-107">Description</span></span>                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0a08-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span><span class="sxs-lookup"><span data-stu-id="f0a08-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span></span><br/>                                                | <span data-ttu-id="f0a08-109">\[in \] 包含在寫入之前的 *dst1* 值。</span><span class="sxs-lookup"><span data-stu-id="f0a08-109">\[in\] Contains the value from *dst1* before the write.</span></span><br/>                                                                |
| <span data-ttu-id="f0a08-110"><span id="dst1"></span><span id="DST1"></span>*dst1*</span><span class="sxs-lookup"><span data-stu-id="f0a08-110"><span id="dst1"></span><span id="DST1"></span>*dst1*</span></span><br/>                                                | <span data-ttu-id="f0a08-111">\[在 \] 未排序的存取視圖中 (UAV)  (u \#) 。</span><span class="sxs-lookup"><span data-stu-id="f0a08-111">\[in\] An unordered access view (UAV) (u\#).</span></span> <span data-ttu-id="f0a08-112">在計算著色器中，這也可以是執行緒群組的共用記憶體 (g \#) 。</span><span class="sxs-lookup"><span data-stu-id="f0a08-112">In the Compute Shader this can also be Thread Group Shared Memory (g\#).</span></span> <br/> |
| <span data-ttu-id="f0a08-113"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*</span><span class="sxs-lookup"><span data-stu-id="f0a08-113"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*</span></span><br/> | <span data-ttu-id="f0a08-114">\[在 \] 記憶體位址中。</span><span class="sxs-lookup"><span data-stu-id="f0a08-114">\[in\] The memory address.</span></span><br/>                                                                                             |
| <span data-ttu-id="f0a08-115"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="f0a08-115"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                                | <span data-ttu-id="f0a08-116">\[在 \] *dstAddress* 要寫入至 *dst1* 的值。</span><span class="sxs-lookup"><span data-stu-id="f0a08-116">\[in\] The value to write to *dst1* at *dstAddress*.</span></span><br/>                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="f0a08-117">備註</span><span class="sxs-lookup"><span data-stu-id="f0a08-117">Remarks</span></span>

<span data-ttu-id="f0a08-118">此指令會在每個元件位址 *dstAddress* 的32位上執行單一元件32位值寫入運算元 *src0* 至 *dst1* 。</span><span class="sxs-lookup"><span data-stu-id="f0a08-118">This instruction performs a single component 32-bit value write of operand *src0* to *dst1* at 32-bit per component address *dstAddress*.</span></span>

<span data-ttu-id="f0a08-119">如果 *dst1* 是 u \# ，則可能已宣告為 raw、具型別或結構化。</span><span class="sxs-lookup"><span data-stu-id="f0a08-119">If *dst1* is a u\#, it may have been declared as raw, typed or structured.</span></span> <span data-ttu-id="f0a08-120">如果具型別，則必須使用 R32 uint/聖的系結資源格式宣告為 UINT/聖 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="f0a08-120">If typed, it must be declared as UINT/SINT with the bound resource format being R32\_UINT/\_SINT.</span></span>

<span data-ttu-id="f0a08-121">如果 *dst1* 為 g \# ，則必須將它宣告為 raw 或結構化。</span><span class="sxs-lookup"><span data-stu-id="f0a08-121">If *dst1* is g\#, it must be declared as raw or structured.</span></span>

<span data-ttu-id="f0a08-122">從位址取得的元件數目取決於在 *dst1* 中宣告之資源的維度。</span><span class="sxs-lookup"><span data-stu-id="f0a08-122">The number of components taken from the address is determined by the dimensionality of the resource declared at *dst1*.</span></span>

<span data-ttu-id="f0a08-123">目的地記憶體中的原始32位值會寫入至 *dst0*。</span><span class="sxs-lookup"><span data-stu-id="f0a08-123">The original 32-bit value in the destination memory is written to *dst0*.</span></span>

<span data-ttu-id="f0a08-124">整個作業會以不可部分完成的方式執行。</span><span class="sxs-lookup"><span data-stu-id="f0a08-124">The entire operation is performed atomically.</span></span>

<span data-ttu-id="f0a08-125">如果著色器調用處于非使用中狀態，例如，如果圖元先前在其執行過程中已捨棄，或圖元/樣本調用僅存在做為衍生的真實圖元/樣本的協助程式，則此指令完全不會改變 *dst1* 記憶體，且傳回的值為未定義。</span><span class="sxs-lookup"><span data-stu-id="f0a08-125">If the shader invocation is inactive, for example if the pixel has been discarded earlier in its execution, or a pixel/sample invocation only exists to serve as a helper to a real pixel/sample for derivatives, this instruction does not alter the *dst1* memory at all, and the returned value is undefined.</span></span>

<span data-ttu-id="f0a08-126">除了 u 的範圍外， \# 不會將任何內容寫入記憶體，除非 u \# 是結構化的，且在結構 (第二個元件) 的結構中的位元組位移會造成超出界限存取權，否則 UAV 的整個內容會變成未定義。</span><span class="sxs-lookup"><span data-stu-id="f0a08-126">Out of bounds addressing on u\# causes nothing to be written to memory, except if the u\# is structured, and byte offset into the struct (second component of the address) is causing the out of bounds access, then the entire contents of the UAV become undefined.</span></span>

<span data-ttu-id="f0a08-127">U 或 g 的超出範圍定址 \# \# 會導致未定義的結果傳回 *dst0* 中的著色器。</span><span class="sxs-lookup"><span data-stu-id="f0a08-127">Out of bounds addressing on u\# or g\# causes an undefined result to be returned to the shader in *dst0*.</span></span>

<span data-ttu-id="f0a08-128">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="f0a08-128">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="f0a08-129">頂點</span><span class="sxs-lookup"><span data-stu-id="f0a08-129">Vertex</span></span> | <span data-ttu-id="f0a08-130">船體</span><span class="sxs-lookup"><span data-stu-id="f0a08-130">Hull</span></span> | <span data-ttu-id="f0a08-131">網域</span><span class="sxs-lookup"><span data-stu-id="f0a08-131">Domain</span></span> | <span data-ttu-id="f0a08-132">幾何</span><span class="sxs-lookup"><span data-stu-id="f0a08-132">Geometry</span></span> | <span data-ttu-id="f0a08-133">像素</span><span class="sxs-lookup"><span data-stu-id="f0a08-133">Pixel</span></span> | <span data-ttu-id="f0a08-134">計算</span><span class="sxs-lookup"><span data-stu-id="f0a08-134">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="f0a08-135">X</span><span class="sxs-lookup"><span data-stu-id="f0a08-135">X</span></span>     | <span data-ttu-id="f0a08-136">X</span><span class="sxs-lookup"><span data-stu-id="f0a08-136">X</span></span>       |



 

<span data-ttu-id="f0a08-137">由於 UAVs 可在 Direct3D 11.1 的所有著色器階段使用，因此此指示適用于 Direct3D 11.1 執行時間的所有著色器階段，從 Windows 8 開始提供。</span><span class="sxs-lookup"><span data-stu-id="f0a08-137">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="f0a08-138">頂點</span><span class="sxs-lookup"><span data-stu-id="f0a08-138">Vertex</span></span> | <span data-ttu-id="f0a08-139">船體</span><span class="sxs-lookup"><span data-stu-id="f0a08-139">Hull</span></span> | <span data-ttu-id="f0a08-140">網域</span><span class="sxs-lookup"><span data-stu-id="f0a08-140">Domain</span></span> | <span data-ttu-id="f0a08-141">幾何</span><span class="sxs-lookup"><span data-stu-id="f0a08-141">Geometry</span></span> | <span data-ttu-id="f0a08-142">像素</span><span class="sxs-lookup"><span data-stu-id="f0a08-142">Pixel</span></span> | <span data-ttu-id="f0a08-143">計算</span><span class="sxs-lookup"><span data-stu-id="f0a08-143">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="f0a08-144">X</span><span class="sxs-lookup"><span data-stu-id="f0a08-144">X</span></span>      | <span data-ttu-id="f0a08-145">X</span><span class="sxs-lookup"><span data-stu-id="f0a08-145">X</span></span>    | <span data-ttu-id="f0a08-146">X</span><span class="sxs-lookup"><span data-stu-id="f0a08-146">X</span></span>      | <span data-ttu-id="f0a08-147">X</span><span class="sxs-lookup"><span data-stu-id="f0a08-147">X</span></span>        | <span data-ttu-id="f0a08-148">X</span><span class="sxs-lookup"><span data-stu-id="f0a08-148">X</span></span>     | <span data-ttu-id="f0a08-149">X</span><span class="sxs-lookup"><span data-stu-id="f0a08-149">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="f0a08-150">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="f0a08-150">Minimum Shader Model</span></span>

<span data-ttu-id="f0a08-151">下列著色器模型支援此指令：</span><span class="sxs-lookup"><span data-stu-id="f0a08-151">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="f0a08-152">著色器模型</span><span class="sxs-lookup"><span data-stu-id="f0a08-152">Shader Model</span></span>                                              | <span data-ttu-id="f0a08-153">支援</span><span class="sxs-lookup"><span data-stu-id="f0a08-153">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="f0a08-154">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="f0a08-154">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="f0a08-155">是</span><span class="sxs-lookup"><span data-stu-id="f0a08-155">yes</span></span>       |
| [<span data-ttu-id="f0a08-156">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="f0a08-156">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="f0a08-157">不可以</span><span class="sxs-lookup"><span data-stu-id="f0a08-157">no</span></span>        |
| [<span data-ttu-id="f0a08-158">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="f0a08-158">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="f0a08-159">不可以</span><span class="sxs-lookup"><span data-stu-id="f0a08-159">no</span></span>        |
| [<span data-ttu-id="f0a08-160">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="f0a08-160">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="f0a08-161">不可以</span><span class="sxs-lookup"><span data-stu-id="f0a08-161">no</span></span>        |
| [<span data-ttu-id="f0a08-162">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="f0a08-162">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="f0a08-163">不可以</span><span class="sxs-lookup"><span data-stu-id="f0a08-163">no</span></span>        |
| [<span data-ttu-id="f0a08-164">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="f0a08-164">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="f0a08-165">不可以</span><span class="sxs-lookup"><span data-stu-id="f0a08-165">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="f0a08-166">相關主題</span><span class="sxs-lookup"><span data-stu-id="f0a08-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f0a08-167">著色器模型5元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="f0a08-167">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





