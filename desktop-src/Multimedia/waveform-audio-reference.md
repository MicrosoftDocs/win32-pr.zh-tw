---
title: 波形音訊參考
description: 此區段會列出與波形音訊相關聯的函式、結構和訊息，這些功能是在 [多媒體參考] 下記載。 這些元素的分組方式如下。
ms.assetid: 723953f7-b38e-4f24-8d54-9849e013011d
keywords:
- Windows 多媒體，波形音訊參考
- 多媒體、波形音訊參考
- 多媒體音訊、波形參考
- 音訊、波形參考
- Windows 多媒體，波形音訊
- 多媒體、波形音訊
- 多媒體音訊、波形
- 音訊、波形
- 波形音訊，參考
- 波形音訊參考，關於
- wavefore 音訊的參考資料，關於
- 波形音訊參考，輔助裝置
- wavefore 音訊、輔助裝置的參考
- 波形音訊參考，播放
- wavefore 音訊、播放的參考
- 波形音訊參考，錯誤
- wavefore 音訊、錯誤的參考
- 波形音訊參考，開啟
- wavefore 音訊的參考，開啟
- 波形音訊參考，關閉
- wavefore 音訊的參考，關閉
- 波形音訊參考，音調
- wavefore 音訊、音調的參考
- 波形音訊參考，音量
- wavefore 音訊、磁片區的參考
- 波形音訊參考，訊息
- wavefore 音訊、訊息的參考
- 波形音訊參考，目前位置
- wavefore 音訊、目前位置的參考
- 波形音訊參考，錄製
- wavefore 音訊、錄製的參考
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c74b37984b2d3fab5dad1ea0df4f1f62dfa1855e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104023386"
---
# <a name="waveform-audio-reference"></a><span data-ttu-id="03167-135">波形音訊參考</span><span class="sxs-lookup"><span data-stu-id="03167-135">Waveform Audio Reference</span></span>

<span data-ttu-id="03167-136">此區段會列出與波形音訊相關聯的函式、結構和訊息，這些功能是在 [ [多媒體參考](multimedia-reference.md)] 下記載。</span><span class="sxs-lookup"><span data-stu-id="03167-136">This section lists the functions, structures, and messages associated with waveform audio, which are documented under [Multimedia Reference](multimedia-reference.md).</span></span> <span data-ttu-id="03167-137">這些元素的分組方式如下。</span><span class="sxs-lookup"><span data-stu-id="03167-137">These elements are grouped as follows.</span></span>

## <a name="auxiliary-devices"></a><span data-ttu-id="03167-138">輔助裝置</span><span class="sxs-lookup"><span data-stu-id="03167-138">Auxiliary Devices</span></span>

-   [<span data-ttu-id="03167-139">**AUXCAPS**</span><span class="sxs-lookup"><span data-stu-id="03167-139">**AUXCAPS**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-auxcaps)
-   [<span data-ttu-id="03167-140">**auxGetDevCaps**</span><span class="sxs-lookup"><span data-stu-id="03167-140">**auxGetDevCaps**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-auxgetdevcaps)
-   [<span data-ttu-id="03167-141">**auxGetNumDevs**</span><span class="sxs-lookup"><span data-stu-id="03167-141">**auxGetNumDevs**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-auxgetnumdevs)
-   [<span data-ttu-id="03167-142">**auxGetVolume**</span><span class="sxs-lookup"><span data-stu-id="03167-142">**auxGetVolume**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-auxgetvolume)
-   [<span data-ttu-id="03167-143">**auxOutMessage**</span><span class="sxs-lookup"><span data-stu-id="03167-143">**auxOutMessage**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-auxoutmessage)
-   [<span data-ttu-id="03167-144">**auxSetVolume**</span><span class="sxs-lookup"><span data-stu-id="03167-144">**auxSetVolume**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-auxsetvolume)

## <a name="easy-playback"></a><span data-ttu-id="03167-145">輕鬆播放</span><span class="sxs-lookup"><span data-stu-id="03167-145">Easy Playback</span></span>

