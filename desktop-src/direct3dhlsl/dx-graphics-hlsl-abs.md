---
title: abs
description: 傳回指定之值的絕對值。
ms.assetid: 8c4cfd8f-8aac-4db3-8247-ce2bbf501e80
keywords:
- abs HLSL
topic_type:
- apiref
api_name:
- abs
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1acd1903e1a65a38f5af7549ab52577bc6cba51c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104971769"
---
# <a name="abs"></a><span data-ttu-id="1923e-104">abs</span><span class="sxs-lookup"><span data-stu-id="1923e-104">abs</span></span>

<span data-ttu-id="1923e-105">傳回指定之值的絕對值。</span><span class="sxs-lookup"><span data-stu-id="1923e-105">Returns the absolute value of the specified value.</span></span>



| <span data-ttu-id="1923e-106">ret abs (*x*) </span><span class="sxs-lookup"><span data-stu-id="1923e-106">ret abs(*x*)</span></span> |
|--------------|



 

## <a name="parameters"></a><span data-ttu-id="1923e-107">參數</span><span class="sxs-lookup"><span data-stu-id="1923e-107">Parameters</span></span>



| <span data-ttu-id="1923e-108">項目</span><span class="sxs-lookup"><span data-stu-id="1923e-108">Item</span></span>                                                   | <span data-ttu-id="1923e-109">描述</span><span class="sxs-lookup"><span data-stu-id="1923e-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="1923e-110"><span id="x"></span><span id="X"></span>*X*</span><span class="sxs-lookup"><span data-stu-id="1923e-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="1923e-111">\[在 \] 指定的值中。</span><span class="sxs-lookup"><span data-stu-id="1923e-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="1923e-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="1923e-112">Return Value</span></span>

<span data-ttu-id="1923e-113">*X* 參數的絕對值。</span><span class="sxs-lookup"><span data-stu-id="1923e-113">The absolute value of the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="1923e-114">類型描述</span><span class="sxs-lookup"><span data-stu-id="1923e-114">Type Description</span></span>



| <span data-ttu-id="1923e-115">Name</span><span class="sxs-lookup"><span data-stu-id="1923e-115">Name</span></span>  | [<span data-ttu-id="1923e-116">**範本類型**</span><span class="sxs-lookup"><span data-stu-id="1923e-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="1923e-117">**元件類型**</span><span class="sxs-lookup"><span data-stu-id="1923e-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                 | <span data-ttu-id="1923e-118">大小</span><span class="sxs-lookup"><span data-stu-id="1923e-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="1923e-119">*x*</span><span class="sxs-lookup"><span data-stu-id="1923e-119">*x*</span></span>   | <span data-ttu-id="1923e-120">純 [**量、**](dx-graphics-hlsl-intrinsic-functions.md)**向量** 或 **矩陣**</span><span class="sxs-lookup"><span data-stu-id="1923e-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | <span data-ttu-id="1923e-121">[**float**](/windows/desktop/WinProg/windows-data-types)、 [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="1923e-121">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="1923e-122">任意</span><span class="sxs-lookup"><span data-stu-id="1923e-122">any</span></span>                            |
| <span data-ttu-id="1923e-123">*Ret*</span><span class="sxs-lookup"><span data-stu-id="1923e-123">*ret*</span></span> | <span data-ttu-id="1923e-124">與輸入 *x* 相同</span><span class="sxs-lookup"><span data-stu-id="1923e-124">same as input *x*</span></span>                                                                                              | <span data-ttu-id="1923e-125">與輸入 *x* 相同</span><span class="sxs-lookup"><span data-stu-id="1923e-125">same as input *x*</span></span>                                                              | <span data-ttu-id="1923e-126">) 為輸入 *x* 的相同維度 (s</span><span class="sxs-lookup"><span data-stu-id="1923e-126">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="1923e-127">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="1923e-127">Minimum Shader Model</span></span>

<span data-ttu-id="1923e-128">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="1923e-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="1923e-129">著色器模型</span><span class="sxs-lookup"><span data-stu-id="1923e-129">Shader Model</span></span>                                                                       | <span data-ttu-id="1923e-130">支援</span><span class="sxs-lookup"><span data-stu-id="1923e-130">Supported</span></span>             |
|------------------------------------------------------------------------------------|-----------------------|
| <span data-ttu-id="1923e-131">[著色器模型 2 (DIRECTX HLSL) ](dx-graphics-hlsl-sm2.md) 和更高的著色器模型</span><span class="sxs-lookup"><span data-stu-id="1923e-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="1923e-132">是</span><span class="sxs-lookup"><span data-stu-id="1923e-132">yes</span></span>                   |
| [<span data-ttu-id="1923e-133">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="1923e-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="1923e-134">vs \_ 1 \_ 1 和 ps \_ 1 \_ 4</span><span class="sxs-lookup"><span data-stu-id="1923e-134">vs\_1\_1 and ps\_1\_4</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="1923e-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1923e-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1923e-136">**(DirectX HLSL) 內建函式**</span><span class="sxs-lookup"><span data-stu-id="1923e-136">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

