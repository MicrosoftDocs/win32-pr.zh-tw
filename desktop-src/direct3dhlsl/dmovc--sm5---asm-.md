---
title: 'dmovc (sm5-asm) '
description: '以元件為條件的移動。 |dmovc (sm5-asm) '
ms.assetid: E376FE08-E251-4BE5-9F15-99B3B67A29C8
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e364e6340733c42ae69412db726851329eb2809d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104386360"
---
# <a name="dmovc-sm5---asm"></a><span data-ttu-id="6a32a-104">dmovc (sm5-asm) </span><span class="sxs-lookup"><span data-stu-id="6a32a-104">dmovc (sm5 - asm)</span></span>

<span data-ttu-id="6a32a-105">以元件為條件的移動。</span><span class="sxs-lookup"><span data-stu-id="6a32a-105">Component-wise conditional move.</span></span>



| <span data-ttu-id="6a32a-106">dmovc \[ \_ sat \] dest \[ . mask \] 、src0 \[ . swizzle \] 、 \[ - \] src1 \[ \_ abs \] \[ . swizzle \] 、 \[ - \] src2 收取 \[ \_ abs \] \[ . swizzle \] 、</span><span class="sxs-lookup"><span data-stu-id="6a32a-106">dmovc\[\_sat\] dest\[.mask\], src0\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\], \[-\]src2\[\_abs\]\[.swizzle\],</span></span> |
|-----------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="6a32a-107">項目</span><span class="sxs-lookup"><span data-stu-id="6a32a-107">Item</span></span>                                                            | <span data-ttu-id="6a32a-108">描述</span><span class="sxs-lookup"><span data-stu-id="6a32a-108">Description</span></span>                                                                                              |
|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a32a-109"><span id="dest"></span><span id="DEST"></span>*目標*</span><span class="sxs-lookup"><span data-stu-id="6a32a-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="6a32a-110">\[在 \] 移動目的地。</span><span class="sxs-lookup"><span data-stu-id="6a32a-110">\[in\] The move destination.</span></span><br/> <span data-ttu-id="6a32a-111">如果是 *src0*，則 *dest*  =  *src1* else *dest*  =  *src2 收取*。</span><span class="sxs-lookup"><span data-stu-id="6a32a-111">If *src0*, then *dest* = *src1* else *dest* = *src2*.</span></span><br/> |
| <span data-ttu-id="6a32a-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="6a32a-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="6a32a-113">\[用 \] 來測試條件的元件。</span><span class="sxs-lookup"><span data-stu-id="6a32a-113">\[in\] The components to test the condition against.</span></span><br/>                                          |
| <span data-ttu-id="6a32a-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="6a32a-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="6a32a-115">\[在 \] 條件為 true 時要移動的元件中。</span><span class="sxs-lookup"><span data-stu-id="6a32a-115">\[in\] The components to move if the condition is true.</span></span><br/>                                       |
| <span data-ttu-id="6a32a-116"><span id="src2"></span><span id="SRC2"></span>*src2 收取*</span><span class="sxs-lookup"><span data-stu-id="6a32a-116"><span id="src2"></span><span id="SRC2"></span>*src2*</span></span><br/> | <span data-ttu-id="6a32a-117">\[\]如果條件為 false，則在要移動的元件中。</span><span class="sxs-lookup"><span data-stu-id="6a32a-117">\[in\] The components to move if the condition is false.</span></span><br/>                                      |



 

## <a name="remarks"></a><span data-ttu-id="6a32a-118">備註</span><span class="sxs-lookup"><span data-stu-id="6a32a-118">Remarks</span></span>

<span data-ttu-id="6a32a-119">下列範例示範如何使用此指令。</span><span class="sxs-lookup"><span data-stu-id="6a32a-119">The following example shows how to use this instruction.</span></span>

``` syntax
                if(the dest mask contains .xy)
                {
                    if(the first 32-bit component of src0, post-swizzle, 
                       has any bit set)
                    {
                        copy the first double from src1 (post swizzle)
                        into dest.xy
                    }
                    else
                    {
                        copy the first double from src2 (post swizzle)
                        into dest.xy
                    }
                }
                if(the dest mask contains .zw)
                {
                    if(the second 32-bit component of src0, post-swizzle, 
                       has any bit set)
                    {
                        copy the second double from src1 (post swizzle)
                        into dest.zw
                    }
                    else
                    {
                        copy the second double from src2 (post swizzle)
                        into dest.zw
                    }
                }
```

<span data-ttu-id="6a32a-120">適用于 dest 的有效遮罩是 xy、. zw、. xyzw。</span><span class="sxs-lookup"><span data-stu-id="6a32a-120">The valid masks for dest are .xy, .zw, .xyzw.</span></span>

<span data-ttu-id="6a32a-121">適用于 *src0* 的有效 swizzles 為任何。</span><span class="sxs-lookup"><span data-stu-id="6a32a-121">The valid swizzles for *src0* are anything.</span></span> <span data-ttu-id="6a32a-122">Swizzle 後的前兩個元件會用來識別 2 32 位的條件值。</span><span class="sxs-lookup"><span data-stu-id="6a32a-122">The first two components post-swizzle are used to indentify two 32-bit condition values.</span></span>

<span data-ttu-id="6a32a-123">包含雙精度浮點數的 *src1* 和 *src2 收取* 的有效 swizzles 為. xyzw、. xyxy、. zwxy、. zwzw。</span><span class="sxs-lookup"><span data-stu-id="6a32a-123">The valid swizzles for *src1* and *src2* containing doubles are .xyzw, .xyxy, .zwxy, .zwzw.</span></span> <span data-ttu-id="6a32a-124">是 xy、. zw 和. xyzw。</span><span class="sxs-lookup"><span data-stu-id="6a32a-124">are .xy, .zw, and .xyzw.</span></span>

