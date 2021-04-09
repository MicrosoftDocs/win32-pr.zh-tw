---
title: 貼上命令
description: '[貼上] 命令會將剪貼簿的內容複寫到工作區。 數位影片裝置辨識此命令。'
ms.assetid: c09418e1-2535-40d1-8912-e5ece91ee673
keywords:
- 貼上命令 Windows 多媒體
topic_type:
- apiref
api_name:
- paste
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 482fd744d7e6e163059330148b6e3f081d435880
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024782"
---
# <a name="paste-command"></a><span data-ttu-id="d24a4-105">貼上命令</span><span class="sxs-lookup"><span data-stu-id="d24a4-105">paste command</span></span>

<span data-ttu-id="d24a4-106">[貼上] 命令會將剪貼簿的內容複寫到工作區。</span><span class="sxs-lookup"><span data-stu-id="d24a4-106">The paste command copies the contents of the clipboard into the workspace.</span></span> <span data-ttu-id="d24a4-107">數位影片裝置辨識此命令。</span><span class="sxs-lookup"><span data-stu-id="d24a4-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="d24a4-108">若要傳送此命令，請使用 *lpszCommand* 參數設定來呼叫 [**mciSendString**](/previous-versions//dd757161(v=vs.85))函式，如下所示。</span><span class="sxs-lookup"><span data-stu-id="d24a4-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("paste %s %s %s"), 
  lpszDeviceID, 
  lpszItem, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="d24a4-109">參數</span><span class="sxs-lookup"><span data-stu-id="d24a4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d24a4-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="d24a4-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="d24a4-111">MCI 裝置的識別碼。</span><span class="sxs-lookup"><span data-stu-id="d24a4-111">Identifier of an MCI device.</span></span> <span data-ttu-id="d24a4-112">開啟裝置時，會指派此識別碼或別名。</span><span class="sxs-lookup"><span data-stu-id="d24a4-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="d24a4-113"><span id="lpszItem"></span><span id="lpszitem"></span><span id="LPSZITEM"></span>*lpszItem*</span><span class="sxs-lookup"><span data-stu-id="d24a4-113"><span id="lpszItem"></span><span id="lpszitem"></span><span id="LPSZITEM"></span>*lpszItem*</span></span>
</dt> <dd>

<span data-ttu-id="d24a4-114">下列一或多個旗標。</span><span class="sxs-lookup"><span data-stu-id="d24a4-114">One or more of the following flags.</span></span>



