---
description: Microsoft 媒體基礎是在 Windows Vista 中引進，作為 DirectShow 的取代。 當然，Windows 7 仍支援 DirectShow，但鼓勵開發人員在新的數位媒體應用程式中使用媒體基礎。
ms.assetid: c345c0d9-5325-4f73-b9ec-1673ad10e3e4
title: 媒體基礎的新新
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0270c28e5aca2a1f0fdad893743a1e8fb630fa5
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "104321523"
---
# <a name="whats-new-for-media-foundation"></a><span data-ttu-id="ba585-104">媒體基礎的新功能</span><span class="sxs-lookup"><span data-stu-id="ba585-104">What's New for Media Foundation</span></span>

<span data-ttu-id="ba585-105">Microsoft 媒體基礎是在 Windows Vista 中引進，作為 DirectShow 的取代。</span><span class="sxs-lookup"><span data-stu-id="ba585-105">Microsoft Media Foundation was introduced in Windows Vista as the replacement for DirectShow.</span></span> <span data-ttu-id="ba585-106">當然，Windows 7 仍支援 DirectShow，但鼓勵開發人員在新的數位媒體應用程式中使用媒體基礎。</span><span class="sxs-lookup"><span data-stu-id="ba585-106">Of course, DirectShow is still supported in Windows 7, but developers are encouraged to use Media Foundation in their new digital media applications.</span></span>

<span data-ttu-id="ba585-107">媒體基礎的改進可摘要如下：</span><span class="sxs-lookup"><span data-stu-id="ba585-107">The improvements to Media Foundation can be summarized as follows:</span></span>

-   <span data-ttu-id="ba585-108">更好的格式支援，包括 MPEG 4</span><span class="sxs-lookup"><span data-stu-id="ba585-108">Better format support, including MPEG-4</span></span>
-   <span data-ttu-id="ba585-109">支援捕獲裝置和硬體編解碼器</span><span class="sxs-lookup"><span data-stu-id="ba585-109">Support for capture devices and hardware codecs</span></span>
-   <span data-ttu-id="ba585-110">簡化的程式設計模型</span><span class="sxs-lookup"><span data-stu-id="ba585-110">A simplified programming model</span></span>
-   <span data-ttu-id="ba585-111">平臺的改進</span><span class="sxs-lookup"><span data-stu-id="ba585-111">Improvements to the platform</span></span>

## <a name="better-format-support"></a><span data-ttu-id="ba585-112">更好的格式支援</span><span class="sxs-lookup"><span data-stu-id="ba585-112">Better Format Support</span></span>

<span data-ttu-id="ba585-113">媒體基礎的音訊/影片管線是在 Windows Vista 中執行，但它支援一組有限的格式和檔案容器，這表示某些應用程式需要在較舊的技術（例如 DirectShow）上切換。</span><span class="sxs-lookup"><span data-stu-id="ba585-113">The Media Foundation audio/video pipeline was implemented in Windows Vista, but it supported a limited set of formats and file containers, which meant that some applications needed to fall back on older technologies such as DirectShow.</span></span> <span data-ttu-id="ba585-114">在 Windows 7 中，媒體基礎包含下列新的編解碼器、媒體來源和媒體接收器：</span><span class="sxs-lookup"><span data-stu-id="ba585-114">In Windows 7, Media Foundation includes the following new codecs, media sources, and media sinks:</span></span>

