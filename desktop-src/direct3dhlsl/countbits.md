---
title: countbits 函式
description: 計算輸入整數中每個元件)  (的位數。
ms.assetid: c4fafbc8-e21c-48cb-b433-8241a989ec85
keywords:
- countbits 函式 HLSL
topic_type:
- apiref
api_name:
- countbits
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 60d3cd63502c6217e6fb0b0ff17685b2d2b5bf25
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104022610"
---
# <a name="countbits-function"></a><span data-ttu-id="bb934-104">countbits 函式</span><span class="sxs-lookup"><span data-stu-id="bb934-104">countbits function</span></span>

<span data-ttu-id="bb934-105">計算輸入整數中每個元件)  (的位數。</span><span class="sxs-lookup"><span data-stu-id="bb934-105">Counts the number of bits (per component) in the input integer.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb934-106">語法</span><span class="sxs-lookup"><span data-stu-id="bb934-106">Syntax</span></span>

``` syntax
uint countbits(
  in uint value
);
```

## <a name="parameters"></a><span data-ttu-id="bb934-107">參數</span><span class="sxs-lookup"><span data-stu-id="bb934-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb934-108">*值* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bb934-108">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb934-109">類型： **uint**</span><span class="sxs-lookup"><span data-stu-id="bb934-109">Type: **uint**</span></span>

<span data-ttu-id="bb934-110">輸入值。</span><span class="sxs-lookup"><span data-stu-id="bb934-110">The input value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb934-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="bb934-111">Return value</span></span>

<span data-ttu-id="bb934-112">類型： **uint**</span><span class="sxs-lookup"><span data-stu-id="bb934-112">Type: **uint**</span></span>

<span data-ttu-id="bb934-113">位數。</span><span class="sxs-lookup"><span data-stu-id="bb934-113">The number of bits.</span></span>

## <a name="remarks"></a><span data-ttu-id="bb934-114">備註</span><span class="sxs-lookup"><span data-stu-id="bb934-114">Remarks</span></span>

<span data-ttu-id="bb934-115">您也可以使用下列多載版本：</span><span class="sxs-lookup"><span data-stu-id="bb934-115">The following overloaded versions are also available:</span></span>

``` syntax
uint count_bits(uint value);
uint2 count_bits(uint2 value);
uint3 count_bits(uint3 value);
uint4 count_bits(uint4 value);
```

### <a name="minimum-shader-model"></a><span data-ttu-id="bb934-116">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="bb934-116">Minimum Shader Model</span></span>

<span data-ttu-id="bb934-117">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="bb934-117">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="bb934-118">著色器模型</span><span class="sxs-lookup"><span data-stu-id="bb934-118">Shader Model</span></span>                                                                | <span data-ttu-id="bb934-119">支援</span><span class="sxs-lookup"><span data-stu-id="bb934-119">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="bb934-120">[著色器模型 5](d3d11-graphics-reference-sm5.md) 和更新版本的著色器模型</span><span class="sxs-lookup"><span data-stu-id="bb934-120">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="bb934-121">是</span><span class="sxs-lookup"><span data-stu-id="bb934-121">yes</span></span>       |



 

<span data-ttu-id="bb934-122">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="bb934-122">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="bb934-123">頂點</span><span class="sxs-lookup"><span data-stu-id="bb934-123">Vertex</span></span> | <span data-ttu-id="bb934-124">船體</span><span class="sxs-lookup"><span data-stu-id="bb934-124">Hull</span></span> | <span data-ttu-id="bb934-125">網域</span><span class="sxs-lookup"><span data-stu-id="bb934-125">Domain</span></span> | <span data-ttu-id="bb934-126">幾何</span><span class="sxs-lookup"><span data-stu-id="bb934-126">Geometry</span></span> | <span data-ttu-id="bb934-127">像素</span><span class="sxs-lookup"><span data-stu-id="bb934-127">Pixel</span></span> | <span data-ttu-id="bb934-128">計算</span><span class="sxs-lookup"><span data-stu-id="bb934-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="bb934-129">x</span><span class="sxs-lookup"><span data-stu-id="bb934-129">x</span></span>      | <span data-ttu-id="bb934-130">x</span><span class="sxs-lookup"><span data-stu-id="bb934-130">x</span></span>    | <span data-ttu-id="bb934-131">x</span><span class="sxs-lookup"><span data-stu-id="bb934-131">x</span></span>      | <span data-ttu-id="bb934-132">x</span><span class="sxs-lookup"><span data-stu-id="bb934-132">x</span></span>        | <span data-ttu-id="bb934-133">x</span><span class="sxs-lookup"><span data-stu-id="bb934-133">x</span></span>     | <span data-ttu-id="bb934-134">x</span><span class="sxs-lookup"><span data-stu-id="bb934-134">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="bb934-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bb934-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb934-136">內建函式</span><span class="sxs-lookup"><span data-stu-id="bb934-136">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="bb934-137">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="bb934-137">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




