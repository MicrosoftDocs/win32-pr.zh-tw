---
title: 管理 MIDI
description: 管理 MIDI
ms.assetid: ba03a2a1-d998-498d-ad53-027ba2b6e276
keywords:
- 透過驅動程式 (MIDI) 的音樂檢測數位介面
- '透過驅動程式的 MIDI (音樂檢測數位介面) '
- 透過驅動程式錄製 MIDI 音訊
- MIDI 至驅動程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24214dd3f6cd13ca034b2555398f6055e4ce2da1
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103933131"
---
# <a name="managing-midi-thru"></a><span data-ttu-id="e80e8-107">管理 MIDI</span><span class="sxs-lookup"><span data-stu-id="e80e8-107">Managing MIDI Thru</span></span>

<span data-ttu-id="e80e8-108">您可以直接將 MIDI 輸入裝置連線到 MIDI 輸出裝置，如此一來，當輸入裝置收到 [**MIM \_ 資料**](mim-data.md) 訊息時，系統就會將具有相同 MIDI 事件資料的訊息傳送至輸出裝置磁碟機。</span><span class="sxs-lookup"><span data-stu-id="e80e8-108">You can connect a MIDI input device directly to a MIDI output device so that when the input device receives an [**MIM\_DATA**](mim-data.md) message, the system sends a message with the same MIDI event data to the output device driver.</span></span> <span data-ttu-id="e80e8-109">若要將 MIDI 輸出裝置連線至 MIDI 輸入裝置，請使用 [**midiConnect**](/windows/win32/api/mmeapi/nf-mmeapi-midiconnect) 函式。</span><span class="sxs-lookup"><span data-stu-id="e80e8-109">To connect a MIDI output device to a MIDI input device, use the [**midiConnect**](/windows/win32/api/mmeapi/nf-mmeapi-midiconnect) function.</span></span>

<span data-ttu-id="e80e8-110">為了達到具有多個輸出的最佳效能，應用程式可以選擇提供特殊形式的 MIDI 輸出驅動程式，稱為「透過 *驅動程式*」。</span><span class="sxs-lookup"><span data-stu-id="e80e8-110">To achieve the best possible performance with multiple outputs, an application can choose to supply a special form of MIDI output driver, called a *thru driver*.</span></span> <span data-ttu-id="e80e8-111">雖然系統只允許一個 MIDI 輸出裝置連線至 MIDI 輸入裝置，但多個 MIDI 輸出裝置可連接到「透過」驅動程式。</span><span class="sxs-lookup"><span data-stu-id="e80e8-111">Although the system allows only one MIDI output device to be connected to a MIDI input device, multiple MIDI output devices can be connected to a thru driver.</span></span> <span data-ttu-id="e80e8-112">這類系統上的應用程式可以透過裝置將 MIDI 輸入裝置連線到此裝置，並視需要將 MIDI 裝置連線到任意數量的 MIDI 輸出裝置。</span><span class="sxs-lookup"><span data-stu-id="e80e8-112">An application on such a system could connect the MIDI input device to this thru device and connect the MIDI thru device to as many MIDI output devices as needed.</span></span> <span data-ttu-id="e80e8-113">如需有關驅動程式的詳細資訊，請參閱 Windows 裝置驅動程式檔集。</span><span class="sxs-lookup"><span data-stu-id="e80e8-113">For more information about thru drivers, see the Windows device-driver documentation.</span></span>

## <a name="using-messages-to-manage-midi-recording"></a><span data-ttu-id="e80e8-114">使用訊息來管理 MIDI 記錄</span><span class="sxs-lookup"><span data-stu-id="e80e8-114">Using Messages to Manage MIDI Recording</span></span>

<span data-ttu-id="e80e8-115">下列訊息可以傳送至視窗或執行緒回呼程式，以管理 MIDI 錄製。</span><span class="sxs-lookup"><span data-stu-id="e80e8-115">The following messages can be sent to a window or thread callback procedure for managing MIDI recording.</span></span>



