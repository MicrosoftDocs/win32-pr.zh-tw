---
description: 本主題概述 Microsoft 媒體基礎中提供的檔案編碼 Api。
ms.assetid: 69dbef63-e272-4ad2-8d04-ae9366f79b33
title: 媒體基礎中的編碼總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81882bd6da43f4040614347b662d988844c7b7a6
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "104559715"
---
# <a name="overview-of-encoding-in-media-foundation"></a><span data-ttu-id="7b54a-103">媒體基礎中的編碼總覽</span><span class="sxs-lookup"><span data-stu-id="7b54a-103">Overview of Encoding in Media Foundation</span></span>

<span data-ttu-id="7b54a-104">本主題概述 Microsoft 媒體基礎中提供的檔案編碼 Api。</span><span class="sxs-lookup"><span data-stu-id="7b54a-104">This topic is an overview of the file encoding APIs provided in Microsoft Media Foundation.</span></span>

## <a name="terminology"></a><span data-ttu-id="7b54a-105">詞彙</span><span class="sxs-lookup"><span data-stu-id="7b54a-105">Terminology</span></span>

<span data-ttu-id="7b54a-106">*編碼* 是涵蓋數個不同程式的一般詞彙：</span><span class="sxs-lookup"><span data-stu-id="7b54a-106">*Encoding* is a general term that covers several distinct processes:</span></span>

1.  <span data-ttu-id="7b54a-107">將音訊或影片串流編碼為壓縮格式。</span><span class="sxs-lookup"><span data-stu-id="7b54a-107">Encoding an audio or video stream into a compressed formats.</span></span> <span data-ttu-id="7b54a-108">例如，將影片串流編碼為 h.264 video。</span><span class="sxs-lookup"><span data-stu-id="7b54a-108">For example, encoding a video stream to H.264 video.</span></span>
2.  <span data-ttu-id="7b54a-109">多工 ( "muxing" ) 一個或多個資料流程轉換成單一位元組資料流程。</span><span class="sxs-lookup"><span data-stu-id="7b54a-109">Multiplexing ("muxing") one or more streams into a single byte stream.</span></span> <span data-ttu-id="7b54a-110">一般而言，傳入的資料流程會先進行編碼。</span><span class="sxs-lookup"><span data-stu-id="7b54a-110">Typically, the incoming streams are encoded first.</span></span> <span data-ttu-id="7b54a-111">此步驟可能涉及 packetizing 編碼的資料流程。</span><span class="sxs-lookup"><span data-stu-id="7b54a-111">This step might involve packetizing the encoded streams.</span></span>
3.  <span data-ttu-id="7b54a-112">將多工位元組資料流程寫入至檔案（例如，使用檔或 Advanced 系統格式） (ASF) 檔。</span><span class="sxs-lookup"><span data-stu-id="7b54a-112">Writing a multiplexed byte stream to a file, such as an MP4 or Advanced Systems Format (ASF) file.</span></span> <span data-ttu-id="7b54a-113">或者，您也可以透過網路傳送多工資料流程。</span><span class="sxs-lookup"><span data-stu-id="7b54a-113">Alternatively, the multiplexed stream can be sent over the network.</span></span>

<span data-ttu-id="7b54a-114">下圖顯示這三個進程：</span><span class="sxs-lookup"><span data-stu-id="7b54a-114">The following diagram shows these three processes:</span></span>

![顯示編碼和多工處理常式的圖表](images/encoding03.png)

<span data-ttu-id="7b54a-116">此流程的變化包括轉碼和 remuxing：</span><span class="sxs-lookup"><span data-stu-id="7b54a-116">Variations of this process include transcoding and remuxing:</span></span>

