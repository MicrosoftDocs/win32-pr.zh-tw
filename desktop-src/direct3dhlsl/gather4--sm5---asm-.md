---
title: 'gather4 (sm5-asm) '
description: '收集在雙線性篩選作業中使用的四個材質，並將其封裝成單一登入。 |gather4 (sm5-asm) '
ms.assetid: 5F93BB70-7696-48E4-BCD3-91D5D42FF63E
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5657265738f12331afc7596286f02170de2a635
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104195950"
---
# <a name="gather4-sm5---asm"></a><span data-ttu-id="c7bb3-104">gather4 (sm5-asm) </span><span class="sxs-lookup"><span data-stu-id="c7bb3-104">gather4 (sm5 - asm)</span></span>

<span data-ttu-id="c7bb3-105">收集在雙線性篩選作業中使用的四個材質，並將其封裝成單一登入。</span><span class="sxs-lookup"><span data-stu-id="c7bb3-105">Gathers the four texels that would be used in a bi-linear filtering operation and packs them into a single register.</span></span> <span data-ttu-id="c7bb3-106">此指示只適用于2D 或立方體貼圖材質，包括陣列。</span><span class="sxs-lookup"><span data-stu-id="c7bb3-106">This instruction only works with 2D or CubeMap textures, including arrays.</span></span> <span data-ttu-id="c7bb3-107">只會使用取樣器的定址模式，並使用任何 mip 金字塔的最上層。</span><span class="sxs-lookup"><span data-stu-id="c7bb3-107">Only the addressing modes of the sampler are used and the top level of any mip pyramid is used.</span></span>



| <span data-ttu-id="c7bb3-108">gather4 \[ \_ aoffimmi (u、v) \] dest \[ \] 、srcAddress \[ . swizzle \] 、srcResource \[ . swizzle \] 、srcSampler \[ . select \_ component\]</span><span class="sxs-lookup"><span data-stu-id="c7bb3-108">gather4\[\_aoffimmi(u,v)\] dest\[.mask\], srcAddress\[.swizzle\], srcResource\[.swizzle\], srcSampler\[.select\_component\]</span></span> |
|-----------------------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="c7bb3-109">項目</span><span class="sxs-lookup"><span data-stu-id="c7bb3-109">Item</span></span>                                                                                                               | <span data-ttu-id="c7bb3-110">描述</span><span class="sxs-lookup"><span data-stu-id="c7bb3-110">Description</span></span>                                                    |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="c7bb3-111"><span id="dest"></span><span id="DEST"></span>*目標*</span><span class="sxs-lookup"><span data-stu-id="c7bb3-111"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                    | <span data-ttu-id="c7bb3-112">\[在 \] 操作結果的位址中。</span><span class="sxs-lookup"><span data-stu-id="c7bb3-112">\[in\] The address of the results of the operation.</span></span><br/> |
| <span data-ttu-id="c7bb3-113"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span><span class="sxs-lookup"><span data-stu-id="c7bb3-113"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span></span><br/>     | <span data-ttu-id="c7bb3-114">\[在 \] 一組材質座標中。</span><span class="sxs-lookup"><span data-stu-id="c7bb3-114">\[in\] A set of texture coordinates.</span></span><br/>                |
| <span data-ttu-id="c7bb3-115"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span><span class="sxs-lookup"><span data-stu-id="c7bb3-115"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/> | <span data-ttu-id="c7bb3-116">\[在材質暫存器中 \] 。</span><span class="sxs-lookup"><span data-stu-id="c7bb3-116">\[in\] A texture register.</span></span><br/>                          |
| <span data-ttu-id="c7bb3-117"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span><span class="sxs-lookup"><span data-stu-id="c7bb3-117"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span></span><br/>     | <span data-ttu-id="c7bb3-118">\[在 \] 取樣器註冊中。</span><span class="sxs-lookup"><span data-stu-id="c7bb3-118">\[in\] A sampler register.</span></span><br/>                          |



 

## <a name="remarks"></a><span data-ttu-id="c7bb3-119">備註</span><span class="sxs-lookup"><span data-stu-id="c7bb3-119">Remarks</span></span>

