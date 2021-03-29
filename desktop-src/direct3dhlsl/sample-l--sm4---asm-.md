---
title: 'sample_l (sm4-asm) '
description: '使用指定之取樣器所識別的指定位址和篩選模式，從指定的專案/材質取樣資料。 |sample_l (sm4-asm) '
ms.assetid: D285F63E-1026-45F1-9959-6F5AB2A27C95
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5acd83d81e4648cc9eae5f8e0166013dcca512a8
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104322320"
---
# <a name="sample_l-sm4---asm"></a><span data-ttu-id="9c388-104">範例 \_ l (sm4-asm) </span><span class="sxs-lookup"><span data-stu-id="9c388-104">sample\_l (sm4 - asm)</span></span>

<span data-ttu-id="9c388-105">使用指定之取樣器所識別的指定位址和篩選模式，從指定的專案/材質取樣資料。</span><span class="sxs-lookup"><span data-stu-id="9c388-105">Samples data from the specified Element/texture using the specified address and the filtering mode identified by the given sampler.</span></span>



| <span data-ttu-id="9c388-106">範例 \_ l \[ \_ aoffimmi (u，v，w) \] dest \[ \] ，srcAddress \[ . swizzle \] ，srcResource \[ . swizzle \] ，srcSampler，srcLOD. select \_ component</span><span class="sxs-lookup"><span data-stu-id="9c388-106">sample\_l\[\_aoffimmi(u,v,w)\] dest\[.mask\], srcAddress\[.swizzle\], srcResource\[.swizzle\], srcSampler, srcLOD.select\_component</span></span> |
|-------------------------------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="9c388-107">項目</span><span class="sxs-lookup"><span data-stu-id="9c388-107">Item</span></span>                                                                                                               | <span data-ttu-id="9c388-108">描述</span><span class="sxs-lookup"><span data-stu-id="9c388-108">Description</span></span>                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c388-109"><span id="dest"></span><span id="DEST"></span>*目標*</span><span class="sxs-lookup"><span data-stu-id="9c388-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                    | <span data-ttu-id="9c388-110">\[在 \] 操作結果的位址中。</span><span class="sxs-lookup"><span data-stu-id="9c388-110">\[in\] The address of the results of the operation.</span></span><br/>                                                             |
| <span data-ttu-id="9c388-111"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span><span class="sxs-lookup"><span data-stu-id="9c388-111"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span></span><br/>     | <span data-ttu-id="9c388-112">\[在 \] 一組材質座標中。</span><span class="sxs-lookup"><span data-stu-id="9c388-112">\[in\] A set of texture coordinates.</span></span> <span data-ttu-id="9c388-113">如需詳細資訊，請參閱 [範例](sample--sm4---asm-.md) 指令。</span><span class="sxs-lookup"><span data-stu-id="9c388-113">For more information see the [sample](sample--sm4---asm-.md) instruction.</span></span><br/> |
| <span data-ttu-id="9c388-114"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span><span class="sxs-lookup"><span data-stu-id="9c388-114"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/> | <span data-ttu-id="9c388-115">\[在材質暫存器中 \] 。</span><span class="sxs-lookup"><span data-stu-id="9c388-115">\[in\] A texture register.</span></span> <span data-ttu-id="9c388-116">如需詳細資訊，請參閱 **範例** 指令。</span><span class="sxs-lookup"><span data-stu-id="9c388-116">For more information see the **sample** instruction.</span></span><br/>                                 |
| <span data-ttu-id="9c388-117"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span><span class="sxs-lookup"><span data-stu-id="9c388-117"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span></span><br/>     | <span data-ttu-id="9c388-118">\[在 \] 取樣器註冊中。</span><span class="sxs-lookup"><span data-stu-id="9c388-118">\[in\] A sampler register.</span></span> <span data-ttu-id="9c388-119">如需詳細資訊，請參閱 **範例** 指令。</span><span class="sxs-lookup"><span data-stu-id="9c388-119">For more information see the **sample** instruction.</span></span><br/>                                 |
| <span data-ttu-id="9c388-120"><span id="srcLOD"></span><span id="srclod"></span><span id="SRCLOD"></span>*srcLOD*</span><span class="sxs-lookup"><span data-stu-id="9c388-120"><span id="srcLOD"></span><span id="srclod"></span><span id="SRCLOD"></span>*srcLOD*</span></span><br/>                     | <span data-ttu-id="9c388-121">\[在 \] 」 lod 中。</span><span class="sxs-lookup"><span data-stu-id="9c388-121">\[in\] The LOD.</span></span><br/>                                                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="9c388-122">備註</span><span class="sxs-lookup"><span data-stu-id="9c388-122">Remarks</span></span>

<span data-ttu-id="9c388-123">此指示與 [範例](sample--sm4---asm-.md)相同，不同之處在于」 lod 是由應用程式直接提供為純量值，表示沒有 anisotropy。</span><span class="sxs-lookup"><span data-stu-id="9c388-123">This instruction is identical to [sample](sample--sm4---asm-.md), except that LOD is provided directly by the application as a scalar value, representing no anisotropy.</span></span> <span data-ttu-id="9c388-124">此指示適用于所有 progammable 著色器階段。</span><span class="sxs-lookup"><span data-stu-id="9c388-124">This instruction is available in all progammable Shader stages.</span></span>

