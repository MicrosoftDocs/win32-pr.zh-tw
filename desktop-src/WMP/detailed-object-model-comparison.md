---
title: 詳細的物件模型比較
description: 詳細的物件模型比較
ms.assetid: 8f08e2a6-1944-4814-b3b7-680a3722e1a0
keywords:
- Windows Media Player，物件模型
- Windows Media Player 物件模型，版本差異
- 物件模型，版本差異
- Windows Media Player ActiveX 控制，版本差異
- ActiveX 控制項，版本差異
- Windows Media PlayerMobile ActiveX 控制項，版本差異
- Windows Media Player行動裝置，物件模型
- 遷移指南，版本差異
- Windows Media Player 的版本，物件模型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6f2e092f7e32b889056841b5802dffa141c0be4
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122884770"
---
# <a name="detailed-object-model-comparison"></a>詳細的物件模型比較

下表比較 Windows Media Player 6.4 物件模型屬性與 Windows Media Player 7 或更新版本的物件模型。



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Windows Media Player 6.4 屬性</th>
<th>Windows Media Player 7 或更新版本相等</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><em>Player6</em>。<strong>AllowChangeDisplaySize</strong></td>
<td>Windows Media Player 7 或更新版本的顯示會自動調整大小以符合媒體的大小。 您可以設定 &lt; 物件 &gt; 標記或腳本中的高度和寬度屬性。</td>
</tr>
<tr class="even">
<td><em>Player6</em>。<strong>AllowScan</strong></td>
<td><em>控制項</em>。 <strong>fastForward</strong> 和 <em>控制項</em>。支援這些方法的檔案類型會自動啟用<strong>fastReverse</strong> 。</td>
</tr>
<tr class="odd">
<td><em>Player6</em>。<strong>AnglesAvailable</strong></td>
<td>不適用。</td>
</tr>
<tr class="even">
<td><em>Player6</em>。<strong>AnimationAtStart</strong></td>
<td>不適用。</td>
</tr>
<tr class="odd">
<td><em>Player6</em>。<strong>AudioStream</strong></td>
<td>使用 <em>控制項</em>。<strong>currentAudioLanguageIndex</strong>。</td>
</tr>
<tr class="even">
<td><em>Player6</em>。<strong>AudioStreamsAvailable</strong></td>
<td>使用 <em>控制項</em>。<strong>audioLanguageCount</strong>。</td>
</tr>
<tr class="odd">
<td><em>Player6</em>。<strong>AutoRewind</strong></td>
<td>使用 <em>控制項</em>。在腳本中<strong>currentPosition</strong> ，以指定或取出目前的位置。 或者，使用標記和 <em>播放機</em>。<strong>markerHit</strong> 事件。</td>
</tr>
<tr class="even">
<td><em>Player6</em>。自動<strong>調整</strong></td>
<td>自動調整大小是預設行為。 若要覆寫自動調整大小，請在 &lt; 物件 &gt; 標記或腳本中設定 [高度] 和 [寬度] 屬性。</td>
</tr>
<tr class="odd">
<td><em>Player6</em>。<strong>自動啟動</strong></td>
<td>使用<em>設定</em>。<strong>自動啟動</strong>。</td>
</tr>
<tr class="even">
<td><em>Player6</em>。<strong>餘額</strong></td>
<td>使用<em>設定</em>。<strong>餘額</strong>。</td>
</tr>
<tr class="odd">
<td><em>Player6</em>。<strong>頻寬</strong></td>
<td>使用 <em>網路</em>。<strong>頻寬</strong>。</td>
</tr>
<tr class="even">
<td><em>Player6</em>。<strong>BaseURL</strong></td>
<td>使用<em>設定</em>。<strong>baseURL</strong>。</td>
</tr>
<tr class="odd">
<td><em>Player6</em>。<strong>BufferingCount</strong></td>
<td>使用 <em>網路。</em><strong>bufferingCount</strong>。</td>
</tr>
<tr class="even">
<td><em>Player6</em>。<strong>BufferingProgress</strong></td>
<td>使用 <em>網路</em>。<strong>bufferingProgress</strong>。</td>
</tr>
<tr class="odd">
<td><em>Player6</em>。<strong>BufferingTime</strong></td>
<td>使用 <em>網路</em>。<strong>bufferingTime</strong>。</td>
</tr>
<tr class="even">
<td><em>Player6</em>。<strong>ButtonsAvailable</strong></td>
<td>不適用。</td>
</tr>
<tr class="odd">
<td><em>Player6</em>。<strong>CanPreview</strong></td>
<td>不適用。</td>
</tr>
<tr class="even">
<td><em>Player6</em>。<strong>CanScan</strong></td>
<td>使用 <em>控制項</em>。<strong>isAvailable</strong> (&quot; FastForward &quot;) 和 <em>控制項</em>。<strong>isAvailable</strong> (&quot; FastReverse &quot;) 。</td>
</tr>
<tr class="odd">
<td><em>Player6</em>。<strong>CanSeek</strong></td>
<td>使用 <em>控制項</em>。<strong>isAvailable</strong> ，測試是否可以執行特定的 seek 方法。</td>
</tr>
<tr class="even">
<td><em>Player6</em>。<strong>CanSeekToMarkers</strong></td>
<td>使用 <em>控制項</em>。<strong>isAvailable</strong> (&quot; CurrentMarker &quot;) 。 使用 <em>媒體</em>。<strong>markerCount</strong> ，以取得特定媒體專案中的標記計數。 使用 <em>控制項</em>。<strong>currentMarker</strong> 指定或取出目前的標記編號。</td>
</tr>
<tr class="odd">
<td><em>Player6</em>。<strong>CaptioningID</strong></td>
<td>使用 <em>ClosedCaption</em>。<strong>captioningID</strong>。</td>
</tr>
<tr class="even">
<td><em>Player6</em>。<strong>CCActive</strong></td>
<td>不適用。 如需如何在 Windows Media Player 中變更隱藏式字幕的詳細資訊，請參閱<a href="closed-captioning.md">隱藏式字幕</a>。</td>
</tr>
<tr class="odd">
<td><em>Player6</em>。<strong>ChannelDescription</strong></td>
<td>不適用。</td>
</tr>
<tr class="even">
<td><em>Player6</em>。<strong>ChannelName</strong></td>
<td>不適用。</td>
</tr>
<tr class="odd">
<td><em>Player6</em>。<strong>ChannelURL</strong></td>
<td>不適用。</td>
</tr>
<tr class="even">
<td><em>Player6</em>。<strong>ClickToPlay</strong></td>
<td>不適用。 您應該在使用者介面中提供控制項以開始播放。 或者，使用者可以用滑鼠右鍵按一下影片影像來開啟快顯功能表，其中包含<em>播放機</em>的<strong>播放/暫停</strong>選擇。<strong>enableCoNtextMenu</strong>等於 true。</td>
</tr>
<tr class="odd">
<td><em>Player6</em>。<strong>ClientID</strong></td>
<td>無法使用。Windows Media Player 9 系列或更新版本可讓使用者選取是否要將唯一的播放程式識別碼傳送給內容提供者。<br/> 如果使用者選取這個選項，播放者會將唯一的識別碼傳送至 Windows 媒體伺服器。 識別碼會記錄在伺服器的記錄檔中，位於中。預設為<em>system32\logfiles</em> 資料夾。 記錄功能變數名稱為 &quot; c-playerid &quot; 。 在 Windows Media Services 中，預設不會啟用伺服器記錄。<br/> 如果使用者未選取此選項，伺服器會產生隨機會話識別碼，這對指定會話的每個用戶端而言是唯一的。<br/> 如需詳細資訊，請參閱 Windows Media Services 9 系列檔。<br/></td>
</tr>
<tr class="even">
<td><em>Player6</em>。<strong>CodecCount</strong></td>
<td>不適用。</td>
</tr>
<tr class="odd">
<td><em>Player6</em>。<strong>>Colorkey</strong></td>
<td>不適用。</td>
</tr>
<tr class="even">
<td><em>Player6</em>。<strong>ConnectionSpeed</strong></td>
<td>不適用。 使用 <em>網路</em>。<strong>位元速率</strong> 判斷目前的位元速率。</td>
</tr>
<tr class="odd">
<td><em>Player6</em>。<strong>ContactAddress</strong></td>
<td>不適用。</td>
</tr>
<tr class="even">
<td><em>Player6</em>。<strong>ContactEmail</strong></td>
<td>不適用。</td>
</tr>
<tr class="odd">
<td><em>Player6</em>。<strong>ContactPhone</strong></td>
<td>不適用。</td>
</tr>
<tr class="even">
<td><em>Player6</em>。<strong>CreationDate</strong></td>
<td>使用 <em>MediaCollection</em>。<strong>getMediaAtom</strong> (&quot; CreationDate &quot;) 取得建立日期 atom 的索引。 使用 <em>媒體</em>。<strong>getItemInfoByAtom</strong> 以取得中繼資料。</td>
</tr>
<tr class="odd">
<td><em>Player6</em>。<strong>CurrentAngle</strong></td>
<td>不適用。</td>
</tr>
<tr class="even">
<td><em>Player6</em>。<strong>CurrentAudioStream</strong></td>
<td>使用 <em>控制項</em>。<strong>currentAudioLanguageIndex</strong>。</td>
</tr>
<tr class="odd">
<td><em>Player6</em>。<strong>CurrentButton</strong></td>
<td>不適用。</td>
</tr>
<tr class="even">
<td><em>Player6</em>。<strong>CurrentCCService</strong></td>
<td>不適用。</td>
</tr>
<tr class="odd">
<td><em>Player6</em>。<strong>CurrentChapter</strong></td>
<td>取出目前的播放清單。 如果目前的播放清單與 <em>Cdrom</em>所傳回的播放清單不同。<strong>播放清單</strong>，則沒有最新的章節。 否則，目前的章節編號是目前播放清單中目前媒體的索引。</td>
</tr>
<tr class="even">
<td><em>Player6</em>。<strong>CurrentDiscSide</strong></td>
<td>不適用。</td>
</tr>
<tr class="odd">
<td><em>Player6</em>。<strong>CurrentDomain</strong></td>
<td>使用 <em>DVD</em>。<strong>網域</strong>。</td>
</tr>
<tr class="even">
<td><em>Player6</em>。<strong>CurrentMarker</strong></td>
<td>使用 <em>控制項</em>。<strong>currentMarker</strong>。</td>
</tr>
<tr class="odd">
<td><em>Player6</em>。<strong>CurrentPosition</strong></td>
<td>使用 <em>控制項</em>。<strong>currentPosition</strong>。</td>
</tr>
<tr class="even">
<td><em>Player6</em>。<strong>CurrentSubpictureStream</strong></td>
<td>不適用。</td>
</tr>
<tr class="odd">
<td><em>Player6</em>。<strong>CurrentTime</strong></td>
<td>使用 <em>控制項</em>。<strong>currentPositionTimeCode</strong>、 <em>控制項</em>。<strong>currentPositionString</strong>或 <em>控制項</em>。<strong>currentPosition。</strong></td>
</tr>
<tr class="even">
<td><em>Player6</em>。<strong>CurrentTitle</strong></td>
<td>取出目前的播放清單。 如果目前的播放清單與 <em>Cdrom</em>所傳回的播放清單相同。<strong>播放清單</strong>之後，標題號碼即為目前媒體在目前播放清單中的索引。</td>
</tr>
<tr class="odd">
<td><em>Player6</em>。<strong>CurrentVolume</strong></td>
<td>不適用。</td>
</tr>
<tr class="even">
<td><em>Player6</em>。<strong>CursorType</strong></td>
<td>不適用。 請改用 Internet Explorer 的樣式。</td>
</tr>
<tr class="odd">
<td><em>Player6</em>。<strong>DefaultFrame</strong></td>
<td>使用<em>設定</em>。<strong>defaultFrame</strong>，或使用 <PARAM> OBJECT 元素中的屬性 &lt; &gt; ：
<pre data-space="preserve"><code><PARAM NAME=&quot;defaultFrame&quot; VALUE=&quot;right&quot;></code></pre></td>
</tr>
<tr class="even">
<td><em>Player6</em>。<strong>DisplayBackColor</strong></td>
<td>不適用。</td>
</tr>
<tr class="odd">
<td><em>Player6</em>。<strong>DisplayForeColor</strong></td>
<td>不適用。</td>
</tr>
<tr class="even">
<td><em>Player6</em>。<strong>>Displaymode</strong></td>
<td>您可以使用<em>控制項</em><strong>以秒</strong>為單位，從開頭開始抓取目前的位置。<strong>currentPosition</strong>，格式為 HH： MM： SS (時、分、秒) 使用<em>控制項</em>的<strong>字串</strong>。使用<em>控制項</em>的<strong>currentPositionString</strong>或時間碼格式。<strong>currentPositionTimeCode</strong>。</td>
</tr>
<tr class="odd">
<td><em>Player6</em>。<strong>DisplaySize</strong></td>
<td>預設顯示會自動調整大小以符合媒體。 您可以設定 &lt; 物件 &gt; 標記或腳本中的高度和寬度屬性。 使用 <em>Player</em>。<strong>全</strong> 螢幕切換至全螢幕模式。</td>
</tr>
<tr class="even">
<td><em>Player6</em>。<strong>持續時間</strong></td>
<td>使用 <em>媒體</em>。<strong>持續時間</strong>。</td>
</tr>
<tr class="odd">
<td><em>Player6</em>。<strong>DVD</strong></td>
<td>使用 <em>Player</em>。<strong>DVD</strong>。</td>
</tr>
<tr class="even">
<td><em>Player6</em>。<strong>EnableCoNtextMenu</strong></td>
<td>使用 <em>Player</em>。<strong>enableCoNtextMenu</strong>。</td>
</tr>
<tr class="odd">
<td><em>Player6</em>。<strong>已啟用</strong></td>
<td>使用 <em>Player</em>。<strong>已啟用</strong>。</td>
</tr>
<tr class="even">
<td><em>Player6</em>。<strong>EnableFullScreenControls</strong></td>
<td>使用 Windows Media Player 9 系列或更新版本時，會自動啟用全螢幕控制項，除非<em>播放玩家</em>。<strong></strong>  =  uiMode &quot;無 &quot; 。</td>
</tr>
<tr class="odd">
<td><em>Player6</em>。<strong>EnablePositionControls</strong></td>
<td>不適用。 您可以提供自訂控制項或使用 <em>播放</em>。<strong>uimode</strong> 選擇預設設定。</td>
</tr>
<tr class="even">
<td><em>Player6</em>。<strong>EnableTracker</strong></td>
<td>不適用。 您可以提供自訂控制項或使用 <em>播放</em>。<strong>uimode</strong> 選擇預設設定。</td>
</tr>
<tr class="odd">
<td><em>Player6</em>。<strong>EntryCount</strong></td>
<td>使用 <em>播放清單</em>。<strong>計數</strong></td>
</tr>
<tr class="even">
<td><em>Player6</em>。<strong>ErrorCode</strong></td>
<td>使用 <em>ErrorItem</em>。<strong>errorCode</strong>。</td>
</tr>
<tr class="odd">
<td><em>Player6</em>。<strong>ErrorCorrection</strong></td>
<td>不適用。</td>
</tr>
<tr class="even">
<td><em>Player6</em>。<strong>ErrorDescription</strong></td>
<td>使用 <em>ErrorItem</em>。<strong>errorDescription</strong>。</td>
</tr>
<tr class="odd">
<td><em>Player6</em>。<strong>檔案名</strong></td>
<td>使用 <em>Player</em>。<strong>URL</strong> 或 <em>播放機</em>。<strong>currentMedia</strong>。 使用 <em>控制項</em>。在播放清單中工作時<strong>currentItem</strong> 。</td>
</tr>
<tr class="even">
<td><em>Player6</em>。<strong>FramesPerSecond</strong></td>
<td>不適用。</td>
</tr>
<tr class="odd">
<td><em>Player6</em>。<strong>HasError</strong></td>
<td>使用 <em>錯誤</em>。<strong>errorCount</strong>。</td>
</tr>
<tr class="even">
<td><em>Player6</em>。<strong>HasMultipleItems</strong></td>
<td>不適用。</td>
</tr>
<tr class="odd">
<td><em>Player6</em>。<strong>ImageSourceHeight</strong></td>
<td>使用 <em>媒體</em>。<strong>imageSourceHeight</strong>。</td>
</tr>
<tr class="even">
<td><em>Player6</em>。<strong>ImageSourceWidth</strong></td>
<td>使用 <em>媒體</em>。<strong>imageSourceWidth</strong>。</td>
</tr>
<tr class="odd">
<td><em>Player6</em>。<strong>InvokeURLs</strong></td>
<td>使用<em>設定</em>。<strong>invokeURLs</strong>。</td>
</tr>
<tr class="even">
<td><em>Player6</em>。<strong>IsBroadcast</strong></td>
<td>使用 <em>網路</em>。<strong>sourceProtocol</strong>。</td>
</tr>
<tr class="odd">
<td><em>Player6</em>。<strong>IsDurationValid</strong></td>
<td>不適用。 <em>媒體</em>。使用目前的媒體物件時，<strong>持續時間</strong> 包含有效的值。</td>
</tr>
<tr class="even">
<td><em>Player6</em>。<strong>語言</strong></td>
<td>使用 <em>控制項</em>。<strong>currentAudioLanguage</strong></td>
</tr>
<tr class="odd">
<td><em>Player6</em>。<strong>LostPackets</strong></td>
<td>使用 <em>網路</em>。<strong>lostPackets</strong>。</td>
</tr>
<tr class="even">
<td><em>Player6</em>。<strong>MarkerCount</strong></td>
<td>使用 <em>媒體</em>。<strong>markerCount</strong>。</td>
</tr>
<tr class="odd">
<td><em>Player6</em>。<strong>靜音</strong></td>
<td>使用<em>設定</em>。<strong>靜音</strong>。</td>
</tr>
<tr class="even">
<td><em>Player6</em>。<strong>OpenState</strong></td>
<td>使用 <em>Player</em>。<strong>openState</strong>。</td>
</tr>
<tr class="odd">
<td><em>Player6</em>。<strong>PlayCount</strong></td>
<td>使用<em>設定</em>。<strong>playCount</strong>。</td>
</tr>
<tr class="even">
<td><em>Player6</em>。<strong>PlayState</strong></td>
<td>使用 <em>Player</em>。<strong>playState</strong>。</td>
</tr>
<tr class="odd">
<td><em>Player6</em>。<strong>PreviewMode</strong></td>
<td>不適用。 使用具有 HTML 計時器的腳本迴圈結構來複製此功能。</td>
</tr>
<tr class="even">
<td><em>Player6</em>。<strong>費率</strong></td>
<td>使用<em>設定</em>。<strong>費率</strong>。</td>
</tr>
<tr class="odd">
<td><em>Player6</em>。<strong>ReadyState</strong></td>
<td>使用 <em>Player</em>。<strong>openState</strong>。</td>
</tr>
<tr class="even">
<td><em>Player6</em>。<strong>ReceivedPackets</strong></td>
<td>使用 <em>網路</em>。<strong>receivedPackets</strong>。</td>
</tr>
<tr class="odd">
<td><em>Player6</em>。<strong>ReceptionQuality</strong></td>
<td>使用 <em>網路</em>。<strong>receptionQuality</strong>。</td>
</tr>
<tr class="even">
<td><em>Player6</em>。<strong>RecoveredPackets</strong></td>
<td>使用 <em>網路</em>。<strong>recoveredPackets</strong>。</td>
</tr>
<tr class="odd">
<td><em>Player6</em>。<strong>根目錄</strong></td>
<td>不適用。</td>
</tr>
<tr class="even">
<td><em>Player6</em>。<strong>SAMIFileName</strong></td>
<td>使用 <em>ClosedCaption</em>。<strong>SAMIFileName</strong>。</td>
</tr>
<tr class="odd">
<td><em>Player6</em>。<strong>SAMILang</strong></td>
<td>使用 <em>ClosedCaption</em>。<strong>SAMILang</strong>。</td>
</tr>
<tr class="even">
<td><em>Player6</em>。<strong>SAMIStyle</strong></td>
<td>使用 <em>ClosedCaption</em>。<strong>SAMIStyle</strong>。</td>
</tr>
<tr class="odd">
<td><em>Player6</em>。<strong>SelectionEnd</strong></td>
<td>使用<em>媒體</em>。決定<strong>媒體</strong>物件長度的<strong>持續時間</strong>。 使用具有 <em>控制項</em>的標記。<strong>currentMarker</strong> 指定自訂結束位置。</td>
</tr>
<tr class="even">
<td><em>Player6</em>。<strong>SelectionStart</strong></td>
<td>使用 <em>控制項</em>。<strong>currentPosition</strong> 從特定位置開始播放，或使用具有 <em>控制項</em>的標記。<strong>currentMarker</strong> 指定自訂開始位置。</td>
</tr>
<tr class="odd">
<td><em>Player6</em>。<strong>SendErrorEvents</strong></td>
<td>錯誤已排入佇列。 使用 <strong>error</strong> 物件和 <strong>ErrorItem</strong> 物件來取得錯誤資訊。</td>
</tr>
<tr class="even">
<td><em>Player6</em>。<strong>SendKeyboardEvents</strong></td>
<td>不適用。</td>
</tr>
<tr class="odd">
<td><em>Player6</em>。<strong>SendMouseClickEvents</strong></td>
<td>不適用。</td>
</tr>
<tr class="even">
<td><em>Player6</em>。<strong>SendMouseMoveEvents</strong></td>
<td>不適用。</td>
</tr>
<tr class="odd">
<td><em>Player6</em>。<strong>SendOpenStateChangeEvents</strong></td>
<td>不適用。</td>
</tr>
<tr class="even">
<td><em>Player6</em>。<strong>SendPlayStateChangeEvents</strong></td>
<td>不適用。</td>
</tr>
<tr class="odd">
<td><em>Player6</em>。<strong>SendWarningEvents</strong></td>
<td>不適用。</td>
</tr>
<tr class="even">
<td><em>Player6</em>。<strong>ShowAudioControls</strong></td>
<td>不適用。 您可以提供自訂控制項或使用 <em>播放</em>。<strong>uimode</strong> 選擇預設設定。</td>
</tr>
<tr class="odd">
<td><em>Player6</em>。<strong>ShowCaptioning</strong></td>
<td>不適用。 您可以提供自訂的隱藏式輔助字幕顯示。</td>
</tr>
<tr class="even">
<td><em>Player6</em>。<strong>ShowControls</strong></td>
<td>不適用。 您可以提供自訂控制項或使用 <em>播放</em>。<strong>uimode</strong> 選擇預設設定。</td>
</tr>
<tr class="odd">
<td><em>Player6</em>。<strong>ShowDisplay</strong></td>
<td>不適用。</td>
</tr>
<tr class="even">
<td><em>Player6</em>。<strong>ShowGotoBar</strong></td>
<td>不適用。 您可以使用媒體物件提供自訂功能</td>
</tr>
<tr class="odd">
<td><em>Player6</em>。<strong>ShowPositionControls</strong></td>
<td>不適用。 您可以提供自訂控制項或使用 <em>播放</em>。<strong>uimode</strong> 選擇預設設定。</td>
</tr>
<tr class="even">
<td><em>Player6</em>。<strong>ShowStatusBar</strong></td>
<td>不適用。 您可以提供自訂控制項或使用 <em>播放</em>。<strong>uimode</strong> 選擇預設設定。</td>
</tr>
<tr class="odd">
<td><em>Player6</em>。<strong>ShowTracker</strong></td>
<td>不適用。 您可以提供自訂控制項或使用 <em>播放</em>。<strong>uimode</strong> 選擇預設設定。</td>
</tr>
<tr class="even">
<td><em>Player6</em>。<strong>SourceLink</strong></td>
<td>使用 <em>媒體</em>。<strong>sourceURL</strong>。</td>
</tr>
<tr class="odd">
<td><em>Player6</em>。<strong>SourceProtocol</strong></td>
<td>使用 <em>網路</em>。<strong>sourceProtocol</strong>。</td>
</tr>
<tr class="even">
<td><em>Player6</em>。<strong>StreamCount</strong></td>
<td>不適用。 使用 <em>控制項</em>。<strong>audioLanguageCount</strong> 可取出音訊語言資料流程的數目。</td>
</tr>
<tr class="odd">
<td><em>Player6</em>。<strong>SubpictureOn</strong></td>
<td>不適用。</td>
</tr>
<tr class="even">
<td><em>Player6</em>。<strong>SubpictureStreamsAvailable</strong></td>
<td>無法使用</td>
</tr>
<tr class="odd">
<td><em>Player6</em>。<strong>TitlesAvailable</strong></td>
<td>使用下列各項：<code>Player.Cdrom.playlist.count - 1</code><br/></td>
</tr>
<tr class="even">
<td><em>Player6</em>。<strong>TotalTitleTime</strong></td>
<td>使用 <em>currentMedia</em>。<strong>duration</strong> 或 <em>currentMedia</em>。<strong>durationString</strong>。</td>
</tr>
<tr class="odd">
<td><em>Player6</em>。<strong>TransparentAtStart</strong></td>
<td>使用腳本來指定高度和寬度值，讓播放玩家可見或隱藏。</td>
</tr>
<tr class="even">
<td><em>Player6</em>。<strong>UniqueID</strong></td>
<td>不適用。</td>
</tr>
<tr class="odd">
<td><em>Player6</em>。<strong>VideoBorder3D</strong></td>
<td>不適用。</td>
</tr>
<tr class="even">
<td><em>Player6</em>。<strong>VideoBorderColor</strong></td>
<td>不適用。</td>
</tr>
<tr class="odd">
<td><em>Player6</em>。<strong>VideoBorderWidth</strong></td>
<td>不適用。</td>
</tr>
<tr class="even">
<td><em>Player6</em>。<strong>磁片</strong>區</td>
<td>使用<em>設定</em>。<strong>磁片</strong>區。</td>
</tr>
<tr class="odd">
<td><em>Player6</em>。<strong>VolumesAvailable</strong></td>
<td>不適用。</td>
</tr>
</tbody>
</table>



 