| <span data-ttu-id="d24a4-115">值</span><span class="sxs-lookup"><span data-stu-id="d24a4-115">Value</span></span>                 | <span data-ttu-id="d24a4-116">意義</span><span class="sxs-lookup"><span data-stu-id="d24a4-116">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d24a4-117">在 *矩形*</span><span class="sxs-lookup"><span data-stu-id="d24a4-117">at *rectangle*</span></span>        | <span data-ttu-id="d24a4-118">指定要貼上資料的框架內的位置。</span><span class="sxs-lookup"><span data-stu-id="d24a4-118">Specifies the location within the frame where the data is pasted.</span></span> <span data-ttu-id="d24a4-119">*矩形* 的左上角會對應至已加入資料的左上角。</span><span class="sxs-lookup"><span data-stu-id="d24a4-119">The upper left corner of the *rectangle* corresponds to the upper left corner of the added data.</span></span> <span data-ttu-id="d24a4-120">如果矩形在 X 或 Y 中的大小為非零，則在將剪貼簿的內容貼到框架時，剪貼簿的內容會在這些維度中縮放。</span><span class="sxs-lookup"><span data-stu-id="d24a4-120">If the rectangle has a nonzero size in X or Y, the contents of the clipboard are scaled in those dimensions when they are pasted into the frame.</span></span> <span data-ttu-id="d24a4-121">如果省略， *矩形* 就會預設為整個框架。</span><span class="sxs-lookup"><span data-stu-id="d24a4-121">If omitted, the *rectangle* defaults to the entire frame.</span></span> <span data-ttu-id="d24a4-122">如果這個旗標是在 [插入] 模式中指定 (預設) ，則矩形之外的任何區域都是以純色繪製。</span><span class="sxs-lookup"><span data-stu-id="d24a4-122">If this flag is specified in "insert" mode (the default), any region outside the rectangle is painted a solid color.</span></span>                       |
| <span data-ttu-id="d24a4-123">音訊串流 *串流*</span><span class="sxs-lookup"><span data-stu-id="d24a4-123">audio stream *stream*</span></span> | <span data-ttu-id="d24a4-124">指定工作區中受命令影響的音訊串流。</span><span class="sxs-lookup"><span data-stu-id="d24a4-124">Specifies the audio stream in the workspace affected by the command.</span></span> <span data-ttu-id="d24a4-125">如果剪貼簿中只有一個音訊串流，則會將音訊資料貼入指定的 *資料流程*。</span><span class="sxs-lookup"><span data-stu-id="d24a4-125">If only one audio stream exists on the clipboard, the audio data is pasted into the designated *stream*.</span></span> <span data-ttu-id="d24a4-126">如果剪貼簿中有一個以上的音訊串流， *資料流程* 就會指出資料流程順序的起始數位。</span><span class="sxs-lookup"><span data-stu-id="d24a4-126">If more than one audio stream exists on the clipboard, the *stream* indicates the starting number for the stream sequences.</span></span> <span data-ttu-id="d24a4-127">如果您使用此旗標，而且也想要貼上影片，您也必須使用「影片串流」旗標。</span><span class="sxs-lookup"><span data-stu-id="d24a4-127">If you use this flag and also want to paste video, you must also use the "video stream" flag.</span></span> <span data-ttu-id="d24a4-128"> (如果未指定任何旗標，則會貼上所有音訊和影片串流，並保留原始的串流號碼。 ) </span><span class="sxs-lookup"><span data-stu-id="d24a4-128">(If neither flag is specified, all audio and video streams are pasted and retain their original stream numbers.)</span></span> |
| <span data-ttu-id="d24a4-129">insert</span><span class="sxs-lookup"><span data-stu-id="d24a4-129">insert</span></span>                | <span data-ttu-id="d24a4-130">指定將資料插入工作區中。</span><span class="sxs-lookup"><span data-stu-id="d24a4-130">Specifies that the data is inserted into the workspace.</span></span> <span data-ttu-id="d24a4-131">插入點之後的任何資料會在工作空間中向前移動以騰出空間。</span><span class="sxs-lookup"><span data-stu-id="d24a4-131">Any data after the insertion point is moved forward in the workspace to make room.</span></span> <span data-ttu-id="d24a4-132">這是預設值。</span><span class="sxs-lookup"><span data-stu-id="d24a4-132">This is the default value.</span></span>                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="d24a4-133">overwrite</span><span class="sxs-lookup"><span data-stu-id="d24a4-133">overwrite</span></span>             | <span data-ttu-id="d24a4-134">指定在插入點之後寫入任何現有資料，以將資料複製到工作區。</span><span class="sxs-lookup"><span data-stu-id="d24a4-134">Specifies that the data is copied into the workspace by writing over any existing data after the insertion point.</span></span> <span data-ttu-id="d24a4-135">「插入」和「覆寫」旗標會影響在貼上作業期間是否終結或移動框架，而不是在每個框架中貼上資料的方式。</span><span class="sxs-lookup"><span data-stu-id="d24a4-135">The "insert" and "overwrite" flags affect whether frames are destroyed or moved during the paste operation, not how the data is pasted within each frame.</span></span>                                                                                                                                                                                                                                              |
| <span data-ttu-id="d24a4-136">*定位*</span><span class="sxs-lookup"><span data-stu-id="d24a4-136">to *position*</span></span>         | <span data-ttu-id="d24a4-137">指定工作區中貼上資料的位置。</span><span class="sxs-lookup"><span data-stu-id="d24a4-137">Specifies the position in the workspace at which the data is pasted.</span></span> <span data-ttu-id="d24a4-138">如果省略，則會預設為目前的位置。</span><span class="sxs-lookup"><span data-stu-id="d24a4-138">If omitted, it defaults to the current position.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="d24a4-139">影片串流 *串流*</span><span class="sxs-lookup"><span data-stu-id="d24a4-139">video stream *stream*</span></span> | <span data-ttu-id="d24a4-140">在工作區中指定受命令影響的影片串流。</span><span class="sxs-lookup"><span data-stu-id="d24a4-140">Specifies the video stream in the workspace affected by the command.</span></span> <span data-ttu-id="d24a4-141">如果剪貼簿中只有一個影片串流，則會將影片資料貼入指定的 *資料流程*。</span><span class="sxs-lookup"><span data-stu-id="d24a4-141">If only one video stream exists on the clipboard, the video data is pasted into the designated *stream*.</span></span> <span data-ttu-id="d24a4-142">如果剪貼簿中有一個以上的影片串流， *資料流程* 就會指出資料流程順序的起始數位。</span><span class="sxs-lookup"><span data-stu-id="d24a4-142">If more than one video stream exists on the clipboard, the *stream* indicates the starting number for the stream sequences.</span></span> <span data-ttu-id="d24a4-143">如果您使用此旗標，而且也想要貼上音訊，您也必須使用「音訊串流」旗標。</span><span class="sxs-lookup"><span data-stu-id="d24a4-143">If you use this flag and also want to paste audio, you must also use the "audio stream" flag.</span></span> <span data-ttu-id="d24a4-144"> (如果未指定任何旗標，則會貼上所有音訊和影片串流，並保留原始的串流號碼。 ) </span><span class="sxs-lookup"><span data-stu-id="d24a4-144">(If neither flag is specified, all audio and video streams are pasted and retain their original stream numbers.)</span></span> |



 

