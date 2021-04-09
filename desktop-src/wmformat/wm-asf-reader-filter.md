---
title: 'WM ASF 讀取器篩選器 (Windows Media Format 11 SDK) '
description: WM ASF 讀取器篩選器
ms.assetid: 3d5ca88a-86bd-4d84-b4f4-782564ced58d
keywords:
- Windows Media Format SDK，WM ASF 讀取器
- DirectShow、WM ASF 讀取器
- QASF 篩選，WM ASF 讀取器
- WM ASF 讀取器
- Advanced Systems Format (ASF) 、WM ASF 讀取器
- ASF (Advanced Systems Format) 、WM ASF 讀取器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e13b7944f45b850a158c9832e174ae5ec7dce4d6
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "103685378"
---
# <a name="wm-asf-reader-filter-windows-media-format-11-sdk"></a><span data-ttu-id="90bd5-109">WM ASF 讀取器篩選器 (Windows Media Format 11 SDK) </span><span class="sxs-lookup"><span data-stu-id="90bd5-109">WM ASF Reader Filter (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="90bd5-110">當提供 ASF 檔案或 URL 的名稱時，WM ASF 讀取器會讀取壓縮的內容、剖析資料流程，並公開每一個的輸出圖釘。</span><span class="sxs-lookup"><span data-stu-id="90bd5-110">When given the name of an ASF file or a URL, the WM ASF Reader reads the compressed content, parses the streams, and exposes an output pin for each one.</span></span> <span data-ttu-id="90bd5-111">此篩選器會將下游連接到 Windows Media 音訊或 Windows Media 視訊 DMOs，以進行解壓縮。</span><span class="sxs-lookup"><span data-stu-id="90bd5-111">This filter connects downstream to the Windows Media Audio or Windows Media Video DMOs, which do the decompression.</span></span> <span data-ttu-id="90bd5-112">如果 ASF 檔案是可搜尋的，則支援搜尋。</span><span class="sxs-lookup"><span data-stu-id="90bd5-112">Seeking is supported if the ASF file is seekable.</span></span> <span data-ttu-id="90bd5-113">WM ASF 讀取器會根據 ASF 檔案中的時間戳記，將時間戳記套用至媒體範例，但不會以任何方式修改時間戳記。</span><span class="sxs-lookup"><span data-stu-id="90bd5-113">The WM ASF Reader applies time stamps to the media samples based on the time stamp in the ASF file, but it does not modify the time stamps in any way.</span></span> <span data-ttu-id="90bd5-114">就內部而言，此篩選器會使用 Windows Media Format reader 物件來讀取 Windows Media 格式的內容。</span><span class="sxs-lookup"><span data-stu-id="90bd5-114">Internally, the filter uses the Windows Media Format reader object to read the Windows Media–based content.</span></span>

> [!Note]  
> <span data-ttu-id="90bd5-115">在 DirectX SDK 中，此篩選器不是 ASF 檔案的預設來源篩選，因此使用該 SDK 時，您不能使用此篩選搭配 **RenderFile** 方法;您必須使用 (CLSID) 的類別識別碼，明確地將它新增至篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="90bd5-115">In the DirectX SDK, this filter is not the default source filter for ASF files, so with that SDK you cannot use this filter with the **RenderFile** method; you must explicitly add it to the filter graph by using its class identifier (CLSID).</span></span> <span data-ttu-id="90bd5-116">此行為與 Windows Media Format SDK 不同。</span><span class="sxs-lookup"><span data-stu-id="90bd5-116">This behavior is different with the Windows Media Format SDK.</span></span> <span data-ttu-id="90bd5-117">當您安裝 Windows Media Format SDK 執行時間程式庫時，會將 WM ASF 讀取器註冊為 ASF 檔案的預設篩選。</span><span class="sxs-lookup"><span data-stu-id="90bd5-117">When you install the Windows Media Format SDK runtime libraries, the WM ASF Reader is registered as the default filter for ASF files.</span></span>

 

<span data-ttu-id="90bd5-118">下表包含有關 WM ASF 讀取器篩選器的資訊，例如它所支援的介面和媒體類型。</span><span class="sxs-lookup"><span data-stu-id="90bd5-118">The following table contains information about the WM ASF Reader filter, such as the interfaces and media types it supports.</span></span>



