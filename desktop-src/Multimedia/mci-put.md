---
title: 'MCI_PUT 命令 (Mmsystem .h) '
description: MCI \_ PUT 命令會設定來源、目的地和框架矩形。 數位影片和影片重迭裝置會辨識此命令。
ms.assetid: 9d81682b-6546-4e6d-a6df-e2de8c013b66
keywords:
- MCI_PUT 命令 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_PUT
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8fa4af30aa2b3aa6f7cdd50f453bc8edca83334
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106536"
---
# <a name="mci_put-command"></a><span data-ttu-id="58212-105">MCI \_ PUT 命令</span><span class="sxs-lookup"><span data-stu-id="58212-105">MCI\_PUT command</span></span>

<span data-ttu-id="58212-106">MCI \_ PUT 命令會設定來源、目的地和框架矩形。</span><span class="sxs-lookup"><span data-stu-id="58212-106">The MCI\_PUT command sets the source, destination, and frame rectangles.</span></span> <span data-ttu-id="58212-107">數位影片和影片重迭裝置會辨識此命令。</span><span class="sxs-lookup"><span data-stu-id="58212-107">Digital-video and video-overlay devices recognize this command.</span></span>

<span data-ttu-id="58212-108">若要傳送此命令，請使用下列參數呼叫 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) 函數。</span><span class="sxs-lookup"><span data-stu-id="58212-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_PUT, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpDest
);
```



## <a name="parameters"></a><span data-ttu-id="58212-109">參數</span><span class="sxs-lookup"><span data-stu-id="58212-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58212-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="58212-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="58212-111">要接收命令訊息之 MCI 裝置的裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="58212-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="58212-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="58212-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="58212-113">\_ \_ 適用于數位視訊裝置、mci 測試的 mci 通知、mci 等待或 \_ 。</span><span class="sxs-lookup"><span data-stu-id="58212-113">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video devices, MCI\_TEST.</span></span> <span data-ttu-id="58212-114">如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。</span><span class="sxs-lookup"><span data-stu-id="58212-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="58212-115"><span id="lpDest"></span><span id="lpdest"></span><span id="LPDEST"></span>*lpDest*</span><span class="sxs-lookup"><span data-stu-id="58212-115"><span id="lpDest"></span><span id="lpdest"></span><span id="LPDEST"></span>*lpDest*</span></span>
</dt> <dd>

<span data-ttu-id="58212-116">[**MCI \_ 泛型 \_ PARMS**](mci-generic-parms.md)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="58212-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="58212-117">具有擴充命令集的 (裝置，可能會以裝置特定結構取代此結構。 ) </span><span class="sxs-lookup"><span data-stu-id="58212-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58212-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="58212-118">Return Value</span></span>

<span data-ttu-id="58212-119">如果成功則傳回零，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="58212-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="58212-120">備註</span><span class="sxs-lookup"><span data-stu-id="58212-120">Remarks</span></span>

<span data-ttu-id="58212-121">下列其他旗標適用于 **digitalvideo** 裝置類型：</span><span class="sxs-lookup"><span data-stu-id="58212-121">The following additional flags are used with the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="58212-122"><span id="MCI_DGV_PUT_CLIENT"></span><span id="mci_dgv_put_client"></span>MCI \_ DGV \_ PUT \_ 用戶端</span><span class="sxs-lookup"><span data-stu-id="58212-122"><span id="MCI_DGV_PUT_CLIENT"></span><span id="mci_dgv_put_client"></span>MCI\_DGV\_PUT\_CLIENT</span></span>
</dt> <dd>

<span data-ttu-id="58212-123">針對 MCI DGV RECT 定義的矩形會 \_ \_ 套用至用戶端視窗的位置。</span><span class="sxs-lookup"><span data-stu-id="58212-123">The rectangle defined for MCI\_DGV\_RECT applies to the position of the client window.</span></span> <span data-ttu-id="58212-124">指定的矩形是相對於顯示視窗的父視窗。</span><span class="sxs-lookup"><span data-stu-id="58212-124">The rectangle specified is relative to the parent window of the display window.</span></span> <span data-ttu-id="58212-125">您 \_ \_ \_ 必須使用此旗標同時設定 MCI DGV PUT 視窗。</span><span class="sxs-lookup"><span data-stu-id="58212-125">MCI\_DGV\_PUT\_WINDOW must be set concurrently with this flag.</span></span>

</dd> <dt>

<span data-ttu-id="58212-126"><span id="MCI_DGV_PUT_DESTINATION"></span><span id="mci_dgv_put_destination"></span>MCI \_ DGV \_ PUT \_ DESTINATION</span><span class="sxs-lookup"><span data-stu-id="58212-126"><span id="MCI_DGV_PUT_DESTINATION"></span><span id="mci_dgv_put_destination"></span>MCI\_DGV\_PUT\_DESTINATION</span></span>
</dt> <dd>

<span data-ttu-id="58212-127">針對 MCI DGV RECT 定義的矩形會 \_ \_ 指定目的地矩形。</span><span class="sxs-lookup"><span data-stu-id="58212-127">The rectangle defined for MCI\_DGV\_RECT specifies a destination rectangle.</span></span> <span data-ttu-id="58212-128">目的地矩形會指定與此設備磁碟機實例相關聯的用戶端視窗部分，以顯示影像或影片。</span><span class="sxs-lookup"><span data-stu-id="58212-128">The destination rectangle specifies the portion of the client window associated with this device driver instance that shows the image or video.</span></span>

</dd> <dt>

<span data-ttu-id="58212-129"><span id="MCI_DGV_PUT_FRAME"></span><span id="mci_dgv_put_frame"></span>MCI \_ DGV \_ PUT \_ FRAME</span><span class="sxs-lookup"><span data-stu-id="58212-129"><span id="MCI_DGV_PUT_FRAME"></span><span id="mci_dgv_put_frame"></span>MCI\_DGV\_PUT\_FRAME</span></span>
</dt> <dd>

<span data-ttu-id="58212-130">針對 MCI DGV RECT 定義的矩形會 \_ \_ 套用至框架矩形。</span><span class="sxs-lookup"><span data-stu-id="58212-130">The rectangle defined for MCI\_DGV\_RECT applies to the frame rectangle.</span></span> <span data-ttu-id="58212-131">框架矩形會指定框架緩衝區的部分，作為從影片矩形取得之影片影像的目的地。</span><span class="sxs-lookup"><span data-stu-id="58212-131">The frame rectangle specifies the portion of the frame buffer used as the destination of the video images obtained from the video rectangle.</span></span> <span data-ttu-id="58212-132">影片應該調整以符合框架緩衝區矩形。</span><span class="sxs-lookup"><span data-stu-id="58212-132">The video should be scaled to fit within the frame buffer rectangle.</span></span>

<span data-ttu-id="58212-133">矩形是在框架緩衝區座標中指定。</span><span class="sxs-lookup"><span data-stu-id="58212-133">The rectangle is specified in frame buffer coordinates.</span></span> <span data-ttu-id="58212-134">預設的矩形是完整的框架緩衝區。</span><span class="sxs-lookup"><span data-stu-id="58212-134">The default rectangle is the full frame buffer.</span></span> <span data-ttu-id="58212-135">指定此矩形可讓裝置在 digitizes 資料時調整影像。</span><span class="sxs-lookup"><span data-stu-id="58212-135">Specifying this rectangle lets the device scale the image as it digitizes the data.</span></span> <span data-ttu-id="58212-136">無法調整映射的裝置會使用 MCIERR 不支援的功能來拒絕此命令 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="58212-136">Devices that cannot scale the image reject this command with MCIERR\_UNSUPPORTED\_FUNCTION.</span></span> <span data-ttu-id="58212-137">您可以使用 MCI \_ GETDEVCAPS \_ 來 \_ 延展旗標與 [mci \_ GETDEVCAPS](mci-getdevcaps.md) 命令，以判斷裝置是否調整映射。</span><span class="sxs-lookup"><span data-stu-id="58212-137">You can use the MCI\_GETDEVCAPS\_CAN\_STRETCH flag with the [MCI\_GETDEVCAPS](mci-getdevcaps.md) command to determine if a device scales the image.</span></span> <span data-ttu-id="58212-138">如果裝置無法調整影像，則會傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="58212-138">A device returns **FALSE** if it cannot scale the image.</span></span>

</dd> <dt>

<span data-ttu-id="58212-139"><span id="MCI_DGV_PUT_SOURCE"></span><span id="mci_dgv_put_source"></span>MCI \_ DGV \_ PUT \_ 來源</span><span class="sxs-lookup"><span data-stu-id="58212-139"><span id="MCI_DGV_PUT_SOURCE"></span><span id="mci_dgv_put_source"></span>MCI\_DGV\_PUT\_SOURCE</span></span>
</dt> <dd>

<span data-ttu-id="58212-140">針對 MCI DGV RECT 定義的矩形會 \_ \_ 指定來源矩形。</span><span class="sxs-lookup"><span data-stu-id="58212-140">The rectangle defined for MCI\_DGV\_RECT specifies a source rectangle.</span></span> <span data-ttu-id="58212-141">來源矩形會指定要調整的框架緩衝區部分，以符合目的矩形。</span><span class="sxs-lookup"><span data-stu-id="58212-141">The source rectangle specifies which portion of the frame buffer is to be scaled to fit into the destination rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="58212-142"><span id="MCI_DGV_PUT_VIDEO"></span><span id="mci_dgv_put_video"></span>MCI \_ DGV \_ PUT \_ 影片</span><span class="sxs-lookup"><span data-stu-id="58212-142"><span id="MCI_DGV_PUT_VIDEO"></span><span id="mci_dgv_put_video"></span>MCI\_DGV\_PUT\_VIDEO</span></span>
</dt> <dd>

<span data-ttu-id="58212-143">針對 MCI DGV RECT 定義的矩形會 \_ \_ 套用至影片矩形。</span><span class="sxs-lookup"><span data-stu-id="58212-143">The rectangle defined for MCI\_DGV\_RECT applies to the video rectangle.</span></span> <span data-ttu-id="58212-144">影片矩形會指定目前展示來源的哪個部分儲存在框架緩衝區中。</span><span class="sxs-lookup"><span data-stu-id="58212-144">The video rectangle specifies which portion of the current presentation source is stored in the frame buffer.</span></span> <span data-ttu-id="58212-145">矩形是使用展示來源的自然座標來指定。</span><span class="sxs-lookup"><span data-stu-id="58212-145">The rectangle is specified using the natural coordinates of the presentation source.</span></span> <span data-ttu-id="58212-146">它允許在框架緩衝區中儲存影像和影片之前所發生的裁剪規格。</span><span class="sxs-lookup"><span data-stu-id="58212-146">It allows the specification of cropping that occurs prior to storing images and video in the frame buffer.</span></span> <span data-ttu-id="58212-147">預設矩形是完整的主動式掃描區域或完整解壓縮的影像和影片。</span><span class="sxs-lookup"><span data-stu-id="58212-147">The default rectangle is the full active scan area or the full decompressed images and video.</span></span>

</dd> <dt>

<span data-ttu-id="58212-148"><span id="MCI_DGV_PUT_WINDOW"></span><span id="mci_dgv_put_window"></span>MCI \_ DGV \_ PUT \_ 視窗</span><span class="sxs-lookup"><span data-stu-id="58212-148"><span id="MCI_DGV_PUT_WINDOW"></span><span id="mci_dgv_put_window"></span>MCI\_DGV\_PUT\_WINDOW</span></span>
</dt> <dd>

<span data-ttu-id="58212-149">針對 MCI DGV RECT 定義的矩形會 \_ \_ 套用至顯示視窗。</span><span class="sxs-lookup"><span data-stu-id="58212-149">The rectangle defined for MCI\_DGV\_RECT applies to the display window.</span></span> <span data-ttu-id="58212-150">這個矩形相對於顯示視窗的父視窗， (通常是桌面) 。</span><span class="sxs-lookup"><span data-stu-id="58212-150">This rectangle is relative to the parent window of the display window (usually the desktop).</span></span> <span data-ttu-id="58212-151">如果未指定視窗，則會預設為初始視窗大小和位置。</span><span class="sxs-lookup"><span data-stu-id="58212-151">If the window is not specified, it defaults to the initial window size and position.</span></span>

</dd> <dt>

<span data-ttu-id="58212-152"><span id="MCI_DGV_RECT"></span><span id="mci_dgv_rect"></span>MCI \_ DGV \_ RECT</span><span class="sxs-lookup"><span data-stu-id="58212-152"><span id="MCI_DGV_RECT"></span><span id="mci_dgv_rect"></span>MCI\_DGV\_RECT</span></span>
</dt> <dd>

<span data-ttu-id="58212-153">*LpDest* 所識別之結構的 **rc** 成員包含有效的矩形。</span><span class="sxs-lookup"><span data-stu-id="58212-153">The **rc** member of the structure identified by *lpDest* contains a valid rectangle.</span></span>

</dd> </dl>

<span data-ttu-id="58212-154">針對數位影片裝置， *lpDest* 會指向 [**MCI \_ DGV \_ PUT \_ PARMS**](/previous-versions//dd743397(v=vs.85)) 結構。</span><span class="sxs-lookup"><span data-stu-id="58212-154">For digital-video devices, *lpDest* points to an [**MCI\_DGV\_PUT\_PARMS**](/previous-versions//dd743397(v=vs.85)) structure.</span></span>

<span data-ttu-id="58212-155">下列其他旗標會搭配覆迭 **裝置類型** 使用：</span><span class="sxs-lookup"><span data-stu-id="58212-155">The following additional flags are used with the **overlay** device type:</span></span>

<dl> <dt>

<span data-ttu-id="58212-156"><span id="MCI_OVLY_PUT_DESTINATION"></span><span id="mci_ovly_put_destination"></span>MCI \_ OVLY \_ PUT \_ DESTINATION</span><span class="sxs-lookup"><span data-stu-id="58212-156"><span id="MCI_OVLY_PUT_DESTINATION"></span><span id="mci_ovly_put_destination"></span>MCI\_OVLY\_PUT\_DESTINATION</span></span>
</dt> <dd>

<span data-ttu-id="58212-157">針對 MCI OVLY RECT 定義的矩形會 \_ \_ 指定用來顯示影像的用戶端視窗區域。</span><span class="sxs-lookup"><span data-stu-id="58212-157">The rectangle defined for MCI\_OVLY\_RECT specifies the area of the client window used to display an image.</span></span> <span data-ttu-id="58212-158">矩形包含相對於視窗原點之影像的位移和可見範圍。</span><span class="sxs-lookup"><span data-stu-id="58212-158">The rectangle contains the offset and visible extent of the image relative to the window origin.</span></span> <span data-ttu-id="58212-159">如果框架正在延展，則來源會延伸至目的地矩形。</span><span class="sxs-lookup"><span data-stu-id="58212-159">If the frame is being stretched, the source is stretched to the destination rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="58212-160"><span id="MCI_OVLY_PUT_FRAME"></span><span id="mci_ovly_put_frame"></span>MCI \_ OVLY \_ PUT \_ FRAME</span><span class="sxs-lookup"><span data-stu-id="58212-160"><span id="MCI_OVLY_PUT_FRAME"></span><span id="mci_ovly_put_frame"></span>MCI\_OVLY\_PUT\_FRAME</span></span>
</dt> <dd>

<span data-ttu-id="58212-161">針對 MCI OVLY RECT 定義的矩形 \_ \_ 會指定用來接收影片影像的影片緩衝區區域。</span><span class="sxs-lookup"><span data-stu-id="58212-161">The rectangle defined for MCI\_OVLY\_RECT specifies the area of the video buffer used to receive the video image.</span></span> <span data-ttu-id="58212-162">矩形包含相對於影片緩衝區原點的緩衝區區域位移與範圍。</span><span class="sxs-lookup"><span data-stu-id="58212-162">The rectangle contains the offset and extent of the buffer area relative to the video buffer origin.</span></span>

</dd> <dt>

<span data-ttu-id="58212-163"><span id="MCI_OVLY_PUT_SOURCE"></span><span id="mci_ovly_put_source"></span>MCI \_ OVLY \_ PUT \_ 來源</span><span class="sxs-lookup"><span data-stu-id="58212-163"><span id="MCI_OVLY_PUT_SOURCE"></span><span id="mci_ovly_put_source"></span>MCI\_OVLY\_PUT\_SOURCE</span></span>
</dt> <dd>

<span data-ttu-id="58212-164">針對 MCI OVLY RECT 定義的矩形會 \_ \_ 指定用來做為數位影像來源的影片緩衝區區域。</span><span class="sxs-lookup"><span data-stu-id="58212-164">The rectangle defined for MCI\_OVLY\_RECT specifies the area of the video buffer used as the source of the digital image.</span></span> <span data-ttu-id="58212-165">矩形包含相對於影片緩衝區之剪輯矩形的位移和範圍（相對於其來源）。</span><span class="sxs-lookup"><span data-stu-id="58212-165">The rectangle contains the offset and extent of the clipping rectangle for the video buffer relative to its origin.</span></span>

</dd> <dt>

<span data-ttu-id="58212-166"><span id="MCI_OVLY_PUT_VIDEO"></span><span id="mci_ovly_put_video"></span>MCI \_ OVLY \_ PUT \_ 影片</span><span class="sxs-lookup"><span data-stu-id="58212-166"><span id="MCI_OVLY_PUT_VIDEO"></span><span id="mci_ovly_put_video"></span>MCI\_OVLY\_PUT\_VIDEO</span></span>
</dt> <dd>

<span data-ttu-id="58212-167">針對 MCI OVLY RECT 定義的矩形會 \_ \_ 指定影片緩衝區的影片來源捕捉區域。</span><span class="sxs-lookup"><span data-stu-id="58212-167">The rectangle defined for MCI\_OVLY\_RECT specifies the area of the video source capture by the video buffer.</span></span> <span data-ttu-id="58212-168">矩形包含影片來源（相對於其原點）之裁剪矩形的位移與範圍。</span><span class="sxs-lookup"><span data-stu-id="58212-168">The rectangle contains the offset and extent of the clipping rectangle for the video source relative to its origin.</span></span>

</dd> <dt>

<span data-ttu-id="58212-169"><span id="MCI_OVLY_RECT"></span><span id="mci_ovly_rect"></span>MCI \_ OVLY \_ RECT</span><span class="sxs-lookup"><span data-stu-id="58212-169"><span id="MCI_OVLY_RECT"></span><span id="mci_ovly_rect"></span>MCI\_OVLY\_RECT</span></span>
</dt> <dd>

<span data-ttu-id="58212-170">*LpDest* 所識別之結構的 **rc** 成員包含有效的顯示矩形。</span><span class="sxs-lookup"><span data-stu-id="58212-170">The **rc** member of the structure identified by *lpDest* contains a valid display rectangle.</span></span> <span data-ttu-id="58212-171">如果未指定此旗標，則預設矩形會符合要裁剪的影片緩衝區或視窗的座標。</span><span class="sxs-lookup"><span data-stu-id="58212-171">If this flag is not specified, the default rectangle matches the coordinates of the video buffer or window being clipped.</span></span>

</dd> </dl>

<span data-ttu-id="58212-172">針對影片重迭裝置， *lpDest* 會指向 [**MCI \_ OVLY \_ RECT \_ PARMS**](mci-ovly-rect-parms.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="58212-172">For video-overlay devices, *lpDest* points to an [**MCI\_OVLY\_RECT\_PARMS**](mci-ovly-rect-parms.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="58212-173">規格需求</span><span class="sxs-lookup"><span data-stu-id="58212-173">Requirements</span></span>



| <span data-ttu-id="58212-174">需求</span><span class="sxs-lookup"><span data-stu-id="58212-174">Requirement</span></span> | <span data-ttu-id="58212-175">值</span><span class="sxs-lookup"><span data-stu-id="58212-175">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="58212-176">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="58212-176">Minimum supported client</span></span><br/> | <span data-ttu-id="58212-177">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="58212-177">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="58212-178">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="58212-178">Minimum supported server</span></span><br/> | <span data-ttu-id="58212-179">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="58212-179">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="58212-180">標頭</span><span class="sxs-lookup"><span data-stu-id="58212-180">Header</span></span><br/>                   | <dl> <span data-ttu-id="58212-181"><dt>Mmsystem (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="58212-181"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58212-182">另請參閱</span><span class="sxs-lookup"><span data-stu-id="58212-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58212-183">Mci</span><span class="sxs-lookup"><span data-stu-id="58212-183">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="58212-184">MCI 命令</span><span class="sxs-lookup"><span data-stu-id="58212-184">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

