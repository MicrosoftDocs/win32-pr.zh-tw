---
title: 'MCI_STOP 命令 (Mmsystem .h) '
description: MCI \_ 停止命令會停止所有播放和記錄順序、卸載所有播放緩衝區，並停止顯示影片影像。 CD 音訊、數位影片、MIDI sequencer、videodisc、VCR 和波形音訊裝置都會辨識此命令。
ms.assetid: e5ae20b3-7439-4314-8354-d06e83b29729
keywords:
- MCI_STOP 命令 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_STOP
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ea5f2acbe39b0be64ebc640ae31ceede7591c7b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384769"
---
# <a name="mci_stop-command"></a><span data-ttu-id="2c1f7-105">MCI \_ 停止命令</span><span class="sxs-lookup"><span data-stu-id="2c1f7-105">MCI\_STOP command</span></span>

<span data-ttu-id="2c1f7-106">MCI \_ 停止命令會停止所有播放和記錄順序、卸載所有播放緩衝區，並停止顯示影片影像。</span><span class="sxs-lookup"><span data-stu-id="2c1f7-106">The MCI\_STOP command stops all play and record sequences, unloads all play buffers, and ceases display of video images.</span></span> <span data-ttu-id="2c1f7-107">CD 音訊、數位影片、MIDI sequencer、videodisc、VCR 和波形音訊裝置都會辨識此命令。</span><span class="sxs-lookup"><span data-stu-id="2c1f7-107">CD audio, digital-video, MIDI sequencer, videodisc, VCR, and waveform-audio devices recognize this command.</span></span>

<span data-ttu-id="2c1f7-108">若要傳送此命令，請使用下列參數呼叫 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) 函數。</span><span class="sxs-lookup"><span data-stu-id="2c1f7-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_STOP, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpStop
);
```



## <a name="parameters"></a><span data-ttu-id="2c1f7-109">參數</span><span class="sxs-lookup"><span data-stu-id="2c1f7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c1f7-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="2c1f7-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="2c1f7-111">要接收命令訊息之 MCI 裝置的裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="2c1f7-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="2c1f7-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="2c1f7-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="2c1f7-113">\_ \_ 針對數位-視頻和 VCR 裝置，mci 測試的 mci 通知、mci 等候或 \_ 。</span><span class="sxs-lookup"><span data-stu-id="2c1f7-113">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video and VCR devices, MCI\_TEST.</span></span> <span data-ttu-id="2c1f7-114">如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。</span><span class="sxs-lookup"><span data-stu-id="2c1f7-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="2c1f7-115"><span id="lpStop"></span><span id="lpstop"></span><span id="LPSTOP"></span>*lpStop*</span><span class="sxs-lookup"><span data-stu-id="2c1f7-115"><span id="lpStop"></span><span id="lpstop"></span><span id="LPSTOP"></span>*lpStop*</span></span>
</dt> <dd>

<span data-ttu-id="2c1f7-116">[**MCI \_ 泛型 \_ PARMS**](mci-generic-parms.md)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="2c1f7-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="2c1f7-117">具有擴充命令集的 (裝置，可能會以裝置特定結構取代此結構。 ) </span><span class="sxs-lookup"><span data-stu-id="2c1f7-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c1f7-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="2c1f7-118">Return Value</span></span>

<span data-ttu-id="2c1f7-119">如果成功則傳回零，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="2c1f7-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="2c1f7-120">備註</span><span class="sxs-lookup"><span data-stu-id="2c1f7-120">Remarks</span></span>

<span data-ttu-id="2c1f7-121">MCI \_ STOP 和 [mci \_ PAUSE](mci-pause.md) 命令之間的差異取決於裝置。</span><span class="sxs-lookup"><span data-stu-id="2c1f7-121">The difference between the MCI\_STOP and [MCI\_PAUSE](mci-pause.md) commands depends on the device.</span></span> <span data-ttu-id="2c1f7-122">可能的話，MCI 會 \_ 暫停裝置操作，但讓裝置可以立即繼續播放。</span><span class="sxs-lookup"><span data-stu-id="2c1f7-122">If possible, MCI\_PAUSE suspends device operation but leaves the device ready to resume play immediately.</span></span>

<span data-ttu-id="2c1f7-123">針對 CD 音訊裝置，MCI 會 \_ 停止將目前的曲目位置重設為零; 相反地， [mci \_ PAUSE](mci-pause.md) 會維持目前的曲目位置，並預期裝置將繼續播放。</span><span class="sxs-lookup"><span data-stu-id="2c1f7-123">For the CD audio device, MCI\_STOP resets the current track position to zero; in contrast, [MCI\_PAUSE](mci-pause.md) maintains the current track position, anticipating that the device will resume playing.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c1f7-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="2c1f7-124">Requirements</span></span>



| <span data-ttu-id="2c1f7-125">需求</span><span class="sxs-lookup"><span data-stu-id="2c1f7-125">Requirement</span></span> | <span data-ttu-id="2c1f7-126">值</span><span class="sxs-lookup"><span data-stu-id="2c1f7-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c1f7-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2c1f7-127">Minimum supported client</span></span><br/> | <span data-ttu-id="2c1f7-128">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2c1f7-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="2c1f7-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2c1f7-129">Minimum supported server</span></span><br/> | <span data-ttu-id="2c1f7-130">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2c1f7-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="2c1f7-131">標頭</span><span class="sxs-lookup"><span data-stu-id="2c1f7-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c1f7-132"><dt>Mmsystem (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="2c1f7-132"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c1f7-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2c1f7-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c1f7-134">Mci</span><span class="sxs-lookup"><span data-stu-id="2c1f7-134">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="2c1f7-135">MCI 命令</span><span class="sxs-lookup"><span data-stu-id="2c1f7-135">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

