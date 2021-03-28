---
title: breakp-ps
description: 有條件地在最接近的 endloop-ps 或 endrep-ps 中斷目前的迴圈。 使用述詞註冊的其中一個元件做為條件，以判斷是否要執行指令。
ms.assetid: be219239-fccb-4561-8b71-083c47ba915b
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6e358debb2377f08574997acd96c11f83d32e66c
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104373822"
---
# <a name="breakp---ps"></a><span data-ttu-id="29503-104">breakp-ps</span><span class="sxs-lookup"><span data-stu-id="29503-104">breakp - ps</span></span>

<span data-ttu-id="29503-105">有條件地在最接近的 [endloop-ps](endloop---ps.md) 或 [endrep-ps](endrep---ps.md)中斷目前的迴圈。</span><span class="sxs-lookup"><span data-stu-id="29503-105">Conditionally break out of the current loop at the nearest [endloop - ps](endloop---ps.md) or [endrep - ps](endrep---ps.md).</span></span> <span data-ttu-id="29503-106">使用述詞註冊的其中一個元件做為條件，以判斷是否要執行指令。</span><span class="sxs-lookup"><span data-stu-id="29503-106">Use one of the components of the predicate register as a condition to determine whether or not to perform the instruction.</span></span>

## <a name="syntax"></a><span data-ttu-id="29503-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="29503-107">Syntax</span></span>



| <span data-ttu-id="29503-108">breakp \[ ！ \]P。版</span><span class="sxs-lookup"><span data-stu-id="29503-108">breakp \[!\]p0.{x\</span></span>|<span data-ttu-id="29503-109">x</span><span class="sxs-lookup"><span data-stu-id="29503-109">y\</span></span>|<span data-ttu-id="29503-110">#a1</span><span class="sxs-lookup"><span data-stu-id="29503-110">z\</span></span>|<span data-ttu-id="29503-111">w</span><span class="sxs-lookup"><span data-stu-id="29503-111">w}</span></span> |
|-----------------------------|



 

<span data-ttu-id="29503-112">其中：</span><span class="sxs-lookup"><span data-stu-id="29503-112">Where:</span></span>

-   <span data-ttu-id="29503-113">\[!\] 這是選擇性的否定修飾詞。</span><span class="sxs-lookup"><span data-stu-id="29503-113">\[!\] is an optional negate modifier.</span></span>
-   <span data-ttu-id="29503-114">p0 是述詞 [註冊](dx9-graphics-reference-asm-ps-registers-predicate.md)。</span><span class="sxs-lookup"><span data-stu-id="29503-114">p0 is the [Predicate Register](dx9-graphics-reference-asm-ps-registers-predicate.md).</span></span>
-   <span data-ttu-id="29503-115">{x \| y \| z \| w} 是 p0 上所需的複寫 swizzle。</span><span class="sxs-lookup"><span data-stu-id="29503-115">{x\|y\|z\|w} is the required replicate swizzle on p0.</span></span>

## <a name="remarks"></a><span data-ttu-id="29503-116">備註</span><span class="sxs-lookup"><span data-stu-id="29503-116">Remarks</span></span>



| <span data-ttu-id="29503-117">圖元著色器版本</span><span class="sxs-lookup"><span data-stu-id="29503-117">Pixel shader versions</span></span> | <span data-ttu-id="29503-118">1\_1</span><span class="sxs-lookup"><span data-stu-id="29503-118">1\_1</span></span> | <span data-ttu-id="29503-119">1\_2</span><span class="sxs-lookup"><span data-stu-id="29503-119">1\_2</span></span> | <span data-ttu-id="29503-120">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="29503-120">1\_3</span></span> | <span data-ttu-id="29503-121">1\_4</span><span class="sxs-lookup"><span data-stu-id="29503-121">1\_4</span></span> | <span data-ttu-id="29503-122">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="29503-122">2\_0</span></span> | <span data-ttu-id="29503-123">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="29503-123">2\_x</span></span> | <span data-ttu-id="29503-124">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="29503-124">2\_sw</span></span> | <span data-ttu-id="29503-125">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="29503-125">3\_0</span></span> | <span data-ttu-id="29503-126">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="29503-126">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="29503-127">breakp</span><span class="sxs-lookup"><span data-stu-id="29503-127">breakp</span></span>                |      |      |      |      |      | <span data-ttu-id="29503-128">x</span><span class="sxs-lookup"><span data-stu-id="29503-128">x</span></span>    | <span data-ttu-id="29503-129">x</span><span class="sxs-lookup"><span data-stu-id="29503-129">x</span></span>     | <span data-ttu-id="29503-130">x</span><span class="sxs-lookup"><span data-stu-id="29503-130">x</span></span>    | <span data-ttu-id="29503-131">x</span><span class="sxs-lookup"><span data-stu-id="29503-131">x</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="29503-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="29503-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="29503-133">圖元著色器指示</span><span class="sxs-lookup"><span data-stu-id="29503-133">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




