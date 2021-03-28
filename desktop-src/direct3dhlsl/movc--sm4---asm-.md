---
title: 'movc (sm4-asm) '
description: '以元件為條件的移動。 |movc (sm4-asm) '
ms.assetid: B7F19DF5-282F-41D4-AE2D-6ACF61A42088
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91aa3116b7bc13102386c57c9b8c63d3534147a8
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104991962"
---
# <a name="movc-sm4---asm"></a><span data-ttu-id="887c2-104">movc (sm4-asm) </span><span class="sxs-lookup"><span data-stu-id="887c2-104">movc (sm4 - asm)</span></span>

<span data-ttu-id="887c2-105">以元件為條件的移動。</span><span class="sxs-lookup"><span data-stu-id="887c2-105">Component-wise conditional move.</span></span>



| <span data-ttu-id="887c2-106">movc \[ \_ sat \] dest \[ . mask \] 、src0 \[ . swizzle \] 、 \[ - \] src1 \[ \_ abs \] \[ . swizzle \] 、 \[ - \] src2 收取 \[ \_ abs \] \[ . swizzle \] 、</span><span class="sxs-lookup"><span data-stu-id="887c2-106">movc\[\_sat\] dest\[.mask\], src0\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\], \[-\]src2\[\_abs\]\[.swizzle\],</span></span> |
|----------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="887c2-107">項目</span><span class="sxs-lookup"><span data-stu-id="887c2-107">Item</span></span>                                                            | <span data-ttu-id="887c2-108">描述</span><span class="sxs-lookup"><span data-stu-id="887c2-108">Description</span></span>                                                                                                                    |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="887c2-109"><span id="dest"></span><span id="DEST"></span>*目標*</span><span class="sxs-lookup"><span data-stu-id="887c2-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="887c2-110">\[在 \] 操作結果的位址中。</span><span class="sxs-lookup"><span data-stu-id="887c2-110">\[in\] The address of the result of the operation.</span></span> <br/> <span data-ttu-id="887c2-111">如果是 *src0*，則 *dest*  =  *src1* else *dest*  =  *src2 收取*</span><span class="sxs-lookup"><span data-stu-id="887c2-111">If *src0*, then *dest* = *src1* else *dest* = *src2*</span></span><br/> |
| <span data-ttu-id="887c2-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="887c2-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="887c2-113">\[在 \] 測試條件的元件中。</span><span class="sxs-lookup"><span data-stu-id="887c2-113">\[in\] The components on which to test the condition.</span></span><br/>                                                               |
| <span data-ttu-id="887c2-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="887c2-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="887c2-115">\[在 \] 要移動的元件中。</span><span class="sxs-lookup"><span data-stu-id="887c2-115">\[in\] The components to move.</span></span> <br/>                                                                                     |
| <span data-ttu-id="887c2-116"><span id="src2"></span><span id="SRC2"></span>*src2 收取*</span><span class="sxs-lookup"><span data-stu-id="887c2-116"><span id="src2"></span><span id="SRC2"></span>*src2*</span></span><br/> | <span data-ttu-id="887c2-117">\[在 \] 要移動的元件中。</span><span class="sxs-lookup"><span data-stu-id="887c2-117">\[in\] The components to move.</span></span><br/>                                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="887c2-118">備註</span><span class="sxs-lookup"><span data-stu-id="887c2-118">Remarks</span></span>

<span data-ttu-id="887c2-119">下列範例示範如何使用此指令。</span><span class="sxs-lookup"><span data-stu-id="887c2-119">The following example shows how to use this instruction.</span></span>

``` syntax
                for each component in dest[.mask]
                    if the corresponding component in src0 (POS-swizzle)
                       has any bit set
                    {
                        copy this component (POS-swizzle) from src1 into dest
                    }
                    else
                    {
                        copy this component (POS-swizzle) from src2 into dest
                    }
                endfor
```

<span data-ttu-id="887c2-120">*Src1* 和 *src2 收取* 上的修飾詞（除了 swizzle 以外）會假設資料是浮點數。</span><span class="sxs-lookup"><span data-stu-id="887c2-120">The modifiers on *src1* and *src2*, other than swizzle, assume the data is floating point.</span></span> <span data-ttu-id="887c2-121">缺少修飾詞只會在不改變位的情況下移動資料。</span><span class="sxs-lookup"><span data-stu-id="887c2-121">The absence of modifiers just moves data without altering bits.</span></span>

<span data-ttu-id="887c2-122">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="887c2-122">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="887c2-123">頂點著色器</span><span class="sxs-lookup"><span data-stu-id="887c2-123">Vertex Shader</span></span> | <span data-ttu-id="887c2-124">幾何著色器</span><span class="sxs-lookup"><span data-stu-id="887c2-124">Geometry Shader</span></span> | <span data-ttu-id="887c2-125">像素著色器</span><span class="sxs-lookup"><span data-stu-id="887c2-125">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="887c2-126">x</span><span class="sxs-lookup"><span data-stu-id="887c2-126">x</span></span>             | <span data-ttu-id="887c2-127">x</span><span class="sxs-lookup"><span data-stu-id="887c2-127">x</span></span>               | <span data-ttu-id="887c2-128">x</span><span class="sxs-lookup"><span data-stu-id="887c2-128">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="887c2-129">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="887c2-129">Minimum Shader Model</span></span>

<span data-ttu-id="887c2-130">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="887c2-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="887c2-131">著色器模型</span><span class="sxs-lookup"><span data-stu-id="887c2-131">Shader Model</span></span>                                              | <span data-ttu-id="887c2-132">支援</span><span class="sxs-lookup"><span data-stu-id="887c2-132">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="887c2-133">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="887c2-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="887c2-134">是</span><span class="sxs-lookup"><span data-stu-id="887c2-134">yes</span></span>       |
| [<span data-ttu-id="887c2-135">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="887c2-135">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="887c2-136">是</span><span class="sxs-lookup"><span data-stu-id="887c2-136">yes</span></span>       |
| [<span data-ttu-id="887c2-137">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="887c2-137">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="887c2-138">是</span><span class="sxs-lookup"><span data-stu-id="887c2-138">yes</span></span>       |
| [<span data-ttu-id="887c2-139">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="887c2-139">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="887c2-140">不可以</span><span class="sxs-lookup"><span data-stu-id="887c2-140">no</span></span>        |
| [<span data-ttu-id="887c2-141">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="887c2-141">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="887c2-142">不可以</span><span class="sxs-lookup"><span data-stu-id="887c2-142">no</span></span>        |
| [<span data-ttu-id="887c2-143">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="887c2-143">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="887c2-144">不可以</span><span class="sxs-lookup"><span data-stu-id="887c2-144">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="887c2-145">相關主題</span><span class="sxs-lookup"><span data-stu-id="887c2-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="887c2-146">著色器模型4元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="887c2-146">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





