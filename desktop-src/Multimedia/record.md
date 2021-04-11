---
title: 記錄命令
description: 記錄命令會開始記錄資料。 VCR 和波形-音訊裝置會辨識此命令。 雖然數位視訊裝置和 MIDI sequencers 也會辨識此命令，但 MCIAVI 和 MCISEQ 驅動程式並不會執行此命令。
ms.assetid: a0838153-5ac2-437f-ae1e-0c4f950fcac5
keywords:
- 錄製命令 Windows 多媒體
topic_type:
- apiref
api_name:
- record
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b39d3659d4577517726260f948563cd31ecc07bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843120"
---
# <a name="record-command"></a><span data-ttu-id="d0dd8-106">記錄命令</span><span class="sxs-lookup"><span data-stu-id="d0dd8-106">record command</span></span>

<span data-ttu-id="d0dd8-107">記錄命令會開始記錄資料。</span><span class="sxs-lookup"><span data-stu-id="d0dd8-107">The record command starts recording data.</span></span> <span data-ttu-id="d0dd8-108">VCR 和波形-音訊裝置會辨識此命令。</span><span class="sxs-lookup"><span data-stu-id="d0dd8-108">VCR and waveform-audio devices recognize this command.</span></span> <span data-ttu-id="d0dd8-109">雖然數位視訊裝置和 MIDI sequencers 也會辨識此命令，但 MCIAVI 和 MCISEQ 驅動程式並不會執行此命令。</span><span class="sxs-lookup"><span data-stu-id="d0dd8-109">Although digital-video devices and MIDI sequencers also recognize this command, the MCIAVI and MCISEQ drivers do not implement it.</span></span>