|                        |                                                                                                                                                                                                                                               |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="90bd5-119">篩選介面</span><span class="sxs-lookup"><span data-stu-id="90bd5-119">Filter interfaces</span></span>      | <span data-ttu-id="90bd5-120">**IBaseFilter**、 **IFileSourceFilter**、 **IServiceProvider**、 **IWMHeaderInfo**、 **IWMReaderAdvanced** (部分實行。</span><span class="sxs-lookup"><span data-stu-id="90bd5-120">**IBaseFilter**, **IFileSourceFilter**, **IServiceProvider**, **IWMHeaderInfo**, **IWMReaderAdvanced** (partially implemented.</span></span> <span data-ttu-id="90bd5-121">請參閱備註。 ) ， **IWMReaderAdvanced2** (部分實行) 、透過 **IServiceProvider** 的 **IWMDRMReader** () </span><span class="sxs-lookup"><span data-stu-id="90bd5-121">See Remarks.), **IWMReaderAdvanced2** (partially implemented), **IWMDRMReader** (through **IServiceProvider**)</span></span> |
| <span data-ttu-id="90bd5-122">輸入 pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="90bd5-122">Input pin media types</span></span>  | <span data-ttu-id="90bd5-123">不適用</span><span class="sxs-lookup"><span data-stu-id="90bd5-123">Not applicable</span></span>                                                                                                                                                                                                                                |
| <span data-ttu-id="90bd5-124">輸入 pin 介面</span><span class="sxs-lookup"><span data-stu-id="90bd5-124">Input pin interfaces</span></span>   | <span data-ttu-id="90bd5-125">不適用</span><span class="sxs-lookup"><span data-stu-id="90bd5-125">Not applicable</span></span>                                                                                                                                                                                                                                |
| <span data-ttu-id="90bd5-126">輸出 pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="90bd5-126">Output pin media types</span></span> | <span data-ttu-id="90bd5-127">媒體媒體、媒體媒體 \_ \_ 、媒體媒體 \_ SCRIPTCOMMAND、媒體媒體 \_ FileTransfer</span><span class="sxs-lookup"><span data-stu-id="90bd5-127">MEDIATYPE\_Video, MEDIATYPE\_Audio, MEDIATYPE\_ScriptCommand, MEDIATYPE\_FileTransfer</span></span>                                                                                                                                                         |
| <span data-ttu-id="90bd5-128">格式類型</span><span class="sxs-lookup"><span data-stu-id="90bd5-128">Format type</span></span>            | <span data-ttu-id="90bd5-129">如果內容是 [*交錯*](wmformat-glossary.md)的，則為 **VIDEOINFOHEADER2** ，否則為 **VIDEOINFOHEADER**</span><span class="sxs-lookup"><span data-stu-id="90bd5-129">**VIDEOINFOHEADER2** if content is [*interlaced*](wmformat-glossary.md), otherwise **VIDEOINFOHEADER**</span></span>                                                                                                                    |
| <span data-ttu-id="90bd5-130">輸出 pin 介面</span><span class="sxs-lookup"><span data-stu-id="90bd5-130">Output pin interfaces</span></span>  | <span data-ttu-id="90bd5-131">**IMediaSeeking**、 **IAMWMBufferPass**、 **IServiceProvider**、 **IWMStreamConfig2** (到 **IServiceProvider**) </span><span class="sxs-lookup"><span data-stu-id="90bd5-131">**IMediaSeeking**, **IAMWMBufferPass**, **IServiceProvider**, **IWMStreamConfig2** (through **IServiceProvider**)</span></span>                                                                                                                             |
| <span data-ttu-id="90bd5-132">篩選 CLSID</span><span class="sxs-lookup"><span data-stu-id="90bd5-132">Filter CLSID</span></span>           | <span data-ttu-id="90bd5-133">CLSID \_ WMAsfReader</span><span class="sxs-lookup"><span data-stu-id="90bd5-133">CLSID\_WMAsfReader</span></span>                                                                                                                                                                                                                            |
| <span data-ttu-id="90bd5-134">屬性頁 CLSID</span><span class="sxs-lookup"><span data-stu-id="90bd5-134">Property Page CLSID</span></span>    | <span data-ttu-id="90bd5-135">沒有屬性頁</span><span class="sxs-lookup"><span data-stu-id="90bd5-135">No property page</span></span>                                                                                                                                                                                                                              |
| <span data-ttu-id="90bd5-136">可執行檔</span><span class="sxs-lookup"><span data-stu-id="90bd5-136">Executable</span></span>             | <span data-ttu-id="90bd5-137">Qasf.dll</span><span class="sxs-lookup"><span data-stu-id="90bd5-137">Qasf.dll</span></span>                                                                                                                                                                                                                                      |
| <span data-ttu-id="90bd5-138">優點</span><span class="sxs-lookup"><span data-stu-id="90bd5-138">Merit</span></span>                  | <span data-ttu-id="90bd5-139">不 \_ 太可能</span><span class="sxs-lookup"><span data-stu-id="90bd5-139">MERIT\_UNLIKELY</span></span>                                                                                                                                                                                                                               |
| <span data-ttu-id="90bd5-140">篩選準則分類</span><span class="sxs-lookup"><span data-stu-id="90bd5-140">Filter Category</span></span>        | <span data-ttu-id="90bd5-141">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="90bd5-141">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                                                                                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="90bd5-142">備註</span><span class="sxs-lookup"><span data-stu-id="90bd5-142">Remarks</span></span>

