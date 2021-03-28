---
title: HLSL 與參考) 的指令修飾詞 (
description: 指令修飾詞
ms.assetid: b713d847-c858-4492-918c-7a105f751624
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 573f2ef618c4cd29092fb38fb4c805bdeeecc219
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/23/2019
ms.locfileid: "104462624"
---
# <a name="instruction-modifiers-hlsl-vs-reference"></a><span data-ttu-id="52c2c-103">HLSL 與參考) 的指令修飾詞 (</span><span class="sxs-lookup"><span data-stu-id="52c2c-103">Instruction modifiers (HLSL VS reference)</span></span>

<span data-ttu-id="52c2c-104">指令修飾詞會在將指令寫入目的地登錄之前，先影響指令的結果。</span><span class="sxs-lookup"><span data-stu-id="52c2c-104">Instruction modifiers affect the result of the instruction before it is written into the destination register.</span></span>

## <a name="_sat"></a><span data-ttu-id="52c2c-105">\_坐</span><span class="sxs-lookup"><span data-stu-id="52c2c-105">\_sat</span></span>

<span data-ttu-id="52c2c-106">在寫入目的地登錄之前， (或個將指令結果) 至 \[ 0，1個 \] 範圍內。</span><span class="sxs-lookup"><span data-stu-id="52c2c-106">Saturates (or clamps) the instruction result to \[0,1\] range before writing to the destination register.</span></span>

<span data-ttu-id="52c2c-107">例如：</span><span class="sxs-lookup"><span data-stu-id="52c2c-107">For example:</span></span>


```
add_sat dst, src0, src1
```



<span data-ttu-id="52c2c-108">其中：</span><span class="sxs-lookup"><span data-stu-id="52c2c-108">Where:</span></span>

<span data-ttu-id="52c2c-109">dst = \_ 介於 \_ 0 \_ 和1之間的夾具 \_ (src0 + src1) </span><span class="sxs-lookup"><span data-stu-id="52c2c-109">dst = clamp\_between\_0\_and\_1(src0 + src1)</span></span>

<span data-ttu-id="52c2c-110">\_Sat 指令修飾詞的成本沒有額外的指示位置。</span><span class="sxs-lookup"><span data-stu-id="52c2c-110">The \_sat instruction modifier costs no additional instruction slots.</span></span>

<span data-ttu-id="52c2c-111">如果支援，則 \_ 除了： [frc-vs](frc---vs.md)、 [sincos-vs](sincos---vs.md)和 [texldl-vs](texldl---vs.md)，sat 指令修飾詞可以搭配任何指令使用。</span><span class="sxs-lookup"><span data-stu-id="52c2c-111">If supported, the \_sat instruction modifier can be used with any instruction except: [frc - vs](frc---vs.md), [sincos - vs](sincos---vs.md), and [texldl - vs](texldl---vs.md).</span></span>



| <span data-ttu-id="52c2c-112">頂點著色器版本</span><span class="sxs-lookup"><span data-stu-id="52c2c-112">Vertex shader versions</span></span> | <span data-ttu-id="52c2c-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="52c2c-113">1\_1</span></span> | <span data-ttu-id="52c2c-114">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="52c2c-114">2\_0</span></span> | <span data-ttu-id="52c2c-115">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="52c2c-115">2\_x</span></span> | <span data-ttu-id="52c2c-116">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="52c2c-116">2\_sw</span></span> | <span data-ttu-id="52c2c-117">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="52c2c-117">3\_0</span></span> | <span data-ttu-id="52c2c-118">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="52c2c-118">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="52c2c-119">\_坐</span><span class="sxs-lookup"><span data-stu-id="52c2c-119">\_sat</span></span>                  |      |      |      |       | <span data-ttu-id="52c2c-120">x</span><span class="sxs-lookup"><span data-stu-id="52c2c-120">x</span></span>    | <span data-ttu-id="52c2c-121">x</span><span class="sxs-lookup"><span data-stu-id="52c2c-121">x</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="52c2c-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="52c2c-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="52c2c-123">頂點著色器指示</span><span class="sxs-lookup"><span data-stu-id="52c2c-123">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




