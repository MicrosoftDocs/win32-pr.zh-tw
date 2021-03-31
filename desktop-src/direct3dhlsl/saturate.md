---
title: " (HLSL 參考) 飽和"
description: 將單一或雙精確度浮點算數運算的結果個至 \ 0.0 f .。。1.0 f-範圍。
ms.assetid: ce3e79c7-c3e6-4a2c-910a-2cd568aece50
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 05b6048777ac7b6ecd2c4b59ff3c9e0287380949
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/23/2019
ms.locfileid: "104373983"
---
# <a name="saturate-hlsl-reference"></a><span data-ttu-id="543b8-103"> (HLSL 參考) 飽和</span><span class="sxs-lookup"><span data-stu-id="543b8-103">Saturate (HLSL reference)</span></span>

<span data-ttu-id="543b8-104">個單或雙精確度浮點算數運算的結果為 \[ 0.0 f .。。1.0 f \] 範圍。</span><span class="sxs-lookup"><span data-stu-id="543b8-104">Clamps the result of a single or double precision floating point arithmetic operation to \[0.0f...1.0f\] range.</span></span>



| <span data-ttu-id="543b8-105">\_坐</span><span class="sxs-lookup"><span data-stu-id="543b8-105">\_sat</span></span> |
|-------|



 

<span data-ttu-id="543b8-106">[ **飽和** 指令結果] 修飾詞會針對結果值執行下列作業， (s 從已套用 sat 的浮點算數運算) \_ ：</span><span class="sxs-lookup"><span data-stu-id="543b8-106">The **saturate** instruction result modifier performs the following operation on the result values(s) from a floating point arithmetic operation that has \_sat applied to it:</span></span>

`min(1.0f, max(0.0f, value))`

<span data-ttu-id="543b8-107">上述運算式中最小 () 和最大 () 的運作方式是 [最小值](min--sm4---asm-.md)、 [最大](max--sm4---asm-.md)值、最小值、 [dmin](dmin--sm5---asm-.md)或 [dmax](dmax--sm5---asm-.md) 的運作方式。</span><span class="sxs-lookup"><span data-stu-id="543b8-107">where min() and max() in the above expression behave in the way [min](min--sm4---asm-.md), [max](max--sm4---asm-.md), [dmin](dmin--sm5---asm-.md), or [dmax](dmax--sm5---asm-.md) operate.</span></span>

<span data-ttu-id="543b8-108">`_sat(NaN)` 依 min 和 max 的規則傳回0。</span><span class="sxs-lookup"><span data-stu-id="543b8-108">`_sat(NaN)` returns 0, by the rules for min and max.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="543b8-109">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="543b8-109">Minimum Shader Model</span></span>

<span data-ttu-id="543b8-110">下列著色器模型支援此修飾詞。</span><span class="sxs-lookup"><span data-stu-id="543b8-110">This modifier is supported in the following shader models.</span></span>



| <span data-ttu-id="543b8-111">著色器模型</span><span class="sxs-lookup"><span data-stu-id="543b8-111">Shader Model</span></span>                                              | <span data-ttu-id="543b8-112">支援</span><span class="sxs-lookup"><span data-stu-id="543b8-112">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="543b8-113">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="543b8-113">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="543b8-114">是</span><span class="sxs-lookup"><span data-stu-id="543b8-114">yes</span></span>       |
| [<span data-ttu-id="543b8-115">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="543b8-115">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="543b8-116">是</span><span class="sxs-lookup"><span data-stu-id="543b8-116">yes</span></span>       |
| [<span data-ttu-id="543b8-117">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="543b8-117">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="543b8-118">是</span><span class="sxs-lookup"><span data-stu-id="543b8-118">yes</span></span>       |
| [<span data-ttu-id="543b8-119">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="543b8-119">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="543b8-120">不可以</span><span class="sxs-lookup"><span data-stu-id="543b8-120">no</span></span>        |
| [<span data-ttu-id="543b8-121">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="543b8-121">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="543b8-122">不可以</span><span class="sxs-lookup"><span data-stu-id="543b8-122">no</span></span>        |
| [<span data-ttu-id="543b8-123">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="543b8-123">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="543b8-124">不可以</span><span class="sxs-lookup"><span data-stu-id="543b8-124">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="543b8-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="543b8-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="543b8-126">指令修飾詞</span><span class="sxs-lookup"><span data-stu-id="543b8-126">Instruction Modifiers</span></span>](instruction-modifiers.md)
</dt> </dl>

 

 




