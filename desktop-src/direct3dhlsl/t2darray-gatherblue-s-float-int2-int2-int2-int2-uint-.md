---
title: Texture2DArray：： GatherBlue (S、float、int2、int2、int2、int2、uint) 函數
description: 傳回四個材質值的藍色元件，這些值會用於雙線性篩選作業，以及磚對應狀態。 |Texture2DArray：： GatherBlue (S、float、int2、int2、int2、int2、uint) 函數
ms.assetid: 82CDD092-D1C9-4FA9-BD85-65098BA457CD
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
ms.openlocfilehash: fe53bfecad3c79f3b7439e6f38effe55c4045fea
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104974060"
---
# <a name="texture2darraygatherbluesfloatint2int2int2int2uint-function"></a><span data-ttu-id="c27d2-105">Texture2DArray：： GatherBlue (S、float、int2、int2、int2、int2、uint) 函數</span><span class="sxs-lookup"><span data-stu-id="c27d2-105">Texture2DArray::GatherBlue(S,float,int2,int2,int2,int2,uint) function</span></span>

<span data-ttu-id="c27d2-106">傳回四個材質值的藍色元件，這些值會用於雙線性篩選作業，以及磚對應狀態。</span><span class="sxs-lookup"><span data-stu-id="c27d2-106">Returns the blue components of the four texel values that would be used in a bi-linear filtering operation, along with tile-mapping status.</span></span>

## <a name="syntax"></a><span data-ttu-id="c27d2-107">語法</span><span class="sxs-lookup"><span data-stu-id="c27d2-107">Syntax</span></span>


