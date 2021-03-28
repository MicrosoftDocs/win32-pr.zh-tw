---
title: 'breakc (sm4-asm) '
description: 有條件地將執行點移到下一個 endloop 或 endswitch 之後的指令。
ms.assetid: 5735EF88-1E8C-4142-8442-9328D78999A7
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 019a1c859f7d1e0ee6368f5b9984775ef9bfaba1
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104373819"
---
# <a name="breakc-sm4---asm"></a><span data-ttu-id="9b563-103">breakc (sm4-asm) </span><span class="sxs-lookup"><span data-stu-id="9b563-103">breakc (sm4 - asm)</span></span>

<span data-ttu-id="9b563-104">有條件地將執行點移到下一個 [endloop](endloop--sm4---asm-.md) 或 [endswitch](endswitch--sm4---asm-.md)之後的指令。</span><span class="sxs-lookup"><span data-stu-id="9b563-104">Conditionally moves the point of execution to the instruction after the next [endloop](endloop--sm4---asm-.md) or [endswitch](endswitch--sm4---asm-.md).</span></span>



| <span data-ttu-id="9b563-105">breakc { \_ z </span><span class="sxs-lookup"><span data-stu-id="9b563-105">breakc{\_z</span></span>\|<span data-ttu-id="9b563-106">\_nz} src0. 選取 \_ 元件</span><span class="sxs-lookup"><span data-stu-id="9b563-106">\_nz} src0.select\_component</span></span> |
|------------------------------------------|



 



| <span data-ttu-id="9b563-107">項目</span><span class="sxs-lookup"><span data-stu-id="9b563-107">Item</span></span>                                                            | <span data-ttu-id="9b563-108">描述</span><span class="sxs-lookup"><span data-stu-id="9b563-108">Description</span></span>                                                     |
|-----------------------------------------------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="9b563-109"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="9b563-109"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="9b563-110">\[在 \] 測試條件的元件中。</span><span class="sxs-lookup"><span data-stu-id="9b563-110">\[in\] The component on which to test the condition.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="9b563-111">備註</span><span class="sxs-lookup"><span data-stu-id="9b563-111">Remarks</span></span>

<span data-ttu-id="9b563-112">標記格式包含著色器中對應 **endloop** 指令的位移，以方便使用。</span><span class="sxs-lookup"><span data-stu-id="9b563-112">The token format contains the offset of the corresponding **endloop** instruction in the Shader as a convenience.</span></span>

<span data-ttu-id="9b563-113">下列範例顯示 **breakc** 指令。</span><span class="sxs-lookup"><span data-stu-id="9b563-113">The following example shows the **breakc** instruction.</span></span>


```
                loop
                    // example of termination condition
                    breakc_z  r0.x // break if all bits in r0.x are 0
                    breakc_nz r1.x // break if any bit in r1.x is nonzero
                    ...
                endloop

```



<span data-ttu-id="9b563-114">這個指令必須出現在 **迴圈** / **endloop** 或 **switch** / **endswitch** 內。</span><span class="sxs-lookup"><span data-stu-id="9b563-114">This instruction must appear within a **loop**/**endloop** or **switch**/**endswitch**.</span></span>

<span data-ttu-id="9b563-115">*Src0* 提供的32位暫存器會在位層級進行測試。</span><span class="sxs-lookup"><span data-stu-id="9b563-115">The 32-bit register supplied by *src0* is tested at a bit level.</span></span> <span data-ttu-id="9b563-116">如果有任何位為非零值， **breakc \_ nz** 將會執行中斷。</span><span class="sxs-lookup"><span data-stu-id="9b563-116">If any bit is nonzero, **breakc\_nz** will perform the break.</span></span> <span data-ttu-id="9b563-117">如果所有位都是零， **breakc \_ z** 將會執行中斷。</span><span class="sxs-lookup"><span data-stu-id="9b563-117">If all bits are zero, **breakc\_z** will perform the break.</span></span>

<span data-ttu-id="9b563-118">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="9b563-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="9b563-119">頂點著色器</span><span class="sxs-lookup"><span data-stu-id="9b563-119">Vertex Shader</span></span> | <span data-ttu-id="9b563-120">幾何著色器</span><span class="sxs-lookup"><span data-stu-id="9b563-120">Geometry Shader</span></span> | <span data-ttu-id="9b563-121">像素著色器</span><span class="sxs-lookup"><span data-stu-id="9b563-121">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="9b563-122">x</span><span class="sxs-lookup"><span data-stu-id="9b563-122">x</span></span>             | <span data-ttu-id="9b563-123">x</span><span class="sxs-lookup"><span data-stu-id="9b563-123">x</span></span>               | <span data-ttu-id="9b563-124">x</span><span class="sxs-lookup"><span data-stu-id="9b563-124">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="9b563-125">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="9b563-125">Minimum Shader Model</span></span>

<span data-ttu-id="9b563-126">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="9b563-126">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="9b563-127">著色器模型</span><span class="sxs-lookup"><span data-stu-id="9b563-127">Shader Model</span></span>                                              | <span data-ttu-id="9b563-128">支援</span><span class="sxs-lookup"><span data-stu-id="9b563-128">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="9b563-129">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="9b563-129">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="9b563-130">是</span><span class="sxs-lookup"><span data-stu-id="9b563-130">yes</span></span>       |
| [<span data-ttu-id="9b563-131">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="9b563-131">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="9b563-132">是</span><span class="sxs-lookup"><span data-stu-id="9b563-132">yes</span></span>       |
| [<span data-ttu-id="9b563-133">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="9b563-133">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="9b563-134">是</span><span class="sxs-lookup"><span data-stu-id="9b563-134">yes</span></span>       |
| [<span data-ttu-id="9b563-135">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="9b563-135">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="9b563-136">不可以</span><span class="sxs-lookup"><span data-stu-id="9b563-136">no</span></span>        |
| [<span data-ttu-id="9b563-137">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="9b563-137">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="9b563-138">不可以</span><span class="sxs-lookup"><span data-stu-id="9b563-138">no</span></span>        |
| [<span data-ttu-id="9b563-139">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="9b563-139">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="9b563-140">不可以</span><span class="sxs-lookup"><span data-stu-id="9b563-140">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="9b563-141">相關主題</span><span class="sxs-lookup"><span data-stu-id="9b563-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9b563-142">著色器模型4元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="9b563-142">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





