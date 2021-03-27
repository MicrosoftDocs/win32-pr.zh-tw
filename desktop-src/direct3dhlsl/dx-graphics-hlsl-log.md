---
title: log
description: 傳回指定之值的以 e 為底數的對數。
ms.assetid: 443e7aa7-7219-40ad-aafc-4bce09c8f596
keywords:
- 記錄 HLSL
topic_type:
- apiref
api_name:
- log
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0cdd08fe178925406145476b3250e8d256b263c3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682823"
---
# <a name="log"></a><span data-ttu-id="e28c3-104">log</span><span class="sxs-lookup"><span data-stu-id="e28c3-104">log</span></span>

<span data-ttu-id="e28c3-105">傳回指定之值的以 e 為底數的對數。</span><span class="sxs-lookup"><span data-stu-id="e28c3-105">Returns the base-e logarithm of the specified value.</span></span>



| <span data-ttu-id="e28c3-106">*ret* 記錄 (*x*) </span><span class="sxs-lookup"><span data-stu-id="e28c3-106">*ret* log(*x*)</span></span> |
|----------------|



 

## <a name="parameters"></a><span data-ttu-id="e28c3-107">參數</span><span class="sxs-lookup"><span data-stu-id="e28c3-107">Parameters</span></span>



| <span data-ttu-id="e28c3-108">項目</span><span class="sxs-lookup"><span data-stu-id="e28c3-108">Item</span></span>                                                   | <span data-ttu-id="e28c3-109">描述</span><span class="sxs-lookup"><span data-stu-id="e28c3-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="e28c3-110"><span id="x"></span><span id="X"></span>*X*</span><span class="sxs-lookup"><span data-stu-id="e28c3-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="e28c3-111">\[在 \] 指定的值中。</span><span class="sxs-lookup"><span data-stu-id="e28c3-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="e28c3-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="e28c3-112">Return Value</span></span>

<span data-ttu-id="e28c3-113">*X* 參數的以 e 為底數的對數。</span><span class="sxs-lookup"><span data-stu-id="e28c3-113">The base-e logarithm of the *x* parameter.</span></span> <span data-ttu-id="e28c3-114">如果 *x* 參數為負值，則此函式會傳回不定。</span><span class="sxs-lookup"><span data-stu-id="e28c3-114">If the *x* parameter is negative, this function returns indefinite.</span></span> <span data-ttu-id="e28c3-115">如果 *x* 參數為0，則此函式會傳回-INF。</span><span class="sxs-lookup"><span data-stu-id="e28c3-115">If the *x* parameter is 0, this function returns -INF.</span></span>

## <a name="type-description"></a><span data-ttu-id="e28c3-116">類型描述</span><span class="sxs-lookup"><span data-stu-id="e28c3-116">Type Description</span></span>



| <span data-ttu-id="e28c3-117">名稱</span><span class="sxs-lookup"><span data-stu-id="e28c3-117">Name</span></span>  | [<span data-ttu-id="e28c3-118">**範本類型**</span><span class="sxs-lookup"><span data-stu-id="e28c3-118">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="e28c3-119">**元件類型**</span><span class="sxs-lookup"><span data-stu-id="e28c3-119">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="e28c3-120">大小</span><span class="sxs-lookup"><span data-stu-id="e28c3-120">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="e28c3-121">*x*</span><span class="sxs-lookup"><span data-stu-id="e28c3-121">*x*</span></span>   | <span data-ttu-id="e28c3-122">純 [**量、**](dx-graphics-hlsl-intrinsic-functions.md)**向量** 或 **矩陣**</span><span class="sxs-lookup"><span data-stu-id="e28c3-122">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="e28c3-123">**浮動**</span><span class="sxs-lookup"><span data-stu-id="e28c3-123">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="e28c3-124">任意</span><span class="sxs-lookup"><span data-stu-id="e28c3-124">any</span></span>                            |
| <span data-ttu-id="e28c3-125">*Ret*</span><span class="sxs-lookup"><span data-stu-id="e28c3-125">*ret*</span></span> | <span data-ttu-id="e28c3-126">與輸入 *x* 相同</span><span class="sxs-lookup"><span data-stu-id="e28c3-126">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="e28c3-127">**浮動**</span><span class="sxs-lookup"><span data-stu-id="e28c3-127">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="e28c3-128">) 為輸入 *x* 的相同維度 (s</span><span class="sxs-lookup"><span data-stu-id="e28c3-128">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="e28c3-129">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="e28c3-129">Minimum Shader Model</span></span>

<span data-ttu-id="e28c3-130">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="e28c3-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="e28c3-131">著色器模型</span><span class="sxs-lookup"><span data-stu-id="e28c3-131">Shader Model</span></span>                                                                       | <span data-ttu-id="e28c3-132">支援</span><span class="sxs-lookup"><span data-stu-id="e28c3-132">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="e28c3-133">[著色器模型 2 (DIRECTX HLSL) ](dx-graphics-hlsl-sm2.md) 和更高的著色器模型</span><span class="sxs-lookup"><span data-stu-id="e28c3-133">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="e28c3-134">是</span><span class="sxs-lookup"><span data-stu-id="e28c3-134">yes</span></span>                 |
| [<span data-ttu-id="e28c3-135">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="e28c3-135">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="e28c3-136">是 (\_ \_ 只有) 的 vs 1</span><span class="sxs-lookup"><span data-stu-id="e28c3-136">yes (vs\_1\_1 only)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="e28c3-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e28c3-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e28c3-138">**(DirectX HLSL) 內建函式**</span><span class="sxs-lookup"><span data-stu-id="e28c3-138">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

