---
title: 'MCI_SPIN 命令 (Mmsystem .h) '
description: MCI \_ 微調命令會啟動裝置向上或向下轉動。 Videodisc 裝置會辨識此命令。
ms.assetid: 9e491455-d06d-44c6-8aca-6360384ec266
keywords:
- MCI_SPIN 命令 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_SPIN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0b154d9a2f54248ac6174e71a24d4afe74918d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384474"
---
# <a name="mci_spin-command"></a><span data-ttu-id="2f155-105">MCI \_ 微調命令</span><span class="sxs-lookup"><span data-stu-id="2f155-105">MCI\_SPIN command</span></span>

<span data-ttu-id="2f155-106">MCI \_ 微調命令會啟動裝置向上或向下轉動。</span><span class="sxs-lookup"><span data-stu-id="2f155-106">The MCI\_SPIN command starts the device spinning up or down.</span></span> <span data-ttu-id="2f155-107">Videodisc 裝置會辨識此命令。</span><span class="sxs-lookup"><span data-stu-id="2f155-107">Videodisc devices recognize this command.</span></span>

<span data-ttu-id="2f155-108">若要傳送此命令，請使用下列參數呼叫 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) 函數。</span><span class="sxs-lookup"><span data-stu-id="2f155-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SPIN, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpSpin
);
```



## <a name="parameters"></a><span data-ttu-id="2f155-109">參數</span><span class="sxs-lookup"><span data-stu-id="2f155-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f155-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="2f155-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="2f155-111">要接收命令訊息之 MCI 裝置的裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="2f155-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="2f155-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="2f155-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="2f155-113">MCI \_ 通知或 mci \_ 等候。</span><span class="sxs-lookup"><span data-stu-id="2f155-113">MCI\_NOTIFY or MCI\_WAIT.</span></span> <span data-ttu-id="2f155-114">如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。</span><span class="sxs-lookup"><span data-stu-id="2f155-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="2f155-115"><span id="lpSpin"></span><span id="lpspin"></span><span id="LPSPIN"></span>*lpSpin*</span><span class="sxs-lookup"><span data-stu-id="2f155-115"><span id="lpSpin"></span><span id="lpspin"></span><span id="LPSPIN"></span>*lpSpin*</span></span>
</dt> <dd>

<span data-ttu-id="2f155-116">[**MCI \_ 泛型 \_ PARMS**](mci-generic-parms.md)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="2f155-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="2f155-117">具有擴充命令集的 (裝置，可能會以裝置特定結構取代此結構。 ) </span><span class="sxs-lookup"><span data-stu-id="2f155-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f155-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="2f155-118">Return Value</span></span>

<span data-ttu-id="2f155-119">如果成功則傳回零，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="2f155-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="2f155-120">備註</span><span class="sxs-lookup"><span data-stu-id="2f155-120">Remarks</span></span>

<span data-ttu-id="2f155-121">下列其他旗標適用于 videodisc 裝置：</span><span class="sxs-lookup"><span data-stu-id="2f155-121">The following additional flags apply to videodisc devices:</span></span>

<dl> <dt>

<span data-ttu-id="2f155-122"><span id="MCI_VD_SPIN_DOWN"></span><span id="mci_vd_spin_down"></span>MCI \_ VD \_ 微調 \_</span><span class="sxs-lookup"><span data-stu-id="2f155-122"><span id="MCI_VD_SPIN_DOWN"></span><span id="mci_vd_spin_down"></span>MCI\_VD\_SPIN\_DOWN</span></span>
</dt> <dd>

<span data-ttu-id="2f155-123">停止光碟旋轉。</span><span class="sxs-lookup"><span data-stu-id="2f155-123">Stops the disc spinning.</span></span>

</dd> <dt>

<span data-ttu-id="2f155-124"><span id="MCI_VD_SPIN_UP"></span><span id="mci_vd_spin_up"></span>MCI \_ VD \_ 加速 \_</span><span class="sxs-lookup"><span data-stu-id="2f155-124"><span id="MCI_VD_SPIN_UP"></span><span id="mci_vd_spin_up"></span>MCI\_VD\_SPIN\_UP</span></span>
</dt> <dd>

<span data-ttu-id="2f155-125">開始旋轉磁片。</span><span class="sxs-lookup"><span data-stu-id="2f155-125">Starts the disc spinning.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2f155-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="2f155-126">Requirements</span></span>



| <span data-ttu-id="2f155-127">需求</span><span class="sxs-lookup"><span data-stu-id="2f155-127">Requirement</span></span> | <span data-ttu-id="2f155-128">值</span><span class="sxs-lookup"><span data-stu-id="2f155-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f155-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2f155-129">Minimum supported client</span></span><br/> | <span data-ttu-id="2f155-130">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2f155-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="2f155-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2f155-131">Minimum supported server</span></span><br/> | <span data-ttu-id="2f155-132">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2f155-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="2f155-133">標頭</span><span class="sxs-lookup"><span data-stu-id="2f155-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f155-134"><dt>Mmsystem (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="2f155-134"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f155-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2f155-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f155-136">Mci</span><span class="sxs-lookup"><span data-stu-id="2f155-136">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="2f155-137">MCI 命令</span><span class="sxs-lookup"><span data-stu-id="2f155-137">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

