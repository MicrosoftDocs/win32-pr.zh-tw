---
title: Texture2DArray
description: Texture2DArray
ms.assetid: 78ab2feb-4d67-4f6f-bffe-48d55183ce28
keywords:
- Texture2DArray HLSL
topic_type:
- apiref
api_name:
- Texture2DArray
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f1aefa9171ed634934ea5e1306973fe3b22abdfa
ms.sourcegitcommit: 5724b38883e518ac565e1b266defa85ad0941bb2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "104973872"
---
# <a name="texture2darray"></a><span data-ttu-id="caab1-104">Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="caab1-104">Texture2DArray</span></span>

<span data-ttu-id="caab1-105">Texture2DArray 類型 ([存在於著色器模型 4](dx-graphics-hlsl-to-type.md)) 加上資源變數中。</span><span class="sxs-lookup"><span data-stu-id="caab1-105">Texture2DArray type ([as it exists in Shader Model 4](dx-graphics-hlsl-to-type.md)) plus resource variables.</span></span> <span data-ttu-id="caab1-106">除了著色器模型4中的方法之外，此材質物件還支援下列方法。</span><span class="sxs-lookup"><span data-stu-id="caab1-106">This texture object supports the following methods in addition to the methods in Shader Model 4.</span></span>



| <span data-ttu-id="caab1-107">方法</span><span class="sxs-lookup"><span data-stu-id="caab1-107">Method</span></span>                                                                      | <span data-ttu-id="caab1-108">描述</span><span class="sxs-lookup"><span data-stu-id="caab1-108">Description</span></span>                                                                                                                                         |
|-----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="caab1-109">**收集**</span><span class="sxs-lookup"><span data-stu-id="caab1-109">**Gather**</span></span>](texture2darray-gather.md)                                      | <span data-ttu-id="caab1-110">傳回要在雙線性篩選作業中使用的四個材質值。</span><span class="sxs-lookup"><span data-stu-id="caab1-110">Returns the four texel values that would be used in a bi-linear filtering operation.</span></span>                                                                |
| [<span data-ttu-id="caab1-111">**GatherRed**</span><span class="sxs-lookup"><span data-stu-id="caab1-111">**GatherRed**</span></span>](texture2darray-gatherred.md)                                | <span data-ttu-id="caab1-112">傳回四個材質值的紅色元件，這些值會在雙線性篩選作業中使用。</span><span class="sxs-lookup"><span data-stu-id="caab1-112">Returns the red components of the four texel values that would be used in a bi-linear filtering operation.</span></span>                                          |
| [<span data-ttu-id="caab1-113">**GatherGreen**</span><span class="sxs-lookup"><span data-stu-id="caab1-113">**GatherGreen**</span></span>](texture2darray-gathergreen.md)                            | <span data-ttu-id="caab1-114">傳回雙線性篩選作業中所使用之四個材質值的綠色元件。</span><span class="sxs-lookup"><span data-stu-id="caab1-114">Returns the green components of the four texel values that would be used in a bi-linear filtering operation.</span></span>                                        |
| [<span data-ttu-id="caab1-115">**GatherBlue**</span><span class="sxs-lookup"><span data-stu-id="caab1-115">**GatherBlue**</span></span>](texture2darray-gatherblue.md)                              | <span data-ttu-id="caab1-116">傳回四個材質值的藍色元件，這些值會用於雙線性篩選作業。</span><span class="sxs-lookup"><span data-stu-id="caab1-116">Returns the blue components of the four texel values that would be used in a bi-linear filtering operation.</span></span>                                         |
| [<span data-ttu-id="caab1-117">**GatherAlpha**</span><span class="sxs-lookup"><span data-stu-id="caab1-117">**GatherAlpha**</span></span>](texture2darray-gatheralpha.md)                            | <span data-ttu-id="caab1-118">傳回四個材質值的 Alpha 元件，這些值會在雙線性篩選作業中使用。</span><span class="sxs-lookup"><span data-stu-id="caab1-118">Returns the alpha components of the four texel values that would be used in a bi-linear filtering operation.</span></span>                                        |
| [<span data-ttu-id="caab1-119">**GatherCmp**</span><span class="sxs-lookup"><span data-stu-id="caab1-119">**GatherCmp**</span></span>](texture2darray-gathercmp.md)                                | <span data-ttu-id="caab1-120">針對要在雙線性篩選作業中使用的四個材質值，會傳回與比較值的比較。</span><span class="sxs-lookup"><span data-stu-id="caab1-120">For four texel values that would be used in a bi-linear filtering operation, returns their comparison against a compare value.</span></span>                      |
| [<span data-ttu-id="caab1-121">**GatherCmpRed**</span><span class="sxs-lookup"><span data-stu-id="caab1-121">**GatherCmpRed**</span></span>](texture2darray-gathercmpred.md)                          | <span data-ttu-id="caab1-122">針對在雙線性篩選作業中使用的四個材質值，會傳回其紅色元件與比較值的比較。</span><span class="sxs-lookup"><span data-stu-id="caab1-122">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their red component against a compare value.</span></span>   |
| [<span data-ttu-id="caab1-123">**GatherCmpGreen**</span><span class="sxs-lookup"><span data-stu-id="caab1-123">**GatherCmpGreen**</span></span>](texture2darray-gathercmpgreen.md)                      | <span data-ttu-id="caab1-124">針對在雙線性篩選作業中使用的四個材質值，會傳回其綠色元件與比較值的比較。</span><span class="sxs-lookup"><span data-stu-id="caab1-124">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their green component against a compare value.</span></span> |
| [<span data-ttu-id="caab1-125">**GatherCmpBlue**</span><span class="sxs-lookup"><span data-stu-id="caab1-125">**GatherCmpBlue**</span></span>](texture2darray-gathercmpblue.md)                        | <span data-ttu-id="caab1-126">針對在雙線性篩選作業中使用的四個材質值，會傳回其藍色元件與比較值的比較。</span><span class="sxs-lookup"><span data-stu-id="caab1-126">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their blue component against a compare value.</span></span>  |
| [<span data-ttu-id="caab1-127">**GatherCmpAlpha**</span><span class="sxs-lookup"><span data-stu-id="caab1-127">**GatherCmpAlpha**</span></span>](texture2darray-gathercmpalpha.md)                      | <span data-ttu-id="caab1-128">針對在雙線性篩選作業中使用的四個材質值，會傳回其 Alpha 元件與比較值的比較。</span><span class="sxs-lookup"><span data-stu-id="caab1-128">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their alpha component against a compare value.</span></span> |
| [<span data-ttu-id="caab1-129">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="caab1-129">**GetDimensions**</span></span>](sm5-object-texture2darray-getdimensions.md)             | <span data-ttu-id="caab1-130">取得資源維度。</span><span class="sxs-lookup"><span data-stu-id="caab1-130">Gets the resource dimensions.</span></span>                                                                                                                       |
| [<span data-ttu-id="caab1-131">**載入**</span><span class="sxs-lookup"><span data-stu-id="caab1-131">**Load**</span></span>](texture2darray-load.md)                                          | <span data-ttu-id="caab1-132">讀取紋理資料。</span><span class="sxs-lookup"><span data-stu-id="caab1-132">Reads texture data.</span></span>                                                                                                                                 |
| <span data-ttu-id="caab1-133">[**Mips。運算元\[\]\[\]**](sm5-object-texture2darray-mipsoperatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="caab1-133">[**mips.Operator\[\]\[\]**](sm5-object-texture2darray-mipsoperatorindex.md)</span></span> | <span data-ttu-id="caab1-134">取得唯讀的資源變數。</span><span class="sxs-lookup"><span data-stu-id="caab1-134">Gets a read-only resource variable.</span></span>                                                                                                                 |
| <span data-ttu-id="caab1-135">[**運算子\[\]**](sm5-object-texture2darray-operatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="caab1-135">[**Operator\[\]**](sm5-object-texture2darray-operatorindex.md)</span></span>              | <span data-ttu-id="caab1-136">取得唯讀的資源變數。</span><span class="sxs-lookup"><span data-stu-id="caab1-136">Gets a read-only resource variable.</span></span>                                                                                                                 |
| [<span data-ttu-id="caab1-137">**範例**</span><span class="sxs-lookup"><span data-stu-id="caab1-137">**Sample**</span></span>](texture2darray-sample.md)                                      | <span data-ttu-id="caab1-138">範例材質。</span><span class="sxs-lookup"><span data-stu-id="caab1-138">Samples a texture.</span></span>                                                                                                                                  |
| [<span data-ttu-id="caab1-139">**SampleBias**</span><span class="sxs-lookup"><span data-stu-id="caab1-139">**SampleBias**</span></span>](texture2darray-samplebias.md)                              | <span data-ttu-id="caab1-140">將偏差值套用至 mipmap 層級之後，將材質取樣。</span><span class="sxs-lookup"><span data-stu-id="caab1-140">Samples a texture, after applying the bias value to the mipmap level.</span></span>                                                                               |
| [<span data-ttu-id="caab1-141">**SampleCmp**</span><span class="sxs-lookup"><span data-stu-id="caab1-141">**SampleCmp**</span></span>](texture2darray-samplecmp.md)                                | <span data-ttu-id="caab1-142">使用比較值來拒絕範例，以取樣材質。</span><span class="sxs-lookup"><span data-stu-id="caab1-142">Samples a texture, using a comparison value to reject samples.</span></span>                                                                                      |
| [<span data-ttu-id="caab1-143">**SampleCmpLevelZero**</span><span class="sxs-lookup"><span data-stu-id="caab1-143">**SampleCmpLevelZero**</span></span>](texture2darray-samplecmplevelzero.md)              | <span data-ttu-id="caab1-144"> (只) 使用比較值來拒絕範例的材質的材質。</span><span class="sxs-lookup"><span data-stu-id="caab1-144">Samples a texture (mipmap level 0 only), using a comparison value to reject samples.</span></span>                                                                |
| [<span data-ttu-id="caab1-145">**SampleGrad**</span><span class="sxs-lookup"><span data-stu-id="caab1-145">**SampleGrad**</span></span>](texture2darray-samplegrad.md)                              | <span data-ttu-id="caab1-146">使用漸層來取樣材質，以影響範例位置的計算方式。</span><span class="sxs-lookup"><span data-stu-id="caab1-146">Samples a texture using a gradient to influence the way the sample location is calculated.</span></span>                                                          |
| [<span data-ttu-id="caab1-147">**SampleLevel**</span><span class="sxs-lookup"><span data-stu-id="caab1-147">**SampleLevel**</span></span>](texture2darray-samplelevel.md)                            | <span data-ttu-id="caab1-148">針對指定的 mipmap 層級進行紋理取樣。</span><span class="sxs-lookup"><span data-stu-id="caab1-148">Samples a texture on the specified mipmap level.</span></span>                                                                                                    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="caab1-149">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="caab1-149">Minimum Shader Model</span></span>

<span data-ttu-id="caab1-150">下列著色器模型支援此物件。</span><span class="sxs-lookup"><span data-stu-id="caab1-150">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="caab1-151">著色器模型</span><span class="sxs-lookup"><span data-stu-id="caab1-151">Shader Model</span></span>                                                                | <span data-ttu-id="caab1-152">支援</span><span class="sxs-lookup"><span data-stu-id="caab1-152">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="caab1-153">[著色器模型 5](d3d11-graphics-reference-sm5.md) 和更新版本的著色器模型</span><span class="sxs-lookup"><span data-stu-id="caab1-153">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="caab1-154">是</span><span class="sxs-lookup"><span data-stu-id="caab1-154">yes</span></span>       |



 

<span data-ttu-id="caab1-155">下列著色器類型支援此物件：</span><span class="sxs-lookup"><span data-stu-id="caab1-155">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="caab1-156">頂點</span><span class="sxs-lookup"><span data-stu-id="caab1-156">Vertex</span></span> | <span data-ttu-id="caab1-157">船體</span><span class="sxs-lookup"><span data-stu-id="caab1-157">Hull</span></span> | <span data-ttu-id="caab1-158">網域</span><span class="sxs-lookup"><span data-stu-id="caab1-158">Domain</span></span> | <span data-ttu-id="caab1-159">幾何</span><span class="sxs-lookup"><span data-stu-id="caab1-159">Geometry</span></span> | <span data-ttu-id="caab1-160">像素</span><span class="sxs-lookup"><span data-stu-id="caab1-160">Pixel</span></span> | <span data-ttu-id="caab1-161">計算</span><span class="sxs-lookup"><span data-stu-id="caab1-161">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="caab1-162">x</span><span class="sxs-lookup"><span data-stu-id="caab1-162">x</span></span>      | <span data-ttu-id="caab1-163">x</span><span class="sxs-lookup"><span data-stu-id="caab1-163">x</span></span>    | <span data-ttu-id="caab1-164">x</span><span class="sxs-lookup"><span data-stu-id="caab1-164">x</span></span>      | <span data-ttu-id="caab1-165">x</span><span class="sxs-lookup"><span data-stu-id="caab1-165">x</span></span>        | <span data-ttu-id="caab1-166">x</span><span class="sxs-lookup"><span data-stu-id="caab1-166">x</span></span>     | <span data-ttu-id="caab1-167">x</span><span class="sxs-lookup"><span data-stu-id="caab1-167">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="caab1-168">另請參閱</span><span class="sxs-lookup"><span data-stu-id="caab1-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="caab1-169">著色器模型5物件</span><span class="sxs-lookup"><span data-stu-id="caab1-169">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




