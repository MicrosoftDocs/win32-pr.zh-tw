---
description: 'QueryAccept (上游) '
ms.assetid: 3153e3a4-2227-4fdd-b2b0-218763013d2d
title: 'QueryAccept (上游) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7707c52d36c3d065c4a7277939f724aabdb73e46
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103688224"
---
# <a name="queryaccept-upstream"></a><span data-ttu-id="46330-103">QueryAccept (上游) </span><span class="sxs-lookup"><span data-stu-id="46330-103">QueryAccept (Upstream)</span></span>

<span data-ttu-id="46330-104">這種機制可讓輸入的 pin 提議對其上游對等的格式變更。</span><span class="sxs-lookup"><span data-stu-id="46330-104">This mechanism enables an input pin to propose a format change to its upstream peer.</span></span> <span data-ttu-id="46330-105">下游篩選器必須將媒體類型附加至上游篩選器在下一次呼叫 [**IMemAllocator：： GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer)時取得的範例。</span><span class="sxs-lookup"><span data-stu-id="46330-105">The downstream filter must attach a media type to the sample that the upstream filter will obtain in its next call to [**IMemAllocator::GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer).</span></span> <span data-ttu-id="46330-106">不過，若要這樣做，下游篩選器必須提供連接的自訂配置器。</span><span class="sxs-lookup"><span data-stu-id="46330-106">In order to do this, however, the downstream filter must provide a custom allocator for the connection.</span></span> <span data-ttu-id="46330-107">此配置器必須執行下游篩選器可在下一個範例中用來設定媒體類型的私用方法。</span><span class="sxs-lookup"><span data-stu-id="46330-107">This allocator must implement a private method that the downstream filter can use to set the media type on the next sample.</span></span>

<span data-ttu-id="46330-108">會進行下列步驟：</span><span class="sxs-lookup"><span data-stu-id="46330-108">The following steps occur:</span></span>

1.  <span data-ttu-id="46330-109">下游篩選器會檢查 pin 連接是否使用篩選器的自訂配置器。</span><span class="sxs-lookup"><span data-stu-id="46330-109">The downstream filter checks whether the pin connection uses the filter's custom allocator.</span></span> <span data-ttu-id="46330-110">如果上游篩選準則擁有配置器，下游篩選器將無法變更格式。</span><span class="sxs-lookup"><span data-stu-id="46330-110">If the upstream filter owns the allocator, the downstream filter cannot change the format.</span></span>
2.  <span data-ttu-id="46330-111">下游篩選器會在上游輸出 pin 上呼叫 [**IPin：： QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) (請參閱圖、步驟 A) 。</span><span class="sxs-lookup"><span data-stu-id="46330-111">The downstream filter calls [**IPin::QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) on the upstream output pin (see illustration, step A).</span></span>
3.  <span data-ttu-id="46330-112">如果傳回 `QueryAccept` S \_ ，下游篩選器會在其配置器上呼叫私用方法，以便設定媒體類型。</span><span class="sxs-lookup"><span data-stu-id="46330-112">If `QueryAccept` returns S\_OK, the downstream filter calls the private method on its allocator in order to set the media type.</span></span> <span data-ttu-id="46330-113">在此私用方法中，配置器會在下一個可用的範例 (B) 上呼叫 [**IMediaSample：： SetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatype) 。</span><span class="sxs-lookup"><span data-stu-id="46330-113">Within this private method, the allocator calls [**IMediaSample::SetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatype) on the next available sample (B).</span></span>
4.  <span data-ttu-id="46330-114">上游篩選準則會呼叫 **GetBuffer** 以取得新的 (C) 和 [**IMediaSample：： GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype) 範例，以取得 (D) 的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="46330-114">The upstream filter calls **GetBuffer** to get a new sample (C) and [**IMediaSample::GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype) to get the media type (D).</span></span>
5.  <span data-ttu-id="46330-115">當上游篩選器傳遞範例時，它應該將媒體類型附加至該範例。</span><span class="sxs-lookup"><span data-stu-id="46330-115">When the upstream filter delivers the sample, it should leave the media type attached to that sample.</span></span> <span data-ttu-id="46330-116">如此一來，下游篩選可以確認媒體類型已 (E) 變更。</span><span class="sxs-lookup"><span data-stu-id="46330-116">That way, the downstream filter can confirm that the media type has changed (E).</span></span>

<span data-ttu-id="46330-117">如果上游篩選器接受格式變更，它也必須能夠切換回原始媒體類型，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="46330-117">If the upstream filter accepts the format change, it must also be able to switch back to the original media type, as shown in the following diagram.</span></span>

![queryaccept (上游) ](images/dynformat4.png)

<span data-ttu-id="46330-119">這種格式變更的主要範例包括 DirectShow 影片轉譯器。</span><span class="sxs-lookup"><span data-stu-id="46330-119">The main examples of this kind of format change involve the DirectShow video renderers.</span></span>

