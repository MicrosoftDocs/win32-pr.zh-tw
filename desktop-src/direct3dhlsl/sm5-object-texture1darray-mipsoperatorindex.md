---
title: Texture1DArray：： mips。Operator 函數
description: 傳回唯讀的資源變數。 |Texture1DArray：： mips。Operator 函數
ms.assetid: b8f2ef78-4b50-4051-a00f-5b81cd77d1e0
keywords:
- Mips。運算子函式 HLSL
topic_type:
- apiref
api_name:
- mips.Operator
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cbe2d1116839cede8dda69f1b0b8cf9a049595e9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104035282"
---
# <a name="texture1darraymipsoperator----function"></a><span data-ttu-id="68d6f-105">Texture1DArray：： mips。Operator 函數</span><span class="sxs-lookup"><span data-stu-id="68d6f-105">Texture1DArray::mips.Operator    function</span></span>

<span data-ttu-id="68d6f-106">傳回唯讀的資源變數。</span><span class="sxs-lookup"><span data-stu-id="68d6f-106">Returns a read-only resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="68d6f-107">語法</span><span class="sxs-lookup"><span data-stu-id="68d6f-107">Syntax</span></span>

``` syntax
R mips.Operator[][](
  in uint mipSlice,
  in uint2 pos
);
```

## <a name="parameters"></a><span data-ttu-id="68d6f-108">參數</span><span class="sxs-lookup"><span data-stu-id="68d6f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68d6f-109">*mipSlice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="68d6f-109">*mipSlice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68d6f-110">類型： **uint**</span><span class="sxs-lookup"><span data-stu-id="68d6f-110">Type: **uint**</span></span>

<span data-ttu-id="68d6f-111">Mip 配量索引。</span><span class="sxs-lookup"><span data-stu-id="68d6f-111">The mip slice index.</span></span>

</dd> <dt>

<span data-ttu-id="68d6f-112">*pos* \[在\]</span><span class="sxs-lookup"><span data-stu-id="68d6f-112">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68d6f-113">類型： **uint2**</span><span class="sxs-lookup"><span data-stu-id="68d6f-113">Type: **uint2**</span></span>

<span data-ttu-id="68d6f-114">索引位置。</span><span class="sxs-lookup"><span data-stu-id="68d6f-114">The index position.</span></span> <span data-ttu-id="68d6f-115">第一個元件包含 x 座標。</span><span class="sxs-lookup"><span data-stu-id="68d6f-115">The first component contains the x-coordinate.</span></span> <span data-ttu-id="68d6f-116">第二個元件表示所要的陣列配量。</span><span class="sxs-lookup"><span data-stu-id="68d6f-116">The second component indicates the desired array slice.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68d6f-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="68d6f-117">Return value</span></span>

<span data-ttu-id="68d6f-118">類型： **R**</span><span class="sxs-lookup"><span data-stu-id="68d6f-118">Type: **R**</span></span>

<span data-ttu-id="68d6f-119">唯讀的資源變數。</span><span class="sxs-lookup"><span data-stu-id="68d6f-119">A read-only resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="68d6f-120">備註</span><span class="sxs-lookup"><span data-stu-id="68d6f-120">Remarks</span></span>

### <a name="usage-example"></a><span data-ttu-id="68d6f-121">使用範例</span><span class="sxs-lookup"><span data-stu-id="68d6f-121">Usage Example</span></span>


```
Texture1DArray<float4> tex;
uint mip = 2;
uint2 pos_x_and_array = {1234, 3};
float4 f = tex.mips[mip][pos_x_and_array];        
        
```



<span data-ttu-id="68d6f-122">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="68d6f-122">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="68d6f-123">頂點</span><span class="sxs-lookup"><span data-stu-id="68d6f-123">Vertex</span></span> | <span data-ttu-id="68d6f-124">船體</span><span class="sxs-lookup"><span data-stu-id="68d6f-124">Hull</span></span> | <span data-ttu-id="68d6f-125">網域</span><span class="sxs-lookup"><span data-stu-id="68d6f-125">Domain</span></span> | <span data-ttu-id="68d6f-126">幾何</span><span class="sxs-lookup"><span data-stu-id="68d6f-126">Geometry</span></span> | <span data-ttu-id="68d6f-127">像素</span><span class="sxs-lookup"><span data-stu-id="68d6f-127">Pixel</span></span> | <span data-ttu-id="68d6f-128">計算</span><span class="sxs-lookup"><span data-stu-id="68d6f-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="68d6f-129">x</span><span class="sxs-lookup"><span data-stu-id="68d6f-129">x</span></span>      | <span data-ttu-id="68d6f-130">x</span><span class="sxs-lookup"><span data-stu-id="68d6f-130">x</span></span>    | <span data-ttu-id="68d6f-131">x</span><span class="sxs-lookup"><span data-stu-id="68d6f-131">x</span></span>      | <span data-ttu-id="68d6f-132">x</span><span class="sxs-lookup"><span data-stu-id="68d6f-132">x</span></span>        | <span data-ttu-id="68d6f-133">x</span><span class="sxs-lookup"><span data-stu-id="68d6f-133">x</span></span>     | <span data-ttu-id="68d6f-134">x</span><span class="sxs-lookup"><span data-stu-id="68d6f-134">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="68d6f-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="68d6f-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68d6f-136">Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="68d6f-136">Texture1DArray</span></span>](sm5-object-texture1darray.md)
</dt> <dt>

[<span data-ttu-id="68d6f-137">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="68d6f-137">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




