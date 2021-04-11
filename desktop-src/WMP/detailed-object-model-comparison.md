---
title: 詳細的物件模型比較
description: 詳細的物件模型比較
ms.assetid: 8f08e2a6-1944-4814-b3b7-680a3722e1a0
keywords:
- Windows Media Player，物件模型
- Windows Media Player 物件模型，版本差異
- 物件模型，版本差異
- Windows Media Player ActiveX 控制項，版本差異
- ActiveX 控制項，版本差異
- Windows Media Player 的行動 ActiveX 控制項，版本差異
- Windows Media Player 行動裝置，物件模型
- 遷移指南，版本差異
- Windows Media Player 的版本，物件模型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 086607a9d367f42479e155e3273c30d88425a457
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/11/2020
ms.locfileid: "104022987"
---
# <a name="detailed-object-model-comparison"></a><span data-ttu-id="7b71b-112">詳細的物件模型比較</span><span class="sxs-lookup"><span data-stu-id="7b71b-112">Detailed Object Model Comparison</span></span>

<span data-ttu-id="7b71b-113">下表比較 Windows Media Player 6.4 物件模型屬性與 Windows Media Player 7 或更新版本的物件模型。</span><span class="sxs-lookup"><span data-stu-id="7b71b-113">The following table compares the Windows Media Player 6.4 object model properties with the Windows Media Player 7 or later object model.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7b71b-114">Windows Media Player 6.4 屬性</span><span class="sxs-lookup"><span data-stu-id="7b71b-114">Windows Media Player 6.4 property</span></span></th>
<th><span data-ttu-id="7b71b-115">Windows Media Player 7 或更新版本相等</span><span class="sxs-lookup"><span data-stu-id="7b71b-115">Windows Media Player 7 or later equivalent</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7b71b-116"><em>Player6</em>。<strong>AllowChangeDisplaySize</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-116"><em>Player6</em>.<strong>AllowChangeDisplaySize</strong></span></span></td>
<td><span data-ttu-id="7b71b-117">Windows Media Player 7 或更新版本的顯示會自動調整大小以符合媒體的大小。</span><span class="sxs-lookup"><span data-stu-id="7b71b-117">The display of Windows Media Player 7 or later automatically resizes to fit the media.</span></span> <span data-ttu-id="7b71b-118">您可以在 <OBJECT> 標記或腳本中設定 [高度] 和 [寬度] 屬性。</span><span class="sxs-lookup"><span data-stu-id="7b71b-118">You can set the height and width properties in the <OBJECT> tag or in script.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b71b-119"><em>Player6</em>。<strong>AllowScan</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-119"><em>Player6</em>.<strong>AllowScan</strong></span></span></td>
<td><span data-ttu-id="7b71b-120"><em>控制項</em>。</span><span class="sxs-lookup"><span data-stu-id="7b71b-120"><em>Controls</em>.</span></span> <span data-ttu-id="7b71b-121"><strong>fastForward</strong> 和 <em>控制項</em>。支援這些方法的檔案類型會自動啟用<strong>fastReverse</strong> 。</span><span class="sxs-lookup"><span data-stu-id="7b71b-121"><strong>fastForward</strong> and <em>Controls</em>.<strong>fastReverse</strong> are automatically enabled for file types that support these methods.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b71b-122"><em>Player6</em>。<strong>AnglesAvailable</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-122"><em>Player6</em>.<strong>AnglesAvailable</strong></span></span></td>
<td><span data-ttu-id="7b71b-123">不適用。</span><span class="sxs-lookup"><span data-stu-id="7b71b-123">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b71b-124"><em>Player6</em>。<strong>AnimationAtStart</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-124"><em>Player6</em>.<strong>AnimationAtStart</strong></span></span></td>
<td><span data-ttu-id="7b71b-125">不適用。</span><span class="sxs-lookup"><span data-stu-id="7b71b-125">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b71b-126"><em>Player6</em>。<strong>AudioStream</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-126"><em>Player6</em>.<strong>AudioStream</strong></span></span></td>
<td><span data-ttu-id="7b71b-127">使用 <em>控制項</em>。<strong>currentAudioLanguageIndex</strong>。</span><span class="sxs-lookup"><span data-stu-id="7b71b-127">Use <em>Controls</em>.<strong>currentAudioLanguageIndex</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b71b-128"><em>Player6</em>。<strong>AudioStreamsAvailable</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-128"><em>Player6</em>.<strong>AudioStreamsAvailable</strong></span></span></td>
<td><span data-ttu-id="7b71b-129">使用 <em>控制項</em>。<strong>audioLanguageCount</strong>。</span><span class="sxs-lookup"><span data-stu-id="7b71b-129">Use <em>Controls</em>.<strong>audioLanguageCount</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b71b-130"><em>Player6</em>。<strong>AutoRewind</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-130"><em>Player6</em>.<strong>AutoRewind</strong></span></span></td>
<td><span data-ttu-id="7b71b-131">使用 <em>控制項</em>。在腳本中<strong>currentPosition</strong> ，以指定或取出目前的位置。</span><span class="sxs-lookup"><span data-stu-id="7b71b-131">Use <em>Controls</em>.<strong>currentPosition</strong> in script to specify or retrieve the current position.</span></span> <span data-ttu-id="7b71b-132">或者，使用標記和 <em>播放機</em>。<strong>markerHit</strong> 事件。</span><span class="sxs-lookup"><span data-stu-id="7b71b-132">Alternatively, use markers and the <em>Player</em>.<strong>markerHit</strong> event.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b71b-133"><em>Player6</em>。自動<strong>調整</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-133"><em>Player6</em>.<strong>AutoSize</strong></span></span></td>
<td><span data-ttu-id="7b71b-134">自動調整大小是預設行為。</span><span class="sxs-lookup"><span data-stu-id="7b71b-134">Automatic sizing is the default behavior.</span></span> <span data-ttu-id="7b71b-135">若要覆寫自動調整大小，請在 <OBJECT> 標記或腳本中設定 [高度] 和 [寬度] 屬性。</span><span class="sxs-lookup"><span data-stu-id="7b71b-135">To override automatic sizing, set the height and width properties in the <OBJECT> tag or in script.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b71b-136"><em>Player6</em>。<strong>自動啟動</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-136"><em>Player6</em>.<strong>AutoStart</strong></span></span></td>
<td><span data-ttu-id="7b71b-137">使用 [ <em>設定</em>]。<strong>自動啟動</strong>。</span><span class="sxs-lookup"><span data-stu-id="7b71b-137">Use <em>Settings</em>.<strong>autoStart</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b71b-138"><em>Player6</em>。<strong>餘額</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-138"><em>Player6</em>.<strong>Balance</strong></span></span></td>
<td><span data-ttu-id="7b71b-139">使用 [ <em>設定</em>]。<strong>餘額</strong>。</span><span class="sxs-lookup"><span data-stu-id="7b71b-139">Use <em>Settings</em>.<strong>balance</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b71b-140"><em>Player6</em>。<strong>頻寬</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-140"><em>Player6</em>.<strong>Bandwidth</strong></span></span></td>
<td><span data-ttu-id="7b71b-141">使用 <em>網路</em>。<strong>頻寬</strong>。</span><span class="sxs-lookup"><span data-stu-id="7b71b-141">Use <em>Network</em>.<strong>bandWidth</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b71b-142"><em>Player6</em>。<strong>BaseURL</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-142"><em>Player6</em>.<strong>BaseURL</strong></span></span></td>
<td><span data-ttu-id="7b71b-143">使用 [ <em>設定</em>]。<strong>baseURL</strong>。</span><span class="sxs-lookup"><span data-stu-id="7b71b-143">Use <em>Settings</em>.<strong>baseURL</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b71b-144"><em>Player6</em>。<strong>BufferingCount</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-144"><em>Player6</em>.<strong>BufferingCount</strong></span></span></td>
<td><span data-ttu-id="7b71b-145">使用 <em>網路。</em><strong>bufferingCount</strong>。</span><span class="sxs-lookup"><span data-stu-id="7b71b-145">Use <em>Network.</em><strong>bufferingCount</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b71b-146"><em>Player6</em>。<strong>BufferingProgress</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-146"><em>Player6</em>.<strong>BufferingProgress</strong></span></span></td>
<td><span data-ttu-id="7b71b-147">使用 <em>網路</em>。<strong>bufferingProgress</strong>。</span><span class="sxs-lookup"><span data-stu-id="7b71b-147">Use <em>Network</em>.<strong>bufferingProgress</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b71b-148"><em>Player6</em>。<strong>BufferingTime</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-148"><em>Player6</em>.<strong>BufferingTime</strong></span></span></td>
<td><span data-ttu-id="7b71b-149">使用 <em>網路</em>。<strong>bufferingTime</strong>。</span><span class="sxs-lookup"><span data-stu-id="7b71b-149">Use <em>Network</em>.<strong>bufferingTime</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b71b-150"><em>Player6</em>。<strong>ButtonsAvailable</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-150"><em>Player6</em>.<strong>ButtonsAvailable</strong></span></span></td>
<td><span data-ttu-id="7b71b-151">不適用。</span><span class="sxs-lookup"><span data-stu-id="7b71b-151">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b71b-152"><em>Player6</em>。<strong>CanPreview</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-152"><em>Player6</em>.<strong>CanPreview</strong></span></span></td>
<td><span data-ttu-id="7b71b-153">不適用。</span><span class="sxs-lookup"><span data-stu-id="7b71b-153">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b71b-154"><em>Player6</em>。<strong>CanScan</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-154"><em>Player6</em>.<strong>CanScan</strong></span></span></td>
<td><span data-ttu-id="7b71b-155">使用 <em>控制項</em>。<strong>isAvailable</strong> (&quot; FastForward &quot;) 和 <em>控制項</em>。<strong>isAvailable</strong> (&quot; FastReverse &quot;) 。</span><span class="sxs-lookup"><span data-stu-id="7b71b-155">Use <em>Controls</em>.<strong>isAvailable</strong>(&quot;FastForward&quot;) and <em>Controls</em>.<strong>isAvailable</strong>(&quot;FastReverse&quot;).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b71b-156"><em>Player6</em>。<strong>CanSeek</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-156"><em>Player6</em>.<strong>CanSeek</strong></span></span></td>
<td><span data-ttu-id="7b71b-157">使用 <em>控制項</em>。<strong>isAvailable</strong> ，測試是否可以執行特定的 seek 方法。</span><span class="sxs-lookup"><span data-stu-id="7b71b-157">Use <em>Controls</em>.<strong>isAvailable</strong> to test whether a particular seek method can be performed.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b71b-158"><em>Player6</em>。<strong>CanSeekToMarkers</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-158"><em>Player6</em>.<strong>CanSeekToMarkers</strong></span></span></td>
<td><span data-ttu-id="7b71b-159">使用 <em>控制項</em>。<strong>isAvailable</strong> (&quot; CurrentMarker &quot;) 。</span><span class="sxs-lookup"><span data-stu-id="7b71b-159">Use <em>Controls</em>.<strong>isAvailable</strong>(&quot;CurrentMarker&quot;).</span></span> <span data-ttu-id="7b71b-160">使用 <em>媒體</em>。<strong>markerCount</strong> ，以取得特定媒體專案中的標記計數。</span><span class="sxs-lookup"><span data-stu-id="7b71b-160">Use <em>Media</em>.<strong>markerCount</strong> to retrieve the count of markers in a particular media item.</span></span> <span data-ttu-id="7b71b-161">使用 <em>控制項</em>。<strong>currentMarker</strong> 指定或取出目前的標記編號。</span><span class="sxs-lookup"><span data-stu-id="7b71b-161">Use <em>Controls</em>.<strong>currentMarker</strong> to specify or retrieve the current marker number.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b71b-162"><em>Player6</em>。<strong>CaptioningID</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-162"><em>Player6</em>.<strong>CaptioningID</strong></span></span></td>
<td><span data-ttu-id="7b71b-163">使用 <em>ClosedCaption</em>。<strong>captioningID</strong>。</span><span class="sxs-lookup"><span data-stu-id="7b71b-163">Use <em>ClosedCaption</em>.<strong>captioningID</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b71b-164"><em>Player6</em>。<strong>CCActive</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-164"><em>Player6</em>.<strong>CCActive</strong></span></span></td>
<td><span data-ttu-id="7b71b-165">不適用。</span><span class="sxs-lookup"><span data-stu-id="7b71b-165">Not available.</span></span> <span data-ttu-id="7b71b-166">如需如何在 Windows Media Player 中變更隱藏式字幕的詳細資訊，請參閱 <a href="closed-captioning.md">隱藏式字幕</a> 。</span><span class="sxs-lookup"><span data-stu-id="7b71b-166">See <a href="closed-captioning.md">Closed Captioning</a> for information about how closed captioning has changed in Windows Media Player.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b71b-167"><em>Player6</em>。<strong>ChannelDescription</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-167"><em>Player6</em>.<strong>ChannelDescription</strong></span></span></td>
<td><span data-ttu-id="7b71b-168">不適用。</span><span class="sxs-lookup"><span data-stu-id="7b71b-168">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b71b-169"><em>Player6</em>。<strong>ChannelName</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-169"><em>Player6</em>.<strong>ChannelName</strong></span></span></td>
<td><span data-ttu-id="7b71b-170">不適用。</span><span class="sxs-lookup"><span data-stu-id="7b71b-170">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b71b-171"><em>Player6</em>。<strong>ChannelURL</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-171"><em>Player6</em>.<strong>ChannelURL</strong></span></span></td>
<td><span data-ttu-id="7b71b-172">不適用。</span><span class="sxs-lookup"><span data-stu-id="7b71b-172">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b71b-173"><em>Player6</em>。<strong>ClickToPlay</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-173"><em>Player6</em>.<strong>ClickToPlay</strong></span></span></td>
<td><span data-ttu-id="7b71b-174">不適用。</span><span class="sxs-lookup"><span data-stu-id="7b71b-174">Not available.</span></span> <span data-ttu-id="7b71b-175">您應該在使用者介面中提供控制項以開始播放。</span><span class="sxs-lookup"><span data-stu-id="7b71b-175">You should provide controls in your user interface to start playback.</span></span> <span data-ttu-id="7b71b-176">或者，使用者可以用滑鼠右鍵按一下影片影像來開啟快顯功能表，其中包含<em>播放機</em>的<strong>播放/暫停</strong>選擇。<strong>enableCoNtextMenu</strong>等於 true。</span><span class="sxs-lookup"><span data-stu-id="7b71b-176">Alternatively, the user can right-click the video image to open a pop-up menu that contains a <strong>Play/Pause</strong> selection if <em>Player</em>.<strong>enableContextMenu</strong> equals true.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b71b-177"><em>Player6</em>。<strong>ClientID</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-177"><em>Player6</em>.<strong>ClientID</strong></span></span></td>
<td><span data-ttu-id="7b71b-178">無法使用。Windows Media Player 9 系列或更新版本可讓使用者選取是否要將唯一的播放程式識別碼傳送給內容提供者。</span><span class="sxs-lookup"><span data-stu-id="7b71b-178">Not available.Windows Media Player 9 Series or later allows the user to select whether a unique Player ID is transmitted to content providers.</span></span><br/> <span data-ttu-id="7b71b-179">如果使用者選取這個選項，則播放會將唯一識別碼傳送至 Windows Media 伺服器。</span><span class="sxs-lookup"><span data-stu-id="7b71b-179">If the user selects this option, the Player sends a unique ID to the Windows Media server.</span></span> <span data-ttu-id="7b71b-180">識別碼會記錄在伺服器的記錄檔中，位於中。預設為<em>system32\logfiles</em> 資料夾。</span><span class="sxs-lookup"><span data-stu-id="7b71b-180">The ID is logged in the server's log file, located in the ..<em>system32\logfiles</em> folder by default.</span></span> <span data-ttu-id="7b71b-181">記錄功能變數名稱為 &quot; c-playerid &quot; 。</span><span class="sxs-lookup"><span data-stu-id="7b71b-181">The log field name is &quot;c-playerid&quot;.</span></span> <span data-ttu-id="7b71b-182">在 Windows Media Services 中，預設不會啟用伺服器記錄。</span><span class="sxs-lookup"><span data-stu-id="7b71b-182">Server logging is not enabled by default in Windows Media Services.</span></span><br/> <span data-ttu-id="7b71b-183">如果使用者未選取此選項，伺服器會產生隨機會話識別碼，這對指定會話的每個用戶端而言是唯一的。</span><span class="sxs-lookup"><span data-stu-id="7b71b-183">If the user does not select this option, the server generates a random session ID, which is unique for each client for a given session.</span></span><br/> <span data-ttu-id="7b71b-184">如需詳細資訊，請參閱 Windows Media Services 9 系列檔。</span><span class="sxs-lookup"><span data-stu-id="7b71b-184">For more information, see the Windows Media Services 9 Series documentation.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b71b-185"><em>Player6</em>。<strong>CodecCount</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-185"><em>Player6</em>.<strong>CodecCount</strong></span></span></td>
<td><span data-ttu-id="7b71b-186">不適用。</span><span class="sxs-lookup"><span data-stu-id="7b71b-186">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b71b-187"><em>Player6</em>。<strong>>colorkey</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-187"><em>Player6</em>.<strong>ColorKey</strong></span></span></td>
<td><span data-ttu-id="7b71b-188">不適用。</span><span class="sxs-lookup"><span data-stu-id="7b71b-188">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b71b-189"><em>Player6</em>。<strong>ConnectionSpeed</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-189"><em>Player6</em>.<strong>ConnectionSpeed</strong></span></span></td>
<td><span data-ttu-id="7b71b-190">不適用。</span><span class="sxs-lookup"><span data-stu-id="7b71b-190">Not available.</span></span> <span data-ttu-id="7b71b-191">使用 <em>網路</em>。<strong>位元速率</strong> 判斷目前的位元速率。</span><span class="sxs-lookup"><span data-stu-id="7b71b-191">Use <em>Network</em>.<strong>bitRate</strong> to determine the current bit rate.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b71b-192"><em>Player6</em>。<strong>ContactAddress</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-192"><em>Player6</em>.<strong>ContactAddress</strong></span></span></td>
<td><span data-ttu-id="7b71b-193">不適用。</span><span class="sxs-lookup"><span data-stu-id="7b71b-193">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b71b-194"><em>Player6</em>。<strong>ContactEmail</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-194"><em>Player6</em>.<strong>ContactEmail</strong></span></span></td>
<td><span data-ttu-id="7b71b-195">不適用。</span><span class="sxs-lookup"><span data-stu-id="7b71b-195">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b71b-196"><em>Player6</em>。<strong>ContactPhone</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-196"><em>Player6</em>.<strong>ContactPhone</strong></span></span></td>
<td><span data-ttu-id="7b71b-197">不適用。</span><span class="sxs-lookup"><span data-stu-id="7b71b-197">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b71b-198"><em>Player6</em>。<strong>CreationDate</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-198"><em>Player6</em>.<strong>CreationDate</strong></span></span></td>
<td><span data-ttu-id="7b71b-199">使用 <em>MediaCollection</em>。<strong>getMediaAtom</strong> (&quot; CreationDate &quot;) 取得建立日期 atom 的索引。</span><span class="sxs-lookup"><span data-stu-id="7b71b-199">Use <em>MediaCollection</em>.<strong>getMediaAtom</strong>(&quot;CreationDate&quot;) to retrieve the index of the creation date atom.</span></span> <span data-ttu-id="7b71b-200">使用 <em>媒體</em>。<strong>getItemInfoByAtom</strong> 以取得中繼資料。</span><span class="sxs-lookup"><span data-stu-id="7b71b-200">Use <em>Media</em>.<strong>getItemInfoByAtom</strong> to retrieve the metadata.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b71b-201"><em>Player6</em>。<strong>CurrentAngle</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-201"><em>Player6</em>.<strong>CurrentAngle</strong></span></span></td>
<td><span data-ttu-id="7b71b-202">不適用。</span><span class="sxs-lookup"><span data-stu-id="7b71b-202">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b71b-203"><em>Player6</em>。<strong>CurrentAudioStream</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-203"><em>Player6</em>.<strong>CurrentAudioStream</strong></span></span></td>
<td><span data-ttu-id="7b71b-204">使用 <em>控制項</em>。<strong>currentAudioLanguageIndex</strong>。</span><span class="sxs-lookup"><span data-stu-id="7b71b-204">Use <em>Controls</em>.<strong>currentAudioLanguageIndex</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b71b-205"><em>Player6</em>。<strong>CurrentButton</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-205"><em>Player6</em>.<strong>CurrentButton</strong></span></span></td>
<td><span data-ttu-id="7b71b-206">不適用。</span><span class="sxs-lookup"><span data-stu-id="7b71b-206">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b71b-207"><em>Player6</em>。<strong>CurrentCCService</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-207"><em>Player6</em>.<strong>CurrentCCService</strong></span></span></td>
<td><span data-ttu-id="7b71b-208">不適用。</span><span class="sxs-lookup"><span data-stu-id="7b71b-208">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b71b-209"><em>Player6</em>。<strong>CurrentChapter</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-209"><em>Player6</em>.<strong>CurrentChapter</strong></span></span></td>
<td><span data-ttu-id="7b71b-210">取出目前的播放清單。</span><span class="sxs-lookup"><span data-stu-id="7b71b-210">Retrieve the current playlist.</span></span> <span data-ttu-id="7b71b-211">如果目前的播放清單與 <em>Cdrom</em>所傳回的播放清單不同。<strong>播放清單</strong>，則沒有最新的章節。</span><span class="sxs-lookup"><span data-stu-id="7b71b-211">If the current playlist is not the same one as the playlist returned by <em>Cdrom</em>.<strong>playlist</strong>, then there is no current chapter.</span></span> <span data-ttu-id="7b71b-212">否則，目前的章節編號是目前播放清單中目前媒體的索引。</span><span class="sxs-lookup"><span data-stu-id="7b71b-212">Otherwise, the current chapter number is the index of the current media in the current playlist.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b71b-213"><em>Player6</em>。<strong>CurrentDiscSide</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-213"><em>Player6</em>.<strong>CurrentDiscSide</strong></span></span></td>
<td><span data-ttu-id="7b71b-214">不適用。</span><span class="sxs-lookup"><span data-stu-id="7b71b-214">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b71b-215"><em>Player6</em>。<strong>CurrentDomain</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-215"><em>Player6</em>.<strong>CurrentDomain</strong></span></span></td>
<td><span data-ttu-id="7b71b-216">使用 <em>DVD</em>。<strong>網域</strong>。</span><span class="sxs-lookup"><span data-stu-id="7b71b-216">Use <em>DVD</em>.<strong>domain</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b71b-217"><em>Player6</em>。<strong>CurrentMarker</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-217"><em>Player6</em>.<strong>CurrentMarker</strong></span></span></td>
<td><span data-ttu-id="7b71b-218">使用 <em>控制項</em>。<strong>currentMarker</strong>。</span><span class="sxs-lookup"><span data-stu-id="7b71b-218">Use <em>Controls</em>.<strong>currentMarker</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b71b-219"><em>Player6</em>。<strong>CurrentPosition</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-219"><em>Player6</em>.<strong>CurrentPosition</strong></span></span></td>
<td><span data-ttu-id="7b71b-220">使用 <em>控制項</em>。<strong>currentPosition</strong>。</span><span class="sxs-lookup"><span data-stu-id="7b71b-220">Use <em>Controls</em>.<strong>currentPosition</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b71b-221"><em>Player6</em>。<strong>CurrentSubpictureStream</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-221"><em>Player6</em>.<strong>CurrentSubpictureStream</strong></span></span></td>
<td><span data-ttu-id="7b71b-222">不適用。</span><span class="sxs-lookup"><span data-stu-id="7b71b-222">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b71b-223"><em>Player6</em>。<strong>CurrentTime</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-223"><em>Player6</em>.<strong>CurrentTime</strong></span></span></td>
<td><span data-ttu-id="7b71b-224">使用 <em>控制項</em>。<strong>currentPositionTimeCode</strong>、 <em>控制項</em>。<strong>currentPositionString</strong>或 <em>控制項</em>。<strong>currentPosition。</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-224">Use <em>Controls</em>.<strong>currentPositionTimeCode</strong>, <em>Controls</em>.<strong>currentPositionString</strong>, or <em>Controls</em>.<strong>currentPosition.</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b71b-225"><em>Player6</em>。<strong>CurrentTitle</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-225"><em>Player6</em>.<strong>CurrentTitle</strong></span></span></td>
<td><span data-ttu-id="7b71b-226">取出目前的播放清單。</span><span class="sxs-lookup"><span data-stu-id="7b71b-226">Retrieve the current playlist.</span></span> <span data-ttu-id="7b71b-227">如果目前的播放清單與 <em>Cdrom</em>所傳回的播放清單相同。<strong>播放清單</strong>之後，標題號碼即為目前媒體在目前播放清單中的索引。</span><span class="sxs-lookup"><span data-stu-id="7b71b-227">If the current playlist is the same one as the playlist returned by <em>Cdrom</em>.<strong>playlist</strong>, then the title number is the index of the current media in the current playlist.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b71b-228"><em>Player6</em>。<strong>CurrentVolume</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-228"><em>Player6</em>.<strong>CurrentVolume</strong></span></span></td>
<td><span data-ttu-id="7b71b-229">不適用。</span><span class="sxs-lookup"><span data-stu-id="7b71b-229">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b71b-230"><em>Player6</em>。<strong>CursorType</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-230"><em>Player6</em>.<strong>CursorType</strong></span></span></td>
<td><span data-ttu-id="7b71b-231">不適用。</span><span class="sxs-lookup"><span data-stu-id="7b71b-231">Not available.</span></span> <span data-ttu-id="7b71b-232">請改用 Internet Explorer 的樣式。</span><span class="sxs-lookup"><span data-stu-id="7b71b-232">Use Internet Explorer styles instead.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b71b-233"><em>Player6</em>。<strong>DefaultFrame</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-233"><em>Player6</em>.<strong>DefaultFrame</strong></span></span></td>
<td><span data-ttu-id="7b71b-234">使用 [ <em>設定</em>]。<strong>defaultFrame</strong>，或使用</span><span class="sxs-lookup"><span data-stu-id="7b71b-234">Use <em>Settings</em>.<strong>defaultFrame</strong>, or use a</span></span> <PARAM> <span data-ttu-id="7b71b-235">元素中的屬性 <OBJECT> ： <pre data-space="preserve"><code><PARAM NAME=&quot;defaultFrame&quot; VALUE=&quot;right&quot;></code></pre></span><span class="sxs-lookup"><span data-stu-id="7b71b-235">attribute in the <OBJECT> element: <pre data-space="preserve"><code><PARAM NAME=&quot;defaultFrame&quot; VALUE=&quot;right&quot;></code></pre></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b71b-236"><em>Player6</em>。<strong>DisplayBackColor</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-236"><em>Player6</em>.<strong>DisplayBackColor</strong></span></span></td>
<td><span data-ttu-id="7b71b-237">不適用。</span><span class="sxs-lookup"><span data-stu-id="7b71b-237">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b71b-238"><em>Player6</em>。<strong>DisplayForeColor</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-238"><em>Player6</em>.<strong>DisplayForeColor</strong></span></span></td>
<td><span data-ttu-id="7b71b-239">不適用。</span><span class="sxs-lookup"><span data-stu-id="7b71b-239">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b71b-240"><em>Player6</em>。<strong>>displaymode</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-240"><em>Player6</em>.<strong>DisplayMode</strong></span></span></td>
<td><span data-ttu-id="7b71b-241">您可以使用<em>控制項</em><strong>以秒</strong>為單位，從開頭開始抓取目前的位置。<strong>currentPosition</strong>，格式為 HH： MM： SS (時、分、秒) 使用<em>控制項</em>的<strong>字串</strong>。使用<em>控制項</em>的<strong>currentPositionString</strong>或時間碼格式。<strong>currentPositionTimeCode</strong>。</span><span class="sxs-lookup"><span data-stu-id="7b71b-241">The current position can be retrieved in seconds from the beginning as a <strong>Number</strong> using <em>Controls</em>.<strong>currentPosition</strong>, as a <strong>String</strong> formatted as HH:MM:SS (hours, minutes, seconds) using <em>Controls</em>.<strong>currentPositionString</strong>, or in time code format using <em>Controls</em>.<strong>currentPositionTimeCode</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b71b-242"><em>Player6</em>。<strong>DisplaySize</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-242"><em>Player6</em>.<strong>DisplaySize</strong></span></span></td>
<td><span data-ttu-id="7b71b-243">預設顯示會自動調整大小以符合媒體。</span><span class="sxs-lookup"><span data-stu-id="7b71b-243">The default display automatically resizes to fit the media.</span></span> <span data-ttu-id="7b71b-244">您可以設定 <OBJECT> 標記或腳本中的高度和寬度屬性。</span><span class="sxs-lookup"><span data-stu-id="7b71b-244">You can set the height and width properties in the <OBJECT> tag, or in script.</span></span> <span data-ttu-id="7b71b-245">使用 <em>Player</em>。<strong>全</strong> 螢幕切換至全螢幕模式。</span><span class="sxs-lookup"><span data-stu-id="7b71b-245">Use <em>Player</em>.<strong>fullScreen</strong> to switch to full-screen mode.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b71b-246"><em>Player6</em>。<strong>持續時間</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-246"><em>Player6</em>.<strong>Duration</strong></span></span></td>
<td><span data-ttu-id="7b71b-247">使用 <em>媒體</em>。<strong>持續時間</strong>。</span><span class="sxs-lookup"><span data-stu-id="7b71b-247">Use <em>Media</em>.<strong>duration</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b71b-248"><em>Player6</em>。<strong>DVD</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-248"><em>Player6</em>.<strong>DVD</strong></span></span></td>
<td><span data-ttu-id="7b71b-249">使用 <em>Player</em>。<strong>DVD</strong>。</span><span class="sxs-lookup"><span data-stu-id="7b71b-249">Use <em>Player</em>.<strong>DVD</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b71b-250"><em>Player6</em>。<strong>EnableCoNtextMenu</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-250"><em>Player6</em>.<strong>EnableContextMenu</strong></span></span></td>
<td><span data-ttu-id="7b71b-251">使用 <em>Player</em>。<strong>enableCoNtextMenu</strong>。</span><span class="sxs-lookup"><span data-stu-id="7b71b-251">Use <em>Player</em>.<strong>enableContextMenu</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b71b-252"><em>Player6</em>。<strong>已啟用</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-252"><em>Player6</em>.<strong>Enabled</strong></span></span></td>
<td><span data-ttu-id="7b71b-253">使用 <em>Player</em>。<strong>已啟用</strong>。</span><span class="sxs-lookup"><span data-stu-id="7b71b-253">Use <em>Player</em>.<strong>enabled</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b71b-254"><em>Player6</em>。<strong>EnableFullScreenControls</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-254"><em>Player6</em>.<strong>EnableFullScreenControls</strong></span></span></td>
<td><span data-ttu-id="7b71b-255">使用 Windows Media Player 9 系列或更新版本時，會自動啟用全螢幕控制項，除非<em>播放玩家</em>。<strong></strong>  =  uiMode &quot;無 &quot; 。</span><span class="sxs-lookup"><span data-stu-id="7b71b-255">When using Windows Media Player 9 Series or later, full-screen controls are enabled automatically unless <em>Player</em>.<strong>uiMode</strong> = &quot;none&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b71b-256"><em>Player6</em>。<strong>EnablePositionControls</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-256"><em>Player6</em>.<strong>EnablePositionControls</strong></span></span></td>
<td><span data-ttu-id="7b71b-257">不適用。</span><span class="sxs-lookup"><span data-stu-id="7b71b-257">Not available.</span></span> <span data-ttu-id="7b71b-258">您可以提供自訂控制項或使用 <em>播放</em>。<strong>uimode</strong> 選擇預設設定。</span><span class="sxs-lookup"><span data-stu-id="7b71b-258">You can provide custom controls or use <em>Player</em>.<strong>uimode</strong> to choose a default configuration.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b71b-259"><em>Player6</em>。<strong>EnableTracker</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-259"><em>Player6</em>.<strong>EnableTracker</strong></span></span></td>
<td><span data-ttu-id="7b71b-260">不適用。</span><span class="sxs-lookup"><span data-stu-id="7b71b-260">Not available.</span></span> <span data-ttu-id="7b71b-261">您可以提供自訂控制項或使用 <em>播放</em>。<strong>uimode</strong> 選擇預設設定。</span><span class="sxs-lookup"><span data-stu-id="7b71b-261">You can provide a custom control or use <em>Player</em>.<strong>uimode</strong> to choose a default configuration.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b71b-262"><em>Player6</em>。<strong>EntryCount</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-262"><em>Player6</em>.<strong>EntryCount</strong></span></span></td>
<td><span data-ttu-id="7b71b-263">使用 <em>播放清單</em>。<strong>計數</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-263">Use <em>Playlist</em>.<strong>count</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b71b-264"><em>Player6</em>。<strong>ErrorCode</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-264"><em>Player6</em>.<strong>ErrorCode</strong></span></span></td>
<td><span data-ttu-id="7b71b-265">使用 <em>ErrorItem</em>。<strong>errorCode</strong>。</span><span class="sxs-lookup"><span data-stu-id="7b71b-265">Use <em>ErrorItem</em>.<strong>errorCode</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b71b-266"><em>Player6</em>。<strong>ErrorCorrection</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-266"><em>Player6</em>.<strong>ErrorCorrection</strong></span></span></td>
<td><span data-ttu-id="7b71b-267">不適用。</span><span class="sxs-lookup"><span data-stu-id="7b71b-267">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b71b-268"><em>Player6</em>。<strong>ErrorDescription</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-268"><em>Player6</em>.<strong>ErrorDescription</strong></span></span></td>
<td><span data-ttu-id="7b71b-269">使用 <em>ErrorItem</em>。<strong>errorDescription</strong>。</span><span class="sxs-lookup"><span data-stu-id="7b71b-269">Use <em>ErrorItem</em>.<strong>errorDescription</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b71b-270"><em>Player6</em>。<strong>檔案名</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-270"><em>Player6</em>.<strong>FileName</strong></span></span></td>
<td><span data-ttu-id="7b71b-271">使用 <em>Player</em>。<strong>URL</strong> 或 <em>播放機</em>。<strong>currentMedia</strong>。</span><span class="sxs-lookup"><span data-stu-id="7b71b-271">Use <em>Player</em>.<strong>URL</strong> or <em>Player</em>.<strong>currentMedia</strong>.</span></span> <span data-ttu-id="7b71b-272">使用 <em>控制項</em>。在播放清單中工作時<strong>currentItem</strong> 。</span><span class="sxs-lookup"><span data-stu-id="7b71b-272">Use <em>Controls</em>.<strong>currentItem</strong> when working within a playlist.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b71b-273"><em>Player6</em>。<strong>FramesPerSecond</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-273"><em>Player6</em>.<strong>FramesPerSecond</strong></span></span></td>
<td><span data-ttu-id="7b71b-274">不適用。</span><span class="sxs-lookup"><span data-stu-id="7b71b-274">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b71b-275"><em>Player6</em>。<strong>HasError</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-275"><em>Player6</em>.<strong>HasError</strong></span></span></td>
<td><span data-ttu-id="7b71b-276">使用 <em>錯誤</em>。<strong>errorCount</strong>。</span><span class="sxs-lookup"><span data-stu-id="7b71b-276">Use <em>Error</em>.<strong>errorCount</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b71b-277"><em>Player6</em>。<strong>HasMultipleItems</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-277"><em>Player6</em>.<strong>HasMultipleItems</strong></span></span></td>
<td><span data-ttu-id="7b71b-278">不適用。</span><span class="sxs-lookup"><span data-stu-id="7b71b-278">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b71b-279"><em>Player6</em>。<strong>ImageSourceHeight</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-279"><em>Player6</em>.<strong>ImageSourceHeight</strong></span></span></td>
<td><span data-ttu-id="7b71b-280">使用 <em>媒體</em>。<strong>imageSourceHeight</strong>。</span><span class="sxs-lookup"><span data-stu-id="7b71b-280">Use <em>Media</em>.<strong>imageSourceHeight</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b71b-281"><em>Player6</em>。<strong>ImageSourceWidth</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-281"><em>Player6</em>.<strong>ImageSourceWidth</strong></span></span></td>
<td><span data-ttu-id="7b71b-282">使用 <em>媒體</em>。<strong>imageSourceWidth</strong>。</span><span class="sxs-lookup"><span data-stu-id="7b71b-282">Use <em>Media</em>.<strong>imageSourceWidth</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b71b-283"><em>Player6</em>。<strong>InvokeURLs</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-283"><em>Player6</em>.<strong>InvokeURLs</strong></span></span></td>
<td><span data-ttu-id="7b71b-284">使用 [ <em>設定</em>]。<strong>invokeURLs</strong>。</span><span class="sxs-lookup"><span data-stu-id="7b71b-284">Use <em>Settings</em>.<strong>invokeURLs</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b71b-285"><em>Player6</em>。<strong>IsBroadcast</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-285"><em>Player6</em>.<strong>IsBroadcast</strong></span></span></td>
<td><span data-ttu-id="7b71b-286">使用 <em>網路</em>。<strong>sourceProtocol</strong>。</span><span class="sxs-lookup"><span data-stu-id="7b71b-286">Use <em>Network</em>.<strong>sourceProtocol</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b71b-287"><em>Player6</em>。<strong>IsDurationValid</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-287"><em>Player6</em>.<strong>IsDurationValid</strong></span></span></td>
<td><span data-ttu-id="7b71b-288">不適用。</span><span class="sxs-lookup"><span data-stu-id="7b71b-288">Not available.</span></span> <span data-ttu-id="7b71b-289"><em>媒體</em>。使用目前的媒體物件時，<strong>持續時間</strong> 包含有效的值。</span><span class="sxs-lookup"><span data-stu-id="7b71b-289"><em>Media</em>.<strong>duration</strong> contains a valid value when used with the current media object.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b71b-290"><em>Player6</em>。<strong>語言</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-290"><em>Player6</em>.<strong>Language</strong></span></span></td>
<td><span data-ttu-id="7b71b-291">使用 <em>控制項</em>。<strong>currentAudioLanguage</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-291">Use <em>Controls</em>.<strong>currentAudioLanguage</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b71b-292"><em>Player6</em>。<strong>LostPackets</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-292"><em>Player6</em>.<strong>LostPackets</strong></span></span></td>
<td><span data-ttu-id="7b71b-293">使用 <em>網路</em>。<strong>lostPackets</strong>。</span><span class="sxs-lookup"><span data-stu-id="7b71b-293">Use <em>Network</em>.<strong>lostPackets</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b71b-294"><em>Player6</em>。<strong>MarkerCount</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-294"><em>Player6</em>.<strong>MarkerCount</strong></span></span></td>
<td><span data-ttu-id="7b71b-295">使用 <em>媒體</em>。<strong>markerCount</strong>。</span><span class="sxs-lookup"><span data-stu-id="7b71b-295">Use <em>Media</em>.<strong>markerCount</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b71b-296"><em>Player6</em>。<strong>靜音</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-296"><em>Player6</em>.<strong>Mute</strong></span></span></td>
<td><span data-ttu-id="7b71b-297">使用 [ <em>設定</em>]。<strong>靜音</strong>。</span><span class="sxs-lookup"><span data-stu-id="7b71b-297">Use <em>Settings</em>.<strong>mute</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b71b-298"><em>Player6</em>。<strong>OpenState</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-298"><em>Player6</em>.<strong>OpenState</strong></span></span></td>
<td><span data-ttu-id="7b71b-299">使用 <em>Player</em>。<strong>openState</strong>。</span><span class="sxs-lookup"><span data-stu-id="7b71b-299">Use <em>Player</em>.<strong>openState</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b71b-300"><em>Player6</em>。<strong>PlayCount</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-300"><em>Player6</em>.<strong>PlayCount</strong></span></span></td>
<td><span data-ttu-id="7b71b-301">使用 [ <em>設定</em>]。<strong>playCount</strong>。</span><span class="sxs-lookup"><span data-stu-id="7b71b-301">Use <em>Settings</em>.<strong>playCount</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b71b-302"><em>Player6</em>。<strong>PlayState</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-302"><em>Player6</em>.<strong>PlayState</strong></span></span></td>
<td><span data-ttu-id="7b71b-303">使用 <em>Player</em>。<strong>playState</strong>。</span><span class="sxs-lookup"><span data-stu-id="7b71b-303">Use <em>Player</em>.<strong>playState</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b71b-304"><em>Player6</em>。<strong>PreviewMode</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-304"><em>Player6</em>.<strong>PreviewMode</strong></span></span></td>
<td><span data-ttu-id="7b71b-305">不適用。</span><span class="sxs-lookup"><span data-stu-id="7b71b-305">Not available.</span></span> <span data-ttu-id="7b71b-306">使用具有 HTML 計時器的腳本迴圈結構來複製此功能。</span><span class="sxs-lookup"><span data-stu-id="7b71b-306">Use a script loop structure with an HTML timer to duplicate this functionality.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b71b-307"><em>Player6</em>。<strong>費率</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-307"><em>Player6</em>.<strong>Rate</strong></span></span></td>
<td><span data-ttu-id="7b71b-308">使用 [ <em>設定</em>]。<strong>費率</strong>。</span><span class="sxs-lookup"><span data-stu-id="7b71b-308">Use <em>Settings</em>.<strong>rate</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b71b-309"><em>Player6</em>。<strong>ReadyState</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-309"><em>Player6</em>.<strong>ReadyState</strong></span></span></td>
<td><span data-ttu-id="7b71b-310">使用 <em>Player</em>。<strong>openState</strong>。</span><span class="sxs-lookup"><span data-stu-id="7b71b-310">Use <em>Player</em>.<strong>openState</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b71b-311"><em>Player6</em>。<strong>ReceivedPackets</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-311"><em>Player6</em>.<strong>ReceivedPackets</strong></span></span></td>
<td><span data-ttu-id="7b71b-312">使用 <em>網路</em>。<strong>receivedPackets</strong>。</span><span class="sxs-lookup"><span data-stu-id="7b71b-312">Use <em>Network</em>.<strong>receivedPackets</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b71b-313"><em>Player6</em>。<strong>ReceptionQuality</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-313"><em>Player6</em>.<strong>ReceptionQuality</strong></span></span></td>
<td><span data-ttu-id="7b71b-314">使用 <em>網路</em>。<strong>receptionQuality</strong>。</span><span class="sxs-lookup"><span data-stu-id="7b71b-314">Use <em>Network</em>.<strong>receptionQuality</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b71b-315"><em>Player6</em>。<strong>RecoveredPackets</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-315"><em>Player6</em>.<strong>RecoveredPackets</strong></span></span></td>
<td><span data-ttu-id="7b71b-316">使用 <em>網路</em>。<strong>recoveredPackets</strong>。</span><span class="sxs-lookup"><span data-stu-id="7b71b-316">Use <em>Network</em>.<strong>recoveredPackets</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b71b-317"><em>Player6</em>。<strong>根目錄</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-317"><em>Player6</em>.<strong>Root</strong></span></span></td>
<td><span data-ttu-id="7b71b-318">不適用。</span><span class="sxs-lookup"><span data-stu-id="7b71b-318">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b71b-319"><em>Player6</em>。<strong>SAMIFileName</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-319"><em>Player6</em>.<strong>SAMIFileName</strong></span></span></td>
<td><span data-ttu-id="7b71b-320">使用 <em>ClosedCaption</em>。<strong>SAMIFileName</strong>。</span><span class="sxs-lookup"><span data-stu-id="7b71b-320">Use <em>ClosedCaption</em>.<strong>SAMIFileName</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b71b-321"><em>Player6</em>。<strong>SAMILang</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-321"><em>Player6</em>.<strong>SAMILang</strong></span></span></td>
<td><span data-ttu-id="7b71b-322">使用 <em>ClosedCaption</em>。<strong>SAMILang</strong>。</span><span class="sxs-lookup"><span data-stu-id="7b71b-322">Use <em>ClosedCaption</em>.<strong>SAMILang</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b71b-323"><em>Player6</em>。<strong>SAMIStyle</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-323"><em>Player6</em>.<strong>SAMIStyle</strong></span></span></td>
<td><span data-ttu-id="7b71b-324">使用 <em>ClosedCaption</em>。<strong>SAMIStyle</strong>。</span><span class="sxs-lookup"><span data-stu-id="7b71b-324">Use <em>ClosedCaption</em>.<strong>SAMIStyle</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b71b-325"><em>Player6</em>。<strong>SelectionEnd</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-325"><em>Player6</em>.<strong>SelectionEnd</strong></span></span></td>
<td><span data-ttu-id="7b71b-326">使用<em>媒體</em>。決定<strong>媒體</strong>物件長度的<strong>持續時間</strong>。</span><span class="sxs-lookup"><span data-stu-id="7b71b-326">Use <em>Media</em>.<strong>duration</strong> to determine the length of a <strong>Media</strong> object.</span></span> <span data-ttu-id="7b71b-327">使用具有 <em>控制項</em>的標記。<strong>currentMarker</strong> 指定自訂結束位置。</span><span class="sxs-lookup"><span data-stu-id="7b71b-327">Use a marker with <em>Controls</em>.<strong>currentMarker</strong> to specify a custom end position.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b71b-328"><em>Player6</em>。<strong>SelectionStart</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-328"><em>Player6</em>.<strong>SelectionStart</strong></span></span></td>
<td><span data-ttu-id="7b71b-329">使用 <em>控制項</em>。<strong>currentPosition</strong> 從特定位置開始播放，或使用具有 <em>控制項</em>的標記。<strong>currentMarker</strong> 指定自訂開始位置。</span><span class="sxs-lookup"><span data-stu-id="7b71b-329">Use <em>Controls</em>.<strong>currentPosition</strong> to start playback from a particular position or use a marker with <em>Controls</em>.<strong>currentMarker</strong> to specify a custom start position.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b71b-330"><em>Player6</em>。<strong>SendErrorEvents</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-330"><em>Player6</em>.<strong>SendErrorEvents</strong></span></span></td>
<td><span data-ttu-id="7b71b-331">錯誤已排入佇列。</span><span class="sxs-lookup"><span data-stu-id="7b71b-331">Errors are queued.</span></span> <span data-ttu-id="7b71b-332">使用 <strong>error</strong> 物件和 <strong>ErrorItem</strong> 物件來取得錯誤資訊。</span><span class="sxs-lookup"><span data-stu-id="7b71b-332">Use the <strong>Error</strong> object and the <strong>ErrorItem</strong> object to retrieve error information.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b71b-333"><em>Player6</em>。<strong>SendKeyboardEvents</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-333"><em>Player6</em>.<strong>SendKeyboardEvents</strong></span></span></td>
<td><span data-ttu-id="7b71b-334">不適用。</span><span class="sxs-lookup"><span data-stu-id="7b71b-334">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b71b-335"><em>Player6</em>。<strong>SendMouseClickEvents</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-335"><em>Player6</em>.<strong>SendMouseClickEvents</strong></span></span></td>
<td><span data-ttu-id="7b71b-336">不適用。</span><span class="sxs-lookup"><span data-stu-id="7b71b-336">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b71b-337"><em>Player6</em>。<strong>SendMouseMoveEvents</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-337"><em>Player6</em>.<strong>SendMouseMoveEvents</strong></span></span></td>
<td><span data-ttu-id="7b71b-338">不適用。</span><span class="sxs-lookup"><span data-stu-id="7b71b-338">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b71b-339"><em>Player6</em>。<strong>SendOpenStateChangeEvents</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-339"><em>Player6</em>.<strong>SendOpenStateChangeEvents</strong></span></span></td>
<td><span data-ttu-id="7b71b-340">不適用。</span><span class="sxs-lookup"><span data-stu-id="7b71b-340">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b71b-341"><em>Player6</em>。<strong>SendPlayStateChangeEvents</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-341"><em>Player6</em>.<strong>SendPlayStateChangeEvents</strong></span></span></td>
<td><span data-ttu-id="7b71b-342">不適用。</span><span class="sxs-lookup"><span data-stu-id="7b71b-342">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b71b-343"><em>Player6</em>。<strong>SendWarningEvents</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-343"><em>Player6</em>.<strong>SendWarningEvents</strong></span></span></td>
<td><span data-ttu-id="7b71b-344">不適用。</span><span class="sxs-lookup"><span data-stu-id="7b71b-344">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b71b-345"><em>Player6</em>。<strong>ShowAudioControls</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-345"><em>Player6</em>.<strong>ShowAudioControls</strong></span></span></td>
<td><span data-ttu-id="7b71b-346">不適用。</span><span class="sxs-lookup"><span data-stu-id="7b71b-346">Not available.</span></span> <span data-ttu-id="7b71b-347">您可以提供自訂控制項或使用 <em>播放</em>。<strong>uimode</strong> 選擇預設設定。</span><span class="sxs-lookup"><span data-stu-id="7b71b-347">You can provide custom controls or use <em>Player</em>.<strong>uimode</strong> to choose a default configuration.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b71b-348"><em>Player6</em>。<strong>ShowCaptioning</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-348"><em>Player6</em>.<strong>ShowCaptioning</strong></span></span></td>
<td><span data-ttu-id="7b71b-349">不適用。</span><span class="sxs-lookup"><span data-stu-id="7b71b-349">Not available.</span></span> <span data-ttu-id="7b71b-350">您可以提供自訂的隱藏式輔助字幕顯示。</span><span class="sxs-lookup"><span data-stu-id="7b71b-350">You can provide a custom closed caption display.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b71b-351"><em>Player6</em>。<strong>ShowControls</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-351"><em>Player6</em>.<strong>ShowControls</strong></span></span></td>
<td><span data-ttu-id="7b71b-352">不適用。</span><span class="sxs-lookup"><span data-stu-id="7b71b-352">Not available.</span></span> <span data-ttu-id="7b71b-353">您可以提供自訂控制項或使用 <em>播放</em>。<strong>uimode</strong> 選擇預設設定。</span><span class="sxs-lookup"><span data-stu-id="7b71b-353">You can provide custom controls or use <em>Player</em>.<strong>uimode</strong> to choose a default configuration.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b71b-354"><em>Player6</em>。<strong>ShowDisplay</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-354"><em>Player6</em>.<strong>ShowDisplay</strong></span></span></td>
<td><span data-ttu-id="7b71b-355">不適用。</span><span class="sxs-lookup"><span data-stu-id="7b71b-355">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b71b-356"><em>Player6</em>。<strong>ShowGotoBar</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-356"><em>Player6</em>.<strong>ShowGotoBar</strong></span></span></td>
<td><span data-ttu-id="7b71b-357">不適用。</span><span class="sxs-lookup"><span data-stu-id="7b71b-357">Not available.</span></span> <span data-ttu-id="7b71b-358">您可以使用媒體物件提供自訂功能</span><span class="sxs-lookup"><span data-stu-id="7b71b-358">You can provide custom functionality using the Media object</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b71b-359"><em>Player6</em>。<strong>ShowPositionControls</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-359"><em>Player6</em>.<strong>ShowPositionControls</strong></span></span></td>
<td><span data-ttu-id="7b71b-360">不適用。</span><span class="sxs-lookup"><span data-stu-id="7b71b-360">Not available.</span></span> <span data-ttu-id="7b71b-361">您可以提供自訂控制項或使用 <em>播放</em>。<strong>uimode</strong> 選擇預設設定。</span><span class="sxs-lookup"><span data-stu-id="7b71b-361">You can provide custom controls or use <em>Player</em>.<strong>uimode</strong> to choose a default configuration.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b71b-362"><em>Player6</em>。<strong>ShowStatusBar</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-362"><em>Player6</em>.<strong>ShowStatusBar</strong></span></span></td>
<td><span data-ttu-id="7b71b-363">不適用。</span><span class="sxs-lookup"><span data-stu-id="7b71b-363">Not available.</span></span> <span data-ttu-id="7b71b-364">您可以提供自訂控制項或使用 <em>播放</em>。<strong>uimode</strong> 選擇預設設定。</span><span class="sxs-lookup"><span data-stu-id="7b71b-364">You can provide custom controls or use <em>Player</em>.<strong>uimode</strong> to choose a default configuration.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b71b-365"><em>Player6</em>。<strong>ShowTracker</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-365"><em>Player6</em>.<strong>ShowTracker</strong></span></span></td>
<td><span data-ttu-id="7b71b-366">不適用。</span><span class="sxs-lookup"><span data-stu-id="7b71b-366">Not available.</span></span> <span data-ttu-id="7b71b-367">您可以提供自訂控制項或使用 <em>播放</em>。<strong>uimode</strong> 選擇預設設定。</span><span class="sxs-lookup"><span data-stu-id="7b71b-367">You can provide custom controls or use <em>Player</em>.<strong>uimode</strong> to choose a default configuration.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b71b-368"><em>Player6</em>。<strong>SourceLink</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-368"><em>Player6</em>.<strong>SourceLink</strong></span></span></td>
<td><span data-ttu-id="7b71b-369">使用 <em>媒體</em>。<strong>sourceURL</strong>。</span><span class="sxs-lookup"><span data-stu-id="7b71b-369">Use <em>Media</em>.<strong>sourceURL</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b71b-370"><em>Player6</em>。<strong>SourceProtocol</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-370"><em>Player6</em>.<strong>SourceProtocol</strong></span></span></td>
<td><span data-ttu-id="7b71b-371">使用 <em>網路</em>。<strong>sourceProtocol</strong>。</span><span class="sxs-lookup"><span data-stu-id="7b71b-371">Use <em>Network</em>.<strong>sourceProtocol</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b71b-372"><em>Player6</em>。<strong>StreamCount</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-372"><em>Player6</em>.<strong>StreamCount</strong></span></span></td>
<td><span data-ttu-id="7b71b-373">不適用。</span><span class="sxs-lookup"><span data-stu-id="7b71b-373">Not available.</span></span> <span data-ttu-id="7b71b-374">使用 <em>控制項</em>。<strong>audioLanguageCount</strong> 可取出音訊語言資料流程的數目。</span><span class="sxs-lookup"><span data-stu-id="7b71b-374">Use <em>Controls</em>.<strong>audioLanguageCount</strong> to retrieve the number of audio language streams.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b71b-375"><em>Player6</em>。<strong>SubpictureOn</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-375"><em>Player6</em>.<strong>SubpictureOn</strong></span></span></td>
<td><span data-ttu-id="7b71b-376">不適用。</span><span class="sxs-lookup"><span data-stu-id="7b71b-376">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b71b-377"><em>Player6</em>。<strong>SubpictureStreamsAvailable</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-377"><em>Player6</em>.<strong>SubpictureStreamsAvailable</strong></span></span></td>
<td><span data-ttu-id="7b71b-378">無法使用</span><span class="sxs-lookup"><span data-stu-id="7b71b-378">Not available</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b71b-379"><em>Player6</em>。<strong>TitlesAvailable</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-379"><em>Player6</em>.<strong>TitlesAvailable</strong></span></span></td>
<td><span data-ttu-id="7b71b-380">使用下列各項：<code>Player.Cdrom.playlist.count - 1</code></span><span class="sxs-lookup"><span data-stu-id="7b71b-380">Use the following:<code>Player.Cdrom.playlist.count - 1</code></span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b71b-381"><em>Player6</em>。<strong>TotalTitleTime</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-381"><em>Player6</em>.<strong>TotalTitleTime</strong></span></span></td>
<td><span data-ttu-id="7b71b-382">使用 <em>currentMedia</em>。<strong>duration</strong> 或 <em>currentMedia</em>。<strong>durationString</strong>。</span><span class="sxs-lookup"><span data-stu-id="7b71b-382">Use <em>currentMedia</em>.<strong>duration</strong> or <em>currentMedia</em>.<strong>durationString</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b71b-383"><em>Player6</em>。<strong>TransparentAtStart</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-383"><em>Player6</em>.<strong>TransparentAtStart</strong></span></span></td>
<td><span data-ttu-id="7b71b-384">使用腳本來指定高度和寬度值，讓播放玩家可見或隱藏。</span><span class="sxs-lookup"><span data-stu-id="7b71b-384">Use script to specify the height and width values to make the player visible or invisible.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b71b-385"><em>Player6</em>。<strong>UniqueID</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-385"><em>Player6</em>.<strong>UniqueID</strong></span></span></td>
<td><span data-ttu-id="7b71b-386">不適用。</span><span class="sxs-lookup"><span data-stu-id="7b71b-386">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b71b-387"><em>Player6</em>。<strong>VideoBorder3D</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-387"><em>Player6</em>.<strong>VideoBorder3D</strong></span></span></td>
<td><span data-ttu-id="7b71b-388">不適用。</span><span class="sxs-lookup"><span data-stu-id="7b71b-388">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b71b-389"><em>Player6</em>。<strong>VideoBorderColor</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-389"><em>Player6</em>.<strong>VideoBorderColor</strong></span></span></td>
<td><span data-ttu-id="7b71b-390">不適用。</span><span class="sxs-lookup"><span data-stu-id="7b71b-390">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b71b-391"><em>Player6</em>。<strong>VideoBorderWidth</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-391"><em>Player6</em>.<strong>VideoBorderWidth</strong></span></span></td>
<td><span data-ttu-id="7b71b-392">不適用。</span><span class="sxs-lookup"><span data-stu-id="7b71b-392">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b71b-393"><em>Player6</em>。<strong>磁片</strong>區</span><span class="sxs-lookup"><span data-stu-id="7b71b-393"><em>Player6</em>.<strong>Volume</strong></span></span></td>
<td><span data-ttu-id="7b71b-394">使用 [ <em>設定</em>]。<strong>磁片</strong>區。</span><span class="sxs-lookup"><span data-stu-id="7b71b-394">Use <em>Settings</em>.<strong>Volume</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b71b-395"><em>Player6</em>。<strong>VolumesAvailable</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-395"><em>Player6</em>.<strong>VolumesAvailable</strong></span></span></td>
<td><span data-ttu-id="7b71b-396">不適用。</span><span class="sxs-lookup"><span data-stu-id="7b71b-396">Not available.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="7b71b-397">下表比較 Windows Media Player 6.4 版物件模型方法與 Windows Media Player 7 或更新版本的物件模型。</span><span class="sxs-lookup"><span data-stu-id="7b71b-397">The following table compares the Windows Media Player version 6.4 object model methods with the Windows Media Player 7 or later object model.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7b71b-398">Windows Media Player 6.4 方法</span><span class="sxs-lookup"><span data-stu-id="7b71b-398">Windows Media Player 6.4 method</span></span></th>
<th><span data-ttu-id="7b71b-399">Windows Media Player 7 或更新版本相等</span><span class="sxs-lookup"><span data-stu-id="7b71b-399">Windows Media Player 7 or later equivalent</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7b71b-400"><em>Player6</em>。<strong>AboutBox</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-400"><em>Player6</em>.<strong>AboutBox</strong></span></span></td>
<td><span data-ttu-id="7b71b-401">使用 <em>Player</em>。<strong>versionInfo</strong> ，以取得 Windows Media Player 的版本。</span><span class="sxs-lookup"><span data-stu-id="7b71b-401">Use <em>Player</em>.<strong>versionInfo</strong> to retrieve the version of Windows Media Player.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b71b-402"><em>Player6</em>。<strong>BackwardScan</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-402"><em>Player6</em>.<strong>BackwardScan</strong></span></span></td>
<td><span data-ttu-id="7b71b-403">使用 [ <em>設定</em>]。<strong>費率</strong>。</span><span class="sxs-lookup"><span data-stu-id="7b71b-403">Use <em>Settings</em>.<strong>rate</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b71b-404"><em>Player6</em>。<strong>ButtonActivate</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-404"><em>Player6</em>.<strong>ButtonActivate</strong></span></span></td>
<td><span data-ttu-id="7b71b-405">不適用。</span><span class="sxs-lookup"><span data-stu-id="7b71b-405">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b71b-406"><em>Player6</em>。<strong>ButtonSelectAndActivate</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-406"><em>Player6</em>.<strong>ButtonSelectAndActivate</strong></span></span></td>
<td><span data-ttu-id="7b71b-407">不適用。</span><span class="sxs-lookup"><span data-stu-id="7b71b-407">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b71b-408"><em>Player6</em>。<strong>取消</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-408"><em>Player6</em>.<strong>Cancel</strong></span></span></td>
<td><span data-ttu-id="7b71b-409">不適用。</span><span class="sxs-lookup"><span data-stu-id="7b71b-409">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b71b-410"><em>Player6</em>。<strong>ChapterPlay</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-410"><em>Player6</em>.<strong>ChapterPlay</strong></span></span></td>
<td><span data-ttu-id="7b71b-411">如果已經在播放指定的標題播放清單，請使用下列語法，以媒體物件的形式取出所需的章節：</span><span class="sxs-lookup"><span data-stu-id="7b71b-411">If already playing the specified title playlist, retrieve the desired chapter as a media object using the following syntax:</span></span>
<pre data-space="preserve"><code>var media = Player.currentPlaylist.item(index);</code></pre>
<span data-ttu-id="7b71b-412">然後指定 [ <em>Player</em>]。<strong>currentMedia</strong> 使用傳回的媒體物件。</span><span class="sxs-lookup"><span data-stu-id="7b71b-412">Then, specify <em>Player</em>.<strong>currentMedia</strong> using the media object returned.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b71b-413"><em>Player6</em>。<strong>ChapterPlayAutoStop</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-413"><em>Player6</em>.<strong>ChapterPlayAutoStop</strong></span></span></td>
<td><span data-ttu-id="7b71b-414">不適用。</span><span class="sxs-lookup"><span data-stu-id="7b71b-414">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b71b-415"><em>Player6</em>。<strong>ChapterSearch</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-415"><em>Player6</em>.<strong>ChapterSearch</strong></span></span></td>
<td><span data-ttu-id="7b71b-416">如果已經在播放指定的標題播放清單，請使用下列語法，以媒體物件的形式取出所需的章節：</span><span class="sxs-lookup"><span data-stu-id="7b71b-416">If already playing the specified title playlist, retrieve the desired chapter as a media object using the following syntax:</span></span>
<pre data-space="preserve"><code>var media = Player.currentPlaylist.item(index);</code></pre>
<span data-ttu-id="7b71b-417">然後指定 [ <em>Player</em>]。<strong>currentMedia</strong> 使用傳回的媒體物件。</span><span class="sxs-lookup"><span data-stu-id="7b71b-417">Then, specify <em>Player</em>.<strong>currentMedia</strong> using the media object returned.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b71b-418"><em>Player6</em>。<strong>FastForward</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-418"><em>Player6</em>.<strong>FastForward</strong></span></span></td>
<td><span data-ttu-id="7b71b-419">使用 <em>控制項</em>。<strong>fastForward</strong>。</span><span class="sxs-lookup"><span data-stu-id="7b71b-419">Use <em>Controls</em>.<strong>fastForward</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b71b-420"><em>Player6</em>。<strong>FastReverse</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-420"><em>Player6</em>.<strong>FastReverse</strong></span></span></td>
<td><span data-ttu-id="7b71b-421">使用 <em>控制項</em>。<strong>fastReverse</strong>。</span><span class="sxs-lookup"><span data-stu-id="7b71b-421">Use <em>Controls</em>.<strong>fastReverse</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b71b-422"><em>Player6</em>。<strong>ForwardScan</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-422"><em>Player6</em>.<strong>ForwardScan</strong></span></span></td>
<td><span data-ttu-id="7b71b-423">使用 [ <em>設定</em>]。<strong>費率</strong>。</span><span class="sxs-lookup"><span data-stu-id="7b71b-423">Use <em>Settings</em>.<strong>rate</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b71b-424"><em>Player6</em>。<strong>GetAllGPRMs</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-424"><em>Player6</em>.<strong>GetAllGPRMs</strong></span></span></td>
<td><span data-ttu-id="7b71b-425">不適用。</span><span class="sxs-lookup"><span data-stu-id="7b71b-425">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b71b-426"><em>Player6</em>。<strong>GetAllSPRMs</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-426"><em>Player6</em>.<strong>GetAllSPRMs</strong></span></span></td>
<td><span data-ttu-id="7b71b-427">不適用。</span><span class="sxs-lookup"><span data-stu-id="7b71b-427">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b71b-428"><em>Player6</em>。<strong>GetAudioLanguage</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-428"><em>Player6</em>.<strong>GetAudioLanguage</strong></span></span></td>
<td><span data-ttu-id="7b71b-429">使用 <em>控制項</em>。<strong>currentAudioLanguage</strong> ，以取得目前音訊語言的 LCID。</span><span class="sxs-lookup"><span data-stu-id="7b71b-429">Use <em>Controls</em>.<strong>currentAudioLanguage</strong> to retrieve the LCID of the current audio language.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b71b-430"><em>Player6</em>。<strong>GetCodecDescription</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-430"><em>Player6</em>.<strong>GetCodecDescription</strong></span></span></td>
<td><span data-ttu-id="7b71b-431">不適用。</span><span class="sxs-lookup"><span data-stu-id="7b71b-431">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b71b-432"><em>Player6</em>。<strong>GetCodecInstalled</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-432"><em>Player6</em>.<strong>GetCodecInstalled</strong></span></span></td>
<td><span data-ttu-id="7b71b-433">不適用。</span><span class="sxs-lookup"><span data-stu-id="7b71b-433">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b71b-434"><em>Player6</em>。<strong>GetCodecURL</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-434"><em>Player6</em>.<strong>GetCodecURL</strong></span></span></td>
<td><span data-ttu-id="7b71b-435">使用 <em>ErrorItem</em>。<strong>customUrl</strong>。</span><span class="sxs-lookup"><span data-stu-id="7b71b-435">Use <em>ErrorItem</em>.<strong>customUrl</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b71b-436"><em>Player6</em>。<strong>GetCurrentEntry</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-436"><em>Player6</em>.<strong>GetCurrentEntry</strong></span></span></td>
<td><span data-ttu-id="7b71b-437">使用腳本對目前的播放清單執行迴圈。</span><span class="sxs-lookup"><span data-stu-id="7b71b-437">Use script to loop through the current playlist.</span></span> <span data-ttu-id="7b71b-438">使用 <em>媒體</em>。<strong>isIdentical</strong> ，將播放清單中的每個專案與 <em>播放</em>清單進行比較。<strong>currentMedia</strong> 物件。</span><span class="sxs-lookup"><span data-stu-id="7b71b-438">Use <em>Media</em>.<strong>isIdentical</strong> to compare each entry in the playlist to the <em>Player</em>.<strong>currentMedia</strong> object.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b71b-439"><em>Player6</em>。<strong>GetMarkerName</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-439"><em>Player6</em>.<strong>GetMarkerName</strong></span></span></td>
<td><span data-ttu-id="7b71b-440">使用 <em>媒體</em>。<strong>getMarkerName</strong>。</span><span class="sxs-lookup"><span data-stu-id="7b71b-440">Use <em>Media</em>.<strong>getMarkerName</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b71b-441"><em>Player6</em>。<strong>GetMarkerTime</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-441"><em>Player6</em>.<strong>GetMarkerTime</strong></span></span></td>
<td><span data-ttu-id="7b71b-442">使用 <em>媒體</em>。<strong>getMarkerTime</strong>。</span><span class="sxs-lookup"><span data-stu-id="7b71b-442">Use <em>Media</em>.<strong>getMarkerTime</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b71b-443"><em>Player6</em>。<strong>GetMediaInfoString</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-443"><em>Player6</em>.<strong>GetMediaInfoString</strong></span></span></td>
<td><span data-ttu-id="7b71b-444">使用 <em>媒體</em>。<strong>getItemInfo</strong>、 <em>Media</em>。<strong>getItemInfoByAtom</strong>及其相關聯的方法，以取得中繼資料。</span><span class="sxs-lookup"><span data-stu-id="7b71b-444">Use <em>Media</em>.<strong>getItemInfo</strong>, <em>Media</em>.<strong>getItemInfoByAtom</strong>, and their associated methods to retrieve metadata.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b71b-445"><em>Player6</em>。<strong>GetMediaParameter</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-445"><em>Player6</em>.<strong>GetMediaParameter</strong></span></span></td>
<td><span data-ttu-id="7b71b-446">使用 <em>播放清單</em>。取得媒體專案的<strong>專案</strong> 。</span><span class="sxs-lookup"><span data-stu-id="7b71b-446">Use <em>Playlist</em>.<strong>item</strong> to retrieve a media item.</span></span> <span data-ttu-id="7b71b-447">然後使用 <em>媒體</em>。<strong>getItemInfo</strong> 以取得參數字串。</span><span class="sxs-lookup"><span data-stu-id="7b71b-447">Then use <em>Media</em>.<strong>getItemInfo</strong> to retrieve the parameter string.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b71b-448"><em>Player6</em>。<strong>GetMediaParameterName</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-448"><em>Player6</em>.<strong>GetMediaParameterName</strong></span></span></td>
<td><span data-ttu-id="7b71b-449">使用 <em>播放清單</em>。取得媒體專案的<strong>專案</strong> 。</span><span class="sxs-lookup"><span data-stu-id="7b71b-449">Use <em>Playlist</em>.<strong>item</strong> to retrieve a media item.</span></span> <span data-ttu-id="7b71b-450">然後使用 <em>媒體</em>。<strong>getAttributeName</strong> 以取得參數字串。</span><span class="sxs-lookup"><span data-stu-id="7b71b-450">Then use <em>Media</em>.<strong>getAttributeName</strong> to retrieve the parameter string.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b71b-451"><em>Player6</em>。<strong>GetMoreInfoURL</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-451"><em>Player6</em>.<strong>GetMoreInfoURL</strong></span></span></td>
<td><span data-ttu-id="7b71b-452">不適用。</span><span class="sxs-lookup"><span data-stu-id="7b71b-452">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b71b-453"><em>Player6</em>。<strong>GetNumberOfChapters</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-453"><em>Player6</em>.<strong>GetNumberOfChapters</strong></span></span></td>
<td><span data-ttu-id="7b71b-454">如果目前現正播放標題，請使用 <em>currentPlaylist</em>。<strong>計數</strong>。</span><span class="sxs-lookup"><span data-stu-id="7b71b-454">If a title is currently playing, use <em>currentPlaylist</em>.<strong>count</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b71b-455"><em>Player6</em>。<strong>GetStreamGroup</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-455"><em>Player6</em>.<strong>GetStreamGroup</strong></span></span></td>
<td><span data-ttu-id="7b71b-456">不適用。</span><span class="sxs-lookup"><span data-stu-id="7b71b-456">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b71b-457"><em>Player6</em>。<strong>GetStreamName</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-457"><em>Player6</em>.<strong>GetStreamName</strong></span></span></td>
<td><span data-ttu-id="7b71b-458">不適用。</span><span class="sxs-lookup"><span data-stu-id="7b71b-458">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b71b-459"><em>Player6</em>。<strong>GetStreamSelected</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-459"><em>Player6</em>.<strong>GetStreamSelected</strong></span></span></td>
<td><span data-ttu-id="7b71b-460">不適用。</span><span class="sxs-lookup"><span data-stu-id="7b71b-460">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b71b-461"><em>Player6</em>。<strong>GetSubpictureLanguage</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-461"><em>Player6</em>.<strong>GetSubpictureLanguage</strong></span></span></td>
<td><span data-ttu-id="7b71b-462">不適用。</span><span class="sxs-lookup"><span data-stu-id="7b71b-462">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b71b-463"><em>Player6</em>。<strong>群組</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-463"><em>Player6</em>.<strong>GoUp</strong></span></span></td>
<td><span data-ttu-id="7b71b-464">使用 <em>DVD</em>。<strong>回來</strong>。</span><span class="sxs-lookup"><span data-stu-id="7b71b-464">Use <em>DVD</em>.<strong>back</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b71b-465"><em>Player6</em>。<strong>IsSoundCardEnabled</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-465"><em>Player6</em>.<strong>IsSoundCardEnabled</strong></span></span></td>
<td><span data-ttu-id="7b71b-466">不適用。</span><span class="sxs-lookup"><span data-stu-id="7b71b-466">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b71b-467"><em>Player6</em>。<strong>LeftButtonSelect</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-467"><em>Player6</em>.<strong>LeftButtonSelect</strong></span></span></td>
<td><span data-ttu-id="7b71b-468">不適用。</span><span class="sxs-lookup"><span data-stu-id="7b71b-468">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b71b-469"><em>Player6</em>。<strong>LowerButtonSelect</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-469"><em>Player6</em>.<strong>LowerButtonSelect</strong></span></span></td>
<td><span data-ttu-id="7b71b-470">不適用。</span><span class="sxs-lookup"><span data-stu-id="7b71b-470">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b71b-471"><em>Player6</em>。<strong>MenuCall</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-471"><em>Player6</em>.<strong>MenuCall</strong></span></span></td>
<td><span data-ttu-id="7b71b-472">使用 <em>DVD</em>。<strong>titleMenu</strong> 或 <em>DVD</em>。<strong>topMenu</strong>。</span><span class="sxs-lookup"><span data-stu-id="7b71b-472">Use <em>DVD</em>.<strong>titleMenu</strong> or <em>DVD</em>.<strong>topMenu</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b71b-473"><em>Player6</em>。<strong>下一步</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-473"><em>Player6</em>.<strong>Next</strong></span></span></td>
<td><span data-ttu-id="7b71b-474">使用 <em>控制項</em>。<strong>接下來</strong>。</span><span class="sxs-lookup"><span data-stu-id="7b71b-474">Use <em>Controls</em>.<strong>next</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b71b-475"><em>Player6</em>。<strong>NextPGSearch</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-475"><em>Player6</em>.<strong>NextPGSearch</strong></span></span></td>
<td><span data-ttu-id="7b71b-476">使用 <em>控制項</em>。<strong>接下來</strong>。</span><span class="sxs-lookup"><span data-stu-id="7b71b-476">Use <em>Controls</em>.<strong>next</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b71b-477"><em>Player6</em>。<strong>開啟</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-477"><em>Player6</em>.<strong>Open</strong></span></span></td>
<td><span data-ttu-id="7b71b-478">使用 <em>Player</em>。<strong>URL</strong> 或 <em>播放機</em>。<strong>currentMedia</strong>。</span><span class="sxs-lookup"><span data-stu-id="7b71b-478">Use <em>Player</em>.<strong>URL</strong> or <em>Player</em>.<strong>currentMedia</strong>.</span></span> <span data-ttu-id="7b71b-479">檔案一律會以非同步方式開啟。</span><span class="sxs-lookup"><span data-stu-id="7b71b-479">Files always open asynchronously.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b71b-480"><em>Player6</em>。<strong>暫停</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-480"><em>Player6</em>.<strong>Pause</strong></span></span></td>
<td><span data-ttu-id="7b71b-481">使用 <em>控制項</em>。<strong>暫停</strong>。</span><span class="sxs-lookup"><span data-stu-id="7b71b-481">Use <em>Controls</em>.<strong>pause</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b71b-482"><em>Player6</em>。<strong>播放</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-482"><em>Player6</em>.<strong>Play</strong></span></span></td>
<td><span data-ttu-id="7b71b-483">使用 <em>控制項</em>。<strong>玩</strong>。</span><span class="sxs-lookup"><span data-stu-id="7b71b-483">Use <em>Controls</em>.<strong>play</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b71b-484"><em>Player6</em>。<strong>上一個</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-484"><em>Player6</em>.<strong>Previous</strong></span></span></td>
<td><span data-ttu-id="7b71b-485">使用 <em>控制項</em>。<strong>上一步</strong>。</span><span class="sxs-lookup"><span data-stu-id="7b71b-485">Use <em>Controls</em>.<strong>previous</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b71b-486"><em>Player6</em>。<strong>PrevPGSearch</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-486"><em>Player6</em>.<strong>PrevPGSearch</strong></span></span></td>
<td><span data-ttu-id="7b71b-487">使用 <em>控制項</em>。<strong>上一步</strong>。</span><span class="sxs-lookup"><span data-stu-id="7b71b-487">Use <em>Controls</em>.<strong>previous</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b71b-488"><em>Player6</em>。<strong>ResumeFromMenu</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-488"><em>Player6</em>.<strong>ResumeFromMenu</strong></span></span></td>
<td><span data-ttu-id="7b71b-489">使用 <em>DVD</em>。<strong>繼續</strong>。</span><span class="sxs-lookup"><span data-stu-id="7b71b-489">Use <em>DVD</em>.<strong>resume</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b71b-490"><em>Player6</em>。<strong>RightButtonSelect</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-490"><em>Player6</em>.<strong>RightButtonSelect</strong></span></span></td>
<td><span data-ttu-id="7b71b-491">不適用。</span><span class="sxs-lookup"><span data-stu-id="7b71b-491">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b71b-492"><em>Player6</em>。<strong>SetCurrentEntry</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-492"><em>Player6</em>.<strong>SetCurrentEntry</strong></span></span></td>
<td><span data-ttu-id="7b71b-493">使用<em>currentPlaylist</em>取出媒體物件。 (<em>entryNumber</em>) 的<strong>專案</strong>。</span><span class="sxs-lookup"><span data-stu-id="7b71b-493">Retrieve a media object using <em>currentPlaylist</em>.<strong>item</strong>(<em>entryNumber</em>).</span></span> <span data-ttu-id="7b71b-494">然後，使用 <em>控制項</em>來指定抓取的媒體物件。<strong>currentItem</strong>。</span><span class="sxs-lookup"><span data-stu-id="7b71b-494">Then, specify the retrieved media object using <em>Controls</em>.<strong>currentItem</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b71b-495"><em>Player6</em>。<strong>ShowDialog</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-495"><em>Player6</em>.<strong>ShowDialog</strong></span></span></td>
<td><span data-ttu-id="7b71b-496">不適用。</span><span class="sxs-lookup"><span data-stu-id="7b71b-496">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b71b-497"><em>Player6</em>。<strong>StillOff</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-497"><em>Player6</em>.<strong>StillOff</strong></span></span></td>
<td><span data-ttu-id="7b71b-498">使用 <em>控制項</em>。<strong>玩</strong>。</span><span class="sxs-lookup"><span data-stu-id="7b71b-498">Use <em>Controls</em>.<strong>play</strong>.</span></span> <span data-ttu-id="7b71b-499">或者，使用 <em>控制項</em>。<strong>接下來</strong> ，如果目前處於仍處於模式中。</span><span class="sxs-lookup"><span data-stu-id="7b71b-499">Alternatively, use <em>Controls</em>.<strong>Next</strong> if currently in still mode.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b71b-500"><em>Player6</em>。<strong>停止</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-500"><em>Player6</em>.<strong>Stop</strong></span></span></td>
<td><span data-ttu-id="7b71b-501">使用 <em>控制項</em>。<strong>停止</strong>。</span><span class="sxs-lookup"><span data-stu-id="7b71b-501">Use <em>Controls</em>.<strong>stop</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b71b-502"><em>Player6</em>。<strong>StreamSelect</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-502"><em>Player6</em>.<strong>StreamSelect</strong></span></span></td>
<td><span data-ttu-id="7b71b-503">不適用。</span><span class="sxs-lookup"><span data-stu-id="7b71b-503">Not available.</span></span> <span data-ttu-id="7b71b-504">使用 <em>控制項</em>。<strong>currentAudioLanguage</strong> 指定音訊語言資料流程。</span><span class="sxs-lookup"><span data-stu-id="7b71b-504">Use <em>Controls</em>.<strong>currentAudioLanguage</strong> to specify an audio language stream.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b71b-505"><em>Player6</em>。<strong>TimePlay</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-505"><em>Player6</em>.<strong>TimePlay</strong></span></span></td>
<td><span data-ttu-id="7b71b-506">從根播放清單中，使用<em>currentPlaylist</em>。取得媒體物件的 (<em>索引</em>) <strong>專案</strong>。</span><span class="sxs-lookup"><span data-stu-id="7b71b-506">From the root playlist, use <em>currentPlaylist</em>.<strong>item</strong>(<em>index</em>) to retrieve a media object.</span></span> <span data-ttu-id="7b71b-507">然後，使用 <em>控制項</em>將媒體物件設定為目前的物件。<strong>currentItem</strong>。</span><span class="sxs-lookup"><span data-stu-id="7b71b-507">Then, set the media object as the current one using <em>Controls</em>.<strong>currentItem</strong>.</span></span> <span data-ttu-id="7b71b-508">然後，指定 <em>控制項</em>。<strong>currentPosition</strong> 使用時間值（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="7b71b-508">Then, specify <em>Controls</em>.<strong>currentPosition</strong> using a time value in seconds.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b71b-509"><em>Player6</em>。<strong>TimeSearch</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-509"><em>Player6</em>.<strong>TimeSearch</strong></span></span></td>
<td><span data-ttu-id="7b71b-510">使用 <em>控制項</em>。<strong>currentPosition</strong>。</span><span class="sxs-lookup"><span data-stu-id="7b71b-510">Use <em>Controls</em>.<strong>currentPosition</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b71b-511"><em>Player6</em>。<strong>TitlePlay</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-511"><em>Player6</em>.<strong>TitlePlay</strong></span></span></td>
<td><span data-ttu-id="7b71b-512">如果已經在播放指定的標題播放清單，請使用下列語法，以媒體物件的形式取出所需的章節：</span><span class="sxs-lookup"><span data-stu-id="7b71b-512">If already playing the specified title playlist, retrieve the desired chapter as a media object using the following syntax:</span></span>
<pre data-space="preserve"><code>var media = Player.currentPlaylist.item(index);</code></pre>
<span data-ttu-id="7b71b-513">然後指定 [ <em>Player</em>]。<strong>currentMedia</strong> 使用傳回的媒體物件。</span><span class="sxs-lookup"><span data-stu-id="7b71b-513">Then, specify <em>Player</em>.<strong>currentMedia</strong> using the media object returned.</span></span><br/> <span data-ttu-id="7b71b-514">或者，使用 <em>currentPlaylist</em>。取得媒體物件的<strong>專案</strong> ，然後使用傳回的媒體物件來指定 <em>控制項</em>。<strong>currentItem</strong>。</span><span class="sxs-lookup"><span data-stu-id="7b71b-514">Alternatively, use <em>currentPlaylist</em>.<strong>item</strong> to retrieve a media object, and then use the media object returned to specify <em>Controls</em>.<strong>currentItem</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b71b-515"><em>Player6</em>。<strong>TopPGSearch</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-515"><em>Player6</em>.<strong>TopPGSearch</strong></span></span></td>
<td><span data-ttu-id="7b71b-516">不適用。</span><span class="sxs-lookup"><span data-stu-id="7b71b-516">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b71b-517"><em>Player6</em>。<strong>UOPValid</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-517"><em>Player6</em>.<strong>UOPValid</strong></span></span></td>
<td><span data-ttu-id="7b71b-518">無法使用</span><span class="sxs-lookup"><span data-stu-id="7b71b-518">Not available</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b71b-519"><em>Player6</em>。<strong>UpperButtonSelect</strong></span><span class="sxs-lookup"><span data-stu-id="7b71b-519"><em>Player6</em>.<strong>UpperButtonSelect</strong></span></span></td>
<td><span data-ttu-id="7b71b-520">不適用。</span><span class="sxs-lookup"><span data-stu-id="7b71b-520">Not available.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="7b71b-521">下表比較 Windows Media Player 6.4 版物件模型事件與 Windows Media Player 7 或更新版本的物件模型。</span><span class="sxs-lookup"><span data-stu-id="7b71b-521">The following table compares the Windows Media Player version 6.4 object model events with the Windows Media Player 7 or later object model.</span></span>



