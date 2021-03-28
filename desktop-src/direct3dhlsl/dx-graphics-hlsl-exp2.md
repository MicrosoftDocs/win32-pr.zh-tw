---
title: 'exp2 (Corecrt \_ math .h) '
description: 傳回指定值的基底2指數或2x。
ms.assetid: 68b0057c-864d-440b-84f6-781d5fa3b019
keywords:
- exp2 HLSL
topic_type:
- apiref
api_name:
- exp2
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63aaf5ee7c29da49ca2e7b21d80af6967721058d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974501"
---
# <a name="exp2"></a><span data-ttu-id="25128-104">exp2</span><span class="sxs-lookup"><span data-stu-id="25128-104">exp2</span></span>

<span data-ttu-id="25128-105">傳回指定值的基底2指數或 2<sup>x</sup>。</span><span class="sxs-lookup"><span data-stu-id="25128-105">Returns the base 2 exponential, or 2<sup>x</sup>, of the specified value.</span></span>



| <span data-ttu-id="25128-106">*ret* exp2 (*x*) </span><span class="sxs-lookup"><span data-stu-id="25128-106">*ret* exp2(*x*)</span></span> |
|-----------------|



 

## <a name="parameters"></a><span data-ttu-id="25128-107">參數</span><span class="sxs-lookup"><span data-stu-id="25128-107">Parameters</span></span>



| <span data-ttu-id="25128-108">項目</span><span class="sxs-lookup"><span data-stu-id="25128-108">Item</span></span>                                                   | <span data-ttu-id="25128-109">描述</span><span class="sxs-lookup"><span data-stu-id="25128-109">Description</span></span>                                           |
|--------------------------------------------------------|-------------------------------------------------------|
| <span data-ttu-id="25128-110"><span id="x"></span><span id="X"></span>*X*</span><span class="sxs-lookup"><span data-stu-id="25128-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="25128-111">\[在 \] 指定的浮點值中。</span><span class="sxs-lookup"><span data-stu-id="25128-111">\[in\] The specified floating-point value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="25128-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="25128-112">Return Value</span></span>

<span data-ttu-id="25128-113">*X* 參數的基底2指數。</span><span class="sxs-lookup"><span data-stu-id="25128-113">The base 2 exponential of the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="25128-114">類型描述</span><span class="sxs-lookup"><span data-stu-id="25128-114">Type Description</span></span>



| <span data-ttu-id="25128-115">Name</span><span class="sxs-lookup"><span data-stu-id="25128-115">Name</span></span>  | [<span data-ttu-id="25128-116">**範本類型**</span><span class="sxs-lookup"><span data-stu-id="25128-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="25128-117">**元件類型**</span><span class="sxs-lookup"><span data-stu-id="25128-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="25128-118">大小</span><span class="sxs-lookup"><span data-stu-id="25128-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="25128-119">*x*</span><span class="sxs-lookup"><span data-stu-id="25128-119">*x*</span></span>   | <span data-ttu-id="25128-120">純 [**量、**](dx-graphics-hlsl-intrinsic-functions.md)**向量** 或 **矩陣**</span><span class="sxs-lookup"><span data-stu-id="25128-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="25128-121">**浮動**</span><span class="sxs-lookup"><span data-stu-id="25128-121">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="25128-122">任意</span><span class="sxs-lookup"><span data-stu-id="25128-122">any</span></span>                            |
| <span data-ttu-id="25128-123">*Ret*</span><span class="sxs-lookup"><span data-stu-id="25128-123">*ret*</span></span> | <span data-ttu-id="25128-124">與輸入 *x* 相同</span><span class="sxs-lookup"><span data-stu-id="25128-124">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="25128-125">**浮動**</span><span class="sxs-lookup"><span data-stu-id="25128-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="25128-126">) 為輸入 *x* 的相同維度 (s</span><span class="sxs-lookup"><span data-stu-id="25128-126">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="25128-127">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="25128-127">Minimum Shader Model</span></span>

<span data-ttu-id="25128-128">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="25128-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="25128-129">著色器模型</span><span class="sxs-lookup"><span data-stu-id="25128-129">Shader Model</span></span>                                                                       | <span data-ttu-id="25128-130">支援</span><span class="sxs-lookup"><span data-stu-id="25128-130">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="25128-131">[著色器模型 2 (DIRECTX HLSL) ](dx-graphics-hlsl-sm2.md) 和更高的著色器模型</span><span class="sxs-lookup"><span data-stu-id="25128-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="25128-132">是</span><span class="sxs-lookup"><span data-stu-id="25128-132">yes</span></span>       |
| [<span data-ttu-id="25128-133">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="25128-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="25128-134">vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="25128-134">vs\_1\_1</span></span>  |



 

## <a name="requirements"></a><span data-ttu-id="25128-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="25128-135">Requirements</span></span>



| <span data-ttu-id="25128-136">需求</span><span class="sxs-lookup"><span data-stu-id="25128-136">Requirement</span></span> | <span data-ttu-id="25128-137">值</span><span class="sxs-lookup"><span data-stu-id="25128-137">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="25128-138">標頭</span><span class="sxs-lookup"><span data-stu-id="25128-138">Header</span></span><br/> | <dl> <span data-ttu-id="25128-139"><dt>Corecrt \_ math。h</dt></span><span class="sxs-lookup"><span data-stu-id="25128-139"><dt>Corecrt\_math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25128-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="25128-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25128-141">**(DirectX HLSL) 內建函式**</span><span class="sxs-lookup"><span data-stu-id="25128-141">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

