---
title: 'MCI_PASTE 命令 (Mmsystem .h) '
description: MCI \_ 貼上命令會將剪貼簿中的資料貼入檔案中。 數位影片裝置辨識此命令。
ms.assetid: cad5799a-08ef-4e34-803a-415b937d8fbd
keywords:
- MCI_PASTE 命令 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_PASTE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b15ff0ae3d14c1df63fbd9ab0c93a85446bdf066
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685489"
---
# <a name="mci_paste-command"></a><span data-ttu-id="6912b-105">MCI \_ 貼上命令</span><span class="sxs-lookup"><span data-stu-id="6912b-105">MCI\_PASTE command</span></span>

<span data-ttu-id="6912b-106">MCI \_ 貼上命令會將剪貼簿中的資料貼入檔案中。</span><span class="sxs-lookup"><span data-stu-id="6912b-106">The MCI\_PASTE command pastes data from the clipboard into a file.</span></span> <span data-ttu-id="6912b-107">數位影片裝置辨識此命令。</span><span class="sxs-lookup"><span data-stu-id="6912b-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="6912b-108">若要傳送此命令，請使用下列參數呼叫 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) 函數。</span><span class="sxs-lookup"><span data-stu-id="6912b-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_PASTE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_PASTE_PARMS) lpPaste
);
```



## <a name="parameters"></a><span data-ttu-id="6912b-109">參數</span><span class="sxs-lookup"><span data-stu-id="6912b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6912b-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="6912b-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="6912b-111">要接收命令訊息之 MCI 裝置的裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="6912b-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="6912b-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="6912b-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="6912b-113">MCI \_ 通知、mci \_ 等候或 mci \_ 測試。</span><span class="sxs-lookup"><span data-stu-id="6912b-113">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="6912b-114">如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。</span><span class="sxs-lookup"><span data-stu-id="6912b-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="6912b-115"><span id="lpPaste"></span><span id="lppaste"></span><span id="LPPASTE"></span>*lpPaste*</span><span class="sxs-lookup"><span data-stu-id="6912b-115"><span id="lpPaste"></span><span id="lppaste"></span><span id="LPPASTE"></span>*lpPaste*</span></span>
</dt> <dd>

<span data-ttu-id="6912b-116">[**MCI \_ DGV \_ 貼上 \_ PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_paste_parms)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="6912b-116">Pointer to an [**MCI\_ DGV\_ PASTE\_ PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_paste_parms) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6912b-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="6912b-117">Return Value</span></span>

<span data-ttu-id="6912b-118">如果成功則傳回零，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="6912b-118">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="6912b-119">備註</span><span class="sxs-lookup"><span data-stu-id="6912b-119">Remarks</span></span>

<span data-ttu-id="6912b-120">下列其他旗標適用于數位視訊裝置：</span><span class="sxs-lookup"><span data-stu-id="6912b-120">The following additional flags apply to digital-video devices:</span></span>

<dl> <dt>

<span data-ttu-id="6912b-121"><span id="MCI_DGV_PASTE_AT"></span><span id="mci_dgv_paste_at"></span>MCI \_ DGV \_ 貼 \_ 在</span><span class="sxs-lookup"><span data-stu-id="6912b-121"><span id="MCI_DGV_PASTE_AT"></span><span id="mci_dgv_paste_at"></span>MCI\_DGV\_PASTE\_AT</span></span>
</dt> <dd>

<span data-ttu-id="6912b-122">矩形會包含在 *lpPaste* 所識別之結構的 **rc** 成員中。</span><span class="sxs-lookup"><span data-stu-id="6912b-122">A rectangle is included in the **rc** member of the structure identified by *lpPaste*.</span></span> <span data-ttu-id="6912b-123">矩形的前兩個值會指定框架內的點，以放置剪貼簿資訊。</span><span class="sxs-lookup"><span data-stu-id="6912b-123">The first two values of the rectangle specify the point within the frame to place the clipboard information.</span></span> <span data-ttu-id="6912b-124">如果矩形高度和寬度為非零值，當剪貼簿的內容貼到框架中時，剪貼簿的內容會調整為這些維度。</span><span class="sxs-lookup"><span data-stu-id="6912b-124">If the rectangle height and width are nonzero, the clipboard contents are scaled to those dimensions when they are pasted in the frame.</span></span> <span data-ttu-id="6912b-125">如果省略旗標，則會將 MCI \_ 貼上預設為整個框架矩形。</span><span class="sxs-lookup"><span data-stu-id="6912b-125">If the flag is omitted, MCI\_PASTE defaults to the entire frame rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="6912b-126"><span id="MCI_DGV_PASTE_AUDIO_STREAM"></span><span id="mci_dgv_paste_audio_stream"></span>MCI \_ DGV \_ 貼上 \_ 音訊 \_ 串流</span><span class="sxs-lookup"><span data-stu-id="6912b-126"><span id="MCI_DGV_PASTE_AUDIO_STREAM"></span><span id="mci_dgv_paste_audio_stream"></span>MCI\_DGV\_PASTE\_AUDIO\_STREAM</span></span>
</dt> <dd>

<span data-ttu-id="6912b-127">音訊串流號碼包含在 *lpPaste* 所識別之結構的 **dwAudioStream** 成員中。</span><span class="sxs-lookup"><span data-stu-id="6912b-127">An audio-stream number is included in the **dwAudioStream** member of the structure identified by *lpPaste*.</span></span> <span data-ttu-id="6912b-128">如果剪貼簿中只有一個音訊串流，則會將音訊資料貼入指定的資料流程。</span><span class="sxs-lookup"><span data-stu-id="6912b-128">If only one audio stream exists on the clipboard, the audio data is pasted into the designated stream.</span></span> <span data-ttu-id="6912b-129">如果剪貼簿中有一個以上的音訊串流，資料流程就會指出資料流程順序的起始數位。</span><span class="sxs-lookup"><span data-stu-id="6912b-129">If more than one audio stream exists on the clipboard, the stream indicates the starting number for the stream sequences.</span></span> <span data-ttu-id="6912b-130">如果您使用此旗標，而且也想要貼上影片，您也必須使用 MCI \_ DGV \_ 貼上影片的旗標 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="6912b-130">If you use this flag and also want to paste video, you must also use the MCI\_DGV\_PASTE\_VIDEO\_STREAM flag.</span></span> <span data-ttu-id="6912b-131"> (如果未指定任何旗標，則會從第一個音訊和影片串流開始貼上所有音訊和影片串流。</span><span class="sxs-lookup"><span data-stu-id="6912b-131">(If neither flag is specified, all audio and video streams are pasted starting with the first audio and video stream.</span></span> <span data-ttu-id="6912b-132">每個貼上的資料流程都會保留其原始資料流程號碼。 ) </span><span class="sxs-lookup"><span data-stu-id="6912b-132">Each pasted stream retains its original stream number.)</span></span>

</dd> <dt>

<span data-ttu-id="6912b-133"><span id="MCI_DGV_PASTE_INSERT"></span><span id="mci_dgv_paste_insert"></span>MCI \_ DGV \_ 貼上 \_ 插入</span><span class="sxs-lookup"><span data-stu-id="6912b-133"><span id="MCI_DGV_PASTE_INSERT"></span><span id="mci_dgv_paste_insert"></span>MCI\_DGV\_PASTE\_INSERT</span></span>
</dt> <dd>

<span data-ttu-id="6912b-134">剪貼簿資料應插入至現有的工作區中，位於 MCI 所指定的位置， \_ 以進行旗標。</span><span class="sxs-lookup"><span data-stu-id="6912b-134">Clipboard data should be inserted in the existing workspace at the position specified by the MCI\_TO flag.</span></span> <span data-ttu-id="6912b-135">在插入點之後，任何現有的資料都會移至工作區，以騰出空間。</span><span class="sxs-lookup"><span data-stu-id="6912b-135">Any existing data after the insertion point is moved in the workspace to make room.</span></span> <span data-ttu-id="6912b-136">此為預設值。</span><span class="sxs-lookup"><span data-stu-id="6912b-136">This is the default.</span></span>

</dd> <dt>

<span data-ttu-id="6912b-137"><span id="MCI_DGV_PASTE_OVERWRITE"></span><span id="mci_dgv_paste_overwrite"></span>MCI \_ DGV \_ 貼上 \_ 覆寫</span><span class="sxs-lookup"><span data-stu-id="6912b-137"><span id="MCI_DGV_PASTE_OVERWRITE"></span><span id="mci_dgv_paste_overwrite"></span>MCI\_DGV\_PASTE\_OVERWRITE</span></span>
</dt> <dd>

<span data-ttu-id="6912b-138">剪貼簿資料應取代已存在於工作區中的資料。</span><span class="sxs-lookup"><span data-stu-id="6912b-138">Clipboard data should replace data already present in the workspace.</span></span> <span data-ttu-id="6912b-139">工作區資料會在插入點之後取代。</span><span class="sxs-lookup"><span data-stu-id="6912b-139">The workspace data replaced follows the insertion point.</span></span>

</dd> <dt>

<span data-ttu-id="6912b-140"><span id="MCI_DGV_PASTE_VIDEO_STREAM"></span><span id="mci_dgv_paste_video_stream"></span>MCI \_ DGV \_ 貼上 \_ 影片 \_ 串流</span><span class="sxs-lookup"><span data-stu-id="6912b-140"><span id="MCI_DGV_PASTE_VIDEO_STREAM"></span><span id="mci_dgv_paste_video_stream"></span>MCI\_DGV\_PASTE\_VIDEO\_STREAM</span></span>
</dt> <dd>

<span data-ttu-id="6912b-141">影片串流號碼包含在 *lpPaste* 所識別之結構的 **dwVideoStream** 成員中。</span><span class="sxs-lookup"><span data-stu-id="6912b-141">A video-stream number is included in the **dwVideoStream** member of the structure identified by *lpPaste*.</span></span> <span data-ttu-id="6912b-142">如果剪貼簿中只有一個影片串流，則會將影片資料貼入指定的資料流程。</span><span class="sxs-lookup"><span data-stu-id="6912b-142">If only one video stream exists on the clipboard, the video data is pasted into the designated stream.</span></span> <span data-ttu-id="6912b-143">如果剪貼簿中有一個以上的影片串流，資料流程就會指出資料流程順序的起始數位。</span><span class="sxs-lookup"><span data-stu-id="6912b-143">If more than one video stream exists on the clipboard, the stream indicates the starting number for the stream sequences.</span></span> <span data-ttu-id="6912b-144">如果您使用此旗標，而且也想要貼上音訊，您也必須使用 MCI \_ DGV \_ 貼上 \_ 音訊 \_ 串流旗標。</span><span class="sxs-lookup"><span data-stu-id="6912b-144">If you use this flag and also want to paste audio, you must also use the MCI\_DGV\_PASTE\_AUDIO\_STREAM flag.</span></span> <span data-ttu-id="6912b-145"> (如果未指定任何旗標，則會從第一個音訊和影片串流開始貼上所有音訊和影片串流。</span><span class="sxs-lookup"><span data-stu-id="6912b-145">(If neither flag is specified, all audio and video streams are pasted starting with the first audio and video stream.</span></span> <span data-ttu-id="6912b-146">每個貼上的資料流程都會保留其原始資料流程號碼。 ) </span><span class="sxs-lookup"><span data-stu-id="6912b-146">Each pasted stream retains its original stream number.)</span></span>

</dd> <dt>

<span data-ttu-id="6912b-147"><span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ 至</span><span class="sxs-lookup"><span data-stu-id="6912b-147"><span id="MCI_TO"></span><span id="mci_to"></span>MCI\_TO</span></span>
</dt> <dd>

<span data-ttu-id="6912b-148">Position 值會包含在 *lpPaste* 所識別之結構的 **dwTo** 成員中。</span><span class="sxs-lookup"><span data-stu-id="6912b-148">A position value is included in the **dwTo** member of the structure identified by *lpPaste*.</span></span> <span data-ttu-id="6912b-149">Position 值指定開始將資料貼入工作區的位置。</span><span class="sxs-lookup"><span data-stu-id="6912b-149">The position value specifies the position to begin pasting data into the workspace.</span></span> <span data-ttu-id="6912b-150">如果省略此旗標，位置就會預設為目前的位置。</span><span class="sxs-lookup"><span data-stu-id="6912b-150">If this flag is omitted, the position defaults to the current position.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6912b-151">規格需求</span><span class="sxs-lookup"><span data-stu-id="6912b-151">Requirements</span></span>



| <span data-ttu-id="6912b-152">需求</span><span class="sxs-lookup"><span data-stu-id="6912b-152">Requirement</span></span> | <span data-ttu-id="6912b-153">值</span><span class="sxs-lookup"><span data-stu-id="6912b-153">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6912b-154">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6912b-154">Minimum supported client</span></span><br/> | <span data-ttu-id="6912b-155">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6912b-155">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="6912b-156">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6912b-156">Minimum supported server</span></span><br/> | <span data-ttu-id="6912b-157">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6912b-157">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="6912b-158">標頭</span><span class="sxs-lookup"><span data-stu-id="6912b-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="6912b-159"><dt>Mmsystem (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="6912b-159"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6912b-160">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6912b-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6912b-161">Mci</span><span class="sxs-lookup"><span data-stu-id="6912b-161">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="6912b-162">MCI 命令</span><span class="sxs-lookup"><span data-stu-id="6912b-162">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

