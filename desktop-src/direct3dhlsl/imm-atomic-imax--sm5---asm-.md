---
title: 'imm_atomic_imax (sm5-asm) '
description: 立即可部分完成的帶正負號的最大記憶體。 傳回 max 作業之前的記憶體值。
ms.assetid: 360E542C-F3F6-4103-8A22-4914A5103D17
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8143073065955a00df412ecf453cc523d7e98493
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "103932821"
---
# <a name="imm_atomic_imax-sm5---asm"></a><span data-ttu-id="41ea0-104">imm 不可部分完成 \_ \_ imax (sm5-asm) </span><span class="sxs-lookup"><span data-stu-id="41ea0-104">imm\_atomic\_imax (sm5 - asm)</span></span>

<span data-ttu-id="41ea0-105">立即可部分完成的帶正負號的最大記憶體。</span><span class="sxs-lookup"><span data-stu-id="41ea0-105">Immediate atomic signed max to memory.</span></span> <span data-ttu-id="41ea0-106">傳回 max 作業之前的記憶體值。</span><span class="sxs-lookup"><span data-stu-id="41ea0-106">Returns value in memory before the max operation.</span></span>



| <span data-ttu-id="41ea0-107">imm \_ 不可 \_ 部分完成 imax dst0 \[ 。單一 \_ 元件 \_ 遮罩 \] 、dst1、dstAddress \[ . swizzle \] 、src0 \[ 。選取 \_ 元件\]</span><span class="sxs-lookup"><span data-stu-id="41ea0-107">imm\_atomic\_imax dst0\[.single\_component\_mask\], dst1, dstAddress\[.swizzle\], src0\[.select\_component\]</span></span> |
|--------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="41ea0-108">項目</span><span class="sxs-lookup"><span data-stu-id="41ea0-108">Item</span></span>                                                                                                           | <span data-ttu-id="41ea0-109">描述</span><span class="sxs-lookup"><span data-stu-id="41ea0-109">Description</span></span>                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41ea0-110"><span id="dst0"></span><span id="DST0"></span>*dst0*</span><span class="sxs-lookup"><span data-stu-id="41ea0-110"><span id="dst0"></span><span id="DST0"></span>*dst0*</span></span><br/>                                                | <span data-ttu-id="41ea0-111">\[in \] 包含此指令之前的 *dst1* 值。</span><span class="sxs-lookup"><span data-stu-id="41ea0-111">\[in\] Contains the value from *dst1* before this instruction.</span></span><br/>                                                         |
| <span data-ttu-id="41ea0-112"><span id="dst1"></span><span id="DST1"></span>*dst1*</span><span class="sxs-lookup"><span data-stu-id="41ea0-112"><span id="dst1"></span><span id="DST1"></span>*dst1*</span></span><br/>                                                | <span data-ttu-id="41ea0-113">\[在 \] 未排序的存取視圖中 (UAV)  (u \#) 。</span><span class="sxs-lookup"><span data-stu-id="41ea0-113">\[in\] An unordered access view (UAV) (u\#).</span></span> <span data-ttu-id="41ea0-114">在計算著色器中，這也可以是執行緒群組的共用記憶體 (g \#) 。</span><span class="sxs-lookup"><span data-stu-id="41ea0-114">In the compute shader this can also be thread group shared memory (g\#).</span></span> <br/> |
| <span data-ttu-id="41ea0-115"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*</span><span class="sxs-lookup"><span data-stu-id="41ea0-115"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*</span></span><br/> | <span data-ttu-id="41ea0-116">\[在 \] 記憶體位址中。</span><span class="sxs-lookup"><span data-stu-id="41ea0-116">\[in\] The memory address.</span></span><br/>                                                                                             |
| <span data-ttu-id="41ea0-117"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="41ea0-117"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                                | <span data-ttu-id="41ea0-118">\[在 \] [要與 *dst1* 比較的值 *dstAddress*] 中。</span><span class="sxs-lookup"><span data-stu-id="41ea0-118">\[in\] The value to compare to *dst1* at *dstAddress*.</span></span><br/>                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="41ea0-119">備註</span><span class="sxs-lookup"><span data-stu-id="41ea0-119">Remarks</span></span>

<span data-ttu-id="41ea0-120">此指令會在每個元件位址 *dstAddress* 的32位上執行具有 *dst1* 的運算元 *src0* 的單一元件32位帶正負號的最大值。</span><span class="sxs-lookup"><span data-stu-id="41ea0-120">This instruction performs a single component 32-bit signed maximum of operand *src0* with *dst1* at 32-bit per component address *dstAddress*.</span></span>

<span data-ttu-id="41ea0-121">如果 *dst1* 是 u \# ，則可能已宣告為 raw、具型別或結構化。</span><span class="sxs-lookup"><span data-stu-id="41ea0-121">If *dst1* is a u\#, it may have been declared as raw, typed or structured.</span></span> <span data-ttu-id="41ea0-122">如果具型別，則必須使用 R32 uint/聖的系結資源格式宣告為 UINT/聖 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="41ea0-122">If typed, it must be declared as UINT/SINT with the bound resource format being R32\_UINT/\_SINT.</span></span>

<span data-ttu-id="41ea0-123">如果 *dst1* 為 g \# ，則必須將它宣告為 raw 或結構化。</span><span class="sxs-lookup"><span data-stu-id="41ea0-123">If *dst1* is g\#, it must be declared as raw or structured.</span></span>

<span data-ttu-id="41ea0-124">在 max 之前， *dst1* 記憶體中的值會傳回至 *dst0*。</span><span class="sxs-lookup"><span data-stu-id="41ea0-124">The value in *dst1* memory before max is returned to *dst0*.</span></span>

<span data-ttu-id="41ea0-125">從位址取得的元件數目取決於 *dst1* 的維度。</span><span class="sxs-lookup"><span data-stu-id="41ea0-125">The number of components taken from the address is determined by the dimensionality of *dst1*.</span></span>

<span data-ttu-id="41ea0-126">整個作業會以不可部分完成的方式執行。</span><span class="sxs-lookup"><span data-stu-id="41ea0-126">The entire operation is performed atomically.</span></span>

<span data-ttu-id="41ea0-127">如果著色器調用處于非使用中狀態，例如，如果圖元先前在其執行過程中已捨棄，或圖元/樣本調用僅存在做為衍生的真實圖元/樣本的協助程式，則此指令完全不會改變 *dst1* 記憶體，且傳回的值為未定義。</span><span class="sxs-lookup"><span data-stu-id="41ea0-127">If the shader invocation is inactive, for example if the pixel has been discarded earlier in its execution, or a pixel/sample invocation only exists to serve as a helper to a real pixel/sample for derivatives, this instruction does not alter the *dst1* memory at all, and the returned value is undefined.</span></span>

<span data-ttu-id="41ea0-128">除了 u 的範圍外， \# 不會將任何內容寫入記憶體，除非 u \# 是結構化的，且在結構 (第二個元件) 的結構中的位元組位移會造成超出界限存取權，否則 UAV 的整個內容會變成未定義。</span><span class="sxs-lookup"><span data-stu-id="41ea0-128">Out of bounds addressing on u\# causes nothing to be written to memory, except if the u\# is structured, and byte offset into the struct (second component of the address) is causing the out of bounds access, then the entire contents of the UAV become undefined.</span></span>

<span data-ttu-id="41ea0-129">U 或 g 的超出範圍定址 \# \# 會導致未定義的結果傳回 *dst0* 中的著色器。</span><span class="sxs-lookup"><span data-stu-id="41ea0-129">Out of bounds addressing on u\# or g\# causes an undefined result to be returned to the shader in *dst0*.</span></span>

<span data-ttu-id="41ea0-130">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="41ea0-130">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="41ea0-131">頂點</span><span class="sxs-lookup"><span data-stu-id="41ea0-131">Vertex</span></span> | <span data-ttu-id="41ea0-132">船體</span><span class="sxs-lookup"><span data-stu-id="41ea0-132">Hull</span></span> | <span data-ttu-id="41ea0-133">網域</span><span class="sxs-lookup"><span data-stu-id="41ea0-133">Domain</span></span> | <span data-ttu-id="41ea0-134">幾何</span><span class="sxs-lookup"><span data-stu-id="41ea0-134">Geometry</span></span> | <span data-ttu-id="41ea0-135">像素</span><span class="sxs-lookup"><span data-stu-id="41ea0-135">Pixel</span></span> | <span data-ttu-id="41ea0-136">計算</span><span class="sxs-lookup"><span data-stu-id="41ea0-136">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="41ea0-137">X</span><span class="sxs-lookup"><span data-stu-id="41ea0-137">X</span></span>     | <span data-ttu-id="41ea0-138">X</span><span class="sxs-lookup"><span data-stu-id="41ea0-138">X</span></span>       |



 

<span data-ttu-id="41ea0-139">由於 UAVs 可在 Direct3D 11.1 的所有著色器階段使用，因此此指示適用于 Direct3D 11.1 執行時間的所有著色器階段，從 Windows 8 開始提供。</span><span class="sxs-lookup"><span data-stu-id="41ea0-139">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="41ea0-140">頂點</span><span class="sxs-lookup"><span data-stu-id="41ea0-140">Vertex</span></span> | <span data-ttu-id="41ea0-141">船體</span><span class="sxs-lookup"><span data-stu-id="41ea0-141">Hull</span></span> | <span data-ttu-id="41ea0-142">網域</span><span class="sxs-lookup"><span data-stu-id="41ea0-142">Domain</span></span> | <span data-ttu-id="41ea0-143">幾何</span><span class="sxs-lookup"><span data-stu-id="41ea0-143">Geometry</span></span> | <span data-ttu-id="41ea0-144">像素</span><span class="sxs-lookup"><span data-stu-id="41ea0-144">Pixel</span></span> | <span data-ttu-id="41ea0-145">計算</span><span class="sxs-lookup"><span data-stu-id="41ea0-145">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="41ea0-146">X</span><span class="sxs-lookup"><span data-stu-id="41ea0-146">X</span></span>      | <span data-ttu-id="41ea0-147">X</span><span class="sxs-lookup"><span data-stu-id="41ea0-147">X</span></span>    | <span data-ttu-id="41ea0-148">X</span><span class="sxs-lookup"><span data-stu-id="41ea0-148">X</span></span>      | <span data-ttu-id="41ea0-149">X</span><span class="sxs-lookup"><span data-stu-id="41ea0-149">X</span></span>        | <span data-ttu-id="41ea0-150">X</span><span class="sxs-lookup"><span data-stu-id="41ea0-150">X</span></span>     | <span data-ttu-id="41ea0-151">X</span><span class="sxs-lookup"><span data-stu-id="41ea0-151">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="41ea0-152">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="41ea0-152">Minimum Shader Model</span></span>

<span data-ttu-id="41ea0-153">下列著色器模型支援此指令：</span><span class="sxs-lookup"><span data-stu-id="41ea0-153">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="41ea0-154">著色器模型</span><span class="sxs-lookup"><span data-stu-id="41ea0-154">Shader Model</span></span>                                              | <span data-ttu-id="41ea0-155">支援</span><span class="sxs-lookup"><span data-stu-id="41ea0-155">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="41ea0-156">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="41ea0-156">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="41ea0-157">是</span><span class="sxs-lookup"><span data-stu-id="41ea0-157">yes</span></span>       |
| [<span data-ttu-id="41ea0-158">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="41ea0-158">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="41ea0-159">不可以</span><span class="sxs-lookup"><span data-stu-id="41ea0-159">no</span></span>        |
| [<span data-ttu-id="41ea0-160">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="41ea0-160">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="41ea0-161">不可以</span><span class="sxs-lookup"><span data-stu-id="41ea0-161">no</span></span>        |
| [<span data-ttu-id="41ea0-162">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="41ea0-162">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="41ea0-163">不可以</span><span class="sxs-lookup"><span data-stu-id="41ea0-163">no</span></span>        |
| [<span data-ttu-id="41ea0-164">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="41ea0-164">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="41ea0-165">不可以</span><span class="sxs-lookup"><span data-stu-id="41ea0-165">no</span></span>        |
| [<span data-ttu-id="41ea0-166">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="41ea0-166">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="41ea0-167">不可以</span><span class="sxs-lookup"><span data-stu-id="41ea0-167">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="41ea0-168">相關主題</span><span class="sxs-lookup"><span data-stu-id="41ea0-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="41ea0-169">著色器模型5元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="41ea0-169">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





