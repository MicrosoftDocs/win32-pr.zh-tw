---
title: texCUBEbias
description: 依 t.w. 在偏差 mip 層級之後，對 cube 材質進行取樣
ms.assetid: dad27cff-6b10-45db-b70f-c4ad78c64e76
keywords:
- texCUBEbias HLSL
topic_type:
- apiref
api_name:
- texCUBEbias
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0129c20db1da320e9cb85aacfc4490124be28f8a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104092773"
---
# <a name="texcubebias"></a><span data-ttu-id="18777-104">texCUBEbias</span><span class="sxs-lookup"><span data-stu-id="18777-104">texCUBEbias</span></span>

<span data-ttu-id="18777-105">依 t.w. 在偏差 mip 層級之後，對 cube 材質進行取樣</span><span class="sxs-lookup"><span data-stu-id="18777-105">Samples a cube texture after biasing the mip level by t.w.</span></span>



| <span data-ttu-id="18777-106">ret texCUBEbias (s，t) </span><span class="sxs-lookup"><span data-stu-id="18777-106">ret texCUBEbias(s, t)</span></span> |
|-----------------------|



 

## <a name="parameters"></a><span data-ttu-id="18777-107">參數</span><span class="sxs-lookup"><span data-stu-id="18777-107">Parameters</span></span>



| <span data-ttu-id="18777-108">項目</span><span class="sxs-lookup"><span data-stu-id="18777-108">Item</span></span>                                                   | <span data-ttu-id="18777-109">描述</span><span class="sxs-lookup"><span data-stu-id="18777-109">Description</span></span>                               |
|--------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="18777-110"><span id="s"></span><span id="S"></span>*！*</span><span class="sxs-lookup"><span data-stu-id="18777-110"><span id="s"></span><span id="S"></span>*s*</span></span><br/> | <span data-ttu-id="18777-111">\[在 \] 取樣器狀態中。</span><span class="sxs-lookup"><span data-stu-id="18777-111">\[in\] The sampler state.</span></span><br/>      |
| <span data-ttu-id="18777-112"><span id="t"></span><span id="T"></span>*10gbase-t*</span><span class="sxs-lookup"><span data-stu-id="18777-112"><span id="t"></span><span id="T"></span>*t*</span></span><br/> | <span data-ttu-id="18777-113">\[在 \] 紋理座標中。</span><span class="sxs-lookup"><span data-stu-id="18777-113">\[in\] The texture coordinate.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="18777-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="18777-114">Return Value</span></span>

<span data-ttu-id="18777-115">材質資料的值。</span><span class="sxs-lookup"><span data-stu-id="18777-115">The value of the texture data.</span></span>

## <a name="type-description"></a><span data-ttu-id="18777-116">類型描述</span><span class="sxs-lookup"><span data-stu-id="18777-116">Type Description</span></span>



| <span data-ttu-id="18777-117">名稱</span><span class="sxs-lookup"><span data-stu-id="18777-117">Name</span></span> | <span data-ttu-id="18777-118">輸入/輸出</span><span class="sxs-lookup"><span data-stu-id="18777-118">In/Out</span></span> | [<span data-ttu-id="18777-119">**範本類型**</span><span class="sxs-lookup"><span data-stu-id="18777-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="18777-120">**元件類型**</span><span class="sxs-lookup"><span data-stu-id="18777-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="18777-121">大小</span><span class="sxs-lookup"><span data-stu-id="18777-121">Size</span></span> |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="18777-122">s</span><span class="sxs-lookup"><span data-stu-id="18777-122">s</span></span>    | <span data-ttu-id="18777-123">in</span><span class="sxs-lookup"><span data-stu-id="18777-123">in</span></span>     | [<span data-ttu-id="18777-124">**物件**</span><span class="sxs-lookup"><span data-stu-id="18777-124">**object**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="18777-125">samplerCUBE</span><span class="sxs-lookup"><span data-stu-id="18777-125">samplerCUBE</span></span>](dx-graphics-hlsl-sampler.md)                    | <span data-ttu-id="18777-126">1</span><span class="sxs-lookup"><span data-stu-id="18777-126">1</span></span>    |
| <span data-ttu-id="18777-127">t</span><span class="sxs-lookup"><span data-stu-id="18777-127">t</span></span>    | <span data-ttu-id="18777-128">in</span><span class="sxs-lookup"><span data-stu-id="18777-128">in</span></span>     | [<span data-ttu-id="18777-129">**向量**</span><span class="sxs-lookup"><span data-stu-id="18777-129">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="18777-130">**浮動**</span><span class="sxs-lookup"><span data-stu-id="18777-130">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="18777-131">4</span><span class="sxs-lookup"><span data-stu-id="18777-131">4</span></span>    |
| <span data-ttu-id="18777-132">Ret</span><span class="sxs-lookup"><span data-stu-id="18777-132">ret</span></span>  | <span data-ttu-id="18777-133">out</span><span class="sxs-lookup"><span data-stu-id="18777-133">out</span></span>    | [<span data-ttu-id="18777-134">**向量**</span><span class="sxs-lookup"><span data-stu-id="18777-134">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="18777-135">**浮動**</span><span class="sxs-lookup"><span data-stu-id="18777-135">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="18777-136">4</span><span class="sxs-lookup"><span data-stu-id="18777-136">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="18777-137">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="18777-137">Minimum Shader Model</span></span>

<span data-ttu-id="18777-138">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="18777-138">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="18777-139">著色器模型</span><span class="sxs-lookup"><span data-stu-id="18777-139">Shader Model</span></span>                                              | <span data-ttu-id="18777-140">支援</span><span class="sxs-lookup"><span data-stu-id="18777-140">Supported</span></span>               |
|-----------------------------------------------------------|-------------------------|
| [<span data-ttu-id="18777-141">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="18777-141">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="18777-142">是 (只) 圖元著色器</span><span class="sxs-lookup"><span data-stu-id="18777-142">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="18777-143">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="18777-143">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="18777-144">是 (只) 圖元著色器</span><span class="sxs-lookup"><span data-stu-id="18777-144">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="18777-145">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="18777-145">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="18777-146">是 (只) 圖元著色器</span><span class="sxs-lookup"><span data-stu-id="18777-146">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="18777-147">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="18777-147">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="18777-148">不可以</span><span class="sxs-lookup"><span data-stu-id="18777-148">no</span></span>                      |



 

## <a name="see-also"></a><span data-ttu-id="18777-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="18777-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18777-150">**(DirectX HLSL) 內建函式**</span><span class="sxs-lookup"><span data-stu-id="18777-150">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

