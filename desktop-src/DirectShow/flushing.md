---
description: 沖洗
ms.assetid: 868218c4-3e1a-4da0-89fa-30a9848da0e8
title: 沖洗
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 575f311020c2c7a567e544b80ba323a29051cc38
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104510261"
---
# <a name="flushing"></a><span data-ttu-id="53b55-103">沖洗</span><span class="sxs-lookup"><span data-stu-id="53b55-103">Flushing</span></span>

<span data-ttu-id="53b55-104">當篩選圖形正在執行時，任意數量的資料都可以透過圖形來移動。</span><span class="sxs-lookup"><span data-stu-id="53b55-104">While the filter graph is running, arbitrary amounts of data can be moving through the graph.</span></span> <span data-ttu-id="53b55-105">其中有些可能會在佇列中等候傳遞。</span><span class="sxs-lookup"><span data-stu-id="53b55-105">Some of it might be in queues, waiting to be delivered.</span></span> <span data-ttu-id="53b55-106">有時候，篩選圖形需要儘快移除此暫止的資料，並將它取代為新的資料。</span><span class="sxs-lookup"><span data-stu-id="53b55-106">There are times when the filter graph needs to remove this pending data as quickly as possible and replace it with new data.</span></span> <span data-ttu-id="53b55-107">例如，在搜尋命令之後，來源篩選會從來源中的新位置產生樣本。</span><span class="sxs-lookup"><span data-stu-id="53b55-107">After a seek command, for example, the source filter generates samples from a new position in the source.</span></span> <span data-ttu-id="53b55-108">為了將延遲降到最低，下游篩選應捨棄在 seek 命令之前建立的任何範例。</span><span class="sxs-lookup"><span data-stu-id="53b55-108">To minimize latency, downstream filters should discard any samples that were created before the seek command.</span></span> <span data-ttu-id="53b55-109">捨棄範例的進程稱為排清 *。*</span><span class="sxs-lookup"><span data-stu-id="53b55-109">The process of discarding samples is called *flushing*.</span></span> <span data-ttu-id="53b55-110">當事件改變一般的資料流程時，可讓圖形更具回應性。</span><span class="sxs-lookup"><span data-stu-id="53b55-110">It enables the graph to be more responsive when events alter the normal data flow.</span></span>

<span data-ttu-id="53b55-111">提取模型會以稍微不同于推送模型的方式來處理排清。</span><span class="sxs-lookup"><span data-stu-id="53b55-111">Flushing is handled slightly differently by the pull model than the push model.</span></span> <span data-ttu-id="53b55-112">本文一開始會描述推送模型;然後，它會描述提取模型中的差異。</span><span class="sxs-lookup"><span data-stu-id="53b55-112">This article starts by describing the push model; then it describes the differences in the pull model.</span></span>

<span data-ttu-id="53b55-113">清除會以兩個階段進行。</span><span class="sxs-lookup"><span data-stu-id="53b55-113">Flushing happens in two stages.</span></span>

-   <span data-ttu-id="53b55-114">首先，來源篩選準則會在下游篩選器的輸入 pin 上呼叫 [**IPin：： BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) 。</span><span class="sxs-lookup"><span data-stu-id="53b55-114">First, the source filter calls [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) on the downstream filter's input pin.</span></span> <span data-ttu-id="53b55-115">下游篩選器會開始拒絕上游的範例。</span><span class="sxs-lookup"><span data-stu-id="53b55-115">The downstream filter starts rejecting samples from upstream.</span></span> <span data-ttu-id="53b55-116">它也會捨棄所持有的任何範例，並將下游的 **BeginFlush** 呼叫傳送至下一個篩選準則。</span><span class="sxs-lookup"><span data-stu-id="53b55-116">It also discards any samples it is holding, and sends the **BeginFlush** call downstream to the next filter.</span></span>
-   <span data-ttu-id="53b55-117">當來源篩選器準備好要傳送新的資料時，它會在輸入 pin 上呼叫 [**IPin：： EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) 。</span><span class="sxs-lookup"><span data-stu-id="53b55-117">When the source filter is ready to send new data, it calls [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) on the input pin.</span></span> <span data-ttu-id="53b55-118">這會對下游篩選器發出可接收新範例的信號。</span><span class="sxs-lookup"><span data-stu-id="53b55-118">This signals the downstream filter that it can receive new samples.</span></span> <span data-ttu-id="53b55-119">下游篩選器會將 **EndFlush** 呼叫傳送至下一個篩選準則。</span><span class="sxs-lookup"><span data-stu-id="53b55-119">The downstream filter sends the **EndFlush** call to the next filter.</span></span>

<span data-ttu-id="53b55-120">在 **BeginFlush** 方法中，輸入 pin 會執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="53b55-120">In the **BeginFlush** method, the input pin does the following:</span></span>

