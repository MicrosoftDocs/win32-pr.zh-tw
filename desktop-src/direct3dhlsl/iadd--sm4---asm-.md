---
title: 'iadd (sm4-asm) '
description: 整數加法。
ms.assetid: EF78EA65-DC16-469A-9E45-52844FF4BD93
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b593484aa7c1ef376bb5febf141b144ddef338e0
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104373867"
---
# <a name="iadd-sm4---asm"></a><span data-ttu-id="7b867-103">iadd (sm4-asm) </span><span class="sxs-lookup"><span data-stu-id="7b867-103">iadd (sm4 - asm)</span></span>

<span data-ttu-id="7b867-104">整數加法。</span><span class="sxs-lookup"><span data-stu-id="7b867-104">Integer addition.</span></span>



| <span data-ttu-id="7b867-105">iadd dest \[ . mask \] 、 \[ - \] src0 \[ . swizzle \] 、 \[ - \] src1 \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="7b867-105">iadd dest\[.mask\], \[-\]src0\[.swizzle\], \[-\]src1\[.swizzle\]</span></span> |
|------------------------------------------------------------------|



 



| <span data-ttu-id="7b867-106">項目</span><span class="sxs-lookup"><span data-stu-id="7b867-106">Item</span></span>                                                            | <span data-ttu-id="7b867-107">描述</span><span class="sxs-lookup"><span data-stu-id="7b867-107">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="7b867-108"><span id="dest"></span><span id="DEST"></span>*目標*</span><span class="sxs-lookup"><span data-stu-id="7b867-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="7b867-109">\[在 \] 操作結果的位址中。</span><span class="sxs-lookup"><span data-stu-id="7b867-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="7b867-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="7b867-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="7b867-111">\[在 \] 要加入至 *src1* 的數位中。</span><span class="sxs-lookup"><span data-stu-id="7b867-111">\[in\] The number to be added to *src1*.</span></span><br/>           |
| <span data-ttu-id="7b867-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="7b867-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="7b867-113">\[在 \] 要加入至 *src0* 的數位中。</span><span class="sxs-lookup"><span data-stu-id="7b867-113">\[in\] The number to be added to *src0*.</span></span><br/>           |



 

## <a name="remarks"></a><span data-ttu-id="7b867-114">備註</span><span class="sxs-lookup"><span data-stu-id="7b867-114">Remarks</span></span>

<span data-ttu-id="7b867-115">32位運算元的元件 *src0* 和 *src1*，將正確的32位結果放置在 *dest* 中。</span><span class="sxs-lookup"><span data-stu-id="7b867-115">Component-wise add of 32-bit operands *src0* and *src1*, placing the correct 32-bit result in *dest*.</span></span> <span data-ttu-id="7b867-116">不會對每個元件的32位值執行任何運算或借用，因此此指令對其運算元的正負號性質而言並不敏感。</span><span class="sxs-lookup"><span data-stu-id="7b867-116">No carry or borrow beyond the 32-bit values of each component is performed, so this instruction is not sensitive to the signed-ness of its operands.</span></span>

<span data-ttu-id="7b867-117">在執行作業之前，來源運算元上的選擇性否定修飾詞會採用2的補數。</span><span class="sxs-lookup"><span data-stu-id="7b867-117">Optional negate modifier on source operands takes 2's complement before performing operation.</span></span>

<span data-ttu-id="7b867-118">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="7b867-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="7b867-119">頂點著色器</span><span class="sxs-lookup"><span data-stu-id="7b867-119">Vertex Shader</span></span> | <span data-ttu-id="7b867-120">幾何著色器</span><span class="sxs-lookup"><span data-stu-id="7b867-120">Geometry Shader</span></span> | <span data-ttu-id="7b867-121">像素著色器</span><span class="sxs-lookup"><span data-stu-id="7b867-121">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="7b867-122">x</span><span class="sxs-lookup"><span data-stu-id="7b867-122">x</span></span>             | <span data-ttu-id="7b867-123">x</span><span class="sxs-lookup"><span data-stu-id="7b867-123">x</span></span>               | <span data-ttu-id="7b867-124">x</span><span class="sxs-lookup"><span data-stu-id="7b867-124">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="7b867-125">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="7b867-125">Minimum Shader Model</span></span>

<span data-ttu-id="7b867-126">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="7b867-126">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="7b867-127">著色器模型</span><span class="sxs-lookup"><span data-stu-id="7b867-127">Shader Model</span></span>                                              | <span data-ttu-id="7b867-128">支援</span><span class="sxs-lookup"><span data-stu-id="7b867-128">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="7b867-129">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="7b867-129">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="7b867-130">是</span><span class="sxs-lookup"><span data-stu-id="7b867-130">yes</span></span>       |
| [<span data-ttu-id="7b867-131">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="7b867-131">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="7b867-132">是</span><span class="sxs-lookup"><span data-stu-id="7b867-132">yes</span></span>       |
| [<span data-ttu-id="7b867-133">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="7b867-133">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="7b867-134">是</span><span class="sxs-lookup"><span data-stu-id="7b867-134">yes</span></span>       |
| [<span data-ttu-id="7b867-135">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="7b867-135">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="7b867-136">不可以</span><span class="sxs-lookup"><span data-stu-id="7b867-136">no</span></span>        |
| [<span data-ttu-id="7b867-137">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="7b867-137">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="7b867-138">不可以</span><span class="sxs-lookup"><span data-stu-id="7b867-138">no</span></span>        |
| [<span data-ttu-id="7b867-139">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="7b867-139">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="7b867-140">不可以</span><span class="sxs-lookup"><span data-stu-id="7b867-140">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="7b867-141">相關主題</span><span class="sxs-lookup"><span data-stu-id="7b867-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7b867-142">著色器模型4元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="7b867-142">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





