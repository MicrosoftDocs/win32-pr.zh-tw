---
title: 管理 MIDI 資料區塊
description: 管理 MIDI 資料區塊
ms.assetid: f29fbc08-ef67-489c-aedf-5a2bc65233f7
keywords:
- " (MIDI) 的音樂檢測數位介面，管理資料區塊"
- MIDI (的音樂檢測數位介面) ，管理資料區塊
- MIDI 服務，管理資料區塊
- 管理 MIDI 資料區塊
- 音樂檢測數位介面 (MIDI) ，處理驅動程式訊息
- MIDI (的音樂檢測數位介面) ，處理驅動程式訊息
- MIDI 服務，處理驅動程式訊息
- 處理驅動程式訊息
- 音樂檢測數位介面 (MIDI) 、資料區塊
- MIDI (音樂檢測數位介面) 、資料區塊
- MIDI 服務，資料區塊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af348d6c53d2944bf22c026674704baa1fe74e07
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103933132"
---
# <a name="managing-midi-data-blocks"></a><span data-ttu-id="59a8a-114">管理 MIDI 資料區塊</span><span class="sxs-lookup"><span data-stu-id="59a8a-114">Managing MIDI Data Blocks</span></span>

<span data-ttu-id="59a8a-115">使用資料區塊傳遞系統專屬訊息的應用程式 (使用 [**midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg) 和 [**midiInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-midiinaddbuffer) 函式) 和串流緩衝區 (使用 [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) 函式) 必須持續提供設備磁碟機與資料區塊，直到播放或錄製完成為止。</span><span class="sxs-lookup"><span data-stu-id="59a8a-115">Applications that use data blocks for passing system-exclusive messages (using the [**midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg) and [**midiInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-midiinaddbuffer) functions) and stream buffers (using the [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) function) must continually supply the device driver with data blocks until playback or recording is complete.</span></span>

<span data-ttu-id="59a8a-116">即使使用了單一資料區塊，應用程式也必須能夠判斷設備磁碟機何時完成資料區塊，讓它可以釋放與資料區塊和標頭結構相關聯的記憶體。</span><span class="sxs-lookup"><span data-stu-id="59a8a-116">Even if a single data block is used, an application must be able to determine when a device driver is finished with the data block so it can free the memory associated with the data block and header structure.</span></span> <span data-ttu-id="59a8a-117">有三種方法可用來判斷設備磁碟機何時完成資料區塊：</span><span class="sxs-lookup"><span data-stu-id="59a8a-117">Three methods can be used to determine when a device driver is finished with a data block:</span></span>

-   <span data-ttu-id="59a8a-118">指定回呼函式，以在使用資料區塊完成時，接收驅動程式所傳送的訊息。</span><span class="sxs-lookup"><span data-stu-id="59a8a-118">Specify a callback function to receive a message sent by the driver when it is finished with a data block.</span></span> <span data-ttu-id="59a8a-119">若要取得時間戳記的 MIDI 輸入資料，您必須使用回呼函數。</span><span class="sxs-lookup"><span data-stu-id="59a8a-119">To get time-stamped MIDI input data, you must use a callback function.</span></span>
-   <span data-ttu-id="59a8a-120">使用事件回呼 (僅適用于輸出) 。</span><span class="sxs-lookup"><span data-stu-id="59a8a-120">Use an event callback (for output only).</span></span>
-   <span data-ttu-id="59a8a-121">使用視窗或執行緒回呼來接收驅動程式完成資料區塊時所傳送的訊息。</span><span class="sxs-lookup"><span data-stu-id="59a8a-121">Use a window or thread callback to receive a message sent by the driver when it is finished with a data block.</span></span>

<span data-ttu-id="59a8a-122">如果應用程式在需要時無法取得設備磁碟機的資料區塊，則可能會發生播放或遺失傳入記錄資訊。</span><span class="sxs-lookup"><span data-stu-id="59a8a-122">If an application does not get a data block to the device driver when it is needed, an audible gap in playback or a loss of incoming recorded information can occur.</span></span> <span data-ttu-id="59a8a-123">應用程式至少應該使用雙重緩衝配置，以在設備磁碟機之前至少保留一個資料區塊。</span><span class="sxs-lookup"><span data-stu-id="59a8a-123">At a minimum, an application should use a double-buffering scheme to stay at least one data block ahead of the device driver.</span></span>

