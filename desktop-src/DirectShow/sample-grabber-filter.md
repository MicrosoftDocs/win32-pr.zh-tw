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
ms.openlocfilehash: f0b0ddffe2bc769b7c2371ef93091d8c1daf379c
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909666"
---
# <a name="sample-grabber-filter"></a><span data-ttu-id="3d110-103">範例捕獲篩選器</span><span class="sxs-lookup"><span data-stu-id="3d110-103">Sample Grabber Filter</span></span>

> [!Note]  
> <span data-ttu-id="3d110-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="3d110-104">\[Deprecated.</span></span> <span data-ttu-id="3d110-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="3d110-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="3d110-106">範例捕獲篩選器可讓您在範例通過篩選圖形時，取得範例。</span><span class="sxs-lookup"><span data-stu-id="3d110-106">The Sample Grabber filter provides a way to retrieve samples as they pass through the filter graph.</span></span> <span data-ttu-id="3d110-107">它是具有一個輸入 pin 和一個輸出 pin 的轉換篩選。</span><span class="sxs-lookup"><span data-stu-id="3d110-107">It is a transform filter with one input pin and one output pin.</span></span> <span data-ttu-id="3d110-108">它會以未變更的方式傳遞所有範例，因此您可以將它插入至篩選圖形，而不需要變更資料流程。</span><span class="sxs-lookup"><span data-stu-id="3d110-108">It passes all samples downstream unchanged, so you can insert it into a filter graph without altering the data stream.</span></span> <span data-ttu-id="3d110-109">然後，您的應用程式可以藉由呼叫 [**ISampleGrabber**](isamplegrabber.md) 介面上的方法，從篩選器中取出個別樣本。</span><span class="sxs-lookup"><span data-stu-id="3d110-109">Your application can then retrieve individual samples from the filter by calling methods on the [**ISampleGrabber**](isamplegrabber.md) interface.</span></span>

<span data-ttu-id="3d110-110">如果您想要在不轉譯資料的情況下取出範例，請將範例抓取器篩選器連接到 [**Null**](null-renderer-filter.md) 轉譯器篩選器。</span><span class="sxs-lookup"><span data-stu-id="3d110-110">If you want to retrieve samples without rendering the data, connect the Sample Grabber filter to the [**Null Renderer**](null-renderer-filter.md) filter.</span></span>



