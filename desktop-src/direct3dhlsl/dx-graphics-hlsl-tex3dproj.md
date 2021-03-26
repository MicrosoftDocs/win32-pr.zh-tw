---
title: tex3Dproj
description: 使用 projective 除的3D 紋理範例;紋理座標會在進行查閱之前除以 t. w。
ms.assetid: c7062ef0-3169-4cbe-b47b-4efc80944963
keywords:
- tex3Dproj HLSL
topic_type:
- apiref
api_name:
- tex3Dproj
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 519477b7dba4f746dc1720a08c2ce581ab7b7205
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104508076"
---
# <a name="tex3dproj"></a><span data-ttu-id="eb25c-104">tex3Dproj</span><span class="sxs-lookup"><span data-stu-id="eb25c-104">tex3Dproj</span></span>

<span data-ttu-id="eb25c-105">使用 projective 除的3D 紋理範例;紋理座標會在進行查閱之前除以 t. w。</span><span class="sxs-lookup"><span data-stu-id="eb25c-105">Samples a 3D texture using a projective divide; the texture coordinate is divided by t.w before the lookup takes place.</span></span>



| <span data-ttu-id="eb25c-106">ret tex3Dproj (s，t) </span><span class="sxs-lookup"><span data-stu-id="eb25c-106">ret tex3Dproj(s, t)</span></span> |
|---------------------|



 

## <a name="parameters"></a><span data-ttu-id="eb25c-107">參數</span><span class="sxs-lookup"><span data-stu-id="eb25c-107">Parameters</span></span>



| <span data-ttu-id="eb25c-108">項目</span><span class="sxs-lookup"><span data-stu-id="eb25c-108">Item</span></span>                                                   | <span data-ttu-id="eb25c-109">描述</span><span class="sxs-lookup"><span data-stu-id="eb25c-109">Description</span></span>                               |
|--------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="eb25c-110"><span id="s"></span><span id="S"></span>*！*</span><span class="sxs-lookup"><span data-stu-id="eb25c-110"><span id="s"></span><span id="S"></span>*s*</span></span><br/> | <span data-ttu-id="eb25c-111">\[在 \] 取樣器狀態中。</span><span class="sxs-lookup"><span data-stu-id="eb25c-111">\[in\] The sampler state.</span></span><br/>      |
| <span data-ttu-id="eb25c-112"><span id="t"></span><span id="T"></span>*10gbase-t*</span><span class="sxs-lookup"><span data-stu-id="eb25c-112"><span id="t"></span><span id="T"></span>*t*</span></span><br/> | <span data-ttu-id="eb25c-113">\[在 \] 紋理座標中。</span><span class="sxs-lookup"><span data-stu-id="eb25c-113">\[in\] The texture coordinate.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="eb25c-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="eb25c-114">Return Value</span></span>

<span data-ttu-id="eb25c-115">材質資料的值。</span><span class="sxs-lookup"><span data-stu-id="eb25c-115">The value of the texture data.</span></span>

## <a name="type-description"></a><span data-ttu-id="eb25c-116">類型描述</span><span class="sxs-lookup"><span data-stu-id="eb25c-116">Type Description</span></span>



| <span data-ttu-id="eb25c-117">Name</span><span class="sxs-lookup"><span data-stu-id="eb25c-117">Name</span></span> | <span data-ttu-id="eb25c-118">輸入/輸出</span><span class="sxs-lookup"><span data-stu-id="eb25c-118">In/Out</span></span> | [<span data-ttu-id="eb25c-119">**範本類型**</span><span class="sxs-lookup"><span data-stu-id="eb25c-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="eb25c-120">**元件類型**</span><span class="sxs-lookup"><span data-stu-id="eb25c-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="eb25c-121">大小</span><span class="sxs-lookup"><span data-stu-id="eb25c-121">Size</span></span> |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="eb25c-122">s</span><span class="sxs-lookup"><span data-stu-id="eb25c-122">s</span></span>    | <span data-ttu-id="eb25c-123">in</span><span class="sxs-lookup"><span data-stu-id="eb25c-123">in</span></span>     | [<span data-ttu-id="eb25c-124">**物件**</span><span class="sxs-lookup"><span data-stu-id="eb25c-124">**object**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="eb25c-125">sampler3D</span><span class="sxs-lookup"><span data-stu-id="eb25c-125">sampler3D</span></span>](dx-graphics-hlsl-sampler.md)                      | <span data-ttu-id="eb25c-126">1</span><span class="sxs-lookup"><span data-stu-id="eb25c-126">1</span></span>    |
| <span data-ttu-id="eb25c-127">t</span><span class="sxs-lookup"><span data-stu-id="eb25c-127">t</span></span>    | <span data-ttu-id="eb25c-128">in</span><span class="sxs-lookup"><span data-stu-id="eb25c-128">in</span></span>     | [<span data-ttu-id="eb25c-129">**向量**</span><span class="sxs-lookup"><span data-stu-id="eb25c-129">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="eb25c-130">**浮動**</span><span class="sxs-lookup"><span data-stu-id="eb25c-130">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="eb25c-131">4</span><span class="sxs-lookup"><span data-stu-id="eb25c-131">4</span></span>    |
| <span data-ttu-id="eb25c-132">Ret</span><span class="sxs-lookup"><span data-stu-id="eb25c-132">ret</span></span>  | <span data-ttu-id="eb25c-133">out</span><span class="sxs-lookup"><span data-stu-id="eb25c-133">out</span></span>    | [<span data-ttu-id="eb25c-134">**向量**</span><span class="sxs-lookup"><span data-stu-id="eb25c-134">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="eb25c-135">**浮動**</span><span class="sxs-lookup"><span data-stu-id="eb25c-135">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="eb25c-136">4</span><span class="sxs-lookup"><span data-stu-id="eb25c-136">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="eb25c-137">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="eb25c-137">Minimum Shader Model</span></span>

<span data-ttu-id="eb25c-138">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="eb25c-138">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="eb25c-139">著色器模型</span><span class="sxs-lookup"><span data-stu-id="eb25c-139">Shader Model</span></span>                                              | <span data-ttu-id="eb25c-140">支援</span><span class="sxs-lookup"><span data-stu-id="eb25c-140">Supported</span></span>               |
|-----------------------------------------------------------|-------------------------|
| [<span data-ttu-id="eb25c-141">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="eb25c-141">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="eb25c-142">是 (只) 圖元著色器</span><span class="sxs-lookup"><span data-stu-id="eb25c-142">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="eb25c-143">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="eb25c-143">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="eb25c-144">是 (只) 圖元著色器</span><span class="sxs-lookup"><span data-stu-id="eb25c-144">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="eb25c-145">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="eb25c-145">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="eb25c-146">是 (只) 圖元著色器</span><span class="sxs-lookup"><span data-stu-id="eb25c-146">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="eb25c-147">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="eb25c-147">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="eb25c-148">不可以</span><span class="sxs-lookup"><span data-stu-id="eb25c-148">no</span></span>                      |



 

## <a name="see-also"></a><span data-ttu-id="eb25c-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="eb25c-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb25c-150">**(DirectX HLSL) 內建函式**</span><span class="sxs-lookup"><span data-stu-id="eb25c-150">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

