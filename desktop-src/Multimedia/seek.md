---
title: 搜尋命令
description: 搜尋命令會移至指定的位置，並停止。 CD 音訊、數位影片、MIDI sequencer、VCR、videodisc 和波形-音訊裝置都會辨識此命令。
ms.assetid: e9e8ca14-d181-4f29-b4d3-c7f5b0301164
keywords:
- 搜尋命令 Windows 多媒體
topic_type:
- apiref
api_name:
- seek
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d40f3467d328e161245e77217b4ce6edfa9665ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104383925"
---
# <a name="seek-command"></a><span data-ttu-id="4a372-105">搜尋命令</span><span class="sxs-lookup"><span data-stu-id="4a372-105">seek command</span></span>

<span data-ttu-id="4a372-106">搜尋命令會移至指定的位置，並停止。</span><span class="sxs-lookup"><span data-stu-id="4a372-106">The seek command moves to the specified position and stops.</span></span> <span data-ttu-id="4a372-107">CD 音訊、數位影片、MIDI sequencer、VCR、videodisc 和波形-音訊裝置都會辨識此命令。</span><span class="sxs-lookup"><span data-stu-id="4a372-107">CD audio, digital-video, MIDI sequencer, VCR, videodisc, and waveform-audio devices recognize this command.</span></span>