-   <span data-ttu-id="ba585-115">AAC 解碼器</span><span class="sxs-lookup"><span data-stu-id="ba585-115">AAC decoder</span></span>
-   <span data-ttu-id="ba585-116">AAC 編碼器</span><span class="sxs-lookup"><span data-stu-id="ba585-116">AAC encoder</span></span>
-   <span data-ttu-id="ba585-117">AVI/WAVE 檔案來源</span><span class="sxs-lookup"><span data-stu-id="ba585-117">AVI/WAVE file source</span></span>
-   <span data-ttu-id="ba585-118">DV 影片解碼</span><span class="sxs-lookup"><span data-stu-id="ba585-118">DV video decoder</span></span>
-   <span data-ttu-id="ba585-119">H.264 video 解碼</span><span class="sxs-lookup"><span data-stu-id="ba585-119">H.264 video decoder</span></span>
-   <span data-ttu-id="ba585-120">H.264 影片編碼器</span><span class="sxs-lookup"><span data-stu-id="ba585-120">H.264 video encoder</span></span>
-   <span data-ttu-id="ba585-121">MJPEG 解碼器</span><span class="sxs-lookup"><span data-stu-id="ba585-121">MJPEG decoder</span></span>
-   <span data-ttu-id="ba585-122">MP3 檔案接收\*</span><span class="sxs-lookup"><span data-stu-id="ba585-122">MP3 file sink\*</span></span>
-   <span data-ttu-id="ba585-123">3GP 檔案來源</span><span class="sxs-lookup"><span data-stu-id="ba585-123">MP4/3GP file source</span></span>
-   <span data-ttu-id="ba585-124">3GP 檔案接收</span><span class="sxs-lookup"><span data-stu-id="ba585-124">MP4/3GP file sink</span></span>

> [!Note]  
> <span data-ttu-id="ba585-125">MP3 檔案接收不包含 MP3 音訊編碼器。</span><span class="sxs-lookup"><span data-stu-id="ba585-125">The MP3 file sink does not include an MP3 audio encoder.</span></span>

 

<span data-ttu-id="ba585-126">如需詳細資訊，請參閱 [媒體基礎中支援的媒體格式](supported-media-formats-in-media-foundation.md)。</span><span class="sxs-lookup"><span data-stu-id="ba585-126">For more information, see [Supported Media Formats in Media Foundation](supported-media-formats-in-media-foundation.md).</span></span>

## <a name="hardware-device-support"></a><span data-ttu-id="ba585-127">硬體裝置支援</span><span class="sxs-lookup"><span data-stu-id="ba585-127">Hardware Device Support</span></span>

<span data-ttu-id="ba585-128">媒體基礎現在支援音訊/影片管線中的下列硬體裝置類型：</span><span class="sxs-lookup"><span data-stu-id="ba585-128">Media Foundation now supports the following types of hardware devices in the audio/video pipeline:</span></span>

-   <span data-ttu-id="ba585-129">UVC 1.1 影片捕獲裝置，例如網路攝影機</span><span class="sxs-lookup"><span data-stu-id="ba585-129">UVC 1.1 video capture devices, such as webcams</span></span>
-   <span data-ttu-id="ba585-130">音訊捕獲裝置</span><span class="sxs-lookup"><span data-stu-id="ba585-130">Audio capture devices</span></span>
-   <span data-ttu-id="ba585-131">硬體編碼器和解碼器</span><span class="sxs-lookup"><span data-stu-id="ba585-131">Hardware encoders and decoders</span></span>
-   <span data-ttu-id="ba585-132">硬體視頻處理器，例如色彩空間轉換器</span><span class="sxs-lookup"><span data-stu-id="ba585-132">Hardware video processors, such as color-space converters</span></span>

<span data-ttu-id="ba585-133">硬體編解碼器可以執行非常快速的影片轉碼。</span><span class="sxs-lookup"><span data-stu-id="ba585-133">Hardware codecs can perform very fast video transcoding.</span></span> <span data-ttu-id="ba585-134">例如，應用程式可能會將 Windows Media 視訊 (WMV) 檔傳送到只支援3GP 檔案的行動電話。</span><span class="sxs-lookup"><span data-stu-id="ba585-134">For example, an application might transfer Windows Media Video (WMV) files to a cell phone that supports only 3GP files.</span></span> <span data-ttu-id="ba585-135">使用硬體編碼器，應用程式可以在將檔案傳送到裝置之前，在 backgound 中轉碼該檔案。</span><span class="sxs-lookup"><span data-stu-id="ba585-135">Using a hardware encoder, the application can transcode the file in the backgound, just before transferring it to the device.</span></span>

