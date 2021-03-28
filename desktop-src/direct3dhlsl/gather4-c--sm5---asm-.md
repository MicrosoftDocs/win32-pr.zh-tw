---
title: 'gather4_c (sm5-asm) '
description: 與 gather4 相同，不同之處在于此 instrution 會在材質上執行比較，類似于範例 \_ c。
ms.assetid: 6265151A-36CE-4D31-B7B2-233CEEBDCF87
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35414aa2cd4d9f0686ab7a5cc17b94caa960cec1
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104990791"
---
# <a name="gather4_c-sm5---asm"></a><span data-ttu-id="f8b77-103">gather4 \_ c (sm5-asm) </span><span class="sxs-lookup"><span data-stu-id="f8b77-103">gather4\_c (sm5 - asm)</span></span>

<span data-ttu-id="f8b77-104">與 [**gather4**](gather4--sm5---asm-.md)相同，不同之處在于此 instrution 會在材質上執行比較，類似于 [**範例 \_ c**](sample-c--sm4---asm-.md)。</span><span class="sxs-lookup"><span data-stu-id="f8b77-104">Same as [**gather4**](gather4--sm5---asm-.md), except this instrution performs comparison on texels, similar to [**sample\_c**](sample-c--sm4---asm-.md).</span></span>



| <span data-ttu-id="f8b77-105">gather4 \_ c \[ \_ aoffimmi (u、v) \] dest \[ \] 、srcAddress \[ . swizzle \] 、srcResource. swizzle \[ \] 、srcSampler \[ 。R \] 、srcReferenceValue</span><span class="sxs-lookup"><span data-stu-id="f8b77-105">gather4\_c\[\_aoffimmi(u,v)\] dest\[.mask\], srcAddress\[.swizzle\], srcResource\[.swizzle\], srcSampler\[.R\], srcReferenceValue</span></span> |
|-----------------------------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="f8b77-106">項目</span><span class="sxs-lookup"><span data-stu-id="f8b77-106">Item</span></span>                                                                                                                                       | <span data-ttu-id="f8b77-107">描述</span><span class="sxs-lookup"><span data-stu-id="f8b77-107">Description</span></span>                                                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8b77-108"><span id="dest"></span><span id="DEST"></span>*目標*</span><span class="sxs-lookup"><span data-stu-id="f8b77-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                                            | <span data-ttu-id="f8b77-109">\[在 \] 操作結果的位址中</span><span class="sxs-lookup"><span data-stu-id="f8b77-109">\[in\] The address of the result of the operation</span></span><br/>                                    |
| <span data-ttu-id="f8b77-110"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span><span class="sxs-lookup"><span data-stu-id="f8b77-110"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span></span><br/>                             | <span data-ttu-id="f8b77-111">\[在 \] 一組材質座標中。</span><span class="sxs-lookup"><span data-stu-id="f8b77-111">\[in\] A set of texture coordinates.</span></span><br/>                                                 |
| <span data-ttu-id="f8b77-112"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span><span class="sxs-lookup"><span data-stu-id="f8b77-112"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/>                         | <span data-ttu-id="f8b77-113">\[在材質暫存器中 \] 。</span><span class="sxs-lookup"><span data-stu-id="f8b77-113">\[in\] A texture register.</span></span><br/>                                                           |
| <span data-ttu-id="f8b77-114"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span><span class="sxs-lookup"><span data-stu-id="f8b77-114"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span></span><br/>                             | <span data-ttu-id="f8b77-115">\[在 \] 取樣器註冊中。</span><span class="sxs-lookup"><span data-stu-id="f8b77-115">\[in\] A sampler register.</span></span><br/>                                                           |
| <span data-ttu-id="f8b77-116"><span id="srcReferenceValue"></span><span id="srcreferencevalue"></span><span id="SRCREFERENCEVALUE"></span>*srcReferenceValue*</span><span class="sxs-lookup"><span data-stu-id="f8b77-116"><span id="srcReferenceValue"></span><span id="srcreferencevalue"></span><span id="SRCREFERENCEVALUE"></span>*srcReferenceValue*</span></span><br/> | <span data-ttu-id="f8b77-117">\[在 \] 已選取單一元件的註冊中，用於比較。</span><span class="sxs-lookup"><span data-stu-id="f8b77-117">\[in\] A register with a single component selected, which is used in the comparison.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f8b77-118">備註</span><span class="sxs-lookup"><span data-stu-id="f8b77-118">Remarks</span></span>

