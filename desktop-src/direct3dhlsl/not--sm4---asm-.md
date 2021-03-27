---
title: '不 (sm4-asm) '
description: 位 not。
ms.assetid: AC7EBBC2-4B52-4793-812C-B25897FB8D05
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0bf224e6e5af7f2db6bcbaf7ae287ba2d399727
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104971597"
---
# <a name="not-sm4---asm"></a><span data-ttu-id="5c68d-103">不 (sm4-asm) </span><span class="sxs-lookup"><span data-stu-id="5c68d-103">not (sm4 - asm)</span></span>

<span data-ttu-id="5c68d-104">位 not。</span><span class="sxs-lookup"><span data-stu-id="5c68d-104">Bitwise not.</span></span>



| <span data-ttu-id="5c68d-105">not dest \[ \] 、src0 \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="5c68d-105">not dest\[.mask\], src0\[.swizzle\]</span></span> |
|-------------------------------------|



 



| <span data-ttu-id="5c68d-106">項目</span><span class="sxs-lookup"><span data-stu-id="5c68d-106">Item</span></span>                                                            | <span data-ttu-id="5c68d-107">描述</span><span class="sxs-lookup"><span data-stu-id="5c68d-107">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="5c68d-108"><span id="dest"></span><span id="DEST"></span>*目標*</span><span class="sxs-lookup"><span data-stu-id="5c68d-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="5c68d-109">\[在 \] 操作結果的位址中。</span><span class="sxs-lookup"><span data-stu-id="5c68d-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="5c68d-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="5c68d-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="5c68d-111">\[在 \] 原始的元件中。</span><span class="sxs-lookup"><span data-stu-id="5c68d-111">\[in\] The original components.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="5c68d-112">備註</span><span class="sxs-lookup"><span data-stu-id="5c68d-112">Remarks</span></span>

<span data-ttu-id="5c68d-113">此指令會在 *src0* 中執行每個32位值的元件一補數。</span><span class="sxs-lookup"><span data-stu-id="5c68d-113">This instruction performs a component-wise one's complement of each 32-bit value in *src0*.</span></span> <span data-ttu-id="5c68d-114">32位的結果會儲存在 *dest* 中。</span><span class="sxs-lookup"><span data-stu-id="5c68d-114">The 32-bit results are stored in *dest*.</span></span>

<span data-ttu-id="5c68d-115">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="5c68d-115">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="5c68d-116">頂點著色器</span><span class="sxs-lookup"><span data-stu-id="5c68d-116">Vertex Shader</span></span> | <span data-ttu-id="5c68d-117">幾何著色器</span><span class="sxs-lookup"><span data-stu-id="5c68d-117">Geometry Shader</span></span> | <span data-ttu-id="5c68d-118">像素著色器</span><span class="sxs-lookup"><span data-stu-id="5c68d-118">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="5c68d-119">x</span><span class="sxs-lookup"><span data-stu-id="5c68d-119">x</span></span>             | <span data-ttu-id="5c68d-120">x</span><span class="sxs-lookup"><span data-stu-id="5c68d-120">x</span></span>               | <span data-ttu-id="5c68d-121">x</span><span class="sxs-lookup"><span data-stu-id="5c68d-121">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="5c68d-122">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="5c68d-122">Minimum Shader Model</span></span>

<span data-ttu-id="5c68d-123">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="5c68d-123">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="5c68d-124">著色器模型</span><span class="sxs-lookup"><span data-stu-id="5c68d-124">Shader Model</span></span>                                              | <span data-ttu-id="5c68d-125">支援</span><span class="sxs-lookup"><span data-stu-id="5c68d-125">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="5c68d-126">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="5c68d-126">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="5c68d-127">是</span><span class="sxs-lookup"><span data-stu-id="5c68d-127">yes</span></span>       |
| [<span data-ttu-id="5c68d-128">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="5c68d-128">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="5c68d-129">是</span><span class="sxs-lookup"><span data-stu-id="5c68d-129">yes</span></span>       |
| [<span data-ttu-id="5c68d-130">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="5c68d-130">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="5c68d-131">是</span><span class="sxs-lookup"><span data-stu-id="5c68d-131">yes</span></span>       |
| [<span data-ttu-id="5c68d-132">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="5c68d-132">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="5c68d-133">不可以</span><span class="sxs-lookup"><span data-stu-id="5c68d-133">no</span></span>        |
| [<span data-ttu-id="5c68d-134">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="5c68d-134">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="5c68d-135">不可以</span><span class="sxs-lookup"><span data-stu-id="5c68d-135">no</span></span>        |
| [<span data-ttu-id="5c68d-136">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="5c68d-136">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="5c68d-137">不可以</span><span class="sxs-lookup"><span data-stu-id="5c68d-137">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="5c68d-138">相關主題</span><span class="sxs-lookup"><span data-stu-id="5c68d-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5c68d-139">著色器模型4元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="5c68d-139">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





