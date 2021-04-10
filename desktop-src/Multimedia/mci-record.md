---
title: 'MCI_RECORD 命令 (Mmsystem .h) '
description: MCI \_ 記錄命令會從目前位置或從某個指定位置開始記錄到另一個指定的位置。
ms.assetid: d3c4e8a3-7d81-428e-91d8-d8d63fc0aa02
keywords:
- MCI_RECORD 命令 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_RECORD
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec1cd15974753b8f40abd87b8d93622c090e2a57
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104010"
---
# <a name="mci_record-command"></a><span data-ttu-id="14893-104">MCI \_ 記錄命令</span><span class="sxs-lookup"><span data-stu-id="14893-104">MCI\_RECORD command</span></span>

<span data-ttu-id="14893-105">[**MCI \_ 記錄**](mci-record-parms.md)命令會從目前位置或從某個指定位置開始記錄到另一個指定的位置。</span><span class="sxs-lookup"><span data-stu-id="14893-105">The [**MCI\_RECORD**](mci-record-parms.md) command starts recording from the current position or from one specified location to another specified location.</span></span> <span data-ttu-id="14893-106">VCR 和波形-音訊裝置會辨識此命令。</span><span class="sxs-lookup"><span data-stu-id="14893-106">VCR and waveform-audio devices recognize this command.</span></span> <span data-ttu-id="14893-107">雖然數位視訊裝置和 MIDI sequencers 也會辨識此命令，但 MCIAVI 和 MCISEQ 驅動程式並不會執行此命令。</span><span class="sxs-lookup"><span data-stu-id="14893-107">Although digital-video devices and MIDI sequencers also recognize this command, the MCIAVI and MCISEQ drivers do not implement it.</span></span>

