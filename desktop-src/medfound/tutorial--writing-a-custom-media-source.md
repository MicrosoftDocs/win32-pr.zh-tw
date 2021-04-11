---
description: 本主題深入探討 MPEG-2 媒體來源 SDK 範例。
ms.assetid: d392f30c-c963-4eb3-add2-1bb986919c0b
title: 案例研究： MPEG-2 媒體來源
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87e1f72cc6ae6df119439bdae1942732bf8d2fa2
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "104027646"
---
# <a name="case-study-mpeg-1-media-source"></a><span data-ttu-id="62cc4-103">案例研究： MPEG-2 媒體來源</span><span class="sxs-lookup"><span data-stu-id="62cc4-103">Case Study: MPEG-1 Media Source</span></span>

<span data-ttu-id="62cc4-104">在 Microsoft 媒體基礎中，將媒體資料引進資料管線的物件稱為 *媒體來源*。</span><span class="sxs-lookup"><span data-stu-id="62cc4-104">In Microsoft Media Foundation, the object that introduces media data into the data pipeline is called a *media source*.</span></span> <span data-ttu-id="62cc4-105">本主題深入探討 [Mpeg-2 媒體來源](mpeg1source-sample.md) SDK 範例。</span><span class="sxs-lookup"><span data-stu-id="62cc4-105">This topic takes an in-depth look at the [MPEG-1 Media Source](mpeg1source-sample.md) SDK Sample.</span></span>

