---
title: 裝置和資料類型
description: 裝置和資料類型
ms.assetid: 46247983-19c3-4c7a-a615-ba6cd8bd3289
keywords:
- 波形音訊，開啟輸出裝置
- 波形-音訊介面，開啟輸出裝置
- 開啟波形音訊輸出裝置
- 波形音訊，查詢輸出裝置
- 波形-音訊介面，查詢輸出裝置
- 查詢波形音訊輸出裝置
- 波形音訊、裝置控點
- 波形-音訊介面、裝置控點
- 波形音訊、裝置識別碼
- 波形-音訊介面、裝置識別碼
- 波形音訊，輸出資料類型
- 波形-音訊介面、輸出資料類型
- 波形音訊，資料格式
- 波形-音訊介面、資料格式
- 寫入波形-音訊資料
- 波形音訊，寫入資料
- 波形-音訊介面，寫入資料
- PCM 波形-音訊資料
- 波形音訊、PCM 資料
- 波形-音訊介面、PCM 資料
- 波形音訊，關閉輸出裝置
- 波形-音訊介面，關閉輸出裝置
- 關閉波形-音訊輸出裝置
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2abe0c2c20c52f4498316fb619885d41f85e41d6
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120243"
---
# <a name="devices-and-data-types"></a><span data-ttu-id="ec622-126">裝置和資料類型</span><span class="sxs-lookup"><span data-stu-id="ec622-126">Devices and Data Types</span></span>

<span data-ttu-id="ec622-127">本節說明如何使用波形音訊裝置，並包含如何開啟、關閉和查詢其功能的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="ec622-127">This section describes working with waveform-audio devices, and includes information on how to open, close and query them for their capabilities.</span></span> <span data-ttu-id="ec622-128">它也會說明如何使用裝置控制碼和裝置識別碼，來追蹤系統中的裝置。</span><span class="sxs-lookup"><span data-stu-id="ec622-128">It also describes how to keep track of the devices in a system by using device handles and device identifiers.</span></span>

## <a name="opening-waveform-audio-output-devices"></a><span data-ttu-id="ec622-129">開啟 Waveform-Audio 輸出裝置</span><span class="sxs-lookup"><span data-stu-id="ec622-129">Opening Waveform-Audio Output Devices</span></span>

<span data-ttu-id="ec622-130">使用 [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) 函式來開啟波形音訊輸出裝置以進行播放。</span><span class="sxs-lookup"><span data-stu-id="ec622-130">Use the [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) function to open a waveform-audio output device for playback.</span></span> <span data-ttu-id="ec622-131">此函式會開啟與指定裝置識別碼相關聯的裝置，並藉由撰寫指定記憶體位置的控制碼，傳回開啟裝置的控制碼。</span><span class="sxs-lookup"><span data-stu-id="ec622-131">This function opens the device associated with the specified device identifier and returns a handle of the open device by writing the handle of a specified memory location.</span></span>

<span data-ttu-id="ec622-132">有些多媒體電腦有多個波形音訊輸出裝置。</span><span class="sxs-lookup"><span data-stu-id="ec622-132">Some multimedia computers have multiple waveform-audio output devices.</span></span> <span data-ttu-id="ec622-133">除非您想要在系統中開啟特定的波形音訊輸出裝置，否則 \_ 當您開啟裝置時，應該針對裝置識別碼使用 WAVE 對應程式旗標。</span><span class="sxs-lookup"><span data-stu-id="ec622-133">Unless you want to open a specific waveform-audio output device in a system, you should use the WAVE\_MAPPER flag for the device identifier when you open a device.</span></span> <span data-ttu-id="ec622-134">**WaveOutOpen** 函式會在系統中選擇最能播放指定資料格式的裝置。</span><span class="sxs-lookup"><span data-stu-id="ec622-134">The **waveOutOpen** function chooses the device in the system that is best able to play the specified data format.</span></span>

## <a name="querying-audio-devices"></a><span data-ttu-id="ec622-135">查詢音訊裝置</span><span class="sxs-lookup"><span data-stu-id="ec622-135">Querying Audio Devices</span></span>

<span data-ttu-id="ec622-136">Windows 提供下列功能來判斷系統中有多少裝置具有特定類型。</span><span class="sxs-lookup"><span data-stu-id="ec622-136">Windows provides the following functions to determine how many devices of a certain type are available in a system.</span></span>



