---
title: 精確
description: 依指令停用算術重構。
ms.assetid: A26E569A-32EA-4AED-83C2-4F937AD3829E
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 03f288fb5dafee0e29c8c11cab72156f7ad3d569
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104507708"
---
# <a name="precise"></a><span data-ttu-id="cbc3d-103">精確</span><span class="sxs-lookup"><span data-stu-id="cbc3d-103">Precise</span></span>

<span data-ttu-id="cbc3d-104">依指令停用算術重構。</span><span class="sxs-lookup"><span data-stu-id="cbc3d-104">Per-instruction disabling of arithmetic refactoring.</span></span>



| <span data-ttu-id="cbc3d-105">精確 (元件遮罩) </span><span class="sxs-lookup"><span data-stu-id="cbc3d-105">precise (component mask)</span></span> |
|--------------------------|



 

<span data-ttu-id="cbc3d-106">此修飾詞需要全域著色器旗標「允許重構」 \_ 。</span><span class="sxs-lookup"><span data-stu-id="cbc3d-106">This modifier requires the global shader flag "REFACTORING\_ALLOWED".</span></span> <span data-ttu-id="cbc3d-107">當 \_ 有允許重構時，個別指令的個別元件結果可能會被強制由編譯器或驅動程式保持精確或不 refactorable。</span><span class="sxs-lookup"><span data-stu-id="cbc3d-107">When REFACTORING\_ALLOWED is present, individual component results of individual instructions can be forced to remain precise or not-refactorable by compilers or drivers.</span></span> <span data-ttu-id="cbc3d-108">如果將 [**mad**](mad--sm4---asm-.md) 指令的元件標記為 **精確**，則硬體必須執行 **mad** 指令或完全相同的對等指令，而且無法將它分割成乘上的乘號。</span><span class="sxs-lookup"><span data-stu-id="cbc3d-108">If components of a [**mad**](mad--sm4---asm-.md) instruction are tagged as **precise**, the hardware must execute a **mad** instruction or the exact equivalent, and it cannot split it into a multiply followed by an add.</span></span> <span data-ttu-id="cbc3d-109">相反地，後面接著一個加上的乘法，其中任一或兩者都會標示為 **精確**，因此無法合併到融合的 **mad** 中。</span><span class="sxs-lookup"><span data-stu-id="cbc3d-109">Conversely, a multiply followed by an add, where either or both are flagged as **precise**, cannot be merged into a fused **mad**.</span></span>

<span data-ttu-id="cbc3d-110">如果尚未 \_ 指定允許的重構，則不允許 **精確** 的修飾詞。</span><span class="sxs-lookup"><span data-stu-id="cbc3d-110">If REFACTORING\_ALLOWED has not been specified, the **precise** modifier is not allowed.</span></span> <span data-ttu-id="cbc3d-111">這是不需要的，因為所有專案都是精確的。</span><span class="sxs-lookup"><span data-stu-id="cbc3d-111">It is not needed because everything is precise.</span></span> <span data-ttu-id="cbc3d-112">**精確** 修飾詞會影響任何運算，而不只是算術。</span><span class="sxs-lookup"><span data-stu-id="cbc3d-112">The **precise** modifier affects any operation, not just arithmetic.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="cbc3d-113">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="cbc3d-113">Minimum Shader Model</span></span>

<span data-ttu-id="cbc3d-114">下列著色器模型支援此修飾詞。</span><span class="sxs-lookup"><span data-stu-id="cbc3d-114">This modifier is supported in the following shader models.</span></span>



| <span data-ttu-id="cbc3d-115">著色器模型</span><span class="sxs-lookup"><span data-stu-id="cbc3d-115">Shader Model</span></span>                                              | <span data-ttu-id="cbc3d-116">支援</span><span class="sxs-lookup"><span data-stu-id="cbc3d-116">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="cbc3d-117">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="cbc3d-117">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="cbc3d-118">是</span><span class="sxs-lookup"><span data-stu-id="cbc3d-118">yes</span></span>       |
| [<span data-ttu-id="cbc3d-119">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="cbc3d-119">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="cbc3d-120">不可以</span><span class="sxs-lookup"><span data-stu-id="cbc3d-120">no</span></span>        |
| [<span data-ttu-id="cbc3d-121">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="cbc3d-121">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="cbc3d-122">是</span><span class="sxs-lookup"><span data-stu-id="cbc3d-122">yes</span></span>       |
| [<span data-ttu-id="cbc3d-123">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="cbc3d-123">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="cbc3d-124">不可以</span><span class="sxs-lookup"><span data-stu-id="cbc3d-124">no</span></span>        |
| [<span data-ttu-id="cbc3d-125">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="cbc3d-125">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="cbc3d-126">不可以</span><span class="sxs-lookup"><span data-stu-id="cbc3d-126">no</span></span>        |
| [<span data-ttu-id="cbc3d-127">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="cbc3d-127">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="cbc3d-128">不可以</span><span class="sxs-lookup"><span data-stu-id="cbc3d-128">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="cbc3d-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="cbc3d-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cbc3d-130">著色器模型5指令修飾詞</span><span class="sxs-lookup"><span data-stu-id="cbc3d-130">Shader Model 5 Instruction Modifiers</span></span>](shader-model-5-instruction-modifiers.md)
</dt> </dl>

 

 




