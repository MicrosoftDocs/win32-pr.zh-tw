---
title: 'ceil (Corecrt \_ math .h) '
description: 傳回大於或等於指定值的最小整數值。
ms.assetid: 9823f321-14c3-4b27-9a4b-7a885cece39b
keywords:
- ceil HLSL
topic_type:
- apiref
api_name:
- ceil
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec86db320119b7f162ed48a748c1d1ff4335b6f3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992170"
---
# <a name="ceil"></a><span data-ttu-id="e5b5c-104">ceil</span><span class="sxs-lookup"><span data-stu-id="e5b5c-104">ceil</span></span>

<span data-ttu-id="e5b5c-105">傳回大於或等於指定值的最小整數值。</span><span class="sxs-lookup"><span data-stu-id="e5b5c-105">Returns the smallest integer value that is greater than or equal to the specified value.</span></span>



| <span data-ttu-id="e5b5c-106">*ret* ceil (*x*) </span><span class="sxs-lookup"><span data-stu-id="e5b5c-106">*ret* ceil(*x*)</span></span> |
|-----------------|



 

## <a name="parameters"></a><span data-ttu-id="e5b5c-107">參數</span><span class="sxs-lookup"><span data-stu-id="e5b5c-107">Parameters</span></span>



| <span data-ttu-id="e5b5c-108">項目</span><span class="sxs-lookup"><span data-stu-id="e5b5c-108">Item</span></span>                                                   | <span data-ttu-id="e5b5c-109">描述</span><span class="sxs-lookup"><span data-stu-id="e5b5c-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="e5b5c-110"><span id="x"></span><span id="X"></span>*X*</span><span class="sxs-lookup"><span data-stu-id="e5b5c-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="e5b5c-111">\[在 \] 指定的值中。</span><span class="sxs-lookup"><span data-stu-id="e5b5c-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="e5b5c-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="e5b5c-112">Return Value</span></span>

<span data-ttu-id="e5b5c-113">最小整數值 (傳回做為浮點數類型) 大於或等於 *x* 參數。</span><span class="sxs-lookup"><span data-stu-id="e5b5c-113">The smallest integer value (returned as a floating-point type) that is greater than or equal to the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="e5b5c-114">類型描述</span><span class="sxs-lookup"><span data-stu-id="e5b5c-114">Type Description</span></span>



| <span data-ttu-id="e5b5c-115">Name</span><span class="sxs-lookup"><span data-stu-id="e5b5c-115">Name</span></span>  | [<span data-ttu-id="e5b5c-116">**範本類型**</span><span class="sxs-lookup"><span data-stu-id="e5b5c-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="e5b5c-117">**元件類型**</span><span class="sxs-lookup"><span data-stu-id="e5b5c-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="e5b5c-118">大小</span><span class="sxs-lookup"><span data-stu-id="e5b5c-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="e5b5c-119">*x*</span><span class="sxs-lookup"><span data-stu-id="e5b5c-119">*x*</span></span>   | <span data-ttu-id="e5b5c-120">純 [**量、**](dx-graphics-hlsl-intrinsic-functions.md)**向量** 或 **矩陣**</span><span class="sxs-lookup"><span data-stu-id="e5b5c-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="e5b5c-121">**浮動**</span><span class="sxs-lookup"><span data-stu-id="e5b5c-121">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="e5b5c-122">任意</span><span class="sxs-lookup"><span data-stu-id="e5b5c-122">any</span></span>                            |
| <span data-ttu-id="e5b5c-123">*Ret*</span><span class="sxs-lookup"><span data-stu-id="e5b5c-123">*ret*</span></span> | <span data-ttu-id="e5b5c-124">與輸入 *x* 相同</span><span class="sxs-lookup"><span data-stu-id="e5b5c-124">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="e5b5c-125">**浮動**</span><span class="sxs-lookup"><span data-stu-id="e5b5c-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="e5b5c-126">) 為輸入 *x* 的相同維度 (s</span><span class="sxs-lookup"><span data-stu-id="e5b5c-126">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="e5b5c-127">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="e5b5c-127">Minimum Shader Model</span></span>

<span data-ttu-id="e5b5c-128">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="e5b5c-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="e5b5c-129">著色器模型</span><span class="sxs-lookup"><span data-stu-id="e5b5c-129">Shader Model</span></span>                                                                       | <span data-ttu-id="e5b5c-130">支援</span><span class="sxs-lookup"><span data-stu-id="e5b5c-130">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="e5b5c-131">[著色器模型 2 (DIRECTX HLSL) ](dx-graphics-hlsl-sm2.md) 和更高的著色器模型</span><span class="sxs-lookup"><span data-stu-id="e5b5c-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="e5b5c-132">是</span><span class="sxs-lookup"><span data-stu-id="e5b5c-132">yes</span></span>       |
| [<span data-ttu-id="e5b5c-133">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="e5b5c-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="e5b5c-134">vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="e5b5c-134">vs\_1\_1</span></span>  |



 

## <a name="requirements"></a><span data-ttu-id="e5b5c-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="e5b5c-135">Requirements</span></span>



| <span data-ttu-id="e5b5c-136">需求</span><span class="sxs-lookup"><span data-stu-id="e5b5c-136">Requirement</span></span> | <span data-ttu-id="e5b5c-137">值</span><span class="sxs-lookup"><span data-stu-id="e5b5c-137">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5b5c-138">標頭</span><span class="sxs-lookup"><span data-stu-id="e5b5c-138">Header</span></span><br/> | <dl> <span data-ttu-id="e5b5c-139"><dt>Corecrt \_ math。h</dt></span><span class="sxs-lookup"><span data-stu-id="e5b5c-139"><dt>Corecrt\_math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5b5c-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e5b5c-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5b5c-141">**(DirectX HLSL) 內建函式**</span><span class="sxs-lookup"><span data-stu-id="e5b5c-141">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