-   [<span data-ttu-id="62cc4-106">先決條件</span><span class="sxs-lookup"><span data-stu-id="62cc4-106">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="62cc4-107">MPEG 1 來源中使用的 c + + 類別</span><span class="sxs-lookup"><span data-stu-id="62cc4-107">C++ Classes Used in the MPEG-1 Source</span></span>](#c-classes-used-in-the-mpeg-1-source)
-   [<span data-ttu-id="62cc4-108">位元組資料流程處理常式</span><span class="sxs-lookup"><span data-stu-id="62cc4-108">Byte-Stream Handler</span></span>](#byte-stream-handler)
-   [<span data-ttu-id="62cc4-109">簡報描述項</span><span class="sxs-lookup"><span data-stu-id="62cc4-109">Presentation Descriptor</span></span>](#presentation-descriptor)
-   [<span data-ttu-id="62cc4-110">串流狀態</span><span class="sxs-lookup"><span data-stu-id="62cc4-110">Streaming States</span></span>](#streaming-states)
    -   [<span data-ttu-id="62cc4-111">開始</span><span class="sxs-lookup"><span data-stu-id="62cc4-111">Start</span></span>](#start)
    -   [<span data-ttu-id="62cc4-112">暫停</span><span class="sxs-lookup"><span data-stu-id="62cc4-112">Pause</span></span>](#pause)
    -   [<span data-ttu-id="62cc4-113">停止</span><span class="sxs-lookup"><span data-stu-id="62cc4-113">Stop</span></span>](#stop)
-   [<span data-ttu-id="62cc4-114">範例要求</span><span class="sxs-lookup"><span data-stu-id="62cc4-114">Sample Requests</span></span>](#sample-requests)
-   [<span data-ttu-id="62cc4-115">資料流程結尾</span><span class="sxs-lookup"><span data-stu-id="62cc4-115">End of Stream</span></span>](#end-of-stream)
-   [<span data-ttu-id="62cc4-116">非同步作業</span><span class="sxs-lookup"><span data-stu-id="62cc4-116">Asynchronous Operations</span></span>](#asynchronous-operations)
    -   [<span data-ttu-id="62cc4-117">作業佇列</span><span class="sxs-lookup"><span data-stu-id="62cc4-117">Operation Queue</span></span>](#operation-queue)
-   [<span data-ttu-id="62cc4-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="62cc4-118">Related topics</span></span>](#related-topics)

## <a name="prerequisites"></a><span data-ttu-id="62cc4-119">必要條件</span><span class="sxs-lookup"><span data-stu-id="62cc4-119">Prerequisites</span></span>

<span data-ttu-id="62cc4-120">閱讀本主題之前，您應該先瞭解下列媒體基礎概念：</span><span class="sxs-lookup"><span data-stu-id="62cc4-120">Before reading this topic you should understand the following Media Foundation concepts:</span></span>

-   [<span data-ttu-id="62cc4-121">媒體來源物件模型</span><span class="sxs-lookup"><span data-stu-id="62cc4-121">Media Source Object Model</span></span>](media-source-object-model.md)
-   <span data-ttu-id="62cc4-122">[非同步回呼方法](asynchronous-callback-methods.md)。</span><span class="sxs-lookup"><span data-stu-id="62cc4-122">[Asynchronous Callback Methods](asynchronous-callback-methods.md).</span></span>
-   [<span data-ttu-id="62cc4-123">工作佇列</span><span class="sxs-lookup"><span data-stu-id="62cc4-123">Work Queues</span></span>](work-queues.md)
-   [<span data-ttu-id="62cc4-124">媒體事件產生器</span><span class="sxs-lookup"><span data-stu-id="62cc4-124">Media Event Generators</span></span>](media-event-generators.md)
-   [<span data-ttu-id="62cc4-125">媒體緩衝區</span><span class="sxs-lookup"><span data-stu-id="62cc4-125">Media Buffers</span></span>](media-buffers.md)
-   [<span data-ttu-id="62cc4-126">媒體範例</span><span class="sxs-lookup"><span data-stu-id="62cc4-126">Media Samples</span></span>](media-samples.md)
-   [<span data-ttu-id="62cc4-127">媒體類型</span><span class="sxs-lookup"><span data-stu-id="62cc4-127">Media Types</span></span>](media-types.md)

<span data-ttu-id="62cc4-128">您也應該對媒體基礎架構有基本的瞭解，特別是管線中媒體來源的角色。</span><span class="sxs-lookup"><span data-stu-id="62cc4-128">You should also have a basic understanding of the Media Foundation architecture, particularly the role of media sources in the pipeline.</span></span> <span data-ttu-id="62cc4-129"> (需詳細資訊，請參閱 [媒體來源](media-sources.md)。 ) </span><span class="sxs-lookup"><span data-stu-id="62cc4-129">(For more information, see [Media Sources](media-sources.md).)</span></span>

<span data-ttu-id="62cc4-130">此外，您可能會想要閱讀 [撰寫自訂媒體來源](writing-a-custom-media-source.md)的主題，以提供此處所述步驟的一般總覽。</span><span class="sxs-lookup"><span data-stu-id="62cc4-130">In addition, you may want to read the topic [Writing a Custom Media Source](writing-a-custom-media-source.md), which gives a more general overview of the steps described here.</span></span>

<span data-ttu-id="62cc4-131">本主題不會重現 SDK 範例中的所有程式碼，因為此範例相當大。</span><span class="sxs-lookup"><span data-stu-id="62cc4-131">This topic does not reproduce all of the code from the SDK sample, because the sample is fairly large.</span></span>

## <a name="c-classes-used-in-the-mpeg-1-source"></a><span data-ttu-id="62cc4-132">MPEG 1 來源中使用的 c + + 類別</span><span class="sxs-lookup"><span data-stu-id="62cc4-132">C++ Classes Used in the MPEG-1 Source</span></span>

<span data-ttu-id="62cc4-133">範例 MPEG-2 來源會使用下列 c + + 類別來執行：</span><span class="sxs-lookup"><span data-stu-id="62cc4-133">The sample MPEG-1 source is implemented with the following C++ classes:</span></span>

-   <span data-ttu-id="62cc4-134">`MPEG1ByteStreamHandler`.</span><span class="sxs-lookup"><span data-stu-id="62cc4-134">`MPEG1ByteStreamHandler`.</span></span> <span data-ttu-id="62cc4-135">針對媒體來源執行位元組資料流程處理常式。</span><span class="sxs-lookup"><span data-stu-id="62cc4-135">Implements the byte-stream handler for the media source.</span></span> <span data-ttu-id="62cc4-136">在指定位元組資料流程的情況下，位元組資料流程處理常式會建立來源的實例。</span><span class="sxs-lookup"><span data-stu-id="62cc4-136">Given a byte stream, the byte-stream handler creates an instance of the source.</span></span>
-   <span data-ttu-id="62cc4-137">`MPEG1Source`.</span><span class="sxs-lookup"><span data-stu-id="62cc4-137">`MPEG1Source`.</span></span> <span data-ttu-id="62cc4-138">實行媒體來源。</span><span class="sxs-lookup"><span data-stu-id="62cc4-138">Implements the media source.</span></span>
-   <span data-ttu-id="62cc4-139">`MPEG1Stream`.</span><span class="sxs-lookup"><span data-stu-id="62cc4-139">`MPEG1Stream`.</span></span> <span data-ttu-id="62cc4-140">實行媒體資料流程物件。</span><span class="sxs-lookup"><span data-stu-id="62cc4-140">Implements the media stream objects.</span></span> <span data-ttu-id="62cc4-141">媒體來源會 `MPEG1Stream` 為 MPEG 1 位流中的每個音訊或影片串流建立一個物件。</span><span class="sxs-lookup"><span data-stu-id="62cc4-141">The media source creates one `MPEG1Stream` object for every audio or video stream in the MPEG-1 bitstream.</span></span>
-   <span data-ttu-id="62cc4-142">`Parser`.</span><span class="sxs-lookup"><span data-stu-id="62cc4-142">`Parser`.</span></span> <span data-ttu-id="62cc4-143">剖析 MPEG 1 位流。</span><span class="sxs-lookup"><span data-stu-id="62cc4-143">Parses the MPEG-1 bitstream.</span></span> <span data-ttu-id="62cc4-144">在大部分的情況下，這個類別的詳細資料與媒體基礎 Api 無關。</span><span class="sxs-lookup"><span data-stu-id="62cc4-144">For the most part, the details of this class are not relevant to the Media Foundation APIs.</span></span>
-   <span data-ttu-id="62cc4-145">SourceOp，OpQueue：這兩個類別會管理媒體來源中的非同步作業。</span><span class="sxs-lookup"><span data-stu-id="62cc4-145">SourceOp, OpQueue: These two classes manage asynchronous operations in the media source.</span></span> <span data-ttu-id="62cc4-146"> (查看) 的 [非同步作業](#asynchronous-operations) 。</span><span class="sxs-lookup"><span data-stu-id="62cc4-146">(See [Asynchronous Operations](#asynchronous-operations)).</span></span>

<span data-ttu-id="62cc4-147">本主題稍後將說明其他其他協助程式類別。</span><span class="sxs-lookup"><span data-stu-id="62cc4-147">Other miscellaneous helper classes are described later in the topic.</span></span>

## <a name="byte-stream-handler"></a><span data-ttu-id="62cc4-148">Byte-Stream 處理常式</span><span class="sxs-lookup"><span data-stu-id="62cc4-148">Byte-Stream Handler</span></span>

<span data-ttu-id="62cc4-149">*位元組資料流程* 處理常式是建立媒體來源的物件。</span><span class="sxs-lookup"><span data-stu-id="62cc4-149">The *byte-stream* handler is the object that creates the media source.</span></span> <span data-ttu-id="62cc4-150">位元組資料流程處理常式是由來源解析程式所建立;應用程式不會直接與位元組資料流程處理常式互動。</span><span class="sxs-lookup"><span data-stu-id="62cc4-150">The byte-stream handler is created by the source resolver; applications do not interact directly with the byte-stream handler.</span></span> <span data-ttu-id="62cc4-151">來源解析程式會藉由查看登錄來探索位元組資料流程處理常式。</span><span class="sxs-lookup"><span data-stu-id="62cc4-151">The source resolver discovers the byte-stream handler by looking in the registry.</span></span> <span data-ttu-id="62cc4-152">處理常式是依副檔名或 MIME 類型來註冊。</span><span class="sxs-lookup"><span data-stu-id="62cc4-152">Handler are registered by file name extension or MIME type.</span></span> <span data-ttu-id="62cc4-153">針對 MPEG-2 來源，位元組資料流程處理常式會註冊 ". mpg" 副檔名。</span><span class="sxs-lookup"><span data-stu-id="62cc4-153">For the MPEG-1 source, the byte-stream handler is registered for the ".mpg" file name extension.</span></span>

> [!Note]  
> <span data-ttu-id="62cc4-154">如果您想要支援自訂 URL 配置，您也可以撰寫 *配置處理常式*。</span><span class="sxs-lookup"><span data-stu-id="62cc4-154">If you want to support custom URL schemes, you can also write a *scheme handler*.</span></span> <span data-ttu-id="62cc4-155">MPEG-2 來源是針對本機檔案所設計，媒體基礎已經提供 "file://" Url 的配置處理常式。</span><span class="sxs-lookup"><span data-stu-id="62cc4-155">The MPEG-1 source is designed for local files, and Media Foundation already provides a scheme handler for "file://" URLs.</span></span>

 

<span data-ttu-id="62cc4-156">位元組資料流程處理常式會執行 [**IMFByteStreamHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler) 介面。</span><span class="sxs-lookup"><span data-stu-id="62cc4-156">The byte-stream handler implements the [**IMFByteStreamHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler) interface.</span></span> <span data-ttu-id="62cc4-157">這個介面有兩個必須執行的最重要方法：</span><span class="sxs-lookup"><span data-stu-id="62cc4-157">This interface has two most important methods that must be implemented:</span></span>

-   <span data-ttu-id="62cc4-158">[**BeginCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-begincreateobject)。</span><span class="sxs-lookup"><span data-stu-id="62cc4-158">[**BeginCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-begincreateobject).</span></span> <span data-ttu-id="62cc4-159">開始非同步作業以建立媒體來源。</span><span class="sxs-lookup"><span data-stu-id="62cc4-159">Starts an asynchronous operation to create the media source.</span></span>
-   <span data-ttu-id="62cc4-160">[**EndCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-endcreateobject)。</span><span class="sxs-lookup"><span data-stu-id="62cc4-160">[**EndCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-endcreateobject).</span></span> <span data-ttu-id="62cc4-161">完成非同步呼叫。</span><span class="sxs-lookup"><span data-stu-id="62cc4-161">Completes the asynchronous call.</span></span>

<span data-ttu-id="62cc4-162">另外兩個方法是選擇性的，且未在 SDK 範例中執行：</span><span class="sxs-lookup"><span data-stu-id="62cc4-162">Two other methods are optional and not implemented in the SDK sample:</span></span>

-   <span data-ttu-id="62cc4-163">[**CancelObjectCreation**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-cancelobjectcreation)。</span><span class="sxs-lookup"><span data-stu-id="62cc4-163">[**CancelObjectCreation**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-cancelobjectcreation).</span></span> <span data-ttu-id="62cc4-164">取消 [**BeginCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-begincreateobject) 方法。</span><span class="sxs-lookup"><span data-stu-id="62cc4-164">Cancels the [**BeginCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-begincreateobject) method.</span></span> <span data-ttu-id="62cc4-165">此方法適用于啟動時可能會有高延遲的網路來源。</span><span class="sxs-lookup"><span data-stu-id="62cc4-165">This method is useful for a network source that might have a high latency at startup.</span></span>
-   <span data-ttu-id="62cc4-166">[**GetMaxNumberOfBytesRequiredForResolution**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-getmaxnumberofbytesrequiredforresolution)。</span><span class="sxs-lookup"><span data-stu-id="62cc4-166">[**GetMaxNumberOfBytesRequiredForResolution**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-getmaxnumberofbytesrequiredforresolution).</span></span> <span data-ttu-id="62cc4-167">取得處理常式將從來來源資料流讀取的最大位元組數目。</span><span class="sxs-lookup"><span data-stu-id="62cc4-167">Gets the maximum number of bytes that the handler will read from the source stream.</span></span> <span data-ttu-id="62cc4-168">如果您知道位元組資料流程處理常式可以建立媒體來源之前的資料量，請執行此方法。</span><span class="sxs-lookup"><span data-stu-id="62cc4-168">Implement this method if you know how much data the byte-stream handler before it can create the media source.</span></span> <span data-ttu-id="62cc4-169">否則，只會傳回 **E \_ >notimpl**。</span><span class="sxs-lookup"><span data-stu-id="62cc4-169">Otherwise, simply return **E\_NOTIMPL**.</span></span>

<span data-ttu-id="62cc4-170">以下是 [**BeginCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-begincreateobject) 方法的實作為：</span><span class="sxs-lookup"><span data-stu-id="62cc4-170">Here is the implementation of the [**BeginCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-begincreateobject) method:</span></span>


```C++
HRESULT MPEG1ByteStreamHandler::BeginCreateObject(
        /* [in] */ IMFByteStream *pByteStream,
        /* [in] */ LPCWSTR pwszURL,
        /* [in] */ DWORD dwFlags,
        /* [in] */ IPropertyStore *pProps,
        /* [out] */ IUnknown **ppIUnknownCancelCookie,  // Can be NULL
        /* [in] */ IMFAsyncCallback *pCallback,
        /* [in] */ IUnknown *punkState                  // Can be NULL
        )
{
    if (pByteStream == NULL)
    {
        return E_POINTER;
    }

    if (pCallback == NULL)
    {
        return E_POINTER;
    }

    if ((dwFlags & MF_RESOLUTION_MEDIASOURCE) == 0)
    {
        return E_INVALIDARG;
    }

    HRESULT hr = S_OK;

    IMFAsyncResult *pResult = NULL;
    MPEG1Source    *pSource = NULL;

    // Create an instance of the media source.
    hr = MPEG1Source::CreateInstance(&pSource);

    // Create a result object for the caller's async callback.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateAsyncResult(NULL, pCallback, punkState, &pResult);
    }

    // Start opening the source. This is an async operation.
    // When it completes, the source will invoke our callback
    // and then we will invoke the caller's callback.
    if (SUCCEEDED(hr))
    {
        hr = pSource->BeginOpen(pByteStream, this, NULL);
    }

    if (SUCCEEDED(hr))
    {
        if (ppIUnknownCancelCookie)
        {
            *ppIUnknownCancelCookie = NULL;
        }

        m_pSource = pSource;
        m_pSource->AddRef();

        m_pResult = pResult;
        m_pResult->AddRef();
    }

// cleanup
    SafeRelease(&pSource);
    SafeRelease(&pResult);
    return hr;
}
```



<span data-ttu-id="62cc4-171">此方法會執行下列步驟：</span><span class="sxs-lookup"><span data-stu-id="62cc4-171">The method performs the following steps:</span></span>

1.  <span data-ttu-id="62cc4-172">建立 `MPEG1Source` 物件的新執行個體。</span><span class="sxs-lookup"><span data-stu-id="62cc4-172">Creates a new instance of the `MPEG1Source` object.</span></span>
2.  <span data-ttu-id="62cc4-173">建立異步結果物件。</span><span class="sxs-lookup"><span data-stu-id="62cc4-173">Create an asynchronous result object.</span></span> <span data-ttu-id="62cc4-174">稍後會使用此物件來叫用來源解析程式的回呼方法。</span><span class="sxs-lookup"><span data-stu-id="62cc4-174">This object is used later to invoke the source resolver's callback method.</span></span>
3.  <span data-ttu-id="62cc4-175">呼叫 `MPEG1Source::BeginOpen` ，在類別中定義的非同步方法 `MPEG1Source` 。</span><span class="sxs-lookup"><span data-stu-id="62cc4-175">Calls `MPEG1Source::BeginOpen`, an asynchronous method defined in the `MPEG1Source` class.</span></span>
4.  <span data-ttu-id="62cc4-176">將 *ppIUnknownCancelCookie* 設定為 **Null**，這會通知呼叫端不支援 [**CancelObjectCreation**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-cancelobjectcreation) 。</span><span class="sxs-lookup"><span data-stu-id="62cc4-176">Sets *ppIUnknownCancelCookie* to **NULL**, which informs the caller that [**CancelObjectCreation**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-cancelobjectcreation) is not supported.</span></span>

<span data-ttu-id="62cc4-177">`MPEG1Source::BeginOpen`方法會執行讀取位元組資料流程和初始化物件的實際工作 `MPEG1Source` 。</span><span class="sxs-lookup"><span data-stu-id="62cc4-177">The `MPEG1Source::BeginOpen` method does the actual work of reading the byte stream and initializing the `MPEG1Source` object.</span></span> <span data-ttu-id="62cc4-178">這個方法不是公用 API 的一部分。</span><span class="sxs-lookup"><span data-stu-id="62cc4-178">This method is not part of the public API.</span></span> <span data-ttu-id="62cc4-179">您可以在處理常式和媒體來源之間定義符合您需求的任何機制。</span><span class="sxs-lookup"><span data-stu-id="62cc4-179">You can define any mechanism between the handler and the media source that suits your needs.</span></span> <span data-ttu-id="62cc4-180">將大部分的邏輯放入媒體來源，可讓位元組資料流程處理常式保持相當簡單。</span><span class="sxs-lookup"><span data-stu-id="62cc4-180">Putting most of the logic into the media source keeps the byte-stream handler relatively simple.</span></span>

<span data-ttu-id="62cc4-181">簡單地說， `BeginOpen` 會執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="62cc4-181">Briefly, `BeginOpen` does the following:</span></span>

1.  <span data-ttu-id="62cc4-182">呼叫 [**IMFByteStream：： GetCapabilities**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-getcapabilities) ，以驗證來源位元組資料流程是否可讀取和可搜尋。</span><span class="sxs-lookup"><span data-stu-id="62cc4-182">Calls [**IMFByteStream::GetCapabilities**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-getcapabilities) to verify that the source byte stream is both readable and seekable.</span></span>
2.  <span data-ttu-id="62cc4-183">呼叫 [**IMFByteStream：： BeginRead**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-beginread) 來啟動非同步 i/o 要求。</span><span class="sxs-lookup"><span data-stu-id="62cc4-183">Calls [**IMFByteStream::BeginRead**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-beginread) to start an asynchronous I/O request.</span></span>

<span data-ttu-id="62cc4-184">其餘的初始化會以非同步方式進行。</span><span class="sxs-lookup"><span data-stu-id="62cc4-184">The rest of the initialization occurs asynchronously.</span></span> <span data-ttu-id="62cc4-185">媒體來源會從資料流程讀取足夠的資料，以剖析 MPEG-2 序列標頭。</span><span class="sxs-lookup"><span data-stu-id="62cc4-185">The media source reads enough data from the stream to parse the MPEG-1 sequence headers.</span></span> <span data-ttu-id="62cc4-186">然後，它會建立 *展示* 描述項，這是用來描述檔案中音訊和影片資料流程的物件。</span><span class="sxs-lookup"><span data-stu-id="62cc4-186">Then it creates a *presentation descriptor*, which is the object used to describe the audio and video streams in the file.</span></span> <span data-ttu-id="62cc4-187"> (如需詳細資訊，請參閱 [展示描述](#presentation-descriptor)項。當作業完成時 ) `BeginOpen` ，位元組資料流程處理常式會叫用來源解析程式的回呼方法。</span><span class="sxs-lookup"><span data-stu-id="62cc4-187">(For more information, see [Presentation Descriptor](#presentation-descriptor).) When the `BeginOpen` operation completes, the byte-stream handler invokes the source resolver's callback method.</span></span> <span data-ttu-id="62cc4-188">屆時，來源解析程式會呼叫 [**IMFByteStreamHandler：： EndCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-endcreateobject)。</span><span class="sxs-lookup"><span data-stu-id="62cc4-188">At that point, the source resolver calls [**IMFByteStreamHandler::EndCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-endcreateobject).</span></span> <span data-ttu-id="62cc4-189">**EndCreateObject** 方法會傳回作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="62cc4-189">The **EndCreateObject** method returns the status of the operation.</span></span>


```C++
HRESULT MPEG1ByteStreamHandler::EndCreateObject(
        /* [in] */ IMFAsyncResult *pResult,
        /* [out] */ MF_OBJECT_TYPE *pObjectType,
        /* [out] */ IUnknown **ppObject)
{
    if (pResult == NULL || pObjectType == NULL || ppObject == NULL)
    {
        return E_POINTER;
    }

    HRESULT hr = S_OK;

    *pObjectType = MF_OBJECT_INVALID;
    *ppObject = NULL;

    hr = pResult->GetStatus();

    if (SUCCEEDED(hr))
    {
        *pObjectType = MF_OBJECT_MEDIASOURCE;

        assert(m_pSource != NULL);

        hr = m_pSource->QueryInterface(IID_PPV_ARGS(ppObject));
    }

    SafeRelease(&m_pSource);
    SafeRelease(&m_pResult);
    return hr;
}
```



<span data-ttu-id="62cc4-190">如果在此程式期間任何時候發生錯誤，則會叫用具有錯誤狀態碼的回呼。</span><span class="sxs-lookup"><span data-stu-id="62cc4-190">If an error occurs at any time during this process, the callback is invoked with an error status code.</span></span>

## <a name="presentation-descriptor"></a><span data-ttu-id="62cc4-191">簡報描述項</span><span class="sxs-lookup"><span data-stu-id="62cc4-191">Presentation Descriptor</span></span>

<span data-ttu-id="62cc4-192">簡報描述項描述 MPEG-2 檔案的內容，包括下列資訊：</span><span class="sxs-lookup"><span data-stu-id="62cc4-192">The presentation descriptor describes the contents of the MPEG-1 file, including the following information:</span></span>

-   <span data-ttu-id="62cc4-193">資料流程的數目。</span><span class="sxs-lookup"><span data-stu-id="62cc4-193">The number of the streams.</span></span>
-   <span data-ttu-id="62cc4-194">每個資料流程的格式。</span><span class="sxs-lookup"><span data-stu-id="62cc4-194">The format of each stream.</span></span>
-   <span data-ttu-id="62cc4-195">資料流程識別碼。</span><span class="sxs-lookup"><span data-stu-id="62cc4-195">Stream identifiers.</span></span>
-   <span data-ttu-id="62cc4-196">每個資料流程的選取狀態 (選取或取消選取) 。</span><span class="sxs-lookup"><span data-stu-id="62cc4-196">The selection status of each stream (selected or deselected).</span></span>

<span data-ttu-id="62cc4-197">就媒體基礎架構而言，表示描述項會包含一或多個 *資料流程描述* 項。</span><span class="sxs-lookup"><span data-stu-id="62cc4-197">In terms of the Media Foundation architecture, the presentation descriptor contains one or more *stream descriptors*.</span></span> <span data-ttu-id="62cc4-198">每個資料流程描述項都包含一個 *媒體類型處理常式*，可用來取得或設定資料流程上的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="62cc4-198">Each stream descriptor contains a *media type handler*, which is used to get or set media types on the stream.</span></span> <span data-ttu-id="62cc4-199">媒體基礎提供簡報描述元和資料流程描述項的內建實值;這些適用于大部分的媒體來源。</span><span class="sxs-lookup"><span data-stu-id="62cc4-199">Media Foundation provides stock implementations for the presentation descriptor and stream descriptor; these are suitable for most media sources.</span></span>

<span data-ttu-id="62cc4-200">若要建立展示描述項，請執行下列步驟：</span><span class="sxs-lookup"><span data-stu-id="62cc4-200">To create a presentation descriptor, perform the following steps:</span></span>

1.  <span data-ttu-id="62cc4-201">針對每個資料流程：</span><span class="sxs-lookup"><span data-stu-id="62cc4-201">For each stream:</span></span>
    1.  <span data-ttu-id="62cc4-202">提供資料流程識別碼和可能媒體類型的陣列。</span><span class="sxs-lookup"><span data-stu-id="62cc4-202">Provide a stream ID and an array of possible media types.</span></span> <span data-ttu-id="62cc4-203">如果資料流程支援一種以上的媒體類型，請依喜好設定排列媒體類型清單（若有的話）。</span><span class="sxs-lookup"><span data-stu-id="62cc4-203">If the stream supports more than one media type, order the list of media types by preference, if any.</span></span> <span data-ttu-id="62cc4-204"> (先放置最佳類型，最後才是最不理想的類型。 ) </span><span class="sxs-lookup"><span data-stu-id="62cc4-204">(Put the optimal type first, and the least optimal type last.)</span></span>
    2.  <span data-ttu-id="62cc4-205">呼叫 [**MFCreateStreamDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatestreamdescriptor) 來建立資料流程描述項。</span><span class="sxs-lookup"><span data-stu-id="62cc4-205">Call [**MFCreateStreamDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatestreamdescriptor) to create the stream descriptor.</span></span>
    3.  <span data-ttu-id="62cc4-206">在新建立的資料流程描述項上呼叫 [**IMFStreamDescriptor：： GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) 。</span><span class="sxs-lookup"><span data-stu-id="62cc4-206">Call [**IMFStreamDescriptor::GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) on the newly created stream descriptor.</span></span>
    4.  <span data-ttu-id="62cc4-207">呼叫 [**IMFMediaTypeHandler：： SetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype) 來設定資料流程的預設格式。</span><span class="sxs-lookup"><span data-stu-id="62cc4-207">Call [**IMFMediaTypeHandler::SetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype) to set the default format for the stream.</span></span> <span data-ttu-id="62cc4-208">如果有一種以上的媒體類型，您通常應該設定清單中的第一種類型。</span><span class="sxs-lookup"><span data-stu-id="62cc4-208">If there is more than one media type, you should generally set the first type in the list.</span></span>
2.  <span data-ttu-id="62cc4-209">呼叫 [**MFCreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepresentationdescriptor) 並傳入資料流程描述項指標的陣列。</span><span class="sxs-lookup"><span data-stu-id="62cc4-209">Call [**MFCreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepresentationdescriptor) and pass in the array of stream descriptor pointers.</span></span>
3.  <span data-ttu-id="62cc4-210">針對每個資料流程，呼叫 [**IMFPresentationDescriptor：： SelectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-selectstream) 或 [**DeselectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-deselectstream) 來設定預設選取狀態。</span><span class="sxs-lookup"><span data-stu-id="62cc4-210">For each stream, call [**IMFPresentationDescriptor::SelectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-selectstream) or [**DeselectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-deselectstream) to set the default selection state.</span></span> <span data-ttu-id="62cc4-211">如果有多個相同類型的資料流程 (音訊或影片) ，預設應該只選取其中一個。</span><span class="sxs-lookup"><span data-stu-id="62cc4-211">If there is more than one stream of the same type (audio or video), only one should be selected by default.</span></span>

<span data-ttu-id="62cc4-212">`MPEG1Source`物件會在其方法中建立展示描述項 `InitPresentationDescriptor` ：</span><span class="sxs-lookup"><span data-stu-id="62cc4-212">The `MPEG1Source` object creates the presentation descriptor in its `InitPresentationDescriptor` method:</span></span>


```C++
HRESULT MPEG1Source::InitPresentationDescriptor()
{
    HRESULT hr = S_OK;
    DWORD cStreams = 0;

    assert(m_pPresentationDescriptor == NULL);
    assert(m_state == STATE_OPENING);

    if (m_pHeader == NULL)
    {
        return E_FAIL;
    }

    // Get the number of streams, as declared in the MPEG-1 header, skipping
    // any streams with an unsupported format.
    for (DWORD i = 0; i < m_pHeader->cStreams; i++)
    {
        if (IsStreamTypeSupported(m_pHeader->streams[i].type))
        {
            cStreams++;
        }
    }

    // How many streams do we actually have?
    if (cStreams > m_streams.GetCount())
    {
        // Keep reading data until we have seen a packet for each stream.
        return S_OK;
    }

    // We should never create a stream we don't support.
    assert(cStreams == m_streams.GetCount());

    // Ready to create the presentation descriptor.

    // Create an array of IMFStreamDescriptor pointers.
    IMFStreamDescriptor **ppSD =
            new (std::nothrow) IMFStreamDescriptor*[cStreams];

    if (ppSD == NULL)
    {
        hr = E_OUTOFMEMORY;
        goto done;
    }

    ZeroMemory(ppSD, cStreams * sizeof(IMFStreamDescriptor*));

    // Fill the array by getting the stream descriptors from the streams.
    for (DWORD i = 0; i < cStreams; i++)
    {
        hr = m_streams[i]->GetStreamDescriptor(&ppSD[i]);
        if (FAILED(hr))
        {
            goto done;
        }
    }

    // Create the presentation descriptor.
    hr = MFCreatePresentationDescriptor(cStreams, ppSD,
        &m_pPresentationDescriptor);

    if (FAILED(hr))
    {
        goto done;
    }

    // Select the first video stream (if any).
    for (DWORD i = 0; i < cStreams; i++)
    {
        GUID majorType = GUID_NULL;

        hr = GetStreamMajorType(ppSD[i], &majorType);
        if (FAILED(hr))
        {
            goto done;
        }

        if (majorType == MFMediaType_Video)
        {
            hr = m_pPresentationDescriptor->SelectStream(i);
            if (FAILED(hr))
            {
                goto done;
            }
            break;
        }
    }

    // Switch state from "opening" to stopped.
    m_state = STATE_STOPPED;

    // Invoke the async callback to complete the BeginOpen operation.
    hr = CompleteOpen(S_OK);

done:
    // clean up:
    if (ppSD)
    {
        for (DWORD i = 0; i < cStreams; i++)
        {
            SafeRelease(&ppSD[i]);
        }
        delete [] ppSD;
    }
    return hr;
}
```



<span data-ttu-id="62cc4-213">應用程式會藉由呼叫 [**IMFMediaSource：： CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor)來取得簡報描述項。</span><span class="sxs-lookup"><span data-stu-id="62cc4-213">The application gets the presentation descriptor by calling [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).</span></span> <span data-ttu-id="62cc4-214">這個方法會藉由呼叫 [**IMFPresentationDescriptor：： Clone**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-clone)來建立簡報描述項的淺層複本。</span><span class="sxs-lookup"><span data-stu-id="62cc4-214">This method creates a shallow copy of the presentation descriptor by calling [**IMFPresentationDescriptor::Clone**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-clone).</span></span> <span data-ttu-id="62cc4-215"> (複本包含原始資料流程描述項的指標。 ) 應用程式可以使用展示描述項來設定媒體類型、選取資料流程或取消選取資料流程。</span><span class="sxs-lookup"><span data-stu-id="62cc4-215">(The copy contains pointers to the original stream descriptors.) The application can use the presentation descriptor to set the media type, select a stream, or deselect a stream.</span></span>

<span data-ttu-id="62cc4-216">（選擇性）表示描述項和資料流程描述項可以包含屬性，以提供來源的其他相關資訊。</span><span class="sxs-lookup"><span data-stu-id="62cc4-216">Optionally, presentation descriptors and stream descriptors can contain attributes that give additional information about the source.</span></span> <span data-ttu-id="62cc4-217">如需屬性的清單，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="62cc4-217">For a list such attributes, see the following topics:</span></span>

-   [<span data-ttu-id="62cc4-218">展示描述項屬性</span><span class="sxs-lookup"><span data-stu-id="62cc4-218">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
-   [<span data-ttu-id="62cc4-219">資料流程描述元屬性</span><span class="sxs-lookup"><span data-stu-id="62cc4-219">Stream Descriptor Attributes</span></span>](stream-descriptor-attributes.md)

<span data-ttu-id="62cc4-220">其中一個屬性值得特別注明： [ [**MF \_ PD \_ duration**](mf-pd-duration-attribute.md) ] 屬性包含來源的總持續時間。</span><span class="sxs-lookup"><span data-stu-id="62cc4-220">One attribute deserves special mention: The [**MF\_PD\_DURATION**](mf-pd-duration-attribute.md) attribute contains the total duration of the source.</span></span> <span data-ttu-id="62cc4-221">如果您事先知道持續時間，請設定此屬性;例如，視檔案格式而定，可能會在檔案標頭中指定持續時間。</span><span class="sxs-lookup"><span data-stu-id="62cc4-221">Set this attribute if you know the duration up front; for example, the duration might be specified in the file headers, depending on the file format.</span></span> <span data-ttu-id="62cc4-222">應用程式可能會顯示此值，或使用它來設定進度列或搜尋列。</span><span class="sxs-lookup"><span data-stu-id="62cc4-222">The application might display this value, or use it to set a progress bar or seek bar.</span></span>

## <a name="streaming-states"></a><span data-ttu-id="62cc4-223">串流狀態</span><span class="sxs-lookup"><span data-stu-id="62cc4-223">Streaming States</span></span>

<span data-ttu-id="62cc4-224">媒體來源會定義下列狀態：</span><span class="sxs-lookup"><span data-stu-id="62cc4-224">A media source defines the following states:</span></span>



| <span data-ttu-id="62cc4-225">州</span><span class="sxs-lookup"><span data-stu-id="62cc4-225">State</span></span>    | <span data-ttu-id="62cc4-226">描述</span><span class="sxs-lookup"><span data-stu-id="62cc4-226">Description</span></span>                                                                                                     |
|----------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62cc4-227">已開始</span><span class="sxs-lookup"><span data-stu-id="62cc4-227">Started</span></span>  | <span data-ttu-id="62cc4-228">來源接受並處理範例要求。</span><span class="sxs-lookup"><span data-stu-id="62cc4-228">The source accepts and processes sample requests.</span></span>                                                               |
| <span data-ttu-id="62cc4-229">已暫停</span><span class="sxs-lookup"><span data-stu-id="62cc4-229">Paused</span></span>   | <span data-ttu-id="62cc4-230">來源接受範例要求，但不會處理它們。</span><span class="sxs-lookup"><span data-stu-id="62cc4-230">The source accepts sample requests, but does not process them.</span></span> <span data-ttu-id="62cc4-231">要求會排入佇列，直到來源啟動為止。</span><span class="sxs-lookup"><span data-stu-id="62cc4-231">Requests are queued until the source is started.</span></span> |
| <span data-ttu-id="62cc4-232">已停止。</span><span class="sxs-lookup"><span data-stu-id="62cc4-232">Stopped.</span></span> | <span data-ttu-id="62cc4-233">來源會拒絕範例要求。</span><span class="sxs-lookup"><span data-stu-id="62cc4-233">The source rejects sample requests.</span></span>                                                                             |



 

### <a name="start"></a><span data-ttu-id="62cc4-234">開始</span><span class="sxs-lookup"><span data-stu-id="62cc4-234">Start</span></span>

<span data-ttu-id="62cc4-235">[**IMFMediaSource：： Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start)方法會啟動媒體來源。</span><span class="sxs-lookup"><span data-stu-id="62cc4-235">The [**IMFMediaSource::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) method starts the media source.</span></span> <span data-ttu-id="62cc4-236">它需要以下參數：</span><span class="sxs-lookup"><span data-stu-id="62cc4-236">It takes the following parameters:</span></span>

-   <span data-ttu-id="62cc4-237">展示描述項。</span><span class="sxs-lookup"><span data-stu-id="62cc4-237">A presentation descriptor.</span></span>
-   <span data-ttu-id="62cc4-238">時間格式 GUID。</span><span class="sxs-lookup"><span data-stu-id="62cc4-238">A time-format GUID.</span></span>
-   <span data-ttu-id="62cc4-239">開始位置。</span><span class="sxs-lookup"><span data-stu-id="62cc4-239">A start position.</span></span>

<span data-ttu-id="62cc4-240">應用程式必須藉由在來源上呼叫 [**CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepresentationdescriptor) 來取得簡報描述項。</span><span class="sxs-lookup"><span data-stu-id="62cc4-240">The application must obtain the presentation descriptor by calling [**CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepresentationdescriptor) on the source.</span></span> <span data-ttu-id="62cc4-241">沒有任何已定義的機制可驗證簡報描述項。</span><span class="sxs-lookup"><span data-stu-id="62cc4-241">There is no defined mechanism for validating a presentation descriptor.</span></span> <span data-ttu-id="62cc4-242">如果應用程式指定錯誤的表示描述項，則會產生未定義的結果。</span><span class="sxs-lookup"><span data-stu-id="62cc4-242">If the application specifies the wrong presentation descriptor, the results are undefined.</span></span>

<span data-ttu-id="62cc4-243">時間格式 GUID 會指定如何解讀開始位置。</span><span class="sxs-lookup"><span data-stu-id="62cc4-243">The time-format GUID specifies how to interpret the starting position.</span></span> <span data-ttu-id="62cc4-244">標準格式為 100-納 (ns) 單位，以 GUID Null 表示 \_ 。</span><span class="sxs-lookup"><span data-stu-id="62cc4-244">The standard format is 100-nanosecond (ns) units, indicated by GUID\_NULL.</span></span> <span data-ttu-id="62cc4-245">每個媒體來源都必須支援 100-ns 單位。</span><span class="sxs-lookup"><span data-stu-id="62cc4-245">Every media source must support 100-ns units.</span></span> <span data-ttu-id="62cc4-246">（選擇性）來源可支援其他時間單位，例如框架數或時間代碼。</span><span class="sxs-lookup"><span data-stu-id="62cc4-246">Optionally, a source can support other units of time, such as frame number or time code.</span></span> <span data-ttu-id="62cc4-247">不過，沒有標準的方式可以查詢媒體來源，以取得它所支援的時間格式清單。</span><span class="sxs-lookup"><span data-stu-id="62cc4-247">However, there is no standard way to query a media source for the list of time formats it supports.</span></span>

<span data-ttu-id="62cc4-248">開始位置會以 **PROPVARIANT** 的形式提供，根據時間格式允許不同的資料類型。</span><span class="sxs-lookup"><span data-stu-id="62cc4-248">The start position is given as a **PROPVARIANT**, allowing for different data types depending on the time format.</span></span> <span data-ttu-id="62cc4-249">若為 100-ns， **PROPVARIANT** 類型為 **Vt \_ I8** 或 **vt \_ 空白**。</span><span class="sxs-lookup"><span data-stu-id="62cc4-249">For 100-ns, the **PROPVARIANT** type is either **VT\_I8** or **VT\_EMPTY**.</span></span> <span data-ttu-id="62cc4-250">如果 **VT \_ I8**， **PROPVARIANT** 就會包含 100-ns 單位中的開始位置。</span><span class="sxs-lookup"><span data-stu-id="62cc4-250">If **VT\_I8**, the **PROPVARIANT** contains the start position in 100-ns units.</span></span> <span data-ttu-id="62cc4-251">**VT \_ 空白** 值具有「從目前位置開始」的特殊意義。</span><span class="sxs-lookup"><span data-stu-id="62cc4-251">The value **VT\_EMPTY** has the special meaning "start at the current position."</span></span>

<span data-ttu-id="62cc4-252">依照下列方式執行 [**啟動**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) 方法：</span><span class="sxs-lookup"><span data-stu-id="62cc4-252">Implement the [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) method as follows:</span></span>

1.  <span data-ttu-id="62cc4-253">驗證參數和狀態：</span><span class="sxs-lookup"><span data-stu-id="62cc4-253">Validate parameters and state:</span></span>
    -   <span data-ttu-id="62cc4-254">檢查是否有 **Null** 參數。</span><span class="sxs-lookup"><span data-stu-id="62cc4-254">Check for **NULL** parameters.</span></span>
    -   <span data-ttu-id="62cc4-255">檢查時間格式 GUID。</span><span class="sxs-lookup"><span data-stu-id="62cc4-255">Check the time-format GUID.</span></span> <span data-ttu-id="62cc4-256">如果值無效，則傳回 **MF \_ E \_ 不支援的 \_ 時間 \_ 格式**。</span><span class="sxs-lookup"><span data-stu-id="62cc4-256">If the value is invalid, return **MF\_E\_UNSUPPORTED\_TIME\_FORMAT**.</span></span>
    -   <span data-ttu-id="62cc4-257">檢查保存開始位置的 **PROPVARIANT** 資料類型。</span><span class="sxs-lookup"><span data-stu-id="62cc4-257">Check the data type of the **PROPVARIANT** that holds the start position.</span></span>
    -   <span data-ttu-id="62cc4-258">驗證開始位置。</span><span class="sxs-lookup"><span data-stu-id="62cc4-258">Validate the start position.</span></span> <span data-ttu-id="62cc4-259">如果無效，則傳回 **MF \_ E \_ INVALIDREQUEST**。</span><span class="sxs-lookup"><span data-stu-id="62cc4-259">If invalid, return **MF\_E\_INVALIDREQUEST**.</span></span>
    -   <span data-ttu-id="62cc4-260">如果來源已關閉，則傳回 **MF \_ E \_ 關機**。</span><span class="sxs-lookup"><span data-stu-id="62cc4-260">If the source has been shut down, return **MF\_E\_SHUTDOWN**.</span></span>
2.  <span data-ttu-id="62cc4-261">如果步驟1中未發生任何錯誤，請將非同步作業排入佇列。</span><span class="sxs-lookup"><span data-stu-id="62cc4-261">If no error occurs in step 1, queue an asynchronous operation.</span></span> <span data-ttu-id="62cc4-262">此步驟之後的所有專案都會在工作佇列執行緒上發生。</span><span class="sxs-lookup"><span data-stu-id="62cc4-262">Everything after this step occurs on a work-queue thread.</span></span>
3.  <span data-ttu-id="62cc4-263">針對每個資料流程：</span><span class="sxs-lookup"><span data-stu-id="62cc4-263">For each stream:</span></span>
    1.  <span data-ttu-id="62cc4-264">檢查資料流程是否已從先前的 [**啟動要求開始**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) 作用中。</span><span class="sxs-lookup"><span data-stu-id="62cc4-264">Check if the stream is already active from a previous [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) request.</span></span>
    2.  <span data-ttu-id="62cc4-265">呼叫 [**IMFPresentationDescriptor：： GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) ，以檢查應用程式是否已選取或取消選取資料流程。</span><span class="sxs-lookup"><span data-stu-id="62cc4-265">Call [**IMFPresentationDescriptor::GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) to check whether the application selected or deselected the stream.</span></span>
    3.  <span data-ttu-id="62cc4-266">如果先前選取的資料流程現在已取消選取，請清除該資料流程的任何未傳遞範例。</span><span class="sxs-lookup"><span data-stu-id="62cc4-266">If a previously selected stream is now deselected, flush any undelivered samples for that stream.</span></span>
    4.  <span data-ttu-id="62cc4-267">如果資料流程為使用中，則媒體來源 (不是資料流程) 傳送下列其中一個事件：</span><span class="sxs-lookup"><span data-stu-id="62cc4-267">If the stream is active, the media source (not the stream) sends one of the following events:</span></span>
        -   <span data-ttu-id="62cc4-268">如果資料流程先前為使用中，則會傳送 [MEUpdatedStream](meupdatedstream.md) 。</span><span class="sxs-lookup"><span data-stu-id="62cc4-268">It sends [MEUpdatedStream](meupdatedstream.md) if the stream was previously active.</span></span>
        -   <span data-ttu-id="62cc4-269">否則，它會傳送 [MENewStream](menewstream.md)。</span><span class="sxs-lookup"><span data-stu-id="62cc4-269">Otherwise, it sends [MENewStream](menewstream.md).</span></span>

        <span data-ttu-id="62cc4-270">針對這兩個事件，事件資料是資料流程的 [**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) 指標。</span><span class="sxs-lookup"><span data-stu-id="62cc4-270">For both events, the event data is the [**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) pointer for the stream.</span></span>
    5.  <span data-ttu-id="62cc4-271">如果來源從暫停狀態重新開機，可能會有擱置範例要求。</span><span class="sxs-lookup"><span data-stu-id="62cc4-271">If the source is restarting from the paused state, there might be pending sample requests.</span></span> <span data-ttu-id="62cc4-272">如果是，請立即傳遞。</span><span class="sxs-lookup"><span data-stu-id="62cc4-272">If so, deliver these now.</span></span>
    6.  <span data-ttu-id="62cc4-273">如果來源正在搜尋新的位置，每個資料流程物件都會傳送 [MEStreamSeeked](mestreamseeked.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="62cc4-273">If the source is seeking to a new position, each stream object sends an [MEStreamSeeked](mestreamseeked.md) event.</span></span> <span data-ttu-id="62cc4-274">否則，每個資料流程都會傳送 [MEStreamStarted](mestreamstarted.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="62cc4-274">Otherwise, each stream sends an [MEStreamStarted](mestreamstarted.md) event.</span></span>
4.  <span data-ttu-id="62cc4-275">如果來源正在搜尋新的位置，則媒體來源會傳送 [MESourceSeeked](mesourceseeked.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="62cc4-275">If the source is seeking to a new position, the media source sends an [MESourceSeeked](mesourceseeked.md) event.</span></span> <span data-ttu-id="62cc4-276">否則，它會傳送 [MESourceStarted](mesourcestarted.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="62cc4-276">Otherwise, it sends an [MESourceStarted](mesourcestarted.md) event.</span></span>

<span data-ttu-id="62cc4-277">如果在步驟2之後的任何時間發生錯誤，來源就會傳送含有錯誤碼的 [MESourceStarted](mesourcestarted.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="62cc4-277">If an error occurs at any time after step 2, the source sends an [MESourceStarted](mesourcestarted.md) event with an error code.</span></span> <span data-ttu-id="62cc4-278">這會對應用程式發出 [**啟動**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) 方法非同步失敗的警示。</span><span class="sxs-lookup"><span data-stu-id="62cc4-278">This alerts the application that the [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) method failed asynchronously.</span></span>

<span data-ttu-id="62cc4-279">下列程式碼顯示步驟 1-2：</span><span class="sxs-lookup"><span data-stu-id="62cc4-279">The following code shows steps 1–2:</span></span>


```C++
HRESULT MPEG1Source::Start(
        IMFPresentationDescriptor* pPresentationDescriptor,
        const GUID* pguidTimeFormat,
        const PROPVARIANT* pvarStartPos
    )
{

    HRESULT hr = S_OK;
    SourceOp *pAsyncOp = NULL;

    // Check parameters.

    // Start position and presentation descriptor cannot be NULL.
    if (pvarStartPos == NULL || pPresentationDescriptor == NULL)
    {
        return E_INVALIDARG;
    }

    // Check the time format.
    if ((pguidTimeFormat != NULL) && (*pguidTimeFormat != GUID_NULL))
    {
        // Unrecognized time format GUID.
        return MF_E_UNSUPPORTED_TIME_FORMAT;
    }

    // Check the data type of the start position.
    if ((pvarStartPos->vt != VT_I8) && (pvarStartPos->vt != VT_EMPTY))
    {
        return MF_E_UNSUPPORTED_TIME_FORMAT;
    }

    EnterCriticalSection(&m_critSec);

    // Check if this is a seek request. This sample does not support seeking.

    if (pvarStartPos->vt == VT_I8)
    {
        // If the current state is STOPPED, then position 0 is valid.
        // Otherwise, the start position must be VT_EMPTY (current position).

        if ((m_state != STATE_STOPPED) || (pvarStartPos->hVal.QuadPart != 0))
        {
            hr = MF_E_INVALIDREQUEST;
            goto done;
        }
    }

    // Fail if the source is shut down.
    hr = CheckShutdown();
    if (FAILED(hr))
    {
        goto done;
    }

    // Fail if the source was not initialized yet.
    hr = IsInitialized();
    if (FAILED(hr))
    {
        goto done;
    }

    // Perform a basic check on the caller's presentation descriptor.
    hr = ValidatePresentationDescriptor(pPresentationDescriptor);
    if (FAILED(hr))
    {
        goto done;
    }

    // The operation looks OK. Complete the operation asynchronously.
    hr = SourceOp::CreateStartOp(pPresentationDescriptor, &pAsyncOp);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pAsyncOp->SetData(*pvarStartPos);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = QueueOperation(pAsyncOp);

done:
    SafeRelease(&pAsyncOp);
    LeaveCriticalSection(&m_critSec);
    return hr;
}
```



<span data-ttu-id="62cc4-280">其餘步驟會顯示在下一個範例中：</span><span class="sxs-lookup"><span data-stu-id="62cc4-280">The remaining steps are shown in the next example:</span></span>


```C++
HRESULT MPEG1Source::DoStart(StartOp *pOp)
{
    assert(pOp->Op() == SourceOp::OP_START);

    IMFPresentationDescriptor *pPD = NULL;
    IMFMediaEvent  *pEvent = NULL;

    HRESULT     hr = S_OK;
    LONGLONG    llStartOffset = 0;
    BOOL        bRestartFromCurrentPosition = FALSE;
    BOOL        bSentEvents = FALSE;

    hr = BeginAsyncOp(pOp);

    // Get the presentation descriptor from the SourceOp object.
    // This is the PD that the caller passed into the Start() method.
    // The PD has already been validated.
    if (SUCCEEDED(hr))
    {
        hr = pOp->GetPresentationDescriptor(&pPD);
    }

    // Because this sample does not support seeking, the start
    // position must be 0 (from stopped) or "current position."

    // If the sample supported seeking, we would need to get the
    // start position from the PROPVARIANT data contained in pOp.

    if (SUCCEEDED(hr))
    {
        // Select/deselect streams, based on what the caller set in the PD.
        // This method also sends the MENewStream/MEUpdatedStream events.
        hr = SelectStreams(pPD, pOp->Data());
    }

    if (SUCCEEDED(hr))
    {
        m_state = STATE_STARTED;

        // Queue the "started" event. The event data is the start position.
        hr = m_pEventQueue->QueueEventParamVar(
            MESourceStarted,
            GUID_NULL,
            S_OK,
            &pOp->Data()
            );
    }

    if (FAILED(hr))
    {
        // Failure. Send the error code to the application.

        // Note: It's possible that QueueEvent itself failed, in which case it
        // is likely to fail again. But there is no good way to recover in
        // that case.

        (void)m_pEventQueue->QueueEventParamVar(
            MESourceStarted, GUID_NULL, hr, NULL);
    }

    CompleteAsyncOp(pOp);

    SafeRelease(&pEvent);
    SafeRelease(&pPD);
    return hr;
}
```



### <a name="pause"></a><span data-ttu-id="62cc4-281">暫停</span><span class="sxs-lookup"><span data-stu-id="62cc4-281">Pause</span></span>

<span data-ttu-id="62cc4-282">[**IMFMediaSource：:P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-pause)方法會暫停媒體來源。</span><span class="sxs-lookup"><span data-stu-id="62cc4-282">The [**IMFMediaSource::Pause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-pause) method pauses the media source.</span></span> <span data-ttu-id="62cc4-283">依照下列方式執行此方法：</span><span class="sxs-lookup"><span data-stu-id="62cc4-283">Implement this method as follows:</span></span>

1.  <span data-ttu-id="62cc4-284">將非同步作業排在佇列中。</span><span class="sxs-lookup"><span data-stu-id="62cc4-284">Queue an asynchronous operation.</span></span>
2.  <span data-ttu-id="62cc4-285">每個作用中的資料流程都會傳送 [MEStreamPaused](mestreampaused.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="62cc4-285">Each active stream sends an [MEStreamPaused](mestreampaused.md) event.</span></span>
3.  <span data-ttu-id="62cc4-286">媒體來源會傳送 [MESourcePaused](mesourcepaused.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="62cc4-286">The media source sends an [MESourcePaused](mesourcepaused.md) event.</span></span>

<span data-ttu-id="62cc4-287">暫停時，來源會將要求排在佇列中，而不需要處理它們。</span><span class="sxs-lookup"><span data-stu-id="62cc4-287">While paused, the source queues sample requests without processing them.</span></span> <span data-ttu-id="62cc4-288"> (查看 [範例要求](#sample-requests)。 ) </span><span class="sxs-lookup"><span data-stu-id="62cc4-288">(See [Sample Requests](#sample-requests).)</span></span>

### <a name="stop"></a><span data-ttu-id="62cc4-289">停止</span><span class="sxs-lookup"><span data-stu-id="62cc4-289">Stop</span></span>

<span data-ttu-id="62cc4-290">[**IMFMediaSource：： Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop)方法會停止媒體來源。</span><span class="sxs-lookup"><span data-stu-id="62cc4-290">The [**IMFMediaSource::Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop) method stops the media source.</span></span> <span data-ttu-id="62cc4-291">依照下列方式執行此方法：</span><span class="sxs-lookup"><span data-stu-id="62cc4-291">Implement this method as follows:</span></span>

1.  <span data-ttu-id="62cc4-292">將非同步作業排在佇列中。</span><span class="sxs-lookup"><span data-stu-id="62cc4-292">Queue an asynchronous operation.</span></span>
2.  <span data-ttu-id="62cc4-293">每個作用中的資料流程都會傳送 [MEStreamStopped](mestreamstopped.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="62cc4-293">Each active stream sends an [MEStreamStopped](mestreamstopped.md) event.</span></span>
3.  <span data-ttu-id="62cc4-294">清除所有已排入佇列的範例和範例要求。</span><span class="sxs-lookup"><span data-stu-id="62cc4-294">Clear all queued samples and sample requests.</span></span>
4.  <span data-ttu-id="62cc4-295">媒體來源會傳送 [MESourceStopped](mesourcestopped.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="62cc4-295">The media source sends an [MESourceStopped](mesourcestopped.md) event.</span></span>

<span data-ttu-id="62cc4-296">當停止時，來源會拒絕範例的所有要求。</span><span class="sxs-lookup"><span data-stu-id="62cc4-296">While stopped, the source rejects all requests for samples.</span></span>

<span data-ttu-id="62cc4-297">如果來源是在 i/o 要求進行時停止，則 i/o 要求可能會在來源進入 [已停止] 狀態之後完成。</span><span class="sxs-lookup"><span data-stu-id="62cc4-297">If the source is stopped while an I/O request is in progress, the I/O request might complete after the source enters the stopped state.</span></span> <span data-ttu-id="62cc4-298">在這種情況下，來源應該捨棄該 i/o 要求的結果。</span><span class="sxs-lookup"><span data-stu-id="62cc4-298">In that case, the source should discard the result of that I/O request.</span></span>

## <a name="sample-requests"></a><span data-ttu-id="62cc4-299">範例要求</span><span class="sxs-lookup"><span data-stu-id="62cc4-299">Sample Requests</span></span>

<span data-ttu-id="62cc4-300">媒體基礎使用 *提取* 模型，在此模型中，管線會從媒體來源要求範例。</span><span class="sxs-lookup"><span data-stu-id="62cc4-300">Media Foundation use a *pull* model, in which the pipeline requests samples from the media source.</span></span> <span data-ttu-id="62cc4-301">這不同于 DirectShow 所使用的模型，其中來源會「推送」範例。</span><span class="sxs-lookup"><span data-stu-id="62cc4-301">This differs from the model used by DirectShow, in which the sources "pushes" samples.</span></span>

<span data-ttu-id="62cc4-302">若要要求新的範例，媒體基礎管線會呼叫 [**IMFMediaStream：： RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample)。</span><span class="sxs-lookup"><span data-stu-id="62cc4-302">To request a new sample, the Media Foundation pipeline calls [**IMFMediaStream::RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample).</span></span> <span data-ttu-id="62cc4-303">這個方法會採用表示 *權杖* 物件的 **IUnknown** 指標。</span><span class="sxs-lookup"><span data-stu-id="62cc4-303">This method takes an **IUnknown** pointer that represents a *token* object.</span></span> <span data-ttu-id="62cc4-304">Token 物件的實作為呼叫端;它只會提供一種方法讓呼叫端追蹤範例要求。</span><span class="sxs-lookup"><span data-stu-id="62cc4-304">The implementation of the token object is up to the caller; it simply provides a way for the caller to track sample requests.</span></span> <span data-ttu-id="62cc4-305">Token 參數也可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="62cc4-305">The token parameter can also be **NULL**.</span></span>

<span data-ttu-id="62cc4-306">假設來源使用非同步 i/o 要求來讀取資料，則產生的範例不會與範例要求同步處理。</span><span class="sxs-lookup"><span data-stu-id="62cc4-306">Assuming the source uses asynchronous I/O requests to read data, sample generation will not be synchronized with sample requests.</span></span> <span data-ttu-id="62cc4-307">若要同步處理範例要求和產生範例，媒體來源會執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="62cc4-307">To synchronize sample requests with sample generation, a media source does the following:</span></span>

1.  <span data-ttu-id="62cc4-308">要求權杖會放置在佇列中。</span><span class="sxs-lookup"><span data-stu-id="62cc4-308">Request tokens are placed on a queue.</span></span>
2.  <span data-ttu-id="62cc4-309">當產生樣本時，會將它們放在第二個佇列上。</span><span class="sxs-lookup"><span data-stu-id="62cc4-309">As samples are generated, they are placed on a second queue.</span></span>
3.  <span data-ttu-id="62cc4-310">媒體來源會從第一個佇列提取要求權杖，並從第二個佇列提取一個範例，以完成範例要求。</span><span class="sxs-lookup"><span data-stu-id="62cc4-310">The media source completes a sample request by pulling a request token from the first queue and a sample from the second queue.</span></span>
4.  <span data-ttu-id="62cc4-311">媒體來源會傳送 MEMediaSample 事件。</span><span class="sxs-lookup"><span data-stu-id="62cc4-311">The media source sends an MEMediaSample event.</span></span> <span data-ttu-id="62cc4-312">此事件包含範例的指標，且範例包含權杖的指標。</span><span class="sxs-lookup"><span data-stu-id="62cc4-312">The event contains a pointer to the sample, and the sample contains a pointer to the token.</span></span>

<span data-ttu-id="62cc4-313">下圖顯示 [MEMediaSample](memediasample.md) 事件、範例與要求權杖之間的關聯性。</span><span class="sxs-lookup"><span data-stu-id="62cc4-313">The following diagram shows the relationship between the [MEMediaSample](memediasample.md) event, the sample, and the request token.</span></span>

![顯示 memediasample 和指向 imfsample 的範例佇列的圖表;imfsample 和要求佇列點至 iunknown](images/mediasourceimpl01.png)

<span data-ttu-id="62cc4-315">範例 MPEG-2 來源會依照下列方式來執行此程式：</span><span class="sxs-lookup"><span data-stu-id="62cc4-315">The example MPEG-1 source implements this process as follows:</span></span>

1.  <span data-ttu-id="62cc4-316">[**RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample)方法會將要求放在 FIFO 佇列上。</span><span class="sxs-lookup"><span data-stu-id="62cc4-316">The [**RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) method puts the request on a FIFO queue.</span></span>
2.  <span data-ttu-id="62cc4-317">當 i/o 要求完成時，媒體來源會建立新的範例，並將它們放在第二個 FIFO 佇列上。</span><span class="sxs-lookup"><span data-stu-id="62cc4-317">As I/O requests are completed, the media source creates new samples and puts them on a second FIFO queue.</span></span> <span data-ttu-id="62cc4-318"> (此佇列的大小上限，以防止來源讀取太遠的進度。 ) </span><span class="sxs-lookup"><span data-stu-id="62cc4-318">(This queue has a maximum size, to prevent the source from reading too far ahead.)</span></span>
3.  <span data-ttu-id="62cc4-319">只要兩個佇列都至少有一個專案 (一個要求和一個範例) ，媒體來源就會從範例佇列中送出第一個範例，以完成要求佇列中的第一個要求。</span><span class="sxs-lookup"><span data-stu-id="62cc4-319">Whenever both of these queues have at least one item (one request and one sample), the media source completes the first request from the request queue by sending out the first sample from the sample queue.</span></span>
4.  <span data-ttu-id="62cc4-320">為了傳遞範例，資料流程物件 (不是) 傳送 [MEMediaSample](memediasample.md) 事件的來源物件。</span><span class="sxs-lookup"><span data-stu-id="62cc4-320">To deliver a sample, the stream object (not the source object) sends an [MEMediaSample](memediasample.md) event.</span></span>
    -   <span data-ttu-id="62cc4-321">事件資料是範例 [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="62cc4-321">The event data is a pointer to the sample's [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) interface.</span></span>
    -   <span data-ttu-id="62cc4-322">如果要求包含權杖，請在範例上設定 [**MFSampleExtension \_ token**](mfsampleextension-token-attribute.md) 屬性，以將權杖附加至範例。</span><span class="sxs-lookup"><span data-stu-id="62cc4-322">If the request included a token, attach the token to the sample by setting the [**MFSampleExtension\_Token**](mfsampleextension-token-attribute.md) attribute on the sample.</span></span>

<span data-ttu-id="62cc4-323">目前有三種可能性：</span><span class="sxs-lookup"><span data-stu-id="62cc4-323">At this point, there are three possibilities:</span></span>

-   <span data-ttu-id="62cc4-324">範例佇列中有另一個範例，但沒有相符的要求。</span><span class="sxs-lookup"><span data-stu-id="62cc4-324">There is another sample in the sample queue, but no matching request.</span></span>
-   <span data-ttu-id="62cc4-325">有一個要求，但沒有範例。</span><span class="sxs-lookup"><span data-stu-id="62cc4-325">There is a request, but no sample.</span></span>
-   <span data-ttu-id="62cc4-326">這兩個佇列都是空的;沒有任何範例和要求。</span><span class="sxs-lookup"><span data-stu-id="62cc4-326">Both queues are empty; there are no samples and no requests.</span></span>

<span data-ttu-id="62cc4-327">如果範例佇列是空的，則來源會檢查資料流程的結尾 (查看資料流程) 的 [結尾](#end-of-stream) 。</span><span class="sxs-lookup"><span data-stu-id="62cc4-327">If the sample queue is empty, the source checks for the end of the stream (see [End of Stream](#end-of-stream)).</span></span> <span data-ttu-id="62cc4-328">否則，它會啟動資料的另一個 i/o 要求。</span><span class="sxs-lookup"><span data-stu-id="62cc4-328">Otherwise, it starts another I/O request for data.</span></span> <span data-ttu-id="62cc4-329">如果在此程式期間發生任何錯誤，資料流程將會傳送 [MEError](meerror.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="62cc4-329">If any error occurs during this process, the stream sends an [MEError](meerror.md) event.</span></span>

<span data-ttu-id="62cc4-330">下列程式碼會實行 [**IMFMediaStream：： RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) 方法：</span><span class="sxs-lookup"><span data-stu-id="62cc4-330">The following code implements the [**IMFMediaStream::RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) method:</span></span>


```C++
HRESULT MPEG1Stream::RequestSample(IUnknown* pToken)
{
    HRESULT hr = S_OK;
    IMFMediaSource *pSource = NULL;

    // Hold the media source object's critical section.
    SourceLock lock(m_pSource);

    hr = CheckShutdown();
    if (FAILED(hr))
    {
        goto done;
    }

    if (m_state == STATE_STOPPED)
    {
        hr = MF_E_INVALIDREQUEST;
        goto done;
    }

    if (!m_bActive)
    {
        // If the stream is not active, it should not get sample requests.
        hr = MF_E_INVALIDREQUEST;
        goto done;
    }

    if (m_bEOS && m_Samples.IsEmpty())
    {
        // This stream has already reached the end of the stream, and the
        // sample queue is empty.
        hr = MF_E_END_OF_STREAM;
        goto done;
    }

    hr = m_Requests.InsertBack(pToken);
    if (FAILED(hr))
    {
        goto done;
    }

    // Dispatch the request.
    hr = DispatchSamples();
    if (FAILED(hr))
    {
        goto done;
    }

done:
    if (FAILED(hr) && (m_state != STATE_SHUTDOWN))
    {
        // An error occurred. Send an MEError even from the source,
        // unless the source is already shut down.
        hr = m_pSource->QueueEvent(MEError, GUID_NULL, hr, NULL);
    }
    return hr;
}
```



<span data-ttu-id="62cc4-331">`DispatchSamples`方法會從範例佇列提取範例、將它們與擱置的範例要求比對，以及佇列[MEMediaSample](memediasample.md)事件：</span><span class="sxs-lookup"><span data-stu-id="62cc4-331">The `DispatchSamples` method pulls samples from the sample queue, matches them with pending sample requests, and queues [MEMediaSample](memediasample.md) events:</span></span>


```C++
HRESULT MPEG1Stream::DispatchSamples()
{
    HRESULT hr = S_OK;
    BOOL bNeedData = FALSE;
    BOOL bEOS = FALSE;

    SourceLock lock(m_pSource);

    // An I/O request can complete after the source is paused, stopped, or
    // shut down. Do not deliver samples unless the source is running.
    if (m_state != STATE_STARTED)
    {
        return S_OK;
    }

    IMFSample *pSample = NULL;
    IUnknown  *pToken = NULL;

    // Deliver as many samples as we can.
    while (!m_Samples.IsEmpty() && !m_Requests.IsEmpty())
    {
        // Pull the next sample from the queue.
        hr = m_Samples.RemoveFront(&pSample);
        if (FAILED(hr))
        {
            goto done;
        }

        // Pull the next request token from the queue. Tokens can be NULL.
        hr = m_Requests.RemoveFront(&pToken);
        if (FAILED(hr))
        {
            goto done;
        }

        if (pToken)
        {
            // Set the token on the sample.
            hr = pSample->SetUnknown(MFSampleExtension_Token, pToken);
            if (FAILED(hr))
            {
                goto done;
            }
        }

        // Send an MEMediaSample event with the sample.
        hr = m_pEventQueue->QueueEventParamUnk(
            MEMediaSample, GUID_NULL, S_OK, pSample);

        if (FAILED(hr))
        {
            goto done;
        }

        SafeRelease(&pSample);
        SafeRelease(&pToken);
    }

    if (m_Samples.IsEmpty() && m_bEOS)
    {
        // The sample queue is empty AND we have reached the end of the source
        // stream. Notify the pipeline by sending the end-of-stream event.

        hr = m_pEventQueue->QueueEventParamVar(
            MEEndOfStream, GUID_NULL, S_OK, NULL);

        if (FAILED(hr))
        {
            goto done;
        }

        // Notify the source. It will send the end-of-presentation event.
        hr = m_pSource->QueueAsyncOperation(SourceOp::OP_END_OF_STREAM);
        if (FAILED(hr))
        {
            goto done;
        }
    }
    else if (NeedsData())
    {
        // The sample queue is empty; the request queue is not empty; and we
        // have not reached the end of the stream. Ask for more data.
        hr = m_pSource->QueueAsyncOperation(SourceOp::OP_REQUEST_DATA);
        if (FAILED(hr))
        {
            goto done;
        }
    }

done:
    if (FAILED(hr) && (m_state != STATE_SHUTDOWN))
    {
        // An error occurred. Send an MEError even from the source,
        // unless the source is already shut down.
        m_pSource->QueueEvent(MEError, GUID_NULL, hr, NULL);
    }

    SafeRelease(&pSample);
    SafeRelease(&pToken);
    return S_OK;
}
```



<span data-ttu-id="62cc4-332">在 `DispatchSamples` 下列情況下，會呼叫方法：</span><span class="sxs-lookup"><span data-stu-id="62cc4-332">The `DispatchSamples` method is called in the following circumstances:</span></span>

-   <span data-ttu-id="62cc4-333">在 [**RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) 方法內。</span><span class="sxs-lookup"><span data-stu-id="62cc4-333">Inside the [**RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) method.</span></span>
-   <span data-ttu-id="62cc4-334">當媒體來源從暫停狀態重新開機時。</span><span class="sxs-lookup"><span data-stu-id="62cc4-334">When the media source restarts from the paused state.</span></span>
-   <span data-ttu-id="62cc4-335">當 i/o 要求完成時。</span><span class="sxs-lookup"><span data-stu-id="62cc4-335">When an I/O request completes.</span></span>

## <a name="end-of-stream"></a><span data-ttu-id="62cc4-336">資料流程結尾</span><span class="sxs-lookup"><span data-stu-id="62cc4-336">End of Stream</span></span>

<span data-ttu-id="62cc4-337">當資料流程沒有其他資料，而且已傳遞該資料流程的所有範例時，資料流程物件就會傳送 [MEEndOfStream](meendofstream.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="62cc4-337">When a stream has no more data, and all of the samples for that stream have been delivered, the stream objects sends an [MEEndOfStream](meendofstream.md) event.</span></span>

<span data-ttu-id="62cc4-338">當所有作用中資料流程完成時，媒體來源會傳送 [MEEndOfPresentation](meendofpresentation.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="62cc4-338">When all of the active streams are done, the media source sends an [MEEndOfPresentation](meendofpresentation.md) event.</span></span>

## <a name="asynchronous-operations"></a><span data-ttu-id="62cc4-339">非同步作業</span><span class="sxs-lookup"><span data-stu-id="62cc4-339">Asynchronous Operations</span></span>

<span data-ttu-id="62cc4-340">撰寫媒體來源最困難的部分是瞭解媒體基礎的非同步模型。</span><span class="sxs-lookup"><span data-stu-id="62cc4-340">Perhaps the hardest part of writing a media source is understanding the Media Foundation asynchronous model.</span></span>

<span data-ttu-id="62cc4-341">媒體來源上控制串流的所有方法都是非同步。</span><span class="sxs-lookup"><span data-stu-id="62cc4-341">All of the methods on a media source that control streaming are asynchronous.</span></span> <span data-ttu-id="62cc4-342">在每個案例中，方法會執行一些初始驗證，例如檢查參數。</span><span class="sxs-lookup"><span data-stu-id="62cc4-342">In each case, the method does some initial validation, such as checking parameters.</span></span> <span data-ttu-id="62cc4-343">然後，來源會將其餘的工作分派至工作佇列。</span><span class="sxs-lookup"><span data-stu-id="62cc4-343">The source then dispatches the rest of the work to a work queue.</span></span> <span data-ttu-id="62cc4-344">作業完成之後，媒體來源會透過媒體來源的 [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) 介面，將事件傳回給呼叫者。</span><span class="sxs-lookup"><span data-stu-id="62cc4-344">After the operation completes, the media source sends an event back to the caller, through the media source's [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) interface.</span></span> <span data-ttu-id="62cc4-345">因此，瞭解工作佇列是很重要的。</span><span class="sxs-lookup"><span data-stu-id="62cc4-345">It is therefore important to understand work queues.</span></span>

<span data-ttu-id="62cc4-346">若要將專案放在工作佇列中，您可以呼叫 [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) 或 [**MFPutWorkItemEx**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitemex)。</span><span class="sxs-lookup"><span data-stu-id="62cc4-346">To put an item on a work queue, you can call either [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) or [**MFPutWorkItemEx**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitemex).</span></span> <span data-ttu-id="62cc4-347">MPEG-2 來源是使用 **MFPutWorkItem**，但這兩個函式會執行相同的動作。</span><span class="sxs-lookup"><span data-stu-id="62cc4-347">The MPEG-1 source happens to use **MFPutWorkItem**, but the two functions do the same thing.</span></span> <span data-ttu-id="62cc4-348">**MFPutWorkItem** 函式會使用下列參數：</span><span class="sxs-lookup"><span data-stu-id="62cc4-348">The **MFPutWorkItem** function takes the following parameters:</span></span>

-   <span data-ttu-id="62cc4-349">識別工作佇列的 **DWORD** 值。</span><span class="sxs-lookup"><span data-stu-id="62cc4-349">A **DWORD** value that identifies the work queue.</span></span> <span data-ttu-id="62cc4-350">您可以建立私用工作佇列，或使用 **MFASYNC \_ 回呼 \_ 佇列 \_ 標準**。</span><span class="sxs-lookup"><span data-stu-id="62cc4-350">You can create a private work queue or use **MFASYNC\_CALLBACK\_QUEUE\_STANDARD**.</span></span>
-   <span data-ttu-id="62cc4-351">[**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback)介面的指標。</span><span class="sxs-lookup"><span data-stu-id="62cc4-351">A pointer to the [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface.</span></span> <span data-ttu-id="62cc4-352">叫用此回呼介面來執行工作。</span><span class="sxs-lookup"><span data-stu-id="62cc4-352">This callback interface is invoked to perform the work.</span></span>
-   <span data-ttu-id="62cc4-353">選用的狀態物件，必須執行 **IUnknown**。</span><span class="sxs-lookup"><span data-stu-id="62cc4-353">An optional state object, which must implement **IUnknown**.</span></span>

<span data-ttu-id="62cc4-354">工作佇列是由一或多個背景工作執行緒所提供，這些執行緒會持續從佇列提取下一個工作專案，並叫用回呼介面的 [**IMFAsyncCallback：： invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) 方法。</span><span class="sxs-lookup"><span data-stu-id="62cc4-354">The work queue is serviced by one or more worker threads that continuously pull the next work item from the queue and invoke the [**IMFAsyncCallback::Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) method of the callback interface.</span></span>

<span data-ttu-id="62cc4-355">不保證會以您將工作專案放在佇列上的相同順序來執行工作專案。</span><span class="sxs-lookup"><span data-stu-id="62cc4-355">Work items are not guaranteed to execute in the same order that you put them on the queue.</span></span> <span data-ttu-id="62cc4-356">請記住，有一個以上的執行緒可以服務相同的工作佇列 [**，因此叫**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) 用呼叫可以依順序重迭或發生。</span><span class="sxs-lookup"><span data-stu-id="62cc4-356">Remember that more than one thread can service the same work queue, so [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) calls can overlap or occur out of order.</span></span> <span data-ttu-id="62cc4-357">因此，以正確的順序提交工作佇列專案，可由媒體來源維持正確的內部狀態。</span><span class="sxs-lookup"><span data-stu-id="62cc4-357">Therefore, it is up to the media source to maintain the correct internal state, by submitting work queue items in the right order.</span></span> <span data-ttu-id="62cc4-358">只有當先前的作業完成時，來源才會開始下一項作業。</span><span class="sxs-lookup"><span data-stu-id="62cc4-358">Only when the previous operation is complete does the source start the next operation.</span></span>

<span data-ttu-id="62cc4-359">為了表示暫止的作業，MPEG 1 來源定義了名為的類別 `SourceOp` ：</span><span class="sxs-lookup"><span data-stu-id="62cc4-359">To represent pending operations, the MPEG-1 source defines a class named `SourceOp`:</span></span>


```C++
// Represents a request for an asynchronous operation.

class SourceOp : public IUnknown
{
public:

    enum Operation
    {
        OP_START,
        OP_PAUSE,
        OP_STOP,
        OP_REQUEST_DATA,
        OP_END_OF_STREAM
    };

    static HRESULT CreateOp(Operation op, SourceOp **ppOp);
    static HRESULT CreateStartOp(IMFPresentationDescriptor *pPD, SourceOp **ppOp);

    // IUnknown
    STDMETHODIMP QueryInterface(REFIID iid, void** ppv);
    STDMETHODIMP_(ULONG) AddRef();
    STDMETHODIMP_(ULONG) Release();

    SourceOp(Operation op);
    virtual ~SourceOp();

    HRESULT SetData(const PROPVARIANT& var);

    Operation Op() const { return m_op; }
    const PROPVARIANT& Data() { return m_data;}

protected:
    long        m_cRef;     // Reference count.
    Operation   m_op;
    PROPVARIANT m_data;     // Data for the operation.
};
```



<span data-ttu-id="62cc4-360">`Operation`列舉會識別正在暫止的作業。</span><span class="sxs-lookup"><span data-stu-id="62cc4-360">The `Operation` enumeration identifies which operation is pending.</span></span> <span data-ttu-id="62cc4-361">類別也包含 **PROPVARIANT** ，以傳達作業的任何其他資料。</span><span class="sxs-lookup"><span data-stu-id="62cc4-361">The class also contains a **PROPVARIANT** to convey any additional data for the operation.</span></span>

### <a name="operation-queue"></a><span data-ttu-id="62cc4-362">作業佇列</span><span class="sxs-lookup"><span data-stu-id="62cc4-362">Operation Queue</span></span>

<span data-ttu-id="62cc4-363">為了序列化作業，媒體來源會維護物件的佇列 `SourceOp` 。</span><span class="sxs-lookup"><span data-stu-id="62cc4-363">To serialize operations, the media source maintains a queue of `SourceOp` objects.</span></span> <span data-ttu-id="62cc4-364">它會使用 helper 類別來管理佇列：</span><span class="sxs-lookup"><span data-stu-id="62cc4-364">It uses a helper class to manage the queue:</span></span>


```C++
template <class OP_TYPE>
class OpQueue : public IUnknown
{
public:

    typedef ComPtrList<OP_TYPE>   OpList;

    HRESULT QueueOperation(OP_TYPE *pOp);

protected:

    HRESULT ProcessQueue();
    HRESULT ProcessQueueAsync(IMFAsyncResult *pResult);

    virtual HRESULT DispatchOperation(OP_TYPE *pOp) = 0;
    virtual HRESULT ValidateOperation(OP_TYPE *pOp) = 0;

    OpQueue(CRITICAL_SECTION& critsec)
        : m_OnProcessQueue(this, &OpQueue::ProcessQueueAsync),
          m_critsec(critsec)
    {
    }

    virtual ~OpQueue()
    {
    }

protected:
    OpList                  m_OpQueue;         // Queue of operations.
    CRITICAL_SECTION&       m_critsec;         // Protects the queue state.
    AsyncCallback<OpQueue>  m_OnProcessQueue;  // ProcessQueueAsync callback.
};
```



<span data-ttu-id="62cc4-365">`OpQueue`類別的設計是要由執行非同步工作專案的元件所繼承。</span><span class="sxs-lookup"><span data-stu-id="62cc4-365">The `OpQueue` class is designed to be inherited by the component that performs asynchronous work items.</span></span> <span data-ttu-id="62cc4-366">*Op \_ 型* 別範本參數是用來表示佇列中之工作專案的物件類型，在此案例中， *op \_ 類型* 會是 `SourceOp` 。</span><span class="sxs-lookup"><span data-stu-id="62cc4-366">The *OP\_TYPE* template parameter is the object type used to represent work items in the queue—in this case, *OP\_TYPE* will be `SourceOp`.</span></span> <span data-ttu-id="62cc4-367">`OpQueue`類別會執行下列方法：</span><span class="sxs-lookup"><span data-stu-id="62cc4-367">The `OpQueue` class implements the following methods:</span></span>

-   <span data-ttu-id="62cc4-368">`QueueOperation` 將新專案放在佇列上。</span><span class="sxs-lookup"><span data-stu-id="62cc4-368">`QueueOperation` puts a new item on the queue.</span></span>
-   <span data-ttu-id="62cc4-369">`ProcessQueue` 從佇列分派下一次作業。</span><span class="sxs-lookup"><span data-stu-id="62cc4-369">`ProcessQueue` dispatches the next operation from the queue.</span></span> <span data-ttu-id="62cc4-370">這個方法是非同步方法。</span><span class="sxs-lookup"><span data-stu-id="62cc4-370">This method is asynchronous.</span></span>
-   <span data-ttu-id="62cc4-371">`ProcessQueueAsync` 完成非同步 `ProcessQueue` 方法。</span><span class="sxs-lookup"><span data-stu-id="62cc4-371">`ProcessQueueAsync` completes the asynchronous `ProcessQueue` method.</span></span>

<span data-ttu-id="62cc4-372">另兩個方法必須由衍生類別來執行：</span><span class="sxs-lookup"><span data-stu-id="62cc4-372">Another two methods must be implemented by the derived class:</span></span>

-   <span data-ttu-id="62cc4-373">`ValidateOperation` 在指定媒體來源的目前狀態時，檢查是否有效，以執行指定的作業。</span><span class="sxs-lookup"><span data-stu-id="62cc4-373">`ValidateOperation` checks whether it is valid to perform a specified operation, given the current state of the media source.</span></span>
-   <span data-ttu-id="62cc4-374">`DispatchOperation` 執行非同步工作專案。</span><span class="sxs-lookup"><span data-stu-id="62cc4-374">`DispatchOperation` carries out the asynchronous work item.</span></span>

<span data-ttu-id="62cc4-375">作業佇列的使用方式如下：</span><span class="sxs-lookup"><span data-stu-id="62cc4-375">The operation queue is used as follows:</span></span>

1.  <span data-ttu-id="62cc4-376">媒體基礎管線會呼叫媒體來源上的非同步方法，例如 [**IMFMediaSource：： Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start)。</span><span class="sxs-lookup"><span data-stu-id="62cc4-376">The Media Foundation pipeline calls an asynchronous method on the media source, such as [**IMFMediaSource::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start).</span></span>
2.  <span data-ttu-id="62cc4-377">非同步方法會呼叫 `QueueOperation` ，這會將 [**開始**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) 作業放在佇列上，並 `ProcessQueue` 以物件) 的形式呼叫 (`SourceOp` 。</span><span class="sxs-lookup"><span data-stu-id="62cc4-377">The asynchronous method calls `QueueOperation`, which puts the [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) operation on the queue and calls `ProcessQueue` (in the form of a `SourceOp` object).</span></span>
3.  <span data-ttu-id="62cc4-378">`ProcessQueue` 呼叫 [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem)。</span><span class="sxs-lookup"><span data-stu-id="62cc4-378">`ProcessQueue` calls [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem).</span></span>
4.  <span data-ttu-id="62cc4-379">工作佇列執行緒會呼叫 `ProcessQueueAsync` 。</span><span class="sxs-lookup"><span data-stu-id="62cc4-379">The work-queue thread calls `ProcessQueueAsync`.</span></span>
5.  <span data-ttu-id="62cc4-380">`ProcessQueueAsync`方法會呼叫 `ValidateOperation` 和 `DispatchOperation` 。</span><span class="sxs-lookup"><span data-stu-id="62cc4-380">The `ProcessQueueAsync` method calls `ValidateOperation` and `DispatchOperation`.</span></span>

<span data-ttu-id="62cc4-381">下列程式碼會將 MPEG-2 來源上的新作業排入佇列：</span><span class="sxs-lookup"><span data-stu-id="62cc4-381">The following code queues a new operation on the MPEG-1 source:</span></span>


```C++
template <class OP_TYPE>
HRESULT OpQueue<OP_TYPE>::QueueOperation(OP_TYPE *pOp)
{
    HRESULT hr = S_OK;

    EnterCriticalSection(&m_critsec);

    hr = m_OpQueue.InsertBack(pOp);
    if (SUCCEEDED(hr))
    {
        hr = ProcessQueue();
    }

    LeaveCriticalSection(&m_critsec);
    return hr;
}
```



<span data-ttu-id="62cc4-382">下列程式碼會處理佇列：</span><span class="sxs-lookup"><span data-stu-id="62cc4-382">The following code processes the queue:</span></span>


```C++
template <class OP_TYPE>
HRESULT OpQueue<OP_TYPE>::ProcessQueue()
{
    HRESULT hr = S_OK;
    if (m_OpQueue.GetCount() > 0)
    {
        hr = MFPutWorkItem(
            MFASYNC_CALLBACK_QUEUE_STANDARD,    // Use the standard work queue.
            &m_OnProcessQueue,                  // Callback method.
            NULL                                // State object.
            );
    }
    return hr;
}
```



<span data-ttu-id="62cc4-383">`ValidateOperation`方法會檢查 mpeg-2 來源是否可以分派佇列中的下一項作業。</span><span class="sxs-lookup"><span data-stu-id="62cc4-383">The `ValidateOperation` method checks whether the MPEG-1 source can dispatch the next operation in the queue.</span></span> <span data-ttu-id="62cc4-384">如果另一個作業正在進行中，則會傳回 `ValidateOperation` **MF \_ E \_ NOTACCEPTING**。</span><span class="sxs-lookup"><span data-stu-id="62cc4-384">If another operation is in progress, `ValidateOperation` returns **MF\_E\_NOTACCEPTING**.</span></span> <span data-ttu-id="62cc4-385">這可確保 `DispatchOperation` 當另一個作業暫止時，不會呼叫。</span><span class="sxs-lookup"><span data-stu-id="62cc4-385">This ensures that `DispatchOperation` is not called while there is another operation pending.</span></span>


```C++
HRESULT MPEG1Source::ValidateOperation(SourceOp *pOp)
{
    if (m_pCurrentOp != NULL)
    {
        return MF_E_NOTACCEPTING;
    }
    return S_OK;
}
```



<span data-ttu-id="62cc4-386">DispatchOperation 方法會在作業類型上切換：</span><span class="sxs-lookup"><span data-stu-id="62cc4-386">The DispatchOperation method switches on the operation type:</span></span>


```C++
//-------------------------------------------------------------------
// DispatchOperation
//
// Performs the asynchronous operation indicated by pOp.
//
// NOTE:
// This method implements the pure-virtual OpQueue::DispatchOperation
// method. It is always called from a work-queue thread.
//-------------------------------------------------------------------

HRESULT MPEG1Source::DispatchOperation(SourceOp *pOp)
{
    EnterCriticalSection(&m_critSec);

    HRESULT hr = S_OK;

    if (m_state == STATE_SHUTDOWN)
    {
        LeaveCriticalSection(&m_critSec);

        return S_OK; // Already shut down, ignore the request.
    }

    switch (pOp->Op())
    {

    // IMFMediaSource methods:

    case SourceOp::OP_START:
        hr = DoStart((StartOp*)pOp);
        break;

    case SourceOp::OP_STOP:
        hr = DoStop(pOp);
        break;

    case SourceOp::OP_PAUSE:
        hr = DoPause(pOp);
        break;

    // Operations requested by the streams:

    case SourceOp::OP_REQUEST_DATA:
        hr = OnStreamRequestSample(pOp);
        break;

    case SourceOp::OP_END_OF_STREAM:
        hr = OnEndOfStream(pOp);
        break;

    default:
        hr = E_UNEXPECTED;
    }

    if (FAILED(hr))
    {
        StreamingError(hr);
    }

    LeaveCriticalSection(&m_critSec);
    return hr;
}
```



<span data-ttu-id="62cc4-387">總括來說：</span><span class="sxs-lookup"><span data-stu-id="62cc4-387">To summarize:</span></span>

1.  <span data-ttu-id="62cc4-388">管線會呼叫非同步方法，例如 [**IMFMediaSource：： Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start)。</span><span class="sxs-lookup"><span data-stu-id="62cc4-388">The pipeline calls an asynchronous method, such as [**IMFMediaSource::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start).</span></span>
2.  <span data-ttu-id="62cc4-389">非同步方法會呼叫 `OpQueue::QueueOperation` ，將指標傳入 `SourceOp` 物件。</span><span class="sxs-lookup"><span data-stu-id="62cc4-389">The asynchronous method calls `OpQueue::QueueOperation`, passing in a pointer to a `SourceOp` object.</span></span>
3.  <span data-ttu-id="62cc4-390">方法會將作業 `QueueOperation` 放在 *m \_ OpQueue* 佇列上，並呼叫 `OpQueue::ProcessQueue` 。</span><span class="sxs-lookup"><span data-stu-id="62cc4-390">The `QueueOperation` method puts the operation on the *m\_OpQueue* queue and calls `OpQueue::ProcessQueue`.</span></span>
4.  <span data-ttu-id="62cc4-391">`ProcessQueue`方法會呼叫 [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem)。</span><span class="sxs-lookup"><span data-stu-id="62cc4-391">The `ProcessQueue` method calls [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem).</span></span> <span data-ttu-id="62cc4-392">從此時開始，所有專案都會在媒體基礎的工作佇列執行緒上發生。</span><span class="sxs-lookup"><span data-stu-id="62cc4-392">From this point, everything happens on a Media Foundation work-queue thread.</span></span> <span data-ttu-id="62cc4-393">非同步方法會傳回給呼叫端。</span><span class="sxs-lookup"><span data-stu-id="62cc4-393">The asynchronous method returns to the caller.</span></span>
5.  <span data-ttu-id="62cc4-394">工作佇列執行緒會呼叫 `OpQueue::ProcessQueueAsync` 方法。</span><span class="sxs-lookup"><span data-stu-id="62cc4-394">The work-queue thread calls the `OpQueue::ProcessQueueAsync` method.</span></span>
6.  <span data-ttu-id="62cc4-395">`ProcessQueueAsync`方法會呼叫 `MPEG1Source:ValidateOperation` 以驗證作業。</span><span class="sxs-lookup"><span data-stu-id="62cc4-395">The `ProcessQueueAsync` method calls `MPEG1Source:ValidateOperation` to validate the operation.</span></span>
7.  <span data-ttu-id="62cc4-396">`ProcessQueueAsync`方法會呼叫 `MPEG1Source::DispatchOperation` 以處理作業。</span><span class="sxs-lookup"><span data-stu-id="62cc4-396">The `ProcessQueueAsync` method calls `MPEG1Source::DispatchOperation` to process the operation.</span></span>

<span data-ttu-id="62cc4-397">此設計有幾個優點：</span><span class="sxs-lookup"><span data-stu-id="62cc4-397">There are several benefits to this design:</span></span>

-   <span data-ttu-id="62cc4-398">方法是非同步，因此不會封鎖呼叫應用程式的執行緒。</span><span class="sxs-lookup"><span data-stu-id="62cc4-398">Methods are asynchronous, so they do not block the calling application's thread.</span></span>
-   <span data-ttu-id="62cc4-399">作業會分派在媒體基礎的工作佇列執行緒上，其會在管線元件之間共用。</span><span class="sxs-lookup"><span data-stu-id="62cc4-399">Operations are dispatched on a Media Foundation work-queue thread, which is shared among pipeline components.</span></span> <span data-ttu-id="62cc4-400">因此，媒體來源不會建立自己的執行緒，而會減少所建立的執行緒總數。</span><span class="sxs-lookup"><span data-stu-id="62cc4-400">Therefore, the media source does not create its own thread, reducing the total number of threads that are created.</span></span>
-   <span data-ttu-id="62cc4-401">等候作業完成時，媒體來源不會封鎖。</span><span class="sxs-lookup"><span data-stu-id="62cc4-401">The media source does not block while waiting for operations to complete.</span></span> <span data-ttu-id="62cc4-402">這樣可減少媒體來源意外造成鎖死的機率，並有助於減少內容切換。</span><span class="sxs-lookup"><span data-stu-id="62cc4-402">This reduces the chance that a media source will accidentally cause a deadlock, and helps to reduce context switching.</span></span>
-   <span data-ttu-id="62cc4-403">媒體來源可以使用非同步 i/o，藉由呼叫 [**IMFByteStream：： BeginRead**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-beginread)) 來讀取原始程式檔 (。</span><span class="sxs-lookup"><span data-stu-id="62cc4-403">The media source can use asynchronous I/O to read the source file (by calling [**IMFByteStream::BeginRead**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-beginread)).</span></span> <span data-ttu-id="62cc4-404">在等候 i/o 常式完成時，不需要封鎖媒體來源。</span><span class="sxs-lookup"><span data-stu-id="62cc4-404">The media source does not need to block while waiting for I/O routine complete.</span></span>

<span data-ttu-id="62cc4-405">如果您遵循 SDK 範例所示的模式，您可以將焦點放在媒體來源的特定詳細資料。</span><span class="sxs-lookup"><span data-stu-id="62cc4-405">If you follow the pattern shown in the SDK sample, you can focus on the particular details of your media source.</span></span>

## <a name="related-topics"></a><span data-ttu-id="62cc4-406">相關主題</span><span class="sxs-lookup"><span data-stu-id="62cc4-406">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="62cc4-407">媒體來源</span><span class="sxs-lookup"><span data-stu-id="62cc4-407">Media Sources</span></span>](media-sources.md)
</dt> <dt>

[<span data-ttu-id="62cc4-408">撰寫自訂媒體來源</span><span class="sxs-lookup"><span data-stu-id="62cc4-408">Writing a Custom Media Source</span></span>](writing-a-custom-media-source.md)
</dt> </dl>

 

 



