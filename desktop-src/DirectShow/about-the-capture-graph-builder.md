---
description: 關於 Capture Graph Builder
ms.assetid: 9399a06e-7305-41e8-aefe-3d158052a8ed
title: 關於 Capture Graph Builder
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae321665e0eae65a1d464bf87a12ac33e935d7ac
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103935951"
---
# <a name="about-the-capture-graph-builder"></a><span data-ttu-id="14f49-103">關於 Capture Graph Builder</span><span class="sxs-lookup"><span data-stu-id="14f49-103">About the Capture Graph Builder</span></span>

<span data-ttu-id="14f49-104">執行影片或音訊捕獲的篩選圖形稱為「 *捕獲圖形*」。</span><span class="sxs-lookup"><span data-stu-id="14f49-104">A filter graph that performs video or audio capture is called a *capture graph*.</span></span> <span data-ttu-id="14f49-105">捕捉圖形通常比檔案播放圖形更為複雜。</span><span class="sxs-lookup"><span data-stu-id="14f49-105">Capture graphs are often more complicated than file playback graphs.</span></span> <span data-ttu-id="14f49-106">為了讓應用程式更容易建立組建圖形，DirectShow 提供了一個 helper 物件，稱為「捕獲圖形產生器」。</span><span class="sxs-lookup"><span data-stu-id="14f49-106">To make it easier for applications to build capture graphs, DirectShow provides a helper object called the Capture Graph Builder.</span></span> <span data-ttu-id="14f49-107">「Capture Graph 建立器」會公開 [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) 介面，其中包含用來建立和控制捕捉圖形的方法。</span><span class="sxs-lookup"><span data-stu-id="14f49-107">The Capture Graph Builder exposes the [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) interface, which contains methods for building and controlling a capture graph.</span></span> <span data-ttu-id="14f49-108">下圖說明 [Capture Graph Builder] 和 [ **ICaptureGraphBuilder2** ] 介面。</span><span class="sxs-lookup"><span data-stu-id="14f49-108">The following diagram illustrates the Capture Graph Builder and the **ICaptureGraphBuilder2** interface.</span></span>

![使用 capture graph builder](images/cgb01.png)

<span data-ttu-id="14f49-110">首先，呼叫 CoCreateInstance 以建立「Capture Graph 建立器」和「篩選圖形管理員」的新實例。</span><span class="sxs-lookup"><span data-stu-id="14f49-110">Start by calling CoCreateInstance to create new instances of the Capture Graph Builder and the Filter Graph Manager.</span></span> <span data-ttu-id="14f49-111">然後藉由呼叫 [**ICaptureGraphBuilder2：： SetFiltergraph**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setfiltergraph) 與篩選圖形管理員 [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) 介面的指標，初始化 Capture Graph Builder。</span><span class="sxs-lookup"><span data-stu-id="14f49-111">Then initialize the Capture Graph Builder by calling [**ICaptureGraphBuilder2::SetFiltergraph**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setfiltergraph) with a pointer to the Filter Graph Manager's [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) interface.</span></span> <span data-ttu-id="14f49-112">下圖說明此程序。</span><span class="sxs-lookup"><span data-stu-id="14f49-112">The following diagram illustrates this process.</span></span>

![初始化 capture graph builder](images/cgb03.png)

<span data-ttu-id="14f49-114">下列程式碼顯示 helper 函式來執行這些步驟：</span><span class="sxs-lookup"><span data-stu-id="14f49-114">The following code shows a helper function to perform these steps:</span></span>


```C++
HRESULT InitCaptureGraphBuilder(
  IGraphBuilder **ppGraph,  // Receives the pointer.
  ICaptureGraphBuilder2 **ppBuild  // Receives the pointer.
)
{
    if (!ppGraph || !ppBuild)
    {
        return E_POINTER;
    }
    IGraphBuilder *pGraph = NULL;
    ICaptureGraphBuilder2 *pBuild = NULL;

    // Create the Capture Graph Builder.
    HRESULT hr = CoCreateInstance(CLSID_CaptureGraphBuilder2, NULL, 
        CLSCTX_INPROC_SERVER, IID_ICaptureGraphBuilder2, (void**)&pBuild );
    if (SUCCEEDED(hr))
    {
        // Create the Filter Graph Manager.
        hr = CoCreateInstance(CLSID_FilterGraph, 0, CLSCTX_INPROC_SERVER,
            IID_IGraphBuilder, (void**)&pGraph);
        if (SUCCEEDED(hr))
        {
            // Initialize the Capture Graph Builder.
            pBuild->SetFiltergraph(pGraph);

            // Return both interface pointers to the caller.
            *ppBuild = pBuild;
            *ppGraph = pGraph; // The caller must release both interfaces.
            return S_OK;
        }
        else
        {
            pBuild->Release();
        }
    }
    return hr; // Failed
}
```



<span data-ttu-id="14f49-115">在本節中，我們會假設您使用的是「Capture Graph 建立器」來建立「capture graph」。</span><span class="sxs-lookup"><span data-stu-id="14f49-115">Throughout this section on video capture, it is assumed that you are using the Capture Graph Builder to create the capture graph.</span></span> <span data-ttu-id="14f49-116">不過，您可以使用 IGraphBuilder 方法，完全建立 capture 圖形。</span><span class="sxs-lookup"><span data-stu-id="14f49-116">However, it is possible to build capture graphs entirely by using IGraphBuilder methods.</span></span> <span data-ttu-id="14f49-117">不過，這是一個很好的主題，而且偏好使用 Capture Graph Builder 方法。</span><span class="sxs-lookup"><span data-stu-id="14f49-117">This is considered an advanced topic, however, and the Capture Graph Builder methods are preferred.</span></span> <span data-ttu-id="14f49-118">如需詳細資訊，請參閱「 [Advanced Capture」主題](advanced-capture-topics.md)。</span><span class="sxs-lookup"><span data-stu-id="14f49-118">For more information, see [Advanced Capture Topics](advanced-capture-topics.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="14f49-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="14f49-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="14f49-120">關於 DirectShow 中的影片捕獲</span><span class="sxs-lookup"><span data-stu-id="14f49-120">About Video Capture in DirectShow</span></span>](about-video-capture-in-directshow.md)
</dt> </dl>

 

 



