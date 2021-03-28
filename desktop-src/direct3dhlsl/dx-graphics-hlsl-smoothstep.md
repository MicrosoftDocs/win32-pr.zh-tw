---
title: smoothstep
description: 如果 x 位於0到1的範圍內，則傳回介於0和1之間的平滑 Hermite 插補。
ms.assetid: 6a879d82-f5ab-4e9b-bc9c-8988cbe6aa82
keywords:
- smoothstep HLSL
topic_type:
- apiref
api_name:
- smoothstep
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 64e828b52a4d4517e53ba1f1aaf0f687255ad02b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104971708"
---
# <a name="smoothstep"></a><span data-ttu-id="2919a-104">smoothstep</span><span class="sxs-lookup"><span data-stu-id="2919a-104">smoothstep</span></span>

<span data-ttu-id="2919a-105">如果 *x* 位於 \[ *min*、 *max* 的範圍內，則傳回0和1之間的平滑 Hermite 插補 \] 。</span><span class="sxs-lookup"><span data-stu-id="2919a-105">Returns a smooth Hermite interpolation between 0 and 1, if *x* is in the range \[*min*, *max*\].</span></span>



| <span data-ttu-id="2919a-106">*ret* smoothstep (*min*， *max*， *x*) </span><span class="sxs-lookup"><span data-stu-id="2919a-106">*ret* smoothstep(*min*, *max*, *x*)</span></span> |
|-------------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="2919a-107">參數</span><span class="sxs-lookup"><span data-stu-id="2919a-107">Parameters</span></span>



| <span data-ttu-id="2919a-108">項目</span><span class="sxs-lookup"><span data-stu-id="2919a-108">Item</span></span>                                                         | <span data-ttu-id="2919a-109">描述</span><span class="sxs-lookup"><span data-stu-id="2919a-109">Description</span></span>                                               |
|--------------------------------------------------------------|-----------------------------------------------------------|
| <span data-ttu-id="2919a-110"><span id="min"></span><span id="MIN"></span>*化*</span><span class="sxs-lookup"><span data-stu-id="2919a-110"><span id="min"></span><span id="MIN"></span>*min*</span></span><br/> | <span data-ttu-id="2919a-111">\[在 \] *x* 參數的最小範圍內。</span><span class="sxs-lookup"><span data-stu-id="2919a-111">\[in\] The minimum range of the *x* parameter.</span></span><br/> |
| <span data-ttu-id="2919a-112"><span id="max"></span><span id="MAX"></span>*麥克斯*</span><span class="sxs-lookup"><span data-stu-id="2919a-112"><span id="max"></span><span id="MAX"></span>*max*</span></span><br/> | <span data-ttu-id="2919a-113">\[在 \] *x* 參數的最大範圍內。</span><span class="sxs-lookup"><span data-stu-id="2919a-113">\[in\] The maximum range of the *x* parameter.</span></span><br/> |
| <span data-ttu-id="2919a-114"><span id="x"></span><span id="X"></span>*X*</span><span class="sxs-lookup"><span data-stu-id="2919a-114"><span id="x"></span><span id="X"></span>*x*</span></span><br/>       | <span data-ttu-id="2919a-115">\[\]指定要插入的值。</span><span class="sxs-lookup"><span data-stu-id="2919a-115">\[in\] The specified value to be interpolated.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="2919a-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="2919a-116">Return Value</span></span>

<span data-ttu-id="2919a-117">如果 *x* 小於 *最小值*，則傳回 0;如果 *x* 大於 *最大值*，則為1。否則，如果 *x* 是在 \[ *min*、 *max* 的範圍內，則介於0和1之間的值 \] 。</span><span class="sxs-lookup"><span data-stu-id="2919a-117">Returns 0 if *x* is less than *min*; 1 if *x* is greater than *max*; otherwise, a value between 0 and 1 if *x* is in the range \[*min*, *max*\].</span></span>

## <a name="remarks"></a><span data-ttu-id="2919a-118">備註</span><span class="sxs-lookup"><span data-stu-id="2919a-118">Remarks</span></span>

<span data-ttu-id="2919a-119">使用 **smoothstep** HLSL 內建函式可在兩個值之間建立順暢的轉換。</span><span class="sxs-lookup"><span data-stu-id="2919a-119">Use the **smoothstep** HLSL intrinsic function to create a smooth transition between two values.</span></span> <span data-ttu-id="2919a-120">例如，您可以使用此函數順暢地混合兩種色彩。</span><span class="sxs-lookup"><span data-stu-id="2919a-120">For example, you can use this function to blend two colors smoothly.</span></span>

