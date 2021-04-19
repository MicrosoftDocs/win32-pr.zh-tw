---
description: DirectShow 篩選器開發簡介
ms.assetid: d5162ea4-ef37-4993-a82c-782f03b08c64
title: DirectShow 篩選器開發簡介
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a42c5d2437b32f521b0efc39775f186267d3c99
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106971928"
---
# <a name="introduction-to-directshow-filter-development"></a><span data-ttu-id="28996-103">DirectShow 篩選器開發簡介</span><span class="sxs-lookup"><span data-stu-id="28996-103">Introduction to DirectShow Filter Development</span></span>

<span data-ttu-id="28996-104">本節提供有關開發自訂 DirectShow 篩選器之工作的簡短大綱。</span><span class="sxs-lookup"><span data-stu-id="28996-104">This section gives a brief outline of the tasks involved in developing a custom DirectShow filter.</span></span> <span data-ttu-id="28996-105">它也提供更詳細地討論這些工作的主題連結。</span><span class="sxs-lookup"><span data-stu-id="28996-105">It also provides links to topics that discuss these tasks in greater detail.</span></span> <span data-ttu-id="28996-106">閱讀本節之前，請閱讀 [有關 directshow](about-directshow.md)的主題，其中描述整體的 directshow 架構。</span><span class="sxs-lookup"><span data-stu-id="28996-106">Before reading this section, read the topics in [About DirectShow](about-directshow.md), which describe the overall DirectShow architecture.</span></span>

<span data-ttu-id="28996-107">**DirectShow 基礎類別庫**</span><span class="sxs-lookup"><span data-stu-id="28996-107">**DirectShow Base Class Library**</span></span>

<span data-ttu-id="28996-108">DirectShow SDK 包含一組用於撰寫篩選的 c + + 類別。</span><span class="sxs-lookup"><span data-stu-id="28996-108">The DirectShow SDK includes a set of C++ classes for writing filters.</span></span> <span data-ttu-id="28996-109">雖然它們並非必要，但建議您採用這些類別來撰寫新的篩選準則。</span><span class="sxs-lookup"><span data-stu-id="28996-109">Although they are not required, these classes are the recommended way to write a new filter.</span></span> <span data-ttu-id="28996-110">若要使用基類，請將它們編譯成靜態程式庫，並將 .lib 檔案連結至您的專案，如 [建立 DirectShow 篩選器](building-directshow-filters.md)中所述。</span><span class="sxs-lookup"><span data-stu-id="28996-110">To use the base classes, compile them into a static library and link the .lib file to your project, as described in [Building DirectShow Filters](building-directshow-filters.md).</span></span>

<span data-ttu-id="28996-111">基類庫會定義篩選的根類別，也就是 [**CBaseFilter**](cbasefilter.md) 類別。</span><span class="sxs-lookup"><span data-stu-id="28996-111">The base class library defines a root class for filters, the [**CBaseFilter**](cbasefilter.md) class.</span></span> <span data-ttu-id="28996-112">有幾個其他類別衍生自 **CBaseFilter**，而且專屬於特定種類的篩選準則。</span><span class="sxs-lookup"><span data-stu-id="28996-112">Several other classes derive from **CBaseFilter**, and are specialized for particular kinds of filters.</span></span> <span data-ttu-id="28996-113">例如， [**CTransformFilter**](ctransformfilter.md) 類別是針對轉換篩選所設計。</span><span class="sxs-lookup"><span data-stu-id="28996-113">For example, the [**CTransformFilter**](ctransformfilter.md) class is designed for transform filters.</span></span> <span data-ttu-id="28996-114">若要建立新的篩選，請執行繼承自其中一個篩選準則類別的類別。</span><span class="sxs-lookup"><span data-stu-id="28996-114">To create a new filter, implement a class that inherits from one of the filter classes.</span></span> <span data-ttu-id="28996-115">例如，您的類別宣告可能如下所示：</span><span class="sxs-lookup"><span data-stu-id="28996-115">For example, your class declaration might be as follows:</span></span>


```C++
class CMyFilter : public CTransformFilter
{
private:
    /* Declare variables and methods that are specific to your filter.
public:
    /* Override various methods in CTransformFilter */
};
```



<span data-ttu-id="28996-116">如需有關 DirectShow 基類的詳細資訊，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="28996-116">For more information about the DirectShow base classes, see the following topics:</span></span>

-   [<span data-ttu-id="28996-117">DirectShow 基類</span><span class="sxs-lookup"><span data-stu-id="28996-117">DirectShow Base Classes</span></span>](directshow-base-classes.md)
-   [<span data-ttu-id="28996-118">建立 DirectShow 篩選器</span><span class="sxs-lookup"><span data-stu-id="28996-118">Building DirectShow Filters</span></span>](building-directshow-filters.md)

<span data-ttu-id="28996-119">**建立釘選**</span><span class="sxs-lookup"><span data-stu-id="28996-119">**Creating Pins**</span></span>

