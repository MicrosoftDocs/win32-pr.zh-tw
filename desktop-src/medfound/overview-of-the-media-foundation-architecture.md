---
description: 本主題說明 Microsoft 媒體基礎的一般設計。 如需使用媒體基礎進行特定程式設計工作的詳細資訊，請參閱媒體基礎程式設計指南。
ms.assetid: DEA2B19A-CF15-4BF4-84C3-9A6417C942E2
title: 媒體基礎架構的總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0944eae1a74c1a5ba3dda8d94b69088128237f1
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "104551798"
---
# <a name="overview-of-the-media-foundation-architecture"></a><span data-ttu-id="6315b-104">媒體基礎架構的總覽</span><span class="sxs-lookup"><span data-stu-id="6315b-104">Overview of the Media Foundation Architecture</span></span>

<span data-ttu-id="6315b-105">本主題說明 Microsoft 媒體基礎的一般設計。</span><span class="sxs-lookup"><span data-stu-id="6315b-105">This topic describes the general design of Microsoft Media Foundation.</span></span> <span data-ttu-id="6315b-106">如需使用媒體基礎進行特定程式設計工作的詳細資訊，請參閱 [媒體基礎程式設計指南](media-foundation-programming-guide.md)。</span><span class="sxs-lookup"><span data-stu-id="6315b-106">For information about using Media Foundation for specific programming tasks, see [Media Foundation Programming Guide](media-foundation-programming-guide.md).</span></span>

<span data-ttu-id="6315b-107">下圖顯示媒體基礎架構的高階觀點。</span><span class="sxs-lookup"><span data-stu-id="6315b-107">The following diagram shows a high-level view of the Media Foundation architecture.</span></span>

![此圖顯示 media foundation 架構的高階觀點。](images/mfarch01.png)

<span data-ttu-id="6315b-109">媒體基礎提供兩種不同的程式設計模型。</span><span class="sxs-lookup"><span data-stu-id="6315b-109">Media Foundation provides two distinct programming models.</span></span> <span data-ttu-id="6315b-110">圖表左側所顯示的第一個模型會使用媒體資料的端對端管線。</span><span class="sxs-lookup"><span data-stu-id="6315b-110">The first model, shown on the left side of the diagram, uses an end-to-end pipeline for media data.</span></span> <span data-ttu-id="6315b-111">應用程式會初始化管線，例如，藉由提供要播放之檔案的 URL，然後呼叫方法來控制串流。</span><span class="sxs-lookup"><span data-stu-id="6315b-111">The application initializes the pipeline—for example, by providing the URL of a file to play—and then calls methods to control streaming.</span></span> <span data-ttu-id="6315b-112">在第二個模型（顯示于圖表右側）中，應用程式會從來源提取資料，或將資料推送至目的地 (或兩個) 。</span><span class="sxs-lookup"><span data-stu-id="6315b-112">In the second model, shown on the right side of the diagram, the application either pulls data from a source, or pushes it to a destination (or both).</span></span> <span data-ttu-id="6315b-113">如果您需要處理資料，此模型特別有用，因為應用程式可以直接存取資料流程。</span><span class="sxs-lookup"><span data-stu-id="6315b-113">This model is particularly useful if you need to process the data, because the application has direct access to the data stream.</span></span>

### <a name="primitives-and-platform"></a><span data-ttu-id="6315b-114">基本和平臺</span><span class="sxs-lookup"><span data-stu-id="6315b-114">Primitives and Platform</span></span>

<span data-ttu-id="6315b-115">從圖表底部開始， *基本* 專案是在整個媒體基礎 API 中使用的 helper 物件：</span><span class="sxs-lookup"><span data-stu-id="6315b-115">Starting from the bottom of the diagram, the *primitives* are helper objects used throughout the Media Foundation API:</span></span>

-   <span data-ttu-id="6315b-116">[屬性](attributes-and-properties.md) 是在物件內儲存資訊的一般方式，作為索引鍵/值組的清單。</span><span class="sxs-lookup"><span data-stu-id="6315b-116">[Attributes](attributes-and-properties.md) are a generic way to store information inside an object, as a list of key/value pairs.</span></span>
-   <span data-ttu-id="6315b-117">[媒體類型](media-types.md) 描述媒體資料流程的格式。</span><span class="sxs-lookup"><span data-stu-id="6315b-117">[Media Types](media-types.md) describe the format of a media data stream.</span></span>
-   <span data-ttu-id="6315b-118">[媒體緩衝區](media-buffers.md) 會保存媒體資料的區塊，例如影片畫面和音訊範例，並可用來在物件之間傳輸資料。</span><span class="sxs-lookup"><span data-stu-id="6315b-118">[Media Buffers](media-buffers.md) hold chunks of media data, such as video frames and audio samples, and are used to transport data between objects.</span></span>
-   <span data-ttu-id="6315b-119">[媒體範例](media-samples.md) 是媒體緩衝區的容器。</span><span class="sxs-lookup"><span data-stu-id="6315b-119">[Media Samples](media-samples.md) are containers for media buffers.</span></span> <span data-ttu-id="6315b-120">它們也包含有關緩衝區的中繼資料，例如時間戳記。</span><span class="sxs-lookup"><span data-stu-id="6315b-120">They also contain metadata about the buffers, such as time stamps.</span></span>

<span data-ttu-id="6315b-121">[媒體基礎平臺 api](media-foundation-platform-apis.md)提供媒體基礎管線所使用的一些核心功能，例如非同步回呼和工作佇列。</span><span class="sxs-lookup"><span data-stu-id="6315b-121">The [Media Foundation Platform APIs](media-foundation-platform-apis.md) provide some core functionality that is used by the Media Foundation pipeline, such as asynchronous callbacks and work queues.</span></span> <span data-ttu-id="6315b-122">某些應用程式可能需要直接呼叫這些 Api;此外，如果您針對媒體基礎執行自訂來源、轉換或接收，則需要它們。</span><span class="sxs-lookup"><span data-stu-id="6315b-122">Certain applications might need to call these APIs directly; also, you will need them if you implement a custom source, transform, or sink for Media Foundation.</span></span>

