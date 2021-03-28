---
title: 'loop (sm4-asm) '
description: 指定迴圈，直到遇到 break 指令為止。
ms.assetid: 0BEFADF4-036E-4FDA-9681-10965D6BA9FC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 243bdf3b370d3505d787451162c22340acef3a45
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104990775"
---
# <a name="loop-sm4---asm"></a><span data-ttu-id="9181a-103">loop (sm4-asm) </span><span class="sxs-lookup"><span data-stu-id="9181a-103">loop (sm4 - asm)</span></span>

<span data-ttu-id="9181a-104">指定迴圈，直到遇到 break 指令為止。</span><span class="sxs-lookup"><span data-stu-id="9181a-104">Specifies a loop which iterates until a break instruction is encountered.</span></span>



| <span data-ttu-id="9181a-105">loop</span><span class="sxs-lookup"><span data-stu-id="9181a-105">loop</span></span> |
|------|



 

## <a name="remarks"></a><span data-ttu-id="9181a-106">備註</span><span class="sxs-lookup"><span data-stu-id="9181a-106">Remarks</span></span>

<span data-ttu-id="9181a-107">**迴圈** 可以無限期地逐一查看，不過在執行一些指令之後，可能會強制將著色器的整體執行終止。</span><span class="sxs-lookup"><span data-stu-id="9181a-107">**loop** can iterate indefinitely, although overall execution of the Shader may be forced to terminate after some number of instructions are executed.</span></span>

<span data-ttu-id="9181a-108">流程式控制制區塊最多可在每個副程式和主要的64個深度上進行。</span><span class="sxs-lookup"><span data-stu-id="9181a-108">Flow control blocks can nest up to 64 deep per subroutine and main.</span></span> <span data-ttu-id="9181a-109">HLSL 編譯器將不會產生超過此限制的副程式。</span><span class="sxs-lookup"><span data-stu-id="9181a-109">The HLSL compiler will not generate subroutines that exceed this limit.</span></span> <span data-ttu-id="9181a-110">除了64層級之外，每個副程式的控制流程指令行為未定義。</span><span class="sxs-lookup"><span data-stu-id="9181a-110">Behavior of control flow instructions beyond 64 levels deep per subroutine is undefined.</span></span>

<span data-ttu-id="9181a-111">標記格式包含著色器中對應 [endloop](endloop--sm4---asm-.md) 指令的位移，以方便使用。</span><span class="sxs-lookup"><span data-stu-id="9181a-111">The token format contains the offset of the corresponding [endloop](endloop--sm4---asm-.md) instruction in the Shader as a convenience.</span></span>

<span data-ttu-id="9181a-112">下列範例顯示如何使用迴圈指令。</span><span class="sxs-lookup"><span data-stu-id="9181a-112">The following example shows how to use the loop instruction.</span></span>

``` syntax
                loop
                    // example of termination condition
                    if_nz r0.x
                        break
                    endif
                    ...
                endloop
```

<span data-ttu-id="9181a-113">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="9181a-113">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="9181a-114">頂點著色器</span><span class="sxs-lookup"><span data-stu-id="9181a-114">Vertex Shader</span></span> | <span data-ttu-id="9181a-115">幾何著色器</span><span class="sxs-lookup"><span data-stu-id="9181a-115">Geometry Shader</span></span> | <span data-ttu-id="9181a-116">像素著色器</span><span class="sxs-lookup"><span data-stu-id="9181a-116">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="9181a-117">x</span><span class="sxs-lookup"><span data-stu-id="9181a-117">x</span></span>             | <span data-ttu-id="9181a-118">x</span><span class="sxs-lookup"><span data-stu-id="9181a-118">x</span></span>               | <span data-ttu-id="9181a-119">x</span><span class="sxs-lookup"><span data-stu-id="9181a-119">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="9181a-120">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="9181a-120">Minimum Shader Model</span></span>

<span data-ttu-id="9181a-121">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="9181a-121">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="9181a-122">著色器模型</span><span class="sxs-lookup"><span data-stu-id="9181a-122">Shader Model</span></span>                                              | <span data-ttu-id="9181a-123">支援</span><span class="sxs-lookup"><span data-stu-id="9181a-123">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="9181a-124">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="9181a-124">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="9181a-125">是</span><span class="sxs-lookup"><span data-stu-id="9181a-125">yes</span></span>       |
| [<span data-ttu-id="9181a-126">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="9181a-126">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="9181a-127">是</span><span class="sxs-lookup"><span data-stu-id="9181a-127">yes</span></span>       |
| [<span data-ttu-id="9181a-128">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="9181a-128">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="9181a-129">是</span><span class="sxs-lookup"><span data-stu-id="9181a-129">yes</span></span>       |
| [<span data-ttu-id="9181a-130">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="9181a-130">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="9181a-131">不可以</span><span class="sxs-lookup"><span data-stu-id="9181a-131">no</span></span>        |
| [<span data-ttu-id="9181a-132">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="9181a-132">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="9181a-133">不可以</span><span class="sxs-lookup"><span data-stu-id="9181a-133">no</span></span>        |
| [<span data-ttu-id="9181a-134">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="9181a-134">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="9181a-135">不可以</span><span class="sxs-lookup"><span data-stu-id="9181a-135">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="9181a-136">相關主題</span><span class="sxs-lookup"><span data-stu-id="9181a-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9181a-137">著色器模型4元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="9181a-137">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




