---
title: Texture2DArray：：搜集 (S、float、int、uint) 函數
description: 傳回要在雙線性篩選作業中使用的四個材質值。 |Texture2DArray：：搜集 (S、float、int、uint) 函數
ms.assetid: 311A5042-19AA-41C7-8B22-2E34E4554250
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
ms.openlocfilehash: a1677fae87d8bbec3c0144cc8da0b5d13f0e0ae9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104514456"
---
# <a name="texture2darraygathersfloatintuint-function"></a><span data-ttu-id="4106e-105">Texture2DArray：：搜集 (S、float、int、uint) 函數</span><span class="sxs-lookup"><span data-stu-id="4106e-105">Texture2DArray::Gather(S,float,int,uint) function</span></span>

<span data-ttu-id="4106e-106">傳回要在雙線性篩選作業中使用的四個材質值。</span><span class="sxs-lookup"><span data-stu-id="4106e-106">Returns the four texel values that would be used in a bi-linear filtering operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="4106e-107">語法</span><span class="sxs-lookup"><span data-stu-id="4106e-107">Syntax</span></span>


``` syntax
TemplateType Gather(
  in  SamplerState S,
  in  float        Location,
  in  int          Offset,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="4106e-108">參數</span><span class="sxs-lookup"><span data-stu-id="4106e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4106e-109"> \[ 中的 S\]</span><span class="sxs-lookup"><span data-stu-id="4106e-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4106e-110">類型： **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="4106e-110">Type: **SamplerState**</span></span>

<span data-ttu-id="4106e-111">以零為基底的取樣器索引。</span><span class="sxs-lookup"><span data-stu-id="4106e-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="4106e-112">*位置* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4106e-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4106e-113">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="4106e-113">Type: **float**</span></span>

<span data-ttu-id="4106e-114">此範例會協調 (u，v) 。</span><span class="sxs-lookup"><span data-stu-id="4106e-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="4106e-115">*位移* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4106e-115">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4106e-116">類型： **int**</span><span class="sxs-lookup"><span data-stu-id="4106e-116">Type: **int**</span></span>

<span data-ttu-id="4106e-117">取樣之前套用至材質座標的位移。</span><span class="sxs-lookup"><span data-stu-id="4106e-117">The offset applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="4106e-118">*狀態* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="4106e-118">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4106e-119">類型： **uint**</span><span class="sxs-lookup"><span data-stu-id="4106e-119">Type: **uint**</span></span>

<span data-ttu-id="4106e-120">作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="4106e-120">The status of the operation.</span></span> <span data-ttu-id="4106e-121">您無法直接存取狀態;相反地，請將狀態傳遞給 [**CheckAccessFullyMapped**](checkaccessfullymapped.md) 內建函式。</span><span class="sxs-lookup"><span data-stu-id="4106e-121">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="4106e-122">如果對應的 **範例**、**收集** 或 **載入** 作業中的所有值都是在 [磚資源](/windows/desktop/direct3d11/direct3d-11-2-features)中存取對應的磚， **CheckAccessFullyMapped** 會傳回 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="4106e-122">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="4106e-123">如果有任何值取自未對應的磚， **CheckAccessFullyMapped** 會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="4106e-123">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4106e-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="4106e-124">Return value</span></span>

<span data-ttu-id="4106e-125">類型： **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="4106e-125">Type: **TemplateType**</span></span>

<span data-ttu-id="4106e-126">四個元件的值，其類型與範本類型相同。</span><span class="sxs-lookup"><span data-stu-id="4106e-126">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="4106e-127">備註</span><span class="sxs-lookup"><span data-stu-id="4106e-127">Remarks</span></span>

<span data-ttu-id="4106e-128">紋理範例可用於雙線性插補。</span><span class="sxs-lookup"><span data-stu-id="4106e-128">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="4106e-129">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="4106e-129">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="4106e-130">頂點</span><span class="sxs-lookup"><span data-stu-id="4106e-130">Vertex</span></span> | <span data-ttu-id="4106e-131">船體</span><span class="sxs-lookup"><span data-stu-id="4106e-131">Hull</span></span> | <span data-ttu-id="4106e-132">網域</span><span class="sxs-lookup"><span data-stu-id="4106e-132">Domain</span></span> | <span data-ttu-id="4106e-133">幾何</span><span class="sxs-lookup"><span data-stu-id="4106e-133">Geometry</span></span> | <span data-ttu-id="4106e-134">像素</span><span class="sxs-lookup"><span data-stu-id="4106e-134">Pixel</span></span> | <span data-ttu-id="4106e-135">計算</span><span class="sxs-lookup"><span data-stu-id="4106e-135">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="4106e-136">x</span><span class="sxs-lookup"><span data-stu-id="4106e-136">x</span></span>      | <span data-ttu-id="4106e-137">x</span><span class="sxs-lookup"><span data-stu-id="4106e-137">x</span></span>    | <span data-ttu-id="4106e-138">x</span><span class="sxs-lookup"><span data-stu-id="4106e-138">x</span></span>      | <span data-ttu-id="4106e-139">x</span><span class="sxs-lookup"><span data-stu-id="4106e-139">x</span></span>        | <span data-ttu-id="4106e-140">x</span><span class="sxs-lookup"><span data-stu-id="4106e-140">x</span></span>     | <span data-ttu-id="4106e-141">x</span><span class="sxs-lookup"><span data-stu-id="4106e-141">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="4106e-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4106e-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4106e-143">收集方法</span><span class="sxs-lookup"><span data-stu-id="4106e-143">Gather methods</span></span>](texture2darray-gather.md)
</dt> </dl>

 

 
