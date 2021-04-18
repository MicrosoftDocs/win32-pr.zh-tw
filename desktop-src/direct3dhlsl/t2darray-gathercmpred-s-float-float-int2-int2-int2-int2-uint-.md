---
title: Texture2DArray：： GatherCmpRed (S、float、float、int2、int2、int2、int2、uint) 函數
description: 針對在雙線性篩選作業中使用的四個材質值，會傳回其紅色元件與比較值的比較，以及磚對應狀態。 |Texture2DArray：： GatherCmpRed (S、float、float、int2、int2、int2、int2、uint) 函數
ms.assetid: E41E1328-AE31-445E-AF01-1DB201E8A278
keywords:
- GatherCmpRed 函式 HLSL
topic_type:
- apiref
api_name:
- GatherCmpRed
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 12c6e3762ed4152d1e75bcb93c67663f92e923b1
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104974361"
---
# <a name="texture2darraygathercmpredsfloatfloatint2int2int2int2uint-function"></a><span data-ttu-id="1504c-105">Texture2DArray：： GatherCmpRed (S、float、float、int2、int2、int2、int2、uint) 函數</span><span class="sxs-lookup"><span data-stu-id="1504c-105">Texture2DArray::GatherCmpRed(S,float,float,int2,int2,int2,int2,uint) function</span></span>

<span data-ttu-id="1504c-106">針對在雙線性篩選作業中使用的四個材質值，會傳回其紅色元件與比較值的比較，以及磚對應狀態。</span><span class="sxs-lookup"><span data-stu-id="1504c-106">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their red component against a compare value along with tile-mapping status.</span></span>

## <a name="syntax"></a><span data-ttu-id="1504c-107">語法</span><span class="sxs-lookup"><span data-stu-id="1504c-107">Syntax</span></span>


