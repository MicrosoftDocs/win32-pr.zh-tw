---
title: 'MCI_FREEZE 命令 (Mmsystem .h) '
description: MCI \_ 凍結命令會凍結顯示器上的動作。 數位影片、影片重迭和 VCR 裝置都會辨識此命令。
ms.assetid: 6f90984a-24dc-4046-8234-986b2125bab4
keywords:
- MCI_FREEZE 命令 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_FREEZE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 705117aef85fe69382657c647240849b515afa07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024790"
---
# <a name="mci_freeze-command"></a><span data-ttu-id="900ed-105">MCI \_ 凍結命令</span><span class="sxs-lookup"><span data-stu-id="900ed-105">MCI\_FREEZE command</span></span>

<span data-ttu-id="900ed-106">MCI \_ 凍結命令會凍結顯示器上的動作。</span><span class="sxs-lookup"><span data-stu-id="900ed-106">The MCI\_FREEZE command freezes motion on the display.</span></span> <span data-ttu-id="900ed-107">數位影片、影片重迭和 VCR 裝置都會辨識此命令。</span><span class="sxs-lookup"><span data-stu-id="900ed-107">Digital-video, video-overlay, and VCR devices recognize this command.</span></span>

<span data-ttu-id="900ed-108">若要傳送此命令，請使用下列參數呼叫 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) 函數。</span><span class="sxs-lookup"><span data-stu-id="900ed-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_FREEZE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpFreeze
);
```



## <a name="parameters"></a><span data-ttu-id="900ed-109">參數</span><span class="sxs-lookup"><span data-stu-id="900ed-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="900ed-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="900ed-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="900ed-111">要接收命令訊息之 MCI 裝置的裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="900ed-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="900ed-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="900ed-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="900ed-113">\_ \_ 針對數位-視頻和 VCR 裝置，mci 測試的 mci 通知、mci 等候或 \_ 。</span><span class="sxs-lookup"><span data-stu-id="900ed-113">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video and VCR devices, MCI\_TEST.</span></span> <span data-ttu-id="900ed-114">如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。</span><span class="sxs-lookup"><span data-stu-id="900ed-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="900ed-115"><span id="lpFreeze"></span><span id="lpfreeze"></span><span id="LPFREEZE"></span>*lpFreeze*</span><span class="sxs-lookup"><span data-stu-id="900ed-115"><span id="lpFreeze"></span><span id="lpfreeze"></span><span id="LPFREEZE"></span>*lpFreeze*</span></span>
</dt> <dd>

<span data-ttu-id="900ed-116">[**MCI \_ 泛型 \_ PARMS**](mci-generic-parms.md)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="900ed-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="900ed-117">具有其他參數的 (裝置，可能會以裝置特定結構取代此結構。 ) </span><span class="sxs-lookup"><span data-stu-id="900ed-117">(Devices with additional parameters might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="900ed-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="900ed-118">Return Value</span></span>

<span data-ttu-id="900ed-119">如果成功則傳回零，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="900ed-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="900ed-120">備註</span><span class="sxs-lookup"><span data-stu-id="900ed-120">Remarks</span></span>

<span data-ttu-id="900ed-121">**Digitalvideo** 裝置類型會使用下列其他旗標：</span><span class="sxs-lookup"><span data-stu-id="900ed-121">The following additional flags are used by the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="900ed-122"><span id="MCI_DGV_FREEZE_AT"></span><span id="mci_dgv_freeze_at"></span>MCI \_ DGV \_ 凍結 \_ 于</span><span class="sxs-lookup"><span data-stu-id="900ed-122"><span id="MCI_DGV_FREEZE_AT"></span><span id="mci_dgv_freeze_at"></span>MCI\_DGV\_FREEZE\_AT</span></span>
</dt> <dd>

<span data-ttu-id="900ed-123">*LpFreeze* 所識別之結構的 **rc** 成員包含有效的矩形。</span><span class="sxs-lookup"><span data-stu-id="900ed-123">The **rc** member of the structure identified by *lpFreeze* contains a valid rectangle.</span></span> <span data-ttu-id="900ed-124">矩形會指定框架緩衝區內的區域，以開啟每個圖元的鎖定遮罩位。</span><span class="sxs-lookup"><span data-stu-id="900ed-124">The rectangle specifies a region within the frame buffer that will have the lock mask bit for each pixel turned on.</span></span> <span data-ttu-id="900ed-125">在關閉鎖定遮罩位之前，將不會更新指定的圖元。</span><span class="sxs-lookup"><span data-stu-id="900ed-125">The specified pixels will not be updated until their lock mask bit is turned off.</span></span> <span data-ttu-id="900ed-126">如果未指定此旗標，矩形就會預設為整個框架緩衝區。</span><span class="sxs-lookup"><span data-stu-id="900ed-126">If this flag is not specified, the rectangle defaults to the entire frame buffer.</span></span> <span data-ttu-id="900ed-127">只有當[mci \_ GETDEVCAPS](mci-getdevcaps.md)命令針對 mci  \_ DGV \_ GETDEVCAPS \_ 可鎖定旗標傳回 TRUE 時，才支援此旗標 \_ 。</span><span class="sxs-lookup"><span data-stu-id="900ed-127">This flag is supported only if the [MCI\_GETDEVCAPS](mci-getdevcaps.md) command returns **TRUE** for the MCI\_DGV\_GETDEVCAPS\_CAN\_LOCK flag.</span></span>

</dd> <dt>

<span data-ttu-id="900ed-128"><span id="MCI_DGV_FREEZE_OUTSIDE"></span><span id="mci_dgv_freeze_outside"></span>MCI \_ DGV \_ 凍結 \_</span><span class="sxs-lookup"><span data-stu-id="900ed-128"><span id="MCI_DGV_FREEZE_OUTSIDE"></span><span id="mci_dgv_freeze_outside"></span>MCI\_DGV\_FREEZE\_OUTSIDE</span></span>
</dt> <dd>

<span data-ttu-id="900ed-129">在旗標上為 MCI DGV 凍結指定的區域以外的區域 \_ \_ \_ 已凍結。</span><span class="sxs-lookup"><span data-stu-id="900ed-129">The area outside the region specified for the MCI\_DGV\_FREEZE\_AT flag is frozen.</span></span>

</dd> </dl>

<span data-ttu-id="900ed-130">針對數位影片裝置， *lpFreeze* 參數會指向 [**MCI \_ DGV \_ 凍結 \_ PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_rect_parms) 結構。</span><span class="sxs-lookup"><span data-stu-id="900ed-130">For digital-video devices, the *lpFreeze* parameter points to an [**MCI\_DGV\_FREEZE\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_rect_parms) structure.</span></span>

<span data-ttu-id="900ed-131">**Vcr** 裝置類型會使用下列其他旗標：</span><span class="sxs-lookup"><span data-stu-id="900ed-131">The following additional flags are used by the **vcr** device type:</span></span>

<dl> <dt>

<span data-ttu-id="900ed-132"><span id="MCI_VCR_FREEZE_FIELD"></span><span id="mci_vcr_freeze_field"></span>MCI \_ VCR \_ 凍結 \_ 欄位</span><span class="sxs-lookup"><span data-stu-id="900ed-132"><span id="MCI_VCR_FREEZE_FIELD"></span><span id="mci_vcr_freeze_field"></span>MCI\_VCR\_FREEZE\_FIELD</span></span>
</dt> <dd>

<span data-ttu-id="900ed-133">只凍結目前框架的一個成員。</span><span class="sxs-lookup"><span data-stu-id="900ed-133">Freeze only one member of the current frame.</span></span>

</dd> <dt>

<span data-ttu-id="900ed-134"><span id="MCI_VCR_FREEZE_FRAME"></span><span id="mci_vcr_freeze_frame"></span>MCI \_ VCR \_ 凍結 \_ 框架</span><span class="sxs-lookup"><span data-stu-id="900ed-134"><span id="MCI_VCR_FREEZE_FRAME"></span><span id="mci_vcr_freeze_frame"></span>MCI\_VCR\_FREEZE\_FRAME</span></span>
</dt> <dd>

<span data-ttu-id="900ed-135">凍結目前框架的兩個欄位。</span><span class="sxs-lookup"><span data-stu-id="900ed-135">Freeze both fields of the current frame.</span></span>

</dd> <dt>

<span data-ttu-id="900ed-136"><span id="MCI_VCR_FREEZE_INPUT"></span><span id="mci_vcr_freeze_input"></span>MCI \_ VCR \_ 凍結 \_ 輸入</span><span class="sxs-lookup"><span data-stu-id="900ed-136"><span id="MCI_VCR_FREEZE_INPUT"></span><span id="mci_vcr_freeze_input"></span>MCI\_VCR\_FREEZE\_INPUT</span></span>
</dt> <dd>

<span data-ttu-id="900ed-137">凍結螢幕上的目前畫面格 (用於錄製) 。</span><span class="sxs-lookup"><span data-stu-id="900ed-137">Freeze the current frame on the screen (used for recording).</span></span>

</dd> <dt>

<span data-ttu-id="900ed-138"><span id="MCI_VCR_FREEZE_OUTPUT"></span><span id="mci_vcr_freeze_output"></span>MCI \_ VCR \_ 凍結 \_ 輸出</span><span class="sxs-lookup"><span data-stu-id="900ed-138"><span id="MCI_VCR_FREEZE_OUTPUT"></span><span id="mci_vcr_freeze_output"></span>MCI\_VCR\_FREEZE\_OUTPUT</span></span>
</dt> <dd>

<span data-ttu-id="900ed-139">從 VCR (中，凍結框架捕獲) 所用的目前畫面格。</span><span class="sxs-lookup"><span data-stu-id="900ed-139">Freeze the current frame from the VCR (used with frame capture).</span></span>

</dd> </dl>

<span data-ttu-id="900ed-140">若為 VCR 裝置， *lpFreeze* 參數會指向 [**MCI \_ 一般 \_ PARMS**](mci-generic-parms.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="900ed-140">For VCR devices, the *lpFreeze* parameter points to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span>

<span data-ttu-id="900ed-141">覆 **迭裝置類型** 會使用下列其他旗標：</span><span class="sxs-lookup"><span data-stu-id="900ed-141">The following additional flag is used by the **overlay** device type:</span></span>

<dl> <dt>

<span data-ttu-id="900ed-142"><span id="MCI_OVLY_RECT"></span><span id="mci_ovly_rect"></span>MCI \_ OVLY \_ RECT</span><span class="sxs-lookup"><span data-stu-id="900ed-142"><span id="MCI_OVLY_RECT"></span><span id="mci_ovly_rect"></span>MCI\_OVLY\_RECT</span></span>
</dt> <dd>

<span data-ttu-id="900ed-143">*LpFreeze* 所識別之結構的 **rc** 成員包含有效的矩形。</span><span class="sxs-lookup"><span data-stu-id="900ed-143">The **rc** member of the structure identified by *lpFreeze* contains a valid rectangle.</span></span> <span data-ttu-id="900ed-144">如果未指定此旗標，設備磁碟機將會凍結整個框架。</span><span class="sxs-lookup"><span data-stu-id="900ed-144">If this flag is not specified, the device driver will freeze the entire frame.</span></span>

</dd> </dl>

<span data-ttu-id="900ed-145">針對影片重迭裝置， *lpFreeze* 參數會指向 [**MCI \_ OVLY \_ RECT \_ PARMS**](mci-ovly-rect-parms.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="900ed-145">For video-overlay devices, the *lpFreeze* parameter points to an [**MCI\_OVLY\_RECT\_PARMS**](mci-ovly-rect-parms.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="900ed-146">規格需求</span><span class="sxs-lookup"><span data-stu-id="900ed-146">Requirements</span></span>



| <span data-ttu-id="900ed-147">需求</span><span class="sxs-lookup"><span data-stu-id="900ed-147">Requirement</span></span> | <span data-ttu-id="900ed-148">值</span><span class="sxs-lookup"><span data-stu-id="900ed-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="900ed-149">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="900ed-149">Minimum supported client</span></span><br/> | <span data-ttu-id="900ed-150">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="900ed-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="900ed-151">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="900ed-151">Minimum supported server</span></span><br/> | <span data-ttu-id="900ed-152">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="900ed-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="900ed-153">標頭</span><span class="sxs-lookup"><span data-stu-id="900ed-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="900ed-154"><dt>Mmsystem (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="900ed-154"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="900ed-155">另請參閱</span><span class="sxs-lookup"><span data-stu-id="900ed-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="900ed-156">Mci</span><span class="sxs-lookup"><span data-stu-id="900ed-156">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="900ed-157">MCI 命令</span><span class="sxs-lookup"><span data-stu-id="900ed-157">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

