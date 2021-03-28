---
title: 'atomic_iadd (sm5-asm) '
description: 將不可部分完成的整數加入至記憶體。
ms.assetid: 093C7FA5-41BF-4BDD-A35D-1AACE8CB9B5C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6a8652d4e29aae9f32a84f7a4e4d477abd54b7c
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104313731"
---
# <a name="atomic_iadd-sm5---asm"></a><span data-ttu-id="7b41c-103">不可部分完成 \_ 的 iadd (sm5-asm) </span><span class="sxs-lookup"><span data-stu-id="7b41c-103">atomic\_iadd (sm5 - asm)</span></span>

<span data-ttu-id="7b41c-104">將不可部分完成的整數加入至記憶體。</span><span class="sxs-lookup"><span data-stu-id="7b41c-104">Atomic integer add to memory.</span></span>



| <span data-ttu-id="7b41c-105">不可 \_ 部分完成的 iadd dst，dstAddress \[ . swizzle \] ，src0 \[ . select \_ component\]</span><span class="sxs-lookup"><span data-stu-id="7b41c-105">atomic\_iadd dst, dstAddress\[.swizzle\], src0\[.select\_component\]</span></span> |
|----------------------------------------------------------------------|



 



| <span data-ttu-id="7b41c-106">項目</span><span class="sxs-lookup"><span data-stu-id="7b41c-106">Item</span></span>                                                                                                           | <span data-ttu-id="7b41c-107">描述</span><span class="sxs-lookup"><span data-stu-id="7b41c-107">Description</span></span>                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b41c-108"><span id="dst"></span><span id="DST"></span>*Dst*</span><span class="sxs-lookup"><span data-stu-id="7b41c-108"><span id="dst"></span><span id="DST"></span>*dst*</span></span><br/>                                                   | <span data-ttu-id="7b41c-109">\[在 \] 要以 *src0* 新增的元件中。</span><span class="sxs-lookup"><span data-stu-id="7b41c-109">\[in\] The components to add with *src0*.</span></span> <span data-ttu-id="7b41c-110">此值必須是未排序的存取視圖 (UAV)  (u \#) 。</span><span class="sxs-lookup"><span data-stu-id="7b41c-110">This value must be an unordered access view (UAV) (u\#).</span></span> <span data-ttu-id="7b41c-111">在計算著色器中，它也可以是執行緒群組的共用記憶體 (g \#) 。</span><span class="sxs-lookup"><span data-stu-id="7b41c-111">In the compute shader it can also be thread group shared memory (g\#).</span></span> <br/> |
| <span data-ttu-id="7b41c-112"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*</span><span class="sxs-lookup"><span data-stu-id="7b41c-112"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*</span></span><br/> | <span data-ttu-id="7b41c-113">\[在 \] 記憶體位址中。</span><span class="sxs-lookup"><span data-stu-id="7b41c-113">\[in\] The memory address.</span></span><br/>                                                                                                                                                 |
| <span data-ttu-id="7b41c-114"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="7b41c-114"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                                | <span data-ttu-id="7b41c-115">\[在 \] 要加入至 *dst* 的元件中。</span><span class="sxs-lookup"><span data-stu-id="7b41c-115">\[in\] The components to add to *dst*.</span></span><br/>                                                                                                                                     |



 

## <a name="remarks"></a><span data-ttu-id="7b41c-116">備註</span><span class="sxs-lookup"><span data-stu-id="7b41c-116">Remarks</span></span>

<span data-ttu-id="7b41c-117">此指令會針對每個元件位址 DstAddress，在每個元件位址的每個元件中，執行 *src0* 至 *dst* 的單一元件32位整數，並32以自動方式執行。</span><span class="sxs-lookup"><span data-stu-id="7b41c-117">This instruction performs a single component 32-bit integer add of operand *src0* into *dst* at 32-bit per component address *dstAddress*, performed atomically.</span></span> <span data-ttu-id="7b41c-118">此指令不區分正負號。</span><span class="sxs-lookup"><span data-stu-id="7b41c-118">This instruction is insensitive to sign.</span></span>