<span data-ttu-id="f8b77-119">如需有關 *srcReferenceValue* 如何與每個提取的材質進行比較的說明，請參閱 [**範例 \_ c**](sample-c--sm4---asm-.md) 。</span><span class="sxs-lookup"><span data-stu-id="f8b77-119">See [**sample\_c**](sample-c--sm4---asm-.md) for a description of how *srcReferenceValue* gets compared against each fetched texel.</span></span> <span data-ttu-id="f8b77-120">不同于 **範例 \_ c**， **gather4 \_ c** 會傳回每個比較結果，而不是篩選它們。</span><span class="sxs-lookup"><span data-stu-id="f8b77-120">Unlike **sample\_c**, **gather4\_c** returns each comparison result, rather than filtering them.</span></span>

<span data-ttu-id="f8b77-121">若為 TextureCube 角落，其中有三個真正的材質，而第四個必須合成，則必須在比較步驟之後進行合成。</span><span class="sxs-lookup"><span data-stu-id="f8b77-121">For TextureCube corners, where there are three real texels and a fourth must be synthesized, the synthesis must occur after the comparison step.</span></span> <span data-ttu-id="f8b77-122">這表示 syntesized 材質傳回的比較結果可以是0、0.33、0.66 或1。</span><span class="sxs-lookup"><span data-stu-id="f8b77-122">This means the returned comparison result for the syntesized texel can be 0, 0.33 , 0.66 , or 1.</span></span> <span data-ttu-id="f8b77-123">某些實作為合成材質可能只會傳回0或1。</span><span class="sxs-lookup"><span data-stu-id="f8b77-123">Some implementations may only return either 0 or 1 for the synthesized texel.</span></span> <span data-ttu-id="f8b77-124">除了這份可能的結果清單之外，未指定合成材質的方法。</span><span class="sxs-lookup"><span data-stu-id="f8b77-124">Aside from this listing of possible results, the method for synthesizing the texel is unspecified.</span></span>

<span data-ttu-id="f8b77-125">針對具有 float32 元件的格式，如果要提取的值是正規化的或 +-INF，比較作業就會使用此值。</span><span class="sxs-lookup"><span data-stu-id="f8b77-125">For formats with float32 components, if the value being fetched is normalized, or +-INF, it is used in the comparison operation untouched.</span></span> <span data-ttu-id="f8b77-126">在比較作業中使用 NaN 做為 NaN，但 NaN 的精確位標記法可能會變更。</span><span class="sxs-lookup"><span data-stu-id="f8b77-126">NaN is used in the comparison operation as NaN, but the exact bit representation of the NaN may be changed.</span></span> <span data-ttu-id="f8b77-127">Denorms 會排清到零進行比較。</span><span class="sxs-lookup"><span data-stu-id="f8b77-127">Denorms are flushed to zero going into the comparison.</span></span> <span data-ttu-id="f8b77-128">針對 TextureCubes，遺漏的第四個材質的部分合成必須在角落進行，因此未變更合成材質的未變更的概念。</span><span class="sxs-lookup"><span data-stu-id="f8b77-128">For TextureCubes, some synthesis of the missing 4th texel must occur at corners, so the notion of returning bits unchanged for the synthesized texel does not apply.</span></span>

<span data-ttu-id="f8b77-129">*Gather4 \_ c* 支援的格式與 *範例 \_ c* 所支援的格式相同。</span><span class="sxs-lookup"><span data-stu-id="f8b77-129">Formats supported for *gather4\_c* are same as those supported for *sample\_c*.</span></span> <span data-ttu-id="f8b77-130">這些都是單一元件格式，因此。 *SrcSampler* 上的 R，而非任意 swizzle。</span><span class="sxs-lookup"><span data-stu-id="f8b77-130">These are single-component formats, thus the .R on *srcSampler*, rather than an arbitrary swizzle.</span></span> <span data-ttu-id="f8b77-131">未系結資源上的 **gather4 \_ c** 會傳回0。</span><span class="sxs-lookup"><span data-stu-id="f8b77-131">**gather4\_c** on an unbound resource returns 0.</span></span>

