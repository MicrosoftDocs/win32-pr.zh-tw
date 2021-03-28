---
title: distance
description: 傳回兩個向量之間的距離純量。
ms.assetid: dda8dc39-fd72-4e92-bf9d-e700db0ede9e
keywords:
- 距離 HLSL
topic_type:
- apiref
api_name:
- distance
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c0f3a64778666ac8f7de16b91eed202e36e90ed1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315586"
---
# <a name="distance"></a><span data-ttu-id="fd30c-104">distance</span><span class="sxs-lookup"><span data-stu-id="fd30c-104">distance</span></span>

<span data-ttu-id="fd30c-105">傳回兩個向量之間的距離純量。</span><span class="sxs-lookup"><span data-stu-id="fd30c-105">Returns a distance scalar between two vectors.</span></span>



| <span data-ttu-id="fd30c-106">*ret* 距離 (*x*， *y*) </span><span class="sxs-lookup"><span data-stu-id="fd30c-106">*ret* distance(*x*, *y*)</span></span> |
|--------------------------|



 

## <a name="parameters"></a><span data-ttu-id="fd30c-107">參數</span><span class="sxs-lookup"><span data-stu-id="fd30c-107">Parameters</span></span>



| <span data-ttu-id="fd30c-108">項目</span><span class="sxs-lookup"><span data-stu-id="fd30c-108">Item</span></span>                                                   | <span data-ttu-id="fd30c-109">描述</span><span class="sxs-lookup"><span data-stu-id="fd30c-109">Description</span></span>                                                    |
|--------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="fd30c-110"><span id="x"></span><span id="X"></span>*X*</span><span class="sxs-lookup"><span data-stu-id="fd30c-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="fd30c-111">\[在 \] 要比較的第一個浮點向量中。</span><span class="sxs-lookup"><span data-stu-id="fd30c-111">\[in\] The first floating-point vector to compare.</span></span><br/>  |
| <span data-ttu-id="fd30c-112"><span id="y"></span><span id="Y"></span>*Y*</span><span class="sxs-lookup"><span data-stu-id="fd30c-112"><span id="y"></span><span id="Y"></span>*y*</span></span><br/> | <span data-ttu-id="fd30c-113">\[在 \] 要比較的第二個浮點數向量中。</span><span class="sxs-lookup"><span data-stu-id="fd30c-113">\[in\] The second floating-point vector to compare.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="fd30c-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="fd30c-114">Return Value</span></span>

<span data-ttu-id="fd30c-115">浮點純量值，表示 *x* 參數與 *y* 參數之間的距離。</span><span class="sxs-lookup"><span data-stu-id="fd30c-115">A floating-point, scalar value that represents the distance between the *x* parameter and the *y* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="fd30c-116">類型描述</span><span class="sxs-lookup"><span data-stu-id="fd30c-116">Type Description</span></span>



| <span data-ttu-id="fd30c-117">Name</span><span class="sxs-lookup"><span data-stu-id="fd30c-117">Name</span></span>  | [<span data-ttu-id="fd30c-118">**範本類型**</span><span class="sxs-lookup"><span data-stu-id="fd30c-118">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="fd30c-119">**元件類型**</span><span class="sxs-lookup"><span data-stu-id="fd30c-119">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="fd30c-120">大小</span><span class="sxs-lookup"><span data-stu-id="fd30c-120">Size</span></span>                           |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="fd30c-121">*x*</span><span class="sxs-lookup"><span data-stu-id="fd30c-121">*x*</span></span>   | [<span data-ttu-id="fd30c-122">**向量**</span><span class="sxs-lookup"><span data-stu-id="fd30c-122">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="fd30c-123">**浮動**</span><span class="sxs-lookup"><span data-stu-id="fd30c-123">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="fd30c-124">任意</span><span class="sxs-lookup"><span data-stu-id="fd30c-124">any</span></span>                            |
| <span data-ttu-id="fd30c-125">*y*</span><span class="sxs-lookup"><span data-stu-id="fd30c-125">*y*</span></span>   | [<span data-ttu-id="fd30c-126">**向量**</span><span class="sxs-lookup"><span data-stu-id="fd30c-126">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="fd30c-127">**浮動**</span><span class="sxs-lookup"><span data-stu-id="fd30c-127">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="fd30c-128">) 為輸入 *x* 的相同維度 (s</span><span class="sxs-lookup"><span data-stu-id="fd30c-128">same dimension(s) as input *x*</span></span> |
| <span data-ttu-id="fd30c-129">*Ret*</span><span class="sxs-lookup"><span data-stu-id="fd30c-129">*ret*</span></span> | [<span data-ttu-id="fd30c-130">**純量 (scalar)**</span><span class="sxs-lookup"><span data-stu-id="fd30c-130">**scalar**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="fd30c-131">**FLOAT**</span><span class="sxs-lookup"><span data-stu-id="fd30c-131">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="fd30c-132">1</span><span class="sxs-lookup"><span data-stu-id="fd30c-132">1</span></span>                              |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="fd30c-133">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="fd30c-133">Minimum Shader Model</span></span>

<span data-ttu-id="fd30c-134">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="fd30c-134">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="fd30c-135">著色器模型</span><span class="sxs-lookup"><span data-stu-id="fd30c-135">Shader Model</span></span>                                                                       | <span data-ttu-id="fd30c-136">支援</span><span class="sxs-lookup"><span data-stu-id="fd30c-136">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="fd30c-137">[著色器模型 2 (DIRECTX HLSL) ](dx-graphics-hlsl-sm2.md) 和更高的著色器模型</span><span class="sxs-lookup"><span data-stu-id="fd30c-137">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="fd30c-138">是</span><span class="sxs-lookup"><span data-stu-id="fd30c-138">yes</span></span>       |
| [<span data-ttu-id="fd30c-139">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="fd30c-139">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="fd30c-140">vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="fd30c-140">vs\_1\_1</span></span>  |



 

## <a name="see-also"></a><span data-ttu-id="fd30c-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fd30c-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd30c-142">**(DirectX HLSL) 內建函式**</span><span class="sxs-lookup"><span data-stu-id="fd30c-142">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

