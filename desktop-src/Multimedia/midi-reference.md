---
title: MIDI 參考
description: MIDI 參考
ms.assetid: 6229a4a7-be42-4e2a-af9d-695c4759a4ef
keywords:
- 'Windows 多媒體、音樂檢測數位介面 (MIDI) '
- '多媒體、音樂檢測數位介面 (MIDI) '
- '多媒體音訊、音樂檢測數位介面 (MIDI) '
- '音訊、音樂檢測數位介面 (MIDI) '
- Windows 多媒體，MIDI 參考
- 多媒體、MIDI 參考
- 多媒體音訊、MIDI 參考
- 音訊、MIDI 參考
- 音樂檢測數位介面 (MIDI) ，參考
- MIDI (音樂檢測數位介面) ，參考
- 適用于 MIDI 的參考資訊，關於
- MIDI 參考，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c21542867faf1e09d68dc4fc81a50d25f56b5c5e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104375208"
---
# <a name="midi-reference"></a><span data-ttu-id="c230f-115">MIDI 參考</span><span class="sxs-lookup"><span data-stu-id="c230f-115">MIDI Reference</span></span>

<span data-ttu-id="c230f-116">本節說明與 (MIDI) 的音樂檢測數位介面相關聯的函式、宏、訊息和結構。</span><span class="sxs-lookup"><span data-stu-id="c230f-116">This section describes the functions, macros, messages, and structures associated with the Musical Instrument Digital Interface (MIDI).</span></span> <span data-ttu-id="c230f-117">這些元素的分組方式如下。</span><span class="sxs-lookup"><span data-stu-id="c230f-117">These elements are grouped as follows.</span></span>

## <a name="allocating-and-managing-buffers"></a><span data-ttu-id="c230f-118">配置和管理緩衝區</span><span class="sxs-lookup"><span data-stu-id="c230f-118">Allocating and Managing Buffers</span></span>

-   [<span data-ttu-id="c230f-119">**MIDIHDR**</span><span class="sxs-lookup"><span data-stu-id="c230f-119">**MIDIHDR**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-midihdr)
-   [<span data-ttu-id="c230f-120">**midiInAddBuffer**</span><span class="sxs-lookup"><span data-stu-id="c230f-120">**midiInAddBuffer**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinaddbuffer)
-   [<span data-ttu-id="c230f-121">**midiInPrepareHeader**</span><span class="sxs-lookup"><span data-stu-id="c230f-121">**midiInPrepareHeader**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinprepareheader)
-   [<span data-ttu-id="c230f-122">**midiInUnprepareHeader**</span><span class="sxs-lookup"><span data-stu-id="c230f-122">**midiInUnprepareHeader**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinunprepareheader)
-   [<span data-ttu-id="c230f-123">**midiOutPrepareHeader**</span><span class="sxs-lookup"><span data-stu-id="c230f-123">**midiOutPrepareHeader**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutprepareheader)
-   [<span data-ttu-id="c230f-124">**midiOutUnprepareHeader**</span><span class="sxs-lookup"><span data-stu-id="c230f-124">**midiOutUnprepareHeader**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutunprepareheader)

## <a name="callback-functions"></a><span data-ttu-id="c230f-125">回呼函式</span><span class="sxs-lookup"><span data-stu-id="c230f-125">Callback Functions</span></span>

