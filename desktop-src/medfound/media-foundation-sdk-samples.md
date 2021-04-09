---
description: 本節說明範例應用程式，示範如何使用媒體基礎的編碼 SamplesPlayback SamplesPlug-InsSource Reader SamplesVideo CaptureMiscellaneous SamplesDeprecated 或淘汰的 SamplesRelated 主題
ms.assetid: 9d460107-ec12-4df5-a7a9-d19943685599
title: 媒體基礎 SDK 範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f335b5ba744b098efdb7570aa861ad36fc9216cf
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "103696234"
---
# <a name="media-foundation-sdk-samples"></a><span data-ttu-id="7e1d3-103">媒體基礎 SDK 範例</span><span class="sxs-lookup"><span data-stu-id="7e1d3-103">Media Foundation SDK Samples</span></span>

<span data-ttu-id="7e1d3-104">本節說明示範如何使用媒體基礎的範例應用程式。</span><span class="sxs-lookup"><span data-stu-id="7e1d3-104">This section describes sample applications that demonstrate how to use Media Foundation.</span></span>

-   [<span data-ttu-id="7e1d3-105">編碼範例</span><span class="sxs-lookup"><span data-stu-id="7e1d3-105">Encoding Samples</span></span>](#encoding-samples)
-   [<span data-ttu-id="7e1d3-106">播放範例</span><span class="sxs-lookup"><span data-stu-id="7e1d3-106">Playback Samples</span></span>](#playback-samples)
-   [<span data-ttu-id="7e1d3-107">外掛程式</span><span class="sxs-lookup"><span data-stu-id="7e1d3-107">Plug-Ins</span></span>](#plug-ins)
-   [<span data-ttu-id="7e1d3-108">來源讀取器範例</span><span class="sxs-lookup"><span data-stu-id="7e1d3-108">Source Reader Samples</span></span>](#source-reader-samples)
-   [<span data-ttu-id="7e1d3-109">影片捕獲</span><span class="sxs-lookup"><span data-stu-id="7e1d3-109">Video Capture</span></span>](#video-capture)
-   [<span data-ttu-id="7e1d3-110">其他範例</span><span class="sxs-lookup"><span data-stu-id="7e1d3-110">Miscellaneous Samples</span></span>](#miscellaneous-samples)
-   [<span data-ttu-id="7e1d3-111">已淘汰或已淘汰的範例</span><span class="sxs-lookup"><span data-stu-id="7e1d3-111">Deprecated or Obsolete Samples</span></span>](#deprecated-or-obsolete-samples)
-   [<span data-ttu-id="7e1d3-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="7e1d3-112">Related topics</span></span>](#related-topics)

## <a name="encoding-samples"></a><span data-ttu-id="7e1d3-113">編碼範例</span><span class="sxs-lookup"><span data-stu-id="7e1d3-113">Encoding Samples</span></span>



| <span data-ttu-id="7e1d3-114">範例</span><span class="sxs-lookup"><span data-stu-id="7e1d3-114">Sample</span></span>                            | <span data-ttu-id="7e1d3-115">描述</span><span class="sxs-lookup"><span data-stu-id="7e1d3-115">Description</span></span>                                                 |
|-----------------------------------|-------------------------------------------------------------|
| [<span data-ttu-id="7e1d3-116">轉碼</span><span class="sxs-lookup"><span data-stu-id="7e1d3-116">Transcode</span></span>](transcode-sample.md) | <span data-ttu-id="7e1d3-117">說明如何將媒體檔案 reencode 為 Windows Media 格式。</span><span class="sxs-lookup"><span data-stu-id="7e1d3-117">Shows how to reencode a media file to Windows Media format.</span></span> |



 

## <a name="playback-samples"></a><span data-ttu-id="7e1d3-118">播放範例</span><span class="sxs-lookup"><span data-stu-id="7e1d3-118">Playback Samples</span></span>



| <span data-ttu-id="7e1d3-119">範例</span><span class="sxs-lookup"><span data-stu-id="7e1d3-119">Sample</span></span>                                            | <span data-ttu-id="7e1d3-120">描述</span><span class="sxs-lookup"><span data-stu-id="7e1d3-120">Description</span></span>                                                                                                                                                                                                     |
|---------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e1d3-121">[BasicPlayback](/previous-versions//bb970475(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7e1d3-121">[BasicPlayback](/previous-versions//bb970475(v=vs.85))</span></span>          | <span data-ttu-id="7e1d3-122">使用 [媒體會話](media-session.md)播放音訊和影片檔案。</span><span class="sxs-lookup"><span data-stu-id="7e1d3-122">Plays audio and video files by using the [Media Session](media-session.md).</span></span> <span data-ttu-id="7e1d3-123">這個範例示範如何建立播放拓撲、控制媒體會話，以及在播放期間接收會話事件。</span><span class="sxs-lookup"><span data-stu-id="7e1d3-123">This sample demonstrates how to create playback topologies, control the Media Session, and receive session events during playback.</span></span> |
| <span data-ttu-id="7e1d3-124">[MFPlayer](/previous-versions//bb970516(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7e1d3-124">[MFPlayer](/previous-versions//bb970516(v=vs.85))</span></span>                    | <span data-ttu-id="7e1d3-125">示範 [BasicPlayback](/previous-versions//bb970475(v=vs.85)) 範例中未包含的一些播放函式。</span><span class="sxs-lookup"><span data-stu-id="7e1d3-125">Demonstrates some playback functions that are not included in the [BasicPlayback](/previous-versions//bb970475(v=vs.85)) sample.</span></span>                                                                                              |
| [<span data-ttu-id="7e1d3-126">ProtectedPlayback</span><span class="sxs-lookup"><span data-stu-id="7e1d3-126">ProtectedPlayback</span></span>](protectedplayback-sample.md) | <span data-ttu-id="7e1d3-127">播放受保護的音訊和影片檔案。</span><span class="sxs-lookup"><span data-stu-id="7e1d3-127">Plays protected audio and video files.</span></span> <span data-ttu-id="7e1d3-128">此範例說明如何使用受保護的媒體路徑 (PMP) 會話，以及如何使用內容啟用程式物件。</span><span class="sxs-lookup"><span data-stu-id="7e1d3-128">This sample shows how to use the protected media path (PMP) session and how to use content enabler objects.</span></span>                                                              |



 

## <a name="plug-ins"></a><span data-ttu-id="7e1d3-129">Plug-Ins</span><span class="sxs-lookup"><span data-stu-id="7e1d3-129">Plug-Ins</span></span>



| <span data-ttu-id="7e1d3-130">範例</span><span class="sxs-lookup"><span data-stu-id="7e1d3-130">Sample</span></span>                                       | <span data-ttu-id="7e1d3-131">Sub-Area</span><span class="sxs-lookup"><span data-stu-id="7e1d3-131">Sub-Area</span></span>                         | <span data-ttu-id="7e1d3-132">Description</span><span class="sxs-lookup"><span data-stu-id="7e1d3-132">Description</span></span>                                                                                            |
|----------------------------------------------|----------------------------------|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7e1d3-133">解碼 器</span><span class="sxs-lookup"><span data-stu-id="7e1d3-133">Decoder</span></span>](decoder-sample.md)                | <span data-ttu-id="7e1d3-134">媒體基礎轉換 (MFT) </span><span class="sxs-lookup"><span data-stu-id="7e1d3-134">Media Foundation transform (MFT)</span></span> | <span data-ttu-id="7e1d3-135">影片解碼器。</span><span class="sxs-lookup"><span data-stu-id="7e1d3-135">Video decoder.</span></span>                                                                                         |
| [<span data-ttu-id="7e1d3-136">EVRPresenter</span><span class="sxs-lookup"><span data-stu-id="7e1d3-136">EVRPresenter</span></span>](evrpresenter-sample.md)      | <span data-ttu-id="7e1d3-137">其他</span><span class="sxs-lookup"><span data-stu-id="7e1d3-137">Miscellaneous</span></span>                    | <span data-ttu-id="7e1d3-138">[增強型影片](enhanced-video-renderer.md)轉譯器的自訂展示者 (EVR) 。</span><span class="sxs-lookup"><span data-stu-id="7e1d3-138">Custom presenter for the [Enhanced Video Renderer](enhanced-video-renderer.md) (EVR).</span></span>                 |
| [<span data-ttu-id="7e1d3-139">MFT \_ AudioDelay</span><span class="sxs-lookup"><span data-stu-id="7e1d3-139">MFT\_AudioDelay</span></span>](mft-audiodelay-sample.md) | <span data-ttu-id="7e1d3-140">Mft</span><span class="sxs-lookup"><span data-stu-id="7e1d3-140">MFT</span></span>                              | <span data-ttu-id="7e1d3-141">音訊效果轉換。</span><span class="sxs-lookup"><span data-stu-id="7e1d3-141">Audio effect transform.</span></span> <span data-ttu-id="7e1d3-142">說明如何撰寫音訊處理的基本 MFT。</span><span class="sxs-lookup"><span data-stu-id="7e1d3-142">Shows how to write a basic MFT for audio processing.</span></span>                           |
| [<span data-ttu-id="7e1d3-143">MFT \_ 灰階</span><span class="sxs-lookup"><span data-stu-id="7e1d3-143">MFT\_Grayscale</span></span>](mft-grayscale-sample.md)   | <span data-ttu-id="7e1d3-144">Mft</span><span class="sxs-lookup"><span data-stu-id="7e1d3-144">MFT</span></span>                              | <span data-ttu-id="7e1d3-145">灰階影片效果。</span><span class="sxs-lookup"><span data-stu-id="7e1d3-145">Grayscale video effect.</span></span> <span data-ttu-id="7e1d3-146">說明如何撰寫影片處理的基本 MFT。</span><span class="sxs-lookup"><span data-stu-id="7e1d3-146">Shows how to write a basic MFT for video processing.</span></span>                           |
| [<span data-ttu-id="7e1d3-147">MPEG1Source</span><span class="sxs-lookup"><span data-stu-id="7e1d3-147">MPEG1Source</span></span>](mpeg1source-sample.md)        | <span data-ttu-id="7e1d3-148">媒體來源</span><span class="sxs-lookup"><span data-stu-id="7e1d3-148">Media source</span></span>                     | <span data-ttu-id="7e1d3-149">剖析 MPEG-2 系統層串流。</span><span class="sxs-lookup"><span data-stu-id="7e1d3-149">Parses MPEG-1 systems-layer streams.</span></span> <span data-ttu-id="7e1d3-150">說明如何撰寫自訂媒體來源和位元組資料流程處理常式。</span><span class="sxs-lookup"><span data-stu-id="7e1d3-150">Shows how to write a custom media source and byte-stream handler.</span></span> |
| [<span data-ttu-id="7e1d3-151">WavSink</span><span class="sxs-lookup"><span data-stu-id="7e1d3-151">WavSink</span></span>](wavsink-sample.md)                | <span data-ttu-id="7e1d3-152">媒體接收器</span><span class="sxs-lookup"><span data-stu-id="7e1d3-152">Media sink</span></span>                       | <span data-ttu-id="7e1d3-153">寫入 .wav 檔案的封存接收。</span><span class="sxs-lookup"><span data-stu-id="7e1d3-153">An archive sink that writes .wav files.</span></span> <span data-ttu-id="7e1d3-154">說明如何撰寫自訂媒體接收。</span><span class="sxs-lookup"><span data-stu-id="7e1d3-154">Shows how to write a custom media sink.</span></span>                        |
| [<span data-ttu-id="7e1d3-155">WavSource</span><span class="sxs-lookup"><span data-stu-id="7e1d3-155">WavSource</span></span>](wavsource-sample.md)            | <span data-ttu-id="7e1d3-156">媒體來源</span><span class="sxs-lookup"><span data-stu-id="7e1d3-156">Media source</span></span>                     | <span data-ttu-id="7e1d3-157">剖析 .wav 檔。</span><span class="sxs-lookup"><span data-stu-id="7e1d3-157">Parses .wav files.</span></span> <span data-ttu-id="7e1d3-158">說明如何撰寫自訂媒體來源和位元組資料流程處理常式。</span><span class="sxs-lookup"><span data-stu-id="7e1d3-158">Shows how to write a custom media source and byte-stream handler.</span></span>                   |



 

## <a name="source-reader-samples"></a><span data-ttu-id="7e1d3-159">來源讀取器範例</span><span class="sxs-lookup"><span data-stu-id="7e1d3-159">Source Reader Samples</span></span>



| <span data-ttu-id="7e1d3-160">範例</span><span class="sxs-lookup"><span data-stu-id="7e1d3-160">Sample</span></span>                                      | <span data-ttu-id="7e1d3-161">描述</span><span class="sxs-lookup"><span data-stu-id="7e1d3-161">Description</span></span>                                                                         |
|---------------------------------------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="7e1d3-162">音訊剪輯</span><span class="sxs-lookup"><span data-stu-id="7e1d3-162">Audio Clip</span></span>](audio-clip-sample.md)         | <span data-ttu-id="7e1d3-163">使用 [來源讀取器](source-reader.md) 將音訊從媒體檔案解碼。</span><span class="sxs-lookup"><span data-stu-id="7e1d3-163">Uses the [Source Reader](source-reader.md) to decode audio from a media file.</span></span>      |
| [<span data-ttu-id="7e1d3-164">VideoThumbnail</span><span class="sxs-lookup"><span data-stu-id="7e1d3-164">VideoThumbnail</span></span>](videothumbnail-sample.md) | <span data-ttu-id="7e1d3-165">使用 [來源讀取器](source-reader.md) 從影片檔案取得單一畫面格。</span><span class="sxs-lookup"><span data-stu-id="7e1d3-165">Uses the [Source Reader](source-reader.md) to get single frames from a video file.</span></span> |



 

## <a name="video-capture"></a><span data-ttu-id="7e1d3-166">影片捕獲</span><span class="sxs-lookup"><span data-stu-id="7e1d3-166">Video Capture</span></span>



| <span data-ttu-id="7e1d3-167">範例</span><span class="sxs-lookup"><span data-stu-id="7e1d3-167">Sample</span></span>                                        | <span data-ttu-id="7e1d3-168">描述</span><span class="sxs-lookup"><span data-stu-id="7e1d3-168">Description</span></span>                                                                                 |
|-----------------------------------------------|---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7e1d3-169">MFCaptureD3D</span><span class="sxs-lookup"><span data-stu-id="7e1d3-169">MFCaptureD3D</span></span>](mfcaptured3d-sample.md)       | <span data-ttu-id="7e1d3-170">示範如何使用 Direct3D 轉譯影片，從影片捕獲裝置預覽影片。</span><span class="sxs-lookup"><span data-stu-id="7e1d3-170">Shows how to preview video from a video capture device, using Direct3D to render the video.</span></span> |
| [<span data-ttu-id="7e1d3-171">MFCaptureToFile</span><span class="sxs-lookup"><span data-stu-id="7e1d3-171">MFCaptureToFile</span></span>](mfcapturetofile-sample.md) | <span data-ttu-id="7e1d3-172">說明如何從攝影機將影片捕獲到檔案。</span><span class="sxs-lookup"><span data-stu-id="7e1d3-172">Shows how to capture video from a video camera to a file.</span></span>                                   |



 

## <a name="miscellaneous-samples"></a><span data-ttu-id="7e1d3-173">其他範例</span><span class="sxs-lookup"><span data-stu-id="7e1d3-173">Miscellaneous Samples</span></span>



| <span data-ttu-id="7e1d3-174">範例</span><span class="sxs-lookup"><span data-stu-id="7e1d3-174">Sample</span></span>                                         | <span data-ttu-id="7e1d3-175">描述</span><span class="sxs-lookup"><span data-stu-id="7e1d3-175">Description</span></span>                                                                                                                                           |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7e1d3-176">ASFParser</span><span class="sxs-lookup"><span data-stu-id="7e1d3-176">ASFParser</span></span>](asfparser-sample.md)              | <span data-ttu-id="7e1d3-177">示範如何從 Advanced 系統格式剖析資料， (ASF) 檔。</span><span class="sxs-lookup"><span data-stu-id="7e1d3-177">Shows how to parse data from an Advanced Systems Format (ASF) file.</span></span>                                                                                   |
| [<span data-ttu-id="7e1d3-178">DXVA-HD</span><span class="sxs-lookup"><span data-stu-id="7e1d3-178">DXVA-HD</span></span>](dxva-hd-sample.md)                  | <span data-ttu-id="7e1d3-179">說明如何使用 Microsoft DirectX Video 加速 High Definition (DXVA-HD) 。</span><span class="sxs-lookup"><span data-stu-id="7e1d3-179">Shows how to use Microsoft DirectX Video Acceleration High Definition (DXVA-HD).</span></span>                                                                      |
| [<span data-ttu-id="7e1d3-180">DXVA2 \_ VideoProc</span><span class="sxs-lookup"><span data-stu-id="7e1d3-180">DXVA2\_VideoProc</span></span>](dxva2-videoproc-sample.md) | <span data-ttu-id="7e1d3-181">使用 DirectX Video 加速 (DXVA) 2.0 來建立 4:2:2 YUV 影片的串流。</span><span class="sxs-lookup"><span data-stu-id="7e1d3-181">Uses DirectX Video Acceleration (DXVA) 2.0 to create a stream of 4:2:2 YUV video.</span></span> <span data-ttu-id="7e1d3-182">此範例說明如何使用 DXVA 的影片處理功能。</span><span class="sxs-lookup"><span data-stu-id="7e1d3-182">This sample shows how to use the video processing features of DXVA.</span></span> |



 

## <a name="deprecated-or-obsolete-samples"></a><span data-ttu-id="7e1d3-183">已淘汰或已淘汰的範例</span><span class="sxs-lookup"><span data-stu-id="7e1d3-183">Deprecated or Obsolete Samples</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7e1d3-184">範例</span><span class="sxs-lookup"><span data-stu-id="7e1d3-184">Sample</span></span></th>
<th><span data-ttu-id="7e1d3-185">描述</span><span class="sxs-lookup"><span data-stu-id="7e1d3-185">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7e1d3-186"><a href="mfplayer2-sample.md">MFPlayer2</a></span><span class="sxs-lookup"><span data-stu-id="7e1d3-186"><a href="mfplayer2-sample.md">MFPlayer2</a></span></span></td>
<td><span data-ttu-id="7e1d3-187">示範 <a href="using-mfplay-for-audio-video-playback.md">MFPlay</a> API 的一些先進播放功能。</span><span class="sxs-lookup"><span data-stu-id="7e1d3-187">Demonstrates some advanced playback features of the <a href="using-mfplay-for-audio-video-playback.md">MFPlay</a> API.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7e1d3-188"><a href="/previous-versions//bb970336(v=vs.85)">PlaybackFX</a></span><span class="sxs-lookup"><span data-stu-id="7e1d3-188"><a href="/previous-versions//bb970336(v=vs.85)">PlaybackFX</a></span></span></td>
<td><span data-ttu-id="7e1d3-189">將灰階效果套用到影片。</span><span class="sxs-lookup"><span data-stu-id="7e1d3-189">Applies a grayscale effect to video.</span></span> <span data-ttu-id="7e1d3-190">說明如何將 MFTs 插入播放拓撲中。</span><span class="sxs-lookup"><span data-stu-id="7e1d3-190">Shows how to insert MFTs into a playback topology.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="7e1d3-191">SDK 中已不再包含此範例。</span><span class="sxs-lookup"><span data-stu-id="7e1d3-191">This sample is no longer included in the SDK.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7e1d3-192"><a href="playlist-sample.md">播放 清單</a></span><span class="sxs-lookup"><span data-stu-id="7e1d3-192"><a href="playlist-sample.md">Playlist</a></span></span></td>
<td><span data-ttu-id="7e1d3-193">使用 sequencer 來源播放一系列的音訊檔案。</span><span class="sxs-lookup"><span data-stu-id="7e1d3-193">Plays a sequence of audio files using the sequencer source.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="7e1d3-194">SDK 中已不再包含此範例。</span><span class="sxs-lookup"><span data-stu-id="7e1d3-194">This sample is no longer included in the SDK.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7e1d3-195"><a href="simplecapture-sample.md">SimpleCapture</a></span><span class="sxs-lookup"><span data-stu-id="7e1d3-195"><a href="simplecapture-sample.md">SimpleCapture</a></span></span></td>
<td><span data-ttu-id="7e1d3-196">說明如何使用 MFPlay API，從影片捕獲裝置預覽影片。</span><span class="sxs-lookup"><span data-stu-id="7e1d3-196">Shows how to preview video from a video capture device, using the MFPlay API.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7e1d3-197"><a href="simpleplay-sample.md">SimplePlay</a></span><span class="sxs-lookup"><span data-stu-id="7e1d3-197"><a href="simpleplay-sample.md">SimplePlay</a></span></span></td>
<td><span data-ttu-id="7e1d3-198">說明如何使用 MFPlay API 播放媒體檔案。</span><span class="sxs-lookup"><span data-stu-id="7e1d3-198">Shows how to play a media file using the MFPlay API.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="7e1d3-199">相關主題</span><span class="sxs-lookup"><span data-stu-id="7e1d3-199">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7e1d3-200">Microsoft 媒體基礎</span><span class="sxs-lookup"><span data-stu-id="7e1d3-200">Microsoft Media Foundation</span></span>](microsoft-media-foundation-sdk.md)
</dt> <dt>

[<span data-ttu-id="7e1d3-201">關於媒體基礎</span><span class="sxs-lookup"><span data-stu-id="7e1d3-201">About Media Foundation</span></span>](about-the-media-foundation-sdk.md)
</dt> </dl>

 

 
