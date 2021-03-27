---
title: 鉗
description: 將指定的值個至指定的最小和最大範圍。
ms.assetid: bcfafcec-3f9c-4b65-950c-da34184d5cdb
keywords:
- 夾具 HLSL
topic_type:
- apiref
api_name:
- clamp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f5d6b0a3e83c0b1a5e511aba96df03b828b90c11
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682918"
---
# <a name="clamp"></a><span data-ttu-id="a26f6-104">鉗</span><span class="sxs-lookup"><span data-stu-id="a26f6-104">clamp</span></span>

<span data-ttu-id="a26f6-105">將指定的值個至指定的最小和最大範圍。</span><span class="sxs-lookup"><span data-stu-id="a26f6-105">Clamps the specified value to the specified minimum and maximum range.</span></span>



| <span data-ttu-id="a26f6-106">*ret* 夾具 (*x*、 *min*、 *max*) </span><span class="sxs-lookup"><span data-stu-id="a26f6-106">*ret* clamp(*x*, *min*, *max*)</span></span> |
|--------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="a26f6-107">參數</span><span class="sxs-lookup"><span data-stu-id="a26f6-107">Parameters</span></span>



| <span data-ttu-id="a26f6-108">項目</span><span class="sxs-lookup"><span data-stu-id="a26f6-108">Item</span></span>                                                         | <span data-ttu-id="a26f6-109">描述</span><span class="sxs-lookup"><span data-stu-id="a26f6-109">Description</span></span>                                    |
|--------------------------------------------------------------|------------------------------------------------|
| <span data-ttu-id="a26f6-110"><span id="x"></span><span id="X"></span>*X*</span><span class="sxs-lookup"><span data-stu-id="a26f6-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/>       | <span data-ttu-id="a26f6-111">\[在 [夾具] 中 \] 的值。</span><span class="sxs-lookup"><span data-stu-id="a26f6-111">\[in\] A value to clamp.</span></span><br/>            |
| <span data-ttu-id="a26f6-112"><span id="min"></span><span id="MIN"></span>*化*</span><span class="sxs-lookup"><span data-stu-id="a26f6-112"><span id="min"></span><span id="MIN"></span>*min*</span></span><br/> | <span data-ttu-id="a26f6-113">\[在 \] 指定的最小範圍內。</span><span class="sxs-lookup"><span data-stu-id="a26f6-113">\[in\] The specified minimum range.</span></span><br/> |
| <span data-ttu-id="a26f6-114"><span id="max"></span><span id="MAX"></span>*麥克斯*</span><span class="sxs-lookup"><span data-stu-id="a26f6-114"><span id="max"></span><span id="MAX"></span>*max*</span></span><br/> | <span data-ttu-id="a26f6-115">\[在 \] 指定的最大範圍內。</span><span class="sxs-lookup"><span data-stu-id="a26f6-115">\[in\] The specified maximum range.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="a26f6-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="a26f6-116">Return Value</span></span>

<span data-ttu-id="a26f6-117">*X* 參數的壓制值。</span><span class="sxs-lookup"><span data-stu-id="a26f6-117">The clamped value for the *x* parameter.</span></span>

## <a name="remarks"></a><span data-ttu-id="a26f6-118">備註</span><span class="sxs-lookup"><span data-stu-id="a26f6-118">Remarks</span></span>

<span data-ttu-id="a26f6-119">若為-INF 或 INF 的值，則會如預期般運作。</span><span class="sxs-lookup"><span data-stu-id="a26f6-119">For values of -INF or INF, clamp will behave as expected.</span></span> <span data-ttu-id="a26f6-120">不過，若為 NaN 的值，則結果為未定義。</span><span class="sxs-lookup"><span data-stu-id="a26f6-120">However for values of NaN, the results are undefined.</span></span>

## <a name="type-description"></a><span data-ttu-id="a26f6-121">類型描述</span><span class="sxs-lookup"><span data-stu-id="a26f6-121">Type Description</span></span>



