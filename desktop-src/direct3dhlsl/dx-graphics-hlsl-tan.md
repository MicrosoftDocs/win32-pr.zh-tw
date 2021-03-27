---
title: tan
description: 傳回指定值的正切函數。
ms.assetid: ca03b184-9e1a-4152-9292-f8af38aa9423
keywords:
- tan HLSL
topic_type:
- apiref
api_name:
- tan
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cf9451a2bf1a5759470e87343f1b4a15583b470a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682584"
---
# <a name="tan"></a><span data-ttu-id="d5b73-104">tan</span><span class="sxs-lookup"><span data-stu-id="d5b73-104">tan</span></span>

<span data-ttu-id="d5b73-105">傳回指定值的正切函數。</span><span class="sxs-lookup"><span data-stu-id="d5b73-105">Returns the tangent of the specified value.</span></span>



| <span data-ttu-id="d5b73-106">*ret* tan (*x*) </span><span class="sxs-lookup"><span data-stu-id="d5b73-106">*ret* tan(*x*)</span></span> |
|----------------|



 

## <a name="parameters"></a><span data-ttu-id="d5b73-107">參數</span><span class="sxs-lookup"><span data-stu-id="d5b73-107">Parameters</span></span>



| <span data-ttu-id="d5b73-108">項目</span><span class="sxs-lookup"><span data-stu-id="d5b73-108">Item</span></span>                                                   | <span data-ttu-id="d5b73-109">描述</span><span class="sxs-lookup"><span data-stu-id="d5b73-109">Description</span></span>                                        |
|--------------------------------------------------------|----------------------------------------------------|
| <span data-ttu-id="d5b73-110"><span id="x"></span><span id="X"></span>*X*</span><span class="sxs-lookup"><span data-stu-id="d5b73-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="d5b73-111">\[在 \] 指定的值中，以弧度為單位。</span><span class="sxs-lookup"><span data-stu-id="d5b73-111">\[in\] The specified value, in radians.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="d5b73-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="d5b73-112">Return Value</span></span>

<span data-ttu-id="d5b73-113">*X* 參數的正切函數。</span><span class="sxs-lookup"><span data-stu-id="d5b73-113">The tangent of the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="d5b73-114">類型描述</span><span class="sxs-lookup"><span data-stu-id="d5b73-114">Type Description</span></span>



| <span data-ttu-id="d5b73-115">名稱</span><span class="sxs-lookup"><span data-stu-id="d5b73-115">Name</span></span>  | [<span data-ttu-id="d5b73-116">**範本類型**</span><span class="sxs-lookup"><span data-stu-id="d5b73-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="d5b73-117">**元件類型**</span><span class="sxs-lookup"><span data-stu-id="d5b73-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="d5b73-118">大小</span><span class="sxs-lookup"><span data-stu-id="d5b73-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="d5b73-119">*x*</span><span class="sxs-lookup"><span data-stu-id="d5b73-119">*x*</span></span>   | <span data-ttu-id="d5b73-120">純 [**量、**](dx-graphics-hlsl-intrinsic-functions.md)**向量** 或 **矩陣**</span><span class="sxs-lookup"><span data-stu-id="d5b73-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="d5b73-121">**浮動**</span><span class="sxs-lookup"><span data-stu-id="d5b73-121">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="d5b73-122">任意</span><span class="sxs-lookup"><span data-stu-id="d5b73-122">any</span></span>                            |
| <span data-ttu-id="d5b73-123">*Ret*</span><span class="sxs-lookup"><span data-stu-id="d5b73-123">*ret*</span></span> | <span data-ttu-id="d5b73-124">與輸入 *x* 相同</span><span class="sxs-lookup"><span data-stu-id="d5b73-124">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="d5b73-125">**浮動**</span><span class="sxs-lookup"><span data-stu-id="d5b73-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="d5b73-126">) 為輸入 *x* 的相同維度 (s</span><span class="sxs-lookup"><span data-stu-id="d5b73-126">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="d5b73-127">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="d5b73-127">Minimum Shader Model</span></span>

<span data-ttu-id="d5b73-128">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="d5b73-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="d5b73-129">著色器模型</span><span class="sxs-lookup"><span data-stu-id="d5b73-129">Shader Model</span></span>                                                                       | <span data-ttu-id="d5b73-130">支援</span><span class="sxs-lookup"><span data-stu-id="d5b73-130">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="d5b73-131">[著色器模型 2 (DIRECTX HLSL) ](dx-graphics-hlsl-sm2.md) 和更高的著色器模型</span><span class="sxs-lookup"><span data-stu-id="d5b73-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="d5b73-132">是</span><span class="sxs-lookup"><span data-stu-id="d5b73-132">yes</span></span>                 |
| [<span data-ttu-id="d5b73-133">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="d5b73-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="d5b73-134">是 (\_ \_ 只有) 的 vs 1</span><span class="sxs-lookup"><span data-stu-id="d5b73-134">yes (vs\_1\_1 only)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="d5b73-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d5b73-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5b73-136">**(DirectX HLSL) 內建函式**</span><span class="sxs-lookup"><span data-stu-id="d5b73-136">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

