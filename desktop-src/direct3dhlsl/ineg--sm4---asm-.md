---
title: 'ineg (sm4-asm) '
description: 2的補數。
ms.assetid: 20C1EEC8-E349-4398-8EE3-EDD01EBCD4B1
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec4da3e0cbb08bee7bd732a4da8175705d1e1a0f
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104373847"
---
# <a name="ineg-sm4---asm"></a><span data-ttu-id="4d2fa-103">ineg (sm4-asm) </span><span class="sxs-lookup"><span data-stu-id="4d2fa-103">ineg (sm4 - asm)</span></span>

<span data-ttu-id="4d2fa-104">2的補數。</span><span class="sxs-lookup"><span data-stu-id="4d2fa-104">2's complement.</span></span>



| <span data-ttu-id="4d2fa-105">ineg dest \[ . mask \] ，src0 \[ . swizzle</span><span class="sxs-lookup"><span data-stu-id="4d2fa-105">ineg dest\[.mask\], src0\[.swizzle</span></span> |
|------------------------------------|



 



| <span data-ttu-id="4d2fa-106">項目</span><span class="sxs-lookup"><span data-stu-id="4d2fa-106">Item</span></span>                                                            | <span data-ttu-id="4d2fa-107">描述</span><span class="sxs-lookup"><span data-stu-id="4d2fa-107">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="4d2fa-108"><span id="dest"></span><span id="DEST"></span>*目標*</span><span class="sxs-lookup"><span data-stu-id="4d2fa-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="4d2fa-109">\[在 \] 操作結果的位址中。</span><span class="sxs-lookup"><span data-stu-id="4d2fa-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="4d2fa-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="4d2fa-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="4d2fa-111">\[in \] 包含作業的值。</span><span class="sxs-lookup"><span data-stu-id="4d2fa-111">\[in\] Contains the values for the operation.</span></span><br/>      |



 

## <a name="remarks"></a><span data-ttu-id="4d2fa-112">備註</span><span class="sxs-lookup"><span data-stu-id="4d2fa-112">Remarks</span></span>

<span data-ttu-id="4d2fa-113">此指令會在 *src0* 中執行每個32位值的元件成對2補數。</span><span class="sxs-lookup"><span data-stu-id="4d2fa-113">This instruction performs component-wise 2's complement of each 32-bit value in *src0*.</span></span> <span data-ttu-id="4d2fa-114">32位的結果會儲存在 *dest* 中。</span><span class="sxs-lookup"><span data-stu-id="4d2fa-114">The 32-bit results are stored in *dest*.</span></span>

<span data-ttu-id="4d2fa-115">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="4d2fa-115">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="4d2fa-116">頂點著色器</span><span class="sxs-lookup"><span data-stu-id="4d2fa-116">Vertex Shader</span></span> | <span data-ttu-id="4d2fa-117">幾何著色器</span><span class="sxs-lookup"><span data-stu-id="4d2fa-117">Geometry Shader</span></span> | <span data-ttu-id="4d2fa-118">像素著色器</span><span class="sxs-lookup"><span data-stu-id="4d2fa-118">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="4d2fa-119">x</span><span class="sxs-lookup"><span data-stu-id="4d2fa-119">x</span></span>             | <span data-ttu-id="4d2fa-120">x</span><span class="sxs-lookup"><span data-stu-id="4d2fa-120">x</span></span>               | <span data-ttu-id="4d2fa-121">x</span><span class="sxs-lookup"><span data-stu-id="4d2fa-121">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="4d2fa-122">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="4d2fa-122">Minimum Shader Model</span></span>

<span data-ttu-id="4d2fa-123">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="4d2fa-123">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="4d2fa-124">著色器模型</span><span class="sxs-lookup"><span data-stu-id="4d2fa-124">Shader Model</span></span>                                              | <span data-ttu-id="4d2fa-125">支援</span><span class="sxs-lookup"><span data-stu-id="4d2fa-125">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="4d2fa-126">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="4d2fa-126">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="4d2fa-127">是</span><span class="sxs-lookup"><span data-stu-id="4d2fa-127">yes</span></span>       |
| [<span data-ttu-id="4d2fa-128">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="4d2fa-128">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="4d2fa-129">是</span><span class="sxs-lookup"><span data-stu-id="4d2fa-129">yes</span></span>       |
| [<span data-ttu-id="4d2fa-130">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="4d2fa-130">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="4d2fa-131">是</span><span class="sxs-lookup"><span data-stu-id="4d2fa-131">yes</span></span>       |
| [<span data-ttu-id="4d2fa-132">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="4d2fa-132">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="4d2fa-133">不可以</span><span class="sxs-lookup"><span data-stu-id="4d2fa-133">no</span></span>        |
| [<span data-ttu-id="4d2fa-134">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="4d2fa-134">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="4d2fa-135">不可以</span><span class="sxs-lookup"><span data-stu-id="4d2fa-135">no</span></span>        |
| [<span data-ttu-id="4d2fa-136">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="4d2fa-136">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="4d2fa-137">不可以</span><span class="sxs-lookup"><span data-stu-id="4d2fa-137">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="4d2fa-138">相關主題</span><span class="sxs-lookup"><span data-stu-id="4d2fa-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4d2fa-139">著色器模型4元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="4d2fa-139">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





