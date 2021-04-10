---
title: 'MCI_STEP 命令 (Mmsystem .h) '
description: MCI \_ 步驟命令會將玩家帶到一或多個畫面。 數位影片、VCR 和 CAV 格式的 videodisc 裝置都會辨識此命令。
ms.assetid: 8d976840-fe9d-4393-b9fc-10f847166b1b
keywords:
- MCI_STEP 命令 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_STEP
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd81b3ad0e1f10c14d68df12399045149f686a8c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104093795"
---
# <a name="mci_step-command"></a><span data-ttu-id="36cc4-105">MCI \_ 步驟命令</span><span class="sxs-lookup"><span data-stu-id="36cc4-105">MCI\_STEP command</span></span>

<span data-ttu-id="36cc4-106">MCI \_ 步驟命令會將玩家帶到一或多個畫面。</span><span class="sxs-lookup"><span data-stu-id="36cc4-106">The MCI\_STEP command steps the player one or more frames.</span></span> <span data-ttu-id="36cc4-107">數位影片、VCR 和 CAV 格式的 videodisc 裝置都會辨識此命令。</span><span class="sxs-lookup"><span data-stu-id="36cc4-107">Digital-video, VCR, and CAV-format videodisc devices recognize this command.</span></span>

<span data-ttu-id="36cc4-108">若要傳送此命令，請使用下列參數呼叫 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) 函數。</span><span class="sxs-lookup"><span data-stu-id="36cc4-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_STEP, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpStep
);
```



## <a name="parameters"></a><span data-ttu-id="36cc4-109">參數</span><span class="sxs-lookup"><span data-stu-id="36cc4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36cc4-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="36cc4-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="36cc4-111">要接收命令訊息之 MCI 裝置的裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="36cc4-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="36cc4-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="36cc4-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="36cc4-113">\_ \_ 針對數位-視頻和 VCR 裝置，mci 測試的 mci 通知、mci 等候或 \_ 。</span><span class="sxs-lookup"><span data-stu-id="36cc4-113">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video and VCR devices, MCI\_TEST.</span></span> <span data-ttu-id="36cc4-114">如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。</span><span class="sxs-lookup"><span data-stu-id="36cc4-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="36cc4-115"><span id="lpStep"></span><span id="lpstep"></span><span id="LPSTEP"></span>*lpStep*</span><span class="sxs-lookup"><span data-stu-id="36cc4-115"><span id="lpStep"></span><span id="lpstep"></span><span id="LPSTEP"></span>*lpStep*</span></span>
</dt> <dd>

<span data-ttu-id="36cc4-116">[**MCI \_ 泛型 \_ PARMS**](mci-generic-parms.md)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="36cc4-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="36cc4-117">具有擴充命令集的 (裝置，可能會以裝置特定結構取代此結構。 ) </span><span class="sxs-lookup"><span data-stu-id="36cc4-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36cc4-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="36cc4-118">Return Value</span></span>

<span data-ttu-id="36cc4-119">如果成功則傳回零，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="36cc4-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="36cc4-120">備註</span><span class="sxs-lookup"><span data-stu-id="36cc4-120">Remarks</span></span>

<span data-ttu-id="36cc4-121">此命令支援在 MCI  \_ GETDEVCAPS \_ 具有 \_ [mci \_ GETDEVCAPS](mci-getdevcaps.md)命令的影片旗標時，傳回 TRUE 的裝置。</span><span class="sxs-lookup"><span data-stu-id="36cc4-121">This command supports devices that return **TRUE** to the MCI\_GETDEVCAPS\_HAS\_VIDEO flag of the [MCI\_GETDEVCAPS](mci-getdevcaps.md) command.</span></span>

<span data-ttu-id="36cc4-122">下列其他旗標適用于 **digitalvideo** 裝置類型：</span><span class="sxs-lookup"><span data-stu-id="36cc4-122">The following additional flags are used with the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="36cc4-123"><span id="MCI_DGV_STEP_FRAMES"></span><span id="mci_dgv_step_frames"></span>MCI \_ DGV \_ 步驟 \_ 框架</span><span class="sxs-lookup"><span data-stu-id="36cc4-123"><span id="MCI_DGV_STEP_FRAMES"></span><span id="mci_dgv_step_frames"></span>MCI\_DGV\_STEP\_FRAMES</span></span>
</dt> <dd>

<span data-ttu-id="36cc4-124">*LpStep* 所識別之結構的 **dwFrames** 成員會指定在顯示另一個影像之前要前進的框架數目。</span><span class="sxs-lookup"><span data-stu-id="36cc4-124">The **dwFrames** member of the structure identified by *lpStep* specifies the number of frames to advance before displaying another image.</span></span>

</dd> <dt>

<span data-ttu-id="36cc4-125"><span id="MCI_DGV_STEP_REVERSE"></span><span id="mci_dgv_step_reverse"></span>MCI \_ DGV \_ 步驟 \_ 反轉</span><span class="sxs-lookup"><span data-stu-id="36cc4-125"><span id="MCI_DGV_STEP_REVERSE"></span><span id="mci_dgv_step_reverse"></span>MCI\_DGV\_STEP\_REVERSE</span></span>
</dt> <dd>

<span data-ttu-id="36cc4-126">反向步驟。</span><span class="sxs-lookup"><span data-stu-id="36cc4-126">Steps in reverse.</span></span>

</dd> </dl>

<span data-ttu-id="36cc4-127">針對數位影片裝置， *lpStep* 參數會指向 [**MCI \_ DGV \_ 步驟 \_ PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_step_parms) 結構。</span><span class="sxs-lookup"><span data-stu-id="36cc4-127">For digital-video devices, the *lpStep* parameter points to an [**MCI\_DGV\_STEP\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_step_parms) structure.</span></span>

<span data-ttu-id="36cc4-128">下列其他旗標適用于 **vcr** 裝置類型：</span><span class="sxs-lookup"><span data-stu-id="36cc4-128">The following additional flags are used with the **vcr** device type:</span></span>

<dl> <dt>

<span data-ttu-id="36cc4-129"><span id="MCI_VCR_STEP_FRAMES"></span><span id="mci_vcr_step_frames"></span>MCI \_ VCR \_ 步驟 \_ 框架</span><span class="sxs-lookup"><span data-stu-id="36cc4-129"><span id="MCI_VCR_STEP_FRAMES"></span><span id="mci_vcr_step_frames"></span>MCI\_VCR\_STEP\_FRAMES</span></span>
</dt> <dd>

<span data-ttu-id="36cc4-130">*LpStep* 所識別之結構的 **dwFrames** 成員會指定在顯示另一個影像之前要前進的框架數目。</span><span class="sxs-lookup"><span data-stu-id="36cc4-130">The **dwFrames** member of the structure identified by *lpStep* specifies the number of frames to advance before displaying another image.</span></span>

</dd> <dt>

<span data-ttu-id="36cc4-131"><span id="MCI_VCR_STEP_REVERSE"></span><span id="mci_vcr_step_reverse"></span>MCI \_ VCR \_ 步驟 \_ 反轉</span><span class="sxs-lookup"><span data-stu-id="36cc4-131"><span id="MCI_VCR_STEP_REVERSE"></span><span id="mci_vcr_step_reverse"></span>MCI\_VCR\_STEP\_REVERSE</span></span>
</dt> <dd>

<span data-ttu-id="36cc4-132">反向步驟。</span><span class="sxs-lookup"><span data-stu-id="36cc4-132">Steps in reverse.</span></span>

</dd> </dl>

<span data-ttu-id="36cc4-133">若為 VCR 裝置， *lpStep* 參數會指向 [**MCI \_ VCR \_ 步驟 \_ PARMS**](mci-vcr-step-parms.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="36cc4-133">For VCR devices, the *lpStep* parameter points to an [**MCI\_VCR\_STEP\_PARMS**](mci-vcr-step-parms.md) structure.</span></span>

<span data-ttu-id="36cc4-134">下列其他旗標適用于 **videodisc** 裝置類型：</span><span class="sxs-lookup"><span data-stu-id="36cc4-134">The following additional flags are used with the **videodisc** device type:</span></span>

<dl> <dt>

<span data-ttu-id="36cc4-135"><span id="MCI_VD_STEP_FRAMES"></span><span id="mci_vd_step_frames"></span>MCI \_ VD \_ 步驟 \_ 框架</span><span class="sxs-lookup"><span data-stu-id="36cc4-135"><span id="MCI_VD_STEP_FRAMES"></span><span id="mci_vd_step_frames"></span>MCI\_VD\_STEP\_FRAMES</span></span>
</dt> <dd>

<span data-ttu-id="36cc4-136">由 *lpStep* 所識別之結構的 **dwFrames** 成員會指定要逐步執行的框架數目。</span><span class="sxs-lookup"><span data-stu-id="36cc4-136">The **dwFrames** member of the structure identified by *lpStep* specifies the number of frames to step.</span></span>

</dd> <dt>

<span data-ttu-id="36cc4-137"><span id="MCI_VD_STEP_REVERSE"></span><span id="mci_vd_step_reverse"></span>MCI \_ VD \_ 步驟 \_ 反轉</span><span class="sxs-lookup"><span data-stu-id="36cc4-137"><span id="MCI_VD_STEP_REVERSE"></span><span id="mci_vd_step_reverse"></span>MCI\_VD\_STEP\_REVERSE</span></span>
</dt> <dd>

<span data-ttu-id="36cc4-138">反向步驟。</span><span class="sxs-lookup"><span data-stu-id="36cc4-138">Steps in reverse.</span></span>

</dd> </dl>

<span data-ttu-id="36cc4-139">針對 videodisc 裝置， *lpStep* 參數會指向 [**MCI \_ VD \_ 步驟 \_ PARMS**](mci-vd-step-parms.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="36cc4-139">For videodisc devices, the *lpStep* parameter points to an [**MCI\_VD\_STEP\_PARMS**](mci-vd-step-parms.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="36cc4-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="36cc4-140">Requirements</span></span>



| <span data-ttu-id="36cc4-141">需求</span><span class="sxs-lookup"><span data-stu-id="36cc4-141">Requirement</span></span> | <span data-ttu-id="36cc4-142">值</span><span class="sxs-lookup"><span data-stu-id="36cc4-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36cc4-143">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="36cc4-143">Minimum supported client</span></span><br/> | <span data-ttu-id="36cc4-144">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="36cc4-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="36cc4-145">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="36cc4-145">Minimum supported server</span></span><br/> | <span data-ttu-id="36cc4-146">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="36cc4-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="36cc4-147">標頭</span><span class="sxs-lookup"><span data-stu-id="36cc4-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="36cc4-148"><dt>Mmsystem (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="36cc4-148"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36cc4-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="36cc4-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36cc4-150">Mci</span><span class="sxs-lookup"><span data-stu-id="36cc4-150">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="36cc4-151">MCI 命令</span><span class="sxs-lookup"><span data-stu-id="36cc4-151">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

