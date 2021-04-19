---
description: XAudio2 常數，可指定預設參數、最大值和旗標。
ms.assetid: 074ac40e-a17e-7366-1954-6699407b82f7
title: 'XAudio2 界限值和旗標 (Xaudio2 .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe59f229ea406eb5bf6c6b3f5c124d6d0d19c047
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984340"
---
# <a name="xaudio2-boundary-values-and-flags"></a><span data-ttu-id="1888c-103">XAudio2 界限值和旗標</span><span class="sxs-lookup"><span data-stu-id="1888c-103">XAudio2 Boundary Values and Flags</span></span>

<span data-ttu-id="1888c-104">XAudio2 常數，可指定預設參數、最大值和旗標。</span><span class="sxs-lookup"><span data-stu-id="1888c-104">XAudio2 constants that specify default parameters, maximum values, and flags.</span></span>

<span data-ttu-id="1888c-105">**XAudio2 界限值**</span><span class="sxs-lookup"><span data-stu-id="1888c-105">**XAudio2 boundary values**</span></span>



| <span data-ttu-id="1888c-106">常數</span><span class="sxs-lookup"><span data-stu-id="1888c-106">Constant</span></span>                                                                                                                                                                                                     | <span data-ttu-id="1888c-107">描述</span><span class="sxs-lookup"><span data-stu-id="1888c-107">Description</span></span>                                                                                                                                     |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="XAUDIO2_MAX_BUFFER_BYTES"></span><span id="xaudio2_max_buffer_bytes"></span><dl> <span data-ttu-id="1888c-108"><dt>**XAUDIO2 \_ 最大 \_ 緩衝區 \_ 位元組數**</dt></span><span class="sxs-lookup"><span data-stu-id="1888c-108"><dt>**XAUDIO2\_MAX\_BUFFER\_BYTES**</dt></span></span> </dl>             | <span data-ttu-id="1888c-109">[**XAUDIO2 \_ 緩衝區**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer)允許的最大值。AudioBytes.</span><span class="sxs-lookup"><span data-stu-id="1888c-109">Maximum value allowed for [**XAUDIO2\_BUFFER**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer).AudioBytes.</span></span><br/>                                                      |
| <span id="XAUDIO2_MAX_QUEUED_BUFFERS"></span><span id="xaudio2_max_queued_buffers"></span><dl> <span data-ttu-id="1888c-110"><dt>**XAUDIO2 \_ \_ 佇列 \_ 緩衝區上限**</dt></span><span class="sxs-lookup"><span data-stu-id="1888c-110"><dt>**XAUDIO2\_MAX\_QUEUED\_BUFFERS**</dt></span></span> </dl>       | <span data-ttu-id="1888c-111">語音佇列中允許的最大緩衝區。</span><span class="sxs-lookup"><span data-stu-id="1888c-111">Maximum buffers allowed in a voice queue.</span></span><br/>                                                                                            |
| <span id="XAUDIO2_MAX_BUFFERS_SYSTEM"></span><span id="xaudio2_max_buffers_system"></span><dl> <span data-ttu-id="1888c-112"><dt>**XAUDIO2 \_ 最大 \_ 緩衝區 \_ 系統**</dt></span><span class="sxs-lookup"><span data-stu-id="1888c-112"><dt>**XAUDIO2\_MAX\_BUFFERS\_SYSTEM**</dt></span></span> </dl>       | <span data-ttu-id="1888c-113">系統執行緒 (只 Xbox 360) 的緩衝區數目上限。</span><span class="sxs-lookup"><span data-stu-id="1888c-113">Maximum buffers allowed for system threads (Xbox 360 only).</span></span><br/>                                                                          |
| <span id="XAUDIO2_MAX_AUDIO_CHANNELS"></span><span id="xaudio2_max_audio_channels"></span><dl> <span data-ttu-id="1888c-114"><dt>**XAUDIO2 \_ 最大 \_ 音訊 \_ 頻道**</dt></span><span class="sxs-lookup"><span data-stu-id="1888c-114"><dt>**XAUDIO2\_MAX\_AUDIO\_CHANNELS**</dt></span></span> </dl>       | <span data-ttu-id="1888c-115">**WAVEFORMATEX. nChannels** 允許的最大值。</span><span class="sxs-lookup"><span data-stu-id="1888c-115">Maximum value allowed for **WAVEFORMATEX.nChannels**.</span></span><br/>                                                                                |
| <span id="XAUDIO2_MIN_SAMPLE_RATE"></span><span id="xaudio2_min_sample_rate"></span><dl> <span data-ttu-id="1888c-116"><dt>**XAUDIO2 \_ MIN \_ 取樣 \_ 率**</dt></span><span class="sxs-lookup"><span data-stu-id="1888c-116"><dt>**XAUDIO2\_MIN\_SAMPLE\_RATE**</dt></span></span> </dl>                | <span data-ttu-id="1888c-117">支援的最小音訊取樣率。</span><span class="sxs-lookup"><span data-stu-id="1888c-117">Minimum audio sample rate supported.</span></span><br/>                                                                                                 |
| <span id="XAUDIO2_MAX_SAMPLE_RATE"></span><span id="xaudio2_max_sample_rate"></span><dl> <span data-ttu-id="1888c-118"><dt>**XAUDIO2 \_ 最大 \_ 取樣 \_ 率**</dt></span><span class="sxs-lookup"><span data-stu-id="1888c-118"><dt>**XAUDIO2\_MAX\_SAMPLE\_RATE**</dt></span></span> </dl>                | <span data-ttu-id="1888c-119">支援的最大音訊取樣率。</span><span class="sxs-lookup"><span data-stu-id="1888c-119">Maximum audio sample rate supported.</span></span><br/>                                                                                                 |
| <span id="XAUDIO2_MAX_VOLUME_LEVEL"></span><span id="xaudio2_max_volume_level"></span><dl> <span data-ttu-id="1888c-120"><dt>**XAUDIO2 \_ 最大 \_ 磁片區 \_ 層級**</dt></span><span class="sxs-lookup"><span data-stu-id="1888c-120"><dt>**XAUDIO2\_MAX\_VOLUME\_LEVEL**</dt></span></span> </dl>             | <span data-ttu-id="1888c-121">允許的磁片區層級上限。</span><span class="sxs-lookup"><span data-stu-id="1888c-121">Maximum allowed volume level.</span></span><br/>                                                                                                        |
| <span id="XAUDIO2_MIN_FREQ_RATIO"></span><span id="xaudio2_min_freq_ratio"></span><dl> <span data-ttu-id="1888c-122"><dt>**XAUDIO2 \_ 最小 \_ 頻率 \_ 比率**</dt></span><span class="sxs-lookup"><span data-stu-id="1888c-122"><dt>**XAUDIO2\_MIN\_FREQ\_RATIO**</dt></span></span> </dl>                   | <span data-ttu-id="1888c-123">來源語音中允許的最小頻率比率。</span><span class="sxs-lookup"><span data-stu-id="1888c-123">Minimum frequency ratio allowed in a source voice.</span></span><br/>                                                                                   |
| <span id="XAUDIO2_MAX_FREQ_RATIO"></span><span id="xaudio2_max_freq_ratio"></span><dl> <span data-ttu-id="1888c-124"><dt>**XAUDIO2 \_ 最大 \_ 頻率 \_ 比率**</dt></span><span class="sxs-lookup"><span data-stu-id="1888c-124"><dt>**XAUDIO2\_MAX\_FREQ\_RATIO**</dt></span></span> </dl>                   | <span data-ttu-id="1888c-125">來源語音中允許的最大頻率比率。</span><span class="sxs-lookup"><span data-stu-id="1888c-125">Maximum frequency ratio allowed in a source voice.</span></span><br/>                                                                                   |
| <span id="XAUDIO2_DEFAULT_FREQ_RATIO"></span><span id="xaudio2_default_freq_ratio"></span><dl> <span data-ttu-id="1888c-126"><dt>**XAUDIO2 \_ 預設 \_ 頻率 \_ 比率**</dt></span><span class="sxs-lookup"><span data-stu-id="1888c-126"><dt>**XAUDIO2\_DEFAULT\_FREQ\_RATIO**</dt></span></span> </dl>       | <span data-ttu-id="1888c-127">[**IXAudio2：： CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice)的 **MaxFrequencyRatio** 引數的預設值。</span><span class="sxs-lookup"><span data-stu-id="1888c-127">Default value for the **MaxFrequencyRatio** argument of [**IXAudio2::CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice).</span></span><br/> |
| <span id="XAUDIO2_MAX_FILTER_ONEOVERQ"></span><span id="xaudio2_max_filter_oneoverq"></span><dl> <span data-ttu-id="1888c-128"><dt>**XAUDIO2 \_ MAX \_ FILTER \_ ONEOVERQ**</dt></span><span class="sxs-lookup"><span data-stu-id="1888c-128"><dt>**XAUDIO2\_MAX\_FILTER\_ONEOVERQ**</dt></span></span> </dl>    | <span data-ttu-id="1888c-129">[**XAUDIO2 \_ 篩選 \_ 參數**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_filter_parameters)的最大值。**OneOverQ**。</span><span class="sxs-lookup"><span data-stu-id="1888c-129">Maximum value for [**XAUDIO2\_FILTER\_PARAMETERS**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_filter_parameters).**OneOverQ**.</span></span><br/>                                     |
| <span id="XAUDIO2_MAX_FILTER_FREQUENCY"></span><span id="xaudio2_max_filter_frequency"></span><dl> <span data-ttu-id="1888c-130"><dt>**XAUDIO2 \_ 最大 \_ 篩選 \_ 頻率**</dt></span><span class="sxs-lookup"><span data-stu-id="1888c-130"><dt>**XAUDIO2\_MAX\_FILTER\_FREQUENCY**</dt></span></span> </dl> | <span data-ttu-id="1888c-131">[**XAUDIO2 \_ 篩選 \_ 參數**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_filter_parameters)的最大值。**頻率**。</span><span class="sxs-lookup"><span data-stu-id="1888c-131">Maximum value for [**XAUDIO2\_FILTER\_PARAMETERS**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_filter_parameters).**Frequency**.</span></span><br/>                                    |
| <span id="XAUDIO2_MAX_LOOP_COUNT"></span><span id="xaudio2_max_loop_count"></span><dl> <span data-ttu-id="1888c-132"><dt>**XAUDIO2 \_ 最大 \_ 迴圈 \_ 計數**</dt></span><span class="sxs-lookup"><span data-stu-id="1888c-132"><dt>**XAUDIO2\_MAX\_LOOP\_COUNT**</dt></span></span> </dl>                   | <span data-ttu-id="1888c-133">不會被視為 [**XAUDIO2 \_ 緩衝區**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer)無限迴圈的最大值。**LoopCount**。</span><span class="sxs-lookup"><span data-stu-id="1888c-133">Maximum value that will not be treated as infinite looping for [**XAUDIO2\_BUFFER**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer).**LoopCount**.</span></span><br/>              |
| <span id="XAUDIO2_MAX_INSTANCES"></span><span id="xaudio2_max_instances"></span><dl> <span data-ttu-id="1888c-134"><dt>**XAUDIO2 \_ 實例數目上限 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1888c-134"><dt>**XAUDIO2\_MAX\_INSTANCES**</dt></span></span> </dl>                       | <span data-ttu-id="1888c-135">Xbox 360 上允許的 XAudio2 並行實例數上限。</span><span class="sxs-lookup"><span data-stu-id="1888c-135">Maximum simultaneous instances of XAudio2 allowed on Xbox 360.</span></span><br/>                                                                       |



