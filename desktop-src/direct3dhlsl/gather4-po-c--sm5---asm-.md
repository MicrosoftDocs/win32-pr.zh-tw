---
title: 'gather4_po_c (sm5-asm) '
description: 的行為與 gather4 \_ po 相同，但在材質上執行比較，類似于範例 \_ c。
ms.assetid: B128EEF3-3440-4F00-9792-20FB1AE075E9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36b07dcad08b4d117a453a3c97e461e6b9b4cab6
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104373862"
---
# <a name="gather4_po_c-sm5---asm"></a><span data-ttu-id="54e72-103">gather4 \_ po \_ c (sm5-asm) </span><span class="sxs-lookup"><span data-stu-id="54e72-103">gather4\_po\_c (sm5 - asm)</span></span>

<span data-ttu-id="54e72-104">的行為與 [**gather4 \_ po**](gather4-po--sm5---asm-.md)相同，但在材質上執行比較，類似于 [**範例 \_ c**](sample-c--sm4---asm-.md)。</span><span class="sxs-lookup"><span data-stu-id="54e72-104">Behaves the same as [**gather4\_po**](gather4-po--sm5---asm-.md), except performs comparison on texels, similar to [**sample\_c**](sample-c--sm4---asm-.md).</span></span>



| <span data-ttu-id="54e72-105">gather4 \_ po \_ c dest \[ . mask \] 、srcAddress \[ . swizzle \] 、srcOffset \[ . swizzle \] 、srcResource \[ . swizzle \] 、srcSampler \[ 。R \] 、srcReferenceValue</span><span class="sxs-lookup"><span data-stu-id="54e72-105">gather4\_po\_c dest\[.mask\], srcAddress\[.swizzle\], srcOffset\[.swizzle\], srcResource\[.swizzle\], srcSampler\[.R\], srcReferenceValue</span></span> |
|-------------------------------------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="54e72-106">項目</span><span class="sxs-lookup"><span data-stu-id="54e72-106">Item</span></span>                                                                                                                                       | <span data-ttu-id="54e72-107">描述</span><span class="sxs-lookup"><span data-stu-id="54e72-107">Description</span></span>                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="54e72-108"><span id="dest"></span><span id="DEST"></span>*目標*</span><span class="sxs-lookup"><span data-stu-id="54e72-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                                            | <span data-ttu-id="54e72-109">\[在 \] 操作結果的位址中。</span><span class="sxs-lookup"><span data-stu-id="54e72-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="54e72-110"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span><span class="sxs-lookup"><span data-stu-id="54e72-110"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span></span><br/>                             | <span data-ttu-id="54e72-111">\[在 \] 一組材質座標中。</span><span class="sxs-lookup"><span data-stu-id="54e72-111">\[in\] A set of texture coordinates.</span></span><br/>               |
| <span data-ttu-id="54e72-112"><span id="srcOffset"></span><span id="srcoffset"></span><span id="SRCOFFSET"></span>*srcOffset*</span><span class="sxs-lookup"><span data-stu-id="54e72-112"><span id="srcOffset"></span><span id="srcoffset"></span><span id="SRCOFFSET"></span>*srcOffset*</span></span><br/>                                 | <span data-ttu-id="54e72-113">\[在 \] 位移中。</span><span class="sxs-lookup"><span data-stu-id="54e72-113">\[in\] The offset.</span></span><br/>                                 |
| <span data-ttu-id="54e72-114"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span><span class="sxs-lookup"><span data-stu-id="54e72-114"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/>                         | <span data-ttu-id="54e72-115">\[在材質暫存器中 \] 。</span><span class="sxs-lookup"><span data-stu-id="54e72-115">\[in\] A texture register.</span></span><br/>                         |
| <span data-ttu-id="54e72-116"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span><span class="sxs-lookup"><span data-stu-id="54e72-116"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span></span><br/>                             | <span data-ttu-id="54e72-117">\[在 \] 取樣器註冊中。</span><span class="sxs-lookup"><span data-stu-id="54e72-117">\[in\] A sampler register.</span></span><br/>                         |
| <span data-ttu-id="54e72-118"><span id="srcReferenceValue"></span><span id="srcreferencevalue"></span><span id="SRCREFERENCEVALUE"></span>*srcReferenceValue*</span><span class="sxs-lookup"><span data-stu-id="54e72-118"><span id="srcReferenceValue"></span><span id="srcreferencevalue"></span><span id="SRCREFERENCEVALUE"></span>*srcReferenceValue*</span></span><br/> | <span data-ttu-id="54e72-119">\[在 \] 選取的單一元件中。</span><span class="sxs-lookup"><span data-stu-id="54e72-119">\[in\] Single component selected.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="54e72-120">備註</span><span class="sxs-lookup"><span data-stu-id="54e72-120">Remarks</span></span>

