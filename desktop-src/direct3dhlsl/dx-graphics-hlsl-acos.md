---
title: acos
description: 傳回指定之值的反余弦值。
ms.assetid: c9bc33b8-d586-4c64-9453-5ab97396f2cf
keywords:
- acos HLSL
topic_type:
- apiref
api_name:
- acos
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2cd909c4a4c1300374bba723f1edabb48d51b2e0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104093208"
---
# <a name="acos"></a><span data-ttu-id="714bd-104">acos</span><span class="sxs-lookup"><span data-stu-id="714bd-104">acos</span></span>

<span data-ttu-id="714bd-105">傳回指定之值的反余弦值。</span><span class="sxs-lookup"><span data-stu-id="714bd-105">Returns the arccosine of the specified value.</span></span>



| <span data-ttu-id="714bd-106">*ret* acos (*x*) </span><span class="sxs-lookup"><span data-stu-id="714bd-106">*ret* acos(*x*)</span></span> |
|-----------------|



 

## <a name="parameters"></a><span data-ttu-id="714bd-107">參數</span><span class="sxs-lookup"><span data-stu-id="714bd-107">Parameters</span></span>



| <span data-ttu-id="714bd-108">項目</span><span class="sxs-lookup"><span data-stu-id="714bd-108">Item</span></span>                                                   | <span data-ttu-id="714bd-109">描述</span><span class="sxs-lookup"><span data-stu-id="714bd-109">Description</span></span>                                                                                                         |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="714bd-110"><span id="x"></span><span id="X"></span>*X*</span><span class="sxs-lookup"><span data-stu-id="714bd-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="714bd-111">\[在 \] 指定的值中。</span><span class="sxs-lookup"><span data-stu-id="714bd-111">\[in\] The specified value.</span></span> <span data-ttu-id="714bd-112">每個元件都應該是介於-1 到1範圍內的浮點值。</span><span class="sxs-lookup"><span data-stu-id="714bd-112">Each component should be a floating-point value within the range of -1 to 1.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="714bd-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="714bd-113">Return Value</span></span>

<span data-ttu-id="714bd-114">*X* 參數的反余弦。</span><span class="sxs-lookup"><span data-stu-id="714bd-114">The arccosine of the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="714bd-115">類型描述</span><span class="sxs-lookup"><span data-stu-id="714bd-115">Type Description</span></span>



| <span data-ttu-id="714bd-116">Name</span><span class="sxs-lookup"><span data-stu-id="714bd-116">Name</span></span>  | [<span data-ttu-id="714bd-117">**範本類型**</span><span class="sxs-lookup"><span data-stu-id="714bd-117">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="714bd-118">**元件類型**</span><span class="sxs-lookup"><span data-stu-id="714bd-118">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="714bd-119">大小</span><span class="sxs-lookup"><span data-stu-id="714bd-119">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="714bd-120">*x*</span><span class="sxs-lookup"><span data-stu-id="714bd-120">*x*</span></span>   | <span data-ttu-id="714bd-121">純 [**量、**](dx-graphics-hlsl-intrinsic-functions.md)**向量** 或 **矩陣**</span><span class="sxs-lookup"><span data-stu-id="714bd-121">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="714bd-122">**浮動**</span><span class="sxs-lookup"><span data-stu-id="714bd-122">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="714bd-123">任意</span><span class="sxs-lookup"><span data-stu-id="714bd-123">any</span></span>                            |
| <span data-ttu-id="714bd-124">*Ret*</span><span class="sxs-lookup"><span data-stu-id="714bd-124">*ret*</span></span> | <span data-ttu-id="714bd-125">與輸入 *x* 相同</span><span class="sxs-lookup"><span data-stu-id="714bd-125">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="714bd-126">**浮動**</span><span class="sxs-lookup"><span data-stu-id="714bd-126">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="714bd-127">) 為輸入 *x* 的相同維度 (s</span><span class="sxs-lookup"><span data-stu-id="714bd-127">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="714bd-128">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="714bd-128">Minimum Shader Model</span></span>

<span data-ttu-id="714bd-129">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="714bd-129">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="714bd-130">著色器模型</span><span class="sxs-lookup"><span data-stu-id="714bd-130">Shader Model</span></span>                                                                       | <span data-ttu-id="714bd-131">支援</span><span class="sxs-lookup"><span data-stu-id="714bd-131">Supported</span></span>     |
|------------------------------------------------------------------------------------|---------------|
| <span data-ttu-id="714bd-132">[著色器模型 2 (DIRECTX HLSL) ](dx-graphics-hlsl-sm2.md) 和更高的著色器模型</span><span class="sxs-lookup"><span data-stu-id="714bd-132">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="714bd-133">是</span><span class="sxs-lookup"><span data-stu-id="714bd-133">yes</span></span>           |
| [<span data-ttu-id="714bd-134">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="714bd-134">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="714bd-135">\_ \_ 僅限 vs 1 1</span><span class="sxs-lookup"><span data-stu-id="714bd-135">vs\_1\_1 only</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="714bd-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="714bd-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="714bd-137">**(DirectX HLSL) 內建函式**</span><span class="sxs-lookup"><span data-stu-id="714bd-137">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

