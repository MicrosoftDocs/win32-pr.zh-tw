---
title: '切換 (sm4-asm) '
description: 將控制權傳輸至切換主體內的不同語句區塊，取決於選取器的值。
ms.assetid: ECAEECFD-B955-4356-B5C9-1D6A04C71D8F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: feed346b8aa33feecc13fe2a6ffad59c961b0173
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104022822"
---
# <a name="switch-sm4---asm"></a><span data-ttu-id="bbc27-103">切換 (sm4-asm) </span><span class="sxs-lookup"><span data-stu-id="bbc27-103">switch (sm4 - asm)</span></span>

<span data-ttu-id="bbc27-104">將控制權傳輸至切換主體內的不同語句區塊，取決於選取器的值。</span><span class="sxs-lookup"><span data-stu-id="bbc27-104">Transfers control to a different statement block within the switch body depending on the value of a selector.</span></span>



| <span data-ttu-id="bbc27-105">切換 src0 選取的 \_ 元件</span><span class="sxs-lookup"><span data-stu-id="bbc27-105">switch src0.selected\_component</span></span> |
|---------------------------------|



 



| <span data-ttu-id="bbc27-106">項目</span><span class="sxs-lookup"><span data-stu-id="bbc27-106">Item</span></span>                                                            | <span data-ttu-id="bbc27-107">描述</span><span class="sxs-lookup"><span data-stu-id="bbc27-107">Description</span></span>                                              |
|-----------------------------------------------------------------|----------------------------------------------------------|
| <span data-ttu-id="bbc27-108"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="bbc27-108"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="bbc27-109">\[在 \] switch 語句的選取器中。</span><span class="sxs-lookup"><span data-stu-id="bbc27-109">\[in\] The selector for the switch statement.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="bbc27-110">備註</span><span class="sxs-lookup"><span data-stu-id="bbc27-110">Remarks</span></span>

