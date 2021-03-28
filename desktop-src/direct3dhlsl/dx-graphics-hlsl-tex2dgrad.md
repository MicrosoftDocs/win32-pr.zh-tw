---
title: tex2Dgrad
description: 使用漸層來選取 mip 層級，以取樣2D 材質。 |tex2Dgrad
ms.assetid: a9ab7972-3480-4b37-aa10-c5cf811bdd0e
keywords:
- tex2Dgrad HLSL
topic_type:
- apiref
api_name:
- tex2Dgrad
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 74b20f1cf1f6f5d3b2873f4546dd57ef73b23dbb
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104973932"
---
# <a name="tex2dgrad"></a><span data-ttu-id="abed0-105">tex2Dgrad</span><span class="sxs-lookup"><span data-stu-id="abed0-105">tex2Dgrad</span></span>

<span data-ttu-id="abed0-106">使用漸層來選取 mip 層級，以取樣2D 材質。</span><span class="sxs-lookup"><span data-stu-id="abed0-106">Samples a 2D texture using a gradient to select the mip level.</span></span>



| <span data-ttu-id="abed0-107">ret tex2Dgrad (s、t、ddx、ddy) </span><span class="sxs-lookup"><span data-stu-id="abed0-107">ret tex2Dgrad(s, t, ddx, ddy)</span></span> |
|-------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="abed0-108">參數</span><span class="sxs-lookup"><span data-stu-id="abed0-108">Parameters</span></span>



| <span data-ttu-id="abed0-109">項目</span><span class="sxs-lookup"><span data-stu-id="abed0-109">Item</span></span>                                                         | <span data-ttu-id="abed0-110">描述</span><span class="sxs-lookup"><span data-stu-id="abed0-110">Description</span></span>                                                                  |
|--------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="abed0-111"><span id="s"></span><span id="S"></span>*！*</span><span class="sxs-lookup"><span data-stu-id="abed0-111"><span id="s"></span><span id="S"></span>*s*</span></span><br/>       | <span data-ttu-id="abed0-112">\[在 \] 取樣器狀態中。</span><span class="sxs-lookup"><span data-stu-id="abed0-112">\[in\] The sampler state.</span></span><br/>                                         |
| <span data-ttu-id="abed0-113"><span id="t"></span><span id="T"></span>*10gbase-t*</span><span class="sxs-lookup"><span data-stu-id="abed0-113"><span id="t"></span><span id="T"></span>*t*</span></span><br/>       | <span data-ttu-id="abed0-114">\[在 \] 紋理座標中。</span><span class="sxs-lookup"><span data-stu-id="abed0-114">\[in\] The texture coordinates.</span></span><br/>                                   |
| <span data-ttu-id="abed0-115"><span id="ddx"></span><span id="DDX"></span>*ddx*</span><span class="sxs-lookup"><span data-stu-id="abed0-115"><span id="ddx"></span><span id="DDX"></span>*ddx*</span></span><br/> | <span data-ttu-id="abed0-116">\[以 \] x 方向變更 surface 幾何的速率。</span><span class="sxs-lookup"><span data-stu-id="abed0-116">\[in\] Rate of change of the surface geometry in the x direction.</span></span><br/> |
| <span data-ttu-id="abed0-117"><span id="ddy"></span><span id="DDY"></span>*ddy*</span><span class="sxs-lookup"><span data-stu-id="abed0-117"><span id="ddy"></span><span id="DDY"></span>*ddy*</span></span><br/> | <span data-ttu-id="abed0-118">\[以 \] y 方向變更 surface 幾何的速率。</span><span class="sxs-lookup"><span data-stu-id="abed0-118">\[in\] Rate of change of the surface geometry in the y direction.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="abed0-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="abed0-119">Return Value</span></span>

<span data-ttu-id="abed0-120">材質資料的值。</span><span class="sxs-lookup"><span data-stu-id="abed0-120">The value of the texture data.</span></span>

## <a name="type-description"></a><span data-ttu-id="abed0-121">類型描述</span><span class="sxs-lookup"><span data-stu-id="abed0-121">Type Description</span></span>