<span data-ttu-id="7b41c-119">從位址取得的元件數目取決於 *dst* u \# 或 g 的維度 \# 。</span><span class="sxs-lookup"><span data-stu-id="7b41c-119">The number of components taken from the address is determined by the dimensionality of *dst* u\# or g\#.</span></span>

<span data-ttu-id="7b41c-120">如果 *dst* 是 u \# ，則可以宣告為 raw、具類型或結構化。</span><span class="sxs-lookup"><span data-stu-id="7b41c-120">If *dst* is a u\#, it can be declared as raw, typed or structured.</span></span> <span data-ttu-id="7b41c-121">如果具型別，則必須使用 R32 uint/聖的系結資源格式宣告為 UINT/聖 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="7b41c-121">If typed, it must be declared as UINT/SINT with the bound resource format being R32\_UINT/\_SINT.</span></span>

<span data-ttu-id="7b41c-122">如果 *dst* 為 g \# ，則必須將它宣告為 raw 或結構化。</span><span class="sxs-lookup"><span data-stu-id="7b41c-122">If *dst* is g\#, it must be declared as raw or structured.</span></span>

<span data-ttu-id="7b41c-123">沒有任何專案會傳回給著色器。</span><span class="sxs-lookup"><span data-stu-id="7b41c-123">Nothing is returned to the shader.</span></span>

<span data-ttu-id="7b41c-124">如果著色器調用處于非使用中狀態，例如，如果圖元在先前的執行中已被捨棄，或圖元/樣本調用僅存在做為衍生的真實圖元/樣本的協助程式，則此指令不會在所有 (無訊息的情況下變更 *dst* 記憶體) 。</span><span class="sxs-lookup"><span data-stu-id="7b41c-124">If the shader invocation is inactive, for example if the pixel has been discarded earlier in its execution, or if a pixel/sample invocation only exists to serve as a helper to a real pixel/sample for derivatives, this instruction does not alter the *dst* memory at all (silently).</span></span>

<span data-ttu-id="7b41c-125">除了 u 的範圍外， \# 不會將任何內容寫入記憶體，除非 u \# 是結構化的，且在結構 (第二個元件) 的結構中的位元組位移會造成超出界限存取權，否則 UAV 的整個內容會變成未定義。</span><span class="sxs-lookup"><span data-stu-id="7b41c-125">Out of bounds addressing on u\# causes nothing to be written to memory, except if the u\# is structured, and byte offset into the struct (second component of the address) is causing the out of bounds access, then the entire contents of the UAV become undefined.</span></span>

