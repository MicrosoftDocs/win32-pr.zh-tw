---
title: TextureCubeArray 物件
description: TextureCubeArray 類型 (存在於著色器模型 4) 加上資源變數中。 除了著色器模型4中的方法之外，此材質物件也支援這些方法。
ms.assetid: 62AAF0F9-D552-4FFA-B681-749D6DC205BD
keywords:
- TextureCubeArray 物件 HLSL
- TextureCubeArray 物件 HLSL，描述
topic_type:
- apiref
api_name:
- TextureCubeArray
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e559214626fadbc08b8e9cd4d5568358f130779c
ms.sourcegitcommit: 5724b38883e518ac565e1b266defa85ad0941bb2
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "104991846"
---
# <a name="texturecubearray-object"></a><span data-ttu-id="6081c-106">TextureCubeArray 物件</span><span class="sxs-lookup"><span data-stu-id="6081c-106">TextureCubeArray object</span></span>

<span data-ttu-id="6081c-107">**TextureCubeArray** 類型 ([存在於著色器模型 4](dx-graphics-hlsl-to-type.md)) 加上資源變數中。</span><span class="sxs-lookup"><span data-stu-id="6081c-107">**TextureCubeArray** type ([as it exists in Shader Model 4](dx-graphics-hlsl-to-type.md)) plus resource variables.</span></span> <span data-ttu-id="6081c-108">除了著色器模型4中的方法之外，此材質物件也支援這些方法。</span><span class="sxs-lookup"><span data-stu-id="6081c-108">This texture object supports these methods in addition to the methods in Shader Model 4.</span></span>

