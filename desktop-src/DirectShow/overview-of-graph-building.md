---
description: 圖表建立的總覽
ms.assetid: 5753f06c-ecfd-48d7-a8e9-768b798e9279
title: 圖表建立的總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f69ef9ea0f4f9e21d33372ad2a37a59b512d5dcc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109077"
---
# <a name="overview-of-graph-building"></a><span data-ttu-id="e72a9-103">圖表建立的總覽</span><span class="sxs-lookup"><span data-stu-id="e72a9-103">Overview of Graph Building</span></span>

<span data-ttu-id="e72a9-104">若要建立篩選圖形，請先建立篩選圖形管理員的實例：</span><span class="sxs-lookup"><span data-stu-id="e72a9-104">To create a filter graph, begin by creating an instance of the Filter Graph Manager:</span></span>


```C++
IGraphBuilder* pIGB;
HRESULT hr = CoCreateInstance(CLSID_FilterGraph,
    NULL, CLSCTX_INPROC_SERVER, IID_IGraphBuilder,
    (void **)&pIGB);
```



<span data-ttu-id="e72a9-105">篩選圖形管理員支援下列圖表建立方法：</span><span class="sxs-lookup"><span data-stu-id="e72a9-105">The Filter Graph Manager supports the following graph-building methods:</span></span>

-   <span data-ttu-id="e72a9-106">[**IFilterGraph：： ConnectDirect**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-connectdirect) 會嘗試在兩個 pin 之間進行直接連接。</span><span class="sxs-lookup"><span data-stu-id="e72a9-106">[**IFilterGraph::ConnectDirect**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-connectdirect) tries to make a direct connection between two pins.</span></span> <span data-ttu-id="e72a9-107">如果 pin 無法連接，則方法會失敗。</span><span class="sxs-lookup"><span data-stu-id="e72a9-107">If the pins cannot connect, the method fails.</span></span>
-   <span data-ttu-id="e72a9-108">[**IGraphBuilder：： Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) 連接兩個圖釘。</span><span class="sxs-lookup"><span data-stu-id="e72a9-108">[**IGraphBuilder::Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) connects two pins.</span></span> <span data-ttu-id="e72a9-109">可能的話，它會直接連接。</span><span class="sxs-lookup"><span data-stu-id="e72a9-109">If possible, it makes a direct connection.</span></span> <span data-ttu-id="e72a9-110">否則，它會使用中繼篩選來完成連接。</span><span class="sxs-lookup"><span data-stu-id="e72a9-110">Otherwise, it uses intermediate filters to complete the connection.</span></span>
-   <span data-ttu-id="e72a9-111">[**IGraphBuilder：： Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) 會從輸出圖釘開始，並建立圖形的其餘部分。</span><span class="sxs-lookup"><span data-stu-id="e72a9-111">[**IGraphBuilder::Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) starts from an output pin and builds the rest of the graph.</span></span> <span data-ttu-id="e72a9-112">此方法會視需要新增篩選準則，直到到達轉譯器篩選器為止。</span><span class="sxs-lookup"><span data-stu-id="e72a9-112">This methods adds filters as needed, working downstream, until it reaches a renderer filter.</span></span>
-   <span data-ttu-id="e72a9-113">[**IGraphBuilder：： RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) 會建立完整的檔案播放圖形。</span><span class="sxs-lookup"><span data-stu-id="e72a9-113">[**IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) builds a complete file-playback graph.</span></span>
-   <span data-ttu-id="e72a9-114">[**IFilterGraph：： AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) 將篩選新增至圖形。</span><span class="sxs-lookup"><span data-stu-id="e72a9-114">[**IFilterGraph::AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) adds a filter to the graph.</span></span> <span data-ttu-id="e72a9-115">它不會連接篩選。</span><span class="sxs-lookup"><span data-stu-id="e72a9-115">It does not connect the filter.</span></span> <span data-ttu-id="e72a9-116">您必須藉由呼叫 **CoCreateInstance** 或使用篩選器對應程式或系統裝置列舉值，在呼叫這個方法之前建立篩選。</span><span class="sxs-lookup"><span data-stu-id="e72a9-116">You must create the filter before calling this method, either by calling **CoCreateInstance** or by using the Filter Mapper or System Device Enumerator.</span></span>

<span data-ttu-id="e72a9-117">這些方法提供三種基本的方法來建立圖形：</span><span class="sxs-lookup"><span data-stu-id="e72a9-117">These methods provide three basic approaches to building the graph:</span></span>

1.  <span data-ttu-id="e72a9-118">篩選圖形管理員會建立整個圖形。</span><span class="sxs-lookup"><span data-stu-id="e72a9-118">The Filter Graph Manager builds the entire graph.</span></span>
2.  <span data-ttu-id="e72a9-119">篩選圖形管理員會建立圖形的一部分。</span><span class="sxs-lookup"><span data-stu-id="e72a9-119">The Filter Graph Manager builds part of the graph.</span></span>
3.  <span data-ttu-id="e72a9-120">應用程式會建立整個圖形。</span><span class="sxs-lookup"><span data-stu-id="e72a9-120">The application builds the entire graph.</span></span>

