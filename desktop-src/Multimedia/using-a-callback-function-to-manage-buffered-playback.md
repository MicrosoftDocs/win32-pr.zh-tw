---
title: 使用回呼函式來管理緩衝的播放
description: 使用回呼函式來管理緩衝的播放
ms.assetid: aaaf9c5f-c9b2-4e55-a4c1-28c99cc03945
keywords:
- 音樂檢測數位介面 (MIDI) 、緩衝播放
- MIDI (的音樂檢測數位介面) ，經過緩衝的播放
- 播放 MIDI 檔案，緩衝播放
- 緩衝播放
- MOM_CLOSE 訊息
- MOM_DONE 訊息
- MOM_OPEN 訊息
- 音樂檢測數位介面 (MIDI) ，傳送訊息
- MIDI (的音樂檢測數位介面) ，傳送訊息
- 播放 MIDI 檔案，傳送訊息
- 傳送 MIDI 訊息
- 音樂檢測數位介面 (MIDI) 、回呼函式
- MIDI (音樂檢測數位介面) 、回呼函式
- 播放 MIDI 檔案，回呼函數
- MidiOutProc 回呼函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bccccd8e5fb052b89e8ca1804b89de6da26cd5b7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103682106"
---
# <a name="using-a-callback-function-to-manage-buffered-playback"></a><span data-ttu-id="6a9d5-118">使用回呼函式來管理緩衝的播放</span><span class="sxs-lookup"><span data-stu-id="6a9d5-118">Using a Callback Function to Manage Buffered Playback</span></span>

<span data-ttu-id="6a9d5-119">您可以定義自己的回呼函式，以管理已緩衝播放的 MIDI 輸出裝置。</span><span class="sxs-lookup"><span data-stu-id="6a9d5-119">You can define your own callback function to manage buffered playback of MIDI output devices.</span></span> <span data-ttu-id="6a9d5-120">回呼函數記載為 [**MidiOutProc**](/previous-versions//dd798478(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="6a9d5-120">The callback function is documented as [**MidiOutProc**](/previous-versions//dd798478(v=vs.85)).</span></span>

<span data-ttu-id="6a9d5-121">下列訊息可以傳送至 **MidiOutProc** 回呼函數的 *wMsg* 參數。</span><span class="sxs-lookup"><span data-stu-id="6a9d5-121">The following messages can be sent to the *wMsg* parameter of the **MidiOutProc** callback function.</span></span>



| <span data-ttu-id="6a9d5-122">值</span><span class="sxs-lookup"><span data-stu-id="6a9d5-122">Value</span></span>                           | <span data-ttu-id="6a9d5-123">意義</span><span class="sxs-lookup"><span data-stu-id="6a9d5-123">Meaning</span></span>                                                                                                                                                                  |
|---------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6a9d5-124">**MOM \_ 關閉**</span><span class="sxs-lookup"><span data-stu-id="6a9d5-124">**MOM\_CLOSE**</span></span>](mom-close.md) | <span data-ttu-id="6a9d5-125">在使用 [**midiOutClose**](/windows/win32/api/mmeapi/nf-mmeapi-midioutclose) 函式關閉裝置時傳送。</span><span class="sxs-lookup"><span data-stu-id="6a9d5-125">Sent when the device is closed by using the [**midiOutClose**](/windows/win32/api/mmeapi/nf-mmeapi-midioutclose) function.</span></span>                                                                               |
| [<span data-ttu-id="6a9d5-126">**MOM \_ 完成**</span><span class="sxs-lookup"><span data-stu-id="6a9d5-126">**MOM\_DONE**</span></span>](mom-done.md)   | <span data-ttu-id="6a9d5-127">當設備磁碟機使用 [**midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg) 或 [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) 函數傳送的資料區塊完成時傳送。</span><span class="sxs-lookup"><span data-stu-id="6a9d5-127">Sent when the device driver is finished with a data block sent by using the [**midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg) or [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) function.</span></span> |
| [<span data-ttu-id="6a9d5-128">**MOM \_ OPEN**</span><span class="sxs-lookup"><span data-stu-id="6a9d5-128">**MOM\_OPEN**</span></span>](mom-open.md)   | <span data-ttu-id="6a9d5-129">在使用 [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) 函式開啟裝置時傳送。</span><span class="sxs-lookup"><span data-stu-id="6a9d5-129">Sent when the device is opened by using the [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) function.</span></span>                                                                                 |



 

<span data-ttu-id="6a9d5-130">這些訊息類似于傳送至視窗程式函式的訊息，但參數不同。</span><span class="sxs-lookup"><span data-stu-id="6a9d5-130">These messages are similar to those sent to window procedure functions, but the parameters are different.</span></span> <span data-ttu-id="6a9d5-131">開啟之 MIDI 裝置的控制碼會以參數形式傳遞給回呼函式，以及使用 **midiOutOpen** 傳遞的實例資料的雙量。</span><span class="sxs-lookup"><span data-stu-id="6a9d5-131">A handle of the open MIDI device is passed as a parameter to the callback function, along with the doubleword of instance data passed by using **midiOutOpen**.</span></span>

<span data-ttu-id="6a9d5-132">使用資料區塊完成驅動程式之後，您可以清除並釋放資料區塊。</span><span class="sxs-lookup"><span data-stu-id="6a9d5-132">After the driver is finished with a data block, you can clean up and free the data block.</span></span> <span data-ttu-id="6a9d5-133">因為回呼函式有建議的限制，所以最好不要從回呼函式內進行。</span><span class="sxs-lookup"><span data-stu-id="6a9d5-133">Because of the suggested restrictions on callback functions, it is better not to do this from within the callback function.</span></span>

 

 