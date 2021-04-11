---
title: '在 DirectShow 中讀取 ASF 檔案 (Windows Media Format 11 SDK) '
description: 在 DirectShow 中讀取 ASF 檔案
ms.assetid: eec2c91f-1762-4798-91d0-d68ec2160d6a
keywords:
- Windows Media Format SDK、DirectShow
- Windows Media Format SDK，讀取 ASF 檔案
- Windows Media Format SDK，WM ASF 讀取器篩選器
- Windows Media Format SDK，IMediaSeeking 介面
- Advanced Systems Format (ASF) 、DirectShow
- ASF (Advanced Systems Format) ，DirectShow
- Advanced Systems Format (ASF) ，讀取檔案
- ASF (Advanced Systems Format) ，讀取檔案
- Advanced Systems Format (ASF) 、WM ASF 讀取器篩選器
- ASF (Advanced Systems Format) 、WM ASF Reader 篩選器
- Advanced Systems Format (ASF) ，IMediaSeeking 介面
- ASF (Advanced Systems Format) ，IMediaSeeking 介面
- DirectShow，讀取 ASF 檔案
- DirectShow、WM ASF 讀取器篩選器
- DirectShow、IMediaSeeking 介面
- WM ASF 讀取器篩選器
- IMediaSeeking
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1ddf7ba34444f4a3b46f4413958bd26ba4bafc8
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104317035"
---
# <a name="reading-asf-files-in-directshow-windows-media-format-11-sdk"></a><span data-ttu-id="e81de-120">在 DirectShow 中讀取 ASF 檔案 (Windows Media Format 11 SDK) </span><span class="sxs-lookup"><span data-stu-id="e81de-120">Reading ASF Files in DirectShow (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="e81de-121">ASF 檔案的播放是由 [WM Asf 讀取](wm-asf-reader-filter.md) 器篩選器所處理。</span><span class="sxs-lookup"><span data-stu-id="e81de-121">Playback of ASF files is handled by the [WM ASF Reader](wm-asf-reader-filter.md) filter.</span></span> <span data-ttu-id="e81de-122">當 WM ASF 讀取器讀取檔案時，它會自動建立每個資料流程的輸出針腳，包括 Web 資料流程、指令碼命令資料流程，以及任何其他類型的任意資料流程。</span><span class="sxs-lookup"><span data-stu-id="e81de-122">When the WM ASF Reader reads a file, it automatically creates an output pin for each stream, including Web streams, script command streams, and any other type of arbitrary stream.</span></span> <span data-ttu-id="e81de-123">如果是多位元率檔案，則只會針對目前選取的資料流程建立 pin。</span><span class="sxs-lookup"><span data-stu-id="e81de-123">In the case of multiple bit rate files, pins are created only for the currently selected streams.</span></span>