下表比較 Windows Media Player 6.4 版物件模型方法與 Windows Media Player 7 或更新版本的物件模型。



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Windows Media Player 6.4 方法</th>
<th>Windows Media Player 7 或更新版本相等</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><em>Player6</em>。<strong>AboutBox</strong></td>
<td>使用<em>Player</em>。<strong>versionInfo</strong> ，以取得 Windows Media Player 的版本。</td>
</tr>
<tr class="even">
<td><em>Player6</em>。<strong>BackwardScan</strong></td>
<td>使用<em>設定</em>。<strong>費率</strong>。</td>
</tr>
<tr class="odd">
<td><em>Player6</em>。<strong>ButtonActivate</strong></td>
<td>不適用。</td>
</tr>
<tr class="even">
<td><em>Player6</em>。<strong>ButtonSelectAndActivate</strong></td>
<td>不適用。</td>
</tr>
<tr class="odd">
<td><em>Player6</em>。<strong>取消</strong></td>
<td>不適用。</td>
</tr>
<tr class="even">
<td><em>Player6</em>。<strong>ChapterPlay</strong></td>
<td>如果已經在播放指定的標題播放清單，請使用下列語法，以媒體物件的形式取出所需的章節：
<pre data-space="preserve"><code>var media = Player.currentPlaylist.item(index);</code></pre>
然後指定 [ <em>Player</em>]。<strong>currentMedia</strong> 使用傳回的媒體物件。<br/></td>
</tr>
<tr class="odd">
<td><em>Player6</em>。<strong>ChapterPlayAutoStop</strong></td>
<td>不適用。</td>
</tr>
<tr class="even">
<td><em>Player6</em>。<strong>ChapterSearch</strong></td>
<td>如果已經在播放指定的標題播放清單，請使用下列語法，以媒體物件的形式取出所需的章節：
<pre data-space="preserve"><code>var media = Player.currentPlaylist.item(index);</code></pre>
然後指定 [ <em>Player</em>]。<strong>currentMedia</strong> 使用傳回的媒體物件。<br/></td>
</tr>
<tr class="odd">
<td><em>Player6</em>。<strong>FastForward</strong></td>
<td>使用 <em>控制項</em>。<strong>fastForward</strong>。</td>
</tr>
<tr class="even">
<td><em>Player6</em>。<strong>FastReverse</strong></td>
<td>使用 <em>控制項</em>。<strong>fastReverse</strong>。</td>
</tr>
<tr class="odd">
<td><em>Player6</em>。<strong>ForwardScan</strong></td>
<td>使用<em>設定</em>。<strong>費率</strong>。</td>
</tr>
<tr class="even">
<td><em>Player6</em>。<strong>GetAllGPRMs</strong></td>
<td>不適用。</td>
</tr>
<tr class="odd">
<td><em>Player6</em>。<strong>GetAllSPRMs</strong></td>
<td>不適用。</td>
</tr>
<tr class="even">
<td><em>Player6</em>。<strong>GetAudioLanguage</strong></td>
<td>使用 <em>控制項</em>。<strong>currentAudioLanguage</strong> ，以取得目前音訊語言的 LCID。</td>
</tr>
<tr class="odd">
<td><em>Player6</em>。<strong>GetCodecDescription</strong></td>
<td>不適用。</td>
</tr>
<tr class="even">
<td><em>Player6</em>。<strong>GetCodecInstalled</strong></td>
<td>不適用。</td>
</tr>
<tr class="odd">
<td><em>Player6</em>。<strong>GetCodecURL</strong></td>
<td>使用 <em>ErrorItem</em>。<strong>customUrl</strong>。</td>
</tr>
<tr class="even">
<td><em>Player6</em>。<strong>GetCurrentEntry</strong></td>
<td>使用腳本對目前的播放清單執行迴圈。 使用 <em>媒體</em>。<strong>isIdentical</strong> ，將播放清單中的每個專案與 <em>播放</em>清單進行比較。<strong>currentMedia</strong> 物件。</td>
</tr>
<tr class="odd">
<td><em>Player6</em>。<strong>GetMarkerName</strong></td>
<td>使用 <em>媒體</em>。<strong>getMarkerName</strong>。</td>
</tr>
<tr class="even">
<td><em>Player6</em>。<strong>GetMarkerTime</strong></td>
<td>使用 <em>媒體</em>。<strong>getMarkerTime</strong>。</td>
</tr>
<tr class="odd">
<td><em>Player6</em>。<strong>GetMediaInfoString</strong></td>
<td>使用 <em>媒體</em>。<strong>getItemInfo</strong>、 <em>Media</em>。<strong>getItemInfoByAtom</strong>及其相關聯的方法，以取得中繼資料。</td>
</tr>
<tr class="even">
<td><em>Player6</em>。<strong>GetMediaParameter</strong></td>
<td>使用 <em>播放清單</em>。取得媒體專案的<strong>專案</strong> 。 然後使用 <em>媒體</em>。<strong>getItemInfo</strong> 以取得參數字串。</td>
</tr>
<tr class="odd">
<td><em>Player6</em>。<strong>GetMediaParameterName</strong></td>
<td>使用 <em>播放清單</em>。取得媒體專案的<strong>專案</strong> 。 然後使用 <em>媒體</em>。<strong>getAttributeName</strong> 以取得參數字串。</td>
</tr>
<tr class="even">
<td><em>Player6</em>。<strong>GetMoreInfoURL</strong></td>
<td>不適用。</td>
</tr>
<tr class="odd">
<td><em>Player6</em>。<strong>GetNumberOfChapters</strong></td>
<td>如果目前現正播放標題，請使用 <em>currentPlaylist</em>。<strong>計數</strong>。</td>
</tr>
<tr class="even">
<td><em>Player6</em>。<strong>GetStreamGroup</strong></td>
<td>不適用。</td>
</tr>
<tr class="odd">
<td><em>Player6</em>。<strong>GetStreamName</strong></td>
<td>不適用。</td>
</tr>
<tr class="even">
<td><em>Player6</em>。<strong>GetStreamSelected</strong></td>
<td>不適用。</td>
</tr>
<tr class="odd">
<td><em>Player6</em>。<strong>GetSubpictureLanguage</strong></td>
<td>不適用。</td>
</tr>
<tr class="even">
<td><em>Player6</em>。<strong>群組</strong></td>
<td>使用 <em>DVD</em>。<strong>回來</strong>。</td>
</tr>
<tr class="odd">
<td><em>Player6</em>。<strong>IsSoundCardEnabled</strong></td>
<td>不適用。</td>
</tr>
<tr class="even">
<td><em>Player6</em>。<strong>LeftButtonSelect</strong></td>
<td>不適用。</td>
</tr>
<tr class="odd">
<td><em>Player6</em>。<strong>LowerButtonSelect</strong></td>
<td>不適用。</td>
</tr>
<tr class="even">
<td><em>Player6</em>。<strong>MenuCall</strong></td>
<td>使用 <em>DVD</em>。<strong>titleMenu</strong> 或 <em>DVD</em>。<strong>topMenu</strong>。</td>
</tr>
<tr class="odd">
<td><em>Player6</em>。<strong>下一步</strong></td>
<td>使用 <em>控制項</em>。<strong>接下來</strong>。</td>
</tr>
<tr class="even">
<td><em>Player6</em>。<strong>NextPGSearch</strong></td>
<td>使用 <em>控制項</em>。<strong>接下來</strong>。</td>
</tr>
<tr class="odd">
<td><em>Player6</em>。<strong>開啟</strong></td>
<td>使用 <em>Player</em>。<strong>URL</strong> 或 <em>播放機</em>。<strong>currentMedia</strong>。 檔案一律會以非同步方式開啟。</td>
</tr>
<tr class="even">
<td><em>Player6</em>。<strong>暫停</strong></td>
<td>使用 <em>控制項</em>。<strong>暫停</strong>。</td>
</tr>
<tr class="odd">
<td><em>Player6</em>。<strong>播放</strong></td>
<td>使用 <em>控制項</em>。<strong>玩</strong>。</td>
</tr>
<tr class="even">
<td><em>Player6</em>。<strong>上一個</strong></td>
<td>使用 <em>控制項</em>。<strong>上一步</strong>。</td>
</tr>
<tr class="odd">
<td><em>Player6</em>。<strong>PrevPGSearch</strong></td>
<td>使用 <em>控制項</em>。<strong>上一步</strong>。</td>
</tr>
<tr class="even">
<td><em>Player6</em>。<strong>ResumeFromMenu</strong></td>
<td>使用 <em>DVD</em>。<strong>繼續</strong>。</td>
</tr>
<tr class="odd">
<td><em>Player6</em>。<strong>RightButtonSelect</strong></td>
<td>不適用。</td>
</tr>
<tr class="even">
<td><em>Player6</em>。<strong>SetCurrentEntry</strong></td>
<td>使用<em>currentPlaylist</em>取出媒體物件。 (<em>entryNumber</em>) 的<strong>專案</strong>。 然後，使用 <em>控制項</em>來指定抓取的媒體物件。<strong>currentItem</strong>。</td>
</tr>
<tr class="odd">
<td><em>Player6</em>。<strong>ShowDialog</strong></td>
<td>不適用。</td>
</tr>
<tr class="even">
<td><em>Player6</em>。<strong>StillOff</strong></td>
<td>使用 <em>控制項</em>。<strong>玩</strong>。 或者，使用 <em>控制項</em>。<strong>接下來</strong> ，如果目前處於仍處於模式中。</td>
</tr>
<tr class="odd">
<td><em>Player6</em>。<strong>停止</strong></td>
<td>使用 <em>控制項</em>。<strong>停止</strong>。</td>
</tr>
<tr class="even">
<td><em>Player6</em>。<strong>StreamSelect</strong></td>
<td>不適用。 使用 <em>控制項</em>。<strong>currentAudioLanguage</strong> 指定音訊語言資料流程。</td>
</tr>
<tr class="odd">
<td><em>Player6</em>。<strong>TimePlay</strong></td>
<td>從根播放清單中，使用<em>currentPlaylist</em>。取得媒體物件的 (<em>索引</em>) <strong>專案</strong>。 然後，使用 <em>控制項</em>將媒體物件設定為目前的物件。<strong>currentItem</strong>。 然後，指定 <em>控制項</em>。<strong>currentPosition</strong> 使用時間值（以秒為單位）。</td>
</tr>
<tr class="even">
<td><em>Player6</em>。<strong>TimeSearch</strong></td>
<td>使用 <em>控制項</em>。<strong>currentPosition</strong>。</td>
</tr>
<tr class="odd">
<td><em>Player6</em>。<strong>TitlePlay</strong></td>
<td>如果已經在播放指定的標題播放清單，請使用下列語法，以媒體物件的形式取出所需的章節：
<pre data-space="preserve"><code>var media = Player.currentPlaylist.item(index);</code></pre>
然後指定 [ <em>Player</em>]。<strong>currentMedia</strong> 使用傳回的媒體物件。<br/> 或者，使用 <em>currentPlaylist</em>。取得媒體物件的<strong>專案</strong> ，然後使用傳回的媒體物件來指定 <em>控制項</em>。<strong>currentItem</strong>。<br/></td>
</tr>
<tr class="even">
<td><em>Player6</em>。<strong>TopPGSearch</strong></td>
<td>不適用。</td>
</tr>
<tr class="odd">
<td><em>Player6</em>。<strong>UOPValid</strong></td>
<td>無法使用</td>
</tr>
<tr class="even">
<td><em>Player6</em>。<strong>UpperButtonSelect</strong></td>
<td>不適用。</td>
</tr>
</tbody>
</table>



 

