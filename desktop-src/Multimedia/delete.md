---
title: delete 命令
description: Delete 命令會刪除檔案中的資料區段。 數位-視頻和波形-音訊裝置辨識此命令。
ms.assetid: 9cf084f6-d64e-4487-9407-b68502b7cec9
keywords:
- 刪除命令 Windows 多媒體
topic_type:
- apiref
api_name:
- delete
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e356d4972384e676f2e521bd2ca102bb21d7ef2c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844231"
---
# <a name="delete-command"></a><span data-ttu-id="adba8-105">delete 命令</span><span class="sxs-lookup"><span data-stu-id="adba8-105">delete command</span></span>

<span data-ttu-id="adba8-106">Delete 命令會刪除檔案中的資料區段。</span><span class="sxs-lookup"><span data-stu-id="adba8-106">The delete command deletes a data segment from a file.</span></span> <span data-ttu-id="adba8-107">數位-視頻和波形-音訊裝置辨識此命令。</span><span class="sxs-lookup"><span data-stu-id="adba8-107">Digital-video and waveform-audio devices recognize this command.</span></span>

<span data-ttu-id="adba8-108">若要傳送此命令，請使用 *lpszCommand* 參數設定來呼叫 [**mciSendString**](/previous-versions//dd757161(v=vs.85))函式，如下所示。</span><span class="sxs-lookup"><span data-stu-id="adba8-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("delete %s %s %s"), 
  lpszDeviceID, 
  lpszPosition, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="adba8-109">參數</span><span class="sxs-lookup"><span data-stu-id="adba8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="adba8-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="adba8-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="adba8-111">MCI 裝置的識別碼。</span><span class="sxs-lookup"><span data-stu-id="adba8-111">Identifier of an MCI device.</span></span> <span data-ttu-id="adba8-112">開啟裝置時，會指派此識別碼或別名。</span><span class="sxs-lookup"><span data-stu-id="adba8-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="adba8-113"><span id="lpszPosition"></span><span id="lpszposition"></span><span id="LPSZPOSITION"></span>*lpszPosition*</span><span class="sxs-lookup"><span data-stu-id="adba8-113"><span id="lpszPosition"></span><span id="lpszposition"></span><span id="LPSZPOSITION"></span>*lpszPosition*</span></span>
</dt> <dd>

<span data-ttu-id="adba8-114">識別要刪除之資料區段的旗標。</span><span class="sxs-lookup"><span data-stu-id="adba8-114">Flag that identifies a data segment to delete.</span></span> <span data-ttu-id="adba8-115">下表列出可辨識 **刪除** 命令的裝置類型，以及每種類型所使用的旗標。</span><span class="sxs-lookup"><span data-stu-id="adba8-115">The following table lists device types that recognize the **delete** command and the flags used by each type.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="adba8-116">值</span><span class="sxs-lookup"><span data-stu-id="adba8-116">Value</span></span></th>
<th><span data-ttu-id="adba8-117">意義</span><span class="sxs-lookup"><span data-stu-id="adba8-117">Meaning</span></span></th>
<th><span data-ttu-id="adba8-118">意義</span><span class="sxs-lookup"><span data-stu-id="adba8-118">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="adba8-119">digitalvideo</span><span class="sxs-lookup"><span data-stu-id="adba8-119">digitalvideo</span></span></td>
<td><ul>
<li><span data-ttu-id="adba8-120">在 <em>矩形</em></span><span class="sxs-lookup"><span data-stu-id="adba8-120">at <em>rectangle</em></span></span></li>
<li><span data-ttu-id="adba8-121">音訊串流 <em>串流</em></span><span class="sxs-lookup"><span data-stu-id="adba8-121">audio stream <em>stream</em></span></span></li>
<li><span data-ttu-id="adba8-122">從 <em>位置</em></span><span class="sxs-lookup"><span data-stu-id="adba8-122">from <em>position</em></span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="adba8-123"><em>定位</em></span><span class="sxs-lookup"><span data-stu-id="adba8-123">to <em>position</em></span></span></li>
<li><span data-ttu-id="adba8-124">影片串流 <em>串流</em></span><span class="sxs-lookup"><span data-stu-id="adba8-124">video stream <em>stream</em></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="adba8-125">waveaudio</span><span class="sxs-lookup"><span data-stu-id="adba8-125">waveaudio</span></span></td>
<td><span data-ttu-id="adba8-126">從 <em>位置</em></span><span class="sxs-lookup"><span data-stu-id="adba8-126">from <em>position</em></span></span></td>
<td><span data-ttu-id="adba8-127"><em>定位</em></span><span class="sxs-lookup"><span data-stu-id="adba8-127">to <em>position</em></span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="adba8-128">下表列出可在 *lpszPosition* 參數中指定的旗標，以及它們的意義。</span><span class="sxs-lookup"><span data-stu-id="adba8-128">The following table lists the flags that can be specified in the *lpszPosition* parameter and their meanings.</span></span>



| <span data-ttu-id="adba8-129">值</span><span class="sxs-lookup"><span data-stu-id="adba8-129">Value</span></span>                 | <span data-ttu-id="adba8-130">意義</span><span class="sxs-lookup"><span data-stu-id="adba8-130">Meaning</span></span>                                                                                                                                                                                                                                      |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="adba8-131">在 *矩形*</span><span class="sxs-lookup"><span data-stu-id="adba8-131">at *rectangle*</span></span>        | <span data-ttu-id="adba8-132">指定刪除每個框架的部分。</span><span class="sxs-lookup"><span data-stu-id="adba8-132">Specifies the portion of each frame deleted.</span></span> <span data-ttu-id="adba8-133">如果省略，則會預設為整個框架。</span><span class="sxs-lookup"><span data-stu-id="adba8-133">If omitted, it defaults to the entire frame.</span></span> <span data-ttu-id="adba8-134">指定此專案時，不會刪除畫面格。</span><span class="sxs-lookup"><span data-stu-id="adba8-134">When this item is specified, frames are not deleted.</span></span> <span data-ttu-id="adba8-135">而是矩形內的區域會變成黑色。</span><span class="sxs-lookup"><span data-stu-id="adba8-135">Instead the area inside the rectangle becomes black.</span></span>                                          |
| <span data-ttu-id="adba8-136">音訊串流 *串流*</span><span class="sxs-lookup"><span data-stu-id="adba8-136">audio stream *stream*</span></span> | <span data-ttu-id="adba8-137">指定工作區中受命令影響的音訊串流。</span><span class="sxs-lookup"><span data-stu-id="adba8-137">Specifies the audio stream in the workspace affected by the command.</span></span> <span data-ttu-id="adba8-138">如果您使用此旗標，而且也想要刪除影片，您也必須使用「影片串流」旗標。</span><span class="sxs-lookup"><span data-stu-id="adba8-138">If you use this flag and also want to delete video, you must also use the "video stream" flag.</span></span> <span data-ttu-id="adba8-139"> (如果未指定任何旗標，則會刪除所有音訊和影片串流。 ) </span><span class="sxs-lookup"><span data-stu-id="adba8-139">(If neither flag is specified, all audio and video streams are deleted.)</span></span> |
| <span data-ttu-id="adba8-140">從 *位置*</span><span class="sxs-lookup"><span data-stu-id="adba8-140">from *position*</span></span>       | <span data-ttu-id="adba8-141">指定開始刪除的位置。</span><span class="sxs-lookup"><span data-stu-id="adba8-141">Specifies the position at which deletion begins.</span></span> <span data-ttu-id="adba8-142">如果省略此旗標，則會從目前的位置開始刪除。</span><span class="sxs-lookup"><span data-stu-id="adba8-142">If this flag is omitted, the deletion begins at the current position.</span></span>                                                                                                                       |
| <span data-ttu-id="adba8-143">*定位*</span><span class="sxs-lookup"><span data-stu-id="adba8-143">to *position*</span></span>         | <span data-ttu-id="adba8-144">指定刪除結束的位置。</span><span class="sxs-lookup"><span data-stu-id="adba8-144">Specifies the position at which deletion ends.</span></span> <span data-ttu-id="adba8-145">如果省略此旗標，則刪除作業會繼續至內容或工作區的結尾。</span><span class="sxs-lookup"><span data-stu-id="adba8-145">If this flag is omitted, the deletion continues to the end of the content or workspace.</span></span>                                                                                                       |
| <span data-ttu-id="adba8-146">影片串流 *串流*</span><span class="sxs-lookup"><span data-stu-id="adba8-146">video stream *stream*</span></span> | <span data-ttu-id="adba8-147">在工作區中指定受命令影響的影片串流。</span><span class="sxs-lookup"><span data-stu-id="adba8-147">Specifies the video stream in the workspace affected by the command.</span></span> <span data-ttu-id="adba8-148">如果您使用此旗標，而且也想要刪除音訊，您也必須使用「音訊串流」旗標。</span><span class="sxs-lookup"><span data-stu-id="adba8-148">If you use this flag and also want to delete audio, you must also use "audio stream" flag.</span></span> <span data-ttu-id="adba8-149"> (如果未指定任何旗標，則會刪除所有音訊和影片串流。 ) </span><span class="sxs-lookup"><span data-stu-id="adba8-149">(If neither flag is specified, all audio and video streams are deleted.)</span></span>     |



 

</dd> <dt>

<span data-ttu-id="adba8-150"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="adba8-150"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="adba8-151">可以是「等候」、「通知」或兩者。</span><span class="sxs-lookup"><span data-stu-id="adba8-151">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="adba8-152">針對數位影片和 VCR 裝置，也可以指定「測試」。</span><span class="sxs-lookup"><span data-stu-id="adba8-152">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="adba8-153">如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。</span><span class="sxs-lookup"><span data-stu-id="adba8-153">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="adba8-154">傳回值</span><span class="sxs-lookup"><span data-stu-id="adba8-154">Return Value</span></span>

<span data-ttu-id="adba8-155">如果成功則傳回零，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="adba8-155">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="adba8-156">備註</span><span class="sxs-lookup"><span data-stu-id="adba8-156">Remarks</span></span>

<span data-ttu-id="adba8-157">發出使用位置值的任何命令之前，您應該使用 [set](set.md) 命令來設定所需的時間格式。</span><span class="sxs-lookup"><span data-stu-id="adba8-157">Before issuing any commands that use position values, you should set the desired time format by using the [set](set.md) command.</span></span>

## <a name="examples"></a><span data-ttu-id="adba8-158">範例</span><span class="sxs-lookup"><span data-stu-id="adba8-158">Examples</span></span>

<span data-ttu-id="adba8-159">下列命令會從1毫秒到900毫秒來刪除波形音訊資料 (假設時間格式設定為毫秒) 。</span><span class="sxs-lookup"><span data-stu-id="adba8-159">The following command deletes the waveform-audio data from 1 millisecond through 900 milliseconds (assuming the time format is set to milliseconds).</span></span>

``` syntax
delete mysound from 1 to 900
```

## <a name="requirements"></a><span data-ttu-id="adba8-160">規格需求</span><span class="sxs-lookup"><span data-stu-id="adba8-160">Requirements</span></span>



| <span data-ttu-id="adba8-161">需求</span><span class="sxs-lookup"><span data-stu-id="adba8-161">Requirement</span></span> | <span data-ttu-id="adba8-162">值</span><span class="sxs-lookup"><span data-stu-id="adba8-162">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="adba8-163">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="adba8-163">Minimum supported client</span></span><br/> | <span data-ttu-id="adba8-164">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="adba8-164">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="adba8-165">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="adba8-165">Minimum supported server</span></span><br/> | <span data-ttu-id="adba8-166">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="adba8-166">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="adba8-167">另請參閱</span><span class="sxs-lookup"><span data-stu-id="adba8-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="adba8-168">Mci</span><span class="sxs-lookup"><span data-stu-id="adba8-168">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="adba8-169">MCI 命令字串</span><span class="sxs-lookup"><span data-stu-id="adba8-169">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="adba8-170">set</span><span class="sxs-lookup"><span data-stu-id="adba8-170">set</span></span>](set.md)
</dt> </dl>

 

