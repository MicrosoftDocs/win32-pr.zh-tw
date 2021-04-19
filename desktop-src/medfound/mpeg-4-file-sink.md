---
description: MPEG-2 檔案接收會建立檔案。
ms.assetid: 069b8e72-d081-466e-ac8d-c3f81c8a6f35
title: MPEG-2 File 接收
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c27517463bca7dfa88fdbc09d77f7a6512c896d
ms.sourcegitcommit: 9c8ddec1e955f181beecad0478c1fb79013b5e9d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/21/2021
ms.locfileid: "106982122"
---
# <a name="mpeg-4-file-sink"></a><span data-ttu-id="a72b4-103">MPEG-2 File 接收</span><span class="sxs-lookup"><span data-stu-id="a72b4-103">MPEG-4 File Sink</span></span>

<span data-ttu-id="a72b4-104">MPEG-2 檔案接收會建立檔案。</span><span class="sxs-lookup"><span data-stu-id="a72b4-104">The MPEG-4 file sink creates MP4 files.</span></span> <span data-ttu-id="a72b4-105">如需有關檔案格式的詳細資訊，請參閱下列標準檔：</span><span class="sxs-lookup"><span data-stu-id="a72b4-105">For more information about the MP4 file format, refer to the following standards documents:</span></span>

-   <span data-ttu-id="a72b4-106">ISO/IEC 14496-12： *資訊技術--音訊-視覺化物件的編碼--第12部分： ISO 基底媒體檔案格式*</span><span class="sxs-lookup"><span data-stu-id="a72b4-106">ISO/IEC 14496-12: *Information technology -- Coding of audio-visual objects -- Part 12: ISO Base Media File Format*</span></span>
-   <span data-ttu-id="a72b4-107">ISO/IEC 14496-14： *資訊技術--音訊-視覺化物件的編碼--第14部分：數量檔案格式*</span><span class="sxs-lookup"><span data-stu-id="a72b4-107">ISO/IEC 14496-14: *Information technology -- Coding of audio-visual objects -- Part 14: MP4 File Format*</span></span>

> [!Note]  
> <span data-ttu-id="a72b4-108"> (這些資源可能無法在某些語言及國家/地區使用。 ) </span><span class="sxs-lookup"><span data-stu-id="a72b4-108">(These resources may not be available in some languages and countries.)</span></span>

 

<span data-ttu-id="a72b4-109">MPEG-2 file 接收不會封裝編碼功能。</span><span class="sxs-lookup"><span data-stu-id="a72b4-109">The MPEG-4 file sink does not encapsulate encoding functionality.</span></span>

<span data-ttu-id="a72b4-110">若要建立 MPEG-2 file 接收器，請呼叫 [**MFCreateMPEG4MediaSink**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatempeg4mediasink) 函式。</span><span class="sxs-lookup"><span data-stu-id="a72b4-110">To create the MPEG-4 file sink, call the [**MFCreateMPEG4MediaSink**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatempeg4mediasink) function.</span></span> <span data-ttu-id="a72b4-111">MPEG 4 檔案接收會透過 **QueryInterface** 公開下列介面：</span><span class="sxs-lookup"><span data-stu-id="a72b4-111">The MPEG-4 file sink exposes the following interfaces through **QueryInterface**:</span></span>

