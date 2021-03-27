---
title: 'atomic_or (sm5-asm) '
description: 不可部分完成的位 OR 至記憶體。
ms.assetid: 5AFB96AA-267B-454E-9526-BA61A876ED42
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 245f1b02edd74712471206b095f0c8a9040962b6
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104507724"
---
# <a name="atomic_or-sm5---asm"></a><span data-ttu-id="0f3ec-103">不可部分完成 \_ 或 (sm5-asm) </span><span class="sxs-lookup"><span data-stu-id="0f3ec-103">atomic\_or (sm5 - asm)</span></span>

<span data-ttu-id="0f3ec-104">不可部分完成的位 OR 至記憶體。</span><span class="sxs-lookup"><span data-stu-id="0f3ec-104">Atomic bitwise OR to memory.</span></span>



| <span data-ttu-id="0f3ec-105">不可 \_ 部分完成或 dst、dstAddress \[ . swizzle \] 、src0 \[ . 選取 \_ 元件\]</span><span class="sxs-lookup"><span data-stu-id="0f3ec-105">atomic\_or dst, dstAddress\[.swizzle\], src0\[.select\_component\]</span></span> |
|--------------------------------------------------------------------|



 



| <span data-ttu-id="0f3ec-106">項目</span><span class="sxs-lookup"><span data-stu-id="0f3ec-106">Item</span></span>                                                                                                           | <span data-ttu-id="0f3ec-107">描述</span><span class="sxs-lookup"><span data-stu-id="0f3ec-107">Description</span></span>                                                                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f3ec-108"><span id="dst"></span><span id="DST"></span>*Dst*</span><span class="sxs-lookup"><span data-stu-id="0f3ec-108"><span id="dst"></span><span id="DST"></span>*dst*</span></span><br/>                                                   | <span data-ttu-id="0f3ec-109">\[在 \] *src0* 的元件中。</span><span class="sxs-lookup"><span data-stu-id="0f3ec-109">\[in\] The components to OR with *src0*.</span></span> <span data-ttu-id="0f3ec-110">此值必須是未排序的存取視圖 (UAV)  (u \#) 。</span><span class="sxs-lookup"><span data-stu-id="0f3ec-110">This value must be an unordered access view (UAV) (u\#).</span></span> <span data-ttu-id="0f3ec-111">在計算著色器中，它也可以是執行緒群組的共用記憶體 (g \#) 。</span><span class="sxs-lookup"><span data-stu-id="0f3ec-111">In the compute shader it can also be thread group shared memory (g\#).</span></span> <br/> |
| <span data-ttu-id="0f3ec-112"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*</span><span class="sxs-lookup"><span data-stu-id="0f3ec-112"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*</span></span><br/> | <span data-ttu-id="0f3ec-113">\[在 \] 記憶體位址中。</span><span class="sxs-lookup"><span data-stu-id="0f3ec-113">\[in\] The memory address.</span></span><br/>                                                                                                                                                |
| <span data-ttu-id="0f3ec-114"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="0f3ec-114"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                                | <span data-ttu-id="0f3ec-115">\[在與 \] *dst* 的元件中。</span><span class="sxs-lookup"><span data-stu-id="0f3ec-115">\[in\] The components to OR with *dst*.</span></span><br/>                                                                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="0f3ec-116">備註</span><span class="sxs-lookup"><span data-stu-id="0f3ec-116">Remarks</span></span>

<span data-ttu-id="0f3ec-117">此指令會32在每個元件位址 DstAddress 的每個元件位址的 dst 中，執行單一元件32位或運算元 *src0* 至 *dst* ，以不可部分完成的方式執行。</span><span class="sxs-lookup"><span data-stu-id="0f3ec-117">This instruction performs a single component 32-bit bitwise OR of operand *src0* into *dst* at 32-bit per component address *dstAddress*, performed atomically.</span></span>

