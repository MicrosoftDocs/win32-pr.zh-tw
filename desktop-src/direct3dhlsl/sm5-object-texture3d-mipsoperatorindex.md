---
title: Texture3D：： mips。Operator 函數
description: 傳回唯讀的資源變數。 |Texture3D：： mips。Operator 函數
ms.assetid: d5f6cb3b-4163-44c2-8379-ac8a412b1aa6
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
ms.openlocfilehash: e8f7064459354ec4827ba6d96795e82ccab3800c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104195933"
---
# <a name="texture3dmipsoperator----function"></a><span data-ttu-id="ddf50-105">Texture3D：： mips。Operator 函數</span><span class="sxs-lookup"><span data-stu-id="ddf50-105">Texture3D::mips.Operator    function</span></span>

<span data-ttu-id="ddf50-106">傳回唯讀的資源變數。</span><span class="sxs-lookup"><span data-stu-id="ddf50-106">Returns a read-only resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="ddf50-107">語法</span><span class="sxs-lookup"><span data-stu-id="ddf50-107">Syntax</span></span>

``` syntax
R mips.Operator[][](
  in uint mipSlice,
  in uint3 pos
);
```

## <a name="parameters"></a><span data-ttu-id="ddf50-108">參數</span><span class="sxs-lookup"><span data-stu-id="ddf50-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ddf50-109">*mipSlice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ddf50-109">*mipSlice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ddf50-110">類型： **uint**</span><span class="sxs-lookup"><span data-stu-id="ddf50-110">Type: **uint**</span></span>

<span data-ttu-id="ddf50-111">Mip 配量索引。</span><span class="sxs-lookup"><span data-stu-id="ddf50-111">The mip slice index.</span></span>

</dd> <dt>

<span data-ttu-id="ddf50-112">*pos* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ddf50-112">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ddf50-113">類型： **uint3**</span><span class="sxs-lookup"><span data-stu-id="ddf50-113">Type: **uint3**</span></span>

<span data-ttu-id="ddf50-114">索引位置。</span><span class="sxs-lookup"><span data-stu-id="ddf50-114">The index position.</span></span> <span data-ttu-id="ddf50-115">包含 (x，y，z) 座標。</span><span class="sxs-lookup"><span data-stu-id="ddf50-115">Contains the (x, y, z) coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ddf50-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="ddf50-116">Return value</span></span>

<span data-ttu-id="ddf50-117">類型： **R**</span><span class="sxs-lookup"><span data-stu-id="ddf50-117">Type: **R**</span></span>

<span data-ttu-id="ddf50-118">唯讀的資源變數。</span><span class="sxs-lookup"><span data-stu-id="ddf50-118">A read-only resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="ddf50-119">備註</span><span class="sxs-lookup"><span data-stu-id="ddf50-119">Remarks</span></span>

### <a name="usage-example"></a><span data-ttu-id="ddf50-120">使用範例</span><span class="sxs-lookup"><span data-stu-id="ddf50-120">Usage Example</span></span>


```
Texture3D<float4> tex;
uint mip = 2;
uint3 pos_xyz = {123, 456, 789};
float4 f = tex.mips[mip][pos_xyz];
        
```



<span data-ttu-id="ddf50-121">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="ddf50-121">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="ddf50-122">頂點</span><span class="sxs-lookup"><span data-stu-id="ddf50-122">Vertex</span></span> | <span data-ttu-id="ddf50-123">船體</span><span class="sxs-lookup"><span data-stu-id="ddf50-123">Hull</span></span> | <span data-ttu-id="ddf50-124">網域</span><span class="sxs-lookup"><span data-stu-id="ddf50-124">Domain</span></span> | <span data-ttu-id="ddf50-125">幾何</span><span class="sxs-lookup"><span data-stu-id="ddf50-125">Geometry</span></span> | <span data-ttu-id="ddf50-126">像素</span><span class="sxs-lookup"><span data-stu-id="ddf50-126">Pixel</span></span> | <span data-ttu-id="ddf50-127">計算</span><span class="sxs-lookup"><span data-stu-id="ddf50-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="ddf50-128">x</span><span class="sxs-lookup"><span data-stu-id="ddf50-128">x</span></span>      | <span data-ttu-id="ddf50-129">x</span><span class="sxs-lookup"><span data-stu-id="ddf50-129">x</span></span>    | <span data-ttu-id="ddf50-130">x</span><span class="sxs-lookup"><span data-stu-id="ddf50-130">x</span></span>      | <span data-ttu-id="ddf50-131">x</span><span class="sxs-lookup"><span data-stu-id="ddf50-131">x</span></span>        | <span data-ttu-id="ddf50-132">x</span><span class="sxs-lookup"><span data-stu-id="ddf50-132">x</span></span>     | <span data-ttu-id="ddf50-133">x</span><span class="sxs-lookup"><span data-stu-id="ddf50-133">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="ddf50-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ddf50-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ddf50-135">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ddf50-135">Texture3D</span></span>](sm5-object-texture3d.md)
</dt> <dt>

[<span data-ttu-id="ddf50-136">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="ddf50-136">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