<span data-ttu-id="6a32a-125">下列 *src* 對應為 swizzle 後：</span><span class="sxs-lookup"><span data-stu-id="6a32a-125">The following *src* mappings below are post-swizzle:</span></span>

-   <span data-ttu-id="6a32a-126">*dest* 是跨 (x 32LSB、y 32MSB) 和 (z 32LSB、w 32MSB) 的雙 vec2。</span><span class="sxs-lookup"><span data-stu-id="6a32a-126">*dest* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>
-   <span data-ttu-id="6a32a-127">*src0* 是跨 x 和 y 的32位/元件 vec2 (zw 忽略) 。</span><span class="sxs-lookup"><span data-stu-id="6a32a-127">*src0* is a 32bit/component vec2 across x and y (zw ignored).</span></span>
-   <span data-ttu-id="6a32a-128">*src1* 是跨 (x 32LSB、y 32MSB) 和 (z 32LSB、w 32MSB) 的雙重 vec2。</span><span class="sxs-lookup"><span data-stu-id="6a32a-128">*src1* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>
-   <span data-ttu-id="6a32a-129">*src2 收取* 是跨 (x 32LSB、y 32MSB) 和 (z 32LSB、w 32MSB) 的雙重 vec2。</span><span class="sxs-lookup"><span data-stu-id="6a32a-129">*src2* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>

<span data-ttu-id="6a32a-130">*Src1* 和 *src2 收取* 上的修飾詞（除了 swizzle 以外）會假設資料是雙精度浮點數。</span><span class="sxs-lookup"><span data-stu-id="6a32a-130">The modifiers on *src1* and *src2*, other than swizzle, assume the data is double.</span></span> <span data-ttu-id="6a32a-131">缺少修飾詞會移動資料，而不會改變位。</span><span class="sxs-lookup"><span data-stu-id="6a32a-131">The absence of modifiers moves data without altering bits.</span></span>

<span data-ttu-id="6a32a-132">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="6a32a-132">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="6a32a-133">頂點</span><span class="sxs-lookup"><span data-stu-id="6a32a-133">Vertex</span></span> | <span data-ttu-id="6a32a-134">船體</span><span class="sxs-lookup"><span data-stu-id="6a32a-134">Hull</span></span> | <span data-ttu-id="6a32a-135">網域</span><span class="sxs-lookup"><span data-stu-id="6a32a-135">Domain</span></span> | <span data-ttu-id="6a32a-136">幾何</span><span class="sxs-lookup"><span data-stu-id="6a32a-136">Geometry</span></span> | <span data-ttu-id="6a32a-137">像素</span><span class="sxs-lookup"><span data-stu-id="6a32a-137">Pixel</span></span> | <span data-ttu-id="6a32a-138">計算</span><span class="sxs-lookup"><span data-stu-id="6a32a-138">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="6a32a-139">X</span><span class="sxs-lookup"><span data-stu-id="6a32a-139">X</span></span>      | <span data-ttu-id="6a32a-140">X</span><span class="sxs-lookup"><span data-stu-id="6a32a-140">X</span></span>    | <span data-ttu-id="6a32a-141">X</span><span class="sxs-lookup"><span data-stu-id="6a32a-141">X</span></span>      | <span data-ttu-id="6a32a-142">X</span><span class="sxs-lookup"><span data-stu-id="6a32a-142">X</span></span>        | <span data-ttu-id="6a32a-143">X</span><span class="sxs-lookup"><span data-stu-id="6a32a-143">X</span></span>     | <span data-ttu-id="6a32a-144">X</span><span class="sxs-lookup"><span data-stu-id="6a32a-144">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="6a32a-145">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="6a32a-145">Minimum Shader Model</span></span>

<span data-ttu-id="6a32a-146">下列著色器模型支援此指令：</span><span class="sxs-lookup"><span data-stu-id="6a32a-146">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="6a32a-147">著色器模型</span><span class="sxs-lookup"><span data-stu-id="6a32a-147">Shader Model</span></span>                                              | <span data-ttu-id="6a32a-148">支援</span><span class="sxs-lookup"><span data-stu-id="6a32a-148">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="6a32a-149">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="6a32a-149">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="6a32a-150">是</span><span class="sxs-lookup"><span data-stu-id="6a32a-150">yes</span></span>       |
| [<span data-ttu-id="6a32a-151">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="6a32a-151">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="6a32a-152">不可以</span><span class="sxs-lookup"><span data-stu-id="6a32a-152">no</span></span>        |
| [<span data-ttu-id="6a32a-153">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="6a32a-153">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="6a32a-154">不可以</span><span class="sxs-lookup"><span data-stu-id="6a32a-154">no</span></span>        |
| [<span data-ttu-id="6a32a-155">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="6a32a-155">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="6a32a-156">不可以</span><span class="sxs-lookup"><span data-stu-id="6a32a-156">no</span></span>        |
| [<span data-ttu-id="6a32a-157">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="6a32a-157">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="6a32a-158">不可以</span><span class="sxs-lookup"><span data-stu-id="6a32a-158">no</span></span>        |
| [<span data-ttu-id="6a32a-159">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="6a32a-159">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="6a32a-160">不可以</span><span class="sxs-lookup"><span data-stu-id="6a32a-160">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="6a32a-161">相關主題</span><span class="sxs-lookup"><span data-stu-id="6a32a-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6a32a-162">著色器模型5元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="6a32a-162">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





