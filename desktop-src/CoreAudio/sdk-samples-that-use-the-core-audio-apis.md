---
description: 使用核心音訊 Api 的 SDK 範例
ms.assetid: 4460df28-a77d-4bf5-9dee-5fb69ba2ded6
title: 使用核心音訊 Api 的 SDK 範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15eb05da5fefc22eaa0987d9996f0ddb48702158
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936334"
---
# <a name="sdk-samples-that-use-the-core-audio-apis"></a>使用核心音訊 Api 的 SDK 範例

Windows SDK 包含下列示範核心音訊 Api 使用的程式碼範例。 下列範例位於目錄% MSSdk% \\ 範例 \\ 多媒體 \\ 音訊中，其中% MSSdk% 是您電腦上 Windows SDK 安裝的根目錄。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>範例</th>
<th>Deascription</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="aecmicarray.md">AECMicArray</a></td>
<td>此範例會使用 MMDevice、WASAPI、DeviceTopology 和 EndpointVolume Api 來捕捉高品質的語音串流。 此範例支援聲場 echo 取消 (AEC) 和麥克風陣列處理，方法是使用 AEC，也稱為 Microsoft 提供的語音捕獲 DSP。</td>
</tr>
<tr class="even">
<td><a href="capturesharedeventdriven.md">CaptureSharedEventDriven</a></td>
<td>這個範例應用程式會使用核心音訊 Api 來從輸入裝置（由使用者指定）捕獲音訊資料，並將其寫入唯一命名的。目前的目錄中的 WAV 檔案。 這個範例示範事件驅動的緩衝。</td>
</tr>
<tr class="odd">
<td><a href="capturesharedtimerdriven.md">CaptureSharedTimerDriven</a></td>
<td>這個範例應用程式會使用核心音訊 Api 來從輸入裝置（由使用者指定）捕獲音訊資料，並將其寫入唯一命名的。目前的目錄中的 WAV 檔案。 這個範例示範計時器驅動的緩衝。</td>
</tr>
<tr class="even">
<td><a href="duckingcapturesample.md">DuckingCaptureSample</a></td>
<td>這個範例應用程式會示範如何開啟和關閉通訊資料流程，以及造成應用程式可取得以執行資料流程衰減的回避事件。 此應用程式會執行聊天用戶端，此用戶端會使用核心音訊 Api 從通訊裝置讀取音訊資料，並在輸出裝置上播放。</td>
</tr>
<tr class="odd">
<td><a href="endpointvolume.md">EndpointVolume</a></td>
<td>這個範例應用程式會使用核心音訊 Api 來變更由使用者指定的裝置數量。</td>
</tr>
<tr class="even">
<td><a href="osd.md">Osd</a></td>
<td>此範例會使用 MMDevice 和 EndpointVolume Api 來執行螢幕顯示，以顯示透過預設音訊轉譯端點裝置播放之輸出資料流程的音量變更。 當使用者調整 Windows 音量控制程式中的音量層級時，會顯示幕幕畫面顯示，Sndvol.exe，且在短時間內，磁片區層級保持不變之後就會消失。</td>
</tr>
<tr class="odd">
<td><a href="renderexclusiveeventdriven.md">RenderExclusiveEventDriven</a></td>
<td>這個範例應用程式會使用核心音訊 Api，將音訊資料轉譯至使用者指定的輸出裝置。 這個範例會示範在獨佔模式中呈現用戶端的事件驅動緩衝。 如果是獨佔模式資料流程，用戶端會與音訊裝置共用端點緩衝區。</td>
</tr>
<tr class="even">
<td><a href="renderexclusivetimerdriven.md">RenderExclusiveTimerDriven</a></td>
<td>這個範例應用程式會使用核心音訊 Api，將音訊資料轉譯至使用者指定的輸出裝置。 這個範例會示範在獨佔模式中呈現用戶端的計時器驅動緩衝。 如果是獨佔模式資料流程，用戶端會與音訊裝置共用端點緩衝區。</td>
</tr>
<tr class="odd">
<td><a href="rendersharedeventdriven.md">RenderSharedEventDriven</a></td>
<td>這個範例應用程式會使用核心音訊 Api，將音訊資料轉譯至使用者指定的輸出裝置。 這個範例會示範在共用模式中呈現用戶端的事件驅動緩衝。 若是共用模式資料流程，用戶端會與音訊引擎共用端點緩衝區。</td>
</tr>
<tr class="even">
<td><a href="rendersharedtimerdriven.md">RenderSharedTimerDriven</a></td>
<td>這個範例應用程式會使用核心音訊 Api，將音訊資料轉譯至使用者指定的輸出裝置。 這個範例會示範在共用模式中呈現用戶端的計時器驅動緩衝。 若是共用模式資料流程，用戶端會與音訊引擎共用端點緩衝區。</td>
</tr>
<tr class="odd">
<td>WinAudio</td>
<td>此範例會使用 MMDevice API 和 WASAPI 來播放和捕獲音訊串流。 這個範例應用程式的使用者介面可讓使用者選取音訊端點裝置、變更本機音訊會話的音量層級，以及播放 .wav 檔和麥克風輸入。
<blockquote>
[!Note]<br />
此範例已在 Windows 7 中淘汰。
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

您可以從 [Microsoft Windows SDK 下載中心](https://developer.microsoft.com/windows/downloads/sdk-archive/) 網站下載 Windows SDK。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於 Windows Core 音訊 Api](about-the-windows-core-audio-apis.md)
</dt> </dl>

 

 