<span data-ttu-id="7b41c-126">G (超出範圍的界限 \# \# ，而不是所有的共用記憶體) 會導致所有共用記憶體的整個內容變成未定義。</span><span class="sxs-lookup"><span data-stu-id="7b41c-126">Out of bounds addressing on g\# (the bounds of that particular g\#, as opposed to all shared memory) causes the entire contents of all shared memory to become undefined.</span></span>

<span data-ttu-id="7b41c-127">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="7b41c-127">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="7b41c-128">頂點</span><span class="sxs-lookup"><span data-stu-id="7b41c-128">Vertex</span></span> | <span data-ttu-id="7b41c-129">船體</span><span class="sxs-lookup"><span data-stu-id="7b41c-129">Hull</span></span> | <span data-ttu-id="7b41c-130">網域</span><span class="sxs-lookup"><span data-stu-id="7b41c-130">Domain</span></span> | <span data-ttu-id="7b41c-131">幾何</span><span class="sxs-lookup"><span data-stu-id="7b41c-131">Geometry</span></span> | <span data-ttu-id="7b41c-132">像素</span><span class="sxs-lookup"><span data-stu-id="7b41c-132">Pixel</span></span> | <span data-ttu-id="7b41c-133">計算</span><span class="sxs-lookup"><span data-stu-id="7b41c-133">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="7b41c-134">X</span><span class="sxs-lookup"><span data-stu-id="7b41c-134">X</span></span>     | <span data-ttu-id="7b41c-135">X</span><span class="sxs-lookup"><span data-stu-id="7b41c-135">X</span></span>       |



 

<span data-ttu-id="7b41c-136">由於 UAVs 可在 Direct3D 11.1 的所有著色器階段使用，因此此指示適用于 Direct3D 11.1 執行時間的所有著色器階段，從 Windows 8 開始提供。</span><span class="sxs-lookup"><span data-stu-id="7b41c-136">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="7b41c-137">頂點</span><span class="sxs-lookup"><span data-stu-id="7b41c-137">Vertex</span></span> | <span data-ttu-id="7b41c-138">船體</span><span class="sxs-lookup"><span data-stu-id="7b41c-138">Hull</span></span> | <span data-ttu-id="7b41c-139">網域</span><span class="sxs-lookup"><span data-stu-id="7b41c-139">Domain</span></span> | <span data-ttu-id="7b41c-140">幾何</span><span class="sxs-lookup"><span data-stu-id="7b41c-140">Geometry</span></span> | <span data-ttu-id="7b41c-141">像素</span><span class="sxs-lookup"><span data-stu-id="7b41c-141">Pixel</span></span> | <span data-ttu-id="7b41c-142">計算</span><span class="sxs-lookup"><span data-stu-id="7b41c-142">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="7b41c-143">X</span><span class="sxs-lookup"><span data-stu-id="7b41c-143">X</span></span>      | <span data-ttu-id="7b41c-144">X</span><span class="sxs-lookup"><span data-stu-id="7b41c-144">X</span></span>    | <span data-ttu-id="7b41c-145">X</span><span class="sxs-lookup"><span data-stu-id="7b41c-145">X</span></span>      | <span data-ttu-id="7b41c-146">X</span><span class="sxs-lookup"><span data-stu-id="7b41c-146">X</span></span>        | <span data-ttu-id="7b41c-147">X</span><span class="sxs-lookup"><span data-stu-id="7b41c-147">X</span></span>     | <span data-ttu-id="7b41c-148">X</span><span class="sxs-lookup"><span data-stu-id="7b41c-148">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="7b41c-149">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="7b41c-149">Minimum Shader Model</span></span>

<span data-ttu-id="7b41c-150">下列著色器模型支援此指令：</span><span class="sxs-lookup"><span data-stu-id="7b41c-150">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="7b41c-151">著色器模型</span><span class="sxs-lookup"><span data-stu-id="7b41c-151">Shader Model</span></span>                                              | <span data-ttu-id="7b41c-152">支援</span><span class="sxs-lookup"><span data-stu-id="7b41c-152">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="7b41c-153">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="7b41c-153">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="7b41c-154">是</span><span class="sxs-lookup"><span data-stu-id="7b41c-154">yes</span></span>       |
| [<span data-ttu-id="7b41c-155">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="7b41c-155">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="7b41c-156">不可以</span><span class="sxs-lookup"><span data-stu-id="7b41c-156">no</span></span>        |
| [<span data-ttu-id="7b41c-157">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="7b41c-157">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="7b41c-158">不可以</span><span class="sxs-lookup"><span data-stu-id="7b41c-158">no</span></span>        |
| [<span data-ttu-id="7b41c-159">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="7b41c-159">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="7b41c-160">不可以</span><span class="sxs-lookup"><span data-stu-id="7b41c-160">no</span></span>        |
| [<span data-ttu-id="7b41c-161">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="7b41c-161">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="7b41c-162">不可以</span><span class="sxs-lookup"><span data-stu-id="7b41c-162">no</span></span>        |
| [<span data-ttu-id="7b41c-163">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="7b41c-163">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="7b41c-164">不可以</span><span class="sxs-lookup"><span data-stu-id="7b41c-164">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="7b41c-165">相關主題</span><span class="sxs-lookup"><span data-stu-id="7b41c-165">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7b41c-166">著色器模型5元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="7b41c-166">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





