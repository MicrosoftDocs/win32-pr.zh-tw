---
title: if bool-ps
description: If 區塊的開頭。
ms.assetid: cff53072-1c73-4cf8-9ecd-11032a9c4bbb
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 92c3158a09aeb871ef367133c07278b0f3b87390
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "103679103"
---
# <a name="if-bool---ps"></a><span data-ttu-id="157f8-103">if bool-ps</span><span class="sxs-lookup"><span data-stu-id="157f8-103">if bool - ps</span></span>

<span data-ttu-id="157f8-104">If 區塊的開頭。</span><span class="sxs-lookup"><span data-stu-id="157f8-104">Start of an if block.</span></span>

## <a name="syntax"></a><span data-ttu-id="157f8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="157f8-105">Syntax</span></span>



| <span data-ttu-id="157f8-106">if bool</span><span class="sxs-lookup"><span data-stu-id="157f8-106">if bool</span></span> |
|---------|



 

<span data-ttu-id="157f8-107">其中：</span><span class="sxs-lookup"><span data-stu-id="157f8-107">Where:</span></span>

-   <span data-ttu-id="157f8-108">bool 是布林值 (布林值) register 號碼。</span><span class="sxs-lookup"><span data-stu-id="157f8-108">bool is a bool (Boolean) register number.</span></span> <span data-ttu-id="157f8-109">請參閱 [常數布林值](dx9-graphics-reference-asm-ps-registers-constant-boolean.md)暫存器。</span><span class="sxs-lookup"><span data-stu-id="157f8-109">See [Constant Boolean Register](dx9-graphics-reference-asm-ps-registers-constant-boolean.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="157f8-110">備註</span><span class="sxs-lookup"><span data-stu-id="157f8-110">Remarks</span></span>



| <span data-ttu-id="157f8-111">圖元著色器版本</span><span class="sxs-lookup"><span data-stu-id="157f8-111">Pixel shader versions</span></span> | <span data-ttu-id="157f8-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="157f8-112">1\_1</span></span> | <span data-ttu-id="157f8-113">1\_2</span><span class="sxs-lookup"><span data-stu-id="157f8-113">1\_2</span></span> | <span data-ttu-id="157f8-114">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="157f8-114">1\_3</span></span> | <span data-ttu-id="157f8-115">1\_4</span><span class="sxs-lookup"><span data-stu-id="157f8-115">1\_4</span></span> | <span data-ttu-id="157f8-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="157f8-116">2\_0</span></span> | <span data-ttu-id="157f8-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="157f8-117">2\_x</span></span> | <span data-ttu-id="157f8-118">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="157f8-118">2\_sw</span></span> | <span data-ttu-id="157f8-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="157f8-119">3\_0</span></span> | <span data-ttu-id="157f8-120">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="157f8-120">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="157f8-121">if bool</span><span class="sxs-lookup"><span data-stu-id="157f8-121">if bool</span></span>               |      |      |      |      |      | <span data-ttu-id="157f8-122">x</span><span class="sxs-lookup"><span data-stu-id="157f8-122">x</span></span>    | <span data-ttu-id="157f8-123">x</span><span class="sxs-lookup"><span data-stu-id="157f8-123">x</span></span>     | <span data-ttu-id="157f8-124">x</span><span class="sxs-lookup"><span data-stu-id="157f8-124">x</span></span>    | <span data-ttu-id="157f8-125">x</span><span class="sxs-lookup"><span data-stu-id="157f8-125">x</span></span>     |



 

<span data-ttu-id="157f8-126">如果 if 語句中的來源布林值暫存器為 true，則會執行 if 語句所括住的程式碼和對應的 [endif-ps](endif---ps.md) 或 [else-ps](else---ps.md) 。</span><span class="sxs-lookup"><span data-stu-id="157f8-126">If the source Boolean register in the if statement is true, the code enclosed by the if statement and the matching [endif - ps](endif---ps.md) or [else - ps](else---ps.md) is executed.</span></span> <span data-ttu-id="157f8-127">否則，程式碼是由 else-ps 所括住 .。。endif-執行的 ps 語句。</span><span class="sxs-lookup"><span data-stu-id="157f8-127">Otherwise, the code enclosed by the else - ps...endif - ps statements is executed.</span></span> <span data-ttu-id="157f8-128">此指令會使用一個指令位置。</span><span class="sxs-lookup"><span data-stu-id="157f8-128">This instruction consumes one instruction slot.</span></span>

<span data-ttu-id="157f8-129">如果可以嵌套 if 區塊，則為。</span><span class="sxs-lookup"><span data-stu-id="157f8-129">An if block can be nested.</span></span>

<span data-ttu-id="157f8-130">If 區塊無法跨迴圈區塊。</span><span class="sxs-lookup"><span data-stu-id="157f8-130">An if block cannot straddle a loop block.</span></span>

<span data-ttu-id="157f8-131">If 區塊後面可以接著語句區塊、/或 [其他-ps](else---ps.md) 指令，以及/或 [endif-ps](endif---ps.md) 指令。</span><span class="sxs-lookup"><span data-stu-id="157f8-131">An if block can be followed by a statement block, and/or an [else - ps](else---ps.md) instruction, and/or an [endif - ps](endif---ps.md) instruction.</span></span>

## <a name="example"></a><span data-ttu-id="157f8-132">範例</span><span class="sxs-lookup"><span data-stu-id="157f8-132">Example</span></span>

<span data-ttu-id="157f8-133">此指令提供條件式靜態流程式控制制。</span><span class="sxs-lookup"><span data-stu-id="157f8-133">This instruction provides conditional static flow control.</span></span>


```
defb b3, true

if b3
// Instructions to run if b3 is nonzero
else
// Instructions to run otherwise
endif
```



## <a name="related-topics"></a><span data-ttu-id="157f8-134">相關主題</span><span class="sxs-lookup"><span data-stu-id="157f8-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="157f8-135">圖元著色器指示</span><span class="sxs-lookup"><span data-stu-id="157f8-135">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> <dt>

[<span data-ttu-id="157f8-136">其他-ps</span><span class="sxs-lookup"><span data-stu-id="157f8-136">else - ps</span></span>](else---ps.md)
</dt> <dt>

[<span data-ttu-id="157f8-137">endif-ps</span><span class="sxs-lookup"><span data-stu-id="157f8-137">endif - ps</span></span>](endif---ps.md)
</dt> </dl>

 

 




