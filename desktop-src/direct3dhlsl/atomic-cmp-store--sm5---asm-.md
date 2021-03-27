---
title: 'atomic_cmp_store (sm5-asm) '
description: 不可部分完成的比較和寫入至記憶體。
ms.assetid: 1B97E983-11A9-47E4-B274-E94083837C6E
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26a5292d65b32988017044a2ec52680848dffbef
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "103679160"
---
# <a name="atomic_cmp_store-sm5---asm"></a><span data-ttu-id="f65d2-103">不可部分完成 \_ \_ 的 cmp 存放區 (sm5-asm) </span><span class="sxs-lookup"><span data-stu-id="f65d2-103">atomic\_cmp\_store (sm5 - asm)</span></span>

<span data-ttu-id="f65d2-104">不可部分完成的比較和寫入至記憶體。</span><span class="sxs-lookup"><span data-stu-id="f65d2-104">Atomic compare and write to memory.</span></span>



| <span data-ttu-id="f65d2-105">不可 \_ \_ 部分完成的 cmp store Dst、dstAddress \[ . swizzle \] 、src0 \[ 。 select \_ component \] ，src1 \[ . select \_ component\]</span><span class="sxs-lookup"><span data-stu-id="f65d2-105">atomic\_cmp\_store dst, dstAddress\[.swizzle\], src0\[.select\_component\], src1\[.select\_component\]</span></span> |
|--------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="f65d2-106">項目</span><span class="sxs-lookup"><span data-stu-id="f65d2-106">Item</span></span>                                                                                                           | <span data-ttu-id="f65d2-107">描述</span><span class="sxs-lookup"><span data-stu-id="f65d2-107">Description</span></span>                                                                                                                                                                               |
|----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f65d2-108"><span id="dst"></span><span id="DST"></span>*Dst*</span><span class="sxs-lookup"><span data-stu-id="f65d2-108"><span id="dst"></span><span id="DST"></span>*dst*</span></span><br/>                                                   | <span data-ttu-id="f65d2-109">\[在 \] 要與 *src0* 比較的元件中。</span><span class="sxs-lookup"><span data-stu-id="f65d2-109">\[in\] The components to compare with *src0*.</span></span> <span data-ttu-id="f65d2-110">此值必須是未排序的存取視圖 (UAV)  (u \#) 。</span><span class="sxs-lookup"><span data-stu-id="f65d2-110">This value must be an unordered access view (UAV) (u\#).</span></span> <span data-ttu-id="f65d2-111">在計算著色器中，它也可以是執行緒群組的共用記憶體 (g \#) 。</span><span class="sxs-lookup"><span data-stu-id="f65d2-111">In the compute shader it can also be thread group shared memory (g\#).</span></span> <br/> |
| <span data-ttu-id="f65d2-112"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*</span><span class="sxs-lookup"><span data-stu-id="f65d2-112"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*</span></span><br/> | <span data-ttu-id="f65d2-113">\[在 \] 記憶體位址中。</span><span class="sxs-lookup"><span data-stu-id="f65d2-113">\[in\] The memory address.</span></span><br/>                                                                                                                                                     |
| <span data-ttu-id="f65d2-114"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="f65d2-114"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                                | <span data-ttu-id="f65d2-115">\[\]與 *dst* 比較的32位值。</span><span class="sxs-lookup"><span data-stu-id="f65d2-115">\[in\] The 32-bit value to compare with *dst*.</span></span><br/>                                                                                                                                 |
| <span data-ttu-id="f65d2-116"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="f65d2-116"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/>                                                | <span data-ttu-id="f65d2-117">\[\]如果比較的值相同，則為要寫入記憶體的值。</span><span class="sxs-lookup"><span data-stu-id="f65d2-117">\[in\] The value to write to memory if the compared values are identical.</span></span> <br/>                                                                                                     |



 

## <a name="remarks"></a><span data-ttu-id="f65d2-118">備註</span><span class="sxs-lookup"><span data-stu-id="f65d2-118">Remarks</span></span>

<span data-ttu-id="f65d2-119">此指令會在每個元件位址 *dstAddress* 的32位上執行運算元 *src0* 與 *dst* 的單一元件32位值比較。</span><span class="sxs-lookup"><span data-stu-id="f65d2-119">This instruction performs a single component 32-bit value compare of operand *src0* with *dst* at 32-bit per component address *dstAddress*.</span></span>

