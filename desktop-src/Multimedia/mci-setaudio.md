---
title: 'MCI_SETAUDIO 命令 (Mmsystem .h) '
description: MCI \_ SETAUDIO 命令會設定與音訊播放和捕捉相關聯的值。 數位影片和 VCR 裝置會辨識此命令。
ms.assetid: 78624596-e465-4ef1-8988-edcfe9a46f89
keywords:
- MCI_SETAUDIO 命令 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_SETAUDIO
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20605ff78c62a8e688778692d5ca8f8e1342a968
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104187305"
---
# <a name="mci_setaudio-command"></a><span data-ttu-id="8700a-105">MCI \_ SETAUDIO 命令</span><span class="sxs-lookup"><span data-stu-id="8700a-105">MCI\_SETAUDIO command</span></span>

<span data-ttu-id="8700a-106">MCI \_ SETAUDIO 命令會設定與音訊播放和捕捉相關聯的值。</span><span class="sxs-lookup"><span data-stu-id="8700a-106">The MCI\_SETAUDIO command sets values associated with audio playback and capture.</span></span> <span data-ttu-id="8700a-107">數位影片和 VCR 裝置會辨識此命令。</span><span class="sxs-lookup"><span data-stu-id="8700a-107">Digital-video and VCR devices recognize this command.</span></span>

