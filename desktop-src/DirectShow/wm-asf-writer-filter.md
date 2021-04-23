---
description: WM ASF 寫入器篩選器
ms.assetid: 1b12f65f-8d77-4d38-aad9-92bb15cc0426
title: 'WM ASF 寫入器篩選器 (DirectShow) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bf09a99673b07e88198fd57b95a766ce821eb02
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909276"
---
# <a name="wm-asf-writer-filter-directshow"></a><span data-ttu-id="e907f-103">WM ASF 寫入器篩選器 (DirectShow) </span><span class="sxs-lookup"><span data-stu-id="e907f-103">WM ASF Writer Filter (DirectShow)</span></span>

<span data-ttu-id="e907f-104">WM ASF 寫入器是 Windows Media™ Format SDK 所提供之寫入器物件的包裝函式篩選。</span><span class="sxs-lookup"><span data-stu-id="e907f-104">The WM ASF Writer is a wrapper filter for the writer object provided with the Windows Media™ Format SDK.</span></span> <span data-ttu-id="e907f-105">篩選器會接受數量不定的輸入資料流程，並建立 Advanced 系統格式 (ASF) 檔。</span><span class="sxs-lookup"><span data-stu-id="e907f-105">The filter accepts a variable number of input streams and creates an Advanced Systems Format (ASF) file.</span></span> <span data-ttu-id="e907f-106">此篩選器會處理所有的壓縮和多工處理 (雖然可以略過壓縮機制) 。</span><span class="sxs-lookup"><span data-stu-id="e907f-106">The filter handles all compression and multiplexing (although the compression mechanism can be bypassed).</span></span> <span data-ttu-id="e907f-107">您可以在各種案例中使用 WM ASF 寫入器，包括數位視訊 (DV) 捕捉、音訊 recompression，以及 Audio-Video 交錯式 (AVI) 或 MPEG 多媒體檔案的轉換，以進行網路串流處理。</span><span class="sxs-lookup"><span data-stu-id="e907f-107">You can use the WM ASF Writer in various scenarios including digital video (DV) capture, audio recompression, and conversion of Audio-Video Interleaved (AVI) or MPEG multimedia files for network streaming.</span></span> <span data-ttu-id="e907f-108">此篩選器提供在 Microsoft DirectShow 中建立 Microsoft® Windows Media™音訊和 Windows Media 視訊檔案的唯一方法。</span><span class="sxs-lookup"><span data-stu-id="e907f-108">This filter provides the only way to create Microsoft® Windows Media™ Audio and Windows Media Video files in Microsoft DirectShow.</span></span>

<span data-ttu-id="e907f-109">如需詳細資訊，請參閱 [在 DirectShow 中建立 ASF](creating-asf-files-in-directshow.md)檔。</span><span class="sxs-lookup"><span data-stu-id="e907f-109">For more information, see [Creating ASF Files in DirectShow](creating-asf-files-in-directshow.md).</span></span>



