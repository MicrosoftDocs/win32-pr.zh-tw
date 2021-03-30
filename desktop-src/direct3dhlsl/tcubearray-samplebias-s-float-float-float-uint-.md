---
title: SampleBias：： SampleBias (S、float、float、float、uint) 函數
description: 將偏差值套用至 mipmap 層級之後，將材質取樣，並使用選擇性的值來壓 (」 LOD) 值到的範例詳細層級。 傳回操作的相關狀態。 |SampleBias：： SampleBias (S、float、float、float、uint) 函數
ms.assetid: 376F11E6-4FFF-4685-9285-9D6143C77F2D
keywords:
- SampleBias 函式 HLSL
topic_type:
- apiref
api_name:
- SampleBias
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b91491b6ff43862a8dbbdb55120f5af8f80bec85
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104974109"
---
# <a name="samplebiassamplebiassfloatfloatfloatuint-function"></a><span data-ttu-id="d59ae-106">SampleBias：： SampleBias (S、float、float、float、uint) 函數</span><span class="sxs-lookup"><span data-stu-id="d59ae-106">SampleBias::SampleBias(S,float,float,float,uint) function</span></span>

<span data-ttu-id="d59ae-107">將偏差值套用至 mipmap 層級之後，將材質取樣，並使用選擇性的值來壓 (」 LOD) 值到的範例詳細層級。</span><span class="sxs-lookup"><span data-stu-id="d59ae-107">Samples a texture, after applying the bias value to the mipmap level, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span> <span data-ttu-id="d59ae-108">傳回操作的相關狀態。</span><span class="sxs-lookup"><span data-stu-id="d59ae-108">Returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="d59ae-109">語法</span><span class="sxs-lookup"><span data-stu-id="d59ae-109">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleBias(
  in  SamplerState S,
  in  float        Location,
  in  float        Bias,
  in  float        Clamp,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="d59ae-110">參數</span><span class="sxs-lookup"><span data-stu-id="d59ae-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d59ae-111"> \[ 中的 S\]</span><span class="sxs-lookup"><span data-stu-id="d59ae-111">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d59ae-112">類型： **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="d59ae-112">Type: **SamplerState**</span></span>

<span data-ttu-id="d59ae-113">[取樣器狀態](dx-graphics-hlsl-sampler.md)。</span><span class="sxs-lookup"><span data-stu-id="d59ae-113">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="d59ae-114">這是在包含狀態指派的效果檔案中宣告的物件。</span><span class="sxs-lookup"><span data-stu-id="d59ae-114">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="d59ae-115">*位置* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d59ae-115">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d59ae-116">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="d59ae-116">Type: **float**</span></span>

<span data-ttu-id="d59ae-117">材質座標。</span><span class="sxs-lookup"><span data-stu-id="d59ae-117">The texture coordinates.</span></span> <span data-ttu-id="d59ae-118">引數類型相依于材質物件類型。</span><span class="sxs-lookup"><span data-stu-id="d59ae-118">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="d59ae-119">Texture-Object 類型</span><span class="sxs-lookup"><span data-stu-id="d59ae-119">Texture-Object Type</span></span>                    | <span data-ttu-id="d59ae-120">參數類型</span><span class="sxs-lookup"><span data-stu-id="d59ae-120">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="d59ae-121">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d59ae-121">Texture1D</span></span>                              | <span data-ttu-id="d59ae-122">FLOAT</span><span class="sxs-lookup"><span data-stu-id="d59ae-122">float</span></span>          |
| <span data-ttu-id="d59ae-123">Texture1DArray、Texture2D</span><span class="sxs-lookup"><span data-stu-id="d59ae-123">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="d59ae-124">float2</span><span class="sxs-lookup"><span data-stu-id="d59ae-124">float2</span></span>         |
| <span data-ttu-id="d59ae-125">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="d59ae-125">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="d59ae-126">float3</span><span class="sxs-lookup"><span data-stu-id="d59ae-126">float3</span></span>         |
| <span data-ttu-id="d59ae-127">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="d59ae-127">TextureCubeArray</span></span>                       | <span data-ttu-id="d59ae-128">float4</span><span class="sxs-lookup"><span data-stu-id="d59ae-128">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="d59ae-129">*偏差* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d59ae-129">*Bias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d59ae-130">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="d59ae-130">Type: **float**</span></span>

<span data-ttu-id="d59ae-131">偏差值（介於0.0 到1.0 （含）之間的浮點數）會在取樣之前套用至 mip 層級。</span><span class="sxs-lookup"><span data-stu-id="d59ae-131">The bias value, which is a floating-point number between 0.0 and 1.0 inclusive, is applied to a mip level before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="d59ae-132">*夾具* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d59ae-132">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d59ae-133">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="d59ae-133">Type: **float**</span></span>

<span data-ttu-id="d59ae-134">用來將範例」 LOD 值設為的選擇性值。</span><span class="sxs-lookup"><span data-stu-id="d59ae-134">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="d59ae-135">例如，如果您傳遞 2.0 f 作為夾具值，您可以確保沒有任何個別的範例存取小於 2.0 f 的 mip 層級。</span><span class="sxs-lookup"><span data-stu-id="d59ae-135">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> <dt>

<span data-ttu-id="d59ae-136">*狀態* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="d59ae-136">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d59ae-137">類型： **uint**</span><span class="sxs-lookup"><span data-stu-id="d59ae-137">Type: **uint**</span></span>

<span data-ttu-id="d59ae-138">作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="d59ae-138">The status of the operation.</span></span> <span data-ttu-id="d59ae-139">您無法直接存取狀態;相反地，請將狀態傳遞給 [**CheckAccessFullyMapped**](checkaccessfullymapped.md) 內建函式。</span><span class="sxs-lookup"><span data-stu-id="d59ae-139">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="d59ae-140">如果對應的 **範例**、**收集** 或 **載入** 作業中的所有值都是在 [磚資源](/windows/desktop/direct3d11/direct3d-11-2-features)中存取對應的磚， **CheckAccessFullyMapped** 會傳回 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="d59ae-140">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="d59ae-141">如果有任何值取自未對應的磚， **CheckAccessFullyMapped** 會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="d59ae-141">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d59ae-142">傳回值</span><span class="sxs-lookup"><span data-stu-id="d59ae-142">Return value</span></span>

<span data-ttu-id="d59ae-143">類型： **[ **DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="d59ae-143">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="d59ae-144">材質格式，這是以 [**DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)列出的其中一個具類型值。</span><span class="sxs-lookup"><span data-stu-id="d59ae-144">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="d59ae-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d59ae-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d59ae-146">SampleBias 方法</span><span class="sxs-lookup"><span data-stu-id="d59ae-146">SampleBias methods</span></span>](texturecubearray-samplebias.md)
</dt> <dt>

[<span data-ttu-id="d59ae-147">**TextureCubeArray**</span><span class="sxs-lookup"><span data-stu-id="d59ae-147">**TextureCubeArray**</span></span>](texturecubearray.md)
</dt> </dl>

 

 
