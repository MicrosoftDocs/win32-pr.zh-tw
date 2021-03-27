---
title: '和 (sm4-asm) '
description: 位元 AND。
ms.assetid: 403DA289-E2CF-4736-8882-4131F884F777
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7ec9474322aafda2706502898902d01d0e13143
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "103679163"
---
# <a name="and-sm4---asm"></a><span data-ttu-id="37953-103">和 (sm4-asm) </span><span class="sxs-lookup"><span data-stu-id="37953-103">and (sm4 - asm)</span></span>

<span data-ttu-id="37953-104">位 **and**。</span><span class="sxs-lookup"><span data-stu-id="37953-104">Bitwise **AND**.</span></span>



| <span data-ttu-id="37953-105">和 dest \[ \] 、src0 \[ . swizzle \] 、src1 \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="37953-105">and dest\[.mask\], src0\[.swizzle\], src1\[.swizzle\]</span></span> |
|-------------------------------------------------------|



 



| <span data-ttu-id="37953-106">項目</span><span class="sxs-lookup"><span data-stu-id="37953-106">Item</span></span>                                                            | <span data-ttu-id="37953-107">描述</span><span class="sxs-lookup"><span data-stu-id="37953-107">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="37953-108"><span id="dest"></span><span id="DEST"></span>*目標*</span><span class="sxs-lookup"><span data-stu-id="37953-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="37953-109">\[在 \] 操作結果的位址中。</span><span class="sxs-lookup"><span data-stu-id="37953-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="37953-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="37953-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="37953-111">\[在與 \] *src1* 的32位值中。</span><span class="sxs-lookup"><span data-stu-id="37953-111">\[in\] The 32-bit value to **AND** with *src1*.</span></span><br/>    |
| <span data-ttu-id="37953-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="37953-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="37953-113">\[在與 \] *src0* 的32位值中。</span><span class="sxs-lookup"><span data-stu-id="37953-113">\[in\] The 32-bit value to **AND** with *src0*.</span></span><br/>    |



 

## <a name="remarks"></a><span data-ttu-id="37953-114">備註</span><span class="sxs-lookup"><span data-stu-id="37953-114">Remarks</span></span>

<span data-ttu-id="37953-115">*Src0* 和 *src1* 的每一對32位值的元件的邏輯 **AND** 。</span><span class="sxs-lookup"><span data-stu-id="37953-115">Component-wise logical **AND** of each pair of 32-bit values from *src0* and *src1*.</span></span> <span data-ttu-id="37953-116">32位的結果會放在 *dest* 中。</span><span class="sxs-lookup"><span data-stu-id="37953-116">The 32-bit results are placed in *dest*.</span></span>

<span data-ttu-id="37953-117">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="37953-117">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="37953-118">頂點著色器</span><span class="sxs-lookup"><span data-stu-id="37953-118">Vertex Shader</span></span> | <span data-ttu-id="37953-119">幾何著色器</span><span class="sxs-lookup"><span data-stu-id="37953-119">Geometry Shader</span></span> | <span data-ttu-id="37953-120">像素著色器</span><span class="sxs-lookup"><span data-stu-id="37953-120">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="37953-121">x</span><span class="sxs-lookup"><span data-stu-id="37953-121">x</span></span>             | <span data-ttu-id="37953-122">x</span><span class="sxs-lookup"><span data-stu-id="37953-122">x</span></span>               | <span data-ttu-id="37953-123">x</span><span class="sxs-lookup"><span data-stu-id="37953-123">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="37953-124">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="37953-124">Minimum Shader Model</span></span>

<span data-ttu-id="37953-125">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="37953-125">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="37953-126">著色器模型</span><span class="sxs-lookup"><span data-stu-id="37953-126">Shader Model</span></span>                                              | <span data-ttu-id="37953-127">支援</span><span class="sxs-lookup"><span data-stu-id="37953-127">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="37953-128">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="37953-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="37953-129">是</span><span class="sxs-lookup"><span data-stu-id="37953-129">yes</span></span>       |
| [<span data-ttu-id="37953-130">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="37953-130">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="37953-131">是</span><span class="sxs-lookup"><span data-stu-id="37953-131">yes</span></span>       |
| [<span data-ttu-id="37953-132">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="37953-132">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="37953-133">是</span><span class="sxs-lookup"><span data-stu-id="37953-133">yes</span></span>       |
| [<span data-ttu-id="37953-134">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="37953-134">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="37953-135">不可以</span><span class="sxs-lookup"><span data-stu-id="37953-135">no</span></span>        |
| [<span data-ttu-id="37953-136">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="37953-136">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="37953-137">不可以</span><span class="sxs-lookup"><span data-stu-id="37953-137">no</span></span>        |
| [<span data-ttu-id="37953-138">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="37953-138">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="37953-139">不可以</span><span class="sxs-lookup"><span data-stu-id="37953-139">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="37953-140">相關主題</span><span class="sxs-lookup"><span data-stu-id="37953-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="37953-141">著色器模型4元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="37953-141">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





