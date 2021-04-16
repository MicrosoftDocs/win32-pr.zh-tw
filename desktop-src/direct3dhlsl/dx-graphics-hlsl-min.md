---
title: 分鐘
description: 選取 x 和 y 的較小者。
ms.assetid: 4e10cfc2-d680-4d7f-81b2-fa52024f902d
keywords:
- 最小 HLSL
topic_type:
- apiref
api_name:
- min
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 129c5cb641c2d69b6c1365d8221663e264060532
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463636"
---
# <a name="min"></a><span data-ttu-id="fb687-104">分鐘</span><span class="sxs-lookup"><span data-stu-id="fb687-104">min</span></span>

<span data-ttu-id="fb687-105">選取 x 和 y 的較小者。</span><span class="sxs-lookup"><span data-stu-id="fb687-105">Selects the lesser of x and y.</span></span>



| <span data-ttu-id="fb687-106">ret min (x，y) </span><span class="sxs-lookup"><span data-stu-id="fb687-106">ret min(x, y)</span></span> |
|---------------|



 

## <a name="parameters"></a><span data-ttu-id="fb687-107">參數</span><span class="sxs-lookup"><span data-stu-id="fb687-107">Parameters</span></span>



| <span data-ttu-id="fb687-108">項目</span><span class="sxs-lookup"><span data-stu-id="fb687-108">Item</span></span>                                                   | <span data-ttu-id="fb687-109">描述</span><span class="sxs-lookup"><span data-stu-id="fb687-109">Description</span></span>                          |
|--------------------------------------------------------|--------------------------------------|
| <span data-ttu-id="fb687-110"><span id="x"></span><span id="X"></span>*X*</span><span class="sxs-lookup"><span data-stu-id="fb687-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="fb687-111">\[在 \] [x 輸入值] 中。</span><span class="sxs-lookup"><span data-stu-id="fb687-111">\[in\] The x input value.</span></span><br/> |
| <span data-ttu-id="fb687-112"><span id="y"></span><span id="Y"></span>*Y*</span><span class="sxs-lookup"><span data-stu-id="fb687-112"><span id="y"></span><span id="Y"></span>*y*</span></span><br/> | <span data-ttu-id="fb687-113">\[（在 \] y 輸入值中）。</span><span class="sxs-lookup"><span data-stu-id="fb687-113">\[in\] The y input value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="fb687-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="fb687-114">Return Value</span></span>

<span data-ttu-id="fb687-115">*X* 或 *y* 參數，以最小值為准。</span><span class="sxs-lookup"><span data-stu-id="fb687-115">The *x* or *y* parameter, whichever is the smallest value.</span></span>


## <a name="remarks"></a><span data-ttu-id="fb687-116">備註</span><span class="sxs-lookup"><span data-stu-id="fb687-116">Remarks</span></span>

<span data-ttu-id="fb687-117">Denormals 的處理方式如下：</span><span class="sxs-lookup"><span data-stu-id="fb687-117">Denormals are handled as follows:</span></span>

