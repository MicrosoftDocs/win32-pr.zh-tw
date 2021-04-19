---
description: 關於媒體範例和配置器
ms.assetid: d6283bf0-0460-4519-9a56-fd4c78cfaabc
title: 關於媒體範例和配置器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9105228e70f82aaa7c36b7e7d28cf7e748e1e2f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106991946"
---
# <a name="about-media-samples-and-allocators"></a><span data-ttu-id="ca086-103">關於媒體範例和配置器</span><span class="sxs-lookup"><span data-stu-id="ca086-103">About Media Samples and Allocators</span></span>

<span data-ttu-id="ca086-104">篩選會跨 pin 連接傳遞資料。</span><span class="sxs-lookup"><span data-stu-id="ca086-104">Filters deliver data across pin connections.</span></span> <span data-ttu-id="ca086-105">資料會從一個篩選的輸出圖釘移至另一個篩選的輸入圖釘。</span><span class="sxs-lookup"><span data-stu-id="ca086-105">Data moves from the output pin of one filter to the input pin of another filter.</span></span> <span data-ttu-id="ca086-106">輸出圖釘傳遞資料的最常見方式，是在輸入上呼叫 [**IMemInputPin：： Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) 方法，雖然另外還有一些其他機制也存在。</span><span class="sxs-lookup"><span data-stu-id="ca086-106">The most common way for the output pin to deliver the data is by calling the [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) method on the input, although a few other mechanisms exist as well.</span></span>

