---
title: TextureCubeArray：： GatherAlpha (S，float，uint) 函數
description: 傳回四個材質值的 Alpha 元件，這些值會用於雙線性篩選作業，以及磚對應狀態。 |TextureCubeArray：： GatherAlpha (S，float，uint) 函數
ms.assetid: C6AF896A-C68E-44EA-A779-DD9DBA30A039
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
ms.openlocfilehash: c1f9b692d81f6e26753496bb58ac114145ed21de
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104514492"
---
# <a name="texturecubearraygatheralphasfloatuint-function"></a><span data-ttu-id="ae266-105">TextureCubeArray：： GatherAlpha (S，float，uint) 函數</span><span class="sxs-lookup"><span data-stu-id="ae266-105">TextureCubeArray::GatherAlpha(S,float,uint) function</span></span>

<span data-ttu-id="ae266-106">傳回四個材質值的 Alpha 元件，這些值會用於雙線性篩選作業，以及磚對應狀態。</span><span class="sxs-lookup"><span data-stu-id="ae266-106">Returns the alpha components of the four texel values that would be used in a bi-linear filtering operation, along with tile-mapping status.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae266-107">語法</span><span class="sxs-lookup"><span data-stu-id="ae266-107">Syntax</span></span>


``` syntax
TemplateType GatherAlpha(
  in  SamplerState S,
  in  float        Location,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="ae266-108">參數</span><span class="sxs-lookup"><span data-stu-id="ae266-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae266-109"> \[ 中的 S\]</span><span class="sxs-lookup"><span data-stu-id="ae266-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae266-110">類型： **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="ae266-110">Type: **SamplerState**</span></span>

<span data-ttu-id="ae266-111">以零為基底的取樣器索引。</span><span class="sxs-lookup"><span data-stu-id="ae266-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="ae266-112">*位置* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ae266-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae266-113">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="ae266-113">Type: **float**</span></span>

<span data-ttu-id="ae266-114">此範例會協調 (u，v) 。</span><span class="sxs-lookup"><span data-stu-id="ae266-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="ae266-115">*狀態* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="ae266-115">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ae266-116">類型： **uint**</span><span class="sxs-lookup"><span data-stu-id="ae266-116">Type: **uint**</span></span>

<span data-ttu-id="ae266-117">作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="ae266-117">The status of the operation.</span></span> <span data-ttu-id="ae266-118">您無法直接存取狀態;相反地，請將狀態傳遞給 [**CheckAccessFullyMapped**](checkaccessfullymapped.md) 內建函式。</span><span class="sxs-lookup"><span data-stu-id="ae266-118">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="ae266-119">如果對應的 **範例**、**收集** 或 **載入** 作業中的所有值都是在 [磚資源](/windows/desktop/direct3d11/direct3d-11-2-features)中存取對應的磚， **CheckAccessFullyMapped** 會傳回 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="ae266-119">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="ae266-120">如果有任何值取自未對應的磚， **CheckAccessFullyMapped** 會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="ae266-120">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae266-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="ae266-121">Return value</span></span>

<span data-ttu-id="ae266-122">類型： **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="ae266-122">Type: **TemplateType**</span></span>

<span data-ttu-id="ae266-123">四個元件的值，其類型與範本類型相同。</span><span class="sxs-lookup"><span data-stu-id="ae266-123">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="ae266-124">備註</span><span class="sxs-lookup"><span data-stu-id="ae266-124">Remarks</span></span>

<span data-ttu-id="ae266-125">紋理範例可用於雙線性插補。</span><span class="sxs-lookup"><span data-stu-id="ae266-125">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="ae266-126">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="ae266-126">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="ae266-127">頂點</span><span class="sxs-lookup"><span data-stu-id="ae266-127">Vertex</span></span> | <span data-ttu-id="ae266-128">船體</span><span class="sxs-lookup"><span data-stu-id="ae266-128">Hull</span></span> | <span data-ttu-id="ae266-129">網域</span><span class="sxs-lookup"><span data-stu-id="ae266-129">Domain</span></span> | <span data-ttu-id="ae266-130">幾何</span><span class="sxs-lookup"><span data-stu-id="ae266-130">Geometry</span></span> | <span data-ttu-id="ae266-131">像素</span><span class="sxs-lookup"><span data-stu-id="ae266-131">Pixel</span></span> | <span data-ttu-id="ae266-132">計算</span><span class="sxs-lookup"><span data-stu-id="ae266-132">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="ae266-133">x</span><span class="sxs-lookup"><span data-stu-id="ae266-133">x</span></span>      | <span data-ttu-id="ae266-134">x</span><span class="sxs-lookup"><span data-stu-id="ae266-134">x</span></span>    | <span data-ttu-id="ae266-135">x</span><span class="sxs-lookup"><span data-stu-id="ae266-135">x</span></span>      | <span data-ttu-id="ae266-136">x</span><span class="sxs-lookup"><span data-stu-id="ae266-136">x</span></span>        | <span data-ttu-id="ae266-137">x</span><span class="sxs-lookup"><span data-stu-id="ae266-137">x</span></span>     | <span data-ttu-id="ae266-138">x</span><span class="sxs-lookup"><span data-stu-id="ae266-138">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="ae266-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ae266-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae266-140">GatherAlpha 方法</span><span class="sxs-lookup"><span data-stu-id="ae266-140">GatherAlpha methods</span></span>](texturecubearray-gatheralpha.md)
</dt> <dt>

[<span data-ttu-id="ae266-141">**TextureCubeArray**</span><span class="sxs-lookup"><span data-stu-id="ae266-141">**TextureCubeArray**</span></span>](texturecubearray.md)
</dt> </dl>

 

 
