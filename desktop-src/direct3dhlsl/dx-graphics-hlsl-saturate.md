---
title: " (HLSL 參考) 飽和"
description: 個0到1範圍內的指定值。
ms.assetid: efe4dedd-732a-4643-8a57-61814434f6ff
keywords:
- 飽和 HLSL
topic_type:
- apiref
api_name:
- saturate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 609443bdc1d0cff6a4c81c8eb26d86a30ea1e721
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315187"
---
# <a name="saturate-hlsl-reference"></a><span data-ttu-id="afbfc-104"> (HLSL 參考) 飽和</span><span class="sxs-lookup"><span data-stu-id="afbfc-104">saturate (HLSL reference)</span></span>

<span data-ttu-id="afbfc-105">個0到1範圍內的指定值。</span><span class="sxs-lookup"><span data-stu-id="afbfc-105">Clamps the specified value within the range of 0 to 1.</span></span>



| <span data-ttu-id="afbfc-106">*ret* 飽和 (*x*) </span><span class="sxs-lookup"><span data-stu-id="afbfc-106">*ret* saturate(*x*)</span></span> |
|---------------------|



 

## <a name="parameters"></a><span data-ttu-id="afbfc-107">參數</span><span class="sxs-lookup"><span data-stu-id="afbfc-107">Parameters</span></span>



| <span data-ttu-id="afbfc-108">項目</span><span class="sxs-lookup"><span data-stu-id="afbfc-108">Item</span></span>                                                   | <span data-ttu-id="afbfc-109">描述</span><span class="sxs-lookup"><span data-stu-id="afbfc-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="afbfc-110"><span id="x"></span><span id="X"></span>*X*</span><span class="sxs-lookup"><span data-stu-id="afbfc-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="afbfc-111">\[在 \] 指定的值中。</span><span class="sxs-lookup"><span data-stu-id="afbfc-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="afbfc-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="afbfc-112">Return Value</span></span>

<span data-ttu-id="afbfc-113">*X* 參數，在0到1的範圍內壓制。</span><span class="sxs-lookup"><span data-stu-id="afbfc-113">The *x* parameter, clamped within the range of 0 to 1.</span></span>

## <a name="type-description"></a><span data-ttu-id="afbfc-114">類型描述</span><span class="sxs-lookup"><span data-stu-id="afbfc-114">Type Description</span></span>



| <span data-ttu-id="afbfc-115">Name</span><span class="sxs-lookup"><span data-stu-id="afbfc-115">Name</span></span>  | [<span data-ttu-id="afbfc-116">**範本類型**</span><span class="sxs-lookup"><span data-stu-id="afbfc-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="afbfc-117">**元件類型**</span><span class="sxs-lookup"><span data-stu-id="afbfc-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="afbfc-118">大小</span><span class="sxs-lookup"><span data-stu-id="afbfc-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="afbfc-119">*x*</span><span class="sxs-lookup"><span data-stu-id="afbfc-119">*x*</span></span>   | <span data-ttu-id="afbfc-120">純 [**量、**](dx-graphics-hlsl-intrinsic-functions.md)**向量** 或 **矩陣**</span><span class="sxs-lookup"><span data-stu-id="afbfc-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="afbfc-121">**浮動**</span><span class="sxs-lookup"><span data-stu-id="afbfc-121">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="afbfc-122">任意</span><span class="sxs-lookup"><span data-stu-id="afbfc-122">any</span></span>                            |
| <span data-ttu-id="afbfc-123">*Ret*</span><span class="sxs-lookup"><span data-stu-id="afbfc-123">*ret*</span></span> | <span data-ttu-id="afbfc-124">與輸入 *x* 相同</span><span class="sxs-lookup"><span data-stu-id="afbfc-124">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="afbfc-125">**浮動**</span><span class="sxs-lookup"><span data-stu-id="afbfc-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="afbfc-126">) 為輸入 *x* 的相同維度 (s</span><span class="sxs-lookup"><span data-stu-id="afbfc-126">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="afbfc-127">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="afbfc-127">Minimum Shader Model</span></span>

<span data-ttu-id="afbfc-128">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="afbfc-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="afbfc-129">著色器模型</span><span class="sxs-lookup"><span data-stu-id="afbfc-129">Shader Model</span></span>                                                                       | <span data-ttu-id="afbfc-130">支援</span><span class="sxs-lookup"><span data-stu-id="afbfc-130">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="afbfc-131">[著色器模型 1 (DIRECTX HLSL) ](dx-graphics-hlsl-sm1.md) 和更高的著色器模型</span><span class="sxs-lookup"><span data-stu-id="afbfc-131">[Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) and higher shader models</span></span> | <span data-ttu-id="afbfc-132">是</span><span class="sxs-lookup"><span data-stu-id="afbfc-132">yes</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="afbfc-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="afbfc-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="afbfc-134">**(DirectX HLSL) 內建函式**</span><span class="sxs-lookup"><span data-stu-id="afbfc-134">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

