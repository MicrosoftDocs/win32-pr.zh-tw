---
title: Texture2DMS：： sample。Operator 函數
description: 在提供的位置和樣本索引上，抓取資源的值。 |Texture2DMS：： sample。Operator 函數
ms.assetid: 5bc24129-b690-44dd-ae85-8533b10befaa
keywords:
- 樣品。運算子函式 HLSL
topic_type:
- apiref
api_name:
- sample.Operator
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1a73577fa67992b212b4769059f1523e584acbaf
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104196125"
---
# <a name="texture2dmssampleoperator----function"></a><span data-ttu-id="239c7-105">Texture2DMS：： sample。Operator 函數</span><span class="sxs-lookup"><span data-stu-id="239c7-105">Texture2DMS::sample.Operator    function</span></span>

<span data-ttu-id="239c7-106">在提供的位置和樣本索引上，抓取資源的值。</span><span class="sxs-lookup"><span data-stu-id="239c7-106">Retrieves a value from the resource at the location and sample index provided.</span></span>

## <a name="syntax"></a><span data-ttu-id="239c7-107">語法</span><span class="sxs-lookup"><span data-stu-id="239c7-107">Syntax</span></span>

``` syntax
R sample.Operator[][](
  in uint sampleSlice,
  in uint2 pos
);
```

## <a name="parameters"></a><span data-ttu-id="239c7-108">參數</span><span class="sxs-lookup"><span data-stu-id="239c7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="239c7-109">*sampleSlice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="239c7-109">*sampleSlice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="239c7-110">類型： **uint**</span><span class="sxs-lookup"><span data-stu-id="239c7-110">Type: **uint**</span></span>

<span data-ttu-id="239c7-111">範例配量索引。</span><span class="sxs-lookup"><span data-stu-id="239c7-111">The sample slice index.</span></span>

</dd> <dt>

<span data-ttu-id="239c7-112">*pos* \[在\]</span><span class="sxs-lookup"><span data-stu-id="239c7-112">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="239c7-113">類型： **uint2**</span><span class="sxs-lookup"><span data-stu-id="239c7-113">Type: **uint2**</span></span>

<span data-ttu-id="239c7-114">索引位置。</span><span class="sxs-lookup"><span data-stu-id="239c7-114">The index position.</span></span> <span data-ttu-id="239c7-115">元件包含 (x，y) 座標。</span><span class="sxs-lookup"><span data-stu-id="239c7-115">The components contain the (x, y) coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="239c7-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="239c7-116">Return value</span></span>

<span data-ttu-id="239c7-117">類型： **R**</span><span class="sxs-lookup"><span data-stu-id="239c7-117">Type: **R**</span></span>

<span data-ttu-id="239c7-118">唯讀的資源變數。</span><span class="sxs-lookup"><span data-stu-id="239c7-118">A read-only resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="239c7-119">備註</span><span class="sxs-lookup"><span data-stu-id="239c7-119">Remarks</span></span>

### <a name="usage-example"></a><span data-ttu-id="239c7-120">使用範例</span><span class="sxs-lookup"><span data-stu-id="239c7-120">Usage Example</span></span>


```
Texture2DMS<float4, 8> tex;

float4 main( float3 tcoord : texturecoord0 ) : SV_Target
{
     return s_msTexture.sample[2][tcoord];
}
```



<span data-ttu-id="239c7-121">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="239c7-121">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="239c7-122">頂點</span><span class="sxs-lookup"><span data-stu-id="239c7-122">Vertex</span></span> | <span data-ttu-id="239c7-123">船體</span><span class="sxs-lookup"><span data-stu-id="239c7-123">Hull</span></span> | <span data-ttu-id="239c7-124">網域</span><span class="sxs-lookup"><span data-stu-id="239c7-124">Domain</span></span> | <span data-ttu-id="239c7-125">幾何</span><span class="sxs-lookup"><span data-stu-id="239c7-125">Geometry</span></span> | <span data-ttu-id="239c7-126">像素</span><span class="sxs-lookup"><span data-stu-id="239c7-126">Pixel</span></span> | <span data-ttu-id="239c7-127">計算</span><span class="sxs-lookup"><span data-stu-id="239c7-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="239c7-128">x</span><span class="sxs-lookup"><span data-stu-id="239c7-128">x</span></span>      | <span data-ttu-id="239c7-129">x</span><span class="sxs-lookup"><span data-stu-id="239c7-129">x</span></span>    | <span data-ttu-id="239c7-130">x</span><span class="sxs-lookup"><span data-stu-id="239c7-130">x</span></span>      | <span data-ttu-id="239c7-131">x</span><span class="sxs-lookup"><span data-stu-id="239c7-131">x</span></span>        | <span data-ttu-id="239c7-132">x</span><span class="sxs-lookup"><span data-stu-id="239c7-132">x</span></span>     | <span data-ttu-id="239c7-133">x</span><span class="sxs-lookup"><span data-stu-id="239c7-133">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="239c7-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="239c7-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="239c7-135">Texture2DMS</span><span class="sxs-lookup"><span data-stu-id="239c7-135">Texture2DMS</span></span>](sm5-object-texture2dms.md)
</dt> <dt>

[<span data-ttu-id="239c7-136">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="239c7-136">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