<span data-ttu-id="14893-108">若要傳送此命令，請使用下列參數呼叫 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) 函數。</span><span class="sxs-lookup"><span data-stu-id="14893-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_RECORD, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_RECORD_PARMS) lpRecord
);
```



## <a name="parameters"></a><span data-ttu-id="14893-109">參數</span><span class="sxs-lookup"><span data-stu-id="14893-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14893-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="14893-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="14893-111">要接收命令訊息之 MCI 裝置的裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="14893-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="14893-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="14893-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="14893-113">\_ \_ 針對數位-視頻和 VCR 裝置，mci 測試的 mci 通知、mci 等候或 \_ 。</span><span class="sxs-lookup"><span data-stu-id="14893-113">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video and VCR devices, MCI\_TEST.</span></span> <span data-ttu-id="14893-114">如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。</span><span class="sxs-lookup"><span data-stu-id="14893-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="14893-115"><span id="lpRecord"></span><span id="lprecord"></span><span id="LPRECORD"></span>*lpRecord*</span><span class="sxs-lookup"><span data-stu-id="14893-115"><span id="lpRecord"></span><span id="lprecord"></span><span id="LPRECORD"></span>*lpRecord*</span></span>
</dt> <dd>

<span data-ttu-id="14893-116">[**MCI \_ 記錄 \_ PARMS**](mci-record-parms.md)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="14893-116">Pointer to an [**MCI\_RECORD\_PARMS**](mci-record-parms.md) structure.</span></span> <span data-ttu-id="14893-117">具有擴充命令集的 (裝置，可能會以裝置特定結構取代此結構。 ) </span><span class="sxs-lookup"><span data-stu-id="14893-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14893-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="14893-118">Return Value</span></span>

<span data-ttu-id="14893-119">如果成功則傳回零，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="14893-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="14893-120">備註</span><span class="sxs-lookup"><span data-stu-id="14893-120">Remarks</span></span>

<span data-ttu-id="14893-121">當您使用 MCI  GETDEVCAPS 可以[ \_ ](mci-getdevcaps.md) \_ \_ \_ 記錄旗標呼叫 mci GETDEVCAPS 命令時，會傳回 TRUE 的裝置支援此命令。</span><span class="sxs-lookup"><span data-stu-id="14893-121">This command is supported by devices that return **TRUE** when you call the [MCI\_GETDEVCAPS](mci-getdevcaps.md) command with the MCI\_GETDEVCAPS\_CAN\_RECORD flag.</span></span> <span data-ttu-id="14893-122">針對 MCIWAVE 驅動程式，如果檔案已關閉而不儲存，則會捨棄檔案之後記錄的所有資料。</span><span class="sxs-lookup"><span data-stu-id="14893-122">For the MCIWAVE driver, all data recorded after a file is opened is discarded if the file is closed without saving it.</span></span>

<span data-ttu-id="14893-123">下列其他旗標適用于所有支援 MCI 記錄的裝置 \_ ：</span><span class="sxs-lookup"><span data-stu-id="14893-123">The following additional flags apply to all devices supporting MCI\_RECORD:</span></span>

<dl> <dt>

<span data-ttu-id="14893-124"><span id="MCI_FROM"></span><span id="mci_from"></span>MCI \_ 來源</span><span class="sxs-lookup"><span data-stu-id="14893-124"><span id="MCI_FROM"></span><span id="mci_from"></span>MCI\_FROM</span></span>
</dt> <dd>

<span data-ttu-id="14893-125">起始位置會包含在 *lpRecord* 所識別之結構的 **dwFrom** 成員中。</span><span class="sxs-lookup"><span data-stu-id="14893-125">A starting location is included in the **dwFrom** member of the structure identified by *lpRecord*.</span></span> <span data-ttu-id="14893-126">指派給位置值的單位，會以 Mci 設定的 \_ \_ 時間格式旗標，以 \_ [mci \_ set](mci-set.md) 命令來指定。</span><span class="sxs-lookup"><span data-stu-id="14893-126">The units assigned to the position values are specified with the MCI\_SET\_TIME\_FORMAT flag of the [MCI\_SET](mci-set.md) command.</span></span> <span data-ttu-id="14893-127">如果 \_ 未指定來自的 MCI，開始位置會預設為目前的位置。</span><span class="sxs-lookup"><span data-stu-id="14893-127">If MCI\_FROM is not specified, the starting location defaults to the current position.</span></span>

</dd> <dt>

<span data-ttu-id="14893-128"><span id="MCI_RECORD_INSERT"></span><span id="mci_record_insert"></span>MCI \_ 記錄 \_ 插入</span><span class="sxs-lookup"><span data-stu-id="14893-128"><span id="MCI_RECORD_INSERT"></span><span id="mci_record_insert"></span>MCI\_RECORD\_INSERT</span></span>
</dt> <dd>

<span data-ttu-id="14893-129">新記錄的資訊應該插入或貼到現有的資料中。</span><span class="sxs-lookup"><span data-stu-id="14893-129">Newly recorded information should be inserted or pasted into the existing data.</span></span> <span data-ttu-id="14893-130">某些裝置可能不支援這種情況。</span><span class="sxs-lookup"><span data-stu-id="14893-130">Some devices might not support this.</span></span> <span data-ttu-id="14893-131">如果支援，這是預設值。</span><span class="sxs-lookup"><span data-stu-id="14893-131">If supported, this is the default.</span></span>

</dd> <dt>

<span data-ttu-id="14893-132"><span id="MCI_RECORD_OVERWRITE"></span><span id="mci_record_overwrite"></span>MCI \_ 記錄 \_ 覆寫</span><span class="sxs-lookup"><span data-stu-id="14893-132"><span id="MCI_RECORD_OVERWRITE"></span><span id="mci_record_overwrite"></span>MCI\_RECORD\_OVERWRITE</span></span>
</dt> <dd>

<span data-ttu-id="14893-133">資料應覆寫現有的資料。</span><span class="sxs-lookup"><span data-stu-id="14893-133">Data should overwrite existing data.</span></span> <span data-ttu-id="14893-134">MCIWAVE。WINSPOOL.DRV 裝置會傳回 MCIERR \_ 不支援的函式以 \_ 回應此旗標。</span><span class="sxs-lookup"><span data-stu-id="14893-134">The MCIWAVE.DRV device returns MCIERR\_UNSUPPORTED\_FUNCTION in response to this flag.</span></span>

</dd> <dt>

<span data-ttu-id="14893-135"><span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ 至</span><span class="sxs-lookup"><span data-stu-id="14893-135"><span id="MCI_TO"></span><span id="mci_to"></span>MCI\_TO</span></span>
</dt> <dd>

<span data-ttu-id="14893-136">結束位置會包含在由 *lpRecord* 所識別之結構的 **dwTo** 成員中。</span><span class="sxs-lookup"><span data-stu-id="14893-136">An ending location is included in the **dwTo** member of the structure identified by *lpRecord*.</span></span> <span data-ttu-id="14893-137">指派給位置值的單位，會以 Mci 設定的 \_ \_ 時間格式旗標，以 \_ [mci \_ set](mci-set.md) 命令來指定。</span><span class="sxs-lookup"><span data-stu-id="14893-137">The units assigned to the position values are specified with the MCI\_SET\_TIME\_FORMAT flag of the [MCI\_SET](mci-set.md) command.</span></span> <span data-ttu-id="14893-138">如果 \_ 未指定 MCI 至，結束位置會預設為內容結尾。</span><span class="sxs-lookup"><span data-stu-id="14893-138">If MCI\_TO is not specified, the ending location defaults to the end of the content.</span></span>

</dd> </dl>

<span data-ttu-id="14893-139">下列其他旗標適用于 **digitalvideo** 裝置類型：</span><span class="sxs-lookup"><span data-stu-id="14893-139">The following additional flags are used with the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="14893-140"><span id="MCI_DGV_RECORD_AUDIO_STREAM"></span><span id="mci_dgv_record_audio_stream"></span>MCI \_ DGV \_ 錄製 \_ 音訊 \_ 串流</span><span class="sxs-lookup"><span data-stu-id="14893-140"><span id="MCI_DGV_RECORD_AUDIO_STREAM"></span><span id="mci_dgv_record_audio_stream"></span>MCI\_DGV\_RECORD\_AUDIO\_STREAM</span></span>
</dt> <dd>

<span data-ttu-id="14893-141">音訊串流號碼包含在 *lpRecord* 所識別之結構的 **dwAudioStream** 成員中。</span><span class="sxs-lookup"><span data-stu-id="14893-141">An audio-stream number is included in the **dwAudioStream** member of the structure identified by *lpRecord*.</span></span> <span data-ttu-id="14893-142">如果您省略此旗標，則會將音訊資料記錄到第一個實體資料流程中。</span><span class="sxs-lookup"><span data-stu-id="14893-142">If you omit this flag, audio data is recorded into the first physical stream.</span></span>

</dd> <dt>

<span data-ttu-id="14893-143"><span id="MCI_DGV_RECORD_HOLD"></span><span id="mci_dgv_record_hold"></span>MCI \_ DGV \_ 記錄 \_ 保存</span><span class="sxs-lookup"><span data-stu-id="14893-143"><span id="MCI_DGV_RECORD_HOLD"></span><span id="mci_dgv_record_hold"></span>MCI\_DGV\_RECORD\_HOLD</span></span>
</dt> <dd>

<span data-ttu-id="14893-144">錄製停止時，畫面將會保留最後一個影像，而且在發出 [MCI \_ 監視器](mci-monitor.md) 命令之前，將不會繼續顯示影片。</span><span class="sxs-lookup"><span data-stu-id="14893-144">When recording stops, the screen will hold the last image and will not resume showing the video until an [MCI\_MONITOR](mci-monitor.md) command is issued.</span></span>

</dd> <dt>

<span data-ttu-id="14893-145"><span id="MCI_DGV_RECORD_VIDEO_STREAM"></span><span id="mci_dgv_record_video_stream"></span>MCI \_ DGV \_ 錄製 \_ 影片 \_ 串流</span><span class="sxs-lookup"><span data-stu-id="14893-145"><span id="MCI_DGV_RECORD_VIDEO_STREAM"></span><span id="mci_dgv_record_video_stream"></span>MCI\_DGV\_RECORD\_VIDEO\_STREAM</span></span>
</dt> <dd>

<span data-ttu-id="14893-146">影片串流號碼包含在 *lpRecord* 所識別之結構的 **dwVideoStream** 成員中。</span><span class="sxs-lookup"><span data-stu-id="14893-146">A video-stream number is included in the **dwVideoStream** member of the structure identified by *lpRecord*.</span></span> <span data-ttu-id="14893-147">如果您省略此旗標，則會將影片資料記錄到第一個實體串流中。</span><span class="sxs-lookup"><span data-stu-id="14893-147">If you omit this flag, video data is recorded into the first physical stream.</span></span>

</dd> <dt>

<span data-ttu-id="14893-148"><span id="MCI_DGV_RECT"></span><span id="mci_dgv_rect"></span>MCI \_ DGV \_ RECT</span><span class="sxs-lookup"><span data-stu-id="14893-148"><span id="MCI_DGV_RECT"></span><span id="mci_dgv_rect"></span>MCI\_DGV\_RECT</span></span>
</dt> <dd>

<span data-ttu-id="14893-149">在 *lpRecord* 所識別之結構的 **rc** 成員中指定矩形。</span><span class="sxs-lookup"><span data-stu-id="14893-149">A rectangle is specified in the **rc** member of the structure identified by *lpRecord*.</span></span> <span data-ttu-id="14893-150">矩形會指定外部輸入的區域，做為壓縮和儲存的圖元來源。</span><span class="sxs-lookup"><span data-stu-id="14893-150">The rectangle specifies the region of the external input used as the source for the pixels compressed and saved.</span></span> <span data-ttu-id="14893-151">這個矩形預設為 DGV 所指定的矩形 (或預設) 由 mci \_ put 命令的 mci \_ PUT \_ 影片旗標。 [ \_ ](mci-put.md)</span><span class="sxs-lookup"><span data-stu-id="14893-151">This rectangle defaults to the rectangle specified (or defaulted) by the MCI\_DGV\_PUT\_VIDEO flag for the [MCI\_PUT](mci-put.md) command.</span></span> <span data-ttu-id="14893-152">當其設定方式不同于影片矩形時，顯示的內容不是錄製的內容</span><span class="sxs-lookup"><span data-stu-id="14893-152">When it is set differently than the video rectangle, what is displayed is not what is recorded</span></span>

</dd> </dl>

<span data-ttu-id="14893-153">針對數位影片裝置， *lpRecord* 會指向 [**MCI \_ DGV \_ 記錄 \_ PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_record_parms) 結構。</span><span class="sxs-lookup"><span data-stu-id="14893-153">For digital-video devices, *lpRecord* points to an [**MCI\_DGV\_RECORD\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_record_parms) structure.</span></span>

<span data-ttu-id="14893-154">下列其他旗標適用于 **vcr** 裝置類型：</span><span class="sxs-lookup"><span data-stu-id="14893-154">The following additional flags are used with the **vcr** device type:</span></span>

<dl> <dt>

<span data-ttu-id="14893-155"><span id="MCI_VCR_RECORD_AT"></span><span id="mci_vcr_record_at"></span>MCI \_ VCR \_ 記錄 \_ 于</span><span class="sxs-lookup"><span data-stu-id="14893-155"><span id="MCI_VCR_RECORD_AT"></span><span id="mci_vcr_record_at"></span>MCI\_VCR\_RECORD\_AT</span></span>
</dt> <dd>

<span data-ttu-id="14893-156">*LpRecord* 所識別之結構的 **dwAt** 成員，包含整個命令開始的時間，或如果裝置是 cued，則會在裝置到達提示命令所提供的位置時。</span><span class="sxs-lookup"><span data-stu-id="14893-156">The **dwAt** member of the structure identified by *lpRecord* contains a time when the entire command begins, or if the device is cued, when the device reaches the from position given by the cue command.</span></span>

</dd> <dt>

<span data-ttu-id="14893-157"><span id="MCI_VCR_RECORD_INITIALIZE"></span><span id="mci_vcr_record_initialize"></span>MCI \_ VCR \_ 記錄 \_ 初始化</span><span class="sxs-lookup"><span data-stu-id="14893-157"><span id="MCI_VCR_RECORD_INITIALIZE"></span><span id="mci_vcr_record_initialize"></span>MCI\_VCR\_RECORD\_INITIALIZE</span></span>
</dt> <dd>

<span data-ttu-id="14893-158">將裝置搜尋至媒體的開頭，開始錄製空白的影片和音訊，以及記錄時間碼（如果可能的話）。</span><span class="sxs-lookup"><span data-stu-id="14893-158">Seek the device to the start of the media, begin recording blank video and audio, and record timecode, if possible.</span></span>

</dd> </dl>

<span data-ttu-id="14893-159">若為 VCR 裝置， *lpRecord* 會指向 [**MCI \_ VCR \_ 記錄 \_ PARMS**](mci-vcr-record-parms.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="14893-159">For VCR devices, *lpRecord* points to an [**MCI\_VCR\_RECORD\_PARMS**](mci-vcr-record-parms.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="14893-160">規格需求</span><span class="sxs-lookup"><span data-stu-id="14893-160">Requirements</span></span>



| <span data-ttu-id="14893-161">需求</span><span class="sxs-lookup"><span data-stu-id="14893-161">Requirement</span></span> | <span data-ttu-id="14893-162">值</span><span class="sxs-lookup"><span data-stu-id="14893-162">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14893-163">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="14893-163">Minimum supported client</span></span><br/> | <span data-ttu-id="14893-164">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="14893-164">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="14893-165">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="14893-165">Minimum supported server</span></span><br/> | <span data-ttu-id="14893-166">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="14893-166">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="14893-167">標頭</span><span class="sxs-lookup"><span data-stu-id="14893-167">Header</span></span><br/>                   | <dl> <span data-ttu-id="14893-168"><dt>Mmsystem (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="14893-168"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14893-169">另請參閱</span><span class="sxs-lookup"><span data-stu-id="14893-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14893-170">Mci</span><span class="sxs-lookup"><span data-stu-id="14893-170">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="14893-171">MCI 命令</span><span class="sxs-lookup"><span data-stu-id="14893-171">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

