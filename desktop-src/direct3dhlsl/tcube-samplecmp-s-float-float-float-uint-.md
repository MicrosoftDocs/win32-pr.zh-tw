---
title: TextureCube 的 SampleCmp：： SampleCmp (S、float、float、float、uint) 函數
description: 此函式會使用比較值來拒絕範例，並使用選擇性的值來將範例層級 (」 LOD) 值為，以進行紋理取樣。 |TextureCube 的 SampleCmp：： SampleCmp (S、float、float、float、uint) 函數
ms.assetid: 050E2856-1E93-4C69-8213-EEC082E82D40
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
ms.openlocfilehash: b73bf86b0c24feae87ea0bb4150d313fff604002
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/16/2021
ms.locfileid: "104974735"
---
# <a name="samplecmpsamplecmpsfloatfloatfloatuint-function-for-texturecube"></a><span data-ttu-id="fc1a1-105">TextureCube 的 SampleCmp：： SampleCmp (S、float、float、float、uint) 函數</span><span class="sxs-lookup"><span data-stu-id="fc1a1-105">SampleCmp::SampleCmp(S,float,float,float,uint) function for TextureCube</span></span>

<span data-ttu-id="fc1a1-106">使用比較值來拒絕範例，並使用選擇性的值來將範例層級 (」 LOD) 值設為，以將材質取樣。</span><span class="sxs-lookup"><span data-stu-id="fc1a1-106">Samples a texture, using a comparison value to reject samples, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span> <span data-ttu-id="fc1a1-107">傳回操作的相關狀態。</span><span class="sxs-lookup"><span data-stu-id="fc1a1-107">Returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc1a1-108">語法</span><span class="sxs-lookup"><span data-stu-id="fc1a1-108">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleCmp(
  in  SamplerState S,
  in  float        Location,
  in  float        CompareValue,
  in  float        Clamp,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="fc1a1-109">參數</span><span class="sxs-lookup"><span data-stu-id="fc1a1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc1a1-110"> \[ 中的 S\]</span><span class="sxs-lookup"><span data-stu-id="fc1a1-110">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc1a1-111">類型： **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="fc1a1-111">Type: **SamplerState**</span></span>

<span data-ttu-id="fc1a1-112">[取樣器狀態](dx-graphics-hlsl-sampler.md)。</span><span class="sxs-lookup"><span data-stu-id="fc1a1-112">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="fc1a1-113">這是在包含狀態指派的效果檔案中宣告的物件。</span><span class="sxs-lookup"><span data-stu-id="fc1a1-113">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="fc1a1-114">*位置* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fc1a1-114">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc1a1-115">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="fc1a1-115">Type: **float**</span></span>

<span data-ttu-id="fc1a1-116">材質座標。</span><span class="sxs-lookup"><span data-stu-id="fc1a1-116">The texture coordinates.</span></span> <span data-ttu-id="fc1a1-117">引數類型相依于材質物件類型。</span><span class="sxs-lookup"><span data-stu-id="fc1a1-117">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="fc1a1-118">Texture-Object 類型</span><span class="sxs-lookup"><span data-stu-id="fc1a1-118">Texture-Object Type</span></span>                    | <span data-ttu-id="fc1a1-119">參數類型</span><span class="sxs-lookup"><span data-stu-id="fc1a1-119">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="fc1a1-120">Texture1D</span><span class="sxs-lookup"><span data-stu-id="fc1a1-120">Texture1D</span></span>                              | <span data-ttu-id="fc1a1-121">FLOAT</span><span class="sxs-lookup"><span data-stu-id="fc1a1-121">float</span></span>          |
| <span data-ttu-id="fc1a1-122">Texture1DArray、Texture2D</span><span class="sxs-lookup"><span data-stu-id="fc1a1-122">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="fc1a1-123">float2</span><span class="sxs-lookup"><span data-stu-id="fc1a1-123">float2</span></span>         |
| <span data-ttu-id="fc1a1-124">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="fc1a1-124">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="fc1a1-125">float3</span><span class="sxs-lookup"><span data-stu-id="fc1a1-125">float3</span></span>         |
| <span data-ttu-id="fc1a1-126">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="fc1a1-126">TextureCubeArray</span></span>                       | <span data-ttu-id="fc1a1-127">float4</span><span class="sxs-lookup"><span data-stu-id="fc1a1-127">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="fc1a1-128">*CompareValue* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fc1a1-128">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc1a1-129">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="fc1a1-129">Type: **float**</span></span>

<span data-ttu-id="fc1a1-130">用來作為比較值的浮點值。</span><span class="sxs-lookup"><span data-stu-id="fc1a1-130">A floating-point value to use as a comparison value.</span></span>

</dd> <dt>

<span data-ttu-id="fc1a1-131">*夾具* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fc1a1-131">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc1a1-132">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="fc1a1-132">Type: **float**</span></span>

<span data-ttu-id="fc1a1-133">用來將範例」 LOD 值設為的選擇性值。</span><span class="sxs-lookup"><span data-stu-id="fc1a1-133">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="fc1a1-134">例如，如果您傳遞 2.0 f 作為夾具值，您可以確保沒有任何個別的範例存取小於 2.0 f 的 mip 層級。</span><span class="sxs-lookup"><span data-stu-id="fc1a1-134">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> <dt>

<span data-ttu-id="fc1a1-135">*狀態* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="fc1a1-135">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fc1a1-136">類型： **uint**</span><span class="sxs-lookup"><span data-stu-id="fc1a1-136">Type: **uint**</span></span>

<span data-ttu-id="fc1a1-137">作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="fc1a1-137">The status of the operation.</span></span> <span data-ttu-id="fc1a1-138">您無法直接存取狀態;相反地，請將狀態傳遞給 [**CheckAccessFullyMapped**](checkaccessfullymapped.md) 內建函式。</span><span class="sxs-lookup"><span data-stu-id="fc1a1-138">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="fc1a1-139">如果對應的 **範例**、**收集** 或 **載入** 作業中的所有值都是在 [磚資源](/windows/desktop/direct3d11/direct3d-11-2-features)中存取對應的磚， **CheckAccessFullyMapped** 會傳回 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="fc1a1-139">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="fc1a1-140">如果有任何值取自未對應的磚， **CheckAccessFullyMapped** 會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="fc1a1-140">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc1a1-141">傳回值</span><span class="sxs-lookup"><span data-stu-id="fc1a1-141">Return value</span></span>

<span data-ttu-id="fc1a1-142">類型： **[ **DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="fc1a1-142">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="fc1a1-143">材質格式，這是以 [**DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)列出的其中一個具類型值。</span><span class="sxs-lookup"><span data-stu-id="fc1a1-143">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="fc1a1-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fc1a1-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc1a1-145">SampleCmp 方法</span><span class="sxs-lookup"><span data-stu-id="fc1a1-145">SampleCmp methods</span></span>](texturecube-samplecmp.md)
</dt> <dt>

[<span data-ttu-id="fc1a1-146">**TextureCube**</span><span class="sxs-lookup"><span data-stu-id="fc1a1-146">**TextureCube**</span></span>](texturecube.md)
</dt> </dl>

 

 
