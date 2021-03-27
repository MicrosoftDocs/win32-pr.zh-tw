---
title: Texture2DArray：： mips。Operator 函數
description: 傳回唯讀的資源變數。 |Texture2DArray：： mips。Operator 函數
ms.assetid: 66639bf6-74dd-4c69-9cc1-74cc9314de57
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
ms.openlocfilehash: 17f24dd54768f3583f508527b7e03f72399bf98e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "103696501"
---
# <a name="texture2darraymipsoperator----function"></a><span data-ttu-id="8d276-105">Texture2DArray：： mips。Operator 函數</span><span class="sxs-lookup"><span data-stu-id="8d276-105">Texture2DArray::mips.Operator    function</span></span>

<span data-ttu-id="8d276-106">傳回唯讀的資源變數。</span><span class="sxs-lookup"><span data-stu-id="8d276-106">Returns a read-only resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d276-107">語法</span><span class="sxs-lookup"><span data-stu-id="8d276-107">Syntax</span></span>

``` syntax
R mips.Operator[][](
  in uint mipSlice,
  in uint3 pos
);
```

## <a name="parameters"></a><span data-ttu-id="8d276-108">參數</span><span class="sxs-lookup"><span data-stu-id="8d276-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d276-109">*mipSlice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8d276-109">*mipSlice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d276-110">類型： **uint**</span><span class="sxs-lookup"><span data-stu-id="8d276-110">Type: **uint**</span></span>

<span data-ttu-id="8d276-111">Mip 配量索引。</span><span class="sxs-lookup"><span data-stu-id="8d276-111">The mip slice index.</span></span>

</dd> <dt>

<span data-ttu-id="8d276-112">*pos* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8d276-112">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d276-113">類型： **uint3**</span><span class="sxs-lookup"><span data-stu-id="8d276-113">Type: **uint3**</span></span>

<span data-ttu-id="8d276-114">索引位置。</span><span class="sxs-lookup"><span data-stu-id="8d276-114">The index position.</span></span> <span data-ttu-id="8d276-115">第一個和第二個元件包含 (x，y) 座標。</span><span class="sxs-lookup"><span data-stu-id="8d276-115">The first and second components contain the (x, y) coordinates.</span></span> <span data-ttu-id="8d276-116">第三個元件表示所要的陣列配量。</span><span class="sxs-lookup"><span data-stu-id="8d276-116">The third component indicates the desired array slice.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d276-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="8d276-117">Return value</span></span>

<span data-ttu-id="8d276-118">類型： **R**</span><span class="sxs-lookup"><span data-stu-id="8d276-118">Type: **R**</span></span>

<span data-ttu-id="8d276-119">唯讀的資源變數。</span><span class="sxs-lookup"><span data-stu-id="8d276-119">A read-only resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="8d276-120">備註</span><span class="sxs-lookup"><span data-stu-id="8d276-120">Remarks</span></span>

### <a name="usage-example"></a><span data-ttu-id="8d276-121">使用範例</span><span class="sxs-lookup"><span data-stu-id="8d276-121">Usage Example</span></span>


```
Texture2DArray<float4> tex;
uint mip = 2;
uint2 pos_xy_and_array = {123, 456, 3};
float4 f = tex.mips[mip][pos_xy_and_array];
        
```



<span data-ttu-id="8d276-122">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="8d276-122">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="8d276-123">頂點</span><span class="sxs-lookup"><span data-stu-id="8d276-123">Vertex</span></span> | <span data-ttu-id="8d276-124">船體</span><span class="sxs-lookup"><span data-stu-id="8d276-124">Hull</span></span> | <span data-ttu-id="8d276-125">網域</span><span class="sxs-lookup"><span data-stu-id="8d276-125">Domain</span></span> | <span data-ttu-id="8d276-126">幾何</span><span class="sxs-lookup"><span data-stu-id="8d276-126">Geometry</span></span> | <span data-ttu-id="8d276-127">像素</span><span class="sxs-lookup"><span data-stu-id="8d276-127">Pixel</span></span> | <span data-ttu-id="8d276-128">計算</span><span class="sxs-lookup"><span data-stu-id="8d276-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="8d276-129">x</span><span class="sxs-lookup"><span data-stu-id="8d276-129">x</span></span>      | <span data-ttu-id="8d276-130">x</span><span class="sxs-lookup"><span data-stu-id="8d276-130">x</span></span>    | <span data-ttu-id="8d276-131">x</span><span class="sxs-lookup"><span data-stu-id="8d276-131">x</span></span>      | <span data-ttu-id="8d276-132">x</span><span class="sxs-lookup"><span data-stu-id="8d276-132">x</span></span>        | <span data-ttu-id="8d276-133">x</span><span class="sxs-lookup"><span data-stu-id="8d276-133">x</span></span>     | <span data-ttu-id="8d276-134">x</span><span class="sxs-lookup"><span data-stu-id="8d276-134">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="8d276-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8d276-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d276-136">Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="8d276-136">Texture2DArray</span></span>](sm5-object-texture2darray.md)
</dt> <dt>

[<span data-ttu-id="8d276-137">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="8d276-137">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