## <a name="type-description"></a><span data-ttu-id="2919a-121">類型描述</span><span class="sxs-lookup"><span data-stu-id="2919a-121">Type Description</span></span>



| <span data-ttu-id="2919a-122">Name</span><span class="sxs-lookup"><span data-stu-id="2919a-122">Name</span></span>  | [<span data-ttu-id="2919a-123">**範本類型**</span><span class="sxs-lookup"><span data-stu-id="2919a-123">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="2919a-124">**元件類型**</span><span class="sxs-lookup"><span data-stu-id="2919a-124">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="2919a-125">大小</span><span class="sxs-lookup"><span data-stu-id="2919a-125">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="2919a-126">*x*</span><span class="sxs-lookup"><span data-stu-id="2919a-126">*x*</span></span>   | <span data-ttu-id="2919a-127">純 [**量、**](dx-graphics-hlsl-intrinsic-functions.md)**向量** 或 **矩陣**</span><span class="sxs-lookup"><span data-stu-id="2919a-127">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="2919a-128">**浮動**</span><span class="sxs-lookup"><span data-stu-id="2919a-128">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="2919a-129">任意</span><span class="sxs-lookup"><span data-stu-id="2919a-129">any</span></span>                            |
| <span data-ttu-id="2919a-130">*min*</span><span class="sxs-lookup"><span data-stu-id="2919a-130">*min*</span></span> | <span data-ttu-id="2919a-131">與輸入 *x* 相同</span><span class="sxs-lookup"><span data-stu-id="2919a-131">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="2919a-132">**浮動**</span><span class="sxs-lookup"><span data-stu-id="2919a-132">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="2919a-133">) 為輸入 *x* 的相同維度 (s</span><span class="sxs-lookup"><span data-stu-id="2919a-133">same dimension(s) as input *x*</span></span> |
| <span data-ttu-id="2919a-134">*max*</span><span class="sxs-lookup"><span data-stu-id="2919a-134">*max*</span></span> | <span data-ttu-id="2919a-135">與輸入 *x* 相同</span><span class="sxs-lookup"><span data-stu-id="2919a-135">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="2919a-136">**浮動**</span><span class="sxs-lookup"><span data-stu-id="2919a-136">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="2919a-137">) 為輸入 *x* 的相同維度 (s</span><span class="sxs-lookup"><span data-stu-id="2919a-137">same dimension(s) as input *x*</span></span> |
| <span data-ttu-id="2919a-138">*Ret*</span><span class="sxs-lookup"><span data-stu-id="2919a-138">*ret*</span></span> | <span data-ttu-id="2919a-139">與輸入 *x* 相同</span><span class="sxs-lookup"><span data-stu-id="2919a-139">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="2919a-140">**浮動**</span><span class="sxs-lookup"><span data-stu-id="2919a-140">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="2919a-141">) 為輸入 *x* 的相同維度 (s</span><span class="sxs-lookup"><span data-stu-id="2919a-141">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="2919a-142">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="2919a-142">Minimum Shader Model</span></span>

<span data-ttu-id="2919a-143">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="2919a-143">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="2919a-144">著色器模型</span><span class="sxs-lookup"><span data-stu-id="2919a-144">Shader Model</span></span>                                                                       | <span data-ttu-id="2919a-145">支援</span><span class="sxs-lookup"><span data-stu-id="2919a-145">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="2919a-146">[著色器模型 2 (DIRECTX HLSL) ](dx-graphics-hlsl-sm2.md) 和更高的著色器模型</span><span class="sxs-lookup"><span data-stu-id="2919a-146">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="2919a-147">是</span><span class="sxs-lookup"><span data-stu-id="2919a-147">yes</span></span>                 |
| [<span data-ttu-id="2919a-148">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="2919a-148">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="2919a-149">是 (\_ \_ 只有) 的 vs 1</span><span class="sxs-lookup"><span data-stu-id="2919a-149">yes (vs\_1\_1 only)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="2919a-150">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2919a-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2919a-151">**(DirectX HLSL) 內建函式**</span><span class="sxs-lookup"><span data-stu-id="2919a-151">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

