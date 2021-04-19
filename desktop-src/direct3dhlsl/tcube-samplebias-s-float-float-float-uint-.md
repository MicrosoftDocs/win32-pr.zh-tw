---
title: TextureCube 的 SampleBias：： SampleBias (S、float、float、float、uint) 函數
description: SampleBias：： SampleBias (S、float、float、float、uint) function for TextureCube 會在將偏差值套用至 mipmap 層級之後，進行紋理的取樣。
ms.assetid: A2F10B9B-5DF2-4389-83A9-F6A29781BF0A
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
ms.openlocfilehash: 116749acdc23bb8ac2fd057139bf8ef7c8f5ddcc
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/02/2021
ms.locfileid: "106990863"
---
# <a name="samplebiassamplebiassfloatfloatfloatuint-function-for-texturecube"></a><span data-ttu-id="89124-104">TextureCube 的 SampleBias：： SampleBias (S、float、float、float、uint) 函數</span><span class="sxs-lookup"><span data-stu-id="89124-104">SampleBias::SampleBias(S,float,float,float,uint) function for TextureCube</span></span>

<span data-ttu-id="89124-105">將偏差值套用至 mipmap 層級之後，將材質取樣，並使用選擇性的值來壓 (」 LOD) 值到的範例詳細層級。</span><span class="sxs-lookup"><span data-stu-id="89124-105">Samples a texture, after applying the bias value to the mipmap level, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span> <span data-ttu-id="89124-106">傳回操作的相關狀態。</span><span class="sxs-lookup"><span data-stu-id="89124-106">Returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="89124-107">語法</span><span class="sxs-lookup"><span data-stu-id="89124-107">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleBias(
  in  SamplerState S,
  in  float        Location,
  in  float        Bias,
  in  float        Clamp,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="89124-108">參數</span><span class="sxs-lookup"><span data-stu-id="89124-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89124-109"> \[ 中的 S\]</span><span class="sxs-lookup"><span data-stu-id="89124-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89124-110">類型： **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="89124-110">Type: **SamplerState**</span></span>

<span data-ttu-id="89124-111">[取樣器狀態](dx-graphics-hlsl-sampler.md)。</span><span class="sxs-lookup"><span data-stu-id="89124-111">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="89124-112">這是在包含狀態指派的效果檔案中宣告的物件。</span><span class="sxs-lookup"><span data-stu-id="89124-112">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="89124-113">*位置* \[在\]</span><span class="sxs-lookup"><span data-stu-id="89124-113">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89124-114">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="89124-114">Type: **float**</span></span>

<span data-ttu-id="89124-115">材質座標。</span><span class="sxs-lookup"><span data-stu-id="89124-115">The texture coordinates.</span></span> <span data-ttu-id="89124-116">引數類型相依于材質物件類型。</span><span class="sxs-lookup"><span data-stu-id="89124-116">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="89124-117">Texture-Object 類型</span><span class="sxs-lookup"><span data-stu-id="89124-117">Texture-Object Type</span></span>                    | <span data-ttu-id="89124-118">參數類型</span><span class="sxs-lookup"><span data-stu-id="89124-118">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="89124-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="89124-119">Texture1D</span></span>                              | <span data-ttu-id="89124-120">FLOAT</span><span class="sxs-lookup"><span data-stu-id="89124-120">float</span></span>          |
| <span data-ttu-id="89124-121">Texture1DArray、Texture2D</span><span class="sxs-lookup"><span data-stu-id="89124-121">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="89124-122">float2</span><span class="sxs-lookup"><span data-stu-id="89124-122">float2</span></span>         |
| <span data-ttu-id="89124-123">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="89124-123">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="89124-124">float3</span><span class="sxs-lookup"><span data-stu-id="89124-124">float3</span></span>         |
| <span data-ttu-id="89124-125">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="89124-125">TextureCubeArray</span></span>                       | <span data-ttu-id="89124-126">float4</span><span class="sxs-lookup"><span data-stu-id="89124-126">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="89124-127">*偏差* \[在\]</span><span class="sxs-lookup"><span data-stu-id="89124-127">*Bias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89124-128">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="89124-128">Type: **float**</span></span>

<span data-ttu-id="89124-129">偏差值（介於0.0 到1.0 （含）之間的浮點數）會在取樣之前套用至 mip 層級。</span><span class="sxs-lookup"><span data-stu-id="89124-129">The bias value, which is a floating-point number between 0.0 and 1.0 inclusive, is applied to a mip level before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="89124-130">*夾具* \[在\]</span><span class="sxs-lookup"><span data-stu-id="89124-130">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89124-131">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="89124-131">Type: **float**</span></span>

<span data-ttu-id="89124-132">用來將範例」 LOD 值設為的選擇性值。</span><span class="sxs-lookup"><span data-stu-id="89124-132">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="89124-133">例如，如果您傳遞 2.0 f 作為夾具值，您可以確保沒有任何個別的範例存取小於 2.0 f 的 mip 層級。</span><span class="sxs-lookup"><span data-stu-id="89124-133">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> <dt>

<span data-ttu-id="89124-134">*狀態* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="89124-134">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="89124-135">類型： **uint**</span><span class="sxs-lookup"><span data-stu-id="89124-135">Type: **uint**</span></span>

<span data-ttu-id="89124-136">作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="89124-136">The status of the operation.</span></span> <span data-ttu-id="89124-137">您無法直接存取狀態;相反地，請將狀態傳遞給 [**CheckAccessFullyMapped**](checkaccessfullymapped.md) 內建函式。</span><span class="sxs-lookup"><span data-stu-id="89124-137">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="89124-138">如果對應的 **範例**、**收集** 或 **載入** 作業中的所有值都是在 [磚資源](/windows/desktop/direct3d11/direct3d-11-2-features)中存取對應的磚， **CheckAccessFullyMapped** 會傳回 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="89124-138">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="89124-139">如果有任何值取自未對應的磚， **CheckAccessFullyMapped** 會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="89124-139">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89124-140">傳回值</span><span class="sxs-lookup"><span data-stu-id="89124-140">Return value</span></span>

<span data-ttu-id="89124-141">類型： **[ **DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="89124-141">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="89124-142">材質格式，這是以 [**DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)列出的其中一個具類型值。</span><span class="sxs-lookup"><span data-stu-id="89124-142">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="89124-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="89124-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89124-144">SampleBias 方法</span><span class="sxs-lookup"><span data-stu-id="89124-144">SampleBias methods</span></span>](texturecube-samplebias.md)
</dt> <dt>

[<span data-ttu-id="89124-145">**TextureCube**</span><span class="sxs-lookup"><span data-stu-id="89124-145">**TextureCube**</span></span>](texturecube.md)
</dt> </dl>

 

 
