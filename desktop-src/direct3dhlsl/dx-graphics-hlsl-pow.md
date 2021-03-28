---
title: pow
description: 傳回指定之乘冪的指定值。
ms.assetid: 1d64452c-81c7-4ef5-a332-13e0263c2cd1
keywords:
- pow HLSL
topic_type:
- apiref
api_name:
- pow
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f190c374b6c0ac42d41862eb918f0c0482b6d785
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463633"
---
# <a name="pow"></a><span data-ttu-id="31855-104">pow</span><span class="sxs-lookup"><span data-stu-id="31855-104">pow</span></span>

<span data-ttu-id="31855-105">傳回指定之乘冪的指定值。</span><span class="sxs-lookup"><span data-stu-id="31855-105">Returns the specified value raised to the specified power.</span></span>



| <span data-ttu-id="31855-106">*ret* pow (*x*， *y*) </span><span class="sxs-lookup"><span data-stu-id="31855-106">*ret* pow(*x*, *y*)</span></span> |
|---------------------|



 

## <a name="parameters"></a><span data-ttu-id="31855-107">參數</span><span class="sxs-lookup"><span data-stu-id="31855-107">Parameters</span></span>



| <span data-ttu-id="31855-108">項目</span><span class="sxs-lookup"><span data-stu-id="31855-108">Item</span></span>                                                   | <span data-ttu-id="31855-109">描述</span><span class="sxs-lookup"><span data-stu-id="31855-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="31855-110"><span id="x"></span><span id="X"></span>*X*</span><span class="sxs-lookup"><span data-stu-id="31855-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="31855-111">\[在 \] 指定的值中。</span><span class="sxs-lookup"><span data-stu-id="31855-111">\[in\] The specified value.</span></span><br/> |
| <span data-ttu-id="31855-112"><span id="y"></span><span id="Y"></span>*Y*</span><span class="sxs-lookup"><span data-stu-id="31855-112"><span id="y"></span><span id="Y"></span>*y*</span></span><br/> | <span data-ttu-id="31855-113">\[在 \] 指定的電源中。</span><span class="sxs-lookup"><span data-stu-id="31855-113">\[in\] The specified power.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="31855-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="31855-114">Return Value</span></span>

<span data-ttu-id="31855-115">*X* 參數，引發至 *y* 參數的乘冪。</span><span class="sxs-lookup"><span data-stu-id="31855-115">The *x* parameter raised to the power of the *y* parameter.</span></span>

## <a name="remarks"></a><span data-ttu-id="31855-116">備註</span><span class="sxs-lookup"><span data-stu-id="31855-116">Remarks</span></span>

<span data-ttu-id="31855-117">**Pow** HLSL 內建函式會計算 *x*<sup>y</sup>。</span><span class="sxs-lookup"><span data-stu-id="31855-117">The **pow** HLSL intrinsic function calculates *x*<sup>y</sup>.</span></span>



| <span data-ttu-id="31855-118">X</span><span class="sxs-lookup"><span data-stu-id="31855-118">X</span></span>      | <span data-ttu-id="31855-119">Y</span><span class="sxs-lookup"><span data-stu-id="31855-119">Y</span></span>      | <span data-ttu-id="31855-120">結果</span><span class="sxs-lookup"><span data-stu-id="31855-120">Result</span></span>                                                                      |
|--------|--------|-----------------------------------------------------------------------------|
| <span data-ttu-id="31855-121">< 0</span><span class="sxs-lookup"><span data-stu-id="31855-121">< 0</span></span> | <span data-ttu-id="31855-122">任意</span><span class="sxs-lookup"><span data-stu-id="31855-122">any</span></span>    | <span data-ttu-id="31855-123">NAN</span><span class="sxs-lookup"><span data-stu-id="31855-123">NAN</span></span>                                                                         |
| <span data-ttu-id="31855-124">> 0</span><span class="sxs-lookup"><span data-stu-id="31855-124">> 0</span></span> | <span data-ttu-id="31855-125">= = 0</span><span class="sxs-lookup"><span data-stu-id="31855-125">== 0</span></span>   | <span data-ttu-id="31855-126">1</span><span class="sxs-lookup"><span data-stu-id="31855-126">1</span></span>                                                                           |
| <span data-ttu-id="31855-127">= = 0</span><span class="sxs-lookup"><span data-stu-id="31855-127">== 0</span></span>   | <span data-ttu-id="31855-128">> 0</span><span class="sxs-lookup"><span data-stu-id="31855-128">> 0</span></span> | <span data-ttu-id="31855-129">0</span><span class="sxs-lookup"><span data-stu-id="31855-129">0</span></span>                                                                           |
| <span data-ttu-id="31855-130">= = 0</span><span class="sxs-lookup"><span data-stu-id="31855-130">== 0</span></span>   | <span data-ttu-id="31855-131">< 0</span><span class="sxs-lookup"><span data-stu-id="31855-131">< 0</span></span> | <span data-ttu-id="31855-132">inf</span><span class="sxs-lookup"><span data-stu-id="31855-132">inf</span></span>                                                                         |
| <span data-ttu-id="31855-133">> 0</span><span class="sxs-lookup"><span data-stu-id="31855-133">> 0</span></span> | <span data-ttu-id="31855-134">< 0</span><span class="sxs-lookup"><span data-stu-id="31855-134">< 0</span></span> | <span data-ttu-id="31855-135">1/X<sup>-Y</sup></span><span class="sxs-lookup"><span data-stu-id="31855-135">1/X<sup>-Y</sup></span></span>                                                            |
| <span data-ttu-id="31855-136">= = 0</span><span class="sxs-lookup"><span data-stu-id="31855-136">== 0</span></span>   | <span data-ttu-id="31855-137">= = 0</span><span class="sxs-lookup"><span data-stu-id="31855-137">== 0</span></span>   | <span data-ttu-id="31855-138">相依于特定圖形處理器</span><span class="sxs-lookup"><span data-stu-id="31855-138">Depends on the particular graphics processor</span></span><br/> <span data-ttu-id="31855-139">0、1或 NAN</span><span class="sxs-lookup"><span data-stu-id="31855-139">0, or 1, or NAN</span></span><br/> |



 

