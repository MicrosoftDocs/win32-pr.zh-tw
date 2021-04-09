---
title: 凍結命令
description: 凍結命令會凍結 VCR 的影片輸入或影片輸出，或停用框架緩衝區的影片捕獲。 數位影片、影片重迭和 VCR 裝置都會辨識此命令。
ms.assetid: 49f3ab98-e893-402a-be78-6140af3b81df
keywords:
- 凍結命令 Windows 多媒體
topic_type:
- apiref
api_name:
- freeze
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7b63fbb2d888fc1ca315c0b511bcb18224c8168
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024568"
---
# <a name="freeze-command"></a><span data-ttu-id="1a763-105">凍結命令</span><span class="sxs-lookup"><span data-stu-id="1a763-105">freeze command</span></span>

<span data-ttu-id="1a763-106">凍結命令會凍結 VCR 的影片輸入或影片輸出，或停用框架緩衝區的影片捕獲。</span><span class="sxs-lookup"><span data-stu-id="1a763-106">The freeze command freezes video input or video output on a VCR or disables video acquisition to the frame buffer.</span></span> <span data-ttu-id="1a763-107">數位影片、影片重迭和 VCR 裝置都會辨識此命令。</span><span class="sxs-lookup"><span data-stu-id="1a763-107">Digital-video, video-overlay, and VCR devices recognize this command.</span></span>

