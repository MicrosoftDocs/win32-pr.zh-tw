---
title: 米
description: 米
ms.assetid: 11a98d2a-7cdd-4249-bba9-7edc51d7f8b0
keywords:
- 音訊 mixers，控制項
- 音訊 mixers，計量
- mixers，控制項
- mixers，計量
- 計量控制項
- MIXERCONTROLDETAILS_BOOLEAN 結構
- MIXERCONTROLDETAILS_SIGNED 結構
- MIXERCONTROLDETAILS_UNSIGNED 結構
- 布林值控制項
- 尖峰控制
- 簽署的控制項
- 未簽署的控制項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f36f1bebfca22b963e5c1eb6fede3f2786b35199
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104463144"
---
# <a name="meters"></a><span data-ttu-id="93f24-115">米</span><span class="sxs-lookup"><span data-stu-id="93f24-115">Meters</span></span>

<span data-ttu-id="93f24-116">量測計控制項會測量透過音訊行傳遞的資料。</span><span class="sxs-lookup"><span data-stu-id="93f24-116">The meter controls measure data passing through an audio line.</span></span> <span data-ttu-id="93f24-117">這些控制項使用 [**MIXERCONTROLDETAILS 的 \_ 布林值**](/previous-versions//dd757295(v=vs.85))、 [**MIXERCONTROLDETAILS \_ 簽署**](/previous-versions//dd757297(v=vs.85))和 [**MIXERCONTROLDETAILS 不 \_ 帶正負**](/previous-versions//dd757298(v=vs.85)) 號的結構來取得和設定控制項屬性。</span><span class="sxs-lookup"><span data-stu-id="93f24-117">These controls use the [**MIXERCONTROLDETAILS\_BOOLEAN**](/previous-versions//dd757295(v=vs.85)), [**MIXERCONTROLDETAILS\_SIGNED**](/previous-versions//dd757297(v=vs.85)), and [**MIXERCONTROLDETAILS\_UNSIGNED**](/previous-versions//dd757298(v=vs.85)) structures to retrieve and set control properties.</span></span> <span data-ttu-id="93f24-118">下表描述計量的類型。</span><span class="sxs-lookup"><span data-stu-id="93f24-118">The following table describes the types of meters.</span></span>



| <span data-ttu-id="93f24-119">控制</span><span class="sxs-lookup"><span data-stu-id="93f24-119">Control</span></span>  | <span data-ttu-id="93f24-120">描述</span><span class="sxs-lookup"><span data-stu-id="93f24-120">Description</span></span>                                                                                                                                            |
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93f24-121">Boolean</span><span class="sxs-lookup"><span data-stu-id="93f24-121">Boolean</span></span>  | <span data-ttu-id="93f24-122">測量整數值是否為 FALSE/OFF (零) 或 TRUE/ON (非零) 。</span><span class="sxs-lookup"><span data-stu-id="93f24-122">Measures whether an integer value is FALSE/OFF (zero) or TRUE/ON (nonzero).</span></span>                                                                            |
| <span data-ttu-id="93f24-123">Peak</span><span class="sxs-lookup"><span data-stu-id="93f24-123">Peak</span></span>     | <span data-ttu-id="93f24-124">從0開始測量正面和負面方向的偏離。</span><span class="sxs-lookup"><span data-stu-id="93f24-124">Measures the deflection from 0 in both the positive and negative directions.</span></span> <span data-ttu-id="93f24-125">尖峰計量的整數值範圍是–32768到32767。</span><span class="sxs-lookup"><span data-stu-id="93f24-125">The range of integer values for the peak meter is –32,768 through 32,767.</span></span> |
| <span data-ttu-id="93f24-126">簽署人</span><span class="sxs-lookup"><span data-stu-id="93f24-126">Signed</span></span>   | <span data-ttu-id="93f24-127">測量介於-231 到 (231 – 1) 範圍內的整數值。</span><span class="sxs-lookup"><span data-stu-id="93f24-127">Measures integer values in the range of –231 through (231 – 1).</span></span> <span data-ttu-id="93f24-128">混音器驅動程式會定義此計量的限制。</span><span class="sxs-lookup"><span data-stu-id="93f24-128">The mixer driver defines the limits of this meter.</span></span>                                     |
| <span data-ttu-id="93f24-129">不帶正負號</span><span class="sxs-lookup"><span data-stu-id="93f24-129">Unsigned</span></span> | <span data-ttu-id="93f24-130">測量0到 (232 – 1) 範圍內的整數值。</span><span class="sxs-lookup"><span data-stu-id="93f24-130">Measures integer values in the range of 0 through (232 – 1).</span></span> <span data-ttu-id="93f24-131">混音器驅動程式會定義此計量的限制。</span><span class="sxs-lookup"><span data-stu-id="93f24-131">The mixer driver defines the limits of this meter.</span></span>                                        |



 

 

 