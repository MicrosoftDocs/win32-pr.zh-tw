---
title: tex2Dlod
description: 使用 mipmap 取樣2D 材質。 Mipmap」 LOD 是在 t.w. 中指定的
ms.assetid: 689eff39-f6ac-4c25-8b92-ca68707ae8ad
keywords:
- tex2Dlod HLSL
topic_type:
- apiref
api_name:
- tex2Dlod
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f63a922fe86dc10d984369a1a872f84089b4db34
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104971696"
---
# <a name="tex2dlod"></a><span data-ttu-id="3298e-105">tex2Dlod</span><span class="sxs-lookup"><span data-stu-id="3298e-105">tex2Dlod</span></span>

<span data-ttu-id="3298e-106">使用 mipmap 取樣2D 材質。</span><span class="sxs-lookup"><span data-stu-id="3298e-106">Samples a 2D texture with mipmaps.</span></span> <span data-ttu-id="3298e-107">Mipmap」 LOD 是在 t.w. 中指定的</span><span class="sxs-lookup"><span data-stu-id="3298e-107">The mipmap LOD is specified in t.w.</span></span>



| <span data-ttu-id="3298e-108">ret tex2Dlod (s，t) </span><span class="sxs-lookup"><span data-stu-id="3298e-108">ret tex2Dlod(s, t)</span></span> |
|--------------------|



 

## <a name="parameters"></a><span data-ttu-id="3298e-109">參數</span><span class="sxs-lookup"><span data-stu-id="3298e-109">Parameters</span></span>



| <span data-ttu-id="3298e-110">項目</span><span class="sxs-lookup"><span data-stu-id="3298e-110">Item</span></span>                                                   | <span data-ttu-id="3298e-111">描述</span><span class="sxs-lookup"><span data-stu-id="3298e-111">Description</span></span>                               |
|--------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="3298e-112"><span id="s"></span><span id="S"></span>*！*</span><span class="sxs-lookup"><span data-stu-id="3298e-112"><span id="s"></span><span id="S"></span>*s*</span></span><br/> | <span data-ttu-id="3298e-113">\[在 \] 取樣器狀態中。</span><span class="sxs-lookup"><span data-stu-id="3298e-113">\[in\] The sampler state.</span></span><br/>      |
| <span data-ttu-id="3298e-114"><span id="t"></span><span id="T"></span>*10gbase-t*</span><span class="sxs-lookup"><span data-stu-id="3298e-114"><span id="t"></span><span id="T"></span>*t*</span></span><br/> | <span data-ttu-id="3298e-115">\[在 \] 紋理座標中。</span><span class="sxs-lookup"><span data-stu-id="3298e-115">\[in\] The texture coordinate.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="3298e-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="3298e-116">Return Value</span></span>

<span data-ttu-id="3298e-117">材質資料的值。</span><span class="sxs-lookup"><span data-stu-id="3298e-117">The value of the texture data.</span></span>

## <a name="type-description"></a><span data-ttu-id="3298e-118">類型描述</span><span class="sxs-lookup"><span data-stu-id="3298e-118">Type Description</span></span>



