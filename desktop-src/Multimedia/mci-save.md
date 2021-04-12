---
title: 'MCI_SAVE 命令 (Mmsystem .h) '
description: MCI \_ SAVE 命令會儲存目前的檔案。
ms.assetid: 286e6f31-cb93-443b-8191-8c363b366eae
keywords:
- MCI_SAVE 命令 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_SAVE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a241c0379731e870940cd676c33ae192efc5d297
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464625"
---
# <a name="mci_save-command"></a><span data-ttu-id="b771f-104">MCI \_ 儲存命令</span><span class="sxs-lookup"><span data-stu-id="b771f-104">MCI\_SAVE command</span></span>

<span data-ttu-id="b771f-105">MCI \_ SAVE 命令會儲存目前的檔案。</span><span class="sxs-lookup"><span data-stu-id="b771f-105">The MCI\_SAVE command saves the current file.</span></span> <span data-ttu-id="b771f-106">修改檔案的裝置在收到儲存訊息之前，不應終結原始複本。</span><span class="sxs-lookup"><span data-stu-id="b771f-106">Devices that modify files should not destroy the original copy until they receive the save message.</span></span> <span data-ttu-id="b771f-107">影片-重迭和波形-音訊裝置會辨識此命令。</span><span class="sxs-lookup"><span data-stu-id="b771f-107">Video-overlay and waveform-audio devices recognize this command.</span></span> <span data-ttu-id="b771f-108">雖然數位視訊裝置和 MIDI sequencers 也會辨識此命令，但 MCIAVI 和 MCISEQ 驅動程式並不會執行此命令。</span><span class="sxs-lookup"><span data-stu-id="b771f-108">Although digital-video devices and MIDI sequencers also recognize this command, the MCIAVI and MCISEQ drivers do not implement it.</span></span>

