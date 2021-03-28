---
title: tanh
description: 傳回指定之值的雙曲正切值。
ms.assetid: e2d27aa0-5e03-4f2f-a29c-884711710c8d
keywords:
- tanh HLSL
topic_type:
- apiref
api_name:
- tanh
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7c5312aaac6d6f164e940f99183e61688b393fbd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023672"
---
# <a name="tanh"></a><span data-ttu-id="1624d-104">tanh</span><span class="sxs-lookup"><span data-stu-id="1624d-104">tanh</span></span>

<span data-ttu-id="1624d-105">傳回指定之值的雙曲正切值。</span><span class="sxs-lookup"><span data-stu-id="1624d-105">Returns the hyperbolic tangent of the specified value.</span></span>



| <span data-ttu-id="1624d-106">*ret* tanh (*x*) </span><span class="sxs-lookup"><span data-stu-id="1624d-106">*ret* tanh(*x*)</span></span> |
|-----------------|



 

## <a name="parameters"></a><span data-ttu-id="1624d-107">參數</span><span class="sxs-lookup"><span data-stu-id="1624d-107">Parameters</span></span>



| <span data-ttu-id="1624d-108">項目</span><span class="sxs-lookup"><span data-stu-id="1624d-108">Item</span></span>                                                   | <span data-ttu-id="1624d-109">描述</span><span class="sxs-lookup"><span data-stu-id="1624d-109">Description</span></span>                                        |
|--------------------------------------------------------|----------------------------------------------------|
| <span data-ttu-id="1624d-110"><span id="x"></span><span id="X"></span>*X*</span><span class="sxs-lookup"><span data-stu-id="1624d-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="1624d-111">\[在 \] 指定的值中，以弧度為單位。</span><span class="sxs-lookup"><span data-stu-id="1624d-111">\[in\] The specified value, in radians.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="1624d-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="1624d-112">Return Value</span></span>

<span data-ttu-id="1624d-113">*X* 參數的雙曲正切值。</span><span class="sxs-lookup"><span data-stu-id="1624d-113">The hyperbolic tangent of the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="1624d-114">類型描述</span><span class="sxs-lookup"><span data-stu-id="1624d-114">Type Description</span></span>



| <span data-ttu-id="1624d-115">名稱</span><span class="sxs-lookup"><span data-stu-id="1624d-115">Name</span></span>  | [<span data-ttu-id="1624d-116">**範本類型**</span><span class="sxs-lookup"><span data-stu-id="1624d-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="1624d-117">**元件類型**</span><span class="sxs-lookup"><span data-stu-id="1624d-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="1624d-118">大小</span><span class="sxs-lookup"><span data-stu-id="1624d-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="1624d-119">*x*</span><span class="sxs-lookup"><span data-stu-id="1624d-119">*x*</span></span>   | <span data-ttu-id="1624d-120">純 [**量、**](dx-graphics-hlsl-intrinsic-functions.md)**向量** 或 **矩陣**</span><span class="sxs-lookup"><span data-stu-id="1624d-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="1624d-121">**浮動**</span><span class="sxs-lookup"><span data-stu-id="1624d-121">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="1624d-122">任意</span><span class="sxs-lookup"><span data-stu-id="1624d-122">any</span></span>                            |
| <span data-ttu-id="1624d-123">*Ret*</span><span class="sxs-lookup"><span data-stu-id="1624d-123">*ret*</span></span> | <span data-ttu-id="1624d-124">與輸入 *x* 相同</span><span class="sxs-lookup"><span data-stu-id="1624d-124">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="1624d-125">**浮動**</span><span class="sxs-lookup"><span data-stu-id="1624d-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="1624d-126">) 為輸入 *x* 的相同維度 (s</span><span class="sxs-lookup"><span data-stu-id="1624d-126">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="1624d-127">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="1624d-127">Minimum Shader Model</span></span>

<span data-ttu-id="1624d-128">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="1624d-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="1624d-129">著色器模型</span><span class="sxs-lookup"><span data-stu-id="1624d-129">Shader Model</span></span>                                                                       | <span data-ttu-id="1624d-130">支援</span><span class="sxs-lookup"><span data-stu-id="1624d-130">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="1624d-131">[著色器模型 2 (DIRECTX HLSL) ](dx-graphics-hlsl-sm2.md) 和更高的著色器模型</span><span class="sxs-lookup"><span data-stu-id="1624d-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="1624d-132">是</span><span class="sxs-lookup"><span data-stu-id="1624d-132">yes</span></span>                 |
| [<span data-ttu-id="1624d-133">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="1624d-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="1624d-134">是 (\_ \_ 只有) 的 vs 1</span><span class="sxs-lookup"><span data-stu-id="1624d-134">yes (vs\_1\_1 only)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="1624d-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1624d-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1624d-136">**(DirectX HLSL) 內建函式**</span><span class="sxs-lookup"><span data-stu-id="1624d-136">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