| <span data-ttu-id="ec622-137">函式</span><span class="sxs-lookup"><span data-stu-id="ec622-137">Function</span></span>                                       | <span data-ttu-id="ec622-138">描述</span><span class="sxs-lookup"><span data-stu-id="ec622-138">Description</span></span>                                                                  |
|------------------------------------------------|------------------------------------------------------------------------------|
| [<span data-ttu-id="ec622-139">**auxGetNumDevs**</span><span class="sxs-lookup"><span data-stu-id="ec622-139">**auxGetNumDevs**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-auxgetnumdevs)         | <span data-ttu-id="ec622-140">抓取系統中出現的輔助輸出裝置數目。</span><span class="sxs-lookup"><span data-stu-id="ec622-140">Retrieves the number of auxiliary output devices present in the system.</span></span>      |
| [<span data-ttu-id="ec622-141">**waveInGetNumDevs**</span><span class="sxs-lookup"><span data-stu-id="ec622-141">**waveInGetNumDevs**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveingetnumdevs)   | <span data-ttu-id="ec622-142">抓取系統中顯示的波形音訊輸入裝置數目。</span><span class="sxs-lookup"><span data-stu-id="ec622-142">Retrieves the number of waveform-audio input devices present in the system.</span></span>  |
| [<span data-ttu-id="ec622-143">**waveOutGetNumDevs**</span><span class="sxs-lookup"><span data-stu-id="ec622-143">**waveOutGetNumDevs**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetnumdevs) | <span data-ttu-id="ec622-144">抓取系統中出現的波形音訊輸出裝置數目。</span><span class="sxs-lookup"><span data-stu-id="ec622-144">Retrieves the number of waveform-audio output devices present in the system.</span></span> |



 

<span data-ttu-id="ec622-145">音訊裝置是由裝置識別碼來識別。</span><span class="sxs-lookup"><span data-stu-id="ec622-145">Audio devices are identified by a device identifier.</span></span> <span data-ttu-id="ec622-146">裝置識別碼是由系統中的裝置數目隱含決定。</span><span class="sxs-lookup"><span data-stu-id="ec622-146">The device identifier is determined implicitly from the number of devices present in a system.</span></span> <span data-ttu-id="ec622-147">裝置識別碼的範圍介於0到1之間，且小於裝置數目。</span><span class="sxs-lookup"><span data-stu-id="ec622-147">Device identifiers range from zero to one less than the number of devices present.</span></span> <span data-ttu-id="ec622-148">例如，如果系統中有兩個波形音訊輸出裝置，則有效的裝置識別碼為0和1。</span><span class="sxs-lookup"><span data-stu-id="ec622-148">For example, if there are two waveform-audio output devices in a system, valid device identifiers are 0 and 1.</span></span>

<span data-ttu-id="ec622-149">判斷系統中有多少個特定類型的裝置之後，您可以使用下列其中一項功能來查詢每個裝置的功能。</span><span class="sxs-lookup"><span data-stu-id="ec622-149">After you determine how many devices of a certain type are present in a system, you can use one of the following functions to query the capabilities of each device.</span></span>



| <span data-ttu-id="ec622-150">函式</span><span class="sxs-lookup"><span data-stu-id="ec622-150">Function</span></span>                                       | <span data-ttu-id="ec622-151">描述</span><span class="sxs-lookup"><span data-stu-id="ec622-151">Description</span></span>                                                             |
|------------------------------------------------|-------------------------------------------------------------------------|
| [<span data-ttu-id="ec622-152">**auxGetDevCaps**</span><span class="sxs-lookup"><span data-stu-id="ec622-152">**auxGetDevCaps**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-auxgetdevcaps)         | <span data-ttu-id="ec622-153">抓取指定之輔助輸出裝置的功能。</span><span class="sxs-lookup"><span data-stu-id="ec622-153">Retrieves the capabilities of a specified auxiliary output device.</span></span>      |
| [<span data-ttu-id="ec622-154">**waveInGetDevCaps**</span><span class="sxs-lookup"><span data-stu-id="ec622-154">**waveInGetDevCaps**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveingetdevcaps)   | <span data-ttu-id="ec622-155">抓取指定之波形音訊輸入裝置的功能。</span><span class="sxs-lookup"><span data-stu-id="ec622-155">Retrieves the capabilities of a specified waveform-audio input device.</span></span>  |
| [<span data-ttu-id="ec622-156">**waveOutGetDevCaps**</span><span class="sxs-lookup"><span data-stu-id="ec622-156">**waveOutGetDevCaps**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetdevcaps) | <span data-ttu-id="ec622-157">抓取指定之波形音訊輸出裝置的功能。</span><span class="sxs-lookup"><span data-stu-id="ec622-157">Retrieves the capabilities of a specified waveform-audio output device.</span></span> |



 

