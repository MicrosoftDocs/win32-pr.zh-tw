---
title: 'samplepos (sm 4.1-asm) '
description: 查詢指定之著色器資源檢視或轉譯器中範例的位置。
ms.assetid: 5A53B342-3A1D-4016-ABF2-CA6236D562C9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 910a542dafddb8b855e218f8702c746220780d6e
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104373886"
---
# <a name="samplepos-sm41---asm"></a><span data-ttu-id="e1d22-103">samplepos (sm 4.1-asm) </span><span class="sxs-lookup"><span data-stu-id="e1d22-103">samplepos (sm4.1 - asm)</span></span>

<span data-ttu-id="e1d22-104">查詢指定之著色器資源檢視或轉譯器中範例的位置。</span><span class="sxs-lookup"><span data-stu-id="e1d22-104">Queries the position of a sample in a given shader resource view or in the rasterizer.</span></span>



| <span data-ttu-id="e1d22-105">samplepos dest \[ . mask \] ，srcResource \[ . swizzle \] ，sampleIndex (純量運算元) </span><span class="sxs-lookup"><span data-stu-id="e1d22-105">samplepos dest\[.mask\], srcResource\[.swizzle\], sampleIndex (scalar operand)</span></span> |
|--------------------------------------------------------------------------------|



 



| <span data-ttu-id="e1d22-106">項目</span><span class="sxs-lookup"><span data-stu-id="e1d22-106">Item</span></span>                                                                                                               | <span data-ttu-id="e1d22-107">描述</span><span class="sxs-lookup"><span data-stu-id="e1d22-107">Description</span></span>                                                    |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="e1d22-108"><span id="dest"></span><span id="DEST"></span>*目標*</span><span class="sxs-lookup"><span data-stu-id="e1d22-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                    | <span data-ttu-id="e1d22-109">\[在 \] 操作結果的位址中。</span><span class="sxs-lookup"><span data-stu-id="e1d22-109">\[in\] The address of the results of the operation.</span></span><br/> |
| <span data-ttu-id="e1d22-110"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span><span class="sxs-lookup"><span data-stu-id="e1d22-110"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/> | <span data-ttu-id="e1d22-111">\[在 \] 著色器資源中。</span><span class="sxs-lookup"><span data-stu-id="e1d22-111">\[in\] The shader resource.</span></span><br/>                         |
| <span data-ttu-id="e1d22-112"><span id="sampleIndex"></span><span id="sampleindex"></span><span id="SAMPLEINDEX"></span>*sampleIndex*</span><span class="sxs-lookup"><span data-stu-id="e1d22-112"><span id="sampleIndex"></span><span id="sampleindex"></span><span id="SAMPLEINDEX"></span>*sampleIndex*</span></span><br/> | <span data-ttu-id="e1d22-113">\[在 \] 範例的索引中。</span><span class="sxs-lookup"><span data-stu-id="e1d22-113">\[in\] The index of the sample.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="e1d22-114">備註</span><span class="sxs-lookup"><span data-stu-id="e1d22-114">Remarks</span></span>

<span data-ttu-id="e1d22-115">此指令會針對指定的資源傳回範例 *sampleIndex* 的2d 樣本位置。</span><span class="sxs-lookup"><span data-stu-id="e1d22-115">This instruction returns the 2D sample position of sample *sampleIndex* for the given resource.</span></span> <span data-ttu-id="e1d22-116">它只適用于可以使用 [**ld2dms**](ld2dms--sm4-1---asm-.md) 載入的資源，除非轉譯器已指定為 *srcResource*。</span><span class="sxs-lookup"><span data-stu-id="e1d22-116">It is valid only for resources that can be loaded using [**ld2dms**](ld2dms--sm4-1---asm-.md) unless the rasterizer is specified as *srcResource*.</span></span>

<span data-ttu-id="e1d22-117">*srcResource* 可以是 \# (著色器資源檢視) 或轉譯器註冊的 t 註冊。</span><span class="sxs-lookup"><span data-stu-id="e1d22-117">*srcResource* can be a t\# register (a shader resource view) or a rasterizer register.</span></span>

