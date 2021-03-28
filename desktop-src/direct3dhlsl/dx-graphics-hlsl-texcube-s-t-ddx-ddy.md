---
title: texCUBE (HLSL 參考) -選取 mip 層級
description: '使用漸層來選取 mip 層級，以取樣 cube 紋理。 |texCUBE (HLSL 參考) '
ms.assetid: 5615f48b-eb0a-4de7-a441-51ec3cecf6fd
keywords:
- texCUBE HLSL
topic_type:
- apiref
api_name:
- texCUBE
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6286b4fedb94b9fd5c84c76171e9478f06e16ce4
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/16/2021
ms.locfileid: "104974739"
---
# <a name="texcube-hlsl-reference---select-the-mip-level"></a><span data-ttu-id="5d7d3-105">texCUBE (HLSL 參考) -選取 mip 層級</span><span class="sxs-lookup"><span data-stu-id="5d7d3-105">texCUBE (HLSL reference) - Select the mip level</span></span>

<span data-ttu-id="5d7d3-106">使用漸層來選取 mip 層級，以取樣 cube 紋理。</span><span class="sxs-lookup"><span data-stu-id="5d7d3-106">Samples a cube texture using a gradient to select the mip level.</span></span>



| <span data-ttu-id="5d7d3-107">ret texCUBE (s、t、ddx、ddy) </span><span class="sxs-lookup"><span data-stu-id="5d7d3-107">ret texCUBE(s, t, ddx, ddy)</span></span> |
|-----------------------------|



 

## <a name="parameters"></a><span data-ttu-id="5d7d3-108">參數</span><span class="sxs-lookup"><span data-stu-id="5d7d3-108">Parameters</span></span>



| <span data-ttu-id="5d7d3-109">項目</span><span class="sxs-lookup"><span data-stu-id="5d7d3-109">Item</span></span>                                                         | <span data-ttu-id="5d7d3-110">描述</span><span class="sxs-lookup"><span data-stu-id="5d7d3-110">Description</span></span>                                                                  |
|--------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="5d7d3-111"><span id="s"></span><span id="S"></span>*！*</span><span class="sxs-lookup"><span data-stu-id="5d7d3-111"><span id="s"></span><span id="S"></span>*s*</span></span><br/>       | <span data-ttu-id="5d7d3-112">\[在 \] 取樣器狀態中。</span><span class="sxs-lookup"><span data-stu-id="5d7d3-112">\[in\] The sampler state.</span></span><br/>                                         |
| <span data-ttu-id="5d7d3-113"><span id="t"></span><span id="T"></span>*10gbase-t*</span><span class="sxs-lookup"><span data-stu-id="5d7d3-113"><span id="t"></span><span id="T"></span>*t*</span></span><br/>       | <span data-ttu-id="5d7d3-114">\[在 \] 紋理座標中。</span><span class="sxs-lookup"><span data-stu-id="5d7d3-114">\[in\] The texture coordinate.</span></span><br/>                                    |
| <span data-ttu-id="5d7d3-115"><span id="ddx"></span><span id="DDX"></span>*ddx*</span><span class="sxs-lookup"><span data-stu-id="5d7d3-115"><span id="ddx"></span><span id="DDX"></span>*ddx*</span></span><br/> | <span data-ttu-id="5d7d3-116">\[以 \] x 方向變更 surface 幾何的速率。</span><span class="sxs-lookup"><span data-stu-id="5d7d3-116">\[in\] Rate of change of the surface geometry in the x direction.</span></span><br/> |
| <span data-ttu-id="5d7d3-117"><span id="ddy"></span><span id="DDY"></span>*ddy*</span><span class="sxs-lookup"><span data-stu-id="5d7d3-117"><span id="ddy"></span><span id="DDY"></span>*ddy*</span></span><br/> | <span data-ttu-id="5d7d3-118">\[以 \] y 方向變更 surface 幾何的速率。</span><span class="sxs-lookup"><span data-stu-id="5d7d3-118">\[in\] Rate of change of the surface geometry in the y direction.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="5d7d3-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="5d7d3-119">Return Value</span></span>

<span data-ttu-id="5d7d3-120">材質資料的值。</span><span class="sxs-lookup"><span data-stu-id="5d7d3-120">The value of the texture data.</span></span>

## <a name="type-description"></a><span data-ttu-id="5d7d3-121">類型描述</span><span class="sxs-lookup"><span data-stu-id="5d7d3-121">Type Description</span></span>