| <span data-ttu-id="abed0-122">Name</span><span class="sxs-lookup"><span data-stu-id="abed0-122">Name</span></span> | <span data-ttu-id="abed0-123">輸入/輸出</span><span class="sxs-lookup"><span data-stu-id="abed0-123">In/Out</span></span> | [<span data-ttu-id="abed0-124">**範本類型**</span><span class="sxs-lookup"><span data-stu-id="abed0-124">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="abed0-125">**元件類型**</span><span class="sxs-lookup"><span data-stu-id="abed0-125">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="abed0-126">大小</span><span class="sxs-lookup"><span data-stu-id="abed0-126">Size</span></span> |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="abed0-127">s</span><span class="sxs-lookup"><span data-stu-id="abed0-127">s</span></span>    | <span data-ttu-id="abed0-128">in</span><span class="sxs-lookup"><span data-stu-id="abed0-128">in</span></span>     | [<span data-ttu-id="abed0-129">**物件**</span><span class="sxs-lookup"><span data-stu-id="abed0-129">**object**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="abed0-130">sampler2D</span><span class="sxs-lookup"><span data-stu-id="abed0-130">sampler2D</span></span>](dx-graphics-hlsl-sampler.md)                      | <span data-ttu-id="abed0-131">1</span><span class="sxs-lookup"><span data-stu-id="abed0-131">1</span></span>    |
| <span data-ttu-id="abed0-132">t</span><span class="sxs-lookup"><span data-stu-id="abed0-132">t</span></span>    | <span data-ttu-id="abed0-133">in</span><span class="sxs-lookup"><span data-stu-id="abed0-133">in</span></span>     | [<span data-ttu-id="abed0-134">**向量**</span><span class="sxs-lookup"><span data-stu-id="abed0-134">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="abed0-135">**浮動**</span><span class="sxs-lookup"><span data-stu-id="abed0-135">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="abed0-136">2</span><span class="sxs-lookup"><span data-stu-id="abed0-136">2</span></span>    |
| <span data-ttu-id="abed0-137">ddx</span><span class="sxs-lookup"><span data-stu-id="abed0-137">ddx</span></span>  | <span data-ttu-id="abed0-138">in</span><span class="sxs-lookup"><span data-stu-id="abed0-138">in</span></span>     | [<span data-ttu-id="abed0-139">**向量**</span><span class="sxs-lookup"><span data-stu-id="abed0-139">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="abed0-140">**浮動**</span><span class="sxs-lookup"><span data-stu-id="abed0-140">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="abed0-141">2</span><span class="sxs-lookup"><span data-stu-id="abed0-141">2</span></span>    |
| <span data-ttu-id="abed0-142">ddy</span><span class="sxs-lookup"><span data-stu-id="abed0-142">ddy</span></span>  | <span data-ttu-id="abed0-143">in</span><span class="sxs-lookup"><span data-stu-id="abed0-143">in</span></span>     | [<span data-ttu-id="abed0-144">**向量**</span><span class="sxs-lookup"><span data-stu-id="abed0-144">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="abed0-145">**浮動**</span><span class="sxs-lookup"><span data-stu-id="abed0-145">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="abed0-146">2</span><span class="sxs-lookup"><span data-stu-id="abed0-146">2</span></span>    |
| <span data-ttu-id="abed0-147">Ret</span><span class="sxs-lookup"><span data-stu-id="abed0-147">ret</span></span>  | <span data-ttu-id="abed0-148">out</span><span class="sxs-lookup"><span data-stu-id="abed0-148">out</span></span>    | [<span data-ttu-id="abed0-149">**向量**</span><span class="sxs-lookup"><span data-stu-id="abed0-149">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="abed0-150">**浮動**</span><span class="sxs-lookup"><span data-stu-id="abed0-150">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="abed0-151">4</span><span class="sxs-lookup"><span data-stu-id="abed0-151">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="abed0-152">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="abed0-152">Minimum Shader Model</span></span>

<span data-ttu-id="abed0-153">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="abed0-153">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="abed0-154">著色器模型</span><span class="sxs-lookup"><span data-stu-id="abed0-154">Shader Model</span></span>                                              | <span data-ttu-id="abed0-155">支援</span><span class="sxs-lookup"><span data-stu-id="abed0-155">Supported</span></span>                |
|-----------------------------------------------------------|--------------------------|
| [<span data-ttu-id="abed0-156">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="abed0-156">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="abed0-157">是 (只) 圖元著色器</span><span class="sxs-lookup"><span data-stu-id="abed0-157">yes (pixel shader only)</span></span>  |
| [<span data-ttu-id="abed0-158">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="abed0-158">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="abed0-159">是 (只) 圖元著色器</span><span class="sxs-lookup"><span data-stu-id="abed0-159">yes  (pixel shader only)</span></span> |
| [<span data-ttu-id="abed0-160">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="abed0-160">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="abed0-161">是 (只) 圖元著色器</span><span class="sxs-lookup"><span data-stu-id="abed0-161">yes  (pixel shader only)</span></span> |
| [<span data-ttu-id="abed0-162">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="abed0-162">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="abed0-163">不可以</span><span class="sxs-lookup"><span data-stu-id="abed0-163">no</span></span>                       |



 

1.  <span data-ttu-id="abed0-164">大量的程式碼重新排列是為了將漸層計算移至流程式控制制之外。</span><span class="sxs-lookup"><span data-stu-id="abed0-164">Significant code reordering is done to move gradient computations outside of flow control.</span></span>
2.  <span data-ttu-id="abed0-165">如果 D3DPSHADERCAPS2 \_ 0 cap 設定了 D3DD3DPSHADERCAPS2 \_ 0 \_ GRADIENTINSTRUCTIONS，則編譯器會將此函式對應至 texldd。</span><span class="sxs-lookup"><span data-stu-id="abed0-165">If the D3DPSHADERCAPS2\_0 cap is set with D3DD3DPSHADERCAPS2\_0\_GRADIENTINSTRUCTIONS, the compiler maps this function to texldd.</span></span>

## <a name="remarks"></a><span data-ttu-id="abed0-166">備註</span><span class="sxs-lookup"><span data-stu-id="abed0-166">Remarks</span></span>

<span data-ttu-id="abed0-167">當流程式控制件存在於著色器中時，在指定分支路徑內要求的漸層計算結果，在連續的圖元可能會中斷個別的流程式控制制路徑時則不明確。</span><span class="sxs-lookup"><span data-stu-id="abed0-167">When flow control is present in a shader, the result of a gradient calculation requested inside a given branch path is ambiguous when adjacent pixels may go down separate flow control paths.</span></span> <span data-ttu-id="abed0-168">因此，使用任何圖元著色器作業時，可能會要求漸層計算發生在流程式控制制結構內的位置，而該位置可能會因圖元而異，而對指定的基本類型進行了點陣化。</span><span class="sxs-lookup"><span data-stu-id="abed0-168">Therefore, it is deemed illegal to use any pixel shader operation that requests a gradient calculation to occur at a location that is inside a flow control construct which could vary across pixels for a given primitive being rasterized.</span></span> <span data-ttu-id="abed0-169">如果 **if** 語句的任一端與 branch 屬性使用漸層函式，可能會產生編譯器錯誤。</span><span class="sxs-lookup"><span data-stu-id="abed0-169">If either side of an **if** statement with the branch attribute uses a gradient function a compiler error may be generated.</span></span> <span data-ttu-id="abed0-170">請參閱 [ (DIRECTX HLSL) 的 If 語句 ](dx-graphics-hlsl-if.md)。</span><span class="sxs-lookup"><span data-stu-id="abed0-170">See [if Statement (DirectX HLSL)](dx-graphics-hlsl-if.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="abed0-171">另請參閱</span><span class="sxs-lookup"><span data-stu-id="abed0-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="abed0-172">**(DirectX HLSL) 內建函式**</span><span class="sxs-lookup"><span data-stu-id="abed0-172">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

