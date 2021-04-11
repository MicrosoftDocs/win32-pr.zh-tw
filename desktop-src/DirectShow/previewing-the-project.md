---
description: 預覽專案
ms.assetid: 00d72a39-f848-47ea-8460-8b826684eeea
title: 預覽專案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bdf38fe19e500cfe9bd9a8dfb77f7ff56528a2f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103935927"
---
# <a name="previewing-the-project"></a><span data-ttu-id="242ab-103">預覽專案</span><span class="sxs-lookup"><span data-stu-id="242ab-103">Previewing the Project</span></span>

<span data-ttu-id="242ab-104">\[此 API 不受支援，而且可能會在未來變更或無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="242ab-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="242ab-105">若要預覽專案，您需要一個稱為轉譯 *引擎* 的元件，該元件會從時間軸建立 DirectShow 篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="242ab-105">To preview the project, you need a component called a *render engine*, which builds a DirectShow filter graph from a timeline.</span></span> <span data-ttu-id="242ab-106">篩選圖形是實際呈現專案的專案。</span><span class="sxs-lookup"><span data-stu-id="242ab-106">The filter graph is what actually renders the project.</span></span> <span data-ttu-id="242ab-107">您可以使用轉譯引擎來預覽專案或寫入最終輸出檔。</span><span class="sxs-lookup"><span data-stu-id="242ab-107">You can use the render engine to preview a project or to write the final output file.</span></span>

<span data-ttu-id="242ab-108">本文不會詳細說明轉譯引擎。</span><span class="sxs-lookup"><span data-stu-id="242ab-108">This article does not go into detail about the render engine.</span></span> <span data-ttu-id="242ab-109">針對預覽，您只需要幾個方法呼叫。</span><span class="sxs-lookup"><span data-stu-id="242ab-109">For preview, you only need a few method calls.</span></span> <span data-ttu-id="242ab-110">您可以在轉譯 [專案](rendering-a-project.md)中找到更詳盡的討論，包括如何寫入輸出檔。</span><span class="sxs-lookup"><span data-stu-id="242ab-110">You can find a more thorough discussion, including how to write output files, in [Rendering a Project](rendering-a-project.md).</span></span> <span data-ttu-id="242ab-111">下列程式碼範例顯示如何建立預覽圖形。</span><span class="sxs-lookup"><span data-stu-id="242ab-111">The following code example shows how to construct a preview graph.</span></span>


```C++
IRenderEngine *pRender = NULL; 
hr = CoCreateInstance(CLSID_RenderEngine, NULL, CLSCTX_INPROC_SERVER,
            IID_IRenderEngine, (void**) &pRender);

hr = pRender->SetTimelineObject(pTL);
hr = pRender->ConnectFrontEnd( );
hr = pRender->RenderOutputPins( );
```



<span data-ttu-id="242ab-112">使用 **CoCreateInstance** 函數建立轉譯引擎。</span><span class="sxs-lookup"><span data-stu-id="242ab-112">Create the render engine using the **CoCreateInstance** function.</span></span> <span data-ttu-id="242ab-113">然後，在轉譯引擎的 [**IRenderEngine**](irenderengine.md) 介面上呼叫下列方法：</span><span class="sxs-lookup"><span data-stu-id="242ab-113">Then call the following methods on the render engine's [**IRenderEngine**](irenderengine.md) interface:</span></span>

-   <span data-ttu-id="242ab-114">[**SetTimelineObject**](irenderengine-settimelineobject.md)。</span><span class="sxs-lookup"><span data-stu-id="242ab-114">[**SetTimelineObject**](irenderengine-settimelineobject.md).</span></span> <span data-ttu-id="242ab-115">指定要使用的時間軸。</span><span class="sxs-lookup"><span data-stu-id="242ab-115">Specifies the timeline to use.</span></span>
-   <span data-ttu-id="242ab-116">[**ConnectFrontEnd**](irenderengine-connectfrontend.md)。</span><span class="sxs-lookup"><span data-stu-id="242ab-116">[**ConnectFrontEnd**](irenderengine-connectfrontend.md).</span></span> <span data-ttu-id="242ab-117">建立部分篩選圖形，其中每個群組的輸出釘選在時間軸中。</span><span class="sxs-lookup"><span data-stu-id="242ab-117">Builds a partial filter graph, with one output pin for each group in the timeline.</span></span>
-   <span data-ttu-id="242ab-118">[**RenderOutputPins**](irenderengine-renderoutputpins.md)。</span><span class="sxs-lookup"><span data-stu-id="242ab-118">[**RenderOutputPins**](irenderengine-renderoutputpins.md).</span></span> <span data-ttu-id="242ab-119">將每個輸出圖釘連接至影片或音訊轉譯器，以完成預覽圖形。</span><span class="sxs-lookup"><span data-stu-id="242ab-119">Completes the preview graph by connecting each output pin to a video or audio renderer.</span></span>

<span data-ttu-id="242ab-120">建立圖表之後，您可以執行圖形來預覽專案，就像使用任何 DirectShow 篩選圖形一樣。</span><span class="sxs-lookup"><span data-stu-id="242ab-120">Once the graph is built, you can preview the project by running the graph, as you would with any DirectShow filter graph.</span></span> <span data-ttu-id="242ab-121">首先，藉由呼叫 [**IRenderEngine：： GetFilterGraph**](irenderengine-getfiltergraph.md) 方法來取得篩選圖形的指標。</span><span class="sxs-lookup"><span data-stu-id="242ab-121">First, obtain a pointer to the filter graph by calling the [**IRenderEngine::GetFilterGraph**](irenderengine-getfiltergraph.md) method.</span></span>


```C++
IGraphBuilder   *pGraph = NULL;
hr = pRender->GetFilterGraph(&pGraph);
```



<span data-ttu-id="242ab-122">查詢 [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) 和 [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) 介面的篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="242ab-122">Query the filter graph for the [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) and [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) interfaces.</span></span> <span data-ttu-id="242ab-123">您可以使用這兩個介面來執行圖形，並等候播放完成。</span><span class="sxs-lookup"><span data-stu-id="242ab-123">Use these two interfaces to run the graph and wait for playback to complete.</span></span> <span data-ttu-id="242ab-124">如需如何使用這些介面的說明，請參閱 [如何播放](how-to-play-a-file.md) 檔案和 [回應事件](responding-to-events.md)。</span><span class="sxs-lookup"><span data-stu-id="242ab-124">For an explanation of how to use these interfaces, see [How To Play a File](how-to-play-a-file.md) and [Responding to Events](responding-to-events.md).</span></span> <span data-ttu-id="242ab-125">下列程式碼顯示使用這些介面的一種方式。</span><span class="sxs-lookup"><span data-stu-id="242ab-125">The following code shows one way to use these interfaces.</span></span>


```C++
IMediaControl   *pControl = NULL;
IMediaEvent     *pEvent = NULL;
long evCode;
pGraph->QueryInterface(IID_IMediaControl, (void **)&pControl);
pGraph->QueryInterface(IID_IMediaEvent, (void **)&pEvent);
hr = pControl->Run();
hr = pEvent->WaitForCompletion(INFINITE, &evCode);
pControl->Stop();
```



<span data-ttu-id="242ab-126">此範例中的程式碼會封鎖程式執行，直到播放完成為止，因為 [**IMediaEvent：： WaitForCompletion**](/windows/desktop/api/Control/nf-control-imediaevent-waitforcompletion) 方法呼叫中有無限的參數。</span><span class="sxs-lookup"><span data-stu-id="242ab-126">The code in this example blocks program execution until playback completes, because of the INFINITE parameter in the [**IMediaEvent::WaitForCompletion**](/windows/desktop/api/Control/nf-control-imediaevent-waitforcompletion) method call.</span></span> <span data-ttu-id="242ab-127">但是，如果在播放期間發生錯誤，可能會導致程式停止回應。</span><span class="sxs-lookup"><span data-stu-id="242ab-127">If something goes wrong during playback, however, it could cause the program to stop responding.</span></span> <span data-ttu-id="242ab-128">在實際的應用程式中，使用訊息迴圈來等候播放完成。</span><span class="sxs-lookup"><span data-stu-id="242ab-128">In a real application, use a message loop to wait for playback to complete.</span></span> <span data-ttu-id="242ab-129">此外，也建議您為使用者提供中斷播放的方式。</span><span class="sxs-lookup"><span data-stu-id="242ab-129">It's also recommended that you provide the user with a way to interrupt playback.</span></span>

<span data-ttu-id="242ab-130">當您完成使用轉譯引擎時，請一律呼叫 [**IRenderEngine：： ScrapIt**](irenderengine-scrapit.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="242ab-130">When you finish using the render engine, always call the [**IRenderEngine::ScrapIt**](irenderengine-scrapit.md) method.</span></span> <span data-ttu-id="242ab-131">這個方法會刪除篩選圖形，並釋放轉譯引擎所持有的任何資源。</span><span class="sxs-lookup"><span data-stu-id="242ab-131">This method deletes the filter graph and releases any resources held by the render engine.</span></span>


```C++
pRender->ScrapIt();
```



## <a name="related-topics"></a><span data-ttu-id="242ab-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="242ab-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="242ab-133">載入和預覽專案</span><span class="sxs-lookup"><span data-stu-id="242ab-133">Loading and Previewing a Project</span></span>](loading-and-previewing-a-project.md)
</dt> </dl>

 

 



