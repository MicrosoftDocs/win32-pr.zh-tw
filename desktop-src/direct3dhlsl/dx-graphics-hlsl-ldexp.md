---
title: 'ldexp (Corecrt \_ math .h) '
description: 傳回將指定的值乘以二的結果，並將其提升為指定指數的乘冪。
ms.assetid: 6d6fee96-f952-4058-a1ac-3abb98dbd540
keywords:
- ldexp HLSL
topic_type:
- apiref
api_name:
- ldexp
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 731cb5cbf933ea3f8754a7d70b9ef0b7a54e783b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103854023"
---
# <a name="ldexp"></a><span data-ttu-id="9fe2b-104">ldexp</span><span class="sxs-lookup"><span data-stu-id="9fe2b-104">ldexp</span></span>

<span data-ttu-id="9fe2b-105">傳回將指定的值乘以二的結果，並將其提升為指定指數的乘冪。</span><span class="sxs-lookup"><span data-stu-id="9fe2b-105">Returns the result of multiplying the specified value by two, raised to the power of the specified exponent.</span></span>



| <span data-ttu-id="9fe2b-106">*ret* ldexp (*x*， *exp*) </span><span class="sxs-lookup"><span data-stu-id="9fe2b-106">*ret* ldexp(*x*, *exp*)</span></span> |
|-------------------------|



 

<span data-ttu-id="9fe2b-107">此函數使用下列公式： *x* \* 2 <sup>exp</sup></span><span class="sxs-lookup"><span data-stu-id="9fe2b-107">This function uses the following formula: *x* \* 2<sup>exp</sup></span></span>

## <a name="parameters"></a><span data-ttu-id="9fe2b-108">參數</span><span class="sxs-lookup"><span data-stu-id="9fe2b-108">Parameters</span></span>



| <span data-ttu-id="9fe2b-109">項目</span><span class="sxs-lookup"><span data-stu-id="9fe2b-109">Item</span></span>                                                         | <span data-ttu-id="9fe2b-110">描述</span><span class="sxs-lookup"><span data-stu-id="9fe2b-110">Description</span></span>                               |
|--------------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="9fe2b-111"><span id="x"></span><span id="X"></span>*X*</span><span class="sxs-lookup"><span data-stu-id="9fe2b-111"><span id="x"></span><span id="X"></span>*x*</span></span><br/>       | <span data-ttu-id="9fe2b-112">\[在 \] 指定的值中。</span><span class="sxs-lookup"><span data-stu-id="9fe2b-112">\[in\] The specified value.</span></span><br/>    |
| <span data-ttu-id="9fe2b-113"><span id="exp"></span><span id="EXP"></span>*exp*</span><span class="sxs-lookup"><span data-stu-id="9fe2b-113"><span id="exp"></span><span id="EXP"></span>*exp*</span></span><br/> | <span data-ttu-id="9fe2b-114">\[在 \] 指定的指數中。</span><span class="sxs-lookup"><span data-stu-id="9fe2b-114">\[in\] The specified exponent.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="9fe2b-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="9fe2b-115">Return Value</span></span>

<span data-ttu-id="9fe2b-116">將 *x* 參數乘以二的結果，並提升為 *exp* 參數的乘冪。</span><span class="sxs-lookup"><span data-stu-id="9fe2b-116">The result of multiplying the *x* parameter by two, raised to the power of the *exp* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="9fe2b-117">類型描述</span><span class="sxs-lookup"><span data-stu-id="9fe2b-117">Type Description</span></span>



