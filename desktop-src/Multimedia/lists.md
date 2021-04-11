---
title: 清單
description: 清單
ms.assetid: 89fb4457-307a-4693-94d4-57f57c422d1e
keywords:
- 音訊 mixers，控制項
- 音訊 mixers，清單
- mixers，控制項
- mixers，清單
- 清單控制項
- MIXERCONTROLDETAILS_BOOLEAN 結構
- MIXERCONTROLDETAILS_LISTTEXT 結構
- 單一選取控制項
- 多重選取控制項
- 混音器控制項
- '多工器 (MUX) '
- 'MUX (多工器) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d475816d7090ee241a1508cc054b12742c4ab27
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314779"
---
# <a name="lists"></a><span data-ttu-id="5db77-115">清單</span><span class="sxs-lookup"><span data-stu-id="5db77-115">Lists</span></span>

<span data-ttu-id="5db77-116">清單控制項提供複雜音訊線的單一選取或多重選取狀態。</span><span class="sxs-lookup"><span data-stu-id="5db77-116">The list controls provide single-select or multiple-select states for complex audio lines.</span></span> <span data-ttu-id="5db77-117">這些控制項使用 [**MIXERCONTROLDETAILS 的 \_ 布林值**](/previous-versions//dd757295(v=vs.85)) 結構來取得和設定控制項屬性。</span><span class="sxs-lookup"><span data-stu-id="5db77-117">These controls use the [**MIXERCONTROLDETAILS\_BOOLEAN**](/previous-versions//dd757295(v=vs.85)) structure to retrieve and set control properties.</span></span> <span data-ttu-id="5db77-118">[**MIXERCONTROLDETAILS \_ LISTTEXT**](/previous-versions//dd757296(v=vs.85))結構也用來取得多重專案控制項的所有文字描述。</span><span class="sxs-lookup"><span data-stu-id="5db77-118">The [**MIXERCONTROLDETAILS\_LISTTEXT**](/previous-versions//dd757296(v=vs.85)) structure is also used to retrieve all text descriptions of a multiple-item control.</span></span> <span data-ttu-id="5db77-119">下表描述清單控制項的類型。</span><span class="sxs-lookup"><span data-stu-id="5db77-119">The following table describes the types of list controls.</span></span>



| <span data-ttu-id="5db77-120">控制</span><span class="sxs-lookup"><span data-stu-id="5db77-120">Control</span></span>           | <span data-ttu-id="5db77-121">描述</span><span class="sxs-lookup"><span data-stu-id="5db77-121">Description</span></span>                                                                                                                                                                                                                                                                      |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5db77-122">單一選取</span><span class="sxs-lookup"><span data-stu-id="5db77-122">Single-select</span></span>     | <span data-ttu-id="5db77-123">一次將控制項選取範圍限制為一個專案。</span><span class="sxs-lookup"><span data-stu-id="5db77-123">Restricts the control selection to one item at a time.</span></span> <span data-ttu-id="5db77-124">與多工器控制項不同的是，此控制項可以用來控制音訊來源行以上的行。</span><span class="sxs-lookup"><span data-stu-id="5db77-124">Unlike the multiplexer control, this control can be used to control more than audio source lines.</span></span> <span data-ttu-id="5db77-125">例如，您可以使用此控制項，從混音器裝置所支援的篩選器清單中選取低傳遞篩選。</span><span class="sxs-lookup"><span data-stu-id="5db77-125">For example, you could use this control to select a low-pass filter from a list of filters supported by a mixer device.</span></span> |
| <span data-ttu-id="5db77-126">多工器 (MUX) </span><span class="sxs-lookup"><span data-stu-id="5db77-126">Multiplexer (MUX)</span></span> | <span data-ttu-id="5db77-127">將一次行選取範圍限制為一個原始程式列。</span><span class="sxs-lookup"><span data-stu-id="5db77-127">Restricts the line selection to one source line at a time.</span></span>                                                                                                                                                                                                                       |
| <span data-ttu-id="5db77-128">多重選取</span><span class="sxs-lookup"><span data-stu-id="5db77-128">Multiple-select</span></span>   | <span data-ttu-id="5db77-129">可讓使用者同時選取清單中的多個專案。</span><span class="sxs-lookup"><span data-stu-id="5db77-129">Allows the user to select multiple items from a list simultaneously.</span></span> <span data-ttu-id="5db77-130">不同于混音器控制項，多重選取控制項可以用來控制音訊來源行以上。</span><span class="sxs-lookup"><span data-stu-id="5db77-130">Unlike the mixer control, the multiple-select control can be used to control more than audio source lines.</span></span>                                                                                                  |
| <span data-ttu-id="5db77-131">攪拌機</span><span class="sxs-lookup"><span data-stu-id="5db77-131">Mixer</span></span>             | <span data-ttu-id="5db77-132">允許使用者同時從清單中選取來源行。</span><span class="sxs-lookup"><span data-stu-id="5db77-132">Allows the user to select source lines from a list simultaneously.</span></span>                                                                                                                                                                                                               |



 

 

 