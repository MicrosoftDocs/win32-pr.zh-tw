---
title: 'round (Corecrt \_ math) '
description: 將指定的值四捨五入到最接近的整數。
ms.assetid: 258ce717-dca1-4ed2-ad98-1ecfdb58f939
keywords:
- 四捨五入 HLSL
topic_type:
- apiref
api_name:
- round
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f00bf845dfe16a92729b523fba62f6fd6dcde2b5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103946140"
---
# <a name="round"></a><span data-ttu-id="9caad-104">round</span><span class="sxs-lookup"><span data-stu-id="9caad-104">round</span></span>

<span data-ttu-id="9caad-105">將指定的值四捨五入到最接近的整數。</span><span class="sxs-lookup"><span data-stu-id="9caad-105">Rounds the specified value to the nearest integer.</span></span> <span data-ttu-id="9caad-106">中間的案例會四捨五入至最接近的偶數。</span><span class="sxs-lookup"><span data-stu-id="9caad-106">Halfway cases are rounded to the nearest even.</span></span>



| <span data-ttu-id="9caad-107">*ret* round (*x*) </span><span class="sxs-lookup"><span data-stu-id="9caad-107">*ret* round(*x*)</span></span> |
|------------------|



 

## <a name="parameters"></a><span data-ttu-id="9caad-108">參數</span><span class="sxs-lookup"><span data-stu-id="9caad-108">Parameters</span></span>



| <span data-ttu-id="9caad-109">項目</span><span class="sxs-lookup"><span data-stu-id="9caad-109">Item</span></span>                                                   | <span data-ttu-id="9caad-110">描述</span><span class="sxs-lookup"><span data-stu-id="9caad-110">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="9caad-111"><span id="x"></span><span id="X"></span>*X*</span><span class="sxs-lookup"><span data-stu-id="9caad-111"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="9caad-112">\[在 \] 指定的值中。</span><span class="sxs-lookup"><span data-stu-id="9caad-112">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="9caad-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="9caad-113">Return Value</span></span>

<span data-ttu-id="9caad-114">*X* 參數，四捨五入為浮點數類型內最接近的整數。</span><span class="sxs-lookup"><span data-stu-id="9caad-114">The *x* parameter, rounded to the nearest integer within a floating-point type.</span></span>

## <a name="type-description"></a><span data-ttu-id="9caad-115">類型描述</span><span class="sxs-lookup"><span data-stu-id="9caad-115">Type Description</span></span>



| <span data-ttu-id="9caad-116">Name</span><span class="sxs-lookup"><span data-stu-id="9caad-116">Name</span></span>  | [<span data-ttu-id="9caad-117">**範本類型**</span><span class="sxs-lookup"><span data-stu-id="9caad-117">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="9caad-118">**元件類型**</span><span class="sxs-lookup"><span data-stu-id="9caad-118">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="9caad-119">大小</span><span class="sxs-lookup"><span data-stu-id="9caad-119">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="9caad-120">*x*</span><span class="sxs-lookup"><span data-stu-id="9caad-120">*x*</span></span>   | <span data-ttu-id="9caad-121">純 [**量、**](dx-graphics-hlsl-intrinsic-functions.md)**向量** 或 **矩陣**</span><span class="sxs-lookup"><span data-stu-id="9caad-121">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="9caad-122">**浮動**</span><span class="sxs-lookup"><span data-stu-id="9caad-122">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="9caad-123">任意</span><span class="sxs-lookup"><span data-stu-id="9caad-123">any</span></span>                            |
| <span data-ttu-id="9caad-124">*Ret*</span><span class="sxs-lookup"><span data-stu-id="9caad-124">*ret*</span></span> | <span data-ttu-id="9caad-125">與輸入 *x* 相同</span><span class="sxs-lookup"><span data-stu-id="9caad-125">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="9caad-126">**浮動**</span><span class="sxs-lookup"><span data-stu-id="9caad-126">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="9caad-127">) 為輸入 *x* 的相同維度 (s</span><span class="sxs-lookup"><span data-stu-id="9caad-127">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="9caad-128">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="9caad-128">Minimum Shader Model</span></span>

<span data-ttu-id="9caad-129">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="9caad-129">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="9caad-130">著色器模型</span><span class="sxs-lookup"><span data-stu-id="9caad-130">Shader Model</span></span>                                                                       | <span data-ttu-id="9caad-131">支援</span><span class="sxs-lookup"><span data-stu-id="9caad-131">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="9caad-132">[著色器模型 2 (DIRECTX HLSL) ](dx-graphics-hlsl-sm2.md) 和更高的著色器模型</span><span class="sxs-lookup"><span data-stu-id="9caad-132">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="9caad-133">是</span><span class="sxs-lookup"><span data-stu-id="9caad-133">yes</span></span>                 |
| [<span data-ttu-id="9caad-134">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="9caad-134">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="9caad-135">是 (\_ \_ 只有) 的 vs 1</span><span class="sxs-lookup"><span data-stu-id="9caad-135">yes (vs\_1\_1 only)</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="9caad-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="9caad-136">Requirements</span></span>



| <span data-ttu-id="9caad-137">需求</span><span class="sxs-lookup"><span data-stu-id="9caad-137">Requirement</span></span> | <span data-ttu-id="9caad-138">值</span><span class="sxs-lookup"><span data-stu-id="9caad-138">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="9caad-139">標頭</span><span class="sxs-lookup"><span data-stu-id="9caad-139">Header</span></span><br/> | <dl> <span data-ttu-id="9caad-140"><dt>Corecrt \_ math。h</dt></span><span class="sxs-lookup"><span data-stu-id="9caad-140"><dt>Corecrt\_math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9caad-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9caad-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9caad-142">**(DirectX HLSL) 內建函式**</span><span class="sxs-lookup"><span data-stu-id="9caad-142">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

