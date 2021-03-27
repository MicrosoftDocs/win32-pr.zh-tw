---
title: '」 lod (sm 4.1-asm) '
description: 傳回用於材質篩選 (」 LOD) 的詳細層級。
ms.assetid: A5931203-8CD7-4FC9-A4A4-CA981F38C7A3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a1c1ca5a22a735945b76a60c175c665c5cf58fb
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "103679140"
---
# <a name="lod-sm41---asm"></a><span data-ttu-id="955ca-103">」 lod (sm 4.1-asm) </span><span class="sxs-lookup"><span data-stu-id="955ca-103">lod (sm4.1 - asm)</span></span>

<span data-ttu-id="955ca-104">傳回用於材質篩選 (」 LOD) 的詳細層級。</span><span class="sxs-lookup"><span data-stu-id="955ca-104">Returns the level of detail (LOD) that would be used for texture filtering.</span></span>



| <span data-ttu-id="955ca-105">」 lod dest \[ . mask \] 、srcAddress \[ . swizzle \] 、srcResource \[ . swizzle \] 、srcSampler</span><span class="sxs-lookup"><span data-stu-id="955ca-105">lod dest\[.mask\], srcAddress\[.swizzle\], srcResource\[.swizzle\], srcSampler</span></span> |
|--------------------------------------------------------------------------------|



 



| <span data-ttu-id="955ca-106">項目</span><span class="sxs-lookup"><span data-stu-id="955ca-106">Item</span></span>                                                                                                               | <span data-ttu-id="955ca-107">描述</span><span class="sxs-lookup"><span data-stu-id="955ca-107">Description</span></span>                                     |
|--------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| <span data-ttu-id="955ca-108"><span id="dest"></span><span id="DEST"></span>*目標*</span><span class="sxs-lookup"><span data-stu-id="955ca-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                    | <span data-ttu-id="955ca-109">\[在 \] 結果的位址中。</span><span class="sxs-lookup"><span data-stu-id="955ca-109">\[in\] The address of the results.</span></span><br/>   |
| <span data-ttu-id="955ca-110"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span><span class="sxs-lookup"><span data-stu-id="955ca-110"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span></span><br/>     | <span data-ttu-id="955ca-111">\[在 \] 一組材質座標中。</span><span class="sxs-lookup"><span data-stu-id="955ca-111">\[in\] A set of texture coordinates.</span></span><br/> |
| <span data-ttu-id="955ca-112"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span><span class="sxs-lookup"><span data-stu-id="955ca-112"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/> | <span data-ttu-id="955ca-113">\[在材質暫存器中 \] 。</span><span class="sxs-lookup"><span data-stu-id="955ca-113">\[in\] A texture register.</span></span><br/>           |
| <span data-ttu-id="955ca-114"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span><span class="sxs-lookup"><span data-stu-id="955ca-114"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span></span><br/>     | <span data-ttu-id="955ca-115">\[在 \] 取樣器註冊中。</span><span class="sxs-lookup"><span data-stu-id="955ca-115">\[in\] A sampler register.</span></span><br/>           |



 

## <a name="remarks"></a><span data-ttu-id="955ca-116">備註</span><span class="sxs-lookup"><span data-stu-id="955ca-116">Remarks</span></span>

<span data-ttu-id="955ca-117">這種行為類似 [範例](sample--sm4---asm-.md) 指令，但不會產生已篩選的範例。</span><span class="sxs-lookup"><span data-stu-id="955ca-117">This behaves like the [sample](sample--sm4---asm-.md) instruction, but a filtered sample is not generated.</span></span> <span data-ttu-id="955ca-118">指令會計算下列向量 (ClampedLOD、NonClampedLOD、0、0) 。</span><span class="sxs-lookup"><span data-stu-id="955ca-118">The instruction computes the following vector (ClampedLOD, NonClampedLOD, 0, 0).</span></span> <span data-ttu-id="955ca-119">NonClampedLOD 是一種計算的」 LOD 值，會忽略取樣器或材質 (的任何固定，也就是它可以傳回負值。 ) ClampedLOD 是計算的」 LOD 值，會由實際的 **範例** 指令使用。</span><span class="sxs-lookup"><span data-stu-id="955ca-119">NonClampedLOD is a computed LOD value that ignores any clamping from either the sampler or the texture (ie: it can return negative values.) ClampedLOD is a computed LOD value that would be used by the actual **sample** instruction.</span></span> <span data-ttu-id="955ca-120">*SrcResource* 上的 swizzle 允許在將傳回的值寫入目的地之前，任意加以 swizzled。</span><span class="sxs-lookup"><span data-stu-id="955ca-120">The swizzle on *srcResource* allows the returned values to be swizzled arbitrarily before they are written to the destination.</span></span>

