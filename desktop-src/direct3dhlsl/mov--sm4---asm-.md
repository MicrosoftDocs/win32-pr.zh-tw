---
title: 'mov (sm4-asm) '
description: '元件取向的移動。 |mov (sm4-asm) '
ms.assetid: A8865237-59D3-4332-9F09-157E10C4FFC6
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f029cd8a31a9348e729681878773c225b87b9fbb
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104195881"
---
# <a name="mov-sm4---asm"></a><span data-ttu-id="14ba9-104">mov (sm4-asm) </span><span class="sxs-lookup"><span data-stu-id="14ba9-104">mov (sm4 - asm)</span></span>

<span data-ttu-id="14ba9-105">元件取向的移動。</span><span class="sxs-lookup"><span data-stu-id="14ba9-105">Component-wise move.</span></span>



| <span data-ttu-id="14ba9-106">指示： mov \[ \_ sat \] dest \[ . mask \] ， \[ - \] src0 \[ \_ abs \] \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="14ba9-106">Instruction: mov\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|-------------------------------------------------------------------------|



 



| <span data-ttu-id="14ba9-107">項目</span><span class="sxs-lookup"><span data-stu-id="14ba9-107">Item</span></span>                                                            | <span data-ttu-id="14ba9-108">描述</span><span class="sxs-lookup"><span data-stu-id="14ba9-108">Description</span></span>                                                                              |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="14ba9-109"><span id="dest"></span><span id="DEST"></span>*目標*</span><span class="sxs-lookup"><span data-stu-id="14ba9-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="14ba9-110">\[在 \] 操作結果的位址中。</span><span class="sxs-lookup"><span data-stu-id="14ba9-110">\[in\] The address of the result of the operation.</span></span><br/> <span data-ttu-id="14ba9-111">*目的地*  = *src0*</span><span class="sxs-lookup"><span data-stu-id="14ba9-111">*dest* = *src0*</span></span><br/> |
| <span data-ttu-id="14ba9-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="14ba9-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="14ba9-113">\[在 \] 要移動的元件中。</span><span class="sxs-lookup"><span data-stu-id="14ba9-113">\[in\] The components to move.</span></span><br/>                                                |



 

## <a name="remarks"></a><span data-ttu-id="14ba9-114">備註</span><span class="sxs-lookup"><span data-stu-id="14ba9-114">Remarks</span></span>

<span data-ttu-id="14ba9-115">Swizzle 以外的修飾詞會假設資料是浮點。</span><span class="sxs-lookup"><span data-stu-id="14ba9-115">The modifiers, other than swizzle, assume the data is floating point.</span></span> <span data-ttu-id="14ba9-116">缺少修飾詞只會在不改變位的情況下移動資料。</span><span class="sxs-lookup"><span data-stu-id="14ba9-116">The absence of modifiers just moves data without altering bits.</span></span>

<span data-ttu-id="14ba9-117">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="14ba9-117">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="14ba9-118">頂點著色器</span><span class="sxs-lookup"><span data-stu-id="14ba9-118">Vertex Shader</span></span> | <span data-ttu-id="14ba9-119">幾何著色器</span><span class="sxs-lookup"><span data-stu-id="14ba9-119">Geometry Shader</span></span> | <span data-ttu-id="14ba9-120">像素著色器</span><span class="sxs-lookup"><span data-stu-id="14ba9-120">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="14ba9-121">x</span><span class="sxs-lookup"><span data-stu-id="14ba9-121">x</span></span>             | <span data-ttu-id="14ba9-122">x</span><span class="sxs-lookup"><span data-stu-id="14ba9-122">x</span></span>               | <span data-ttu-id="14ba9-123">x</span><span class="sxs-lookup"><span data-stu-id="14ba9-123">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="14ba9-124">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="14ba9-124">Minimum Shader Model</span></span>

<span data-ttu-id="14ba9-125">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="14ba9-125">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="14ba9-126">著色器模型</span><span class="sxs-lookup"><span data-stu-id="14ba9-126">Shader Model</span></span>                                              | <span data-ttu-id="14ba9-127">支援</span><span class="sxs-lookup"><span data-stu-id="14ba9-127">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="14ba9-128">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="14ba9-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="14ba9-129">是</span><span class="sxs-lookup"><span data-stu-id="14ba9-129">yes</span></span>       |
| [<span data-ttu-id="14ba9-130">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="14ba9-130">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="14ba9-131">是</span><span class="sxs-lookup"><span data-stu-id="14ba9-131">yes</span></span>       |
| [<span data-ttu-id="14ba9-132">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="14ba9-132">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="14ba9-133">是</span><span class="sxs-lookup"><span data-stu-id="14ba9-133">yes</span></span>       |
| [<span data-ttu-id="14ba9-134">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="14ba9-134">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="14ba9-135">不可以</span><span class="sxs-lookup"><span data-stu-id="14ba9-135">no</span></span>        |
| [<span data-ttu-id="14ba9-136">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="14ba9-136">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="14ba9-137">不可以</span><span class="sxs-lookup"><span data-stu-id="14ba9-137">no</span></span>        |
| [<span data-ttu-id="14ba9-138">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="14ba9-138">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="14ba9-139">不可以</span><span class="sxs-lookup"><span data-stu-id="14ba9-139">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="14ba9-140">相關主題</span><span class="sxs-lookup"><span data-stu-id="14ba9-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="14ba9-141">著色器模型4元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="14ba9-141">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