-   <span data-ttu-id="7b54a-117">*轉碼* 表示解碼現有的檔案、重新編碼資料流程，以及重新多工編碼的資料流程。</span><span class="sxs-lookup"><span data-stu-id="7b54a-117">*Transcoding* means decoding an existing file, re-encoding the streams, and re-multiplexing the encoded streams.</span></span> <span data-ttu-id="7b54a-118">您可以執行轉碼來將檔案從某種編碼類型轉換成另一種編碼類型;例如，若要將 h.264 video 轉換成 Windows Media 視訊 (WMV) 。</span><span class="sxs-lookup"><span data-stu-id="7b54a-118">Transcoding might be done to convert a file from one encoding type to another; for example, to convert H.264 video to Windows Media Video (WMV).</span></span> <span data-ttu-id="7b54a-119">也可以這樣做來變更編碼的位元速率。影片框架大小;畫面播放速率;或其他格式參數。</span><span class="sxs-lookup"><span data-stu-id="7b54a-119">It can also be done to change the encoded bit rate; the video frame size; the frame rate; or other format parameters.</span></span>
-   <span data-ttu-id="7b54a-120">*Remultiplexing* 或 *remuxing* 表示分離信號檔案並重新多工處理資料流程，而不使用解碼/編碼步驟。</span><span class="sxs-lookup"><span data-stu-id="7b54a-120">*Remultiplexing* or *remuxing* means demultiplexing a file and re-multiplexing the streams, with no decode/encode step.</span></span> <span data-ttu-id="7b54a-121">這可能是為了變更音訊/影片封包的多工處理方式、移除資料流程或合併來自兩個不同來源檔案的資料流程。</span><span class="sxs-lookup"><span data-stu-id="7b54a-121">This might be done to change how the audio/video packets are multiplexed, to remove a stream, or to combine streams from two different source files.</span></span>
-   <span data-ttu-id="7b54a-122">*Transrating* 是轉碼的特殊案例，其中的位元速率會變更，而不會變更壓縮類型。</span><span class="sxs-lookup"><span data-stu-id="7b54a-122">*Transrating* is a special case of transcoding, where the bit-rate is changed without changing the compression type.</span></span> <span data-ttu-id="7b54a-123">例如，您可以將高位元速率檔案轉換成較低的位元速率。</span><span class="sxs-lookup"><span data-stu-id="7b54a-123">For example, you might convert a high-bit-rate file to a lower bit-rate.</span></span> <span data-ttu-id="7b54a-124">Transrating 可能使用的一般案例是將媒體內容從電腦同步處理到可攜式裝置。</span><span class="sxs-lookup"><span data-stu-id="7b54a-124">A typical scenario in which transrating might be used is when synchronizing media content from a PC to a portable device.</span></span> <span data-ttu-id="7b54a-125">如果可攜式裝置不支援較高的位元速率，則檔案可能會在複製到可攜式裝置之前 transrated。</span><span class="sxs-lookup"><span data-stu-id="7b54a-125">If the portable device does not support a high bit rate, the file might be transrated before it is copied to the portable device.</span></span>

<span data-ttu-id="7b54a-126">下列區塊圖顯示轉碼進程。</span><span class="sxs-lookup"><span data-stu-id="7b54a-126">The following block diagram shows the transcoding process.</span></span>

![顯示轉碼進程的圖表](images/encoding05.png)

<span data-ttu-id="7b54a-128">下列區塊圖顯示 remuxing 流程。</span><span class="sxs-lookup"><span data-stu-id="7b54a-128">The following block diagram shows the remuxing process.</span></span>

![顯示 remuxing 流程的圖表](images/encoding06.png)

<span data-ttu-id="7b54a-130">此檔有時會使用詞彙 *編碼* 來同時包含轉碼和 remuxing。</span><span class="sxs-lookup"><span data-stu-id="7b54a-130">This documentation sometimes uses the term *encoding* to include both transcoding and remuxing.</span></span> <span data-ttu-id="7b54a-131">很重要的一點是要區分它們，檔將會注意到差異。</span><span class="sxs-lookup"><span data-stu-id="7b54a-131">When it is important to distinguish between them, the documentation will note the difference.</span></span>

<span data-ttu-id="7b54a-132">另請參閱： [媒體基礎：基本概念](media-foundation-programming--essential-concepts.md)。</span><span class="sxs-lookup"><span data-stu-id="7b54a-132">See also: [Media Foundation: Essential Concepts](media-foundation-programming--essential-concepts.md).</span></span>

## <a name="media-foundation-encoding-architecture"></a><span data-ttu-id="7b54a-133">媒體基礎編碼架構</span><span class="sxs-lookup"><span data-stu-id="7b54a-133">Media Foundation Encoding Architecture</span></span>

<span data-ttu-id="7b54a-134">在媒體基礎架構的最低層級中，會使用下列類型的元件來進行編碼：</span><span class="sxs-lookup"><span data-stu-id="7b54a-134">At the lowest layer of the Media Foundation architecture, the following types of component are used for encoding:</span></span>

-   <span data-ttu-id="7b54a-135">針對轉碼， [媒體來源](media-sources.md) 會用來 demultiplex 原始程式檔。</span><span class="sxs-lookup"><span data-stu-id="7b54a-135">For transcoding, [Media Sources](media-sources.md) are used to demultiplex the source file.</span></span>
-   <span data-ttu-id="7b54a-136">針對編碼程式， [媒體基礎轉換](media-foundation-transforms.md) 會用來將資料流程解碼和編碼。</span><span class="sxs-lookup"><span data-stu-id="7b54a-136">For the encoding process, [Media Foundation Transforms](media-foundation-transforms.md) are used to decode and encode streams.</span></span>
-   <span data-ttu-id="7b54a-137">針對多工處理常式，會使用 [媒體接收器](media-sinks.md) 來多工處理資料流程，並將多工資料流程寫入檔案或網路。</span><span class="sxs-lookup"><span data-stu-id="7b54a-137">For the multiplexing process, [Media Sinks](media-sinks.md) are used to multiplex the streams and write the multiplexed stream to a file or network.</span></span>

<span data-ttu-id="7b54a-138">下圖顯示在轉碼案例中，這些元件之間的資料流程：</span><span class="sxs-lookup"><span data-stu-id="7b54a-138">The following diagram shows the data flow between these components in a transcoding scenario:</span></span>

![顯示轉碼中使用之元件的圖表](images/encoding04.png)

