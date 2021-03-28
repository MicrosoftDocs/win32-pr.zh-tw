---
title: 'sample_c (sm4-asm) '
description: 執行比較篩選。
ms.assetid: 59786ED2-48FB-494E-A5A4-F732D63BF01B
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23563fe52bbc943e8756d04085b66d156ab259d7
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104990735"
---
# <a name="sample_c-sm4---asm"></a><span data-ttu-id="b97b4-103">範例 \_ c (sm4-asm) </span><span class="sxs-lookup"><span data-stu-id="b97b4-103">sample\_c (sm4 - asm)</span></span>

<span data-ttu-id="b97b4-104">執行比較篩選。</span><span class="sxs-lookup"><span data-stu-id="b97b4-104">Performs a comparison filter.</span></span>



| <span data-ttu-id="b97b4-105">範例 \_ c \[ \_ aoffimmi (u，v，w) \] dest \[ \] ，srcAddress \[ . swizzle \] ，srcResource. r，//必須是。 r swizzle srcSampler，srcReferenceValue//選取單一元件</span><span class="sxs-lookup"><span data-stu-id="b97b4-105">sample\_c\[\_aoffimmi(u,v,w)\] dest\[.mask\], srcAddress\[.swizzle\], srcResource.r, // must be .r swizzle srcSampler, srcReferenceValue // single component selected</span></span> |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="b97b4-106">項目</span><span class="sxs-lookup"><span data-stu-id="b97b4-106">Item</span></span>                                                                                                                                       | <span data-ttu-id="b97b4-107">描述</span><span class="sxs-lookup"><span data-stu-id="b97b4-107">Description</span></span>                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b97b4-108"><span id="dest"></span><span id="DEST"></span>*目標*</span><span class="sxs-lookup"><span data-stu-id="b97b4-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                                            | <span data-ttu-id="b97b4-109">\[在 \] 操作結果的位址中。</span><span class="sxs-lookup"><span data-stu-id="b97b4-109">\[in\] The address of the results of the operation.</span></span><br/>                                                             |
| <span data-ttu-id="b97b4-110"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span><span class="sxs-lookup"><span data-stu-id="b97b4-110"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span></span><br/>                             | <span data-ttu-id="b97b4-111">\[在 \] 一組材質座標中。</span><span class="sxs-lookup"><span data-stu-id="b97b4-111">\[in\] A set of texture coordinates.</span></span> <span data-ttu-id="b97b4-112">如需詳細資訊，請參閱 [範例](sample--sm4---asm-.md) 指令。</span><span class="sxs-lookup"><span data-stu-id="b97b4-112">For more information see the [sample](sample--sm4---asm-.md) instruction.</span></span><br/> |
| <span data-ttu-id="b97b4-113"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span><span class="sxs-lookup"><span data-stu-id="b97b4-113"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/>                         | <span data-ttu-id="b97b4-114">\[在材質暫存器中 \] 。</span><span class="sxs-lookup"><span data-stu-id="b97b4-114">\[in\] A texture register.</span></span> <span data-ttu-id="b97b4-115">如需詳細資訊，請參閱 **範例** 指令。</span><span class="sxs-lookup"><span data-stu-id="b97b4-115">For more information see the **sample** instruction.</span></span><br/>                                 |
| <span data-ttu-id="b97b4-116"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span><span class="sxs-lookup"><span data-stu-id="b97b4-116"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span></span><br/>                             | <span data-ttu-id="b97b4-117">\[在 \] 取樣器註冊中。</span><span class="sxs-lookup"><span data-stu-id="b97b4-117">\[in\] A sampler register.</span></span> <span data-ttu-id="b97b4-118">如需詳細資訊，請參閱 **範例** 指令。</span><span class="sxs-lookup"><span data-stu-id="b97b4-118">For more information see the **sample** instruction.</span></span><br/>                                 |
| <span data-ttu-id="b97b4-119"><span id="srcReferenceValue"></span><span id="srcreferencevalue"></span><span id="SRCREFERENCEVALUE"></span>*srcReferenceValue*</span><span class="sxs-lookup"><span data-stu-id="b97b4-119"><span id="srcReferenceValue"></span><span id="srcreferencevalue"></span><span id="SRCREFERENCEVALUE"></span>*srcReferenceValue*</span></span><br/> | <span data-ttu-id="b97b4-120">\[在 \] 已選取單一元件的註冊中，用於比較。</span><span class="sxs-lookup"><span data-stu-id="b97b4-120">\[in\] A register with a single component selected, which is used in the comparison.</span></span><br/>                            |



 

## <a name="remarks"></a><span data-ttu-id="b97b4-121">備註</span><span class="sxs-lookup"><span data-stu-id="b97b4-121">Remarks</span></span>