## <a name="using-a-callback-function-to-process-driver-messages"></a><span data-ttu-id="59a8a-124">使用回呼函式來處理驅動程式訊息</span><span class="sxs-lookup"><span data-stu-id="59a8a-124">Using a Callback Function to Process Driver Messages</span></span>

<span data-ttu-id="59a8a-125">您可以撰寫自己的回呼函式來處理設備磁碟機所傳送的訊息。</span><span class="sxs-lookup"><span data-stu-id="59a8a-125">You can write your own callback function to process messages sent by the device driver.</span></span> <span data-ttu-id="59a8a-126">若要使用回呼函式，請在 \_ *dwFlags* 參數中指定回呼函式旗標，並在 [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen)或 [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen)函數的 *dwCallback* 參數中指定回呼函數的位址。</span><span class="sxs-lookup"><span data-stu-id="59a8a-126">To use a callback function, specify the CALLBACK\_FUNCTION flag in the *dwFlags* parameter and the address of the callback function in the *dwCallback* parameter of the [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) or [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) function.</span></span>

<span data-ttu-id="59a8a-127">傳送至回呼函式的訊息類似于傳送至視窗的訊息，但它們有兩個雙字參數，而不是不帶正負號的整數參數和雙量參數。</span><span class="sxs-lookup"><span data-stu-id="59a8a-127">Messages sent to a callback function are similar to messages sent to a window, except they have two doubleword parameters instead of an unsigned integer parameter and a doubleword parameter.</span></span> <span data-ttu-id="59a8a-128">如需這些訊息的詳細資訊，請參閱傳送 [System-Exclusive 訊息](sending-system-exclusive-messages.md) 和 [管理 MIDI 記錄](managing-midi-recording.md)。</span><span class="sxs-lookup"><span data-stu-id="59a8a-128">For more information about these messages, see [Sending System-Exclusive Messages](sending-system-exclusive-messages.md) and [Managing MIDI Recording](managing-midi-recording.md).</span></span>

<span data-ttu-id="59a8a-129">您可以使用下列其中一種技術，將實例資料從應用程式傳遞至回呼函數：</span><span class="sxs-lookup"><span data-stu-id="59a8a-129">Use one of the following techniques to pass instance data from an application to a callback function:</span></span>

