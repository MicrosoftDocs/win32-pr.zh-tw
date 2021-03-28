---
title: sqrt
description: 傳回指定之浮點值的平方根（每個元件）。
ms.assetid: e8debc60-1441-4974-9ab3-6d1c2217caaf
keywords:
- sqrt HLSL
topic_type:
- apiref
api_name:
- sqrt
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ff3c872dac6da28a1ec92993e387bd23daec7f86
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375377"
---
# <a name="sqrt"></a><span data-ttu-id="4499d-104">sqrt</span><span class="sxs-lookup"><span data-stu-id="4499d-104">sqrt</span></span>

<span data-ttu-id="4499d-105">傳回指定之浮點值的平方根（每個元件）。</span><span class="sxs-lookup"><span data-stu-id="4499d-105">Returns the square root of the specified floating-point value, per component.</span></span>



| <span data-ttu-id="4499d-106">*ret* sqrt (*x*) </span><span class="sxs-lookup"><span data-stu-id="4499d-106">*ret* sqrt(*x*)</span></span> |
|-----------------|



 

## <a name="parameters"></a><span data-ttu-id="4499d-107">參數</span><span class="sxs-lookup"><span data-stu-id="4499d-107">Parameters</span></span>



| <span data-ttu-id="4499d-108">項目</span><span class="sxs-lookup"><span data-stu-id="4499d-108">Item</span></span>                                                   | <span data-ttu-id="4499d-109">描述</span><span class="sxs-lookup"><span data-stu-id="4499d-109">Description</span></span>                                           |
|--------------------------------------------------------|-------------------------------------------------------|
| <span data-ttu-id="4499d-110"><span id="x"></span><span id="X"></span>*X*</span><span class="sxs-lookup"><span data-stu-id="4499d-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="4499d-111">\[在 \] 指定的浮點值中。</span><span class="sxs-lookup"><span data-stu-id="4499d-111">\[in\] The specified floating-point value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="4499d-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="4499d-112">Return Value</span></span>

<span data-ttu-id="4499d-113">每個元件 *x* 參數的平方根。</span><span class="sxs-lookup"><span data-stu-id="4499d-113">The square root of the *x* parameter, per component.</span></span>

## <a name="type-description"></a><span data-ttu-id="4499d-114">類型描述</span><span class="sxs-lookup"><span data-stu-id="4499d-114">Type Description</span></span>



| <span data-ttu-id="4499d-115">Name</span><span class="sxs-lookup"><span data-stu-id="4499d-115">Name</span></span>  | [<span data-ttu-id="4499d-116">**範本類型**</span><span class="sxs-lookup"><span data-stu-id="4499d-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="4499d-117">**元件類型**</span><span class="sxs-lookup"><span data-stu-id="4499d-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="4499d-118">大小</span><span class="sxs-lookup"><span data-stu-id="4499d-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="4499d-119">*x*</span><span class="sxs-lookup"><span data-stu-id="4499d-119">*x*</span></span>   | <span data-ttu-id="4499d-120">純 [**量、**](dx-graphics-hlsl-intrinsic-functions.md)**向量** 或 **矩陣**</span><span class="sxs-lookup"><span data-stu-id="4499d-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="4499d-121">**浮動**</span><span class="sxs-lookup"><span data-stu-id="4499d-121">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="4499d-122">任意</span><span class="sxs-lookup"><span data-stu-id="4499d-122">any</span></span>                            |
| <span data-ttu-id="4499d-123">*Ret*</span><span class="sxs-lookup"><span data-stu-id="4499d-123">*ret*</span></span> | <span data-ttu-id="4499d-124">與輸入 *x* 相同</span><span class="sxs-lookup"><span data-stu-id="4499d-124">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="4499d-125">**浮動**</span><span class="sxs-lookup"><span data-stu-id="4499d-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="4499d-126">) 為輸入 *x* 的相同維度 (s</span><span class="sxs-lookup"><span data-stu-id="4499d-126">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="4499d-127">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="4499d-127">Minimum Shader Model</span></span>

<span data-ttu-id="4499d-128">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="4499d-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="4499d-129">著色器模型</span><span class="sxs-lookup"><span data-stu-id="4499d-129">Shader Model</span></span>                                                                       | <span data-ttu-id="4499d-130">支援</span><span class="sxs-lookup"><span data-stu-id="4499d-130">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="4499d-131">[著色器模型 2 (DIRECTX HLSL) ](dx-graphics-hlsl-sm2.md) 和更高的著色器模型</span><span class="sxs-lookup"><span data-stu-id="4499d-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="4499d-132">是</span><span class="sxs-lookup"><span data-stu-id="4499d-132">yes</span></span>                 |
| [<span data-ttu-id="4499d-133">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="4499d-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="4499d-134">是 (\_ \_ 只有) 的 vs 1</span><span class="sxs-lookup"><span data-stu-id="4499d-134">yes (vs\_1\_1 only)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="4499d-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4499d-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4499d-136">**(DirectX HLSL) 內建函式**</span><span class="sxs-lookup"><span data-stu-id="4499d-136">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