<span data-ttu-id="b771f-109">若要傳送此命令，請使用下列參數呼叫 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) 函數。</span><span class="sxs-lookup"><span data-stu-id="b771f-109">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SAVE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_SAVE_PARMS ) lpSave
);
```



## <a name="parameters"></a><span data-ttu-id="b771f-110">參數</span><span class="sxs-lookup"><span data-stu-id="b771f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b771f-111"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="b771f-111"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="b771f-112">要接收命令訊息之 MCI 裝置的裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="b771f-112">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="b771f-113"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="b771f-113"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="b771f-114">\_ \_ 針對數位-視頻和 VCR 裝置，mci 測試的 mci 通知、mci 等候或 \_ 。</span><span class="sxs-lookup"><span data-stu-id="b771f-114">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video and VCR devices, MCI\_TEST.</span></span> <span data-ttu-id="b771f-115">如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。</span><span class="sxs-lookup"><span data-stu-id="b771f-115">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="b771f-116"><span id="lpSave"></span><span id="lpsave"></span><span id="LPSAVE"></span>*lpSave*</span><span class="sxs-lookup"><span data-stu-id="b771f-116"><span id="lpSave"></span><span id="lpsave"></span><span id="LPSAVE"></span>*lpSave*</span></span>
</dt> <dd>

<span data-ttu-id="b771f-117">[**MCI \_ 儲存 \_ PARMS**](mci-save-parms.md)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="b771f-117">Pointer to an [**MCI\_SAVE\_PARMS**](mci-save-parms.md) structure.</span></span> <span data-ttu-id="b771f-118">具有其他參數的 (裝置，可能會以裝置特定結構取代此結構。 ) </span><span class="sxs-lookup"><span data-stu-id="b771f-118">(Devices with additional parameters might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b771f-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="b771f-119">Return Value</span></span>

<span data-ttu-id="b771f-120">如果成功則傳回零，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="b771f-120">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="b771f-121">備註</span><span class="sxs-lookup"><span data-stu-id="b771f-121">Remarks</span></span>

<span data-ttu-id="b771f-122">當您使用 MCI  GETDEVCAPS 可以[ \_ ](mci-getdevcaps.md) \_ \_ \_ 儲存旗標來呼叫 mci GETDEVCAPS 命令時，會傳回 TRUE 的裝置支援此命令。</span><span class="sxs-lookup"><span data-stu-id="b771f-122">This command is supported by devices that return **TRUE** when you call the [MCI\_GETDEVCAPS](mci-getdevcaps.md) command with the MCI\_GETDEVCAPS\_CAN\_SAVE flag.</span></span>

<span data-ttu-id="b771f-123">下列其他旗標適用于所有支援 [MCI \_ 儲存](/windows)的裝置：</span><span class="sxs-lookup"><span data-stu-id="b771f-123">The following additional flag applies to all devices supporting [MCI\_SAVE](/windows):</span></span>

<dl> <dt>

<span data-ttu-id="b771f-124"><span id="MCI_SAVE_FILE"></span><span id="mci_save_file"></span>MCI \_ 儲存檔案 \_</span><span class="sxs-lookup"><span data-stu-id="b771f-124"><span id="MCI_SAVE_FILE"></span><span id="mci_save_file"></span>MCI\_SAVE\_FILE</span></span>
</dt> <dd>

<span data-ttu-id="b771f-125">*LpSave* 所識別之結構的 **lpfilename** 成員包含包含目的地檔案名之緩衝區的位址。</span><span class="sxs-lookup"><span data-stu-id="b771f-125">The **lpfilename** member of the structure identified by *lpSave* contains an address of a buffer containing the destination filename.</span></span>

</dd> </dl>

<span data-ttu-id="b771f-126">下列其他旗標適用于 **digitalvideo** 裝置類型：</span><span class="sxs-lookup"><span data-stu-id="b771f-126">The following additional flags are used with the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="b771f-127"><span id="MCI_DGV_RECT"></span><span id="mci_dgv_rect"></span>MCI \_ DGV \_ RECT</span><span class="sxs-lookup"><span data-stu-id="b771f-127"><span id="MCI_DGV_RECT"></span><span id="mci_dgv_rect"></span>MCI\_DGV\_RECT</span></span>
</dt> <dd>

<span data-ttu-id="b771f-128">*LpSave* 所識別之結構的 **rc** 成員包含有效的矩形。</span><span class="sxs-lookup"><span data-stu-id="b771f-128">The **rc** member of the structure identified by *lpSave* contains a valid rectangle.</span></span> <span data-ttu-id="b771f-129">矩形會指定將儲存到指定檔案的框架緩衝區區域。</span><span class="sxs-lookup"><span data-stu-id="b771f-129">The rectangle specifies a region of the frame buffer that will be saved to the specified file.</span></span> <span data-ttu-id="b771f-130">第一對座標指定矩形的左上角;第二個配對指定寬度和高度。</span><span class="sxs-lookup"><span data-stu-id="b771f-130">The first pair of coordinates specifies the upper left corner of the rectangle; the second pair specifies the width and height.</span></span> <span data-ttu-id="b771f-131">數位視訊裝置必須使用 [MCI \_ capture](mci-capture.md) 命令來捕獲框架緩衝區的內容。</span><span class="sxs-lookup"><span data-stu-id="b771f-131">Digital-video devices must use the [MCI\_CAPTURE](mci-capture.md) command to capture the contents of the frame buffer.</span></span> <span data-ttu-id="b771f-132"> (的影片重迭裝置也應使用 MCI \_ CAPTURE。 ) 此旗標是為了與現有的 MCI 影片重迭命令集相容。</span><span class="sxs-lookup"><span data-stu-id="b771f-132">(Video-overlay devices should also use MCI\_CAPTURE.) This flag is for compatibility with the existing MCI video-overlay command set.</span></span>

</dd> <dt>

<span data-ttu-id="b771f-133"><span id="MCI_DGV_SAVE_ABORT"></span><span id="mci_dgv_save_abort"></span>MCI \_ DGV \_ 儲存 \_ 中止</span><span class="sxs-lookup"><span data-stu-id="b771f-133"><span id="MCI_DGV_SAVE_ABORT"></span><span id="mci_dgv_save_abort"></span>MCI\_DGV\_SAVE\_ABORT</span></span>
</dt> <dd>

<span data-ttu-id="b771f-134">停止進行中的儲存作業。</span><span class="sxs-lookup"><span data-stu-id="b771f-134">Stops a save operation in progress.</span></span> <span data-ttu-id="b771f-135">這必須是唯一的旗標。</span><span class="sxs-lookup"><span data-stu-id="b771f-135">This must be the only flag present.</span></span>

</dd> <dt>

<span data-ttu-id="b771f-136"><span id="MCI_DGV_SAVE_KEEPRESERVE"></span><span id="mci_dgv_save_keepreserve"></span>MCI \_ DGV \_ 儲存 \_ KEEPRESERVE</span><span class="sxs-lookup"><span data-stu-id="b771f-136"><span id="MCI_DGV_SAVE_KEEPRESERVE"></span><span id="mci_dgv_save_keepreserve"></span>MCI\_DGV\_SAVE\_KEEPRESERVE</span></span>
</dt> <dd>

<span data-ttu-id="b771f-137">未解除配置原始 [MCI \_ 保留](mci-reserve.md) 命令剩餘的未使用磁碟空間。</span><span class="sxs-lookup"><span data-stu-id="b771f-137">Unused disk space left over from the original [MCI\_RESERVE](mci-reserve.md) command is not deallocated.</span></span>

</dd> </dl>

<span data-ttu-id="b771f-138">針對數位影片裝置， *lpSave* 參數會指向 [**MCI \_ DGV \_ 儲存 \_ PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_save_parmsa) 結構。</span><span class="sxs-lookup"><span data-stu-id="b771f-138">For digital-video devices, the *lpSave* parameter points to an [**MCI\_DGV\_SAVE\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_save_parmsa) structure.</span></span>

<span data-ttu-id="b771f-139">下列其他旗標會搭配覆迭 **裝置類型** 使用：</span><span class="sxs-lookup"><span data-stu-id="b771f-139">The following additional flag is used with the **overlay** device type:</span></span>

<dl> <dt>

<span data-ttu-id="b771f-140"><span id="MCI_OVLY_RECT"></span><span id="mci_ovly_rect"></span>MCI \_ OVLY \_ RECT</span><span class="sxs-lookup"><span data-stu-id="b771f-140"><span id="MCI_OVLY_RECT"></span><span id="mci_ovly_rect"></span>MCI\_OVLY\_RECT</span></span>
</dt> <dd>

<span data-ttu-id="b771f-141">*LpSave* 所識別之結構的 **rc** 成員包含有效的顯示矩形，指出要儲存的影片緩衝區區域。</span><span class="sxs-lookup"><span data-stu-id="b771f-141">The **rc** member of the structure identified by *lpSave* contains a valid display rectangle indicating the area of the video buffer to save.</span></span>

</dd> </dl>

<span data-ttu-id="b771f-142">針對影片重迭裝置， *lpSave* 參數會指向 [**MCI \_ OVLY \_ 儲存 \_ PARMS**](/previous-versions//dd743447(v=vs.85)) 結構。</span><span class="sxs-lookup"><span data-stu-id="b771f-142">For video-overlay devices, the *lpSave* parameter points to an [**MCI\_OVLY\_SAVE\_PARMS**](/previous-versions//dd743447(v=vs.85)) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="b771f-143">規格需求</span><span class="sxs-lookup"><span data-stu-id="b771f-143">Requirements</span></span>



| <span data-ttu-id="b771f-144">需求</span><span class="sxs-lookup"><span data-stu-id="b771f-144">Requirement</span></span> | <span data-ttu-id="b771f-145">值</span><span class="sxs-lookup"><span data-stu-id="b771f-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b771f-146">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b771f-146">Minimum supported client</span></span><br/> | <span data-ttu-id="b771f-147">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b771f-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="b771f-148">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b771f-148">Minimum supported server</span></span><br/> | <span data-ttu-id="b771f-149">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b771f-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="b771f-150">標頭</span><span class="sxs-lookup"><span data-stu-id="b771f-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="b771f-151"><dt>Mmsystem (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="b771f-151"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b771f-152">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b771f-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b771f-153">Mci</span><span class="sxs-lookup"><span data-stu-id="b771f-153">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="b771f-154">MCI 命令</span><span class="sxs-lookup"><span data-stu-id="b771f-154">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

