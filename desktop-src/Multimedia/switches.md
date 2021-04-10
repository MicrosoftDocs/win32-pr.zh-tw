---
title: 交換器
description: 交換器
ms.assetid: ab92d30d-97ab-4229-aed8-1080b6e6dc88
keywords:
- 音訊 mixers，控制項
- 音訊 mixers，切換
- mixers，控制項
- mixers，切換
- 切換控制項
- MIXERCONTROLDETAILS_BOOLEAN 結構
- 布林值控制項
- 按鈕控制項
- on/off 控制項
- mono 控制項
- 音量控制項
- 身歷聲增強型控制項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1d65bb2a14a0e7dc527fab0e628035839855934
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103842171"
---
# <a name="switches"></a><span data-ttu-id="0b823-115">交換器</span><span class="sxs-lookup"><span data-stu-id="0b823-115">Switches</span></span>

<span data-ttu-id="0b823-116">Switch 控制項是雙狀態參數。</span><span class="sxs-lookup"><span data-stu-id="0b823-116">The switch controls are two-state switches.</span></span> <span data-ttu-id="0b823-117">這些控制項使用 [**MIXERCONTROLDETAILS 的 \_ 布林值**](/previous-versions//dd757295(v=vs.85)) 結構來取得和設定控制項屬性。</span><span class="sxs-lookup"><span data-stu-id="0b823-117">These controls use the [**MIXERCONTROLDETAILS\_BOOLEAN**](/previous-versions//dd757295(v=vs.85)) structure to retrieve and set control properties.</span></span> <span data-ttu-id="0b823-118">下表說明參數的類型。</span><span class="sxs-lookup"><span data-stu-id="0b823-118">The following table describes the types of switches.</span></span>



| <span data-ttu-id="0b823-119">控制</span><span class="sxs-lookup"><span data-stu-id="0b823-119">Control</span></span>         | <span data-ttu-id="0b823-120">描述</span><span class="sxs-lookup"><span data-stu-id="0b823-120">Description</span></span>                                                                                                                                                                                                                           |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b823-121">Boolean</span><span class="sxs-lookup"><span data-stu-id="0b823-121">Boolean</span></span>         | <span data-ttu-id="0b823-122">泛型參數。</span><span class="sxs-lookup"><span data-stu-id="0b823-122">The generic switch.</span></span> <span data-ttu-id="0b823-123">可以設定為 **TRUE** 或 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="0b823-123">It can be set to **TRUE** or **FALSE**.</span></span>                                                                                                                                                                           |
| <span data-ttu-id="0b823-124">按鈕</span><span class="sxs-lookup"><span data-stu-id="0b823-124">Button</span></span>          | <span data-ttu-id="0b823-125">針對驅動程式應處理的所有按鈕，將其設定為 **TRUE** ，就好像已按下一樣。</span><span class="sxs-lookup"><span data-stu-id="0b823-125">Set to **TRUE** for all buttons that the driver should handle as though they had been pressed.</span></span> <span data-ttu-id="0b823-126">如果值為 **FALSE**，則不會採取任何動作。</span><span class="sxs-lookup"><span data-stu-id="0b823-126">If the value is **FALSE**, no action is taken.</span></span>                                                                                         |
| <span data-ttu-id="0b823-127">開啟/關閉</span><span class="sxs-lookup"><span data-stu-id="0b823-127">On/Off</span></span>          | <span data-ttu-id="0b823-128">替代參數，以除了用於布林值參數的其他圖形來表示。</span><span class="sxs-lookup"><span data-stu-id="0b823-128">An alternative switch that is represented by a graphic other than the one used for the Boolean switch.</span></span> <span data-ttu-id="0b823-129">可以設定為 ON 或 OFF。</span><span class="sxs-lookup"><span data-stu-id="0b823-129">It can be set to ON or OFF.</span></span>                                                                                                    |
| <span data-ttu-id="0b823-130">Mute</span><span class="sxs-lookup"><span data-stu-id="0b823-130">Mute</span></span>            | <span data-ttu-id="0b823-131">靜音音訊行 (隱藏線) 的資料流程，或允許播放音訊資料。</span><span class="sxs-lookup"><span data-stu-id="0b823-131">Mutes an audio line (suppressing the data flow of the line) or allows the audio data to play.</span></span> <span data-ttu-id="0b823-132">此參數經常用來協助控制送入混音器的行。</span><span class="sxs-lookup"><span data-stu-id="0b823-132">This switch is frequently used to help control the lines feeding into the mixer.</span></span>                                                        |
| <span data-ttu-id="0b823-133">Mono</span><span class="sxs-lookup"><span data-stu-id="0b823-133">Mono</span></span>            | <span data-ttu-id="0b823-134">切換身歷聲音訊線的 mono 和身歷聲輸出。</span><span class="sxs-lookup"><span data-stu-id="0b823-134">Switches between mono and stereo output for a stereo audio line.</span></span> <span data-ttu-id="0b823-135">設定為 [關閉] 可播放身歷聲資料作為個別的通道。</span><span class="sxs-lookup"><span data-stu-id="0b823-135">Set to OFF to play stereo data as separate channels.</span></span> <span data-ttu-id="0b823-136">設定為 ON 可將這兩個通道的資料結合成 mono 音訊行。</span><span class="sxs-lookup"><span data-stu-id="0b823-136">Set to ON to combine data from both channels into a mono audio line.</span></span>                                            |
| <span data-ttu-id="0b823-137">響度</span><span class="sxs-lookup"><span data-stu-id="0b823-137">Loudness</span></span>        | <span data-ttu-id="0b823-138">提升音訊線的低音量低音。</span><span class="sxs-lookup"><span data-stu-id="0b823-138">Boosts low-volume bass for an audio line.</span></span> <span data-ttu-id="0b823-139">設定為 [開啟] 可提升低音量的低音。</span><span class="sxs-lookup"><span data-stu-id="0b823-139">Set to ON to boost low-volume bass.</span></span> <span data-ttu-id="0b823-140">設定為 OFF 可將磁片區層級設定為 [正常]。</span><span class="sxs-lookup"><span data-stu-id="0b823-140">Set to OFF to set volume levels to normal.</span></span> <span data-ttu-id="0b823-141">提升量是硬體專用的。</span><span class="sxs-lookup"><span data-stu-id="0b823-141">The amount of boost is hardware specific.</span></span> <span data-ttu-id="0b823-142">如需詳細資訊，請參閱混音器裝置的檔。</span><span class="sxs-lookup"><span data-stu-id="0b823-142">For more information, see the documentation for your mixer device.</span></span> |
| <span data-ttu-id="0b823-143">立體增強</span><span class="sxs-lookup"><span data-stu-id="0b823-143">Stereo Enhanced</span></span> | <span data-ttu-id="0b823-144">增加身歷聲分隔。</span><span class="sxs-lookup"><span data-stu-id="0b823-144">Increases stereo separation.</span></span> <span data-ttu-id="0b823-145">設定為 [開啟] 以增加身歷聲分隔。</span><span class="sxs-lookup"><span data-stu-id="0b823-145">Set to ON to increase stereo separation.</span></span> <span data-ttu-id="0b823-146">如果沒有增強功能，請設定為 [關閉]。</span><span class="sxs-lookup"><span data-stu-id="0b823-146">Set to OFF for no enhancement.</span></span>                                                                                                                                  |



 

 

 