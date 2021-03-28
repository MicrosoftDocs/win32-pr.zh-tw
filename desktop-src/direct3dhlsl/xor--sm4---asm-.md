---
title: 'xor (sm4-asm) '
description: 位 xor。
ms.assetid: 6B949653-6DDA-402B-8ABE-B93858B68470
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7a998bd1e95793f463d7f234b464a542bed4fc0
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104373707"
---
# <a name="xor-sm4---asm"></a><span data-ttu-id="60385-103">xor (sm4-asm) </span><span class="sxs-lookup"><span data-stu-id="60385-103">xor (sm4 - asm)</span></span>

<span data-ttu-id="60385-104">位 xor。</span><span class="sxs-lookup"><span data-stu-id="60385-104">Bitwise xor.</span></span>



| <span data-ttu-id="60385-105">xor dest \[ . mask \] 、src0 \[ . swizzle \] 、src1 \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="60385-105">xor dest\[.mask\], src0\[.swizzle\], src1\[.swizzle\]</span></span> |
|-------------------------------------------------------|



 



| <span data-ttu-id="60385-106">項目</span><span class="sxs-lookup"><span data-stu-id="60385-106">Item</span></span>                                                            | <span data-ttu-id="60385-107">描述</span><span class="sxs-lookup"><span data-stu-id="60385-107">Description</span></span>                                          |
|-----------------------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="60385-108"><span id="dest"></span><span id="DEST"></span>*目標*</span><span class="sxs-lookup"><span data-stu-id="60385-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="60385-109">\[在作業的 \] 結果中。</span><span class="sxs-lookup"><span data-stu-id="60385-109">\[in\] The result of the operation.</span></span><br/>       |
| <span data-ttu-id="60385-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="60385-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="60385-111">\[在 \] 與 *src1* XOR 的元件中。</span><span class="sxs-lookup"><span data-stu-id="60385-111">\[in\] The components to XOR with *src1*.</span></span><br/> |
| <span data-ttu-id="60385-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="60385-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="60385-113">\[在 \] 與 *src0* XOR 的元件中。</span><span class="sxs-lookup"><span data-stu-id="60385-113">\[in\] The components to XOR with *src0*.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="60385-114">備註</span><span class="sxs-lookup"><span data-stu-id="60385-114">Remarks</span></span>

<span data-ttu-id="60385-115">此指令會針對 *src0* 和 *src1* 中的每一對32位值，執行每一組的元件的邏輯 XOR。</span><span class="sxs-lookup"><span data-stu-id="60385-115">This instruction performs a component-wise logical XOR of each pair of 32-bit values from *src0* and *src1*.</span></span> <span data-ttu-id="60385-116">32位結果會放在 *dest* 中。</span><span class="sxs-lookup"><span data-stu-id="60385-116">32-bit results are placed in *dest*.</span></span>

<span data-ttu-id="60385-117">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="60385-117">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="60385-118">頂點著色器</span><span class="sxs-lookup"><span data-stu-id="60385-118">Vertex Shader</span></span> | <span data-ttu-id="60385-119">幾何著色器</span><span class="sxs-lookup"><span data-stu-id="60385-119">Geometry Shader</span></span> | <span data-ttu-id="60385-120">像素著色器</span><span class="sxs-lookup"><span data-stu-id="60385-120">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="60385-121">x</span><span class="sxs-lookup"><span data-stu-id="60385-121">x</span></span>             | <span data-ttu-id="60385-122">x</span><span class="sxs-lookup"><span data-stu-id="60385-122">x</span></span>               | <span data-ttu-id="60385-123">x</span><span class="sxs-lookup"><span data-stu-id="60385-123">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="60385-124">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="60385-124">Minimum Shader Model</span></span>

<span data-ttu-id="60385-125">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="60385-125">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="60385-126">著色器模型</span><span class="sxs-lookup"><span data-stu-id="60385-126">Shader Model</span></span>                                              | <span data-ttu-id="60385-127">支援</span><span class="sxs-lookup"><span data-stu-id="60385-127">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="60385-128">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="60385-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="60385-129">是</span><span class="sxs-lookup"><span data-stu-id="60385-129">yes</span></span>       |
| [<span data-ttu-id="60385-130">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="60385-130">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="60385-131">是</span><span class="sxs-lookup"><span data-stu-id="60385-131">yes</span></span>       |
| [<span data-ttu-id="60385-132">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="60385-132">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="60385-133">是</span><span class="sxs-lookup"><span data-stu-id="60385-133">yes</span></span>       |
| [<span data-ttu-id="60385-134">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="60385-134">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="60385-135">不可以</span><span class="sxs-lookup"><span data-stu-id="60385-135">no</span></span>        |
| [<span data-ttu-id="60385-136">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="60385-136">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="60385-137">不可以</span><span class="sxs-lookup"><span data-stu-id="60385-137">no</span></span>        |
| [<span data-ttu-id="60385-138">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="60385-138">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="60385-139">不可以</span><span class="sxs-lookup"><span data-stu-id="60385-139">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="60385-140">相關主題</span><span class="sxs-lookup"><span data-stu-id="60385-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="60385-141">著色器模型4元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="60385-141">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





