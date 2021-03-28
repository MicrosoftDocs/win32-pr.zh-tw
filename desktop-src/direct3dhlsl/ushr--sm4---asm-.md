---
title: 'ushr (sm4-asm) '
description: '右移。 |ushr (sm4-asm) '
ms.assetid: 3E7CB515-9D0F-44C7-A770-AD0584631BFE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c48b706afb1223a5289f93b5ca393a89c36e915
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104195916"
---
# <a name="ushr-sm4---asm"></a><span data-ttu-id="a3feb-104">ushr (sm4-asm) </span><span class="sxs-lookup"><span data-stu-id="a3feb-104">ushr (sm4 - asm)</span></span>

<span data-ttu-id="a3feb-105">右移。</span><span class="sxs-lookup"><span data-stu-id="a3feb-105">Shift right.</span></span>



| <span data-ttu-id="a3feb-106">ushr dest \[ . mask \] ，src0 \[ . swizzle \] ，src1. select \_ component</span><span class="sxs-lookup"><span data-stu-id="a3feb-106">ushr dest\[.mask\], src0\[.swizzle\], src1.select\_component</span></span> |
|--------------------------------------------------------------|



 



| <span data-ttu-id="a3feb-107">項目</span><span class="sxs-lookup"><span data-stu-id="a3feb-107">Item</span></span>                                                            | <span data-ttu-id="a3feb-108">描述</span><span class="sxs-lookup"><span data-stu-id="a3feb-108">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="a3feb-109"><span id="dest"></span><span id="DEST"></span>*目標*</span><span class="sxs-lookup"><span data-stu-id="a3feb-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="a3feb-110">\[在 \] 操作結果的位址中。</span><span class="sxs-lookup"><span data-stu-id="a3feb-110">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="a3feb-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="a3feb-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="a3feb-112">\[在 \] 要移位的元件中。</span><span class="sxs-lookup"><span data-stu-id="a3feb-112">\[in\] The components to shift.</span></span><br/>                    |
| <span data-ttu-id="a3feb-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="a3feb-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="a3feb-114">\[在 \] [要移位的數量] *src0* 中。</span><span class="sxs-lookup"><span data-stu-id="a3feb-114">\[in\] The amount to shift *src0*.</span></span><br/>                 |



 

## <a name="remarks"></a><span data-ttu-id="a3feb-115">備註</span><span class="sxs-lookup"><span data-stu-id="a3feb-115">Remarks</span></span>

<span data-ttu-id="a3feb-116">此指令會在 *src0* 中執行每個32位值的元件轉移，由 LSB 5 位所提供的不帶正負號整數位計數 (0-31 範圍) 在 *src1 中。選取 \_ 元件*，插入0。</span><span class="sxs-lookup"><span data-stu-id="a3feb-116">This instruction performs a component-wise shift of each 32-bit value in *src0* right by an unsigned integer bit count provided by the LSB 5 bits (0-31 range) in *src1.select\_component*, inserting 0.</span></span> <span data-ttu-id="a3feb-117">每個元件的32位結果都會放置在 *dest* 中。</span><span class="sxs-lookup"><span data-stu-id="a3feb-117">The 32-bit per component result is placed in *dest*.</span></span> <span data-ttu-id="a3feb-118">計數是套用至所有元件的純量值。</span><span class="sxs-lookup"><span data-stu-id="a3feb-118">The count is a scalar value applied to all components.</span></span>

<span data-ttu-id="a3feb-119">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="a3feb-119">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="a3feb-120">頂點著色器</span><span class="sxs-lookup"><span data-stu-id="a3feb-120">Vertex Shader</span></span> | <span data-ttu-id="a3feb-121">幾何著色器</span><span class="sxs-lookup"><span data-stu-id="a3feb-121">Geometry Shader</span></span> | <span data-ttu-id="a3feb-122">像素著色器</span><span class="sxs-lookup"><span data-stu-id="a3feb-122">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="a3feb-123">x</span><span class="sxs-lookup"><span data-stu-id="a3feb-123">x</span></span>             | <span data-ttu-id="a3feb-124">x</span><span class="sxs-lookup"><span data-stu-id="a3feb-124">x</span></span>               | <span data-ttu-id="a3feb-125">x</span><span class="sxs-lookup"><span data-stu-id="a3feb-125">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="a3feb-126">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="a3feb-126">Minimum Shader Model</span></span>

<span data-ttu-id="a3feb-127">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="a3feb-127">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="a3feb-128">著色器模型</span><span class="sxs-lookup"><span data-stu-id="a3feb-128">Shader Model</span></span>                                              | <span data-ttu-id="a3feb-129">支援</span><span class="sxs-lookup"><span data-stu-id="a3feb-129">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="a3feb-130">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="a3feb-130">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="a3feb-131">是</span><span class="sxs-lookup"><span data-stu-id="a3feb-131">yes</span></span>       |
| [<span data-ttu-id="a3feb-132">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="a3feb-132">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="a3feb-133">是</span><span class="sxs-lookup"><span data-stu-id="a3feb-133">yes</span></span>       |
| [<span data-ttu-id="a3feb-134">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="a3feb-134">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="a3feb-135">是</span><span class="sxs-lookup"><span data-stu-id="a3feb-135">yes</span></span>       |
| [<span data-ttu-id="a3feb-136">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="a3feb-136">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="a3feb-137">不可以</span><span class="sxs-lookup"><span data-stu-id="a3feb-137">no</span></span>        |
| [<span data-ttu-id="a3feb-138">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="a3feb-138">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="a3feb-139">不可以</span><span class="sxs-lookup"><span data-stu-id="a3feb-139">no</span></span>        |
| [<span data-ttu-id="a3feb-140">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="a3feb-140">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="a3feb-141">不可以</span><span class="sxs-lookup"><span data-stu-id="a3feb-141">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="a3feb-142">相關主題</span><span class="sxs-lookup"><span data-stu-id="a3feb-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a3feb-143">著色器模型4元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="a3feb-143">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





