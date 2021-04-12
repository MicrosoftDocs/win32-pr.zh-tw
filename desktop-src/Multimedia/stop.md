---
title: 停止命令
description: Stop 命令會停止播放或錄製。 CD 音訊、數位影片、MIDI sequencer、videodisc、VCR 和波形音訊裝置都會辨識此命令。
ms.assetid: 82b2da63-f1ac-48f3-a206-6c5cfe00f5be
keywords:
- 停止命令 Windows 多媒體
topic_type:
- apiref
api_name:
- stop
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79d70aa150c01bd4c0ceab10332b4eca8b15d041
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384641"
---
# <a name="stop-command"></a><span data-ttu-id="3f2f2-105">停止命令</span><span class="sxs-lookup"><span data-stu-id="3f2f2-105">stop command</span></span>

<span data-ttu-id="3f2f2-106">Stop 命令會停止播放或錄製。</span><span class="sxs-lookup"><span data-stu-id="3f2f2-106">The stop command stops playback or recording.</span></span> <span data-ttu-id="3f2f2-107">CD 音訊、數位影片、MIDI sequencer、videodisc、VCR 和波形音訊裝置都會辨識此命令。</span><span class="sxs-lookup"><span data-stu-id="3f2f2-107">CD audio, digital-video, MIDI sequencer, videodisc, VCR, and waveform-audio devices recognize this command.</span></span>

<span data-ttu-id="3f2f2-108">若要傳送此命令，請使用 *lpszCommand* 參數設定來呼叫 [**mciSendString**](/previous-versions//dd757161(v=vs.85))函式，如下所示。</span><span class="sxs-lookup"><span data-stu-id="3f2f2-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("stop %s %s %s"), 
  lpszDeviceID, 
  lpszStopFlags, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="3f2f2-109">參數</span><span class="sxs-lookup"><span data-stu-id="3f2f2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f2f2-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="3f2f2-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="3f2f2-111">MCI 裝置的識別碼。</span><span class="sxs-lookup"><span data-stu-id="3f2f2-111">Identifier of an MCI device.</span></span> <span data-ttu-id="3f2f2-112">開啟裝置時，會指派此識別碼或別名。</span><span class="sxs-lookup"><span data-stu-id="3f2f2-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="3f2f2-113"><span id="lpszStopFlags"></span><span id="lpszstopflags"></span><span id="LPSZSTOPFLAGS"></span>*lpszStopFlags*</span><span class="sxs-lookup"><span data-stu-id="3f2f2-113"><span id="lpszStopFlags"></span><span id="lpszstopflags"></span><span id="LPSZSTOPFLAGS"></span>*lpszStopFlags*</span></span>
</dt> <dd>

<span data-ttu-id="3f2f2-114">針對數位視訊裝置，它可以是下列旗標。</span><span class="sxs-lookup"><span data-stu-id="3f2f2-114">For digital-video devices, it can be the following flag.</span></span>



| <span data-ttu-id="3f2f2-115">值</span><span class="sxs-lookup"><span data-stu-id="3f2f2-115">Value</span></span> | <span data-ttu-id="3f2f2-116">意義</span><span class="sxs-lookup"><span data-stu-id="3f2f2-116">Meaning</span></span>                                                                                                                                                                                      |
|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f2f2-117">hold</span><span class="sxs-lookup"><span data-stu-id="3f2f2-117">hold</span></span>  | <span data-ttu-id="3f2f2-118">防止在螢幕上重新繪製靜止影像所需的資源版本。</span><span class="sxs-lookup"><span data-stu-id="3f2f2-118">Prevents the release of resources required to redraw a still image on the screen.</span></span> <span data-ttu-id="3f2f2-119">例如，當移動視窗時，框架緩衝區仍可用於更新顯示。</span><span class="sxs-lookup"><span data-stu-id="3f2f2-119">The frame buffer remains available for use in updating the display when, for example, the window is moved.</span></span> |



 

</dd> <dt>

<span data-ttu-id="3f2f2-120"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="3f2f2-120"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="3f2f2-121">可以是「等候」、「通知」或兩者。</span><span class="sxs-lookup"><span data-stu-id="3f2f2-121">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="3f2f2-122">針對數位影片和 VCR 裝置，也可以指定「測試」。</span><span class="sxs-lookup"><span data-stu-id="3f2f2-122">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="3f2f2-123">如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。</span><span class="sxs-lookup"><span data-stu-id="3f2f2-123">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f2f2-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="3f2f2-124">Return Value</span></span>

<span data-ttu-id="3f2f2-125">如果成功則傳回零，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="3f2f2-125">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="3f2f2-126">備註</span><span class="sxs-lookup"><span data-stu-id="3f2f2-126">Remarks</span></span>

<span data-ttu-id="3f2f2-127">針對 CD 音訊裝置，stop 命令會停止播放，並將目前的曲目位置重設為零。</span><span class="sxs-lookup"><span data-stu-id="3f2f2-127">For CD audio devices, the stop command stops playback and resets the current track position to zero.</span></span>

## <a name="examples"></a><span data-ttu-id="3f2f2-128">範例</span><span class="sxs-lookup"><span data-stu-id="3f2f2-128">Examples</span></span>

<span data-ttu-id="3f2f2-129">下列命令會停止在 "mysound" 裝置上播放或錄製。</span><span class="sxs-lookup"><span data-stu-id="3f2f2-129">The following command stops playback or recording on the "mysound" device.</span></span>

``` syntax
stop mysound
```

## <a name="requirements"></a><span data-ttu-id="3f2f2-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="3f2f2-130">Requirements</span></span>



| <span data-ttu-id="3f2f2-131">需求</span><span class="sxs-lookup"><span data-stu-id="3f2f2-131">Requirement</span></span> | <span data-ttu-id="3f2f2-132">值</span><span class="sxs-lookup"><span data-stu-id="3f2f2-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="3f2f2-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3f2f2-133">Minimum supported client</span></span><br/> | <span data-ttu-id="3f2f2-134">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3f2f2-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="3f2f2-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3f2f2-135">Minimum supported server</span></span><br/> | <span data-ttu-id="3f2f2-136">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3f2f2-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="3f2f2-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3f2f2-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f2f2-138">Mci</span><span class="sxs-lookup"><span data-stu-id="3f2f2-138">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="3f2f2-139">MCI 命令字串</span><span class="sxs-lookup"><span data-stu-id="3f2f2-139">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 

