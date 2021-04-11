---
description: 本主題說明用來連接 DirectShow 篩選器的一些協助程式函式。
ms.assetid: cfd85944-7ae7-49e6-948f-9e190cdeed12
title: 連接兩個篩選器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7e70e607c510490e7ed841ea44303153a94e83f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109413"
---
# <a name="connect-two-filters"></a><span data-ttu-id="80a0d-103">連接兩個篩選器</span><span class="sxs-lookup"><span data-stu-id="80a0d-103">Connect Two Filters</span></span>

<span data-ttu-id="80a0d-104">本主題說明用來連接 DirectShow 篩選器的一些協助程式函式。</span><span class="sxs-lookup"><span data-stu-id="80a0d-104">This topic shows some helper functions for connecting DirectShow filters.</span></span>

<span data-ttu-id="80a0d-105">若要連接兩個篩選器，您必須在上游篩選器上找到未連接的輸出 pin，以及下游篩選器上未連接的輸入 pin。</span><span class="sxs-lookup"><span data-stu-id="80a0d-105">To connect two filters, you must find an unconnected output pin on the upstream filter, and an unconnected input pin on the downstream filter.</span></span>

<span data-ttu-id="80a0d-106">如果您已經有兩個釘選的指標，請呼叫 [**IGraphBuilder：： connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) 方法來連接它們。</span><span class="sxs-lookup"><span data-stu-id="80a0d-106">If you already have pointers to both pins, call the [**IGraphBuilder::Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) method to connect them.</span></span> <span data-ttu-id="80a0d-107">如果 pin 無法直接連接到彼此， **IGraphBuilder：： connect** 方法可能會插入其他篩選器，以完成連線。</span><span class="sxs-lookup"><span data-stu-id="80a0d-107">If the pins cannot connect directly to each other, the **IGraphBuilder::Connect** method might insert additional filters, to complete the connection.</span></span> <span data-ttu-id="80a0d-108">如需詳細資訊，請參閱 [智慧型 Connect](intelligent-connect.md)。</span><span class="sxs-lookup"><span data-stu-id="80a0d-108">For more information, see [Intelligent Connect](intelligent-connect.md).</span></span>

<span data-ttu-id="80a0d-109">如果您有指向篩選準則的指標，而不是釘選，您必須使用 [**IBaseFilter：： EnumPins**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-enumpins) 方法來尋找釘選。</span><span class="sxs-lookup"><span data-stu-id="80a0d-109">If you have a pointer to the filters but not the pins, you must use the [**IBaseFilter::EnumPins**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-enumpins) method to find the pins.</span></span> <span data-ttu-id="80a0d-110"> (參閱 [列舉釘](enumerating-pins.md)選。 ) 本主題中的 helper 函式會示範這項技巧。</span><span class="sxs-lookup"><span data-stu-id="80a0d-110">(See [Enumerating Pins](enumerating-pins.md).) The helper functions in this topic demonstrate this technique.</span></span>

### <a name="output-pin-to-filter"></a><span data-ttu-id="80a0d-111">輸出釘選至篩選</span><span class="sxs-lookup"><span data-stu-id="80a0d-111">Output Pin to Filter</span></span>

<span data-ttu-id="80a0d-112">下列函式會採用兩個參數：輸出圖釘的指標，以及篩選的指標。</span><span class="sxs-lookup"><span data-stu-id="80a0d-112">The following function takes two parameters: A pointer to an output pin, and a pointer to a filter.</span></span> <span data-ttu-id="80a0d-113">此函式會將輸出圖釘連接至篩選上的第一個可用輸入圖釘。</span><span class="sxs-lookup"><span data-stu-id="80a0d-113">The function connects the output pin to the first available input pin on the filter.</span></span>


```C++
// Connect output pin to filter.

HRESULT ConnectFilters(
    IGraphBuilder *pGraph, // Filter Graph Manager.
    IPin *pOut,            // Output pin on the upstream filter.
    IBaseFilter *pDest)    // Downstream filter.
{
    IPin *pIn = NULL;
        
    // Find an input pin on the downstream filter.
    HRESULT hr = FindUnconnectedPin(pDest, PINDIR_INPUT, &pIn);
    if (SUCCEEDED(hr))
    {
        // Try to connect them.
        hr = pGraph->Connect(pOut, pIn);
        pIn->Release();
    }
    return hr;
}
```



