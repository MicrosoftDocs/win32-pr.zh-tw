---
description: MPEG-2 檔案來源會剖析3GPP 檔案。
ms.assetid: e64c1554-9702-4cc0-98ad-8a33e04ed09d
title: MPEG-2 檔案來源
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c90df56d58df19a53c37436bd631a1cc68dd8114
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191776"
---
# <a name="mpeg-4-file-source"></a><span data-ttu-id="085ac-103">MPEG-2 檔案來源</span><span class="sxs-lookup"><span data-stu-id="085ac-103">MPEG-4 File Source</span></span>

<span data-ttu-id="085ac-104">MPEG-2 檔案來源會剖析3GPP 檔案。</span><span class="sxs-lookup"><span data-stu-id="085ac-104">The MPEG-4 file source parses MP4 and 3GPP files.</span></span> <span data-ttu-id="085ac-105">如需有關檔案格式的詳細資訊，請參閱下列標準檔：</span><span class="sxs-lookup"><span data-stu-id="085ac-105">For more information about the MP4 file format, refer to the following standards documents:</span></span>

-   <span data-ttu-id="085ac-106">ISO/IEC 14496-12： *資訊技術--音訊-視覺化物件的編碼--第12部分： ISO 基底媒體檔案格式*</span><span class="sxs-lookup"><span data-stu-id="085ac-106">ISO/IEC 14496-12: *Information technology -- Coding of audio-visual objects -- Part 12: ISO Base Media File Format*</span></span>
-   <span data-ttu-id="085ac-107">ISO/IEC 14496-14： *資訊技術--音訊-視覺化物件的編碼--第14部分：數量檔案格式*</span><span class="sxs-lookup"><span data-stu-id="085ac-107">ISO/IEC 14496-14: *Information technology -- Coding of audio-visual objects -- Part 14: MP4 File Format*</span></span>

> [!Note]  
> <span data-ttu-id="085ac-108"> (這些資源可能無法在某些語言及國家/地區使用。 ) </span><span class="sxs-lookup"><span data-stu-id="085ac-108">(These resources may not be available in some languages and countries.)</span></span>

 

<span data-ttu-id="085ac-109">MPEG 4 檔案來源不會將檔案中的音訊/影片資料解碼。</span><span class="sxs-lookup"><span data-stu-id="085ac-109">The MPEG-4 file source does not decode the audio/video data in the file.</span></span>

<span data-ttu-id="085ac-110">本主題包含下列幾節：</span><span class="sxs-lookup"><span data-stu-id="085ac-110">This topic contains the following sections:</span></span>

## <a name="file-extensions-and-mime-types"></a><span data-ttu-id="085ac-111">副檔名和 MIME 類型</span><span class="sxs-lookup"><span data-stu-id="085ac-111">File Extensions and MIME Types</span></span>

<span data-ttu-id="085ac-112">MPEG 4 檔案來源是下列副檔名的預設媒體來源。</span><span class="sxs-lookup"><span data-stu-id="085ac-112">The MPEG-4 file source is the default media source for the following file name extensions.</span></span>



| <span data-ttu-id="085ac-113">副檔名</span><span class="sxs-lookup"><span data-stu-id="085ac-113">File extension</span></span> | <span data-ttu-id="085ac-114">Description</span><span class="sxs-lookup"><span data-stu-id="085ac-114">Description</span></span>           |
|----------------|-----------------------|
| <span data-ttu-id="085ac-115">.3g2</span><span class="sxs-lookup"><span data-stu-id="085ac-115">.3g2</span></span>           | <span data-ttu-id="085ac-116">3GPP2</span><span class="sxs-lookup"><span data-stu-id="085ac-116">3GPP2</span></span>                 |
| <span data-ttu-id="085ac-117">.3gp</span><span class="sxs-lookup"><span data-stu-id="085ac-117">.3gp</span></span>           | <span data-ttu-id="085ac-118">3GPP</span><span class="sxs-lookup"><span data-stu-id="085ac-118">3GPP</span></span>                  |
| <span data-ttu-id="085ac-119">.3gp2</span><span class="sxs-lookup"><span data-stu-id="085ac-119">.3gp2</span></span>          | <span data-ttu-id="085ac-120">3GPP2</span><span class="sxs-lookup"><span data-stu-id="085ac-120">3GPP2</span></span>                 |
| <span data-ttu-id="085ac-121">.3gpp</span><span class="sxs-lookup"><span data-stu-id="085ac-121">.3gpp</span></span>          | <span data-ttu-id="085ac-122">3GPP</span><span class="sxs-lookup"><span data-stu-id="085ac-122">3GPP</span></span>                  |
| <span data-ttu-id="085ac-123">.m4a</span><span class="sxs-lookup"><span data-stu-id="085ac-123">.m4a</span></span>           | <span data-ttu-id="085ac-124">MPEG-2 音訊</span><span class="sxs-lookup"><span data-stu-id="085ac-124">MPEG-4 audio</span></span>          |
| <span data-ttu-id="085ac-125">.m4v</span><span class="sxs-lookup"><span data-stu-id="085ac-125">.m4v</span></span>           | <span data-ttu-id="085ac-126">MPEG 4 影片</span><span class="sxs-lookup"><span data-stu-id="085ac-126">MPEG-4 video</span></span>          |
| <span data-ttu-id="085ac-127">.mov</span><span class="sxs-lookup"><span data-stu-id="085ac-127">.mov</span></span>           | <span data-ttu-id="085ac-128">Apple QuickTime 電影</span><span class="sxs-lookup"><span data-stu-id="085ac-128">Apple QuickTime Movie</span></span> |
| <span data-ttu-id="085ac-129">.mp4</span><span class="sxs-lookup"><span data-stu-id="085ac-129">.mp4</span></span>           | <span data-ttu-id="085ac-130">MPEG-2 音訊或影片</span><span class="sxs-lookup"><span data-stu-id="085ac-130">MPEG-4 audio or video</span></span> |
| <span data-ttu-id="085ac-131">.mp4v</span><span class="sxs-lookup"><span data-stu-id="085ac-131">.mp4v</span></span>          | <span data-ttu-id="085ac-132">MPEG 4 影片</span><span class="sxs-lookup"><span data-stu-id="085ac-132">MPEG-4 video</span></span>          |



 

<span data-ttu-id="085ac-133">它也是下列 MIME 類型的預設媒體來源。</span><span class="sxs-lookup"><span data-stu-id="085ac-133">It is also the default media source for the following MIME types.</span></span>



