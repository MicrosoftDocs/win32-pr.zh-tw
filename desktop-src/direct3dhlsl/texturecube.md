---
title: TextureCube 物件
description: TextureCube 類型 (存在於著色器模型 4) 加上資源變數中。 除了著色器模型4中的方法之外，此材質物件也支援這些方法。
ms.assetid: BC96D7BB-992E-48CC-A774-E211E1BB1720
keywords:
- TextureCube 物件 HLSL
- TextureCube 物件 HLSL，描述
topic_type:
- apiref
api_name:
- TextureCube
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 939c79895ae1c24665fc70d6b6cf2ced19854e2b
ms.sourcegitcommit: 5724b38883e518ac565e1b266defa85ad0941bb2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "104116021"
---
# <a name="texturecube-object"></a><span data-ttu-id="d865f-106">TextureCube 物件</span><span class="sxs-lookup"><span data-stu-id="d865f-106">TextureCube object</span></span>

<span data-ttu-id="d865f-107">**TextureCube** 類型 ([存在於著色器模型 4](dx-graphics-hlsl-to-type.md)) 加上資源變數中。</span><span class="sxs-lookup"><span data-stu-id="d865f-107">**TextureCube** type ([as it exists in Shader Model 4](dx-graphics-hlsl-to-type.md)) plus resource variables.</span></span> <span data-ttu-id="d865f-108">除了著色器模型4中的方法之外，此材質物件也支援這些方法。</span><span class="sxs-lookup"><span data-stu-id="d865f-108">This texture object supports these methods in addition to the methods in Shader Model 4.</span></span>

