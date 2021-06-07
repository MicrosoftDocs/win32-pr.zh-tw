---
title: 'WM ASF 讀取器篩選器 (Windows Media Format 11 SDK) '
description: 瞭解 WM ASF 讀取器篩選器。
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
ms.openlocfilehash: 421ab634a0d68837b22961b37005c5670d73e5fa
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444279"
---
# <a name="wm-asf-reader-filter-windows-media-format-11-sdk"></a><span data-ttu-id="cee07-109">WM ASF 讀取器篩選器 (Windows Media Format 11 SDK) </span><span class="sxs-lookup"><span data-stu-id="cee07-109">WM ASF Reader Filter (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="cee07-110">當提供 ASF 檔案或 URL 的名稱時，WM ASF 讀取器會讀取壓縮的內容、剖析資料流程，並公開每一個的輸出圖釘。</span><span class="sxs-lookup"><span data-stu-id="cee07-110">When given the name of an ASF file or a URL, the WM ASF Reader reads the compressed content, parses the streams, and exposes an output pin for each one.</span></span> <span data-ttu-id="cee07-111">此篩選器會將下游連接到 Windows Media 音訊或 Windows Media 視訊 DMOs，以進行解壓縮。</span><span class="sxs-lookup"><span data-stu-id="cee07-111">This filter connects downstream to the Windows Media Audio or Windows Media Video DMOs, which do the decompression.</span></span> <span data-ttu-id="cee07-112">如果 ASF 檔案是可搜尋的，則支援搜尋。</span><span class="sxs-lookup"><span data-stu-id="cee07-112">Seeking is supported if the ASF file is seekable.</span></span> <span data-ttu-id="cee07-113">WM ASF 讀取器會根據 ASF 檔案中的時間戳記，將時間戳記套用至媒體範例，但不會以任何方式修改時間戳記。</span><span class="sxs-lookup"><span data-stu-id="cee07-113">The WM ASF Reader applies time stamps to the media samples based on the time stamp in the ASF file, but it does not modify the time stamps in any way.</span></span> <span data-ttu-id="cee07-114">就內部而言，此篩選器會使用 Windows Media Format reader 物件來讀取 Windows Media 格式的內容。</span><span class="sxs-lookup"><span data-stu-id="cee07-114">Internally, the filter uses the Windows Media Format reader object to read the Windows Media–based content.</span></span>

> [!Note]  
> <span data-ttu-id="cee07-115">在 DirectX SDK 中，此篩選器不是 ASF 檔案的預設來源篩選，因此使用該 SDK 時，您不能使用此篩選搭配 **RenderFile** 方法;您必須使用 (CLSID) 的類別識別碼，明確地將它新增至篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="cee07-115">In the DirectX SDK, this filter is not the default source filter for ASF files, so with that SDK you cannot use this filter with the **RenderFile** method; you must explicitly add it to the filter graph by using its class identifier (CLSID).</span></span> <span data-ttu-id="cee07-116">此行為與 Windows Media Format SDK 不同。</span><span class="sxs-lookup"><span data-stu-id="cee07-116">This behavior is different with the Windows Media Format SDK.</span></span> <span data-ttu-id="cee07-117">當您安裝 Windows Media Format SDK 執行時間程式庫時，會將 WM ASF 讀取器註冊為 ASF 檔案的預設篩選。</span><span class="sxs-lookup"><span data-stu-id="cee07-117">When you install the Windows Media Format SDK runtime libraries, the WM ASF Reader is registered as the default filter for ASF files.</span></span>

 

<span data-ttu-id="cee07-118">下表包含有關 WM ASF 讀取器篩選器的資訊，例如它所支援的介面和媒體類型。</span><span class="sxs-lookup"><span data-stu-id="cee07-118">The following table contains information about the WM ASF Reader filter, such as the interfaces and media types it supports.</span></span>



