---
title: 'isfinite (Corecrt \_ math .h) '
description: 判斷指定的浮點值是否為有限。
ms.assetid: 8be10499-2d06-4520-9697-dab2f461bd0d
keywords:
- isfinite HLSL
topic_type:
- apiref
api_name:
- isfinite
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f63c943dadccad9f485668948f366698f3bce5e6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992190"
---
# <a name="isfinite"></a><span data-ttu-id="277e4-104">isfinite</span><span class="sxs-lookup"><span data-stu-id="277e4-104">isfinite</span></span>

<span data-ttu-id="277e4-105">判斷指定的浮點值是否為有限。</span><span class="sxs-lookup"><span data-stu-id="277e4-105">Determines if the specified floating-point value is finite.</span></span>



| <span data-ttu-id="277e4-106">*ret* isfinite (*x*) </span><span class="sxs-lookup"><span data-stu-id="277e4-106">*ret* isfinite(*x*)</span></span> |
|---------------------|



 

## <a name="parameters"></a><span data-ttu-id="277e4-107">參數</span><span class="sxs-lookup"><span data-stu-id="277e4-107">Parameters</span></span>



| <span data-ttu-id="277e4-108">項目</span><span class="sxs-lookup"><span data-stu-id="277e4-108">Item</span></span>                                                   | <span data-ttu-id="277e4-109">描述</span><span class="sxs-lookup"><span data-stu-id="277e4-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="277e4-110"><span id="x"></span><span id="X"></span>*X*</span><span class="sxs-lookup"><span data-stu-id="277e4-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="277e4-111">\[在 \] 指定的值中。</span><span class="sxs-lookup"><span data-stu-id="277e4-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="277e4-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="277e4-112">Return Value</span></span>

<span data-ttu-id="277e4-113">傳回與輸入相同大小的值，如果 *x* 參數是有限的，則值設定為 **True** 。否則 **為 False**。</span><span class="sxs-lookup"><span data-stu-id="277e4-113">Returns a value of the same size as the input, with a value set to **True** if the *x* parameter is finite; otherwise **False**.</span></span>

## <a name="type-description"></a><span data-ttu-id="277e4-114">類型描述</span><span class="sxs-lookup"><span data-stu-id="277e4-114">Type Description</span></span>



| <span data-ttu-id="277e4-115">Name</span><span class="sxs-lookup"><span data-stu-id="277e4-115">Name</span></span>  | [<span data-ttu-id="277e4-116">**範本類型**</span><span class="sxs-lookup"><span data-stu-id="277e4-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="277e4-117">**元件類型**</span><span class="sxs-lookup"><span data-stu-id="277e4-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="277e4-118">大小</span><span class="sxs-lookup"><span data-stu-id="277e4-118">Size</span></span>     |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|----------|
| <span data-ttu-id="277e4-119">*x*</span><span class="sxs-lookup"><span data-stu-id="277e4-119">*x*</span></span>   | <span data-ttu-id="277e4-120">純 [**量、**](dx-graphics-hlsl-intrinsic-functions.md)**向量** 或 **矩陣**</span><span class="sxs-lookup"><span data-stu-id="277e4-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="277e4-121">**浮動**</span><span class="sxs-lookup"><span data-stu-id="277e4-121">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="277e4-122">任意</span><span class="sxs-lookup"><span data-stu-id="277e4-122">any</span></span>      |
| <span data-ttu-id="277e4-123">*Ret*</span><span class="sxs-lookup"><span data-stu-id="277e4-123">*ret*</span></span> | <span data-ttu-id="277e4-124">純 [**量、**](dx-graphics-hlsl-intrinsic-functions.md)**向量** 或 **矩陣**</span><span class="sxs-lookup"><span data-stu-id="277e4-124">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="277e4-125">**bool**</span><span class="sxs-lookup"><span data-stu-id="277e4-125">**bool**</span></span>](/windows/desktop/WinProg/windows-data-types)                         | <span data-ttu-id="277e4-126">作為輸入</span><span class="sxs-lookup"><span data-stu-id="277e4-126">as input</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="277e4-127">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="277e4-127">Minimum Shader Model</span></span>

<span data-ttu-id="277e4-128">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="277e4-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="277e4-129">著色器模型</span><span class="sxs-lookup"><span data-stu-id="277e4-129">Shader Model</span></span>                                                                       | <span data-ttu-id="277e4-130">支援</span><span class="sxs-lookup"><span data-stu-id="277e4-130">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="277e4-131">[著色器模型 2 (DIRECTX HLSL) ](dx-graphics-hlsl-sm2.md) 和更高的著色器模型</span><span class="sxs-lookup"><span data-stu-id="277e4-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="277e4-132">是</span><span class="sxs-lookup"><span data-stu-id="277e4-132">yes</span></span>                 |
| [<span data-ttu-id="277e4-133">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="277e4-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="277e4-134">是 (\_ \_ 只有) 的 vs 1</span><span class="sxs-lookup"><span data-stu-id="277e4-134">yes (vs\_1\_1 only)</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="277e4-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="277e4-135">Requirements</span></span>



| <span data-ttu-id="277e4-136">需求</span><span class="sxs-lookup"><span data-stu-id="277e4-136">Requirement</span></span> | <span data-ttu-id="277e4-137">值</span><span class="sxs-lookup"><span data-stu-id="277e4-137">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="277e4-138">標頭</span><span class="sxs-lookup"><span data-stu-id="277e4-138">Header</span></span><br/> | <dl> <span data-ttu-id="277e4-139"><dt>Corecrt \_ math。h</dt></span><span class="sxs-lookup"><span data-stu-id="277e4-139"><dt>Corecrt\_math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="277e4-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="277e4-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="277e4-141">**(DirectX HLSL) 內建函式**</span><span class="sxs-lookup"><span data-stu-id="277e4-141">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

