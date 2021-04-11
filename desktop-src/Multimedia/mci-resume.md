---
title: 'MCI_RESUME 命令 (Mmsystem .h) '
description: MCI \_ resume 命令會導致暫停的裝置繼續暫停的操作。
ms.assetid: 2df712c1-5005-4e89-a439-a651076bbb73
keywords:
- MCI_RESUME 命令 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_RESUME
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd83b6d753cd223235b8b11f2d4b0be4c828ec28
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934034"
---
# <a name="mci_resume-command"></a><span data-ttu-id="5c638-104">MCI \_ RESUME 命令</span><span class="sxs-lookup"><span data-stu-id="5c638-104">MCI\_RESUME command</span></span>

<span data-ttu-id="5c638-105">MCI \_ resume 命令會導致暫停的裝置繼續暫停的操作。</span><span class="sxs-lookup"><span data-stu-id="5c638-105">The MCI\_RESUME command causes a paused device to resume the paused operation.</span></span> <span data-ttu-id="5c638-106">數位-影片、VCR 和波形-音訊裝置會辨識此命令。</span><span class="sxs-lookup"><span data-stu-id="5c638-106">Digital-video, VCR, and waveform-audio devices recognize this command.</span></span> <span data-ttu-id="5c638-107">雖然 CD 音訊、MIDI sequencer 和 videodisc 裝置也會辨識此命令，但 MCICDA、MCISEQ 和 MCIPIONR 設備磁碟機並不支援。</span><span class="sxs-lookup"><span data-stu-id="5c638-107">Although CD audio, MIDI sequencer, and videodisc devices also recognize this command, the MCICDA, MCISEQ, and MCIPIONR device drivers do not support it.</span></span>

<span data-ttu-id="5c638-108">若要傳送此命令，請使用下列參數呼叫 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) 函數。</span><span class="sxs-lookup"><span data-stu-id="5c638-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_RESUME, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpResume
);
```



## <a name="parameters"></a><span data-ttu-id="5c638-109">參數</span><span class="sxs-lookup"><span data-stu-id="5c638-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c638-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="5c638-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="5c638-111">要接收命令訊息之 MCI 裝置的裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="5c638-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="5c638-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="5c638-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="5c638-113">\_ \_ 針對數位-視頻和 VCR 裝置，mci 測試的 mci 通知、mci 等候或 \_ 。</span><span class="sxs-lookup"><span data-stu-id="5c638-113">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video and VCR devices, MCI\_TEST.</span></span> <span data-ttu-id="5c638-114">如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。</span><span class="sxs-lookup"><span data-stu-id="5c638-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="5c638-115"><span id="lpResume"></span><span id="lpresume"></span><span id="LPRESUME"></span>*lpResume*</span><span class="sxs-lookup"><span data-stu-id="5c638-115"><span id="lpResume"></span><span id="lpresume"></span><span id="LPRESUME"></span>*lpResume*</span></span>
</dt> <dd>

<span data-ttu-id="5c638-116">[**MCI \_ 泛型 \_ PARMS**](mci-generic-parms.md)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="5c638-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="5c638-117">具有擴充命令集的 (裝置，可能會以裝置特定結構取代此結構。 ) </span><span class="sxs-lookup"><span data-stu-id="5c638-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c638-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="5c638-118">Return Value</span></span>

<span data-ttu-id="5c638-119">如果成功則傳回零，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="5c638-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="5c638-120">備註</span><span class="sxs-lookup"><span data-stu-id="5c638-120">Remarks</span></span>

<span data-ttu-id="5c638-121">此命令會繼續播放和錄製，而不會變更使用 [mci \_ PLAY](mci-play.md) 或 [mci \_ 記錄](mci-record.md)所設定的目前曲目位置。</span><span class="sxs-lookup"><span data-stu-id="5c638-121">This command resumes playing and recording without changing the current track position set with [MCI\_PLAY](mci-play.md) or [MCI\_RECORD](mci-record.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5c638-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="5c638-122">Requirements</span></span>



| <span data-ttu-id="5c638-123">需求</span><span class="sxs-lookup"><span data-stu-id="5c638-123">Requirement</span></span> | <span data-ttu-id="5c638-124">值</span><span class="sxs-lookup"><span data-stu-id="5c638-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c638-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5c638-125">Minimum supported client</span></span><br/> | <span data-ttu-id="5c638-126">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5c638-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="5c638-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5c638-127">Minimum supported server</span></span><br/> | <span data-ttu-id="5c638-128">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5c638-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="5c638-129">標頭</span><span class="sxs-lookup"><span data-stu-id="5c638-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="5c638-130"><dt>Mmsystem (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="5c638-130"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c638-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5c638-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c638-132">Mci</span><span class="sxs-lookup"><span data-stu-id="5c638-132">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="5c638-133">MCI 命令</span><span class="sxs-lookup"><span data-stu-id="5c638-133">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

