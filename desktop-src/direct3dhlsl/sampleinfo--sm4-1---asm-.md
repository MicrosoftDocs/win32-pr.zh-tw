---
title: 'sampleinfo (sm 4.1-asm) '
description: 查詢指定著色器資源檢視或轉譯器中的樣本數。
ms.assetid: 1F0968D7-01E9-4213-9F83-172B88374C3C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d307dbc8c79618a6401737874a9f6e060a899ccc
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "103841699"
---
# <a name="sampleinfo-sm41---asm"></a><span data-ttu-id="1fbf0-103">sampleinfo (sm 4.1-asm) </span><span class="sxs-lookup"><span data-stu-id="1fbf0-103">sampleinfo (sm4.1 - asm)</span></span>

<span data-ttu-id="1fbf0-104">查詢指定著色器資源檢視或轉譯器中的樣本數。</span><span class="sxs-lookup"><span data-stu-id="1fbf0-104">Queries the number of samples in a given shader resource view or in the rasterizer.</span></span>



| <span data-ttu-id="1fbf0-105">\[\_uint \] dest \[ . mask \] 、srcResource \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="1fbf0-105">\[\_uint\] dest\[.mask\], srcResource\[.swizzle\]</span></span> |
|---------------------------------------------------|



 



| <span data-ttu-id="1fbf0-106">項目</span><span class="sxs-lookup"><span data-stu-id="1fbf0-106">Item</span></span>                                                                                                               | <span data-ttu-id="1fbf0-107">描述</span><span class="sxs-lookup"><span data-stu-id="1fbf0-107">Description</span></span>                                                    |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="1fbf0-108"><span id="dest"></span><span id="DEST"></span>*目標*</span><span class="sxs-lookup"><span data-stu-id="1fbf0-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                    | <span data-ttu-id="1fbf0-109">\[在 \] 操作結果的位址中。</span><span class="sxs-lookup"><span data-stu-id="1fbf0-109">\[in\] The address of the results of the operation.</span></span><br/> |
| <span data-ttu-id="1fbf0-110"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span><span class="sxs-lookup"><span data-stu-id="1fbf0-110"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/> | <span data-ttu-id="1fbf0-111">\[在 \] 著色器資源中。</span><span class="sxs-lookup"><span data-stu-id="1fbf0-111">\[in\] The shader resource.</span></span><br/>                         |



 

## <a name="remarks"></a><span data-ttu-id="1fbf0-112">備註</span><span class="sxs-lookup"><span data-stu-id="1fbf0-112">Remarks</span></span>

<span data-ttu-id="1fbf0-113">此指令會傳回指定資源或轉譯器的樣本數。</span><span class="sxs-lookup"><span data-stu-id="1fbf0-113">This instruction returns the number of samples for the given resource or the rasterizer.</span></span> <span data-ttu-id="1fbf0-114">它只適用于可以使用 [**ld2dms**](ld2dms--sm4-1---asm-.md) 載入的資源，除非轉譯器已指定為 *srcResource*。</span><span class="sxs-lookup"><span data-stu-id="1fbf0-114">It is valid only for resources that can be loaded using [**ld2dms**](ld2dms--sm4-1---asm-.md) unless the rasterizer is specified as *srcResource*.</span></span> <span data-ttu-id="1fbf0-115">*srcResource* 可以是 \# (著色器資源檢視) 或轉譯器註冊的 t 註冊。</span><span class="sxs-lookup"><span data-stu-id="1fbf0-115">*srcResource* could be a t\# register (a shader resource view) or a rasterizer register.</span></span>

<span data-ttu-id="1fbf0-116">指令會計算向量 (SampleCount、0、0、0) 。</span><span class="sxs-lookup"><span data-stu-id="1fbf0-116">The instruction computes the vector (SampleCount,0,0,0).</span></span>

<span data-ttu-id="1fbf0-117">*SrcResource* 上的 swizzle 允許在將傳回的值寫入目的地之前，任意加以 swizzled。</span><span class="sxs-lookup"><span data-stu-id="1fbf0-117">The swizzle on *srcResource* allows the returned values to be swizzled arbitrarily before they are written to the destination.</span></span> <span data-ttu-id="1fbf0-118">除非使用 uint 修飾詞，否則傳回的值為浮點數， \_ 在這種情況下，傳回的值為整數。</span><span class="sxs-lookup"><span data-stu-id="1fbf0-118">The returned value is floating point, unless the \_uint modifier is used, in which case the returned value is integer.</span></span> <span data-ttu-id="1fbf0-119">如果沒有任何資源系結至指定的位置，則會傳回0。</span><span class="sxs-lookup"><span data-stu-id="1fbf0-119">If there is no resource bound to the specified slot, 0 is returned.</span></span>

<span data-ttu-id="1fbf0-120">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="1fbf0-120">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="1fbf0-121">頂點著色器</span><span class="sxs-lookup"><span data-stu-id="1fbf0-121">Vertex Shader</span></span> | <span data-ttu-id="1fbf0-122">幾何著色器</span><span class="sxs-lookup"><span data-stu-id="1fbf0-122">Geometry Shader</span></span> | <span data-ttu-id="1fbf0-123">像素著色器</span><span class="sxs-lookup"><span data-stu-id="1fbf0-123">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="1fbf0-124">X</span><span class="sxs-lookup"><span data-stu-id="1fbf0-124">X</span></span>             | <span data-ttu-id="1fbf0-125">X</span><span class="sxs-lookup"><span data-stu-id="1fbf0-125">X</span></span>               | <span data-ttu-id="1fbf0-126">x</span><span class="sxs-lookup"><span data-stu-id="1fbf0-126">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="1fbf0-127">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="1fbf0-127">Minimum Shader Model</span></span>

<span data-ttu-id="1fbf0-128">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="1fbf0-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="1fbf0-129">著色器模型</span><span class="sxs-lookup"><span data-stu-id="1fbf0-129">Shader Model</span></span>                                              | <span data-ttu-id="1fbf0-130">支援</span><span class="sxs-lookup"><span data-stu-id="1fbf0-130">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="1fbf0-131">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="1fbf0-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="1fbf0-132">是</span><span class="sxs-lookup"><span data-stu-id="1fbf0-132">yes</span></span>       |
| [<span data-ttu-id="1fbf0-133">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="1fbf0-133">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="1fbf0-134">是</span><span class="sxs-lookup"><span data-stu-id="1fbf0-134">yes</span></span>       |
| [<span data-ttu-id="1fbf0-135">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="1fbf0-135">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="1fbf0-136">不可以</span><span class="sxs-lookup"><span data-stu-id="1fbf0-136">no</span></span>        |
| [<span data-ttu-id="1fbf0-137">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="1fbf0-137">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="1fbf0-138">不可以</span><span class="sxs-lookup"><span data-stu-id="1fbf0-138">no</span></span>        |
| [<span data-ttu-id="1fbf0-139">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="1fbf0-139">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="1fbf0-140">不可以</span><span class="sxs-lookup"><span data-stu-id="1fbf0-140">no</span></span>        |
| [<span data-ttu-id="1fbf0-141">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="1fbf0-141">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="1fbf0-142">不可以</span><span class="sxs-lookup"><span data-stu-id="1fbf0-142">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="1fbf0-143">相關主題</span><span class="sxs-lookup"><span data-stu-id="1fbf0-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1fbf0-144">著色器模型4元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="1fbf0-144">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





