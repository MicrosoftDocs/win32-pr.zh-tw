---
title: 'frexp (Corecrt \_ math .h) '
description: 傳回指定之浮點值的尾數和指數。
ms.assetid: 9252feff-da85-4b3e-97db-1fcddd786695
keywords:
- frexp HLSL
topic_type:
- apiref
api_name:
- frexp
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bddbcbbf9e97aff739bb06a0f0d0ddac12134463
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103946092"
---
# <a name="frexp"></a><span data-ttu-id="f612d-104">frexp</span><span class="sxs-lookup"><span data-stu-id="f612d-104">frexp</span></span>

<span data-ttu-id="f612d-105">傳回指定之浮點值的尾數和指數。</span><span class="sxs-lookup"><span data-stu-id="f612d-105">Returns the mantissa and exponent of the specified floating-point value.</span></span>



| <span data-ttu-id="f612d-106">*ret* frexp (*x*， *exp*) </span><span class="sxs-lookup"><span data-stu-id="f612d-106">*ret* frexp(*x*, *exp*)</span></span> |
|-------------------------|



 

<span data-ttu-id="f612d-107">傳回值是尾數，而 *exp* 參數所傳回的值是指數。</span><span class="sxs-lookup"><span data-stu-id="f612d-107">The return value is the mantissa, and the value returned by *exp* parameter is the exponent.</span></span>

## <a name="parameters"></a><span data-ttu-id="f612d-108">參數</span><span class="sxs-lookup"><span data-stu-id="f612d-108">Parameters</span></span>



| <span data-ttu-id="f612d-109">項目</span><span class="sxs-lookup"><span data-stu-id="f612d-109">Item</span></span>                                                         | <span data-ttu-id="f612d-110">描述</span><span class="sxs-lookup"><span data-stu-id="f612d-110">Description</span></span>                                                                                                                                      |
|--------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f612d-111"><span id="x"></span><span id="X"></span>*X*</span><span class="sxs-lookup"><span data-stu-id="f612d-111"><span id="x"></span><span id="X"></span>*x*</span></span><br/>       | <span data-ttu-id="f612d-112">\[在 \] 指定的浮點值中。</span><span class="sxs-lookup"><span data-stu-id="f612d-112">\[in\] The specified floating-point value.</span></span> <span data-ttu-id="f612d-113">如果 *x* 參數為0，則此函式會針對尾數和指數傳回0。</span><span class="sxs-lookup"><span data-stu-id="f612d-113">If the *x* parameter is 0, this function returns 0 for both the mantissa and the exponent.</span></span><br/> |
| <span data-ttu-id="f612d-114"><span id="exp"></span><span id="EXP"></span>*exp*</span><span class="sxs-lookup"><span data-stu-id="f612d-114"><span id="exp"></span><span id="EXP"></span>*exp*</span></span><br/> | <span data-ttu-id="f612d-115">\[輸出 \] *x* 參數的傳回指數。</span><span class="sxs-lookup"><span data-stu-id="f612d-115">\[out\] The returned exponent of the *x* parameter.</span></span><br/>                                                                                   |



 

## <a name="return-value"></a><span data-ttu-id="f612d-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="f612d-116">Return Value</span></span>

<span data-ttu-id="f612d-117">*X* 參數的尾數。</span><span class="sxs-lookup"><span data-stu-id="f612d-117">The mantissa of the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="f612d-118">類型描述</span><span class="sxs-lookup"><span data-stu-id="f612d-118">Type Description</span></span>