-   <span data-ttu-id="c230f-126">[**MidiInProc**](/previous-versions//dd798460(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c230f-126">[**MidiInProc**](/previous-versions//dd798460(v=vs.85))</span></span>
-   <span data-ttu-id="c230f-127">[**MidiOutProc**](/previous-versions//dd798478(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c230f-127">[**MidiOutProc**](/previous-versions//dd798478(v=vs.85))</span></span>

## <a name="device-capabilities"></a><span data-ttu-id="c230f-128">裝置功能</span><span class="sxs-lookup"><span data-stu-id="c230f-128">Device Capabilities</span></span>

-   [<span data-ttu-id="c230f-129">**MIDIINCAPS**</span><span class="sxs-lookup"><span data-stu-id="c230f-129">**MIDIINCAPS**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-midiincaps)
-   [<span data-ttu-id="c230f-130">**midiInGetDevCaps**</span><span class="sxs-lookup"><span data-stu-id="c230f-130">**midiInGetDevCaps**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiingetdevcaps)
-   [<span data-ttu-id="c230f-131">**midiInGetID**</span><span class="sxs-lookup"><span data-stu-id="c230f-131">**midiInGetID**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiingetid)
-   [<span data-ttu-id="c230f-132">**midiInGetNumDevs**</span><span class="sxs-lookup"><span data-stu-id="c230f-132">**midiInGetNumDevs**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiingetnumdevs)
-   [<span data-ttu-id="c230f-133">**MIDIOUTCAPS**</span><span class="sxs-lookup"><span data-stu-id="c230f-133">**MIDIOUTCAPS**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-midioutcaps)
-   [<span data-ttu-id="c230f-134">**midiOutGetDevCaps**</span><span class="sxs-lookup"><span data-stu-id="c230f-134">**midiOutGetDevCaps**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetdevcaps)
-   [<span data-ttu-id="c230f-135">**midiOutGetID**</span><span class="sxs-lookup"><span data-stu-id="c230f-135">**midiOutGetID**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetid)
-   [<span data-ttu-id="c230f-136">**midiOutGetNumDevs**</span><span class="sxs-lookup"><span data-stu-id="c230f-136">**midiOutGetNumDevs**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetnumdevs)
-   [<span data-ttu-id="c230f-137">**MIDISTRMBUFFVER**</span><span class="sxs-lookup"><span data-stu-id="c230f-137">**MIDISTRMBUFFVER**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-midistrmbuffver)

## <a name="error-processing"></a><span data-ttu-id="c230f-138">錯誤處理</span><span class="sxs-lookup"><span data-stu-id="c230f-138">Error Processing</span></span>

-   [<span data-ttu-id="c230f-139">**midiInGetErrorText**</span><span class="sxs-lookup"><span data-stu-id="c230f-139">**midiInGetErrorText**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiingeterrortext)
-   [<span data-ttu-id="c230f-140">**midiOutGetErrorText**</span><span class="sxs-lookup"><span data-stu-id="c230f-140">**midiOutGetErrorText**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutgeterrortext)
-   [<span data-ttu-id="c230f-141">**MIM \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="c230f-141">**MIM\_ERROR**</span></span>](mim-error.md)
-   [<span data-ttu-id="c230f-142">**MIM \_ LONGERROR**</span><span class="sxs-lookup"><span data-stu-id="c230f-142">**MIM\_LONGERROR**</span></span>](mim-longerror.md)
-   [<span data-ttu-id="c230f-143">**MM \_ MIM \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="c230f-143">**MM\_MIM\_ERROR**</span></span>](mm-mim-error.md)
-   [<span data-ttu-id="c230f-144">**MM \_ MIM \_ LONGERROR**</span><span class="sxs-lookup"><span data-stu-id="c230f-144">**MM\_MIM\_LONGERROR**</span></span>](mm-mim-longerror.md)

## <a name="managing-midi-streams"></a><span data-ttu-id="c230f-145">管理 MIDI 串流</span><span class="sxs-lookup"><span data-stu-id="c230f-145">Managing MIDI Streams</span></span>

-   [<span data-ttu-id="c230f-146">**midiStreamClose**</span><span class="sxs-lookup"><span data-stu-id="c230f-146">**midiStreamClose**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamclose)
-   [<span data-ttu-id="c230f-147">**midiStreamOpen**</span><span class="sxs-lookup"><span data-stu-id="c230f-147">**midiStreamOpen**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamopen)
-   [<span data-ttu-id="c230f-148">**midiStreamOut**</span><span class="sxs-lookup"><span data-stu-id="c230f-148">**midiStreamOut**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout)
-   [<span data-ttu-id="c230f-149">**midiStreamPause**</span><span class="sxs-lookup"><span data-stu-id="c230f-149">**midiStreamPause**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreampause)
-   [<span data-ttu-id="c230f-150">**midiStreamPosition**</span><span class="sxs-lookup"><span data-stu-id="c230f-150">**midiStreamPosition**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamposition)
-   [<span data-ttu-id="c230f-151">**midiStreamProperty**</span><span class="sxs-lookup"><span data-stu-id="c230f-151">**midiStreamProperty**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamproperty)
-   [<span data-ttu-id="c230f-152">**midiStreamRestart**</span><span class="sxs-lookup"><span data-stu-id="c230f-152">**midiStreamRestart**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamrestart)
-   [<span data-ttu-id="c230f-153">**midiStreamStop**</span><span class="sxs-lookup"><span data-stu-id="c230f-153">**midiStreamStop**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamstop)

## <a name="opening-and-closing-devices"></a><span data-ttu-id="c230f-154">開啟和關閉裝置</span><span class="sxs-lookup"><span data-stu-id="c230f-154">Opening and Closing Devices</span></span>

-   [<span data-ttu-id="c230f-155">**midiInClose**</span><span class="sxs-lookup"><span data-stu-id="c230f-155">**midiInClose**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinclose)
-   [<span data-ttu-id="c230f-156">**midiInOpen**</span><span class="sxs-lookup"><span data-stu-id="c230f-156">**midiInOpen**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen)
-   [<span data-ttu-id="c230f-157">**midiOutClose**</span><span class="sxs-lookup"><span data-stu-id="c230f-157">**midiOutClose**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutclose)
-   [<span data-ttu-id="c230f-158">**midiOutOpen**</span><span class="sxs-lookup"><span data-stu-id="c230f-158">**midiOutOpen**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen)
-   [<span data-ttu-id="c230f-159">**MIM \_ 關閉**</span><span class="sxs-lookup"><span data-stu-id="c230f-159">**MIM\_CLOSE**</span></span>](mim-close.md)
-   [<span data-ttu-id="c230f-160">**MIM \_ 開啟**</span><span class="sxs-lookup"><span data-stu-id="c230f-160">**MIM\_OPEN**</span></span>](mim-open.md)
-   [<span data-ttu-id="c230f-161">**MM \_ MIM \_ 關閉**</span><span class="sxs-lookup"><span data-stu-id="c230f-161">**MM\_MIM\_CLOSE**</span></span>](mm-mim-close.md)
-   [<span data-ttu-id="c230f-162">**MM \_ MIM \_ 開啟**</span><span class="sxs-lookup"><span data-stu-id="c230f-162">**MM\_MIM\_OPEN**</span></span>](mm-mim-open.md)
-   [<span data-ttu-id="c230f-163">**MM \_ MOM \_ 關閉**</span><span class="sxs-lookup"><span data-stu-id="c230f-163">**MM\_MOM\_CLOSE**</span></span>](mm-mom-close.md)
-   [<span data-ttu-id="c230f-164">**分鐘 \_ MOM \_ 開啟**</span><span class="sxs-lookup"><span data-stu-id="c230f-164">**MM\_MOM\_OPEN**</span></span>](mm-mom-open.md)
-   [<span data-ttu-id="c230f-165">**MOM \_ 關閉**</span><span class="sxs-lookup"><span data-stu-id="c230f-165">**MOM\_CLOSE**</span></span>](mom-close.md)
-   [<span data-ttu-id="c230f-166">**MOM \_ OPEN**</span><span class="sxs-lookup"><span data-stu-id="c230f-166">**MOM\_OPEN**</span></span>](mom-open.md)

## <a name="output-devices"></a><span data-ttu-id="c230f-167">輸出裝置</span><span class="sxs-lookup"><span data-stu-id="c230f-167">Output Devices</span></span>

-   [<span data-ttu-id="c230f-168">KEYARRAY</span><span class="sxs-lookup"><span data-stu-id="c230f-168">KEYARRAY</span></span>](keyarray.md)
-   [<span data-ttu-id="c230f-169">**midiOutCacheDrumPatches**</span><span class="sxs-lookup"><span data-stu-id="c230f-169">**midiOutCacheDrumPatches**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutcachedrumpatches)
-   [<span data-ttu-id="c230f-170">**midiOutCachePatches**</span><span class="sxs-lookup"><span data-stu-id="c230f-170">**midiOutCachePatches**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutcachepatches)
-   [<span data-ttu-id="c230f-171">**midiOutGetVolume**</span><span class="sxs-lookup"><span data-stu-id="c230f-171">**midiOutGetVolume**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetvolume)
-   [<span data-ttu-id="c230f-172">**midiOutSetVolume**</span><span class="sxs-lookup"><span data-stu-id="c230f-172">**midiOutSetVolume**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutsetvolume)
-   [<span data-ttu-id="c230f-173">PATCHARRAY</span><span class="sxs-lookup"><span data-stu-id="c230f-173">PATCHARRAY</span></span>](patcharray.md)

## <a name="playing-a-message-or-messages"></a><span data-ttu-id="c230f-174">播放訊息或訊息</span><span class="sxs-lookup"><span data-stu-id="c230f-174">Playing a Message or Messages</span></span>

-   [<span data-ttu-id="c230f-175">**MEVT \_ EVENTPARM**</span><span class="sxs-lookup"><span data-stu-id="c230f-175">**MEVT\_EVENTPARM**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-mevt_eventparm)
-   [<span data-ttu-id="c230f-176">**MEVT 的 \_ 事件**</span><span class="sxs-lookup"><span data-stu-id="c230f-176">**MEVT\_EVENTTYPE**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-mevt_eventtype)
-   [<span data-ttu-id="c230f-177">**MIDIEVENT**</span><span class="sxs-lookup"><span data-stu-id="c230f-177">**MIDIEVENT**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-midievent)
-   [<span data-ttu-id="c230f-178">**midiOutLongMsg**</span><span class="sxs-lookup"><span data-stu-id="c230f-178">**midiOutLongMsg**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg)
-   [<span data-ttu-id="c230f-179">**midiOutReset**</span><span class="sxs-lookup"><span data-stu-id="c230f-179">**midiOutReset**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutreset)
-   [<span data-ttu-id="c230f-180">**midiOutShortMsg**</span><span class="sxs-lookup"><span data-stu-id="c230f-180">**midiOutShortMsg**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutshortmsg)
-   [<span data-ttu-id="c230f-181">**midiStreamOut**</span><span class="sxs-lookup"><span data-stu-id="c230f-181">**midiStreamOut**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout)
-   [<span data-ttu-id="c230f-182">**midiStreamPause**</span><span class="sxs-lookup"><span data-stu-id="c230f-182">**midiStreamPause**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreampause)
-   [<span data-ttu-id="c230f-183">**midiStreamRestart**</span><span class="sxs-lookup"><span data-stu-id="c230f-183">**midiStreamRestart**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamrestart)
-   [<span data-ttu-id="c230f-184">**midiStreamStop**</span><span class="sxs-lookup"><span data-stu-id="c230f-184">**midiStreamStop**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamstop)
-   [<span data-ttu-id="c230f-185">**MM \_ MOM \_ 完成**</span><span class="sxs-lookup"><span data-stu-id="c230f-185">**MM\_MOM\_DONE**</span></span>](mm-mom-done.md)
-   [<span data-ttu-id="c230f-186">**MM \_ MOM \_ POSITIONCB**</span><span class="sxs-lookup"><span data-stu-id="c230f-186">**MM\_MOM\_POSITIONCB**</span></span>](mm-mom-positioncb.md)
-   [<span data-ttu-id="c230f-187">**MOM \_ 完成**</span><span class="sxs-lookup"><span data-stu-id="c230f-187">**MOM\_DONE**</span></span>](mom-done.md)
-   [<span data-ttu-id="c230f-188">**MOM \_ POSITIONCB**</span><span class="sxs-lookup"><span data-stu-id="c230f-188">**MOM\_POSITIONCB**</span></span>](mom-positioncb.md)

## <a name="recording"></a><span data-ttu-id="c230f-189">記錄</span><span class="sxs-lookup"><span data-stu-id="c230f-189">Recording</span></span>

-   [<span data-ttu-id="c230f-190">**midiConnect**</span><span class="sxs-lookup"><span data-stu-id="c230f-190">**midiConnect**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiconnect)
-   [<span data-ttu-id="c230f-191">**midiDisconnect**</span><span class="sxs-lookup"><span data-stu-id="c230f-191">**midiDisconnect**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-mididisconnect)
-   [<span data-ttu-id="c230f-192">**midiInReset**</span><span class="sxs-lookup"><span data-stu-id="c230f-192">**midiInReset**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinreset)
-   [<span data-ttu-id="c230f-193">**midiInStart**</span><span class="sxs-lookup"><span data-stu-id="c230f-193">**midiInStart**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart)
-   [<span data-ttu-id="c230f-194">**midiInStop**</span><span class="sxs-lookup"><span data-stu-id="c230f-194">**midiInStop**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinstop)
-   [<span data-ttu-id="c230f-195">**MIDIPROPTEMPO**</span><span class="sxs-lookup"><span data-stu-id="c230f-195">**MIDIPROPTEMPO**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-midiproptempo)
-   [<span data-ttu-id="c230f-196">**MIDIPROPTIMEDIV**</span><span class="sxs-lookup"><span data-stu-id="c230f-196">**MIDIPROPTIMEDIV**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-midiproptimediv)
-   [<span data-ttu-id="c230f-197">**MIM \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="c230f-197">**MIM\_DATA**</span></span>](mim-data.md)
-   [<span data-ttu-id="c230f-198">**MIM \_ LONGDATA**</span><span class="sxs-lookup"><span data-stu-id="c230f-198">**MIM\_LONGDATA**</span></span>](mim-longdata.md)
-   [<span data-ttu-id="c230f-199">**MIM \_ MOREDATA**</span><span class="sxs-lookup"><span data-stu-id="c230f-199">**MIM\_MOREDATA**</span></span>](mim-moredata.md)
-   [<span data-ttu-id="c230f-200">**MM \_ MIM \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="c230f-200">**MM\_MIM\_DATA**</span></span>](mm-mim-data.md)
-   [<span data-ttu-id="c230f-201">**MM \_ MIM \_ MOREDATA**</span><span class="sxs-lookup"><span data-stu-id="c230f-201">**MM\_MIM\_MOREDATA**</span></span>](mm-mim-moredata.md)
-   [<span data-ttu-id="c230f-202">**MM \_ MIM \_ LONGDATA**</span><span class="sxs-lookup"><span data-stu-id="c230f-202">**MM\_MIM\_LONGDATA**</span></span>](mm-mim-longdata.md)

## <a name="sending-messages-to-devices"></a><span data-ttu-id="c230f-203">將訊息傳送至裝置</span><span class="sxs-lookup"><span data-stu-id="c230f-203">Sending Messages to Devices</span></span>

-   [<span data-ttu-id="c230f-204">**midiInMessage**</span><span class="sxs-lookup"><span data-stu-id="c230f-204">**midiInMessage**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinmessage)
-   [<span data-ttu-id="c230f-205">**midiOutMessage**</span><span class="sxs-lookup"><span data-stu-id="c230f-205">**midiOutMessage**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutmessage)

## <a name="related-topics"></a><span data-ttu-id="c230f-206">相關主題</span><span class="sxs-lookup"><span data-stu-id="c230f-206">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c230f-207">樂器數位介面 (MIDI)</span><span class="sxs-lookup"><span data-stu-id="c230f-207">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> </dl>

 

 