<span data-ttu-id="1888c-136">**XAudio2 具有特殊意義的值**</span><span class="sxs-lookup"><span data-stu-id="1888c-136">**XAudio2 values with special meaning**</span></span>



| <span data-ttu-id="1888c-137">常數</span><span class="sxs-lookup"><span data-stu-id="1888c-137">Constant</span></span>                                                                                                                                                                                              | <span data-ttu-id="1888c-138">描述</span><span class="sxs-lookup"><span data-stu-id="1888c-138">Description</span></span>                                                                                                                                                              |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="XAUDIO2_COMMIT_NOW"></span><span id="xaudio2_commit_now"></span><dl> <span data-ttu-id="1888c-139"><dt>**\_立即 XAUDIO2 認可 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1888c-139"><dt>**XAUDIO2\_COMMIT\_NOW**</dt></span></span> </dl>                         | <span data-ttu-id="1888c-140">當做具有 OperationSet 引數之方法的參數使用。</span><span class="sxs-lookup"><span data-stu-id="1888c-140">Used as a parameter to methods with an OperationSet argument.</span></span> <span data-ttu-id="1888c-141">如需詳細資訊，請參閱 [XAudio2 操作集合](xaudio2-operation-sets.md) 。</span><span class="sxs-lookup"><span data-stu-id="1888c-141">See [XAudio2 Operation Sets](xaudio2-operation-sets.md) for more information.</span></span><br/>                  |
| <span id="XAUDIO2_COMMIT_ALL"></span><span id="xaudio2_commit_all"></span><dl> <span data-ttu-id="1888c-142"><dt>**XAUDIO2 \_ 認可 \_ 全部**</dt></span><span class="sxs-lookup"><span data-stu-id="1888c-142"><dt>**XAUDIO2\_COMMIT\_ALL**</dt></span></span> </dl>                         | <span data-ttu-id="1888c-143">當做 [**IXAudio2：： CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges)中的參數使用。</span><span class="sxs-lookup"><span data-stu-id="1888c-143">Used as a parameter in [**IXAudio2::CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges).</span></span><br/>                                                                   |
| <span id="XAUDIO2_INVALID_OPSET"></span><span id="xaudio2_invalid_opset"></span><dl> <span data-ttu-id="1888c-144"><dt>**XAUDIO2 \_ 不正確 \_ OPSET**</dt></span><span class="sxs-lookup"><span data-stu-id="1888c-144"><dt>**XAUDIO2\_INVALID\_OPSET**</dt></span></span> </dl>                | <span data-ttu-id="1888c-145">指定不正確 OperationSet 引數值。</span><span class="sxs-lookup"><span data-stu-id="1888c-145">Specifies an invalid value for OperationSet arguments.</span></span> <span data-ttu-id="1888c-146">如需詳細資訊，請參閱 [XAudio2 操作集合](xaudio2-operation-sets.md) 。</span><span class="sxs-lookup"><span data-stu-id="1888c-146">See [XAudio2 Operation Sets](xaudio2-operation-sets.md) for more information.</span></span><br/>                         |
| <span id="XAUDIO2_NO_LOOP_REGION"></span><span id="xaudio2_no_loop_region"></span><dl> <span data-ttu-id="1888c-147"><dt>**XAUDIO2 \_ 無 \_ 迴圈 \_ 區域**</dt></span><span class="sxs-lookup"><span data-stu-id="1888c-147"><dt>**XAUDIO2\_NO\_LOOP\_REGION**</dt></span></span> </dl>            | <span data-ttu-id="1888c-148">指定 [**XAUDIO2 \_ 緩衝區**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer)中未使用的迴圈區域。**LoopCount**。</span><span class="sxs-lookup"><span data-stu-id="1888c-148">Specifies no loop region, used in [**XAUDIO2\_BUFFER**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer).**LoopCount**.</span></span><br/>                                                                    |
| <span id="XAUDIO2_LOOP_INFINITE"></span><span id="xaudio2_loop_infinite"></span><dl> <span data-ttu-id="1888c-149"><dt>**XAUDIO2 \_ 迴圈 \_ 無限**</dt></span><span class="sxs-lookup"><span data-stu-id="1888c-149"><dt>**XAUDIO2\_LOOP\_INFINITE**</dt></span></span> </dl>                | <span data-ttu-id="1888c-150">指定 [**XAUDIO2 \_ 緩衝區**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer)中使用的無限迴圈。**LoopCount**。</span><span class="sxs-lookup"><span data-stu-id="1888c-150">Specifies infinite looping, used in [**XAUDIO2\_BUFFER**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer).**LoopCount**.</span></span><br/>                                                                  |
| <span id="XAUDIO2_DEFAULT_CHANNELS"></span><span id="xaudio2_default_channels"></span><dl> <span data-ttu-id="1888c-151"><dt>**XAUDIO2 \_ 預設 \_ 通道**</dt></span><span class="sxs-lookup"><span data-stu-id="1888c-151"><dt>**XAUDIO2\_DEFAULT\_CHANNELS**</dt></span></span> </dl>       | <span data-ttu-id="1888c-152">指定目前平臺的預設通道數目（用於 [**IXAudio2：： CreateMasteringVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice)）。</span><span class="sxs-lookup"><span data-stu-id="1888c-152">Specifies the default number of channels for the current platform, used in [**IXAudio2::CreateMasteringVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice).</span></span><br/> |
| <span id="XAUDIO2_DEFAULT_SAMPLERATE"></span><span id="xaudio2_default_samplerate"></span><dl> <span data-ttu-id="1888c-153"><dt>**XAUDIO2 \_ 預設 \_ SAMPLERATE**</dt></span><span class="sxs-lookup"><span data-stu-id="1888c-153"><dt>**XAUDIO2\_DEFAULT\_SAMPLERATE**</dt></span></span> </dl> | <span data-ttu-id="1888c-154">指定目前平臺的預設取樣率，用於 [**IXAudio2：： CreateMasteringVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice)。</span><span class="sxs-lookup"><span data-stu-id="1888c-154">Specifies the default sample rate for the current platform, used in [**IXAudio2::CreateMasteringVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice).</span></span><br/>        |



