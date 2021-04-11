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
# <a name="sdk-samples-that-use-the-core-audio-apis"></a><span data-ttu-id="ccc52-103">使用核心音訊 Api 的 SDK 範例</span><span class="sxs-lookup"><span data-stu-id="ccc52-103">SDK Samples That Use the Core Audio APIs</span></span>

<span data-ttu-id="ccc52-104">Windows SDK 包含下列示範核心音訊 Api 使用的程式碼範例。</span><span class="sxs-lookup"><span data-stu-id="ccc52-104">The Windows SDK includes the following code samples that demonstrate the use of the Core Audio APIs.</span></span> <span data-ttu-id="ccc52-105">下列範例位於目錄% MSSdk% \\ 範例 \\ 多媒體 \\ 音訊中，其中% MSSdk% 是您電腦上 Windows SDK 安裝的根目錄。</span><span class="sxs-lookup"><span data-stu-id="ccc52-105">The following samples are located in the directory %MSSdk%\\samples\\multimedia\\audio, where %MSSdk% is the root directory of the Windows SDK installation on your computer.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ccc52-106">範例</span><span class="sxs-lookup"><span data-stu-id="ccc52-106">Sample</span></span></th>
<th><span data-ttu-id="ccc52-107">Deascription</span><span class="sxs-lookup"><span data-stu-id="ccc52-107">Deascription</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ccc52-108"><a href="aecmicarray.md">AECMicArray</a></span><span class="sxs-lookup"><span data-stu-id="ccc52-108"><a href="aecmicarray.md">AECMicArray</a></span></span></td>
<td><span data-ttu-id="ccc52-109">此範例會使用 MMDevice、WASAPI、DeviceTopology 和 EndpointVolume Api 來捕捉高品質的語音串流。</span><span class="sxs-lookup"><span data-stu-id="ccc52-109">This sample uses the MMDevice, WASAPI, DeviceTopology, and EndpointVolume APIs to capture a high-quality voice stream.</span></span> <span data-ttu-id="ccc52-110">此範例支援聲場 echo 取消 (AEC) 和麥克風陣列處理，方法是使用 AEC，也稱為 Microsoft 提供的語音捕獲 DSP。</span><span class="sxs-lookup"><span data-stu-id="ccc52-110">TThe sample supports acoustic echo cancellation (AEC) and microphone array processing by using the AEC DMO also called the Voice capture DSP provided by Microsoft .</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ccc52-111"><a href="capturesharedeventdriven.md">CaptureSharedEventDriven</a></span><span class="sxs-lookup"><span data-stu-id="ccc52-111"><a href="capturesharedeventdriven.md">CaptureSharedEventDriven</a></span></span></td>
<td><span data-ttu-id="ccc52-112">這個範例應用程式會使用核心音訊 Api 來從輸入裝置（由使用者指定）捕獲音訊資料，並將其寫入唯一命名的。目前的目錄中的 WAV 檔案。</span><span class="sxs-lookup"><span data-stu-id="ccc52-112">This sample application uses the Core Audio APIs to capture audio data from an input device, specified by the user and writes it to a uniquely named .WAV file in the current directory.</span></span> <span data-ttu-id="ccc52-113">這個範例示範事件驅動的緩衝。</span><span class="sxs-lookup"><span data-stu-id="ccc52-113">This sample demonstrates event-driven buffering.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ccc52-114"><a href="capturesharedtimerdriven.md">CaptureSharedTimerDriven</a></span><span class="sxs-lookup"><span data-stu-id="ccc52-114"><a href="capturesharedtimerdriven.md">CaptureSharedTimerDriven</a></span></span></td>
<td><span data-ttu-id="ccc52-115">這個範例應用程式會使用核心音訊 Api 來從輸入裝置（由使用者指定）捕獲音訊資料，並將其寫入唯一命名的。目前的目錄中的 WAV 檔案。</span><span class="sxs-lookup"><span data-stu-id="ccc52-115">This sample application uses the Core Audio APIs to capture audio data from an input device, specified by the user and writes it to a uniquely named .WAV file in the current directory.</span></span> <span data-ttu-id="ccc52-116">這個範例示範計時器驅動的緩衝。</span><span class="sxs-lookup"><span data-stu-id="ccc52-116">This sample demonstrates timer-driven buffering.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ccc52-117"><a href="duckingcapturesample.md">DuckingCaptureSample</a></span><span class="sxs-lookup"><span data-stu-id="ccc52-117"><a href="duckingcapturesample.md">DuckingCaptureSample</a></span></span></td>
<td><span data-ttu-id="ccc52-118">這個範例應用程式會示範如何開啟和關閉通訊資料流程，以及造成應用程式可取得以執行資料流程衰減的回避事件。</span><span class="sxs-lookup"><span data-stu-id="ccc52-118">This sample application demonstrates opening and closing communication streams and causing ducking events that an application can get to implement stream attenuation.</span></span> <span data-ttu-id="ccc52-119">此應用程式會執行聊天用戶端，此用戶端會使用核心音訊 Api 從通訊裝置讀取音訊資料，並在輸出裝置上播放。</span><span class="sxs-lookup"><span data-stu-id="ccc52-119">This application implements a chat client that uses Core Audio APIs to read audio data from a communication device and to play it on the output device.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ccc52-120"><a href="endpointvolume.md">EndpointVolume</a></span><span class="sxs-lookup"><span data-stu-id="ccc52-120"><a href="endpointvolume.md">EndpointVolume</a></span></span></td>
<td><span data-ttu-id="ccc52-121">這個範例應用程式會使用核心音訊 Api 來變更由使用者指定的裝置數量。</span><span class="sxs-lookup"><span data-stu-id="ccc52-121">This sample application uses the Core Audio APIs to change the volume of the device, specified by the user.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ccc52-122"><a href="osd.md">Osd</a></span><span class="sxs-lookup"><span data-stu-id="ccc52-122"><a href="osd.md">OSD</a></span></span></td>
<td><span data-ttu-id="ccc52-123">此範例會使用 MMDevice 和 EndpointVolume Api 來執行螢幕顯示，以顯示透過預設音訊轉譯端點裝置播放之輸出資料流程的音量變更。</span><span class="sxs-lookup"><span data-stu-id="ccc52-123">This sample uses the MMDevice and EndpointVolume APIs to implement an on-screen display that shows volume changes to the output stream that plays through the default audio-rendering endpoint device.</span></span> <span data-ttu-id="ccc52-124">當使用者調整 Windows 音量控制程式中的音量層級時，會顯示幕幕畫面顯示，Sndvol.exe，且在短時間內，磁片區層級保持不變之後就會消失。</span><span class="sxs-lookup"><span data-stu-id="ccc52-124">The on-screen display appears when the user adjusts the volume level in the Windows volume-control program, Sndvol.exe, and it disappears after the volume level remains unchanged for a short period.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ccc52-125"><a href="renderexclusiveeventdriven.md">RenderExclusiveEventDriven</a></span><span class="sxs-lookup"><span data-stu-id="ccc52-125"><a href="renderexclusiveeventdriven.md">RenderExclusiveEventDriven</a></span></span></td>
<td><span data-ttu-id="ccc52-126">這個範例應用程式會使用核心音訊 Api，將音訊資料轉譯至使用者指定的輸出裝置。</span><span class="sxs-lookup"><span data-stu-id="ccc52-126">This sample application uses the Core Audio APIs to render audio data to an output device, specified by the user.</span></span> <span data-ttu-id="ccc52-127">這個範例會示範在獨佔模式中呈現用戶端的事件驅動緩衝。</span><span class="sxs-lookup"><span data-stu-id="ccc52-127">This sample demonstrates event-driven buffering for a rendering client in exclusive mode.</span></span> <span data-ttu-id="ccc52-128">如果是獨佔模式資料流程，用戶端會與音訊裝置共用端點緩衝區。</span><span class="sxs-lookup"><span data-stu-id="ccc52-128">For an exclusive-mode stream, the client shares the endpoint buffer with the audio device.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ccc52-129"><a href="renderexclusivetimerdriven.md">RenderExclusiveTimerDriven</a></span><span class="sxs-lookup"><span data-stu-id="ccc52-129"><a href="renderexclusivetimerdriven.md">RenderExclusiveTimerDriven</a></span></span></td>
<td><span data-ttu-id="ccc52-130">這個範例應用程式會使用核心音訊 Api，將音訊資料轉譯至使用者指定的輸出裝置。</span><span class="sxs-lookup"><span data-stu-id="ccc52-130">This sample application uses the Core Audio APIs to render audio data to an output device, specified by the user.</span></span> <span data-ttu-id="ccc52-131">這個範例會示範在獨佔模式中呈現用戶端的計時器驅動緩衝。</span><span class="sxs-lookup"><span data-stu-id="ccc52-131">This sample demonstrates timer-driven buffering for a rendering client in exclusive mode.</span></span> <span data-ttu-id="ccc52-132">如果是獨佔模式資料流程，用戶端會與音訊裝置共用端點緩衝區。</span><span class="sxs-lookup"><span data-stu-id="ccc52-132">For an exclusive-mode stream, the client shares the endpoint buffer with the audio device.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ccc52-133"><a href="rendersharedeventdriven.md">RenderSharedEventDriven</a></span><span class="sxs-lookup"><span data-stu-id="ccc52-133"><a href="rendersharedeventdriven.md">RenderSharedEventDriven</a></span></span></td>
<td><span data-ttu-id="ccc52-134">這個範例應用程式會使用核心音訊 Api，將音訊資料轉譯至使用者指定的輸出裝置。</span><span class="sxs-lookup"><span data-stu-id="ccc52-134">This sample application uses the Core Audio APIs to render audio data to an output device, specified by the user.</span></span> <span data-ttu-id="ccc52-135">這個範例會示範在共用模式中呈現用戶端的事件驅動緩衝。</span><span class="sxs-lookup"><span data-stu-id="ccc52-135">This sample demonstrates event-driven buffering for a rendering client in shared mode.</span></span> <span data-ttu-id="ccc52-136">若是共用模式資料流程，用戶端會與音訊引擎共用端點緩衝區。</span><span class="sxs-lookup"><span data-stu-id="ccc52-136">For a shared-mode stream, the client shares the endpoint buffer with the audio engine.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ccc52-137"><a href="rendersharedtimerdriven.md">RenderSharedTimerDriven</a></span><span class="sxs-lookup"><span data-stu-id="ccc52-137"><a href="rendersharedtimerdriven.md">RenderSharedTimerDriven</a></span></span></td>
<td><span data-ttu-id="ccc52-138">這個範例應用程式會使用核心音訊 Api，將音訊資料轉譯至使用者指定的輸出裝置。</span><span class="sxs-lookup"><span data-stu-id="ccc52-138">This sample application uses the Core Audio APIs to render audio data to an output device, specified by the user.</span></span> <span data-ttu-id="ccc52-139">這個範例會示範在共用模式中呈現用戶端的計時器驅動緩衝。</span><span class="sxs-lookup"><span data-stu-id="ccc52-139">This sample demonstrates timer-driven buffering for a rendering client in shared mode.</span></span> <span data-ttu-id="ccc52-140">若是共用模式資料流程，用戶端會與音訊引擎共用端點緩衝區。</span><span class="sxs-lookup"><span data-stu-id="ccc52-140">For a shared-mode stream, the client shares the endpoint buffer with the audio engine.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ccc52-141">WinAudio</span><span class="sxs-lookup"><span data-stu-id="ccc52-141">WinAudio</span></span></td>
<td><span data-ttu-id="ccc52-142">此範例會使用 MMDevice API 和 WASAPI 來播放和捕獲音訊串流。</span><span class="sxs-lookup"><span data-stu-id="ccc52-142">This sample uses the MMDevice API and WASAPI to play and capture audio streams.</span></span> <span data-ttu-id="ccc52-143">這個範例應用程式的使用者介面可讓使用者選取音訊端點裝置、變更本機音訊會話的音量層級，以及播放 .wav 檔和麥克風輸入。</span><span class="sxs-lookup"><span data-stu-id="ccc52-143">The user interface of this sample application enables users to select audio endpoint devices, to change the volume level of the local audio session, and to play .wav files and microphone input.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="ccc52-144">此範例已在 Windows 7 中淘汰。</span><span class="sxs-lookup"><span data-stu-id="ccc52-144">This sample has been deprecated in Windows 7.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="ccc52-145">您可以從 [Microsoft Windows SDK 下載中心](https://developer.microsoft.com/windows/downloads/sdk-archive/) 網站下載 Windows SDK。</span><span class="sxs-lookup"><span data-stu-id="ccc52-145">You can download the Windows SDK from the [Microsoft Windows SDK Download Center](https://developer.microsoft.com/windows/downloads/sdk-archive/) website.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ccc52-146">相關主題</span><span class="sxs-lookup"><span data-stu-id="ccc52-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ccc52-147">關於 Windows Core 音訊 Api</span><span class="sxs-lookup"><span data-stu-id="ccc52-147">About the Windows Core Audio APIs</span></span>](about-the-windows-core-audio-apis.md)
</dt> </dl>

 

 




