---
title: 設定檔案讀取的緩衝區
description: 設定檔案讀取的緩衝區
ms.assetid: da66ef5b-ec92-445c-90ba-5ee89e0def36
keywords:
- Windows Media Format SDK，讀取 ASF 檔案
- Advanced Systems Format (ASF) ，讀取檔案
- ASF (Advanced Systems Format) ，讀取檔案
- Windows Media Format SDK，配置緩衝區
- Advanced Systems Format (ASF) ，配置緩衝區
- ASF (Advanced Systems Format) ，配置緩衝區
- Advanced Systems Format (ASF) ，緩衝區配置
- ASF (Advanced 系統格式) ，緩衝區配置
- 緩衝區配置
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecdf9ba0a333bbe25c94ec087911237b68f38f74
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104374366"
---
# <a name="allocating-buffers-for-file-reading"></a><span data-ttu-id="f9d91-112">設定檔案讀取的緩衝區</span><span class="sxs-lookup"><span data-stu-id="f9d91-112">Allocating Buffers for File Reading</span></span>

<span data-ttu-id="f9d91-113">在最基本的檔案讀取案例中，用來傳遞範例的緩衝區是由讀取物件 (讀取器物件或同步讀取器物件) 所配置。</span><span class="sxs-lookup"><span data-stu-id="f9d91-113">In the most basic file-reading scenario, the buffers used to deliver samples are allocated by the reading object (the reader object or the synchronous reader object).</span></span> <span data-ttu-id="f9d91-114">不過，您可以自行配置緩衝區。</span><span class="sxs-lookup"><span data-stu-id="f9d91-114">You can, however, allocate buffers yourself.</span></span> <span data-ttu-id="f9d91-115">如需有關配置自己的緩衝區之優點的詳細資訊，請參閱使用者配置的 [範例支援](user-allocated-sample-support.md)。</span><span class="sxs-lookup"><span data-stu-id="f9d91-115">For more information about the benefits of allocating your own buffers, see [User Allocated Sample Support](user-allocated-sample-support.md).</span></span>

<span data-ttu-id="f9d91-116">若要使用您自己的緩衝區進行檔案讀取，請執行下列步驟。</span><span class="sxs-lookup"><span data-stu-id="f9d91-116">To use your own buffers for file reading, perform the following steps.</span></span>

1.  <span data-ttu-id="f9d91-117">針對讀取器執行回呼或回呼，以在需要緩衝區時呼叫。</span><span class="sxs-lookup"><span data-stu-id="f9d91-117">Implement a callback or callbacks for the reader to call when it needs a buffer.</span></span> <span data-ttu-id="f9d91-118">如果您正在讀取輸出範例，請使用 [**IWMReaderAllocatorEx：： AllocateForOutputEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderallocatorex-allocateforoutputex)。</span><span class="sxs-lookup"><span data-stu-id="f9d91-118">If you are reading output samples, use [**IWMReaderAllocatorEx::AllocateForOutputEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderallocatorex-allocateforoutputex).</span></span> <span data-ttu-id="f9d91-119">如果您正在讀取串流範例，請使用 [**IWMReaderAllocatorEx：： AllocateForStreamEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderallocatorex-allocateforstreamex)。</span><span class="sxs-lookup"><span data-stu-id="f9d91-119">If you are reading stream samples, use [**IWMReaderAllocatorEx::AllocateForStreamEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderallocatorex-allocateforstreamex).</span></span> <span data-ttu-id="f9d91-120">包含管理適合您應用程式之緩衝區的任何邏輯。</span><span class="sxs-lookup"><span data-stu-id="f9d91-120">Include whatever logic for managing buffers that suits your application.</span></span>
2.  <span data-ttu-id="f9d91-121">配置您將用於讀取檔案的緩衝區集區。</span><span class="sxs-lookup"><span data-stu-id="f9d91-121">Allocate a pool of buffers that you will use for file reading.</span></span>
    -   <span data-ttu-id="f9d91-122">藉由呼叫 [**IWMReaderAdvanced：： GetMaxOutputSampleSize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getmaxoutputsamplesize) 或 [**IWMReaderAdvanced：： GetMaxStreamSampleSize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getmaxstreamsamplesize) 來尋找緩衝區所使用的每個輸出和/或資料流程，以找出緩衝區所需的大小。</span><span class="sxs-lookup"><span data-stu-id="f9d91-122">Find the size required for your buffers by calling [**IWMReaderAdvanced::GetMaxOutputSampleSize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getmaxoutputsamplesize) or [**IWMReaderAdvanced::GetMaxStreamSampleSize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getmaxstreamsamplesize) for each output and/or stream for which the buffer is used.</span></span> <span data-ttu-id="f9d91-123">如果使用同步讀取器，請改用 [**IWMSyncReader：： GetMaxOutputSampleSize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getmaxoutputsamplesize) 或 [**IWMSyncReader：： GetMaxStreamSampleSize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getmaxstreamsamplesize) 。</span><span class="sxs-lookup"><span data-stu-id="f9d91-123">If using the synchronous reader, use [**IWMSyncReader::GetMaxOutputSampleSize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getmaxoutputsamplesize) or [**IWMSyncReader::GetMaxStreamSampleSize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getmaxstreamsamplesize) instead.</span></span>
    -   <span data-ttu-id="f9d91-124">建立集區的每個緩衝區。</span><span class="sxs-lookup"><span data-stu-id="f9d91-124">Create each buffer for the pool.</span></span>
