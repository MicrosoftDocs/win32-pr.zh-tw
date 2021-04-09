---
title: 'MCI_MONITOR 命令 (Mmsystem .h) '
description: MCI \_ 監視器命令會指定展示來源。 數位影片裝置辨識此命令。
ms.assetid: b6c476ef-d1a4-477d-a104-dda10be60915
keywords:
- MCI_MONITOR 命令 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_MONITOR
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6aa2f36b0e486143dc348d2e150422b2b082ecf7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934684"
---
# <a name="mci_monitor-command"></a><span data-ttu-id="bf39d-105">MCI \_ 監視器命令</span><span class="sxs-lookup"><span data-stu-id="bf39d-105">MCI\_MONITOR command</span></span>

<span data-ttu-id="bf39d-106">MCI \_ 監視器命令會指定展示來源。</span><span class="sxs-lookup"><span data-stu-id="bf39d-106">The MCI\_MONITOR command specifies the presentation source.</span></span> <span data-ttu-id="bf39d-107">數位影片裝置辨識此命令。</span><span class="sxs-lookup"><span data-stu-id="bf39d-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="bf39d-108">若要傳送此命令，請使用下列參數呼叫 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) 函數。</span><span class="sxs-lookup"><span data-stu-id="bf39d-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_MONITOR, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_MONITOR_PARMS) lpMonitor
);
```



## <a name="parameters"></a><span data-ttu-id="bf39d-109">參數</span><span class="sxs-lookup"><span data-stu-id="bf39d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf39d-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="bf39d-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="bf39d-111">要接收命令訊息之 MCI 裝置的裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="bf39d-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="bf39d-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="bf39d-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="bf39d-113">MCI \_ 通知、mci \_ 等候或 mci \_ 測試。</span><span class="sxs-lookup"><span data-stu-id="bf39d-113">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="bf39d-114">如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。</span><span class="sxs-lookup"><span data-stu-id="bf39d-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="bf39d-115"><span id="lpMonitor"></span><span id="lpmonitor"></span><span id="LPMONITOR"></span>*lpMonitor*</span><span class="sxs-lookup"><span data-stu-id="bf39d-115"><span id="lpMonitor"></span><span id="lpmonitor"></span><span id="LPMONITOR"></span>*lpMonitor*</span></span>
</dt> <dd>

<span data-ttu-id="bf39d-116">[**MCI \_ DGV \_ 監視 \_ PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_monitor_parms)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="bf39d-116">Pointer to an [**MCI\_DGV\_MONITOR\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_monitor_parms) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf39d-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="bf39d-117">Return Value</span></span>

<span data-ttu-id="bf39d-118">如果成功則傳回零，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="bf39d-118">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="bf39d-119">備註</span><span class="sxs-lookup"><span data-stu-id="bf39d-119">Remarks</span></span>

<span data-ttu-id="bf39d-120">下列其他旗標適用于數位視訊裝置：</span><span class="sxs-lookup"><span data-stu-id="bf39d-120">The following additional flags apply to digital-video devices:</span></span>

<dl> <dt>

<span data-ttu-id="bf39d-121"><span id="MCI_DGV_MONITOR_METHOD"></span><span id="mci_dgv_monitor_method"></span>MCI \_ DGV \_ 監視 \_ 方法</span><span class="sxs-lookup"><span data-stu-id="bf39d-121"><span id="MCI_DGV_MONITOR_METHOD"></span><span id="mci_dgv_monitor_method"></span>MCI\_DGV\_MONITOR\_METHOD</span></span>
</dt> <dd>

<span data-ttu-id="bf39d-122">常數，表示監視的方法會包含在 *lpMonitor* 所識別之結構的 **dwMethod** 成員中。</span><span class="sxs-lookup"><span data-stu-id="bf39d-122">A constant indicating the method of monitoring is included in the **dwMethod** member of the structure identified by *lpMonitor*.</span></span>

<span data-ttu-id="bf39d-123">在 \_ \_ \_ **DWSOURCE** 成員中使用 MCI DGV 監視器輸入旗標時，這會選取監視的方法。</span><span class="sxs-lookup"><span data-stu-id="bf39d-123">When the MCI\_DGV\_MONITOR\_INPUT flag is used in the **dwSource** member, this selects the method of monitoring.</span></span> <span data-ttu-id="bf39d-124">一般而言，不同的監視方法對硬體的使用方式有不同的影響。</span><span class="sxs-lookup"><span data-stu-id="bf39d-124">Typically, different monitoring methods have different implications on how the hardware is used.</span></span> <span data-ttu-id="bf39d-125">裝置會選取預設的監視方法。</span><span class="sxs-lookup"><span data-stu-id="bf39d-125">The default monitoring method is selected by the device.</span></span>

</dd> <dt>

<span data-ttu-id="bf39d-126"><span id="MCI_DGV_MONITOR_SOURCE"></span><span id="mci_dgv_monitor_source"></span>MCI \_ DGV \_ 監視 \_ 來源</span><span class="sxs-lookup"><span data-stu-id="bf39d-126"><span id="MCI_DGV_MONITOR_SOURCE"></span><span id="mci_dgv_monitor_source"></span>MCI\_DGV\_MONITOR\_SOURCE</span></span>
</dt> <dd>

<span data-ttu-id="bf39d-127">常數，表示監視器來源包含在 *lpMonitor* 所識別之結構的 **dwSource** 成員中。</span><span class="sxs-lookup"><span data-stu-id="bf39d-127">A constant indicating the monitor source is included in the **dwSource** member of the structure identified by *lpMonitor*.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bf39d-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="bf39d-128">Requirements</span></span>



| <span data-ttu-id="bf39d-129">需求</span><span class="sxs-lookup"><span data-stu-id="bf39d-129">Requirement</span></span> | <span data-ttu-id="bf39d-130">值</span><span class="sxs-lookup"><span data-stu-id="bf39d-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf39d-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bf39d-131">Minimum supported client</span></span><br/> | <span data-ttu-id="bf39d-132">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bf39d-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="bf39d-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bf39d-133">Minimum supported server</span></span><br/> | <span data-ttu-id="bf39d-134">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bf39d-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="bf39d-135">標頭</span><span class="sxs-lookup"><span data-stu-id="bf39d-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="bf39d-136"><dt>Mmsystem (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="bf39d-136"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf39d-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bf39d-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf39d-138">Mci</span><span class="sxs-lookup"><span data-stu-id="bf39d-138">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="bf39d-139">MCI 命令</span><span class="sxs-lookup"><span data-stu-id="bf39d-139">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

