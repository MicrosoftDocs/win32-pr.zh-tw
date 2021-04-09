---
title: pause 命令
description: Pause 命令會暫停播放或錄製。
ms.assetid: 8fa1a40d-fdb1-4c9f-a8db-9dd6a0d83b87
keywords:
- 暫停命令 Windows 多媒體
topic_type:
- apiref
api_name:
- pause
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25957defa4db514ce84f2e013dcc3751e21779b8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844395"
---
# <a name="pause-command"></a><span data-ttu-id="f543a-104">pause 命令</span><span class="sxs-lookup"><span data-stu-id="f543a-104">pause command</span></span>

<span data-ttu-id="f543a-105">Pause 命令會暫停播放或錄製。</span><span class="sxs-lookup"><span data-stu-id="f543a-105">The pause command pauses playing or recording.</span></span> <span data-ttu-id="f543a-106">大部分的驅動程式都會保留目前的位置，最後會在此位置繼續播放或錄製。</span><span class="sxs-lookup"><span data-stu-id="f543a-106">Most drivers retain the current position and eventually resume playback or recording at this position.</span></span> <span data-ttu-id="f543a-107">CD 音訊、數位影片、MIDI sequencer、VCR、videodisc 和波形-音訊裝置都會辨識此命令。</span><span class="sxs-lookup"><span data-stu-id="f543a-107">CD audio, digital-video, MIDI sequencer, VCR, videodisc, and waveform-audio devices recognize this command.</span></span>

<span data-ttu-id="f543a-108">若要傳送此命令，請使用 *lpszCommand* 參數設定來呼叫 [**mciSendString**](/previous-versions//dd757161(v=vs.85))函式，如下所示。</span><span class="sxs-lookup"><span data-stu-id="f543a-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("pause %s %s"), 
  lpszDeviceID, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="f543a-109">參數</span><span class="sxs-lookup"><span data-stu-id="f543a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f543a-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="f543a-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="f543a-111">MCI 裝置的識別碼。</span><span class="sxs-lookup"><span data-stu-id="f543a-111">Identifier of an MCI device.</span></span> <span data-ttu-id="f543a-112">開啟裝置時，會指派此識別碼或別名。</span><span class="sxs-lookup"><span data-stu-id="f543a-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="f543a-113"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="f543a-113"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="f543a-114">可以是「等候」、「通知」或兩者。</span><span class="sxs-lookup"><span data-stu-id="f543a-114">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="f543a-115">針對數位影片和 VCR 裝置，也可以指定「測試」。</span><span class="sxs-lookup"><span data-stu-id="f543a-115">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="f543a-116">如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。</span><span class="sxs-lookup"><span data-stu-id="f543a-116">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f543a-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="f543a-117">Return Value</span></span>

<span data-ttu-id="f543a-118">如果成功則傳回零，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="f543a-118">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="f543a-119">備註</span><span class="sxs-lookup"><span data-stu-id="f543a-119">Remarks</span></span>

<span data-ttu-id="f543a-120">使用 MCICDA、MCISEQ 和 MCIPIONR 驅動程式時，pause 命令的運作方式與 [stop](stop.md) 命令相同。</span><span class="sxs-lookup"><span data-stu-id="f543a-120">With the MCICDA, MCISEQ, and MCIPIONR drivers, the pause command works the same as the [stop](stop.md) command.</span></span>

## <a name="examples"></a><span data-ttu-id="f543a-121">範例</span><span class="sxs-lookup"><span data-stu-id="f543a-121">Examples</span></span>

<span data-ttu-id="f543a-122">下列命令會暫停 "mysound" 裝置。</span><span class="sxs-lookup"><span data-stu-id="f543a-122">The following command pauses the "mysound" device.</span></span>

``` syntax
pause mysound
```

## <a name="requirements"></a><span data-ttu-id="f543a-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="f543a-123">Requirements</span></span>



| <span data-ttu-id="f543a-124">需求</span><span class="sxs-lookup"><span data-stu-id="f543a-124">Requirement</span></span> | <span data-ttu-id="f543a-125">值</span><span class="sxs-lookup"><span data-stu-id="f543a-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="f543a-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f543a-126">Minimum supported client</span></span><br/> | <span data-ttu-id="f543a-127">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f543a-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="f543a-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f543a-128">Minimum supported server</span></span><br/> | <span data-ttu-id="f543a-129">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f543a-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="f543a-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f543a-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f543a-131">Mci</span><span class="sxs-lookup"><span data-stu-id="f543a-131">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="f543a-132">MCI 命令字串</span><span class="sxs-lookup"><span data-stu-id="f543a-132">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="f543a-133">停止</span><span class="sxs-lookup"><span data-stu-id="f543a-133">stop</span></span>](stop.md)
</dt> </dl>

 

