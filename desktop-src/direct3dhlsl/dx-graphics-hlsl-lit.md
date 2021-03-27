---
title: 點燃
description: 傳回光源係數向量。
ms.assetid: 6ae116df-41b7-42f1-96cb-da480a7c1bab
keywords:
- 亮 HLSL
topic_type:
- apiref
api_name:
- lit
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6dbf6f1e53218355ba1ee9ccf58dac6176007218
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842312"
---
# <a name="lit"></a><span data-ttu-id="61d81-104">點燃</span><span class="sxs-lookup"><span data-stu-id="61d81-104">lit</span></span>

<span data-ttu-id="61d81-105">傳回光源係數向量。</span><span class="sxs-lookup"><span data-stu-id="61d81-105">Returns a lighting coefficient vector.</span></span>



| <span data-ttu-id="61d81-106">*ret* 燈亮 (*n \_ 點 \_ l*、 *n \_ 點 \_ h*、 *m*) </span><span class="sxs-lookup"><span data-stu-id="61d81-106">*ret* lit(*n\_dot\_l*, *n\_dot\_h*, *m*)</span></span> |
|------------------------------------------|



 

<span data-ttu-id="61d81-107">此函式會傳回光源係數向量 (環境、漫射、反光、1) where：</span><span class="sxs-lookup"><span data-stu-id="61d81-107">This function returns a lighting coefficient vector (ambient, diffuse, specular, 1) where:</span></span>

-   <span data-ttu-id="61d81-108">環境 = 1</span><span class="sxs-lookup"><span data-stu-id="61d81-108">ambient = 1</span></span>
-   <span data-ttu-id="61d81-109">擴散 = n ·l < 0？</span><span class="sxs-lookup"><span data-stu-id="61d81-109">diffuse = n · l < 0 ?</span></span> <span data-ttu-id="61d81-110">0： n ·我</span><span class="sxs-lookup"><span data-stu-id="61d81-110">0 : n · l</span></span>
-   <span data-ttu-id="61d81-111">反射 = n ·l < 0 \| \| n · h < 0？</span><span class="sxs-lookup"><span data-stu-id="61d81-111">specular = n · l < 0 \|\| n · h < 0 ?</span></span> <span data-ttu-id="61d81-112">0： (n ·h) ^ m</span><span class="sxs-lookup"><span data-stu-id="61d81-112">0 : (n · h) ^ m</span></span>

<span data-ttu-id="61d81-113">其中向量 n 是一般向量，l 是淺色的方向，h 是半向量。</span><span class="sxs-lookup"><span data-stu-id="61d81-113">Where the vector n is the normal vector, l is the direction to light and h is the half vector.</span></span>

## <a name="parameters"></a><span data-ttu-id="61d81-114">參數</span><span class="sxs-lookup"><span data-stu-id="61d81-114">Parameters</span></span>



| <span data-ttu-id="61d81-115">項目</span><span class="sxs-lookup"><span data-stu-id="61d81-115">Item</span></span>                                                                       | <span data-ttu-id="61d81-116">描述</span><span class="sxs-lookup"><span data-stu-id="61d81-116">Description</span></span>                                                                              |
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="61d81-117"><span id="n_dot_l"></span><span id="N_DOT_L"></span>*n \_ 點 \_ l*</span><span class="sxs-lookup"><span data-stu-id="61d81-117"><span id="n_dot_l"></span><span id="N_DOT_L"></span>*n\_dot\_l*</span></span><br/> | <span data-ttu-id="61d81-118">\[在 \] 正規化曲面標準和燈光向量的點乘積。</span><span class="sxs-lookup"><span data-stu-id="61d81-118">\[in\] The dot product of the normalized surface normal and the light vector.</span></span><br/> |
| <span data-ttu-id="61d81-119"><span id="n_dot_h"></span><span id="N_DOT_H"></span>*n \_ 點 \_ h*</span><span class="sxs-lookup"><span data-stu-id="61d81-119"><span id="n_dot_h"></span><span id="N_DOT_H"></span>*n\_dot\_h*</span></span><br/> | <span data-ttu-id="61d81-120">\[在 \] 半形向量和曲面法線的點乘積。</span><span class="sxs-lookup"><span data-stu-id="61d81-120">\[in\] The dot product of the half-angle vector and the surface normal.</span></span><br/>       |
| <span data-ttu-id="61d81-121"><span id="m"></span><span id="M"></span>*m*</span><span class="sxs-lookup"><span data-stu-id="61d81-121"><span id="m"></span><span id="M"></span>*m*</span></span><br/>                     | <span data-ttu-id="61d81-122">\[在 \] 反射指數中。</span><span class="sxs-lookup"><span data-stu-id="61d81-122">\[in\] A specular exponent.</span></span><br/>                                                   |



 

