---
title: 'MCI_CUE 命令 (Mmsystem .h) '
description: MCI \_ 提示命令會提示裝置，以便從最小延遲開始播放或錄製。 數位-影片、VCR 和波形-音訊裝置會辨識此命令。
ms.assetid: 22da4a84-a7af-42df-b950-8d1184fff9ba
keywords:
- MCI_CUE 命令 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_CUE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec8463c68f304fe216049568e0df518cbe1d0090
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967985"
---
# <a name="mci_cue-command"></a><span data-ttu-id="e4b13-105">MCI \_ 提示命令</span><span class="sxs-lookup"><span data-stu-id="e4b13-105">MCI\_CUE command</span></span>

<span data-ttu-id="e4b13-106">MCI \_ 提示命令會提示裝置，以便從最小延遲開始播放或錄製。</span><span class="sxs-lookup"><span data-stu-id="e4b13-106">The MCI\_CUE command cues a device so that playback or recording begins with minimum delay.</span></span> <span data-ttu-id="e4b13-107">數位-影片、VCR 和波形-音訊裝置會辨識此命令。</span><span class="sxs-lookup"><span data-stu-id="e4b13-107">Digital-video, VCR, and waveform-audio devices recognize this command.</span></span>

<span data-ttu-id="e4b13-108">若要傳送此命令，請使用下列參數呼叫 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) 函數。</span><span class="sxs-lookup"><span data-stu-id="e4b13-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_CUE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpCue
);
```



## <a name="parameters"></a><span data-ttu-id="e4b13-109">參數</span><span class="sxs-lookup"><span data-stu-id="e4b13-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4b13-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="e4b13-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="e4b13-111">要接收命令訊息之 MCI 裝置的裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="e4b13-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="e4b13-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="e4b13-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="e4b13-113">\_ \_ 針對數位-視頻和 VCR 裝置，mci 測試的 mci 通知、mci 等候或 \_ 。</span><span class="sxs-lookup"><span data-stu-id="e4b13-113">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video and VCR devices, MCI\_TEST.</span></span> <span data-ttu-id="e4b13-114">如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。</span><span class="sxs-lookup"><span data-stu-id="e4b13-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="e4b13-115"><span id="lpCue"></span><span id="lpcue"></span><span id="LPCUE"></span>*lpCue*</span><span class="sxs-lookup"><span data-stu-id="e4b13-115"><span id="lpCue"></span><span id="lpcue"></span><span id="LPCUE"></span>*lpCue*</span></span>
</dt> <dd>

<span data-ttu-id="e4b13-116">[**MCI \_ 泛型 \_ PARMS**](mci-generic-parms.md)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="e4b13-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="e4b13-117">具有擴充命令集的 (裝置，可能會以裝置特定結構取代此結構。 ) </span><span class="sxs-lookup"><span data-stu-id="e4b13-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4b13-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="e4b13-118">Return Value</span></span>

<span data-ttu-id="e4b13-119">如果成功則傳回零，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="e4b13-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="e4b13-120">備註</span><span class="sxs-lookup"><span data-stu-id="e4b13-120">Remarks</span></span>

<span data-ttu-id="e4b13-121">下列其他旗標適用于 **digitalvideo** 裝置類型：</span><span class="sxs-lookup"><span data-stu-id="e4b13-121">The following additional flags are used with the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="e4b13-122"><span id="MCI_DGV_CUE_INPUT"></span><span id="mci_dgv_cue_input"></span>MCI \_ DGV \_ 提示 \_ 輸入</span><span class="sxs-lookup"><span data-stu-id="e4b13-122"><span id="MCI_DGV_CUE_INPUT"></span><span id="mci_dgv_cue_input"></span>MCI\_DGV\_CUE\_INPUT</span></span>
</dt> <dd>

<span data-ttu-id="e4b13-123">數位影片實例應準備進行錄製。</span><span class="sxs-lookup"><span data-stu-id="e4b13-123">A digital-video instance should prepare for recording.</span></span> <span data-ttu-id="e4b13-124">如果應用程式未保留磁碟空間，則裝置會使用其預設參數保留磁碟空間。</span><span class="sxs-lookup"><span data-stu-id="e4b13-124">If the application has not reserved disk space, the device reserves the disk space using its default parameters.</span></span> <span data-ttu-id="e4b13-125">如果目前的簡報來源已經是外部輸入，應用程式可以省略此旗標。</span><span class="sxs-lookup"><span data-stu-id="e4b13-125">The application can omit this flag if the current presentation source is already the external input.</span></span> <span data-ttu-id="e4b13-126"> (此旗標不會影響選取展示來源。 ) </span><span class="sxs-lookup"><span data-stu-id="e4b13-126">(This flag has no effect on selecting the presentation source.)</span></span>

</dd> <dt>

<span data-ttu-id="e4b13-127"><span id="MCI_DGV_CUE_NOSHOW"></span><span id="mci_dgv_cue_noshow"></span>MCI \_ DGV \_ 提示 \_ NOSHOW</span><span class="sxs-lookup"><span data-stu-id="e4b13-127"><span id="MCI_DGV_CUE_NOSHOW"></span><span id="mci_dgv_cue_noshow"></span>MCI\_DGV\_CUE\_NOSHOW</span></span>
</dt> <dd>

<span data-ttu-id="e4b13-128">數位影片實例應該準備好播放使用命令指定的框架，而不顯示它。</span><span class="sxs-lookup"><span data-stu-id="e4b13-128">A digital-video instance should prepare for playing the frame specified with the command without displaying it.</span></span> <span data-ttu-id="e4b13-129">當指定這個旗標時，即使對應的框架不是目前的位置，顯示器仍會繼續在框架緩衝區中顯示影像。</span><span class="sxs-lookup"><span data-stu-id="e4b13-129">When this flag is specified, the display continues to show the image in the frame buffer even though its corresponding frame is not the current position.</span></span> <span data-ttu-id="e4b13-130">例如，如果框架緩衝區包含來自框架7的影像，則當使用此旗標將裝置提示至任何其他位置時，裝置會繼續顯示框架7。</span><span class="sxs-lookup"><span data-stu-id="e4b13-130">For example, if the frame buffer contains the image from frame 7, the device continues to show frame 7 when this flag is used to cue the device to any other position.</span></span> <span data-ttu-id="e4b13-131">未使用此旗標且不含 MCI 旗標的後續提示命令會 \_ 顯示目前的畫面格。</span><span class="sxs-lookup"><span data-stu-id="e4b13-131">A subsequent cue command without this flag and without the MCI\_TO flag displays the current frame.</span></span>

</dd> <dt>

<span data-ttu-id="e4b13-132"><span id="MCI_DGV_CUE_OUTPUT"></span><span id="mci_dgv_cue_output"></span>MCI \_ DGV \_ 提示 \_ 輸出</span><span class="sxs-lookup"><span data-stu-id="e4b13-132"><span id="MCI_DGV_CUE_OUTPUT"></span><span id="mci_dgv_cue_output"></span>MCI\_DGV\_CUE\_OUTPUT</span></span>
</dt> <dd>

<span data-ttu-id="e4b13-133">數位影片實例應該準備好進行播放。</span><span class="sxs-lookup"><span data-stu-id="e4b13-133">A digital-video instance should prepare for playing.</span></span> <span data-ttu-id="e4b13-134">如果工作區暫停，則不會發生定位。</span><span class="sxs-lookup"><span data-stu-id="e4b13-134">If the workspace is paused, no positioning occurs.</span></span> <span data-ttu-id="e4b13-135">如果工作區已停止，此位置可能會變更為先前的主要畫面格影像。</span><span class="sxs-lookup"><span data-stu-id="e4b13-135">If the workspace is stopped, the position might change to a previous key-frame image.</span></span> <span data-ttu-id="e4b13-136">如果目前的簡報來源已經是工作區，應用程式可以省略此旗標。</span><span class="sxs-lookup"><span data-stu-id="e4b13-136">The application can omit this flag if the current presentation source is already the workspace.</span></span>

</dd> <dt>

<span data-ttu-id="e4b13-137"><span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ 至</span><span class="sxs-lookup"><span data-stu-id="e4b13-137"><span id="MCI_TO"></span><span id="mci_to"></span>MCI\_TO</span></span>
</dt> <dd>

<span data-ttu-id="e4b13-138">工作區位置會包含在 *lpCue* 所識別之結構的 **dwTo** 成員中。</span><span class="sxs-lookup"><span data-stu-id="e4b13-138">A workspace position is included in the **dwTo** member of the structure identified by *lpCue*.</span></span> <span data-ttu-id="e4b13-139">指派給位置值的單位會使用 \_ \_ mci set 命令的 mci set TIME \_ FORMAT 旗 [ \_ ](mci-set.md) 標來指定。</span><span class="sxs-lookup"><span data-stu-id="e4b13-139">The units assigned to position values are specified using the MCI\_SET\_TIME\_FORMAT flag of the [MCI\_SET](mci-set.md) command.</span></span> <span data-ttu-id="e4b13-140">這相當於搜尋位置，但裝置會在命令之後暫停。</span><span class="sxs-lookup"><span data-stu-id="e4b13-140">This is equivalent to seeking to a position, except the device is paused after the command.</span></span>

</dd> </dl>

<span data-ttu-id="e4b13-141">針對 **digitalvideo** 裝置， *lpCue* 參數會指向 [**MCI \_ DGV \_ 提示 \_ PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_cue_parms) 結構。</span><span class="sxs-lookup"><span data-stu-id="e4b13-141">For **digitalvideo** devices, the *lpCue* parameter points to an [**MCI\_DGV\_CUE\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_cue_parms) structure.</span></span>

<span data-ttu-id="e4b13-142">下列其他旗標適用于 **vcr** 裝置類型：</span><span class="sxs-lookup"><span data-stu-id="e4b13-142">The following additional flags are used with the **vcr** device type:</span></span>

<dl> <dt>

<span data-ttu-id="e4b13-143"><span id="MCI_FROM"></span><span id="mci_from"></span>MCI \_ 來源</span><span class="sxs-lookup"><span data-stu-id="e4b13-143"><span id="MCI_FROM"></span><span id="mci_from"></span>MCI\_FROM</span></span>
</dt> <dd>

<span data-ttu-id="e4b13-144">*LpCue* 所指向結構的 **dwFrom** 成員包含以目前時間格式指定的起始位置。</span><span class="sxs-lookup"><span data-stu-id="e4b13-144">The **dwFrom** member of the structure pointed to by *lpCue* contains the starting location specified in the current time format.</span></span>

</dd> <dt>

<span data-ttu-id="e4b13-145"><span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ 至</span><span class="sxs-lookup"><span data-stu-id="e4b13-145"><span id="MCI_TO"></span><span id="mci_to"></span>MCI\_TO</span></span>
</dt> <dd>

<span data-ttu-id="e4b13-146">*LpCue* 所指向之結構的 **dwTo** 成員包含結束 (目前時間格式所指定的) 位置。</span><span class="sxs-lookup"><span data-stu-id="e4b13-146">The **dwTo** member of the structure pointed to by *lpCue* contains the ending (pausing) location specified in the current time format.</span></span>

</dd> <dt>

<span data-ttu-id="e4b13-147"><span id="MCI_VCR_CUE_INPUT"></span><span id="mci_vcr_cue_input"></span>MCI \_ VCR \_ 提示 \_ 輸入</span><span class="sxs-lookup"><span data-stu-id="e4b13-147"><span id="MCI_VCR_CUE_INPUT"></span><span id="mci_vcr_cue_input"></span>MCI\_VCR\_CUE\_INPUT</span></span>
</dt> <dd>

<span data-ttu-id="e4b13-148">準備錄製。</span><span class="sxs-lookup"><span data-stu-id="e4b13-148">Prepare for recording.</span></span>

</dd> <dt>

<span data-ttu-id="e4b13-149"><span id="MCI_VCR_CUE_OUTPUT"></span><span id="mci_vcr_cue_output"></span>MCI \_ VCR \_ 提示 \_ 輸出</span><span class="sxs-lookup"><span data-stu-id="e4b13-149"><span id="MCI_VCR_CUE_OUTPUT"></span><span id="mci_vcr_cue_output"></span>MCI\_VCR\_CUE\_OUTPUT</span></span>
</dt> <dd>

<span data-ttu-id="e4b13-150">準備進行播放。</span><span class="sxs-lookup"><span data-stu-id="e4b13-150">Prepare for playing.</span></span> <span data-ttu-id="e4b13-151">如果沒有 \_ 指定 mci vcr \_ 提示 \_ 輸入或 mci \_ vcr \_ 提示 \_ 輸出， \_ \_ \_ 則會假設為 mci vcr 提示輸出。</span><span class="sxs-lookup"><span data-stu-id="e4b13-151">If neither MCI\_VCR\_CUE\_INPUT nor MCI\_VCR\_CUE\_OUTPUT is specified, MCI\_VCR\_CUE\_OUTPUT is assumed.</span></span>

</dd> <dt>

<span data-ttu-id="e4b13-152"><span id="MCI_VCR_CUE_PREROLL"></span><span id="mci_vcr_cue_preroll"></span>MCI \_ VCR \_ 提示預先進行 \_</span><span class="sxs-lookup"><span data-stu-id="e4b13-152"><span id="MCI_VCR_CUE_PREROLL"></span><span id="mci_vcr_cue_preroll"></span>MCI\_VCR\_CUE\_PREROLL</span></span>
</dt> <dd>

<span data-ttu-id="e4b13-153">將裝置提示至目前的位置或 **dwFrom** 位置，減去預先進行的持續時間。</span><span class="sxs-lookup"><span data-stu-id="e4b13-153">Cue the device to the current position, or the **dwFrom** position, minus the preroll duration.</span></span> <span data-ttu-id="e4b13-154">這可讓裝置在進入錄製或播放模式之前做好準備。</span><span class="sxs-lookup"><span data-stu-id="e4b13-154">This will allow the device to prepare itself before entering record or playback mode.</span></span>

</dd> <dt>

<span data-ttu-id="e4b13-155"><span id="MCI_VCR_CUE_REVERSE"></span><span id="mci_vcr_cue_reverse"></span>MCI \_ VCR \_ 提示 \_ 反向</span><span class="sxs-lookup"><span data-stu-id="e4b13-155"><span id="MCI_VCR_CUE_REVERSE"></span><span id="mci_vcr_cue_reverse"></span>MCI\_VCR\_CUE\_REVERSE</span></span>
</dt> <dd>

<span data-ttu-id="e4b13-156">下一個 play 或 record 命令的方向相反。</span><span class="sxs-lookup"><span data-stu-id="e4b13-156">The direction of the next play or record command is reverse.</span></span>

</dd> </dl>

<span data-ttu-id="e4b13-157">使用 mci \_ 提示命令搭配 mci vcr 提示輸出旗標來提示播放時 \_ \_ \_ ，您可以藉 \_ 由從、mci [ \_ ](mci-play.md) \_ \_ TO 或 mci \_ VCR \_ 播放的 mci 發出 mci play 命令，來取消 mci 提示 \_ 。</span><span class="sxs-lookup"><span data-stu-id="e4b13-157">When cueing for playback by using the MCI\_CUE command with the MCI\_VCR\_CUE\_OUTPUT flag, you can cancel MCI\_CUE by issuing the [MCI\_PLAY](mci-play.md) command with MCI\_FROM, MCI\_TO, or MCI\_VCR\_PLAY\_REVERSE.</span></span>

<span data-ttu-id="e4b13-158">使用 mci vcr 提示輸入旗標來提示記錄時 \_ \_ \_ \_ ，您可以藉 \_ 由發出 mci [ \_ 記錄](mci-record.md) 命令與 mci \_ 、mci \_ TO 或 mci \_ vcr \_ 記錄 \_ 初始化，來取消 mci 提示。</span><span class="sxs-lookup"><span data-stu-id="e4b13-158">When cueing for recording by using MCI\_CUE with the MCI\_VCR\_CUE\_INPUT flag, you can cancel MCI\_CUE by issuing the [MCI\_RECORD](mci-record.md) command with MCI\_FROM, MCI\_TO, or MCI\_VCR\_RECORD\_INITIALIZE.</span></span>

<span data-ttu-id="e4b13-159">若為 **vcr** 裝置， *lpCue* 參數會指向 [**MCI \_ vcr \_ 提示 \_ PARMS**](mci-vcr-cue-parms.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="e4b13-159">For **vcr** devices, the *lpCue* parameter points to an [**MCI\_VCR\_CUE\_PARMS**](mci-vcr-cue-parms.md) structure.</span></span>

<span data-ttu-id="e4b13-160">下列其他旗標適用于 **waveaudio** 裝置類型：</span><span class="sxs-lookup"><span data-stu-id="e4b13-160">The following additional flags are used with the **waveaudio** device type:</span></span>

<dl> <dt>

<span data-ttu-id="e4b13-161"><span id="MCI_WAVE_INPUT"></span><span id="mci_wave_input"></span>MCI \_ WAVE \_ 輸入</span><span class="sxs-lookup"><span data-stu-id="e4b13-161"><span id="MCI_WAVE_INPUT"></span><span id="mci_wave_input"></span>MCI\_WAVE\_INPUT</span></span>
</dt> <dd>

<span data-ttu-id="e4b13-162">波形音訊輸入裝置應 cued。</span><span class="sxs-lookup"><span data-stu-id="e4b13-162">A waveform-audio input device should be cued.</span></span>

</dd> <dt>

<span data-ttu-id="e4b13-163"><span id="MCI_WAVE_OUTPUT"></span><span id="mci_wave_output"></span>MCI \_ WAVE \_ 輸出</span><span class="sxs-lookup"><span data-stu-id="e4b13-163"><span id="MCI_WAVE_OUTPUT"></span><span id="mci_wave_output"></span>MCI\_WAVE\_OUTPUT</span></span>
</dt> <dd>

<span data-ttu-id="e4b13-164">波形音訊輸出裝置應 cued。</span><span class="sxs-lookup"><span data-stu-id="e4b13-164">A waveform-audio output device should be cued.</span></span> <span data-ttu-id="e4b13-165">如果未指定旗標，這會是預設旗標。</span><span class="sxs-lookup"><span data-stu-id="e4b13-165">This is the default flag if a flag is not specified.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e4b13-166">規格需求</span><span class="sxs-lookup"><span data-stu-id="e4b13-166">Requirements</span></span>



| <span data-ttu-id="e4b13-167">需求</span><span class="sxs-lookup"><span data-stu-id="e4b13-167">Requirement</span></span> | <span data-ttu-id="e4b13-168">值</span><span class="sxs-lookup"><span data-stu-id="e4b13-168">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4b13-169">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e4b13-169">Minimum supported client</span></span><br/> | <span data-ttu-id="e4b13-170">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e4b13-170">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="e4b13-171">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e4b13-171">Minimum supported server</span></span><br/> | <span data-ttu-id="e4b13-172">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e4b13-172">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="e4b13-173">標頭</span><span class="sxs-lookup"><span data-stu-id="e4b13-173">Header</span></span><br/>                   | <dl> <span data-ttu-id="e4b13-174"><dt>Mmsystem (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="e4b13-174"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4b13-175">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e4b13-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4b13-176">Mci</span><span class="sxs-lookup"><span data-stu-id="e4b13-176">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="e4b13-177">MCI 命令</span><span class="sxs-lookup"><span data-stu-id="e4b13-177">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