| <span data-ttu-id="e80e8-116">值</span><span class="sxs-lookup"><span data-stu-id="e80e8-116">Value</span></span>                                          | <span data-ttu-id="e80e8-117">意義</span><span class="sxs-lookup"><span data-stu-id="e80e8-117">Meaning</span></span>                                                                                                                                |
|------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e80e8-118">**MM \_ MIM \_ 關閉**</span><span class="sxs-lookup"><span data-stu-id="e80e8-118">**MM\_MIM\_CLOSE**</span></span>](mm-mim-close.md)         | <span data-ttu-id="e80e8-119">在使用 [**midiInClose**](/windows/win32/api/mmeapi/nf-mmeapi-midiinclose) 函式關閉 MIDI 輸入裝置時傳送。</span><span class="sxs-lookup"><span data-stu-id="e80e8-119">Sent when a MIDI input device is closed by using the [**midiInClose**](/windows/win32/api/mmeapi/nf-mmeapi-midiinclose) function.</span></span>                                      |
| [<span data-ttu-id="e80e8-120">**MM \_ MIM \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="e80e8-120">**MM\_MIM\_DATA**</span></span>](mm-mim-data.md)           | <span data-ttu-id="e80e8-121">收到完整的 MIDI 訊息時傳送。</span><span class="sxs-lookup"><span data-stu-id="e80e8-121">Sent when a complete MIDI message is received.</span></span> <span data-ttu-id="e80e8-122"> (此訊息適用于除系統專屬訊息以外的所有 MIDI 訊息。 ) </span><span class="sxs-lookup"><span data-stu-id="e80e8-122">(This message is used for all MIDI messages except system-exclusive messages.)</span></span>          |
| [<span data-ttu-id="e80e8-123">**MM \_ MIM \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="e80e8-123">**MM\_MIM\_ERROR**</span></span>](mm-mim-error.md)         | <span data-ttu-id="e80e8-124">收到不正確 MIDI 訊息時傳送。</span><span class="sxs-lookup"><span data-stu-id="e80e8-124">Sent when an invalid MIDI message is received.</span></span> <span data-ttu-id="e80e8-125"> (此訊息適用于除系統專屬訊息以外的所有 MIDI 訊息。 ) </span><span class="sxs-lookup"><span data-stu-id="e80e8-125">(This message is used for all MIDI messages except system-exclusive messages.)</span></span>          |
| [<span data-ttu-id="e80e8-126">**MM \_ MIM \_ LONGDATA**</span><span class="sxs-lookup"><span data-stu-id="e80e8-126">**MM\_MIM\_LONGDATA**</span></span>](mm-mim-longdata.md)   | <span data-ttu-id="e80e8-127">當收到完整的 MIDI 系統專屬訊息或緩衝區已填滿系統專屬資料時傳送。</span><span class="sxs-lookup"><span data-stu-id="e80e8-127">Sent when either a complete MIDI system-exclusive message is received or when a buffer has been filled with system-exclusive data.</span></span>     |
| [<span data-ttu-id="e80e8-128">**MM \_ MIM \_ LONGERROR**</span><span class="sxs-lookup"><span data-stu-id="e80e8-128">**MM\_MIM\_LONGERROR**</span></span>](mm-mim-longerror.md) | <span data-ttu-id="e80e8-129">收到不正確 MIDI 系統專屬訊息時傳送。</span><span class="sxs-lookup"><span data-stu-id="e80e8-129">Sent when an invalid MIDI system-exclusive message is received.</span></span>                                                                        |
| [<span data-ttu-id="e80e8-130">**MM \_ MIM \_ MOREDATA**</span><span class="sxs-lookup"><span data-stu-id="e80e8-130">**MM\_MIM\_MOREDATA**</span></span>](mm-mim-moredata.md)   | <span data-ttu-id="e80e8-131">當應用程式處理 [**MIM \_ 資料**](mim-data.md) 訊息的速度不夠快，無法跟上輸入裝置磁碟機時傳送。</span><span class="sxs-lookup"><span data-stu-id="e80e8-131">Sent when an application is not processing [**MIM\_DATA**](mim-data.md) messages fast enough to keep up with the input device driver.</span></span> |
| [<span data-ttu-id="e80e8-132">**MM \_ MIM \_ 開啟**</span><span class="sxs-lookup"><span data-stu-id="e80e8-132">**MM\_MIM\_OPEN**</span></span>](mm-mim-open.md)           | <span data-ttu-id="e80e8-133">在使用 [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) 函式開啟 MIDI 輸入裝置時傳送。</span><span class="sxs-lookup"><span data-stu-id="e80e8-133">Sent when a MIDI input device is opened by using the [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) function.</span></span>                                        |



 

<span data-ttu-id="e80e8-134">*WParam* 參數和 *lParam* 參數會與這些訊息相關聯。</span><span class="sxs-lookup"><span data-stu-id="e80e8-134">A *wParam* parameter and an *lParam* parameter are associated with each of these messages.</span></span> <span data-ttu-id="e80e8-135">*WParam* 參數一律會指定開啟之 MIDI 裝置的控制碼。</span><span class="sxs-lookup"><span data-stu-id="e80e8-135">The *wParam* parameter always specifies the handle of an open MIDI device.</span></span> <span data-ttu-id="e80e8-136">*LParam* 參數未針對 [**MM \_ mim \_ CLOSE**](mm-mim-close.md)和 [**mm \_ mim \_ OPEN**](mm-mim-open.md)訊息使用。</span><span class="sxs-lookup"><span data-stu-id="e80e8-136">The *lParam* parameter is unused for the [**MM\_MIM\_CLOSE**](mm-mim-close.md) and [**MM\_MIM\_OPEN**](mm-mim-open.md) messages.</span></span>

