---
title: 'imm_atomic_iadd (sm5-asm) '
description: 立即不可部分完成的整數加入至記憶體。 在加入之前，傳回記憶體中的值。
ms.assetid: 24136B4C-D37C-4449-A318-57145BB8D8E9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2695e23707fb61cd576748e2e83829cd7dc65259
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104373855"
---
# <a name="imm_atomic_iadd-sm5---asm"></a><span data-ttu-id="aa65b-104">imm 不可部分完成 \_ \_ iadd (sm5-asm) </span><span class="sxs-lookup"><span data-stu-id="aa65b-104">imm\_atomic\_iadd (sm5 - asm)</span></span>

<span data-ttu-id="aa65b-105">立即不可部分完成的整數加入至記憶體。</span><span class="sxs-lookup"><span data-stu-id="aa65b-105">Immediate atomic integer add to memory.</span></span> <span data-ttu-id="aa65b-106">在加入之前，傳回記憶體中的值。</span><span class="sxs-lookup"><span data-stu-id="aa65b-106">Returns the value in memory before the add.</span></span>



| <span data-ttu-id="aa65b-107">imm \_ 不可 \_ 部分完成 iadd dst0 \[ 。單一 \_ 元件 \_ 遮罩 \] 、dst1、dstAddress \[ . swizzle \] 、src0 \[ 。選取 \_ 元件\]</span><span class="sxs-lookup"><span data-stu-id="aa65b-107">imm\_atomic\_iadd dst0\[.single\_component\_mask\], dst1, dstAddress\[.swizzle\], src0\[.select\_component\]</span></span> |
|--------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="aa65b-108">項目</span><span class="sxs-lookup"><span data-stu-id="aa65b-108">Item</span></span>                                                                                                           | <span data-ttu-id="aa65b-109">描述</span><span class="sxs-lookup"><span data-stu-id="aa65b-109">Description</span></span>                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa65b-110"><span id="dst0"></span><span id="DST0"></span>*dst0*</span><span class="sxs-lookup"><span data-stu-id="aa65b-110"><span id="dst0"></span><span id="DST0"></span>*dst0*</span></span><br/>                                                | <span data-ttu-id="aa65b-111">\[中 \] 的包含在寫入之前的 *dst1* 值。</span><span class="sxs-lookup"><span data-stu-id="aa65b-111">\[in\] Contains the value in *dst1* before the write.</span></span> <br/>                                                                           |
| <span data-ttu-id="aa65b-112"><span id="dst1"></span><span id="DST1"></span>*dst1*</span><span class="sxs-lookup"><span data-stu-id="aa65b-112"><span id="dst1"></span><span id="DST1"></span>*dst1*</span></span><br/>                                                | <span data-ttu-id="aa65b-113">此值必須是未排序的存取視圖 (UAV)  (u \#) 。</span><span class="sxs-lookup"><span data-stu-id="aa65b-113">This value must be an unordered access view (UAV) (u\#).</span></span> <span data-ttu-id="aa65b-114">在計算著色器中，它也可以是執行緒群組的共用記憶體 (g \#) 。</span><span class="sxs-lookup"><span data-stu-id="aa65b-114">In the compute shader it can also be thread group shared memory (g\#).</span></span> <br/> |
| <span data-ttu-id="aa65b-115"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*</span><span class="sxs-lookup"><span data-stu-id="aa65b-115"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*</span></span><br/> | <span data-ttu-id="aa65b-116">\[在 \] [記憶體] naddress 中。</span><span class="sxs-lookup"><span data-stu-id="aa65b-116">\[in\] The memory naddress.</span></span><br/>                                                                                                      |
| <span data-ttu-id="aa65b-117"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="aa65b-117"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                                | <span data-ttu-id="aa65b-118">\[在 \] [要加入至 *dst1* 的值] 中。</span><span class="sxs-lookup"><span data-stu-id="aa65b-118">\[in\] The value to add to *dst1*.</span></span><br/>                                                                                               |



 

## <a name="remarks"></a><span data-ttu-id="aa65b-119">備註</span><span class="sxs-lookup"><span data-stu-id="aa65b-119">Remarks</span></span>

<span data-ttu-id="aa65b-120">此指令會在每個元件位址 *dstAddress* 的32位上執行具有 *dst1* 的運算元 *src0* 的單一元件32位整數新增。</span><span class="sxs-lookup"><span data-stu-id="aa65b-120">This instruction performs a single component 32-bit integer add of operand *src0* with *dst1* at 32-bit per component address *dstAddress*.</span></span> <span data-ttu-id="aa65b-121">不區分正負號。</span><span class="sxs-lookup"><span data-stu-id="aa65b-121">It is insensitive to sign.</span></span>

<span data-ttu-id="aa65b-122">如果 *dst1* 是 u \# ，則可能已宣告為 raw、具型別或結構化。</span><span class="sxs-lookup"><span data-stu-id="aa65b-122">If *dst1* is a u\#, it may have been declared as raw, typed or structured.</span></span> <span data-ttu-id="aa65b-123">如果具型別，則必須使用 R32 uint/聖的系結資源格式宣告為 UINT/聖 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="aa65b-123">If typed, it must be declared as UINT/SINT with the bound resource format being R32\_UINT/\_SINT.</span></span>

<span data-ttu-id="aa65b-124">如果 *dst1* 為 g \# ，則必須將它宣告為 raw 或結構化。</span><span class="sxs-lookup"><span data-stu-id="aa65b-124">If *dst1* is g\#, it must be declared as raw or structured.</span></span>

<span data-ttu-id="aa65b-125">*Dst1* 記憶體中的值會在加法之前傳回 *dst0*。</span><span class="sxs-lookup"><span data-stu-id="aa65b-125">The value in *dst1* memory before addition is returned to *dst0*.</span></span>

<span data-ttu-id="aa65b-126">從位址取得的元件數目取決於 *dst1* 的維度。</span><span class="sxs-lookup"><span data-stu-id="aa65b-126">The number of components taken from the address is determined by the dimensionality of *dst1*.</span></span>

<span data-ttu-id="aa65b-127">整個作業會以不可部分完成的方式執行。</span><span class="sxs-lookup"><span data-stu-id="aa65b-127">The entire operation is performed atomically.</span></span>

<span data-ttu-id="aa65b-128">如果著色器調用處于非使用中狀態，例如，如果圖元先前在其執行過程中已捨棄，或圖元/樣本調用僅存在做為衍生的真實圖元/樣本的協助程式，則此指令完全不會改變 *dst1* 記憶體，且傳回的值為未定義。</span><span class="sxs-lookup"><span data-stu-id="aa65b-128">If the shader invocation is inactive, for example if the pixel has been discarded earlier in its execution, or a pixel/sample invocation only exists to serve as a helper to a real pixel/sample for derivatives, this instruction does not alter the *dst1* memory at all, and the returned value is undefined.</span></span>

<span data-ttu-id="aa65b-129">除了 u 的範圍外， \# 不會將任何內容寫入記憶體，除非 u \# 是結構化的，且在結構 (第二個元件) 的結構中的位元組位移會造成超出界限存取權，否則 UAV 的整個內容會變成未定義。</span><span class="sxs-lookup"><span data-stu-id="aa65b-129">Out of bounds addressing on u\# causes nothing to be written to memory, except if the u\# is structured, and byte offset into the struct (second component of the address) is causing the out of bounds access, then the entire contents of the UAV become undefined.</span></span>

<span data-ttu-id="aa65b-130">U 或 g 的超出範圍定址 \# \# 會導致未定義的結果傳回 *dst0* 中的著色器。</span><span class="sxs-lookup"><span data-stu-id="aa65b-130">Out of bounds addressing on u\# or g\# causes an undefined result to be returned to the shader in *dst0*.</span></span>

<span data-ttu-id="aa65b-131">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="aa65b-131">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="aa65b-132">頂點</span><span class="sxs-lookup"><span data-stu-id="aa65b-132">Vertex</span></span> | <span data-ttu-id="aa65b-133">船體</span><span class="sxs-lookup"><span data-stu-id="aa65b-133">Hull</span></span> | <span data-ttu-id="aa65b-134">網域</span><span class="sxs-lookup"><span data-stu-id="aa65b-134">Domain</span></span> | <span data-ttu-id="aa65b-135">幾何</span><span class="sxs-lookup"><span data-stu-id="aa65b-135">Geometry</span></span> | <span data-ttu-id="aa65b-136">像素</span><span class="sxs-lookup"><span data-stu-id="aa65b-136">Pixel</span></span> | <span data-ttu-id="aa65b-137">計算</span><span class="sxs-lookup"><span data-stu-id="aa65b-137">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="aa65b-138">X</span><span class="sxs-lookup"><span data-stu-id="aa65b-138">X</span></span>     | <span data-ttu-id="aa65b-139">X</span><span class="sxs-lookup"><span data-stu-id="aa65b-139">X</span></span>       |



 

<span data-ttu-id="aa65b-140">由於 UAVs 可在 Direct3D 11.1 的所有著色器階段使用，因此此指示適用于 Direct3D 11.1 執行時間的所有著色器階段，從 Windows 8 開始提供。</span><span class="sxs-lookup"><span data-stu-id="aa65b-140">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="aa65b-141">頂點</span><span class="sxs-lookup"><span data-stu-id="aa65b-141">Vertex</span></span> | <span data-ttu-id="aa65b-142">船體</span><span class="sxs-lookup"><span data-stu-id="aa65b-142">Hull</span></span> | <span data-ttu-id="aa65b-143">網域</span><span class="sxs-lookup"><span data-stu-id="aa65b-143">Domain</span></span> | <span data-ttu-id="aa65b-144">幾何</span><span class="sxs-lookup"><span data-stu-id="aa65b-144">Geometry</span></span> | <span data-ttu-id="aa65b-145">像素</span><span class="sxs-lookup"><span data-stu-id="aa65b-145">Pixel</span></span> | <span data-ttu-id="aa65b-146">計算</span><span class="sxs-lookup"><span data-stu-id="aa65b-146">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="aa65b-147">X</span><span class="sxs-lookup"><span data-stu-id="aa65b-147">X</span></span>      | <span data-ttu-id="aa65b-148">X</span><span class="sxs-lookup"><span data-stu-id="aa65b-148">X</span></span>    | <span data-ttu-id="aa65b-149">X</span><span class="sxs-lookup"><span data-stu-id="aa65b-149">X</span></span>      | <span data-ttu-id="aa65b-150">X</span><span class="sxs-lookup"><span data-stu-id="aa65b-150">X</span></span>        | <span data-ttu-id="aa65b-151">X</span><span class="sxs-lookup"><span data-stu-id="aa65b-151">X</span></span>     | <span data-ttu-id="aa65b-152">X</span><span class="sxs-lookup"><span data-stu-id="aa65b-152">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="aa65b-153">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="aa65b-153">Minimum Shader Model</span></span>

<span data-ttu-id="aa65b-154">下列著色器模型支援此指令：</span><span class="sxs-lookup"><span data-stu-id="aa65b-154">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="aa65b-155">著色器模型</span><span class="sxs-lookup"><span data-stu-id="aa65b-155">Shader Model</span></span>                                              | <span data-ttu-id="aa65b-156">支援</span><span class="sxs-lookup"><span data-stu-id="aa65b-156">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="aa65b-157">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="aa65b-157">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="aa65b-158">是</span><span class="sxs-lookup"><span data-stu-id="aa65b-158">yes</span></span>       |
| [<span data-ttu-id="aa65b-159">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="aa65b-159">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="aa65b-160">不可以</span><span class="sxs-lookup"><span data-stu-id="aa65b-160">no</span></span>        |
| [<span data-ttu-id="aa65b-161">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="aa65b-161">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="aa65b-162">不可以</span><span class="sxs-lookup"><span data-stu-id="aa65b-162">no</span></span>        |
| [<span data-ttu-id="aa65b-163">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="aa65b-163">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="aa65b-164">不可以</span><span class="sxs-lookup"><span data-stu-id="aa65b-164">no</span></span>        |
| [<span data-ttu-id="aa65b-165">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="aa65b-165">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="aa65b-166">不可以</span><span class="sxs-lookup"><span data-stu-id="aa65b-166">no</span></span>        |
| [<span data-ttu-id="aa65b-167">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="aa65b-167">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="aa65b-168">不可以</span><span class="sxs-lookup"><span data-stu-id="aa65b-168">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="aa65b-169">相關主題</span><span class="sxs-lookup"><span data-stu-id="aa65b-169">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aa65b-170">著色器模型5元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="aa65b-170">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