| <span data-ttu-id="9fe2b-118">Name</span><span class="sxs-lookup"><span data-stu-id="9fe2b-118">Name</span></span>  | [<span data-ttu-id="9fe2b-119">**範本類型**</span><span class="sxs-lookup"><span data-stu-id="9fe2b-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="9fe2b-120">**元件類型**</span><span class="sxs-lookup"><span data-stu-id="9fe2b-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="9fe2b-121">大小</span><span class="sxs-lookup"><span data-stu-id="9fe2b-121">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="9fe2b-122">*x*</span><span class="sxs-lookup"><span data-stu-id="9fe2b-122">*x*</span></span>   | <span data-ttu-id="9fe2b-123">純 [**量、**](dx-graphics-hlsl-intrinsic-functions.md)**向量** 或 **矩陣**</span><span class="sxs-lookup"><span data-stu-id="9fe2b-123">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="9fe2b-124">**浮動**</span><span class="sxs-lookup"><span data-stu-id="9fe2b-124">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="9fe2b-125">任意</span><span class="sxs-lookup"><span data-stu-id="9fe2b-125">any</span></span>                            |
| <span data-ttu-id="9fe2b-126">*exp*</span><span class="sxs-lookup"><span data-stu-id="9fe2b-126">*exp*</span></span> | <span data-ttu-id="9fe2b-127">與輸入 *x* 相同</span><span class="sxs-lookup"><span data-stu-id="9fe2b-127">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="9fe2b-128">**浮動**</span><span class="sxs-lookup"><span data-stu-id="9fe2b-128">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="9fe2b-129">) 為輸入 *x* 的相同維度 (s</span><span class="sxs-lookup"><span data-stu-id="9fe2b-129">same dimension(s) as input *x*</span></span> |
| <span data-ttu-id="9fe2b-130">*Ret*</span><span class="sxs-lookup"><span data-stu-id="9fe2b-130">*ret*</span></span> | <span data-ttu-id="9fe2b-131">與輸入 *x* 相同</span><span class="sxs-lookup"><span data-stu-id="9fe2b-131">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="9fe2b-132">**浮動**</span><span class="sxs-lookup"><span data-stu-id="9fe2b-132">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="9fe2b-133">) 為輸入 *x* 的相同維度 (s</span><span class="sxs-lookup"><span data-stu-id="9fe2b-133">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="9fe2b-134">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="9fe2b-134">Minimum Shader Model</span></span>

<span data-ttu-id="9fe2b-135">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="9fe2b-135">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="9fe2b-136">著色器模型</span><span class="sxs-lookup"><span data-stu-id="9fe2b-136">Shader Model</span></span>                                                                       | <span data-ttu-id="9fe2b-137">支援</span><span class="sxs-lookup"><span data-stu-id="9fe2b-137">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="9fe2b-138">[著色器模型 2 (DIRECTX HLSL) ](dx-graphics-hlsl-sm2.md) 和更高的著色器模型</span><span class="sxs-lookup"><span data-stu-id="9fe2b-138">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="9fe2b-139">是</span><span class="sxs-lookup"><span data-stu-id="9fe2b-139">yes</span></span>                 |
| [<span data-ttu-id="9fe2b-140">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="9fe2b-140">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="9fe2b-141">是 (\_ \_ 只有) 的 vs 1</span><span class="sxs-lookup"><span data-stu-id="9fe2b-141">yes (vs\_1\_1 only)</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="9fe2b-142">規格需求</span><span class="sxs-lookup"><span data-stu-id="9fe2b-142">Requirements</span></span>



| <span data-ttu-id="9fe2b-143">需求</span><span class="sxs-lookup"><span data-stu-id="9fe2b-143">Requirement</span></span> | <span data-ttu-id="9fe2b-144">值</span><span class="sxs-lookup"><span data-stu-id="9fe2b-144">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="9fe2b-145">標頭</span><span class="sxs-lookup"><span data-stu-id="9fe2b-145">Header</span></span><br/> | <dl> <span data-ttu-id="9fe2b-146"><dt>Corecrt \_ math。h</dt></span><span class="sxs-lookup"><span data-stu-id="9fe2b-146"><dt>Corecrt\_math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9fe2b-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9fe2b-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9fe2b-148">**(DirectX HLSL) 內建函式**</span><span class="sxs-lookup"><span data-stu-id="9fe2b-148">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

