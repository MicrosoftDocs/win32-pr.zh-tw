---
title: ddx_coarse 函式
description: 計算相對於螢幕空間 x 座標的低精確度部分衍生。
ms.assetid: 5719f45d-b2ae-4916-8f31-c2797b661814
keywords:
- ddx_coarse 函式 HLSL
topic_type:
- apiref
api_name:
- ddx_coarse
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4f9d4805a1d516a5d8980fcd8209fd6733fe86c4
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104022609"
---
# <a name="ddx_coarse-function"></a><span data-ttu-id="a4006-104">ddx \_ 粗略函數</span><span class="sxs-lookup"><span data-stu-id="a4006-104">ddx\_coarse function</span></span>

<span data-ttu-id="a4006-105">計算相對於螢幕空間 x 座標的低精確度部分衍生。</span><span class="sxs-lookup"><span data-stu-id="a4006-105">Computes a low precision partial derivative with respect to the screen-space x-coordinate.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4006-106">語法</span><span class="sxs-lookup"><span data-stu-id="a4006-106">Syntax</span></span>

``` syntax
float ddx_coarse(
  in float value
);
```

## <a name="parameters"></a><span data-ttu-id="a4006-107">參數</span><span class="sxs-lookup"><span data-stu-id="a4006-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4006-108">*值* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a4006-108">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4006-109">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="a4006-109">Type: **float**</span></span>

<span data-ttu-id="a4006-110">輸入值。</span><span class="sxs-lookup"><span data-stu-id="a4006-110">The input value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4006-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="a4006-111">Return value</span></span>

<span data-ttu-id="a4006-112">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="a4006-112">Type: **float**</span></span>

<span data-ttu-id="a4006-113">*值* 的低精確度部分衍生。</span><span class="sxs-lookup"><span data-stu-id="a4006-113">The low precision partial derivative of *value*.</span></span>

## <a name="remarks"></a><span data-ttu-id="a4006-114">備註</span><span class="sxs-lookup"><span data-stu-id="a4006-114">Remarks</span></span>

<span data-ttu-id="a4006-115">您也可以使用下列多載版本：</span><span class="sxs-lookup"><span data-stu-id="a4006-115">The following overloaded versions are also available:</span></span>

``` syntax
float2 ddx_coarse(float2 value);
float3 ddx_coarse(float3 value);
float4 ddx_coarse(float4 value);
```

### <a name="minimum-shader-model"></a><span data-ttu-id="a4006-116">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="a4006-116">Minimum Shader Model</span></span>

<span data-ttu-id="a4006-117">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="a4006-117">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="a4006-118">著色器模型</span><span class="sxs-lookup"><span data-stu-id="a4006-118">Shader Model</span></span>                                                                | <span data-ttu-id="a4006-119">支援</span><span class="sxs-lookup"><span data-stu-id="a4006-119">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="a4006-120">[著色器模型 5](d3d11-graphics-reference-sm5.md) 和更新版本的著色器模型</span><span class="sxs-lookup"><span data-stu-id="a4006-120">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="a4006-121">是</span><span class="sxs-lookup"><span data-stu-id="a4006-121">yes</span></span>       |



 

<span data-ttu-id="a4006-122">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="a4006-122">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="a4006-123">頂點</span><span class="sxs-lookup"><span data-stu-id="a4006-123">Vertex</span></span> | <span data-ttu-id="a4006-124">船體</span><span class="sxs-lookup"><span data-stu-id="a4006-124">Hull</span></span> | <span data-ttu-id="a4006-125">網域</span><span class="sxs-lookup"><span data-stu-id="a4006-125">Domain</span></span> | <span data-ttu-id="a4006-126">幾何</span><span class="sxs-lookup"><span data-stu-id="a4006-126">Geometry</span></span> | <span data-ttu-id="a4006-127">像素</span><span class="sxs-lookup"><span data-stu-id="a4006-127">Pixel</span></span> | <span data-ttu-id="a4006-128">計算</span><span class="sxs-lookup"><span data-stu-id="a4006-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="a4006-129">x</span><span class="sxs-lookup"><span data-stu-id="a4006-129">x</span></span>     |         |



 

## <a name="see-also"></a><span data-ttu-id="a4006-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a4006-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4006-131">內建函式</span><span class="sxs-lookup"><span data-stu-id="a4006-131">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="a4006-132">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="a4006-132">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




