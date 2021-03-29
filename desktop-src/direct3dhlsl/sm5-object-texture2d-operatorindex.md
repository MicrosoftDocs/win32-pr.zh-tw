---
title: Texture2D：： Operator 函數
description: 傳回唯讀的資源變數。 |Texture2D：： Operator 函數
ms.assetid: 72ba3fc8-04c3-479a-b307-525020898bac
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
ms.openlocfilehash: 2c397b1b80836f48cb856d03ccdf52ad2c95ce48
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104974224"
---
# <a name="texture2doperator--function"></a><span data-ttu-id="155bc-105">Texture2D：： Operator 函數</span><span class="sxs-lookup"><span data-stu-id="155bc-105">Texture2D::Operator  function</span></span>

<span data-ttu-id="155bc-106">傳回唯讀的資源變數。</span><span class="sxs-lookup"><span data-stu-id="155bc-106">Returns a read-only resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="155bc-107">語法</span><span class="sxs-lookup"><span data-stu-id="155bc-107">Syntax</span></span>

``` syntax
R Operator[](
  in uint2 pos
);
```

## <a name="parameters"></a><span data-ttu-id="155bc-108">參數</span><span class="sxs-lookup"><span data-stu-id="155bc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="155bc-109">*pos* \[在\]</span><span class="sxs-lookup"><span data-stu-id="155bc-109">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="155bc-110">類型： **uint2**</span><span class="sxs-lookup"><span data-stu-id="155bc-110">Type: **uint2**</span></span>

<span data-ttu-id="155bc-111">索引位置。</span><span class="sxs-lookup"><span data-stu-id="155bc-111">The index position.</span></span> <span data-ttu-id="155bc-112">包含 (x，y) 座標。</span><span class="sxs-lookup"><span data-stu-id="155bc-112">Contains the (x, y) coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="155bc-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="155bc-113">Return value</span></span>

<span data-ttu-id="155bc-114">類型： **R**</span><span class="sxs-lookup"><span data-stu-id="155bc-114">Type: **R**</span></span>

<span data-ttu-id="155bc-115">唯讀的資源變數。</span><span class="sxs-lookup"><span data-stu-id="155bc-115">A read-only resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="155bc-116">備註</span><span class="sxs-lookup"><span data-stu-id="155bc-116">Remarks</span></span>

<span data-ttu-id="155bc-117">這個方法一律會存取第一個 mip 層級。</span><span class="sxs-lookup"><span data-stu-id="155bc-117">This method always accesses the first mip level.</span></span> <span data-ttu-id="155bc-118">若要指定其他 mip 層級，請改用 [**mip \[ \] \[ \] . operator**](sm5-object-texture2d-mipsoperatorindex.md)方法。</span><span class="sxs-lookup"><span data-stu-id="155bc-118">To specify other mip levels, use the [**mip.operator\[\]\[\]**](sm5-object-texture2d-mipsoperatorindex.md) method instead.</span></span>

<span data-ttu-id="155bc-119">紋理範例可用於雙線性插補。</span><span class="sxs-lookup"><span data-stu-id="155bc-119">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="155bc-120">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="155bc-120">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="155bc-121">頂點</span><span class="sxs-lookup"><span data-stu-id="155bc-121">Vertex</span></span> | <span data-ttu-id="155bc-122">船體</span><span class="sxs-lookup"><span data-stu-id="155bc-122">Hull</span></span> | <span data-ttu-id="155bc-123">網域</span><span class="sxs-lookup"><span data-stu-id="155bc-123">Domain</span></span> | <span data-ttu-id="155bc-124">幾何</span><span class="sxs-lookup"><span data-stu-id="155bc-124">Geometry</span></span> | <span data-ttu-id="155bc-125">像素</span><span class="sxs-lookup"><span data-stu-id="155bc-125">Pixel</span></span> | <span data-ttu-id="155bc-126">計算</span><span class="sxs-lookup"><span data-stu-id="155bc-126">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="155bc-127">x</span><span class="sxs-lookup"><span data-stu-id="155bc-127">x</span></span>      | <span data-ttu-id="155bc-128">x</span><span class="sxs-lookup"><span data-stu-id="155bc-128">x</span></span>    | <span data-ttu-id="155bc-129">x</span><span class="sxs-lookup"><span data-stu-id="155bc-129">x</span></span>      | <span data-ttu-id="155bc-130">x</span><span class="sxs-lookup"><span data-stu-id="155bc-130">x</span></span>        | <span data-ttu-id="155bc-131">x</span><span class="sxs-lookup"><span data-stu-id="155bc-131">x</span></span>     | <span data-ttu-id="155bc-132">x</span><span class="sxs-lookup"><span data-stu-id="155bc-132">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="155bc-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="155bc-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="155bc-134">Texture2D</span><span class="sxs-lookup"><span data-stu-id="155bc-134">Texture2D</span></span>](sm5-object-texture2d.md)
</dt> <dt>

[<span data-ttu-id="155bc-135">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="155bc-135">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