<span data-ttu-id="c7bb3-120">此指令的行為就像 [**範例**](sample--sm4---asm-.md) 指令，但不會產生已篩選的範例。</span><span class="sxs-lookup"><span data-stu-id="c7bb3-120">This instruction behaves like the [**sample**](sample--sm4---asm-.md) instruction, but a filtered sample is not generated.</span></span> <span data-ttu-id="c7bb3-121">這四個會造成篩選的範例會以順時針順序的方式放入 xyzw 中，從取樣到查詢位置的左下方開始。</span><span class="sxs-lookup"><span data-stu-id="c7bb3-121">The four samples that would contribute to filtering are placed into xyzw in counter clockwise order starting with the sample to the lower left of the queried location.</span></span> <span data-ttu-id="c7bb3-122">這與 (u、v) 材質座標差異于下列位置的點取樣相同： (-、+) 、 (+、+) 、 (+、-) 、 (-,-) ，其中差異的大小一律為材質。</span><span class="sxs-lookup"><span data-stu-id="c7bb3-122">This is the same as point sampling with (u,v) texture coordinate deltas at the following locations: (-,+),(+,+),(+,-),(-,-), where the magnitude of the deltas are always half a texel.</span></span>

<span data-ttu-id="c7bb3-123">針對立方體貼圖材質，當雙線性使用量橫跨邊緣時，就會使用來自相鄰臉部的材質。</span><span class="sxs-lookup"><span data-stu-id="c7bb3-123">For CubeMap textures, when a bi-linear footprint spans an edge, texels from the neighboring face are used.</span></span> <span data-ttu-id="c7bb3-124">角落使用與 [**範例**](sample--sm4---asm-.md) 指令相同的規則;也就是說，未知的邊角會被視為三個 impinging 臉部角落的平均值。</span><span class="sxs-lookup"><span data-stu-id="c7bb3-124">Corners use the same rules as the [**sample**](sample--sm4---asm-.md) instruction; that is, the unknown corner is considered the average of the three impinging face corners.</span></span>

<span data-ttu-id="c7bb3-125">有適用于 **gather4** 的材質格式限制（以格式清單表示）。</span><span class="sxs-lookup"><span data-stu-id="c7bb3-125">There are texture format restrictions that apply to **gather4** which are expressed in the format list.</span></span>

<span data-ttu-id="c7bb3-126">*SrcResource* 上的 swizzle 允許在將傳回的值寫入目的地之前，任意加以 swizzled。</span><span class="sxs-lookup"><span data-stu-id="c7bb3-126">The swizzle on *srcResource* allows the returned values to be swizzled arbitrarily before they are written to the destination.</span></span>

<span data-ttu-id="c7bb3-127">[ \_ *SrcSampler* 上的元件] 會選擇來源材質的哪個元件 (r/g/b/a) 讀取4個材質。</span><span class="sxs-lookup"><span data-stu-id="c7bb3-127">The .select\_component on *srcSampler* chooses which component of the source texture (r/g/b/a) to read 4 texels from.</span></span>

<span data-ttu-id="c7bb3-128">針對具有 float32 元件的格式，如果要提取的值是正規化、反正規化、+-0 或 +-INF，則會傳回未改變的著色器。</span><span class="sxs-lookup"><span data-stu-id="c7bb3-128">For formats with float32 components, if the value being fetched is normalized, denormalized, +-0 or +-INF, it is returned to the shader unaltered.</span></span> <span data-ttu-id="c7bb3-129">NaN 會以 NaN 傳回，但是 NaN 的精確位標記法可能會變更。</span><span class="sxs-lookup"><span data-stu-id="c7bb3-129">NaN is returned as NaN, but the exact bit representation of the NaN may be changed.</span></span> <span data-ttu-id="c7bb3-130">針對 TextureCubes，遺漏的第四個材質的部分合成必須在角落進行，因此不會套用合成材質未變更的位，而且可以清除 denorms。</span><span class="sxs-lookup"><span data-stu-id="c7bb3-130">For TextureCubes, some synthesis of the missing 4th texel must occur at corners, so returning bits unchanged for the synthesized texel does not apply, and denorms could be flushed.</span></span>