<span data-ttu-id="e1d22-118">指令會計算浮點數向量 (Xposition、Yposition、0、0) 。</span><span class="sxs-lookup"><span data-stu-id="e1d22-118">The instruction computes the floating point vector (Xposition, Yposition, 0, 0).</span></span>

<span data-ttu-id="e1d22-119">*SrcResource* 上的 swizzle 允許在將傳回的值寫入目的地之前，任意加以 swizzled。</span><span class="sxs-lookup"><span data-stu-id="e1d22-119">The swizzle on *srcResource* allows the returned values to be swizzled arbitrarily before they are written to the destination.</span></span> <span data-ttu-id="e1d22-120">樣本位置是相對於圖元的中心（以圖元座標系統為基礎）。</span><span class="sxs-lookup"><span data-stu-id="e1d22-120">The sample position is relative to the pixel's center, based on the Pixel Coordinate System.</span></span>

<span data-ttu-id="e1d22-121">如果 *sampleIndex* 超出範圍，則會傳回零向量。</span><span class="sxs-lookup"><span data-stu-id="e1d22-121">If *sampleIndex* is out of bounds a zero vector is returned.</span></span> <span data-ttu-id="e1d22-122">如果沒有任何資源系結至指定的位置，則會傳回0。</span><span class="sxs-lookup"><span data-stu-id="e1d22-122">If there is no resource bound to the specified slot, 0 is returned.</span></span>

<span data-ttu-id="e1d22-123">**samplepos** 可用於自訂程式碼中所解析的自訂專案。</span><span class="sxs-lookup"><span data-stu-id="e1d22-123">**samplepos** can be used for things like custom resolves in shader code.</span></span>

<span data-ttu-id="e1d22-124">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="e1d22-124">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="e1d22-125">頂點著色器</span><span class="sxs-lookup"><span data-stu-id="e1d22-125">Vertex Shader</span></span> | <span data-ttu-id="e1d22-126">幾何著色器</span><span class="sxs-lookup"><span data-stu-id="e1d22-126">Geometry Shader</span></span> | <span data-ttu-id="e1d22-127">像素著色器</span><span class="sxs-lookup"><span data-stu-id="e1d22-127">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
|               |                 | <span data-ttu-id="e1d22-128">x</span><span class="sxs-lookup"><span data-stu-id="e1d22-128">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="e1d22-129">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="e1d22-129">Minimum Shader Model</span></span>

<span data-ttu-id="e1d22-130">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="e1d22-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="e1d22-131">著色器模型</span><span class="sxs-lookup"><span data-stu-id="e1d22-131">Shader Model</span></span>                                              | <span data-ttu-id="e1d22-132">支援</span><span class="sxs-lookup"><span data-stu-id="e1d22-132">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="e1d22-133">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="e1d22-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="e1d22-134">是</span><span class="sxs-lookup"><span data-stu-id="e1d22-134">yes</span></span>       |
| [<span data-ttu-id="e1d22-135">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="e1d22-135">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="e1d22-136">是</span><span class="sxs-lookup"><span data-stu-id="e1d22-136">yes</span></span>       |
| [<span data-ttu-id="e1d22-137">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="e1d22-137">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="e1d22-138">不可以</span><span class="sxs-lookup"><span data-stu-id="e1d22-138">no</span></span>        |
| [<span data-ttu-id="e1d22-139">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="e1d22-139">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="e1d22-140">不可以</span><span class="sxs-lookup"><span data-stu-id="e1d22-140">no</span></span>        |
| [<span data-ttu-id="e1d22-141">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="e1d22-141">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="e1d22-142">不可以</span><span class="sxs-lookup"><span data-stu-id="e1d22-142">no</span></span>        |
| [<span data-ttu-id="e1d22-143">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="e1d22-143">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="e1d22-144">不可以</span><span class="sxs-lookup"><span data-stu-id="e1d22-144">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="e1d22-145">相關主題</span><span class="sxs-lookup"><span data-stu-id="e1d22-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e1d22-146">著色器模型4元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="e1d22-146">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