<span data-ttu-id="1888c-155">**XAudio2 旗標**</span><span class="sxs-lookup"><span data-stu-id="1888c-155">**XAudio2 Flags**</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="1888c-156">常數</span><span class="sxs-lookup"><span data-stu-id="1888c-156">Constant</span></span></th>
<th style="text-align: left;"><span data-ttu-id="1888c-157">描述</span><span class="sxs-lookup"><span data-stu-id="1888c-157">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="XAUDIO2_DEBUG_ENGINE"></span><span id="xaudio2_debug_engine"></span><dl> <span data-ttu-id="1888c-158"><dt><strong>XAUDIO2_DEBUG_ENGINE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="1888c-158"><dt><strong>XAUDIO2_DEBUG_ENGINE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1888c-159">指定應使用音訊引擎的 debug/checked 版本，而不是發行版本。</span><span class="sxs-lookup"><span data-stu-id="1888c-159">Specifies that the debug/checked version of the audio engine should be used instead of the release version.</span></span> <span data-ttu-id="1888c-160">請參閱 <a href="/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create"><strong>XAudio2Create</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="1888c-160">See <a href="/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create"><strong>XAudio2Create</strong></a>.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="1888c-161">Windows 8 或 Windows 10 不支援此旗標。</span><span class="sxs-lookup"><span data-stu-id="1888c-161">This flag is not supported on Windows 8 or Windows 10.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="XAUDIO2_VOICE_NOPITCH"></span><span id="xaudio2_voice_nopitch"></span><dl> <span data-ttu-id="1888c-162"><dt><strong>XAUDIO2_VOICE_NOPITCH</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="1888c-162"><dt><strong>XAUDIO2_VOICE_NOPITCH</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1888c-163">指定來源語音不會使用移動音調，請參閱 <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice"><strong>IXAudio2：： CreateSourceVoice</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="1888c-163">Specifies that a source voice will not use pitch shifting, see <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice"><strong>IXAudio2::CreateSourceVoice</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="XAUDIO2_VOICE_NOSRC"></span><span id="xaudio2_voice_nosrc"></span><dl> <span data-ttu-id="1888c-164"><dt><strong>XAUDIO2_VOICE_NOSRC</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="1888c-164"><dt><strong>XAUDIO2_VOICE_NOSRC</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1888c-165">指定來源語音上沒有可用的取樣率轉換，語音的輸出必須具有相同的取樣率。</span><span class="sxs-lookup"><span data-stu-id="1888c-165">Specifies that no sample rate conversion is available on a source voice, the voice's outputs must have the same sample rate.</span></span> <span data-ttu-id="1888c-166">請參閱 <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice"><strong>IXAudio2：： CreateSourceVoice</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="1888c-166">See <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice"><strong>IXAudio2::CreateSourceVoice</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="XAUDIO2_VOICE_USEFILTER"></span><span id="xaudio2_voice_usefilter"></span><dl> <span data-ttu-id="1888c-167"><dt><strong>XAUDIO2_VOICE_USEFILTER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="1888c-167"><dt><strong>XAUDIO2_VOICE_USEFILTER</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1888c-168">指定要在語音上使用篩選效果。</span><span class="sxs-lookup"><span data-stu-id="1888c-168">Specifies that the filter effect should be available on a voice.</span></span> <span data-ttu-id="1888c-169">請參閱 <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice"><strong>IXAudio2：： CreateSourceVoice</strong></a> 和 <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2-createsubmixvoice"><strong>IXAudio2：： CreateSubmixVoice</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="1888c-169">See <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice"><strong>IXAudio2::CreateSourceVoice</strong></a> and <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2-createsubmixvoice"><strong>IXAudio2::CreateSubmixVoice</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="XAUDIO2_PLAY_TAILS"></span><span id="xaudio2_play_tails"></span><dl> <span data-ttu-id="1888c-170"><dt><strong>XAUDIO2_PLAY_TAILS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="1888c-170"><dt><strong>XAUDIO2_PLAY_TAILS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1888c-171">指定語音在停止之後，應繼續發出效果輸出。</span><span class="sxs-lookup"><span data-stu-id="1888c-171">Specifies that a voice should continue emitting effect output after it is stopped.</span></span> <span data-ttu-id="1888c-172">請參閱 <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-stop"><strong>IXAudio2SourceVoice：： Stop</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="1888c-172">See <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-stop"><strong>IXAudio2SourceVoice::Stop</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="XAUDIO2_END_OF_STREAM"></span><span id="xaudio2_end_of_stream"></span><dl> <span data-ttu-id="1888c-173"><dt><strong>XAUDIO2_END_OF_STREAM</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="1888c-173"><dt><strong>XAUDIO2_END_OF_STREAM</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1888c-174">表示資料流程中的最後一個緩衝區。</span><span class="sxs-lookup"><span data-stu-id="1888c-174">Indicates the last buffer in a stream.</span></span> <span data-ttu-id="1888c-175">請參閱 <a href="/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer"><strong>XAUDIO2_BUFFER</strong></a>。<strong>旗標</strong>。</span><span class="sxs-lookup"><span data-stu-id="1888c-175">See <a href="/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer"><strong>XAUDIO2_BUFFER</strong></a>.<strong>Flags</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="XAUDIO2_STOP_ENGINE_WHEN_IDLE"></span><span id="xaudio2_stop_engine_when_idle"></span><dl> <span data-ttu-id="1888c-176"><dt><strong>XAUDIO2_STOP_ENGINE_WHEN_IDLE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="1888c-176"><dt><strong>XAUDIO2_STOP_ENGINE_WHEN_IDLE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1888c-177">指定當語音啟動時，音訊引擎應該停止，並在啟動時啟動。</span><span class="sxs-lookup"><span data-stu-id="1888c-177">Specifies that the audio engine should stop when no source voices are started and start when a voice is started.</span></span> <span data-ttu-id="1888c-178">請參閱 <a href="/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create"><strong>XAudio2Create</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="1888c-178">See <a href="/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create"><strong>XAudio2Create</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="XAUDIO2_SEND_USEFILTER"></span><span id="xaudio2_send_usefilter"></span><dl> <span data-ttu-id="1888c-179"><dt><strong>XAUDIO2_SEND_USEFILTER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="1888c-179"><dt><strong>XAUDIO2_SEND_USEFILTER</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1888c-180">表示篩選準則應該用於語音傳送。</span><span class="sxs-lookup"><span data-stu-id="1888c-180">Indicates a filter should be used on a voice send.</span></span> <span data-ttu-id="1888c-181">請參閱 <a href="/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_send_descriptor"><strong>XAUDIO2_SEND_DESCRIPTOR</strong></a>。<strong>旗標</strong>。</span><span class="sxs-lookup"><span data-stu-id="1888c-181">See <a href="/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_send_descriptor"><strong>XAUDIO2_SEND_DESCRIPTOR</strong></a>.<strong>Flags</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="XAUDIO2_1024_QUANTUM"></span><span id="xaudio2_1024_quantum"></span><dl> <span data-ttu-id="1888c-182"><dt><strong>XAUDIO2_1024_QUANTUM</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="1888c-182"><dt><strong>XAUDIO2_1024_QUANTUM</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1888c-183">在 48KHz) 指定非預設的處理量子 21.33 ms (1024 範例。</span><span class="sxs-lookup"><span data-stu-id="1888c-183">Specifies a non-default processing quantum of 21.33 ms (1024 samples at 48KHz).</span></span> <span data-ttu-id="1888c-184">請參閱 <a href="/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create"><strong>XAudio2Create</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="1888c-184">See <a href="/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create"><strong>XAudio2Create</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="XAUDIO2_NO_VIRTUAL_AUDIO_CLIENT"></span><span id="xaudio2_no_virtual_audio_client"></span><dl> <span data-ttu-id="1888c-185"><dt><strong>XAUDIO2_NO_VIRTUAL_AUDIO_CLIENT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="1888c-185"><dt><strong>XAUDIO2_NO_VIRTUAL_AUDIO_CLIENT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1888c-186">指定不應使用虛擬音訊用戶端。</span><span class="sxs-lookup"><span data-stu-id="1888c-186">Specifies that a virtual audio client should not be used.</span></span> <span data-ttu-id="1888c-187">請參閱 <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice"><strong>IXAudio2：： CreateMasteringVoice</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="1888c-187">See <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice"><strong>IXAudio2::CreateMasteringVoice</strong></a>.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="1888c-188">在行動裝置家族中的裝置上，一律會使用虛擬音訊用戶端，不論是否使用此旗標。</span><span class="sxs-lookup"><span data-stu-id="1888c-188">On devices in the Mobile device family, a virtual audio client is always used, regardless of whether this flag is used.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



