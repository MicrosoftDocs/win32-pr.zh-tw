---
title: 音訊輸出
description: 音訊輸出
ms.assetid: 2bedf804-c9fd-4a44-9289-e36a50517b7f
keywords:
- Windows Media Player，音訊輸出
- Windows Media Player，預設 DirectSound 裝置
- Windows Media Player、eConsole
- Windows Media Player、eMultimedia
- Windows Media Player、eCommunications
- 音訊輸出
- 預設 DirectSound 裝置
- eConsole
- eMultimedia
- eCommunications
- Windows Media Player ActiveX 控制項、音訊輸出
- Windows Media Player ActiveX 控制項，預設 DirectSound 裝置
- Windows Media Player ActiveX 控制項，eConsole
- Windows Media Player ActiveX 控制項，eMultimedia
- Windows Media Player ActiveX 控制項，eCommunications
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b41e5fc3284a054ba7497889eab80ec240c9801
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/25/2021
ms.locfileid: "110423858"
---
# <a name="audio-outputs"></a><span data-ttu-id="2b15a-118">音訊輸出</span><span class="sxs-lookup"><span data-stu-id="2b15a-118">Audio Outputs</span></span>

<span data-ttu-id="2b15a-119">Windows XP 中的主控台可讓使用者將名稱預設 DirectSound 裝置指派給特定音訊輸出裝置。</span><span class="sxs-lookup"><span data-stu-id="2b15a-119">The Control Panel in Windows XP enables the user to assign the name Default DirectSound Device to a particular audio output device.</span></span> <span data-ttu-id="2b15a-120">在 Windows Vista 中，主控台可讓使用者將三個名稱 (eConsole、eMultimedia 和 eCommunications) 指派給音訊輸出裝置。</span><span class="sxs-lookup"><span data-stu-id="2b15a-120">In Windows Vista, the Control Panel lets the user assign each of three names (eConsole, eMultimedia, and eCommunications) to an audio output device.</span></span> <span data-ttu-id="2b15a-121">這些名稱都可以指派給不同的裝置，或多個名稱可以指派給相同的裝置。</span><span class="sxs-lookup"><span data-stu-id="2b15a-121">These names can all be assigned to different devices, or multiple names can be assigned to the same device.</span></span> <span data-ttu-id="2b15a-122">下表顯示 Windows Media Player 和 Windows Media Player ActiveX 控制項如何選擇預設音訊輸出裝置。</span><span class="sxs-lookup"><span data-stu-id="2b15a-122">The following table shows how Windows Media Player and the Windows Media Player ActiveX control choose default audio output devices.</span></span>



|       &nbsp;                               | <span data-ttu-id="2b15a-123">Windows XP</span><span class="sxs-lookup"><span data-stu-id="2b15a-123">Windows XP</span></span>                                                                                                                                                                                | <span data-ttu-id="2b15a-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2b15a-124">Windows Vista</span></span>                                                                                                                                                              |
|--------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b15a-125">Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="2b15a-125">Windows Media Player</span></span>                 | <span data-ttu-id="2b15a-126">根據預設，播放程式會使用指定為預設 DirectSound 裝置的音訊裝置。</span><span class="sxs-lookup"><span data-stu-id="2b15a-126">By default, the Player uses the audio device designated as Default DirectSound Device.</span></span> <span data-ttu-id="2b15a-127">播放程式會提供一個對話方塊，讓使用者將播放機切換到不同的音訊裝置。</span><span class="sxs-lookup"><span data-stu-id="2b15a-127">The Player provides a dialog box that lets the user switch the Player to a different audio device.</span></span> | <span data-ttu-id="2b15a-128">根據預設，播放程式會使用指定為 eMultimedia 的音訊裝置。</span><span class="sxs-lookup"><span data-stu-id="2b15a-128">By default, the Player uses the audio device designated as eMultimedia.</span></span> <span data-ttu-id="2b15a-129">播放程式會提供一個對話方塊，讓使用者將播放機切換到不同的音訊裝置。</span><span class="sxs-lookup"><span data-stu-id="2b15a-129">The Player provides a dialog box that lets the user switch the Player to a different audio device.</span></span> |
| <span data-ttu-id="2b15a-130">Windows Media Player ActiveX 控制項</span><span class="sxs-lookup"><span data-stu-id="2b15a-130">Windows Media Player ActiveX control</span></span> | <span data-ttu-id="2b15a-131">根據預設，播放程式控制項會使用指定為預設 DirectSound 裝置的音訊裝置。</span><span class="sxs-lookup"><span data-stu-id="2b15a-131">By default, the Player control uses the audio device designated as Default DirectSound Device.</span></span> <span data-ttu-id="2b15a-132">音訊輸出裝置無法以程式設計方式變更。</span><span class="sxs-lookup"><span data-stu-id="2b15a-132">The audio output device cannot be changed programmatically.</span></span>                                | <span data-ttu-id="2b15a-133">根據預設，播放程式控制項會使用指定為 eMultimedia 的音訊裝置。</span><span class="sxs-lookup"><span data-stu-id="2b15a-133">By default, the Player control uses the audio device designated as eMultimedia.</span></span> <span data-ttu-id="2b15a-134">音訊輸出裝置無法以程式設計方式變更。</span><span class="sxs-lookup"><span data-stu-id="2b15a-134">The audio output device cannot be changed programmatically.</span></span>                                |



 

## <a name="related-topics"></a><span data-ttu-id="2b15a-135">相關主題</span><span class="sxs-lookup"><span data-stu-id="2b15a-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2b15a-136">**Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="2b15a-136">**Windows Media Player**</span></span>](windows-media-player.md)
</dt> </dl>

 

 