| <span data-ttu-id="e907f-110">標籤</span><span class="sxs-lookup"><span data-stu-id="e907f-110">Label</span></span> | <span data-ttu-id="e907f-111">值</span><span class="sxs-lookup"><span data-stu-id="e907f-111">Value</span></span> |
|------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e907f-112">篩選介面</span><span class="sxs-lookup"><span data-stu-id="e907f-112">Filter interfaces</span></span>                        | <span data-ttu-id="e907f-113">[**IAMFilterMiscFlags**](/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags)、 [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)、 [**IConfigAsfWriter**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iconfigasfwriter)、 [**IConfigAsfWriter2**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iconfigasfwriter2)、 [**IFileSinkFilter2**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter2)、 [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)、 **IPersistStream**、 **ISERVICEPROVIDER**、 **ISpecifyPropertyPages**，此外，此篩選器會公開下列 Windows Media 格式 SDK 介面： **IWMIndexer2**、 **IWMHeaderInfo**、 **IWMWriterAdvanced2**</span><span class="sxs-lookup"><span data-stu-id="e907f-113">[**IAMFilterMiscFlags**](/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IConfigAsfWriter**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iconfigasfwriter), [**IConfigAsfWriter2**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iconfigasfwriter2), [**IFileSinkFilter2**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter2), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), **IPersistStream**, **IServiceProvider**, **ISpecifyPropertyPages** In addition, the filter exposes the following Windows Media Format SDK interfaces: **IWMIndexer2**, **IWMHeaderInfo**, **IWMWriterAdvanced2**</span></span><br/> |
| <span data-ttu-id="e907f-114">輸入 pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="e907f-114">Input pin media types</span></span>                    | <span data-ttu-id="e907f-115">相依于 ASF 設定檔。</span><span class="sxs-lookup"><span data-stu-id="e907f-115">Depends on the ASF profile.</span></span> <span data-ttu-id="e907f-116">通常未壓縮的音訊和影片類型，雖然篩選準則會在符合 ASF 設定檔的情況下接受壓縮類型。</span><span class="sxs-lookup"><span data-stu-id="e907f-116">Typically uncompressed audio and video types, although the filter will accept compressed types if they match the ASF profile.</span></span>                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="e907f-117">輸入 pin 介面</span><span class="sxs-lookup"><span data-stu-id="e907f-117">Input pin interfaces</span></span>                     | <span data-ttu-id="e907f-118">[**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig)、 [**IAMWMBufferPass**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iamwmbufferpass)、 [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)、 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)、 **IServiceProvider** 此外，Pin 會公開下列 Windows Media 格式 SDK 介面： **IWMStreamConfig2** (至 **IServiceProvider**) </span><span class="sxs-lookup"><span data-stu-id="e907f-118">[**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**IAMWMBufferPass**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iamwmbufferpass), [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), **IServiceProvider** In addition, the pin exposes the following Windows Media Format SDK interface: **IWMStreamConfig2** (through **IServiceProvider**)</span></span><br/>                                                                                                                                                                                 |
| <span data-ttu-id="e907f-119">輸出 pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="e907f-119">Output pin media types</span></span>                   | <span data-ttu-id="e907f-120">不適用。</span><span class="sxs-lookup"><span data-stu-id="e907f-120">Not applicable.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="e907f-121">輸出 pin 介面</span><span class="sxs-lookup"><span data-stu-id="e907f-121">Output pin interfaces</span></span>                    | <span data-ttu-id="e907f-122">不適用。</span><span class="sxs-lookup"><span data-stu-id="e907f-122">Not applicable.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="e907f-123">篩選 CLSID</span><span class="sxs-lookup"><span data-stu-id="e907f-123">Filter CLSID</span></span>                             | <span data-ttu-id="e907f-124">CLSID \_ WMAsfWriter</span><span class="sxs-lookup"><span data-stu-id="e907f-124">CLSID\_WMAsfWriter</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="e907f-125">屬性頁 CLSID</span><span class="sxs-lookup"><span data-stu-id="e907f-125">Property page CLSID</span></span>                      | <span data-ttu-id="e907f-126">CLSID \_ AsfWriterProperties</span><span class="sxs-lookup"><span data-stu-id="e907f-126">CLSID\_AsfWriterProperties</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="e907f-127">可執行檔</span><span class="sxs-lookup"><span data-stu-id="e907f-127">Executable</span></span>                               | <span data-ttu-id="e907f-128">Qasf.dll</span><span class="sxs-lookup"><span data-stu-id="e907f-128">Qasf.dll</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="e907f-129">優點</span><span class="sxs-lookup"><span data-stu-id="e907f-129">Merit</span></span>](merit.md)                       | <span data-ttu-id="e907f-130">\_ \_ 未 \_ 使用的業績</span><span class="sxs-lookup"><span data-stu-id="e907f-130">MERIT\_DO\_NOT\_USE</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| [<span data-ttu-id="e907f-131">篩選準則分類</span><span class="sxs-lookup"><span data-stu-id="e907f-131">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="e907f-132">未指定</span><span class="sxs-lookup"><span data-stu-id="e907f-132">Not specified</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

## <a name="remarks"></a><span data-ttu-id="e907f-133">備註</span><span class="sxs-lookup"><span data-stu-id="e907f-133">Remarks</span></span>

<span data-ttu-id="e907f-134">篩選器需要 Windows Media Format 軟體發展工具組 (SDK) 及其基礎相依性。</span><span class="sxs-lookup"><span data-stu-id="e907f-134">The filter requires the Windows Media Format Software Development Kit (SDK) and its underlying dependencies.</span></span>

<span data-ttu-id="e907f-135">在 ASF 資料流程的設定檔或設定檔識別碼上，篩選 dependings 上的輸入圖釘數目。</span><span class="sxs-lookup"><span data-stu-id="e907f-135">The number of input pins on the filter dependings on the profile or profile identifier of the ASF stream.</span></span>

<span data-ttu-id="e907f-136">輸入 pin 支援來自 **IAMStreamConfig** 介面的一種方法： [**IAMStreamConfig：： >iformatprovider.getformat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getformat)。</span><span class="sxs-lookup"><span data-stu-id="e907f-136">The input pins support one method from the **IAMStreamConfig** interface: [**IAMStreamConfig::GetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getformat).</span></span> <span data-ttu-id="e907f-137">所有其他方法都會傳回 E \_ >notimpl。</span><span class="sxs-lookup"><span data-stu-id="e907f-137">All other methods return E\_NOTIMPL.</span></span> <span data-ttu-id="e907f-138">呼叫 **>iformatprovider.getformat** 方法來查詢釘選的目的地壓縮格式，此格式是由目前的 ASF 設定檔所定義。</span><span class="sxs-lookup"><span data-stu-id="e907f-138">Call the **GetFormat** method to query the pin's destination compression format, which is defined by the current ASF profile.</span></span> <span data-ttu-id="e907f-139">使用 [**IConfigAsfWriter**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iconfigasfwriter) 介面設定設定檔。</span><span class="sxs-lookup"><span data-stu-id="e907f-139">Use the [**IConfigAsfWriter**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iconfigasfwriter) interface to set the profile.</span></span>

<span data-ttu-id="e907f-140">您可以使用篩選器的 **IServiceProvider** 介面來取得 **IWMWriterAdvanced2** 介面的指標，該介面是在 Windows Media 格式 SDK 中定義。</span><span class="sxs-lookup"><span data-stu-id="e907f-140">You can use the filter's **IServiceProvider** interface to get a pointer to the **IWMWriterAdvanced2** interface, which is defined in the Windows Media Format SDK.</span></span> <span data-ttu-id="e907f-141">您可以使用 **IWMWriterAdvanced2** 介面來控制來源影片交錯時的影片去交錯。</span><span class="sxs-lookup"><span data-stu-id="e907f-141">You can use the **IWMWriterAdvanced2** interface to control video deinterlacing when the source video is interlaced.</span></span> <span data-ttu-id="e907f-142">若要設定去交錯模式，請呼叫 **IWMWriterAdvanced2：： SetInputSetting**。</span><span class="sxs-lookup"><span data-stu-id="e907f-142">To set the deinterlacing mode, call **IWMWriterAdvanced2::SetInputSetting**.</span></span> <span data-ttu-id="e907f-143">針對 *dwInputNum* 參數，請使用影片輸入圖釘以零為基底的索引，如 [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) 介面所列舉。</span><span class="sxs-lookup"><span data-stu-id="e907f-143">For the *dwInputNum* parameter, use the zero-based index of the video input pin, as enumerated by the [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) interface.</span></span>

<span data-ttu-id="e907f-144">下列範例顯示如何查詢此介面：</span><span class="sxs-lookup"><span data-stu-id="e907f-144">The following example shows how to query for this interface:</span></span>


```C++
// Assume that pAsfWriter is a valid IBaseFilter pointer.
IServiceProvider *pProvider = NULL;
IWMWriterAdvanced2 *pWMWA2 = NULL;

hr = pAsfWriter->QueryInterface(
    IID_IServiceProvider, 
    (void**)&pProvider
    );
if (SUCCEEDED(hr))
{
    hr = pProvider->QueryService(
        IID_IWMWriterAdvanced2,
        IID_IWMWriterAdvanced2, 
        (void**)&pWMWA2
        );
    pProvider->Release();
    if (SUCCEEDED(hr))
    {
        // Use pWMWA2. (Not shown.)
        pWMWA2->Release();
    }
}
```



<span data-ttu-id="e907f-145">應用程式不應使用 **IWMWriterAdvanced2** 介面所繼承的任何 **IWMWriterAdvanced** 方法。</span><span class="sxs-lookup"><span data-stu-id="e907f-145">Applications should not use any of the **IWMWriterAdvanced** methods that the **IWMWriterAdvanced2** interface inherits.</span></span> <span data-ttu-id="e907f-146">呼叫任何這些方法時，可以使用篩選準則來 interere。</span><span class="sxs-lookup"><span data-stu-id="e907f-146">Calling any these methods could interere with the operation of the filter.</span></span>

<span data-ttu-id="e907f-147">此篩選器所支援的唯一檔案寫入模式是檔案 \_ \_ 覆寫。</span><span class="sxs-lookup"><span data-stu-id="e907f-147">The only file-writing mode supported by this filter is AM\_FILE\_OVERWRITE.</span></span> <span data-ttu-id="e907f-148">請參閱 [**IFileSinkFilter2：： GetMode**](/windows/desktop/api/Strmif/nf-strmif-ifilesinkfilter2-getmode)。</span><span class="sxs-lookup"><span data-stu-id="e907f-148">See [**IFileSinkFilter2::GetMode**](/windows/desktop/api/Strmif/nf-strmif-ifilesinkfilter2-getmode).</span></span>

<span data-ttu-id="e907f-149">當 Windows Media Format SDK 執行時間將 WMT \_ 狀態訊息傳送至 WM ASF 寫入器篩選器時，篩選器會將它們轉送為 [**EC \_ WMT \_ 事件**](ec-wmt-event.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="e907f-149">When the Windows Media Format SDK runtime sends WMT\_STATUS messages to the WM ASF Writer filter, the filter forwards them as [**EC\_WMT\_EVENT**](ec-wmt-event.md) events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e907f-150">相關主題</span><span class="sxs-lookup"><span data-stu-id="e907f-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e907f-151">DirectShow 篩選</span><span class="sxs-lookup"><span data-stu-id="e907f-151">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 




