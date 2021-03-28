---
title: 迴圈-vs
description: 開始迴圈 .。。endloop 組塊。
ms.assetid: vs|directx_sdk|~\loop___vs.htm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6a96a1ce53b850ec8feeba282055e8111b275bfd
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104990778"
---
# <a name="loop---vs"></a><span data-ttu-id="59069-103">迴圈-vs</span><span class="sxs-lookup"><span data-stu-id="59069-103">loop - vs</span></span>

<span data-ttu-id="59069-104">開始迴圈 .。。[endloop](endloop---vs.md) 組塊。</span><span class="sxs-lookup"><span data-stu-id="59069-104">Start a loop...[endloop](endloop---vs.md) block.</span></span>

## <a name="syntax"></a><span data-ttu-id="59069-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="59069-105">Syntax</span></span>



| <span data-ttu-id="59069-106">迴圈 aL、i\#</span><span class="sxs-lookup"><span data-stu-id="59069-106">loop aL, i\#</span></span> |
|--------------|



 

<span data-ttu-id="59069-107">其中：</span><span class="sxs-lookup"><span data-stu-id="59069-107">Where:</span></span>

-   <span data-ttu-id="59069-108">aL 是包含目前迴圈計數的 [迴圈計數器](dx9-graphics-reference-asm-vs-registers-loop-counter.md) 暫存器。</span><span class="sxs-lookup"><span data-stu-id="59069-108">aL is the [Loop Counter Register](dx9-graphics-reference-asm-vs-registers-loop-counter.md) holding the current loop count.</span></span>
-   <span data-ttu-id="59069-109">我 \# 是 [常數整數註冊](dx9-graphics-reference-asm-vs-registers-constant-integer.md)。</span><span class="sxs-lookup"><span data-stu-id="59069-109">i\# is a [Constant Integer Register](dx9-graphics-reference-asm-vs-registers-constant-integer.md).</span></span> <span data-ttu-id="59069-110">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="59069-110">See remarks.</span></span>

## <a name="remarks"></a><span data-ttu-id="59069-111">備註</span><span class="sxs-lookup"><span data-stu-id="59069-111">Remarks</span></span>



| <span data-ttu-id="59069-112">頂點著色器版本</span><span class="sxs-lookup"><span data-stu-id="59069-112">Vertex shader versions</span></span> | <span data-ttu-id="59069-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="59069-113">1\_1</span></span> | <span data-ttu-id="59069-114">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="59069-114">2\_0</span></span> | <span data-ttu-id="59069-115">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="59069-115">2\_x</span></span> | <span data-ttu-id="59069-116">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="59069-116">2\_sw</span></span> | <span data-ttu-id="59069-117">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="59069-117">3\_0</span></span> | <span data-ttu-id="59069-118">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="59069-118">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="59069-119">loop</span><span class="sxs-lookup"><span data-stu-id="59069-119">loop</span></span>                   |      | <span data-ttu-id="59069-120">x</span><span class="sxs-lookup"><span data-stu-id="59069-120">x</span></span>    | <span data-ttu-id="59069-121">x</span><span class="sxs-lookup"><span data-stu-id="59069-121">x</span></span>    | <span data-ttu-id="59069-122">x</span><span class="sxs-lookup"><span data-stu-id="59069-122">x</span></span>     | <span data-ttu-id="59069-123">x</span><span class="sxs-lookup"><span data-stu-id="59069-123">x</span></span>    | <span data-ttu-id="59069-124">x</span><span class="sxs-lookup"><span data-stu-id="59069-124">x</span></span>     |



 

