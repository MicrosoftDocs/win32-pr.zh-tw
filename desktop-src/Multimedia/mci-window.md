---
title: 'MCI_WINDOW 命令 (Mmsystem .h) '
description: MCI \_ 視窗命令可指定圖形裝置的視窗和視窗特性。 數位影片和影片重迭裝置會辨識此命令。
ms.assetid: 8b6c4d9a-ee72-4c64-aebe-6c8153167496
keywords:
- MCI_WINDOW 命令 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_WINDOW
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41b4d630dbc9dbc7403e93cd0bda3de2eef1e5cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934522"
---
# <a name="mci_window-command"></a><span data-ttu-id="bc257-105">MCI \_ 視窗命令</span><span class="sxs-lookup"><span data-stu-id="bc257-105">MCI\_WINDOW command</span></span>

<span data-ttu-id="bc257-106">MCI \_ 視窗命令可指定圖形裝置的視窗和視窗特性。</span><span class="sxs-lookup"><span data-stu-id="bc257-106">The MCI\_WINDOW command specifies the window and the window characteristics for graphic devices.</span></span> <span data-ttu-id="bc257-107">數位影片和影片重迭裝置會辨識此命令。</span><span class="sxs-lookup"><span data-stu-id="bc257-107">Digital-video, and video-overlay devices recognize this command.</span></span>