<span data-ttu-id="955ca-121">如果沒有任何資源系結至指定的位置，則會傳回0。</span><span class="sxs-lookup"><span data-stu-id="955ca-121">If there is no resource bound to the specified slot, 0 is returned.</span></span>

<span data-ttu-id="955ca-122">如果取樣器使用非等向性篩選，則」 LOD 應該根據橢圓磁片使用量的較小軸，對應至小數 mip 層級。</span><span class="sxs-lookup"><span data-stu-id="955ca-122">If the sampler is using anisotropic filtering the LOD should correspond to the fractional mip level based on the smaller axis of the elliptical footprint.</span></span>

<span data-ttu-id="955ca-123">這適用于下列材質類型： Texture1D、Texture2D、Texture3D 和 TextureCube。</span><span class="sxs-lookup"><span data-stu-id="955ca-123">This is valid for the following texture types: Texture1D, Texture2D, Texture3D and TextureCube.</span></span>

<span data-ttu-id="955ca-124">搭配指定點 mip 篩選的取樣器（特別是 \_ 在 mip 點結束的任何 D3D10 篩選準則列舉）使用時，不會定義」 lod 指令 \_ 。</span><span class="sxs-lookup"><span data-stu-id="955ca-124">The **lod** instruction is not defined when used with a sampler that specifies point mip filtering, specifically, any D3D10\_FILTER enum that ends in MIP\_POINT.</span></span> <span data-ttu-id="955ca-125"> (其中一個範例是 D3D10 \_ FILTER \_ MIN \_ MAG \_ MIP \_ POINT. ) </span><span class="sxs-lookup"><span data-stu-id="955ca-125">(An example of this would be D3D10\_FILTER\_MIN\_MAG\_MIP\_POINT.)</span></span>

<span data-ttu-id="955ca-126">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="955ca-126">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="955ca-127">頂點著色器</span><span class="sxs-lookup"><span data-stu-id="955ca-127">Vertex Shader</span></span> | <span data-ttu-id="955ca-128">幾何著色器</span><span class="sxs-lookup"><span data-stu-id="955ca-128">Geometry Shader</span></span> | <span data-ttu-id="955ca-129">像素著色器</span><span class="sxs-lookup"><span data-stu-id="955ca-129">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
|               |                 | <span data-ttu-id="955ca-130">x</span><span class="sxs-lookup"><span data-stu-id="955ca-130">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="955ca-131">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="955ca-131">Minimum Shader Model</span></span>

<span data-ttu-id="955ca-132">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="955ca-132">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="955ca-133">著色器模型</span><span class="sxs-lookup"><span data-stu-id="955ca-133">Shader Model</span></span>                                              | <span data-ttu-id="955ca-134">支援</span><span class="sxs-lookup"><span data-stu-id="955ca-134">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="955ca-135">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="955ca-135">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="955ca-136">是</span><span class="sxs-lookup"><span data-stu-id="955ca-136">yes</span></span>       |
| [<span data-ttu-id="955ca-137">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="955ca-137">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="955ca-138">是</span><span class="sxs-lookup"><span data-stu-id="955ca-138">yes</span></span>       |
| [<span data-ttu-id="955ca-139">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="955ca-139">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="955ca-140">不可以</span><span class="sxs-lookup"><span data-stu-id="955ca-140">no</span></span>        |
| [<span data-ttu-id="955ca-141">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="955ca-141">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="955ca-142">不可以</span><span class="sxs-lookup"><span data-stu-id="955ca-142">no</span></span>        |
| [<span data-ttu-id="955ca-143">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="955ca-143">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="955ca-144">不可以</span><span class="sxs-lookup"><span data-stu-id="955ca-144">no</span></span>        |
| [<span data-ttu-id="955ca-145">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="955ca-145">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="955ca-146">不可以</span><span class="sxs-lookup"><span data-stu-id="955ca-146">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="955ca-147">相關主題</span><span class="sxs-lookup"><span data-stu-id="955ca-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="955ca-148">著色器模型4元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="955ca-148">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