| <span data-ttu-id="f612d-119">Name</span><span class="sxs-lookup"><span data-stu-id="f612d-119">Name</span></span>  | [<span data-ttu-id="f612d-120">**範本類型**</span><span class="sxs-lookup"><span data-stu-id="f612d-120">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="f612d-121">**元件類型**</span><span class="sxs-lookup"><span data-stu-id="f612d-121">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="f612d-122">大小</span><span class="sxs-lookup"><span data-stu-id="f612d-122">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="f612d-123">*x*</span><span class="sxs-lookup"><span data-stu-id="f612d-123">*x*</span></span>   | <span data-ttu-id="f612d-124">純 [**量、**](dx-graphics-hlsl-intrinsic-functions.md)**向量** 或 **矩陣**</span><span class="sxs-lookup"><span data-stu-id="f612d-124">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="f612d-125">**浮動**</span><span class="sxs-lookup"><span data-stu-id="f612d-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="f612d-126">任意</span><span class="sxs-lookup"><span data-stu-id="f612d-126">any</span></span>                            |
| <span data-ttu-id="f612d-127">*exp*</span><span class="sxs-lookup"><span data-stu-id="f612d-127">*exp*</span></span> | <span data-ttu-id="f612d-128">與輸入 *x* 相同</span><span class="sxs-lookup"><span data-stu-id="f612d-128">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="f612d-129">**浮動**</span><span class="sxs-lookup"><span data-stu-id="f612d-129">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="f612d-130">) 為輸入 *x* 的相同維度 (s</span><span class="sxs-lookup"><span data-stu-id="f612d-130">same dimension(s) as input *x*</span></span> |
| <span data-ttu-id="f612d-131">*Ret*</span><span class="sxs-lookup"><span data-stu-id="f612d-131">*ret*</span></span> | <span data-ttu-id="f612d-132">與輸入 *x* 相同</span><span class="sxs-lookup"><span data-stu-id="f612d-132">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="f612d-133">**浮動**</span><span class="sxs-lookup"><span data-stu-id="f612d-133">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="f612d-134">) 為輸入 *x* 的相同維度 (s</span><span class="sxs-lookup"><span data-stu-id="f612d-134">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="f612d-135">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="f612d-135">Minimum Shader Model</span></span>

<span data-ttu-id="f612d-136">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="f612d-136">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="f612d-137">著色器模型</span><span class="sxs-lookup"><span data-stu-id="f612d-137">Shader Model</span></span>                                                                       | <span data-ttu-id="f612d-138">支援</span><span class="sxs-lookup"><span data-stu-id="f612d-138">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="f612d-139">[著色器模型 3 (DIRECTX HLSL) ](dx-graphics-hlsl-sm3.md) 和更高的著色器模型</span><span class="sxs-lookup"><span data-stu-id="f612d-139">[Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) and higher shader models</span></span> | <span data-ttu-id="f612d-140">是</span><span class="sxs-lookup"><span data-stu-id="f612d-140">yes</span></span>                 |
| [<span data-ttu-id="f612d-141">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="f612d-141">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md)                          | <span data-ttu-id="f612d-142">是 (ps \_ 2 \_ x 僅) </span><span class="sxs-lookup"><span data-stu-id="f612d-142">yes (ps\_2\_x only)</span></span> |
| [<span data-ttu-id="f612d-143">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="f612d-143">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="f612d-144">不可以</span><span class="sxs-lookup"><span data-stu-id="f612d-144">no</span></span>                  |



 

## <a name="remarks"></a><span data-ttu-id="f612d-145">備註</span><span class="sxs-lookup"><span data-stu-id="f612d-145">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="f612d-146">需求</span><span class="sxs-lookup"><span data-stu-id="f612d-146">Requirements</span></span>



| <span data-ttu-id="f612d-147">需求</span><span class="sxs-lookup"><span data-stu-id="f612d-147">Requirement</span></span> | <span data-ttu-id="f612d-148">值</span><span class="sxs-lookup"><span data-stu-id="f612d-148">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="f612d-149">標頭</span><span class="sxs-lookup"><span data-stu-id="f612d-149">Header</span></span><br/> | <dl> <span data-ttu-id="f612d-150"><dt>Corecrt \_ math。h</dt></span><span class="sxs-lookup"><span data-stu-id="f612d-150"><dt>Corecrt\_math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f612d-151">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f612d-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f612d-152">**(DirectX HLSL) 內建函式**</span><span class="sxs-lookup"><span data-stu-id="f612d-152">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

