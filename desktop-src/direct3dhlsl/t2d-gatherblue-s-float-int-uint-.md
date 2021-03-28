---
title: Texture2D：： GatherBlue (S，float，int，uint) 函數
description: 傳回四個材質值的藍色元件，這些值會用於雙線性篩選作業，以及磚對應狀態。 |Texture2D：： GatherBlue (S，float，int，uint) 函數
ms.assetid: 9E2A57C3-4EC4-4414-B16A-64AF759F04E9
keywords:
- GatherBlue 函式 HLSL
topic_type:
- apiref
api_name:
- GatherBlue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 68eb7676cdb74eaff1087baa7879d41d098b4ace
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104974312"
---
# <a name="texture2dgatherbluesfloatintuint-function"></a><span data-ttu-id="aebee-105">Texture2D：： GatherBlue (S，float，int，uint) 函數</span><span class="sxs-lookup"><span data-stu-id="aebee-105">Texture2D::GatherBlue(S,float,int,uint) function</span></span>

<span data-ttu-id="aebee-106">傳回四個材質值的藍色元件，這些值會用於雙線性篩選作業，以及磚對應狀態。</span><span class="sxs-lookup"><span data-stu-id="aebee-106">Returns the blue components of the four texel values that would be used in a bi-linear filtering operation, along with tile-mapping status.</span></span>

## <a name="syntax"></a><span data-ttu-id="aebee-107">語法</span><span class="sxs-lookup"><span data-stu-id="aebee-107">Syntax</span></span>


``` syntax
TemplateType GatherBlue(
  in  SamplerState S,
  in  float        Location,
  in  int          Offset,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="aebee-108">參數</span><span class="sxs-lookup"><span data-stu-id="aebee-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aebee-109"> \[ 中的 S\]</span><span class="sxs-lookup"><span data-stu-id="aebee-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aebee-110">類型： **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="aebee-110">Type: **SamplerState**</span></span>

<span data-ttu-id="aebee-111">以零為基底的取樣器索引。</span><span class="sxs-lookup"><span data-stu-id="aebee-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="aebee-112">*位置* \[在\]</span><span class="sxs-lookup"><span data-stu-id="aebee-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aebee-113">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="aebee-113">Type: **float**</span></span>

<span data-ttu-id="aebee-114">此範例會協調 (u，v) 。</span><span class="sxs-lookup"><span data-stu-id="aebee-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="aebee-115">*位移* \[在\]</span><span class="sxs-lookup"><span data-stu-id="aebee-115">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aebee-116">類型： **int**</span><span class="sxs-lookup"><span data-stu-id="aebee-116">Type: **int**</span></span>

<span data-ttu-id="aebee-117">取樣之前套用至材質座標的位移。</span><span class="sxs-lookup"><span data-stu-id="aebee-117">The offset applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="aebee-118">*狀態* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="aebee-118">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="aebee-119">類型： **uint**</span><span class="sxs-lookup"><span data-stu-id="aebee-119">Type: **uint**</span></span>

<span data-ttu-id="aebee-120">作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="aebee-120">The status of the operation.</span></span> <span data-ttu-id="aebee-121">您無法直接存取狀態;相反地，請將狀態傳遞給 [**CheckAccessFullyMapped**](checkaccessfullymapped.md) 內建函式。</span><span class="sxs-lookup"><span data-stu-id="aebee-121">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="aebee-122">如果對應的 **範例**、**收集** 或 **載入** 作業中的所有值都是在 [磚資源](/windows/desktop/direct3d11/direct3d-11-2-features)中存取對應的磚， **CheckAccessFullyMapped** 會傳回 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="aebee-122">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="aebee-123">如果有任何值取自未對應的磚， **CheckAccessFullyMapped** 會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="aebee-123">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aebee-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="aebee-124">Return value</span></span>

<span data-ttu-id="aebee-125">類型： **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="aebee-125">Type: **TemplateType**</span></span>

<span data-ttu-id="aebee-126">四個元件的值，其類型與範本類型相同。</span><span class="sxs-lookup"><span data-stu-id="aebee-126">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="aebee-127">備註</span><span class="sxs-lookup"><span data-stu-id="aebee-127">Remarks</span></span>

<span data-ttu-id="aebee-128">紋理範例可用於雙線性插補。</span><span class="sxs-lookup"><span data-stu-id="aebee-128">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="aebee-129">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="aebee-129">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="aebee-130">頂點</span><span class="sxs-lookup"><span data-stu-id="aebee-130">Vertex</span></span> | <span data-ttu-id="aebee-131">船體</span><span class="sxs-lookup"><span data-stu-id="aebee-131">Hull</span></span> | <span data-ttu-id="aebee-132">網域</span><span class="sxs-lookup"><span data-stu-id="aebee-132">Domain</span></span> | <span data-ttu-id="aebee-133">幾何</span><span class="sxs-lookup"><span data-stu-id="aebee-133">Geometry</span></span> | <span data-ttu-id="aebee-134">像素</span><span class="sxs-lookup"><span data-stu-id="aebee-134">Pixel</span></span> | <span data-ttu-id="aebee-135">計算</span><span class="sxs-lookup"><span data-stu-id="aebee-135">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="aebee-136">x</span><span class="sxs-lookup"><span data-stu-id="aebee-136">x</span></span>      | <span data-ttu-id="aebee-137">x</span><span class="sxs-lookup"><span data-stu-id="aebee-137">x</span></span>    | <span data-ttu-id="aebee-138">x</span><span class="sxs-lookup"><span data-stu-id="aebee-138">x</span></span>      | <span data-ttu-id="aebee-139">x</span><span class="sxs-lookup"><span data-stu-id="aebee-139">x</span></span>        | <span data-ttu-id="aebee-140">x</span><span class="sxs-lookup"><span data-stu-id="aebee-140">x</span></span>     | <span data-ttu-id="aebee-141">x</span><span class="sxs-lookup"><span data-stu-id="aebee-141">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="aebee-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="aebee-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aebee-143">GatherBlue 方法</span><span class="sxs-lookup"><span data-stu-id="aebee-143">GatherBlue methods</span></span>](texture2d-gatherblue.md)
</dt> </dl>

 

 
