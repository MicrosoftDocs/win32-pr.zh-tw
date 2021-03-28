---
title: 'gather4 (sm 4.1-asm) '
description: '收集在雙線性篩選作業中使用的四個材質，並將其封裝成單一登入。 |gather4 (sm 4.1-asm) '
ms.assetid: 219B25AE-CBF9-4B68-B2DB-6D8C3C5B4CEA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84387bfe027e30b338b4701ec941a9d4e1b5e242
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104974152"
---
# <a name="gather4-sm41---asm"></a><span data-ttu-id="67197-104">gather4 (sm 4.1-asm) </span><span class="sxs-lookup"><span data-stu-id="67197-104">gather4 (sm4.1 - asm)</span></span>

<span data-ttu-id="67197-105">收集在雙線性篩選作業中使用的四個材質，並將其封裝成單一登入。</span><span class="sxs-lookup"><span data-stu-id="67197-105">Gathers the four texels that would be used in a bi-linear filtering operation and packs them into a single register.</span></span>



| <span data-ttu-id="67197-106">gather4 \[ \_ aoffimmi (u、v) \] dest \[ \] 、srcAddress \[ . swizzle \] 、srcResource \[ . swizzle \] srcSampler. r</span><span class="sxs-lookup"><span data-stu-id="67197-106">gather4\[\_aoffimmi(u,v)\] dest\[.mask\], srcAddress\[.swizzle\], srcResource\[.swizzle\] srcSampler.r</span></span> |
|--------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="67197-107">項目</span><span class="sxs-lookup"><span data-stu-id="67197-107">Item</span></span>                                                                                                               | <span data-ttu-id="67197-108">描述</span><span class="sxs-lookup"><span data-stu-id="67197-108">Description</span></span>                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67197-109"><span id="dest"></span><span id="DEST"></span>*目標*</span><span class="sxs-lookup"><span data-stu-id="67197-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                    | <span data-ttu-id="67197-110">\[在 \] 操作結果的位址中。</span><span class="sxs-lookup"><span data-stu-id="67197-110">\[in\] The address of the result of the operation.</span></span><br/>                                                                                                       |
| <span data-ttu-id="67197-111"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span><span class="sxs-lookup"><span data-stu-id="67197-111"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span></span><br/>     | <span data-ttu-id="67197-112">\[中 \] 的包含材質座標。</span><span class="sxs-lookup"><span data-stu-id="67197-112">\[in\] Contains the texture coordinates.</span></span> <br/>                                                                                                                |
| <span data-ttu-id="67197-113"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span><span class="sxs-lookup"><span data-stu-id="67197-113"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/> | <span data-ttu-id="67197-114">\[在資源暫存器中 \] 。</span><span class="sxs-lookup"><span data-stu-id="67197-114">\[in\] A resource register.</span></span> <br/> <span data-ttu-id="67197-115">Swizzle 可讓傳回的值在寫入至 *目的地* 之前，任意地 swizzled。</span><span class="sxs-lookup"><span data-stu-id="67197-115">The swizzle allows the returned values to be swizzled arbitrarily before they are written to *dest*.</span></span> <br/>            |
| <span data-ttu-id="67197-116"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span><span class="sxs-lookup"><span data-stu-id="67197-116"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span></span><br/>     | <span data-ttu-id="67197-117">\[在 \] 取樣器註冊中。</span><span class="sxs-lookup"><span data-stu-id="67197-117">\[in\] A sampler register.</span></span><br/> <span data-ttu-id="67197-118">此參數的 (red) swizzle，表示 R 通道的值已複製到 *目的地*。</span><span class="sxs-lookup"><span data-stu-id="67197-118">This parameter must have a .r (red) swizzle, which indicates that the value of the R channel is copied to *dest*.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="67197-119">備註</span><span class="sxs-lookup"><span data-stu-id="67197-119">Remarks</span></span>

<span data-ttu-id="67197-120">此作業僅適用于單一通道2D 或立方體貼圖材質。</span><span class="sxs-lookup"><span data-stu-id="67197-120">This operation only works with single channel 2D or CubeMap textures.</span></span> <span data-ttu-id="67197-121">若是2D 紋理，則會使用取樣器的定址模式，並使用任何 mip 金字塔的最上層。</span><span class="sxs-lookup"><span data-stu-id="67197-121">For 2D textures only the addressing modes of the sampler are used and the top level of any mip pyramid is used.</span></span>

