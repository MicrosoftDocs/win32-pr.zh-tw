---
title: 'texCUBE (HLSL 參考) '
description: 範例 cube 紋理。
ms.assetid: 77943eb9-86e8-4ae4-8975-8f925e084ce4
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
ms.openlocfilehash: 524ed44028372eeabf176c30da8b3a31a8ee7988
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023608"
---
# <a name="texcube-hlsl-reference"></a><span data-ttu-id="ee869-104">texCUBE (HLSL 參考) </span><span class="sxs-lookup"><span data-stu-id="ee869-104">texCUBE (HLSL reference)</span></span>

<span data-ttu-id="ee869-105">範例 cube 紋理。</span><span class="sxs-lookup"><span data-stu-id="ee869-105">Samples a cube texture.</span></span>



| <span data-ttu-id="ee869-106">ret texCUBE (s，t) </span><span class="sxs-lookup"><span data-stu-id="ee869-106">ret texCUBE(s, t)</span></span> |
|-------------------|



 

## <a name="parameters"></a><span data-ttu-id="ee869-107">參數</span><span class="sxs-lookup"><span data-stu-id="ee869-107">Parameters</span></span>



| <span data-ttu-id="ee869-108">項目</span><span class="sxs-lookup"><span data-stu-id="ee869-108">Item</span></span>                                                   | <span data-ttu-id="ee869-109">描述</span><span class="sxs-lookup"><span data-stu-id="ee869-109">Description</span></span>                               |
|--------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="ee869-110"><span id="s"></span><span id="S"></span>*！*</span><span class="sxs-lookup"><span data-stu-id="ee869-110"><span id="s"></span><span id="S"></span>*s*</span></span><br/> | <span data-ttu-id="ee869-111">\[在 \] 取樣器狀態中。</span><span class="sxs-lookup"><span data-stu-id="ee869-111">\[in\] The sampler state.</span></span><br/>      |
| <span data-ttu-id="ee869-112"><span id="t"></span><span id="T"></span>*10gbase-t*</span><span class="sxs-lookup"><span data-stu-id="ee869-112"><span id="t"></span><span id="T"></span>*t*</span></span><br/> | <span data-ttu-id="ee869-113">\[在 \] 紋理座標中。</span><span class="sxs-lookup"><span data-stu-id="ee869-113">\[in\] The texture coordinate.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="ee869-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="ee869-114">Return Value</span></span>

<span data-ttu-id="ee869-115">材質資料的值。</span><span class="sxs-lookup"><span data-stu-id="ee869-115">The value of the texture data.</span></span>

## <a name="type-description"></a><span data-ttu-id="ee869-116">類型描述</span><span class="sxs-lookup"><span data-stu-id="ee869-116">Type Description</span></span>



| <span data-ttu-id="ee869-117">Name</span><span class="sxs-lookup"><span data-stu-id="ee869-117">Name</span></span> | <span data-ttu-id="ee869-118">輸入/輸出</span><span class="sxs-lookup"><span data-stu-id="ee869-118">In/Out</span></span> | [<span data-ttu-id="ee869-119">**範本類型**</span><span class="sxs-lookup"><span data-stu-id="ee869-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="ee869-120">**元件類型**</span><span class="sxs-lookup"><span data-stu-id="ee869-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="ee869-121">大小</span><span class="sxs-lookup"><span data-stu-id="ee869-121">Size</span></span> |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="ee869-122">s</span><span class="sxs-lookup"><span data-stu-id="ee869-122">s</span></span>    | <span data-ttu-id="ee869-123">in</span><span class="sxs-lookup"><span data-stu-id="ee869-123">in</span></span>     | [<span data-ttu-id="ee869-124">**物件**</span><span class="sxs-lookup"><span data-stu-id="ee869-124">**object**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="ee869-125">samplerCUBE</span><span class="sxs-lookup"><span data-stu-id="ee869-125">samplerCUBE</span></span>](dx-graphics-hlsl-sampler.md)                    | <span data-ttu-id="ee869-126">1</span><span class="sxs-lookup"><span data-stu-id="ee869-126">1</span></span>    |
| <span data-ttu-id="ee869-127">t</span><span class="sxs-lookup"><span data-stu-id="ee869-127">t</span></span>    | <span data-ttu-id="ee869-128">in</span><span class="sxs-lookup"><span data-stu-id="ee869-128">in</span></span>     | [<span data-ttu-id="ee869-129">**向量**</span><span class="sxs-lookup"><span data-stu-id="ee869-129">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="ee869-130">**浮動**</span><span class="sxs-lookup"><span data-stu-id="ee869-130">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="ee869-131">3</span><span class="sxs-lookup"><span data-stu-id="ee869-131">3</span></span>    |
| <span data-ttu-id="ee869-132">Ret</span><span class="sxs-lookup"><span data-stu-id="ee869-132">ret</span></span>  | <span data-ttu-id="ee869-133">out</span><span class="sxs-lookup"><span data-stu-id="ee869-133">out</span></span>    | [<span data-ttu-id="ee869-134">**向量**</span><span class="sxs-lookup"><span data-stu-id="ee869-134">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="ee869-135">**浮動**</span><span class="sxs-lookup"><span data-stu-id="ee869-135">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="ee869-136">4</span><span class="sxs-lookup"><span data-stu-id="ee869-136">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="ee869-137">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="ee869-137">Minimum Shader Model</span></span>

<span data-ttu-id="ee869-138">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="ee869-138">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="ee869-139">著色器模型</span><span class="sxs-lookup"><span data-stu-id="ee869-139">Shader Model</span></span>                                              | <span data-ttu-id="ee869-140">支援</span><span class="sxs-lookup"><span data-stu-id="ee869-140">Supported</span></span>               |
|-----------------------------------------------------------|-------------------------|
| [<span data-ttu-id="ee869-141">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="ee869-141">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="ee869-142">是 (只) 圖元著色器</span><span class="sxs-lookup"><span data-stu-id="ee869-142">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="ee869-143">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="ee869-143">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="ee869-144">是 (只) 圖元著色器</span><span class="sxs-lookup"><span data-stu-id="ee869-144">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="ee869-145">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="ee869-145">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="ee869-146">是 (只) 圖元著色器</span><span class="sxs-lookup"><span data-stu-id="ee869-146">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="ee869-147">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="ee869-147">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="ee869-148">是 (只) 圖元著色器</span><span class="sxs-lookup"><span data-stu-id="ee869-148">yes (pixel shader only)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="ee869-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ee869-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee869-150">**(DirectX HLSL) 內建函式**</span><span class="sxs-lookup"><span data-stu-id="ee869-150">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

