---
description: 編解碼器物件
ms.assetid: c944e5df-c375-4bad-92dc-bb3d8c09b1b3
title: 編解碼器物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3a4f140c81f162aaee2ffc416ed1de96dfcb470
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689352"
---
# <a name="codec-objects"></a><span data-ttu-id="c4929-103">編解碼器物件</span><span class="sxs-lookup"><span data-stu-id="c4929-103">Codec Objects</span></span>

<span data-ttu-id="c4929-104">本節說明 Microsoft 媒體基礎中支援的編碼器和解碼器。</span><span class="sxs-lookup"><span data-stu-id="c4929-104">This section describes the encoders and decoders that are supported in Microsoft Media Foundation.</span></span> <span data-ttu-id="c4929-105">此章節包含下列主題。</span><span class="sxs-lookup"><span data-stu-id="c4929-105">This section contains the following topics.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c4929-106">主題</span><span class="sxs-lookup"><span data-stu-id="c4929-106">Topic</span></span></th>
<th><span data-ttu-id="c4929-107">描述</span><span class="sxs-lookup"><span data-stu-id="c4929-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c4929-108"><a href="aac-decoder.md"><strong>AAC 解碼器</strong></a></span><span class="sxs-lookup"><span data-stu-id="c4929-108"><a href="aac-decoder.md"><strong>AAC Decoder</strong></a></span></span></td>
<td><span data-ttu-id="c4929-109">音訊解碼器，可將下列高階音訊編碼編碼 (AAC) 和高效率 AAC (AAC) 設定檔：</span><span class="sxs-lookup"><span data-stu-id="c4929-109">An audio decoder that decodes the following Advanced Audio Coding (AAC) and High Efficiency AAC (HE-AAC) profiles:</span></span>
<ul>
<li><span data-ttu-id="c4929-110">MPEG-2 AAC 低複雜度 (LC) 設定檔 (多重通道) 。</span><span class="sxs-lookup"><span data-stu-id="c4929-110">MPEG-2 AAC Low Complexity (LC) profile (multichannel).</span></span></li>
<li><span data-ttu-id="c4929-111">MPEG-2 AAC v1 (多重通道) 搭配 AAC-LC 核心。</span><span class="sxs-lookup"><span data-stu-id="c4929-111">MPEG-4 HE-AAC v1 (multichannel) with AAC-LC core.</span></span></li>
<li><span data-ttu-id="c4929-112">使用 AAC-LC 核心的 MPEG-2 AAC v2 (身歷聲) 。</span><span class="sxs-lookup"><span data-stu-id="c4929-112">MPEG-4 HE-AAC v2 (stereo) with AAC-LC core.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4929-113"><a href="aac-encoder.md"><strong>AAC 編碼器</strong></a></span><span class="sxs-lookup"><span data-stu-id="c4929-113"><a href="aac-encoder.md"><strong>AAC Encoder</strong></a></span></span></td>
<td><span data-ttu-id="c4929-114">編碼 Advanced Audio 編碼 (AAC) 低複雜度 (LC) 設定檔的音訊編碼器。</span><span class="sxs-lookup"><span data-stu-id="c4929-114">An audio encoder that encodes Advanced Audio Coding (AAC) Low Complexity (LC) profile.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4929-115"><a href="dv-video-decoder.md"><strong>DV 影片解碼</strong></a></span><span class="sxs-lookup"><span data-stu-id="c4929-115"><a href="dv-video-decoder.md"><strong>DV Video Decoder</strong></a></span></span></td>
<td><span data-ttu-id="c4929-116">解碼 DV 影片的視頻解碼器。</span><span class="sxs-lookup"><span data-stu-id="c4929-116">A video decoder that decodes DV video.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4929-117"><a href="h-264-video-decoder.md"><strong>H.264 Video 解碼</strong></a></span><span class="sxs-lookup"><span data-stu-id="c4929-117"><a href="h-264-video-decoder.md"><strong>H.264 Video Decoder</strong></a></span></span></td>
<td><span data-ttu-id="c4929-118">解碼 h.264 video 的視頻解碼器。</span><span class="sxs-lookup"><span data-stu-id="c4929-118">A video decoder that decodes H.264 video.</span></span> <span data-ttu-id="c4929-119">它支援解碼基準、主要和高設定檔，最多可達層級5.1。</span><span class="sxs-lookup"><span data-stu-id="c4929-119">It supports decoding of Baseline, Main, and High profiles, up to level 5.1.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4929-120"><a href="h-264-video-encoder.md"><strong>H.264 影片編碼器</strong></a></span><span class="sxs-lookup"><span data-stu-id="c4929-120"><a href="h-264-video-encoder.md"><strong>H.264 Video Encoder</strong></a></span></span></td>
<td><span data-ttu-id="c4929-121">編碼 h.264 影片的視頻編碼器。</span><span class="sxs-lookup"><span data-stu-id="c4929-121">A video encoder that encodes H.264 video.</span></span> <span data-ttu-id="c4929-122">它支援下列 h.264 設定檔：</span><span class="sxs-lookup"><span data-stu-id="c4929-122">It supports the following H.264 profiles:</span></span>
<ul>
<li><span data-ttu-id="c4929-123">基準設定檔</span><span class="sxs-lookup"><span data-stu-id="c4929-123">Baseline Profile</span></span></li>
<li><span data-ttu-id="c4929-124">主要設定檔</span><span class="sxs-lookup"><span data-stu-id="c4929-124">Main Profile</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4929-125"><a href="h-264-video-decoder.md"><strong>H. 265/HEVC 影片解碼器</strong></a></span><span class="sxs-lookup"><span data-stu-id="c4929-125"><a href="h-264-video-decoder.md"><strong>H.265 / HEVC Video Decoder</strong></a></span></span></td>
<td><span data-ttu-id="c4929-126">支援以附錄 B 格式解碼 H. 265/HEVC 內容的視頻解碼器，可用於播放數量和 .m2ts 檔案。</span><span class="sxs-lookup"><span data-stu-id="c4929-126">A video decoder that supports decoding H.265/HEVC content in Annex B format and can be used in playback of mp4 and m2ts files.</span></span> <span data-ttu-id="c4929-127">它支援下列 h.264 設定檔：</span><span class="sxs-lookup"><span data-stu-id="c4929-127">It supports the following H.264 profiles:</span></span>
<ul>
<li><span data-ttu-id="c4929-128">主要設定檔</span><span class="sxs-lookup"><span data-stu-id="c4929-128">Main Profile</span></span></li>
<li><span data-ttu-id="c4929-129">主要10設定檔</span><span class="sxs-lookup"><span data-stu-id="c4929-129">Main 10 Profile</span></span></li>
<li><span data-ttu-id="c4929-130">主要還是圖片</span><span class="sxs-lookup"><span data-stu-id="c4929-130">Main still picture</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4929-131"><a href="h-264-video-encoder.md"><strong>H. 265/HEVC 影片編碼器</strong></a></span><span class="sxs-lookup"><span data-stu-id="c4929-131"><a href="h-264-video-encoder.md"><strong>H.265 / HEVC Video Encoder</strong></a></span></span></td>
<td><span data-ttu-id="c4929-132">編碼 H 265/HEVC 格式的影片編碼器。</span><span class="sxs-lookup"><span data-stu-id="c4929-132">A video encoder that encodes H.265/HEVC format.</span></span> <span data-ttu-id="c4929-133">它支援下列 .H 設定檔：</span><span class="sxs-lookup"><span data-stu-id="c4929-133">It supports the following H.265 profiles:</span></span>
<ul>
<li><span data-ttu-id="c4929-134">主要設定檔</span><span class="sxs-lookup"><span data-stu-id="c4929-134">Main Profile</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4929-135"><a href="mpeg4part2videodecoder.md"><strong>MPEG4 第2部分影片解碼</strong></a></span><span class="sxs-lookup"><span data-stu-id="c4929-135"><a href="mpeg4part2videodecoder.md"><strong>MPEG4 Part 2 Video Decoder</strong></a></span></span></td>
<td><span data-ttu-id="c4929-136">MPEG-2 第2部分影片解碼器。</span><span class="sxs-lookup"><span data-stu-id="c4929-136">MPEG-4 Part 2 video decoder.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4929-137"><a href="windowsmediaaudiodecoder.md"><strong>Windows Media 音訊的解碼器</strong></a></span><span class="sxs-lookup"><span data-stu-id="c4929-137"><a href="windowsmediaaudiodecoder.md"><strong>Windows Media Audio Decoder</strong></a></span></span></td>
<td><span data-ttu-id="c4929-138">解碼 Windows Media 音訊編碼器所編碼之資料流程的解碼器。</span><span class="sxs-lookup"><span data-stu-id="c4929-138">A decoder that decodes streams encoded by the Windows Media Audio Encoder.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4929-139"><a href="windowsmediaaudioencoder.md">Windows Media 音訊編碼器</a></span><span class="sxs-lookup"><span data-stu-id="c4929-139"><a href="windowsmediaaudioencoder.md">Windows Media Audio Encoder</a></span></span></td>
<td><span data-ttu-id="c4929-140">支援三種編碼輸出類別的音訊編碼器：</span><span class="sxs-lookup"><span data-stu-id="c4929-140">An audio encoder that supports three categories of encoded output:</span></span>
<ul>
<li><span data-ttu-id="c4929-141">標準</span><span class="sxs-lookup"><span data-stu-id="c4929-141">Standard</span></span></li>
<li><span data-ttu-id="c4929-142">Professional</span><span class="sxs-lookup"><span data-stu-id="c4929-142">Professional</span></span></li>
<li><span data-ttu-id="c4929-143">Lossless</span><span class="sxs-lookup"><span data-stu-id="c4929-143">Lossless</span></span></li>
</ul>
<span data-ttu-id="c4929-144">標準類別適用于一般用途的音訊編碼。</span><span class="sxs-lookup"><span data-stu-id="c4929-144">The Standard category is for general-purpose audio encoding.</span></span> <span data-ttu-id="c4929-145">Professional 類別目錄適用于編碼多重通道或高定義音訊。</span><span class="sxs-lookup"><span data-stu-id="c4929-145">The Professional category is for encoding multi-channel or high-definition audio.</span></span> <span data-ttu-id="c4929-146">無失真類別是用來壓縮音訊，而不會遺失任何原始資料。</span><span class="sxs-lookup"><span data-stu-id="c4929-146">The Lossless category is for compressing audio without losing any of the original data.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4929-147"><a href="windowsmediaaudiovoicedecoder.md"><strong>Windows Media 音訊語音解碼器</strong></a></span><span class="sxs-lookup"><span data-stu-id="c4929-147"><a href="windowsmediaaudiovoicedecoder.md"><strong>Windows Media Audio Voice Decoder</strong></a></span></span></td>
<td><span data-ttu-id="c4929-148">解碼 Windows Media 音訊聲音編碼程式所編碼之資料流程的解碼器。</span><span class="sxs-lookup"><span data-stu-id="c4929-148">A decoder that decodes streams encoded by the Windows Media Audio Voice Encoder.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4929-149"><a href="windowsmediaaudiovoiceencoder.md">Windows Media 音訊語音編碼器</a></span><span class="sxs-lookup"><span data-stu-id="c4929-149"><a href="windowsmediaaudiovoiceencoder.md">Windows Media Audio Voice Encoder</a></span></span></td>
<td><span data-ttu-id="c4929-150">編碼音訊的編碼器，其中包含大部分的語音。</span><span class="sxs-lookup"><span data-stu-id="c4929-150">An encoder for encoding audio containing mostly speech.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4929-151"><a href="windows-media-mp3-decoder.md"><strong>Windows Media MP3 解碼</strong></a></span><span class="sxs-lookup"><span data-stu-id="c4929-151"><a href="windows-media-mp3-decoder.md"><strong>Windows Media MP3 Decoder</strong></a></span></span></td>
<td><span data-ttu-id="c4929-152">解碼下列音訊格式的音訊解碼器。</span><span class="sxs-lookup"><span data-stu-id="c4929-152">An audio decoder that decodes the following audio formats.</span></span>
<ul>
<li><span data-ttu-id="c4929-153">ISO/IEC 11172-3 (MPEG 1 音訊) 第3層</span><span class="sxs-lookup"><span data-stu-id="c4929-153">ISO/IEC 11172-3 (MPEG-1 Audio) Layer 3</span></span></li>
<li><span data-ttu-id="c4929-154">ISO/IEC 13818-3 (MPEG-2 音訊) 第3層，低取樣頻率延伸</span><span class="sxs-lookup"><span data-stu-id="c4929-154">ISO/IEC 13818-3 (MPEG-2 Audio) Layer 3, low sampling frequency extension</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4929-155"><a href="windowsmediampeg4decoder.md"><strong>Windows Media MPEG4 V1/V2 解碼器</strong></a></span><span class="sxs-lookup"><span data-stu-id="c4929-155"><a href="windowsmediampeg4decoder.md"><strong>Windows Media MPEG4 V1/V2 Decoder</strong></a></span></span></td>
<td><span data-ttu-id="c4929-156">可執行 MPEG 4 V1/V2 影片解碼的解碼器。</span><span class="sxs-lookup"><span data-stu-id="c4929-156">A decoder that implements MPEG-4 V1/V2 video decoding.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4929-157"><a href="windows-media-video-7-and-8-encoders.md"><strong>Windows Media 視訊7/8 編碼器</strong></a></span><span class="sxs-lookup"><span data-stu-id="c4929-157"><a href="windows-media-video-7-and-8-encoders.md"><strong>Windows Media Video 7/8 Encoder</strong></a></span></span></td>
<td><span data-ttu-id="c4929-158">可執行舊版 Windows Media 視訊編碼器的影片編碼器。</span><span class="sxs-lookup"><span data-stu-id="c4929-158">A video encoder that implements previous versions of the Windows Media Video encoder.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4929-159"><a href="windowsmediavideo9decoder.md">Windows Media 視訊9解碼器</a></span><span class="sxs-lookup"><span data-stu-id="c4929-159"><a href="windowsmediavideo9decoder.md">Windows Media Video 9 Decoder</a></span></span></td>
<td><span data-ttu-id="c4929-160">可解碼 Windows Media 視訊9編碼器編碼之資料流程的視頻編碼器。</span><span class="sxs-lookup"><span data-stu-id="c4929-160">A video decoder that decodes streams encoded by the Windows Media Video 9 encoder.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4929-161"><a href="windowsmediavideo9encoder.md">Windows Media 視訊9編碼器</a></span><span class="sxs-lookup"><span data-stu-id="c4929-161"><a href="windowsmediavideo9encoder.md">Windows Media Video 9 Encoder</a></span></span></td>
<td><span data-ttu-id="c4929-162">支援三種 endoded 輸出類別的影片編碼器：</span><span class="sxs-lookup"><span data-stu-id="c4929-162">A video encoder that supports three categories of endoded output:</span></span>
<ul>
<li><span data-ttu-id="c4929-163">Windows Media 視訊9</span><span class="sxs-lookup"><span data-stu-id="c4929-163">Windows Media Video 9</span></span></li>
<li><span data-ttu-id="c4929-164">Windows Media 視訊 9 Advanced Profile</span><span class="sxs-lookup"><span data-stu-id="c4929-164">Windows Media Video 9 Advanced Profile</span></span></li>
<li><span data-ttu-id="c4929-165">Windows Media 視訊9.1 影像</span><span class="sxs-lookup"><span data-stu-id="c4929-165">Windows Media Video 9.1 Image</span></span></li>
</ul>
<span data-ttu-id="c4929-166">Windows Media 視訊9類別適用于一般用途的影片編碼。</span><span class="sxs-lookup"><span data-stu-id="c4929-166">The Windows Media Video 9 category is for general-purpose video encoding.</span></span> <span data-ttu-id="c4929-167">「高階設定檔」類別適用于編碼符合 VC 1 Advanced Profile SMPTE 標準的高定義影片或影片。</span><span class="sxs-lookup"><span data-stu-id="c4929-167">The Advanced Profile category is for encoding high-definition video or video that conforms to the VC-1 Advanced Profile SMPTE standard.</span></span> <span data-ttu-id="c4929-168">影像類別目錄是用來將點陣圖影像轉換成動態影片。</span><span class="sxs-lookup"><span data-stu-id="c4929-168">The Image category is for converting bitmap images to dynamic video.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4929-169"><a href="windowsmediavideo9screendecoder.md"><strong>Windows Media 視訊9螢幕解碼</strong></a></span><span class="sxs-lookup"><span data-stu-id="c4929-169"><a href="windowsmediavideo9screendecoder.md"><strong>Windows Media Video 9 Screen Decoder</strong></a></span></span></td>
<td><span data-ttu-id="c4929-170">解碼 Windows Media 視訊9螢幕編碼器所編碼之資料流程的解碼器。</span><span class="sxs-lookup"><span data-stu-id="c4929-170">A decoder that decodes streams encoded by the Windows Media Video 9 Screen encoder.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4929-171"><a href="windowsmediavideo9screenencoder.md"><strong>Windows Media 視訊9螢幕編碼器</strong></a></span><span class="sxs-lookup"><span data-stu-id="c4929-171"><a href="windowsmediavideo9screenencoder.md"><strong>Windows Media Video 9 Screen Encoder</strong></a></span></span></td>
<td><span data-ttu-id="c4929-172">編碼電腦的編碼程式影片 (螢幕擷取畫面) 或其他高度靜態的影片。</span><span class="sxs-lookup"><span data-stu-id="c4929-172">An encoder for encoding computer-application video (screen capture) or other highly static video.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="c4929-173">相關主題</span><span class="sxs-lookup"><span data-stu-id="c4929-173">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c4929-174">媒體基礎程式設計參考</span><span class="sxs-lookup"><span data-stu-id="c4929-174">Media Foundation Programming Reference</span></span>](media-foundation-programming-reference.md)
</dt> <dt>

[<span data-ttu-id="c4929-175">媒體基礎中支援的媒體格式</span><span class="sxs-lookup"><span data-stu-id="c4929-175">Supported Media Formats in Media Foundation</span></span>](supported-media-formats-in-media-foundation.md)
</dt> </dl>

 

 