<span data-ttu-id="ca086-107">根據篩選準則，媒體資料的記憶體可以不同的方式配置：在堆積上、DirectDraw 介面、使用共用的 GDI 記憶體，或使用其他的配置機制。</span><span class="sxs-lookup"><span data-stu-id="ca086-107">Depending on the filter, memory for the media data can be allocated in various ways: on the heap, in a DirectDraw surface, using shared GDI memory, or using some other allocation mechanism.</span></span> <span data-ttu-id="ca086-108">負責配置記憶體的物件稱為配置 *器，它* 是公開 [**IMEMALLOCATOR**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) 介面的 COM 物件。</span><span class="sxs-lookup"><span data-stu-id="ca086-108">The object responsible for allocating the memory is called an *allocator*, which is a COM object that exposes the [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span>

<span data-ttu-id="ca086-109">當兩個 pin 連接時，其中一個 pin 必須提供配置器。</span><span class="sxs-lookup"><span data-stu-id="ca086-109">When two pins connect, one of the pins must provide an allocator.</span></span> <span data-ttu-id="ca086-110">DirectShow 定義了一系列的方法呼叫，用來建立配置器所提供的 pin。</span><span class="sxs-lookup"><span data-stu-id="ca086-110">DirectShow defines a sequence of method calls that is used to establish which pin provides the allocator.</span></span> <span data-ttu-id="ca086-111">釘選也會同意配置器將建立的緩衝區數目，以及緩衝區的大小。</span><span class="sxs-lookup"><span data-stu-id="ca086-111">The pins also agree on the number of buffers that the allocator will create, and the size of the buffers.</span></span>

<span data-ttu-id="ca086-112">開始串流之前，配置器會建立緩衝區集區。</span><span class="sxs-lookup"><span data-stu-id="ca086-112">Before streaming begins, the allocator creates a pool of buffers.</span></span> <span data-ttu-id="ca086-113">在串流處理期間，上游篩選器會將資料填入緩衝區，並將其傳遞至下游篩選器。</span><span class="sxs-lookup"><span data-stu-id="ca086-113">During streaming, the upstream filter fills buffers with data and delivers them to the downstream filter.</span></span> <span data-ttu-id="ca086-114">但上游篩選不會將下游篩選器的原始指標提供給緩衝區。</span><span class="sxs-lookup"><span data-stu-id="ca086-114">But the upstream filter does not give the downstream filter raw pointers to the buffers.</span></span> <span data-ttu-id="ca086-115">相反地，它會使用稱為「 *媒體範例*」的 COM 物件，而配置器會建立這些物件來管理緩衝區。</span><span class="sxs-lookup"><span data-stu-id="ca086-115">Instead, it uses COM objects called *media samples*, which the allocator creates to manage the buffers.</span></span> <span data-ttu-id="ca086-116">媒體範例會公開 [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) 介面。</span><span class="sxs-lookup"><span data-stu-id="ca086-116">Media samples expose the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span> <span data-ttu-id="ca086-117">媒體範例包含：</span><span class="sxs-lookup"><span data-stu-id="ca086-117">A media sample contains:</span></span>

-   <span data-ttu-id="ca086-118">基礎緩衝區的指標</span><span class="sxs-lookup"><span data-stu-id="ca086-118">a pointer to the underlying buffer</span></span>
-   <span data-ttu-id="ca086-119">時間戳記</span><span class="sxs-lookup"><span data-stu-id="ca086-119">a time stamp</span></span>
-   <span data-ttu-id="ca086-120">各種旗標</span><span class="sxs-lookup"><span data-stu-id="ca086-120">various flags</span></span>
-   <span data-ttu-id="ca086-121">（選擇性）媒體類型</span><span class="sxs-lookup"><span data-stu-id="ca086-121">optionally, a media type</span></span>

<span data-ttu-id="ca086-122">時間戳記會定義轉譯器篩選器用來排程轉譯的呈現時間。</span><span class="sxs-lookup"><span data-stu-id="ca086-122">The time stamp defines the presentation time, which the renderer filter uses to schedule rendering.</span></span> <span data-ttu-id="ca086-123">旗標指出自上一個範例之後，資料中是否有中斷的情況。</span><span class="sxs-lookup"><span data-stu-id="ca086-123">The flags indicate things like whether there was a break in the data since the previous sample.</span></span> <span data-ttu-id="ca086-124">媒體類型提供一種方式，讓篩選器變更中間資料流程的格式。</span><span class="sxs-lookup"><span data-stu-id="ca086-124">The media type provides a way for filters to change formats mid-stream.</span></span> <span data-ttu-id="ca086-125">通常，此範例不會有媒體類型，這表示格式自上一個範例之後未變更。</span><span class="sxs-lookup"><span data-stu-id="ca086-125">Usually, the sample has no media type, which indicates that the format has not changed since the previous sample.</span></span>

<span data-ttu-id="ca086-126">當篩選使用緩衝區時，它會保存範例上的參考計數。</span><span class="sxs-lookup"><span data-stu-id="ca086-126">While a filter is using a buffer, it holds reference count on the sample.</span></span> <span data-ttu-id="ca086-127">配置器會使用參考計數來決定何時可以重複使用緩衝區。</span><span class="sxs-lookup"><span data-stu-id="ca086-127">The allocator uses the reference count to determine when it can re-use the buffer.</span></span> <span data-ttu-id="ca086-128">這可防止篩選覆寫另一個篩選仍在使用中的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="ca086-128">This prevents a filter from overwriting a buffer that another filter is still using.</span></span> <span data-ttu-id="ca086-129">在每個篩選器發行之前，範例都不會回到配置器的可用樣本集區。</span><span class="sxs-lookup"><span data-stu-id="ca086-129">A sample does not return to the allocator's pool of available samples until every filter has released it.</span></span>

<span data-ttu-id="ca086-130">如需詳細資訊，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="ca086-130">For more information, see the following topics:</span></span>

-   <span data-ttu-id="ca086-131">主題 [範例和配置器](samples-and-allocators.md) 提供配置器運作方式的詳細描述。</span><span class="sxs-lookup"><span data-stu-id="ca086-131">The topic [Samples and Allocators](samples-and-allocators.md) provides a more detailed description of how allocators work.</span></span>
-   <span data-ttu-id="ca086-132">[篩選圖形中](data-flow-in-the-filter-graph.md)的主題資料流程提供有關 DirectShow 中資料流程的一般總覽。</span><span class="sxs-lookup"><span data-stu-id="ca086-132">The topic [Data Flow in the Filter Graph](data-flow-in-the-filter-graph.md) gives a general overview of data flow in DirectShow.</span></span>

<span data-ttu-id="ca086-133">下列主題適用于撰寫自己的自訂篩選器的開發人員：</span><span class="sxs-lookup"><span data-stu-id="ca086-133">The following topics are intended for developers who are writing their own custom filters:</span></span>

-   [<span data-ttu-id="ca086-134">篩選開發人員的資料流程</span><span class="sxs-lookup"><span data-stu-id="ca086-134">Data Flow for Filter Developers</span></span>](data-flow-for-filter-developers.md)
-   [<span data-ttu-id="ca086-135">執行緒和重要區段</span><span class="sxs-lookup"><span data-stu-id="ca086-135">Threads and Critical Sections</span></span>](threads-and-critical-sections.md)

## <a name="related-topics"></a><span data-ttu-id="ca086-136">相關主題</span><span class="sxs-lookup"><span data-stu-id="ca086-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ca086-137">篩選圖形及其元件</span><span class="sxs-lookup"><span data-stu-id="ca086-137">The Filter Graph and Its Components</span></span>](the-filter-graph-and-its-components.md)
</dt> </dl>

 

 



