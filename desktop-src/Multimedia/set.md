---
title: set 命令
description: Set 命令會建立裝置的控制項設定。 CD 音訊、數位影片、MIDI sequencer、VCR、videodisc、影片重迭和波形音訊裝置都會辨識此命令。
ms.assetid: 1ec4d84e-372a-4b6d-b694-f5afb41f90b2
keywords:
- 設定命令 Windows 多媒體
topic_type:
- apiref
api_name:
- set
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 914743db038b0cae32b53fa79b7696ddba1ad05b
ms.sourcegitcommit: 8276af9231bdbf5a7334299f0d13fc8ff069a065
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/12/2021
ms.locfileid: "107000204"
---
# <a name="set-command"></a><span data-ttu-id="3b76b-105">set 命令</span><span class="sxs-lookup"><span data-stu-id="3b76b-105">set command</span></span>

> [!NOTE]
> <span data-ttu-id="3b76b-106">無偏差的通訊-Microsoft 支援多樣化且 inclusionary 的環境。</span><span class="sxs-lookup"><span data-stu-id="3b76b-106">Bias-free Communication Microsoft supports a diverse and inclusionary environment.</span></span>  <span data-ttu-id="3b76b-107">本檔中有 ' 從屬 ' 這個字的參考。</span><span class="sxs-lookup"><span data-stu-id="3b76b-107">Within this document, there are references to the word 'slave.'</span></span> <span data-ttu-id="3b76b-108">Microsoft 的 [Bias-Free 通訊樣式指南](https://github.com/MicrosoftDocs/microsoft-style-guide/blob/master/styleguide/bias-free-communication.md) 會將此視為排他性行為單字。</span><span class="sxs-lookup"><span data-stu-id="3b76b-108">Microsoft's [Style Guide for Bias-Free Communications](https://github.com/MicrosoftDocs/microsoft-style-guide/blob/master/styleguide/bias-free-communication.md) recognizes this as an exclusionary word.</span></span>  <span data-ttu-id="3b76b-109">這種用語是用來做為命令內所使用的用語。</span><span class="sxs-lookup"><span data-stu-id="3b76b-109">This wording is used as it is currently the wording used within the commands.</span></span> <span data-ttu-id="3b76b-110">為求一致，本檔包含此字。</span><span class="sxs-lookup"><span data-stu-id="3b76b-110">For consistency, this document contains this word.</span></span> <span data-ttu-id="3b76b-111">當您在命令中更改這個字時，我們會將此檔修正為一致。</span><span class="sxs-lookup"><span data-stu-id="3b76b-111">When this word is altered in the commands, we will correct this document to be in alignment.</span></span>


<span data-ttu-id="3b76b-112">Set 命令會建立裝置的控制項設定。</span><span class="sxs-lookup"><span data-stu-id="3b76b-112">The set command establishes control settings for the device.</span></span> <span data-ttu-id="3b76b-113">CD 音訊、數位影片、MIDI sequencer、VCR、videodisc、影片重迭和波形音訊裝置都會辨識此命令。</span><span class="sxs-lookup"><span data-stu-id="3b76b-113">CD audio, digital-video, MIDI sequencer, VCR, videodisc, video-overlay, and waveform-audio devices recognize this command.</span></span>

<span data-ttu-id="3b76b-114">若要傳送此命令，請使用 *lpszCommand* 參數設定來呼叫 [**mciSendString**](/previous-versions//dd757161(v=vs.85))函式，如下所示。</span><span class="sxs-lookup"><span data-stu-id="3b76b-114">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand,
  TEXT("set %s %s %s"),
  lpszDeviceID,
  lpszSetting,
  lpszFlags
);
      
```

## <a name="parameters"></a><span data-ttu-id="3b76b-115">參數</span><span class="sxs-lookup"><span data-stu-id="3b76b-115">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b76b-116"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="3b76b-116"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="3b76b-117">MCI 裝置的識別碼。</span><span class="sxs-lookup"><span data-stu-id="3b76b-117">Identifier of an MCI device.</span></span> <span data-ttu-id="3b76b-118">開啟裝置時，會指派此識別碼或別名。</span><span class="sxs-lookup"><span data-stu-id="3b76b-118">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="3b76b-119"><span id="lpszSetting"></span><span id="lpszsetting"></span><span id="LPSZSETTING"></span>*lpszSetting*</span><span class="sxs-lookup"><span data-stu-id="3b76b-119"><span id="lpszSetting"></span><span id="lpszsetting"></span><span id="LPSZSETTING"></span>*lpszSetting*</span></span>
</dt> <dd>

<span data-ttu-id="3b76b-120">用來建立控制項設定的旗標。</span><span class="sxs-lookup"><span data-stu-id="3b76b-120">Flag for establishing control settings.</span></span> <span data-ttu-id="3b76b-121">下表列出可辨識 **set** 命令和每個型別所使用之旗標的裝置類型。</span><span class="sxs-lookup"><span data-stu-id="3b76b-121">The following table lists device types that recognize the **set** command and the flags used by each type.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3b76b-122">裝置類型</span><span class="sxs-lookup"><span data-stu-id="3b76b-122">Device Type</span></span></th>
<th><span data-ttu-id="3b76b-123">命令旗標</span><span class="sxs-lookup"><span data-stu-id="3b76b-123">Command Flags</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3b76b-124">cdaudio</span><span class="sxs-lookup"><span data-stu-id="3b76b-124">cdaudio</span></span></td>
<td><ul>
<li><span data-ttu-id="3b76b-125">全音訊</span><span class="sxs-lookup"><span data-stu-id="3b76b-125">audio all off</span></span></li>
<li><span data-ttu-id="3b76b-126">全部音訊</span><span class="sxs-lookup"><span data-stu-id="3b76b-126">audio all on</span></span></li>
<li><span data-ttu-id="3b76b-127">音訊停止</span><span class="sxs-lookup"><span data-stu-id="3b76b-127">audio left off</span></span></li>
<li><span data-ttu-id="3b76b-128">剩餘的音訊</span><span class="sxs-lookup"><span data-stu-id="3b76b-128">audio left on</span></span></li>
<li><span data-ttu-id="3b76b-129">音訊立即關閉</span><span class="sxs-lookup"><span data-stu-id="3b76b-129">audio right off</span></span></li>
<li><span data-ttu-id="3b76b-130">音訊右邊</span><span class="sxs-lookup"><span data-stu-id="3b76b-130">audio right on</span></span></li>
<li><span data-ttu-id="3b76b-131">門已關閉</span><span class="sxs-lookup"><span data-stu-id="3b76b-131">door closed</span></span></li>
<li><span data-ttu-id="3b76b-132">門開啟</span><span class="sxs-lookup"><span data-stu-id="3b76b-132">door open</span></span></li>
<li><span data-ttu-id="3b76b-133">時間格式毫秒</span><span class="sxs-lookup"><span data-stu-id="3b76b-133">time format milliseconds</span></span></li>
<li><span data-ttu-id="3b76b-134">時間格式 msf</span><span class="sxs-lookup"><span data-stu-id="3b76b-134">time format msf</span></span></li>
<li><span data-ttu-id="3b76b-135">時間格式 tmsf</span><span class="sxs-lookup"><span data-stu-id="3b76b-135">time format tmsf</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3b76b-136">digitalvideo</span><span class="sxs-lookup"><span data-stu-id="3b76b-136">digitalvideo</span></span></td>
<td><ul>
<li><span data-ttu-id="3b76b-137">全音訊</span><span class="sxs-lookup"><span data-stu-id="3b76b-137">audio all off</span></span></li>
<li><span data-ttu-id="3b76b-138">全部音訊</span><span class="sxs-lookup"><span data-stu-id="3b76b-138">audio all on</span></span></li>
<li><span data-ttu-id="3b76b-139">音訊停止</span><span class="sxs-lookup"><span data-stu-id="3b76b-139">audio left off</span></span></li>
<li><span data-ttu-id="3b76b-140">剩餘的音訊</span><span class="sxs-lookup"><span data-stu-id="3b76b-140">audio left on</span></span></li>
<li><span data-ttu-id="3b76b-141">音訊立即關閉</span><span class="sxs-lookup"><span data-stu-id="3b76b-141">audio right off</span></span></li>
<li><span data-ttu-id="3b76b-142">音訊右邊</span><span class="sxs-lookup"><span data-stu-id="3b76b-142">audio right on</span></span></li>
<li><span data-ttu-id="3b76b-143">門已關閉</span><span class="sxs-lookup"><span data-stu-id="3b76b-143">door closed</span></span></li>
<li><span data-ttu-id="3b76b-144">門開啟</span><span class="sxs-lookup"><span data-stu-id="3b76b-144">door open</span></span></li>
<li><span data-ttu-id="3b76b-145">檔案格式 <em>格式</em></span><span class="sxs-lookup"><span data-stu-id="3b76b-145">file format <em>format</em></span></span></li>
<li><span data-ttu-id="3b76b-146">確切搜尋</span><span class="sxs-lookup"><span data-stu-id="3b76b-146">seek exactly on</span></span></li>
<li><span data-ttu-id="3b76b-147">完全搜尋</span><span class="sxs-lookup"><span data-stu-id="3b76b-147">seek exactly off</span></span></li>
<li><span data-ttu-id="3b76b-148">速度 <em>因素</em></span><span class="sxs-lookup"><span data-stu-id="3b76b-148">speed <em>factor</em></span></span></li>
<li><span data-ttu-id="3b76b-149">仍為檔案格式 <em>格式</em></span><span class="sxs-lookup"><span data-stu-id="3b76b-149">still file format <em>format</em></span></span></li>
<li><span data-ttu-id="3b76b-150">時間格式框架</span><span class="sxs-lookup"><span data-stu-id="3b76b-150">time format frames</span></span></li>
<li><span data-ttu-id="3b76b-151">時間格式毫秒</span><span class="sxs-lookup"><span data-stu-id="3b76b-151">time format milliseconds</span></span></li>
<li><span data-ttu-id="3b76b-152">關閉影片</span><span class="sxs-lookup"><span data-stu-id="3b76b-152">video off</span></span></li>
<li><span data-ttu-id="3b76b-153">影片開啟</span><span class="sxs-lookup"><span data-stu-id="3b76b-153">video on</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3b76b-154">overlay</span><span class="sxs-lookup"><span data-stu-id="3b76b-154">overlay</span></span></td>
<td><ul>
<li><span data-ttu-id="3b76b-155">全音訊</span><span class="sxs-lookup"><span data-stu-id="3b76b-155">audio all off</span></span></li>
<li><span data-ttu-id="3b76b-156">全部音訊</span><span class="sxs-lookup"><span data-stu-id="3b76b-156">audio all on</span></span></li>
<li><span data-ttu-id="3b76b-157">音訊停止</span><span class="sxs-lookup"><span data-stu-id="3b76b-157">audio left off</span></span></li>
<li><span data-ttu-id="3b76b-158">剩餘的音訊</span><span class="sxs-lookup"><span data-stu-id="3b76b-158">audio left on</span></span></li>
<li><span data-ttu-id="3b76b-159">音訊立即關閉</span><span class="sxs-lookup"><span data-stu-id="3b76b-159">audio right off</span></span></li>
<li><span data-ttu-id="3b76b-160">音訊右邊</span><span class="sxs-lookup"><span data-stu-id="3b76b-160">audio right on</span></span></li>
<li><span data-ttu-id="3b76b-161">門已關閉</span><span class="sxs-lookup"><span data-stu-id="3b76b-161">door closed</span></span></li>
<li><span data-ttu-id="3b76b-162">門開啟</span><span class="sxs-lookup"><span data-stu-id="3b76b-162">door open</span></span></li>
<li><span data-ttu-id="3b76b-163">關閉影片</span><span class="sxs-lookup"><span data-stu-id="3b76b-163">video off</span></span></li>
<li><span data-ttu-id="3b76b-164">影片開啟</span><span class="sxs-lookup"><span data-stu-id="3b76b-164">video on</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3b76b-165">排序器</span><span class="sxs-lookup"><span data-stu-id="3b76b-165">sequencer</span></span></td>
<td><ul>
<li><span data-ttu-id="3b76b-166">全音訊</span><span class="sxs-lookup"><span data-stu-id="3b76b-166">audio all off</span></span></li>
<li><span data-ttu-id="3b76b-167">全部音訊</span><span class="sxs-lookup"><span data-stu-id="3b76b-167">audio all on</span></span></li>
<li><span data-ttu-id="3b76b-168">音訊停止</span><span class="sxs-lookup"><span data-stu-id="3b76b-168">audio left off</span></span></li>
<li><span data-ttu-id="3b76b-169">剩餘的音訊</span><span class="sxs-lookup"><span data-stu-id="3b76b-169">audio left on</span></span></li>
<li><span data-ttu-id="3b76b-170">音訊立即關閉</span><span class="sxs-lookup"><span data-stu-id="3b76b-170">audio right off</span></span></li>
<li><span data-ttu-id="3b76b-171">音訊右邊</span><span class="sxs-lookup"><span data-stu-id="3b76b-171">audio right on</span></span></li>
<li><span data-ttu-id="3b76b-172">門已關閉</span><span class="sxs-lookup"><span data-stu-id="3b76b-172">door closed</span></span></li>
<li><span data-ttu-id="3b76b-173">門開啟</span><span class="sxs-lookup"><span data-stu-id="3b76b-173">door open</span></span></li>
<li><span data-ttu-id="3b76b-174">主要 MIDI</span><span class="sxs-lookup"><span data-stu-id="3b76b-174">master MIDI</span></span></li>
<li><span data-ttu-id="3b76b-175">master 無</span><span class="sxs-lookup"><span data-stu-id="3b76b-175">master none</span></span></li>
<li><span data-ttu-id="3b76b-176">master SMPTE</span><span class="sxs-lookup"><span data-stu-id="3b76b-176">master SMPTE</span></span></li>
<li><span data-ttu-id="3b76b-177">位移 <em>時間</em></span><span class="sxs-lookup"><span data-stu-id="3b76b-177">offset <em>time</em></span></span></li>
<li><span data-ttu-id="3b76b-178">埠對應程式</span><span class="sxs-lookup"><span data-stu-id="3b76b-178">port mapper</span></span></li>
<li><span data-ttu-id="3b76b-179">埠無</span><span class="sxs-lookup"><span data-stu-id="3b76b-179">port none</span></span></li>
<li><span data-ttu-id="3b76b-180">埠 <em>port_number</em></span><span class="sxs-lookup"><span data-stu-id="3b76b-180">port <em>port_number</em></span></span></li>
<li><span data-ttu-id="3b76b-181">從屬檔案</span><span class="sxs-lookup"><span data-stu-id="3b76b-181">slave file</span></span></li>
<li><span data-ttu-id="3b76b-182">從屬 MIDI</span><span class="sxs-lookup"><span data-stu-id="3b76b-182">slave MIDI</span></span></li>
<li><span data-ttu-id="3b76b-183">從屬無</span><span class="sxs-lookup"><span data-stu-id="3b76b-183">slave none</span></span></li>
<li><span data-ttu-id="3b76b-184">從屬的 SMPTE</span><span class="sxs-lookup"><span data-stu-id="3b76b-184">slave SMPTE</span></span></li>
<li><span data-ttu-id="3b76b-185">節奏 <em>tempo_value</em></span><span class="sxs-lookup"><span data-stu-id="3b76b-185">tempo <em>tempo_value</em></span></span></li>
<li><span data-ttu-id="3b76b-186">時間格式毫秒</span><span class="sxs-lookup"><span data-stu-id="3b76b-186">time format milliseconds</span></span></li>
<li><span data-ttu-id="3b76b-187">時間格式的 SMPTE <em>fps</em></span><span class="sxs-lookup"><span data-stu-id="3b76b-187">time format SMPTE <em>fps</em></span></span></li>
<li><span data-ttu-id="3b76b-188">時間格式 SMPTE 30 捨棄</span><span class="sxs-lookup"><span data-stu-id="3b76b-188">time format SMPTE 30 drop</span></span></li>
<li><span data-ttu-id="3b76b-189">時間格式歌曲指標</span><span class="sxs-lookup"><span data-stu-id="3b76b-189">time format song pointer</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3b76b-190"><strong>錄影機</strong></span><span class="sxs-lookup"><span data-stu-id="3b76b-190"><strong>vcr</strong></span></span></td>
<td><ul>
<li><span data-ttu-id="3b76b-191">組合記錄</span><span class="sxs-lookup"><span data-stu-id="3b76b-191">assemble record on</span></span></li>
<li><span data-ttu-id="3b76b-192">將記錄組合為關閉</span><span class="sxs-lookup"><span data-stu-id="3b76b-192">assemble record off</span></span></li>
<li><span data-ttu-id="3b76b-193">全音訊</span><span class="sxs-lookup"><span data-stu-id="3b76b-193">audio all off</span></span></li>
<li><span data-ttu-id="3b76b-194">全部音訊</span><span class="sxs-lookup"><span data-stu-id="3b76b-194">audio all on</span></span></li>
<li><span data-ttu-id="3b76b-195">音訊停止</span><span class="sxs-lookup"><span data-stu-id="3b76b-195">audio left off</span></span></li>
<li><span data-ttu-id="3b76b-196">剩餘的音訊</span><span class="sxs-lookup"><span data-stu-id="3b76b-196">audio left on</span></span></li>
<li><span data-ttu-id="3b76b-197">音訊立即關閉</span><span class="sxs-lookup"><span data-stu-id="3b76b-197">audio right off</span></span></li>
<li><span data-ttu-id="3b76b-198">音訊右邊</span><span class="sxs-lookup"><span data-stu-id="3b76b-198">audio right on</span></span></li>
<li><span data-ttu-id="3b76b-199">時鐘 <em>時間</em></span><span class="sxs-lookup"><span data-stu-id="3b76b-199">clock <em>time</em></span></span></li>
<li><span data-ttu-id="3b76b-200">計數器格式</span><span class="sxs-lookup"><span data-stu-id="3b76b-200">counter format</span></span></li>
<li><span data-ttu-id="3b76b-201">計數器 <em>值</em></span><span class="sxs-lookup"><span data-stu-id="3b76b-201">counter <em>value</em></span></span></li>
<li><span data-ttu-id="3b76b-202">門已關閉</span><span class="sxs-lookup"><span data-stu-id="3b76b-202">door closed</span></span></li>
<li><span data-ttu-id="3b76b-203">門開啟</span><span class="sxs-lookup"><span data-stu-id="3b76b-203">door open</span></span></li>
<li><span data-ttu-id="3b76b-204">索引計數器</span><span class="sxs-lookup"><span data-stu-id="3b76b-204">index counter</span></span></li>
<li><span data-ttu-id="3b76b-205">索引日期</span><span class="sxs-lookup"><span data-stu-id="3b76b-205">index date</span></span></li>
<li><span data-ttu-id="3b76b-206">索引時間</span><span class="sxs-lookup"><span data-stu-id="3b76b-206">index time</span></span></li>
<li><span data-ttu-id="3b76b-207">索引時間</span><span class="sxs-lookup"><span data-stu-id="3b76b-207">index time</span></span></li>
<li><span data-ttu-id="3b76b-208">codelength <em>持續期間</em></span><span class="sxs-lookup"><span data-stu-id="3b76b-208">codelength <em>duration</em></span></span></li>
<li><span data-ttu-id="3b76b-209">暫停 <em>timeout</em></span><span class="sxs-lookup"><span data-stu-id="3b76b-209">pause <em>timeout</em></span></span></li>
<li><span data-ttu-id="3b76b-210">postroll 持續期間-</span><span class="sxs-lookup"><span data-stu-id="3b76b-210">postroll duration -</span></span></li>
<li><span data-ttu-id="3b76b-211"><em>duration</em></span><span class="sxs-lookup"><span data-stu-id="3b76b-211"><em>duration</em></span></span></li>
<li><span data-ttu-id="3b76b-212">開啟電源</span><span class="sxs-lookup"><span data-stu-id="3b76b-212">power on</span></span></li>
<li><span data-ttu-id="3b76b-213">關閉電源</span><span class="sxs-lookup"><span data-stu-id="3b76b-213">power off</span></span></li>
<li><span data-ttu-id="3b76b-214">預先進行 <em>持續時間持續時間</em></span><span class="sxs-lookup"><span data-stu-id="3b76b-214">preroll duration <em>duration</em></span></span></li>
<li><span data-ttu-id="3b76b-215">記錄格式 SP</span><span class="sxs-lookup"><span data-stu-id="3b76b-215">record format SP</span></span></li>
<li><span data-ttu-id="3b76b-216">LP 記錄格式</span><span class="sxs-lookup"><span data-stu-id="3b76b-216">record format LP</span></span></li>
<li><span data-ttu-id="3b76b-217">記錄格式 EP</span><span class="sxs-lookup"><span data-stu-id="3b76b-217">record format EP</span></span></li>
<li><span data-ttu-id="3b76b-218">速度 <em>因素</em></span><span class="sxs-lookup"><span data-stu-id="3b76b-218">speed <em>factor</em></span></span></li>
<li><span data-ttu-id="3b76b-219">時間格式框架</span><span class="sxs-lookup"><span data-stu-id="3b76b-219">time format frames</span></span></li>
<li><span data-ttu-id="3b76b-220">時間格式 hms</span><span class="sxs-lookup"><span data-stu-id="3b76b-220">time format hms</span></span></li>
<li><span data-ttu-id="3b76b-221">時間格式毫秒</span><span class="sxs-lookup"><span data-stu-id="3b76b-221">time format milliseconds</span></span></li>
<li><span data-ttu-id="3b76b-222">時間格式 msf</span><span class="sxs-lookup"><span data-stu-id="3b76b-222">time format msf</span></span></li>
<li><span data-ttu-id="3b76b-223">時間格式的 SMPTE <em>fps</em></span><span class="sxs-lookup"><span data-stu-id="3b76b-223">time format SMPTE <em>fps</em></span></span></li>
<li><span data-ttu-id="3b76b-224">時間格式 SMPTE 30 捨棄</span><span class="sxs-lookup"><span data-stu-id="3b76b-224">time format SMPTE 30 drop</span></span></li>
<li><span data-ttu-id="3b76b-225">時間格式 tmsf</span><span class="sxs-lookup"><span data-stu-id="3b76b-225">time format tmsf</span></span></li>
<li><span data-ttu-id="3b76b-226">時間模式計數器</span><span class="sxs-lookup"><span data-stu-id="3b76b-226">time mode counter</span></span></li>
<li><span data-ttu-id="3b76b-227">偵測時間模式</span><span class="sxs-lookup"><span data-stu-id="3b76b-227">time mode detect</span></span></li>
<li><span data-ttu-id="3b76b-228">時間模式時間碼</span><span class="sxs-lookup"><span data-stu-id="3b76b-228">time mode timecode</span></span></li>
<li><span data-ttu-id="3b76b-229">追蹤加號</span><span class="sxs-lookup"><span data-stu-id="3b76b-229">tracking plus</span></span></li>
<li><span data-ttu-id="3b76b-230">追蹤減號</span><span class="sxs-lookup"><span data-stu-id="3b76b-230">tracking minus</span></span></li>
<li><span data-ttu-id="3b76b-231">追蹤重設</span><span class="sxs-lookup"><span data-stu-id="3b76b-231">tracking reset</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3b76b-232">videodisc</span><span class="sxs-lookup"><span data-stu-id="3b76b-232">videodisc</span></span></td>
<td><ul>
<li><span data-ttu-id="3b76b-233">全音訊</span><span class="sxs-lookup"><span data-stu-id="3b76b-233">audio all off</span></span></li>
<li><span data-ttu-id="3b76b-234">全部音訊</span><span class="sxs-lookup"><span data-stu-id="3b76b-234">audio all on</span></span></li>
<li><span data-ttu-id="3b76b-235">音訊停止</span><span class="sxs-lookup"><span data-stu-id="3b76b-235">audio left off</span></span></li>
<li><span data-ttu-id="3b76b-236">剩餘的音訊</span><span class="sxs-lookup"><span data-stu-id="3b76b-236">audio left on</span></span></li>
<li><span data-ttu-id="3b76b-237">音訊立即關閉</span><span class="sxs-lookup"><span data-stu-id="3b76b-237">audio right off</span></span></li>
<li><span data-ttu-id="3b76b-238">音訊右邊</span><span class="sxs-lookup"><span data-stu-id="3b76b-238">audio right on</span></span></li>
<li><span data-ttu-id="3b76b-239">門已關閉</span><span class="sxs-lookup"><span data-stu-id="3b76b-239">door closed</span></span></li>
<li><span data-ttu-id="3b76b-240">門開啟</span><span class="sxs-lookup"><span data-stu-id="3b76b-240">door open</span></span></li>
<li><span data-ttu-id="3b76b-241">時間格式框架</span><span class="sxs-lookup"><span data-stu-id="3b76b-241">time format frames</span></span></li>
<li><span data-ttu-id="3b76b-242">時間格式 hms</span><span class="sxs-lookup"><span data-stu-id="3b76b-242">time format hms</span></span></li>
<li><span data-ttu-id="3b76b-243">時間格式毫秒</span><span class="sxs-lookup"><span data-stu-id="3b76b-243">time format milliseconds</span></span></li>
<li><span data-ttu-id="3b76b-244">時間格式追蹤</span><span class="sxs-lookup"><span data-stu-id="3b76b-244">time format track</span></span></li>
<li><span data-ttu-id="3b76b-245">關閉影片</span><span class="sxs-lookup"><span data-stu-id="3b76b-245">video off</span></span></li>
<li><span data-ttu-id="3b76b-246">影片開啟</span><span class="sxs-lookup"><span data-stu-id="3b76b-246">video on</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3b76b-247">waveaudio</span><span class="sxs-lookup"><span data-stu-id="3b76b-247">waveaudio</span></span></td>
<td><ul>
<li><span data-ttu-id="3b76b-248">對齊 <em>整數</em></span><span class="sxs-lookup"><span data-stu-id="3b76b-248">alignment <em>integer</em></span></span></li>
<li><span data-ttu-id="3b76b-249">任何輸入</span><span class="sxs-lookup"><span data-stu-id="3b76b-249">any input</span></span></li>
<li><span data-ttu-id="3b76b-250">任何輸出</span><span class="sxs-lookup"><span data-stu-id="3b76b-250">any output</span></span></li>
<li><span data-ttu-id="3b76b-251">全音訊</span><span class="sxs-lookup"><span data-stu-id="3b76b-251">audio all off</span></span></li>
<li><span data-ttu-id="3b76b-252">全部音訊</span><span class="sxs-lookup"><span data-stu-id="3b76b-252">audio all on</span></span></li>
<li><span data-ttu-id="3b76b-253">音訊停止</span><span class="sxs-lookup"><span data-stu-id="3b76b-253">audio left off</span></span></li>
<li><span data-ttu-id="3b76b-254">剩餘的音訊</span><span class="sxs-lookup"><span data-stu-id="3b76b-254">audio left on</span></span></li>
<li><span data-ttu-id="3b76b-255">音訊立即關閉</span><span class="sxs-lookup"><span data-stu-id="3b76b-255">audio right off</span></span></li>
<li><span data-ttu-id="3b76b-256">音訊右邊</span><span class="sxs-lookup"><span data-stu-id="3b76b-256">audio right on</span></span></li>
<li><span data-ttu-id="3b76b-257">bitspersample <em>bit_count</em></span><span class="sxs-lookup"><span data-stu-id="3b76b-257">bitspersample <em>bit_count</em></span></span></li>
<li><span data-ttu-id="3b76b-258">bytespersec <em>byte_rate</em></span><span class="sxs-lookup"><span data-stu-id="3b76b-258">bytespersec <em>byte_rate</em></span></span></li>
<li><span data-ttu-id="3b76b-259">通道 <em>channel_count</em></span><span class="sxs-lookup"><span data-stu-id="3b76b-259">channels <em>channel_count</em></span></span></li>
<li><span data-ttu-id="3b76b-260">門已關閉</span><span class="sxs-lookup"><span data-stu-id="3b76b-260">door closed</span></span></li>
<li><span data-ttu-id="3b76b-261">門開啟</span><span class="sxs-lookup"><span data-stu-id="3b76b-261">door open</span></span></li>
<li><span data-ttu-id="3b76b-262">格式化標記 pcm</span><span class="sxs-lookup"><span data-stu-id="3b76b-262">format tag pcm</span></span></li>
<li><span data-ttu-id="3b76b-263">格式化標記 <em>標記</em></span><span class="sxs-lookup"><span data-stu-id="3b76b-263">format tag <em>tag</em></span></span></li>
<li><span data-ttu-id="3b76b-264">輸入 <em>整數</em></span><span class="sxs-lookup"><span data-stu-id="3b76b-264">input <em>integer</em></span></span></li>
<li><span data-ttu-id="3b76b-265">輸出 <em>整數</em></span><span class="sxs-lookup"><span data-stu-id="3b76b-265">output <em>integer</em></span></span></li>
<li><span data-ttu-id="3b76b-266">samplespersec <em>整數</em></span><span class="sxs-lookup"><span data-stu-id="3b76b-266">samplespersec <em>integer</em></span></span></li>
<li><span data-ttu-id="3b76b-267">時間格式位元組</span><span class="sxs-lookup"><span data-stu-id="3b76b-267">time format bytes</span></span></li>
<li><span data-ttu-id="3b76b-268">時間格式毫秒</span><span class="sxs-lookup"><span data-stu-id="3b76b-268">time format milliseconds</span></span></li>
<li><span data-ttu-id="3b76b-269">時間格式範例</span><span class="sxs-lookup"><span data-stu-id="3b76b-269">time format samples</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="3b76b-270">下表列出可在 **lpszSetting** 參數中指定的旗標，以及它們的意義。</span><span class="sxs-lookup"><span data-stu-id="3b76b-270">The following table lists the flags that can be specified in the **lpszSetting** parameter and their meanings.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3b76b-271">值</span><span class="sxs-lookup"><span data-stu-id="3b76b-271">Value</span></span></th>
<th><span data-ttu-id="3b76b-272">意義</span><span class="sxs-lookup"><span data-stu-id="3b76b-272">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3b76b-273">對齊 <em>整數</em></span><span class="sxs-lookup"><span data-stu-id="3b76b-273">alignment <em>integer</em></span></span></td>
<td><span data-ttu-id="3b76b-274">設定資料區塊相對於傳遞到波形-音訊裝置的開頭的對齊方式。</span><span class="sxs-lookup"><span data-stu-id="3b76b-274">Sets the alignment of data blocks relative to the start of data passed to the waveform-audio device.</span></span> <span data-ttu-id="3b76b-275">檔案會以這種格式儲存。</span><span class="sxs-lookup"><span data-stu-id="3b76b-275">The file is saved in this format.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3b76b-276">任何輸入</span><span class="sxs-lookup"><span data-stu-id="3b76b-276">any input</span></span></td>
<td><span data-ttu-id="3b76b-277">錄製時，請使用支援目前格式的任何輸入。</span><span class="sxs-lookup"><span data-stu-id="3b76b-277">Use any input that supports the current format when recording.</span></span> <span data-ttu-id="3b76b-278">這是預設值。</span><span class="sxs-lookup"><span data-stu-id="3b76b-278">This is the default setting.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3b76b-279">任何輸出</span><span class="sxs-lookup"><span data-stu-id="3b76b-279">any output</span></span></td>
<td><span data-ttu-id="3b76b-280">在播放時，請使用任何支援目前格式的輸出。</span><span class="sxs-lookup"><span data-stu-id="3b76b-280">Use any output that supports the current format when playing.</span></span> <span data-ttu-id="3b76b-281">此為預設值。</span><span class="sxs-lookup"><span data-stu-id="3b76b-281">This is the default.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3b76b-282">組合記錄</span><span class="sxs-lookup"><span data-stu-id="3b76b-282">assemble record on</span></span> <br/> <span data-ttu-id="3b76b-283">將記錄組合為關閉</span><span class="sxs-lookup"><span data-stu-id="3b76b-283">assemble record off</span></span> <br/></td>
<td><span data-ttu-id="3b76b-284">在組合模式中，所有的追蹤都會依裝置的定義記錄。</span><span class="sxs-lookup"><span data-stu-id="3b76b-284">In assemble mode, all tracks are recorded as defined by the device.</span></span> <span data-ttu-id="3b76b-285">大部分的 Vcr 預設為組合模式。</span><span class="sxs-lookup"><span data-stu-id="3b76b-285">Most VCRs are in assemble mode by default.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3b76b-286">全音訊</span><span class="sxs-lookup"><span data-stu-id="3b76b-286">audio all off</span></span> <br/> <span data-ttu-id="3b76b-287">全部音訊</span><span class="sxs-lookup"><span data-stu-id="3b76b-287">audio all on</span></span> <br/></td>
<td><span data-ttu-id="3b76b-288">停用或啟用音訊輸出。</span><span class="sxs-lookup"><span data-stu-id="3b76b-288">Disables or enables audio output.</span></span> <span data-ttu-id="3b76b-289">影片重迭裝置、MCISEQ sequencer 和 MCIWAVE 波形-音訊裝置不支援此旗標。</span><span class="sxs-lookup"><span data-stu-id="3b76b-289">Video-overlay devices, the MCISEQ sequencer, and the MCIWAVE waveform-audio device do not support this flag.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3b76b-290">音訊停止</span><span class="sxs-lookup"><span data-stu-id="3b76b-290">audio left off</span></span> <br/> <span data-ttu-id="3b76b-291">剩餘的音訊</span><span class="sxs-lookup"><span data-stu-id="3b76b-291">audio left on</span></span> <br/> <span data-ttu-id="3b76b-292">音訊立即關閉</span><span class="sxs-lookup"><span data-stu-id="3b76b-292">audio right off</span></span> <br/> <span data-ttu-id="3b76b-293">音訊右邊</span><span class="sxs-lookup"><span data-stu-id="3b76b-293">audio right on</span></span> <br/></td>
<td><span data-ttu-id="3b76b-294">停用或啟用向左或向右音訊頻道的輸出。</span><span class="sxs-lookup"><span data-stu-id="3b76b-294">Disables or enables output to either the left or the right audio channel.</span></span> <span data-ttu-id="3b76b-295">影片重迭裝置、MCISEQ sequencer 和 MCIWAVE 波形-音訊裝置不支援此旗標。</span><span class="sxs-lookup"><span data-stu-id="3b76b-295">Video-overlay devices, the MCISEQ sequencer, and the MCIWAVE waveform-audio device do not support this flag.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3b76b-296">bitspersample <em>bit_count</em></span><span class="sxs-lookup"><span data-stu-id="3b76b-296">bitspersample <em>bit_count</em></span></span></td>
<td><span data-ttu-id="3b76b-297">設定每個 PCM (脈衝程式碼調製) 範例播放或錄製的位數。</span><span class="sxs-lookup"><span data-stu-id="3b76b-297">Sets the number of bits per PCM (Pulse Code Modulation) sample played or recorded.</span></span> <span data-ttu-id="3b76b-298">檔案會以這種格式儲存。</span><span class="sxs-lookup"><span data-stu-id="3b76b-298">The file is saved in this format.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3b76b-299">bytespersec <em>byte_rate</em></span><span class="sxs-lookup"><span data-stu-id="3b76b-299">bytespersec <em>byte_rate</em></span></span></td>
<td><span data-ttu-id="3b76b-300">設定每秒播放或記錄的平均位元組數。</span><span class="sxs-lookup"><span data-stu-id="3b76b-300">Sets the average number of bytes per second played or recorded.</span></span> <span data-ttu-id="3b76b-301">檔案會以這種格式儲存。</span><span class="sxs-lookup"><span data-stu-id="3b76b-301">The file is saved in this format.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3b76b-302">通道 <em>channel_count</em></span><span class="sxs-lookup"><span data-stu-id="3b76b-302">channels <em>channel_count</em></span></span></td>
<td><span data-ttu-id="3b76b-303">設定播放和錄製的通道。</span><span class="sxs-lookup"><span data-stu-id="3b76b-303">Sets the channels for playing and recording.</span></span> <span data-ttu-id="3b76b-304">檔案會以這種格式儲存。</span><span class="sxs-lookup"><span data-stu-id="3b76b-304">The file is saved in this format.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3b76b-305">時鐘 <em>時間</em></span><span class="sxs-lookup"><span data-stu-id="3b76b-305">clock <em>time</em></span></span></td>
<td><span data-ttu-id="3b76b-306">將外部時鐘的時間設定為 <em>時間。</em></span><span class="sxs-lookup"><span data-stu-id="3b76b-306">Sets time on the external clock to <em>time.</em></span></span> <span data-ttu-id="3b76b-307">格式會指定為長帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="3b76b-307">The format is specified as a long unsigned integer.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3b76b-308">計數器格式</span><span class="sxs-lookup"><span data-stu-id="3b76b-308">counter format</span></span></td>
<td><span data-ttu-id="3b76b-309">設定計數器的時間格式，如 status 計數器所傳回<a href="status.md"></a> &quot; &quot; 。</span><span class="sxs-lookup"><span data-stu-id="3b76b-309">Set the time format for the counter, as returned by <a href="status.md">status</a> &quot;counter&quot;.</span></span> <span data-ttu-id="3b76b-310">如需適用類型的詳細資訊，請參閱 <strong>設定</strong> &quot; 時間格式 &quot; 命令。</span><span class="sxs-lookup"><span data-stu-id="3b76b-310">For information about applicable types, see the <strong>set</strong> &quot;time format&quot; command.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3b76b-311">計數器 <em>值</em></span><span class="sxs-lookup"><span data-stu-id="3b76b-311">counter <em>value</em></span></span></td>
<td><span data-ttu-id="3b76b-312">將 VCR 計數器設定為指定的值。</span><span class="sxs-lookup"><span data-stu-id="3b76b-312">Sets the VCR counter to the specified value.</span></span> <span data-ttu-id="3b76b-313">您必須在目前的計數器格式中指定此值。</span><span class="sxs-lookup"><span data-stu-id="3b76b-313">The value must be specified in the current counter format.</span></span> <span data-ttu-id="3b76b-314">如需詳細資訊，請參閱 <strong>設定</strong> &quot; 計數器格式 &quot; 命令。</span><span class="sxs-lookup"><span data-stu-id="3b76b-314">For more information, see the <strong>set</strong> &quot;counter format&quot; command.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3b76b-315">門已關閉</span><span class="sxs-lookup"><span data-stu-id="3b76b-315">door closed</span></span></td>
<td><span data-ttu-id="3b76b-316">在可能的情況下，收回紙匣並關閉門。</span><span class="sxs-lookup"><span data-stu-id="3b76b-316">Retracts the tray and closes the door, if possible.</span></span> <span data-ttu-id="3b76b-317">若為 Vcr，則會自動載入磁帶。</span><span class="sxs-lookup"><span data-stu-id="3b76b-317">For VCRs, loads the tape automatically.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3b76b-318">門開啟</span><span class="sxs-lookup"><span data-stu-id="3b76b-318">door open</span></span></td>
<td><span data-ttu-id="3b76b-319">開啟門並取出紙匣或磁帶（可能的話）。</span><span class="sxs-lookup"><span data-stu-id="3b76b-319">Opens the door and ejects the tray or tape, if possible.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3b76b-320">檔案格式 <em>格式</em></span><span class="sxs-lookup"><span data-stu-id="3b76b-320">file format <em>format</em></span></span></td>
<td><span data-ttu-id="3b76b-321">指定用於 <a href="save.md">儲存</a> 或 <a href="capture.md">捕捉</a> 命令的檔案格式。</span><span class="sxs-lookup"><span data-stu-id="3b76b-321">Specifies a file format that is used for <a href="save.md">save</a> or <a href="capture.md">capture</a> commands.</span></span> <span data-ttu-id="3b76b-322">如果省略此參數，則可能會預設為設備磁碟機定義的格式。</span><span class="sxs-lookup"><span data-stu-id="3b76b-322">If omitted, this might default to a device driver defined format.</span></span> <span data-ttu-id="3b76b-323">如果指定的檔案格式與目前選取的演算法和品質相衝突，則會將它們變更為檔案格式的預設值。</span><span class="sxs-lookup"><span data-stu-id="3b76b-323">If the specified file format conflicts with the currently selected algorithm and quality, then they are changed to the defaults for the file format.</span></span> <span data-ttu-id="3b76b-324">以下是定義的檔案格式：</span><span class="sxs-lookup"><span data-stu-id="3b76b-324">The following file formats are defined:</span></span>
<ul>
<li><span data-ttu-id="3b76b-325">avi：指定 AVI 格式。</span><span class="sxs-lookup"><span data-stu-id="3b76b-325">avi: Specifies AVI format.</span></span></li>
<li><span data-ttu-id="3b76b-326">avss：指定 AVSS 格式。</span><span class="sxs-lookup"><span data-stu-id="3b76b-326">avss: Specifies AVSS format.</span></span></li>
<li><span data-ttu-id="3b76b-327">dib：指定 DIB 格式。</span><span class="sxs-lookup"><span data-stu-id="3b76b-327">dib: Specifies DIB format.</span></span></li>
<li><span data-ttu-id="3b76b-328">jfif：指定 JFIF 格式。</span><span class="sxs-lookup"><span data-stu-id="3b76b-328">jfif: Specifies JFIF format.</span></span></li>
<li><span data-ttu-id="3b76b-329">jpeg：指定 JPEG 格式。</span><span class="sxs-lookup"><span data-stu-id="3b76b-329">jpeg: Specifies JPEG format.</span></span></li>
<li><span data-ttu-id="3b76b-330">mpeg：指定 MPEG 格式。</span><span class="sxs-lookup"><span data-stu-id="3b76b-330">mpeg: Specifies MPEG format.</span></span></li>
<li><span data-ttu-id="3b76b-331">rdib：指定 RLE DIB 格式。</span><span class="sxs-lookup"><span data-stu-id="3b76b-331">rdib: Specifies RLE DIB format.</span></span></li>
<li><span data-ttu-id="3b76b-332">rjpeg：指定 RJPEG 格式。</span><span class="sxs-lookup"><span data-stu-id="3b76b-332">rjpeg: Specifies RJPEG format.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3b76b-333">格式化標記 pcm</span><span class="sxs-lookup"><span data-stu-id="3b76b-333">format tag pcm</span></span></td>
<td><span data-ttu-id="3b76b-334">將格式類型設定為 PCM 以進行播放和錄製。</span><span class="sxs-lookup"><span data-stu-id="3b76b-334">Sets the format type to PCM for playing and recording.</span></span> <span data-ttu-id="3b76b-335">檔案會以這種格式儲存。</span><span class="sxs-lookup"><span data-stu-id="3b76b-335">The file is saved in this format.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3b76b-336">格式化標記 <em>標記</em></span><span class="sxs-lookup"><span data-stu-id="3b76b-336">format tag <em>tag</em></span></span></td>
<td><span data-ttu-id="3b76b-337">設定播放和錄製的格式類型。</span><span class="sxs-lookup"><span data-stu-id="3b76b-337">Sets the format type for playing and recording.</span></span> <span data-ttu-id="3b76b-338">檔案會以這種格式儲存。</span><span class="sxs-lookup"><span data-stu-id="3b76b-338">The file is saved in this format.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3b76b-339">索引時間碼</span><span class="sxs-lookup"><span data-stu-id="3b76b-339">index timecode</span></span> <br/> <span data-ttu-id="3b76b-340">索引計數器</span><span class="sxs-lookup"><span data-stu-id="3b76b-340">index counter</span></span> <br/> <span data-ttu-id="3b76b-341">索引日期</span><span class="sxs-lookup"><span data-stu-id="3b76b-341">index date</span></span> <br/> <span data-ttu-id="3b76b-342">索引時間</span><span class="sxs-lookup"><span data-stu-id="3b76b-342">index time</span></span> <br/></td>
<td><span data-ttu-id="3b76b-343">設定 VCR 的目前顯示畫面。</span><span class="sxs-lookup"><span data-stu-id="3b76b-343">Sets the current display screen on the VCR.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3b76b-344">輸入 <em>整數</em></span><span class="sxs-lookup"><span data-stu-id="3b76b-344">input <em>integer</em></span></span></td>
<td><span data-ttu-id="3b76b-345">設定用來做為輸入的音訊通道。</span><span class="sxs-lookup"><span data-stu-id="3b76b-345">Sets the audio channel used as the input.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3b76b-346">長度 <em>持續時間</em></span><span class="sxs-lookup"><span data-stu-id="3b76b-346">length <em>duration</em></span></span></td>
<td><span data-ttu-id="3b76b-347">在 VCR 中設定磁帶的使用者指定長度。</span><span class="sxs-lookup"><span data-stu-id="3b76b-347">Sets the user-specified length of the tape in the VCR.</span></span> <span data-ttu-id="3b76b-348">此長度是由 <a href="status.md">status</a> &quot; length 命令所傳回 &quot; ，而且是為了與需要這個命令以傳回有效長度的應用程式相容而提供。</span><span class="sxs-lookup"><span data-stu-id="3b76b-348">This length is returned by the <a href="status.md">status</a> &quot;length&quot; command and is provided for compatibility with applications that require this command to return a valid length.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3b76b-349">主要 midi</span><span class="sxs-lookup"><span data-stu-id="3b76b-349">master midi</span></span></td>
<td><span data-ttu-id="3b76b-350">將 MIDI sequencer 設定為同步處理來源。</span><span class="sxs-lookup"><span data-stu-id="3b76b-350">Sets the MIDI sequencer as the synchronization source.</span></span> <span data-ttu-id="3b76b-351">同步處理資料會以 MIDI 格式傳送。</span><span class="sxs-lookup"><span data-stu-id="3b76b-351">Synchronization data is sent in MIDI format.</span></span> <span data-ttu-id="3b76b-352">MCISEQ sequencer 不支援此旗標。</span><span class="sxs-lookup"><span data-stu-id="3b76b-352">The MCISEQ sequencer does not support this flag.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3b76b-353">master 無</span><span class="sxs-lookup"><span data-stu-id="3b76b-353">master none</span></span></td>
<td><span data-ttu-id="3b76b-354">禁止 MIDI sequencer 傳送同步處理資料。</span><span class="sxs-lookup"><span data-stu-id="3b76b-354">Inhibits the MIDI sequencer from sending synchronization data.</span></span> <span data-ttu-id="3b76b-355">MCISEQ sequencer 不支援此旗標。</span><span class="sxs-lookup"><span data-stu-id="3b76b-355">The MCISEQ sequencer does not support this flag.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3b76b-356">master smpte</span><span class="sxs-lookup"><span data-stu-id="3b76b-356">master smpte</span></span></td>
<td><span data-ttu-id="3b76b-357">將 MIDI sequencer 設定為同步處理來源。</span><span class="sxs-lookup"><span data-stu-id="3b76b-357">Sets the MIDI sequencer as the synchronization source.</span></span> <span data-ttu-id="3b76b-358">同步處理資料會以 SMPTE (社會的運動圖片和電視工程師) 格式傳送。</span><span class="sxs-lookup"><span data-stu-id="3b76b-358">Synchronization data is sent in SMPTE (Society of Motion Picture and Television Engineers) format.</span></span> <span data-ttu-id="3b76b-359">MCISEQ sequencer 不支援此旗標。</span><span class="sxs-lookup"><span data-stu-id="3b76b-359">The MCISEQ sequencer does not support this flag.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3b76b-360">位移 <em>時間</em></span><span class="sxs-lookup"><span data-stu-id="3b76b-360">offset <em>time</em></span></span></td>
<td><span data-ttu-id="3b76b-361">設定 SMPTE 時差 <em>時間</em>。</span><span class="sxs-lookup"><span data-stu-id="3b76b-361">Sets the SMPTE offset <em>time</em>.</span></span> <span data-ttu-id="3b76b-362">位移是以 SMPTE 為基礎之序列的開始時間。</span><span class="sxs-lookup"><span data-stu-id="3b76b-362">The offset is the beginning time of a SMPTE based sequence.</span></span> <span data-ttu-id="3b76b-363"><em>時間</em>會表示為<em>hh</em>： <em>mm</em>： <em>ss</em>： <em>ff</em>，其中<em>hh</em>是小時， <em>mm</em>是分鐘， <em>ss</em>是秒，而<em>ff</em>是畫面格。</span><span class="sxs-lookup"><span data-stu-id="3b76b-363">The <em>time</em> is expressed as <em>hh</em>: <em>mm</em>: <em>ss</em>: <em>ff</em>, where <em>hh</em> is hours, <em>mm</em> is minutes, <em>ss</em> is seconds, and <em>ff</em> is frames.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3b76b-364">輸出 <em>整數</em></span><span class="sxs-lookup"><span data-stu-id="3b76b-364">output <em>integer</em></span></span></td>
<td><span data-ttu-id="3b76b-365">設定用來作為輸出的音訊通道。</span><span class="sxs-lookup"><span data-stu-id="3b76b-365">Sets the audio channel used as the output.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3b76b-366">暫停 <em>timeout</em></span><span class="sxs-lookup"><span data-stu-id="3b76b-366">pause <em>timeout</em></span></span></td>
<td><span data-ttu-id="3b76b-367">設定 <a href="pause.md">pause</a> 命令的最長持續時間（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="3b76b-367">Sets the maximum duration, in milliseconds, of a <a href="pause.md">pause</a> command.</span></span> <span data-ttu-id="3b76b-368"><em>Timeout</em>值為零表示不會進行任何超時。</span><span class="sxs-lookup"><span data-stu-id="3b76b-368">A <em>timeout</em> value of zero indicates that no time-out will occur.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3b76b-369">postroll 持續 <em>期間</em></span><span class="sxs-lookup"><span data-stu-id="3b76b-369">postroll duration <em>duration</em></span></span></td>
<td><span data-ttu-id="3b76b-370">設定在發出 <a href="stop.md">stop</a> 或 <strong>pause</strong> 命令時，煞車 VCR 傳輸所需的長度（以目前的時間格式）。</span><span class="sxs-lookup"><span data-stu-id="3b76b-370">Sets the length, in the current time format, needed to brake the VCR transport when a <a href="stop.md">stop</a> or <strong>pause</strong> command is issued.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3b76b-371">埠對應程式</span><span class="sxs-lookup"><span data-stu-id="3b76b-371">port mapper</span></span></td>
<td><span data-ttu-id="3b76b-372">將 MIDI 對應程式設定為接收 MIDI 訊息的埠。</span><span class="sxs-lookup"><span data-stu-id="3b76b-372">Sets the MIDI mapper as the port receiving the MIDI messages.</span></span> <span data-ttu-id="3b76b-373">如果 MIDI 對應程式或其所需的埠正由另一個應用程式使用中，則此命令會失敗。</span><span class="sxs-lookup"><span data-stu-id="3b76b-373">This command fails if the MIDI mapper or a port it needs is being used by another application.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3b76b-374">埠無</span><span class="sxs-lookup"><span data-stu-id="3b76b-374">port none</span></span></td>
<td><span data-ttu-id="3b76b-375">停用傳送 MIDI 訊息。</span><span class="sxs-lookup"><span data-stu-id="3b76b-375">Disables the sending of MIDI messages.</span></span> <span data-ttu-id="3b76b-376">此命令也會關閉 MIDI 埠。</span><span class="sxs-lookup"><span data-stu-id="3b76b-376">This command also closes a MIDI port.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3b76b-377">埠 <em>port_number</em></span><span class="sxs-lookup"><span data-stu-id="3b76b-377">port <em>port_number</em></span></span></td>
<td><span data-ttu-id="3b76b-378">設定接收 MIDI 訊息的 MIDI 埠。</span><span class="sxs-lookup"><span data-stu-id="3b76b-378">Sets the MIDI port receiving the MIDI messages.</span></span> <span data-ttu-id="3b76b-379">如果您嘗試開啟的埠正由另一個應用程式使用中，則此命令會失敗。</span><span class="sxs-lookup"><span data-stu-id="3b76b-379">This command fails if the port you are trying to open is being used by another application.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3b76b-380">開啟電源</span><span class="sxs-lookup"><span data-stu-id="3b76b-380">power on</span></span> <br/> <span data-ttu-id="3b76b-381">關閉電源</span><span class="sxs-lookup"><span data-stu-id="3b76b-381">power off</span></span> <br/></td>
<td><span data-ttu-id="3b76b-382">將裝置電源設定為開啟或關閉。</span><span class="sxs-lookup"><span data-stu-id="3b76b-382">Sets the device power to on or off.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3b76b-383">預先進行 <em>持續時間持續時間</em></span><span class="sxs-lookup"><span data-stu-id="3b76b-383">preroll duration <em>duration</em></span></span></td>
<td><span data-ttu-id="3b76b-384">設定穩定的 VCR 輸出所需的長度（以目前的時間格式）。</span><span class="sxs-lookup"><span data-stu-id="3b76b-384">Sets the length, in the current time format, needed to stabilize the VCR output.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3b76b-385">記錄格式 SP</span><span class="sxs-lookup"><span data-stu-id="3b76b-385">record format SP</span></span> <br/> <span data-ttu-id="3b76b-386">LP 記錄格式</span><span class="sxs-lookup"><span data-stu-id="3b76b-386">record format LP</span></span> <br/> <span data-ttu-id="3b76b-387">記錄格式 EP</span><span class="sxs-lookup"><span data-stu-id="3b76b-387">record format EP</span></span> <br/></td>
<td><span data-ttu-id="3b76b-388">將 VCR 的錄製模式設定為標準 play 的 SP、EP （延長播放）或適用于長時間播放的 LP。</span><span class="sxs-lookup"><span data-stu-id="3b76b-388">Sets the recording mode for the VCR to SP for standard play, EP for extended play, or LP for long play.</span></span> <span data-ttu-id="3b76b-389">這些值並非 VHS 特定的。</span><span class="sxs-lookup"><span data-stu-id="3b76b-389">These values are not intended to be VHS specific.</span></span> <span data-ttu-id="3b76b-390">它們會對應到具有其他磁帶格式的三種適當模式。</span><span class="sxs-lookup"><span data-stu-id="3b76b-390">They map to any three appropriate modes with other tape formats.</span></span> <span data-ttu-id="3b76b-391">例如，SP 對應到最快、最高品質的記錄。</span><span class="sxs-lookup"><span data-stu-id="3b76b-391">For example, SP maps to the fastest, highest quality recording.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3b76b-392">samplespersec <em>整數</em></span><span class="sxs-lookup"><span data-stu-id="3b76b-392">samplespersec <em>integer</em></span></span></td>
<td><span data-ttu-id="3b76b-393">設定播放和錄製的取樣率。</span><span class="sxs-lookup"><span data-stu-id="3b76b-393">Sets the sample rate for playing and recording.</span></span> <span data-ttu-id="3b76b-394">檔案會以這種格式儲存。</span><span class="sxs-lookup"><span data-stu-id="3b76b-394">The file is saved in this format.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3b76b-395">確切搜尋</span><span class="sxs-lookup"><span data-stu-id="3b76b-395">seek exactly on</span></span><br/> <span data-ttu-id="3b76b-396">完全搜尋</span><span class="sxs-lookup"><span data-stu-id="3b76b-396">seek exactly off</span></span> <br/></td>
<td><span data-ttu-id="3b76b-397">選取兩種搜尋模式的其中一種。</span><span class="sxs-lookup"><span data-stu-id="3b76b-397">Selects one of two seek modes.</span></span> <span data-ttu-id="3b76b-398">&quot;在完全搜尋的情況 &quot; 下，seek 一律會移至指定的框架。</span><span class="sxs-lookup"><span data-stu-id="3b76b-398">With &quot;seek exactly on&quot;, seek will always move to the frame specified.</span></span> <span data-ttu-id="3b76b-399">當 &quot; 完全搜尋時 &quot; ，搜尋會在指定的框架之前移至最接近的主要畫面格。</span><span class="sxs-lookup"><span data-stu-id="3b76b-399">With &quot;seek exactly off&quot;, seek will move to the closest key frame prior to the frame specified.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3b76b-400">從屬檔案</span><span class="sxs-lookup"><span data-stu-id="3b76b-400">slave file</span></span></td>
<td><span data-ttu-id="3b76b-401">將 MIDI sequencer 設定為使用檔案資料作為同步處理來源。</span><span class="sxs-lookup"><span data-stu-id="3b76b-401">Sets the MIDI sequencer to use file data as the synchronization source.</span></span> <span data-ttu-id="3b76b-402">這是預設值。</span><span class="sxs-lookup"><span data-stu-id="3b76b-402">This is the default setting.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3b76b-403">從屬 midi</span><span class="sxs-lookup"><span data-stu-id="3b76b-403">slave midi</span></span></td>
<td><span data-ttu-id="3b76b-404">將 MIDI sequencer 設定為使用連入的 MIDI 資料作為同步處理來源。</span><span class="sxs-lookup"><span data-stu-id="3b76b-404">Sets the MIDI sequencer to use incoming MIDI data for the synchronization source.</span></span> <span data-ttu-id="3b76b-405">Sequencer 會以 MIDI 格式辨識同步處理資料。</span><span class="sxs-lookup"><span data-stu-id="3b76b-405">The sequencer recognizes synchronization data with the MIDI format.</span></span> <span data-ttu-id="3b76b-406">MCISEQ sequencer 不支援此旗標。</span><span class="sxs-lookup"><span data-stu-id="3b76b-406">The MCISEQ sequencer does not support this flag.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3b76b-407">從屬無</span><span class="sxs-lookup"><span data-stu-id="3b76b-407">slave none</span></span></td>
<td><span data-ttu-id="3b76b-408">將 MIDI sequencer 設定為忽略同步處理</span><span class="sxs-lookup"><span data-stu-id="3b76b-408">Sets the MIDI sequencer to ignore synchronization</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3b76b-409">從屬的 smpte</span><span class="sxs-lookup"><span data-stu-id="3b76b-409">slave smpte</span></span></td>
<td><span data-ttu-id="3b76b-410">將 MIDI sequencer 設定為使用連入的 MIDI 資料作為同步處理來源。</span><span class="sxs-lookup"><span data-stu-id="3b76b-410">Sets the MIDI sequencer to use incoming MIDI data for the synchronization source.</span></span> <span data-ttu-id="3b76b-411">Sequencer 會以 SMPTE 格式辨識同步處理資料。</span><span class="sxs-lookup"><span data-stu-id="3b76b-411">The sequencer recognizes synchronization data with the SMPTE format.</span></span> <span data-ttu-id="3b76b-412">MCISEQ sequencer 不支援此旗標。</span><span class="sxs-lookup"><span data-stu-id="3b76b-412">The MCISEQ sequencer does not support this flag.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3b76b-413">速度因素</span><span class="sxs-lookup"><span data-stu-id="3b76b-413">speed factor</span></span></td>
<td><span data-ttu-id="3b76b-414">設定從工作區播放影片和音訊的相對速度。</span><span class="sxs-lookup"><span data-stu-id="3b76b-414">Sets the relative speed of video and audio playback from the workspace.</span></span> <span data-ttu-id="3b76b-415">因素是名義畫面播放速率與所需畫面播放速率之間的比率，其中名義畫面播放速率會指定為1000。</span><span class="sxs-lookup"><span data-stu-id="3b76b-415">Factor is the ratio between the nominal frame rate and the desired frame rate, where the nominal frame rate is designated as 1000.</span></span> <span data-ttu-id="3b76b-416"> (的速率為500的一半是正常的速度、2000是兩倍的一般速度，依此類推。 ) 將速度設定為零，就會盡可能快速地播放影片，而不會卸載畫面格而不需要音訊。</span><span class="sxs-lookup"><span data-stu-id="3b76b-416">(A rate of 500 is half normal speed, 2000 is twice normal speed, and so on.) Setting the speed to zero plays the video as fast as possible without dropping frames and without audio.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3b76b-417">仍為檔案格式 <em>格式</em></span><span class="sxs-lookup"><span data-stu-id="3b76b-417">still file format <em>format</em></span></span></td>
<td><span data-ttu-id="3b76b-418">指定用於 capture 命令的檔案格式。</span><span class="sxs-lookup"><span data-stu-id="3b76b-418">Specifies the file format used for capture commands.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3b76b-419">節奏 tempo_value</span><span class="sxs-lookup"><span data-stu-id="3b76b-419">tempo tempo_value</span></span></td>
<td><span data-ttu-id="3b76b-420">根據目前時間格式設定序列的節奏。</span><span class="sxs-lookup"><span data-stu-id="3b76b-420">Sets the tempo of the sequence according to the current time format.</span></span> <span data-ttu-id="3b76b-421">如果是以 PPQN 為基礎的檔案，tempo_value 會以每分鐘的節拍來解讀。</span><span class="sxs-lookup"><span data-stu-id="3b76b-421">For a PPQN-based file, the tempo_value is interpreted as beats per minute.</span></span> <span data-ttu-id="3b76b-422">針對以 SMPTE 為基礎的檔案，tempo_value 會轉譯為每秒的畫面格。</span><span class="sxs-lookup"><span data-stu-id="3b76b-422">For a SMPTE-based file, the tempo_value is interpreted as frames per second.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3b76b-423">時間格式位元組</span><span class="sxs-lookup"><span data-stu-id="3b76b-423">time format bytes</span></span></td>
<td><span data-ttu-id="3b76b-424">在 PCM 檔案格式中，將時間格式設定為 bytes。</span><span class="sxs-lookup"><span data-stu-id="3b76b-424">In a PCM file format, sets the time format to bytes.</span></span> <span data-ttu-id="3b76b-425">此命令之後的所有位置資訊都指定為位元組。</span><span class="sxs-lookup"><span data-stu-id="3b76b-425">All position information is specified as bytes following this command.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3b76b-426">時間格式框架</span><span class="sxs-lookup"><span data-stu-id="3b76b-426">time format frames</span></span></td>
<td><span data-ttu-id="3b76b-427">將時間格式設定為框架。</span><span class="sxs-lookup"><span data-stu-id="3b76b-427">Sets the time format to frames.</span></span> <span data-ttu-id="3b76b-428">所有使用位置值的命令都將採用框架。</span><span class="sxs-lookup"><span data-stu-id="3b76b-428">All commands that use position values will assume frames.</span></span> <span data-ttu-id="3b76b-429">開啟裝置時，框架是預設模式。</span><span class="sxs-lookup"><span data-stu-id="3b76b-429">When the device is opened, frames is the default mode.</span></span> <span data-ttu-id="3b76b-430">使用 CAV 格式的 videodiscs 支援。</span><span class="sxs-lookup"><span data-stu-id="3b76b-430">Supported by videodiscs using CAV format.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3b76b-431">時間格式 hms</span><span class="sxs-lookup"><span data-stu-id="3b76b-431">time format hms</span></span></td>
<td><span data-ttu-id="3b76b-432">將時間格式設定為小時、分鐘和秒。</span><span class="sxs-lookup"><span data-stu-id="3b76b-432">Sets the time format to hours, minutes, and seconds.</span></span> <span data-ttu-id="3b76b-433">所有使用位置值的命令都將採用 HMS。</span><span class="sxs-lookup"><span data-stu-id="3b76b-433">All commands that use position values will assume HMS.</span></span> <span data-ttu-id="3b76b-434">HMS 是 CLV videodiscs 的預設格式。</span><span class="sxs-lookup"><span data-stu-id="3b76b-434">HMS is the default format for CLV videodiscs.</span></span> <span data-ttu-id="3b76b-435">將 HMS 值指定為 hh： mm： ss，其中 hh 為 hours，mm 為分鐘，ss 為秒。</span><span class="sxs-lookup"><span data-stu-id="3b76b-435">Specify an HMS value as hh:mm:ss, where hh is hours, mm is minutes, and ss is seconds.</span></span> <span data-ttu-id="3b76b-436">如果欄位和下列所有欄位都為零，您可以省略欄位。</span><span class="sxs-lookup"><span data-stu-id="3b76b-436">You can omit a field if it and all following fields are zero.</span></span> <span data-ttu-id="3b76b-437">例如，3、3:0 和3:0:0 都是表示3小時的有效方式。</span><span class="sxs-lookup"><span data-stu-id="3b76b-437">For example, 3, 3:0, and 3:0:0 are all valid ways to express 3 hours.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3b76b-438">時間格式毫秒</span><span class="sxs-lookup"><span data-stu-id="3b76b-438">time format milliseconds</span></span></td>
<td><span data-ttu-id="3b76b-439">將時間格式設定為毫秒。</span><span class="sxs-lookup"><span data-stu-id="3b76b-439">Sets the time format to milliseconds.</span></span> <span data-ttu-id="3b76b-440">使用位置值的所有命令都將採用毫秒。</span><span class="sxs-lookup"><span data-stu-id="3b76b-440">All commands that use position values will assume milliseconds.</span></span> <span data-ttu-id="3b76b-441">您可以將毫秒縮寫為 &quot; 毫秒 &quot; 。</span><span class="sxs-lookup"><span data-stu-id="3b76b-441">You can abbreviate milliseconds as &quot;ms&quot;.</span></span> <span data-ttu-id="3b76b-442">針對 sequencer 裝置，順序檔會將預設格式設定為 PPQN 或 SMPTE。</span><span class="sxs-lookup"><span data-stu-id="3b76b-442">For sequencer devices, the sequence file sets the default format to PPQN or SMPTE.</span></span> <span data-ttu-id="3b76b-443">影片重迭裝置不支援此旗標。</span><span class="sxs-lookup"><span data-stu-id="3b76b-443">Video-overlay devices do not support this flag.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3b76b-444">時間格式 msf</span><span class="sxs-lookup"><span data-stu-id="3b76b-444">time format msf</span></span></td>
<td><span data-ttu-id="3b76b-445">將時間格式設定為分鐘、秒和框架。</span><span class="sxs-lookup"><span data-stu-id="3b76b-445">Sets the time format to minutes, seconds, and frames.</span></span> <span data-ttu-id="3b76b-446">使用位置值的所有命令都會假設 MSF (CD 音訊) 的預設格式。</span><span class="sxs-lookup"><span data-stu-id="3b76b-446">All commands that use position values will assume MSF (the default format for CD audio).</span></span> <span data-ttu-id="3b76b-447">將 MSF 值指定為 mm： ss： ff，其中 mm 為分鐘，ss 為秒，而 ff 為框架。</span><span class="sxs-lookup"><span data-stu-id="3b76b-447">Specify an MSF value as mm:ss:ff, where mm is minutes, ss is seconds, and ff is frames.</span></span> <span data-ttu-id="3b76b-448">如果欄位和下列所有欄位都為零，您可以省略欄位。</span><span class="sxs-lookup"><span data-stu-id="3b76b-448">You can omit a field if it and all following fields are zero.</span></span> <span data-ttu-id="3b76b-449">例如，3、3:0 和3:0:0 是表示3分鐘的有效方式。</span><span class="sxs-lookup"><span data-stu-id="3b76b-449">For example, 3, 3:0, and 3:0:0 are valid ways to express 3 minutes.</span></span><br/> <span data-ttu-id="3b76b-450">MSF 欄位具有下列最大值：</span><span class="sxs-lookup"><span data-stu-id="3b76b-450">The MSF fields have the following maximum values:</span></span><br/>
<ul>
<li><span data-ttu-id="3b76b-451">分鐘99</span><span class="sxs-lookup"><span data-stu-id="3b76b-451">Minutes 99</span></span></li>
<li><span data-ttu-id="3b76b-452">秒59</span><span class="sxs-lookup"><span data-stu-id="3b76b-452">Seconds 59</span></span></li>
<li><span data-ttu-id="3b76b-453">畫面格74</span><span class="sxs-lookup"><span data-stu-id="3b76b-453">Frames 74</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3b76b-454">時間格式範例</span><span class="sxs-lookup"><span data-stu-id="3b76b-454">time format samples</span></span></td>
<td><span data-ttu-id="3b76b-455">將時間格式設定為範例。</span><span class="sxs-lookup"><span data-stu-id="3b76b-455">Sets the time format to samples.</span></span> <span data-ttu-id="3b76b-456">在此命令之後，所有位置資訊都指定為範例。</span><span class="sxs-lookup"><span data-stu-id="3b76b-456">All position information is specified as samples following this command.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3b76b-457">時間格式 smpte 24</span><span class="sxs-lookup"><span data-stu-id="3b76b-457">time format smpte 24</span></span><br/> <span data-ttu-id="3b76b-458">時間格式 smpte 25</span><span class="sxs-lookup"><span data-stu-id="3b76b-458">time format smpte 25</span></span><br/> <span data-ttu-id="3b76b-459">時間格式 smpte 30</span><span class="sxs-lookup"><span data-stu-id="3b76b-459">time format smpte 30</span></span><br/></td>
<td><span data-ttu-id="3b76b-460">將時間格式設定為 SMPTE 畫面播放速率。</span><span class="sxs-lookup"><span data-stu-id="3b76b-460">Sets the time format to an SMPTE frame rate.</span></span> <span data-ttu-id="3b76b-461">若為 Vcr，請將時間格式設定為 hh： mm： ss： ff，其中合法的值為00:00:00:00 到23：59：59： xx，而 xx 則小於以旗標中指定的數位24、25或30所指定的每秒畫面格數。</span><span class="sxs-lookup"><span data-stu-id="3b76b-461">For VCRs, sets the time format to hh:mm:ss:ff, where the legal values are 00:00:00:00 through 23:59:59:xx, and xx is one less than the frames per second as specified by the number 24, 25, or 30 as specified in the flag.</span></span> <span data-ttu-id="3b76b-462">在輸入時，冒號 (： ) 需要分隔元件。</span><span class="sxs-lookup"><span data-stu-id="3b76b-462">On input, colons (:) are required to separate the components.</span></span> <span data-ttu-id="3b76b-463">若為00，則可以省略最不重要的單位;例如，02:00 與02:00:00:00 相同。</span><span class="sxs-lookup"><span data-stu-id="3b76b-463">The least significant units can be omitted if they are 00; for example, 02:00 is the same as 02:00:00:00.</span></span> <span data-ttu-id="3b76b-464">使用位置值的所有命令都會採用 SMPTE 格式。</span><span class="sxs-lookup"><span data-stu-id="3b76b-464">All commands that use position values will assume SMPTE format.</span></span><br/> <span data-ttu-id="3b76b-465">順序檔會將預設格式設定為 PPQN 或 SMPTE。</span><span class="sxs-lookup"><span data-stu-id="3b76b-465">The sequence file sets the default format to PPQN or SMPTE.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3b76b-466">時間格式 smpte 30 捨棄</span><span class="sxs-lookup"><span data-stu-id="3b76b-466">time format smpte 30 drop</span></span></td>
<td><span data-ttu-id="3b76b-467">將時間格式設定為 SMPTE 30 捨棄畫面播放速率。</span><span class="sxs-lookup"><span data-stu-id="3b76b-467">Sets the time format to SMPTE 30 drop frame rate.</span></span> <span data-ttu-id="3b76b-468">針對 Vcr （與 SMPTE 30 相同），不同之處在于會從格式中卸載特定的時間碼位置，以將每個畫面格的記錄時間碼位置 (為 NTSC 畫面播放速率 29.97 fps) 對應至 30 fps) 的即時 (。</span><span class="sxs-lookup"><span data-stu-id="3b76b-468">For VCRs, same as SMPTE 30, except that certain timecode positions are dropped from the format to have the recorded timecode positions for each frame (at the NTSC frame rate of 29.97 fps) correspond to real time (at 30 fps).</span></span> <span data-ttu-id="3b76b-469">已卸載的時間碼位置如下：每分鐘的兩分鐘（每分鐘），針對記錄內容的每十分鐘的前九個。</span><span class="sxs-lookup"><span data-stu-id="3b76b-469">Timecode positions that are dropped are as follows: two every minute, on the minute, for the first nine of every ten minutes of recorded content.</span></span> <span data-ttu-id="3b76b-470">例如，在01:04:59:29，下一個時間碼位置會是01:05:00:02，而不是01:05:00:00。</span><span class="sxs-lookup"><span data-stu-id="3b76b-470">For example, at 01:04:59:29, the next timecode position would be 01:05:00:02, not 01:05:00:00.</span></span> <span data-ttu-id="3b76b-471">使用位置值的所有命令都會採用 SMPTE 格式。</span><span class="sxs-lookup"><span data-stu-id="3b76b-471">All commands that use position values will assume SMPTE format.</span></span><br/> <span data-ttu-id="3b76b-472">順序檔會將預設格式設定為 PPQN 或 SMPTE。</span><span class="sxs-lookup"><span data-stu-id="3b76b-472">The sequence file sets the default format to PPQN or SMPTE.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3b76b-473">時間格式歌曲指標</span><span class="sxs-lookup"><span data-stu-id="3b76b-473">time format song pointer</span></span></td>
<td><span data-ttu-id="3b76b-474">將時間格式設定為歌曲指標， (第十六個附注) 。</span><span class="sxs-lookup"><span data-stu-id="3b76b-474">Sets the time format to song pointer (sixteenth notes).</span></span> <span data-ttu-id="3b76b-475">所有使用位置值的命令都將採用歌曲指標單位。</span><span class="sxs-lookup"><span data-stu-id="3b76b-475">All commands that use position values will assume song pointer units.</span></span> <span data-ttu-id="3b76b-476">此旗標只適用于一系列的除法類型 PPQN。</span><span class="sxs-lookup"><span data-stu-id="3b76b-476">This flag is valid only for a sequence of division type PPQN.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3b76b-477">時間格式 tmsf</span><span class="sxs-lookup"><span data-stu-id="3b76b-477">time format tmsf</span></span></td>
<td><span data-ttu-id="3b76b-478">設定要追蹤、分、秒和框架的時間格式。</span><span class="sxs-lookup"><span data-stu-id="3b76b-478">Sets the time format to tracks, minutes, seconds, and frames.</span></span> <span data-ttu-id="3b76b-479">所有使用位置值的命令都將採用 TMSF。</span><span class="sxs-lookup"><span data-stu-id="3b76b-479">All commands that use position values will assume TMSF.</span></span> <span data-ttu-id="3b76b-480">將 TMSF 值指定為 tt： mm： ss： ff，其中 tt 為曲目，mm 為分鐘，ss 為秒，而 ff 為框架。</span><span class="sxs-lookup"><span data-stu-id="3b76b-480">Specify a TMSF value as tt:mm:ss:ff, where tt is tracks, mm is minutes, ss is seconds, and ff is frames.</span></span> <span data-ttu-id="3b76b-481">如果欄位和下列所有欄位都為零，您可以省略欄位。</span><span class="sxs-lookup"><span data-stu-id="3b76b-481">You can omit a field if it and all following fields are zero.</span></span> <span data-ttu-id="3b76b-482">例如，3、3:0、3:0:0 和3:0:0:0 都是快速追蹤3的有效方式。</span><span class="sxs-lookup"><span data-stu-id="3b76b-482">For example, 3, 3:0, 3:0:0, and 3:0:0:0 are all valid ways to express track 3.</span></span> <br/> <span data-ttu-id="3b76b-483">TMSF 欄位的最大值如下：</span><span class="sxs-lookup"><span data-stu-id="3b76b-483">The TMSF fields have the following maximum values:</span></span><br/>
<ul>
<li><span data-ttu-id="3b76b-484">追蹤99</span><span class="sxs-lookup"><span data-stu-id="3b76b-484">Tracks 99</span></span></li>
<li><span data-ttu-id="3b76b-485">分鐘90</span><span class="sxs-lookup"><span data-stu-id="3b76b-485">Minutes 90</span></span></li>
<li><span data-ttu-id="3b76b-486">秒59</span><span class="sxs-lookup"><span data-stu-id="3b76b-486">Seconds 59</span></span></li>
<li><span data-ttu-id="3b76b-487">畫面格74</span><span class="sxs-lookup"><span data-stu-id="3b76b-487">Frames 74</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3b76b-488">時間格式追蹤</span><span class="sxs-lookup"><span data-stu-id="3b76b-488">time format track</span></span></td>
<td><span data-ttu-id="3b76b-489">設定要追蹤的位置格式。</span><span class="sxs-lookup"><span data-stu-id="3b76b-489">Sets the position format to tracks.</span></span> <span data-ttu-id="3b76b-490">所有使用位置值的命令都將採用追蹤。</span><span class="sxs-lookup"><span data-stu-id="3b76b-490">All commands that use position values will assume tracks.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3b76b-491">時間模式計數器</span><span class="sxs-lookup"><span data-stu-id="3b76b-491">time mode counter</span></span></td>
<td><span data-ttu-id="3b76b-492">設定位置資訊模式以使用 VCR 計數器。</span><span class="sxs-lookup"><span data-stu-id="3b76b-492">Sets the position-information mode to use the VCR counters.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3b76b-493">偵測時間模式</span><span class="sxs-lookup"><span data-stu-id="3b76b-493">time mode detect</span></span></td>
<td><span data-ttu-id="3b76b-494">根據磁帶上的時間碼資訊偵測來設定位置資訊模式。</span><span class="sxs-lookup"><span data-stu-id="3b76b-494">Sets the position information mode based on detection of timecode information on the tape.</span></span> <span data-ttu-id="3b76b-495">如果偵測到時間碼資訊，則時間類型會設定為時間 &quot; 碼， &quot; 否則，時間類型會設定為 &quot; counter &quot; 。</span><span class="sxs-lookup"><span data-stu-id="3b76b-495">If timecode information is detected, the time type is set to &quot;timecode&quot;; otherwise, the time type is set to &quot;counter&quot;.</span></span> <span data-ttu-id="3b76b-496">&quot;偵測 &quot; 是一種特殊模式。</span><span class="sxs-lookup"><span data-stu-id="3b76b-496">&quot;Detect&quot; is a special mode.</span></span> <span data-ttu-id="3b76b-497">只要開啟驅動程式、插入新的磁帶，或 &quot; 發出時間模式 &quot; 命令，驅動程式就會檢查磁帶上目前可用的時間模式，並將 &quot; 時間類型設定 &quot; 為時間 &quot; 碼 &quot; 或 &quot; 計數器 &quot; 。</span><span class="sxs-lookup"><span data-stu-id="3b76b-497">Whenever the driver is opened, a new tape is inserted, or the &quot;time mode&quot; command is issued, the driver checks the current time mode available on the tape and sets &quot;time type&quot; to either &quot;timecode&quot; or &quot;counter&quot;.</span></span> <span data-ttu-id="3b76b-498">一旦 &quot; 設定時間類型之後 &quot; ，驅動程式就不會變更它，直到上述其中一個條件再次發生為止。</span><span class="sxs-lookup"><span data-stu-id="3b76b-498">Once &quot;time type&quot; is set, the driver doesn't change it until one of the above conditions occurs again.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3b76b-499">時間模式時間碼</span><span class="sxs-lookup"><span data-stu-id="3b76b-499">time mode timecode</span></span></td>
<td><span data-ttu-id="3b76b-500">設定位置資訊模式，以使用 &quot; &quot; 磁帶上的時間碼資訊。</span><span class="sxs-lookup"><span data-stu-id="3b76b-500">Sets the position information mode to use &quot;timecode&quot; information on the tape.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3b76b-501">追蹤加號</span><span class="sxs-lookup"><span data-stu-id="3b76b-501">tracking plus</span></span> <br/> <span data-ttu-id="3b76b-502">追蹤減號</span><span class="sxs-lookup"><span data-stu-id="3b76b-502">tracking minus</span></span> <br/> <span data-ttu-id="3b76b-503">追蹤重設</span><span class="sxs-lookup"><span data-stu-id="3b76b-503">tracking reset</span></span> <br/></td>
<td><span data-ttu-id="3b76b-504">以精確的遞增方式調整磁帶傳輸的速度。</span><span class="sxs-lookup"><span data-stu-id="3b76b-504">Adjusts the speed of the videotape transport in fine increments.</span></span> <span data-ttu-id="3b76b-505">&quot; &quot; 從 VCR 取得有雜訊的圖片時，請使用追蹤旗標。</span><span class="sxs-lookup"><span data-stu-id="3b76b-505">Use the &quot;tracking&quot; flags when a noisy picture is obtained from a VCR.</span></span> <span data-ttu-id="3b76b-506">&quot;追蹤加號 &quot; 會增加傳送速率。</span><span class="sxs-lookup"><span data-stu-id="3b76b-506">&quot;Tracking plus&quot; increases the transport speed.</span></span> <span data-ttu-id="3b76b-507">&quot;追蹤減號可 &quot; 減少傳送速率。</span><span class="sxs-lookup"><span data-stu-id="3b76b-507">&quot;Tracking minus&quot; decreases the transport speed.</span></span> <span data-ttu-id="3b76b-508">&quot;追蹤重設會 &quot; 將追蹤調整傳回零。</span><span class="sxs-lookup"><span data-stu-id="3b76b-508">&quot;Tracking reset&quot; returns the tracking adjustment to zero.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3b76b-509">關閉影片</span><span class="sxs-lookup"><span data-stu-id="3b76b-509">video off</span></span></td>
<td><span data-ttu-id="3b76b-510">停用影片輸出。</span><span class="sxs-lookup"><span data-stu-id="3b76b-510">Disables video output.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3b76b-511">影片開啟</span><span class="sxs-lookup"><span data-stu-id="3b76b-511">video on</span></span></td>
<td><span data-ttu-id="3b76b-512">啟用影片輸出。</span><span class="sxs-lookup"><span data-stu-id="3b76b-512">Enables video output.</span></span></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="3b76b-513"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="3b76b-513"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="3b76b-514">可以是「等候」、「通知」或兩者。</span><span class="sxs-lookup"><span data-stu-id="3b76b-514">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="3b76b-515">針對數位影片和 VCR 裝置，也可以指定「測試」。</span><span class="sxs-lookup"><span data-stu-id="3b76b-515">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="3b76b-516">如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。</span><span class="sxs-lookup"><span data-stu-id="3b76b-516">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b76b-517">傳回值</span><span class="sxs-lookup"><span data-stu-id="3b76b-517">Return Value</span></span>

<span data-ttu-id="3b76b-518">如果成功則傳回零，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="3b76b-518">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="3b76b-519">備註</span><span class="sxs-lookup"><span data-stu-id="3b76b-519">Remarks</span></span>

<span data-ttu-id="3b76b-520">在儲存資料的檔案建立時，會定義多個波形音訊資料的屬性。</span><span class="sxs-lookup"><span data-stu-id="3b76b-520">Several properties of waveform-audio data are defined when the file to store the data is created.</span></span> <span data-ttu-id="3b76b-521">這些屬性會描述如何在檔案中結構化資料，而且在錄製開始之後就無法變更。</span><span class="sxs-lookup"><span data-stu-id="3b76b-521">These properties describe how the data is structured within the file and cannot be changed once recording begins.</span></span> <span data-ttu-id="3b76b-522">下列清單會識別這些屬性：</span><span class="sxs-lookup"><span data-stu-id="3b76b-522">The following list identifies these properties:</span></span>

-   <span data-ttu-id="3b76b-523">對齊</span><span class="sxs-lookup"><span data-stu-id="3b76b-523">alignment</span></span>
-   <span data-ttu-id="3b76b-524">bitspersample</span><span class="sxs-lookup"><span data-stu-id="3b76b-524">bitspersample</span></span>
-   <span data-ttu-id="3b76b-525">bytespersec</span><span class="sxs-lookup"><span data-stu-id="3b76b-525">bytespersec</span></span>
-   <span data-ttu-id="3b76b-526">通道</span><span class="sxs-lookup"><span data-stu-id="3b76b-526">channels</span></span>
-   <span data-ttu-id="3b76b-527">格式標記</span><span class="sxs-lookup"><span data-stu-id="3b76b-527">format tag</span></span>
-   <span data-ttu-id="3b76b-528">samplespersec</span><span class="sxs-lookup"><span data-stu-id="3b76b-528">samplespersec</span></span>

## <a name="examples"></a><span data-ttu-id="3b76b-529">範例</span><span class="sxs-lookup"><span data-stu-id="3b76b-529">Examples</span></span>

<span data-ttu-id="3b76b-530">下列命令會將時間格式設定為毫秒，並將波形-音訊格式設定為8位、mono、11 kHz。</span><span class="sxs-lookup"><span data-stu-id="3b76b-530">The following command sets the time format to milliseconds and sets the waveform-audio format to 8 bit, mono, 11 kHz.</span></span>

``` syntax
set mysound time format ms bitspersample 8 channels 1 samplespersec 11025
```

## <a name="requirements"></a><span data-ttu-id="3b76b-531">規格需求</span><span class="sxs-lookup"><span data-stu-id="3b76b-531">Requirements</span></span>



| <span data-ttu-id="3b76b-532">需求</span><span class="sxs-lookup"><span data-stu-id="3b76b-532">Requirement</span></span> | <span data-ttu-id="3b76b-533">值</span><span class="sxs-lookup"><span data-stu-id="3b76b-533">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="3b76b-534">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3b76b-534">Minimum supported client</span></span><br/> | <span data-ttu-id="3b76b-535">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3b76b-535">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="3b76b-536">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3b76b-536">Minimum supported server</span></span><br/> | <span data-ttu-id="3b76b-537">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3b76b-537">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="3b76b-538">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3b76b-538">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b76b-539">Mci</span><span class="sxs-lookup"><span data-stu-id="3b76b-539">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="3b76b-540">MCI 命令字串</span><span class="sxs-lookup"><span data-stu-id="3b76b-540">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="3b76b-541">捕獲</span><span class="sxs-lookup"><span data-stu-id="3b76b-541">capture</span></span>](capture.md)
</dt> <dt>

[<span data-ttu-id="3b76b-542">pause</span><span class="sxs-lookup"><span data-stu-id="3b76b-542">pause</span></span>](pause.md)
</dt> <dt>

[<span data-ttu-id="3b76b-543">儲存</span><span class="sxs-lookup"><span data-stu-id="3b76b-543">save</span></span>](save.md)
</dt> <dt>

[<span data-ttu-id="3b76b-544">停止</span><span class="sxs-lookup"><span data-stu-id="3b76b-544">stop</span></span>](stop.md)
</dt> </dl>

 

