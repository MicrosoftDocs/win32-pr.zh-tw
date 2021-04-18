---
title: 'gather4_po (sm5-asm) '
description: Gather4 的變體，但不支援立即位移--8. 7 \，此位移是指令的參數，而且也有更大範圍的-32.. 31 \。
ms.assetid: A77A32B4-BD4F-46E7-9999-13EAA8A26974
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9197fee97645333d37d589db36c3774852b12229
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104971585"
---
# <a name="gather4_po-sm5---asm"></a><span data-ttu-id="f4d77-103">gather4 \_ po (sm5-asm) </span><span class="sxs-lookup"><span data-stu-id="f4d77-103">gather4\_po (sm5 - asm)</span></span>

<span data-ttu-id="f4d77-104">[Gather4](gather4--sm5---asm-.md)的變體，但不支援立即位移 \[ -8. 7 \] ，此位移會作為指令的參數，也會有較大範圍的 \[ -32.. 31 \] 。</span><span class="sxs-lookup"><span data-stu-id="f4d77-104">A variant of [gather4](gather4--sm5---asm-.md), but instead of supporting an immediate offset \[-8..7\], the offset comes as a parameter to the instruction, and also has larger range of \[-32..31\].</span></span>



| <span data-ttu-id="f4d77-105">gather4 \_ po dest \[ . mask \] ，srcAddress \[ . swizzle \] ，srcOffset \[ . swizzle \] ，srcResource \[ ，swizzle \] ，srcSampler \[ . select \_ component\]</span><span class="sxs-lookup"><span data-stu-id="f4d77-105">gather4\_po dest\[.mask\], srcAddress\[.swizzle\], srcOffset\[.swizzle\], srcResource\[.swizzle\], srcSampler\[.select\_component\]</span></span> |
|-------------------------------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="f4d77-106">項目</span><span class="sxs-lookup"><span data-stu-id="f4d77-106">Item</span></span>                                                                                                               | <span data-ttu-id="f4d77-107">描述</span><span class="sxs-lookup"><span data-stu-id="f4d77-107">Description</span></span>                                                   |
|--------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="f4d77-108"><span id="dest"></span><span id="DEST"></span>*目標*</span><span class="sxs-lookup"><span data-stu-id="f4d77-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                    | <span data-ttu-id="f4d77-109">\[在 \] 操作結果的位址中。</span><span class="sxs-lookup"><span data-stu-id="f4d77-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="f4d77-110"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span><span class="sxs-lookup"><span data-stu-id="f4d77-110"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span></span><br/>     | <span data-ttu-id="f4d77-111">\[在 \] 一組材質座標中。</span><span class="sxs-lookup"><span data-stu-id="f4d77-111">\[in\] A set of texture coordinates.</span></span><br/>               |
| <span data-ttu-id="f4d77-112"><span id="srcOffset"></span><span id="srcoffset"></span><span id="SRCOFFSET"></span>*srcOffset*</span><span class="sxs-lookup"><span data-stu-id="f4d77-112"><span id="srcOffset"></span><span id="srcoffset"></span><span id="SRCOFFSET"></span>*srcOffset*</span></span><br/>         | <span data-ttu-id="f4d77-113">\[在 \] 位移中。</span><span class="sxs-lookup"><span data-stu-id="f4d77-113">\[in\] The offset.</span></span><br/>                                 |
| <span data-ttu-id="f4d77-114"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span><span class="sxs-lookup"><span data-stu-id="f4d77-114"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/> | <span data-ttu-id="f4d77-115">\[在材質暫存器中 \] 。</span><span class="sxs-lookup"><span data-stu-id="f4d77-115">\[in\] A texture register.</span></span><br/>                         |
| <span data-ttu-id="f4d77-116"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span><span class="sxs-lookup"><span data-stu-id="f4d77-116"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span></span><br/>     | <span data-ttu-id="f4d77-117">\[在 \] 取樣器註冊中。</span><span class="sxs-lookup"><span data-stu-id="f4d77-117">\[in\] A sampler register.</span></span><br/>                         |



 

