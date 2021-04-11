---
title: Texture2D：： GatherCmpGreen (S、float、float、int2、int2、int2、int2、uint) 函數
description: 針對在雙線性篩選作業中使用的四個材質值，會傳回其綠色元件與比較值的比較，以及磚對應狀態。 |Texture2D：： GatherCmpGreen (S、float、float、int2、int2、int2、int2、uint) 函數
ms.assetid: E7EB3D17-3110-4167-B255-C451BA4EFB27
keywords:
- GatherCmpGreen 函式 HLSL
topic_type:
- apiref
api_name:
- GatherCmpGreen
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8b490fd47bd9346c4f514867de63df7a4d090e5b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104196034"
---
# <a name="texture2dgathercmpgreensfloatfloatint2int2int2int2uint-function"></a><span data-ttu-id="ad7df-105">Texture2D：： GatherCmpGreen (S、float、float、int2、int2、int2、int2、uint) 函數</span><span class="sxs-lookup"><span data-stu-id="ad7df-105">Texture2D::GatherCmpGreen(S,float,float,int2,int2,int2,int2,uint) function</span></span>

<span data-ttu-id="ad7df-106">針對在雙線性篩選作業中使用的四個材質值，會傳回其綠色元件與比較值的比較，以及磚對應狀態。</span><span class="sxs-lookup"><span data-stu-id="ad7df-106">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their green component against a compare value along with tile-mapping status.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad7df-107">語法</span><span class="sxs-lookup"><span data-stu-id="ad7df-107">Syntax</span></span>