<span data-ttu-id="d0dd8-110">若要傳送此命令，請使用 *lpszCommand* 參數設定來呼叫 [**mciSendString**](/previous-versions//dd757161(v=vs.85))函式，如下所示。</span><span class="sxs-lookup"><span data-stu-id="d0dd8-110">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("record %s %s %s"), 
  lpszDeviceID, 
  lpszRecordFlags, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="d0dd8-111">參數</span><span class="sxs-lookup"><span data-stu-id="d0dd8-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0dd8-112"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="d0dd8-112"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="d0dd8-113">MCI 裝置的識別碼。</span><span class="sxs-lookup"><span data-stu-id="d0dd8-113">Identifier of an MCI device.</span></span> <span data-ttu-id="d0dd8-114">開啟裝置時，會指派此識別碼或別名。</span><span class="sxs-lookup"><span data-stu-id="d0dd8-114">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="d0dd8-115"><span id="lpszRecordFlags"></span><span id="lpszrecordflags"></span><span id="LPSZRECORDFLAGS"></span>*lpszRecordFlags*</span><span class="sxs-lookup"><span data-stu-id="d0dd8-115"><span id="lpszRecordFlags"></span><span id="lpszrecordflags"></span><span id="LPSZRECORDFLAGS"></span>*lpszRecordFlags*</span></span>
</dt> <dd>

<span data-ttu-id="d0dd8-116">記錄資料的旗標。</span><span class="sxs-lookup"><span data-stu-id="d0dd8-116">Flag for recording data.</span></span> <span data-ttu-id="d0dd8-117">下表列出可辨識 **記錄** 命令的裝置類型，以及每種類型使用的旗標。</span><span class="sxs-lookup"><span data-stu-id="d0dd8-117">The following table lists device types that recognize the **record** command and the flags used by each type.</span></span>



| <span data-ttu-id="d0dd8-118">值</span><span class="sxs-lookup"><span data-stu-id="d0dd8-118">Value</span></span>        | <span data-ttu-id="d0dd8-119">意義</span><span class="sxs-lookup"><span data-stu-id="d0dd8-119">Meaning</span></span>                                                | <span data-ttu-id="d0dd8-120">意義</span><span class="sxs-lookup"><span data-stu-id="d0dd8-120">Meaning</span></span>                                             |
|--------------|--------------------------------------------------------|-----------------------------------------------------|
| <span data-ttu-id="d0dd8-121">digitalvideo</span><span class="sxs-lookup"><span data-stu-id="d0dd8-121">digitalvideo</span></span> | <span data-ttu-id="d0dd8-122">從 *位置* 保留的 *矩形* 音訊串流 *串流*</span><span class="sxs-lookup"><span data-stu-id="d0dd8-122">at *rectangle* audio stream *stream* from *position* hold</span></span> | <span data-ttu-id="d0dd8-123">插入覆寫以 *定位* 影片串流 *串流*</span><span class="sxs-lookup"><span data-stu-id="d0dd8-123">insert overwrite to *position* video stream *stream*</span></span> |
| <span data-ttu-id="d0dd8-124">排序器</span><span class="sxs-lookup"><span data-stu-id="d0dd8-124">sequencer</span></span>    | <span data-ttu-id="d0dd8-125">從 *位置* 插入</span><span class="sxs-lookup"><span data-stu-id="d0dd8-125">from *position* insert</span></span>                                  | <span data-ttu-id="d0dd8-126">覆寫至 *位置*</span><span class="sxs-lookup"><span data-stu-id="d0dd8-126">overwrite to *position*</span></span>                             |
| <span data-ttu-id="d0dd8-127">錄影機</span><span class="sxs-lookup"><span data-stu-id="d0dd8-127">vcr</span></span>          | <span data-ttu-id="d0dd8-128">從 *位置* 初始化的 *時間*</span><span class="sxs-lookup"><span data-stu-id="d0dd8-128">at *time* from *position* initialize</span></span>                     | <span data-ttu-id="d0dd8-129">將覆寫插入至 *位置*</span><span class="sxs-lookup"><span data-stu-id="d0dd8-129">insert overwrite to *position*</span></span>                      |
| <span data-ttu-id="d0dd8-130">waveaudio</span><span class="sxs-lookup"><span data-stu-id="d0dd8-130">waveaudio</span></span>    | <span data-ttu-id="d0dd8-131">從 *位置* 插入</span><span class="sxs-lookup"><span data-stu-id="d0dd8-131">from *position* insert</span></span>                                  | <span data-ttu-id="d0dd8-132">覆寫至 *位置*</span><span class="sxs-lookup"><span data-stu-id="d0dd8-132">overwrite to *position*</span></span>                             |



 

<span data-ttu-id="d0dd8-133">下表列出可在 **lpszRecordFlags** 參數中指定的旗標，以及它們的意義。</span><span class="sxs-lookup"><span data-stu-id="d0dd8-133">The following table lists the flags that can be specified in the **lpszRecordFlags** parameter and their meanings.</span></span>



| <span data-ttu-id="d0dd8-134">值</span><span class="sxs-lookup"><span data-stu-id="d0dd8-134">Value</span></span>                 | <span data-ttu-id="d0dd8-135">意義</span><span class="sxs-lookup"><span data-stu-id="d0dd8-135">Meaning</span></span>                                                                                                                                                                                                                                                                                                          |
|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0dd8-136">在 *矩形*</span><span class="sxs-lookup"><span data-stu-id="d0dd8-136">at *rectangle*</span></span>        | <span data-ttu-id="d0dd8-137">指定外部輸入的矩形區域，做為壓縮和儲存的圖元來源。</span><span class="sxs-lookup"><span data-stu-id="d0dd8-137">Specifies a rectangular region of the external input used as the source for the pixels compressed and saved.</span></span> <span data-ttu-id="d0dd8-138">如果未指定，矩形會預設為 [put](put.md) "video" 所指定的矩形。</span><span class="sxs-lookup"><span data-stu-id="d0dd8-138">If not specified, the rectangle defaults to the rectangle specified for [put](put.md) "video".</span></span> <span data-ttu-id="d0dd8-139">當不同于「影片」矩形的設定時，所顯示的影像並不是所錄製的影像。</span><span class="sxs-lookup"><span data-stu-id="d0dd8-139">When it is set differently from the "video" rectangle, the displayed image is not what is recorded.</span></span> |
| <span data-ttu-id="d0dd8-140">*準時*</span><span class="sxs-lookup"><span data-stu-id="d0dd8-140">at *time*</span></span>             | <span data-ttu-id="d0dd8-141">指出裝置應該開始執行此命令的時間，如果裝置已 cued，則在 cued 命令開始時。</span><span class="sxs-lookup"><span data-stu-id="d0dd8-141">Indicates when the device should begin performing this command, or, if the device has been cued, when the cued command begins.</span></span> <span data-ttu-id="d0dd8-142">如需詳細資訊，請參閱 [提示](cue.md) 命令。</span><span class="sxs-lookup"><span data-stu-id="d0dd8-142">For more information, see the [cue](cue.md) command.</span></span>                                                                                                                             |
| <span data-ttu-id="d0dd8-143">音訊串流 *串流*</span><span class="sxs-lookup"><span data-stu-id="d0dd8-143">audio stream *stream*</span></span> | <span data-ttu-id="d0dd8-144">指定用於錄製的音訊資料流程。</span><span class="sxs-lookup"><span data-stu-id="d0dd8-144">Specifies the audio stream used for recording.</span></span> <span data-ttu-id="d0dd8-145">如果未指定此旗標，而且檔案格式未定義預設值，則會將它記錄到實際優先的資料流程中。</span><span class="sxs-lookup"><span data-stu-id="d0dd8-145">If this flag is not specified and the file format does not define a default, it is recorded into the stream that is physically first.</span></span>                                                                                                                             |
| <span data-ttu-id="d0dd8-146">從 *位置*</span><span class="sxs-lookup"><span data-stu-id="d0dd8-146">from *position*</span></span>       | <span data-ttu-id="d0dd8-147">指定錄製的開始位置。</span><span class="sxs-lookup"><span data-stu-id="d0dd8-147">Specifies a starting position for the recording.</span></span> <span data-ttu-id="d0dd8-148">如果未指定 "from" 旗標，則裝置會在目前的位置開始錄製。</span><span class="sxs-lookup"><span data-stu-id="d0dd8-148">If the "from" flag is not specified, the device starts recording at the current position.</span></span>                                                                                                                                                                       |
| <span data-ttu-id="d0dd8-149">hold</span><span class="sxs-lookup"><span data-stu-id="d0dd8-149">hold</span></span>                  | <span data-ttu-id="d0dd8-150">錄製完成時凍結影像，而不是顯示即時影片。</span><span class="sxs-lookup"><span data-stu-id="d0dd8-150">Freezes the image when recording has finished instead of showing live video.</span></span> <span data-ttu-id="d0dd8-151">錄製停止時，會執行自動 [監視](monitor.md) "file" 命令。</span><span class="sxs-lookup"><span data-stu-id="d0dd8-151">When recording stops, an automatic [monitor](monitor.md) "file" command is performed.</span></span> <span data-ttu-id="d0dd8-152">若要返回即時影片，請發出 **監視器** "input" 命令。</span><span class="sxs-lookup"><span data-stu-id="d0dd8-152">To return to live video, issue the **monitor** "input" command.</span></span>                                                                              |
| <span data-ttu-id="d0dd8-153">initialize</span><span class="sxs-lookup"><span data-stu-id="d0dd8-153">initialize</span></span>            | <span data-ttu-id="d0dd8-154">將磁帶 (媒體) ，其牽涉到錄製時間碼 (如果可能) 空白的影片和音訊。</span><span class="sxs-lookup"><span data-stu-id="d0dd8-154">Initialize the tape (media), which involves recording timecode (if possible) for blank video and audio.</span></span> <span data-ttu-id="d0dd8-155">如果必須初始化整個磁帶，此命令可能需要數小時的時間。</span><span class="sxs-lookup"><span data-stu-id="d0dd8-155">This command might take several hours if the entire tape must be initialized.</span></span>                                                                                                                            |
| <span data-ttu-id="d0dd8-156">insert</span><span class="sxs-lookup"><span data-stu-id="d0dd8-156">insert</span></span>                | <span data-ttu-id="d0dd8-157">指定將新的資料加入至檔案中的目前位置。</span><span class="sxs-lookup"><span data-stu-id="d0dd8-157">Specifies that new data is added to the file at the current position.</span></span>                                                                                                                                                                                                                                            |
| <span data-ttu-id="d0dd8-158">overwrite</span><span class="sxs-lookup"><span data-stu-id="d0dd8-158">overwrite</span></span>             | <span data-ttu-id="d0dd8-159">指定新的資料將會取代檔案中的資料。</span><span class="sxs-lookup"><span data-stu-id="d0dd8-159">Specifies that new data will replace data in the file.</span></span>                                                                                                                                                                                                                                                           |
| <span data-ttu-id="d0dd8-160">*定位*</span><span class="sxs-lookup"><span data-stu-id="d0dd8-160">to *position*</span></span>         | <span data-ttu-id="d0dd8-161">指定錄製的結束位置。</span><span class="sxs-lookup"><span data-stu-id="d0dd8-161">Specifies an ending position for the recording.</span></span> <span data-ttu-id="d0dd8-162">如果未指定「到」旗標，則會記錄裝置，直到收到「 [停止](stop.md) 」或「 [暫停](pause.md) 」命令為止。</span><span class="sxs-lookup"><span data-stu-id="d0dd8-162">If the "to" flag is not specified, the device records until it receives a [stop](stop.md) or [pause](pause.md) command.</span></span>                                                                                                                                        |
| <span data-ttu-id="d0dd8-163">影片串流 *串流*</span><span class="sxs-lookup"><span data-stu-id="d0dd8-163">video stream *stream*</span></span> | <span data-ttu-id="d0dd8-164">指定用於錄製的影片資料流程。</span><span class="sxs-lookup"><span data-stu-id="d0dd8-164">Specifies the video stream used for recording.</span></span> <span data-ttu-id="d0dd8-165">如果未指定此值，且檔案格式未定義預設值，則會將它記錄到實際優先的資料流程中。</span><span class="sxs-lookup"><span data-stu-id="d0dd8-165">If this is not specified and the file format does not define a default, then it is recorded into the stream that is physically first.</span></span>                                                                                                                             |



 

</dd> <dt>

<span data-ttu-id="d0dd8-166"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="d0dd8-166"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="d0dd8-167">可以是「等候」、「通知」或兩者。</span><span class="sxs-lookup"><span data-stu-id="d0dd8-167">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="d0dd8-168">針對數位影片和 VCR 裝置，也可以指定「測試」。</span><span class="sxs-lookup"><span data-stu-id="d0dd8-168">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="d0dd8-169">如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。</span><span class="sxs-lookup"><span data-stu-id="d0dd8-169">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0dd8-170">傳回值</span><span class="sxs-lookup"><span data-stu-id="d0dd8-170">Return Value</span></span>

<span data-ttu-id="d0dd8-171">如果成功則傳回零，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="d0dd8-171">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="d0dd8-172">備註</span><span class="sxs-lookup"><span data-stu-id="d0dd8-172">Remarks</span></span>

<span data-ttu-id="d0dd8-173">發出 [停止](stop.md) 或 [暫停](pause.md) 命令時，會停止錄製。</span><span class="sxs-lookup"><span data-stu-id="d0dd8-173">The recording stops when a [stop](stop.md) or [pause](pause.md) command is issued.</span></span> <span data-ttu-id="d0dd8-174">針對 MCIWAVE 驅動程式，如果檔案已關閉而不儲存，則會捨棄檔案之後記錄的所有資料。</span><span class="sxs-lookup"><span data-stu-id="d0dd8-174">For the MCIWAVE driver, all data recorded after a file is opened is discarded if the file is closed without saving it.</span></span>

<span data-ttu-id="d0dd8-175">發出使用位置值的任何命令之前，您應該使用 [set](set.md) 命令來設定所需的時間格式。</span><span class="sxs-lookup"><span data-stu-id="d0dd8-175">Before issuing any commands that use position values, you should set the desired time format by using the [set](set.md) command.</span></span> <span data-ttu-id="d0dd8-176">要記錄的追蹤是由 [settimecode](settimecode.md) "record" 指定、設定 "組合記錄"、 [setvideo](setvideo.md) "record" 和 [setaudio](setaudio.md) "record" 命令。</span><span class="sxs-lookup"><span data-stu-id="d0dd8-176">The tracks to be recorded are specified by the [settimecode](settimecode.md) "record", set "assemble record", [setvideo](setvideo.md) "record", and [setaudio](setaudio.md) "record" commands.</span></span>

## <a name="examples"></a><span data-ttu-id="d0dd8-177">範例</span><span class="sxs-lookup"><span data-stu-id="d0dd8-177">Examples</span></span>

<span data-ttu-id="d0dd8-178">下列命令會在目前的位置開始錄製。</span><span class="sxs-lookup"><span data-stu-id="d0dd8-178">The following command starts recording at the current position.</span></span>

``` syntax
record mysound
```

## <a name="requirements"></a><span data-ttu-id="d0dd8-179">規格需求</span><span class="sxs-lookup"><span data-stu-id="d0dd8-179">Requirements</span></span>



| <span data-ttu-id="d0dd8-180">需求</span><span class="sxs-lookup"><span data-stu-id="d0dd8-180">Requirement</span></span> | <span data-ttu-id="d0dd8-181">值</span><span class="sxs-lookup"><span data-stu-id="d0dd8-181">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="d0dd8-182">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d0dd8-182">Minimum supported client</span></span><br/> | <span data-ttu-id="d0dd8-183">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d0dd8-183">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="d0dd8-184">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d0dd8-184">Minimum supported server</span></span><br/> | <span data-ttu-id="d0dd8-185">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d0dd8-185">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="d0dd8-186">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d0dd8-186">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0dd8-187">Mci</span><span class="sxs-lookup"><span data-stu-id="d0dd8-187">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="d0dd8-188">MCI 命令字串</span><span class="sxs-lookup"><span data-stu-id="d0dd8-188">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="d0dd8-189">提示</span><span class="sxs-lookup"><span data-stu-id="d0dd8-189">cue</span></span>](cue.md)
</dt> <dt>

