---
title: 推子
description: 推子
ms.assetid: 2ca6be9f-9825-44d9-99c1-abcf6f0b42f7
keywords:
- 音訊 mixers，控制項
- 音訊 mixers、faders
- mixers，控制項
- mixers,faders
- 推子
- MIXERCONTROLDETAILS_UNSIGNED 結構
- 音量淡化控制項
- 低音磁片區淡化控制項
- 高音磁片區淡化控制項
- 圖形等化器控制項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd2b560b61a694089b947b0cfda7a54b486f1e3a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103933135"
---
# <a name="faders"></a><span data-ttu-id="044f4-113">推子</span><span class="sxs-lookup"><span data-stu-id="044f4-113">Faders</span></span>

<span data-ttu-id="044f4-114">Fader 控制項通常是可以向上或向下調整的垂直控制項。</span><span class="sxs-lookup"><span data-stu-id="044f4-114">The fader controls are typically vertical controls that can be adjusted up or down.</span></span> <span data-ttu-id="044f4-115">這些控制項具有線性尺規，並使用 [**MIXERCONTROLDETAILS 不 \_ 帶正負**](/previous-versions//dd757298(v=vs.85)) 號的結構來取得和設定控制項詳細資料。</span><span class="sxs-lookup"><span data-stu-id="044f4-115">These controls have a linear scale and use the [**MIXERCONTROLDETAILS\_UNSIGNED**](/previous-versions//dd757298(v=vs.85)) structure to retrieve and set control details.</span></span> <span data-ttu-id="044f4-116">下表描述 faders 的類型。</span><span class="sxs-lookup"><span data-stu-id="044f4-116">The following table describes the types of faders.</span></span>



| <span data-ttu-id="044f4-117">控制</span><span class="sxs-lookup"><span data-stu-id="044f4-117">Control</span></span>   | <span data-ttu-id="044f4-118">描述</span><span class="sxs-lookup"><span data-stu-id="044f4-118">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                     |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="044f4-119">推子</span><span class="sxs-lookup"><span data-stu-id="044f4-119">Fader</span></span>     | <span data-ttu-id="044f4-120">一般淡化控制項。</span><span class="sxs-lookup"><span data-stu-id="044f4-120">General fade control.</span></span> <span data-ttu-id="044f4-121">可接受的值範圍為0到65535。</span><span class="sxs-lookup"><span data-stu-id="044f4-121">The range of acceptable values is 0 through 65,535.</span></span>                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="044f4-122">磁碟區</span><span class="sxs-lookup"><span data-stu-id="044f4-122">Volume</span></span>    | <span data-ttu-id="044f4-123">一般磁片區淡化控制項。</span><span class="sxs-lookup"><span data-stu-id="044f4-123">General volume fade control.</span></span> <span data-ttu-id="044f4-124">可接受的值範圍為0到65535。</span><span class="sxs-lookup"><span data-stu-id="044f4-124">The range of acceptable values is 0 through 65,535.</span></span> <span data-ttu-id="044f4-125">如需變更此範圍的詳細資訊，請參閱混音器裝置的檔。</span><span class="sxs-lookup"><span data-stu-id="044f4-125">For information about changing this range, see the documentation for your mixer device.</span></span>                                                                                                                                                                                                                                        |
| <span data-ttu-id="044f4-126">低音</span><span class="sxs-lookup"><span data-stu-id="044f4-126">Bass</span></span>      | <span data-ttu-id="044f4-127">低音音量淡化控制項。</span><span class="sxs-lookup"><span data-stu-id="044f4-127">Bass volume fade control.</span></span> <span data-ttu-id="044f4-128">可接受的值範圍為0到65535。</span><span class="sxs-lookup"><span data-stu-id="044f4-128">The range of acceptable values is 0 through 65,535.</span></span> <span data-ttu-id="044f4-129">低音訊頻的限制是硬體專用的。</span><span class="sxs-lookup"><span data-stu-id="044f4-129">The limits of the bass frequency band are hardware specific.</span></span> <span data-ttu-id="044f4-130">如需有關頻外限制的詳細資訊，請參閱混音器裝置的檔。</span><span class="sxs-lookup"><span data-stu-id="044f4-130">For information about band limits, see the documentation for your mixer device.</span></span>                                                                                                                                                                                      |
| <span data-ttu-id="044f4-131">高音</span><span class="sxs-lookup"><span data-stu-id="044f4-131">Treble</span></span>    | <span data-ttu-id="044f4-132">高音磁片區淡化控制項。</span><span class="sxs-lookup"><span data-stu-id="044f4-132">Treble volume fade control.</span></span> <span data-ttu-id="044f4-133">可接受的值範圍為0到65535。</span><span class="sxs-lookup"><span data-stu-id="044f4-133">The range of acceptable values is 0 through 65,535.</span></span> <span data-ttu-id="044f4-134">高音訊率波段的限制是硬體專屬的。</span><span class="sxs-lookup"><span data-stu-id="044f4-134">The limits of the treble frequency band are hardware specific.</span></span> <span data-ttu-id="044f4-135">如需有關頻外限制的詳細資訊，請參閱混音器裝置的檔。</span><span class="sxs-lookup"><span data-stu-id="044f4-135">For information about the band limits, see the documentation for your mixer device.</span></span>                                                                                                                                                                              |
| <span data-ttu-id="044f4-136">等化器</span><span class="sxs-lookup"><span data-stu-id="044f4-136">Equalizer</span></span> | <span data-ttu-id="044f4-137">圖形等化器控制項。</span><span class="sxs-lookup"><span data-stu-id="044f4-137">Graphic equalizer control.</span></span> <span data-ttu-id="044f4-138">一個值區的可接受值範圍為0到65535。</span><span class="sxs-lookup"><span data-stu-id="044f4-138">The range of acceptable values for one band of the equalizer is 0 through 65,535.</span></span> <span data-ttu-id="044f4-139">等化器群組和其限制的數目是硬體專屬的。</span><span class="sxs-lookup"><span data-stu-id="044f4-139">The number of equalizer bands and their limits are hardware specific.</span></span> <span data-ttu-id="044f4-140">如需有關等化器的詳細資訊，請參閱混音器裝置的檔。</span><span class="sxs-lookup"><span data-stu-id="044f4-140">For information about the equalizer, see the documentation for your mixer device.</span></span> <span data-ttu-id="044f4-141">您可以使用 [**MIXERCONTROLDETAILS \_ LISTTEXT**](/previous-versions//dd757296(v=vs.85)) 結構來取得適用于等化器的文字標籤。</span><span class="sxs-lookup"><span data-stu-id="044f4-141">You can use the [**MIXERCONTROLDETAILS\_LISTTEXT**](/previous-versions//dd757296(v=vs.85)) structure to retrieve text labels for the equalizer.</span></span> |



 

 

 