| <span data-ttu-id="085ac-134">MIME 類型 (MIME type)</span><span class="sxs-lookup"><span data-stu-id="085ac-134">MIME type</span></span>   | <span data-ttu-id="085ac-135">Description</span><span class="sxs-lookup"><span data-stu-id="085ac-135">Description</span></span>  |
|-------------|--------------|
| <span data-ttu-id="085ac-136">音訊/3gpp</span><span class="sxs-lookup"><span data-stu-id="085ac-136">audio/3gpp</span></span>  | <span data-ttu-id="085ac-137">3GPP 音訊</span><span class="sxs-lookup"><span data-stu-id="085ac-137">3GPP audio</span></span>   |
| <span data-ttu-id="085ac-138">音訊/3gpp2</span><span class="sxs-lookup"><span data-stu-id="085ac-138">audio/3gpp2</span></span> | <span data-ttu-id="085ac-139">3GPP2 音訊</span><span class="sxs-lookup"><span data-stu-id="085ac-139">3GPP2 audio</span></span>  |
| <span data-ttu-id="085ac-140">音訊/的</span><span class="sxs-lookup"><span data-stu-id="085ac-140">audio/mp4</span></span>   | <span data-ttu-id="085ac-141">MPEG-2 音訊</span><span class="sxs-lookup"><span data-stu-id="085ac-141">MPEG-4 audio</span></span> |
| <span data-ttu-id="085ac-142">影片/3gpp</span><span class="sxs-lookup"><span data-stu-id="085ac-142">video/3gpp</span></span>  | <span data-ttu-id="085ac-143">3GPP 影片</span><span class="sxs-lookup"><span data-stu-id="085ac-143">3GPP video</span></span>   |
| <span data-ttu-id="085ac-144">影片/3gpp2</span><span class="sxs-lookup"><span data-stu-id="085ac-144">video/3gpp2</span></span> | <span data-ttu-id="085ac-145">3GPP2 影片</span><span class="sxs-lookup"><span data-stu-id="085ac-145">3GPP2 video</span></span>  |
| <span data-ttu-id="085ac-146">影片/</span><span class="sxs-lookup"><span data-stu-id="085ac-146">video/mp4</span></span>   | <span data-ttu-id="085ac-147">MPEG 4 影片</span><span class="sxs-lookup"><span data-stu-id="085ac-147">MPEG-4 video</span></span> |



 

## <a name="media-types"></a><span data-ttu-id="085ac-148">媒體類型</span><span class="sxs-lookup"><span data-stu-id="085ac-148">Media Types</span></span>

<span data-ttu-id="085ac-149">使用的是可擴充的容器格式。</span><span class="sxs-lookup"><span data-stu-id="085ac-149">MP4 is an extensible container format.</span></span> <span data-ttu-id="085ac-150">使用規定規格不會定義固定的結構，以描述未設定的容器中的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="085ac-150">The MP4 specification does not define a fixed structure for describing media types in an MP4 container.</span></span> <span data-ttu-id="085ac-151">相反地，它會定義物件階層，讓您針對每個格式定義自訂結構。</span><span class="sxs-lookup"><span data-stu-id="085ac-151">Instead, it defines an object hierarchy that allows custom structures to be defined for each format.</span></span> <span data-ttu-id="085ac-152">格式描述會儲存在該資料流程 ( [stsd] ) 框的範例描述中。</span><span class="sxs-lookup"><span data-stu-id="085ac-152">The format description is stored in the sample description ('stsd') box for that stream.</span></span> <span data-ttu-id="085ac-153">[範例描述] 方塊包含範例專案的清單。</span><span class="sxs-lookup"><span data-stu-id="085ac-153">The sample description box contains a list of sample entries.</span></span> <span data-ttu-id="085ac-154">針對每個範例專案，4位元組的程式碼（類似于 FOURCC）會定義格式結構。</span><span class="sxs-lookup"><span data-stu-id="085ac-154">For each sample entry, a 4-byte code, similar to a FOURCC, defines the format structure.</span></span>

<span data-ttu-id="085ac-155">此擴充性表示 MPEG 4 檔案來源無法辨識每個可能的格式描述。</span><span class="sxs-lookup"><span data-stu-id="085ac-155">This extensibility means the MPEG-4 file source cannot recognize every possible format description.</span></span> <span data-ttu-id="085ac-156">相反地，在建立資料流程的媒體類型時，它會採用兩層式的方法。</span><span class="sxs-lookup"><span data-stu-id="085ac-156">Instead, it takes a two-tiered approach when creating media types for the streams.</span></span> <span data-ttu-id="085ac-157">每個媒體類型至少包含下列屬性。</span><span class="sxs-lookup"><span data-stu-id="085ac-157">At a minimum, every media type contains the following attributes.</span></span>



| <span data-ttu-id="085ac-158">屬性</span><span class="sxs-lookup"><span data-stu-id="085ac-158">Attribute</span></span>                                                                     | <span data-ttu-id="085ac-159">描述</span><span class="sxs-lookup"><span data-stu-id="085ac-159">Description</span></span>                                                    |
|-------------------------------------------------------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="085ac-160">**MF \_ MT \_ 主要 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="085ac-160">**MF\_MT\_MAJOR\_TYPE**</span></span>](mf-mt-major-type-attribute.md)                     | <span data-ttu-id="085ac-161">等於 **MFMediaType \_ 音訊** 或 **MFMediaType \_ 影片**。</span><span class="sxs-lookup"><span data-stu-id="085ac-161">Equal to **MFMediaType\_Audio** or **MFMediaType\_Video**.</span></span>     |
| [<span data-ttu-id="085ac-162">**MF \_ MT \_ 子類型**</span><span class="sxs-lookup"><span data-stu-id="085ac-162">**MF\_MT\_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)                            | <span data-ttu-id="085ac-163">指定資料流程子類型。</span><span class="sxs-lookup"><span data-stu-id="085ac-163">Specifies the stream subtype.</span></span>                                  |
| [<span data-ttu-id="085ac-164">MF \_ MT \_ MPEG4 \_ 範例 \_ 說明</span><span class="sxs-lookup"><span data-stu-id="085ac-164">MF\_MT\_MPEG4\_SAMPLE\_DESCRIPTION</span></span>](mf-mt-mpeg4-sample-description.md)      | <span data-ttu-id="085ac-165">以二進位 blob 的形式包含完整的範例描述方塊。</span><span class="sxs-lookup"><span data-stu-id="085ac-165">Contains the complete sample description box as a binary blob.</span></span> |
| [<span data-ttu-id="085ac-166">MF \_ MT \_ MPEG4 \_ 目前的 \_ 範例 \_ 專案</span><span class="sxs-lookup"><span data-stu-id="085ac-166">MF\_MT\_MPEG4\_CURRENT\_SAMPLE\_ENTRY</span></span>](mf-mt-mpeg4-current-sample-entry.md) | <span data-ttu-id="085ac-167">在 [範例描述] 方塊中指定目前的專案。</span><span class="sxs-lookup"><span data-stu-id="085ac-167">Specifies the current entry in the sample description box.</span></span>     |



 

