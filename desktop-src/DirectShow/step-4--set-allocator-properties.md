---
description: 將配置器屬性設定為寫入轉換篩選的一部分。 轉換篩選器的輸出釘選會選取下游配置器。
ms.assetid: c2fd6d8b-b239-45e4-9c02-41edafa58762
title: 步驟 4： 設定配置器屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9ee7d9ecdc85b63ec6bd774a3a47e0e9399dcf3
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406821"
---
# <a name="step-4-set-allocator-properties"></a><span data-ttu-id="378c4-105">步驟 4：</span><span class="sxs-lookup"><span data-stu-id="378c4-105">Step 4.</span></span> <span data-ttu-id="378c4-106">設定配置器屬性</span><span class="sxs-lookup"><span data-stu-id="378c4-106">Set Allocator Properties</span></span>

<span data-ttu-id="378c4-107">這是 [撰寫轉換篩選](writing-transform-filters.md)之教學課程的步驟4。</span><span class="sxs-lookup"><span data-stu-id="378c4-107">This is step 4 of the tutorial [Writing Transform Filters](writing-transform-filters.md).</span></span>

> [!Note]  
> <span data-ttu-id="378c4-108">衍生自 **CTransInPlaceFilter** 的篩選不需要此步驟。</span><span class="sxs-lookup"><span data-stu-id="378c4-108">This step is not required for filters that derive from **CTransInPlaceFilter**.</span></span>

 

<span data-ttu-id="378c4-109">在兩個 pin 在媒體類型上同意之後，他們會選取連接的配置器和協調配置器屬性，例如緩衝區大小和緩衝區數目。</span><span class="sxs-lookup"><span data-stu-id="378c4-109">After two pins agree on a media type, they select an allocator for the connection and negotiate allocator properties, such as the buffer size and the number of buffers.</span></span>

