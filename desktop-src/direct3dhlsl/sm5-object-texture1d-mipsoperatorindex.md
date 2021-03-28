---
title: Texture1D：： mips。Operator 函數
description: 傳回唯讀資源變數或 Texture1D。
ms.assetid: 0b64f0d3-f9a1-474b-b229-d91d18922d5c
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
ms.openlocfilehash: 4713fe20fa52e948113a220969229c413c5dc4d1
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104317068"
---
# <a name="texture1dmipsoperator----function"></a><span data-ttu-id="1ae2d-104">Texture1D：： mips。Operator 函數</span><span class="sxs-lookup"><span data-stu-id="1ae2d-104">Texture1D::mips.Operator    function</span></span>

<span data-ttu-id="1ae2d-105">傳回唯讀資源變數或 [**Texture1D**](sm5-object-texture1d.md)。</span><span class="sxs-lookup"><span data-stu-id="1ae2d-105">Returns a read-only resource variable or a [**Texture1D**](sm5-object-texture1d.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="1ae2d-106">語法</span><span class="sxs-lookup"><span data-stu-id="1ae2d-106">Syntax</span></span>

``` syntax
R mips.Operator[][](
  in uint mipSlice,
  in uint pos
);
```

## <a name="parameters"></a><span data-ttu-id="1ae2d-107">參數</span><span class="sxs-lookup"><span data-stu-id="1ae2d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ae2d-108">*mipSlice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1ae2d-108">*mipSlice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ae2d-109">類型： **uint**</span><span class="sxs-lookup"><span data-stu-id="1ae2d-109">Type: **uint**</span></span>

<span data-ttu-id="1ae2d-110">Mip 配量索引。</span><span class="sxs-lookup"><span data-stu-id="1ae2d-110">The mip slice index.</span></span>

</dd> <dt>

<span data-ttu-id="1ae2d-111">*pos* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1ae2d-111">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ae2d-112">類型： **uint**</span><span class="sxs-lookup"><span data-stu-id="1ae2d-112">Type: **uint**</span></span>

<span data-ttu-id="1ae2d-113">索引位置。</span><span class="sxs-lookup"><span data-stu-id="1ae2d-113">The index position.</span></span> <span data-ttu-id="1ae2d-114">包含 x 座標。</span><span class="sxs-lookup"><span data-stu-id="1ae2d-114">Contains the x-coordinate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ae2d-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="1ae2d-115">Return value</span></span>

<span data-ttu-id="1ae2d-116">類型： **R**</span><span class="sxs-lookup"><span data-stu-id="1ae2d-116">Type: **R**</span></span>

<span data-ttu-id="1ae2d-117">唯讀的資源變數。</span><span class="sxs-lookup"><span data-stu-id="1ae2d-117">A read-only resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="1ae2d-118">備註</span><span class="sxs-lookup"><span data-stu-id="1ae2d-118">Remarks</span></span>

### <a name="usage-example"></a><span data-ttu-id="1ae2d-119">使用範例</span><span class="sxs-lookup"><span data-stu-id="1ae2d-119">Usage Example</span></span>


```
Texture1D<float4> tex;
uint mip = 2;
uint pos = 1234;
float4 f = tex.mips[mip][pos];
      
```



<span data-ttu-id="1ae2d-120">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="1ae2d-120">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="1ae2d-121">頂點</span><span class="sxs-lookup"><span data-stu-id="1ae2d-121">Vertex</span></span> | <span data-ttu-id="1ae2d-122">船體</span><span class="sxs-lookup"><span data-stu-id="1ae2d-122">Hull</span></span> | <span data-ttu-id="1ae2d-123">網域</span><span class="sxs-lookup"><span data-stu-id="1ae2d-123">Domain</span></span> | <span data-ttu-id="1ae2d-124">幾何</span><span class="sxs-lookup"><span data-stu-id="1ae2d-124">Geometry</span></span> | <span data-ttu-id="1ae2d-125">像素</span><span class="sxs-lookup"><span data-stu-id="1ae2d-125">Pixel</span></span> | <span data-ttu-id="1ae2d-126">計算</span><span class="sxs-lookup"><span data-stu-id="1ae2d-126">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="1ae2d-127">x</span><span class="sxs-lookup"><span data-stu-id="1ae2d-127">x</span></span>      | <span data-ttu-id="1ae2d-128">x</span><span class="sxs-lookup"><span data-stu-id="1ae2d-128">x</span></span>    | <span data-ttu-id="1ae2d-129">x</span><span class="sxs-lookup"><span data-stu-id="1ae2d-129">x</span></span>      | <span data-ttu-id="1ae2d-130">x</span><span class="sxs-lookup"><span data-stu-id="1ae2d-130">x</span></span>        | <span data-ttu-id="1ae2d-131">x</span><span class="sxs-lookup"><span data-stu-id="1ae2d-131">x</span></span>     | <span data-ttu-id="1ae2d-132">x</span><span class="sxs-lookup"><span data-stu-id="1ae2d-132">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="1ae2d-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1ae2d-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ae2d-134">Texture1D</span><span class="sxs-lookup"><span data-stu-id="1ae2d-134">Texture1D</span></span>](sm5-object-texture1d.md)
</dt> <dt>

[<span data-ttu-id="1ae2d-135">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="1ae2d-135">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