| <span data-ttu-id="a26f6-122">Name</span><span class="sxs-lookup"><span data-stu-id="a26f6-122">Name</span></span>  | [<span data-ttu-id="a26f6-123">**範本類型**</span><span class="sxs-lookup"><span data-stu-id="a26f6-123">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="a26f6-124">**元件類型**</span><span class="sxs-lookup"><span data-stu-id="a26f6-124">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                 | <span data-ttu-id="a26f6-125">大小</span><span class="sxs-lookup"><span data-stu-id="a26f6-125">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="a26f6-126">*x*</span><span class="sxs-lookup"><span data-stu-id="a26f6-126">*x*</span></span>   | <span data-ttu-id="a26f6-127">純 [**量、**](dx-graphics-hlsl-intrinsic-functions.md)**向量** 或 **矩陣**</span><span class="sxs-lookup"><span data-stu-id="a26f6-127">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | <span data-ttu-id="a26f6-128">[**float**](/windows/desktop/WinProg/windows-data-types)、 [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="a26f6-128">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="a26f6-129">任意</span><span class="sxs-lookup"><span data-stu-id="a26f6-129">any</span></span>                            |
| <span data-ttu-id="a26f6-130">*min*</span><span class="sxs-lookup"><span data-stu-id="a26f6-130">*min*</span></span> | <span data-ttu-id="a26f6-131">與輸入 *x* 相同</span><span class="sxs-lookup"><span data-stu-id="a26f6-131">same as input *x*</span></span>                                                                                              | <span data-ttu-id="a26f6-132">[**float**](/windows/desktop/WinProg/windows-data-types)、 [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="a26f6-132">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="a26f6-133">) 為輸入 *x* 的相同維度 (s</span><span class="sxs-lookup"><span data-stu-id="a26f6-133">same dimension(s) as input *x*</span></span> |
| <span data-ttu-id="a26f6-134">*max*</span><span class="sxs-lookup"><span data-stu-id="a26f6-134">*max*</span></span> | <span data-ttu-id="a26f6-135">與輸入 *x* 相同</span><span class="sxs-lookup"><span data-stu-id="a26f6-135">same as input *x*</span></span>                                                                                              | <span data-ttu-id="a26f6-136">[**float**](/windows/desktop/WinProg/windows-data-types)、 [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="a26f6-136">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="a26f6-137">) 為輸入 *x* 的相同維度 (s</span><span class="sxs-lookup"><span data-stu-id="a26f6-137">same dimension(s) as input *x*</span></span> |
| <span data-ttu-id="a26f6-138">*Ret*</span><span class="sxs-lookup"><span data-stu-id="a26f6-138">*ret*</span></span> | <span data-ttu-id="a26f6-139">與輸入 *x* 相同</span><span class="sxs-lookup"><span data-stu-id="a26f6-139">same as input *x*</span></span>                                                                                              | <span data-ttu-id="a26f6-140">[**float**](/windows/desktop/WinProg/windows-data-types)、 [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="a26f6-140">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="a26f6-141">) 為輸入 *x* 的相同維度 (s</span><span class="sxs-lookup"><span data-stu-id="a26f6-141">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="a26f6-142">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="a26f6-142">Minimum Shader Model</span></span>

<span data-ttu-id="a26f6-143">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="a26f6-143">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="a26f6-144">著色器模型</span><span class="sxs-lookup"><span data-stu-id="a26f6-144">Shader Model</span></span>                                                                       | <span data-ttu-id="a26f6-145">支援</span><span class="sxs-lookup"><span data-stu-id="a26f6-145">Supported</span></span>             |
|------------------------------------------------------------------------------------|-----------------------|
| <span data-ttu-id="a26f6-146">[著色器模型 2 (DIRECTX HLSL) ](dx-graphics-hlsl-sm2.md) 和更高的著色器模型</span><span class="sxs-lookup"><span data-stu-id="a26f6-146">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="a26f6-147">是</span><span class="sxs-lookup"><span data-stu-id="a26f6-147">yes</span></span>                   |
| [<span data-ttu-id="a26f6-148">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="a26f6-148">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="a26f6-149">vs \_ 1 \_ 1 和 ps \_ 1 \_ 4</span><span class="sxs-lookup"><span data-stu-id="a26f6-149">vs\_1\_1 and ps\_1\_4</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="a26f6-150">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a26f6-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a26f6-151">**(DirectX HLSL) 內建函式**</span><span class="sxs-lookup"><span data-stu-id="a26f6-151">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

