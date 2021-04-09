---
title: 'MCI_PLAY 命令 (Mmsystem .h) '
description: MCI \_ PLAY 命令會指示裝置開始傳輸輸出資料。 CD 音訊、數位影片、MIDI sequencer、videodisc、VCR 和波形音訊裝置都會辨識此命令。
ms.assetid: d912ab49-63f0-40a9-aa4c-f9463782b54c
keywords:
- MCI_PLAY 命令 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_PLAY
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f985a8d5d6be7ad42702afc898b3aaf437ef320
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844404"
---
# <a name="mci_play-command"></a><span data-ttu-id="13913-105">MCI \_ PLAY 命令</span><span class="sxs-lookup"><span data-stu-id="13913-105">MCI\_PLAY command</span></span>

<span data-ttu-id="13913-106">MCI \_ PLAY 命令會指示裝置開始傳輸輸出資料。</span><span class="sxs-lookup"><span data-stu-id="13913-106">The MCI\_PLAY command signals the device to begin transmitting output data.</span></span> <span data-ttu-id="13913-107">CD 音訊、數位影片、MIDI sequencer、videodisc、VCR 和波形音訊裝置都會辨識此命令。</span><span class="sxs-lookup"><span data-stu-id="13913-107">CD audio, digital-video, MIDI sequencer, videodisc, VCR, and waveform-audio devices recognize this command.</span></span>

