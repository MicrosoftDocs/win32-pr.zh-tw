---
description: 篩選鏈
ms.assetid: c17b3b58-65ab-4e83-91f2-54a995f22ddf
title: 篩選鏈
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d46e374aca71b024773e4177d09e67c7ee6034ac
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846599"
---
# <a name="filter-chains"></a><span data-ttu-id="95fe7-103">篩選鏈</span><span class="sxs-lookup"><span data-stu-id="95fe7-103">Filter Chains</span></span>

<span data-ttu-id="95fe7-104">*篩選鏈* 是符合下列條件的一系列篩選準則：</span><span class="sxs-lookup"><span data-stu-id="95fe7-104">A *filter chain* is a sequence of filters that meets the following conditions:</span></span>

-   <span data-ttu-id="95fe7-105">鏈中的每個篩選器最多隻會有一個連接的輸入 pin 和一個連線的輸出 pin。</span><span class="sxs-lookup"><span data-stu-id="95fe7-105">Each filter in the chain has at most one connected input pin and one connected output pin.</span></span>
-   <span data-ttu-id="95fe7-106">您可以跨越鏈中的每個篩選器，而不需要在鏈外遍歷篩選。</span><span class="sxs-lookup"><span data-stu-id="95fe7-106">It is possible to traverse every filter in the chain without traversing filters outside the chain.</span></span>

<span data-ttu-id="95fe7-107">例如，在下圖中，篩選 A-B、C – D 和 F – G – H 是篩選鏈。</span><span class="sxs-lookup"><span data-stu-id="95fe7-107">For example, in the following diagram, filters A–B, C–D, and F–G–H are filter chains.</span></span> <span data-ttu-id="95fe7-108">F – G – H (F – G 和 G – H) 中的每個 subchain 也是篩選鏈。</span><span class="sxs-lookup"><span data-stu-id="95fe7-108">Each subchain in F–G–H (F–G and G–H) is also a filter chain.</span></span> <span data-ttu-id="95fe7-109">篩選鏈可以由單一篩選準則組成，因此篩選 A、B、C、D、F、G 和 H 也是不同的篩選鏈。</span><span class="sxs-lookup"><span data-stu-id="95fe7-109">A filter chain can consist of a single filter, so filters A, B, C, D, F, G, and H are also distinct filter chains.</span></span> <span data-ttu-id="95fe7-110">篩選 E 有兩個輸入連接，因此包含篩選 E 的任何篩選準則順序都不是篩選鏈。</span><span class="sxs-lookup"><span data-stu-id="95fe7-110">Filter E has two input connections, so any sequence of filters that includes filter E is not a filter chain.</span></span>

![篩選鏈 (範例 1) ](images/filter-chain1.png)

<span data-ttu-id="95fe7-112">[**IFilterChain**](/windows/desktop/api/Strmif/nn-strmif-ifilterchain)介面提供下列方法來控制篩選鏈：</span><span class="sxs-lookup"><span data-stu-id="95fe7-112">The [**IFilterChain**](/windows/desktop/api/Strmif/nn-strmif-ifilterchain) interface provides the following methods for controlling filter chains:</span></span>