## <a name="return-value"></a><span data-ttu-id="61d81-123">傳回值</span><span class="sxs-lookup"><span data-stu-id="61d81-123">Return Value</span></span>

<span data-ttu-id="61d81-124">光源係數向量。</span><span class="sxs-lookup"><span data-stu-id="61d81-124">The lighting coefficient vector.</span></span>

## <a name="type-description"></a><span data-ttu-id="61d81-125">類型描述</span><span class="sxs-lookup"><span data-stu-id="61d81-125">Type Description</span></span>



| <span data-ttu-id="61d81-126">Name</span><span class="sxs-lookup"><span data-stu-id="61d81-126">Name</span></span>        | [<span data-ttu-id="61d81-127">**範本類型**</span><span class="sxs-lookup"><span data-stu-id="61d81-127">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="61d81-128">**元件類型**</span><span class="sxs-lookup"><span data-stu-id="61d81-128">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="61d81-129">大小</span><span class="sxs-lookup"><span data-stu-id="61d81-129">Size</span></span> |
|-------------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="61d81-130">*n \_ 點 \_ l*</span><span class="sxs-lookup"><span data-stu-id="61d81-130">*n\_dot\_l*</span></span> | [<span data-ttu-id="61d81-131">**純量 (scalar)**</span><span class="sxs-lookup"><span data-stu-id="61d81-131">**scalar**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="61d81-132">**FLOAT**</span><span class="sxs-lookup"><span data-stu-id="61d81-132">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="61d81-133">1</span><span class="sxs-lookup"><span data-stu-id="61d81-133">1</span></span>    |
| <span data-ttu-id="61d81-134">*n \_ 點 \_ h*</span><span class="sxs-lookup"><span data-stu-id="61d81-134">*n\_dot\_h*</span></span> | [<span data-ttu-id="61d81-135">**純量 (scalar)**</span><span class="sxs-lookup"><span data-stu-id="61d81-135">**scalar**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="61d81-136">**FLOAT**</span><span class="sxs-lookup"><span data-stu-id="61d81-136">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="61d81-137">1</span><span class="sxs-lookup"><span data-stu-id="61d81-137">1</span></span>    |
| <span data-ttu-id="61d81-138">*m*</span><span class="sxs-lookup"><span data-stu-id="61d81-138">*m*</span></span>         | [<span data-ttu-id="61d81-139">**純量 (scalar)**</span><span class="sxs-lookup"><span data-stu-id="61d81-139">**scalar**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="61d81-140">**FLOAT**</span><span class="sxs-lookup"><span data-stu-id="61d81-140">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="61d81-141">1</span><span class="sxs-lookup"><span data-stu-id="61d81-141">1</span></span>    |
| <span data-ttu-id="61d81-142">*Ret*</span><span class="sxs-lookup"><span data-stu-id="61d81-142">*ret*</span></span>       | [<span data-ttu-id="61d81-143">**向量**</span><span class="sxs-lookup"><span data-stu-id="61d81-143">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="61d81-144">**浮動**</span><span class="sxs-lookup"><span data-stu-id="61d81-144">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="61d81-145">4</span><span class="sxs-lookup"><span data-stu-id="61d81-145">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="61d81-146">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="61d81-146">Minimum Shader Model</span></span>

<span data-ttu-id="61d81-147">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="61d81-147">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="61d81-148">著色器模型</span><span class="sxs-lookup"><span data-stu-id="61d81-148">Shader Model</span></span>                                                                       | <span data-ttu-id="61d81-149">支援</span><span class="sxs-lookup"><span data-stu-id="61d81-149">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="61d81-150">[著色器模型 2 (DIRECTX HLSL) ](dx-graphics-hlsl-sm2.md) 和更高的著色器模型</span><span class="sxs-lookup"><span data-stu-id="61d81-150">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="61d81-151">是</span><span class="sxs-lookup"><span data-stu-id="61d81-151">yes</span></span>                 |
| [<span data-ttu-id="61d81-152">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="61d81-152">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="61d81-153">是 (\_ \_ 只有) 的 vs 1</span><span class="sxs-lookup"><span data-stu-id="61d81-153">yes (vs\_1\_1 only)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="61d81-154">另請參閱</span><span class="sxs-lookup"><span data-stu-id="61d81-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61d81-155">**(DirectX HLSL) 內建函式**</span><span class="sxs-lookup"><span data-stu-id="61d81-155">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

