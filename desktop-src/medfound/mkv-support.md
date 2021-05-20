---
description: 本節說明 Matroska Media Container (.MKV) 檔的媒體基礎支援。
title: Matroska Media Container (.MKV) 支援
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdd860f58087bc8a0f3fe95d278bfa81edc412d0
ms.sourcegitcommit: 88049609e29f91a42442235885abf56f598b06b3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/19/2021
ms.locfileid: "110154211"
---
# <a name="matroska-media-container-mkv-support"></a><span data-ttu-id="6ba58-103">Matroska Media Container (.MKV) 支援</span><span class="sxs-lookup"><span data-stu-id="6ba58-103">Matroska Media Container (MKV) support</span></span>

<span data-ttu-id="6ba58-104">本節說明 Matroska Media Container (.MKV) 檔的媒體基礎支援。</span><span class="sxs-lookup"><span data-stu-id="6ba58-104">This section describes the Media Foundation support for Matroska Media Container (MKV) files.</span></span>

<span data-ttu-id="6ba58-105">.MKV 格式可支援多種影片和音訊編解碼器，例如 h.264 和 AAC 音訊。</span><span class="sxs-lookup"><span data-stu-id="6ba58-105">The MKV format can support multiple video and audio codecs, such as H.264 and AAC audio.</span></span> <span data-ttu-id="6ba58-106">一般而言，容器會描述影片和音訊資料的配置方式，以及用來描述這些 A/V 串流的補充資訊。</span><span class="sxs-lookup"><span data-stu-id="6ba58-106">In general, containers describe how video and audio data is laid out and what supplementary information is used to describe those A/V streams.</span></span> <span data-ttu-id="6ba58-107">容器也可以包含輔助/V 資料流程的資料，例如標題、音訊串流的語言、副標題或字幕軌、這些字幕的字型、影像、章節資訊和功能表。</span><span class="sxs-lookup"><span data-stu-id="6ba58-107">Containers can also include data that complements A/V streams, such as the title, languages of the audio streams, subtitle or caption tracks, fonts for those subtitles, images, chapter information, and menus.</span></span> <span data-ttu-id="6ba58-108">.MKV 是高度彈性的格式，可支援許多容器功能。</span><span class="sxs-lookup"><span data-stu-id="6ba58-108">MKV is a highly flexible format that supports many of these container features.</span></span> <span data-ttu-id="6ba58-109">如需 .MKV 格式的詳細資訊，請參閱。 [https://matroska.org](https://matroska.org/)</span><span class="sxs-lookup"><span data-stu-id="6ba58-109">For more info about the MKV format, see [https://matroska.org](https://matroska.org/)</span></span>


## <a name="mkv-container-feature-support"></a><span data-ttu-id="6ba58-110">.MKV 容器功能支援</span><span class="sxs-lookup"><span data-stu-id="6ba58-110">MKV container feature support</span></span>
<span data-ttu-id="6ba58-111">媒體基礎的 .MKV 容器功能可透過下列方式在中受到支援：</span><span class="sxs-lookup"><span data-stu-id="6ba58-111">MKV container features are supported on the by Media Foundation in the following ways:</span></span>
- <span data-ttu-id="6ba58-112">如果有一或多個影片曲目，將會播放第一個曲目。</span><span class="sxs-lookup"><span data-stu-id="6ba58-112">If one or more video tracks are present, the first track will be played.</span></span>
- <span data-ttu-id="6ba58-113">如果有一或多個音訊曲目，將會播放第一個曲目。</span><span class="sxs-lookup"><span data-stu-id="6ba58-113">If one or more audio tracks are present, the first track will be played.</span></span>
- <span data-ttu-id="6ba58-114">支援字幕軌，但預設 (播放) 則不會選取這些字幕。</span><span class="sxs-lookup"><span data-stu-id="6ba58-114">Caption tracks are supported, but are not selected (played) by default.</span></span>
- <span data-ttu-id="6ba58-115">如果有一或多個字型或影像，則不會轉譯字幕和影像，雖然檔案將會載入並播放。</span><span class="sxs-lookup"><span data-stu-id="6ba58-115">If one or more fonts or images are present, captions and images won’t render, although the file will load and play.</span></span>
- <span data-ttu-id="6ba58-116">不支援且不會顯示功能表資訊，但會載入並播放檔案。</span><span class="sxs-lookup"><span data-stu-id="6ba58-116">Menu information is not supported and won’t be displayed, but the file will load and play.</span></span>
- <span data-ttu-id="6ba58-117">如果有章節的檔案參考補充檔案，則補充檔案將不會播放。</span><span class="sxs-lookup"><span data-stu-id="6ba58-117">If files with chapters refer to supplemental files, the supplemental files won’t play.</span></span>
- <span data-ttu-id="6ba58-118">使用檔案瀏覽器流覽 USB 磁片磁碟機上的檔案時，可以使用縮圖影像。</span><span class="sxs-lookup"><span data-stu-id="6ba58-118">Thumbnail images are available when browsing for files on USB drives using the file browser.</span></span>

<span data-ttu-id="6ba58-119">如果包含支援的編解碼器，這組功能應該允許播放大部分的 .MKV 檔案。</span><span class="sxs-lookup"><span data-stu-id="6ba58-119">This set of features should allow playback of most MKV files if they contain supported codecs.</span></span>
<span data-ttu-id="6ba58-120">支援包含以下節所列編解碼器編碼之影片和音訊播放軌的 .MKV 檔案。</span><span class="sxs-lookup"><span data-stu-id="6ba58-120">MKV files that contain video and audio tracks encoded with the codecs listed in the following section are supported.</span></span>

## <a name="supported-mkv-codecs"></a><span data-ttu-id="6ba58-121">支援的 .MKV 編解碼器</span><span class="sxs-lookup"><span data-stu-id="6ba58-121">Supported MKV codecs</span></span>

### <a name="video-codec-support-for-mkv"></a><span data-ttu-id="6ba58-122">.MKV 的影片編解碼器支援</span><span class="sxs-lookup"><span data-stu-id="6ba58-122">Video codec support for MKV</span></span>

<span data-ttu-id="6ba58-123">Matroska 識別碼： V_MPEG4/ISO/AVC</span><span class="sxs-lookup"><span data-stu-id="6ba58-123">Matroska ID: V_MPEG4/ISO/AVC</span></span>

- <span data-ttu-id="6ba58-124">MSFT 媒體基礎 MF_MT_SUBTYPE： MFVideoFormat_H264</span><span class="sxs-lookup"><span data-stu-id="6ba58-124">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_H264</span></span>
- <span data-ttu-id="6ba58-125">描述： h.264 影片</span><span class="sxs-lookup"><span data-stu-id="6ba58-125">Description: H.264 video</span></span>
- <span data-ttu-id="6ba58-126">FourCC 或 WAV 識別碼： H264</span><span class="sxs-lookup"><span data-stu-id="6ba58-126">FourCC or WAV identifiers: H264</span></span>

<span data-ttu-id="6ba58-127">Matroska 識別碼： V_MPEG2</span><span class="sxs-lookup"><span data-stu-id="6ba58-127">Matroska ID: V_MPEG2</span></span>

- <span data-ttu-id="6ba58-128">MSFT 媒體基礎 MF_MT_SUBTYPE： MFVideoFormat_MPEG2</span><span class="sxs-lookup"><span data-stu-id="6ba58-128">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_MPEG2</span></span>
- <span data-ttu-id="6ba58-129">描述： MPEG-2 影片</span><span class="sxs-lookup"><span data-stu-id="6ba58-129">Description: MPEG-2 video</span></span>

<span data-ttu-id="6ba58-130">Matroska 識別碼： V_MPEG1</span><span class="sxs-lookup"><span data-stu-id="6ba58-130">Matroska ID: V_MPEG1</span></span>

- <span data-ttu-id="6ba58-131">MSFT 媒體基礎 MF_MT_SUBTYPE： MFVideoFormat_MPG1</span><span class="sxs-lookup"><span data-stu-id="6ba58-131">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_MPG1</span></span>
- <span data-ttu-id="6ba58-132">描述： MPEG 1 影片</span><span class="sxs-lookup"><span data-stu-id="6ba58-132">Description: MPEG-1 video</span></span>
- <span data-ttu-id="6ba58-133">FourCC 或 WAV 識別碼： MPG1</span><span class="sxs-lookup"><span data-stu-id="6ba58-133">FourCC or WAV identifiers: MPG1</span></span>

<span data-ttu-id="6ba58-134">Matroska 識別碼： V_MPEG4/MS/V3</span><span class="sxs-lookup"><span data-stu-id="6ba58-134">Matroska ID: V_MPEG4/MS/V3</span></span>

- <span data-ttu-id="6ba58-135">MSFT 媒體基礎 MF_MT_SUBTYPE： MFVideoFormat_MP43</span><span class="sxs-lookup"><span data-stu-id="6ba58-135">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_MP43</span></span>
- <span data-ttu-id="6ba58-136">描述： Microsoft MPEG 4 編解碼器第3版</span><span class="sxs-lookup"><span data-stu-id="6ba58-136">Description: Microsoft MPEG 4 codec version 3</span></span>
- <span data-ttu-id="6ba58-137">FourCC 或 WAV 識別碼： MP43</span><span class="sxs-lookup"><span data-stu-id="6ba58-137">FourCC or WAV identifiers: MP43</span></span>

<span data-ttu-id="6ba58-138">Matroska 識別碼： V_MPEG4/ISO/ASP</span><span class="sxs-lookup"><span data-stu-id="6ba58-138">Matroska ID: V_MPEG4/ISO/ASP</span></span>

- <span data-ttu-id="6ba58-139">MSFT 媒體基礎 MF_MT_SUBTYPE： MFVideoFormat_MP4V</span><span class="sxs-lookup"><span data-stu-id="6ba58-139">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_MP4V</span></span>
- <span data-ttu-id="6ba58-140">描述： MPEG 4 第2部分影片</span><span class="sxs-lookup"><span data-stu-id="6ba58-140">Description: MPEG-4 part 2 video</span></span>
- <span data-ttu-id="6ba58-141">FourCC 或 WAV 識別碼： MP4V</span><span class="sxs-lookup"><span data-stu-id="6ba58-141">FourCC or WAV identifiers: MP4V</span></span>

<span data-ttu-id="6ba58-142">Matroska 識別碼： V_MS/VFW/FOURCC</span><span class="sxs-lookup"><span data-stu-id="6ba58-142">Matroska ID: V_MS/VFW/FOURCC</span></span>

- <span data-ttu-id="6ba58-143">描述：對應至數個通常以可在主控台上使用的 AVI 格式支援的編解碼器。</span><span class="sxs-lookup"><span data-stu-id="6ba58-143">Description: Maps to several codecs usually supported in the AVI format that are available on the console.</span></span>

<span data-ttu-id="6ba58-144">Matroska 識別碼： V_THEORA</span><span class="sxs-lookup"><span data-stu-id="6ba58-144">Matroska ID: V_THEORA</span></span>

- <span data-ttu-id="6ba58-145">MSFT 媒體基礎 MF_MT_SUBTYPE： MFVideoFormat_Theora</span><span class="sxs-lookup"><span data-stu-id="6ba58-145">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_Theora</span></span>
- <span data-ttu-id="6ba58-146">描述： Theora</span><span class="sxs-lookup"><span data-stu-id="6ba58-146">Description: Theora</span></span>
- <span data-ttu-id="6ba58-147">FourCC 或 WAV 識別碼： theo</span><span class="sxs-lookup"><span data-stu-id="6ba58-147">FourCC or WAV identifiers: theo</span></span>

<span data-ttu-id="6ba58-148">Matroska 識別碼： V_MPEG4/ISO/SP</span><span class="sxs-lookup"><span data-stu-id="6ba58-148">Matroska ID: V_MPEG4/ISO/SP</span></span>

- <span data-ttu-id="6ba58-149">MSFT 媒體基礎 MF_MT_SUBTYPE： MFVideoFormat_MP4V</span><span class="sxs-lookup"><span data-stu-id="6ba58-149">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_MP4V</span></span>
- <span data-ttu-id="6ba58-150">描述： MPEG4 ISO 簡單設定檔 (DivX4) </span><span class="sxs-lookup"><span data-stu-id="6ba58-150">Description: MPEG4 ISO simple profile (DivX4)</span></span>
- <span data-ttu-id="6ba58-151">FourCC 或 WAV 識別碼： MP4V</span><span class="sxs-lookup"><span data-stu-id="6ba58-151">FourCC or WAV identifiers: MP4V</span></span>

<span data-ttu-id="6ba58-152">Matroska 識別碼： V_MPEG4/ISO/AP</span><span class="sxs-lookup"><span data-stu-id="6ba58-152">Matroska ID: V_MPEG4/ISO/AP</span></span>

- <span data-ttu-id="6ba58-153">MSFT 媒體基礎 MF_MT_SUBTYPE： MFVideoFormat_MP4V</span><span class="sxs-lookup"><span data-stu-id="6ba58-153">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_MP4V</span></span>
- <span data-ttu-id="6ba58-154">描述： MPEG4 ISO advanced 簡單設定檔 (DivX5、XviD、FFMPEG) </span><span class="sxs-lookup"><span data-stu-id="6ba58-154">Description: MPEG4 ISO advanced simple profile (DivX5, XviD, FFMPEG)</span></span>
- <span data-ttu-id="6ba58-155">FourCC 或 WAV 識別碼： MP4V</span><span class="sxs-lookup"><span data-stu-id="6ba58-155">FourCC or WAV identifiers: MP4V</span></span>


<span data-ttu-id="6ba58-156">Matroska 識別碼： V_MPEGH/ISO/HEVC</span><span class="sxs-lookup"><span data-stu-id="6ba58-156">Matroska ID: V_MPEGH/ISO/HEVC</span></span> 

- <span data-ttu-id="6ba58-157">MSFT 媒體基礎 MF_MT_SUBTYPE： MFVideoFormat_HEVC</span><span class="sxs-lookup"><span data-stu-id="6ba58-157">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_HEVC</span></span>
- <span data-ttu-id="6ba58-158">描述： HEVC/。H</span><span class="sxs-lookup"><span data-stu-id="6ba58-158">Description: HEVC/H.265</span></span>
- <span data-ttu-id="6ba58-159">FourCC 或 WAV 識別碼：</span><span class="sxs-lookup"><span data-stu-id="6ba58-159">FourCC or WAV identifiers:</span></span> 

<span data-ttu-id="6ba58-160">Matroska 識別碼： V_VP8</span><span class="sxs-lookup"><span data-stu-id="6ba58-160">Matroska ID: V_VP8</span></span>

- <span data-ttu-id="6ba58-161">MSFT 媒體基礎 MF_MT_SUBTYPE： MFVideoFormat_VP80</span><span class="sxs-lookup"><span data-stu-id="6ba58-161">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_VP80</span></span>
- <span data-ttu-id="6ba58-162">描述： VP8 編解碼器格式</span><span class="sxs-lookup"><span data-stu-id="6ba58-162">Description: VP8 Codec format</span></span>
- <span data-ttu-id="6ba58-163">FourCC 或 WAV 識別碼： VP80</span><span class="sxs-lookup"><span data-stu-id="6ba58-163">FourCC or WAV identifiers: VP80</span></span>

<span data-ttu-id="6ba58-164">Matroska 識別碼： V_VP9</span><span class="sxs-lookup"><span data-stu-id="6ba58-164">Matroska ID: V_VP9</span></span>

- <span data-ttu-id="6ba58-165">MSFT 媒體基礎 MF_MT_SUBTYPE： MFVideoFormat_VP90</span><span class="sxs-lookup"><span data-stu-id="6ba58-165">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_VP90</span></span>
- <span data-ttu-id="6ba58-166">描述： VP9 編解碼器格式</span><span class="sxs-lookup"><span data-stu-id="6ba58-166">Description: VP9 Codec format</span></span>
- <span data-ttu-id="6ba58-167">FourCC 或 WAV 識別碼： VP90</span><span class="sxs-lookup"><span data-stu-id="6ba58-167">FourCC or WAV identifiers: VP90</span></span>

<span data-ttu-id="6ba58-168">Matroska 識別碼： V_MJPEG</span><span class="sxs-lookup"><span data-stu-id="6ba58-168">Matroska ID: V_MJPEG</span></span>

- <span data-ttu-id="6ba58-169">MSFT 媒體基礎 MF_MT_SUBTYPE： MFVideoFormat_MJPG</span><span class="sxs-lookup"><span data-stu-id="6ba58-169">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_MJPG</span></span>
- <span data-ttu-id="6ba58-170">描述：動畫 JPEG</span><span class="sxs-lookup"><span data-stu-id="6ba58-170">Description: Motion JPEG</span></span>
- <span data-ttu-id="6ba58-171">FourCC 或 WAV 識別碼： MJPG</span><span class="sxs-lookup"><span data-stu-id="6ba58-171">FourCC or WAV identifiers: MJPG</span></span>

<span data-ttu-id="6ba58-172">Matroska 識別碼： V_AV1</span><span class="sxs-lookup"><span data-stu-id="6ba58-172">Matroska ID: V_AV1</span></span>

- <span data-ttu-id="6ba58-173">MSFT 媒體基礎 MF_MT_SUBTYPE： MFVideoFormat_AV1</span><span class="sxs-lookup"><span data-stu-id="6ba58-173">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_AV1</span></span>
- <span data-ttu-id="6ba58-174">描述： AOMedia Video 1</span><span class="sxs-lookup"><span data-stu-id="6ba58-174">Description: AOMedia Video 1</span></span>
- <span data-ttu-id="6ba58-175">FourCC 或 WAV 識別碼： AV01</span><span class="sxs-lookup"><span data-stu-id="6ba58-175">FourCC or WAV identifiers: AV01</span></span>

### <a name="audio-codec-support-for-mkv"></a><span data-ttu-id="6ba58-176">.MKV 的音訊編解碼器支援</span><span class="sxs-lookup"><span data-stu-id="6ba58-176">Audio codec support for MKV</span></span>

<span data-ttu-id="6ba58-177">Matroska 識別碼： A_AAC</span><span class="sxs-lookup"><span data-stu-id="6ba58-177">Matroska ID: A_AAC</span></span>

- <span data-ttu-id="6ba58-178">MSFT 媒體基礎 MF_MT_SUBTYPE： MFAudioFormat_AAC</span><span class="sxs-lookup"><span data-stu-id="6ba58-178">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_AAC</span></span>
- <span data-ttu-id="6ba58-179">描述： Advanced Audio 編碼 (AAC) </span><span class="sxs-lookup"><span data-stu-id="6ba58-179">Description: Advanced Audio Coding (AAC)</span></span>
- <span data-ttu-id="6ba58-180">FourCC 或 WAV 識別碼： WAVE_FORMAT_MPEG_HEAAC</span><span class="sxs-lookup"><span data-stu-id="6ba58-180">FourCC or WAV identifiers: WAVE_FORMAT_MPEG_HEAAC</span></span>

<span data-ttu-id="6ba58-181">Matroska 識別碼： A_AC3</span><span class="sxs-lookup"><span data-stu-id="6ba58-181">Matroska ID: A_AC3</span></span>

- <span data-ttu-id="6ba58-182">MSFT 媒體基礎 MF_MT_SUBTYPE： MFAudioFormat_Dolby_AC3</span><span class="sxs-lookup"><span data-stu-id="6ba58-182">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_Dolby_AC3</span></span>
- <span data-ttu-id="6ba58-183">描述：杜 AC3</span><span class="sxs-lookup"><span data-stu-id="6ba58-183">Description: Dolby AC3</span></span>
- <span data-ttu-id="6ba58-184">FourCC 或 WAV 識別碼： WAVE_FORMAT_DOLBY_AC3_SPDIF</span><span class="sxs-lookup"><span data-stu-id="6ba58-184">FourCC or WAV identifiers: WAVE_FORMAT_DOLBY_AC3_SPDIF</span></span>

<span data-ttu-id="6ba58-185">Matroska 識別碼： A_MPEG/L3</span><span class="sxs-lookup"><span data-stu-id="6ba58-185">Matroska ID: A_MPEG/L3</span></span>

- <span data-ttu-id="6ba58-186">MSFT 媒體基礎 MF_MT_SUBTYPE： MFAudioFormat_MP3</span><span class="sxs-lookup"><span data-stu-id="6ba58-186">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_MP3</span></span>
- <span data-ttu-id="6ba58-187">描述： MPEG 音訊第3層 (MP3) </span><span class="sxs-lookup"><span data-stu-id="6ba58-187">Description: MPEG Audio Layer-3 (MP3)</span></span>
- <span data-ttu-id="6ba58-188">FourCC 或 WAV 識別碼： WAVE_FORMAT_MPEGLAYER3</span><span class="sxs-lookup"><span data-stu-id="6ba58-188">FourCC or WAV identifiers: WAVE_FORMAT_MPEGLAYER3</span></span>

<span data-ttu-id="6ba58-189">Matroska 識別碼： A_MPEG/L1</span><span class="sxs-lookup"><span data-stu-id="6ba58-189">Matroska ID: A_MPEG/L1</span></span>

- <span data-ttu-id="6ba58-190">MSFT 媒體基礎 MF_MT_SUBTYPE： MFAudioFormat_MPEG</span><span class="sxs-lookup"><span data-stu-id="6ba58-190">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_MPEG</span></span>
- <span data-ttu-id="6ba58-191">描述： MPEG-2 音訊承載</span><span class="sxs-lookup"><span data-stu-id="6ba58-191">Description: MPEG-1 audio payload</span></span>
- <span data-ttu-id="6ba58-192">FourCC 或 WAV 識別碼： WAVE_FORMAT_MPEG</span><span class="sxs-lookup"><span data-stu-id="6ba58-192">FourCC or WAV identifiers: WAVE_FORMAT_MPEG</span></span>

<span data-ttu-id="6ba58-193">Matroska 識別碼： A_PCM/INT/BIG</span><span class="sxs-lookup"><span data-stu-id="6ba58-193">Matroska ID: A_PCM/INT/BIG</span></span>

- <span data-ttu-id="6ba58-194">MSFT 媒體基礎 MF_MT_SUBTYPE： MFAudioFormat_PCM</span><span class="sxs-lookup"><span data-stu-id="6ba58-194">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_PCM</span></span>
- <span data-ttu-id="6ba58-195">描述：未壓縮的 PCM 音訊</span><span class="sxs-lookup"><span data-stu-id="6ba58-195">Description: Uncompressed PCM audio</span></span>
- <span data-ttu-id="6ba58-196">FourCC 或 WAV 識別碼： WAVE_FORMAT_PCM</span><span class="sxs-lookup"><span data-stu-id="6ba58-196">FourCC or WAV identifiers: WAVE_FORMAT_PCM</span></span>

<span data-ttu-id="6ba58-197">Matroska 識別碼： A_PCM/INT/LIT</span><span class="sxs-lookup"><span data-stu-id="6ba58-197">Matroska ID: A_PCM/INT/LIT</span></span>

- <span data-ttu-id="6ba58-198">MSFT 媒體基礎 MF_MT_SUBTYPE： MFAudioFormat_PCM</span><span class="sxs-lookup"><span data-stu-id="6ba58-198">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_PCM</span></span>
- <span data-ttu-id="6ba58-199">描述：未壓縮的 PCM 音訊</span><span class="sxs-lookup"><span data-stu-id="6ba58-199">Description: Uncompressed PCM audio</span></span>
- <span data-ttu-id="6ba58-200">FourCC 或 WAV 識別碼： WAVE_FORMAT_PCM</span><span class="sxs-lookup"><span data-stu-id="6ba58-200">FourCC or WAV identifiers: WAVE_FORMAT_PCM</span></span>

<span data-ttu-id="6ba58-201">Matroska 識別碼： A_PCM/FLOAT/IEEE</span><span class="sxs-lookup"><span data-stu-id="6ba58-201">Matroska ID: A_PCM/FLOAT/IEEE</span></span>

- <span data-ttu-id="6ba58-202">MSFT 媒體基礎 MF_MT_SUBTYPE： MFAudioFormat_Float</span><span class="sxs-lookup"><span data-stu-id="6ba58-202">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_Float</span></span>
- <span data-ttu-id="6ba58-203">描述：未壓縮的 IEEE 浮點音訊</span><span class="sxs-lookup"><span data-stu-id="6ba58-203">Description: Uncompressed IEEE floating-point audio</span></span>
- <span data-ttu-id="6ba58-204">FourCC 或 WAV 識別碼： WAVE_FORMAT_IEEE_FLOAT</span><span class="sxs-lookup"><span data-stu-id="6ba58-204">FourCC or WAV identifiers: WAVE_FORMAT_IEEE_FLOAT</span></span>

<span data-ttu-id="6ba58-205">Matroska 識別碼： A_ALAC</span><span class="sxs-lookup"><span data-stu-id="6ba58-205">Matroska ID: A_ALAC</span></span>

- <span data-ttu-id="6ba58-206">MSFT 媒體基礎 MF_MT_SUBTYPE： MFAudioFormat_ALAC</span><span class="sxs-lookup"><span data-stu-id="6ba58-206">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_ALAC</span></span>
- <span data-ttu-id="6ba58-207">描述： Apple 無損音訊編解碼器</span><span class="sxs-lookup"><span data-stu-id="6ba58-207">Description: Apple Lossless Audio Codec</span></span>
- <span data-ttu-id="6ba58-208">FourCC 或 WAV 識別碼：</span><span class="sxs-lookup"><span data-stu-id="6ba58-208">FourCC or WAV identifiers:</span></span> 

<span data-ttu-id="6ba58-209">Matroska 識別碼： A_MPEG/L2</span><span class="sxs-lookup"><span data-stu-id="6ba58-209">Matroska ID: A_MPEG/L2</span></span>

- <span data-ttu-id="6ba58-210">MSFT 媒體基礎 MF_MT_SUBTYPE： MFAudioFormat_MPEG</span><span class="sxs-lookup"><span data-stu-id="6ba58-210">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_MPEG</span></span>
- <span data-ttu-id="6ba58-211">描述： MPEG 音訊1、2層 II</span><span class="sxs-lookup"><span data-stu-id="6ba58-211">Description: MPEG Audio 1, 2 Layer II</span></span>
- <span data-ttu-id="6ba58-212">FourCC 或 WAV 識別碼： WAVE_FORMAT_MPEG</span><span class="sxs-lookup"><span data-stu-id="6ba58-212">FourCC or WAV identifiers: WAVE_FORMAT_MPEG</span></span>

<span data-ttu-id="6ba58-213">Matroska 識別碼： A_DTS</span><span class="sxs-lookup"><span data-stu-id="6ba58-213">Matroska ID: A_DTS</span></span>

- <span data-ttu-id="6ba58-214">MSFT 媒體基礎 MF_MT_SUBTYPE： MEDIASUBTYPE_DTS_HD</span><span class="sxs-lookup"><span data-stu-id="6ba58-214">MSFT Media Foundation MF_MT_SUBTYPE: MEDIASUBTYPE_DTS_HD</span></span>
- <span data-ttu-id="6ba58-215">描述：數位劇院系統</span><span class="sxs-lookup"><span data-stu-id="6ba58-215">Description: Digital Theatre System</span></span>
- <span data-ttu-id="6ba58-216">FourCC 或 WAV 識別碼： WAVE_FORMAT_DTS</span><span class="sxs-lookup"><span data-stu-id="6ba58-216">FourCC or WAV identifiers: WAVE_FORMAT_DTS</span></span>

<span data-ttu-id="6ba58-217">Matroska 識別碼： A_OPUS</span><span class="sxs-lookup"><span data-stu-id="6ba58-217">Matroska ID: A_OPUS</span></span>

- <span data-ttu-id="6ba58-218">MSFT 媒體基礎 MF_MT_SUBTYPE： MFAudioFormat_Opus</span><span class="sxs-lookup"><span data-stu-id="6ba58-218">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_Opus</span></span>
- <span data-ttu-id="6ba58-219">描述： Opus</span><span class="sxs-lookup"><span data-stu-id="6ba58-219">Description: Opus</span></span>
- <span data-ttu-id="6ba58-220">FourCC 或 WAV 識別碼： WAVE_FORMAT_OPUS</span><span class="sxs-lookup"><span data-stu-id="6ba58-220">FourCC or WAV identifiers: WAVE_FORMAT_OPUS</span></span>

<span data-ttu-id="6ba58-221">Matroska 識別碼： A_VORBIS</span><span class="sxs-lookup"><span data-stu-id="6ba58-221">Matroska ID: A_VORBIS</span></span>

- <span data-ttu-id="6ba58-222">MSFT 媒體基礎 MF_MT_SUBTYPE： MFAudioFormat_Vorbis</span><span class="sxs-lookup"><span data-stu-id="6ba58-222">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_Vorbis</span></span>
- <span data-ttu-id="6ba58-223">描述： Vorbis</span><span class="sxs-lookup"><span data-stu-id="6ba58-223">Description: Vorbis</span></span>
- <span data-ttu-id="6ba58-224">FourCC 或 WAV 識別碼：</span><span class="sxs-lookup"><span data-stu-id="6ba58-224">FourCC or WAV identifiers:</span></span> 

<span data-ttu-id="6ba58-225">Matroska 識別碼： A_FLAC</span><span class="sxs-lookup"><span data-stu-id="6ba58-225">Matroska ID: A_FLAC</span></span>

- <span data-ttu-id="6ba58-226">MSFT 媒體基礎 MF_MT_SUBTYPE： MFAudioFormat_FLAC</span><span class="sxs-lookup"><span data-stu-id="6ba58-226">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_FLAC</span></span>
- <span data-ttu-id="6ba58-227">描述：無失真音訊編解碼器</span><span class="sxs-lookup"><span data-stu-id="6ba58-227">Description: Free Lossless Audio Codec</span></span>
- <span data-ttu-id="6ba58-228">FourCC 或 WAV 識別碼： WAVE_FORMAT_FLAC</span><span class="sxs-lookup"><span data-stu-id="6ba58-228">FourCC or WAV identifiers: WAVE_FORMAT_FLAC</span></span>

<span data-ttu-id="6ba58-229">Matroska ID： A_AAC/MAIN</span><span class="sxs-lookup"><span data-stu-id="6ba58-229">Matroska ID: A_AAC/MAIN</span></span>

- <span data-ttu-id="6ba58-230">MSFT 媒體基礎 MF_MT_SUBTYPE： MFAudioFormat_AAC</span><span class="sxs-lookup"><span data-stu-id="6ba58-230">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_AAC</span></span>
- <span data-ttu-id="6ba58-231">描述： Advanced Audio 編碼 (AAC) </span><span class="sxs-lookup"><span data-stu-id="6ba58-231">Description: Advanced Audio Coding (AAC)</span></span>
- <span data-ttu-id="6ba58-232">FourCC 或 WAV 識別碼： WAVE_FORMAT_MPEG_HEAAC</span><span class="sxs-lookup"><span data-stu-id="6ba58-232">FourCC or WAV identifiers: WAVE_FORMAT_MPEG_HEAAC</span></span>

<span data-ttu-id="6ba58-233">Matroska 識別碼： A_EAC3</span><span class="sxs-lookup"><span data-stu-id="6ba58-233">Matroska ID: A_EAC3</span></span>

- <span data-ttu-id="6ba58-234">MSFT 媒體基礎 MF_MT_SUBTYPE： MFAudioFormat_Dolby_DDPlus</span><span class="sxs-lookup"><span data-stu-id="6ba58-234">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_Dolby_DDPlus</span></span>
- <span data-ttu-id="6ba58-235">描述：增強的 AC-3</span><span class="sxs-lookup"><span data-stu-id="6ba58-235">Description: Enhanced AC-3</span></span>
- <span data-ttu-id="6ba58-236">FourCC 或 WAV 識別碼：</span><span class="sxs-lookup"><span data-stu-id="6ba58-236">FourCC or WAV identifiers:</span></span> 

<span data-ttu-id="6ba58-237">Matroska 識別碼： A_TRUEHD</span><span class="sxs-lookup"><span data-stu-id="6ba58-237">Matroska ID: A_TRUEHD</span></span>

- <span data-ttu-id="6ba58-238">MSFT 媒體基礎 MF_MT_SUBTYPE： MEDIASUBTYPE_DOLBY_TRUEHD</span><span class="sxs-lookup"><span data-stu-id="6ba58-238">MSFT Media Foundation MF_MT_SUBTYPE: MEDIASUBTYPE_DOLBY_TRUEHD</span></span>
- <span data-ttu-id="6ba58-239">描述：杜 TrueHD</span><span class="sxs-lookup"><span data-stu-id="6ba58-239">Description: Dolby TrueHD</span></span>
- <span data-ttu-id="6ba58-240">FourCC 或 WAV 識別碼：</span><span class="sxs-lookup"><span data-stu-id="6ba58-240">FourCC or WAV identifiers:</span></span> 

<span data-ttu-id="6ba58-241">Matroska 識別碼： A_MS/ACM</span><span class="sxs-lookup"><span data-stu-id="6ba58-241">Matroska ID: A_MS/ACM</span></span>

- <span data-ttu-id="6ba58-242">MSFT 媒體基礎 MF_MT_SUBTYPE：對應至 mmreg 中定義的數個 WAVE_FORMAT 音訊類型</span><span class="sxs-lookup"><span data-stu-id="6ba58-242">MSFT Media Foundation MF_MT_SUBTYPE: Maps to several WAVE_FORMAT audio types defined in mmreg.h</span></span>


### <a name="subtitles-codec-support-for-mkv"></a><span data-ttu-id="6ba58-243">.MKV 的字幕編解碼器支援</span><span class="sxs-lookup"><span data-stu-id="6ba58-243">Subtitles codec support for MKV</span></span>

<span data-ttu-id="6ba58-244">Matroska 識別碼： S_TEXT/ASCII</span><span class="sxs-lookup"><span data-stu-id="6ba58-244">Matroska ID: S_TEXT/ASCII</span></span>

- <span data-ttu-id="6ba58-245">MSFT 媒體基礎 MF_MT_SUBTYPE： MFSubtitleFormat_SRT</span><span class="sxs-lookup"><span data-stu-id="6ba58-245">MSFT Media Foundation MF_MT_SUBTYPE: MFSubtitleFormat_SRT</span></span>
- <span data-ttu-id="6ba58-246">描述： ASCII 文字</span><span class="sxs-lookup"><span data-stu-id="6ba58-246">Description: ASCII text</span></span>

<span data-ttu-id="6ba58-247">Matroska 識別碼： S_TEXT/UTF8</span><span class="sxs-lookup"><span data-stu-id="6ba58-247">Matroska ID: S_TEXT/UTF8</span></span>

- <span data-ttu-id="6ba58-248">MSFT 媒體基礎 MF_MT_SUBTYPE： MFSubtitleFormat_SRT</span><span class="sxs-lookup"><span data-stu-id="6ba58-248">MSFT Media Foundation MF_MT_SUBTYPE: MFSubtitleFormat_SRT</span></span>
- <span data-ttu-id="6ba58-249">描述： UTF-8 純文字</span><span class="sxs-lookup"><span data-stu-id="6ba58-249">Description: UTF-8 Plain Text</span></span>

<span data-ttu-id="6ba58-250">Matroska 識別碼： S_TEXT/SSA</span><span class="sxs-lookup"><span data-stu-id="6ba58-250">Matroska ID: S_TEXT/SSA</span></span>

- <span data-ttu-id="6ba58-251">MSFT 媒體基礎 MF_MT_SUBTYPE： MFSubtitleFormat_SSA</span><span class="sxs-lookup"><span data-stu-id="6ba58-251">MSFT Media Foundation MF_MT_SUBTYPE: MFSubtitleFormat_SSA</span></span>
- <span data-ttu-id="6ba58-252">描述：字幕格式</span><span class="sxs-lookup"><span data-stu-id="6ba58-252">Description: Subtitles Format</span></span>

<span data-ttu-id="6ba58-253">Matroska 識別碼： S_TEXT/ASS</span><span class="sxs-lookup"><span data-stu-id="6ba58-253">Matroska ID: S_TEXT/ASS</span></span>

- <span data-ttu-id="6ba58-254">MSFT 媒體基礎 MF_MT_SUBTYPE： MFSubtitleFormat_SSA</span><span class="sxs-lookup"><span data-stu-id="6ba58-254">MSFT Media Foundation MF_MT_SUBTYPE: MFSubtitleFormat_SSA</span></span>
- <span data-ttu-id="6ba58-255">描述： Advanced 字幕格式</span><span class="sxs-lookup"><span data-stu-id="6ba58-255">Description: Advanced Subtitles Format</span></span>

<span data-ttu-id="6ba58-256">Matroska 識別碼： S_VOBSUB</span><span class="sxs-lookup"><span data-stu-id="6ba58-256">Matroska ID: S_VOBSUB</span></span>

- <span data-ttu-id="6ba58-257">MSFT 媒體基礎 MF_MT_SUBTYPE： MFSubtitleFormat_VobSub</span><span class="sxs-lookup"><span data-stu-id="6ba58-257">MSFT Media Foundation MF_MT_SUBTYPE: MFSubtitleFormat_VobSub</span></span>
- <span data-ttu-id="6ba58-258">描述： VobSub 字幕</span><span class="sxs-lookup"><span data-stu-id="6ba58-258">Description: VobSub subtitles</span></span>

<span data-ttu-id="6ba58-259">Matroska 識別碼： S_HDMV/PGS</span><span class="sxs-lookup"><span data-stu-id="6ba58-259">Matroska ID: S_HDMV/PGS</span></span>

- <span data-ttu-id="6ba58-260">MSFT 媒體基礎 MF_MT_SUBTYPE： MFSubtitleFormat_PGS</span><span class="sxs-lookup"><span data-stu-id="6ba58-260">MSFT Media Foundation MF_MT_SUBTYPE: MFSubtitleFormat_PGS</span></span>
- <span data-ttu-id="6ba58-261">描述： HDMV 簡報圖形副標題 (PG) </span><span class="sxs-lookup"><span data-stu-id="6ba58-261">Description: HDMV presentation graphics subtitles (PGS)</span></span>


## <a name="technical-details-regarding-codecs"></a><span data-ttu-id="6ba58-262">編解碼器的相關技術詳細資料</span><span class="sxs-lookup"><span data-stu-id="6ba58-262">Technical details regarding codecs</span></span>

<span data-ttu-id="6ba58-263">如需編解碼器的相關技術詳細資料，請參閱下列各項。</span><span class="sxs-lookup"><span data-stu-id="6ba58-263">See the following for technical details regarding codecs.</span></span>

- [<span data-ttu-id="6ba58-264">Matroska 編解碼器規格</span><span class="sxs-lookup"><span data-stu-id="6ba58-264">Matroska Codec Specs</span></span>](http://www.matroska.org/technical/specs/codecid/index.html)
- [<span data-ttu-id="6ba58-265">音訊子類型 Guid</span><span class="sxs-lookup"><span data-stu-id="6ba58-265">Audio Subtype GUIDs</span></span>](audio-subtype-guids.md)
- [<span data-ttu-id="6ba58-266">影片子類型 Guid</span><span class="sxs-lookup"><span data-stu-id="6ba58-266">Video Subtype GUIDs</span></span>](video-subtype-guids.md)


## <a name="related-topics"></a><span data-ttu-id="6ba58-267">相關主題</span><span class="sxs-lookup"><span data-stu-id="6ba58-267">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6ba58-268">媒體基礎中支援的媒體格式</span><span class="sxs-lookup"><span data-stu-id="6ba58-268">Supported Media Formats in Media Foundation</span></span>](supported-media-formats-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="6ba58-269">媒體基礎程式設計指南</span><span class="sxs-lookup"><span data-stu-id="6ba58-269">Media Foundation Programming Guide</span></span>](media-foundation-programming-guide.md)
</dt> </dl>

 

 



