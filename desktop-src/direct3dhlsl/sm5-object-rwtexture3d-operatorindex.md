---
title: RWTexture3D：： Operator 函數
description: 傳回 RWTexture3D 的資源變數。
ms.assetid: 0b4ea895-ac34-49e5-80e6-74229c33bfe9
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
ms.openlocfilehash: e41ff4db387c4d0926083419082fd589005d96a6
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104971840"
---
# <a name="rwtexture3doperator--function"></a><span data-ttu-id="666f9-104">RWTexture3D：： Operator 函數</span><span class="sxs-lookup"><span data-stu-id="666f9-104">RWTexture3D::Operator  function</span></span>

<span data-ttu-id="666f9-105">傳回 [**RWTexture3D**](sm5-object-rwtexture3d.md)的資源變數。</span><span class="sxs-lookup"><span data-stu-id="666f9-105">Returns a resource variable of a [**RWTexture3D**](sm5-object-rwtexture3d.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="666f9-106">語法</span><span class="sxs-lookup"><span data-stu-id="666f9-106">Syntax</span></span>

``` syntax
R Operator[](
  in uint3 pos
);
```

## <a name="parameters"></a><span data-ttu-id="666f9-107">參數</span><span class="sxs-lookup"><span data-stu-id="666f9-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="666f9-108">*pos* \[在\]</span><span class="sxs-lookup"><span data-stu-id="666f9-108">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="666f9-109">類型： **uint3**</span><span class="sxs-lookup"><span data-stu-id="666f9-109">Type: **uint3**</span></span>

<span data-ttu-id="666f9-110">索引位置。</span><span class="sxs-lookup"><span data-stu-id="666f9-110">The index position.</span></span> <span data-ttu-id="666f9-111">包含 (x，y，z) 座標。</span><span class="sxs-lookup"><span data-stu-id="666f9-111">Contains the (x, y, z) coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="666f9-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="666f9-112">Return value</span></span>

<span data-ttu-id="666f9-113">類型： **R**</span><span class="sxs-lookup"><span data-stu-id="666f9-113">Type: **R**</span></span>

<span data-ttu-id="666f9-114">資源變數。</span><span class="sxs-lookup"><span data-stu-id="666f9-114">A resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="666f9-115">備註</span><span class="sxs-lookup"><span data-stu-id="666f9-115">Remarks</span></span>

<span data-ttu-id="666f9-116">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="666f9-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="666f9-117">頂點</span><span class="sxs-lookup"><span data-stu-id="666f9-117">Vertex</span></span> | <span data-ttu-id="666f9-118">船體</span><span class="sxs-lookup"><span data-stu-id="666f9-118">Hull</span></span> | <span data-ttu-id="666f9-119">網域</span><span class="sxs-lookup"><span data-stu-id="666f9-119">Domain</span></span> | <span data-ttu-id="666f9-120">幾何</span><span class="sxs-lookup"><span data-stu-id="666f9-120">Geometry</span></span> | <span data-ttu-id="666f9-121">像素</span><span class="sxs-lookup"><span data-stu-id="666f9-121">Pixel</span></span> | <span data-ttu-id="666f9-122">計算</span><span class="sxs-lookup"><span data-stu-id="666f9-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="666f9-123">x</span><span class="sxs-lookup"><span data-stu-id="666f9-123">x</span></span>     | <span data-ttu-id="666f9-124">x</span><span class="sxs-lookup"><span data-stu-id="666f9-124">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="666f9-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="666f9-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="666f9-126">RWTexture3D</span><span class="sxs-lookup"><span data-stu-id="666f9-126">RWTexture3D</span></span>](sm5-object-rwtexture3d.md)
</dt> <dt>

[<span data-ttu-id="666f9-127">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="666f9-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




