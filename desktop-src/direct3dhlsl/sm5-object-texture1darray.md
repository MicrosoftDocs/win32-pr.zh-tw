---
title: Texture1DArray
description: Texture1DArray
ms.assetid: 3d793423-3d79-48c1-aa78-f9d93b79e0b6
keywords:
- Texture1DArray HLSL
topic_type:
- apiref
api_name:
- Texture1DArray
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 39cea5692e29ead74ba20c4a35ab8d43a1b19d42
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104022586"
---
# <a name="texture1darray"></a><span data-ttu-id="59a71-104">Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="59a71-104">Texture1DArray</span></span>

<span data-ttu-id="59a71-105">Texture1DArray 類型 ([存在於著色器模型 4](dx-graphics-hlsl-to-type.md)) 加上資源變數中。</span><span class="sxs-lookup"><span data-stu-id="59a71-105">Texture1DArray type ([as it exists in Shader Model 4](dx-graphics-hlsl-to-type.md)) plus resource variables.</span></span> <span data-ttu-id="59a71-106">除了著色器模型4中的方法之外，此材質物件還支援下列方法。</span><span class="sxs-lookup"><span data-stu-id="59a71-106">This texture object supports the following methods in addition to the methods in Shader Model 4.</span></span>



| <span data-ttu-id="59a71-107">方法</span><span class="sxs-lookup"><span data-stu-id="59a71-107">Method</span></span>                                                                       | <span data-ttu-id="59a71-108">描述</span><span class="sxs-lookup"><span data-stu-id="59a71-108">Description</span></span>                                                                                |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="59a71-109">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="59a71-109">**GetDimensions**</span></span>](sm5-object-texture1darray-getdimensions.md)             | <span data-ttu-id="59a71-110">取得資源維度。</span><span class="sxs-lookup"><span data-stu-id="59a71-110">Gets the resource dimensions.</span></span>                                                              |
| [<span data-ttu-id="59a71-111">**載入**</span><span class="sxs-lookup"><span data-stu-id="59a71-111">**Load**</span></span>](texture1darray-load.md)                                          | <span data-ttu-id="59a71-112">讀取紋理資料。</span><span class="sxs-lookup"><span data-stu-id="59a71-112">Reads texture data.</span></span>                                                                        |
| <span data-ttu-id="59a71-113">[**Mips。運算元\[\]\[\]**](sm5-object-texture1darray-mipsoperatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="59a71-113">[**mips.Operator\[\]\[\]**](sm5-object-texture1darray-mipsoperatorindex.md)</span></span> | <span data-ttu-id="59a71-114">取得唯讀的資源變數。</span><span class="sxs-lookup"><span data-stu-id="59a71-114">Gets a read-only resource variable.</span></span>                                                        |
| <span data-ttu-id="59a71-115">[**運算子\[\]**](sm5-object-texture1darray-operatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="59a71-115">[**Operator\[\]**](sm5-object-texture1darray-operatorindex.md)</span></span>              | <span data-ttu-id="59a71-116">取得唯讀的資源變數。</span><span class="sxs-lookup"><span data-stu-id="59a71-116">Gets a read-only resource variable.</span></span>                                                        |
| [<span data-ttu-id="59a71-117">**範例**</span><span class="sxs-lookup"><span data-stu-id="59a71-117">**Sample**</span></span>](texture1darray-sample.md)                                      | <span data-ttu-id="59a71-118">範例材質。</span><span class="sxs-lookup"><span data-stu-id="59a71-118">Samples a texture.</span></span>                                                                         |
| [<span data-ttu-id="59a71-119">**SampleBias**</span><span class="sxs-lookup"><span data-stu-id="59a71-119">**SampleBias**</span></span>](texture1darray-samplebias.md)                              | <span data-ttu-id="59a71-120">將偏差值套用至 mipmap 層級之後，將材質取樣。</span><span class="sxs-lookup"><span data-stu-id="59a71-120">Samples a texture, after applying the bias value to the mipmap level.</span></span>                      |
| [<span data-ttu-id="59a71-121">**SampleCmp**</span><span class="sxs-lookup"><span data-stu-id="59a71-121">**SampleCmp**</span></span>](texture1darray-samplecmp.md)                                | <span data-ttu-id="59a71-122">使用比較值來拒絕範例，以取樣材質。</span><span class="sxs-lookup"><span data-stu-id="59a71-122">Samples a texture, using a comparison value to reject samples.</span></span>                             |
| [<span data-ttu-id="59a71-123">**SampleCmpLevelZero**</span><span class="sxs-lookup"><span data-stu-id="59a71-123">**SampleCmpLevelZero**</span></span>](texture1darray-samplecmplevelzero.md)              | <span data-ttu-id="59a71-124"> (只) 使用比較值來拒絕範例的材質的材質。</span><span class="sxs-lookup"><span data-stu-id="59a71-124">Samples a texture (mipmap level 0 only), using a comparison value to reject samples.</span></span>       |
| [<span data-ttu-id="59a71-125">**SampleGrad**</span><span class="sxs-lookup"><span data-stu-id="59a71-125">**SampleGrad**</span></span>](texture1darray-samplegrad.md)                              | <span data-ttu-id="59a71-126">使用漸層來取樣材質，以影響範例位置的計算方式。</span><span class="sxs-lookup"><span data-stu-id="59a71-126">Samples a texture using a gradient to influence the way the sample location is calculated.</span></span> |
| [<span data-ttu-id="59a71-127">**SampleLevel**</span><span class="sxs-lookup"><span data-stu-id="59a71-127">**SampleLevel**</span></span>](texture1darray-samplelevel.md)                            | <span data-ttu-id="59a71-128">針對指定的 mipmap 層級進行紋理取樣。</span><span class="sxs-lookup"><span data-stu-id="59a71-128">Samples a texture on the specified mipmap level.</span></span>                                           |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="59a71-129">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="59a71-129">Minimum Shader Model</span></span>

<span data-ttu-id="59a71-130">下列著色器模型支援此物件。</span><span class="sxs-lookup"><span data-stu-id="59a71-130">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="59a71-131">著色器模型</span><span class="sxs-lookup"><span data-stu-id="59a71-131">Shader Model</span></span>                                                                | <span data-ttu-id="59a71-132">支援</span><span class="sxs-lookup"><span data-stu-id="59a71-132">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="59a71-133">[著色器模型 5](d3d11-graphics-reference-sm5.md) 和更新版本的著色器模型</span><span class="sxs-lookup"><span data-stu-id="59a71-133">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="59a71-134">是</span><span class="sxs-lookup"><span data-stu-id="59a71-134">yes</span></span>       |



 

<span data-ttu-id="59a71-135">下列著色器類型支援此物件：</span><span class="sxs-lookup"><span data-stu-id="59a71-135">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="59a71-136">頂點</span><span class="sxs-lookup"><span data-stu-id="59a71-136">Vertex</span></span> | <span data-ttu-id="59a71-137">船體</span><span class="sxs-lookup"><span data-stu-id="59a71-137">Hull</span></span> | <span data-ttu-id="59a71-138">網域</span><span class="sxs-lookup"><span data-stu-id="59a71-138">Domain</span></span> | <span data-ttu-id="59a71-139">幾何</span><span class="sxs-lookup"><span data-stu-id="59a71-139">Geometry</span></span> | <span data-ttu-id="59a71-140">像素</span><span class="sxs-lookup"><span data-stu-id="59a71-140">Pixel</span></span> | <span data-ttu-id="59a71-141">計算</span><span class="sxs-lookup"><span data-stu-id="59a71-141">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="59a71-142">x</span><span class="sxs-lookup"><span data-stu-id="59a71-142">x</span></span>      | <span data-ttu-id="59a71-143">x</span><span class="sxs-lookup"><span data-stu-id="59a71-143">x</span></span>    | <span data-ttu-id="59a71-144">x</span><span class="sxs-lookup"><span data-stu-id="59a71-144">x</span></span>      | <span data-ttu-id="59a71-145">x</span><span class="sxs-lookup"><span data-stu-id="59a71-145">x</span></span>        | <span data-ttu-id="59a71-146">x</span><span class="sxs-lookup"><span data-stu-id="59a71-146">x</span></span>     | <span data-ttu-id="59a71-147">x</span><span class="sxs-lookup"><span data-stu-id="59a71-147">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="59a71-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="59a71-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59a71-149">著色器模型5物件</span><span class="sxs-lookup"><span data-stu-id="59a71-149">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




