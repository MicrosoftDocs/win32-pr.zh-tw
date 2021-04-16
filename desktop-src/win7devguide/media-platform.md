---
title: 媒體平臺
description: 媒體基礎和 DirectShow 在 Windows 中提供媒體支援的基礎。
ms.assetid: 020f009c-7432-432b-a39b-9295dd784d2e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71f756112384451ac3f5b4055d73a60a170b2e29
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104508095"
---
# <a name="media-platform"></a><span data-ttu-id="f0012-103">媒體平臺</span><span class="sxs-lookup"><span data-stu-id="f0012-103">Media Platform</span></span>

<span data-ttu-id="f0012-104">[媒體基礎](/windows/desktop/medfound/microsoft-media-foundation-sdk) 和 [DirectShow](/windows/desktop/DirectShow/directshow) 在 Windows 中提供媒體支援的基礎。</span><span class="sxs-lookup"><span data-stu-id="f0012-104">[Media Foundation](/windows/desktop/medfound/microsoft-media-foundation-sdk) and [DirectShow](/windows/desktop/DirectShow/directshow) provide the basis for media support in Windows.</span></span> <span data-ttu-id="f0012-105">媒體基礎是在 Windows Vista 中引進，作為 DirectShow 的取代。</span><span class="sxs-lookup"><span data-stu-id="f0012-105">Media Foundation was introduced in Windows Vista as the replacement for DirectShow.</span></span> <span data-ttu-id="f0012-106">在 Windows 7 中，已增強媒體基礎，以提供更好的格式支援，包括 *MPEG 4*，以及支援影片捕獲裝置和硬體編解碼器。</span><span class="sxs-lookup"><span data-stu-id="f0012-106">In Windows 7, Media Foundation has been enhanced to provide better format support, including *MPEG-4*, as well as support for video capture devices and hardware codecs.</span></span>

## <a name="format-support"></a><span data-ttu-id="f0012-107">格式支援</span><span class="sxs-lookup"><span data-stu-id="f0012-107">Format Support</span></span>

<span data-ttu-id="f0012-108">在 Windows 7 中，[媒體基礎](/windows/desktop/medfound/microsoft-media-foundation-sdk)提供廣泛的格式支援，其中包括 *H.264 video、* *MJPEG* 和 *MP3* 的編解碼器;新 *3GP*、 *AAC* 音訊和 *AVI\*\*的來源*;*以及新的檔案* 接收、 *3GP* 和 *MP3*。</span><span class="sxs-lookup"><span data-stu-id="f0012-108">In Windows 7, [Media Foundation](/windows/desktop/medfound/microsoft-media-foundation-sdk) provides extensive format support that includes codecs for *H.264* video, *MJPEG*, and *MP3*; new sources for *MP4*, *3GP*, *AAC* audio, and *AVI*; and new file sinks for *MP4*, *3GP*, and *MP3*.</span></span> <span data-ttu-id="f0012-109"> ([在媒體基礎中查看支援的媒體格式](../medfound/supported-media-formats-in-media-foundation.md)。 ) </span><span class="sxs-lookup"><span data-stu-id="f0012-109">(See [Supported Media Formats in Media Foundation](../medfound/supported-media-formats-in-media-foundation.md).)</span></span>

## <a name="hardware-devices"></a><span data-ttu-id="f0012-110">硬體裝置</span><span class="sxs-lookup"><span data-stu-id="f0012-110">Hardware Devices</span></span>

<span data-ttu-id="f0012-111">[媒體基礎](/windows/desktop/medfound/microsoft-media-foundation-sdk) 現在支援音訊/影片管線中的下列硬體裝置類型：</span><span class="sxs-lookup"><span data-stu-id="f0012-111">[Media Foundation](/windows/desktop/medfound/microsoft-media-foundation-sdk) now supports the following types of hardware devices in the audio/video pipeline:</span></span>

-   <span data-ttu-id="f0012-112">*UVC 1.1* 影片捕獲裝置，例如網路攝影機</span><span class="sxs-lookup"><span data-stu-id="f0012-112">*UVC 1.1* video capture devices, such as webcams</span></span>
-   <span data-ttu-id="f0012-113">音訊捕獲裝置</span><span class="sxs-lookup"><span data-stu-id="f0012-113">Audio capture devices</span></span>
-   <span data-ttu-id="f0012-114">硬體編碼器和解碼器</span><span class="sxs-lookup"><span data-stu-id="f0012-114">Hardware encoders and decoders</span></span>
-   <span data-ttu-id="f0012-115">硬體視頻處理器，例如色彩空間轉換器</span><span class="sxs-lookup"><span data-stu-id="f0012-115">Hardware video processors, such as color-space converters</span></span>

