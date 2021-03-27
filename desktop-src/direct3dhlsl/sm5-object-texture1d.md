---
title: Texture1D
description: Texture1D
ms.assetid: 5f6fd0e4-a73e-4d13-b3a0-c884b7912581
keywords:
- Texture1D HLSL
topic_type:
- apiref
api_name:
- Texture1D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8b8a60706ea2752109cdda9907ffe7c654efe531
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "103932743"
---
# <a name="texture1d"></a><span data-ttu-id="7d46d-104">Texture1D</span><span class="sxs-lookup"><span data-stu-id="7d46d-104">Texture1D</span></span>

<span data-ttu-id="7d46d-105">一維紋理類型 ([存在於著色器模型 4](dx-graphics-hlsl-to-type.md)) 加上資源變數中。</span><span class="sxs-lookup"><span data-stu-id="7d46d-105">A 1D texture type ([as it exists in Shader Model 4](dx-graphics-hlsl-to-type.md)) plus resource variables.</span></span> <span data-ttu-id="7d46d-106">除了著色器模型4中的方法之外，此材質物件還支援下列方法。</span><span class="sxs-lookup"><span data-stu-id="7d46d-106">This texture object supports the following methods in addition to the methods in Shader Model 4.</span></span>



| <span data-ttu-id="7d46d-107">方法</span><span class="sxs-lookup"><span data-stu-id="7d46d-107">Method</span></span>                                                                  | <span data-ttu-id="7d46d-108">描述</span><span class="sxs-lookup"><span data-stu-id="7d46d-108">Description</span></span>                                                                                |
|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7d46d-109">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="7d46d-109">**GetDimensions**</span></span>](sm5-object-texture1d-getdimensions.md)             | <span data-ttu-id="7d46d-110">取得資源維度。</span><span class="sxs-lookup"><span data-stu-id="7d46d-110">Gets the resource dimensions.</span></span>                                                              |
| [<span data-ttu-id="7d46d-111">**載入**</span><span class="sxs-lookup"><span data-stu-id="7d46d-111">**Load**</span></span>](texture1d-load.md)                                          | <span data-ttu-id="7d46d-112">讀取紋理資料。</span><span class="sxs-lookup"><span data-stu-id="7d46d-112">Reads texture data.</span></span>                                                                        |
| <span data-ttu-id="7d46d-113">[**運算子\[\]**](sm5-object-texture1d-operatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="7d46d-113">[**Operator\[\]**](sm5-object-texture1d-operatorindex.md)</span></span>              | <span data-ttu-id="7d46d-114">取得唯讀的資源變數。</span><span class="sxs-lookup"><span data-stu-id="7d46d-114">Gets a read-only resource variable.</span></span>                                                        |
| <span data-ttu-id="7d46d-115">[**Mips。運算元\[\]\[\]**](sm5-object-texture1d-mipsoperatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="7d46d-115">[**mips.Operator\[\]\[\]**](sm5-object-texture1d-mipsoperatorindex.md)</span></span> | <span data-ttu-id="7d46d-116">取得唯讀的資源變數。</span><span class="sxs-lookup"><span data-stu-id="7d46d-116">Gets a read-only resource variable.</span></span>                                                        |
| [<span data-ttu-id="7d46d-117">**範例**</span><span class="sxs-lookup"><span data-stu-id="7d46d-117">**Sample**</span></span>](texture1d-sample.md)                                      | <span data-ttu-id="7d46d-118">範例材質。</span><span class="sxs-lookup"><span data-stu-id="7d46d-118">Samples a texture.</span></span>                                                                         |
| [<span data-ttu-id="7d46d-119">**SampleBias**</span><span class="sxs-lookup"><span data-stu-id="7d46d-119">**SampleBias**</span></span>](texture1d-samplebias.md)                              | <span data-ttu-id="7d46d-120">將偏差值套用至 mipmap 層級之後，將材質取樣。</span><span class="sxs-lookup"><span data-stu-id="7d46d-120">Samples a texture, after applying the bias value to the mipmap level.</span></span>                      |
| [<span data-ttu-id="7d46d-121">**SampleCmp**</span><span class="sxs-lookup"><span data-stu-id="7d46d-121">**SampleCmp**</span></span>](texture1d-samplecmp.md)                                | <span data-ttu-id="7d46d-122">使用比較值來拒絕範例，以取樣材質。</span><span class="sxs-lookup"><span data-stu-id="7d46d-122">Samples a texture, using a comparison value to reject samples.</span></span>                             |
| [<span data-ttu-id="7d46d-123">**SampleCmpLevelZero**</span><span class="sxs-lookup"><span data-stu-id="7d46d-123">**SampleCmpLevelZero**</span></span>](texture1d-samplecmplevelzero.md)              | <span data-ttu-id="7d46d-124"> (只) 使用比較值來拒絕範例的材質的材質。</span><span class="sxs-lookup"><span data-stu-id="7d46d-124">Samples a texture (mipmap level 0 only), using a comparison value to reject samples.</span></span>       |
| [<span data-ttu-id="7d46d-125">**SampleGrad**</span><span class="sxs-lookup"><span data-stu-id="7d46d-125">**SampleGrad**</span></span>](texture1d-samplegrad.md)                              | <span data-ttu-id="7d46d-126">使用漸層來取樣材質，以影響範例位置的計算方式。</span><span class="sxs-lookup"><span data-stu-id="7d46d-126">Samples a texture using a gradient to influence the way the sample location is calculated.</span></span> |
| [<span data-ttu-id="7d46d-127">**SampleLevel**</span><span class="sxs-lookup"><span data-stu-id="7d46d-127">**SampleLevel**</span></span>](texture1d-samplelevel.md)                            | <span data-ttu-id="7d46d-128">針對指定的 mipmap 層級進行紋理取樣。</span><span class="sxs-lookup"><span data-stu-id="7d46d-128">Samples a texture on the specified mipmap level.</span></span>                                           |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="7d46d-129">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="7d46d-129">Minimum Shader Model</span></span>

<span data-ttu-id="7d46d-130">下列著色器模型支援此物件。</span><span class="sxs-lookup"><span data-stu-id="7d46d-130">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="7d46d-131">著色器模型</span><span class="sxs-lookup"><span data-stu-id="7d46d-131">Shader Model</span></span>                                                                | <span data-ttu-id="7d46d-132">支援</span><span class="sxs-lookup"><span data-stu-id="7d46d-132">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="7d46d-133">[著色器模型 5](d3d11-graphics-reference-sm5.md) 和更新版本的著色器模型</span><span class="sxs-lookup"><span data-stu-id="7d46d-133">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="7d46d-134">是</span><span class="sxs-lookup"><span data-stu-id="7d46d-134">yes</span></span>       |



 

<span data-ttu-id="7d46d-135">下列著色器類型支援此物件：</span><span class="sxs-lookup"><span data-stu-id="7d46d-135">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="7d46d-136">頂點</span><span class="sxs-lookup"><span data-stu-id="7d46d-136">Vertex</span></span> | <span data-ttu-id="7d46d-137">船體</span><span class="sxs-lookup"><span data-stu-id="7d46d-137">Hull</span></span> | <span data-ttu-id="7d46d-138">網域</span><span class="sxs-lookup"><span data-stu-id="7d46d-138">Domain</span></span> | <span data-ttu-id="7d46d-139">幾何</span><span class="sxs-lookup"><span data-stu-id="7d46d-139">Geometry</span></span> | <span data-ttu-id="7d46d-140">像素</span><span class="sxs-lookup"><span data-stu-id="7d46d-140">Pixel</span></span> | <span data-ttu-id="7d46d-141">計算</span><span class="sxs-lookup"><span data-stu-id="7d46d-141">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="7d46d-142">x</span><span class="sxs-lookup"><span data-stu-id="7d46d-142">x</span></span>      | <span data-ttu-id="7d46d-143">x</span><span class="sxs-lookup"><span data-stu-id="7d46d-143">x</span></span>    | <span data-ttu-id="7d46d-144">x</span><span class="sxs-lookup"><span data-stu-id="7d46d-144">x</span></span>      | <span data-ttu-id="7d46d-145">x</span><span class="sxs-lookup"><span data-stu-id="7d46d-145">x</span></span>        | <span data-ttu-id="7d46d-146">x</span><span class="sxs-lookup"><span data-stu-id="7d46d-146">x</span></span>     | <span data-ttu-id="7d46d-147">x</span><span class="sxs-lookup"><span data-stu-id="7d46d-147">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="7d46d-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7d46d-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d46d-149">著色器模型5物件</span><span class="sxs-lookup"><span data-stu-id="7d46d-149">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