-   <span data-ttu-id="46330-120">原始的 [影片](video-renderer-filter.md) 轉譯器篩選器可以在串流期間于 RGB 和 YUV 類型之間切換。</span><span class="sxs-lookup"><span data-stu-id="46330-120">The original [Video Renderer](video-renderer-filter.md) filter can switch between RGB and YUV types during streaming.</span></span> <span data-ttu-id="46330-121">當篩選連接時，需要符合目前顯示設定的 RGB 格式。</span><span class="sxs-lookup"><span data-stu-id="46330-121">When the filter connects, it requires an RGB format that matches the current display settings.</span></span> <span data-ttu-id="46330-122">這可保證在需要的情況下，可以切換回 GDI。</span><span class="sxs-lookup"><span data-stu-id="46330-122">This guarantees that it can fall back on GDI if it needs to.</span></span> <span data-ttu-id="46330-123">串流處理開始之後，如果有 DirectDraw 可用，則影片轉譯器會要求使用 YUV 類型的格式變更。</span><span class="sxs-lookup"><span data-stu-id="46330-123">After streaming begins, if DirectDraw is available, the Video Renderer requests a format change to a YUV type.</span></span> <span data-ttu-id="46330-124">之後，如果有任何原因，它可能會切換回 RGB。</span><span class="sxs-lookup"><span data-stu-id="46330-124">Later, it might switch back to RGB if it loses the DirectDraw surface for any reason.</span></span>
-   <span data-ttu-id="46330-125">較新的影片混合轉譯器 (VMR) 篩選器會以圖形硬體支援的任何格式（包括 YUV 類型）進行連接。</span><span class="sxs-lookup"><span data-stu-id="46330-125">The newer Video Mixing Renderer (VMR) filter will connect with any format that is supported by the graphics hardware, including YUV types.</span></span> <span data-ttu-id="46330-126">不過，圖形硬體可能會變更基礎 DirectDraw 表面的 stride，以將效能優化。</span><span class="sxs-lookup"><span data-stu-id="46330-126">However, the graphics hardware might change the stride of the underlying DirectDraw surface in order to optimize performance.</span></span> <span data-ttu-id="46330-127">VMR 篩選器 `QueryAccept` 會使用來報告新的 stride，這是在 **BITMAPINFOHEADER** 結構的 **biWidth** 成員中指定的。</span><span class="sxs-lookup"><span data-stu-id="46330-127">The VMR filter uses `QueryAccept` to report the new stride, which is specified in the **biWidth** member of the **BITMAPINFOHEADER** structure.</span></span> <span data-ttu-id="46330-128">**VIDEOINFOHEADER** 或 **VIDEOINFOHEADER2** 結構中的來源和目標矩形會識別應該將影片解碼的區域。</span><span class="sxs-lookup"><span data-stu-id="46330-128">The source and target rectangles in the **VIDEOINFOHEADER** or **VIDEOINFOHEADER2** structure identify the region where the video should be decoded.</span></span>

<span data-ttu-id="46330-129">**執行附注**</span><span class="sxs-lookup"><span data-stu-id="46330-129">**Implementation Note**</span></span>

<span data-ttu-id="46330-130">您不太可能會撰寫需要要求上游格式變更的篩選準則，因為這主要是影片轉譯器的一項功能。</span><span class="sxs-lookup"><span data-stu-id="46330-130">It is unlikely that you will write a filter that needs to request upstream format changes, since this is mainly a feature of video renderers.</span></span> <span data-ttu-id="46330-131">但是，如果您撰寫影片轉換篩選或影片解碼，您的篩選器必須正確地回應來自影片轉譯器的要求。</span><span class="sxs-lookup"><span data-stu-id="46330-131">However, if you write a video transform filter or a video decoder, your filter must respond correctly to requests from the video renderer.</span></span>

<span data-ttu-id="46330-132">位於影片轉譯器與解碼器之間的就地篩選應傳遞所有 `QueryAccept` 上游的呼叫。</span><span class="sxs-lookup"><span data-stu-id="46330-132">A trans-in-place filter that sits between the video renderer and the decoder should pass all `QueryAccept` calls upstream.</span></span> <span data-ttu-id="46330-133">儲存新的格式資訊。</span><span class="sxs-lookup"><span data-stu-id="46330-133">Store the new format information when it arrives.</span></span>

<span data-ttu-id="46330-134">複製轉換篩選 (也就是說，非就地篩選) 應該執行下列其中一種行為：</span><span class="sxs-lookup"><span data-stu-id="46330-134">A copy-transform filter (that is, a non-trans-in-place filter) should implement one of the following behaviors:</span></span>

