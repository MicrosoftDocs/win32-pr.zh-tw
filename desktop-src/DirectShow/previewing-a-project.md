---
description: 預覽專案
ms.assetid: 2efa3f25-a93f-4362-b461-b67475e5d78c
title: 預覽專案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cd9d299a99a0a7315cec986fbc044d427385647
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104317668"
---
# <a name="previewing-a-project"></a><span data-ttu-id="6ae79-103">預覽專案</span><span class="sxs-lookup"><span data-stu-id="6ae79-103">Previewing a Project</span></span>

<span data-ttu-id="6ae79-104">\[此 API 不受支援，而且可能會在未來變更或無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="6ae79-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="6ae79-105">若要預覽專案，請先呼叫 **CoCreateInstance** 來建立基本轉譯引擎的實例。</span><span class="sxs-lookup"><span data-stu-id="6ae79-105">To preview a project, first call **CoCreateInstance** to create an instance of the Basic Render Engine.</span></span> <span data-ttu-id="6ae79-106">類別識別碼是 CLSID \_ RenderEngine。</span><span class="sxs-lookup"><span data-stu-id="6ae79-106">The class identifier is CLSID\_RenderEngine.</span></span> <span data-ttu-id="6ae79-107">然後呼叫 [**IRenderEngine：： SetTimelineObject**](irenderengine-settimelineobject.md) 方法，以指定您要轉譯的時間軸。</span><span class="sxs-lookup"><span data-stu-id="6ae79-107">Then call the [**IRenderEngine::SetTimelineObject**](irenderengine-settimelineobject.md) method to specify the timeline that you are rendering.</span></span>

<span data-ttu-id="6ae79-108">當您第一次預覽時程表時，請依列出的循序執行下列呼叫：</span><span class="sxs-lookup"><span data-stu-id="6ae79-108">The first time that you preview the timeline, perform the following calls in the order listed:</span></span>

1.  <span data-ttu-id="6ae79-109">呼叫 [**IRenderEngine：： SetRenderRange**](irenderengine-setrenderrange.md) ，以指定要預覽的時間軸部分。</span><span class="sxs-lookup"><span data-stu-id="6ae79-109">Call [**IRenderEngine::SetRenderRange**](irenderengine-setrenderrange.md) to specify which portion of the timeline to preview.</span></span> <span data-ttu-id="6ae79-110">(選用)</span><span class="sxs-lookup"><span data-stu-id="6ae79-110">(Optional)</span></span>
2.  <span data-ttu-id="6ae79-111">呼叫 [**IRenderEngine：： ConnectFrontEnd**](irenderengine-connectfrontend.md) 來建立圖形的前端。</span><span class="sxs-lookup"><span data-stu-id="6ae79-111">Call [**IRenderEngine::ConnectFrontEnd**](irenderengine-connectfrontend.md) to build the front end of the graph.</span></span>
3.  <span data-ttu-id="6ae79-112">呼叫 [**IRenderEngine：： RenderOutputPins**](irenderengine-renderoutputpins.md)。</span><span class="sxs-lookup"><span data-stu-id="6ae79-112">Call [**IRenderEngine::RenderOutputPins**](irenderengine-renderoutputpins.md).</span></span> <span data-ttu-id="6ae79-113">此方法會將每個輸出圖釘連接至影片轉譯器或音訊轉譯器，以完成圖形。</span><span class="sxs-lookup"><span data-stu-id="6ae79-113">This method connects each output pin to a video renderer or audio renderer, completing the graph.</span></span>

<span data-ttu-id="6ae79-114">下列程式碼範例會顯示這些步驟：</span><span class="sxs-lookup"><span data-stu-id="6ae79-114">The following code example shows these steps:</span></span>


```C++
IRenderEngine *pRender = NULL; 
hr = CoCreateInstance(CLSID_RenderEngine, NULL, 
    CLSCTX_INPROC_SERVER, IID_IRenderEngine, (void**)&pRender);

hr = pRender->SetTimelineObject(pTL);
hr = pRender->ConnectFrontEnd();
hr = pRender->RenderOutputPins();
```



<span data-ttu-id="6ae79-115">現在執行篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="6ae79-115">Now run the filter graph.</span></span> <span data-ttu-id="6ae79-116">首先，呼叫 [**IRenderEngine：： GetFilterGraph**](irenderengine-getfiltergraph.md) 方法，以取得篩選圖形管理員 [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="6ae79-116">First, call the [**IRenderEngine::GetFilterGraph**](irenderengine-getfiltergraph.md) method to retrieve a pointer to the Filter Graph Manager's [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) interface.</span></span> <span data-ttu-id="6ae79-117">然後查詢 [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) 介面的篩選圖形管理員，然後呼叫 [**IMediaControl：： Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run)，如下列程式碼所示：</span><span class="sxs-lookup"><span data-stu-id="6ae79-117">Then query the Filter Graph Manager for the [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) interface and call [**IMediaControl::Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run), as shown in the following code:</span></span>


```C++
IGraphBuilder   *pGraph = NULL;
IMediaControl   *pControl = NULL;
hr = pRender->GetFilterGraph(&pGraph);
hr = pGraph->QueryInterface(IID_IMediaControl, (void **)&pControl);
hr = pControl->Run();
```



<span data-ttu-id="6ae79-118">使用篩選圖形管理員的 [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) 介面來等候預覽完成。</span><span class="sxs-lookup"><span data-stu-id="6ae79-118">Use the Filter Graph Manager's [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) interface to wait for the preview to complete.</span></span> <span data-ttu-id="6ae79-119">您也可以使用篩選圖形管理員的 [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) 介面來搜尋圖形，就像使用檔案播放圖表一樣。</span><span class="sxs-lookup"><span data-stu-id="6ae79-119">You can also seek the graph using the Filter Graph Manager's [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) interface, just as you would with a file playback graph.</span></span>

<span data-ttu-id="6ae79-120">若要再次預覽專案，請將圖形向上搜尋至時間零，然後再次呼叫 **執行** 。</span><span class="sxs-lookup"><span data-stu-id="6ae79-120">To preview the project again, seek the graph back to time zero and call **Run** again.</span></span> <span data-ttu-id="6ae79-121">如果您變更時間軸的內容，請執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="6ae79-121">If you change the contents of the timeline, do the following:</span></span>

1.  <span data-ttu-id="6ae79-122">呼叫 **SetRenderRange**。</span><span class="sxs-lookup"><span data-stu-id="6ae79-122">Call **SetRenderRange**.</span></span> <span data-ttu-id="6ae79-123">(選用)</span><span class="sxs-lookup"><span data-stu-id="6ae79-123">(Optional)</span></span>
2.  <span data-ttu-id="6ae79-124">呼叫 **ConnectFrontEnd**。</span><span class="sxs-lookup"><span data-stu-id="6ae79-124">Call **ConnectFrontEnd**.</span></span>
3.  <span data-ttu-id="6ae79-125">如果 **ConnectFrontEnd** 方法傳回 S \_ 警告 \_ OUTPUTRESET，請呼叫 **RenderOutputPins**。</span><span class="sxs-lookup"><span data-stu-id="6ae79-125">If the **ConnectFrontEnd** method returns S\_WARN\_OUTPUTRESET, call **RenderOutputPins**.</span></span> <span data-ttu-id="6ae79-126"> (如果 **ConnectFrontEnd** 傳回 S \_ OK，您可以略過此步驟。 ) </span><span class="sxs-lookup"><span data-stu-id="6ae79-126">(If **ConnectFrontEnd** returns S\_OK, you can skip this step.)</span></span>
4.  <span data-ttu-id="6ae79-127">將圖形向後搜尋至時間零。</span><span class="sxs-lookup"><span data-stu-id="6ae79-127">Seek the graph back to time zero.</span></span>
5.  <span data-ttu-id="6ae79-128">執行圖形。</span><span class="sxs-lookup"><span data-stu-id="6ae79-128">Run the graph.</span></span>

<span data-ttu-id="6ae79-129">下列範例會顯示這些步驟：</span><span class="sxs-lookup"><span data-stu-id="6ae79-129">The following example shows these steps:</span></span>


```C++
hr = pRender->ConnectFrontEnd();
if (hr == S_WARN_OUTPUTRESET)
{
    hr = pRender->RenderOutputPins();
}
LONGLONG llStart = 0; 
hr = pSeek->SetPositions(&llStart, AM_SEEKING_AbsolutePositioning, 0, 0); 
hr = pControl->Run();
```



<span data-ttu-id="6ae79-130">如需載入和預覽專案檔的完整範例，請參閱 [載入和預覽專案](loading-and-previewing-a-project.md)。</span><span class="sxs-lookup"><span data-stu-id="6ae79-130">For a complete example that loads and previews a project file, see [Loading and Previewing a Project](loading-and-previewing-a-project.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="6ae79-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="6ae79-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6ae79-132">管理影片編輯專案</span><span class="sxs-lookup"><span data-stu-id="6ae79-132">Managing Video Editing Projects</span></span>](managing-video-editing-projects.md)
</dt> <dt>

[<span data-ttu-id="6ae79-133">轉譯專案</span><span class="sxs-lookup"><span data-stu-id="6ae79-133">Rendering a Project</span></span>](rendering-a-project.md)
</dt> </dl>

 

 



