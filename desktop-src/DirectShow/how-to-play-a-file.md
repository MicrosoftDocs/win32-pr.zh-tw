---
description: 如何播放檔案
ms.assetid: 3d8c5d06-8690-4298-a1d1-f21af35bcfd4
title: 如何播放檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc84ef751db318354da36454e6a30fd2ce4bd8e7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104385803"
---
# <a name="how-to-play-a-file"></a><span data-ttu-id="2e2f5-103">如何播放檔案</span><span class="sxs-lookup"><span data-stu-id="2e2f5-103">How To Play a File</span></span>

<span data-ttu-id="2e2f5-104">本文旨在提供您 DirectShow 程式設計的特色。</span><span class="sxs-lookup"><span data-stu-id="2e2f5-104">This article is intended to give you the flavor of DirectShow programming.</span></span> <span data-ttu-id="2e2f5-105">它會顯示一個簡單的主控台應用程式，可播放音訊或影片檔案。</span><span class="sxs-lookup"><span data-stu-id="2e2f5-105">It presents a simple console application that plays an audio or video file.</span></span> <span data-ttu-id="2e2f5-106">程式只有幾行時間，但它會示範一些 DirectShow 程式設計的威力。</span><span class="sxs-lookup"><span data-stu-id="2e2f5-106">The program is only a few lines long, but it demonstrates some of the power of DirectShow programming.</span></span>

<span data-ttu-id="2e2f5-107">在「 [Directshow 應用程式程式設計」簡介](introduction-to-directshow-application-programming.md) 文章中，directshow 應用程式一律會執行相同的基本步驟：</span><span class="sxs-lookup"><span data-stu-id="2e2f5-107">As the article [Introduction to DirectShow Application Programming](introduction-to-directshow-application-programming.md) describes, a DirectShow application always performs the same basic steps:</span></span>

1.  <span data-ttu-id="2e2f5-108">建立 [篩選圖形管理員](filter-graph-manager.md)的實例。</span><span class="sxs-lookup"><span data-stu-id="2e2f5-108">Create an instance of the [Filter Graph Manager](filter-graph-manager.md).</span></span>
2.  <span data-ttu-id="2e2f5-109">使用篩選圖形管理員來建立篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="2e2f5-109">Use the Filter Graph Manager to build a filter graph.</span></span>
3.  <span data-ttu-id="2e2f5-110">執行圖形，使資料在篩選準則下移動。</span><span class="sxs-lookup"><span data-stu-id="2e2f5-110">Run the graph, causing data to move through the filters.</span></span>

<span data-ttu-id="2e2f5-111">若要編譯及連結此主題中的程式碼，請包含標頭檔 Dshow，並連結至靜態程式庫檔案 strmiids。</span><span class="sxs-lookup"><span data-stu-id="2e2f5-111">To compile and link the code in this topic, include the header file Dshow.h and link to the static library file strmiids.lib.</span></span> <span data-ttu-id="2e2f5-112">如需詳細資訊，請參閱 [建立 DirectShow 應用程式](setting-up-the-build-environment.md)。</span><span class="sxs-lookup"><span data-stu-id="2e2f5-112">For more information, see [Building DirectShow Applications](setting-up-the-build-environment.md).</span></span>

<span data-ttu-id="2e2f5-113">首先，呼叫 [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) 或 [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) 初始化 COM 程式庫：</span><span class="sxs-lookup"><span data-stu-id="2e2f5-113">Start by calling [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) or [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) to initialize the COM library:</span></span>


```C++
HRESULT hr = CoInitialize(NULL);
if (FAILED(hr))
{
    // Add error-handling code here. (Omitted for clarity.)
}
```



<span data-ttu-id="2e2f5-114">為了簡單起見，此範例會忽略傳回值，但您應該一律從任何方法呼叫中檢查 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="2e2f5-114">To keep things simple, this example ignores the return value, but you should always check the **HRESULT** value from any method call.</span></span>

<span data-ttu-id="2e2f5-115">接下來，呼叫 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) 以建立篩選圖形管理員：</span><span class="sxs-lookup"><span data-stu-id="2e2f5-115">Next, call [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) to create the Filter Graph Manager:</span></span>


```C++
IGraphBuilder *pGraph;
HRESULT hr = CoCreateInstance(CLSID_FilterGraph, NULL, 
    CLSCTX_INPROC_SERVER, IID_IGraphBuilder, (void **)&pGraph);
```



