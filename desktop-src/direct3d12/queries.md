---
title: 查詢
description: 在 Direct3D 12 中，查詢會分組為稱為查詢堆積的查詢陣列。 查詢堆積有一種類型，可定義可搭配該堆積使用的有效查詢類型。
ms.assetid: d7403b5d-7e1b-4dd2-ae45-52e1153233c6
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22c4db895eb0d4a727db2e32757f7ab0f1f9b1e2
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/12/2021
ms.locfileid: "104548435"
---
# <a name="queries"></a><span data-ttu-id="f5620-104">查詢</span><span class="sxs-lookup"><span data-stu-id="f5620-104">Queries</span></span>

<span data-ttu-id="f5620-105">在 Direct3D 12 中，查詢會分組為稱為查詢堆積的查詢陣列。</span><span class="sxs-lookup"><span data-stu-id="f5620-105">In Direct3D 12, queries are grouped into arrays of queries called a query heap.</span></span> <span data-ttu-id="f5620-106">查詢堆積有一種類型，可定義可搭配該堆積使用的有效查詢類型。</span><span class="sxs-lookup"><span data-stu-id="f5620-106">A query heap has a type which defines the valid types of queries that can be used with that heap.</span></span>

-   [<span data-ttu-id="f5620-107">從 Direct3D 11 至 Direct3D 12 的查詢差異</span><span class="sxs-lookup"><span data-stu-id="f5620-107">Differences in Queries from Direct3D 11 to Direct3D 12</span></span>](#differences-in-queries-from-direct3d-11-to-direct3d-12)
-   [<span data-ttu-id="f5620-108">查詢堆積</span><span class="sxs-lookup"><span data-stu-id="f5620-108">Query Heaps</span></span>](#query-heaps)
-   [<span data-ttu-id="f5620-109">建立查詢堆積</span><span class="sxs-lookup"><span data-stu-id="f5620-109">Creating Query heaps</span></span>](#creating-query-heaps)
-   [<span data-ttu-id="f5620-110">從查詢中解壓縮資料</span><span class="sxs-lookup"><span data-stu-id="f5620-110">Extracting data from a query</span></span>](#extracting-data-from-a-query)
-   [<span data-ttu-id="f5620-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="f5620-111">Related topics</span></span>](#related-topics)

## <a name="differences-in-queries-from-direct3d-11-to-direct3d-12"></a><span data-ttu-id="f5620-112">從 Direct3D 11 至 Direct3D 12 的查詢差異</span><span class="sxs-lookup"><span data-stu-id="f5620-112">Differences in Queries from Direct3D 11 to Direct3D 12</span></span>

<span data-ttu-id="f5620-113">下列查詢類型不再存在於 Direct3D 12 中，其功能會併入其他進程：</span><span class="sxs-lookup"><span data-stu-id="f5620-113">The following query types are no longer present in Direct3D 12, their functionality being incorporated into other processes:</span></span>

-   <span data-ttu-id="f5620-114">**事件查詢** -事件功能現在由圍牆處理。</span><span class="sxs-lookup"><span data-stu-id="f5620-114">**Event queries** - event functionally is now handled by fences.</span></span>
-   <span data-ttu-id="f5620-115">無 **交集的時間戳記查詢**-在 Direct3D 12 中，GPU 時鐘可以設定為穩定狀態 (請參閱) 的 [計時](timing.md)區段。</span><span class="sxs-lookup"><span data-stu-id="f5620-115">**Disjoint timestamp queries** - GPU clocks can be set to a stable state in Direct3D 12 (see the [Timing](timing.md) section).</span></span> <span data-ttu-id="f5620-116">如果 GPU 在 (時間戳記之間的閒置（稱為脫離的查詢) ）之間的，GPU 時鐘比較沒有意義。</span><span class="sxs-lookup"><span data-stu-id="f5620-116">GPU clock comparisons are not meaningful if the GPU idled at all between the timestamps (known as a disjoint query).</span></span> <span data-ttu-id="f5620-117">具有穩定的電源，從不同的命令清單發出的兩個時間戳記查詢可以可靠地進行比較。</span><span class="sxs-lookup"><span data-stu-id="f5620-117">With stable power two timestamp queries issued from different command lists are reliably comparable.</span></span> <span data-ttu-id="f5620-118">相同命令清單中的兩個時間戳記一律可以可靠地進行比較。</span><span class="sxs-lookup"><span data-stu-id="f5620-118">Two timestamps within the same command list are always reliably comparable.</span></span>
-   <span data-ttu-id="f5620-119">**串流輸出統計資料查詢** -在 Direct3D 12 中，沒有單一資料流程輸出 (因此) 溢位查詢用於所有輸出資料流程。</span><span class="sxs-lookup"><span data-stu-id="f5620-119">**Stream output statistics queries** - in Direct3D 12 there is no single stream output (SO) overflow query for all the output streams.</span></span> <span data-ttu-id="f5620-120">應用程式需要發出多個單一資料流程查詢，然後將結果相互關聯。</span><span class="sxs-lookup"><span data-stu-id="f5620-120">Apps need to issue multiple single-stream queries, and then correlate the results.</span></span>
-   <span data-ttu-id="f5620-121">**資料流程輸出統計資料述詞和遮蔽** 述詞查詢- (寫入記憶體) 和 [Predication](predication.md) 的查詢， (讀取記憶體) 不再結合，因此不需要這些查詢類型。</span><span class="sxs-lookup"><span data-stu-id="f5620-121">**Stream output statistics predicate and occlusion predicate queries** - queries (which write to memory) and [Predication](predication.md) (which reads from memory) are no longer coupled, and so these query types are not needed.</span></span>

<span data-ttu-id="f5620-122">已將新的二進位遮蔽查詢類型新增至 Direct3D 12。</span><span class="sxs-lookup"><span data-stu-id="f5620-122">A new binary occlusion query type has been added to Direct3D 12.</span></span> <span data-ttu-id="f5620-123">這可讓您只在意物件是否完全 pixels occluded 或不 (的 predication 策略，而不是 pixels occluded 的圖元數) 來指出此裝置的數量，這可能會更有效率地執行查詢。</span><span class="sxs-lookup"><span data-stu-id="f5620-123">This allows predication strategies that care only whether an object was fully occluded or not (rather than how many pixels were occluded) to indicate this to the device, which might be able to more efficiently perform the queries.</span></span>

## <a name="query-heaps"></a><span data-ttu-id="f5620-124">查詢堆積</span><span class="sxs-lookup"><span data-stu-id="f5620-124">Query Heaps</span></span>

<span data-ttu-id="f5620-125">查詢可以是數種類型的其中一種 ([**D3D12 \_ 查詢 \_ 堆積 \_ 類型**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_heap_type)) ，並在提交至 GPU 之前分組為查詢堆積。</span><span class="sxs-lookup"><span data-stu-id="f5620-125">Queries can be one from a number of types ([**D3D12\_QUERY\_HEAP\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_heap_type)), and are grouped into query heaps before being submitted to the GPU.</span></span>

<span data-ttu-id="f5620-126">您可以使用新的查詢類型 D3D12 \_ 查詢 \_ 類型 \_ BINARY \_ 遮蔽，其行為就像 D3D12 \_ 查詢 \_ 類型 \_ 遮蔽，但它會傳回二進位0/1 結果：0表示沒有樣本通過深度和樣板測試，1表示至少有一個樣本通過深度和樣板測試。</span><span class="sxs-lookup"><span data-stu-id="f5620-126">A new query type D3D12\_QUERY\_TYPE\_BINARY\_OCCLUSION is available and acts like D3D12\_QUERY\_TYPE\_OCCLUSION except that it returns a binary 0/1 result: 0 indicates that no samples passed depth and stencil testing, 1 indicates that at least one sample passed depth and stencil testing.</span></span> <span data-ttu-id="f5620-127">這可讓遮蔽查詢不會干擾與深度/樣板測試相關聯的任何 GPU 效能優化。</span><span class="sxs-lookup"><span data-stu-id="f5620-127">This enables occlusion queries to not interfere with any GPU performance optimization associated with depth/stencil testing.</span></span>

## <a name="creating-query-heaps"></a><span data-ttu-id="f5620-128">建立查詢堆積</span><span class="sxs-lookup"><span data-stu-id="f5620-128">Creating Query heaps</span></span>

<span data-ttu-id="f5620-129">與建立查詢堆積相關的 Api 是列舉 [**D3D12 \_ 查詢 \_ 堆積 \_ 類型**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_heap_type)、結構 [**D3D12 \_ 查詢 \_ 堆積 \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_query_heap_desc)和方法 [**CreateQueryHeap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createqueryheap)。</span><span class="sxs-lookup"><span data-stu-id="f5620-129">The APIs relevant to creating query heaps are the enum [**D3D12\_QUERY\_HEAP\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_heap_type), the struct [**D3D12\_QUERY\_HEAP\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_query_heap_desc), and the method [**CreateQueryHeap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createqueryheap).</span></span>

<span data-ttu-id="f5620-130">核心執行時間會驗證查詢堆積類型是否為 [**D3D12 \_ 堆積 \_ 型**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type) 別列舉的有效成員，以及計數是否大於0。</span><span class="sxs-lookup"><span data-stu-id="f5620-130">The core runtime will validate that the query heap type is a valid member of the [**D3D12\_HEAP\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type) enumeration, and that the count is greater than 0.</span></span>

<span data-ttu-id="f5620-131">查詢堆積內的每個個別查詢元素都可以個別啟動和停止。</span><span class="sxs-lookup"><span data-stu-id="f5620-131">Each individual query element within a query heap can be started and stopped separately.</span></span>

<span data-ttu-id="f5620-132">使用查詢堆積的 Api 是列舉 [**D3D12 \_ 查詢 \_ 類型**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_type)，以及 [**BeginQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery) 和 [**EndQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery)方法。</span><span class="sxs-lookup"><span data-stu-id="f5620-132">The APIs for using the query heaps are the enum [**D3D12\_QUERY\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_type), and the methods [**BeginQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery) and [**EndQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery).</span></span>

<span data-ttu-id="f5620-133">D3D12 \_ query \_ 類型 \_ TIMESTAMP 是唯一僅支援 [**EndQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery) 的查詢。</span><span class="sxs-lookup"><span data-stu-id="f5620-133">D3D12\_QUERY\_TYPE\_TIMESTAMP is the only query that supports [**EndQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery) only.</span></span> <span data-ttu-id="f5620-134">所有其他查詢類型都需要 [**BeginQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery) 和 **EndQuery**。</span><span class="sxs-lookup"><span data-stu-id="f5620-134">All other query types require [**BeginQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery) and **EndQuery**.</span></span>

<span data-ttu-id="f5620-135">Debug 層會驗證下列各項：</span><span class="sxs-lookup"><span data-stu-id="f5620-135">The debug layer will validate the following:</span></span>

-   <span data-ttu-id="f5620-136">開始時間戳查詢是不合法的， &mdash; 您只能將它結束</span><span class="sxs-lookup"><span data-stu-id="f5620-136">It is illegal to begin a timestamp query&mdash;you can only end it</span></span>
-   <span data-ttu-id="f5620-137">不合法地開始查詢兩次，而不需要結束指定元素) 的 (。</span><span class="sxs-lookup"><span data-stu-id="f5620-137">It is illegal to begin a query twice without ending it (for a given element).</span></span> <span data-ttu-id="f5620-138">對於需要 begin 和 end 的查詢，在指定專案) 的對應開始 (之前結束查詢是不合法的。</span><span class="sxs-lookup"><span data-stu-id="f5620-138">For queries that require both begin and end, it is illegal to end a query before the corresponding begin (for a given element).</span></span>
-   <span data-ttu-id="f5620-139">傳遞至 [**BeginQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery) 的查詢類型必須符合傳遞至 [**EndQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery)的查詢類型。</span><span class="sxs-lookup"><span data-stu-id="f5620-139">The query type passed to [**BeginQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery) must match the query type passed to [**EndQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery).</span></span>

<span data-ttu-id="f5620-140">核心執行時間會驗證下列各項：</span><span class="sxs-lookup"><span data-stu-id="f5620-140">The core runtime will validate the following:</span></span>

-   <span data-ttu-id="f5620-141">無法在時間戳記查詢上呼叫 [**BeginQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery) 。</span><span class="sxs-lookup"><span data-stu-id="f5620-141">[**BeginQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery) cannot be called on a timestamp query.</span></span>
-   <span data-ttu-id="f5620-142">針對支援 [**BeginQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery) 和 [**EndQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery) 的查詢類型 (除了 timestamp) 以外的所有專案，指定元素的查詢不得跨越命令清單界限。</span><span class="sxs-lookup"><span data-stu-id="f5620-142">For the query types which support both [**BeginQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery) and [**EndQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery) (all except for timestamp), a query for a given element must not span command list boundaries.</span></span>
-   <span data-ttu-id="f5620-143">*ElementIndex* 必須在範圍內。</span><span class="sxs-lookup"><span data-stu-id="f5620-143">*ElementIndex* must be within range.</span></span>
-   <span data-ttu-id="f5620-144">查詢類型是 [**D3D12 \_ 查詢 \_ 類型**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_type) 列舉的有效成員。</span><span class="sxs-lookup"><span data-stu-id="f5620-144">The query type is a valid member of the [**D3D12\_QUERY\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_type) enum.</span></span>
-   <span data-ttu-id="f5620-145">查詢類型必須與查詢堆積相容。</span><span class="sxs-lookup"><span data-stu-id="f5620-145">The query type must be compatible with the query heap.</span></span> <span data-ttu-id="f5620-146">下表顯示每個查詢類型所需的查詢堆積類型：</span><span class="sxs-lookup"><span data-stu-id="f5620-146">The following table shows the query heap type required for each query type:</span></span>

    

    | <span data-ttu-id="f5620-147">查詢類型</span><span class="sxs-lookup"><span data-stu-id="f5620-147">Query Type</span></span>                                  | <span data-ttu-id="f5620-148">查詢堆積類型</span><span class="sxs-lookup"><span data-stu-id="f5620-148">Query Heap type</span></span>                                |
    |---------------------------------------------|------------------------------------------------|
    | <span data-ttu-id="f5620-149">D3D12 \_ 查詢 \_ 類型 \_ 遮蔽</span><span class="sxs-lookup"><span data-stu-id="f5620-149">D3D12\_QUERY\_TYPE\_OCCLUSION</span></span>               | <span data-ttu-id="f5620-150">D3D12 \_ 查詢 \_ 堆積 \_ 類型 \_ 遮蔽</span><span class="sxs-lookup"><span data-stu-id="f5620-150">D3D12\_QUERY\_HEAP\_TYPE\_OCCLUSION</span></span>            |
    | <span data-ttu-id="f5620-151">D3D12 \_ 查詢 \_ 類型 \_ BINARY \_ 遮蔽</span><span class="sxs-lookup"><span data-stu-id="f5620-151">D3D12\_QUERY\_TYPE\_BINARY\_OCCLUSION</span></span>       | <span data-ttu-id="f5620-152">D3D12 \_ 查詢 \_ 堆積 \_ 類型 \_ 遮蔽</span><span class="sxs-lookup"><span data-stu-id="f5620-152">D3D12\_QUERY\_HEAP\_TYPE\_OCCLUSION</span></span>            |
    | <span data-ttu-id="f5620-153">D3D12 \_ 查詢 \_ 類型 \_ 時間戳記</span><span class="sxs-lookup"><span data-stu-id="f5620-153">D3D12\_QUERY\_TYPE\_TIMESTAMP</span></span>               | <span data-ttu-id="f5620-154">D3D12 \_ 查詢 \_ 堆積 \_ 類型 \_ 時間戳記</span><span class="sxs-lookup"><span data-stu-id="f5620-154">D3D12\_QUERY\_HEAP\_TYPE\_TIMESTAMP</span></span>            |
    | <span data-ttu-id="f5620-155">D3D12 \_ 查詢 \_ 類型 \_ 管線 \_ 統計資料</span><span class="sxs-lookup"><span data-stu-id="f5620-155">D3D12\_QUERY\_TYPE\_PIPELINE\_STATISTICS</span></span>    | <span data-ttu-id="f5620-156">D3D12 \_ 查詢 \_ 堆積 \_ 類型 \_ 管線 \_ 統計資料</span><span class="sxs-lookup"><span data-stu-id="f5620-156">D3D12\_QUERY\_HEAP\_TYPE\_PIPELINE\_STATISTICS</span></span> |
    | <span data-ttu-id="f5620-157">D3D12 \_ 查詢 \_ 類型 \_ ，使 \_ 統計資料 \_ STREAM0</span><span class="sxs-lookup"><span data-stu-id="f5620-157">D3D12\_QUERY\_TYPE\_SO\_STATISTICS\_STREAM0</span></span> | <span data-ttu-id="f5620-158">D3D12 \_ 查詢 \_ 堆積 \_ 類型 \_ 的 \_ 統計資料</span><span class="sxs-lookup"><span data-stu-id="f5620-158">D3D12\_QUERY\_HEAP\_TYPE\_SO\_STATISTICS</span></span>       |
    | <span data-ttu-id="f5620-159">D3D12 \_ 查詢 \_ 類型 \_ ，使 \_ 統計資料 \_ STREAM1</span><span class="sxs-lookup"><span data-stu-id="f5620-159">D3D12\_QUERY\_TYPE\_SO\_STATISTICS\_STREAM1</span></span> | <span data-ttu-id="f5620-160">D3D12 \_ 查詢 \_ 堆積 \_ 類型 \_ 的 \_ 統計資料</span><span class="sxs-lookup"><span data-stu-id="f5620-160">D3D12\_QUERY\_HEAP\_TYPE\_SO\_STATISTICS</span></span>       |
    | <span data-ttu-id="f5620-161">D3D12 \_ 查詢 \_ 類型 \_ ，使 \_ 統計資料 \_ STREAM2</span><span class="sxs-lookup"><span data-stu-id="f5620-161">D3D12\_QUERY\_TYPE\_SO\_STATISTICS\_STREAM2</span></span> | <span data-ttu-id="f5620-162">D3D12 \_ 查詢 \_ 堆積 \_ 類型 \_ 的 \_ 統計資料</span><span class="sxs-lookup"><span data-stu-id="f5620-162">D3D12\_QUERY\_HEAP\_TYPE\_SO\_STATISTICS</span></span>       |
    | <span data-ttu-id="f5620-163">D3D12 \_ 查詢 \_ 類型 \_ ，使 \_ 統計資料 \_ STREAM3</span><span class="sxs-lookup"><span data-stu-id="f5620-163">D3D12\_QUERY\_TYPE\_SO\_STATISTICS\_STREAM3</span></span> | <span data-ttu-id="f5620-164">D3D12 \_ 查詢 \_ 堆積 \_ 類型 \_ 的 \_ 統計資料</span><span class="sxs-lookup"><span data-stu-id="f5620-164">D3D12\_QUERY\_HEAP\_TYPE\_SO\_STATISTICS</span></span>       |

    

     

-   <span data-ttu-id="f5620-165">命令清單類型支援此查詢類型。</span><span class="sxs-lookup"><span data-stu-id="f5620-165">The query type is supported by the command list type.</span></span> <span data-ttu-id="f5620-166">下表顯示哪些命令清單類型支援的查詢。</span><span class="sxs-lookup"><span data-stu-id="f5620-166">The following table shows which queries are supported on which command list types.</span></span>

    

    | <span data-ttu-id="f5620-167">查詢類型</span><span class="sxs-lookup"><span data-stu-id="f5620-167">Query Type</span></span>                                  | <span data-ttu-id="f5620-168">支援的命令清單類型</span><span class="sxs-lookup"><span data-stu-id="f5620-168">Supported Command List Types</span></span>         |
    |---------------------------------------------|--------------------------------------|
    | <span data-ttu-id="f5620-169">D3D12 \_ 查詢 \_ 類型 \_ 遮蔽</span><span class="sxs-lookup"><span data-stu-id="f5620-169">D3D12\_QUERY\_TYPE\_OCCLUSION</span></span>               | <span data-ttu-id="f5620-170">直接</span><span class="sxs-lookup"><span data-stu-id="f5620-170">Direct</span></span>                               |
    | <span data-ttu-id="f5620-171">D3D12 \_ 查詢 \_ 類型 \_ BINARY \_ 遮蔽</span><span class="sxs-lookup"><span data-stu-id="f5620-171">D3D12\_QUERY\_TYPE\_BINARY\_OCCLUSION</span></span>       | <span data-ttu-id="f5620-172">直接</span><span class="sxs-lookup"><span data-stu-id="f5620-172">Direct</span></span>                               |
    | <span data-ttu-id="f5620-173">D3D12 \_ 查詢 \_ 類型 \_ 時間戳記</span><span class="sxs-lookup"><span data-stu-id="f5620-173">D3D12\_QUERY\_TYPE\_TIMESTAMP</span></span>               | <span data-ttu-id="f5620-174">直接、計算和選擇性複製</span><span class="sxs-lookup"><span data-stu-id="f5620-174">Direct, Compute, and optionally Copy</span></span> |
    | <span data-ttu-id="f5620-175">D3D12 \_ 查詢 \_ 類型 \_ 管線 \_ 統計資料</span><span class="sxs-lookup"><span data-stu-id="f5620-175">D3D12\_QUERY\_TYPE\_PIPELINE\_STATISTICS</span></span>    | <span data-ttu-id="f5620-176">直接</span><span class="sxs-lookup"><span data-stu-id="f5620-176">Direct</span></span>                               |
    | <span data-ttu-id="f5620-177">D3D12 \_ 查詢 \_ 類型 \_ ，使 \_ 統計資料 \_ STREAM0</span><span class="sxs-lookup"><span data-stu-id="f5620-177">D3D12\_QUERY\_TYPE\_SO\_STATISTICS\_STREAM0</span></span> | <span data-ttu-id="f5620-178">直接</span><span class="sxs-lookup"><span data-stu-id="f5620-178">Direct</span></span>                               |
    | <span data-ttu-id="f5620-179">D3D12 \_ 查詢 \_ 類型 \_ ，使 \_ 統計資料 \_ STREAM1</span><span class="sxs-lookup"><span data-stu-id="f5620-179">D3D12\_QUERY\_TYPE\_SO\_STATISTICS\_STREAM1</span></span> | <span data-ttu-id="f5620-180">直接</span><span class="sxs-lookup"><span data-stu-id="f5620-180">Direct</span></span>                               |
    | <span data-ttu-id="f5620-181">D3D12 \_ 查詢 \_ 類型 \_ ，使 \_ 統計資料 \_ STREAM2</span><span class="sxs-lookup"><span data-stu-id="f5620-181">D3D12\_QUERY\_TYPE\_SO\_STATISTICS\_STREAM2</span></span> | <span data-ttu-id="f5620-182">直接</span><span class="sxs-lookup"><span data-stu-id="f5620-182">Direct</span></span>                               |
    | <span data-ttu-id="f5620-183">D3D12 \_ 查詢 \_ 類型 \_ ，使 \_ 統計資料 \_ STREAM3</span><span class="sxs-lookup"><span data-stu-id="f5620-183">D3D12\_QUERY\_TYPE\_SO\_STATISTICS\_STREAM3</span></span> | <span data-ttu-id="f5620-184">直接</span><span class="sxs-lookup"><span data-stu-id="f5620-184">Direct</span></span>                               |

    

     

## <a name="extracting-data-from-a-query"></a><span data-ttu-id="f5620-185">從查詢中解壓縮資料</span><span class="sxs-lookup"><span data-stu-id="f5620-185">Extracting data from a query</span></span>

<span data-ttu-id="f5620-186">從查詢中取出資料的方法是使用 [**ResolveQueryData**](/windows/win32p/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvequerydata) 方法。</span><span class="sxs-lookup"><span data-stu-id="f5620-186">The way to extract data from a query is to use the [**ResolveQueryData**](/windows/win32p/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvequerydata) method.</span></span> <span data-ttu-id="f5620-187">**ResolveQueryData** 適用于所有記憶體類型 (是否為系統記憶體或裝置本機記憶體) ，但需要目的地資源 [**D3D12_RESOURCE_STATE_COPY_DEST**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states)。</span><span class="sxs-lookup"><span data-stu-id="f5620-187">**ResolveQueryData** works with all memory types (whether they are system memory or device local memory), but requires the destination resource to be in [**D3D12_RESOURCE_STATE_COPY_DEST**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states).</span></span> 

## <a name="related-topics"></a><span data-ttu-id="f5620-188">相關主題</span><span class="sxs-lookup"><span data-stu-id="f5620-188">Related topics</span></span>

* [<span data-ttu-id="f5620-189">計數器和查詢</span><span class="sxs-lookup"><span data-stu-id="f5620-189">Counters and Queries</span></span>](counters-and-queries.md)
* [<span data-ttu-id="f5620-190">Predication 查詢逐步解說</span><span class="sxs-lookup"><span data-stu-id="f5620-190">Predication queries walk-through</span></span>](predication-queries.md)
