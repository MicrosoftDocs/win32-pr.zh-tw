---
description: 設定圖形時鐘
ms.assetid: 23deab26-6c9a-4f94-b750-11c9b1a14ce3
title: 設定圖形時鐘
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfe98c8dce1ab5f94664fbe1406c682e5d4e50b8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106970675"
---
# <a name="setting-the-graph-clock"></a><span data-ttu-id="16de3-103">設定圖形時鐘</span><span class="sxs-lookup"><span data-stu-id="16de3-103">Setting the Graph Clock</span></span>

<span data-ttu-id="16de3-104">當您建立篩選圖形時，篩選圖形管理員會自動為圖形選擇參考時鐘。</span><span class="sxs-lookup"><span data-stu-id="16de3-104">When you build a filter graph, the Filter Graph Manager automatically chooses a reference clock for the graph.</span></span> <span data-ttu-id="16de3-105">圖形中的所有篩選都會同步處理到參考時鐘。</span><span class="sxs-lookup"><span data-stu-id="16de3-105">All filters in the graph are synchronized to the reference clock.</span></span> <span data-ttu-id="16de3-106">尤其是，轉譯器篩選器會使用參考時鐘來判斷每個樣本的呈現時間。</span><span class="sxs-lookup"><span data-stu-id="16de3-106">In particular, renderer filters use the reference clock to determine the presentation time of each sample.</span></span>

<span data-ttu-id="16de3-107">應用程式通常不會有理由覆寫篩選圖形管理員選擇的參考時鐘。</span><span class="sxs-lookup"><span data-stu-id="16de3-107">There is usually no reason for an application to override the Filter Graph Manager's choice of reference clock.</span></span> <span data-ttu-id="16de3-108">不過，您可以在篩選圖形管理員上呼叫 [**IMediaFilter：： SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) 方法來這麼做。</span><span class="sxs-lookup"><span data-stu-id="16de3-108">However, you can do so by calling the [**IMediaFilter::SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) method on the Filter Graph Manager.</span></span> <span data-ttu-id="16de3-109">這個方法會採用時鐘 **IReferenceClock** 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="16de3-109">This method takes a pointer to the clock's **IReferenceClock** interface.</span></span> <span data-ttu-id="16de3-110">當圖形停止時，呼叫方法。</span><span class="sxs-lookup"><span data-stu-id="16de3-110">Call the method while the graph is stopped.</span></span>

<span data-ttu-id="16de3-111">如果篩選準則提供時鐘，您可以藉由呼叫篩選準則的 **QueryInterface** 來取得 **IReferenceClock** 指標。</span><span class="sxs-lookup"><span data-stu-id="16de3-111">If a filter provides a clock, you can get the **IReferenceClock** pointer by calling **QueryInterface** on the filter.</span></span> <span data-ttu-id="16de3-112">或者，只要您的外部時鐘實 **IReferenceClock**，您就可以執行篩選不提供的外部參考時鐘。</span><span class="sxs-lookup"><span data-stu-id="16de3-112">Alternatively, you can implement an external reference clock that is not provided by a filter, as long as your external clock implements **IReferenceClock**.</span></span> <span data-ttu-id="16de3-113">下列範例顯示如何指定時鐘：</span><span class="sxs-lookup"><span data-stu-id="16de3-113">The following example shows how to specify a clock:</span></span>


```C++
IGraphBuilder *pGraph = 0;
IReferenceClock *pClock = 0;

CoCreateInstance(CLSID_FilterGraph, NULL, CLSCTX_INPROC_SERVER, 
    IID_IGraphBuilder, (void **)&pGraph);

// Build the graph.
pGraph->RenderFile(L"C:\\Example.avi", 0);

// Create your clock.
hr = CreateMyPrivateClock(&pClock);
if (SUCCEEDED(hr))
{
    // Set the graph clock.
    IMediaFilter *pMediaFilter = 0;
    pGraph->QueryInterface(IID_IMediaFilter, (void**)&pMediaFilter);
    pMediaFilter->SetSyncSource(pClock);
    pClock->Release();
    pMediaFilter->Release();
}
```



<span data-ttu-id="16de3-114">此範例假設 CreateMyPrivateClock 是應用程式定義的函式，它會建立時鐘並傳回 **IReferenceClock** 指標。</span><span class="sxs-lookup"><span data-stu-id="16de3-114">This example assumes that CreateMyPrivateClock is an application-defined function that creates a clock and returns an **IReferenceClock** pointer.</span></span>

<span data-ttu-id="16de3-115">您也可以使用 **Null** 值呼叫 **SetSyncSource** ，將篩選圖形設定為不使用時鐘執行。</span><span class="sxs-lookup"><span data-stu-id="16de3-115">You can also set the filter graph to run with no clock, by calling **SetSyncSource** with the value **NULL**.</span></span> <span data-ttu-id="16de3-116">如果沒有時鐘，圖形會儘快執行。</span><span class="sxs-lookup"><span data-stu-id="16de3-116">If there is no clock, the graph runs as quickly as possible.</span></span> <span data-ttu-id="16de3-117">如果沒有時鐘，轉譯器篩選不會等候樣本的呈現時間。</span><span class="sxs-lookup"><span data-stu-id="16de3-117">With no clock, renderer filters do not wait for a sample's presentation time.</span></span> <span data-ttu-id="16de3-118">相反地，它們會在每個範例抵達時立即轉譯。</span><span class="sxs-lookup"><span data-stu-id="16de3-118">Instead, they render each sample as soon as it arrives.</span></span> <span data-ttu-id="16de3-119">如果您想要快速地處理資料，而不是即時預覽，則將圖形設定為在沒有時鐘的情況下執行會很有用。</span><span class="sxs-lookup"><span data-stu-id="16de3-119">Setting the graph to run without a clock is useful if you want to process data quickly, rather than previewing it in real time.</span></span>

## <a name="related-topics"></a><span data-ttu-id="16de3-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="16de3-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="16de3-121">基本的 DirectShow 工作</span><span class="sxs-lookup"><span data-stu-id="16de3-121">Basic DirectShow Tasks</span></span>](basic-directshow-tasks.md)
</dt> <dt>

[<span data-ttu-id="16de3-122">**CBaseReferenceClock 類別**</span><span class="sxs-lookup"><span data-stu-id="16de3-122">**CBaseReferenceClock Class**</span></span>](cbasereferenceclock.md)
</dt> <dt>

[<span data-ttu-id="16de3-123">DirectShow 中的時間和時鐘</span><span class="sxs-lookup"><span data-stu-id="16de3-123">Time and Clocks in DirectShow</span></span>](time-and-clocks-in-directshow.md)
</dt> </dl>

 

 



