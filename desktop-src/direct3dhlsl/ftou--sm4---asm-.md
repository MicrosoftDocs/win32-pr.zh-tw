---
title: 'ftou (sm4-asm) '
description: 浮點數轉換為不帶正負號的整數。
ms.assetid: 0E3E090B-72C0-4CED-AFA5-2DDCF67D7263
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4a5e65e4bb9d4e71e4a2000f00861cf63e7c181
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104313646"
---
# <a name="ftou-sm4---asm"></a><span data-ttu-id="b448f-103">ftou (sm4-asm) </span><span class="sxs-lookup"><span data-stu-id="b448f-103">ftou (sm4 - asm)</span></span>

<span data-ttu-id="b448f-104">浮點數轉換為不帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="b448f-104">Floating point to unsigned integer conversion.</span></span>



| <span data-ttu-id="b448f-105">ftou dest \[ . mask \] ， \[ - \] src0 \[ \_ abs \] \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="b448f-105">ftou dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|----------------------------------------------------|



 



| <span data-ttu-id="b448f-106">ftoi dest \[ . mask \] ， \[ - \] src0 \[ \_ abs \] \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="b448f-106">ftoi dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|----------------------------------------------------|



 



| <span data-ttu-id="b448f-107">項目</span><span class="sxs-lookup"><span data-stu-id="b448f-107">Item</span></span>                                                            | <span data-ttu-id="b448f-108">描述</span><span class="sxs-lookup"><span data-stu-id="b448f-108">Description</span></span>                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="b448f-109"><span id="dest"></span><span id="DEST"></span>*目標*</span><span class="sxs-lookup"><span data-stu-id="b448f-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="b448f-110">\[在 \] 操作結果的位址中。</span><span class="sxs-lookup"><span data-stu-id="b448f-110">\[in\] The address of the result of the operation.</span></span> <br/> |
| <span data-ttu-id="b448f-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="b448f-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="b448f-112">\[以 \] 轉換的值。</span><span class="sxs-lookup"><span data-stu-id="b448f-112">\[in\] The value to convert.</span></span><br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="b448f-113">備註</span><span class="sxs-lookup"><span data-stu-id="b448f-113">Remarks</span></span>

<span data-ttu-id="b448f-114">每個元件都會執行轉換。</span><span class="sxs-lookup"><span data-stu-id="b448f-114">The conversion is performed per-component.</span></span> <span data-ttu-id="b448f-115">舍入一律會對零執行，並遵循 C 慣例，從 float 轉換成 int。</span><span class="sxs-lookup"><span data-stu-id="b448f-115">Rounding is always performed towards zero, following the C convention for casts from float to int.</span></span>

<span data-ttu-id="b448f-116">需要不同四捨五入語義的應用程式可以在轉換成整數之前叫用 **舍入** 指令。</span><span class="sxs-lookup"><span data-stu-id="b448f-116">Applications that require different rounding semantics can invoke the **round** instructions before casting to integer.</span></span>

<span data-ttu-id="b448f-117">輸入會壓制至範圍 \[ 0.0 f .。。4294967295.999 f \] 轉換之前，輸入 NaN 值會產生零結果。</span><span class="sxs-lookup"><span data-stu-id="b448f-117">Inputs are clamped to the range \[0.0f ... 4294967295.999f\] prior to conversion, and input NaN values produce a zero result.</span></span>

<span data-ttu-id="b448f-118">選擇性的否定和絕對值修飾詞會在轉換之前套用至來源值。</span><span class="sxs-lookup"><span data-stu-id="b448f-118">Optional negate and absolute value modifiers are applied to the source values before conversion.</span></span>

<span data-ttu-id="b448f-119">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="b448f-119">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="b448f-120">頂點著色器</span><span class="sxs-lookup"><span data-stu-id="b448f-120">Vertex Shader</span></span> | <span data-ttu-id="b448f-121">幾何著色器</span><span class="sxs-lookup"><span data-stu-id="b448f-121">Geometry Shader</span></span> | <span data-ttu-id="b448f-122">像素著色器</span><span class="sxs-lookup"><span data-stu-id="b448f-122">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="b448f-123">x</span><span class="sxs-lookup"><span data-stu-id="b448f-123">x</span></span>             | <span data-ttu-id="b448f-124">x</span><span class="sxs-lookup"><span data-stu-id="b448f-124">x</span></span>               | <span data-ttu-id="b448f-125">x</span><span class="sxs-lookup"><span data-stu-id="b448f-125">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="b448f-126">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="b448f-126">Minimum Shader Model</span></span>

<span data-ttu-id="b448f-127">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="b448f-127">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="b448f-128">著色器模型</span><span class="sxs-lookup"><span data-stu-id="b448f-128">Shader Model</span></span>                                              | <span data-ttu-id="b448f-129">支援</span><span class="sxs-lookup"><span data-stu-id="b448f-129">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="b448f-130">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="b448f-130">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="b448f-131">是</span><span class="sxs-lookup"><span data-stu-id="b448f-131">yes</span></span>       |
| [<span data-ttu-id="b448f-132">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="b448f-132">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="b448f-133">是</span><span class="sxs-lookup"><span data-stu-id="b448f-133">yes</span></span>       |
| [<span data-ttu-id="b448f-134">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="b448f-134">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="b448f-135">是</span><span class="sxs-lookup"><span data-stu-id="b448f-135">yes</span></span>       |
| [<span data-ttu-id="b448f-136">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="b448f-136">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="b448f-137">不可以</span><span class="sxs-lookup"><span data-stu-id="b448f-137">no</span></span>        |
| [<span data-ttu-id="b448f-138">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="b448f-138">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="b448f-139">不可以</span><span class="sxs-lookup"><span data-stu-id="b448f-139">no</span></span>        |
| [<span data-ttu-id="b448f-140">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="b448f-140">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="b448f-141">不可以</span><span class="sxs-lookup"><span data-stu-id="b448f-141">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="b448f-142">相關主題</span><span class="sxs-lookup"><span data-stu-id="b448f-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b448f-143">著色器模型4元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="b448f-143">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





