---
title: 'MCI_BREAK 命令 (Mmsystem .h) '
description: MCI \_ BREAK 命令會設定 mci 裝置的 BREAK 鍵。 MCI 直接支援此命令，而不是將它傳遞至裝置。 任何 MCI 應用程式都可以使用此命令。
ms.assetid: 127b5179-2838-4bde-8d0c-37a4cc87fa4d
keywords:
- MCI_BREAK 命令 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_BREAK
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33b17e3796192344ef974fed1af7229d41746aaf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464989"
---
# <a name="mci_break-command"></a><span data-ttu-id="b049b-106">MCI \_ BREAK 命令</span><span class="sxs-lookup"><span data-stu-id="b049b-106">MCI\_BREAK command</span></span>

<span data-ttu-id="b049b-107">MCI \_ BREAK 命令會設定 mci 裝置的 BREAK 鍵。</span><span class="sxs-lookup"><span data-stu-id="b049b-107">The MCI\_BREAK command sets a break key for an MCI device.</span></span> <span data-ttu-id="b049b-108">MCI 直接支援此命令，而不是將它傳遞至裝置。</span><span class="sxs-lookup"><span data-stu-id="b049b-108">MCI supports this command directly rather than passing it to the device.</span></span> <span data-ttu-id="b049b-109">任何 MCI 應用程式都可以使用此命令。</span><span class="sxs-lookup"><span data-stu-id="b049b-109">Any MCI application can use this command.</span></span>

