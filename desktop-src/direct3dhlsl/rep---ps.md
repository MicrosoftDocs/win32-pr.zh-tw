---
title: rep-ps
description: 開始 a rep .。。endrep-ps block。
ms.assetid: vs|directx_sdk|~\rep___ps.htm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a6873a6aee9e31b1f28ba2755b1869cddb177306
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "103679124"
---
# <a name="rep---ps"></a><span data-ttu-id="208c7-103">rep-ps</span><span class="sxs-lookup"><span data-stu-id="208c7-103">rep - ps</span></span>

<span data-ttu-id="208c7-104">開始 a rep .。。[endrep-ps](endrep---ps.md) block。</span><span class="sxs-lookup"><span data-stu-id="208c7-104">Start a rep...[endrep - ps](endrep---ps.md) block.</span></span>

## <a name="syntax"></a><span data-ttu-id="208c7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="208c7-105">Syntax</span></span>



| <span data-ttu-id="208c7-106">rep\#</span><span class="sxs-lookup"><span data-stu-id="208c7-106">rep i\#</span></span> |
|---------|



 

<span data-ttu-id="208c7-107">其中 i \# 是指定. x 元件中重複計數的整數暫存器。</span><span class="sxs-lookup"><span data-stu-id="208c7-107">where i\# is an integer register that specifies the repeat count in the .x component.</span></span> <span data-ttu-id="208c7-108">請參閱 [常數整數註冊](dx9-graphics-reference-asm-ps-registers-constant-integer.md)。</span><span class="sxs-lookup"><span data-stu-id="208c7-108">See [Constant Integer Register](dx9-graphics-reference-asm-ps-registers-constant-integer.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="208c7-109">備註</span><span class="sxs-lookup"><span data-stu-id="208c7-109">Remarks</span></span>



| <span data-ttu-id="208c7-110">圖元著色器版本</span><span class="sxs-lookup"><span data-stu-id="208c7-110">Pixel shader versions</span></span> | <span data-ttu-id="208c7-111">1\_1</span><span class="sxs-lookup"><span data-stu-id="208c7-111">1\_1</span></span> | <span data-ttu-id="208c7-112">1\_2</span><span class="sxs-lookup"><span data-stu-id="208c7-112">1\_2</span></span> | <span data-ttu-id="208c7-113">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="208c7-113">1\_3</span></span> | <span data-ttu-id="208c7-114">1\_4</span><span class="sxs-lookup"><span data-stu-id="208c7-114">1\_4</span></span> | <span data-ttu-id="208c7-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="208c7-115">2\_0</span></span> | <span data-ttu-id="208c7-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="208c7-116">2\_x</span></span> | <span data-ttu-id="208c7-117">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="208c7-117">2\_sw</span></span> | <span data-ttu-id="208c7-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="208c7-118">3\_0</span></span> | <span data-ttu-id="208c7-119">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="208c7-119">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="208c7-120">代表</span><span class="sxs-lookup"><span data-stu-id="208c7-120">rep</span></span>                   |      |      |      |      |      | <span data-ttu-id="208c7-121">x</span><span class="sxs-lookup"><span data-stu-id="208c7-121">x</span></span>    | <span data-ttu-id="208c7-122">x</span><span class="sxs-lookup"><span data-stu-id="208c7-122">x</span></span>     | <span data-ttu-id="208c7-123">x</span><span class="sxs-lookup"><span data-stu-id="208c7-123">x</span></span>    | <span data-ttu-id="208c7-124">x</span><span class="sxs-lookup"><span data-stu-id="208c7-124">x</span></span>     |



 

-   <span data-ttu-id="208c7-125">\#x.x.x.x 會指定反復專案計數。</span><span class="sxs-lookup"><span data-stu-id="208c7-125">i\#.x specifies the iteration count.</span></span> <span data-ttu-id="208c7-126">合法範圍是 \[ 0，255 \] 。</span><span class="sxs-lookup"><span data-stu-id="208c7-126">The legal range is \[0, 255\].</span></span> <span data-ttu-id="208c7-127">請注意，此指令不會遞增或遞減 i \# . x 的值。</span><span class="sxs-lookup"><span data-stu-id="208c7-127">Note that this instruction does not increment or decrement the value of i\#.x.</span></span>
-   <span data-ttu-id="208c7-128">\#yzw 不是由重複區塊使用。</span><span class="sxs-lookup"><span data-stu-id="208c7-128">i\#.yzw are not used by the repeat block.</span></span>
-   <span data-ttu-id="208c7-129">重複區塊可能會進行嵌套。</span><span class="sxs-lookup"><span data-stu-id="208c7-129">Repeat blocks may be nested.</span></span> <span data-ttu-id="208c7-130">請參閱 [流程式控制制限制](dx9-graphics-reference-asm-ps-instructions-flow-control.md)。</span><span class="sxs-lookup"><span data-stu-id="208c7-130">See [Flow Control Limitations](dx9-graphics-reference-asm-ps-instructions-flow-control.md).</span></span>
-   <span data-ttu-id="208c7-131">重複區塊可以完全在 if \* 區塊內或完全圍繞它。</span><span class="sxs-lookup"><span data-stu-id="208c7-131">Repeat blocks are allowed to be either completely inside an if\* block or completely surrounding it.</span></span> <span data-ttu-id="208c7-132">不允許任何 straddling。</span><span class="sxs-lookup"><span data-stu-id="208c7-132">No straddling is allowed.</span></span>
-   <span data-ttu-id="208c7-133">針對不同或嵌套的 rep 表示，使用相同的 i， \# 每個迴圈都會根據指定的計數逐一進行反覆運算。</span><span class="sxs-lookup"><span data-stu-id="208c7-133">Using the same i\# for different or nested rep instructions is fine - each loop will iterate based on the specified count.</span></span>

## <a name="example"></a><span data-ttu-id="208c7-134">範例</span><span class="sxs-lookup"><span data-stu-id="208c7-134">Example</span></span>


```
rep i2
    add r0, r0, c0
endrep  
```



## <a name="related-topics"></a><span data-ttu-id="208c7-135">相關主題</span><span class="sxs-lookup"><span data-stu-id="208c7-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="208c7-136">圖元著色器指示</span><span class="sxs-lookup"><span data-stu-id="208c7-136">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