<span data-ttu-id="ba585-136">硬體裝置會以 proxy 物件媒體基礎表示，並在管線中使用，就像以軟體為基礎的元件一樣。</span><span class="sxs-lookup"><span data-stu-id="ba585-136">Hardware devices are represented in Media Foundation by a proxy object, and are used in the pipeline just like software-based components.</span></span>

## <a name="simplified-programming-model"></a><span data-ttu-id="ba585-137">簡化的程式設計模型</span><span class="sxs-lookup"><span data-stu-id="ba585-137">Simplified Programming Model</span></span>

<span data-ttu-id="ba585-138">在 Windows Vista 中，媒體基礎公開一組相對較低層級的 Api。</span><span class="sxs-lookup"><span data-stu-id="ba585-138">In Windows Vista, Media Foundation exposed a relatively low-level set of APIs.</span></span> <span data-ttu-id="ba585-139">這些 Api 很有彈性，但對簡單的工作來說太複雜。</span><span class="sxs-lookup"><span data-stu-id="ba585-139">These APIs are flexible, but too complex for simple tasks.</span></span> <span data-ttu-id="ba585-140">Windows 7 新增了高階 Api，可讓您更輕鬆地以 c + + 撰寫媒體應用程式。</span><span class="sxs-lookup"><span data-stu-id="ba585-140">Windows 7 adds new high-level APIs that make it simpler to write media applications in C++.</span></span> <span data-ttu-id="ba585-141">這些新的高層級 Api 包括下列各項。</span><span class="sxs-lookup"><span data-stu-id="ba585-141">These new high-level APIs include the following.</span></span>



| <span data-ttu-id="ba585-142">API</span><span class="sxs-lookup"><span data-stu-id="ba585-142">API</span></span>                                | <span data-ttu-id="ba585-143">描述</span><span class="sxs-lookup"><span data-stu-id="ba585-143">Description</span></span>                                                                                                                                                                                                                                                                                                    |
|------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ba585-144">來源讀取程式</span><span class="sxs-lookup"><span data-stu-id="ba585-144">Source Reader</span></span>](source-reader.md) | <span data-ttu-id="ba585-145">來源讀取器會從媒體檔案提取原始或解碼的資料。</span><span class="sxs-lookup"><span data-stu-id="ba585-145">The source reader pulls raw or decoded data from a media file.</span></span> <span data-ttu-id="ba585-146">例如，您可以使用來源讀取器從影片檔案取得縮圖點陣圖，或分析音訊檔案中的波形資料。</span><span class="sxs-lookup"><span data-stu-id="ba585-146">For example, you can use the source reader to get thumbnail bitmaps from a video file, or to analyze the waveform data in an audio file.</span></span> <span data-ttu-id="ba585-147">您也可以使用來源讀取器來取得音訊或影片捕獲裝置的即時資料。</span><span class="sxs-lookup"><span data-stu-id="ba585-147">You can also use the source reader to get live data from an audio or video capture device.</span></span> <br/> |
| [<span data-ttu-id="ba585-148">接收寫入器</span><span class="sxs-lookup"><span data-stu-id="ba585-148">Sink Writer</span></span>](sink-writer.md)     | <span data-ttu-id="ba585-149">接收寫入器可讓您藉由傳入未壓縮或編碼的資料來撰寫媒體檔案。</span><span class="sxs-lookup"><span data-stu-id="ba585-149">The sink writer enables you to author media files by passing in uncompressed or encoded data.</span></span> <span data-ttu-id="ba585-150">例如，您可以使用它來重新編碼影片檔案，或從網路攝影機將即時影片帶到檔案。</span><span class="sxs-lookup"><span data-stu-id="ba585-150">For example, you can use it to re-encode a video file, or to capture live video from a webcam to a file.</span></span>                                                                                                         |
| [<span data-ttu-id="ba585-151">轉碼 API</span><span class="sxs-lookup"><span data-stu-id="ba585-151">Transcode API</span></span>](transcode-api.md) | <span data-ttu-id="ba585-152">這項功能支援最常見的音訊/影片編碼案例。</span><span class="sxs-lookup"><span data-stu-id="ba585-152">This feature supports the most common audio/video encoding scenarios.</span></span><br/>                                                                                                                                                                                                                               |



 

