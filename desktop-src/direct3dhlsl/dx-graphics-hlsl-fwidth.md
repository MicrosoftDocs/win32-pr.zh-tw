---
title: fwidth
description: 傳回指定之值的部分衍生值的絕對值。
ms.assetid: 7184c3b4-1720-4176-a494-7f73322a918e
keywords:
- fwidth HLSL
topic_type:
- apiref
api_name:
- fwidth
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cf2d5a34e1f387aadb3b044ddd1264616a61109b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104093004"
---
# <a name="fwidth"></a><span data-ttu-id="ba003-104">fwidth</span><span class="sxs-lookup"><span data-stu-id="ba003-104">fwidth</span></span>

<span data-ttu-id="ba003-105">傳回指定之值的部分衍生值的絕對值。</span><span class="sxs-lookup"><span data-stu-id="ba003-105">Returns the absolute value of the partial derivatives of the specified value.</span></span>



| <span data-ttu-id="ba003-106">*ret* fwidth (*x*) </span><span class="sxs-lookup"><span data-stu-id="ba003-106">*ret* fwidth(*x*)</span></span> |
|-------------------|



 

<span data-ttu-id="ba003-107">此函數會計算下列各項： [**abs**](dx-graphics-hlsl-abs.md) ([**ddx**](dx-graphics-hlsl-ddx.md) (*x*) ) + [**abs**](dx-graphics-hlsl-abs.md) ([**ddy**](dx-graphics-hlsl-ddy.md) (*x*) ) 。</span><span class="sxs-lookup"><span data-stu-id="ba003-107">This function computes the following: [**abs**](dx-graphics-hlsl-abs.md)([**ddx**](dx-graphics-hlsl-ddx.md)(*x*)) + [**abs**](dx-graphics-hlsl-abs.md)([**ddy**](dx-graphics-hlsl-ddy.md)(*x*)).</span></span>

<span data-ttu-id="ba003-108">只有圖元著色器支援此函式。</span><span class="sxs-lookup"><span data-stu-id="ba003-108">This function is only supported in pixel shaders.</span></span>

## <a name="parameters"></a><span data-ttu-id="ba003-109">參數</span><span class="sxs-lookup"><span data-stu-id="ba003-109">Parameters</span></span>



| <span data-ttu-id="ba003-110">項目</span><span class="sxs-lookup"><span data-stu-id="ba003-110">Item</span></span>                                                   | <span data-ttu-id="ba003-111">描述</span><span class="sxs-lookup"><span data-stu-id="ba003-111">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="ba003-112"><span id="x"></span><span id="X"></span>*X*</span><span class="sxs-lookup"><span data-stu-id="ba003-112"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="ba003-113">\[在 \] 指定的值中。</span><span class="sxs-lookup"><span data-stu-id="ba003-113">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="ba003-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="ba003-114">Return Value</span></span>

<span data-ttu-id="ba003-115">*X* 參數的部分衍生值的絕對值。</span><span class="sxs-lookup"><span data-stu-id="ba003-115">The absolute value of the partial derivatives of the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="ba003-116">類型描述</span><span class="sxs-lookup"><span data-stu-id="ba003-116">Type Description</span></span>



| <span data-ttu-id="ba003-117">名稱</span><span class="sxs-lookup"><span data-stu-id="ba003-117">Name</span></span>  | [<span data-ttu-id="ba003-118">**範本類型**</span><span class="sxs-lookup"><span data-stu-id="ba003-118">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="ba003-119">**元件類型**</span><span class="sxs-lookup"><span data-stu-id="ba003-119">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="ba003-120">大小</span><span class="sxs-lookup"><span data-stu-id="ba003-120">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="ba003-121">*x*</span><span class="sxs-lookup"><span data-stu-id="ba003-121">*x*</span></span>   | <span data-ttu-id="ba003-122">純 [**量、**](dx-graphics-hlsl-intrinsic-functions.md)**向量** 或 **矩陣**</span><span class="sxs-lookup"><span data-stu-id="ba003-122">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="ba003-123">**浮動**</span><span class="sxs-lookup"><span data-stu-id="ba003-123">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="ba003-124">任意</span><span class="sxs-lookup"><span data-stu-id="ba003-124">any</span></span>                            |
| <span data-ttu-id="ba003-125">*Ret*</span><span class="sxs-lookup"><span data-stu-id="ba003-125">*ret*</span></span> | <span data-ttu-id="ba003-126">與輸入 *x* 相同</span><span class="sxs-lookup"><span data-stu-id="ba003-126">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="ba003-127">**浮動**</span><span class="sxs-lookup"><span data-stu-id="ba003-127">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="ba003-128">) 為輸入 *x* 的相同維度 (s</span><span class="sxs-lookup"><span data-stu-id="ba003-128">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="ba003-129">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="ba003-129">Minimum Shader Model</span></span>

<span data-ttu-id="ba003-130">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="ba003-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="ba003-131">著色器模型</span><span class="sxs-lookup"><span data-stu-id="ba003-131">Shader Model</span></span>                                                                       | <span data-ttu-id="ba003-132">支援</span><span class="sxs-lookup"><span data-stu-id="ba003-132">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="ba003-133">[著色器模型 3 (DIRECTX HLSL) ](dx-graphics-hlsl-sm3.md) 和更高的著色器模型</span><span class="sxs-lookup"><span data-stu-id="ba003-133">[Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) and higher shader models</span></span> | <span data-ttu-id="ba003-134">是</span><span class="sxs-lookup"><span data-stu-id="ba003-134">yes</span></span>                 |
| [<span data-ttu-id="ba003-135">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="ba003-135">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md)                          | <span data-ttu-id="ba003-136">是 (ps \_ 2 \_ x 僅) </span><span class="sxs-lookup"><span data-stu-id="ba003-136">yes (ps\_2\_x only)</span></span> |
| [<span data-ttu-id="ba003-137">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="ba003-137">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="ba003-138">不可以</span><span class="sxs-lookup"><span data-stu-id="ba003-138">no</span></span>                  |



 

## <a name="see-also"></a><span data-ttu-id="ba003-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ba003-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba003-140">**(DirectX HLSL) 內建函式**</span><span class="sxs-lookup"><span data-stu-id="ba003-140">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

