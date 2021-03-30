---
title: Texture2DArray：： Sample (S，float，int，float，uint) 函數
description: 使用選擇性值來取樣材質，以將範例詳細資料 (」 LOD) 值，並傳回作業的狀態。 |Texture2DArray：： Sample (S，float，int，float，uint) 函數
ms.assetid: 0F9DBC0D-F35D-4A7A-B8F5-1EFBF7E14615
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
ms.openlocfilehash: e2027377a1659aa46fcf10e39f39b21e2243c943
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104973969"
---
# <a name="texture2darraysamplesfloatintfloatuint-function"></a><span data-ttu-id="03bae-105">Texture2DArray：： Sample (S，float，int，float，uint) 函數</span><span class="sxs-lookup"><span data-stu-id="03bae-105">Texture2DArray::Sample(S,float,int,float,uint) function</span></span>

<span data-ttu-id="03bae-106">使用選擇性值來取樣材質，以將範例詳細資料 (」 LOD) 值，並傳回作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="03bae-106">Samples a texture with an optional value to clamp sample level-of-detail (LOD) values to, and returns status of the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="03bae-107">語法</span><span class="sxs-lookup"><span data-stu-id="03bae-107">Syntax</span></span>


``` syntax
DXGI_FORMAT Sample(
  in  SamplerState S,
  in  float        Location,
  in  int          Offset,
  in  float        Clamp,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="03bae-108">參數</span><span class="sxs-lookup"><span data-stu-id="03bae-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03bae-109"> \[ 中的 S\]</span><span class="sxs-lookup"><span data-stu-id="03bae-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03bae-110">[取樣器狀態](dx-graphics-hlsl-sampler.md)。</span><span class="sxs-lookup"><span data-stu-id="03bae-110">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="03bae-111">這是在包含狀態指派的效果檔案中宣告的物件。</span><span class="sxs-lookup"><span data-stu-id="03bae-111">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="03bae-112">*位置* \[在\]</span><span class="sxs-lookup"><span data-stu-id="03bae-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03bae-113">材質座標。</span><span class="sxs-lookup"><span data-stu-id="03bae-113">The texture coordinates.</span></span> <span data-ttu-id="03bae-114">引數類型相依于材質物件類型。</span><span class="sxs-lookup"><span data-stu-id="03bae-114">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="03bae-115">Texture-Object 類型</span><span class="sxs-lookup"><span data-stu-id="03bae-115">Texture-Object Type</span></span>                    | <span data-ttu-id="03bae-116">參數類型</span><span class="sxs-lookup"><span data-stu-id="03bae-116">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="03bae-117">Texture1D</span><span class="sxs-lookup"><span data-stu-id="03bae-117">Texture1D</span></span>                              | <span data-ttu-id="03bae-118">FLOAT</span><span class="sxs-lookup"><span data-stu-id="03bae-118">float</span></span>          |
| <span data-ttu-id="03bae-119">Texture1DArray、Texture2D</span><span class="sxs-lookup"><span data-stu-id="03bae-119">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="03bae-120">float2</span><span class="sxs-lookup"><span data-stu-id="03bae-120">float2</span></span>         |
| <span data-ttu-id="03bae-121">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="03bae-121">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="03bae-122">float3</span><span class="sxs-lookup"><span data-stu-id="03bae-122">float3</span></span>         |
| <span data-ttu-id="03bae-123">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="03bae-123">TextureCubeArray</span></span>                       | <span data-ttu-id="03bae-124">float4</span><span class="sxs-lookup"><span data-stu-id="03bae-124">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="03bae-125">*位移* \[在\]</span><span class="sxs-lookup"><span data-stu-id="03bae-125">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03bae-126">選擇性的材質座標位移，可用於任何材質物件類型;位移會套用至取樣之前的位置。</span><span class="sxs-lookup"><span data-stu-id="03bae-126">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="03bae-127">只在整數 miplevel 使用位移;否則，您可能會得到無法妥善轉譯至硬體的結果。</span><span class="sxs-lookup"><span data-stu-id="03bae-127">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="03bae-128">引數類型相依于材質物件類型。</span><span class="sxs-lookup"><span data-stu-id="03bae-128">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="03bae-129">如需詳細資訊，請參閱套用 [整數位移](dx-graphics-hlsl-to-sample.md)。</span><span class="sxs-lookup"><span data-stu-id="03bae-129">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="03bae-130">Texture-Object 類型</span><span class="sxs-lookup"><span data-stu-id="03bae-130">Texture-Object Type</span></span>           | <span data-ttu-id="03bae-131">參數類型</span><span class="sxs-lookup"><span data-stu-id="03bae-131">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="03bae-132">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="03bae-132">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="03bae-133">int</span><span class="sxs-lookup"><span data-stu-id="03bae-133">int</span></span>            |
| <span data-ttu-id="03bae-134">Texture2D、Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="03bae-134">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="03bae-135">int2</span><span class="sxs-lookup"><span data-stu-id="03bae-135">int2</span></span>           |
| <span data-ttu-id="03bae-136">Texture3D</span><span class="sxs-lookup"><span data-stu-id="03bae-136">Texture3D</span></span>                     | <span data-ttu-id="03bae-137">int3</span><span class="sxs-lookup"><span data-stu-id="03bae-137">int3</span></span>           |
| <span data-ttu-id="03bae-138">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="03bae-138">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="03bae-139">不支援</span><span class="sxs-lookup"><span data-stu-id="03bae-139">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="03bae-140">*夾具* \[在\]</span><span class="sxs-lookup"><span data-stu-id="03bae-140">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03bae-141">用來將範例」 LOD 值設為的選擇性值。</span><span class="sxs-lookup"><span data-stu-id="03bae-141">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="03bae-142">例如，如果您傳遞 2.0 f 作為夾具值，您可以確保沒有任何個別的範例存取小於 2.0 f 的 mip 層級。</span><span class="sxs-lookup"><span data-stu-id="03bae-142">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> <dt>

<span data-ttu-id="03bae-143">*狀態* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="03bae-143">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="03bae-144">作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="03bae-144">The status of the operation.</span></span> <span data-ttu-id="03bae-145">您無法直接存取狀態;相反地，請將狀態傳遞給 [**CheckAccessFullyMapped**](checkaccessfullymapped.md) 內建函式。</span><span class="sxs-lookup"><span data-stu-id="03bae-145">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="03bae-146">如果對應的 **範例**、**收集** 或 **載入** 作業中的所有值都是在 [磚資源](/windows/desktop/direct3d11/direct3d-11-2-features)中存取對應的磚， **CheckAccessFullyMapped** 會傳回 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="03bae-146">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="03bae-147">如果有任何值取自未對應的磚， **CheckAccessFullyMapped** 會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="03bae-147">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="03bae-148">傳回值</span><span class="sxs-lookup"><span data-stu-id="03bae-148">Return value</span></span>

<span data-ttu-id="03bae-149">材質格式，這是以 [**DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)列出的其中一個具類型值。</span><span class="sxs-lookup"><span data-stu-id="03bae-149">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="03bae-150">另請參閱</span><span class="sxs-lookup"><span data-stu-id="03bae-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03bae-151">範例方法</span><span class="sxs-lookup"><span data-stu-id="03bae-151">Sample methods</span></span>](texture2darray-sample.md)
</dt> </dl>

 

 
