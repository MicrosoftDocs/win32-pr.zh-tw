---
title: 'MCI_DELETE 命令 (Mmsystem .h) '
description: MCI \_ DELETE 命令會移除檔案中的資料。 數位-視頻和波形-音訊裝置辨識此命令。
ms.assetid: cf7fae86-e81e-4006-9755-fd01f81aeb62
keywords:
- MCI_DELETE 命令 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_DELETE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8c1b9f81712c842e06085c323ca2110c8e06784
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934685"
---
# <a name="mci_delete-command"></a><span data-ttu-id="f5290-105">MCI \_ 刪除命令</span><span class="sxs-lookup"><span data-stu-id="f5290-105">MCI\_DELETE command</span></span>

<span data-ttu-id="f5290-106">MCI \_ DELETE 命令會移除檔案中的資料。</span><span class="sxs-lookup"><span data-stu-id="f5290-106">The MCI\_DELETE command removes data from the file.</span></span> <span data-ttu-id="f5290-107">數位-視頻和波形-音訊裝置辨識此命令。</span><span class="sxs-lookup"><span data-stu-id="f5290-107">Digital-video and waveform-audio devices recognize this command.</span></span>

<span data-ttu-id="f5290-108">若要傳送此命令，請使用下列參數呼叫 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) 函數。</span><span class="sxs-lookup"><span data-stu-id="f5290-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_DELETE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpDelete
);
```



## <a name="parameters"></a><span data-ttu-id="f5290-109">參數</span><span class="sxs-lookup"><span data-stu-id="f5290-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5290-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="f5290-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="f5290-111">要接收命令訊息之 MCI 裝置的裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="f5290-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="f5290-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="f5290-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="f5290-113">\_ \_ 適用于數位視訊裝置、mci 測試的 mci 通知、mci 等待或 \_ 。</span><span class="sxs-lookup"><span data-stu-id="f5290-113">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video devices, MCI\_TEST.</span></span> <span data-ttu-id="f5290-114">如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。</span><span class="sxs-lookup"><span data-stu-id="f5290-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="f5290-115"><span id="lpDelete"></span><span id="lpdelete"></span><span id="LPDELETE"></span>*lpDelete*</span><span class="sxs-lookup"><span data-stu-id="f5290-115"><span id="lpDelete"></span><span id="lpdelete"></span><span id="LPDELETE"></span>*lpDelete*</span></span>
</dt> <dd>

<span data-ttu-id="f5290-116">[**MCI \_ 泛型 \_ PARMS**](mci-generic-parms.md)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="f5290-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="f5290-117">具有擴充命令集的 (裝置，可能會以裝置特定結構取代此結構。 ) </span><span class="sxs-lookup"><span data-stu-id="f5290-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5290-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="f5290-118">Return Value</span></span>

<span data-ttu-id="f5290-119">如果成功則傳回零，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="f5290-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="f5290-120">備註</span><span class="sxs-lookup"><span data-stu-id="f5290-120">Remarks</span></span>

<span data-ttu-id="f5290-121">下列旗標適用于 **digitalvideo** 裝置類型：</span><span class="sxs-lookup"><span data-stu-id="f5290-121">The following flags apply to the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="f5290-122"><span id="MCI_DGV_DELETE_AT"></span><span id="mci_dgv_delete_at"></span>MCI \_ DGV \_ 刪除 \_ 于</span><span class="sxs-lookup"><span data-stu-id="f5290-122"><span id="MCI_DGV_DELETE_AT"></span><span id="mci_dgv_delete_at"></span>MCI\_DGV\_DELETE\_AT</span></span>
</dt> <dd>

<span data-ttu-id="f5290-123">矩形會包含在 *lpDelete* 所識別之結構的 **rc** 成員中。</span><span class="sxs-lookup"><span data-stu-id="f5290-123">A rectangle is included in the **rc** member of the structure identified by *lpDelete*.</span></span> <span data-ttu-id="f5290-124">矩形會指定要刪除之每個畫面格的部分。</span><span class="sxs-lookup"><span data-stu-id="f5290-124">The rectangle specifies the portion of each frame to delete.</span></span> <span data-ttu-id="f5290-125">使用這個旗標時，框架會保留在工作區中，而矩形所指定的區域會變成黑色。</span><span class="sxs-lookup"><span data-stu-id="f5290-125">When this flag is used, the frame is retained in the workspace and the area specified by the rectangle becomes black.</span></span> <span data-ttu-id="f5290-126">如果省略旗標，則 MCI \_ 刪除會預設為整個畫面格，並從工作區中移除框架。</span><span class="sxs-lookup"><span data-stu-id="f5290-126">If the flag is omitted, MCI\_DELETE defaults to the entire frame and removes the frame from the workspace.</span></span>

</dd> <dt>

<span data-ttu-id="f5290-127"><span id="MCI_DGV_DELETE_AUDIO_STREAM"></span><span id="mci_dgv_delete_audio_stream"></span>MCI \_ DGV \_ 刪除 \_ 音訊 \_ 串流</span><span class="sxs-lookup"><span data-stu-id="f5290-127"><span id="MCI_DGV_DELETE_AUDIO_STREAM"></span><span id="mci_dgv_delete_audio_stream"></span>MCI\_DGV\_DELETE\_AUDIO\_STREAM</span></span>
</dt> <dd>

<span data-ttu-id="f5290-128">音訊串流號碼包含在 *lpDelete* 所識別之結構的 **dwAudioStream** 成員中。</span><span class="sxs-lookup"><span data-stu-id="f5290-128">An audio-stream number is included in the **dwAudioStream** member of the structure identified by *lpDelete*.</span></span> <span data-ttu-id="f5290-129">如果您使用此旗標，而且也想要刪除影片，您也必須使用 MCI \_ DGV \_ delete \_ 影片旗標 \_ 。</span><span class="sxs-lookup"><span data-stu-id="f5290-129">If you use this flag and also want to delete video, you must also use the MCI\_DGV\_DELETE\_VIDEO\_STREAM flag.</span></span> <span data-ttu-id="f5290-130"> (如果未指定任何旗標，則會刪除所有音訊和影片資料流程中的資料。 ) </span><span class="sxs-lookup"><span data-stu-id="f5290-130">(If neither flag is specified, data from all audio and video streams is deleted.)</span></span>

</dd> <dt>

<span data-ttu-id="f5290-131"><span id="MCI_DGV_DELETE_VIDEO_STREAM"></span><span id="mci_dgv_delete_video_stream"></span>MCI \_ DGV \_ 刪除 \_ 影片 \_ 串流</span><span class="sxs-lookup"><span data-stu-id="f5290-131"><span id="MCI_DGV_DELETE_VIDEO_STREAM"></span><span id="mci_dgv_delete_video_stream"></span>MCI\_DGV\_DELETE\_VIDEO\_STREAM</span></span>
</dt> <dd>

<span data-ttu-id="f5290-132">影片串流號碼包含在 *lpDelete* 所識別之結構的 **dwVideoStream** 成員中。</span><span class="sxs-lookup"><span data-stu-id="f5290-132">A video-stream number is included in the **dwVideoStream** member of the structure identified by *lpDelete*.</span></span> <span data-ttu-id="f5290-133">如果您使用此旗標，而且也想要刪除音訊，您也必須使用 MCI \_ DGV \_ delete \_ 音訊 \_ 串流旗標。</span><span class="sxs-lookup"><span data-stu-id="f5290-133">If you use this flag and also want to delete audio, you must also use the MCI\_DGV\_DELETE\_AUDIO\_STREAM flag.</span></span> <span data-ttu-id="f5290-134"> (如果未指定任何旗標，則會刪除所有音訊和影片資料流程中的資料。 ) </span><span class="sxs-lookup"><span data-stu-id="f5290-134">(If neither flag is specified, data from all audio and video streams is deleted.)</span></span>

</dd> <dt>

<span data-ttu-id="f5290-135"><span id="MCI_FROM"></span><span id="mci_from"></span>MCI \_ 來源</span><span class="sxs-lookup"><span data-stu-id="f5290-135"><span id="MCI_FROM"></span><span id="mci_from"></span>MCI\_FROM</span></span>
</dt> <dd>

<span data-ttu-id="f5290-136">起始位置會包含在 *lpDelete* 所識別之結構的 **dwFrom** 成員中。</span><span class="sxs-lookup"><span data-stu-id="f5290-136">A starting location is included in the **dwFrom** member of the structure identified by *lpDelete*.</span></span> <span data-ttu-id="f5290-137">指派給位置值的單位，會以 Mci 設定的 \_ \_ 時間格式旗標，以 \_ [mci \_ set](mci-set.md) 命令來指定。</span><span class="sxs-lookup"><span data-stu-id="f5290-137">The units assigned to the position values are specified with the MCI\_SET\_TIME\_FORMAT flag of the [MCI\_SET](mci-set.md) command.</span></span>

</dd> <dt>

<span data-ttu-id="f5290-138"><span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ 至</span><span class="sxs-lookup"><span data-stu-id="f5290-138"><span id="MCI_TO"></span><span id="mci_to"></span>MCI\_TO</span></span>
</dt> <dd>

<span data-ttu-id="f5290-139">結束位置會包含在由 *lpDelete* 所識別之結構的 **dwTo** 成員中。</span><span class="sxs-lookup"><span data-stu-id="f5290-139">An ending location is included in the **dwTo** member of the structure identified by *lpDelete*.</span></span> <span data-ttu-id="f5290-140">指派給位置值的單位是使用 mci \_ set \_ TIME \_ FORMAT 旗標來指定 \_ 。</span><span class="sxs-lookup"><span data-stu-id="f5290-140">The units assigned to the position values are specified with the MCI\_SET\_TIME\_FORMAT flag of MCI\_SET.</span></span>

</dd> </dl>

<span data-ttu-id="f5290-141">針對數位影片裝置， *lpDelete* 參數會指向 [**MCI \_ DGV \_ 刪除 \_ PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_delete_parms) 結構。</span><span class="sxs-lookup"><span data-stu-id="f5290-141">For digital-video devices, the *lpDelete* parameter points to an [**MCI\_DGV\_DELETE\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_delete_parms) structure.</span></span>

<span data-ttu-id="f5290-142">下列旗標適用于 **waveaudio** 裝置類型：</span><span class="sxs-lookup"><span data-stu-id="f5290-142">The following flags apply to the **waveaudio** device type:</span></span>

<dl> <dt>

<span data-ttu-id="f5290-143"><span id="MCI_FROM"></span><span id="mci_from"></span>MCI \_ 來源</span><span class="sxs-lookup"><span data-stu-id="f5290-143"><span id="MCI_FROM"></span><span id="mci_from"></span>MCI\_FROM</span></span>
</dt> <dd>

<span data-ttu-id="f5290-144">起始位置會包含在 *lpDelete* 所識別之結構的 **dwFrom** 成員中。</span><span class="sxs-lookup"><span data-stu-id="f5290-144">A starting location is included in the **dwFrom** member of the structure identified by *lpDelete*.</span></span> <span data-ttu-id="f5290-145">指派給位置值的單位是使用 mci \_ set \_ TIME \_ FORMAT 旗標來指定。 [ \_ ](mci-set.md)</span><span class="sxs-lookup"><span data-stu-id="f5290-145">The units assigned to the position values are specified with the MCI\_SET\_TIME\_FORMAT flag of [MCI\_SET](mci-set.md).</span></span>

</dd> <dt>

<span data-ttu-id="f5290-146"><span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ 至</span><span class="sxs-lookup"><span data-stu-id="f5290-146"><span id="MCI_TO"></span><span id="mci_to"></span>MCI\_TO</span></span>
</dt> <dd>

<span data-ttu-id="f5290-147">結束位置會包含在由 *lpDelete* 所識別之結構的 **dwTo** 成員中。</span><span class="sxs-lookup"><span data-stu-id="f5290-147">An ending location is included in the **dwTo** member of the structure identified by *lpDelete*.</span></span> <span data-ttu-id="f5290-148">指派給位置值的單位是使用 mci \_ set \_ TIME \_ FORMAT 旗標來指定 \_ 。</span><span class="sxs-lookup"><span data-stu-id="f5290-148">The units assigned to the position values are specified with the MCI\_SET\_TIME\_FORMAT flag of MCI\_SET.</span></span>

</dd> </dl>

<span data-ttu-id="f5290-149">針對波形音訊裝置， *lpDelete* 參數會指向 [**MCI \_ WAVE \_ DELETE \_ PARMS**](mci-wave-delete-parms.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="f5290-149">For waveform-audio devices, the *lpDelete* parameter points to an [**MCI\_WAVE\_DELETE\_PARMS**](mci-wave-delete-parms.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5290-150">規格需求</span><span class="sxs-lookup"><span data-stu-id="f5290-150">Requirements</span></span>



| <span data-ttu-id="f5290-151">需求</span><span class="sxs-lookup"><span data-stu-id="f5290-151">Requirement</span></span> | <span data-ttu-id="f5290-152">值</span><span class="sxs-lookup"><span data-stu-id="f5290-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5290-153">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f5290-153">Minimum supported client</span></span><br/> | <span data-ttu-id="f5290-154">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f5290-154">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="f5290-155">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f5290-155">Minimum supported server</span></span><br/> | <span data-ttu-id="f5290-156">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f5290-156">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="f5290-157">標頭</span><span class="sxs-lookup"><span data-stu-id="f5290-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="f5290-158"><dt>Mmsystem (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="f5290-158"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5290-159">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f5290-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5290-160">Mci</span><span class="sxs-lookup"><span data-stu-id="f5290-160">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="f5290-161">MCI 命令</span><span class="sxs-lookup"><span data-stu-id="f5290-161">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