<span data-ttu-id="2e2f5-116">如所示， (CLSID) 的類別識別碼是 CLSID \_ FilterGraph。</span><span class="sxs-lookup"><span data-stu-id="2e2f5-116">As shown, the class identifier (CLSID) is CLSID\_FilterGraph.</span></span> <span data-ttu-id="2e2f5-117">篩選圖形管理員是由同進程 DLL 提供，因此執行內容是 **CLSCTX \_ INPROC \_ SERVER**。</span><span class="sxs-lookup"><span data-stu-id="2e2f5-117">The Filter Graph Manager is provided by an in-process DLL, so the execution context is **CLSCTX\_INPROC\_SERVER**.</span></span> <span data-ttu-id="2e2f5-118">DirectShow 支援自由執行緒模型，因此您也可以使用 **COINIT \_ 多執行緒** 旗標來呼叫 [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) 。</span><span class="sxs-lookup"><span data-stu-id="2e2f5-118">DirectShow supports the free-threading model, so you can also call [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) with the **COINIT\_MULTITHREADED** flag.</span></span>

<span data-ttu-id="2e2f5-119">對 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) 的呼叫會傳回 [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) 介面，此介面大多包含用來建立篩選圖形的方法。</span><span class="sxs-lookup"><span data-stu-id="2e2f5-119">The call to [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) returns the [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) interface, which mostly contains methods for building the filter graph.</span></span> <span data-ttu-id="2e2f5-120">此範例需要兩個其他介面：</span><span class="sxs-lookup"><span data-stu-id="2e2f5-120">Two other interfaces are needed for this example:</span></span>

-   <span data-ttu-id="2e2f5-121">[**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) 控制項串流處理。</span><span class="sxs-lookup"><span data-stu-id="2e2f5-121">[**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) controls streaming.</span></span> <span data-ttu-id="2e2f5-122">它包含用來停止和啟動圖形的方法。</span><span class="sxs-lookup"><span data-stu-id="2e2f5-122">It contains methods for stopping and starting the graph.</span></span>
-   <span data-ttu-id="2e2f5-123">[**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) 具有從篩選圖形管理員取得事件的方法。</span><span class="sxs-lookup"><span data-stu-id="2e2f5-123">[**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) has methods for getting events from the Filter Graph Manager.</span></span> <span data-ttu-id="2e2f5-124">在此範例中，會使用介面來等候播放完成。</span><span class="sxs-lookup"><span data-stu-id="2e2f5-124">In this example, the interface is used to wait for playback to complete.</span></span>

<span data-ttu-id="2e2f5-125">這兩個介面都是由篩選圖形管理員所公開。</span><span class="sxs-lookup"><span data-stu-id="2e2f5-125">Both of these interfaces are exposed by the Filter Graph Manager.</span></span> <span data-ttu-id="2e2f5-126">使用傳回的 [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) 指標來查詢它們：</span><span class="sxs-lookup"><span data-stu-id="2e2f5-126">Use the returned [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) pointer to query for them:</span></span>


```C++
IMediaControl *pControl;
IMediaEvent   *pEvent;
hr = pGraph->QueryInterface(IID_IMediaControl, (void **)&pControl);
hr = pGraph->QueryInterface(IID_IMediaEvent, (void **)&pEvent);
```



<span data-ttu-id="2e2f5-127">現在您可以建立篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="2e2f5-127">Now you can build the filter graph.</span></span> <span data-ttu-id="2e2f5-128">針對檔案播放，這是透過單一方法呼叫來完成：</span><span class="sxs-lookup"><span data-stu-id="2e2f5-128">For file playback, this is done by a single method call:</span></span>


```C++
hr = pGraph->RenderFile(L"C:\\Example.avi", NULL);
```



<span data-ttu-id="2e2f5-129">[**IGraphBuilder：： RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile)方法會建立可播放指定檔案的篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="2e2f5-129">The [**IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) method builds a filter graph that can play the specified file.</span></span> <span data-ttu-id="2e2f5-130">第一個參數是檔案名，以寬字元表示 (2 位元組) 字串。</span><span class="sxs-lookup"><span data-stu-id="2e2f5-130">The first parameter is the file name, represented as a wide character (2-byte) string.</span></span> <span data-ttu-id="2e2f5-131">第二個參數是保留的，而且必須等於 **Null**。</span><span class="sxs-lookup"><span data-stu-id="2e2f5-131">The second parameter is reserved and must equal **NULL**.</span></span>

