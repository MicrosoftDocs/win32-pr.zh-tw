---
title: ddx_fine 函式
description: 計算相對於螢幕空間 x 座標的高精確度部分衍生。 |ddx_fine 函式
ms.assetid: 41062d6f-2b7f-4594-a6de-da37ded5d444
keywords:
- ddx_fine 函式 HLSL
topic_type:
- apiref
api_name:
- ddx_fine
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c1a579ba5899cf4d3ac3f25ef5a40337f6291977
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104974432"
---
# <a name="ddx_fine-function"></a><span data-ttu-id="2bfbb-105">ddx \_ 精細函數</span><span class="sxs-lookup"><span data-stu-id="2bfbb-105">ddx\_fine function</span></span>

<span data-ttu-id="2bfbb-106">計算相對於螢幕空間 x 座標的高精確度部分衍生。</span><span class="sxs-lookup"><span data-stu-id="2bfbb-106">Computes a high precision partial derivative with respect to the screen-space x-coordinate.</span></span>

## <a name="syntax"></a><span data-ttu-id="2bfbb-107">語法</span><span class="sxs-lookup"><span data-stu-id="2bfbb-107">Syntax</span></span>

``` syntax
float ddx_fine(
  in float value
);
```

## <a name="parameters"></a><span data-ttu-id="2bfbb-108">參數</span><span class="sxs-lookup"><span data-stu-id="2bfbb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2bfbb-109">*值* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2bfbb-109">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2bfbb-110">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="2bfbb-110">Type: **float**</span></span>

<span data-ttu-id="2bfbb-111">輸入值。</span><span class="sxs-lookup"><span data-stu-id="2bfbb-111">The input value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2bfbb-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="2bfbb-112">Return value</span></span>

<span data-ttu-id="2bfbb-113">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="2bfbb-113">Type: **float**</span></span>

<span data-ttu-id="2bfbb-114">*值* 的高精確度部分衍生。</span><span class="sxs-lookup"><span data-stu-id="2bfbb-114">The high precision partial derivative of *value*.</span></span>

## <a name="remarks"></a><span data-ttu-id="2bfbb-115">備註</span><span class="sxs-lookup"><span data-stu-id="2bfbb-115">Remarks</span></span>

<span data-ttu-id="2bfbb-116">您也可以使用下列多載版本：</span><span class="sxs-lookup"><span data-stu-id="2bfbb-116">The following overloaded versions are also available:</span></span>

``` syntax
float2 ddx_fine(float2 value);
float3 ddx_fine(float3 value);
float4 ddx_fine(float4 value);
```

### <a name="minimum-shader-model"></a><span data-ttu-id="2bfbb-117">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="2bfbb-117">Minimum Shader Model</span></span>

<span data-ttu-id="2bfbb-118">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="2bfbb-118">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="2bfbb-119">著色器模型</span><span class="sxs-lookup"><span data-stu-id="2bfbb-119">Shader Model</span></span>                                                                | <span data-ttu-id="2bfbb-120">支援</span><span class="sxs-lookup"><span data-stu-id="2bfbb-120">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="2bfbb-121">[著色器模型 5](d3d11-graphics-reference-sm5.md) 和更新版本的著色器模型</span><span class="sxs-lookup"><span data-stu-id="2bfbb-121">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="2bfbb-122">是</span><span class="sxs-lookup"><span data-stu-id="2bfbb-122">yes</span></span>       |



 

<span data-ttu-id="2bfbb-123">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="2bfbb-123">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="2bfbb-124">頂點</span><span class="sxs-lookup"><span data-stu-id="2bfbb-124">Vertex</span></span> | <span data-ttu-id="2bfbb-125">船體</span><span class="sxs-lookup"><span data-stu-id="2bfbb-125">Hull</span></span> | <span data-ttu-id="2bfbb-126">網域</span><span class="sxs-lookup"><span data-stu-id="2bfbb-126">Domain</span></span> | <span data-ttu-id="2bfbb-127">幾何</span><span class="sxs-lookup"><span data-stu-id="2bfbb-127">Geometry</span></span> | <span data-ttu-id="2bfbb-128">像素</span><span class="sxs-lookup"><span data-stu-id="2bfbb-128">Pixel</span></span> | <span data-ttu-id="2bfbb-129">計算</span><span class="sxs-lookup"><span data-stu-id="2bfbb-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="2bfbb-130">x</span><span class="sxs-lookup"><span data-stu-id="2bfbb-130">x</span></span>     |         |



 

## <a name="see-also"></a><span data-ttu-id="2bfbb-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2bfbb-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2bfbb-132">內建函式</span><span class="sxs-lookup"><span data-stu-id="2bfbb-132">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="2bfbb-133">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="2bfbb-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




