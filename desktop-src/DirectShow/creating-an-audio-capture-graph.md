---
description: 建立音訊捕獲圖形
ms.assetid: 2302bb40-a5db-473a-afeb-71905ac41f47
title: 建立音訊捕獲圖形
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bd3c731a7dc498fcb7180bc56ae6a7f94dbec6d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106973362"
---
# <a name="creating-an-audio-capture-graph"></a><span data-ttu-id="042ff-103">建立音訊捕獲圖形</span><span class="sxs-lookup"><span data-stu-id="042ff-103">Creating an Audio Capture Graph</span></span>

<span data-ttu-id="042ff-104">音訊捕獲應用程式的第一個步驟是建立篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="042ff-104">The first step for an audio capture application is to build a filter graph.</span></span> <span data-ttu-id="042ff-105">圖形的設定取決於您想要建立的檔案類型。</span><span class="sxs-lookup"><span data-stu-id="042ff-105">The configuration of the graph depends on the type of file that you want to create.</span></span>

-   <span data-ttu-id="042ff-106">僅限音訊的 AVI 檔：將音訊捕獲篩選至 [Avi mux](avi-mux-filter.md) 篩選，並將 Avi mux 篩選至檔案 [寫入](file-writer-filter.md) 器篩選器。</span><span class="sxs-lookup"><span data-stu-id="042ff-106">Audio-only AVI file: Audio Capture Filter to [AVI Mux](avi-mux-filter.md) filter, and AVI Mux to [File Writer](file-writer-filter.md) filter.</span></span>
-   <span data-ttu-id="042ff-107">WAV 檔：音訊捕獲篩選器可將 [篩選範例 WavDest](wavdest-filter-sample.md) 至檔案寫入器篩選</span><span class="sxs-lookup"><span data-stu-id="042ff-107">WAV file: Audio Capture Filter to [WavDest Filter Sample](wavdest-filter-sample.md) to File Writer Filter</span></span>
-   <span data-ttu-id="042ff-108">Windows Media 音訊 ( .wma) 檔：將音訊捕獲篩選器篩選至 [WM ASF 寫入](wm-asf-writer-filter.md) 器篩選器。</span><span class="sxs-lookup"><span data-stu-id="042ff-108">Windows Media Audio (.wma) file: Audio Capture Filter to [WM ASF Writer](wm-asf-writer-filter.md) filter.</span></span>

<span data-ttu-id="042ff-109">WavDest 篩選器會以 SDK 範例的形式提供。</span><span class="sxs-lookup"><span data-stu-id="042ff-109">The WavDest filter is provided as an SDK sample.</span></span> <span data-ttu-id="042ff-110">若要使用它，您必須建立並註冊篩選準則。</span><span class="sxs-lookup"><span data-stu-id="042ff-110">To use it, you must build and register the filter.</span></span>

<span data-ttu-id="042ff-111">若要使用 ASF 寫入器篩選器，您必須安裝 Windows Media SDK 並取得軟體金鑰以解除鎖定篩選。</span><span class="sxs-lookup"><span data-stu-id="042ff-111">To use the ASF Writer filter, you must install the Windows Media SDK and obtain a software key to unlock the filter.</span></span> <span data-ttu-id="042ff-112">如需詳細資訊，請參閱 [在 DirectShow 中使用 Windows Media](using-windows-media-in-directshow.md)。</span><span class="sxs-lookup"><span data-stu-id="042ff-112">For more information, see [Using Windows Media in DirectShow](using-windows-media-in-directshow.md).</span></span>

<span data-ttu-id="042ff-113">您可以使用 [ [Capture Graph Builder]](capture-graph-builder.md) 物件來建立篩選圖形，也可以「手動」建立圖形;也就是，讓應用程式以程式設計方式新增並連接每個篩選準則。</span><span class="sxs-lookup"><span data-stu-id="042ff-113">You can build the filter graph using the [Capture Graph Builder](capture-graph-builder.md) object, or you can build the graph "manually"; that is, have the application programmatically add and connect each filter.</span></span> <span data-ttu-id="042ff-114">本文描述手動方法。</span><span class="sxs-lookup"><span data-stu-id="042ff-114">This article describes the manual approach.</span></span> <span data-ttu-id="042ff-115">如需使用 [Capture Graph Builder] 的詳細資訊，請參閱 [影片捕獲](video-capture.md)。</span><span class="sxs-lookup"><span data-stu-id="042ff-115">For more information about using the Capture Graph Builder, see [Video Capture](video-capture.md).</span></span> <span data-ttu-id="042ff-116">本文中大部分的資訊都適用于僅限音訊的圖形。</span><span class="sxs-lookup"><span data-stu-id="042ff-116">Much of the information in that article applies to audio-only graphs.</span></span>

