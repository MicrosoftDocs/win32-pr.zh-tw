---
title: 'MCI_SIGNAL 命令 (Mmsystem .h) '
description: MCI \_ 信號命令會在工作區中設定指定的位置。 數位影片裝置辨識此命令。 MCIAVI 一次只支援一個作用中的信號。
ms.assetid: 32ca21a0-e2df-47f1-8e13-67c9d8f149db
keywords:
- MCI_SIGNAL 命令 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_SIGNAL
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 711238d73ee40f5809f15a2d6df93183fb17bf67
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384477"
---
# <a name="mci_signal-command"></a><span data-ttu-id="30471-106">MCI \_ 信號命令</span><span class="sxs-lookup"><span data-stu-id="30471-106">MCI\_SIGNAL command</span></span>

<span data-ttu-id="30471-107">MCI \_ 信號命令會在工作區中設定指定的位置。</span><span class="sxs-lookup"><span data-stu-id="30471-107">The MCI\_SIGNAL command sets a specified position in the workspace.</span></span> <span data-ttu-id="30471-108">數位影片裝置辨識此命令。</span><span class="sxs-lookup"><span data-stu-id="30471-108">Digital-video devices recognize this command.</span></span> <span data-ttu-id="30471-109">MCIAVI 一次只支援一個作用中的信號。</span><span class="sxs-lookup"><span data-stu-id="30471-109">MCIAVI supports only one active signal at a time.</span></span>