</dd> <dt>

<span data-ttu-id="d24a4-145"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="d24a4-145"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="d24a4-146">可以是「等候」、「通知」、「測試」或它們的組合。</span><span class="sxs-lookup"><span data-stu-id="d24a4-146">Can be "wait", "notify", "test", or a combination of these.</span></span> <span data-ttu-id="d24a4-147">如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。</span><span class="sxs-lookup"><span data-stu-id="d24a4-147">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d24a4-148">傳回值</span><span class="sxs-lookup"><span data-stu-id="d24a4-148">Return Value</span></span>

<span data-ttu-id="d24a4-149">如果成功則傳回零，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="d24a4-149">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="d24a4-150">備註</span><span class="sxs-lookup"><span data-stu-id="d24a4-150">Remarks</span></span>

<span data-ttu-id="d24a4-151">從剪貼簿複製的資料中不會出現任何信號。</span><span class="sxs-lookup"><span data-stu-id="d24a4-151">No signals are present in the data copied from the clipboard.</span></span> <span data-ttu-id="d24a4-152">只有在明確儲存資料時，變更才會變成永久;不過，播放的行為就如同已新增資料一樣。</span><span class="sxs-lookup"><span data-stu-id="d24a4-152">The change becomes permanent only when the data is explicitly saved; however, playback acts as if the data has been added.</span></span>

## <a name="requirements"></a><span data-ttu-id="d24a4-153">規格需求</span><span class="sxs-lookup"><span data-stu-id="d24a4-153">Requirements</span></span>



| <span data-ttu-id="d24a4-154">需求</span><span class="sxs-lookup"><span data-stu-id="d24a4-154">Requirement</span></span> | <span data-ttu-id="d24a4-155">值</span><span class="sxs-lookup"><span data-stu-id="d24a4-155">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="d24a4-156">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d24a4-156">Minimum supported client</span></span><br/> | <span data-ttu-id="d24a4-157">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d24a4-157">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="d24a4-158">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d24a4-158">Minimum supported server</span></span><br/> | <span data-ttu-id="d24a4-159">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d24a4-159">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="d24a4-160">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d24a4-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d24a4-161">Mci</span><span class="sxs-lookup"><span data-stu-id="d24a4-161">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="d24a4-162">MCI 命令字串</span><span class="sxs-lookup"><span data-stu-id="d24a4-162">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 

