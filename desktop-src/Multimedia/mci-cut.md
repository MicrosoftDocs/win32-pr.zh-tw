---
title: 'MCI_CUT 命令 (Mmsystem .h) '
description: MCI \_ 剪下命令會移除檔案中的資料，並將資料複製到剪貼簿。 數位影片裝置辨識此命令。
ms.assetid: 09bb505b-715a-4393-80f0-e9ba270a8ac1
keywords:
- MCI_CUT 命令 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_CUT
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c564451596f115daca8514785449abf001e224ef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934686"
---
# <a name="mci_cut-command"></a><span data-ttu-id="afdad-105">MCI \_ 剪下命令</span><span class="sxs-lookup"><span data-stu-id="afdad-105">MCI\_CUT command</span></span>

<span data-ttu-id="afdad-106">MCI \_ 剪下命令會移除檔案中的資料，並將資料複製到剪貼簿。</span><span class="sxs-lookup"><span data-stu-id="afdad-106">The MCI\_CUT command removes data from the file and copies it to the clipboard.</span></span> <span data-ttu-id="afdad-107">數位影片裝置辨識此命令。</span><span class="sxs-lookup"><span data-stu-id="afdad-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="afdad-108">若要傳送此命令，請使用下列參數呼叫 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) 函數。</span><span class="sxs-lookup"><span data-stu-id="afdad-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_CUT, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_CUT_PARMS) lpCut
);
```



## <a name="parameters"></a><span data-ttu-id="afdad-109">參數</span><span class="sxs-lookup"><span data-stu-id="afdad-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="afdad-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="afdad-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="afdad-111">要接收命令訊息之 MCI 裝置的裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="afdad-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="afdad-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="afdad-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="afdad-113">MCI \_ 通知、mci \_ 等候或 mci \_ 測試。</span><span class="sxs-lookup"><span data-stu-id="afdad-113">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="afdad-114">如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。</span><span class="sxs-lookup"><span data-stu-id="afdad-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="afdad-115"><span id="lpCut"></span><span id="lpcut"></span><span id="LPCUT"></span>*lpCut*</span><span class="sxs-lookup"><span data-stu-id="afdad-115"><span id="lpCut"></span><span id="lpcut"></span><span id="LPCUT"></span>*lpCut*</span></span>
</dt> <dd>

<span data-ttu-id="afdad-116">[**MCI \_ DGV \_ 剪下 \_ PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_cut_parms)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="afdad-116">Pointer to an [**MCI\_DGV\_CUT\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_cut_parms) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="afdad-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="afdad-117">Return Value</span></span>

<span data-ttu-id="afdad-118">如果成功則傳回零，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="afdad-118">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="afdad-119">備註</span><span class="sxs-lookup"><span data-stu-id="afdad-119">Remarks</span></span>

<span data-ttu-id="afdad-120">下列其他旗標適用于數位視訊裝置：</span><span class="sxs-lookup"><span data-stu-id="afdad-120">The following additional flags apply to digital-video devices:</span></span>

<dl> <dt>

<span data-ttu-id="afdad-121"><span id="MCI_DGV_CUT_AT"></span><span id="mci_dgv_cut_at"></span>MCI \_ DGV \_ 剪 \_ 下</span><span class="sxs-lookup"><span data-stu-id="afdad-121"><span id="MCI_DGV_CUT_AT"></span><span id="mci_dgv_cut_at"></span>MCI\_DGV\_CUT\_AT</span></span>
</dt> <dd>

<span data-ttu-id="afdad-122">矩形會包含在 *lpCut* 所識別之結構的 **rc** 成員中。</span><span class="sxs-lookup"><span data-stu-id="afdad-122">A rectangle is included in the **rc** member of the structure identified by *lpCut*.</span></span> <span data-ttu-id="afdad-123">矩形會指定要剪下之每個框架的部分。</span><span class="sxs-lookup"><span data-stu-id="afdad-123">The rectangle specifies the portion of each frame to cut.</span></span> <span data-ttu-id="afdad-124">如果省略旗標，MCI 會 \_ 剪下整個框架。</span><span class="sxs-lookup"><span data-stu-id="afdad-124">If the flag is omitted, MCI\_CUT cuts the entire frame.</span></span>

</dd> <dt>

<span data-ttu-id="afdad-125"><span id="MCI_DGV_CUT_AUDIO_STREAM"></span><span id="mci_dgv_cut_audio_stream"></span>MCI \_ DGV \_ 剪下 \_ 音訊 \_ 串流</span><span class="sxs-lookup"><span data-stu-id="afdad-125"><span id="MCI_DGV_CUT_AUDIO_STREAM"></span><span id="mci_dgv_cut_audio_stream"></span>MCI\_DGV\_CUT\_AUDIO\_STREAM</span></span>
</dt> <dd>

<span data-ttu-id="afdad-126">音訊串流號碼包含在 *lpCut* 所識別之結構的 **dwAudioStream** 成員中。</span><span class="sxs-lookup"><span data-stu-id="afdad-126">An audio-stream number is included in the **dwAudioStream** member of the structure identified by *lpCut*.</span></span> <span data-ttu-id="afdad-127">如果您使用此旗標，而且也想要剪下影片，您也必須使用 MCI \_ DGV 剪下的 \_ \_ 影片 \_ 資料流程旗標。</span><span class="sxs-lookup"><span data-stu-id="afdad-127">If you use this flag and also want to cut video, you must also use the MCI\_DGV\_CUT\_VIDEO\_STREAM flag.</span></span> <span data-ttu-id="afdad-128"> (如果未指定任何旗標，則會剪下所有音訊和影片資料流程中的資料。 ) </span><span class="sxs-lookup"><span data-stu-id="afdad-128">(If neither flag is specified, data from all audio and video streams is cut.)</span></span>

</dd> <dt>

<span data-ttu-id="afdad-129"><span id="MCI_DGV_CUT_VIDEO_STREAM"></span><span id="mci_dgv_cut_video_stream"></span>MCI \_ DGV \_ 剪下 \_ 影片 \_ 串流</span><span class="sxs-lookup"><span data-stu-id="afdad-129"><span id="MCI_DGV_CUT_VIDEO_STREAM"></span><span id="mci_dgv_cut_video_stream"></span>MCI\_DGV\_CUT\_VIDEO\_STREAM</span></span>
</dt> <dd>

<span data-ttu-id="afdad-130">影片串流號碼包含在 *lpCut* 所識別之結構的 **dwVideoStream** 成員中。</span><span class="sxs-lookup"><span data-stu-id="afdad-130">A video-stream number is included in the **dwVideoStream** member of the structure identified by *lpCut*.</span></span> <span data-ttu-id="afdad-131">如果您使用此旗標，而且也想要剪下音訊，您也必須使用 MCI \_ DGV \_ 剪下 \_ 音訊 \_ 串流旗標。</span><span class="sxs-lookup"><span data-stu-id="afdad-131">If you use this flag and also want to cut audio, you must also use the MCI\_DGV\_CUT\_AUDIO\_STREAM flag.</span></span> <span data-ttu-id="afdad-132"> (如果未指定任何旗標，則會剪下所有音訊和影片資料流程中的資料。 ) </span><span class="sxs-lookup"><span data-stu-id="afdad-132">(If neither flag is specified, data from all audio and video streams is cut.)</span></span>

</dd> <dt>

<span data-ttu-id="afdad-133"><span id="MCI_FROM"></span><span id="mci_from"></span>MCI \_ 來源</span><span class="sxs-lookup"><span data-stu-id="afdad-133"><span id="MCI_FROM"></span><span id="mci_from"></span>MCI\_FROM</span></span>
</dt> <dd>

<span data-ttu-id="afdad-134">起始位置會包含在 *lpCut* 所識別之結構的 **dwFrom** 成員中。</span><span class="sxs-lookup"><span data-stu-id="afdad-134">A starting location is included in the **dwFrom** member of the structure identified by *lpCut*.</span></span> <span data-ttu-id="afdad-135">指派給位置值的單位，會以 Mci 設定的 \_ \_ 時間格式旗標，以 \_ [mci \_ set](mci-set.md) 命令來指定。</span><span class="sxs-lookup"><span data-stu-id="afdad-135">The units assigned to the position values are specified with the MCI\_SET\_TIME\_FORMAT flag of the [MCI\_SET](mci-set.md) command.</span></span>

</dd> <dt>

<span data-ttu-id="afdad-136"><span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ 至</span><span class="sxs-lookup"><span data-stu-id="afdad-136"><span id="MCI_TO"></span><span id="mci_to"></span>MCI\_TO</span></span>
</dt> <dd>

<span data-ttu-id="afdad-137">結束位置會包含在由 *lpCut* 所識別之結構的 **dwTo** 成員中。</span><span class="sxs-lookup"><span data-stu-id="afdad-137">An ending location is included in the **dwTo** member of the structure identified by *lpCut*.</span></span> <span data-ttu-id="afdad-138">指派給位置值的單位是使用 mci \_ set \_ TIME \_ FORMAT 旗標來指定 \_ 。</span><span class="sxs-lookup"><span data-stu-id="afdad-138">The units assigned to the position values are specified with the MCI\_SET\_TIME\_FORMAT flag of MCI\_SET.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="afdad-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="afdad-139">Requirements</span></span>



| <span data-ttu-id="afdad-140">需求</span><span class="sxs-lookup"><span data-stu-id="afdad-140">Requirement</span></span> | <span data-ttu-id="afdad-141">值</span><span class="sxs-lookup"><span data-stu-id="afdad-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="afdad-142">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="afdad-142">Minimum supported client</span></span><br/> | <span data-ttu-id="afdad-143">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="afdad-143">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="afdad-144">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="afdad-144">Minimum supported server</span></span><br/> | <span data-ttu-id="afdad-145">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="afdad-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="afdad-146">標頭</span><span class="sxs-lookup"><span data-stu-id="afdad-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="afdad-147"><dt>Mmsystem (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="afdad-147"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="afdad-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="afdad-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="afdad-149">Mci</span><span class="sxs-lookup"><span data-stu-id="afdad-149">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="afdad-150">MCI 命令</span><span class="sxs-lookup"><span data-stu-id="afdad-150">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