1.  <span data-ttu-id="53b55-121">在下游輸入 pin 上呼叫 **BeginFlush** 。</span><span class="sxs-lookup"><span data-stu-id="53b55-121">Calls **BeginFlush** on downstream input pins.</span></span>
2.  <span data-ttu-id="53b55-122">拒絕任何其他串流資料的呼叫，包括 **接收** 和 **EndOfStream**。</span><span class="sxs-lookup"><span data-stu-id="53b55-122">Rejects any further calls that stream data, including **Receive** and **EndOfStream**.</span></span>
3.  <span data-ttu-id="53b55-123">從篩選器配置器解除封鎖等候範例的任何上游篩選。</span><span class="sxs-lookup"><span data-stu-id="53b55-123">Unblocks any upstream filters that are blocked waiting for a sample from the filter's allocator.</span></span> <span data-ttu-id="53b55-124">某些篩選準則會取消認可其配置器的用途。</span><span class="sxs-lookup"><span data-stu-id="53b55-124">Some filters decommit their allocators for this purpose.</span></span>
4.  <span data-ttu-id="53b55-125">離開任何區塊串流的等候。</span><span class="sxs-lookup"><span data-stu-id="53b55-125">Exits from any waits that block streaming.</span></span> <span data-ttu-id="53b55-126">例如，轉譯器篩選會在暫停時封鎖。</span><span class="sxs-lookup"><span data-stu-id="53b55-126">For example, renderer filters block when paused.</span></span> <span data-ttu-id="53b55-127">它們也會在等候于正確資料流程時間轉譯樣本時封鎖。</span><span class="sxs-lookup"><span data-stu-id="53b55-127">They also block when they are waiting to render a sample at the correct stream time.</span></span> <span data-ttu-id="53b55-128">篩選準則必須解除封鎖，才能傳遞和拒絕佇列上游的範例。</span><span class="sxs-lookup"><span data-stu-id="53b55-128">The filter must unblock, so that samples queued upstream can be delivered and rejected.</span></span> <span data-ttu-id="53b55-129">此步驟可確保所有上游篩選器最後都會解除封鎖。</span><span class="sxs-lookup"><span data-stu-id="53b55-129">This step ensures that all upstream filters eventually unblock.</span></span>

<span data-ttu-id="53b55-130">在 **EndFlush** 方法中，輸入 pin 會執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="53b55-130">In the **EndFlush** method, the input pin does the following:</span></span>

1.  <span data-ttu-id="53b55-131">等候所有已排入佇列的樣本被捨棄。</span><span class="sxs-lookup"><span data-stu-id="53b55-131">Waits for all queued samples to be discarded.</span></span>
2.  <span data-ttu-id="53b55-132">釋放任何緩衝的資料。</span><span class="sxs-lookup"><span data-stu-id="53b55-132">Frees any buffered data.</span></span> <span data-ttu-id="53b55-133">此步驟有時可以在 **BeginFlush** 方法中執行。</span><span class="sxs-lookup"><span data-stu-id="53b55-133">This step can sometimes be performed in the **BeginFlush** method.</span></span> <span data-ttu-id="53b55-134">但是， **BeginFlush** 不會與資料流程處理執行緒同步處理。</span><span class="sxs-lookup"><span data-stu-id="53b55-134">However, **BeginFlush** is not synchronized with the streaming thread.</span></span> <span data-ttu-id="53b55-135">篩選準則不能在呼叫 **BeginFlush** 和 **EndFlush** 呼叫之間處理或緩衝任何其他資料。</span><span class="sxs-lookup"><span data-stu-id="53b55-135">The filter must not process or buffer any more data between the call to **BeginFlush** and the call to **EndFlush**.</span></span>
3.  <span data-ttu-id="53b55-136">清除任何暫止 \_ 的 EC 完成通知。</span><span class="sxs-lookup"><span data-stu-id="53b55-136">Clears any pending EC\_COMPLETE notifications.</span></span>
4.  <span data-ttu-id="53b55-137">呼叫 **EndFlush** 下游。</span><span class="sxs-lookup"><span data-stu-id="53b55-137">Calls **EndFlush** downstream.</span></span>

<span data-ttu-id="53b55-138">此時，篩選可以再次接受範例。</span><span class="sxs-lookup"><span data-stu-id="53b55-138">At this point, the filter can accept samples again.</span></span> <span data-ttu-id="53b55-139">所有範例保證會比排清更新。</span><span class="sxs-lookup"><span data-stu-id="53b55-139">All samples are guaranteed to be more recent than the flush.</span></span>

<span data-ttu-id="53b55-140">在提取模型中，剖析器篩選器會起始清除，而不是來源篩選。</span><span class="sxs-lookup"><span data-stu-id="53b55-140">In the pull model, the parser filter initiates flushing, rather than the source filter.</span></span> <span data-ttu-id="53b55-141">它不只會在下游篩選器上呼叫 **IPin：： BeginFlush** 和 **IPin：： EndFlush** ，也會在來源篩選的 *輸出* 釘選上呼叫 [**IAsyncReader：： BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-beginflush)和 [**IAsyncReader：： EndFlush**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-endflush) 。</span><span class="sxs-lookup"><span data-stu-id="53b55-141">Not only does it call **IPin::BeginFlush** and **IPin::EndFlush** on the downstream filter, it also calls [**IAsyncReader::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-beginflush) and [**IAsyncReader::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-endflush) on the *output* pin of the source filter.</span></span> <span data-ttu-id="53b55-142">如果來源篩選具有暫止的讀取要求，則會捨棄這些要求。</span><span class="sxs-lookup"><span data-stu-id="53b55-142">If the source filter has pending read requests, it will discard them.</span></span>

## <a name="related-topics"></a><span data-ttu-id="53b55-143">相關主題</span><span class="sxs-lookup"><span data-stu-id="53b55-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="53b55-144">清除資料</span><span class="sxs-lookup"><span data-stu-id="53b55-144">Flushing Data</span></span>](flushing-data.md)
</dt> </dl>

 

 



