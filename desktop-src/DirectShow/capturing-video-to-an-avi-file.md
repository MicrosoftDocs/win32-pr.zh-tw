---
description: 將影片捕獲到 AVI 檔案
ms.assetid: 0f5f4a82-4a2e-4c48-b201-bda641cb8619
title: 將影片捕獲到 AVI 檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86504e9ce149f495e1ea31664f56382340d33887
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104561027"
---
# <a name="capturing-video-to-an-avi-file"></a><span data-ttu-id="9eb11-103">將影片捕獲到 AVI 檔案</span><span class="sxs-lookup"><span data-stu-id="9eb11-103">Capturing Video to an AVI File</span></span>

<span data-ttu-id="9eb11-104">下圖顯示將影片捕獲到 AVI 檔案的最簡單圖形。</span><span class="sxs-lookup"><span data-stu-id="9eb11-104">The following illustration shows the simplest possible graph for capturing video to an AVI file.</span></span>

![avi 影片捕獲圖形](images/vidcap02.png)

<span data-ttu-id="9eb11-106">[AVI Mux](avi-mux-filter.md)篩選器會從 capture 釘選影片串流，並將其封裝成 AVI 資料流程。</span><span class="sxs-lookup"><span data-stu-id="9eb11-106">The [AVI Mux](avi-mux-filter.md) filter takes the video stream from the capture pin and packages it into an AVI stream.</span></span> <span data-ttu-id="9eb11-107">音訊串流也可以連接到 AVI Mux 篩選器，在這種情況下，Mux 會交錯兩個數據流。</span><span class="sxs-lookup"><span data-stu-id="9eb11-107">An audio stream could also be connected to the AVI Mux filter, in which case the mux would interleave the two streams.</span></span> <span data-ttu-id="9eb11-108">檔案 [寫入](file-writer-filter.md) 器篩選器會將 AVI 資料流程寫入磁片。</span><span class="sxs-lookup"><span data-stu-id="9eb11-108">The [File Writer](file-writer-filter.md) filter writes the AVI stream to disk.</span></span>

<span data-ttu-id="9eb11-109">若要建立圖形，請先呼叫 [**ICaptureGraphBuilder2：： SetOutputFileName**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) 方法，如下所示：</span><span class="sxs-lookup"><span data-stu-id="9eb11-109">To build the graph, start by calling the [**ICaptureGraphBuilder2::SetOutputFileName**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) method, as follows:</span></span>


```C++
IBaseFilter *pMux;
hr = pBuild->SetOutputFileName(
    &MEDIASUBTYPE_Avi,  // Specifies AVI for the target file.
    L"C:\\Example.avi", // File name.
    &pMux,              // Receives a pointer to the mux.
    NULL);              // (Optional) Receives a pointer to the file sink.
```



