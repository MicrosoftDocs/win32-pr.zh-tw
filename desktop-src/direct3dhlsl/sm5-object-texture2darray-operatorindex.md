---
title: Texture2DArray：： Operator 函數
description: 傳回唯讀的資源變數。 |Texture2DArray：： Operator 函數
ms.assetid: eb6ff496-c46f-405f-a172-ab747415a2f9
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
ms.openlocfilehash: 1b86aad839fbf28a4fc666b3a5fe5c5788b7b3ae
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104035244"
---
# <a name="texture2darrayoperator--function"></a><span data-ttu-id="02ff4-105">Texture2DArray：： Operator 函數</span><span class="sxs-lookup"><span data-stu-id="02ff4-105">Texture2DArray::Operator  function</span></span>

<span data-ttu-id="02ff4-106">傳回唯讀的資源變數。</span><span class="sxs-lookup"><span data-stu-id="02ff4-106">Returns a read-only resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="02ff4-107">語法</span><span class="sxs-lookup"><span data-stu-id="02ff4-107">Syntax</span></span>

``` syntax
R Operator[](
  in uint3 pos
);
```

## <a name="parameters"></a><span data-ttu-id="02ff4-108">參數</span><span class="sxs-lookup"><span data-stu-id="02ff4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02ff4-109">*pos* \[在\]</span><span class="sxs-lookup"><span data-stu-id="02ff4-109">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02ff4-110">類型： **uint3**</span><span class="sxs-lookup"><span data-stu-id="02ff4-110">Type: **uint3**</span></span>

<span data-ttu-id="02ff4-111">索引位置。</span><span class="sxs-lookup"><span data-stu-id="02ff4-111">The index position.</span></span> <span data-ttu-id="02ff4-112">第一個和第二個元件包含 (x，y) 座標。</span><span class="sxs-lookup"><span data-stu-id="02ff4-112">The first and second components contain the (x, y) coordinates.</span></span> <span data-ttu-id="02ff4-113">第三個元件表示所要的陣列配量。</span><span class="sxs-lookup"><span data-stu-id="02ff4-113">The third component indicates the desired array slice.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02ff4-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="02ff4-114">Return value</span></span>

<span data-ttu-id="02ff4-115">類型： **R**</span><span class="sxs-lookup"><span data-stu-id="02ff4-115">Type: **R**</span></span>

<span data-ttu-id="02ff4-116">唯讀的資源變數。</span><span class="sxs-lookup"><span data-stu-id="02ff4-116">A read-only resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="02ff4-117">備註</span><span class="sxs-lookup"><span data-stu-id="02ff4-117">Remarks</span></span>

<span data-ttu-id="02ff4-118">這個方法一律會存取第一個 mip 層級。</span><span class="sxs-lookup"><span data-stu-id="02ff4-118">This method always accesses the first mip level.</span></span> <span data-ttu-id="02ff4-119">若要指定其他 mip 層級，請改用 [**mip \[ \] \[ \] . operator**](sm5-object-texture2darray-mipsoperatorindex.md)方法。</span><span class="sxs-lookup"><span data-stu-id="02ff4-119">To specify other mip levels, use the [**mip.operator\[\]\[\]**](sm5-object-texture2darray-mipsoperatorindex.md) method instead.</span></span>

<span data-ttu-id="02ff4-120">紋理範例可用於雙線性插補。</span><span class="sxs-lookup"><span data-stu-id="02ff4-120">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="02ff4-121">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="02ff4-121">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="02ff4-122">頂點</span><span class="sxs-lookup"><span data-stu-id="02ff4-122">Vertex</span></span> | <span data-ttu-id="02ff4-123">船體</span><span class="sxs-lookup"><span data-stu-id="02ff4-123">Hull</span></span> | <span data-ttu-id="02ff4-124">網域</span><span class="sxs-lookup"><span data-stu-id="02ff4-124">Domain</span></span> | <span data-ttu-id="02ff4-125">幾何</span><span class="sxs-lookup"><span data-stu-id="02ff4-125">Geometry</span></span> | <span data-ttu-id="02ff4-126">像素</span><span class="sxs-lookup"><span data-stu-id="02ff4-126">Pixel</span></span> | <span data-ttu-id="02ff4-127">計算</span><span class="sxs-lookup"><span data-stu-id="02ff4-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="02ff4-128">x</span><span class="sxs-lookup"><span data-stu-id="02ff4-128">x</span></span>      | <span data-ttu-id="02ff4-129">x</span><span class="sxs-lookup"><span data-stu-id="02ff4-129">x</span></span>    | <span data-ttu-id="02ff4-130">x</span><span class="sxs-lookup"><span data-stu-id="02ff4-130">x</span></span>      | <span data-ttu-id="02ff4-131">x</span><span class="sxs-lookup"><span data-stu-id="02ff4-131">x</span></span>        | <span data-ttu-id="02ff4-132">x</span><span class="sxs-lookup"><span data-stu-id="02ff4-132">x</span></span>     | <span data-ttu-id="02ff4-133">x</span><span class="sxs-lookup"><span data-stu-id="02ff4-133">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="02ff4-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="02ff4-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02ff4-135">Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="02ff4-135">Texture2DArray</span></span>](sm5-object-texture2darray.md)
</dt> <dt>

[<span data-ttu-id="02ff4-136">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="02ff4-136">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