-   [<span data-ttu-id="6081c-109">方法</span><span class="sxs-lookup"><span data-stu-id="6081c-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="6081c-110">方法</span><span class="sxs-lookup"><span data-stu-id="6081c-110">Methods</span></span>

<span data-ttu-id="6081c-111">**TextureCubeArray** 物件有這些方法。</span><span class="sxs-lookup"><span data-stu-id="6081c-111">The **TextureCubeArray** object has these methods.</span></span>



| <span data-ttu-id="6081c-112">方法</span><span class="sxs-lookup"><span data-stu-id="6081c-112">Method</span></span>                                                           | <span data-ttu-id="6081c-113">描述</span><span class="sxs-lookup"><span data-stu-id="6081c-113">Description</span></span>                                                                                                                                              |
|:-----------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6081c-114">**收集**</span><span class="sxs-lookup"><span data-stu-id="6081c-114">**Gather**</span></span>](texturecubearray-gather.md)                         | <span data-ttu-id="6081c-115">傳回要在雙線性篩選作業中使用的四個材質值。</span><span class="sxs-lookup"><span data-stu-id="6081c-115">Returns the four texel values that would be used in a bi-linear filtering operation.</span></span><br/>                                                                |
| [<span data-ttu-id="6081c-116">**GatherAlpha**</span><span class="sxs-lookup"><span data-stu-id="6081c-116">**GatherAlpha**</span></span>](texturecubearray-gatheralpha.md)               | <span data-ttu-id="6081c-117">傳回四個材質值的 Alpha 元件，這些值會在雙線性篩選作業中使用。</span><span class="sxs-lookup"><span data-stu-id="6081c-117">Returns the alpha components of the four texel values that would be used in a bi-linear filtering operation.</span></span><br/>                                        |
| [<span data-ttu-id="6081c-118">**GatherBlue**</span><span class="sxs-lookup"><span data-stu-id="6081c-118">**GatherBlue**</span></span>](texturecubearray-gatherblue.md)                 | <span data-ttu-id="6081c-119">傳回四個材質值的藍色元件，這些值會用於雙線性篩選作業。</span><span class="sxs-lookup"><span data-stu-id="6081c-119">Returns the blue components of the four texel values that would be used in a bi-linear filtering operation.</span></span><br/>                                         |
| [<span data-ttu-id="6081c-120">**GatherCmp**</span><span class="sxs-lookup"><span data-stu-id="6081c-120">**GatherCmp**</span></span>](texturecubearray-gathercmp.md)                   | <span data-ttu-id="6081c-121">針對要在雙線性篩選作業中使用的四個材質值，會傳回與比較值的比較。</span><span class="sxs-lookup"><span data-stu-id="6081c-121">For four texel values that would be used in a bi-linear filtering operation, returns their comparison against a compare value.</span></span><br/>                      |
| [<span data-ttu-id="6081c-122">**GatherCmpAlpha**</span><span class="sxs-lookup"><span data-stu-id="6081c-122">**GatherCmpAlpha**</span></span>](texturecubearray-gathercmpalpha.md)         | <span data-ttu-id="6081c-123">針對在雙線性篩選作業中使用的四個材質值，會傳回其 Alpha 元件與比較值的比較。</span><span class="sxs-lookup"><span data-stu-id="6081c-123">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their alpha component against a compare value.</span></span><br/> |
| [<span data-ttu-id="6081c-124">**GatherCmpBlue**</span><span class="sxs-lookup"><span data-stu-id="6081c-124">**GatherCmpBlue**</span></span>](texturecubearray-gathercmpblue.md)           | <span data-ttu-id="6081c-125">針對在雙線性篩選作業中使用的四個材質值，會傳回其藍色元件與比較值的比較。</span><span class="sxs-lookup"><span data-stu-id="6081c-125">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their blue component against a compare value.</span></span><br/>  |
| [<span data-ttu-id="6081c-126">**GatherCmpGreen**</span><span class="sxs-lookup"><span data-stu-id="6081c-126">**GatherCmpGreen**</span></span>](texturecubearray-gathercmpgreen.md)         | <span data-ttu-id="6081c-127">針對在雙線性篩選作業中使用的四個材質值，會傳回其綠色元件與比較值的比較。</span><span class="sxs-lookup"><span data-stu-id="6081c-127">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their green component against a compare value.</span></span><br/> |
| [<span data-ttu-id="6081c-128">**GatherCmpRed**</span><span class="sxs-lookup"><span data-stu-id="6081c-128">**GatherCmpRed**</span></span>](texturecubearray-gathercmpred.md)             | <span data-ttu-id="6081c-129">針對在雙線性篩選作業中使用的四個材質值，會傳回其紅色元件與比較值的比較。</span><span class="sxs-lookup"><span data-stu-id="6081c-129">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their red component against a compare value.</span></span><br/>   |
| [<span data-ttu-id="6081c-130">**GatherGreen**</span><span class="sxs-lookup"><span data-stu-id="6081c-130">**GatherGreen**</span></span>](texturecubearray-gathergreen.md)               | <span data-ttu-id="6081c-131">傳回雙線性篩選作業中所使用之四個材質值的綠色元件。</span><span class="sxs-lookup"><span data-stu-id="6081c-131">Returns the green components of the four texel values that would be used in a bi-linear filtering operation.</span></span><br/>                                        |
| [<span data-ttu-id="6081c-132">**GatherRed**</span><span class="sxs-lookup"><span data-stu-id="6081c-132">**GatherRed**</span></span>](texturecubearray-gatherred.md)                   | <span data-ttu-id="6081c-133">傳回四個材質值的紅色元件，這些值會在雙線性篩選作業中使用。</span><span class="sxs-lookup"><span data-stu-id="6081c-133">Returns the red components of the four texel values that would be used in a bi-linear filtering operation.</span></span><br/>                                          |
| [<span data-ttu-id="6081c-134">**範例**</span><span class="sxs-lookup"><span data-stu-id="6081c-134">**Sample**</span></span>](texturecubearray-sample.md)                         | <span data-ttu-id="6081c-135">範例材質。</span><span class="sxs-lookup"><span data-stu-id="6081c-135">Samples a texture.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="6081c-136">**SampleBias**</span><span class="sxs-lookup"><span data-stu-id="6081c-136">**SampleBias**</span></span>](texturecubearray-samplebias.md)                 | <span data-ttu-id="6081c-137">將偏差值套用至 mipmap 層級之後，將材質取樣。</span><span class="sxs-lookup"><span data-stu-id="6081c-137">Samples a texture, after applying the bias value to the mipmap level.</span></span><br/>                                                                               |
| [<span data-ttu-id="6081c-138">**SampleCmp**</span><span class="sxs-lookup"><span data-stu-id="6081c-138">**SampleCmp**</span></span>](texturecubearray-samplecmp.md)                   | <span data-ttu-id="6081c-139">使用比較值來拒絕範例，以取樣材質。</span><span class="sxs-lookup"><span data-stu-id="6081c-139">Samples a texture, using a comparison value to reject samples.</span></span><br/>                                                                                      |
| [<span data-ttu-id="6081c-140">**SampleCmpLevelZero**</span><span class="sxs-lookup"><span data-stu-id="6081c-140">**SampleCmpLevelZero**</span></span>](texturecubearray-samplecmplevelzero.md) | <span data-ttu-id="6081c-141"> (只) 使用比較值來拒絕範例的材質的材質。</span><span class="sxs-lookup"><span data-stu-id="6081c-141">Samples a texture (mipmap level 0 only), using a comparison value to reject samples.</span></span><br/>                                                                |
| [<span data-ttu-id="6081c-142">**SampleGrad**</span><span class="sxs-lookup"><span data-stu-id="6081c-142">**SampleGrad**</span></span>](texturecubearray-samplegrad.md)                 | <span data-ttu-id="6081c-143">使用漸層來取樣材質，以影響範例位置的計算方式。</span><span class="sxs-lookup"><span data-stu-id="6081c-143">Samples a texture using a gradient to influence the way the sample location is calculated.</span></span><br/>                                                          |
| [<span data-ttu-id="6081c-144">**SampleLevel**</span><span class="sxs-lookup"><span data-stu-id="6081c-144">**SampleLevel**</span></span>](texturecubearray-samplelevel.md)               | <span data-ttu-id="6081c-145">針對指定的 mipmap 層級進行紋理取樣。</span><span class="sxs-lookup"><span data-stu-id="6081c-145">Samples a texture on the specified mipmap level.</span></span><br/>                                                                                                    |



 