<span data-ttu-id="ec622-158">這些函式中的每一個都會以指定裝置功能的相關資訊填入結構。</span><span class="sxs-lookup"><span data-stu-id="ec622-158">Each of these functions fills a structure with information about the capabilities of a specified device.</span></span> <span data-ttu-id="ec622-159">下表列出對應至每個函數的結構。</span><span class="sxs-lookup"><span data-stu-id="ec622-159">The following table lists the structures that correspond to each of these functions.</span></span>



|  <span data-ttu-id="ec622-160">函式</span><span class="sxs-lookup"><span data-stu-id="ec622-160">Function</span></span>                                              |  <span data-ttu-id="ec622-161">結構</span><span class="sxs-lookup"><span data-stu-id="ec622-161">Structure</span></span>                                  |
|------------------------------------------------|------------------------------------|
| [<span data-ttu-id="ec622-162">**auxGetDevCaps**</span><span class="sxs-lookup"><span data-stu-id="ec622-162">**auxGetDevCaps**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-auxgetdevcaps)         | [<span data-ttu-id="ec622-163">**AUXCAPS**</span><span class="sxs-lookup"><span data-stu-id="ec622-163">**AUXCAPS**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-auxcaps)         |
| [<span data-ttu-id="ec622-164">**waveInGetDevCaps**</span><span class="sxs-lookup"><span data-stu-id="ec622-164">**waveInGetDevCaps**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveingetdevcaps)   | [<span data-ttu-id="ec622-165">**WAVEINCAPS**</span><span class="sxs-lookup"><span data-stu-id="ec622-165">**WAVEINCAPS**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-waveincaps)   |
| [<span data-ttu-id="ec622-166">**waveOutGetDevCaps**</span><span class="sxs-lookup"><span data-stu-id="ec622-166">**waveOutGetDevCaps**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetdevcaps) | [<span data-ttu-id="ec622-167">**WAVEOUTCAPS**</span><span class="sxs-lookup"><span data-stu-id="ec622-167">**WAVEOUTCAPS**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-waveoutcaps) |



 

<span data-ttu-id="ec622-168">標準格式會列在 **WAVEOUTCAPS** 結構的 **dwFormats** 成員中。</span><span class="sxs-lookup"><span data-stu-id="ec622-168">Standard formats are listed in the **dwFormats** member of the **WAVEOUTCAPS** structure.</span></span> <span data-ttu-id="ec622-169">波形-音訊裝置可支援非標準格式。</span><span class="sxs-lookup"><span data-stu-id="ec622-169">Waveform-audio devices can support nonstandard formats.</span></span> <span data-ttu-id="ec622-170">若要判斷裝置是否支援特定格式 (標準或非標準) ，您可以使用 WAVE [](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) \_ 格式查詢旗標來呼叫 waveOutOpen 函數 \_ 。</span><span class="sxs-lookup"><span data-stu-id="ec622-170">To determine whether a particular format (standard or nonstandard) is supported by a device, you can call the [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) function with the WAVE\_FORMAT\_QUERY flag.</span></span> <span data-ttu-id="ec622-171">此旗標不會開啟裝置。</span><span class="sxs-lookup"><span data-stu-id="ec622-171">This flag does not open the device.</span></span> <span data-ttu-id="ec622-172">您可以在傳遞給 **waveOutOpen** 的 *pwfx* 參數所指向的 [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex)結構中指定有問題的格式。</span><span class="sxs-lookup"><span data-stu-id="ec622-172">You specify the format in question in the [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) structure pointed to by the *pwfx* parameter passed to **waveOutOpen**.</span></span>

<span data-ttu-id="ec622-173">波形-音訊輸出裝置所支援的功能不同。</span><span class="sxs-lookup"><span data-stu-id="ec622-173">Waveform-audio output devices vary in the capabilities they support.</span></span> <span data-ttu-id="ec622-174">[**WAVEOUTCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-waveoutcaps)結構的 **dwSupport** 成員會指出裝置是否支援磁片區和音調變更這類功能。</span><span class="sxs-lookup"><span data-stu-id="ec622-174">The **dwSupport** member of the [**WAVEOUTCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-waveoutcaps) structure indicates whether a device supports such capabilities as volume and pitch changes.</span></span>

## <a name="device-handles-and-device-identifiers"></a><span data-ttu-id="ec622-175">裝置控制碼和裝置識別碼</span><span class="sxs-lookup"><span data-stu-id="ec622-175">Device Handles and Device Identifiers</span></span>

