---
description: 從類型1檔案傳輸
ms.assetid: 5be2248b-7917-4c1b-9ae7-29e06779eac6
title: 從類型1檔案傳輸
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74e38ed3e549b6cd671248ba1df9b24df8fbfe3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104026898"
---
# <a name="transmit-from-type-1-file"></a><span data-ttu-id="a2631-103">從類型1檔案傳輸</span><span class="sxs-lookup"><span data-stu-id="a2631-103">Transmit from Type-1 File</span></span>

<span data-ttu-id="a2631-104">若要在預覽檔時傳輸類型1檔案，請使用下圖所示的篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="a2631-104">To transmit a type-1 file while previewing the file, use the filter graph shown in the following diagram.</span></span>

![類型1以預覽傳送](images/dv1-transmit.png)

<span data-ttu-id="a2631-106">此圖表中的篩選包括：</span><span class="sxs-lookup"><span data-stu-id="a2631-106">Filters in this graph include:</span></span>

-   <span data-ttu-id="a2631-107">[Avi 分隔器](avi-splitter-filter.md)會剖析 AVI 檔。</span><span class="sxs-lookup"><span data-stu-id="a2631-107">The [AVI Splitter](avi-splitter-filter.md) parses the AVI file.</span></span> <span data-ttu-id="a2631-108">針對類型 1 DV 檔案，輸出 pin 會提供交錯式 DV 範例。</span><span class="sxs-lookup"><span data-stu-id="a2631-108">For a type-1 DV file, the output pin delivers interleaved DV samples.</span></span>
-   <span data-ttu-id="a2631-109">[無限的 Pin 指標](infinite-pin-tee-filter.md)濾波器會將交錯的 DV 分割成傳輸資料流程和預覽資料流程。</span><span class="sxs-lookup"><span data-stu-id="a2631-109">The [Infinite Pin Tee](infinite-pin-tee-filter.md) filter splits the interleaved DV into a transmit stream and a preview stream.</span></span> <span data-ttu-id="a2631-110">這兩個數據流都包含相同的交錯資料。</span><span class="sxs-lookup"><span data-stu-id="a2631-110">Both streams contain the same interleaved data.</span></span> <span data-ttu-id="a2631-111"> (此圖形使用無限的 Pin 碼 t，而不是 [智慧型](smart-tee-filter.md)指標，因為在從檔案讀取時，不會有任何風險可卸載框架，如同 live capture 一樣。 ) </span><span class="sxs-lookup"><span data-stu-id="a2631-111">(This graph uses the Infinite Pin Tee instead of the [Smart Tee](smart-tee-filter.md), because there is no danger of dropping frames when reading from a file, as there is with live capture.)</span></span>
-   <span data-ttu-id="a2631-112">[Dv 分隔器](dv-splitter-filter.md)會將交錯的資料流程分割成 dv 影片串流，並以[dv video 解碼器](dv-video-decoder-filter.md)解碼，以及音訊串流。</span><span class="sxs-lookup"><span data-stu-id="a2631-112">The [DV Splitter](dv-splitter-filter.md) splits the interleaved stream into a DV video stream, which is decoded by the [DV Video Decoder](dv-video-decoder-filter.md), and an audio stream.</span></span> <span data-ttu-id="a2631-113">這兩個串流都是 rendererd 進行預覽。</span><span class="sxs-lookup"><span data-stu-id="a2631-113">Both streams are rendererd for preview.</span></span>

<span data-ttu-id="a2631-114">建立此圖形，如下所示：</span><span class="sxs-lookup"><span data-stu-id="a2631-114">Build this graph as follows:</span></span>


