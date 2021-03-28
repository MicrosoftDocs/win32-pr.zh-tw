---
title: Texture3D
description: Texture3D
ms.assetid: a3640aac-b503-4716-8bc6-105e96bea03c
keywords:
- Texture3D HLSL
topic_type:
- apiref
api_name:
- Texture3D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 50b12f2184f6eca0fd7a68feb3e96d8d6fc65a61
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104022356"
---
# <a name="texture3d"></a><span data-ttu-id="1e32d-104">Texture3D</span><span class="sxs-lookup"><span data-stu-id="1e32d-104">Texture3D</span></span>

<span data-ttu-id="1e32d-105">Texture3D 類型 ([存在於著色器模型 4](dx-graphics-hlsl-to-type.md)) 加上資源變數中。</span><span class="sxs-lookup"><span data-stu-id="1e32d-105">Texture3D type ([as it exists in Shader Model 4](dx-graphics-hlsl-to-type.md)) plus resource variables.</span></span> <span data-ttu-id="1e32d-106">除了著色器模型4中的方法之外，此材質物件還支援下列方法。</span><span class="sxs-lookup"><span data-stu-id="1e32d-106">This texture object supports the following methods in addition to the methods in Shader Model 4.</span></span>



| <span data-ttu-id="1e32d-107">方法</span><span class="sxs-lookup"><span data-stu-id="1e32d-107">Method</span></span>                                                                  | <span data-ttu-id="1e32d-108">描述</span><span class="sxs-lookup"><span data-stu-id="1e32d-108">Description</span></span>                                                                                |
|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1e32d-109">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="1e32d-109">**GetDimensions**</span></span>](sm5-object-texture3d-getdimensions.md)             | <span data-ttu-id="1e32d-110">取得資源維度。</span><span class="sxs-lookup"><span data-stu-id="1e32d-110">Gets the resource dimensions.</span></span>                                                              |
| [<span data-ttu-id="1e32d-111">**載入**</span><span class="sxs-lookup"><span data-stu-id="1e32d-111">**Load**</span></span>](texture3d-load.md)                                          | <span data-ttu-id="1e32d-112">讀取紋理資料。</span><span class="sxs-lookup"><span data-stu-id="1e32d-112">Reads texture data.</span></span>                                                                        |
| <span data-ttu-id="1e32d-113">[**Mips。運算元\[\]\[\]**](sm5-object-texture3d-mipsoperatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="1e32d-113">[**mips.Operator\[\]\[\]**](sm5-object-texture3d-mipsoperatorindex.md)</span></span> | <span data-ttu-id="1e32d-114">取得唯讀的資源變數。</span><span class="sxs-lookup"><span data-stu-id="1e32d-114">Gets a read-only resource variable.</span></span>                                                        |
| <span data-ttu-id="1e32d-115">[**運算子\[\]**](sm5-object-texture3d-operatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="1e32d-115">[**Operator\[\]**](sm5-object-texture3d-operatorindex.md)</span></span>              | <span data-ttu-id="1e32d-116">取得唯讀的資源變數。</span><span class="sxs-lookup"><span data-stu-id="1e32d-116">Gets a read-only resource variable.</span></span>                                                        |
| [<span data-ttu-id="1e32d-117">**範例**</span><span class="sxs-lookup"><span data-stu-id="1e32d-117">**Sample**</span></span>](texture3d-sample.md)                                      | <span data-ttu-id="1e32d-118">範例材質。</span><span class="sxs-lookup"><span data-stu-id="1e32d-118">Samples a texture.</span></span>                                                                         |
| [<span data-ttu-id="1e32d-119">**SampleBias**</span><span class="sxs-lookup"><span data-stu-id="1e32d-119">**SampleBias**</span></span>](texture3d-samplebias.md)                              | <span data-ttu-id="1e32d-120">將偏差值套用至 mipmap 層級之後，將材質取樣。</span><span class="sxs-lookup"><span data-stu-id="1e32d-120">Samples a texture, after applying the bias value to the mipmap level.</span></span>                      |
| [<span data-ttu-id="1e32d-121">**SampleGrad**</span><span class="sxs-lookup"><span data-stu-id="1e32d-121">**SampleGrad**</span></span>](texture3d-samplegrad.md)                              | <span data-ttu-id="1e32d-122">使用漸層來取樣材質，以影響範例位置的計算方式。</span><span class="sxs-lookup"><span data-stu-id="1e32d-122">Samples a texture using a gradient to influence the way the sample location is calculated.</span></span> |
| [<span data-ttu-id="1e32d-123">**SampleLevel**</span><span class="sxs-lookup"><span data-stu-id="1e32d-123">**SampleLevel**</span></span>](texture3d-samplelevel.md)                            | <span data-ttu-id="1e32d-124">針對指定的 mipmap 層級進行紋理取樣。</span><span class="sxs-lookup"><span data-stu-id="1e32d-124">Samples a texture on the specified mipmap level.</span></span>                                           |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="1e32d-125">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="1e32d-125">Minimum Shader Model</span></span>

<span data-ttu-id="1e32d-126">下列著色器模型支援此物件。</span><span class="sxs-lookup"><span data-stu-id="1e32d-126">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="1e32d-127">著色器模型</span><span class="sxs-lookup"><span data-stu-id="1e32d-127">Shader Model</span></span>                                                                | <span data-ttu-id="1e32d-128">支援</span><span class="sxs-lookup"><span data-stu-id="1e32d-128">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="1e32d-129">[著色器模型 5](d3d11-graphics-reference-sm5.md) 和更新版本的著色器模型</span><span class="sxs-lookup"><span data-stu-id="1e32d-129">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="1e32d-130">是</span><span class="sxs-lookup"><span data-stu-id="1e32d-130">yes</span></span>       |



 

<span data-ttu-id="1e32d-131">下列著色器類型支援此物件：</span><span class="sxs-lookup"><span data-stu-id="1e32d-131">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="1e32d-132">頂點</span><span class="sxs-lookup"><span data-stu-id="1e32d-132">Vertex</span></span> | <span data-ttu-id="1e32d-133">船體</span><span class="sxs-lookup"><span data-stu-id="1e32d-133">Hull</span></span> | <span data-ttu-id="1e32d-134">網域</span><span class="sxs-lookup"><span data-stu-id="1e32d-134">Domain</span></span> | <span data-ttu-id="1e32d-135">幾何</span><span class="sxs-lookup"><span data-stu-id="1e32d-135">Geometry</span></span> | <span data-ttu-id="1e32d-136">像素</span><span class="sxs-lookup"><span data-stu-id="1e32d-136">Pixel</span></span> | <span data-ttu-id="1e32d-137">計算</span><span class="sxs-lookup"><span data-stu-id="1e32d-137">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="1e32d-138">x</span><span class="sxs-lookup"><span data-stu-id="1e32d-138">x</span></span>      | <span data-ttu-id="1e32d-139">x</span><span class="sxs-lookup"><span data-stu-id="1e32d-139">x</span></span>    | <span data-ttu-id="1e32d-140">x</span><span class="sxs-lookup"><span data-stu-id="1e32d-140">x</span></span>      | <span data-ttu-id="1e32d-141">x</span><span class="sxs-lookup"><span data-stu-id="1e32d-141">x</span></span>        | <span data-ttu-id="1e32d-142">x</span><span class="sxs-lookup"><span data-stu-id="1e32d-142">x</span></span>     | <span data-ttu-id="1e32d-143">x</span><span class="sxs-lookup"><span data-stu-id="1e32d-143">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="1e32d-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1e32d-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e32d-145">著色器模型5物件</span><span class="sxs-lookup"><span data-stu-id="1e32d-145">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