|                                                               |                                 |
|---------------------------------------------------------------|---------------------------------|
| [<span data-ttu-id="95fe7-113">**IFilterChain::StartChain**</span><span class="sxs-lookup"><span data-stu-id="95fe7-113">**IFilterChain::StartChain**</span></span>](/windows/desktop/api/Strmif/nf-strmif-ifilterchain-startchain)   | <span data-ttu-id="95fe7-114">啟動鏈。</span><span class="sxs-lookup"><span data-stu-id="95fe7-114">Starts a chain.</span></span>                 |
| [<span data-ttu-id="95fe7-115">**IFilterChain::StopChain**</span><span class="sxs-lookup"><span data-stu-id="95fe7-115">**IFilterChain::StopChain**</span></span>](/windows/desktop/api/Strmif/nf-strmif-ifilterchain-stopchain)     | <span data-ttu-id="95fe7-116">停止鏈。</span><span class="sxs-lookup"><span data-stu-id="95fe7-116">Stops a chain.</span></span>                  |
| [<span data-ttu-id="95fe7-117">**IFilterChain：:P auseChain**</span><span class="sxs-lookup"><span data-stu-id="95fe7-117">**IFilterChain::PauseChain**</span></span>](/windows/desktop/api/Strmif/nf-strmif-ifilterchain-pausechain)   | <span data-ttu-id="95fe7-118">暫停鏈。</span><span class="sxs-lookup"><span data-stu-id="95fe7-118">Pauses a chain.</span></span>                 |
| [<span data-ttu-id="95fe7-119">**IFilterChain::RemoveChain**</span><span class="sxs-lookup"><span data-stu-id="95fe7-119">**IFilterChain::RemoveChain**</span></span>](/windows/desktop/api/Strmif/nf-strmif-ifilterchain-removechain) | <span data-ttu-id="95fe7-120">從圖形中移除鏈。</span><span class="sxs-lookup"><span data-stu-id="95fe7-120">Removes a chain from the graph.</span></span> |



 

<span data-ttu-id="95fe7-121">沒有任何特定的方法可以新增鏈。</span><span class="sxs-lookup"><span data-stu-id="95fe7-121">There is no specific method for adding a chain.</span></span> <span data-ttu-id="95fe7-122">若要加入鏈，請使用 [**IFilterGraph：： AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) 方法插入新的篩選準則。</span><span class="sxs-lookup"><span data-stu-id="95fe7-122">To add a chain, insert the new filters using the [**IFilterGraph::AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) method.</span></span> <span data-ttu-id="95fe7-123">然後藉由呼叫 [**IGraphBuilder：： connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect)、 [**IGraphBuilder：： Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render)或類似的方法來連接篩選。</span><span class="sxs-lookup"><span data-stu-id="95fe7-123">Then connect the filters by calling [**IGraphBuilder::Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect), [**IGraphBuilder::Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render), or similar methods.</span></span>

<span data-ttu-id="95fe7-124">當圖形正在執行時，篩選鏈可以在執行和停止之間切換。</span><span class="sxs-lookup"><span data-stu-id="95fe7-124">When the graph is running, a filter chain can switch between running and stopped.</span></span> <span data-ttu-id="95fe7-125">當圖形暫停時，它可以在暫停和停止之間切換。</span><span class="sxs-lookup"><span data-stu-id="95fe7-125">When the graph is paused, it can switch between paused and stopped.</span></span> <span data-ttu-id="95fe7-126">這些是唯一可以使用篩選鏈進行的狀態轉換。</span><span class="sxs-lookup"><span data-stu-id="95fe7-126">These are the only state transitions possible with filter chains.</span></span>

## <a name="filter-chain-guidelines"></a><span data-ttu-id="95fe7-127">篩選鏈指導方針</span><span class="sxs-lookup"><span data-stu-id="95fe7-127">Filter Chain Guidelines</span></span>

<span data-ttu-id="95fe7-128">當您使用 **IFilterChain** 方法時，請務必確定圖形中的篩選準則可以支援篩選連結作業。</span><span class="sxs-lookup"><span data-stu-id="95fe7-128">When you use **IFilterChain** methods, it is important to make sure that the filters in the graph can support filter chaining operations.</span></span> <span data-ttu-id="95fe7-129">否則，您可能會造成鎖死或圖形錯誤。</span><span class="sxs-lookup"><span data-stu-id="95fe7-129">Otherwise, you might cause deadlocks or graph errors.</span></span> <span data-ttu-id="95fe7-130">連線到鏈的篩選準則必須在鏈變更狀態之後正確運作。</span><span class="sxs-lookup"><span data-stu-id="95fe7-130">Filters connected to the chain must function correctly after the chain changes state.</span></span>

