---
description: 本主題說明如何使用轉碼 API 來編碼媒體檔案。
ms.assetid: 52b27359-b319-41a0-88e8-d23567420e92
title: 使用轉碼 API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bb97dd61ef75e71a82b522b65b682f861022bcf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111772"
---
# <a name="using-the-transcode-api"></a><span data-ttu-id="142ed-103">使用轉碼 API</span><span class="sxs-lookup"><span data-stu-id="142ed-103">Using the Transcode API</span></span>

<span data-ttu-id="142ed-104">本主題說明如何使用轉碼 API 來編碼媒體檔案。</span><span class="sxs-lookup"><span data-stu-id="142ed-104">This topic described how to use the transcode API to encode a media file.</span></span>

-   [<span data-ttu-id="142ed-105">概觀</span><span class="sxs-lookup"><span data-stu-id="142ed-105">Overview</span></span>](#overview)
-   [<span data-ttu-id="142ed-106">建立媒體來源</span><span class="sxs-lookup"><span data-stu-id="142ed-106">Creating a Media Source</span></span>](#creating-a-media-source)
-   [<span data-ttu-id="142ed-107">建立轉碼設定檔</span><span class="sxs-lookup"><span data-stu-id="142ed-107">Creating a Transcode Profile</span></span>](#creating-a-transcode-profile)
    -   [<span data-ttu-id="142ed-108">音訊屬性</span><span class="sxs-lookup"><span data-stu-id="142ed-108">Audio Attributes</span></span>](#audio-attributes)
    -   [<span data-ttu-id="142ed-109">影片屬性</span><span class="sxs-lookup"><span data-stu-id="142ed-109">Video Attributes</span></span>](#video-attributes)
    -   [<span data-ttu-id="142ed-110">容器屬性</span><span class="sxs-lookup"><span data-stu-id="142ed-110">Container Attributes</span></span>](#container-attributes)
-   [<span data-ttu-id="142ed-111">建立轉碼拓撲</span><span class="sxs-lookup"><span data-stu-id="142ed-111">Creating a Transcode Topology</span></span>](#creating-a-transcode-topology)
-   [<span data-ttu-id="142ed-112">正在執行編碼會話</span><span class="sxs-lookup"><span data-stu-id="142ed-112">Running the Encoding Session</span></span>](#running-the-encoding-session)
-   [<span data-ttu-id="142ed-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="142ed-113">Related topics</span></span>](#related-topics)

## <a name="overview"></a><span data-ttu-id="142ed-114">概觀</span><span class="sxs-lookup"><span data-stu-id="142ed-114">Overview</span></span>

<span data-ttu-id="142ed-115">在使用轉碼 API 之前，應用程式必須具有下列資訊片段：</span><span class="sxs-lookup"><span data-stu-id="142ed-115">Before using the transcode API, the application must have the following pieces of information:</span></span>

-   <span data-ttu-id="142ed-116">將會重新編碼之現有媒體檔案的路徑或 URL。</span><span class="sxs-lookup"><span data-stu-id="142ed-116">The path or URL to an existing media file that will be re-encoded.</span></span>
-   <span data-ttu-id="142ed-117">輸出檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="142ed-117">The name of the output file.</span></span>
-   <span data-ttu-id="142ed-118">輸出檔的容器類型，例如，「設定」或「Advanced 串流格式」 (ASF) 。</span><span class="sxs-lookup"><span data-stu-id="142ed-118">The container type for the output file, such as MP4 or Advanced Streaming Format (ASF).</span></span>
-   <span data-ttu-id="142ed-119">編碼格式。</span><span class="sxs-lookup"><span data-stu-id="142ed-119">The encoding format.</span></span> <span data-ttu-id="142ed-120">此資訊包含描述編碼音訊和影片串流的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="142ed-120">This information includes the media types that describe the encoded audio and video streams.</span></span>

<span data-ttu-id="142ed-121">若要使用轉碼 API，應用程式會執行下列步驟。</span><span class="sxs-lookup"><span data-stu-id="142ed-121">To use the transcode API, an application performs the following steps.</span></span>

1.  <span data-ttu-id="142ed-122">建立媒體來源以讀取原始檔。</span><span class="sxs-lookup"><span data-stu-id="142ed-122">Create a media source to read the source file.</span></span>
2.  <span data-ttu-id="142ed-123">建立轉碼設定檔。</span><span class="sxs-lookup"><span data-stu-id="142ed-123">Create a transcode profile.</span></span> <span data-ttu-id="142ed-124">新增描述音訊串流、影片串流和檔案容器的屬性。</span><span class="sxs-lookup"><span data-stu-id="142ed-124">Add attributes that describe the audio stream, video stream, and file container.</span></span>
3.  <span data-ttu-id="142ed-125">使用轉碼設定檔來建立編碼拓撲。</span><span class="sxs-lookup"><span data-stu-id="142ed-125">Use the transcode profile to create an encoding topology.</span></span> <span data-ttu-id="142ed-126">如需拓撲的詳細資訊，請參閱 [關於拓撲](about-topologies.md)的詳細資訊 (。 ) </span><span class="sxs-lookup"><span data-stu-id="142ed-126">(For more information about topologies, see [About Topologies](about-topologies.md).)</span></span>
4.  <span data-ttu-id="142ed-127">在 [媒體會話](media-session.md)上設定拓撲。</span><span class="sxs-lookup"><span data-stu-id="142ed-127">Set the topology on the [Media Session](media-session.md).</span></span>
5.  <span data-ttu-id="142ed-128">啟動媒體會話，並等候 [MESessionEnded](mesessionended.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="142ed-128">Start the Media Session and wait for the [MESessionEnded](mesessionended.md) event.</span></span>

<span data-ttu-id="142ed-129">本主題的其餘部分將更詳細地描述這些步驟。</span><span class="sxs-lookup"><span data-stu-id="142ed-129">The remainder of this topic describes these steps in more detail.</span></span>

## <a name="creating-a-media-source"></a><span data-ttu-id="142ed-130">建立媒體來源</span><span class="sxs-lookup"><span data-stu-id="142ed-130">Creating a Media Source</span></span>

<span data-ttu-id="142ed-131">媒體來源是讀取和剖析來源檔案的物件。</span><span class="sxs-lookup"><span data-stu-id="142ed-131">A media source is an object that reads and parses the source file.</span></span> <span data-ttu-id="142ed-132">若要建立媒體來源，請使用 [來源解析程式](source-resolver.md)。</span><span class="sxs-lookup"><span data-stu-id="142ed-132">To create a media source, use the [Source Resolver](source-resolver.md).</span></span> <span data-ttu-id="142ed-133">您可以 [使用來源解析程式](using-the-source-resolver.md)，在主題中找到範例程式碼。</span><span class="sxs-lookup"><span data-stu-id="142ed-133">You can find example code in the topic [Using the Source Resolver](using-the-source-resolver.md).</span></span>

## <a name="creating-a-transcode-profile"></a><span data-ttu-id="142ed-134">建立轉碼設定檔</span><span class="sxs-lookup"><span data-stu-id="142ed-134">Creating a Transcode Profile</span></span>

<span data-ttu-id="142ed-135">*轉碼設定檔* 說明用來編碼輸出檔的格式和設定。</span><span class="sxs-lookup"><span data-stu-id="142ed-135">A *transcode profile* describes the format and settings that are used to encode the output file.</span></span> <span data-ttu-id="142ed-136">轉碼設定檔包含三組屬性：</span><span class="sxs-lookup"><span data-stu-id="142ed-136">The transcode profile contains three sets of attributes:</span></span>

-   <span data-ttu-id="142ed-137">音訊屬性：描述目標音訊格式和音訊編碼器設定。</span><span class="sxs-lookup"><span data-stu-id="142ed-137">Audio attributes: Describe the target audio format and audio encoder settings.</span></span>
-   <span data-ttu-id="142ed-138">影片屬性：描述目標影片格式和影片編碼器設定。</span><span class="sxs-lookup"><span data-stu-id="142ed-138">Video attributes: Describe the target video format and video encoder settings.</span></span>
-   <span data-ttu-id="142ed-139">容器屬性：定義檔案容器的類型，以及某些全域編碼設定。</span><span class="sxs-lookup"><span data-stu-id="142ed-139">Container attributes: Define the type of file container, as well as some global encoding settings.</span></span>

<span data-ttu-id="142ed-140">若要建立轉碼設定檔，請呼叫 [**MFCreateTranscodeProfile**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodeprofile) 函數。</span><span class="sxs-lookup"><span data-stu-id="142ed-140">To create a transcode profile, call the [**MFCreateTranscodeProfile**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodeprofile) function.</span></span> <span data-ttu-id="142ed-141">此函數會傳回 [**IMFTranscodeProfile**](/windows/desktop/api/mfidl/nn-mfidl-imftranscodeprofile) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="142ed-141">This function returns a pointer to the [**IMFTranscodeProfile**](/windows/desktop/api/mfidl/nn-mfidl-imftranscodeprofile) interface.</span></span> <span data-ttu-id="142ed-142">初始設定檔物件是空的;它不包含任何屬性。</span><span class="sxs-lookup"><span data-stu-id="142ed-142">The initial profile object is empty; it contains no attributes.</span></span> <span data-ttu-id="142ed-143">下一步是加入定義設定檔的屬性。</span><span class="sxs-lookup"><span data-stu-id="142ed-143">The next step is to add the attributes that define the profile.</span></span>

### <a name="audio-attributes"></a><span data-ttu-id="142ed-144">音訊屬性</span><span class="sxs-lookup"><span data-stu-id="142ed-144">Audio Attributes</span></span>

<span data-ttu-id="142ed-145">若要加入音訊資料流程的屬性，請呼叫 [**IMFTranscodeProfile：： SetAudioAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setaudioattributes)。</span><span class="sxs-lookup"><span data-stu-id="142ed-145">To add attributes for the audio stream, call [**IMFTranscodeProfile::SetAudioAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setaudioattributes).</span></span> <span data-ttu-id="142ed-146">這些屬性會指定音訊串流的編碼方式。</span><span class="sxs-lookup"><span data-stu-id="142ed-146">These attributes specify how the audio stream is encoded.</span></span> <span data-ttu-id="142ed-147">如果輸出檔案不會包含音訊資料流程，請省略這些屬性。</span><span class="sxs-lookup"><span data-stu-id="142ed-147">If the output file will not contain an audio stream, omit these attributes.</span></span>

<span data-ttu-id="142ed-148">音訊屬性分為兩類：</span><span class="sxs-lookup"><span data-stu-id="142ed-148">Audio attributes fall into two categories:</span></span>

-   <span data-ttu-id="142ed-149">指定編碼資料流程格式的屬性</span><span class="sxs-lookup"><span data-stu-id="142ed-149">Attributes that specify the format of the encoded stream</span></span>
-   <span data-ttu-id="142ed-150">指定其他編碼參數的屬性。</span><span class="sxs-lookup"><span data-stu-id="142ed-150">Attributes that specify other encoding parameters.</span></span>

<span data-ttu-id="142ed-151">格式屬性只是媒體類型的屬性，如 [音訊媒體類型](audio-media-types.md)一節中所述。</span><span class="sxs-lookup"><span data-stu-id="142ed-151">Format attributes are simply media-type attributes, as described in the section [Audio Media Types](audio-media-types.md).</span></span> <span data-ttu-id="142ed-152">確切的格式屬性集會視編碼器而定。</span><span class="sxs-lookup"><span data-stu-id="142ed-152">The exact set of format attributes depends on the encoder.</span></span> <span data-ttu-id="142ed-153"> ([在媒體基礎中查看支援的媒體格式](supported-media-formats-in-media-foundation.md)。 ) 以下是典型的音訊格式屬性清單：</span><span class="sxs-lookup"><span data-stu-id="142ed-153">(See [Supported Media Formats in Media Foundation](supported-media-formats-in-media-foundation.md).) Here is a list of typical audio format attributes:</span></span>



| <span data-ttu-id="142ed-154">Format 屬性</span><span class="sxs-lookup"><span data-stu-id="142ed-154">Format Attribute</span></span>                                                                         | <span data-ttu-id="142ed-155">Description</span><span class="sxs-lookup"><span data-stu-id="142ed-155">Description</span></span>                                                      |
|------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="142ed-156">MF \_ MT \_ 子類型</span><span class="sxs-lookup"><span data-stu-id="142ed-156">MF\_MT\_SUBTYPE</span></span>](mf-mt-subtype-attribute.md)                                           | <span data-ttu-id="142ed-157">子型別。</span><span class="sxs-lookup"><span data-stu-id="142ed-157">The subtype.</span></span> <span data-ttu-id="142ed-158">請參閱 [音訊子類型 guid](audio-subtype-guids.md)。</span><span class="sxs-lookup"><span data-stu-id="142ed-158">See [Audio Subtype GUIDs](audio-subtype-guids.md).</span></span> |
| [<span data-ttu-id="142ed-159">MF \_ MT \_ 音訊 \_ 數目 \_ 通道</span><span class="sxs-lookup"><span data-stu-id="142ed-159">MF\_MT\_AUDIO\_NUM\_CHANNELS</span></span>](mf-mt-audio-num-channels-attribute.md)                   | <span data-ttu-id="142ed-160">音訊頻道的數目。</span><span class="sxs-lookup"><span data-stu-id="142ed-160">The number of audio channels.</span></span>                                    |
| [<span data-ttu-id="142ed-161">\_每秒的 MF MT \_ 音訊 \_ 範例 \_ \_</span><span class="sxs-lookup"><span data-stu-id="142ed-161">MF\_MT\_AUDIO\_SAMPLES\_PER\_SECOND</span></span>](mf-mt-audio-samples-per-second-attribute.md)      | <span data-ttu-id="142ed-162">每秒音訊樣本數。</span><span class="sxs-lookup"><span data-stu-id="142ed-162">The number of audio samples per second.</span></span>                          |
| [<span data-ttu-id="142ed-163">MF \_ MT \_ 音訊 \_ 區塊 \_ 對齊</span><span class="sxs-lookup"><span data-stu-id="142ed-163">MF\_MT\_AUDIO\_BLOCK\_ALIGNMENT</span></span>](mf-mt-audio-block-alignment-attribute.md)             | <span data-ttu-id="142ed-164">區塊對齊。</span><span class="sxs-lookup"><span data-stu-id="142ed-164">The block alignment.</span></span>                                             |
| [<span data-ttu-id="142ed-165">\_每秒的 MF MT \_ 音訊 \_ 平均 \_ 位元組數 \_ \_</span><span class="sxs-lookup"><span data-stu-id="142ed-165">MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND</span></span>](mf-mt-audio-avg-bytes-per-second-attribute.md) | <span data-ttu-id="142ed-166">每秒的平均位元組數目 (編碼的位速率) 。</span><span class="sxs-lookup"><span data-stu-id="142ed-166">The average number of bytes per second (the encoded bit rate).</span></span>   |



 

<span data-ttu-id="142ed-167">已定義下列編碼參數。</span><span class="sxs-lookup"><span data-stu-id="142ed-167">The following encoding parameters are defined.</span></span>



| <span data-ttu-id="142ed-168">編碼參數</span><span class="sxs-lookup"><span data-stu-id="142ed-168">Encoding Parameter</span></span>                                                             | <span data-ttu-id="142ed-169">Description</span><span class="sxs-lookup"><span data-stu-id="142ed-169">Description</span></span>                                                                |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [<span data-ttu-id="142ed-170">MF \_ 轉碼 \_ 沒有 \_ 插入 \_ 編碼器</span><span class="sxs-lookup"><span data-stu-id="142ed-170">MF\_TRANSCODE\_DONOT\_INSERT\_ENCODER</span></span>](mf-transcode-donot-insert-encoder.md) | <span data-ttu-id="142ed-171">防止轉碼 API 插入音訊串流的編碼器。</span><span class="sxs-lookup"><span data-stu-id="142ed-171">Prevents the transcode API from inserting an encoder for the audio stream.</span></span> |
| [<span data-ttu-id="142ed-172">MF \_ 轉碼 \_ ENCODINGPROFILE</span><span class="sxs-lookup"><span data-stu-id="142ed-172">MF\_TRANSCODE\_ENCODINGPROFILE</span></span>](mf-transcode-encodingprofile.md)             | <span data-ttu-id="142ed-173">指定裝置一致性範本。</span><span class="sxs-lookup"><span data-stu-id="142ed-173">Specifies the device conformance template.</span></span> <span data-ttu-id="142ed-174"> (僅適用于 ASF 檔案。 ) </span><span class="sxs-lookup"><span data-stu-id="142ed-174">(Applies only to ASF files.)</span></span>    |
| [<span data-ttu-id="142ed-175">MF \_ 轉碼 \_ QUALITYVSSPEED</span><span class="sxs-lookup"><span data-stu-id="142ed-175">MF\_TRANSCODE\_QUALITYVSSPEED</span></span>](mf-transcode-qualityvsspeed.md)               | <span data-ttu-id="142ed-176">指定編碼品質與速度之間的取捨。</span><span class="sxs-lookup"><span data-stu-id="142ed-176">Specifies the trade-off between encoding quality and speed.</span></span>                |



 

<span data-ttu-id="142ed-177">您必須設定格式屬性。</span><span class="sxs-lookup"><span data-stu-id="142ed-177">You must set the format attributes.</span></span> <span data-ttu-id="142ed-178">編碼參數是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="142ed-178">The encoding parameters are optional.</span></span>

<span data-ttu-id="142ed-179">若要尋找與編碼器相容的格式，其中一種方式就是呼叫 [**MFTranscodeGetAudioOutputAvailableTypes**](/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes) 函式。</span><span class="sxs-lookup"><span data-stu-id="142ed-179">One way to find a format that is compatible with the encoder is to call the [**MFTranscodeGetAudioOutputAvailableTypes**](/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes) function.</span></span> <span data-ttu-id="142ed-180">所需的編碼器是由子類型所指定。</span><span class="sxs-lookup"><span data-stu-id="142ed-180">The desired encoder is specified by subtype.</span></span> <span data-ttu-id="142ed-181">函數會傳回該編碼器的媒體類型集合。</span><span class="sxs-lookup"><span data-stu-id="142ed-181">The function returns a collection of media types for that encoder.</span></span> <span data-ttu-id="142ed-182">您可以從清單中選取類型，並將屬性複製到設定檔。</span><span class="sxs-lookup"><span data-stu-id="142ed-182">You can select a type from the list and copy the attributes to the profile.</span></span> <span data-ttu-id="142ed-183">如需使用這種方法的範例程式碼，請參閱 [教學課程：編碼 WMA](tutorial--converting-an-mp3-file-to-a-wma-file.md)檔案。</span><span class="sxs-lookup"><span data-stu-id="142ed-183">For example code that uses this approach, see [Tutorial: Encoding a WMA File](tutorial--converting-an-mp3-file-to-a-wma-file.md).</span></span>

### <a name="video-attributes"></a><span data-ttu-id="142ed-184">影片屬性</span><span class="sxs-lookup"><span data-stu-id="142ed-184">Video Attributes</span></span>

<span data-ttu-id="142ed-185">若要加入影片資料流程的屬性，請呼叫 [**IMFTranscodeProfile：： SetVideoAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setvideoattributes)。</span><span class="sxs-lookup"><span data-stu-id="142ed-185">To add attributes for the video stream, call [**IMFTranscodeProfile::SetVideoAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setvideoattributes).</span></span> <span data-ttu-id="142ed-186">這些屬性會指定影片串流的編碼方式。</span><span class="sxs-lookup"><span data-stu-id="142ed-186">These attributes specify how the video stream is encoded.</span></span> <span data-ttu-id="142ed-187">如果輸出檔案不會包含影片資料流程，請省略這些屬性。</span><span class="sxs-lookup"><span data-stu-id="142ed-187">If the output file will not contain a video stream, omit these attributes.</span></span>

<span data-ttu-id="142ed-188">如同音訊屬性，影片屬性分為兩類：</span><span class="sxs-lookup"><span data-stu-id="142ed-188">As with audio attributes, the video attributes fall into two categories:</span></span>

-   <span data-ttu-id="142ed-189">指定編碼資料流程格式的屬性</span><span class="sxs-lookup"><span data-stu-id="142ed-189">Attributes that specify the format of the encoded stream</span></span>
-   <span data-ttu-id="142ed-190">指定其他編碼參數的屬性。</span><span class="sxs-lookup"><span data-stu-id="142ed-190">Attributes that specify other encoding parameters.</span></span>

<span data-ttu-id="142ed-191">格式屬性是媒體類型的屬性，如 [影片媒體類型](video-media-types.md)一節中所述。</span><span class="sxs-lookup"><span data-stu-id="142ed-191">Format attributes are media-type attributes, as described in the section [Video Media Types](video-media-types.md).</span></span> <span data-ttu-id="142ed-192">以下是典型的影片格式屬性清單：</span><span class="sxs-lookup"><span data-stu-id="142ed-192">Here is a list of typical video format attributes:</span></span>



| <span data-ttu-id="142ed-193">Format 屬性</span><span class="sxs-lookup"><span data-stu-id="142ed-193">Format Attribute</span></span>                                                       | <span data-ttu-id="142ed-194">Description</span><span class="sxs-lookup"><span data-stu-id="142ed-194">Description</span></span>                                                      |
|------------------------------------------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="142ed-195">MF \_ MT \_ 子類型</span><span class="sxs-lookup"><span data-stu-id="142ed-195">MF\_MT\_SUBTYPE</span></span>](mf-mt-subtype-attribute.md)                         | <span data-ttu-id="142ed-196">子型別。</span><span class="sxs-lookup"><span data-stu-id="142ed-196">The subtype.</span></span> <span data-ttu-id="142ed-197">請參閱 [影片子類型 guid](video-subtype-guids.md)。</span><span class="sxs-lookup"><span data-stu-id="142ed-197">See [Video Subtype GUIDs](video-subtype-guids.md).</span></span> |
| [<span data-ttu-id="142ed-198">MF \_ MT \_ 幀 \_ 速率</span><span class="sxs-lookup"><span data-stu-id="142ed-198">MF\_MT\_FRAME\_RATE</span></span>](mf-mt-frame-rate-attribute.md)                  | <span data-ttu-id="142ed-199">畫面播放速率。</span><span class="sxs-lookup"><span data-stu-id="142ed-199">The frame rate.</span></span>                                                  |
| [<span data-ttu-id="142ed-200">MF \_ MT \_ 框架 \_ 大小</span><span class="sxs-lookup"><span data-stu-id="142ed-200">MF\_MT\_FRAME\_SIZE</span></span>](mf-mt-frame-size-attribute.md)                  | <span data-ttu-id="142ed-201">框架大小。</span><span class="sxs-lookup"><span data-stu-id="142ed-201">The frame size.</span></span>                                                  |
| [<span data-ttu-id="142ed-202">**MF \_ MT \_ 平均 \_ 位元速率**</span><span class="sxs-lookup"><span data-stu-id="142ed-202">**MF\_MT\_AVG\_BITRATE**</span></span>](mf-mt-avg-bitrate-attribute.md)            | <span data-ttu-id="142ed-203">平均位元速率。</span><span class="sxs-lookup"><span data-stu-id="142ed-203">The average bit rate.</span></span>                                            |
| [<span data-ttu-id="142ed-204">MF \_ MT \_ 圖元 \_ 外觀 \_ 比例</span><span class="sxs-lookup"><span data-stu-id="142ed-204">MF\_MT\_PIXEL\_ASPECT\_RATIO</span></span>](mf-mt-pixel-aspect-ratio-attribute.md) | <span data-ttu-id="142ed-205">圖元外觀比例。</span><span class="sxs-lookup"><span data-stu-id="142ed-205">The pixel aspect ratio.</span></span>                                          |



 

<span data-ttu-id="142ed-206">已定義下列編碼參數。</span><span class="sxs-lookup"><span data-stu-id="142ed-206">The following encoding parameters are defined.</span></span>



| <span data-ttu-id="142ed-207">編碼參數</span><span class="sxs-lookup"><span data-stu-id="142ed-207">Encoding Parameter</span></span>                                                             | <span data-ttu-id="142ed-208">Description</span><span class="sxs-lookup"><span data-stu-id="142ed-208">Description</span></span>                                                                |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [<span data-ttu-id="142ed-209">MF \_ 轉碼 \_ 沒有 \_ 插入 \_ 編碼器</span><span class="sxs-lookup"><span data-stu-id="142ed-209">MF\_TRANSCODE\_DONOT\_INSERT\_ENCODER</span></span>](mf-transcode-donot-insert-encoder.md) | <span data-ttu-id="142ed-210">防止轉碼 API 插入影片串流的編碼器。</span><span class="sxs-lookup"><span data-stu-id="142ed-210">Prevents the transcode API from inserting an encoder for the video stream.</span></span> |
| [<span data-ttu-id="142ed-211">MF \_ 轉碼 \_ ENCODINGPROFILE</span><span class="sxs-lookup"><span data-stu-id="142ed-211">MF\_TRANSCODE\_ENCODINGPROFILE</span></span>](mf-transcode-encodingprofile.md)             | <span data-ttu-id="142ed-212">指定裝置一致性範本。</span><span class="sxs-lookup"><span data-stu-id="142ed-212">Specifies the device conformance template.</span></span> <span data-ttu-id="142ed-213"> (僅適用于 ASF 檔案。 ) </span><span class="sxs-lookup"><span data-stu-id="142ed-213">(Applies only to ASF files.)</span></span>    |
| [<span data-ttu-id="142ed-214">MF \_ 轉碼 \_ QUALITYVSSPEED</span><span class="sxs-lookup"><span data-stu-id="142ed-214">MF\_TRANSCODE\_QUALITYVSSPEED</span></span>](mf-transcode-qualityvsspeed.md)               | <span data-ttu-id="142ed-215">指定編碼品質與速度之間的取捨。</span><span class="sxs-lookup"><span data-stu-id="142ed-215">Specifies the trade-off between encoding quality and speed.</span></span>                |



 

<span data-ttu-id="142ed-216">您必須設定格式屬性。</span><span class="sxs-lookup"><span data-stu-id="142ed-216">You must set the format attributes.</span></span> <span data-ttu-id="142ed-217">編碼參數是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="142ed-217">The encoding parameters are optional.</span></span>

### <a name="container-attributes"></a><span data-ttu-id="142ed-218">容器屬性</span><span class="sxs-lookup"><span data-stu-id="142ed-218">Container Attributes</span></span>

<span data-ttu-id="142ed-219">容器屬性會定義輸出檔案的檔案層級特性。</span><span class="sxs-lookup"><span data-stu-id="142ed-219">Container attributes define file-level characteristics of the output file.</span></span> <span data-ttu-id="142ed-220">若要設定容器屬性，請呼叫 [**IMFTranscodeProfile：： SetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes)。</span><span class="sxs-lookup"><span data-stu-id="142ed-220">To set container attributes, call [**IMFTranscodeProfile::SetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes).</span></span> <span data-ttu-id="142ed-221">會定義下列屬性。</span><span class="sxs-lookup"><span data-stu-id="142ed-221">The following attributes are defined.</span></span>



| <span data-ttu-id="142ed-222">屬性</span><span class="sxs-lookup"><span data-stu-id="142ed-222">Attribute</span></span>                                                                          | <span data-ttu-id="142ed-223">描述</span><span class="sxs-lookup"><span data-stu-id="142ed-223">Description</span></span>                                                                                                                                            |
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="142ed-224">MF \_ 轉碼 \_ 調整 \_ 設定檔</span><span class="sxs-lookup"><span data-stu-id="142ed-224">MF\_TRANSCODE\_ADJUST\_PROFILE</span></span>](mf-transcode-adjust-profile.md)                  | <span data-ttu-id="142ed-225">定義要用於轉碼拓撲的資料流程設定。</span><span class="sxs-lookup"><span data-stu-id="142ed-225">Defines the stream settings to use for the transcode topology.</span></span> <span data-ttu-id="142ed-226">您可以設定旗標使用輸入來源設定，或使用自訂資料流程屬性。</span><span class="sxs-lookup"><span data-stu-id="142ed-226">You can set the flags to use the input source settings or use custom stream attributes.</span></span> |
| [<span data-ttu-id="142ed-227">MF \_ 轉碼 \_ CONTAINERTYPE</span><span class="sxs-lookup"><span data-stu-id="142ed-227">MF\_TRANSCODE\_CONTAINERTYPE</span></span>](mf-transcode-containertype.md)                     | <span data-ttu-id="142ed-228">指定輸出檔的檔案格式，例如「數量」或「ASF」。</span><span class="sxs-lookup"><span data-stu-id="142ed-228">Specifies the file format of the output file, such as MP4 or ASF.</span></span> <span data-ttu-id="142ed-229">根據此值，會將適當的媒體接收器新增至拓撲。</span><span class="sxs-lookup"><span data-stu-id="142ed-229">Based on this value, the appropriate media sink is added to the topology.</span></span>            |
| [<span data-ttu-id="142ed-230">MF \_ 轉碼 \_ 略過 \_ 中繼資料 \_ 傳輸</span><span class="sxs-lookup"><span data-stu-id="142ed-230">MF\_TRANSCODE\_SKIP\_METADATA\_TRANSFER</span></span>](mf-transcode-skip-metadata-transfer.md) | <span data-ttu-id="142ed-231">指定是否將來源的中繼資料複製到輸出檔。</span><span class="sxs-lookup"><span data-stu-id="142ed-231">Specifies whether metadata from the source is copied to the output file.</span></span>                                                                               |
| [<span data-ttu-id="142ed-232">MF \_ 轉碼 \_ TOPOLOGYMODE</span><span class="sxs-lookup"><span data-stu-id="142ed-232">MF\_TRANSCODE\_TOPOLOGYMODE</span></span>](mf-transcode-topologymode.md)                       | <span data-ttu-id="142ed-233">指定轉碼期間是否可使用以硬體為基礎的編解碼器。</span><span class="sxs-lookup"><span data-stu-id="142ed-233">Specifies whether hardware-based codecs may be used during transcoding.</span></span>                                                                                |
| [<span data-ttu-id="142ed-234">MFT \_ FIELDOFUSE \_ 解除鎖定 \_ 屬性</span><span class="sxs-lookup"><span data-stu-id="142ed-234">MFT\_FIELDOFUSE\_UNLOCK\_Attribute</span></span>](mft-fieldofuse-unlock-attribute.md)          | <span data-ttu-id="142ed-235">解除鎖定具有使用規定限制的編解碼器。</span><span class="sxs-lookup"><span data-stu-id="142ed-235">Unlocks a codec that has field-of-use restrictions.</span></span> <span data-ttu-id="142ed-236">如需詳細資訊，請參閱 [使用限制欄位](field-of-use-restrictions.md)。</span><span class="sxs-lookup"><span data-stu-id="142ed-236">For more information, see [Field of Use Restrictions](field-of-use-restrictions.md).</span></span>              |



 

<span data-ttu-id="142ed-237">需要有 [MF \_ 轉碼 \_ CONTAINERTYPE](mf-transcode-containertype.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="142ed-237">The [MF\_TRANSCODE\_CONTAINERTYPE](mf-transcode-containertype.md) attribute is required.</span></span> <span data-ttu-id="142ed-238">其他容器屬性是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="142ed-238">The other container attributes are optional.</span></span>

## <a name="creating-a-transcode-topology"></a><span data-ttu-id="142ed-239">建立轉碼拓撲</span><span class="sxs-lookup"><span data-stu-id="142ed-239">Creating a Transcode Topology</span></span>

<span data-ttu-id="142ed-240">轉碼拓撲是部分拓撲，其中包含媒體來源、適當的編解碼器和媒體接收器。</span><span class="sxs-lookup"><span data-stu-id="142ed-240">The transcode topology is a partial topology that contains the media source, the appropriate codecs, and the media sink.</span></span> <span data-ttu-id="142ed-241">若要建立轉碼拓撲，請呼叫 [**MFCreateTranscodeTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodetopology) 函數。</span><span class="sxs-lookup"><span data-stu-id="142ed-241">To create the transcode topology, call to the [**MFCreateTranscodeTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodetopology) function.</span></span> <span data-ttu-id="142ed-242">此函式會採用下列參數作為輸入：</span><span class="sxs-lookup"><span data-stu-id="142ed-242">This function takes the following parameters as input:</span></span>

-   <span data-ttu-id="142ed-243">媒體來源之 [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="142ed-243">A pointer to the [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) interface of the media source.</span></span>
-   <span data-ttu-id="142ed-244">輸出檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="142ed-244">The name of the output file.</span></span>
-   <span data-ttu-id="142ed-245">轉碼設定檔之 [**IMFTranscodeProfile**](/windows/desktop/api/mfidl/nn-mfidl-imftranscodeprofile) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="142ed-245">A pointer to the [**IMFTranscodeProfile**](/windows/desktop/api/mfidl/nn-mfidl-imftranscodeprofile) interface of the transcode profile.</span></span>

<span data-ttu-id="142ed-246">函數會傳回 [**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="142ed-246">The function returns a pointer to the [**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) interface.</span></span>

## <a name="running-the-encoding-session"></a><span data-ttu-id="142ed-247">正在執行編碼會話</span><span class="sxs-lookup"><span data-stu-id="142ed-247">Running the Encoding Session</span></span>

<span data-ttu-id="142ed-248">建立拓撲之後，您就可以開始將檔案編碼。</span><span class="sxs-lookup"><span data-stu-id="142ed-248">After you create the topology, you are ready to encode the file.</span></span> <span data-ttu-id="142ed-249">您可以在此時捨棄設定檔。</span><span class="sxs-lookup"><span data-stu-id="142ed-249">You can discard the profile at this point.</span></span>

1.  <span data-ttu-id="142ed-250">呼叫 [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) 來建立媒體會話。</span><span class="sxs-lookup"><span data-stu-id="142ed-250">Call [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) to create the Media Session.</span></span>
2.  <span data-ttu-id="142ed-251">呼叫 [**IMFMediaSession：： SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) 來設定媒體會話上的拓撲。</span><span class="sxs-lookup"><span data-stu-id="142ed-251">Call [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) to set the topology on the Media Session.</span></span>
3.  <span data-ttu-id="142ed-252">呼叫 [**IMFMediaSession：： start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) 以開始編碼會話。</span><span class="sxs-lookup"><span data-stu-id="142ed-252">Call [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) to start the encoding session.</span></span>
4.  <span data-ttu-id="142ed-253">等候 [MESessionEnded](mesessionended.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="142ed-253">Wait for the [MESessionEnded](mesessionended.md) event.</span></span>
5.  <span data-ttu-id="142ed-254">呼叫 [**IMFMediaSession：： close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) 以關閉媒體會話。</span><span class="sxs-lookup"><span data-stu-id="142ed-254">Call [**IMFMediaSession::Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) to close the Media Session.</span></span>
6.  <span data-ttu-id="142ed-255">等候 [MESessionClosed](mesessionclosed.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="142ed-255">Wait for the [MESessionClosed](mesessionclosed.md) event.</span></span>
7.  <span data-ttu-id="142ed-256">呼叫 [**IMFMediaSource：： Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown)。</span><span class="sxs-lookup"><span data-stu-id="142ed-256">Call [**IMFMediaSource::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown).</span></span>
8.  <span data-ttu-id="142ed-257">呼叫 [**IMFMediaSession：： Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown)。</span><span class="sxs-lookup"><span data-stu-id="142ed-257">Call [**IMFMediaSession::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown).</span></span>

<span data-ttu-id="142ed-258">在步驟3和4之間進行編碼所花費的時間大多很久。</span><span class="sxs-lookup"><span data-stu-id="142ed-258">Most of the time spent encoding occurs between steps 3 and 4.</span></span>

## <a name="related-topics"></a><span data-ttu-id="142ed-259">相關主題</span><span class="sxs-lookup"><span data-stu-id="142ed-259">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="142ed-260">轉碼 API</span><span class="sxs-lookup"><span data-stu-id="142ed-260">Transcode API</span></span>](transcode-api.md)
</dt> <dt>

[<span data-ttu-id="142ed-261">關於媒體會話</span><span class="sxs-lookup"><span data-stu-id="142ed-261">About the Media Session</span></span>](about-the-media-session.md)
</dt> </dl>

 

 



