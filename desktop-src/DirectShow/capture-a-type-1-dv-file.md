---
description: 捕捉類型 1 DV 檔案
ms.assetid: fba11e9b-4900-4b29-a0c9-702272cd7387
title: 捕捉類型 1 DV 檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8098669f124bdd4c0168e3549cd8eed8e1825c47
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104567413"
---
# <a name="capture-a-type-1-dv-file"></a><span data-ttu-id="19e22-103">捕捉類型 1 DV 檔案</span><span class="sxs-lookup"><span data-stu-id="19e22-103">Capture a Type-1 DV File</span></span>

<span data-ttu-id="19e22-104">類型 1 DV AVI 檔案包含單一交錯式資料流程。</span><span class="sxs-lookup"><span data-stu-id="19e22-104">A type-1 DV AVI file contains a single interleaved stream.</span></span> <span data-ttu-id="19e22-105">若要在預覽時捕捉類型1檔案，請使用下圖所示的篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="19e22-105">To capture a type-1 file while previewing, use the filter graph shown in the following diagram.</span></span>

![具有預覽的類型 1 capture](images/dv1-cap.png)

<span data-ttu-id="19e22-107">此圖表中的篩選包括：</span><span class="sxs-lookup"><span data-stu-id="19e22-107">Filters in this graph include:</span></span>

-   <span data-ttu-id="19e22-108">[Smart t](smart-tee-filter.md)濾波器會將交錯的 DV 分割成捕獲資料流程和預覽資料流程。</span><span class="sxs-lookup"><span data-stu-id="19e22-108">The [Smart Tee](smart-tee-filter.md) filter splits the interleaved DV into a capture stream and a preview stream.</span></span> <span data-ttu-id="19e22-109">這兩個數據流都包含相同的交錯資料。</span><span class="sxs-lookup"><span data-stu-id="19e22-109">Both streams contain the same interleaved data.</span></span>
-   <span data-ttu-id="19e22-110">[AVI Mux](avi-mux-filter.md)和檔案[寫入器](file-writer-filter.md)會將交錯串流寫入磁片。</span><span class="sxs-lookup"><span data-stu-id="19e22-110">The [AVI Mux](avi-mux-filter.md) and [File Writer](file-writer-filter.md) write the interleaved stream to disk.</span></span>
-   <span data-ttu-id="19e22-111">[Dv 分隔器](dv-splitter-filter.md)會將交錯的資料流程分割成 DV 影片串流和音訊串流。</span><span class="sxs-lookup"><span data-stu-id="19e22-111">The [DV Splitter](dv-splitter-filter.md) splits the interleaved stream into a DV video stream and an audio stream.</span></span> <span data-ttu-id="19e22-112">這兩個串流都是 rendererd 進行預覽。</span><span class="sxs-lookup"><span data-stu-id="19e22-112">Both streams are rendererd for preview.</span></span>
-   <span data-ttu-id="19e22-113">[Dv 影片解碼會解碼](dv-video-decoder-filter.md)dv 影片串流以進行預覽。</span><span class="sxs-lookup"><span data-stu-id="19e22-113">The [DV Video Decoder](dv-video-decoder-filter.md) decodes the DV video stream for previewing.</span></span>

<span data-ttu-id="19e22-114">建立此圖形，如下所示：</span><span class="sxs-lookup"><span data-stu-id="19e22-114">Build this graph as follows:</span></span>


```C++
ICaptureGraphBuilder2 *pBuilder;  // Capture graph builder.
IBaseFilter           *pDV;       // DV capture filter (MSDV)
IBaseFilter           *pAviMux    // Avi Mux filter.

// Initialize pDV (not shown). 
// Create and initialize the Capture Graph Builder (not shown).

// Create the file-writing section of the graph.
hr = pBuilder->SetOutputFileName(&MEDIASUBTYPE_Avi, 
    OLESTR("C:\\Example1.avi"), &pAviMux, 0);

// Render the capture stream.
hr = pBuilder->RenderStream(&PIN_CATEGORY_CAPTURE, &MEDIATYPE_Interleaved, 
    pDV, 0, pAviMux);

// Render the preview stream.
hr = pBuilder->RenderStream(&PIN_CATEGORY_PREVIEW, &MEDIATYPE_Interleaved,
    pDV, 0, 0);

// Remember to release all interfaces.
```



1.  <span data-ttu-id="19e22-115">呼叫 [**ICaptureGraphBuilder2：： SetOutputFileName**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) ，將 AVI Mux 篩選器連線到檔案寫入器篩選器。</span><span class="sxs-lookup"><span data-stu-id="19e22-115">Call [**ICaptureGraphBuilder2::SetOutputFileName**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) to connect the AVI Mux filter to the File Writer filter.</span></span>
2.  <span data-ttu-id="19e22-116">使用釘選分類釘選類別捕獲來呼叫 [**ICaptureGraphBuilder2：： RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) \_ \_ ，以轉譯捕獲資料流程。</span><span class="sxs-lookup"><span data-stu-id="19e22-116">Call [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) with the pin category PIN\_CATEGORY\_CAPTURE to render the capture stream.</span></span> <span data-ttu-id="19e22-117">「捕獲圖形產生器」會自動插入智慧的 t a 濾波器。</span><span class="sxs-lookup"><span data-stu-id="19e22-117">The Capture Graph Builder automatically inserts the Smart Tee filter.</span></span>
3.  <span data-ttu-id="19e22-118">再次呼叫 RenderStream，但使用釘選類別 PIN \_ 類別目錄 \_ 預覽，以轉譯預覽資料流程。</span><span class="sxs-lookup"><span data-stu-id="19e22-118">Call RenderStream again, but with the pin category PIN\_CATEGORY\_PREVIEW, to render the preview stream.</span></span> <span data-ttu-id="19e22-119">如果您不想要預覽影片，請略過此呼叫。</span><span class="sxs-lookup"><span data-stu-id="19e22-119">Skip this call if you do not want to preview the video.</span></span>

<span data-ttu-id="19e22-120">對於 RenderStream 的這兩個呼叫，媒體類型是媒體類型 \_ ，表示交錯 DV 影片。</span><span class="sxs-lookup"><span data-stu-id="19e22-120">For both calls to RenderStream, the media type is MEDIATYPE\_Interleaved, meaning interleaved DV video.</span></span> <span data-ttu-id="19e22-121">在此程式碼中，「捕獲圖形產生器」會自動新增所需的每個篩選準則，但 MSDV Capture 篩選器除外。</span><span class="sxs-lookup"><span data-stu-id="19e22-121">In this code, the Capture Graph Builder automatically adds every filter that is needed, except for the MSDV capture filter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="19e22-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="19e22-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="19e22-123">DirectShow 中的數位視訊</span><span class="sxs-lookup"><span data-stu-id="19e22-123">Digital Video in DirectShow</span></span>](digital-video-in-directshow.md)
</dt> </dl>

 

 