<span data-ttu-id="67197-122">此指令的行為就像 [範例](sample--sm4---asm-.md) 指令，但不會產生已篩選的範例。</span><span class="sxs-lookup"><span data-stu-id="67197-122">This instruction behaves like the [sample](sample--sm4---asm-.md) instruction, but a filtered sample is not generated.</span></span> <span data-ttu-id="67197-123">這四個會造成篩選的範例會以順時針順序的方式放入 xyzw 中，從取樣到查詢位置的左下方開始。</span><span class="sxs-lookup"><span data-stu-id="67197-123">The four samples that would contribute to filtering are placed into xyzw in counter clockwise order starting with the sample to the lower left of the queried location.</span></span> <span data-ttu-id="67197-124">這與 (u、v) 材質座標差異于下列位置的點取樣相同： (-、+) 、 (+、+) 、 (+、-) 、 (-,-) ，其中差異的大小一律為材質。</span><span class="sxs-lookup"><span data-stu-id="67197-124">This is the same as point sampling with (u,v) texture coordinate deltas at the following locations: (-,+),(+,+),(+,-),(-,-), where the magnitude of the deltas are always half a texel.</span></span>

<span data-ttu-id="67197-125">當雙線性使用量橫跨鄰近臉部的邊緣材質時，適用于立方體貼圖紋理。</span><span class="sxs-lookup"><span data-stu-id="67197-125">For CubeMap textures when a bi-linear footprint spans an edge texels from the neighboring face are used.</span></span> <span data-ttu-id="67197-126">角落使用與 **範例** 指令相同的規則;這是未知的邊角會被視為三個 impinging 臉部角落的平均值。</span><span class="sxs-lookup"><span data-stu-id="67197-126">Corners use the same rules as the **sample** instruction; that is the unkown corner is considered the average of the three impinging face corners.</span></span>

<span data-ttu-id="67197-127">適用于 **範例** 指令的材質格式限制也適用于 **gather4** 指令。</span><span class="sxs-lookup"><span data-stu-id="67197-127">The texture format restrictions that apply to the **sample** instructions also apply to the **gather4** instruction.</span></span>

<span data-ttu-id="67197-128">針對硬體的執行，在傳統雙線性篩選中進行優化，可直接在材質上偵測樣本，並略過讀取具有權數0的材質無法與 **gather4** 搭配使用。</span><span class="sxs-lookup"><span data-stu-id="67197-128">For hardware implementations, optimizations in traditional bilinear filtering that detect samples directly on texels and skip reading of texels that would have weight 0 cannot be leveraged with **gather4**.</span></span> <span data-ttu-id="67197-129">**gather4** 一律會傳回所有要求的材質。</span><span class="sxs-lookup"><span data-stu-id="67197-129">**gather4** always returns all requested texels.</span></span>

<span data-ttu-id="67197-130">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="67197-130">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="67197-131">頂點著色器</span><span class="sxs-lookup"><span data-stu-id="67197-131">Vertex Shader</span></span> | <span data-ttu-id="67197-132">幾何著色器</span><span class="sxs-lookup"><span data-stu-id="67197-132">Geometry Shader</span></span> | <span data-ttu-id="67197-133">像素著色器</span><span class="sxs-lookup"><span data-stu-id="67197-133">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="67197-134">x</span><span class="sxs-lookup"><span data-stu-id="67197-134">x</span></span>             | <span data-ttu-id="67197-135">x</span><span class="sxs-lookup"><span data-stu-id="67197-135">x</span></span>               | <span data-ttu-id="67197-136">x</span><span class="sxs-lookup"><span data-stu-id="67197-136">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="67197-137">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="67197-137">Minimum Shader Model</span></span>

<span data-ttu-id="67197-138">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="67197-138">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="67197-139">著色器模型</span><span class="sxs-lookup"><span data-stu-id="67197-139">Shader Model</span></span>                                              | <span data-ttu-id="67197-140">支援</span><span class="sxs-lookup"><span data-stu-id="67197-140">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="67197-141">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="67197-141">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="67197-142">是</span><span class="sxs-lookup"><span data-stu-id="67197-142">yes</span></span>       |
| [<span data-ttu-id="67197-143">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="67197-143">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="67197-144">是</span><span class="sxs-lookup"><span data-stu-id="67197-144">yes</span></span>       |
| [<span data-ttu-id="67197-145">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="67197-145">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="67197-146">不可以</span><span class="sxs-lookup"><span data-stu-id="67197-146">no</span></span>        |
| [<span data-ttu-id="67197-147">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="67197-147">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="67197-148">不可以</span><span class="sxs-lookup"><span data-stu-id="67197-148">no</span></span>        |
| [<span data-ttu-id="67197-149">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="67197-149">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="67197-150">不可以</span><span class="sxs-lookup"><span data-stu-id="67197-150">no</span></span>        |
| [<span data-ttu-id="67197-151">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="67197-151">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="67197-152">不可以</span><span class="sxs-lookup"><span data-stu-id="67197-152">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="67197-153">相關主題</span><span class="sxs-lookup"><span data-stu-id="67197-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="67197-154">著色器模型4元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="67197-154">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