<span data-ttu-id="1888c-189">**XAudio2 內建聲音篩選器的預設參數**</span><span class="sxs-lookup"><span data-stu-id="1888c-189">**XAudio2 Default Parameters for the Built-in Voice Filter**</span></span>



| <span data-ttu-id="1888c-190">常數</span><span class="sxs-lookup"><span data-stu-id="1888c-190">Constant</span></span>                                                                                                                                                                                                                 | <span data-ttu-id="1888c-191">描述</span><span class="sxs-lookup"><span data-stu-id="1888c-191">Description</span></span>                                                                                   |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------|
| <span id="XAUDIO2_DEFAULT_FILTER_TYPE"></span><span id="xaudio2_default_filter_type"></span><dl> <span data-ttu-id="1888c-192"><dt>**XAUDIO2 \_ 預設 \_ 篩選 \_ 類型**</dt></span><span class="sxs-lookup"><span data-stu-id="1888c-192"><dt>**XAUDIO2\_DEFAULT\_FILTER\_TYPE**</dt></span></span> </dl>                | <span data-ttu-id="1888c-193">指定要搭配語音和語音傳送使用的預設篩選類型。</span><span class="sxs-lookup"><span data-stu-id="1888c-193">Specifies the default filter type to be used with voices and voice sends.</span></span><br/>          |
| <span id="XAUDIO2_DEFAULT_FILTER_FREQUENCY"></span><span id="xaudio2_default_filter_frequency"></span><dl> <span data-ttu-id="1888c-194"><dt>**XAUDIO2 \_ 預設 \_ 篩選 \_ 頻率**</dt></span><span class="sxs-lookup"><span data-stu-id="1888c-194"><dt>**XAUDIO2\_DEFAULT\_FILTER\_FREQUENCY**</dt></span></span> </dl> | <span data-ttu-id="1888c-195">指定要搭配語音和語音傳送使用的預設篩選頻率。</span><span class="sxs-lookup"><span data-stu-id="1888c-195">Specifies the default filter frequency to be used with voices and voice sends.</span></span><br/>     |
| <span id="XAUDIO2_DEFAULT_FILTER_ONEOVERQ"></span><span id="xaudio2_default_filter_oneoverq"></span><dl> <span data-ttu-id="1888c-196"><dt>**XAUDIO2 \_ 預設 \_ 篩選 \_ ONEOVERQ**</dt></span><span class="sxs-lookup"><span data-stu-id="1888c-196"><dt>**XAUDIO2\_DEFAULT\_FILTER\_ONEOVERQ**</dt></span></span> </dl>    | <span data-ttu-id="1888c-197">指定要搭配語音和語音傳送使用之衰減的預設篩選速率。</span><span class="sxs-lookup"><span data-stu-id="1888c-197">Specifies the default filter rate of decay to be used with voices and voice sends.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="1888c-198">備註</span><span class="sxs-lookup"><span data-stu-id="1888c-198">Remarks</span></span>

