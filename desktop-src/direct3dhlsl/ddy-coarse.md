---
title: ddy_coarse 函式
description: 計算相對於螢幕空間 y 座標的低精確度部分衍生。
ms.assetid: f6103cd3-f7ee-41c2-b3cf-9e72ca84b25e
keywords:
- ddy_coarse 函式 HLSL
topic_type:
- apiref
api_name:
- ddy_coarse
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b6fef330e919a31e39306742bb03280454d47626
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104022608"
---
# <a name="ddy_coarse-function"></a><span data-ttu-id="26256-104">ddy \_ 粗略函數</span><span class="sxs-lookup"><span data-stu-id="26256-104">ddy\_coarse function</span></span>

<span data-ttu-id="26256-105">計算相對於螢幕空間 y 座標的低精確度部分衍生。</span><span class="sxs-lookup"><span data-stu-id="26256-105">Computes a low precision partial derivative with respect to the screen-space y-coordinate.</span></span>

## <a name="syntax"></a><span data-ttu-id="26256-106">語法</span><span class="sxs-lookup"><span data-stu-id="26256-106">Syntax</span></span>

``` syntax
float ddy_coarse(
  in float value
);
```

## <a name="parameters"></a><span data-ttu-id="26256-107">參數</span><span class="sxs-lookup"><span data-stu-id="26256-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26256-108">*值* \[在\]</span><span class="sxs-lookup"><span data-stu-id="26256-108">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26256-109">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="26256-109">Type: **float**</span></span>

<span data-ttu-id="26256-110">輸入值。</span><span class="sxs-lookup"><span data-stu-id="26256-110">The input value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26256-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="26256-111">Return value</span></span>

<span data-ttu-id="26256-112">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="26256-112">Type: **float**</span></span>

<span data-ttu-id="26256-113">*值* 的低精確度部分衍生。</span><span class="sxs-lookup"><span data-stu-id="26256-113">The low precision partial derivative of *value*.</span></span>

## <a name="remarks"></a><span data-ttu-id="26256-114">備註</span><span class="sxs-lookup"><span data-stu-id="26256-114">Remarks</span></span>

<span data-ttu-id="26256-115">您也可以使用下列多載版本：</span><span class="sxs-lookup"><span data-stu-id="26256-115">The following overloaded versions are also available:</span></span>

``` syntax
float2 ddy_coarse(float2 value);
float3 ddy_coarse(float3 value);
float4 ddy_coarse(float4 value);
```

### <a name="minimum-shader-model"></a><span data-ttu-id="26256-116">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="26256-116">Minimum Shader Model</span></span>

<span data-ttu-id="26256-117">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="26256-117">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="26256-118">著色器模型</span><span class="sxs-lookup"><span data-stu-id="26256-118">Shader Model</span></span>                                                                | <span data-ttu-id="26256-119">支援</span><span class="sxs-lookup"><span data-stu-id="26256-119">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="26256-120">[著色器模型 5](d3d11-graphics-reference-sm5.md) 和更新版本的著色器模型</span><span class="sxs-lookup"><span data-stu-id="26256-120">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="26256-121">是</span><span class="sxs-lookup"><span data-stu-id="26256-121">yes</span></span>       |



 

<span data-ttu-id="26256-122">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="26256-122">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="26256-123">頂點</span><span class="sxs-lookup"><span data-stu-id="26256-123">Vertex</span></span> | <span data-ttu-id="26256-124">船體</span><span class="sxs-lookup"><span data-stu-id="26256-124">Hull</span></span> | <span data-ttu-id="26256-125">網域</span><span class="sxs-lookup"><span data-stu-id="26256-125">Domain</span></span> | <span data-ttu-id="26256-126">幾何</span><span class="sxs-lookup"><span data-stu-id="26256-126">Geometry</span></span> | <span data-ttu-id="26256-127">像素</span><span class="sxs-lookup"><span data-stu-id="26256-127">Pixel</span></span> | <span data-ttu-id="26256-128">計算</span><span class="sxs-lookup"><span data-stu-id="26256-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="26256-129">x</span><span class="sxs-lookup"><span data-stu-id="26256-129">x</span></span>     |         |



 

## <a name="see-also"></a><span data-ttu-id="26256-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="26256-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26256-131">內建函式</span><span class="sxs-lookup"><span data-stu-id="26256-131">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="26256-132">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="26256-132">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