<span data-ttu-id="f65d2-120">如果比較的值相同， *src1* 中的單一元件32位值會寫入目的地記憶體。</span><span class="sxs-lookup"><span data-stu-id="f65d2-120">If the compared values are identical, the single-component 32-bit value in *src1* is written to destination memory.</span></span> <span data-ttu-id="f65d2-121">否則，不會變更目的地。</span><span class="sxs-lookup"><span data-stu-id="f65d2-121">Otherwise, the destination is not changed.</span></span>

<span data-ttu-id="f65d2-122">整個比較和寫入作業會以不可部分完成的方式執行。</span><span class="sxs-lookup"><span data-stu-id="f65d2-122">The entire compare and write operation is performed atomically.</span></span>

<span data-ttu-id="f65d2-123">如果 *dst* 是 u \# ，則可以宣告為 raw、具類型或結構化。</span><span class="sxs-lookup"><span data-stu-id="f65d2-123">If *dst* is a u\#, it can be declared as raw, typed or structured.</span></span> <span data-ttu-id="f65d2-124">如果具型別，則必須使用 R32 uint/聖的系結資源格式宣告為 UINT/聖 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="f65d2-124">If typed, it must be declared as UINT/SINT with the bound resource format being R32\_UINT/\_SINT.</span></span>

<span data-ttu-id="f65d2-125">如果 *dst* 為 g \# ，則必須將它宣告為 raw 或結構化。</span><span class="sxs-lookup"><span data-stu-id="f65d2-125">If *dst* is g\#, it must be declared as raw or structured.</span></span>

<span data-ttu-id="f65d2-126">從位址取得的元件數目取決於 dst u \# 或 g 的維度 \# 。</span><span class="sxs-lookup"><span data-stu-id="f65d2-126">The number of components taken from the address is determined by the dimensionality of dst u\# or g\#.</span></span>

<span data-ttu-id="f65d2-127">沒有任何專案會傳回給著色器。</span><span class="sxs-lookup"><span data-stu-id="f65d2-127">Nothing is returned to the shader.</span></span>

<span data-ttu-id="f65d2-128">如果著色器調用處于非使用中狀態，例如，如果已在其執行之前捨棄圖元，或圖元/範例指令未以無訊息方式變更所有 (的 *dst* 記憶體) 。</span><span class="sxs-lookup"><span data-stu-id="f65d2-128">If the shader invocation is inactive, for example if the pixel has been discarded earlier in its execution, or a pixel/sample instruction does not alter the *dst* memory at all (silently).</span></span>

<span data-ttu-id="f65d2-129">除了 u 的範圍外， \# 不會將任何內容寫入記憶體，除非 u \# 是結構化的，且在結構 (第二個元件) 的結構中的位元組位移會造成超出界限存取權，否則 UAV 的整個內容會變成未定義。</span><span class="sxs-lookup"><span data-stu-id="f65d2-129">Out of bounds addressing on u\# causes nothing to be written to memory, except if the u\# is structured, and byte offset into the struct (second component of the address) is causing the out of bounds access, then the entire contents of the UAV become undefined.</span></span>

