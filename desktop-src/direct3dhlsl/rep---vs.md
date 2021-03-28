---
title: rep-vs
description: 開始 a rep .。。endrep 組塊。
ms.assetid: vs|directx_sdk|~\rep___vs.htm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5441d5d134ee2d60e14db9f273ec374323f93902
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104373767"
---
# <a name="rep---vs"></a><span data-ttu-id="193d3-103">rep-vs</span><span class="sxs-lookup"><span data-stu-id="193d3-103">rep - vs</span></span>

<span data-ttu-id="193d3-104">開始 a rep .。。[endrep](endrep---vs.md) 組塊。</span><span class="sxs-lookup"><span data-stu-id="193d3-104">Start a rep...[endrep](endrep---vs.md) block.</span></span>

## <a name="syntax"></a><span data-ttu-id="193d3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="193d3-105">Syntax</span></span>



| <span data-ttu-id="193d3-106">rep\#</span><span class="sxs-lookup"><span data-stu-id="193d3-106">rep i\#</span></span> |
|---------|



 

<span data-ttu-id="193d3-107">其中 i \# 是指定. x 元件中重複計數的整數暫存器。</span><span class="sxs-lookup"><span data-stu-id="193d3-107">where i\# is an integer register that specifies the repeat count in the .x component.</span></span> <span data-ttu-id="193d3-108">請參閱 [常數整數註冊](dx9-graphics-reference-asm-vs-registers-constant-integer.md)。</span><span class="sxs-lookup"><span data-stu-id="193d3-108">See [Constant Integer Register](dx9-graphics-reference-asm-vs-registers-constant-integer.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="193d3-109">備註</span><span class="sxs-lookup"><span data-stu-id="193d3-109">Remarks</span></span>



| <span data-ttu-id="193d3-110">頂點著色器版本</span><span class="sxs-lookup"><span data-stu-id="193d3-110">Vertex shader versions</span></span> | <span data-ttu-id="193d3-111">1\_1</span><span class="sxs-lookup"><span data-stu-id="193d3-111">1\_1</span></span> | <span data-ttu-id="193d3-112">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="193d3-112">2\_0</span></span> | <span data-ttu-id="193d3-113">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="193d3-113">2\_x</span></span> | <span data-ttu-id="193d3-114">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="193d3-114">2\_sw</span></span> | <span data-ttu-id="193d3-115">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="193d3-115">3\_0</span></span> | <span data-ttu-id="193d3-116">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="193d3-116">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="193d3-117">代表</span><span class="sxs-lookup"><span data-stu-id="193d3-117">rep</span></span>                    |      | <span data-ttu-id="193d3-118">x</span><span class="sxs-lookup"><span data-stu-id="193d3-118">x</span></span>    | <span data-ttu-id="193d3-119">x</span><span class="sxs-lookup"><span data-stu-id="193d3-119">x</span></span>    | <span data-ttu-id="193d3-120">x</span><span class="sxs-lookup"><span data-stu-id="193d3-120">x</span></span>     | <span data-ttu-id="193d3-121">x</span><span class="sxs-lookup"><span data-stu-id="193d3-121">x</span></span>    | <span data-ttu-id="193d3-122">x</span><span class="sxs-lookup"><span data-stu-id="193d3-122">x</span></span>     |



 

-   <span data-ttu-id="193d3-123">\#x.x.x.x 會指定反復專案計數。</span><span class="sxs-lookup"><span data-stu-id="193d3-123">i\#.x specifies the iteration count.</span></span> <span data-ttu-id="193d3-124">合法範圍是 \[ 0，255 \] 。</span><span class="sxs-lookup"><span data-stu-id="193d3-124">The legal range is \[0, 255\].</span></span> <span data-ttu-id="193d3-125">請注意，此指令不會遞增或遞減 i \# . x 的值。</span><span class="sxs-lookup"><span data-stu-id="193d3-125">Note that this instruction does not increment or decrement the value of i\#.x.</span></span>
-   <span data-ttu-id="193d3-126">\#yzw 不是由重複區塊使用。</span><span class="sxs-lookup"><span data-stu-id="193d3-126">i\#.yzw are not used by the repeat block.</span></span>
-   <span data-ttu-id="193d3-127">重複區塊可能會進行嵌套。</span><span class="sxs-lookup"><span data-stu-id="193d3-127">Repeat blocks may be nested.</span></span> <span data-ttu-id="193d3-128">請參閱 [流程式控制制的嵌套限制](dx9-graphics-reference-asm-vs-instructions-flow-control.md)。</span><span class="sxs-lookup"><span data-stu-id="193d3-128">See [Flow Control Nesting Limits](dx9-graphics-reference-asm-vs-instructions-flow-control.md).</span></span>
-   <span data-ttu-id="193d3-129">重複區塊可以完全在 if \* 區塊內或完全圍繞它。</span><span class="sxs-lookup"><span data-stu-id="193d3-129">Repeat blocks are allowed to be either completely inside an if\* block or completely surrounding it.</span></span> <span data-ttu-id="193d3-130">不允許任何 straddling。</span><span class="sxs-lookup"><span data-stu-id="193d3-130">No straddling is allowed.</span></span>
-   <span data-ttu-id="193d3-131">針對不同或嵌套的 rep 表示，使用相同的 i， \# 每個迴圈都會根據指定的計數逐一進行反覆運算。</span><span class="sxs-lookup"><span data-stu-id="193d3-131">Using the same i\# for different or nested rep instructions is fine - each loop will iterate based on the specified count.</span></span>

## <a name="example"></a><span data-ttu-id="193d3-132">範例</span><span class="sxs-lookup"><span data-stu-id="193d3-132">Example</span></span>


```
rep i2
    add r0, r0, c0
endrep  
```



## <a name="related-topics"></a><span data-ttu-id="193d3-133">相關主題</span><span class="sxs-lookup"><span data-stu-id="193d3-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="193d3-134">頂點著色器指示</span><span class="sxs-lookup"><span data-stu-id="193d3-134">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




