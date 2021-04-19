---
description: 範例捕獲篩選器可讓您在範例通過篩選圖形時，取得範例。
ms.assetid: 3c2fb52f-2b44-449a-ae96-3cf35a0a401d
title: " (Qedit 的範例捕獲篩選) "
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Sample
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: 18cedd24b0ddcb8f71373641905228f8252ae4ef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995192"
---
# <a name="sample-grabber-filter"></a><span data-ttu-id="3aa6e-103">範例捕獲篩選器</span><span class="sxs-lookup"><span data-stu-id="3aa6e-103">Sample Grabber Filter</span></span>

> [!Note]  
> <span data-ttu-id="3aa6e-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="3aa6e-104">\[Deprecated.</span></span> <span data-ttu-id="3aa6e-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="3aa6e-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="3aa6e-106">範例捕獲篩選器可讓您在範例通過篩選圖形時，取得範例。</span><span class="sxs-lookup"><span data-stu-id="3aa6e-106">The Sample Grabber filter provides a way to retrieve samples as they pass through the filter graph.</span></span> <span data-ttu-id="3aa6e-107">它是具有一個輸入 pin 和一個輸出 pin 的轉換篩選。</span><span class="sxs-lookup"><span data-stu-id="3aa6e-107">It is a transform filter with one input pin and one output pin.</span></span> <span data-ttu-id="3aa6e-108">它會以未變更的方式傳遞所有範例，因此您可以將它插入至篩選圖形，而不需要變更資料流程。</span><span class="sxs-lookup"><span data-stu-id="3aa6e-108">It passes all samples downstream unchanged, so you can insert it into a filter graph without altering the data stream.</span></span> <span data-ttu-id="3aa6e-109">然後，您的應用程式可以藉由呼叫 [**ISampleGrabber**](isamplegrabber.md) 介面上的方法，從篩選器中取出個別樣本。</span><span class="sxs-lookup"><span data-stu-id="3aa6e-109">Your application can then retrieve individual samples from the filter by calling methods on the [**ISampleGrabber**](isamplegrabber.md) interface.</span></span>

<span data-ttu-id="3aa6e-110">如果您想要在不轉譯資料的情況下取出範例，請將範例抓取器篩選器連接到 [**Null**](null-renderer-filter.md) 轉譯器篩選器。</span><span class="sxs-lookup"><span data-stu-id="3aa6e-110">If you want to retrieve samples without rendering the data, connect the Sample Grabber filter to the [**Null Renderer**](null-renderer-filter.md) filter.</span></span>