-   [<span data-ttu-id="a72b4-112">**IMFClockStateSink**</span><span class="sxs-lookup"><span data-stu-id="a72b4-112">**IMFClockStateSink**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink)
-   [<span data-ttu-id="a72b4-113">**IMFFinalizableMediaSink**</span><span class="sxs-lookup"><span data-stu-id="a72b4-113">**IMFFinalizableMediaSink**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imffinalizablemediasink)
-   [<span data-ttu-id="a72b4-114">**IMFGetService**</span><span class="sxs-lookup"><span data-stu-id="a72b4-114">**IMFGetService**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
-   [<span data-ttu-id="a72b4-115">**IMFMediaEventGenerator**</span><span class="sxs-lookup"><span data-stu-id="a72b4-115">**IMFMediaEventGenerator**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator)
-   [<span data-ttu-id="a72b4-116">**IMFMediaSink**</span><span class="sxs-lookup"><span data-stu-id="a72b4-116">**IMFMediaSink**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink)

## <a name="sample-description-box"></a><span data-ttu-id="a72b4-117">範例描述方塊</span><span class="sxs-lookup"><span data-stu-id="a72b4-117">Sample Description Box</span></span>

<span data-ttu-id="a72b4-118">使用的是可擴充的容器格式。</span><span class="sxs-lookup"><span data-stu-id="a72b4-118">MP4 is an extensible container format.</span></span> <span data-ttu-id="a72b4-119">使用規定規格不會定義固定的結構，以描述未設定的容器中的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="a72b4-119">The MP4 specification does not define a fixed structure for describing media types in an MP4 container.</span></span> <span data-ttu-id="a72b4-120">相反地，它會定義物件階層，讓您針對每個格式定義自訂結構。</span><span class="sxs-lookup"><span data-stu-id="a72b4-120">Instead, it defines an object hierarchy that allows custom structures to be defined for each format.</span></span> <span data-ttu-id="a72b4-121">格式描述會儲存在每個資料流程 ( [stsd] ) 方塊的範例描述中。</span><span class="sxs-lookup"><span data-stu-id="a72b4-121">The format description is stored in the sample description ('stsd') box for each stream.</span></span> <span data-ttu-id="a72b4-122">[範例描述] 方塊包含範例專案的清單。</span><span class="sxs-lookup"><span data-stu-id="a72b4-122">The sample description box contains a list of sample entries.</span></span> <span data-ttu-id="a72b4-123">針對每個範例專案，4位元組的程式碼（類似于 FOURCC）會定義格式結構。</span><span class="sxs-lookup"><span data-stu-id="a72b4-123">For each sample entry, a 4-byte code, similar to a FOURCC, defines the format structure.</span></span>

<span data-ttu-id="a72b4-124">MPEG-2 檔案接收可以針對下列格式產生範例描述方塊：</span><span class="sxs-lookup"><span data-stu-id="a72b4-124">The MPEG-4 File Sink can generate the sample description box for the following formats:</span></span>

-   <span data-ttu-id="a72b4-125">H.264/AVC 影片</span><span class="sxs-lookup"><span data-stu-id="a72b4-125">H.264/AVC video</span></span>
-   <span data-ttu-id="a72b4-126">AAC 音訊</span><span class="sxs-lookup"><span data-stu-id="a72b4-126">AAC audio</span></span>
-   <span data-ttu-id="a72b4-127">MP3 音訊</span><span class="sxs-lookup"><span data-stu-id="a72b4-127">MP3 audio</span></span>

<span data-ttu-id="a72b4-128">針對其他格式，則必須在每個資料流程的媒體類型中提供 [範例描述] 方塊。</span><span class="sxs-lookup"><span data-stu-id="a72b4-128">For other formats, the sample description box must be provided in the media type for each stream.</span></span> <span data-ttu-id="a72b4-129">若要指定 [範例描述] 方塊，請在媒體類型上設定下列屬性：</span><span class="sxs-lookup"><span data-stu-id="a72b4-129">To specify the sample description box, set the following attributes on the media type:</span></span>



| <span data-ttu-id="a72b4-130">屬性</span><span class="sxs-lookup"><span data-stu-id="a72b4-130">Attribute</span></span>                                                                     | <span data-ttu-id="a72b4-131">描述</span><span class="sxs-lookup"><span data-stu-id="a72b4-131">Description</span></span>                                                                                                                                                   |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a72b4-132">MF \_ MT \_ MPEG4 \_ 範例 \_ 說明</span><span class="sxs-lookup"><span data-stu-id="a72b4-132">MF\_MT\_MPEG4\_SAMPLE\_DESCRIPTION</span></span>](mf-mt-mpeg4-sample-description.md)      | <span data-ttu-id="a72b4-133">以二進位 blob 的形式包含範例描述方塊。</span><span class="sxs-lookup"><span data-stu-id="a72b4-133">Contains the sample description box as a binary blob.</span></span>                                                                                                         |
| [<span data-ttu-id="a72b4-134">MF \_ MT \_ MPEG4 \_ 目前的 \_ 範例 \_ 專案</span><span class="sxs-lookup"><span data-stu-id="a72b4-134">MF\_MT\_MPEG4\_CURRENT\_SAMPLE\_ENTRY</span></span>](mf-mt-mpeg4-current-sample-entry.md) | <span data-ttu-id="a72b4-135">指定 [範例描述] 方塊中的哪些範例專案目前為使用中狀態。</span><span class="sxs-lookup"><span data-stu-id="a72b4-135">Specifies which of the sample entries in the sample description box is currently active.</span></span> <span data-ttu-id="a72b4-136">(選擇性。)</span><span class="sxs-lookup"><span data-stu-id="a72b4-136">(Optional.)</span></span><br/> <span data-ttu-id="a72b4-137">目前，此值必須為零。</span><span class="sxs-lookup"><span data-stu-id="a72b4-137">Currently, the value must be zero.</span></span><br/> |



 

<span data-ttu-id="a72b4-138">在某些情況下，必須等到所有資料都經過編碼之後，才可以產生範例描述方塊。</span><span class="sxs-lookup"><span data-stu-id="a72b4-138">In some cases, it is not possible to generate a sample description box until all of the data has been encoded.</span></span> <span data-ttu-id="a72b4-139">例如，可能事先不知道平均位元速率等資訊。</span><span class="sxs-lookup"><span data-stu-id="a72b4-139">For example, information such as the average bit rate might not be known ahead of time.</span></span> <span data-ttu-id="a72b4-140">在這種情況下，您可以使用 MPEG 4 檔案接收上的 [**IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) 介面來更新媒體類型。</span><span class="sxs-lookup"><span data-stu-id="a72b4-140">In that case, you can update the media type by using the [**IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) interface on the MPEG-4 file sink.</span></span> <span data-ttu-id="a72b4-141">這必須在媒體接收完成之前完成。</span><span class="sxs-lookup"><span data-stu-id="a72b4-141">This must be done before the media sink is finalized.</span></span>

<span data-ttu-id="a72b4-142">媒體類型通常是由上游編碼器所建立。</span><span class="sxs-lookup"><span data-stu-id="a72b4-142">Typically the media type is created by an upstream encoder.</span></span> <span data-ttu-id="a72b4-143">編碼器可透過動態格式變更，在串流期間產生新的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="a72b4-143">The encoder can generate a new media type during streaming, through a dynamic format change.</span></span> <span data-ttu-id="a72b4-144">如需詳細資訊，請參閱 [動態格式變更](basic-mft-processing-model.md)。</span><span class="sxs-lookup"><span data-stu-id="a72b4-144">For more information, see [Dynamic Format Changes](basic-mft-processing-model.md).</span></span>

## <a name="h264avc-video"></a><span data-ttu-id="a72b4-145">H.264/AVC 影片</span><span class="sxs-lookup"><span data-stu-id="a72b4-145">H.264/AVC Video</span></span>

<span data-ttu-id="a72b4-146">MPEG-2 檔案接收支援具有基本影片串流的 AVC 資料流程版本，其序列參數設定 (SPS) 和 [範例描述] 方塊中所含的圖片參數集 (PPS) NALUs，如 ISO/IEC 14496 第15節5.1 節所定義。</span><span class="sxs-lookup"><span data-stu-id="a72b4-146">The MPEG-4 file sink supports the version of the AVC stream that has an elementary video stream, with sequence parameter set (SPS) and picture parameter set (PPS) NALUs contained in the sample description box, as defined in ISO/IEC 14496 part 15 section 5.1.</span></span> <span data-ttu-id="a72b4-147">File 接收不支援另一種將 SPS/PPS NALUs 儲存為個別參數集基本資料流程的方法。</span><span class="sxs-lookup"><span data-stu-id="a72b4-147">The file sink does not support the alternate method of storing SPS/PPS NALUs as a separate parameter-set elementary stream.</span></span>

<span data-ttu-id="a72b4-148">MPEG-2 file 接收器可以產生範例描述方塊，但必須提供給 SPS 和 PPS NALUs。</span><span class="sxs-lookup"><span data-stu-id="a72b4-148">The MPEG-4 file sink can generate the sample description box, but must be provided with the SPS and PPS NALUs.</span></span> <span data-ttu-id="a72b4-149">藉由設定 [ [**MF \_ MT \_ MPEG \_ 序列 \_ 標頭**](mf-mt-mpeg-sequence-header-attribute.md) ] 屬性，在媒體類型中指定這項資訊。</span><span class="sxs-lookup"><span data-stu-id="a72b4-149">Specify this information in the media type by setting the [**MF\_MT\_MPEG\_SEQUENCE\_HEADER**](mf-mt-mpeg-sequence-header-attribute.md) attribute.</span></span> <span data-ttu-id="a72b4-150">屬性的值是 h.264 序列標頭。</span><span class="sxs-lookup"><span data-stu-id="a72b4-150">The value of the attribute is the H.264 sequence header.</span></span> <span data-ttu-id="a72b4-151">Sequence 標頭必須由 SP 和 PPS NALUs （以3位元組或4位元組起始碼分隔）組成。</span><span class="sxs-lookup"><span data-stu-id="a72b4-151">The sequence header must consist of the SPS and PPS NALUs delimited by either 3-byte or 4-byte start codes.</span></span>

<span data-ttu-id="a72b4-152">（選擇性）當您設定 file 接收時，您可以從初始媒體類型省略 [**MF \_ MT \_ MPEG \_ 順序 \_ 標頭**](mf-mt-mpeg-sequence-header-attribute.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="a72b4-152">Optionally, when you configure the file sink, you can omit the [**MF\_MT\_MPEG\_SEQUENCE\_HEADER**](mf-mt-mpeg-sequence-header-attribute.md) attribute from the initial media type.</span></span> <span data-ttu-id="a72b4-153">在這種情況下，您必須稍後更新媒體類型以包含 sequence 標頭。</span><span class="sxs-lookup"><span data-stu-id="a72b4-153">In that case, you must update the media type later to include the sequence header.</span></span>

<span data-ttu-id="a72b4-154">MPEG-2 檔案接收的 AVC bitstreams 需求如下：</span><span class="sxs-lookup"><span data-stu-id="a72b4-154">The MPEG-4 file sink has the following requirements for AVC bitstreams:</span></span>

-   <span data-ttu-id="a72b4-155">位流必須符合 h.264 附錄 B 格式規格。</span><span class="sxs-lookup"><span data-stu-id="a72b4-155">The bitstream must conform to the H.264 Annex B format specification.</span></span> <span data-ttu-id="a72b4-156">尤其是，NALUs 必須以3個位元組或4位元組起始碼分隔。</span><span class="sxs-lookup"><span data-stu-id="a72b4-156">In particular, NALUs must be delimited with either 3-byte or 4-byte start codes.</span></span>
-   <span data-ttu-id="a72b4-157">媒體範例必須包含對應至單一呈現時間的所有配量和資料 NALUs。</span><span class="sxs-lookup"><span data-stu-id="a72b4-157">Media samples must contain all slice and data NALUs that correspond to a single presentation time.</span></span>
-   <span data-ttu-id="a72b4-158">將 B 框架寫入至設定檔案時，您必須同時設定簡報時間戳記和解碼時間戳記。</span><span class="sxs-lookup"><span data-stu-id="a72b4-158">When writing B-frames into an MP4 file, you must set both the presentation time stamp and the decode time stamp.</span></span> <span data-ttu-id="a72b4-159">如果 stream 有 B 框架，但未設定解碼時間戳記，則配置寫入器將會看到畫面上的時間，並會捨棄框架。</span><span class="sxs-lookup"><span data-stu-id="a72b4-159">If stream has a B frame and the decode timestamp is not set, the MP4 writer will see the frame time going backwards and will drop the frame.</span></span> 

## <a name="aac-audio"></a><span data-ttu-id="a72b4-160">AAC 音訊</span><span class="sxs-lookup"><span data-stu-id="a72b4-160">AAC Audio</span></span>

<span data-ttu-id="a72b4-161">針對 AAC 音訊，MPEG-2 檔案接收可以針對下列子類型產生範例描述方塊：</span><span class="sxs-lookup"><span data-stu-id="a72b4-161">For AAC audio, the MPEG-4 file sink can generate the sample description box for the following subtypes:</span></span>

-   <span data-ttu-id="a72b4-162">**MFAudioFormat \_ AAC**</span><span class="sxs-lookup"><span data-stu-id="a72b4-162">**MFAudioFormat\_AAC**</span></span>
-   <span data-ttu-id="a72b4-163">**MEDIASUBTYPE \_ 原始 \_ AAC1**</span><span class="sxs-lookup"><span data-stu-id="a72b4-163">**MEDIASUBTYPE\_RAW\_AAC1**</span></span>

<span data-ttu-id="a72b4-164">如需這些 substypes 的詳細資訊，請參閱 [AAC 媒體類型](aac-media-types.md)。</span><span class="sxs-lookup"><span data-stu-id="a72b4-164">For more information about these substypes, see [AAC Media Types](aac-media-types.md).</span></span>

<span data-ttu-id="a72b4-165">針對 **MFAudioFormat \_ AAC** 子類型，媒體類型可選擇性地包含 [**MF \_ MT \_ 使用者 \_ 資料**](mf-mt-user-data-attribute.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="a72b4-165">For the **MFAudioFormat\_AAC** subtype, the media type optionally contains the [**MF\_MT\_USER\_DATA**](mf-mt-user-data-attribute.md) attribute.</span></span> <span data-ttu-id="a72b4-166">如果有的話，這個屬性會出現在 **WAVEFORMATEX** 結構後面的 [**HEAACWAVEINFO**](/windows/win32/api/mmreg/ns-mmreg-heaacwaveinfo)結構部分 (也就是 **wfx** 成員) 之後。</span><span class="sxs-lookup"><span data-stu-id="a72b4-166">If present, this attribute the portion of the [**HEAACWAVEINFO**](/windows/win32/api/mmreg/ns-mmreg-heaacwaveinfo) structure that appears after the **WAVEFORMATEX** structure (that is, after the **wfx** member).</span></span> <span data-ttu-id="a72b4-167">後面接著 AudioSpecificConfig () 資料，如 ISO/IEC 14496-3 所定義。</span><span class="sxs-lookup"><span data-stu-id="a72b4-167">This is followed by the AudioSpecificConfig() data, as defined by ISO/IEC 14496-3.</span></span> <span data-ttu-id="a72b4-168">如果不存在 **MF \_ MT \_ 使用者 \_ 資料** 屬性，則會假設資料流程 AAC 低複雜度 (LC) 設定檔，而 MPEG 4 檔案接收會產生適當的範例描述方塊。</span><span class="sxs-lookup"><span data-stu-id="a72b4-168">If the **MF\_MT\_USER\_DATA** attribute is not present, the stream is assumed to be AAC Low Complexity (LC) profile, and the MPEG-4 file sink generates a suitable sample description box.</span></span>

<span data-ttu-id="a72b4-169">針對 **MEDIASUBTYPE \_ RAW \_ AAC1** 子類型，媒體接收器必須包含 [**MF \_ MT \_ 使用者 \_ 資料**](mf-mt-user-data-attribute.md) 屬性，而且屬性必須包含 AudioSpecificConfig () 資料。</span><span class="sxs-lookup"><span data-stu-id="a72b4-169">For the **MEDIASUBTYPE\_RAW\_AAC1** subtype, the media sink must contain the [**MF\_MT\_USER\_DATA**](mf-mt-user-data-attribute.md) attribute, and the attribute must contain the AudioSpecificConfig() data.</span></span>

<span data-ttu-id="a72b4-170">MPEG-2 檔案接收會使用 ' mp4a ' 範例專案搭配 objectTypeIndication = 0x40 來建立 AAC 範例描述方塊的 MPEG-2 變化。</span><span class="sxs-lookup"><span data-stu-id="a72b4-170">The MPEG-4 file sink creates the MPEG-4 variant of the AAC sample description box, using an 'mp4a' sample entry with objectTypeIndication = 0x40.</span></span> <span data-ttu-id="a72b4-171">它不會使用 MPEG-2 物件類型。</span><span class="sxs-lookup"><span data-stu-id="a72b4-171">It does not use MPEG-2 object types.</span></span>

## <a name="mp3-audio"></a><span data-ttu-id="a72b4-172">MP3 音訊</span><span class="sxs-lookup"><span data-stu-id="a72b4-172">MP3 Audio</span></span>

<span data-ttu-id="a72b4-173">若為 MP3 音訊，MPEG-2 file 接收器可以從標準音頻媒體類型產生範例描述方塊。</span><span class="sxs-lookup"><span data-stu-id="a72b4-173">For MP3 audio, the MPEG-4 file sink can generate the sample description box from a standard audio media type.</span></span> <span data-ttu-id="a72b4-174"> (查看 [音訊媒體類型](audio-media-types.md)。 ) </span><span class="sxs-lookup"><span data-stu-id="a72b4-174">(See [Audio Media Types](audio-media-types.md).)</span></span>

<span data-ttu-id="a72b4-175">MPEG-2 檔案接收會使用 ' mp4a ' 範例專案搭配 objectTypeIndication = 0x6b 的 MPEG-2 音訊，建立 MP3 範例描述方塊的 MPEG 4 變化。</span><span class="sxs-lookup"><span data-stu-id="a72b4-175">The MPEG-4 file sink creates the MPEG-4 variant of the MP3 sample description box, using an 'mp4a' sample entry with objectTypeIndication = 0x6b for MPEG-1 audio.</span></span>

## <a name="limitations"></a><span data-ttu-id="a72b4-176">限制</span><span class="sxs-lookup"><span data-stu-id="a72b4-176">Limitations</span></span>

-   <span data-ttu-id="a72b4-177">所撰寫檔案的大小上限為 4 GB。</span><span class="sxs-lookup"><span data-stu-id="a72b4-177">The maximum size of the authored file is 4 GB.</span></span> <span data-ttu-id="a72b4-178">在 Windows 8 中，支援超過4個 GBGB 的檔案。</span><span class="sxs-lookup"><span data-stu-id="a72b4-178">In Windows 8, files large than 4 GBGB are supported.</span></span>
-   <span data-ttu-id="a72b4-179">MPEG-2 檔案接收不支援 [edts] 和 [elst] 方塊 ( 編輯清單) 。</span><span class="sxs-lookup"><span data-stu-id="a72b4-179">The MPEG-4 file sink does not support edit lists ('edts' and 'elst' boxes).</span></span>

## <a name="windows-8-updates-to-mpeg-4-source-and-sink"></a><span data-ttu-id="a72b4-180">Windows 8 更新至 MPEG-2 來源和接收</span><span class="sxs-lookup"><span data-stu-id="a72b4-180">Windows 8 updates to MPEG-4 source and sink</span></span>

-   <span data-ttu-id="a72b4-181">Windows 8 MPEG-2 來源和接收中新增的旋轉讀取和寫入支援。</span><span class="sxs-lookup"><span data-stu-id="a72b4-181">Rotation read and write support added in Windows 8 MPEG-4 source and sink.</span></span> <span data-ttu-id="a72b4-182">Windows 7 MPEG-2 來源和接收中不支援此功能。</span><span class="sxs-lookup"><span data-stu-id="a72b4-182">This is not supported in the Windows 7 MPEG-4 source and sink.</span></span>

    <span data-ttu-id="a72b4-183">MPEG 4 來源會讀取作用中影片播放軌的旋轉角度，作為從 ' mvhd ' 和 ' tkhd ' 旋轉角度的總和。</span><span class="sxs-lookup"><span data-stu-id="a72b4-183">MPEG-4 source reads the rotation angle for an active video track as the sum of the rotation angle from ‘mvhd’ and from ‘tkhd’.</span></span>

    <span data-ttu-id="a72b4-184">Microsoft MPEG-2 接收會在 ' tkhd ' 中寫入旋轉角度，但會在 ' mvhd ' 中寫入0度的 (識別) 矩陣。</span><span class="sxs-lookup"><span data-stu-id="a72b4-184">Microsoft MPEG-4 sink writes the rotation angle in ‘tkhd’ but writes 0 degree (identity) matrix in ‘mvhd’.</span></span> <span data-ttu-id="a72b4-185">請注意，Microsoft MPEG 4 接收器只支援單一影片播放軌。</span><span class="sxs-lookup"><span data-stu-id="a72b4-185">Note, Microsoft MPEG-4 sink only supports single video track.</span></span>

    <span data-ttu-id="a72b4-186">IPropertyStore 只會讀取第一個影片播放軌的旋轉角度，作為從 ' mvhd ' 和 ' tkhd ' 旋轉角度的總和。</span><span class="sxs-lookup"><span data-stu-id="a72b4-186">IPropertyStore reads the rotation angle for only the first video track as the sum of the rotation angle from ‘mvhd’ and from ‘tkhd’.</span></span>

    <span data-ttu-id="a72b4-187">IPropertyStore 只會在旋轉角度根據 ' mvhd ' 中的旋轉角度（如果有的話）調整旋轉角度之後，才在 ' tkhd ' 中寫入第一個影片播放軌的旋轉角度。</span><span class="sxs-lookup"><span data-stu-id="a72b4-187">IPropertyStore writes the rotation angle for only the first video track in ‘tkhd’ after the rotation angle is adjusted according to the rotation angle in ‘mvhd’, if it exists.</span></span>

-   <span data-ttu-id="a72b4-188">Windows 8 MPEG-2 來源和接收中支援 ' moof ' )  ( 的電影片段，但 ' mfra ' 不支援。</span><span class="sxs-lookup"><span data-stu-id="a72b4-188">Movie fragments ('moof') is supported in Windows 8 MPEG-4 source and sink, but 'mfra' is not.</span></span>
-   <span data-ttu-id="a72b4-189">Windows 8 的 MPEG-2 來源支援 .h。</span><span class="sxs-lookup"><span data-stu-id="a72b4-189">H.263 is supported in Windows 8 MPEG-4 source.</span></span>

    <span data-ttu-id="a72b4-190">MPEG 4 來源現在會將 MPEG-2 檔案格式的兩個 fourcc ' h263 ' 和 ' 263 ' 對應到 **MFVideoFormat \_ h263** 的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="a72b4-190">MPEG-4 source now maps two fourcc’s of ‘h263’ and ‘s263’ in MPEG-4 file format to the media type of **MFVideoFormat\_H263**.</span></span>

-   <span data-ttu-id="a72b4-191">在 Windows 8 MPEG-2 來源的 MJPEG 中新增了更多 fourcc 支援。</span><span class="sxs-lookup"><span data-stu-id="a72b4-191">More fourcc support added for MJPEG in Windows 8 MPEG-4 source.</span></span>

    <span data-ttu-id="a72b4-192">MPEG 4 來源會將 ' dmb1 ' 的 foucc 對應至 **MFVideoFormat \_ MJPG** 的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="a72b4-192">MPEG-4 source maps foucc of ‘dmb1’ to the media type of **MFVideoFormat\_MJPG**.</span></span>

-   <span data-ttu-id="a72b4-193">Windows 8 MPEG-2 來源中新增的漢字中繼資料支援。</span><span class="sxs-lookup"><span data-stu-id="a72b4-193">Furigana metadata support added in Windows 8 MPEG-4 source.</span></span>

    <span data-ttu-id="a72b4-194">MPEG-2 來源會從 ' soal '、' soar '、' soaa '、' sonm ' 和 ' soco ' 讀取中繼資料。</span><span class="sxs-lookup"><span data-stu-id="a72b4-194">MPEG-4 source reads Furigana metadata from ’soal’, ‘soar’, ‘soaa’, ‘sonm’, and ‘soco’.</span></span> <span data-ttu-id="a72b4-195">IPropertyStore 會透過一組對應的 PKEYs 來讀取 Furignana 中繼資料。</span><span class="sxs-lookup"><span data-stu-id="a72b4-195">IPropertyStore reads Furignana metadata through the set of corresponding PKEYs.</span></span>

    <span data-ttu-id="a72b4-196">下表顯示 shell 正式名稱、屬性索引鍵，以及 MPEG-2 檔案格式的 box/標記識別項之間的對應。</span><span class="sxs-lookup"><span data-stu-id="a72b4-196">The following table shows the mapping between the shell canonical name, the property key, and the box/tag ID in MPEG-4 file format.</span></span>

    

    | <span data-ttu-id="a72b4-197">欄位</span><span class="sxs-lookup"><span data-stu-id="a72b4-197">Field</span></span>                                | <span data-ttu-id="a72b4-198">屬性索引鍵</span><span class="sxs-lookup"><span data-stu-id="a72b4-198">Property Key</span></span>                         | <span data-ttu-id="a72b4-199">標記/Box 識別碼</span><span class="sxs-lookup"><span data-stu-id="a72b4-199">Tag/Box ID</span></span> |
    |--------------------------------------|--------------------------------------|------------|
    | <span data-ttu-id="a72b4-200">AlbumTitleSortOverride</span><span class="sxs-lookup"><span data-stu-id="a72b4-200">System.Music.AlbumTitleSortOverride</span></span>  | <span data-ttu-id="a72b4-201">PKEY \_ 音樂 \_ AlbumTitleSortOverride</span><span class="sxs-lookup"><span data-stu-id="a72b4-201">PKEY\_Music\_AlbumTitleSortOverride</span></span>  | <span data-ttu-id="a72b4-202">soal</span><span class="sxs-lookup"><span data-stu-id="a72b4-202">soal</span></span>       |
    | <span data-ttu-id="a72b4-203">ArtistSortOverride</span><span class="sxs-lookup"><span data-stu-id="a72b4-203">System.Music.ArtistSortOverride</span></span>      | <span data-ttu-id="a72b4-204">PKEY \_ 音樂 \_ ArtistSortOverride</span><span class="sxs-lookup"><span data-stu-id="a72b4-204">PKEY\_Music\_ArtistSortOverride</span></span>      | <span data-ttu-id="a72b4-205">飆升</span><span class="sxs-lookup"><span data-stu-id="a72b4-205">soar</span></span>       |
    | <span data-ttu-id="a72b4-206">AlbumArtistSortOverride</span><span class="sxs-lookup"><span data-stu-id="a72b4-206">System.Music.AlbumArtistSortOverride</span></span> | <span data-ttu-id="a72b4-207">PKEY \_ 音樂 \_ AlbumArtistSortOverride</span><span class="sxs-lookup"><span data-stu-id="a72b4-207">PKEY\_Music\_AlbumArtistSortOverride</span></span> | <span data-ttu-id="a72b4-208">soaa</span><span class="sxs-lookup"><span data-stu-id="a72b4-208">soaa</span></span>       |
    | <span data-ttu-id="a72b4-209">System. TitleSortOverride</span><span class="sxs-lookup"><span data-stu-id="a72b4-209">System.TitleSortOverride</span></span>             | <span data-ttu-id="a72b4-210">PKEY \_ TitleSortOverride</span><span class="sxs-lookup"><span data-stu-id="a72b4-210">PKEY \_TitleSortOverride</span></span>             | <span data-ttu-id="a72b4-211">sonm</span><span class="sxs-lookup"><span data-stu-id="a72b4-211">sonm</span></span>       |
    | <span data-ttu-id="a72b4-212">ComposerSortOverride</span><span class="sxs-lookup"><span data-stu-id="a72b4-212">System.Music.ComposerSortOverride</span></span>    | <span data-ttu-id="a72b4-213">PKEY \_ 音樂 \_ ComposerSortOverride</span><span class="sxs-lookup"><span data-stu-id="a72b4-213">PKEY\_Music\_ComposerSortOverride</span></span>    | <span data-ttu-id="a72b4-214">soco</span><span class="sxs-lookup"><span data-stu-id="a72b4-214">soco</span></span>       |

    

     

-   <span data-ttu-id="a72b4-215">Windows 8 MPEG-2 來源中新增了身歷聲 3D atom 支援。</span><span class="sxs-lookup"><span data-stu-id="a72b4-215">Stereo 3D atom support added in Windows 8 MPEG-4 source.</span></span>

-   <span data-ttu-id="a72b4-216">Windows 8 的 MPEG-2 來源和接收中新增了 AC3 和 DD + 支援。</span><span class="sxs-lookup"><span data-stu-id="a72b4-216">AC3 and DD+ support added in Windows 8 MPEG-4 source and sink.</span></span>
-   <span data-ttu-id="a72b4-217">針對非 fragmental 的，支援大於 4 GB 的檔案的 Windows 8 MPEG 接收器。</span><span class="sxs-lookup"><span data-stu-id="a72b4-217">Files larger than 4 GB are supported in Windows 8 MPEG-4 sink for non-fragmental MP4.</span></span>
-   <span data-ttu-id="a72b4-218">Windows 8 的 MPEG-2 來源已優化清除。</span><span class="sxs-lookup"><span data-stu-id="a72b4-218">Scrubbing has been optimized in Windows 8 MPEG-4 source.</span></span>

    <span data-ttu-id="a72b4-219">為了減少延遲，特定搜尋位置的兩個最接近主要畫面格的資訊會透過 [**IMFSeekInfo：： GetNearestKeyFrames**](/windows/desktop/api/mfidl/nf-mfidl-imfseekinfo-getnearestkeyframes)公開。</span><span class="sxs-lookup"><span data-stu-id="a72b4-219">To reduce latency, information for the two nearest key frames for a particular seek position are exposed through [**IMFSeekInfo::GetNearestKeyFrames**](/windows/desktop/api/mfidl/nf-mfidl-imfseekinfo-getnearestkeyframes).</span></span> <span data-ttu-id="a72b4-220">由於主要畫面格沒有相依的框架，因此只會在解碼一個畫面格之後呈現畫面格。</span><span class="sxs-lookup"><span data-stu-id="a72b4-220">Since the key frame does not have dependent frames, it presents the frame after decoding only one frame.</span></span> <span data-ttu-id="a72b4-221">使用 [**IMFGetService：： GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) 透過媒體來源、管線或應用程式取得這個介面。</span><span class="sxs-lookup"><span data-stu-id="a72b4-221">Use [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) to obtain this interface through the media source, pipeline, or application.</span></span>

    <span data-ttu-id="a72b4-222">在 MPEG 4 來源中將速率設定為零。</span><span class="sxs-lookup"><span data-stu-id="a72b4-222">Set rate to zero in MPEG-4 source.</span></span> <span data-ttu-id="a72b4-223">當管線處於清除模式時，速率為零。</span><span class="sxs-lookup"><span data-stu-id="a72b4-223">When the pipeline is in scrubbing mode, the rate is zero.</span></span>

-   <span data-ttu-id="a72b4-224">您可以將 SPS 和 PPS 儲存在 MPEG 4 接收的範例資料中。</span><span class="sxs-lookup"><span data-stu-id="a72b4-224">SPS and PPS can be stored in sample data in MPEG-4 sink.</span></span>

    <span data-ttu-id="a72b4-225">[MF \_在 MPEG 4 接收上的 MPEG4SINK \_ SPSPPS \_ 傳遞](mf-mpeg4sink-spspps-passthrough.md) 屬性定義為允許將 SPS 和 PPS 儲存在一起， (h.264 video 資料) 的輸入範例。</span><span class="sxs-lookup"><span data-stu-id="a72b4-225">[MF\_MPEG4SINK\_SPSPPS\_PASSTHROUGH](mf-mpeg4sink-spspps-passthrough.md) attribute on MPEG-4 sink is defined to allow SPS’s and PPS’s to be saved together with input samples (H.264 video data).</span></span> <span data-ttu-id="a72b4-226">產生的已產生的等式剪輯可由 Windows 7 MPEG-2 來源與其他專案播放。</span><span class="sxs-lookup"><span data-stu-id="a72b4-226">The produced mp4 clips are play-able by Windows 7 MPEG-4 source and others.</span></span>

-   <span data-ttu-id="a72b4-227">您可以從 MPEG 接收器的輸入範例中解壓縮 SPS 和 PPS。</span><span class="sxs-lookup"><span data-stu-id="a72b4-227">SPS and PPS can be extracted from input samples in MPEG-4 sink.</span></span>

    <span data-ttu-id="a72b4-228">當 SP 和 PPS 未設定在 MPEG 接收器的輸入媒體類型上的 [MF \_ MT \_ MPEG \_ 序列 \_ 標頭](mf-mt-mpeg-sequence-header-attribute.md) 時，mpeg 4 接收會嘗試從輸入範例中解壓縮 sps 和 pps。</span><span class="sxs-lookup"><span data-stu-id="a72b4-228">When SPS and PPS are not set through [MF\_MT\_MPEG\_SEQUENCE\_HEADER](mf-mt-mpeg-sequence-header-attribute.md) on input media type of the MPEG-4 sink, MPEG-4 sink will try to extract SPS and PPS from input samples.</span></span> <span data-ttu-id="a72b4-229">MPEG-2 接收會忽略任何輸入範例，直到它找到第一個 SPS 和 PPS 為止，因為沒有 SPS 和 PPS 的所有輸入範例都不能進行解碼。</span><span class="sxs-lookup"><span data-stu-id="a72b4-229">MPEG-4 sink ignores any input samples until it finds the first SPS and PPS, because all input samples without SPS and PPS are not decode-able.</span></span>

-   <span data-ttu-id="a72b4-230">AVC 設定記錄中的3D 資訊支援非 fragmental 的配置。</span><span class="sxs-lookup"><span data-stu-id="a72b4-230">3D information in AVC configuration record is supported for non-fragmental MP4.</span></span>
-   <span data-ttu-id="a72b4-231">NALU 長度會針對 h.264 壓縮範例公開，以優化 h.264 VLD DXVA 解碼。</span><span class="sxs-lookup"><span data-stu-id="a72b4-231">NALU length is exposed for H.264 compressed samples to optimize H.264 VLD DXVA decoding.</span></span>

    <span data-ttu-id="a72b4-232">MPEG-2 來源集會設定 **MFVideoFormat \_ H264** 或 **MFVideoFormat \_ H264** 輸出媒體類型的 [MF \_ NALU \_ 長度 \_](mf-nalu-length-set.md) 。</span><span class="sxs-lookup"><span data-stu-id="a72b4-232">MPEG-4 source sets [MF\_NALU\_LENGTH\_SET](mf-nalu-length-set.md) on the output media type of **MFVideoFormat\_H264** or **MFVideoFormat\_h264**.</span></span> <span data-ttu-id="a72b4-233">它會在每個輸出範例上設定 [MF \_ NALU \_ 長度 \_ 資訊](mf-nalu-length-information.md) 的 blob，其中有一個壓縮範例中不同 NALU 的四位元組 NALU 長度。</span><span class="sxs-lookup"><span data-stu-id="a72b4-233">It sets the blob of [MF\_NALU\_LENGTH\_INFORMATION](mf-nalu-length-information.md) on each output sample, with four-byte NALU length for different NALU’s in one compressed sample.</span></span>

-   <span data-ttu-id="a72b4-234">針對在 ADTS 中的的 MPEG2 音訊新增支援。</span><span class="sxs-lookup"><span data-stu-id="a72b4-234">Support added for MPEG2 ADTS audio in MP4 source.</span></span>

## <a name="requirements"></a><span data-ttu-id="a72b4-235">規格需求</span><span class="sxs-lookup"><span data-stu-id="a72b4-235">Requirements</span></span>



| <span data-ttu-id="a72b4-236">需求</span><span class="sxs-lookup"><span data-stu-id="a72b4-236">Requirement</span></span> | <span data-ttu-id="a72b4-237">值</span><span class="sxs-lookup"><span data-stu-id="a72b4-237">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="a72b4-238">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a72b4-238">Minimum supported client</span></span><br/> | <span data-ttu-id="a72b4-239">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a72b4-239">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="a72b4-240">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a72b4-240">Minimum supported server</span></span><br/> | <span data-ttu-id="a72b4-241">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a72b4-241">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a72b4-242">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a72b4-242">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a72b4-243">媒體來源和接收</span><span class="sxs-lookup"><span data-stu-id="a72b4-243">Media Sources and Sinks</span></span>](media-sources-and-sinks.md)
</dt> <dt>

[<span data-ttu-id="a72b4-244">媒體接收器</span><span class="sxs-lookup"><span data-stu-id="a72b4-244">Media Sinks</span></span>](media-sinks.md)
</dt> <dt>

[<span data-ttu-id="a72b4-245">媒體基礎中的 MPEG 4 支援</span><span class="sxs-lookup"><span data-stu-id="a72b4-245">MPEG-4 Support in Media Foundation</span></span>](mpeg-4-support-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="a72b4-246">媒體基礎中支援的媒體格式</span><span class="sxs-lookup"><span data-stu-id="a72b4-246">Supported Media Formats in Media Foundation</span></span>](supported-media-formats-in-media-foundation.md)
</dt> </dl>

 

 