<span data-ttu-id="95fe7-131">使用 **IFilterChain** 的最佳方式是使用一組專為連結而設計的篩選。</span><span class="sxs-lookup"><span data-stu-id="95fe7-131">The best way to use **IFilterChain** is with a set of filters that you have designed specifically for chaining.</span></span> <span data-ttu-id="95fe7-132">使用下列指導方針，以確保您的篩選準則對篩選鏈作業是安全的。</span><span class="sxs-lookup"><span data-stu-id="95fe7-132">Use the following guidelines to ensure that your filters are safe for filter chain operations.</span></span> <span data-ttu-id="95fe7-133">這些點會參考下圖。</span><span class="sxs-lookup"><span data-stu-id="95fe7-133">These points refer to the following diagram.</span></span>

![篩選鏈 (範例 2) ](images/filter-chain2.png)

-   <span data-ttu-id="95fe7-135">在篩選鏈的狀態變更之前，所有在篩選鏈界限的資料處理呼叫都必須完成。</span><span class="sxs-lookup"><span data-stu-id="95fe7-135">Before the filter chain's state changes, all data processing calls at the boundary of the filter chain must be completed.</span></span> <span data-ttu-id="95fe7-136">此規則適用于 [**IMemInputPin：： Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive)、 [**IPin：： NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment)和 [**IPin：： EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream)方法。</span><span class="sxs-lookup"><span data-stu-id="95fe7-136">This rule applies to the methods [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive), [**IPin::NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment), and [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream).</span></span> <span data-ttu-id="95fe7-137">鏈中的篩選準則必須從鏈外部篩選器所提出的這些方法呼叫傳回。鏈外的篩選準則必須從鏈內的篩選準則所進行的呼叫傳回。</span><span class="sxs-lookup"><span data-stu-id="95fe7-137">Filters in the chain must return from calls to these methods made by filters outside the chain; and filters outside the chain must return from calls made by filters within the chain.</span></span>

<span data-ttu-id="95fe7-138">例如，在上圖中，篩選 B 必須從篩選 A 完成任何資料處理呼叫，而篩選 E 必須從篩選 D 完成任何呼叫。如果釘選公開 [**IPinFlowControl**](/windows/desktop/api/Strmif/nn-strmif-ipinflowcontrol) 和 [**IPinConnection**](/windows/desktop/api/Strmif/nn-strmif-ipinconnection) 介面，您可以藉由呼叫 [**IPinFlowControl：： Block**](/windows/desktop/api/Strmif/nf-strmif-ipinflowcontrol-block) 和 [**IGraphConfig：:P ushthroughdata**](/windows/desktop/api/Strmif/nf-strmif-igraphconfig-pushthroughdata) 方法（如 [動態重新連接](dynamic-reconnection.md)中所述），將資料推送到圖形。</span><span class="sxs-lookup"><span data-stu-id="95fe7-138">For example, in the previous diagram, filter B must complete any data processing calls from filter A, and filter E must finish any calls from filter D. If the pins expose the [**IPinFlowControl**](/windows/desktop/api/Strmif/nn-strmif-ipinflowcontrol) and [**IPinConnection**](/windows/desktop/api/Strmif/nn-strmif-ipinconnection) interfaces, you can push the data through the graph by calling the [**IPinFlowControl::Block**](/windows/desktop/api/Strmif/nf-strmif-ipinflowcontrol-block) and [**IGraphConfig::PushThroughData**](/windows/desktop/api/Strmif/nf-strmif-igraphconfig-pushthroughdata) methods, as described in [Dynamic Reconnection](dynamic-reconnection.md).</span></span> <span data-ttu-id="95fe7-139">篩選器可能也支援用來推送資料的私用方法。</span><span class="sxs-lookup"><span data-stu-id="95fe7-139">Filters might also support private methods for pushing the data.</span></span>