## <a name="type-description"></a><span data-ttu-id="31855-140">類型描述</span><span class="sxs-lookup"><span data-stu-id="31855-140">Type Description</span></span>



| <span data-ttu-id="31855-141">Name</span><span class="sxs-lookup"><span data-stu-id="31855-141">Name</span></span>  | [<span data-ttu-id="31855-142">**範本類型**</span><span class="sxs-lookup"><span data-stu-id="31855-142">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="31855-143">**元件類型**</span><span class="sxs-lookup"><span data-stu-id="31855-143">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="31855-144">大小</span><span class="sxs-lookup"><span data-stu-id="31855-144">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="31855-145">*x*</span><span class="sxs-lookup"><span data-stu-id="31855-145">*x*</span></span>   | <span data-ttu-id="31855-146">純 [**量、**](dx-graphics-hlsl-intrinsic-functions.md)**向量** 或 **矩陣**</span><span class="sxs-lookup"><span data-stu-id="31855-146">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="31855-147">**浮動**</span><span class="sxs-lookup"><span data-stu-id="31855-147">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="31855-148">任意</span><span class="sxs-lookup"><span data-stu-id="31855-148">any</span></span>                            |
| <span data-ttu-id="31855-149">*y*</span><span class="sxs-lookup"><span data-stu-id="31855-149">*y*</span></span>   | <span data-ttu-id="31855-150">與輸入 *x* 相同</span><span class="sxs-lookup"><span data-stu-id="31855-150">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="31855-151">**浮動**</span><span class="sxs-lookup"><span data-stu-id="31855-151">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="31855-152">) 為輸入 *x* 的相同維度 (s</span><span class="sxs-lookup"><span data-stu-id="31855-152">same dimension(s) as input *x*</span></span> |
| <span data-ttu-id="31855-153">*Ret*</span><span class="sxs-lookup"><span data-stu-id="31855-153">*ret*</span></span> | <span data-ttu-id="31855-154">與輸入 *x* 相同</span><span class="sxs-lookup"><span data-stu-id="31855-154">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="31855-155">**浮動**</span><span class="sxs-lookup"><span data-stu-id="31855-155">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="31855-156">) 為輸入 *x* 的相同維度 (s</span><span class="sxs-lookup"><span data-stu-id="31855-156">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="31855-157">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="31855-157">Minimum Shader Model</span></span>

<span data-ttu-id="31855-158">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="31855-158">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="31855-159">著色器模型</span><span class="sxs-lookup"><span data-stu-id="31855-159">Shader Model</span></span>                                                                       | <span data-ttu-id="31855-160">支援</span><span class="sxs-lookup"><span data-stu-id="31855-160">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="31855-161">[著色器模型 2 (DIRECTX HLSL) ](dx-graphics-hlsl-sm2.md) 和更高的著色器模型</span><span class="sxs-lookup"><span data-stu-id="31855-161">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="31855-162">是</span><span class="sxs-lookup"><span data-stu-id="31855-162">yes</span></span>                 |
| [<span data-ttu-id="31855-163">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="31855-163">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="31855-164">是 (\_ \_ 只有) 的 vs 1</span><span class="sxs-lookup"><span data-stu-id="31855-164">yes (vs\_1\_1 only)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="31855-165">另請參閱</span><span class="sxs-lookup"><span data-stu-id="31855-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31855-166">**(DirectX HLSL) 內建函式**</span><span class="sxs-lookup"><span data-stu-id="31855-166">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