<span data-ttu-id="28996-120">篩選準則必須建立一或多個 pin。</span><span class="sxs-lookup"><span data-stu-id="28996-120">A filter must create one or more pins.</span></span> <span data-ttu-id="28996-121">您可以在設計階段修正 pin 數目，或視需要建立新的釘選。</span><span class="sxs-lookup"><span data-stu-id="28996-121">The number of pins can be fixed at design time, or the filter can create new pins as needed.</span></span> <span data-ttu-id="28996-122">釘選通常衍生自 [**CBasePin**](cbasepin.md) 類別，或衍生自繼承 **CBasePin** 的類別，例如 [**CBaseInputPin**](cbaseinputpin.md)。</span><span class="sxs-lookup"><span data-stu-id="28996-122">Pins generally derive from the [**CBasePin**](cbasepin.md) class, or from a class that inherits **CBasePin**, such as [**CBaseInputPin**](cbaseinputpin.md).</span></span> <span data-ttu-id="28996-123">篩選器的 pin 應宣告為篩選準則類別中的成員變數。</span><span class="sxs-lookup"><span data-stu-id="28996-123">The filter's pins should be declared as member variables in the filter class.</span></span> <span data-ttu-id="28996-124">某些篩選準則類別已定義釘選，但如果您的篩選準則直接繼承自 **CBaseFilter**，您就必須在衍生類別中宣告釘選。</span><span class="sxs-lookup"><span data-stu-id="28996-124">Some of the filter classes already define the pins, but if your filter inherits directly from **CBaseFilter**, you must declare the pins in your derived class.</span></span>

<span data-ttu-id="28996-125">**協商 Pin 連接**</span><span class="sxs-lookup"><span data-stu-id="28996-125">**Negotiating Pin Connections**</span></span>

<span data-ttu-id="28996-126">當篩選圖形管理員嘗試連接兩個篩選器時，pin 必須同意各種不同的專案。</span><span class="sxs-lookup"><span data-stu-id="28996-126">When the Filter Graph Manager tries to connect two filters, the pins must agree on various things.</span></span> <span data-ttu-id="28996-127">如果無法連線，連接嘗試就會失敗。</span><span class="sxs-lookup"><span data-stu-id="28996-127">If they cannot, the connection attempt fails.</span></span> <span data-ttu-id="28996-128">一般而言，pin 會協商下列各項：</span><span class="sxs-lookup"><span data-stu-id="28996-128">Generally, pins negotiate the following:</span></span>

-   <span data-ttu-id="28996-129">傳輸。</span><span class="sxs-lookup"><span data-stu-id="28996-129">Transport.</span></span> <span data-ttu-id="28996-130">傳輸是篩選器將用來將媒體樣本從輸出圖釘移至輸入釘選的機制。</span><span class="sxs-lookup"><span data-stu-id="28996-130">The transport is the mechanism that the filters will use to move media samples from the output pin to the input pin.</span></span> <span data-ttu-id="28996-131">例如，他們可以使用 [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) 介面 ( 「推送模型」 ) 或 [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) 介面 ( 「提取模型」 ) 。</span><span class="sxs-lookup"><span data-stu-id="28996-131">For example, they can use the [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) interface ("push model") or the [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) interface ("pull model").</span></span>
-   <span data-ttu-id="28996-132">媒體類型。</span><span class="sxs-lookup"><span data-stu-id="28996-132">Media type.</span></span> <span data-ttu-id="28996-133">幾乎所有的針腳都會使用媒體類型來描述所要傳遞的資料格式。</span><span class="sxs-lookup"><span data-stu-id="28996-133">Almost all pins use media types to describe the format of the data they will deliver.</span></span>
-   <span data-ttu-id="28996-134">分配器。</span><span class="sxs-lookup"><span data-stu-id="28996-134">Allocator.</span></span> <span data-ttu-id="28996-135">配置器是建立保存資料之緩衝區的物件。</span><span class="sxs-lookup"><span data-stu-id="28996-135">The allocator is the object that creates the buffers that hold the data.</span></span> <span data-ttu-id="28996-136">Pin 必須同意哪些 pin 將提供配置器。</span><span class="sxs-lookup"><span data-stu-id="28996-136">The pins must agree which pin will provide the allocator.</span></span> <span data-ttu-id="28996-137">它們也必須同意緩衝區大小、要建立的緩衝區數目，以及其他緩衝區屬性。</span><span class="sxs-lookup"><span data-stu-id="28996-137">They must also agree on the size of the buffers, the number of buffers to create, and other buffer properties.</span></span>

<span data-ttu-id="28996-138">基類會針對這些協商執行架構。</span><span class="sxs-lookup"><span data-stu-id="28996-138">The base classes implement a framework for these negotiations.</span></span> <span data-ttu-id="28996-139">您必須覆寫基類中的各種方法，以完成詳細資料。</span><span class="sxs-lookup"><span data-stu-id="28996-139">You must complete the details by overriding various methods in the base class.</span></span> <span data-ttu-id="28996-140">您必須覆寫的方法集合取決於類別以及篩選的功能。</span><span class="sxs-lookup"><span data-stu-id="28996-140">The set of methods that you must override depends on the class and on the functionality of your filter.</span></span> <span data-ttu-id="28996-141">如需詳細資訊，請參閱 [篩選準則的連接方式](how-filters-connect.md)。</span><span class="sxs-lookup"><span data-stu-id="28996-141">For more information, see [How Filters Connect](how-filters-connect.md).</span></span>

