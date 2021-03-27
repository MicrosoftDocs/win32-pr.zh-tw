---
title: 若為 pred-ps
description: If bool-ps 的開頭 .。。其他-ps .。。endif-ps 區塊，其中的條件取自述詞登錄的內容。
ms.assetid: 7b43bf71-a2e9-468f-805f-620de065db08
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ead7c5936550715d48ee1ef6a3938b6219558823
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "103679116"
---
# <a name="if-pred---ps"></a><span data-ttu-id="ad3cd-103">若為 pred-ps</span><span class="sxs-lookup"><span data-stu-id="ad3cd-103">if pred - ps</span></span>

<span data-ttu-id="ad3cd-104">[If bool-ps](if-bool---ps.md)的開頭 .。。[其他-ps](else---ps.md).。。[endif-ps](endif---ps.md)區塊，其中的條件取自述詞登錄的內容。</span><span class="sxs-lookup"><span data-stu-id="ad3cd-104">Start of an [if bool - ps](if-bool---ps.md)...[else - ps](else---ps.md)...[endif - ps](endif---ps.md) block, with the condition taken from the content of the predicate register.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad3cd-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ad3cd-105">Syntax</span></span>



| <span data-ttu-id="ad3cd-106">如果 \[ ！ \]pred. replicateSwizzle</span><span class="sxs-lookup"><span data-stu-id="ad3cd-106">if \[!\]pred.replicateSwizzle</span></span> |
|-------------------------------|



 

<span data-ttu-id="ad3cd-107">其中：</span><span class="sxs-lookup"><span data-stu-id="ad3cd-107">Where:</span></span>

-   <span data-ttu-id="ad3cd-108">\[!\] 這是選擇性的 NOT 修飾詞。</span><span class="sxs-lookup"><span data-stu-id="ad3cd-108">\[!\] is an optional NOT modifier.</span></span> <span data-ttu-id="ad3cd-109">這會修改述詞註冊中的值。</span><span class="sxs-lookup"><span data-stu-id="ad3cd-109">This modifies the value in the predicate register.</span></span>
-   <span data-ttu-id="ad3cd-110">pred 是述詞 [註冊](dx9-graphics-reference-asm-ps-registers-predicate.md)。</span><span class="sxs-lookup"><span data-stu-id="ad3cd-110">pred is the [Predicate Register](dx9-graphics-reference-asm-ps-registers-predicate.md).</span></span>
-   <span data-ttu-id="ad3cd-111">replicateSwizzle 是將 (或複寫) 複製到所有四個元件 (swizzled) 的單一元件。</span><span class="sxs-lookup"><span data-stu-id="ad3cd-111">replicateSwizzle is a single component that is copied (or replicated) to all four components (swizzled).</span></span> <span data-ttu-id="ad3cd-112">有效的元件為： \[ x、y、z、w \] 或 \[ r、g、b、a \] 。</span><span class="sxs-lookup"><span data-stu-id="ad3cd-112">Valid components are: \[x, y, z, w\] or \[r, g, b, a\].</span></span>

## <a name="remarks"></a><span data-ttu-id="ad3cd-113">備註</span><span class="sxs-lookup"><span data-stu-id="ad3cd-113">Remarks</span></span>



| <span data-ttu-id="ad3cd-114">圖元著色器版本</span><span class="sxs-lookup"><span data-stu-id="ad3cd-114">Pixel shader versions</span></span> | <span data-ttu-id="ad3cd-115">1\_1</span><span class="sxs-lookup"><span data-stu-id="ad3cd-115">1\_1</span></span> | <span data-ttu-id="ad3cd-116">1\_2</span><span class="sxs-lookup"><span data-stu-id="ad3cd-116">1\_2</span></span> | <span data-ttu-id="ad3cd-117">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="ad3cd-117">1\_3</span></span> | <span data-ttu-id="ad3cd-118">1\_4</span><span class="sxs-lookup"><span data-stu-id="ad3cd-118">1\_4</span></span> | <span data-ttu-id="ad3cd-119">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="ad3cd-119">2\_0</span></span> | <span data-ttu-id="ad3cd-120">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="ad3cd-120">2\_x</span></span> | <span data-ttu-id="ad3cd-121">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="ad3cd-121">2\_sw</span></span> | <span data-ttu-id="ad3cd-122">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="ad3cd-122">3\_0</span></span> | <span data-ttu-id="ad3cd-123">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="ad3cd-123">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="ad3cd-124">如果 \_ pred</span><span class="sxs-lookup"><span data-stu-id="ad3cd-124">if\_pred</span></span>              |      |      |      |      |      | <span data-ttu-id="ad3cd-125">x</span><span class="sxs-lookup"><span data-stu-id="ad3cd-125">x</span></span>    | <span data-ttu-id="ad3cd-126">x</span><span class="sxs-lookup"><span data-stu-id="ad3cd-126">x</span></span>     | <span data-ttu-id="ad3cd-127">x</span><span class="sxs-lookup"><span data-stu-id="ad3cd-127">x</span></span>    | <span data-ttu-id="ad3cd-128">x</span><span class="sxs-lookup"><span data-stu-id="ad3cd-128">x</span></span>     |



 

<span data-ttu-id="ad3cd-129">此指令是用來根據述詞登錄的通道，略過程式碼區塊。</span><span class="sxs-lookup"><span data-stu-id="ad3cd-129">This instruction is used to skip a block of code, based on a channel of the predicate register.</span></span> <span data-ttu-id="ad3cd-130">每個 if \_ pred 區塊都必須以 [else-ps](else---ps.md) 或 [endif-ps](endif---ps.md) 指令結尾。</span><span class="sxs-lookup"><span data-stu-id="ad3cd-130">Each if\_pred block must end with an [else - ps](else---ps.md) or [endif - ps](endif---ps.md) instruction.</span></span>

<span data-ttu-id="ad3cd-131">限制包含：</span><span class="sxs-lookup"><span data-stu-id="ad3cd-131">Restrictions include:</span></span>

<span data-ttu-id="ad3cd-132">如果 \_ pred 區塊可以進行嵌套，則為。</span><span class="sxs-lookup"><span data-stu-id="ad3cd-132">if\_pred blocks can be nested.</span></span> <span data-ttu-id="ad3cd-133">這會計算為動態嵌套深度的總計，以及 [if \_ 複合](if-comp---ps.md) 區塊。</span><span class="sxs-lookup"><span data-stu-id="ad3cd-133">This counts to the total dynamic nesting depth along with [if\_comp](if-comp---ps.md) blocks.</span></span>

<span data-ttu-id="ad3cd-134">如果 \_ pred 區塊無法跨迴圈區塊，則應該完全在其中，或將它括住。</span><span class="sxs-lookup"><span data-stu-id="ad3cd-134">An if\_pred block cannot straddle a loop block; it should either be completely inside it or surround it.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ad3cd-135">相關主題</span><span class="sxs-lookup"><span data-stu-id="ad3cd-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ad3cd-136">圖元著色器指示</span><span class="sxs-lookup"><span data-stu-id="ad3cd-136">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