| <span data-ttu-id="fb687-118">src0 src1-></span><span class="sxs-lookup"><span data-stu-id="fb687-118">src0 src1-></span></span> | <span data-ttu-id="fb687-119">-inf</span><span class="sxs-lookup"><span data-stu-id="fb687-119">-inf</span></span> | <span data-ttu-id="fb687-120">F</span><span class="sxs-lookup"><span data-stu-id="fb687-120">F</span></span>             | <span data-ttu-id="fb687-121">+inf</span><span class="sxs-lookup"><span data-stu-id="fb687-121">+inf</span></span> | <span data-ttu-id="fb687-122">NAN</span><span class="sxs-lookup"><span data-stu-id="fb687-122">NAN</span></span>  |
|-------------|------|---------------|------|------|
| <span data-ttu-id="fb687-123">-inf</span><span class="sxs-lookup"><span data-stu-id="fb687-123">-inf</span></span>        | <span data-ttu-id="fb687-124">-inf</span><span class="sxs-lookup"><span data-stu-id="fb687-124">-inf</span></span> | <span data-ttu-id="fb687-125">-inf</span><span class="sxs-lookup"><span data-stu-id="fb687-125">-inf</span></span>          | <span data-ttu-id="fb687-126">-inf</span><span class="sxs-lookup"><span data-stu-id="fb687-126">-inf</span></span> | <span data-ttu-id="fb687-127">-inf</span><span class="sxs-lookup"><span data-stu-id="fb687-127">-inf</span></span> |
| <span data-ttu-id="fb687-128">F</span><span class="sxs-lookup"><span data-stu-id="fb687-128">F</span></span>           | <span data-ttu-id="fb687-129">-inf</span><span class="sxs-lookup"><span data-stu-id="fb687-129">-inf</span></span> | <span data-ttu-id="fb687-130">src0 或 src1</span><span class="sxs-lookup"><span data-stu-id="fb687-130">src0 or src1</span></span>  | <span data-ttu-id="fb687-131">src0</span><span class="sxs-lookup"><span data-stu-id="fb687-131">src0</span></span> | <span data-ttu-id="fb687-132">src0</span><span class="sxs-lookup"><span data-stu-id="fb687-132">src0</span></span> |
| <span data-ttu-id="fb687-133">+inf</span><span class="sxs-lookup"><span data-stu-id="fb687-133">+inf</span></span>        | <span data-ttu-id="fb687-134">-inf</span><span class="sxs-lookup"><span data-stu-id="fb687-134">-inf</span></span> | <span data-ttu-id="fb687-135">src1</span><span class="sxs-lookup"><span data-stu-id="fb687-135">src1</span></span>          | <span data-ttu-id="fb687-136">+inf</span><span class="sxs-lookup"><span data-stu-id="fb687-136">+inf</span></span> | <span data-ttu-id="fb687-137">+inf</span><span class="sxs-lookup"><span data-stu-id="fb687-137">+inf</span></span> |
| <span data-ttu-id="fb687-138">NaN</span><span class="sxs-lookup"><span data-stu-id="fb687-138">NaN</span></span>         | <span data-ttu-id="fb687-139">-inf</span><span class="sxs-lookup"><span data-stu-id="fb687-139">-inf</span></span> | <span data-ttu-id="fb687-140">src1</span><span class="sxs-lookup"><span data-stu-id="fb687-140">src1</span></span>          | <span data-ttu-id="fb687-141">+inf</span><span class="sxs-lookup"><span data-stu-id="fb687-141">+inf</span></span> | <span data-ttu-id="fb687-142">NaN</span><span class="sxs-lookup"><span data-stu-id="fb687-142">NaN</span></span>  |

<span data-ttu-id="fb687-143">F 表示有限實數。</span><span class="sxs-lookup"><span data-stu-id="fb687-143">F means finite-real number.</span></span>


## <a name="type-description"></a><span data-ttu-id="fb687-144">類型描述</span><span class="sxs-lookup"><span data-stu-id="fb687-144">Type Description</span></span>

