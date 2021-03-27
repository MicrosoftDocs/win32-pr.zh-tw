---
title: dot
description: 傳回兩個向量的內積。
ms.assetid: ad24c06c-0b40-4dc5-a2b9-1d5438635ed8
keywords:
- 點 HLSL
topic_type:
- apiref
api_name:
- dot
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d6d05abf0d67628d1d77b362b028107e07b83457
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933495"
---
# <a name="dot"></a><span data-ttu-id="0ddc8-104">dot</span><span class="sxs-lookup"><span data-stu-id="0ddc8-104">dot</span></span>

<span data-ttu-id="0ddc8-105">傳回兩個向量的內積。</span><span class="sxs-lookup"><span data-stu-id="0ddc8-105">Returns the dot product of two vectors.</span></span>



| <span data-ttu-id="0ddc8-106">*ret* 點 (*x*， *y*) </span><span class="sxs-lookup"><span data-stu-id="0ddc8-106">*ret* dot(*x*, *y*)</span></span> |
|---------------------|



 

## <a name="parameters"></a><span data-ttu-id="0ddc8-107">參數</span><span class="sxs-lookup"><span data-stu-id="0ddc8-107">Parameters</span></span>



| <span data-ttu-id="0ddc8-108">項目</span><span class="sxs-lookup"><span data-stu-id="0ddc8-108">Item</span></span>                                                   | <span data-ttu-id="0ddc8-109">描述</span><span class="sxs-lookup"><span data-stu-id="0ddc8-109">Description</span></span>                          |
|--------------------------------------------------------|--------------------------------------|
| <span data-ttu-id="0ddc8-110"><span id="x"></span><span id="X"></span>*X*</span><span class="sxs-lookup"><span data-stu-id="0ddc8-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="0ddc8-111">\[在 \] 第一個向量中。</span><span class="sxs-lookup"><span data-stu-id="0ddc8-111">\[in\] The first vector.</span></span><br/>  |
| <span data-ttu-id="0ddc8-112"><span id="y"></span><span id="Y"></span>*Y*</span><span class="sxs-lookup"><span data-stu-id="0ddc8-112"><span id="y"></span><span id="Y"></span>*y*</span></span><br/> | <span data-ttu-id="0ddc8-113">\[在 \] 第二個向量中。</span><span class="sxs-lookup"><span data-stu-id="0ddc8-113">\[in\] The second vector.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="0ddc8-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="0ddc8-114">Return Value</span></span>

<span data-ttu-id="0ddc8-115">*X* 參數和 *y* 參數的點乘積。</span><span class="sxs-lookup"><span data-stu-id="0ddc8-115">The dot product of the *x* parameter and the *y* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="0ddc8-116">類型描述</span><span class="sxs-lookup"><span data-stu-id="0ddc8-116">Type Description</span></span>



| <span data-ttu-id="0ddc8-117">Name</span><span class="sxs-lookup"><span data-stu-id="0ddc8-117">Name</span></span>  | [<span data-ttu-id="0ddc8-118">**範本類型**</span><span class="sxs-lookup"><span data-stu-id="0ddc8-118">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="0ddc8-119">**元件類型**</span><span class="sxs-lookup"><span data-stu-id="0ddc8-119">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                 | <span data-ttu-id="0ddc8-120">大小</span><span class="sxs-lookup"><span data-stu-id="0ddc8-120">Size</span></span>                            |
|-------|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|---------------------------------|
| <span data-ttu-id="0ddc8-121">*x*</span><span class="sxs-lookup"><span data-stu-id="0ddc8-121">*x*</span></span>   | [<span data-ttu-id="0ddc8-122">**向量**</span><span class="sxs-lookup"><span data-stu-id="0ddc8-122">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="0ddc8-123">[**float**](/windows/desktop/WinProg/windows-data-types)、 [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="0ddc8-123">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="0ddc8-124">任意</span><span class="sxs-lookup"><span data-stu-id="0ddc8-124">any</span></span>                             |
| <span data-ttu-id="0ddc8-125">*y*</span><span class="sxs-lookup"><span data-stu-id="0ddc8-125">*y*</span></span>   | [<span data-ttu-id="0ddc8-126">**向量**</span><span class="sxs-lookup"><span data-stu-id="0ddc8-126">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="0ddc8-127">[**float**](/windows/desktop/WinProg/windows-data-types)、 [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="0ddc8-127">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="0ddc8-128"> (s 的相同維度) 為輸入 *x*</span><span class="sxs-lookup"><span data-stu-id="0ddc8-128">same dimensions(s) as input *x*</span></span> |
| <span data-ttu-id="0ddc8-129">*Ret*</span><span class="sxs-lookup"><span data-stu-id="0ddc8-129">*ret*</span></span> | [<span data-ttu-id="0ddc8-130">**純量 (scalar)**</span><span class="sxs-lookup"><span data-stu-id="0ddc8-130">**scalar**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="0ddc8-131">[**float**](/windows/desktop/WinProg/windows-data-types)、 [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="0ddc8-131">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="0ddc8-132">1</span><span class="sxs-lookup"><span data-stu-id="0ddc8-132">1</span></span>                               |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="0ddc8-133">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="0ddc8-133">Minimum Shader Model</span></span>

<span data-ttu-id="0ddc8-134">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="0ddc8-134">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="0ddc8-135">著色器模型</span><span class="sxs-lookup"><span data-stu-id="0ddc8-135">Shader Model</span></span>                                                                       | <span data-ttu-id="0ddc8-136">支援</span><span class="sxs-lookup"><span data-stu-id="0ddc8-136">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="0ddc8-137">[著色器模型 2 (DIRECTX HLSL) ](dx-graphics-hlsl-sm2.md) 和更高的著色器模型</span><span class="sxs-lookup"><span data-stu-id="0ddc8-137">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="0ddc8-138">是</span><span class="sxs-lookup"><span data-stu-id="0ddc8-138">yes</span></span>       |
| [<span data-ttu-id="0ddc8-139">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="0ddc8-139">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="0ddc8-140">是</span><span class="sxs-lookup"><span data-stu-id="0ddc8-140">yes</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="0ddc8-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0ddc8-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ddc8-142">**(DirectX HLSL) 內建函式**</span><span class="sxs-lookup"><span data-stu-id="0ddc8-142">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

