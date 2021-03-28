---
title: 'imm_atomic_or (sm5-asm) '
description: 立即不可部分完成的位 OR 至記憶體。 傳回在或之前的記憶體中的值。
ms.assetid: 0ACE977D-5D0E-4E9C-A49F-B81D789B0D43
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2bc3b9afd2ba9f4dc63a8fb5c5818c1121c7ec6
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104022838"
---
# <a name="imm_atomic_or-sm5---asm"></a><span data-ttu-id="ff3cf-104">imm 不可部分完成 \_ \_ 或 (sm5-asm) </span><span class="sxs-lookup"><span data-stu-id="ff3cf-104">imm\_atomic\_or (sm5 - asm)</span></span>

<span data-ttu-id="ff3cf-105">立即不可部分完成的位 OR 至記憶體。</span><span class="sxs-lookup"><span data-stu-id="ff3cf-105">Immediate atomic bitwise OR to memory.</span></span> <span data-ttu-id="ff3cf-106">傳回在或之前的記憶體中的值。</span><span class="sxs-lookup"><span data-stu-id="ff3cf-106">Returns the value in memory before the OR.</span></span>



| <span data-ttu-id="ff3cf-107">imm \_ 不可 \_ 部分完成或 dst0 \[ 。單一 \_ 元件 \_ 遮罩 \] 、dst1、dstAddress \[ swizzle \] 、src0 \[ 。選取 \_ 元件\]</span><span class="sxs-lookup"><span data-stu-id="ff3cf-107">imm\_atomic\_or dst0\[.single\_component\_mask\], dst1, dstAddress\[.swizzle\], src0\[.select\_component\]</span></span> |
|------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="ff3cf-108">項目</span><span class="sxs-lookup"><span data-stu-id="ff3cf-108">Item</span></span>                                                                                                           | <span data-ttu-id="ff3cf-109">描述</span><span class="sxs-lookup"><span data-stu-id="ff3cf-109">Description</span></span>                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff3cf-110"><span id="dst0"></span><span id="DST0"></span>*dst0*</span><span class="sxs-lookup"><span data-stu-id="ff3cf-110"><span id="dst0"></span><span id="DST0"></span>*dst0*</span></span><br/>                                                | <span data-ttu-id="ff3cf-111">\[in \] 包含在或之前的 *dst1* 值。</span><span class="sxs-lookup"><span data-stu-id="ff3cf-111">\[in\] Contains the value from *dst1* before the OR.</span></span><br/>                                                                   |
| <span data-ttu-id="ff3cf-112"><span id="dst1"></span><span id="DST1"></span>*dst1*</span><span class="sxs-lookup"><span data-stu-id="ff3cf-112"><span id="dst1"></span><span id="DST1"></span>*dst1*</span></span><br/>                                                | <span data-ttu-id="ff3cf-113">\[在 \] 未排序的存取視圖中 (UAV)  (u \#) 。</span><span class="sxs-lookup"><span data-stu-id="ff3cf-113">\[in\] An unordered access view (UAV) (u\#).</span></span> <span data-ttu-id="ff3cf-114">在計算著色器中，這也可以是執行緒群組的共用記憶體 (g \#) 。</span><span class="sxs-lookup"><span data-stu-id="ff3cf-114">In the compute shader this can also be thread group shared memory (g\#).</span></span> <br/> |
| <span data-ttu-id="ff3cf-115"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*</span><span class="sxs-lookup"><span data-stu-id="ff3cf-115"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*</span></span><br/> | <span data-ttu-id="ff3cf-116">\[在 \] 記憶體位址中。</span><span class="sxs-lookup"><span data-stu-id="ff3cf-116">\[in\] The memory address.</span></span><br/>                                                                                             |
| <span data-ttu-id="ff3cf-117"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="ff3cf-117"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                                | <span data-ttu-id="ff3cf-118">*Dst1* 的值。</span><span class="sxs-lookup"><span data-stu-id="ff3cf-118">The value to OR with *dst1*.</span></span><br/>                                                                                           |



 

## <a name="remarks"></a><span data-ttu-id="ff3cf-119">備註</span><span class="sxs-lookup"><span data-stu-id="ff3cf-119">Remarks</span></span>

<span data-ttu-id="ff3cf-120">此指令會在每個元件位址 *dstAddress* 的32位上執行單一元件32位位 or of 運算元 *src0* with *dst1* 。</span><span class="sxs-lookup"><span data-stu-id="ff3cf-120">This instruction performs a single component 32-bit bitwise OR of operand *src0* with *dst1* at 32-bit per component address *dstAddress*.</span></span>

<span data-ttu-id="ff3cf-121">如果 *dst1* 是 u \# ，則可能已宣告為 raw、具型別或結構化。</span><span class="sxs-lookup"><span data-stu-id="ff3cf-121">If *dst1* is a u\#, it may have been declared as raw, typed or structured.</span></span> <span data-ttu-id="ff3cf-122">如果具型別，則必須使用 R32 uint/聖的系結資源格式宣告為 UINT/聖 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="ff3cf-122">If typed, it must be declared as UINT/SINT with the bound resource format being R32\_UINT/\_SINT.</span></span>

<span data-ttu-id="ff3cf-123">如果 *dst1* 為 g \# ，則必須將它宣告為 raw 或結構化。</span><span class="sxs-lookup"><span data-stu-id="ff3cf-123">If *dst1* is g\#, it must be declared as raw or structured.</span></span>

<span data-ttu-id="ff3cf-124">在或之前 *dst1* 記憶體中的值會傳回至 *dst0*。</span><span class="sxs-lookup"><span data-stu-id="ff3cf-124">The value in *dst1* memory before the OR is returned to *dst0*.</span></span>

<span data-ttu-id="ff3cf-125">整個作業會以不可部分完成的方式執行。</span><span class="sxs-lookup"><span data-stu-id="ff3cf-125">The entire operation is performed atomically.</span></span>

<span data-ttu-id="ff3cf-126">從位址取得的元件數目取決於在 *dst1* 中宣告之資源的維度。</span><span class="sxs-lookup"><span data-stu-id="ff3cf-126">The number of components taken from the address is determined by the dimensionality of the resource declared at *dst1*.</span></span>

<span data-ttu-id="ff3cf-127">如果著色器調用處于非使用中狀態，例如，如果圖元先前在其執行過程中已捨棄，或圖元/樣本調用僅存在做為衍生的真實圖元/樣本的協助程式，則此指令完全不會改變 *dst1* 記憶體，且傳回的值為未定義。</span><span class="sxs-lookup"><span data-stu-id="ff3cf-127">If the shader invocation is inactive, for example if the pixel has been discarded earlier in its execution, or a pixel/sample invocation only exists to serve as a helper to a real pixel/sample for derivatives, this instruction does not alter the *dst1* memory at all, and the returned value is undefined.</span></span>

<span data-ttu-id="ff3cf-128">除了 u 的範圍外， \# 不會將任何內容寫入記憶體，除非 u \# 是結構化的，且在結構 (第二個元件) 的結構中的位元組位移會造成超出界限存取權，否則 UAV 的整個內容會變成未定義。</span><span class="sxs-lookup"><span data-stu-id="ff3cf-128">Out of bounds addressing on u\# causes nothing to be written to memory, except if the u\# is structured, and byte offset into the struct (second component of the address) is causing the out of bounds access, then the entire contents of the UAV become undefined.</span></span>

<span data-ttu-id="ff3cf-129">U 或 g 的超出範圍定址 \# \# 會導致未定義的結果傳回 *dst0* 中的著色器。</span><span class="sxs-lookup"><span data-stu-id="ff3cf-129">Out of bounds addressing on u\# or g\# causes an undefined result to be returned to the shader in *dst0*.</span></span>

<span data-ttu-id="ff3cf-130">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="ff3cf-130">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="ff3cf-131">頂點</span><span class="sxs-lookup"><span data-stu-id="ff3cf-131">Vertex</span></span> | <span data-ttu-id="ff3cf-132">船體</span><span class="sxs-lookup"><span data-stu-id="ff3cf-132">Hull</span></span> | <span data-ttu-id="ff3cf-133">網域</span><span class="sxs-lookup"><span data-stu-id="ff3cf-133">Domain</span></span> | <span data-ttu-id="ff3cf-134">幾何</span><span class="sxs-lookup"><span data-stu-id="ff3cf-134">Geometry</span></span> | <span data-ttu-id="ff3cf-135">像素</span><span class="sxs-lookup"><span data-stu-id="ff3cf-135">Pixel</span></span> | <span data-ttu-id="ff3cf-136">計算</span><span class="sxs-lookup"><span data-stu-id="ff3cf-136">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="ff3cf-137">X</span><span class="sxs-lookup"><span data-stu-id="ff3cf-137">X</span></span>     | <span data-ttu-id="ff3cf-138">X</span><span class="sxs-lookup"><span data-stu-id="ff3cf-138">X</span></span>       |



 

<span data-ttu-id="ff3cf-139">由於 UAVs 可在 Direct3D 11.1 的所有著色器階段使用，因此此指示適用于 Direct3D 11.1 執行時間的所有著色器階段，從 Windows 8 開始提供。</span><span class="sxs-lookup"><span data-stu-id="ff3cf-139">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="ff3cf-140">頂點</span><span class="sxs-lookup"><span data-stu-id="ff3cf-140">Vertex</span></span> | <span data-ttu-id="ff3cf-141">船體</span><span class="sxs-lookup"><span data-stu-id="ff3cf-141">Hull</span></span> | <span data-ttu-id="ff3cf-142">網域</span><span class="sxs-lookup"><span data-stu-id="ff3cf-142">Domain</span></span> | <span data-ttu-id="ff3cf-143">幾何</span><span class="sxs-lookup"><span data-stu-id="ff3cf-143">Geometry</span></span> | <span data-ttu-id="ff3cf-144">像素</span><span class="sxs-lookup"><span data-stu-id="ff3cf-144">Pixel</span></span> | <span data-ttu-id="ff3cf-145">計算</span><span class="sxs-lookup"><span data-stu-id="ff3cf-145">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="ff3cf-146">X</span><span class="sxs-lookup"><span data-stu-id="ff3cf-146">X</span></span>      | <span data-ttu-id="ff3cf-147">X</span><span class="sxs-lookup"><span data-stu-id="ff3cf-147">X</span></span>    | <span data-ttu-id="ff3cf-148">X</span><span class="sxs-lookup"><span data-stu-id="ff3cf-148">X</span></span>      | <span data-ttu-id="ff3cf-149">X</span><span class="sxs-lookup"><span data-stu-id="ff3cf-149">X</span></span>        | <span data-ttu-id="ff3cf-150">X</span><span class="sxs-lookup"><span data-stu-id="ff3cf-150">X</span></span>     | <span data-ttu-id="ff3cf-151">X</span><span class="sxs-lookup"><span data-stu-id="ff3cf-151">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="ff3cf-152">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="ff3cf-152">Minimum Shader Model</span></span>

<span data-ttu-id="ff3cf-153">下列著色器模型支援此指令：</span><span class="sxs-lookup"><span data-stu-id="ff3cf-153">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="ff3cf-154">著色器模型</span><span class="sxs-lookup"><span data-stu-id="ff3cf-154">Shader Model</span></span>                                              | <span data-ttu-id="ff3cf-155">支援</span><span class="sxs-lookup"><span data-stu-id="ff3cf-155">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="ff3cf-156">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="ff3cf-156">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="ff3cf-157">是</span><span class="sxs-lookup"><span data-stu-id="ff3cf-157">yes</span></span>       |
| [<span data-ttu-id="ff3cf-158">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="ff3cf-158">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="ff3cf-159">不可以</span><span class="sxs-lookup"><span data-stu-id="ff3cf-159">no</span></span>        |
| [<span data-ttu-id="ff3cf-160">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="ff3cf-160">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="ff3cf-161">不可以</span><span class="sxs-lookup"><span data-stu-id="ff3cf-161">no</span></span>        |
| [<span data-ttu-id="ff3cf-162">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="ff3cf-162">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="ff3cf-163">不可以</span><span class="sxs-lookup"><span data-stu-id="ff3cf-163">no</span></span>        |
| [<span data-ttu-id="ff3cf-164">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="ff3cf-164">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="ff3cf-165">不可以</span><span class="sxs-lookup"><span data-stu-id="ff3cf-165">no</span></span>        |
| [<span data-ttu-id="ff3cf-166">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="ff3cf-166">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="ff3cf-167">不可以</span><span class="sxs-lookup"><span data-stu-id="ff3cf-167">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="ff3cf-168">相關主題</span><span class="sxs-lookup"><span data-stu-id="ff3cf-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ff3cf-169">著色器模型5元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="ff3cf-169">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





