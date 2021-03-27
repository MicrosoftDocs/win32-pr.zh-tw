---
title: atan
description: 傳回指定值的反正切值。
ms.assetid: e3ce3ac3-1012-414f-a193-102208083e39
keywords:
- atan HLSL
topic_type:
- apiref
api_name:
- atan
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 290ced1e5100e3bbc780fab6ab984deaca38528f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682499"
---
# <a name="atan"></a><span data-ttu-id="4d9f9-104">atan</span><span class="sxs-lookup"><span data-stu-id="4d9f9-104">atan</span></span>

<span data-ttu-id="4d9f9-105">傳回指定值的反正切值。</span><span class="sxs-lookup"><span data-stu-id="4d9f9-105">Returns the arctangent of the specified value.</span></span>



| <span data-ttu-id="4d9f9-106">*ret* atan (*x*) </span><span class="sxs-lookup"><span data-stu-id="4d9f9-106">*ret* atan(*x*)</span></span> |
|-----------------|



 

## <a name="parameters"></a><span data-ttu-id="4d9f9-107">參數</span><span class="sxs-lookup"><span data-stu-id="4d9f9-107">Parameters</span></span>



| <span data-ttu-id="4d9f9-108">項目</span><span class="sxs-lookup"><span data-stu-id="4d9f9-108">Item</span></span>                                                   | <span data-ttu-id="4d9f9-109">描述</span><span class="sxs-lookup"><span data-stu-id="4d9f9-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="4d9f9-110"><span id="x"></span><span id="X"></span>*X*</span><span class="sxs-lookup"><span data-stu-id="4d9f9-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="4d9f9-111">\[在 \] 指定的值中。</span><span class="sxs-lookup"><span data-stu-id="4d9f9-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="4d9f9-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="4d9f9-112">Return Value</span></span>

<span data-ttu-id="4d9f9-113">*X* 參數的反正切值。</span><span class="sxs-lookup"><span data-stu-id="4d9f9-113">The arctangent of the *x* parameter.</span></span> <span data-ttu-id="4d9f9-114">這個值在-π/2 到π/2 的範圍內。</span><span class="sxs-lookup"><span data-stu-id="4d9f9-114">This value is within the range of -π/2 to π/2.</span></span>

## <a name="type-description"></a><span data-ttu-id="4d9f9-115">類型描述</span><span class="sxs-lookup"><span data-stu-id="4d9f9-115">Type Description</span></span>



| <span data-ttu-id="4d9f9-116">Name</span><span class="sxs-lookup"><span data-stu-id="4d9f9-116">Name</span></span>  | [<span data-ttu-id="4d9f9-117">**範本類型**</span><span class="sxs-lookup"><span data-stu-id="4d9f9-117">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="4d9f9-118">**元件類型**</span><span class="sxs-lookup"><span data-stu-id="4d9f9-118">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="4d9f9-119">大小</span><span class="sxs-lookup"><span data-stu-id="4d9f9-119">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="4d9f9-120">*x*</span><span class="sxs-lookup"><span data-stu-id="4d9f9-120">*x*</span></span>   | <span data-ttu-id="4d9f9-121">純 [**量、**](dx-graphics-hlsl-intrinsic-functions.md)**向量** 或 **矩陣**</span><span class="sxs-lookup"><span data-stu-id="4d9f9-121">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="4d9f9-122">**浮動**</span><span class="sxs-lookup"><span data-stu-id="4d9f9-122">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="4d9f9-123">任意</span><span class="sxs-lookup"><span data-stu-id="4d9f9-123">any</span></span>                            |
| <span data-ttu-id="4d9f9-124">*Ret*</span><span class="sxs-lookup"><span data-stu-id="4d9f9-124">*ret*</span></span> | <span data-ttu-id="4d9f9-125">與輸入 *x* 相同</span><span class="sxs-lookup"><span data-stu-id="4d9f9-125">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="4d9f9-126">**浮動**</span><span class="sxs-lookup"><span data-stu-id="4d9f9-126">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="4d9f9-127">) 為輸入 *x* 的相同維度 (s</span><span class="sxs-lookup"><span data-stu-id="4d9f9-127">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="4d9f9-128">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="4d9f9-128">Minimum Shader Model</span></span>

<span data-ttu-id="4d9f9-129">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="4d9f9-129">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="4d9f9-130">著色器模型</span><span class="sxs-lookup"><span data-stu-id="4d9f9-130">Shader Model</span></span>                                                                       | <span data-ttu-id="4d9f9-131">支援</span><span class="sxs-lookup"><span data-stu-id="4d9f9-131">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="4d9f9-132">[著色器模型 2 (DIRECTX HLSL) ](dx-graphics-hlsl-sm2.md) 和更高的著色器模型</span><span class="sxs-lookup"><span data-stu-id="4d9f9-132">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="4d9f9-133">是</span><span class="sxs-lookup"><span data-stu-id="4d9f9-133">yes</span></span>       |
| [<span data-ttu-id="4d9f9-134">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="4d9f9-134">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="4d9f9-135">vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="4d9f9-135">vs\_1\_1</span></span>  |



 

## <a name="see-also"></a><span data-ttu-id="4d9f9-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4d9f9-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d9f9-137">**(DirectX HLSL) 內建函式**</span><span class="sxs-lookup"><span data-stu-id="4d9f9-137">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

