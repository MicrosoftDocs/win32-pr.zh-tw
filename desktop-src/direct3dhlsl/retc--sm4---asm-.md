---
title: 'retc (sm4-asm) '
description: 條件式傳回。
ms.assetid: D936099D-4A75-4AE2-9FE3-70ED213DF4D9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e394bc6b947d91fafb09dbfdc075b0c60be2cf8
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104971593"
---
# <a name="retc-sm4---asm"></a><span data-ttu-id="caf4d-103">retc (sm4-asm) </span><span class="sxs-lookup"><span data-stu-id="caf4d-103">retc (sm4 - asm)</span></span>

<span data-ttu-id="caf4d-104">條件式傳回。</span><span class="sxs-lookup"><span data-stu-id="caf4d-104">Conditional return.</span></span>



| <span data-ttu-id="caf4d-105">retc { \_ z </span><span class="sxs-lookup"><span data-stu-id="caf4d-105">retc{\_z</span></span>\|<span data-ttu-id="caf4d-106">\_nz} src0. 選取 \_ 元件</span><span class="sxs-lookup"><span data-stu-id="caf4d-106">\_nz} src0.select\_component</span></span> |
|----------------------------------------|



 



| <span data-ttu-id="caf4d-107">項目</span><span class="sxs-lookup"><span data-stu-id="caf4d-107">Item</span></span>                                                            | <span data-ttu-id="caf4d-108">描述</span><span class="sxs-lookup"><span data-stu-id="caf4d-108">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="caf4d-109"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="caf4d-109"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="caf4d-110">\[用 \] 來測試條件的註冊。</span><span class="sxs-lookup"><span data-stu-id="caf4d-110">\[in\] The register to test the condition against.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="caf4d-111">備註</span><span class="sxs-lookup"><span data-stu-id="caf4d-111">Remarks</span></span>

<span data-ttu-id="caf4d-112">如果在副程式中，此指令會有條件地傳回呼叫之後的指令。</span><span class="sxs-lookup"><span data-stu-id="caf4d-112">If within a subroutine, this instruction conditionally returns to the instruction after the call.</span></span> <span data-ttu-id="caf4d-113">如果不在副程式內，此指令會終止程式執行。</span><span class="sxs-lookup"><span data-stu-id="caf4d-113">If not inside a subroutine, this instruction terminates program execution.</span></span>

<span data-ttu-id="caf4d-114">下列範例示範如何使用此指令。</span><span class="sxs-lookup"><span data-stu-id="caf4d-114">The following example shows how to use this instruction.</span></span>

``` syntax
           ...
           call l3
           ...
           ret
           label l3
               ...
               retc_nz r0.x  // If any bit in r0.x is nonzero, then return
               retc_z  r1.x  // If all bits in r0.x are zero, then return.
               ...
           ret
```

### <a name="restrictions"></a><span data-ttu-id="caf4d-115">限制</span><span class="sxs-lookup"><span data-stu-id="caf4d-115">Restrictions</span></span>

-   <span data-ttu-id="caf4d-116">**retc** 可以出現在程式中的任何位置，不限次數。</span><span class="sxs-lookup"><span data-stu-id="caf4d-116">**retc** can appear anywhere in a program, any number of times.</span></span>
-   <span data-ttu-id="caf4d-117">Main 程式或副程式中的最後一個指令不能是 **retc \_ z** 或 **retc \_ nz**。</span><span class="sxs-lookup"><span data-stu-id="caf4d-117">The last instruction in a main program or subroutine cannot be a **retc\_z** or **retc\_nz**.</span></span> <span data-ttu-id="caf4d-118">相反地，可以使用無條件的 [ret](ret--sm4---asm-.md) 。</span><span class="sxs-lookup"><span data-stu-id="caf4d-118">Instead, the unconditional [ret](ret--sm4---asm-.md) can be used.</span></span>
-   <span data-ttu-id="caf4d-119">*Src0* 提供的32位暫存器會在位層級進行測試。</span><span class="sxs-lookup"><span data-stu-id="caf4d-119">The 32-bit register supplied by *src0* is tested at a bit level.</span></span> <span data-ttu-id="caf4d-120">如果有任何位為非零值，則會傳回 **ret \_ nz** 。</span><span class="sxs-lookup"><span data-stu-id="caf4d-120">If any bit is nonzero, **ret\_nz** will return.</span></span> <span data-ttu-id="caf4d-121">如果所有位都是零， **retc \_ z** 將會傳回。</span><span class="sxs-lookup"><span data-stu-id="caf4d-121">If all bits are zero, **retc\_z** will return.</span></span>

<span data-ttu-id="caf4d-122">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="caf4d-122">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="caf4d-123">頂點著色器</span><span class="sxs-lookup"><span data-stu-id="caf4d-123">Vertex Shader</span></span> | <span data-ttu-id="caf4d-124">幾何著色器</span><span class="sxs-lookup"><span data-stu-id="caf4d-124">Geometry Shader</span></span> | <span data-ttu-id="caf4d-125">像素著色器</span><span class="sxs-lookup"><span data-stu-id="caf4d-125">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="caf4d-126">x</span><span class="sxs-lookup"><span data-stu-id="caf4d-126">x</span></span>             | <span data-ttu-id="caf4d-127">x</span><span class="sxs-lookup"><span data-stu-id="caf4d-127">x</span></span>               | <span data-ttu-id="caf4d-128">x</span><span class="sxs-lookup"><span data-stu-id="caf4d-128">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="caf4d-129">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="caf4d-129">Minimum Shader Model</span></span>

<span data-ttu-id="caf4d-130">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="caf4d-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="caf4d-131">著色器模型</span><span class="sxs-lookup"><span data-stu-id="caf4d-131">Shader Model</span></span>                                              | <span data-ttu-id="caf4d-132">支援</span><span class="sxs-lookup"><span data-stu-id="caf4d-132">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="caf4d-133">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="caf4d-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="caf4d-134">是</span><span class="sxs-lookup"><span data-stu-id="caf4d-134">yes</span></span>       |
| [<span data-ttu-id="caf4d-135">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="caf4d-135">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="caf4d-136">是</span><span class="sxs-lookup"><span data-stu-id="caf4d-136">yes</span></span>       |
| [<span data-ttu-id="caf4d-137">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="caf4d-137">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="caf4d-138">是</span><span class="sxs-lookup"><span data-stu-id="caf4d-138">yes</span></span>       |
| [<span data-ttu-id="caf4d-139">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="caf4d-139">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="caf4d-140">不可以</span><span class="sxs-lookup"><span data-stu-id="caf4d-140">no</span></span>        |
| [<span data-ttu-id="caf4d-141">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="caf4d-141">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="caf4d-142">不可以</span><span class="sxs-lookup"><span data-stu-id="caf4d-142">no</span></span>        |
| [<span data-ttu-id="caf4d-143">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="caf4d-143">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="caf4d-144">不可以</span><span class="sxs-lookup"><span data-stu-id="caf4d-144">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="caf4d-145">相關主題</span><span class="sxs-lookup"><span data-stu-id="caf4d-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="caf4d-146">著色器模型4元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="caf4d-146">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





