---
title: 'sample_d (sm4-asm) '
description: '使用指定之取樣器所識別的指定位址和篩選模式，從指定的專案/材質取樣資料。 |sample_d (sm4-asm) '
ms.assetid: 9CF57C4A-C0D1-4D57-A5EE-62BBBB291438
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abe2d3ad310c18ff2bb10e101c95e0267d534fed
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104992042"
---
# <a name="sample_d-sm4---asm"></a><span data-ttu-id="a5357-104">範例 \_ d (sm4-asm) </span><span class="sxs-lookup"><span data-stu-id="a5357-104">sample\_d (sm4 - asm)</span></span>

<span data-ttu-id="a5357-105">使用指定之取樣器所識別的指定位址和篩選模式，從指定的專案/材質取樣資料。</span><span class="sxs-lookup"><span data-stu-id="a5357-105">Samples data from the specified Element/texture using the specified address and the filtering mode identified by the given sampler.</span></span>



| <span data-ttu-id="a5357-106">ssample \_ d \[ \_ aoffimmi (u、v、w) \] dest \[ \] 、srcAddress \[ . swizzle \] 、srcResource、swizzle、 \[ \] srcSampler、srcXDerivatives \[ . swizzle \] 、srcYDerivatives \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="a5357-106">ssample\_d\[\_aoffimmi(u,v,w)\] dest\[.mask\], srcAddress\[.swizzle\], srcResource\[.swizzle\], srcSampler, srcXDerivatives\[.swizzle\], srcYDerivatives\[.swizzle\]</span></span> |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="a5357-107">項目</span><span class="sxs-lookup"><span data-stu-id="a5357-107">Item</span></span>                                                                                                                               | <span data-ttu-id="a5357-108">描述</span><span class="sxs-lookup"><span data-stu-id="a5357-108">Description</span></span>                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5357-109"><span id="dest"></span><span id="DEST"></span>*目標*</span><span class="sxs-lookup"><span data-stu-id="a5357-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                                    | <span data-ttu-id="a5357-110">\[在 \] 操作結果的位址中。</span><span class="sxs-lookup"><span data-stu-id="a5357-110">\[in\] The address of the results of the operation.</span></span><br/>                                                                  |
| <span data-ttu-id="a5357-111"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span><span class="sxs-lookup"><span data-stu-id="a5357-111"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span></span><br/>                     | <span data-ttu-id="a5357-112">\[在 \] 一組材質座標中。</span><span class="sxs-lookup"><span data-stu-id="a5357-112">\[in\] A set of texture coordinates.</span></span> <span data-ttu-id="a5357-113">如需詳細資訊，請參閱 [範例](sample--sm4---asm-.md) 指令。</span><span class="sxs-lookup"><span data-stu-id="a5357-113">For more information see the [sample](sample--sm4---asm-.md) instruction.</span></span><br/>      |
| <span data-ttu-id="a5357-114"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span><span class="sxs-lookup"><span data-stu-id="a5357-114"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/>                 | <span data-ttu-id="a5357-115">\[在材質暫存器中 \] 。</span><span class="sxs-lookup"><span data-stu-id="a5357-115">\[in\] A texture register.</span></span> <span data-ttu-id="a5357-116">如需詳細資訊，請參閱 **範例** 指令。</span><span class="sxs-lookup"><span data-stu-id="a5357-116">For more information see the **sample** instruction.</span></span><br/>                                      |
| <span data-ttu-id="a5357-117"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span><span class="sxs-lookup"><span data-stu-id="a5357-117"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span></span><br/>                     | <span data-ttu-id="a5357-118">\[在 \] 取樣器註冊中。</span><span class="sxs-lookup"><span data-stu-id="a5357-118">\[in\] A sampler register.</span></span> <span data-ttu-id="a5357-119">如需詳細資訊，請參閱 **範例** 指令。</span><span class="sxs-lookup"><span data-stu-id="a5357-119">For more information see the **sample** instruction.</span></span><br/>                                      |
| <span data-ttu-id="a5357-120"><span id="srcXDerivatives"></span><span id="srcxderivatives"></span><span id="SRCXDERIVATIVES"></span>*srcXDerivatives*</span><span class="sxs-lookup"><span data-stu-id="a5357-120"><span id="srcXDerivatives"></span><span id="srcxderivatives"></span><span id="SRCXDERIVATIVES"></span>*srcXDerivatives*</span></span><br/> | <span data-ttu-id="a5357-121">\[以 \] x 方向的來源位址衍生。</span><span class="sxs-lookup"><span data-stu-id="a5357-121">\[in\] The derivatives for the source address in the x direction.</span></span> <span data-ttu-id="a5357-122">如需詳細資訊，請參閱「 **備註** 」一節。</span><span class="sxs-lookup"><span data-stu-id="a5357-122">For more information, see the **Remarks** section.</span></span><br/> |
| <span data-ttu-id="a5357-123"><span id="srcYDerivatives"></span><span id="srcyderivatives"></span><span id="SRCYDERIVATIVES"></span>*srcYDerivatives*</span><span class="sxs-lookup"><span data-stu-id="a5357-123"><span id="srcYDerivatives"></span><span id="srcyderivatives"></span><span id="SRCYDERIVATIVES"></span>*srcYDerivatives*</span></span><br/> | <span data-ttu-id="a5357-124">\[以 \] y 方向的來源位址衍生。</span><span class="sxs-lookup"><span data-stu-id="a5357-124">\[in\] The derivatives for the source address in the y direction.</span></span> <span data-ttu-id="a5357-125">如需詳細資訊，請參閱「 **備註** 」一節。</span><span class="sxs-lookup"><span data-stu-id="a5357-125">For more information, see the **Remarks** section.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a5357-126">備註</span><span class="sxs-lookup"><span data-stu-id="a5357-126">Remarks</span></span>