| <span data-ttu-id="5d7d3-122">Name</span><span class="sxs-lookup"><span data-stu-id="5d7d3-122">Name</span></span> | <span data-ttu-id="5d7d3-123">輸入/輸出</span><span class="sxs-lookup"><span data-stu-id="5d7d3-123">In/Out</span></span> | [<span data-ttu-id="5d7d3-124">**範本類型**</span><span class="sxs-lookup"><span data-stu-id="5d7d3-124">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="5d7d3-125">**元件類型**</span><span class="sxs-lookup"><span data-stu-id="5d7d3-125">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="5d7d3-126">大小</span><span class="sxs-lookup"><span data-stu-id="5d7d3-126">Size</span></span> |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="5d7d3-127">s</span><span class="sxs-lookup"><span data-stu-id="5d7d3-127">s</span></span>    | <span data-ttu-id="5d7d3-128">in</span><span class="sxs-lookup"><span data-stu-id="5d7d3-128">in</span></span>     | [<span data-ttu-id="5d7d3-129">**物件**</span><span class="sxs-lookup"><span data-stu-id="5d7d3-129">**object**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="5d7d3-130">samplerCUBE</span><span class="sxs-lookup"><span data-stu-id="5d7d3-130">samplerCUBE</span></span>](dx-graphics-hlsl-sampler.md)                    | <span data-ttu-id="5d7d3-131">1</span><span class="sxs-lookup"><span data-stu-id="5d7d3-131">1</span></span>    |
| <span data-ttu-id="5d7d3-132">t</span><span class="sxs-lookup"><span data-stu-id="5d7d3-132">t</span></span>    | <span data-ttu-id="5d7d3-133">in</span><span class="sxs-lookup"><span data-stu-id="5d7d3-133">in</span></span>     | [<span data-ttu-id="5d7d3-134">**向量**</span><span class="sxs-lookup"><span data-stu-id="5d7d3-134">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="5d7d3-135">**浮動**</span><span class="sxs-lookup"><span data-stu-id="5d7d3-135">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="5d7d3-136">3</span><span class="sxs-lookup"><span data-stu-id="5d7d3-136">3</span></span>    |
| <span data-ttu-id="5d7d3-137">ddx</span><span class="sxs-lookup"><span data-stu-id="5d7d3-137">ddx</span></span>  | <span data-ttu-id="5d7d3-138">in</span><span class="sxs-lookup"><span data-stu-id="5d7d3-138">in</span></span>     | [<span data-ttu-id="5d7d3-139">**向量**</span><span class="sxs-lookup"><span data-stu-id="5d7d3-139">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="5d7d3-140">**浮動**</span><span class="sxs-lookup"><span data-stu-id="5d7d3-140">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="5d7d3-141">3</span><span class="sxs-lookup"><span data-stu-id="5d7d3-141">3</span></span>    |
| <span data-ttu-id="5d7d3-142">ddy</span><span class="sxs-lookup"><span data-stu-id="5d7d3-142">ddy</span></span>  | <span data-ttu-id="5d7d3-143">in</span><span class="sxs-lookup"><span data-stu-id="5d7d3-143">in</span></span>     | [<span data-ttu-id="5d7d3-144">**向量**</span><span class="sxs-lookup"><span data-stu-id="5d7d3-144">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="5d7d3-145">**浮動**</span><span class="sxs-lookup"><span data-stu-id="5d7d3-145">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="5d7d3-146">3</span><span class="sxs-lookup"><span data-stu-id="5d7d3-146">3</span></span>    |
| <span data-ttu-id="5d7d3-147">Ret</span><span class="sxs-lookup"><span data-stu-id="5d7d3-147">ret</span></span>  | <span data-ttu-id="5d7d3-148">out</span><span class="sxs-lookup"><span data-stu-id="5d7d3-148">out</span></span>    | [<span data-ttu-id="5d7d3-149">**向量**</span><span class="sxs-lookup"><span data-stu-id="5d7d3-149">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="5d7d3-150">**浮動**</span><span class="sxs-lookup"><span data-stu-id="5d7d3-150">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="5d7d3-151">4</span><span class="sxs-lookup"><span data-stu-id="5d7d3-151">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="5d7d3-152">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="5d7d3-152">Minimum Shader Model</span></span>

<span data-ttu-id="5d7d3-153">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="5d7d3-153">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="5d7d3-154">著色器模型</span><span class="sxs-lookup"><span data-stu-id="5d7d3-154">Shader Model</span></span>                                              | <span data-ttu-id="5d7d3-155">支援</span><span class="sxs-lookup"><span data-stu-id="5d7d3-155">Supported</span></span>                |
|-----------------------------------------------------------|--------------------------|
| [<span data-ttu-id="5d7d3-156">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="5d7d3-156">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="5d7d3-157">是 (只) 圖元著色器</span><span class="sxs-lookup"><span data-stu-id="5d7d3-157">yes (pixel shader only)</span></span>  |
| [<span data-ttu-id="5d7d3-158">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="5d7d3-158">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="5d7d3-159">是 (只) 圖元著色器</span><span class="sxs-lookup"><span data-stu-id="5d7d3-159">yes  (pixel shader only)</span></span> |
| [<span data-ttu-id="5d7d3-160">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="5d7d3-160">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="5d7d3-161">是 (只) 圖元著色器</span><span class="sxs-lookup"><span data-stu-id="5d7d3-161">yes  (pixel shader only)</span></span> |
| [<span data-ttu-id="5d7d3-162">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="5d7d3-162">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="5d7d3-163">不可以</span><span class="sxs-lookup"><span data-stu-id="5d7d3-163">no</span></span>                       |



 

1.  <span data-ttu-id="5d7d3-164">大量的程式碼重新排列是為了將漸層計算移至流程式控制制之外。</span><span class="sxs-lookup"><span data-stu-id="5d7d3-164">Significant code reordering is done to move gradient computations outside of flow control.</span></span>
2.  <span data-ttu-id="5d7d3-165">如果 D3DPSHADERCAPS2 \_ 0 cap 設定了 D3DD3DPSHADERCAPS2 \_ 0 \_ GRADIENTINSTRUCTIONS，則編譯器會將此函式對應至 texldd。</span><span class="sxs-lookup"><span data-stu-id="5d7d3-165">If the D3DPSHADERCAPS2\_0 cap is set with D3DD3DPSHADERCAPS2\_0\_GRADIENTINSTRUCTIONS, the compiler maps this function to texldd.</span></span>

## <a name="see-also"></a><span data-ttu-id="5d7d3-166">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5d7d3-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d7d3-167">**(DirectX HLSL) 內建函式**</span><span class="sxs-lookup"><span data-stu-id="5d7d3-167">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

