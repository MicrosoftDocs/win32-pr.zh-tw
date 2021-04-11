---
title: 停止、暫停及重新開機播放
description: 停止、暫停及重新開機播放
ms.assetid: 39751342-63bc-4e68-bf9e-38665db8a05c
keywords:
- 波形音訊，停止播放
- 波形-音訊介面，停止播放
- 播放波形-音訊檔案，停止播放
- 波形音訊，暫停播放
- 波形-音訊介面，暫停播放
- 播放波形-音訊檔案，暫停播放
- 波形音訊，重新開機播放
- 波形-音訊介面，重新開機播放
- 播放波形-音訊檔案，重新開機播放
- waveOutPause 函式
- waveOutReset 函式
- waveOutRestart 函式
- 停止波形-音訊播放
- 暫停波形-音訊播放
- 重新開機波形-音訊播放
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d6a4756a08317923056114259588a95bc62e97f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104092657"
---
# <a name="stopping-pausing-and-restarting-playback"></a><span data-ttu-id="4b5b5-118">停止、暫停及重新開機播放</span><span class="sxs-lookup"><span data-stu-id="4b5b5-118">Stopping, Pausing, and Restarting Playback</span></span>

<span data-ttu-id="4b5b5-119">您可以在波形音訊播放時停止或暫停播放。</span><span class="sxs-lookup"><span data-stu-id="4b5b5-119">You can stop or pause playback while waveform audio is playing.</span></span> <span data-ttu-id="4b5b5-120">暫停播放之後，您可以重新開機。</span><span class="sxs-lookup"><span data-stu-id="4b5b5-120">After playback has been paused, you can restart it.</span></span> <span data-ttu-id="4b5b5-121">Windows 提供下列功能來控制波形音訊播放。</span><span class="sxs-lookup"><span data-stu-id="4b5b5-121">Windows provides the following functions for controlling waveform-audio playback.</span></span>



| <span data-ttu-id="4b5b5-122">函式</span><span class="sxs-lookup"><span data-stu-id="4b5b5-122">Function</span></span>                                 | <span data-ttu-id="4b5b5-123">描述</span><span class="sxs-lookup"><span data-stu-id="4b5b5-123">Description</span></span>                                                                                 |
|------------------------------------------|---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4b5b5-124">**waveOutPause**</span><span class="sxs-lookup"><span data-stu-id="4b5b5-124">**waveOutPause**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutpause)     | <span data-ttu-id="4b5b5-125">暫停波形音訊輸出裝置上的播放。</span><span class="sxs-lookup"><span data-stu-id="4b5b5-125">Pauses playback on a waveform-audio output device.</span></span>                                          |
| [<span data-ttu-id="4b5b5-126">**waveOutReset**</span><span class="sxs-lookup"><span data-stu-id="4b5b5-126">**waveOutReset**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset)     | <span data-ttu-id="4b5b5-127">停止在波形音訊輸出裝置上播放，並將所有暫止的資料區塊標示為已完成。</span><span class="sxs-lookup"><span data-stu-id="4b5b5-127">Stops playback on a waveform-audio output device and marks all pending data blocks as done.</span></span> |
| [<span data-ttu-id="4b5b5-128">**waveOutRestart**</span><span class="sxs-lookup"><span data-stu-id="4b5b5-128">**waveOutRestart**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutrestart) | <span data-ttu-id="4b5b5-129">繼續在暫停的波形音訊輸出裝置上播放。</span><span class="sxs-lookup"><span data-stu-id="4b5b5-129">Resumes playback on a paused waveform-audio output device.</span></span>                                  |



 

<span data-ttu-id="4b5b5-130">使用 [**waveOutPause**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutpause) 暫停波形音訊裝置可能不會立即進行;驅動程式可能會在暫停播放之前完成播放目前的區塊。</span><span class="sxs-lookup"><span data-stu-id="4b5b5-130">Pausing a waveform-audio device by using [**waveOutPause**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutpause) might not be instantaneous; the driver may finish playing the current block before pausing playback.</span></span>

<span data-ttu-id="4b5b5-131">一般來說，只要使用 [**waveOutWrite**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite) 函式來傳送第一個波形-音訊資料區塊，就會開始播放波形音訊裝置。</span><span class="sxs-lookup"><span data-stu-id="4b5b5-131">Generally, as soon as the first waveform-audio data block is sent by using the [**waveOutWrite**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite) function, the waveform-audio device begins playing.</span></span> <span data-ttu-id="4b5b5-132">如果您不想讓音效立即開始播放，請先呼叫 **waveOutPause** 再呼叫 **waveOutWrite**。</span><span class="sxs-lookup"><span data-stu-id="4b5b5-132">If you do not want the sound to start playing immediately, call **waveOutPause** before calling **waveOutWrite**.</span></span> <span data-ttu-id="4b5b5-133">然後，當您想要開始播放波形音訊資料時，請呼叫 [**waveOutRestart**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutrestart)。</span><span class="sxs-lookup"><span data-stu-id="4b5b5-133">Then, when you want to begin playing waveform-audio data, call [**waveOutRestart**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutrestart).</span></span>

<span data-ttu-id="4b5b5-134">您無法使用 **waveOutRestart** 重新開機已使用 [**waveOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset)停止的裝置;您必須使用 **waveOutWrite** 來傳送第一個資料區塊，以繼續在裝置上播放。</span><span class="sxs-lookup"><span data-stu-id="4b5b5-134">You cannot use **waveOutRestart** to restart a device that has been stopped with [**waveOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset); you must use **waveOutWrite** to send the first data block to resume playback on the device.</span></span>

 

 