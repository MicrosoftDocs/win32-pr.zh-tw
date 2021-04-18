---
title: 'MCI_REALIZE 命令 (Mmsystem .h) '
description: MCI 的「 \_ 實現」命令會使圖形裝置將其選擇區實現到 (DC) 的裝置內容中。 數位影片裝置辨識此命令。
ms.assetid: cbc9e6ef-a372-4ddb-b7f3-ea99ac14ec95
keywords:
- MCI_REALIZE 命令 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_REALIZE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35f2e59bfe9bbe1443f55ae0fbcf8819b932bb1c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965712"
---
# <a name="mci_realize-command"></a><span data-ttu-id="9f543-105">MCI \_ 實現命令</span><span class="sxs-lookup"><span data-stu-id="9f543-105">MCI\_REALIZE command</span></span>

<span data-ttu-id="9f543-106">MCI 的「 \_ 實現」命令會使圖形裝置將其選擇區實現到 (DC) 的裝置內容中。</span><span class="sxs-lookup"><span data-stu-id="9f543-106">The MCI\_REALIZE command causes a graphic device to realize its palette into a device context (DC).</span></span> <span data-ttu-id="9f543-107">數位影片裝置辨識此命令。</span><span class="sxs-lookup"><span data-stu-id="9f543-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="9f543-108">若要傳送此命令，請使用下列參數呼叫 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) 函數。</span><span class="sxs-lookup"><span data-stu-id="9f543-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_REALIZE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpRealize
);
```



## <a name="parameters"></a><span data-ttu-id="9f543-109">參數</span><span class="sxs-lookup"><span data-stu-id="9f543-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f543-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="9f543-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="9f543-111">要接收命令訊息之 MCI 裝置的裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="9f543-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="9f543-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="9f543-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="9f543-113">**MCI \_通知**、 **mci \_ 等候**，或適用于數位影片裝置、 **mci \_ 測試**。</span><span class="sxs-lookup"><span data-stu-id="9f543-113">**MCI\_NOTIFY**, **MCI\_WAIT**, or, for digital-video devices, **MCI\_TEST**.</span></span> <span data-ttu-id="9f543-114">如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。</span><span class="sxs-lookup"><span data-stu-id="9f543-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="9f543-115"><span id="lpRealize"></span><span id="lprealize"></span><span id="LPREALIZE"></span>*lpRealize*</span><span class="sxs-lookup"><span data-stu-id="9f543-115"><span id="lpRealize"></span><span id="lprealize"></span><span id="LPREALIZE"></span>*lpRealize*</span></span>
</dt> <dd>

<span data-ttu-id="9f543-116">[**MCI \_ 泛型 \_ PARMS**](mci-generic-parms.md)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="9f543-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="9f543-117">具有擴充命令集的 (裝置，可能會以裝置特定結構取代此結構。 ) </span><span class="sxs-lookup"><span data-stu-id="9f543-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f543-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="9f543-118">Return Value</span></span>

<span data-ttu-id="9f543-119">如果成功則傳回零，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="9f543-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="9f543-120">備註</span><span class="sxs-lookup"><span data-stu-id="9f543-120">Remarks</span></span>

<span data-ttu-id="9f543-121">當您的應用程式收到 [**WM \_ QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette) 訊息時，您應該使用此命令。</span><span class="sxs-lookup"><span data-stu-id="9f543-121">You should use this command when your application receives the [**WM\_QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette) message.</span></span>

<span data-ttu-id="9f543-122">下列其他旗標會搭配 "digitalvideo" 裝置類型使用：</span><span class="sxs-lookup"><span data-stu-id="9f543-122">The following additional flags are used with the "digitalvideo" device type:</span></span>

<dl> <dt>

<span data-ttu-id="9f543-123"><span id="MCI_DGV_REALIZE_BKGD"></span><span id="mci_dgv_realize_bkgd"></span>MCI \_ DGV \_ 實現 \_ BKGD</span><span class="sxs-lookup"><span data-stu-id="9f543-123"><span id="MCI_DGV_REALIZE_BKGD"></span><span id="mci_dgv_realize_bkgd"></span>MCI\_DGV\_REALIZE\_BKGD</span></span>
</dt> <dd>

<span data-ttu-id="9f543-124">將調色板視為背景調色板。</span><span class="sxs-lookup"><span data-stu-id="9f543-124">Realizes the palette as a background palette.</span></span>

</dd> <dt>

<span data-ttu-id="9f543-125"><span id="MCI_DGV_REALIZE_NORM"></span><span id="mci_dgv_realize_norm"></span>MCI \_ DGV \_ 實現 \_ 標準</span><span class="sxs-lookup"><span data-stu-id="9f543-125"><span id="MCI_DGV_REALIZE_NORM"></span><span id="mci_dgv_realize_norm"></span>MCI\_DGV\_REALIZE\_NORM</span></span>
</dt> <dd>

<span data-ttu-id="9f543-126">正常地發現調色板。</span><span class="sxs-lookup"><span data-stu-id="9f543-126">Realizes the palette normally.</span></span> <span data-ttu-id="9f543-127">此為預設值。</span><span class="sxs-lookup"><span data-stu-id="9f543-127">This is the default.</span></span>

</dd> </dl>

<span data-ttu-id="9f543-128">針對數位影片裝置， *lpRealize* 參數會指向 **MCI \_ 實現 \_ PARMS** 結構。</span><span class="sxs-lookup"><span data-stu-id="9f543-128">For digital-video devices, the *lpRealize* parameter points to an **MCI\_REALIZE\_PARMS** structure.</span></span> <span data-ttu-id="9f543-129">如需詳細資訊，請參閱 [**MCI \_ 一般 \_ PARMS**](mci-generic-parms.md) 結構中的批註。</span><span class="sxs-lookup"><span data-stu-id="9f543-129">For more information, see comments in the [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f543-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="9f543-130">Requirements</span></span>



| <span data-ttu-id="9f543-131">需求</span><span class="sxs-lookup"><span data-stu-id="9f543-131">Requirement</span></span> | <span data-ttu-id="9f543-132">值</span><span class="sxs-lookup"><span data-stu-id="9f543-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f543-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9f543-133">Minimum supported client</span></span><br/> | <span data-ttu-id="9f543-134">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9f543-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="9f543-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9f543-135">Minimum supported server</span></span><br/> | <span data-ttu-id="9f543-136">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9f543-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="9f543-137">標頭</span><span class="sxs-lookup"><span data-stu-id="9f543-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="9f543-138"><dt>Mmsystem (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="9f543-138"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f543-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9f543-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f543-140">Mci</span><span class="sxs-lookup"><span data-stu-id="9f543-140">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="9f543-141">MCI 命令</span><span class="sxs-lookup"><span data-stu-id="9f543-141">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