<span data-ttu-id="ba585-153">您仍然可以在媒體基礎中使用低層級 Api。</span><span class="sxs-lookup"><span data-stu-id="ba585-153">You can still use the low-level APIs in Media Foundation.</span></span> <span data-ttu-id="ba585-154">如果您需要更充分掌控音訊/影片管線，您可能會這麼做。</span><span class="sxs-lookup"><span data-stu-id="ba585-154">You might do so if you need more control over the audio/video pipeline.</span></span>

## <a name="platform-improvements"></a><span data-ttu-id="ba585-155">平臺改善</span><span class="sxs-lookup"><span data-stu-id="ba585-155">Platform Improvements</span></span>

<span data-ttu-id="ba585-156">Windows 7 包含了許多基礎媒體基礎平臺 Api 的增強功能。</span><span class="sxs-lookup"><span data-stu-id="ba585-156">Windows 7 includes numerous enhancements to the underlying Media Foundation platform APIs.</span></span> <span data-ttu-id="ba585-157">Advanced applications 可以直接使用這些 Api;其他應用程式可以間接取得權益。</span><span class="sxs-lookup"><span data-stu-id="ba585-157">Advanced applications can use these APIs directly; other applications will get the benefits indirectly.</span></span> <span data-ttu-id="ba585-158">其改善項目包括︰</span><span class="sxs-lookup"><span data-stu-id="ba585-158">The improvements include:</span></span>

-   <span data-ttu-id="ba585-159">影片管線中的變更，可減少耗電量和視訊記憶體使用量。</span><span class="sxs-lookup"><span data-stu-id="ba585-159">Changes in the video pipeline to reduce power consumption and video memory usage.</span></span>
-   <span data-ttu-id="ba585-160">[DXVA-hd](dxva-hd.md)： Microsoft DirectX Video 加速 High DEFINITION (DXVA-hd) 是硬體加速影片處理的新 API。</span><span class="sxs-lookup"><span data-stu-id="ba585-160">[DXVA-HD](dxva-hd.md): Microsoft DirectX Video Acceleration High Definition (DXVA-HD) is a new API for hardware-accelerated video processing.</span></span> <span data-ttu-id="ba585-161">DXVA-HD 提供比先前的 DXVA 影片處理 API 更具彈性的組合模型，而且更適合用於高定義的影片格式。</span><span class="sxs-lookup"><span data-stu-id="ba585-161">DXVA-HD offers a more flexible compositing model than the previous DXVA video processing API, and is better suited for high-definition video formats..</span></span>
-   <span data-ttu-id="ba585-162">用來列舉來源和解碼器的新機制，其中包括使用值和慣用/封鎖清單。</span><span class="sxs-lookup"><span data-stu-id="ba585-162">A new mechanism for enumerating sources and decoders, which includes merit values and a preferred/blocked list.</span></span> <span data-ttu-id="ba585-163">這項功能可提升系統的整體可靠性。</span><span class="sxs-lookup"><span data-stu-id="ba585-163">This feature improves the overall reliability of the system.</span></span> <span data-ttu-id="ba585-164">如需詳細資訊，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="ba585-164">For more information, see the following topics:</span></span>
    -   [<span data-ttu-id="ba585-165">**MFTEnumEx**</span><span class="sxs-lookup"><span data-stu-id="ba585-165">**MFTEnumEx**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mftenumex)
    -   [<span data-ttu-id="ba585-166">**IMFPluginControl**</span><span class="sxs-lookup"><span data-stu-id="ba585-166">**IMFPluginControl**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfplugincontrol)
    -   [<span data-ttu-id="ba585-167">編解碼器的優點</span><span class="sxs-lookup"><span data-stu-id="ba585-167">Codec Merit</span></span>](codec-merit.md)