<span data-ttu-id="ec622-176">開啟音訊裝置的每個函式都會指定裝置識別碼、記憶體位置的指標，以及每種裝置類型特有的一些參數。</span><span class="sxs-lookup"><span data-stu-id="ec622-176">Each function that opens an audio device specifies a device identifier, a pointer to a memory location, and some parameters that are unique to each type of device.</span></span> <span data-ttu-id="ec622-177">記憶體位置會以裝置控制碼填滿。</span><span class="sxs-lookup"><span data-stu-id="ec622-177">The memory location is filled with a device handle.</span></span> <span data-ttu-id="ec622-178">呼叫其他音訊函式時，請使用此裝置控制碼來識別開啟的音訊裝置。</span><span class="sxs-lookup"><span data-stu-id="ec622-178">Use this device handle to identify the open audio device when calling other audio functions.</span></span>

<span data-ttu-id="ec622-179">音訊裝置的識別碼和控制碼之間的差異很微妙，但很重要：</span><span class="sxs-lookup"><span data-stu-id="ec622-179">The difference between identifiers and handles for audio devices is subtle but important:</span></span>

-   <span data-ttu-id="ec622-180">裝置識別碼是由系統中出現的裝置數目隱含決定。</span><span class="sxs-lookup"><span data-stu-id="ec622-180">Device identifiers are determined implicitly from the number of devices present in a system.</span></span> <span data-ttu-id="ec622-181">您可以使用 [**auxGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetnumdevs)、 [**waveInGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetnumdevs)或 [**waveOutGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetnumdevs) 函數來取得這個數位。</span><span class="sxs-lookup"><span data-stu-id="ec622-181">This number is obtained by using the [**auxGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetnumdevs), [**waveInGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetnumdevs), or [**waveOutGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetnumdevs) function.</span></span>
-   <span data-ttu-id="ec622-182">使用 [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) 或 [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) 函式開啟設備磁碟機時，會傳回裝置控制碼。</span><span class="sxs-lookup"><span data-stu-id="ec622-182">Device handles are returned when device drivers are opened by using the [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) or [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) function.</span></span>

<span data-ttu-id="ec622-183">沒有可開啟或關閉輔助音訊裝置的函式。</span><span class="sxs-lookup"><span data-stu-id="ec622-183">There are no functions that open or close auxiliary audio devices.</span></span> <span data-ttu-id="ec622-184">因為沒有任何與它們相關聯的連續資料傳輸，所以不需要開啟和關閉輔助音訊裝置，例如波形音訊裝置。</span><span class="sxs-lookup"><span data-stu-id="ec622-184">Auxiliary audio devices need not be opened and closed like waveform-audio devices because there is no continuous data transfer associated with them.</span></span> <span data-ttu-id="ec622-185">所有輔助音訊功能都會使用裝置識別碼來識別裝置。</span><span class="sxs-lookup"><span data-stu-id="ec622-185">All auxiliary audio functions use device identifiers to identify devices.</span></span>

## <a name="waveform-audio-output-data-types"></a><span data-ttu-id="ec622-186">Waveform-Audio 輸出資料類型</span><span class="sxs-lookup"><span data-stu-id="ec622-186">Waveform-Audio Output Data Types</span></span>

<span data-ttu-id="ec622-187">下列資料類型是針對波形音訊輸出函式所定義。</span><span class="sxs-lookup"><span data-stu-id="ec622-187">The following data types are defined for waveform-audio output functions.</span></span>



| <span data-ttu-id="ec622-188">類型</span><span class="sxs-lookup"><span data-stu-id="ec622-188">Type</span></span>                                 | <span data-ttu-id="ec622-189">描述</span><span class="sxs-lookup"><span data-stu-id="ec622-189">Description</span></span>                                                                                                                                                   |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec622-190">**HWAVEOUT**</span><span class="sxs-lookup"><span data-stu-id="ec622-190">**HWAVEOUT**</span></span>                         | <span data-ttu-id="ec622-191">開啟波形音訊輸出裝置的控制碼。</span><span class="sxs-lookup"><span data-stu-id="ec622-191">Handle to an open waveform-audio output device.</span></span>                                                                                                               |
| [<span data-ttu-id="ec622-192">**WAVEFORMATEX**</span><span class="sxs-lookup"><span data-stu-id="ec622-192">**WAVEFORMATEX**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) | <span data-ttu-id="ec622-193">結構，指定特定波形音訊輸入裝置所支援的資料格式。</span><span class="sxs-lookup"><span data-stu-id="ec622-193">Structure that specifies the data formats supported by a particular waveform-audio input device.</span></span> <span data-ttu-id="ec622-194">此結構也會 usedfor 波形-音訊輸入裝置。</span><span class="sxs-lookup"><span data-stu-id="ec622-194">This structure is also usedfor waveform-audio input devices.</span></span> |
| [<span data-ttu-id="ec622-195">**WAVEHDR**</span><span class="sxs-lookup"><span data-stu-id="ec622-195">**WAVEHDR**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr)           | <span data-ttu-id="ec622-196">結構，用來做為波形音訊輸入資料區塊的標頭。</span><span class="sxs-lookup"><span data-stu-id="ec622-196">Structure used as a header for a block of waveform-audio input data.</span></span> <span data-ttu-id="ec622-197">此結構也可用於波形音訊輸入裝置。</span><span class="sxs-lookup"><span data-stu-id="ec622-197">This structure is also used for waveform-audio input devices.</span></span>                            |
| [<span data-ttu-id="ec622-198">**WAVEOUTCAPS**</span><span class="sxs-lookup"><span data-stu-id="ec622-198">**WAVEOUTCAPS**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-waveoutcaps)   | <span data-ttu-id="ec622-199">用來查詢特定波形音訊輸出裝置功能的結構。</span><span class="sxs-lookup"><span data-stu-id="ec622-199">Structure used to query the capabilities of a particular waveform-audio output device.</span></span>                                                                        |



 

