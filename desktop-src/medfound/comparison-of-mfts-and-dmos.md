---
description: 媒體基礎轉換 (MFTs) 是首次以 DirectX 媒體物件（ (DMOs) ）引進的轉換模型演進。
ms.assetid: 4e8c3ec9-6ffa-4858-a4ea-8ef8ccaf9253
title: MFT 和 DMO 的比較
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e76e128ece1609f25e053486dbb6bcf4578161c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026049"
---
# <a name="comparison-of-mfts-and-dmos"></a><span data-ttu-id="c1d13-103">MFT 和 DMO 的比較</span><span class="sxs-lookup"><span data-stu-id="c1d13-103">Comparison of MFTs and DMOs</span></span>

<span data-ttu-id="c1d13-104">媒體基礎轉換 (MFTs) 是首次以 DirectX 媒體物件（ (DMOs) ）引進的轉換模型演進。</span><span class="sxs-lookup"><span data-stu-id="c1d13-104">Media Foundation transforms (MFTs) are an evolution of the transform model first introduced with DirectX Media Objects (DMOs).</span></span> <span data-ttu-id="c1d13-105">本主題摘要說明 MFTs 與 DMOs 有何不同的主要方式。</span><span class="sxs-lookup"><span data-stu-id="c1d13-105">This topic summarizes the main ways in which MFTs differ from DMOs.</span></span> <span data-ttu-id="c1d13-106">如果您已經熟悉 SQL-DMO 介面，或者您想要將現有的 SQL-DMO 轉換成 MFT，請閱讀本主題。</span><span class="sxs-lookup"><span data-stu-id="c1d13-106">Read this topic if you are already familiar with the DMO interfaces, or if you want to convert an existing DMO into an MFT.</span></span>