<span data-ttu-id="0f3ec-118">從位址取得的元件數目取決於 *dst* u \# 或 g 的維度 \# 。</span><span class="sxs-lookup"><span data-stu-id="0f3ec-118">The number of components taken from the address is determined by the dimensionality of *dst* u\# or g\#.</span></span>

<span data-ttu-id="0f3ec-119">如果 *dst* 是 u \# ，則可以宣告為 raw、具類型或結構化。</span><span class="sxs-lookup"><span data-stu-id="0f3ec-119">If *dst* is a u\#, it can be declared as raw, typed or structured.</span></span> <span data-ttu-id="0f3ec-120">如果具型別，則必須使用 R32 uint/聖的系結資源格式宣告為 UINT/聖 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="0f3ec-120">If typed, it must be declared as UINT/SINT with the bound resource format being R32\_UINT/\_SINT.</span></span>

<span data-ttu-id="0f3ec-121">如果 *dst* 為 g \# ，則必須將它宣告為 raw 或結構化。</span><span class="sxs-lookup"><span data-stu-id="0f3ec-121">If *dst* is g\#, it must be declared as raw or structured.</span></span>

<span data-ttu-id="0f3ec-122">沒有任何專案會傳回給著色器。</span><span class="sxs-lookup"><span data-stu-id="0f3ec-122">Nothing is returned to the shader.</span></span>

<span data-ttu-id="0f3ec-123">如果著色器調用處于非使用中狀態，例如，如果圖元在先前的執行中已被捨棄，或圖元/樣本調用僅存在做為衍生的真實圖元/樣本的協助程式，則此指令不會在所有 (無訊息的情況下變更 *dst* 記憶體) 。</span><span class="sxs-lookup"><span data-stu-id="0f3ec-123">If the shader invocation is inactive, for example if the pixel has been discarded earlier in its execution, or if a pixel/sample invocation only exists to serve as a helper to a real pixel/sample for derivatives, this instruction does not alter the *dst* memory at all (silently).</span></span>

<span data-ttu-id="0f3ec-124">除了 u 的範圍外， \# 不會將任何內容寫入記憶體中，但如果 u \# 是結構化的，且位址) 的結構 (第二個元件的位元組位移造成超出界限存取權，則 UAV 的整個內容都會變成未定義。</span><span class="sxs-lookup"><span data-stu-id="0f3ec-124">Out of bounds addressing on u\# causes nothing to be written to memory, except if the u\# is structured, and the byte offset into the struct (second component of the address) is causing the out of bounds access, then the entire contents of the UAV become undefined.</span></span>

