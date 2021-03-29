---
title: ddy
description: 傳回指定值的部分導數（相對於螢幕空間 y 座標）。
ms.assetid: 1c88804f-a13f-4714-a3ef-466307afbc1b
keywords:
- ddy HLSL
topic_type:
- apiref
api_name:
- ddy
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d27e48a6d9ae237e4e58d1fd30afbac3b2b40d3d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375697"
---
# <a name="ddy"></a><span data-ttu-id="135eb-104">ddy</span><span class="sxs-lookup"><span data-stu-id="135eb-104">ddy</span></span>

<span data-ttu-id="135eb-105">傳回指定值的部分導數（相對於螢幕空間 y 座標）。</span><span class="sxs-lookup"><span data-stu-id="135eb-105">Returns the partial derivative of the specified value with respect to the screen-space y-coordinate.</span></span>



| <span data-ttu-id="135eb-106">*ret* ddy (*x*) </span><span class="sxs-lookup"><span data-stu-id="135eb-106">*ret* ddy(*x*)</span></span> |
|----------------|



 

<span data-ttu-id="135eb-107">此函數會計算相對於螢幕空間 y 座標的部分衍生。</span><span class="sxs-lookup"><span data-stu-id="135eb-107">This function computes the partial derivative with respect to the screen-space y-coordinate.</span></span> <span data-ttu-id="135eb-108">若要計算相對於螢幕空間 x 座標的部分衍生，請使用 [**ddx**](dx-graphics-hlsl-ddx.md) 函數。</span><span class="sxs-lookup"><span data-stu-id="135eb-108">To compute the partial derivative with respect to the screen-space x-coordinate, use the [**ddx**](dx-graphics-hlsl-ddx.md) function.</span></span>

<span data-ttu-id="135eb-109">只有圖元著色器支援此函式。</span><span class="sxs-lookup"><span data-stu-id="135eb-109">This function is only supported in pixel shaders.</span></span>

## <a name="parameters"></a><span data-ttu-id="135eb-110">參數</span><span class="sxs-lookup"><span data-stu-id="135eb-110">Parameters</span></span>



| <span data-ttu-id="135eb-111">項目</span><span class="sxs-lookup"><span data-stu-id="135eb-111">Item</span></span>                                                   | <span data-ttu-id="135eb-112">描述</span><span class="sxs-lookup"><span data-stu-id="135eb-112">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="135eb-113"><span id="x"></span><span id="X"></span>*X*</span><span class="sxs-lookup"><span data-stu-id="135eb-113"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="135eb-114">\[在 \] 指定的值中。</span><span class="sxs-lookup"><span data-stu-id="135eb-114">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="135eb-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="135eb-115">Return Value</span></span>

<span data-ttu-id="135eb-116">*X* 參數的部分衍生。</span><span class="sxs-lookup"><span data-stu-id="135eb-116">The partial derivative of the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="135eb-117">類型描述</span><span class="sxs-lookup"><span data-stu-id="135eb-117">Type Description</span></span>



| <span data-ttu-id="135eb-118">Name</span><span class="sxs-lookup"><span data-stu-id="135eb-118">Name</span></span>  | [<span data-ttu-id="135eb-119">**範本類型**</span><span class="sxs-lookup"><span data-stu-id="135eb-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="135eb-120">**元件類型**</span><span class="sxs-lookup"><span data-stu-id="135eb-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="135eb-121">大小</span><span class="sxs-lookup"><span data-stu-id="135eb-121">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="135eb-122">*x*</span><span class="sxs-lookup"><span data-stu-id="135eb-122">*x*</span></span>   | <span data-ttu-id="135eb-123">純 [**量、**](dx-graphics-hlsl-intrinsic-functions.md)**向量** 或 **矩陣**</span><span class="sxs-lookup"><span data-stu-id="135eb-123">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="135eb-124">**浮動**</span><span class="sxs-lookup"><span data-stu-id="135eb-124">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="135eb-125">任意</span><span class="sxs-lookup"><span data-stu-id="135eb-125">any</span></span>                            |
| <span data-ttu-id="135eb-126">*Ret*</span><span class="sxs-lookup"><span data-stu-id="135eb-126">*ret*</span></span> | <span data-ttu-id="135eb-127">與輸入 *x* 相同</span><span class="sxs-lookup"><span data-stu-id="135eb-127">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="135eb-128">**浮動**</span><span class="sxs-lookup"><span data-stu-id="135eb-128">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="135eb-129">) 為輸入 *x* 的相同維度 (s</span><span class="sxs-lookup"><span data-stu-id="135eb-129">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="135eb-130">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="135eb-130">Minimum Shader Model</span></span>

<span data-ttu-id="135eb-131">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="135eb-131">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="135eb-132">著色器模型</span><span class="sxs-lookup"><span data-stu-id="135eb-132">Shader Model</span></span>                                                                | <span data-ttu-id="135eb-133">支援</span><span class="sxs-lookup"><span data-stu-id="135eb-133">Supported</span></span>                                 |
|-----------------------------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="135eb-134">[著色器模型 5](d3d11-graphics-reference-sm5.md) 和更新版本的著色器模型</span><span class="sxs-lookup"><span data-stu-id="135eb-134">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="135eb-135">是</span><span class="sxs-lookup"><span data-stu-id="135eb-135">yes</span></span>                                       |
| [<span data-ttu-id="135eb-136">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="135eb-136">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                                  | <span data-ttu-id="135eb-137">是</span><span class="sxs-lookup"><span data-stu-id="135eb-137">yes</span></span>                                       |
| [<span data-ttu-id="135eb-138">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="135eb-138">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md)                   | <span data-ttu-id="135eb-139">是</span><span class="sxs-lookup"><span data-stu-id="135eb-139">yes</span></span>                                       |
| [<span data-ttu-id="135eb-140">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="135eb-140">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md)                   | <span data-ttu-id="135eb-141">是在 ps \_ 2 \_ x 中，不支援在 ps \_ 2 \_ 0 中。</span><span class="sxs-lookup"><span data-stu-id="135eb-141">yes in ps\_2\_x; unsupported in ps\_2\_0.</span></span> |
| [<span data-ttu-id="135eb-142">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="135eb-142">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                   | <span data-ttu-id="135eb-143">不可以</span><span class="sxs-lookup"><span data-stu-id="135eb-143">no</span></span>                                        |



 

<span data-ttu-id="135eb-144">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="135eb-144">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="135eb-145">頂點</span><span class="sxs-lookup"><span data-stu-id="135eb-145">Vertex</span></span> | <span data-ttu-id="135eb-146">船體</span><span class="sxs-lookup"><span data-stu-id="135eb-146">Hull</span></span> | <span data-ttu-id="135eb-147">網域</span><span class="sxs-lookup"><span data-stu-id="135eb-147">Domain</span></span> | <span data-ttu-id="135eb-148">幾何</span><span class="sxs-lookup"><span data-stu-id="135eb-148">Geometry</span></span> | <span data-ttu-id="135eb-149">像素</span><span class="sxs-lookup"><span data-stu-id="135eb-149">Pixel</span></span> | <span data-ttu-id="135eb-150">計算</span><span class="sxs-lookup"><span data-stu-id="135eb-150">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="135eb-151">x</span><span class="sxs-lookup"><span data-stu-id="135eb-151">x</span></span>     |         |



 

## <a name="see-also"></a><span data-ttu-id="135eb-152">另請參閱</span><span class="sxs-lookup"><span data-stu-id="135eb-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="135eb-153">**(DirectX HLSL) 內建函式**</span><span class="sxs-lookup"><span data-stu-id="135eb-153">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