<span data-ttu-id="2e2f5-132">如果指定的檔案不存在，或無法辨識檔案格式，這個方法可能會失敗。</span><span class="sxs-lookup"><span data-stu-id="2e2f5-132">This method can fail if the specified file does not exist, or the file format is not recognized.</span></span> <span data-ttu-id="2e2f5-133">不過，假設此方法成功，則篩選圖形現在已準備好進行播放。</span><span class="sxs-lookup"><span data-stu-id="2e2f5-133">Assuming that the method succeeds, however, the filter graph is now ready for playback.</span></span> <span data-ttu-id="2e2f5-134">若要執行圖形，請呼叫 [**IMediaControl：： run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) 方法：</span><span class="sxs-lookup"><span data-stu-id="2e2f5-134">To run the graph, call the [**IMediaControl::Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) method:</span></span>


```C++
hr = pControl->Run();
```



<span data-ttu-id="2e2f5-135">當篩選圖形執行時，資料會在篩選器中移動，並轉譯成影片和音訊。</span><span class="sxs-lookup"><span data-stu-id="2e2f5-135">When the filter graph runs, data moves through the filters and is rendered as video and audio.</span></span> <span data-ttu-id="2e2f5-136">播放會在個別的執行緒上執行。</span><span class="sxs-lookup"><span data-stu-id="2e2f5-136">Playback occurs on a separate thread.</span></span> <span data-ttu-id="2e2f5-137">您可以藉由呼叫 [**IMediaEvent：： WaitForCompletion**](/windows/desktop/api/Control/nf-control-imediaevent-waitforcompletion) 方法來等候播放完成：</span><span class="sxs-lookup"><span data-stu-id="2e2f5-137">You can wait for playback to complete by calling the [**IMediaEvent::WaitForCompletion**](/windows/desktop/api/Control/nf-control-imediaevent-waitforcompletion) method:</span></span>


```C++
long evCode = 0;
pEvent->WaitForCompletion(INFINITE, &evCode);
```



<span data-ttu-id="2e2f5-138">這個方法會封鎖直到檔案完成播放為止，或直到指定的逾時間隔到期為止。</span><span class="sxs-lookup"><span data-stu-id="2e2f5-138">This method blocks until the file is done playing, or until the specified time-out interval elapses.</span></span> <span data-ttu-id="2e2f5-139">值無限大表示應用程式會無限期地封鎖，直到檔案完成播放為止。</span><span class="sxs-lookup"><span data-stu-id="2e2f5-139">The value INFINITE means the application blocks indefinitely until the file is done playing.</span></span> <span data-ttu-id="2e2f5-140">如需事件處理的更實際範例，請參閱 [回應事件](responding-to-events.md)。</span><span class="sxs-lookup"><span data-stu-id="2e2f5-140">For a more realistic example of event handling, see [Responding to Events](responding-to-events.md).</span></span>

<span data-ttu-id="2e2f5-141">當應用程式完成時，請釋放介面指標並關閉 COM 程式庫：</span><span class="sxs-lookup"><span data-stu-id="2e2f5-141">When the application is finished, release the interface pointers and close the COM library:</span></span>


```C++
pControl->Release();
pEvent->Release();
pGraph->Release();
CoUninitialize();
```



## <a name="example-code"></a><span data-ttu-id="2e2f5-142">範例程式碼</span><span class="sxs-lookup"><span data-stu-id="2e2f5-142">Example Code</span></span>

<span data-ttu-id="2e2f5-143">以下是本文所述範例的完整程式碼：</span><span class="sxs-lookup"><span data-stu-id="2e2f5-143">Here is the complete code for the example described in this article:</span></span>


```C++
#include <dshow.h>
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

    // Create the filter graph manager and query for interfaces.
    hr = CoCreateInstance(CLSID_FilterGraph, NULL, CLSCTX_INPROC_SERVER, 
                        IID_IGraphBuilder, (void **)&pGraph);
    if (FAILED(hr))
    {
        printf("ERROR - Could not create the Filter Graph Manager.");
        return;
    }

    hr = pGraph->QueryInterface(IID_IMediaControl, (void **)&pControl);
    hr = pGraph->QueryInterface(IID_IMediaEvent, (void **)&pEvent);

    // Build the graph. IMPORTANT: Change this string to a file on your system.
    hr = pGraph->RenderFile(L"C:\\Example.avi", NULL);
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



## <a name="related-topics"></a><span data-ttu-id="2e2f5-144">相關主題</span><span class="sxs-lookup"><span data-stu-id="2e2f5-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2e2f5-145">基本的 DirectShow 工作</span><span class="sxs-lookup"><span data-stu-id="2e2f5-145">Basic DirectShow Tasks</span></span>](basic-directshow-tasks.md)
</dt> </dl>

 

 