-   <span data-ttu-id="95fe7-140">上游篩選準則必須預期鏈的狀態才會變更。</span><span class="sxs-lookup"><span data-stu-id="95fe7-140">Upstream filters must expect the chain's state to change.</span></span> <span data-ttu-id="95fe7-141">例如，在上圖中，假設鏈已停止，但篩選 A 呼叫 **IMemInputPin：： Receive**。</span><span class="sxs-lookup"><span data-stu-id="95fe7-141">For example, in the previous diagram, suppose the chain is stopped but filter A calls **IMemInputPin::Receive**.</span></span> <span data-ttu-id="95fe7-142">呼叫失敗，而篩選 A 的回應是停止串流。</span><span class="sxs-lookup"><span data-stu-id="95fe7-142">The call fails and the response of filter A is to stop streaming.</span></span> <span data-ttu-id="95fe7-143">當應用程式重新開機鏈時，不會有任何作用，因為篩選 A 已不再串流資料。</span><span class="sxs-lookup"><span data-stu-id="95fe7-143">When the application restarts the chain, it has no effect because filter A is no longer streaming data.</span></span>
-   <span data-ttu-id="95fe7-144">下游篩選器也必須預期鏈的狀態才會變更。</span><span class="sxs-lookup"><span data-stu-id="95fe7-144">Downstream filters must also expect the chain's state to change.</span></span> <span data-ttu-id="95fe7-145">如果沒有，下游篩選器可能會在等候從未抵達的範例時封鎖。</span><span class="sxs-lookup"><span data-stu-id="95fe7-145">If not, the downstream filter might block while it waits for samples that never arrive.</span></span> <span data-ttu-id="95fe7-146">例如，多工器 (MUX) 篩選器通常需要其所有輸入插針的資料。</span><span class="sxs-lookup"><span data-stu-id="95fe7-146">For example, multiplexer (MUX) filters often require data from all of their input pins.</span></span> <span data-ttu-id="95fe7-147">停止某個輸入 pin 的資料流程程，可能會封鎖其他串流進行處理。</span><span class="sxs-lookup"><span data-stu-id="95fe7-147">Halting the flow of data from one input pin might block the other streams from processing.</span></span> <span data-ttu-id="95fe7-148">這可能會導致圖形鎖死。</span><span class="sxs-lookup"><span data-stu-id="95fe7-148">This can cause the graph to deadlock.</span></span>
-   <span data-ttu-id="95fe7-149">每個從鏈外的篩選連線到鏈內篩選器的連接，都應該有自己的配置器，而不是由其他連接所共用。</span><span class="sxs-lookup"><span data-stu-id="95fe7-149">Each pin connection from a filter outside the chain to a filter within the chain should have its own allocator, which is not shared by other connections.</span></span> <span data-ttu-id="95fe7-150">當鏈變更狀態或從圖形中移除時，配置器可能會已取消認可。</span><span class="sxs-lookup"><span data-stu-id="95fe7-150">When the chain changes state or is removed from the graph, the allocator might be decommitted.</span></span> <span data-ttu-id="95fe7-151">如果其他連接使用相同的配置器，則無法再處理範例。</span><span class="sxs-lookup"><span data-stu-id="95fe7-151">If other connections were using the same allocator, they can no longer process samples.</span></span>
-   <span data-ttu-id="95fe7-152">除非連接到鏈的篩選支援動態中斷連線，否則請勿移除鏈。</span><span class="sxs-lookup"><span data-stu-id="95fe7-152">Do not remove a chain unless the filters connected to the chain support dynamic disconnection.</span></span> <span data-ttu-id="95fe7-153">一般而言，連接的篩選準則會支援 **IPinConnection** 或 **IPinFlowControl** 介面，但可能會改為支援私用介面。</span><span class="sxs-lookup"><span data-stu-id="95fe7-153">Typically, the connected filters will support the **IPinConnection** or **IPinFlowControl** interface, but might support private interfaces instead.</span></span>

## <a name="related-topics"></a><span data-ttu-id="95fe7-154">相關主題</span><span class="sxs-lookup"><span data-stu-id="95fe7-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="95fe7-155">動態圖表建立</span><span class="sxs-lookup"><span data-stu-id="95fe7-155">Dynamic Graph Building</span></span>](dynamic-graph-building.md)
</dt> </dl>

 

 



