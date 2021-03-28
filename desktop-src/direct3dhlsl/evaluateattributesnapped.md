---
title: EvaluateAttributeSnapped 函式
description: 以位移的圖元距心進行評估。
ms.assetid: f5085016-0e94-49bb-96b6-42fa15c30b9f
keywords:
- EvaluateAttributeSnapped 函式 HLSL
topic_type:
- apiref
api_name:
- EvaluateAttributeSnapped
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 70a9389ed9e9f4fff16f82610cb611bc4da2c7a3
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104990671"
---
# <a name="evaluateattributesnapped-function"></a><span data-ttu-id="715ab-104">EvaluateAttributeSnapped 函式</span><span class="sxs-lookup"><span data-stu-id="715ab-104">EvaluateAttributeSnapped function</span></span>

<span data-ttu-id="715ab-105">以位移的圖元距心進行評估。</span><span class="sxs-lookup"><span data-stu-id="715ab-105">Evaluates at the pixel centroid with an offset.</span></span>

## <a name="syntax"></a><span data-ttu-id="715ab-106">語法</span><span class="sxs-lookup"><span data-stu-id="715ab-106">Syntax</span></span>

``` syntax
numeric EvaluateAttributeSnapped(
  in attrib numeric value,
  in 
            int2 offset
);
```

## <a name="parameters"></a><span data-ttu-id="715ab-107">參數</span><span class="sxs-lookup"><span data-stu-id="715ab-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="715ab-108">*值* \[在\]</span><span class="sxs-lookup"><span data-stu-id="715ab-108">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="715ab-109">類型： **attrib 數值**</span><span class="sxs-lookup"><span data-stu-id="715ab-109">Type: **attrib numeric**</span></span>

<span data-ttu-id="715ab-110">輸入值。</span><span class="sxs-lookup"><span data-stu-id="715ab-110">The input value.</span></span>

</dd> <dt>

<span data-ttu-id="715ab-111">*位移* \[在\]</span><span class="sxs-lookup"><span data-stu-id="715ab-111">*offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="715ab-112">類型： **int2**</span><span class="sxs-lookup"><span data-stu-id="715ab-112">Type: **int2**</span></span>

<span data-ttu-id="715ab-113">使用16x16 方格的圖元中心2D 位移。</span><span class="sxs-lookup"><span data-stu-id="715ab-113">A 2D offset from the pixel center using a 16x16 grid.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="715ab-114">備註</span><span class="sxs-lookup"><span data-stu-id="715ab-114">Remarks</span></span>

<span data-ttu-id="715ab-115">*Offset* 參數的範圍必須由下列位元組碼定義。</span><span class="sxs-lookup"><span data-stu-id="715ab-115">The range for the *offset* parameter must be defined by the following byte code.</span></span>

<span data-ttu-id="715ab-116">系統只會使用前兩個元件中最少的4個位 (U，V) 的圖元位移。</span><span class="sxs-lookup"><span data-stu-id="715ab-116">Only the least significant 4 bits of the first two components (U, V) of the pixel offset are used.</span></span> <span data-ttu-id="715ab-117">從4位固定點到 float 的轉換如下 (MSB .。。LSB) ，其中 MSB 是分數的一部分，並決定正負號：</span><span class="sxs-lookup"><span data-stu-id="715ab-117">The conversion from the 4-bit fixed point to float is as follows (MSB...LSB), where the MSB is both a part of the fraction and determines the sign:</span></span>

-   <span data-ttu-id="715ab-118">1000 =-0.5 f (-8/16) </span><span class="sxs-lookup"><span data-stu-id="715ab-118">1000 = -0.5f (-8 / 16)</span></span>
-   <span data-ttu-id="715ab-119">1001 =-0.4375 f (-7/16) </span><span class="sxs-lookup"><span data-stu-id="715ab-119">1001 = -0.4375f (-7 / 16)</span></span>
-   <span data-ttu-id="715ab-120">1010 =-0.375 f (-6/16) </span><span class="sxs-lookup"><span data-stu-id="715ab-120">1010 = -0.375f (-6 / 16)</span></span>
-   <span data-ttu-id="715ab-121">1011 =-0.3125 f (-5/16) </span><span class="sxs-lookup"><span data-stu-id="715ab-121">1011 = -0.3125f (-5 / 16)</span></span>
-   <span data-ttu-id="715ab-122">1100 =-0.25 f (-4/16) </span><span class="sxs-lookup"><span data-stu-id="715ab-122">1100 = -0.25f (-4 / 16)</span></span>
-   <span data-ttu-id="715ab-123">1101 =-0.1875 f (-3/16) </span><span class="sxs-lookup"><span data-stu-id="715ab-123">1101 = -0.1875f (-3 / 16)</span></span>
-   <span data-ttu-id="715ab-124">1110 =-0.125 f (-2/16) </span><span class="sxs-lookup"><span data-stu-id="715ab-124">1110 = -0.125f (-2 / 16)</span></span>
-   <span data-ttu-id="715ab-125">1111 =-0.0625 f (-1/16) </span><span class="sxs-lookup"><span data-stu-id="715ab-125">1111 = -0.0625f (-1 / 16)</span></span>
-   <span data-ttu-id="715ab-126">0000 = 0.0 f ( 0/16) </span><span class="sxs-lookup"><span data-stu-id="715ab-126">0000 = 0.0f ( 0 / 16)</span></span>
-   <span data-ttu-id="715ab-127">0001 = 0.0625 f ( 1/16) </span><span class="sxs-lookup"><span data-stu-id="715ab-127">0001 = 0.0625f ( 1 / 16)</span></span>
-   <span data-ttu-id="715ab-128">0010 = 0.125 f ( 2/16) </span><span class="sxs-lookup"><span data-stu-id="715ab-128">0010 = 0.125f ( 2 / 16)</span></span>
-   <span data-ttu-id="715ab-129">0011 = 0.1875 f ( 3/16) </span><span class="sxs-lookup"><span data-stu-id="715ab-129">0011 = 0.1875f ( 3 / 16)</span></span>
-   <span data-ttu-id="715ab-130">0100 = 0.25 f ( 4/16) </span><span class="sxs-lookup"><span data-stu-id="715ab-130">0100 = 0.25f ( 4 / 16)</span></span>
-   <span data-ttu-id="715ab-131">0101 = 0.3125 f ( 5/16) </span><span class="sxs-lookup"><span data-stu-id="715ab-131">0101 = 0.3125f ( 5 / 16)</span></span>
-   <span data-ttu-id="715ab-132">0110 = 0.375 f ( 6/16) </span><span class="sxs-lookup"><span data-stu-id="715ab-132">0110 = 0.375f ( 6 / 16)</span></span>
-   <span data-ttu-id="715ab-133">0111 = 0.4375 f ( 7/16) </span><span class="sxs-lookup"><span data-stu-id="715ab-133">0111 = 0.4375f ( 7 / 16)</span></span>

