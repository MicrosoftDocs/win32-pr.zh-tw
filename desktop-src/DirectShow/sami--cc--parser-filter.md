---
description: " (CC) 剖析器篩選器的薩米文"
ms.assetid: 9b09dd86-3c22-4565-82a0-106d5ca2e42d
title: " (CC) 剖析器篩選器的薩米文"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b77f0aa2d913b7f0295a078c8174ae483bb1cb62
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909676"
---
# <a name="sami-cc-parser-filter"></a><span data-ttu-id="39cec-103"> (CC) 剖析器篩選器的薩米文</span><span class="sxs-lookup"><span data-stu-id="39cec-103">SAMI (CC) Parser Filter</span></span>

<span data-ttu-id="39cec-104">剖析從已同步處理的可存取媒體交換的資料字幕資料 (薩米) 的檔案。</span><span class="sxs-lookup"><span data-stu-id="39cec-104">Parses captioning data from Synchronized Accessible Media Interchange (SAMI) files.</span></span>

<span data-ttu-id="39cec-105">薩米文是類似于 HTML 的文字格式，用於編碼以時間為基礎的標題。</span><span class="sxs-lookup"><span data-stu-id="39cec-105">SAMI is a text format similar to HTML, and is used for encoding time-based captions.</span></span> <span data-ttu-id="39cec-106">此篩選會將薩米的資料轉換成文字資料流程。</span><span class="sxs-lookup"><span data-stu-id="39cec-106">This filter converts SAMI data into a text stream.</span></span> <span data-ttu-id="39cec-107">資料流程中的每個範例都包含一個標題專案，以及格式資訊。</span><span class="sxs-lookup"><span data-stu-id="39cec-107">Each sample in the stream contains one caption entry, along with format information.</span></span> <span data-ttu-id="39cec-108">範例上的時間戳記是從薩米文檔案中的時間資訊產生的。</span><span class="sxs-lookup"><span data-stu-id="39cec-108">The time stamps on the samples are generated from the time information in the SAMI file.</span></span>

<span data-ttu-id="39cec-109">此篩選器的設計目的是要搭配 [內部指令碼命令](internal-script-command-renderer-filter.md) 轉譯器篩選準則使用。</span><span class="sxs-lookup"><span data-stu-id="39cec-109">This filter is designed to be used with the [Internal Script Command Renderer](internal-script-command-renderer-filter.md) filter.</span></span> <span data-ttu-id="39cec-110">內部指令碼命令轉譯器會接收文字範例，並以事件通知的形式將它們傳送至應用程式。</span><span class="sxs-lookup"><span data-stu-id="39cec-110">The Internal Script Command Renderer receives the text samples and sends them to the application, in the form of event notifications.</span></span> <span data-ttu-id="39cec-111">如需詳細資訊，請參閱＜備註＞一節。</span><span class="sxs-lookup"><span data-stu-id="39cec-111">For more information, see the Remarks section.</span></span>



