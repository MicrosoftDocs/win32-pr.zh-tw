---
title: 'tex3D (HLSL 參考) '
description: 範例3D 紋理。
ms.assetid: 713eec24-bdf5-456e-98da-30e2c9d7e808
keywords:
- tex3D HLSL
topic_type:
- apiref
api_name:
- tex3D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e3a071d00dedabdff02bae302c71aa8ecece4ba2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682912"
---
# <a name="tex3d-hlsl-reference"></a><span data-ttu-id="94511-104">tex3D (HLSL 參考) </span><span class="sxs-lookup"><span data-stu-id="94511-104">tex3D (HLSL reference)</span></span>

<span data-ttu-id="94511-105">範例3D 紋理。</span><span class="sxs-lookup"><span data-stu-id="94511-105">Samples a 3D texture.</span></span>



| <span data-ttu-id="94511-106">ret tex3D (s，t) </span><span class="sxs-lookup"><span data-stu-id="94511-106">ret tex3D(s, t)</span></span> |
|-----------------|



 

## <a name="parameters"></a><span data-ttu-id="94511-107">參數</span><span class="sxs-lookup"><span data-stu-id="94511-107">Parameters</span></span>



| <span data-ttu-id="94511-108">項目</span><span class="sxs-lookup"><span data-stu-id="94511-108">Item</span></span>                                                   | <span data-ttu-id="94511-109">描述</span><span class="sxs-lookup"><span data-stu-id="94511-109">Description</span></span>                               |
|--------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="94511-110"><span id="s"></span><span id="S"></span>*！*</span><span class="sxs-lookup"><span data-stu-id="94511-110"><span id="s"></span><span id="S"></span>*s*</span></span><br/> | <span data-ttu-id="94511-111">\[在 \] 取樣器狀態中。</span><span class="sxs-lookup"><span data-stu-id="94511-111">\[in\] The sampler state.</span></span><br/>      |
| <span data-ttu-id="94511-112"><span id="t"></span><span id="T"></span>*10gbase-t*</span><span class="sxs-lookup"><span data-stu-id="94511-112"><span id="t"></span><span id="T"></span>*t*</span></span><br/> | <span data-ttu-id="94511-113">\[在 \] 紋理座標中。</span><span class="sxs-lookup"><span data-stu-id="94511-113">\[in\] The texture coordinate.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="94511-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="94511-114">Return Value</span></span>

<span data-ttu-id="94511-115">材質資料的值。</span><span class="sxs-lookup"><span data-stu-id="94511-115">The value of the texture data.</span></span>

## <a name="type-description"></a><span data-ttu-id="94511-116">類型描述</span><span class="sxs-lookup"><span data-stu-id="94511-116">Type Description</span></span>



| <span data-ttu-id="94511-117">Name</span><span class="sxs-lookup"><span data-stu-id="94511-117">Name</span></span> | <span data-ttu-id="94511-118">輸入/輸出</span><span class="sxs-lookup"><span data-stu-id="94511-118">In/Out</span></span> | [<span data-ttu-id="94511-119">**範本類型**</span><span class="sxs-lookup"><span data-stu-id="94511-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="94511-120">**元件類型**</span><span class="sxs-lookup"><span data-stu-id="94511-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="94511-121">大小</span><span class="sxs-lookup"><span data-stu-id="94511-121">Size</span></span> |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="94511-122">s</span><span class="sxs-lookup"><span data-stu-id="94511-122">s</span></span>    | <span data-ttu-id="94511-123">in</span><span class="sxs-lookup"><span data-stu-id="94511-123">in</span></span>     | [<span data-ttu-id="94511-124">**物件**</span><span class="sxs-lookup"><span data-stu-id="94511-124">**object**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="94511-125">sampler3D</span><span class="sxs-lookup"><span data-stu-id="94511-125">sampler3D</span></span>](dx-graphics-hlsl-sampler.md)                      | <span data-ttu-id="94511-126">1</span><span class="sxs-lookup"><span data-stu-id="94511-126">1</span></span>    |
| <span data-ttu-id="94511-127">t</span><span class="sxs-lookup"><span data-stu-id="94511-127">t</span></span>    | <span data-ttu-id="94511-128">in</span><span class="sxs-lookup"><span data-stu-id="94511-128">in</span></span>     | [<span data-ttu-id="94511-129">**向量**</span><span class="sxs-lookup"><span data-stu-id="94511-129">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="94511-130">**浮動**</span><span class="sxs-lookup"><span data-stu-id="94511-130">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="94511-131">3</span><span class="sxs-lookup"><span data-stu-id="94511-131">3</span></span>    |
| <span data-ttu-id="94511-132">Ret</span><span class="sxs-lookup"><span data-stu-id="94511-132">ret</span></span>  | <span data-ttu-id="94511-133">out</span><span class="sxs-lookup"><span data-stu-id="94511-133">out</span></span>    | [<span data-ttu-id="94511-134">**向量**</span><span class="sxs-lookup"><span data-stu-id="94511-134">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="94511-135">**浮動**</span><span class="sxs-lookup"><span data-stu-id="94511-135">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="94511-136">4</span><span class="sxs-lookup"><span data-stu-id="94511-136">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="94511-137">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="94511-137">Minimum Shader Model</span></span>

<span data-ttu-id="94511-138">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="94511-138">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="94511-139">著色器模型</span><span class="sxs-lookup"><span data-stu-id="94511-139">Shader Model</span></span>                                              | <span data-ttu-id="94511-140">支援</span><span class="sxs-lookup"><span data-stu-id="94511-140">Supported</span></span>                                                                                                                         |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="94511-141">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="94511-141">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="94511-142">是 (只) 圖元著色器，但在編譯時，您必須使用 [舊版編譯選項](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax) 。</span><span class="sxs-lookup"><span data-stu-id="94511-142">yes (pixel shader only), but you must use the [legacy compile option](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax) when compiling.</span></span> |
| [<span data-ttu-id="94511-143">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="94511-143">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="94511-144">是 (只) 圖元著色器</span><span class="sxs-lookup"><span data-stu-id="94511-144">yes (pixel shader only)</span></span>                                                                                                           |
| [<span data-ttu-id="94511-145">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="94511-145">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="94511-146">是 (只) 圖元著色器</span><span class="sxs-lookup"><span data-stu-id="94511-146">yes (pixel shader only)</span></span>                                                                                                           |
| [<span data-ttu-id="94511-147">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="94511-147">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="94511-148">是 (只) 圖元著色器</span><span class="sxs-lookup"><span data-stu-id="94511-148">yes (pixel shader only)</span></span>                                                                                                           |



 

## <a name="see-also"></a><span data-ttu-id="94511-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="94511-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94511-150">**(DirectX HLSL) 內建函式**</span><span class="sxs-lookup"><span data-stu-id="94511-150">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