<span data-ttu-id="54e72-121">如需有關如何將 *srcReferenceValue* 與每個提取的材質進行比較的詳細資訊，請參閱 [**範例 \_ c**](sample-c--sm4---asm-.md) 。</span><span class="sxs-lookup"><span data-stu-id="54e72-121">See [**sample\_c**](sample-c--sm4---asm-.md) for information about how *srcReferenceValue* is compared against each fetched texel.</span></span> <span data-ttu-id="54e72-122">不同于 **範例 \_ c**， *gather4 \_ po \_ c* 會傳回每個比較結果，而不是篩選結果。</span><span class="sxs-lookup"><span data-stu-id="54e72-122">Unlike **sample\_c**, *gather4\_po\_c* returns each comparison result, rather than filtering them.</span></span>

<span data-ttu-id="54e72-123">此指令（例如 **gather4 \_ po**）僅適用于2d 材質。</span><span class="sxs-lookup"><span data-stu-id="54e72-123">This instruction, like **gather4\_po**, only works with 2D textures.</span></span> <span data-ttu-id="54e72-124">這與 [**gather4 \_ c**](gather4-c--sm5---asm-.md)不同，它也可以搭配 TextureCubes 使用。</span><span class="sxs-lookup"><span data-stu-id="54e72-124">This is unlike [**gather4\_c**](gather4-c--sm5---asm-.md), which also works with TextureCubes.</span></span>

<span data-ttu-id="54e72-125">針對具有 float32 元件的格式，如果要提取的值是正規化的或 +-INF，比較作業就會使用此值。</span><span class="sxs-lookup"><span data-stu-id="54e72-125">For formats with float32 components, if the value being fetched is normalized, or +-INF, it is used in the comparison operation untouched.</span></span> <span data-ttu-id="54e72-126">在比較作業中使用 NaN 做為 NaN，但 NaN 的精確位標記法可能會變更。</span><span class="sxs-lookup"><span data-stu-id="54e72-126">NaN is used in the comparison operation as NaN, but the exact bit representation of the NaN may be changed.</span></span> <span data-ttu-id="54e72-127">Denorms 會排清到零進行比較。</span><span class="sxs-lookup"><span data-stu-id="54e72-127">Denorms are flushed to zero going into the comparison.</span></span> <span data-ttu-id="54e72-128">針對 TextureCubes，遺漏的第四個材質的部分合成必須在角落進行，因此未變更合成材質的未變更的概念。</span><span class="sxs-lookup"><span data-stu-id="54e72-128">For TextureCubes, some synthesis of the missing 4th texel must occur at corners, so the notion of returning bits unchanged for the synthesized texel does not apply.</span></span>

<span data-ttu-id="54e72-129">支援的 **gather4 \_ po \_ c** 格式與 **範例 \_ c** 所支援的格式相同。</span><span class="sxs-lookup"><span data-stu-id="54e72-129">Formats supported for **gather4\_po\_c** are same as those supported for **sample\_c**.</span></span> <span data-ttu-id="54e72-130">這些都是單一元件格式，因此。SrcSampler 上的 R，而非任意 swizzle。</span><span class="sxs-lookup"><span data-stu-id="54e72-130">These are single-component formats, thus the .R on srcSampler, rather than an arbitrary swizzle.</span></span>