| <span data-ttu-id="39cec-112">標籤</span><span class="sxs-lookup"><span data-stu-id="39cec-112">Label</span></span> | <span data-ttu-id="39cec-113">值</span><span class="sxs-lookup"><span data-stu-id="39cec-113">Value</span></span> |
|------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39cec-114">篩選介面</span><span class="sxs-lookup"><span data-stu-id="39cec-114">Filter Interfaces</span></span>                        | <span data-ttu-id="39cec-115">[**IAMStreamSelect**](/windows/desktop/api/Strmif/nn-strmif-iamstreamselect)、 [ **IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)</span><span class="sxs-lookup"><span data-stu-id="39cec-115">[**IAMStreamSelect**](/windows/desktop/api/Strmif/nn-strmif-iamstreamselect), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)</span></span>                           |
| <span data-ttu-id="39cec-116">輸入 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="39cec-116">Input Pin Media Types</span></span>                    | <span data-ttu-id="39cec-117">媒體媒體的 \_ 串流</span><span class="sxs-lookup"><span data-stu-id="39cec-117">MEDIATYPE\_Stream</span></span>                                                                                        |
| <span data-ttu-id="39cec-118">輸入 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="39cec-118">Input Pin Interfaces</span></span>                     | <span data-ttu-id="39cec-119">[**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)、 [ **IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="39cec-119">[**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                         |
| <span data-ttu-id="39cec-120">輸出 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="39cec-120">Output Pin Media Types</span></span>                   | <span data-ttu-id="39cec-121">媒體 \_ 文字、MEDIASUBTYPE \_ Null</span><span class="sxs-lookup"><span data-stu-id="39cec-121">MEDIATYPE\_Text, MEDIASUBTYPE\_NULL</span></span>                                                                      |
| <span data-ttu-id="39cec-122">輸出 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="39cec-122">Output Pin Interfaces</span></span>                    | <span data-ttu-id="39cec-123">[**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)、 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)、 [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="39cec-123">[**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span> |
| <span data-ttu-id="39cec-124">篩選 CLSID</span><span class="sxs-lookup"><span data-stu-id="39cec-124">Filter CLSID</span></span>                             | <span data-ttu-id="39cec-125">{33FACFE0-A9BE-11D0-A520-00A0D10129C0}</span><span class="sxs-lookup"><span data-stu-id="39cec-125">{33FACFE0-A9BE-11D0-A520-00A0D10129C0}</span></span>                                                                   |
| <span data-ttu-id="39cec-126">屬性頁 CLSID</span><span class="sxs-lookup"><span data-stu-id="39cec-126">Property Page CLSID</span></span>                      | <span data-ttu-id="39cec-127">沒有屬性頁</span><span class="sxs-lookup"><span data-stu-id="39cec-127">No property page</span></span>                                                                                         |
| <span data-ttu-id="39cec-128">可執行檔</span><span class="sxs-lookup"><span data-stu-id="39cec-128">Executable</span></span>                               | <span data-ttu-id="39cec-129">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="39cec-129">quartz.dll</span></span>                                                                                               |
| [<span data-ttu-id="39cec-130">優點</span><span class="sxs-lookup"><span data-stu-id="39cec-130">Merit</span></span>](merit.md)                       | <span data-ttu-id="39cec-131">不 \_ 太可能</span><span class="sxs-lookup"><span data-stu-id="39cec-131">MERIT\_UNLIKELY</span></span>                                                                                          |
| [<span data-ttu-id="39cec-132">篩選準則分類</span><span class="sxs-lookup"><span data-stu-id="39cec-132">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="39cec-133">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="39cec-133">CLSID\_LegacyAmFilterCategory</span></span>                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="39cec-134">備註</span><span class="sxs-lookup"><span data-stu-id="39cec-134">Remarks</span></span>

<span data-ttu-id="39cec-135">以下是一個簡單的薩米文檔案：</span><span class="sxs-lookup"><span data-stu-id="39cec-135">The following is a simple SAMI file:</span></span>


```C++
<SAMI>
<Head>
<STYLE TYPE="text/css"> <!--
    .ENCC {Name: English; lang:en-US; SAMI_TYPE: CC;}
    .FRCC {Name: French; lang:fr-FR; SAMI_TYPE: CC;}
    #NORMAL {Name: Normal; font-family: arial;}
    #GREENTEXT {Name: GreenText; color:green; font-family: verdana;}
-->
</STYLE>
</Head>
<BODY>
<Sync Start=1000>
    <P CLASS="ENCC">One
    <P CLASS="FRCC">Un

<Sync Start=2000>
    <P CLASS="ENCC">Two
    <P CLASS="FRCC">Deux

<Sync Start=3000>
    <P CLASS="ENCC">Three
    <P CLASS="FRCC">Trois
</BODY>
</SAMI>
```



<span data-ttu-id="39cec-136">**STYLE** 標記會定義兩種語言設定：英文 (。ENCC) 和法文 (。FRCC) 。</span><span class="sxs-lookup"><span data-stu-id="39cec-136">The **STYLE** tag defines two language settings, English (.ENCC) and French (.FRCC).</span></span> <span data-ttu-id="39cec-137">它也會定義兩種樣式： \# 標準和 \# GREENTEXT。</span><span class="sxs-lookup"><span data-stu-id="39cec-137">It also defines two styles, \#NORMAL and \#GREENTEXT.</span></span> <span data-ttu-id="39cec-138">每個 **同步** 標記會定義標題的開始時間（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="39cec-138">Each **SYNC** tag defines the start time for a caption, in milliseconds.</span></span> <span data-ttu-id="39cec-139">**P** 標記包含標題文字，而 **類別** 屬性則會指定要套用標題的語言設定。</span><span class="sxs-lookup"><span data-stu-id="39cec-139">The **P** tags contain the caption text, while the **CLASS** attribute specifies the language setting to which the caption applies.</span></span>

<span data-ttu-id="39cec-140">針對每個語言和樣式，此篩選準則會建立邏輯資料流程。</span><span class="sxs-lookup"><span data-stu-id="39cec-140">For each language and style, the filter creates a logical stream.</span></span> <span data-ttu-id="39cec-141">在任何時候，都只會啟用一個語言資料流程和一個樣式資料流程。</span><span class="sxs-lookup"><span data-stu-id="39cec-141">At any time, exactly one language stream and one style stream are enabled.</span></span> <span data-ttu-id="39cec-142">當篩選準則產生範例時，它會選取目前語言的標題，並套用目前的樣式。</span><span class="sxs-lookup"><span data-stu-id="39cec-142">When the filter generates a sample, it selects the caption for the current language and applies the current style.</span></span> <span data-ttu-id="39cec-143">預設會啟用在檔案中宣告的第一個語言和樣式。</span><span class="sxs-lookup"><span data-stu-id="39cec-143">By default, the first language and style declared in the file are enabled.</span></span> <span data-ttu-id="39cec-144">應用程式可以使用 [**IAMStreamSelect：： enable**](/windows/desktop/api/Strmif/nf-strmif-iamstreamselect-enable) 方法來啟用不同的資料流程。</span><span class="sxs-lookup"><span data-stu-id="39cec-144">An application can use the [**IAMStreamSelect::Enable**](/windows/desktop/api/Strmif/nf-strmif-iamstreamselect-enable) method to enable a different stream.</span></span>

<span data-ttu-id="39cec-145">使用預設設定時，範例檔案中的第一個標題會產生下列輸出：</span><span class="sxs-lookup"><span data-stu-id="39cec-145">With the default settings, the first caption in the example file produces the following output:</span></span>


```C++
<P STYLE=" Name: English; lang:en-US; SAMI_TYPE: CC; Name: Normal; font-family: arial;">One
```



<span data-ttu-id="39cec-146">如果輸出移至內部指令碼命令轉譯器，則該篩選準則會傳送 [**EC \_ OLE \_ 事件**](ec-ole-event.md) 事件通知。</span><span class="sxs-lookup"><span data-stu-id="39cec-146">If the output goes to the Internal Script Command Renderer, that filter sends an [**EC\_OLE\_EVENT**](ec-ole-event.md) event notification.</span></span> <span data-ttu-id="39cec-147">第二個事件參數是具有標題文字的 BSTR。</span><span class="sxs-lookup"><span data-stu-id="39cec-147">The second event parameter is a BSTR with the caption text.</span></span> <span data-ttu-id="39cec-148">應用程式可以取出事件並顯示標題。</span><span class="sxs-lookup"><span data-stu-id="39cec-148">The application can retrieve the event and display the caption.</span></span>

<span data-ttu-id="39cec-149">下列範例顯示如何轉譯薩米文的檔案、取出串流資訊、啟用資料流程，以及顯示標題文字。</span><span class="sxs-lookup"><span data-stu-id="39cec-149">The following example shows how to render a SAMI file, retrieve stream information, enable streams, and display caption text.</span></span> <span data-ttu-id="39cec-150">此範例假設先前的薩米文檔案儲存為 C： \\ 薩米文的 \_ 測試檔案 \_ 。</span><span class="sxs-lookup"><span data-stu-id="39cec-150">The example assumes that the previous SAMI file is saved as C:\\Sami\_test\_file.sami.</span></span>

<span data-ttu-id="39cec-151">為了簡潔起見，此範例會在呼叫 **IAMStreamSelect：： Enable** 方法時使用硬式編碼的資料流程索引。</span><span class="sxs-lookup"><span data-stu-id="39cec-151">For brevity, this example used hard-coded stream indexes when it calls the **IAMStreamSelect::Enable** method.</span></span> <span data-ttu-id="39cec-152">它也會執行基本的錯誤檢查。</span><span class="sxs-lookup"><span data-stu-id="39cec-152">It also performs minimal error checking.</span></span>


```C++
void __cdecl main()
{
    HRESULT hr;
    IGraphBuilder *pGraph;
    IMediaControl *pMediaControl;
    IMediaEventEx *pEv;
    IBaseFilter   *pSAMI;

    CoInitialize(NULL);
    
    // Create the filter graph manager.
    CoCreateInstance(CLSID_FilterGraph, NULL, CLSCTX_INPROC, 
                        IID_IGraphBuilder, (void **)&pGraph);
    pGraph->QueryInterface(IID_IMediaControl, (void **)&pMediaControl);
    pGraph->QueryInterface(IID_IMediaEventEx, (void**)&pEv);

    // Create the graph and find the SAMI parser.
    pGraph->RenderFile(L"C:\\Sami_test_file.sami", NULL);
    hr = pGraph->FindFilterByName(L"SAMI (CC) Parser", &pSAMI);
    if (SUCCEEDED(hr)) 
    {
        IAMStreamSelect *pStrm = NULL;
        hr = pSAMI->QueryInterface(IID_IAMStreamSelect, (void**)&pStrm);
        if (SUCCEEDED(hr)) 
        {
            DWORD dwStreams = 0;
            pStrm->Count(&dwStreams);
            printf("Stream count: %d\n", dwStreams);

            // Select French and "GreenText"
            hr = pStrm->Enable(1, AMSTREAMSELECTENABLE_ENABLE);
            hr = pStrm->Enable(3, AMSTREAMSELECTENABLE_ENABLE);

            // Print the name of each logical stream.
            for (DWORD index = 0; index < dwStreams; index++)
            {
                DWORD dwFlags;
                WCHAR *wszName;
                hr = pStrm->Info(index, NULL, &dwFlags, NULL, NULL,
                    &wszName, NULL, NULL);
                if (hr == S_OK)
                {
                    wprintf(L"Stream %d: %s [%s]\n", index, wszName, 
                        (dwFlags ?  L"ENABLED" : L"DISABLED"));
                    CoTaskMemFree(wszName);
                }
            }
            pStrm->Release();
        }
        pSAMI->Release();
    }

    // Run the graph and display the captions.
    pMediaControl->Run();
    while (1)
    {
        long evCode, lParam1, lParam2;
        pEv->GetEvent(&evCode, &lParam1, &lParam2, 100);
        
        if (evCode == EC_OLE_EVENT) {
            wprintf(L"%s\n", (BSTR)lParam2);
        }
        pEv->FreeEventParams(evCode, lParam1, lParam2);

        if (evCode == EC_USERABORT || evCode == EC_COMPLETE || evCode == EC_ERRORABORT)
            break;
    }

    // Clean up.
    pMediaControl->Release();
    pEv->Release();
    pGraph->Release();
    CoUninitialize();
}
```



<span data-ttu-id="39cec-153">此篩選器會使用 [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) 介面從來源篩選器提取範例。</span><span class="sxs-lookup"><span data-stu-id="39cec-153">This filter uses the [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) interface to pull samples from the source filter.</span></span> <span data-ttu-id="39cec-154">因此，它不支援其輸入 pin 上的 [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) 介面。</span><span class="sxs-lookup"><span data-stu-id="39cec-154">Therefore, it does not support the [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) interface on its input pin.</span></span>

## <a name="related-topics"></a><span data-ttu-id="39cec-155">相關主題</span><span class="sxs-lookup"><span data-stu-id="39cec-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="39cec-156">DirectShow 篩選</span><span class="sxs-lookup"><span data-stu-id="39cec-156">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