<span data-ttu-id="8700a-108">若要傳送此命令，請使用下列參數呼叫 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) 函數。</span><span class="sxs-lookup"><span data-stu-id="8700a-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SETAUDIO, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpSetAudio
);
```



## <a name="parameters"></a><span data-ttu-id="8700a-109">參數</span><span class="sxs-lookup"><span data-stu-id="8700a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8700a-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="8700a-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="8700a-111">要接收命令訊息之 MCI 裝置的裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="8700a-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="8700a-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="8700a-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="8700a-113">MCI \_ 通知、mci \_ 等候或 mci \_ 測試。</span><span class="sxs-lookup"><span data-stu-id="8700a-113">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="8700a-114">如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。</span><span class="sxs-lookup"><span data-stu-id="8700a-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="8700a-115"><span id="lpSetAudio"></span><span id="lpsetaudio"></span><span id="LPSETAUDIO"></span>*lpSetAudio*</span><span class="sxs-lookup"><span data-stu-id="8700a-115"><span id="lpSetAudio"></span><span id="lpsetaudio"></span><span id="LPSETAUDIO"></span>*lpSetAudio*</span></span>
</dt> <dd>

<span data-ttu-id="8700a-116">[**MCI \_ 泛型 \_ PARMS**](mci-generic-parms.md)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="8700a-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="8700a-117">具有擴充命令集的 (裝置，可能會以裝置特定結構取代此結構。 ) </span><span class="sxs-lookup"><span data-stu-id="8700a-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8700a-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="8700a-118">Return Value</span></span>

<span data-ttu-id="8700a-119">如果成功則傳回零，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="8700a-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="8700a-120">備註</span><span class="sxs-lookup"><span data-stu-id="8700a-120">Remarks</span></span>

<span data-ttu-id="8700a-121">下列旗標適用于 **digitalvideo** 裝置類型：</span><span class="sxs-lookup"><span data-stu-id="8700a-121">The following flags apply to the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="8700a-122"><span id="MCI_DGV_SETAUDIO_ALG"></span><span id="mci_dgv_setaudio_alg"></span>MCI \_ DGV \_ SETAUDIO \_ ALG</span><span class="sxs-lookup"><span data-stu-id="8700a-122"><span id="MCI_DGV_SETAUDIO_ALG"></span><span id="mci_dgv_setaudio_alg"></span>MCI\_DGV\_SETAUDIO\_ALG</span></span>
</dt> <dd>

<span data-ttu-id="8700a-123">*LpSetAudio* 所識別之結構的 **lpstrAlgorithm** 成員包含包含音訊壓縮演算法名稱的緩衝區位址。</span><span class="sxs-lookup"><span data-stu-id="8700a-123">The **lpstrAlgorithm** member of the structure identified by *lpSetAudio* contains an address of a buffer containing the name of an audio compression algorithm.</span></span> <span data-ttu-id="8700a-124">壓縮演算法會由後續的 [mci \_ 保留](mci-reserve.md) 或 [MCI \_ 記錄](mci-record.md) 命令使用。</span><span class="sxs-lookup"><span data-stu-id="8700a-124">The compression algorithm is used by subsequent [MCI\_RESERVE](mci-reserve.md) or [MCI\_RECORD](mci-record.md) commands.</span></span> <span data-ttu-id="8700a-125">可用的演算法取決於裝置。</span><span class="sxs-lookup"><span data-stu-id="8700a-125">The available algorithms are device dependent.</span></span> <span data-ttu-id="8700a-126">如果演算法與目前的檔案格式不相容，則檔案格式會變更為演算法的預設格式。</span><span class="sxs-lookup"><span data-stu-id="8700a-126">If the algorithm is incompatible with the current file format, the file format is changed to the default format for the algorithm.</span></span>

</dd> <dt>

<span data-ttu-id="8700a-127"><span id="MCI_DGV_SETAUDIO_CLOCKTIME"></span><span id="mci_dgv_setaudio_clocktime"></span>MCI \_ DGV \_ SETAUDIO \_ CLOCKTIME</span><span class="sxs-lookup"><span data-stu-id="8700a-127"><span id="MCI_DGV_SETAUDIO_CLOCKTIME"></span><span id="mci_dgv_setaudio_clocktime"></span>MCI\_DGV\_SETAUDIO\_CLOCKTIME</span></span>
</dt> <dd>

<span data-ttu-id="8700a-128">指定的時間是以毫秒為單位，而在與 MCI DGV SETAUDIO 搭配使用時是絕對時間 \_ \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="8700a-128">The time specified is in milliseconds and is absolute time when used with MCI\_DGV\_SETAUDIO\_OVER.</span></span> <span data-ttu-id="8700a-129"> (這次無法在工作區的播放中執行。 ) </span><span class="sxs-lookup"><span data-stu-id="8700a-129">(This time is not in step with the playing of the workspace.)</span></span>

</dd> <dt>

<span data-ttu-id="8700a-130"><span id="MCI_DGV_SETAUDIO_INPUT"></span><span id="mci_dgv_setaudio_input"></span>MCI \_ DGV \_ SETAUDIO \_ 輸入</span><span class="sxs-lookup"><span data-stu-id="8700a-130"><span id="MCI_DGV_SETAUDIO_INPUT"></span><span id="mci_dgv_setaudio_input"></span>MCI\_DGV\_SETAUDIO\_INPUT</span></span>
</dt> <dd>

<span data-ttu-id="8700a-131">修改低音、高音或音量旗標，使其影響輸入信號，並修改所記錄的內容。</span><span class="sxs-lookup"><span data-stu-id="8700a-131">Modifies the bass, treble, or volume flag so that it affects the input signal and modifies what is recorded.</span></span> <span data-ttu-id="8700a-132">可能的話，這是監視輸入時的預設值。</span><span class="sxs-lookup"><span data-stu-id="8700a-132">If possible, this is the default when monitoring the input.</span></span>

</dd> <dt>

<span data-ttu-id="8700a-133"><span id="MCI_DGV_SETAUDIO_ITEM"></span><span id="mci_dgv_setaudio_item"></span>MCI \_ DGV \_ SETAUDIO \_ 專案</span><span class="sxs-lookup"><span data-stu-id="8700a-133"><span id="MCI_DGV_SETAUDIO_ITEM"></span><span id="mci_dgv_setaudio_item"></span>MCI\_DGV\_SETAUDIO\_ITEM</span></span>
</dt> <dd>

<span data-ttu-id="8700a-134">音訊常數指定于 *lpSetAudio* 所識別之結構的 **dwItem** 成員中。</span><span class="sxs-lookup"><span data-stu-id="8700a-134">An audio constant is specified in the **dwItem** member of the structure identified by *lpSetAudio*.</span></span> <span data-ttu-id="8700a-135">常數可識別正在設定的值。</span><span class="sxs-lookup"><span data-stu-id="8700a-135">The constant identifies the value that is being set.</span></span> <span data-ttu-id="8700a-136">以下是定義的常數：</span><span class="sxs-lookup"><span data-stu-id="8700a-136">The following constants are defined:</span></span>

</dd> <dt>

<span data-ttu-id="8700a-137"><span id="MCI_DGV_SETAUDIO_AVGBYTESPERSEC"></span><span id="mci_dgv_setaudio_avgbytespersec"></span>MCI \_ DGV \_ SETAUDIO \_ AVGBYTESPERSEC</span><span class="sxs-lookup"><span data-stu-id="8700a-137"><span id="MCI_DGV_SETAUDIO_AVGBYTESPERSEC"></span><span id="mci_dgv_setaudio_avgbytespersec"></span>MCI\_DGV\_SETAUDIO\_AVGBYTESPERSEC</span></span>
</dt> <dd>

<span data-ttu-id="8700a-138">平均位元組數是在 *lpSetAudio* 所識別之結構的 **dwValue** 成員中指定。</span><span class="sxs-lookup"><span data-stu-id="8700a-138">The average number of bytes is specified in the **dwValue** member of the structure identified by *lpSetAudio*.</span></span> <span data-ttu-id="8700a-139">此值會設定在 PCM (脈衝程式碼調製) 中播放或錄製的平均每秒位元組數，並 ADPCM (調適型差異脈衝程式碼調製) 格式。</span><span class="sxs-lookup"><span data-stu-id="8700a-139">This value sets the average number of bytes per second for playing or recording in the PCM (Pulse Code Modulation) and ADPCM (Adaptive Differential Pulse Code Modulation) formats.</span></span> <span data-ttu-id="8700a-140">檔案會以這種格式儲存。</span><span class="sxs-lookup"><span data-stu-id="8700a-140">The file is saved in this format.</span></span>

</dd> <dt>

<span data-ttu-id="8700a-141"><span id="MCI_DGV_SETAUDIO_BASS"></span><span id="mci_dgv_setaudio_bass"></span>MCI \_ DGV \_ SETAUDIO \_ 低音</span><span class="sxs-lookup"><span data-stu-id="8700a-141"><span id="MCI_DGV_SETAUDIO_BASS"></span><span id="mci_dgv_setaudio_bass"></span>MCI\_DGV\_SETAUDIO\_BASS</span></span>
</dt> <dd>

<span data-ttu-id="8700a-142">音訊低頻率層級會指定為 *lpSetAudio* 所識別之結構的 **dwValue** 成員中的因素。</span><span class="sxs-lookup"><span data-stu-id="8700a-142">The audio low frequency level is specified as a factor in the **dwValue** member of the structure identified by *lpSetAudio*.</span></span>

</dd> <dt>

<span data-ttu-id="8700a-143"><span id="MCI_DGV_SETAUDIO_BITSPERSAMPLE"></span><span id="mci_dgv_setaudio_bitspersample"></span>MCI \_ DGV \_ SETAUDIO \_ BITSPERSAMPLE</span><span class="sxs-lookup"><span data-stu-id="8700a-143"><span id="MCI_DGV_SETAUDIO_BITSPERSAMPLE"></span><span id="mci_dgv_setaudio_bitspersample"></span>MCI\_DGV\_SETAUDIO\_BITSPERSAMPLE</span></span>
</dt> <dd>

<span data-ttu-id="8700a-144">依 *lpSetAudio* 所識別之結構的 **dwValue** 成員，指定每個樣本的位數。</span><span class="sxs-lookup"><span data-stu-id="8700a-144">The number of bits per sample is specified in the **dwValue** member of the structure identified by *lpSetAudio*.</span></span> <span data-ttu-id="8700a-145">此值會設定以 PCM 格式播放或錄製的每個樣本位數。</span><span class="sxs-lookup"><span data-stu-id="8700a-145">This value sets the number of bits per sample played or recorded in the PCM format.</span></span> <span data-ttu-id="8700a-146">檔案會以這種格式儲存。</span><span class="sxs-lookup"><span data-stu-id="8700a-146">The file is saved in this format.</span></span>

</dd> <dt>

<span data-ttu-id="8700a-147"><span id="MCI_DGV_SETAUDIO_BLOCKALIGN"></span><span id="mci_dgv_setaudio_blockalign"></span>MCI \_ DGV \_ SETAUDIO \_ BLOCKALIGN</span><span class="sxs-lookup"><span data-stu-id="8700a-147"><span id="MCI_DGV_SETAUDIO_BLOCKALIGN"></span><span id="mci_dgv_setaudio_blockalign"></span>MCI\_DGV\_SETAUDIO\_BLOCKALIGN</span></span>
</dt> <dd>

<span data-ttu-id="8700a-148">資料區塊對齊是在 *lpSetAudio* 所識別之結構的 **dwValue** 成員中指定。</span><span class="sxs-lookup"><span data-stu-id="8700a-148">The data block alignment is specified in the **dwValue** member of the structure identified by *lpSetAudio*.</span></span> <span data-ttu-id="8700a-149">此值會設定資料區塊相對於輸入波形資料開頭的對齊方式。</span><span class="sxs-lookup"><span data-stu-id="8700a-149">This value sets the alignment of data blocks relative to the start of input waveform data.</span></span>

</dd> <dt>

<span data-ttu-id="8700a-150"><span id="MCI_DGV_SETAUDIO_SAMPLESPERSEC"></span><span id="mci_dgv_setaudio_samplespersec"></span>MCI \_ DGV \_ SETAUDIO \_ SAMPLESPERSEC</span><span class="sxs-lookup"><span data-stu-id="8700a-150"><span id="MCI_DGV_SETAUDIO_SAMPLESPERSEC"></span><span id="mci_dgv_setaudio_samplespersec"></span>MCI\_DGV\_SETAUDIO\_SAMPLESPERSEC</span></span>
</dt> <dd>

<span data-ttu-id="8700a-151">取樣率是在 *lpSetAudio* 所識別之結構的 **dwValue** 成員中指定。</span><span class="sxs-lookup"><span data-stu-id="8700a-151">The sample rate is specified in the **dwValue** member of the structure identified by *lpSetAudio*.</span></span> <span data-ttu-id="8700a-152">此值會設定用 PCM 和 ADPCM 演算法播放和錄製的取樣率。</span><span class="sxs-lookup"><span data-stu-id="8700a-152">This value sets the sample rate for playing and recording with the PCM and ADPCM algorithms.</span></span> <span data-ttu-id="8700a-153">檔案會以這種格式儲存。</span><span class="sxs-lookup"><span data-stu-id="8700a-153">The file is saved in this format.</span></span>

</dd> <dt>

<span data-ttu-id="8700a-154"><span id="MCI_DGV_SETAUDIO_SOURCE"></span><span id="mci_dgv_setaudio_source"></span>MCI \_ DGV \_ SETAUDIO \_ 來源</span><span class="sxs-lookup"><span data-stu-id="8700a-154"><span id="MCI_DGV_SETAUDIO_SOURCE"></span><span id="mci_dgv_setaudio_source"></span>MCI\_DGV\_SETAUDIO\_SOURCE</span></span>
</dt> <dd>

<span data-ttu-id="8700a-155">指定音訊輸入來源的常數會包含在由 *lpSetAudio* 所識別之結構的 **dwValue** 成員中。</span><span class="sxs-lookup"><span data-stu-id="8700a-155">A constant specifying the source of audio input is included in the **dwValue** member of the structure identified by *lpSetAudio*.</span></span> <span data-ttu-id="8700a-156">下列是針對音訊輸入來源定義的常數：</span><span class="sxs-lookup"><span data-stu-id="8700a-156">The following constants are defined for the audio input sources:</span></span>

<span data-ttu-id="8700a-157">MCI \_ DGV \_ SETAUDIO \_ 來源 \_ 平均</span><span class="sxs-lookup"><span data-stu-id="8700a-157">MCI\_DGV\_SETAUDIO\_SOURCE\_AVERAGE</span></span>

<span data-ttu-id="8700a-158">左右音訊頻道的平均值。</span><span class="sxs-lookup"><span data-stu-id="8700a-158">The average of the left and right audio channels.</span></span>

<span data-ttu-id="8700a-159">剩餘的 MCI \_ DGV \_ SETAUDIO \_ 來源 \_</span><span class="sxs-lookup"><span data-stu-id="8700a-159">MCI\_DGV\_SETAUDIO\_SOURCE\_LEFT</span></span>

<span data-ttu-id="8700a-160">左聲道。</span><span class="sxs-lookup"><span data-stu-id="8700a-160">Left audio channel.</span></span>

<span data-ttu-id="8700a-161">MCI \_ DGV \_ SETAUDIO \_ 來源 \_ 右邊</span><span class="sxs-lookup"><span data-stu-id="8700a-161">MCI\_DGV\_SETAUDIO\_SOURCE\_RIGHT</span></span>

<span data-ttu-id="8700a-162">右音訊頻道。</span><span class="sxs-lookup"><span data-stu-id="8700a-162">Right audio channel.</span></span>

<span data-ttu-id="8700a-163">MCI \_ DGV \_ SETAUDIO \_ 來源 \_ 身歷聲</span><span class="sxs-lookup"><span data-stu-id="8700a-163">MCI\_DGV\_SETAUDIO\_SOURCE\_STEREO</span></span>

<span data-ttu-id="8700a-164">立體。</span><span class="sxs-lookup"><span data-stu-id="8700a-164">Stereo.</span></span>

</dd> <dt>

<span data-ttu-id="8700a-165"><span id="MCI_DGV_SETAUDIO_STREAM"></span><span id="mci_dgv_setaudio_stream"></span>MCI \_ DGV \_ SETAUDIO \_ STREAM</span><span class="sxs-lookup"><span data-stu-id="8700a-165"><span id="MCI_DGV_SETAUDIO_STREAM"></span><span id="mci_dgv_setaudio_stream"></span>MCI\_DGV\_SETAUDIO\_STREAM</span></span>
</dt> <dd>

<span data-ttu-id="8700a-166">音訊資料流程是在 *lpSetAudio* 所識別之結構的 **dwValue** 成員中指定。</span><span class="sxs-lookup"><span data-stu-id="8700a-166">An audio-stream is specified in the **dwValue** member of the structure identified by *lpSetAudio*.</span></span> <span data-ttu-id="8700a-167">整數值指定從工作區播放的音訊串流。</span><span class="sxs-lookup"><span data-stu-id="8700a-167">The integer value specifies the audio stream played back from the workspace.</span></span> <span data-ttu-id="8700a-168">如果未指定資料流程，則會播放第一個實際交錯的音訊資料流程。</span><span class="sxs-lookup"><span data-stu-id="8700a-168">If the stream is not specified, the first physically interleaved audio stream is played.</span></span>

</dd> <dt>

<span data-ttu-id="8700a-169"><span id="MCI_DGV_SETAUDIO_TREBLE"></span><span id="mci_dgv_setaudio_treble"></span>MCI \_ DGV \_ SETAUDIO \_ 高音</span><span class="sxs-lookup"><span data-stu-id="8700a-169"><span id="MCI_DGV_SETAUDIO_TREBLE"></span><span id="mci_dgv_setaudio_treble"></span>MCI\_DGV\_SETAUDIO\_TREBLE</span></span>
</dt> <dd>

<span data-ttu-id="8700a-170">音訊高頻率層級會指定為 *lpSetAudio* 所識別之結構的 **dwValue** 成員中的一個因素。</span><span class="sxs-lookup"><span data-stu-id="8700a-170">The audio high-frequency level is specified as a factor in the **dwValue** member of the structure identified by *lpSetAudio*.</span></span>

</dd> <dt>

<span data-ttu-id="8700a-171"><span id="MCI_DGV_SETAUDIO_VOLUME"></span><span id="mci_dgv_setaudio_volume"></span>MCI \_ DGV \_ SETAUDIO \_ VOLUME</span><span class="sxs-lookup"><span data-stu-id="8700a-171"><span id="MCI_DGV_SETAUDIO_VOLUME"></span><span id="mci_dgv_setaudio_volume"></span>MCI\_DGV\_SETAUDIO\_VOLUME</span></span>
</dt> <dd>

<span data-ttu-id="8700a-172">其中一個或兩個音訊通道的音訊層級，會指定為 *lpSetAudio* 所識別之結構的 **dwValue** 成員中的一個因素。</span><span class="sxs-lookup"><span data-stu-id="8700a-172">The audio level for one or both audio channels is specified as a factor in the **dwValue** member of the structure identified by *lpSetAudio*.</span></span> <span data-ttu-id="8700a-173">如果左方和右邊的磁片區已設定為不同的值，則從左至右磁片區的比率大約是未變更。</span><span class="sxs-lookup"><span data-stu-id="8700a-173">If the left and right volumes have been set to different values, then the ratio of left to right volume is approximately unchanged.</span></span>

</dd> <dt>

<span data-ttu-id="8700a-174"><span id="MCI_DGV_SETAUDIO_LEFT"></span><span id="mci_dgv_setaudio_left"></span>\_ \_ SETAUDIO \_ 剩下的 MCI DGV</span><span class="sxs-lookup"><span data-stu-id="8700a-174"><span id="MCI_DGV_SETAUDIO_LEFT"></span><span id="mci_dgv_setaudio_left"></span>MCI\_DGV\_SETAUDIO\_LEFT</span></span>
</dt> <dd>

<span data-ttu-id="8700a-175">在搭配使用的 MCI 設定時啟用左 \_ 聲道 \_ 。</span><span class="sxs-lookup"><span data-stu-id="8700a-175">Enables the left audio channel when used with MCI\_SET\_ON.</span></span> <span data-ttu-id="8700a-176">當使用的 MCI 設定為 OFF 時，停用左聲道 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="8700a-176">Disables the left audio channel when used with MCI\_SET\_OFF.</span></span> <span data-ttu-id="8700a-177">當此旗標搭配 MCI \_ DGV \_ SETAUDIO \_ VALUE 和 mci DGV SETAUDIO VOLUME 的組合使用時 \_ \_ \_ ，它會設定左方音訊頻道的音量。</span><span class="sxs-lookup"><span data-stu-id="8700a-177">When this flag is used with the combination of MCI\_DGV\_SETAUDIO\_VALUE and MCI\_DGV\_SETAUDIO\_VOLUME, it sets the volume of the left audio channel.</span></span> <span data-ttu-id="8700a-178">當此旗標與 MCI \_ DGV SETAUDIO 來源搭配使用時 \_ \_ ，它會指定左方音訊頻道作為音訊輸入數位板的來源。</span><span class="sxs-lookup"><span data-stu-id="8700a-178">When this flag is used with MCI\_DGV\_SETAUDIO\_SOURCE, it specifies the left audio channel as the source for the audio input digitizer.</span></span>

</dd> <dt>

<span data-ttu-id="8700a-179"><span id="MCI_DGV_SETAUDIO_OVER"></span><span id="mci_dgv_setaudio_over"></span>MCI \_ DGV \_ SETAUDIO \_</span><span class="sxs-lookup"><span data-stu-id="8700a-179"><span id="MCI_DGV_SETAUDIO_OVER"></span><span id="mci_dgv_setaudio_over"></span>MCI\_DGV\_SETAUDIO\_OVER</span></span>
</dt> <dd>

<span data-ttu-id="8700a-180">轉換長度參數會包含在由 *lpSetAudio* 所識別之結構的 **dwOver** 成員中。</span><span class="sxs-lookup"><span data-stu-id="8700a-180">A transition length parameter is included in the **dwOver** member of the structure identified by *lpSetAudio*.</span></span> <span data-ttu-id="8700a-181">[長度] 值會指定以目前時間格式的單位 (的時間長度，) 需要進行使用因素的變更。</span><span class="sxs-lookup"><span data-stu-id="8700a-181">The length value specifies how long (in units of the current time format) it should take to make a change that uses a factor.</span></span> <span data-ttu-id="8700a-182">如果未使用此旗標，則會立即進行變更。</span><span class="sxs-lookup"><span data-stu-id="8700a-182">If this flag is not used, changes occur immediately.</span></span>

</dd> <dt>

<span data-ttu-id="8700a-183"><span id="MCI_DGV_SETAUDIO_QUALITY"></span><span id="mci_dgv_setaudio_quality"></span>MCI \_ DGV \_ SETAUDIO \_ 品質</span><span class="sxs-lookup"><span data-stu-id="8700a-183"><span id="MCI_DGV_SETAUDIO_QUALITY"></span><span id="mci_dgv_setaudio_quality"></span>MCI\_DGV\_SETAUDIO\_QUALITY</span></span>
</dt> <dd>

<span data-ttu-id="8700a-184">*LpSetAudio* 所識別之結構的 **lpstrQuality** 成員包含定義音訊品質的緩衝區位址。</span><span class="sxs-lookup"><span data-stu-id="8700a-184">The **lpstrQuality** member of the structure identified by *lpSetAudio* contains an address of a buffer defining the audio quality.</span></span> <span data-ttu-id="8700a-185">緩衝區內的文字字串會指定音訊壓縮演算法的特性。</span><span class="sxs-lookup"><span data-stu-id="8700a-185">A text-string within the buffer specifies the characteristics of the audio compression algorithm.</span></span>

<span data-ttu-id="8700a-186">您 \_ \_ 可以使用 MCI DGV SETAUDIO \_ ALG 旗標來選取指定演算法的品質描述項。</span><span class="sxs-lookup"><span data-stu-id="8700a-186">The MCI\_DGV\_SETAUDIO\_ALG flag can be used to select a quality descriptor for the specified algorithm.</span></span> <span data-ttu-id="8700a-187">如果省略此旗標，則會使用目前的演算法。</span><span class="sxs-lookup"><span data-stu-id="8700a-187">If this flag is omitted, then the current algorithm is used.</span></span>

<span data-ttu-id="8700a-188">可用的演算法和描述項名稱取決於裝置。</span><span class="sxs-lookup"><span data-stu-id="8700a-188">The algorithms and descriptor names available depend on the device.</span></span> <span data-ttu-id="8700a-189">每個裝置都會提供可用演算法的相關檔，以及適用描述項名稱的描述。</span><span class="sxs-lookup"><span data-stu-id="8700a-189">Each device supplies documentation for the available algorithms and a description of the applicable descriptor names.</span></span> <span data-ttu-id="8700a-190">[MCI \_ QUALITY](mci-quality.md)命令可以定義其他描述項名稱。</span><span class="sxs-lookup"><span data-stu-id="8700a-190">The [MCI\_QUALITY](mci-quality.md) command can define additional descriptor names.</span></span>

</dd> <dt>

<span data-ttu-id="8700a-191"><span id="MCI_DGV_SETAUDIO_RECORD"></span><span id="mci_dgv_setaudio_record"></span>MCI \_ DGV \_ SETAUDIO \_ 記錄</span><span class="sxs-lookup"><span data-stu-id="8700a-191"><span id="MCI_DGV_SETAUDIO_RECORD"></span><span id="mci_dgv_setaudio_record"></span>MCI\_DGV\_SETAUDIO\_RECORD</span></span>
</dt> <dd>

<span data-ttu-id="8700a-192">指定錄製是否包含或排除音訊資料。</span><span class="sxs-lookup"><span data-stu-id="8700a-192">Specifies whether recording includes or excludes audio data.</span></span> <span data-ttu-id="8700a-193">當結合的 MCI \_ 設定 \_ 為時，會記錄音訊資料。</span><span class="sxs-lookup"><span data-stu-id="8700a-193">When combined with MCI\_SET\_ON, audio data is recorded.</span></span> <span data-ttu-id="8700a-194">當 \_ 將 MCI 設定為 \_ OFF 時，會排除音訊資料。</span><span class="sxs-lookup"><span data-stu-id="8700a-194">When combined with MCI\_SET\_OFF, audio data is excluded.</span></span> <span data-ttu-id="8700a-195">預設值包含音訊資料。</span><span class="sxs-lookup"><span data-stu-id="8700a-195">The default includes audio data.</span></span>

</dd> <dt>

<span data-ttu-id="8700a-196"><span id="MCI_DGV_SETAUDIO_RIGHT"></span><span id="mci_dgv_setaudio_right"></span>MCI \_ DGV \_ SETAUDIO \_ RIGHT</span><span class="sxs-lookup"><span data-stu-id="8700a-196"><span id="MCI_DGV_SETAUDIO_RIGHT"></span><span id="mci_dgv_setaudio_right"></span>MCI\_DGV\_SETAUDIO\_RIGHT</span></span>
</dt> <dd>

<span data-ttu-id="8700a-197">搭配使用設定的 MCI 時，可啟用正確的音訊通道 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="8700a-197">Enables the right audio channel when used with MCI\_SET\_ON.</span></span> <span data-ttu-id="8700a-198">當搭配使用的 MCI 設定為 OFF 時，會停用正確的音訊通道 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="8700a-198">Disables the right audio channel when used with MCI\_SET\_OFF.</span></span> <span data-ttu-id="8700a-199">當此旗標搭配 MCI \_ DGV \_ SETAUDIO \_ VALUE 和 mci DGV SETAUDIO VOLUME 的組合使用時 \_ \_ \_ ，它會設定正確音訊通道的音量。</span><span class="sxs-lookup"><span data-stu-id="8700a-199">When this flag is used with the combination of MCI\_DGV\_SETAUDIO\_VALUE and MCI\_DGV\_SETAUDIO\_VOLUME, it sets the volume of the right audio channel.</span></span>

</dd> <dt>

<span data-ttu-id="8700a-200"><span id="MCI_DGV_SETAUDIO_VALUE"></span><span id="mci_dgv_setaudio_value"></span>MCI \_ DGV \_ SETAUDIO \_ 值</span><span class="sxs-lookup"><span data-stu-id="8700a-200"><span id="MCI_DGV_SETAUDIO_VALUE"></span><span id="mci_dgv_setaudio_value"></span>MCI\_DGV\_SETAUDIO\_VALUE</span></span>
</dt> <dd>

<span data-ttu-id="8700a-201">值是在 *lpSetAudio* 所識別之結構的 **dwValue** 成員中指定。</span><span class="sxs-lookup"><span data-stu-id="8700a-201">A value is specified in the **dwValue** member of the structure identified by *lpSetAudio*.</span></span> <span data-ttu-id="8700a-202">值的意義是由針對 MCI \_ DGV \_ SETAUDIO 專案旗標定義的常數所指定 \_ 。</span><span class="sxs-lookup"><span data-stu-id="8700a-202">The meaning of the value is specified by the constant defined for the MCI\_DGV\_SETAUDIO\_ITEM flag.</span></span>

</dd> <dt>

<span data-ttu-id="8700a-203"><span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>已 \_ 設定 \_ MCI</span><span class="sxs-lookup"><span data-stu-id="8700a-203"><span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>MCI\_SET\_OFF</span></span>
</dt> <dd>

<span data-ttu-id="8700a-204">停用指定的音訊通道。</span><span class="sxs-lookup"><span data-stu-id="8700a-204">Disables the specified audio channel.</span></span>

</dd> <dt>

<span data-ttu-id="8700a-205"><span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI \_ 設定 \_ 于</span><span class="sxs-lookup"><span data-stu-id="8700a-205"><span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI\_SET\_ON</span></span>
</dt> <dd>

<span data-ttu-id="8700a-206">啟用指定的音訊通道。</span><span class="sxs-lookup"><span data-stu-id="8700a-206">Enables the specified audio channel.</span></span>

</dd> <dt>

<span data-ttu-id="8700a-207"><span id="MCI_SETAUDIO_OUTPUT"></span><span id="mci_setaudio_output"></span>MCI \_ SETAUDIO \_ 輸出</span><span class="sxs-lookup"><span data-stu-id="8700a-207"><span id="MCI_SETAUDIO_OUTPUT"></span><span id="mci_setaudio_output"></span>MCI\_SETAUDIO\_OUTPUT</span></span>
</dt> <dd>

<span data-ttu-id="8700a-208">修改低音、高音或音量旗標，讓它只修改播放的信號，而不是記錄的內容。</span><span class="sxs-lookup"><span data-stu-id="8700a-208">Modifies the bass, treble, or volume flag so that it modifies only the played signal and not what is recorded.</span></span> <span data-ttu-id="8700a-209">可能的話，這是監視輸入時的預設值。</span><span class="sxs-lookup"><span data-stu-id="8700a-209">If possible, this is the default when monitoring the input.</span></span>

</dd> </dl>

<span data-ttu-id="8700a-210">針對數位影片裝置， *lpSetAudio* 參數會指向 [**MCI \_ DGV \_ SETAUDIO \_ PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_setaudio_parmsa) 結構。</span><span class="sxs-lookup"><span data-stu-id="8700a-210">For digital-video devices, the *lpSetAudio* parameter points to an [**MCI\_DGV\_SETAUDIO\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_setaudio_parmsa) structure.</span></span>

<span data-ttu-id="8700a-211">下列其他旗標適用于 **vcr** 裝置類型：</span><span class="sxs-lookup"><span data-stu-id="8700a-211">The following additional flags are used with the **vcr** device type:</span></span>

<dl> <dt>

<span data-ttu-id="8700a-212"><span id="MCI_VCR_SETAUDIO_RECORD"></span><span id="mci_vcr_setaudio_record"></span>MCI \_ VCR \_ SETAUDIO \_ 記錄</span><span class="sxs-lookup"><span data-stu-id="8700a-212"><span id="MCI_VCR_SETAUDIO_RECORD"></span><span id="mci_vcr_setaudio_record"></span>MCI\_VCR\_SETAUDIO\_RECORD</span></span>
</dt> <dd>

<span data-ttu-id="8700a-213">將音訊錄製設定為 on 或 off，以搭配下列其中一個旗標使用：</span><span class="sxs-lookup"><span data-stu-id="8700a-213">Sets the audio recording to on or off, which is used in conjunction with one of following flags:</span></span>

<span data-ttu-id="8700a-214">MCI \_ 設定 \_ 于</span><span class="sxs-lookup"><span data-stu-id="8700a-214">MCI\_SET\_ON</span></span>

<span data-ttu-id="8700a-215">錄製音訊。</span><span class="sxs-lookup"><span data-stu-id="8700a-215">Audio recording on.</span></span>

<span data-ttu-id="8700a-216">已 \_ 設定 \_ MCI</span><span class="sxs-lookup"><span data-stu-id="8700a-216">MCI\_SET\_OFF</span></span>

<span data-ttu-id="8700a-217">錄製音訊。</span><span class="sxs-lookup"><span data-stu-id="8700a-217">Audio recording off.</span></span> <span data-ttu-id="8700a-218">您可能必須先關閉組合錄製 (使用 [mci \_ set](mci-set.md) 命令，並將 [mci \_ VCR \_ 組 \_ 組合 \_ 記錄] 旗標設為 [關閉]) ，然後才能關閉音訊錄製。</span><span class="sxs-lookup"><span data-stu-id="8700a-218">It might be necessary to first turn off the assemble recording (using the [MCI\_SET](mci-set.md) command with the MCI\_VCR\_SET\_ASSEMBLE\_RECORD flag set to off) before the audio recording can be turned off.</span></span>

<span data-ttu-id="8700a-219">MCI \_ 曲目</span><span class="sxs-lookup"><span data-stu-id="8700a-219">MCI\_TRACK</span></span>

<span data-ttu-id="8700a-220">*LpSetAudio* 所識別之結構的 **dwTrack** 成員會指定受命令影響的追蹤。</span><span class="sxs-lookup"><span data-stu-id="8700a-220">The **dwTrack** member of the structure identified by *lpSetAudio* specifies which track is affected by the command.</span></span>

<span data-ttu-id="8700a-221">MCI \_ VCR \_ SETAUDIO \_ 來源</span><span class="sxs-lookup"><span data-stu-id="8700a-221">MCI\_VCR\_SETAUDIO\_SOURCE</span></span>

<span data-ttu-id="8700a-222">設定音訊來源。</span><span class="sxs-lookup"><span data-stu-id="8700a-222">Sets the audio source.</span></span> <span data-ttu-id="8700a-223">此旗標必須與 MCI \_ VCR SETAUDIO 搭配 \_ 使用 \_ 以進行旗標。</span><span class="sxs-lookup"><span data-stu-id="8700a-223">This flag must be used with the MCI\_VCR\_SETAUDIO\_TO flag.</span></span>

<span data-ttu-id="8700a-224">MCI \_ VCR \_ SETAUDIO \_ 監視</span><span class="sxs-lookup"><span data-stu-id="8700a-224">MCI\_VCR\_SETAUDIO\_MONITOR</span></span>

<span data-ttu-id="8700a-225">設定音訊來源監視器。</span><span class="sxs-lookup"><span data-stu-id="8700a-225">Sets the audio source monitor.</span></span> <span data-ttu-id="8700a-226">此旗標必須與 MCI \_ VCR SETAUDIO 搭配 \_ 使用 \_ 以進行旗標。</span><span class="sxs-lookup"><span data-stu-id="8700a-226">This flag must be used with the MCI\_VCR\_SETAUDIO\_TO flag.</span></span>

<span data-ttu-id="8700a-227">MCI \_ VCR \_ SETAUDIO \_ 至</span><span class="sxs-lookup"><span data-stu-id="8700a-227">MCI\_VCR\_SETAUDIO\_TO</span></span>

<span data-ttu-id="8700a-228">由 *lpSetAudio* 所識別之結構的 **dwTo** 成員，包含描述輸入或受監視輸入類型的常數。</span><span class="sxs-lookup"><span data-stu-id="8700a-228">The **dwTo** member of the structure identified by *lpSetAudio* contains a constant describing the type of input or monitored input.</span></span> <span data-ttu-id="8700a-229">它必須是下列其中一項：</span><span class="sxs-lookup"><span data-stu-id="8700a-229">It must be one of the following:</span></span>

<span data-ttu-id="8700a-230"><dl> <dd></span><span class="sxs-lookup"><span data-stu-id="8700a-230"><dl> <dd></span></span>

<span data-ttu-id="8700a-231">MCI \_ VCR \_ SRC \_ 類型 \_ 調諧器</span><span class="sxs-lookup"><span data-stu-id="8700a-231">MCI\_VCR\_SRC\_TYPE\_TUNER</span></span>

<span data-ttu-id="8700a-232">類型為調諧器。</span><span class="sxs-lookup"><span data-stu-id="8700a-232">Type is tuner.</span></span>

</dd> <dd>

<span data-ttu-id="8700a-233">MCI \_ VCR \_ SRC \_ 類型 \_ 行</span><span class="sxs-lookup"><span data-stu-id="8700a-233">MCI\_VCR\_SRC\_TYPE\_LINE</span></span>

<span data-ttu-id="8700a-234">類型為 line。</span><span class="sxs-lookup"><span data-stu-id="8700a-234">Type is line.</span></span>

</dd> <dd>

<span data-ttu-id="8700a-235">MCI \_ VCR \_ SRC \_ 類型 \_ AUX</span><span class="sxs-lookup"><span data-stu-id="8700a-235">MCI\_VCR\_SRC\_TYPE\_AUX</span></span>

<span data-ttu-id="8700a-236">類型為輔助。</span><span class="sxs-lookup"><span data-stu-id="8700a-236">Type is auxiliary.</span></span>

</dd> <dd>

<span data-ttu-id="8700a-237">MCI \_ VCR \_ SRC \_ 類型 \_ 泛型</span><span class="sxs-lookup"><span data-stu-id="8700a-237">MCI\_VCR\_SRC\_TYPE\_GENERIC</span></span>

<span data-ttu-id="8700a-238">類型為泛型。</span><span class="sxs-lookup"><span data-stu-id="8700a-238">Type is generic.</span></span>

</dd> <dd>

<span data-ttu-id="8700a-239">MCI \_ VCR \_ SRC \_ 類型 \_ 靜音</span><span class="sxs-lookup"><span data-stu-id="8700a-239">MCI\_VCR\_SRC\_TYPE\_MUTE</span></span>

<span data-ttu-id="8700a-240">類型為靜音。</span><span class="sxs-lookup"><span data-stu-id="8700a-240">Type is mute.</span></span> <span data-ttu-id="8700a-241">這只能與 MCI \_ VCR \_ SETAUDIO 來源旗標搭配使用 \_ 。</span><span class="sxs-lookup"><span data-stu-id="8700a-241">This can be used only with the MCI\_VCR\_SETAUDIO\_SOURCE flag.</span></span>

</dd> <dd>

<span data-ttu-id="8700a-242">MCI \_ VCR \_ SRC \_ 類型 \_ 輸出</span><span class="sxs-lookup"><span data-stu-id="8700a-242">MCI\_VCR\_SRC\_TYPE\_OUTPUT</span></span>

<span data-ttu-id="8700a-243">類型為 output。</span><span class="sxs-lookup"><span data-stu-id="8700a-243">Type is output.</span></span>

</dd> <dd>

<span data-ttu-id="8700a-244">MCI \_ VCR \_ SETAUDIO \_ 號碼</span><span class="sxs-lookup"><span data-stu-id="8700a-244">MCI\_VCR\_SETAUDIO\_NUMBER</span></span>

<span data-ttu-id="8700a-245">LpSetAudio 所識別之結構的 dwNumber 成員包含要使用的 dwTo 成員) 中所指定類型的音訊輸入 (。</span><span class="sxs-lookup"><span data-stu-id="8700a-245">The dwNumber member of the structure identified by lpSetAudio contains the audio input (of the type specified in the dwTo member) to use.</span></span>

</dd> </dl> </dd> <dt>


</dt> <dd></dd> <dt>


</dt> <dd></dd> <dt>


</dt> <dd></dd> </dl>

<span data-ttu-id="8700a-246">若為 VCR 裝置， *lpSetAudio* 參數會指向 [**MCI \_ VCR \_ SETAUDIO \_ PARMS**](mci-vcr-setaudio-parms.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="8700a-246">For VCR devices, the *lpSetAudio* parameter points to an [**MCI\_VCR\_SETAUDIO\_PARMS**](mci-vcr-setaudio-parms.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="8700a-247">規格需求</span><span class="sxs-lookup"><span data-stu-id="8700a-247">Requirements</span></span>



| <span data-ttu-id="8700a-248">需求</span><span class="sxs-lookup"><span data-stu-id="8700a-248">Requirement</span></span> | <span data-ttu-id="8700a-249">值</span><span class="sxs-lookup"><span data-stu-id="8700a-249">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8700a-250">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8700a-250">Minimum supported client</span></span><br/> | <span data-ttu-id="8700a-251">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8700a-251">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="8700a-252">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8700a-252">Minimum supported server</span></span><br/> | <span data-ttu-id="8700a-253">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8700a-253">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="8700a-254">標頭</span><span class="sxs-lookup"><span data-stu-id="8700a-254">Header</span></span><br/>                   | <dl> <span data-ttu-id="8700a-255"><dt>Mmsystem (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="8700a-255"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8700a-256">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8700a-256">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8700a-257">Mci</span><span class="sxs-lookup"><span data-stu-id="8700a-257">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="8700a-258">MCI 命令</span><span class="sxs-lookup"><span data-stu-id="8700a-258">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

