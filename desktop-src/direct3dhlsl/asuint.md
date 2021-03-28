---
title: asuint 函式
description: 以兩個不帶正負號的32位整數向量64位值的位模式。
ms.assetid: 29671661-4fec-46e5-9b6f-56fba8e1d756
keywords:
- asuint 函式 HLSL
topic_type:
- apiref
api_name:
- asuint
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c54ed89e112482df4a54f35e24a04694e88fa490
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104022626"
---
# <a name="asuint-function"></a><span data-ttu-id="600b4-104">asuint 函式</span><span class="sxs-lookup"><span data-stu-id="600b4-104">asuint function</span></span>

<span data-ttu-id="600b4-105">以兩個不帶正負號的32位整數向量64位值的位模式。</span><span class="sxs-lookup"><span data-stu-id="600b4-105">Reinterprets the bit pattern of a 64-bit value as two unsigned 32-bit integers.</span></span>

## <a name="syntax"></a><span data-ttu-id="600b4-106">語法</span><span class="sxs-lookup"><span data-stu-id="600b4-106">Syntax</span></span>

``` syntax
void asuint(
  in  double value,
  out uint lowbits,
  out uint highbits
);
```

## <a name="parameters"></a><span data-ttu-id="600b4-107">參數</span><span class="sxs-lookup"><span data-stu-id="600b4-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="600b4-108">*值* \[在\]</span><span class="sxs-lookup"><span data-stu-id="600b4-108">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="600b4-109">類型： **double**</span><span class="sxs-lookup"><span data-stu-id="600b4-109">Type: **double**</span></span>

<span data-ttu-id="600b4-110">輸入值。</span><span class="sxs-lookup"><span data-stu-id="600b4-110">The input value.</span></span>

</dd> <dt>

<span data-ttu-id="600b4-111">*lowbits* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="600b4-111">*lowbits* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="600b4-112">類型： **uint**</span><span class="sxs-lookup"><span data-stu-id="600b4-112">Type: **uint**</span></span>

<span data-ttu-id="600b4-113">*值* 的低32位模式。</span><span class="sxs-lookup"><span data-stu-id="600b4-113">The low 32-bit pattern of *value*.</span></span>

</dd> <dt>

<span data-ttu-id="600b4-114">*highbits* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="600b4-114">*highbits* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="600b4-115">類型： **uint**</span><span class="sxs-lookup"><span data-stu-id="600b4-115">Type: **uint**</span></span>

<span data-ttu-id="600b4-116">*值* 的高32位模式。</span><span class="sxs-lookup"><span data-stu-id="600b4-116">The high 32-bit pattern of *value*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="600b4-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="600b4-117">Return value</span></span>

<span data-ttu-id="600b4-118">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="600b4-118">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="600b4-119">備註</span><span class="sxs-lookup"><span data-stu-id="600b4-119">Remarks</span></span>

<span data-ttu-id="600b4-120">此函式是 [**asuint**](dx-graphics-hlsl-asuint.md) 內建的替代版本，已在先前的著色器模型中提供，並已針對著色器模型5引進。</span><span class="sxs-lookup"><span data-stu-id="600b4-120">This function is an alternate version of the [**asuint**](dx-graphics-hlsl-asuint.md) intrinsic that has been available in earlier shader models, and was introduced for Shader Model 5.</span></span> <span data-ttu-id="600b4-121">原始函式 (由其不同簽章在 HLSL 編譯器中辨識) 仍可供著色器模型5使用。</span><span class="sxs-lookup"><span data-stu-id="600b4-121">The original function (recognized in the HLSL compiler by its different signature) remains available to Shader Model 5.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="600b4-122">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="600b4-122">Minimum Shader Model</span></span>

<span data-ttu-id="600b4-123">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="600b4-123">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="600b4-124">著色器模型</span><span class="sxs-lookup"><span data-stu-id="600b4-124">Shader Model</span></span>                                                                | <span data-ttu-id="600b4-125">支援</span><span class="sxs-lookup"><span data-stu-id="600b4-125">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="600b4-126">[著色器模型 5](d3d11-graphics-reference-sm5.md) 和更新版本的著色器模型</span><span class="sxs-lookup"><span data-stu-id="600b4-126">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="600b4-127">是</span><span class="sxs-lookup"><span data-stu-id="600b4-127">yes</span></span>       |



 

<span data-ttu-id="600b4-128">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="600b4-128">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="600b4-129">頂點</span><span class="sxs-lookup"><span data-stu-id="600b4-129">Vertex</span></span> | <span data-ttu-id="600b4-130">船體</span><span class="sxs-lookup"><span data-stu-id="600b4-130">Hull</span></span> | <span data-ttu-id="600b4-131">網域</span><span class="sxs-lookup"><span data-stu-id="600b4-131">Domain</span></span> | <span data-ttu-id="600b4-132">幾何</span><span class="sxs-lookup"><span data-stu-id="600b4-132">Geometry</span></span> | <span data-ttu-id="600b4-133">像素</span><span class="sxs-lookup"><span data-stu-id="600b4-133">Pixel</span></span> | <span data-ttu-id="600b4-134">計算</span><span class="sxs-lookup"><span data-stu-id="600b4-134">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="600b4-135">x</span><span class="sxs-lookup"><span data-stu-id="600b4-135">x</span></span>      | <span data-ttu-id="600b4-136">x</span><span class="sxs-lookup"><span data-stu-id="600b4-136">x</span></span>    | <span data-ttu-id="600b4-137">x</span><span class="sxs-lookup"><span data-stu-id="600b4-137">x</span></span>      | <span data-ttu-id="600b4-138">x</span><span class="sxs-lookup"><span data-stu-id="600b4-138">x</span></span>        | <span data-ttu-id="600b4-139">x</span><span class="sxs-lookup"><span data-stu-id="600b4-139">x</span></span>     | <span data-ttu-id="600b4-140">x</span><span class="sxs-lookup"><span data-stu-id="600b4-140">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="600b4-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="600b4-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="600b4-142">內建函式</span><span class="sxs-lookup"><span data-stu-id="600b4-142">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="600b4-143">**asuint (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="600b4-143">**asuint (DirectX HLSL)**</span></span>](dx-graphics-hlsl-asuint.md)
</dt> <dt>

[<span data-ttu-id="600b4-144">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="600b4-144">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