## <a name="remarks"></a><span data-ttu-id="f4d77-118">備註</span><span class="sxs-lookup"><span data-stu-id="f4d77-118">Remarks</span></span>

<span data-ttu-id="f4d77-119">4向量 offset 參數的前兩個元件提供32位整數位移。</span><span class="sxs-lookup"><span data-stu-id="f4d77-119">The first two components of the 4-vector offset parameter supply 32-bit integer offsets.</span></span> <span data-ttu-id="f4d77-120">系統會忽略此參數的其他元件。</span><span class="sxs-lookup"><span data-stu-id="f4d77-120">The other components of this parameter are ignored.</span></span>

<span data-ttu-id="f4d77-121">每個位移值6個最少的有效位會接受為帶正負號的值，並產生 \[ -32.. 31 的 \] 範圍。</span><span class="sxs-lookup"><span data-stu-id="f4d77-121">The 6 least significant bits of each offset value is honored as a signed value, yielding \[-32..31\] range.</span></span>

<span data-ttu-id="f4d77-122">此指示只適用于2D 材質，不同于 **gather4**，它也可搭配 TextureCubes 使用。</span><span class="sxs-lookup"><span data-stu-id="f4d77-122">This instruction only works with 2D textures, unlike **gather4**, which also works with TextureCubes.</span></span>

<span data-ttu-id="f4d77-123">取樣器中唯一接受的模式是定址模式。</span><span class="sxs-lookup"><span data-stu-id="f4d77-123">The only modes honored in the sampler are the addressing modes.</span></span> <span data-ttu-id="f4d77-124">只會使用資源檢視中最詳細的 mip。</span><span class="sxs-lookup"><span data-stu-id="f4d77-124">Only the most detailed mip in the resource view is used.</span></span>

<span data-ttu-id="f4d77-125">如果位址落在材質中心，這並不表示其他材質可以清空。</span><span class="sxs-lookup"><span data-stu-id="f4d77-125">If the address falls on a texel center, this does not mean the other texels can be zeroed out.</span></span>

<span data-ttu-id="f4d77-126">*SrcSampler* 參數包含 \[ . select \_ 元件 \] ，允許抓取紋理的任何單一元件，包括傳回遺漏元件的預設值。</span><span class="sxs-lookup"><span data-stu-id="f4d77-126">The *srcSampler* parameter includes \[.select\_component\], allowing any single component of a texture to be retrieved, including returning defaults for missing components.</span></span>

<span data-ttu-id="f4d77-127">針對具有 float32 元件的格式，如果要提取的值是正規化、反正規化、+-0 或 +-INF，則會傳回未改變的著色器。</span><span class="sxs-lookup"><span data-stu-id="f4d77-127">For formats with float32 components, if the value being fetched is normalized, denormalized, +-0 or +-INF, it is returned to the shader unaltered.</span></span> <span data-ttu-id="f4d77-128">NaN 會以 NaN 傳回，但是 NaN 的精確位標記法可能會變更。</span><span class="sxs-lookup"><span data-stu-id="f4d77-128">NaN is returned as NaN, but the exact bit representation of the NaN may be changed.</span></span> <span data-ttu-id="f4d77-129">針對 TextureCubes，遺漏第四個材質的部分合成必須在角落髮生，因此不會套用合成材質未變更的位的概念，而且可以清除 denorms。</span><span class="sxs-lookup"><span data-stu-id="f4d77-129">For TextureCubes, some synthesis of the missing 4th texel must occur at corners, so the notion of returning bits unchanged for the synthesized texel does not apply, and denorms could be flushed.</span></span>

