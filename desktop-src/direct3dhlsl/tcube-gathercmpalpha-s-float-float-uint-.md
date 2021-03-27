---
title: TextureCube：： GatherCmpAlpha (S，float，float，uint) 函數
description: 針對在雙線性篩選作業中使用的四個材質值，會傳回其 Alpha 元件與比較值的比較，以及磚對應狀態。 |TextureCube：： GatherCmpAlpha (S，float，float，uint) 函數
ms.assetid: 8DC43B02-0B3C-49F0-AA94-80894A1A54BD
keywords:
- GatherCmpAlpha 函式 HLSL
topic_type:
- apiref
api_name:
- GatherCmpAlpha
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cdc4ca9f7dcbe439b9d19bbc8449347d93994e23
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "103853787"
---
# <a name="texturecubegathercmpalphasfloatfloatuint-function"></a><span data-ttu-id="d0e06-105">TextureCube：： GatherCmpAlpha (S，float，float，uint) 函數</span><span class="sxs-lookup"><span data-stu-id="d0e06-105">TextureCube::GatherCmpAlpha(S,float,float,uint) function</span></span>

<span data-ttu-id="d0e06-106">針對在雙線性篩選作業中使用的四個材質值，會傳回其 Alpha 元件與比較值的比較，以及磚對應狀態。</span><span class="sxs-lookup"><span data-stu-id="d0e06-106">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their alpha component against a compare value along with tile-mapping status.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0e06-107">語法</span><span class="sxs-lookup"><span data-stu-id="d0e06-107">Syntax</span></span>


``` syntax
TemplateType GatherCmpAlpha(
  in  SamplerState S,
  in  float        Location,
  in  float        CompareValue,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="d0e06-108">參數</span><span class="sxs-lookup"><span data-stu-id="d0e06-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0e06-109"> \[ 中的 S\]</span><span class="sxs-lookup"><span data-stu-id="d0e06-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0e06-110">類型： **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="d0e06-110">Type: **SamplerState**</span></span>

<span data-ttu-id="d0e06-111">以零為基底的取樣器索引。</span><span class="sxs-lookup"><span data-stu-id="d0e06-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="d0e06-112">*位置* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d0e06-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0e06-113">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="d0e06-113">Type: **float**</span></span>

<span data-ttu-id="d0e06-114">此範例會協調 (u，v) 。</span><span class="sxs-lookup"><span data-stu-id="d0e06-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="d0e06-115">*CompareValue* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d0e06-115">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0e06-116">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="d0e06-116">Type: **float**</span></span>

<span data-ttu-id="d0e06-117">要針對每個取樣值進行比較的值。</span><span class="sxs-lookup"><span data-stu-id="d0e06-117">A value to compare each against each sampled value.</span></span>

</dd> <dt>

<span data-ttu-id="d0e06-118">*狀態* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="d0e06-118">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d0e06-119">類型： **uint**</span><span class="sxs-lookup"><span data-stu-id="d0e06-119">Type: **uint**</span></span>

<span data-ttu-id="d0e06-120">作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="d0e06-120">The status of the operation.</span></span> <span data-ttu-id="d0e06-121">您無法直接存取狀態;相反地，請將狀態傳遞給 [**CheckAccessFullyMapped**](checkaccessfullymapped.md) 內建函式。</span><span class="sxs-lookup"><span data-stu-id="d0e06-121">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="d0e06-122">如果對應的 **範例**、**收集** 或 **載入** 作業中的所有值都是在 [磚資源](/windows/desktop/direct3d11/direct3d-11-2-features)中存取對應的磚， **CheckAccessFullyMapped** 會傳回 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="d0e06-122">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="d0e06-123">如果有任何值取自未對應的磚， **CheckAccessFullyMapped** 會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="d0e06-123">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0e06-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="d0e06-124">Return value</span></span>

<span data-ttu-id="d0e06-125">類型： **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="d0e06-125">Type: **TemplateType**</span></span>

<span data-ttu-id="d0e06-126">四個元件的值，其類型與範本類型相同。</span><span class="sxs-lookup"><span data-stu-id="d0e06-126">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="d0e06-127">備註</span><span class="sxs-lookup"><span data-stu-id="d0e06-127">Remarks</span></span>

<span data-ttu-id="d0e06-128">紋理範例可用於雙線性插補。</span><span class="sxs-lookup"><span data-stu-id="d0e06-128">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="d0e06-129">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="d0e06-129">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="d0e06-130">頂點</span><span class="sxs-lookup"><span data-stu-id="d0e06-130">Vertex</span></span> | <span data-ttu-id="d0e06-131">船體</span><span class="sxs-lookup"><span data-stu-id="d0e06-131">Hull</span></span> | <span data-ttu-id="d0e06-132">網域</span><span class="sxs-lookup"><span data-stu-id="d0e06-132">Domain</span></span> | <span data-ttu-id="d0e06-133">幾何</span><span class="sxs-lookup"><span data-stu-id="d0e06-133">Geometry</span></span> | <span data-ttu-id="d0e06-134">像素</span><span class="sxs-lookup"><span data-stu-id="d0e06-134">Pixel</span></span> | <span data-ttu-id="d0e06-135">計算</span><span class="sxs-lookup"><span data-stu-id="d0e06-135">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="d0e06-136">x</span><span class="sxs-lookup"><span data-stu-id="d0e06-136">x</span></span>      | <span data-ttu-id="d0e06-137">x</span><span class="sxs-lookup"><span data-stu-id="d0e06-137">x</span></span>    | <span data-ttu-id="d0e06-138">x</span><span class="sxs-lookup"><span data-stu-id="d0e06-138">x</span></span>      | <span data-ttu-id="d0e06-139">x</span><span class="sxs-lookup"><span data-stu-id="d0e06-139">x</span></span>        | <span data-ttu-id="d0e06-140">x</span><span class="sxs-lookup"><span data-stu-id="d0e06-140">x</span></span>     | <span data-ttu-id="d0e06-141">x</span><span class="sxs-lookup"><span data-stu-id="d0e06-141">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="d0e06-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d0e06-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0e06-143">GatherCmpAlpha 方法</span><span class="sxs-lookup"><span data-stu-id="d0e06-143">GatherCmpAlpha methods</span></span>](texturecube-gathercmpalpha.md)
</dt> <dt>

[<span data-ttu-id="d0e06-144">**TextureCube**</span><span class="sxs-lookup"><span data-stu-id="d0e06-144">**TextureCube**</span></span>](texturecube.md)
</dt> </dl>

 

 