下表比較 Windows Media Player 6.4 版物件模型事件與 Windows Media Player 7 或更新版本的物件模型。



| Windows Media Player 6.4 事件  | Windows Media Player 7 或更新版本相等                                                                                                                                                                               |
|---------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Player6*。**緩衝**         | 使用 *Player*。**緩衝** 處理。                                                                                                                                                                                              |
| *Player6*。**按一下**             | 使用 *Player*。**按一下**                                                                                                                                                                                                   |
| *Player6*。**DblClick**          | 使用 *Player*。**DoubleClick**                                                                                                                                                                                             |
| *Player6*。**中斷** 連線        | 不適用。                                                                                                                                                                                                           |
| *Player6*。**DisplayModeChange** | 不適用。                                                                                                                                                                                                           |
| *Player6*。**DVDNotify**         | *玩家*。**DomainChange** 和 *Player*。**OpenPlaylistSwitch** 是 DVD 特定的事件。 與播放清單、媒體和 CD-ROM 媒體相關的其他事件，也可能會根據應用程式而套用。                        |
| *Player6*。**EndOfStream**       | 使用 *Player*。**PlayState**。                                                                                                                                                                                              |
| *Player6*。**錯誤**             | 事件未變更。 但是，錯誤會排入佇列。 使用 **Error** 物件與 **ErrorItem** 物件，從佇列中取出錯誤資訊。 請參閱上一節中的錯誤處理常式代碼範例。 |
| *Player6*。**KeyDown**           | 使用 *Player*。**Keydown**                                                                                                                                                                                                 |
| *Player6*。**按鍵**          | 使用 *Player*。**按鍵**                                                                                                                                                                                                |
| *Player6*。**KeyUp**             | 使用 *Player*。**KeyUp**                                                                                                                                                                                                   |
| *Player6*。**MarkerHit**         | 使用 *Player*。**MarkerHit**。                                                                                                                                                                                              |
| *Player6*。**MouseDown**         | 使用 *Player*。**MouseDown**                                                                                                                                                                                               |
| *Player6*。**MouseMove**         | 使用 *Player*。**MouseMove**                                                                                                                                                                                               |
| *Player6*。**MouseUp**           | 使用 *Player*。**MouseUp**                                                                                                                                                                                                 |
| *Player6*。**NewStream**         | 使用 *Player*。**OpenStateChange**                                                                                                                                                                                         |
| *Player6*。**OpenStateChange**   | 使用 *Player*。**OpenStateChange**。                                                                                                                                                                                        |
| *Player6*。**PlayStateChange**   | 使用 *Player*。**PlayStateChange**。                                                                                                                                                                                        |
| *Player6*。**PositionChange**    | 使用 *Player*。**PositionChange**。                                                                                                                                                                                         |
| *Player6*。**ReadyStateChange**  | 使用 *Player*。**PlayStateChange**。                                                                                                                                                                                        |
| *Player6*。**ScriptCommand**     | 使用 *Player*。**ScriptCommand**。                                                                                                                                                                                          |
| *Player6*。**警告**           | 不適用。                                                                                                                                                                                                           |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**物件模型遷移指南**](object-model-migration-guide.md)
</dt> <dt>

[**腳本的物件模型參考**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 