[<span data-ttu-id="d0dd8-190">監控</span><span class="sxs-lookup"><span data-stu-id="d0dd8-190">monitor</span></span>](monitor.md)
</dt> <dt>

[<span data-ttu-id="d0dd8-191">pause</span><span class="sxs-lookup"><span data-stu-id="d0dd8-191">pause</span></span>](pause.md)
</dt> <dt>

[<span data-ttu-id="d0dd8-192">把</span><span class="sxs-lookup"><span data-stu-id="d0dd8-192">put</span></span>](put.md)
</dt> <dt>

[<span data-ttu-id="d0dd8-193">set</span><span class="sxs-lookup"><span data-stu-id="d0dd8-193">set</span></span>](set.md)
</dt> <dt>

[<span data-ttu-id="d0dd8-194">setaudio</span><span class="sxs-lookup"><span data-stu-id="d0dd8-194">setaudio</span></span>](setaudio.md)
</dt> <dt>

[<span data-ttu-id="d0dd8-195">settimecode</span><span class="sxs-lookup"><span data-stu-id="d0dd8-195">settimecode</span></span>](settimecode.md)
</dt> <dt>

[<span data-ttu-id="d0dd8-196">setvideo</span><span class="sxs-lookup"><span data-stu-id="d0dd8-196">setvideo</span></span>](setvideo.md)
</dt> <dt>

[<span data-ttu-id="d0dd8-197">停止</span><span class="sxs-lookup"><span data-stu-id="d0dd8-197">stop</span></span>](stop.md)
</dt> </dl>

 

