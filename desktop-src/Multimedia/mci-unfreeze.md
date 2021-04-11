---
title: 'MCI_UNFREEZE 命令 (Mmsystem .h) '
description: MCI \_ 解除凍結命令會將動作還原至視訊緩衝區的區域，並透過 MCI \_ 凍結命令加以凍結。 數位影片、VCR 和影片重迭裝置會辨識此命令。
ms.assetid: 79ff1be5-6e30-4ef4-ab81-fc5643e3a72d
keywords:
- MCI_UNFREEZE 命令 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_UNFREEZE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8736e27998330f9337bb21569e145a4395e90020
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105912"
---
# <a name="mci_unfreeze-command"></a><span data-ttu-id="5c78f-105">MCI \_ 解除凍結命令</span><span class="sxs-lookup"><span data-stu-id="5c78f-105">MCI\_UNFREEZE command</span></span>

<span data-ttu-id="5c78f-106">MCI \_ 解除凍結命令會將動作還原至視訊緩衝區的區域，並透過 [MCI \_ 凍結](mci-freeze.md) 命令加以凍結。</span><span class="sxs-lookup"><span data-stu-id="5c78f-106">The MCI\_UNFREEZE command restores motion to an area of the video buffer frozen with the [MCI\_FREEZE](mci-freeze.md) command.</span></span> <span data-ttu-id="5c78f-107">數位影片、VCR 和影片重迭裝置會辨識此命令。</span><span class="sxs-lookup"><span data-stu-id="5c78f-107">Digital-video, VCR, and video-overlay devices recognize this command.</span></span>