<span data-ttu-id="bbc27-111">**Switch** / [endswitch](endswitch--sm4---asm-.md)結構的運作方式與 C 語言中的 **switch** 結構完全相同，但有下列例外狀況：若為 D3D11 [案例](case--sm4---asm-.md) / ，而不使用 break 的 [預設](default--sm4---asm-.md)語句，則 / 不能有任何程式碼。 [](break--sm4---asm-.md)</span><span class="sxs-lookup"><span data-stu-id="bbc27-111">A **switch**/[endswitch](endswitch--sm4---asm-.md) construct behaves exactly as a **switch** construct in the C language, with the following exception: for D3D11 [case](case--sm4---asm-.md)/[default](default--sm4---asm-.md) statements that fall through to the next **case**/**default** without a [break](break--sm4---asm-.md) cannot have any code in them.</span></span> <span data-ttu-id="bbc27-112">允許多個 **case** 語句（包括 **預設值**）依序出現，並共用相同的程式碼區塊。</span><span class="sxs-lookup"><span data-stu-id="bbc27-112">It is permitted for multiple **case** statements, including **default**, to appear sequentially, sharing the same code block.</span></span>

<span data-ttu-id="bbc27-113">條件必須是32位的註冊元件或立即數量。</span><span class="sxs-lookup"><span data-stu-id="bbc27-113">The condition must be a 32-bit register component or immediate quantity.</span></span> <span data-ttu-id="bbc27-114">相等比較是位 (整數) 。</span><span class="sxs-lookup"><span data-stu-id="bbc27-114">The equality comparison is bitwise (integer).</span></span>

<span data-ttu-id="bbc27-115">如同 D3D11 中的任何著色器指令，硬體可能會或可能不會直接執行 **switch** 結構。</span><span class="sxs-lookup"><span data-stu-id="bbc27-115">As with any Shader instruction in the D3D11, hardware may or may not implement the **switch** construct directly.</span></span>

<span data-ttu-id="bbc27-116">**Switch** 語句可以嵌套。</span><span class="sxs-lookup"><span data-stu-id="bbc27-116">**Switch** statements can be nested.</span></span> <span data-ttu-id="bbc27-117">每個 **switch** 區塊都會針對每個副程式和 main 的流程式控制制對應深度64限制為1個層級，而不受 **case** 語句的數目影響。</span><span class="sxs-lookup"><span data-stu-id="bbc27-117">Each **switch** block counts as 1 level against the flow control nesting depth limit of 64 per subroutine and main, independent of the number of **case** statements.</span></span> <span data-ttu-id="bbc27-118">HLSL 編譯器將不會產生超過此限制的副程式。</span><span class="sxs-lookup"><span data-stu-id="bbc27-118">The HLSL compiler will not generate subroutines that exceed this limit.</span></span> <span data-ttu-id="bbc27-119">除了64層級之外，每個副程式的控制流程指令行為未定義。</span><span class="sxs-lookup"><span data-stu-id="bbc27-119">Behavior of control flow instructions beyond 64 levels deep per subroutine is undefined.</span></span>

<span data-ttu-id="bbc27-120">下列範例示範如何使用此指令。</span><span class="sxs-lookup"><span data-stu-id="bbc27-120">The following example shows how to use this instruction.</span></span>

``` syntax
                ...
                switch r0.x
                default: // falling through
                case 3
                    switch r1.x
                    case 4
                        ...
                        break
                    case 5
                        ...
                        break
                    endswitch
                    break
                case 0
                    break
                endswitch
```

<span data-ttu-id="bbc27-121">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="bbc27-121">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="bbc27-122">頂點著色器</span><span class="sxs-lookup"><span data-stu-id="bbc27-122">Vertex Shader</span></span> | <span data-ttu-id="bbc27-123">幾何著色器</span><span class="sxs-lookup"><span data-stu-id="bbc27-123">Geometry Shader</span></span> | <span data-ttu-id="bbc27-124">像素著色器</span><span class="sxs-lookup"><span data-stu-id="bbc27-124">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="bbc27-125">x</span><span class="sxs-lookup"><span data-stu-id="bbc27-125">x</span></span>             | <span data-ttu-id="bbc27-126">x</span><span class="sxs-lookup"><span data-stu-id="bbc27-126">x</span></span>               | <span data-ttu-id="bbc27-127">x</span><span class="sxs-lookup"><span data-stu-id="bbc27-127">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="bbc27-128">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="bbc27-128">Minimum Shader Model</span></span>

<span data-ttu-id="bbc27-129">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="bbc27-129">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="bbc27-130">著色器模型</span><span class="sxs-lookup"><span data-stu-id="bbc27-130">Shader Model</span></span>                                              | <span data-ttu-id="bbc27-131">支援</span><span class="sxs-lookup"><span data-stu-id="bbc27-131">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="bbc27-132">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="bbc27-132">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="bbc27-133">是</span><span class="sxs-lookup"><span data-stu-id="bbc27-133">yes</span></span>       |
| [<span data-ttu-id="bbc27-134">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="bbc27-134">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="bbc27-135">是</span><span class="sxs-lookup"><span data-stu-id="bbc27-135">yes</span></span>       |
| [<span data-ttu-id="bbc27-136">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="bbc27-136">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="bbc27-137">是</span><span class="sxs-lookup"><span data-stu-id="bbc27-137">yes</span></span>       |
| [<span data-ttu-id="bbc27-138">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="bbc27-138">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="bbc27-139">不可以</span><span class="sxs-lookup"><span data-stu-id="bbc27-139">no</span></span>        |
| [<span data-ttu-id="bbc27-140">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="bbc27-140">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="bbc27-141">不可以</span><span class="sxs-lookup"><span data-stu-id="bbc27-141">no</span></span>        |
| [<span data-ttu-id="bbc27-142">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="bbc27-142">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="bbc27-143">不可以</span><span class="sxs-lookup"><span data-stu-id="bbc27-143">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="bbc27-144">相關主題</span><span class="sxs-lookup"><span data-stu-id="bbc27-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bbc27-145">著色器模型4元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="bbc27-145">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





