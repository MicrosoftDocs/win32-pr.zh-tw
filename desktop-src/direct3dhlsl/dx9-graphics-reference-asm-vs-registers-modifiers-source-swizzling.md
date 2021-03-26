---
title: '來源登錄 Swizzling (HLSL 與參考) '
description: 在執行指令之前，會將來源暫存器中的資料複製到臨時暫存器。 Swizzling 是指將任何來源暫存器元件複製到任何暫存登錄元件的能力。 Swizzling 不會影響來源註冊資料。
ms.assetid: 6271d846-c68d-467c-a110-be3279e0c11a
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c075d8ff47b1f76adf378b6a583cd4d675651a87
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/23/2019
ms.locfileid: "104373959"
---
# <a name="source-register-swizzling-hlsl-vs-reference"></a><span data-ttu-id="2bbb2-105">來源登錄 Swizzling (HLSL 與參考) </span><span class="sxs-lookup"><span data-stu-id="2bbb2-105">Source Register Swizzling (HLSL VS reference)</span></span>

<span data-ttu-id="2bbb2-106">在執行指令之前，會將來源暫存器中的資料複製到臨時暫存器。</span><span class="sxs-lookup"><span data-stu-id="2bbb2-106">Before an instruction runs, the data in a source register is copied to a temporary register.</span></span> <span data-ttu-id="2bbb2-107">Swizzling 是指將任何來源暫存器元件複製到任何暫存登錄元件的能力。</span><span class="sxs-lookup"><span data-stu-id="2bbb2-107">Swizzling refers to the ability to copy any source register component to any temporary register component.</span></span> <span data-ttu-id="2bbb2-108">Swizzling 不會影響來源註冊資料。</span><span class="sxs-lookup"><span data-stu-id="2bbb2-108">Swizzling does not affect the source register data.</span></span>

## <a name="component-swizzling"></a><span data-ttu-id="2bbb2-109">元件 Swizzling</span><span class="sxs-lookup"><span data-stu-id="2bbb2-109">Component Swizzling</span></span>

<span data-ttu-id="2bbb2-110">如下表所示，swizzling 可以套用至來源暫存器資料的個別元件 (其中是其中一個有效的頂點著色器輸入暫存器 [-vs \_ 1 \_ 1](dx9-graphics-reference-asm-vs-registers-vs-1-1.md)) 。</span><span class="sxs-lookup"><span data-stu-id="2bbb2-110">As shown in the following table, swizzling can be applied to the individual components of the source register data (where r is one of the valid vertex shader input [Registers - vs\_1\_1](dx9-graphics-reference-asm-vs-registers-vs-1-1.md)).</span></span>



| <span data-ttu-id="2bbb2-111">元件修飾詞</span><span class="sxs-lookup"><span data-stu-id="2bbb2-111">Component modifier</span></span>                 | <span data-ttu-id="2bbb2-112">Description</span><span class="sxs-lookup"><span data-stu-id="2bbb2-112">Description</span></span>    |
|------------------------------------|----------------|
| <span data-ttu-id="2bbb2-113">r。 \[xyzw \] \[ xyzw \] \[ xyzw \] \[ xyzw\]</span><span class="sxs-lookup"><span data-stu-id="2bbb2-113">r.\[xyzw\]\[xyzw\]\[xyzw\]\[xyzw\]</span></span> | <span data-ttu-id="2bbb2-114">來源 swizzle</span><span class="sxs-lookup"><span data-stu-id="2bbb2-114">Source swizzle</span></span> |



 

-   <span data-ttu-id="2bbb2-115">所有四個元件一律都會複製。</span><span class="sxs-lookup"><span data-stu-id="2bbb2-115">All four components are always copied.</span></span> <span data-ttu-id="2bbb2-116">如果指定了四個以上的元件，則會重複 (xy 表示 xyyy) 的最後一個元件。</span><span class="sxs-lookup"><span data-stu-id="2bbb2-116">If fewer than four components are specified, the last component is repeated (xy means .xyyy).</span></span> <span data-ttu-id="2bbb2-117">如果未指定任何元件，則 x 會重複 ( xxxx) 。</span><span class="sxs-lookup"><span data-stu-id="2bbb2-117">If no components are specified, x is repeated (.xxxx).</span></span>
-   <span data-ttu-id="2bbb2-118">元件可以依任何順序顯示。</span><span class="sxs-lookup"><span data-stu-id="2bbb2-118">The components can appear in any order.</span></span> <span data-ttu-id="2bbb2-119">v0 ywx 會產生 v0. ywxx。</span><span class="sxs-lookup"><span data-stu-id="2bbb2-119">v0.ywx results in v0.ywxx.</span></span>
-   <span data-ttu-id="2bbb2-120">Rgba 元件可以分別用於 xyzw (r for x、g for b 等 ) 。</span><span class="sxs-lookup"><span data-stu-id="2bbb2-120">The rgba components can be used respectively for xyzw (r for x, g for b, etc.).</span></span>
-   <span data-ttu-id="2bbb2-121">這些指示會實作為來源-註冊單一元件 swizzles： exp、expp、log、logp、pow、rcp、rsq。</span><span class="sxs-lookup"><span data-stu-id="2bbb2-121">These instructions implement source-register single component swizzles: exp, expp, log, logp, pow, rcp, rsq.</span></span> <span data-ttu-id="2bbb2-122">這些指示的結果會複製到所有的四個目的地註冊元件。</span><span class="sxs-lookup"><span data-stu-id="2bbb2-122">The result of these instructions is copied to all four destination register components.</span></span>

<span data-ttu-id="2bbb2-123">Swizzling 不能用於 [m3x2-vs](m3x2---vs.md)、 [m3x3-vs](m3x3---vs.md)、 [m4x3-vs](m4x3---vs.md)和 [m4x4-vs](m4x4---vs.md) 指令。</span><span class="sxs-lookup"><span data-stu-id="2bbb2-123">Swizzling cannot be used on the [m3x2 - vs](m3x2---vs.md), [m3x3 - vs](m3x3---vs.md), [m4x3 - vs](m4x3---vs.md), and [m4x4 - vs](m4x4---vs.md) instructions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2bbb2-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="2bbb2-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2bbb2-125">頂點著色器暫存器修飾詞</span><span class="sxs-lookup"><span data-stu-id="2bbb2-125">Vertex Shader Register Modifiers</span></span>](dx9-graphics-reference-asm-vs-registers-modifiers.md)
</dt> </dl>

 

 




