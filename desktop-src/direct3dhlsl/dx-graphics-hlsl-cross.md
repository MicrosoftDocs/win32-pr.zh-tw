---
title: 交叉
description: 傳回兩個浮點數3D 向量的交叉乘積。
ms.assetid: 5f1832af-6bc5-49a7-956a-fd762f674f5f
keywords:
- 跨 HLSL
topic_type:
- apiref
api_name:
- cross
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 91959bf415c3e56edf370942de268523bf998743
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104991014"
---
# <a name="cross"></a><span data-ttu-id="b7516-104">交叉</span><span class="sxs-lookup"><span data-stu-id="b7516-104">cross</span></span>

<span data-ttu-id="b7516-105">傳回兩個浮點數3D 向量的交叉乘積。</span><span class="sxs-lookup"><span data-stu-id="b7516-105">Returns the cross product of two floating-point, 3D vectors.</span></span>



| <span data-ttu-id="b7516-106">*ret* cross (*x*， *y*) </span><span class="sxs-lookup"><span data-stu-id="b7516-106">*ret* cross(*x*, *y*)</span></span> |
|-----------------------|



 

## <a name="parameters"></a><span data-ttu-id="b7516-107">參數</span><span class="sxs-lookup"><span data-stu-id="b7516-107">Parameters</span></span>



| <span data-ttu-id="b7516-108">項目</span><span class="sxs-lookup"><span data-stu-id="b7516-108">Item</span></span>                                                   | <span data-ttu-id="b7516-109">描述</span><span class="sxs-lookup"><span data-stu-id="b7516-109">Description</span></span>                                             |
|--------------------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="b7516-110"><span id="x"></span><span id="X"></span>*X*</span><span class="sxs-lookup"><span data-stu-id="b7516-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="b7516-111">\[在 \] 第一個浮點的3d 向量中。</span><span class="sxs-lookup"><span data-stu-id="b7516-111">\[in\] The first floating-point, 3D vector.</span></span><br/>  |
| <span data-ttu-id="b7516-112"><span id="y"></span><span id="Y"></span>*Y*</span><span class="sxs-lookup"><span data-stu-id="b7516-112"><span id="y"></span><span id="Y"></span>*y*</span></span><br/> | <span data-ttu-id="b7516-113">\[在 \] 第二個浮點數的立體向量中。</span><span class="sxs-lookup"><span data-stu-id="b7516-113">\[in\] The second floating-point, 3D vector.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="b7516-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="b7516-114">Return Value</span></span>

<span data-ttu-id="b7516-115">*X* 參數和 *y* 參數的交叉乘積。</span><span class="sxs-lookup"><span data-stu-id="b7516-115">The cross product of the *x* parameter and the *y* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="b7516-116">類型描述</span><span class="sxs-lookup"><span data-stu-id="b7516-116">Type Description</span></span>



| <span data-ttu-id="b7516-117">Name</span><span class="sxs-lookup"><span data-stu-id="b7516-117">Name</span></span>  | [<span data-ttu-id="b7516-118">**範本類型**</span><span class="sxs-lookup"><span data-stu-id="b7516-118">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="b7516-119">**元件類型**</span><span class="sxs-lookup"><span data-stu-id="b7516-119">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="b7516-120">大小</span><span class="sxs-lookup"><span data-stu-id="b7516-120">Size</span></span> |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="b7516-121">*x*</span><span class="sxs-lookup"><span data-stu-id="b7516-121">*x*</span></span>   | [<span data-ttu-id="b7516-122">**向量**</span><span class="sxs-lookup"><span data-stu-id="b7516-122">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="b7516-123">**浮動**</span><span class="sxs-lookup"><span data-stu-id="b7516-123">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="b7516-124">3</span><span class="sxs-lookup"><span data-stu-id="b7516-124">3</span></span>    |
| <span data-ttu-id="b7516-125">*y*</span><span class="sxs-lookup"><span data-stu-id="b7516-125">*y*</span></span>   | [<span data-ttu-id="b7516-126">**向量**</span><span class="sxs-lookup"><span data-stu-id="b7516-126">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="b7516-127">**浮動**</span><span class="sxs-lookup"><span data-stu-id="b7516-127">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="b7516-128">3</span><span class="sxs-lookup"><span data-stu-id="b7516-128">3</span></span>    |
| <span data-ttu-id="b7516-129">*Ret*</span><span class="sxs-lookup"><span data-stu-id="b7516-129">*ret*</span></span> | [<span data-ttu-id="b7516-130">**向量**</span><span class="sxs-lookup"><span data-stu-id="b7516-130">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="b7516-131">**浮動**</span><span class="sxs-lookup"><span data-stu-id="b7516-131">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="b7516-132">3</span><span class="sxs-lookup"><span data-stu-id="b7516-132">3</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="b7516-133">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="b7516-133">Minimum Shader Model</span></span>

<span data-ttu-id="b7516-134">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="b7516-134">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="b7516-135">著色器模型</span><span class="sxs-lookup"><span data-stu-id="b7516-135">Shader Model</span></span>                                                                       | <span data-ttu-id="b7516-136">支援</span><span class="sxs-lookup"><span data-stu-id="b7516-136">Supported</span></span>             |
|------------------------------------------------------------------------------------|-----------------------|
| <span data-ttu-id="b7516-137">[著色器模型 2 (DIRECTX HLSL) ](dx-graphics-hlsl-sm2.md) 和更高的著色器模型</span><span class="sxs-lookup"><span data-stu-id="b7516-137">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="b7516-138">是</span><span class="sxs-lookup"><span data-stu-id="b7516-138">yes</span></span>                   |
| [<span data-ttu-id="b7516-139">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="b7516-139">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="b7516-140">vs \_ 1 \_ 1 和 ps \_ 1 \_ 4</span><span class="sxs-lookup"><span data-stu-id="b7516-140">vs\_1\_1 and ps\_1\_4</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="b7516-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b7516-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7516-142">**(DirectX HLSL) 內建函式**</span><span class="sxs-lookup"><span data-stu-id="b7516-142">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