|  <span data-ttu-id="cee07-119">篩選資訊</span><span class="sxs-lookup"><span data-stu-id="cee07-119">Filter Information</span></span>                      |  <span data-ttu-id="cee07-120">類型</span><span class="sxs-lookup"><span data-stu-id="cee07-120">Types</span></span>                                                                                                                                                                                                                                             |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cee07-121">篩選介面</span><span class="sxs-lookup"><span data-stu-id="cee07-121">Filter interfaces</span></span>      | <span data-ttu-id="cee07-122">**IBaseFilter**、 **IFileSourceFilter**、 **IServiceProvider**、 **IWMHeaderInfo**、 **IWMReaderAdvanced** (部分實行。</span><span class="sxs-lookup"><span data-stu-id="cee07-122">**IBaseFilter**, **IFileSourceFilter**, **IServiceProvider**, **IWMHeaderInfo**, **IWMReaderAdvanced** (partially implemented.</span></span> <span data-ttu-id="cee07-123">請參閱備註。 ) ， **IWMReaderAdvanced2** (部分實行) 、透過 **IServiceProvider** 的 **IWMDRMReader** () </span><span class="sxs-lookup"><span data-stu-id="cee07-123">See Remarks.), **IWMReaderAdvanced2** (partially implemented), **IWMDRMReader** (through **IServiceProvider**)</span></span> |
| <span data-ttu-id="cee07-124">輸入 pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="cee07-124">Input pin media types</span></span>  | <span data-ttu-id="cee07-125">不適用</span><span class="sxs-lookup"><span data-stu-id="cee07-125">Not applicable</span></span>                                                                                                                                                                                                                                |
| <span data-ttu-id="cee07-126">輸入 pin 介面</span><span class="sxs-lookup"><span data-stu-id="cee07-126">Input pin interfaces</span></span>   | <span data-ttu-id="cee07-127">不適用</span><span class="sxs-lookup"><span data-stu-id="cee07-127">Not applicable</span></span>                                                                                                                                                                                                                                |
| <span data-ttu-id="cee07-128">輸出 pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="cee07-128">Output pin media types</span></span> | <span data-ttu-id="cee07-129">媒體媒體、媒體媒體 \_ \_ 、媒體媒體 \_ SCRIPTCOMMAND、媒體媒體 \_ FileTransfer</span><span class="sxs-lookup"><span data-stu-id="cee07-129">MEDIATYPE\_Video, MEDIATYPE\_Audio, MEDIATYPE\_ScriptCommand, MEDIATYPE\_FileTransfer</span></span>                                                                                                                                                         |
| <span data-ttu-id="cee07-130">格式類型</span><span class="sxs-lookup"><span data-stu-id="cee07-130">Format type</span></span>            | <span data-ttu-id="cee07-131">如果內容是 [*交錯*](wmformat-glossary.md)的，則為 **VIDEOINFOHEADER2** ，否則為 **VIDEOINFOHEADER**</span><span class="sxs-lookup"><span data-stu-id="cee07-131">**VIDEOINFOHEADER2** if content is [*interlaced*](wmformat-glossary.md), otherwise **VIDEOINFOHEADER**</span></span>                                                                                                                    |
| <span data-ttu-id="cee07-132">輸出 pin 介面</span><span class="sxs-lookup"><span data-stu-id="cee07-132">Output pin interfaces</span></span>  | <span data-ttu-id="cee07-133">**IMediaSeeking**、 **IAMWMBufferPass**、 **IServiceProvider**、 **IWMStreamConfig2** (到 **IServiceProvider**) </span><span class="sxs-lookup"><span data-stu-id="cee07-133">**IMediaSeeking**, **IAMWMBufferPass**, **IServiceProvider**, **IWMStreamConfig2** (through **IServiceProvider**)</span></span>                                                                                                                             |
| <span data-ttu-id="cee07-134">篩選 CLSID</span><span class="sxs-lookup"><span data-stu-id="cee07-134">Filter CLSID</span></span>           | <span data-ttu-id="cee07-135">CLSID \_ WMAsfReader</span><span class="sxs-lookup"><span data-stu-id="cee07-135">CLSID\_WMAsfReader</span></span>                                                                                                                                                                                                                            |
| <span data-ttu-id="cee07-136">屬性頁 CLSID</span><span class="sxs-lookup"><span data-stu-id="cee07-136">Property Page CLSID</span></span>    | <span data-ttu-id="cee07-137">沒有屬性頁</span><span class="sxs-lookup"><span data-stu-id="cee07-137">No property page</span></span>                                                                                                                                                                                                                              |
| <span data-ttu-id="cee07-138">可執行檔</span><span class="sxs-lookup"><span data-stu-id="cee07-138">Executable</span></span>             | <span data-ttu-id="cee07-139">Qasf.dll</span><span class="sxs-lookup"><span data-stu-id="cee07-139">Qasf.dll</span></span>                                                                                                                                                                                                                                      |
| <span data-ttu-id="cee07-140">優點</span><span class="sxs-lookup"><span data-stu-id="cee07-140">Merit</span></span>                  | <span data-ttu-id="cee07-141">不 \_ 太可能</span><span class="sxs-lookup"><span data-stu-id="cee07-141">MERIT\_UNLIKELY</span></span>                                                                                                                                                                                                                               |
| <span data-ttu-id="cee07-142">篩選準則分類</span><span class="sxs-lookup"><span data-stu-id="cee07-142">Filter Category</span></span>        | <span data-ttu-id="cee07-143">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="cee07-143">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                                                                                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="cee07-144">備註</span><span class="sxs-lookup"><span data-stu-id="cee07-144">Remarks</span></span>

