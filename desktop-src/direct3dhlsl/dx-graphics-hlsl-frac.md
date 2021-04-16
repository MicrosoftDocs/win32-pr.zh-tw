---
title: 壓裂
description: 傳回 x 的小數 (或小數) 部分;大於或等於0且小於1。
ms.assetid: 4e85390f-2b1a-402b-b932-09b80097f7e6
keywords:
- frac HLSL
topic_type:
- apiref
api_name:
- frac
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 468bddc34f22f9bb5f34871102678e1765148b11
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463641"
---
# <a name="frac"></a><span data-ttu-id="9ffb3-104">壓裂</span><span class="sxs-lookup"><span data-stu-id="9ffb3-104">frac</span></span>

<span data-ttu-id="9ffb3-105">傳回 x 的小數 (或小數) 部分;大於或等於0且小於1。</span><span class="sxs-lookup"><span data-stu-id="9ffb3-105">Returns the fractional (or decimal) part of x; which is greater than or equal to 0 and less than 1.</span></span>

<span data-ttu-id="9ffb3-106">另請參閱 [trunc](./dx-graphics-hlsl-trunc.md)。</span><span class="sxs-lookup"><span data-stu-id="9ffb3-106">Also see [trunc](./dx-graphics-hlsl-trunc.md).</span></span>

| <span data-ttu-id="9ffb3-107">*ret* frac (*x*) </span><span class="sxs-lookup"><span data-stu-id="9ffb3-107">*ret* frac(*x*)</span></span> |
|-----------------|



 

## <a name="parameters"></a><span data-ttu-id="9ffb3-108">參數</span><span class="sxs-lookup"><span data-stu-id="9ffb3-108">Parameters</span></span>



| <span data-ttu-id="9ffb3-109">項目</span><span class="sxs-lookup"><span data-stu-id="9ffb3-109">Item</span></span>                                                   | <span data-ttu-id="9ffb3-110">描述</span><span class="sxs-lookup"><span data-stu-id="9ffb3-110">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="9ffb3-111"><span id="x"></span><span id="X"></span>*X*</span><span class="sxs-lookup"><span data-stu-id="9ffb3-111"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="9ffb3-112">\[在 \] 指定的值中。</span><span class="sxs-lookup"><span data-stu-id="9ffb3-112">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="9ffb3-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="9ffb3-113">Return Value</span></span>

<span data-ttu-id="9ffb3-114">*X* 參數的小數部分。</span><span class="sxs-lookup"><span data-stu-id="9ffb3-114">The fractional part of the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="9ffb3-115">類型描述</span><span class="sxs-lookup"><span data-stu-id="9ffb3-115">Type Description</span></span>



| <span data-ttu-id="9ffb3-116">Name</span><span class="sxs-lookup"><span data-stu-id="9ffb3-116">Name</span></span>  | [<span data-ttu-id="9ffb3-117">**範本類型**</span><span class="sxs-lookup"><span data-stu-id="9ffb3-117">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="9ffb3-118">**元件類型**</span><span class="sxs-lookup"><span data-stu-id="9ffb3-118">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="9ffb3-119">大小</span><span class="sxs-lookup"><span data-stu-id="9ffb3-119">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="9ffb3-120">*x*</span><span class="sxs-lookup"><span data-stu-id="9ffb3-120">*x*</span></span>   | <span data-ttu-id="9ffb3-121">純 [**量、**](dx-graphics-hlsl-intrinsic-functions.md)**向量** 或 **矩陣**</span><span class="sxs-lookup"><span data-stu-id="9ffb3-121">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="9ffb3-122">**浮動**</span><span class="sxs-lookup"><span data-stu-id="9ffb3-122">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="9ffb3-123">任意</span><span class="sxs-lookup"><span data-stu-id="9ffb3-123">any</span></span>                            |
| <span data-ttu-id="9ffb3-124">*Ret*</span><span class="sxs-lookup"><span data-stu-id="9ffb3-124">*ret*</span></span> | <span data-ttu-id="9ffb3-125">與輸入 *x* 相同</span><span class="sxs-lookup"><span data-stu-id="9ffb3-125">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="9ffb3-126">**浮動**</span><span class="sxs-lookup"><span data-stu-id="9ffb3-126">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="9ffb3-127">) 為輸入 *x* 的相同維度 (s</span><span class="sxs-lookup"><span data-stu-id="9ffb3-127">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="9ffb3-128">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="9ffb3-128">Minimum Shader Model</span></span>

<span data-ttu-id="9ffb3-129">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="9ffb3-129">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="9ffb3-130">著色器模型</span><span class="sxs-lookup"><span data-stu-id="9ffb3-130">Shader Model</span></span>                                                                       | <span data-ttu-id="9ffb3-131">支援</span><span class="sxs-lookup"><span data-stu-id="9ffb3-131">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="9ffb3-132">[著色器模型 2 (DIRECTX HLSL) ](dx-graphics-hlsl-sm2.md) 和更高的著色器模型</span><span class="sxs-lookup"><span data-stu-id="9ffb3-132">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="9ffb3-133">是</span><span class="sxs-lookup"><span data-stu-id="9ffb3-133">yes</span></span>       |
| [<span data-ttu-id="9ffb3-134">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="9ffb3-134">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="9ffb3-135">vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="9ffb3-135">vs\_1\_1</span></span>  |



 

## <a name="see-also"></a><span data-ttu-id="9ffb3-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9ffb3-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ffb3-137">**(DirectX HLSL) 內建函式**</span><span class="sxs-lookup"><span data-stu-id="9ffb3-137">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