<span data-ttu-id="9eb11-110">第一個參數會指定檔案類型，在此案例中為 AVI。</span><span class="sxs-lookup"><span data-stu-id="9eb11-110">The first parameter specifies the file type — in this case, AVI.</span></span> <span data-ttu-id="9eb11-111">第二個參數會提供檔案名。</span><span class="sxs-lookup"><span data-stu-id="9eb11-111">The second parameter gives the file name.</span></span> <span data-ttu-id="9eb11-112">針對 AVI，SetOutputFileName 方法會 cocreates AVI Mux 篩選器和檔案寫入器篩選器，並將它們新增至圖形。</span><span class="sxs-lookup"><span data-stu-id="9eb11-112">For AVI, the SetOutputFileName method cocreates the AVI Mux filter and the File Writer filter and adds them to the graph.</span></span> <span data-ttu-id="9eb11-113">它也會藉由呼叫 [**IFileSinkFilter：： SetFileName**](/windows/desktop/api/Strmif/nf-strmif-ifilesinkfilter-setfilename) 方法來設定檔案寫入器篩選器上的檔案名，並連接這兩個篩選器。</span><span class="sxs-lookup"><span data-stu-id="9eb11-113">It also sets the file name on the File Writer filter, by calling the [**IFileSinkFilter::SetFileName**](/windows/desktop/api/Strmif/nf-strmif-ifilesinkfilter-setfilename) method, and connects the two filters.</span></span> <span data-ttu-id="9eb11-114">方法會傳回第三個參數中 AVI Mux 的指標。</span><span class="sxs-lookup"><span data-stu-id="9eb11-114">The method returns a pointer to the AVI Mux in the third parameter.</span></span> <span data-ttu-id="9eb11-115">（選擇性）它會傳回第四個參數中 [**IFileSinkFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="9eb11-115">Optionally, it returns a pointer to the [**IFileSinkFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter) interface in the fourth parameter.</span></span> <span data-ttu-id="9eb11-116">如果您不需要此介面，您可以將此參數設定為 **Null**，如先前的範例所示。</span><span class="sxs-lookup"><span data-stu-id="9eb11-116">If you don't need this interface, you can set this parameter to **NULL**, as shown in the previous example.</span></span>

<span data-ttu-id="9eb11-117">接下來，呼叫 [**ICaptureGraphBuilder2：： RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) 方法，將捕獲篩選器連線到 AVI Mux，如下所示：</span><span class="sxs-lookup"><span data-stu-id="9eb11-117">Next, call the [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method to connect the capture filter to the AVI Mux, as follows:</span></span>


```C++
hr = pBuild->RenderStream(
    &PIN_CATEGORY_CAPTURE, // Pin category.
    &MEDIATYPE_Video,      // Media type.
    pCap,                  // Capture filter.
    NULL,                  // Intermediate filter (optional).
    pMux);                 // Mux or file sink filter.

// Release the mux filter.
pMux->Release();
```



<span data-ttu-id="9eb11-118">第一個參數會提供 pin 類別，也就是 \_ 用於捕捉的釘選類別 \_ 捕獲。</span><span class="sxs-lookup"><span data-stu-id="9eb11-118">The first parameter gives the pin category, which is PIN\_CATEGORY\_CAPTURE for capture.</span></span> <span data-ttu-id="9eb11-119">第二個參數會提供媒體類型。</span><span class="sxs-lookup"><span data-stu-id="9eb11-119">The second parameter gives the media type.</span></span> <span data-ttu-id="9eb11-120">第三個參數是捕獲篩選器 [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="9eb11-120">The third parameter is a pointer to the capture filter's [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface.</span></span> <span data-ttu-id="9eb11-121">第四個參數是選擇性的;它可讓您透過中繼篩選（例如編碼器）路由傳送影片串流，然後再將它傳遞至 mux 篩選器。</span><span class="sxs-lookup"><span data-stu-id="9eb11-121">The fourth parameter is optional; it lets you route the video stream through an intermediate filter, such as an encoder, before passing it to the mux filter.</span></span> <span data-ttu-id="9eb11-122">否則，請將此參數設定為 **Null**，如先前的範例所示。</span><span class="sxs-lookup"><span data-stu-id="9eb11-122">Otherwise, set this parameter to **NULL**, as shown in the previous example.</span></span> <span data-ttu-id="9eb11-123">第五個參數是 mux 篩選器的指標。</span><span class="sxs-lookup"><span data-stu-id="9eb11-123">The fifth parameter is the pointer to the mux filter.</span></span> <span data-ttu-id="9eb11-124">呼叫 SetOutputFileName 方法即可取得這個指標。</span><span class="sxs-lookup"><span data-stu-id="9eb11-124">This pointer is obtained by calling the SetOutputFileName method.</span></span>

<span data-ttu-id="9eb11-125">若要捕獲音訊，請使用媒體類型媒體類型來呼叫 RenderStream \_ 。</span><span class="sxs-lookup"><span data-stu-id="9eb11-125">To capture audio, call RenderStream with the media type MEDIATYPE\_Audio.</span></span> <span data-ttu-id="9eb11-126">如果您從兩部不同的裝置捕獲音訊和影片，最好讓音訊串流成為主要串流。</span><span class="sxs-lookup"><span data-stu-id="9eb11-126">If you are capturing audio and video from two separate devices, it is a good idea to make the audio stream the master stream.</span></span> <span data-ttu-id="9eb11-127">這有助於防止兩個數據流之間的漂移，因為 AVI Mux 篩選器會調整影片資料流程的播放速率以符合音訊串流。</span><span class="sxs-lookup"><span data-stu-id="9eb11-127">This helps to prevent drift between the two streams, because the AVI Mux filter adjust the playback rate on the video stream to match the audio stream.</span></span> <span data-ttu-id="9eb11-128">若要設定主要串流，請在 AVI Mux 篩選器上呼叫 [**IConfigAviMux：： SetMasterStream**](/windows/desktop/api/Strmif/nf-strmif-iconfigavimux-setmasterstream) 方法：</span><span class="sxs-lookup"><span data-stu-id="9eb11-128">To set the master stream, call the [**IConfigAviMux::SetMasterStream**](/windows/desktop/api/Strmif/nf-strmif-iconfigavimux-setmasterstream) method on the AVI Mux filter:</span></span>


```C++
IConfigAviMux *pConfigMux = NULL;
hr = pMux->QueryInterface(IID_IConfigAviMux, (void**)&pConfigMux);
if (SUCCEEDED(hr))
{
    pConfigMux->SetMasterStream(1);
    pConfigMux->Release();
}
```



<span data-ttu-id="9eb11-129">SetMasterStream 的參數是資料流程號碼，由您呼叫 RenderStream 的順序決定。</span><span class="sxs-lookup"><span data-stu-id="9eb11-129">The parameter to SetMasterStream is the stream number, which is determined by the order in which you call RenderStream.</span></span> <span data-ttu-id="9eb11-130">例如，如果您先針對影片呼叫 RenderStream，然後針對音訊撥號，則影片為串流0，而音訊為串流1。</span><span class="sxs-lookup"><span data-stu-id="9eb11-130">For example, if you call RenderStream first for video and then for audio, the video is stream 0 and the audio is stream 1.</span></span>

<span data-ttu-id="9eb11-131">您也可能想要設定 AVI Mux 篩選器交錯音訊和影片資料流程的方式，方法是呼叫 [**IConfigInterleaving：:p ui \_ 模式**](/windows/desktop/api/Strmif/nf-strmif-iconfiginterleaving-put_mode) 方法。</span><span class="sxs-lookup"><span data-stu-id="9eb11-131">You may also want to set how the AVI Mux filter interleaves the audio and video streams, by calling the [**IConfigInterleaving::put\_Mode**](/windows/desktop/api/Strmif/nf-strmif-iconfiginterleaving-put_mode) method.</span></span>


```C++
IConfigInterleaving *pInterleave = NULL;
hr = pMux->QueryInterface(IID_IConfigInterleaving, (void**)&pInterleave);
if (SUCCEEDED(hr))
{
    pInterleave->put_Mode(INTERLEAVE_CAPTURE);
    pInterleave->Release();
}
```



<span data-ttu-id="9eb11-132">使用交錯 \_ 捕獲旗標，AVI Mux 會以適用于影片捕獲的速率來執行交錯。</span><span class="sxs-lookup"><span data-stu-id="9eb11-132">With the INTERLEAVE\_CAPTURE flag, the AVI Mux performs interleaving at a rate that is suitable for video capture.</span></span> <span data-ttu-id="9eb11-133">您也可以使用交錯 \_ 無，也就是沒有交錯的，AVI Mux 只會以抵達的順序寫入資料。</span><span class="sxs-lookup"><span data-stu-id="9eb11-133">You can also use INTERLEAVE\_NONE, which means no interleaving — the AVI Mux will simply write the data in the order that it arrives.</span></span> <span data-ttu-id="9eb11-134">交錯的 \_ 完整旗標表示 AVI Mux 會執行完全交錯的功能; 不過，此模式較不適合用于影片捕獲，因為它需要最多段無意。</span><span class="sxs-lookup"><span data-stu-id="9eb11-134">The INTERLEAVE\_FULL flag means the AVI Mux performs full interleaving; however, this mode is less suitable for video capture because it requires the most overheard.</span></span>

<span data-ttu-id="9eb11-135">編碼影片串流</span><span class="sxs-lookup"><span data-stu-id="9eb11-135">Encoding the Video Stream</span></span>

<span data-ttu-id="9eb11-136">您可以藉由在捕獲篩選器和 AVI Mux 篩選器之間插入編碼器篩選器，將影片串流編碼。</span><span class="sxs-lookup"><span data-stu-id="9eb11-136">You can encode the video stream by inserting an encoder filter between the capture filter and the AVI Mux filter.</span></span> <span data-ttu-id="9eb11-137">使用 [系統裝置列舉](system-device-enumerator.md) 值或 [篩選器](filter-mapper.md) 對應程式來選取編碼器篩選器。</span><span class="sxs-lookup"><span data-stu-id="9eb11-137">Use the [System Device Enumerator](system-device-enumerator.md) or the [Filter Mapper](filter-mapper.md) to select an encoder filter.</span></span> <span data-ttu-id="9eb11-138"> (需詳細資訊，請參閱 [列舉裝置和篩選器](enumerating-devices-and-filters.md)。 ) </span><span class="sxs-lookup"><span data-stu-id="9eb11-138">(For more information, see [Enumerating Devices and Filters](enumerating-devices-and-filters.md).)</span></span>

<span data-ttu-id="9eb11-139">將編碼器篩選器指定為要 RenderStream 的第四個參數，以粗體顯示在下列範例中：</span><span class="sxs-lookup"><span data-stu-id="9eb11-139">Specify the encoder filter as the fourth parameter to RenderStream, shown in bold in the following example:</span></span>


```C++
IBaseFilter *pEncoder;
/* Create the encoder filter (not shown). */
// Add it to the filter graph.
pGraph->AddFilter(pEncoder, L"Encoder");

/* Call SetOutputFileName as shown previously. */

// Render the stream.
hr = pBuild->RenderStream(&PIN_CATEGORY_CAPTURE, &MEDIATYPE_Video, 
    pCap, 
pEncoder, pMux);
pEncoder->Release();
```



<span data-ttu-id="9eb11-140">編碼器篩選器可能支援 [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) 或其他介面來設定編碼參數。</span><span class="sxs-lookup"><span data-stu-id="9eb11-140">The encoder filter might support [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) or other interfaces for setting the encoding parameters.</span></span> <span data-ttu-id="9eb11-141">如需可能的介面清單，請參閱檔案 [編碼和解碼介面](file-encoding-and-decoding-interfaces.md)。</span><span class="sxs-lookup"><span data-stu-id="9eb11-141">For a list of possible interfaces, see [File Encoding and Decoding Interfaces](file-encoding-and-decoding-interfaces.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9eb11-142">相關主題</span><span class="sxs-lookup"><span data-stu-id="9eb11-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9eb11-143">將影片捕獲至檔案</span><span class="sxs-lookup"><span data-stu-id="9eb11-143">Capturing Video to a File</span></span>](capturing-video-to-a-file.md)
</dt> </dl>

 

 



