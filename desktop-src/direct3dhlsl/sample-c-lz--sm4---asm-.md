---
title: 'sample_c_lz (sm4-asm) '
description: 執行比較篩選。 此指令的行為類似範例 \_ c，但」 lod 為0，而衍生項則會被忽略。
ms.assetid: 5F11F091-AF2F-4293-88C7-824F11FE01E4
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24ec2889dd3ea4c86af51c8e36bf2e302c6ad4dd
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104373779"
---
# <a name="sample_c_lz-sm4---asm"></a><span data-ttu-id="1ef65-104">範例 \_ c \_ lz (sm4-asm) </span><span class="sxs-lookup"><span data-stu-id="1ef65-104">sample\_c\_lz (sm4 - asm)</span></span>

<span data-ttu-id="1ef65-105">執行比較篩選。</span><span class="sxs-lookup"><span data-stu-id="1ef65-105">Performs a comparison filter.</span></span> <span data-ttu-id="1ef65-106">此指令的行為類似 [範例 \_ c](sample-c--sm4---asm-.md)，但」 lod 為0，而衍生項則會被忽略。</span><span class="sxs-lookup"><span data-stu-id="1ef65-106">This instruction behaves like [sample\_c](sample-c--sm4---asm-.md), except LOD is 0, and derivatives are ignored.</span></span>



| <span data-ttu-id="1ef65-107">範例 \_ c \_ lz \[ \_ aoffimmi (u、v、w) \] dest \[ \] 、srcAddress \[ . swizzle \] 、srcResource. r、//必須是. r swizzle srcSampler、srcReferenceValue//選取單一元件</span><span class="sxs-lookup"><span data-stu-id="1ef65-107">sample\_c\_lz\[\_aoffimmi(u,v,w)\] dest\[.mask\], srcAddress\[.swizzle\], srcResource.r, // must be .r swizzle srcSampler, srcReferenceValue // single component selected</span></span> |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="1ef65-108">項目</span><span class="sxs-lookup"><span data-stu-id="1ef65-108">Item</span></span>                                                                                                                                       | <span data-ttu-id="1ef65-109">描述</span><span class="sxs-lookup"><span data-stu-id="1ef65-109">Description</span></span>                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ef65-110"><span id="dest"></span><span id="DEST"></span>*目標*</span><span class="sxs-lookup"><span data-stu-id="1ef65-110"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                                            | <span data-ttu-id="1ef65-111">\[在 \] 操作結果的位址中。</span><span class="sxs-lookup"><span data-stu-id="1ef65-111">\[in\] The address of the results of the operation.</span></span><br/>                                                             |
| <span data-ttu-id="1ef65-112"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span><span class="sxs-lookup"><span data-stu-id="1ef65-112"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span></span><br/>                             | <span data-ttu-id="1ef65-113">\[在 \] 一組材質座標中。</span><span class="sxs-lookup"><span data-stu-id="1ef65-113">\[in\] A set of texture coordinates.</span></span> <span data-ttu-id="1ef65-114">如需詳細資訊，請參閱 [範例](sample--sm4---asm-.md) 指令。</span><span class="sxs-lookup"><span data-stu-id="1ef65-114">For more information see the [sample](sample--sm4---asm-.md) instruction.</span></span><br/> |
| <span data-ttu-id="1ef65-115"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span><span class="sxs-lookup"><span data-stu-id="1ef65-115"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/>                         | <span data-ttu-id="1ef65-116">\[在材質暫存器中 \] 。</span><span class="sxs-lookup"><span data-stu-id="1ef65-116">\[in\] A texture register.</span></span> <span data-ttu-id="1ef65-117">如需詳細資訊，請參閱 **範例** 指令。</span><span class="sxs-lookup"><span data-stu-id="1ef65-117">For more information see the **sample** instruction.</span></span><br/>                                 |
| <span data-ttu-id="1ef65-118"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span><span class="sxs-lookup"><span data-stu-id="1ef65-118"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span></span><br/>                             | <span data-ttu-id="1ef65-119">\[在 \] 取樣器註冊中。</span><span class="sxs-lookup"><span data-stu-id="1ef65-119">\[in\] A sampler register.</span></span> <span data-ttu-id="1ef65-120">如需詳細資訊，請參閱 **範例** 指令。</span><span class="sxs-lookup"><span data-stu-id="1ef65-120">For more information see the **sample** instruction.</span></span><br/>                                 |
| <span data-ttu-id="1ef65-121"><span id="srcReferenceValue"></span><span id="srcreferencevalue"></span><span id="SRCREFERENCEVALUE"></span>*srcReferenceValue*</span><span class="sxs-lookup"><span data-stu-id="1ef65-121"><span id="srcReferenceValue"></span><span id="srcreferencevalue"></span><span id="SRCREFERENCEVALUE"></span>*srcReferenceValue*</span></span><br/> | <span data-ttu-id="1ef65-122">\[在 \] 已選取單一元件的註冊中，用於比較。</span><span class="sxs-lookup"><span data-stu-id="1ef65-122">\[in\] A register with a single component selected, which is used in the comparison.</span></span><br/>                            |



 