``` syntax
TemplateType GatherBlue(
  in  SamplerState S,
  in  float        Location,
  in  int2         Offset1,
  in  int2         Offset2,
  in  int2         Offset3,
  in  int2         Offset4,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="c27d2-108">參數</span><span class="sxs-lookup"><span data-stu-id="c27d2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c27d2-109"> \[ 中的 S\]</span><span class="sxs-lookup"><span data-stu-id="c27d2-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c27d2-110">類型： **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="c27d2-110">Type: **SamplerState**</span></span>

<span data-ttu-id="c27d2-111">以零為基底的取樣器索引。</span><span class="sxs-lookup"><span data-stu-id="c27d2-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="c27d2-112">*位置* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c27d2-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c27d2-113">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="c27d2-113">Type: **float**</span></span>

<span data-ttu-id="c27d2-114">此範例會協調 (u，v) 。</span><span class="sxs-lookup"><span data-stu-id="c27d2-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="c27d2-115">*Offset1* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c27d2-115">*Offset1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c27d2-116">類型： **int2**</span><span class="sxs-lookup"><span data-stu-id="c27d2-116">Type: **int2**</span></span>

<span data-ttu-id="c27d2-117">第一個位移元件會在取樣之前套用至材質座標。</span><span class="sxs-lookup"><span data-stu-id="c27d2-117">The first offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="c27d2-118">*Offset2* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c27d2-118">*Offset2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c27d2-119">類型： **int2**</span><span class="sxs-lookup"><span data-stu-id="c27d2-119">Type: **int2**</span></span>

<span data-ttu-id="c27d2-120">第二個位移元件會在取樣之前套用至材質座標。</span><span class="sxs-lookup"><span data-stu-id="c27d2-120">The second offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="c27d2-121">*Offset3* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c27d2-121">*Offset3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c27d2-122">類型： **int2**</span><span class="sxs-lookup"><span data-stu-id="c27d2-122">Type: **int2**</span></span>

<span data-ttu-id="c27d2-123">第三個位移元件會在取樣之前套用至材質座標。</span><span class="sxs-lookup"><span data-stu-id="c27d2-123">The third offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="c27d2-124">*Offset4* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c27d2-124">*Offset4* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c27d2-125">類型： **int2**</span><span class="sxs-lookup"><span data-stu-id="c27d2-125">Type: **int2**</span></span>

<span data-ttu-id="c27d2-126">第四個位移元件會在取樣之前套用至材質座標。</span><span class="sxs-lookup"><span data-stu-id="c27d2-126">The fourth offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="c27d2-127">*狀態* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="c27d2-127">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c27d2-128">類型： **uint**</span><span class="sxs-lookup"><span data-stu-id="c27d2-128">Type: **uint**</span></span>

<span data-ttu-id="c27d2-129">作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="c27d2-129">The status of the operation.</span></span> <span data-ttu-id="c27d2-130">您無法直接存取狀態;相反地，請將狀態傳遞給 [**CheckAccessFullyMapped**](checkaccessfullymapped.md) 內建函式。</span><span class="sxs-lookup"><span data-stu-id="c27d2-130">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="c27d2-131">如果對應的 **範例**、**收集** 或 **載入** 作業中的所有值都是在 [磚資源](/windows/desktop/direct3d11/direct3d-11-2-features)中存取對應的磚， **CheckAccessFullyMapped** 會傳回 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="c27d2-131">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="c27d2-132">如果有任何值取自未對應的磚， **CheckAccessFullyMapped** 會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="c27d2-132">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c27d2-133">傳回值</span><span class="sxs-lookup"><span data-stu-id="c27d2-133">Return value</span></span>

<span data-ttu-id="c27d2-134">類型： **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="c27d2-134">Type: **TemplateType**</span></span>

<span data-ttu-id="c27d2-135">四個元件的值，其類型與範本類型相同。</span><span class="sxs-lookup"><span data-stu-id="c27d2-135">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="c27d2-136">備註</span><span class="sxs-lookup"><span data-stu-id="c27d2-136">Remarks</span></span>

<span data-ttu-id="c27d2-137">紋理範例可用於雙線性插補。</span><span class="sxs-lookup"><span data-stu-id="c27d2-137">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="c27d2-138">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="c27d2-138">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="c27d2-139">頂點</span><span class="sxs-lookup"><span data-stu-id="c27d2-139">Vertex</span></span> | <span data-ttu-id="c27d2-140">船體</span><span class="sxs-lookup"><span data-stu-id="c27d2-140">Hull</span></span> | <span data-ttu-id="c27d2-141">網域</span><span class="sxs-lookup"><span data-stu-id="c27d2-141">Domain</span></span> | <span data-ttu-id="c27d2-142">幾何</span><span class="sxs-lookup"><span data-stu-id="c27d2-142">Geometry</span></span> | <span data-ttu-id="c27d2-143">像素</span><span class="sxs-lookup"><span data-stu-id="c27d2-143">Pixel</span></span> | <span data-ttu-id="c27d2-144">計算</span><span class="sxs-lookup"><span data-stu-id="c27d2-144">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="c27d2-145">x</span><span class="sxs-lookup"><span data-stu-id="c27d2-145">x</span></span>      | <span data-ttu-id="c27d2-146">x</span><span class="sxs-lookup"><span data-stu-id="c27d2-146">x</span></span>    | <span data-ttu-id="c27d2-147">x</span><span class="sxs-lookup"><span data-stu-id="c27d2-147">x</span></span>      | <span data-ttu-id="c27d2-148">x</span><span class="sxs-lookup"><span data-stu-id="c27d2-148">x</span></span>        | <span data-ttu-id="c27d2-149">x</span><span class="sxs-lookup"><span data-stu-id="c27d2-149">x</span></span>     | <span data-ttu-id="c27d2-150">x</span><span class="sxs-lookup"><span data-stu-id="c27d2-150">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="c27d2-151">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c27d2-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c27d2-152">GatherBlue 方法</span><span class="sxs-lookup"><span data-stu-id="c27d2-152">GatherBlue methods</span></span>](texture2darray-gatherblue.md)
</dt> </dl>

 

 
