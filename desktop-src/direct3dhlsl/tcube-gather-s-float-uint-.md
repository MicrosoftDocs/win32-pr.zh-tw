---
title: TextureCube：：搜集 (S、float、uint) 函數
description: 傳回要在雙線性篩選作業中使用的四個材質值。 |TextureCube：：搜集 (S、float、uint) 函數
ms.assetid: 23FA8135-ECF0-4CAE-9A1C-B05DA3676453
keywords:
- 收集函數 HLSL
topic_type:
- apiref
api_name:
- Gather
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e9710343ff9b09e4425bc133db6dab4d118d807e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104973964"
---
# <a name="texturecubegathersfloatuint-function"></a><span data-ttu-id="7147b-105">TextureCube：：搜集 (S、float、uint) 函數</span><span class="sxs-lookup"><span data-stu-id="7147b-105">TextureCube::Gather(S,float,uint) function</span></span>

<span data-ttu-id="7147b-106">傳回要在雙線性篩選作業中使用的四個材質值。</span><span class="sxs-lookup"><span data-stu-id="7147b-106">Returns the four texel values that would be used in a bi-linear filtering operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="7147b-107">語法</span><span class="sxs-lookup"><span data-stu-id="7147b-107">Syntax</span></span>


``` syntax
TemplateType Gather(
  in  SamplerState S,
  in  float        Location,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="7147b-108">參數</span><span class="sxs-lookup"><span data-stu-id="7147b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7147b-109"> \[ 中的 S\]</span><span class="sxs-lookup"><span data-stu-id="7147b-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7147b-110">類型： **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="7147b-110">Type: **SamplerState**</span></span>

<span data-ttu-id="7147b-111">以零為基底的取樣器索引。</span><span class="sxs-lookup"><span data-stu-id="7147b-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="7147b-112">*位置* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7147b-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7147b-113">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="7147b-113">Type: **float**</span></span>

<span data-ttu-id="7147b-114">此範例會協調 (u，v) 。</span><span class="sxs-lookup"><span data-stu-id="7147b-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="7147b-115">*狀態* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="7147b-115">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7147b-116">類型： **uint**</span><span class="sxs-lookup"><span data-stu-id="7147b-116">Type: **uint**</span></span>

<span data-ttu-id="7147b-117">作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="7147b-117">The status of the operation.</span></span> <span data-ttu-id="7147b-118">您無法直接存取狀態;相反地，請將狀態傳遞給 [**CheckAccessFullyMapped**](checkaccessfullymapped.md) 內建函式。</span><span class="sxs-lookup"><span data-stu-id="7147b-118">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="7147b-119">如果對應的 **範例**、**收集** 或 **載入** 作業中的所有值都是在 [磚資源](/windows/desktop/direct3d11/direct3d-11-2-features)中存取對應的磚， **CheckAccessFullyMapped** 會傳回 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="7147b-119">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="7147b-120">如果有任何值取自未對應的磚， **CheckAccessFullyMapped** 會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="7147b-120">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7147b-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="7147b-121">Return value</span></span>

<span data-ttu-id="7147b-122">類型： **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="7147b-122">Type: **TemplateType**</span></span>

<span data-ttu-id="7147b-123">四個元件的值，其類型與範本類型相同。</span><span class="sxs-lookup"><span data-stu-id="7147b-123">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="7147b-124">備註</span><span class="sxs-lookup"><span data-stu-id="7147b-124">Remarks</span></span>

<span data-ttu-id="7147b-125">紋理範例可用於雙線性插補。</span><span class="sxs-lookup"><span data-stu-id="7147b-125">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="7147b-126">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="7147b-126">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="7147b-127">頂點</span><span class="sxs-lookup"><span data-stu-id="7147b-127">Vertex</span></span> | <span data-ttu-id="7147b-128">船體</span><span class="sxs-lookup"><span data-stu-id="7147b-128">Hull</span></span> | <span data-ttu-id="7147b-129">網域</span><span class="sxs-lookup"><span data-stu-id="7147b-129">Domain</span></span> | <span data-ttu-id="7147b-130">幾何</span><span class="sxs-lookup"><span data-stu-id="7147b-130">Geometry</span></span> | <span data-ttu-id="7147b-131">像素</span><span class="sxs-lookup"><span data-stu-id="7147b-131">Pixel</span></span> | <span data-ttu-id="7147b-132">計算</span><span class="sxs-lookup"><span data-stu-id="7147b-132">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="7147b-133">x</span><span class="sxs-lookup"><span data-stu-id="7147b-133">x</span></span>      | <span data-ttu-id="7147b-134">x</span><span class="sxs-lookup"><span data-stu-id="7147b-134">x</span></span>    | <span data-ttu-id="7147b-135">x</span><span class="sxs-lookup"><span data-stu-id="7147b-135">x</span></span>      | <span data-ttu-id="7147b-136">x</span><span class="sxs-lookup"><span data-stu-id="7147b-136">x</span></span>        | <span data-ttu-id="7147b-137">x</span><span class="sxs-lookup"><span data-stu-id="7147b-137">x</span></span>     | <span data-ttu-id="7147b-138">x</span><span class="sxs-lookup"><span data-stu-id="7147b-138">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="7147b-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7147b-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7147b-140">收集方法</span><span class="sxs-lookup"><span data-stu-id="7147b-140">Gather methods</span></span>](texturecube-gather.md)
</dt> <dt>

[<span data-ttu-id="7147b-141">**TextureCube**</span><span class="sxs-lookup"><span data-stu-id="7147b-141">**TextureCube**</span></span>](texturecube.md)
</dt> </dl>

 

 