| <span data-ttu-id="7b71b-522">Windows Media Player 6.4 事件</span><span class="sxs-lookup"><span data-stu-id="7b71b-522">Windows Media Player 6.4 event</span></span>  | <span data-ttu-id="7b71b-523">Windows Media Player 7 或更新版本相等</span><span class="sxs-lookup"><span data-stu-id="7b71b-523">Windows Media Player 7 or later equivalent</span></span>                                                                                                                                                                               |
|---------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b71b-524">*Player6*。**緩衝**</span><span class="sxs-lookup"><span data-stu-id="7b71b-524">*Player6*.**Buffering**</span></span>         | <span data-ttu-id="7b71b-525">使用 *Player*。**緩衝** 處理。</span><span class="sxs-lookup"><span data-stu-id="7b71b-525">Use *Player*.**Buffering**.</span></span>                                                                                                                                                                                              |
| <span data-ttu-id="7b71b-526">*Player6*。**按一下**</span><span class="sxs-lookup"><span data-stu-id="7b71b-526">*Player6*.**Click**</span></span>             | <span data-ttu-id="7b71b-527">使用 *Player*。**按一下**</span><span class="sxs-lookup"><span data-stu-id="7b71b-527">Use *Player*.**Click**</span></span>                                                                                                                                                                                                   |
| <span data-ttu-id="7b71b-528">*Player6*。**DblClick**</span><span class="sxs-lookup"><span data-stu-id="7b71b-528">*Player6*.**DblClick**</span></span>          | <span data-ttu-id="7b71b-529">使用 *Player*。**DoubleClick**</span><span class="sxs-lookup"><span data-stu-id="7b71b-529">Use *Player*.**DoubleClick**</span></span>                                                                                                                                                                                             |
| <span data-ttu-id="7b71b-530">*Player6*。**中斷** 連線</span><span class="sxs-lookup"><span data-stu-id="7b71b-530">*Player6*.**Disconnect**</span></span>        | <span data-ttu-id="7b71b-531">不適用。</span><span class="sxs-lookup"><span data-stu-id="7b71b-531">Not available.</span></span>                                                                                                                                                                                                           |
| <span data-ttu-id="7b71b-532">*Player6*。**DisplayModeChange**</span><span class="sxs-lookup"><span data-stu-id="7b71b-532">*Player6*.**DisplayModeChange**</span></span> | <span data-ttu-id="7b71b-533">不適用。</span><span class="sxs-lookup"><span data-stu-id="7b71b-533">Not available.</span></span>                                                                                                                                                                                                           |
| <span data-ttu-id="7b71b-534">*Player6*。**DVDNotify**</span><span class="sxs-lookup"><span data-stu-id="7b71b-534">*Player6*.**DVDNotify**</span></span>         | <span data-ttu-id="7b71b-535">*玩家*。**DomainChange** 和 *Player*。**OpenPlaylistSwitch** 是 DVD 特定的事件。</span><span class="sxs-lookup"><span data-stu-id="7b71b-535">*Player*.**DomainChange** and *Player*.**OpenPlaylistSwitch** are DVD-specific events.</span></span> <span data-ttu-id="7b71b-536">與播放清單、媒體和 CD-ROM 媒體相關的其他事件，也可能會根據應用程式而套用。</span><span class="sxs-lookup"><span data-stu-id="7b71b-536">Other events related to playlists, media, and CD-ROM media may apply as well depending on the application.</span></span>                        |
| <span data-ttu-id="7b71b-537">*Player6*。**EndOfStream**</span><span class="sxs-lookup"><span data-stu-id="7b71b-537">*Player6*.**EndOfStream**</span></span>       | <span data-ttu-id="7b71b-538">使用 *Player*。**PlayState**。</span><span class="sxs-lookup"><span data-stu-id="7b71b-538">Use *Player*.**PlayState**.</span></span>                                                                                                                                                                                              |
| <span data-ttu-id="7b71b-539">*Player6*。**錯誤**</span><span class="sxs-lookup"><span data-stu-id="7b71b-539">*Player6*.**Error**</span></span>             | <span data-ttu-id="7b71b-540">事件未變更。</span><span class="sxs-lookup"><span data-stu-id="7b71b-540">The event is unchanged.</span></span> <span data-ttu-id="7b71b-541">但是，錯誤會排入佇列。</span><span class="sxs-lookup"><span data-stu-id="7b71b-541">Errors, however, are queued.</span></span> <span data-ttu-id="7b71b-542">使用 **Error** 物件與 **ErrorItem** 物件，從佇列中取出錯誤資訊。</span><span class="sxs-lookup"><span data-stu-id="7b71b-542">Use the **Error** object with the **ErrorItem** object to retrieve error information from the queue.</span></span> <span data-ttu-id="7b71b-543">請參閱上一節中的錯誤處理常式代碼範例。</span><span class="sxs-lookup"><span data-stu-id="7b71b-543">See the example code in the preceding section, Error handling.</span></span> |
| <span data-ttu-id="7b71b-544">*Player6*。**KeyDown**</span><span class="sxs-lookup"><span data-stu-id="7b71b-544">*Player6*.**KeyDown**</span></span>           | <span data-ttu-id="7b71b-545">使用 *Player*。**Keydown**</span><span class="sxs-lookup"><span data-stu-id="7b71b-545">Use *Player*.**Keydown**</span></span>                                                                                                                                                                                                 |
| <span data-ttu-id="7b71b-546">*Player6*。**按鍵**</span><span class="sxs-lookup"><span data-stu-id="7b71b-546">*Player6*.**KeyPress**</span></span>          | <span data-ttu-id="7b71b-547">使用 *Player*。**按鍵**</span><span class="sxs-lookup"><span data-stu-id="7b71b-547">Use *Player*.**KeyPress**</span></span>                                                                                                                                                                                                |
| <span data-ttu-id="7b71b-548">*Player6*。**KeyUp**</span><span class="sxs-lookup"><span data-stu-id="7b71b-548">*Player6*.**KeyUp**</span></span>             | <span data-ttu-id="7b71b-549">使用 *Player*。**KeyUp**</span><span class="sxs-lookup"><span data-stu-id="7b71b-549">Use *Player*.**KeyUp**</span></span>                                                                                                                                                                                                   |
| <span data-ttu-id="7b71b-550">*Player6*。**MarkerHit**</span><span class="sxs-lookup"><span data-stu-id="7b71b-550">*Player6*.**MarkerHit**</span></span>         | <span data-ttu-id="7b71b-551">使用 *Player*。**MarkerHit**。</span><span class="sxs-lookup"><span data-stu-id="7b71b-551">Use *Player*.**MarkerHit**.</span></span>                                                                                                                                                                                              |
| <span data-ttu-id="7b71b-552">*Player6*。**MouseDown**</span><span class="sxs-lookup"><span data-stu-id="7b71b-552">*Player6*.**MouseDown**</span></span>         | <span data-ttu-id="7b71b-553">使用 *Player*。**MouseDown**</span><span class="sxs-lookup"><span data-stu-id="7b71b-553">Use *Player*.**MouseDown**</span></span>                                                                                                                                                                                               |
| <span data-ttu-id="7b71b-554">*Player6*。**MouseMove**</span><span class="sxs-lookup"><span data-stu-id="7b71b-554">*Player6*.**MouseMove**</span></span>         | <span data-ttu-id="7b71b-555">使用 *Player*。**MouseMove**</span><span class="sxs-lookup"><span data-stu-id="7b71b-555">Use *Player*.**MouseMove**</span></span>                                                                                                                                                                                               |
| <span data-ttu-id="7b71b-556">*Player6*。**MouseUp**</span><span class="sxs-lookup"><span data-stu-id="7b71b-556">*Player6*.**MouseUp**</span></span>           | <span data-ttu-id="7b71b-557">使用 *Player*。**MouseUp**</span><span class="sxs-lookup"><span data-stu-id="7b71b-557">Use *Player*.**MouseUp**</span></span>                                                                                                                                                                                                 |
| <span data-ttu-id="7b71b-558">*Player6*。**NewStream**</span><span class="sxs-lookup"><span data-stu-id="7b71b-558">*Player6*.**NewStream**</span></span>         | <span data-ttu-id="7b71b-559">使用 *Player*。**OpenStateChange**</span><span class="sxs-lookup"><span data-stu-id="7b71b-559">Use *Player*.**OpenStateChange**</span></span>                                                                                                                                                                                         |
| <span data-ttu-id="7b71b-560">*Player6*。**OpenStateChange**</span><span class="sxs-lookup"><span data-stu-id="7b71b-560">*Player6*.**OpenStateChange**</span></span>   | <span data-ttu-id="7b71b-561">使用 *Player*。**OpenStateChange**。</span><span class="sxs-lookup"><span data-stu-id="7b71b-561">Use *Player*.**OpenStateChange**.</span></span>                                                                                                                                                                                        |
| <span data-ttu-id="7b71b-562">*Player6*。**PlayStateChange**</span><span class="sxs-lookup"><span data-stu-id="7b71b-562">*Player6*.**PlayStateChange**</span></span>   | <span data-ttu-id="7b71b-563">使用 *Player*。**PlayStateChange**。</span><span class="sxs-lookup"><span data-stu-id="7b71b-563">Use *Player*.**PlayStateChange**.</span></span>                                                                                                                                                                                        |
| <span data-ttu-id="7b71b-564">*Player6*。**PositionChange**</span><span class="sxs-lookup"><span data-stu-id="7b71b-564">*Player6*.**PositionChange**</span></span>    | <span data-ttu-id="7b71b-565">使用 *Player*。**PositionChange**。</span><span class="sxs-lookup"><span data-stu-id="7b71b-565">Use *Player*.**PositionChange**.</span></span>                                                                                                                                                                                         |
| <span data-ttu-id="7b71b-566">*Player6*。**ReadyStateChange**</span><span class="sxs-lookup"><span data-stu-id="7b71b-566">*Player6*.**ReadyStateChange**</span></span>  | <span data-ttu-id="7b71b-567">使用 *Player*。**PlayStateChange**。</span><span class="sxs-lookup"><span data-stu-id="7b71b-567">Use *Player*.**PlayStateChange**.</span></span>                                                                                                                                                                                        |
| <span data-ttu-id="7b71b-568">*Player6*。**ScriptCommand**</span><span class="sxs-lookup"><span data-stu-id="7b71b-568">*Player6*.**ScriptCommand**</span></span>     | <span data-ttu-id="7b71b-569">使用 *Player*。**ScriptCommand**。</span><span class="sxs-lookup"><span data-stu-id="7b71b-569">Use *Player*.**ScriptCommand**.</span></span>                                                                                                                                                                                          |
| <span data-ttu-id="7b71b-570">*Player6*。**警告**</span><span class="sxs-lookup"><span data-stu-id="7b71b-570">*Player6*.**Warning**</span></span>           | <span data-ttu-id="7b71b-571">不適用。</span><span class="sxs-lookup"><span data-stu-id="7b71b-571">Not available.</span></span>                                                                                                                                                                                                           |



 

## <a name="related-topics"></a><span data-ttu-id="7b71b-572">相關主題</span><span class="sxs-lookup"><span data-stu-id="7b71b-572">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7b71b-573">**物件模型遷移指南**</span><span class="sxs-lookup"><span data-stu-id="7b71b-573">**Object Model Migration Guide**</span></span>](object-model-migration-guide.md)
</dt> <dt>

[<span data-ttu-id="7b71b-574">**腳本的物件模型參考**</span><span class="sxs-lookup"><span data-stu-id="7b71b-574">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> </dl>

 

 





