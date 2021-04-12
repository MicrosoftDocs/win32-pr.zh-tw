---
title: info 命令
description: Info 命令會從裝置捕獲硬體描述。 所有 MCI 裝置都會辨識此命令。
ms.assetid: cdd6628b-bff8-4a0d-9dad-a63321f584ea
keywords:
- info 命令 Windows 多媒體
topic_type:
- apiref
api_name:
- info
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6d401efca6a59d1ed3cbf433d7c33311678705d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385141"
---
# <a name="info-command"></a><span data-ttu-id="4f078-105">info 命令</span><span class="sxs-lookup"><span data-stu-id="4f078-105">info command</span></span>

<span data-ttu-id="4f078-106">Info 命令會從裝置捕獲硬體描述。</span><span class="sxs-lookup"><span data-stu-id="4f078-106">The info command retrieves a hardware description from a device.</span></span> <span data-ttu-id="4f078-107">所有 MCI 裝置都會辨識此命令。</span><span class="sxs-lookup"><span data-stu-id="4f078-107">All MCI devices recognize this command.</span></span>

<span data-ttu-id="4f078-108">若要傳送此命令，請使用 *lpszCommand* 參數設定來呼叫 [**mciSendString**](/previous-versions//dd757161(v=vs.85))函式，如下所示。</span><span class="sxs-lookup"><span data-stu-id="4f078-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("info %s %s %s"), 
  lpszDeviceID, 
  lpszInfoType, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="4f078-109">參數</span><span class="sxs-lookup"><span data-stu-id="4f078-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f078-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="4f078-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="4f078-111">MCI 裝置的識別碼。</span><span class="sxs-lookup"><span data-stu-id="4f078-111">Identifier of an MCI device.</span></span> <span data-ttu-id="4f078-112">開啟裝置時，會指派此識別碼或別名。</span><span class="sxs-lookup"><span data-stu-id="4f078-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="4f078-113"><span id="lpszInfoType"></span><span id="lpszinfotype"></span><span id="LPSZINFOTYPE"></span>*lpszInfoType*</span><span class="sxs-lookup"><span data-stu-id="4f078-113"><span id="lpszInfoType"></span><span id="lpszinfotype"></span><span id="LPSZINFOTYPE"></span>*lpszInfoType*</span></span>
</dt> <dd>

<span data-ttu-id="4f078-114">識別所需資訊類型的旗標。</span><span class="sxs-lookup"><span data-stu-id="4f078-114">Flag that identifies the type of information required.</span></span> <span data-ttu-id="4f078-115">下表列出可辨識 **info** 命令的裝置類型，以及每種類型所使用的旗標。</span><span class="sxs-lookup"><span data-stu-id="4f078-115">The following table lists device types that recognize the **info** command and the flags used by each type.</span></span>



| <span data-ttu-id="4f078-116">值</span><span class="sxs-lookup"><span data-stu-id="4f078-116">Value</span></span>        | <span data-ttu-id="4f078-117">意義</span><span class="sxs-lookup"><span data-stu-id="4f078-117">Meaning</span></span>                                                             | <span data-ttu-id="4f078-118">意義</span><span class="sxs-lookup"><span data-stu-id="4f078-118">Meaning</span></span>                                             |
|--------------|---------------------------------------------------------------------|-----------------------------------------------------|
| <span data-ttu-id="4f078-119">cdaudio</span><span class="sxs-lookup"><span data-stu-id="4f078-119">cdaudio</span></span>      | <span data-ttu-id="4f078-120">資訊 identityinfo upc</span><span class="sxs-lookup"><span data-stu-id="4f078-120">info identityinfo upc</span></span>                                               | <span data-ttu-id="4f078-121">product</span><span class="sxs-lookup"><span data-stu-id="4f078-121">product</span></span>                                             |
| <span data-ttu-id="4f078-122">digitalvideo</span><span class="sxs-lookup"><span data-stu-id="4f078-122">digitalvideo</span></span> | <span data-ttu-id="4f078-123">音訊 algorithmaudio qualityfileproductstill algorithmstill 品質</span><span class="sxs-lookup"><span data-stu-id="4f078-123">audio algorithmaudio qualityfileproductstill algorithmstill quality</span></span> | <span data-ttu-id="4f078-124">usageversionvideo algorithmvideo qualitywindow text</span><span class="sxs-lookup"><span data-stu-id="4f078-124">usageversionvideo algorithmvideo qualitywindow text</span></span> |
| <span data-ttu-id="4f078-125">overlay</span><span class="sxs-lookup"><span data-stu-id="4f078-125">overlay</span></span>      | <span data-ttu-id="4f078-126">fileproduct</span><span class="sxs-lookup"><span data-stu-id="4f078-126">fileproduct</span></span>                                                         | <span data-ttu-id="4f078-127">視窗文字</span><span class="sxs-lookup"><span data-stu-id="4f078-127">window text</span></span>                                         |
| <span data-ttu-id="4f078-128">排序器</span><span class="sxs-lookup"><span data-stu-id="4f078-128">sequencer</span></span>    | <span data-ttu-id="4f078-129">copyrightfile</span><span class="sxs-lookup"><span data-stu-id="4f078-129">copyrightfile</span></span>                                                       | <span data-ttu-id="4f078-130">nameproduct</span><span class="sxs-lookup"><span data-stu-id="4f078-130">nameproduct</span></span>                                         |
| <span data-ttu-id="4f078-131">錄影機</span><span class="sxs-lookup"><span data-stu-id="4f078-131">vcr</span></span>          | <span data-ttu-id="4f078-132">product</span><span class="sxs-lookup"><span data-stu-id="4f078-132">product</span></span>                                                             | <span data-ttu-id="4f078-133">version</span><span class="sxs-lookup"><span data-stu-id="4f078-133">version</span></span>                                             |
| <span data-ttu-id="4f078-134">videodisk</span><span class="sxs-lookup"><span data-stu-id="4f078-134">videodisk</span></span>    | <span data-ttu-id="4f078-135">product</span><span class="sxs-lookup"><span data-stu-id="4f078-135">product</span></span>                                                             |                                                     |
| <span data-ttu-id="4f078-136">waveaudio</span><span class="sxs-lookup"><span data-stu-id="4f078-136">waveaudio</span></span>    | <span data-ttu-id="4f078-137">fileinput</span><span class="sxs-lookup"><span data-stu-id="4f078-137">fileinput</span></span>                                                           | <span data-ttu-id="4f078-138">outputproduct</span><span class="sxs-lookup"><span data-stu-id="4f078-138">outputproduct</span></span>                                       |



 

<span data-ttu-id="4f078-139">下表列出可在 **lpszInfoType** 參數中指定的旗標，以及它們的意義。</span><span class="sxs-lookup"><span data-stu-id="4f078-139">The following table lists the flags that can be specified in the **lpszInfoType** parameter and their meanings.</span></span>



| <span data-ttu-id="4f078-140">值</span><span class="sxs-lookup"><span data-stu-id="4f078-140">Value</span></span>           | <span data-ttu-id="4f078-141">意義</span><span class="sxs-lookup"><span data-stu-id="4f078-141">Meaning</span></span>                                                                                                                                                                                            |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f078-142">音訊演算法</span><span class="sxs-lookup"><span data-stu-id="4f078-142">audio algorithm</span></span> | <span data-ttu-id="4f078-143">傳回目前音訊壓縮演算法的名稱。</span><span class="sxs-lookup"><span data-stu-id="4f078-143">Returns the name of the current audio compression algorithm.</span></span>                                                                                                                                       |
| <span data-ttu-id="4f078-144">音訊品質</span><span class="sxs-lookup"><span data-stu-id="4f078-144">audio quality</span></span>   | <span data-ttu-id="4f078-145">傳回目前音訊品質描述項的名稱。</span><span class="sxs-lookup"><span data-stu-id="4f078-145">Returns the name for the current audio quality descriptor.</span></span> <span data-ttu-id="4f078-146">如果應用程式將參數設定為未對應至已定義品質的特定值，這可能會傳回「未知」。</span><span class="sxs-lookup"><span data-stu-id="4f078-146">This might return "unknown" if the application has set parameters to specific values that do not correspond to defined qualities.</span></span>       |
| <span data-ttu-id="4f078-147">著作權</span><span class="sxs-lookup"><span data-stu-id="4f078-147">copyright</span></span>       | <span data-ttu-id="4f078-148">從著作權中繼事件中抓取 MIDI 檔案的著作權注意事項。</span><span class="sxs-lookup"><span data-stu-id="4f078-148">Retrieves the MIDI file copyright notice from the copyright meta event.</span></span>                                                                                                                            |
| <span data-ttu-id="4f078-149">file</span><span class="sxs-lookup"><span data-stu-id="4f078-149">file</span></span>            | <span data-ttu-id="4f078-150">抓取複合裝置所使用的檔案名。</span><span class="sxs-lookup"><span data-stu-id="4f078-150">Retrieves the name of the file used by the compound device.</span></span> <span data-ttu-id="4f078-151">如果在沒有檔案的情況下開啟裝置，而且未使用 [load](load.md) 命令，則會傳回 null 字串。</span><span class="sxs-lookup"><span data-stu-id="4f078-151">If the device is opened without a file and the [load](load.md) command has not been used, a null string is returned.</span></span>                  |
| <span data-ttu-id="4f078-152">資訊身分識別</span><span class="sxs-lookup"><span data-stu-id="4f078-152">info identity</span></span>   | <span data-ttu-id="4f078-153">針對目前已在正在進行查詢的播放程式中載入的音訊 CD 產生唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="4f078-153">Produces a unique identifier for the audio CD currently loaded in the player being queried.</span></span>                                                                                                        |
| <span data-ttu-id="4f078-154">資訊 upc</span><span class="sxs-lookup"><span data-stu-id="4f078-154">info upc</span></span>        | <span data-ttu-id="4f078-155">產生在音訊 CD 上編碼 (UPC) 的通用產品程式碼。</span><span class="sxs-lookup"><span data-stu-id="4f078-155">Produces the Universal Product Code (UPC) that is encoded on an audio CD.</span></span> <span data-ttu-id="4f078-156">UPC 是數位的字串。</span><span class="sxs-lookup"><span data-stu-id="4f078-156">The UPC is a string of digits.</span></span> <span data-ttu-id="4f078-157">它可能不適用於所有 Cd。</span><span class="sxs-lookup"><span data-stu-id="4f078-157">It might not be available for all CDs.</span></span>                                                    |
| <span data-ttu-id="4f078-158">input</span><span class="sxs-lookup"><span data-stu-id="4f078-158">input</span></span>           | <span data-ttu-id="4f078-159">抓取目前輸入裝置的描述。</span><span class="sxs-lookup"><span data-stu-id="4f078-159">Retrieves the description of the current input device.</span></span> <span data-ttu-id="4f078-160">如果未設定輸入裝置，則會傳回「無」。</span><span class="sxs-lookup"><span data-stu-id="4f078-160">Returns "none" if an input device is not set.</span></span>                                                                                               |
| <span data-ttu-id="4f078-161">NAME</span><span class="sxs-lookup"><span data-stu-id="4f078-161">name</span></span>            | <span data-ttu-id="4f078-162">從 sequence/track name 中繼事件中抓取序列名稱。</span><span class="sxs-lookup"><span data-stu-id="4f078-162">Retrieves the sequence name from the sequence/track name meta event.</span></span>                                                                                                                               |
| <span data-ttu-id="4f078-163">output</span><span class="sxs-lookup"><span data-stu-id="4f078-163">output</span></span>          | <span data-ttu-id="4f078-164">抓取目前輸出裝置的描述。</span><span class="sxs-lookup"><span data-stu-id="4f078-164">Retrieves the description of the current output device.</span></span> <span data-ttu-id="4f078-165">如果未設定輸出裝置，則會傳回「無」。</span><span class="sxs-lookup"><span data-stu-id="4f078-165">Returns "none" if an output device is not set.</span></span>                                                                                             |
| <span data-ttu-id="4f078-166">product</span><span class="sxs-lookup"><span data-stu-id="4f078-166">product</span></span>         | <span data-ttu-id="4f078-167">抓取裝置的描述。</span><span class="sxs-lookup"><span data-stu-id="4f078-167">Retrieves a description of the device.</span></span> <span data-ttu-id="4f078-168">這種資訊通常包含產品名稱和型號。</span><span class="sxs-lookup"><span data-stu-id="4f078-168">This information often includes the product name and model.</span></span> <span data-ttu-id="4f078-169">字串長度將是31個字元或更少。</span><span class="sxs-lookup"><span data-stu-id="4f078-169">The string length will be 31 characters or fewer.</span></span>                                               |
| <span data-ttu-id="4f078-170">仍為演算法</span><span class="sxs-lookup"><span data-stu-id="4f078-170">still algorithm</span></span> | <span data-ttu-id="4f078-171">傳回目前靜止影像壓縮演算法的名稱。</span><span class="sxs-lookup"><span data-stu-id="4f078-171">Returns the name of the current still image compression algorithm.</span></span>                                                                                                                                 |
| <span data-ttu-id="4f078-172">仍為品質</span><span class="sxs-lookup"><span data-stu-id="4f078-172">still quality</span></span>   | <span data-ttu-id="4f078-173">傳回目前靜止影像品質描述項的名稱。</span><span class="sxs-lookup"><span data-stu-id="4f078-173">Returns the name for the current still image quality descriptor.</span></span> <span data-ttu-id="4f078-174">如果應用程式將參數設定為未對應至已定義品質的特定值，這可能會傳回「未知」。</span><span class="sxs-lookup"><span data-stu-id="4f078-174">This might return "unknown" if the application has set parameters to specific values that do not correspond to defined qualities.</span></span> |
| <span data-ttu-id="4f078-175">usage</span><span class="sxs-lookup"><span data-stu-id="4f078-175">usage</span></span>           | <span data-ttu-id="4f078-176">傳回字串，這個字串描述工作區中視覺效果或音訊資料的擁有者可能會加諸的使用限制。</span><span class="sxs-lookup"><span data-stu-id="4f078-176">Returns a string describing usage restrictions that might be imposed by the owner of the visual or audio data in the workspace.</span></span>                                                                    |
| <span data-ttu-id="4f078-177">version</span><span class="sxs-lookup"><span data-stu-id="4f078-177">version</span></span>         | <span data-ttu-id="4f078-178">傳回設備磁碟機和硬體的版本層級。</span><span class="sxs-lookup"><span data-stu-id="4f078-178">Returns the release level of the device driver and hardware.</span></span>                                                                                                                                       |
| <span data-ttu-id="4f078-179">影片演算法</span><span class="sxs-lookup"><span data-stu-id="4f078-179">video algorithm</span></span> | <span data-ttu-id="4f078-180">傳回目前視訊壓縮演算法的名稱。</span><span class="sxs-lookup"><span data-stu-id="4f078-180">Returns the name of the current video compression algorithm.</span></span>                                                                                                                                       |
| <span data-ttu-id="4f078-181">影片品質</span><span class="sxs-lookup"><span data-stu-id="4f078-181">video quality</span></span>   | <span data-ttu-id="4f078-182">傳回目前影片品質描述項的名稱。</span><span class="sxs-lookup"><span data-stu-id="4f078-182">Returns the name for the current video quality descriptor.</span></span> <span data-ttu-id="4f078-183">如果應用程式將參數設定為未對應至已定義品質的特定值，這可能會傳回「未知」。</span><span class="sxs-lookup"><span data-stu-id="4f078-183">This might return "unknown" if the application has set parameters to specific values that do not correspond to defined qualities.</span></span>       |
| <span data-ttu-id="4f078-184">視窗文字</span><span class="sxs-lookup"><span data-stu-id="4f078-184">window text</span></span>     | <span data-ttu-id="4f078-185">抓取裝置使用的視窗標題。</span><span class="sxs-lookup"><span data-stu-id="4f078-185">Retrieves the caption of the window used by the device.</span></span>                                                                                                                                            |



 

</dd> <dt>

<span data-ttu-id="4f078-186"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="4f078-186"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="4f078-187">可以是「等候」、「通知」或兩者。</span><span class="sxs-lookup"><span data-stu-id="4f078-187">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="4f078-188">針對數位影片和 VCR 裝置，也可以指定「測試」。</span><span class="sxs-lookup"><span data-stu-id="4f078-188">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="4f078-189">如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。</span><span class="sxs-lookup"><span data-stu-id="4f078-189">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f078-190">傳回值</span><span class="sxs-lookup"><span data-stu-id="4f078-190">Return Value</span></span>

<span data-ttu-id="4f078-191">如果成功則傳回零，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="4f078-191">Returns zero if successful or an error otherwise.</span></span>

## <a name="examples"></a><span data-ttu-id="4f078-192">範例</span><span class="sxs-lookup"><span data-stu-id="4f078-192">Examples</span></span>

<span data-ttu-id="4f078-193">下列命令會抓取與 "mysound" 裝置相關聯的硬體描述。</span><span class="sxs-lookup"><span data-stu-id="4f078-193">The following command retrieves a description of the hardware associated with the "mysound" device.</span></span>

``` syntax
info mysound product
```

## <a name="requirements"></a><span data-ttu-id="4f078-194">規格需求</span><span class="sxs-lookup"><span data-stu-id="4f078-194">Requirements</span></span>



| <span data-ttu-id="4f078-195">需求</span><span class="sxs-lookup"><span data-stu-id="4f078-195">Requirement</span></span> | <span data-ttu-id="4f078-196">值</span><span class="sxs-lookup"><span data-stu-id="4f078-196">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="4f078-197">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4f078-197">Minimum supported client</span></span><br/> | <span data-ttu-id="4f078-198">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4f078-198">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="4f078-199">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4f078-199">Minimum supported server</span></span><br/> | <span data-ttu-id="4f078-200">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4f078-200">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="4f078-201">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4f078-201">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f078-202">Mci</span><span class="sxs-lookup"><span data-stu-id="4f078-202">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="4f078-203">MCI 命令字串</span><span class="sxs-lookup"><span data-stu-id="4f078-203">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="4f078-204">載入</span><span class="sxs-lookup"><span data-stu-id="4f078-204">load</span></span>](load.md)
</dt> </dl>

 

