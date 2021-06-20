---
description: 使用此範例來瞭解在寫入轉換篩選時，RLE 編碼器可能會如何實作為此方法的一部分。
ms.assetid: b7d878ab-523f-4b52-b98d-c9d4fa18ce8a
title: 步驟 5。 轉換映射
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ac9d32e48ba438f8bde2d8d4d9aca3b827ebc0c
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406781"
---
# <a name="step-5-transform-the-image"></a><span data-ttu-id="f3f37-104">步驟 5。</span><span class="sxs-lookup"><span data-stu-id="f3f37-104">Step 5.</span></span> <span data-ttu-id="f3f37-105">轉換映射</span><span class="sxs-lookup"><span data-stu-id="f3f37-105">Transform the Image</span></span>

<span data-ttu-id="f3f37-106">這是 [撰寫轉換篩選](writing-transform-filters.md)之教學課程的步驟5。</span><span class="sxs-lookup"><span data-stu-id="f3f37-106">This is step 5 of the tutorial [Writing Transform Filters](writing-transform-filters.md).</span></span>

<span data-ttu-id="f3f37-107">上游篩選器會藉由在轉換篩選的輸入釘上呼叫 [**IMemInputPin：： Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) 方法，將媒體範例傳遞給轉換篩選。</span><span class="sxs-lookup"><span data-stu-id="f3f37-107">The upstream filter delivers media samples to the transform filter by calling the [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) method on the transform filter's input pin.</span></span> <span data-ttu-id="f3f37-108">若要處理資料，轉換篩選會呼叫 **轉換** 方法，這是單純的虛擬。</span><span class="sxs-lookup"><span data-stu-id="f3f37-108">To process the data, the transform filter calls the **Transform** method, which is pure virtual.</span></span> <span data-ttu-id="f3f37-109">**CTransformFilter** 和 **CTransInPlaceFilter** 類別會使用此方法的兩個不同版本：</span><span class="sxs-lookup"><span data-stu-id="f3f37-109">The **CTransformFilter** and **CTransInPlaceFilter** classes use two different versions of this method:</span></span>

-   <span data-ttu-id="f3f37-110">[**CTransformFilter：： Transform**](ctransformfilter-transform.md) 採用輸入範例的指標和輸出範例的指標。</span><span class="sxs-lookup"><span data-stu-id="f3f37-110">[**CTransformFilter::Transform**](ctransformfilter-transform.md) takes a pointer to the input sample and a pointer to the output sample.</span></span> <span data-ttu-id="f3f37-111">在篩選準則呼叫方法之前，它會將範例屬性從輸入範例複製到輸出範例（包括時間戳記）。</span><span class="sxs-lookup"><span data-stu-id="f3f37-111">Before the filter calls the method, it copies the sample properties from the input sample to the output sample, including the time stamps.</span></span>
-   <span data-ttu-id="f3f37-112">[**CTransInPlaceFilter：： Transform**](ctransinplacefilter-transform.md) 會取得輸入範例的指標。</span><span class="sxs-lookup"><span data-stu-id="f3f37-112">[**CTransInPlaceFilter::Transform**](ctransinplacefilter-transform.md) takes a pointer to the input sample.</span></span> <span data-ttu-id="f3f37-113">篩選準則會就地修改資料。</span><span class="sxs-lookup"><span data-stu-id="f3f37-113">The filter modifies the data in place.</span></span>

<span data-ttu-id="f3f37-114">如果 **轉換** 方法傳回 S \_ OK，則篩選準則會傳遞範例下游。</span><span class="sxs-lookup"><span data-stu-id="f3f37-114">If the **Transform** method returns S\_OK, the filter delivers the sample downstream.</span></span> <span data-ttu-id="f3f37-115">若要略過框架，請傳回 \_ FALSE。</span><span class="sxs-lookup"><span data-stu-id="f3f37-115">To skip a frame, return S\_FALSE.</span></span> <span data-ttu-id="f3f37-116">如果有資料流程錯誤，則傳回失敗碼。</span><span class="sxs-lookup"><span data-stu-id="f3f37-116">If there is a streaming error, return a failure code.</span></span>

<span data-ttu-id="f3f37-117">下列範例顯示 RLE 編碼器可能如何執行此方法。</span><span class="sxs-lookup"><span data-stu-id="f3f37-117">The following example shows how the RLE encoder might implement this method.</span></span> <span data-ttu-id="f3f37-118">視您的篩選準則而定，您自己的執行可能會有很大的差異。</span><span class="sxs-lookup"><span data-stu-id="f3f37-118">Your own implementation might differ considerably, depending on what your filter does.</span></span>