<span data-ttu-id="042ff-117">新增音訊捕獲裝置</span><span class="sxs-lookup"><span data-stu-id="042ff-117">Adding the Audio Capture Device</span></span>

<span data-ttu-id="042ff-118">因為音訊捕獲篩選器會與特定硬體裝置通訊，所以您無法直接呼叫 **CoCreateInstance** 來建立篩選器。</span><span class="sxs-lookup"><span data-stu-id="042ff-118">Because the Audio Capture Filter communicates with a specific hardware device, you cannot simply call **CoCreateInstance** to create the filter.</span></span> <span data-ttu-id="042ff-119">相反地，請使用 [系統裝置](system-device-enumerator.md) 列舉值來列舉 [音訊捕獲來源] 類別目錄中的所有裝置（由類別識別碼 CLSID AudioInputDeviceCategory 來識別） \_ 。</span><span class="sxs-lookup"><span data-stu-id="042ff-119">Instead, use the [System Device Enumerator](system-device-enumerator.md) to enumerate all of the devices in the "Audio Capture Sources" category, which is identified by the class identifier CLSID\_AudioInputDeviceCategory.</span></span>

<span data-ttu-id="042ff-120">系統裝置列舉值會傳回裝置的名字組清單;每個名字標記的易記名稱都會對應到裝置的名稱。</span><span class="sxs-lookup"><span data-stu-id="042ff-120">The System Device Enumerator returns a list of monikers for the devices; each moniker's friendly name corresponds to the name of the device.</span></span> <span data-ttu-id="042ff-121">選擇其中一個傳回的名字，並使用它來建立該裝置的音訊捕獲篩選準則實例。</span><span class="sxs-lookup"><span data-stu-id="042ff-121">Choose one of the returned monikers and use it to create an instance of the Audio Capture Filter for that device.</span></span> <span data-ttu-id="042ff-122">將篩選準則加入至篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="042ff-122">Add the filter to the filter graph.</span></span> <span data-ttu-id="042ff-123">使用者的慣用音訊錄製裝置會先出現在 [標記清單] 中。</span><span class="sxs-lookup"><span data-stu-id="042ff-123">The user's preferred audio recording device appears first in the moniker list.</span></span> <span data-ttu-id="042ff-124"> (使用者選取慣用的裝置，方法是按一下主控台中的 [音效和多媒體]。 ) </span><span class="sxs-lookup"><span data-stu-id="042ff-124">(The user selects a preferred device by clicking Sounds and Multimedia in Control Panel.)</span></span>

<span data-ttu-id="042ff-125">如需詳細資訊，請參閱 [使用系統裝置枚舉器](using-the-system-device-enumerator.md)。</span><span class="sxs-lookup"><span data-stu-id="042ff-125">For more information, see [Using the System Device Enumerator](using-the-system-device-enumerator.md).</span></span>

