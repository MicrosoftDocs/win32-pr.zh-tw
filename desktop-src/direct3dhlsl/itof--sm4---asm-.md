---
title: 'itof (sm4-asm) '
description: 帶正負號的整數轉換浮點數。
ms.assetid: 60652168-25FA-4084-8CC1-73F12984ECED
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f9d262f65801cd2caa0e6432b335ce32fff0d4e
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "103841668"
---
# <a name="itof-sm4---asm"></a><span data-ttu-id="efa63-103">itof (sm4-asm) </span><span class="sxs-lookup"><span data-stu-id="efa63-103">itof (sm4 - asm)</span></span>

<span data-ttu-id="efa63-104">帶正負號的整數轉換浮點數。</span><span class="sxs-lookup"><span data-stu-id="efa63-104">Signed integer to floating point conversion.</span></span>



| <span data-ttu-id="efa63-105">itof dest \[ . mask \] ， \[ - \] src0 \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="efa63-105">itof dest\[.mask\], \[-\]src0\[.swizzle\]</span></span> |
|-------------------------------------------|



 



| <span data-ttu-id="efa63-106">項目</span><span class="sxs-lookup"><span data-stu-id="efa63-106">Item</span></span>                                                            | <span data-ttu-id="efa63-107">描述</span><span class="sxs-lookup"><span data-stu-id="efa63-107">Description</span></span>                                             |
|-----------------------------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="efa63-108"><span id="dest"></span><span id="DEST"></span>*目標*</span><span class="sxs-lookup"><span data-stu-id="efa63-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="efa63-109">\[中的 \] 包含運算的結果。</span><span class="sxs-lookup"><span data-stu-id="efa63-109">\[in\] Contains the result of the operation.</span></span><br/> |
| <span data-ttu-id="efa63-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="efa63-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="efa63-111">\[in \] 包含要轉換的值。</span><span class="sxs-lookup"><span data-stu-id="efa63-111">\[in\] Contains the value to convert.</span></span><br/>        |



 

## <a name="remarks"></a><span data-ttu-id="efa63-112">備註</span><span class="sxs-lookup"><span data-stu-id="efa63-112">Remarks</span></span>

<span data-ttu-id="efa63-113">此帶正負號的整數到浮點數轉換指令會假設 *src0* 包含帶正負號的32位整數4元組。</span><span class="sxs-lookup"><span data-stu-id="efa63-113">This signed integer-to-float conversion instruction assumes that *src0* contains a signed 32-bit integer 4-tuple.</span></span> <span data-ttu-id="efa63-114">在執行指令之後， *dest* 將包含浮點數4元組。</span><span class="sxs-lookup"><span data-stu-id="efa63-114">After the instruction executes, *dest* will contain a floating-point 4-tuple.</span></span>

<span data-ttu-id="efa63-115">每個元件都會執行轉換。</span><span class="sxs-lookup"><span data-stu-id="efa63-115">The conversion is performed per-component.</span></span>

<span data-ttu-id="efa63-116">當整數輸入值的大小太大而無法以浮點數格式表示時，強烈建議您四捨五入到最接近的偶數模式，但並非必要。</span><span class="sxs-lookup"><span data-stu-id="efa63-116">When an integer input value is too large in magnitude to be represented exactly in the floating point format, rounding to nearest even mode is strongly recommended but not required.</span></span>

<span data-ttu-id="efa63-117">在執行算數運算之前，來源運算元的選擇性否定修飾詞會採用2的補數。</span><span class="sxs-lookup"><span data-stu-id="efa63-117">The optional negate modifier on source operand takes 2's complement before performing arithmetic operation.</span></span>

<span data-ttu-id="efa63-118">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="efa63-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="efa63-119">頂點著色器</span><span class="sxs-lookup"><span data-stu-id="efa63-119">Vertex Shader</span></span> | <span data-ttu-id="efa63-120">幾何著色器</span><span class="sxs-lookup"><span data-stu-id="efa63-120">Geometry Shader</span></span> | <span data-ttu-id="efa63-121">像素著色器</span><span class="sxs-lookup"><span data-stu-id="efa63-121">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="efa63-122">x</span><span class="sxs-lookup"><span data-stu-id="efa63-122">x</span></span>             | <span data-ttu-id="efa63-123">x</span><span class="sxs-lookup"><span data-stu-id="efa63-123">x</span></span>               | <span data-ttu-id="efa63-124">x</span><span class="sxs-lookup"><span data-stu-id="efa63-124">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="efa63-125">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="efa63-125">Minimum Shader Model</span></span>

<span data-ttu-id="efa63-126">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="efa63-126">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="efa63-127">著色器模型</span><span class="sxs-lookup"><span data-stu-id="efa63-127">Shader Model</span></span>                                              | <span data-ttu-id="efa63-128">支援</span><span class="sxs-lookup"><span data-stu-id="efa63-128">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="efa63-129">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="efa63-129">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="efa63-130">是</span><span class="sxs-lookup"><span data-stu-id="efa63-130">yes</span></span>       |
| [<span data-ttu-id="efa63-131">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="efa63-131">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="efa63-132">是</span><span class="sxs-lookup"><span data-stu-id="efa63-132">yes</span></span>       |
| [<span data-ttu-id="efa63-133">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="efa63-133">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="efa63-134">是</span><span class="sxs-lookup"><span data-stu-id="efa63-134">yes</span></span>       |
| [<span data-ttu-id="efa63-135">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="efa63-135">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="efa63-136">不可以</span><span class="sxs-lookup"><span data-stu-id="efa63-136">no</span></span>        |
| [<span data-ttu-id="efa63-137">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="efa63-137">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="efa63-138">不可以</span><span class="sxs-lookup"><span data-stu-id="efa63-138">no</span></span>        |
| [<span data-ttu-id="efa63-139">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="efa63-139">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="efa63-140">不可以</span><span class="sxs-lookup"><span data-stu-id="efa63-140">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="efa63-141">相關主題</span><span class="sxs-lookup"><span data-stu-id="efa63-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="efa63-142">著色器模型4元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="efa63-142">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





