---
title: 'MCI_SEEK 命令 (Mmsystem .h) '
description: MCI \_ 搜尋命令會儘快變更內容中的目前位置。
ms.assetid: 5ffab964-a28d-4dc2-ac04-da501cd34d24
keywords:
- MCI_SEEK 命令 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_SEEK
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0e34f6fa823092968e74515a885e7a40db9f2d7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024785"
---
# <a name="mci_seek-command"></a><span data-ttu-id="c3c5f-104">MCI \_ 搜尋命令</span><span class="sxs-lookup"><span data-stu-id="c3c5f-104">MCI\_SEEK command</span></span>

<span data-ttu-id="c3c5f-105">MCI \_ 搜尋命令會儘快變更內容中的目前位置。</span><span class="sxs-lookup"><span data-stu-id="c3c5f-105">The MCI\_SEEK command changes the current position in the content as quickly as possible.</span></span> <span data-ttu-id="c3c5f-106">影片和音訊輸出會在搜尋期間停用。</span><span class="sxs-lookup"><span data-stu-id="c3c5f-106">Video and audio output are disabled during the seek.</span></span> <span data-ttu-id="c3c5f-107">搜尋完成後，裝置就會停止。</span><span class="sxs-lookup"><span data-stu-id="c3c5f-107">After the seek is complete, the device is stopped.</span></span> <span data-ttu-id="c3c5f-108">CD 音訊、數位影片、MIDI sequencer、VCR、videodisc 和波形-音訊裝置都會辨識此命令。</span><span class="sxs-lookup"><span data-stu-id="c3c5f-108">CD audio, digital-video, MIDI sequencer, VCR, videodisc, and waveform-audio devices recognize this command.</span></span>

