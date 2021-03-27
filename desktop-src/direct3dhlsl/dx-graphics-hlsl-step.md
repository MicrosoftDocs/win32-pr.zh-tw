---
title: 步驟
description: 比較兩個值，並根據值大於的值傳回0或1。
ms.assetid: 1c1c4ec4-ae97-42ce-99af-71903e0b5edf
keywords:
- 步驟 HLSL
topic_type:
- apiref
api_name:
- step
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f9c800e8d8c6f78386139f822f118163f3b431f5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682914"
---
# <a name="step"></a><span data-ttu-id="0aae0-104">步驟</span><span class="sxs-lookup"><span data-stu-id="0aae0-104">step</span></span>

<span data-ttu-id="0aae0-105">比較兩個值，並根據值大於的值傳回0或1。</span><span class="sxs-lookup"><span data-stu-id="0aae0-105">Compares two values, returning 0 or 1 based on which value is greater.</span></span>



| <span data-ttu-id="0aae0-106">*ret* 步驟 (*y*， *x*) </span><span class="sxs-lookup"><span data-stu-id="0aae0-106">*ret* step(*y*, *x*)</span></span> |
|----------------------|



 

## <a name="parameters"></a><span data-ttu-id="0aae0-107">參數</span><span class="sxs-lookup"><span data-stu-id="0aae0-107">Parameters</span></span>



| <span data-ttu-id="0aae0-108">項目</span><span class="sxs-lookup"><span data-stu-id="0aae0-108">Item</span></span>                                                   | <span data-ttu-id="0aae0-109">描述</span><span class="sxs-lookup"><span data-stu-id="0aae0-109">Description</span></span>                                                   |
|--------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="0aae0-110"><span id="y"></span><span id="Y"></span>*Y*</span><span class="sxs-lookup"><span data-stu-id="0aae0-110"><span id="y"></span><span id="Y"></span>*y*</span></span><br/> | <span data-ttu-id="0aae0-111">\[\]要比較的第一個浮點值。</span><span class="sxs-lookup"><span data-stu-id="0aae0-111">\[in\] The first floating-point value to compare.</span></span><br/>  |
| <span data-ttu-id="0aae0-112"><span id="x"></span><span id="X"></span>*X*</span><span class="sxs-lookup"><span data-stu-id="0aae0-112"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="0aae0-113">\[\]要比較的第二個浮點值。</span><span class="sxs-lookup"><span data-stu-id="0aae0-113">\[in\] The second floating-point value to compare.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="0aae0-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="0aae0-114">Return Value</span></span>

<span data-ttu-id="0aae0-115">如果 *x* 參數大於或等於 *y* 參數，則為1。否則為0。</span><span class="sxs-lookup"><span data-stu-id="0aae0-115">1 if the *x* parameter is greater than or equal to the *y* parameter; otherwise, 0.</span></span>

## <a name="remarks"></a><span data-ttu-id="0aae0-116">備註</span><span class="sxs-lookup"><span data-stu-id="0aae0-116">Remarks</span></span>

<span data-ttu-id="0aae0-117">此函數使用下列公式： (*x*  >=  *y*) ？</span><span class="sxs-lookup"><span data-stu-id="0aae0-117">This function uses the following formula: (*x* >= *y*) ?</span></span> <span data-ttu-id="0aae0-118">1: 0。</span><span class="sxs-lookup"><span data-stu-id="0aae0-118">1 : 0.</span></span> <span data-ttu-id="0aae0-119">根據 *x* 參數是否大於 *y* 參數，函數會傳回0或1。</span><span class="sxs-lookup"><span data-stu-id="0aae0-119">The function returns either 0 or 1 depending on whether the *x* parameter is greater than the *y* parameter.</span></span> <span data-ttu-id="0aae0-120">若要計算0和1之間的平滑插補，請使用 [**smoothstep**](dx-graphics-hlsl-smoothstep.md) HLSL 內建函式。</span><span class="sxs-lookup"><span data-stu-id="0aae0-120">To compute a smooth interpolation between 0 and 1, use the [**smoothstep**](dx-graphics-hlsl-smoothstep.md) HLSL intrinsic function.</span></span>