| <span data-ttu-id="3d110-111">標籤</span><span class="sxs-lookup"><span data-stu-id="3d110-111">Label</span></span> | <span data-ttu-id="3d110-112">值</span><span class="sxs-lookup"><span data-stu-id="3d110-112">Value</span></span> |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d110-113">篩選介面</span><span class="sxs-lookup"><span data-stu-id="3d110-113">Filter interfaces</span></span>                        | <span data-ttu-id="3d110-114">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)、 [ **ISampleGrabber**](isamplegrabber.md)</span><span class="sxs-lookup"><span data-stu-id="3d110-114">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**ISampleGrabber**](isamplegrabber.md)</span></span>                                                                       |
| <span data-ttu-id="3d110-115">輸入 pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="3d110-115">Input pin media types</span></span>                    | <span data-ttu-id="3d110-116">任何媒體類型。</span><span class="sxs-lookup"><span data-stu-id="3d110-116">Any media type.</span></span>                                                                                                                                    |
| <span data-ttu-id="3d110-117">輸入 pin 介面</span><span class="sxs-lookup"><span data-stu-id="3d110-117">Input pin interfaces</span></span>                     | <span data-ttu-id="3d110-118">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)、 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)、 [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="3d110-118">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                             |
| <span data-ttu-id="3d110-119">輸出 pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="3d110-119">Output pin media types</span></span>                   | <span data-ttu-id="3d110-120">任何媒體類型。</span><span class="sxs-lookup"><span data-stu-id="3d110-120">Any media type.</span></span> <span data-ttu-id="3d110-121">符合輸入媒體類型。</span><span class="sxs-lookup"><span data-stu-id="3d110-121">Matches input media type.</span></span>                                                                                                          |
| <span data-ttu-id="3d110-122">輸出 pin 介面</span><span class="sxs-lookup"><span data-stu-id="3d110-122">Output pin interfaces</span></span>                    | <span data-ttu-id="3d110-123">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition)、 [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)、 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)、 [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="3d110-123">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span> |
| <span data-ttu-id="3d110-124">篩選 CLSID</span><span class="sxs-lookup"><span data-stu-id="3d110-124">Filter CLSID</span></span>                             | <span data-ttu-id="3d110-125">CLSID \_ SampleGrabber</span><span class="sxs-lookup"><span data-stu-id="3d110-125">CLSID\_SampleGrabber</span></span>                                                                                                                               |
| <span data-ttu-id="3d110-126">屬性頁 CLSID</span><span class="sxs-lookup"><span data-stu-id="3d110-126">Property Page CLSID</span></span>                      | <span data-ttu-id="3d110-127">沒有屬性頁。</span><span class="sxs-lookup"><span data-stu-id="3d110-127">No property page.</span></span>                                                                                                                                  |
| <span data-ttu-id="3d110-128">可執行檔</span><span class="sxs-lookup"><span data-stu-id="3d110-128">Executable</span></span>                               | <span data-ttu-id="3d110-129">Qedit.dll</span><span class="sxs-lookup"><span data-stu-id="3d110-129">Qedit.dll</span></span>                                                                                                                                          |
| [<span data-ttu-id="3d110-130">優點</span><span class="sxs-lookup"><span data-stu-id="3d110-130">Merit</span></span>](merit.md)                       | <span data-ttu-id="3d110-131">\_ \_ 未 \_ 使用的業績</span><span class="sxs-lookup"><span data-stu-id="3d110-131">MERIT\_DO\_NOT\_USE</span></span>                                                                                                                                |
| [<span data-ttu-id="3d110-132">篩選準則分類</span><span class="sxs-lookup"><span data-stu-id="3d110-132">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="3d110-133">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="3d110-133">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="3d110-134">備註</span><span class="sxs-lookup"><span data-stu-id="3d110-134">Remarks</span></span>

<span data-ttu-id="3d110-135">若要使用此篩選，請將它新增至篩選圖形，並以所需的媒體類型呼叫 [**ISampleGrabber：： SetMediaType**](isamplegrabber-setmediatype.md) 。</span><span class="sxs-lookup"><span data-stu-id="3d110-135">To use this filter, add it to the filter graph and call [**ISampleGrabber::SetMediaType**](isamplegrabber-setmediatype.md) with the desired media type.</span></span> <span data-ttu-id="3d110-136">這個方法會指定篩選的輸入和輸出連接的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="3d110-136">This method specifies the media type for the filter's input and output pin connections.</span></span> <span data-ttu-id="3d110-137">然後將篩選連接到圖形中的其他篩選。</span><span class="sxs-lookup"><span data-stu-id="3d110-137">Then connect the filter to other filters in the graph.</span></span>

<span data-ttu-id="3d110-138">如果您使用值 **TRUE** 來呼叫 [**ISampleGrabber：： SetBufferSamples**](isamplegrabber-setbuffersamples.md) ，則篩選會緩衝處理其所接收的每個範例，然後再將它傳遞給下游。</span><span class="sxs-lookup"><span data-stu-id="3d110-138">If you call [**ISampleGrabber::SetBufferSamples**](isamplegrabber-setbuffersamples.md) with the value **TRUE**, the filter buffers each sample that it receives before passing it downstream.</span></span> <span data-ttu-id="3d110-139">呼叫 [**ISampleGrabber：： GetCurrentBuffer**](isamplegrabber-getcurrentbuffer.md) 方法，以取出緩衝區的目前內容。</span><span class="sxs-lookup"><span data-stu-id="3d110-139">Call the [**ISampleGrabber::GetCurrentBuffer**](isamplegrabber-getcurrentbuffer.md) method to retrieve the current contents of the buffer.</span></span> <span data-ttu-id="3d110-140">或者，您可以呼叫 [**ISampleGrabber：： SetCallback**](isamplegrabber-setcallback.md) ，讓篩選器在每次收到範例時叫用回呼函式。</span><span class="sxs-lookup"><span data-stu-id="3d110-140">Alternatively, you can call [**ISampleGrabber::SetCallback**](isamplegrabber-setcallback.md) to have the filter invoke a callback function whenever it receives a sample.</span></span>

<span data-ttu-id="3d110-141">篩選準則的影片格式有下列限制：</span><span class="sxs-lookup"><span data-stu-id="3d110-141">The filter has the following limitations for video formats:</span></span>

-   <span data-ttu-id="3d110-142">它不支援由上而下方向 (負面 **biHeight**) 的影片類型。</span><span class="sxs-lookup"><span data-stu-id="3d110-142">It does not support video types with top-down orientation (negative **biHeight**).</span></span>
-   <span data-ttu-id="3d110-143">它不支援 [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) 格式結構 (格式類型等於 **format \_ VideoInfo2**) 。</span><span class="sxs-lookup"><span data-stu-id="3d110-143">It does not support the [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) format structure (format type equal to **FORMAT\_VideoInfo2**).</span></span>
-   <span data-ttu-id="3d110-144">它會拒絕表面 stride 不符合影片寬度的任何影片類型。</span><span class="sxs-lookup"><span data-stu-id="3d110-144">It rejects any video type where the surface stride does not match the video width.</span></span>

<span data-ttu-id="3d110-145">如此一來，範例抓取程式將無法連線到影片混合轉譯器 (VMR) 適用于某些影片類型。</span><span class="sxs-lookup"><span data-stu-id="3d110-145">As a result, the Sample Grabber will not connect to the Video Mixing Renderer (VMR) for some video types.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d110-146">規格需求</span><span class="sxs-lookup"><span data-stu-id="3d110-146">Requirements</span></span>



| <span data-ttu-id="3d110-147">需求</span><span class="sxs-lookup"><span data-stu-id="3d110-147">Requirement</span></span> | <span data-ttu-id="3d110-148">值</span><span class="sxs-lookup"><span data-stu-id="3d110-148">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3d110-149">標頭</span><span class="sxs-lookup"><span data-stu-id="3d110-149">Header</span></span><br/> | <dl> <span data-ttu-id="3d110-150"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="3d110-150"><dt>Qedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d110-151">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3d110-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d110-152">DirectShow 編輯服務物件</span><span class="sxs-lookup"><span data-stu-id="3d110-152">DirectShow Editing Services Objects</span></span>](directshow-editing-services-objects.md)
</dt> <dt>

[<span data-ttu-id="3d110-153">使用範例捕獲</span><span class="sxs-lookup"><span data-stu-id="3d110-153">Using the Sample Grabber</span></span>](using-the-sample-grabber.md)
</dt> </dl>

 

 




