---
title: rsqrt
description: 傳回指定之值的倒數平方根。
ms.assetid: 4e266e41-cde9-4a59-8937-98bfc63f3b5d
keywords:
- rsqrt HLSL
topic_type:
- apiref
api_name:
- rsqrt
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 56eb5f1cba8510e57a2c4b5622e10dc91666b6a6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104990938"
---
# <a name="rsqrt"></a><span data-ttu-id="d47ab-104">rsqrt</span><span class="sxs-lookup"><span data-stu-id="d47ab-104">rsqrt</span></span>

<span data-ttu-id="d47ab-105">傳回指定之值的倒數平方根。</span><span class="sxs-lookup"><span data-stu-id="d47ab-105">Returns the reciprocal of the square root of the specified value.</span></span>



| <span data-ttu-id="d47ab-106">*ret* rsqrt (*x*) </span><span class="sxs-lookup"><span data-stu-id="d47ab-106">*ret* rsqrt(*x*)</span></span> |
|------------------|



 

## <a name="parameters"></a><span data-ttu-id="d47ab-107">參數</span><span class="sxs-lookup"><span data-stu-id="d47ab-107">Parameters</span></span>



| <span data-ttu-id="d47ab-108">項目</span><span class="sxs-lookup"><span data-stu-id="d47ab-108">Item</span></span>                                                   | <span data-ttu-id="d47ab-109">描述</span><span class="sxs-lookup"><span data-stu-id="d47ab-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="d47ab-110"><span id="x"></span><span id="X"></span>*X*</span><span class="sxs-lookup"><span data-stu-id="d47ab-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="d47ab-111">\[在 \] 指定的值中。</span><span class="sxs-lookup"><span data-stu-id="d47ab-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="d47ab-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="d47ab-112">Return Value</span></span>

<span data-ttu-id="d47ab-113">*X* 參數的倒數平方根。</span><span class="sxs-lookup"><span data-stu-id="d47ab-113">The reciprocal of the square root of the *x* parameter.</span></span>

## <a name="remarks"></a><span data-ttu-id="d47ab-114">備註</span><span class="sxs-lookup"><span data-stu-id="d47ab-114">Remarks</span></span>

<span data-ttu-id="d47ab-115">此函數會使用下列公式： 1/ **sqrt** (*x*) 。</span><span class="sxs-lookup"><span data-stu-id="d47ab-115">This function uses the following formula: 1 / **sqrt**(*x*).</span></span>

## <a name="type-description"></a><span data-ttu-id="d47ab-116">類型描述</span><span class="sxs-lookup"><span data-stu-id="d47ab-116">Type Description</span></span>



| <span data-ttu-id="d47ab-117">Name</span><span class="sxs-lookup"><span data-stu-id="d47ab-117">Name</span></span>  | [<span data-ttu-id="d47ab-118">**範本類型**</span><span class="sxs-lookup"><span data-stu-id="d47ab-118">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="d47ab-119">**元件類型**</span><span class="sxs-lookup"><span data-stu-id="d47ab-119">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="d47ab-120">大小</span><span class="sxs-lookup"><span data-stu-id="d47ab-120">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="d47ab-121">*x*</span><span class="sxs-lookup"><span data-stu-id="d47ab-121">*x*</span></span>   | <span data-ttu-id="d47ab-122">純 [**量、**](dx-graphics-hlsl-intrinsic-functions.md)**向量** 或 **矩陣**</span><span class="sxs-lookup"><span data-stu-id="d47ab-122">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="d47ab-123">**浮動**</span><span class="sxs-lookup"><span data-stu-id="d47ab-123">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="d47ab-124">任意</span><span class="sxs-lookup"><span data-stu-id="d47ab-124">any</span></span>                            |
| <span data-ttu-id="d47ab-125">*Ret*</span><span class="sxs-lookup"><span data-stu-id="d47ab-125">*ret*</span></span> | <span data-ttu-id="d47ab-126">與輸入 *x* 相同</span><span class="sxs-lookup"><span data-stu-id="d47ab-126">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="d47ab-127">**浮動**</span><span class="sxs-lookup"><span data-stu-id="d47ab-127">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="d47ab-128">) 為輸入 *x* 的相同維度 (s</span><span class="sxs-lookup"><span data-stu-id="d47ab-128">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="d47ab-129">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="d47ab-129">Minimum Shader Model</span></span>

<span data-ttu-id="d47ab-130">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="d47ab-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="d47ab-131">著色器模型</span><span class="sxs-lookup"><span data-stu-id="d47ab-131">Shader Model</span></span>                                                                       | <span data-ttu-id="d47ab-132">支援</span><span class="sxs-lookup"><span data-stu-id="d47ab-132">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="d47ab-133">[著色器模型 2 (DIRECTX HLSL) ](dx-graphics-hlsl-sm2.md) 和更高的著色器模型</span><span class="sxs-lookup"><span data-stu-id="d47ab-133">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="d47ab-134">是</span><span class="sxs-lookup"><span data-stu-id="d47ab-134">yes</span></span>                 |
| [<span data-ttu-id="d47ab-135">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="d47ab-135">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="d47ab-136">是 (\_ \_ 只有) 的 vs 1</span><span class="sxs-lookup"><span data-stu-id="d47ab-136">yes (vs\_1\_1 only)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="d47ab-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d47ab-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d47ab-138">**(DirectX HLSL) 內建函式**</span><span class="sxs-lookup"><span data-stu-id="d47ab-138">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

