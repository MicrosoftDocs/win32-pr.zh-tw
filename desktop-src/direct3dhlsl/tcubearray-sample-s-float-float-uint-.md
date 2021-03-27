---
title: TextureCubeArray：： Sample (S，float，float，uint) 函數
description: 使用選擇性值來取樣材質，以將範例詳細資料 (」 LOD) 值，並傳回作業的狀態。 |TextureCubeArray：： Sample (S，float，float，uint) 函數
ms.assetid: 5645841D-A32E-452E-873C-E070CF6A4C00
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
ms.openlocfilehash: 24e6d77698507f0d1673b66954db8e78466ac728
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "103696418"
---
# <a name="texturecubearraysamplesfloatfloatuint-function"></a><span data-ttu-id="3ce23-105">TextureCubeArray：： Sample (S，float，float，uint) 函數</span><span class="sxs-lookup"><span data-stu-id="3ce23-105">TextureCubeArray::Sample(S,float,float,uint) function</span></span>

<span data-ttu-id="3ce23-106">使用選擇性值來取樣材質，以將範例詳細資料 (」 LOD) 值，並傳回作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="3ce23-106">Samples a texture with an optional value to clamp sample level-of-detail (LOD) values to, and returns status of the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ce23-107">語法</span><span class="sxs-lookup"><span data-stu-id="3ce23-107">Syntax</span></span>


``` syntax
DXGI_FORMAT Sample(
  in  SamplerState S,
  in  float        Location,
  in  float        Clamp,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="3ce23-108">參數</span><span class="sxs-lookup"><span data-stu-id="3ce23-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ce23-109"> \[ 中的 S\]</span><span class="sxs-lookup"><span data-stu-id="3ce23-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ce23-110">[取樣器狀態](dx-graphics-hlsl-sampler.md)。</span><span class="sxs-lookup"><span data-stu-id="3ce23-110">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="3ce23-111">這是在包含狀態指派的效果檔案中宣告的物件。</span><span class="sxs-lookup"><span data-stu-id="3ce23-111">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="3ce23-112">*位置* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3ce23-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ce23-113">材質座標。</span><span class="sxs-lookup"><span data-stu-id="3ce23-113">The texture coordinates.</span></span> <span data-ttu-id="3ce23-114">引數類型相依于材質物件類型。</span><span class="sxs-lookup"><span data-stu-id="3ce23-114">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="3ce23-115">Texture-Object 類型</span><span class="sxs-lookup"><span data-stu-id="3ce23-115">Texture-Object Type</span></span>                    | <span data-ttu-id="3ce23-116">參數類型</span><span class="sxs-lookup"><span data-stu-id="3ce23-116">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="3ce23-117">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3ce23-117">Texture1D</span></span>                              | <span data-ttu-id="3ce23-118">FLOAT</span><span class="sxs-lookup"><span data-stu-id="3ce23-118">float</span></span>          |
| <span data-ttu-id="3ce23-119">Texture1DArray、Texture2D</span><span class="sxs-lookup"><span data-stu-id="3ce23-119">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="3ce23-120">float2</span><span class="sxs-lookup"><span data-stu-id="3ce23-120">float2</span></span>         |
| <span data-ttu-id="3ce23-121">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="3ce23-121">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="3ce23-122">float3</span><span class="sxs-lookup"><span data-stu-id="3ce23-122">float3</span></span>         |
| <span data-ttu-id="3ce23-123">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="3ce23-123">TextureCubeArray</span></span>                       | <span data-ttu-id="3ce23-124">float4</span><span class="sxs-lookup"><span data-stu-id="3ce23-124">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="3ce23-125">*夾具* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3ce23-125">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ce23-126">用來將範例」 LOD 值設為的選擇性值。</span><span class="sxs-lookup"><span data-stu-id="3ce23-126">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="3ce23-127">例如，如果您傳遞 2.0 f 作為夾具值，您可以確保沒有任何個別的範例存取小於 2.0 f 的 mip 層級。</span><span class="sxs-lookup"><span data-stu-id="3ce23-127">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> <dt>

<span data-ttu-id="3ce23-128">*狀態* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="3ce23-128">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3ce23-129">作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="3ce23-129">The status of the operation.</span></span> <span data-ttu-id="3ce23-130">您無法直接存取狀態;相反地，請將狀態傳遞給 [**CheckAccessFullyMapped**](checkaccessfullymapped.md) 內建函式。</span><span class="sxs-lookup"><span data-stu-id="3ce23-130">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="3ce23-131">如果對應的 **範例**、**收集** 或 **載入** 作業中的所有值都是在 [磚資源](/windows/desktop/direct3d11/direct3d-11-2-features)中存取對應的磚， **CheckAccessFullyMapped** 會傳回 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="3ce23-131">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="3ce23-132">如果有任何值取自未對應的磚， **CheckAccessFullyMapped** 會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="3ce23-132">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ce23-133">傳回值</span><span class="sxs-lookup"><span data-stu-id="3ce23-133">Return value</span></span>

<span data-ttu-id="3ce23-134">材質格式，這是以 [**DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)列出的其中一個具類型值。</span><span class="sxs-lookup"><span data-stu-id="3ce23-134">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="3ce23-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3ce23-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ce23-136">範例方法</span><span class="sxs-lookup"><span data-stu-id="3ce23-136">Sample methods</span></span>](texturecubearray-sample.md)
</dt> <dt>

[<span data-ttu-id="3ce23-137">**TextureCubeArray**</span><span class="sxs-lookup"><span data-stu-id="3ce23-137">**TextureCubeArray**</span></span>](texturecubearray.md)
</dt> </dl>

 

 
