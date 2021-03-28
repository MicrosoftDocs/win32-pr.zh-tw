---
title: asin
description: 傳回指定之值的反正弦值。
ms.assetid: 49559cb2-3305-4c97-8071-1589bcca3a75
keywords:
- asin HLSL
topic_type:
- apiref
api_name:
- asin
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a2f64865cb3172037f6630dc422a69aa4d135b1d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104024032"
---
# <a name="asin"></a><span data-ttu-id="76a70-104">asin</span><span class="sxs-lookup"><span data-stu-id="76a70-104">asin</span></span>

<span data-ttu-id="76a70-105">傳回指定之值的反正弦值。</span><span class="sxs-lookup"><span data-stu-id="76a70-105">Returns the arcsine of the specified value.</span></span>



| <span data-ttu-id="76a70-106">*ret* asin (*x*) </span><span class="sxs-lookup"><span data-stu-id="76a70-106">*ret* asin(*x*)</span></span> |
|-----------------|



 

## <a name="parameters"></a><span data-ttu-id="76a70-107">參數</span><span class="sxs-lookup"><span data-stu-id="76a70-107">Parameters</span></span>



| <span data-ttu-id="76a70-108">項目</span><span class="sxs-lookup"><span data-stu-id="76a70-108">Item</span></span>                                                   | <span data-ttu-id="76a70-109">描述</span><span class="sxs-lookup"><span data-stu-id="76a70-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="76a70-110"><span id="x"></span><span id="X"></span>*X*</span><span class="sxs-lookup"><span data-stu-id="76a70-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="76a70-111">\[在 \] 指定的值中。</span><span class="sxs-lookup"><span data-stu-id="76a70-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="76a70-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="76a70-112">Return Value</span></span>

<span data-ttu-id="76a70-113">*X* 參數的反正弦。</span><span class="sxs-lookup"><span data-stu-id="76a70-113">The arcsine of the *x* parameter.</span></span>

## <a name="remarks"></a><span data-ttu-id="76a70-114">備註</span><span class="sxs-lookup"><span data-stu-id="76a70-114">Remarks</span></span>

<span data-ttu-id="76a70-115">*X* 參數的每個元件都應該在-π/2 到π/2 的範圍內。</span><span class="sxs-lookup"><span data-stu-id="76a70-115">Each component of the *x* parameter should be within the range of -π/2 to π/2.</span></span>

## <a name="type-description"></a><span data-ttu-id="76a70-116">類型描述</span><span class="sxs-lookup"><span data-stu-id="76a70-116">Type Description</span></span>



| <span data-ttu-id="76a70-117">Name</span><span class="sxs-lookup"><span data-stu-id="76a70-117">Name</span></span>  | [<span data-ttu-id="76a70-118">**範本類型**</span><span class="sxs-lookup"><span data-stu-id="76a70-118">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="76a70-119">**元件類型**</span><span class="sxs-lookup"><span data-stu-id="76a70-119">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="76a70-120">大小</span><span class="sxs-lookup"><span data-stu-id="76a70-120">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="76a70-121">*x*</span><span class="sxs-lookup"><span data-stu-id="76a70-121">*x*</span></span>   | <span data-ttu-id="76a70-122">純 [**量、**](dx-graphics-hlsl-intrinsic-functions.md)**向量** 或 **矩陣**</span><span class="sxs-lookup"><span data-stu-id="76a70-122">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="76a70-123">**浮動**</span><span class="sxs-lookup"><span data-stu-id="76a70-123">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="76a70-124">任意</span><span class="sxs-lookup"><span data-stu-id="76a70-124">any</span></span>                            |
| <span data-ttu-id="76a70-125">*Ret*</span><span class="sxs-lookup"><span data-stu-id="76a70-125">*ret*</span></span> | <span data-ttu-id="76a70-126">與輸入 *x* 相同</span><span class="sxs-lookup"><span data-stu-id="76a70-126">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="76a70-127">**浮動**</span><span class="sxs-lookup"><span data-stu-id="76a70-127">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="76a70-128">) 為輸入 *x* 的相同維度 (s</span><span class="sxs-lookup"><span data-stu-id="76a70-128">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="76a70-129">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="76a70-129">Minimum Shader Model</span></span>

<span data-ttu-id="76a70-130">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="76a70-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="76a70-131">著色器模型</span><span class="sxs-lookup"><span data-stu-id="76a70-131">Shader Model</span></span>                                                                       | <span data-ttu-id="76a70-132">支援</span><span class="sxs-lookup"><span data-stu-id="76a70-132">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="76a70-133">[著色器模型 2 (DIRECTX HLSL) ](dx-graphics-hlsl-sm2.md) 和更高的著色器模型</span><span class="sxs-lookup"><span data-stu-id="76a70-133">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="76a70-134">是</span><span class="sxs-lookup"><span data-stu-id="76a70-134">yes</span></span>       |
| [<span data-ttu-id="76a70-135">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="76a70-135">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="76a70-136">vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="76a70-136">vs\_1\_1</span></span>  |



 

## <a name="see-also"></a><span data-ttu-id="76a70-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="76a70-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76a70-138">**(DirectX HLSL) 內建函式**</span><span class="sxs-lookup"><span data-stu-id="76a70-138">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

