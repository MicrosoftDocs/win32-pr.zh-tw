---
title: 'trunc (Corecrt \_ math .h) '
description: 將浮點值截斷為整陣列件。
ms.assetid: a0978fa2-71f8-4257-8c90-96224c2ec953
keywords:
- trunc HLSL
topic_type:
- apiref
api_name:
- trunc
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34493f60e60bc0dce35f5f9db50360265191c742
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992235"
---
# <a name="trunc"></a><span data-ttu-id="7470a-104">trunc</span><span class="sxs-lookup"><span data-stu-id="7470a-104">trunc</span></span>

<span data-ttu-id="7470a-105">將浮點值截斷為整陣列件。</span><span class="sxs-lookup"><span data-stu-id="7470a-105">Truncates a floating-point value to the integer component.</span></span>



| <span data-ttu-id="7470a-106">ret trunc (*x*) </span><span class="sxs-lookup"><span data-stu-id="7470a-106">ret trunc(*x*)</span></span> |
|----------------|



 

## <a name="parameters"></a><span data-ttu-id="7470a-107">參數</span><span class="sxs-lookup"><span data-stu-id="7470a-107">Parameters</span></span>



| <span data-ttu-id="7470a-108">項目</span><span class="sxs-lookup"><span data-stu-id="7470a-108">Item</span></span>                                                   | <span data-ttu-id="7470a-109">描述</span><span class="sxs-lookup"><span data-stu-id="7470a-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="7470a-110"><span id="x"></span><span id="X"></span>*X*</span><span class="sxs-lookup"><span data-stu-id="7470a-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="7470a-111">\[在 \] 指定的輸入中。</span><span class="sxs-lookup"><span data-stu-id="7470a-111">\[in\] The specified input.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="7470a-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="7470a-112">Return Value</span></span>

<span data-ttu-id="7470a-113">輸入值已截斷為整陣列件。</span><span class="sxs-lookup"><span data-stu-id="7470a-113">The input value truncated to an integer component.</span></span>

## <a name="remarks"></a><span data-ttu-id="7470a-114">備註</span><span class="sxs-lookup"><span data-stu-id="7470a-114">Remarks</span></span>

<span data-ttu-id="7470a-115">此函式會將浮點值截斷為整陣列件。</span><span class="sxs-lookup"><span data-stu-id="7470a-115">This function truncates a floating-point value to the integer component.</span></span> <span data-ttu-id="7470a-116">假設浮點值為1.6，trunc 函式會傳回1.0，其中的 [**round (DIRECTX HLSL)**](dx-graphics-hlsl-round.md) 函數會傳回2.0。</span><span class="sxs-lookup"><span data-stu-id="7470a-116">Given a floating-point value of 1.6, the trunc function would return 1.0, where as the [**round (DirectX HLSL)**](dx-graphics-hlsl-round.md) function would return 2.0.</span></span>

## <a name="type-description"></a><span data-ttu-id="7470a-117">類型描述</span><span class="sxs-lookup"><span data-stu-id="7470a-117">Type Description</span></span>



| <span data-ttu-id="7470a-118">Name</span><span class="sxs-lookup"><span data-stu-id="7470a-118">Name</span></span> | [<span data-ttu-id="7470a-119">**範本類型**</span><span class="sxs-lookup"><span data-stu-id="7470a-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="7470a-120">**元件類型**</span><span class="sxs-lookup"><span data-stu-id="7470a-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="7470a-121">大小</span><span class="sxs-lookup"><span data-stu-id="7470a-121">Size</span></span>                         |
|------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|------------------------------|
| <span data-ttu-id="7470a-122">*x*</span><span class="sxs-lookup"><span data-stu-id="7470a-122">*x*</span></span>  | <span data-ttu-id="7470a-123">純 [**量、**](dx-graphics-hlsl-intrinsic-functions.md)**向量** 或 **矩陣**</span><span class="sxs-lookup"><span data-stu-id="7470a-123">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="7470a-124">**浮動**</span><span class="sxs-lookup"><span data-stu-id="7470a-124">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="7470a-125">任意</span><span class="sxs-lookup"><span data-stu-id="7470a-125">any</span></span>                          |
| <span data-ttu-id="7470a-126">Ret</span><span class="sxs-lookup"><span data-stu-id="7470a-126">ret</span></span>  | <span data-ttu-id="7470a-127">與輸入 x 相同的類型</span><span class="sxs-lookup"><span data-stu-id="7470a-127">Same type as input x</span></span>                                                                                           | [<span data-ttu-id="7470a-128">**浮動**</span><span class="sxs-lookup"><span data-stu-id="7470a-128">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="7470a-129">) 為輸入 x 的相同維度 (s</span><span class="sxs-lookup"><span data-stu-id="7470a-129">Same dimension(s) as input x</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="7470a-130">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="7470a-130">Minimum Shader Model</span></span>

<span data-ttu-id="7470a-131">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="7470a-131">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="7470a-132">著色器模型</span><span class="sxs-lookup"><span data-stu-id="7470a-132">Shader Model</span></span>                                                                       | <span data-ttu-id="7470a-133">支援</span><span class="sxs-lookup"><span data-stu-id="7470a-133">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="7470a-134">[著色器模型 1 (DIRECTX HLSL) ](dx-graphics-hlsl-sm1.md) 和更高的著色器模型</span><span class="sxs-lookup"><span data-stu-id="7470a-134">[Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) and higher shader models</span></span> | <span data-ttu-id="7470a-135">是</span><span class="sxs-lookup"><span data-stu-id="7470a-135">yes</span></span>       |



 

## <a name="requirements"></a><span data-ttu-id="7470a-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="7470a-136">Requirements</span></span>



| <span data-ttu-id="7470a-137">需求</span><span class="sxs-lookup"><span data-stu-id="7470a-137">Requirement</span></span> | <span data-ttu-id="7470a-138">值</span><span class="sxs-lookup"><span data-stu-id="7470a-138">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="7470a-139">標頭</span><span class="sxs-lookup"><span data-stu-id="7470a-139">Header</span></span><br/> | <dl> <span data-ttu-id="7470a-140"><dt>Corecrt \_ math。h</dt></span><span class="sxs-lookup"><span data-stu-id="7470a-140"><dt>Corecrt\_math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7470a-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7470a-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7470a-142">**(DirectX HLSL) 內建函式**</span><span class="sxs-lookup"><span data-stu-id="7470a-142">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