<span data-ttu-id="7b54a-140">大部分的應用程式都不會直接使用這些元件。</span><span class="sxs-lookup"><span data-stu-id="7b54a-140">Most applications will not use these components directly.</span></span> <span data-ttu-id="7b54a-141">相反地，應用程式會使用較高層級的 Api 來管理這些較低層級的元件。</span><span class="sxs-lookup"><span data-stu-id="7b54a-141">Instead, an application will use higher-level APIs that manage these lower-level components.</span></span> <span data-ttu-id="7b54a-142">媒體基礎提供兩個較高層級 Api 來進行編碼：</span><span class="sxs-lookup"><span data-stu-id="7b54a-142">Media Foundation provides two higher-level APIs for encoding:</span></span>

<dl> <dt>

<span data-ttu-id="7b54a-143"><span id="Media_Session"></span><span id="media_session"></span><span id="MEDIA_SESSION"></span>[媒體會話](media-session.md)</span><span class="sxs-lookup"><span data-stu-id="7b54a-143"><span id="Media_Session"></span><span id="media_session"></span><span id="MEDIA_SESSION"></span>[Media Session](media-session.md)</span></span>
</dt> <dd>

<span data-ttu-id="7b54a-144">媒體會話提供端對端管線，可將資料從媒體來源、編解碼器，最後移至媒體接收器。</span><span class="sxs-lookup"><span data-stu-id="7b54a-144">The Media Session provides an end-to-end pipeline that moves data from the media source, through the codecs, and finally to the media sink.</span></span> <span data-ttu-id="7b54a-145">應用程式會控制媒體會話，並接收來自媒體會話的狀態事件。</span><span class="sxs-lookup"><span data-stu-id="7b54a-145">The application controls the Media Session and receives status events from the Media Session.</span></span>

</dd> <dt>

<span data-ttu-id="7b54a-146"><span id="Source_Reader_plus_Sink_Writer"></span><span id="source_reader_plus_sink_writer"></span><span id="SOURCE_READER_PLUS_SINK_WRITER"></span>[來源讀取器](source-reader.md) 加上 [接收寫入器](sink-writer.md)</span><span class="sxs-lookup"><span data-stu-id="7b54a-146"><span id="Source_Reader_plus_Sink_Writer"></span><span id="source_reader_plus_sink_writer"></span><span id="SOURCE_READER_PLUS_SINK_WRITER"></span>[Source Reader](source-reader.md) plus [Sink Writer](sink-writer.md)</span></span>
</dt> <dd>

<span data-ttu-id="7b54a-147">來源讀取器會包裝媒體來源和選擇性的解碼器。</span><span class="sxs-lookup"><span data-stu-id="7b54a-147">The Source Reader wraps the media source and optionally the decoders.</span></span> <span data-ttu-id="7b54a-148">它會為應用程式提供編碼或解碼的範例。</span><span class="sxs-lookup"><span data-stu-id="7b54a-148">It delivers either encoded or decoded samples the application.</span></span> <span data-ttu-id="7b54a-149">接收寫入器會包裝媒體接收和選擇性的編碼器。</span><span class="sxs-lookup"><span data-stu-id="7b54a-149">The Sink Writer wraps the media sink and optionally the encoders.</span></span> <span data-ttu-id="7b54a-150">應用程式會將範例傳遞給接收寫入器。</span><span class="sxs-lookup"><span data-stu-id="7b54a-150">The application passes samples to the Sink Writer.</span></span>

</dd> </dl>

<span data-ttu-id="7b54a-151">下圖顯示媒體會話：</span><span class="sxs-lookup"><span data-stu-id="7b54a-151">The following diagram shows the Media Session:</span></span>

![顯示媒體會話如何執行轉碼的圖表](images/encoding01.png)

<span data-ttu-id="7b54a-153">[轉碼 API](transcode-api.md) (藍色陰影方塊) 是一組在 Windows 7 中引進的 api，可讓您更輕鬆地設定媒體會話以進行編碼。</span><span class="sxs-lookup"><span data-stu-id="7b54a-153">The [Transcode API](transcode-api.md) (the blue shaded box) is a set of APIs introduced in Windows 7, which make it easier to configure the Media Session for encoding.</span></span>

<span data-ttu-id="7b54a-154">下圖顯示來源讀取器和接收寫入器：</span><span class="sxs-lookup"><span data-stu-id="7b54a-154">The next diagram shows the Source Reader and Sink Writer:</span></span>

![顯示具有來源讀取器和接收寫入器之轉碼的圖表](images/encoding02.png)

## <a name="related-topics"></a><span data-ttu-id="7b54a-156">相關主題</span><span class="sxs-lookup"><span data-stu-id="7b54a-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7b54a-157">編碼與檔案編寫</span><span class="sxs-lookup"><span data-stu-id="7b54a-157">Encoding and File Authoring</span></span>](encoding-and-file-authoring.md)
</dt> <dt>

[<span data-ttu-id="7b54a-158">媒體基礎程式設計：基本概念</span><span class="sxs-lookup"><span data-stu-id="7b54a-158">Media Foundation Programming: Essential Concepts</span></span>](media-foundation-programming--essential-concepts.md)
</dt> </dl>

 

 



