---
title: log10
description: 傳回指定值的以10為底數的對數。
ms.assetid: a94f8438-8153-4a31-bde3-98831edf99e5
keywords:
- log10 HLSL
topic_type:
- apiref
api_name:
- log10
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2d226dcc33da1aee6d55e21c6d97febc23577503
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315979"
---
# <a name="log10"></a><span data-ttu-id="6f446-104">log10</span><span class="sxs-lookup"><span data-stu-id="6f446-104">log10</span></span>

<span data-ttu-id="6f446-105">傳回指定值的以10為底數的對數。</span><span class="sxs-lookup"><span data-stu-id="6f446-105">Returns the base-10 logarithm of the specified value.</span></span>



| <span data-ttu-id="6f446-106">*ret* log10 (*x*) </span><span class="sxs-lookup"><span data-stu-id="6f446-106">*ret* log10(*x*)</span></span> |
|------------------|



 

## <a name="parameters"></a><span data-ttu-id="6f446-107">參數</span><span class="sxs-lookup"><span data-stu-id="6f446-107">Parameters</span></span>



| <span data-ttu-id="6f446-108">項目</span><span class="sxs-lookup"><span data-stu-id="6f446-108">Item</span></span>                                                   | <span data-ttu-id="6f446-109">描述</span><span class="sxs-lookup"><span data-stu-id="6f446-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="6f446-110"><span id="x"></span><span id="X"></span>*X*</span><span class="sxs-lookup"><span data-stu-id="6f446-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="6f446-111">\[在 \] 指定的值中。</span><span class="sxs-lookup"><span data-stu-id="6f446-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="6f446-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="6f446-112">Return Value</span></span>

<span data-ttu-id="6f446-113">*X* 參數以10為底數的對數。</span><span class="sxs-lookup"><span data-stu-id="6f446-113">The base-10 logarithm of the *x* parameter.</span></span> <span data-ttu-id="6f446-114">如果 *x* 參數為負值，則此函式會傳回不定。</span><span class="sxs-lookup"><span data-stu-id="6f446-114">If the *x* parameter is negative, this function returns indefinite.</span></span> <span data-ttu-id="6f446-115">如果 *x* 是0，則此函式會傳回-INF。</span><span class="sxs-lookup"><span data-stu-id="6f446-115">If the *x* is 0, this function returns -INF.</span></span>

## <a name="type-description"></a><span data-ttu-id="6f446-116">類型描述</span><span class="sxs-lookup"><span data-stu-id="6f446-116">Type Description</span></span>



| <span data-ttu-id="6f446-117">Name</span><span class="sxs-lookup"><span data-stu-id="6f446-117">Name</span></span>  | [<span data-ttu-id="6f446-118">**範本類型**</span><span class="sxs-lookup"><span data-stu-id="6f446-118">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="6f446-119">**元件類型**</span><span class="sxs-lookup"><span data-stu-id="6f446-119">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="6f446-120">大小</span><span class="sxs-lookup"><span data-stu-id="6f446-120">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="6f446-121">*x*</span><span class="sxs-lookup"><span data-stu-id="6f446-121">*x*</span></span>   | <span data-ttu-id="6f446-122">純 [**量、**](dx-graphics-hlsl-intrinsic-functions.md)**向量** 或 **矩陣**</span><span class="sxs-lookup"><span data-stu-id="6f446-122">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="6f446-123">**浮動**</span><span class="sxs-lookup"><span data-stu-id="6f446-123">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="6f446-124">任意</span><span class="sxs-lookup"><span data-stu-id="6f446-124">any</span></span>                            |
| <span data-ttu-id="6f446-125">*Ret*</span><span class="sxs-lookup"><span data-stu-id="6f446-125">*ret*</span></span> | <span data-ttu-id="6f446-126">與輸入 *x* 相同</span><span class="sxs-lookup"><span data-stu-id="6f446-126">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="6f446-127">**浮動**</span><span class="sxs-lookup"><span data-stu-id="6f446-127">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="6f446-128">) 為輸入 *x* 的相同維度 (s</span><span class="sxs-lookup"><span data-stu-id="6f446-128">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="6f446-129">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="6f446-129">Minimum Shader Model</span></span>

<span data-ttu-id="6f446-130">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="6f446-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="6f446-131">著色器模型</span><span class="sxs-lookup"><span data-stu-id="6f446-131">Shader Model</span></span>                                                                       | <span data-ttu-id="6f446-132">支援</span><span class="sxs-lookup"><span data-stu-id="6f446-132">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="6f446-133">[著色器模型 2 (DIRECTX HLSL) ](dx-graphics-hlsl-sm2.md) 和更高的著色器模型</span><span class="sxs-lookup"><span data-stu-id="6f446-133">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="6f446-134">是</span><span class="sxs-lookup"><span data-stu-id="6f446-134">yes</span></span>                 |
| [<span data-ttu-id="6f446-135">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="6f446-135">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="6f446-136">是 (\_ \_ 只有) 的 vs 1</span><span class="sxs-lookup"><span data-stu-id="6f446-136">yes (vs\_1\_1 only)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="6f446-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6f446-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f446-138">**(DirectX HLSL) 內建函式**</span><span class="sxs-lookup"><span data-stu-id="6f446-138">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

