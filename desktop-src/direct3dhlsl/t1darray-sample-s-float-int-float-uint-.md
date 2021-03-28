---
title: Texture1DArray：： Sample (S，float，int，float，uint) 函數
description: 使用選擇性值來取樣材質，以將範例詳細資料 (」 LOD) 值，並傳回作業的狀態。 |Texture1DArray：： Sample (S，float，int，float，uint) 函數
ms.assetid: 584901B7-4F58-4491-9543-F27433386292
keywords:
- 範例函式 HLSL
topic_type:
- apiref
api_name:
- Sample
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4a2f608d7dbbd4eec51139b6f285529849f708af
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104992106"
---
# <a name="texture1darraysamplesfloatintfloatuint-function"></a><span data-ttu-id="901e5-105">Texture1DArray：： Sample (S，float，int，float，uint) 函數</span><span class="sxs-lookup"><span data-stu-id="901e5-105">Texture1DArray::Sample(S,float,int,float,uint) function</span></span>

<span data-ttu-id="901e5-106">使用選擇性值來取樣材質，以將範例詳細資料 (」 LOD) 值，並傳回作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="901e5-106">Samples a texture with an optional value to clamp sample level-of-detail (LOD) values to, and returns status of the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="901e5-107">語法</span><span class="sxs-lookup"><span data-stu-id="901e5-107">Syntax</span></span>