3.  <span data-ttu-id="f9d91-125">設定讀取器或同步讀取器進行讀取。</span><span class="sxs-lookup"><span data-stu-id="f9d91-125">Set up the reader or synchronous reader for reading.</span></span> <span data-ttu-id="f9d91-126">如需詳細資訊，請參閱 [使用非同步讀取器讀取](reading-files-with-the-asynchronous-reader.md) 檔案，或 [使用同步讀取器讀取](reading-files-with-the-synchronous-reader.md)檔案。</span><span class="sxs-lookup"><span data-stu-id="f9d91-126">For more information see [Reading Files with the Asynchronous Reader](reading-files-with-the-asynchronous-reader.md) or [Reading Files with the Synchronous Reader](reading-files-with-the-synchronous-reader.md).</span></span>
4.  <span data-ttu-id="f9d91-127">開始撰寫之前，請針對您要使用 reader 物件配置緩衝區的每個輸出和資料流程，呼叫 [**IWMReaderAdvanced：： SetAllocateForOutput**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setallocateforoutput) 或 [**IWMReaderAdvanced：： SetAllocateForStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setallocateforstream) 。</span><span class="sxs-lookup"><span data-stu-id="f9d91-127">Before beginning writing, call [**IWMReaderAdvanced::SetAllocateForOutput**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setallocateforoutput) or [**IWMReaderAdvanced::SetAllocateForStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setallocateforstream) for each output and stream for which you are allocating buffers using the reader object.</span></span> <span data-ttu-id="f9d91-128">若為同步讀取器，請改為呼叫 [**IWMSyncReader2：： SetAllocateForOutput**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader2-setallocateforoutput) 或 [**IWMSyncReader2：： SetAllocateForStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader2-setallocateforstream) 。</span><span class="sxs-lookup"><span data-stu-id="f9d91-128">For the synchronous reader, call [**IWMSyncReader2::SetAllocateForOutput**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader2-setallocateforoutput) or [**IWMSyncReader2::SetAllocateForStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader2-setallocateforstream) instead.</span></span>
5.  <span data-ttu-id="f9d91-129">開始讀取檔案。</span><span class="sxs-lookup"><span data-stu-id="f9d91-129">Begin reading the file.</span></span>

<span data-ttu-id="f9d91-130">讀取物件將會呼叫適當的配置器回呼，並從您的應用程式取得範例。</span><span class="sxs-lookup"><span data-stu-id="f9d91-130">The reading object will make calls to the appropriate allocator callback and get samples from your application.</span></span> <span data-ttu-id="f9d91-131">您的緩衝區管理邏輯必須包含一個方法，告知緩衝區可自由使用。</span><span class="sxs-lookup"><span data-stu-id="f9d91-131">Your buffer management logic must include a way to signal that a buffer is free to be used again.</span></span> <span data-ttu-id="f9d91-132">一般來說，當轉譯其內容時，會將緩衝區放回集區。</span><span class="sxs-lookup"><span data-stu-id="f9d91-132">Typically, a buffer is put back into the pool when its contents are rendered.</span></span> <span data-ttu-id="f9d91-133">視您的應用程式而定，您可能只需要在集區中有幾個緩衝區，或多個緩衝區。</span><span class="sxs-lookup"><span data-stu-id="f9d91-133">Depending upon your application, you may need just a few buffers in the pool or many.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f9d91-134">相關主題</span><span class="sxs-lookup"><span data-stu-id="f9d91-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f9d91-135">**讀取 ASF 檔案**</span><span class="sxs-lookup"><span data-stu-id="f9d91-135">**Reading ASF Files**</span></span>](reading-asf-files.md)
</dt> </dl>

 

 