<span data-ttu-id="f0012-116">硬體編解碼器可以執行非常快速的影片轉碼。</span><span class="sxs-lookup"><span data-stu-id="f0012-116">Hardware codecs can perform very fast video transcoding.</span></span> <span data-ttu-id="f0012-117">例如，假設您想要將 *Windows Media 視訊 (WMV)* 檔傳送到只支援 *3GP* 檔案的行動電話。</span><span class="sxs-lookup"><span data-stu-id="f0012-117">For example, suppose you want to transfer a *Windows Media Video (WMV)* file to a cell phone that supports only *3GP* files.</span></span> <span data-ttu-id="f0012-118">使用硬體編碼器時，可以在將檔案傳送到裝置之前，立即轉碼檔案。</span><span class="sxs-lookup"><span data-stu-id="f0012-118">With a hardware encoder, the file can be transcoded "as needed," immediately before transferring it to the device.</span></span>

<span data-ttu-id="f0012-119">硬體裝置會以 proxy 物件 [媒體基礎](/windows/desktop/medfound/microsoft-media-foundation-sdk) 表示，並在管線中使用，就像以軟體為基礎的元件一樣。</span><span class="sxs-lookup"><span data-stu-id="f0012-119">Hardware devices are represented in [Media Foundation](/windows/desktop/medfound/microsoft-media-foundation-sdk) by a proxy object, and are used in the pipeline just like software-based components.</span></span> <span data-ttu-id="f0012-120"> (請參閱 [媒體基礎的新功能](../medfound/whats-new-for-media-foundation.md)。 ) </span><span class="sxs-lookup"><span data-stu-id="f0012-120">(See [What's New for Media Foundation](../medfound/whats-new-for-media-foundation.md).)</span></span>

## <a name="simplified-programming-model"></a><span data-ttu-id="f0012-121">簡化的程式設計模型</span><span class="sxs-lookup"><span data-stu-id="f0012-121">Simplified Programming Model</span></span>

<span data-ttu-id="f0012-122">在 Windows Vista 中， [媒體基礎](/windows/desktop/medfound/microsoft-media-foundation-sdk) 公開一組相對較低層級的 api。</span><span class="sxs-lookup"><span data-stu-id="f0012-122">In Windows Vista, [Media Foundation](/windows/desktop/medfound/microsoft-media-foundation-sdk) exposed a relatively low-level set of APIs.</span></span> <span data-ttu-id="f0012-123">這些 Api 很有彈性，但可能不適合用來執行工作。</span><span class="sxs-lookup"><span data-stu-id="f0012-123">These APIs are flexible, but may not be appropriate for performing tasks.</span></span> <span data-ttu-id="f0012-124">Windows 7 新增了高階 Api，可讓您更輕鬆地以 *c + +* 撰寫媒體應用程式。</span><span class="sxs-lookup"><span data-stu-id="f0012-124">Windows 7 adds new high-level APIs that make it simpler to write media applications in *C++*.</span></span> <span data-ttu-id="f0012-125">這些新的高層級 Api 包括：</span><span class="sxs-lookup"><span data-stu-id="f0012-125">These new high-level APIs include:</span></span>

-   <span data-ttu-id="f0012-126">**MFPlay**。</span><span class="sxs-lookup"><span data-stu-id="f0012-126">**MFPlay**.</span></span> <span data-ttu-id="f0012-127">這些 Api 是針對音訊和影片播放所設計。</span><span class="sxs-lookup"><span data-stu-id="f0012-127">These APIs are designed for audio and video playback.</span></span> <span data-ttu-id="f0012-128">它們支援一般的播放作業 (停止、暫停、播放、搜尋、速率控制、音訊音量等等) ，同時隱藏低層級 Api 的詳細資料 (會話和拓撲層) 。</span><span class="sxs-lookup"><span data-stu-id="f0012-128">They support the typical playback operations (stop, pause, play, seek, rate control, audio volume, and so forth), while hiding the details of the low-level APIs (the session and topology layers).</span></span>
-   <span data-ttu-id="f0012-129">**來源讀取器**。</span><span class="sxs-lookup"><span data-stu-id="f0012-129">**Source Reader**.</span></span> <span data-ttu-id="f0012-130">您可以使用這些 Api 從媒體檔案提取未經處理或解碼的資料，而不需要知道任何關於基礎格式的資訊。</span><span class="sxs-lookup"><span data-stu-id="f0012-130">You can use these APIs to pull raw or decoded data from a media file, without knowing anything about the underlying format.</span></span> <span data-ttu-id="f0012-131">例如，您可以從影片檔案取得縮圖點陣圖，或從網路攝影機取得實況影片畫面。</span><span class="sxs-lookup"><span data-stu-id="f0012-131">For example, you can get a thumbnail bitmap from a video file or get live video frames from a webcam.</span></span>
-   <span data-ttu-id="f0012-132">**接收寫入器**。</span><span class="sxs-lookup"><span data-stu-id="f0012-132">**Sink Writer**.</span></span> <span data-ttu-id="f0012-133">您可以使用這些 Api，藉由傳入未壓縮或編碼的資料來撰寫媒體檔案。</span><span class="sxs-lookup"><span data-stu-id="f0012-133">You can use these APIs to author media files by passing in uncompressed or encoded data.</span></span> <span data-ttu-id="f0012-134">例如，您可以重新編碼或 remix 影片檔案。</span><span class="sxs-lookup"><span data-stu-id="f0012-134">For example, you can re-encode or remix a video file.</span></span>
-   <span data-ttu-id="f0012-135">**轉碼**。</span><span class="sxs-lookup"><span data-stu-id="f0012-135">**Transcode**.</span></span> <span data-ttu-id="f0012-136">這些 Api 會以最常見的音訊和影片編碼案例為目標。</span><span class="sxs-lookup"><span data-stu-id="f0012-136">These APIs target the most common audio and video encoding scenarios.</span></span>

## <a name="platform-improvements"></a><span data-ttu-id="f0012-137">平臺改善</span><span class="sxs-lookup"><span data-stu-id="f0012-137">Platform Improvements</span></span>

<span data-ttu-id="f0012-138">Windows 7 包含了許多基礎 [媒體基礎](/windows/desktop/medfound/microsoft-media-foundation-sdk) 平臺 api 的增強功能。</span><span class="sxs-lookup"><span data-stu-id="f0012-138">Windows 7 includes numerous enhancements to the underlying [Media Foundation](/windows/desktop/medfound/microsoft-media-foundation-sdk) platform APIs.</span></span> <span data-ttu-id="f0012-139">Advanced applications 可以直接使用這些 Api;其他應用程式可以間接取得權益。</span><span class="sxs-lookup"><span data-stu-id="f0012-139">Advanced applications can use these APIs directly; other applications will get the benefits indirectly.</span></span> <span data-ttu-id="f0012-140">這些優點包括：</span><span class="sxs-lookup"><span data-stu-id="f0012-140">These benefits include:</span></span>

-   <span data-ttu-id="f0012-141">影片管線中的增強功能，可減少耗電量和視訊記憶體使用量。</span><span class="sxs-lookup"><span data-stu-id="f0012-141">Improvements in the video pipeline to reduce power consumption and video memory usage.</span></span>
-   <span data-ttu-id="f0012-142">新的 *DVXA* 影片處理 api，其使用更具彈性的撰寫模型，且更適合 *HD* 影片格式。</span><span class="sxs-lookup"><span data-stu-id="f0012-142">New *DVXA* video processing APIs, which use a more flexible compositing model and are better suited for *HD* video formats.</span></span>
-   <span data-ttu-id="f0012-143">改進了外掛程式 (來源和解碼器) 的列舉與管理方式。</span><span class="sxs-lookup"><span data-stu-id="f0012-143">Improvements to the way in which plug-ins (sources and decoders) are enumerated and managed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f0012-144">相關主題</span><span class="sxs-lookup"><span data-stu-id="f0012-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f0012-145">媒體基礎的新功能</span><span class="sxs-lookup"><span data-stu-id="f0012-145">What's New for Media Foundation</span></span>](../medfound/whats-new-for-media-foundation.md)
</dt> </dl>

 

 