## <a name="specifying-waveform-audio-data-formats"></a><span data-ttu-id="ec622-200">指定 Waveform-Audio 資料格式</span><span class="sxs-lookup"><span data-stu-id="ec622-200">Specifying Waveform-Audio Data Formats</span></span>

<span data-ttu-id="ec622-201">當您呼叫 [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) 函式來開啟設備磁碟機以供播放，或查詢驅動程式是否支援特定的資料格式時，請使用 *pwfx* 參數來指定 [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) 結構的指標，其中包含要求的波形-音訊資料格式。</span><span class="sxs-lookup"><span data-stu-id="ec622-201">When you call the [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) function to open a device driver for playback or to query whether the driver supports a particular data format, use the *pwfx* parameter to specify a pointer to a [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) structure containing the requested waveform-audio data format.</span></span> <span data-ttu-id="ec622-202">**WAVEFORMATEX** 會取代 [**WAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-waveformat) 和 [**PCMWAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-pcmwaveformat) 結構。</span><span class="sxs-lookup"><span data-stu-id="ec622-202">**WAVEFORMATEX** supersedes the [**WAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-waveformat) and [**PCMWAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-pcmwaveformat) structures.</span></span>

<span data-ttu-id="ec622-203">如果音訊資料分成兩個以上的通道，或其樣本大小不是8的倍數，您應該使用 [**WAVEFORMATEXTENSIBLE**](/windows/win32/api/mmreg/ns-mmreg-waveformatextensible)。</span><span class="sxs-lookup"><span data-stu-id="ec622-203">For audio data that is separated into more than two channels or has a sample size that is not a multiple of 8, you should use [**WAVEFORMATEXTENSIBLE**](/windows/win32/api/mmreg/ns-mmreg-waveformatextensible).</span></span> <span data-ttu-id="ec622-204">此結構只會設定 **WAVEFORMATEX** 的 **cbSize** 成員所指向的額外位元組，以提供有關格式的額外資訊。</span><span class="sxs-lookup"><span data-stu-id="ec622-204">This structure simply configures the extra bytes pointed to by the **cbSize** member of **WAVEFORMATEX** to give extra information about the format.</span></span> <span data-ttu-id="ec622-205">**WAVEFORMATEXTENSIBLE** 可以轉換成 **WAVEFORMATEX**。</span><span class="sxs-lookup"><span data-stu-id="ec622-205">**WAVEFORMATEXTENSIBLE** can be cast as **WAVEFORMATEX**.</span></span>

<span data-ttu-id="ec622-206">另外還有兩種剪貼簿格式可供您用來代表音訊資料： CF \_ WAVE 和 cf \_ RIFF。</span><span class="sxs-lookup"><span data-stu-id="ec622-206">There are also two clipboard formats you can use to represent audio data: CF\_WAVE and CF\_RIFF.</span></span> <span data-ttu-id="ec622-207">使用 CF \_ WAVE 格式來代表其中一種標準格式的資料，例如 11 khz 或 22 KHZ PCM。</span><span class="sxs-lookup"><span data-stu-id="ec622-207">Use the CF\_WAVE format to represent data in one of the standard formats, such as 11 kHz or 22 kHz PCM.</span></span> <span data-ttu-id="ec622-208">使用 CF \_ RIFF 格式來表示更複雜的資料格式，而這些格式無法表示為標準波形-音訊檔案。</span><span class="sxs-lookup"><span data-stu-id="ec622-208">Use the CF\_RIFF format to represent more complex data formats that cannot be represented as standard waveform-audio files.</span></span>

## <a name="writing-waveform-audio-data"></a><span data-ttu-id="ec622-209">寫入 Waveform-Audio 資料</span><span class="sxs-lookup"><span data-stu-id="ec622-209">Writing Waveform-Audio Data</span></span>

