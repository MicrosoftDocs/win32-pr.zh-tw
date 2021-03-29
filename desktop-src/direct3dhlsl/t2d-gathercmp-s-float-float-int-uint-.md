---
title: Texture2D：： GatherCmp (S、float、float、int、uint) 函數
description: 針對要在雙線性篩選作業中使用的四個材質值，會傳回與比較值的比較，以及磚對應狀態。 |Texture2D：： GatherCmp (S、float、float、int、uint) 函數
ms.assetid: A6610587-97C3-4CE5-86A7-3411D422BC8F
keywords:
- GatherCmp 函式 HLSL
topic_type:
- apiref
api_name:
- GatherCmp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: be8246053e0f7ba6357bdd68dc59059fd225bbc8
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104974308"
---
# <a name="texture2dgathercmpsfloatfloatintuint-function"></a><span data-ttu-id="9a391-105">Texture2D：： GatherCmp (S、float、float、int、uint) 函數</span><span class="sxs-lookup"><span data-stu-id="9a391-105">Texture2D::GatherCmp(S,float,float,int,uint) function</span></span>

<span data-ttu-id="9a391-106">針對要在雙線性篩選作業中使用的四個材質值，會傳回與比較值的比較，以及磚對應狀態。</span><span class="sxs-lookup"><span data-stu-id="9a391-106">For four texel values that would be used in a bi-linear filtering operation, returns their comparison against a compare value along with tile-mapping status.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a391-107">語法</span><span class="sxs-lookup"><span data-stu-id="9a391-107">Syntax</span></span>


``` syntax
TemplateType GatherCmp(
  in  SamplerState S,
  in  float        Location,
  in  float        CompareValue,
  in  int2         Offset,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="9a391-108">參數</span><span class="sxs-lookup"><span data-stu-id="9a391-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a391-109"> \[ 中的 S\]</span><span class="sxs-lookup"><span data-stu-id="9a391-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a391-110">類型： **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="9a391-110">Type: **SamplerState**</span></span>

<span data-ttu-id="9a391-111">以零為基底的取樣器索引。</span><span class="sxs-lookup"><span data-stu-id="9a391-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="9a391-112">*位置* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9a391-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a391-113">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="9a391-113">Type: **float**</span></span>

<span data-ttu-id="9a391-114">此範例會協調 (u，v) 。</span><span class="sxs-lookup"><span data-stu-id="9a391-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="9a391-115">*CompareValue* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9a391-115">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a391-116">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="9a391-116">Type: **float**</span></span>

<span data-ttu-id="9a391-117">要針對每個取樣值進行比較的值。</span><span class="sxs-lookup"><span data-stu-id="9a391-117">A value to compare each against each sampled value.</span></span>

</dd> <dt>

<span data-ttu-id="9a391-118">*位移* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9a391-118">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a391-119">類型： **int2**</span><span class="sxs-lookup"><span data-stu-id="9a391-119">Type: **int2**</span></span>

<span data-ttu-id="9a391-120">材質中的位移會在取樣之前套用至材質座標。</span><span class="sxs-lookup"><span data-stu-id="9a391-120">The offset in texels applied to the texture coordinates before sampling.</span></span> <span data-ttu-id="9a391-121">必須是常值。</span><span class="sxs-lookup"><span data-stu-id="9a391-121">Must be a literal value.</span></span>

</dd> <dt>

<span data-ttu-id="9a391-122">*狀態* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="9a391-122">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9a391-123">類型： **uint**</span><span class="sxs-lookup"><span data-stu-id="9a391-123">Type: **uint**</span></span>

<span data-ttu-id="9a391-124">作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="9a391-124">The status of the operation.</span></span> <span data-ttu-id="9a391-125">您無法直接存取狀態;相反地，請將狀態傳遞給 [**CheckAccessFullyMapped**](checkaccessfullymapped.md) 內建函式。</span><span class="sxs-lookup"><span data-stu-id="9a391-125">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="9a391-126">如果對應的 **範例**、**收集** 或 **載入** 作業中的所有值都是在 [磚資源](/windows/desktop/direct3d11/direct3d-11-2-features)中存取對應的磚， **CheckAccessFullyMapped** 會傳回 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="9a391-126">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="9a391-127">如果有任何值取自未對應的磚， **CheckAccessFullyMapped** 會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="9a391-127">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a391-128">傳回值</span><span class="sxs-lookup"><span data-stu-id="9a391-128">Return value</span></span>

<span data-ttu-id="9a391-129">類型： **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="9a391-129">Type: **TemplateType**</span></span>

<span data-ttu-id="9a391-130">四個元件的值，其類型與範本類型相同。</span><span class="sxs-lookup"><span data-stu-id="9a391-130">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="9a391-131">備註</span><span class="sxs-lookup"><span data-stu-id="9a391-131">Remarks</span></span>

<span data-ttu-id="9a391-132">紋理範例可用於雙線性插補。</span><span class="sxs-lookup"><span data-stu-id="9a391-132">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="9a391-133">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="9a391-133">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="9a391-134">頂點</span><span class="sxs-lookup"><span data-stu-id="9a391-134">Vertex</span></span> | <span data-ttu-id="9a391-135">船體</span><span class="sxs-lookup"><span data-stu-id="9a391-135">Hull</span></span> | <span data-ttu-id="9a391-136">網域</span><span class="sxs-lookup"><span data-stu-id="9a391-136">Domain</span></span> | <span data-ttu-id="9a391-137">幾何</span><span class="sxs-lookup"><span data-stu-id="9a391-137">Geometry</span></span> | <span data-ttu-id="9a391-138">像素</span><span class="sxs-lookup"><span data-stu-id="9a391-138">Pixel</span></span> | <span data-ttu-id="9a391-139">計算</span><span class="sxs-lookup"><span data-stu-id="9a391-139">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="9a391-140">x</span><span class="sxs-lookup"><span data-stu-id="9a391-140">x</span></span>      | <span data-ttu-id="9a391-141">x</span><span class="sxs-lookup"><span data-stu-id="9a391-141">x</span></span>    | <span data-ttu-id="9a391-142">x</span><span class="sxs-lookup"><span data-stu-id="9a391-142">x</span></span>      | <span data-ttu-id="9a391-143">x</span><span class="sxs-lookup"><span data-stu-id="9a391-143">x</span></span>        | <span data-ttu-id="9a391-144">x</span><span class="sxs-lookup"><span data-stu-id="9a391-144">x</span></span>     | <span data-ttu-id="9a391-145">x</span><span class="sxs-lookup"><span data-stu-id="9a391-145">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="9a391-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9a391-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a391-147">GatherCmp 方法</span><span class="sxs-lookup"><span data-stu-id="9a391-147">GatherCmp methods</span></span>](texture2d-gathercmp.md)
</dt> </dl>

 

 