<span data-ttu-id="cee07-145">WM ASF 讀取器會部分執行 **IWMReaderAdvanced** 和 **IWMReaderAdvanced2** 介面，以便讓應用程式能夠存取 Reader 物件上的參考方法。</span><span class="sxs-lookup"><span data-stu-id="cee07-145">The WM ASF Reader partially implements the **IWMReaderAdvanced** and **IWMReaderAdvanced2** interfaces in order to give applications access to the informational methods on the reader object.</span></span> <span data-ttu-id="cee07-146">篩選準則的執行只會將呼叫傳遞至讀取器物件上的介面。</span><span class="sxs-lookup"><span data-stu-id="cee07-146">The filter's implementation simply passes the calls through to the interface on the reader object.</span></span> <span data-ttu-id="cee07-147">因為篩選準則必須具有串流處理常式的完整控制權，所以不會實作為串流方法。</span><span class="sxs-lookup"><span data-stu-id="cee07-147">The streaming methods are not implemented because the filter must have complete control over the streaming process.</span></span> <span data-ttu-id="cee07-148">下列 **IWMReaderAdvanced** 和 **IWMReaderAdvanced2** 方法會實作為：</span><span class="sxs-lookup"><span data-stu-id="cee07-148">The following **IWMReaderAdvanced** and **IWMReaderAdvanced2** methods are implemented:</span></span>

-   [<span data-ttu-id="cee07-149">**IWMReaderAdvanced::GetStatistics**</span><span class="sxs-lookup"><span data-stu-id="cee07-149">**IWMReaderAdvanced::GetStatistics**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getstatistics)
-   [<span data-ttu-id="cee07-150">**IWMReaderAdvanced：： SetClientInfo**</span><span class="sxs-lookup"><span data-stu-id="cee07-150">**IWMReaderAdvanced::SetClientInfo**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setclientinfo)
-   [<span data-ttu-id="cee07-151">**IWMReaderAdvanced2::GetBufferProgress**</span><span class="sxs-lookup"><span data-stu-id="cee07-151">**IWMReaderAdvanced2::GetBufferProgress**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getbufferprogress)
-   [<span data-ttu-id="cee07-152">**IWMReaderAdvanced2::GetDownloadProgress**</span><span class="sxs-lookup"><span data-stu-id="cee07-152">**IWMReaderAdvanced2::GetDownloadProgress**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getdownloadprogress)
-   [<span data-ttu-id="cee07-153">**IWMReaderAdvanced2::GetPlayMode**</span><span class="sxs-lookup"><span data-stu-id="cee07-153">**IWMReaderAdvanced2::GetPlayMode**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getplaymode)
-   [<span data-ttu-id="cee07-154">**IWMReaderAdvanced2::GetProtocolName**</span><span class="sxs-lookup"><span data-stu-id="cee07-154">**IWMReaderAdvanced2::GetProtocolName**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getprotocolname)
-   [<span data-ttu-id="cee07-155">**IWMReaderAdvanced2::SetLogClientID**</span><span class="sxs-lookup"><span data-stu-id="cee07-155">**IWMReaderAdvanced2::SetLogClientID**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setlogclientid)
-   [<span data-ttu-id="cee07-156">**IWMReaderAdvanced2::SetPlayMode**</span><span class="sxs-lookup"><span data-stu-id="cee07-156">**IWMReaderAdvanced2::SetPlayMode**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setplaymode)

## <a name="related-topics"></a><span data-ttu-id="cee07-157">相關主題</span><span class="sxs-lookup"><span data-stu-id="cee07-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cee07-158">**DirectShow QASF 參考**</span><span class="sxs-lookup"><span data-stu-id="cee07-158">**DirectShow QASF Reference**</span></span>](directshow-qasf-reference.md)
</dt> <dt>

[<span data-ttu-id="cee07-159">**在 DirectShow 中讀取 ASF 檔案**</span><span class="sxs-lookup"><span data-stu-id="cee07-159">**Reading ASF Files in DirectShow**</span></span>](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 