<span data-ttu-id="54e72-131">未系結資源上的 **gather4 \_ po \_ c** 會傳回0。</span><span class="sxs-lookup"><span data-stu-id="54e72-131">**gather4\_po\_c** on an unbound resource returns 0.</span></span>

<span data-ttu-id="54e72-132">使用這個方法來進行陰影對應篩選。</span><span class="sxs-lookup"><span data-stu-id="54e72-132">Use this method for shadow map filtering.</span></span>

<span data-ttu-id="54e72-133">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="54e72-133">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="54e72-134">頂點</span><span class="sxs-lookup"><span data-stu-id="54e72-134">Vertex</span></span> | <span data-ttu-id="54e72-135">船體</span><span class="sxs-lookup"><span data-stu-id="54e72-135">Hull</span></span> | <span data-ttu-id="54e72-136">網域</span><span class="sxs-lookup"><span data-stu-id="54e72-136">Domain</span></span> | <span data-ttu-id="54e72-137">幾何</span><span class="sxs-lookup"><span data-stu-id="54e72-137">Geometry</span></span> | <span data-ttu-id="54e72-138">像素</span><span class="sxs-lookup"><span data-stu-id="54e72-138">Pixel</span></span> | <span data-ttu-id="54e72-139">計算</span><span class="sxs-lookup"><span data-stu-id="54e72-139">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="54e72-140">X</span><span class="sxs-lookup"><span data-stu-id="54e72-140">X</span></span>      | <span data-ttu-id="54e72-141">X</span><span class="sxs-lookup"><span data-stu-id="54e72-141">X</span></span>    | <span data-ttu-id="54e72-142">X</span><span class="sxs-lookup"><span data-stu-id="54e72-142">X</span></span>      | <span data-ttu-id="54e72-143">X</span><span class="sxs-lookup"><span data-stu-id="54e72-143">X</span></span>        | <span data-ttu-id="54e72-144">X</span><span class="sxs-lookup"><span data-stu-id="54e72-144">X</span></span>     | <span data-ttu-id="54e72-145">X</span><span class="sxs-lookup"><span data-stu-id="54e72-145">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="54e72-146">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="54e72-146">Minimum Shader Model</span></span>

<span data-ttu-id="54e72-147">下列著色器模型支援此指令：</span><span class="sxs-lookup"><span data-stu-id="54e72-147">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="54e72-148">著色器模型</span><span class="sxs-lookup"><span data-stu-id="54e72-148">Shader Model</span></span>                                              | <span data-ttu-id="54e72-149">支援</span><span class="sxs-lookup"><span data-stu-id="54e72-149">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="54e72-150">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="54e72-150">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="54e72-151">是</span><span class="sxs-lookup"><span data-stu-id="54e72-151">yes</span></span>       |
| [<span data-ttu-id="54e72-152">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="54e72-152">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="54e72-153">不可以</span><span class="sxs-lookup"><span data-stu-id="54e72-153">no</span></span>        |
| [<span data-ttu-id="54e72-154">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="54e72-154">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="54e72-155">不可以</span><span class="sxs-lookup"><span data-stu-id="54e72-155">no</span></span>        |
| [<span data-ttu-id="54e72-156">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="54e72-156">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="54e72-157">不可以</span><span class="sxs-lookup"><span data-stu-id="54e72-157">no</span></span>        |
| [<span data-ttu-id="54e72-158">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="54e72-158">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="54e72-159">不可以</span><span class="sxs-lookup"><span data-stu-id="54e72-159">no</span></span>        |
| [<span data-ttu-id="54e72-160">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="54e72-160">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="54e72-161">不可以</span><span class="sxs-lookup"><span data-stu-id="54e72-161">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="54e72-162">相關主題</span><span class="sxs-lookup"><span data-stu-id="54e72-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="54e72-163">著色器模型5元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="54e72-163">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





