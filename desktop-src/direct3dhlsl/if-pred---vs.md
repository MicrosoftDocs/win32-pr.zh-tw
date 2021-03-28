---
title: 如果 pred-vs
description: If pred 的開頭-vs .。。else-vs .。。endif-vs block，其條件取自述詞登錄的內容。
ms.assetid: 03f60ca3-cda0-4653-8582-74d1a75e0aee
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0a1a36bb0c6c68f5132757719bbc7e37fbc71501
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104313635"
---
# <a name="if-pred---vs"></a><span data-ttu-id="6b922-103">如果 pred-vs</span><span class="sxs-lookup"><span data-stu-id="6b922-103">if pred - vs</span></span>

<span data-ttu-id="6b922-104">If pred 的開頭-vs .。。[else-vs](else---vs.md).。。[endif-vs](endif---vs.md) block，其條件取自述詞登錄的內容。</span><span class="sxs-lookup"><span data-stu-id="6b922-104">Start of an if pred - vs...[else - vs](else---vs.md)...[endif - vs](endif---vs.md) block, with the condition taken from the content of the predicate register.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b922-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6b922-105">Syntax</span></span>



| <span data-ttu-id="6b922-106">如果 \[ ！ \]pred. replicateSwizzle</span><span class="sxs-lookup"><span data-stu-id="6b922-106">if \[!\]pred.replicateSwizzle</span></span> |
|-------------------------------|



 

<span data-ttu-id="6b922-107">其中：</span><span class="sxs-lookup"><span data-stu-id="6b922-107">Where:</span></span>

-   <span data-ttu-id="6b922-108">\[!\] 選擇性的 NOT 修飾詞。</span><span class="sxs-lookup"><span data-stu-id="6b922-108">\[!\] an optional NOT modifier.</span></span> <span data-ttu-id="6b922-109">這會修改述詞註冊中的值。</span><span class="sxs-lookup"><span data-stu-id="6b922-109">This modifies the value in the predicate register.</span></span>
-   <span data-ttu-id="6b922-110">pred 是述詞 register，p0。</span><span class="sxs-lookup"><span data-stu-id="6b922-110">pred is the predicate register, p0.</span></span> <span data-ttu-id="6b922-111">請參閱述詞 [註冊](dx9-graphics-reference-asm-vs-registers-predicate.md)。</span><span class="sxs-lookup"><span data-stu-id="6b922-111">See [Predicate Register](dx9-graphics-reference-asm-vs-registers-predicate.md).</span></span>
-   <span data-ttu-id="6b922-112">replicateSwizzle 是將 (或複寫) 複製到所有四個元件 (swizzled) 的單一元件。</span><span class="sxs-lookup"><span data-stu-id="6b922-112">replicateSwizzle is a single component that is copied (or replicated) to all four components (swizzled).</span></span> <span data-ttu-id="6b922-113">有效的元件為： x、y、z、w 或 r、g、b、a。</span><span class="sxs-lookup"><span data-stu-id="6b922-113">Valid components are: x, y, z, w or r, g, b, a.</span></span>

## <a name="remarks"></a><span data-ttu-id="6b922-114">備註</span><span class="sxs-lookup"><span data-stu-id="6b922-114">Remarks</span></span>



| <span data-ttu-id="6b922-115">頂點著色器版本</span><span class="sxs-lookup"><span data-stu-id="6b922-115">Vertex shader versions</span></span> | <span data-ttu-id="6b922-116">1\_1</span><span class="sxs-lookup"><span data-stu-id="6b922-116">1\_1</span></span> | <span data-ttu-id="6b922-117">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="6b922-117">2\_0</span></span> | <span data-ttu-id="6b922-118">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="6b922-118">2\_x</span></span> | <span data-ttu-id="6b922-119">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="6b922-119">2\_sw</span></span> | <span data-ttu-id="6b922-120">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="6b922-120">3\_0</span></span> | <span data-ttu-id="6b922-121">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="6b922-121">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="6b922-122">如果 pred</span><span class="sxs-lookup"><span data-stu-id="6b922-122">if pred</span></span>                |      |      | <span data-ttu-id="6b922-123">x</span><span class="sxs-lookup"><span data-stu-id="6b922-123">x</span></span>    | <span data-ttu-id="6b922-124">x</span><span class="sxs-lookup"><span data-stu-id="6b922-124">x</span></span>     | <span data-ttu-id="6b922-125">x</span><span class="sxs-lookup"><span data-stu-id="6b922-125">x</span></span>    | <span data-ttu-id="6b922-126">x</span><span class="sxs-lookup"><span data-stu-id="6b922-126">x</span></span>     |



 

<span data-ttu-id="6b922-127">此指令是用來根據述詞登錄的通道，略過程式碼區塊。</span><span class="sxs-lookup"><span data-stu-id="6b922-127">This instruction is used to skip a block of code, based on a channel of the predicate register.</span></span> <span data-ttu-id="6b922-128">每個 if \_ pred 區塊都必須以 else 或 endif 指令結尾。</span><span class="sxs-lookup"><span data-stu-id="6b922-128">Each if\_pred block must end with an else or endif instruction.</span></span>

<span data-ttu-id="6b922-129">限制包含：</span><span class="sxs-lookup"><span data-stu-id="6b922-129">Restrictions include:</span></span>

<span data-ttu-id="6b922-130">如果 \_ pred 區塊可以進行嵌套，則為。</span><span class="sxs-lookup"><span data-stu-id="6b922-130">if\_pred blocks can be nested.</span></span> <span data-ttu-id="6b922-131">這會計算為動態嵌套深度的總計，以及 [if \_ 複合](if-comp---vs.md) 區塊。</span><span class="sxs-lookup"><span data-stu-id="6b922-131">This counts to the total dynamic nesting depth along with [if\_comp](if-comp---vs.md) blocks.</span></span>

<span data-ttu-id="6b922-132">如果 \_ pred 區塊無法跨迴圈區塊，則應該完全在其中，或將它括住。</span><span class="sxs-lookup"><span data-stu-id="6b922-132">An if\_pred block cannot straddle a loop block, it should be either completely inside it or surround it.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6b922-133">相關主題</span><span class="sxs-lookup"><span data-stu-id="6b922-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6b922-134">頂點著色器指示</span><span class="sxs-lookup"><span data-stu-id="6b922-134">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




