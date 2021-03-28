---
title: 'fmod (Corecrt \_ math .h) '
description: 傳回 x/y 的浮點餘數。
ms.assetid: bb940548-c4c5-4109-a488-4ea7295c7213
keywords:
- fmod HLSL
topic_type:
- apiref
api_name:
- fmod
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9dc4367e3aa80484098e88926567953fc8e9a90
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322872"
---
# <a name="fmod"></a><span data-ttu-id="c48f4-104">fmod</span><span class="sxs-lookup"><span data-stu-id="c48f4-104">fmod</span></span>

<span data-ttu-id="c48f4-105">傳回 x/y 的浮點餘數。</span><span class="sxs-lookup"><span data-stu-id="c48f4-105">Returns the floating-point remainder of x/y.</span></span>



| <span data-ttu-id="c48f4-106">*ret* fmod (*x*， *y*) </span><span class="sxs-lookup"><span data-stu-id="c48f4-106">*ret* fmod(*x*, *y*)</span></span> |
|----------------------|



 

## <a name="parameters"></a><span data-ttu-id="c48f4-107">參數</span><span class="sxs-lookup"><span data-stu-id="c48f4-107">Parameters</span></span>



| <span data-ttu-id="c48f4-108">項目</span><span class="sxs-lookup"><span data-stu-id="c48f4-108">Item</span></span>                                                   | <span data-ttu-id="c48f4-109">描述</span><span class="sxs-lookup"><span data-stu-id="c48f4-109">Description</span></span>                                    |
|--------------------------------------------------------|------------------------------------------------|
| <span data-ttu-id="c48f4-110"><span id="x"></span><span id="X"></span>*X*</span><span class="sxs-lookup"><span data-stu-id="c48f4-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="c48f4-111">\[在被 \] 除數的浮點數中。</span><span class="sxs-lookup"><span data-stu-id="c48f4-111">\[in\] The floating-point dividend.</span></span><br/> |
| <span data-ttu-id="c48f4-112"><span id="y"></span><span id="Y"></span>*Y*</span><span class="sxs-lookup"><span data-stu-id="c48f4-112"><span id="y"></span><span id="Y"></span>*y*</span></span><br/> | <span data-ttu-id="c48f4-113">\[在 \] 浮點除數中。</span><span class="sxs-lookup"><span data-stu-id="c48f4-113">\[in\] The floating-point divisor.</span></span><br/>  |



 

## <a name="return-value"></a><span data-ttu-id="c48f4-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="c48f4-114">Return Value</span></span>

<span data-ttu-id="c48f4-115">*X* 參數的浮點餘數除以 *y* 參數。</span><span class="sxs-lookup"><span data-stu-id="c48f4-115">The floating-point remainder of the *x* parameter divided by the *y* parameter.</span></span>

## <a name="remarks"></a><span data-ttu-id="c48f4-116">備註</span><span class="sxs-lookup"><span data-stu-id="c48f4-116">Remarks</span></span>

<span data-ttu-id="c48f4-117">浮點數餘數的計算方式為 x = i \* y + f，其中 i 是整數，f 的正負號和 x 相同，而且 f 的絕對值小於 y 的絕對值。</span><span class="sxs-lookup"><span data-stu-id="c48f4-117">The floating-point remainder is calculated such that x = i \* y + f, where i is an integer, f has the same sign as x, and the absolute value of f is less than the absolute value of y.</span></span>

## <a name="type-description"></a><span data-ttu-id="c48f4-118">類型描述</span><span class="sxs-lookup"><span data-stu-id="c48f4-118">Type Description</span></span>