## <a name="remarks"></a><span data-ttu-id="1ef65-123">備註</span><span class="sxs-lookup"><span data-stu-id="1ef65-123">Remarks</span></span>

<span data-ttu-id="1ef65-124">"Lz" 代表層級0。</span><span class="sxs-lookup"><span data-stu-id="1ef65-124">The "lz" stands for level-zero.</span></span> <span data-ttu-id="1ef65-125">因為會忽略衍生項，所以在圖元著色器以外的著色器中可使用此指令。</span><span class="sxs-lookup"><span data-stu-id="1ef65-125">Because derivatives are ignored, this instruction is available in shaders other than the Pixel Shader.</span></span>

<span data-ttu-id="1ef65-126">如果此指令搭配 mipmapped 材質使用，則會取樣」 LOD 0，除非取樣器有」 LOD 的夾具，這會將」 LOD 放在其他位置，或如果有」 LOD 偏差，這就是從0開始的偏差。</span><span class="sxs-lookup"><span data-stu-id="1ef65-126">If this instruction is used with a mipmapped texture, LOD 0 gets sampled, unless the sampler has an LOD clamp which places the LOD somewhere else, or if there is an LOD Bias, which would simply bias starting from 0.</span></span> <span data-ttu-id="1ef65-127">因為衍生的會被忽略，所以會以 isotropic 篩選的形式來運作。</span><span class="sxs-lookup"><span data-stu-id="1ef65-127">Because derivatives are ignored, anisotropic filtering behaves as isotropic filtering.</span></span>

<span data-ttu-id="1ef65-128">在圖元著色器中，當材質座標衍生於著色器中時，此指令可在不同的流量控制內使用，與 **範例 \_ c** 不同。</span><span class="sxs-lookup"><span data-stu-id="1ef65-128">In Pixel Shaders, this instruction can be used inside varying flow control when the texture coordinates are derived in the shader, unlike **sample\_c**.</span></span>

<span data-ttu-id="1ef65-129">從未系結任何專案的輸入位置提取，會針對所有元件傳回0。</span><span class="sxs-lookup"><span data-stu-id="1ef65-129">Fetching from an input slot that has nothing bound to it returns 0 for all components.</span></span>

<span data-ttu-id="1ef65-130">此指示適用于所有著色器，而不只是圖元著色器，以保持一致性。</span><span class="sxs-lookup"><span data-stu-id="1ef65-130">This instruction is available in all shaders, not just the Pixel Shader, for consistency.</span></span>



| <span data-ttu-id="1ef65-131">頂點著色器</span><span class="sxs-lookup"><span data-stu-id="1ef65-131">Vertex Shader</span></span> | <span data-ttu-id="1ef65-132">幾何著色器</span><span class="sxs-lookup"><span data-stu-id="1ef65-132">Geometry Shader</span></span> | <span data-ttu-id="1ef65-133">像素著色器</span><span class="sxs-lookup"><span data-stu-id="1ef65-133">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="1ef65-134">X</span><span class="sxs-lookup"><span data-stu-id="1ef65-134">X</span></span>             | <span data-ttu-id="1ef65-135">X</span><span class="sxs-lookup"><span data-stu-id="1ef65-135">X</span></span>               | <span data-ttu-id="1ef65-136">x</span><span class="sxs-lookup"><span data-stu-id="1ef65-136">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="1ef65-137">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="1ef65-137">Minimum Shader Model</span></span>

<span data-ttu-id="1ef65-138">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="1ef65-138">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="1ef65-139">著色器模型</span><span class="sxs-lookup"><span data-stu-id="1ef65-139">Shader Model</span></span>                                              | <span data-ttu-id="1ef65-140">支援</span><span class="sxs-lookup"><span data-stu-id="1ef65-140">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="1ef65-141">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="1ef65-141">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="1ef65-142">是</span><span class="sxs-lookup"><span data-stu-id="1ef65-142">yes</span></span>       |
| [<span data-ttu-id="1ef65-143">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="1ef65-143">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="1ef65-144">是</span><span class="sxs-lookup"><span data-stu-id="1ef65-144">yes</span></span>       |
| [<span data-ttu-id="1ef65-145">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="1ef65-145">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="1ef65-146">是</span><span class="sxs-lookup"><span data-stu-id="1ef65-146">yes</span></span>       |
| [<span data-ttu-id="1ef65-147">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="1ef65-147">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="1ef65-148">不可以</span><span class="sxs-lookup"><span data-stu-id="1ef65-148">no</span></span>        |
| [<span data-ttu-id="1ef65-149">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="1ef65-149">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="1ef65-150">不可以</span><span class="sxs-lookup"><span data-stu-id="1ef65-150">no</span></span>        |
| [<span data-ttu-id="1ef65-151">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="1ef65-151">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="1ef65-152">不可以</span><span class="sxs-lookup"><span data-stu-id="1ef65-152">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="1ef65-153">相關主題</span><span class="sxs-lookup"><span data-stu-id="1ef65-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1ef65-154">著色器模型4元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="1ef65-154">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





