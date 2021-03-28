---
title: tex2Dproj
description: 使用 projective 除法來取樣2D 材質;紋理座標會在進行查閱之前除以 t. w。
ms.assetid: c6b79360-3737-4b74-bdf3-6d46323e8e54
keywords:
- tex2Dproj HLSL
topic_type:
- apiref
api_name:
- tex2Dproj
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 365401e4e4eca8703207ffb5c7676748f4a06d30
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104507967"
---
# <a name="tex2dproj"></a><span data-ttu-id="6a432-104">tex2Dproj</span><span class="sxs-lookup"><span data-stu-id="6a432-104">tex2Dproj</span></span>

<span data-ttu-id="6a432-105">使用 projective 除法來取樣2D 材質;紋理座標會在進行查閱之前除以 t. w。</span><span class="sxs-lookup"><span data-stu-id="6a432-105">Samples a 2D texture using a projective divide; the texture coordinate is divided by t.w before the lookup takes place.</span></span>



| <span data-ttu-id="6a432-106">ret tex2Dproj (s，t) </span><span class="sxs-lookup"><span data-stu-id="6a432-106">ret tex2Dproj(s, t)</span></span> |
|---------------------|



 

## <a name="parameters"></a><span data-ttu-id="6a432-107">參數</span><span class="sxs-lookup"><span data-stu-id="6a432-107">Parameters</span></span>



| <span data-ttu-id="6a432-108">項目</span><span class="sxs-lookup"><span data-stu-id="6a432-108">Item</span></span>                                                   | <span data-ttu-id="6a432-109">描述</span><span class="sxs-lookup"><span data-stu-id="6a432-109">Description</span></span>                               |
|--------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="6a432-110"><span id="s"></span><span id="S"></span>*！*</span><span class="sxs-lookup"><span data-stu-id="6a432-110"><span id="s"></span><span id="S"></span>*s*</span></span><br/> | <span data-ttu-id="6a432-111">\[在 \] 取樣器狀態中。</span><span class="sxs-lookup"><span data-stu-id="6a432-111">\[in\] The sampler state.</span></span><br/>      |
| <span data-ttu-id="6a432-112"><span id="t"></span><span id="T"></span>*10gbase-t*</span><span class="sxs-lookup"><span data-stu-id="6a432-112"><span id="t"></span><span id="T"></span>*t*</span></span><br/> | <span data-ttu-id="6a432-113">\[在 \] 紋理座標中。</span><span class="sxs-lookup"><span data-stu-id="6a432-113">\[in\] The texture coordinate.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="6a432-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="6a432-114">Return Value</span></span>

<span data-ttu-id="6a432-115">材質資料的值。</span><span class="sxs-lookup"><span data-stu-id="6a432-115">The value of the texture data.</span></span>

## <a name="type-description"></a><span data-ttu-id="6a432-116">類型描述</span><span class="sxs-lookup"><span data-stu-id="6a432-116">Type Description</span></span>



| <span data-ttu-id="6a432-117">Name</span><span class="sxs-lookup"><span data-stu-id="6a432-117">Name</span></span> | <span data-ttu-id="6a432-118">輸入/輸出</span><span class="sxs-lookup"><span data-stu-id="6a432-118">In/Out</span></span> | [<span data-ttu-id="6a432-119">**範本類型**</span><span class="sxs-lookup"><span data-stu-id="6a432-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="6a432-120">**元件類型**</span><span class="sxs-lookup"><span data-stu-id="6a432-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="6a432-121">大小</span><span class="sxs-lookup"><span data-stu-id="6a432-121">Size</span></span> |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="6a432-122">s</span><span class="sxs-lookup"><span data-stu-id="6a432-122">s</span></span>    | <span data-ttu-id="6a432-123">in</span><span class="sxs-lookup"><span data-stu-id="6a432-123">in</span></span>     | [<span data-ttu-id="6a432-124">**物件**</span><span class="sxs-lookup"><span data-stu-id="6a432-124">**object**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="6a432-125">sampler2D</span><span class="sxs-lookup"><span data-stu-id="6a432-125">sampler2D</span></span>](dx-graphics-hlsl-sampler.md)                      | <span data-ttu-id="6a432-126">1</span><span class="sxs-lookup"><span data-stu-id="6a432-126">1</span></span>    |
| <span data-ttu-id="6a432-127">t</span><span class="sxs-lookup"><span data-stu-id="6a432-127">t</span></span>    | <span data-ttu-id="6a432-128">in</span><span class="sxs-lookup"><span data-stu-id="6a432-128">in</span></span>     | [<span data-ttu-id="6a432-129">**向量**</span><span class="sxs-lookup"><span data-stu-id="6a432-129">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="6a432-130">**浮動**</span><span class="sxs-lookup"><span data-stu-id="6a432-130">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="6a432-131">4</span><span class="sxs-lookup"><span data-stu-id="6a432-131">4</span></span>    |
| <span data-ttu-id="6a432-132">Ret</span><span class="sxs-lookup"><span data-stu-id="6a432-132">ret</span></span>  | <span data-ttu-id="6a432-133">out</span><span class="sxs-lookup"><span data-stu-id="6a432-133">out</span></span>    | [<span data-ttu-id="6a432-134">**向量**</span><span class="sxs-lookup"><span data-stu-id="6a432-134">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="6a432-135">**浮動**</span><span class="sxs-lookup"><span data-stu-id="6a432-135">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="6a432-136">4</span><span class="sxs-lookup"><span data-stu-id="6a432-136">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="6a432-137">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="6a432-137">Minimum Shader Model</span></span>

<span data-ttu-id="6a432-138">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="6a432-138">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="6a432-139">著色器模型</span><span class="sxs-lookup"><span data-stu-id="6a432-139">Shader Model</span></span>                                              | <span data-ttu-id="6a432-140">支援</span><span class="sxs-lookup"><span data-stu-id="6a432-140">Supported</span></span>               |
|-----------------------------------------------------------|-------------------------|
| [<span data-ttu-id="6a432-141">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="6a432-141">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="6a432-142">是 (只) 圖元著色器</span><span class="sxs-lookup"><span data-stu-id="6a432-142">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="6a432-143">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="6a432-143">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="6a432-144">是 (只) 圖元著色器</span><span class="sxs-lookup"><span data-stu-id="6a432-144">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="6a432-145">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="6a432-145">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="6a432-146">是 (只) 圖元著色器</span><span class="sxs-lookup"><span data-stu-id="6a432-146">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="6a432-147">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="6a432-147">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="6a432-148">不可以</span><span class="sxs-lookup"><span data-stu-id="6a432-148">no</span></span>                      |



 

## <a name="see-also"></a><span data-ttu-id="6a432-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6a432-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a432-150">**(DirectX HLSL) 內建函式**</span><span class="sxs-lookup"><span data-stu-id="6a432-150">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

