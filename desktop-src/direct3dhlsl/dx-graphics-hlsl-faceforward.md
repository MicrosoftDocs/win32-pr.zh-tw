---
title: faceforward
description: 如有需要，請將表面垂直 (翻轉，) 以與 i 相反的方向呈現;傳回 n 中的結果。
ms.assetid: 6530a928-d221-49e4-ab68-6285c3db370f
keywords:
- faceforward HLSL
topic_type:
- apiref
api_name:
- faceforward
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c6a3f035ed4f0d16b500864f941bc4fe5413ff54
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104092823"
---
# <a name="faceforward"></a><span data-ttu-id="8fd09-104">faceforward</span><span class="sxs-lookup"><span data-stu-id="8fd09-104">faceforward</span></span>

<span data-ttu-id="8fd09-105">如有需要，請將表面垂直 (翻轉，) 以與 i 相反的方向呈現;傳回 n 中的結果。</span><span class="sxs-lookup"><span data-stu-id="8fd09-105">Flips the surface-normal (if needed) to face in a direction opposite to i; returns the result in n.</span></span>



| <span data-ttu-id="8fd09-106">*ret* faceforward (*n*、 *i*、 *ng*) </span><span class="sxs-lookup"><span data-stu-id="8fd09-106">*ret* faceforward(*n*, *i*, *ng*)</span></span> |
|-----------------------------------|



 

<span data-ttu-id="8fd09-107">此函式會使用下列公式：-*n*  sign (點 (*i*， *ng*) ) 。</span><span class="sxs-lookup"><span data-stu-id="8fd09-107">This function uses the following formula: -*n*  sign(dot(*i*, *ng*)).</span></span>

## <a name="parameters"></a><span data-ttu-id="8fd09-108">參數</span><span class="sxs-lookup"><span data-stu-id="8fd09-108">Parameters</span></span>



| <span data-ttu-id="8fd09-109">項目</span><span class="sxs-lookup"><span data-stu-id="8fd09-109">Item</span></span>                                                      | <span data-ttu-id="8fd09-110">描述</span><span class="sxs-lookup"><span data-stu-id="8fd09-110">Description</span></span>                                                                                                     |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8fd09-111"><span id="n"></span><span id="N"></span>*n-1*</span><span class="sxs-lookup"><span data-stu-id="8fd09-111"><span id="n"></span><span id="N"></span>*n*</span></span><br/>    | <span data-ttu-id="8fd09-112">\[在 \] 產生的浮點表面標準向量中。</span><span class="sxs-lookup"><span data-stu-id="8fd09-112">\[in\] The resulting floating-point surface-normal vector.</span></span><br/>                                           |
| <span data-ttu-id="8fd09-113"><span id="i"></span><span id="I"></span>*我*</span><span class="sxs-lookup"><span data-stu-id="8fd09-113"><span id="i"></span><span id="I"></span>*i*</span></span><br/>    | <span data-ttu-id="8fd09-114">\[在 \] 浮點的事件向量中，從視圖位置指向陰影位置。</span><span class="sxs-lookup"><span data-stu-id="8fd09-114">\[in\] A floating-point, incident vector that points from the view position to the shading position.</span></span><br/> |
| <span data-ttu-id="8fd09-115"><span id="ng"></span><span id="NG"></span>*議員*</span><span class="sxs-lookup"><span data-stu-id="8fd09-115"><span id="ng"></span><span id="NG"></span>*ng*</span></span><br/> | <span data-ttu-id="8fd09-116">\[在 \] 浮點介面標準向量中。</span><span class="sxs-lookup"><span data-stu-id="8fd09-116">\[in\] A floating-point surface-normal vector.</span></span><br/>                                                       |



 

## <a name="return-value"></a><span data-ttu-id="8fd09-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="8fd09-117">Return Value</span></span>

<span data-ttu-id="8fd09-118">面向視圖方向的浮點、表面法線向量。</span><span class="sxs-lookup"><span data-stu-id="8fd09-118">A floating-point, surface normal vector that is facing the view direction.</span></span>

## <a name="type-description"></a><span data-ttu-id="8fd09-119">類型描述</span><span class="sxs-lookup"><span data-stu-id="8fd09-119">Type Description</span></span>



