---
title: 'MCI_COPY 命令 (Mmsystem .h) '
description: MCI \_ 複製命令會將資料複製到剪貼簿。 數位影片裝置辨識此命令。
ms.assetid: 41807920-3312-4cdb-82e6-6ab4b9b35162
keywords:
- MCI_COPY 命令 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_COPY
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4c27950b9599d0b565b982eb59755e4d3f2ea65
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934436"
---
# <a name="mci_copy-command"></a><span data-ttu-id="9727d-105">MCI \_ 複製命令</span><span class="sxs-lookup"><span data-stu-id="9727d-105">MCI\_COPY command</span></span>

<span data-ttu-id="9727d-106">MCI \_ 複製命令會將資料複製到剪貼簿。</span><span class="sxs-lookup"><span data-stu-id="9727d-106">The MCI\_COPY command copies data to the clipboard.</span></span> <span data-ttu-id="9727d-107">數位影片裝置辨識此命令。</span><span class="sxs-lookup"><span data-stu-id="9727d-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="9727d-108">若要傳送此命令，請使用下列參數呼叫 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) 函數。</span><span class="sxs-lookup"><span data-stu-id="9727d-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_COPY, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_COPY_PARMS) lpCopy
);
```



## <a name="parameters"></a><span data-ttu-id="9727d-109">參數</span><span class="sxs-lookup"><span data-stu-id="9727d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9727d-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="9727d-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="9727d-111">要接收命令訊息之 MCI 裝置的裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="9727d-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="9727d-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="9727d-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="9727d-113">MCI \_ 通知、mci \_ 等候或 mci \_ 測試。</span><span class="sxs-lookup"><span data-stu-id="9727d-113">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="9727d-114">如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。</span><span class="sxs-lookup"><span data-stu-id="9727d-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="9727d-115"><span id="lpCopy"></span><span id="lpcopy"></span><span id="LPCOPY"></span>*lpCopy*</span><span class="sxs-lookup"><span data-stu-id="9727d-115"><span id="lpCopy"></span><span id="lpcopy"></span><span id="LPCOPY"></span>*lpCopy*</span></span>
</dt> <dd>

<span data-ttu-id="9727d-116">[**MCI \_ DGV \_ 複製 \_ PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_copy_parms)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="9727d-116">Pointer to an [**MCI\_DGV\_COPY\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_copy_parms) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9727d-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="9727d-117">Return Value</span></span>

<span data-ttu-id="9727d-118">如果成功則傳回零，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="9727d-118">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="9727d-119">備註</span><span class="sxs-lookup"><span data-stu-id="9727d-119">Remarks</span></span>

<span data-ttu-id="9727d-120">下列其他旗標適用于數位視訊裝置：</span><span class="sxs-lookup"><span data-stu-id="9727d-120">The following additional flags apply to digital-video devices:</span></span>

<dl> <dt>

<span data-ttu-id="9727d-121"><span id="MCI_DGV_COPY_AT"></span><span id="mci_dgv_copy_at"></span>MCI \_ DGV \_ 複製 \_ 位置</span><span class="sxs-lookup"><span data-stu-id="9727d-121"><span id="MCI_DGV_COPY_AT"></span><span id="mci_dgv_copy_at"></span>MCI\_DGV\_COPY\_AT</span></span>
</dt> <dd>

<span data-ttu-id="9727d-122">矩形會包含在 *lpCopy* 所識別之結構的 **rc** 成員中。</span><span class="sxs-lookup"><span data-stu-id="9727d-122">A rectangle is included in the **rc** member of the structure identified by *lpCopy*.</span></span> <span data-ttu-id="9727d-123">矩形會指定要複製的每個畫面格的部分。</span><span class="sxs-lookup"><span data-stu-id="9727d-123">The rectangle specifies the portion of each frame to copy.</span></span> <span data-ttu-id="9727d-124">如果省略旗標，MCI 複製會複製 \_ 整個框架。</span><span class="sxs-lookup"><span data-stu-id="9727d-124">If the flag is omitted, MCI\_COPY copies the entire frame.</span></span>

</dd> <dt>

<span data-ttu-id="9727d-125"><span id="MCI_DGV_COPY_AUDIO_STREAM"></span><span id="mci_dgv_copy_audio_stream"></span>MCI \_ DGV \_ 複製 \_ 音訊 \_ 串流</span><span class="sxs-lookup"><span data-stu-id="9727d-125"><span id="MCI_DGV_COPY_AUDIO_STREAM"></span><span id="mci_dgv_copy_audio_stream"></span>MCI\_DGV\_COPY\_AUDIO\_STREAM</span></span>
</dt> <dd>

<span data-ttu-id="9727d-126">音訊串流號碼包含在 *lpCopy* 所識別之結構的 **dwAudioStream** 成員中。</span><span class="sxs-lookup"><span data-stu-id="9727d-126">An audio-stream number is included in the **dwAudioStream** member of the structure identified by *lpCopy*.</span></span> <span data-ttu-id="9727d-127">如果您使用此旗標，而且也想要複製影片，您也必須使用 MCI \_ DGV \_ 複製 \_ 影片旗標 \_ 。</span><span class="sxs-lookup"><span data-stu-id="9727d-127">If you use this flag and also want to copy video, you must also use the MCI\_DGV\_COPY\_VIDEO\_STREAM flag.</span></span> <span data-ttu-id="9727d-128"> (如果未指定任何旗標，則會複製所有音訊和影片資料流程中的資料。 ) </span><span class="sxs-lookup"><span data-stu-id="9727d-128">(If neither flag is specified, data from all audio and video streams is copied.)</span></span>

</dd> <dt>

<span data-ttu-id="9727d-129"><span id="MCI_DGV_COPY_VIDEO_STREAM"></span><span id="mci_dgv_copy_video_stream"></span>MCI \_ DGV \_ 複製 \_ 影片 \_ 串流</span><span class="sxs-lookup"><span data-stu-id="9727d-129"><span id="MCI_DGV_COPY_VIDEO_STREAM"></span><span id="mci_dgv_copy_video_stream"></span>MCI\_DGV\_COPY\_VIDEO\_STREAM</span></span>
</dt> <dd>

<span data-ttu-id="9727d-130">影片串流號碼包含在 *lpCopy* 所識別之結構的 **dwVideoStream** 成員中。</span><span class="sxs-lookup"><span data-stu-id="9727d-130">A video-stream number is included in the **dwVideoStream** member of the structure identified by *lpCopy*.</span></span> <span data-ttu-id="9727d-131">如果您使用此旗標，而且也想要複製音訊，您也必須使用 MCI \_ DGV \_ 複製 \_ 音訊 \_ 串流旗標。</span><span class="sxs-lookup"><span data-stu-id="9727d-131">If you use this flag and also want to copy audio, you must also use the MCI\_DGV\_COPY\_AUDIO\_STREAM flag.</span></span> <span data-ttu-id="9727d-132"> (如果未指定任何旗標，則會複製所有音訊和影片資料流程中的資料。 ) </span><span class="sxs-lookup"><span data-stu-id="9727d-132">(If neither flag is specified, data from all audio and video streams is copied.)</span></span>

</dd> <dt>

<span data-ttu-id="9727d-133"><span id="MCI_FROM"></span><span id="mci_from"></span>MCI \_ 來源</span><span class="sxs-lookup"><span data-stu-id="9727d-133"><span id="MCI_FROM"></span><span id="mci_from"></span>MCI\_FROM</span></span>
</dt> <dd>

<span data-ttu-id="9727d-134">起始位置會包含在 *lpCopy* 所識別之結構的 **dwFrom** 成員中。</span><span class="sxs-lookup"><span data-stu-id="9727d-134">A starting location is included in the **dwFrom** member of the structure identified by *lpCopy*.</span></span> <span data-ttu-id="9727d-135">指派給位置值的單位，會以 Mci 設定的 \_ \_ 時間格式旗標，以 \_ [mci \_ set](mci-set.md) 命令來指定。</span><span class="sxs-lookup"><span data-stu-id="9727d-135">The units assigned to the position values are specified with the MCI\_SET\_TIME\_FORMAT flag of the [MCI\_SET](mci-set.md) command.</span></span>

</dd> <dt>

<span data-ttu-id="9727d-136"><span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ 至</span><span class="sxs-lookup"><span data-stu-id="9727d-136"><span id="MCI_TO"></span><span id="mci_to"></span>MCI\_TO</span></span>
</dt> <dd>

<span data-ttu-id="9727d-137">結束位置會包含在由 *lpCopy* 所識別之結構的 **dwTo** 成員中。</span><span class="sxs-lookup"><span data-stu-id="9727d-137">An ending location is included in the **dwTo** member of the structure identified by *lpCopy*.</span></span> <span data-ttu-id="9727d-138">指派給位置值的單位，會以 MCI 設定的 \_ \_ 時間格式旗標，以 \_ mci \_ set 命令來指定。</span><span class="sxs-lookup"><span data-stu-id="9727d-138">The units assigned to the position values are specified with the MCI\_SET\_TIME\_FORMAT flag of the MCI\_SET command.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9727d-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="9727d-139">Requirements</span></span>



| <span data-ttu-id="9727d-140">需求</span><span class="sxs-lookup"><span data-stu-id="9727d-140">Requirement</span></span> | <span data-ttu-id="9727d-141">值</span><span class="sxs-lookup"><span data-stu-id="9727d-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9727d-142">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9727d-142">Minimum supported client</span></span><br/> | <span data-ttu-id="9727d-143">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9727d-143">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="9727d-144">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9727d-144">Minimum supported server</span></span><br/> | <span data-ttu-id="9727d-145">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9727d-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="9727d-146">標頭</span><span class="sxs-lookup"><span data-stu-id="9727d-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="9727d-147"><dt>Mmsystem (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="9727d-147"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9727d-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9727d-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9727d-149">Mci</span><span class="sxs-lookup"><span data-stu-id="9727d-149">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="9727d-150">MCI 命令</span><span class="sxs-lookup"><span data-stu-id="9727d-150">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

