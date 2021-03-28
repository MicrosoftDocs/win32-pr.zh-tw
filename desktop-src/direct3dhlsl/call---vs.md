---
title: 呼叫-vs
description: 對以提供的標籤標記的指令執行函式呼叫。 |呼叫-vs
ms.assetid: 3c1ec529-1ee4-40d9-8ce5-f8e7a61fde9c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c797e7ef6745f5710752fe059d2a2ff1f94a8aa3
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "103946024"
---
# <a name="call---vs"></a><span data-ttu-id="1b2c1-104">呼叫-vs</span><span class="sxs-lookup"><span data-stu-id="1b2c1-104">call - vs</span></span>

<span data-ttu-id="1b2c1-105">對以提供的標籤標記的指令執行函式呼叫。</span><span class="sxs-lookup"><span data-stu-id="1b2c1-105">Performs a function call to the instruction marked with the provided label.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b2c1-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="1b2c1-106">Syntax</span></span>



| <span data-ttu-id="1b2c1-107">呼叫 l\#</span><span class="sxs-lookup"><span data-stu-id="1b2c1-107">call l\#</span></span> |
|----------|



 

<span data-ttu-id="1b2c1-108">其中 l \# 是 [標籤-vs](label---vs.md) 標示要呼叫的副程式開頭。</span><span class="sxs-lookup"><span data-stu-id="1b2c1-108">where l\# is a [label - vs](label---vs.md) marking the beginning of the subroutine to be called.</span></span>

## <a name="remarks"></a><span data-ttu-id="1b2c1-109">備註</span><span class="sxs-lookup"><span data-stu-id="1b2c1-109">Remarks</span></span>



| <span data-ttu-id="1b2c1-110">頂點著色器版本</span><span class="sxs-lookup"><span data-stu-id="1b2c1-110">Vertex shader versions</span></span> | <span data-ttu-id="1b2c1-111">1\_1</span><span class="sxs-lookup"><span data-stu-id="1b2c1-111">1\_1</span></span> | <span data-ttu-id="1b2c1-112">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="1b2c1-112">2\_0</span></span> | <span data-ttu-id="1b2c1-113">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="1b2c1-113">2\_x</span></span> | <span data-ttu-id="1b2c1-114">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="1b2c1-114">2\_sw</span></span> | <span data-ttu-id="1b2c1-115">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="1b2c1-115">3\_0</span></span> | <span data-ttu-id="1b2c1-116">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="1b2c1-116">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="1b2c1-117">call</span><span class="sxs-lookup"><span data-stu-id="1b2c1-117">call</span></span>                   |      | <span data-ttu-id="1b2c1-118">x</span><span class="sxs-lookup"><span data-stu-id="1b2c1-118">x</span></span>    | <span data-ttu-id="1b2c1-119">x</span><span class="sxs-lookup"><span data-stu-id="1b2c1-119">x</span></span>    | <span data-ttu-id="1b2c1-120">x</span><span class="sxs-lookup"><span data-stu-id="1b2c1-120">x</span></span>     | <span data-ttu-id="1b2c1-121">x</span><span class="sxs-lookup"><span data-stu-id="1b2c1-121">x</span></span>    | <span data-ttu-id="1b2c1-122">x</span><span class="sxs-lookup"><span data-stu-id="1b2c1-122">x</span></span>     |



 

<span data-ttu-id="1b2c1-123">此指令會執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="1b2c1-123">This instruction does the following:</span></span>

1.  <span data-ttu-id="1b2c1-124">將下一個指令推送至傳回位址堆疊的位址。</span><span class="sxs-lookup"><span data-stu-id="1b2c1-124">Push address of the next instruction to the return address stack.</span></span>
2.  <span data-ttu-id="1b2c1-125">從標籤標記的指令繼續執行。</span><span class="sxs-lookup"><span data-stu-id="1b2c1-125">Continue execution from the instruction marked by the label.</span></span>

<span data-ttu-id="1b2c1-126">在頂點著色器 2 \_ 0 中，不允許使用嵌套呼叫。</span><span class="sxs-lookup"><span data-stu-id="1b2c1-126">In vertex shader 2\_0, nesting calls are not allowed.</span></span>

<span data-ttu-id="1b2c1-127">在頂點著色器 2 \_ x 中，嵌套深度會受限於 [**D3DVSHADERCAPS2 \_ 0**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dvshadercaps2_0) 結構的 StaticFlowControlDepth 元素。</span><span class="sxs-lookup"><span data-stu-id="1b2c1-127">In vertex shader 2\_x, the nesting depth is limited by the StaticFlowControlDepth element of the [**D3DVSHADERCAPS2\_0**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dvshadercaps2_0) structure.</span></span> <span data-ttu-id="1b2c1-128">如需詳細資訊，請參閱 [**GetDeviceCaps**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9-getdevicecaps)。</span><span class="sxs-lookup"><span data-stu-id="1b2c1-128">For more information, see [**GetDeviceCaps**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9-getdevicecaps).</span></span>

<span data-ttu-id="1b2c1-129">在頂點著色器 3 \_ 0 中，允許四個層級的呼叫嵌套。</span><span class="sxs-lookup"><span data-stu-id="1b2c1-129">In vertex shader 3\_0, four levels of call nesting are allowed.</span></span>

<span data-ttu-id="1b2c1-130">只允許轉送的呼叫。</span><span class="sxs-lookup"><span data-stu-id="1b2c1-130">Only forward calls are allowed.</span></span> <span data-ttu-id="1b2c1-131">這表示，在頂點著色器中，標籤的位置應該在呼叫指令參考之後。</span><span class="sxs-lookup"><span data-stu-id="1b2c1-131">This means that the location of the label inside the vertex shader should be after the call instruction referencing it.</span></span>

<span data-ttu-id="1b2c1-132">如果在 [迴圈](loop---vs.md)內部叫用呼叫指令 .。。[endloop](endloop---vs.md) 區塊，可在副程式內部存取 [迴圈計數器 Register](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (aL) 的值。</span><span class="sxs-lookup"><span data-stu-id="1b2c1-132">If a call instruction is invoked inside [loop](loop---vs.md)...[endloop](endloop---vs.md) block, the value of the [Loop Counter Register](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (aL) is accessible inside the subroutine.</span></span>

<span data-ttu-id="1b2c1-133">如果副程式參考 [迴圈計數器](dx9-graphics-reference-asm-vs-registers-loop-counter.md) 暫存器 (aL) 位於副程式之外，則每個對此副程式的呼叫實例都應該以 [迴圈](loop---vs.md)括住 .。。[endloop](endloop---vs.md) 組塊。</span><span class="sxs-lookup"><span data-stu-id="1b2c1-133">If a subroutine is referencing the [Loop Counter Register](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (aL) located outside of the subroutine, every instance of the call to this subroutine should be surrounded by a [loop](loop---vs.md)...[endloop](endloop---vs.md) block.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1b2c1-134">相關主題</span><span class="sxs-lookup"><span data-stu-id="1b2c1-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1b2c1-135">頂點著色器指示</span><span class="sxs-lookup"><span data-stu-id="1b2c1-135">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 