<span data-ttu-id="1a763-108">若要傳送此命令，請使用 *lpszCommand* 參數設定來呼叫 [**mciSendString**](/previous-versions//dd757161(v=vs.85))函式，如下所示。</span><span class="sxs-lookup"><span data-stu-id="1a763-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("freeze %s %s %s"), 
  lpszDeviceID, 
  lpszFreezeFlags, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="1a763-109">參數</span><span class="sxs-lookup"><span data-stu-id="1a763-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a763-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="1a763-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="1a763-111">MCI 裝置的識別碼。</span><span class="sxs-lookup"><span data-stu-id="1a763-111">Identifier of an MCI device.</span></span> <span data-ttu-id="1a763-112">開啟裝置時，會指派此識別碼或別名。</span><span class="sxs-lookup"><span data-stu-id="1a763-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="1a763-113"><span id="lpszFreezeFlags"></span><span id="lpszfreezeflags"></span><span id="LPSZFREEZEFLAGS"></span>*lpszFreezeFlags*</span><span class="sxs-lookup"><span data-stu-id="1a763-113"><span id="lpszFreezeFlags"></span><span id="lpszfreezeflags"></span><span id="LPSZFREEZEFLAGS"></span>*lpszFreezeFlags*</span></span>
</dt> <dd>

<span data-ttu-id="1a763-114">識別要凍結之內容的旗標。</span><span class="sxs-lookup"><span data-stu-id="1a763-114">Flag that identifies what to freeze.</span></span> <span data-ttu-id="1a763-115">下表列出可辨識 **凍結** 命令的裝置類型，以及每種類型所使用的旗標。</span><span class="sxs-lookup"><span data-stu-id="1a763-115">The following table lists device types that recognize the **freeze** command and the flags used by each type.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1a763-116">值</span><span class="sxs-lookup"><span data-stu-id="1a763-116">Value</span></span></th>
<th><span data-ttu-id="1a763-117">意義</span><span class="sxs-lookup"><span data-stu-id="1a763-117">Meaning</span></span></th>
<th><span data-ttu-id="1a763-118">意義</span><span class="sxs-lookup"><span data-stu-id="1a763-118">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1a763-119">digitalvideo</span><span class="sxs-lookup"><span data-stu-id="1a763-119">digitalvideo</span></span></td>
<td><span data-ttu-id="1a763-120">在 <em>矩形</em></span><span class="sxs-lookup"><span data-stu-id="1a763-120">at <em>rectangle</em></span></span></td>
<td><span data-ttu-id="1a763-121">外面</span><span class="sxs-lookup"><span data-stu-id="1a763-121">outside</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1a763-122">overlay</span><span class="sxs-lookup"><span data-stu-id="1a763-122">overlay</span></span></td>
<td><span data-ttu-id="1a763-123">在 <em>矩形</em></span><span class="sxs-lookup"><span data-stu-id="1a763-123">at <em>rectangle</em></span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="1a763-124">錄影機</span><span class="sxs-lookup"><span data-stu-id="1a763-124">vcr</span></span></td>
<td><ul>
<li><span data-ttu-id="1a763-125">field</span><span class="sxs-lookup"><span data-stu-id="1a763-125">field</span></span></li>
<li><span data-ttu-id="1a763-126">框架</span><span class="sxs-lookup"><span data-stu-id="1a763-126">frame</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="1a763-127">input</span><span class="sxs-lookup"><span data-stu-id="1a763-127">input</span></span></li>
<li><span data-ttu-id="1a763-128">output</span><span class="sxs-lookup"><span data-stu-id="1a763-128">output</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="1a763-129">下表列出可在 *lpszFreezeFlags* 參數中指定的旗標，以及它們的意義。</span><span class="sxs-lookup"><span data-stu-id="1a763-129">The following table lists the flags that can be specified in the *lpszFreezeFlags* parameter and their meanings.</span></span>



| <span data-ttu-id="1a763-130">值</span><span class="sxs-lookup"><span data-stu-id="1a763-130">Value</span></span>          | <span data-ttu-id="1a763-131">意義</span><span class="sxs-lookup"><span data-stu-id="1a763-131">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a763-132">在 *矩形*</span><span class="sxs-lookup"><span data-stu-id="1a763-132">at *rectangle*</span></span> | <span data-ttu-id="1a763-133">指定即將凍結的區域。</span><span class="sxs-lookup"><span data-stu-id="1a763-133">Specifies the region that will be frozen.</span></span> <span data-ttu-id="1a763-134">針對影片重迭裝置，此區域將會停用影片的取得。</span><span class="sxs-lookup"><span data-stu-id="1a763-134">For video-overlay devices, this region will have video acquisition disabled.</span></span> <span data-ttu-id="1a763-135">針對數位影片裝置，除非) 指定「外部」旗標，否則矩形內的圖元將會開啟其鎖定遮罩位 (。</span><span class="sxs-lookup"><span data-stu-id="1a763-135">For digital-video devices, the pixels within the rectangle will have their lock mask bit turned on (unless the "outside" flag is specified).</span></span> <span data-ttu-id="1a763-136">矩形相對於影片緩衝區原點，並指定為 *X1 Y1 X2 Y2*。</span><span class="sxs-lookup"><span data-stu-id="1a763-136">The rectangle is relative to the video buffer origin and is specified as *X1 Y1 X2 Y2*.</span></span> <span data-ttu-id="1a763-137">座標 *X1 Y1* 指定矩形的左上角，而座標 *X2 Y2* 指定寬度和高度。</span><span class="sxs-lookup"><span data-stu-id="1a763-137">The coordinates *X1 Y1* specify the upper left corner of the rectangle, and the coordinates *X2 Y2* specify the width and height.</span></span> |
| <span data-ttu-id="1a763-138">field</span><span class="sxs-lookup"><span data-stu-id="1a763-138">field</span></span>          | <span data-ttu-id="1a763-139">凍結第一個欄位。</span><span class="sxs-lookup"><span data-stu-id="1a763-139">Freezes the first field.</span></span> <span data-ttu-id="1a763-140">如果未指定) 的框架或欄位，預設會假設為 (的欄位。</span><span class="sxs-lookup"><span data-stu-id="1a763-140">Field is assumed by default (if neither frame nor field is specified).</span></span>                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="1a763-141">框架</span><span class="sxs-lookup"><span data-stu-id="1a763-141">frame</span></span>          | <span data-ttu-id="1a763-142">凍結整個框架，同時顯示這兩個欄位。</span><span class="sxs-lookup"><span data-stu-id="1a763-142">Freezes the entire frame, displaying both fields.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="1a763-143">input</span><span class="sxs-lookup"><span data-stu-id="1a763-143">input</span></span>          | <span data-ttu-id="1a763-144">凍結輸入影像的目前畫面格（不論其是否已暫停或正在執行）。</span><span class="sxs-lookup"><span data-stu-id="1a763-144">Freezes the current frame of the input image, whether it is paused or running.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="1a763-145">output</span><span class="sxs-lookup"><span data-stu-id="1a763-145">output</span></span>         | <span data-ttu-id="1a763-146">從 VCR 凍結目前輸出的畫面格。</span><span class="sxs-lookup"><span data-stu-id="1a763-146">Freezes the current frame of the output from the VCR.</span></span> <span data-ttu-id="1a763-147">如果在發出凍結時現正播放 VCR，則會凍結目前的框架，並暫停 VCR。</span><span class="sxs-lookup"><span data-stu-id="1a763-147">If the VCR is playing when freeze is issued, the current frame is frozen and the VCR is paused.</span></span> <span data-ttu-id="1a763-148">如果在發出此命令時，會暫停 VCR，則會凍結目前的框架。</span><span class="sxs-lookup"><span data-stu-id="1a763-148">If the VCR is paused when this command is issued, the current frame is frozen.</span></span> <span data-ttu-id="1a763-149">凍結的映射會保留在輸出裝置上，直到發出 [解除凍結](unfreeze.md) 命令為止。</span><span class="sxs-lookup"><span data-stu-id="1a763-149">The frozen image remains on the output device until an [unfreeze](unfreeze.md) command is issued.</span></span> <span data-ttu-id="1a763-150">如果未指定 "input" 或 "output"，則會假設為 "output"。</span><span class="sxs-lookup"><span data-stu-id="1a763-150">If neither "input" nor "output" is specified, "output" is assumed.</span></span>                                                                                    |
| <span data-ttu-id="1a763-151">外面</span><span class="sxs-lookup"><span data-stu-id="1a763-151">outside</span></span>        | <span data-ttu-id="1a763-152">表示已凍結使用 "at" 旗標指定區域以外的區域。</span><span class="sxs-lookup"><span data-stu-id="1a763-152">Indicates that the area outside the region specified using the "at" flag is frozen.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                           |



 

</dd> <dt>

<span data-ttu-id="1a763-153"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="1a763-153"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="1a763-154">可以是「等候」、「通知」或兩者。</span><span class="sxs-lookup"><span data-stu-id="1a763-154">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="1a763-155">針對數位影片和 VCR 裝置，也可以指定「測試」。</span><span class="sxs-lookup"><span data-stu-id="1a763-155">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="1a763-156">如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。</span><span class="sxs-lookup"><span data-stu-id="1a763-156">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a763-157">傳回值</span><span class="sxs-lookup"><span data-stu-id="1a763-157">Return Value</span></span>

<span data-ttu-id="1a763-158">如果成功則傳回零，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="1a763-158">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="1a763-159">備註</span><span class="sxs-lookup"><span data-stu-id="1a763-159">Remarks</span></span>

<span data-ttu-id="1a763-160">搭配使用 VCR 裝置時，此命令適用于框架抓取卡。</span><span class="sxs-lookup"><span data-stu-id="1a763-160">When used with VCR devices, this command is intended for frame-grabbing cards.</span></span>

<span data-ttu-id="1a763-161">若要使用 "at" 旗標來指定不規則的取得區域，請使用一連串的凍結和 [解除凍結](unfreeze.md) 命令。</span><span class="sxs-lookup"><span data-stu-id="1a763-161">To specify irregular acquisition regions with the "at" flag, use a series of freeze and [unfreeze](unfreeze.md) commands.</span></span> <span data-ttu-id="1a763-162">某些影片重迭裝置會限制取得區域的複雜度。</span><span class="sxs-lookup"><span data-stu-id="1a763-162">Some video-overlay devices limit the complexity of the acquisition region.</span></span>

<span data-ttu-id="1a763-163">只有在具有「可凍結」旗標的 [ [功能](capability.md) ] 命令呼叫傳回 **TRUE** 時，才支援這個命令。</span><span class="sxs-lookup"><span data-stu-id="1a763-163">This command is supported only if a call to the [capability](capability.md) command with the "can freeze" flag returns **TRUE**.</span></span>

## <a name="examples"></a><span data-ttu-id="1a763-164">範例</span><span class="sxs-lookup"><span data-stu-id="1a763-164">Examples</span></span>

<span data-ttu-id="1a763-165">下列命令會停用影片緩衝區左上角 100-圖元正方形的影片取得。</span><span class="sxs-lookup"><span data-stu-id="1a763-165">The following command disables video acquisition in a 100-pixel square at the upper left corner of the video buffer.</span></span>

``` syntax
freeze vboard at 0 0 100 100
```

## <a name="requirements"></a><span data-ttu-id="1a763-166">規格需求</span><span class="sxs-lookup"><span data-stu-id="1a763-166">Requirements</span></span>



| <span data-ttu-id="1a763-167">需求</span><span class="sxs-lookup"><span data-stu-id="1a763-167">Requirement</span></span> | <span data-ttu-id="1a763-168">值</span><span class="sxs-lookup"><span data-stu-id="1a763-168">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="1a763-169">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1a763-169">Minimum supported client</span></span><br/> | <span data-ttu-id="1a763-170">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1a763-170">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="1a763-171">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1a763-171">Minimum supported server</span></span><br/> | <span data-ttu-id="1a763-172">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1a763-172">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="1a763-173">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1a763-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a763-174">Mci</span><span class="sxs-lookup"><span data-stu-id="1a763-174">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="1a763-175">MCI 命令字串</span><span class="sxs-lookup"><span data-stu-id="1a763-175">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="1a763-176">capability</span><span class="sxs-lookup"><span data-stu-id="1a763-176">capability</span></span>](capability.md)
</dt> <dt>

[<span data-ttu-id="1a763-177">解凍</span><span class="sxs-lookup"><span data-stu-id="1a763-177">unfreeze</span></span>](unfreeze.md)
</dt> </dl>

 