### <a name="media-pipeline"></a><span data-ttu-id="6315b-123">媒體管線</span><span class="sxs-lookup"><span data-stu-id="6315b-123">Media Pipeline</span></span>

<span data-ttu-id="6315b-124">媒體管線包含產生或處理媒體資料的三種物件類型：</span><span class="sxs-lookup"><span data-stu-id="6315b-124">The media pipeline contains three types of object that generate or process media data:</span></span>

-   <span data-ttu-id="6315b-125">[媒體來源](media-sources.md) 會將資料導入管線中。</span><span class="sxs-lookup"><span data-stu-id="6315b-125">[Media Sources](media-sources.md) introduce data into the pipeline.</span></span> <span data-ttu-id="6315b-126">媒體來源可能會從本機檔案（例如影片檔案）取得資料;從網路資料流程;或從硬體捕獲裝置。</span><span class="sxs-lookup"><span data-stu-id="6315b-126">A media source might get data from a local file, such as a video file; from a network stream; or from a hardware capture device.</span></span>
-   <span data-ttu-id="6315b-127">[媒體基礎轉換](media-foundation-transforms.md) (MFTs) 處理來自資料流程的資料。</span><span class="sxs-lookup"><span data-stu-id="6315b-127">[Media Foundation Transforms](media-foundation-transforms.md) (MFTs) process data from a stream.</span></span> <span data-ttu-id="6315b-128">編碼器和解碼器會實作為 MFTs。</span><span class="sxs-lookup"><span data-stu-id="6315b-128">Encoders and decoders are implemented as MFTs.</span></span>
-   <span data-ttu-id="6315b-129">[媒體接收器](media-sinks.md) 耗用資料;例如，藉由顯示顯示器上的影片、播放音訊，或將資料寫入媒體檔案。</span><span class="sxs-lookup"><span data-stu-id="6315b-129">[Media Sinks](media-sinks.md) consume the data; for example, by showing video on the display, playing audio, or writing the data to a media file.</span></span>

<span data-ttu-id="6315b-130">協力廠商可以實行自己的自訂來源、接收和 MFTs;例如，支援新的媒體檔案格式。</span><span class="sxs-lookup"><span data-stu-id="6315b-130">Third parties can implement their own custom sources, sinks, and MFTs; for example, to support new media file formats.</span></span>

<span data-ttu-id="6315b-131">[媒體會話](media-session.md)可控制流經管線的資料流程，並處理品質控制、音訊/影片同步處理及回應格式變更等工作。</span><span class="sxs-lookup"><span data-stu-id="6315b-131">The [Media Session](media-session.md) controls the flow of data through the pipeline, and handles tasks such as quality control, audio/video synchronization, and responding to format changes.</span></span>

### <a name="source-reader-and-sink-writer"></a><span data-ttu-id="6315b-132">來源讀取器和接收寫入器</span><span class="sxs-lookup"><span data-stu-id="6315b-132">Source Reader and Sink Writer</span></span>

<span data-ttu-id="6315b-133">[來源讀取](source-reader.md)器和[接收寫入器](sink-writer.md)提供另一種方式，可讓您使用基本媒體基礎元件 (媒體來源、轉換和媒體接收器) 。</span><span class="sxs-lookup"><span data-stu-id="6315b-133">The [Source Reader](source-reader.md) and [Sink Writer](sink-writer.md) provide an alternative way to use the basic Media Foundation components (media sources, transforms, and media sinks).</span></span> <span data-ttu-id="6315b-134">來源讀取器會裝載媒體來源和零或多個編碼器，而接收寫入器則會裝載媒體接收器和零或多個編碼器。</span><span class="sxs-lookup"><span data-stu-id="6315b-134">The source reader hosts a media source and zero or more decoders, while the sink writer hosts a media sink and zero or more encoders.</span></span> <span data-ttu-id="6315b-135">您可以使用來源讀取器從媒體來源取得壓縮或未壓縮的資料，並使用接收寫入器來對資料進行編碼，並將資料傳送至媒體接收。</span><span class="sxs-lookup"><span data-stu-id="6315b-135">You can use the source reader to get compressed or uncompressed data from a media source, and use the sink writer to encode data and send the data to a media sink.</span></span>

> [!Note]  
> <span data-ttu-id="6315b-136">來源讀取器和接收寫入器可在 Windows 7 中取得。</span><span class="sxs-lookup"><span data-stu-id="6315b-136">The source reader and sink writer are available in Windows 7.</span></span>

 

<span data-ttu-id="6315b-137">此程式設計模型可讓應用程式更充分掌控資料的流程，也可讓應用程式直接存取來源的資料。</span><span class="sxs-lookup"><span data-stu-id="6315b-137">This programming model gives the application more control over the flow of data, and also gives the application direct access to the data from the source.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6315b-138">相關主題</span><span class="sxs-lookup"><span data-stu-id="6315b-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6315b-139">媒體基礎：基本概念</span><span class="sxs-lookup"><span data-stu-id="6315b-139">Media Foundation: Essential Concepts</span></span>](media-foundation-programming--essential-concepts.md)
</dt> <dt>

[<span data-ttu-id="6315b-140">媒體基礎架構</span><span class="sxs-lookup"><span data-stu-id="6315b-140">Media Foundation Architecture</span></span>](media-foundation-architecture.md)
</dt> </dl>

 

 



