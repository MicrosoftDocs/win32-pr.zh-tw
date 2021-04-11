---
title: Texture2DArray：： GatherAlpha (S、float、int2、int2、int2、int2、uint) 函數
description: 傳回四個材質值的 Alpha 元件，這些值會用於雙線性篩選作業，以及磚對應狀態。 |Texture2DArray：： GatherAlpha (S、float、int2、int2、int2、int2、uint) 函數
ms.assetid: 1B069708-FC77-4FD0-A264-3AB170F48D58
keywords:
- GatherAlpha 函式 HLSL
topic_type:
- apiref
api_name:
- GatherAlpha
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bb9a9911c242a678d9de5aea0d9ec7508ceb8775
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104196039"
---
# <a name="texture2darraygatheralphasfloatint2int2int2int2uint-function"></a><span data-ttu-id="c06bc-105">Texture2DArray：： GatherAlpha (S、float、int2、int2、int2、int2、uint) 函數</span><span class="sxs-lookup"><span data-stu-id="c06bc-105">Texture2DArray::GatherAlpha(S,float,int2,int2,int2,int2,uint) function</span></span>

<span data-ttu-id="c06bc-106">傳回四個材質值的 Alpha 元件，這些值會用於雙線性篩選作業，以及磚對應狀態。</span><span class="sxs-lookup"><span data-stu-id="c06bc-106">Returns the alpha components of the four texel values that would be used in a bi-linear filtering operation, along with tile-mapping status.</span></span>

## <a name="syntax"></a><span data-ttu-id="c06bc-107">語法</span><span class="sxs-lookup"><span data-stu-id="c06bc-107">Syntax</span></span>