<span data-ttu-id="f4d77-130">使用此指令可將 **gather4** 的位移範圍延伸到更大和可程式化。</span><span class="sxs-lookup"><span data-stu-id="f4d77-130">Use this instruction to extend offset range of **gather4** to be larger and programmable.</span></span> <span data-ttu-id="f4d77-131">名稱上的 "po" 尾碼表示「可程式化的位移」。</span><span class="sxs-lookup"><span data-stu-id="f4d77-131">The "po" suffix on the name means "programmable offset".</span></span>

<span data-ttu-id="f4d77-132">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="f4d77-132">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="f4d77-133">頂點</span><span class="sxs-lookup"><span data-stu-id="f4d77-133">Vertex</span></span> | <span data-ttu-id="f4d77-134">船體</span><span class="sxs-lookup"><span data-stu-id="f4d77-134">Hull</span></span> | <span data-ttu-id="f4d77-135">網域</span><span class="sxs-lookup"><span data-stu-id="f4d77-135">Domain</span></span> | <span data-ttu-id="f4d77-136">幾何</span><span class="sxs-lookup"><span data-stu-id="f4d77-136">Geometry</span></span> | <span data-ttu-id="f4d77-137">像素</span><span class="sxs-lookup"><span data-stu-id="f4d77-137">Pixel</span></span> | <span data-ttu-id="f4d77-138">計算</span><span class="sxs-lookup"><span data-stu-id="f4d77-138">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="f4d77-139">X</span><span class="sxs-lookup"><span data-stu-id="f4d77-139">X</span></span>      | <span data-ttu-id="f4d77-140">X</span><span class="sxs-lookup"><span data-stu-id="f4d77-140">X</span></span>    | <span data-ttu-id="f4d77-141">X</span><span class="sxs-lookup"><span data-stu-id="f4d77-141">X</span></span>      | <span data-ttu-id="f4d77-142">X</span><span class="sxs-lookup"><span data-stu-id="f4d77-142">X</span></span>        | <span data-ttu-id="f4d77-143">X</span><span class="sxs-lookup"><span data-stu-id="f4d77-143">X</span></span>     | <span data-ttu-id="f4d77-144">X</span><span class="sxs-lookup"><span data-stu-id="f4d77-144">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="f4d77-145">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="f4d77-145">Minimum Shader Model</span></span>

<span data-ttu-id="f4d77-146">下列著色器模型支援此指令：</span><span class="sxs-lookup"><span data-stu-id="f4d77-146">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="f4d77-147">著色器模型</span><span class="sxs-lookup"><span data-stu-id="f4d77-147">Shader Model</span></span>                                              | <span data-ttu-id="f4d77-148">支援</span><span class="sxs-lookup"><span data-stu-id="f4d77-148">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="f4d77-149">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="f4d77-149">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="f4d77-150">是</span><span class="sxs-lookup"><span data-stu-id="f4d77-150">yes</span></span>       |
| [<span data-ttu-id="f4d77-151">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="f4d77-151">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="f4d77-152">不可以</span><span class="sxs-lookup"><span data-stu-id="f4d77-152">no</span></span>        |
| [<span data-ttu-id="f4d77-153">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="f4d77-153">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="f4d77-154">不可以</span><span class="sxs-lookup"><span data-stu-id="f4d77-154">no</span></span>        |
| [<span data-ttu-id="f4d77-155">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="f4d77-155">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="f4d77-156">不可以</span><span class="sxs-lookup"><span data-stu-id="f4d77-156">no</span></span>        |
| [<span data-ttu-id="f4d77-157">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="f4d77-157">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="f4d77-158">不可以</span><span class="sxs-lookup"><span data-stu-id="f4d77-158">no</span></span>        |
| [<span data-ttu-id="f4d77-159">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="f4d77-159">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="f4d77-160">不可以</span><span class="sxs-lookup"><span data-stu-id="f4d77-160">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="f4d77-161">相關主題</span><span class="sxs-lookup"><span data-stu-id="f4d77-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f4d77-162">著色器模型5元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="f4d77-162">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





