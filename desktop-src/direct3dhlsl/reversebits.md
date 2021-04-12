---
title: reversebits 函式
description: 反轉每個元件的位順序。
ms.assetid: dad46e25-9980-4645-98eb-d834db704fc8
keywords:
- reversebits 函式 HLSL
topic_type:
- apiref
api_name:
- reversebits
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d98b824883ddc4f06e6c11d30c2759bb0fc2be26
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104462565"
---
# <a name="reversebits-function"></a><span data-ttu-id="ecbbd-104">reversebits 函式</span><span class="sxs-lookup"><span data-stu-id="ecbbd-104">reversebits function</span></span>

<span data-ttu-id="ecbbd-105">反轉每個元件的位順序。</span><span class="sxs-lookup"><span data-stu-id="ecbbd-105">Reverses the order of the bits, per component.</span></span>

## <a name="syntax"></a><span data-ttu-id="ecbbd-106">語法</span><span class="sxs-lookup"><span data-stu-id="ecbbd-106">Syntax</span></span>

``` syntax
uint reversebits(
  in uint value
);
```

## <a name="parameters"></a><span data-ttu-id="ecbbd-107">參數</span><span class="sxs-lookup"><span data-stu-id="ecbbd-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ecbbd-108">*值* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ecbbd-108">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ecbbd-109">類型： **uint**</span><span class="sxs-lookup"><span data-stu-id="ecbbd-109">Type: **uint**</span></span>

<span data-ttu-id="ecbbd-110">輸入值。</span><span class="sxs-lookup"><span data-stu-id="ecbbd-110">The input value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ecbbd-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="ecbbd-111">Return value</span></span>

<span data-ttu-id="ecbbd-112">類型： **uint**</span><span class="sxs-lookup"><span data-stu-id="ecbbd-112">Type: **uint**</span></span>

<span data-ttu-id="ecbbd-113">輸入值，其位順序反轉。</span><span class="sxs-lookup"><span data-stu-id="ecbbd-113">The input value, with the bit order reversed.</span></span>

## <a name="remarks"></a><span data-ttu-id="ecbbd-114">備註</span><span class="sxs-lookup"><span data-stu-id="ecbbd-114">Remarks</span></span>

<span data-ttu-id="ecbbd-115">您也可以使用下列多載版本：</span><span class="sxs-lookup"><span data-stu-id="ecbbd-115">The following overloaded versions are also available:</span></span>

``` syntax
uint2 reversebits(uint2 value);
uint3 reversebits(uint3 value);
uint4 reversebits(uint4 value);
```

### <a name="minimum-shader-model"></a><span data-ttu-id="ecbbd-116">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="ecbbd-116">Minimum Shader Model</span></span>

<span data-ttu-id="ecbbd-117">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="ecbbd-117">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="ecbbd-118">著色器模型</span><span class="sxs-lookup"><span data-stu-id="ecbbd-118">Shader Model</span></span>                                                                | <span data-ttu-id="ecbbd-119">支援</span><span class="sxs-lookup"><span data-stu-id="ecbbd-119">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="ecbbd-120">[著色器模型 5](d3d11-graphics-reference-sm5.md) 和更新版本的著色器模型</span><span class="sxs-lookup"><span data-stu-id="ecbbd-120">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="ecbbd-121">是</span><span class="sxs-lookup"><span data-stu-id="ecbbd-121">yes</span></span>       |



 

<span data-ttu-id="ecbbd-122">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="ecbbd-122">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="ecbbd-123">頂點</span><span class="sxs-lookup"><span data-stu-id="ecbbd-123">Vertex</span></span> | <span data-ttu-id="ecbbd-124">船體</span><span class="sxs-lookup"><span data-stu-id="ecbbd-124">Hull</span></span> | <span data-ttu-id="ecbbd-125">網域</span><span class="sxs-lookup"><span data-stu-id="ecbbd-125">Domain</span></span> | <span data-ttu-id="ecbbd-126">幾何</span><span class="sxs-lookup"><span data-stu-id="ecbbd-126">Geometry</span></span> | <span data-ttu-id="ecbbd-127">像素</span><span class="sxs-lookup"><span data-stu-id="ecbbd-127">Pixel</span></span> | <span data-ttu-id="ecbbd-128">計算</span><span class="sxs-lookup"><span data-stu-id="ecbbd-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="ecbbd-129">x</span><span class="sxs-lookup"><span data-stu-id="ecbbd-129">x</span></span>      | <span data-ttu-id="ecbbd-130">x</span><span class="sxs-lookup"><span data-stu-id="ecbbd-130">x</span></span>    | <span data-ttu-id="ecbbd-131">x</span><span class="sxs-lookup"><span data-stu-id="ecbbd-131">x</span></span>      | <span data-ttu-id="ecbbd-132">x</span><span class="sxs-lookup"><span data-stu-id="ecbbd-132">x</span></span>        | <span data-ttu-id="ecbbd-133">x</span><span class="sxs-lookup"><span data-stu-id="ecbbd-133">x</span></span>     | <span data-ttu-id="ecbbd-134">x</span><span class="sxs-lookup"><span data-stu-id="ecbbd-134">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="ecbbd-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ecbbd-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ecbbd-136">內建函式</span><span class="sxs-lookup"><span data-stu-id="ecbbd-136">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="ecbbd-137">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="ecbbd-137">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




