---
description: 此範例會使用 DirectShow 中的 ICaptureGraphBuilder2：： RenderStream 方法來建立影片預覽圖形。
ms.assetid: 9b401de1-910a-41f7-bf80-dda73ee4a204
title: '預覽影片 (DirectShow) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 482fed2e164bbe867d848b05d417c89d0790256f
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406891"
---
# <a name="previewing-video-directshow"></a><span data-ttu-id="2d540-103">預覽影片 (DirectShow) </span><span class="sxs-lookup"><span data-stu-id="2d540-103">Previewing Video (DirectShow)</span></span>

<span data-ttu-id="2d540-104">若要建立影片預覽圖形，請呼叫 [**ICaptureGraphBuilder2：： RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) 方法，如下所示：</span><span class="sxs-lookup"><span data-stu-id="2d540-104">To build a video preview graph, call the [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method as follows:</span></span>


```C++
ICaptureGraphBuilder2 *pBuild; // Capture Graph Builder
// Initialize pBuild (not shown).

IBaseFilter *pCap; // Video capture filter.

/* Initialize pCap and add it to the filter graph (not shown). */

hr = pBuild->RenderStream(&PIN_CATEGORY_PREVIEW, &MEDIATYPE_Video, 
    pCap, NULL, NULL);
```



<span data-ttu-id="2d540-105">此範例假設下列各項：</span><span class="sxs-lookup"><span data-stu-id="2d540-105">This example assumes the following:</span></span>

-   <span data-ttu-id="2d540-106">*pBuild* 已初始化，如 [關於 Capture Graph Builder](about-the-capture-graph-builder.md)中所述。</span><span class="sxs-lookup"><span data-stu-id="2d540-106">*pBuild* was initialized, as described in [About the Capture Graph Builder](about-the-capture-graph-builder.md).</span></span>
-   <span data-ttu-id="2d540-107">*pCap* 已初始化，方法是建立 capture 篩選器的實例，並將它新增至篩選圖形（如 [選取捕獲裝置](selecting-a-capture-device.md)所述）。</span><span class="sxs-lookup"><span data-stu-id="2d540-107">*pCap* was initialized, by creating an instance of the capture filter and adding it to the filter graph, as described in [Selecting a Capture Device](selecting-a-capture-device.md).</span></span>

<span data-ttu-id="2d540-108">[**ICaptureGraphBuilder2：： RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream)方法的第一個參數會指定釘選類別。針對預覽圖形，請使用 **PIN \_ 類別 \_ 預覽**。</span><span class="sxs-lookup"><span data-stu-id="2d540-108">The first parameter to the [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method specifies a pin category; for a preview graph, use **PIN\_CATEGORY\_PREVIEW**.</span></span> <span data-ttu-id="2d540-109">第二個參數會將媒體類型指定為主要類型 GUID。</span><span class="sxs-lookup"><span data-stu-id="2d540-109">The second parameter specifies a media type, as a major type GUID.</span></span> <span data-ttu-id="2d540-110">如需影片，請使用 **媒體媒體的 \_ 影片**。</span><span class="sxs-lookup"><span data-stu-id="2d540-110">For video, use **MEDIATYPE\_Video**.</span></span> <span data-ttu-id="2d540-111">DV 裝置提供交錯的音訊和影片，媒體類型是媒體類型 **的 \_ 交錯**。</span><span class="sxs-lookup"><span data-stu-id="2d540-111">DV devices deliver interleaved audio and video, for which the media type is **MEDIATYPE\_Interleaved**.</span></span> <span data-ttu-id="2d540-112"> (如需 DV 捕捉的詳細資訊，請參閱 [DirectShow 中的數位視訊](digital-video-in-directshow.md)) </span><span class="sxs-lookup"><span data-stu-id="2d540-112">(For more information about DV capture, see [Digital Video in DirectShow](digital-video-in-directshow.md).)</span></span>

<span data-ttu-id="2d540-113">第三個參數是捕獲篩選器 [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="2d540-113">The third parameter is a pointer to the capture filter's [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface.</span></span> <span data-ttu-id="2d540-114">在此範例中，不需要接下來的兩個參數。</span><span class="sxs-lookup"><span data-stu-id="2d540-114">The next two parameters are not needed in this example.</span></span> <span data-ttu-id="2d540-115">它們可用來指定轉譯資料流程時可能需要的其他篩選。</span><span class="sxs-lookup"><span data-stu-id="2d540-115">They are used to specify additional filters that might be needed to render the stream.</span></span> <span data-ttu-id="2d540-116">將最後一個參數設定為 **Null** ，會使「捕獲圖形產生器」根據媒體類型選取資料流程的預設轉譯器。</span><span class="sxs-lookup"><span data-stu-id="2d540-116">Setting the last parameter to **NULL** causes the Capture Graph Builder to select a default renderer for the stream, based on the media type.</span></span> <span data-ttu-id="2d540-117">若為影片，「捕獲圖形產生器」一律會使用 [影片](video-renderer-filter.md) 轉譯器篩選作為預設轉譯器。</span><span class="sxs-lookup"><span data-stu-id="2d540-117">For video, the Capture Graph Builder always uses the [Video Renderer](video-renderer-filter.md) filter as the default renderer.</span></span>

> [!Note]  
> <span data-ttu-id="2d540-118">在 Windows XP 和更新版本中，雖然 (VMR) 的影片混合轉譯器是 [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) 方法的預設影片轉譯器，但它並不是 [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) 方法的預設轉譯器。</span><span class="sxs-lookup"><span data-stu-id="2d540-118">In Windows XP and later, although the Video Mixing Renderer (VMR) is the default video renderer for [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) methods, it is not the default renderer for the [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method.</span></span> <span data-ttu-id="2d540-119">在任何平臺上，除非您另行指定，否則「捕捉圖形產生器」一律會使用舊的「影片轉譯器」篩選。</span><span class="sxs-lookup"><span data-stu-id="2d540-119">On any platform, the Capture Graph Builder always uses the old Video Renderer filter unless you specify otherwise.</span></span>

 

<span data-ttu-id="2d540-120">雖然 pin 類別是以釘選 **\_ 類別 \_ 預覽** 的形式提供，但篩選準則實際上是否有預覽釘選，但它可以有影片埠 pin 或只是捕捉 pin。</span><span class="sxs-lookup"><span data-stu-id="2d540-120">Although the pin category is given as **PIN\_CATEGORY\_PREVIEW**, it does not matter whether the filter actually has a preview pin; it could have a video port pin or just a capture pin.</span></span> <span data-ttu-id="2d540-121">無論是哪一種情況，[Capture Graph Builder] 都會自動建立正確的圖形。</span><span class="sxs-lookup"><span data-stu-id="2d540-121">In either case, the Capture Graph Builder automatically builds the correct graph.</span></span>

<span data-ttu-id="2d540-122">下圖顯示預覽影片的最簡單圖形。</span><span class="sxs-lookup"><span data-stu-id="2d540-122">The following diagram shows the simplest possible graph for previewing video.</span></span>

![影片預覽圖形](images/vidcap01.png)

<span data-ttu-id="2d540-124">在此圖中，capture 篩選器具有預覽 pin，可直接連接到影片轉譯器。</span><span class="sxs-lookup"><span data-stu-id="2d540-124">In this diagram, the capture filter has a preview pin, which connects directly to the video renderer.</span></span>

<span data-ttu-id="2d540-125">如果「捕捉」篩選只有一個「捕捉」釘選，「捕獲圖形產生器」會插入一個 [智慧型](smart-tee-filter.md) 指標篩選器，它會將資料流程分割成捕獲資料流程和預覽資料流程。</span><span class="sxs-lookup"><span data-stu-id="2d540-125">If the capture filter has only a capture pin, the Capture Graph Builder inserts a [Smart Tee](smart-tee-filter.md) filter, which splits the stream into a capture stream and a preview stream.</span></span> <span data-ttu-id="2d540-126">[結合影片捕獲和預覽](combining-video-capture-and-preview.md)會更詳細地說明這一點。</span><span class="sxs-lookup"><span data-stu-id="2d540-126">This is described in more detail in [Combining Video Capture and Preview](combining-video-capture-and-preview.md).</span></span>

<span data-ttu-id="2d540-127">在某些情況下，影片串流必須經過覆迭混音器篩選器。</span><span class="sxs-lookup"><span data-stu-id="2d540-127">In some cases, the video stream must go through the Overlay Mixer filter.</span></span> <span data-ttu-id="2d540-128">如果是， [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) 方法會自動將它新增至圖形。</span><span class="sxs-lookup"><span data-stu-id="2d540-128">If so, the [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method adds it to the graph automatically.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2d540-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="2d540-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2d540-130">結合影片捕獲和預覽</span><span class="sxs-lookup"><span data-stu-id="2d540-130">Combining Video Capture and Preview</span></span>](combining-video-capture-and-preview.md)
</dt> <dt>

[<span data-ttu-id="2d540-131">影片捕獲</span><span class="sxs-lookup"><span data-stu-id="2d540-131">Video Capture</span></span>](video-capture.md)
</dt> </dl>

 

 