> [!Note]  
> <span data-ttu-id="715ab-134">圖元的左邊和上邊緣包含在位移中;但是，不包含底部和右邊的邊緣。</span><span class="sxs-lookup"><span data-stu-id="715ab-134">The left and top edges of a pixel are included in the offset; however, the bottom and right edges are not included.</span></span> <span data-ttu-id="715ab-135">32位整數中的所有其他位都會被忽略。</span><span class="sxs-lookup"><span data-stu-id="715ab-135">All other bits in the 32-bit integer U and V offset values are ignored.</span></span>

 

<span data-ttu-id="715ab-136">實值可以採用著色器所提供的位移，並透過執行下列計算，取得完整的32位固定點值 (28.4) （橫跨有效範圍）：</span><span class="sxs-lookup"><span data-stu-id="715ab-136">An implementation can take the offset provided by the shader and obtain a full 32-bit fixed point value (28.4), which spans the valid range, by performing the following calculation:</span></span>


```
iU = (iU<<28)>>28  // keep lowest 4 bits and sign extend, which yields [-8..7]
```



<span data-ttu-id="715ab-137">如果實作為必須將位移對應至浮點數位移，則會執行下列計算：</span><span class="sxs-lookup"><span data-stu-id="715ab-137">If an implementation must map the offset to a floating-point offset, it performs the following calculation:</span></span>


```
fU = ((float)iU)/16
```



### <a name="minimum-shader-model"></a><span data-ttu-id="715ab-138">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="715ab-138">Minimum Shader Model</span></span>

<span data-ttu-id="715ab-139">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="715ab-139">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="715ab-140">著色器模型</span><span class="sxs-lookup"><span data-stu-id="715ab-140">Shader Model</span></span>                                                                | <span data-ttu-id="715ab-141">支援</span><span class="sxs-lookup"><span data-stu-id="715ab-141">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="715ab-142">[著色器模型 5](d3d11-graphics-reference-sm5.md) 和更新版本的著色器模型</span><span class="sxs-lookup"><span data-stu-id="715ab-142">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="715ab-143">是</span><span class="sxs-lookup"><span data-stu-id="715ab-143">yes</span></span>       |



 

<span data-ttu-id="715ab-144">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="715ab-144">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="715ab-145">頂點</span><span class="sxs-lookup"><span data-stu-id="715ab-145">Vertex</span></span> | <span data-ttu-id="715ab-146">船體</span><span class="sxs-lookup"><span data-stu-id="715ab-146">Hull</span></span> | <span data-ttu-id="715ab-147">網域</span><span class="sxs-lookup"><span data-stu-id="715ab-147">Domain</span></span> | <span data-ttu-id="715ab-148">幾何</span><span class="sxs-lookup"><span data-stu-id="715ab-148">Geometry</span></span> | <span data-ttu-id="715ab-149">像素</span><span class="sxs-lookup"><span data-stu-id="715ab-149">Pixel</span></span> | <span data-ttu-id="715ab-150">計算</span><span class="sxs-lookup"><span data-stu-id="715ab-150">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="715ab-151">x</span><span class="sxs-lookup"><span data-stu-id="715ab-151">x</span></span>     |         |



 

## <a name="see-also"></a><span data-ttu-id="715ab-152">另請參閱</span><span class="sxs-lookup"><span data-stu-id="715ab-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="715ab-153">內建函式</span><span class="sxs-lookup"><span data-stu-id="715ab-153">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="715ab-154">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="715ab-154">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