| <span data-ttu-id="fb687-145">Name</span><span class="sxs-lookup"><span data-stu-id="fb687-145">Name</span></span> | <span data-ttu-id="fb687-146">輸入/輸出</span><span class="sxs-lookup"><span data-stu-id="fb687-146">In/Out</span></span>      | [<span data-ttu-id="fb687-147">**範本類型**</span><span class="sxs-lookup"><span data-stu-id="fb687-147">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="fb687-148">**元件類型**</span><span class="sxs-lookup"><span data-stu-id="fb687-148">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                 | <span data-ttu-id="fb687-149">大小</span><span class="sxs-lookup"><span data-stu-id="fb687-149">Size</span></span>                         |
|------|-------------|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|------------------------------|
| <span data-ttu-id="fb687-150">x</span><span class="sxs-lookup"><span data-stu-id="fb687-150">x</span></span>    | <span data-ttu-id="fb687-151">in</span><span class="sxs-lookup"><span data-stu-id="fb687-151">in</span></span>          | <span data-ttu-id="fb687-152">純 [**量、**](dx-graphics-hlsl-intrinsic-functions.md)**向量** 或 **矩陣**</span><span class="sxs-lookup"><span data-stu-id="fb687-152">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | <span data-ttu-id="fb687-153">[**float**](/windows/desktop/WinProg/windows-data-types)、 [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="fb687-153">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="fb687-154">任意</span><span class="sxs-lookup"><span data-stu-id="fb687-154">any</span></span>                          |
| <span data-ttu-id="fb687-155">y</span><span class="sxs-lookup"><span data-stu-id="fb687-155">y</span></span>    | <span data-ttu-id="fb687-156">in</span><span class="sxs-lookup"><span data-stu-id="fb687-156">in</span></span>          | <span data-ttu-id="fb687-157">與輸入 x 相同</span><span class="sxs-lookup"><span data-stu-id="fb687-157">same as input x</span></span>                                                                                                | <span data-ttu-id="fb687-158">[**float**](/windows/desktop/WinProg/windows-data-types)、 [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="fb687-158">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="fb687-159">) 為輸入 x 的相同維度 (s</span><span class="sxs-lookup"><span data-stu-id="fb687-159">same dimension(s) as input x</span></span> |
| <span data-ttu-id="fb687-160">Ret</span><span class="sxs-lookup"><span data-stu-id="fb687-160">ret</span></span>  | <span data-ttu-id="fb687-161">傳回類型</span><span class="sxs-lookup"><span data-stu-id="fb687-161">return type</span></span> | <span data-ttu-id="fb687-162">與輸入 x 相同</span><span class="sxs-lookup"><span data-stu-id="fb687-162">same as input x</span></span>                                                                                                | <span data-ttu-id="fb687-163">[**float**](/windows/desktop/WinProg/windows-data-types)、 [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="fb687-163">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="fb687-164">) 為輸入 x 的相同維度 (s</span><span class="sxs-lookup"><span data-stu-id="fb687-164">same dimension(s) as input x</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="fb687-165">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="fb687-165">Minimum Shader Model</span></span>

<span data-ttu-id="fb687-166">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="fb687-166">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="fb687-167">著色器模型</span><span class="sxs-lookup"><span data-stu-id="fb687-167">Shader Model</span></span>                                                                       | <span data-ttu-id="fb687-168">支援</span><span class="sxs-lookup"><span data-stu-id="fb687-168">Supported</span></span>                   |
|------------------------------------------------------------------------------------|-----------------------------|
| <span data-ttu-id="fb687-169">[著色器模型 2 (DIRECTX HLSL) ](dx-graphics-hlsl-sm2.md) 和更高的著色器模型</span><span class="sxs-lookup"><span data-stu-id="fb687-169">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="fb687-170">是</span><span class="sxs-lookup"><span data-stu-id="fb687-170">yes</span></span>                         |
| [<span data-ttu-id="fb687-171">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="fb687-171">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="fb687-172">是 (vs \_ 1 \_ 1 和 ps \_ 1 \_ 4) </span><span class="sxs-lookup"><span data-stu-id="fb687-172">yes (vs\_1\_1 and ps\_1\_4)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="fb687-173">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fb687-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb687-174">**(DirectX HLSL) 內建函式**</span><span class="sxs-lookup"><span data-stu-id="fb687-174">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

[<span data-ttu-id="fb687-175">**DirectX 功能規格**</span><span class="sxs-lookup"><span data-stu-id="fb687-175">**DirectX Functional Specification**</span></span>](https://microsoft.github.io/DirectX-Specs/d3d/archive/D3D11_3_FunctionalSpec.htm#inst_MIN)