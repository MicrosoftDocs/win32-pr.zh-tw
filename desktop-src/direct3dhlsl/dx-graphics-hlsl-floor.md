---
title: 'floor (Corecrt \_ math .h) '
description: 傳回小於或等於指定值的最大整數。
ms.assetid: f7193425-2448-4ae6-99d5-bb5e1aa74111
keywords:
- 樓層 HLSL
topic_type:
- apiref
api_name:
- floor
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ecb46719d5361ec9f7c36b21d94793bc9a67ffe
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974500"
---
# <a name="floor"></a><span data-ttu-id="12c64-104">floor</span><span class="sxs-lookup"><span data-stu-id="12c64-104">floor</span></span>

<span data-ttu-id="12c64-105">傳回小於或等於指定值的最大整數。</span><span class="sxs-lookup"><span data-stu-id="12c64-105">Returns the largest integer that is less than or equal to the specified value.</span></span>



| <span data-ttu-id="12c64-106">*ret* floor (*x*) </span><span class="sxs-lookup"><span data-stu-id="12c64-106">*ret* floor(*x*)</span></span> |
|------------------|



 

## <a name="parameters"></a><span data-ttu-id="12c64-107">參數</span><span class="sxs-lookup"><span data-stu-id="12c64-107">Parameters</span></span>



| <span data-ttu-id="12c64-108">項目</span><span class="sxs-lookup"><span data-stu-id="12c64-108">Item</span></span>                                                   | <span data-ttu-id="12c64-109">描述</span><span class="sxs-lookup"><span data-stu-id="12c64-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="12c64-110"><span id="x"></span><span id="X"></span>*X*</span><span class="sxs-lookup"><span data-stu-id="12c64-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="12c64-111">\[在 \] 指定的值中。</span><span class="sxs-lookup"><span data-stu-id="12c64-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="12c64-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="12c64-112">Return Value</span></span>

<span data-ttu-id="12c64-113">最大整數值 (傳回為浮點數類型) 小於或等於 *x* 參數。</span><span class="sxs-lookup"><span data-stu-id="12c64-113">The largest integer value (returned as a floating-point type) that is less than or equal to the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="12c64-114">類型描述</span><span class="sxs-lookup"><span data-stu-id="12c64-114">Type Description</span></span>



| <span data-ttu-id="12c64-115">Name</span><span class="sxs-lookup"><span data-stu-id="12c64-115">Name</span></span>  | [<span data-ttu-id="12c64-116">**範本類型**</span><span class="sxs-lookup"><span data-stu-id="12c64-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="12c64-117">**元件類型**</span><span class="sxs-lookup"><span data-stu-id="12c64-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="12c64-118">大小</span><span class="sxs-lookup"><span data-stu-id="12c64-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="12c64-119">*x*</span><span class="sxs-lookup"><span data-stu-id="12c64-119">*x*</span></span>   | <span data-ttu-id="12c64-120">純 [**量、**](dx-graphics-hlsl-intrinsic-functions.md)**向量** 或 **矩陣**</span><span class="sxs-lookup"><span data-stu-id="12c64-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="12c64-121">**浮動**</span><span class="sxs-lookup"><span data-stu-id="12c64-121">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="12c64-122">任意</span><span class="sxs-lookup"><span data-stu-id="12c64-122">any</span></span>                            |
| <span data-ttu-id="12c64-123">*Ret*</span><span class="sxs-lookup"><span data-stu-id="12c64-123">*ret*</span></span> | <span data-ttu-id="12c64-124">與輸入 *x* 相同</span><span class="sxs-lookup"><span data-stu-id="12c64-124">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="12c64-125">**浮動**</span><span class="sxs-lookup"><span data-stu-id="12c64-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="12c64-126">) 為輸入 *x* 的相同維度 (s</span><span class="sxs-lookup"><span data-stu-id="12c64-126">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="12c64-127">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="12c64-127">Minimum Shader Model</span></span>

<span data-ttu-id="12c64-128">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="12c64-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="12c64-129">著色器模型</span><span class="sxs-lookup"><span data-stu-id="12c64-129">Shader Model</span></span>                                                                       | <span data-ttu-id="12c64-130">支援</span><span class="sxs-lookup"><span data-stu-id="12c64-130">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="12c64-131">[著色器模型 2 (DIRECTX HLSL) ](dx-graphics-hlsl-sm2.md) 和更高的著色器模型</span><span class="sxs-lookup"><span data-stu-id="12c64-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="12c64-132">是</span><span class="sxs-lookup"><span data-stu-id="12c64-132">yes</span></span>       |
| [<span data-ttu-id="12c64-133">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="12c64-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="12c64-134">vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="12c64-134">vs\_1\_1</span></span>  |



 

## <a name="requirements"></a><span data-ttu-id="12c64-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="12c64-135">Requirements</span></span>



| <span data-ttu-id="12c64-136">需求</span><span class="sxs-lookup"><span data-stu-id="12c64-136">Requirement</span></span> | <span data-ttu-id="12c64-137">值</span><span class="sxs-lookup"><span data-stu-id="12c64-137">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="12c64-138">標頭</span><span class="sxs-lookup"><span data-stu-id="12c64-138">Header</span></span><br/> | <dl> <span data-ttu-id="12c64-139"><dt>Corecrt \_ math。h</dt></span><span class="sxs-lookup"><span data-stu-id="12c64-139"><dt>Corecrt\_math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12c64-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="12c64-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12c64-141">**(DirectX HLSL) 內建函式**</span><span class="sxs-lookup"><span data-stu-id="12c64-141">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

