---
title: tex3Dlod
description: 使用 mipmap 來取樣3D 紋理。 Mipmap」 LOD 是在 t.w. 中指定的
ms.assetid: 9bdd8fa1-8c02-4765-8f4d-61ceb532354e
keywords:
- tex3Dlod HLSL
topic_type:
- apiref
api_name:
- tex3Dlod
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bc25af449f7f32e94d4ca344bf5ef3a4d09b376c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104971705"
---
# <a name="tex3dlod"></a><span data-ttu-id="112ea-105">tex3Dlod</span><span class="sxs-lookup"><span data-stu-id="112ea-105">tex3Dlod</span></span>

<span data-ttu-id="112ea-106">使用 mipmap 來取樣3D 紋理。</span><span class="sxs-lookup"><span data-stu-id="112ea-106">Samples a 3D texture with mipmaps.</span></span> <span data-ttu-id="112ea-107">Mipmap」 LOD 是在 t.w. 中指定的</span><span class="sxs-lookup"><span data-stu-id="112ea-107">The mipmap LOD is specified in t.w.</span></span>



| <span data-ttu-id="112ea-108">ret tex3Dlod (s，t) </span><span class="sxs-lookup"><span data-stu-id="112ea-108">ret tex3Dlod(s, t)</span></span> |
|--------------------|



 

## <a name="parameters"></a><span data-ttu-id="112ea-109">參數</span><span class="sxs-lookup"><span data-stu-id="112ea-109">Parameters</span></span>



| <span data-ttu-id="112ea-110">項目</span><span class="sxs-lookup"><span data-stu-id="112ea-110">Item</span></span>                                                   | <span data-ttu-id="112ea-111">描述</span><span class="sxs-lookup"><span data-stu-id="112ea-111">Description</span></span>                               |
|--------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="112ea-112"><span id="s"></span><span id="S"></span>*！*</span><span class="sxs-lookup"><span data-stu-id="112ea-112"><span id="s"></span><span id="S"></span>*s*</span></span><br/> | <span data-ttu-id="112ea-113">\[在 \] 取樣器狀態中。</span><span class="sxs-lookup"><span data-stu-id="112ea-113">\[in\] The sampler state.</span></span><br/>      |
| <span data-ttu-id="112ea-114"><span id="t"></span><span id="T"></span>*10gbase-t*</span><span class="sxs-lookup"><span data-stu-id="112ea-114"><span id="t"></span><span id="T"></span>*t*</span></span><br/> | <span data-ttu-id="112ea-115">\[在 \] 紋理座標中。</span><span class="sxs-lookup"><span data-stu-id="112ea-115">\[in\] The texture coordinate.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="112ea-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="112ea-116">Return Value</span></span>

<span data-ttu-id="112ea-117">材質資料的值。</span><span class="sxs-lookup"><span data-stu-id="112ea-117">The value of the texture data.</span></span>

## <a name="type-description"></a><span data-ttu-id="112ea-118">類型描述</span><span class="sxs-lookup"><span data-stu-id="112ea-118">Type Description</span></span>



| <span data-ttu-id="112ea-119">Name</span><span class="sxs-lookup"><span data-stu-id="112ea-119">Name</span></span> | <span data-ttu-id="112ea-120">輸入/輸出</span><span class="sxs-lookup"><span data-stu-id="112ea-120">In/Out</span></span> | [<span data-ttu-id="112ea-121">**範本類型**</span><span class="sxs-lookup"><span data-stu-id="112ea-121">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="112ea-122">**元件類型**</span><span class="sxs-lookup"><span data-stu-id="112ea-122">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="112ea-123">大小</span><span class="sxs-lookup"><span data-stu-id="112ea-123">Size</span></span> |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="112ea-124">s</span><span class="sxs-lookup"><span data-stu-id="112ea-124">s</span></span>    | <span data-ttu-id="112ea-125">in</span><span class="sxs-lookup"><span data-stu-id="112ea-125">in</span></span>     | [<span data-ttu-id="112ea-126">**物件**</span><span class="sxs-lookup"><span data-stu-id="112ea-126">**object**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="112ea-127">sampler3D</span><span class="sxs-lookup"><span data-stu-id="112ea-127">sampler3D</span></span>](dx-graphics-hlsl-sampler.md)                      | <span data-ttu-id="112ea-128">1</span><span class="sxs-lookup"><span data-stu-id="112ea-128">1</span></span>    |
| <span data-ttu-id="112ea-129">t</span><span class="sxs-lookup"><span data-stu-id="112ea-129">t</span></span>    | <span data-ttu-id="112ea-130">in</span><span class="sxs-lookup"><span data-stu-id="112ea-130">in</span></span>     | [<span data-ttu-id="112ea-131">**向量**</span><span class="sxs-lookup"><span data-stu-id="112ea-131">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="112ea-132">**浮動**</span><span class="sxs-lookup"><span data-stu-id="112ea-132">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="112ea-133">4</span><span class="sxs-lookup"><span data-stu-id="112ea-133">4</span></span>    |
| <span data-ttu-id="112ea-134">Ret</span><span class="sxs-lookup"><span data-stu-id="112ea-134">ret</span></span>  | <span data-ttu-id="112ea-135">out</span><span class="sxs-lookup"><span data-stu-id="112ea-135">out</span></span>    | [<span data-ttu-id="112ea-136">**向量**</span><span class="sxs-lookup"><span data-stu-id="112ea-136">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="112ea-137">**浮動**</span><span class="sxs-lookup"><span data-stu-id="112ea-137">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="112ea-138">4</span><span class="sxs-lookup"><span data-stu-id="112ea-138">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="112ea-139">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="112ea-139">Minimum Shader Model</span></span>

<span data-ttu-id="112ea-140">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="112ea-140">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="112ea-141">著色器模型</span><span class="sxs-lookup"><span data-stu-id="112ea-141">Shader Model</span></span>                                              | <span data-ttu-id="112ea-142">支援</span><span class="sxs-lookup"><span data-stu-id="112ea-142">Supported</span></span>               |
|-----------------------------------------------------------|-------------------------|
| [<span data-ttu-id="112ea-143">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="112ea-143">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="112ea-144">是 (只) 圖元著色器</span><span class="sxs-lookup"><span data-stu-id="112ea-144">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="112ea-145">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="112ea-145">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="112ea-146">是 (只) 圖元著色器</span><span class="sxs-lookup"><span data-stu-id="112ea-146">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="112ea-147">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="112ea-147">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="112ea-148">不可以</span><span class="sxs-lookup"><span data-stu-id="112ea-148">no</span></span>                      |
| [<span data-ttu-id="112ea-149">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="112ea-149">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="112ea-150">不可以</span><span class="sxs-lookup"><span data-stu-id="112ea-150">no</span></span>                      |



 

## <a name="see-also"></a><span data-ttu-id="112ea-151">另請參閱</span><span class="sxs-lookup"><span data-stu-id="112ea-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="112ea-152">**(DirectX HLSL) 內建函式**</span><span class="sxs-lookup"><span data-stu-id="112ea-152">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