<span data-ttu-id="042ff-126">若要指定要從中取得的輸入，請從音訊捕獲篩選器取得 [**IAMAudioInputMixer**](/windows/desktop/api/Strmif/nn-strmif-iamaudioinputmixer) 介面，然後呼叫 **put \_ Enable** 方法來指定輸入。</span><span class="sxs-lookup"><span data-stu-id="042ff-126">To specify which input to capture from, obtain the [**IAMAudioInputMixer**](/windows/desktop/api/Strmif/nn-strmif-iamaudioinputmixer) interface from the Audio Capture filter and call the **put\_Enable** method to specify the input.</span></span> <span data-ttu-id="042ff-127">不過，此方法的一項限制是，不同的硬體裝置可能會使用不同的字串來識別其輸入。</span><span class="sxs-lookup"><span data-stu-id="042ff-127">One limitation of this method, however, is that different hardware devices may use different strings to identify their inputs.</span></span> <span data-ttu-id="042ff-128">例如，一張卡片可能會使用「麥克風」來識別麥克風輸入，而另一張卡片可能會使用「Mic」。</span><span class="sxs-lookup"><span data-stu-id="042ff-128">For example, one card may use "Microphone" to identify the microphone input and another card may use "Mic".</span></span> <span data-ttu-id="042ff-129">若要判斷指定輸入的字串識別碼，請使用 Windows 多媒體功能 [**waveOutOpen**](/previous-versions//dd743866(v=vs.85))、 [**mixerOpen**](/previous-versions//dd757308(v=vs.85))和 [**mixerGetLineInfo**](/previous-versions//dd757303(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="042ff-129">To determine the string identifier for a given input, use the Windows Multimedia functions [**waveOutOpen**](/previous-versions//dd743866(v=vs.85)), [**mixerOpen**](/previous-versions//dd757308(v=vs.85)), and [**mixerGetLineInfo**](/previous-versions//dd757303(v=vs.85)).</span></span> <span data-ttu-id="042ff-130">如需詳細資訊，請參閱 MSDN 主題 [混音器裝置查詢](/windows/desktop/Multimedia/mixer-device-queries) 。</span><span class="sxs-lookup"><span data-stu-id="042ff-130">See the MSDN topic [Mixer Device Queries](/windows/desktop/Multimedia/mixer-device-queries) for more information.</span></span>

<span data-ttu-id="042ff-131">新增多工器和檔案寫入器</span><span class="sxs-lookup"><span data-stu-id="042ff-131">Adding the Multiplexer and the File Writer</span></span>

<span data-ttu-id="042ff-132">音訊捕獲圖形必須包含多工器和檔案寫入器。</span><span class="sxs-lookup"><span data-stu-id="042ff-132">An audio capture graph must contain a multiplexer and a file writer.</span></span>

<span data-ttu-id="042ff-133">多工器是一種篩選器， *可將一* 或多個資料流程合併為具有特定格式的單一資料流程。</span><span class="sxs-lookup"><span data-stu-id="042ff-133">A *multiplexer* is a filter that combines one or more streams into a single stream with a particular format.</span></span> <span data-ttu-id="042ff-134">例如，AVI Mux 篩選器會將音訊和影片串流合併到交錯的 AVI 資料流程中。</span><span class="sxs-lookup"><span data-stu-id="042ff-134">For example, the AVI Mux filter combines audio and video streams into an interleaved AVI stream.</span></span> <span data-ttu-id="042ff-135">針對音訊捕獲，通常只有一個音訊串流，但音訊資料仍然必須封裝成可儲存至磁片的格式，而這需要多工器。</span><span class="sxs-lookup"><span data-stu-id="042ff-135">For audio capture, there is typically only a single audio stream, but the audio data must still be packaged into a format that can be saved to disk, which requires a multiplexer.</span></span> <span data-ttu-id="042ff-136">多工器的選擇取決於目標格式：</span><span class="sxs-lookup"><span data-stu-id="042ff-136">The choice of multiplexer depends on the target format:</span></span>

-   <span data-ttu-id="042ff-137">AVI： AVI 多工器</span><span class="sxs-lookup"><span data-stu-id="042ff-137">AVI: AVI Multiplexer</span></span>
-   <span data-ttu-id="042ff-138">WAV： WavDest</span><span class="sxs-lookup"><span data-stu-id="042ff-138">WAV: WavDest</span></span>
-   <span data-ttu-id="042ff-139">WMA： ASF 寫入器</span><span class="sxs-lookup"><span data-stu-id="042ff-139">WMA: ASF Writer</span></span>

<span data-ttu-id="042ff-140">檔案 *寫入器* 是一種篩選器，可將傳入的資料寫入檔案。</span><span class="sxs-lookup"><span data-stu-id="042ff-140">A *file writer* is a filter that writes incoming data to a file.</span></span> <span data-ttu-id="042ff-141">若是 AVI 或 WAV 檔案，請使用檔案 [寫入器篩選器](file-writer-filter.md)。</span><span class="sxs-lookup"><span data-stu-id="042ff-141">For AVI or WAV files, use the [File Writer Filter](file-writer-filter.md).</span></span> <span data-ttu-id="042ff-142">針對 WMA 檔案，ASF 寫入器可作為多工器和檔案寫入器。</span><span class="sxs-lookup"><span data-stu-id="042ff-142">For WMA files, the ASF Writer acts as both multiplexer and file writer.</span></span>

<span data-ttu-id="042ff-143">在您建立篩選並將它們新增至圖形之後，請將音訊捕獲篩選器的輸出接點連接到多工器的輸入 pin，然後將多工器的輸出圖釘連接到篩選寫入器的輸入 pin 碼 (假設這些是個別的篩選) 。</span><span class="sxs-lookup"><span data-stu-id="042ff-143">After you create the filters and add them to the graph, connect the Audio Capture Filter's output pin to the multiplexer's input pin, and connect the multiplexer's output pin to the filter writer's input pin (assuming these are separate filters).</span></span> <span data-ttu-id="042ff-144">若要指定檔案名，請查詢 [**IFileSinkFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter) 介面的檔案寫入器，然後呼叫 [**IFileSinkFilter：： SetFileName**](/windows/desktop/api/Strmif/nf-strmif-ifilesinkfilter-setfilename) 方法。</span><span class="sxs-lookup"><span data-stu-id="042ff-144">To specify the file name, query the file writer for the [**IFileSinkFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter) interface and call the [**IFileSinkFilter::SetFileName**](/windows/desktop/api/Strmif/nf-strmif-ifilesinkfilter-setfilename) method.</span></span>

### <a name="example-code"></a><span data-ttu-id="042ff-145">範例程式碼</span><span class="sxs-lookup"><span data-stu-id="042ff-145">Example Code</span></span>

<span data-ttu-id="042ff-146">下列範例說明如何使用 WavDest 篩選器來建立音訊捕獲圖形。</span><span class="sxs-lookup"><span data-stu-id="042ff-146">The following example shows how to build an audio capture graph using the WavDest filter.</span></span> <span data-ttu-id="042ff-147">相同的原則也適用于其他檔案類型。</span><span class="sxs-lookup"><span data-stu-id="042ff-147">The same principles apply for the other file types.</span></span>


```C++
IBaseFilter *pSrc = NULL, *pWaveDest = NULL, *pWriter = NULL;
IFileSinkFilter *pSink= NULL;
IGraphBuilder *pGraph;

// Create the Filter Graph Manager.
hr = CoCreateInstance(CLSID_FilterGraph, NULL, CLSCTX_INPROC_SERVER,
    IID_IGraphBuilder, (void**)&pGraph);

// This example omits error handling.

// Not shown: Use the System Device Enumerator to create the 
// audio capture filter.

// Add the audio capture filter to the filter graph. 
hr = pGraph->AddFilter(pSrc, L"Capture");

// Add the WavDest and the File Writer.
hr = AddFilterByCLSID(pGraph, CLSID_WavDest, L"WavDest", &pWaveDest);
hr = AddFilterByCLSID(pGraph, CLSID_FileWriter, L"File Writer", &pWriter);

// Set the file name.
hr = pWriter->QueryInterface(IID_IFileSinkFilter, (void**)&pSink);
hr = pSink->SetFileName(L"C:\\MyWavFile.wav", NULL);

// Connect the filters.
hr = ConnectFilters(pGraph, pSrc, pWaveDest);
hr = ConnectFilters(pGraph, pWaveDest, pWriter);

// Not shown: Release interface pointers.

```



<span data-ttu-id="042ff-148">這個範例會使用 `AddFilterByCLSID` 在 [ [加入篩選依據 CLSID](add-a-filter-by-clsid.md)] 中所述的函式，以及 [ `ConnectFilters` [連接兩個篩選器]](connect-two-filters.md)中所述的函數。</span><span class="sxs-lookup"><span data-stu-id="042ff-148">This example uses the `AddFilterByCLSID` function described in [Add a Filter by CLSID](add-a-filter-by-clsid.md), and the `ConnectFilters` function described in [Connect Two Filters](connect-two-filters.md).</span></span> <span data-ttu-id="042ff-149">這兩種都不是 DirectShow API。</span><span class="sxs-lookup"><span data-stu-id="042ff-149">Neither of these is a DirectShow API.</span></span>

## <a name="related-topics"></a><span data-ttu-id="042ff-150">相關主題</span><span class="sxs-lookup"><span data-stu-id="042ff-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="042ff-151">音訊捕獲</span><span class="sxs-lookup"><span data-stu-id="042ff-151">Audio Capture</span></span>](audio-capture.md)
</dt> </dl>

 

 