-   <span data-ttu-id="59069-125">[迴圈計數器](dx9-graphics-reference-asm-vs-registers-loop-counter.md)暫存器 (aL) 保留目前的迴圈計數，並且可用於在迴圈區塊內 (o) 中的「[常數整數](dx9-graphics-reference-asm-vs-registers-constant-integer.md)暫存器」 (c \#) 或[輸出](dx9-graphics-reference-asm-vs-registers-vs-3-0.md)暫存器的相對定址 \# 。</span><span class="sxs-lookup"><span data-stu-id="59069-125">The [Loop Counter Register](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (aL) holds the current loop count, and can be used for relative addressing into [Constant Integer Register](dx9-graphics-reference-asm-vs-registers-constant-integer.md) (c\#) or [Output Registers](dx9-graphics-reference-asm-vs-registers-vs-3-0.md) (o\#) inside the loop block.</span></span>
-   <span data-ttu-id="59069-126">\#x.x.x.x 會指定反復專案計數。</span><span class="sxs-lookup"><span data-stu-id="59069-126">i\#.x specifies the iteration count.</span></span> <span data-ttu-id="59069-127">合法範圍是 \[ 0，255 \] 。</span><span class="sxs-lookup"><span data-stu-id="59069-127">The legal range is \[0, 255\].</span></span> <span data-ttu-id="59069-128">請注意，此指令不會遞增或遞減 i \# . x 的值。</span><span class="sxs-lookup"><span data-stu-id="59069-128">Note that this instruction does not increment or decrement the value of i\#.x.</span></span>
-   <span data-ttu-id="59069-129">i. \# 指定 [迴圈計數器 Register](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (aL) Register 的初始值。</span><span class="sxs-lookup"><span data-stu-id="59069-129">i\#.y specifies the initial value of the [Loop Counter Register](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (aL) register.</span></span> <span data-ttu-id="59069-130">合法範圍是 \[ 0，255 \] 。</span><span class="sxs-lookup"><span data-stu-id="59069-130">The legal range is \[0, 255\].</span></span> <span data-ttu-id="59069-131">請注意，此指令不會遞增或遞減 i \# . y 的值。</span><span class="sxs-lookup"><span data-stu-id="59069-131">Note that this instruction does not increment or decrement the value of i\#.y.</span></span>
-   <span data-ttu-id="59069-132">i \# . z 指定步驟/stride 的大小。</span><span class="sxs-lookup"><span data-stu-id="59069-132">i\#.z specifies the step/stride size.</span></span> <span data-ttu-id="59069-133">合法範圍為 \[ -128、127 \] 。</span><span class="sxs-lookup"><span data-stu-id="59069-133">The legal range is \[-128, 127\].</span></span>
-   <span data-ttu-id="59069-134">i. \# 未使用，且必須設定為0。</span><span class="sxs-lookup"><span data-stu-id="59069-134">i\#.w is not used and must be set to 0.</span></span>
-   <span data-ttu-id="59069-135">迴圈區塊可能會進行嵌套。</span><span class="sxs-lookup"><span data-stu-id="59069-135">Loop blocks may be nested.</span></span> <span data-ttu-id="59069-136">請參閱 [流程式控制制的嵌套限制](dx9-graphics-reference-asm-vs-instructions-flow-control.md)。</span><span class="sxs-lookup"><span data-stu-id="59069-136">See [Flow Control Nesting Limits](dx9-graphics-reference-asm-vs-instructions-flow-control.md).</span></span>
-   <span data-ttu-id="59069-137">當進行嵌套時， [迴圈計數器 Register](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (aL) 是指立即封閉迴圈區塊。</span><span class="sxs-lookup"><span data-stu-id="59069-137">When nested, the value of the [Loop Counter Register](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (aL) refers to the immediate enclosing loop block.</span></span>
-   <span data-ttu-id="59069-138">迴圈區塊可以完全在 if \* 區塊內或完全圍繞它。</span><span class="sxs-lookup"><span data-stu-id="59069-138">Loop blocks are allowed to be either completely inside an if\* block or completely surrounding it.</span></span> <span data-ttu-id="59069-139">不允許任何 straddling。</span><span class="sxs-lookup"><span data-stu-id="59069-139">No straddling is allowed.</span></span>

## <a name="example"></a><span data-ttu-id="59069-140">範例</span><span class="sxs-lookup"><span data-stu-id="59069-140">Example</span></span>


```
loop aL, i3
    add r1, r0, c2[aL]
endloop
```



## <a name="related-topics"></a><span data-ttu-id="59069-141">相關主題</span><span class="sxs-lookup"><span data-stu-id="59069-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="59069-142">頂點著色器指示</span><span class="sxs-lookup"><span data-stu-id="59069-142">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