<span data-ttu-id="ec622-210">成功開啟波形音訊輸出設備磁碟機之後，您就可以開始播放音效。</span><span class="sxs-lookup"><span data-stu-id="ec622-210">After successfully opening a waveform-audio output device driver, you can begin playing a sound.</span></span> <span data-ttu-id="ec622-211">Windows 提供 [**waveOutWrite**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite) 函式，可將資料區區塊轉送到波形音訊輸出裝置。</span><span class="sxs-lookup"><span data-stu-id="ec622-211">Windows provides the [**waveOutWrite**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite) function for sending data blocks to waveform-audio output devices.</span></span>

<span data-ttu-id="ec622-212">使用 [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) 結構來指定您使用 **waveOutWrite** 傳送的波形音訊資料區塊。</span><span class="sxs-lookup"><span data-stu-id="ec622-212">Use the [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) structure to specify the waveform-audio data block you are sending using **waveOutWrite**.</span></span> <span data-ttu-id="ec622-213">此結構包含鎖定資料區塊的指標、資料區塊的長度，以及某些旗標。</span><span class="sxs-lookup"><span data-stu-id="ec622-213">This structure contains a pointer to a locked data block, the length of the data block, and some flags.</span></span> <span data-ttu-id="ec622-214">您必須先備妥此資料區塊，才能使用它。如需準備資料區塊的相關資訊，請參閱 [音訊資料區塊](audio-data-blocks.md)。</span><span class="sxs-lookup"><span data-stu-id="ec622-214">This data block must be prepared before you use it; for information about preparing a data block, see [Audio Data Blocks](audio-data-blocks.md).</span></span>

<span data-ttu-id="ec622-215">使用 **waveOutWrite** 將資料區區塊轉送到輸出裝置之後，您必須等到設備磁碟機完成後再釋放資料區塊。</span><span class="sxs-lookup"><span data-stu-id="ec622-215">After you send a data block to an output device by using **waveOutWrite**, you must wait until the device driver is finished with the data block before freeing it.</span></span> <span data-ttu-id="ec622-216">如果您要傳送多個資料區塊，則必須監視資料區塊的完成，以瞭解何時傳送其他區塊。</span><span class="sxs-lookup"><span data-stu-id="ec622-216">If you are sending multiple data blocks, you must monitor the completion of data blocks to know when to send additional blocks.</span></span> <span data-ttu-id="ec622-217">如需資料區塊的詳細資訊，請參閱 [音訊資料區塊](audio-data-blocks.md)。</span><span class="sxs-lookup"><span data-stu-id="ec622-217">For more information about data blocks, see [Audio Data Blocks](audio-data-blocks.md).</span></span>

## <a name="pcm-waveform-audio-data-format"></a><span data-ttu-id="ec622-218">PCM Waveform-Audio 資料格式</span><span class="sxs-lookup"><span data-stu-id="ec622-218">PCM Waveform-Audio Data Format</span></span>

<span data-ttu-id="ec622-219">[**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr)結構 Pointsetts 的 **lpData** 成員會至波形音訊資料樣本。</span><span class="sxs-lookup"><span data-stu-id="ec622-219">The **lpData** member of the [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) structure pointsetts to the waveform-audio data samples.</span></span> <span data-ttu-id="ec622-220">若為8位 PCM 資料，每個範例都會以單一不帶正負號的資料位元組來表示。</span><span class="sxs-lookup"><span data-stu-id="ec622-220">For 8-bit PCM data, each sample is represented by a single unsigned data byte.</span></span> <span data-ttu-id="ec622-221">若是16位 PCM 資料，每個範例都會以16位帶正負號的值表示。</span><span class="sxs-lookup"><span data-stu-id="ec622-221">For 16-bit PCM data, each sample is represented by a 16-bit signed value.</span></span> <span data-ttu-id="ec622-222">下表摘要說明 PCM 波形-音訊資料的最大值、最小值和中點值。</span><span class="sxs-lookup"><span data-stu-id="ec622-222">The following table summarizes the maximum, minimum, and midpoint values for PCM waveform-audio data.</span></span>



