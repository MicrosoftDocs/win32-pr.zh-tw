---
title: Texture3D：： Operator 函數
description: 傳回唯讀的資源變數。 |Texture3D：： Operator 函數
ms.assetid: d7e27778-6a96-47f8-a58a-1966452adf04
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
ms.openlocfilehash: 5c3bb3718094ee859d1e33a046fde7016973a0aa
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "103696433"
---
# <a name="texture3doperator--function"></a><span data-ttu-id="0dcf8-105">Texture3D：： Operator 函數</span><span class="sxs-lookup"><span data-stu-id="0dcf8-105">Texture3D::Operator  function</span></span>

<span data-ttu-id="0dcf8-106">傳回唯讀的資源變數。</span><span class="sxs-lookup"><span data-stu-id="0dcf8-106">Returns a read-only resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="0dcf8-107">語法</span><span class="sxs-lookup"><span data-stu-id="0dcf8-107">Syntax</span></span>

``` syntax
R Operator[](
  in uint3 pos
);
```

## <a name="parameters"></a><span data-ttu-id="0dcf8-108">參數</span><span class="sxs-lookup"><span data-stu-id="0dcf8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0dcf8-109">*pos* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0dcf8-109">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0dcf8-110">類型： **uint3**</span><span class="sxs-lookup"><span data-stu-id="0dcf8-110">Type: **uint3**</span></span>

<span data-ttu-id="0dcf8-111">索引位置。</span><span class="sxs-lookup"><span data-stu-id="0dcf8-111">The index position.</span></span> <span data-ttu-id="0dcf8-112">包含 (x，y，z) 座標。</span><span class="sxs-lookup"><span data-stu-id="0dcf8-112">Contains the (x, y, z) coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0dcf8-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="0dcf8-113">Return value</span></span>

<span data-ttu-id="0dcf8-114">類型： **R**</span><span class="sxs-lookup"><span data-stu-id="0dcf8-114">Type: **R**</span></span>

<span data-ttu-id="0dcf8-115">唯讀的資源變數。</span><span class="sxs-lookup"><span data-stu-id="0dcf8-115">A read-only resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="0dcf8-116">備註</span><span class="sxs-lookup"><span data-stu-id="0dcf8-116">Remarks</span></span>

<span data-ttu-id="0dcf8-117">這個方法一律會存取第一個 mip 層級。</span><span class="sxs-lookup"><span data-stu-id="0dcf8-117">This method always accesses the first mip level.</span></span> <span data-ttu-id="0dcf8-118">若要指定其他 mip 層級，請改用 [**mip. 運算子 \[ \] \[ \]**](sm5-object-texture3d-mipsoperatorindex.md) 。</span><span class="sxs-lookup"><span data-stu-id="0dcf8-118">To specify other mip levels use the [**mip.operator\[\]\[\]**](sm5-object-texture3d-mipsoperatorindex.md) instead.</span></span>

<span data-ttu-id="0dcf8-119">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="0dcf8-119">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="0dcf8-120">頂點</span><span class="sxs-lookup"><span data-stu-id="0dcf8-120">Vertex</span></span> | <span data-ttu-id="0dcf8-121">船體</span><span class="sxs-lookup"><span data-stu-id="0dcf8-121">Hull</span></span> | <span data-ttu-id="0dcf8-122">網域</span><span class="sxs-lookup"><span data-stu-id="0dcf8-122">Domain</span></span> | <span data-ttu-id="0dcf8-123">幾何</span><span class="sxs-lookup"><span data-stu-id="0dcf8-123">Geometry</span></span> | <span data-ttu-id="0dcf8-124">像素</span><span class="sxs-lookup"><span data-stu-id="0dcf8-124">Pixel</span></span> | <span data-ttu-id="0dcf8-125">計算</span><span class="sxs-lookup"><span data-stu-id="0dcf8-125">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="0dcf8-126">x</span><span class="sxs-lookup"><span data-stu-id="0dcf8-126">x</span></span>      | <span data-ttu-id="0dcf8-127">x</span><span class="sxs-lookup"><span data-stu-id="0dcf8-127">x</span></span>    | <span data-ttu-id="0dcf8-128">x</span><span class="sxs-lookup"><span data-stu-id="0dcf8-128">x</span></span>      | <span data-ttu-id="0dcf8-129">x</span><span class="sxs-lookup"><span data-stu-id="0dcf8-129">x</span></span>        | <span data-ttu-id="0dcf8-130">x</span><span class="sxs-lookup"><span data-stu-id="0dcf8-130">x</span></span>     | <span data-ttu-id="0dcf8-131">x</span><span class="sxs-lookup"><span data-stu-id="0dcf8-131">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="0dcf8-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0dcf8-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0dcf8-133">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0dcf8-133">Texture3D</span></span>](sm5-object-texture3d.md)
</dt> <dt>

[<span data-ttu-id="0dcf8-134">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="0dcf8-134">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




