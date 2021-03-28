---
title: Texture2D：： mips。Operator 函數
description: 傳回唯讀的資源變數。 |Texture2D：： mips。Operator 函數
ms.assetid: 201996a7-741f-4457-ab77-9cd653f3682b
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
ms.openlocfilehash: 994ede49563b1d4e568769be48a0e60592fe3dde
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104973957"
---
# <a name="texture2dmipsoperator----function"></a><span data-ttu-id="15a39-105">Texture2D：： mips。Operator 函數</span><span class="sxs-lookup"><span data-stu-id="15a39-105">Texture2D::mips.Operator    function</span></span>

<span data-ttu-id="15a39-106">傳回唯讀的資源變數。</span><span class="sxs-lookup"><span data-stu-id="15a39-106">Returns a read-only resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="15a39-107">語法</span><span class="sxs-lookup"><span data-stu-id="15a39-107">Syntax</span></span>

``` syntax
R mips.Operator[][](
  in uint mipSlice,
  in uint2 pos
);
```

## <a name="parameters"></a><span data-ttu-id="15a39-108">參數</span><span class="sxs-lookup"><span data-stu-id="15a39-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15a39-109">*mipSlice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="15a39-109">*mipSlice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15a39-110">類型： **uint**</span><span class="sxs-lookup"><span data-stu-id="15a39-110">Type: **uint**</span></span>

<span data-ttu-id="15a39-111">Mip 配量索引。</span><span class="sxs-lookup"><span data-stu-id="15a39-111">The mip slice index.</span></span>

</dd> <dt>

<span data-ttu-id="15a39-112">*pos* \[在\]</span><span class="sxs-lookup"><span data-stu-id="15a39-112">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15a39-113">類型： **uint2**</span><span class="sxs-lookup"><span data-stu-id="15a39-113">Type: **uint2**</span></span>

<span data-ttu-id="15a39-114">索引位置。</span><span class="sxs-lookup"><span data-stu-id="15a39-114">The index position.</span></span> <span data-ttu-id="15a39-115">包含 (x，y) 座標。</span><span class="sxs-lookup"><span data-stu-id="15a39-115">Contains the (x, y) coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15a39-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="15a39-116">Return value</span></span>

<span data-ttu-id="15a39-117">類型： **R**</span><span class="sxs-lookup"><span data-stu-id="15a39-117">Type: **R**</span></span>

<span data-ttu-id="15a39-118">唯讀的資源變數。</span><span class="sxs-lookup"><span data-stu-id="15a39-118">A read-only resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="15a39-119">備註</span><span class="sxs-lookup"><span data-stu-id="15a39-119">Remarks</span></span>

### <a name="usage-example"></a><span data-ttu-id="15a39-120">使用範例</span><span class="sxs-lookup"><span data-stu-id="15a39-120">Usage Example</span></span>


```
Texture2D<float4> tex;
uint mip = 2;
uint2 pos_xy = {123, 456};
float4 f = tex.mips[mip][pos_xy];
        
```



<span data-ttu-id="15a39-121">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="15a39-121">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="15a39-122">頂點</span><span class="sxs-lookup"><span data-stu-id="15a39-122">Vertex</span></span> | <span data-ttu-id="15a39-123">船體</span><span class="sxs-lookup"><span data-stu-id="15a39-123">Hull</span></span> | <span data-ttu-id="15a39-124">網域</span><span class="sxs-lookup"><span data-stu-id="15a39-124">Domain</span></span> | <span data-ttu-id="15a39-125">幾何</span><span class="sxs-lookup"><span data-stu-id="15a39-125">Geometry</span></span> | <span data-ttu-id="15a39-126">像素</span><span class="sxs-lookup"><span data-stu-id="15a39-126">Pixel</span></span> | <span data-ttu-id="15a39-127">計算</span><span class="sxs-lookup"><span data-stu-id="15a39-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="15a39-128">x</span><span class="sxs-lookup"><span data-stu-id="15a39-128">x</span></span>      | <span data-ttu-id="15a39-129">x</span><span class="sxs-lookup"><span data-stu-id="15a39-129">x</span></span>    | <span data-ttu-id="15a39-130">x</span><span class="sxs-lookup"><span data-stu-id="15a39-130">x</span></span>      | <span data-ttu-id="15a39-131">x</span><span class="sxs-lookup"><span data-stu-id="15a39-131">x</span></span>        | <span data-ttu-id="15a39-132">x</span><span class="sxs-lookup"><span data-stu-id="15a39-132">x</span></span>     | <span data-ttu-id="15a39-133">x</span><span class="sxs-lookup"><span data-stu-id="15a39-133">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="15a39-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="15a39-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15a39-135">Texture2D</span><span class="sxs-lookup"><span data-stu-id="15a39-135">Texture2D</span></span>](sm5-object-texture2d.md)
</dt> <dt>

[<span data-ttu-id="15a39-136">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="15a39-136">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