<span data-ttu-id="80a0d-114">此函式會執行下列工作：</span><span class="sxs-lookup"><span data-stu-id="80a0d-114">This function does the following:</span></span>

1.  <span data-ttu-id="80a0d-115">呼叫函 `FindUnconnectedPin` 式以取得未連接的輸入 pin。</span><span class="sxs-lookup"><span data-stu-id="80a0d-115">Calls the `FindUnconnectedPin` function to get an unconnected input pin.</span></span> <span data-ttu-id="80a0d-116">此函式會顯示在 [篩選器的 [尋找未](find-an-unconnected-pin-on-a-filter.md)連接的 Pin] 主題中。</span><span class="sxs-lookup"><span data-stu-id="80a0d-116">This function is shown in the topic [Find an Unconnected Pin on a Filter](find-an-unconnected-pin-on-a-filter.md).</span></span>
2.  <span data-ttu-id="80a0d-117">呼叫 [**IGraphBuilder：： connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) 來連接兩個圖釘。</span><span class="sxs-lookup"><span data-stu-id="80a0d-117">Calls [**IGraphBuilder::Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) to connect the two pins.</span></span>

### <a name="filter-to-input-pin"></a><span data-ttu-id="80a0d-118">篩選至輸入釘選</span><span class="sxs-lookup"><span data-stu-id="80a0d-118">Filter to Input Pin</span></span>

<span data-ttu-id="80a0d-119">下一個函式會接受篩選的指標和指向輸入圖釘的指標。</span><span class="sxs-lookup"><span data-stu-id="80a0d-119">The next function takes a pointer to a filter and a pointer to an input pin.</span></span> <span data-ttu-id="80a0d-120">它會將輸入釘選到篩選器上的第一個可用輸出圖釘。</span><span class="sxs-lookup"><span data-stu-id="80a0d-120">It connects the input pin to the first available output pin on the filter.</span></span>


```C++
// Connect filter to input pin.

HRESULT ConnectFilters(IGraphBuilder *pGraph, IBaseFilter *pSrc, IPin *pIn)
{
    IPin *pOut = NULL;
        
    // Find an output pin on the upstream filter.
    HRESULT hr = FindUnconnectedPin(pSrc, PINDIR_OUTPUT, &pOut);
    if (SUCCEEDED(hr))
    {
        // Try to connect them.
        hr = pGraph->Connect(pOut, pIn);
        pOut->Release();
    }
    return hr;
}
```



### <a name="filter-to-filter"></a><span data-ttu-id="80a0d-121">篩選篩選</span><span class="sxs-lookup"><span data-stu-id="80a0d-121">Filter to Filter</span></span>

<span data-ttu-id="80a0d-122">第三個函式會接受上游篩選的指標和下游篩選的指標，並嘗試連接這兩個篩選準則。</span><span class="sxs-lookup"><span data-stu-id="80a0d-122">The third function takes a pointer to an upstream filter and a pointer to a downstream filter, and tries to connect both filters.</span></span>


```C++
// Connect filter to filter

HRESULT ConnectFilters(IGraphBuilder *pGraph, IBaseFilter *pSrc, IBaseFilter *pDest)
{
    IPin *pOut = NULL;

    // Find an output pin on the first filter.
    HRESULT hr = FindUnconnectedPin(pSrc, PINDIR_OUTPUT, &pOut);
    if (SUCCEEDED(hr))
    {
        hr = ConnectFilters(pGraph, pOut, pDest);
        pOut->Release();
    }
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="80a0d-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="80a0d-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="80a0d-124">一般 Graph-Building 技術</span><span class="sxs-lookup"><span data-stu-id="80a0d-124">General Graph-Building Techniques</span></span>](general-graph-building-techniques.md)
</dt> <dt>

[<span data-ttu-id="80a0d-125">**ICaptureGraphBuilder2：： RenderStream**</span><span class="sxs-lookup"><span data-stu-id="80a0d-125">**ICaptureGraphBuilder2::RenderStream**</span></span>](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream)
</dt> </dl>

 

 



