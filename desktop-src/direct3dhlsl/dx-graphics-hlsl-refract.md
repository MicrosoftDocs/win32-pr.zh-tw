---
title: 折射
description: 使用輸入光線、表面標準和折射索引，傳回折射向量。
ms.assetid: 9f9467d7-dd9b-472a-bbdc-752394d382c6
keywords:
- refract HLSL
topic_type:
- apiref
api_name:
- refract
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9e499d078a020ade1ff9ff2566c3fd15b2a820d2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104991007"
---
# <a name="refract"></a><span data-ttu-id="34c5a-104">折射</span><span class="sxs-lookup"><span data-stu-id="34c5a-104">refract</span></span>

<span data-ttu-id="34c5a-105">使用輸入光線、表面標準和折射索引，傳回折射向量。</span><span class="sxs-lookup"><span data-stu-id="34c5a-105">Returns a refraction vector using an entering ray, a surface normal, and a refraction index.</span></span>



| <span data-ttu-id="34c5a-106">*ret* refract (*i*， *n*，？ ) </span><span class="sxs-lookup"><span data-stu-id="34c5a-106">*ret* refract(*i*, *n*, ?)</span></span> |
|----------------------------|



 

## <a name="parameters"></a><span data-ttu-id="34c5a-107">參數</span><span class="sxs-lookup"><span data-stu-id="34c5a-107">Parameters</span></span>



| <span data-ttu-id="34c5a-108">項目</span><span class="sxs-lookup"><span data-stu-id="34c5a-108">Item</span></span>                                                   | <span data-ttu-id="34c5a-109">描述</span><span class="sxs-lookup"><span data-stu-id="34c5a-109">Description</span></span>                                                  |
|--------------------------------------------------------|--------------------------------------------------------------|
| <span data-ttu-id="34c5a-110"><span id="i"></span><span id="I"></span>*我*</span><span class="sxs-lookup"><span data-stu-id="34c5a-110"><span id="i"></span><span id="I"></span>*i*</span></span><br/> | <span data-ttu-id="34c5a-111">\[在 \] 浮點的光線方向向量中。</span><span class="sxs-lookup"><span data-stu-id="34c5a-111">\[in\] A floating-point, ray direction vector.</span></span><br/>    |
| <span data-ttu-id="34c5a-112"><span id="n"></span><span id="N"></span>*n-1*</span><span class="sxs-lookup"><span data-stu-id="34c5a-112"><span id="n"></span><span id="N"></span>*n*</span></span><br/> | <span data-ttu-id="34c5a-113">\[在 \] 浮點的表面標準向量中。</span><span class="sxs-lookup"><span data-stu-id="34c5a-113">\[in\] A floating-point, surface normal vector.</span></span><br/>   |
| <span data-ttu-id="34c5a-114">*?*</span><span class="sxs-lookup"><span data-stu-id="34c5a-114">*?*</span></span><br/>                                         | <span data-ttu-id="34c5a-115">\[\]浮點數中的折射索引純量。</span><span class="sxs-lookup"><span data-stu-id="34c5a-115">\[in\] A floating-point, refraction index scalar.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="34c5a-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="34c5a-116">Return Value</span></span>

<span data-ttu-id="34c5a-117">浮點數折射向量。</span><span class="sxs-lookup"><span data-stu-id="34c5a-117">A floating-point, refraction vector.</span></span> <span data-ttu-id="34c5a-118">如果輸入光線 i 和表面標準 n 之間的角度太適合指定的折射索引，則傳回值會是 (0，0，0) 。</span><span class="sxs-lookup"><span data-stu-id="34c5a-118">If the angle between the entering ray i and the surface normal n is too great for a given refraction index ?, the return value is (0,0,0).</span></span>

## <a name="type-description"></a><span data-ttu-id="34c5a-119">類型描述</span><span class="sxs-lookup"><span data-stu-id="34c5a-119">Type Description</span></span>