<span data-ttu-id="90bd5-143">WM ASF 讀取器會部分執行 **IWMReaderAdvanced** 和 **IWMReaderAdvanced2** 介面，以便讓應用程式能夠存取 Reader 物件上的參考方法。</span><span class="sxs-lookup"><span data-stu-id="90bd5-143">The WM ASF Reader partially implements the **IWMReaderAdvanced** and **IWMReaderAdvanced2** interfaces in order to give applications access to the informational methods on the reader object.</span></span> <span data-ttu-id="90bd5-144">篩選準則的執行只會將呼叫傳遞至讀取器物件上的介面。</span><span class="sxs-lookup"><span data-stu-id="90bd5-144">The filter's implementation simply passes the calls through to the interface on the reader object.</span></span> <span data-ttu-id="90bd5-145">因為篩選準則必須具有串流處理常式的完整控制權，所以不會實作為串流方法。</span><span class="sxs-lookup"><span data-stu-id="90bd5-145">The streaming methods are not implemented because the filter must have complete control over the streaming process.</span></span> <span data-ttu-id="90bd5-146">下列 **IWMReaderAdvanced** 和 **IWMReaderAdvanced2** 方法會實作為：</span><span class="sxs-lookup"><span data-stu-id="90bd5-146">The following **IWMReaderAdvanced** and **IWMReaderAdvanced2** methods are implemented:</span></span>

-   [<span data-ttu-id="90bd5-147">**IWMReaderAdvanced::GetStatistics**</span><span class="sxs-lookup"><span data-stu-id="90bd5-147">**IWMReaderAdvanced::GetStatistics**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getstatistics)
-   [<span data-ttu-id="90bd5-148">**IWMReaderAdvanced：： SetClientInfo**</span><span class="sxs-lookup"><span data-stu-id="90bd5-148">**IWMReaderAdvanced::SetClientInfo**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setclientinfo)
-   [<span data-ttu-id="90bd5-149">**IWMReaderAdvanced2::GetBufferProgress**</span><span class="sxs-lookup"><span data-stu-id="90bd5-149">**IWMReaderAdvanced2::GetBufferProgress**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getbufferprogress)
-   [<span data-ttu-id="90bd5-150">**IWMReaderAdvanced2::GetDownloadProgress**</span><span class="sxs-lookup"><span data-stu-id="90bd5-150">**IWMReaderAdvanced2::GetDownloadProgress**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getdownloadprogress)
-   [<span data-ttu-id="90bd5-151">**IWMReaderAdvanced2::GetPlayMode**</span><span class="sxs-lookup"><span data-stu-id="90bd5-151">**IWMReaderAdvanced2::GetPlayMode**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getplaymode)
-   [<span data-ttu-id="90bd5-152">**IWMReaderAdvanced2::GetProtocolName**</span><span class="sxs-lookup"><span data-stu-id="90bd5-152">**IWMReaderAdvanced2::GetProtocolName**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getprotocolname)
-   [<span data-ttu-id="90bd5-153">**IWMReaderAdvanced2::SetLogClientID**</span><span class="sxs-lookup"><span data-stu-id="90bd5-153">**IWMReaderAdvanced2::SetLogClientID**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setlogclientid)
-   [<span data-ttu-id="90bd5-154">**IWMReaderAdvanced2::SetPlayMode**</span><span class="sxs-lookup"><span data-stu-id="90bd5-154">**IWMReaderAdvanced2::SetPlayMode**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setplaymode)

## <a name="related-topics"></a><span data-ttu-id="90bd5-155">相關主題</span><span class="sxs-lookup"><span data-stu-id="90bd5-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="90bd5-156">**DirectShow QASF 參考**</span><span class="sxs-lookup"><span data-stu-id="90bd5-156">**DirectShow QASF Reference**</span></span>](directshow-qasf-reference.md)
</dt> <dt>

[<span data-ttu-id="90bd5-157">**在 DirectShow 中讀取 ASF 檔案**</span><span class="sxs-lookup"><span data-stu-id="90bd5-157">**Reading ASF Files in DirectShow**</span></span>](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 