| <span data-ttu-id="8fd09-120">Name</span><span class="sxs-lookup"><span data-stu-id="8fd09-120">Name</span></span>  | [<span data-ttu-id="8fd09-121">**範本類型**</span><span class="sxs-lookup"><span data-stu-id="8fd09-121">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="8fd09-122">**元件類型**</span><span class="sxs-lookup"><span data-stu-id="8fd09-122">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="8fd09-123">大小</span><span class="sxs-lookup"><span data-stu-id="8fd09-123">Size</span></span>                           |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="8fd09-124">*n*</span><span class="sxs-lookup"><span data-stu-id="8fd09-124">*n*</span></span>   | [<span data-ttu-id="8fd09-125">**向量**</span><span class="sxs-lookup"><span data-stu-id="8fd09-125">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="8fd09-126">**浮動**</span><span class="sxs-lookup"><span data-stu-id="8fd09-126">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="8fd09-127">任意</span><span class="sxs-lookup"><span data-stu-id="8fd09-127">any</span></span>                            |
| <span data-ttu-id="8fd09-128">*i*</span><span class="sxs-lookup"><span data-stu-id="8fd09-128">*i*</span></span>   | [<span data-ttu-id="8fd09-129">**向量**</span><span class="sxs-lookup"><span data-stu-id="8fd09-129">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="8fd09-130">**浮動**</span><span class="sxs-lookup"><span data-stu-id="8fd09-130">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="8fd09-131">相同維度 (s) 作為輸入 *n*</span><span class="sxs-lookup"><span data-stu-id="8fd09-131">same dimension(s) as input *n*</span></span> |
| <span data-ttu-id="8fd09-132">*議員*</span><span class="sxs-lookup"><span data-stu-id="8fd09-132">*ng*</span></span>  | [<span data-ttu-id="8fd09-133">**向量**</span><span class="sxs-lookup"><span data-stu-id="8fd09-133">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="8fd09-134">**浮動**</span><span class="sxs-lookup"><span data-stu-id="8fd09-134">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="8fd09-135">輸入 *n* 的相同維度</span><span class="sxs-lookup"><span data-stu-id="8fd09-135">same dimensions as input *n*</span></span>   |
| <span data-ttu-id="8fd09-136">*Ret*</span><span class="sxs-lookup"><span data-stu-id="8fd09-136">*ret*</span></span> | [<span data-ttu-id="8fd09-137">**向量**</span><span class="sxs-lookup"><span data-stu-id="8fd09-137">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="8fd09-138">**浮動**</span><span class="sxs-lookup"><span data-stu-id="8fd09-138">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="8fd09-139">輸入 *n* 的相同維度</span><span class="sxs-lookup"><span data-stu-id="8fd09-139">same dimensions as input *n*</span></span>   |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="8fd09-140">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="8fd09-140">Minimum Shader Model</span></span>

<span data-ttu-id="8fd09-141">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="8fd09-141">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="8fd09-142">著色器模型</span><span class="sxs-lookup"><span data-stu-id="8fd09-142">Shader Model</span></span>                                                                       | <span data-ttu-id="8fd09-143">支援</span><span class="sxs-lookup"><span data-stu-id="8fd09-143">Supported</span></span>             |
|------------------------------------------------------------------------------------|-----------------------|
| <span data-ttu-id="8fd09-144">[著色器模型 2 (DIRECTX HLSL) ](dx-graphics-hlsl-sm2.md) 和更高的著色器模型</span><span class="sxs-lookup"><span data-stu-id="8fd09-144">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="8fd09-145">是</span><span class="sxs-lookup"><span data-stu-id="8fd09-145">yes</span></span>                   |
| [<span data-ttu-id="8fd09-146">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="8fd09-146">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="8fd09-147">vs \_ 1 \_ 1 和 ps \_ 1 \_ 4</span><span class="sxs-lookup"><span data-stu-id="8fd09-147">vs\_1\_1 and ps\_1\_4</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="8fd09-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8fd09-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fd09-149">**(DirectX HLSL) 內建函式**</span><span class="sxs-lookup"><span data-stu-id="8fd09-149">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

