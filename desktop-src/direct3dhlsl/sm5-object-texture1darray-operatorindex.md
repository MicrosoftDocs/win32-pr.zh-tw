---
title: Texture1DArray：： Operator 函數
description: 傳回唯讀的資源變數。 |Texture1DArray：： Operator 函數
ms.assetid: 05ec9652-b5dd-41cf-8bef-730c507c5ba4
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
ms.openlocfilehash: 578d778cd1e0e064c435c19fb094feb66f651e05
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104974188"
---
# <a name="texture1darrayoperator--function"></a><span data-ttu-id="74bc8-105">Texture1DArray：： Operator 函數</span><span class="sxs-lookup"><span data-stu-id="74bc8-105">Texture1DArray::Operator  function</span></span>

<span data-ttu-id="74bc8-106">傳回唯讀的資源變數。</span><span class="sxs-lookup"><span data-stu-id="74bc8-106">Returns a read-only resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="74bc8-107">語法</span><span class="sxs-lookup"><span data-stu-id="74bc8-107">Syntax</span></span>

``` syntax
R Operator[](
  in uint2 pos
);
```

## <a name="parameters"></a><span data-ttu-id="74bc8-108">參數</span><span class="sxs-lookup"><span data-stu-id="74bc8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74bc8-109">*pos* \[在\]</span><span class="sxs-lookup"><span data-stu-id="74bc8-109">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74bc8-110">類型： **uint2**</span><span class="sxs-lookup"><span data-stu-id="74bc8-110">Type: **uint2**</span></span>

<span data-ttu-id="74bc8-111">索引位置。</span><span class="sxs-lookup"><span data-stu-id="74bc8-111">The index position.</span></span> <span data-ttu-id="74bc8-112">第一個元件包含 x 座標。</span><span class="sxs-lookup"><span data-stu-id="74bc8-112">The first component contains the x-coordinate.</span></span> <span data-ttu-id="74bc8-113">第二個元件表示所要的陣列配量。</span><span class="sxs-lookup"><span data-stu-id="74bc8-113">The second component indicates the desired array slice.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74bc8-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="74bc8-114">Return value</span></span>

<span data-ttu-id="74bc8-115">類型： **R**</span><span class="sxs-lookup"><span data-stu-id="74bc8-115">Type: **R**</span></span>

<span data-ttu-id="74bc8-116">唯讀的資源變數。</span><span class="sxs-lookup"><span data-stu-id="74bc8-116">A read-only resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="74bc8-117">備註</span><span class="sxs-lookup"><span data-stu-id="74bc8-117">Remarks</span></span>

<span data-ttu-id="74bc8-118">這個方法一律會存取第一個 mip 層級。</span><span class="sxs-lookup"><span data-stu-id="74bc8-118">This method always accesses the first mip level.</span></span> <span data-ttu-id="74bc8-119">若要指定其他 mip 層級，請改用 [**mip \[ \] \[ \] . operator**](sm5-object-texture1darray-mipsoperatorindex.md)方法。</span><span class="sxs-lookup"><span data-stu-id="74bc8-119">To specify other mip levels, use the [**mip.operator\[\]\[\]**](sm5-object-texture1darray-mipsoperatorindex.md) method instead.</span></span>

<span data-ttu-id="74bc8-120">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="74bc8-120">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="74bc8-121">頂點</span><span class="sxs-lookup"><span data-stu-id="74bc8-121">Vertex</span></span> | <span data-ttu-id="74bc8-122">船體</span><span class="sxs-lookup"><span data-stu-id="74bc8-122">Hull</span></span> | <span data-ttu-id="74bc8-123">網域</span><span class="sxs-lookup"><span data-stu-id="74bc8-123">Domain</span></span> | <span data-ttu-id="74bc8-124">幾何</span><span class="sxs-lookup"><span data-stu-id="74bc8-124">Geometry</span></span> | <span data-ttu-id="74bc8-125">像素</span><span class="sxs-lookup"><span data-stu-id="74bc8-125">Pixel</span></span> | <span data-ttu-id="74bc8-126">計算</span><span class="sxs-lookup"><span data-stu-id="74bc8-126">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="74bc8-127">x</span><span class="sxs-lookup"><span data-stu-id="74bc8-127">x</span></span>      | <span data-ttu-id="74bc8-128">x</span><span class="sxs-lookup"><span data-stu-id="74bc8-128">x</span></span>    | <span data-ttu-id="74bc8-129">x</span><span class="sxs-lookup"><span data-stu-id="74bc8-129">x</span></span>      | <span data-ttu-id="74bc8-130">x</span><span class="sxs-lookup"><span data-stu-id="74bc8-130">x</span></span>        | <span data-ttu-id="74bc8-131">x</span><span class="sxs-lookup"><span data-stu-id="74bc8-131">x</span></span>     | <span data-ttu-id="74bc8-132">x</span><span class="sxs-lookup"><span data-stu-id="74bc8-132">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="74bc8-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="74bc8-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74bc8-134">Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="74bc8-134">Texture1DArray</span></span>](sm5-object-texture1darray.md)
</dt> <dt>

[<span data-ttu-id="74bc8-135">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="74bc8-135">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