<span data-ttu-id="378c4-110">在 **CTransformFilter** 類別中，有兩個配置器，一個用於上游連線，另一個用於下游連接。</span><span class="sxs-lookup"><span data-stu-id="378c4-110">In the **CTransformFilter** class, there are two allocators, one for the upstream pin connection and one for the downstream pin connection.</span></span> <span data-ttu-id="378c4-111">上游篩選器會選取上游配置器，也會選擇配置器屬性。</span><span class="sxs-lookup"><span data-stu-id="378c4-111">The upstream filter selects the upstream allocator and also chooses the allocator properties.</span></span> <span data-ttu-id="378c4-112">輸入 pin 會接受上游篩選器所決定的任何內容。</span><span class="sxs-lookup"><span data-stu-id="378c4-112">The input pin accepts whatever the upstream filter decides.</span></span> <span data-ttu-id="378c4-113">如果您需要修改此行為，請覆寫 [**CBaseInputPin：： NotifyAllocator**](cbaseinputpin-notifyallocator.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="378c4-113">If you need to modify this behavior, override the [**CBaseInputPin::NotifyAllocator**](cbaseinputpin-notifyallocator.md) method.</span></span>

<span data-ttu-id="378c4-114">轉換篩選器的輸出釘選會選取下游配置器。</span><span class="sxs-lookup"><span data-stu-id="378c4-114">The transform filter's output pin selects the downstream allocator.</span></span> <span data-ttu-id="378c4-115">它會執行下列步驟：</span><span class="sxs-lookup"><span data-stu-id="378c4-115">It performs the following steps:</span></span>

1.  <span data-ttu-id="378c4-116">如果下游篩選器可以提供配置器，則輸出 pin 會使用該配置器。</span><span class="sxs-lookup"><span data-stu-id="378c4-116">If the downstream filter can provide an allocator, the output pin uses that one.</span></span> <span data-ttu-id="378c4-117">否則，輸出 pin 會建立新的配置器。</span><span class="sxs-lookup"><span data-stu-id="378c4-117">Otherwise, the output pin creates a new allocator.</span></span>
2.  <span data-ttu-id="378c4-118">如果任何) 呼叫 [**IMemInputPin：： GetAllocatorRequirements**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocatorrequirements)，輸出釘選會取得下游篩選器的配置器需求 (。</span><span class="sxs-lookup"><span data-stu-id="378c4-118">The output pin gets the downstream filter's allocator requirements (if any) by calling [**IMemInputPin::GetAllocatorRequirements**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocatorrequirements).</span></span>
3.  <span data-ttu-id="378c4-119">輸出圖釘會呼叫轉換篩選器的 [**CTransformFilter：:D ecidebuffersize**](ctransformfilter-decidebuffersize.md) 方法，這是純虛擬的方法。</span><span class="sxs-lookup"><span data-stu-id="378c4-119">The output pin calls the transform filter's [**CTransformFilter::DecideBufferSize**](ctransformfilter-decidebuffersize.md) method, which is pure virtual.</span></span> <span data-ttu-id="378c4-120">此方法的參數是配置器的指標，以及具有下游篩選準則需求的配置器 [**\_ 屬性**](/windows/win32/api/strmif/ns-strmif-allocator_properties) 結構。</span><span class="sxs-lookup"><span data-stu-id="378c4-120">The parameters to this method are a pointer to the allocator and an [**ALLOCATOR\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) structure with the downstream filter's requirements.</span></span> <span data-ttu-id="378c4-121">如果下游篩選器沒有配置器需求，則會將結構清空。</span><span class="sxs-lookup"><span data-stu-id="378c4-121">If the downstream filter has no allocator requirements, the structure is zeroed out.</span></span>
4.  <span data-ttu-id="378c4-122">在 **DecideBufferSize** 方法中，衍生類別會藉由呼叫 [**IMemAllocator：： SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-setproperties)來設定配置器屬性。</span><span class="sxs-lookup"><span data-stu-id="378c4-122">In the **DecideBufferSize** method, the derived class sets the allocator properties by calling [**IMemAllocator::SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-setproperties).</span></span>

<span data-ttu-id="378c4-123">一般而言，衍生的類別會根據輸出格式、下游篩選準則的需求，以及篩選準則本身的需求，來選取配置器屬性。</span><span class="sxs-lookup"><span data-stu-id="378c4-123">Generally, the derived class will select allocator properties based on the output format, the downstream filter's requirements, and the filter's own requirements.</span></span> <span data-ttu-id="378c4-124">請嘗試選取與下游篩選器要求相容的屬性。</span><span class="sxs-lookup"><span data-stu-id="378c4-124">Try to select properties that are compatible with the downstream filter's request.</span></span> <span data-ttu-id="378c4-125">否則，下游篩選可能會拒絕連接。</span><span class="sxs-lookup"><span data-stu-id="378c4-125">Otherwise, the downstream filter might reject the connection.</span></span>

<span data-ttu-id="378c4-126">在下列範例中，RLE 編碼器會設定緩衝區大小、緩衝區對齊和緩衝區計數的最小值。</span><span class="sxs-lookup"><span data-stu-id="378c4-126">In the following example, the RLE encoder sets minimum values for the buffer size, buffer alignment, and buffer count.</span></span> <span data-ttu-id="378c4-127">針對前置詞，它會使用下游篩選要求的任何值。</span><span class="sxs-lookup"><span data-stu-id="378c4-127">For the prefix, it uses whatever value the downstream filter requested.</span></span> <span data-ttu-id="378c4-128">前置詞通常是零個位元組，但有些篩選器需要它。</span><span class="sxs-lookup"><span data-stu-id="378c4-128">The prefix is typically zero bytes, but some filters require it.</span></span> <span data-ttu-id="378c4-129">例如， [AVI Mux](avi-mux-filter.md) 篩選器會使用前置詞來寫入 RIFF 標頭。</span><span class="sxs-lookup"><span data-stu-id="378c4-129">For example, the [AVI Mux](avi-mux-filter.md) filter uses the prefix to write RIFF headers.</span></span>


```C++
HRESULT CRleFilter::DecideBufferSize(
    IMemAllocator *pAlloc, ALLOCATOR_PROPERTIES *pProp)
{
    AM_MEDIA_TYPE mt;
    HRESULT hr = m_pOutput->ConnectionMediaType(&mt);
    if (FAILED(hr))
    {
        return hr;
    }

    ASSERT(mt.formattype == FORMAT_VideoInfo);
    BITMAPINFOHEADER *pbmi = HEADER(mt.pbFormat);
    pProp->cbBuffer = DIBSIZE(*pbmi) * 2; 
    if (pProp->cbAlign == 0)
    {
        pProp->cbAlign = 1;
    }
    if (pProp->cBuffers == 0)
    {
        pProp->cBuffers = 1;
    }
    // Release the format block.
    FreeMediaType(mt);

    // Set allocator properties.
    ALLOCATOR_PROPERTIES Actual;
    hr = pAlloc->SetProperties(pProp, &Actual);
    if (FAILED(hr)) 
    {
        return hr;
    }
    // Even when it succeeds, check the actual result.
    if (pProp->cbBuffer > Actual.cbBuffer) 
    {
        return E_FAIL;
    }
    return S_OK;
}
```



<span data-ttu-id="378c4-130">配置器可能無法完全符合您的要求。</span><span class="sxs-lookup"><span data-stu-id="378c4-130">The allocator may not be able to match your request exactly.</span></span> <span data-ttu-id="378c4-131">因此， **SetProperties** 方法會以個別的配置器 **\_ 屬性** 結構傳回實際的結果， () 上一個範例中的 *實際* 參數。</span><span class="sxs-lookup"><span data-stu-id="378c4-131">Therefore, the **SetProperties** method returns the actual result in a separate **ALLOCATOR\_PROPERTIES** structure (the *Actual* parameter, in the previous example).</span></span> <span data-ttu-id="378c4-132">即使在 **SetProperties** 成功時，您也應該檢查結果，以確定它們符合您篩選準則的最低需求。</span><span class="sxs-lookup"><span data-stu-id="378c4-132">Even when **SetProperties** succeeds, you should check the result to make sure they meet your filter's minimum requirements.</span></span>

<span data-ttu-id="378c4-133">**自訂配置器**</span><span class="sxs-lookup"><span data-stu-id="378c4-133">**Custom Allocators**</span></span>

<span data-ttu-id="378c4-134">根據預設，所有篩選準則類別都會使用 [**CMemAllocator**](cmemallocator.md) 類別進行其配置器。</span><span class="sxs-lookup"><span data-stu-id="378c4-134">By default, all of the filter classes use the [**CMemAllocator**](cmemallocator.md) class for their allocators.</span></span> <span data-ttu-id="378c4-135">這個類別會使用 **VirtualAlloc**) ，從用戶端進程的虛擬位址空間配置記憶體 (。</span><span class="sxs-lookup"><span data-stu-id="378c4-135">This class allocates memory from the virtual address space of the client process (using **VirtualAlloc**).</span></span> <span data-ttu-id="378c4-136">如果您的篩選準則需要使用其他種類的記憶體（例如 DirectDraw 表面），您可以執行自訂配置器。</span><span class="sxs-lookup"><span data-stu-id="378c4-136">If your filter needs to use some other kind of memory, such as DirectDraw surfaces, you can implement a custom allocator.</span></span> <span data-ttu-id="378c4-137">您可以使用 [**CBaseAllocator**](cbaseallocator.md) 類別，或是撰寫全新的配置器類別。</span><span class="sxs-lookup"><span data-stu-id="378c4-137">You can use the [**CBaseAllocator**](cbaseallocator.md) class or write an entirely new allocator class.</span></span> <span data-ttu-id="378c4-138">如果您的篩選準則有自訂配置器，請根據使用配置器的 pin 碼覆寫下列方法：</span><span class="sxs-lookup"><span data-stu-id="378c4-138">If your filter has a custom allocator, override the following methods, depending on which pin uses the allocator:</span></span>

-   <span data-ttu-id="378c4-139">輸入 pin： [**CBaseInputPin：： GetAllocator**](cbaseinputpin-getallocator.md) 和 [**CBaseInputPin：： NotifyAllocator**](cbaseinputpin-notifyallocator.md)。</span><span class="sxs-lookup"><span data-stu-id="378c4-139">Input pin: [**CBaseInputPin::GetAllocator**](cbaseinputpin-getallocator.md) and [**CBaseInputPin::NotifyAllocator**](cbaseinputpin-notifyallocator.md).</span></span>
-   <span data-ttu-id="378c4-140">輸出 pin： [**CBaseOutputPin：:D ecideallocator**](cbaseoutputpin-decideallocator.md)。</span><span class="sxs-lookup"><span data-stu-id="378c4-140">Output pin: [**CBaseOutputPin::DecideAllocator**](cbaseoutputpin-decideallocator.md).</span></span>

<span data-ttu-id="378c4-141">如果另一個篩選器拒絕使用您的自訂配置器進行連線，則您的篩選器可能會使連接失敗，或其他篩選器的配置器。</span><span class="sxs-lookup"><span data-stu-id="378c4-141">If the other filter refuses to connect using your custom allocator, your filter can either fail the connection, or else connect with the other filter's allocator.</span></span> <span data-ttu-id="378c4-142">在後者的情況下，您可能需要設定一個指示配置器類型的內部旗標。</span><span class="sxs-lookup"><span data-stu-id="378c4-142">In the latter case, you might need to set an internal flag indicating the type of allocator.</span></span> <span data-ttu-id="378c4-143">如需此方法的範例，請參閱 [**CDrawImage 類別**](cdrawimage.md)。</span><span class="sxs-lookup"><span data-stu-id="378c4-143">For an example of this approach, see [**CDrawImage Class**](cdrawimage.md).</span></span>

<span data-ttu-id="378c4-144">下一 [步：步驟5。轉換映射](step-5--transform-the-image.md)。</span><span class="sxs-lookup"><span data-stu-id="378c4-144">Next: [Step 5. Transform the Image](step-5--transform-the-image.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="378c4-145">相關主題</span><span class="sxs-lookup"><span data-stu-id="378c4-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="378c4-146">撰寫 DirectShow 篩選器</span><span class="sxs-lookup"><span data-stu-id="378c4-146">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



