---
title: Texture2DArray：： GatherGreen (S、float、int2、int2、int2、int2、uint) 函數
description: 傳回四個材質值的綠色元件，這些值會用於雙線性篩選作業，以及磚對應狀態。 |Texture2DArray：： GatherGreen (S、float、int2、int2、int2、int2、uint) 函數
ms.assetid: 994320C6-3BE5-40F9-9B9F-1913134DA71A
keywords:
- GatherGreen 函式 HLSL
topic_type:
- apiref
api_name:
- GatherGreen
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 37e307ea9be68f48b8d53b813abffb1fbfd86853
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "103853919"
---
# <a name="texture2darraygathergreensfloatint2int2int2int2uint-function"></a><span data-ttu-id="3f332-105">Texture2DArray：： GatherGreen (S、float、int2、int2、int2、int2、uint) 函數</span><span class="sxs-lookup"><span data-stu-id="3f332-105">Texture2DArray::GatherGreen(S,float,int2,int2,int2,int2,uint) function</span></span>

<span data-ttu-id="3f332-106">傳回四個材質值的綠色元件，這些值會用於雙線性篩選作業，以及磚對應狀態。</span><span class="sxs-lookup"><span data-stu-id="3f332-106">Returns the green components of the four texel values that would be used in a bi-linear filtering operation, along with tile-mapping status.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f332-107">語法</span><span class="sxs-lookup"><span data-stu-id="3f332-107">Syntax</span></span>


``` syntax
TemplateType GatherGreen(
  in  SamplerState S,
  in  float        Location,
  in  int2         Offset1,
  in  int2         Offset2,
  in  int2         Offset3,
  in  int2         Offset4,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="3f332-108">參數</span><span class="sxs-lookup"><span data-stu-id="3f332-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f332-109"> \[ 中的 S\]</span><span class="sxs-lookup"><span data-stu-id="3f332-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f332-110">類型： **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="3f332-110">Type: **SamplerState**</span></span>

<span data-ttu-id="3f332-111">以零為基底的取樣器索引。</span><span class="sxs-lookup"><span data-stu-id="3f332-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="3f332-112">*位置* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3f332-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f332-113">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="3f332-113">Type: **float**</span></span>

<span data-ttu-id="3f332-114">此範例會協調 (u，v) 。</span><span class="sxs-lookup"><span data-stu-id="3f332-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="3f332-115">*Offset1* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3f332-115">*Offset1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f332-116">類型： **int2**</span><span class="sxs-lookup"><span data-stu-id="3f332-116">Type: **int2**</span></span>

<span data-ttu-id="3f332-117">第一個位移元件會在取樣之前套用至材質座標。</span><span class="sxs-lookup"><span data-stu-id="3f332-117">The first offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="3f332-118">*Offset2* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3f332-118">*Offset2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f332-119">類型： **int2**</span><span class="sxs-lookup"><span data-stu-id="3f332-119">Type: **int2**</span></span>

<span data-ttu-id="3f332-120">第二個位移元件會在取樣之前套用至材質座標。</span><span class="sxs-lookup"><span data-stu-id="3f332-120">The second offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="3f332-121">*Offset3* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3f332-121">*Offset3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f332-122">類型： **int2**</span><span class="sxs-lookup"><span data-stu-id="3f332-122">Type: **int2**</span></span>

<span data-ttu-id="3f332-123">第三個位移元件會在取樣之前套用至材質座標。</span><span class="sxs-lookup"><span data-stu-id="3f332-123">The third offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="3f332-124">*Offset4* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3f332-124">*Offset4* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f332-125">類型： **int2**</span><span class="sxs-lookup"><span data-stu-id="3f332-125">Type: **int2**</span></span>

<span data-ttu-id="3f332-126">第四個位移元件會在取樣之前套用至材質座標。</span><span class="sxs-lookup"><span data-stu-id="3f332-126">The fourth offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="3f332-127">*狀態* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="3f332-127">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3f332-128">類型： **uint**</span><span class="sxs-lookup"><span data-stu-id="3f332-128">Type: **uint**</span></span>

<span data-ttu-id="3f332-129">作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="3f332-129">The status of the operation.</span></span> <span data-ttu-id="3f332-130">您無法直接存取狀態;相反地，請將狀態傳遞給 [**CheckAccessFullyMapped**](checkaccessfullymapped.md) 內建函式。</span><span class="sxs-lookup"><span data-stu-id="3f332-130">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="3f332-131">如果對應的 **範例**、**收集** 或 **載入** 作業中的所有值都是在 [磚資源](/windows/desktop/direct3d11/direct3d-11-2-features)中存取對應的磚， **CheckAccessFullyMapped** 會傳回 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="3f332-131">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="3f332-132">如果有任何值取自未對應的磚， **CheckAccessFullyMapped** 會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="3f332-132">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f332-133">傳回值</span><span class="sxs-lookup"><span data-stu-id="3f332-133">Return value</span></span>

<span data-ttu-id="3f332-134">類型： **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="3f332-134">Type: **TemplateType**</span></span>

<span data-ttu-id="3f332-135">四個元件的值，其類型與範本類型相同。</span><span class="sxs-lookup"><span data-stu-id="3f332-135">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="3f332-136">備註</span><span class="sxs-lookup"><span data-stu-id="3f332-136">Remarks</span></span>

<span data-ttu-id="3f332-137">紋理範例可用於雙線性插補。</span><span class="sxs-lookup"><span data-stu-id="3f332-137">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="3f332-138">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="3f332-138">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="3f332-139">頂點</span><span class="sxs-lookup"><span data-stu-id="3f332-139">Vertex</span></span> | <span data-ttu-id="3f332-140">船體</span><span class="sxs-lookup"><span data-stu-id="3f332-140">Hull</span></span> | <span data-ttu-id="3f332-141">網域</span><span class="sxs-lookup"><span data-stu-id="3f332-141">Domain</span></span> | <span data-ttu-id="3f332-142">幾何</span><span class="sxs-lookup"><span data-stu-id="3f332-142">Geometry</span></span> | <span data-ttu-id="3f332-143">像素</span><span class="sxs-lookup"><span data-stu-id="3f332-143">Pixel</span></span> | <span data-ttu-id="3f332-144">計算</span><span class="sxs-lookup"><span data-stu-id="3f332-144">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="3f332-145">x</span><span class="sxs-lookup"><span data-stu-id="3f332-145">x</span></span>      | <span data-ttu-id="3f332-146">x</span><span class="sxs-lookup"><span data-stu-id="3f332-146">x</span></span>    | <span data-ttu-id="3f332-147">x</span><span class="sxs-lookup"><span data-stu-id="3f332-147">x</span></span>      | <span data-ttu-id="3f332-148">x</span><span class="sxs-lookup"><span data-stu-id="3f332-148">x</span></span>        | <span data-ttu-id="3f332-149">x</span><span class="sxs-lookup"><span data-stu-id="3f332-149">x</span></span>     | <span data-ttu-id="3f332-150">x</span><span class="sxs-lookup"><span data-stu-id="3f332-150">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="3f332-151">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3f332-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f332-152">GatherGreen 方法</span><span class="sxs-lookup"><span data-stu-id="3f332-152">GatherGreen methods</span></span>](texture2darray-gathergreen.md)
</dt> </dl>

 

 
