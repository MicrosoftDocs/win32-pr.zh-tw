---
title: Texture2DArray：： GatherCmpRed (S、float、float、int、uint) 函數
description: 針對在雙線性篩選作業中使用的四個材質值，會傳回其紅色元件與比較值的比較，以及磚對應狀態。 |Texture2DArray：： GatherCmpRed (S、float、float、int、uint) 函數
ms.assetid: 83974A85-26CB-4724-A60F-64F214800723
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
ms.openlocfilehash: 79743d4d2b30049a580309aa79bf6b3d79c73d3f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104974349"
---
# <a name="texture2darraygathercmpredsfloatfloatintuint-function"></a><span data-ttu-id="8cda8-105">Texture2DArray：： GatherCmpRed (S、float、float、int、uint) 函數</span><span class="sxs-lookup"><span data-stu-id="8cda8-105">Texture2DArray::GatherCmpRed(S,float,float,int,uint) function</span></span>

<span data-ttu-id="8cda8-106">針對在雙線性篩選作業中使用的四個材質值，會傳回其紅色元件與比較值的比較，以及磚對應狀態。</span><span class="sxs-lookup"><span data-stu-id="8cda8-106">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their red component against a compare value along with tile-mapping status.</span></span>

## <a name="syntax"></a><span data-ttu-id="8cda8-107">語法</span><span class="sxs-lookup"><span data-stu-id="8cda8-107">Syntax</span></span>


``` syntax
TemplateType GatherCmpRed(
  in  SamplerState S,
  in  float        Location,
  in  float        CompareValue,
  in  int          Offset,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="8cda8-108">參數</span><span class="sxs-lookup"><span data-stu-id="8cda8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8cda8-109"> \[ 中的 S\]</span><span class="sxs-lookup"><span data-stu-id="8cda8-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8cda8-110">類型： **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="8cda8-110">Type: **SamplerState**</span></span>

<span data-ttu-id="8cda8-111">以零為基底的取樣器索引。</span><span class="sxs-lookup"><span data-stu-id="8cda8-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="8cda8-112">*位置* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8cda8-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8cda8-113">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="8cda8-113">Type: **float**</span></span>

<span data-ttu-id="8cda8-114">此範例會協調 (u，v) 。</span><span class="sxs-lookup"><span data-stu-id="8cda8-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="8cda8-115">*CompareValue* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8cda8-115">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8cda8-116">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="8cda8-116">Type: **float**</span></span>

<span data-ttu-id="8cda8-117">要針對每個取樣值進行比較的值。</span><span class="sxs-lookup"><span data-stu-id="8cda8-117">A value to compare each against each sampled value.</span></span>

</dd> <dt>

<span data-ttu-id="8cda8-118">*位移* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8cda8-118">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8cda8-119">類型： **int**</span><span class="sxs-lookup"><span data-stu-id="8cda8-119">Type: **int**</span></span>

<span data-ttu-id="8cda8-120">取樣之前套用至材質座標的位移。</span><span class="sxs-lookup"><span data-stu-id="8cda8-120">The offset applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="8cda8-121">*狀態* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="8cda8-121">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8cda8-122">類型： **uint**</span><span class="sxs-lookup"><span data-stu-id="8cda8-122">Type: **uint**</span></span>

<span data-ttu-id="8cda8-123">作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="8cda8-123">The status of the operation.</span></span> <span data-ttu-id="8cda8-124">您無法直接存取狀態;相反地，請將狀態傳遞給 [**CheckAccessFullyMapped**](checkaccessfullymapped.md) 內建函式。</span><span class="sxs-lookup"><span data-stu-id="8cda8-124">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="8cda8-125">如果對應的 **範例**、**收集** 或 **載入** 作業中的所有值都是在 [磚資源](/windows/desktop/direct3d11/direct3d-11-2-features)中存取對應的磚， **CheckAccessFullyMapped** 會傳回 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="8cda8-125">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="8cda8-126">如果有任何值取自未對應的磚， **CheckAccessFullyMapped** 會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="8cda8-126">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8cda8-127">傳回值</span><span class="sxs-lookup"><span data-stu-id="8cda8-127">Return value</span></span>

<span data-ttu-id="8cda8-128">類型： **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="8cda8-128">Type: **TemplateType**</span></span>

<span data-ttu-id="8cda8-129">四個元件的值，其類型與範本類型相同。</span><span class="sxs-lookup"><span data-stu-id="8cda8-129">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="8cda8-130">備註</span><span class="sxs-lookup"><span data-stu-id="8cda8-130">Remarks</span></span>

<span data-ttu-id="8cda8-131">紋理範例可用於雙線性插補。</span><span class="sxs-lookup"><span data-stu-id="8cda8-131">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="8cda8-132">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="8cda8-132">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="8cda8-133">頂點</span><span class="sxs-lookup"><span data-stu-id="8cda8-133">Vertex</span></span> | <span data-ttu-id="8cda8-134">船體</span><span class="sxs-lookup"><span data-stu-id="8cda8-134">Hull</span></span> | <span data-ttu-id="8cda8-135">網域</span><span class="sxs-lookup"><span data-stu-id="8cda8-135">Domain</span></span> | <span data-ttu-id="8cda8-136">幾何</span><span class="sxs-lookup"><span data-stu-id="8cda8-136">Geometry</span></span> | <span data-ttu-id="8cda8-137">像素</span><span class="sxs-lookup"><span data-stu-id="8cda8-137">Pixel</span></span> | <span data-ttu-id="8cda8-138">計算</span><span class="sxs-lookup"><span data-stu-id="8cda8-138">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="8cda8-139">x</span><span class="sxs-lookup"><span data-stu-id="8cda8-139">x</span></span>      | <span data-ttu-id="8cda8-140">x</span><span class="sxs-lookup"><span data-stu-id="8cda8-140">x</span></span>    | <span data-ttu-id="8cda8-141">x</span><span class="sxs-lookup"><span data-stu-id="8cda8-141">x</span></span>      | <span data-ttu-id="8cda8-142">x</span><span class="sxs-lookup"><span data-stu-id="8cda8-142">x</span></span>        | <span data-ttu-id="8cda8-143">x</span><span class="sxs-lookup"><span data-stu-id="8cda8-143">x</span></span>     | <span data-ttu-id="8cda8-144">x</span><span class="sxs-lookup"><span data-stu-id="8cda8-144">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="8cda8-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8cda8-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8cda8-146">GatherCmpRed 方法</span><span class="sxs-lookup"><span data-stu-id="8cda8-146">GatherCmpRed methods</span></span>](texture2darray-gathercmpred.md)
</dt> </dl>

 

 
