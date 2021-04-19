---
title: status 命令
description: Status 命令會要求來自裝置的狀態資訊。 所有裝置都會辨識此命令。
ms.assetid: 39961bd7-866d-450d-9fbf-347a8f508481
keywords:
- 狀態命令 Windows 多媒體
topic_type:
- apiref
api_name:
- status
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14ab184ddaca16d0ea96b86a6b062f1e66e2eee2
ms.sourcegitcommit: 8276af9231bdbf5a7334299f0d13fc8ff069a065
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/12/2021
ms.locfileid: "106997289"
---
# <a name="status-command"></a><span data-ttu-id="c37e2-105">status 命令</span><span class="sxs-lookup"><span data-stu-id="c37e2-105">status command</span></span>

> [!NOTE]
> <span data-ttu-id="c37e2-106">無偏差的通訊-Microsoft 支援多樣化且 inclusionary 的環境。</span><span class="sxs-lookup"><span data-stu-id="c37e2-106">Bias-free Communication Microsoft supports a diverse and inclusionary environment.</span></span>  <span data-ttu-id="c37e2-107">本檔中有 ' 從屬 ' 這個字的參考。</span><span class="sxs-lookup"><span data-stu-id="c37e2-107">Within this document, there are references to the word 'slave.'</span></span> <span data-ttu-id="c37e2-108">Microsoft 的 [Bias-Free 通訊樣式指南](https://github.com/MicrosoftDocs/microsoft-style-guide/blob/master/styleguide/bias-free-communication.md) 會將此視為排他性行為單字。</span><span class="sxs-lookup"><span data-stu-id="c37e2-108">Microsoft's [Style Guide for Bias-Free Communications](https://github.com/MicrosoftDocs/microsoft-style-guide/blob/master/styleguide/bias-free-communication.md) recognizes this as an exclusionary word.</span></span>  <span data-ttu-id="c37e2-109">這種用語是用來做為命令內所使用的用語。</span><span class="sxs-lookup"><span data-stu-id="c37e2-109">This wording is used as it is currently the wording used within the commands.</span></span> <span data-ttu-id="c37e2-110">為求一致，本檔包含此字。</span><span class="sxs-lookup"><span data-stu-id="c37e2-110">For consistency, this document contains this word.</span></span> <span data-ttu-id="c37e2-111">當您在命令中更改這個字時，我們會將此檔修正為一致。</span><span class="sxs-lookup"><span data-stu-id="c37e2-111">When this word is altered in the commands, we will correct this document to be in alignment.</span></span>

<span data-ttu-id="c37e2-112">Status 命令會要求來自裝置的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="c37e2-112">The status command requests status information from a device.</span></span> <span data-ttu-id="c37e2-113">所有裝置都會辨識此命令。</span><span class="sxs-lookup"><span data-stu-id="c37e2-113">All devices recognize this command.</span></span>

<span data-ttu-id="c37e2-114">若要傳送此命令，請使用 *lpszCommand* 參數設定來呼叫 [**mciSendString**](/previous-versions//dd757161(v=vs.85))函式，如下所示。</span><span class="sxs-lookup"><span data-stu-id="c37e2-114">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand,
  TEXT("status %s %s %s"),
  lpszDeviceID,
  lpszRequest,
  lpszFlags
);
      
```

## <a name="parameters"></a><span data-ttu-id="c37e2-115">參數</span><span class="sxs-lookup"><span data-stu-id="c37e2-115">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c37e2-116"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="c37e2-116"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="c37e2-117">MCI 裝置的識別碼。</span><span class="sxs-lookup"><span data-stu-id="c37e2-117">Identifier of an MCI device.</span></span> <span data-ttu-id="c37e2-118">開啟裝置時，會指派此識別碼或別名。</span><span class="sxs-lookup"><span data-stu-id="c37e2-118">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="c37e2-119"><span id="lpszRequest"></span><span id="lpszrequest"></span><span id="LPSZREQUEST"></span>*lpszRequest*</span><span class="sxs-lookup"><span data-stu-id="c37e2-119"><span id="lpszRequest"></span><span id="lpszrequest"></span><span id="LPSZREQUEST"></span>*lpszRequest*</span></span>
</dt> <dd>

<span data-ttu-id="c37e2-120">要求狀態資訊的旗標。</span><span class="sxs-lookup"><span data-stu-id="c37e2-120">Flag for requesting status information.</span></span> <span data-ttu-id="c37e2-121">下表列出可辨識 **status** 命令的裝置類型，以及每種類型所使用的旗標。</span><span class="sxs-lookup"><span data-stu-id="c37e2-121">The following table lists device types that recognize the **status** command and the flags used by each type.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c37e2-122">裝置類型</span><span class="sxs-lookup"><span data-stu-id="c37e2-122">Device Type</span></span></th>
<th><span data-ttu-id="c37e2-123">要求旗標</span><span class="sxs-lookup"><span data-stu-id="c37e2-123">Request Flags</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c37e2-124">cdaudio</span><span class="sxs-lookup"><span data-stu-id="c37e2-124">cdaudio</span></span></td>
<td><ul>
<li><span data-ttu-id="c37e2-125">cdaudio 類型追蹤 <em>編號</em></span><span class="sxs-lookup"><span data-stu-id="c37e2-125">cdaudio type track <em>number</em></span></span></li>
<li><span data-ttu-id="c37e2-126">目前的曲目</span><span class="sxs-lookup"><span data-stu-id="c37e2-126">current track</span></span></li>
<li><span data-ttu-id="c37e2-127">長度</span><span class="sxs-lookup"><span data-stu-id="c37e2-127">length</span></span></li>
<li><span data-ttu-id="c37e2-128">長度追蹤 <em>號碼</em></span><span class="sxs-lookup"><span data-stu-id="c37e2-128">length track <em>number</em></span></span></li>
<li><span data-ttu-id="c37e2-129">媒體存在</span><span class="sxs-lookup"><span data-stu-id="c37e2-129">media present</span></span></li>
<li><span data-ttu-id="c37e2-130">mode</span><span class="sxs-lookup"><span data-stu-id="c37e2-130">mode</span></span></li>
<li><span data-ttu-id="c37e2-131">曲目數</span><span class="sxs-lookup"><span data-stu-id="c37e2-131">number of tracks</span></span></li>
<li><span data-ttu-id="c37e2-132">position</span><span class="sxs-lookup"><span data-stu-id="c37e2-132">position</span></span></li>
<li><span data-ttu-id="c37e2-133">位置曲目 <em>編號</em></span><span class="sxs-lookup"><span data-stu-id="c37e2-133">position track <em>number</em></span></span></li>
<li><span data-ttu-id="c37e2-134">準備</span><span class="sxs-lookup"><span data-stu-id="c37e2-134">ready</span></span></li>
<li><span data-ttu-id="c37e2-135">開始位置</span><span class="sxs-lookup"><span data-stu-id="c37e2-135">start position</span></span></li>
<li><span data-ttu-id="c37e2-136">時間格式</span><span class="sxs-lookup"><span data-stu-id="c37e2-136">time format</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c37e2-137">digitalvideo</span><span class="sxs-lookup"><span data-stu-id="c37e2-137">digitalvideo</span></span></td>
<td><ul>
<li><span data-ttu-id="c37e2-138">音訊</span><span class="sxs-lookup"><span data-stu-id="c37e2-138">audio</span></span></li>
<li><span data-ttu-id="c37e2-139">音訊對齊</span><span class="sxs-lookup"><span data-stu-id="c37e2-139">audio alignment</span></span></li>
<li><span data-ttu-id="c37e2-140">音訊 bitspersample</span><span class="sxs-lookup"><span data-stu-id="c37e2-140">audio bitspersample</span></span></li>
<li><span data-ttu-id="c37e2-141">音訊中斷</span><span class="sxs-lookup"><span data-stu-id="c37e2-141">audio breaks</span></span></li>
<li><span data-ttu-id="c37e2-142">音訊 bytespersec</span><span class="sxs-lookup"><span data-stu-id="c37e2-142">audio bytespersec</span></span></li>
<li><span data-ttu-id="c37e2-143">音訊輸入</span><span class="sxs-lookup"><span data-stu-id="c37e2-143">audio input</span></span></li>
<li><span data-ttu-id="c37e2-144">音訊記錄</span><span class="sxs-lookup"><span data-stu-id="c37e2-144">audio record</span></span></li>
<li><span data-ttu-id="c37e2-145">音訊來源</span><span class="sxs-lookup"><span data-stu-id="c37e2-145">audio source</span></span></li>
<li><span data-ttu-id="c37e2-146">音訊 samplespersec</span><span class="sxs-lookup"><span data-stu-id="c37e2-146">audio samplespersec</span></span></li>
<li><span data-ttu-id="c37e2-147">音訊串流</span><span class="sxs-lookup"><span data-stu-id="c37e2-147">audio stream</span></span></li>
<li><span data-ttu-id="c37e2-148">低音</span><span class="sxs-lookup"><span data-stu-id="c37e2-148">bass</span></span></li>
<li><span data-ttu-id="c37e2-149">bitsperpel</span><span class="sxs-lookup"><span data-stu-id="c37e2-149">bitsperpel</span></span></li>
<li><span data-ttu-id="c37e2-150">亮度</span><span class="sxs-lookup"><span data-stu-id="c37e2-150">brightness</span></span></li>
<li><span data-ttu-id="c37e2-151">color</span><span class="sxs-lookup"><span data-stu-id="c37e2-151">color</span></span></li>
<li><span data-ttu-id="c37e2-152">對比</span><span class="sxs-lookup"><span data-stu-id="c37e2-152">contrast</span></span></li>
<li><span data-ttu-id="c37e2-153">目前的曲目</span><span class="sxs-lookup"><span data-stu-id="c37e2-153">current track</span></span></li>
<li><span data-ttu-id="c37e2-154">磁碟空間磁片 <em>磁碟機</em></span><span class="sxs-lookup"><span data-stu-id="c37e2-154">disk space <em>drive</em></span></span></li>
<li><span data-ttu-id="c37e2-155">檔案完成</span><span class="sxs-lookup"><span data-stu-id="c37e2-155">file completion</span></span></li>
<li><span data-ttu-id="c37e2-156">檔案格式</span><span class="sxs-lookup"><span data-stu-id="c37e2-156">file format</span></span></li>
<li><span data-ttu-id="c37e2-157">檔案模式</span><span class="sxs-lookup"><span data-stu-id="c37e2-157">file mode</span></span></li>
<li><span data-ttu-id="c37e2-158">forward</span><span class="sxs-lookup"><span data-stu-id="c37e2-158">forward</span></span></li>
<li><span data-ttu-id="c37e2-159">略過框架</span><span class="sxs-lookup"><span data-stu-id="c37e2-159">frames skipped</span></span></li>
<li><span data-ttu-id="c37e2-160">gamma</span><span class="sxs-lookup"><span data-stu-id="c37e2-160">gamma</span></span></li>
<li><span data-ttu-id="c37e2-161">input</span><span class="sxs-lookup"><span data-stu-id="c37e2-161">input</span></span></li>
<li><span data-ttu-id="c37e2-162">左方磁片區</span><span class="sxs-lookup"><span data-stu-id="c37e2-162">left volume</span></span></li>
<li><span data-ttu-id="c37e2-163">長度</span><span class="sxs-lookup"><span data-stu-id="c37e2-163">length</span></span></li>
<li><span data-ttu-id="c37e2-164">長度追蹤 <em>號碼</em></span><span class="sxs-lookup"><span data-stu-id="c37e2-164">length track <em>number</em></span></span></li>
<li><span data-ttu-id="c37e2-165">媒體存在</span><span class="sxs-lookup"><span data-stu-id="c37e2-165">media present</span></span></li>
<li><span data-ttu-id="c37e2-166">mode</span><span class="sxs-lookup"><span data-stu-id="c37e2-166">mode</span></span></li>
<li><span data-ttu-id="c37e2-167">monitor</span><span class="sxs-lookup"><span data-stu-id="c37e2-167">monitor</span></span></li>
<li><span data-ttu-id="c37e2-168">監視方法</span><span class="sxs-lookup"><span data-stu-id="c37e2-168">monitor method</span></span></li>
<li><span data-ttu-id="c37e2-169">名義</span><span class="sxs-lookup"><span data-stu-id="c37e2-169">nominal</span></span></li>
<li><span data-ttu-id="c37e2-170">名義畫面播放速率</span><span class="sxs-lookup"><span data-stu-id="c37e2-170">nominal frame rate</span></span></li>
<li><span data-ttu-id="c37e2-171">名義記錄畫面播放速率</span><span class="sxs-lookup"><span data-stu-id="c37e2-171">nominal record frame rate</span></span></li>
<li><span data-ttu-id="c37e2-172">曲目數</span><span class="sxs-lookup"><span data-stu-id="c37e2-172">number of tracks</span></span></li>
<li><span data-ttu-id="c37e2-173">output</span><span class="sxs-lookup"><span data-stu-id="c37e2-173">output</span></span></li>
<li><span data-ttu-id="c37e2-174">調色板控制碼</span><span class="sxs-lookup"><span data-stu-id="c37e2-174">palette handle</span></span></li>
<li><span data-ttu-id="c37e2-175">暫停模式</span><span class="sxs-lookup"><span data-stu-id="c37e2-175">pause mode</span></span></li>
<li><span data-ttu-id="c37e2-176">播放速度</span><span class="sxs-lookup"><span data-stu-id="c37e2-176">play speed</span></span></li>
<li><span data-ttu-id="c37e2-177">position</span><span class="sxs-lookup"><span data-stu-id="c37e2-177">position</span></span></li>
<li><span data-ttu-id="c37e2-178">位置曲目 <em>編號</em></span><span class="sxs-lookup"><span data-stu-id="c37e2-178">position track <em>number</em></span></span></li>
<li><span data-ttu-id="c37e2-179">準備</span><span class="sxs-lookup"><span data-stu-id="c37e2-179">ready</span></span></li>
<li><span data-ttu-id="c37e2-180">記錄畫面播放速率</span><span class="sxs-lookup"><span data-stu-id="c37e2-180">record frame rate</span></span></li>
<li><span data-ttu-id="c37e2-181">參考 <em>框架</em></span><span class="sxs-lookup"><span data-stu-id="c37e2-181">reference <em>frame</em></span></span></li>
<li><span data-ttu-id="c37e2-182">保留大小</span><span class="sxs-lookup"><span data-stu-id="c37e2-182">reserved size</span></span></li>
<li><span data-ttu-id="c37e2-183">右磁片區</span><span class="sxs-lookup"><span data-stu-id="c37e2-183">right volume</span></span></li>
<li><span data-ttu-id="c37e2-184">確切搜尋</span><span class="sxs-lookup"><span data-stu-id="c37e2-184">seek exactly</span></span></li>
<li><span data-ttu-id="c37e2-185">清晰度</span><span class="sxs-lookup"><span data-stu-id="c37e2-185">sharpness</span></span></li>
<li><span data-ttu-id="c37e2-186">smpte</span><span class="sxs-lookup"><span data-stu-id="c37e2-186">smpte</span></span></li>
<li><span data-ttu-id="c37e2-187">速度</span><span class="sxs-lookup"><span data-stu-id="c37e2-187">speed</span></span></li>
<li><span data-ttu-id="c37e2-188">開始位置</span><span class="sxs-lookup"><span data-stu-id="c37e2-188">start position</span></span></li>
<li><span data-ttu-id="c37e2-189">仍為檔案格式</span><span class="sxs-lookup"><span data-stu-id="c37e2-189">still file format</span></span></li>
<li><span data-ttu-id="c37e2-190">時間格式</span><span class="sxs-lookup"><span data-stu-id="c37e2-190">time format</span></span></li>
<li><span data-ttu-id="c37e2-191">色調</span><span class="sxs-lookup"><span data-stu-id="c37e2-191">tint</span></span></li>
<li><span data-ttu-id="c37e2-192">高音</span><span class="sxs-lookup"><span data-stu-id="c37e2-192">treble</span></span></li>
<li><span data-ttu-id="c37e2-193">未儲存</span><span class="sxs-lookup"><span data-stu-id="c37e2-193">unsaved</span></span></li>
<li><span data-ttu-id="c37e2-194">影片</span><span class="sxs-lookup"><span data-stu-id="c37e2-194">video</span></span></li>
<li><span data-ttu-id="c37e2-195">影片索引鍵索引</span><span class="sxs-lookup"><span data-stu-id="c37e2-195">video key index</span></span></li>
<li><span data-ttu-id="c37e2-196">影片按鍵色彩</span><span class="sxs-lookup"><span data-stu-id="c37e2-196">video key color</span></span></li>
<li><span data-ttu-id="c37e2-197">影片記錄</span><span class="sxs-lookup"><span data-stu-id="c37e2-197">video record</span></span></li>
<li><span data-ttu-id="c37e2-198">影片來源</span><span class="sxs-lookup"><span data-stu-id="c37e2-198">video source</span></span></li>
<li><span data-ttu-id="c37e2-199">影片來源編號</span><span class="sxs-lookup"><span data-stu-id="c37e2-199">video source number</span></span></li>
<li><span data-ttu-id="c37e2-200">影片串流</span><span class="sxs-lookup"><span data-stu-id="c37e2-200">video stream</span></span></li>
<li><span data-ttu-id="c37e2-201">磁碟區</span><span class="sxs-lookup"><span data-stu-id="c37e2-201">volume</span></span></li>
<li><span data-ttu-id="c37e2-202">視窗控制碼</span><span class="sxs-lookup"><span data-stu-id="c37e2-202">window handle</span></span></li>
<li><span data-ttu-id="c37e2-203">視窗可見</span><span class="sxs-lookup"><span data-stu-id="c37e2-203">window visible</span></span></li>
<li><span data-ttu-id="c37e2-204">視窗最小化</span><span class="sxs-lookup"><span data-stu-id="c37e2-204">window minimized</span></span></li>
<li><span data-ttu-id="c37e2-205">視窗最大化</span><span class="sxs-lookup"><span data-stu-id="c37e2-205">window maximized</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c37e2-206">overlay</span><span class="sxs-lookup"><span data-stu-id="c37e2-206">overlay</span></span></td>
<td><ul>
<li><span data-ttu-id="c37e2-207">媒體存在</span><span class="sxs-lookup"><span data-stu-id="c37e2-207">media present</span></span></li>
<li><span data-ttu-id="c37e2-208">mode</span><span class="sxs-lookup"><span data-stu-id="c37e2-208">mode</span></span></li>
<li><span data-ttu-id="c37e2-209">曲目數</span><span class="sxs-lookup"><span data-stu-id="c37e2-209">number of tracks</span></span></li>
<li><span data-ttu-id="c37e2-210">準備</span><span class="sxs-lookup"><span data-stu-id="c37e2-210">ready</span></span></li>
<li><span data-ttu-id="c37e2-211">Stretch - 自動縮放</span><span class="sxs-lookup"><span data-stu-id="c37e2-211">stretch</span></span></li>
<li><span data-ttu-id="c37e2-212">視窗控制碼</span><span class="sxs-lookup"><span data-stu-id="c37e2-212">window handle</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c37e2-213">排序器</span><span class="sxs-lookup"><span data-stu-id="c37e2-213">sequencer</span></span></td>
<td><ul>
<li><span data-ttu-id="c37e2-214">目前的曲目</span><span class="sxs-lookup"><span data-stu-id="c37e2-214">current track</span></span></li>
<li><span data-ttu-id="c37e2-215">除法類型</span><span class="sxs-lookup"><span data-stu-id="c37e2-215">division type</span></span></li>
<li><span data-ttu-id="c37e2-216">長度</span><span class="sxs-lookup"><span data-stu-id="c37e2-216">length</span></span></li>
<li><span data-ttu-id="c37e2-217">長度追蹤 <em>號碼</em> 主機</span><span class="sxs-lookup"><span data-stu-id="c37e2-217">length track <em>number</em> master</span></span></li>
<li><span data-ttu-id="c37e2-218">媒體存在</span><span class="sxs-lookup"><span data-stu-id="c37e2-218">media present</span></span></li>
<li><span data-ttu-id="c37e2-219">mode</span><span class="sxs-lookup"><span data-stu-id="c37e2-219">mode</span></span></li>
<li><span data-ttu-id="c37e2-220">曲目數</span><span class="sxs-lookup"><span data-stu-id="c37e2-220">number of tracks</span></span></li>
<li><span data-ttu-id="c37e2-221">Offset</span><span class="sxs-lookup"><span data-stu-id="c37e2-221">offset</span></span></li>
<li><span data-ttu-id="c37e2-222">連接埠</span><span class="sxs-lookup"><span data-stu-id="c37e2-222">port</span></span></li>
<li><span data-ttu-id="c37e2-223">position</span><span class="sxs-lookup"><span data-stu-id="c37e2-223">position</span></span></li>
<li><span data-ttu-id="c37e2-224">位置曲目 <em>編號</em></span><span class="sxs-lookup"><span data-stu-id="c37e2-224">position track <em>number</em></span></span></li>
<li><span data-ttu-id="c37e2-225">準備</span><span class="sxs-lookup"><span data-stu-id="c37e2-225">ready</span></span></li>
<li><span data-ttu-id="c37e2-226">奴隸</span><span class="sxs-lookup"><span data-stu-id="c37e2-226">slave</span></span></li>
<li><span data-ttu-id="c37e2-227">開始位置</span><span class="sxs-lookup"><span data-stu-id="c37e2-227">start position</span></span></li>
<li><span data-ttu-id="c37e2-228">節奏</span><span class="sxs-lookup"><span data-stu-id="c37e2-228">tempo</span></span></li>
<li><span data-ttu-id="c37e2-229">時間格式</span><span class="sxs-lookup"><span data-stu-id="c37e2-229">time format</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c37e2-230">錄影機</span><span class="sxs-lookup"><span data-stu-id="c37e2-230">vcr</span></span></td>
<td><ul>
<li><span data-ttu-id="c37e2-231">組合記錄</span><span class="sxs-lookup"><span data-stu-id="c37e2-231">assemble record</span></span></li>
<li><span data-ttu-id="c37e2-232">音訊監視器</span><span class="sxs-lookup"><span data-stu-id="c37e2-232">audio monitor</span></span></li>
<li><span data-ttu-id="c37e2-233">音訊監視器編號</span><span class="sxs-lookup"><span data-stu-id="c37e2-233">audio monitor number</span></span></li>
<li><span data-ttu-id="c37e2-234">音訊記錄</span><span class="sxs-lookup"><span data-stu-id="c37e2-234">audio record</span></span></li>
<li><span data-ttu-id="c37e2-235">音訊記錄播放軌 <em>編號</em></span><span class="sxs-lookup"><span data-stu-id="c37e2-235">audio record track <em>number</em></span></span></li>
<li><span data-ttu-id="c37e2-236">音訊來源</span><span class="sxs-lookup"><span data-stu-id="c37e2-236">audio source</span></span></li>
<li><span data-ttu-id="c37e2-237">音訊來源編號</span><span class="sxs-lookup"><span data-stu-id="c37e2-237">audio source number</span></span></li>
<li><span data-ttu-id="c37e2-238">通道</span><span class="sxs-lookup"><span data-stu-id="c37e2-238">channel</span></span></li>
<li><span data-ttu-id="c37e2-239">通道調諧器 <em>號碼</em></span><span class="sxs-lookup"><span data-stu-id="c37e2-239">channel tuner <em>number</em></span></span></li>
<li><span data-ttu-id="c37e2-240">時鐘</span><span class="sxs-lookup"><span data-stu-id="c37e2-240">clock</span></span></li>
<li><span data-ttu-id="c37e2-241">時鐘識別碼</span><span class="sxs-lookup"><span data-stu-id="c37e2-241">clock id</span></span></li>
<li><span data-ttu-id="c37e2-242">counter</span><span class="sxs-lookup"><span data-stu-id="c37e2-242">counter</span></span></li>
<li><span data-ttu-id="c37e2-243">計數器格式</span><span class="sxs-lookup"><span data-stu-id="c37e2-243">counter format</span></span></li>
<li><span data-ttu-id="c37e2-244">計數器解析</span><span class="sxs-lookup"><span data-stu-id="c37e2-244">counter resolution</span></span></li>
<li><span data-ttu-id="c37e2-245">目前的曲目</span><span class="sxs-lookup"><span data-stu-id="c37e2-245">current track</span></span></li>
<li><span data-ttu-id="c37e2-246">畫面播放速率</span><span class="sxs-lookup"><span data-stu-id="c37e2-246">frame rate</span></span></li>
<li><span data-ttu-id="c37e2-247">索引</span><span class="sxs-lookup"><span data-stu-id="c37e2-247">index</span></span></li>
<li><span data-ttu-id="c37e2-248">索引開啟</span><span class="sxs-lookup"><span data-stu-id="c37e2-248">index on</span></span></li>
<li><span data-ttu-id="c37e2-249">長度</span><span class="sxs-lookup"><span data-stu-id="c37e2-249">length</span></span></li>
<li><span data-ttu-id="c37e2-250">長度追蹤 <em>號碼</em></span><span class="sxs-lookup"><span data-stu-id="c37e2-250">length track <em>number</em></span></span></li>
<li><span data-ttu-id="c37e2-251">媒體存在</span><span class="sxs-lookup"><span data-stu-id="c37e2-251">media present</span></span></li>
<li><span data-ttu-id="c37e2-252">媒體類型</span><span class="sxs-lookup"><span data-stu-id="c37e2-252">media type</span></span></li>
<li><span data-ttu-id="c37e2-253">mode</span><span class="sxs-lookup"><span data-stu-id="c37e2-253">mode</span></span></li>
<li><span data-ttu-id="c37e2-254">音訊曲目數目</span><span class="sxs-lookup"><span data-stu-id="c37e2-254">number of audio tracks</span></span></li>
<li><span data-ttu-id="c37e2-255">曲目數</span><span class="sxs-lookup"><span data-stu-id="c37e2-255">number of tracks</span></span></li>
<li><span data-ttu-id="c37e2-256">影片曲目數</span><span class="sxs-lookup"><span data-stu-id="c37e2-256">number of video tracks</span></span></li>
<li><span data-ttu-id="c37e2-257">暫停 <em>timeout</em></span><span class="sxs-lookup"><span data-stu-id="c37e2-257">pause <em>timeout</em></span></span></li>
<li><span data-ttu-id="c37e2-258">播放格式</span><span class="sxs-lookup"><span data-stu-id="c37e2-258">play format</span></span></li>
<li><span data-ttu-id="c37e2-259">position</span><span class="sxs-lookup"><span data-stu-id="c37e2-259">position</span></span></li>
<li><span data-ttu-id="c37e2-260">開始位置</span><span class="sxs-lookup"><span data-stu-id="c37e2-260">position start</span></span></li>
<li><span data-ttu-id="c37e2-261">位置曲目 <em>編號</em></span><span class="sxs-lookup"><span data-stu-id="c37e2-261">position track <em>number</em></span></span></li>
<li><span data-ttu-id="c37e2-262">postroll <em>持續期間</em></span><span class="sxs-lookup"><span data-stu-id="c37e2-262">postroll <em>duration</em></span></span></li>
<li><span data-ttu-id="c37e2-263">開啟電源</span><span class="sxs-lookup"><span data-stu-id="c37e2-263">power on</span></span></li>
<li><span data-ttu-id="c37e2-264">預先的 <em>持續時間</em></span><span class="sxs-lookup"><span data-stu-id="c37e2-264">preroll <em>duration</em></span></span></li>
<li><span data-ttu-id="c37e2-265">準備</span><span class="sxs-lookup"><span data-stu-id="c37e2-265">ready</span></span></li>
<li><span data-ttu-id="c37e2-266">記錄格式</span><span class="sxs-lookup"><span data-stu-id="c37e2-266">record format</span></span></li>
<li><span data-ttu-id="c37e2-267">速度</span><span class="sxs-lookup"><span data-stu-id="c37e2-267">speed</span></span></li>
<li><span data-ttu-id="c37e2-268">時間格式</span><span class="sxs-lookup"><span data-stu-id="c37e2-268">time format</span></span></li>
<li><span data-ttu-id="c37e2-269">時間模式</span><span class="sxs-lookup"><span data-stu-id="c37e2-269">time mode</span></span></li>
<li><span data-ttu-id="c37e2-270">時間類型</span><span class="sxs-lookup"><span data-stu-id="c37e2-270">time type</span></span></li>
<li><span data-ttu-id="c37e2-271">出現的時間碼</span><span class="sxs-lookup"><span data-stu-id="c37e2-271">timecode present</span></span></li>
<li><span data-ttu-id="c37e2-272">時間碼記錄</span><span class="sxs-lookup"><span data-stu-id="c37e2-272">timecode record</span></span></li>
<li><span data-ttu-id="c37e2-273">時間碼類型</span><span class="sxs-lookup"><span data-stu-id="c37e2-273">timecode type</span></span></li>
<li><span data-ttu-id="c37e2-274">調諧器數目</span><span class="sxs-lookup"><span data-stu-id="c37e2-274">tuner number</span></span></li>
<li><span data-ttu-id="c37e2-275">影片監視器</span><span class="sxs-lookup"><span data-stu-id="c37e2-275">video monitor</span></span></li>
<li><span data-ttu-id="c37e2-276">影片監視器編號</span><span class="sxs-lookup"><span data-stu-id="c37e2-276">video monitor number</span></span></li>
<li><span data-ttu-id="c37e2-277">影片記錄</span><span class="sxs-lookup"><span data-stu-id="c37e2-277">video record</span></span></li>
<li><span data-ttu-id="c37e2-278">影片記錄播放軌 <em>編號</em></span><span class="sxs-lookup"><span data-stu-id="c37e2-278">video record track <em>number</em></span></span></li>
<li><span data-ttu-id="c37e2-279">影片來源</span><span class="sxs-lookup"><span data-stu-id="c37e2-279">video source</span></span></li>
<li><span data-ttu-id="c37e2-280">影片來源編號</span><span class="sxs-lookup"><span data-stu-id="c37e2-280">video source number</span></span></li>
<li><span data-ttu-id="c37e2-281">寫入受保護</span><span class="sxs-lookup"><span data-stu-id="c37e2-281">write protected</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c37e2-282">videodisc</span><span class="sxs-lookup"><span data-stu-id="c37e2-282">videodisc</span></span></td>
<td><ul>
<li><span data-ttu-id="c37e2-283">目前的曲目</span><span class="sxs-lookup"><span data-stu-id="c37e2-283">current track</span></span></li>
<li><span data-ttu-id="c37e2-284">磁片大小</span><span class="sxs-lookup"><span data-stu-id="c37e2-284">disc size</span></span></li>
<li><span data-ttu-id="c37e2-285">forward</span><span class="sxs-lookup"><span data-stu-id="c37e2-285">forward</span></span></li>
<li><span data-ttu-id="c37e2-286">長度</span><span class="sxs-lookup"><span data-stu-id="c37e2-286">length</span></span></li>
<li><span data-ttu-id="c37e2-287">長度追蹤 <em>號碼</em></span><span class="sxs-lookup"><span data-stu-id="c37e2-287">length track <em>number</em></span></span></li>
<li><span data-ttu-id="c37e2-288">媒體存在</span><span class="sxs-lookup"><span data-stu-id="c37e2-288">media present</span></span></li>
<li><span data-ttu-id="c37e2-289">媒體類型</span><span class="sxs-lookup"><span data-stu-id="c37e2-289">media type</span></span></li>
<li><span data-ttu-id="c37e2-290">mode</span><span class="sxs-lookup"><span data-stu-id="c37e2-290">mode</span></span></li>
<li><span data-ttu-id="c37e2-291">曲目數</span><span class="sxs-lookup"><span data-stu-id="c37e2-291">number of tracks</span></span></li>
<li><span data-ttu-id="c37e2-292">position</span><span class="sxs-lookup"><span data-stu-id="c37e2-292">position</span></span></li>
<li><span data-ttu-id="c37e2-293">位置曲目 <em>編號</em></span><span class="sxs-lookup"><span data-stu-id="c37e2-293">position track <em>number</em></span></span></li>
<li><span data-ttu-id="c37e2-294">準備</span><span class="sxs-lookup"><span data-stu-id="c37e2-294">ready</span></span></li>
<li><span data-ttu-id="c37e2-295">一邊</span><span class="sxs-lookup"><span data-stu-id="c37e2-295">side</span></span></li>
<li><span data-ttu-id="c37e2-296">速度</span><span class="sxs-lookup"><span data-stu-id="c37e2-296">speed</span></span></li>
<li><span data-ttu-id="c37e2-297">開始位置</span><span class="sxs-lookup"><span data-stu-id="c37e2-297">start position</span></span></li>
<li><span data-ttu-id="c37e2-298">時間格式</span><span class="sxs-lookup"><span data-stu-id="c37e2-298">time format</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c37e2-299">waveaudio</span><span class="sxs-lookup"><span data-stu-id="c37e2-299">waveaudio</span></span></td>
<td><ul>
<li><span data-ttu-id="c37e2-300">對齊</span><span class="sxs-lookup"><span data-stu-id="c37e2-300">alignment</span></span></li>
<li><span data-ttu-id="c37e2-301">bitspersample</span><span class="sxs-lookup"><span data-stu-id="c37e2-301">bitspersample</span></span></li>
<li><span data-ttu-id="c37e2-302">bytespersec</span><span class="sxs-lookup"><span data-stu-id="c37e2-302">bytespersec</span></span></li>
<li><span data-ttu-id="c37e2-303">通道</span><span class="sxs-lookup"><span data-stu-id="c37e2-303">channels</span></span></li>
<li><span data-ttu-id="c37e2-304">目前的曲目</span><span class="sxs-lookup"><span data-stu-id="c37e2-304">current track</span></span></li>
<li><span data-ttu-id="c37e2-305">格式標記</span><span class="sxs-lookup"><span data-stu-id="c37e2-305">format tag</span></span></li>
<li><span data-ttu-id="c37e2-306">input</span><span class="sxs-lookup"><span data-stu-id="c37e2-306">input</span></span></li>
<li><span data-ttu-id="c37e2-307">長度</span><span class="sxs-lookup"><span data-stu-id="c37e2-307">length</span></span></li>
<li><span data-ttu-id="c37e2-308">長度追蹤 <em>號碼</em></span><span class="sxs-lookup"><span data-stu-id="c37e2-308">length track <em>number</em></span></span></li>
<li><span data-ttu-id="c37e2-309">等級</span><span class="sxs-lookup"><span data-stu-id="c37e2-309">level</span></span></li>
<li><span data-ttu-id="c37e2-310">媒體存在</span><span class="sxs-lookup"><span data-stu-id="c37e2-310">media present</span></span></li>
<li><span data-ttu-id="c37e2-311">mode</span><span class="sxs-lookup"><span data-stu-id="c37e2-311">mode</span></span></li>
<li><span data-ttu-id="c37e2-312">曲目數</span><span class="sxs-lookup"><span data-stu-id="c37e2-312">number of tracks</span></span></li>
<li><span data-ttu-id="c37e2-313">output</span><span class="sxs-lookup"><span data-stu-id="c37e2-313">output</span></span></li>
<li><span data-ttu-id="c37e2-314">position</span><span class="sxs-lookup"><span data-stu-id="c37e2-314">position</span></span></li>
<li><span data-ttu-id="c37e2-315">位置曲目 <em>編號</em></span><span class="sxs-lookup"><span data-stu-id="c37e2-315">position track <em>number</em></span></span></li>
<li><span data-ttu-id="c37e2-316">準備</span><span class="sxs-lookup"><span data-stu-id="c37e2-316">ready</span></span></li>
<li><span data-ttu-id="c37e2-317">samplespersec</span><span class="sxs-lookup"><span data-stu-id="c37e2-317">samplespersec</span></span></li>
<li><span data-ttu-id="c37e2-318">開始位置</span><span class="sxs-lookup"><span data-stu-id="c37e2-318">start position</span></span></li>
<li><span data-ttu-id="c37e2-319">時間格式</span><span class="sxs-lookup"><span data-stu-id="c37e2-319">time format</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="c37e2-320">下表列出可在 **lpszRequest** 參數中指定的旗標，以及它們的意義。</span><span class="sxs-lookup"><span data-stu-id="c37e2-320">The following table lists the flags that can be specified in the **lpszRequest** parameter and their meanings.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c37e2-321">值</span><span class="sxs-lookup"><span data-stu-id="c37e2-321">Value</span></span></th>
<th><span data-ttu-id="c37e2-322">意義</span><span class="sxs-lookup"><span data-stu-id="c37e2-322">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c37e2-323">對齊</span><span class="sxs-lookup"><span data-stu-id="c37e2-323">alignment</span></span></td>
<td><span data-ttu-id="c37e2-324">傳回資料的區塊對齊（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="c37e2-324">Returns the block alignment of data, in bytes.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c37e2-325">組合記錄</span><span class="sxs-lookup"><span data-stu-id="c37e2-325">assemble record</span></span></td>
<td><span data-ttu-id="c37e2-326">如果裝置設定為組合模式記錄，則傳回 <strong>TRUE</strong> 。</span><span class="sxs-lookup"><span data-stu-id="c37e2-326">Returns <strong>TRUE</strong> if the device is set to assemble mode recording.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c37e2-327">音訊</span><span class="sxs-lookup"><span data-stu-id="c37e2-327">audio</span></span></td>
<td><span data-ttu-id="c37e2-328">&quot; &quot; &quot; &quot; 根據最新的<a href="setaudio.md">setaudio</a> &quot; on &quot; 或 &quot; off &quot; 命令傳回 on 或 off。</span><span class="sxs-lookup"><span data-stu-id="c37e2-328">Returns &quot;on&quot; or &quot;off&quot; depending on the most recent <a href="setaudio.md">setaudio</a> &quot;on&quot; or &quot;off&quot; command.</span></span> <span data-ttu-id="c37e2-329">&quot; &quot; 如果已啟用其中一或兩個喇叭，則會傳回，否則會傳回 &quot; &quot; 。</span><span class="sxs-lookup"><span data-stu-id="c37e2-329">It returns &quot;on&quot; if either or both speakers are enabled, and &quot;off&quot; otherwise.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c37e2-330">音訊對齊</span><span class="sxs-lookup"><span data-stu-id="c37e2-330">audio alignment</span></span></td>
<td><span data-ttu-id="c37e2-331">傳回資料區塊相對於輸入波形-音訊資料開頭的對齊方式。</span><span class="sxs-lookup"><span data-stu-id="c37e2-331">Returns the alignment of data blocks relative to the start of input waveform-audio data.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c37e2-332">音訊 bitspersample</span><span class="sxs-lookup"><span data-stu-id="c37e2-332">audio bitspersample</span></span></td>
<td><span data-ttu-id="c37e2-333">傳回裝置用來錄製的每個樣本位數。</span><span class="sxs-lookup"><span data-stu-id="c37e2-333">Returns the number of bits per sample the device uses for recording.</span></span> <span data-ttu-id="c37e2-334">此旗標只適用于支援 &quot; pcm 演算法的裝置 &quot; 。</span><span class="sxs-lookup"><span data-stu-id="c37e2-334">This flag applies only to devices supporting the &quot;pcm&quot; algorithm.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c37e2-335">音訊中斷</span><span class="sxs-lookup"><span data-stu-id="c37e2-335">audio breaks</span></span></td>
<td><span data-ttu-id="c37e2-336">傳回最後一個 AVI 序列的音訊部分中斷的次數。</span><span class="sxs-lookup"><span data-stu-id="c37e2-336">Returns the number of times the audio portion of the last AVI sequence broke up.</span></span> <span data-ttu-id="c37e2-337">當系統嘗試將音訊資料寫入設備磁碟機，併發現該驅動程式已經播放了所有可用的資料時，系統就會計算出一份音訊中斷的次數。</span><span class="sxs-lookup"><span data-stu-id="c37e2-337">The system counts an audio break whenever it attempts to write audio data to the device driver and discovers that the driver has already played all of the available data.</span></span> <span data-ttu-id="c37e2-338">只有 MCIAVI 數位視訊驅動程式能辨識此旗標。</span><span class="sxs-lookup"><span data-stu-id="c37e2-338">This flag is recognized only by the MCIAVI digital-video driver.</span></span> <span data-ttu-id="c37e2-339">它僅適用于效能評估;傳回值難以解讀。</span><span class="sxs-lookup"><span data-stu-id="c37e2-339">It is meant for performance evaluation only; the return value is difficult to interpret.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c37e2-340">音訊 bytespersec</span><span class="sxs-lookup"><span data-stu-id="c37e2-340">audio bytespersec</span></span></td>
<td><span data-ttu-id="c37e2-341">傳回用於錄製的平均每秒位元組數。</span><span class="sxs-lookup"><span data-stu-id="c37e2-341">Returns the average number of bytes per second used for recording.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c37e2-342">音訊輸入</span><span class="sxs-lookup"><span data-stu-id="c37e2-342">audio input</span></span></td>
<td><span data-ttu-id="c37e2-343">傳回類比輸入音訊信號的近似即時音訊層級。</span><span class="sxs-lookup"><span data-stu-id="c37e2-343">Returns the approximate instantaneous audio level of the analog input audio signal.</span></span> <span data-ttu-id="c37e2-344">大於1000的值表示裁剪扭曲。</span><span class="sxs-lookup"><span data-stu-id="c37e2-344">A value greater than 1000 implies clipping distortion.</span></span> <span data-ttu-id="c37e2-345">某些裝置只能在錄製音訊時傳回此值。</span><span class="sxs-lookup"><span data-stu-id="c37e2-345">Some devices can return this value only while recording audio.</span></span> <span data-ttu-id="c37e2-346">值沒有相關聯的 <a href="set.md">set</a> 或 <a href="setaudio.md">setaudio</a> 命令。</span><span class="sxs-lookup"><span data-stu-id="c37e2-346">The value has no associated <a href="set.md">set</a> or <a href="setaudio.md">setaudio</a> command.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c37e2-347">音訊監視器</span><span class="sxs-lookup"><span data-stu-id="c37e2-347">audio monitor</span></span></td>
<td><span data-ttu-id="c37e2-348">傳回 &quot; 輸出 &quot; ，或其中一個有效的來源輸入類型。</span><span class="sxs-lookup"><span data-stu-id="c37e2-348">Returns &quot;output&quot;, or one of the valid source-input types.</span></span> <span data-ttu-id="c37e2-349">如需詳細資訊，請參閱 <strong>setaudio</strong> &quot; 監視器 &quot; 命令。</span><span class="sxs-lookup"><span data-stu-id="c37e2-349">For more information, see the <strong>setaudio</strong> &quot;monitor&quot; command.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c37e2-350">音訊監視器編號</span><span class="sxs-lookup"><span data-stu-id="c37e2-350">audio monitor number</span></span></td>
<td><span data-ttu-id="c37e2-351">傳回 <strong>狀態</strong>音訊監視器所指定之類型的監視影片編號 &quot; &quot; 。</span><span class="sxs-lookup"><span data-stu-id="c37e2-351">Returns the monitored-video number of the type specified by <strong>status</strong> &quot;audio monitor&quot;.</span></span> <span data-ttu-id="c37e2-352">如需詳細資訊，請參閱 <a href="setaudio.md">setaudio</a> 命令。</span><span class="sxs-lookup"><span data-stu-id="c37e2-352">For more information, see the <a href="setaudio.md">setaudio</a> command.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c37e2-353">音訊記錄</span><span class="sxs-lookup"><span data-stu-id="c37e2-353">audio record</span></span></td>
<td><span data-ttu-id="c37e2-354">傳回 &quot; &quot; 或 &quot; 關閉 &quot; ，反映 <strong>setaudio</strong>記錄所設定的狀態 &quot; &quot; 。</span><span class="sxs-lookup"><span data-stu-id="c37e2-354">Returns &quot;on&quot; or &quot;off&quot;, reflecting the state set by <strong>setaudio</strong> &quot;record&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c37e2-355">音訊記錄播放軌 <em>編號</em></span><span class="sxs-lookup"><span data-stu-id="c37e2-355">audio record track <em>number</em></span></span></td>
<td><span data-ttu-id="c37e2-356">如果 VCR 設定為錄製音訊，則傳回 <strong>TRUE</strong> 。</span><span class="sxs-lookup"><span data-stu-id="c37e2-356">Returns <strong>TRUE</strong> if the VCR is set to record audio.</span></span> <span data-ttu-id="c37e2-357">如果未指定任何追蹤編號，則會假設為預設值1。</span><span class="sxs-lookup"><span data-stu-id="c37e2-357">If no track number is given, the default value of 1 is assumed.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c37e2-358">音訊 samplespersec</span><span class="sxs-lookup"><span data-stu-id="c37e2-358">audio samplespersec</span></span></td>
<td><span data-ttu-id="c37e2-359">傳回每秒記錄的樣本數。</span><span class="sxs-lookup"><span data-stu-id="c37e2-359">Returns the number of samples per second recorded.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c37e2-360">音訊來源</span><span class="sxs-lookup"><span data-stu-id="c37e2-360">audio source</span></span></td>
<td><span data-ttu-id="c37e2-361">傳回目前的音訊數位板來源： &quot; 左方 &quot; 、 &quot; 右邊 &quot; 、 &quot; 平均 &quot; 或 &quot; 身歷聲 &quot; 。</span><span class="sxs-lookup"><span data-stu-id="c37e2-361">Returns the current audio digitizer source: &quot;left&quot;, &quot;right&quot;, &quot;average&quot;, or &quot;stereo&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c37e2-362">音訊來源編號</span><span class="sxs-lookup"><span data-stu-id="c37e2-362">audio source number</span></span></td>
<td><span data-ttu-id="c37e2-363">傳回 <strong>狀態</strong>音訊來源所傳回之類型的音訊來源編號 &quot; &quot; 。</span><span class="sxs-lookup"><span data-stu-id="c37e2-363">Returns the audio-source number of the type returned by <strong>status</strong> &quot;audio source&quot;.</span></span> <span data-ttu-id="c37e2-364">如需詳細資訊，請參閱 <a href="setaudio.md">setaudio</a> 命令。</span><span class="sxs-lookup"><span data-stu-id="c37e2-364">For more information, see the <a href="setaudio.md">setaudio</a> command.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c37e2-365">音訊串流</span><span class="sxs-lookup"><span data-stu-id="c37e2-365">audio stream</span></span></td>
<td><span data-ttu-id="c37e2-366">傳回目前的音訊資料流程數目。</span><span class="sxs-lookup"><span data-stu-id="c37e2-366">Returns the current audio-stream number.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c37e2-367">低音</span><span class="sxs-lookup"><span data-stu-id="c37e2-367">bass</span></span></td>
<td><span data-ttu-id="c37e2-368">傳回目前的音訊低音等級。</span><span class="sxs-lookup"><span data-stu-id="c37e2-368">Returns the current audio-bass level.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c37e2-369">bitsperpel</span><span class="sxs-lookup"><span data-stu-id="c37e2-369">bitsperpel</span></span></td>
<td><span data-ttu-id="c37e2-370">傳回儲存已捕捉或已記錄資料之每個圖元的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="c37e2-370">Returns the number of bits per pixel for saving captured or recorded data.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c37e2-371">bitspersample</span><span class="sxs-lookup"><span data-stu-id="c37e2-371">bitspersample</span></span></td>
<td><span data-ttu-id="c37e2-372">傳回每個樣本的位數。</span><span class="sxs-lookup"><span data-stu-id="c37e2-372">Returns the bits per sample.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c37e2-373">亮度</span><span class="sxs-lookup"><span data-stu-id="c37e2-373">brightness</span></span></td>
<td><span data-ttu-id="c37e2-374">傳回目前的視頻亮度層級。</span><span class="sxs-lookup"><span data-stu-id="c37e2-374">Returns the current video-brightness level.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c37e2-375">bytespersec</span><span class="sxs-lookup"><span data-stu-id="c37e2-375">bytespersec</span></span></td>
<td><span data-ttu-id="c37e2-376">傳回每秒播放或記錄的平均位元組數。</span><span class="sxs-lookup"><span data-stu-id="c37e2-376">Returns the average number of bytes per second played or recorded.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c37e2-377">cdaudio 類型追蹤 <em>編號</em></span><span class="sxs-lookup"><span data-stu-id="c37e2-377">cdaudio type track <em>number</em></span></span></td>
<td><span data-ttu-id="c37e2-378">傳回指定之追蹤編號的型別。</span><span class="sxs-lookup"><span data-stu-id="c37e2-378">Returns the type of the specified track number.</span></span> <span data-ttu-id="c37e2-379">這可以是 &quot; 音訊 &quot; 或 &quot; 其他。&quot;</span><span class="sxs-lookup"><span data-stu-id="c37e2-379">This can be &quot;audio&quot; or &quot;other.&quot;</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c37e2-380">通道</span><span class="sxs-lookup"><span data-stu-id="c37e2-380">channel</span></span></td>
<td><span data-ttu-id="c37e2-381">傳回檔諧器上通道集的整數值。</span><span class="sxs-lookup"><span data-stu-id="c37e2-381">Returns the integer value of the channel set on the tuner.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c37e2-382">通道調諧器 <em>號碼</em></span><span class="sxs-lookup"><span data-stu-id="c37e2-382">channel tuner <em>number</em></span></span></td>
<td><span data-ttu-id="c37e2-383">如果 &quot; 指定了調諧器 &quot; <em>號碼</em>，則會傳回邏輯調諧器上目前選取的<em></em>通道。</span><span class="sxs-lookup"><span data-stu-id="c37e2-383">If &quot;tuner&quot; <em>number</em> is given, then the currently selected channel on the logical tuner <em>number</em> will be returned.</span></span> <span data-ttu-id="c37e2-384">請注意，您可以有數個邏輯調諧器。</span><span class="sxs-lookup"><span data-stu-id="c37e2-384">Note that there can be several logical tuners.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c37e2-385">通道</span><span class="sxs-lookup"><span data-stu-id="c37e2-385">channels</span></span></td>
<td><span data-ttu-id="c37e2-386">傳回為 mono 設定的通道數目 (1，) 為身歷聲的2。</span><span class="sxs-lookup"><span data-stu-id="c37e2-386">Returns the number of channels set (1 for mono, 2 for stereo).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c37e2-387">時鐘</span><span class="sxs-lookup"><span data-stu-id="c37e2-387">clock</span></span></td>
<td><span data-ttu-id="c37e2-388">傳回外部時間。</span><span class="sxs-lookup"><span data-stu-id="c37e2-388">Returns the external time.</span></span> <span data-ttu-id="c37e2-389">時間必須是以不帶正負號的長整數表示總增量。</span><span class="sxs-lookup"><span data-stu-id="c37e2-389">The time must be an unsigned long integer expressing total increments.</span></span> <span data-ttu-id="c37e2-390">如需詳細資訊，請參閱 <a href="capability.md">功能</a> &quot; 頻率遞增速率 &quot; 命令。</span><span class="sxs-lookup"><span data-stu-id="c37e2-390">For more information, see the <a href="capability.md">capability</a> &quot;clock increment rate&quot; command.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c37e2-391">時鐘識別碼</span><span class="sxs-lookup"><span data-stu-id="c37e2-391">clock id</span></span></td>
<td><span data-ttu-id="c37e2-392">傳回識別時鐘的唯一整數。</span><span class="sxs-lookup"><span data-stu-id="c37e2-392">Returns a unique integer identifying the clock.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c37e2-393">color</span><span class="sxs-lookup"><span data-stu-id="c37e2-393">color</span></span></td>
<td><span data-ttu-id="c37e2-394">傳回目前的色彩層級。</span><span class="sxs-lookup"><span data-stu-id="c37e2-394">Returns the current color level.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c37e2-395">對比</span><span class="sxs-lookup"><span data-stu-id="c37e2-395">contrast</span></span></td>
<td><span data-ttu-id="c37e2-396">傳回目前的對比層級。</span><span class="sxs-lookup"><span data-stu-id="c37e2-396">Returns the current contrast level.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c37e2-397">counter</span><span class="sxs-lookup"><span data-stu-id="c37e2-397">counter</span></span></td>
<td><span data-ttu-id="c37e2-398">傳回目前計數器格式的計數器位置。</span><span class="sxs-lookup"><span data-stu-id="c37e2-398">Returns the counter position, in the current counter format.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c37e2-399">計數器格式</span><span class="sxs-lookup"><span data-stu-id="c37e2-399">counter format</span></span></td>
<td><span data-ttu-id="c37e2-400">傳回目前的計數器格式。</span><span class="sxs-lookup"><span data-stu-id="c37e2-400">Returns the current counter format.</span></span> <span data-ttu-id="c37e2-401">如需詳細資訊，請參閱 <a href="set.md">設定</a> &quot; 計數器格式 &quot; 命令。</span><span class="sxs-lookup"><span data-stu-id="c37e2-401">For more information, see the <a href="set.md">set</a> &quot;counter format&quot; command.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c37e2-402">計數器解析</span><span class="sxs-lookup"><span data-stu-id="c37e2-402">counter resolution</span></span></td>
<td><span data-ttu-id="c37e2-403">傳回 &quot; &quot; 表示計數器解析度的框架或 &quot; 秒數 &quot; 。</span><span class="sxs-lookup"><span data-stu-id="c37e2-403">Returns &quot;frames&quot; or &quot;seconds&quot;, indicating the counter's resolution.</span></span> <span data-ttu-id="c37e2-404">這與精確度不同。</span><span class="sxs-lookup"><span data-stu-id="c37e2-404">This is not the same as accuracy.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c37e2-405">目前的曲目</span><span class="sxs-lookup"><span data-stu-id="c37e2-405">current track</span></span></td>
<td><span data-ttu-id="c37e2-406">傳回目前的曲目。MCISEQ sequencer 會傳回1。</span><span class="sxs-lookup"><span data-stu-id="c37e2-406">Returns the current track. The MCISEQ sequencer returns 1.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c37e2-407">磁片大小</span><span class="sxs-lookup"><span data-stu-id="c37e2-407">disc size</span></span></td>
<td><span data-ttu-id="c37e2-408">傳回8或12，表示載入的光碟大小（以英寸為單位）。</span><span class="sxs-lookup"><span data-stu-id="c37e2-408">Returns either 8 or 12, indicating the size of the loaded disc in inches.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c37e2-409">磁碟空間磁片 <em>磁碟機</em></span><span class="sxs-lookup"><span data-stu-id="c37e2-409">disk space <em>drive</em></span></span></td>
<td><span data-ttu-id="c37e2-410">傳回指定磁片磁碟機的 <a href="reserve.md">reserve</a> 命令可取得的大約磁碟空間（以目前的時間格式表示） <em>。</em></span><span class="sxs-lookup"><span data-stu-id="c37e2-410">Returns the approximate disk space, in the current time format, that can be obtained by a <a href="reserve.md">reserve</a> command for the specified disk <em>drive.</em></span></span> <span data-ttu-id="c37e2-411"><em>磁片磁碟機</em>通常會指定為單一字母或單一字母，後面接著冒號 (： ) 。</span><span class="sxs-lookup"><span data-stu-id="c37e2-411">The <em>drive</em> is usually specified as a single letter or a single letter followed by a colon (:).</span></span> <span data-ttu-id="c37e2-412">不過，某些裝置可能會使用路徑。</span><span class="sxs-lookup"><span data-stu-id="c37e2-412">Some devices, however, might use a path.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c37e2-413">除法類型</span><span class="sxs-lookup"><span data-stu-id="c37e2-413">division type</span></span></td>
<td><span data-ttu-id="c37e2-414">傳回下列其中一個檔案除法類型：</span><span class="sxs-lookup"><span data-stu-id="c37e2-414">Returns one of the following file division types:</span></span>
<ul>
<li><span data-ttu-id="c37e2-415">PPQN</span><span class="sxs-lookup"><span data-stu-id="c37e2-415">PPQN</span></span></li>
<li><span data-ttu-id="c37e2-416">SMPTE 24 框架</span><span class="sxs-lookup"><span data-stu-id="c37e2-416">SMPTE 24 frame</span></span></li>
<li><span data-ttu-id="c37e2-417">SMPTE 25 框架</span><span class="sxs-lookup"><span data-stu-id="c37e2-417">SMPTE 25 frame</span></span></li>
<li><span data-ttu-id="c37e2-418">SMPTE 30 捨棄框架</span><span class="sxs-lookup"><span data-stu-id="c37e2-418">SMPTE 30 drop frame</span></span></li>
<li><span data-ttu-id="c37e2-419">SMPTE 30 框架</span><span class="sxs-lookup"><span data-stu-id="c37e2-419">SMPTE 30 frame</span></span></li>
</ul>
<br/> <span data-ttu-id="c37e2-420">您可以使用這項資訊來判斷 MIDI 檔案的格式，以及節奏和位置資訊的意義。</span><span class="sxs-lookup"><span data-stu-id="c37e2-420">Use this information to determine the format of the MIDI file and the meaning of tempo and position information.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c37e2-421">檔案完成</span><span class="sxs-lookup"><span data-stu-id="c37e2-421">file completion</span></span></td>
<td><span data-ttu-id="c37e2-422">傳回 <a href="load.md">負載</a>、 <a href="save.md">儲存</a>、 <a href="capture.md">捕捉</a>、 <a href="cut.md">剪</a>下、 <a href="copy.md">複製</a>、 <a href="delete.md">刪除</a>、 <a href="paste.md">貼</a>上或 <a href="undo.md">復原</a> 作業進度的估計百分比。</span><span class="sxs-lookup"><span data-stu-id="c37e2-422">Returns the estimated percentage a <a href="load.md">load</a>, <a href="save.md">save</a>, <a href="capture.md">capture</a>, <a href="cut.md">cut</a>, <a href="copy.md">copy</a>, <a href="delete.md">delete</a>, <a href="paste.md">paste</a>, or <a href="undo.md">undo</a> operation has progressed.</span></span> <span data-ttu-id="c37e2-423"> (的應用程式可以使用它來提供進度的視覺指標。 ) </span><span class="sxs-lookup"><span data-stu-id="c37e2-423">(Applications can use this to provide a visual indicator of progress.)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c37e2-424">檔案格式</span><span class="sxs-lookup"><span data-stu-id="c37e2-424">file format</span></span></td>
<td><span data-ttu-id="c37e2-425">傳回 <a href="record.md">記錄</a> 或 <strong>儲存</strong> 命令的目前檔案格式。</span><span class="sxs-lookup"><span data-stu-id="c37e2-425">Returns the current file format for <a href="record.md">record</a> or <strong>save</strong> commands.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c37e2-426">檔案模式</span><span class="sxs-lookup"><span data-stu-id="c37e2-426">file mode</span></span></td>
<td><span data-ttu-id="c37e2-427">傳回 &quot; 載入 &quot; 、 &quot; 儲存 &quot; 、 &quot; 編輯 &quot; 或 &quot; 閒置 &quot; 。</span><span class="sxs-lookup"><span data-stu-id="c37e2-427">Returns &quot;loading&quot;, &quot;saving&quot;, &quot;editing&quot;, or &quot;idle&quot;.</span></span> <span data-ttu-id="c37e2-428">在 <a href="load.md"><strong>載入</strong></a> 作業期間，它會傳回 &quot; 載入 &quot; 。</span><span class="sxs-lookup"><span data-stu-id="c37e2-428">During a <a href="load.md"><strong>load</strong></a> operation, it returns &quot;loading&quot;.</span></span> <span data-ttu-id="c37e2-429">在 <a href="https://www.bing.com/search?q=<strong>save</strong>"><strong>儲存</strong></a> 和 <a href="capture.md"><strong>捕獲</strong></a> 作業期間，它會傳回 &quot; 儲存 &quot; 。</span><span class="sxs-lookup"><span data-stu-id="c37e2-429">During <a href="https://www.bing.com/search?q=<strong>save</strong>"><strong>save</strong></a> and <a href="capture.md"><strong>capture</strong></a> operations, it returns &quot;saving&quot;.</span></span> <span data-ttu-id="c37e2-430">在 <a href="cut.md"><strong>剪</strong></a>下、 <a href="copy.md"><strong>複製</strong></a>、 <a href="delete.md"><strong>刪除</strong></a>、 <a href="paste.md"><strong>貼</strong></a>上或 <a href="undo.md"><strong>復原</strong></a> 作業期間，它會傳回 &quot; 編輯 &quot; 。</span><span class="sxs-lookup"><span data-stu-id="c37e2-430">During <a href="cut.md"><strong>cut</strong></a>, <a href="copy.md"><strong>copy</strong></a>, <a href="delete.md"><strong>delete</strong></a>, <a href="paste.md"><strong>paste</strong></a>, or <a href="undo.md"><strong>undo</strong></a> operations, it returns &quot;editing&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c37e2-431">格式標記</span><span class="sxs-lookup"><span data-stu-id="c37e2-431">format tag</span></span></td>
<td><span data-ttu-id="c37e2-432">傳回格式標記。</span><span class="sxs-lookup"><span data-stu-id="c37e2-432">Returns the format tag.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c37e2-433">forward</span><span class="sxs-lookup"><span data-stu-id="c37e2-433">forward</span></span></td>
<td><span data-ttu-id="c37e2-434">如果播放方向為向前或裝置未播放，則傳回 <strong>TRUE</strong> 。</span><span class="sxs-lookup"><span data-stu-id="c37e2-434">Returns <strong>TRUE</strong> if the play direction is forward or if the device is not playing.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c37e2-435">畫面播放速率</span><span class="sxs-lookup"><span data-stu-id="c37e2-435">frame rate</span></span></td>
<td><span data-ttu-id="c37e2-436">傳回裝置預設會使用的每秒畫面格數數目。</span><span class="sxs-lookup"><span data-stu-id="c37e2-436">Returns the number of frames per second that the device will use by default.</span></span> <span data-ttu-id="c37e2-437">NTSC 裝置會傳回30、PAL 25 等等。</span><span class="sxs-lookup"><span data-stu-id="c37e2-437">NTSC devices return 30, PAL 25, and so on.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c37e2-438">略過框架</span><span class="sxs-lookup"><span data-stu-id="c37e2-438">frames skipped</span></span></td>
<td><span data-ttu-id="c37e2-439">傳回播放最後一個 AVI 序列時未繪製的框架數目。</span><span class="sxs-lookup"><span data-stu-id="c37e2-439">Returns the number of frames that were not drawn when the last AVI sequence was played.</span></span> <span data-ttu-id="c37e2-440">只有 MCIAVI 數位視訊驅動程式能辨識此旗標。</span><span class="sxs-lookup"><span data-stu-id="c37e2-440">This flag is recognized only by the MCIAVI digital-video driver.</span></span> <span data-ttu-id="c37e2-441">它僅適用于效能評估;傳回值難以解讀。</span><span class="sxs-lookup"><span data-stu-id="c37e2-441">It is meant for performance evaluation only; the return value is difficult to interpret.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c37e2-442">gamma</span><span class="sxs-lookup"><span data-stu-id="c37e2-442">gamma</span></span></td>
<td><span data-ttu-id="c37e2-443">傳回將 <a href="setvideo.md"><strong>setvideo</strong></a> &quot; gamma 設定為 &quot; <em>value</em>的值。</span><span class="sxs-lookup"><span data-stu-id="c37e2-443">Returns the value set with <a href="setvideo.md"><strong>setvideo</strong></a> &quot;gamma to&quot; <em>value</em>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c37e2-444">索引</span><span class="sxs-lookup"><span data-stu-id="c37e2-444">index</span></span></td>
<td><span data-ttu-id="c37e2-445">傳回目前的索引顯示。</span><span class="sxs-lookup"><span data-stu-id="c37e2-445">Returns the current index display.</span></span> <span data-ttu-id="c37e2-446">如需詳細資訊，請參閱 <a href="set.md"><strong>set</strong></a> &quot; index &quot; 命令。</span><span class="sxs-lookup"><span data-stu-id="c37e2-446">For more information, see the <a href="set.md"><strong>set</strong></a> &quot;index&quot; command.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c37e2-447">索引開啟</span><span class="sxs-lookup"><span data-stu-id="c37e2-447">index on</span></span></td>
<td><span data-ttu-id="c37e2-448">如果索引為 on，則傳回 <strong>TRUE</strong> 。</span><span class="sxs-lookup"><span data-stu-id="c37e2-448">Returns <strong>TRUE</strong> if the index is on.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c37e2-449">input</span><span class="sxs-lookup"><span data-stu-id="c37e2-449">input</span></span></td>
<td><span data-ttu-id="c37e2-450">傳回輸入集。</span><span class="sxs-lookup"><span data-stu-id="c37e2-450">Returns the input set.</span></span> <span data-ttu-id="c37e2-451">如果未設定，則傳回的錯誤表示可以使用任何裝置。</span><span class="sxs-lookup"><span data-stu-id="c37e2-451">If one is not set, the error returned indicates that any device can be used.</span></span> <span data-ttu-id="c37e2-452">針對數位視訊裝置，修改 &quot; 低音 &quot; 、 &quot; 高音 &quot; 、 &quot; 音量 &quot; 、 &quot; 亮度 &quot; 、 &quot; 色彩 &quot; 、 &quot; 對比 &quot; 、 &quot; gamma &quot; 、 &quot; 清晰度 &quot; 或 &quot; 色調旗標， &quot; 使其僅適用于輸入。</span><span class="sxs-lookup"><span data-stu-id="c37e2-452">For digital-video devices, modifies the &quot;bass&quot;, &quot;treble&quot;, &quot;volume&quot;, &quot;brightness&quot;, &quot;color&quot;, &quot;contrast&quot;, &quot;gamma&quot;, &quot;sharpness&quot;, or &quot;tint&quot; flag so that it applies only to the input.</span></span> <span data-ttu-id="c37e2-453">這是監視輸入時的預設值。</span><span class="sxs-lookup"><span data-stu-id="c37e2-453">This is the default when monitoring the input.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c37e2-454">左方磁片區</span><span class="sxs-lookup"><span data-stu-id="c37e2-454">left volume</span></span></td>
<td><span data-ttu-id="c37e2-455">傳回左方音訊頻道的磁片區集合。</span><span class="sxs-lookup"><span data-stu-id="c37e2-455">Returns the volume set for the left audio channel.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c37e2-456">長度</span><span class="sxs-lookup"><span data-stu-id="c37e2-456">length</span></span></td>
<td><span data-ttu-id="c37e2-457">以目前的時間格式傳回媒體的總長度。</span><span class="sxs-lookup"><span data-stu-id="c37e2-457">Returns the total length of the media, in the current time format.</span></span> <span data-ttu-id="c37e2-458">若為 PPQN 檔案，則會以首歌指標單位傳回長度。</span><span class="sxs-lookup"><span data-stu-id="c37e2-458">For PPQN files, the length is returned in song pointer units.</span></span> <span data-ttu-id="c37e2-459">對於 SMPTE 檔案，它會傳回為 <em>hh： mm： ss： ff</em>，其中 <em>hh</em> 是小時， <em>mm</em> 是分鐘， <em>ss</em> 是秒，而 <em>ff</em> 是畫面格。</span><span class="sxs-lookup"><span data-stu-id="c37e2-459">For SMPTE files, it is returned as <em>hh:mm:ss:ff</em>, where <em>hh</em> is hours, <em>mm</em> is minutes, <em>ss</em> is seconds, and <em>ff</em> is frames.</span></span> <span data-ttu-id="c37e2-460">若為 VCR 裝置，長度為2小時 (除非已使用 <a href="https://www.bing.com/search?q=<strong>set</strong>"><strong>set</strong></a> 命令) 明確變更長度。</span><span class="sxs-lookup"><span data-stu-id="c37e2-460">For VCR devices, the length is 2 hours (unless the length has been explicitly changed using the <a href="https://www.bing.com/search?q=<strong>set</strong>"><strong>set</strong></a> command).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c37e2-461">長度追蹤 <em>號碼</em></span><span class="sxs-lookup"><span data-stu-id="c37e2-461">length track <em>number</em></span></span></td>
<td><span data-ttu-id="c37e2-462">傳回以 <em>數位</em>指定的曲目長度（以時間或框架為限）。若為 PPQN 檔案，則會以首歌指標單位傳回長度。</span><span class="sxs-lookup"><span data-stu-id="c37e2-462">Returns the length of the track, in time or frames, specified by <em>number</em>.For PPQN files, the length is returned in song pointer units.</span></span> <span data-ttu-id="c37e2-463">對於 SMPTE 檔案，它會傳回為 <em>hh： mm： ss： ff</em>，其中 <em>hh</em> 是小時， <em>mm</em> 是分鐘， <em>ss</em> 是秒，而 <em>ff</em> 是畫面格。</span><span class="sxs-lookup"><span data-stu-id="c37e2-463">For SMPTE files, it is returned as <em>hh:mm:ss:ff</em>, where <em>hh</em> is hours, <em>mm</em> is minutes, <em>ss</em> is seconds, and <em>ff</em> is frames.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c37e2-464">等級</span><span class="sxs-lookup"><span data-stu-id="c37e2-464">level</span></span></td>
<td><span data-ttu-id="c37e2-465">傳回目前的 PCM 音訊範例值。</span><span class="sxs-lookup"><span data-stu-id="c37e2-465">Returns the current PCM audio sample value.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c37e2-466">master</span><span class="sxs-lookup"><span data-stu-id="c37e2-466">master</span></span></td>
<td><span data-ttu-id="c37e2-467">&quot; &quot; &quot; &quot; &quot; &quot; 根據同步處理集的類型，傳回 midi、無或 smpte。</span><span class="sxs-lookup"><span data-stu-id="c37e2-467">Returns &quot;midi&quot;, &quot;none&quot;, or &quot;smpte&quot; depending on the type of synchronization set.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c37e2-468">媒體存在</span><span class="sxs-lookup"><span data-stu-id="c37e2-468">media present</span></span></td>
<td><span data-ttu-id="c37e2-469">如果媒體插入裝置中，則傳回 <strong>TRUE</strong> ，否則傳回 <strong>FALSE</strong> 。</span><span class="sxs-lookup"><span data-stu-id="c37e2-469">Returns <strong>TRUE</strong> if the media is inserted in the device or <strong>FALSE</strong> otherwise.</span></span> <span data-ttu-id="c37e2-470">Sequencer、影片重迭、數位影片和波形音訊裝置都會傳回 <strong>TRUE</strong>。</span><span class="sxs-lookup"><span data-stu-id="c37e2-470">Sequencer, video-overlay, digital-video, and waveform-audio devices return <strong>TRUE</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c37e2-471">媒體類型</span><span class="sxs-lookup"><span data-stu-id="c37e2-471">media type</span></span></td>
<td><span data-ttu-id="c37e2-472">傳回媒體的類型。</span><span class="sxs-lookup"><span data-stu-id="c37e2-472">Returns the type of the media.</span></span> <span data-ttu-id="c37e2-473">若為 VCR，此為 &quot; 8：8、 &quot; &quot; vhs &quot; 、 &quot; svhs &quot; 、 &quot; Beta &quot; 、 &quot; Hi8 &quot; 、 &quot; edBeta &quot; 或 &quot; 其他 &quot; 。</span><span class="sxs-lookup"><span data-stu-id="c37e2-473">For VCRS, this is &quot;8mm&quot;, &quot;vhs&quot;, &quot;svhs&quot;, &quot;beta&quot;, &quot;Hi8&quot;, &quot;edbeta&quot;, or &quot;other&quot;.</span></span> <span data-ttu-id="c37e2-474">針對 videodiscs，這是 &quot; CAV &quot; 、 &quot; CLV &quot; 或 &quot; 其他 &quot; ，視 videodisc 類型而定。</span><span class="sxs-lookup"><span data-stu-id="c37e2-474">For videodiscs, this is &quot;CAV&quot;, &quot;CLV&quot;, or &quot;other&quot;, depending on the type of videodisc.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c37e2-475">mode</span><span class="sxs-lookup"><span data-stu-id="c37e2-475">mode</span></span></td>
<td><span data-ttu-id="c37e2-476">傳回裝置的目前模式。</span><span class="sxs-lookup"><span data-stu-id="c37e2-476">Returns the current mode of the device.</span></span> <span data-ttu-id="c37e2-477">所有裝置都可以傳回 &quot; 未就緒 &quot; 、 &quot; &quot; 已暫停、 &quot; 播放 &quot; 和 &quot; 停止的 &quot; 值。</span><span class="sxs-lookup"><span data-stu-id="c37e2-477">All devices can return the &quot;not ready&quot;, &quot;paused&quot;, &quot;playing&quot;, and &quot;stopped&quot; values.</span></span> <span data-ttu-id="c37e2-478">某些裝置可以傳回額外的 &quot; 開啟 &quot; 、 &quot; 暫停 &quot; 、 &quot; 錄製 &quot; 和 &quot; 搜尋 &quot; 值。</span><span class="sxs-lookup"><span data-stu-id="c37e2-478">Some devices can return the additional &quot;open&quot;, &quot;parked&quot;, &quot;recording&quot;, and &quot;seeking&quot; values.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c37e2-479">monitor</span><span class="sxs-lookup"><span data-stu-id="c37e2-479">monitor</span></span></td>
<td><span data-ttu-id="c37e2-480">傳回 &quot; 檔案 &quot; 或 &quot; 輸入 &quot; 。</span><span class="sxs-lookup"><span data-stu-id="c37e2-480">Returns &quot;file&quot; or &quot;input&quot;.</span></span> <span data-ttu-id="c37e2-481">傳回的值表示目前的展示來源。</span><span class="sxs-lookup"><span data-stu-id="c37e2-481">The returned value indicates the current presentation source.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c37e2-482">監視方法</span><span class="sxs-lookup"><span data-stu-id="c37e2-482">monitor method</span></span></td>
<td><span data-ttu-id="c37e2-483">傳回 &quot; 前置 &quot; 、 &quot; 貼文 &quot; 或 &quot; 直接 &quot; 。</span><span class="sxs-lookup"><span data-stu-id="c37e2-483">Returns &quot;pre&quot;, &quot;post&quot;, or &quot;direct&quot;.</span></span> <span data-ttu-id="c37e2-484">傳回的值表示用於輸入監視的方法。</span><span class="sxs-lookup"><span data-stu-id="c37e2-484">The returned value indicates the method used for input monitoring.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c37e2-485">名義</span><span class="sxs-lookup"><span data-stu-id="c37e2-485">nominal</span></span></td>
<td><span data-ttu-id="c37e2-486">專案會修改 &quot; 低音 &quot; 、 &quot; 亮度 &quot; 、 &quot; 色彩 &quot; 、 &quot; 對比 &quot; 、 &quot; gamma &quot; 、清晰度、 &quot; &quot; &quot; 色調 &quot; 、 &quot; 高音 &quot; 和 &quot; 音量 &quot; 旗標，以傳回名義值，而不是目前的設定。</span><span class="sxs-lookup"><span data-stu-id="c37e2-486">The item modifies the &quot;bass&quot;, &quot;brightness&quot;, &quot;color&quot;, &quot;contrast&quot;, &quot;gamma&quot;, &quot;sharpness&quot;, &quot;tint&quot;, &quot;treble,&quot; and &quot;volume&quot; flags to return the nominal value instead of the current setting.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c37e2-487">名義畫面播放速率</span><span class="sxs-lookup"><span data-stu-id="c37e2-487">nominal frame rate</span></span></td>
<td><span data-ttu-id="c37e2-488">傳回與檔案相關聯的名義畫面播放速率。</span><span class="sxs-lookup"><span data-stu-id="c37e2-488">Returns the nominal frame rate associated with the file.</span></span> <span data-ttu-id="c37e2-489">單位為每秒畫面數乘以1000。</span><span class="sxs-lookup"><span data-stu-id="c37e2-489">The units are in frames per second multiplied by 1000.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c37e2-490">名義記錄畫面播放速率</span><span class="sxs-lookup"><span data-stu-id="c37e2-490">nominal record frame rate</span></span></td>
<td><span data-ttu-id="c37e2-491">傳回與輸入視訊訊號相關聯的名義畫面播放速率。</span><span class="sxs-lookup"><span data-stu-id="c37e2-491">Returns the nominal frame rate associated with the input video signal.</span></span> <span data-ttu-id="c37e2-492">單位為每秒畫面數乘以1000。</span><span class="sxs-lookup"><span data-stu-id="c37e2-492">The units are in frames per second multiplied by 1000.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c37e2-493">音訊曲目數目</span><span class="sxs-lookup"><span data-stu-id="c37e2-493">number of audio tracks</span></span></td>
<td><span data-ttu-id="c37e2-494">傳回媒體上的音訊曲目數目。</span><span class="sxs-lookup"><span data-stu-id="c37e2-494">Returns the number of audio tracks on the media.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c37e2-495">曲目數</span><span class="sxs-lookup"><span data-stu-id="c37e2-495">number of tracks</span></span></td>
<td><span data-ttu-id="c37e2-496">傳回媒體上的曲目數目。</span><span class="sxs-lookup"><span data-stu-id="c37e2-496">Returns the number of tracks on the media.</span></span> <span data-ttu-id="c37e2-497">MCISEQ 和 MCIWAVE 裝置會傳回1，就像大部分的 VCR 裝置一樣。</span><span class="sxs-lookup"><span data-stu-id="c37e2-497">The MCISEQ and MCIWAVE devices return 1, as do most VCR devices.</span></span> <span data-ttu-id="c37e2-498">MCIPIONR 裝置不支援此旗標。</span><span class="sxs-lookup"><span data-stu-id="c37e2-498">The MCIPIONR device does not support this flag.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c37e2-499">影片曲目數</span><span class="sxs-lookup"><span data-stu-id="c37e2-499">number of video tracks</span></span></td>
<td><span data-ttu-id="c37e2-500">傳回媒體上的影片曲目數目。</span><span class="sxs-lookup"><span data-stu-id="c37e2-500">Returns the number of video tracks on the media.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c37e2-501">Offset</span><span class="sxs-lookup"><span data-stu-id="c37e2-501">offset</span></span></td>
<td><span data-ttu-id="c37e2-502">傳回以 SMPTE 為基礎之檔案的位移。</span><span class="sxs-lookup"><span data-stu-id="c37e2-502">Returns the offset of a SMPTE-based file.</span></span> <span data-ttu-id="c37e2-503">位移是以 SMPTE 為基礎之序列的開始時間。</span><span class="sxs-lookup"><span data-stu-id="c37e2-503">The offset is the start time of a SMPTE-based sequence.</span></span> <span data-ttu-id="c37e2-504">時間會以 <em>hh： mm： ss： ff</em>傳回，其中 <em>hh</em> 是小時， <em>mm</em> 是分鐘， <em>ss</em> 是秒，而 <em>ff</em> 是畫面格。</span><span class="sxs-lookup"><span data-stu-id="c37e2-504">The time is returned as <em>hh:mm:ss:ff</em>, where <em>hh</em> is hours, <em>mm</em> is minutes, <em>ss</em> is seconds, and <em>ff</em> is frames.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c37e2-505">output</span><span class="sxs-lookup"><span data-stu-id="c37e2-505">output</span></span></td>
<td><span data-ttu-id="c37e2-506">傳回目前設定的輸出。</span><span class="sxs-lookup"><span data-stu-id="c37e2-506">Returns the currently set output.</span></span> <span data-ttu-id="c37e2-507">如果未設定任何輸出，則傳回的錯誤表示可以使用任何裝置。</span><span class="sxs-lookup"><span data-stu-id="c37e2-507">If no output is set, the error returned indicates that any device can be used.</span></span> <span data-ttu-id="c37e2-508">針對數位視訊裝置，修改 &quot; 低音 &quot; 、 &quot; 高音 &quot; 、 &quot; 音量 &quot; 、 &quot; 亮度 &quot; 、 &quot; 色彩 &quot; 、 &quot; 對比 &quot; 、 &quot; gamma &quot; 、 &quot; 清晰度 &quot; 或 &quot; 色調旗標， &quot; 使其僅適用于輸出。</span><span class="sxs-lookup"><span data-stu-id="c37e2-508">For digital-video devices, modifies the &quot;bass&quot;, &quot;treble&quot;, &quot;volume&quot;, &quot;brightness&quot;, &quot;color&quot;, &quot;contrast&quot;, &quot;gamma&quot;, &quot;sharpness&quot;, or &quot;tint&quot; flag so that it applies only to the output.</span></span> <span data-ttu-id="c37e2-509">這是監視檔案時的預設值。</span><span class="sxs-lookup"><span data-stu-id="c37e2-509">This is the default when monitoring a file.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c37e2-510">暫停模式</span><span class="sxs-lookup"><span data-stu-id="c37e2-510">pause mode</span></span></td>
<td><span data-ttu-id="c37e2-511">&quot; &quot; 如果裝置在錄製時暫停，則會傳回錄製。</span><span class="sxs-lookup"><span data-stu-id="c37e2-511">Returns &quot;recording&quot; if the device is paused while recording.</span></span> <span data-ttu-id="c37e2-512">&quot; &quot; 如果裝置在播放時暫停，則會傳回播放。</span><span class="sxs-lookup"><span data-stu-id="c37e2-512">It returns &quot;playing&quot; if the device is paused while playing.</span></span> <span data-ttu-id="c37e2-513">如果裝置未暫停，則會傳回 &quot; 目前模式中不適用的錯誤動作 &quot; 。</span><span class="sxs-lookup"><span data-stu-id="c37e2-513">It returns the error &quot;Action not applicable in current mode&quot; if the device is not paused.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c37e2-514">暫停 timeout</span><span class="sxs-lookup"><span data-stu-id="c37e2-514">pause timeout</span></span></td>
<td><span data-ttu-id="c37e2-515">傳回 <a href="pause.md"><strong>pause</strong></a> 命令的最長持續時間（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="c37e2-515">Returns the maximum duration, in milliseconds, of a <a href="pause.md"><strong>pause</strong></a> command.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c37e2-516">播放格式</span><span class="sxs-lookup"><span data-stu-id="c37e2-516">play format</span></span></td>
<td><span data-ttu-id="c37e2-517">傳回程序代碼，指出磁帶將播放的格式（如果可偵測）： &quot; lp &quot; 、 &quot; ep &quot; 、 &quot; sp &quot; 或 &quot; 其他 &quot; 。</span><span class="sxs-lookup"><span data-stu-id="c37e2-517">Returns a code indicating the format that the videotape will be played back in, if detectable: &quot;lp&quot;, &quot;ep&quot;, &quot;sp&quot;, or &quot;other&quot;.</span></span> <span data-ttu-id="c37e2-518">如需詳細資訊，請參閱 &quot; 記錄格式 &quot; 旗標。</span><span class="sxs-lookup"><span data-stu-id="c37e2-518">For more information, see the &quot;record format&quot; flag.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c37e2-519">播放速度</span><span class="sxs-lookup"><span data-stu-id="c37e2-519">play speed</span></span></td>
<td><span data-ttu-id="c37e2-520">傳回值，這個值表示上一個 AVI 序列的實際播放時間與目標播放時間相符的程度。</span><span class="sxs-lookup"><span data-stu-id="c37e2-520">Returns a value representing how closely the actual playing time of the last AVI sequence matched the target playing time.</span></span> <span data-ttu-id="c37e2-521">值1000表示目標時間和實際時間相同。</span><span class="sxs-lookup"><span data-stu-id="c37e2-521">The value 1000 indicates that the target time and the actual time were the same.</span></span> <span data-ttu-id="c37e2-522">例如，值為2000時，會指出 AVI 序列所花的時間比應該有兩倍的時間。</span><span class="sxs-lookup"><span data-stu-id="c37e2-522">A value of 2000, for example, would indicate that the AVI sequence took twice as long to play as it should have.</span></span> <span data-ttu-id="c37e2-523">只有 MCIAVI 數位視訊驅動程式能辨識此旗標。</span><span class="sxs-lookup"><span data-stu-id="c37e2-523">This flag is recognized only by the MCIAVI digital-video driver.</span></span> <span data-ttu-id="c37e2-524">它僅適用于效能評估;傳回值難以解讀。</span><span class="sxs-lookup"><span data-stu-id="c37e2-524">It is meant for performance evaluation only; the return value is difficult to interpret.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c37e2-525">連接埠</span><span class="sxs-lookup"><span data-stu-id="c37e2-525">port</span></span></td>
<td><span data-ttu-id="c37e2-526">傳回指派給順序的 MIDI 埠號碼。</span><span class="sxs-lookup"><span data-stu-id="c37e2-526">Returns the MIDI port number assigned to the sequence.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c37e2-527">position</span><span class="sxs-lookup"><span data-stu-id="c37e2-527">position</span></span></td>
<td><span data-ttu-id="c37e2-528">傳回目前的位置。若為 PPQN 檔案，則會以首歌指標單位傳回位置。</span><span class="sxs-lookup"><span data-stu-id="c37e2-528">Returns the current position.For PPQN files, the position is returned in song pointer units.</span></span> <span data-ttu-id="c37e2-529">對於 SMPTE 檔案，它會傳回為 <em>hh： mm： ss： ff</em>，其中 <em>hh</em> 是小時， <em>mm</em> 是分鐘，ss 是秒，而 <em>ff</em> 是畫面格。</span><span class="sxs-lookup"><span data-stu-id="c37e2-529">For SMPTE files, it is returned as <em>hh:mm:ss:ff</em>, where <em>hh</em> is hours, <em>mm</em> is minutes, ss is seconds, and <em>ff</em> is frames.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c37e2-530">開始位置</span><span class="sxs-lookup"><span data-stu-id="c37e2-530">position start</span></span></td>
<td><span data-ttu-id="c37e2-531">傳回可用媒體開始的位置。</span><span class="sxs-lookup"><span data-stu-id="c37e2-531">Returns the position of the start of the usable media.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c37e2-532">位置曲目 <em>編號</em></span><span class="sxs-lookup"><span data-stu-id="c37e2-532">position track <em>number</em></span></span></td>
<td><span data-ttu-id="c37e2-533">傳回由 <em>數位</em>指定的曲目開始位置。</span><span class="sxs-lookup"><span data-stu-id="c37e2-533">Returns the position of the start of the track specified by <em>number</em>.</span></span> <span data-ttu-id="c37e2-534">若為 PPQN 檔案，則會以首歌指標單位傳回時間格式。</span><span class="sxs-lookup"><span data-stu-id="c37e2-534">For PPQN files, the time format is returned in song pointer units.</span></span> <span data-ttu-id="c37e2-535">對於 SMPTE 檔案，它會傳回為 <em>hh： mm： ss： ff</em>，其中 <em>hh</em> 是小時， <em>mm</em> 是分鐘， <em>ss</em> 是秒，而 <em>ff</em> 是畫面格。</span><span class="sxs-lookup"><span data-stu-id="c37e2-535">For SMPTE files, it is returned as <em>hh:mm:ss:ff</em>, where <em>hh</em> is hours, <em>mm</em> is minutes, <em>ss</em> is seconds, and <em>ff</em> is frames.</span></span> <span data-ttu-id="c37e2-536">MCISEQ sequencer 會傳回零。</span><span class="sxs-lookup"><span data-stu-id="c37e2-536">The MCISEQ sequencer returns zero.</span></span> <span data-ttu-id="c37e2-537">MCIPIONR 裝置不支援此旗標。</span><span class="sxs-lookup"><span data-stu-id="c37e2-537">The MCIPIONR device does not support this flag.</span></span> <span data-ttu-id="c37e2-538">MCIWAVE 裝置會傳回零。</span><span class="sxs-lookup"><span data-stu-id="c37e2-538">The MCIWAVE device returns zero.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c37e2-539">postroll 持續期間</span><span class="sxs-lookup"><span data-stu-id="c37e2-539">postroll duration</span></span></td>
<td><span data-ttu-id="c37e2-540">傳回在發出 <a href="stop.md"><strong>stop</strong></a> 或 <a href="pause.md"><strong>pause</strong></a> 命令時，煞車 VCR 傳輸所需的磁帶長度（以目前的時間格式）。</span><span class="sxs-lookup"><span data-stu-id="c37e2-540">Returns the length of videotape, in the current time format, needed to brake the VCR transport when a <a href="stop.md"><strong>stop</strong></a> or <a href="pause.md"><strong>pause</strong></a> command is issued.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c37e2-541">開啟電源</span><span class="sxs-lookup"><span data-stu-id="c37e2-541">power on</span></span></td>
<td><span data-ttu-id="c37e2-542">如果 VCR 的電源開啟，則傳回 <strong>TRUE</strong> 。</span><span class="sxs-lookup"><span data-stu-id="c37e2-542">Returns <strong>TRUE</strong> if the VCR's power is on.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c37e2-543">預先的持續時間</span><span class="sxs-lookup"><span data-stu-id="c37e2-543">preroll duration</span></span></td>
<td><span data-ttu-id="c37e2-544">以目前時間格式傳回磁帶的長度（以目前時間格式為限），以穩定 VCR 輸出。</span><span class="sxs-lookup"><span data-stu-id="c37e2-544">Returns the length of videotape, in the current time format, needed to stabilize the VCR output.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c37e2-545">準備</span><span class="sxs-lookup"><span data-stu-id="c37e2-545">ready</span></span></td>
<td><span data-ttu-id="c37e2-546">如果裝置已準備好接受另一個命令，則會傳回 <strong>TRUE</strong> 。</span><span class="sxs-lookup"><span data-stu-id="c37e2-546">Returns <strong>TRUE</strong> if the device is ready to accept another command.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c37e2-547">記錄格式</span><span class="sxs-lookup"><span data-stu-id="c37e2-547">record format</span></span></td>
<td><span data-ttu-id="c37e2-548">傳回程序代碼，指出將在其中記錄磁帶的格式。</span><span class="sxs-lookup"><span data-stu-id="c37e2-548">Returns a code indicating the format that the videotape will be recorded in.</span></span> <span data-ttu-id="c37e2-549">目前的傳回型別為 &quot; lp &quot; 、 &quot; ep &quot; 、 &quot; sp &quot; 或 &quot; 其他類型 &quot; 。</span><span class="sxs-lookup"><span data-stu-id="c37e2-549">The current return types are &quot;lp&quot;, &quot;ep&quot;, &quot;sp&quot;, or &quot;other&quot;.</span></span> <span data-ttu-id="c37e2-550">這些格式不是 VHS 特有的，而且可以套用至任何具有多個可選取記錄格式的 VCR。</span><span class="sxs-lookup"><span data-stu-id="c37e2-550">These formats are not VHS specific and can be applied to any VCR that has multiple selectable recording formats.</span></span> <span data-ttu-id="c37e2-551">&quot;Sp &quot; 類型是最快、最高品質的錄製格式，並且在單一格式的 vcr 上當做預設值使用。</span><span class="sxs-lookup"><span data-stu-id="c37e2-551">The &quot;sp&quot; type is the fastest, highest quality recording format and is used as default on single format VCRs.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c37e2-552">記錄畫面播放速率</span><span class="sxs-lookup"><span data-stu-id="c37e2-552">record frame rate</span></span></td>
<td><span data-ttu-id="c37e2-553">傳回畫面播放速率（以每秒畫面數乘以1000），用於壓縮。</span><span class="sxs-lookup"><span data-stu-id="c37e2-553">Returns the frame rate, in frames per second multiplied by 1000, used for compression.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c37e2-554">參考 <em>框架</em></span><span class="sxs-lookup"><span data-stu-id="c37e2-554">reference <em>frame</em></span></span></td>
<td><span data-ttu-id="c37e2-555">傳回指定 <em>框架</em>之前最接近之主要畫面格影像的框架編號。</span><span class="sxs-lookup"><span data-stu-id="c37e2-555">Returns the frame number for the nearest key frame image that precedes the specified <em>frame</em>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c37e2-556">保留大小</span><span class="sxs-lookup"><span data-stu-id="c37e2-556">reserved size</span></span></td>
<td><span data-ttu-id="c37e2-557">傳回保留工作區的大小（以目前的時間格式）。</span><span class="sxs-lookup"><span data-stu-id="c37e2-557">Returns the size, in the current time format, of the reserved workspace.</span></span> <span data-ttu-id="c37e2-558">大小對應于從完整工作區播放壓縮資料所需的大約時間。</span><span class="sxs-lookup"><span data-stu-id="c37e2-558">The size corresponds to the approximate time it would take to play the compressed data from a full workspace.</span></span> <span data-ttu-id="c37e2-559">如果沒有保留的磁碟空間，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="c37e2-559">It returns zero if there is no reserved disk space.</span></span> <span data-ttu-id="c37e2-560">此旗標會傳回大約的大小，因為壓縮資料的精確磁碟空間無法在資料壓縮後才進行預測。</span><span class="sxs-lookup"><span data-stu-id="c37e2-560">This flag returns the approximate size because the precise disk space for compressed data cannot, in general, be predicted until after the data has been compressed.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c37e2-561">右磁片區</span><span class="sxs-lookup"><span data-stu-id="c37e2-561">right volume</span></span></td>
<td><span data-ttu-id="c37e2-562">傳回右邊音訊頻道的磁片區集。</span><span class="sxs-lookup"><span data-stu-id="c37e2-562">Returns the volume set for the right audio channel.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c37e2-563">samplespersec</span><span class="sxs-lookup"><span data-stu-id="c37e2-563">samplespersec</span></span></td>
<td><span data-ttu-id="c37e2-564">傳回每秒播放或錄製的樣本數。</span><span class="sxs-lookup"><span data-stu-id="c37e2-564">Returns the number of samples per second played or recorded.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c37e2-565">確切搜尋</span><span class="sxs-lookup"><span data-stu-id="c37e2-565">seek exactly</span></span></td>
<td><span data-ttu-id="c37e2-566">傳回 &quot; &quot; 或 &quot; 關閉 &quot; ，指出是否 &quot; 已設定搜尋確切旗標 &quot; 。</span><span class="sxs-lookup"><span data-stu-id="c37e2-566">Returns &quot;on&quot; or &quot;off&quot;, indicating whether or not the &quot;seek exactly&quot; flag is set.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c37e2-567">清晰度</span><span class="sxs-lookup"><span data-stu-id="c37e2-567">sharpness</span></span></td>
<td><span data-ttu-id="c37e2-568">傳回裝置目前的清晰度層級。</span><span class="sxs-lookup"><span data-stu-id="c37e2-568">Returns the current sharpness level of the device.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c37e2-569">一邊</span><span class="sxs-lookup"><span data-stu-id="c37e2-569">side</span></span></td>
<td><span data-ttu-id="c37e2-570">傳回1或2，表示載入 videodisc 的哪一端。</span><span class="sxs-lookup"><span data-stu-id="c37e2-570">Returns 1 or 2 to indicate which side of the videodisc is loaded.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c37e2-571">奴隸</span><span class="sxs-lookup"><span data-stu-id="c37e2-571">slave</span></span></td>
<td><span data-ttu-id="c37e2-572">&quot; &quot; &quot; &quot; &quot; &quot; &quot; &quot; 根據同步處理集的類型，傳回 file、midi、none 或 smpte。</span><span class="sxs-lookup"><span data-stu-id="c37e2-572">Returns &quot;file&quot; , &quot;midi&quot;, &quot;none&quot;, or &quot;smpte&quot; depending on the type of synchronization set.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c37e2-573">smpte</span><span class="sxs-lookup"><span data-stu-id="c37e2-573">smpte</span></span></td>
<td><span data-ttu-id="c37e2-574">傳回與工作區中目前位置相關聯的 SMPTE 時間碼。</span><span class="sxs-lookup"><span data-stu-id="c37e2-574">Returns the SMPTE timecode associated with the current position in the workspace.</span></span> <span data-ttu-id="c37e2-575">這是格式為 <em>dd</em>： dd： dd 的字串，其中每個 <em>d</em> 代表0到9的數位。</span><span class="sxs-lookup"><span data-stu-id="c37e2-575">This is a string with the form <em>dd:dd:dd:dd</em>, where each <em>d</em> denotes a digit from 0 to 9.</span></span> <span data-ttu-id="c37e2-576">如果工作區資料不包含時間碼資料，則此旗標會傳回00:00:00:00。</span><span class="sxs-lookup"><span data-stu-id="c37e2-576">If the workspace data does not include timecode data, then this flag returns 00:00:00:00.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c37e2-577">速度</span><span class="sxs-lookup"><span data-stu-id="c37e2-577">speed</span></span></td>
<td><span data-ttu-id="c37e2-578">以 [ <a href="https://www.bing.com/search?q=<strong>set</strong>"><strong>設定</strong></a> &quot; 速度] 命令) 所使用的相同格式，傳回裝置的目前速度（以每秒的畫面格為單位） (或相同的格式 &quot; 。</span><span class="sxs-lookup"><span data-stu-id="c37e2-578">Returns the current speed of the device in frames per second (or in the same format used by the <a href="https://www.bing.com/search?q=<strong>set</strong>"><strong>set</strong></a> &quot;speed&quot; command).</span></span> <span data-ttu-id="c37e2-579">MCIPIONR videodisc player 不支援此旗標。</span><span class="sxs-lookup"><span data-stu-id="c37e2-579">The MCIPIONR videodisc player does not support this flag.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c37e2-580">開始位置</span><span class="sxs-lookup"><span data-stu-id="c37e2-580">start position</span></span></td>
<td><span data-ttu-id="c37e2-581">傳回媒體的開始位置。</span><span class="sxs-lookup"><span data-stu-id="c37e2-581">Returns the starting position of the media.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c37e2-582">仍為檔案格式</span><span class="sxs-lookup"><span data-stu-id="c37e2-582">still file format</span></span></td>
<td><span data-ttu-id="c37e2-583">傳回 <a href="capture.md"><strong>capture</strong></a> 命令的目前檔案格式。</span><span class="sxs-lookup"><span data-stu-id="c37e2-583">Returns the current file format for the <a href="capture.md"><strong>capture</strong></a> command.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c37e2-584">Stretch - 自動縮放</span><span class="sxs-lookup"><span data-stu-id="c37e2-584">stretch</span></span></td>
<td><span data-ttu-id="c37e2-585">如果已啟用延展， <strong>則傳回 TRUE</strong> 。</span><span class="sxs-lookup"><span data-stu-id="c37e2-585">Returns <strong>TRUE</strong> if stretching is enabled.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c37e2-586">節奏</span><span class="sxs-lookup"><span data-stu-id="c37e2-586">tempo</span></span></td>
<td><span data-ttu-id="c37e2-587">傳回目前時間格式之 MIDI 序列的目前節奏。</span><span class="sxs-lookup"><span data-stu-id="c37e2-587">Returns the current tempo of a MIDI sequence in the current time format.</span></span> <span data-ttu-id="c37e2-588">針對具有 PPQN 格式的檔案，節奏是每分鐘的節拍。</span><span class="sxs-lookup"><span data-stu-id="c37e2-588">For files with PPQN format, the tempo is in beats per minute.</span></span> <span data-ttu-id="c37e2-589">針對具有 SMPTE 格式的檔案，節奏是以每秒的畫面格為單位。</span><span class="sxs-lookup"><span data-stu-id="c37e2-589">For files with SMPTE format, the tempo is in frames per second.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c37e2-590">時間格式</span><span class="sxs-lookup"><span data-stu-id="c37e2-590">time format</span></span></td>
<td><span data-ttu-id="c37e2-591">傳回目前的時間格式。</span><span class="sxs-lookup"><span data-stu-id="c37e2-591">Returns the current time format.</span></span> <span data-ttu-id="c37e2-592">如需詳細資訊，請參閱 <a href="set.md"><strong>set</strong></a> 命令中的時間格式。</span><span class="sxs-lookup"><span data-stu-id="c37e2-592">For more information, see the time formats in the <a href="set.md"><strong>set</strong></a> command.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c37e2-593">時間模式</span><span class="sxs-lookup"><span data-stu-id="c37e2-593">time mode</span></span></td>
<td><span data-ttu-id="c37e2-594">傳回目前的位置時間模式。</span><span class="sxs-lookup"><span data-stu-id="c37e2-594">Returns the current position time mode.</span></span> <span data-ttu-id="c37e2-595">它可以是 &quot; 偵測 &quot; 、時間 &quot; 碼 &quot; 或 &quot; 計數器 &quot; 。</span><span class="sxs-lookup"><span data-stu-id="c37e2-595">It can be &quot;detect&quot;, &quot;timecode&quot;, or &quot;counter&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c37e2-596">時間類型</span><span class="sxs-lookup"><span data-stu-id="c37e2-596">time type</span></span></td>
<td><span data-ttu-id="c37e2-597">傳回使用中的目前位置時間：時間 &quot; 碼 &quot; 或 &quot; 計數器 &quot; 。</span><span class="sxs-lookup"><span data-stu-id="c37e2-597">Returns the current position time in use: &quot;timecode&quot; or &quot;counter&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c37e2-598">出現的時間碼</span><span class="sxs-lookup"><span data-stu-id="c37e2-598">timecode present</span></span></td>
<td><span data-ttu-id="c37e2-599">如果已在磁帶的目前位置記錄時間碼， <strong>則傳回 TRUE</strong> 。</span><span class="sxs-lookup"><span data-stu-id="c37e2-599">Returns <strong>TRUE</strong> if timecode has been recorded at the current position on the tape.</span></span> <span data-ttu-id="c37e2-600">時間碼必須從目前的位置前進。</span><span class="sxs-lookup"><span data-stu-id="c37e2-600">The timecode must advance from the current position.</span></span> <span data-ttu-id="c37e2-601">可能必須播放 VCR 才能檢查這種情況。</span><span class="sxs-lookup"><span data-stu-id="c37e2-601">A VCR might need to be played to check this condition.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c37e2-602">時間碼記錄</span><span class="sxs-lookup"><span data-stu-id="c37e2-602">timecode record</span></span></td>
<td><span data-ttu-id="c37e2-603">如果 VCR 設定為記錄時間碼，則傳回 <strong>TRUE</strong> 。</span><span class="sxs-lookup"><span data-stu-id="c37e2-603">Returns <strong>TRUE</strong> if the VCR is set to record timecode.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c37e2-604">時間碼類型</span><span class="sxs-lookup"><span data-stu-id="c37e2-604">timecode type</span></span></td>
<td><span data-ttu-id="c37e2-605">傳回 &quot; smpte &quot; 、 &quot; smpte drop &quot; 、 &quot; other &quot; 或 &quot; none &quot; 。</span><span class="sxs-lookup"><span data-stu-id="c37e2-605">Returns &quot;smpte&quot;, &quot;smpte drop&quot;, &quot;other&quot;, or &quot;none&quot;.</span></span> <span data-ttu-id="c37e2-606">請注意，每秒畫面格數可以從 [狀態 &quot; 畫面播放速率] &quot; 命令取得，而 [ <a href="capability.md"><strong>功能</strong></a> &quot; 搜尋精確度] 命令可以傳回裝置的精確度 &quot; 。</span><span class="sxs-lookup"><span data-stu-id="c37e2-606">Note the frames per second can be obtained from the status &quot;frame rate&quot; command, and the accuracy of the device can be returned by the <a href="capability.md"><strong>capability</strong></a> &quot;seek accuracy&quot; command.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c37e2-607">色調</span><span class="sxs-lookup"><span data-stu-id="c37e2-607">tint</span></span></td>
<td><span data-ttu-id="c37e2-608">傳回目前的影片色調層級。</span><span class="sxs-lookup"><span data-stu-id="c37e2-608">Returns the current video-tint level.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c37e2-609">高音</span><span class="sxs-lookup"><span data-stu-id="c37e2-609">treble</span></span></td>
<td><span data-ttu-id="c37e2-610">傳回目前的音訊高音層級。</span><span class="sxs-lookup"><span data-stu-id="c37e2-610">Returns the current audio-treble level.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c37e2-611">調諧器數目</span><span class="sxs-lookup"><span data-stu-id="c37e2-611">tuner number</span></span></td>
<td><span data-ttu-id="c37e2-612">傳回目前的邏輯調諧器數目。</span><span class="sxs-lookup"><span data-stu-id="c37e2-612">Returns the current logical-tuner number.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c37e2-613">未儲存</span><span class="sxs-lookup"><span data-stu-id="c37e2-613">unsaved</span></span></td>
<td><span data-ttu-id="c37e2-614">如果工作區中有記錄的資料可能因為<a href="close.md"><strong>close</strong></a>、 <a href="load.md"><strong>load</strong></a>、 <a href="record.md"><strong>record</strong></a>、 <a href="reserve.md"><strong>reserve</strong></a>、<a href="cut.md"><strong>剪</strong></a>下、<a href="delete.md"><strong>刪除</strong></a>或<a href="paste.md"><strong>貼</strong></a>上命令而遺失，則傳回<strong>TRUE</strong> 。</span><span class="sxs-lookup"><span data-stu-id="c37e2-614">Returns <strong>TRUE</strong> if there is recorded data in the workspace that might be lost as a result of a <a href="close.md"><strong>close</strong></a>, <a href="load.md"><strong>load</strong></a>, <a href="record.md"><strong>record</strong></a>, <a href="reserve.md"><strong>reserve</strong></a>, <a href="cut.md"><strong>cut</strong></a>, <a href="delete.md"><strong>delete</strong></a>, or <a href="paste.md"><strong>paste</strong></a> command.</span></span> <span data-ttu-id="c37e2-615">否則傳回 <strong>FALSE</strong> 。</span><span class="sxs-lookup"><span data-stu-id="c37e2-615">Returns <strong>FALSE</strong> otherwise.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c37e2-616">影片</span><span class="sxs-lookup"><span data-stu-id="c37e2-616">video</span></span></td>
<td><span data-ttu-id="c37e2-617">傳回 &quot; &quot; 或 &quot; 關閉 &quot; ，反映 <a href="setvideo.md"><strong>setvideo</strong></a> 命令所設定的狀態。</span><span class="sxs-lookup"><span data-stu-id="c37e2-617">Returns &quot;on&quot; or &quot;off&quot;, reflecting the state set by the <a href="setvideo.md"><strong>setvideo</strong></a> command.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c37e2-618">影片按鍵色彩</span><span class="sxs-lookup"><span data-stu-id="c37e2-618">video key color</span></span></td>
<td><span data-ttu-id="c37e2-619">傳回索引鍵色彩的值。</span><span class="sxs-lookup"><span data-stu-id="c37e2-619">Returns the value for the key color.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c37e2-620">影片索引鍵索引</span><span class="sxs-lookup"><span data-stu-id="c37e2-620">video key index</span></span></td>
<td><span data-ttu-id="c37e2-621">傳回索引鍵索引的值。</span><span class="sxs-lookup"><span data-stu-id="c37e2-621">Returns the value for the key index.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c37e2-622">影片監視器</span><span class="sxs-lookup"><span data-stu-id="c37e2-622">video monitor</span></span></td>
<td><span data-ttu-id="c37e2-623">傳回 &quot; 輸出 &quot; 或其中一個有效的來源輸入類型。</span><span class="sxs-lookup"><span data-stu-id="c37e2-623">Returns &quot;output&quot; or one of the valid source-input types.</span></span> <span data-ttu-id="c37e2-624">如需詳細資訊，請參閱 <a href="setvideo.md"><strong>setvideo</strong></a> &quot; 監視器 &quot; 命令。</span><span class="sxs-lookup"><span data-stu-id="c37e2-624">For more information, see the <a href="setvideo.md"><strong>setvideo</strong></a> &quot;monitor&quot; command.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c37e2-625">影片監視器編號</span><span class="sxs-lookup"><span data-stu-id="c37e2-625">video monitor number</span></span></td>
<td><span data-ttu-id="c37e2-626">傳回狀態影片監視器所傳回之類型的受監視影片編號 &quot; &quot; 。</span><span class="sxs-lookup"><span data-stu-id="c37e2-626">Returns the monitored-video number of the type returned by status &quot;video monitor&quot;.</span></span> <span data-ttu-id="c37e2-627">如需詳細資訊，請參閱 <a href="setvideo.md">setvideo</a> 命令。</span><span class="sxs-lookup"><span data-stu-id="c37e2-627">For more information, see the <a href="setvideo.md">setvideo</a> command.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c37e2-628">影片記錄</span><span class="sxs-lookup"><span data-stu-id="c37e2-628">video record</span></span></td>
<td><span data-ttu-id="c37e2-629">傳回 &quot; &quot; 或 &quot; 關閉 &quot; ，反映 <a href="setvideo.md"><strong>setvideo</strong></a>記錄所設定的目前狀態 &quot; &quot; 。</span><span class="sxs-lookup"><span data-stu-id="c37e2-629">Returns &quot;on&quot; or &quot;off&quot;, reflecting the current state set by <a href="setvideo.md"><strong>setvideo</strong></a> &quot;record&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c37e2-630">影片記錄播放軌 <em>編號</em></span><span class="sxs-lookup"><span data-stu-id="c37e2-630">video record track <em>number</em></span></span></td>
<td><span data-ttu-id="c37e2-631">如果 VCR 設定為錄製影片，則傳回 <strong>TRUE</strong> 。</span><span class="sxs-lookup"><span data-stu-id="c37e2-631">Return <strong>TRUE</strong> if the VCR is set to record video.</span></span> <span data-ttu-id="c37e2-632">如果未指定任何追蹤編號，則會假設為預設值1。</span><span class="sxs-lookup"><span data-stu-id="c37e2-632">If no track number is given, the default value of 1 is assumed.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c37e2-633">影片來源</span><span class="sxs-lookup"><span data-stu-id="c37e2-633">video source</span></span></td>
<td><span data-ttu-id="c37e2-634">傳回影片來源類型。</span><span class="sxs-lookup"><span data-stu-id="c37e2-634">Returns the video-source type.</span></span> <span data-ttu-id="c37e2-635">如需詳細資訊，請參閱 <a href="setvideo.md"><strong>setvideo</strong></a> 命令。</span><span class="sxs-lookup"><span data-stu-id="c37e2-635">For more information, see the <a href="setvideo.md"><strong>setvideo</strong></a> command.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c37e2-636">影片來源編號</span><span class="sxs-lookup"><span data-stu-id="c37e2-636">video source number</span></span></td>
<td><span data-ttu-id="c37e2-637">傳回數位，此數位對應于所使用之類型的影片來源。</span><span class="sxs-lookup"><span data-stu-id="c37e2-637">Returns a number corresponding to the video source of the type in use.</span></span> <span data-ttu-id="c37e2-638">例如，如果使用第二個 NTSC video 來源輸入，則會傳回2。</span><span class="sxs-lookup"><span data-stu-id="c37e2-638">For example, it returns 2 if the second NTSC video source input is being used.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c37e2-639">影片串流</span><span class="sxs-lookup"><span data-stu-id="c37e2-639">video stream</span></span></td>
<td><span data-ttu-id="c37e2-640">傳回目前的視頻串流號碼。</span><span class="sxs-lookup"><span data-stu-id="c37e2-640">Returns the current video-stream number.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c37e2-641">磁碟區</span><span class="sxs-lookup"><span data-stu-id="c37e2-641">volume</span></span></td>
<td><span data-ttu-id="c37e2-642">將平均音量傳回到左邊和右邊的喇叭。</span><span class="sxs-lookup"><span data-stu-id="c37e2-642">Returns the average volume to the left and right speaker.</span></span> <span data-ttu-id="c37e2-643">如果裝置尚未播放或尚未設定磁片區，則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="c37e2-643">This returns an error if the device has not been played or volume has not been set.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c37e2-644">視窗控制碼</span><span class="sxs-lookup"><span data-stu-id="c37e2-644">window handle</span></span></td>
<td><span data-ttu-id="c37e2-645">傳回傳回值低序位字組中視窗控制碼的 ASCII 十進位值。</span><span class="sxs-lookup"><span data-stu-id="c37e2-645">Returns the ASCII decimal value for the window handle in the low-order word of the return value.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c37e2-646">視窗最大化</span><span class="sxs-lookup"><span data-stu-id="c37e2-646">window maximized</span></span></td>
<td><span data-ttu-id="c37e2-647">如果視窗最大化，則傳回 <strong>TRUE</strong> 。</span><span class="sxs-lookup"><span data-stu-id="c37e2-647">Returns <strong>TRUE</strong> if the window is maximized.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c37e2-648">視窗最小化</span><span class="sxs-lookup"><span data-stu-id="c37e2-648">window minimized</span></span></td>
<td><span data-ttu-id="c37e2-649">如果視窗最小化，則傳回 <strong>TRUE</strong> 。</span><span class="sxs-lookup"><span data-stu-id="c37e2-649">Returns <strong>TRUE</strong> if the window is minimized.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c37e2-650">視窗可見</span><span class="sxs-lookup"><span data-stu-id="c37e2-650">window visible</span></span></td>
<td><span data-ttu-id="c37e2-651">如果視窗不是隱藏的，則傳回 <strong>TRUE</strong> 。</span><span class="sxs-lookup"><span data-stu-id="c37e2-651">Returns <strong>TRUE</strong> if the window is not hidden.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c37e2-652">寫入受保護</span><span class="sxs-lookup"><span data-stu-id="c37e2-652">write protected</span></span></td>
<td><span data-ttu-id="c37e2-653">如果裝置 (偵測到寫入保護是在) 上，則會傳回 <strong>TRUE</strong> 。</span><span class="sxs-lookup"><span data-stu-id="c37e2-653">Returns <strong>TRUE</strong> if the device detects that it cannot record (that is, if the write protect is on).</span></span> <span data-ttu-id="c37e2-654">如果可以錄製，或無法判斷它是否可以記錄 (而不實際寫入) ，驅動程式會傳回 <strong>FALSE</strong>。</span><span class="sxs-lookup"><span data-stu-id="c37e2-654">If it can record, or if it is unable to determine whether or not it can record (without actually writing), the driver returns <strong>FALSE</strong>.</span></span></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="c37e2-655"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="c37e2-655"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="c37e2-656">可以是「等候」、「通知」或兩者。</span><span class="sxs-lookup"><span data-stu-id="c37e2-656">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="c37e2-657">針對數位影片和 VCR 裝置，也可以指定「測試」。</span><span class="sxs-lookup"><span data-stu-id="c37e2-657">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="c37e2-658">如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。</span><span class="sxs-lookup"><span data-stu-id="c37e2-658">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c37e2-659">傳回值</span><span class="sxs-lookup"><span data-stu-id="c37e2-659">Return Value</span></span>

<span data-ttu-id="c37e2-660">傳回 [**mciSendString**](/previous-versions//dd757161(v=vs.85))的 *lpszReturnString* 參數中的資訊。</span><span class="sxs-lookup"><span data-stu-id="c37e2-660">Returns information in the *lpszReturnString* parameter of [**mciSendString**](/previous-versions//dd757161(v=vs.85)).</span></span> <span data-ttu-id="c37e2-661">此資訊取決於要求類型。</span><span class="sxs-lookup"><span data-stu-id="c37e2-661">The information is dependent on the request type.</span></span>

## <a name="remarks"></a><span data-ttu-id="c37e2-662">備註</span><span class="sxs-lookup"><span data-stu-id="c37e2-662">Remarks</span></span>

<span data-ttu-id="c37e2-663">發出使用位置值的任何命令之前，您應該使用 [set](set.md) 命令來設定所需的時間格式。</span><span class="sxs-lookup"><span data-stu-id="c37e2-663">Before issuing any commands that use position values, you should set the desired time format by using the [set](set.md) command.</span></span>

## <a name="examples"></a><span data-ttu-id="c37e2-664">範例</span><span class="sxs-lookup"><span data-stu-id="c37e2-664">Examples</span></span>

<span data-ttu-id="c37e2-665">下列命令會傳回 "mysound" 裝置的目前模式。</span><span class="sxs-lookup"><span data-stu-id="c37e2-665">The following command returns the current mode of the "mysound" device.</span></span>

``` syntax
status mysound mode
```

## <a name="requirements"></a><span data-ttu-id="c37e2-666">規格需求</span><span class="sxs-lookup"><span data-stu-id="c37e2-666">Requirements</span></span>



| <span data-ttu-id="c37e2-667">需求</span><span class="sxs-lookup"><span data-stu-id="c37e2-667">Requirement</span></span> | <span data-ttu-id="c37e2-668">值</span><span class="sxs-lookup"><span data-stu-id="c37e2-668">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="c37e2-669">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c37e2-669">Minimum supported client</span></span><br/> | <span data-ttu-id="c37e2-670">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c37e2-670">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="c37e2-671">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c37e2-671">Minimum supported server</span></span><br/> | <span data-ttu-id="c37e2-672">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c37e2-672">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="c37e2-673">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c37e2-673">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c37e2-674">Mci</span><span class="sxs-lookup"><span data-stu-id="c37e2-674">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="c37e2-675">MCI 命令字串</span><span class="sxs-lookup"><span data-stu-id="c37e2-675">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="c37e2-676">capability</span><span class="sxs-lookup"><span data-stu-id="c37e2-676">capability</span></span>](capability.md)
</dt> <dt>

[<span data-ttu-id="c37e2-677">捕獲</span><span class="sxs-lookup"><span data-stu-id="c37e2-677">capture</span></span>](capture.md)
</dt> <dt>

[<span data-ttu-id="c37e2-678">close</span><span class="sxs-lookup"><span data-stu-id="c37e2-678">close</span></span>](close.md)
</dt> <dt>

[<span data-ttu-id="c37e2-679">削減</span><span class="sxs-lookup"><span data-stu-id="c37e2-679">cut</span></span>](cut.md)
</dt> <dt>

[<span data-ttu-id="c37e2-680">delete</span><span class="sxs-lookup"><span data-stu-id="c37e2-680">delete</span></span>](delete.md)
</dt> <dt>

[<span data-ttu-id="c37e2-681">載入</span><span class="sxs-lookup"><span data-stu-id="c37e2-681">load</span></span>](load.md)
</dt> <dt>

[<span data-ttu-id="c37e2-682">pause</span><span class="sxs-lookup"><span data-stu-id="c37e2-682">pause</span></span>](pause.md)
</dt> <dt>

[<span data-ttu-id="c37e2-683">粘貼</span><span class="sxs-lookup"><span data-stu-id="c37e2-683">paste</span></span>](paste.md)
</dt> <dt>

[<span data-ttu-id="c37e2-684">記錄</span><span class="sxs-lookup"><span data-stu-id="c37e2-684">record</span></span>](record.md)
</dt> <dt>

[<span data-ttu-id="c37e2-685">儲備</span><span class="sxs-lookup"><span data-stu-id="c37e2-685">reserve</span></span>](reserve.md)
</dt> <dt>

[<span data-ttu-id="c37e2-686">儲存</span><span class="sxs-lookup"><span data-stu-id="c37e2-686">save</span></span>](save.md)
</dt> <dt>

[<span data-ttu-id="c37e2-687">set</span><span class="sxs-lookup"><span data-stu-id="c37e2-687">set</span></span>](set.md)
</dt> <dt>

[<span data-ttu-id="c37e2-688">setaudio</span><span class="sxs-lookup"><span data-stu-id="c37e2-688">setaudio</span></span>](setaudio.md)
</dt> <dt>

[<span data-ttu-id="c37e2-689">setvideo</span><span class="sxs-lookup"><span data-stu-id="c37e2-689">setvideo</span></span>](setvideo.md)
</dt> <dt>

[<span data-ttu-id="c37e2-690">停止</span><span class="sxs-lookup"><span data-stu-id="c37e2-690">stop</span></span>](stop.md)
</dt> <dt>

[<span data-ttu-id="c37e2-691">復原</span><span class="sxs-lookup"><span data-stu-id="c37e2-691">undo</span></span>](undo.md)
</dt> </dl>

 