``` syntax
TemplateType GatherCmpGreen(
  in  SamplerState S,
  in  float        Location,
  in  float        CompareValue,
  in  int2         Offset1,
  in  int2         Offset2,
  in  int2         Offset3,
  in  int2         Offset4,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="ad7df-108">參數</span><span class="sxs-lookup"><span data-stu-id="ad7df-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad7df-109"> \[ 中的 S\]</span><span class="sxs-lookup"><span data-stu-id="ad7df-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad7df-110">類型： **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="ad7df-110">Type: **SamplerState**</span></span>

<span data-ttu-id="ad7df-111">以零為基底的取樣器索引。</span><span class="sxs-lookup"><span data-stu-id="ad7df-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="ad7df-112">*位置* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ad7df-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad7df-113">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="ad7df-113">Type: **float**</span></span>

<span data-ttu-id="ad7df-114">此範例會協調 (u，v) 。</span><span class="sxs-lookup"><span data-stu-id="ad7df-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="ad7df-115">*CompareValue* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ad7df-115">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad7df-116">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="ad7df-116">Type: **float**</span></span>

<span data-ttu-id="ad7df-117">要針對每個取樣值進行比較的值。</span><span class="sxs-lookup"><span data-stu-id="ad7df-117">A value to compare each against each sampled value.</span></span>

</dd> <dt>

<span data-ttu-id="ad7df-118">*Offset1* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ad7df-118">*Offset1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad7df-119">類型： **int2**</span><span class="sxs-lookup"><span data-stu-id="ad7df-119">Type: **int2**</span></span>

<span data-ttu-id="ad7df-120">第一個位移元件會在取樣之前套用至材質座標。</span><span class="sxs-lookup"><span data-stu-id="ad7df-120">The first offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="ad7df-121">*Offset2* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ad7df-121">*Offset2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad7df-122">類型： **int2**</span><span class="sxs-lookup"><span data-stu-id="ad7df-122">Type: **int2**</span></span>

<span data-ttu-id="ad7df-123">第二個位移元件會在取樣之前套用至材質座標。</span><span class="sxs-lookup"><span data-stu-id="ad7df-123">The second offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="ad7df-124">*Offset3* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ad7df-124">*Offset3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad7df-125">類型： **int2**</span><span class="sxs-lookup"><span data-stu-id="ad7df-125">Type: **int2**</span></span>

<span data-ttu-id="ad7df-126">第三個位移元件會在取樣之前套用至材質座標。</span><span class="sxs-lookup"><span data-stu-id="ad7df-126">The third offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="ad7df-127">*Offset4* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ad7df-127">*Offset4* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad7df-128">類型： **int2**</span><span class="sxs-lookup"><span data-stu-id="ad7df-128">Type: **int2**</span></span>

<span data-ttu-id="ad7df-129">第四個位移元件會在取樣之前套用至材質座標。</span><span class="sxs-lookup"><span data-stu-id="ad7df-129">The fourth offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="ad7df-130">*狀態* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="ad7df-130">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ad7df-131">類型： **uint**</span><span class="sxs-lookup"><span data-stu-id="ad7df-131">Type: **uint**</span></span>

<span data-ttu-id="ad7df-132">作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="ad7df-132">The status of the operation.</span></span> <span data-ttu-id="ad7df-133">您無法直接存取狀態;相反地，請將狀態傳遞給 [**CheckAccessFullyMapped**](checkaccessfullymapped.md) 內建函式。</span><span class="sxs-lookup"><span data-stu-id="ad7df-133">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="ad7df-134">如果對應的 **範例**、**收集** 或 **載入** 作業中的所有值都是在 [磚資源](/windows/desktop/direct3d11/direct3d-11-2-features)中存取對應的磚， **CheckAccessFullyMapped** 會傳回 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="ad7df-134">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="ad7df-135">如果有任何值取自未對應的磚， **CheckAccessFullyMapped** 會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="ad7df-135">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad7df-136">傳回值</span><span class="sxs-lookup"><span data-stu-id="ad7df-136">Return value</span></span>

<span data-ttu-id="ad7df-137">類型： **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="ad7df-137">Type: **TemplateType**</span></span>

<span data-ttu-id="ad7df-138">四個元件的值，其類型與範本類型相同。</span><span class="sxs-lookup"><span data-stu-id="ad7df-138">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="ad7df-139">備註</span><span class="sxs-lookup"><span data-stu-id="ad7df-139">Remarks</span></span>

<span data-ttu-id="ad7df-140">紋理範例可用於雙線性插補。</span><span class="sxs-lookup"><span data-stu-id="ad7df-140">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="ad7df-141">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="ad7df-141">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="ad7df-142">頂點</span><span class="sxs-lookup"><span data-stu-id="ad7df-142">Vertex</span></span> | <span data-ttu-id="ad7df-143">船體</span><span class="sxs-lookup"><span data-stu-id="ad7df-143">Hull</span></span> | <span data-ttu-id="ad7df-144">網域</span><span class="sxs-lookup"><span data-stu-id="ad7df-144">Domain</span></span> | <span data-ttu-id="ad7df-145">幾何</span><span class="sxs-lookup"><span data-stu-id="ad7df-145">Geometry</span></span> | <span data-ttu-id="ad7df-146">像素</span><span class="sxs-lookup"><span data-stu-id="ad7df-146">Pixel</span></span> | <span data-ttu-id="ad7df-147">計算</span><span class="sxs-lookup"><span data-stu-id="ad7df-147">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="ad7df-148">x</span><span class="sxs-lookup"><span data-stu-id="ad7df-148">x</span></span>      | <span data-ttu-id="ad7df-149">x</span><span class="sxs-lookup"><span data-stu-id="ad7df-149">x</span></span>    | <span data-ttu-id="ad7df-150">x</span><span class="sxs-lookup"><span data-stu-id="ad7df-150">x</span></span>      | <span data-ttu-id="ad7df-151">x</span><span class="sxs-lookup"><span data-stu-id="ad7df-151">x</span></span>        | <span data-ttu-id="ad7df-152">x</span><span class="sxs-lookup"><span data-stu-id="ad7df-152">x</span></span>     | <span data-ttu-id="ad7df-153">x</span><span class="sxs-lookup"><span data-stu-id="ad7df-153">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="ad7df-154">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ad7df-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad7df-155">GatherCmpGreen 方法</span><span class="sxs-lookup"><span data-stu-id="ad7df-155">GatherCmpGreen methods</span></span>](texture2d-gathercmpgreen.md)
</dt> </dl>

 

 