<span data-ttu-id="085ac-168">MPEG 4 檔案來源會辨識某些範例專案類型。</span><span class="sxs-lookup"><span data-stu-id="085ac-168">The MPEG-4 file source recognizes some sample entry types.</span></span> <span data-ttu-id="085ac-169">針對這些專案，它可以剖析格式結構並建立完整的媒體類型，以及描述格式詳細資料的其他屬性。</span><span class="sxs-lookup"><span data-stu-id="085ac-169">For these entries, it can parse the format structure and create a complete media type, with additional attributes that describe the format details.</span></span> <span data-ttu-id="085ac-170">請參閱 [媒體類型屬性](media-type-attributes.md)。</span><span class="sxs-lookup"><span data-stu-id="085ac-170">See [Media Type Attributes](media-type-attributes.md).</span></span>

<span data-ttu-id="085ac-171">MPEG 4 檔案來源可以剖析下列範例專案。</span><span class="sxs-lookup"><span data-stu-id="085ac-171">The MPEG-4 file source can parse the following sample entries.</span></span>



| <span data-ttu-id="085ac-172">範例輸入碼</span><span class="sxs-lookup"><span data-stu-id="085ac-172">Sample entry code</span></span> | <span data-ttu-id="085ac-173">主要類型</span><span class="sxs-lookup"><span data-stu-id="085ac-173">Major type</span></span> | <span data-ttu-id="085ac-174">Subtype</span><span class="sxs-lookup"><span data-stu-id="085ac-174">Subtype</span></span>                                                               | <span data-ttu-id="085ac-175">描述</span><span class="sxs-lookup"><span data-stu-id="085ac-175">Description</span></span>                                         | <span data-ttu-id="085ac-176">附註</span><span class="sxs-lookup"><span data-stu-id="085ac-176">Notes</span></span>                                                                                                                                                                                            |
|-------------------|------------|-----------------------------------------------------------------------|-----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="085ac-177">alaw</span><span class="sxs-lookup"><span data-stu-id="085ac-177">'alaw'</span></span>            | <span data-ttu-id="085ac-178">音訊</span><span class="sxs-lookup"><span data-stu-id="085ac-178">Audio</span></span>      | <span data-ttu-id="085ac-179">**WAVE \_ 格式 \_ ALAW**</span><span class="sxs-lookup"><span data-stu-id="085ac-179">**WAVE\_FORMAT\_ALAW**</span></span>                                                | <span data-ttu-id="085ac-180">定律編碼</span><span class="sxs-lookup"><span data-stu-id="085ac-180">A-law coding</span></span>                                        |                                                                                                                                                                                                  |
| <span data-ttu-id="085ac-181">幅</span><span class="sxs-lookup"><span data-stu-id="085ac-181">'jpeg'</span></span>            | <span data-ttu-id="085ac-182">影片</span><span class="sxs-lookup"><span data-stu-id="085ac-182">Video</span></span>      | <span data-ttu-id="085ac-183">**MFVideoFormat \_ MJPG**</span><span class="sxs-lookup"><span data-stu-id="085ac-183">**MFVideoFormat\_MJPG**</span></span>                                               | <span data-ttu-id="085ac-184">相片-JPEG 資料流程</span><span class="sxs-lookup"><span data-stu-id="085ac-184">Photo-JPEG stream</span></span>                                   | <span data-ttu-id="085ac-185">QuickTime 容器格式也支援具有 ' mjpa ' 或 ' mjpb ' 專案的動畫 JPEG 串流，但 MPEG 4 檔案來源並不提供這些類型的完整媒體類型。</span><span class="sxs-lookup"><span data-stu-id="085ac-185">The QuickTime container format also supports motion JPEG streams with 'mjpa' or 'mjpb' entries, but the MPEG-4 file source does not provide a complete media type for those types.</span></span>               |
| <span data-ttu-id="085ac-186">avc1</span><span class="sxs-lookup"><span data-stu-id="085ac-186">'avc1'</span></span>            | <span data-ttu-id="085ac-187">影片</span><span class="sxs-lookup"><span data-stu-id="085ac-187">Video</span></span>      | <span data-ttu-id="085ac-188">**MFVideoFormat \_ H264**</span><span class="sxs-lookup"><span data-stu-id="085ac-188">**MFVideoFormat\_H264**</span></span>                                               | <span data-ttu-id="085ac-189">H.264 影片</span><span class="sxs-lookup"><span data-stu-id="085ac-189">H.264 video</span></span>                                         |                                                                                                                                                                                                  |
| <span data-ttu-id="085ac-190">mp4a</span><span class="sxs-lookup"><span data-stu-id="085ac-190">'mp4a'</span></span>            | <span data-ttu-id="085ac-191">音訊</span><span class="sxs-lookup"><span data-stu-id="085ac-191">Audio</span></span>      | <span data-ttu-id="085ac-192">**MFAudioFormat \_ AAC**</span><span class="sxs-lookup"><span data-stu-id="085ac-192">**MFAudioFormat\_AAC**</span></span><br/> <span data-ttu-id="085ac-193">**MFAudioFormat \_ MP3**</span><span class="sxs-lookup"><span data-stu-id="085ac-193">**MFAudioFormat\_MP3**</span></span><br/>   | <span data-ttu-id="085ac-194">AAC 或 MP3</span><span class="sxs-lookup"><span data-stu-id="085ac-194">AAC or MP3</span></span>                                          | <span data-ttu-id="085ac-195">' Mp4a ' 專案可以描述其他 MPEG 音訊格式，但 MPEG 4 檔案來源不會剖析格式結構。</span><span class="sxs-lookup"><span data-stu-id="085ac-195">The 'mp4a' entry can describe other MPEG audio formats, but the MPEG-4 file source does not parse the format structure.</span></span>                                                                          |
| <span data-ttu-id="085ac-196">'mp4v'</span><span class="sxs-lookup"><span data-stu-id="085ac-196">'mp4v'</span></span>            | <span data-ttu-id="085ac-197">影片</span><span class="sxs-lookup"><span data-stu-id="085ac-197">Video</span></span>      | <span data-ttu-id="085ac-198">**MFVideoFormat \_ M4S2**</span><span class="sxs-lookup"><span data-stu-id="085ac-198">**MFVideoFormat\_M4S2**</span></span><br/> <span data-ttu-id="085ac-199">**MFVideoFormat \_ MP4V**</span><span class="sxs-lookup"><span data-stu-id="085ac-199">**MFVideoFormat\_MP4V**</span></span><br/> | <span data-ttu-id="085ac-200">MPEG 4 第2部分</span><span class="sxs-lookup"><span data-stu-id="085ac-200">MPEG-4 part 2</span></span>                                       | <span data-ttu-id="085ac-201">**MFVideoFormat \_M4S2** 可用於 mpeg-2 第2部分的簡單設定檔。</span><span class="sxs-lookup"><span data-stu-id="085ac-201">**MFVideoFormat\_M4S2** is used for MPEG-4 part 2 Simple Profile.</span></span><br/> <span data-ttu-id="085ac-202">**MFVideoFormat \_MP4V** 適用于所有其他 MPEG 4 第2部分的設定檔，包括 Advanced Simple Profile。</span><span class="sxs-lookup"><span data-stu-id="085ac-202">**MFVideoFormat\_MP4V** is used for all other MPEG-4 part 2 profiles, including Advanced Simple Profile.</span></span><br/> |
| <span data-ttu-id="085ac-203">原始</span><span class="sxs-lookup"><span data-stu-id="085ac-203">'raw '</span></span>            | <span data-ttu-id="085ac-204">音訊</span><span class="sxs-lookup"><span data-stu-id="085ac-204">Audio</span></span>      | <span data-ttu-id="085ac-205">**MFAudioFormat \_ PCM**</span><span class="sxs-lookup"><span data-stu-id="085ac-205">**MFAudioFormat\_PCM**</span></span>                                                | <span data-ttu-id="085ac-206">8位 PCM 音訊</span><span class="sxs-lookup"><span data-stu-id="085ac-206">8-bit PCM audio</span></span>                                     |                                                                                                                                                                                                  |
| <span data-ttu-id="085ac-207">'sowt'</span><span class="sxs-lookup"><span data-stu-id="085ac-207">'sowt'</span></span>            | <span data-ttu-id="085ac-208">音訊</span><span class="sxs-lookup"><span data-stu-id="085ac-208">Audio</span></span>      | <span data-ttu-id="085ac-209">**MFAudioFormat \_ PCM**</span><span class="sxs-lookup"><span data-stu-id="085ac-209">**MFAudioFormat\_PCM**</span></span>                                                | <span data-ttu-id="085ac-210">16位位元組由小到大 PCM 音訊</span><span class="sxs-lookup"><span data-stu-id="085ac-210">16-bit little-endian PCM audio</span></span>                      |                                                                                                                                                                                                  |
| <span data-ttu-id="085ac-211">補</span><span class="sxs-lookup"><span data-stu-id="085ac-211">'twos'</span></span>            | <span data-ttu-id="085ac-212">音訊</span><span class="sxs-lookup"><span data-stu-id="085ac-212">Audio</span></span>      | <span data-ttu-id="085ac-213">**MFAudioFormat \_ PCM**</span><span class="sxs-lookup"><span data-stu-id="085ac-213">**MFAudioFormat\_PCM**</span></span>                                                | <span data-ttu-id="085ac-214">16位的位元組由大到小 PCM 音訊</span><span class="sxs-lookup"><span data-stu-id="085ac-214">16-bit big-endian PCM audio</span></span>                         | <span data-ttu-id="085ac-215">MPEG-2 檔案來源會將音訊資料轉換為位元組由小到小的格式。</span><span class="sxs-lookup"><span data-stu-id="085ac-215">The MPEG-4 file source converts the audio data to little-endian format.</span></span>                                                                                                                          |
| <span data-ttu-id="085ac-216">ulaw</span><span class="sxs-lookup"><span data-stu-id="085ac-216">'ulaw'</span></span>            | <span data-ttu-id="085ac-217">音訊</span><span class="sxs-lookup"><span data-stu-id="085ac-217">Audio</span></span>      | <span data-ttu-id="085ac-218">**WAVE \_ 格式 \_ MULAW**</span><span class="sxs-lookup"><span data-stu-id="085ac-218">**WAVE\_FORMAT\_MULAW**</span></span>                                               | <span data-ttu-id="085ac-219">μ定律編碼</span><span class="sxs-lookup"><span data-stu-id="085ac-219">μ-law coding</span></span>                                        |                                                                                                                                                                                                  |
| <span data-ttu-id="085ac-220">' vc-1 '</span><span class="sxs-lookup"><span data-stu-id="085ac-220">'vc-1'</span></span>            | <span data-ttu-id="085ac-221">影片</span><span class="sxs-lookup"><span data-stu-id="085ac-221">Video</span></span>      | <span data-ttu-id="085ac-222">**MFVideoFormat \_ WVC1**</span><span class="sxs-lookup"><span data-stu-id="085ac-222">**MFVideoFormat\_WVC1**</span></span>                                               | <span data-ttu-id="085ac-223">VC-1 影片</span><span class="sxs-lookup"><span data-stu-id="085ac-223">VC-1 video</span></span>                                          |                                                                                                                                                                                                  |
| <span data-ttu-id="085ac-224">以上</span><span class="sxs-lookup"><span data-stu-id="085ac-224">'NONE'</span></span>            | <span data-ttu-id="085ac-225">音訊</span><span class="sxs-lookup"><span data-stu-id="085ac-225">Audio</span></span>      | <span data-ttu-id="085ac-226">**MFAudioFormat \_ PCM**</span><span class="sxs-lookup"><span data-stu-id="085ac-226">**MFAudioFormat\_PCM**</span></span>                                                | <span data-ttu-id="085ac-227">8位或16位的位元組由大到小 PCM 音訊</span><span class="sxs-lookup"><span data-stu-id="085ac-227">8-bit or 16-bit big-endian PCM audio</span></span>                | <span data-ttu-id="085ac-228">MPEG-2 檔案來源會將音訊資料轉換為位元組由小到小的格式。</span><span class="sxs-lookup"><span data-stu-id="085ac-228">The MPEG-4 file source converts the audio data to little-endian format.</span></span>                                                                                                                          |
| <span data-ttu-id="085ac-229">0x00000000</span><span class="sxs-lookup"><span data-stu-id="085ac-229">0x00000000</span></span>        | <span data-ttu-id="085ac-230">音訊</span><span class="sxs-lookup"><span data-stu-id="085ac-230">Audio</span></span>      | <span data-ttu-id="085ac-231">**MFAudioFormat \_ PCM**</span><span class="sxs-lookup"><span data-stu-id="085ac-231">**MFAudioFormat\_PCM**</span></span>                                                | <span data-ttu-id="085ac-232">8位或16位的位元組由大到小 PCM 音訊</span><span class="sxs-lookup"><span data-stu-id="085ac-232">8-bit or 16-bit big-endian PCM audio</span></span>                | <span data-ttu-id="085ac-233">MPEG-2 檔案來源會將音訊資料轉換為位元組由小到小的格式。</span><span class="sxs-lookup"><span data-stu-id="085ac-233">The MPEG-4 file source converts the audio data to little-endian format.</span></span>                                                                                                                          |
| <span data-ttu-id="085ac-234">0x6d730002</span><span class="sxs-lookup"><span data-stu-id="085ac-234">0x6d730002</span></span>        | <span data-ttu-id="085ac-235">音訊</span><span class="sxs-lookup"><span data-stu-id="085ac-235">Audio</span></span>      | <span data-ttu-id="085ac-236">**WAVE \_ 格式 \_ ADPCM**</span><span class="sxs-lookup"><span data-stu-id="085ac-236">**WAVE\_FORMAT\_ADPCM**</span></span>                                               | <span data-ttu-id="085ac-237">適應性差異脈衝程式碼 (ADPCM) </span><span class="sxs-lookup"><span data-stu-id="085ac-237">Adaptive Differential Pulse Code Modulation (ADPCM)</span></span> |                                                                                                                                                                                                  |
| <span data-ttu-id="085ac-238">0x6d730011</span><span class="sxs-lookup"><span data-stu-id="085ac-238">0x6d730011</span></span>        | <span data-ttu-id="085ac-239">音訊</span><span class="sxs-lookup"><span data-stu-id="085ac-239">Audio</span></span>      | <span data-ttu-id="085ac-240">**WAVE \_ 格式 \_ IMA \_ ADPCM**</span><span class="sxs-lookup"><span data-stu-id="085ac-240">**WAVE\_FORMAT\_IMA\_ADPCM**</span></span>                                          | <span data-ttu-id="085ac-241">ADPCM</span><span class="sxs-lookup"><span data-stu-id="085ac-241">ADPCM</span></span>                                               |                                                                                                                                                                                                  |



 

