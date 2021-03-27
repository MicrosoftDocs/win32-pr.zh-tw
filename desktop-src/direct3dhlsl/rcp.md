---
title: rcp
description: 計算每個元件的快速、近似、每個元件。
ms.assetid: c8d451e4-717e-45b3-a0fe-da55feb8f443
keywords:
- rcp HLSL
topic_type:
- apiref
api_name:
- rcp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2a857c897def08f31e18ef19466daa2b4584740a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682581"
---
# <a name="rcp"></a><span data-ttu-id="ee0b5-104">rcp</span><span class="sxs-lookup"><span data-stu-id="ee0b5-104">rcp</span></span>

<span data-ttu-id="ee0b5-105">計算每個元件的快速、近似、每個元件。</span><span class="sxs-lookup"><span data-stu-id="ee0b5-105">Calculates a fast, approximate, per-component reciprocal.</span></span>



| <span data-ttu-id="ee0b5-106">*ret* rcp (*x*) </span><span class="sxs-lookup"><span data-stu-id="ee0b5-106">*ret* rcp(*x*)</span></span> |
|----------------|



 

## <a name="parameters"></a><span data-ttu-id="ee0b5-107">參數</span><span class="sxs-lookup"><span data-stu-id="ee0b5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee0b5-108"><span id="x"></span><span id="X"></span>*X*</span><span class="sxs-lookup"><span data-stu-id="ee0b5-108"><span id="x"></span><span id="X"></span>*x*</span></span>
</dt> <dd>

<span data-ttu-id="ee0b5-109">\[在 \] 輸入值中。</span><span class="sxs-lookup"><span data-stu-id="ee0b5-109">\[in\] The input value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee0b5-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="ee0b5-110">Return Value</span></span>

<span data-ttu-id="ee0b5-111">*X* 參數的倒數。</span><span class="sxs-lookup"><span data-stu-id="ee0b5-111">The reciprocal of the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="ee0b5-112">類型描述</span><span class="sxs-lookup"><span data-stu-id="ee0b5-112">Type Description</span></span>



| <span data-ttu-id="ee0b5-113">Name</span><span class="sxs-lookup"><span data-stu-id="ee0b5-113">Name</span></span>  | [<span data-ttu-id="ee0b5-114">**範本類型**</span><span class="sxs-lookup"><span data-stu-id="ee0b5-114">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="ee0b5-115">**元件類型**</span><span class="sxs-lookup"><span data-stu-id="ee0b5-115">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                      | <span data-ttu-id="ee0b5-116">大小</span><span class="sxs-lookup"><span data-stu-id="ee0b5-116">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="ee0b5-117">*x*</span><span class="sxs-lookup"><span data-stu-id="ee0b5-117">*x*</span></span>   | <span data-ttu-id="ee0b5-118">純 [**量、**](dx-graphics-hlsl-intrinsic-functions.md)**向量** 或 **矩陣**</span><span class="sxs-lookup"><span data-stu-id="ee0b5-118">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | <span data-ttu-id="ee0b5-119">[**浮點數**](/windows/desktop/WinProg/windows-data-types)或 [**雙精度** 浮點數](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="ee0b5-119">[**float**](/windows/desktop/WinProg/windows-data-types) or [**double**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="ee0b5-120">任意</span><span class="sxs-lookup"><span data-stu-id="ee0b5-120">any</span></span>                            |
| <span data-ttu-id="ee0b5-121">*Ret*</span><span class="sxs-lookup"><span data-stu-id="ee0b5-121">*ret*</span></span> | <span data-ttu-id="ee0b5-122">與輸入 *x* 相同</span><span class="sxs-lookup"><span data-stu-id="ee0b5-122">same as input *x*</span></span>                                                                                              | <span data-ttu-id="ee0b5-123">[**浮點數**](/windows/desktop/WinProg/windows-data-types)或 [**雙精度** 浮點數](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="ee0b5-123">[**float**](/windows/desktop/WinProg/windows-data-types) or [**double**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="ee0b5-124">) 為輸入 *x* 的相同維度 (s</span><span class="sxs-lookup"><span data-stu-id="ee0b5-124">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="ee0b5-125">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="ee0b5-125">Minimum Shader Model</span></span>

<span data-ttu-id="ee0b5-126">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="ee0b5-126">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="ee0b5-127">著色器模型</span><span class="sxs-lookup"><span data-stu-id="ee0b5-127">Shader Model</span></span>                                                                | <span data-ttu-id="ee0b5-128">支援</span><span class="sxs-lookup"><span data-stu-id="ee0b5-128">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="ee0b5-129">[著色器模型 5](d3d11-graphics-reference-sm5.md) 和更新版本的著色器模型</span><span class="sxs-lookup"><span data-stu-id="ee0b5-129">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="ee0b5-130">是</span><span class="sxs-lookup"><span data-stu-id="ee0b5-130">yes</span></span>       |



 

<span data-ttu-id="ee0b5-131">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="ee0b5-131">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="ee0b5-132">頂點</span><span class="sxs-lookup"><span data-stu-id="ee0b5-132">Vertex</span></span> | <span data-ttu-id="ee0b5-133">船體</span><span class="sxs-lookup"><span data-stu-id="ee0b5-133">Hull</span></span> | <span data-ttu-id="ee0b5-134">網域</span><span class="sxs-lookup"><span data-stu-id="ee0b5-134">Domain</span></span> | <span data-ttu-id="ee0b5-135">幾何</span><span class="sxs-lookup"><span data-stu-id="ee0b5-135">Geometry</span></span> | <span data-ttu-id="ee0b5-136">像素</span><span class="sxs-lookup"><span data-stu-id="ee0b5-136">Pixel</span></span> | <span data-ttu-id="ee0b5-137">計算</span><span class="sxs-lookup"><span data-stu-id="ee0b5-137">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="ee0b5-138">x</span><span class="sxs-lookup"><span data-stu-id="ee0b5-138">x</span></span>      | <span data-ttu-id="ee0b5-139">x</span><span class="sxs-lookup"><span data-stu-id="ee0b5-139">x</span></span>    | <span data-ttu-id="ee0b5-140">x</span><span class="sxs-lookup"><span data-stu-id="ee0b5-140">x</span></span>      | <span data-ttu-id="ee0b5-141">x</span><span class="sxs-lookup"><span data-stu-id="ee0b5-141">x</span></span>        | <span data-ttu-id="ee0b5-142">x</span><span class="sxs-lookup"><span data-stu-id="ee0b5-142">x</span></span>     | <span data-ttu-id="ee0b5-143">x</span><span class="sxs-lookup"><span data-stu-id="ee0b5-143">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="ee0b5-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ee0b5-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee0b5-145">內建函式</span><span class="sxs-lookup"><span data-stu-id="ee0b5-145">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="ee0b5-146">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="ee0b5-146">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 