<span data-ttu-id="b97b4-122">此指示的主要目的是提供 Percentage-Closer 深度篩選的建立區塊。</span><span class="sxs-lookup"><span data-stu-id="b97b4-122">The primary purpose for this instruction is to provide a building-block for Percentage-Closer Depth filtering.</span></span> <span data-ttu-id="b97b4-123">**範例 \_ c** 中的 "c" 代表比較。</span><span class="sxs-lookup"><span data-stu-id="b97b4-123">The "c" in **sample\_c** stands for Comparison.</span></span>

<span data-ttu-id="b97b4-124">**範例 \_ c** 的運算元與 [範例](sample--sm4---asm-.md)指令相同，不同之處在于有一個額外的 float32 來源運算元 *srcReferenceValue*，它必須是已選取單一元件的暫存器，或純量常值。</span><span class="sxs-lookup"><span data-stu-id="b97b4-124">The operands to **sample\_c** are identical to the [sample](sample--sm4---asm-.md) instruction, except that there is an additional float32 source operand, *srcReferenceValue*, which must be a register with single-component selected, or a scalar literal.</span></span>

<span data-ttu-id="b97b4-125">SrcResource 參數的參數必須是. r (red) swizzle。</span><span class="sxs-lookup"><span data-stu-id="b97b4-125">The *srcResource* parameter must have a .r (red) swizzle.</span></span> <span data-ttu-id="b97b4-126">**範例 \_ c** 專門針對 red 元件運作，並傳回單一值。</span><span class="sxs-lookup"><span data-stu-id="b97b4-126">**sample\_c** operates exclusively on the red component, and returns a single value.</span></span> <span data-ttu-id="b97b4-127">*SrcResource* 上的 r swizzle 表示純量結果會複寫到所有元件。</span><span class="sxs-lookup"><span data-stu-id="b97b4-127">The .r swizzle on *srcResource* indicates that the scalar result is replicated to all components.</span></span>

<span data-ttu-id="b97b4-128">當深度緩衝區設定為輸入材質時，[深度] 值會顯示在紅色的元件中。</span><span class="sxs-lookup"><span data-stu-id="b97b4-128">When a Depth Buffer is set as an input texture, the depth value shows up in the red component.</span></span>

<span data-ttu-id="b97b4-129">如果這個指令與非 Texture1D/2D/2DArray/Cube/CubeArray 的資源搭配使用，它會產生未定義的結果。</span><span class="sxs-lookup"><span data-stu-id="b97b4-129">If this instruction is used with a Resource that is not a Texture1D/2D/2DArray/Cube/CubeArray, it produces undefined results.</span></span>

<span data-ttu-id="b97b4-130">當執行此指令時，取樣硬體會使用目前取樣器的 ComparisonFunction，針對每個篩選「點」位置上來源資源的紅色元件值進行比較 *srcReferenceValue* ， (材質) 目前設定的材質篩選器會根據 *srcAddress* 中提供的座標來涵蓋。</span><span class="sxs-lookup"><span data-stu-id="b97b4-130">When this instruction is executed, the sampling hardware uses the current Sampler's ComparisonFunction to compare *srcReferenceValue* against the Red component value for the source Resource at each filter "tap" location (texel) that the currently configured texture filter covers, based on the provided coordinates in *srcAddress*.</span></span>

<span data-ttu-id="b97b4-131">在 *srcReferenceValue* 已量化至材質格式的有效位數之後，會進行比較，與在輸出合併可見度測試的深度比較之前，z 的量化為深度緩衝區精確度的方式完全相同。</span><span class="sxs-lookup"><span data-stu-id="b97b4-131">The comparison occurs after *srcReferenceValue* has been quantized to the precision of the texture format, in exactly the same way that z is quantized to depth buffer precision before Depth Comparison at the Output Merger visibility test.</span></span> <span data-ttu-id="b97b4-132">這包括格式範圍的夾具 (例如 \[ 0 ..1 \] 表示 UNORM 格式) 。</span><span class="sxs-lookup"><span data-stu-id="b97b4-132">This includes a clamp to the format range (e.g. \[0..1\] for a UNORM format).</span></span>

<span data-ttu-id="b97b4-133">來源材質的紅色元件會與量化 *srcReferenceValue* 進行比較。</span><span class="sxs-lookup"><span data-stu-id="b97b4-133">The source texel's Red component is compared against the quantized *srcReferenceValue*.</span></span> <span data-ttu-id="b97b4-134">若為落在資源的材質，則會藉由套用位址模式 (和 BorderColorR （如果是以框線模式從取樣器) ）來判斷紅色元件值。</span><span class="sxs-lookup"><span data-stu-id="b97b4-134">For texels that fall off the Resource, the Red component value is determined by applying the Address Modes (and BorderColorR if in Border mode) from the Sampler.</span></span> <span data-ttu-id="b97b4-135">這項比較會接受所有的 D3D11 浮點數比較規則，在此情況下，材質格式為浮點數。</span><span class="sxs-lookup"><span data-stu-id="b97b4-135">The comparison honors all D3D11 floating point comparison rules, in the case the texture format is floating point.</span></span>