## <a name="remarks"></a><span data-ttu-id="6081c-146">備註</span><span class="sxs-lookup"><span data-stu-id="6081c-146">Remarks</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="6081c-147">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="6081c-147">Minimum Shader Model</span></span>

<span data-ttu-id="6081c-148">下列著色器模型支援此物件。</span><span class="sxs-lookup"><span data-stu-id="6081c-148">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="6081c-149">著色器模型</span><span class="sxs-lookup"><span data-stu-id="6081c-149">Shader Model</span></span>                                                                | <span data-ttu-id="6081c-150">支援</span><span class="sxs-lookup"><span data-stu-id="6081c-150">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="6081c-151">[著色器模型 5](d3d11-graphics-reference-sm5.md) 和更新版本的著色器模型</span><span class="sxs-lookup"><span data-stu-id="6081c-151">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="6081c-152">是</span><span class="sxs-lookup"><span data-stu-id="6081c-152">yes</span></span>       |



 

<span data-ttu-id="6081c-153">下列著色器類型支援此物件：</span><span class="sxs-lookup"><span data-stu-id="6081c-153">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="6081c-154">頂點</span><span class="sxs-lookup"><span data-stu-id="6081c-154">Vertex</span></span> | <span data-ttu-id="6081c-155">船體</span><span class="sxs-lookup"><span data-stu-id="6081c-155">Hull</span></span> | <span data-ttu-id="6081c-156">網域</span><span class="sxs-lookup"><span data-stu-id="6081c-156">Domain</span></span> | <span data-ttu-id="6081c-157">幾何</span><span class="sxs-lookup"><span data-stu-id="6081c-157">Geometry</span></span> | <span data-ttu-id="6081c-158">像素</span><span class="sxs-lookup"><span data-stu-id="6081c-158">Pixel</span></span> | <span data-ttu-id="6081c-159">計算</span><span class="sxs-lookup"><span data-stu-id="6081c-159">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="6081c-160">x</span><span class="sxs-lookup"><span data-stu-id="6081c-160">x</span></span>      | <span data-ttu-id="6081c-161">x</span><span class="sxs-lookup"><span data-stu-id="6081c-161">x</span></span>    | <span data-ttu-id="6081c-162">x</span><span class="sxs-lookup"><span data-stu-id="6081c-162">x</span></span>      | <span data-ttu-id="6081c-163">x</span><span class="sxs-lookup"><span data-stu-id="6081c-163">x</span></span>        | <span data-ttu-id="6081c-164">x</span><span class="sxs-lookup"><span data-stu-id="6081c-164">x</span></span>     | <span data-ttu-id="6081c-165">x</span><span class="sxs-lookup"><span data-stu-id="6081c-165">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="6081c-166">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6081c-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6081c-167">著色器模型5物件</span><span class="sxs-lookup"><span data-stu-id="6081c-167">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 