-   [<span data-ttu-id="d865f-109">方法</span><span class="sxs-lookup"><span data-stu-id="d865f-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="d865f-110">方法</span><span class="sxs-lookup"><span data-stu-id="d865f-110">Methods</span></span>

<span data-ttu-id="d865f-111">**TextureCube** 物件有這些方法。</span><span class="sxs-lookup"><span data-stu-id="d865f-111">The **TextureCube** object has these methods.</span></span>



| <span data-ttu-id="d865f-112">方法</span><span class="sxs-lookup"><span data-stu-id="d865f-112">Method</span></span>                                                      | <span data-ttu-id="d865f-113">描述</span><span class="sxs-lookup"><span data-stu-id="d865f-113">Description</span></span>                                                                                                                                             |
|:------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d865f-114">**收集**</span><span class="sxs-lookup"><span data-stu-id="d865f-114">**Gather**</span></span>](texturecube-gather.md)                         | <span data-ttu-id="d865f-115">傳回要在雙線性篩選作業中使用的四個材質值。</span><span class="sxs-lookup"><span data-stu-id="d865f-115">Returns the four texel values that would be used in a bi-linear filtering operation.</span></span><br/>                                                                |
| [<span data-ttu-id="d865f-116">**GatherAlpha**</span><span class="sxs-lookup"><span data-stu-id="d865f-116">**GatherAlpha**</span></span>](texturecube-gatheralpha.md)               | <span data-ttu-id="d865f-117">傳回四個材質值的 Alpha 元件，這些值會在雙線性篩選作業中使用。</span><span class="sxs-lookup"><span data-stu-id="d865f-117">Returns the alpha components of the four texel values that would be used in a bi-linear filtering operation.</span></span><br/>                                        |
| [<span data-ttu-id="d865f-118">**GatherBlue**</span><span class="sxs-lookup"><span data-stu-id="d865f-118">**GatherBlue**</span></span>](texturecube-gatherblue.md)                 | <span data-ttu-id="d865f-119">傳回四個材質值的藍色元件，這些值會用於雙線性篩選作業。</span><span class="sxs-lookup"><span data-stu-id="d865f-119">Returns the blue components of the four texel values that would be used in a bi-linear filtering operation.</span></span><br/>                                         |
| [<span data-ttu-id="d865f-120">**GatherCmp**</span><span class="sxs-lookup"><span data-stu-id="d865f-120">**GatherCmp**</span></span>](texturecube-gathercmp.md)                   | <span data-ttu-id="d865f-121">針對要在雙線性篩選作業中使用的四個材質值，會傳回與比較值的比較。</span><span class="sxs-lookup"><span data-stu-id="d865f-121">For four texel values that would be used in a bi-linear filtering operation, returns their comparison against a compare value.</span></span><br/>                      |
| [<span data-ttu-id="d865f-122">**GatherCmpAlpha**</span><span class="sxs-lookup"><span data-stu-id="d865f-122">**GatherCmpAlpha**</span></span>](texturecube-gathercmpalpha.md)         | <span data-ttu-id="d865f-123">針對在雙線性篩選作業中使用的四個材質值，會傳回其 Alpha 元件與比較值的比較。</span><span class="sxs-lookup"><span data-stu-id="d865f-123">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their alpha component against a compare value.</span></span><br/> |
| [<span data-ttu-id="d865f-124">**GatherCmpBlue**</span><span class="sxs-lookup"><span data-stu-id="d865f-124">**GatherCmpBlue**</span></span>](texturecube-gathercmpblue.md)           | <span data-ttu-id="d865f-125">針對在雙線性篩選作業中使用的四個材質值，會傳回其藍色元件與比較值的比較。</span><span class="sxs-lookup"><span data-stu-id="d865f-125">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their blue component against a compare value.</span></span><br/>  |
| [<span data-ttu-id="d865f-126">**GatherCmpGreen**</span><span class="sxs-lookup"><span data-stu-id="d865f-126">**GatherCmpGreen**</span></span>](texturecube-gathercmpgreen.md)         | <span data-ttu-id="d865f-127">針對在雙線性篩選作業中使用的四個材質值，會傳回其綠色元件與比較值的比較。</span><span class="sxs-lookup"><span data-stu-id="d865f-127">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their green component against a compare value.</span></span><br/> |
| [<span data-ttu-id="d865f-128">**GatherCmpRed**</span><span class="sxs-lookup"><span data-stu-id="d865f-128">**GatherCmpRed**</span></span>](texturecube-gathercmpred.md)             | <span data-ttu-id="d865f-129">針對在雙線性篩選作業中使用的四個材質值，會傳回其紅色元件與比較值的比較。</span><span class="sxs-lookup"><span data-stu-id="d865f-129">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their red component against a compare value.</span></span><br/>   |
| [<span data-ttu-id="d865f-130">**GatherGreen**</span><span class="sxs-lookup"><span data-stu-id="d865f-130">**GatherGreen**</span></span>](texturecube-gathergreen.md)               | <span data-ttu-id="d865f-131">傳回雙線性篩選作業中所使用之四個材質值的綠色元件。</span><span class="sxs-lookup"><span data-stu-id="d865f-131">Returns the green components of the four texel values that would be used in a bi-linear filtering operation.</span></span><br/>                                        |
| [<span data-ttu-id="d865f-132">**GatherRed**</span><span class="sxs-lookup"><span data-stu-id="d865f-132">**GatherRed**</span></span>](texturecube-gatherred.md)                   | <span data-ttu-id="d865f-133">傳回四個材質值的紅色元件，這些值會在雙線性篩選作業中使用。</span><span class="sxs-lookup"><span data-stu-id="d865f-133">Returns the red components of the four texel values that would be used in a bi-linear filtering operation.</span></span><br/>                                          |
| [<span data-ttu-id="d865f-134">**範例**</span><span class="sxs-lookup"><span data-stu-id="d865f-134">**Sample**</span></span>](texturecube-sample.md)                         | <span data-ttu-id="d865f-135">範例材質。</span><span class="sxs-lookup"><span data-stu-id="d865f-135">Samples a texture.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="d865f-136">**SampleBias**</span><span class="sxs-lookup"><span data-stu-id="d865f-136">**SampleBias**</span></span>](texturecube-samplebias.md)                 | <span data-ttu-id="d865f-137">將偏差值套用至 mipmap 層級之後，將材質取樣。</span><span class="sxs-lookup"><span data-stu-id="d865f-137">Samples a texture, after applying the bias value to the mipmap level.</span></span><br/>                                                                               |
| [<span data-ttu-id="d865f-138">**SampleCmp**</span><span class="sxs-lookup"><span data-stu-id="d865f-138">**SampleCmp**</span></span>](texturecube-samplecmp.md)                   | <span data-ttu-id="d865f-139">使用比較值來拒絕範例，以取樣材質。</span><span class="sxs-lookup"><span data-stu-id="d865f-139">Samples a texture, using a comparison value to reject samples.</span></span><br/>                                                                                      |
| [<span data-ttu-id="d865f-140">**SampleCmpLevelZero**</span><span class="sxs-lookup"><span data-stu-id="d865f-140">**SampleCmpLevelZero**</span></span>](texturecube-samplecmplevelzero.md) | <span data-ttu-id="d865f-141"> (只) 使用比較值來拒絕範例的材質的材質。</span><span class="sxs-lookup"><span data-stu-id="d865f-141">Samples a texture (mipmap level 0 only), using a comparison value to reject samples.</span></span><br/>                                                                |
| [<span data-ttu-id="d865f-142">**SampleGrad**</span><span class="sxs-lookup"><span data-stu-id="d865f-142">**SampleGrad**</span></span>](texturecube-samplegrad.md)                 | <span data-ttu-id="d865f-143">使用漸層來取樣材質，以影響範例位置的計算方式。</span><span class="sxs-lookup"><span data-stu-id="d865f-143">Samples a texture using a gradient to influence the way the sample location is calculated.</span></span><br/>                                                          |
| [<span data-ttu-id="d865f-144">**SampleLevel**</span><span class="sxs-lookup"><span data-stu-id="d865f-144">**SampleLevel**</span></span>](texturecube-samplelevel.md)               | <span data-ttu-id="d865f-145">針對指定的 mipmap 層級進行紋理取樣。</span><span class="sxs-lookup"><span data-stu-id="d865f-145">Samples a texture on the specified mipmap level.</span></span><br/>                                                                                                    |



 

