---
title: 功能命令
description: 功能命令會要求裝置特定功能的相關資訊。 所有 MCI 裝置都會辨識此命令。
ms.assetid: 1b470473-0de6-41ba-9f6e-41f0b13ceaeb
keywords:
- 功能命令 Windows 多媒體
topic_type:
- apiref
api_name:
- capability
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a6ac87b98fb8d748a5baf2665cc5a63230b6a98
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464636"
---
# <a name="capability-command"></a><span data-ttu-id="746e2-105">功能命令</span><span class="sxs-lookup"><span data-stu-id="746e2-105">capability command</span></span>

<span data-ttu-id="746e2-106">功能命令會要求裝置特定功能的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="746e2-106">The capability command requests information about a particular capability of a device.</span></span> <span data-ttu-id="746e2-107">所有 MCI 裝置都會辨識此命令。</span><span class="sxs-lookup"><span data-stu-id="746e2-107">All MCI devices recognize this command.</span></span>

<span data-ttu-id="746e2-108">若要傳送此命令，請使用 *lpszCommand* 參數設定來呼叫 [**mciSendString**](/previous-versions//dd757161(v=vs.85))函式，如下所示。</span><span class="sxs-lookup"><span data-stu-id="746e2-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("capability %s %s %s"), 
  lpszDeviceID, 
  lpszRequest, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="746e2-109">參數</span><span class="sxs-lookup"><span data-stu-id="746e2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="746e2-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="746e2-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="746e2-111">MCI 裝置的識別碼。</span><span class="sxs-lookup"><span data-stu-id="746e2-111">Identifier of an MCI device.</span></span> <span data-ttu-id="746e2-112">開啟裝置時，會指派此識別碼或別名。</span><span class="sxs-lookup"><span data-stu-id="746e2-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="746e2-113"><span id="lpszRequest"></span><span id="lpszrequest"></span><span id="LPSZREQUEST"></span>*lpszRequest*</span><span class="sxs-lookup"><span data-stu-id="746e2-113"><span id="lpszRequest"></span><span id="lpszrequest"></span><span id="LPSZREQUEST"></span>*lpszRequest*</span></span>
</dt> <dd>

<span data-ttu-id="746e2-114">識別裝置功能的旗標。</span><span class="sxs-lookup"><span data-stu-id="746e2-114">Flag that identifies a device capability.</span></span> <span data-ttu-id="746e2-115">下表列出可辨識 **功能** 命令的裝置類型，以及每種類型使用的旗標：</span><span class="sxs-lookup"><span data-stu-id="746e2-115">The following table lists device types that recognize the **capability** command and the flags used by each type:</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="746e2-116">值</span><span class="sxs-lookup"><span data-stu-id="746e2-116">Value</span></span></th>
<th><span data-ttu-id="746e2-117">類型</span><span class="sxs-lookup"><span data-stu-id="746e2-117">Type</span></span></th>
<th><span data-ttu-id="746e2-118">類型</span><span class="sxs-lookup"><span data-stu-id="746e2-118">Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="746e2-119">cdaudio</span><span class="sxs-lookup"><span data-stu-id="746e2-119">cdaudio</span></span></td>
<td><ul>
<li><span data-ttu-id="746e2-120">可以退出</span><span class="sxs-lookup"><span data-stu-id="746e2-120">can eject</span></span></li>
<li><span data-ttu-id="746e2-121">可以播放</span><span class="sxs-lookup"><span data-stu-id="746e2-121">can play</span></span></li>
<li><span data-ttu-id="746e2-122">可以記錄</span><span class="sxs-lookup"><span data-stu-id="746e2-122">can record</span></span></li>
<li><span data-ttu-id="746e2-123">可以儲存</span><span class="sxs-lookup"><span data-stu-id="746e2-123">can save</span></span></li>
<li><span data-ttu-id="746e2-124">複合裝置</span><span class="sxs-lookup"><span data-stu-id="746e2-124">compound device</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="746e2-125">裝置類型</span><span class="sxs-lookup"><span data-stu-id="746e2-125">device type</span></span></li>
<li><span data-ttu-id="746e2-126">有音訊</span><span class="sxs-lookup"><span data-stu-id="746e2-126">has audio</span></span></li>
<li><span data-ttu-id="746e2-127">有影片</span><span class="sxs-lookup"><span data-stu-id="746e2-127">has video</span></span></li>
<li><span data-ttu-id="746e2-128">使用檔案</span><span class="sxs-lookup"><span data-stu-id="746e2-128">uses files</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="746e2-129">digitalvideo</span><span class="sxs-lookup"><span data-stu-id="746e2-129">digitalvideo</span></span></td>
<td><ul>
<li><span data-ttu-id="746e2-130">可以退出</span><span class="sxs-lookup"><span data-stu-id="746e2-130">can eject</span></span></li>
<li><span data-ttu-id="746e2-131">可以凍結</span><span class="sxs-lookup"><span data-stu-id="746e2-131">can freeze</span></span></li>
<li><span data-ttu-id="746e2-132">可以鎖定</span><span class="sxs-lookup"><span data-stu-id="746e2-132">can lock</span></span></li>
<li><span data-ttu-id="746e2-133">可以播放</span><span class="sxs-lookup"><span data-stu-id="746e2-133">can play</span></span></li>
<li><span data-ttu-id="746e2-134">可以記錄</span><span class="sxs-lookup"><span data-stu-id="746e2-134">can record</span></span></li>
<li><span data-ttu-id="746e2-135">可以反轉</span><span class="sxs-lookup"><span data-stu-id="746e2-135">can reverse</span></span></li>
<li><span data-ttu-id="746e2-136">可以儲存</span><span class="sxs-lookup"><span data-stu-id="746e2-136">can save</span></span></li>
<li><span data-ttu-id="746e2-137">可以延展</span><span class="sxs-lookup"><span data-stu-id="746e2-137">can stretch</span></span></li>
<li><span data-ttu-id="746e2-138">可延展輸入</span><span class="sxs-lookup"><span data-stu-id="746e2-138">can stretch input</span></span></li>
<li><span data-ttu-id="746e2-139">可以測試</span><span class="sxs-lookup"><span data-stu-id="746e2-139">can test</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="746e2-140">複合裝置</span><span class="sxs-lookup"><span data-stu-id="746e2-140">compound device</span></span></li>
<li><span data-ttu-id="746e2-141">裝置類型</span><span class="sxs-lookup"><span data-stu-id="746e2-141">device type</span></span></li>
<li><span data-ttu-id="746e2-142">有音訊</span><span class="sxs-lookup"><span data-stu-id="746e2-142">has audio</span></span></li>
<li><span data-ttu-id="746e2-143">仍有</span><span class="sxs-lookup"><span data-stu-id="746e2-143">has still</span></span></li>
<li><span data-ttu-id="746e2-144">有影片</span><span class="sxs-lookup"><span data-stu-id="746e2-144">has video</span></span></li>
<li><span data-ttu-id="746e2-145">最大播放率</span><span class="sxs-lookup"><span data-stu-id="746e2-145">maximum play rate</span></span></li>
<li><span data-ttu-id="746e2-146">最小播放率</span><span class="sxs-lookup"><span data-stu-id="746e2-146">minimum play rate</span></span></li>
<li><span data-ttu-id="746e2-147">使用檔案</span><span class="sxs-lookup"><span data-stu-id="746e2-147">uses files</span></span></li>
<li><span data-ttu-id="746e2-148">使用調色板</span><span class="sxs-lookup"><span data-stu-id="746e2-148">uses palettes</span></span></li>
<li><span data-ttu-id="746e2-149">windows</span><span class="sxs-lookup"><span data-stu-id="746e2-149">windows</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="746e2-150">overlay</span><span class="sxs-lookup"><span data-stu-id="746e2-150">overlay</span></span></td>
<td><ul>
<li><span data-ttu-id="746e2-151">可以退出</span><span class="sxs-lookup"><span data-stu-id="746e2-151">can eject</span></span></li>
<li><span data-ttu-id="746e2-152">可以凍結</span><span class="sxs-lookup"><span data-stu-id="746e2-152">can freeze</span></span></li>
<li><span data-ttu-id="746e2-153">可以播放</span><span class="sxs-lookup"><span data-stu-id="746e2-153">can play</span></span></li>
<li><span data-ttu-id="746e2-154">可以記錄</span><span class="sxs-lookup"><span data-stu-id="746e2-154">can record</span></span></li>
<li><span data-ttu-id="746e2-155">可以儲存</span><span class="sxs-lookup"><span data-stu-id="746e2-155">can save</span></span></li>
<li><span data-ttu-id="746e2-156">可以延展</span><span class="sxs-lookup"><span data-stu-id="746e2-156">can stretch</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="746e2-157">複合裝置</span><span class="sxs-lookup"><span data-stu-id="746e2-157">compound device</span></span></li>
<li><span data-ttu-id="746e2-158">裝置類型</span><span class="sxs-lookup"><span data-stu-id="746e2-158">device type</span></span></li>
<li><span data-ttu-id="746e2-159">有音訊</span><span class="sxs-lookup"><span data-stu-id="746e2-159">has audio</span></span></li>
<li><span data-ttu-id="746e2-160">有影片</span><span class="sxs-lookup"><span data-stu-id="746e2-160">has video</span></span></li>
<li><span data-ttu-id="746e2-161">使用檔案</span><span class="sxs-lookup"><span data-stu-id="746e2-161">uses files</span></span></li>
<li><span data-ttu-id="746e2-162">windows</span><span class="sxs-lookup"><span data-stu-id="746e2-162">windows</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="746e2-163">排序器</span><span class="sxs-lookup"><span data-stu-id="746e2-163">sequencer</span></span></td>
<td><ul>
<li><span data-ttu-id="746e2-164">可以退出</span><span class="sxs-lookup"><span data-stu-id="746e2-164">can eject</span></span></li>
<li><span data-ttu-id="746e2-165">可以播放</span><span class="sxs-lookup"><span data-stu-id="746e2-165">can play</span></span></li>
<li><span data-ttu-id="746e2-166">可以記錄</span><span class="sxs-lookup"><span data-stu-id="746e2-166">can record</span></span></li>
<li><span data-ttu-id="746e2-167">可以儲存</span><span class="sxs-lookup"><span data-stu-id="746e2-167">can save</span></span></li>
<li><span data-ttu-id="746e2-168">複合裝置</span><span class="sxs-lookup"><span data-stu-id="746e2-168">compound device</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="746e2-169">裝置類型</span><span class="sxs-lookup"><span data-stu-id="746e2-169">device type</span></span></li>
<li><span data-ttu-id="746e2-170">有音訊</span><span class="sxs-lookup"><span data-stu-id="746e2-170">has audio</span></span></li>
<li><span data-ttu-id="746e2-171">有影片</span><span class="sxs-lookup"><span data-stu-id="746e2-171">has video</span></span></li>
<li><span data-ttu-id="746e2-172">使用檔案</span><span class="sxs-lookup"><span data-stu-id="746e2-172">uses files</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="746e2-173">錄影機</span><span class="sxs-lookup"><span data-stu-id="746e2-173">vcr</span></span></td>
<td><ul>
<li><span data-ttu-id="746e2-174">可以偵測長度</span><span class="sxs-lookup"><span data-stu-id="746e2-174">can detect length</span></span></li>
<li><span data-ttu-id="746e2-175">可以退出</span><span class="sxs-lookup"><span data-stu-id="746e2-175">can eject</span></span></li>
<li><span data-ttu-id="746e2-176">可以凍結</span><span class="sxs-lookup"><span data-stu-id="746e2-176">can freeze</span></span></li>
<li><span data-ttu-id="746e2-177">可以監視來源</span><span class="sxs-lookup"><span data-stu-id="746e2-177">can monitor sources</span></span></li>
<li><span data-ttu-id="746e2-178">可以播放</span><span class="sxs-lookup"><span data-stu-id="746e2-178">can play</span></span></li>
<li><span data-ttu-id="746e2-179">可以預先進行</span><span class="sxs-lookup"><span data-stu-id="746e2-179">can preroll</span></span></li>
<li><span data-ttu-id="746e2-180">可以預覽</span><span class="sxs-lookup"><span data-stu-id="746e2-180">can preview</span></span></li>
<li><span data-ttu-id="746e2-181">可以記錄</span><span class="sxs-lookup"><span data-stu-id="746e2-181">can record</span></span></li>
<li><span data-ttu-id="746e2-182">可以反轉</span><span class="sxs-lookup"><span data-stu-id="746e2-182">can reverse</span></span></li>
<li><span data-ttu-id="746e2-183">可以儲存</span><span class="sxs-lookup"><span data-stu-id="746e2-183">can save</span></span></li>
<li><span data-ttu-id="746e2-184">可以測試</span><span class="sxs-lookup"><span data-stu-id="746e2-184">can test</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="746e2-185">頻率遞增率</span><span class="sxs-lookup"><span data-stu-id="746e2-185">clock increment rate</span></span></li>
<li><span data-ttu-id="746e2-186">複合裝置</span><span class="sxs-lookup"><span data-stu-id="746e2-186">compound device</span></span></li>
<li><span data-ttu-id="746e2-187">裝置類型</span><span class="sxs-lookup"><span data-stu-id="746e2-187">device type</span></span></li>
<li><span data-ttu-id="746e2-188">有音訊</span><span class="sxs-lookup"><span data-stu-id="746e2-188">has audio</span></span></li>
<li><span data-ttu-id="746e2-189">具有時鐘</span><span class="sxs-lookup"><span data-stu-id="746e2-189">has clock</span></span></li>
<li><span data-ttu-id="746e2-190">有時間碼</span><span class="sxs-lookup"><span data-stu-id="746e2-190">has timecode</span></span></li>
<li><span data-ttu-id="746e2-191">有影片</span><span class="sxs-lookup"><span data-stu-id="746e2-191">has video</span></span></li>
<li><span data-ttu-id="746e2-192">標記數目</span><span class="sxs-lookup"><span data-stu-id="746e2-192">number of marks</span></span></li>
<li><span data-ttu-id="746e2-193">搜尋精確度</span><span class="sxs-lookup"><span data-stu-id="746e2-193">seek accuracy</span></span></li>
<li><span data-ttu-id="746e2-194">使用檔案</span><span class="sxs-lookup"><span data-stu-id="746e2-194">uses files</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="746e2-195">videodisc</span><span class="sxs-lookup"><span data-stu-id="746e2-195">videodisc</span></span></td>
<td><ul>
<li><span data-ttu-id="746e2-196">可以退出</span><span class="sxs-lookup"><span data-stu-id="746e2-196">can eject</span></span></li>
<li><span data-ttu-id="746e2-197">可以播放</span><span class="sxs-lookup"><span data-stu-id="746e2-197">can play</span></span></li>
<li><span data-ttu-id="746e2-198">可以記錄</span><span class="sxs-lookup"><span data-stu-id="746e2-198">can record</span></span></li>
<li><span data-ttu-id="746e2-199">可以反轉</span><span class="sxs-lookup"><span data-stu-id="746e2-199">can reverse</span></span></li>
<li><span data-ttu-id="746e2-200">可以儲存</span><span class="sxs-lookup"><span data-stu-id="746e2-200">can save</span></span></li>
<li><span data-ttu-id="746e2-201">CAV</span><span class="sxs-lookup"><span data-stu-id="746e2-201">CAV</span></span></li>
<li><span data-ttu-id="746e2-202">CLV</span><span class="sxs-lookup"><span data-stu-id="746e2-202">CLV</span></span></li>
<li><span data-ttu-id="746e2-203">複合裝置</span><span class="sxs-lookup"><span data-stu-id="746e2-203">compound device</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="746e2-204">裝置類型</span><span class="sxs-lookup"><span data-stu-id="746e2-204">device type</span></span></li>
<li><span data-ttu-id="746e2-205">快速播放速率</span><span class="sxs-lookup"><span data-stu-id="746e2-205">fast play rate</span></span></li>
<li><span data-ttu-id="746e2-206">有音訊</span><span class="sxs-lookup"><span data-stu-id="746e2-206">has audio</span></span></li>
<li><span data-ttu-id="746e2-207">有影片</span><span class="sxs-lookup"><span data-stu-id="746e2-207">has video</span></span></li>
<li><span data-ttu-id="746e2-208">正常播放率</span><span class="sxs-lookup"><span data-stu-id="746e2-208">normal play rate</span></span></li>
<li><span data-ttu-id="746e2-209">緩慢的播放率</span><span class="sxs-lookup"><span data-stu-id="746e2-209">slow play rate</span></span></li>
<li><span data-ttu-id="746e2-210">使用檔案</span><span class="sxs-lookup"><span data-stu-id="746e2-210">uses files</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="746e2-211">waveaudio</span><span class="sxs-lookup"><span data-stu-id="746e2-211">waveaudio</span></span></td>
<td><ul>
<li><span data-ttu-id="746e2-212">可以退出</span><span class="sxs-lookup"><span data-stu-id="746e2-212">can eject</span></span></li>
<li><span data-ttu-id="746e2-213">可以播放</span><span class="sxs-lookup"><span data-stu-id="746e2-213">can play</span></span></li>
<li><span data-ttu-id="746e2-214">可以記錄</span><span class="sxs-lookup"><span data-stu-id="746e2-214">can record</span></span></li>
<li><span data-ttu-id="746e2-215">可以儲存</span><span class="sxs-lookup"><span data-stu-id="746e2-215">can save</span></span></li>
<li><span data-ttu-id="746e2-216">複合裝置</span><span class="sxs-lookup"><span data-stu-id="746e2-216">compound device</span></span></li>
<li><span data-ttu-id="746e2-217">裝置類型</span><span class="sxs-lookup"><span data-stu-id="746e2-217">device type</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="746e2-218">有音訊</span><span class="sxs-lookup"><span data-stu-id="746e2-218">has audio</span></span></li>
<li><span data-ttu-id="746e2-219">有影片</span><span class="sxs-lookup"><span data-stu-id="746e2-219">has video</span></span></li>
<li><span data-ttu-id="746e2-220">輸入</span><span class="sxs-lookup"><span data-stu-id="746e2-220">inputs</span></span></li>
<li><span data-ttu-id="746e2-221">輸出</span><span class="sxs-lookup"><span data-stu-id="746e2-221">outputs</span></span></li>
<li><span data-ttu-id="746e2-222">使用檔案</span><span class="sxs-lookup"><span data-stu-id="746e2-222">uses files</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="746e2-223">下表列出可在 *lpszRequest* 參數中指定的旗標，以及它們的意義：</span><span class="sxs-lookup"><span data-stu-id="746e2-223">The following table lists the flags that can be specified in the *lpszRequest* parameter and their meanings:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="746e2-224">Flags</span><span class="sxs-lookup"><span data-stu-id="746e2-224">Flags</span></span></th>
<th><span data-ttu-id="746e2-225">意義</span><span class="sxs-lookup"><span data-stu-id="746e2-225">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="746e2-226">可以偵測長度</span><span class="sxs-lookup"><span data-stu-id="746e2-226">can detect length</span></span></td>
<td><span data-ttu-id="746e2-227">如果裝置可以偵測出媒體的長度，則傳回 <strong>TRUE</strong> 。</span><span class="sxs-lookup"><span data-stu-id="746e2-227">Returns <strong>TRUE</strong> if the device can detect the length of the media.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="746e2-228">可以退出</span><span class="sxs-lookup"><span data-stu-id="746e2-228">can eject</span></span></td>
<td><span data-ttu-id="746e2-229">如果裝置可以退出媒體，則傳回 <strong>TRUE</strong> 。</span><span class="sxs-lookup"><span data-stu-id="746e2-229">Returns <strong>TRUE</strong> if the device can eject the media.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="746e2-230">可以凍結</span><span class="sxs-lookup"><span data-stu-id="746e2-230">can freeze</span></span></td>
<td><span data-ttu-id="746e2-231">如果裝置可以凍結框架緩衝區中的資料，則傳回 <strong>TRUE</strong> 。</span><span class="sxs-lookup"><span data-stu-id="746e2-231">Returns <strong>TRUE</strong> if the device can freeze data in the frame buffer.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="746e2-232">可以鎖定</span><span class="sxs-lookup"><span data-stu-id="746e2-232">can lock</span></span></td>
<td><span data-ttu-id="746e2-233">如果裝置可以鎖定資料，則傳回 <strong>TRUE</strong> 。</span><span class="sxs-lookup"><span data-stu-id="746e2-233">Returns <strong>TRUE</strong> if the device can lock data.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="746e2-234">可以監視來源</span><span class="sxs-lookup"><span data-stu-id="746e2-234">can monitor sources</span></span></td>
<td><span data-ttu-id="746e2-235">如果裝置可將輸入 (來源) 傳遞至受監視的輸出，而不是目前的輸入選取範圍，則傳回 <strong>TRUE</strong> 。</span><span class="sxs-lookup"><span data-stu-id="746e2-235">Returns <strong>TRUE</strong> if the device can pass an input (source) to the monitored output, independent of the current input selection.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="746e2-236">可以播放</span><span class="sxs-lookup"><span data-stu-id="746e2-236">can play</span></span></td>
<td><span data-ttu-id="746e2-237">如果裝置可以播放，則傳回 <strong>TRUE</strong> 。</span><span class="sxs-lookup"><span data-stu-id="746e2-237">Returns <strong>TRUE</strong> if the device can play.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="746e2-238">可以預先進行</span><span class="sxs-lookup"><span data-stu-id="746e2-238">can preroll</span></span></td>
<td><span data-ttu-id="746e2-239">如果<strong></strong>裝置支援 &quot; &quot; 使用<a href="cue.md">提示</a>命令的預先處理旗標，則傳回 TRUE。</span><span class="sxs-lookup"><span data-stu-id="746e2-239">Returns <strong>TRUE</strong> if the device supports the &quot;preroll&quot; flag with the <a href="cue.md">cue</a> command.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="746e2-240">可以預覽</span><span class="sxs-lookup"><span data-stu-id="746e2-240">can preview</span></span></td>
<td><span data-ttu-id="746e2-241">如果裝置支援預覽，則傳回 <strong>TRUE</strong> 。</span><span class="sxs-lookup"><span data-stu-id="746e2-241">Returns <strong>TRUE</strong> if the device supports previews.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="746e2-242">可以記錄</span><span class="sxs-lookup"><span data-stu-id="746e2-242">can record</span></span></td>
<td><span data-ttu-id="746e2-243">如果裝置支援錄製，則傳回 <strong>TRUE</strong> 。</span><span class="sxs-lookup"><span data-stu-id="746e2-243">Returns <strong>TRUE</strong> if the device supports recording.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="746e2-244">可以反轉</span><span class="sxs-lookup"><span data-stu-id="746e2-244">can reverse</span></span></td>
<td><span data-ttu-id="746e2-245">如果裝置可以反向播放，則傳回 <strong>TRUE</strong> 。</span><span class="sxs-lookup"><span data-stu-id="746e2-245">Returns <strong>TRUE</strong> if the device can play in reverse.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="746e2-246">可以儲存</span><span class="sxs-lookup"><span data-stu-id="746e2-246">can save</span></span></td>
<td><span data-ttu-id="746e2-247">如果裝置可以儲存資料，則傳回 <strong>TRUE</strong> 。</span><span class="sxs-lookup"><span data-stu-id="746e2-247">Returns <strong>TRUE</strong> if the device can save data.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="746e2-248">可以延展</span><span class="sxs-lookup"><span data-stu-id="746e2-248">can stretch</span></span></td>
<td><span data-ttu-id="746e2-249">如果裝置可以延展框架以填滿指定的顯示矩形，則傳回 <strong>TRUE</strong> 。</span><span class="sxs-lookup"><span data-stu-id="746e2-249">Returns <strong>TRUE</strong> if the device can stretch frames to fill a given display rectangle.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="746e2-250">可延展輸入</span><span class="sxs-lookup"><span data-stu-id="746e2-250">can stretch input</span></span></td>
<td><span data-ttu-id="746e2-251">如果裝置可以在將影像數位化至框架緩衝區的過程中調整影像的大小，則會傳回 <strong>TRUE</strong> 。</span><span class="sxs-lookup"><span data-stu-id="746e2-251">Returns <strong>TRUE</strong> if the device can resize an image in the process of digitizing it into the frame buffer.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="746e2-252">可以測試</span><span class="sxs-lookup"><span data-stu-id="746e2-252">can test</span></span></td>
<td><span data-ttu-id="746e2-253">如果裝置辨識 test 關鍵字，則傳回 <strong>TRUE</strong> 。</span><span class="sxs-lookup"><span data-stu-id="746e2-253">Returns <strong>TRUE</strong> if the device recognizes the test keyword.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="746e2-254">cav</span><span class="sxs-lookup"><span data-stu-id="746e2-254">cav</span></span></td>
<td><span data-ttu-id="746e2-255">此旗標與其他專案結合時，會指定傳回信息適用于 CAV 格式 videodiscs。</span><span class="sxs-lookup"><span data-stu-id="746e2-255">When combined with other items, this flag specifies that the return information applies to CAV format videodiscs.</span></span> <span data-ttu-id="746e2-256">如果未插入任何 videodisc，則這是預設值。</span><span class="sxs-lookup"><span data-stu-id="746e2-256">This is the default if no videodisc is inserted.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="746e2-257">頻率遞增率</span><span class="sxs-lookup"><span data-stu-id="746e2-257">clock increment rate</span></span></td>
<td><span data-ttu-id="746e2-258">傳回外部時鐘每秒支援的分割數目。</span><span class="sxs-lookup"><span data-stu-id="746e2-258">Returns the number of subdivisions the external clock supports per second.</span></span> <span data-ttu-id="746e2-259">如果外部時鐘為毫秒時鐘，則傳回值為1000。</span><span class="sxs-lookup"><span data-stu-id="746e2-259">If the external clock is a millisecond clock, the return value is 1000.</span></span> <span data-ttu-id="746e2-260">如果傳回值為0，則不支援時鐘。</span><span class="sxs-lookup"><span data-stu-id="746e2-260">If the return value is 0, no clock is supported.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="746e2-261">clv</span><span class="sxs-lookup"><span data-stu-id="746e2-261">clv</span></span></td>
<td><span data-ttu-id="746e2-262">此旗標與其他專案結合時，會指定傳回信息適用于 CLV 格式 videodiscs。</span><span class="sxs-lookup"><span data-stu-id="746e2-262">When combined with other items, this flag specifies that the return information applies to CLV format videodiscs.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="746e2-263">複合裝置</span><span class="sxs-lookup"><span data-stu-id="746e2-263">compound device</span></span></td>
<td><span data-ttu-id="746e2-264">如果裝置支援 (檔案名) 的元素名稱，則傳回 <strong>TRUE</strong> 。</span><span class="sxs-lookup"><span data-stu-id="746e2-264">Returns <strong>TRUE</strong> if the device supports an element name (filename).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="746e2-265">裝置類型</span><span class="sxs-lookup"><span data-stu-id="746e2-265">device type</span></span></td>
<td><span data-ttu-id="746e2-266">傳回裝置類型名稱，此名稱可以是下列其中一項：</span><span class="sxs-lookup"><span data-stu-id="746e2-266">Returns a device type name, which can be one of the following:</span></span>
<ul>
<li><span data-ttu-id="746e2-267">cdaudio</span><span class="sxs-lookup"><span data-stu-id="746e2-267">cdaudio</span></span></li>
<li><span data-ttu-id="746e2-268">Dat</span><span class="sxs-lookup"><span data-stu-id="746e2-268">dat</span></span></li>
<li><span data-ttu-id="746e2-269">digitalvideo</span><span class="sxs-lookup"><span data-stu-id="746e2-269">digitalvideo</span></span></li>
<li><span data-ttu-id="746e2-270">其他</span><span class="sxs-lookup"><span data-stu-id="746e2-270">other</span></span></li>
<li><span data-ttu-id="746e2-271">overlay</span><span class="sxs-lookup"><span data-stu-id="746e2-271">overlay</span></span></li>
<li><span data-ttu-id="746e2-272">掃描器</span><span class="sxs-lookup"><span data-stu-id="746e2-272">scanner</span></span></li>
<li><span data-ttu-id="746e2-273">排序器</span><span class="sxs-lookup"><span data-stu-id="746e2-273">sequencer</span></span></li>
<li><span data-ttu-id="746e2-274">錄影機</span><span class="sxs-lookup"><span data-stu-id="746e2-274">vcr</span></span></li>
<li><span data-ttu-id="746e2-275">videodisc</span><span class="sxs-lookup"><span data-stu-id="746e2-275">videodisc</span></span></li>
<li><span data-ttu-id="746e2-276">waveaudio</span><span class="sxs-lookup"><span data-stu-id="746e2-276">waveaudio</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="746e2-277">快速播放速率</span><span class="sxs-lookup"><span data-stu-id="746e2-277">fast play rate</span></span></td>
<td><span data-ttu-id="746e2-278">傳回每秒畫面格的快速播放速率，如果裝置無法快速播放，則為零。</span><span class="sxs-lookup"><span data-stu-id="746e2-278">Returns the fast play rate in frames per second, or zero if the device cannot play fast.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="746e2-279">有音訊</span><span class="sxs-lookup"><span data-stu-id="746e2-279">has audio</span></span></td>
<td><span data-ttu-id="746e2-280">如果裝置支援音訊播放，則傳回 <strong>TRUE</strong> 。</span><span class="sxs-lookup"><span data-stu-id="746e2-280">Returns <strong>TRUE</strong> if the device supports audio playback.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="746e2-281">具有時鐘</span><span class="sxs-lookup"><span data-stu-id="746e2-281">has clock</span></span></td>
<td><span data-ttu-id="746e2-282">如果裝置具有時鐘，則傳回 <strong>TRUE</strong> 。</span><span class="sxs-lookup"><span data-stu-id="746e2-282">Returns <strong>TRUE</strong> if the device has a clock.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="746e2-283">仍有</span><span class="sxs-lookup"><span data-stu-id="746e2-283">has still</span></span></td>
<td><span data-ttu-id="746e2-284">如果裝置以比動畫影片檔案更有效率的方式來處理具有單一影像的檔案，則會傳回 <strong>TRUE</strong> 。</span><span class="sxs-lookup"><span data-stu-id="746e2-284">Returns <strong>TRUE</strong> if the device treats files with a single image more efficiently than motion video files.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="746e2-285">有時間碼</span><span class="sxs-lookup"><span data-stu-id="746e2-285">has timecode</span></span></td>
<td><span data-ttu-id="746e2-286">如果裝置能夠支援時間碼或不明，則傳回 <strong>TRUE</strong> 。</span><span class="sxs-lookup"><span data-stu-id="746e2-286">Returns <strong>TRUE</strong> if the device is capable of supporting timecode, or if it is unknown.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="746e2-287">有影片</span><span class="sxs-lookup"><span data-stu-id="746e2-287">has video</span></span></td>
<td><span data-ttu-id="746e2-288">如果裝置支援影片，則傳回 <strong>TRUE</strong> 。</span><span class="sxs-lookup"><span data-stu-id="746e2-288">Returns <strong>TRUE</strong> if the device supports video.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="746e2-289">輸入</span><span class="sxs-lookup"><span data-stu-id="746e2-289">inputs</span></span></td>
<td><span data-ttu-id="746e2-290">傳回輸入裝置的總數。</span><span class="sxs-lookup"><span data-stu-id="746e2-290">Returns the total number of input devices.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="746e2-291">最大播放率</span><span class="sxs-lookup"><span data-stu-id="746e2-291">maximum play rate</span></span></td>
<td><span data-ttu-id="746e2-292">傳回裝置的最大播放速率（以每秒畫面數為單位）。</span><span class="sxs-lookup"><span data-stu-id="746e2-292">Returns the maximum play rate, in frames per second, for the device.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="746e2-293">最小播放率</span><span class="sxs-lookup"><span data-stu-id="746e2-293">minimum play rate</span></span></td>
<td><span data-ttu-id="746e2-294">傳回裝置的最小播放速率（以每秒畫面數為單位）。</span><span class="sxs-lookup"><span data-stu-id="746e2-294">Returns the minimum play rate, in frames per second, for the device.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="746e2-295">正常播放率</span><span class="sxs-lookup"><span data-stu-id="746e2-295">normal play rate</span></span></td>
<td><span data-ttu-id="746e2-296">傳回裝置的正常播放速率（以每秒畫面格為單位）。</span><span class="sxs-lookup"><span data-stu-id="746e2-296">Returns the normal play rate, in frames per second, for the device.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="746e2-297">標記數目</span><span class="sxs-lookup"><span data-stu-id="746e2-297">number of marks</span></span></td>
<td><span data-ttu-id="746e2-298">傳回可使用的標記數目上限;零表示不支援標記。</span><span class="sxs-lookup"><span data-stu-id="746e2-298">Returns the maximum number of marks that can be used; zero indicates that marks are unsupported.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="746e2-299">輸出</span><span class="sxs-lookup"><span data-stu-id="746e2-299">outputs</span></span></td>
<td><span data-ttu-id="746e2-300">傳回輸出裝置的總數。</span><span class="sxs-lookup"><span data-stu-id="746e2-300">Returns the total number of output devices.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="746e2-301">搜尋精確度</span><span class="sxs-lookup"><span data-stu-id="746e2-301">seek accuracy</span></span></td>
<td><span data-ttu-id="746e2-302">傳回框架中搜尋的預期精確度;0表示裝置為框架正確，1表示裝置預期會在指定搜尋位置的某個畫面中，依此類推。</span><span class="sxs-lookup"><span data-stu-id="746e2-302">Returns the expected accuracy of a search in frames; 0 indicates that the device is frame accurate, 1 indicates that the device expects to be within one frame of the indicated seek position, and so on.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="746e2-303">緩慢的播放率</span><span class="sxs-lookup"><span data-stu-id="746e2-303">slow play rate</span></span></td>
<td><span data-ttu-id="746e2-304">傳回每秒畫面格的慢速播放速率，如果裝置無法慢慢播放則傳回零。</span><span class="sxs-lookup"><span data-stu-id="746e2-304">Returns the slow play rate in frames per second, or zero if the device cannot play slowly.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="746e2-305">使用檔案</span><span class="sxs-lookup"><span data-stu-id="746e2-305">uses files</span></span></td>
<td><span data-ttu-id="746e2-306">如果複合裝置使用的資料存放區是檔案，則傳回 <strong>TRUE</strong> 。</span><span class="sxs-lookup"><span data-stu-id="746e2-306">Returns <strong>TRUE</strong> if the data storage used by a compound device is a file.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="746e2-307">使用調色板</span><span class="sxs-lookup"><span data-stu-id="746e2-307">uses palettes</span></span></td>
<td><span data-ttu-id="746e2-308">如果裝置使用調色板，則傳回 <strong>TRUE</strong> 。</span><span class="sxs-lookup"><span data-stu-id="746e2-308">Returns <strong>TRUE</strong> if the device uses palettes.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="746e2-309">windows</span><span class="sxs-lookup"><span data-stu-id="746e2-309">windows</span></span></td>
<td><span data-ttu-id="746e2-310">傳回裝置可支援的同時顯示視窗數目。</span><span class="sxs-lookup"><span data-stu-id="746e2-310">Returns the number of simultaneous display windows the device can support.</span></span></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="746e2-311"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="746e2-311"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="746e2-312">可以是「等候」、「通知」或兩者。</span><span class="sxs-lookup"><span data-stu-id="746e2-312">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="746e2-313">針對數位影片和 VCR 裝置，也可以指定「測試」。</span><span class="sxs-lookup"><span data-stu-id="746e2-313">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="746e2-314">如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。</span><span class="sxs-lookup"><span data-stu-id="746e2-314">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="746e2-315">傳回值</span><span class="sxs-lookup"><span data-stu-id="746e2-315">Return Value</span></span>

<span data-ttu-id="746e2-316">傳回 [**mciSendString**](/previous-versions//dd757161(v=vs.85))函數的 *lpszReturnString* 參數中的資訊。</span><span class="sxs-lookup"><span data-stu-id="746e2-316">Returns information in the *lpszReturnString* parameter of the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function.</span></span> <span data-ttu-id="746e2-317">此資訊取決於要求類型。</span><span class="sxs-lookup"><span data-stu-id="746e2-317">The information is dependent on the request type.</span></span>

## <a name="examples"></a><span data-ttu-id="746e2-318">範例</span><span class="sxs-lookup"><span data-stu-id="746e2-318">Examples</span></span>

<span data-ttu-id="746e2-319">下列命令會傳回 "mysound" 裝置的裝置類型。</span><span class="sxs-lookup"><span data-stu-id="746e2-319">The following command returns the device type of the "mysound" device.</span></span>

``` syntax
capability mysound device type
```

## <a name="requirements"></a><span data-ttu-id="746e2-320">規格需求</span><span class="sxs-lookup"><span data-stu-id="746e2-320">Requirements</span></span>



| <span data-ttu-id="746e2-321">需求</span><span class="sxs-lookup"><span data-stu-id="746e2-321">Requirement</span></span> | <span data-ttu-id="746e2-322">值</span><span class="sxs-lookup"><span data-stu-id="746e2-322">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="746e2-323">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="746e2-323">Minimum supported client</span></span><br/> | <span data-ttu-id="746e2-324">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="746e2-324">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="746e2-325">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="746e2-325">Minimum supported server</span></span><br/> | <span data-ttu-id="746e2-326">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="746e2-326">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="746e2-327">另請參閱</span><span class="sxs-lookup"><span data-stu-id="746e2-327">See also</span></span>

<dl> <dt>

[<span data-ttu-id="746e2-328">Mci</span><span class="sxs-lookup"><span data-stu-id="746e2-328">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="746e2-329">MCI 命令字串</span><span class="sxs-lookup"><span data-stu-id="746e2-329">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="746e2-330">提示</span><span class="sxs-lookup"><span data-stu-id="746e2-330">cue</span></span>](cue.md)
</dt> </dl>

 

