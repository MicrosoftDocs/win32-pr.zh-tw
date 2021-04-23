---
title: countbits 函式
description: 計算輸入整數中的每個元件) 設定 (位數。
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
ms.openlocfilehash: 357aceca6e2aea261a9e94212b58ff6308c99560
ms.sourcegitcommit: 435ea8f5bf06808ffa7dce39afb0ee6de842ba2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/23/2021
ms.locfileid: "107925621"
---
# <a name="countbits-function"></a><span data-ttu-id="a1379-104">countbits 函式</span><span class="sxs-lookup"><span data-stu-id="a1379-104">countbits function</span></span>

<span data-ttu-id="a1379-105">計算輸入整數中的每個元件) 設定 (位數。</span><span class="sxs-lookup"><span data-stu-id="a1379-105">Counts the number of bits (per component) set in the input integer.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1379-106">語法</span><span class="sxs-lookup"><span data-stu-id="a1379-106">Syntax</span></span>

``` syntax
uint countbits(
  in uint value
);
```

## <a name="parameters"></a><span data-ttu-id="a1379-107">參數</span><span class="sxs-lookup"><span data-stu-id="a1379-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1379-108">*值* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a1379-108">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1379-109">類型： **uint**</span><span class="sxs-lookup"><span data-stu-id="a1379-109">Type: **uint**</span></span>

<span data-ttu-id="a1379-110">輸入值。</span><span class="sxs-lookup"><span data-stu-id="a1379-110">The input value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1379-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="a1379-111">Return value</span></span>

<span data-ttu-id="a1379-112">類型： **uint**</span><span class="sxs-lookup"><span data-stu-id="a1379-112">Type: **uint**</span></span>

<span data-ttu-id="a1379-113">位數。</span><span class="sxs-lookup"><span data-stu-id="a1379-113">The number of bits.</span></span>

## <a name="remarks"></a><span data-ttu-id="a1379-114">備註</span><span class="sxs-lookup"><span data-stu-id="a1379-114">Remarks</span></span>

<span data-ttu-id="a1379-115">您也可以使用下列多載版本：</span><span class="sxs-lookup"><span data-stu-id="a1379-115">The following overloaded versions are also available:</span></span>

``` syntax
uint count_bits(uint value);
uint2 count_bits(uint2 value);
uint3 count_bits(uint3 value);
uint4 count_bits(uint4 value);
```

### <a name="minimum-shader-model"></a><span data-ttu-id="a1379-116">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="a1379-116">Minimum Shader Model</span></span>

<span data-ttu-id="a1379-117">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="a1379-117">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="a1379-118">著色器模型</span><span class="sxs-lookup"><span data-stu-id="a1379-118">Shader Model</span></span>                                                                | <span data-ttu-id="a1379-119">支援</span><span class="sxs-lookup"><span data-stu-id="a1379-119">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="a1379-120">[著色器模型 5](d3d11-graphics-reference-sm5.md) 和更新版本的著色器模型</span><span class="sxs-lookup"><span data-stu-id="a1379-120">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="a1379-121">是</span><span class="sxs-lookup"><span data-stu-id="a1379-121">yes</span></span>       |



 

<span data-ttu-id="a1379-122">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="a1379-122">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="a1379-123">頂點</span><span class="sxs-lookup"><span data-stu-id="a1379-123">Vertex</span></span> | <span data-ttu-id="a1379-124">船體</span><span class="sxs-lookup"><span data-stu-id="a1379-124">Hull</span></span> | <span data-ttu-id="a1379-125">網域</span><span class="sxs-lookup"><span data-stu-id="a1379-125">Domain</span></span> | <span data-ttu-id="a1379-126">幾何</span><span class="sxs-lookup"><span data-stu-id="a1379-126">Geometry</span></span> | <span data-ttu-id="a1379-127">像素</span><span class="sxs-lookup"><span data-stu-id="a1379-127">Pixel</span></span> | <span data-ttu-id="a1379-128">計算</span><span class="sxs-lookup"><span data-stu-id="a1379-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="a1379-129">x</span><span class="sxs-lookup"><span data-stu-id="a1379-129">x</span></span>      | <span data-ttu-id="a1379-130">x</span><span class="sxs-lookup"><span data-stu-id="a1379-130">x</span></span>    | <span data-ttu-id="a1379-131">x</span><span class="sxs-lookup"><span data-stu-id="a1379-131">x</span></span>      | <span data-ttu-id="a1379-132">x</span><span class="sxs-lookup"><span data-stu-id="a1379-132">x</span></span>        | <span data-ttu-id="a1379-133">x</span><span class="sxs-lookup"><span data-stu-id="a1379-133">x</span></span>     | <span data-ttu-id="a1379-134">x</span><span class="sxs-lookup"><span data-stu-id="a1379-134">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="a1379-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a1379-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1379-136">內建函式</span><span class="sxs-lookup"><span data-stu-id="a1379-136">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="a1379-137">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="a1379-137">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




