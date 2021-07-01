---
title: 'WM ASF 寫入器篩選器 (Windows Media Format 11 SDK) '
description: 瞭解適用于 Windows Media Format 11 SDK 的 WM ASF 寫入器篩選器。 查看篩選資訊並查看相關主題。
ms.assetid: a902c92e-836d-492c-b2d2-89c216125774
keywords:
- Windows Media Format SDK，WM ASF 寫入器
- DirectShow、WM ASF 寫入器
- QASF 篩選，WM ASF 寫入器
- WM ASF 寫入器，關於
- Advanced Systems Format (ASF) 、WM ASF 寫入器
- ASF (Advanced Systems Format) ，WM ASF 寫入器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24ee013b55455c3100ee23e076b767d70fb3ffda
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119663"
---
# <a name="wm-asf-writer-filter-windows-media-format-11-sdk"></a><span data-ttu-id="9a7d9-110">WM ASF 寫入器篩選器 (Windows Media Format 11 SDK) </span><span class="sxs-lookup"><span data-stu-id="9a7d9-110">WM ASF Writer Filter (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="9a7d9-111">WM ASF 寫入器篩選器可接受數量不定的輸入資料流程，並建立一個 ASF 檔案。</span><span class="sxs-lookup"><span data-stu-id="9a7d9-111">The WM ASF Writer filter accepts a variable number of input streams and creates an ASF file.</span></span> <span data-ttu-id="9a7d9-112">此篩選器會處理所有的壓縮和多工處理 (雖然可以略過壓縮機制) 。</span><span class="sxs-lookup"><span data-stu-id="9a7d9-112">The filter handles all compression and multiplexing (although the compression mechanism can be bypassed).</span></span> <span data-ttu-id="9a7d9-113">您可以在各種案例中使用 WM ASF 寫入器篩選器，包括數位視訊 (DV) 捕捉、音訊 recompression，以及 Audio-Video 交錯式 (AVI) 或 MPEG 數位媒體檔案來進行網路串流處理的轉換。</span><span class="sxs-lookup"><span data-stu-id="9a7d9-113">You can use the WM ASF Writer filter in various scenarios including digital video (DV) capture, audio recompression, and conversion of Audio-Video Interleaved (AVI) or MPEG digital media files for network streaming.</span></span> <span data-ttu-id="9a7d9-114">此篩選器提供在 DirectShow 中建立 Microsoft Windows Media 音訊和 Windows Media 視訊檔案的唯一方法。</span><span class="sxs-lookup"><span data-stu-id="9a7d9-114">This filter provides the only way to create Microsoft Windows Media Audio and Windows Media Video files in DirectShow.</span></span>

<span data-ttu-id="9a7d9-115">如需詳細資訊，請參閱 [在 DirectShow 中建立 ASF](creating-asf-files-in-directshow.md)檔。</span><span class="sxs-lookup"><span data-stu-id="9a7d9-115">For more information, see [Creating ASF Files in DirectShow](creating-asf-files-in-directshow.md).</span></span>

<span data-ttu-id="9a7d9-116">下表包含有關 WM ASF 寫入器篩選器的資訊，例如它所支援的介面和媒體類型。</span><span class="sxs-lookup"><span data-stu-id="9a7d9-116">The following table contains information about the WM ASF Writer filter, such as the interfaces and media types it supports.</span></span>