<span data-ttu-id="f8b77-132">使用此指示進行自訂陰影對應篩選。</span><span class="sxs-lookup"><span data-stu-id="f8b77-132">Use this instruction for custom shadow map filtering.</span></span>

<span data-ttu-id="f8b77-133">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="f8b77-133">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="f8b77-134">頂點</span><span class="sxs-lookup"><span data-stu-id="f8b77-134">Vertex</span></span> | <span data-ttu-id="f8b77-135">船體</span><span class="sxs-lookup"><span data-stu-id="f8b77-135">Hull</span></span> | <span data-ttu-id="f8b77-136">網域</span><span class="sxs-lookup"><span data-stu-id="f8b77-136">Domain</span></span> | <span data-ttu-id="f8b77-137">幾何</span><span class="sxs-lookup"><span data-stu-id="f8b77-137">Geometry</span></span> | <span data-ttu-id="f8b77-138">像素</span><span class="sxs-lookup"><span data-stu-id="f8b77-138">Pixel</span></span> | <span data-ttu-id="f8b77-139">計算</span><span class="sxs-lookup"><span data-stu-id="f8b77-139">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="f8b77-140">X</span><span class="sxs-lookup"><span data-stu-id="f8b77-140">X</span></span>      | <span data-ttu-id="f8b77-141">X</span><span class="sxs-lookup"><span data-stu-id="f8b77-141">X</span></span>    | <span data-ttu-id="f8b77-142">X</span><span class="sxs-lookup"><span data-stu-id="f8b77-142">X</span></span>      | <span data-ttu-id="f8b77-143">X</span><span class="sxs-lookup"><span data-stu-id="f8b77-143">X</span></span>        | <span data-ttu-id="f8b77-144">X</span><span class="sxs-lookup"><span data-stu-id="f8b77-144">X</span></span>     | <span data-ttu-id="f8b77-145">X</span><span class="sxs-lookup"><span data-stu-id="f8b77-145">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="f8b77-146">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="f8b77-146">Minimum Shader Model</span></span>

<span data-ttu-id="f8b77-147">下列著色器模型支援此指令：</span><span class="sxs-lookup"><span data-stu-id="f8b77-147">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="f8b77-148">著色器模型</span><span class="sxs-lookup"><span data-stu-id="f8b77-148">Shader Model</span></span>                                              | <span data-ttu-id="f8b77-149">支援</span><span class="sxs-lookup"><span data-stu-id="f8b77-149">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="f8b77-150">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="f8b77-150">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="f8b77-151">是</span><span class="sxs-lookup"><span data-stu-id="f8b77-151">yes</span></span>       |
| [<span data-ttu-id="f8b77-152">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="f8b77-152">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="f8b77-153">不可以</span><span class="sxs-lookup"><span data-stu-id="f8b77-153">no</span></span>        |
| [<span data-ttu-id="f8b77-154">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="f8b77-154">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="f8b77-155">不可以</span><span class="sxs-lookup"><span data-stu-id="f8b77-155">no</span></span>        |
| [<span data-ttu-id="f8b77-156">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="f8b77-156">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="f8b77-157">不可以</span><span class="sxs-lookup"><span data-stu-id="f8b77-157">no</span></span>        |
| [<span data-ttu-id="f8b77-158">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="f8b77-158">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="f8b77-159">不可以</span><span class="sxs-lookup"><span data-stu-id="f8b77-159">no</span></span>        |
| [<span data-ttu-id="f8b77-160">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="f8b77-160">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="f8b77-161">不可以</span><span class="sxs-lookup"><span data-stu-id="f8b77-161">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="f8b77-162">相關主題</span><span class="sxs-lookup"><span data-stu-id="f8b77-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f8b77-163">著色器模型5元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="f8b77-163">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