|                                          |                                                                                                                                                    |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3aa6e-111">篩選介面</span><span class="sxs-lookup"><span data-stu-id="3aa6e-111">Filter interfaces</span></span>                        | <span data-ttu-id="3aa6e-112">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)、 [ **ISampleGrabber**](isamplegrabber.md)</span><span class="sxs-lookup"><span data-stu-id="3aa6e-112">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**ISampleGrabber**](isamplegrabber.md)</span></span>                                                                       |
| <span data-ttu-id="3aa6e-113">輸入 pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="3aa6e-113">Input pin media types</span></span>                    | <span data-ttu-id="3aa6e-114">任何媒體類型。</span><span class="sxs-lookup"><span data-stu-id="3aa6e-114">Any media type.</span></span>                                                                                                                                    |
| <span data-ttu-id="3aa6e-115">輸入 pin 介面</span><span class="sxs-lookup"><span data-stu-id="3aa6e-115">Input pin interfaces</span></span>                     | <span data-ttu-id="3aa6e-116">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)、 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)、 [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="3aa6e-116">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                             |
| <span data-ttu-id="3aa6e-117">輸出 pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="3aa6e-117">Output pin media types</span></span>                   | <span data-ttu-id="3aa6e-118">任何媒體類型。</span><span class="sxs-lookup"><span data-stu-id="3aa6e-118">Any media type.</span></span> <span data-ttu-id="3aa6e-119">符合輸入媒體類型。</span><span class="sxs-lookup"><span data-stu-id="3aa6e-119">Matches input media type.</span></span>                                                                                                          |
| <span data-ttu-id="3aa6e-120">輸出 pin 介面</span><span class="sxs-lookup"><span data-stu-id="3aa6e-120">Output pin interfaces</span></span>                    | <span data-ttu-id="3aa6e-121">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition)、 [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)、 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)、 [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="3aa6e-121">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span> |
| <span data-ttu-id="3aa6e-122">篩選 CLSID</span><span class="sxs-lookup"><span data-stu-id="3aa6e-122">Filter CLSID</span></span>                             | <span data-ttu-id="3aa6e-123">CLSID \_ SampleGrabber</span><span class="sxs-lookup"><span data-stu-id="3aa6e-123">CLSID\_SampleGrabber</span></span>                                                                                                                               |
| <span data-ttu-id="3aa6e-124">屬性頁 CLSID</span><span class="sxs-lookup"><span data-stu-id="3aa6e-124">Property Page CLSID</span></span>                      | <span data-ttu-id="3aa6e-125">沒有屬性頁。</span><span class="sxs-lookup"><span data-stu-id="3aa6e-125">No property page.</span></span>                                                                                                                                  |
| <span data-ttu-id="3aa6e-126">可執行檔</span><span class="sxs-lookup"><span data-stu-id="3aa6e-126">Executable</span></span>                               | <span data-ttu-id="3aa6e-127">Qedit.dll</span><span class="sxs-lookup"><span data-stu-id="3aa6e-127">Qedit.dll</span></span>                                                                                                                                          |
| [<span data-ttu-id="3aa6e-128">優點</span><span class="sxs-lookup"><span data-stu-id="3aa6e-128">Merit</span></span>](merit.md)                       | <span data-ttu-id="3aa6e-129">\_ \_ 未 \_ 使用的業績</span><span class="sxs-lookup"><span data-stu-id="3aa6e-129">MERIT\_DO\_NOT\_USE</span></span>                                                                                                                                |
| [<span data-ttu-id="3aa6e-130">篩選準則分類</span><span class="sxs-lookup"><span data-stu-id="3aa6e-130">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="3aa6e-131">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="3aa6e-131">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="3aa6e-132">備註</span><span class="sxs-lookup"><span data-stu-id="3aa6e-132">Remarks</span></span>

<span data-ttu-id="3aa6e-133">若要使用此篩選，請將它新增至篩選圖形，並以所需的媒體類型呼叫 [**ISampleGrabber：： SetMediaType**](isamplegrabber-setmediatype.md) 。</span><span class="sxs-lookup"><span data-stu-id="3aa6e-133">To use this filter, add it to the filter graph and call [**ISampleGrabber::SetMediaType**](isamplegrabber-setmediatype.md) with the desired media type.</span></span> <span data-ttu-id="3aa6e-134">這個方法會指定篩選的輸入和輸出連接的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="3aa6e-134">This method specifies the media type for the filter's input and output pin connections.</span></span> <span data-ttu-id="3aa6e-135">然後將篩選連接到圖形中的其他篩選。</span><span class="sxs-lookup"><span data-stu-id="3aa6e-135">Then connect the filter to other filters in the graph.</span></span>

<span data-ttu-id="3aa6e-136">如果您使用值 **TRUE** 來呼叫 [**ISampleGrabber：： SetBufferSamples**](isamplegrabber-setbuffersamples.md) ，則篩選會緩衝處理其所接收的每個範例，然後再將它傳遞給下游。</span><span class="sxs-lookup"><span data-stu-id="3aa6e-136">If you call [**ISampleGrabber::SetBufferSamples**](isamplegrabber-setbuffersamples.md) with the value **TRUE**, the filter buffers each sample that it receives before passing it downstream.</span></span> <span data-ttu-id="3aa6e-137">呼叫 [**ISampleGrabber：： GetCurrentBuffer**](isamplegrabber-getcurrentbuffer.md) 方法，以取出緩衝區的目前內容。</span><span class="sxs-lookup"><span data-stu-id="3aa6e-137">Call the [**ISampleGrabber::GetCurrentBuffer**](isamplegrabber-getcurrentbuffer.md) method to retrieve the current contents of the buffer.</span></span> <span data-ttu-id="3aa6e-138">或者，您可以呼叫 [**ISampleGrabber：： SetCallback**](isamplegrabber-setcallback.md) ，讓篩選器在每次收到範例時叫用回呼函式。</span><span class="sxs-lookup"><span data-stu-id="3aa6e-138">Alternatively, you can call [**ISampleGrabber::SetCallback**](isamplegrabber-setcallback.md) to have the filter invoke a callback function whenever it receives a sample.</span></span>

<span data-ttu-id="3aa6e-139">篩選準則的影片格式有下列限制：</span><span class="sxs-lookup"><span data-stu-id="3aa6e-139">The filter has the following limitations for video formats:</span></span>

-   <span data-ttu-id="3aa6e-140">它不支援由上而下方向 (負面 **biHeight**) 的影片類型。</span><span class="sxs-lookup"><span data-stu-id="3aa6e-140">It does not support video types with top-down orientation (negative **biHeight**).</span></span>
-   <span data-ttu-id="3aa6e-141">它不支援 [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) 格式結構 (格式類型等於 **format \_ VideoInfo2**) 。</span><span class="sxs-lookup"><span data-stu-id="3aa6e-141">It does not support the [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) format structure (format type equal to **FORMAT\_VideoInfo2**).</span></span>
-   <span data-ttu-id="3aa6e-142">它會拒絕表面 stride 不符合影片寬度的任何影片類型。</span><span class="sxs-lookup"><span data-stu-id="3aa6e-142">It rejects any video type where the surface stride does not match the video width.</span></span>

<span data-ttu-id="3aa6e-143">如此一來，範例抓取程式將無法連線到影片混合轉譯器 (VMR) 適用于某些影片類型。</span><span class="sxs-lookup"><span data-stu-id="3aa6e-143">As a result, the Sample Grabber will not connect to the Video Mixing Renderer (VMR) for some video types.</span></span>

## <a name="requirements"></a><span data-ttu-id="3aa6e-144">規格需求</span><span class="sxs-lookup"><span data-stu-id="3aa6e-144">Requirements</span></span>



| <span data-ttu-id="3aa6e-145">需求</span><span class="sxs-lookup"><span data-stu-id="3aa6e-145">Requirement</span></span> | <span data-ttu-id="3aa6e-146">值</span><span class="sxs-lookup"><span data-stu-id="3aa6e-146">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3aa6e-147">標頭</span><span class="sxs-lookup"><span data-stu-id="3aa6e-147">Header</span></span><br/> | <dl> <span data-ttu-id="3aa6e-148"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="3aa6e-148"><dt>Qedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3aa6e-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3aa6e-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3aa6e-150">DirectShow 編輯服務物件</span><span class="sxs-lookup"><span data-stu-id="3aa6e-150">DirectShow Editing Services Objects</span></span>](directshow-editing-services-objects.md)
</dt> <dt>

[<span data-ttu-id="3aa6e-151">使用範例捕獲</span><span class="sxs-lookup"><span data-stu-id="3aa6e-151">Using the Sample Grabber</span></span>](using-the-sample-grabber.md)
</dt> </dl>

 

 




