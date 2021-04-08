---
title: 'MCI_PAUSE 命令 (Mmsystem .h) '
description: MCI \_ PAUSE 命令會暫停目前的動作。 CD 音訊、數位影片、MIDI sequencer、VCR、videodisc 和波形-音訊裝置都會辨識此命令。
ms.assetid: c4d0b0a2-cd7b-4641-a318-eb4b4e88b70f
keywords:
- MCI_PAUSE 命令 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_PAUSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b076397ca9ab770d6f9c23cc5b64853bdd2f07ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685488"
---
# <a name="mci_pause-command"></a><span data-ttu-id="6bffe-105">MCI \_ PAUSE 命令</span><span class="sxs-lookup"><span data-stu-id="6bffe-105">MCI\_PAUSE command</span></span>

<span data-ttu-id="6bffe-106">MCI \_ PAUSE 命令會暫停目前的動作。</span><span class="sxs-lookup"><span data-stu-id="6bffe-106">The MCI\_PAUSE command pauses the current action.</span></span> <span data-ttu-id="6bffe-107">CD 音訊、數位影片、MIDI sequencer、VCR、videodisc 和波形-音訊裝置都會辨識此命令。</span><span class="sxs-lookup"><span data-stu-id="6bffe-107">CD audio, digital-video, MIDI sequencer, VCR, videodisc, and waveform-audio devices recognize this command.</span></span>

<span data-ttu-id="6bffe-108">若要傳送此命令，請使用下列參數呼叫 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) 函數。</span><span class="sxs-lookup"><span data-stu-id="6bffe-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_PAUSE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpPause
);
```



## <a name="parameters"></a><span data-ttu-id="6bffe-109">參數</span><span class="sxs-lookup"><span data-stu-id="6bffe-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6bffe-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="6bffe-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="6bffe-111">要接收命令訊息之 MCI 裝置的裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="6bffe-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="6bffe-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="6bffe-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="6bffe-113">\_ \_ 針對數位-視頻和 VCR 裝置，mci 測試的 mci 通知、mci 等候或 \_ 。</span><span class="sxs-lookup"><span data-stu-id="6bffe-113">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video and VCR devices, MCI\_TEST.</span></span> <span data-ttu-id="6bffe-114">如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。</span><span class="sxs-lookup"><span data-stu-id="6bffe-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="6bffe-115"><span id="lpPause"></span><span id="lppause"></span><span id="LPPAUSE"></span>*lpPause*</span><span class="sxs-lookup"><span data-stu-id="6bffe-115"><span id="lpPause"></span><span id="lppause"></span><span id="LPPAUSE"></span>*lpPause*</span></span>
</dt> <dd>

<span data-ttu-id="6bffe-116">[**MCI \_ 泛型 \_ PARMS**](mci-generic-parms.md)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="6bffe-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="6bffe-117">具有擴充命令集的 (裝置，可能會以裝置特定結構取代此結構。 ) </span><span class="sxs-lookup"><span data-stu-id="6bffe-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6bffe-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="6bffe-118">Return Value</span></span>

<span data-ttu-id="6bffe-119">如果成功則傳回零，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="6bffe-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="6bffe-120">備註</span><span class="sxs-lookup"><span data-stu-id="6bffe-120">Remarks</span></span>

<span data-ttu-id="6bffe-121">[Mci \_ STOP](mci-stop.md)和 mci PAUSE 命令之間的差異 \_ 取決於裝置。</span><span class="sxs-lookup"><span data-stu-id="6bffe-121">The difference between the [MCI\_STOP](mci-stop.md) and MCI\_PAUSE commands depends on the device.</span></span> <span data-ttu-id="6bffe-122">可能的話，MCI 會 \_ 暫停裝置操作，但讓裝置可以立即繼續播放。</span><span class="sxs-lookup"><span data-stu-id="6bffe-122">If possible, MCI\_PAUSE suspends device operation but leaves the device ready to resume play immediately.</span></span> <span data-ttu-id="6bffe-123">使用 MCICDA、MCISEQ 和 MCIPIONR 驅動程式時，MCI \_ PAUSE 命令的運作方式與 mci \_ STOP 命令相同。</span><span class="sxs-lookup"><span data-stu-id="6bffe-123">With the MCICDA, MCISEQ, and MCIPIONR drivers, the MCI\_PAUSE command works the same as the MCI\_STOP command.</span></span>

<span data-ttu-id="6bffe-124">針對數位影片裝置， *lpPause* 參數會指向 [**MCI \_ DGV \_ PAUSE \_ PARMS**](/previous-versions//dd743395(v=vs.85)) 結構。</span><span class="sxs-lookup"><span data-stu-id="6bffe-124">For digital-video devices, the *lpPause* parameter points to an [**MCI\_DGV\_PAUSE\_PARMS**](/previous-versions//dd743395(v=vs.85)) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="6bffe-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="6bffe-125">Requirements</span></span>



| <span data-ttu-id="6bffe-126">需求</span><span class="sxs-lookup"><span data-stu-id="6bffe-126">Requirement</span></span> | <span data-ttu-id="6bffe-127">值</span><span class="sxs-lookup"><span data-stu-id="6bffe-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6bffe-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6bffe-128">Minimum supported client</span></span><br/> | <span data-ttu-id="6bffe-129">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6bffe-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="6bffe-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6bffe-130">Minimum supported server</span></span><br/> | <span data-ttu-id="6bffe-131">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6bffe-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="6bffe-132">標頭</span><span class="sxs-lookup"><span data-stu-id="6bffe-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="6bffe-133"><dt>Mmsystem (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="6bffe-133"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6bffe-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6bffe-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6bffe-135">Mci</span><span class="sxs-lookup"><span data-stu-id="6bffe-135">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="6bffe-136">MCI 命令</span><span class="sxs-lookup"><span data-stu-id="6bffe-136">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

