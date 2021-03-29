---
title: lerp
description: 執行線性插補。
ms.assetid: e369f182-b5bd-4b7f-aa77-9cfe11033bc4
keywords:
- lerp HLSL
topic_type:
- apiref
api_name:
- lerp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7c7a5251aaf410d7224b87b9ee9a8f0e8a0c947e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104990939"
---
# <a name="lerp"></a><span data-ttu-id="1fcae-104">lerp</span><span class="sxs-lookup"><span data-stu-id="1fcae-104">lerp</span></span>

<span data-ttu-id="1fcae-105">執行線性插補。</span><span class="sxs-lookup"><span data-stu-id="1fcae-105">Performs a linear interpolation.</span></span>



| <span data-ttu-id="1fcae-106">*ret* lerp (*x*， *y*， *s*) </span><span class="sxs-lookup"><span data-stu-id="1fcae-106">*ret* lerp(*x*, *y*, *s*)</span></span> |
|---------------------------|



 

## <a name="parameters"></a><span data-ttu-id="1fcae-107">參數</span><span class="sxs-lookup"><span data-stu-id="1fcae-107">Parameters</span></span>



| <span data-ttu-id="1fcae-108">項目</span><span class="sxs-lookup"><span data-stu-id="1fcae-108">Item</span></span>                                                   | <span data-ttu-id="1fcae-109">描述</span><span class="sxs-lookup"><span data-stu-id="1fcae-109">Description</span></span>                                                                                           |
|--------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1fcae-110"><span id="x"></span><span id="X"></span>*X*</span><span class="sxs-lookup"><span data-stu-id="1fcae-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="1fcae-111">\[在 \] 第一個浮點數的值中。</span><span class="sxs-lookup"><span data-stu-id="1fcae-111">\[in\] The first-floating point value.</span></span><br/>                                                     |
| <span data-ttu-id="1fcae-112"><span id="y"></span><span id="Y"></span>*Y*</span><span class="sxs-lookup"><span data-stu-id="1fcae-112"><span id="y"></span><span id="Y"></span>*y*</span></span><br/> | <span data-ttu-id="1fcae-113">\[在 \] 第二個浮點數中。</span><span class="sxs-lookup"><span data-stu-id="1fcae-113">\[in\] The second-floating point value.</span></span><br/>                                                    |
| <span data-ttu-id="1fcae-114"><span id="s"></span><span id="S"></span>*！*</span><span class="sxs-lookup"><span data-stu-id="1fcae-114"><span id="s"></span><span id="S"></span>*s*</span></span><br/> | <span data-ttu-id="1fcae-115">\[在 \] *x* 參數和 *y* 參數之間以線性方式插補的值。</span><span class="sxs-lookup"><span data-stu-id="1fcae-115">\[in\] A value that linearly interpolates between the *x* parameter and the *y* parameter.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="1fcae-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="1fcae-116">Return Value</span></span>

<span data-ttu-id="1fcae-117">線性插補的結果。</span><span class="sxs-lookup"><span data-stu-id="1fcae-117">The result of the linear interpolation.</span></span>

## <a name="type-description"></a><span data-ttu-id="1fcae-118">類型描述</span><span class="sxs-lookup"><span data-stu-id="1fcae-118">Type Description</span></span>



