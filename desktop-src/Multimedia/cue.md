---
title: 提示命令
description: 提示命令可準備播放或錄製。 數位-影片、VCR 和波形-音訊裝置會辨識此命令。
ms.assetid: 94fa0d0c-d5c9-4ef1-bb7d-22dfb09a7689
keywords:
- 提示命令 Windows 多媒體
topic_type:
- apiref
api_name:
- cue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1dd71f06a71c8aff4752fc31d750a3612564eb8a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844411"
---
# <a name="cue-command"></a><span data-ttu-id="9dd33-105">提示命令</span><span class="sxs-lookup"><span data-stu-id="9dd33-105">cue command</span></span>

<span data-ttu-id="9dd33-106">提示命令可準備播放或錄製。</span><span class="sxs-lookup"><span data-stu-id="9dd33-106">The cue command prepares for playing or recording.</span></span> <span data-ttu-id="9dd33-107">數位-影片、VCR 和波形-音訊裝置會辨識此命令。</span><span class="sxs-lookup"><span data-stu-id="9dd33-107">Digital-video, VCR, and waveform-audio devices recognize this command.</span></span>

<span data-ttu-id="9dd33-108">若要傳送此命令，請使用 *lpszCommand* 參數設定來呼叫 [**mciSendString**](/previous-versions//dd757161(v=vs.85))函式，如下所示。</span><span class="sxs-lookup"><span data-stu-id="9dd33-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("cue %s %s %s"), 
  lpszDeviceID, 
  lpszInOutTo, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="9dd33-109">參數</span><span class="sxs-lookup"><span data-stu-id="9dd33-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9dd33-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="9dd33-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="9dd33-111">MCI 裝置的識別碼。</span><span class="sxs-lookup"><span data-stu-id="9dd33-111">Identifier of an MCI device.</span></span> <span data-ttu-id="9dd33-112">開啟裝置時，會指派此識別碼或別名。</span><span class="sxs-lookup"><span data-stu-id="9dd33-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="9dd33-113"><span id="lpszInOutTo"></span><span id="lpszinoutto"></span><span id="LPSZINOUTTO"></span>*lpszInOutTo*</span><span class="sxs-lookup"><span data-stu-id="9dd33-113"><span id="lpszInOutTo"></span><span id="lpszinoutto"></span><span id="LPSZINOUTTO"></span>*lpszInOutTo*</span></span>
</dt> <dd>

<span data-ttu-id="9dd33-114">準備裝置以進行播放或錄製的旗標。</span><span class="sxs-lookup"><span data-stu-id="9dd33-114">Flag that prepares a device for playing or recording.</span></span> <span data-ttu-id="9dd33-115">下表列出可辨識 **提示** 命令的裝置類型，以及每種類型所使用的旗標。</span><span class="sxs-lookup"><span data-stu-id="9dd33-115">The following table lists device types that recognize the **cue** command and the flags used by each type.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9dd33-116">值</span><span class="sxs-lookup"><span data-stu-id="9dd33-116">Value</span></span></th>
<th><span data-ttu-id="9dd33-117">提示</span><span class="sxs-lookup"><span data-stu-id="9dd33-117">Cue</span></span></th>
<th><span data-ttu-id="9dd33-118">提示</span><span class="sxs-lookup"><span data-stu-id="9dd33-118">Cue</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9dd33-119">digitalvideo</span><span class="sxs-lookup"><span data-stu-id="9dd33-119">digitalvideo</span></span></td>
<td><ul>
<li><span data-ttu-id="9dd33-120">input</span><span class="sxs-lookup"><span data-stu-id="9dd33-120">input</span></span></li>
<li><span data-ttu-id="9dd33-121">noshow</span><span class="sxs-lookup"><span data-stu-id="9dd33-121">noshow</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="9dd33-122">output</span><span class="sxs-lookup"><span data-stu-id="9dd33-122">output</span></span></li>
<li><span data-ttu-id="9dd33-123"><em>定位</em></span><span class="sxs-lookup"><span data-stu-id="9dd33-123">to <em>position</em></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9dd33-124">錄影機</span><span class="sxs-lookup"><span data-stu-id="9dd33-124">vcr</span></span></td>
<td><ul>
<li><span data-ttu-id="9dd33-125">從 <em>位置</em></span><span class="sxs-lookup"><span data-stu-id="9dd33-125">from <em>position</em></span></span></li>
<li><span data-ttu-id="9dd33-126">input</span><span class="sxs-lookup"><span data-stu-id="9dd33-126">input</span></span></li>
<li><span data-ttu-id="9dd33-127">output</span><span class="sxs-lookup"><span data-stu-id="9dd33-127">output</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="9dd33-128">預</span><span class="sxs-lookup"><span data-stu-id="9dd33-128">preroll</span></span></li>
<li><span data-ttu-id="9dd33-129">reverse</span><span class="sxs-lookup"><span data-stu-id="9dd33-129">reverse</span></span></li>
<li><span data-ttu-id="9dd33-130"><em>定位</em></span><span class="sxs-lookup"><span data-stu-id="9dd33-130">to <em>position</em></span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9dd33-131">waveaudio</span><span class="sxs-lookup"><span data-stu-id="9dd33-131">waveaudio</span></span></td>
<td><span data-ttu-id="9dd33-132">input</span><span class="sxs-lookup"><span data-stu-id="9dd33-132">input</span></span></td>
<td><span data-ttu-id="9dd33-133">output</span><span class="sxs-lookup"><span data-stu-id="9dd33-133">output</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="9dd33-134">下表列出可在 *lpszInOutTo* 參數中指定的旗標，以及它們的意義。</span><span class="sxs-lookup"><span data-stu-id="9dd33-134">The following table lists the flags that can be specified in the *lpszInOutTo* parameter and their meanings.</span></span>



| <span data-ttu-id="9dd33-135">值</span><span class="sxs-lookup"><span data-stu-id="9dd33-135">Value</span></span>           | <span data-ttu-id="9dd33-136">意義</span><span class="sxs-lookup"><span data-stu-id="9dd33-136">Meaning</span></span>                                                                                                                                                                                                                                                                                                        |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9dd33-137">從 *位置*</span><span class="sxs-lookup"><span data-stu-id="9dd33-137">from *position*</span></span> | <span data-ttu-id="9dd33-138">表示要從何處開始。</span><span class="sxs-lookup"><span data-stu-id="9dd33-138">Indicates where to start.</span></span>                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="9dd33-139">input</span><span class="sxs-lookup"><span data-stu-id="9dd33-139">input</span></span>           | <span data-ttu-id="9dd33-140">準備錄製。</span><span class="sxs-lookup"><span data-stu-id="9dd33-140">Prepares for recording.</span></span> <span data-ttu-id="9dd33-141">若為數位視訊裝置，如果目前的簡報來源已經是外部輸入，就可以省略此旗標。</span><span class="sxs-lookup"><span data-stu-id="9dd33-141">For digital-video devices, this flag can be omitted if the current presentation source is already the external input.</span></span>                                                                                                                                                                  |
| <span data-ttu-id="9dd33-142">noshow</span><span class="sxs-lookup"><span data-stu-id="9dd33-142">noshow</span></span>          | <span data-ttu-id="9dd33-143">準備播放框架而不顯示。</span><span class="sxs-lookup"><span data-stu-id="9dd33-143">Prepares for playing a frame without displaying it.</span></span> <span data-ttu-id="9dd33-144">當指定這個旗標時，即使對應的框架不是目前的位置，顯示器仍會繼續在框架緩衝區中顯示影像。</span><span class="sxs-lookup"><span data-stu-id="9dd33-144">When this flag is specified, the display continues to show the image in the frame buffer even though its corresponding frame is not the current position.</span></span> <span data-ttu-id="9dd33-145">沒有此旗標且沒有 "to" 旗標的後續提示命令會顯示目前的畫面格。</span><span class="sxs-lookup"><span data-stu-id="9dd33-145">A subsequent cue command without this flag and without the "to" flag displays the current frame.</span></span> |
| <span data-ttu-id="9dd33-146">output</span><span class="sxs-lookup"><span data-stu-id="9dd33-146">output</span></span>          | <span data-ttu-id="9dd33-147">準備進行播放。</span><span class="sxs-lookup"><span data-stu-id="9dd33-147">Prepares for playing.</span></span> <span data-ttu-id="9dd33-148">如果未指定「輸入」和「輸出」，則預設設定為「輸出」。</span><span class="sxs-lookup"><span data-stu-id="9dd33-148">If neither "input" nor "output" is specified, the default setting is "output".</span></span>                                                                                                                                                                                                           |
| <span data-ttu-id="9dd33-149">預</span><span class="sxs-lookup"><span data-stu-id="9dd33-149">preroll</span></span>         | <span data-ttu-id="9dd33-150">從 *點* 移動向前算起的距離。</span><span class="sxs-lookup"><span data-stu-id="9dd33-150">Moves the preroll distance from the *in-point*.</span></span> <span data-ttu-id="9dd33-151">點對點是目前的位置，或是由 "from" 旗標所指定的位置。</span><span class="sxs-lookup"><span data-stu-id="9dd33-151">The in-point is the current position, or the position specified by the "from" flag.</span></span>                                                                                                                                                                            |
| <span data-ttu-id="9dd33-152">reverse</span><span class="sxs-lookup"><span data-stu-id="9dd33-152">reverse</span></span>         | <span data-ttu-id="9dd33-153">表示播放方向是反向 (回溯) 。</span><span class="sxs-lookup"><span data-stu-id="9dd33-153">Indicates play direction is in reverse (backward).</span></span>                                                                                                                                                                                                                                                             |
| <span data-ttu-id="9dd33-154">*定位*</span><span class="sxs-lookup"><span data-stu-id="9dd33-154">to *position*</span></span>   | <span data-ttu-id="9dd33-155">將工作區移至指定的位置。</span><span class="sxs-lookup"><span data-stu-id="9dd33-155">Moves the workspace to the specified position.</span></span> <span data-ttu-id="9dd33-156">若為 VCR 裝置，此旗標會指出停止的位置。</span><span class="sxs-lookup"><span data-stu-id="9dd33-156">For VCR devices, this flag indicates where to stop.</span></span>                                                                                                                                                                                                             |



 

</dd> <dt>

<span data-ttu-id="9dd33-157"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="9dd33-157"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="9dd33-158">可以是「等候」、「通知」或兩者。</span><span class="sxs-lookup"><span data-stu-id="9dd33-158">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="9dd33-159">針對數位影片和 VCR 裝置，也可以指定「測試」。</span><span class="sxs-lookup"><span data-stu-id="9dd33-159">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="9dd33-160">如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。</span><span class="sxs-lookup"><span data-stu-id="9dd33-160">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9dd33-161">傳回值</span><span class="sxs-lookup"><span data-stu-id="9dd33-161">Return Value</span></span>

<span data-ttu-id="9dd33-162">如果成功則傳回零，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="9dd33-162">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="9dd33-163">備註</span><span class="sxs-lookup"><span data-stu-id="9dd33-163">Remarks</span></span>

<span data-ttu-id="9dd33-164">雖然並非必要，但在某些裝置上播放或錄製之前發出提示命令可能會降低裝置啟動動作之前的延遲。</span><span class="sxs-lookup"><span data-stu-id="9dd33-164">Although it is not necessary, issuing the cue command before playing or recording on some devices might reduce the delay before the device starts the action.</span></span>

<span data-ttu-id="9dd33-165">如果播放或錄製正在進行中，或裝置已暫停，此命令將會失敗。</span><span class="sxs-lookup"><span data-stu-id="9dd33-165">This command fails if playing or recording is in progress or if the device is paused.</span></span>

<span data-ttu-id="9dd33-166">當使用提示 "output" ) 提示播放 (時，發出使用 "from"、"to" 或 "reverse" 旗標的 [play](play.md) 命令會取消提示命令。</span><span class="sxs-lookup"><span data-stu-id="9dd33-166">When cueing for playback (using cue "output"), issuing the [play](play.md) command with the "from", "to", or "reverse" flag cancels the cue command.</span></span>

<span data-ttu-id="9dd33-167">使用提示 "input" ) 提示錄製 (時，發出具有 "from"、"to" 或 "initialize" 旗標的 [記錄](record.md) 命令會取消提示命令。</span><span class="sxs-lookup"><span data-stu-id="9dd33-167">When cueing for recording (using cue "input"), issuing the [record](record.md) command with the "from", "to", or "initialize" flag cancels the cue command.</span></span>

## <a name="examples"></a><span data-ttu-id="9dd33-168">範例</span><span class="sxs-lookup"><span data-stu-id="9dd33-168">Examples</span></span>

<span data-ttu-id="9dd33-169">下列命令會準備 "mysound" 裝置以進行錄製。</span><span class="sxs-lookup"><span data-stu-id="9dd33-169">The following command prepares the "mysound" device for recording.</span></span>

``` syntax
cue mysound input
```

## <a name="requirements"></a><span data-ttu-id="9dd33-170">規格需求</span><span class="sxs-lookup"><span data-stu-id="9dd33-170">Requirements</span></span>



| <span data-ttu-id="9dd33-171">需求</span><span class="sxs-lookup"><span data-stu-id="9dd33-171">Requirement</span></span> | <span data-ttu-id="9dd33-172">值</span><span class="sxs-lookup"><span data-stu-id="9dd33-172">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="9dd33-173">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9dd33-173">Minimum supported client</span></span><br/> | <span data-ttu-id="9dd33-174">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9dd33-174">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="9dd33-175">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9dd33-175">Minimum supported server</span></span><br/> | <span data-ttu-id="9dd33-176">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9dd33-176">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="9dd33-177">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9dd33-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9dd33-178">Mci</span><span class="sxs-lookup"><span data-stu-id="9dd33-178">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="9dd33-179">MCI 命令字串</span><span class="sxs-lookup"><span data-stu-id="9dd33-179">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="9dd33-180">玩</span><span class="sxs-lookup"><span data-stu-id="9dd33-180">play</span></span>](play.md)
</dt> <dt>

[<span data-ttu-id="9dd33-181">記錄</span><span class="sxs-lookup"><span data-stu-id="9dd33-181">record</span></span>](record.md)
</dt> </dl>

 