<span data-ttu-id="13913-108">若要傳送此命令，請使用下列參數呼叫 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) 函數。</span><span class="sxs-lookup"><span data-stu-id="13913-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_PLAY, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_PLAY_PARMS ) lpPlay
);
```



## <a name="parameters"></a><span data-ttu-id="13913-109">參數</span><span class="sxs-lookup"><span data-stu-id="13913-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13913-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="13913-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="13913-111">要接收命令訊息之 MCI 裝置的裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="13913-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="13913-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="13913-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="13913-113">\_ \_ 針對數位-視頻和 VCR 裝置，mci 測試的 mci 通知、mci 等候或 \_ 。</span><span class="sxs-lookup"><span data-stu-id="13913-113">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video and VCR devices, MCI\_TEST.</span></span> <span data-ttu-id="13913-114">如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。</span><span class="sxs-lookup"><span data-stu-id="13913-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="13913-115"><span id="lpPlay"></span><span id="lpplay"></span><span id="LPPLAY"></span>*lpPlay*</span><span class="sxs-lookup"><span data-stu-id="13913-115"><span id="lpPlay"></span><span id="lpplay"></span><span id="LPPLAY"></span>*lpPlay*</span></span>
</dt> <dd>

<span data-ttu-id="13913-116">[**MCI \_ 播放 \_ PARMS**](mci-play-parms.md)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="13913-116">Pointer to an [**MCI\_PLAY\_PARMS**](mci-play-parms.md) structure.</span></span> <span data-ttu-id="13913-117">具有擴充命令集的 (裝置，可能會以裝置特定結構取代此結構。 ) </span><span class="sxs-lookup"><span data-stu-id="13913-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13913-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="13913-118">Return Value</span></span>

<span data-ttu-id="13913-119">如果成功則傳回零，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="13913-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="13913-120">備註</span><span class="sxs-lookup"><span data-stu-id="13913-120">Remarks</span></span>

<span data-ttu-id="13913-121">下列其他旗標適用于所有支援 MCI PLAY 的裝置 \_ ：</span><span class="sxs-lookup"><span data-stu-id="13913-121">The following additional flags apply to all devices supporting MCI\_PLAY:</span></span>

<dl> <dt>

<span data-ttu-id="13913-122"><span id="MCI_FROM"></span><span id="mci_from"></span>MCI \_ 來源</span><span class="sxs-lookup"><span data-stu-id="13913-122"><span id="MCI_FROM"></span><span id="mci_from"></span>MCI\_FROM</span></span>
</dt> <dd>

<span data-ttu-id="13913-123">起始位置會包含在 *lpPlay* 所識別之結構的 **dwFrom** 成員中。</span><span class="sxs-lookup"><span data-stu-id="13913-123">A starting location is included in the **dwFrom** member of the structure identified by *lpPlay*.</span></span> <span data-ttu-id="13913-124">指派給位置值的單位，會以 Mci 設定的 \_ \_ 時間格式旗標，以 \_ [mci \_ set](mci-set.md) 命令來指定。</span><span class="sxs-lookup"><span data-stu-id="13913-124">The units assigned to the position values are specified with the MCI\_SET\_TIME\_FORMAT flag of the [MCI\_SET](mci-set.md) command.</span></span> <span data-ttu-id="13913-125">如果 \_ 未指定來自的 MCI，開始位置會預設為目前的位置。</span><span class="sxs-lookup"><span data-stu-id="13913-125">If MCI\_FROM is not specified, the starting location defaults to the current position.</span></span>

</dd> <dt>

<span data-ttu-id="13913-126"><span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ 至</span><span class="sxs-lookup"><span data-stu-id="13913-126"><span id="MCI_TO"></span><span id="mci_to"></span>MCI\_TO</span></span>
</dt> <dd>

<span data-ttu-id="13913-127">結束位置會包含在由 *lpPlay* 所識別之結構的 **dwTo** 成員中。</span><span class="sxs-lookup"><span data-stu-id="13913-127">An ending location is included in the **dwTo** member of the structure identified by *lpPlay*.</span></span> <span data-ttu-id="13913-128">指派給位置值的單位是使用 mci \_ set \_ TIME \_ FORMAT 旗標來指定 \_ 。</span><span class="sxs-lookup"><span data-stu-id="13913-128">The units assigned to the position values are specified with the MCI\_SET\_TIME\_FORMAT flag of MCI\_SET.</span></span> <span data-ttu-id="13913-129">如果 \_ 未指定 MCI 至，結束位置會預設為媒體的結尾。</span><span class="sxs-lookup"><span data-stu-id="13913-129">If MCI\_TO is not specified, the ending location defaults to the end of the media.</span></span>

</dd> </dl>

<span data-ttu-id="13913-130">下列其他旗標適用于 **digitalvideo** 裝置類型：</span><span class="sxs-lookup"><span data-stu-id="13913-130">The following additional flags are used with the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="13913-131"><span id="MCI_DGV_PLAY_REPEAT"></span><span id="mci_dgv_play_repeat"></span>MCI \_ DGV \_ 播放 \_ 重複</span><span class="sxs-lookup"><span data-stu-id="13913-131"><span id="MCI_DGV_PLAY_REPEAT"></span><span id="mci_dgv_play_repeat"></span>MCI\_DGV\_PLAY\_REPEAT</span></span>
</dt> <dd>

<span data-ttu-id="13913-132">當到達內容的結尾時，播放應該會一開始重新開機。</span><span class="sxs-lookup"><span data-stu-id="13913-132">Playback should start again at the beginning when the end of the content is reached.</span></span>

</dd> <dt>

<span data-ttu-id="13913-133"><span id="MCI_DGV_PLAY_REVERSE"></span><span id="mci_dgv_play_reverse"></span>MCI \_ DGV \_ 播放 \_ 反向</span><span class="sxs-lookup"><span data-stu-id="13913-133"><span id="MCI_DGV_PLAY_REVERSE"></span><span id="mci_dgv_play_reverse"></span>MCI\_DGV\_PLAY\_REVERSE</span></span>
</dt> <dd>

<span data-ttu-id="13913-134">播放應以相反的方式進行。</span><span class="sxs-lookup"><span data-stu-id="13913-134">Playback should occur in reverse.</span></span>

</dd> <dt>

<span data-ttu-id="13913-135"><span id="MCI_MCIAVI_PLAY_WINDOW"></span><span id="mci_mciavi_play_window"></span>MCI \_ MCIAVI \_ 播放 \_ 視窗</span><span class="sxs-lookup"><span data-stu-id="13913-135"><span id="MCI_MCIAVI_PLAY_WINDOW"></span><span id="mci_mciavi_play_window"></span>MCI\_MCIAVI\_PLAY\_WINDOW</span></span>
</dt> <dd>

<span data-ttu-id="13913-136">在 (預設) 的裝置實例相關聯的視窗中，應該會進行播放。</span><span class="sxs-lookup"><span data-stu-id="13913-136">Playback should occur in the window associated with a device instance (the default).</span></span> <span data-ttu-id="13913-137"> (此旗標適用于 MCIAVI。WINSPOOL.DRV。 ) </span><span class="sxs-lookup"><span data-stu-id="13913-137">(This flag is specific to MCIAVI.DRV.)</span></span>

</dd> <dt>

<span data-ttu-id="13913-138"><span id="MCI_MCIAVI_PLAY_FULLSCREEN"></span><span id="mci_mciavi_play_fullscreen"></span>MCI \_ MCIAVI \_ \_ 全螢幕播放</span><span class="sxs-lookup"><span data-stu-id="13913-138"><span id="MCI_MCIAVI_PLAY_FULLSCREEN"></span><span id="mci_mciavi_play_fullscreen"></span>MCI\_MCIAVI\_PLAY\_FULLSCREEN</span></span>
</dt> <dd>

<span data-ttu-id="13913-139">播放應使用全螢幕顯示。</span><span class="sxs-lookup"><span data-stu-id="13913-139">Playback should use a full-screen display.</span></span> <span data-ttu-id="13913-140">只有在播放壓縮或8位檔案時，才使用此旗標。</span><span class="sxs-lookup"><span data-stu-id="13913-140">Use this flag only when playing compressed or 8-bit files.</span></span>

</dd> </dl>

<span data-ttu-id="13913-141">針對數位影片裝置， *lpPlay* 會指向 [**MCI \_ DGV \_ PLAY \_ PARMS**](/previous-versions//dd743396(v=vs.85)) 結構。</span><span class="sxs-lookup"><span data-stu-id="13913-141">For digital-video devices, *lpPlay* points to an [**MCI\_DGV\_PLAY\_PARMS**](/previous-versions//dd743396(v=vs.85)) structure.</span></span>

<span data-ttu-id="13913-142">下列其他旗標適用于 **vcr** 裝置類型：</span><span class="sxs-lookup"><span data-stu-id="13913-142">The following additional flags are used with the **vcr** device type:</span></span>

<dl> <dt>

<span data-ttu-id="13913-143"><span id="MCI_VCR_PLAY_AT"></span><span id="mci_vcr_play_at"></span>MCI \_ VCR \_ \_ 的播放位置</span><span class="sxs-lookup"><span data-stu-id="13913-143"><span id="MCI_VCR_PLAY_AT"></span><span id="mci_vcr_play_at"></span>MCI\_VCR\_PLAY\_AT</span></span>
</dt> <dd>

<span data-ttu-id="13913-144">*LpPlay* 所識別之結構的 **dwAt** 成員，包含整個命令開始的時間，或如果裝置是 cued，則在裝置到達 [MCI \_ 提示](mci-cue.md)命令所提供的 from 位置時。</span><span class="sxs-lookup"><span data-stu-id="13913-144">The **dwAt** member of the structure identified by *lpPlay* contains a time when the entire command begins, or if the device is cued, when the device reaches the from position given by the [MCI\_CUE](mci-cue.md) command.</span></span>

</dd> <dt>

<span data-ttu-id="13913-145"><span id="MCI_VCR_PLAY_REVERSE"></span><span id="mci_vcr_play_reverse"></span>MCI \_ VCR \_ \_ 反向播放</span><span class="sxs-lookup"><span data-stu-id="13913-145"><span id="MCI_VCR_PLAY_REVERSE"></span><span id="mci_vcr_play_reverse"></span>MCI\_VCR\_PLAY\_REVERSE</span></span>
</dt> <dd>

<span data-ttu-id="13913-146">播放應以相反的方式進行。</span><span class="sxs-lookup"><span data-stu-id="13913-146">Playback should occur in reverse.</span></span>

</dd> <dt>

<span data-ttu-id="13913-147"><span id="MCI_VCR_PLAY_SCAN"></span><span id="mci_vcr_play_scan"></span>MCI \_ VCR \_ 播放 \_ 掃描</span><span class="sxs-lookup"><span data-stu-id="13913-147"><span id="MCI_VCR_PLAY_SCAN"></span><span id="mci_vcr_play_scan"></span>MCI\_VCR\_PLAY\_SCAN</span></span>
</dt> <dd>

<span data-ttu-id="13913-148">在維護影片輸出時，播放應該盡可能快越好。</span><span class="sxs-lookup"><span data-stu-id="13913-148">Playback should be as fast as possible while maintaining video output.</span></span>

</dd> </dl>

<span data-ttu-id="13913-149">若為 VCR 裝置， *lpPlay* 會指向 [**MCI \_ VCR \_ 播放 \_ PARMS**](mci-vcr-play-parms.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="13913-149">For VCR devices, *lpPlay* points to an [**MCI\_VCR\_PLAY\_PARMS**](mci-vcr-play-parms.md) structure.</span></span>

<span data-ttu-id="13913-150">下列其他旗標適用于 **videodisc** 裝置類型：</span><span class="sxs-lookup"><span data-stu-id="13913-150">The following additional flags are used with the **videodisc** device type:</span></span>

<dl> <dt>

<span data-ttu-id="13913-151"><span id="MCI_VD_PLAY_FAST"></span><span id="mci_vd_play_fast"></span>MCI \_ VD \_ \_ 快速播放</span><span class="sxs-lookup"><span data-stu-id="13913-151"><span id="MCI_VD_PLAY_FAST"></span><span id="mci_vd_play_fast"></span>MCI\_VD\_PLAY\_FAST</span></span>
</dt> <dd>

<span data-ttu-id="13913-152">快速播放。</span><span class="sxs-lookup"><span data-stu-id="13913-152">Play fast.</span></span>

</dd> <dt>

<span data-ttu-id="13913-153"><span id="MCI_VD_PLAY_REVERSE"></span><span id="mci_vd_play_reverse"></span>MCI \_ VD \_ 播放 \_ 反向</span><span class="sxs-lookup"><span data-stu-id="13913-153"><span id="MCI_VD_PLAY_REVERSE"></span><span id="mci_vd_play_reverse"></span>MCI\_VD\_PLAY\_REVERSE</span></span>
</dt> <dd>

<span data-ttu-id="13913-154">反向播放。</span><span class="sxs-lookup"><span data-stu-id="13913-154">Play in reverse.</span></span>

</dd> <dt>

<span data-ttu-id="13913-155"><span id="MCI_VD_PLAY_SCAN"></span><span id="mci_vd_play_scan"></span>MCI \_ VD \_ PLAY \_ 掃描</span><span class="sxs-lookup"><span data-stu-id="13913-155"><span id="MCI_VD_PLAY_SCAN"></span><span id="mci_vd_play_scan"></span>MCI\_VD\_PLAY\_SCAN</span></span>
</dt> <dd>

<span data-ttu-id="13913-156">快速掃描。</span><span class="sxs-lookup"><span data-stu-id="13913-156">Scan quickly.</span></span>

</dd> <dt>

<span data-ttu-id="13913-157"><span id="MCI_VD_PLAY_SLOW"></span><span id="mci_vd_play_slow"></span>MCI \_ VD \_ 播放 \_ 緩慢</span><span class="sxs-lookup"><span data-stu-id="13913-157"><span id="MCI_VD_PLAY_SLOW"></span><span id="mci_vd_play_slow"></span>MCI\_VD\_PLAY\_SLOW</span></span>
</dt> <dd>

<span data-ttu-id="13913-158">慢慢播放。</span><span class="sxs-lookup"><span data-stu-id="13913-158">Play slowly.</span></span>

</dd> <dt>

<span data-ttu-id="13913-159"><span id="MCI_VD_PLAY_SPEED"></span><span id="mci_vd_play_speed"></span>MCI \_ VD \_ 播放 \_ 速度</span><span class="sxs-lookup"><span data-stu-id="13913-159"><span id="MCI_VD_PLAY_SPEED"></span><span id="mci_vd_play_speed"></span>MCI\_VD\_PLAY\_SPEED</span></span>
</dt> <dd>

<span data-ttu-id="13913-160">播放速度會包含在 *lpPlay* 所識別之結構的 **dwSpeed** 成員中。</span><span class="sxs-lookup"><span data-stu-id="13913-160">The play speed is included in the **dwSpeed** member in the structure identified by *lpPlay*.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="13913-161">規格需求</span><span class="sxs-lookup"><span data-stu-id="13913-161">Requirements</span></span>



| <span data-ttu-id="13913-162">需求</span><span class="sxs-lookup"><span data-stu-id="13913-162">Requirement</span></span> | <span data-ttu-id="13913-163">值</span><span class="sxs-lookup"><span data-stu-id="13913-163">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13913-164">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="13913-164">Minimum supported client</span></span><br/> | <span data-ttu-id="13913-165">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="13913-165">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="13913-166">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="13913-166">Minimum supported server</span></span><br/> | <span data-ttu-id="13913-167">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="13913-167">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="13913-168">標頭</span><span class="sxs-lookup"><span data-stu-id="13913-168">Header</span></span><br/>                   | <dl> <span data-ttu-id="13913-169"><dt>Mmsystem (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="13913-169"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13913-170">另請參閱</span><span class="sxs-lookup"><span data-stu-id="13913-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13913-171">Mci</span><span class="sxs-lookup"><span data-stu-id="13913-171">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="13913-172">MCI 命令</span><span class="sxs-lookup"><span data-stu-id="13913-172">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

