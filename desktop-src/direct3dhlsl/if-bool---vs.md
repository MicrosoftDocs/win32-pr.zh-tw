---
title: if bool-vs
description: 啟動 if .。。還。。。endif-vs block。
ms.assetid: d77e2f81-400c-4997-9c34-426b6e6f47be
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 261ff572cbaf519cc0099f3ab68d1a0becca706f
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104022792"
---
# <a name="if-bool---vs"></a><span data-ttu-id="57222-103">if bool-vs</span><span class="sxs-lookup"><span data-stu-id="57222-103">if bool - vs</span></span>

<span data-ttu-id="57222-104">啟動 if .。。[其他](else---vs.md).。。[endif-vs](endif---vs.md) block。</span><span class="sxs-lookup"><span data-stu-id="57222-104">Starts an if...[else](else---vs.md)...[endif - vs](endif---vs.md) block.</span></span>

## <a name="syntax"></a><span data-ttu-id="57222-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="57222-105">Syntax</span></span>



| <span data-ttu-id="57222-106">if bool</span><span class="sxs-lookup"><span data-stu-id="57222-106">if bool</span></span> |
|---------|



 

<span data-ttu-id="57222-107">其中 bool 是 bool 暫存器號碼。</span><span class="sxs-lookup"><span data-stu-id="57222-107">where bool is a bool register number.</span></span> <span data-ttu-id="57222-108">請參閱 [常數布林值](dx9-graphics-reference-asm-vs-registers-constant-boolean.md)暫存器。</span><span class="sxs-lookup"><span data-stu-id="57222-108">See [Constant Boolean Register](dx9-graphics-reference-asm-vs-registers-constant-boolean.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="57222-109">備註</span><span class="sxs-lookup"><span data-stu-id="57222-109">Remarks</span></span>



| <span data-ttu-id="57222-110">頂點著色器版本</span><span class="sxs-lookup"><span data-stu-id="57222-110">Vertex shader versions</span></span> | <span data-ttu-id="57222-111">1\_1</span><span class="sxs-lookup"><span data-stu-id="57222-111">1\_1</span></span> | <span data-ttu-id="57222-112">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="57222-112">2\_0</span></span> | <span data-ttu-id="57222-113">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="57222-113">2\_x</span></span> | <span data-ttu-id="57222-114">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="57222-114">2\_sw</span></span> | <span data-ttu-id="57222-115">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="57222-115">3\_0</span></span> | <span data-ttu-id="57222-116">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="57222-116">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="57222-117">if bool</span><span class="sxs-lookup"><span data-stu-id="57222-117">if bool</span></span>                |      | <span data-ttu-id="57222-118">x</span><span class="sxs-lookup"><span data-stu-id="57222-118">x</span></span>    | <span data-ttu-id="57222-119">x</span><span class="sxs-lookup"><span data-stu-id="57222-119">x</span></span>    | <span data-ttu-id="57222-120">x</span><span class="sxs-lookup"><span data-stu-id="57222-120">x</span></span>     | <span data-ttu-id="57222-121">x</span><span class="sxs-lookup"><span data-stu-id="57222-121">x</span></span>    | <span data-ttu-id="57222-122">x</span><span class="sxs-lookup"><span data-stu-id="57222-122">x</span></span>     |



 

<span data-ttu-id="57222-123">如果 if 語句中的來源布林值暫存器為 true，則會執行 if 語句所括住的程式碼和相符的 else。</span><span class="sxs-lookup"><span data-stu-id="57222-123">If the source Boolean register in the if statement is true, the code enclosed by the if statement and the matching else is run.</span></span> <span data-ttu-id="57222-124">否則，程式碼會以 [其他](else---vs.md).。。[endif-執行 vs](endif---vs.md) 語句。</span><span class="sxs-lookup"><span data-stu-id="57222-124">Otherwise, the code enclosed by the [else](else---vs.md)...[endif - vs](endif---vs.md) statements is run.</span></span> <span data-ttu-id="57222-125">此指令會使用一個指令位置。</span><span class="sxs-lookup"><span data-stu-id="57222-125">This instruction consumes one instruction slot.</span></span>

<span data-ttu-id="57222-126">如果區塊可以進行嵌套。</span><span class="sxs-lookup"><span data-stu-id="57222-126">if blocks can be nested.</span></span>

<span data-ttu-id="57222-127">If 區塊無法跨迴圈區塊。</span><span class="sxs-lookup"><span data-stu-id="57222-127">An if block cannot straddle a loop block.</span></span>

## <a name="example"></a><span data-ttu-id="57222-128">範例</span><span class="sxs-lookup"><span data-stu-id="57222-128">Example</span></span>

<span data-ttu-id="57222-129">此指令提供條件式靜態流程式控制制。</span><span class="sxs-lookup"><span data-stu-id="57222-129">This instruction provides conditional static flow control.</span></span>


```
defb b2, TRUE

...

if b2
// Instructions to run if b2 is nonzero

else
// Instructions to run otherwise

endif
```



## <a name="related-topics"></a><span data-ttu-id="57222-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="57222-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="57222-131">頂點著色器指示</span><span class="sxs-lookup"><span data-stu-id="57222-131">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> <dt>

[<span data-ttu-id="57222-132">else-vs</span><span class="sxs-lookup"><span data-stu-id="57222-132">else - vs</span></span>](else---vs.md)
</dt> <dt>

[<span data-ttu-id="57222-133">endif-vs</span><span class="sxs-lookup"><span data-stu-id="57222-133">endif - vs</span></span>](endif---vs.md)
</dt> </dl>

 

 