<span data-ttu-id="5c78f-108">若要傳送此命令，請使用下列參數呼叫 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) 函數。</span><span class="sxs-lookup"><span data-stu-id="5c78f-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_UNFREEZE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpUnfreeze
);
```



## <a name="parameters"></a><span data-ttu-id="5c78f-109">參數</span><span class="sxs-lookup"><span data-stu-id="5c78f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c78f-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="5c78f-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="5c78f-111">要接收命令訊息之 MCI 裝置的裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="5c78f-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="5c78f-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="5c78f-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="5c78f-113">\_ \_ 針對數位-視頻和 VCR 裝置，mci 測試的 mci 通知、mci 等候或 \_ 。</span><span class="sxs-lookup"><span data-stu-id="5c78f-113">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video and VCR devices, MCI\_TEST.</span></span> <span data-ttu-id="5c78f-114">如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。</span><span class="sxs-lookup"><span data-stu-id="5c78f-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="5c78f-115"><span id="lpUnfreeze"></span><span id="lpunfreeze"></span><span id="LPUNFREEZE"></span>*lpUnfreeze*</span><span class="sxs-lookup"><span data-stu-id="5c78f-115"><span id="lpUnfreeze"></span><span id="lpunfreeze"></span><span id="LPUNFREEZE"></span>*lpUnfreeze*</span></span>
</dt> <dd>

<span data-ttu-id="5c78f-116">[**MCI \_ 泛型 \_ PARMS**](mci-generic-parms.md)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="5c78f-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="5c78f-117">具有擴充命令集的 (裝置，可能會以裝置特定結構取代此結構。 ) </span><span class="sxs-lookup"><span data-stu-id="5c78f-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c78f-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="5c78f-118">Return Value</span></span>

<span data-ttu-id="5c78f-119">如果成功則傳回零，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="5c78f-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="5c78f-120">備註</span><span class="sxs-lookup"><span data-stu-id="5c78f-120">Remarks</span></span>

<span data-ttu-id="5c78f-121">下列其他旗標適用于 **digitalvideo** 裝置類型：</span><span class="sxs-lookup"><span data-stu-id="5c78f-121">The following additional flag is used with the **digitalvideo** device type:</span></span>

<span data-ttu-id="5c78f-122">MCI \_ DGV \_ RECT</span><span class="sxs-lookup"><span data-stu-id="5c78f-122">MCI\_DGV\_RECT</span></span>

<span data-ttu-id="5c78f-123">*LpUnfreeze* 所識別之結構的 **rc** 成員包含有效的顯示矩形。</span><span class="sxs-lookup"><span data-stu-id="5c78f-123">The **rc** member of the structure identified by *lpUnfreeze* contains a valid display rectangle.</span></span> <span data-ttu-id="5c78f-124">矩形會指定框架緩衝區內的區域，其圖元應關閉其鎖定遮罩位。</span><span class="sxs-lookup"><span data-stu-id="5c78f-124">The rectangle specifies a region within the frame buffer whose pixels should have their lock mask bit turned off.</span></span> <span data-ttu-id="5c78f-125">系統會依照 [MCI \_ PUT](mci-put.md) 命令的說明指定矩形區域。</span><span class="sxs-lookup"><span data-stu-id="5c78f-125">Rectangular regions are specified as described for the [MCI\_PUT](mci-put.md) command.</span></span> <span data-ttu-id="5c78f-126">如果省略，矩形就會預設為整個框架緩衝區。</span><span class="sxs-lookup"><span data-stu-id="5c78f-126">If omitted, the rectangle defaults to the entire frame buffer.</span></span> <span data-ttu-id="5c78f-127">藉由使用一系列的凍結並解除凍結具有不同矩形的命令，即可描述鎖定遮罩位的任意模式。</span><span class="sxs-lookup"><span data-stu-id="5c78f-127">By using a sequence of freeze and unfreeze commands with different rectangles, arbitrary patterns of lock mask bits can be described.</span></span>

<span data-ttu-id="5c78f-128">針對數位影片裝置， *lpUnfreeze* 參數會指向 **MCI DGV，以 \_ \_ 解除凍結 \_ PARMS** 結構。</span><span class="sxs-lookup"><span data-stu-id="5c78f-128">For digital-video devices, the *lpUnfreeze* parameter points to an **MCI\_DGV\_UNFREEZE\_PARMS** structure.</span></span> <span data-ttu-id="5c78f-129">如需詳細資訊，請參閱 [**MCI \_ DGV \_ RECT \_ PARMS**](/windows/win32/api/digitalv/ns-digitalv-mci_dgv_rect_parms) 結構的批註。</span><span class="sxs-lookup"><span data-stu-id="5c78f-129">For more information, see the comments for the [**MCI\_DGV\_RECT\_PARMS**](/windows/win32/api/digitalv/ns-digitalv-mci_dgv_rect_parms) structure.</span></span>

<span data-ttu-id="5c78f-130">下列其他旗標適用于 **vcr** 裝置類型：</span><span class="sxs-lookup"><span data-stu-id="5c78f-130">The following additional flags are used with the **vcr** device type:</span></span>

<dl> <dt>

<span data-ttu-id="5c78f-131"><span id="MCI_VCR_UNFREEZE_INPUT"></span><span id="mci_vcr_unfreeze_input"></span>MCI \_ VCR \_ 解除凍結 \_ 輸入</span><span class="sxs-lookup"><span data-stu-id="5c78f-131"><span id="MCI_VCR_UNFREEZE_INPUT"></span><span id="mci_vcr_unfreeze_input"></span>MCI\_VCR\_UNFREEZE\_INPUT</span></span>
</dt> <dd>

<span data-ttu-id="5c78f-132">解除凍結輸入。</span><span class="sxs-lookup"><span data-stu-id="5c78f-132">Unfreeze the input.</span></span>

</dd> <dt>

<span data-ttu-id="5c78f-133"><span id="MCI_VCR_UNFREEZE_OUTPUT"></span><span id="mci_vcr_unfreeze_output"></span>MCI \_ VCR \_ 解除凍結 \_ 輸出</span><span class="sxs-lookup"><span data-stu-id="5c78f-133"><span id="MCI_VCR_UNFREEZE_OUTPUT"></span><span id="mci_vcr_unfreeze_output"></span>MCI\_VCR\_UNFREEZE\_OUTPUT</span></span>
</dt> <dd>

<span data-ttu-id="5c78f-134">解除凍結輸出。</span><span class="sxs-lookup"><span data-stu-id="5c78f-134">Unfreeze the output.</span></span>

</dd> </dl>

<span data-ttu-id="5c78f-135">下列其他旗標會搭配覆迭 **裝置類型** 使用：</span><span class="sxs-lookup"><span data-stu-id="5c78f-135">The following additional flag is used with the **overlay** device type:</span></span>

<dl> <dt>

<span data-ttu-id="5c78f-136"><span id="MCI_OVLY_RECT"></span><span id="mci_ovly_rect"></span>MCI \_ OVLY \_ RECT</span><span class="sxs-lookup"><span data-stu-id="5c78f-136"><span id="MCI_OVLY_RECT"></span><span id="mci_ovly_rect"></span>MCI\_OVLY\_RECT</span></span>
</dt> <dd>

<span data-ttu-id="5c78f-137">*LpUnfreeze* 所識別之結構的 **rc** 成員包含有效的顯示矩形。</span><span class="sxs-lookup"><span data-stu-id="5c78f-137">The **rc** member of the structure identified by *lpUnfreeze* contains a valid display rectangle.</span></span> <span data-ttu-id="5c78f-138">這是必要參數。</span><span class="sxs-lookup"><span data-stu-id="5c78f-138">This is a required parameter.</span></span>

</dd> </dl>

<span data-ttu-id="5c78f-139">針對影片重迭裝置， *lpUnfreeze* 參數會指向 [**MCI \_ OVLY \_ RECT \_ PARMS**](mci-ovly-rect-parms.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="5c78f-139">For video-overlay devices, the *lpUnfreeze* parameter points to an [**MCI\_OVLY\_RECT\_PARMS**](mci-ovly-rect-parms.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c78f-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="5c78f-140">Requirements</span></span>



| <span data-ttu-id="5c78f-141">需求</span><span class="sxs-lookup"><span data-stu-id="5c78f-141">Requirement</span></span> | <span data-ttu-id="5c78f-142">值</span><span class="sxs-lookup"><span data-stu-id="5c78f-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c78f-143">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5c78f-143">Minimum supported client</span></span><br/> | <span data-ttu-id="5c78f-144">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5c78f-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="5c78f-145">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5c78f-145">Minimum supported server</span></span><br/> | <span data-ttu-id="5c78f-146">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5c78f-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="5c78f-147">標頭</span><span class="sxs-lookup"><span data-stu-id="5c78f-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="5c78f-148"><dt>Mmsystem (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="5c78f-148"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c78f-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5c78f-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c78f-150">Mci</span><span class="sxs-lookup"><span data-stu-id="5c78f-150">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="5c78f-151">MCI 命令</span><span class="sxs-lookup"><span data-stu-id="5c78f-151">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

