---
description: 概述 Windows 7 的索引優先順序和資料列集事件的簡介。
ms.assetid: 6cdfb7d3-f849-432c-960f-912e5024c583
title: 在 Windows 7 中編制優先順序和資料列集事件的索引
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6610500a3c2fcd359f346e5239507fb15ad896d
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "106999958"
---
# <a name="indexing-prioritization-and-rowset-events-in-windows-7"></a><span data-ttu-id="f8f7d-103">在 Windows 7 中編制優先順序和資料列集事件的索引</span><span class="sxs-lookup"><span data-stu-id="f8f7d-103">Indexing Prioritization and Rowset Events in Windows 7</span></span>

<span data-ttu-id="f8f7d-104">本主題概述 Windows 7 的索引優先順序和資料列集事件的簡介。</span><span class="sxs-lookup"><span data-stu-id="f8f7d-104">This topic outlines the introduction of indexing prioritization and rowset events for Windows 7.</span></span>

<span data-ttu-id="f8f7d-105">本主題的組織方式如下：</span><span class="sxs-lookup"><span data-stu-id="f8f7d-105">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="f8f7d-106">編制優先順序和資料列集事件的索引</span><span class="sxs-lookup"><span data-stu-id="f8f7d-106">Indexing Prioritization and Rowset Events</span></span>](#indexing-prioritization-and-rowset-events)
    -   [<span data-ttu-id="f8f7d-107">IRowsetPriorization 範例</span><span class="sxs-lookup"><span data-stu-id="f8f7d-107">IRowsetPriorization Examples</span></span>](#irowsetpriorization-examples)
    -   [<span data-ttu-id="f8f7d-108">IRowsetPrioritization 事件</span><span class="sxs-lookup"><span data-stu-id="f8f7d-108">IRowsetPrioritization Events</span></span>](#indexing-prioritization-and-rowset-events-in-windows-7)
-   [<span data-ttu-id="f8f7d-109">其他資源</span><span class="sxs-lookup"><span data-stu-id="f8f7d-109">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="f8f7d-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="f8f7d-110">Related topics</span></span>](#related-topics)

## <a name="indexing-prioritization-and-rowset-events"></a><span data-ttu-id="f8f7d-111">編制優先順序和資料列集事件的索引</span><span class="sxs-lookup"><span data-stu-id="f8f7d-111">Indexing Prioritization and Rowset Events</span></span>

<span data-ttu-id="f8f7d-112">在 Windows 7？和更新版本中，有一個優先順序堆疊，在此堆疊中，用戶端可以要求在該查詢中使用的範圍優先于一般專案的上方。</span><span class="sxs-lookup"><span data-stu-id="f8f7d-112">In Windows 7?and later, there is a priority stack within which the context of any particular query, the client can request that the scopes used in that query be prioritized above that of normal items.</span></span>

<span data-ttu-id="f8f7d-113">此優先順序堆疊具有下列特性：</span><span class="sxs-lookup"><span data-stu-id="f8f7d-113">This prioritization stack has the following characteristics:</span></span>

-   <span data-ttu-id="f8f7d-114">堆疊中的專案可以有前景、高或低優先順序：</span><span class="sxs-lookup"><span data-stu-id="f8f7d-114">Items in the stack can have foreground, high, or low priority:</span></span>
    -   <span data-ttu-id="f8f7d-115">**前景**：會略過輪詢邏輯，並以機器允許的速度快速進行索引編制。</span><span class="sxs-lookup"><span data-stu-id="f8f7d-115">**Foreground**: Backoff logic is skipped and indexing proceeds as fast as the machine allows.</span></span>
    -   <span data-ttu-id="f8f7d-116">**高**：已使用輪詢要求優先順序。</span><span class="sxs-lookup"><span data-stu-id="f8f7d-116">**High**: Prioritization has been requested with backoff.</span></span>
    -   <span data-ttu-id="f8f7d-117">**低**：已要求優先處理，而不是堆疊上其他範圍的費用，但高於未優先的索引。</span><span class="sxs-lookup"><span data-stu-id="f8f7d-117">**Low**: Prioritization has been requested, not at the expense of other scopes on the stack, but above non-prioritized indexing.</span></span>
-   <span data-ttu-id="f8f7d-118">任何高或前景優先順序的要求都會自動將要求的查詢帶到堆疊的頂端。</span><span class="sxs-lookup"><span data-stu-id="f8f7d-118">Any request for high or foreground priority bumps the requesting query to the top of the stack automatically.</span></span>
-   <span data-ttu-id="f8f7d-119">只有堆疊頂端的專案可以有前景優先順序。</span><span class="sxs-lookup"><span data-stu-id="f8f7d-119">Only the item on top of the stack can have foreground priority.</span></span>
-   <span data-ttu-id="f8f7d-120">具有前景優先順序的查詢會在優先順序中向下遇到，會收到事件，通知它已遺失前景優先順序，且已成為輪詢的高優先權。</span><span class="sxs-lookup"><span data-stu-id="f8f7d-120">A query with foreground priority that is bumped down in priority receives an event notifying it that it has lost foreground priority and has become a high priority with backoff.</span></span>

<span data-ttu-id="f8f7d-121">優先權堆疊會設定在索引子中處理之專案的整體優先順序，如下所示：</span><span class="sxs-lookup"><span data-stu-id="f8f7d-121">The priority stack sets an overall priority of items that are processed in the indexer as follows:</span></span>

-   <span data-ttu-id="f8f7d-122">高優先順序通知沒有輪詢，通常只會針對少數專案傳送。</span><span class="sxs-lookup"><span data-stu-id="f8f7d-122">High Priority notifications have no backoff, and are typically sent only for a small number of items.</span></span> <span data-ttu-id="f8f7d-123">例如，Windows 檔案總管會針對小型複製引擎作業使用此優先順序。</span><span class="sxs-lookup"><span data-stu-id="f8f7d-123">For example, Windows Explorer uses this priority for small copy engine operations.</span></span>
-   <span data-ttu-id="f8f7d-124">優先權堆疊是堆疊的最上層，具有輪詢，而是最後要求的優先權查詢。</span><span class="sxs-lookup"><span data-stu-id="f8f7d-124">Priority Stack is top of the stack, has backoff, and is the last requested priority query.</span></span>
-   <span data-ttu-id="f8f7d-125">堆疊中的第二個查詢。</span><span class="sxs-lookup"><span data-stu-id="f8f7d-125">Second query in the stack.</span></span>
-   <span data-ttu-id="f8f7d-126">堆疊中的第三個查詢。</span><span class="sxs-lookup"><span data-stu-id="f8f7d-126">Third query in the stack.</span></span>
-   <span data-ttu-id="f8f7d-127">堆疊中的第四個查詢等等。</span><span class="sxs-lookup"><span data-stu-id="f8f7d-127">Fourth query in the stack, and so forth.</span></span>
-   <span data-ttu-id="f8f7d-128">一般優先順序專案。</span><span class="sxs-lookup"><span data-stu-id="f8f7d-128">Normal Priority items.</span></span>
-   <span data-ttu-id="f8f7d-129">已刪除的專案。</span><span class="sxs-lookup"><span data-stu-id="f8f7d-129">Deleted items.</span></span>
    > [!Note]  
    > <span data-ttu-id="f8f7d-130">每個群組內的專案會在內部透過較舊的每個專案語義排列優先順序。</span><span class="sxs-lookup"><span data-stu-id="f8f7d-130">Items within each group are prioritized internally through the older per-item semantics.</span></span>

     

### <a name="irowsetpriorization-examples"></a><span data-ttu-id="f8f7d-131">IRowsetPriorization 範例</span><span class="sxs-lookup"><span data-stu-id="f8f7d-131">IRowsetPriorization Examples</span></span>

<span data-ttu-id="f8f7d-132">優先順序工作的主要 API 可透過下列介面取得，您可以藉由查詢傳回的資料列集來呼叫這些 API：</span><span class="sxs-lookup"><span data-stu-id="f8f7d-132">The primary API for prioritization work is available through the following interface, which can be called by querying the returned rowset:</span></span>


```
typedef [v1_enum] enum
{
    PRIORITY_LEVEL_FOREGROUND           = 0,    // process items in the scope first as quickly as possible
    PRIORITY_LEVEL_HIGH                 = 1,    // process items in the scope first at the normal rate
    PRIORITY_LEVEL_LOW                  = 2,    // process items in this scope before those at the normal rate, but after any other prioritization requests
    PRIORITY_LEVEL_DEFAULT              = 3     // process items at the normal indexer rate
} PRIORITY_LEVEL;


[
    object,
    uuid(IRowsetPrioritization_GUID),
    pointer_default(unique)
]
interface IRowsetPrioritization : IUnknown
{
    // Sets or retrieves the current indexer prioritization level for the scope specified by
    // this query.

    HRESULT SetScopePriority( [in] PRIORITY_LEVEL priority, [in] DWORD scopeStatisticsEventFrequency );
    HRESULT GetScopePriority( [out] PRIORITY_LEVEL * priority, [out] DWORD * scopeStatisticsEventFrequency );

    // Gets information describing the scope specified by this query:
    // indexedDocumentCount     -   The total number of documents currently indexed in the scope
    // oustandingAddCount       -   The total number of documents yet to be indexed in the scope (those not yet included in indexedDocumentCount)
    // oustandingModifyCount    -   The total number of documents indexed in the scope that need to be re-indexed (included in indexedDocumentCount)
    
    HRESULT GetScopeStatistics( [out] DWORD * indexedDocumentCount, [out] DWORD * oustandingAddCount, [out] DWORD * oustandingModifyCount );
};
```



<span data-ttu-id="f8f7d-133">資料列集優先順序的運作方式如下：</span><span class="sxs-lookup"><span data-stu-id="f8f7d-133">Rowset prioritization works as follows:</span></span>

1.  <span data-ttu-id="f8f7d-134">在索引子資料列集上使用 [IUnknown：： QueryInterface 方法](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))取得 [**IRowsetPrioritization**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetprioritization) 。</span><span class="sxs-lookup"><span data-stu-id="f8f7d-134">[**IRowsetPrioritization**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetprioritization) is acquired with [IUnknown::QueryInterface Method](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on an indexer rowset.</span></span> <span data-ttu-id="f8f7d-135">**DBPROP \_** 在執行查詢之前，必須先使用 OLE DB [ICommandProperties：： SetProperties](/previous-versions/windows/desktop/ms711497(v=vs.85))方法將 ENABLEROWSETEVENTS 設為 **TRUE** ，才能使用資料列集優先順序。</span><span class="sxs-lookup"><span data-stu-id="f8f7d-135">**DBPROP\_ENABLEROWSETEVENTS** must be set to **TRUE** with the OLE DB [ICommandProperties::SetProperties](/previous-versions/windows/desktop/ms711497(v=vs.85)) method prior to executing the query in order to use rowset prioritization.</span></span>
2.  <span data-ttu-id="f8f7d-136">[**IRowsetPrioritization：： SetScopePriority**](/windows/desktop/api/Searchapi/nf-searchapi-irowsetprioritization-setscopepriority) 會針對屬於查詢的範圍設定優先順序，以及在查詢範圍內有未處理的檔編制索引時，產生範圍統計事件的間隔。</span><span class="sxs-lookup"><span data-stu-id="f8f7d-136">[**IRowsetPrioritization::SetScopePriority**](/windows/desktop/api/Searchapi/nf-searchapi-irowsetprioritization-setscopepriority) sets the prioritization for the scopes belonging to the query, and the interval the scope statistics event is raised when there are outstanding documents to be indexed within the query scopes.</span></span> <span data-ttu-id="f8f7d-137">如果優先權層級設定為 [預設值]，就會引發此事件。</span><span class="sxs-lookup"><span data-stu-id="f8f7d-137">This event is raised if the priority level is set to default.</span></span>
3.  <span data-ttu-id="f8f7d-138">[**IRowsetPrioritization：： GetScopeStatistics**](/windows/desktop/api/Searchapi/nf-searchapi-irowsetprioritization-getscopestatistics) 可用來取得範圍中的索引項目目數、要在範圍中新增的未處理檔數目，以及在此範圍內需要重新編制索引的檔數目。</span><span class="sxs-lookup"><span data-stu-id="f8f7d-138">[**IRowsetPrioritization::GetScopeStatistics**](/windows/desktop/api/Searchapi/nf-searchapi-irowsetprioritization-getscopestatistics) can be used to get the number of indexed items in the scope, the number of outstanding documents to be added in the scope, and the number of documents that need to be re-indexed within this scope.</span></span>

### <a name="irowsetprioritization-events"></a><span data-ttu-id="f8f7d-139">IRowsetPrioritization 事件</span><span class="sxs-lookup"><span data-stu-id="f8f7d-139">IRowsetPrioritization Events</span></span>

<span data-ttu-id="f8f7d-140">[**ROWSETEVENT \_ 類型**](/windows/win32/api/searchapi/ne-searchapi-rowsetevent_type)列舉的 [**IRowsetEvents：： OnRowsetEvent**](/windows/desktop/api/Searchapi/nf-searchapi-irowsetevents-onrowsetevent)中有三個數據列集事件：</span><span class="sxs-lookup"><span data-stu-id="f8f7d-140">There are three rowset events in [**IRowsetEvents::OnRowsetEvent**](/windows/desktop/api/Searchapi/nf-searchapi-irowsetevents-onrowsetevent) in the [**ROWSETEVENT\_TYPE**](/windows/win32/api/searchapi/ne-searchapi-rowsetevent_type) enumeration:</span></span>


```
    // This method allows for future notifications of various actions about your rowset or items within
    // eventType:                               - An identifier of the particular event being sent
    // pVarEventData:                           - The expected value of the EventData for each event type
    //      ROWSETEVENT_TYPE_DATAEXPIRED        - VT_EMPTY
    //      ROWSETEVENT_TYPE_FOREGROUNDLOST     - VT_EMPTY
    //      ROWSETEVENT_TYPE_SCOPESTATISTICS    - VT_VECTOR | VT_UI4 - 3 elements (0 = indexed items, 1 = outstanding adds, 2 = oustanding modifies)

    HRESULT OnRowsetEvent( [in] ROWSETEVENT_TYPE eventType, [in] REFPROPVARIANT eventData );
```



<span data-ttu-id="f8f7d-141">資料列集事件如下所示：</span><span class="sxs-lookup"><span data-stu-id="f8f7d-141">The rowset events are as follows:</span></span>

-   <span data-ttu-id="f8f7d-142">**ROWSETEVENT \_ 類型 \_ DATAEXPIRED** 事件表示支援資料列集的資料已過期，且應要求新的資料列集。</span><span class="sxs-lookup"><span data-stu-id="f8f7d-142">The **ROWSETEVENT\_TYPE\_DATAEXPIRED** event indicates that data backing the rowset has expired, and that a new rowset should be requested.</span></span>
-   <span data-ttu-id="f8f7d-143">資料列 **集 \_ 型別 \_ FOREGROUNDLOST** 事件表示在優先順序堆疊中具有前景優先順序的專案已降級，因為其他人優先處理此查詢。</span><span class="sxs-lookup"><span data-stu-id="f8f7d-143">The **ROWSET\_TYPE\_FOREGROUNDLOST** event indicates that an item that did have foreground priority in the prioritization stack has been demoted, because someone else prioritized themselves ahead of this query.</span></span>
-   <span data-ttu-id="f8f7d-144">**ROWSETEVENT \_ 類型 \_ SCOPESTATISTICS** 事件提供您從 [**IRowsetPrioritization：： GetScopeStatistics**](/windows/desktop/api/Searchapi/nf-searchapi-irowsetprioritization-getscopestatistics)方法呼叫取得的相同資訊，但透過推播技師修理，如下所示：</span><span class="sxs-lookup"><span data-stu-id="f8f7d-144">The **ROWSETEVENT\_TYPE\_SCOPESTATISTICS** event gives you the same information available from the [**IRowsetPrioritization::GetScopeStatistics**](/windows/desktop/api/Searchapi/nf-searchapi-irowsetprioritization-getscopestatistics) method call, but through a push mechanic, as follows:</span></span>
    -   <span data-ttu-id="f8f7d-145">如果已使用優先順序 API 來要求非預設的優先順序層級，以及非零的統計資料事件頻率，就會發生此事件。</span><span class="sxs-lookup"><span data-stu-id="f8f7d-145">The event arises if the prioritization API has been used to request a non-default prioritization level, and a non-zero statistics event frequency.</span></span>
    -   <span data-ttu-id="f8f7d-146">只有當統計資料實際變更，而且 [**IRowsetPrioritization**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetprioritization) 中所指定的間隔已過 (間隔無法保證事件) 的頻率時，才會發生此事件。</span><span class="sxs-lookup"><span data-stu-id="f8f7d-146">The event arises only when statistics actually change, and the interval specified in the [**IRowsetPrioritization**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetprioritization) has elapsed (the interval does not guarantee the frequency of the event).</span></span>
    -   <span data-ttu-id="f8f7d-147">此事件保證會引發「彈跳零」狀態 (剩餘的零個專案，零修改剩餘的) ，但前提是已引發非零的事件。</span><span class="sxs-lookup"><span data-stu-id="f8f7d-147">This event is guaranteed to raise a "bounce zero" state (zero items remaining to be added, zero modifies remaining), provided that a non-zero event has been raised.</span></span>
    -   <span data-ttu-id="f8f7d-148">如果佇列在統計資料事件頻率之前排在佇列中，則索引子可能會處理專案而不傳送此事件。</span><span class="sxs-lookup"><span data-stu-id="f8f7d-148">The indexer may process items without sending this event, if the queue empties before the statistics event frequency.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f8f7d-149">其他資源</span><span class="sxs-lookup"><span data-stu-id="f8f7d-149">Additional Resources</span></span>

<span data-ttu-id="f8f7d-150">請參閱下列與優先順序和資料列集相關的資源：</span><span class="sxs-lookup"><span data-stu-id="f8f7d-150">See the following resources related to prioritization and rowsets:</span></span>

-   <span data-ttu-id="f8f7d-151">介面：</span><span class="sxs-lookup"><span data-stu-id="f8f7d-151">Interfaces:</span></span>
    -   [<span data-ttu-id="f8f7d-152">**IRowsetEvents**</span><span class="sxs-lookup"><span data-stu-id="f8f7d-152">**IRowsetEvents**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-irowsetevents)
    -   [<span data-ttu-id="f8f7d-153">**IRowsetPrioritization**</span><span class="sxs-lookup"><span data-stu-id="f8f7d-153">**IRowsetPrioritization**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-irowsetprioritization)
-   <span data-ttu-id="f8f7d-154">枚舉：</span><span class="sxs-lookup"><span data-stu-id="f8f7d-154">Enumerations:</span></span>
    -   [<span data-ttu-id="f8f7d-155">**設定 \_ 旗標的優先順序**</span><span class="sxs-lookup"><span data-stu-id="f8f7d-155">**PRIORITIZE\_FLAGS**</span></span>](/windows/win32/api/searchapi/ne-searchapi-tagprioritize_flags)
    -   [<span data-ttu-id="f8f7d-156">**優先權 \_ 層級**</span><span class="sxs-lookup"><span data-stu-id="f8f7d-156">**PRIORITY\_LEVEL**</span></span>](/windows/win32/api/searchapi/ne-searchapi-priority_level)
    -   [<span data-ttu-id="f8f7d-157">**ROWSETEVENT \_ ITEMSTATE**</span><span class="sxs-lookup"><span data-stu-id="f8f7d-157">**ROWSETEVENT\_ITEMSTATE**</span></span>](/windows/win32/api/searchapi/ne-searchapi-rowsetevent_itemstate)
    -   [<span data-ttu-id="f8f7d-158">**ROWSETEVENT \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="f8f7d-158">**ROWSETEVENT\_TYPE**</span></span>](/windows/win32/api/searchapi/ne-searchapi-rowsetevent_type)

## <a name="related-topics"></a><span data-ttu-id="f8f7d-159">相關主題</span><span class="sxs-lookup"><span data-stu-id="f8f7d-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f8f7d-160">Windows 7 搜尋</span><span class="sxs-lookup"><span data-stu-id="f8f7d-160">Windows 7 Search</span></span>](./-search-3x-wds-overview.md)
</dt> <dt>

[<span data-ttu-id="f8f7d-161">適用于 Windows 7 搜尋的新</span><span class="sxs-lookup"><span data-stu-id="f8f7d-161">New for Windows 7 Search</span></span>](new-for-windows-7-search.md)
</dt> <dt>

[<span data-ttu-id="f8f7d-162">Windows 7 中的 windows Shell 程式庫</span><span class="sxs-lookup"><span data-stu-id="f8f7d-162">Windows Shell Libraries in Windows 7</span></span>](-search-win7-development-scenarios.md)
</dt> </dl>

 

 