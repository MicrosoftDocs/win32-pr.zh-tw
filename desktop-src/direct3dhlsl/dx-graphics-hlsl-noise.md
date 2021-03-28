---
title: 雜訊
description: 使用 Perlin 雜訊演算法產生隨機值。
ms.assetid: 0188a7f3-9955-4e1c-9370-ef1d8aff3765
keywords:
- 雜訊 HLSL
topic_type:
- apiref
api_name:
- noise
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6a4dc01eaeb8276527d5d78b07a250d2a6fb1ab9
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "104383326"
---
# <a name="noise"></a><span data-ttu-id="e3926-104">雜訊</span><span class="sxs-lookup"><span data-stu-id="e3926-104">noise</span></span>

<span data-ttu-id="e3926-105">使用 Perlin 雜訊演算法產生隨機值。</span><span class="sxs-lookup"><span data-stu-id="e3926-105">Generates a random value using the Perlin-noise algorithm.</span></span>




| <span data-ttu-id="e3926-106">*ret* 雜訊 (*x*) </span><span class="sxs-lookup"><span data-stu-id="e3926-106">*ret* noise(*x*)</span></span> |
|------------------|



 

## <a name="parameters"></a><span data-ttu-id="e3926-107">參數</span><span class="sxs-lookup"><span data-stu-id="e3926-107">Parameters</span></span>



| <span data-ttu-id="e3926-108">項目</span><span class="sxs-lookup"><span data-stu-id="e3926-108">Item</span></span>                                                   | <span data-ttu-id="e3926-109">描述</span><span class="sxs-lookup"><span data-stu-id="e3926-109">Description</span></span>                                                                    |
|--------------------------------------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="e3926-110"><span id="x"></span><span id="X"></span>*X*</span><span class="sxs-lookup"><span data-stu-id="e3926-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="e3926-111">\[在 \] 要產生 Perlin 雜訊的浮點向量中。</span><span class="sxs-lookup"><span data-stu-id="e3926-111">\[in\] A floating-point vector from which to generate Perlin noise.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="e3926-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="e3926-112">Return Value</span></span>

<span data-ttu-id="e3926-113">介於-1 和1之間範圍內的 Perlin 雜訊值。</span><span class="sxs-lookup"><span data-stu-id="e3926-113">The Perlin noise value within a range between -1 and 1.</span></span>

## <a name="remarks"></a><span data-ttu-id="e3926-114">備註</span><span class="sxs-lookup"><span data-stu-id="e3926-114">Remarks</span></span>

<span data-ttu-id="e3926-115">Perlin 雜訊值會從某個點順暢地變更為另一個點，以建立自然查看、隨機產生的值。</span><span class="sxs-lookup"><span data-stu-id="e3926-115">Perlin noise values change smoothly from one point to another over a space, creating natural looking, randomly generated values.</span></span> <span data-ttu-id="e3926-116">您可以使用 Perlin 雜訊來產生像是冒煙和火災等效果的程式紋理。</span><span class="sxs-lookup"><span data-stu-id="e3926-116">You can use Perlin noise to generate procedural textures for effects like smoke and fire.</span></span>

## <a name="type-description"></a><span data-ttu-id="e3926-117">類型描述</span><span class="sxs-lookup"><span data-stu-id="e3926-117">Type Description</span></span>



| <span data-ttu-id="e3926-118">名稱</span><span class="sxs-lookup"><span data-stu-id="e3926-118">Name</span></span>  | [<span data-ttu-id="e3926-119">**範本類型**</span><span class="sxs-lookup"><span data-stu-id="e3926-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="e3926-120">**元件類型**</span><span class="sxs-lookup"><span data-stu-id="e3926-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="e3926-121">大小</span><span class="sxs-lookup"><span data-stu-id="e3926-121">Size</span></span> |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="e3926-122">*x*</span><span class="sxs-lookup"><span data-stu-id="e3926-122">*x*</span></span>   | [<span data-ttu-id="e3926-123">**向量**</span><span class="sxs-lookup"><span data-stu-id="e3926-123">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="e3926-124">**浮動**</span><span class="sxs-lookup"><span data-stu-id="e3926-124">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="e3926-125">任意</span><span class="sxs-lookup"><span data-stu-id="e3926-125">any</span></span>  |
| <span data-ttu-id="e3926-126">*Ret*</span><span class="sxs-lookup"><span data-stu-id="e3926-126">*ret*</span></span> | [<span data-ttu-id="e3926-127">**純量 (scalar)**</span><span class="sxs-lookup"><span data-stu-id="e3926-127">**scalar**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="e3926-128">**FLOAT**</span><span class="sxs-lookup"><span data-stu-id="e3926-128">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="e3926-129">1</span><span class="sxs-lookup"><span data-stu-id="e3926-129">1</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="e3926-130">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="e3926-130">Minimum Shader Model</span></span>

<span data-ttu-id="e3926-131">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="e3926-131">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="e3926-132">著色器模型</span><span class="sxs-lookup"><span data-stu-id="e3926-132">Shader Model</span></span>                                                                       | <span data-ttu-id="e3926-133">支援</span><span class="sxs-lookup"><span data-stu-id="e3926-133">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="e3926-134">[著色器模型 2 (DIRECTX HLSL) ](dx-graphics-hlsl-sm2.md) 和更高的著色器模型</span><span class="sxs-lookup"><span data-stu-id="e3926-134">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="e3926-135">不可以</span><span class="sxs-lookup"><span data-stu-id="e3926-135">no</span></span>                  |
| [<span data-ttu-id="e3926-136">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="e3926-136">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="e3926-137">是 (tx \_ 1 \_ 0 僅) </span><span class="sxs-lookup"><span data-stu-id="e3926-137">yes (tx\_1\_0 only)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="e3926-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e3926-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3926-139">**(DirectX HLSL) 內建函式**</span><span class="sxs-lookup"><span data-stu-id="e3926-139">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