<span data-ttu-id="28996-142">**處理和傳遞資料**</span><span class="sxs-lookup"><span data-stu-id="28996-142">**Processing and Delivering Data**</span></span>

<span data-ttu-id="28996-143">大部分篩選準則的主要功能是處理和傳遞媒體資料。</span><span class="sxs-lookup"><span data-stu-id="28996-143">The primary function of most filters is to process and deliver media data.</span></span> <span data-ttu-id="28996-144">這種情況取決於篩選器的類型：</span><span class="sxs-lookup"><span data-stu-id="28996-144">How that occurs depends on the type of filter:</span></span>

-   <span data-ttu-id="28996-145">推送來源有一個背景工作執行緒，會持續以資料填滿範例，並將其傳遞至下游。</span><span class="sxs-lookup"><span data-stu-id="28996-145">A push source has a worker thread that continuously fills samples with data and delivers them downstream.</span></span>
-   <span data-ttu-id="28996-146">提取來源會等待其下游鄰近要求範例。</span><span class="sxs-lookup"><span data-stu-id="28996-146">A pull source waits for its downstream neighbor to request a sample.</span></span> <span data-ttu-id="28996-147">它會藉由將資料寫入範例，並將範例傳遞給下游篩選器來進行回應。</span><span class="sxs-lookup"><span data-stu-id="28996-147">It responds by writing data into a sample and delivering the sample to the downstream filter.</span></span> <span data-ttu-id="28996-148">下游篩選器會建立驅動資料流程的執行緒。</span><span class="sxs-lookup"><span data-stu-id="28996-148">The downstream filter creates the thread that drives the data flow.</span></span>
-   <span data-ttu-id="28996-149">轉換篩選具有其上游節點傳遞給它的範例。</span><span class="sxs-lookup"><span data-stu-id="28996-149">A transform filter has samples delivered to it by its upstream neighbor.</span></span> <span data-ttu-id="28996-150">當它收到範例時，它會處理資料並將它傳遞給下游。</span><span class="sxs-lookup"><span data-stu-id="28996-150">When it receives a sample, it processes the data and delivers it downstream.</span></span>
-   <span data-ttu-id="28996-151">轉譯器篩選器會從上游接收樣本，然後根據時間戳記進行排程以進行轉譯。</span><span class="sxs-lookup"><span data-stu-id="28996-151">A renderer filter receives samples from upstream, and schedules them for rendering based on the time stamps.</span></span>

<span data-ttu-id="28996-152">與串流相關的其他工作包括從圖形清除資料、處理資料流程的結尾，以及回應搜尋要求。</span><span class="sxs-lookup"><span data-stu-id="28996-152">Other tasks related to streaming include flushing data from the graph, handling the end of the stream, and responding to seek requests.</span></span> <span data-ttu-id="28996-153">如需有關這些問題的詳細資訊，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="28996-153">For more information about these issues, see the following topics:</span></span>

-   [<span data-ttu-id="28996-154">篩選開發人員的資料流程</span><span class="sxs-lookup"><span data-stu-id="28996-154">Data Flow for Filter Developers</span></span>](data-flow-for-filter-developers.md)
-   [<span data-ttu-id="28996-155">品質控制管理</span><span class="sxs-lookup"><span data-stu-id="28996-155">Quality-Control Management</span></span>](quality-control-management.md)
-   [<span data-ttu-id="28996-156">執行緒和重要區段</span><span class="sxs-lookup"><span data-stu-id="28996-156">Threads and Critical Sections</span></span>](threads-and-critical-sections.md)

<span data-ttu-id="28996-157">**支援 COM**</span><span class="sxs-lookup"><span data-stu-id="28996-157">**Supporting COM**</span></span>

<span data-ttu-id="28996-158">DirectShow 篩選器是 COM 物件，通常封裝在 Dll 中。</span><span class="sxs-lookup"><span data-stu-id="28996-158">DirectShow filters are COM objects, typically packaged in DLLs.</span></span> <span data-ttu-id="28996-159">基類程式庫會實作為支援 COM 的架構。</span><span class="sxs-lookup"><span data-stu-id="28996-159">The base class library implements a framework for supporting COM.</span></span> <span data-ttu-id="28996-160">它會在「DirectShow」 [和「COM](directshow-and-com.md)」一節中說明。</span><span class="sxs-lookup"><span data-stu-id="28996-160">It is described in the section [DirectShow and COM](directshow-and-com.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="28996-161">相關主題</span><span class="sxs-lookup"><span data-stu-id="28996-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="28996-162">撰寫 DirectShow 篩選器</span><span class="sxs-lookup"><span data-stu-id="28996-162">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