<span data-ttu-id="e81de-124">WM ASF 讀取器支援 DirectShow **IMediaSeeking** 介面，可讓應用程式在檔案內執行時態搜尋。</span><span class="sxs-lookup"><span data-stu-id="e81de-124">The WM ASF Reader supports the DirectShow **IMediaSeeking** interface, which enables applications to perform temporal seeking within the file.</span></span> <span data-ttu-id="e81de-125">但是，不支援以 **IMediaSeeking：： SetRate**) 中所指定的 1.0 (速度來播放。</span><span class="sxs-lookup"><span data-stu-id="e81de-125">However, playback at speeds other than 1.0 (as specified in **IMediaSeeking::SetRate**) is not supported.</span></span>

<span data-ttu-id="e81de-126">篩選準則也會公開數個 Windows Media 格式 SDK 介面，如下表所述。</span><span class="sxs-lookup"><span data-stu-id="e81de-126">The filter also exposes several Windows Media Format SDK interfaces as described in the following table.</span></span>



| <span data-ttu-id="e81de-127">介面</span><span class="sxs-lookup"><span data-stu-id="e81de-127">Interface</span></span>                                        | <span data-ttu-id="e81de-128">公開的方式</span><span class="sxs-lookup"><span data-stu-id="e81de-128">How exposed</span></span>                            | <span data-ttu-id="e81de-129">註解</span><span class="sxs-lookup"><span data-stu-id="e81de-129">Comments</span></span>                                                                                                                                                                                    |
|--------------------------------------------------|----------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e81de-130">**IWMDRMReader**</span><span class="sxs-lookup"><span data-stu-id="e81de-130">**IWMDRMReader**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader)             | <span data-ttu-id="e81de-131">透過篩選器上的 **IServiceProvider**</span><span class="sxs-lookup"><span data-stu-id="e81de-131">Through **IServiceProvider** on filter</span></span> | <span data-ttu-id="e81de-132">適用于需要播放由數位 Rights Management (DRM) 所保護之內容的應用程式。</span><span class="sxs-lookup"><span data-stu-id="e81de-132">Provided for applications that need to play content protected by Digital Rights Management (DRM).</span></span> <span data-ttu-id="e81de-133">這個介面也可以用來直接取得讀取器物件上的其他介面。</span><span class="sxs-lookup"><span data-stu-id="e81de-133">This interface can also be used to obtain other interfaces on the Reader Object directly.</span></span> |
| [<span data-ttu-id="e81de-134">**IWMHeaderInfo**</span><span class="sxs-lookup"><span data-stu-id="e81de-134">**IWMHeaderInfo**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)           | <span data-ttu-id="e81de-135">篩選上的 **QueryInterface**</span><span class="sxs-lookup"><span data-stu-id="e81de-135">**QueryInterface** on filter</span></span>           | <span data-ttu-id="e81de-136">提供讓應用程式可以讀取檔案和內容屬性，以及標記和腳本資訊和中繼資料。</span><span class="sxs-lookup"><span data-stu-id="e81de-136">Provided so that applications can read file and content attributes, as well as marker and script information and metadata.</span></span>                                                                  |
| [<span data-ttu-id="e81de-137">**IWMReaderAdvanced**</span><span class="sxs-lookup"><span data-stu-id="e81de-137">**IWMReaderAdvanced**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced)   | <span data-ttu-id="e81de-138">篩選上的 **QueryInterface**</span><span class="sxs-lookup"><span data-stu-id="e81de-138">**QueryInterface** on filter</span></span>           | <span data-ttu-id="e81de-139">部分實作為篩選準則，讓應用程式可以存取 WM 讀取器物件上的資訊方法。</span><span class="sxs-lookup"><span data-stu-id="e81de-139">Partially implemented on the filter so that applications can access the informational methods on the WM Reader object.</span></span>                                                                      |
| [<span data-ttu-id="e81de-140">**IWMReaderAdvanced2**</span><span class="sxs-lookup"><span data-stu-id="e81de-140">**IWMReaderAdvanced2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) | <span data-ttu-id="e81de-141">篩選上的 **QueryInterface**</span><span class="sxs-lookup"><span data-stu-id="e81de-141">**QueryInterface** on filter</span></span>           | <span data-ttu-id="e81de-142">部分實作為篩選器，讓應用程式可以存取 Reader 物件上的參考方法。</span><span class="sxs-lookup"><span data-stu-id="e81de-142">Partially implemented on the filter so that applications can access the informational methods on the Reader Object.</span></span>                                                                         |



 

<span data-ttu-id="e81de-143">已先將 [WM ASF 讀取](wm-asf-reader-filter.md) 器篩選器提供給 DirectShow 8.0。</span><span class="sxs-lookup"><span data-stu-id="e81de-143">The [WM ASF Reader](wm-asf-reader-filter.md) filter was first made available in DirectShow 8.0.</span></span> <span data-ttu-id="e81de-144">DirectShow 8.1 和9.0 隨附的篩選版本支援第7版。Windows Media 格式 SDK *x* 。</span><span class="sxs-lookup"><span data-stu-id="e81de-144">The version of the filter that ships with DirectShow 8.1 and 9.0 supports version 7.*x* of the Windows Media Format SDK.</span></span> <span data-ttu-id="e81de-145">最新版本的篩選器和其他 QASF 元件會隨附于並支援 Windows Media Format 9 系列 SDK 和更新版本，並取代 DirectX 9.0 中的篩選器。</span><span class="sxs-lookup"><span data-stu-id="e81de-145">The most recent version of the filter, along with the other QASF components, ships with and supports the Windows Media Format 9 Series SDK, and later versions, and it supersedes the filter in DirectX 9.0.</span></span> <span data-ttu-id="e81de-146">如果您在安裝 DirectX 8 之後安裝 Windows Media Format SDK。*x* 或9。*x* SDK，您將會以9系列版本覆寫 qasf.dll 的 DirectX 版本。</span><span class="sxs-lookup"><span data-stu-id="e81de-146">If you install the Windows Media Format SDK after installing the DirectX 8.*x* or 9.*x* SDK, you will overwrite the DirectX version of qasf.dll with the 9 Series version.</span></span> <span data-ttu-id="e81de-147">這應該不會顯示任何問題，但可能在某個情況下，可能會導致 DirectShow **IGraphBuilder：： RenderFile** 方法中有不同的行為。</span><span class="sxs-lookup"><span data-stu-id="e81de-147">This should not present any problems except possibly in one scenario where it will result in different behavior in the DirectShow **IGraphBuilder::RenderFile** method.</span></span> <span data-ttu-id="e81de-148">WM ASF 讀取器的 Windows Media Format 9 系列 SDK 版本是 .asf、.wmv 和 .wma 副檔名的預設來源篩選器。</span><span class="sxs-lookup"><span data-stu-id="e81de-148">The Windows Media Format 9 Series SDK version of the WM ASF Reader is the default source filter for the .asf, .wmv, and .wma file name extensions.</span></span> <span data-ttu-id="e81de-149">這表示當指定了這個類型的檔案時，會自動建立 WM ASF 讀取器，並將其加入至篩選圖形中的方法（例如 **IGraphBuilder：： RenderFile** 或 **IGraphBuilder：： AddSourceFilter** ）。</span><span class="sxs-lookup"><span data-stu-id="e81de-149">This means that the WM ASF Reader is automatically created and added to the filter graph by the Filter Graph Manager in methods such as **IGraphBuilder::RenderFile** or **IGraphBuilder::AddSourceFilter** when a file of this type is specified.</span></span> <span data-ttu-id="e81de-150">在 DirectX 9.0 及更早版本，以及 Windows XP Service Pack 1 及更早版本中， **RenderFile** 方法會使用較舊的 Windows Media 來源篩選。</span><span class="sxs-lookup"><span data-stu-id="e81de-150">In DirectX 9.0 and earlier, and Windows XP Service Pack 1 and earlier, the **RenderFile** method uses the older Windows Media Source Filter.</span></span> <span data-ttu-id="e81de-151">維護此行為的目的，是為了確保與使用 Windows Media Player 6.4 的應用程式回溯相容。</span><span class="sxs-lookup"><span data-stu-id="e81de-151">This behavior was maintained to ensure backward compatibility with applications that used the Windows Media Player 6.4.</span></span> <span data-ttu-id="e81de-152">如需舊版 Windows Media 來源篩選器的詳細資訊，請參閱 DirectShow SDK 檔。</span><span class="sxs-lookup"><span data-stu-id="e81de-152">For more information about the legacy Windows Media Source Filter, see the DirectShow SDK Documentation.</span></span>

<span data-ttu-id="e81de-153">若要使用 WM ASF 讀取器以 Windows Media 內容播放 ASF 檔案，三個主要步驟是建立篩選圖形管理員的實例，呼叫 **IGraphBuilder：： RenderFile** 來建立圖形，然後呼叫 **IMediaControl：： Run** 來播放該檔案。</span><span class="sxs-lookup"><span data-stu-id="e81de-153">To play an ASF file with Windows Media–based content using the WM ASF Reader, the three primary steps are to create an instance of the Filter Graph Manager, call **IGraphBuilder::RenderFile** to create the graph, and then call **IMediaControl::Run** to play the file.</span></span> <span data-ttu-id="e81de-154">下列程式碼範例是使用 DirectShow 播放 ASF 檔案的完整程式。</span><span class="sxs-lookup"><span data-stu-id="e81de-154">The following code example is a complete program that plays an ASF file using DirectShow.</span></span> <span data-ttu-id="e81de-155">若要執行此範例，您必須安裝 DirectX SDK，而且必須根據 DirectShow SDK 檔主題「設定組建環境」中的指示來設定您的組建環境。</span><span class="sxs-lookup"><span data-stu-id="e81de-155">To run this example, you must have the DirectX SDK installed and your build environment must be configured according to the instructions in the DirectShow SDK documentation topic "Setting Up the Build Environment."</span></span> <span data-ttu-id="e81de-156">此外，您必須在您的電腦上，于 **RenderFile** 的呼叫中指定檔案。</span><span class="sxs-lookup"><span data-stu-id="e81de-156">Also, you must specify a file on your computer in the call to **RenderFile**.</span></span>


```C++
#include <dshow.h>
#include <stdio.h>

void main(void)
{
    IGraphBuilder *pGraph = NULL;
    IMediaControl *pControl = NULL;
    IMediaEvent   *pEvent = NULL;

    // Initialize the COM library.
    HRESULT hr = CoInitialize(NULL);
    if (FAILED(hr))
    {
        printf("ERROR - Could not initialize COM library");
        return;
    }

    // Create the Filter Graph Manager and query for interfaces.
    hr = CoCreateInstance(CLSID_FilterGraph, NULL, CLSCTX_INPROC_SERVER, 
                        IID_IGraphBuilder, (void **)&pGraph);
    if (FAILED(hr))
    {
        printf("ERROR - Could not create the Filter Graph Manager.");
        return;
    }

    hr = pGraph->QueryInterface(IID_IMediaControl, (void **)&pControl);
    hr = pGraph->QueryInterface(IID_IMediaEvent, (void **)&pEvent);

    // Build the graph. IMPORTANT: Change this string to a file
    // on your system.
    hr = pGraph->RenderFile(L"test.wmv", NULL);
    if (SUCCEEDED(hr))
    {
        // Run the graph.
        hr = pControl->Run();
        if (SUCCEEDED(hr))
        {
            // Wait for completion.
            long evCode;
            pEvent->WaitForCompletion(INFINITE, &evCode);

            // Note: Do not use INFINITE in a real application, because it
            // can block indefinitely.
        }
    }
    pControl->Release();
    pEvent->Release();
    pGraph->Release();
    CoUninitialize();
}

```



<span data-ttu-id="e81de-157">請注意，這個簡單範例的應用程式程式碼絕對不會明確參考 WM ASF 讀取器。</span><span class="sxs-lookup"><span data-stu-id="e81de-157">Note that the application code for this simple example never references the WM ASF Reader specifically.</span></span> <span data-ttu-id="e81de-158">篩選圖形管理員會建立、連線、執行和最後發行該篩選。</span><span class="sxs-lookup"><span data-stu-id="e81de-158">That filter is created, connected, run, and eventually released by the Filter Graph Manager.</span></span> <span data-ttu-id="e81de-159">不過，在許多情況下，您可能會想要先設定 WM ASF 讀取器，再開始播放。</span><span class="sxs-lookup"><span data-stu-id="e81de-159">In many scenarios, however, you may want to configure the WM ASF Reader before beginning playback.</span></span>

 

 