| <span data-ttu-id="9a7d9-117">篩選資訊</span><span class="sxs-lookup"><span data-stu-id="9a7d9-117">Filter Information</span></span>                       |  <span data-ttu-id="9a7d9-118">類型</span><span class="sxs-lookup"><span data-stu-id="9a7d9-118">Types</span></span>                                                                                                                                                                                                                       |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a7d9-119">篩選介面</span><span class="sxs-lookup"><span data-stu-id="9a7d9-119">Filter interfaces</span></span>      | <span data-ttu-id="9a7d9-120">**IAMFilterMiscFlags**、 **IBaseFilter**、 **IConfigAsfWriter**、 **IFileSinkFilter2**、IMediaSeeking、IPersistStream、IServiceProvider、ISpecifyPropertyPages、 **IWMIndexer2**、 **IWMHeaderInfo**、 **IWMWriterAdvanced2**</span><span class="sxs-lookup"><span data-stu-id="9a7d9-120">**IAMFilterMiscFlags**, **IBaseFilter**, **IConfigAsfWriter**, **IFileSinkFilter2**, IMediaSeeking, IPersistStream, IServiceProvider, ISpecifyPropertyPages, **IWMIndexer2**, **IWMHeaderInfo**, **IWMWriterAdvanced2**</span></span> |
| <span data-ttu-id="9a7d9-121">輸入 pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="9a7d9-121">Input pin media types</span></span>  | <span data-ttu-id="9a7d9-122">相依于設定檔。</span><span class="sxs-lookup"><span data-stu-id="9a7d9-122">Dependent on the profile.</span></span> <span data-ttu-id="9a7d9-123">一般未壓縮的類型（例如媒體媒體 \_ 或媒體媒體或媒體類型 \_ ），雖然可以在符合設定檔時接受壓縮類型</span><span class="sxs-lookup"><span data-stu-id="9a7d9-123">Typically uncompressed types like MEDIATYPE\_Audio or MEDIATYPE\_Video, although compressed types can be accepted if they match the profile</span></span>                                                   |
| <span data-ttu-id="9a7d9-124">輸入 pin 介面</span><span class="sxs-lookup"><span data-stu-id="9a7d9-124">Input pin interfaces</span></span>   | <span data-ttu-id="9a7d9-125">**IPin**、 **IMemInputPin**、 **IAMStreamConfig**、 **IServiceProvider**、 **IAMWMBufferPass**、 **IWMStreamConfig2** (到 **IServiceProvider**) </span><span class="sxs-lookup"><span data-stu-id="9a7d9-125">**IPin**, **IMemInputPin**, **IAMStreamConfig**, **IServiceProvider**, **IAMWMBufferPass**, **IWMStreamConfig2** (through **IServiceProvider**)</span></span>                                                                         |
| <span data-ttu-id="9a7d9-126">輸出 pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="9a7d9-126">Output pin media types</span></span> | <span data-ttu-id="9a7d9-127">不適用</span><span class="sxs-lookup"><span data-stu-id="9a7d9-127">Not applicable</span></span>                                                                                                                                                                                                          |
| <span data-ttu-id="9a7d9-128">輸出 pin 介面</span><span class="sxs-lookup"><span data-stu-id="9a7d9-128">Output pin interfaces</span></span>  | <span data-ttu-id="9a7d9-129">不適用</span><span class="sxs-lookup"><span data-stu-id="9a7d9-129">Not applicable</span></span>                                                                                                                                                                                                          |
| <span data-ttu-id="9a7d9-130">篩選 CLSID</span><span class="sxs-lookup"><span data-stu-id="9a7d9-130">Filter CLSID</span></span>           | <span data-ttu-id="9a7d9-131">CLSID \_ WMAsfWriter</span><span class="sxs-lookup"><span data-stu-id="9a7d9-131">CLSID\_WMAsfWriter</span></span>                                                                                                                                                                                                      |
| <span data-ttu-id="9a7d9-132">屬性頁 CLSID</span><span class="sxs-lookup"><span data-stu-id="9a7d9-132">Property page CLSID</span></span>    | <span data-ttu-id="9a7d9-133">CLSID \_ WMAsfWriterProperties</span><span class="sxs-lookup"><span data-stu-id="9a7d9-133">CLSID\_WMAsfWriterProperties</span></span>                                                                                                                                                                                            |
| <span data-ttu-id="9a7d9-134">可執行檔</span><span class="sxs-lookup"><span data-stu-id="9a7d9-134">Executable</span></span>             | <span data-ttu-id="9a7d9-135">Qasf.dll</span><span class="sxs-lookup"><span data-stu-id="9a7d9-135">Qasf.dll</span></span>                                                                                                                                                                                                                |
| <span data-ttu-id="9a7d9-136">優點</span><span class="sxs-lookup"><span data-stu-id="9a7d9-136">Merit</span></span>                  | <span data-ttu-id="9a7d9-137">\_ \_ 未 \_ 使用的業績</span><span class="sxs-lookup"><span data-stu-id="9a7d9-137">MERIT\_DO\_NOT\_USE</span></span>                                                                                                                                                                                                     |
| <span data-ttu-id="9a7d9-138">篩選準則分類</span><span class="sxs-lookup"><span data-stu-id="9a7d9-138">Filter Category</span></span>        | <span data-ttu-id="9a7d9-139">未指定</span><span class="sxs-lookup"><span data-stu-id="9a7d9-139">Not specified</span></span>                                                                                                                                                                                                           |



 

## <a name="remarks"></a><span data-ttu-id="9a7d9-140">備註</span><span class="sxs-lookup"><span data-stu-id="9a7d9-140">Remarks</span></span>

