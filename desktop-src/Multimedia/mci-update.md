---
title: 'MCI_UPDATE 命令 (Mmsystem .h) '
description: MCI \_ UPDATE 命令會更新顯示矩形。 數位影片裝置辨識此命令。
ms.assetid: 90a8c10f-61b9-49a1-bbcc-e0729aa8c454
keywords:
- MCI_UPDATE 命令 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_UPDATE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 423186096c88a8f1ff74987ff57c6b49dc6c3131
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105911"
---
# <a name="mci_update-command"></a><span data-ttu-id="bcc85-105">MCI \_ 更新命令</span><span class="sxs-lookup"><span data-stu-id="bcc85-105">MCI\_UPDATE command</span></span>

<span data-ttu-id="bcc85-106">MCI \_ UPDATE 命令會更新顯示矩形。</span><span class="sxs-lookup"><span data-stu-id="bcc85-106">The MCI\_UPDATE command updates the display rectangle.</span></span> <span data-ttu-id="bcc85-107">數位影片裝置辨識此命令。</span><span class="sxs-lookup"><span data-stu-id="bcc85-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="bcc85-108">若要傳送此命令，請使用下列參數呼叫 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) 函數。</span><span class="sxs-lookup"><span data-stu-id="bcc85-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_UPDATE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpDest
);
```



## <a name="parameters"></a><span data-ttu-id="bcc85-109">參數</span><span class="sxs-lookup"><span data-stu-id="bcc85-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bcc85-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="bcc85-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="bcc85-111">要接收命令訊息之 MCI 裝置的裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="bcc85-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="bcc85-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="bcc85-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="bcc85-113">**MCI \_通知**、 **mci \_ 等候**，或適用于數位影片裝置、 **mci \_ 測試**。</span><span class="sxs-lookup"><span data-stu-id="bcc85-113">**MCI\_NOTIFY**, **MCI\_WAIT**, or, for digital-video devices, **MCI\_TEST**.</span></span> <span data-ttu-id="bcc85-114">如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。</span><span class="sxs-lookup"><span data-stu-id="bcc85-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="bcc85-115"><span id="lpDest"></span><span id="lpdest"></span><span id="LPDEST"></span>*lpDest*</span><span class="sxs-lookup"><span data-stu-id="bcc85-115"><span id="lpDest"></span><span id="lpdest"></span><span id="LPDEST"></span>*lpDest*</span></span>
</dt> <dd>

<span data-ttu-id="bcc85-116">[**MCI \_ 泛型 \_ PARMS**](mci-generic-parms.md)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="bcc85-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="bcc85-117">具有擴充命令集的 (裝置，可能會以裝置特定結構取代此結構。 ) </span><span class="sxs-lookup"><span data-stu-id="bcc85-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bcc85-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="bcc85-118">Return Value</span></span>

<span data-ttu-id="bcc85-119">如果成功則傳回零，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="bcc85-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="bcc85-120">備註</span><span class="sxs-lookup"><span data-stu-id="bcc85-120">Remarks</span></span>

<span data-ttu-id="bcc85-121">下列其他旗標會搭配 "digitalvideo" 裝置類型使用：</span><span class="sxs-lookup"><span data-stu-id="bcc85-121">The following additional flags are used with the "digitalvideo" device type:</span></span>

<dl> <dt>

<span data-ttu-id="bcc85-122"><span id="MCI_DGV_UPDATE_HDC"></span><span id="mci_dgv_update_hdc"></span>MCI \_ DGV \_ UPDATE \_ HDC</span><span class="sxs-lookup"><span data-stu-id="bcc85-122"><span id="MCI_DGV_UPDATE_HDC"></span><span id="mci_dgv_update_hdc"></span>MCI\_DGV\_UPDATE\_HDC</span></span>
</dt> <dd>

<span data-ttu-id="bcc85-123">*LpDest* 所識別之結構的 **hDC** 成員包含要繪製之 DC 的有效視窗。</span><span class="sxs-lookup"><span data-stu-id="bcc85-123">The **hDC** member of the structure identified by *lpDest* contains a valid window of the DC to paint.</span></span> <span data-ttu-id="bcc85-124">此為必要旗標。</span><span class="sxs-lookup"><span data-stu-id="bcc85-124">This flag is required.</span></span>

</dd> <dt>

<span data-ttu-id="bcc85-125"><span id="MCI_DGV_RECT"></span><span id="mci_dgv_rect"></span>MCI \_ DGV \_ RECT</span><span class="sxs-lookup"><span data-stu-id="bcc85-125"><span id="MCI_DGV_RECT"></span><span id="mci_dgv_rect"></span>MCI\_DGV\_RECT</span></span>
</dt> <dd>

<span data-ttu-id="bcc85-126">*LpUnfreeze* 所識別之結構的 **rc** 成員包含有效的顯示矩形。</span><span class="sxs-lookup"><span data-stu-id="bcc85-126">The **rc** member of the structure identified by *lpUnfreeze* contains a valid display rectangle.</span></span> <span data-ttu-id="bcc85-127">矩形會指定相對於用戶端矩形的裁剪矩形。</span><span class="sxs-lookup"><span data-stu-id="bcc85-127">The rectangle specifies the clipping rectangle relative to the client rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="bcc85-128"><span id="MCI_DGV_UPDATE_PAINT"></span><span id="mci_dgv_update_paint"></span>MCI \_ DGV \_ 更新 \_ 繪圖</span><span class="sxs-lookup"><span data-stu-id="bcc85-128"><span id="MCI_DGV_UPDATE_PAINT"></span><span id="mci_dgv_update_paint"></span>MCI\_DGV\_UPDATE\_PAINT</span></span>
</dt> <dd>

<span data-ttu-id="bcc85-129">當應用程式收到適用于顯示 DC 的 [**WM \_ 油漆**](/windows/desktop/gdi/wm-paint) 訊息時，會使用此旗標。</span><span class="sxs-lookup"><span data-stu-id="bcc85-129">An application uses this flag when it receives a [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) message that is intended for a display DC.</span></span> <span data-ttu-id="bcc85-130">框架緩衝區裝置通常會繪製按鍵色彩。</span><span class="sxs-lookup"><span data-stu-id="bcc85-130">A frame-buffer device usually paints the key color.</span></span> <span data-ttu-id="bcc85-131">如果顯示裝置沒有框架緩衝區，則 \_ 使用 **mci \_ DGV \_ update \_ 油漆** 旗標時，可能會忽略 mci UPDATE 命令，因為播放作業期間會重新繪製顯示器。</span><span class="sxs-lookup"><span data-stu-id="bcc85-131">If the display device does not have a frame buffer, it might ignore the MCI\_UPDATE command when the **MCI\_DGV\_UPDATE\_PAINT** flag is used because the display will be repainted during the playback operation.</span></span>

</dd> </dl>

<span data-ttu-id="bcc85-132">針對數位影片裝置， *lpDest* 參數會指向 [**MCI \_ DGV \_ 更新 \_ PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_update_parms) 結構。</span><span class="sxs-lookup"><span data-stu-id="bcc85-132">For digital-video devices, the *lpDest* parameter points to an [**MCI\_DGV\_UPDATE\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_update_parms) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="bcc85-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="bcc85-133">Requirements</span></span>



| <span data-ttu-id="bcc85-134">需求</span><span class="sxs-lookup"><span data-stu-id="bcc85-134">Requirement</span></span> | <span data-ttu-id="bcc85-135">值</span><span class="sxs-lookup"><span data-stu-id="bcc85-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bcc85-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bcc85-136">Minimum supported client</span></span><br/> | <span data-ttu-id="bcc85-137">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bcc85-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="bcc85-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bcc85-138">Minimum supported server</span></span><br/> | <span data-ttu-id="bcc85-139">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bcc85-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="bcc85-140">標頭</span><span class="sxs-lookup"><span data-stu-id="bcc85-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="bcc85-141"><dt>Mmsystem (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="bcc85-141"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bcc85-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bcc85-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bcc85-143">Mci</span><span class="sxs-lookup"><span data-stu-id="bcc85-143">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="bcc85-144">MCI 命令</span><span class="sxs-lookup"><span data-stu-id="bcc85-144">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