<span data-ttu-id="e80e8-137">針對 [**MM \_ MIM \_ LONGDATA**](mm-mim-longdata.md) 訊息， *lpMidiHdr* 會指定 [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) 結構的位址，以識別系統專屬訊息的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="e80e8-137">For the [**MM\_MIM\_LONGDATA**](mm-mim-longdata.md) message, *lpMidiHdr* specifies an address of a [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure that identifies the buffer for system-exclusive messages.</span></span> <span data-ttu-id="e80e8-138">緩衝區可能不會完全填滿，因為系統專屬訊息的大小通常在記錄之前不是已知的，而且必須配置大小總計可以包含最大預期訊息的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="e80e8-138">The buffer may not be completely filled, because the size of the system-exclusive messages is usually not known before being recorded and because buffers whose total size can contain the largest expected message must be allocated.</span></span> <span data-ttu-id="e80e8-139">若要判斷存在於緩衝區中的有效資料量，請使用 **MIDIHDR** 結構的 **dwBytesRecorded** 成員。</span><span class="sxs-lookup"><span data-stu-id="e80e8-139">To determine the amount of valid data present in the buffer, use the **dwBytesRecorded** member of the **MIDIHDR** structure.</span></span>

## <a name="using-a-callback-function-to-manage-midi-recording"></a><span data-ttu-id="e80e8-140">使用回呼函式來管理 MIDI 記錄</span><span class="sxs-lookup"><span data-stu-id="e80e8-140">Using a Callback Function to Manage MIDI Recording</span></span>

<span data-ttu-id="e80e8-141">您可以定義自己的回呼函式來管理 MIDI 輸入裝置的錄製。</span><span class="sxs-lookup"><span data-stu-id="e80e8-141">You can define your own callback function to manage recording for MIDI input devices.</span></span> <span data-ttu-id="e80e8-142">回呼函數記載為 [**MidiInProc**](/previous-versions//dd798460(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="e80e8-142">The callback function is documented as [**MidiInProc**](/previous-versions//dd798460(v=vs.85)).</span></span>

<span data-ttu-id="e80e8-143">下列訊息可以傳送至 **MidiInProc** 回呼函數的 *wMsg* 參數。</span><span class="sxs-lookup"><span data-stu-id="e80e8-143">The following messages can be sent to the *wMsg* parameter of the **MidiInProc** callback function.</span></span>



| <span data-ttu-id="e80e8-144">值</span><span class="sxs-lookup"><span data-stu-id="e80e8-144">Value</span></span>                                   | <span data-ttu-id="e80e8-145">意義</span><span class="sxs-lookup"><span data-stu-id="e80e8-145">Meaning</span></span>                                                                                                                                |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e80e8-146">**MIM \_ 關閉**</span><span class="sxs-lookup"><span data-stu-id="e80e8-146">**MIM\_CLOSE**</span></span>](mim-close.md)         | <span data-ttu-id="e80e8-147">在使用 [**midiInClose**](/windows/win32/api/mmeapi/nf-mmeapi-midiinclose) 函式關閉裝置時傳送。</span><span class="sxs-lookup"><span data-stu-id="e80e8-147">Sent when the device is closed by using the [**midiInClose**](/windows/win32/api/mmeapi/nf-mmeapi-midiinclose) function.</span></span>                                               |
| [<span data-ttu-id="e80e8-148">**MIM \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="e80e8-148">**MIM\_DATA**</span></span>](mim-data.md)           | <span data-ttu-id="e80e8-149">收到完整的 MIDI 訊息時傳送 (此訊息會用於所有的 MIDI 訊息，但系統專屬的訊息) 除外。</span><span class="sxs-lookup"><span data-stu-id="e80e8-149">Sent when a complete MIDI message is received (this message is used for all MIDI messages except system-exclusive messages).</span></span>           |
| [<span data-ttu-id="e80e8-150">**MIM \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="e80e8-150">**MIM\_ERROR**</span></span>](mim-error.md)         | <span data-ttu-id="e80e8-151">收到不正確 MIDI 訊息時傳送 (此訊息會用於所有的 MIDI 訊息，但系統專屬的訊息) 除外。</span><span class="sxs-lookup"><span data-stu-id="e80e8-151">Sent when an invalid MIDI message is received (this message is used for all MIDI messages except system-exclusive messages).</span></span>           |
| [<span data-ttu-id="e80e8-152">**MIM \_ LONGDATA**</span><span class="sxs-lookup"><span data-stu-id="e80e8-152">**MIM\_LONGDATA**</span></span>](mim-longdata.md)   | <span data-ttu-id="e80e8-153">當收到完整的 MIDI 系統專屬訊息或緩衝區已填滿系統專屬資料時傳送。</span><span class="sxs-lookup"><span data-stu-id="e80e8-153">Sent when either a complete MIDI system-exclusive message is received or when a buffer has been filled with system-exclusive data.</span></span>     |
| [<span data-ttu-id="e80e8-154">**MIM \_ LONGERROR**</span><span class="sxs-lookup"><span data-stu-id="e80e8-154">**MIM\_LONGERROR**</span></span>](mim-longerror.md) | <span data-ttu-id="e80e8-155">收到不正確 MIDI 系統專屬訊息時傳送。</span><span class="sxs-lookup"><span data-stu-id="e80e8-155">Sent when an invalid MIDI system-exclusive message is received.</span></span>                                                                        |
| [<span data-ttu-id="e80e8-156">**MIM \_ MOREDATA**</span><span class="sxs-lookup"><span data-stu-id="e80e8-156">**MIM\_MOREDATA**</span></span>](mim-moredata.md)   | <span data-ttu-id="e80e8-157">當應用程式處理 [**MIM \_ 資料**](mim-data.md) 訊息的速度不夠快，無法跟上輸入裝置磁碟機時傳送。</span><span class="sxs-lookup"><span data-stu-id="e80e8-157">Sent when an application is not processing [**MIM\_DATA**](mim-data.md) messages fast enough to keep up with the input device driver.</span></span> |
| [<span data-ttu-id="e80e8-158">**MIM \_ 開啟**</span><span class="sxs-lookup"><span data-stu-id="e80e8-158">**MIM\_OPEN**</span></span>](mim-open.md)           | <span data-ttu-id="e80e8-159">在使用 [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) 函式開啟 MIDI 輸入裝置時傳送。</span><span class="sxs-lookup"><span data-stu-id="e80e8-159">Sent when the MIDI input device is opened by using the [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) function.</span></span>                                      |



 

<span data-ttu-id="e80e8-160">這些訊息類似于傳送至視窗程式函式的訊息，但參數不同。</span><span class="sxs-lookup"><span data-stu-id="e80e8-160">These messages are similar to those sent to window procedure functions, but the parameters are different.</span></span> <span data-ttu-id="e80e8-161">開啟之 MIDI 裝置的控制碼會以參數形式傳遞給回呼函式，以及使用 **midiInOpen** 傳遞的實例資料的雙字。</span><span class="sxs-lookup"><span data-stu-id="e80e8-161">A handle of the open MIDI device is passed as a parameter to the callback function, along with the doubleword of instance data that was passed by using **midiInOpen**.</span></span>

<span data-ttu-id="e80e8-162">針對 [**MIM \_ LONGDATA**](mim-longdata.md) 訊息， *lpMidiHdr* 會指定 [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) 結構的位址，以識別系統專屬訊息的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="e80e8-162">For the [**MIM\_LONGDATA**](mim-longdata.md) message, *lpMidiHdr* specifies an address of a [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure that identifies the buffer for system-exclusive messages.</span></span> <span data-ttu-id="e80e8-163">緩衝區可能不會完全填滿。</span><span class="sxs-lookup"><span data-stu-id="e80e8-163">The buffer might not be completely filled.</span></span> <span data-ttu-id="e80e8-164">若要判斷存在於緩衝區中的有效資料量，請使用 **MIDIHDR** 結構的 **dwBytesRecorded** 成員。</span><span class="sxs-lookup"><span data-stu-id="e80e8-164">To determine the amount of valid data present in the buffer, use the **dwBytesRecorded** member of the **MIDIHDR** structure.</span></span>

<span data-ttu-id="e80e8-165">使用資料區塊完成設備磁碟機之後，您可以清除並釋放資料區塊。</span><span class="sxs-lookup"><span data-stu-id="e80e8-165">After the device driver is finished with a data block, you can clean up and free the data block.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e80e8-166">相關主題</span><span class="sxs-lookup"><span data-stu-id="e80e8-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e80e8-167">錄製 MIDI 音訊</span><span class="sxs-lookup"><span data-stu-id="e80e8-167">Recording MIDI Audio</span></span>](recording-midi-audio.md)
</dt> </dl>

 

 