<span data-ttu-id="b97b4-136">每次傳遞的比較都會傳回 1.0 f 做為材質的紅色元件值，而失敗的每個比較都會傳回 0.0 f 作為紋理的紅色值。</span><span class="sxs-lookup"><span data-stu-id="b97b4-136">Each comparison that passes returns 1.0f as the Red component value for the texel, and each comparison that fails returns 0.0f as the Red value for the texture.</span></span> <span data-ttu-id="b97b4-137">然後篩選會完全依照取樣器狀態所指定、只在 Red 元件中運作，並將單一純量篩選結果傳回給著色器，並複寫到所有遮罩的 *目的地* 元件。</span><span class="sxs-lookup"><span data-stu-id="b97b4-137">Filtering then occurs exactly as specified by the Sampler states, operating only in the Red component, and returning a single scalar filter result back to the Shader, replicated to all masked *dest* components.</span></span>

<span data-ttu-id="b97b4-138">**範例 \_ c** 的使用會與其他所有一般用途篩選控制項相互交。</span><span class="sxs-lookup"><span data-stu-id="b97b4-138">The use of **sample\_c** is orthogonal to all other general purpose filtering controls.</span></span> <span data-ttu-id="b97b4-139">**範例 \_ c** 可與其他一般用途篩選模式緊密搭配運作。</span><span class="sxs-lookup"><span data-stu-id="b97b4-139">**sample\_c** works seamlessly with the other general purpose filter modes.</span></span> <span data-ttu-id="b97b4-140">**範例 \_ c** 會變更一般用途篩選器的行為，使篩選的值全都會因為比較結果而變成 1.0 f 或 0.0 f。</span><span class="sxs-lookup"><span data-stu-id="b97b4-140">**sample\_c** changes the behavior of the general purpose filters such that the values being filtered all become 1.0f or 0.0f due to comparison results.</span></span>

<span data-ttu-id="b97b4-141">從未系結任何專案的輸入位置提取，會針對所有元件傳回0。</span><span class="sxs-lookup"><span data-stu-id="b97b4-141">Fetching from an input slot that has nothing bound to it returns 0 for all components.</span></span>

<span data-ttu-id="b97b4-142">如需詳細資訊，請參閱 [範例](sample--sm4---asm-.md) 指令。</span><span class="sxs-lookup"><span data-stu-id="b97b4-142">For more information, see the [sample](sample--sm4---asm-.md) instruction.</span></span>

<span data-ttu-id="b97b4-143">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="b97b4-143">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="b97b4-144">頂點著色器</span><span class="sxs-lookup"><span data-stu-id="b97b4-144">Vertex Shader</span></span> | <span data-ttu-id="b97b4-145">幾何著色器</span><span class="sxs-lookup"><span data-stu-id="b97b4-145">Geometry Shader</span></span> | <span data-ttu-id="b97b4-146">像素著色器</span><span class="sxs-lookup"><span data-stu-id="b97b4-146">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
|               |                 | <span data-ttu-id="b97b4-147">x</span><span class="sxs-lookup"><span data-stu-id="b97b4-147">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="b97b4-148">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="b97b4-148">Minimum Shader Model</span></span>

<span data-ttu-id="b97b4-149">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="b97b4-149">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="b97b4-150">著色器模型</span><span class="sxs-lookup"><span data-stu-id="b97b4-150">Shader Model</span></span>                                              | <span data-ttu-id="b97b4-151">支援</span><span class="sxs-lookup"><span data-stu-id="b97b4-151">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="b97b4-152">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="b97b4-152">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="b97b4-153">是</span><span class="sxs-lookup"><span data-stu-id="b97b4-153">yes</span></span>       |
| [<span data-ttu-id="b97b4-154">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="b97b4-154">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="b97b4-155">是</span><span class="sxs-lookup"><span data-stu-id="b97b4-155">yes</span></span>       |
| [<span data-ttu-id="b97b4-156">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="b97b4-156">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="b97b4-157">是</span><span class="sxs-lookup"><span data-stu-id="b97b4-157">yes</span></span>       |
| [<span data-ttu-id="b97b4-158">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="b97b4-158">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="b97b4-159">不可以</span><span class="sxs-lookup"><span data-stu-id="b97b4-159">no</span></span>        |
| [<span data-ttu-id="b97b4-160">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="b97b4-160">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="b97b4-161">不可以</span><span class="sxs-lookup"><span data-stu-id="b97b4-161">no</span></span>        |
| [<span data-ttu-id="b97b4-162">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="b97b4-162">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="b97b4-163">不可以</span><span class="sxs-lookup"><span data-stu-id="b97b4-163">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="b97b4-164">相關主題</span><span class="sxs-lookup"><span data-stu-id="b97b4-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b97b4-165">著色器模型4元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="b97b4-165">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





