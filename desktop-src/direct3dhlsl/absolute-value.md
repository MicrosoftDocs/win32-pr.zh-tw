---
title: 絕對值
description: 取得算數運算中所使用之來源運算元的絕對值。
ms.assetid: FD2ACE91-0AF6-43E8-80C5-849488E39BEF
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 27ceefa2c4b4ee2eb890b0692a33266e89a18cfb
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104313742"
---
# <a name="absolute-value"></a><span data-ttu-id="3cd9e-103">絕對值</span><span class="sxs-lookup"><span data-stu-id="3cd9e-103">Absolute Value</span></span>

<span data-ttu-id="3cd9e-104">取得算數運算中所使用之來源運算元的絕對值。</span><span class="sxs-lookup"><span data-stu-id="3cd9e-104">Take the absolute value of a source operand used in an arithmetic operation.</span></span>



| <span data-ttu-id="3cd9e-105">\_Abs</span><span class="sxs-lookup"><span data-stu-id="3cd9e-105">\_abs</span></span> |
|-------|



 

<span data-ttu-id="3cd9e-106">此修飾詞僅適用于單一和雙精確度浮點數和指示。</span><span class="sxs-lookup"><span data-stu-id="3cd9e-106">This modifier is used for single and double precision floating point and instructions only.</span></span> <span data-ttu-id="3cd9e-107">**\_ Abs** 修飾詞會強制在來源運算元的 (s) 的正負號，包括 IN光圈值在內。</span><span class="sxs-lookup"><span data-stu-id="3cd9e-107">The **\_abs** modifier forces the sign of the number(s) on the source operand positive, including on INF values.</span></span>

<span data-ttu-id="3cd9e-108">在 NaN 上套用 **\_ abs** 會保留 nan，雖然未定義結果的特定 NaN 位模式。</span><span class="sxs-lookup"><span data-stu-id="3cd9e-108">Applying **\_abs** on NaN preserves NaN, although the particular NaN bit pattern that results is not defined.</span></span>

<span data-ttu-id="3cd9e-109">當 \_ abs 與 [否定](negate.md)修飾詞結合時，此組合會強制正負號為負數，如同先套用 **\_ abs** 修飾詞，然後是 **否定** 的。</span><span class="sxs-lookup"><span data-stu-id="3cd9e-109">When \_abs is combined with the [negate](negate.md) modifier, the combination forces the sign to be negative, as if the **\_abs** modifier is applied first, then the **negate**.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="3cd9e-110">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="3cd9e-110">Minimum Shader Model</span></span>

<span data-ttu-id="3cd9e-111">下列著色器模型支援此修飾詞。</span><span class="sxs-lookup"><span data-stu-id="3cd9e-111">This modifier is supported in the following shader models.</span></span>



| <span data-ttu-id="3cd9e-112">著色器模型</span><span class="sxs-lookup"><span data-stu-id="3cd9e-112">Shader Model</span></span>                                              | <span data-ttu-id="3cd9e-113">支援</span><span class="sxs-lookup"><span data-stu-id="3cd9e-113">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="3cd9e-114">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="3cd9e-114">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="3cd9e-115">是</span><span class="sxs-lookup"><span data-stu-id="3cd9e-115">yes</span></span>       |
| [<span data-ttu-id="3cd9e-116">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="3cd9e-116">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="3cd9e-117">是</span><span class="sxs-lookup"><span data-stu-id="3cd9e-117">yes</span></span>       |
| [<span data-ttu-id="3cd9e-118">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="3cd9e-118">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="3cd9e-119">是</span><span class="sxs-lookup"><span data-stu-id="3cd9e-119">yes</span></span>       |
| [<span data-ttu-id="3cd9e-120">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="3cd9e-120">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="3cd9e-121">不可以</span><span class="sxs-lookup"><span data-stu-id="3cd9e-121">no</span></span>        |
| [<span data-ttu-id="3cd9e-122">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="3cd9e-122">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="3cd9e-123">不可以</span><span class="sxs-lookup"><span data-stu-id="3cd9e-123">no</span></span>        |
| [<span data-ttu-id="3cd9e-124">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="3cd9e-124">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="3cd9e-125">不可以</span><span class="sxs-lookup"><span data-stu-id="3cd9e-125">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="3cd9e-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="3cd9e-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3cd9e-127">指令修飾詞</span><span class="sxs-lookup"><span data-stu-id="3cd9e-127">Instruction Modifiers</span></span>](instruction-modifiers.md)
</dt> </dl>

 

 




