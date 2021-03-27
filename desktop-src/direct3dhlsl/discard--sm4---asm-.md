---
title: '捨棄 (sm4-asm) '
description: 有條件地標示圖元著色器的結果，以在到達程式結束時捨棄。
ms.assetid: 566C4A9A-B32A-4AA6-A888-70F6965B1B5A
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57d98365ae6d80710f15cf7204f98d810be30a13
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "103932813"
---
# <a name="discard-sm4---asm"></a><span data-ttu-id="6feec-103">捨棄 (sm4-asm) </span><span class="sxs-lookup"><span data-stu-id="6feec-103">discard (sm4 - asm)</span></span>

<span data-ttu-id="6feec-104">有條件地標示圖元著色器的結果，以在到達程式結束時捨棄。</span><span class="sxs-lookup"><span data-stu-id="6feec-104">Conditionally flag results of Pixel Shader to be discarded when the end of the program is reached.</span></span>



| <span data-ttu-id="6feec-105">捨棄 { \_ z </span><span class="sxs-lookup"><span data-stu-id="6feec-105">discard{\_z</span></span>\|<span data-ttu-id="6feec-106">\_nz} src0. 選取 \_ 元件</span><span class="sxs-lookup"><span data-stu-id="6feec-106">\_nz} src0.select\_component</span></span> |
|-------------------------------------------|



 



| <span data-ttu-id="6feec-107">項目</span><span class="sxs-lookup"><span data-stu-id="6feec-107">Item</span></span>                                                            | <span data-ttu-id="6feec-108">描述</span><span class="sxs-lookup"><span data-stu-id="6feec-108">Description</span></span>                                                                                       |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6feec-109"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="6feec-109"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="6feec-110">\[\]值，這個值會決定是否要捨棄目前正在處理的圖元。</span><span class="sxs-lookup"><span data-stu-id="6feec-110">\[in\] The value that determines whether to discard the current pixel being processed.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6feec-111">備註</span><span class="sxs-lookup"><span data-stu-id="6feec-111">Remarks</span></span>

<span data-ttu-id="6feec-112">此指令會將目前的圖元標示為已終止，並繼續執行，如此一來，平行執行的其他圖元可能會在必要時取得衍生。</span><span class="sxs-lookup"><span data-stu-id="6feec-112">This instruction flags the current pixel as terminated, while continuing execution, so that other pixels executing in parallel may obtain derivatives if necessary.</span></span> <span data-ttu-id="6feec-113">雖然繼續執行， **但在捨棄指令之前** 或之後的所有圖元著色器輸出寫入都會被捨棄。</span><span class="sxs-lookup"><span data-stu-id="6feec-113">Even though execution continues, all Pixel Shader output writes before or after the **discard** instruction are discarded.</span></span>

<span data-ttu-id="6feec-114">若為 **捨棄 \_ z**，如果 src0 中的所有位， *select \_ 元件* 為零，則會捨棄圖元。</span><span class="sxs-lookup"><span data-stu-id="6feec-114">For **discard\_z**, if all bits in *src0.select\_component* are zero, then the pixel is discarded.</span></span>

<span data-ttu-id="6feec-115">若為 **捨棄 \_ nz**，src0 中的任何位 *。 \_ select 元件* 為非零值，則會捨棄圖元。</span><span class="sxs-lookup"><span data-stu-id="6feec-115">For **discard\_nz**, if any bits in *src0.select\_component* are nonzero, then the pixel is discarded.</span></span>

<span data-ttu-id="6feec-116">此外， **捨棄** 指令可以存在於任何流程式控制制結構內。</span><span class="sxs-lookup"><span data-stu-id="6feec-116">In addition, the **discard** instruction can be present inside any flow control construct.</span></span>

<span data-ttu-id="6feec-117">著色器中可能會有多個 **捨棄** 指令，而且如果有任何執行的，則會結束圖元。</span><span class="sxs-lookup"><span data-stu-id="6feec-117">Multiple **discard** instructions may be present in a Shader, and if any is executed, the pixel is terminated.</span></span>

<span data-ttu-id="6feec-118">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="6feec-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="6feec-119">頂點著色器</span><span class="sxs-lookup"><span data-stu-id="6feec-119">Vertex Shader</span></span> | <span data-ttu-id="6feec-120">幾何著色器</span><span class="sxs-lookup"><span data-stu-id="6feec-120">Geometry Shader</span></span> | <span data-ttu-id="6feec-121">像素著色器</span><span class="sxs-lookup"><span data-stu-id="6feec-121">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
|               |                 | <span data-ttu-id="6feec-122">x</span><span class="sxs-lookup"><span data-stu-id="6feec-122">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="6feec-123">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="6feec-123">Minimum Shader Model</span></span>

<span data-ttu-id="6feec-124">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="6feec-124">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="6feec-125">著色器模型</span><span class="sxs-lookup"><span data-stu-id="6feec-125">Shader Model</span></span>                                              | <span data-ttu-id="6feec-126">支援</span><span class="sxs-lookup"><span data-stu-id="6feec-126">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="6feec-127">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="6feec-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="6feec-128">是</span><span class="sxs-lookup"><span data-stu-id="6feec-128">yes</span></span>       |
| [<span data-ttu-id="6feec-129">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="6feec-129">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="6feec-130">是</span><span class="sxs-lookup"><span data-stu-id="6feec-130">yes</span></span>       |
| [<span data-ttu-id="6feec-131">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="6feec-131">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="6feec-132">是</span><span class="sxs-lookup"><span data-stu-id="6feec-132">yes</span></span>       |
| [<span data-ttu-id="6feec-133">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="6feec-133">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="6feec-134">不可以</span><span class="sxs-lookup"><span data-stu-id="6feec-134">no</span></span>        |
| [<span data-ttu-id="6feec-135">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="6feec-135">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="6feec-136">不可以</span><span class="sxs-lookup"><span data-stu-id="6feec-136">no</span></span>        |
| [<span data-ttu-id="6feec-137">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="6feec-137">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="6feec-138">不可以</span><span class="sxs-lookup"><span data-stu-id="6feec-138">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="6feec-139">相關主題</span><span class="sxs-lookup"><span data-stu-id="6feec-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6feec-140">著色器模型4元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="6feec-140">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