<span data-ttu-id="c7bb3-131">針對硬體的執行，以傳統雙線性篩選進行優化，可直接在材質上偵測樣本，並略過讀取可能具有權數0的材質。</span><span class="sxs-lookup"><span data-stu-id="c7bb3-131">For hardware implementations, optimizations in traditional bilinear filtering that detect samples directly on texels and skip reading of texels that would have weight 0 cannot be leveraged with this instruction.</span></span> <span data-ttu-id="c7bb3-132">*gather4* 一律會傳回所有要求的材質。</span><span class="sxs-lookup"><span data-stu-id="c7bb3-132">*gather4* always returns all requested texels.</span></span>

<span data-ttu-id="c7bb3-133">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="c7bb3-133">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="c7bb3-134">頂點</span><span class="sxs-lookup"><span data-stu-id="c7bb3-134">Vertex</span></span> | <span data-ttu-id="c7bb3-135">船體</span><span class="sxs-lookup"><span data-stu-id="c7bb3-135">Hull</span></span> | <span data-ttu-id="c7bb3-136">網域</span><span class="sxs-lookup"><span data-stu-id="c7bb3-136">Domain</span></span> | <span data-ttu-id="c7bb3-137">幾何</span><span class="sxs-lookup"><span data-stu-id="c7bb3-137">Geometry</span></span> | <span data-ttu-id="c7bb3-138">像素</span><span class="sxs-lookup"><span data-stu-id="c7bb3-138">Pixel</span></span> | <span data-ttu-id="c7bb3-139">計算</span><span class="sxs-lookup"><span data-stu-id="c7bb3-139">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="c7bb3-140">X</span><span class="sxs-lookup"><span data-stu-id="c7bb3-140">X</span></span>      | <span data-ttu-id="c7bb3-141">X</span><span class="sxs-lookup"><span data-stu-id="c7bb3-141">X</span></span>    | <span data-ttu-id="c7bb3-142">X</span><span class="sxs-lookup"><span data-stu-id="c7bb3-142">X</span></span>      | <span data-ttu-id="c7bb3-143">X</span><span class="sxs-lookup"><span data-stu-id="c7bb3-143">X</span></span>        | <span data-ttu-id="c7bb3-144">X</span><span class="sxs-lookup"><span data-stu-id="c7bb3-144">X</span></span>     | <span data-ttu-id="c7bb3-145">X</span><span class="sxs-lookup"><span data-stu-id="c7bb3-145">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="c7bb3-146">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="c7bb3-146">Minimum Shader Model</span></span>

<span data-ttu-id="c7bb3-147">下列著色器模型支援此指令：</span><span class="sxs-lookup"><span data-stu-id="c7bb3-147">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="c7bb3-148">著色器模型</span><span class="sxs-lookup"><span data-stu-id="c7bb3-148">Shader Model</span></span>                                              | <span data-ttu-id="c7bb3-149">支援</span><span class="sxs-lookup"><span data-stu-id="c7bb3-149">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="c7bb3-150">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="c7bb3-150">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="c7bb3-151">是</span><span class="sxs-lookup"><span data-stu-id="c7bb3-151">yes</span></span>       |
| [<span data-ttu-id="c7bb3-152">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="c7bb3-152">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="c7bb3-153">不可以</span><span class="sxs-lookup"><span data-stu-id="c7bb3-153">no</span></span>        |
| [<span data-ttu-id="c7bb3-154">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="c7bb3-154">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="c7bb3-155">不可以</span><span class="sxs-lookup"><span data-stu-id="c7bb3-155">no</span></span>        |
| [<span data-ttu-id="c7bb3-156">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="c7bb3-156">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="c7bb3-157">不可以</span><span class="sxs-lookup"><span data-stu-id="c7bb3-157">no</span></span>        |
| [<span data-ttu-id="c7bb3-158">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="c7bb3-158">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="c7bb3-159">不可以</span><span class="sxs-lookup"><span data-stu-id="c7bb3-159">no</span></span>        |
| [<span data-ttu-id="c7bb3-160">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="c7bb3-160">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="c7bb3-161">不可以</span><span class="sxs-lookup"><span data-stu-id="c7bb3-161">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="c7bb3-162">相關主題</span><span class="sxs-lookup"><span data-stu-id="c7bb3-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c7bb3-163">著色器模型5元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="c7bb3-163">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