<span data-ttu-id="a5357-127">此指示的行為就像 [範例](sample--sm4---asm-.md) 指令，不同之處在于 x 方向和 y 方向的來源位址衍生是由額外的參數（ *srcXDerivatives* 和 *srcYDerivatives*）所提供。</span><span class="sxs-lookup"><span data-stu-id="a5357-127">This instruction behaves like the [sample](sample--sm4---asm-.md) instruction, except that derivatives for the source address in the x direction and the y direction are provided by extra parameters, *srcXDerivatives* and *srcYDerivatives*, respectively.</span></span> <span data-ttu-id="a5357-128">這些衍生的是標準化的材質座標空間。</span><span class="sxs-lookup"><span data-stu-id="a5357-128">These derivatives are in normalized texture coordinate space.</span></span>

<span data-ttu-id="a5357-129">*SrcXDerivatives* 的 r、g 和 b 元件 (POS swizzle) 提供 du/dx、dv/dx 和 dw/dx。</span><span class="sxs-lookup"><span data-stu-id="a5357-129">The r, g and b components of *srcXDerivatives* (POS-swizzle) provide du/dx, dv/dx and dw/dx.</span></span> <span data-ttu-id="a5357-130">會忽略 ' a ' 元件 (POS swizzle) 。</span><span class="sxs-lookup"><span data-stu-id="a5357-130">The 'a' component (POS-swizzle) is ignored.</span></span>

<span data-ttu-id="a5357-131">*SrcYDerivatives* 的 r、g 和 b 元件 (POS-swizzle) 提供 du/dy、dv/dy 和 dw/dy。</span><span class="sxs-lookup"><span data-stu-id="a5357-131">The r, g and b components of *srcYDerivatives* (POS-swizzle) provide du/dy, dv/dy and dw/dy.</span></span> <span data-ttu-id="a5357-132">會忽略 ' a ' 元件 (POS swizzle) 。</span><span class="sxs-lookup"><span data-stu-id="a5357-132">The 'a' component (POS-swizzle) is ignored.</span></span>

<span data-ttu-id="a5357-133">與範例指令不同，這是允許跨2x2 戳記共用單一」 LOD 計算的 **範例** 指令，因此，在圖元著色器中使用時， **範例 \_ d** 必須完全獨立地計算」 lod。</span><span class="sxs-lookup"><span data-stu-id="a5357-133">Unlike the **sample** instruction, which is permitted to share a single LOD calculation across a 2x2 stamp, **sample\_d** must calculate LOD completely independently, per-pixel when used in the Pixel Shader.</span></span>