### <a name="platform-requirements"></a><span data-ttu-id="1888c-199">平台需求</span><span class="sxs-lookup"><span data-stu-id="1888c-199">Platform Requirements</span></span>

<span data-ttu-id="1888c-200">Windows 10 (XAudio 2.9) ;Windows 8、Windows Phone 8 (XAudio 2.8) ;DirectX SDK (XAudio 2.7) </span><span class="sxs-lookup"><span data-stu-id="1888c-200">Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)</span></span>

## <a name="requirements"></a><span data-ttu-id="1888c-201">規格需求</span><span class="sxs-lookup"><span data-stu-id="1888c-201">Requirements</span></span>



| <span data-ttu-id="1888c-202">需求</span><span class="sxs-lookup"><span data-stu-id="1888c-202">Requirement</span></span> | <span data-ttu-id="1888c-203">值</span><span class="sxs-lookup"><span data-stu-id="1888c-203">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="1888c-204">標頭</span><span class="sxs-lookup"><span data-stu-id="1888c-204">Header</span></span><br/> | <dl> <span data-ttu-id="1888c-205"><dt>Xaudio2。h</dt></span><span class="sxs-lookup"><span data-stu-id="1888c-205"><dt>Xaudio2.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1888c-206">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1888c-206">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1888c-207">XAudio2：：常數</span><span class="sxs-lookup"><span data-stu-id="1888c-207">XAudio2::Constants</span></span>](constants.md)
</dt> </dl>

 

 