-   <span data-ttu-id="46330-135">在上游傳遞格式變更，並在到達時儲存新的格式資訊。</span><span class="sxs-lookup"><span data-stu-id="46330-135">Pass format changes upstream and store the new format information when it arrives.</span></span> <span data-ttu-id="46330-136">您的篩選準則必須使用自訂配置器，才能將格式附加至上游範例。</span><span class="sxs-lookup"><span data-stu-id="46330-136">Your filter must use a custom allocator so that it can attach the format to the upstream sample.</span></span>
-   <span data-ttu-id="46330-137">在篩選內執行格式轉換。</span><span class="sxs-lookup"><span data-stu-id="46330-137">Perform the format conversion inside the filter.</span></span> <span data-ttu-id="46330-138">這可能比傳遞格式變更上游更容易。</span><span class="sxs-lookup"><span data-stu-id="46330-138">This is probably easier than passing the format change upstream.</span></span> <span data-ttu-id="46330-139">不過，它可能會比讓解碼器篩選器解碼成正確的格式更有效率。</span><span class="sxs-lookup"><span data-stu-id="46330-139">However, it might be less efficient than letting the decoder filter decode into the correct format.</span></span>
-   <span data-ttu-id="46330-140">最後的手段是拒絕格式變更。</span><span class="sxs-lookup"><span data-stu-id="46330-140">As a last resort, simply reject the format change.</span></span> <span data-ttu-id="46330-141"> (需詳細資訊，請參閱 DirectShow 基類庫中的 [**CTransInPlaceOutputPin：： CheckMediaType**](ctransinplaceoutputpin-checkmediatype.md) 方法的原始程式碼。 ) 拒絕格式變更可能會降低效能，因為它會防止影片轉譯器使用最有效率的格式。</span><span class="sxs-lookup"><span data-stu-id="46330-141">(For more information, refer to the source code for the [**CTransInPlaceOutputPin::CheckMediaType**](ctransinplaceoutputpin-checkmediatype.md) method in the DirectShow base class library.) Rejecting a format change can reduce performance, however, because it prevents the video renderer from using the most efficient format.</span></span>

<span data-ttu-id="46330-142">下列虛擬程式碼示範如何執行複製轉換篩選 (衍生自可在 YUV 和 RGB 輸出類型之間切換的 **CTransformFilter**) 。</span><span class="sxs-lookup"><span data-stu-id="46330-142">The following pseudo-code shows how you might implement a copy-transform filter (derived from **CTransformFilter**) that can switch between YUV and RGB output types.</span></span> <span data-ttu-id="46330-143">此範例假設篩選本身會進行轉換，而不是傳遞格式變更上游。</span><span class="sxs-lookup"><span data-stu-id="46330-143">This example assumes that the filter does the conversion itself, rather than passing the format change upstream.</span></span>


```C++
HRESULT CMyTransform::CheckInputType(const CMediaType *pmt)
{
    if (pmt is a YUV type that you support) {
        return S_OK;
    }
    else {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }
}

HRESULT CMyTransform::CheckTransform(
    const CMediaType *mtIn, const CMediaType *mtOut)
{
    if (mtOut is a YUV or RGB type that you support)
    {
        if ((mtIn has the same video dimensions as mtOut) &&
            (you support the mtIn-to-mtOut transform))
        {
            return S_OK;
        }
    }
    // otherwise
    return VFW_E_TYPE_NOT_ACCEPTED;
}

// GetMediaType: Return a preferred output type.
HRESULT CMyTransform::GetMediaType(int iPosition, CMediaType *pMediaType)
{
    if (iPosition < 0) {
        return E_INVALIDARG;
    }
    switch (iPosition)
    {
    case 0:
        Copy the input type (YUV) to pMediaType
        return S_OK;
    case 1:
        Construct an RGB type that matches the input type.
        return S_OK;
    default:
        return VFW_S_NO_MORE_ITEMS;
    }
}

// SetMediaType: Override from CTransformFilter. 
HRESULT CMyTransform::SetMediaType(
    PIN_DIRECTION direction, const CMediaType *pmt)
{
    // Capture this information...
    if (direction == PINDIR_OUTPUT)
    {
       m_bYuv = (pmt->subtype == MEDIASUBTYPE_UYVY);
    }
    return S_OK;
}

HRESULT CMyTransform::Transform(
    IMediaSample *pSource, IMediaSample *pDest)
{
    // Look for format changes from downstream.
    CMediaType *pMT = NULL;
    HRESULT hr = pDest->GetMediaType((AM_MEDIA_TYPE**)&pMT);
    if (hr == S_OK)
    {
        hr = m_pOutput->CheckMediaType(pMT);
        if(FAILED(hr))
        {
            DeleteMediaType(pMT);
            return E_FAIL;
        }
        // Notify our own output pin about the new type.
        m_pOutput->SetMediaType(pMT);
        DeleteMediaType(pMT);
    }
    // Process the buffers
    if (m_bYuv) {
        return ProcessFrameYUV(pSource, pDest);
    }
    else {
        return ProcessFrameRGB(pSource, pDest);
    }
}
```



 

 