<span data-ttu-id="e72a9-121">**篩選圖形管理員會建立整個圖形**</span><span class="sxs-lookup"><span data-stu-id="e72a9-121">**The Filter Graph Manager Builds the Entire Graph**</span></span>

<span data-ttu-id="e72a9-122">如果您只想要播放以可辨識格式（例如 AVI、MPEG、WAV 或 MP3）撰寫的檔案，請使用 **RenderFile** 方法。</span><span class="sxs-lookup"><span data-stu-id="e72a9-122">If you simply want to play a file that is authored in a recognized format, such as AVI, MPEG, WAV, or MP3, use the **RenderFile** method.</span></span> <span data-ttu-id="e72a9-123">如何 [播放](how-to-play-a-file.md) 檔案的文章會說明如何進行。</span><span class="sxs-lookup"><span data-stu-id="e72a9-123">The article [How To Play a File](how-to-play-a-file.md) shows how to do this.</span></span>

<span data-ttu-id="e72a9-124">**RenderFile** 方法一開始會在登錄中查看可剖析檔案的來源篩選。</span><span class="sxs-lookup"><span data-stu-id="e72a9-124">The **RenderFile** method starts by looking in the registry for a source filter that can parse the file.</span></span> <span data-ttu-id="e72a9-125">它會使用通訊協定 (例如 URL) 中的 " `https://` "、副檔名，或檔案中預先定義的位元組模式，以決定來源篩選。</span><span class="sxs-lookup"><span data-stu-id="e72a9-125">It uses the protocol (such as " `https://` " in the URL), the file extension, or pre-defined byte patterns in the file to determine the source filter.</span></span> <span data-ttu-id="e72a9-126">如需詳細資訊，請參閱 [註冊自訂檔案類型](registering-a-custom-file-type.md)。</span><span class="sxs-lookup"><span data-stu-id="e72a9-126">For details, see [Registering a Custom File Type](registering-a-custom-file-type.md).</span></span>

<span data-ttu-id="e72a9-127">若要建立圖形的其餘部分，篩選圖形管理員會使用反復的程式，其中會採用篩選器在其輸出圖釘上支援的媒體類型，並搜尋登錄中是否接受該媒體類型作為輸入的篩選器。</span><span class="sxs-lookup"><span data-stu-id="e72a9-127">To build the rest of the graph, the Filter Graph Manager uses an iterative process wherein it takes the media types that a filter supports on its output pins, and searches the registry for filters that will accept that media type as input.</span></span> <span data-ttu-id="e72a9-128">它會使用數個準則來縮小搜尋範圍並設定篩選優先順序：</span><span class="sxs-lookup"><span data-stu-id="e72a9-128">It uses several criteria to narrow the search and prioritize filters:</span></span>

-   <span data-ttu-id="e72a9-129">*篩選準則類別* 識別篩選準則的一般功能。</span><span class="sxs-lookup"><span data-stu-id="e72a9-129">The *filter category* identifies the general functionality of the filter.</span></span>
-   <span data-ttu-id="e72a9-130">媒體類型描述篩選可接受做為輸入或作為輸出傳遞的資料類型。</span><span class="sxs-lookup"><span data-stu-id="e72a9-130">The media type describes what kind of data the filter can accept as input or deliver as output.</span></span>
-   <span data-ttu-id="e72a9-131">這些 *業績* 決定了篩選準則的嘗試順序。</span><span class="sxs-lookup"><span data-stu-id="e72a9-131">The *merit* determines the order in which filters are tried.</span></span> <span data-ttu-id="e72a9-132">如果相同篩選準則類別中的兩個篩選準則都支援相同的輸入類型，則篩選圖形管理員會選取具有最高品質值的篩選。</span><span class="sxs-lookup"><span data-stu-id="e72a9-132">If two filters in the same filter category both support the same input types, the Filter Graph Manager selects the one with the highest merit value.</span></span> <span data-ttu-id="e72a9-133">某些篩選器會刻意獲得較低的價值，因為它們是針對特定用途而設計，而且只應由應用程式新增至圖形。</span><span class="sxs-lookup"><span data-stu-id="e72a9-133">Some filters are purposely given a low merit value because they are designed for specialized purposes and should only be added to the graph by the application.</span></span>

<span data-ttu-id="e72a9-134">篩選圖形管理員會使用 [篩選器](filter-mapper.md) 對應程式物件來搜尋登錄。</span><span class="sxs-lookup"><span data-stu-id="e72a9-134">The Filter Graph Manager uses the [Filter Mapper](filter-mapper.md) object to search the registry.</span></span>