```C++
HRESULT CRleFilter::Transform(IMediaSample *pSource, IMediaSample *pDest)
{
    // Get pointers to the underlying buffers.
    BYTE *pBufferIn, *pBufferOut;
    hr = pSource->GetPointer(&pBufferIn);
    if (FAILED(hr))
    {
        return hr;
    }
    hr = pDest->GetPointer(&pBufferOut);
    if (FAILED(hr))
    {
        return hr;
    }
    // Process the data.
    DWORD cbDest = EncodeFrame(pBufferIn, pBufferOut);
    KASSERT((long)cbDest <= pDest->GetSize());

    pDest->SetActualDataLength(cbDest);
    pDest->SetSyncPoint(TRUE);
    return S_OK;
}
```



<span data-ttu-id="f3f37-119">此範例假設 EncodeFrame 是實作為 RLE 編碼的私用方法。</span><span class="sxs-lookup"><span data-stu-id="f3f37-119">This example assumes that EncodeFrame is a private method that implements the RLE encoding.</span></span> <span data-ttu-id="f3f37-120">此處未描述編碼演算法本身;如需詳細資訊，請參閱 Platform SDK 檔中的「點陣圖壓縮」主題。</span><span class="sxs-lookup"><span data-stu-id="f3f37-120">The encoding algorithm itself is not described here; for details, see the topic "Bitmap Compression" in the Platform SDK documentation.</span></span>

<span data-ttu-id="f3f37-121">首先，此範例會呼叫 [**IMediaSample：： GetPointer**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getpointer) 來取出基礎緩衝區的位址。</span><span class="sxs-lookup"><span data-stu-id="f3f37-121">First, the example calls [**IMediaSample::GetPointer**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getpointer) to retrieve the addresses of the underlying buffers.</span></span> <span data-ttu-id="f3f37-122">它會將這些傳遞給私用 EncoderFrame 方法。</span><span class="sxs-lookup"><span data-stu-id="f3f37-122">It passes these to the private EncoderFrame method.</span></span> <span data-ttu-id="f3f37-123">然後，它會呼叫 [**IMediaSample：： SetActualDataLength**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setactualdatalength) 來指定編碼資料的長度。</span><span class="sxs-lookup"><span data-stu-id="f3f37-123">Then it calls [**IMediaSample::SetActualDataLength**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setactualdatalength) to specify the length of the encoded data.</span></span> <span data-ttu-id="f3f37-124">下游篩選器需要此資訊，才能正確地管理緩衝區。</span><span class="sxs-lookup"><span data-stu-id="f3f37-124">The downstream filter needs this information so that it can manage the buffer properly.</span></span> <span data-ttu-id="f3f37-125">最後，此方法會呼叫 [**IMediaSample：： SetSyncPoint**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setsyncpoint) ，將主要畫面格旗標設定為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="f3f37-125">Finally, the method calls [**IMediaSample::SetSyncPoint**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setsyncpoint) to set the key frame flag to **TRUE**.</span></span> <span data-ttu-id="f3f37-126">執行時間長度的編碼不會使用任何差異框架，因此每個畫面格都是主要畫面格。</span><span class="sxs-lookup"><span data-stu-id="f3f37-126">Run-length encoding does not use any delta frames, so every frame is a key frame.</span></span> <span data-ttu-id="f3f37-127">若為 delta 框架，請將值設定為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="f3f37-127">For delta frames, set the value to **FALSE**.</span></span>

<span data-ttu-id="f3f37-128">您必須考慮的其他問題包括：</span><span class="sxs-lookup"><span data-stu-id="f3f37-128">Other issues that you must consider include:</span></span>

