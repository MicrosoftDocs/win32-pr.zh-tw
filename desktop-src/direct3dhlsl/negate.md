---
title: Negate
description: 翻轉算數運算中所使用之來源運算元值的正負號。
ms.assetid: 83ef3f61-7b0b-4033-8f7b-5345b205c441
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: cc2637a76b52b28eefcfb3637cc8b2d406c02c06
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104022806"
---
# <a name="negate"></a><span data-ttu-id="fa5a1-103">Negate</span><span class="sxs-lookup"><span data-stu-id="fa5a1-103">Negate</span></span>

<span data-ttu-id="fa5a1-104">翻轉算數運算中所使用之來源運算元值的正負號。</span><span class="sxs-lookup"><span data-stu-id="fa5a1-104">Flips the sign of the value of a source operand used in an arithmetic operation.</span></span>



| \-  |
|-----|



 

<span data-ttu-id="fa5a1-105">若為單精確度和雙精度浮點數和指示，否定修飾詞會翻轉來源運算元中)  (s 的正負號，包括 IN光圈值在內。</span><span class="sxs-lookup"><span data-stu-id="fa5a1-105">For single and double precision floating point and instructions, the negate modifier flips the sign of the number(s) in the source operand, including on INF values.</span></span> <span data-ttu-id="fa5a1-106">在 NaN 上套用 **否定** 會保留 nan，雖然未定義結果的特定 NaN 位模式。</span><span class="sxs-lookup"><span data-stu-id="fa5a1-106">Applying **negate** on NaN preserves NaN, although the particular NaN bit pattern that results is not defined.</span></span>

<span data-ttu-id="fa5a1-107">若為整數指示， **否定** 修飾詞會採用來源運算元中)  (s 的2補數。</span><span class="sxs-lookup"><span data-stu-id="fa5a1-107">For integer instructions, the **negate** modifier takes the 2's complement of the number(s) in the source operand.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="fa5a1-108">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="fa5a1-108">Minimum Shader Model</span></span>

<span data-ttu-id="fa5a1-109">下列著色器模型支援此修飾詞。</span><span class="sxs-lookup"><span data-stu-id="fa5a1-109">This modifier is supported in the following shader models.</span></span>



| <span data-ttu-id="fa5a1-110">著色器模型</span><span class="sxs-lookup"><span data-stu-id="fa5a1-110">Shader Model</span></span>                                              | <span data-ttu-id="fa5a1-111">支援</span><span class="sxs-lookup"><span data-stu-id="fa5a1-111">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="fa5a1-112">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="fa5a1-112">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="fa5a1-113">是</span><span class="sxs-lookup"><span data-stu-id="fa5a1-113">yes</span></span>       |
| [<span data-ttu-id="fa5a1-114">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="fa5a1-114">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="fa5a1-115">是</span><span class="sxs-lookup"><span data-stu-id="fa5a1-115">yes</span></span>       |
| [<span data-ttu-id="fa5a1-116">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="fa5a1-116">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="fa5a1-117">是</span><span class="sxs-lookup"><span data-stu-id="fa5a1-117">yes</span></span>       |
| [<span data-ttu-id="fa5a1-118">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="fa5a1-118">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="fa5a1-119">不可以</span><span class="sxs-lookup"><span data-stu-id="fa5a1-119">no</span></span>        |
| [<span data-ttu-id="fa5a1-120">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="fa5a1-120">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="fa5a1-121">不可以</span><span class="sxs-lookup"><span data-stu-id="fa5a1-121">no</span></span>        |
| [<span data-ttu-id="fa5a1-122">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="fa5a1-122">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="fa5a1-123">不可以</span><span class="sxs-lookup"><span data-stu-id="fa5a1-123">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="fa5a1-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="fa5a1-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fa5a1-125">指令修飾詞</span><span class="sxs-lookup"><span data-stu-id="fa5a1-125">Instruction Modifiers</span></span>](instruction-modifiers.md)
</dt> </dl>

 

 




