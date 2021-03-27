---
title: TextureCubeArray 的 SampleCmpLevelZero：： SampleCmpLevelZero (S、float、float、uint) 函數
description: 只對 mipmap 層級0上的材質進行取樣，並比較結果與比較值，然後傳回作業的相關狀態。 適用于 TextureCubeArray。
ms.assetid: D73447C6-E77C-4027-B265-24F96C679357
keywords:
- SampleCmpLevelZero 函式 HLSL
topic_type:
- apiref
api_name:
- SampleCmpLevelZero
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ac042bd2856aa69bbba1293fb91ff74d95c0de53
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/16/2021
ms.locfileid: "103696876"
---
# <a name="samplecmplevelzerosamplecmplevelzerosfloatfloatuint-function-for-texturecubearray"></a><span data-ttu-id="8f5a7-105">TextureCubeArray 的 SampleCmpLevelZero：： SampleCmpLevelZero (S、float、float、uint) 函數</span><span class="sxs-lookup"><span data-stu-id="8f5a7-105">SampleCmpLevelZero::SampleCmpLevelZero(S,float,float,uint) function for TextureCubeArray</span></span>

<span data-ttu-id="8f5a7-106">只對 mipmap 層級0進行紋理取樣，並將結果與比較值進行比較。</span><span class="sxs-lookup"><span data-stu-id="8f5a7-106">Samples a texture on mipmap level 0 only and compares the result to a comparison value.</span></span> <span data-ttu-id="8f5a7-107">傳回操作的相關狀態。</span><span class="sxs-lookup"><span data-stu-id="8f5a7-107">Returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f5a7-108">語法</span><span class="sxs-lookup"><span data-stu-id="8f5a7-108">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleCmpLevelZero(
  in  SamplerState S,
  in  float        Location,
  in  float        CompareValue,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="8f5a7-109">參數</span><span class="sxs-lookup"><span data-stu-id="8f5a7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f5a7-110"> \[ 中的 S\]</span><span class="sxs-lookup"><span data-stu-id="8f5a7-110">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f5a7-111">類型： **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="8f5a7-111">Type: **SamplerState**</span></span>

<span data-ttu-id="8f5a7-112">[取樣器狀態](dx-graphics-hlsl-sampler.md)。</span><span class="sxs-lookup"><span data-stu-id="8f5a7-112">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="8f5a7-113">這是在包含狀態指派的效果檔案中宣告的物件。</span><span class="sxs-lookup"><span data-stu-id="8f5a7-113">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="8f5a7-114">*位置* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8f5a7-114">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f5a7-115">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="8f5a7-115">Type: **float**</span></span>

<span data-ttu-id="8f5a7-116">材質座標。</span><span class="sxs-lookup"><span data-stu-id="8f5a7-116">The texture coordinates.</span></span> <span data-ttu-id="8f5a7-117">引數類型相依于材質物件類型。</span><span class="sxs-lookup"><span data-stu-id="8f5a7-117">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="8f5a7-118">Texture-Object 類型</span><span class="sxs-lookup"><span data-stu-id="8f5a7-118">Texture-Object Type</span></span>                    | <span data-ttu-id="8f5a7-119">參數類型</span><span class="sxs-lookup"><span data-stu-id="8f5a7-119">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="8f5a7-120">Texture1D</span><span class="sxs-lookup"><span data-stu-id="8f5a7-120">Texture1D</span></span>                              | <span data-ttu-id="8f5a7-121">FLOAT</span><span class="sxs-lookup"><span data-stu-id="8f5a7-121">float</span></span>          |
| <span data-ttu-id="8f5a7-122">Texture1DArray、Texture2D</span><span class="sxs-lookup"><span data-stu-id="8f5a7-122">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="8f5a7-123">float2</span><span class="sxs-lookup"><span data-stu-id="8f5a7-123">float2</span></span>         |
| <span data-ttu-id="8f5a7-124">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="8f5a7-124">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="8f5a7-125">float3</span><span class="sxs-lookup"><span data-stu-id="8f5a7-125">float3</span></span>         |
| <span data-ttu-id="8f5a7-126">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="8f5a7-126">TextureCubeArray</span></span>                       | <span data-ttu-id="8f5a7-127">float4</span><span class="sxs-lookup"><span data-stu-id="8f5a7-127">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="8f5a7-128">*CompareValue* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8f5a7-128">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f5a7-129">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="8f5a7-129">Type: **float**</span></span>

<span data-ttu-id="8f5a7-130">用來作為比較值的浮點值。</span><span class="sxs-lookup"><span data-stu-id="8f5a7-130">A floating-point value to use as a comparison value.</span></span>

</dd> <dt>

<span data-ttu-id="8f5a7-131">*狀態* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="8f5a7-131">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8f5a7-132">類型： **uint**</span><span class="sxs-lookup"><span data-stu-id="8f5a7-132">Type: **uint**</span></span>

<span data-ttu-id="8f5a7-133">作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="8f5a7-133">The status of the operation.</span></span> <span data-ttu-id="8f5a7-134">您無法直接存取狀態;相反地，請將狀態傳遞給 [**CheckAccessFullyMapped**](checkaccessfullymapped.md) 內建函式。</span><span class="sxs-lookup"><span data-stu-id="8f5a7-134">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="8f5a7-135">如果對應的 **範例**、**收集** 或 **載入** 作業中的所有值都是在 [磚資源](/windows/desktop/direct3d11/direct3d-11-2-features)中存取對應的磚， **CheckAccessFullyMapped** 會傳回 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="8f5a7-135">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="8f5a7-136">如果有任何值取自未對應的磚， **CheckAccessFullyMapped** 會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="8f5a7-136">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f5a7-137">傳回值</span><span class="sxs-lookup"><span data-stu-id="8f5a7-137">Return value</span></span>

<span data-ttu-id="8f5a7-138">類型： **[ **DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="8f5a7-138">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="8f5a7-139">材質格式，這是以 [**DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)列出的其中一個具類型值。</span><span class="sxs-lookup"><span data-stu-id="8f5a7-139">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="8f5a7-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8f5a7-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f5a7-141">SampleCmpLevelZero 方法</span><span class="sxs-lookup"><span data-stu-id="8f5a7-141">SampleCmpLevelZero methods</span></span>](texturecubearray-samplecmplevelzero.md)
</dt> <dt>

[<span data-ttu-id="8f5a7-142">**TextureCubeArray**</span><span class="sxs-lookup"><span data-stu-id="8f5a7-142">**TextureCubeArray**</span></span>](texturecubearray.md)
</dt> </dl>

 

 