``` syntax
TemplateType GatherAlpha(
  in  SamplerState S,
  in  float        Location,
  in  int2         Offset1,
  in  int2         Offset2,
  in  int2         Offset3,
  in  int2         Offset4,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="c06bc-108">參數</span><span class="sxs-lookup"><span data-stu-id="c06bc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c06bc-109"> \[ 中的 S\]</span><span class="sxs-lookup"><span data-stu-id="c06bc-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c06bc-110">類型： **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="c06bc-110">Type: **SamplerState**</span></span>

<span data-ttu-id="c06bc-111">以零為基底的取樣器索引。</span><span class="sxs-lookup"><span data-stu-id="c06bc-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="c06bc-112">*位置* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c06bc-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c06bc-113">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="c06bc-113">Type: **float**</span></span>

<span data-ttu-id="c06bc-114">此範例會協調 (u，v) 。</span><span class="sxs-lookup"><span data-stu-id="c06bc-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="c06bc-115">*Offset1* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c06bc-115">*Offset1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c06bc-116">類型： **int2**</span><span class="sxs-lookup"><span data-stu-id="c06bc-116">Type: **int2**</span></span>

<span data-ttu-id="c06bc-117">第一個位移元件會在取樣之前套用至材質座標。</span><span class="sxs-lookup"><span data-stu-id="c06bc-117">The first offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="c06bc-118">*Offset2* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c06bc-118">*Offset2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c06bc-119">類型： **int2**</span><span class="sxs-lookup"><span data-stu-id="c06bc-119">Type: **int2**</span></span>

<span data-ttu-id="c06bc-120">第二個位移元件會在取樣之前套用至材質座標。</span><span class="sxs-lookup"><span data-stu-id="c06bc-120">The second offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="c06bc-121">*Offset3* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c06bc-121">*Offset3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c06bc-122">類型： **int2**</span><span class="sxs-lookup"><span data-stu-id="c06bc-122">Type: **int2**</span></span>

<span data-ttu-id="c06bc-123">第三個位移元件會在取樣之前套用至材質座標。</span><span class="sxs-lookup"><span data-stu-id="c06bc-123">The third offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="c06bc-124">*Offset4* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c06bc-124">*Offset4* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c06bc-125">類型： **int2**</span><span class="sxs-lookup"><span data-stu-id="c06bc-125">Type: **int2**</span></span>

<span data-ttu-id="c06bc-126">第四個位移元件會在取樣之前套用至材質座標。</span><span class="sxs-lookup"><span data-stu-id="c06bc-126">The fourth offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="c06bc-127">*狀態* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="c06bc-127">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c06bc-128">類型： **uint**</span><span class="sxs-lookup"><span data-stu-id="c06bc-128">Type: **uint**</span></span>

<span data-ttu-id="c06bc-129">作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="c06bc-129">The status of the operation.</span></span> <span data-ttu-id="c06bc-130">您無法直接存取狀態;相反地，請將狀態傳遞給 [**CheckAccessFullyMapped**](checkaccessfullymapped.md) 內建函式。</span><span class="sxs-lookup"><span data-stu-id="c06bc-130">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="c06bc-131">如果對應的 **範例**、**收集** 或 **載入** 作業中的所有值都是在 [磚資源](/windows/desktop/direct3d11/direct3d-11-2-features)中存取對應的磚， **CheckAccessFullyMapped** 會傳回 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="c06bc-131">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="c06bc-132">如果有任何值取自未對應的磚， **CheckAccessFullyMapped** 會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="c06bc-132">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c06bc-133">傳回值</span><span class="sxs-lookup"><span data-stu-id="c06bc-133">Return value</span></span>

<span data-ttu-id="c06bc-134">類型： **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="c06bc-134">Type: **TemplateType**</span></span>

<span data-ttu-id="c06bc-135">四個元件的值，其類型與範本類型相同。</span><span class="sxs-lookup"><span data-stu-id="c06bc-135">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="c06bc-136">備註</span><span class="sxs-lookup"><span data-stu-id="c06bc-136">Remarks</span></span>

<span data-ttu-id="c06bc-137">紋理範例可用於雙線性插補。</span><span class="sxs-lookup"><span data-stu-id="c06bc-137">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="c06bc-138">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="c06bc-138">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="c06bc-139">頂點</span><span class="sxs-lookup"><span data-stu-id="c06bc-139">Vertex</span></span> | <span data-ttu-id="c06bc-140">船體</span><span class="sxs-lookup"><span data-stu-id="c06bc-140">Hull</span></span> | <span data-ttu-id="c06bc-141">網域</span><span class="sxs-lookup"><span data-stu-id="c06bc-141">Domain</span></span> | <span data-ttu-id="c06bc-142">幾何</span><span class="sxs-lookup"><span data-stu-id="c06bc-142">Geometry</span></span> | <span data-ttu-id="c06bc-143">像素</span><span class="sxs-lookup"><span data-stu-id="c06bc-143">Pixel</span></span> | <span data-ttu-id="c06bc-144">計算</span><span class="sxs-lookup"><span data-stu-id="c06bc-144">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="c06bc-145">x</span><span class="sxs-lookup"><span data-stu-id="c06bc-145">x</span></span>      | <span data-ttu-id="c06bc-146">x</span><span class="sxs-lookup"><span data-stu-id="c06bc-146">x</span></span>    | <span data-ttu-id="c06bc-147">x</span><span class="sxs-lookup"><span data-stu-id="c06bc-147">x</span></span>      | <span data-ttu-id="c06bc-148">x</span><span class="sxs-lookup"><span data-stu-id="c06bc-148">x</span></span>        | <span data-ttu-id="c06bc-149">x</span><span class="sxs-lookup"><span data-stu-id="c06bc-149">x</span></span>     | <span data-ttu-id="c06bc-150">x</span><span class="sxs-lookup"><span data-stu-id="c06bc-150">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="c06bc-151">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c06bc-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c06bc-152">GatherAlpha 方法</span><span class="sxs-lookup"><span data-stu-id="c06bc-152">GatherAlpha methods</span></span>](texture2darray-gatheralpha.md)
</dt> </dl>

 

 
