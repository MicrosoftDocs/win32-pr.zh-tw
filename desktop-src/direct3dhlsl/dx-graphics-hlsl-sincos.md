---
title: sincos
description: 傳回 x 的正弦和余弦。
ms.assetid: 2ef9e84e-4539-47f5-9966-d8e02ca15d36
keywords:
- sincos HLSL
topic_type:
- apiref
api_name:
- sincos
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8391c2fcecc939db1d7044fe56fbd281fe3e79fc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104990994"
---
# <a name="sincos"></a><span data-ttu-id="71c3e-104">sincos</span><span class="sxs-lookup"><span data-stu-id="71c3e-104">sincos</span></span>

<span data-ttu-id="71c3e-105">傳回 x 的正弦和余弦。</span><span class="sxs-lookup"><span data-stu-id="71c3e-105">Returns the sine and cosine of x.</span></span>



| <span data-ttu-id="71c3e-106">sincos (*x*、out *s*、out *c*) </span><span class="sxs-lookup"><span data-stu-id="71c3e-106">sincos(*x*, out *s*, out *c*)</span></span> |
|-------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="71c3e-107">參數</span><span class="sxs-lookup"><span data-stu-id="71c3e-107">Parameters</span></span>



| <span data-ttu-id="71c3e-108">項目</span><span class="sxs-lookup"><span data-stu-id="71c3e-108">Item</span></span>                                                   | <span data-ttu-id="71c3e-109">描述</span><span class="sxs-lookup"><span data-stu-id="71c3e-109">Description</span></span>                                        |
|--------------------------------------------------------|----------------------------------------------------|
| <span data-ttu-id="71c3e-110"><span id="x"></span><span id="X"></span>*X*</span><span class="sxs-lookup"><span data-stu-id="71c3e-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="71c3e-111">\[在 \] 指定的值中，以弧度為單位。</span><span class="sxs-lookup"><span data-stu-id="71c3e-111">\[in\] The specified value, in radians.</span></span><br/> |
| <span data-ttu-id="71c3e-112"><span id="s"></span><span id="S"></span>*！*</span><span class="sxs-lookup"><span data-stu-id="71c3e-112"><span id="s"></span><span id="S"></span>*s*</span></span><br/> | <span data-ttu-id="71c3e-113">\[out 會傳回 \] x 的正弦。</span><span class="sxs-lookup"><span data-stu-id="71c3e-113">\[out\] Returns the sine of x.</span></span><br/>          |
| <span data-ttu-id="71c3e-114"><span id="c"></span><span id="C"></span>*C*</span><span class="sxs-lookup"><span data-stu-id="71c3e-114"><span id="c"></span><span id="C"></span>*c*</span></span><br/> | <span data-ttu-id="71c3e-115">\[out 傳回 \] x 的余弦值。</span><span class="sxs-lookup"><span data-stu-id="71c3e-115">\[out\] Returns the cosine of x.</span></span><br/>        |



 

## <a name="return-value"></a><span data-ttu-id="71c3e-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="71c3e-116">Return Value</span></span>

<span data-ttu-id="71c3e-117">無。</span><span class="sxs-lookup"><span data-stu-id="71c3e-117">None.</span></span>

## <a name="type-description"></a><span data-ttu-id="71c3e-118">類型描述</span><span class="sxs-lookup"><span data-stu-id="71c3e-118">Type Description</span></span>



| <span data-ttu-id="71c3e-119">Name</span><span class="sxs-lookup"><span data-stu-id="71c3e-119">Name</span></span> | [<span data-ttu-id="71c3e-120">**範本類型**</span><span class="sxs-lookup"><span data-stu-id="71c3e-120">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="71c3e-121">**元件類型**</span><span class="sxs-lookup"><span data-stu-id="71c3e-121">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="71c3e-122">大小</span><span class="sxs-lookup"><span data-stu-id="71c3e-122">Size</span></span>                           |
|------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="71c3e-123">*x*</span><span class="sxs-lookup"><span data-stu-id="71c3e-123">*x*</span></span>  | <span data-ttu-id="71c3e-124">純 [**量、**](dx-graphics-hlsl-intrinsic-functions.md)**向量** 或 **矩陣**</span><span class="sxs-lookup"><span data-stu-id="71c3e-124">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="71c3e-125">**浮動**</span><span class="sxs-lookup"><span data-stu-id="71c3e-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="71c3e-126">任意</span><span class="sxs-lookup"><span data-stu-id="71c3e-126">any</span></span>                            |
| <span data-ttu-id="71c3e-127">*s*</span><span class="sxs-lookup"><span data-stu-id="71c3e-127">*s*</span></span>  | <span data-ttu-id="71c3e-128">與輸入 *x* 相同</span><span class="sxs-lookup"><span data-stu-id="71c3e-128">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="71c3e-129">**浮動**</span><span class="sxs-lookup"><span data-stu-id="71c3e-129">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="71c3e-130">) 為輸入 *x* 的相同維度 (s</span><span class="sxs-lookup"><span data-stu-id="71c3e-130">same dimension(s) as input *x*</span></span> |
| <span data-ttu-id="71c3e-131">c</span><span class="sxs-lookup"><span data-stu-id="71c3e-131">c</span></span>    | <span data-ttu-id="71c3e-132">與輸入 *x* 相同</span><span class="sxs-lookup"><span data-stu-id="71c3e-132">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="71c3e-133">**浮動**</span><span class="sxs-lookup"><span data-stu-id="71c3e-133">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="71c3e-134">) 為輸入 *x* 的相同維度 (s</span><span class="sxs-lookup"><span data-stu-id="71c3e-134">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="71c3e-135">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="71c3e-135">Minimum Shader Model</span></span>

<span data-ttu-id="71c3e-136">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="71c3e-136">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="71c3e-137">著色器模型</span><span class="sxs-lookup"><span data-stu-id="71c3e-137">Shader Model</span></span>                                                                       | <span data-ttu-id="71c3e-138">支援</span><span class="sxs-lookup"><span data-stu-id="71c3e-138">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="71c3e-139">[著色器模型 2 (DIRECTX HLSL) ](dx-graphics-hlsl-sm2.md) 和更高的著色器模型</span><span class="sxs-lookup"><span data-stu-id="71c3e-139">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="71c3e-140">是</span><span class="sxs-lookup"><span data-stu-id="71c3e-140">yes</span></span>                 |
| [<span data-ttu-id="71c3e-141">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="71c3e-141">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="71c3e-142">是 (\_ \_ 只有) 的 vs 1</span><span class="sxs-lookup"><span data-stu-id="71c3e-142">yes (vs\_1\_1 only)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="71c3e-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="71c3e-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71c3e-144">**(DirectX HLSL) 內建函式**</span><span class="sxs-lookup"><span data-stu-id="71c3e-144">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

