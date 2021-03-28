---
title: '如果 (sm4-asm) '
description: 以邏輯 OR 結果為基礎的分支。
ms.assetid: 9F4CF9E0-4D9D-4300-B432-432C560F34BB
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 653c84be0d30a036bf93d852268e44bcca08bbcb
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104990706"
---
# <a name="if-sm4---asm"></a><span data-ttu-id="9008f-103">如果 (sm4-asm) </span><span class="sxs-lookup"><span data-stu-id="9008f-103">if (sm4 - asm)</span></span>

<span data-ttu-id="9008f-104">以邏輯 OR 結果為基礎的分支。</span><span class="sxs-lookup"><span data-stu-id="9008f-104">Branch based on logical OR result.</span></span>



| <span data-ttu-id="9008f-105">if { \_ z </span><span class="sxs-lookup"><span data-stu-id="9008f-105">if{\_z</span></span>\|<span data-ttu-id="9008f-106">\_nz} src0. 選取 \_ 元件</span><span class="sxs-lookup"><span data-stu-id="9008f-106">\_nz} src0.select\_component</span></span> |
|--------------------------------------|



 



| <span data-ttu-id="9008f-107">項目</span><span class="sxs-lookup"><span data-stu-id="9008f-107">Item</span></span>                                                            | <span data-ttu-id="9008f-108">描述</span><span class="sxs-lookup"><span data-stu-id="9008f-108">Description</span></span>                                                              |
|-----------------------------------------------------------------|--------------------------------------------------------------------------|
| <span data-ttu-id="9008f-109"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="9008f-109"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="9008f-110">\[中的 \] 包含要測試條件的元件。</span><span class="sxs-lookup"><span data-stu-id="9008f-110">\[in\] Contains the component on which to test the condition.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="9008f-111">備註</span><span class="sxs-lookup"><span data-stu-id="9008f-111">Remarks</span></span>

<span data-ttu-id="9008f-112">Token 格式會在著色器中包含對應的 endif 指令位移，以方便使用。</span><span class="sxs-lookup"><span data-stu-id="9008f-112">The token format contains the offset of the corresponding endif instruction in the Shader as a convenience.</span></span>

<span data-ttu-id="9008f-113">下列範例示範如何使用此指令。</span><span class="sxs-lookup"><span data-stu-id="9008f-113">The following example shows how to use this instruction.</span></span>

``` syntax
                if_z r0.x // if all bits in r0.x are zero
                   ...
                else // (optional)
                   ...
                endif
                if_nz r1.x // if any bit in r0.x is nonzero
                   ...
                else // (optional)
                   ...
                endif
```

### <a name="restrictions"></a><span data-ttu-id="9008f-114">限制</span><span class="sxs-lookup"><span data-stu-id="9008f-114">Restrictions</span></span>

-   <span data-ttu-id="9008f-115">如果4個元件向量) 必須使用單一元件選取器，則來源運算元 (。</span><span class="sxs-lookup"><span data-stu-id="9008f-115">The source operands (if 4 component vectors) must use a single component selector.</span></span>
-   <span data-ttu-id="9008f-116">*Src0* 提供的32位暫存器會在位層級進行測試。</span><span class="sxs-lookup"><span data-stu-id="9008f-116">The 32-bit register supplied by *src0* is tested at a bit level.</span></span> <span data-ttu-id="9008f-117">如果有任何位為非零值，則 **\_ z** 為 true。</span><span class="sxs-lookup"><span data-stu-id="9008f-117">If any bit is nonzero, **if\_z** will be true.</span></span> <span data-ttu-id="9008f-118">如果所有位為零， **則為，如果 \_ nz** 為 true。</span><span class="sxs-lookup"><span data-stu-id="9008f-118">If all bits are zero, **if\_nz** will be true.</span></span>
-   <span data-ttu-id="9008f-119">在每個副程式 (和主要) 的流程式控制制區塊最多可有64個深度。</span><span class="sxs-lookup"><span data-stu-id="9008f-119">Flow control blocks can nest up to 64 deep per subroutine (and main).</span></span> <span data-ttu-id="9008f-120">HLSL 編譯器將不會產生超過此限制的副程式。</span><span class="sxs-lookup"><span data-stu-id="9008f-120">The HLSL compiler will not generate subroutines that exceed this limit.</span></span> <span data-ttu-id="9008f-121">除了64層級外的控制流程指令行為之外，每個副程式的 (深度) 未定義。</span><span class="sxs-lookup"><span data-stu-id="9008f-121">Behavior of control flow instructions beyond 64 levels deep (per subroutine) is undefined.</span></span>

<span data-ttu-id="9008f-122">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="9008f-122">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="9008f-123">頂點著色器</span><span class="sxs-lookup"><span data-stu-id="9008f-123">Vertex Shader</span></span> | <span data-ttu-id="9008f-124">幾何著色器</span><span class="sxs-lookup"><span data-stu-id="9008f-124">Geometry Shader</span></span> | <span data-ttu-id="9008f-125">像素著色器</span><span class="sxs-lookup"><span data-stu-id="9008f-125">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="9008f-126">x</span><span class="sxs-lookup"><span data-stu-id="9008f-126">x</span></span>             | <span data-ttu-id="9008f-127">x</span><span class="sxs-lookup"><span data-stu-id="9008f-127">x</span></span>               | <span data-ttu-id="9008f-128">x</span><span class="sxs-lookup"><span data-stu-id="9008f-128">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="9008f-129">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="9008f-129">Minimum Shader Model</span></span>

<span data-ttu-id="9008f-130">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="9008f-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="9008f-131">著色器模型</span><span class="sxs-lookup"><span data-stu-id="9008f-131">Shader Model</span></span>                                              | <span data-ttu-id="9008f-132">支援</span><span class="sxs-lookup"><span data-stu-id="9008f-132">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="9008f-133">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="9008f-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="9008f-134">是</span><span class="sxs-lookup"><span data-stu-id="9008f-134">yes</span></span>       |
| [<span data-ttu-id="9008f-135">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="9008f-135">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="9008f-136">是</span><span class="sxs-lookup"><span data-stu-id="9008f-136">yes</span></span>       |
| [<span data-ttu-id="9008f-137">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="9008f-137">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="9008f-138">是</span><span class="sxs-lookup"><span data-stu-id="9008f-138">yes</span></span>       |
| [<span data-ttu-id="9008f-139">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="9008f-139">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="9008f-140">不可以</span><span class="sxs-lookup"><span data-stu-id="9008f-140">no</span></span>        |
| [<span data-ttu-id="9008f-141">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="9008f-141">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="9008f-142">不可以</span><span class="sxs-lookup"><span data-stu-id="9008f-142">no</span></span>        |
| [<span data-ttu-id="9008f-143">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="9008f-143">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="9008f-144">不可以</span><span class="sxs-lookup"><span data-stu-id="9008f-144">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="9008f-145">相關主題</span><span class="sxs-lookup"><span data-stu-id="9008f-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9008f-146">著色器模型4元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="9008f-146">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





