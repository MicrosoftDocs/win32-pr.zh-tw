---
title: max
description: 選取 x 和 y 的較大。
ms.assetid: 08e17a0c-6d44-49ea-b613-bd262534522c
keywords:
- 最大 HLSL
topic_type:
- apiref
api_name:
- max
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9a40ccb32bb2c2fcd7ca7342b9d7d4d143688102
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104376193"
---
# <a name="max"></a><span data-ttu-id="ca97b-104">max</span><span class="sxs-lookup"><span data-stu-id="ca97b-104">max</span></span>

<span data-ttu-id="ca97b-105">選取 x 和 y 的較大。</span><span class="sxs-lookup"><span data-stu-id="ca97b-105">Selects the greater of x and y.</span></span>



| <span data-ttu-id="ca97b-106">ret max (x，y) </span><span class="sxs-lookup"><span data-stu-id="ca97b-106">ret max(x, y)</span></span> |
|---------------|



 

## <a name="parameters"></a><span data-ttu-id="ca97b-107">參數</span><span class="sxs-lookup"><span data-stu-id="ca97b-107">Parameters</span></span>



| <span data-ttu-id="ca97b-108">項目</span><span class="sxs-lookup"><span data-stu-id="ca97b-108">Item</span></span>                                                   | <span data-ttu-id="ca97b-109">描述</span><span class="sxs-lookup"><span data-stu-id="ca97b-109">Description</span></span>                          |
|--------------------------------------------------------|--------------------------------------|
| <span data-ttu-id="ca97b-110"><span id="x"></span><span id="X"></span>*X*</span><span class="sxs-lookup"><span data-stu-id="ca97b-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="ca97b-111">\[在 \] [x 輸入值] 中。</span><span class="sxs-lookup"><span data-stu-id="ca97b-111">\[in\] The x input value.</span></span><br/> |
| <span data-ttu-id="ca97b-112"><span id="y"></span><span id="Y"></span>*Y*</span><span class="sxs-lookup"><span data-stu-id="ca97b-112"><span id="y"></span><span id="Y"></span>*y*</span></span><br/> | <span data-ttu-id="ca97b-113">\[（在 \] y 輸入值中）。</span><span class="sxs-lookup"><span data-stu-id="ca97b-113">\[in\] The y input value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="ca97b-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="ca97b-114">Return Value</span></span>

<span data-ttu-id="ca97b-115">*X* 或 *y* 參數，以最大值為准。</span><span class="sxs-lookup"><span data-stu-id="ca97b-115">The *x* or *y* parameter, whichever is the largest value.</span></span>


## <a name="remarks"></a><span data-ttu-id="ca97b-116">備註</span><span class="sxs-lookup"><span data-stu-id="ca97b-116">Remarks</span></span>

<span data-ttu-id="ca97b-117">Denormals 的處理方式如下：</span><span class="sxs-lookup"><span data-stu-id="ca97b-117">Denormals are handled as follows:</span></span>