<span data-ttu-id="c1d13-107">本主題包含下列幾節：</span><span class="sxs-lookup"><span data-stu-id="c1d13-107">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="c1d13-108">資料流程數目</span><span class="sxs-lookup"><span data-stu-id="c1d13-108">Number of Streams</span></span>](#number-of-streams)
-   [<span data-ttu-id="c1d13-109">格式協調</span><span class="sxs-lookup"><span data-stu-id="c1d13-109">Format Negotiation</span></span>](#format-negotiation)
-   [<span data-ttu-id="c1d13-110">串流</span><span class="sxs-lookup"><span data-stu-id="c1d13-110">Streaming</span></span>](#streaming)
    -   [<span data-ttu-id="c1d13-111">配置資源</span><span class="sxs-lookup"><span data-stu-id="c1d13-111">Allocating Resources</span></span>](#allocating-resources)
    -   [<span data-ttu-id="c1d13-112">處理資料</span><span class="sxs-lookup"><span data-stu-id="c1d13-112">Processing Data</span></span>](#processing-data)
    -   [<span data-ttu-id="c1d13-113">沖洗</span><span class="sxs-lookup"><span data-stu-id="c1d13-113">Flushing</span></span>](#flushing)
    -   [<span data-ttu-id="c1d13-114">資料流程不連續</span><span class="sxs-lookup"><span data-stu-id="c1d13-114">Stream Discontinuities</span></span>](#stream-discontinuities)
-   [<span data-ttu-id="c1d13-115">其他差異</span><span class="sxs-lookup"><span data-stu-id="c1d13-115">Miscellaneous Differences</span></span>](#miscellaneous-differences)
-   [<span data-ttu-id="c1d13-116">旗標</span><span class="sxs-lookup"><span data-stu-id="c1d13-116">Flags</span></span>](#flags)
    -   [<span data-ttu-id="c1d13-117">ProcessInput 旗標</span><span class="sxs-lookup"><span data-stu-id="c1d13-117">ProcessInput Flags</span></span>](#processinput-flags)
    -   [<span data-ttu-id="c1d13-118">ProcessOutput 旗標</span><span class="sxs-lookup"><span data-stu-id="c1d13-118">ProcessOutput Flags</span></span>](#processoutput-flags)
    -   [<span data-ttu-id="c1d13-119">GetInputStatus 旗標</span><span class="sxs-lookup"><span data-stu-id="c1d13-119">GetInputStatus Flags</span></span>](#getinputstatus-flags)
    -   [<span data-ttu-id="c1d13-120">GetOutputStatus 旗標</span><span class="sxs-lookup"><span data-stu-id="c1d13-120">GetOutputStatus Flags</span></span>](#getoutputstatus-flags)
    -   [<span data-ttu-id="c1d13-121">GetInputStreamInfo 旗標</span><span class="sxs-lookup"><span data-stu-id="c1d13-121">GetInputStreamInfo Flags</span></span>](#getinputstreaminfo-flags)
    -   [<span data-ttu-id="c1d13-122">GetOutputStreamInfo 旗標</span><span class="sxs-lookup"><span data-stu-id="c1d13-122">GetOutputStreamInfo Flags</span></span>](#getoutputstreaminfo-flags)
    -   [<span data-ttu-id="c1d13-123">SetInputType/SetOutputType 旗標</span><span class="sxs-lookup"><span data-stu-id="c1d13-123">SetInputType/SetOutputType Flags</span></span>](#setinputtypesetoutputtype-flags)
-   [<span data-ttu-id="c1d13-124">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="c1d13-124">Error Codes</span></span>](#error-codes)
-   [<span data-ttu-id="c1d13-125">建立混合式 SQL-DMO/MFT 物件</span><span class="sxs-lookup"><span data-stu-id="c1d13-125">Creating Hybrid DMO/MFT Objects</span></span>](#creating-hybrid-dmomft-objects)
-   [<span data-ttu-id="c1d13-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="c1d13-126">Related topics</span></span>](#related-topics)

## <a name="number-of-streams"></a><span data-ttu-id="c1d13-127">資料流程數目</span><span class="sxs-lookup"><span data-stu-id="c1d13-127">Number of Streams</span></span>

<span data-ttu-id="c1d13-128">A 的資料流程有固定的資料流程，而 MFT 可支援動態的資料流程數目。</span><span class="sxs-lookup"><span data-stu-id="c1d13-128">A DMO has a fixed number of streams, while an MFT can support a dynamic number of streams.</span></span> <span data-ttu-id="c1d13-129">用戶端可以新增輸入資料流程，而 MFT 可以在處理期間新增輸出資料流程。</span><span class="sxs-lookup"><span data-stu-id="c1d13-129">The client can add input streams, and the MFT can add new output streams during processing.</span></span> <span data-ttu-id="c1d13-130">但是，不需要 MFTs 就能支援動態資料流。</span><span class="sxs-lookup"><span data-stu-id="c1d13-130">MFTs are not required to support dynamic streams, however.</span></span> <span data-ttu-id="c1d13-131">一個 MFT 可以有固定數目的資料流程，就像說的一樣。</span><span class="sxs-lookup"><span data-stu-id="c1d13-131">An MFT can have a fixed number of streams, just like a DMO.</span></span>

<span data-ttu-id="c1d13-132">下列方法可用來在 MFT 上支援動態資料流：</span><span class="sxs-lookup"><span data-stu-id="c1d13-132">The following methods are used to support dynamic streams on an MFT:</span></span>

-   [<span data-ttu-id="c1d13-133">**IMFTransform::AddInputStreams**</span><span class="sxs-lookup"><span data-stu-id="c1d13-133">**IMFTransform::AddInputStreams**</span></span>](/windows/win32/api/mftransform/nf-mftransform-imftransform-addinputstreams)
-   [<span data-ttu-id="c1d13-134">**IMFTransform：:D eleteInputStream**</span><span class="sxs-lookup"><span data-stu-id="c1d13-134">**IMFTransform::DeleteInputStream**</span></span>](/windows/win32/api/mftransform/nf-mftransform-imftransform-deleteinputstream)
-   [<span data-ttu-id="c1d13-135">**IMFTransform::GetStreamIDs**</span><span class="sxs-lookup"><span data-stu-id="c1d13-135">**IMFTransform::GetStreamIDs**</span></span>](/windows/win32/api/mftransform/nf-mftransform-imftransform-getstreamids)
-   [<span data-ttu-id="c1d13-136">**IMFTransform::GetStreamLimits**</span><span class="sxs-lookup"><span data-stu-id="c1d13-136">**IMFTransform::GetStreamLimits**</span></span>](/windows/win32/api/mftransform/nf-mftransform-imftransform-getstreamlimits)

<span data-ttu-id="c1d13-137">此外， [**IMFTransform：:P rocessoutput**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processoutput) 方法會定義用於加入或移除輸出資料流程的行為。</span><span class="sxs-lookup"><span data-stu-id="c1d13-137">In addition, the [**IMFTransform::ProcessOutput**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processoutput) method defines the behavior for adding or removing output streams.</span></span>

<span data-ttu-id="c1d13-138">因為 DMOs 有固定的資料流程，所以會使用以零為基底的索引值來識別該的資料流程。</span><span class="sxs-lookup"><span data-stu-id="c1d13-138">Because DMOs have fixed streams, the streams on a DMO are identified using zero-based index values.</span></span> <span data-ttu-id="c1d13-139">相反地，MFTs 會使用不一定會對應到索引值的資料流程識別碼。</span><span class="sxs-lookup"><span data-stu-id="c1d13-139">MFTs, on the other hand, use stream identifiers that do not necessarily correspond to index values.</span></span> <span data-ttu-id="c1d13-140">這是因為 MFT 上的資料流程數目可能會變更。</span><span class="sxs-lookup"><span data-stu-id="c1d13-140">This is because the number of streams on an MFT might change.</span></span> <span data-ttu-id="c1d13-141">例如，可能會移除資料流程0，並將 stream 1 保留為第一個資料流程。</span><span class="sxs-lookup"><span data-stu-id="c1d13-141">For example, stream 0 might be removed, leaving stream 1 as the first stream.</span></span> <span data-ttu-id="c1d13-142">不過，具有固定資料流程的 MFT 應該會觀察與 DMOs 相同的慣例，並將索引值用於資料流程識別碼。</span><span class="sxs-lookup"><span data-stu-id="c1d13-142">However, an MFT with a fixed number of streams should observe the same convention as DMOs and use index values for stream identifiers.</span></span>

## <a name="format-negotiation"></a><span data-ttu-id="c1d13-143">格式協調</span><span class="sxs-lookup"><span data-stu-id="c1d13-143">Format Negotiation</span></span>

<span data-ttu-id="c1d13-144">MFTs 使用 [**IMFMediaType**](/windows/win32/api/mfobjects/nn-mfobjects-imfmediatype) 介面來描述媒體類型。</span><span class="sxs-lookup"><span data-stu-id="c1d13-144">MFTs use the [**IMFMediaType**](/windows/win32/api/mfobjects/nn-mfobjects-imfmediatype) interface to describe media types.</span></span> <span data-ttu-id="c1d13-145">否則，使用 MFTs 的格式協商可在與 DMOs 相同的基本原則上運作。</span><span class="sxs-lookup"><span data-stu-id="c1d13-145">Otherwise, format negotiation with MFTs works on the same basic principles as with DMOs.</span></span> <span data-ttu-id="c1d13-146">下表列出 DMOs 的格式協商方法，以及 MFTs 的對應方法。</span><span class="sxs-lookup"><span data-stu-id="c1d13-146">The following table lists the format negotiation methods for DMOs and the corresponding methods for MFTs.</span></span>



| <span data-ttu-id="c1d13-147">SQL-DMO 方法</span><span class="sxs-lookup"><span data-stu-id="c1d13-147">DMO method</span></span>                                                                        | <span data-ttu-id="c1d13-148">MFT 方法</span><span class="sxs-lookup"><span data-stu-id="c1d13-148">MFT method</span></span>                                                                          |
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="c1d13-149">**IMediaObject::GetInputCurrentType**</span><span class="sxs-lookup"><span data-stu-id="c1d13-149">**IMediaObject::GetInputCurrentType**</span></span>](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getinputcurrenttype)   | [<span data-ttu-id="c1d13-150">**IMFTransform::GetInputCurrentType**</span><span class="sxs-lookup"><span data-stu-id="c1d13-150">**IMFTransform::GetInputCurrentType**</span></span>](/windows/win32/api/mftransform/nf-mftransform-imftransform-getinputcurrenttype)       |
| [<span data-ttu-id="c1d13-151">**IMediaObject::GetInputMaxLatency**</span><span class="sxs-lookup"><span data-stu-id="c1d13-151">**IMediaObject::GetInputMaxLatency**</span></span>](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getinputmaxlatency)     | [<span data-ttu-id="c1d13-152">**IMFTransform::GetInputStreamInfo**</span><span class="sxs-lookup"><span data-stu-id="c1d13-152">**IMFTransform::GetInputStreamInfo**</span></span>](/windows/win32/api/mftransform/nf-mftransform-imftransform-getinputstreaminfo)         |
| [<span data-ttu-id="c1d13-153">**IMediaObject::GetInputSizeInfo**</span><span class="sxs-lookup"><span data-stu-id="c1d13-153">**IMediaObject::GetInputSizeInfo**</span></span>](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getinputsizeinfo)         | [<span data-ttu-id="c1d13-154">**IMFTransform::GetInputStreamInfo**</span><span class="sxs-lookup"><span data-stu-id="c1d13-154">**IMFTransform::GetInputStreamInfo**</span></span>](/windows/win32/api/mftransform/nf-mftransform-imftransform-getinputstreaminfo)         |
| [<span data-ttu-id="c1d13-155">**IMediaObject::GetInputType**</span><span class="sxs-lookup"><span data-stu-id="c1d13-155">**IMediaObject::GetInputType**</span></span>](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getinputtype)                 | [<span data-ttu-id="c1d13-156">**IMFTransform::GetInputAvailableType**</span><span class="sxs-lookup"><span data-stu-id="c1d13-156">**IMFTransform::GetInputAvailableType**</span></span>](/windows/win32/api/mftransform/nf-mftransform-imftransform-getinputavailabletype)   |
| [<span data-ttu-id="c1d13-157">**IMediaObject::GetOutputCurrentType**</span><span class="sxs-lookup"><span data-stu-id="c1d13-157">**IMediaObject::GetOutputCurrentType**</span></span>](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputcurrenttype) | [<span data-ttu-id="c1d13-158">**IMFTransform::GetOutputCurrentType**</span><span class="sxs-lookup"><span data-stu-id="c1d13-158">**IMFTransform::GetOutputCurrentType**</span></span>](/windows/win32/api/mftransform/nf-mftransform-imftransform-getoutputcurrenttype)     |
| [<span data-ttu-id="c1d13-159">**IMediaObject::GetOutputSizeInfo**</span><span class="sxs-lookup"><span data-stu-id="c1d13-159">**IMediaObject::GetOutputSizeInfo**</span></span>](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputsizeinfo)       | [<span data-ttu-id="c1d13-160">**IMFTransform::GetOutputStreamInfo**</span><span class="sxs-lookup"><span data-stu-id="c1d13-160">**IMFTransform::GetOutputStreamInfo**</span></span>](/windows/win32/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo)       |
| [<span data-ttu-id="c1d13-161">**IMediaObject::GetOutputType**</span><span class="sxs-lookup"><span data-stu-id="c1d13-161">**IMediaObject::GetOutputType**</span></span>](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputtype)               | [<span data-ttu-id="c1d13-162">**IMFTransform::GetOutputAvailableType**</span><span class="sxs-lookup"><span data-stu-id="c1d13-162">**IMFTransform::GetOutputAvailableType**</span></span>](/windows/win32/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) |



 

## <a name="streaming"></a><span data-ttu-id="c1d13-163">串流</span><span class="sxs-lookup"><span data-stu-id="c1d13-163">Streaming</span></span>

<span data-ttu-id="c1d13-164">如同 DMOs，MFTs 會透過呼叫 [**ProcessInput**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processinput) 和 [**ProcessOutput**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processoutput) 方法來處理資料。</span><span class="sxs-lookup"><span data-stu-id="c1d13-164">Like DMOs, MFTs process data through calls to [**ProcessInput**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processinput) and [**ProcessOutput**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processoutput) methods.</span></span> <span data-ttu-id="c1d13-165">以下是在串流處理資料時，SQL-DMO 和 MFT 程式之間的主要差異。</span><span class="sxs-lookup"><span data-stu-id="c1d13-165">Here are the major differences between DMO and MFT processes when streaming data.</span></span>

### <a name="allocating-resources"></a><span data-ttu-id="c1d13-166">配置資源</span><span class="sxs-lookup"><span data-stu-id="c1d13-166">Allocating Resources</span></span>

<span data-ttu-id="c1d13-167">MFTs 沒有與 FreeStreamingResources 搭配使用的 [**IMediaObject：： AllocateStreamingResources**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-allocatestreamingresources) 和 [**IMediaObject：： DMOs**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-freestreamingresources) 方法。</span><span class="sxs-lookup"><span data-stu-id="c1d13-167">MFTs do not have the [**IMediaObject::AllocateStreamingResources**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-allocatestreamingresources) and [**IMediaObject::FreeStreamingResources**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-freestreamingresources) methods used with DMOs.</span></span> <span data-ttu-id="c1d13-168">若要有效率地處理資源的配置和解除配置，MFT 可以在 [**IMFTransform：:P rocessmessage**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processmessage) 方法中回應下列訊息：</span><span class="sxs-lookup"><span data-stu-id="c1d13-168">To handle allocation and deallocation of resources efficiently, an MFT can respond to the following messages in the [**IMFTransform::ProcessMessage**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processmessage) method:</span></span>

-   [<span data-ttu-id="c1d13-169">**MFT \_ 訊息 \_ 通知 \_ 開始 \_ 串流**</span><span class="sxs-lookup"><span data-stu-id="c1d13-169">**MFT\_MESSAGE\_NOTIFY\_BEGIN\_STREAMING**</span></span>](mft-message-notify-begin-streaming.md)
-   [<span data-ttu-id="c1d13-170">**MFT \_ 訊息 \_ 通知 \_ 開始 \_ \_ 資料流程**</span><span class="sxs-lookup"><span data-stu-id="c1d13-170">**MFT\_MESSAGE\_NOTIFY\_START\_OF\_STREAM**</span></span>](mft-message-notify-start-of-stream.md)

<span data-ttu-id="c1d13-171">此外，用戶端可以藉由呼叫 [**ProcessMessage**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processmessage) 與下列訊息來發出資料流程的開始和結束信號：</span><span class="sxs-lookup"><span data-stu-id="c1d13-171">In addition, the client can signal the start and end of a stream by calling [**ProcessMessage**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processmessage) with the following messages:</span></span>

-   [<span data-ttu-id="c1d13-172">**MFT \_ 訊息 \_ 通知 \_ 結束 \_ \_ 資料流程**</span><span class="sxs-lookup"><span data-stu-id="c1d13-172">**MFT\_MESSAGE\_NOTIFY\_END\_OF\_STREAM**</span></span>](mft-message-notify-end-of-stream.md)
-   [<span data-ttu-id="c1d13-173">**MFT \_ 訊息 \_ 通知 \_ 結束 \_ 資料流程**</span><span class="sxs-lookup"><span data-stu-id="c1d13-173">**MFT\_MESSAGE\_NOTIFY\_END\_STREAMING**</span></span>](mft-message-notify-end-streaming.md)

<span data-ttu-id="c1d13-174">這兩個訊息沒有完全相同的專案。</span><span class="sxs-lookup"><span data-stu-id="c1d13-174">These two messages have no exact DMO equivalent.</span></span>

### <a name="processing-data"></a><span data-ttu-id="c1d13-175">處理資料</span><span class="sxs-lookup"><span data-stu-id="c1d13-175">Processing Data</span></span>

<span data-ttu-id="c1d13-176">MFTs 使用媒體範例來保存輸入和輸出資料。</span><span class="sxs-lookup"><span data-stu-id="c1d13-176">MFTs use media samples to hold input and output data.</span></span> <span data-ttu-id="c1d13-177">媒體範例會公開 [**IMFSample**](/windows/win32/api/mfobjects/nn-mfobjects-imfsample) 介面，並包含下列資料：</span><span class="sxs-lookup"><span data-stu-id="c1d13-177">Media samples expose the [**IMFSample**](/windows/win32/api/mfobjects/nn-mfobjects-imfsample) interface, and contain the following data:</span></span>

-   <span data-ttu-id="c1d13-178">時間戳記和持續時間。</span><span class="sxs-lookup"><span data-stu-id="c1d13-178">Time stamp and duration.</span></span>
-   <span data-ttu-id="c1d13-179">包含每個範例資訊的屬性。</span><span class="sxs-lookup"><span data-stu-id="c1d13-179">Attributes that contain per-sample information.</span></span> <span data-ttu-id="c1d13-180">如需屬性的清單，請參閱 [範例屬性](sample-attributes.md)。</span><span class="sxs-lookup"><span data-stu-id="c1d13-180">For a list of attributes, see [Sample Attributes](sample-attributes.md).</span></span>
-   <span data-ttu-id="c1d13-181">零或多個媒體緩衝區。</span><span class="sxs-lookup"><span data-stu-id="c1d13-181">Zero or more media buffers.</span></span> <span data-ttu-id="c1d13-182">每個媒體緩衝區都會公開 [**IMFMediaBuffer**](/windows/win32/api/mfobjects/nn-mfobjects-imfmediabuffer) 介面。</span><span class="sxs-lookup"><span data-stu-id="c1d13-182">Each media buffer exposes the [**IMFMediaBuffer**](/windows/win32/api/mfobjects/nn-mfobjects-imfmediabuffer) interface.</span></span>

<span data-ttu-id="c1d13-183">[**IMFMediaBuffer**](/windows/win32/api/mfobjects/nn-mfobjects-imfmediabuffer)介面類別似于 sql-dmo **IMediaBuffer** 介面。</span><span class="sxs-lookup"><span data-stu-id="c1d13-183">The [**IMFMediaBuffer**](/windows/win32/api/mfobjects/nn-mfobjects-imfmediabuffer) interface is similar to the DMO **IMediaBuffer** interface.</span></span> <span data-ttu-id="c1d13-184">若要存取基礎記憶體緩衝區，請呼叫 [**IMFMediaBuffer：： Lock**](/windows/win32/api/mfobjects/nf-mfobjects-imfmediabuffer-lock)。</span><span class="sxs-lookup"><span data-stu-id="c1d13-184">To access the underlying memory buffer, call [**IMFMediaBuffer::Lock**](/windows/win32/api/mfobjects/nf-mfobjects-imfmediabuffer-lock).</span></span> <span data-ttu-id="c1d13-185">這個方法大約相當於 DMOs 的 [**IMediaBuffer：： GetBufferAndLength**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediabuffer-getbufferandlength) 。</span><span class="sxs-lookup"><span data-stu-id="c1d13-185">This method is roughly equivalent to [**IMediaBuffer::GetBufferAndLength**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediabuffer-getbufferandlength) for DMOs.</span></span>

<span data-ttu-id="c1d13-186">若是未壓縮的影片資料，媒體緩衝區可能也支援 [**IMF2DBuffer**](/windows/win32/api/mfobjects/nn-mfobjects-imf2dbuffer) 介面。</span><span class="sxs-lookup"><span data-stu-id="c1d13-186">For uncompressed video data, a media buffer might also support the [**IMF2DBuffer**](/windows/win32/api/mfobjects/nn-mfobjects-imf2dbuffer) interface.</span></span> <span data-ttu-id="c1d13-187">處理未壓縮影片 (為輸入或輸出) 的 MFT 應該準備好在緩衝區公開時使用 **IMF2DBuffer** 介面。</span><span class="sxs-lookup"><span data-stu-id="c1d13-187">An MFT that processes uncompressed video (either as input or output) should be prepared to use the **IMF2DBuffer** interface if the buffer exposes it.</span></span> <span data-ttu-id="c1d13-188">如需詳細資訊，請參閱 [未壓縮的影片緩衝區](uncompressed-video-buffers.md)。</span><span class="sxs-lookup"><span data-stu-id="c1d13-188">For more information, see [Uncompressed Video Buffers](uncompressed-video-buffers.md).</span></span>

<span data-ttu-id="c1d13-189">媒體基礎提供一些 [**IMFMediaBuffer**](/windows/win32/api/mfobjects/nn-mfobjects-imfmediabuffer)的標準執行，因此通常不需要撰寫您自己的實作為。</span><span class="sxs-lookup"><span data-stu-id="c1d13-189">Media Foundation provides some standard implementations of [**IMFMediaBuffer**](/windows/win32/api/mfobjects/nn-mfobjects-imfmediabuffer), so it is generally not necessary to write your own implementation.</span></span> <span data-ttu-id="c1d13-190">若要從媒體基礎緩衝區建立 SQL-DMO 緩衝區，請呼叫 [**MFCreateLegacyMediaBufferOnMFMediaBuffer**](/windows/win32/api/mfapi/nf-mfapi-mfcreatelegacymediabufferonmfmediabuffer)。</span><span class="sxs-lookup"><span data-stu-id="c1d13-190">To create a DMO buffer from a Media Foundation buffer, call [**MFCreateLegacyMediaBufferOnMFMediaBuffer**](/windows/win32/api/mfapi/nf-mfapi-mfcreatelegacymediabufferonmfmediabuffer).</span></span>

### <a name="flushing"></a><span data-ttu-id="c1d13-191">沖洗</span><span class="sxs-lookup"><span data-stu-id="c1d13-191">Flushing</span></span>

<span data-ttu-id="c1d13-192">MFTs 沒有 [**Flush**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-flush) 方法。</span><span class="sxs-lookup"><span data-stu-id="c1d13-192">MFTs do not have a [**Flush**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-flush) method.</span></span> <span data-ttu-id="c1d13-193">若要排清 MFT，請使用 [**mft \_ 訊息 \_ 命令 \_ 清除**](mft-message-command-flush.md)訊息來呼叫 [**IMFTransform：:P rocessmessage**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processmessage) 。</span><span class="sxs-lookup"><span data-stu-id="c1d13-193">To flush an MFT, call [**IMFTransform::ProcessMessage**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processmessage) with the [**MFT\_MESSAGE\_COMMAND\_FLUSH**](mft-message-command-flush.md) message.</span></span>

### <a name="stream-discontinuities"></a><span data-ttu-id="c1d13-194">資料流程不連續</span><span class="sxs-lookup"><span data-stu-id="c1d13-194">Stream Discontinuities</span></span>

<span data-ttu-id="c1d13-195">MFTs 沒有不連續的 [**方法。**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-discontinuity)</span><span class="sxs-lookup"><span data-stu-id="c1d13-195">MFTs do not have a [**Discontinuity**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-discontinuity) method.</span></span> <span data-ttu-id="c1d13-196">若要以信號表示資料流程中的中斷，請在輸入範例上設定 MFSampleExtension 不中斷屬性。 [**\_**](mfsampleextension-discontinuity-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="c1d13-196">To signal a discontinuity in a stream, set the [**MFSampleExtension\_Discontinuity**](mfsampleextension-discontinuity-attribute.md) attribute on the input sample.</span></span>

## <a name="miscellaneous-differences"></a><span data-ttu-id="c1d13-197">其他差異</span><span class="sxs-lookup"><span data-stu-id="c1d13-197">Miscellaneous Differences</span></span>

<span data-ttu-id="c1d13-198">以下是 MFTs 和 DMOs 之間的一些額外微小差異。</span><span class="sxs-lookup"><span data-stu-id="c1d13-198">Here are some additional minor differences between MFTs and DMOs.</span></span>

-   <span data-ttu-id="c1d13-199">下列的 SQL-DMO 方法沒有適用于 MFT 的對應專案：</span><span class="sxs-lookup"><span data-stu-id="c1d13-199">There are no MFT equivalents for the following DMO methods:</span></span>
    -   [<span data-ttu-id="c1d13-200">**IMediaObject：： Lock**</span><span class="sxs-lookup"><span data-stu-id="c1d13-200">**IMediaObject::Lock**</span></span>](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-lock)
    -   [<span data-ttu-id="c1d13-201">**IMediaObject::SetInputMaxLatency**</span><span class="sxs-lookup"><span data-stu-id="c1d13-201">**IMediaObject::SetInputMaxLatency**</span></span>](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setinputmaxlatency)
-   <span data-ttu-id="c1d13-202">不需要 MFTs 就能支援匯總。</span><span class="sxs-lookup"><span data-stu-id="c1d13-202">MFTs are not required to support aggregation.</span></span>
-   <span data-ttu-id="c1d13-203">MFTs 支援稱為 *清空* 的作業。</span><span class="sxs-lookup"><span data-stu-id="c1d13-203">MFTs support an operation called *draining*.</span></span> <span data-ttu-id="c1d13-204">清空的目的是要處理保留在 MF 中的任何資料，而不提供任何更多輸入資料給 MFT (例如，在資料流程) 的結尾。</span><span class="sxs-lookup"><span data-stu-id="c1d13-204">The purpose of draining is to process any data that remains in the MF, without providing any more input data to the MFT (for example, at the end of the stream).</span></span> <span data-ttu-id="c1d13-205">若要清空 MFT，請使用 [**mft \_ 訊息 \_ 命令 \_ 清空**](mft-message-command-drain.md)訊息來呼叫 [**IMFTransform：:P rocessmessage**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processmessage) 。</span><span class="sxs-lookup"><span data-stu-id="c1d13-205">To drain an MFT, call [**IMFTransform::ProcessMessage**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processmessage) with the [**MFT\_MESSAGE\_COMMAND\_DRAIN**](mft-message-command-drain.md) message.</span></span> <span data-ttu-id="c1d13-206">如需詳細資訊，請參閱 [基本的 MFT 處理模型](basic-mft-processing-model.md)。</span><span class="sxs-lookup"><span data-stu-id="c1d13-206">For more information, see [Basic MFT Processing Model](basic-mft-processing-model.md).</span></span>
-   <span data-ttu-id="c1d13-207">MFTs 可以有屬性，包括每個資料流程屬性。</span><span class="sxs-lookup"><span data-stu-id="c1d13-207">MFTs can have attributes, including per-stream attributes.</span></span> <span data-ttu-id="c1d13-208">使用下列方法從 MFT 取得屬性：</span><span class="sxs-lookup"><span data-stu-id="c1d13-208">Use the following methods to get the attributes from an MFT:</span></span>

    -   [<span data-ttu-id="c1d13-209">**IMFTransform：： GetAttributes**</span><span class="sxs-lookup"><span data-stu-id="c1d13-209">**IMFTransform::GetAttributes**</span></span>](/windows/win32/api/mftransform/nf-mftransform-imftransform-getattributes)
    -   [<span data-ttu-id="c1d13-210">**IMFTransform::GetInputStreamAttributes**</span><span class="sxs-lookup"><span data-stu-id="c1d13-210">**IMFTransform::GetInputStreamAttributes**</span></span>](/windows/win32/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes)
    -   [<span data-ttu-id="c1d13-211">**IMFTransform::GetOutputStreamAttributes**</span><span class="sxs-lookup"><span data-stu-id="c1d13-211">**IMFTransform::GetOutputStreamAttributes**</span></span>](/windows/win32/api/mftransform/nf-mftransform-imftransform-getoutputstreamattributes)

-   <span data-ttu-id="c1d13-212">MFTs 可以處理事件。</span><span class="sxs-lookup"><span data-stu-id="c1d13-212">MFTs can process events.</span></span> <span data-ttu-id="c1d13-213">若要將事件傳送到 MFT，請呼叫 [**IMFTransform：:P rocessevent**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processevent)。</span><span class="sxs-lookup"><span data-stu-id="c1d13-213">To send an event to an MFT, call [**IMFTransform::ProcessEvent**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processevent).</span></span> <span data-ttu-id="c1d13-214">MFT 可透過 [**ProcessOutput**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processoutput) 方法，將事件傳送給用戶端。</span><span class="sxs-lookup"><span data-stu-id="c1d13-214">An MFT can send an event to the client through the [**ProcessOutput**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processoutput) method.</span></span> <span data-ttu-id="c1d13-215">如需詳細資訊，請參閱 [基本的 MFT 處理模型](basic-mft-processing-model.md)。</span><span class="sxs-lookup"><span data-stu-id="c1d13-215">For more information, see [Basic MFT Processing Model](basic-mft-processing-model.md).</span></span>

## <a name="flags"></a><span data-ttu-id="c1d13-216">Flags</span><span class="sxs-lookup"><span data-stu-id="c1d13-216">Flags</span></span>

<span data-ttu-id="c1d13-217">下表列出各種的 SQL-DMO 旗標及其對等專案。</span><span class="sxs-lookup"><span data-stu-id="c1d13-217">The following tables list the various DMO flags and their MFT equivalents.</span></span> <span data-ttu-id="c1d13-218">只要每個 a 的旗標直接對應到 MFT 旗標，這兩個旗標都有相同的數值。</span><span class="sxs-lookup"><span data-stu-id="c1d13-218">Whenever a DMO flag maps directly to an MFT flag, both flags have the same numeric value.</span></span> <span data-ttu-id="c1d13-219">不過，有些等旗標沒有完全相同的 MFT 對等專案，反之亦然。</span><span class="sxs-lookup"><span data-stu-id="c1d13-219">However, some DMO flags do not have exact MFT equivalents, and vice versa.</span></span>

### <a name="processinput-flags"></a><span data-ttu-id="c1d13-220">ProcessInput 旗標</span><span class="sxs-lookup"><span data-stu-id="c1d13-220">ProcessInput Flags</span></span>

<span data-ttu-id="c1d13-221">DMOs： [**\_ Sql-dmo \_ 輸入 \_ 資料 \_ 緩衝區 \_ 旗標**](/previous-versions/windows/embedded/aa451599(v=msdn.10))列舉。</span><span class="sxs-lookup"><span data-stu-id="c1d13-221">DMOs: [**\_DMO\_INPUT\_DATA\_BUFFER\_FLAGS**](/previous-versions/windows/embedded/aa451599(v=msdn.10)) enumeration.</span></span>

<span data-ttu-id="c1d13-222">MFTs：沒有對等的列舉。</span><span class="sxs-lookup"><span data-stu-id="c1d13-222">MFTs: No equivalent enumeration.</span></span>



| <span data-ttu-id="c1d13-223">SQL-DMO 旗標</span><span class="sxs-lookup"><span data-stu-id="c1d13-223">DMO flag</span></span>                                  | <span data-ttu-id="c1d13-224">MFT 旗標</span><span class="sxs-lookup"><span data-stu-id="c1d13-224">MFT flag</span></span>                                                                                                                                      |
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1d13-225">**SQL-DMO \_ 輸入 \_ 資料 \_ BUFFERF \_ SYNCPOINT**</span><span class="sxs-lookup"><span data-stu-id="c1d13-225">**DMO\_INPUT\_DATA\_BUFFERF\_SYNCPOINT**</span></span>  | <span data-ttu-id="c1d13-226">沒有對等的旗標。</span><span class="sxs-lookup"><span data-stu-id="c1d13-226">No equivalent flag.</span></span> <span data-ttu-id="c1d13-227">請改為在範例上設定 [**MFSampleExtension \_ CleanPoint**](mfsampleextension-cleanpoint-attribute.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="c1d13-227">Instead, set the [**MFSampleExtension\_CleanPoint**](mfsampleextension-cleanpoint-attribute.md) attribute on the sample.</span></span> |
| <span data-ttu-id="c1d13-228">**SQL-DMO \_ 輸入 \_ 資料 \_ BUFFERF \_ 時間**</span><span class="sxs-lookup"><span data-stu-id="c1d13-228">**DMO\_INPUT\_DATA\_BUFFERF\_TIME**</span></span>       | <span data-ttu-id="c1d13-229">沒有對等的旗標。</span><span class="sxs-lookup"><span data-stu-id="c1d13-229">No equivalent flag.</span></span> <span data-ttu-id="c1d13-230">請改為在範例上呼叫 [**IMFSample：： SetSampleTime**](/windows/win32/api/mfobjects/nf-mfobjects-imfsample-setsampletime) 。</span><span class="sxs-lookup"><span data-stu-id="c1d13-230">Instead, call [**IMFSample::SetSampleTime**](/windows/win32/api/mfobjects/nf-mfobjects-imfsample-setsampletime) on the sample.</span></span>                                  |
| <span data-ttu-id="c1d13-231">**SQL-DMO \_ 輸入 \_ 資料 \_ BUFFERF \_ TIMELENGTH**</span><span class="sxs-lookup"><span data-stu-id="c1d13-231">**DMO\_INPUT\_DATA\_BUFFERF\_TIMELENGTH**</span></span> | <span data-ttu-id="c1d13-232">沒有對等的旗標。</span><span class="sxs-lookup"><span data-stu-id="c1d13-232">No equivalent flag.</span></span> <span data-ttu-id="c1d13-233">請改為在範例上呼叫 [**IMFSample：： SetSampleDuration**](/windows/win32/api/mfobjects/nf-mfobjects-imfsample-setsampleduration) 。</span><span class="sxs-lookup"><span data-stu-id="c1d13-233">Instead, call [**IMFSample::SetSampleDuration**](/windows/win32/api/mfobjects/nf-mfobjects-imfsample-setsampleduration) on the sample.</span></span>                          |



 

### <a name="processoutput-flags"></a><span data-ttu-id="c1d13-234">ProcessOutput 旗標</span><span class="sxs-lookup"><span data-stu-id="c1d13-234">ProcessOutput Flags</span></span>

<span data-ttu-id="c1d13-235">DMOs： [**\_ Sql-dmo \_ 進程 \_ 輸出 \_ 旗標**](/previous-versions/windows/desktop/api/Mediaobj/ne-mediaobj-_dmo_process_output_flags)列舉。</span><span class="sxs-lookup"><span data-stu-id="c1d13-235">DMOs: [**\_DMO\_PROCESS\_OUTPUT\_FLAGS**](/previous-versions/windows/desktop/api/Mediaobj/ne-mediaobj-_dmo_process_output_flags) enumeration.</span></span>

<span data-ttu-id="c1d13-236">MFTs： [**\_ MFT \_ 進程 \_ 輸出 \_ 旗標**](/windows/win32/api/mftransform/ne-mftransform-_mft_process_output_flags)列舉。</span><span class="sxs-lookup"><span data-stu-id="c1d13-236">MFTs: [**\_MFT\_PROCESS\_OUTPUT\_FLAGS**](/windows/win32/api/mftransform/ne-mftransform-_mft_process_output_flags) enumeration.</span></span>



| <span data-ttu-id="c1d13-237">SQL-DMO 旗標</span><span class="sxs-lookup"><span data-stu-id="c1d13-237">DMO flag</span></span>                                            | <span data-ttu-id="c1d13-238">MFT 旗標</span><span class="sxs-lookup"><span data-stu-id="c1d13-238">MFT flag</span></span>                                            |
|-----------------------------------------------------|-----------------------------------------------------|
| <span data-ttu-id="c1d13-239">**\_ \_ \_ \_ 當 \_ 沒有 \_ 緩衝區時，會捨棄進程輸出**</span><span class="sxs-lookup"><span data-stu-id="c1d13-239">**DMO\_PROCESS\_OUTPUT\_DISCARD\_WHEN\_NO\_BUFFER**</span></span> | <span data-ttu-id="c1d13-240">**\_ \_ \_ \_ 當 \_ 沒有 \_ 緩衝區時，MFT 進程輸出捨棄**</span><span class="sxs-lookup"><span data-stu-id="c1d13-240">**MFT\_PROCESS\_OUTPUT\_DISCARD\_WHEN\_NO\_BUFFER**</span></span> |



 

<span data-ttu-id="c1d13-241">DMOs： [**\_ Sql-dmo \_ 輸出 \_ 資料 \_ 緩衝區 \_ 旗標**](/previous-versions/windows/desktop/api/Mediaobj/ne-mediaobj-_dmo_output_data_buffer_flags)列舉。</span><span class="sxs-lookup"><span data-stu-id="c1d13-241">DMOs: [**\_DMO\_OUTPUT\_DATA\_BUFFER\_FLAGS**](/previous-versions/windows/desktop/api/Mediaobj/ne-mediaobj-_dmo_output_data_buffer_flags) enumeration.</span></span>


<span data-ttu-id="c1d13-242">MFTs： [**\_ MFT \_ 輸出 \_ 資料 \_ 緩衝區 \_ 旗標**](/windows/win32/api/mftransform/ne-mftransform-_mft_output_data_buffer_flags)列舉。</span><span class="sxs-lookup"><span data-stu-id="c1d13-242">MFTs: [**\_MFT\_OUTPUT\_DATA\_BUFFER\_FLAGS**](/windows/win32/api/mftransform/ne-mftransform-_mft_output_data_buffer_flags) enumeration.</span></span>



| <span data-ttu-id="c1d13-243">SQL-DMO 旗標</span><span class="sxs-lookup"><span data-stu-id="c1d13-243">DMO flag</span></span>                                   | <span data-ttu-id="c1d13-244">MFT 旗標</span><span class="sxs-lookup"><span data-stu-id="c1d13-244">MFT flag</span></span>                                                                                                                                            |
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1d13-245">**SQL-DMO \_ 輸出 \_ 資料 \_ BUFFERF \_ SYNCPOINT**</span><span class="sxs-lookup"><span data-stu-id="c1d13-245">**DMO\_OUTPUT\_DATA\_BUFFERF\_SYNCPOINT**</span></span>  | <span data-ttu-id="c1d13-246">沒有對等的旗標。</span><span class="sxs-lookup"><span data-stu-id="c1d13-246">No equivalent flag.</span></span> <span data-ttu-id="c1d13-247">請改為檢查範例上的 [**MFSampleExtension \_ CleanPoint**](mfsampleextension-cleanpoint-attribute.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="c1d13-247">Instead, check for the [**MFSampleExtension\_CleanPoint**](mfsampleextension-cleanpoint-attribute.md) attribute on the sample.</span></span> |
| <span data-ttu-id="c1d13-248">**SQL-DMO \_ 輸出 \_ 資料 \_ BUFFERF \_ 時間**</span><span class="sxs-lookup"><span data-stu-id="c1d13-248">**DMO\_OUTPUT\_DATA\_BUFFERF\_TIME**</span></span>       | <span data-ttu-id="c1d13-249">沒有對等的旗標。</span><span class="sxs-lookup"><span data-stu-id="c1d13-249">No equivalent flag.</span></span> <span data-ttu-id="c1d13-250">請改為在範例上呼叫 [**IMFSample：： GetSampleTime**](/windows/win32/api/mfobjects/nf-mfobjects-imfsample-getsampletime) 。</span><span class="sxs-lookup"><span data-stu-id="c1d13-250">Instead, call [**IMFSample::GetSampleTime**](/windows/win32/api/mfobjects/nf-mfobjects-imfsample-getsampletime) on the sample.</span></span>                                        |
| <span data-ttu-id="c1d13-251">**SQL-DMO \_ 輸出 \_ 資料 \_ BUFFERF \_ TIMELENGTH**</span><span class="sxs-lookup"><span data-stu-id="c1d13-251">**DMO\_OUTPUT\_DATA\_BUFFERF\_TIMELENGTH**</span></span> | <span data-ttu-id="c1d13-252">沒有對等的旗標。</span><span class="sxs-lookup"><span data-stu-id="c1d13-252">No equivalent flag.</span></span> <span data-ttu-id="c1d13-253">請改為在範例上呼叫 [**IMFSample：： GetSampleDuration**](/windows/win32/api/mfobjects/nf-mfobjects-imfsample-getsampleduration) 。</span><span class="sxs-lookup"><span data-stu-id="c1d13-253">Instead, call [**IMFSample::GetSampleDuration**](/windows/win32/api/mfobjects/nf-mfobjects-imfsample-getsampleduration) on the sample.</span></span>                                |
| <span data-ttu-id="c1d13-254">**SQL-DMO \_ 輸出 \_ 資料 \_ BUFFERF \_ 未完成**</span><span class="sxs-lookup"><span data-stu-id="c1d13-254">**DMO\_OUTPUT\_DATA\_BUFFERF\_INCOMPLETE**</span></span> | <span data-ttu-id="c1d13-255">**MFT \_ 輸出 \_ 資料 \_ 緩衝區 \_ 未完成**</span><span class="sxs-lookup"><span data-stu-id="c1d13-255">**MFT\_OUTPUT\_DATA\_BUFFER\_INCOMPLETE**</span></span>                                                                                                           |
| <span data-ttu-id="c1d13-256">沒有對等的旗標。</span><span class="sxs-lookup"><span data-stu-id="c1d13-256">No equivalent flag.</span></span>                        | <span data-ttu-id="c1d13-257">**MFT \_ 輸出 \_ 資料 \_ 緩衝區 \_ 格式 \_ 變更**</span><span class="sxs-lookup"><span data-stu-id="c1d13-257">**MFT\_OUTPUT\_DATA\_BUFFER\_FORMAT\_CHANGE**</span></span>                                                                                                       |
| <span data-ttu-id="c1d13-258">沒有對等的旗標。</span><span class="sxs-lookup"><span data-stu-id="c1d13-258">No equivalent flag.</span></span>                        | <span data-ttu-id="c1d13-259">**MFT \_ 輸出 \_ 資料 \_ 緩衝區 \_ 資料流程 \_ 結束**</span><span class="sxs-lookup"><span data-stu-id="c1d13-259">**MFT\_OUTPUT\_DATA\_BUFFER\_STREAM\_END**</span></span>                                                                                                          |
| <span data-ttu-id="c1d13-260">沒有對等的旗標。</span><span class="sxs-lookup"><span data-stu-id="c1d13-260">No equivalent flag.</span></span>                        | <span data-ttu-id="c1d13-261">**MFT \_ 輸出 \_ 資料 \_ 緩衝區 \_ 無 \_ 範例**</span><span class="sxs-lookup"><span data-stu-id="c1d13-261">**MFT\_OUTPUT\_DATA\_BUFFER\_NO\_SAMPLE**</span></span>                                                                                                           |



 

### <a name="getinputstatus-flags"></a><span data-ttu-id="c1d13-262">GetInputStatus 旗標</span><span class="sxs-lookup"><span data-stu-id="c1d13-262">GetInputStatus Flags</span></span>

<span data-ttu-id="c1d13-263">DMOs： **\_ Sql-dmo \_ 輸入 \_ 狀態 \_ 旗標** 列舉。</span><span class="sxs-lookup"><span data-stu-id="c1d13-263">DMOs: **\_DMO\_INPUT\_STATUS\_FLAGS** enumeration.</span></span>

<span data-ttu-id="c1d13-264">MFTs： [**\_ MFT \_ 輸入 \_ 狀態 \_ 旗標**](/windows/win32/api/mftransform/ne-mftransform-_mft_input_status_flags)列舉。</span><span class="sxs-lookup"><span data-stu-id="c1d13-264">MFTs: [**\_MFT\_INPUT\_STATUS\_FLAGS**](/windows/win32/api/mftransform/ne-mftransform-_mft_input_status_flags) enumeration.</span></span>



| <span data-ttu-id="c1d13-265">SQL-DMO 旗標</span><span class="sxs-lookup"><span data-stu-id="c1d13-265">DMO flag</span></span>                              | <span data-ttu-id="c1d13-266">MFT 旗標</span><span class="sxs-lookup"><span data-stu-id="c1d13-266">MFT flag</span></span>                             |
|---------------------------------------|--------------------------------------|
| <span data-ttu-id="c1d13-267">**SQL-DMO \_ 輸入 \_ STATUSF \_ 接受 \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="c1d13-267">**DMO\_INPUT\_STATUSF\_ACCEPT\_DATA**</span></span> | <span data-ttu-id="c1d13-268">**MFT \_ 輸入 \_ 狀態 \_ 接受 \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="c1d13-268">**MFT\_INPUT\_STATUS\_ACCEPT\_DATA**</span></span> |



 

### <a name="getoutputstatus-flags"></a><span data-ttu-id="c1d13-269">GetOutputStatus 旗標</span><span class="sxs-lookup"><span data-stu-id="c1d13-269">GetOutputStatus Flags</span></span>

<span data-ttu-id="c1d13-270">DMOs：沒有對等的列舉。</span><span class="sxs-lookup"><span data-stu-id="c1d13-270">DMOs: No equivalent enumeration.</span></span>

<span data-ttu-id="c1d13-271">MFTs： [**\_ MFT \_ 輸出 \_ 狀態 \_ 旗標**](/windows/win32/api/mftransform/ne-mftransform-_mft_output_status_flags)列舉。</span><span class="sxs-lookup"><span data-stu-id="c1d13-271">MFTs: [**\_MFT\_OUTPUT\_STATUS\_FLAGS**](/windows/win32/api/mftransform/ne-mftransform-_mft_output_status_flags) enumeration.</span></span>



| <span data-ttu-id="c1d13-272">SQL-DMO 旗標</span><span class="sxs-lookup"><span data-stu-id="c1d13-272">DMO flag</span></span>            | <span data-ttu-id="c1d13-273">MFT 旗標</span><span class="sxs-lookup"><span data-stu-id="c1d13-273">MFT flag</span></span>                               |
|---------------------|----------------------------------------|
| <span data-ttu-id="c1d13-274">沒有對等的旗標。</span><span class="sxs-lookup"><span data-stu-id="c1d13-274">No equivalent flag.</span></span> | <span data-ttu-id="c1d13-275">**可用的 MFT \_ 輸出 \_ 狀態 \_ 範例 \_**</span><span class="sxs-lookup"><span data-stu-id="c1d13-275">**MFT\_OUTPUT\_STATUS\_SAMPLE\_READY**</span></span> |



 

### <a name="getinputstreaminfo-flags"></a><span data-ttu-id="c1d13-276">GetInputStreamInfo 旗標</span><span class="sxs-lookup"><span data-stu-id="c1d13-276">GetInputStreamInfo Flags</span></span>

<span data-ttu-id="c1d13-277">DMOs： [**\_ Sql-dmo \_ 輸入 \_ 資料流程 \_ 資訊 \_ 旗標**](/previous-versions/windows/embedded/aa451600(v=msdn.10))列舉。</span><span class="sxs-lookup"><span data-stu-id="c1d13-277">DMOs: [**\_DMO\_INPUT\_STREAM\_INFO\_FLAGS**](/previous-versions/windows/embedded/aa451600(v=msdn.10)) enumeration.</span></span>

<span data-ttu-id="c1d13-278">MFTs： [**\_ MFT \_ 輸入 \_ 資料流程 \_ 資訊 \_ 旗標**](/windows/win32/api/mftransform/ne-mftransform-_mft_input_stream_info_flags)列舉。</span><span class="sxs-lookup"><span data-stu-id="c1d13-278">MFTs: [**\_MFT\_INPUT\_STREAM\_INFO\_FLAGS**](/windows/win32/api/mftransform/ne-mftransform-_mft_input_stream_info_flags) enumeration.</span></span>



| <span data-ttu-id="c1d13-279">SQL-DMO 旗標</span><span class="sxs-lookup"><span data-stu-id="c1d13-279">DMO flag</span></span>                                             | <span data-ttu-id="c1d13-280">MFT 旗標</span><span class="sxs-lookup"><span data-stu-id="c1d13-280">MFT flag</span></span>                                            |
|------------------------------------------------------|-----------------------------------------------------|
| <span data-ttu-id="c1d13-281">**SQL-DMO \_ 輸入 \_ STREAMF \_ 完整 \_ 範例**</span><span class="sxs-lookup"><span data-stu-id="c1d13-281">**DMO\_INPUT\_STREAMF\_WHOLE\_SAMPLES**</span></span>              | <span data-ttu-id="c1d13-282">**MFT \_ 輸入 \_ 資料流程的 \_ 完整 \_ 範例**</span><span class="sxs-lookup"><span data-stu-id="c1d13-282">**MFT\_INPUT\_STREAM\_WHOLE\_SAMPLES**</span></span>              |
| <span data-ttu-id="c1d13-283">**SQL-DMO \_ 輸入 \_ STREAMF \_ \_ \_ 每個緩衝區一個樣本 \_**</span><span class="sxs-lookup"><span data-stu-id="c1d13-283">**DMO\_INPUT\_STREAMF\_SINGLE\_SAMPLE\_PER\_BUFFER**</span></span> | <span data-ttu-id="c1d13-284">**\_ \_ \_ \_ \_ 每個 \_ 緩衝區的 MFT 輸入資料流程單一範例**</span><span class="sxs-lookup"><span data-stu-id="c1d13-284">**MFT\_INPUT\_STREAM\_SINGLE\_SAMPLE\_PER\_BUFFER**</span></span> |
| <span data-ttu-id="c1d13-285">**SQL-DMO \_ 輸入 \_ STREAMF \_ 固定 \_ 樣本 \_ 大小**</span><span class="sxs-lookup"><span data-stu-id="c1d13-285">**DMO\_INPUT\_STREAMF\_FIXED\_SAMPLE\_SIZE**</span></span>         | <span data-ttu-id="c1d13-286">**MFT \_ 輸入 \_ 資料流程 \_ 固定 \_ 樣本 \_ 大小**</span><span class="sxs-lookup"><span data-stu-id="c1d13-286">**MFT\_INPUT\_STREAM\_FIXED\_SAMPLE\_SIZE**</span></span>         |
| <span data-ttu-id="c1d13-287">**SQL-DMO \_ 輸入 \_ STREAMF \_ 保留 \_ 緩衝區**</span><span class="sxs-lookup"><span data-stu-id="c1d13-287">**DMO\_INPUT\_STREAMF\_HOLDS\_BUFFERS**</span></span>              | <span data-ttu-id="c1d13-288">**MFT \_ 輸入 \_ 資料流程 \_ 持有 \_ 緩衝區**</span><span class="sxs-lookup"><span data-stu-id="c1d13-288">**MFT\_INPUT\_STREAM\_HOLDS\_BUFFERS**</span></span>              |
| <span data-ttu-id="c1d13-289">沒有對等的旗標。</span><span class="sxs-lookup"><span data-stu-id="c1d13-289">No equivalent flag.</span></span>                                  | <span data-ttu-id="c1d13-290">**MFT \_ 輸入 \_ 資料流程 \_ \_ 未 \_ ADDREF**</span><span class="sxs-lookup"><span data-stu-id="c1d13-290">**MFT\_INPUT\_STREAM\_DOES\_NOT\_ADDREF**</span></span>           |
| <span data-ttu-id="c1d13-291">沒有對等的旗標。</span><span class="sxs-lookup"><span data-stu-id="c1d13-291">No equivalent flag.</span></span>                                  | <span data-ttu-id="c1d13-292">**MFT \_ 輸入 \_ 資料流程 \_ 移除**</span><span class="sxs-lookup"><span data-stu-id="c1d13-292">**MFT\_INPUT\_STREAM\_REMOVABLE**</span></span>                   |
| <span data-ttu-id="c1d13-293">沒有對等的旗標。</span><span class="sxs-lookup"><span data-stu-id="c1d13-293">No equivalent flag.</span></span>                                  | <span data-ttu-id="c1d13-294">**選擇的 MFT \_ 輸入 \_ 資料流程 \_**</span><span class="sxs-lookup"><span data-stu-id="c1d13-294">**MFT\_INPUT\_STREAM\_OPTIONAL**</span></span>                    |



 

### <a name="getoutputstreaminfo-flags"></a><span data-ttu-id="c1d13-295">GetOutputStreamInfo 旗標</span><span class="sxs-lookup"><span data-stu-id="c1d13-295">GetOutputStreamInfo Flags</span></span>

<span data-ttu-id="c1d13-296">DMOs： [**\_ Sql-dmo \_ 輸出 \_ 資料流程 \_ 資訊 \_ 旗標**](/previous-versions/ms806053(v=msdn.10))列舉。</span><span class="sxs-lookup"><span data-stu-id="c1d13-296">DMOs: [**\_DMO\_OUTPUT\_STREAM\_INFO\_FLAGS**](/previous-versions/ms806053(v=msdn.10)) enumeration.</span></span>

<span data-ttu-id="c1d13-297">MFTs： [**\_ MFT \_ 輸出 \_ 資料流程 \_ 資訊 \_ 旗標**](/windows/win32/api/mftransform/ne-mftransform-_mft_output_stream_info_flags)列舉。</span><span class="sxs-lookup"><span data-stu-id="c1d13-297">MFTs: [**\_MFT\_OUTPUT\_STREAM\_INFO\_FLAGS**](/windows/win32/api/mftransform/ne-mftransform-_mft_output_stream_info_flags) enumeration.</span></span>



| <span data-ttu-id="c1d13-298">SQL-DMO 旗標</span><span class="sxs-lookup"><span data-stu-id="c1d13-298">DMO flag</span></span>                                              | <span data-ttu-id="c1d13-299">MFT 旗標</span><span class="sxs-lookup"><span data-stu-id="c1d13-299">MFT flag</span></span>                                             |
|-------------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c1d13-300">**SQL-DMO \_ 輸出 \_ STREAMF \_ 完整 \_ 範例**</span><span class="sxs-lookup"><span data-stu-id="c1d13-300">**DMO\_OUTPUT\_STREAMF\_WHOLE\_SAMPLES**</span></span>              | <span data-ttu-id="c1d13-301">**MFT \_ 輸出 \_ 資料流程的 \_ 完整 \_ 範例**</span><span class="sxs-lookup"><span data-stu-id="c1d13-301">**MFT\_OUTPUT\_STREAM\_WHOLE\_SAMPLES**</span></span>              |
| <span data-ttu-id="c1d13-302">**SQL-DMO \_ 輸出 \_ STREAMF \_ \_ \_ 每個 \_ 緩衝區的單一樣本**</span><span class="sxs-lookup"><span data-stu-id="c1d13-302">**DMO\_OUTPUT\_STREAMF\_SINGLE\_SAMPLE\_PER\_BUFFER**</span></span> | <span data-ttu-id="c1d13-303">**\_ \_ \_ \_ \_ 每個 \_ 緩衝區的 MFT 輸出資料流程單一範例**</span><span class="sxs-lookup"><span data-stu-id="c1d13-303">**MFT\_OUTPUT\_STREAM\_SINGLE\_SAMPLE\_PER\_BUFFER**</span></span> |
| <span data-ttu-id="c1d13-304">**SQL-DMO \_ 輸出 \_ STREAMF \_ 固定 \_ 樣本 \_ 大小**</span><span class="sxs-lookup"><span data-stu-id="c1d13-304">**DMO\_OUTPUT\_STREAMF\_FIXED\_SAMPLE\_SIZE**</span></span>         | <span data-ttu-id="c1d13-305">**MFT \_ 輸出 \_ 資料流程 \_ 固定 \_ 樣本 \_ 大小**</span><span class="sxs-lookup"><span data-stu-id="c1d13-305">**MFT\_OUTPUT\_STREAM\_FIXED\_SAMPLE\_SIZE**</span></span>         |
| <span data-ttu-id="c1d13-306">**SQL-DMO \_ 輸出 \_ STREAMF \_ DISCARDABLE**</span><span class="sxs-lookup"><span data-stu-id="c1d13-306">**DMO\_OUTPUT\_STREAMF\_DISCARDABLE**</span></span>                 | <span data-ttu-id="c1d13-307">**MFT \_ 輸出 \_ 資料流程 \_ DISCARDABLE**</span><span class="sxs-lookup"><span data-stu-id="c1d13-307">**MFT\_OUTPUT\_STREAM\_DISCARDABLE**</span></span>                 |
| <span data-ttu-id="c1d13-308">**SQL-DMO \_ 輸出 \_ STREAMF \_ 選擇性**</span><span class="sxs-lookup"><span data-stu-id="c1d13-308">**DMO\_OUTPUT\_STREAMF\_OPTIONAL**</span></span>                    | <span data-ttu-id="c1d13-309">**MFT \_ 輸出 \_ 資料流程 \_ 選擇性**</span><span class="sxs-lookup"><span data-stu-id="c1d13-309">**MFT\_OUTPUT\_STREAM\_OPTIONAL**</span></span>                    |
| <span data-ttu-id="c1d13-310">沒有對等的旗標。</span><span class="sxs-lookup"><span data-stu-id="c1d13-310">No equivalent flag.</span></span>                                   | <span data-ttu-id="c1d13-311">**MFT \_ 輸出 \_ 資料流程 \_ 提供 \_ 範例**</span><span class="sxs-lookup"><span data-stu-id="c1d13-311">**MFT\_OUTPUT\_STREAM\_PROVIDES\_SAMPLES**</span></span>           |
| <span data-ttu-id="c1d13-312">沒有對等的旗標。</span><span class="sxs-lookup"><span data-stu-id="c1d13-312">No equivalent flag.</span></span>                                   | <span data-ttu-id="c1d13-313">**MFT \_ 輸出 \_ 資料流程 \_ 可以 \_ 提供 \_ 範例**</span><span class="sxs-lookup"><span data-stu-id="c1d13-313">**MFT\_OUTPUT\_STREAM\_CAN\_PROVIDE\_SAMPLES**</span></span>       |
| <span data-ttu-id="c1d13-314">沒有對等的旗標。</span><span class="sxs-lookup"><span data-stu-id="c1d13-314">No equivalent flag.</span></span>                                   | <span data-ttu-id="c1d13-315">**MFT \_ 輸出 \_ 資料流程 \_ 延遲 \_ 讀取**</span><span class="sxs-lookup"><span data-stu-id="c1d13-315">**MFT\_OUTPUT\_STREAM\_LAZY\_READ**</span></span>                  |
| <span data-ttu-id="c1d13-316">沒有對等的旗標。</span><span class="sxs-lookup"><span data-stu-id="c1d13-316">No equivalent flag.</span></span>                                   | <span data-ttu-id="c1d13-317">**MFT \_ 輸出 \_ 資料流程 \_ 移除**</span><span class="sxs-lookup"><span data-stu-id="c1d13-317">**MFT\_OUTPUT\_STREAM\_REMOVABLE**</span></span>                   |



 

### <a name="setinputtypesetoutputtype-flags"></a><span data-ttu-id="c1d13-318">SetInputType/SetOutputType 旗標</span><span class="sxs-lookup"><span data-stu-id="c1d13-318">SetInputType/SetOutputType Flags</span></span>

<span data-ttu-id="c1d13-319">DMOs： [**\_ Sql-dmo \_ 集合 \_ 類型 \_ 旗標**](/previous-versions/windows/desktop/api/Mediaobj/ne-mediaobj-_dmo_set_type_flags)列舉。</span><span class="sxs-lookup"><span data-stu-id="c1d13-319">DMOs: [**\_DMO\_SET\_TYPE\_FLAGS**](/previous-versions/windows/desktop/api/Mediaobj/ne-mediaobj-_dmo_set_type_flags) enumeration.</span></span>

<span data-ttu-id="c1d13-320">MFTs： [**\_ MFT \_ 集合 \_ 類型 \_ 旗標**](/windows/win32/api/mftransform/ne-mftransform-_mft_set_type_flags)列舉。</span><span class="sxs-lookup"><span data-stu-id="c1d13-320">MFTs: [**\_MFT\_SET\_TYPE\_FLAGS**](/windows/win32/api/mftransform/ne-mftransform-_mft_set_type_flags) enumeration.</span></span>



| <span data-ttu-id="c1d13-321">SQL-DMO 旗標</span><span class="sxs-lookup"><span data-stu-id="c1d13-321">DMO flag</span></span>                        | <span data-ttu-id="c1d13-322">MFT 旗標</span><span class="sxs-lookup"><span data-stu-id="c1d13-322">MFT flag</span></span>                                                                             |
|---------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c1d13-323">**SQL-DMO \_ SET \_ TYPEF \_ TEST \_**</span><span class="sxs-lookup"><span data-stu-id="c1d13-323">**DMO\_SET\_TYPEF\_TEST\_ONLY**</span></span> | <span data-ttu-id="c1d13-324">**\_ \_ \_ 僅限設定類型測試 \_ 的 MFT**</span><span class="sxs-lookup"><span data-stu-id="c1d13-324">**MFT\_SET\_TYPE\_TEST\_ONLY**</span></span>                                                       |
| <span data-ttu-id="c1d13-325">**SQL-DMO \_ 設定 \_ TYPEF \_ CLEAR**</span><span class="sxs-lookup"><span data-stu-id="c1d13-325">**DMO\_SET\_TYPEF\_CLEAR**</span></span>      | <span data-ttu-id="c1d13-326">沒有對等的旗標。</span><span class="sxs-lookup"><span data-stu-id="c1d13-326">No equivalent flag.</span></span> <span data-ttu-id="c1d13-327">相反地，請將媒體類型設為 **Null** 以清除媒體類型。</span><span class="sxs-lookup"><span data-stu-id="c1d13-327">Instead, set the media type to **NULL** to clear the media type.</span></span> |



 

## <a name="error-codes"></a><span data-ttu-id="c1d13-328">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="c1d13-328">Error Codes</span></span>

<span data-ttu-id="c1d13-329">下表說明如何將 SQL-DMO 錯誤碼對應至 MFT 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="c1d13-329">The following table shows how to map DMO error codes to MFT error codes.</span></span> <span data-ttu-id="c1d13-330">混合式 MFT/SQL-DMO 物件應從 [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) 方法和來自 [**IMFTRANSFORM**](/windows/win32/api/mftransform/nn-mftransform-imftransform) 方法的 MFT 錯誤碼傳回 sql-dmo 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="c1d13-330">A hybrid MFT/DMO object should return the DMO error codes from [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) methods and the MFT error codes from [**IMFTransform**](/windows/win32/api/mftransform/nn-mftransform-imftransform) methods.</span></span> <span data-ttu-id="c1d13-331">在標頭檔 MediaErr 中定義了 SQL-DMO 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="c1d13-331">The DMO error codes are defined in the header file MediaErr.h.</span></span> <span data-ttu-id="c1d13-332">在標頭檔 mferror 中定義了 MFT 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="c1d13-332">The MFT error codes are defined in the header file mferror.h.</span></span>



| <span data-ttu-id="c1d13-333">SQL-DMO 錯誤碼</span><span class="sxs-lookup"><span data-stu-id="c1d13-333">DMO error code</span></span>                  | <span data-ttu-id="c1d13-334">MFT 錯誤碼</span><span class="sxs-lookup"><span data-stu-id="c1d13-334">MFT error code</span></span>                       |
|---------------------------------|--------------------------------------|
| <span data-ttu-id="c1d13-335">**SQL-DMO \_ E \_ INVALIDTYPE**</span><span class="sxs-lookup"><span data-stu-id="c1d13-335">**DMO\_E\_INVALIDTYPE**</span></span>         | <span data-ttu-id="c1d13-336">**MF \_ E \_ INVALIDTYPE**</span><span class="sxs-lookup"><span data-stu-id="c1d13-336">**MF\_E\_INVALIDTYPE**</span></span>               |
| <span data-ttu-id="c1d13-337">**SQL-DMO \_ E \_ INVALIDSTREAMINDEX**</span><span class="sxs-lookup"><span data-stu-id="c1d13-337">**DMO\_E\_INVALIDSTREAMINDEX**</span></span>  | <span data-ttu-id="c1d13-338">**MF \_ E \_ INVALIDSTREAMNUMBER**</span><span class="sxs-lookup"><span data-stu-id="c1d13-338">**MF\_E\_INVALIDSTREAMNUMBER**</span></span>       |
| <span data-ttu-id="c1d13-339">**SQL-DMO \_ E \_ NOTACCEPTING**</span><span class="sxs-lookup"><span data-stu-id="c1d13-339">**DMO\_E\_NOTACCEPTING**</span></span>        | <span data-ttu-id="c1d13-340">**MF \_ E \_ NOTACCEPTING**</span><span class="sxs-lookup"><span data-stu-id="c1d13-340">**MF\_E\_NOTACCEPTING**</span></span>              |
| <span data-ttu-id="c1d13-341">**\_E E \_ 沒有 \_ 其他 \_ 專案**</span><span class="sxs-lookup"><span data-stu-id="c1d13-341">**DMO\_E\_NO\_MORE\_ITEMS**</span></span>     | <span data-ttu-id="c1d13-342">**MF \_ E \_ 沒有 \_ 其他 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="c1d13-342">**MF\_E\_NO\_MORE\_TYPES**</span></span>           |
| <span data-ttu-id="c1d13-343">**\_E E \_ 類型 \_ 不 \_ 接受**</span><span class="sxs-lookup"><span data-stu-id="c1d13-343">**DMO\_E\_TYPE\_NOT\_ACCEPTED**</span></span> | <span data-ttu-id="c1d13-344">**MF \_ E \_ INVALIDMEDIATYPE**</span><span class="sxs-lookup"><span data-stu-id="c1d13-344">**MF\_E\_INVALIDMEDIATYPE**</span></span>          |
| <span data-ttu-id="c1d13-345">**\_E E \_ 類型 \_ 未 \_ 設定**</span><span class="sxs-lookup"><span data-stu-id="c1d13-345">**DMO\_E\_TYPE\_NOT\_SET**</span></span>      | <span data-ttu-id="c1d13-346">**\_ \_ \_ \_ 未設定 MF E 轉換 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="c1d13-346">**MF\_E\_TRANSFORM\_TYPE\_NOT\_SET**</span></span> |



 

## <a name="creating-hybrid-dmomft-objects"></a><span data-ttu-id="c1d13-347">建立混合式 SQL-DMO/MFT 物件</span><span class="sxs-lookup"><span data-stu-id="c1d13-347">Creating Hybrid DMO/MFT Objects</span></span>

<span data-ttu-id="c1d13-348">[**IMFTransform**](/windows/win32/api/mftransform/nn-mftransform-imftransform)介面會以 [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject)為基礎，這是 DirectX 媒體物件 (DMOs) 的主要介面。</span><span class="sxs-lookup"><span data-stu-id="c1d13-348">The [**IMFTransform**](/windows/win32/api/mftransform/nn-mftransform-imftransform) interface is loosely based on [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject), which is the primary interface for DirectX Media Objects (DMOs).</span></span> <span data-ttu-id="c1d13-349">您可以建立可公開這兩個介面的物件。</span><span class="sxs-lookup"><span data-stu-id="c1d13-349">It is possible to create objects that expose both interfaces.</span></span> <span data-ttu-id="c1d13-350">不過，這可能會導致命名衝突，因為介面具有某些共用相同名稱的方法。</span><span class="sxs-lookup"><span data-stu-id="c1d13-350">However, this can lead to naming collisions, because the interfaces have some methods that share the same name.</span></span> <span data-ttu-id="c1d13-351">您可以透過下列兩種方式之一來解決這個問題：</span><span class="sxs-lookup"><span data-stu-id="c1d13-351">You can solve this problem in one of two ways:</span></span>

<span data-ttu-id="c1d13-352">解決方案1：在包含 MFT 函式的任何 .cpp 檔案頂端包含下列程式程式碼：</span><span class="sxs-lookup"><span data-stu-id="c1d13-352">Solution 1: Include the following line at the top of any .cpp file that contains MFT functions:</span></span>

``` syntax
#define MFT_UNIQUE_METHOD_NAMES
```

<span data-ttu-id="c1d13-353">這會變更 [**IMFTransform**](/windows/win32/api/mftransform/nn-mftransform-imftransform) 介面的宣告，因此大部分的方法名稱前面都會加上 "MFT"。</span><span class="sxs-lookup"><span data-stu-id="c1d13-353">This changes the declaration of the [**IMFTransform**](/windows/win32/api/mftransform/nn-mftransform-imftransform) interface so that most of the method names are prefixed with "MFT".</span></span> <span data-ttu-id="c1d13-354">因此， [**IMFTransform：:P rocessinput**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processinput) 會變成 **IMFTransform：： MFTProcessInput**， [**IMediaObject：:P rocessinput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processinput) 會保留其原始名稱。</span><span class="sxs-lookup"><span data-stu-id="c1d13-354">Thus, [**IMFTransform::ProcessInput**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processinput) becomes **IMFTransform::MFTProcessInput**, while [**IMediaObject::ProcessInput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processinput) keeps its original name.</span></span> <span data-ttu-id="c1d13-355">如果您要將現有的 SQL-DMO 轉換成混合式的 SQL-DMO/MFT，這項技術最有用。</span><span class="sxs-lookup"><span data-stu-id="c1d13-355">This technique is most useful if you are converting an existing DMO to a hybrid DMO/MFT.</span></span> <span data-ttu-id="c1d13-356">您可以加入新的 MFT 方法，而不需要變更 SQL-DMO 方法。</span><span class="sxs-lookup"><span data-stu-id="c1d13-356">You can add the new MFT methods without changing the DMO methods.</span></span>

<span data-ttu-id="c1d13-357">解決方案2：使用 c + + 語法來區分繼承自多個介面的名稱。</span><span class="sxs-lookup"><span data-stu-id="c1d13-357">Solution 2: Use C++ syntax to disambiguate names that are inherited from more than one interface.</span></span> <span data-ttu-id="c1d13-358">例如，宣告 [**ProcessInput**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processinput) 的 MFT 版本，如下所示：</span><span class="sxs-lookup"><span data-stu-id="c1d13-358">For example, declare the MFT version of [**ProcessInput**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processinput) as follows:</span></span>

``` syntax
CMyHybridObject::IMFTransform::ProcessInput(...)
```

<span data-ttu-id="c1d13-359">宣告 [**ProcessInput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processinput) 的 sql-dmo 版本，如下所示：</span><span class="sxs-lookup"><span data-stu-id="c1d13-359">Declare the DMO version of [**ProcessInput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processinput) like this:</span></span>

``` syntax
CMyHybridObject::IMediaObject::ProcessInput(...)
```

<span data-ttu-id="c1d13-360">如果您對物件內的方法進行內部呼叫，您可以使用這個語法，但是這樣做會覆寫方法的虛擬狀態。</span><span class="sxs-lookup"><span data-stu-id="c1d13-360">If you make an internal call to a method within the object, you can use this syntax, but doing so will override the virtual status of the method.</span></span> <span data-ttu-id="c1d13-361">從物件內部進行呼叫的更好方法如下：</span><span class="sxs-lookup"><span data-stu-id="c1d13-361">A better way to make calls from inside the object is the following:</span></span>

``` syntax
hr = ((IMediaObject*)this)->ProcessInput(...)
```

<span data-ttu-id="c1d13-362">如此一來，如果您從 **CMyHybridObject** 衍生另一個類別，並覆寫 CMyHybridObject：： IMediaObject：:P rocessinput 方法，則會呼叫正確的虛擬方法。</span><span class="sxs-lookup"><span data-stu-id="c1d13-362">That way, if you derive another class from **CMyHybridObject** and override the CMyHybridObject::IMediaObject::ProcessInput method, the correct virtual method is called.</span></span> <span data-ttu-id="c1d13-363">SQL-DMO 介面記載于 DirectShow SDK 檔中。</span><span class="sxs-lookup"><span data-stu-id="c1d13-363">The DMO interfaces are documented in the DirectShow SDK documentation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c1d13-364">相關主題</span><span class="sxs-lookup"><span data-stu-id="c1d13-364">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c1d13-365">媒體基礎轉換</span><span class="sxs-lookup"><span data-stu-id="c1d13-365">Media Foundation Transforms</span></span>](media-foundation-transforms.md)
</dt> </dl>

 

 
