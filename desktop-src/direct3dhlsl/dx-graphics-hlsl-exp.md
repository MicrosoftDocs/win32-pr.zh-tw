---
title: exp
description: 傳回指定值的底數-e 指數或例如。
ms.assetid: 7a713251-af47-4f8d-b708-40309b80ba18
keywords:
- exp HLSL
topic_type:
- apiref
api_name:
- exp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 699eb97ae0fd6bbdeba0da47693178d1e4c48e36
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682497"
---
# <a name="exp"></a><span data-ttu-id="dd821-104">exp</span><span class="sxs-lookup"><span data-stu-id="dd821-104">exp</span></span>

<span data-ttu-id="dd821-105">傳回指定值的底數-e 指數或 e<sup>x</sup>。</span><span class="sxs-lookup"><span data-stu-id="dd821-105">Returns the base-e exponential, or e<sup>x</sup>, of the specified value.</span></span>



| <span data-ttu-id="dd821-106">*ret* exp (*x*) </span><span class="sxs-lookup"><span data-stu-id="dd821-106">*ret* exp(*x*)</span></span> |
|----------------|



 

## <a name="parameters"></a><span data-ttu-id="dd821-107">參數</span><span class="sxs-lookup"><span data-stu-id="dd821-107">Parameters</span></span>



| <span data-ttu-id="dd821-108">項目</span><span class="sxs-lookup"><span data-stu-id="dd821-108">Item</span></span>                                                   | <span data-ttu-id="dd821-109">描述</span><span class="sxs-lookup"><span data-stu-id="dd821-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="dd821-110"><span id="x"></span><span id="X"></span>*X*</span><span class="sxs-lookup"><span data-stu-id="dd821-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="dd821-111">\[在 \] 指定的值中。</span><span class="sxs-lookup"><span data-stu-id="dd821-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="dd821-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="dd821-112">Return Value</span></span>

<span data-ttu-id="dd821-113">*X* 參數的底數-e 指數。</span><span class="sxs-lookup"><span data-stu-id="dd821-113">The base-e exponential of the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="dd821-114">類型描述</span><span class="sxs-lookup"><span data-stu-id="dd821-114">Type Description</span></span>



| <span data-ttu-id="dd821-115">Name</span><span class="sxs-lookup"><span data-stu-id="dd821-115">Name</span></span>  | [<span data-ttu-id="dd821-116">**範本類型**</span><span class="sxs-lookup"><span data-stu-id="dd821-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="dd821-117">**元件類型**</span><span class="sxs-lookup"><span data-stu-id="dd821-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="dd821-118">大小</span><span class="sxs-lookup"><span data-stu-id="dd821-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="dd821-119">*x*</span><span class="sxs-lookup"><span data-stu-id="dd821-119">*x*</span></span>   | <span data-ttu-id="dd821-120">純 [**量、**](dx-graphics-hlsl-intrinsic-functions.md)**向量** 或 **矩陣**</span><span class="sxs-lookup"><span data-stu-id="dd821-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="dd821-121">**浮動**</span><span class="sxs-lookup"><span data-stu-id="dd821-121">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="dd821-122">任意</span><span class="sxs-lookup"><span data-stu-id="dd821-122">any</span></span>                            |
| <span data-ttu-id="dd821-123">*Ret*</span><span class="sxs-lookup"><span data-stu-id="dd821-123">*ret*</span></span> | <span data-ttu-id="dd821-124">與輸入 *x* 相同</span><span class="sxs-lookup"><span data-stu-id="dd821-124">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="dd821-125">**浮動**</span><span class="sxs-lookup"><span data-stu-id="dd821-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="dd821-126">) 為輸入 *x* 的相同維度 (s</span><span class="sxs-lookup"><span data-stu-id="dd821-126">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="dd821-127">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="dd821-127">Minimum Shader Model</span></span>

<span data-ttu-id="dd821-128">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="dd821-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="dd821-129">著色器模型</span><span class="sxs-lookup"><span data-stu-id="dd821-129">Shader Model</span></span>                                                                       | <span data-ttu-id="dd821-130">支援</span><span class="sxs-lookup"><span data-stu-id="dd821-130">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="dd821-131">[著色器模型 2 (DIRECTX HLSL) ](dx-graphics-hlsl-sm2.md) 和更高的著色器模型</span><span class="sxs-lookup"><span data-stu-id="dd821-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="dd821-132">是</span><span class="sxs-lookup"><span data-stu-id="dd821-132">yes</span></span>       |
| [<span data-ttu-id="dd821-133">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="dd821-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="dd821-134">vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="dd821-134">vs\_1\_1</span></span>  |



 

## <a name="see-also"></a><span data-ttu-id="dd821-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dd821-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd821-136">**(DirectX HLSL) 內建函式**</span><span class="sxs-lookup"><span data-stu-id="dd821-136">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

