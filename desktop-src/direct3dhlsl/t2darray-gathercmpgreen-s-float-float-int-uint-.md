---
title: Texture2DArray：： GatherCmpGreen (S、float、float、int、uint) 函數
description: 針對在雙線性篩選作業中使用的四個材質值，會傳回其綠色元件與比較值的比較，以及磚對應狀態。 |Texture2DArray：： GatherCmpGreen (S、float、float、int、uint) 函數
ms.assetid: 59DDC27B-EBC1-4C9F-8BF6-B5D82CDB1DAE
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
ms.openlocfilehash: e3c5962b74ccbbc58825bf2a8f621c220cd3b786
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104974404"
---
# <a name="texture2darraygathercmpgreensfloatfloatintuint-function"></a><span data-ttu-id="def6c-105">Texture2DArray：： GatherCmpGreen (S、float、float、int、uint) 函數</span><span class="sxs-lookup"><span data-stu-id="def6c-105">Texture2DArray::GatherCmpGreen(S,float,float,int,uint) function</span></span>

<span data-ttu-id="def6c-106">針對在雙線性篩選作業中使用的四個材質值，會傳回其綠色元件與比較值的比較，以及磚對應狀態。</span><span class="sxs-lookup"><span data-stu-id="def6c-106">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their green component against a compare value along with tile-mapping status.</span></span>

## <a name="syntax"></a><span data-ttu-id="def6c-107">語法</span><span class="sxs-lookup"><span data-stu-id="def6c-107">Syntax</span></span>


``` syntax
TemplateType GatherCmpGreen(
  in  SamplerState S,
  in  float        Location,
  in  float        CompareValue,
  in  int          Offset,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="def6c-108">參數</span><span class="sxs-lookup"><span data-stu-id="def6c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="def6c-109"> \[ 中的 S\]</span><span class="sxs-lookup"><span data-stu-id="def6c-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="def6c-110">類型： **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="def6c-110">Type: **SamplerState**</span></span>

<span data-ttu-id="def6c-111">以零為基底的取樣器索引。</span><span class="sxs-lookup"><span data-stu-id="def6c-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="def6c-112">*位置* \[在\]</span><span class="sxs-lookup"><span data-stu-id="def6c-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="def6c-113">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="def6c-113">Type: **float**</span></span>

<span data-ttu-id="def6c-114">此範例會協調 (u，v) 。</span><span class="sxs-lookup"><span data-stu-id="def6c-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="def6c-115">*CompareValue* \[在\]</span><span class="sxs-lookup"><span data-stu-id="def6c-115">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="def6c-116">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="def6c-116">Type: **float**</span></span>

<span data-ttu-id="def6c-117">要針對每個取樣值進行比較的值。</span><span class="sxs-lookup"><span data-stu-id="def6c-117">A value to compare each against each sampled value.</span></span>

</dd> <dt>

<span data-ttu-id="def6c-118">*位移* \[在\]</span><span class="sxs-lookup"><span data-stu-id="def6c-118">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="def6c-119">類型： **int**</span><span class="sxs-lookup"><span data-stu-id="def6c-119">Type: **int**</span></span>

<span data-ttu-id="def6c-120">取樣之前套用至材質座標的位移。</span><span class="sxs-lookup"><span data-stu-id="def6c-120">The offset applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="def6c-121">*狀態* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="def6c-121">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="def6c-122">類型： **uint**</span><span class="sxs-lookup"><span data-stu-id="def6c-122">Type: **uint**</span></span>

<span data-ttu-id="def6c-123">作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="def6c-123">The status of the operation.</span></span> <span data-ttu-id="def6c-124">您無法直接存取狀態;相反地，請將狀態傳遞給 [**CheckAccessFullyMapped**](checkaccessfullymapped.md) 內建函式。</span><span class="sxs-lookup"><span data-stu-id="def6c-124">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="def6c-125">如果對應的 **範例**、**收集** 或 **載入** 作業中的所有值都是在 [磚資源](/windows/desktop/direct3d11/direct3d-11-2-features)中存取對應的磚， **CheckAccessFullyMapped** 會傳回 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="def6c-125">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="def6c-126">如果有任何值取自未對應的磚， **CheckAccessFullyMapped** 會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="def6c-126">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="def6c-127">傳回值</span><span class="sxs-lookup"><span data-stu-id="def6c-127">Return value</span></span>

<span data-ttu-id="def6c-128">類型： **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="def6c-128">Type: **TemplateType**</span></span>

<span data-ttu-id="def6c-129">四個元件的值，其類型與範本類型相同。</span><span class="sxs-lookup"><span data-stu-id="def6c-129">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="def6c-130">備註</span><span class="sxs-lookup"><span data-stu-id="def6c-130">Remarks</span></span>

<span data-ttu-id="def6c-131">紋理範例可用於雙線性插補。</span><span class="sxs-lookup"><span data-stu-id="def6c-131">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="def6c-132">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="def6c-132">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="def6c-133">頂點</span><span class="sxs-lookup"><span data-stu-id="def6c-133">Vertex</span></span> | <span data-ttu-id="def6c-134">船體</span><span class="sxs-lookup"><span data-stu-id="def6c-134">Hull</span></span> | <span data-ttu-id="def6c-135">網域</span><span class="sxs-lookup"><span data-stu-id="def6c-135">Domain</span></span> | <span data-ttu-id="def6c-136">幾何</span><span class="sxs-lookup"><span data-stu-id="def6c-136">Geometry</span></span> | <span data-ttu-id="def6c-137">像素</span><span class="sxs-lookup"><span data-stu-id="def6c-137">Pixel</span></span> | <span data-ttu-id="def6c-138">計算</span><span class="sxs-lookup"><span data-stu-id="def6c-138">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="def6c-139">x</span><span class="sxs-lookup"><span data-stu-id="def6c-139">x</span></span>      | <span data-ttu-id="def6c-140">x</span><span class="sxs-lookup"><span data-stu-id="def6c-140">x</span></span>    | <span data-ttu-id="def6c-141">x</span><span class="sxs-lookup"><span data-stu-id="def6c-141">x</span></span>      | <span data-ttu-id="def6c-142">x</span><span class="sxs-lookup"><span data-stu-id="def6c-142">x</span></span>        | <span data-ttu-id="def6c-143">x</span><span class="sxs-lookup"><span data-stu-id="def6c-143">x</span></span>     | <span data-ttu-id="def6c-144">x</span><span class="sxs-lookup"><span data-stu-id="def6c-144">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="def6c-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="def6c-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="def6c-146">GatherCmpGreen 方法</span><span class="sxs-lookup"><span data-stu-id="def6c-146">GatherCmpGreen methods</span></span>](texture2darray-gathercmpgreen.md)
</dt> </dl>

 

 
