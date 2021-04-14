---
title: 呼叫-ps
description: 對以提供的標籤標記的指令執行函式呼叫。 |呼叫-ps
ms.assetid: d5f5e5a1-f205-477d-a11b-ff9eeeec6c95
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 27be29c478afdf92c29fefd16a82319e0899d2ec
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104991970"
---
# <a name="call---ps"></a><span data-ttu-id="c1247-104">呼叫-ps</span><span class="sxs-lookup"><span data-stu-id="c1247-104">call - ps</span></span>

<span data-ttu-id="c1247-105">對以提供的標籤標記的指令執行函式呼叫。</span><span class="sxs-lookup"><span data-stu-id="c1247-105">Performs a function call to the instruction marked with the provided label.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1247-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="c1247-106">Syntax</span></span>



| <span data-ttu-id="c1247-107">呼叫 l\#</span><span class="sxs-lookup"><span data-stu-id="c1247-107">call l\#</span></span> |
|----------|



 

<span data-ttu-id="c1247-108">其中：</span><span class="sxs-lookup"><span data-stu-id="c1247-108">Where:</span></span>

-   <span data-ttu-id="c1247-109">l \# 是標示要呼叫的副程式開頭的 [標籤（ps）](label---ps.md) 。</span><span class="sxs-lookup"><span data-stu-id="c1247-109">l\# is a [label - ps](label---ps.md) marking the beginning of the subroutine to be called.</span></span>

## <a name="remarks"></a><span data-ttu-id="c1247-110">備註</span><span class="sxs-lookup"><span data-stu-id="c1247-110">Remarks</span></span>



| <span data-ttu-id="c1247-111">圖元著色器版本</span><span class="sxs-lookup"><span data-stu-id="c1247-111">Pixel shader versions</span></span> | <span data-ttu-id="c1247-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="c1247-112">1\_1</span></span> | <span data-ttu-id="c1247-113">1\_2</span><span class="sxs-lookup"><span data-stu-id="c1247-113">1\_2</span></span> | <span data-ttu-id="c1247-114">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="c1247-114">1\_3</span></span> | <span data-ttu-id="c1247-115">1\_4</span><span class="sxs-lookup"><span data-stu-id="c1247-115">1\_4</span></span> | <span data-ttu-id="c1247-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c1247-116">2\_0</span></span> | <span data-ttu-id="c1247-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="c1247-117">2\_x</span></span> | <span data-ttu-id="c1247-118">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="c1247-118">2\_sw</span></span> | <span data-ttu-id="c1247-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c1247-119">3\_0</span></span> | <span data-ttu-id="c1247-120">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="c1247-120">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="c1247-121">call</span><span class="sxs-lookup"><span data-stu-id="c1247-121">call</span></span>                  |      |      |      |      |      | <span data-ttu-id="c1247-122">x</span><span class="sxs-lookup"><span data-stu-id="c1247-122">x</span></span>    | <span data-ttu-id="c1247-123">x</span><span class="sxs-lookup"><span data-stu-id="c1247-123">x</span></span>     | <span data-ttu-id="c1247-124">x</span><span class="sxs-lookup"><span data-stu-id="c1247-124">x</span></span>    | <span data-ttu-id="c1247-125">x</span><span class="sxs-lookup"><span data-stu-id="c1247-125">x</span></span>     |



 

<span data-ttu-id="c1247-126">此指令會執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="c1247-126">This instruction does the following:</span></span>

1.  <span data-ttu-id="c1247-127">將下一個指令推送至傳回位址堆疊的位址。</span><span class="sxs-lookup"><span data-stu-id="c1247-127">Push address of the next instruction to the return address stack.</span></span>
2.  <span data-ttu-id="c1247-128">從標籤標記的指令繼續執行。</span><span class="sxs-lookup"><span data-stu-id="c1247-128">Continue execution from the instruction marked by the label.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c1247-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="c1247-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c1247-130">圖元著色器指示</span><span class="sxs-lookup"><span data-stu-id="c1247-130">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




