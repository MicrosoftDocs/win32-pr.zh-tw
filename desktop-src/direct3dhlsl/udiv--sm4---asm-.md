---
title: 'udiv (sm4-asm) '
description: 不帶正負號的整數除。
ms.assetid: 87C81418-0F74-4C67-9D4A-DA952EFD008E
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07a3dd2f4170a3c8fe522af12d412cfae49396da
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104373791"
---
# <a name="udiv-sm4---asm"></a><span data-ttu-id="de963-103">udiv (sm4-asm) </span><span class="sxs-lookup"><span data-stu-id="de963-103">udiv (sm4 - asm)</span></span>

<span data-ttu-id="de963-104">不帶正負號的整數除。</span><span class="sxs-lookup"><span data-stu-id="de963-104">Unsigned integer divide.</span></span>



| <span data-ttu-id="de963-105">udiv destQUOT \[ mask \] 、destREM \[ mask \] 、src0 \[ . swizzle \] 、src1 \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="de963-105">udiv destQUOT\[.mask\], destREM\[.mask\], src0\[.swizzle\], src1\[.swizzle\]</span></span> |
|------------------------------------------------------------------------------|



 



| <span data-ttu-id="de963-106">項目</span><span class="sxs-lookup"><span data-stu-id="de963-106">Item</span></span>                                                                                                   | <span data-ttu-id="de963-107">描述</span><span class="sxs-lookup"><span data-stu-id="de963-107">Description</span></span>                                                |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="de963-108"><span id="destQUOT"></span><span id="destquot"></span><span id="DESTQUOT"></span>*destQUOT*</span><span class="sxs-lookup"><span data-stu-id="de963-108"><span id="destQUOT"></span><span id="destquot"></span><span id="DESTQUOT"></span>*destQUOT*</span></span><br/> | <span data-ttu-id="de963-109">\[在 \] 產生的商位址中。</span><span class="sxs-lookup"><span data-stu-id="de963-109">\[in\] The address of the resulting quotient.</span></span><br/>   |
| <span data-ttu-id="de963-110"><span id="destREM"></span><span id="destrem"></span><span id="DESTREM"></span>*destREM*</span><span class="sxs-lookup"><span data-stu-id="de963-110"><span id="destREM"></span><span id="destrem"></span><span id="DESTREM"></span>*destREM*</span></span><br/>     | <span data-ttu-id="de963-111">\[在 \] 結果餘數的位址中。</span><span class="sxs-lookup"><span data-stu-id="de963-111">\[in\] The address of the resulting remainder.</span></span><br/>  |
| <span data-ttu-id="de963-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="de963-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                        | <span data-ttu-id="de963-113">\[在 \] 要除以 *src1* 的元件中。</span><span class="sxs-lookup"><span data-stu-id="de963-113">\[in\] The components to be divided by *src1*.</span></span><br/>  |
| <span data-ttu-id="de963-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="de963-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/>                                        | <span data-ttu-id="de963-115">\[在 \] [我們元件] 中，以分割 *src0*。</span><span class="sxs-lookup"><span data-stu-id="de963-115">\[in\] The components by whch to divide *src0*.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="de963-116">備註</span><span class="sxs-lookup"><span data-stu-id="de963-116">Remarks</span></span>

<span data-ttu-id="de963-117">此指令會執行由32位運算元 *src1* 所 *src0* 之32位運算元的元件的不帶正負號分隔。</span><span class="sxs-lookup"><span data-stu-id="de963-117">This instruction performs a component-wise unsigned divide of the 32-bit operand *src0* by the 32-bit operand *src1*.</span></span> <span data-ttu-id="de963-118">相除的結果是放置在 *destQUOT* 中的32位商數，而32位餘數放置於 *destREM* 中。</span><span class="sxs-lookup"><span data-stu-id="de963-118">The results of the divides are the 32-bit quotients placed in *destQUOT* and 32-bit remainders placed in *destREM*.</span></span>

<span data-ttu-id="de963-119">「零除」會針對商和餘數傳回0xffffffff。</span><span class="sxs-lookup"><span data-stu-id="de963-119">Divide by zero returns 0xffffffff for both quotient and remainder.</span></span>

<span data-ttu-id="de963-120">如果不需要商或餘數，您可以將 *destQUOT* 或 *DESTREM* 指定為 Null，而不是指定註冊。</span><span class="sxs-lookup"><span data-stu-id="de963-120">You can specifiy either *destQUOT* or *destREM* as NULL instead of specifying a register, if the quotient or remainder are not needed.</span></span>

<span data-ttu-id="de963-121">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="de963-121">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="de963-122">頂點著色器</span><span class="sxs-lookup"><span data-stu-id="de963-122">Vertex Shader</span></span> | <span data-ttu-id="de963-123">幾何著色器</span><span class="sxs-lookup"><span data-stu-id="de963-123">Geometry Shader</span></span> | <span data-ttu-id="de963-124">像素著色器</span><span class="sxs-lookup"><span data-stu-id="de963-124">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="de963-125">x</span><span class="sxs-lookup"><span data-stu-id="de963-125">x</span></span>             | <span data-ttu-id="de963-126">x</span><span class="sxs-lookup"><span data-stu-id="de963-126">x</span></span>               | <span data-ttu-id="de963-127">x</span><span class="sxs-lookup"><span data-stu-id="de963-127">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="de963-128">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="de963-128">Minimum Shader Model</span></span>

<span data-ttu-id="de963-129">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="de963-129">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="de963-130">著色器模型</span><span class="sxs-lookup"><span data-stu-id="de963-130">Shader Model</span></span>                                              | <span data-ttu-id="de963-131">支援</span><span class="sxs-lookup"><span data-stu-id="de963-131">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="de963-132">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="de963-132">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="de963-133">是</span><span class="sxs-lookup"><span data-stu-id="de963-133">yes</span></span>       |
| [<span data-ttu-id="de963-134">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="de963-134">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="de963-135">是</span><span class="sxs-lookup"><span data-stu-id="de963-135">yes</span></span>       |
| [<span data-ttu-id="de963-136">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="de963-136">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="de963-137">是</span><span class="sxs-lookup"><span data-stu-id="de963-137">yes</span></span>       |
| [<span data-ttu-id="de963-138">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="de963-138">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="de963-139">不可以</span><span class="sxs-lookup"><span data-stu-id="de963-139">no</span></span>        |
| [<span data-ttu-id="de963-140">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="de963-140">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="de963-141">不可以</span><span class="sxs-lookup"><span data-stu-id="de963-141">no</span></span>        |
| [<span data-ttu-id="de963-142">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="de963-142">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="de963-143">不可以</span><span class="sxs-lookup"><span data-stu-id="de963-143">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="de963-144">相關主題</span><span class="sxs-lookup"><span data-stu-id="de963-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="de963-145">著色器模型4元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="de963-145">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