## <a name="sdk-changes"></a><span data-ttu-id="ba585-168">SDK 變更</span><span class="sxs-lookup"><span data-stu-id="ba585-168">SDK Changes</span></span>

-   <span data-ttu-id="ba585-169">新的標頭和程式庫檔案： [媒體基礎的標頭和程式庫](media-foundation-headers-and-libraries.md)</span><span class="sxs-lookup"><span data-stu-id="ba585-169">New headers and library files: [Media Foundation Headers and Libraries](media-foundation-headers-and-libraries.md)</span></span>
-   <span data-ttu-id="ba585-170">DLL 和 .lib 變更： [Windows 7 中的程式庫變更](media-foundation-headers-and-libraries.md)</span><span class="sxs-lookup"><span data-stu-id="ba585-170">DLL and .lib changes: [Library Changes in Windows 7](media-foundation-headers-and-libraries.md)</span></span>
-   <span data-ttu-id="ba585-171">新的 SDK 範例：</span><span class="sxs-lookup"><span data-stu-id="ba585-171">New SDK Samples:</span></span>
    -   [<span data-ttu-id="ba585-172">音訊剪輯範例</span><span class="sxs-lookup"><span data-stu-id="ba585-172">Audio Clip Sample</span></span>](audio-clip-sample.md)
    -   [<span data-ttu-id="ba585-173">DXVA-HD 範例</span><span class="sxs-lookup"><span data-stu-id="ba585-173">DXVA-HD Sample</span></span>](dxva-hd-sample.md)
    -   [<span data-ttu-id="ba585-174">MFCaptureD3D 範例</span><span class="sxs-lookup"><span data-stu-id="ba585-174">MFCaptureD3D Sample</span></span>](mfcaptured3d-sample.md)
    -   [<span data-ttu-id="ba585-175">MFCaptureToFile 範例</span><span class="sxs-lookup"><span data-stu-id="ba585-175">MFCaptureToFile Sample</span></span>](mfcapturetofile-sample.md)
    -   [<span data-ttu-id="ba585-176">轉碼範例</span><span class="sxs-lookup"><span data-stu-id="ba585-176">Transcode Sample</span></span>](transcode-sample.md)
    -   [<span data-ttu-id="ba585-177">VideoThumbnail 範例</span><span class="sxs-lookup"><span data-stu-id="ba585-177">VideoThumbnail Sample</span></span>](videothumbnail-sample.md)
-   <span data-ttu-id="ba585-178">[TopoEdit](topoedit.md)的改善：</span><span class="sxs-lookup"><span data-stu-id="ba585-178">Improvements to [TopoEdit](topoedit.md):</span></span>
    -   <span data-ttu-id="ba585-179">支援轉碼。</span><span class="sxs-lookup"><span data-stu-id="ba585-179">Support for transcoding.</span></span> <span data-ttu-id="ba585-180">請參閱 [使用 TopoEdit 建立轉碼拓撲](building-a-transcode-topology-with-topoedit.md)。</span><span class="sxs-lookup"><span data-stu-id="ba585-180">See Building a [Transcode Topology with TopoEdit](building-a-transcode-topology-with-topoedit.md).</span></span>
    -   <span data-ttu-id="ba585-181">支援音訊和影片捕捉。</span><span class="sxs-lookup"><span data-stu-id="ba585-181">Support for audio and video capture.</span></span> <span data-ttu-id="ba585-182">請參閱 [ [拓撲] 功能表](topology-menu.md)。</span><span class="sxs-lookup"><span data-stu-id="ba585-182">See [Topology Menu](topology-menu.md).</span></span>