<span data-ttu-id="085ac-242">針對上表中未顯示的任何其他程式碼，MPEG 檔來源會設定子類型，如下所示：</span><span class="sxs-lookup"><span data-stu-id="085ac-242">For any other codes not shown in the previous table, the MPEG-4 file source sets the subtype as follows:</span></span>

1.  <span data-ttu-id="085ac-243">*子類型* = MFMPEG4Format \_ 基底</span><span class="sxs-lookup"><span data-stu-id="085ac-243">*subtype* = MFMPEG4Format\_Base</span></span>
2.  <span data-ttu-id="085ac-244">*子類型*。Data1 = 範例輸入碼</span><span class="sxs-lookup"><span data-stu-id="085ac-244">*subtype*.Data1 = sample entry code</span></span>

<span data-ttu-id="085ac-245">針對未顯示在表格中的程式碼，解碼器必須使用 [MF \_ MT \_ MPEG4 \_ 範例 \_ 描述](mf-mt-mpeg4-sample-description.md) 屬性來剖析範例描述方塊。</span><span class="sxs-lookup"><span data-stu-id="085ac-245">For codes not shown in the table, a decoder must use the [MF\_MT\_MPEG4\_SAMPLE\_DESCRIPTION](mf-mt-mpeg4-sample-description.md) attribute to parse the sample description box.</span></span>

