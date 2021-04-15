---
title: texCUBEproj
description: 使用 projective 除的 cube 紋理範例;紋理座標會在進行查閱之前除以 t. w。
ms.assetid: 86bdd1c3-0a8d-4d09-b70d-1ebcee32c866
keywords:
- texCUBEproj HLSL
topic_type:
- apiref
api_name:
- texCUBEproj
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d23a9b85034c1591cfe695759b29612a3674d436
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463629"
---
# <a name="texcubeproj"></a><span data-ttu-id="04253-104">texCUBEproj</span><span class="sxs-lookup"><span data-stu-id="04253-104">texCUBEproj</span></span>

<span data-ttu-id="04253-105">使用 projective 除的 cube 紋理範例;紋理座標會在進行查閱之前除以 t. w。</span><span class="sxs-lookup"><span data-stu-id="04253-105">Samples a cube texture using a projective divide; the texture coordinate is divided by t.w before the lookup takes place.</span></span>



| <span data-ttu-id="04253-106">ret texCUBEproj (s，t) </span><span class="sxs-lookup"><span data-stu-id="04253-106">ret texCUBEproj(s, t)</span></span> |
|-----------------------|



 

## <a name="parameters"></a><span data-ttu-id="04253-107">參數</span><span class="sxs-lookup"><span data-stu-id="04253-107">Parameters</span></span>



| <span data-ttu-id="04253-108">項目</span><span class="sxs-lookup"><span data-stu-id="04253-108">Item</span></span>                                                   | <span data-ttu-id="04253-109">描述</span><span class="sxs-lookup"><span data-stu-id="04253-109">Description</span></span>                               |
|--------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="04253-110"><span id="s"></span><span id="S"></span>*！*</span><span class="sxs-lookup"><span data-stu-id="04253-110"><span id="s"></span><span id="S"></span>*s*</span></span><br/> | <span data-ttu-id="04253-111">\[在 \] 取樣器狀態中。</span><span class="sxs-lookup"><span data-stu-id="04253-111">\[in\] The sampler state.</span></span><br/>      |
| <span data-ttu-id="04253-112"><span id="t"></span><span id="T"></span>*10gbase-t*</span><span class="sxs-lookup"><span data-stu-id="04253-112"><span id="t"></span><span id="T"></span>*t*</span></span><br/> | <span data-ttu-id="04253-113">\[在 \] 紋理座標中。</span><span class="sxs-lookup"><span data-stu-id="04253-113">\[in\] The texture coordinate.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="04253-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="04253-114">Return Value</span></span>

<span data-ttu-id="04253-115">材質資料的值。</span><span class="sxs-lookup"><span data-stu-id="04253-115">The value of the texture data.</span></span>

## <a name="type-description"></a><span data-ttu-id="04253-116">類型描述</span><span class="sxs-lookup"><span data-stu-id="04253-116">Type Description</span></span>



| <span data-ttu-id="04253-117">名稱</span><span class="sxs-lookup"><span data-stu-id="04253-117">Name</span></span> | <span data-ttu-id="04253-118">輸入/輸出</span><span class="sxs-lookup"><span data-stu-id="04253-118">In/Out</span></span> | [<span data-ttu-id="04253-119">**範本類型**</span><span class="sxs-lookup"><span data-stu-id="04253-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="04253-120">**元件類型**</span><span class="sxs-lookup"><span data-stu-id="04253-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="04253-121">大小</span><span class="sxs-lookup"><span data-stu-id="04253-121">Size</span></span> |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="04253-122">s</span><span class="sxs-lookup"><span data-stu-id="04253-122">s</span></span>    | <span data-ttu-id="04253-123">in</span><span class="sxs-lookup"><span data-stu-id="04253-123">in</span></span>     | [<span data-ttu-id="04253-124">**物件**</span><span class="sxs-lookup"><span data-stu-id="04253-124">**object**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="04253-125">samplerCUBE</span><span class="sxs-lookup"><span data-stu-id="04253-125">samplerCUBE</span></span>](dx-graphics-hlsl-sampler.md)                    | <span data-ttu-id="04253-126">1</span><span class="sxs-lookup"><span data-stu-id="04253-126">1</span></span>    |
| <span data-ttu-id="04253-127">t</span><span class="sxs-lookup"><span data-stu-id="04253-127">t</span></span>    | <span data-ttu-id="04253-128">in</span><span class="sxs-lookup"><span data-stu-id="04253-128">in</span></span>     | [<span data-ttu-id="04253-129">**向量**</span><span class="sxs-lookup"><span data-stu-id="04253-129">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="04253-130">**浮動**</span><span class="sxs-lookup"><span data-stu-id="04253-130">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="04253-131">4</span><span class="sxs-lookup"><span data-stu-id="04253-131">4</span></span>    |
| <span data-ttu-id="04253-132">Ret</span><span class="sxs-lookup"><span data-stu-id="04253-132">ret</span></span>  | <span data-ttu-id="04253-133">out</span><span class="sxs-lookup"><span data-stu-id="04253-133">out</span></span>    | [<span data-ttu-id="04253-134">**向量**</span><span class="sxs-lookup"><span data-stu-id="04253-134">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="04253-135">**浮動**</span><span class="sxs-lookup"><span data-stu-id="04253-135">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="04253-136">4</span><span class="sxs-lookup"><span data-stu-id="04253-136">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="04253-137">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="04253-137">Minimum Shader Model</span></span>

<span data-ttu-id="04253-138">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="04253-138">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="04253-139">著色器模型</span><span class="sxs-lookup"><span data-stu-id="04253-139">Shader Model</span></span>                                              | <span data-ttu-id="04253-140">支援</span><span class="sxs-lookup"><span data-stu-id="04253-140">Supported</span></span>               |
|-----------------------------------------------------------|-------------------------|
| [<span data-ttu-id="04253-141">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="04253-141">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="04253-142">是 (只) 圖元著色器</span><span class="sxs-lookup"><span data-stu-id="04253-142">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="04253-143">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="04253-143">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="04253-144">是 (只) 圖元著色器</span><span class="sxs-lookup"><span data-stu-id="04253-144">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="04253-145">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="04253-145">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="04253-146">是 (只) 圖元著色器</span><span class="sxs-lookup"><span data-stu-id="04253-146">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="04253-147">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="04253-147">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="04253-148">不可以</span><span class="sxs-lookup"><span data-stu-id="04253-148">no</span></span>                      |



 

## <a name="see-also"></a><span data-ttu-id="04253-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="04253-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04253-150">**(DirectX HLSL) 內建函式**</span><span class="sxs-lookup"><span data-stu-id="04253-150">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