```C++
ICaptureGraphBuilder2 *pBuilder;  // Capture graph builder.
IBaseFilter           *pDV;       // DV capture filter (MSDV)

// Initialize pDV (not shown). 
// Create and initialize the Capture Graph Builder (not shown).

// Add the Infinite Pin Tee filter to the graph.
IBaseFilter *pTee;
hr = CoCreateInstance(CLSID_InfTee, 0, CLSCTX_INPROC_SERVER
    IID_IBaseFilter, reinterpret_cast<void**>)(&pTee));
hr = pGraph->AddFilter(pTee, L"Tee");

// Add the File Source filter to the graph.
IBaseFilter *pFileSource;
hr = pGraph->AddSourceFilter(
    L"C:\\YourFileNameHere.avi",
    L"Source", 
    &pFileSource);

// Add the AVI Splitter filter to the graph.
IBaseFilter *pAviSplit;
hr = CoCreateInstance(CLSID_AviSplitter, 0, CLSCTX_INPROC_SERVER
    IID_IBaseFilter, reinterpret_cast<void**>)(&pAviSplit));
hr = pGraph->AddFilter(pAviSplit, L"AVI Splitter");

// Connect the file source to the AVI Splitter.
hr = pBuilder->RenderStream(0, 0, pFileSource, 0, pAviSplit);
if (FAILED(hr))
{
    // This is not an AVI file. 
}

// Connect the file source to the Infinite Pin Tee.
hr = pBuilder->RenderStream(0, &MEDIATYPE_Interleaved, pAviSplit, 0, pTee);
if (FAILED(hr))
{
    // This is not a type-1 DV file.
}

// Render one stream from the Infinite Pin Tee to MSDV, for transmit.
hr = pBuilder->RenderStream(0, 0, pTee, 0, pDV);

// Render another stream from the Infinite Pin Tee for preview.
hr = pBuilder->RenderStream(0, 0, pTee, 0, 0);
```



1.  <span data-ttu-id="a2631-115">呼叫 [**IGraphBuilder：： AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter) ，將來源篩選加入至篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="a2631-115">Call [**IGraphBuilder::AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter) to add the source filter to the filter graph.</span></span>
2.  <span data-ttu-id="a2631-116">建立 AVI 分隔器和無限圖釘指標，然後將它們新增至圖形。</span><span class="sxs-lookup"><span data-stu-id="a2631-116">Create the AVI Splitter and the Infinite Pin Tee, and add them to the graph.</span></span>
3.  <span data-ttu-id="a2631-117">呼叫 [**ICaptureGraphBuilder2：： RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) ，將來源篩選連接到 AVI 分隔器。</span><span class="sxs-lookup"><span data-stu-id="a2631-117">Call [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) to connect the source filter to the AVI Splitter.</span></span> <span data-ttu-id="a2631-118">如果來源檔案不是類型1的 DV 檔案，則指定 \_ 以交錯方式來確保方法會失敗。</span><span class="sxs-lookup"><span data-stu-id="a2631-118">Specifying MEDIATYPE\_Interleaved to ensure that the method fails if the source file is not a type-1 DV file.</span></span> <span data-ttu-id="a2631-119">在這種情況下，您可以改為嘗試建立類型2傳輸圖形。</span><span class="sxs-lookup"><span data-stu-id="a2631-119">In that case, you can back out and attempt to build a type-2 transmit graph instead.</span></span>
4.  <span data-ttu-id="a2631-120">再次呼叫 **RenderStream** ，以將交錯的資料流程從 AVI 分隔器路由傳送到無限的 Pin t</span><span class="sxs-lookup"><span data-stu-id="a2631-120">Call **RenderStream** again to route the interleaved stream from the AVI Splitter to the Infinite Pin Tee</span></span>
5.  <span data-ttu-id="a2631-121">第三次呼叫 RenderStream，以將一個串流從無限的 Pin t 路由傳送至 MSDV 篩選器，以傳送至裝置。</span><span class="sxs-lookup"><span data-stu-id="a2631-121">Call RenderStream a third time to route one stream from the Infinite Pin Tee to the MSDV filter, for transmit to the device.</span></span>
6.  <span data-ttu-id="a2631-122">最後一次呼叫 **RenderStream** ，以建立圖形的預覽區段。</span><span class="sxs-lookup"><span data-stu-id="a2631-122">Call **RenderStream** one last time, to build the preview section of the graph.</span></span>

<span data-ttu-id="a2631-123">如果您不想要預覽，只要將檔案來源連接到 MSDV 篩選器即可：</span><span class="sxs-lookup"><span data-stu-id="a2631-123">If you do not want preview, simply connect the file source to the MSDV filter:</span></span>


```C++
hr = pBuilder->RenderStream(0, &MEDIATYPE_Interleaved, pFileSource, 0, pDV);
```



## <a name="related-topics"></a><span data-ttu-id="a2631-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="a2631-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a2631-125">DirectShow 中的數位視訊</span><span class="sxs-lookup"><span data-stu-id="a2631-125">Digital Video in DirectShow</span></span>](digital-video-in-directshow.md)
</dt> </dl>

 

 



