---
title: ftoi (sm4 - asm)
description: 浮點數轉換為帶正負號的整數。
ms.assetid: 580AB4A6-0C1C-409B-B2B9-BA1D37772F46
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c02ce1b506d112a59d3087f59d219557575b8def
ms.sourcegitcommit: 8c658e9872a2173e3dcec94195f9067fbcd85d3d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/17/2020
ms.locfileid: "104316669"
---
# <a name="ftoi-sm4---asm"></a><span data-ttu-id="cf1a2-103">ftoi (sm4 - asm)</span><span class="sxs-lookup"><span data-stu-id="cf1a2-103">ftoi (sm4 - asm)</span></span>

<span data-ttu-id="cf1a2-104">浮點數轉換為帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="cf1a2-104">Floating point to signed integer conversion.</span></span>

| <span data-ttu-id="cf1a2-105">ftoi dest \[ . mask \] ， \[ - \] src0 \[ \_ abs \] \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="cf1a2-105">ftoi dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|-|

| <span data-ttu-id="cf1a2-106">項目</span><span class="sxs-lookup"><span data-stu-id="cf1a2-106">Item</span></span> | <span data-ttu-id="cf1a2-107">描述</span><span class="sxs-lookup"><span data-stu-id="cf1a2-107">Description</span></span> |
|-|-|
| <span data-ttu-id="cf1a2-108"><span id="dest"></span><span id="DEST"></span>*目標*</span><span class="sxs-lookup"><span data-stu-id="cf1a2-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="cf1a2-109">\[在 \] 操作結果的位址中。</span><span class="sxs-lookup"><span data-stu-id="cf1a2-109">\[in\] The address of the result of the operation.</span></span><br/> <span data-ttu-id="cf1a2-110">*目的地*  = [圓形 \_ z](round-z--sm4---asm-.md) (*src0*) </span><span class="sxs-lookup"><span data-stu-id="cf1a2-110">*dest* = [round\_z](round-z--sm4---asm-.md)(*src0*)</span></span><br/> |
| <span data-ttu-id="cf1a2-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="cf1a2-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="cf1a2-112">\[在 \] 要轉換的元件中。</span><span class="sxs-lookup"><span data-stu-id="cf1a2-112">\[in\] The component to convert.</span></span><br/> |

## <a name="remarks"></a><span data-ttu-id="cf1a2-113">備註</span><span class="sxs-lookup"><span data-stu-id="cf1a2-113">Remarks</span></span>

<span data-ttu-id="cf1a2-114">每個元件都會執行轉換。</span><span class="sxs-lookup"><span data-stu-id="cf1a2-114">The conversion is performed per component.</span></span> <span data-ttu-id="cf1a2-115">舍入一律會對零執行，並遵循 C 慣例，從 float 轉換成 int。需要不同四捨五入語義的應用程式可以在轉換成整數之前叫用 **舍入** 指令。</span><span class="sxs-lookup"><span data-stu-id="cf1a2-115">Rounding is always performed towards zero, following the C convention for casts from float to int. Applications that require different rounding semantics can invoke the **round** instructions before casting to integer.</span></span>

<span data-ttu-id="cf1a2-116">輸入會壓制至 2147483648.999 f 的範圍 ... \[2147483647.999 f \] 轉換之前，輸入 NaN 值會產生零結果。</span><span class="sxs-lookup"><span data-stu-id="cf1a2-116">Inputs are clamped to the range \[-2147483648.999f ... 2147483647.999f\] prior to conversion, and input NaN values produce a zero result.</span></span>

<span data-ttu-id="cf1a2-117">選擇性的否定和絕對值修飾詞會在轉換之前套用至來源值。</span><span class="sxs-lookup"><span data-stu-id="cf1a2-117">Optional negate and absolute value modifiers are applied to the source values before conversion.</span></span>

<span data-ttu-id="cf1a2-118">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="cf1a2-118">This instruction applies to the following shader stages:</span></span>

| <span data-ttu-id="cf1a2-119">頂點著色器</span><span class="sxs-lookup"><span data-stu-id="cf1a2-119">Vertex Shader</span></span> | <span data-ttu-id="cf1a2-120">幾何著色器</span><span class="sxs-lookup"><span data-stu-id="cf1a2-120">Geometry Shader</span></span> | <span data-ttu-id="cf1a2-121">像素著色器</span><span class="sxs-lookup"><span data-stu-id="cf1a2-121">Pixel Shader</span></span> |
|-|-|-|
| <span data-ttu-id="cf1a2-122">x</span><span class="sxs-lookup"><span data-stu-id="cf1a2-122">x</span></span> | <span data-ttu-id="cf1a2-123">x</span><span class="sxs-lookup"><span data-stu-id="cf1a2-123">x</span></span> | <span data-ttu-id="cf1a2-124">x</span><span class="sxs-lookup"><span data-stu-id="cf1a2-124">x</span></span> |

## <a name="minimum-shader-model"></a><span data-ttu-id="cf1a2-125">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="cf1a2-125">Minimum Shader Model</span></span>

<span data-ttu-id="cf1a2-126">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="cf1a2-126">This function is supported in the following shader models.</span></span>

| <span data-ttu-id="cf1a2-127">著色器模型</span><span class="sxs-lookup"><span data-stu-id="cf1a2-127">Shader Model</span></span> | <span data-ttu-id="cf1a2-128">支援</span><span class="sxs-lookup"><span data-stu-id="cf1a2-128">Supported</span></span> |
|-|-|
| [<span data-ttu-id="cf1a2-129">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="cf1a2-129">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md) | <span data-ttu-id="cf1a2-130">是</span><span class="sxs-lookup"><span data-stu-id="cf1a2-130">yes</span></span> |
| [<span data-ttu-id="cf1a2-131">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="cf1a2-131">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md) | <span data-ttu-id="cf1a2-132">是</span><span class="sxs-lookup"><span data-stu-id="cf1a2-132">yes</span></span> |
| [<span data-ttu-id="cf1a2-133">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="cf1a2-133">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md) | <span data-ttu-id="cf1a2-134">是</span><span class="sxs-lookup"><span data-stu-id="cf1a2-134">yes</span></span> |
| [<span data-ttu-id="cf1a2-135">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="cf1a2-135">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="cf1a2-136">不可以</span><span class="sxs-lookup"><span data-stu-id="cf1a2-136">no</span></span> |
| [<span data-ttu-id="cf1a2-137">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="cf1a2-137">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="cf1a2-138">不可以</span><span class="sxs-lookup"><span data-stu-id="cf1a2-138">no</span></span> |
| [<span data-ttu-id="cf1a2-139">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="cf1a2-139">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="cf1a2-140">不可以</span><span class="sxs-lookup"><span data-stu-id="cf1a2-140">no</span></span> |

## <a name="related-topics"></a><span data-ttu-id="cf1a2-141">相關主題</span><span class="sxs-lookup"><span data-stu-id="cf1a2-141">Related topics</span></span>

[<span data-ttu-id="cf1a2-142">著色器模型4元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="cf1a2-142">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
