---
title: " (Direct3D 11) 的效果格式"
ms.assetid: c425f57b-fc14-46a5-bb65-a0a2305bd406
description: '深入瞭解：效果格式 (Direct3D 11) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c08589fcb041591591d033b88e4fafe597e98520
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104187703"
---
# <a name="effect-format-direct3d-11"></a><span data-ttu-id="b0694-103"> (Direct3D 11) 的效果格式</span><span class="sxs-lookup"><span data-stu-id="b0694-103">Effect Format (Direct3D 11)</span></span>

<span data-ttu-id="b0694-104">效果 (通常儲存在副檔名為 fx 的檔案中) 宣告由效果設定的管線狀態。</span><span class="sxs-lookup"><span data-stu-id="b0694-104">An effect (which is often stored in a file with a .fx file extension) declares the pipeline state set by an effect.</span></span> <span data-ttu-id="b0694-105">效果狀態大致可以分為三個類別：</span><span class="sxs-lookup"><span data-stu-id="b0694-105">Effect state can be roughly broken down into three categories:</span></span>

-   <span data-ttu-id="b0694-106">[變數](d3d11-effect-variable-syntax.md)，通常會在效果頂端宣告。</span><span class="sxs-lookup"><span data-stu-id="b0694-106">[Variables](d3d11-effect-variable-syntax.md), which are usually declared at the top of an effect.</span></span>
-   <span data-ttu-id="b0694-107">函[式，可](d3d11-effect-function-syntax.md)執行著色器程式碼，或作為其他函式的 helper 函式使用。</span><span class="sxs-lookup"><span data-stu-id="b0694-107">[Functions](d3d11-effect-function-syntax.md), which implement shader code, or are used as helper functions by other functions.</span></span>
-   <span data-ttu-id="b0694-108">可以在效果群組中排列，並使用一或多個效果階段來實行轉譯順序的[技巧](d3d11-effect-technique-syntax.md)。</span><span class="sxs-lookup"><span data-stu-id="b0694-108">[Techniques](d3d11-effect-technique-syntax.md), which can be arranged in effect groups, and implement rendering sequences using one or more effect passes.</span></span> <span data-ttu-id="b0694-109">每個階段都會設定一個或多個 [狀態群組](d3d11-effect-states.md) ，並呼叫著色器函式。</span><span class="sxs-lookup"><span data-stu-id="b0694-109">Each pass sets one or more [state groups](d3d11-effect-states.md) and calls shader functions.</span></span>

![效果宣告分類的圖表，包括頂端的變數、中間的函式，以及底部的技巧](images/d3d10-effect-intro.png)

<span data-ttu-id="b0694-111">上圖顯示效果狀態的類別。</span><span class="sxs-lookup"><span data-stu-id="b0694-111">The preceding diagram shows the categories of effect state.</span></span>

<span data-ttu-id="b0694-112">效果二進位格式的定義可以在效果原始程式碼的二進位 EffectBinaryFormat 中找到 \\ 。</span><span class="sxs-lookup"><span data-stu-id="b0694-112">The definition of the effect binary format can be found in Binary\\EffectBinaryFormat.h in the effects source code.</span></span>


## <a name="in-this-section"></a><span data-ttu-id="b0694-113">本節內容</span><span class="sxs-lookup"><span data-stu-id="b0694-113">In this section</span></span>



| <span data-ttu-id="b0694-114">主題</span><span class="sxs-lookup"><span data-stu-id="b0694-114">Topic</span></span>                                                                   | <span data-ttu-id="b0694-115">描述</span><span class="sxs-lookup"><span data-stu-id="b0694-115">Description</span></span>                                                                                                          |
|-------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b0694-116">效果變數語法</span><span class="sxs-lookup"><span data-stu-id="b0694-116">Effect Variable Syntax</span></span>](d3d11-effect-variable-syntax.md)<br/>   | <span data-ttu-id="b0694-117">效果變數是利用本節所述的語法來宣告。</span><span class="sxs-lookup"><span data-stu-id="b0694-117">An effect variable is declared with the syntax described in this section.</span></span><br/>                                 |
| [<span data-ttu-id="b0694-118">注釋語法</span><span class="sxs-lookup"><span data-stu-id="b0694-118">Annotation Syntax</span></span>](d3d11-effect-annotation-syntax.md)<br/>      | <span data-ttu-id="b0694-119">批註是使用者定義的資訊片段，以本節所述的語法來宣告。</span><span class="sxs-lookup"><span data-stu-id="b0694-119">An annotation is a user-defined piece of information, declared with the syntax described in this section.</span></span><br/> |
| [<span data-ttu-id="b0694-120">效果函數語法</span><span class="sxs-lookup"><span data-stu-id="b0694-120">Effect Function Syntax</span></span>](d3d11-effect-function-syntax.md)<br/>   | <span data-ttu-id="b0694-121">效果函式是以 HLSL 撰寫，並使用本節所述的語法來宣告。</span><span class="sxs-lookup"><span data-stu-id="b0694-121">An effect function is written in HLSL and is declared with the syntax described in this section.</span></span><br/>          |
| [<span data-ttu-id="b0694-122">效果技巧語法</span><span class="sxs-lookup"><span data-stu-id="b0694-122">Effect Technique Syntax</span></span>](d3d11-effect-technique-syntax.md)<br/> | <span data-ttu-id="b0694-123">效果技術會以本節所述的語法來宣告。</span><span class="sxs-lookup"><span data-stu-id="b0694-123">An effect technique is declared with the syntax described in this section.</span></span><br/>                                |
| [<span data-ttu-id="b0694-124">效果狀態群組</span><span class="sxs-lookup"><span data-stu-id="b0694-124">Effect State Groups</span></span>](d3d11-effect-states.md)<br/>               | <span data-ttu-id="b0694-125">效果狀態是運算式形式的名稱值配對。</span><span class="sxs-lookup"><span data-stu-id="b0694-125">Effect states are name value pairs in the form of an expression.</span></span><br/>                                          |
| [<span data-ttu-id="b0694-126">效果群組語法</span><span class="sxs-lookup"><span data-stu-id="b0694-126">Effect Group Syntax</span></span>](d3d11-effect-group-syntax.md)<br/>         | <span data-ttu-id="b0694-127">使用本節所述的語法來宣告效果群組。</span><span class="sxs-lookup"><span data-stu-id="b0694-127">An effect group is declared with the syntax described in this section.</span></span><br/>                                    |



 

## <a name="related-topics"></a><span data-ttu-id="b0694-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="b0694-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b0694-129">效果11參考</span><span class="sxs-lookup"><span data-stu-id="b0694-129">Effects 11 Reference</span></span>](d3d11-graphics-reference-effects11.md)
</dt> </dl>

 

 