## <a name="new-in-windows-8"></a><span data-ttu-id="ba585-183">Windows 8 的新功能</span><span class="sxs-lookup"><span data-stu-id="ba585-183">New in Windows 8</span></span>

<span data-ttu-id="ba585-184">使用 Windows 8 媒體基礎的一些新更新包括：</span><span class="sxs-lookup"><span data-stu-id="ba585-184">Some of the new updates to Media Foundation with Windows 8 are:</span></span>

-   <span data-ttu-id="ba585-185">[**IMFCaptureEngine**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcaptureengine)會控制一或多個 capture 裝置。</span><span class="sxs-lookup"><span data-stu-id="ba585-185">The [**IMFCaptureEngine**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcaptureengine) controls one or more capture devices.</span></span> <span data-ttu-id="ba585-186">如需屬性清單，請參閱「 [捕獲引擎」屬性](capture-engine-attributes.md) 。</span><span class="sxs-lookup"><span data-stu-id="ba585-186">See the [Capture Engine Attributes](capture-engine-attributes.md) for a list of attributes.</span></span> <span data-ttu-id="ba585-187">其他新的 media capture 相關介面為 [**IMFCapturePhotoSink**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturephotosink)、 [**IMFCapturePreviewSink**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturepreviewsink)、 [**IMFCaptureRecordSink**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturerecordsink)、 [**IMFCaptureSink**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturesink)和 [**IMFCaptureSource**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturesource)。</span><span class="sxs-lookup"><span data-stu-id="ba585-187">Other new media capture related interfaces are [**IMFCapturePhotoSink**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturephotosink), [**IMFCapturePreviewSink**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturepreviewsink), [**IMFCaptureRecordSink**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturerecordsink), [**IMFCaptureSink**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturesink), and [**IMFCaptureSource**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturesource).</span></span>
-   <span data-ttu-id="ba585-188">下列媒體基礎類別延伸模組是 Windows 8 的新功能：</span><span class="sxs-lookup"><span data-stu-id="ba585-188">The following Media Foundation class extensions are new for Windows 8:</span></span>
    -   [<span data-ttu-id="ba585-189">**IMFMediaEngineEx**</span><span class="sxs-lookup"><span data-stu-id="ba585-189">**IMFMediaEngineEx**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineex)
    -   [<span data-ttu-id="ba585-190">**IMFMediaSourceEx**</span><span class="sxs-lookup"><span data-stu-id="ba585-190">**IMFMediaSourceEx**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex)
    -   [<span data-ttu-id="ba585-191">**IMFRealTimeClientEx**</span><span class="sxs-lookup"><span data-stu-id="ba585-191">**IMFRealTimeClientEx**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclientex)
    -   [<span data-ttu-id="ba585-192">**IMFSinkWriterEx**</span><span class="sxs-lookup"><span data-stu-id="ba585-192">**IMFSinkWriterEx**</span></span>](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwriterex)
    -   [<span data-ttu-id="ba585-193">**IMFSourceReaderEx**</span><span class="sxs-lookup"><span data-stu-id="ba585-193">**IMFSourceReaderEx**</span></span>](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereaderex)
    -   [<span data-ttu-id="ba585-194">**IMFVideoSampleAllocatorEx**</span><span class="sxs-lookup"><span data-stu-id="ba585-194">**IMFVideoSampleAllocatorEx**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocatorex)
    -   [<span data-ttu-id="ba585-195">**IMFWorkQueueServicesEx**</span><span class="sxs-lookup"><span data-stu-id="ba585-195">**IMFWorkQueueServicesEx**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservicesex)
