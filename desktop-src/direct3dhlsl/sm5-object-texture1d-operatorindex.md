---
title: Texture1D：： Operator 函數
description: 傳回 Texture1D 的唯讀資源變數。
ms.assetid: df54097d-4d1b-496a-a17d-6e9a10cfb996
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
ms.openlocfilehash: 44e5b502c7ae8b766363956920d7922858b4d771
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104093667"
---
# <a name="texture1doperator--function"></a><span data-ttu-id="bd7a2-104">Texture1D：： Operator 函數</span><span class="sxs-lookup"><span data-stu-id="bd7a2-104">Texture1D::Operator  function</span></span>

<span data-ttu-id="bd7a2-105">傳回 [**Texture1D**](sm5-object-texture1d.md)的唯讀資源變數。</span><span class="sxs-lookup"><span data-stu-id="bd7a2-105">Returns a read-only resource variable for a [**Texture1D**](sm5-object-texture1d.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="bd7a2-106">語法</span><span class="sxs-lookup"><span data-stu-id="bd7a2-106">Syntax</span></span>

``` syntax
R Operator[](
  in uint pos
);
```

## <a name="parameters"></a><span data-ttu-id="bd7a2-107">參數</span><span class="sxs-lookup"><span data-stu-id="bd7a2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd7a2-108">*pos* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bd7a2-108">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bd7a2-109">類型： **uint**</span><span class="sxs-lookup"><span data-stu-id="bd7a2-109">Type: **uint**</span></span>

<span data-ttu-id="bd7a2-110">索引位置。</span><span class="sxs-lookup"><span data-stu-id="bd7a2-110">The index position.</span></span> <span data-ttu-id="bd7a2-111">包含 x 座標。</span><span class="sxs-lookup"><span data-stu-id="bd7a2-111">Contains the x-coordinate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd7a2-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="bd7a2-112">Return value</span></span>

<span data-ttu-id="bd7a2-113">類型： **R**</span><span class="sxs-lookup"><span data-stu-id="bd7a2-113">Type: **R**</span></span>

<span data-ttu-id="bd7a2-114">唯讀的資源變數。</span><span class="sxs-lookup"><span data-stu-id="bd7a2-114">A read-only resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="bd7a2-115">備註</span><span class="sxs-lookup"><span data-stu-id="bd7a2-115">Remarks</span></span>

<span data-ttu-id="bd7a2-116">這個方法一律會存取第一個 mip 層級。</span><span class="sxs-lookup"><span data-stu-id="bd7a2-116">This method always accesses the first mip level.</span></span> <span data-ttu-id="bd7a2-117">若要指定其他 mip 層級，請改用 [**mip \[ \] \[ \] . 運算子**](sm5-object-texture1d-mipsoperatorindex.md)。</span><span class="sxs-lookup"><span data-stu-id="bd7a2-117">To specify other mip levels, use the [**mip.operator\[\]\[\]**](sm5-object-texture1d-mipsoperatorindex.md) instead.</span></span>

<span data-ttu-id="bd7a2-118">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="bd7a2-118">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="bd7a2-119">頂點</span><span class="sxs-lookup"><span data-stu-id="bd7a2-119">Vertex</span></span> | <span data-ttu-id="bd7a2-120">船體</span><span class="sxs-lookup"><span data-stu-id="bd7a2-120">Hull</span></span> | <span data-ttu-id="bd7a2-121">網域</span><span class="sxs-lookup"><span data-stu-id="bd7a2-121">Domain</span></span> | <span data-ttu-id="bd7a2-122">幾何</span><span class="sxs-lookup"><span data-stu-id="bd7a2-122">Geometry</span></span> | <span data-ttu-id="bd7a2-123">像素</span><span class="sxs-lookup"><span data-stu-id="bd7a2-123">Pixel</span></span> | <span data-ttu-id="bd7a2-124">計算</span><span class="sxs-lookup"><span data-stu-id="bd7a2-124">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="bd7a2-125">x</span><span class="sxs-lookup"><span data-stu-id="bd7a2-125">x</span></span>      | <span data-ttu-id="bd7a2-126">x</span><span class="sxs-lookup"><span data-stu-id="bd7a2-126">x</span></span>    | <span data-ttu-id="bd7a2-127">x</span><span class="sxs-lookup"><span data-stu-id="bd7a2-127">x</span></span>      | <span data-ttu-id="bd7a2-128">x</span><span class="sxs-lookup"><span data-stu-id="bd7a2-128">x</span></span>        | <span data-ttu-id="bd7a2-129">x</span><span class="sxs-lookup"><span data-stu-id="bd7a2-129">x</span></span>     | <span data-ttu-id="bd7a2-130">x</span><span class="sxs-lookup"><span data-stu-id="bd7a2-130">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="bd7a2-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bd7a2-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd7a2-132">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bd7a2-132">Texture1D</span></span>](sm5-object-texture1d.md)
</dt> <dt>

[<span data-ttu-id="bd7a2-133">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="bd7a2-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