<span data-ttu-id="4a372-108">若要傳送此命令，請使用 *lpszCommand* 參數設定來呼叫 [**mciSendString**](/previous-versions//dd757161(v=vs.85))函式，如下所示。</span><span class="sxs-lookup"><span data-stu-id="4a372-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("seek %s %s %s"), 
  lpszDeviceID, 
  lpszSeekFlags, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="4a372-109">參數</span><span class="sxs-lookup"><span data-stu-id="4a372-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a372-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="4a372-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="4a372-111">MCI 裝置的識別碼。</span><span class="sxs-lookup"><span data-stu-id="4a372-111">Identifier of an MCI device.</span></span> <span data-ttu-id="4a372-112">開啟裝置時，會指派此識別碼或別名。</span><span class="sxs-lookup"><span data-stu-id="4a372-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="4a372-113"><span id="lpszSeekFlags"></span><span id="lpszseekflags"></span><span id="LPSZSEEKFLAGS"></span>*lpszSeekFlags*</span><span class="sxs-lookup"><span data-stu-id="4a372-113"><span id="lpszSeekFlags"></span><span id="lpszseekflags"></span><span id="LPSZSEEKFLAGS"></span>*lpszSeekFlags*</span></span>
</dt> <dd>

<span data-ttu-id="4a372-114">移至指定位置的旗標。</span><span class="sxs-lookup"><span data-stu-id="4a372-114">Flag for moving to a specified position.</span></span> <span data-ttu-id="4a372-115">下表列出可辨識 **搜尋** 命令的裝置類型，以及每種類型所使用的旗標。</span><span class="sxs-lookup"><span data-stu-id="4a372-115">The following table lists device types that recognize the **seek** command and the flags used by each type.</span></span>



| <span data-ttu-id="4a372-116">值</span><span class="sxs-lookup"><span data-stu-id="4a372-116">Value</span></span>        | <span data-ttu-id="4a372-117">意義</span><span class="sxs-lookup"><span data-stu-id="4a372-117">Meaning</span></span>                          | <span data-ttu-id="4a372-118">意義</span><span class="sxs-lookup"><span data-stu-id="4a372-118">Meaning</span></span>                      |
|--------------|----------------------------------|------------------------------|
| <span data-ttu-id="4a372-119">cdaudio</span><span class="sxs-lookup"><span data-stu-id="4a372-119">cdaudio</span></span>      | <span data-ttu-id="4a372-120">結束至 *位置*</span><span class="sxs-lookup"><span data-stu-id="4a372-120">to end to *position*</span></span>             | <span data-ttu-id="4a372-121">開始</span><span class="sxs-lookup"><span data-stu-id="4a372-121">to start</span></span>                     |
| <span data-ttu-id="4a372-122">digitalvideo</span><span class="sxs-lookup"><span data-stu-id="4a372-122">digitalvideo</span></span> | <span data-ttu-id="4a372-123">結束至 *位置*</span><span class="sxs-lookup"><span data-stu-id="4a372-123">to end to *position*</span></span>             | <span data-ttu-id="4a372-124">開始</span><span class="sxs-lookup"><span data-stu-id="4a372-124">to start</span></span>                     |
| <span data-ttu-id="4a372-125">排序器</span><span class="sxs-lookup"><span data-stu-id="4a372-125">sequencer</span></span>    | <span data-ttu-id="4a372-126">結束至 *位置*</span><span class="sxs-lookup"><span data-stu-id="4a372-126">to end to *position*</span></span>             | <span data-ttu-id="4a372-127">開始</span><span class="sxs-lookup"><span data-stu-id="4a372-127">to start</span></span>                     |
| <span data-ttu-id="4a372-128">錄影機</span><span class="sxs-lookup"><span data-stu-id="4a372-128">vcr</span></span>          | <span data-ttu-id="4a372-129">以 *時間* 標記 *的 \_ 順序反轉*</span><span class="sxs-lookup"><span data-stu-id="4a372-129">at *time* mark *mark\_num* reverse</span></span> | <span data-ttu-id="4a372-130">結束 *位置* 以開始</span><span class="sxs-lookup"><span data-stu-id="4a372-130">to end to *position* to start</span></span> |
| <span data-ttu-id="4a372-131">videodisc</span><span class="sxs-lookup"><span data-stu-id="4a372-131">videodisc</span></span>    | <span data-ttu-id="4a372-132">反向至結尾</span><span class="sxs-lookup"><span data-stu-id="4a372-132">reverse to end</span></span>                   | <span data-ttu-id="4a372-133">開始 *位置*</span><span class="sxs-lookup"><span data-stu-id="4a372-133">to *position* to start</span></span>        |
| <span data-ttu-id="4a372-134">waveaudio</span><span class="sxs-lookup"><span data-stu-id="4a372-134">waveaudio</span></span>    | <span data-ttu-id="4a372-135">結束至 *位置*</span><span class="sxs-lookup"><span data-stu-id="4a372-135">to end to *position*</span></span>             | <span data-ttu-id="4a372-136">開始</span><span class="sxs-lookup"><span data-stu-id="4a372-136">to start</span></span>                     |



 

<span data-ttu-id="4a372-137">下表列出可在 **lpszSeekFlags** 參數中指定的旗標，以及它們的意義。</span><span class="sxs-lookup"><span data-stu-id="4a372-137">The following table lists the flags that can be specified in the **lpszSeekFlags** parameter and their meanings.</span></span>



| <span data-ttu-id="4a372-138">值</span><span class="sxs-lookup"><span data-stu-id="4a372-138">Value</span></span>            | <span data-ttu-id="4a372-139">意義</span><span class="sxs-lookup"><span data-stu-id="4a372-139">Meaning</span></span>                                                                                                                                                                                                          |
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a372-140">*準時*</span><span class="sxs-lookup"><span data-stu-id="4a372-140">at *time*</span></span>        | <span data-ttu-id="4a372-141">指出裝置應該開始執行此命令的時間，如果裝置已 cued，則在 cued 命令開始時。</span><span class="sxs-lookup"><span data-stu-id="4a372-141">Indicates when the device should begin performing this command, or, if the device has been cued, when the cued command begins.</span></span> <span data-ttu-id="4a372-142">如需詳細資訊，請參閱 [提示](cue.md) 命令。</span><span class="sxs-lookup"><span data-stu-id="4a372-142">For more information, see the [cue](cue.md) command.</span></span>                             |
| <span data-ttu-id="4a372-143">標記 *\_ 編號*</span><span class="sxs-lookup"><span data-stu-id="4a372-143">mark *mark\_num*</span></span> | <span data-ttu-id="4a372-144">搜尋 *標記 \_ num* 所指出的相對標記，這必須是正整數值。</span><span class="sxs-lookup"><span data-stu-id="4a372-144">Seeks to the relative mark indicated by *mark\_num*, which must be a positive integer value.</span></span> <span data-ttu-id="4a372-145">標記是使用 [mark](mark.md) 命令寫入至 VCR 磁帶的信號，用於高速搜尋。</span><span class="sxs-lookup"><span data-stu-id="4a372-145">Marks are signals written to the VCR tape using the [mark](mark.md) command and are used for high-speed searching.</span></span> |
| <span data-ttu-id="4a372-146">reverse</span><span class="sxs-lookup"><span data-stu-id="4a372-146">reverse</span></span>          | <span data-ttu-id="4a372-147">指出 Vcr 和 CAV videodiscs 上的搜尋方向是向後。</span><span class="sxs-lookup"><span data-stu-id="4a372-147">Indicates that the seek direction on VCRs and CAV videodiscs is backward.</span></span> <span data-ttu-id="4a372-148">如果指定了 "to" 旗標，則此旗標無效。</span><span class="sxs-lookup"><span data-stu-id="4a372-148">This flag is invalid if the "to" flag is specified.</span></span> <span data-ttu-id="4a372-149">若為 Vcr，此旗標必須與「標記」旗標搭配使用。</span><span class="sxs-lookup"><span data-stu-id="4a372-149">For VCRs, this flag must be used with the "mark" flag.</span></span>                             |
| <span data-ttu-id="4a372-150">結束</span><span class="sxs-lookup"><span data-stu-id="4a372-150">to end</span></span>           | <span data-ttu-id="4a372-151">搜尋內容的結尾。</span><span class="sxs-lookup"><span data-stu-id="4a372-151">Seeks to the end of the content.</span></span>                                                                                                                                                                                 |
| <span data-ttu-id="4a372-152">*定位*</span><span class="sxs-lookup"><span data-stu-id="4a372-152">to *position*</span></span>    | <span data-ttu-id="4a372-153">指定要停止搜尋的位置。</span><span class="sxs-lookup"><span data-stu-id="4a372-153">Specifies the position to stop the seek.</span></span> <span data-ttu-id="4a372-154">針對 **cdaudio** 裝置，如果指定的位置大於光碟的長度，則 MCI 會傳回超出範圍的錯誤。</span><span class="sxs-lookup"><span data-stu-id="4a372-154">For **cdaudio** devices, MCI returns an out-of-range error if the specified position is greater than the length of the disc.</span></span>                                            |
| <span data-ttu-id="4a372-155">開始</span><span class="sxs-lookup"><span data-stu-id="4a372-155">to start</span></span>         | <span data-ttu-id="4a372-156">搜尋內容的開頭。</span><span class="sxs-lookup"><span data-stu-id="4a372-156">Seeks to the start of the content.</span></span>                                                                                                                                                                               |



 

</dd> <dt>

<span data-ttu-id="4a372-157"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="4a372-157"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="4a372-158">可以是「等候」、「通知」或兩者。</span><span class="sxs-lookup"><span data-stu-id="4a372-158">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="4a372-159">針對數位影片和 VCR 裝置，也可以指定「測試」。</span><span class="sxs-lookup"><span data-stu-id="4a372-159">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="4a372-160">如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。</span><span class="sxs-lookup"><span data-stu-id="4a372-160">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a372-161">傳回值</span><span class="sxs-lookup"><span data-stu-id="4a372-161">Return Value</span></span>

<span data-ttu-id="4a372-162">如果成功則傳回零，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="4a372-162">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="4a372-163">備註</span><span class="sxs-lookup"><span data-stu-id="4a372-163">Remarks</span></span>

<span data-ttu-id="4a372-164">發出使用位置值的任何命令之前，您應該使用 [set](set.md) 命令來設定所需的時間格式。</span><span class="sxs-lookup"><span data-stu-id="4a372-164">Before issuing any commands that use position values, you should set the desired time format by using the [set](set.md) command.</span></span>

<span data-ttu-id="4a372-165">數位影片裝置支援兩種搜尋模式，您可以使用 [set](set.md) 命令加以變更。</span><span class="sxs-lookup"><span data-stu-id="4a372-165">Digital-video devices support two seek modes, which you can change by using the [set](set.md) command.</span></span> <span data-ttu-id="4a372-166">「完全搜尋」模式會使 seek 命令移至指定的框架。</span><span class="sxs-lookup"><span data-stu-id="4a372-166">The "seek exactly on" mode causes the seek command to move to the specified frame.</span></span> <span data-ttu-id="4a372-167">「完全搜尋」模式會導致搜尋命令在指定的框架之前移至最接近的主要畫面格。</span><span class="sxs-lookup"><span data-stu-id="4a372-167">The "seek exactly off" mode causes the seek command to move to the closest key frame prior to the specified frame.</span></span>

<span data-ttu-id="4a372-168">如果在發出搜尋命令時播放 CD 音訊裝置，則會停止播放。</span><span class="sxs-lookup"><span data-stu-id="4a372-168">If a CD audio device is playing when the seek command is issued, playback is stopped.</span></span> <span data-ttu-id="4a372-169">當搜尋命令以 videodisc 裝置發出時，裝置會使用向前快轉或快速反轉來搜尋影片和音訊。</span><span class="sxs-lookup"><span data-stu-id="4a372-169">When the seek command is issued with a videodisc device, the device searches using fast forward or fast reverse with video and audio off.</span></span>

<span data-ttu-id="4a372-170">使用波形音訊裝置發出搜尋命令時，行為取決於樣本大小。</span><span class="sxs-lookup"><span data-stu-id="4a372-170">When the seek command is issued with a waveform-audio device, the behavior depends on the sample size.</span></span> <span data-ttu-id="4a372-171">如果樣本大小為16位或更大，則當指定的位置與範例開始不一致時，搜尋會移至最接近的樣本的開頭。</span><span class="sxs-lookup"><span data-stu-id="4a372-171">If the sample size is 16 bits or greater, seek moves to the beginning of the nearest sample when a specified position does not coincide with the start of a sample.</span></span>

## <a name="examples"></a><span data-ttu-id="4a372-172">範例</span><span class="sxs-lookup"><span data-stu-id="4a372-172">Examples</span></span>

<span data-ttu-id="4a372-173">下列命令會搜尋與 "mysound" 裝置相關聯之媒體檔案的開頭。</span><span class="sxs-lookup"><span data-stu-id="4a372-173">The following command seeks to the start of the media file associated with the "mysound" device.</span></span>

``` syntax
seek mysound to start
```

## <a name="requirements"></a><span data-ttu-id="4a372-174">規格需求</span><span class="sxs-lookup"><span data-stu-id="4a372-174">Requirements</span></span>



| <span data-ttu-id="4a372-175">需求</span><span class="sxs-lookup"><span data-stu-id="4a372-175">Requirement</span></span> | <span data-ttu-id="4a372-176">值</span><span class="sxs-lookup"><span data-stu-id="4a372-176">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="4a372-177">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4a372-177">Minimum supported client</span></span><br/> | <span data-ttu-id="4a372-178">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4a372-178">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="4a372-179">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4a372-179">Minimum supported server</span></span><br/> | <span data-ttu-id="4a372-180">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4a372-180">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="4a372-181">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4a372-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a372-182">Mci</span><span class="sxs-lookup"><span data-stu-id="4a372-182">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="4a372-183">MCI 命令字串</span><span class="sxs-lookup"><span data-stu-id="4a372-183">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="4a372-184">提示</span><span class="sxs-lookup"><span data-stu-id="4a372-184">cue</span></span>](cue.md)
</dt> <dt>

[<span data-ttu-id="4a372-185">標記</span><span class="sxs-lookup"><span data-stu-id="4a372-185">mark</span></span>](mark.md)
</dt> <dt>

[<span data-ttu-id="4a372-186">set</span><span class="sxs-lookup"><span data-stu-id="4a372-186">set</span></span>](set.md)
</dt> </dl>

 

