---
title: RWTexture1D：： Operator 函數
description: 傳回資源變數。 |RWTexture1D：： Operator 函數
ms.assetid: 16e62879-8ed3-4b17-9124-9da41c41af4f
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
ms.openlocfilehash: ca44252a99e8b8e373cf109341c8c200636d8cf7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104514401"
---
# <a name="rwtexture1doperator--function"></a><span data-ttu-id="ee80c-105">RWTexture1D：： Operator 函數</span><span class="sxs-lookup"><span data-stu-id="ee80c-105">RWTexture1D::Operator  function</span></span>

<span data-ttu-id="ee80c-106">傳回資源變數。</span><span class="sxs-lookup"><span data-stu-id="ee80c-106">Returns a resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee80c-107">語法</span><span class="sxs-lookup"><span data-stu-id="ee80c-107">Syntax</span></span>

``` syntax
R Operator[](
  in uint pos
);
```

## <a name="parameters"></a><span data-ttu-id="ee80c-108">參數</span><span class="sxs-lookup"><span data-stu-id="ee80c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee80c-109">*pos* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ee80c-109">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee80c-110">類型： **uint**</span><span class="sxs-lookup"><span data-stu-id="ee80c-110">Type: **uint**</span></span>

<span data-ttu-id="ee80c-111">索引位置。</span><span class="sxs-lookup"><span data-stu-id="ee80c-111">The index position.</span></span> <span data-ttu-id="ee80c-112">包含 x 座標。</span><span class="sxs-lookup"><span data-stu-id="ee80c-112">Contains the x coordinate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee80c-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="ee80c-113">Return value</span></span>

<span data-ttu-id="ee80c-114">類型： **R**</span><span class="sxs-lookup"><span data-stu-id="ee80c-114">Type: **R**</span></span>

<span data-ttu-id="ee80c-115">資源變數。</span><span class="sxs-lookup"><span data-stu-id="ee80c-115">A resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="ee80c-116">備註</span><span class="sxs-lookup"><span data-stu-id="ee80c-116">Remarks</span></span>

<span data-ttu-id="ee80c-117">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="ee80c-117">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="ee80c-118">頂點</span><span class="sxs-lookup"><span data-stu-id="ee80c-118">Vertex</span></span> | <span data-ttu-id="ee80c-119">船體</span><span class="sxs-lookup"><span data-stu-id="ee80c-119">Hull</span></span> | <span data-ttu-id="ee80c-120">網域</span><span class="sxs-lookup"><span data-stu-id="ee80c-120">Domain</span></span> | <span data-ttu-id="ee80c-121">幾何</span><span class="sxs-lookup"><span data-stu-id="ee80c-121">Geometry</span></span> | <span data-ttu-id="ee80c-122">像素</span><span class="sxs-lookup"><span data-stu-id="ee80c-122">Pixel</span></span> | <span data-ttu-id="ee80c-123">計算</span><span class="sxs-lookup"><span data-stu-id="ee80c-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="ee80c-124">x</span><span class="sxs-lookup"><span data-stu-id="ee80c-124">x</span></span>     | <span data-ttu-id="ee80c-125">x</span><span class="sxs-lookup"><span data-stu-id="ee80c-125">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="ee80c-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ee80c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee80c-127">RWTexture1D</span><span class="sxs-lookup"><span data-stu-id="ee80c-127">RWTexture1D</span></span>](sm5-object-rwtexture1d.md)
</dt> <dt>

[<span data-ttu-id="ee80c-128">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="ee80c-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




