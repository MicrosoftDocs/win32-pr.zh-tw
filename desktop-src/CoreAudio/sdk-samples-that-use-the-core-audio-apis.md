---
description: 使用核心音訊 Api 的 SDK 範例
ms.assetid: 4460df28-a77d-4bf5-9dee-5fb69ba2ded6
title: 使用核心音訊 Api 的 SDK 範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f875095579b40c6646d89e31328c148c5724c309
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479694"
---
# <a name="sdk-samples-that-use-the-core-audio-apis"></a>使用核心音訊 Api 的 SDK 範例

Windows SDK 包含下列示範核心音訊 api 使用的程式碼範例。 下列範例位於目錄% MSSdk% \\ 範例 \\ 多媒體 \\ 音訊中，其中% MSSdk% 是您電腦上 Windows SDK 安裝的根目錄。




| 範例 | Deascription | 
|--------|--------------|
| <a href="aecmicarray.md">AECMicArray</a> | 此範例會使用 MMDevice、WASAPI、DeviceTopology 和 EndpointVolume Api 來捕捉高品質的語音串流。 此範例支援聲場 echo 取消 (aec) 和麥克風陣列處理，方法是使用 AEC DMO 也稱為 Microsoft 所提供的語音捕獲 DSP。 | 
| <a href="capturesharedeventdriven.md">CaptureSharedEventDriven</a> | 這個範例應用程式會使用核心音訊 Api 來從輸入裝置（由使用者指定）捕獲音訊資料，並將其寫入唯一命名的。目前的目錄中的 WAV 檔案。 這個範例示範事件驅動的緩衝。 | 
| <a href="capturesharedtimerdriven.md">CaptureSharedTimerDriven</a> | 這個範例應用程式會使用核心音訊 Api 來從輸入裝置（由使用者指定）捕獲音訊資料，並將其寫入唯一命名的。目前的目錄中的 WAV 檔案。 這個範例示範計時器驅動的緩衝。 | 
| <a href="duckingcapturesample.md">DuckingCaptureSample</a> | 這個範例應用程式會示範如何開啟和關閉通訊資料流程，以及造成應用程式可取得以執行資料流程衰減的回避事件。 此應用程式會執行聊天用戶端，此用戶端會使用核心音訊 Api 從通訊裝置讀取音訊資料，並在輸出裝置上播放。 | 
| <a href="endpointvolume.md">EndpointVolume</a> | 這個範例應用程式會使用核心音訊 Api 來變更由使用者指定的裝置數量。 | 
| <a href="osd.md">OSD</a> | 此範例會使用 MMDevice 和 EndpointVolume Api 來執行螢幕顯示，以顯示透過預設音訊轉譯端點裝置播放之輸出資料流程的音量變更。 當使用者調整 Windows 音量控制程式中的音量層級時，畫面上顯示畫面會顯示 Sndvol.exe，而且在短時間內，磁片區層級會維持不變。 | 
| <a href="renderexclusiveeventdriven.md">RenderExclusiveEventDriven</a> | 這個範例應用程式會使用核心音訊 Api，將音訊資料轉譯至使用者指定的輸出裝置。 這個範例會示範在獨佔模式中呈現用戶端的事件驅動緩衝。 如果是獨佔模式資料流程，用戶端會與音訊裝置共用端點緩衝區。 | 
| <a href="renderexclusivetimerdriven.md">RenderExclusiveTimerDriven</a> | 這個範例應用程式會使用核心音訊 Api，將音訊資料轉譯至使用者指定的輸出裝置。 這個範例會示範在獨佔模式中呈現用戶端的計時器驅動緩衝。 如果是獨佔模式資料流程，用戶端會與音訊裝置共用端點緩衝區。 | 
| <a href="rendersharedeventdriven.md">RenderSharedEventDriven</a> | 這個範例應用程式會使用核心音訊 Api，將音訊資料轉譯至使用者指定的輸出裝置。 這個範例會示範在共用模式中呈現用戶端的事件驅動緩衝。 若是共用模式資料流程，用戶端會與音訊引擎共用端點緩衝區。 | 
| <a href="rendersharedtimerdriven.md">RenderSharedTimerDriven</a> | 這個範例應用程式會使用核心音訊 Api，將音訊資料轉譯至使用者指定的輸出裝置。 這個範例會示範在共用模式中呈現用戶端的計時器驅動緩衝。 若是共用模式資料流程，用戶端會與音訊引擎共用端點緩衝區。 | 
| WinAudio | 此範例會使用 MMDevice API 和 WASAPI 來播放和捕獲音訊串流。 這個範例應用程式的使用者介面可讓使用者選取音訊端點裝置、變更本機音訊會話的音量層級，以及播放 .wav 檔和麥克風輸入。<blockquote>[!Note]<br />此範例已在 Windows 7 中淘汰。</blockquote><br /> | 




 

您可以從[Microsoft Windows SDK 下載中心](https://developer.microsoft.com/windows/downloads/sdk-archive/)網站下載 Windows SDK。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於 Windows Core 音訊 api](about-the-windows-core-audio-apis.md)
</dt> </dl>

 

 