<span data-ttu-id="e72a9-135">新增每個篩選器時，篩選圖形管理員會嘗試將它連接到先前篩選的輸出圖釘。</span><span class="sxs-lookup"><span data-stu-id="e72a9-135">As each filter is added, the Filter Graph Manager tries to connect it to the previous filter's output pin.</span></span> <span data-ttu-id="e72a9-136">篩選準則會進行協調以判斷它們是否可以連接，如果是，要使用哪種媒體類型來連接。</span><span class="sxs-lookup"><span data-stu-id="e72a9-136">The filters negotiate to determine whether they can connect, and if so, what media type to use for the connection.</span></span> <span data-ttu-id="e72a9-137">如果新的篩選無法連接，則篩選圖形管理員會捨棄它，並嘗試另一個篩選準則。</span><span class="sxs-lookup"><span data-stu-id="e72a9-137">If the new filter cannot connect, the Filter Graph Manager discards it and tries another filter.</span></span> <span data-ttu-id="e72a9-138">此程式會繼續進行，直到轉譯每個資料流程為止。</span><span class="sxs-lookup"><span data-stu-id="e72a9-138">This process continues until every stream is rendered.</span></span>

<span data-ttu-id="e72a9-139">**篩選圖形管理員會建立圖形的一部分**</span><span class="sxs-lookup"><span data-stu-id="e72a9-139">**The Filter Graph Manager Builds Part of the Graph**</span></span>

<span data-ttu-id="e72a9-140">若要執行不只是播放檔案的動作，您的應用程式至少必須執行部分圖形建築工作。</span><span class="sxs-lookup"><span data-stu-id="e72a9-140">To do something beyond simply playing a file, your application must perform at least some of the graph building work.</span></span> <span data-ttu-id="e72a9-141">例如，影片捕獲應用程式必須選取捕獲來源篩選器，並將它新增至圖形。</span><span class="sxs-lookup"><span data-stu-id="e72a9-141">For example, a video capture application must select a capture source filter and add it to the graph.</span></span> <span data-ttu-id="e72a9-142">如果您要將資料寫入至 AVI 檔案，您必須將 AVI Mux 和檔案寫入器篩選器新增至圖形。</span><span class="sxs-lookup"><span data-stu-id="e72a9-142">If you are writing data to an AVI file, you must add the AVI Mux and File Writer filters to the graph.</span></span> <span data-ttu-id="e72a9-143">不過，通常可以讓篩選圖形管理員完成圖形。</span><span class="sxs-lookup"><span data-stu-id="e72a9-143">However, it is often possible to let the Filter Graph Manager complete the graph.</span></span> <span data-ttu-id="e72a9-144">例如，您可以藉由呼叫 **render** 方法來呈現預覽的 pin。</span><span class="sxs-lookup"><span data-stu-id="e72a9-144">For example, you can render a pin for preview by calling the **Render** method.</span></span>

<span data-ttu-id="e72a9-145">**應用程式會建立整個圖形**</span><span class="sxs-lookup"><span data-stu-id="e72a9-145">**The Application Builds the Entire Graph**</span></span>

<span data-ttu-id="e72a9-146">在某些情況下，您的應用程式可能需要加入並連接每個篩選器來建立圖形。</span><span class="sxs-lookup"><span data-stu-id="e72a9-146">In some scenarios, your application may need to build the graph by adding and connecting each filter.</span></span> <span data-ttu-id="e72a9-147">在此情況下，您可能會特別知道哪些篩選準則應該新增至圖形。</span><span class="sxs-lookup"><span data-stu-id="e72a9-147">In this case, you probably know specifically which filters should be added to the graph.</span></span> <span data-ttu-id="e72a9-148">使用這個方法時，應用程式會藉由呼叫 **AddFilter** 來新增每個篩選，列舉篩選上的釘選，然後藉由呼叫 **Connect** 或 **ConnectDirect** 來連接它們。</span><span class="sxs-lookup"><span data-stu-id="e72a9-148">With this approach, the application adds each filter by calling **AddFilter**, enumerates the pins on the filters, and connects them by calling either **Connect** or **ConnectDirect**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e72a9-149">相關主題</span><span class="sxs-lookup"><span data-stu-id="e72a9-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e72a9-150">使用 Capture Graph Builder 建立圖形</span><span class="sxs-lookup"><span data-stu-id="e72a9-150">Building Graphs with the Capture Graph Builder</span></span>](building-graphs-with-the-capture-graph-builder.md)
</dt> <dt>

[<span data-ttu-id="e72a9-151">列舉裝置和篩選器</span><span class="sxs-lookup"><span data-stu-id="e72a9-151">Enumerating Devices and Filters</span></span>](enumerating-devices-and-filters.md)
</dt> <dt>

[<span data-ttu-id="e72a9-152">列舉篩選圖形中的物件</span><span class="sxs-lookup"><span data-stu-id="e72a9-152">Enumerating Objects in a Filter Graph</span></span>](enumerating-objects-in-a-filter-graph.md)
</dt> <dt>

[<span data-ttu-id="e72a9-153">一般 Graph-Building 技術</span><span class="sxs-lookup"><span data-stu-id="e72a9-153">General Graph-Building Techniques</span></span>](general-graph-building-techniques.md)
</dt> <dt>

[<span data-ttu-id="e72a9-154">建立篩選圖形</span><span class="sxs-lookup"><span data-stu-id="e72a9-154">Building the Filter Graph</span></span>](building-the-filter-graph.md)
</dt> </dl>

 

 



