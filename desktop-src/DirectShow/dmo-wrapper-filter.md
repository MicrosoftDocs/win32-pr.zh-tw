---
description: SQL-DMO 包裝函式篩選
ms.assetid: ffa6234d-9040-4838-8f51-0cf87df40a5c
title: SQL-DMO 包裝函式篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d29c5b86bdff4a215ec2ef5854d09a1f842dbf0e
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908626"
---
# <a name="dmo-wrapper-filter"></a><span data-ttu-id="d9ba4-103">SQL-DMO 包裝函式篩選</span><span class="sxs-lookup"><span data-stu-id="d9ba4-103">DMO Wrapper Filter</span></span>

<span data-ttu-id="d9ba4-104">SQL-DMO 包裝函式篩選器可讓 DirectShow 應用程式在篩選圖形中使用 [DirectX 媒體物件](directx-media-objects.md) (的) 。</span><span class="sxs-lookup"><span data-stu-id="d9ba4-104">The DMO Wrapper filter enables a DirectShow application to use a [DirectX Media Object](directx-media-objects.md) (DMO) within a filter graph.</span></span> <span data-ttu-id="d9ba4-105">篩選準則會包裝，並處理所有使用 SQL-DMO 的詳細資料，例如將資料傳入和傳送。</span><span class="sxs-lookup"><span data-stu-id="d9ba4-105">The filter wraps the DMO and handles all the details of using the DMO, such as passing data to and from the DMO.</span></span> <span data-ttu-id="d9ba4-106">此外，篩選準則會匯總]，讓應用程式可以查詢任何適用于 SQL-DMO 所公開之 COM 介面的篩選。</span><span class="sxs-lookup"><span data-stu-id="d9ba4-106">Also, the filter aggregates the DMO, so the application can query the filter for any COM interfaces that the DMO exposes.</span></span>