| <span data-ttu-id="ca97b-118">src0 src1-></span><span class="sxs-lookup"><span data-stu-id="ca97b-118">src0 src1-></span></span> | <span data-ttu-id="ca97b-119">-inf</span><span class="sxs-lookup"><span data-stu-id="ca97b-119">-inf</span></span> | <span data-ttu-id="ca97b-120">F</span><span class="sxs-lookup"><span data-stu-id="ca97b-120">F</span></span>             | <span data-ttu-id="ca97b-121">+inf</span><span class="sxs-lookup"><span data-stu-id="ca97b-121">+inf</span></span> | <span data-ttu-id="ca97b-122">NAN</span><span class="sxs-lookup"><span data-stu-id="ca97b-122">NAN</span></span>  |
|-------------|------|---------------|------|------|
| <span data-ttu-id="ca97b-123">-inf</span><span class="sxs-lookup"><span data-stu-id="ca97b-123">-inf</span></span>        | <span data-ttu-id="ca97b-124">-inf</span><span class="sxs-lookup"><span data-stu-id="ca97b-124">-inf</span></span> | <span data-ttu-id="ca97b-125">src1</span><span class="sxs-lookup"><span data-stu-id="ca97b-125">src1</span></span>          | <span data-ttu-id="ca97b-126">+inf</span><span class="sxs-lookup"><span data-stu-id="ca97b-126">+inf</span></span> | <span data-ttu-id="ca97b-127">-inf</span><span class="sxs-lookup"><span data-stu-id="ca97b-127">-inf</span></span> |
| <span data-ttu-id="ca97b-128">F</span><span class="sxs-lookup"><span data-stu-id="ca97b-128">F</span></span>           | <span data-ttu-id="ca97b-129">src0</span><span class="sxs-lookup"><span data-stu-id="ca97b-129">src0</span></span> | <span data-ttu-id="ca97b-130">src0 或 src1</span><span class="sxs-lookup"><span data-stu-id="ca97b-130">src0 or src1</span></span>  | <span data-ttu-id="ca97b-131">+inf</span><span class="sxs-lookup"><span data-stu-id="ca97b-131">+inf</span></span> | <span data-ttu-id="ca97b-132">src0</span><span class="sxs-lookup"><span data-stu-id="ca97b-132">src0</span></span> |
| <span data-ttu-id="ca97b-133">+inf</span><span class="sxs-lookup"><span data-stu-id="ca97b-133">+inf</span></span>        | <span data-ttu-id="ca97b-134">+inf</span><span class="sxs-lookup"><span data-stu-id="ca97b-134">+inf</span></span> | <span data-ttu-id="ca97b-135">+inf</span><span class="sxs-lookup"><span data-stu-id="ca97b-135">+inf</span></span>          | <span data-ttu-id="ca97b-136">+inf</span><span class="sxs-lookup"><span data-stu-id="ca97b-136">+inf</span></span> | <span data-ttu-id="ca97b-137">+inf</span><span class="sxs-lookup"><span data-stu-id="ca97b-137">+inf</span></span> |
| <span data-ttu-id="ca97b-138">NaN</span><span class="sxs-lookup"><span data-stu-id="ca97b-138">NaN</span></span>         | <span data-ttu-id="ca97b-139">-inf</span><span class="sxs-lookup"><span data-stu-id="ca97b-139">-inf</span></span> | <span data-ttu-id="ca97b-140">src1</span><span class="sxs-lookup"><span data-stu-id="ca97b-140">src1</span></span>          | <span data-ttu-id="ca97b-141">+inf</span><span class="sxs-lookup"><span data-stu-id="ca97b-141">+inf</span></span> | <span data-ttu-id="ca97b-142">NaN</span><span class="sxs-lookup"><span data-stu-id="ca97b-142">NaN</span></span>  |

<span data-ttu-id="ca97b-143">F 表示有限實數。</span><span class="sxs-lookup"><span data-stu-id="ca97b-143">F means finite-real number.</span></span>


## <a name="type-description"></a><span data-ttu-id="ca97b-144">類型描述</span><span class="sxs-lookup"><span data-stu-id="ca97b-144">Type Description</span></span>