<span data-ttu-id="30471-110">若要傳送此命令，請使用下列參數呼叫 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) 函數。</span><span class="sxs-lookup"><span data-stu-id="30471-110">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SIGNAL, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_SIGNAL_PARMS) lpSignal
);
```



## <a name="parameters"></a><span data-ttu-id="30471-111">參數</span><span class="sxs-lookup"><span data-stu-id="30471-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30471-112"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="30471-112"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="30471-113">要接收命令訊息之 MCI 裝置的裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="30471-113">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="30471-114"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="30471-114"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="30471-115">MCI \_ 通知、mci \_ 等候或 mci \_ 測試。</span><span class="sxs-lookup"><span data-stu-id="30471-115">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="30471-116">如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。</span><span class="sxs-lookup"><span data-stu-id="30471-116">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="30471-117"><span id="lpSignal"></span><span id="lpsignal"></span><span id="LPSIGNAL"></span>*lpSignal*</span><span class="sxs-lookup"><span data-stu-id="30471-117"><span id="lpSignal"></span><span id="lpsignal"></span><span id="LPSIGNAL"></span>*lpSignal*</span></span>
</dt> <dd>

<span data-ttu-id="30471-118">[**MCI \_ DGV \_ 信號 \_ PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_signal_parms)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="30471-118">Pointer to an [**MCI\_DGV\_SIGNAL\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_signal_parms) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30471-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="30471-119">Return Value</span></span>

<span data-ttu-id="30471-120">如果成功則傳回零，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="30471-120">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="30471-121">備註</span><span class="sxs-lookup"><span data-stu-id="30471-121">Remarks</span></span>

<span data-ttu-id="30471-122">在 [**MCI \_ DGV \_ 信號 \_ PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_signal_parms)結構的 **dwCallback** 成員中指定其控制碼的視窗，會收到 MM \_ MCISIGNAL 訊息。</span><span class="sxs-lookup"><span data-stu-id="30471-122">The window whose handle you specify in the **dwCallback** member of the [**MCI\_DGV\_SIGNAL\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_signal_parms) structure receives the MM\_MCISIGNAL message.</span></span>

<span data-ttu-id="30471-123">下列旗標適用于數位視訊裝置：</span><span class="sxs-lookup"><span data-stu-id="30471-123">The following flags apply to digital-video devices:</span></span>

<dl> <dt>

<span data-ttu-id="30471-124"><span id="MCI_DGV_SIGNAL_AT"></span><span id="mci_dgv_signal_at"></span>MCI \_ DGV \_ 發出信號 \_</span><span class="sxs-lookup"><span data-stu-id="30471-124"><span id="MCI_DGV_SIGNAL_AT"></span><span id="mci_dgv_signal_at"></span>MCI\_DGV\_SIGNAL\_AT</span></span>
</dt> <dd>

<span data-ttu-id="30471-125">信號位置會包含在由 *lpSignal* 所識別之結構的 **dwPosition** 成員中。</span><span class="sxs-lookup"><span data-stu-id="30471-125">A signal position is included in the **dwPosition** member of the structure identified by *lpSignal*.</span></span>

</dd> <dt>

<span data-ttu-id="30471-126"><span id="MCI_DGV_SIGNAL_CANCEL"></span><span id="mci_dgv_signal_cancel"></span>MCI \_ DGV \_ 信號 \_ 取消</span><span class="sxs-lookup"><span data-stu-id="30471-126"><span id="MCI_DGV_SIGNAL_CANCEL"></span><span id="mci_dgv_signal_cancel"></span>MCI\_DGV\_SIGNAL\_CANCEL</span></span>
</dt> <dd>

<span data-ttu-id="30471-127">移除與 MCI \_ DGV 信號 USERVAL 關聯之值所指定的信號位置 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="30471-127">Removes the signal position specified by the value associated with MCI\_DGV\_SIGNAL\_USERVAL.</span></span>

</dd> <dt>

<span data-ttu-id="30471-128"><span id="MCI_DGV_SIGNAL_EVERY"></span><span id="mci_dgv_signal_every"></span>MCI \_ DGV \_ \_ 每個信號</span><span class="sxs-lookup"><span data-stu-id="30471-128"><span id="MCI_DGV_SIGNAL_EVERY"></span><span id="mci_dgv_signal_every"></span>MCI\_DGV\_SIGNAL\_EVERY</span></span>
</dt> <dd>

<span data-ttu-id="30471-129">信號期間值會包含在由 *lpSignal* 所識別之結構的 **dwPeriod** 成員中。</span><span class="sxs-lookup"><span data-stu-id="30471-129">A signal-period value is included in the **dwPeriod** member of the structure identified by *lpSignal*.</span></span>

</dd> <dt>

<span data-ttu-id="30471-130"><span id="MCI_DGV_SIGNAL_POSITION"></span><span id="mci_dgv_signal_position"></span>MCI \_ DGV \_ 信號 \_ 位置</span><span class="sxs-lookup"><span data-stu-id="30471-130"><span id="MCI_DGV_SIGNAL_POSITION"></span><span id="mci_dgv_signal_position"></span>MCI\_DGV\_SIGNAL\_POSITION</span></span>
</dt> <dd>

<span data-ttu-id="30471-131">裝置會傳送位置值與 Windows 訊息，而不是使用者指定的值。</span><span class="sxs-lookup"><span data-stu-id="30471-131">The device will send the position value with the Windows message instead of the user-specified value.</span></span>

</dd> <dt>

<span data-ttu-id="30471-132"><span id="MCI_DGV_SIGNAL_USERVAL"></span><span id="mci_dgv_signal_userval"></span>MCI \_ DGV \_ 信號 \_ USERVAL</span><span class="sxs-lookup"><span data-stu-id="30471-132"><span id="MCI_DGV_SIGNAL_USERVAL"></span><span id="mci_dgv_signal_userval"></span>MCI\_DGV\_SIGNAL\_USERVAL</span></span>
</dt> <dd>

<span data-ttu-id="30471-133">資料值會包含在 *lpSignal* 所識別之結構的 **dwUserParm** 成員中。</span><span class="sxs-lookup"><span data-stu-id="30471-133">A data value is included in the **dwUserParm** member of the structure identified by *lpSignal*.</span></span> <span data-ttu-id="30471-134">與此要求相關聯的資料值會與 Windows 訊息一起回報。</span><span class="sxs-lookup"><span data-stu-id="30471-134">The data value associated with this request is reported back with the Windows message.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="30471-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="30471-135">Requirements</span></span>



| <span data-ttu-id="30471-136">需求</span><span class="sxs-lookup"><span data-stu-id="30471-136">Requirement</span></span> | <span data-ttu-id="30471-137">值</span><span class="sxs-lookup"><span data-stu-id="30471-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30471-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="30471-138">Minimum supported client</span></span><br/> | <span data-ttu-id="30471-139">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="30471-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="30471-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="30471-140">Minimum supported server</span></span><br/> | <span data-ttu-id="30471-141">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="30471-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="30471-142">標頭</span><span class="sxs-lookup"><span data-stu-id="30471-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="30471-143"><dt>Mmsystem (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="30471-143"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30471-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="30471-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30471-145">Mci</span><span class="sxs-lookup"><span data-stu-id="30471-145">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="30471-146">MCI 命令</span><span class="sxs-lookup"><span data-stu-id="30471-146">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