<span data-ttu-id="9a7d9-141">篩選器上的輸入 pin 數目取決於傳遞給篩選器的設定檔。</span><span class="sxs-lookup"><span data-stu-id="9a7d9-141">The number of input pins on the filter depends on the profile that is passed to the filter.</span></span> <span data-ttu-id="9a7d9-142">針對設定檔中定義的每個資料流程，各建立一個適當媒體類型的 pin。</span><span class="sxs-lookup"><span data-stu-id="9a7d9-142">One pin of the appropriate media type is created for each stream defined in the profile.</span></span>

<span data-ttu-id="9a7d9-143">輸入 pin 支援來自 **IAMStreamConfig** 介面的一種方法： **IAMStreamConfig：： >iformatprovider.getformat**。</span><span class="sxs-lookup"><span data-stu-id="9a7d9-143">The input pins support one method from the **IAMStreamConfig** interface: **IAMStreamConfig::GetFormat**.</span></span> <span data-ttu-id="9a7d9-144">所有其他方法都會傳回 E \_ >notimpl。</span><span class="sxs-lookup"><span data-stu-id="9a7d9-144">All other methods return E\_NOTIMPL.</span></span> <span data-ttu-id="9a7d9-145">呼叫 **>iformatprovider.getformat** 方法來查詢釘選的目的地壓縮格式，此格式是由目前的設定檔所定義。</span><span class="sxs-lookup"><span data-stu-id="9a7d9-145">Call the **GetFormat** method to query the pin's destination compression format, which is defined by the current profile.</span></span> <span data-ttu-id="9a7d9-146">使用 [**IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85)) 介面設定設定檔。</span><span class="sxs-lookup"><span data-stu-id="9a7d9-146">Use the [**IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85)) interface to set the profile.</span></span>

<span data-ttu-id="9a7d9-147">篩選器的 **IServiceProvider** 介面可讓應用程式取出 [**IWMWriterAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced2) 介面，此介面定義于 Windows Media 格式 SDK 中。</span><span class="sxs-lookup"><span data-stu-id="9a7d9-147">The filter's **IServiceProvider** interface enables applications to retrieve the [**IWMWriterAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced2) interface, which is defined in the Windows Media Format SDK.</span></span> <span data-ttu-id="9a7d9-148">**IWMWriterAdvanced2** 介面會控制 video 去交錯，而且如果輸入是 [*交錯*](wmformat-glossary.md)式來源（例如 DV (數位視訊) ，就很有用）。</span><span class="sxs-lookup"><span data-stu-id="9a7d9-148">The **IWMWriterAdvanced2** interface controls video deinterlacing, and is useful if the input is an [*interlaced*](wmformat-glossary.md) source, such as DV (digital video).</span></span> <span data-ttu-id="9a7d9-149">使用 **GetInputSetting** 和 **SetInputSetting** 方法來控制去交錯。</span><span class="sxs-lookup"><span data-stu-id="9a7d9-149">Use the **GetInputSetting** and **SetInputSetting** methods to control deinterlacing.</span></span> <span data-ttu-id="9a7d9-150">不建議用戶端使用此介面上的任何其他方法。</span><span class="sxs-lookup"><span data-stu-id="9a7d9-150">It is not recommended that clients use any of the other methods on this interface.</span></span> <span data-ttu-id="9a7d9-151">只有將篩選準則加入至篩選圖形之後，才能取得這個介面。</span><span class="sxs-lookup"><span data-stu-id="9a7d9-151">This interface can only be obtained after the filter has been added to the filter graph.</span></span> <span data-ttu-id="9a7d9-152">下列範例顯示如何查詢此介面：</span><span class="sxs-lookup"><span data-stu-id="9a7d9-152">The following example shows how to query for this interface:</span></span>


```C++
// Assume that m_pGraph is a valid IGraphBuilder interface pointer,
// and that pAsfWriter points to the IBaseFilter interface
// on the WM ASF Writer filter.

IServiceProvider *pProvider = NULL;
IWMWriterAdvanced2 *pWMWA2 = NULL;

hr = m_pGraph->AddFilter(pAsfWriter, L"WM ASF Writer");
...
hr = pAsfWriter->QueryInterface(IID_IServiceProvider, (void**)&pProvider)
if (SUCCEEDED(hr))
{
    hr = pProvider->QueryService(IID_IWMWriterAdvanced2,
        IID_IWMWriterAdvanced2, (void**)&pWMWA2);
    pProvider->Release();
}

```



## <a name="related-topics"></a><span data-ttu-id="9a7d9-153">相關主題</span><span class="sxs-lookup"><span data-stu-id="9a7d9-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9a7d9-154">**DirectShow QASF 參考**</span><span class="sxs-lookup"><span data-stu-id="9a7d9-154">**DirectShow QASF Reference**</span></span>](directshow-qasf-reference.md)
</dt> </dl>

 

 
