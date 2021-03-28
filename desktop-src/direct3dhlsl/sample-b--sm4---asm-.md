---
title: 'sample_b (sm4-asm) '
description: '使用指定之取樣器所識別的指定位址和篩選模式，從指定的專案/材質取樣資料。 |sample_b (sm4-asm) '
ms.assetid: FC0DF03E-9C21-4E88-96ED-EEFE86017E7C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72e82696ecc5b01847f87b39cbfeba0c665bcde4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104196067"
---
# <a name="sample_b-sm4---asm"></a><span data-ttu-id="50343-104">範例 \_ b (sm4-asm) </span><span class="sxs-lookup"><span data-stu-id="50343-104">sample\_b (sm4 - asm)</span></span>

<span data-ttu-id="50343-105">使用指定之取樣器所識別的指定位址和篩選模式，從指定的專案/材質取樣資料。</span><span class="sxs-lookup"><span data-stu-id="50343-105">Samples data from the specified Element/texture using the specified address and the filtering mode identified by the given sampler.</span></span>



| <span data-ttu-id="50343-106">範例 \_ b \[ \_ aoffimmi (u、v、w) \] dest \[ \] 、srcAddress \[ . swizzle \] 、srcResource \[ . swizzle \] 、srcSampler、srcLODBias. 選取 \_ 元件</span><span class="sxs-lookup"><span data-stu-id="50343-106">sample\_b\[\_aoffimmi(u,v,w)\] dest\[.mask\], srcAddress\[.swizzle\], srcResource\[.swizzle\], srcSampler, srcLODBias.select\_component</span></span> |
|-----------------------------------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="50343-107">項目</span><span class="sxs-lookup"><span data-stu-id="50343-107">Item</span></span>                                                                                                               | <span data-ttu-id="50343-108">描述</span><span class="sxs-lookup"><span data-stu-id="50343-108">Description</span></span>                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50343-109"><span id="dest"></span><span id="DEST"></span>*目標*</span><span class="sxs-lookup"><span data-stu-id="50343-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                    | <span data-ttu-id="50343-110">\[在 \] 操作結果的位址中。</span><span class="sxs-lookup"><span data-stu-id="50343-110">\[in\] The address of the result of the operation.</span></span><br/>                                                              |
| <span data-ttu-id="50343-111"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span><span class="sxs-lookup"><span data-stu-id="50343-111"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span></span><br/>     | <span data-ttu-id="50343-112">\[在 \] 一組材質座標中。</span><span class="sxs-lookup"><span data-stu-id="50343-112">\[in\] A set of texture coordinates.</span></span> <span data-ttu-id="50343-113">如需詳細資訊，請參閱 [範例](sample--sm4---asm-.md) 指令。</span><span class="sxs-lookup"><span data-stu-id="50343-113">For more information see the [sample](sample--sm4---asm-.md) instruction.</span></span><br/> |
| <span data-ttu-id="50343-114"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span><span class="sxs-lookup"><span data-stu-id="50343-114"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/> | <span data-ttu-id="50343-115">\[在材質暫存器中 \] 。</span><span class="sxs-lookup"><span data-stu-id="50343-115">\[in\] A texture register.</span></span> <span data-ttu-id="50343-116">如需詳細資訊，請參閱 **範例** 指令。</span><span class="sxs-lookup"><span data-stu-id="50343-116">For more information see the **sample** instruction.</span></span><br/>                                 |
| <span data-ttu-id="50343-117"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span><span class="sxs-lookup"><span data-stu-id="50343-117"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span></span><br/>     | <span data-ttu-id="50343-118">\[在 \] 取樣器註冊中。</span><span class="sxs-lookup"><span data-stu-id="50343-118">\[in\] A sampler register.</span></span> <span data-ttu-id="50343-119">如需詳細資訊，請參閱 **範例** 指令。</span><span class="sxs-lookup"><span data-stu-id="50343-119">For more information see the **sample** instruction.</span></span><br/>                                 |
| <span data-ttu-id="50343-120"><span id="srcLODBias"></span><span id="srclodbias"></span><span id="SRCLODBIAS"></span>*srcLODBias*</span><span class="sxs-lookup"><span data-stu-id="50343-120"><span id="srcLODBias"></span><span id="srclodbias"></span><span id="SRCLODBIAS"></span>*srcLODBias*</span></span><br/>     | <span data-ttu-id="50343-121">\[\]如需此參數的詳細資訊，請參閱「**備註**」一節。</span><span class="sxs-lookup"><span data-stu-id="50343-121">\[in\] See the **Remarks** section for information about this parameter.</span></span><br/>                                        |



 

## <a name="remarks"></a><span data-ttu-id="50343-122">備註</span><span class="sxs-lookup"><span data-stu-id="50343-122">Remarks</span></span>

