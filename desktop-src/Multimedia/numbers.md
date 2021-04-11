---
title: " (Windows 多媒體) 的數位"
description: 數字
ms.assetid: d416c4c2-a3e1-45a2-9ae1-82050a5e471b
keywords:
- 音訊 mixers，控制項
- 音訊 mixers，數位
- mixers，控制項
- mixers，數位
- 數位控制項
- MIXERCONTROLDETAILS_SIGNED 結構
- MIXERCONTROLDETAILS_UNSIGNED 結構
- 分貝控制項
- 控制百分比
- 簽署的控制項
- 未簽署的控制項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f02c4ffd40f1058fae51af3798135840394be918
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104093623"
---
# <a name="numbers-windows-multimedia"></a><span data-ttu-id="6dc3f-114"> (Windows 多媒體) 的數位</span><span class="sxs-lookup"><span data-stu-id="6dc3f-114">Numbers (Windows Multimedia)</span></span>

<span data-ttu-id="6dc3f-115">Number 控制項可讓使用者輸入與線條相關聯的數值資料。</span><span class="sxs-lookup"><span data-stu-id="6dc3f-115">The number controls allow the user to enter numerical data associated with a line.</span></span> <span data-ttu-id="6dc3f-116">數值資料會以帶正負號的整數、不帶正負號的整數或整數分貝值表示。</span><span class="sxs-lookup"><span data-stu-id="6dc3f-116">The numerical data is expressed as signed integers, unsigned integers, or integer decibel values.</span></span> <span data-ttu-id="6dc3f-117">這些控制項使用 [**MIXERCONTROLDETAILS \_ 簽署**](/previous-versions//dd757297(v=vs.85)) 和 [**MIXERCONTROLDETAILS 不 \_ 帶正負**](/previous-versions//dd757298(v=vs.85)) 號的結構來取得和設定控制項屬性。</span><span class="sxs-lookup"><span data-stu-id="6dc3f-117">These controls use the [**MIXERCONTROLDETAILS\_SIGNED**](/previous-versions//dd757297(v=vs.85)) and [**MIXERCONTROLDETAILS\_UNSIGNED**](/previous-versions//dd757298(v=vs.85)) structures to retrieve and set control properties.</span></span> <span data-ttu-id="6dc3f-118">下表描述數位控制項的類型。</span><span class="sxs-lookup"><span data-stu-id="6dc3f-118">The following table describes the types of number controls.</span></span>



| <span data-ttu-id="6dc3f-119">控制</span><span class="sxs-lookup"><span data-stu-id="6dc3f-119">Control</span></span>  | <span data-ttu-id="6dc3f-120">描述</span><span class="sxs-lookup"><span data-stu-id="6dc3f-120">Description</span></span>                                                                                                                         |
|----------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6dc3f-121">簽署人</span><span class="sxs-lookup"><span data-stu-id="6dc3f-121">Signed</span></span>   | <span data-ttu-id="6dc3f-122">允許在–231到 (231 – 1) 範圍中輸入的整數值。</span><span class="sxs-lookup"><span data-stu-id="6dc3f-122">Allows integer values entered in the range of – 231 through (231 –1).</span></span>                                                               |
| <span data-ttu-id="6dc3f-123">不帶正負號</span><span class="sxs-lookup"><span data-stu-id="6dc3f-123">Unsigned</span></span> | <span data-ttu-id="6dc3f-124">允許從0到 (232 – 1) 的範圍輸入整數值。</span><span class="sxs-lookup"><span data-stu-id="6dc3f-124">Allows integer values entered in the range of 0 through (232 –1).</span></span>                                                                   |
| <span data-ttu-id="6dc3f-125">分貝</span><span class="sxs-lookup"><span data-stu-id="6dc3f-125">Decibel</span></span>  | <span data-ttu-id="6dc3f-126">允許輸入整數分貝值（以分貝為單位）。</span><span class="sxs-lookup"><span data-stu-id="6dc3f-126">Allows integer decibel values to be entered, in tenths of decibels.</span></span> <span data-ttu-id="6dc3f-127">此控制項的值範圍為–32768到32767。</span><span class="sxs-lookup"><span data-stu-id="6dc3f-127">The range of values for this control is –32,768 through 32,767.</span></span> |
| <span data-ttu-id="6dc3f-128">百分比</span><span class="sxs-lookup"><span data-stu-id="6dc3f-128">Percent</span></span>  | <span data-ttu-id="6dc3f-129">允許將值輸入為百分比。</span><span class="sxs-lookup"><span data-stu-id="6dc3f-129">Allows values to be entered as percentages.</span></span>                                                                                         |



 

 

 