-   <span data-ttu-id="59a8a-130">使用函式的 *dwCallbackInstance* 參數來開啟設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="59a8a-130">Use the *dwCallbackInstance* parameter of the function that opens the device driver.</span></span>
-   <span data-ttu-id="59a8a-131">使用 [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr)結構的 **dwUser** 成員，識別要傳送至 MIDI 設備磁碟機的資料區塊。</span><span class="sxs-lookup"><span data-stu-id="59a8a-131">Use the **dwUser** member of the [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure that identifies a data block being sent to a MIDI device driver.</span></span>

<span data-ttu-id="59a8a-132">如果您需要超過32位的實例資料，請傳遞包含額外資訊的結構位址。</span><span class="sxs-lookup"><span data-stu-id="59a8a-132">If you need more than 32 bits of instance data, pass an address of a structure containing the additional information.</span></span>

## <a name="using-an-event-callback-to-process-driver-messages"></a><span data-ttu-id="59a8a-133">使用事件回呼處理驅動程式訊息</span><span class="sxs-lookup"><span data-stu-id="59a8a-133">Using an Event Callback to Process Driver Messages</span></span>

<span data-ttu-id="59a8a-134">若要使用事件回呼，請使用 [CreateEvent](/windows/win32/api/synchapi/nf-synchapi-createeventa) 函數來取出事件的控制碼，並 \_ 在 [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) 函式的呼叫中指定回呼事件。</span><span class="sxs-lookup"><span data-stu-id="59a8a-134">To use an event callback, use the [CreateEvent](/windows/win32/api/synchapi/nf-synchapi-createeventa) function to retrieve the handle of an event and specify CALLBACK\_EVENT in the call to the [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) function.</span></span>

<span data-ttu-id="59a8a-135">事件回呼是由任何可能導致函式回呼的專案所設定。</span><span class="sxs-lookup"><span data-stu-id="59a8a-135">An event callback is set by anything that might cause a function callback.</span></span> <span data-ttu-id="59a8a-136">與回呼函數和視窗或執行緒回呼不同的是，事件回呼不會收到特定的關閉、完成或開啟通知。</span><span class="sxs-lookup"><span data-stu-id="59a8a-136">Unlike callback functions and window or thread callbacks, event callbacks do not receive specific close, done, or open notifications.</span></span> <span data-ttu-id="59a8a-137">因此，在事件發生之後，應用程式可能必須檢查正在等候的進程狀態。</span><span class="sxs-lookup"><span data-stu-id="59a8a-137">Therefore, an application may have to check the status of the process it is waiting for after the event occurs.</span></span>

<span data-ttu-id="59a8a-138">如需事件回呼的詳細資訊，請參閱 [使用事件回呼來管理緩衝的播放](using-an-callback-to-manage-buffered-playback.md)。</span><span class="sxs-lookup"><span data-stu-id="59a8a-138">For more information about event callbacks, see [Using an Event Callback to Manage Buffered Playback](using-an-callback-to-manage-buffered-playback.md).</span></span>

## <a name="using-a-window-or-thread-callback-to-process-driver-messages"></a><span data-ttu-id="59a8a-139">使用視窗或執行緒回呼處理驅動程式訊息</span><span class="sxs-lookup"><span data-stu-id="59a8a-139">Using a Window or Thread Callback to Process Driver Messages</span></span>

<span data-ttu-id="59a8a-140">若要使用視窗回呼，請在 \_ *dwFlags* 參數中指定回呼視窗旗標，並在 [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen)或 [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen)函式之 *dwCallback* 參數的低序位單字中指定視窗控制碼。</span><span class="sxs-lookup"><span data-stu-id="59a8a-140">To use a window callback, specify the CALLBACK\_WINDOW flag in the *dwFlags* parameter and a window handle in the low-order word of the *dwCallback* parameter of the [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) or [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) function.</span></span> <span data-ttu-id="59a8a-141">驅動程式訊息將會傳送至 *dwCallback* 中的控制碼所識別之視窗的視窗程式函式。</span><span class="sxs-lookup"><span data-stu-id="59a8a-141">Driver messages will be sent to the window procedure function for the window identified by the handle in *dwCallback*.</span></span>

<span data-ttu-id="59a8a-142">同樣地，若要使用執行緒回呼，請 \_ 在 **MidiInOpen** 或 **midiOutOpen** 的呼叫中指定回呼執行緒旗標和執行緒識別碼。</span><span class="sxs-lookup"><span data-stu-id="59a8a-142">Similarly, to use a thread callback, specify the CALLBACK\_THREAD flag and a thread identifier in the call to **midiInOpen** or **midiOutOpen**.</span></span> <span data-ttu-id="59a8a-143">在此情況下，訊息將會張貼到指定的執行緒，而不是傳送至視窗。</span><span class="sxs-lookup"><span data-stu-id="59a8a-143">In this case, messages will be posted to the specified thread instead of to a window.</span></span>

<span data-ttu-id="59a8a-144">傳送至視窗或執行緒回呼的訊息是使用的 MIDI 裝置專用的。</span><span class="sxs-lookup"><span data-stu-id="59a8a-144">Messages sent to a window or thread callback are specific to the MIDI device used.</span></span> <span data-ttu-id="59a8a-145">如需這些訊息的詳細資訊，請參閱傳送 [System-Exclusive 訊息](sending-system-exclusive-messages.md) 和 [管理 MIDI 記錄](managing-midi-recording.md)。</span><span class="sxs-lookup"><span data-stu-id="59a8a-145">For more information about these messages, see [Sending System-Exclusive Messages](sending-system-exclusive-messages.md) and [Managing MIDI Recording](managing-midi-recording.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="59a8a-146">相關主題</span><span class="sxs-lookup"><span data-stu-id="59a8a-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="59a8a-147">MIDI 服務</span><span class="sxs-lookup"><span data-stu-id="59a8a-147">MIDI Services</span></span>](midi-services.md)
</dt> </dl>

 

 