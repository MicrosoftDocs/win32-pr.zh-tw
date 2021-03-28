---
title: TextureCubeArray 的 SampleCmp：： SampleCmp (S、float、float、float、uint) 函數
description: 使用比較值來拒絕範例，並使用選擇性的值來將範例層級 (」 LOD) 值設為，以將材質取樣。 |TextureCubeArray 的 SampleCmp：： SampleCmp (S、float、float、float、uint) 函數
ms.assetid: 5596D341-C057-414D-B1EC-7AA78693D32C
keywords:
- SampleCmp 函式 HLSL
topic_type:
- apiref
api_name:
- SampleCmp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 20626fe9d209ef4bfb64805f1a12561fd324f5a2
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/16/2021
ms.locfileid: "104992403"
---
# <a name="samplecmpsamplecmpsfloatfloatfloatuint-function-for-texturecubearray"></a><span data-ttu-id="9bdc9-105">TextureCubeArray 的 SampleCmp：： SampleCmp (S、float、float、float、uint) 函數</span><span class="sxs-lookup"><span data-stu-id="9bdc9-105">SampleCmp::SampleCmp(S,float,float,float,uint) function for TextureCubeArray</span></span>

<span data-ttu-id="9bdc9-106">使用比較值來拒絕範例，並使用選擇性的值來將範例層級 (」 LOD) 值設為，以將材質取樣。</span><span class="sxs-lookup"><span data-stu-id="9bdc9-106">Samples a texture, using a comparison value to reject samples, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span> <span data-ttu-id="9bdc9-107">傳回操作的相關狀態。</span><span class="sxs-lookup"><span data-stu-id="9bdc9-107">Returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="9bdc9-108">語法</span><span class="sxs-lookup"><span data-stu-id="9bdc9-108">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleCmp(
  in  SamplerState S,
  in  float        Location,
  in  float        CompareValue,
  in  float        Clamp,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="9bdc9-109">參數</span><span class="sxs-lookup"><span data-stu-id="9bdc9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9bdc9-110"> \[ 中的 S\]</span><span class="sxs-lookup"><span data-stu-id="9bdc9-110">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9bdc9-111">類型： **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="9bdc9-111">Type: **SamplerState**</span></span>

<span data-ttu-id="9bdc9-112">[取樣器狀態](dx-graphics-hlsl-sampler.md)。</span><span class="sxs-lookup"><span data-stu-id="9bdc9-112">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="9bdc9-113">這是在包含狀態指派的效果檔案中宣告的物件。</span><span class="sxs-lookup"><span data-stu-id="9bdc9-113">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="9bdc9-114">*位置* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9bdc9-114">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9bdc9-115">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="9bdc9-115">Type: **float**</span></span>

<span data-ttu-id="9bdc9-116">材質座標。</span><span class="sxs-lookup"><span data-stu-id="9bdc9-116">The texture coordinates.</span></span> <span data-ttu-id="9bdc9-117">引數類型相依于材質物件類型。</span><span class="sxs-lookup"><span data-stu-id="9bdc9-117">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="9bdc9-118">Texture-Object 類型</span><span class="sxs-lookup"><span data-stu-id="9bdc9-118">Texture-Object Type</span></span>                    | <span data-ttu-id="9bdc9-119">參數類型</span><span class="sxs-lookup"><span data-stu-id="9bdc9-119">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="9bdc9-120">Texture1D</span><span class="sxs-lookup"><span data-stu-id="9bdc9-120">Texture1D</span></span>                              | <span data-ttu-id="9bdc9-121">FLOAT</span><span class="sxs-lookup"><span data-stu-id="9bdc9-121">float</span></span>          |
| <span data-ttu-id="9bdc9-122">Texture1DArray、Texture2D</span><span class="sxs-lookup"><span data-stu-id="9bdc9-122">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="9bdc9-123">float2</span><span class="sxs-lookup"><span data-stu-id="9bdc9-123">float2</span></span>         |
| <span data-ttu-id="9bdc9-124">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="9bdc9-124">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="9bdc9-125">float3</span><span class="sxs-lookup"><span data-stu-id="9bdc9-125">float3</span></span>         |
| <span data-ttu-id="9bdc9-126">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="9bdc9-126">TextureCubeArray</span></span>                       | <span data-ttu-id="9bdc9-127">float4</span><span class="sxs-lookup"><span data-stu-id="9bdc9-127">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="9bdc9-128">*CompareValue* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9bdc9-128">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9bdc9-129">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="9bdc9-129">Type: **float**</span></span>

<span data-ttu-id="9bdc9-130">用來作為比較值的浮點值。</span><span class="sxs-lookup"><span data-stu-id="9bdc9-130">A floating-point value to use as a comparison value.</span></span>

</dd> <dt>

<span data-ttu-id="9bdc9-131">*夾具* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9bdc9-131">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9bdc9-132">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="9bdc9-132">Type: **float**</span></span>

<span data-ttu-id="9bdc9-133">用來將範例」 LOD 值設為的選擇性值。</span><span class="sxs-lookup"><span data-stu-id="9bdc9-133">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="9bdc9-134">例如，如果您傳遞 2.0 f 作為夾具值，您可以確保沒有任何個別的範例存取小於 2.0 f 的 mip 層級。</span><span class="sxs-lookup"><span data-stu-id="9bdc9-134">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> <dt>

<span data-ttu-id="9bdc9-135">*狀態* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="9bdc9-135">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9bdc9-136">類型： **uint**</span><span class="sxs-lookup"><span data-stu-id="9bdc9-136">Type: **uint**</span></span>

<span data-ttu-id="9bdc9-137">作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="9bdc9-137">The status of the operation.</span></span> <span data-ttu-id="9bdc9-138">您無法直接存取狀態;相反地，請將狀態傳遞給 [**CheckAccessFullyMapped**](checkaccessfullymapped.md) 內建函式。</span><span class="sxs-lookup"><span data-stu-id="9bdc9-138">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="9bdc9-139">如果對應的 **範例**、**收集** 或 **載入** 作業中的所有值都是在 [磚資源](/windows/desktop/direct3d11/direct3d-11-2-features)中存取對應的磚， **CheckAccessFullyMapped** 會傳回 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="9bdc9-139">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="9bdc9-140">如果有任何值取自未對應的磚， **CheckAccessFullyMapped** 會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="9bdc9-140">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9bdc9-141">傳回值</span><span class="sxs-lookup"><span data-stu-id="9bdc9-141">Return value</span></span>

<span data-ttu-id="9bdc9-142">類型： **[ **DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="9bdc9-142">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="9bdc9-143">材質格式，這是以 [**DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)列出的其中一個具類型值。</span><span class="sxs-lookup"><span data-stu-id="9bdc9-143">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="9bdc9-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9bdc9-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9bdc9-145">SampleCmp 方法</span><span class="sxs-lookup"><span data-stu-id="9bdc9-145">SampleCmp methods</span></span>](texturecubearray-samplecmp.md)
</dt> <dt>

[<span data-ttu-id="9bdc9-146">**TextureCubeArray**</span><span class="sxs-lookup"><span data-stu-id="9bdc9-146">**TextureCubeArray**</span></span>](texturecubearray.md)
</dt> </dl>

 

 
