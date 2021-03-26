---
title: '剪下 (sm4-asm) '
description: 幾何著色器指令會完成目前的基本拓撲 (如果已發出) 的任何頂點，並啟動幾何著色器所宣告之類型的新拓撲。
ms.assetid: 9B28E33D-F518-4844-BE3F-BE61B5F08B4F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c462d2f4dc2e0c6b4076f577610c93794e890af
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104971536"
---
# <a name="cut-sm4---asm"></a><span data-ttu-id="21f8e-103">剪下 (sm4-asm) </span><span class="sxs-lookup"><span data-stu-id="21f8e-103">cut (sm4 - asm)</span></span>

<span data-ttu-id="21f8e-104">幾何著色器指令會完成目前的基本拓撲 (如果已發出) 的任何頂點，並啟動幾何著色器所宣告之類型的新拓撲。</span><span class="sxs-lookup"><span data-stu-id="21f8e-104">Geometry Shader instruction that completes the current primitive topology (if any vertices have been emitted), and starts a new topology of the type declared by the Geometry Shader.</span></span>



| <span data-ttu-id="21f8e-105">剪下</span><span class="sxs-lookup"><span data-stu-id="21f8e-105">cut</span></span> |
|-----|



 

## <a name="remarks"></a><span data-ttu-id="21f8e-106">備註</span><span class="sxs-lookup"><span data-stu-id="21f8e-106">Remarks</span></span>

<span data-ttu-id="21f8e-107">當執行 **剪** 下時，第一件事就是已完成幾何著色器調用的任何先前發出的拓撲。</span><span class="sxs-lookup"><span data-stu-id="21f8e-107">When **cut** is executed, the first thing that happens is that any previously emitted topology by the Geometry Shader invocation is completed.</span></span> <span data-ttu-id="21f8e-108">如果未針對先前的基本拓撲發出足夠的頂點，則會捨棄這些頂點。</span><span class="sxs-lookup"><span data-stu-id="21f8e-108">If not enough vertices were emitted for the previous primitive topology, they are discarded.</span></span> <span data-ttu-id="21f8e-109">因為幾何著色器的唯一可用輸出拓撲是 pointlist、linestrip 和 trianglestrip，所以 **剪** 下時永遠不會有任何剩餘的頂點。</span><span class="sxs-lookup"><span data-stu-id="21f8e-109">Because the only available output topologies for the Geometry Shader are pointlist, linestrip, and trianglestrip, there are never any leftover vertices upon **cut**.</span></span>

<span data-ttu-id="21f8e-110">在先前的拓撲（如果有的話）完成之後， **剪** 下會使用宣告為幾何著色器輸出的拓撲來開始新的拓撲。</span><span class="sxs-lookup"><span data-stu-id="21f8e-110">After the previous topology, if any, is completed, **cut** causes a new topology to begin, using the topology declared as the Geometry Shader output.</span></span>

## <a name="restrictions"></a><span data-ttu-id="21f8e-111">限制</span><span class="sxs-lookup"><span data-stu-id="21f8e-111">Restrictions</span></span>

-   <span data-ttu-id="21f8e-112">**剪** 下的指令只適用于幾何著色器。</span><span class="sxs-lookup"><span data-stu-id="21f8e-112">The **cut** instruction applies only to the Geometry Shader.</span></span>
-   <span data-ttu-id="21f8e-113">**剪** 下可以在幾何著色器中出現任何次數，包括 flow 控制項內。</span><span class="sxs-lookup"><span data-stu-id="21f8e-113">**cut** can appear any number of times in the Geometry Shader, including within flow control.</span></span>
-   <span data-ttu-id="21f8e-114">如果幾何著色器結束且頂點已發出，則會完成其所建立的拓撲，就像是執行 **剪** 下做為最後一個指令一樣。</span><span class="sxs-lookup"><span data-stu-id="21f8e-114">If the Geometry Shader ends and vertices have been emitted, the topology they are building is completed, as if a **cut** was executed as the last instruction.</span></span>
-   <span data-ttu-id="21f8e-115">如果已宣告資料流程，就必須使用 [剪下 \_ 資料流程](cut-stream---sm5---asm-.md) ，而不是 **剪** 下。</span><span class="sxs-lookup"><span data-stu-id="21f8e-115">If streams have been declared, then [cut\_stream](cut-stream---sm5---asm-.md) must be used instead of **cut**.</span></span>

<span data-ttu-id="21f8e-116">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="21f8e-116">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="21f8e-117">頂點著色器</span><span class="sxs-lookup"><span data-stu-id="21f8e-117">Vertex Shader</span></span> | <span data-ttu-id="21f8e-118">幾何著色器</span><span class="sxs-lookup"><span data-stu-id="21f8e-118">Geometry Shader</span></span> | <span data-ttu-id="21f8e-119">像素著色器</span><span class="sxs-lookup"><span data-stu-id="21f8e-119">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
|               | <span data-ttu-id="21f8e-120">x</span><span class="sxs-lookup"><span data-stu-id="21f8e-120">x</span></span>               |              |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="21f8e-121">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="21f8e-121">Minimum Shader Model</span></span>

<span data-ttu-id="21f8e-122">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="21f8e-122">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="21f8e-123">著色器模型</span><span class="sxs-lookup"><span data-stu-id="21f8e-123">Shader Model</span></span>                                              | <span data-ttu-id="21f8e-124">支援</span><span class="sxs-lookup"><span data-stu-id="21f8e-124">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="21f8e-125">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="21f8e-125">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="21f8e-126">是</span><span class="sxs-lookup"><span data-stu-id="21f8e-126">yes</span></span>       |
| [<span data-ttu-id="21f8e-127">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="21f8e-127">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="21f8e-128">是</span><span class="sxs-lookup"><span data-stu-id="21f8e-128">yes</span></span>       |
| [<span data-ttu-id="21f8e-129">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="21f8e-129">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="21f8e-130">是</span><span class="sxs-lookup"><span data-stu-id="21f8e-130">yes</span></span>       |
| [<span data-ttu-id="21f8e-131">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="21f8e-131">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="21f8e-132">不可以</span><span class="sxs-lookup"><span data-stu-id="21f8e-132">no</span></span>        |
| [<span data-ttu-id="21f8e-133">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="21f8e-133">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="21f8e-134">不可以</span><span class="sxs-lookup"><span data-stu-id="21f8e-134">no</span></span>        |
| [<span data-ttu-id="21f8e-135">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="21f8e-135">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="21f8e-136">不可以</span><span class="sxs-lookup"><span data-stu-id="21f8e-136">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="21f8e-137">相關主題</span><span class="sxs-lookup"><span data-stu-id="21f8e-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="21f8e-138">著色器模型4元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="21f8e-138">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




