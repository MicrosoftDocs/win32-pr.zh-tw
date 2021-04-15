---
title: 'ishl (sm4-asm) '
description: '左移。 |ishl (sm4-asm) '
ms.assetid: FA0213B8-8A76-4916-8B2F-0983C404A838
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e14225f8c8b0e46cf0ba6eda61f96e4563a904e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104992014"
---
# <a name="ishl-sm4---asm"></a><span data-ttu-id="13f91-104">ishl (sm4-asm) </span><span class="sxs-lookup"><span data-stu-id="13f91-104">ishl (sm4 - asm)</span></span>

<span data-ttu-id="13f91-105">左移。</span><span class="sxs-lookup"><span data-stu-id="13f91-105">Shift left.</span></span>



| <span data-ttu-id="13f91-106">目的地 \[ . mask \] 、src0 \[ . swizzle \] 、src1. select \_ component</span><span class="sxs-lookup"><span data-stu-id="13f91-106">dest\[.mask\], src0\[.swizzle\], src1.select\_component</span></span> |
|---------------------------------------------------------|



 



| <span data-ttu-id="13f91-107">項目</span><span class="sxs-lookup"><span data-stu-id="13f91-107">Item</span></span>                                                            | <span data-ttu-id="13f91-108">描述</span><span class="sxs-lookup"><span data-stu-id="13f91-108">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="13f91-109"><span id="dest"></span><span id="DEST"></span>*目標*</span><span class="sxs-lookup"><span data-stu-id="13f91-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="13f91-110">\[在 \] 操作結果的位址中。</span><span class="sxs-lookup"><span data-stu-id="13f91-110">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="13f91-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="13f91-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="13f91-112">\[in \] 包含要移位的值。</span><span class="sxs-lookup"><span data-stu-id="13f91-112">\[in\] Contains the values to be shifted.</span></span><br/>          |
| <span data-ttu-id="13f91-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="13f91-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="13f91-114">\[in \] 包含移位量。</span><span class="sxs-lookup"><span data-stu-id="13f91-114">\[in\] Contains the shift amount.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="13f91-115">備註</span><span class="sxs-lookup"><span data-stu-id="13f91-115">Remarks</span></span>

<span data-ttu-id="13f91-116">此指令會在 src0 中，以 LSB 5) 0-31 (位所提供的不帶正負號的整數位元數目（在 *src1. select \_ 元件* 中，插入0），在中執行每個32位值的元件轉移。</span><span class="sxs-lookup"><span data-stu-id="13f91-116">This instruction performs a component-wise shift of each 32-bit value in *src0* left by an unsigned integer bit count provided by the LSB 5 bits (0-31 range) in *src1.select\_component*, inserting 0.</span></span> <span data-ttu-id="13f91-117">每個元件的32位結果都會放置在 *dest* 中。</span><span class="sxs-lookup"><span data-stu-id="13f91-117">The 32-bit per component results are placed in *dest*.</span></span> <span data-ttu-id="13f91-118">計數是套用至所有元件的純量值。</span><span class="sxs-lookup"><span data-stu-id="13f91-118">The count is a scalar value applied to all components.</span></span>

<span data-ttu-id="13f91-119">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="13f91-119">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="13f91-120">頂點著色器</span><span class="sxs-lookup"><span data-stu-id="13f91-120">Vertex Shader</span></span> | <span data-ttu-id="13f91-121">幾何著色器</span><span class="sxs-lookup"><span data-stu-id="13f91-121">Geometry Shader</span></span> | <span data-ttu-id="13f91-122">像素著色器</span><span class="sxs-lookup"><span data-stu-id="13f91-122">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="13f91-123">x</span><span class="sxs-lookup"><span data-stu-id="13f91-123">x</span></span>             | <span data-ttu-id="13f91-124">x</span><span class="sxs-lookup"><span data-stu-id="13f91-124">x</span></span>               | <span data-ttu-id="13f91-125">x</span><span class="sxs-lookup"><span data-stu-id="13f91-125">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="13f91-126">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="13f91-126">Minimum Shader Model</span></span>

<span data-ttu-id="13f91-127">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="13f91-127">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="13f91-128">著色器模型</span><span class="sxs-lookup"><span data-stu-id="13f91-128">Shader Model</span></span>                                              | <span data-ttu-id="13f91-129">支援</span><span class="sxs-lookup"><span data-stu-id="13f91-129">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="13f91-130">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="13f91-130">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="13f91-131">是</span><span class="sxs-lookup"><span data-stu-id="13f91-131">yes</span></span>       |
| [<span data-ttu-id="13f91-132">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="13f91-132">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="13f91-133">是</span><span class="sxs-lookup"><span data-stu-id="13f91-133">yes</span></span>       |
| [<span data-ttu-id="13f91-134">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="13f91-134">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="13f91-135">是</span><span class="sxs-lookup"><span data-stu-id="13f91-135">yes</span></span>       |
| [<span data-ttu-id="13f91-136">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="13f91-136">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="13f91-137">不可以</span><span class="sxs-lookup"><span data-stu-id="13f91-137">no</span></span>        |
| [<span data-ttu-id="13f91-138">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="13f91-138">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="13f91-139">不可以</span><span class="sxs-lookup"><span data-stu-id="13f91-139">no</span></span>        |
| [<span data-ttu-id="13f91-140">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="13f91-140">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="13f91-141">不可以</span><span class="sxs-lookup"><span data-stu-id="13f91-141">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="13f91-142">相關主題</span><span class="sxs-lookup"><span data-stu-id="13f91-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="13f91-143">著色器模型4元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="13f91-143">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