<span data-ttu-id="bc257-108">若要傳送此命令，請使用下列參數呼叫 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) 函數。</span><span class="sxs-lookup"><span data-stu-id="bc257-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_WINDOW, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpWindow
);
```



## <a name="parameters"></a><span data-ttu-id="bc257-109">參數</span><span class="sxs-lookup"><span data-stu-id="bc257-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc257-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="bc257-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="bc257-111">要接收命令訊息之 MCI 裝置的裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="bc257-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="bc257-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="bc257-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="bc257-113">\_ \_ 適用于數位視訊裝置、mci 測試的 mci 通知、mci 等待或 \_ 。</span><span class="sxs-lookup"><span data-stu-id="bc257-113">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video devices, MCI\_TEST.</span></span> <span data-ttu-id="bc257-114">如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。</span><span class="sxs-lookup"><span data-stu-id="bc257-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="bc257-115"><span id="lpWindow"></span><span id="lpwindow"></span><span id="LPWINDOW"></span>*lpWindow*</span><span class="sxs-lookup"><span data-stu-id="bc257-115"><span id="lpWindow"></span><span id="lpwindow"></span><span id="LPWINDOW"></span>*lpWindow*</span></span>
</dt> <dd>

<span data-ttu-id="bc257-116">[**MCI \_ 泛型 \_ PARMS**](mci-generic-parms.md)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="bc257-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="bc257-117">具有擴充命令集的 (裝置，可能會以裝置特定結構取代此結構。 ) </span><span class="sxs-lookup"><span data-stu-id="bc257-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc257-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="bc257-118">Return Value</span></span>

<span data-ttu-id="bc257-119">如果成功則傳回零，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="bc257-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="bc257-120">備註</span><span class="sxs-lookup"><span data-stu-id="bc257-120">Remarks</span></span>

<span data-ttu-id="bc257-121">圖形裝置應該在裝置開啟時建立預設視窗，但在收到 [MCI \_ PLAY](mci-play.md) 命令之前不應該顯示。</span><span class="sxs-lookup"><span data-stu-id="bc257-121">Graphic devices should create a default window when a device is opened but should not display it until they receive the [MCI\_PLAY](mci-play.md) command.</span></span> <span data-ttu-id="bc257-122">您可以 \_ 使用 [MCI 視窗] 命令，將應用程式建立的視窗提供給裝置，以及變更應用程式定義或預設顯示視窗的顯示特性。</span><span class="sxs-lookup"><span data-stu-id="bc257-122">The MCI\_WINDOW command is used to supply an application-created window to the device and to change the display characteristics of an application-defined or default display window.</span></span> <span data-ttu-id="bc257-123">如果應用程式提供顯示視窗，則應該準備好在視窗上更新不正確矩形。</span><span class="sxs-lookup"><span data-stu-id="bc257-123">If the application supplies the display window, it should be prepared to update an invalid rectangle on the window.</span></span>

<span data-ttu-id="bc257-124">下列其他旗標適用于 **digitalvideo** 裝置類型：</span><span class="sxs-lookup"><span data-stu-id="bc257-124">The following additional flags are used with the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="bc257-125"><span id="MCI_DGV_WINDOW_HWND"></span><span id="mci_dgv_window_hwnd"></span>MCI \_ DGV \_ 視窗 \_ HWND</span><span class="sxs-lookup"><span data-stu-id="bc257-125"><span id="MCI_DGV_WINDOW_HWND"></span><span id="mci_dgv_window_hwnd"></span>MCI\_DGV\_WINDOW\_HWND</span></span>
</dt> <dd>

<span data-ttu-id="bc257-126">使用做為目的地的視窗控制碼包含在 *lpWindow* 所識別之結構的 **hWnd** 成員中。</span><span class="sxs-lookup"><span data-stu-id="bc257-126">The handle of the window needed for use as the destination is included in the **hWnd** member of the structure identified by *lpWindow*.</span></span>

</dd> <dt>

<span data-ttu-id="bc257-127"><span id="MCI_DGV_WINDOW_STATE"></span><span id="mci_dgv_window_state"></span>MCI \_ DGV \_ 視窗 \_ 狀態</span><span class="sxs-lookup"><span data-stu-id="bc257-127"><span id="MCI_DGV_WINDOW_STATE"></span><span id="mci_dgv_window_state"></span>MCI\_DGV\_WINDOW\_STATE</span></span>
</dt> <dd>

<span data-ttu-id="bc257-128">*LpWindow* 所識別之結構的 **nCmdShow** 成員包含設定視窗狀態的參數。</span><span class="sxs-lookup"><span data-stu-id="bc257-128">The **nCmdShow** member of the structure identified by *lpWindow* contains parameters for setting the window state.</span></span>

</dd> <dt>

<span data-ttu-id="bc257-129"><span id="MCI_DGV_WINDOW_TEXT"></span><span id="mci_dgv_window_text"></span>MCI \_ DGV \_ 視窗 \_ 文字</span><span class="sxs-lookup"><span data-stu-id="bc257-129"><span id="MCI_DGV_WINDOW_TEXT"></span><span id="mci_dgv_window_text"></span>MCI\_DGV\_WINDOW\_TEXT</span></span>
</dt> <dd>

<span data-ttu-id="bc257-130">*LpWindow* 所識別之結構的 **lpstrText** 成員包含緩衝區的位址，其中包含視窗標題列中所使用的標題。</span><span class="sxs-lookup"><span data-stu-id="bc257-130">The **lpstrText** member of the structure identified by *lpWindow* contains an address of a buffer containing the caption used in the window title bar.</span></span>

</dd> </dl>

<span data-ttu-id="bc257-131">針對數位影片裝置， *lpWindow* 參數會指向 [**MCI \_ DGV \_ 視窗 \_ PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_window_parmsa) 結構。</span><span class="sxs-lookup"><span data-stu-id="bc257-131">For digital-video devices, the *lpWindow* parameter points to an [**MCI\_DGV\_WINDOW\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_window_parmsa) structure.</span></span>

<span data-ttu-id="bc257-132">下列其他旗標會搭配覆迭 **裝置類型** 使用：</span><span class="sxs-lookup"><span data-stu-id="bc257-132">The following additional flags are used with the **overlay** device type:</span></span>

<dl> <dt>

<span data-ttu-id="bc257-133"><span id="MCI_OVLY_WINDOW_DISABLE_STRETCH"></span><span id="mci_ovly_window_disable_stretch"></span>MCI \_ OVLY \_ 視窗 \_ 停用 \_ STRETCH</span><span class="sxs-lookup"><span data-stu-id="bc257-133"><span id="MCI_OVLY_WINDOW_DISABLE_STRETCH"></span><span id="mci_ovly_window_disable_stretch"></span>MCI\_OVLY\_WINDOW\_DISABLE\_STRETCH</span></span>
</dt> <dd>

<span data-ttu-id="bc257-134">停用影像的延展。</span><span class="sxs-lookup"><span data-stu-id="bc257-134">Disables stretching of the image.</span></span>

</dd> <dt>

<span data-ttu-id="bc257-135"><span id="MCI_OVLY_WINDOW_ENABLE_STRETCH"></span><span id="mci_ovly_window_enable_stretch"></span>MCI \_ OVLY \_ 視窗 \_ 啟用 \_ 延展</span><span class="sxs-lookup"><span data-stu-id="bc257-135"><span id="MCI_OVLY_WINDOW_ENABLE_STRETCH"></span><span id="mci_ovly_window_enable_stretch"></span>MCI\_OVLY\_WINDOW\_ENABLE\_STRETCH</span></span>
</dt> <dd>

<span data-ttu-id="bc257-136">啟用延展影像。</span><span class="sxs-lookup"><span data-stu-id="bc257-136">Enables stretching of the image.</span></span>

</dd> <dt>

<span data-ttu-id="bc257-137"><span id="MCI_OVLY_WINDOW_HWND"></span><span id="mci_ovly_window_hwnd"></span>MCI \_ OVLY \_ 視窗 \_ HWND</span><span class="sxs-lookup"><span data-stu-id="bc257-137"><span id="MCI_OVLY_WINDOW_HWND"></span><span id="mci_ovly_window_hwnd"></span>MCI\_OVLY\_WINDOW\_HWND</span></span>
</dt> <dd>

<span data-ttu-id="bc257-138">用於目的地的視窗控制碼會包含在 *lpWindow* 所識別之結構的 **hWnd** 成員中。</span><span class="sxs-lookup"><span data-stu-id="bc257-138">The handle of the window used for the destination is included in the **hWnd** member of the structure identified by *lpWindow*.</span></span> <span data-ttu-id="bc257-139">將此旗標設定為 MCI \_ OVLY \_ window \_ default，以返回預設視窗。</span><span class="sxs-lookup"><span data-stu-id="bc257-139">Set this flag to MCI\_OVLY\_WINDOW\_DEFAULT to return to the default window.</span></span>

</dd> <dt>

<span data-ttu-id="bc257-140"><span id="MCI_OVLY_WINDOW_STATE"></span><span id="mci_ovly_window_state"></span>MCI \_ OVLY \_ 視窗 \_ 狀態</span><span class="sxs-lookup"><span data-stu-id="bc257-140"><span id="MCI_OVLY_WINDOW_STATE"></span><span id="mci_ovly_window_state"></span>MCI\_OVLY\_WINDOW\_STATE</span></span>
</dt> <dd>

<span data-ttu-id="bc257-141">*LpWindow* 結構的 **nCmdShow** 成員包含設定視窗狀態的參數。</span><span class="sxs-lookup"><span data-stu-id="bc257-141">The **nCmdShow** member of the *lpWindow* structure contains parameters for setting the window state.</span></span> <span data-ttu-id="bc257-142">此旗標相當於以 *state* 參數呼叫 [ShowWindow](/windows/win32/api/winuser/nf-winuser-showwindow) 。</span><span class="sxs-lookup"><span data-stu-id="bc257-142">This flag is equivalent to calling [ShowWindow](/windows/win32/api/winuser/nf-winuser-showwindow) with the *state* parameter.</span></span> <span data-ttu-id="bc257-143">這些常數與 WINDOWS 中定義的常數相同。H (例如 SW \_ HIDE、sw \_ 最小化或 sw \_ SHOWNORMAL) 。</span><span class="sxs-lookup"><span data-stu-id="bc257-143">The constants are the same as those defined in WINDOWS.H (such as SW\_HIDE, SW\_MINIMIZE, or SW\_SHOWNORMAL).</span></span>

</dd> <dt>

<span data-ttu-id="bc257-144"><span id="MCI_OVLY_WINDOW_TEXT"></span><span id="mci_ovly_window_text"></span>MCI \_ OVLY \_ 視窗 \_ 文字</span><span class="sxs-lookup"><span data-stu-id="bc257-144"><span id="MCI_OVLY_WINDOW_TEXT"></span><span id="mci_ovly_window_text"></span>MCI\_OVLY\_WINDOW\_TEXT</span></span>
</dt> <dd>

<span data-ttu-id="bc257-145">*LpWindow* 所識別之結構的 **lpstrText** 成員包含緩衝區的位址，其中包含用於視窗的標題。</span><span class="sxs-lookup"><span data-stu-id="bc257-145">The **lpstrText** member of the structure identified by *lpWindow* contains an address of a buffer containing the caption used for the window.</span></span>

</dd> </dl>

<span data-ttu-id="bc257-146">針對影片重迭裝置， *lpWindow* 參數會指向 [**MCI \_ OVLY \_ 視窗 \_ PARMS**](mci-ovly-window-parms.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="bc257-146">For video-overlay devices, the *lpWindow* parameter points to an [**MCI\_OVLY\_WINDOW\_PARMS**](mci-ovly-window-parms.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc257-147">規格需求</span><span class="sxs-lookup"><span data-stu-id="bc257-147">Requirements</span></span>



| <span data-ttu-id="bc257-148">需求</span><span class="sxs-lookup"><span data-stu-id="bc257-148">Requirement</span></span> | <span data-ttu-id="bc257-149">值</span><span class="sxs-lookup"><span data-stu-id="bc257-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc257-150">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bc257-150">Minimum supported client</span></span><br/> | <span data-ttu-id="bc257-151">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bc257-151">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="bc257-152">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bc257-152">Minimum supported server</span></span><br/> | <span data-ttu-id="bc257-153">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bc257-153">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="bc257-154">標頭</span><span class="sxs-lookup"><span data-stu-id="bc257-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="bc257-155"><dt>Mmsystem (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="bc257-155"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc257-156">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bc257-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc257-157">Mci</span><span class="sxs-lookup"><span data-stu-id="bc257-157">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="bc257-158">MCI 命令</span><span class="sxs-lookup"><span data-stu-id="bc257-158">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

