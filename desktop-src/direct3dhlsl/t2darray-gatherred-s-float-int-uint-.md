---
title: Texture2DArray：： GatherRed (S，float，int，uint) 函數
description: 傳回四個材質值的紅色元件，這些值會用於雙線性篩選作業，以及磚對應狀態。 |Texture2DArray：： GatherRed (S，float，int，uint) 函數
ms.assetid: 9FAFB594-5844-4A2D-9B45-7973B5F85E13
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
ms.openlocfilehash: 7fdd250cb25f6085100bb88204cae6e67a3fc0b3
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "103696497"
---
# <a name="texture2darraygatherredsfloatintuint-function"></a><span data-ttu-id="b20eb-105">Texture2DArray：： GatherRed (S，float，int，uint) 函數</span><span class="sxs-lookup"><span data-stu-id="b20eb-105">Texture2DArray::GatherRed(S,float,int,uint) function</span></span>

<span data-ttu-id="b20eb-106">傳回四個材質值的紅色元件，這些值會用於雙線性篩選作業，以及磚對應狀態。</span><span class="sxs-lookup"><span data-stu-id="b20eb-106">Returns the red components of the four texel values that would be used in a bi-linear filtering operation, along with tile-mapping status.</span></span>

## <a name="syntax"></a><span data-ttu-id="b20eb-107">語法</span><span class="sxs-lookup"><span data-stu-id="b20eb-107">Syntax</span></span>


``` syntax
TemplateType GatherRed(
  in  SamplerState S,
  in  float        Location,
  in  int          Offset,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="b20eb-108">參數</span><span class="sxs-lookup"><span data-stu-id="b20eb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b20eb-109"> \[ 中的 S\]</span><span class="sxs-lookup"><span data-stu-id="b20eb-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b20eb-110">類型： **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="b20eb-110">Type: **SamplerState**</span></span>

<span data-ttu-id="b20eb-111">以零為基底的取樣器索引。</span><span class="sxs-lookup"><span data-stu-id="b20eb-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="b20eb-112">*位置* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b20eb-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b20eb-113">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="b20eb-113">Type: **float**</span></span>

<span data-ttu-id="b20eb-114">此範例會協調 (u，v) 。</span><span class="sxs-lookup"><span data-stu-id="b20eb-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="b20eb-115">*位移* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b20eb-115">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b20eb-116">類型： **int**</span><span class="sxs-lookup"><span data-stu-id="b20eb-116">Type: **int**</span></span>

<span data-ttu-id="b20eb-117">取樣之前套用至材質座標的位移。</span><span class="sxs-lookup"><span data-stu-id="b20eb-117">The offset applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="b20eb-118">*狀態* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="b20eb-118">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b20eb-119">類型： **uint**</span><span class="sxs-lookup"><span data-stu-id="b20eb-119">Type: **uint**</span></span>

<span data-ttu-id="b20eb-120">作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="b20eb-120">The status of the operation.</span></span> <span data-ttu-id="b20eb-121">您無法直接存取狀態;相反地，請將狀態傳遞給 [**CheckAccessFullyMapped**](checkaccessfullymapped.md) 內建函式。</span><span class="sxs-lookup"><span data-stu-id="b20eb-121">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="b20eb-122">如果對應的 **範例**、**收集** 或 **載入** 作業中的所有值都是在 [磚資源](/windows/desktop/direct3d11/direct3d-11-2-features)中存取對應的磚， **CheckAccessFullyMapped** 會傳回 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="b20eb-122">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="b20eb-123">如果有任何值取自未對應的磚， **CheckAccessFullyMapped** 會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="b20eb-123">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b20eb-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="b20eb-124">Return value</span></span>

<span data-ttu-id="b20eb-125">類型： **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="b20eb-125">Type: **TemplateType**</span></span>

<span data-ttu-id="b20eb-126">四個元件的值，其類型與範本類型相同。</span><span class="sxs-lookup"><span data-stu-id="b20eb-126">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="b20eb-127">備註</span><span class="sxs-lookup"><span data-stu-id="b20eb-127">Remarks</span></span>

<span data-ttu-id="b20eb-128">紋理範例可用於雙線性插補。</span><span class="sxs-lookup"><span data-stu-id="b20eb-128">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="b20eb-129">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="b20eb-129">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="b20eb-130">頂點</span><span class="sxs-lookup"><span data-stu-id="b20eb-130">Vertex</span></span> | <span data-ttu-id="b20eb-131">船體</span><span class="sxs-lookup"><span data-stu-id="b20eb-131">Hull</span></span> | <span data-ttu-id="b20eb-132">網域</span><span class="sxs-lookup"><span data-stu-id="b20eb-132">Domain</span></span> | <span data-ttu-id="b20eb-133">幾何</span><span class="sxs-lookup"><span data-stu-id="b20eb-133">Geometry</span></span> | <span data-ttu-id="b20eb-134">像素</span><span class="sxs-lookup"><span data-stu-id="b20eb-134">Pixel</span></span> | <span data-ttu-id="b20eb-135">計算</span><span class="sxs-lookup"><span data-stu-id="b20eb-135">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="b20eb-136">x</span><span class="sxs-lookup"><span data-stu-id="b20eb-136">x</span></span>      | <span data-ttu-id="b20eb-137">x</span><span class="sxs-lookup"><span data-stu-id="b20eb-137">x</span></span>    | <span data-ttu-id="b20eb-138">x</span><span class="sxs-lookup"><span data-stu-id="b20eb-138">x</span></span>      | <span data-ttu-id="b20eb-139">x</span><span class="sxs-lookup"><span data-stu-id="b20eb-139">x</span></span>        | <span data-ttu-id="b20eb-140">x</span><span class="sxs-lookup"><span data-stu-id="b20eb-140">x</span></span>     | <span data-ttu-id="b20eb-141">x</span><span class="sxs-lookup"><span data-stu-id="b20eb-141">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="b20eb-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b20eb-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b20eb-143">GatherRed 方法</span><span class="sxs-lookup"><span data-stu-id="b20eb-143">GatherRed methods</span></span>](texture2darray-gatherred.md)
</dt> </dl>

 

 
