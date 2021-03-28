---
title: texCUBEgrad
description: 使用漸層來選取 mip 層級，以取樣 cube 紋理。 |texCUBEgrad
ms.assetid: ebc5e38a-e314-43b0-9a00-7e4147e24bf0
keywords:
- texCUBEgrad HLSL
topic_type:
- apiref
api_name:
- texCUBEgrad
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 694382488754c221c59df72112678a5971e62c0b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104035250"
---
# <a name="texcubegrad"></a><span data-ttu-id="d623e-105">texCUBEgrad</span><span class="sxs-lookup"><span data-stu-id="d623e-105">texCUBEgrad</span></span>

<span data-ttu-id="d623e-106">使用漸層來選取 mip 層級，以取樣 cube 紋理。</span><span class="sxs-lookup"><span data-stu-id="d623e-106">Samples a cube texture using a gradient to select the mip level.</span></span>



| <span data-ttu-id="d623e-107">ret texCUBEgrad (s、t、ddx、ddy) </span><span class="sxs-lookup"><span data-stu-id="d623e-107">ret texCUBEgrad(s, t, ddx, ddy)</span></span> |
|---------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="d623e-108">參數</span><span class="sxs-lookup"><span data-stu-id="d623e-108">Parameters</span></span>



| <span data-ttu-id="d623e-109">項目</span><span class="sxs-lookup"><span data-stu-id="d623e-109">Item</span></span>                                                         | <span data-ttu-id="d623e-110">描述</span><span class="sxs-lookup"><span data-stu-id="d623e-110">Description</span></span>                                                                  |
|--------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="d623e-111"><span id="s"></span><span id="S"></span>*！*</span><span class="sxs-lookup"><span data-stu-id="d623e-111"><span id="s"></span><span id="S"></span>*s*</span></span><br/>       | <span data-ttu-id="d623e-112">\[在 \] 取樣器狀態中。</span><span class="sxs-lookup"><span data-stu-id="d623e-112">\[in\] The sampler state.</span></span><br/>                                         |
| <span data-ttu-id="d623e-113"><span id="t"></span><span id="T"></span>*10gbase-t*</span><span class="sxs-lookup"><span data-stu-id="d623e-113"><span id="t"></span><span id="T"></span>*t*</span></span><br/>       | <span data-ttu-id="d623e-114">\[在 \] 紋理座標中。</span><span class="sxs-lookup"><span data-stu-id="d623e-114">\[in\] The texture coordinate.</span></span><br/>                                    |
| <span data-ttu-id="d623e-115"><span id="ddx"></span><span id="DDX"></span>*ddx*</span><span class="sxs-lookup"><span data-stu-id="d623e-115"><span id="ddx"></span><span id="DDX"></span>*ddx*</span></span><br/> | <span data-ttu-id="d623e-116">\[以 \] x 方向變更 surface 幾何的速率。</span><span class="sxs-lookup"><span data-stu-id="d623e-116">\[in\] Rate of change of the surface geometry in the x direction.</span></span><br/> |
| <span data-ttu-id="d623e-117"><span id="ddy"></span><span id="DDY"></span>*ddy*</span><span class="sxs-lookup"><span data-stu-id="d623e-117"><span id="ddy"></span><span id="DDY"></span>*ddy*</span></span><br/> | <span data-ttu-id="d623e-118">\[以 \] y 方向變更 surface 幾何的速率。</span><span class="sxs-lookup"><span data-stu-id="d623e-118">\[in\] Rate of change of the surface geometry in the y direction.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="d623e-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="d623e-119">Return Value</span></span>

<span data-ttu-id="d623e-120">材質資料的值。</span><span class="sxs-lookup"><span data-stu-id="d623e-120">The value of the texture data.</span></span>

## <a name="type-description"></a><span data-ttu-id="d623e-121">類型描述</span><span class="sxs-lookup"><span data-stu-id="d623e-121">Type Description</span></span>



