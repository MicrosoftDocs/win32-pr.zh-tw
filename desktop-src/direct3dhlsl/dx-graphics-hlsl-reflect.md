---
title: 反映
description: 使用事件光線和曲面法線傳回反映向量。
ms.assetid: e321b399-f382-4585-83a6-a7da1f7b2327
keywords:
- 反映 HLSL
topic_type:
- apiref
api_name:
- reflect
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 46c981f636a797ecc4e0dd341ce44ed886c202cb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103683014"
---
# <a name="reflect"></a><span data-ttu-id="9683f-104">反映</span><span class="sxs-lookup"><span data-stu-id="9683f-104">reflect</span></span>

<span data-ttu-id="9683f-105">使用事件光線和曲面法線傳回反映向量。</span><span class="sxs-lookup"><span data-stu-id="9683f-105">Returns a reflection vector using an incident ray and a surface normal.</span></span>



| <span data-ttu-id="9683f-106">*ret* 反映 (*i*， *n*) </span><span class="sxs-lookup"><span data-stu-id="9683f-106">*ret* reflect(*i*, *n*)</span></span> |
|-------------------------|



 

## <a name="parameters"></a><span data-ttu-id="9683f-107">參數</span><span class="sxs-lookup"><span data-stu-id="9683f-107">Parameters</span></span>



| <span data-ttu-id="9683f-108">項目</span><span class="sxs-lookup"><span data-stu-id="9683f-108">Item</span></span>                                                   | <span data-ttu-id="9683f-109">描述</span><span class="sxs-lookup"><span data-stu-id="9683f-109">Description</span></span>                                          |
|--------------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9683f-110"><span id="i"></span><span id="I"></span>*我*</span><span class="sxs-lookup"><span data-stu-id="9683f-110"><span id="i"></span><span id="I"></span>*i*</span></span><br/> | <span data-ttu-id="9683f-111">\[在 \] 浮點事件向量中。</span><span class="sxs-lookup"><span data-stu-id="9683f-111">\[in\] A floating-point, incident vector.</span></span><br/> |
| <span data-ttu-id="9683f-112"><span id="n"></span><span id="N"></span>*n-1*</span><span class="sxs-lookup"><span data-stu-id="9683f-112"><span id="n"></span><span id="N"></span>*n*</span></span><br/> | <span data-ttu-id="9683f-113">\[在 \] 浮點的一般向量中。</span><span class="sxs-lookup"><span data-stu-id="9683f-113">\[in\] A floating-point, normal vector.</span></span><br/>   |



 

## <a name="return-value"></a><span data-ttu-id="9683f-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="9683f-114">Return Value</span></span>

<span data-ttu-id="9683f-115">浮點數、反映向量。</span><span class="sxs-lookup"><span data-stu-id="9683f-115">A floating-point, reflection vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="9683f-116">備註</span><span class="sxs-lookup"><span data-stu-id="9683f-116">Remarks</span></span>

<span data-ttu-id="9683f-117">此函數會使用下列公式來計算反映向量： v = i-2 \* n \* 點 (i n) 。</span><span class="sxs-lookup"><span data-stu-id="9683f-117">This function calculates the reflection vector using the following formula: v = i - 2 \* n \* dot(i n) .</span></span>

## <a name="type-description"></a><span data-ttu-id="9683f-118">類型描述</span><span class="sxs-lookup"><span data-stu-id="9683f-118">Type Description</span></span>



| <span data-ttu-id="9683f-119">Name</span><span class="sxs-lookup"><span data-stu-id="9683f-119">Name</span></span>  | [<span data-ttu-id="9683f-120">**範本類型**</span><span class="sxs-lookup"><span data-stu-id="9683f-120">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="9683f-121">**元件類型**</span><span class="sxs-lookup"><span data-stu-id="9683f-121">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="9683f-122">大小</span><span class="sxs-lookup"><span data-stu-id="9683f-122">Size</span></span>                           |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="9683f-123">*i*</span><span class="sxs-lookup"><span data-stu-id="9683f-123">*i*</span></span>   | [<span data-ttu-id="9683f-124">**向量**</span><span class="sxs-lookup"><span data-stu-id="9683f-124">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="9683f-125">**浮動**</span><span class="sxs-lookup"><span data-stu-id="9683f-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="9683f-126">任意</span><span class="sxs-lookup"><span data-stu-id="9683f-126">any</span></span>                            |
| <span data-ttu-id="9683f-127">*n*</span><span class="sxs-lookup"><span data-stu-id="9683f-127">*n*</span></span>   | [<span data-ttu-id="9683f-128">**向量**</span><span class="sxs-lookup"><span data-stu-id="9683f-128">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="9683f-129">**浮動**</span><span class="sxs-lookup"><span data-stu-id="9683f-129">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="9683f-130">相同維度 (s) 為輸入 *i*</span><span class="sxs-lookup"><span data-stu-id="9683f-130">same dimension(s) as input *i*</span></span> |
| <span data-ttu-id="9683f-131">*Ret*</span><span class="sxs-lookup"><span data-stu-id="9683f-131">*ret*</span></span> | [<span data-ttu-id="9683f-132">**向量**</span><span class="sxs-lookup"><span data-stu-id="9683f-132">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="9683f-133">**浮動**</span><span class="sxs-lookup"><span data-stu-id="9683f-133">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="9683f-134">相同維度 (s) 為輸入 *i*</span><span class="sxs-lookup"><span data-stu-id="9683f-134">same dimension(s) as input *i*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="9683f-135">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="9683f-135">Minimum Shader Model</span></span>

<span data-ttu-id="9683f-136">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="9683f-136">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="9683f-137">著色器模型</span><span class="sxs-lookup"><span data-stu-id="9683f-137">Shader Model</span></span>                                                                       | <span data-ttu-id="9683f-138">支援</span><span class="sxs-lookup"><span data-stu-id="9683f-138">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="9683f-139">[著色器模型 1 (DIRECTX HLSL) ](dx-graphics-hlsl-sm1.md) 和更高的著色器模型</span><span class="sxs-lookup"><span data-stu-id="9683f-139">[Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) and higher shader models</span></span> | <span data-ttu-id="9683f-140">是</span><span class="sxs-lookup"><span data-stu-id="9683f-140">yes</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="9683f-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9683f-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9683f-142">**(DirectX HLSL) 內建函式**</span><span class="sxs-lookup"><span data-stu-id="9683f-142">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

