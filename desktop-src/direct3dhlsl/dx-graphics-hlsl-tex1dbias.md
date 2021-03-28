---
title: tex1Dbias
description: 依 t.w. 在偏差 mip 層級之後範例1D 紋理
ms.assetid: 2619ae23-e4b2-4699-b2ac-5ee711f9569a
keywords:
- tex1Dbias HLSL
topic_type:
- apiref
api_name:
- tex1Dbias
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0328b9328a1406177fa26bd566c0fbf7d384db63
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104092821"
---
# <a name="tex1dbias"></a><span data-ttu-id="64a61-104">tex1Dbias</span><span class="sxs-lookup"><span data-stu-id="64a61-104">tex1Dbias</span></span>

<span data-ttu-id="64a61-105">依 t.w. 在偏差 mip 層級之後範例1D 紋理</span><span class="sxs-lookup"><span data-stu-id="64a61-105">Samples a 1D texture after biasing the mip level by t.w.</span></span>



| <span data-ttu-id="64a61-106">ret tex1Dbias (s，t) </span><span class="sxs-lookup"><span data-stu-id="64a61-106">ret tex1Dbias(s, t)</span></span> |
|---------------------|



 

## <a name="parameters"></a><span data-ttu-id="64a61-107">參數</span><span class="sxs-lookup"><span data-stu-id="64a61-107">Parameters</span></span>



| <span data-ttu-id="64a61-108">項目</span><span class="sxs-lookup"><span data-stu-id="64a61-108">Item</span></span>                                                   | <span data-ttu-id="64a61-109">描述</span><span class="sxs-lookup"><span data-stu-id="64a61-109">Description</span></span>                               |
|--------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="64a61-110"><span id="s"></span><span id="S"></span>*！*</span><span class="sxs-lookup"><span data-stu-id="64a61-110"><span id="s"></span><span id="S"></span>*s*</span></span><br/> | <span data-ttu-id="64a61-111">\[在 \] 取樣器狀態中。</span><span class="sxs-lookup"><span data-stu-id="64a61-111">\[in\] The sampler state.</span></span><br/>      |
| <span data-ttu-id="64a61-112"><span id="t"></span><span id="T"></span>*10gbase-t*</span><span class="sxs-lookup"><span data-stu-id="64a61-112"><span id="t"></span><span id="T"></span>*t*</span></span><br/> | <span data-ttu-id="64a61-113">\[在 \] 紋理座標中。</span><span class="sxs-lookup"><span data-stu-id="64a61-113">\[in\] The texture coordinate.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="64a61-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="64a61-114">Return Value</span></span>

<span data-ttu-id="64a61-115">材質資料的值。</span><span class="sxs-lookup"><span data-stu-id="64a61-115">The value of the texture data.</span></span>

## <a name="type-description"></a><span data-ttu-id="64a61-116">類型描述</span><span class="sxs-lookup"><span data-stu-id="64a61-116">Type Description</span></span>



| <span data-ttu-id="64a61-117">名稱</span><span class="sxs-lookup"><span data-stu-id="64a61-117">Name</span></span> | <span data-ttu-id="64a61-118">輸入/輸出</span><span class="sxs-lookup"><span data-stu-id="64a61-118">In/Out</span></span> | [<span data-ttu-id="64a61-119">**範本類型**</span><span class="sxs-lookup"><span data-stu-id="64a61-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="64a61-120">**元件類型**</span><span class="sxs-lookup"><span data-stu-id="64a61-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="64a61-121">大小</span><span class="sxs-lookup"><span data-stu-id="64a61-121">Size</span></span> |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="64a61-122">s</span><span class="sxs-lookup"><span data-stu-id="64a61-122">s</span></span>    | <span data-ttu-id="64a61-123">in</span><span class="sxs-lookup"><span data-stu-id="64a61-123">in</span></span>     | [<span data-ttu-id="64a61-124">**物件**</span><span class="sxs-lookup"><span data-stu-id="64a61-124">**object**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="64a61-125">sampler1D</span><span class="sxs-lookup"><span data-stu-id="64a61-125">sampler1D</span></span>](dx-graphics-hlsl-sampler.md)                      | <span data-ttu-id="64a61-126">1</span><span class="sxs-lookup"><span data-stu-id="64a61-126">1</span></span>    |
| <span data-ttu-id="64a61-127">t</span><span class="sxs-lookup"><span data-stu-id="64a61-127">t</span></span>    | <span data-ttu-id="64a61-128">in</span><span class="sxs-lookup"><span data-stu-id="64a61-128">in</span></span>     | [<span data-ttu-id="64a61-129">**向量**</span><span class="sxs-lookup"><span data-stu-id="64a61-129">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="64a61-130">**浮動**</span><span class="sxs-lookup"><span data-stu-id="64a61-130">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="64a61-131">4</span><span class="sxs-lookup"><span data-stu-id="64a61-131">4</span></span>    |
| <span data-ttu-id="64a61-132">Ret</span><span class="sxs-lookup"><span data-stu-id="64a61-132">ret</span></span>  | <span data-ttu-id="64a61-133">out</span><span class="sxs-lookup"><span data-stu-id="64a61-133">out</span></span>    | [<span data-ttu-id="64a61-134">**向量**</span><span class="sxs-lookup"><span data-stu-id="64a61-134">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="64a61-135">**浮動**</span><span class="sxs-lookup"><span data-stu-id="64a61-135">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="64a61-136">4</span><span class="sxs-lookup"><span data-stu-id="64a61-136">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="64a61-137">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="64a61-137">Minimum Shader Model</span></span>

<span data-ttu-id="64a61-138">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="64a61-138">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="64a61-139">著色器模型</span><span class="sxs-lookup"><span data-stu-id="64a61-139">Shader Model</span></span>                                              | <span data-ttu-id="64a61-140">支援</span><span class="sxs-lookup"><span data-stu-id="64a61-140">Supported</span></span>               |
|-----------------------------------------------------------|-------------------------|
| [<span data-ttu-id="64a61-141">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="64a61-141">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="64a61-142">是 (只) 圖元著色器</span><span class="sxs-lookup"><span data-stu-id="64a61-142">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="64a61-143">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="64a61-143">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="64a61-144">是 (只) 圖元著色器</span><span class="sxs-lookup"><span data-stu-id="64a61-144">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="64a61-145">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="64a61-145">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="64a61-146">是 (只) 圖元著色器</span><span class="sxs-lookup"><span data-stu-id="64a61-146">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="64a61-147">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="64a61-147">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="64a61-148">不可以</span><span class="sxs-lookup"><span data-stu-id="64a61-148">no</span></span>                      |



 

## <a name="see-also"></a><span data-ttu-id="64a61-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="64a61-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64a61-150">**(DirectX HLSL) 內建函式**</span><span class="sxs-lookup"><span data-stu-id="64a61-150">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