<span data-ttu-id="9c388-125">**範例 \_ l** ：使用 *srcLOD* 作為」 lod 的材質範例。</span><span class="sxs-lookup"><span data-stu-id="9c388-125">**sample\_l** samples the texture using *srcLOD* to be the LOD.</span></span> <span data-ttu-id="9c388-126">如果」 LOD 值為 <= 0，則會選擇 zero'th (最大的地圖) ，並根據篩選模式) 套用放大篩選 (如果適用的話。</span><span class="sxs-lookup"><span data-stu-id="9c388-126">If the LOD value is <= 0, the zero'th (biggest map) is chosen, with the magnify filter applied (if applicable based on the filter mode).</span></span> <span data-ttu-id="9c388-127">因為 *srcLOD* 是浮點值，所以如果縮短篩選準則為線性或使用非等向篩選，則會使用小數值在兩個 mip 層級之間插補。</span><span class="sxs-lookup"><span data-stu-id="9c388-127">Because *srcLOD* is a floating point value, the fractional value is used to interpolate between two mip levels, if the minify filter is LINEAR or with anisotropic filtering.</span></span>

<span data-ttu-id="9c388-128">**範例 \_ l** 會忽略位址衍生，因此篩選行為純粹是 isotropic。</span><span class="sxs-lookup"><span data-stu-id="9c388-128">**sample\_l** ignores address derivatives, so filtering behavior is purely isotropic.</span></span> <span data-ttu-id="9c388-129">因為衍生的會被忽略，所以會以 isotropic 篩選的形式來運作。</span><span class="sxs-lookup"><span data-stu-id="9c388-129">Because derivatives are ignored, anisotropic filtering behaves as isotropic filtering.</span></span>

<span data-ttu-id="9c388-130">會接受取樣器狀態 MIPLODBIAS 和 MAX/MINMIPLEVEL。</span><span class="sxs-lookup"><span data-stu-id="9c388-130">Sampler states MIPLODBIAS and MAX/MINMIPLEVEL are honored.</span></span>

<span data-ttu-id="9c388-131">在圖元著色器中使用時， **範例 \_ l** 表示選擇的」 lod 是每個圖元，而不會影響連續的圖元，例如在相同的2x2 戳記中。</span><span class="sxs-lookup"><span data-stu-id="9c388-131">When used in the Pixel Shader, **sample\_l** implies that the choice of LOD is per-pixel, with no effect from neighboring pixels, for example in the same 2x2 stamp.</span></span>

<span data-ttu-id="9c388-132">從未系結任何專案的輸入位置提取，會針對所有元件傳回0。</span><span class="sxs-lookup"><span data-stu-id="9c388-132">Fetching from an input slot that has nothing bound to it returns 0 for all components.</span></span>

<span data-ttu-id="9c388-133">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="9c388-133">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="9c388-134">頂點著色器</span><span class="sxs-lookup"><span data-stu-id="9c388-134">Vertex Shader</span></span> | <span data-ttu-id="9c388-135">幾何著色器</span><span class="sxs-lookup"><span data-stu-id="9c388-135">Geometry Shader</span></span> | <span data-ttu-id="9c388-136">像素著色器</span><span class="sxs-lookup"><span data-stu-id="9c388-136">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="9c388-137">X</span><span class="sxs-lookup"><span data-stu-id="9c388-137">X</span></span>             | <span data-ttu-id="9c388-138">X</span><span class="sxs-lookup"><span data-stu-id="9c388-138">X</span></span>               | <span data-ttu-id="9c388-139">x</span><span class="sxs-lookup"><span data-stu-id="9c388-139">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="9c388-140">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="9c388-140">Minimum Shader Model</span></span>

<span data-ttu-id="9c388-141">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="9c388-141">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="9c388-142">著色器模型</span><span class="sxs-lookup"><span data-stu-id="9c388-142">Shader Model</span></span>                                              | <span data-ttu-id="9c388-143">支援</span><span class="sxs-lookup"><span data-stu-id="9c388-143">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="9c388-144">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="9c388-144">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="9c388-145">是</span><span class="sxs-lookup"><span data-stu-id="9c388-145">yes</span></span>       |
| [<span data-ttu-id="9c388-146">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="9c388-146">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="9c388-147">是</span><span class="sxs-lookup"><span data-stu-id="9c388-147">yes</span></span>       |
| [<span data-ttu-id="9c388-148">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="9c388-148">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="9c388-149">是</span><span class="sxs-lookup"><span data-stu-id="9c388-149">yes</span></span>       |
| [<span data-ttu-id="9c388-150">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="9c388-150">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="9c388-151">不可以</span><span class="sxs-lookup"><span data-stu-id="9c388-151">no</span></span>        |
| [<span data-ttu-id="9c388-152">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="9c388-152">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="9c388-153">不可以</span><span class="sxs-lookup"><span data-stu-id="9c388-153">no</span></span>        |
| [<span data-ttu-id="9c388-154">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="9c388-154">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="9c388-155">不可以</span><span class="sxs-lookup"><span data-stu-id="9c388-155">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="9c388-156">相關主題</span><span class="sxs-lookup"><span data-stu-id="9c388-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9c388-157">著色器模型4元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="9c388-157">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