<span data-ttu-id="c3c5f-109">若要傳送此命令，請使用下列參數呼叫 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) 函數。</span><span class="sxs-lookup"><span data-stu-id="c3c5f-109">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SEEK, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_SEEK_PARMS) lpSeek
);
```



## <a name="parameters"></a><span data-ttu-id="c3c5f-110">參數</span><span class="sxs-lookup"><span data-stu-id="c3c5f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3c5f-111"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="c3c5f-111"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="c3c5f-112">要接收命令訊息之 MCI 裝置的裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="c3c5f-112">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="c3c5f-113"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="c3c5f-113"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="c3c5f-114">\_ \_ 針對數位-視頻和 VCR 裝置，mci 測試的 mci 通知、mci 等候或 \_ 。</span><span class="sxs-lookup"><span data-stu-id="c3c5f-114">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video and VCR devices, MCI\_TEST.</span></span> <span data-ttu-id="c3c5f-115">如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。</span><span class="sxs-lookup"><span data-stu-id="c3c5f-115">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="c3c5f-116"><span id="lpSeek"></span><span id="lpseek"></span><span id="LPSEEK"></span>*lpSeek*</span><span class="sxs-lookup"><span data-stu-id="c3c5f-116"><span id="lpSeek"></span><span id="lpseek"></span><span id="LPSEEK"></span>*lpSeek*</span></span>
</dt> <dd>

<span data-ttu-id="c3c5f-117">[**MCI \_ 搜尋 \_ PARMS**](mci-seek-parms.md)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="c3c5f-117">Pointer to an [**MCI\_SEEK\_PARMS**](mci-seek-parms.md) structure.</span></span> <span data-ttu-id="c3c5f-118">具有擴充命令集的 (裝置，可能會以裝置特定結構取代此結構。 ) </span><span class="sxs-lookup"><span data-stu-id="c3c5f-118">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3c5f-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="c3c5f-119">Return Value</span></span>

<span data-ttu-id="c3c5f-120">如果成功則傳回零，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="c3c5f-120">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="c3c5f-121">備註</span><span class="sxs-lookup"><span data-stu-id="c3c5f-121">Remarks</span></span>

<span data-ttu-id="c3c5f-122">如果裝置的資料取樣大小大於1個位元組 (例如使用波形音訊身歷聲資料) ，此命令會在指定的位置與範例開始不一致時，移至最接近樣本的開頭。</span><span class="sxs-lookup"><span data-stu-id="c3c5f-122">If a data sample size for a device is larger than 1 byte (such as with waveform-audio stereo data), this command moves to the beginning of the nearest sample when a specified position does not coincide with the start of a sample.</span></span>

<span data-ttu-id="c3c5f-123">下列其他旗標適用于所有支援 MCI 搜尋的裝置 \_ ：</span><span class="sxs-lookup"><span data-stu-id="c3c5f-123">The following additional flags apply to all devices supporting MCI\_SEEK:</span></span>

<dl> <dt>

<span data-ttu-id="c3c5f-124"><span id="MCI_SEEK_TO_END"></span><span id="mci_seek_to_end"></span>MCI \_ 搜尋 \_ \_ 結束</span><span class="sxs-lookup"><span data-stu-id="c3c5f-124"><span id="MCI_SEEK_TO_END"></span><span id="mci_seek_to_end"></span>MCI\_SEEK\_TO\_END</span></span>
</dt> <dd>

<span data-ttu-id="c3c5f-125">搜尋至內容的結尾。</span><span class="sxs-lookup"><span data-stu-id="c3c5f-125">Seek to the end of the content.</span></span>

</dd> <dt>

<span data-ttu-id="c3c5f-126"><span id="MCI_SEEK_TO_START"></span><span id="mci_seek_to_start"></span>MCI \_ 搜尋 \_ \_ 開始</span><span class="sxs-lookup"><span data-stu-id="c3c5f-126"><span id="MCI_SEEK_TO_START"></span><span id="mci_seek_to_start"></span>MCI\_SEEK\_TO\_START</span></span>
</dt> <dd>

<span data-ttu-id="c3c5f-127">搜尋內容的開頭。</span><span class="sxs-lookup"><span data-stu-id="c3c5f-127">Seek to the beginning of the content.</span></span>

</dd> <dt>

<span data-ttu-id="c3c5f-128"><span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ 至</span><span class="sxs-lookup"><span data-stu-id="c3c5f-128"><span id="MCI_TO"></span><span id="mci_to"></span>MCI\_TO</span></span>
</dt> <dd>

<span data-ttu-id="c3c5f-129">位置會包含在 *lpSeek* 所識別之結構的 **dwTo** 成員中。</span><span class="sxs-lookup"><span data-stu-id="c3c5f-129">A position is included in the **dwTo** member of the structure identified by *lpSeek*.</span></span> <span data-ttu-id="c3c5f-130">指派給位置值的單位，會以 Mci 設定的 \_ \_ 時間格式旗標，以 \_ [mci \_ set](mci-set.md) 命令來指定。</span><span class="sxs-lookup"><span data-stu-id="c3c5f-130">The units assigned to the position values are specified with the MCI\_SET\_TIME\_FORMAT flag of the [MCI\_SET](mci-set.md) command.</span></span> <span data-ttu-id="c3c5f-131">請勿使用此旗標，讓 \_ mci \_ 搜尋 \_ 結束或 mci \_ 搜尋 \_ \_ 開始。</span><span class="sxs-lookup"><span data-stu-id="c3c5f-131">Do not use this flag with MCI\_SEEK\_TO\_END or MCI\_SEEK\_TO\_START.</span></span>

</dd> </dl>

<span data-ttu-id="c3c5f-132">下列其他旗標適用于 **vcr** 裝置類型：</span><span class="sxs-lookup"><span data-stu-id="c3c5f-132">The following additional flags are used with the **vcr** device type:</span></span>

<dl> <dt>

<span data-ttu-id="c3c5f-133"><span id="MCI_VCR_SEEK_AT"></span><span id="mci_vcr_seek_at"></span>MCI \_ VCR \_ 搜尋 \_ 位置</span><span class="sxs-lookup"><span data-stu-id="c3c5f-133"><span id="MCI_VCR_SEEK_AT"></span><span id="mci_vcr_seek_at"></span>MCI\_VCR\_SEEK\_AT</span></span>
</dt> <dd>

<span data-ttu-id="c3c5f-134">*LpSeek* 所識別之結構的 **dwAt** 成員，包含整個命令開始的時間。</span><span class="sxs-lookup"><span data-stu-id="c3c5f-134">The **dwAt** member of the structure identified by *lpSeek* contains a time when the entire command begins.</span></span>

</dd> <dt>

<span data-ttu-id="c3c5f-135"><span id="MCI_VCR_SEEK_MARK"></span><span id="mci_vcr_seek_mark"></span>MCI \_ VCR \_ 搜尋 \_ 標記</span><span class="sxs-lookup"><span data-stu-id="c3c5f-135"><span id="MCI_VCR_SEEK_MARK"></span><span id="mci_vcr_seek_mark"></span>MCI\_VCR\_SEEK\_MARK</span></span>
</dt> <dd>

<span data-ttu-id="c3c5f-136">*LpSeek* 所識別之結構的 **dwMark** 成員包含要搜尋的編號標記。</span><span class="sxs-lookup"><span data-stu-id="c3c5f-136">The **dwMark** member of the structure identified by *lpSeek* contains the numbered mark to search for.</span></span>

</dd> <dt>

<span data-ttu-id="c3c5f-137"><span id="MCI_VCR_SEEK_REVERSE"></span><span id="mci_vcr_seek_reverse"></span>MCI \_ VCR \_ 搜尋 \_ 反向</span><span class="sxs-lookup"><span data-stu-id="c3c5f-137"><span id="MCI_VCR_SEEK_REVERSE"></span><span id="mci_vcr_seek_reverse"></span>MCI\_VCR\_SEEK\_REVERSE</span></span>
</dt> <dd>

<span data-ttu-id="c3c5f-138">搜尋方向為反向;這僅適用于 MCI \_ VCR \_ 搜尋 \_ 標記旗標。</span><span class="sxs-lookup"><span data-stu-id="c3c5f-138">Seek direction is reverse; this is used only with the MCI\_VCR\_SEEK\_MARK flag.</span></span>

</dd> </dl>

<span data-ttu-id="c3c5f-139">若為 VCR 裝置， *lpSeek* 參數會指向 [**MCI \_ VCR \_ 搜尋 \_ PARMS**](mci-vcr-seek-parms.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="c3c5f-139">For VCR devices, the *lpSeek* parameter points to an [**MCI\_VCR\_SEEK\_PARMS**](mci-vcr-seek-parms.md) structure.</span></span>

<span data-ttu-id="c3c5f-140">下列其他旗標適用于 **videodisc** 裝置類型：</span><span class="sxs-lookup"><span data-stu-id="c3c5f-140">The following additional flag is used with the **videodisc** device type:</span></span>

<dl> <dt>

<span data-ttu-id="c3c5f-141"><span id="MCI_VD_SEEK_REVERSE"></span><span id="mci_vd_seek_reverse"></span>MCI \_ VD \_ 搜尋 \_ 反向</span><span class="sxs-lookup"><span data-stu-id="c3c5f-141"><span id="MCI_VD_SEEK_REVERSE"></span><span id="mci_vd_seek_reverse"></span>MCI\_VD\_SEEK\_REVERSE</span></span>
</dt> <dd>

<span data-ttu-id="c3c5f-142">搜尋方向為反向。</span><span class="sxs-lookup"><span data-stu-id="c3c5f-142">Seek direction is reverse.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c3c5f-143">規格需求</span><span class="sxs-lookup"><span data-stu-id="c3c5f-143">Requirements</span></span>



| <span data-ttu-id="c3c5f-144">需求</span><span class="sxs-lookup"><span data-stu-id="c3c5f-144">Requirement</span></span> | <span data-ttu-id="c3c5f-145">值</span><span class="sxs-lookup"><span data-stu-id="c3c5f-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3c5f-146">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c3c5f-146">Minimum supported client</span></span><br/> | <span data-ttu-id="c3c5f-147">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c3c5f-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="c3c5f-148">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c3c5f-148">Minimum supported server</span></span><br/> | <span data-ttu-id="c3c5f-149">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c3c5f-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="c3c5f-150">標頭</span><span class="sxs-lookup"><span data-stu-id="c3c5f-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="c3c5f-151"><dt>Mmsystem (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="c3c5f-151"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3c5f-152">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c3c5f-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3c5f-153">Mci</span><span class="sxs-lookup"><span data-stu-id="c3c5f-153">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="c3c5f-154">MCI 命令</span><span class="sxs-lookup"><span data-stu-id="c3c5f-154">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