| <span data-ttu-id="c48f4-119">Name</span><span class="sxs-lookup"><span data-stu-id="c48f4-119">Name</span></span>  | [<span data-ttu-id="c48f4-120">**範本類型**</span><span class="sxs-lookup"><span data-stu-id="c48f4-120">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="c48f4-121">**元件類型**</span><span class="sxs-lookup"><span data-stu-id="c48f4-121">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="c48f4-122">大小</span><span class="sxs-lookup"><span data-stu-id="c48f4-122">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="c48f4-123">*x*</span><span class="sxs-lookup"><span data-stu-id="c48f4-123">*x*</span></span>   | <span data-ttu-id="c48f4-124">純 [**量、**](dx-graphics-hlsl-intrinsic-functions.md)**向量** 或 **矩陣**</span><span class="sxs-lookup"><span data-stu-id="c48f4-124">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="c48f4-125">**浮動**</span><span class="sxs-lookup"><span data-stu-id="c48f4-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="c48f4-126">任意</span><span class="sxs-lookup"><span data-stu-id="c48f4-126">any</span></span>                            |
| <span data-ttu-id="c48f4-127">*y*</span><span class="sxs-lookup"><span data-stu-id="c48f4-127">*y*</span></span>   | <span data-ttu-id="c48f4-128">與輸入 *x* 相同</span><span class="sxs-lookup"><span data-stu-id="c48f4-128">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="c48f4-129">**浮動**</span><span class="sxs-lookup"><span data-stu-id="c48f4-129">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="c48f4-130">) 為輸入 *x* 的相同維度 (s</span><span class="sxs-lookup"><span data-stu-id="c48f4-130">same dimension(s) as input *x*</span></span> |
| <span data-ttu-id="c48f4-131">*Ret*</span><span class="sxs-lookup"><span data-stu-id="c48f4-131">*ret*</span></span> | <span data-ttu-id="c48f4-132">與輸入 *x* 相同</span><span class="sxs-lookup"><span data-stu-id="c48f4-132">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="c48f4-133">**浮動**</span><span class="sxs-lookup"><span data-stu-id="c48f4-133">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="c48f4-134">) 為輸入 *x* 的相同維度 (s</span><span class="sxs-lookup"><span data-stu-id="c48f4-134">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="c48f4-135">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="c48f4-135">Minimum Shader Model</span></span>

<span data-ttu-id="c48f4-136">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="c48f4-136">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="c48f4-137">著色器模型</span><span class="sxs-lookup"><span data-stu-id="c48f4-137">Shader Model</span></span>                                                                       | <span data-ttu-id="c48f4-138">支援</span><span class="sxs-lookup"><span data-stu-id="c48f4-138">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="c48f4-139">[著色器模型 2 (DIRECTX HLSL) ](dx-graphics-hlsl-sm2.md) 和更高的著色器模型</span><span class="sxs-lookup"><span data-stu-id="c48f4-139">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="c48f4-140">是</span><span class="sxs-lookup"><span data-stu-id="c48f4-140">yes</span></span>       |
| [<span data-ttu-id="c48f4-141">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="c48f4-141">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="c48f4-142">vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="c48f4-142">vs\_1\_1</span></span>  |



 

## <a name="requirements"></a><span data-ttu-id="c48f4-143">規格需求</span><span class="sxs-lookup"><span data-stu-id="c48f4-143">Requirements</span></span>



| <span data-ttu-id="c48f4-144">需求</span><span class="sxs-lookup"><span data-stu-id="c48f4-144">Requirement</span></span> | <span data-ttu-id="c48f4-145">值</span><span class="sxs-lookup"><span data-stu-id="c48f4-145">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="c48f4-146">標頭</span><span class="sxs-lookup"><span data-stu-id="c48f4-146">Header</span></span><br/> | <dl> <span data-ttu-id="c48f4-147"><dt>Corecrt \_ math。h</dt></span><span class="sxs-lookup"><span data-stu-id="c48f4-147"><dt>Corecrt\_math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c48f4-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c48f4-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c48f4-149">**(DirectX HLSL) 內建函式**</span><span class="sxs-lookup"><span data-stu-id="c48f4-149">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