<span data-ttu-id="a5357-134">如果 **範例 \_ d** 的衍生輸入來自圖元著色器中的衍生計算指示，且值包含 INF/NaN，則 **範例 \_ d** 的行為可能與 **範例** 指令不相符，這會隱含地計算衍生。</span><span class="sxs-lookup"><span data-stu-id="a5357-134">If the derivative inputs to **sample\_d** came from derivative calculation instructions in the Pixel Shader and the values include INF/NaN, the behavior of **sample\_d** may not match the **sample** instruction, which implicitly computes the derivative.</span></span> <span data-ttu-id="a5357-135">INF/NaN 值可能會以不同的方式影響」 LOD 計算。</span><span class="sxs-lookup"><span data-stu-id="a5357-135">The INF/NaN values may affect the LOD calculation differently.</span></span>

<span data-ttu-id="a5357-136">從未系結任何專案的輸入位置提取，會針對所有元件傳回0。</span><span class="sxs-lookup"><span data-stu-id="a5357-136">Fetching from an input slot that has nothing bound to it returns 0 for all components.</span></span>

### <a name="restrictions"></a><span data-ttu-id="a5357-137">限制</span><span class="sxs-lookup"><span data-stu-id="a5357-137">Restrictions</span></span>

-   <span data-ttu-id="a5357-138">**範例 \_ d** 會繼承與 **範例** 指令相同的限制，再加上下列額外參數的限制。</span><span class="sxs-lookup"><span data-stu-id="a5357-138">**sample\_d** inherits the same restrictions as the **sample** instruction, plus additional an restriction below for its additional parameters.</span></span>
-   <span data-ttu-id="a5357-139">*srcXDerivatives* 和 *srcYDerivatives* 必須是 temp (r \# /x \#) 、constantBuffer (cb \#) 、輸入 (v \#) 註冊或立即值 (s) 。</span><span class="sxs-lookup"><span data-stu-id="a5357-139">*srcXDerivatives* and *srcYDerivatives* must be temp (r\#/x\#), constantBuffer (cb\#), input (v\#) registers or immediate value(s).</span></span>

<span data-ttu-id="a5357-140">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="a5357-140">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="a5357-141">頂點著色器</span><span class="sxs-lookup"><span data-stu-id="a5357-141">Vertex Shader</span></span> | <span data-ttu-id="a5357-142">幾何著色器</span><span class="sxs-lookup"><span data-stu-id="a5357-142">Geometry Shader</span></span> | <span data-ttu-id="a5357-143">像素著色器</span><span class="sxs-lookup"><span data-stu-id="a5357-143">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="a5357-144">X</span><span class="sxs-lookup"><span data-stu-id="a5357-144">X</span></span>             | <span data-ttu-id="a5357-145">X</span><span class="sxs-lookup"><span data-stu-id="a5357-145">X</span></span>               | <span data-ttu-id="a5357-146">x</span><span class="sxs-lookup"><span data-stu-id="a5357-146">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="a5357-147">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="a5357-147">Minimum Shader Model</span></span>

<span data-ttu-id="a5357-148">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="a5357-148">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="a5357-149">著色器模型</span><span class="sxs-lookup"><span data-stu-id="a5357-149">Shader Model</span></span>                                              | <span data-ttu-id="a5357-150">支援</span><span class="sxs-lookup"><span data-stu-id="a5357-150">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="a5357-151">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="a5357-151">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="a5357-152">是</span><span class="sxs-lookup"><span data-stu-id="a5357-152">yes</span></span>       |
| [<span data-ttu-id="a5357-153">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="a5357-153">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="a5357-154">是</span><span class="sxs-lookup"><span data-stu-id="a5357-154">yes</span></span>       |
| [<span data-ttu-id="a5357-155">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="a5357-155">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="a5357-156">是</span><span class="sxs-lookup"><span data-stu-id="a5357-156">yes</span></span>       |
| [<span data-ttu-id="a5357-157">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="a5357-157">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="a5357-158">不可以</span><span class="sxs-lookup"><span data-stu-id="a5357-158">no</span></span>        |
| [<span data-ttu-id="a5357-159">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="a5357-159">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="a5357-160">不可以</span><span class="sxs-lookup"><span data-stu-id="a5357-160">no</span></span>        |
| [<span data-ttu-id="a5357-161">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="a5357-161">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="a5357-162">不可以</span><span class="sxs-lookup"><span data-stu-id="a5357-162">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="a5357-163">相關主題</span><span class="sxs-lookup"><span data-stu-id="a5357-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a5357-164">著色器模型4元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="a5357-164">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





