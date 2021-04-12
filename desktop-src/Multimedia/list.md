---
title: list 命令
description: List 命令會決定影片和音訊輸入的數目和類型。 數位影片和 VCR 裝置會辨識此命令。
ms.assetid: b3fe3819-0b8a-4de5-9c79-03e1e089436f
keywords:
- 列出命令 Windows 多媒體
topic_type:
- apiref
api_name:
- list
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5d0a171c6768caf1b947a0d07cb46e5cccd28c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106212"
---
# <a name="list-command"></a><span data-ttu-id="380ac-105">list 命令</span><span class="sxs-lookup"><span data-stu-id="380ac-105">list command</span></span>

<span data-ttu-id="380ac-106">List 命令會決定影片和音訊輸入的數目和類型。</span><span class="sxs-lookup"><span data-stu-id="380ac-106">The list command determines the number and types of video and audio inputs.</span></span> <span data-ttu-id="380ac-107">數位影片和 VCR 裝置會辨識此命令。</span><span class="sxs-lookup"><span data-stu-id="380ac-107">Digital-video and VCR devices recognize this command.</span></span>

<span data-ttu-id="380ac-108">若要傳送此命令，請使用 *lpszCommand* 參數設定來呼叫 [**mciSendString**](/previous-versions//dd757161(v=vs.85))函式，如下所示。</span><span class="sxs-lookup"><span data-stu-id="380ac-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("list %s %s %s"), 
  lpszDeviceID, 
  lpszList, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="380ac-109">參數</span><span class="sxs-lookup"><span data-stu-id="380ac-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="380ac-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="380ac-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="380ac-111">MCI 裝置的識別碼。</span><span class="sxs-lookup"><span data-stu-id="380ac-111">Identifier of an MCI device.</span></span> <span data-ttu-id="380ac-112">開啟裝置時，會指派此識別碼或別名。</span><span class="sxs-lookup"><span data-stu-id="380ac-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="380ac-113"><span id="lpszList"></span><span id="lpszlist"></span><span id="LPSZLIST"></span>*lpszList*</span><span class="sxs-lookup"><span data-stu-id="380ac-113"><span id="lpszList"></span><span id="lpszlist"></span><span id="LPSZLIST"></span>*lpszList*</span></span>
</dt> <dd>

<span data-ttu-id="380ac-114">旗標，可識別影片和音訊輸入的數目和類型。</span><span class="sxs-lookup"><span data-stu-id="380ac-114">Flag that identifies the number and types of video and audio inputs.</span></span> <span data-ttu-id="380ac-115">下表列出可辨識 **清單** 命令的裝置類型，以及每種類型所使用的旗標。</span><span class="sxs-lookup"><span data-stu-id="380ac-115">The following table lists device types that recognize the **list** command and the flags used by each type.</span></span>



| <span data-ttu-id="380ac-116">值</span><span class="sxs-lookup"><span data-stu-id="380ac-116">Value</span></span>        | <span data-ttu-id="380ac-117">意義</span><span class="sxs-lookup"><span data-stu-id="380ac-117">Meaning</span></span>                                                                           | <span data-ttu-id="380ac-118">意義</span><span class="sxs-lookup"><span data-stu-id="380ac-118">Meaning</span></span>                                                                                                                      |
|--------------|-----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="380ac-119">digitalvideo</span><span class="sxs-lookup"><span data-stu-id="380ac-119">digitalvideo</span></span> | <span data-ttu-id="380ac-120">音訊 algorithmaudio 品質演算法 *演算法* 音訊 streamcountnumber *索引*</span><span class="sxs-lookup"><span data-stu-id="380ac-120">audio algorithmaudio quality algorithm *algorithm* audio streamcountnumber *index*</span></span> | <span data-ttu-id="380ac-121">仍 algorithmstill 品質演算法 *演算法* 影片 algorithmvideo 品質演算法 *演算法* 影片 sourcevideo 串流</span><span class="sxs-lookup"><span data-stu-id="380ac-121">still algorithmstill quality algorithm *algorithm* video algorithmvideo quality algorithm *algorithm* video sourcevideo stream</span></span> |
| <span data-ttu-id="380ac-122">錄影機</span><span class="sxs-lookup"><span data-stu-id="380ac-122">vcr</span></span>          | <span data-ttu-id="380ac-123">音訊來源 countaudio 來源編號 *索引*</span><span class="sxs-lookup"><span data-stu-id="380ac-123">audio source countaudio source number *index*</span></span>                                     | <span data-ttu-id="380ac-124">影片來源 countvideo 來源編號 *索引*</span><span class="sxs-lookup"><span data-stu-id="380ac-124">video source countvideo source number *index*</span></span>                                                                                |



 

<span data-ttu-id="380ac-125">下表列出可在 **lpszList** 參數中指定的旗標，以及它們的意義。</span><span class="sxs-lookup"><span data-stu-id="380ac-125">The following table lists the flags that can be specified in the **lpszList** parameter and their meanings.</span></span>



| <span data-ttu-id="380ac-126">值</span><span class="sxs-lookup"><span data-stu-id="380ac-126">Value</span></span>                               | <span data-ttu-id="380ac-127">意義</span><span class="sxs-lookup"><span data-stu-id="380ac-127">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="380ac-128">音訊演算法</span><span class="sxs-lookup"><span data-stu-id="380ac-128">audio algorithm</span></span>                     | <span data-ttu-id="380ac-129">指定命令應該取出音訊演算法名稱。</span><span class="sxs-lookup"><span data-stu-id="380ac-129">Specifies the command should retrieve audio algorithm names.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="380ac-130">音訊品質演算法 *演算法*</span><span class="sxs-lookup"><span data-stu-id="380ac-130">audio quality algorithm *algorithm*</span></span> | <span data-ttu-id="380ac-131">指定命令應該會取得與指定之 *演算法* 相關聯的品質等級。</span><span class="sxs-lookup"><span data-stu-id="380ac-131">Specifies the command should retrieve quality levels associated with the specified *algorithm*.</span></span> <span data-ttu-id="380ac-132">如果 *演算法* 為「目前」，則會傳回目前演算法的品質等級。</span><span class="sxs-lookup"><span data-stu-id="380ac-132">If *algorithm* is "current", the quality level of the current algorithm is returned.</span></span>                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="380ac-133">音訊來源計數</span><span class="sxs-lookup"><span data-stu-id="380ac-133">audio source count</span></span>                  | <span data-ttu-id="380ac-134">傳回音頻輸入的總數目。</span><span class="sxs-lookup"><span data-stu-id="380ac-134">Returns the total number of audio inputs.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="380ac-135">音訊來源編號 *索引*</span><span class="sxs-lookup"><span data-stu-id="380ac-135">audio source number *index*</span></span>         | <span data-ttu-id="380ac-136">傳回來源 *索引* 之音訊輸入的類型。</span><span class="sxs-lookup"><span data-stu-id="380ac-136">Returns the type of audio input of source *index*.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="380ac-137">音訊串流</span><span class="sxs-lookup"><span data-stu-id="380ac-137">audio stream</span></span>                        | <span data-ttu-id="380ac-138">指定命令應該取得與工作區相關聯之音訊串流的名稱。</span><span class="sxs-lookup"><span data-stu-id="380ac-138">Specifies the command should retrieve the names of the audio streams associated with the workspace.</span></span> <span data-ttu-id="380ac-139">這些字串 (例如 "英文" 或 "德文" ) 會內嵌在檔案中，並識別該資料流程。</span><span class="sxs-lookup"><span data-stu-id="380ac-139">These strings (such as "English" or "German") are embedded in the file and identify the stream.</span></span>                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="380ac-140">count</span><span class="sxs-lookup"><span data-stu-id="380ac-140">count</span></span>                               | <span data-ttu-id="380ac-141">傳回指定類型的選項數目。</span><span class="sxs-lookup"><span data-stu-id="380ac-141">Returns the number of options of the specified type.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="380ac-142">數位 *索引*</span><span class="sxs-lookup"><span data-stu-id="380ac-142">number *index*</span></span>                      | <span data-ttu-id="380ac-143">傳回字串，描述指定選項類型的 *索引*) 所識別的特定選項 (。</span><span class="sxs-lookup"><span data-stu-id="380ac-143">Returns a string describing a specific option (as identified by *index*) of the specified option type.</span></span> <span data-ttu-id="380ac-144">*索引* 必須是介於1和 "count" 傳回值之間的整數。</span><span class="sxs-lookup"><span data-stu-id="380ac-144">*Index* must be an integer between 1 and the value returned by "count".</span></span>                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="380ac-145">仍為演算法</span><span class="sxs-lookup"><span data-stu-id="380ac-145">still algorithm</span></span>                     | <span data-ttu-id="380ac-146">指定命令應該取出仍為演算法的名稱。</span><span class="sxs-lookup"><span data-stu-id="380ac-146">Specifies the command should retrieve still algorithm names.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="380ac-147">仍是品質演算法 *演算法*</span><span class="sxs-lookup"><span data-stu-id="380ac-147">still quality algorithm *algorithm*</span></span> | <span data-ttu-id="380ac-148">指定命令應該會取得與指定的仍 *演算法* 相關聯的品質等級。</span><span class="sxs-lookup"><span data-stu-id="380ac-148">Specifies the command should retrieve quality levels associated with the specified still *algorithm*.</span></span> <span data-ttu-id="380ac-149">如果 *演算法* 為「目前」，則會傳回目前演算法的品質等級。</span><span class="sxs-lookup"><span data-stu-id="380ac-149">If *algorithm* is "current", the quality level of the current algorithm is returned.</span></span>                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="380ac-150">影片演算法</span><span class="sxs-lookup"><span data-stu-id="380ac-150">video algorithm</span></span>                     | <span data-ttu-id="380ac-151">指定命令應該取出影片演算法名稱。</span><span class="sxs-lookup"><span data-stu-id="380ac-151">Specifies the command should retrieve video algorithm names.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="380ac-152">影片品質演算法 *演算法*</span><span class="sxs-lookup"><span data-stu-id="380ac-152">video quality algorithm *algorithm*</span></span> | <span data-ttu-id="380ac-153">指定命令應該會取得與指定的影片 *演算法* 相關聯的品質等級。</span><span class="sxs-lookup"><span data-stu-id="380ac-153">Specifies the command should retrieve quality levels associated with the specified video *algorithm*.</span></span> <span data-ttu-id="380ac-154">如果 *演算法* 為「目前」，則會傳回目前演算法的品質等級。</span><span class="sxs-lookup"><span data-stu-id="380ac-154">If *algorithm* is "current", the quality level of the current algorithm is returned.</span></span>                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="380ac-155">影片來源</span><span class="sxs-lookup"><span data-stu-id="380ac-155">video source</span></span>                        | <span data-ttu-id="380ac-156">指定命令應該會傳回影片來源的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="380ac-156">Specifies the command should return information about the video sources.</span></span> <span data-ttu-id="380ac-157">搭配 "count" 旗標使用時，會傳回影片來源的數目。</span><span class="sxs-lookup"><span data-stu-id="380ac-157">When used with the "count" flag, it returns the number of video sources.</span></span> <span data-ttu-id="380ac-158">搭配 "number" 旗標使用時，它會傳回影片來源的類型。</span><span class="sxs-lookup"><span data-stu-id="380ac-158">When used with the "number" flag, it returns the type of a video source.</span></span> <span data-ttu-id="380ac-159">MCI 會定義下列類型的常數：「ntsc」、「rgb」、「pal」、「secam」、「svideo」和「泛型」。</span><span class="sxs-lookup"><span data-stu-id="380ac-159">MCI defines the following constants for type: "ntsc", "rgb", "pal", "secam", "svideo", and "generic".</span></span> <span data-ttu-id="380ac-160">傳回的每個類型可能會有一個以上的來源。</span><span class="sxs-lookup"><span data-stu-id="380ac-160">There might be more than one source of each type returned.</span></span> <span data-ttu-id="380ac-161">當該連接器允許一個以上的信號時，會使用「泛型」來源類型。</span><span class="sxs-lookup"><span data-stu-id="380ac-161">The "generic" source type is used when more than one signal is allowed for that connector.</span></span> |
| <span data-ttu-id="380ac-162">影片來源計數</span><span class="sxs-lookup"><span data-stu-id="380ac-162">video source count</span></span>                  | <span data-ttu-id="380ac-163">傳回影片輸入總數。</span><span class="sxs-lookup"><span data-stu-id="380ac-163">Returns total number of video inputs.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="380ac-164">影片來源編號 *索引*</span><span class="sxs-lookup"><span data-stu-id="380ac-164">video source number *index*</span></span>         | <span data-ttu-id="380ac-165">傳回來源 *索引* 的影片輸入類型。</span><span class="sxs-lookup"><span data-stu-id="380ac-165">Returns the type of video input of source *index*.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="380ac-166">影片串流</span><span class="sxs-lookup"><span data-stu-id="380ac-166">video stream</span></span>                        | <span data-ttu-id="380ac-167">指定命令應該取得與工作區相關聯的影片資料流程名稱。</span><span class="sxs-lookup"><span data-stu-id="380ac-167">Specifies the command should retrieve the names of video streams associated with the workspace.</span></span> <span data-ttu-id="380ac-168">這些字串 (例如「有趣的結束」或「悲傷結束」 ) 會內嵌在檔案中，並識別該資料流程。</span><span class="sxs-lookup"><span data-stu-id="380ac-168">These strings (such as "funny ending" or "sad ending") are embedded in the file and identify the stream.</span></span>                                                                                                                                                                                                                                                                               |



 

</dd> <dt>

<span data-ttu-id="380ac-169"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="380ac-169"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="380ac-170">可以是「等候」、「通知」或「測試」。</span><span class="sxs-lookup"><span data-stu-id="380ac-170">Can be "wait", "notify", or "test".</span></span> <span data-ttu-id="380ac-171">如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。</span><span class="sxs-lookup"><span data-stu-id="380ac-171">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="380ac-172">傳回值</span><span class="sxs-lookup"><span data-stu-id="380ac-172">Return Value</span></span>

<span data-ttu-id="380ac-173">如果成功則傳回零，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="380ac-173">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="380ac-174">備註</span><span class="sxs-lookup"><span data-stu-id="380ac-174">Remarks</span></span>

<span data-ttu-id="380ac-175">若為 VCR 裝置，您必須使用 "count" 或 "number" 旗標來指定「影片來源」或「音訊來源」。</span><span class="sxs-lookup"><span data-stu-id="380ac-175">For VCR devices, either "video source" or "audio source" must be specified with either the "count" or "number" flags.</span></span> <span data-ttu-id="380ac-176">如果指定了 "count"，則會傳回影片或音訊的輸入總數。</span><span class="sxs-lookup"><span data-stu-id="380ac-176">If "count" is specified, the total number of inputs of video or audio is returned.</span></span> <span data-ttu-id="380ac-177">如果指定了 "number"，驅動程式會傳回對應于輸入的類型。</span><span class="sxs-lookup"><span data-stu-id="380ac-177">If "number" is specified, the driver returns a type corresponding to the input.</span></span> <span data-ttu-id="380ac-178">此類型可以是下列任何一項： "調諧器"、"line"、"svideo"、"aux" 或 "generic"。</span><span class="sxs-lookup"><span data-stu-id="380ac-178">The type can be any one of the following: "tuner", "line", "svideo", "aux", or "generic".</span></span> <span data-ttu-id="380ac-179">通常，您應該先查詢 VCR 的 "count"，然後使用 count 作為 "number" 旗標的範圍。</span><span class="sxs-lookup"><span data-stu-id="380ac-179">Typically, you should first query the VCR for the "count" and then use the count as the range for the "number" flag.</span></span> <span data-ttu-id="380ac-180">「來源」數位從1開始。</span><span class="sxs-lookup"><span data-stu-id="380ac-180">The "source" numbers start from 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="380ac-181">規格需求</span><span class="sxs-lookup"><span data-stu-id="380ac-181">Requirements</span></span>



| <span data-ttu-id="380ac-182">需求</span><span class="sxs-lookup"><span data-stu-id="380ac-182">Requirement</span></span> | <span data-ttu-id="380ac-183">值</span><span class="sxs-lookup"><span data-stu-id="380ac-183">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="380ac-184">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="380ac-184">Minimum supported client</span></span><br/> | <span data-ttu-id="380ac-185">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="380ac-185">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="380ac-186">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="380ac-186">Minimum supported server</span></span><br/> | <span data-ttu-id="380ac-187">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="380ac-187">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="380ac-188">另請參閱</span><span class="sxs-lookup"><span data-stu-id="380ac-188">See also</span></span>

<dl> <dt>

[<span data-ttu-id="380ac-189">Mci</span><span class="sxs-lookup"><span data-stu-id="380ac-189">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="380ac-190">MCI 命令字串</span><span class="sxs-lookup"><span data-stu-id="380ac-190">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 