``` syntax
TemplateType GatherCmpRed(
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



## <a name="parameters"></a><span data-ttu-id="1504c-108">參數</span><span class="sxs-lookup"><span data-stu-id="1504c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1504c-109"> \[ 中的 S\]</span><span class="sxs-lookup"><span data-stu-id="1504c-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1504c-110">類型： **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="1504c-110">Type: **SamplerState**</span></span>

<span data-ttu-id="1504c-111">以零為基底的取樣器索引。</span><span class="sxs-lookup"><span data-stu-id="1504c-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="1504c-112">*位置* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1504c-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1504c-113">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="1504c-113">Type: **float**</span></span>

<span data-ttu-id="1504c-114">此範例會協調 (u，v) 。</span><span class="sxs-lookup"><span data-stu-id="1504c-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="1504c-115">*CompareValue* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1504c-115">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1504c-116">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="1504c-116">Type: **float**</span></span>

<span data-ttu-id="1504c-117">要針對每個取樣值進行比較的值。</span><span class="sxs-lookup"><span data-stu-id="1504c-117">A value to compare each against each sampled value.</span></span>

</dd> <dt>

<span data-ttu-id="1504c-118">*Offset1* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1504c-118">*Offset1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1504c-119">類型： **int2**</span><span class="sxs-lookup"><span data-stu-id="1504c-119">Type: **int2**</span></span>

<span data-ttu-id="1504c-120">第一個位移元件會在取樣之前套用至材質座標。</span><span class="sxs-lookup"><span data-stu-id="1504c-120">The first offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="1504c-121">*Offset2* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1504c-121">*Offset2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1504c-122">類型： **int2**</span><span class="sxs-lookup"><span data-stu-id="1504c-122">Type: **int2**</span></span>

<span data-ttu-id="1504c-123">第二個位移元件會在取樣之前套用至材質座標。</span><span class="sxs-lookup"><span data-stu-id="1504c-123">The second offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="1504c-124">*Offset3* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1504c-124">*Offset3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1504c-125">類型： **int2**</span><span class="sxs-lookup"><span data-stu-id="1504c-125">Type: **int2**</span></span>

<span data-ttu-id="1504c-126">第三個位移元件會在取樣之前套用至材質座標。</span><span class="sxs-lookup"><span data-stu-id="1504c-126">The third offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="1504c-127">*Offset4* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1504c-127">*Offset4* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1504c-128">類型： **int2**</span><span class="sxs-lookup"><span data-stu-id="1504c-128">Type: **int2**</span></span>

<span data-ttu-id="1504c-129">第四個位移元件會在取樣之前套用至材質座標。</span><span class="sxs-lookup"><span data-stu-id="1504c-129">The fourth offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="1504c-130">*狀態* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="1504c-130">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1504c-131">類型： **uint**</span><span class="sxs-lookup"><span data-stu-id="1504c-131">Type: **uint**</span></span>

<span data-ttu-id="1504c-132">作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="1504c-132">The status of the operation.</span></span> <span data-ttu-id="1504c-133">您無法直接存取狀態;相反地，請將狀態傳遞給 [**CheckAccessFullyMapped**](checkaccessfullymapped.md) 內建函式。</span><span class="sxs-lookup"><span data-stu-id="1504c-133">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="1504c-134">如果對應的 **範例**、**收集** 或 **載入** 作業中的所有值都是在 [磚資源](/windows/desktop/direct3d11/direct3d-11-2-features)中存取對應的磚， **CheckAccessFullyMapped** 會傳回 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="1504c-134">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="1504c-135">如果有任何值取自未對應的磚， **CheckAccessFullyMapped** 會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="1504c-135">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1504c-136">傳回值</span><span class="sxs-lookup"><span data-stu-id="1504c-136">Return value</span></span>

<span data-ttu-id="1504c-137">類型： **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="1504c-137">Type: **TemplateType**</span></span>

<span data-ttu-id="1504c-138">四個元件的值，其類型與範本類型相同。</span><span class="sxs-lookup"><span data-stu-id="1504c-138">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="1504c-139">備註</span><span class="sxs-lookup"><span data-stu-id="1504c-139">Remarks</span></span>

<span data-ttu-id="1504c-140">紋理範例可用於雙線性插補。</span><span class="sxs-lookup"><span data-stu-id="1504c-140">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="1504c-141">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="1504c-141">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="1504c-142">頂點</span><span class="sxs-lookup"><span data-stu-id="1504c-142">Vertex</span></span> | <span data-ttu-id="1504c-143">船體</span><span class="sxs-lookup"><span data-stu-id="1504c-143">Hull</span></span> | <span data-ttu-id="1504c-144">網域</span><span class="sxs-lookup"><span data-stu-id="1504c-144">Domain</span></span> | <span data-ttu-id="1504c-145">幾何</span><span class="sxs-lookup"><span data-stu-id="1504c-145">Geometry</span></span> | <span data-ttu-id="1504c-146">像素</span><span class="sxs-lookup"><span data-stu-id="1504c-146">Pixel</span></span> | <span data-ttu-id="1504c-147">計算</span><span class="sxs-lookup"><span data-stu-id="1504c-147">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="1504c-148">x</span><span class="sxs-lookup"><span data-stu-id="1504c-148">x</span></span>      | <span data-ttu-id="1504c-149">x</span><span class="sxs-lookup"><span data-stu-id="1504c-149">x</span></span>    | <span data-ttu-id="1504c-150">x</span><span class="sxs-lookup"><span data-stu-id="1504c-150">x</span></span>      | <span data-ttu-id="1504c-151">x</span><span class="sxs-lookup"><span data-stu-id="1504c-151">x</span></span>        | <span data-ttu-id="1504c-152">x</span><span class="sxs-lookup"><span data-stu-id="1504c-152">x</span></span>     | <span data-ttu-id="1504c-153">x</span><span class="sxs-lookup"><span data-stu-id="1504c-153">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="1504c-154">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1504c-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1504c-155">GatherCmpRed 方法</span><span class="sxs-lookup"><span data-stu-id="1504c-155">GatherCmpRed methods</span></span>](texture2darray-gathercmpred.md)
</dt> </dl>

 

 