| <span data-ttu-id="1fcae-119">名稱</span><span class="sxs-lookup"><span data-stu-id="1fcae-119">Name</span></span>  | [<span data-ttu-id="1fcae-120">**範本類型**</span><span class="sxs-lookup"><span data-stu-id="1fcae-120">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="1fcae-121">**元件類型**</span><span class="sxs-lookup"><span data-stu-id="1fcae-121">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="1fcae-122">大小</span><span class="sxs-lookup"><span data-stu-id="1fcae-122">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="1fcae-123">*x*</span><span class="sxs-lookup"><span data-stu-id="1fcae-123">*x*</span></span>   | <span data-ttu-id="1fcae-124">純 [**量、**](dx-graphics-hlsl-intrinsic-functions.md)**向量** 或 **矩陣**</span><span class="sxs-lookup"><span data-stu-id="1fcae-124">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="1fcae-125">**浮動**</span><span class="sxs-lookup"><span data-stu-id="1fcae-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="1fcae-126">任意</span><span class="sxs-lookup"><span data-stu-id="1fcae-126">any</span></span>                            |
| <span data-ttu-id="1fcae-127">*y*</span><span class="sxs-lookup"><span data-stu-id="1fcae-127">*y*</span></span>   | <span data-ttu-id="1fcae-128">與輸入 *x* 相同</span><span class="sxs-lookup"><span data-stu-id="1fcae-128">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="1fcae-129">**浮動**</span><span class="sxs-lookup"><span data-stu-id="1fcae-129">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="1fcae-130">) 為輸入 *x* 的相同維度 (s</span><span class="sxs-lookup"><span data-stu-id="1fcae-130">same dimension(s) as input *x*</span></span> |
| <span data-ttu-id="1fcae-131">*s*</span><span class="sxs-lookup"><span data-stu-id="1fcae-131">*s*</span></span>   | <span data-ttu-id="1fcae-132">與輸入 *x* 相同</span><span class="sxs-lookup"><span data-stu-id="1fcae-132">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="1fcae-133">**浮動**</span><span class="sxs-lookup"><span data-stu-id="1fcae-133">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="1fcae-134">) 為輸入 *x* 的相同維度 (s</span><span class="sxs-lookup"><span data-stu-id="1fcae-134">same dimension(s) as input *x*</span></span> |
| <span data-ttu-id="1fcae-135">*Ret*</span><span class="sxs-lookup"><span data-stu-id="1fcae-135">*ret*</span></span> | <span data-ttu-id="1fcae-136">與輸入 *x* 相同</span><span class="sxs-lookup"><span data-stu-id="1fcae-136">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="1fcae-137">**浮動**</span><span class="sxs-lookup"><span data-stu-id="1fcae-137">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="1fcae-138">) 為輸入 *x* 的相同維度 (s</span><span class="sxs-lookup"><span data-stu-id="1fcae-138">same dimension(s) as input *x*</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="1fcae-139">備註</span><span class="sxs-lookup"><span data-stu-id="1fcae-139">Remarks</span></span>

<span data-ttu-id="1fcae-140">線性插補是以下列公式為基礎： x \* (1-s) + y \* s，可等同于撰寫為 x + s (y x) 。</span><span class="sxs-lookup"><span data-stu-id="1fcae-140">Linear interpolation is based on the following formula: x\*(1-s) + y\*s which can equivalently be written as x + s(y-x).</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="1fcae-141">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="1fcae-141">Minimum Shader Model</span></span>

<span data-ttu-id="1fcae-142">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="1fcae-142">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="1fcae-143">著色器模型</span><span class="sxs-lookup"><span data-stu-id="1fcae-143">Shader Model</span></span>                                                                       | <span data-ttu-id="1fcae-144">支援</span><span class="sxs-lookup"><span data-stu-id="1fcae-144">Supported</span></span>                   |
|------------------------------------------------------------------------------------|-----------------------------|
| <span data-ttu-id="1fcae-145">[著色器模型 2 (DIRECTX HLSL) ](dx-graphics-hlsl-sm2.md) 和更高的著色器模型</span><span class="sxs-lookup"><span data-stu-id="1fcae-145">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="1fcae-146">是</span><span class="sxs-lookup"><span data-stu-id="1fcae-146">yes</span></span>                         |
| [<span data-ttu-id="1fcae-147">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="1fcae-147">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="1fcae-148">是 (vs \_ 1 \_ 1 和 ps \_ 1 \_ 1) </span><span class="sxs-lookup"><span data-stu-id="1fcae-148">yes (vs\_1\_1 and ps\_1\_1)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="1fcae-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1fcae-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1fcae-150">**(DirectX HLSL) 內建函式**</span><span class="sxs-lookup"><span data-stu-id="1fcae-150">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