-   <span data-ttu-id="f3f37-129">時間戳記。</span><span class="sxs-lookup"><span data-stu-id="f3f37-129">Time stamps.</span></span> <span data-ttu-id="f3f37-130">**CTransformFilter** 類別會在呼叫 **轉換** 方法之前，先將輸出範例加上時間戳記。</span><span class="sxs-lookup"><span data-stu-id="f3f37-130">The **CTransformFilter** class timestamps the output sample before calling the **Transform** method.</span></span> <span data-ttu-id="f3f37-131">它會從輸入範例複製時間戳記值，而不加以修改。</span><span class="sxs-lookup"><span data-stu-id="f3f37-131">It copies the time stamp values from the input sample, without modifying them.</span></span> <span data-ttu-id="f3f37-132">如果您的篩選準則需要變更時間戳記，請在輸出範例上呼叫 [**IMediaSample：： SetTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-settime) 。</span><span class="sxs-lookup"><span data-stu-id="f3f37-132">If your filter needs to change the time stamps, call [**IMediaSample::SetTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-settime) on the output sample.</span></span>
-   <span data-ttu-id="f3f37-133">格式變更。</span><span class="sxs-lookup"><span data-stu-id="f3f37-133">Format changes.</span></span> <span data-ttu-id="f3f37-134">上游篩選器可以將媒體類型附加至範例，以變更中型串流的格式。</span><span class="sxs-lookup"><span data-stu-id="f3f37-134">The upstream filter can change formats mid-stream by attaching a media type to the sample.</span></span> <span data-ttu-id="f3f37-135">在這麼做之前，它會在您篩選的輸入 pin 上呼叫 [**IPin：： QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) 。</span><span class="sxs-lookup"><span data-stu-id="f3f37-135">Before doing so, it calls [**IPin::QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) on your filter's input pin.</span></span> <span data-ttu-id="f3f37-136">在 **CTransformFilter** 類別中，這會導致對 **CheckInputType** 的呼叫，後面接著 **CheckTransform**。</span><span class="sxs-lookup"><span data-stu-id="f3f37-136">In the **CTransformFilter** class, this results in a call to **CheckInputType** followed by **CheckTransform**.</span></span> <span data-ttu-id="f3f37-137">下游篩選也可以使用相同的機制來變更媒體類型。</span><span class="sxs-lookup"><span data-stu-id="f3f37-137">The downstream filter can also change media types, using the same mechanism.</span></span> <span data-ttu-id="f3f37-138">在您自己的篩選準則中，有兩件事要注意：</span><span class="sxs-lookup"><span data-stu-id="f3f37-138">In your own filter, there are two things to watch for:</span></span>

    -   <span data-ttu-id="f3f37-139">請確定 **QueryAccept** 不會傳回 false 接受。</span><span class="sxs-lookup"><span data-stu-id="f3f37-139">Make sure that **QueryAccept** does not return false acceptances.</span></span>
    -   <span data-ttu-id="f3f37-140">如果您的篩選準則接受格式變更，請呼叫 [**IMediaSample：： GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype)，在 **轉換** 方法內檢查這些變更。</span><span class="sxs-lookup"><span data-stu-id="f3f37-140">If your filter does accept format changes, check for them inside the **Transform** method by calling [**IMediaSample::GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype).</span></span> <span data-ttu-id="f3f37-141">如果該方法傳回 S \_ OK，則您的篩選準則必須回應格式變更。</span><span class="sxs-lookup"><span data-stu-id="f3f37-141">If that method returns S\_OK, your filter must respond to the format change.</span></span>

    <span data-ttu-id="f3f37-142">如需詳細資訊，請參閱 [動態格式變更](dynamic-format-changes.md)。</span><span class="sxs-lookup"><span data-stu-id="f3f37-142">For more information, see [Dynamic Format Changes](dynamic-format-changes.md).</span></span>

-   <span data-ttu-id="f3f37-143">執行緒。</span><span class="sxs-lookup"><span data-stu-id="f3f37-143">Threads.</span></span> <span data-ttu-id="f3f37-144">在 **CTransformFilter** 和 **CTransInPlaceFilter** 中，轉換篩選 **會在 Receive** 方法內同步傳遞輸出範例。</span><span class="sxs-lookup"><span data-stu-id="f3f37-144">In both **CTransformFilter** and **CTransInPlaceFilter**, the transform filter delivers output samples synchronously inside the **Receive** method.</span></span> <span data-ttu-id="f3f37-145">篩選不會建立任何背景工作執行緒來處理資料。</span><span class="sxs-lookup"><span data-stu-id="f3f37-145">The filter does not create any worker threads to process the data.</span></span> <span data-ttu-id="f3f37-146">通常，轉換篩選不會建立背景工作執行緒。</span><span class="sxs-lookup"><span data-stu-id="f3f37-146">Typically, there is no reason for a transform filter to create worker threads.</span></span>

<span data-ttu-id="f3f37-147">下一 [步：步驟6。新增對 COM 的支援](step-6--add-support-for-com.md)。</span><span class="sxs-lookup"><span data-stu-id="f3f37-147">Next: [Step 6. Add Support for COM](step-6--add-support-for-com.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f3f37-148">相關主題</span><span class="sxs-lookup"><span data-stu-id="f3f37-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f3f37-149">撰寫 DirectShow 篩選器</span><span class="sxs-lookup"><span data-stu-id="f3f37-149">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