<span data-ttu-id="b049b-110">若要傳送此命令，請使用下列參數呼叫 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) 函數。</span><span class="sxs-lookup"><span data-stu-id="b049b-110">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_BREAK, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_BREAK_PARMS) lpBreak
);
```



## <a name="parameters"></a><span data-ttu-id="b049b-111">參數</span><span class="sxs-lookup"><span data-stu-id="b049b-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b049b-112"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="b049b-112"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="b049b-113">要接收命令訊息之 MCI 裝置的裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="b049b-113">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="b049b-114"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="b049b-114"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="b049b-115">\_ \_ (VCR) 裝置、mci 測試的 mci 通知、mci 等候，或。 \_</span><span class="sxs-lookup"><span data-stu-id="b049b-115">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video and video-cassette recorder (VCR) devices, MCI\_TEST.</span></span> <span data-ttu-id="b049b-116">如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。</span><span class="sxs-lookup"><span data-stu-id="b049b-116">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="b049b-117"><span id="lpBreak"></span><span id="lpbreak"></span><span id="LPBREAK"></span>*lpBreak*</span><span class="sxs-lookup"><span data-stu-id="b049b-117"><span id="lpBreak"></span><span id="lpbreak"></span><span id="LPBREAK"></span>*lpBreak*</span></span>
</dt> <dd>

<span data-ttu-id="b049b-118">[**MCI \_ 中斷 \_ PARMS**](mci-break-parms.md)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="b049b-118">Pointer to an [**MCI\_ BREAK\_PARMS**](mci-break-parms.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b049b-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="b049b-119">Return Value</span></span>

<span data-ttu-id="b049b-120">如果成功則傳回零，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="b049b-120">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="b049b-121">備註</span><span class="sxs-lookup"><span data-stu-id="b049b-121">Remarks</span></span>

<span data-ttu-id="b049b-122">您可能必須多次按下 break 鍵，以中斷等候作業。</span><span class="sxs-lookup"><span data-stu-id="b049b-122">You might have to press the break key multiple times to interrupt a wait operation.</span></span> <span data-ttu-id="b049b-123">在裝置等待取消之後按下 break 鍵，可以將中斷傳送至應用程式。</span><span class="sxs-lookup"><span data-stu-id="b049b-123">Pressing the break key after a device wait is canceled can send the break to an application.</span></span> <span data-ttu-id="b049b-124">如果應用程式有針對虛擬機器碼程式碼定義的動作，則可能會不慎回應中斷。</span><span class="sxs-lookup"><span data-stu-id="b049b-124">If an application has an action defined for the virtual-key code, then it can inadvertently respond to the break.</span></span> <span data-ttu-id="b049b-125">例如，如果應用程式使用 VK \_ CANCEL 作為快速鍵，則如果在等候取消之後按下它，就可以回應預設的 CTRL + BREAK 鍵。</span><span class="sxs-lookup"><span data-stu-id="b049b-125">For example, an application using VK\_CANCEL for an accelerator key can respond to the default CTRL+BREAK key if it is pressed after a wait is canceled.</span></span>

<span data-ttu-id="b049b-126">下列其他旗標適用于所有裝置：</span><span class="sxs-lookup"><span data-stu-id="b049b-126">The following additional flags apply to all devices:</span></span>

<dl> <dt>

<span data-ttu-id="b049b-127"><span id="MCI_BREAK_HWND"></span><span id="mci_break_hwnd"></span>MCI \_ BREAK \_ HWND</span><span class="sxs-lookup"><span data-stu-id="b049b-127"><span id="MCI_BREAK_HWND"></span><span id="mci_break_hwnd"></span>MCI\_BREAK\_HWND</span></span>
</dt> <dd>

<span data-ttu-id="b049b-128">*LpBreak* 所識別之結構的 **hwndBreak** 成員包含必須是目前視窗的視窗控制碼，才能啟用該 MCI 裝置的中斷偵測。</span><span class="sxs-lookup"><span data-stu-id="b049b-128">The **hwndBreak** member of the structure identified by *lpBreak* contains a window handle that must be the current window in order to enable break detection for that MCI device.</span></span> <span data-ttu-id="b049b-129">這通常是應用程式的主視窗。</span><span class="sxs-lookup"><span data-stu-id="b049b-129">This is usually the application's main window.</span></span> <span data-ttu-id="b049b-130">如果省略，MCI 不會檢查目前視窗的視窗控制碼。</span><span class="sxs-lookup"><span data-stu-id="b049b-130">If omitted, MCI does not check the window handle of the current window.</span></span>

</dd> <dt>

<span data-ttu-id="b049b-131"><span id="MCI_BREAK_KEY"></span><span id="mci_break_key"></span>MCI \_ 中斷 \_ 金鑰</span><span class="sxs-lookup"><span data-stu-id="b049b-131"><span id="MCI_BREAK_KEY"></span><span id="mci_break_key"></span>MCI\_BREAK\_KEY</span></span>
</dt> <dd>

<span data-ttu-id="b049b-132">由 *lpBreak* 所識別之結構的 **nVirtKey** 成員會指定用於 break 索引鍵的虛擬機器碼程式碼。</span><span class="sxs-lookup"><span data-stu-id="b049b-132">The **nVirtKey** member of the structure identified by *lpBreak* specifies the virtual-key code used for the break key.</span></span> <span data-ttu-id="b049b-133">根據預設，MCI 會將 CTRL + BREAK 指派為 break 鍵。</span><span class="sxs-lookup"><span data-stu-id="b049b-133">By default, MCI assigns CTRL+BREAK as the break key.</span></span> <span data-ttu-id="b049b-134">如果 \_ 未指定 MCI BREAK，則需要此旗標 \_ 。</span><span class="sxs-lookup"><span data-stu-id="b049b-134">This flag is required if MCI\_BREAK\_OFF is not specified.</span></span>

</dd> <dt>

<span data-ttu-id="b049b-135"><span id="MCI_BREAK_OFF"></span><span id="mci_break_off"></span>MCI \_ 中斷 \_</span><span class="sxs-lookup"><span data-stu-id="b049b-135"><span id="MCI_BREAK_OFF"></span><span id="mci_break_off"></span>MCI\_BREAK\_OFF</span></span>
</dt> <dd>

<span data-ttu-id="b049b-136">停用指定裝置的任何現有 break 鍵。</span><span class="sxs-lookup"><span data-stu-id="b049b-136">Disables any existing break key for the indicated device.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b049b-137">規格需求</span><span class="sxs-lookup"><span data-stu-id="b049b-137">Requirements</span></span>



| <span data-ttu-id="b049b-138">需求</span><span class="sxs-lookup"><span data-stu-id="b049b-138">Requirement</span></span> | <span data-ttu-id="b049b-139">值</span><span class="sxs-lookup"><span data-stu-id="b049b-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b049b-140">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b049b-140">Minimum supported client</span></span><br/> | <span data-ttu-id="b049b-141">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b049b-141">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="b049b-142">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b049b-142">Minimum supported server</span></span><br/> | <span data-ttu-id="b049b-143">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b049b-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="b049b-144">標頭</span><span class="sxs-lookup"><span data-stu-id="b049b-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="b049b-145"><dt>Mmsystem (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="b049b-145"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b049b-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b049b-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b049b-147">Mci</span><span class="sxs-lookup"><span data-stu-id="b049b-147">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="b049b-148">MCI 命令</span><span class="sxs-lookup"><span data-stu-id="b049b-148">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

