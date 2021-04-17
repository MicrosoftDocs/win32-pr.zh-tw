---
title: '或 (sm4-asm) '
description: 位 or。
ms.assetid: BBC06F8C-4C86-4077-A1F9-383D6A8FBED3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62064189725b246cc48bbde03a9c094d13f8b9a0
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104990799"
---
# <a name="or-sm4---asm"></a><span data-ttu-id="1cc1b-103">或 (sm4-asm) </span><span class="sxs-lookup"><span data-stu-id="1cc1b-103">or (sm4 - asm)</span></span>

<span data-ttu-id="1cc1b-104">位 or。</span><span class="sxs-lookup"><span data-stu-id="1cc1b-104">Bitwise or.</span></span>



| <span data-ttu-id="1cc1b-105">或 dest \[ \] 、src0 \[ . swizzle \] 、src1 \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="1cc1b-105">or dest\[.mask\], src0\[.swizzle\], src1\[.swizzle\]</span></span> |
|------------------------------------------------------|



 



| <span data-ttu-id="1cc1b-106">項目</span><span class="sxs-lookup"><span data-stu-id="1cc1b-106">Item</span></span>                                                            | <span data-ttu-id="1cc1b-107">描述</span><span class="sxs-lookup"><span data-stu-id="1cc1b-107">Description</span></span>                                         |
|-----------------------------------------------------------------|-----------------------------------------------------|
| <span data-ttu-id="1cc1b-108"><span id="dest"></span><span id="DEST"></span>*目標*</span><span class="sxs-lookup"><span data-stu-id="1cc1b-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="1cc1b-109">\[在作業的 \] 結果中。</span><span class="sxs-lookup"><span data-stu-id="1cc1b-109">\[in\] The result of the operation.</span></span><br/>      |
| <span data-ttu-id="1cc1b-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="1cc1b-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="1cc1b-111">\[在 \] *src1* 的元件中。</span><span class="sxs-lookup"><span data-stu-id="1cc1b-111">\[in\] The components to OR with *src1*.</span></span><br/> |
| <span data-ttu-id="1cc1b-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="1cc1b-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="1cc1b-113">\[在 \] *src0* 的元件中。</span><span class="sxs-lookup"><span data-stu-id="1cc1b-113">\[in\] The components to OR with *src0*.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="1cc1b-114">備註</span><span class="sxs-lookup"><span data-stu-id="1cc1b-114">Remarks</span></span>

<span data-ttu-id="1cc1b-115">此指令會從 *src0* 和 *src1* 執行每對32位值配對的元件邏輯 OR。</span><span class="sxs-lookup"><span data-stu-id="1cc1b-115">This instruction performs a component-wise logical OR of each pair of 32-bit values from *src0* and *src1*.</span></span> <span data-ttu-id="1cc1b-116">32位的結果會放在 *dest* 中。</span><span class="sxs-lookup"><span data-stu-id="1cc1b-116">The 32-bit results are placed in *dest*.</span></span>

<span data-ttu-id="1cc1b-117">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="1cc1b-117">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="1cc1b-118">頂點著色器</span><span class="sxs-lookup"><span data-stu-id="1cc1b-118">Vertex Shader</span></span> | <span data-ttu-id="1cc1b-119">幾何著色器</span><span class="sxs-lookup"><span data-stu-id="1cc1b-119">Geometry Shader</span></span> | <span data-ttu-id="1cc1b-120">像素著色器</span><span class="sxs-lookup"><span data-stu-id="1cc1b-120">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="1cc1b-121">x</span><span class="sxs-lookup"><span data-stu-id="1cc1b-121">x</span></span>             | <span data-ttu-id="1cc1b-122">x</span><span class="sxs-lookup"><span data-stu-id="1cc1b-122">x</span></span>               | <span data-ttu-id="1cc1b-123">x</span><span class="sxs-lookup"><span data-stu-id="1cc1b-123">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="1cc1b-124">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="1cc1b-124">Minimum Shader Model</span></span>

<span data-ttu-id="1cc1b-125">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="1cc1b-125">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="1cc1b-126">著色器模型</span><span class="sxs-lookup"><span data-stu-id="1cc1b-126">Shader Model</span></span>                                              | <span data-ttu-id="1cc1b-127">支援</span><span class="sxs-lookup"><span data-stu-id="1cc1b-127">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="1cc1b-128">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="1cc1b-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="1cc1b-129">是</span><span class="sxs-lookup"><span data-stu-id="1cc1b-129">yes</span></span>       |
| [<span data-ttu-id="1cc1b-130">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="1cc1b-130">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="1cc1b-131">是</span><span class="sxs-lookup"><span data-stu-id="1cc1b-131">yes</span></span>       |
| [<span data-ttu-id="1cc1b-132">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="1cc1b-132">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="1cc1b-133">是</span><span class="sxs-lookup"><span data-stu-id="1cc1b-133">yes</span></span>       |
| [<span data-ttu-id="1cc1b-134">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="1cc1b-134">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="1cc1b-135">不可以</span><span class="sxs-lookup"><span data-stu-id="1cc1b-135">no</span></span>        |
| [<span data-ttu-id="1cc1b-136">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="1cc1b-136">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="1cc1b-137">不可以</span><span class="sxs-lookup"><span data-stu-id="1cc1b-137">no</span></span>        |
| [<span data-ttu-id="1cc1b-138">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="1cc1b-138">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="1cc1b-139">不可以</span><span class="sxs-lookup"><span data-stu-id="1cc1b-139">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="1cc1b-140">相關主題</span><span class="sxs-lookup"><span data-stu-id="1cc1b-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1cc1b-141">著色器模型4元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="1cc1b-141">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





