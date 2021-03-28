---
title: 弧度
description: 將指定的值從度數轉換成弧度。
ms.assetid: 6fc6b1f8-b686-49ba-93ea-2b2470b3fc72
keywords:
- 弧度 HLSL
topic_type:
- apiref
api_name:
- radians
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 029c0ffe2838cdcc997e47cae4e0adafede4411d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382749"
---
# <a name="radians"></a><span data-ttu-id="d380c-104">弧度</span><span class="sxs-lookup"><span data-stu-id="d380c-104">radians</span></span>

<span data-ttu-id="d380c-105">將指定的值從度數轉換成弧度。</span><span class="sxs-lookup"><span data-stu-id="d380c-105">Converts the specified value from degrees to radians.</span></span>



| <span data-ttu-id="d380c-106">*ret* 弧度 (*x*) </span><span class="sxs-lookup"><span data-stu-id="d380c-106">*ret* radians(*x*)</span></span> |
|--------------------|



 

## <a name="parameters"></a><span data-ttu-id="d380c-107">參數</span><span class="sxs-lookup"><span data-stu-id="d380c-107">Parameters</span></span>



| <span data-ttu-id="d380c-108">項目</span><span class="sxs-lookup"><span data-stu-id="d380c-108">Item</span></span>                                                   | <span data-ttu-id="d380c-109">描述</span><span class="sxs-lookup"><span data-stu-id="d380c-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="d380c-110"><span id="x"></span><span id="X"></span>*X*</span><span class="sxs-lookup"><span data-stu-id="d380c-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="d380c-111">\[在 \] 指定的值中。</span><span class="sxs-lookup"><span data-stu-id="d380c-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="d380c-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="d380c-112">Return Value</span></span>

<span data-ttu-id="d380c-113">從度數轉換成弧度的 *x* 參數。</span><span class="sxs-lookup"><span data-stu-id="d380c-113">The *x* parameter converted from degrees to radians.</span></span>

## <a name="type-description"></a><span data-ttu-id="d380c-114">類型描述</span><span class="sxs-lookup"><span data-stu-id="d380c-114">Type Description</span></span>



| <span data-ttu-id="d380c-115">Name</span><span class="sxs-lookup"><span data-stu-id="d380c-115">Name</span></span>  | [<span data-ttu-id="d380c-116">**範本類型**</span><span class="sxs-lookup"><span data-stu-id="d380c-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="d380c-117">**元件類型**</span><span class="sxs-lookup"><span data-stu-id="d380c-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="d380c-118">大小</span><span class="sxs-lookup"><span data-stu-id="d380c-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="d380c-119">*x*</span><span class="sxs-lookup"><span data-stu-id="d380c-119">*x*</span></span>   | <span data-ttu-id="d380c-120">純 [**量、**](dx-graphics-hlsl-intrinsic-functions.md)**向量** 或 **矩陣**</span><span class="sxs-lookup"><span data-stu-id="d380c-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="d380c-121">**浮動**</span><span class="sxs-lookup"><span data-stu-id="d380c-121">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="d380c-122">任意</span><span class="sxs-lookup"><span data-stu-id="d380c-122">any</span></span>                            |
| <span data-ttu-id="d380c-123">*Ret*</span><span class="sxs-lookup"><span data-stu-id="d380c-123">*ret*</span></span> | <span data-ttu-id="d380c-124">與輸入 *x* 相同</span><span class="sxs-lookup"><span data-stu-id="d380c-124">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="d380c-125">**浮動**</span><span class="sxs-lookup"><span data-stu-id="d380c-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="d380c-126">) 為輸入 *x* 的相同維度 (s</span><span class="sxs-lookup"><span data-stu-id="d380c-126">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="d380c-127">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="d380c-127">Minimum Shader Model</span></span>

<span data-ttu-id="d380c-128">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="d380c-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="d380c-129">著色器模型</span><span class="sxs-lookup"><span data-stu-id="d380c-129">Shader Model</span></span>                                                                       | <span data-ttu-id="d380c-130">支援</span><span class="sxs-lookup"><span data-stu-id="d380c-130">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="d380c-131">[著色器模型 1 (DIRECTX HLSL) ](dx-graphics-hlsl-sm1.md) 和更高的著色器模型</span><span class="sxs-lookup"><span data-stu-id="d380c-131">[Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) and higher shader models</span></span> | <span data-ttu-id="d380c-132">是</span><span class="sxs-lookup"><span data-stu-id="d380c-132">yes</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="d380c-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d380c-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d380c-134">**(DirectX HLSL) 內建函式**</span><span class="sxs-lookup"><span data-stu-id="d380c-134">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

