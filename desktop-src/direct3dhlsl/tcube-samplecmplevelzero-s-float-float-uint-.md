---
title: TextureCube 的 SampleCmpLevelZero：： SampleCmpLevelZero (S、float、float、uint) 函數
description: 只對 mipmap 層級0進行紋理取樣，並將結果與比較值進行比較。 傳回操作的相關狀態。 適用于 TextureCube。
ms.assetid: FE40307D-B9BE-434F-A6EF-7CA3C5BC7D70
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
ms.openlocfilehash: ff58c51919e575260c71f7b58d8f3d0fda6c1dd1
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/16/2021
ms.locfileid: "104974746"
---
# <a name="samplecmplevelzerosamplecmplevelzerosfloatfloatuint-function-for-texturecube"></a><span data-ttu-id="cdd5b-106">TextureCube 的 SampleCmpLevelZero：： SampleCmpLevelZero (S、float、float、uint) 函數</span><span class="sxs-lookup"><span data-stu-id="cdd5b-106">SampleCmpLevelZero::SampleCmpLevelZero(S,float,float,uint) function for TextureCube</span></span>

<span data-ttu-id="cdd5b-107">只對 mipmap 層級0進行紋理取樣，並將結果與比較值進行比較。</span><span class="sxs-lookup"><span data-stu-id="cdd5b-107">Samples a texture on mipmap level 0 only and compares the result to a comparison value.</span></span> <span data-ttu-id="cdd5b-108">傳回操作的相關狀態。</span><span class="sxs-lookup"><span data-stu-id="cdd5b-108">Returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="cdd5b-109">語法</span><span class="sxs-lookup"><span data-stu-id="cdd5b-109">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleCmpLevelZero(
  in  SamplerState S,
  in  float        Location,
  in  float        CompareValue,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="cdd5b-110">參數</span><span class="sxs-lookup"><span data-stu-id="cdd5b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cdd5b-111"> \[ 中的 S\]</span><span class="sxs-lookup"><span data-stu-id="cdd5b-111">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cdd5b-112">類型： **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="cdd5b-112">Type: **SamplerState**</span></span>

<span data-ttu-id="cdd5b-113">[取樣器狀態](dx-graphics-hlsl-sampler.md)。</span><span class="sxs-lookup"><span data-stu-id="cdd5b-113">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="cdd5b-114">這是在包含狀態指派的效果檔案中宣告的物件。</span><span class="sxs-lookup"><span data-stu-id="cdd5b-114">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="cdd5b-115">*位置* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cdd5b-115">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cdd5b-116">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="cdd5b-116">Type: **float**</span></span>

<span data-ttu-id="cdd5b-117">材質座標。</span><span class="sxs-lookup"><span data-stu-id="cdd5b-117">The texture coordinates.</span></span> <span data-ttu-id="cdd5b-118">引數類型相依于材質物件類型。</span><span class="sxs-lookup"><span data-stu-id="cdd5b-118">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="cdd5b-119">Texture-Object 類型</span><span class="sxs-lookup"><span data-stu-id="cdd5b-119">Texture-Object Type</span></span>                    | <span data-ttu-id="cdd5b-120">參數類型</span><span class="sxs-lookup"><span data-stu-id="cdd5b-120">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="cdd5b-121">Texture1D</span><span class="sxs-lookup"><span data-stu-id="cdd5b-121">Texture1D</span></span>                              | <span data-ttu-id="cdd5b-122">FLOAT</span><span class="sxs-lookup"><span data-stu-id="cdd5b-122">float</span></span>          |
| <span data-ttu-id="cdd5b-123">Texture1DArray、Texture2D</span><span class="sxs-lookup"><span data-stu-id="cdd5b-123">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="cdd5b-124">float2</span><span class="sxs-lookup"><span data-stu-id="cdd5b-124">float2</span></span>         |
| <span data-ttu-id="cdd5b-125">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="cdd5b-125">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="cdd5b-126">float3</span><span class="sxs-lookup"><span data-stu-id="cdd5b-126">float3</span></span>         |
| <span data-ttu-id="cdd5b-127">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="cdd5b-127">TextureCubeArray</span></span>                       | <span data-ttu-id="cdd5b-128">float4</span><span class="sxs-lookup"><span data-stu-id="cdd5b-128">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="cdd5b-129">*CompareValue* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cdd5b-129">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cdd5b-130">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="cdd5b-130">Type: **float**</span></span>

<span data-ttu-id="cdd5b-131">用來作為比較值的浮點值。</span><span class="sxs-lookup"><span data-stu-id="cdd5b-131">A floating-point value to use as a comparison value.</span></span>

</dd> <dt>

<span data-ttu-id="cdd5b-132">*狀態* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="cdd5b-132">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cdd5b-133">類型： **uint**</span><span class="sxs-lookup"><span data-stu-id="cdd5b-133">Type: **uint**</span></span>

<span data-ttu-id="cdd5b-134">作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="cdd5b-134">The status of the operation.</span></span> <span data-ttu-id="cdd5b-135">您無法直接存取狀態;相反地，請將狀態傳遞給 [**CheckAccessFullyMapped**](checkaccessfullymapped.md) 內建函式。</span><span class="sxs-lookup"><span data-stu-id="cdd5b-135">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="cdd5b-136">如果對應的 **範例**、**收集** 或 **載入** 作業中的所有值都是在 [磚資源](/windows/desktop/direct3d11/direct3d-11-2-features)中存取對應的磚， **CheckAccessFullyMapped** 會傳回 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="cdd5b-136">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="cdd5b-137">如果有任何值取自未對應的磚， **CheckAccessFullyMapped** 會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="cdd5b-137">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cdd5b-138">傳回值</span><span class="sxs-lookup"><span data-stu-id="cdd5b-138">Return value</span></span>

<span data-ttu-id="cdd5b-139">類型： **[ **DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="cdd5b-139">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="cdd5b-140">材質格式，這是以 [**DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)列出的其中一個具類型值。</span><span class="sxs-lookup"><span data-stu-id="cdd5b-140">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="cdd5b-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cdd5b-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cdd5b-142">SampleCmpLevelZero 方法</span><span class="sxs-lookup"><span data-stu-id="cdd5b-142">SampleCmpLevelZero methods</span></span>](texturecube-samplecmplevelzero.md)
</dt> <dt>

[<span data-ttu-id="cdd5b-143">**TextureCube**</span><span class="sxs-lookup"><span data-stu-id="cdd5b-143">**TextureCube**</span></span>](texturecube.md)
</dt> </dl>

 

 
