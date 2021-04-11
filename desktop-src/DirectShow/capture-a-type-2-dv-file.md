---
description: 捕捉類型 2 DV 檔案
ms.assetid: c7d49c86-1b5d-43bf-98a5-78b297682375
title: 捕捉類型 2 DV 檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b919928a4c02ce9e3f3f3e6fcf3d2cd376f880a8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103845851"
---
# <a name="capture-a-type-2-dv-file"></a><span data-ttu-id="3846f-103">捕捉類型 2 DV 檔案</span><span class="sxs-lookup"><span data-stu-id="3846f-103">Capture a Type-2 DV File</span></span>

<span data-ttu-id="3846f-104">類型 2 DV AVI 檔案有兩個數據流，其中一個包含 DV 影片，另一個包含音訊。</span><span class="sxs-lookup"><span data-stu-id="3846f-104">A type-2 DV AVI file has two streams, one that contains DV video and another that contains audio.</span></span> <span data-ttu-id="3846f-105">若要在預覽時捕捉類型2檔案，請使用下圖所示的篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="3846f-105">To capture a type-2 file while previewing, use the filter graph shown in the following diagram.</span></span>

![具有預覽的類型2捕獲](images/dv2-cap.png)

<span data-ttu-id="3846f-107">This graph is almost the same as the graph for type-1 capture (see [Capture a Type-1 DV File](capture-a-type-1-dv-file.md)).</span><span class="sxs-lookup"><span data-stu-id="3846f-107">This graph is almost the same as the graph for type-1 capture (see [Capture a Type-1 DV File](capture-a-type-1-dv-file.md)).</span></span> <span data-ttu-id="3846f-108">不過，capture 資料流程會先經過 [DV 分隔](dv-splitter-filter.md) 器篩選器，再到達 [AVI Mux](avi-mux-filter.md) 篩選器。</span><span class="sxs-lookup"><span data-stu-id="3846f-108">However, the capture stream goes through the [DV Splitter](dv-splitter-filter.md) filter before reaching the [AVI Mux](avi-mux-filter.md) filter.</span></span> <span data-ttu-id="3846f-109">因此，AVI Mux 會接收兩個數據流，也就是音訊串流和 DV 編碼的影片串流。</span><span class="sxs-lookup"><span data-stu-id="3846f-109">The AVI Mux therefore receives two streams, an audio stream and a DV-encoded video stream.</span></span>

<span data-ttu-id="3846f-110">建立此圖形，如下所示：</span><span class="sxs-lookup"><span data-stu-id="3846f-110">Build this graph as follows:</span></span>


```C++
ICaptureGraphBuilder2 *pBuilder;  // Capture graph builder.
IBaseFilter           *pDV;       // DV capture filter (MSDV)
IBaseFilter           *pAviMux    // Avi Mux filter.
IBaseFilter           *pDVSplit;  // DV Splitter

// Initialize pDV (not shown). 
// Create and initialize the Capture Graph Builder (not shown).

// Create the DV Splitter and add it to the filter graph.
hr = CoCreateInstance(CLSID_DVSplitter, 0, CLSCTX_INPROC_SERVER,
    IID_IBaseFilter, reinterpret_cast<void**>)(&pDVSplit));
hr = pGraph->AddFilter(pDVSplit, L"DV Splitter");

// Create the file-writing section of the graph.
hr = pBuilder->SetOutputFileName(&MEDIASUBTYPE_Avi,
    OLESTR("C:\\Example2.avi"), &pAviMux, 0);

// Connect the capture pin to the DV Splitter, and render one stream from
// the DV Splitter to the AVI Mux. 
hr = pBuilder->RenderStream(&PIN_CATEGORY_CAPTURE, &MEDIATYPE_Interleaved, 
    pDV, pDVSplit, pAviMux);

// Render the other stream from the DV splitter to the AVI Mux.
hr = pBuilder->RenderStream(0, 0, pDVSplit, 0, pAviMux);

// Render the preview stream.
hr = pBuilder->RenderStream(&PIN_CATEGORY_PREVIEW, &MEDIATYPE_Interleaved, 
    pDV, 0, 0);

// Remember to release all interfaces.
```



1.  <span data-ttu-id="3846f-111">建立 DV 分隔器，並將它新增至篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="3846f-111">Create the DV Splitter and add it to the filter graph.</span></span>
2.  <span data-ttu-id="3846f-112">呼叫 [**ICaptureGraphBuilder2：： SetOutputFileName**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) ，將 AVI Mux 篩選器連線到檔案寫入器篩選器。</span><span class="sxs-lookup"><span data-stu-id="3846f-112">Call [**ICaptureGraphBuilder2::SetOutputFileName**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) to connect the AVI Mux filter to the File Writer filter.</span></span>
3.  <span data-ttu-id="3846f-113">呼叫 [**ICaptureGraphBuilder2：： RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) ，將 MSDV capture 篩選器連接至 DV 分隔器。</span><span class="sxs-lookup"><span data-stu-id="3846f-113">Call [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) to connect the MSDV capture filter to the DV Splitter.</span></span> <span data-ttu-id="3846f-114">此呼叫也會將其中一個 DV 分隔器的輸出圖釘連接到 AVI Mux。</span><span class="sxs-lookup"><span data-stu-id="3846f-114">This call also connects one of the DV Splitter's output pins to the AVI Mux.</span></span>
4.  <span data-ttu-id="3846f-115">再次呼叫 RenderStream，以將 DV 分隔器的其他釘選到 AVI Mux。</span><span class="sxs-lookup"><span data-stu-id="3846f-115">Call RenderStream again to connect the DV Splitter's other pin to the AVI Mux.</span></span>
5.  <span data-ttu-id="3846f-116">第三次呼叫 RenderStream 以轉譯預覽資料流程。</span><span class="sxs-lookup"><span data-stu-id="3846f-116">Call RenderStream a third time to render the preview stream.</span></span> <span data-ttu-id="3846f-117">如果不想要預覽影片，請略過此步驟。</span><span class="sxs-lookup"><span data-stu-id="3846f-117">Skip this step if do not want to preview the video.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3846f-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="3846f-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3846f-119">DirectShow 中的數位視訊</span><span class="sxs-lookup"><span data-stu-id="3846f-119">Digital Video in DirectShow</span></span>](digital-video-in-directshow.md)
</dt> </dl>

 

 