<span data-ttu-id="085ac-246">如需範例輸入碼清單以及相關規格的連結，請參閱「數量的」 [註冊授權](https://mp4ra.org) 網站。</span><span class="sxs-lookup"><span data-stu-id="085ac-246">For a list of sample entry codes and links to relevant specifications, see the ['MP4' Registration Authority](https://mp4ra.org) website.</span></span>

## <a name="limitations"></a><span data-ttu-id="085ac-247">限制</span><span class="sxs-lookup"><span data-stu-id="085ac-247">Limitations</span></span>

<span data-ttu-id="085ac-248">MPEG-2 檔案來源不支援下列檔的下列功能：</span><span class="sxs-lookup"><span data-stu-id="085ac-248">The MPEG-4 file source does not support the following features of MP4 files:</span></span>

-   <span data-ttu-id="085ac-249">外部追蹤。</span><span class="sxs-lookup"><span data-stu-id="085ac-249">External tracks.</span></span>
-   <span data-ttu-id="085ac-250">電影片段 ( [moof] 或 [mfra] 方塊) 。</span><span class="sxs-lookup"><span data-stu-id="085ac-250">Movie fragments ('moof' or 'mfra' boxes).</span></span> <span data-ttu-id="085ac-251">Windows 8 支援 ' moof '。</span><span class="sxs-lookup"><span data-stu-id="085ac-251">'moof' is supported in Windows 8.</span></span>
-   <span data-ttu-id="085ac-252">資料流程處理的簡報。</span><span class="sxs-lookup"><span data-stu-id="085ac-252">Streamed presentations.</span></span> <span data-ttu-id="085ac-253">MPEG-2 檔案來源會以無訊息方式忽略提示追蹤。</span><span class="sxs-lookup"><span data-stu-id="085ac-253">The MPEG-4 file source silently ignores hint tracks.</span></span>
-   <span data-ttu-id="085ac-254">依 SMPTE 時間碼搜尋。</span><span class="sxs-lookup"><span data-stu-id="085ac-254">Seeking by SMPTE time code.</span></span>
-   <span data-ttu-id="085ac-255">壓縮 ( ' cmov ' ) 原子。</span><span class="sxs-lookup"><span data-stu-id="085ac-255">Compressed ('cmov') atoms.</span></span>

<span data-ttu-id="085ac-256">僅支援影片和音訊串流。</span><span class="sxs-lookup"><span data-stu-id="085ac-256">Only video and audio streams are supported.</span></span> <span data-ttu-id="085ac-257">任何包含其他資料流程類型的追蹤都會以無訊息方式略過。</span><span class="sxs-lookup"><span data-stu-id="085ac-257">Any tracks that contain other stream types are silently ignored.</span></span> <span data-ttu-id="085ac-258">媒體資料必須放在 ' mdat ' 原子內。</span><span class="sxs-lookup"><span data-stu-id="085ac-258">Media data must be placed inside 'mdat' atoms.</span></span>

<span data-ttu-id="085ac-259">如果已安裝 Windows Vista 的平臺更新補充，則會在 Windows Vista 上提供 MPEG-2 檔案來源，但只能使用 [來源讀取器](source-reader.md)在 windows vista 上進行存取。</span><span class="sxs-lookup"><span data-stu-id="085ac-259">If Platform Update Supplement for Windows Vista is installed, the MPEG-4 file source is available on Windows Vista, but is accessible on Windows Vista only by using the [Source Reader](source-reader.md).</span></span>

## <a name="windows-8-updates-to-mpeg-4-source-and-sink"></a><span data-ttu-id="085ac-260">Windows 8 更新至 MPEG-2 來源和接收</span><span class="sxs-lookup"><span data-stu-id="085ac-260">Windows 8 updates to MPEG-4 source and sink</span></span>

-   <span data-ttu-id="085ac-261">Windows 8 MPEG-2 來源和接收中新增的旋轉讀取和寫入支援。</span><span class="sxs-lookup"><span data-stu-id="085ac-261">Rotation read and write support added in Windows 8 MPEG-4 source and sink.</span></span> <span data-ttu-id="085ac-262">Windows 7 MPEG-2 來源和接收中不支援此功能。</span><span class="sxs-lookup"><span data-stu-id="085ac-262">This is not supported in the Windows 7 MPEG-4 source and sink.</span></span>

    <span data-ttu-id="085ac-263">MPEG 4 來源會讀取作用中影片播放軌的旋轉角度，作為從 ' mvhd ' 和 ' tkhd ' 旋轉角度的總和。</span><span class="sxs-lookup"><span data-stu-id="085ac-263">MPEG-4 source reads the rotation angle for an active video track as the sum of the rotation angle from ‘mvhd’ and from ‘tkhd’.</span></span>

    <span data-ttu-id="085ac-264">Microsoft MPEG-2 接收會在 ' tkhd ' 中寫入旋轉角度，但會在 ' mvhd ' 中寫入0度的 (識別) 矩陣。</span><span class="sxs-lookup"><span data-stu-id="085ac-264">Microsoft MPEG-4 sink writes the rotation angle in ‘tkhd’ but writes 0 degree (identity) matrix in ‘mvhd’.</span></span> <span data-ttu-id="085ac-265">請注意，Microsoft MPEG 4 接收器只支援單一影片播放軌。</span><span class="sxs-lookup"><span data-stu-id="085ac-265">Note, Microsoft MPEG-4 sink only supports single video track.</span></span>

    <span data-ttu-id="085ac-266">IPropertyStore 只會讀取第一個影片播放軌的旋轉角度，作為從 ' mvhd ' 和 ' tkhd ' 旋轉角度的總和。</span><span class="sxs-lookup"><span data-stu-id="085ac-266">IPropertyStore reads the rotation angle for only the first video track as the sum of the rotation angle from ‘mvhd’ and from ‘tkhd’.</span></span>

    <span data-ttu-id="085ac-267">IPropertyStore 只會在旋轉角度根據 ' mvhd ' 中的旋轉角度（如果有的話）調整旋轉角度之後，才在 ' tkhd ' 中寫入第一個影片播放軌的旋轉角度。</span><span class="sxs-lookup"><span data-stu-id="085ac-267">IPropertyStore writes the rotation angle for only the first video track in ‘tkhd’ after the rotation angle is adjusted according to the rotation angle in ‘mvhd’, if it exists.</span></span>

-   <span data-ttu-id="085ac-268">Windows 8 MPEG-2 來源和接收中支援 ' moof ' )  ( 的電影片段，但 ' mfra ' 不支援。</span><span class="sxs-lookup"><span data-stu-id="085ac-268">Movie fragments ('moof') is supported in Windows 8 MPEG-4 source and sink, but 'mfra' is not.</span></span>
-   <span data-ttu-id="085ac-269">Windows 8 的 MPEG-2 來源支援 .h。</span><span class="sxs-lookup"><span data-stu-id="085ac-269">H.263 is supported in Windows 8 MPEG-4 source.</span></span>

    <span data-ttu-id="085ac-270">MPEG 4 來源現在會將 MPEG-2 檔案格式的兩個 fourcc ' h263 ' 和 ' 263 ' 對應到 **MFVideoFormat \_ h263** 的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="085ac-270">MPEG-4 source now maps two fourcc’s of ‘h263’ and ‘s263’ in MPEG-4 file format to the media type of **MFVideoFormat\_H263**.</span></span>

-   <span data-ttu-id="085ac-271">在 Windows 8 MPEG-2 來源的 MJPEG 中新增了更多 fourcc 支援。</span><span class="sxs-lookup"><span data-stu-id="085ac-271">More fourcc support added for MJPEG in Windows 8 MPEG-4 source.</span></span>

    <span data-ttu-id="085ac-272">MPEG 4 來源會將 ' dmb1 ' 的 foucc 對應至 **MFVideoFormat \_ MJPG** 的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="085ac-272">MPEG-4 source maps foucc of ‘dmb1’ to the media type of **MFVideoFormat\_MJPG**.</span></span>

-   <span data-ttu-id="085ac-273">Windows 8 MPEG-2 來源中新增的漢字中繼資料支援。</span><span class="sxs-lookup"><span data-stu-id="085ac-273">Furigana metadata support added in Windows 8 MPEG-4 source.</span></span>

    <span data-ttu-id="085ac-274">MPEG-2 來源會從 ' soal '、' soar '、' soaa '、' sonm ' 和 ' soco ' 讀取中繼資料。</span><span class="sxs-lookup"><span data-stu-id="085ac-274">MPEG-4 source reads Furigana metadata from ’soal’, ‘soar’, ‘soaa’, ‘sonm’, and ‘soco’.</span></span> <span data-ttu-id="085ac-275">IPropertyStore 會透過一組對應的 PKEYs 來讀取 Furignana 中繼資料。</span><span class="sxs-lookup"><span data-stu-id="085ac-275">IPropertyStore reads Furignana metadata through the set of corresponding PKEYs.</span></span>

    <span data-ttu-id="085ac-276">下表顯示 shell 正式名稱、屬性索引鍵，以及 MPEG-2 檔案格式的 box/標記識別項之間的對應。</span><span class="sxs-lookup"><span data-stu-id="085ac-276">The following table shows the mapping between the shell canonical name, the property key, and the box/tag ID in MPEG-4 file format.</span></span>

    

    | <span data-ttu-id="085ac-277">欄位</span><span class="sxs-lookup"><span data-stu-id="085ac-277">Field</span></span>                                | <span data-ttu-id="085ac-278">屬性索引鍵</span><span class="sxs-lookup"><span data-stu-id="085ac-278">Property Key</span></span>                         | <span data-ttu-id="085ac-279">標記/Box 識別碼</span><span class="sxs-lookup"><span data-stu-id="085ac-279">Tag/Box ID</span></span> |
    |--------------------------------------|--------------------------------------|------------|
    | <span data-ttu-id="085ac-280">AlbumTitleSortOverride</span><span class="sxs-lookup"><span data-stu-id="085ac-280">System.Music.AlbumTitleSortOverride</span></span>  | <span data-ttu-id="085ac-281">PKEY \_ 音樂 \_ AlbumTitleSortOverride</span><span class="sxs-lookup"><span data-stu-id="085ac-281">PKEY\_Music\_AlbumTitleSortOverride</span></span>  | <span data-ttu-id="085ac-282">soal</span><span class="sxs-lookup"><span data-stu-id="085ac-282">soal</span></span>       |
    | <span data-ttu-id="085ac-283">ArtistSortOverride</span><span class="sxs-lookup"><span data-stu-id="085ac-283">System.Music.ArtistSortOverride</span></span>      | <span data-ttu-id="085ac-284">PKEY \_ 音樂 \_ ArtistSortOverride</span><span class="sxs-lookup"><span data-stu-id="085ac-284">PKEY\_Music\_ArtistSortOverride</span></span>      | <span data-ttu-id="085ac-285">飆升</span><span class="sxs-lookup"><span data-stu-id="085ac-285">soar</span></span>       |
    | <span data-ttu-id="085ac-286">AlbumArtistSortOverride</span><span class="sxs-lookup"><span data-stu-id="085ac-286">System.Music.AlbumArtistSortOverride</span></span> | <span data-ttu-id="085ac-287">PKEY \_ 音樂 \_ AlbumArtistSortOverride</span><span class="sxs-lookup"><span data-stu-id="085ac-287">PKEY\_Music\_AlbumArtistSortOverride</span></span> | <span data-ttu-id="085ac-288">soaa</span><span class="sxs-lookup"><span data-stu-id="085ac-288">soaa</span></span>       |
    | <span data-ttu-id="085ac-289">System. TitleSortOverride</span><span class="sxs-lookup"><span data-stu-id="085ac-289">System.TitleSortOverride</span></span>             | <span data-ttu-id="085ac-290">PKEY \_ TitleSortOverride</span><span class="sxs-lookup"><span data-stu-id="085ac-290">PKEY \_TitleSortOverride</span></span>             | <span data-ttu-id="085ac-291">sonm</span><span class="sxs-lookup"><span data-stu-id="085ac-291">sonm</span></span>       |
    | <span data-ttu-id="085ac-292">ComposerSortOverride</span><span class="sxs-lookup"><span data-stu-id="085ac-292">System.Music.ComposerSortOverride</span></span>    | <span data-ttu-id="085ac-293">PKEY \_ 音樂 \_ ComposerSortOverride</span><span class="sxs-lookup"><span data-stu-id="085ac-293">PKEY\_Music\_ComposerSortOverride</span></span>    | <span data-ttu-id="085ac-294">soco</span><span class="sxs-lookup"><span data-stu-id="085ac-294">soco</span></span>       |

    

     

-   <span data-ttu-id="085ac-295">Windows 8 MPEG-2 來源中新增了身歷聲 3D atom 支援。</span><span class="sxs-lookup"><span data-stu-id="085ac-295">Stereo 3D atom support added in Windows 8 MPEG-4 source.</span></span>

-   <span data-ttu-id="085ac-296">Windows 8 的 MPEG-2 來源和接收中新增了 AC3 和 DD + 支援。</span><span class="sxs-lookup"><span data-stu-id="085ac-296">AC3 and DD+ support added in Windows 8 MPEG-4 source and sink.</span></span>
-   <span data-ttu-id="085ac-297">針對非 fragmental 的，Windows 8 的 MPEG-2 接收器支援大於 4 gb 的檔案 (GB) 。</span><span class="sxs-lookup"><span data-stu-id="085ac-297">Files larger than 4 gigabytes (GB) are supported in Windows 8 MPEG-4 sink for non-fragmental MP4.</span></span>
-   <span data-ttu-id="085ac-298">Windows 8 的 MPEG-2 來源已優化清除。</span><span class="sxs-lookup"><span data-stu-id="085ac-298">Scrubbing has been optimized in Windows 8 MPEG-4 source.</span></span>

    <span data-ttu-id="085ac-299">為了減少延遲，特定搜尋位置的兩個最接近主要畫面格的資訊會透過 [**IMFSeekInfo：： GetNearestKeyFrames**](/windows/desktop/api/mfidl/nf-mfidl-imfseekinfo-getnearestkeyframes)公開。</span><span class="sxs-lookup"><span data-stu-id="085ac-299">To reduce latency, information for the two nearest key frames for a particular seek position are exposed through [**IMFSeekInfo::GetNearestKeyFrames**](/windows/desktop/api/mfidl/nf-mfidl-imfseekinfo-getnearestkeyframes).</span></span> <span data-ttu-id="085ac-300">由於主要畫面格沒有相依的框架，因此只會在解碼一個畫面格之後呈現畫面格。</span><span class="sxs-lookup"><span data-stu-id="085ac-300">Since the key frame does not have dependent frames, it presents the frame after decoding only one frame.</span></span> <span data-ttu-id="085ac-301">使用 [**IMFGetService：： GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) 透過媒體來源、管線或應用程式取得這個介面。</span><span class="sxs-lookup"><span data-stu-id="085ac-301">Use [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) to obtain this interface through the media source, pipeline, or application.</span></span>

    <span data-ttu-id="085ac-302">在 MPEG 4 來源中將速率設定為零。</span><span class="sxs-lookup"><span data-stu-id="085ac-302">Set rate to zero in MPEG-4 source.</span></span> <span data-ttu-id="085ac-303">當管線處於清除模式時，速率為零。</span><span class="sxs-lookup"><span data-stu-id="085ac-303">When the pipeline is in scrubbing mode, the rate is zero.</span></span>

-   <span data-ttu-id="085ac-304">您可以將 SPS 和 PPS 儲存在 MPEG 4 接收的範例資料中。</span><span class="sxs-lookup"><span data-stu-id="085ac-304">SPS and PPS can be stored in sample data in MPEG-4 sink.</span></span>

    <span data-ttu-id="085ac-305">[MF \_在 MPEG 4 接收上的 MPEG4SINK \_ SPSPPS \_ 傳遞](mf-mpeg4sink-spspps-passthrough.md) 屬性定義為允許將 SPS 和 PPS 儲存在一起， (h.264 video 資料) 的輸入範例。</span><span class="sxs-lookup"><span data-stu-id="085ac-305">[MF\_MPEG4SINK\_SPSPPS\_PASSTHROUGH](mf-mpeg4sink-spspps-passthrough.md) attribute on MPEG-4 sink is defined to allow SPS’s and PPS’s to be saved together with input samples (H.264 video data).</span></span> <span data-ttu-id="085ac-306">產生的已產生的等式剪輯可由 Windows 7 MPEG-2 來源與其他專案播放。</span><span class="sxs-lookup"><span data-stu-id="085ac-306">The produced mp4 clips are play-able by Windows 7 MPEG-4 source and others.</span></span>

-   <span data-ttu-id="085ac-307">您可以從 MPEG 接收器的輸入範例中解壓縮 SPS 和 PPS。</span><span class="sxs-lookup"><span data-stu-id="085ac-307">SPS and PPS can be extracted from input samples in MPEG-4 sink.</span></span>

    <span data-ttu-id="085ac-308">當 SP 和 PPS 未設定在 MPEG 接收器的輸入媒體類型上的 [MF \_ MT \_ MPEG \_ 序列 \_ 標頭](mf-mt-mpeg-sequence-header-attribute.md) 時，mpeg 4 接收會嘗試從輸入範例中解壓縮 sps 和 pps。</span><span class="sxs-lookup"><span data-stu-id="085ac-308">When SPS and PPS are not set through [MF\_MT\_MPEG\_SEQUENCE\_HEADER](mf-mt-mpeg-sequence-header-attribute.md) on input media type of the MPEG-4 sink, MPEG-4 sink will try to extract SPS and PPS from input samples.</span></span> <span data-ttu-id="085ac-309">MPEG-2 接收會忽略任何輸入範例，直到它找到第一個 SPS 和 PPS 為止，因為沒有 SPS 和 PPS 的所有輸入範例都不能進行解碼。</span><span class="sxs-lookup"><span data-stu-id="085ac-309">MPEG-4 sink ignores any input samples until it finds the first SPS and PPS, because all input samples without SPS and PPS are not decode-able.</span></span>

-   <span data-ttu-id="085ac-310">AVC 設定記錄中的3D 資訊支援非 fragmental 的配置。</span><span class="sxs-lookup"><span data-stu-id="085ac-310">3D information in AVC configuration record is supported for non-fragmental MP4.</span></span>
-   <span data-ttu-id="085ac-311">NALU 長度會針對 h.264 壓縮範例公開，以優化 h.264 VLD DXVA 解碼。</span><span class="sxs-lookup"><span data-stu-id="085ac-311">NALU length is exposed for H.264 compressed samples to optimize H.264 VLD DXVA decoding.</span></span>

    <span data-ttu-id="085ac-312">MPEG-2 來源集會設定 **MFVideoFormat \_ H264** 或 **MFVideoFormat \_ H264** 輸出媒體類型的 [MF \_ NALU \_ 長度 \_](mf-nalu-length-set.md) 。</span><span class="sxs-lookup"><span data-stu-id="085ac-312">MPEG-4 source sets [MF\_NALU\_LENGTH\_SET](mf-nalu-length-set.md) on the output media type of **MFVideoFormat\_H264** or **MFVideoFormat\_h264**.</span></span> <span data-ttu-id="085ac-313">它會在每個輸出範例上設定 [MF \_ NALU \_ 長度 \_ 資訊](mf-nalu-length-information.md) 的 blob，其中有一個壓縮範例中不同 NALU 的四位元組 NALU 長度。</span><span class="sxs-lookup"><span data-stu-id="085ac-313">It sets the blob of [MF\_NALU\_LENGTH\_INFORMATION](mf-nalu-length-information.md) on each output sample, with four-byte NALU length for different NALU’s in one compressed sample.</span></span>

-   <span data-ttu-id="085ac-314">針對在 ADTS 中的的 MPEG2 音訊新增支援。</span><span class="sxs-lookup"><span data-stu-id="085ac-314">Support added for MPEG2 ADTS audio in MP4 source.</span></span>

## <a name="related-topics"></a><span data-ttu-id="085ac-315">相關主題</span><span class="sxs-lookup"><span data-stu-id="085ac-315">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="085ac-316">媒體來源和接收</span><span class="sxs-lookup"><span data-stu-id="085ac-316">Media Sources and Sinks</span></span>](media-sources-and-sinks.md)
</dt> <dt>

[<span data-ttu-id="085ac-317">媒體基礎中的 MPEG 4 支援</span><span class="sxs-lookup"><span data-stu-id="085ac-317">MPEG-4 Support in Media Foundation</span></span>](mpeg-4-support-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="085ac-318">媒體基礎中支援的媒體格式</span><span class="sxs-lookup"><span data-stu-id="085ac-318">Supported Media Formats in Media Foundation</span></span>](supported-media-formats-in-media-foundation.md)
</dt> </dl>

 

 