-   <span data-ttu-id="ba585-196">[Direct3D 11 VIDEO API](direct3d-11-video-apis.md) 是 Windows 8 的新。</span><span class="sxs-lookup"><span data-stu-id="ba585-196">[Direct3D 11 Video API](direct3d-11-video-apis.md) are new for Windows 8.</span></span> <span data-ttu-id="ba585-197">Windows 8 桌面應用程式仍然可以使用 [direct3d 9 VIDEO api](direct3d-video-apis.md)，但 Windows Store 應用程式必須使用新的 Direct3d 11 video api。</span><span class="sxs-lookup"><span data-stu-id="ba585-197">Windows 8 Desktop apps can still use [Direct3D 9 Video API](direct3d-video-apis.md), but Windows Store apps must use the new Direct3D 11 Video API.</span></span> <span data-ttu-id="ba585-198">如需有關 Microsoft Direct3D 11 Video 的詳細資訊，請參閱 [媒體基礎中的支援 Direct3D 11 影片解碼](supporting-direct3d-11-video-decoding-in-media-foundation.md)。</span><span class="sxs-lookup"><span data-stu-id="ba585-198">For info more info on Microsoft Direct3D 11 Video see [Supporting Direct3D 11 Video Decoding in Media Foundation](supporting-direct3d-11-video-decoding-in-media-foundation.md).</span></span>
-   <span data-ttu-id="ba585-199">媒體基礎工作佇列已有更新和改進。</span><span class="sxs-lookup"><span data-stu-id="ba585-199">There have been updates and improvements to Media Foundation work queues.</span></span> <span data-ttu-id="ba585-200">如需詳細資訊，請參閱 [工作佇列和執行緒改善](media-foundation-work-queue-and-threading-improvements.md) 。</span><span class="sxs-lookup"><span data-stu-id="ba585-200">See [Work Queue and Threading Improvements](media-foundation-work-queue-and-threading-improvements.md) for more info.</span></span>
-   <span data-ttu-id="ba585-201">H.264 [UVC 1.5 攝影機編碼器](camera-encoder-h264-uvc-1-5.md)。</span><span class="sxs-lookup"><span data-stu-id="ba585-201">[H.264 UVC 1.5 camera encoders](camera-encoder-h264-uvc-1-5.md).</span></span>
-   <span data-ttu-id="ba585-202">如需可搭配 Windows Store 應用程式使用媒體基礎 API 的清單，請參閱 [適用于 Windows store 應用程式的 Win32 和 COM (多媒體) ](media-foundation-headers-and-libraries.md)。</span><span class="sxs-lookup"><span data-stu-id="ba585-202">For a list of the Media Foundation API which can be used with Windows Store apps see [Win32 and COM for Windows Store apps (multimedia)](media-foundation-headers-and-libraries.md).</span></span>
-   <span data-ttu-id="ba585-203">媒體基礎不包含在 Windows 8 的 N 和 KN 版本中。</span><span class="sxs-lookup"><span data-stu-id="ba585-203">Media Foundation is not included with the N and KN editions of Windows 8.</span></span> <span data-ttu-id="ba585-204">如需詳細資訊，請參閱 [Microsoft Windows Media Feature Pack 的 N 和 KN 版本的所有 Windows 8 版本](https://support.microsoft.com/kb/2703761)。</span><span class="sxs-lookup"><span data-stu-id="ba585-204">For more information, see [Microsoft Windows Media Feature Pack for N and KN Versions of all Windows 8 Editions](https://support.microsoft.com/kb/2703761).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ba585-205">相關主題</span><span class="sxs-lookup"><span data-stu-id="ba585-205">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ba585-206">關於媒體基礎</span><span class="sxs-lookup"><span data-stu-id="ba585-206">About Media Foundation</span></span>](about-the-media-foundation-sdk.md)
</dt> <dt>

[<span data-ttu-id="ba585-207">Microsoft 媒體基礎</span><span class="sxs-lookup"><span data-stu-id="ba585-207">Microsoft Media Foundation</span></span>](microsoft-media-foundation-sdk.md)
</dt> </dl>

 

 