| <span data-ttu-id="ec622-223">資料格式</span><span class="sxs-lookup"><span data-stu-id="ec622-223">Data format</span></span> | <span data-ttu-id="ec622-224">最大值</span><span class="sxs-lookup"><span data-stu-id="ec622-224">Maximum value</span></span>   | <span data-ttu-id="ec622-225">最小值</span><span class="sxs-lookup"><span data-stu-id="ec622-225">Minimum value</span></span>    | <span data-ttu-id="ec622-226">中點值</span><span class="sxs-lookup"><span data-stu-id="ec622-226">Midpoint value</span></span> |
|-------------|-----------------|------------------|----------------|
| <span data-ttu-id="ec622-227">8位 PCM</span><span class="sxs-lookup"><span data-stu-id="ec622-227">8-bit PCM</span></span>   | <span data-ttu-id="ec622-228">255 (0xFF) </span><span class="sxs-lookup"><span data-stu-id="ec622-228">255 (0xFF)</span></span>      | <span data-ttu-id="ec622-229">0</span><span class="sxs-lookup"><span data-stu-id="ec622-229">0</span></span>                | <span data-ttu-id="ec622-230">128 (0x80) </span><span class="sxs-lookup"><span data-stu-id="ec622-230">128 (0x80)</span></span>     |
| <span data-ttu-id="ec622-231">16位 PCM</span><span class="sxs-lookup"><span data-stu-id="ec622-231">16-bit PCM</span></span>  | <span data-ttu-id="ec622-232">32767 (0x7FFF) </span><span class="sxs-lookup"><span data-stu-id="ec622-232">32,767 (0x7FFF)</span></span> | <span data-ttu-id="ec622-233">– 32768 (0x8000) </span><span class="sxs-lookup"><span data-stu-id="ec622-233">–32,768 (0x8000)</span></span> | <span data-ttu-id="ec622-234">0</span><span class="sxs-lookup"><span data-stu-id="ec622-234">0</span></span>              |



 

## <a name="pcm-data-packing"></a><span data-ttu-id="ec622-235">PCM 資料封裝</span><span class="sxs-lookup"><span data-stu-id="ec622-235">PCM Data Packing</span></span>

<span data-ttu-id="ec622-236">資料位元組的順序會依8位和16位格式，以及 mono 與身歷聲格式而有所不同。</span><span class="sxs-lookup"><span data-stu-id="ec622-236">The order of the data bytes varies between 8-bit and 16-bit formats and between mono and stereo formats.</span></span> <span data-ttu-id="ec622-237">下列清單說明不同 PCM 波形-音訊資料格式的資料封裝。</span><span class="sxs-lookup"><span data-stu-id="ec622-237">The following list describes data packing for the different PCM waveform-audio data formats.</span></span>