-   <span data-ttu-id="03167-146">[**PlaySound**](/previous-versions//dd743680(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="03167-146">[**PlaySound**](/previous-versions//dd743680(v=vs.85))</span></span>
-   <span data-ttu-id="03167-147">[**sndPlaySound**](/previous-versions//dd798676(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="03167-147">[**sndPlaySound**](/previous-versions//dd798676(v=vs.85))</span></span>

## <a name="errors"></a><span data-ttu-id="03167-148">Errors</span><span class="sxs-lookup"><span data-stu-id="03167-148">Errors</span></span>

-   [<span data-ttu-id="03167-149">**waveInGetErrorText**</span><span class="sxs-lookup"><span data-stu-id="03167-149">**waveInGetErrorText**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveingeterrortext)
-   [<span data-ttu-id="03167-150">**waveOutGetErrorText**</span><span class="sxs-lookup"><span data-stu-id="03167-150">**waveOutGetErrorText**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgeterrortext)

## <a name="opening-and-closing"></a><span data-ttu-id="03167-151">開啟和關閉</span><span class="sxs-lookup"><span data-stu-id="03167-151">Opening and Closing</span></span>

-   [<span data-ttu-id="03167-152">**PCMWAVEFORMAT**</span><span class="sxs-lookup"><span data-stu-id="03167-152">**PCMWAVEFORMAT**</span></span>](/windows/win32/api/mmreg/ns-mmreg-pcmwaveformat)
-   [<span data-ttu-id="03167-153">**MM \_ WIM \_ 關閉**</span><span class="sxs-lookup"><span data-stu-id="03167-153">**MM\_WIM\_CLOSE**</span></span>](mm-wim-close.md)
-   [<span data-ttu-id="03167-154">**MM \_ WIM \_ 開啟**</span><span class="sxs-lookup"><span data-stu-id="03167-154">**MM\_WIM\_OPEN**</span></span>](mm-wim-open.md)
-   [<span data-ttu-id="03167-155">**MM \_ WOM \_ 關閉**</span><span class="sxs-lookup"><span data-stu-id="03167-155">**MM\_WOM\_CLOSE**</span></span>](mm-wom-close.md)
-   [<span data-ttu-id="03167-156">**MM \_ WOM \_ 開啟**</span><span class="sxs-lookup"><span data-stu-id="03167-156">**MM\_WOM\_OPEN**</span></span>](mm-wom-open.md)
-   [<span data-ttu-id="03167-157">**WAVEFORMAT**</span><span class="sxs-lookup"><span data-stu-id="03167-157">**WAVEFORMAT**</span></span>](/windows/win32/api/mmreg/ns-mmreg-waveformat)
-   [<span data-ttu-id="03167-158">**WAVEFORMATEX**</span><span class="sxs-lookup"><span data-stu-id="03167-158">**WAVEFORMATEX**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex)
-   [<span data-ttu-id="03167-159">**waveInClose**</span><span class="sxs-lookup"><span data-stu-id="03167-159">**waveInClose**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveinclose)
-   <span data-ttu-id="03167-160">[**waveInProc**](/previous-versions//dd743849(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="03167-160">[**waveInProc**](/previous-versions//dd743849(v=vs.85))</span></span>
-   [<span data-ttu-id="03167-161">**waveInOpen**</span><span class="sxs-lookup"><span data-stu-id="03167-161">**waveInOpen**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen)
-   [<span data-ttu-id="03167-162">**waveOutClose**</span><span class="sxs-lookup"><span data-stu-id="03167-162">**waveOutClose**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutclose)
-   <span data-ttu-id="03167-163">[**waveOutProc**](/previous-versions//dd743869(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="03167-163">[**waveOutProc**](/previous-versions//dd743869(v=vs.85))</span></span>
-   [<span data-ttu-id="03167-164">**waveOutOpen**</span><span class="sxs-lookup"><span data-stu-id="03167-164">**waveOutOpen**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen)
-   [<span data-ttu-id="03167-165">**WIM \_ 關閉**</span><span class="sxs-lookup"><span data-stu-id="03167-165">**WIM\_CLOSE**</span></span>](wim-close.md)
-   [<span data-ttu-id="03167-166">**WIM \_ 開啟**</span><span class="sxs-lookup"><span data-stu-id="03167-166">**WIM\_OPEN**</span></span>](wim-open.md)
-   [<span data-ttu-id="03167-167">**WOM \_ 關閉**</span><span class="sxs-lookup"><span data-stu-id="03167-167">**WOM\_CLOSE**</span></span>](wom-close.md)
-   [<span data-ttu-id="03167-168">**WOM \_ 開啟**</span><span class="sxs-lookup"><span data-stu-id="03167-168">**WOM\_OPEN**</span></span>](wom-open.md)

## <a name="pitch"></a><span data-ttu-id="03167-169">音調</span><span class="sxs-lookup"><span data-stu-id="03167-169">Pitch</span></span>

-   [<span data-ttu-id="03167-170">**waveOutGetPitch**</span><span class="sxs-lookup"><span data-stu-id="03167-170">**waveOutGetPitch**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetpitch)
-   [<span data-ttu-id="03167-171">**waveOutSetPitch**</span><span class="sxs-lookup"><span data-stu-id="03167-171">**waveOutSetPitch**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutsetpitch)

## <a name="playback-rate"></a><span data-ttu-id="03167-172">播放速率</span><span class="sxs-lookup"><span data-stu-id="03167-172">Playback Rate</span></span>

-   [<span data-ttu-id="03167-173">**waveOutGetPlaybackRate**</span><span class="sxs-lookup"><span data-stu-id="03167-173">**waveOutGetPlaybackRate**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetplaybackrate)
-   [<span data-ttu-id="03167-174">**waveOutSetPlaybackRate**</span><span class="sxs-lookup"><span data-stu-id="03167-174">**waveOutSetPlaybackRate**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutsetplaybackrate)

## <a name="playback-progress"></a><span data-ttu-id="03167-175">播放進度</span><span class="sxs-lookup"><span data-stu-id="03167-175">Playback Progress</span></span>

-   [<span data-ttu-id="03167-176">**MM \_ WOM \_ 完成**</span><span class="sxs-lookup"><span data-stu-id="03167-176">**MM\_WOM\_DONE**</span></span>](mm-wom-done.md)
-   [<span data-ttu-id="03167-177">**waveOutBreakLoop**</span><span class="sxs-lookup"><span data-stu-id="03167-177">**waveOutBreakLoop**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutbreakloop)
-   [<span data-ttu-id="03167-178">**waveOutPause**</span><span class="sxs-lookup"><span data-stu-id="03167-178">**waveOutPause**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutpause)
-   [<span data-ttu-id="03167-179">**waveOutReset**</span><span class="sxs-lookup"><span data-stu-id="03167-179">**waveOutReset**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset)
-   [<span data-ttu-id="03167-180">**waveOutRestart**</span><span class="sxs-lookup"><span data-stu-id="03167-180">**waveOutRestart**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutrestart)
-   [<span data-ttu-id="03167-181">**WOM \_ 完成**</span><span class="sxs-lookup"><span data-stu-id="03167-181">**WOM\_DONE**</span></span>](wom-done.md)

## <a name="playing"></a><span data-ttu-id="03167-182">正在播放</span><span class="sxs-lookup"><span data-stu-id="03167-182">Playing</span></span>

-   [<span data-ttu-id="03167-183">**MM \_ WOM \_ 完成**</span><span class="sxs-lookup"><span data-stu-id="03167-183">**MM\_WOM\_DONE**</span></span>](mm-wom-done.md)
-   [<span data-ttu-id="03167-184">**WAVEHDR**</span><span class="sxs-lookup"><span data-stu-id="03167-184">**WAVEHDR**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr)
-   [<span data-ttu-id="03167-185">**waveOutPrepareHeader**</span><span class="sxs-lookup"><span data-stu-id="03167-185">**waveOutPrepareHeader**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutprepareheader)
-   [<span data-ttu-id="03167-186">**waveOutUnprepareHeader**</span><span class="sxs-lookup"><span data-stu-id="03167-186">**waveOutUnprepareHeader**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutunprepareheader)
-   [<span data-ttu-id="03167-187">**waveOutWrite**</span><span class="sxs-lookup"><span data-stu-id="03167-187">**waveOutWrite**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite)
-   [<span data-ttu-id="03167-188">**WOM \_ 完成**</span><span class="sxs-lookup"><span data-stu-id="03167-188">**WOM\_DONE**</span></span>](wom-done.md)

## <a name="querying-a-device"></a><span data-ttu-id="03167-189">查詢裝置</span><span class="sxs-lookup"><span data-stu-id="03167-189">Querying a Device</span></span>

-   [<span data-ttu-id="03167-190">**WAVEINCAPS**</span><span class="sxs-lookup"><span data-stu-id="03167-190">**WAVEINCAPS**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-waveincaps)
-   [<span data-ttu-id="03167-191">**waveInGetDevCaps**</span><span class="sxs-lookup"><span data-stu-id="03167-191">**waveInGetDevCaps**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveingetdevcaps)
-   [<span data-ttu-id="03167-192">**waveInGetNumDevs**</span><span class="sxs-lookup"><span data-stu-id="03167-192">**waveInGetNumDevs**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveingetnumdevs)
-   [<span data-ttu-id="03167-193">**WAVEOUTCAPS**</span><span class="sxs-lookup"><span data-stu-id="03167-193">**WAVEOUTCAPS**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-waveoutcaps)
-   [<span data-ttu-id="03167-194">**waveOutGetDevCaps**</span><span class="sxs-lookup"><span data-stu-id="03167-194">**waveOutGetDevCaps**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetdevcaps)
-   [<span data-ttu-id="03167-195">**waveOutGetNumDevs**</span><span class="sxs-lookup"><span data-stu-id="03167-195">**waveOutGetNumDevs**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetnumdevs)

## <a name="recording"></a><span data-ttu-id="03167-196">記錄</span><span class="sxs-lookup"><span data-stu-id="03167-196">Recording</span></span>

-   [<span data-ttu-id="03167-197">**MM \_ WIM \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="03167-197">**MM\_WIM\_DATA**</span></span>](mm-wim-data.md)
-   [<span data-ttu-id="03167-198">**waveInAddBuffer**</span><span class="sxs-lookup"><span data-stu-id="03167-198">**waveInAddBuffer**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveinaddbuffer)
-   [<span data-ttu-id="03167-199">**waveInPrepareHeader**</span><span class="sxs-lookup"><span data-stu-id="03167-199">**waveInPrepareHeader**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveinprepareheader)
-   [<span data-ttu-id="03167-200">**waveInReset**</span><span class="sxs-lookup"><span data-stu-id="03167-200">**waveInReset**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveinreset)
-   [<span data-ttu-id="03167-201">**waveInStart**</span><span class="sxs-lookup"><span data-stu-id="03167-201">**waveInStart**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveinstart)
-   [<span data-ttu-id="03167-202">**waveInStop**</span><span class="sxs-lookup"><span data-stu-id="03167-202">**waveInStop**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveinstop)
-   [<span data-ttu-id="03167-203">**waveInUnprepareHeader**</span><span class="sxs-lookup"><span data-stu-id="03167-203">**waveInUnprepareHeader**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveinunprepareheader)
-   [<span data-ttu-id="03167-204">**WIM \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="03167-204">**WIM\_DATA**</span></span>](wim-data.md)

## <a name="retrieving-device-identifiers"></a><span data-ttu-id="03167-205">正在抓取裝置識別碼</span><span class="sxs-lookup"><span data-stu-id="03167-205">Retrieving Device Identifiers</span></span>

-   [<span data-ttu-id="03167-206">**waveInGetID**</span><span class="sxs-lookup"><span data-stu-id="03167-206">**waveInGetID**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveingetid)
-   [<span data-ttu-id="03167-207">**waveOutGetID**</span><span class="sxs-lookup"><span data-stu-id="03167-207">**waveOutGetID**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetid)

## <a name="retrieving-the-current-position"></a><span data-ttu-id="03167-208">正在抓取目前的位置</span><span class="sxs-lookup"><span data-stu-id="03167-208">Retrieving the Current Position</span></span>

-   [<span data-ttu-id="03167-209">**waveInGetPosition**</span><span class="sxs-lookup"><span data-stu-id="03167-209">**waveInGetPosition**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveingetposition)
-   [<span data-ttu-id="03167-210">**waveOutGetPosition**</span><span class="sxs-lookup"><span data-stu-id="03167-210">**waveOutGetPosition**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetposition)

## <a name="sending-custom-messages"></a><span data-ttu-id="03167-211">傳送自訂訊息</span><span class="sxs-lookup"><span data-stu-id="03167-211">Sending Custom Messages</span></span>

-   [<span data-ttu-id="03167-212">**waveInMessage**</span><span class="sxs-lookup"><span data-stu-id="03167-212">**waveInMessage**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveinmessage)
-   [<span data-ttu-id="03167-213">**waveOutMessage**</span><span class="sxs-lookup"><span data-stu-id="03167-213">**waveOutMessage**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutmessage)

## <a name="volume"></a><span data-ttu-id="03167-214">磁碟區</span><span class="sxs-lookup"><span data-stu-id="03167-214">Volume</span></span>

-   [<span data-ttu-id="03167-215">**waveOutGetVolume**</span><span class="sxs-lookup"><span data-stu-id="03167-215">**waveOutGetVolume**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetvolume)
-   [<span data-ttu-id="03167-216">**waveOutSetVolume**</span><span class="sxs-lookup"><span data-stu-id="03167-216">**waveOutSetVolume**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutsetvolume)

## <a name="related-topics"></a><span data-ttu-id="03167-217">相關主題</span><span class="sxs-lookup"><span data-stu-id="03167-217">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="03167-218">波形音訊</span><span class="sxs-lookup"><span data-stu-id="03167-218">Waveform Audio</span></span>](waveform-audio.md)
</dt> </dl>

 

 