| <span data-ttu-id="d9ba4-107">標籤</span><span class="sxs-lookup"><span data-stu-id="d9ba4-107">Label</span></span> | <span data-ttu-id="d9ba4-108">值</span><span class="sxs-lookup"><span data-stu-id="d9ba4-108">Value</span></span> |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9ba4-109">篩選介面</span><span class="sxs-lookup"><span data-stu-id="d9ba4-109">Filter Interfaces</span></span>                        | <span data-ttu-id="d9ba4-110">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)、 [**IDMOWrapperFilter**](/previous-versions/windows/desktop/api/Dmodshow/nn-dmodshow-idmowrapperfilter)、 [**IPersistStream**](/windows/desktop/api/objidl/nn-objidl-ipersiststream)</span><span class="sxs-lookup"><span data-stu-id="d9ba4-110">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IDMOWrapperFilter**](/previous-versions/windows/desktop/api/Dmodshow/nn-dmodshow-idmowrapperfilter), [**IPersistStream**](/windows/desktop/api/objidl/nn-objidl-ipersiststream)</span></span>                                                                                                                       |
| <span data-ttu-id="d9ba4-111">輸入 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="d9ba4-111">Input Pin Media Types</span></span>                    | <span data-ttu-id="d9ba4-112">請參閱備註</span><span class="sxs-lookup"><span data-stu-id="d9ba4-112">See Remarks</span></span>                                                                                                                                                                                                                                        |
| <span data-ttu-id="d9ba4-113">輸入 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="d9ba4-113">Input Pin Interfaces</span></span>                     | <span data-ttu-id="d9ba4-114">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)、 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)、 [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="d9ba4-114">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                                                                                                                             |
| <span data-ttu-id="d9ba4-115">輸出 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="d9ba4-115">Output Pin Media Types</span></span>                   | <span data-ttu-id="d9ba4-116">請參閱備註</span><span class="sxs-lookup"><span data-stu-id="d9ba4-116">See Remarks</span></span>                                                                                                                                                                                                                                        |
| <span data-ttu-id="d9ba4-117">輸出 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="d9ba4-117">Output Pin Interfaces</span></span>                    | <span data-ttu-id="d9ba4-118">[**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig)、 [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression)、 [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition)、 [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)、 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)、 [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="d9ba4-118">[**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span> |
| <span data-ttu-id="d9ba4-119">篩選 CLSID</span><span class="sxs-lookup"><span data-stu-id="d9ba4-119">Filter CLSID</span></span>                             | <span data-ttu-id="d9ba4-120">CLSID \_ DMOWrapperFilter</span><span class="sxs-lookup"><span data-stu-id="d9ba4-120">CLSID\_DMOWrapperFilter</span></span>                                                                                                                                                                                                                            |
| <span data-ttu-id="d9ba4-121">屬性頁 CLSID</span><span class="sxs-lookup"><span data-stu-id="d9ba4-121">Property Page CLSID</span></span>                      | <span data-ttu-id="d9ba4-122">沒有屬性頁</span><span class="sxs-lookup"><span data-stu-id="d9ba4-122">No property page</span></span>                                                                                                                                                                                                                                   |
| <span data-ttu-id="d9ba4-123">可執行檔</span><span class="sxs-lookup"><span data-stu-id="d9ba4-123">Executable</span></span>                               | <span data-ttu-id="d9ba4-124">Qasf.dll</span><span class="sxs-lookup"><span data-stu-id="d9ba4-124">Qasf.dll</span></span>                                                                                                                                                                                                                                           |
| [<span data-ttu-id="d9ba4-125">優點</span><span class="sxs-lookup"><span data-stu-id="d9ba4-125">Merit</span></span>](merit.md)                       | <span data-ttu-id="d9ba4-126">請參閱備註</span><span class="sxs-lookup"><span data-stu-id="d9ba4-126">See Remarks</span></span>                                                                                                                                                                                                                                        |
| [<span data-ttu-id="d9ba4-127">篩選準則分類</span><span class="sxs-lookup"><span data-stu-id="d9ba4-127">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="d9ba4-128">請參閱備註</span><span class="sxs-lookup"><span data-stu-id="d9ba4-128">See Remarks</span></span>                                                                                                                                                                                                                                        |



 

## <a name="remarks"></a><span data-ttu-id="d9ba4-129">備註</span><span class="sxs-lookup"><span data-stu-id="d9ba4-129">Remarks</span></span>

### <a name="limitations"></a><span data-ttu-id="d9ba4-130">限制</span><span class="sxs-lookup"><span data-stu-id="d9ba4-130">Limitations</span></span>

<span data-ttu-id="d9ba4-131">SQL-DMO 包裝函式有下列限制：</span><span class="sxs-lookup"><span data-stu-id="d9ba4-131">The DMO Wrapper has the following limitations:</span></span>

-   <span data-ttu-id="d9ba4-132">它不支援 DMOs 包含零個輸入、多個輸入或零個輸出。</span><span class="sxs-lookup"><span data-stu-id="d9ba4-132">It does not support DMOs with zero inputs, multiple inputs, or zero outputs.</span></span> <span data-ttu-id="d9ba4-133"> (它確實支援具有一個輸入和多個輸出的 DMOs。 ) </span><span class="sxs-lookup"><span data-stu-id="d9ba4-133">(It does support DMOs with one input and multiple outputs.)</span></span>
-   <span data-ttu-id="d9ba4-134">它不支援自訂傳輸。</span><span class="sxs-lookup"><span data-stu-id="d9ba4-134">It does not support custom transports.</span></span> <span data-ttu-id="d9ba4-135">所有資料傳輸都是透過 [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) 介面完成。</span><span class="sxs-lookup"><span data-stu-id="d9ba4-135">All data transport is done through the [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) interface.</span></span>
-   <span data-ttu-id="d9ba4-136">它不會使用 **IMediaObjectInPlace** 介面;所有處理都是使用 [**IMediaObject**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject) 方法來完成。</span><span class="sxs-lookup"><span data-stu-id="d9ba4-136">It does not use the **IMediaObjectInPlace** interface; all processing is done using [**IMediaObject**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject) methods.</span></span>

### <a name="pins"></a><span data-ttu-id="d9ba4-137">釘選</span><span class="sxs-lookup"><span data-stu-id="d9ba4-137">Pins</span></span>

<span data-ttu-id="d9ba4-138">針對每個輸入資料流程，此篩選準則會建立對應的輸入 pin。</span><span class="sxs-lookup"><span data-stu-id="d9ba4-138">For each input stream on the DMO, the filter creates a corresponding input pin.</span></span> <span data-ttu-id="d9ba4-139">針對每個輸出資料流程，它會建立對應的輸出圖釘。</span><span class="sxs-lookup"><span data-stu-id="d9ba4-139">For each output stream, it creates a corresponding output pin.</span></span> <span data-ttu-id="d9ba4-140">每個 pin 所支援的媒體類型取決於 SQL-DMO</span><span class="sxs-lookup"><span data-stu-id="d9ba4-140">The media types that each pin supports depends on the DMO</span></span>

### <a name="encoder-interfaces"></a><span data-ttu-id="d9ba4-141">編碼器介面</span><span class="sxs-lookup"><span data-stu-id="d9ba4-141">Encoder Interfaces</span></span>

<span data-ttu-id="d9ba4-142">如果 SQL-DMO 是影片編碼器或音訊編碼器，輸出圖釘會公開 [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) 介面。</span><span class="sxs-lookup"><span data-stu-id="d9ba4-142">If the DMO is a video encoder or an audio encoder, the output pin exposes the [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) interface.</span></span> <span data-ttu-id="d9ba4-143">如果 SQL-DMO 是影片編碼器，輸出釘選也會公開 [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) 介面。</span><span class="sxs-lookup"><span data-stu-id="d9ba4-143">If the DMO is a video encoder, the output pin also exposes the [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) interface.</span></span> <span data-ttu-id="d9ba4-144">在這兩種情況下，如果 SQL-DMO 支援介面，則釘選會委派給 SQL-DMO。</span><span class="sxs-lookup"><span data-stu-id="d9ba4-144">In both cases, if the DMO supports the interface, the pin delegates to the DMO.</span></span> <span data-ttu-id="d9ba4-145">否則，pin 會提供自己的實作為。</span><span class="sxs-lookup"><span data-stu-id="d9ba4-145">Otherwise, the pin provides its own implementation.</span></span>

### <a name="streaming"></a><span data-ttu-id="d9ba4-146">串流</span><span class="sxs-lookup"><span data-stu-id="d9ba4-146">Streaming</span></span>

<span data-ttu-id="d9ba4-147">篩選器會使用 [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) 介面來處理所有串流處理。</span><span class="sxs-lookup"><span data-stu-id="d9ba4-147">The filter uses the [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) interface to handle all streaming.</span></span> <span data-ttu-id="d9ba4-148">它不支援 [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) 連接。</span><span class="sxs-lookup"><span data-stu-id="d9ba4-148">It does not support [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) connections.</span></span> <span data-ttu-id="d9ba4-149">篩選準則只會在 IMediaObject 接收來自上游 (的資料時（包含) 的資料流程結束通知）時，才會呼叫 [**：:P rocessoutput**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-processoutput) 。</span><span class="sxs-lookup"><span data-stu-id="d9ba4-149">The filter calls [**IMediaObject::ProcessOutput**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-processoutput) on the DMO only when it receives data from upstream (including end-of-stream notifications).</span></span> <span data-ttu-id="d9ba4-150">因此，它不支援 DMOs 為零的輸入資料流程。</span><span class="sxs-lookup"><span data-stu-id="d9ba4-150">Therefore, it does not support DMOs with zero input streams.</span></span>

### <a name="seeking"></a><span data-ttu-id="d9ba4-151">尋求</span><span class="sxs-lookup"><span data-stu-id="d9ba4-151">Seeking</span></span>

<span data-ttu-id="d9ba4-152">所有搜尋要求都會透過的第一個輸入 pin，傳遞給您的上游篩選器。</span><span class="sxs-lookup"><span data-stu-id="d9ba4-152">All seek requests are passed to the upstream filter, through the first input pin on the DMO Wrapper.</span></span> <span data-ttu-id="d9ba4-153">針對多個輸出 DMOs，這表示上游篩選器可能會在應用程式搜尋圖形時收到多個搜尋要求。</span><span class="sxs-lookup"><span data-stu-id="d9ba4-153">For multiple-output DMOs, this means that the upstream filter might receive multiple seek requests when the application seeks the graph.</span></span>

### <a name="merit"></a><span data-ttu-id="d9ba4-154">優點</span><span class="sxs-lookup"><span data-stu-id="d9ba4-154">Merit</span></span>

<span data-ttu-id="d9ba4-155">DirectShow 會為所有 DMOs 指派預設的 [ **\_ 一般** ] + [0x800] 值。</span><span class="sxs-lookup"><span data-stu-id="d9ba4-155">DirectShow assigns all DMOs a default merit value of **MERIT\_NORMAL** + 0x800.</span></span> <span data-ttu-id="d9ba4-156">此值落在 **慣用 \_ 標準** 和 **\_ 慣用** 的範圍之間。</span><span class="sxs-lookup"><span data-stu-id="d9ba4-156">This value falls between **MERIT\_NORMAL** and **MERIT\_PREFERRED**.</span></span> <span data-ttu-id="d9ba4-157">「解碼」篩選器通常會有 **「 \_ 正常**」的價值。</span><span class="sxs-lookup"><span data-stu-id="d9ba4-157">Decoder filters generally have a merit value of **MERIT\_NORMAL**.</span></span> <span data-ttu-id="d9ba4-158">因此，篩選圖形管理員通常會在一個解碼篩選器上選取一種，</span><span class="sxs-lookup"><span data-stu-id="d9ba4-158">Therefore, the filter graph manager will usually select a DMO decoder over a decoder filter.</span></span> <span data-ttu-id="d9ba4-159">若要覆寫預設的 [使用] 值，請將登錄專案新增至 HKEY \_ 類別 \_ 根目錄 CLSID 中的 sql-dmo 登錄機碼 \\ 。</span><span class="sxs-lookup"><span data-stu-id="d9ba4-159">To override the default merit value, add a registry entry to the DMO's registry key in HKEY\_CLASSES\_ROOT\\CLSID.</span></span> <span data-ttu-id="d9ba4-160">包含名為「「有」值的 **DWORD** 值，其值會指定「業績」。</span><span class="sxs-lookup"><span data-stu-id="d9ba4-160">Include a **DWORD** value named "Merit" whose value specifies the merit.</span></span>

### <a name="category"></a><span data-ttu-id="d9ba4-161">類別</span><span class="sxs-lookup"><span data-stu-id="d9ba4-161">Category</span></span>

<span data-ttu-id="d9ba4-162">在任何類別中，就不會將它本身顯示為 [i] 包裝函式篩選。</span><span class="sxs-lookup"><span data-stu-id="d9ba4-162">The DMO Wrapper filter does not appear by itself in any category.</span></span> <span data-ttu-id="d9ba4-163">當它換行時，它會出現在 [DirectShow] 類別中，並對應至 [中] 的 [名稱]。</span><span class="sxs-lookup"><span data-stu-id="d9ba4-163">When it wraps a DMO, it appears in the DirectShow category that corresponds to the DMO's category, under the name of the DMO.</span></span>

### <a name="buffers"></a><span data-ttu-id="d9ba4-164">緩衝區</span><span class="sxs-lookup"><span data-stu-id="d9ba4-164">Buffers</span></span>

<span data-ttu-id="d9ba4-165">SQL-DMO 包裝函式篩選會將媒體緩衝區傳遞給用來公開 [**IMediaBuffer**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediabuffer) 介面的]。</span><span class="sxs-lookup"><span data-stu-id="d9ba4-165">The DMO Wrapper filter passes media buffers to the DMO which expose the [**IMediaBuffer**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediabuffer) interface.</span></span>

<span data-ttu-id="d9ba4-166">在 Windows Vista 或更新版本中，媒體緩衝區也會公開 IServiceProvider 介面。</span><span class="sxs-lookup"><span data-stu-id="d9ba4-166">In Windows Vista or later, the media buffers also expose the IServiceProvider interface.</span></span> <span data-ttu-id="d9ba4-167">您可以使用這個介面來取得與緩衝區相關聯之媒體範例的指標。</span><span class="sxs-lookup"><span data-stu-id="d9ba4-167">The DMO can use this interface to get a pointer to the media sample that is associated with the buffer.</span></span> <span data-ttu-id="d9ba4-168">使用服務識別碼 **IID \_ IMediaSample**。</span><span class="sxs-lookup"><span data-stu-id="d9ba4-168">Use the service identifier **IID\_IMediaSample**.</span></span> <span data-ttu-id="d9ba4-169">SQL-DMO 可以使用媒體範例的 [**IMediaSample2**](/windows/desktop/api/Strmif/nn-strmif-imediasample2) 介面來設定範例上的交錯旗標。</span><span class="sxs-lookup"><span data-stu-id="d9ba4-169">A video DMO can use the media sample's [**IMediaSample2**](/windows/desktop/api/Strmif/nn-strmif-imediasample2) interface to set interlace flags on the sample.</span></span> <span data-ttu-id="d9ba4-170">下列程式碼顯示如何取得媒體範例的指標：</span><span class="sxs-lookup"><span data-stu-id="d9ba4-170">The following code shows how to get the pointer to the media sample:</span></span>


```C++
IServiceProvider *pSp = NULL;
IMediaSample2 *pSample2 = NULL;
HRESULT hr = S_OK;

hr = pBuffer->QueryInterface(IID_IServiceProvider, (void**)&pSp);
if (SUCCEEDED(hr))
{
    hr = pSp->QueryService(
        IID_IMediaSample,  // Service identifier.
        IID_IMediaSample2, // Interface identifier.
        (void**)&pSample2
        );
    if (SUCCEEDED(hr))
    {
        // Set flags (not shown).
        pSample2->Release();
    }
    pSp->Release();
}
```



<span data-ttu-id="d9ba4-171">如需有關每個範例交錯旗標的詳細資訊，請參閱 [**AM \_ Sample2.xml \_ 屬性結構**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties)。</span><span class="sxs-lookup"><span data-stu-id="d9ba4-171">For more information about per-sample interlace flags, see [**AM\_SAMPLE2\_PROPERTIES Structure**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties).</span></span>

### <a name="quality-control"></a><span data-ttu-id="d9ba4-172">品質控制</span><span class="sxs-lookup"><span data-stu-id="d9ba4-172">Quality Control</span></span>

<span data-ttu-id="d9ba4-173">如果 SQL-DMO 公開了 [**IDMOQualityControl**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-idmoqualitycontrol) 介面，則篩選會將其輸出圖釘上的 [**IQualityControl：： Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) 呼叫轉譯為上的 [**IDMOQualityControl：： SetNow**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-idmoqualitycontrol-setnow) 呼叫。</span><span class="sxs-lookup"><span data-stu-id="d9ba4-173">If the DMO exposes the [**IDMOQualityControl**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-idmoqualitycontrol) interface, the filter translates [**IQualityControl::Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) calls on its output pin into [**IDMOQualityControl::SetNow**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-idmoqualitycontrol-setnow) calls on the DMO.</span></span> <span data-ttu-id="d9ba4-174">**SetNow** 的 *rtNow* 參數會計算為 [**品質**](/windows/win32/api/strmif/ns-strmif-quality)結構的 **時間戳記** 和 **晚期** 成員的總和。</span><span class="sxs-lookup"><span data-stu-id="d9ba4-174">The *rtNow* parameter of **SetNow** is calculated as the sum of the **TimeStamp** and **Late** members of the [**Quality**](/windows/win32/api/strmif/ns-strmif-quality) structure.</span></span>

### <a name="using-the-fiter-in-graphedit"></a><span data-ttu-id="d9ba4-175">在 GraphEdit 中使用 Fiter</span><span class="sxs-lookup"><span data-stu-id="d9ba4-175">Using the Fiter in GraphEdit</span></span>

<span data-ttu-id="d9ba4-176">在 GraphEdit 中，SQL-DMO 包裝函式篩選不會出現在自己的名稱下。</span><span class="sxs-lookup"><span data-stu-id="d9ba4-176">In GraphEdit, the DMO Wrapper filter does not appear under its own name.</span></span> <span data-ttu-id="d9ba4-177">相反地，每個註冊的每個類型都會列在適當的篩選準則類別之下。</span><span class="sxs-lookup"><span data-stu-id="d9ba4-177">Instead, each registered DMO is listed under the appropriate filter category.</span></span> <span data-ttu-id="d9ba4-178">當您透過 [ **插入篩選器** ] 對話方塊來新增時，GraphEdit 會建立一個 []，並將它設定為使用該。</span><span class="sxs-lookup"><span data-stu-id="d9ba4-178">When you add a DMO through the **Insert Filters** dialog, GraphEdit creates the DMO Wrapper filter and configures it to use that DMO.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d9ba4-179">相關主題</span><span class="sxs-lookup"><span data-stu-id="d9ba4-179">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d9ba4-180">DirectShow 篩選</span><span class="sxs-lookup"><span data-stu-id="d9ba4-180">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="d9ba4-181">DirectX 媒體物件</span><span class="sxs-lookup"><span data-stu-id="d9ba4-181">DirectX Media Objects</span></span>](directx-media-objects.md)
</dt> </dl>

 

 