## <a name="remarks"></a><span data-ttu-id="d865f-146">備註</span><span class="sxs-lookup"><span data-stu-id="d865f-146">Remarks</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="d865f-147">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="d865f-147">Minimum Shader Model</span></span>

<span data-ttu-id="d865f-148">下列著色器模型支援此物件。</span><span class="sxs-lookup"><span data-stu-id="d865f-148">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="d865f-149">著色器模型</span><span class="sxs-lookup"><span data-stu-id="d865f-149">Shader Model</span></span>                                                                | <span data-ttu-id="d865f-150">支援</span><span class="sxs-lookup"><span data-stu-id="d865f-150">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="d865f-151">[著色器模型 5](d3d11-graphics-reference-sm5.md) 和更新版本的著色器模型</span><span class="sxs-lookup"><span data-stu-id="d865f-151">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="d865f-152">是</span><span class="sxs-lookup"><span data-stu-id="d865f-152">yes</span></span>       |



 

<span data-ttu-id="d865f-153">下列著色器類型支援此物件：</span><span class="sxs-lookup"><span data-stu-id="d865f-153">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="d865f-154">頂點</span><span class="sxs-lookup"><span data-stu-id="d865f-154">Vertex</span></span> | <span data-ttu-id="d865f-155">船體</span><span class="sxs-lookup"><span data-stu-id="d865f-155">Hull</span></span> | <span data-ttu-id="d865f-156">網域</span><span class="sxs-lookup"><span data-stu-id="d865f-156">Domain</span></span> | <span data-ttu-id="d865f-157">幾何</span><span class="sxs-lookup"><span data-stu-id="d865f-157">Geometry</span></span> | <span data-ttu-id="d865f-158">像素</span><span class="sxs-lookup"><span data-stu-id="d865f-158">Pixel</span></span> | <span data-ttu-id="d865f-159">計算</span><span class="sxs-lookup"><span data-stu-id="d865f-159">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="d865f-160">x</span><span class="sxs-lookup"><span data-stu-id="d865f-160">x</span></span>      | <span data-ttu-id="d865f-161">x</span><span class="sxs-lookup"><span data-stu-id="d865f-161">x</span></span>    | <span data-ttu-id="d865f-162">x</span><span class="sxs-lookup"><span data-stu-id="d865f-162">x</span></span>      | <span data-ttu-id="d865f-163">x</span><span class="sxs-lookup"><span data-stu-id="d865f-163">x</span></span>        | <span data-ttu-id="d865f-164">x</span><span class="sxs-lookup"><span data-stu-id="d865f-164">x</span></span>     | <span data-ttu-id="d865f-165">x</span><span class="sxs-lookup"><span data-stu-id="d865f-165">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="d865f-166">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d865f-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d865f-167">著色器模型5物件</span><span class="sxs-lookup"><span data-stu-id="d865f-167">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 