``` syntax
DXGI_FORMAT Sample(
  in  SamplerState S,
  in  float        Location,
  in  int          Offset,
  in  float        Clamp,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="901e5-108">參數</span><span class="sxs-lookup"><span data-stu-id="901e5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="901e5-109"> \[ 中的 S\]</span><span class="sxs-lookup"><span data-stu-id="901e5-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="901e5-110">類型： **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="901e5-110">Type: **SamplerState**</span></span>

<span data-ttu-id="901e5-111">[取樣器狀態](dx-graphics-hlsl-sampler.md)。</span><span class="sxs-lookup"><span data-stu-id="901e5-111">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="901e5-112">這是在包含狀態指派的效果檔案中宣告的物件。</span><span class="sxs-lookup"><span data-stu-id="901e5-112">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="901e5-113">*位置* \[在\]</span><span class="sxs-lookup"><span data-stu-id="901e5-113">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="901e5-114">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="901e5-114">Type: **float**</span></span>

<span data-ttu-id="901e5-115">材質座標。</span><span class="sxs-lookup"><span data-stu-id="901e5-115">The texture coordinates.</span></span> <span data-ttu-id="901e5-116">引數類型相依于材質物件類型。</span><span class="sxs-lookup"><span data-stu-id="901e5-116">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="901e5-117">Texture-Object 類型</span><span class="sxs-lookup"><span data-stu-id="901e5-117">Texture-Object Type</span></span>                    | <span data-ttu-id="901e5-118">參數類型</span><span class="sxs-lookup"><span data-stu-id="901e5-118">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="901e5-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="901e5-119">Texture1D</span></span>                              | <span data-ttu-id="901e5-120">FLOAT</span><span class="sxs-lookup"><span data-stu-id="901e5-120">float</span></span>          |
| <span data-ttu-id="901e5-121">Texture1DArray、Texture2D</span><span class="sxs-lookup"><span data-stu-id="901e5-121">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="901e5-122">float2</span><span class="sxs-lookup"><span data-stu-id="901e5-122">float2</span></span>         |
| <span data-ttu-id="901e5-123">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="901e5-123">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="901e5-124">float3</span><span class="sxs-lookup"><span data-stu-id="901e5-124">float3</span></span>         |
| <span data-ttu-id="901e5-125">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="901e5-125">TextureCubeArray</span></span>                       | <span data-ttu-id="901e5-126">float4</span><span class="sxs-lookup"><span data-stu-id="901e5-126">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="901e5-127">*位移* \[在\]</span><span class="sxs-lookup"><span data-stu-id="901e5-127">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="901e5-128">類型： **int**</span><span class="sxs-lookup"><span data-stu-id="901e5-128">Type: **int**</span></span>

<span data-ttu-id="901e5-129">選擇性的材質座標位移，可用於任何材質物件類型;位移會套用至取樣之前的位置。</span><span class="sxs-lookup"><span data-stu-id="901e5-129">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="901e5-130">只在整數 miplevel 使用位移;否則，您可能會得到無法妥善轉譯至硬體的結果。</span><span class="sxs-lookup"><span data-stu-id="901e5-130">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="901e5-131">引數類型相依于材質物件類型。</span><span class="sxs-lookup"><span data-stu-id="901e5-131">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="901e5-132">如需詳細資訊，請參閱套用 [整數位移](dx-graphics-hlsl-to-sample.md)。</span><span class="sxs-lookup"><span data-stu-id="901e5-132">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="901e5-133">Texture-Object 類型</span><span class="sxs-lookup"><span data-stu-id="901e5-133">Texture-Object Type</span></span>           | <span data-ttu-id="901e5-134">參數類型</span><span class="sxs-lookup"><span data-stu-id="901e5-134">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="901e5-135">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="901e5-135">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="901e5-136">int</span><span class="sxs-lookup"><span data-stu-id="901e5-136">int</span></span>            |
| <span data-ttu-id="901e5-137">Texture2D、Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="901e5-137">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="901e5-138">int2</span><span class="sxs-lookup"><span data-stu-id="901e5-138">int2</span></span>           |
| <span data-ttu-id="901e5-139">Texture3D</span><span class="sxs-lookup"><span data-stu-id="901e5-139">Texture3D</span></span>                     | <span data-ttu-id="901e5-140">int3</span><span class="sxs-lookup"><span data-stu-id="901e5-140">int3</span></span>           |
| <span data-ttu-id="901e5-141">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="901e5-141">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="901e5-142">不支援</span><span class="sxs-lookup"><span data-stu-id="901e5-142">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="901e5-143">*夾具* \[在\]</span><span class="sxs-lookup"><span data-stu-id="901e5-143">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="901e5-144">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="901e5-144">Type: **float**</span></span>

<span data-ttu-id="901e5-145">用來將範例」 LOD 值設為的選擇性值。</span><span class="sxs-lookup"><span data-stu-id="901e5-145">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="901e5-146">例如，如果您傳遞 2.0 f 作為夾具值，您可以確保沒有任何個別的範例存取小於 2.0 f 的 mip 層級。</span><span class="sxs-lookup"><span data-stu-id="901e5-146">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> <dt>

<span data-ttu-id="901e5-147">*狀態* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="901e5-147">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="901e5-148">類型： **uint**</span><span class="sxs-lookup"><span data-stu-id="901e5-148">Type: **uint**</span></span>

<span data-ttu-id="901e5-149">作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="901e5-149">The status of the operation.</span></span> <span data-ttu-id="901e5-150">您無法直接存取狀態;相反地，請將狀態傳遞給 [**CheckAccessFullyMapped**](checkaccessfullymapped.md) 內建函式。</span><span class="sxs-lookup"><span data-stu-id="901e5-150">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="901e5-151">如果對應的 **範例**、**收集** 或 **載入** 作業中的所有值都是在 [磚資源](/windows/desktop/direct3d11/direct3d-11-2-features)中存取對應的磚， **CheckAccessFullyMapped** 會傳回 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="901e5-151">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="901e5-152">如果有任何值取自未對應的磚， **CheckAccessFullyMapped** 會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="901e5-152">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="901e5-153">傳回值</span><span class="sxs-lookup"><span data-stu-id="901e5-153">Return value</span></span>

<span data-ttu-id="901e5-154">類型： **[ **DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="901e5-154">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="901e5-155">材質格式，這是以 [**DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)列出的其中一個具類型值。</span><span class="sxs-lookup"><span data-stu-id="901e5-155">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="901e5-156">另請參閱</span><span class="sxs-lookup"><span data-stu-id="901e5-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="901e5-157">範例方法</span><span class="sxs-lookup"><span data-stu-id="901e5-157">Sample methods</span></span>](texture1darray-sample.md)
</dt> </dl>

 

 
