---
title: 監視命令
description: Monitor 命令會指定展示來源。  (預設的展示來源為工作區。 ) 切換展示來源會切換來源中的所有音訊和影片串流。 數位影片裝置辨識此命令。
ms.assetid: 5cacbe88-b94e-4101-badf-2bb4796b19cf
keywords:
- 監視命令 Windows 多媒體
topic_type:
- apiref
api_name:
- monitor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ccbe1d8919c232ab88d04081dad242944868893
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685889"
---
# <a name="monitor-command"></a><span data-ttu-id="1ec4a-106">監視命令</span><span class="sxs-lookup"><span data-stu-id="1ec4a-106">monitor command</span></span>

<span data-ttu-id="1ec4a-107">Monitor 命令會指定展示來源。</span><span class="sxs-lookup"><span data-stu-id="1ec4a-107">The monitor command specifies the presentation source.</span></span> <span data-ttu-id="1ec4a-108"> (預設的展示來源為工作區。 ) 切換展示來源會切換來源中的所有音訊和影片串流。</span><span class="sxs-lookup"><span data-stu-id="1ec4a-108">(The default presentation source is the workspace.) Switching the presentation source switches all audio and video streams in the source.</span></span> <span data-ttu-id="1ec4a-109">數位影片裝置辨識此命令。</span><span class="sxs-lookup"><span data-stu-id="1ec4a-109">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="1ec4a-110">若要傳送此命令，請使用 *lpszCommand* 參數設定來呼叫 [**mciSendString**](/previous-versions//dd757161(v=vs.85))函式，如下所示。</span><span class="sxs-lookup"><span data-stu-id="1ec4a-110">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("monitor %s %s %s"), 
  lpszDeviceID, 
  lpszMonitor, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="1ec4a-111">參數</span><span class="sxs-lookup"><span data-stu-id="1ec4a-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ec4a-112"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="1ec4a-112"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="1ec4a-113">MCI 裝置的識別碼。</span><span class="sxs-lookup"><span data-stu-id="1ec4a-113">Identifier of an MCI device.</span></span> <span data-ttu-id="1ec4a-114">開啟裝置時，會指派此識別碼或別名。</span><span class="sxs-lookup"><span data-stu-id="1ec4a-114">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="1ec4a-115"><span id="lpszMonitor"></span><span id="lpszmonitor"></span><span id="LPSZMONITOR"></span>*lpszMonitor*</span><span class="sxs-lookup"><span data-stu-id="1ec4a-115"><span id="lpszMonitor"></span><span id="lpszmonitor"></span><span id="LPSZMONITOR"></span>*lpszMonitor*</span></span>
</dt> <dd>

<span data-ttu-id="1ec4a-116">下列一或多個旗標。</span><span class="sxs-lookup"><span data-stu-id="1ec4a-116">One or more of the following flags.</span></span>



| <span data-ttu-id="1ec4a-117">值</span><span class="sxs-lookup"><span data-stu-id="1ec4a-117">Value</span></span>           | <span data-ttu-id="1ec4a-118">意義</span><span class="sxs-lookup"><span data-stu-id="1ec4a-118">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ec4a-119">file</span><span class="sxs-lookup"><span data-stu-id="1ec4a-119">file</span></span>            | <span data-ttu-id="1ec4a-120">指定工作區是展示來源。</span><span class="sxs-lookup"><span data-stu-id="1ec4a-120">Specifies that the workspace is the presentation source.</span></span> <span data-ttu-id="1ec4a-121">這是預設來源。</span><span class="sxs-lookup"><span data-stu-id="1ec4a-121">This is the default source.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="1ec4a-122">input</span><span class="sxs-lookup"><span data-stu-id="1ec4a-122">input</span></span>           | <span data-ttu-id="1ec4a-123">指定外部輸入是展示來源。</span><span class="sxs-lookup"><span data-stu-id="1ec4a-123">Specifies that the external input is the presentation source.</span></span> <span data-ttu-id="1ec4a-124">如果 [播放](play.md) 命令正在進行，它會先暫停。</span><span class="sxs-lookup"><span data-stu-id="1ec4a-124">If a [play](play.md) command is in progress, it is first paused.</span></span> <span data-ttu-id="1ec4a-125">如果 [setvideo](setvideo.md) 是 "on"，此旗標會顯示預設的隱藏視窗。</span><span class="sxs-lookup"><span data-stu-id="1ec4a-125">If [setvideo](setvideo.md) is "on", this flag displays a default hidden window.</span></span> <span data-ttu-id="1ec4a-126">裝置可能會限制其他裝置實例可在監視輸入時進行的動作。</span><span class="sxs-lookup"><span data-stu-id="1ec4a-126">Devices might limit what other device instances can do while monitoring input.</span></span>                                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="1ec4a-127">方法 *方法*</span><span class="sxs-lookup"><span data-stu-id="1ec4a-127">method *method*</span></span> | <span data-ttu-id="1ec4a-128">與 **監視** 「輸入」搭配使用時，此旗標會選取監視的方法。</span><span class="sxs-lookup"><span data-stu-id="1ec4a-128">When used with **monitor** "input", this flag selects the method of monitoring.</span></span> <span data-ttu-id="1ec4a-129">*方法* 可以是 "pre"、"post" 或 "direct"。</span><span class="sxs-lookup"><span data-stu-id="1ec4a-129">The *method* is either "pre", "post", or "direct".</span></span> <span data-ttu-id="1ec4a-130">直接監視要求裝置在監視期間設定為最佳顯示品質。</span><span class="sxs-lookup"><span data-stu-id="1ec4a-130">Direct monitoring requests that the device be configured for optimum display quality during monitoring.</span></span> <span data-ttu-id="1ec4a-131">直接監視方法可能與運動影片錄製不相容。前置和後置監視允許播放影片錄影。</span><span class="sxs-lookup"><span data-stu-id="1ec4a-131">The direct monitoring method might be incompatible with motion video recording.Pre- and post-monitoring allow motion video recording.</span></span> <span data-ttu-id="1ec4a-132">預先監視會顯示壓縮前的外部輸入，而後續監視會在壓縮之後顯示外部輸入。</span><span class="sxs-lookup"><span data-stu-id="1ec4a-132">Pre-monitoring shows the external input prior to compression, while post-monitoring shows the external input after compression.</span></span> <span data-ttu-id="1ec4a-133">一般而言，不同的監視方法會有不同的硬體含意。</span><span class="sxs-lookup"><span data-stu-id="1ec4a-133">Typically, different monitoring methods have different hardware implications.</span></span> <span data-ttu-id="1ec4a-134">裝置會選取預設的監視方法。</span><span class="sxs-lookup"><span data-stu-id="1ec4a-134">The default monitoring method is selected by the device.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="1ec4a-135"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="1ec4a-135"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="1ec4a-136">可以是「等候」、「通知」、「測試」或它們的組合。</span><span class="sxs-lookup"><span data-stu-id="1ec4a-136">Can be "wait", "notify", "test", or a combination of these.</span></span> <span data-ttu-id="1ec4a-137">如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。</span><span class="sxs-lookup"><span data-stu-id="1ec4a-137">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ec4a-138">傳回值</span><span class="sxs-lookup"><span data-stu-id="1ec4a-138">Return Value</span></span>

<span data-ttu-id="1ec4a-139">如果成功則傳回零，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="1ec4a-139">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="1ec4a-140">備註</span><span class="sxs-lookup"><span data-stu-id="1ec4a-140">Remarks</span></span>

<span data-ttu-id="1ec4a-141">展示來源會在 [play](play.md)、 [step](step.md)、 [pause](pause.md)、 [提示](cue.md) "output" 或 [seek](seek.md) 命令之後，自動切換至工作區。</span><span class="sxs-lookup"><span data-stu-id="1ec4a-141">The presentation source automatically switches to the workspace after a [play](play.md), [step](step.md), [pause](pause.md), [cue](cue.md) "output", or [seek](seek.md) command.</span></span> <span data-ttu-id="1ec4a-142">[ [記錄](record.md) ] 命令不會自動切換展示來源，可讓您的應用程式在錄製時不會顯示影片的選項。</span><span class="sxs-lookup"><span data-stu-id="1ec4a-142">The [record](record.md) command does not automatically switch presentation sources, which gives your application the option of not showing video while it is being recorded.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ec4a-143">規格需求</span><span class="sxs-lookup"><span data-stu-id="1ec4a-143">Requirements</span></span>



| <span data-ttu-id="1ec4a-144">需求</span><span class="sxs-lookup"><span data-stu-id="1ec4a-144">Requirement</span></span> | <span data-ttu-id="1ec4a-145">值</span><span class="sxs-lookup"><span data-stu-id="1ec4a-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="1ec4a-146">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1ec4a-146">Minimum supported client</span></span><br/> | <span data-ttu-id="1ec4a-147">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1ec4a-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="1ec4a-148">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1ec4a-148">Minimum supported server</span></span><br/> | <span data-ttu-id="1ec4a-149">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1ec4a-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="1ec4a-150">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1ec4a-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ec4a-151">Mci</span><span class="sxs-lookup"><span data-stu-id="1ec4a-151">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="1ec4a-152">MCI 命令字串</span><span class="sxs-lookup"><span data-stu-id="1ec4a-152">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="1ec4a-153">提示</span><span class="sxs-lookup"><span data-stu-id="1ec4a-153">cue</span></span>](cue.md)
</dt> <dt>

[<span data-ttu-id="1ec4a-154">pause</span><span class="sxs-lookup"><span data-stu-id="1ec4a-154">pause</span></span>](pause.md)
</dt> <dt>

[<span data-ttu-id="1ec4a-155">玩</span><span class="sxs-lookup"><span data-stu-id="1ec4a-155">play</span></span>](play.md)
</dt> <dt>

[<span data-ttu-id="1ec4a-156">記錄</span><span class="sxs-lookup"><span data-stu-id="1ec4a-156">record</span></span>](record.md)
</dt> <dt>

[<span data-ttu-id="1ec4a-157">尋求</span><span class="sxs-lookup"><span data-stu-id="1ec4a-157">seek</span></span>](seek.md)
</dt> <dt>

[<span data-ttu-id="1ec4a-158">步</span><span class="sxs-lookup"><span data-stu-id="1ec4a-158">step</span></span>](step.md)
</dt> </dl>

 

