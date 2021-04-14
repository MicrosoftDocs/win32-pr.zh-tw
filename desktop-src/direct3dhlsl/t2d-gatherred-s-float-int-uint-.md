---
title: Texture2D：： GatherRed (S，float，int，uint) 函數
description: 傳回四個材質值的紅色元件，這些值會用於雙線性篩選作業，以及磚對應狀態。 |Texture2D：： GatherRed (S，float，int，uint) 函數
ms.assetid: B49F738F-FB5C-4004-A3F3-D87C566DB597
keywords:
- GatherRed 函式 HLSL
topic_type:
- apiref
api_name:
- GatherRed
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3381bb6f7388b418e22431575b9a8431ed410b2f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104992022"
---
# <a name="texture2dgatherredsfloatintuint-function"></a><span data-ttu-id="da1ac-105">Texture2D：： GatherRed (S，float，int，uint) 函數</span><span class="sxs-lookup"><span data-stu-id="da1ac-105">Texture2D::GatherRed(S,float,int,uint) function</span></span>

<span data-ttu-id="da1ac-106">傳回四個材質值的紅色元件，這些值會用於雙線性篩選作業，以及磚對應狀態。</span><span class="sxs-lookup"><span data-stu-id="da1ac-106">Returns the red components of the four texel values that would be used in a bi-linear filtering operation, along with tile-mapping status.</span></span>

## <a name="syntax"></a><span data-ttu-id="da1ac-107">語法</span><span class="sxs-lookup"><span data-stu-id="da1ac-107">Syntax</span></span>


``` syntax
TemplateType GatherRed(
  in  SamplerState S,
  in  float        Location,
  in  int          Offset,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="da1ac-108">參數</span><span class="sxs-lookup"><span data-stu-id="da1ac-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da1ac-109"> \[ 中的 S\]</span><span class="sxs-lookup"><span data-stu-id="da1ac-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da1ac-110">類型： **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="da1ac-110">Type: **SamplerState**</span></span>

<span data-ttu-id="da1ac-111">以零為基底的取樣器索引。</span><span class="sxs-lookup"><span data-stu-id="da1ac-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="da1ac-112">*位置* \[在\]</span><span class="sxs-lookup"><span data-stu-id="da1ac-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da1ac-113">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="da1ac-113">Type: **float**</span></span>

<span data-ttu-id="da1ac-114">此範例會協調 (u，v) 。</span><span class="sxs-lookup"><span data-stu-id="da1ac-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="da1ac-115">*位移* \[在\]</span><span class="sxs-lookup"><span data-stu-id="da1ac-115">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da1ac-116">類型： **int**</span><span class="sxs-lookup"><span data-stu-id="da1ac-116">Type: **int**</span></span>

<span data-ttu-id="da1ac-117">取樣之前套用至材質座標的位移。</span><span class="sxs-lookup"><span data-stu-id="da1ac-117">The offset applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="da1ac-118">*狀態* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="da1ac-118">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="da1ac-119">類型： **uint**</span><span class="sxs-lookup"><span data-stu-id="da1ac-119">Type: **uint**</span></span>

<span data-ttu-id="da1ac-120">作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="da1ac-120">The status of the operation.</span></span> <span data-ttu-id="da1ac-121">您無法直接存取狀態;相反地，請將狀態傳遞給 [**CheckAccessFullyMapped**](checkaccessfullymapped.md) 內建函式。</span><span class="sxs-lookup"><span data-stu-id="da1ac-121">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="da1ac-122">如果對應的 **範例**、**收集** 或 **載入** 作業中的所有值都是在 [磚資源](/windows/desktop/direct3d11/direct3d-11-2-features)中存取對應的磚， **CheckAccessFullyMapped** 會傳回 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="da1ac-122">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="da1ac-123">如果有任何值取自未對應的磚， **CheckAccessFullyMapped** 會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="da1ac-123">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da1ac-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="da1ac-124">Return value</span></span>

<span data-ttu-id="da1ac-125">類型： **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="da1ac-125">Type: **TemplateType**</span></span>

<span data-ttu-id="da1ac-126">四個元件的值，其類型與範本類型相同。</span><span class="sxs-lookup"><span data-stu-id="da1ac-126">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="da1ac-127">備註</span><span class="sxs-lookup"><span data-stu-id="da1ac-127">Remarks</span></span>

<span data-ttu-id="da1ac-128">紋理範例可用於雙線性插補。</span><span class="sxs-lookup"><span data-stu-id="da1ac-128">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="da1ac-129">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="da1ac-129">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="da1ac-130">頂點</span><span class="sxs-lookup"><span data-stu-id="da1ac-130">Vertex</span></span> | <span data-ttu-id="da1ac-131">船體</span><span class="sxs-lookup"><span data-stu-id="da1ac-131">Hull</span></span> | <span data-ttu-id="da1ac-132">網域</span><span class="sxs-lookup"><span data-stu-id="da1ac-132">Domain</span></span> | <span data-ttu-id="da1ac-133">幾何</span><span class="sxs-lookup"><span data-stu-id="da1ac-133">Geometry</span></span> | <span data-ttu-id="da1ac-134">像素</span><span class="sxs-lookup"><span data-stu-id="da1ac-134">Pixel</span></span> | <span data-ttu-id="da1ac-135">計算</span><span class="sxs-lookup"><span data-stu-id="da1ac-135">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="da1ac-136">x</span><span class="sxs-lookup"><span data-stu-id="da1ac-136">x</span></span>      | <span data-ttu-id="da1ac-137">x</span><span class="sxs-lookup"><span data-stu-id="da1ac-137">x</span></span>    | <span data-ttu-id="da1ac-138">x</span><span class="sxs-lookup"><span data-stu-id="da1ac-138">x</span></span>      | <span data-ttu-id="da1ac-139">x</span><span class="sxs-lookup"><span data-stu-id="da1ac-139">x</span></span>        | <span data-ttu-id="da1ac-140">x</span><span class="sxs-lookup"><span data-stu-id="da1ac-140">x</span></span>     | <span data-ttu-id="da1ac-141">x</span><span class="sxs-lookup"><span data-stu-id="da1ac-141">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="da1ac-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="da1ac-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da1ac-143">GatherRed 方法</span><span class="sxs-lookup"><span data-stu-id="da1ac-143">GatherRed methods</span></span>](texture2d-gatherred.md)
</dt> </dl>

 

 
