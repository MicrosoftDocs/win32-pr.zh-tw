---
title: TextureCube：： GatherCmp (S，float，float，uint) 函數
description: 針對要在雙線性篩選作業中使用的四個材質值，會傳回與比較值的比較。 |TextureCube：： GatherCmp (S，float，float，uint) 函數
ms.assetid: 655F4851-708A-478B-BB31-9DC8CDD480D0
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
ms.openlocfilehash: 827132338c3ba2b858a329ec108ef37b36ed54c2
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104974296"
---
# <a name="texturecubegathercmpsfloatfloatuint-function"></a><span data-ttu-id="55e92-105">TextureCube：： GatherCmp (S，float，float，uint) 函數</span><span class="sxs-lookup"><span data-stu-id="55e92-105">TextureCube::GatherCmp(S,float,float,uint) function</span></span>

<span data-ttu-id="55e92-106">針對要在雙線性篩選作業中使用的四個材質值，會傳回與比較值的比較。</span><span class="sxs-lookup"><span data-stu-id="55e92-106">For four texel values that would be used in a bi-linear filtering operation, returns their comparison against a compare value.</span></span>

## <a name="syntax"></a><span data-ttu-id="55e92-107">語法</span><span class="sxs-lookup"><span data-stu-id="55e92-107">Syntax</span></span>


``` syntax
TemplateType GatherCmp(
  in  SamplerState S,
  in  float        Location,
  in  float        CompareValue,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="55e92-108">參數</span><span class="sxs-lookup"><span data-stu-id="55e92-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55e92-109"> \[ 中的 S\]</span><span class="sxs-lookup"><span data-stu-id="55e92-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55e92-110">類型： **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="55e92-110">Type: **SamplerState**</span></span>

<span data-ttu-id="55e92-111">以零為基底的取樣器索引。</span><span class="sxs-lookup"><span data-stu-id="55e92-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="55e92-112">*位置* \[在\]</span><span class="sxs-lookup"><span data-stu-id="55e92-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55e92-113">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="55e92-113">Type: **float**</span></span>

<span data-ttu-id="55e92-114">此範例會協調 (u，v) 。</span><span class="sxs-lookup"><span data-stu-id="55e92-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="55e92-115">*CompareValue* \[在\]</span><span class="sxs-lookup"><span data-stu-id="55e92-115">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55e92-116">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="55e92-116">Type: **float**</span></span>

<span data-ttu-id="55e92-117">要針對每個取樣值進行比較的值。</span><span class="sxs-lookup"><span data-stu-id="55e92-117">A value to compare each against each sampled value.</span></span>

</dd> <dt>

<span data-ttu-id="55e92-118">*狀態* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="55e92-118">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="55e92-119">類型： **uint**</span><span class="sxs-lookup"><span data-stu-id="55e92-119">Type: **uint**</span></span>

<span data-ttu-id="55e92-120">作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="55e92-120">The status of the operation.</span></span> <span data-ttu-id="55e92-121">您無法直接存取狀態;相反地，請將狀態傳遞給 [**CheckAccessFullyMapped**](checkaccessfullymapped.md) 內建函式。</span><span class="sxs-lookup"><span data-stu-id="55e92-121">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="55e92-122">如果對應的 **範例**、**收集** 或 **載入** 作業中的所有值都是在 [磚資源](/windows/desktop/direct3d11/direct3d-11-2-features)中存取對應的磚， **CheckAccessFullyMapped** 會傳回 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="55e92-122">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="55e92-123">如果有任何值取自未對應的磚， **CheckAccessFullyMapped** 會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="55e92-123">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55e92-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="55e92-124">Return value</span></span>

<span data-ttu-id="55e92-125">類型： **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="55e92-125">Type: **TemplateType**</span></span>

<span data-ttu-id="55e92-126">四個元件的值，其類型與範本類型相同。</span><span class="sxs-lookup"><span data-stu-id="55e92-126">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="55e92-127">備註</span><span class="sxs-lookup"><span data-stu-id="55e92-127">Remarks</span></span>

<span data-ttu-id="55e92-128">紋理範例可用於雙線性插補。</span><span class="sxs-lookup"><span data-stu-id="55e92-128">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="55e92-129">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="55e92-129">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="55e92-130">頂點</span><span class="sxs-lookup"><span data-stu-id="55e92-130">Vertex</span></span> | <span data-ttu-id="55e92-131">船體</span><span class="sxs-lookup"><span data-stu-id="55e92-131">Hull</span></span> | <span data-ttu-id="55e92-132">網域</span><span class="sxs-lookup"><span data-stu-id="55e92-132">Domain</span></span> | <span data-ttu-id="55e92-133">幾何</span><span class="sxs-lookup"><span data-stu-id="55e92-133">Geometry</span></span> | <span data-ttu-id="55e92-134">像素</span><span class="sxs-lookup"><span data-stu-id="55e92-134">Pixel</span></span> | <span data-ttu-id="55e92-135">計算</span><span class="sxs-lookup"><span data-stu-id="55e92-135">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="55e92-136">x</span><span class="sxs-lookup"><span data-stu-id="55e92-136">x</span></span>      | <span data-ttu-id="55e92-137">x</span><span class="sxs-lookup"><span data-stu-id="55e92-137">x</span></span>    | <span data-ttu-id="55e92-138">x</span><span class="sxs-lookup"><span data-stu-id="55e92-138">x</span></span>      | <span data-ttu-id="55e92-139">x</span><span class="sxs-lookup"><span data-stu-id="55e92-139">x</span></span>        | <span data-ttu-id="55e92-140">x</span><span class="sxs-lookup"><span data-stu-id="55e92-140">x</span></span>     | <span data-ttu-id="55e92-141">x</span><span class="sxs-lookup"><span data-stu-id="55e92-141">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="55e92-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="55e92-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55e92-143">GatherCmp 方法</span><span class="sxs-lookup"><span data-stu-id="55e92-143">GatherCmp methods</span></span>](texturecube-gathercmp.md)
</dt> <dt>

[<span data-ttu-id="55e92-144">**TextureCube**</span><span class="sxs-lookup"><span data-stu-id="55e92-144">**TextureCube**</span></span>](texturecube.md)
</dt> </dl>

 

 