<span data-ttu-id="50343-123">來源資料可能來自于緩衝區以外的任何資源類型。</span><span class="sxs-lookup"><span data-stu-id="50343-123">The source data may come from any Resource Type, other than Buffers.</span></span> <span data-ttu-id="50343-124">額外的偏差會套用至在指令執行過程中計算的詳細資料層級。</span><span class="sxs-lookup"><span data-stu-id="50343-124">An additional bias is applied to the level of detail computed as part of the instruction execution.</span></span>

<span data-ttu-id="50343-125">此指令的行為就像是 [範例](sample--sm4---asm-.md) 指令，其中新增了將指定的 *srcLODBias* 值套用至在選取 mip map (s) 之前，在指示執行過程中計算的詳細資料值層級。</span><span class="sxs-lookup"><span data-stu-id="50343-125">This instruction behaves like the [sample](sample--sm4---asm-.md) instruction with the addition of applying the specified *srcLODBias* value to the level of detail value computed as part of the instruction execution prior to selecting the mip map(s).</span></span> <span data-ttu-id="50343-126">*SrcLODBias* 值會以每圖元為單位新增至計算的」 lod，以及在要 MinLOD 和 MaxLOD 的夾具之前的取樣器 MipLODBias 值。</span><span class="sxs-lookup"><span data-stu-id="50343-126">The *srcLODBias* value is added to the computed LOD on a per-pixel basis, along with the sampler MipLODBias value, prior to the clamp to MinLOD and MaxLOD.</span></span>

### <a name="restrictions"></a><span data-ttu-id="50343-127">限制</span><span class="sxs-lookup"><span data-stu-id="50343-127">Restrictions</span></span>

-   <span data-ttu-id="50343-128">**範例 \_ b** 會繼承與 [範例](sample--sm4---asm-.md) 指令相同的限制，再加上其他參數的其他限制。</span><span class="sxs-lookup"><span data-stu-id="50343-128">**sample\_b** inherits the same restrictions as the [sample](sample--sm4---asm-.md) instruction, plus additional restrictions for its additional parameter.</span></span>
-   <span data-ttu-id="50343-129">*SrcLODBias* 範圍是 (-16.0 f 到 15.99 f) ;此範圍外的值會產生未定義的結果。</span><span class="sxs-lookup"><span data-stu-id="50343-129">The range of *srcLODBias* is (-16.0f to 15.99f); values outside of this range will produce undefined results.</span></span>
-   <span data-ttu-id="50343-130">如果 *srcLODBias* 不是純量立即的，則必須使用單一元件選取器。</span><span class="sxs-lookup"><span data-stu-id="50343-130">*srcLODBias* must use a single component selector if it is not a scalar immediate.</span></span>

<span data-ttu-id="50343-131">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="50343-131">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="50343-132">頂點著色器</span><span class="sxs-lookup"><span data-stu-id="50343-132">Vertex Shader</span></span> | <span data-ttu-id="50343-133">幾何著色器</span><span class="sxs-lookup"><span data-stu-id="50343-133">Geometry Shader</span></span> | <span data-ttu-id="50343-134">像素著色器</span><span class="sxs-lookup"><span data-stu-id="50343-134">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
|               |                 | <span data-ttu-id="50343-135">x</span><span class="sxs-lookup"><span data-stu-id="50343-135">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="50343-136">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="50343-136">Minimum Shader Model</span></span>

<span data-ttu-id="50343-137">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="50343-137">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="50343-138">著色器模型</span><span class="sxs-lookup"><span data-stu-id="50343-138">Shader Model</span></span>                                              | <span data-ttu-id="50343-139">支援</span><span class="sxs-lookup"><span data-stu-id="50343-139">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="50343-140">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="50343-140">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="50343-141">是</span><span class="sxs-lookup"><span data-stu-id="50343-141">yes</span></span>       |
| [<span data-ttu-id="50343-142">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="50343-142">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="50343-143">是</span><span class="sxs-lookup"><span data-stu-id="50343-143">yes</span></span>       |
| [<span data-ttu-id="50343-144">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="50343-144">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="50343-145">是</span><span class="sxs-lookup"><span data-stu-id="50343-145">yes</span></span>       |
| [<span data-ttu-id="50343-146">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="50343-146">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="50343-147">不可以</span><span class="sxs-lookup"><span data-stu-id="50343-147">no</span></span>        |
| [<span data-ttu-id="50343-148">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="50343-148">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="50343-149">不可以</span><span class="sxs-lookup"><span data-stu-id="50343-149">no</span></span>        |
| [<span data-ttu-id="50343-150">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="50343-150">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="50343-151">不可以</span><span class="sxs-lookup"><span data-stu-id="50343-151">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="50343-152">相關主題</span><span class="sxs-lookup"><span data-stu-id="50343-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="50343-153">著色器模型4元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="50343-153">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