<span data-ttu-id="f65d2-130">G (超出範圍的界限 \# \# ，而不是所有的共用記憶體) 會導致所有共用記憶體的整個內容變成未定義。</span><span class="sxs-lookup"><span data-stu-id="f65d2-130">Out of bounds addressing on g\# (the bounds of that particular g\#, as opposed to all shared memory) causes the entire contents of all shared memory to become undefined.</span></span>

<span data-ttu-id="f65d2-131">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="f65d2-131">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="f65d2-132">頂點</span><span class="sxs-lookup"><span data-stu-id="f65d2-132">Vertex</span></span> | <span data-ttu-id="f65d2-133">船體</span><span class="sxs-lookup"><span data-stu-id="f65d2-133">Hull</span></span> | <span data-ttu-id="f65d2-134">網域</span><span class="sxs-lookup"><span data-stu-id="f65d2-134">Domain</span></span> | <span data-ttu-id="f65d2-135">幾何</span><span class="sxs-lookup"><span data-stu-id="f65d2-135">Geometry</span></span> | <span data-ttu-id="f65d2-136">像素</span><span class="sxs-lookup"><span data-stu-id="f65d2-136">Pixel</span></span> | <span data-ttu-id="f65d2-137">計算</span><span class="sxs-lookup"><span data-stu-id="f65d2-137">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="f65d2-138">X</span><span class="sxs-lookup"><span data-stu-id="f65d2-138">X</span></span>     | <span data-ttu-id="f65d2-139">X</span><span class="sxs-lookup"><span data-stu-id="f65d2-139">X</span></span>       |



 

<span data-ttu-id="f65d2-140">由於 UAVs 可在 Direct3D 11.1 的所有著色器階段使用，因此此指示適用于 Direct3D 11.1 執行時間的所有著色器階段，從 Windows 8 開始提供。</span><span class="sxs-lookup"><span data-stu-id="f65d2-140">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="f65d2-141">頂點</span><span class="sxs-lookup"><span data-stu-id="f65d2-141">Vertex</span></span> | <span data-ttu-id="f65d2-142">船體</span><span class="sxs-lookup"><span data-stu-id="f65d2-142">Hull</span></span> | <span data-ttu-id="f65d2-143">網域</span><span class="sxs-lookup"><span data-stu-id="f65d2-143">Domain</span></span> | <span data-ttu-id="f65d2-144">幾何</span><span class="sxs-lookup"><span data-stu-id="f65d2-144">Geometry</span></span> | <span data-ttu-id="f65d2-145">像素</span><span class="sxs-lookup"><span data-stu-id="f65d2-145">Pixel</span></span> | <span data-ttu-id="f65d2-146">計算</span><span class="sxs-lookup"><span data-stu-id="f65d2-146">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="f65d2-147">X</span><span class="sxs-lookup"><span data-stu-id="f65d2-147">X</span></span>      | <span data-ttu-id="f65d2-148">X</span><span class="sxs-lookup"><span data-stu-id="f65d2-148">X</span></span>    | <span data-ttu-id="f65d2-149">X</span><span class="sxs-lookup"><span data-stu-id="f65d2-149">X</span></span>      | <span data-ttu-id="f65d2-150">X</span><span class="sxs-lookup"><span data-stu-id="f65d2-150">X</span></span>        | <span data-ttu-id="f65d2-151">X</span><span class="sxs-lookup"><span data-stu-id="f65d2-151">X</span></span>     | <span data-ttu-id="f65d2-152">X</span><span class="sxs-lookup"><span data-stu-id="f65d2-152">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="f65d2-153">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="f65d2-153">Minimum Shader Model</span></span>

<span data-ttu-id="f65d2-154">下列著色器模型支援此指令：</span><span class="sxs-lookup"><span data-stu-id="f65d2-154">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="f65d2-155">著色器模型</span><span class="sxs-lookup"><span data-stu-id="f65d2-155">Shader Model</span></span>                                              | <span data-ttu-id="f65d2-156">支援</span><span class="sxs-lookup"><span data-stu-id="f65d2-156">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="f65d2-157">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="f65d2-157">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="f65d2-158">是</span><span class="sxs-lookup"><span data-stu-id="f65d2-158">yes</span></span>       |
| [<span data-ttu-id="f65d2-159">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="f65d2-159">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="f65d2-160">不可以</span><span class="sxs-lookup"><span data-stu-id="f65d2-160">no</span></span>        |
| [<span data-ttu-id="f65d2-161">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="f65d2-161">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="f65d2-162">不可以</span><span class="sxs-lookup"><span data-stu-id="f65d2-162">no</span></span>        |
| [<span data-ttu-id="f65d2-163">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="f65d2-163">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="f65d2-164">不可以</span><span class="sxs-lookup"><span data-stu-id="f65d2-164">no</span></span>        |
| [<span data-ttu-id="f65d2-165">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="f65d2-165">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="f65d2-166">不可以</span><span class="sxs-lookup"><span data-stu-id="f65d2-166">no</span></span>        |
| [<span data-ttu-id="f65d2-167">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="f65d2-167">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="f65d2-168">不可以</span><span class="sxs-lookup"><span data-stu-id="f65d2-168">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="f65d2-169">相關主題</span><span class="sxs-lookup"><span data-stu-id="f65d2-169">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f65d2-170">著色器模型5元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="f65d2-170">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





