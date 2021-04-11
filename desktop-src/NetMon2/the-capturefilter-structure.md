---
description: 在網路監視器中，capture 篩選器是由 CAPTUREFILTER 結構所定義。
ms.assetid: 03cd35f2-4da5-4ef6-b73f-0bf6e0e33135
title: CAPTUREFILTER 結構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3962ef9828ce13a1d03c58e4d7744d2854624858
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943507"
---
# <a name="the-capturefilter-structure"></a><span data-ttu-id="76fa4-103">CAPTUREFILTER 結構</span><span class="sxs-lookup"><span data-stu-id="76fa4-103">The CAPTUREFILTER Structure</span></span>

<span data-ttu-id="76fa4-104">在網路監視器中， [capture 篩選器](capture-filters.md) 是由 [**CAPTUREFILTER**](capturefilter.md) 結構所定義。</span><span class="sxs-lookup"><span data-stu-id="76fa4-104">In Network Monitor, the [capture filter](capture-filters.md) is defined by the [**CAPTUREFILTER**](capturefilter.md) structure.</span></span> <span data-ttu-id="76fa4-105">旗標、值和運算式的遺漏或組合，會決定網路監視器驅動程式會將哪些框架傳遞或卸載。</span><span class="sxs-lookup"><span data-stu-id="76fa4-105">The absence or combination of flags, values, and expressions determines which frames will be passed on or dropped by the Network Monitor driver.</span></span> <span data-ttu-id="76fa4-106">下圖顯示「capture 濾波器分析」的三個區域： Etype/SAP、address 和 pattern match。</span><span class="sxs-lookup"><span data-stu-id="76fa4-106">The following illustration shows the three areas of the capture filter analysis: Etype/SAP, address, and pattern match.</span></span>

![capture 篩選器分析的三個區域](images/capfilter.png)

<span data-ttu-id="76fa4-108">下表列出每個 capture 篩選元素的函式。</span><span class="sxs-lookup"><span data-stu-id="76fa4-108">The following table lists the function of each capture filter element.</span></span>



| <span data-ttu-id="76fa4-109">Filter 元素</span><span class="sxs-lookup"><span data-stu-id="76fa4-109">Filter element</span></span>                                       | <span data-ttu-id="76fa4-110">動作</span><span class="sxs-lookup"><span data-stu-id="76fa4-110">Action</span></span>                                                                                                                                                                                                       |
|------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="76fa4-111">Etype/SAP</span><span class="sxs-lookup"><span data-stu-id="76fa4-111">Etype/SAP</span></span>](writing-etypesap-filter-portion.md)     | <span data-ttu-id="76fa4-112">評估 Etype/SAP 設定。</span><span class="sxs-lookup"><span data-stu-id="76fa4-112">Evaluates Etype/SAP settings.</span></span> <span data-ttu-id="76fa4-113">旗標的組合可決定要包含或排除的設定類型或值。</span><span class="sxs-lookup"><span data-stu-id="76fa4-113">The combination of flags determines which setting types or values are included or excluded.</span></span>                                                                                    |
| [<span data-ttu-id="76fa4-114">位址</span><span class="sxs-lookup"><span data-stu-id="76fa4-114">Address</span></span>](writing-addresstable-filter-portion.md)   | <span data-ttu-id="76fa4-115">評估來源和目的地位址和位址組。</span><span class="sxs-lookup"><span data-stu-id="76fa4-115">Evaluates source and destination addresses and address pairs.</span></span> <span data-ttu-id="76fa4-116">不同的旗標組合可決定要包含或排除的個別值或位址組組合。</span><span class="sxs-lookup"><span data-stu-id="76fa4-116">Different combinations of flags determine which individual values or combinations of address pairs are included or excluded.</span></span>                   |
| [<span data-ttu-id="76fa4-117">模式比對</span><span class="sxs-lookup"><span data-stu-id="76fa4-117">Pattern Match</span></span>](writing-the-patternmatch-filter.md) | <span data-ttu-id="76fa4-118">定義框架內的複雜模式比對。</span><span class="sxs-lookup"><span data-stu-id="76fa4-118">Defines complex pattern matches within a frame.</span></span> <span data-ttu-id="76fa4-119">針對不同的類型和位移提供旗標。</span><span class="sxs-lookup"><span data-stu-id="76fa4-119">Flags are provided for different types and offsets.</span></span> <span data-ttu-id="76fa4-120">您可以結合模式比對與邏輯 AND 或 or 運算子語句。</span><span class="sxs-lookup"><span data-stu-id="76fa4-120">You can combine pattern matches with logical AND or OR operator statements.</span></span>                              |
| [<span data-ttu-id="76fa4-121">裁剪</span><span class="sxs-lookup"><span data-stu-id="76fa4-121">Clipping</span></span>](clipping-a-frame.md)                     | <span data-ttu-id="76fa4-122">以各種位元組值所指定的方式來剪輯框架。</span><span class="sxs-lookup"><span data-stu-id="76fa4-122">Clips frames in a manner specified by various byte values.</span></span> <span data-ttu-id="76fa4-123">您只能使用這個專案來裁剪所有框架，或將它與其他 capture 濾波器元素搭配使用;例如，若要尋找並裁剪單一畫面格。</span><span class="sxs-lookup"><span data-stu-id="76fa4-123">You can use only this element to clip all frames or use it with other capture filter elements; for example, to find and then clip a single frame.</span></span> |
| [<span data-ttu-id="76fa4-124">**觸發**</span><span class="sxs-lookup"><span data-stu-id="76fa4-124">**Trigger**</span></span>](trigger.md)                           | <span data-ttu-id="76fa4-125">此 capture 篩選元素已淘汰。</span><span class="sxs-lookup"><span data-stu-id="76fa4-125">This capture filter element is obsolete.</span></span> <span data-ttu-id="76fa4-126">觸發程式已不再是 capture 篩選準則的一部分;它們現在包含在自己的 BLOB 標籤中，這些標記是個別指定的。</span><span class="sxs-lookup"><span data-stu-id="76fa4-126">Triggers are no longer part of a capture filter; they are now contained in their own BLOB tags, which are specified separately.</span></span>                                     |



 

<span data-ttu-id="76fa4-127">畫面格會針對 capture 篩選器的所有三個部分進行評估。</span><span class="sxs-lookup"><span data-stu-id="76fa4-127">A frame is evaluated against all three portions of the capture filter.</span></span> <span data-ttu-id="76fa4-128">因此，成功傳輸的框架必須通過每個元素。</span><span class="sxs-lookup"><span data-stu-id="76fa4-128">Therefore, a successfully transmitted frame must pass each element.</span></span> <span data-ttu-id="76fa4-129">請注意，網路監視器驅動程式會將上述三個元素中的任何專案都評估為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="76fa4-129">Be aware that the Network Monitor driver evaluates the absence of any of the three elements as **TRUE**.</span></span> <span data-ttu-id="76fa4-130">例如，驅動程式會將不存在的 Etype/SAP 區段評估為「所有具有任何 Etype/SAP 值的框架都有效」。</span><span class="sxs-lookup"><span data-stu-id="76fa4-130">For example, the driver evaluates the absence of an Etype/SAP section as "ALL frames with the ANY Etype/SAP value are valid."</span></span>

 

 