| <span data-ttu-id="34c5a-120">Name</span><span class="sxs-lookup"><span data-stu-id="34c5a-120">Name</span></span>              | [<span data-ttu-id="34c5a-121">**範本類型**</span><span class="sxs-lookup"><span data-stu-id="34c5a-121">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="34c5a-122">**元件類型**</span><span class="sxs-lookup"><span data-stu-id="34c5a-122">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="34c5a-123">大小</span><span class="sxs-lookup"><span data-stu-id="34c5a-123">Size</span></span>                           |
|-------------------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="34c5a-124">*i*</span><span class="sxs-lookup"><span data-stu-id="34c5a-124">*i*</span></span>               | [<span data-ttu-id="34c5a-125">**向量**</span><span class="sxs-lookup"><span data-stu-id="34c5a-125">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="34c5a-126">**浮動**</span><span class="sxs-lookup"><span data-stu-id="34c5a-126">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="34c5a-127">任意</span><span class="sxs-lookup"><span data-stu-id="34c5a-127">any</span></span>                            |
| <span data-ttu-id="34c5a-128">*n*</span><span class="sxs-lookup"><span data-stu-id="34c5a-128">*n*</span></span>               | [<span data-ttu-id="34c5a-129">**向量**</span><span class="sxs-lookup"><span data-stu-id="34c5a-129">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="34c5a-130">**浮動**</span><span class="sxs-lookup"><span data-stu-id="34c5a-130">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="34c5a-131">相同維度 (s) 為輸入 *i*</span><span class="sxs-lookup"><span data-stu-id="34c5a-131">same dimension(s) as input *i*</span></span> |
| <span data-ttu-id="34c5a-132">?</span><span class="sxs-lookup"><span data-stu-id="34c5a-132">?</span></span>                 | [<span data-ttu-id="34c5a-133">**純量 (scalar)**</span><span class="sxs-lookup"><span data-stu-id="34c5a-133">**scalar**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="34c5a-134">**FLOAT**</span><span class="sxs-lookup"><span data-stu-id="34c5a-134">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="34c5a-135">1</span><span class="sxs-lookup"><span data-stu-id="34c5a-135">1</span></span>                              |
| <span data-ttu-id="34c5a-136">折射向量</span><span class="sxs-lookup"><span data-stu-id="34c5a-136">refraction vector</span></span> | [<span data-ttu-id="34c5a-137">**向量**</span><span class="sxs-lookup"><span data-stu-id="34c5a-137">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="34c5a-138">**浮動**</span><span class="sxs-lookup"><span data-stu-id="34c5a-138">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="34c5a-139">相同維度 (s) 為輸入 *i*</span><span class="sxs-lookup"><span data-stu-id="34c5a-139">same dimension(s) as input *i*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="34c5a-140">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="34c5a-140">Minimum Shader Model</span></span>

<span data-ttu-id="34c5a-141">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="34c5a-141">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="34c5a-142">著色器模型</span><span class="sxs-lookup"><span data-stu-id="34c5a-142">Shader Model</span></span>                                                                       | <span data-ttu-id="34c5a-143">支援</span><span class="sxs-lookup"><span data-stu-id="34c5a-143">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="34c5a-144">[著色器模型 2 (DIRECTX HLSL) ](dx-graphics-hlsl-sm2.md) 和更高的著色器模型</span><span class="sxs-lookup"><span data-stu-id="34c5a-144">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="34c5a-145">是</span><span class="sxs-lookup"><span data-stu-id="34c5a-145">yes</span></span>                 |
| [<span data-ttu-id="34c5a-146">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="34c5a-146">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="34c5a-147">是 (\_ \_ 只有) 的 vs 1</span><span class="sxs-lookup"><span data-stu-id="34c5a-147">yes (vs\_1\_1 only)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="34c5a-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="34c5a-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34c5a-149">**(DirectX HLSL) 內建函式**</span><span class="sxs-lookup"><span data-stu-id="34c5a-149">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

