---
title: asdouble 函式
description: 向量轉換值 (2 32 位值) 成為雙精度浮點數。
ms.assetid: 55e5276d-81e1-4e7e-8cb4-0beb57d2fb7f
keywords:
- asdouble 函式 HLSL
topic_type:
- apiref
api_name:
- asdouble
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: caa2c83ee01739a2e2ee9595d0a26e1bdb80fef1
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104022627"
---
# <a name="asdouble-function"></a><span data-ttu-id="9946e-104">asdouble 函式</span><span class="sxs-lookup"><span data-stu-id="9946e-104">asdouble function</span></span>

<span data-ttu-id="9946e-105">向量轉換值 (2 32 位值) 成為雙精度浮點數。</span><span class="sxs-lookup"><span data-stu-id="9946e-105">Reinterprets a cast value (two 32-bit values) into a double.</span></span>

## <a name="syntax"></a><span data-ttu-id="9946e-106">語法</span><span class="sxs-lookup"><span data-stu-id="9946e-106">Syntax</span></span>

``` syntax
double asdouble(
  in uint lowbits,
  in uint highbits
);
```

## <a name="parameters"></a><span data-ttu-id="9946e-107">參數</span><span class="sxs-lookup"><span data-stu-id="9946e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9946e-108">*lowbits* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9946e-108">*lowbits* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9946e-109">類型： **uint**</span><span class="sxs-lookup"><span data-stu-id="9946e-109">Type: **uint**</span></span>

<span data-ttu-id="9946e-110">輸入值的低32位模式。</span><span class="sxs-lookup"><span data-stu-id="9946e-110">The low 32-bit pattern of the input value.</span></span>

</dd> <dt>

<span data-ttu-id="9946e-111">*highbits* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9946e-111">*highbits* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9946e-112">類型： **uint**</span><span class="sxs-lookup"><span data-stu-id="9946e-112">Type: **uint**</span></span>

<span data-ttu-id="9946e-113">輸入值的高32位模式。</span><span class="sxs-lookup"><span data-stu-id="9946e-113">The high 32-bit pattern of the input value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9946e-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="9946e-114">Return value</span></span>

<span data-ttu-id="9946e-115">類型： **double**</span><span class="sxs-lookup"><span data-stu-id="9946e-115">Type: **double**</span></span>

<span data-ttu-id="9946e-116">輸入 (2 32 位值) 重新轉換為雙精度浮點數。</span><span class="sxs-lookup"><span data-stu-id="9946e-116">The input (two 32-bit values) recast as a double.</span></span>

## <a name="remarks"></a><span data-ttu-id="9946e-117">備註</span><span class="sxs-lookup"><span data-stu-id="9946e-117">Remarks</span></span>

<span data-ttu-id="9946e-118">您也可以使用下列多載版本：</span><span class="sxs-lookup"><span data-stu-id="9946e-118">The following overloaded version is also available:</span></span>

``` syntax
double2 asdouble(uint2 lowbits, uint2 highbits);
```

<span data-ttu-id="9946e-119">如果輸入值為 2 32 位元件，則傳回類型將會包含一個雙精度浮點數。</span><span class="sxs-lookup"><span data-stu-id="9946e-119">If the input value is two 32-bit components, the return type will contain one double.</span></span> <span data-ttu-id="9946e-120">如果輸入值為 4 32 位元件，則傳回類型將包含兩個雙精度浮點數。</span><span class="sxs-lookup"><span data-stu-id="9946e-120">If the input value is four 32-bit components, the return type will contain two doubles.</span></span> <span data-ttu-id="9946e-121">如果輸入值是64位型別，則傳回的值會與輸入值具有相同數目的元件。</span><span class="sxs-lookup"><span data-stu-id="9946e-121">If the input value is a 64-bit type, the returned value will have the same number of components as the input value.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="9946e-122">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="9946e-122">Minimum Shader Model</span></span>

<span data-ttu-id="9946e-123">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="9946e-123">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="9946e-124">著色器模型</span><span class="sxs-lookup"><span data-stu-id="9946e-124">Shader Model</span></span>                                                                | <span data-ttu-id="9946e-125">支援</span><span class="sxs-lookup"><span data-stu-id="9946e-125">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="9946e-126">[著色器模型 5](d3d11-graphics-reference-sm5.md) 和更新版本的著色器模型</span><span class="sxs-lookup"><span data-stu-id="9946e-126">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="9946e-127">是</span><span class="sxs-lookup"><span data-stu-id="9946e-127">yes</span></span>       |



 

<span data-ttu-id="9946e-128">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="9946e-128">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="9946e-129">頂點</span><span class="sxs-lookup"><span data-stu-id="9946e-129">Vertex</span></span> | <span data-ttu-id="9946e-130">船體</span><span class="sxs-lookup"><span data-stu-id="9946e-130">Hull</span></span> | <span data-ttu-id="9946e-131">網域</span><span class="sxs-lookup"><span data-stu-id="9946e-131">Domain</span></span> | <span data-ttu-id="9946e-132">幾何</span><span class="sxs-lookup"><span data-stu-id="9946e-132">Geometry</span></span> | <span data-ttu-id="9946e-133">像素</span><span class="sxs-lookup"><span data-stu-id="9946e-133">Pixel</span></span> | <span data-ttu-id="9946e-134">計算</span><span class="sxs-lookup"><span data-stu-id="9946e-134">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="9946e-135">x</span><span class="sxs-lookup"><span data-stu-id="9946e-135">x</span></span>      | <span data-ttu-id="9946e-136">x</span><span class="sxs-lookup"><span data-stu-id="9946e-136">x</span></span>    | <span data-ttu-id="9946e-137">x</span><span class="sxs-lookup"><span data-stu-id="9946e-137">x</span></span>      | <span data-ttu-id="9946e-138">x</span><span class="sxs-lookup"><span data-stu-id="9946e-138">x</span></span>        | <span data-ttu-id="9946e-139">x</span><span class="sxs-lookup"><span data-stu-id="9946e-139">x</span></span>     | <span data-ttu-id="9946e-140">x</span><span class="sxs-lookup"><span data-stu-id="9946e-140">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="9946e-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9946e-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9946e-142">內建函式</span><span class="sxs-lookup"><span data-stu-id="9946e-142">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="9946e-143">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="9946e-143">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




