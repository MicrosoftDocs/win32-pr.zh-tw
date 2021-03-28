---
title: breakp-vs
description: 有條件地在最接近的 endloop （vs 或 endrep）中斷目前的迴圈。請使用述詞註冊的其中一個元件做為條件，以判斷是否要執行指令。
ms.assetid: 940252a0-6f6a-45d8-9d2f-315cc97686ca
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: dbd0d5e20040bc2d353287eb4243c9e9d6d21dc8
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104022820"
---
# <a name="breakp---vs"></a><span data-ttu-id="22398-103">breakp-vs</span><span class="sxs-lookup"><span data-stu-id="22398-103">breakp - vs</span></span>

<span data-ttu-id="22398-104">有條件地中斷最接近 [endloop-vs](endloop---vs.md) 或 [endrep-vs](endrep---vs.md)的目前迴圈。使用述詞註冊的其中一個元件做為條件，以判斷是否要執行指令。</span><span class="sxs-lookup"><span data-stu-id="22398-104">Conditionally break out of the current loop at the nearest [endloop - vs](endloop---vs.md) or [endrep - vs](endrep---vs.md). Use one of the components of the predicate register as a condition to determine whether or not to perform the instruction.</span></span>

## <a name="syntax"></a><span data-ttu-id="22398-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="22398-105">Syntax</span></span>



| <span data-ttu-id="22398-106">breakp \[ ！ \]P。版</span><span class="sxs-lookup"><span data-stu-id="22398-106">breakp \[!\]p0.{x\</span></span>|<span data-ttu-id="22398-107">x</span><span class="sxs-lookup"><span data-stu-id="22398-107">y\</span></span>|<span data-ttu-id="22398-108">#a1</span><span class="sxs-lookup"><span data-stu-id="22398-108">z\</span></span>|<span data-ttu-id="22398-109">w</span><span class="sxs-lookup"><span data-stu-id="22398-109">w}</span></span> |
|-----------------------------|



 

<span data-ttu-id="22398-110">其中：</span><span class="sxs-lookup"><span data-stu-id="22398-110">Where:</span></span>

-   <span data-ttu-id="22398-111">\[!\] 選擇性的布林值。</span><span class="sxs-lookup"><span data-stu-id="22398-111">\[!\] optional boolean NOT.</span></span>
-   <span data-ttu-id="22398-112">p0 是述詞註冊。</span><span class="sxs-lookup"><span data-stu-id="22398-112">p0 is the predicate register.</span></span> <span data-ttu-id="22398-113">請參閱述詞 [註冊](dx9-graphics-reference-asm-vs-registers-predicate.md)。</span><span class="sxs-lookup"><span data-stu-id="22398-113">See [Predicate Register](dx9-graphics-reference-asm-vs-registers-predicate.md).</span></span>
-   <span data-ttu-id="22398-114">{x \| y \| z \| w} 是 p0 上所需的複寫 swizzle。</span><span class="sxs-lookup"><span data-stu-id="22398-114">{x\|y\|z\|w} is the required replicate swizzle on p0.</span></span>

## <a name="remarks"></a><span data-ttu-id="22398-115">備註</span><span class="sxs-lookup"><span data-stu-id="22398-115">Remarks</span></span>



| <span data-ttu-id="22398-116">頂點著色器版本</span><span class="sxs-lookup"><span data-stu-id="22398-116">Vertex shader versions</span></span> | <span data-ttu-id="22398-117">1\_1</span><span class="sxs-lookup"><span data-stu-id="22398-117">1\_1</span></span> | <span data-ttu-id="22398-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="22398-118">2\_0</span></span> | <span data-ttu-id="22398-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="22398-119">2\_x</span></span> | <span data-ttu-id="22398-120">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="22398-120">2\_sw</span></span> | <span data-ttu-id="22398-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="22398-121">3\_0</span></span> | <span data-ttu-id="22398-122">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="22398-122">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="22398-123">breakp</span><span class="sxs-lookup"><span data-stu-id="22398-123">breakp</span></span>                 |      |      | <span data-ttu-id="22398-124">x</span><span class="sxs-lookup"><span data-stu-id="22398-124">x</span></span>    | <span data-ttu-id="22398-125">x</span><span class="sxs-lookup"><span data-stu-id="22398-125">x</span></span>     | <span data-ttu-id="22398-126">x</span><span class="sxs-lookup"><span data-stu-id="22398-126">x</span></span>    | <span data-ttu-id="22398-127">x</span><span class="sxs-lookup"><span data-stu-id="22398-127">x</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="22398-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="22398-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="22398-129">頂點著色器指示</span><span class="sxs-lookup"><span data-stu-id="22398-129">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