| <span data-ttu-id="d623e-122">Name</span><span class="sxs-lookup"><span data-stu-id="d623e-122">Name</span></span> | <span data-ttu-id="d623e-123">輸入/輸出</span><span class="sxs-lookup"><span data-stu-id="d623e-123">In/Out</span></span> | [<span data-ttu-id="d623e-124">**範本類型**</span><span class="sxs-lookup"><span data-stu-id="d623e-124">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="d623e-125">**元件類型**</span><span class="sxs-lookup"><span data-stu-id="d623e-125">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="d623e-126">大小</span><span class="sxs-lookup"><span data-stu-id="d623e-126">Size</span></span> |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="d623e-127">s</span><span class="sxs-lookup"><span data-stu-id="d623e-127">s</span></span>    | <span data-ttu-id="d623e-128">in</span><span class="sxs-lookup"><span data-stu-id="d623e-128">in</span></span>     | [<span data-ttu-id="d623e-129">**物件**</span><span class="sxs-lookup"><span data-stu-id="d623e-129">**object**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="d623e-130">samplerCUBE</span><span class="sxs-lookup"><span data-stu-id="d623e-130">samplerCUBE</span></span>](dx-graphics-hlsl-sampler.md)                    | <span data-ttu-id="d623e-131">1</span><span class="sxs-lookup"><span data-stu-id="d623e-131">1</span></span>    |
| <span data-ttu-id="d623e-132">t</span><span class="sxs-lookup"><span data-stu-id="d623e-132">t</span></span>    | <span data-ttu-id="d623e-133">in</span><span class="sxs-lookup"><span data-stu-id="d623e-133">in</span></span>     | [<span data-ttu-id="d623e-134">**向量**</span><span class="sxs-lookup"><span data-stu-id="d623e-134">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="d623e-135">**浮動**</span><span class="sxs-lookup"><span data-stu-id="d623e-135">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="d623e-136">3</span><span class="sxs-lookup"><span data-stu-id="d623e-136">3</span></span>    |
| <span data-ttu-id="d623e-137">ddx</span><span class="sxs-lookup"><span data-stu-id="d623e-137">ddx</span></span>  | <span data-ttu-id="d623e-138">in</span><span class="sxs-lookup"><span data-stu-id="d623e-138">in</span></span>     | [<span data-ttu-id="d623e-139">**向量**</span><span class="sxs-lookup"><span data-stu-id="d623e-139">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="d623e-140">**浮動**</span><span class="sxs-lookup"><span data-stu-id="d623e-140">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="d623e-141">3</span><span class="sxs-lookup"><span data-stu-id="d623e-141">3</span></span>    |
| <span data-ttu-id="d623e-142">ddy</span><span class="sxs-lookup"><span data-stu-id="d623e-142">ddy</span></span>  | <span data-ttu-id="d623e-143">in</span><span class="sxs-lookup"><span data-stu-id="d623e-143">in</span></span>     | [<span data-ttu-id="d623e-144">**向量**</span><span class="sxs-lookup"><span data-stu-id="d623e-144">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="d623e-145">**浮動**</span><span class="sxs-lookup"><span data-stu-id="d623e-145">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="d623e-146">3</span><span class="sxs-lookup"><span data-stu-id="d623e-146">3</span></span>    |
| <span data-ttu-id="d623e-147">Ret</span><span class="sxs-lookup"><span data-stu-id="d623e-147">ret</span></span>  | <span data-ttu-id="d623e-148">out</span><span class="sxs-lookup"><span data-stu-id="d623e-148">out</span></span>    | [<span data-ttu-id="d623e-149">**向量**</span><span class="sxs-lookup"><span data-stu-id="d623e-149">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="d623e-150">**浮動**</span><span class="sxs-lookup"><span data-stu-id="d623e-150">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="d623e-151">4</span><span class="sxs-lookup"><span data-stu-id="d623e-151">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="d623e-152">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="d623e-152">Minimum Shader Model</span></span>

<span data-ttu-id="d623e-153">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="d623e-153">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="d623e-154">著色器模型</span><span class="sxs-lookup"><span data-stu-id="d623e-154">Shader Model</span></span>                                              | <span data-ttu-id="d623e-155">支援</span><span class="sxs-lookup"><span data-stu-id="d623e-155">Supported</span></span>                |
|-----------------------------------------------------------|--------------------------|
| [<span data-ttu-id="d623e-156">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="d623e-156">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="d623e-157">是 (只) 圖元著色器</span><span class="sxs-lookup"><span data-stu-id="d623e-157">yes (pixel shader only)</span></span>  |
| [<span data-ttu-id="d623e-158">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="d623e-158">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="d623e-159">是 (只) 圖元著色器</span><span class="sxs-lookup"><span data-stu-id="d623e-159">yes  (pixel shader only)</span></span> |
| [<span data-ttu-id="d623e-160">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="d623e-160">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="d623e-161">是 (只) 圖元著色器</span><span class="sxs-lookup"><span data-stu-id="d623e-161">yes  (pixel shader only)</span></span> |
| [<span data-ttu-id="d623e-162">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="d623e-162">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="d623e-163">不可以</span><span class="sxs-lookup"><span data-stu-id="d623e-163">no</span></span>                       |



 

1.  <span data-ttu-id="d623e-164">大量的程式碼重新排列是為了將漸層計算移至流程式控制制之外。</span><span class="sxs-lookup"><span data-stu-id="d623e-164">Significant code reordering is done to move gradient computations outside of flow control.</span></span>
2.  <span data-ttu-id="d623e-165">如果 D3DPSHADERCAPS2 \_ 0 cap 設定了 D3DD3DPSHADERCAPS2 \_ 0 \_ GRADIENTINSTRUCTIONS，則編譯器會將此函式對應至 texldd。</span><span class="sxs-lookup"><span data-stu-id="d623e-165">If the D3DPSHADERCAPS2\_0 cap is set with D3DD3DPSHADERCAPS2\_0\_GRADIENTINSTRUCTIONS, the compiler maps this function to texldd.</span></span>

## <a name="see-also"></a><span data-ttu-id="d623e-166">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d623e-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d623e-167">**(DirectX HLSL) 內建函式**</span><span class="sxs-lookup"><span data-stu-id="d623e-167">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