| <span data-ttu-id="ca97b-145">Name</span><span class="sxs-lookup"><span data-stu-id="ca97b-145">Name</span></span> | <span data-ttu-id="ca97b-146">輸入/輸出</span><span class="sxs-lookup"><span data-stu-id="ca97b-146">In/Out</span></span>      | [<span data-ttu-id="ca97b-147">**範本類型**</span><span class="sxs-lookup"><span data-stu-id="ca97b-147">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="ca97b-148">**元件類型**</span><span class="sxs-lookup"><span data-stu-id="ca97b-148">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                 | <span data-ttu-id="ca97b-149">大小</span><span class="sxs-lookup"><span data-stu-id="ca97b-149">Size</span></span>                         |
|------|-------------|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|------------------------------|
| <span data-ttu-id="ca97b-150">x</span><span class="sxs-lookup"><span data-stu-id="ca97b-150">x</span></span>    | <span data-ttu-id="ca97b-151">in</span><span class="sxs-lookup"><span data-stu-id="ca97b-151">in</span></span>          | <span data-ttu-id="ca97b-152">純 [**量、**](dx-graphics-hlsl-intrinsic-functions.md)**向量** 或 **矩陣**</span><span class="sxs-lookup"><span data-stu-id="ca97b-152">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | <span data-ttu-id="ca97b-153">[**float**](/windows/desktop/WinProg/windows-data-types)、 [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="ca97b-153">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="ca97b-154">任意</span><span class="sxs-lookup"><span data-stu-id="ca97b-154">any</span></span>                          |
| <span data-ttu-id="ca97b-155">y</span><span class="sxs-lookup"><span data-stu-id="ca97b-155">y</span></span>    | <span data-ttu-id="ca97b-156">in</span><span class="sxs-lookup"><span data-stu-id="ca97b-156">in</span></span>          | <span data-ttu-id="ca97b-157">與輸入 x 相同</span><span class="sxs-lookup"><span data-stu-id="ca97b-157">same as input x</span></span>                                                                                                | <span data-ttu-id="ca97b-158">[**float**](/windows/desktop/WinProg/windows-data-types)、 [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="ca97b-158">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="ca97b-159">) 為輸入 x 的相同維度 (s</span><span class="sxs-lookup"><span data-stu-id="ca97b-159">same dimension(s) as input x</span></span> |
| <span data-ttu-id="ca97b-160">Ret</span><span class="sxs-lookup"><span data-stu-id="ca97b-160">ret</span></span>  | <span data-ttu-id="ca97b-161">傳回類型</span><span class="sxs-lookup"><span data-stu-id="ca97b-161">return type</span></span> | <span data-ttu-id="ca97b-162">與輸入 x 相同</span><span class="sxs-lookup"><span data-stu-id="ca97b-162">same as input x</span></span>                                                                                                | <span data-ttu-id="ca97b-163">[**float**](/windows/desktop/WinProg/windows-data-types)、 [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="ca97b-163">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="ca97b-164">) 為輸入 x 的相同維度 (s</span><span class="sxs-lookup"><span data-stu-id="ca97b-164">same dimension(s) as input x</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="ca97b-165">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="ca97b-165">Minimum Shader Model</span></span>

<span data-ttu-id="ca97b-166">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="ca97b-166">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="ca97b-167">著色器模型</span><span class="sxs-lookup"><span data-stu-id="ca97b-167">Shader Model</span></span>                                                                       | <span data-ttu-id="ca97b-168">支援</span><span class="sxs-lookup"><span data-stu-id="ca97b-168">Supported</span></span>                   |
|------------------------------------------------------------------------------------|-----------------------------|
| <span data-ttu-id="ca97b-169">[著色器模型 2 (DIRECTX HLSL) ](dx-graphics-hlsl-sm2.md) 和更高的著色器模型</span><span class="sxs-lookup"><span data-stu-id="ca97b-169">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="ca97b-170">是</span><span class="sxs-lookup"><span data-stu-id="ca97b-170">yes</span></span>                         |
| [<span data-ttu-id="ca97b-171">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="ca97b-171">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="ca97b-172">是 (vs \_ 1 \_ 1 和 ps \_ 1 \_ 4) </span><span class="sxs-lookup"><span data-stu-id="ca97b-172">yes (vs\_1\_1 and ps\_1\_4)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="ca97b-173">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ca97b-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca97b-174">**(DirectX HLSL) 內建函式**</span><span class="sxs-lookup"><span data-stu-id="ca97b-174">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

[<span data-ttu-id="ca97b-175">**DirectX 功能規格**</span><span class="sxs-lookup"><span data-stu-id="ca97b-175">**DirectX Functional Specification**</span></span>](https://microsoft.github.io/DirectX-Specs/d3d/archive/D3D11_3_FunctionalSpec.htm#inst_MAX) 
</dt> </dl>
 