| <span data-ttu-id="3298e-119">Name</span><span class="sxs-lookup"><span data-stu-id="3298e-119">Name</span></span> | <span data-ttu-id="3298e-120">輸入/輸出</span><span class="sxs-lookup"><span data-stu-id="3298e-120">In/Out</span></span> | [<span data-ttu-id="3298e-121">**範本類型**</span><span class="sxs-lookup"><span data-stu-id="3298e-121">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="3298e-122">**元件類型**</span><span class="sxs-lookup"><span data-stu-id="3298e-122">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="3298e-123">大小</span><span class="sxs-lookup"><span data-stu-id="3298e-123">Size</span></span> |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="3298e-124">s</span><span class="sxs-lookup"><span data-stu-id="3298e-124">s</span></span>    | <span data-ttu-id="3298e-125">in</span><span class="sxs-lookup"><span data-stu-id="3298e-125">in</span></span>     | [<span data-ttu-id="3298e-126">**物件**</span><span class="sxs-lookup"><span data-stu-id="3298e-126">**object**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="3298e-127">sampler2D</span><span class="sxs-lookup"><span data-stu-id="3298e-127">sampler2D</span></span>](dx-graphics-hlsl-sampler.md)                      | <span data-ttu-id="3298e-128">1</span><span class="sxs-lookup"><span data-stu-id="3298e-128">1</span></span>    |
| <span data-ttu-id="3298e-129">t</span><span class="sxs-lookup"><span data-stu-id="3298e-129">t</span></span>    | <span data-ttu-id="3298e-130">in</span><span class="sxs-lookup"><span data-stu-id="3298e-130">in</span></span>     | [<span data-ttu-id="3298e-131">**向量**</span><span class="sxs-lookup"><span data-stu-id="3298e-131">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="3298e-132">**浮動**</span><span class="sxs-lookup"><span data-stu-id="3298e-132">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="3298e-133">4</span><span class="sxs-lookup"><span data-stu-id="3298e-133">4</span></span>    |
| <span data-ttu-id="3298e-134">Ret</span><span class="sxs-lookup"><span data-stu-id="3298e-134">ret</span></span>  | <span data-ttu-id="3298e-135">out</span><span class="sxs-lookup"><span data-stu-id="3298e-135">out</span></span>    | [<span data-ttu-id="3298e-136">**向量**</span><span class="sxs-lookup"><span data-stu-id="3298e-136">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="3298e-137">**浮動**</span><span class="sxs-lookup"><span data-stu-id="3298e-137">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="3298e-138">4</span><span class="sxs-lookup"><span data-stu-id="3298e-138">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="3298e-139">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="3298e-139">Minimum Shader Model</span></span>

<span data-ttu-id="3298e-140">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="3298e-140">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="3298e-141">著色器模型</span><span class="sxs-lookup"><span data-stu-id="3298e-141">Shader Model</span></span>                                                                       | <span data-ttu-id="3298e-142">支援</span><span class="sxs-lookup"><span data-stu-id="3298e-142">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="3298e-143">[著色器模型 3 (DIRECTX HLSL) ](dx-graphics-hlsl-sm3.md) 和更高的著色器模型</span><span class="sxs-lookup"><span data-stu-id="3298e-143">[Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) and higher shader models</span></span> | <span data-ttu-id="3298e-144">是</span><span class="sxs-lookup"><span data-stu-id="3298e-144">yes</span></span>       |
| [<span data-ttu-id="3298e-145">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="3298e-145">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md)                          | <span data-ttu-id="3298e-146">不可以</span><span class="sxs-lookup"><span data-stu-id="3298e-146">no</span></span>        |
| [<span data-ttu-id="3298e-147">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="3298e-147">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="3298e-148">不可以</span><span class="sxs-lookup"><span data-stu-id="3298e-148">no</span></span>        |



 

## <a name="remarks"></a><span data-ttu-id="3298e-149">備註</span><span class="sxs-lookup"><span data-stu-id="3298e-149">Remarks</span></span>

<span data-ttu-id="3298e-150">從 Direct3D 10 開始，您可以使用新的 HLSL 語法來存取材質和其他資源。</span><span class="sxs-lookup"><span data-stu-id="3298e-150">Starting with Direct3D 10, you can use new HLSL syntax to access textures and other resources.</span></span> <span data-ttu-id="3298e-151">您可以使用更多物件導向的樣式來取代內建樣式的紋理查閱函數（例如 **tex2Dlod**）。</span><span class="sxs-lookup"><span data-stu-id="3298e-151">You can replace intrinsic-style texture lookup functions, such as **tex2Dlod**, with a more object-oriented style.</span></span> <span data-ttu-id="3298e-152">在此物件導向的樣式中，紋理會與取樣器分離，並具有載入和取樣的方法。</span><span class="sxs-lookup"><span data-stu-id="3298e-152">In this object-oriented style, textures are decoupled from samplers and have methods for loading and sampling.</span></span>

<span data-ttu-id="3298e-153">若要取樣2D 材質，請不要使用 **tex2Dlod** ，如下列程式碼所示：</span><span class="sxs-lookup"><span data-stu-id="3298e-153">To sample a 2D texture, instead of using **tex2Dlod** as in this code:</span></span>


```
sampler S;
...
color = tex2Dlod(S, Location);
```



<span data-ttu-id="3298e-154">使用 [**紋理物件**](dx-graphics-hlsl-to-type.md)的 [SampleLevel](dx-graphics-hlsl-to-samplelevel.md)方法，如下列程式碼所示：</span><span class="sxs-lookup"><span data-stu-id="3298e-154">Use the [SampleLevel](dx-graphics-hlsl-to-samplelevel.md) method of a [**Texture Object**](dx-graphics-hlsl-to-type.md) as in this code:</span></span>


```
Texture2D MyTexture;
SamplerState MySampler;
...
color = MyTexture.SampleLevel(MySampler, Location, LOD);
```



<span data-ttu-id="3298e-155">若要使用內建樣式的材質查閱函數（例如 **tex2Dlod**），並搭配 [著色器模型 4](dx-graphics-hlsl-sm4.md) 和更高版本，請使用 [**D3DCOMPILE \_ 讓回溯 \_ \_ 相容性**](d3dcompile-constants.md) 進行編譯。</span><span class="sxs-lookup"><span data-stu-id="3298e-155">To use the intrinsic-style texture lookup functions, such as **tex2Dlod**, with [shader model 4](dx-graphics-hlsl-sm4.md) and higher, use [**D3DCOMPILE\_ENABLE\_BACKWARDS\_COMPATIBILITY**](d3dcompile-constants.md) to compile.</span></span> <span data-ttu-id="3298e-156">但是，如果您想要以著色器模型4和更高版本為目標 (甚至是[ \* \_ 4 \_ 0 \_ 層級 \_ 9 \_ \* ](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro)) 具有較新的物件導向樣式程式碼，請遷移至較新的 HLSL 語法。</span><span class="sxs-lookup"><span data-stu-id="3298e-156">However, if you want to target shader model 4 and higher (even [\*\_4\_0\_level\_9\_\*](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro)) with newer object-oriented style code, migrate to the newer HLSL syntax.</span></span>

## <a name="see-also"></a><span data-ttu-id="3298e-157">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3298e-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3298e-158">**(DirectX HLSL) 內建函式**</span><span class="sxs-lookup"><span data-stu-id="3298e-158">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

