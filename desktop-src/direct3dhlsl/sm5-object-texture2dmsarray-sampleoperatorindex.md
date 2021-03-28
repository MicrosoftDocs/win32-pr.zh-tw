---
title: Texture2DMSArray：： sample。Operator 函數
description: 傳回唯讀的資源變數。 |Texture2DMSArray：： sample。Operator 函數
ms.assetid: 5334c1d5-dfbd-4987-875c-0b92967b0f13
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
ms.openlocfilehash: e78746e0afe03e65a313982ca35c27a75ea14f1b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104974380"
---
# <a name="texture2dmsarraysampleoperator----function"></a><span data-ttu-id="12167-105">Texture2DMSArray：： sample。Operator 函數</span><span class="sxs-lookup"><span data-stu-id="12167-105">Texture2DMSArray::sample.Operator    function</span></span>

<span data-ttu-id="12167-106">傳回唯讀的資源變數。</span><span class="sxs-lookup"><span data-stu-id="12167-106">Returns a read-only resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="12167-107">語法</span><span class="sxs-lookup"><span data-stu-id="12167-107">Syntax</span></span>

``` syntax
R sample.Operator[][](
  in uint sampleSlice,
  in uint3 pos
);
```

## <a name="parameters"></a><span data-ttu-id="12167-108">參數</span><span class="sxs-lookup"><span data-stu-id="12167-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12167-109">*sampleSlice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="12167-109">*sampleSlice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12167-110">類型： **uint**</span><span class="sxs-lookup"><span data-stu-id="12167-110">Type: **uint**</span></span>

<span data-ttu-id="12167-111">範例配量索引。</span><span class="sxs-lookup"><span data-stu-id="12167-111">The sample slice index.</span></span>

</dd> <dt>

<span data-ttu-id="12167-112">*pos* \[在\]</span><span class="sxs-lookup"><span data-stu-id="12167-112">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12167-113">類型： **uint3**</span><span class="sxs-lookup"><span data-stu-id="12167-113">Type: **uint3**</span></span>

<span data-ttu-id="12167-114">索引位置。</span><span class="sxs-lookup"><span data-stu-id="12167-114">The index position.</span></span> <span data-ttu-id="12167-115">第一個和第二個元件包含 (x，y) 座標。</span><span class="sxs-lookup"><span data-stu-id="12167-115">The first and second components contain the (x, y) coordinates.</span></span> <span data-ttu-id="12167-116">第三個元件表示所要的陣列配量。</span><span class="sxs-lookup"><span data-stu-id="12167-116">The third component indicates the desired array slice.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12167-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="12167-117">Return value</span></span>

<span data-ttu-id="12167-118">類型： **R**</span><span class="sxs-lookup"><span data-stu-id="12167-118">Type: **R**</span></span>

<span data-ttu-id="12167-119">唯讀的資源變數。</span><span class="sxs-lookup"><span data-stu-id="12167-119">A read-only resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="12167-120">備註</span><span class="sxs-lookup"><span data-stu-id="12167-120">Remarks</span></span>

### <a name="usage-example"></a><span data-ttu-id="12167-121">使用範例</span><span class="sxs-lookup"><span data-stu-id="12167-121">Usage Example</span></span>


```
Texture2DMSArray<float4, 4> alpha;

float4 main( float3 tcoord : texturecoord0 ) : SV_Target
{
     return s_msTexture.sample[2][tcoord];
}
```



<span data-ttu-id="12167-122">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="12167-122">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="12167-123">頂點</span><span class="sxs-lookup"><span data-stu-id="12167-123">Vertex</span></span> | <span data-ttu-id="12167-124">船體</span><span class="sxs-lookup"><span data-stu-id="12167-124">Hull</span></span> | <span data-ttu-id="12167-125">網域</span><span class="sxs-lookup"><span data-stu-id="12167-125">Domain</span></span> | <span data-ttu-id="12167-126">幾何</span><span class="sxs-lookup"><span data-stu-id="12167-126">Geometry</span></span> | <span data-ttu-id="12167-127">像素</span><span class="sxs-lookup"><span data-stu-id="12167-127">Pixel</span></span> | <span data-ttu-id="12167-128">計算</span><span class="sxs-lookup"><span data-stu-id="12167-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="12167-129">x</span><span class="sxs-lookup"><span data-stu-id="12167-129">x</span></span>      | <span data-ttu-id="12167-130">x</span><span class="sxs-lookup"><span data-stu-id="12167-130">x</span></span>    | <span data-ttu-id="12167-131">x</span><span class="sxs-lookup"><span data-stu-id="12167-131">x</span></span>      | <span data-ttu-id="12167-132">x</span><span class="sxs-lookup"><span data-stu-id="12167-132">x</span></span>        | <span data-ttu-id="12167-133">x</span><span class="sxs-lookup"><span data-stu-id="12167-133">x</span></span>     | <span data-ttu-id="12167-134">x</span><span class="sxs-lookup"><span data-stu-id="12167-134">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="12167-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="12167-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12167-136">Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="12167-136">Texture2DMSArray</span></span>](sm5-object-texture2dmsarray.md)
</dt> <dt>

[<span data-ttu-id="12167-137">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="12167-137">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




