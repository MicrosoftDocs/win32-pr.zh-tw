---
title: RWTexture2D：： Operator 函數
description: 傳回資源變數。 |RWTexture2D：： Operator 函數
ms.assetid: 339dba7d-b0c6-4112-ae40-555661577a3e
keywords:
- 運算子函式 HLSL
topic_type:
- apiref
api_name:
- Operator
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8c1ff25cdf4a0f33d041500f6a81220261f216c4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104974189"
---
# <a name="rwtexture2doperator--function"></a><span data-ttu-id="8d448-105">RWTexture2D：： Operator 函數</span><span class="sxs-lookup"><span data-stu-id="8d448-105">RWTexture2D::Operator  function</span></span>

<span data-ttu-id="8d448-106">傳回資源變數。</span><span class="sxs-lookup"><span data-stu-id="8d448-106">Returns a resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d448-107">語法</span><span class="sxs-lookup"><span data-stu-id="8d448-107">Syntax</span></span>

``` syntax
R Operator[](
  in uint2 pos
);
```

## <a name="parameters"></a><span data-ttu-id="8d448-108">參數</span><span class="sxs-lookup"><span data-stu-id="8d448-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d448-109">*pos* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8d448-109">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d448-110">類型： **uint2**</span><span class="sxs-lookup"><span data-stu-id="8d448-110">Type: **uint2**</span></span>

<span data-ttu-id="8d448-111">索引位置。</span><span class="sxs-lookup"><span data-stu-id="8d448-111">The index position.</span></span> <span data-ttu-id="8d448-112">包含 (x，y) 座標。</span><span class="sxs-lookup"><span data-stu-id="8d448-112">Contains the (x, y) coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d448-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="8d448-113">Return value</span></span>

<span data-ttu-id="8d448-114">類型： **R**</span><span class="sxs-lookup"><span data-stu-id="8d448-114">Type: **R**</span></span>

<span data-ttu-id="8d448-115">資源變數。</span><span class="sxs-lookup"><span data-stu-id="8d448-115">A resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="8d448-116">備註</span><span class="sxs-lookup"><span data-stu-id="8d448-116">Remarks</span></span>

<span data-ttu-id="8d448-117">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="8d448-117">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="8d448-118">頂點</span><span class="sxs-lookup"><span data-stu-id="8d448-118">Vertex</span></span> | <span data-ttu-id="8d448-119">船體</span><span class="sxs-lookup"><span data-stu-id="8d448-119">Hull</span></span> | <span data-ttu-id="8d448-120">網域</span><span class="sxs-lookup"><span data-stu-id="8d448-120">Domain</span></span> | <span data-ttu-id="8d448-121">幾何</span><span class="sxs-lookup"><span data-stu-id="8d448-121">Geometry</span></span> | <span data-ttu-id="8d448-122">像素</span><span class="sxs-lookup"><span data-stu-id="8d448-122">Pixel</span></span> | <span data-ttu-id="8d448-123">計算</span><span class="sxs-lookup"><span data-stu-id="8d448-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="8d448-124">x</span><span class="sxs-lookup"><span data-stu-id="8d448-124">x</span></span>     | <span data-ttu-id="8d448-125">x</span><span class="sxs-lookup"><span data-stu-id="8d448-125">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="8d448-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8d448-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d448-127">RWTexture2D</span><span class="sxs-lookup"><span data-stu-id="8d448-127">RWTexture2D</span></span>](sm5-object-rwtexture2d.md)
</dt> <dt>

[<span data-ttu-id="8d448-128">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="8d448-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