<span data-ttu-id="0f3ec-125">G (超出範圍的界限 \# \# ，而不是所有的共用記憶體) 會導致所有共用記憶體的整個內容變成未定義。</span><span class="sxs-lookup"><span data-stu-id="0f3ec-125">Out of bounds addressing on g\# (the bounds of that particular g\#, as opposed to all shared memory) causes the entire contents of all shared memory to become undefined.</span></span>

<span data-ttu-id="0f3ec-126">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="0f3ec-126">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="0f3ec-127">頂點</span><span class="sxs-lookup"><span data-stu-id="0f3ec-127">Vertex</span></span> | <span data-ttu-id="0f3ec-128">船體</span><span class="sxs-lookup"><span data-stu-id="0f3ec-128">Hull</span></span> | <span data-ttu-id="0f3ec-129">網域</span><span class="sxs-lookup"><span data-stu-id="0f3ec-129">Domain</span></span> | <span data-ttu-id="0f3ec-130">幾何</span><span class="sxs-lookup"><span data-stu-id="0f3ec-130">Geometry</span></span> | <span data-ttu-id="0f3ec-131">像素</span><span class="sxs-lookup"><span data-stu-id="0f3ec-131">Pixel</span></span> | <span data-ttu-id="0f3ec-132">計算</span><span class="sxs-lookup"><span data-stu-id="0f3ec-132">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="0f3ec-133">X</span><span class="sxs-lookup"><span data-stu-id="0f3ec-133">X</span></span>     | <span data-ttu-id="0f3ec-134">X</span><span class="sxs-lookup"><span data-stu-id="0f3ec-134">X</span></span>       |



 

<span data-ttu-id="0f3ec-135">由於 UAVs 可在 Direct3D 11.1 的所有著色器階段使用，因此此指示適用于 Direct3D 11.1 執行時間的所有著色器階段，從 Windows 8 開始提供。</span><span class="sxs-lookup"><span data-stu-id="0f3ec-135">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="0f3ec-136">頂點</span><span class="sxs-lookup"><span data-stu-id="0f3ec-136">Vertex</span></span> | <span data-ttu-id="0f3ec-137">船體</span><span class="sxs-lookup"><span data-stu-id="0f3ec-137">Hull</span></span> | <span data-ttu-id="0f3ec-138">網域</span><span class="sxs-lookup"><span data-stu-id="0f3ec-138">Domain</span></span> | <span data-ttu-id="0f3ec-139">幾何</span><span class="sxs-lookup"><span data-stu-id="0f3ec-139">Geometry</span></span> | <span data-ttu-id="0f3ec-140">像素</span><span class="sxs-lookup"><span data-stu-id="0f3ec-140">Pixel</span></span> | <span data-ttu-id="0f3ec-141">計算</span><span class="sxs-lookup"><span data-stu-id="0f3ec-141">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="0f3ec-142">X</span><span class="sxs-lookup"><span data-stu-id="0f3ec-142">X</span></span>      | <span data-ttu-id="0f3ec-143">X</span><span class="sxs-lookup"><span data-stu-id="0f3ec-143">X</span></span>    | <span data-ttu-id="0f3ec-144">X</span><span class="sxs-lookup"><span data-stu-id="0f3ec-144">X</span></span>      | <span data-ttu-id="0f3ec-145">X</span><span class="sxs-lookup"><span data-stu-id="0f3ec-145">X</span></span>        | <span data-ttu-id="0f3ec-146">X</span><span class="sxs-lookup"><span data-stu-id="0f3ec-146">X</span></span>     | <span data-ttu-id="0f3ec-147">X</span><span class="sxs-lookup"><span data-stu-id="0f3ec-147">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="0f3ec-148">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="0f3ec-148">Minimum Shader Model</span></span>

<span data-ttu-id="0f3ec-149">下列著色器模型支援此指令：</span><span class="sxs-lookup"><span data-stu-id="0f3ec-149">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="0f3ec-150">著色器模型</span><span class="sxs-lookup"><span data-stu-id="0f3ec-150">Shader Model</span></span>                                              | <span data-ttu-id="0f3ec-151">支援</span><span class="sxs-lookup"><span data-stu-id="0f3ec-151">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="0f3ec-152">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="0f3ec-152">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="0f3ec-153">是</span><span class="sxs-lookup"><span data-stu-id="0f3ec-153">yes</span></span>       |
| [<span data-ttu-id="0f3ec-154">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="0f3ec-154">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="0f3ec-155">不可以</span><span class="sxs-lookup"><span data-stu-id="0f3ec-155">no</span></span>        |
| [<span data-ttu-id="0f3ec-156">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="0f3ec-156">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="0f3ec-157">不可以</span><span class="sxs-lookup"><span data-stu-id="0f3ec-157">no</span></span>        |
| [<span data-ttu-id="0f3ec-158">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="0f3ec-158">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="0f3ec-159">不可以</span><span class="sxs-lookup"><span data-stu-id="0f3ec-159">no</span></span>        |
| [<span data-ttu-id="0f3ec-160">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="0f3ec-160">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="0f3ec-161">不可以</span><span class="sxs-lookup"><span data-stu-id="0f3ec-161">no</span></span>        |
| [<span data-ttu-id="0f3ec-162">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="0f3ec-162">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="0f3ec-163">不可以</span><span class="sxs-lookup"><span data-stu-id="0f3ec-163">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="0f3ec-164">相關主題</span><span class="sxs-lookup"><span data-stu-id="0f3ec-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0f3ec-165">著色器模型5元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="0f3ec-165">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