| <span data-ttu-id="ec622-238">PCM 波形-音訊格式</span><span class="sxs-lookup"><span data-stu-id="ec622-238">PCM waveform-audio format</span></span> | <span data-ttu-id="ec622-239">描述</span><span class="sxs-lookup"><span data-stu-id="ec622-239">Description</span></span>                                                                                                                                                                                                                                                                                                                                     |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec622-240">8位 mono</span><span class="sxs-lookup"><span data-stu-id="ec622-240">8-bit mono</span></span>                | <span data-ttu-id="ec622-241">每個範例都是一個對應至單一音訊通道的1個位元組。</span><span class="sxs-lookup"><span data-stu-id="ec622-241">Each sample is 1 byte that corresponds to a single audio channel.</span></span> <span data-ttu-id="ec622-242">範例1後面接著範例2、3、4等等。</span><span class="sxs-lookup"><span data-stu-id="ec622-242">Sample 1 is followed by samples 2, 3, 4, and so on.</span></span>                                                                                                                                                                                                                           |
| <span data-ttu-id="ec622-243">8位身歷聲</span><span class="sxs-lookup"><span data-stu-id="ec622-243">8-bit stereo</span></span>              | <span data-ttu-id="ec622-244">每個範例都是2個位元組。</span><span class="sxs-lookup"><span data-stu-id="ec622-244">Each sample is 2 bytes.</span></span> <span data-ttu-id="ec622-245">範例1後面接著範例2、3、4等等。</span><span class="sxs-lookup"><span data-stu-id="ec622-245">Sample 1 is followed by samples 2, 3, 4, and so on.</span></span> <span data-ttu-id="ec622-246">針對每個範例，第一個位元組是通道 0 (左聲道) ，而第二個位元組是通道1， (右通道) 。</span><span class="sxs-lookup"><span data-stu-id="ec622-246">For each sample, the first byte is channel 0 (the left channel) and the second byte is channel 1 (the right channel).</span></span>                                                                                                                                               |
| <span data-ttu-id="ec622-247">16位 mono</span><span class="sxs-lookup"><span data-stu-id="ec622-247">16-bit mono</span></span>               | <span data-ttu-id="ec622-248">每個範例都是2個位元組。</span><span class="sxs-lookup"><span data-stu-id="ec622-248">Each sample is 2 bytes.</span></span> <span data-ttu-id="ec622-249">範例1後面接著範例2、3、4等等。</span><span class="sxs-lookup"><span data-stu-id="ec622-249">Sample 1 is followed by samples 2, 3, 4, and so on.</span></span> <span data-ttu-id="ec622-250">針對每個範例，第一個位元組是通道0的低序位位元組，而第二個位元組是通道0的高序位位元組。</span><span class="sxs-lookup"><span data-stu-id="ec622-250">For each sample, the first byte is the low-order byte of channel 0 and the second byte is the high-order byte of channel 0.</span></span>                                                                                                                                         |
| <span data-ttu-id="ec622-251">16位身歷聲</span><span class="sxs-lookup"><span data-stu-id="ec622-251">16-bit stereo</span></span>             | <span data-ttu-id="ec622-252">每個範例都是4個位元組。</span><span class="sxs-lookup"><span data-stu-id="ec622-252">Each sample is 4 bytes.</span></span> <span data-ttu-id="ec622-253">範例1後面接著範例2、3、4等等。</span><span class="sxs-lookup"><span data-stu-id="ec622-253">Sample 1 is followed by samples 2, 3, 4, and so on.</span></span> <span data-ttu-id="ec622-254">針對每個範例，第一個位元組是通道 0 (左通道) 的低序位位元組;第二個位元組是通道0的高序位位元組;第三個位元組是通道1的低序位位元組 (右通道) ;第四個位元組是通道1的高序位位元組。</span><span class="sxs-lookup"><span data-stu-id="ec622-254">For each sample, the first byte is the low-order byte of channel 0 (left channel); the second byte is the high-order byte of channel 0; the third byte is the low-order byte of channel 1 (right channel); and the fourth byte is the high-order byte of channel 1.</span></span> |
| <span data-ttu-id="ec622-255">其他</span><span class="sxs-lookup"><span data-stu-id="ec622-255">Others</span></span>                    | <span data-ttu-id="ec622-256">每個範例都包含在多個4個位元組的區塊中，但這些樣本可能是非位元組對齊。</span><span class="sxs-lookup"><span data-stu-id="ec622-256">Each sample is contained in a block that is a multiple of 4 bytes, but the samples may be non-byte-aligned.</span></span> <span data-ttu-id="ec622-257">通道的相片順序是由遮罩指定。</span><span class="sxs-lookup"><span data-stu-id="ec622-257">The arrangement of channels is specified by a mask.</span></span> <span data-ttu-id="ec622-258">如需詳細資訊，請參閱 [**WAVEFORMATEXTENSIBLE**](/windows/win32/api/mmreg/ns-mmreg-waveformatextensible)。</span><span class="sxs-lookup"><span data-stu-id="ec622-258">For more information, see [**WAVEFORMATEXTENSIBLE**](/windows/win32/api/mmreg/ns-mmreg-waveformatextensible).</span></span>                                                                                                 |



 

## <a name="closing-waveform-audio-output-devices"></a><span data-ttu-id="ec622-259">關閉 Waveform-Audio 輸出裝置</span><span class="sxs-lookup"><span data-stu-id="ec622-259">Closing Waveform-Audio Output Devices</span></span>

<span data-ttu-id="ec622-260">波形-音訊播放完成之後，請呼叫 [**waveOutClose**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutclose) 來關閉輸出裝置。</span><span class="sxs-lookup"><span data-stu-id="ec622-260">After waveform-audio playback is complete, call [**waveOutClose**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutclose) to close the output device.</span></span> <span data-ttu-id="ec622-261">如果在播放波形音訊檔案時呼叫 **waveOutClose** ，關閉作業就會失敗，且函式會傳回錯誤碼，指出裝置未關閉。</span><span class="sxs-lookup"><span data-stu-id="ec622-261">If **waveOutClose** is called while a waveform-audio file is playing, the close operation fails and the function returns an error code indicating that the device was not closed.</span></span> <span data-ttu-id="ec622-262">如果您不想要在關閉裝置之前等候播放結束，請在關閉之前呼叫 [**waveOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset) 函式。</span><span class="sxs-lookup"><span data-stu-id="ec622-262">If you do not want to wait for playback to end before closing the device, call the [**waveOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset) function before closing.</span></span> <span data-ttu-id="ec622-263">這會結束播放，並允許關閉裝置。</span><span class="sxs-lookup"><span data-stu-id="ec622-263">This ends playback and allows the device to be closed.</span></span> <span data-ttu-id="ec622-264">在關閉裝置之前，請務必使用 [**waveOutUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutunprepareheader) 函式來清除所有資料區塊的準備工作。</span><span class="sxs-lookup"><span data-stu-id="ec622-264">Be sure to use the [**waveOutUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutunprepareheader) function to clean up the preparation on all data blocks before closing the device.</span></span>

 

 