## <a name="type-description"></a><span data-ttu-id="0aae0-121">類型描述</span><span class="sxs-lookup"><span data-stu-id="0aae0-121">Type Description</span></span>



| <span data-ttu-id="0aae0-122">Name</span><span class="sxs-lookup"><span data-stu-id="0aae0-122">Name</span></span>  | [<span data-ttu-id="0aae0-123">**範本類型**</span><span class="sxs-lookup"><span data-stu-id="0aae0-123">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="0aae0-124">**元件類型**</span><span class="sxs-lookup"><span data-stu-id="0aae0-124">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="0aae0-125">大小</span><span class="sxs-lookup"><span data-stu-id="0aae0-125">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="0aae0-126">*y*</span><span class="sxs-lookup"><span data-stu-id="0aae0-126">*y*</span></span>   | <span data-ttu-id="0aae0-127">純 [**量、**](dx-graphics-hlsl-intrinsic-functions.md)**向量** 或 **矩陣**</span><span class="sxs-lookup"><span data-stu-id="0aae0-127">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="0aae0-128">**浮動**</span><span class="sxs-lookup"><span data-stu-id="0aae0-128">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="0aae0-129">任意</span><span class="sxs-lookup"><span data-stu-id="0aae0-129">any</span></span>                            |
| <span data-ttu-id="0aae0-130">*x*</span><span class="sxs-lookup"><span data-stu-id="0aae0-130">*x*</span></span>   | <span data-ttu-id="0aae0-131">與輸入 *y* 相同</span><span class="sxs-lookup"><span data-stu-id="0aae0-131">same as input *y*</span></span>                                                                                              | [<span data-ttu-id="0aae0-132">**浮動**</span><span class="sxs-lookup"><span data-stu-id="0aae0-132">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="0aae0-133">) 為輸入 *y* 的相同維度 (s</span><span class="sxs-lookup"><span data-stu-id="0aae0-133">same dimension(s) as input *y*</span></span> |
| <span data-ttu-id="0aae0-134">*Ret*</span><span class="sxs-lookup"><span data-stu-id="0aae0-134">*ret*</span></span> | <span data-ttu-id="0aae0-135">與輸入 *y* 相同</span><span class="sxs-lookup"><span data-stu-id="0aae0-135">same as input *y*</span></span>                                                                                              | [<span data-ttu-id="0aae0-136">**浮動**</span><span class="sxs-lookup"><span data-stu-id="0aae0-136">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="0aae0-137">) 為輸入 *y* 的相同維度 (s</span><span class="sxs-lookup"><span data-stu-id="0aae0-137">same dimension(s) as input *y*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="0aae0-138">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="0aae0-138">Minimum Shader Model</span></span>

<span data-ttu-id="0aae0-139">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="0aae0-139">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="0aae0-140">著色器模型</span><span class="sxs-lookup"><span data-stu-id="0aae0-140">Shader Model</span></span>                                                                       | <span data-ttu-id="0aae0-141">支援</span><span class="sxs-lookup"><span data-stu-id="0aae0-141">Supported</span></span>                   |
|------------------------------------------------------------------------------------|-----------------------------|
| <span data-ttu-id="0aae0-142">[著色器模型 2 (DIRECTX HLSL) ](dx-graphics-hlsl-sm2.md) 和更高的著色器模型</span><span class="sxs-lookup"><span data-stu-id="0aae0-142">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="0aae0-143">是</span><span class="sxs-lookup"><span data-stu-id="0aae0-143">yes</span></span>                         |
| [<span data-ttu-id="0aae0-144">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="0aae0-144">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="0aae0-145">是 (vs \_ 1 \_ 1 和 ps \_ 1 \_ 4) </span><span class="sxs-lookup"><span data-stu-id="0aae0-145">yes (vs\_1\_1 and ps\_1\_4)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="0aae0-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0aae0-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0aae0-147">**(DirectX HLSL) 內建函式**</span><span class="sxs-lookup"><span data-stu-id="0aae0-147">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

