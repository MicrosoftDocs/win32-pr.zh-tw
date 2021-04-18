---
title: play 命令
description: Play 命令會開始播放裝置。 CD 音訊、數位影片、MIDI sequencer、videodisc、VCR 和波形音訊裝置都會辨識此命令。
ms.assetid: 3ee707d6-6af4-494d-a887-d91ea5666ac4
keywords:
- 播放命令 Windows 多媒體
topic_type:
- apiref
api_name:
- play
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbf262db152677ef5a2f29de9526152c1d48d4c9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965709"
---
# <a name="play-command"></a><span data-ttu-id="f561e-105">play 命令</span><span class="sxs-lookup"><span data-stu-id="f561e-105">play command</span></span>

<span data-ttu-id="f561e-106">Play 命令會開始播放裝置。</span><span class="sxs-lookup"><span data-stu-id="f561e-106">The play command starts playing a device.</span></span> <span data-ttu-id="f561e-107">CD 音訊、數位影片、MIDI sequencer、videodisc、VCR 和波形音訊裝置都會辨識此命令。</span><span class="sxs-lookup"><span data-stu-id="f561e-107">CD audio, digital-video, MIDI sequencer, videodisc, VCR, and waveform-audio devices recognize this command.</span></span>

<span data-ttu-id="f561e-108">若要傳送此命令，請使用 *lpszCommand* 參數設定來呼叫 [**mciSendString**](/previous-versions//dd757161(v=vs.85))函式，如下所示。</span><span class="sxs-lookup"><span data-stu-id="f561e-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("play %s %s %s"), 
  lpszDeviceID, 
  lpszPlayFlags, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="f561e-109">參數</span><span class="sxs-lookup"><span data-stu-id="f561e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f561e-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="f561e-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="f561e-111">MCI 裝置的識別碼。</span><span class="sxs-lookup"><span data-stu-id="f561e-111">Identifier of an MCI device.</span></span> <span data-ttu-id="f561e-112">開啟裝置時，會指派此識別碼或別名。</span><span class="sxs-lookup"><span data-stu-id="f561e-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="f561e-113"><span id="lpszPlayFlags"></span><span id="lpszplayflags"></span><span id="LPSZPLAYFLAGS"></span>*lpszPlayFlags*</span><span class="sxs-lookup"><span data-stu-id="f561e-113"><span id="lpszPlayFlags"></span><span id="lpszplayflags"></span><span id="LPSZPLAYFLAGS"></span>*lpszPlayFlags*</span></span>
</dt> <dd>

<span data-ttu-id="f561e-114">播放裝置的旗標。</span><span class="sxs-lookup"><span data-stu-id="f561e-114">Flag for playing a device.</span></span> <span data-ttu-id="f561e-115">下表列出可辨識 **播放** 命令的裝置類型，以及每種類型所使用的旗標。</span><span class="sxs-lookup"><span data-stu-id="f561e-115">The following table lists device types that recognize the **play** command and the flags used by each type.</span></span>



| <span data-ttu-id="f561e-116">值</span><span class="sxs-lookup"><span data-stu-id="f561e-116">Value</span></span>        | <span data-ttu-id="f561e-117">意義</span><span class="sxs-lookup"><span data-stu-id="f561e-117">Meaning</span></span>                          | <span data-ttu-id="f561e-118">意義</span><span class="sxs-lookup"><span data-stu-id="f561e-118">Meaning</span></span>                           |
|--------------|----------------------------------|-----------------------------------|
| <span data-ttu-id="f561e-119">cdaudio</span><span class="sxs-lookup"><span data-stu-id="f561e-119">cdaudio</span></span>      | <span data-ttu-id="f561e-120">從 *位置*</span><span class="sxs-lookup"><span data-stu-id="f561e-120">from *position*</span></span>                  | <span data-ttu-id="f561e-121">*定位*</span><span class="sxs-lookup"><span data-stu-id="f561e-121">to *position*</span></span>                     |
| <span data-ttu-id="f561e-122">digitalvideo</span><span class="sxs-lookup"><span data-stu-id="f561e-122">digitalvideo</span></span> | <span data-ttu-id="f561e-123">從 *位置* 全螢幕重複</span><span class="sxs-lookup"><span data-stu-id="f561e-123">from *position* fullscreen repeat</span></span> | <span data-ttu-id="f561e-124">反向至 *定位* 視窗</span><span class="sxs-lookup"><span data-stu-id="f561e-124">reverse to *position* window</span></span>       |
| <span data-ttu-id="f561e-125">排序器</span><span class="sxs-lookup"><span data-stu-id="f561e-125">sequencer</span></span>    | <span data-ttu-id="f561e-126">從 *位置*</span><span class="sxs-lookup"><span data-stu-id="f561e-126">from *position*</span></span>                  | <span data-ttu-id="f561e-127">*定位*</span><span class="sxs-lookup"><span data-stu-id="f561e-127">to *position*</span></span>                     |
| <span data-ttu-id="f561e-128">錄影機</span><span class="sxs-lookup"><span data-stu-id="f561e-128">vcr</span></span>          | <span data-ttu-id="f561e-129">從 *位置* 反向的 *時間*</span><span class="sxs-lookup"><span data-stu-id="f561e-129">at *time* from *position* reverse</span></span>  | <span data-ttu-id="f561e-130">掃描至 *位置*</span><span class="sxs-lookup"><span data-stu-id="f561e-130">scan to *position*</span></span>                |
| <span data-ttu-id="f561e-131">videodisc</span><span class="sxs-lookup"><span data-stu-id="f561e-131">videodisc</span></span>    | <span data-ttu-id="f561e-132">從 *位置* 反向掃描快速</span><span class="sxs-lookup"><span data-stu-id="f561e-132">fast from *position* reverse scan</span></span> | <span data-ttu-id="f561e-133">緩慢 *的速度\*\*整數*</span><span class="sxs-lookup"><span data-stu-id="f561e-133">slow speed *integer* to *position*</span></span> |
| <span data-ttu-id="f561e-134">waveaudio</span><span class="sxs-lookup"><span data-stu-id="f561e-134">waveaudio</span></span>    | <span data-ttu-id="f561e-135">從 *位置*</span><span class="sxs-lookup"><span data-stu-id="f561e-135">from *position*</span></span>                  | <span data-ttu-id="f561e-136">*定位*</span><span class="sxs-lookup"><span data-stu-id="f561e-136">to *position*</span></span>                     |



 

<span data-ttu-id="f561e-137">下表列出可在 **lpszPlayFlags** 參數中指定的旗標，以及它們的意義。</span><span class="sxs-lookup"><span data-stu-id="f561e-137">The following table lists the flags that can be specified in the **lpszPlayFlags** parameter and their meanings.</span></span>



| <span data-ttu-id="f561e-138">值</span><span class="sxs-lookup"><span data-stu-id="f561e-138">Value</span></span>           | <span data-ttu-id="f561e-139">意義</span><span class="sxs-lookup"><span data-stu-id="f561e-139">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f561e-140">*準時*</span><span class="sxs-lookup"><span data-stu-id="f561e-140">at *time*</span></span>       | <span data-ttu-id="f561e-141">指出裝置應該開始執行此命令的時間，如果裝置已 cued，則在 cued 命令開始時。</span><span class="sxs-lookup"><span data-stu-id="f561e-141">Indicates when the device should begin performing this command, or, if the device has been cued, when the cued command begins.</span></span> <span data-ttu-id="f561e-142">如需詳細資訊，請參閱 [提示](cue.md) 命令。</span><span class="sxs-lookup"><span data-stu-id="f561e-142">For more information, see the [cue](cue.md) command.</span></span>                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="f561e-143">快速</span><span class="sxs-lookup"><span data-stu-id="f561e-143">fast</span></span>            | <span data-ttu-id="f561e-144">指出裝置的播放速度比平常更快。</span><span class="sxs-lookup"><span data-stu-id="f561e-144">Indicates that the device should play faster than normal.</span></span> <span data-ttu-id="f561e-145">若要判斷 videodisc 播放程式的確切速度，請使用 [status](status.md) 命令的「速度」旗標。</span><span class="sxs-lookup"><span data-stu-id="f561e-145">To determine the exact speed on a videodisc player, use the "speed" flag of the [status](status.md) command.</span></span> <span data-ttu-id="f561e-146">若要更精確地指定速度，請使用此命令的「速度」旗標。</span><span class="sxs-lookup"><span data-stu-id="f561e-146">To specify the speed more precisely, use the "speed" flag of this command.</span></span>                                                                                                                                                                                                   |
| <span data-ttu-id="f561e-147">從 *位置*</span><span class="sxs-lookup"><span data-stu-id="f561e-147">from *position*</span></span> | <span data-ttu-id="f561e-148">指定播放的開始位置。</span><span class="sxs-lookup"><span data-stu-id="f561e-148">Specifies a starting position for the playback.</span></span> <span data-ttu-id="f561e-149">如果未指定 "from" 旗標，則會從目前的位置開始播放。</span><span class="sxs-lookup"><span data-stu-id="f561e-149">If the "from" flag is not specified, playback begins at the current position.</span></span> <span data-ttu-id="f561e-150">針對 **cdaudio** 裝置，如果 "from" 位置大於光碟的結束位置，或「從」位置大於「到」位置，則驅動程式會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="f561e-150">For **cdaudio** devices, if the "from" position is greater than the end position of the disc, or if the "from" position is greater than the "to" position, the driver returns an error.</span></span> <span data-ttu-id="f561e-151">針對 **videodisc** 裝置，預設位置會是 CAV 光碟的框架，而以小時、分鐘和秒為單位的 CLV 光碟。</span><span class="sxs-lookup"><span data-stu-id="f561e-151">For **videodisc** devices, the default positions are in frames for CAV discs and in hours, minutes, and seconds for CLV discs.</span></span> |
| <span data-ttu-id="f561e-152">全螢幕</span><span class="sxs-lookup"><span data-stu-id="f561e-152">fullscreen</span></span>      | <span data-ttu-id="f561e-153">指定應該使用全螢幕顯示。</span><span class="sxs-lookup"><span data-stu-id="f561e-153">Specifies that a full-screen display should be used.</span></span> <span data-ttu-id="f561e-154">只有在播放壓縮檔案時，才使用此旗標。</span><span class="sxs-lookup"><span data-stu-id="f561e-154">Use this flag only when playing compressed files.</span></span> <span data-ttu-id="f561e-155"> (未壓縮檔案將無法播放全螢幕。 ) </span><span class="sxs-lookup"><span data-stu-id="f561e-155">(Uncompressed files won't play full-screen.)</span></span>                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="f561e-156">重複</span><span class="sxs-lookup"><span data-stu-id="f561e-156">repeat</span></span>          | <span data-ttu-id="f561e-157">指定當到達內容的結尾時，播放應該重新開機。</span><span class="sxs-lookup"><span data-stu-id="f561e-157">Specifies that playback should restart when the end of the content is reached.</span></span>                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="f561e-158">reverse</span><span class="sxs-lookup"><span data-stu-id="f561e-158">reverse</span></span>         | <span data-ttu-id="f561e-159">指定播放方向反向。</span><span class="sxs-lookup"><span data-stu-id="f561e-159">Specifies that the play direction is backward.</span></span> <span data-ttu-id="f561e-160">您無法使用「反轉」旗標來指定結束位置。</span><span class="sxs-lookup"><span data-stu-id="f561e-160">You cannot specify an ending location with the "reverse" flag.</span></span> <span data-ttu-id="f561e-161">若為 videodiscs，"scan" 只適用于 CAV 格式。</span><span class="sxs-lookup"><span data-stu-id="f561e-161">For videodiscs, "scan" applies only to CAV format.</span></span>                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="f561e-162">掃描</span><span class="sxs-lookup"><span data-stu-id="f561e-162">scan</span></span>            | <span data-ttu-id="f561e-163">盡可能快速地播放，而不停用影片 (雖然音訊可能會停用) 。</span><span class="sxs-lookup"><span data-stu-id="f561e-163">Plays as fast as possible without disabling video (although audio might be disabled).</span></span> <span data-ttu-id="f561e-164">若為 videodiscs，"scan" 只適用于 CAV 格式。</span><span class="sxs-lookup"><span data-stu-id="f561e-164">For videodiscs, "scan" applies only to CAV format.</span></span>                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="f561e-165">slow</span><span class="sxs-lookup"><span data-stu-id="f561e-165">slow</span></span>            | <span data-ttu-id="f561e-166">的播放速度很慢。</span><span class="sxs-lookup"><span data-stu-id="f561e-166">Plays slowly.</span></span> <span data-ttu-id="f561e-167">若要判斷 videodisc 播放程式的確切速度，請使用 [status](status.md) 命令的「速度」旗標。</span><span class="sxs-lookup"><span data-stu-id="f561e-167">To determine the exact speed on a videodisc player, use the "speed" flag of the [status](status.md) command.</span></span> <span data-ttu-id="f561e-168">若要更精確地指定速度，請使用此命令的「速度」旗標。</span><span class="sxs-lookup"><span data-stu-id="f561e-168">To specify the speed more precisely, use the "speed" flag of this command.</span></span> <span data-ttu-id="f561e-169">針對 videodiscs，「慢」只適用于 CAV 格式。</span><span class="sxs-lookup"><span data-stu-id="f561e-169">For videodiscs, "slow" applies only to CAV format.</span></span>                                                                                                                                                                                            |
| <span data-ttu-id="f561e-170">速度 *整數*</span><span class="sxs-lookup"><span data-stu-id="f561e-170">speed *integer*</span></span> | <span data-ttu-id="f561e-171">以指定的速度（以每秒的畫面格）來播放 videodisc。</span><span class="sxs-lookup"><span data-stu-id="f561e-171">Plays a videodisc at the specified speed, in frames per second.</span></span> <span data-ttu-id="f561e-172">此旗標只適用于 CAV 光碟。</span><span class="sxs-lookup"><span data-stu-id="f561e-172">This flag applies only to CAV discs.</span></span>                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="f561e-173">*定位*</span><span class="sxs-lookup"><span data-stu-id="f561e-173">to *position*</span></span>   | <span data-ttu-id="f561e-174">指定播放的結束位置。</span><span class="sxs-lookup"><span data-stu-id="f561e-174">Specifies an ending position for the playback.</span></span> <span data-ttu-id="f561e-175">如果未指定 "to" 旗標，則會在內容結尾停止播放。</span><span class="sxs-lookup"><span data-stu-id="f561e-175">If the "to" flag is not specified, playback stops at the end of the content.</span></span> <span data-ttu-id="f561e-176">針對 **cdaudio** 裝置，如果「到」位置大於光碟的結束位置，驅動程式會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="f561e-176">For **cdaudio** devices, if the "to" position is greater than the end position of the disc, the driver returns an error.</span></span> <span data-ttu-id="f561e-177">針對 **videodisc** 裝置，預設位置會是 CAV 光碟的框架，而以小時、分鐘和秒為單位的 CLV 光碟。</span><span class="sxs-lookup"><span data-stu-id="f561e-177">For **videodisc** devices, the default positions are in frames for CAV discs and in hours, minutes, and seconds for CLV discs.</span></span>                                                                  |
| <span data-ttu-id="f561e-178">時間範圍</span><span class="sxs-lookup"><span data-stu-id="f561e-178">window</span></span>          | <span data-ttu-id="f561e-179">指定播放應使用與裝置實例相關聯的視窗。</span><span class="sxs-lookup"><span data-stu-id="f561e-179">Specifies that playing should use the window associated with the device instance.</span></span> <span data-ttu-id="f561e-180">這是預設值。</span><span class="sxs-lookup"><span data-stu-id="f561e-180">This is the default setting.</span></span>                                                                                                                                                                                                                                                                                                                                       |



 

</dd> <dt>

<span data-ttu-id="f561e-181"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="f561e-181"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="f561e-182">可以是「等候」、「通知」或兩者。</span><span class="sxs-lookup"><span data-stu-id="f561e-182">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="f561e-183">針對數位影片和 VCR 裝置，也可以指定「測試」。</span><span class="sxs-lookup"><span data-stu-id="f561e-183">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="f561e-184">如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。</span><span class="sxs-lookup"><span data-stu-id="f561e-184">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f561e-185">傳回值</span><span class="sxs-lookup"><span data-stu-id="f561e-185">Return Value</span></span>

<span data-ttu-id="f561e-186">如果成功則傳回零，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="f561e-186">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="f561e-187">備註</span><span class="sxs-lookup"><span data-stu-id="f561e-187">Remarks</span></span>

<span data-ttu-id="f561e-188">發出使用位置值的命令之前，您應該使用 [set](set.md) 命令來設定所需的時間格式。</span><span class="sxs-lookup"><span data-stu-id="f561e-188">Before issuing commands that use position values, you should set the desired time format by using the [set](set.md) command.</span></span> <span data-ttu-id="f561e-189">此命令會以設定的 "speed" 命令開始，以目前的速度開始播放。</span><span class="sxs-lookup"><span data-stu-id="f561e-189">This command begins playing at the current speed, as set with the set "speed" command.</span></span> <span data-ttu-id="f561e-190">如果指定「反轉」旗標，或將 "to" 旗標指定為小於 "from" 旗標的值，則方向會反轉。</span><span class="sxs-lookup"><span data-stu-id="f561e-190">The direction is reverse if the "reverse" flag is specified, or if the "to" flag is specified as a value less than the "from" flag.</span></span> <span data-ttu-id="f561e-191">如果未指定 "from" 旗標，則會從目前的位置開始播放。</span><span class="sxs-lookup"><span data-stu-id="f561e-191">If the "from" flag is not specified, playback begins at the current position.</span></span> <span data-ttu-id="f561e-192">「到」和「反轉」旗標不能一起使用。</span><span class="sxs-lookup"><span data-stu-id="f561e-192">The "to" and "reverse" flags cannot be used together.</span></span>

## <a name="examples"></a><span data-ttu-id="f561e-193">範例</span><span class="sxs-lookup"><span data-stu-id="f561e-193">Examples</span></span>

<span data-ttu-id="f561e-194">下列命令會從位置1000到位置2000播放 "mysound" 裝置，並在播放完成時傳送通知訊息。</span><span class="sxs-lookup"><span data-stu-id="f561e-194">The following command plays the "mysound" device from position 1000 through position 2000, sending a notification message when the playback completes.</span></span>

``` syntax
play mysound from 1000 to 2000 notify
```

## <a name="requirements"></a><span data-ttu-id="f561e-195">規格需求</span><span class="sxs-lookup"><span data-stu-id="f561e-195">Requirements</span></span>



| <span data-ttu-id="f561e-196">需求</span><span class="sxs-lookup"><span data-stu-id="f561e-196">Requirement</span></span> | <span data-ttu-id="f561e-197">值</span><span class="sxs-lookup"><span data-stu-id="f561e-197">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="f561e-198">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f561e-198">Minimum supported client</span></span><br/> | <span data-ttu-id="f561e-199">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f561e-199">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="f561e-200">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f561e-200">Minimum supported server</span></span><br/> | <span data-ttu-id="f561e-201">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f561e-201">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="f561e-202">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f561e-202">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f561e-203">Mci</span><span class="sxs-lookup"><span data-stu-id="f561e-203">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="f561e-204">MCI 命令字串</span><span class="sxs-lookup"><span data-stu-id="f561e-204">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="f561e-205">提示</span><span class="sxs-lookup"><span data-stu-id="f561e-205">cue</span></span>](cue.md)
</dt> <dt>

[<span data-ttu-id="f561e-206">set</span><span class="sxs-lookup"><span data-stu-id="f561e-206">set</span></span>](set.md)
</dt> </dl>

 

