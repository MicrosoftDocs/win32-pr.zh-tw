---
title: 'MCI_LOAD 命令 (Mmsystem .h) '
description: MCI \_ LOAD 命令會載入檔案。 數位影片和影片重迭裝置會辨識此命令。
ms.assetid: 0f48afa0-e845-4de5-8433-15bbf4eae683
keywords:
- MCI_LOAD 命令 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_LOAD
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb00ebe9dc9107c4673fc323fcb7719a89beffd4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103933901"
---
# <a name="mci_load-command"></a><span data-ttu-id="d9a18-105">MCI \_ LOAD 命令</span><span class="sxs-lookup"><span data-stu-id="d9a18-105">MCI\_LOAD command</span></span>

<span data-ttu-id="d9a18-106">MCI \_ LOAD 命令會載入檔案。</span><span class="sxs-lookup"><span data-stu-id="d9a18-106">The MCI\_LOAD command loads a file.</span></span> <span data-ttu-id="d9a18-107">數位影片和影片重迭裝置會辨識此命令。</span><span class="sxs-lookup"><span data-stu-id="d9a18-107">Digital-video and video-overlay devices recognize this command.</span></span>

<span data-ttu-id="d9a18-108">若要傳送此命令，請使用下列參數呼叫 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) 函數。</span><span class="sxs-lookup"><span data-stu-id="d9a18-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_LOAD, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_LOAD_PARMS) lpLoad
);
```



## <a name="parameters"></a><span data-ttu-id="d9a18-109">參數</span><span class="sxs-lookup"><span data-stu-id="d9a18-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9a18-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="d9a18-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="d9a18-111">要接收命令訊息之 MCI 裝置的裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="d9a18-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="d9a18-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="d9a18-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="d9a18-113">\_ \_ 適用于數位視訊裝置、mci 測試的 mci 通知、mci 等待或 \_ 。</span><span class="sxs-lookup"><span data-stu-id="d9a18-113">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video devices, MCI\_TEST.</span></span> <span data-ttu-id="d9a18-114">如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。</span><span class="sxs-lookup"><span data-stu-id="d9a18-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="d9a18-115"><span id="lpLoad"></span><span id="lpload"></span><span id="LPLOAD"></span>*lpLoad*</span><span class="sxs-lookup"><span data-stu-id="d9a18-115"><span id="lpLoad"></span><span id="lpload"></span><span id="LPLOAD"></span>*lpLoad*</span></span>
</dt> <dd>

<span data-ttu-id="d9a18-116">[**MCI \_ LOAD \_ PARMS**](mci-load-parms.md)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="d9a18-116">Pointer to an [**MCI\_LOAD\_PARMS**](mci-load-parms.md) structure.</span></span> <span data-ttu-id="d9a18-117">具有其他參數的 (裝置，可能會以裝置特定的結構取代此結構。</span><span class="sxs-lookup"><span data-stu-id="d9a18-117">(Devices with additional parameters might replace this structure with a device-specific structure.</span></span> <span data-ttu-id="d9a18-118">針對數位影片裝置， **lpLoad** 參數會指向 [**MCI \_ DGV \_ LOAD \_ PARMS**](/previous-versions//dd743391(v=vs.85)) 結構。 ) </span><span class="sxs-lookup"><span data-stu-id="d9a18-118">For digital-video devices, the **lpLoad** parameter points to an [**MCI\_DGV\_LOAD\_PARMS**](/previous-versions//dd743391(v=vs.85)) structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9a18-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="d9a18-119">Return Value</span></span>

<span data-ttu-id="d9a18-120">如果成功則傳回零，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="d9a18-120">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="d9a18-121">備註</span><span class="sxs-lookup"><span data-stu-id="d9a18-121">Remarks</span></span>

<span data-ttu-id="d9a18-122">下列其他旗標適用于所有支援 MCI 負載的裝置 \_ ：</span><span class="sxs-lookup"><span data-stu-id="d9a18-122">The following additional flag applies to all devices supporting MCI\_LOAD:</span></span>

<dl> <dt>

<span data-ttu-id="d9a18-123"><span id="MCI_LOAD_FILE"></span><span id="mci_load_file"></span>MCI \_ 載入 \_ 檔</span><span class="sxs-lookup"><span data-stu-id="d9a18-123"><span id="MCI_LOAD_FILE"></span><span id="mci_load_file"></span>MCI\_LOAD\_FILE</span></span>
</dt> <dd>

<span data-ttu-id="d9a18-124">*LpLoad* 所識別之結構的 **lpfilename** 成員包含包含檔案名之緩衝區的位址。</span><span class="sxs-lookup"><span data-stu-id="d9a18-124">The **lpfilename** member of the structure identified by *lpLoad* contains an address of a buffer containing the filename.</span></span>

</dd> </dl>

<span data-ttu-id="d9a18-125">下列其他旗標會搭配覆迭 **裝置類型** 使用：</span><span class="sxs-lookup"><span data-stu-id="d9a18-125">The following additional flag is used with the **overlay** device type:</span></span>

<dl> <dt>

<span data-ttu-id="d9a18-126"><span id="MCI_OVLY_RECT"></span><span id="mci_ovly_rect"></span>MCI \_ OVLY \_ RECT</span><span class="sxs-lookup"><span data-stu-id="d9a18-126"><span id="MCI_OVLY_RECT"></span><span id="mci_ovly_rect"></span>MCI\_OVLY\_RECT</span></span>
</dt> <dd>

<span data-ttu-id="d9a18-127">*LpLoad* 所識別之結構的 **rc** 成員包含有效的顯示矩形，可識別要更新的影片緩衝區區域。</span><span class="sxs-lookup"><span data-stu-id="d9a18-127">The **rc** member of the structure identified by *lpLoad* contains a valid display rectangle that identifies the area of the video buffer to update.</span></span>

</dd> </dl>

<span data-ttu-id="d9a18-128">針對影片重迭裝置， *lpLoad* 參數會指向 [**MCI \_ OVLY \_ LOAD \_ PARMS**](mci-ovly-load-parms.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="d9a18-128">For video-overlay devices, the *lpLoad* parameter points to an [**MCI\_OVLY\_LOAD\_PARMS**](mci-ovly-load-parms.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9a18-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="d9a18-129">Requirements</span></span>



| <span data-ttu-id="d9a18-130">需求</span><span class="sxs-lookup"><span data-stu-id="d9a18-130">Requirement</span></span> | <span data-ttu-id="d9a18-131">值</span><span class="sxs-lookup"><span data-stu-id="d9a18-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9a18-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d9a18-132">Minimum supported client</span></span><br/> | <span data-ttu-id="d9a18-133">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d9a18-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="d9a18-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d9a18-134">Minimum supported server</span></span><br/> | <span data-ttu-id="d9a18-135">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d9a18-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="d9a18-136">標頭</span><span class="sxs-lookup"><span data-stu-id="d9a18-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="d9a18-137"><dt>Mmsystem (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="d9a18-137"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9a18-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d9a18-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9a18-139">Mci</span><span class="sxs-lookup"><span data-stu-id="d9a18-139">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="d9a18-140">MCI 命令</span><span class="sxs-lookup"><span data-stu-id="d9a18-140">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

