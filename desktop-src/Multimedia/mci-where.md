---
title: 'MCI_WHERE 命令 (Mmsystem .h) '
description: MCI \_ ，其中命令可取得影片裝置的剪切矩形。
ms.assetid: f64a7e49-4ee1-4836-ba9a-0bbdc47626b3
keywords:
- MCI_WHERE 命令 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_WHERE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6619131319863d1159a3bdb8bb85d366243544a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934434"
---
# <a name="mci_where-command"></a><span data-ttu-id="b77df-104">MCI \_ WHERE 命令</span><span class="sxs-lookup"><span data-stu-id="b77df-104">MCI\_WHERE command</span></span>

<span data-ttu-id="b77df-105">MCI \_ ，其中命令可取得影片裝置的剪切矩形。</span><span class="sxs-lookup"><span data-stu-id="b77df-105">The MCI\_WHERE command obtains the clipping rectangle for the video device.</span></span> <span data-ttu-id="b77df-106">數位影片和影片重迭裝置會辨識此命令。</span><span class="sxs-lookup"><span data-stu-id="b77df-106">Digital-video, and video-overlay devices recognize this command.</span></span> <span data-ttu-id="b77df-107">[傳回之矩形的](/previous-versions//ms536136(v=vs.85))**左上角** 和 **左方** 成員包含裁剪矩形的原點，**右邊** 和 **底部** 的成員則包含裁剪矩形的寬度和高度。</span><span class="sxs-lookup"><span data-stu-id="b77df-107">The **top** and **left** members of the returned [RECT](/previous-versions//ms536136(v=vs.85)) contain the origin of the clipping rectangle, and the **right** and **bottom** members contain the width and height of the clipping rectangle.</span></span> <span data-ttu-id="b77df-108"> (這不是 **右邊** 和 **底部** 成員的標準使用。 ) </span><span class="sxs-lookup"><span data-stu-id="b77df-108">(This is not the standard use of the **right** and **bottom** members.)</span></span>

<span data-ttu-id="b77df-109">若要傳送此命令，請使用下列參數呼叫 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) 函數。</span><span class="sxs-lookup"><span data-stu-id="b77df-109">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_WHERE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpQuery
);
```



## <a name="parameters"></a><span data-ttu-id="b77df-110">參數</span><span class="sxs-lookup"><span data-stu-id="b77df-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b77df-111"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="b77df-111"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="b77df-112">要接收命令訊息之 MCI 裝置的裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="b77df-112">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="b77df-113"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="b77df-113"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="b77df-114">\_ \_ 適用于數位視訊裝置、mci 測試的 mci 通知、mci 等待或 \_ 。</span><span class="sxs-lookup"><span data-stu-id="b77df-114">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video devices, MCI\_TEST.</span></span> <span data-ttu-id="b77df-115">如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。</span><span class="sxs-lookup"><span data-stu-id="b77df-115">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="b77df-116"><span id="lpQuery"></span><span id="lpquery"></span><span id="LPQUERY"></span>*lpQuery*</span><span class="sxs-lookup"><span data-stu-id="b77df-116"><span id="lpQuery"></span><span id="lpquery"></span><span id="LPQUERY"></span>*lpQuery*</span></span>
</dt> <dd>

<span data-ttu-id="b77df-117">[**MCI \_ 泛型 \_ PARMS**](mci-generic-parms.md)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="b77df-117">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="b77df-118">具有擴充命令集的 (裝置，可能會以裝置特定結構取代此結構。 ) </span><span class="sxs-lookup"><span data-stu-id="b77df-118">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b77df-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="b77df-119">Return Value</span></span>

<span data-ttu-id="b77df-120">如果成功則傳回零，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="b77df-120">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="b77df-121">備註</span><span class="sxs-lookup"><span data-stu-id="b77df-121">Remarks</span></span>

<span data-ttu-id="b77df-122">下列其他旗標適用于 **digitalvideo** 裝置類型：</span><span class="sxs-lookup"><span data-stu-id="b77df-122">The following additional flags are used with the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="b77df-123"><span id="MCI_DGV_WHERE_DESTINATION"></span><span id="mci_dgv_where_destination"></span>\_ \_ 目的地的 MCI \_ DGV</span><span class="sxs-lookup"><span data-stu-id="b77df-123"><span id="MCI_DGV_WHERE_DESTINATION"></span><span id="mci_dgv_where_destination"></span>MCI\_DGV\_WHERE\_DESTINATION</span></span>
</dt> <dd>

<span data-ttu-id="b77df-124">取得用來在目前視窗的工作區中顯示影片和影像的矩形區域描述。</span><span class="sxs-lookup"><span data-stu-id="b77df-124">Obtains a description of the rectangular region used to display video and images in the client area of the current window.</span></span>

</dd> <dt>

<span data-ttu-id="b77df-125"><span id="MCI_DGV_WHERE_FRAME"></span><span id="mci_dgv_where_frame"></span>MCI \_ DGV \_ WHERE \_ FRAME</span><span class="sxs-lookup"><span data-stu-id="b77df-125"><span id="MCI_DGV_WHERE_FRAME"></span><span id="mci_dgv_where_frame"></span>MCI\_DGV\_WHERE\_FRAME</span></span>
</dt> <dd>

<span data-ttu-id="b77df-126">取得畫面格緩衝區矩形區域的描述，以縮放影片矩形中的影像。</span><span class="sxs-lookup"><span data-stu-id="b77df-126">Obtains a description of the rectangular region of the frame buffer into which images from the video rectangle are scaled.</span></span> <span data-ttu-id="b77df-127">矩形座標會放置在 *lpQuery* 所識別之結構的 **rc** 成員中。</span><span class="sxs-lookup"><span data-stu-id="b77df-127">The rectangle coordinates are placed in the **rc** member of the structure identified by *lpQuery*.</span></span>

</dd> <dt>

<span data-ttu-id="b77df-128"><span id="MCI_DGV_WHERE_MAX"></span><span id="mci_dgv_where_max"></span>MCI \_ DGV \_ ，其中 \_ 最大值</span><span class="sxs-lookup"><span data-stu-id="b77df-128"><span id="MCI_DGV_WHERE_MAX"></span><span id="mci_dgv_where_max"></span>MCI\_DGV\_WHERE\_MAX</span></span>
</dt> <dd>

<span data-ttu-id="b77df-129">搭配 \_ \_ \_ 目的地或 mci DGV 來源的 mci DGV 使用時 \_ \_ \_ ，傳回的矩形表示指定區域的最大寬度和高度。</span><span class="sxs-lookup"><span data-stu-id="b77df-129">When used with MCI\_DGV\_WHERE\_DESTINATION or MCI\_DGV\_WHERE\_SOURCE, the rectangle returned indicates the maximum width and height of the specified region.</span></span> <span data-ttu-id="b77df-130">與 MCI \_ DGV \_ （其中 \_ 的視窗）搭配使用時，傳回的矩形表示整個顯示器的大小。</span><span class="sxs-lookup"><span data-stu-id="b77df-130">When used with MCI\_DGV\_WHERE\_WINDOW, the rectangle returned indicates the size of the entire display.</span></span>

</dd> <dt>

<span data-ttu-id="b77df-131"><span id="MCI_DGV_WHERE_SOURCE"></span><span id="mci_dgv_where_source"></span>\_DGV \_ 來源的 \_ MCI</span><span class="sxs-lookup"><span data-stu-id="b77df-131"><span id="MCI_DGV_WHERE_SOURCE"></span><span id="mci_dgv_where_source"></span>MCI\_DGV\_WHERE\_SOURCE</span></span>
</dt> <dd>

<span data-ttu-id="b77df-132">取得矩形區域的描述， (裁剪自框架緩衝區) ，該緩衝區會延展以符合顯示器上的目的地矩形。</span><span class="sxs-lookup"><span data-stu-id="b77df-132">Obtains a description of the rectangular region (cropped from the frame buffer) that is stretched to fit the destination rectangle on the display.</span></span>

</dd> <dt>

<span data-ttu-id="b77df-133"><span id="MCI_DGV_WHERE_VIDEO"></span><span id="mci_dgv_where_video"></span>MCI \_ DGV \_ ，其中 \_ 影片</span><span class="sxs-lookup"><span data-stu-id="b77df-133"><span id="MCI_DGV_WHERE_VIDEO"></span><span id="mci_dgv_where_video"></span>MCI\_DGV\_WHERE\_VIDEO</span></span>
</dt> <dd>

<span data-ttu-id="b77df-134">取得裁剪自展示來源之矩形區域的描述，以填滿框架緩衝區中的框架矩形。</span><span class="sxs-lookup"><span data-stu-id="b77df-134">Obtains a description of the rectangular region cropped from the presentation source to fill the frame rectangle in the frame buffer.</span></span> <span data-ttu-id="b77df-135">矩形座標會放置在 *lpQuery* 所識別之結構的 **rc** 成員中。</span><span class="sxs-lookup"><span data-stu-id="b77df-135">The rectangle coordinates are placed in the **rc** member of the structure identified by *lpQuery*.</span></span>

</dd> <dt>

<span data-ttu-id="b77df-136"><span id="MCI_DGV_WHERE_WINDOW"></span><span id="mci_dgv_where_window"></span>MCI \_ DGV \_ WHERE \_ WINDOW</span><span class="sxs-lookup"><span data-stu-id="b77df-136"><span id="MCI_DGV_WHERE_WINDOW"></span><span id="mci_dgv_where_window"></span>MCI\_DGV\_WHERE\_WINDOW</span></span>
</dt> <dd>

<span data-ttu-id="b77df-137">取得顯示視窗框架的描述。</span><span class="sxs-lookup"><span data-stu-id="b77df-137">Obtains a description of the display-window frame.</span></span>

</dd> <dt>


</dt> <dd></dd> </dl>

<span data-ttu-id="b77df-138">針對數位影片裝置， *lpQuery* 參數會指向 **PARMS 結構所在的 \_ MCI \_ DGV \_** 。</span><span class="sxs-lookup"><span data-stu-id="b77df-138">For digital-video devices, the *lpQuery* parameter points to an **MCI\_DGV\_WHERE\_PARMS** structure.</span></span> <span data-ttu-id="b77df-139">**Mci \_ DGV \_ ，其中 \_ PARMS** 結構等同于 [**mci \_ DGV \_ RECT \_ PARMS**](/windows/win32/api/digitalv/ns-digitalv-mci_dgv_rect_parms)結構。</span><span class="sxs-lookup"><span data-stu-id="b77df-139">The **MCI\_DGV\_WHERE\_PARMS** structure is identical to the [**MCI\_DGV\_RECT\_PARMS**](/windows/win32/api/digitalv/ns-digitalv-mci_dgv_rect_parms) structure.</span></span>

<span data-ttu-id="b77df-140">下列其他旗標會搭配覆迭 **裝置類型** 使用：</span><span class="sxs-lookup"><span data-stu-id="b77df-140">The following additional flags are used with the **overlay** device type:</span></span>

<dl> <dt>

<span data-ttu-id="b77df-141"><span id="MCI_OVLY_WHERE_DESTINATION"></span><span id="mci_ovly_where_destination"></span>\_ \_ 目的地的 MCI \_ OVLY</span><span class="sxs-lookup"><span data-stu-id="b77df-141"><span id="MCI_OVLY_WHERE_DESTINATION"></span><span id="mci_ovly_where_destination"></span>MCI\_OVLY\_WHERE\_DESTINATION</span></span>
</dt> <dd>

<span data-ttu-id="b77df-142">取得目的地顯示矩形。</span><span class="sxs-lookup"><span data-stu-id="b77df-142">Obtains the destination display rectangle.</span></span> <span data-ttu-id="b77df-143">矩形座標會放置在 *lpQuery* 所識別之結構的 **rc** 成員中。</span><span class="sxs-lookup"><span data-stu-id="b77df-143">The rectangle coordinates are placed in the **rc** member of the structure identified by *lpQuery*.</span></span>

</dd> <dt>

<span data-ttu-id="b77df-144"><span id="MCI_OVLY_WHERE_FRAME"></span><span id="mci_ovly_where_frame"></span>MCI \_ OVLY \_ WHERE \_ FRAME</span><span class="sxs-lookup"><span data-stu-id="b77df-144"><span id="MCI_OVLY_WHERE_FRAME"></span><span id="mci_ovly_where_frame"></span>MCI\_OVLY\_WHERE\_FRAME</span></span>
</dt> <dd>

<span data-ttu-id="b77df-145">取得覆蓋框架矩形。</span><span class="sxs-lookup"><span data-stu-id="b77df-145">Obtains the overlay frame rectangle.</span></span> <span data-ttu-id="b77df-146">矩形座標會放置在 *lpQuery* 所識別之結構的 **rc** 成員中。</span><span class="sxs-lookup"><span data-stu-id="b77df-146">The rectangle coordinates are placed in the **rc** member of the structure identified by *lpQuery*.</span></span>

</dd> <dt>

<span data-ttu-id="b77df-147"><span id="MCI_OVLY_WHERE_SOURCE"></span><span id="mci_ovly_where_source"></span>\_OVLY \_ 來源的 \_ MCI</span><span class="sxs-lookup"><span data-stu-id="b77df-147"><span id="MCI_OVLY_WHERE_SOURCE"></span><span id="mci_ovly_where_source"></span>MCI\_OVLY\_WHERE\_SOURCE</span></span>
</dt> <dd>

<span data-ttu-id="b77df-148">取得來源矩形。</span><span class="sxs-lookup"><span data-stu-id="b77df-148">Obtains the source rectangle.</span></span> <span data-ttu-id="b77df-149">矩形座標會放置在 *lpQuery* 所識別之結構的 **rc** 成員中。</span><span class="sxs-lookup"><span data-stu-id="b77df-149">The rectangle coordinates are placed in the **rc** member of the structure identified by *lpQuery*.</span></span>

</dd> <dt>

<span data-ttu-id="b77df-150"><span id="MCI_OVLY_WHERE_VIDEO"></span><span id="mci_ovly_where_video"></span>MCI \_ OVLY \_ ，其中 \_ 影片</span><span class="sxs-lookup"><span data-stu-id="b77df-150"><span id="MCI_OVLY_WHERE_VIDEO"></span><span id="mci_ovly_where_video"></span>MCI\_OVLY\_WHERE\_VIDEO</span></span>
</dt> <dd>

<span data-ttu-id="b77df-151">取得影片矩形。</span><span class="sxs-lookup"><span data-stu-id="b77df-151">Obtains the video rectangle.</span></span> <span data-ttu-id="b77df-152">矩形座標會放置在 *lpQuery* 所識別之結構的 **rc** 成員中。</span><span class="sxs-lookup"><span data-stu-id="b77df-152">The rectangle coordinates are placed in the **rc** member of the structure identified by *lpQuery*.</span></span>

</dd> </dl>

<span data-ttu-id="b77df-153">針對影片重迭裝置， *lpQuery* 參數會指向 [**MCI \_ OVLY \_ RECT \_ PARMS**](mci-ovly-rect-parms.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="b77df-153">For video-overlay devices, the *lpQuery* parameter points to an [**MCI\_OVLY\_RECT\_PARMS**](mci-ovly-rect-parms.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="b77df-154">規格需求</span><span class="sxs-lookup"><span data-stu-id="b77df-154">Requirements</span></span>



| <span data-ttu-id="b77df-155">需求</span><span class="sxs-lookup"><span data-stu-id="b77df-155">Requirement</span></span> | <span data-ttu-id="b77df-156">值</span><span class="sxs-lookup"><span data-stu-id="b77df-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b77df-157">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b77df-157">Minimum supported client</span></span><br/> | <span data-ttu-id="b77df-158">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b77df-158">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="b77df-159">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b77df-159">Minimum supported server</span></span><br/> | <span data-ttu-id="b77df-160">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b77df-160">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="b77df-161">標頭</span><span class="sxs-lookup"><span data-stu-id="b77df-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="b77df-162"><dt>Mmsystem (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="b77df-162"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b77df-163">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b77df-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b77df-164">Mci</span><span class="sxs-lookup"><span data-stu-id="b77df-164">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="b77df-165">MCI 命令</span><span class="sxs-lookup"><span data-stu-id="b77df-165">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

