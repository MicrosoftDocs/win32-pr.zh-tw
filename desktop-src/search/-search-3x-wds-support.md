---
description: Windows Search 中的通知處理
ms.assetid: 378e346b-2067-484f-85e9-76673a35550b
title: Windows Search 中的通知處理
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b37747d1ec13c3a4a865e16721c64d4a0186dbc
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089816"
---
# <a name="notifications-process-in-windows-search"></a><span data-ttu-id="cff24-103">Windows Search 中的通知處理</span><span class="sxs-lookup"><span data-stu-id="cff24-103">Notifications Process in Windows Search</span></span>

<span data-ttu-id="cff24-104">本主題的組織方式如下：</span><span class="sxs-lookup"><span data-stu-id="cff24-104">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="cff24-105">通知流程的總覽</span><span class="sxs-lookup"><span data-stu-id="cff24-105">Overview of the Notifications Process</span></span>](#overview-of-the-notifications-process)
-   [<span data-ttu-id="cff24-106">爬</span><span class="sxs-lookup"><span data-stu-id="cff24-106">Crawls</span></span>](#crawls)
-   [<span data-ttu-id="cff24-107">索引子管理的通知</span><span class="sxs-lookup"><span data-stu-id="cff24-107">Indexer-Managed Notifications</span></span>](#indexer-managed-notifications)
-   [<span data-ttu-id="cff24-108">提供者管理的通知</span><span class="sxs-lookup"><span data-stu-id="cff24-108">Provider-Managed Notifications</span></span>](#provider-managed-notifications)
-   [<span data-ttu-id="cff24-109">資料列集的通知</span><span class="sxs-lookup"><span data-stu-id="cff24-109">Notifications on Rowsets</span></span>](#notifications-on-rowsets)
-   [<span data-ttu-id="cff24-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="cff24-110">Related topics</span></span>](#related-topics)

## <a name="overview-of-the-notifications-process"></a><span data-ttu-id="cff24-111">通知流程的總覽</span><span class="sxs-lookup"><span data-stu-id="cff24-111">Overview of the Notifications Process</span></span>

<span data-ttu-id="cff24-112">有三種方法可將資料存放區中的資料編制索引：</span><span class="sxs-lookup"><span data-stu-id="cff24-112">There are three approaches by which data from your data store can be indexed:</span></span>

-   <span data-ttu-id="cff24-113">爬</span><span class="sxs-lookup"><span data-stu-id="cff24-113">Crawls</span></span>
-   <span data-ttu-id="cff24-114">索引子管理的通知</span><span class="sxs-lookup"><span data-stu-id="cff24-114">Indexer-managed notifications</span></span>
-   <span data-ttu-id="cff24-115">提供者管理的通知</span><span class="sxs-lookup"><span data-stu-id="cff24-115">Provider-managed notifications</span></span>

<span data-ttu-id="cff24-116">下列各節將說明每個方法的優點。</span><span class="sxs-lookup"><span data-stu-id="cff24-116">The merits of each approach are described in the following sections.</span></span>

## <a name="crawls"></a><span data-ttu-id="cff24-117">爬</span><span class="sxs-lookup"><span data-stu-id="cff24-117">Crawls</span></span>

<span data-ttu-id="cff24-118">啟用通知的來源會在啟動時進行累加式編目，然後依賴通知或明確的命令來再次編目。</span><span class="sxs-lookup"><span data-stu-id="cff24-118">Notification-enabled sources do an incremental crawl on start-up and then rely on notifications or an explicit command to crawl again.</span></span> <span data-ttu-id="cff24-119">這會在 Windows Vista 和更新版本上自動發生。</span><span class="sxs-lookup"><span data-stu-id="cff24-119">This happens automatically on Windows Vista and later.</span></span> <span data-ttu-id="cff24-120">在 Windows Vista 之前的作業系統上，您必須在 [工作排程器](../taskschd/task-scheduler-start-page.md) 中設定已排程的事件，以呼叫您的程式碼，以起始 (s) 的起始頁編目。</span><span class="sxs-lookup"><span data-stu-id="cff24-120">On operating systems prior to Windows Vista, you must set up a scheduled event in the [Task Scheduler](../taskschd/task-scheduler-start-page.md) that calls into your code to initiate a crawl over your start page(s).</span></span> <span data-ttu-id="cff24-121">您不需要執行任何形式的通知。</span><span class="sxs-lookup"><span data-stu-id="cff24-121">You do not need to implement any form of notifications.</span></span> <span data-ttu-id="cff24-122">在背景進程中，索引子會取得其編目範圍、尋找變更和更新目錄。</span><span class="sxs-lookup"><span data-stu-id="cff24-122">As a background process, the indexer traverses its crawl scope, looking for changes and updating the catalog.</span></span> <span data-ttu-id="cff24-123">在幾乎所有情況下，建議使用這個選項。</span><span class="sxs-lookup"><span data-stu-id="cff24-123">This option is recommended for almost all situations.</span></span>

## <a name="indexer-managed-notifications"></a><span data-ttu-id="cff24-124">Indexer-Managed 通知</span><span class="sxs-lookup"><span data-stu-id="cff24-124">Indexer-Managed Notifications</span></span>

<span data-ttu-id="cff24-125">利用索引子管理的通知，您可以執行通知策略，以在資料存放區中的資料已變更時通知索引子，而索引子會管理追蹤通知和編制資料索引。</span><span class="sxs-lookup"><span data-stu-id="cff24-125">With indexer-managed notifications, you implement a notification strategy that notifies the indexer when data in the data store has changed, and the indexer manages tracking the notifications and indexing the data.</span></span> <span data-ttu-id="cff24-126">在這種情況下，您的元件 (我們將呼叫通知提供者) 監視資料存放區、收集儲存變更的相關資訊，然後使用需要編制索引的專案清單定期通知索引子。</span><span class="sxs-lookup"><span data-stu-id="cff24-126">In this situation, your component (which we'll call a notifications provider) monitors the data store, collects information about changes to the store, and then periodically notifies the indexer with a list of items that need indexing.</span></span> <span data-ttu-id="cff24-127">索引子會負責復原和解決失敗時的通知。</span><span class="sxs-lookup"><span data-stu-id="cff24-127">The indexer is responsible for recovering and resolving notifications in case of failure.</span></span> <span data-ttu-id="cff24-128">這個選項（您可以將它視為「傳送它並忘記密碼」策略）可減少索引子編目的頻率。</span><span class="sxs-lookup"><span data-stu-id="cff24-128">This option, which you can think of as the "send it and forget it" strategy, reduces the frequency of indexer crawls.</span></span>

## <a name="provider-managed-notifications"></a><span data-ttu-id="cff24-129">Provider-Managed 通知</span><span class="sxs-lookup"><span data-stu-id="cff24-129">Provider-Managed Notifications</span></span>

<span data-ttu-id="cff24-130">透過提供者管理的通知，您可以執行類似于第二個方法的通知策略，不同之處在于您的通知提供者必須追蹤通知，並負責在發生失敗時復原和解決通知。</span><span class="sxs-lookup"><span data-stu-id="cff24-130">With provider-managed notifications, you implement a notification strategy that is similar to the second approach, except that your notifications provider must track notifications and is responsible for recovering and resolving notifications in case of failure.</span></span> <span data-ttu-id="cff24-131">在此情況下，您的通知提供者會監視資料存放區、收集和維護存放區變更的相關資訊、定期通知索引子，其中包含需要編制索引的專案清單、接收來自索引子的狀態更新，並在發生失敗時重新傳送通知。</span><span class="sxs-lookup"><span data-stu-id="cff24-131">In this situation, your notifications provider monitors the data store, collects and maintains information about changes to the store, periodically notifies the indexer with a list of items that need indexing, receives status updates from the indexer, and re-sends notifications in case of failure.</span></span>

> [!Note]  
> <span data-ttu-id="cff24-132">除非您預期資料存放區的累加式編目會大幅降低效能，而且您需要更細微地控制或深入瞭解索引狀態，否則 **不建議使用** 此選項。</span><span class="sxs-lookup"><span data-stu-id="cff24-132">This option is **not recommended unless** you expect incremental crawls of your data store to hinder performance significantly, and you require granular control over or insight into the indexing status.</span></span>

 

## <a name="notifications-on-rowsets"></a><span data-ttu-id="cff24-133">資料列集的通知</span><span class="sxs-lookup"><span data-stu-id="cff24-133">Notifications on Rowsets</span></span>

<span data-ttu-id="cff24-134">在 Windows 7 和更新版本中，索引編制事件可讓提供者接收其資料列集的通知。</span><span class="sxs-lookup"><span data-stu-id="cff24-134">In Windows 7 and later, indexing eventing enables providers to receive notifications about their rowsets.</span></span> <span data-ttu-id="cff24-135">使用索引編制事件的提供者可以用類似實際檔案系統位置行為的方式來維護其資料列集。</span><span class="sxs-lookup"><span data-stu-id="cff24-135">Providers that use indexing eventing can maintain their rowsets in a manner that resembles the behavior of actual file system locations.</span></span> <span data-ttu-id="cff24-136">程式庫和搜尋是 Windows 7 中非檔案系統位置的主要範例。</span><span class="sxs-lookup"><span data-stu-id="cff24-136">Libraries and searches are the primary examples of non-file-system locations in Windows 7.</span></span> <span data-ttu-id="cff24-137">索引子事件就是程式庫視圖，因為通知是檔案資料夾的視圖。</span><span class="sxs-lookup"><span data-stu-id="cff24-137">Indexer eventing is to library views as notifications are to file-folder views.</span></span> <span data-ttu-id="cff24-138">必須執行 [**IRowsetEvents**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetevents) 介面，才能接收事件的通知。</span><span class="sxs-lookup"><span data-stu-id="cff24-138">The [**IRowsetEvents**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetevents) interface must be implemented in order to receive notifications of events.</span></span> <span data-ttu-id="cff24-139">資料層是索引子事件的主要用戶端，並決定要如何處理 Items View UI 中的事件。</span><span class="sxs-lookup"><span data-stu-id="cff24-139">The data layer is the primary client of indexer eventing, and decides what to do with events in the Items View UI.</span></span> <span data-ttu-id="cff24-140">如需詳細資訊，請參閱 [在 Windows 7 中編制優先順序和資料列集事件的索引](indexing-prioritization-and-rowset-events.md)。</span><span class="sxs-lookup"><span data-stu-id="cff24-140">For more information, see [Indexing Prioritization and Rowset Events in Windows 7](indexing-prioritization-and-rowset-events.md).</span></span>

<span data-ttu-id="cff24-141">相反地，在 Windows Vista 中，以查詢為基礎的視圖沒有相關聯的事件，但檔案屬性編輯的 Shell 快取除外。</span><span class="sxs-lookup"><span data-stu-id="cff24-141">In contrast, in Windows Vista, query based views have no associated eventing, except for the Shell cache for file property edits.</span></span> <span data-ttu-id="cff24-142">當您執行搜尋時，傳回的結果是靜態的。</span><span class="sxs-lookup"><span data-stu-id="cff24-142">When you perform a search, the results that are returned are static.</span></span> <span data-ttu-id="cff24-143">因此，如果您的系統中新增了與搜尋字詞相符的另一份檔，則您的 view 不會更新為包含新的新增專案。</span><span class="sxs-lookup"><span data-stu-id="cff24-143">Hence, if another document is added to your system that matches your search term, your view is not updated to include the new addition.</span></span> <span data-ttu-id="cff24-144">這是靜態 web 型結果的標準行為。</span><span class="sxs-lookup"><span data-stu-id="cff24-144">This behavior is standard for static web-based results.</span></span> <span data-ttu-id="cff24-145">但是，當您嘗試在儲存位置上提供以查詢為基礎的視圖時，靜態結果較不容易接受。</span><span class="sxs-lookup"><span data-stu-id="cff24-145">However, static results are less acceptable when you are trying to provide a query-based view over a storage location.</span></span> <span data-ttu-id="cff24-146">使用者預期索引子的內容是最新的。</span><span class="sxs-lookup"><span data-stu-id="cff24-146">Users expect that content from the indexer is current.</span></span> <span data-ttu-id="cff24-147">如需詳細資訊，請參閱 [通知索引的變更](-search-3x-wds-notifyingofchanges.md)。</span><span class="sxs-lookup"><span data-stu-id="cff24-147">For more information, see [Notifying the Index of Changes](-search-3x-wds-notifyingofchanges.md).</span></span> <span data-ttu-id="cff24-148">如需參考檔，請參閱 [通知介面](-search-notifications-interfaces-entry-page.md)。</span><span class="sxs-lookup"><span data-stu-id="cff24-148">For reference documentation, see [Notifications Interfaces](-search-notifications-interfaces-entry-page.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="cff24-149">相關主題</span><span class="sxs-lookup"><span data-stu-id="cff24-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cff24-150">Windows Search 中的編制索引、查詢和通知</span><span class="sxs-lookup"><span data-stu-id="cff24-150">Indexing, Querying and Notifications in Windows Search</span></span>](-search-3x-wds-included-in-index.md)
</dt> <dt>

[<span data-ttu-id="cff24-151">索引中包含的內容</span><span class="sxs-lookup"><span data-stu-id="cff24-151">What is Included in the Index</span></span>](-search-indexing-process-overview.md)
</dt> <dt>

[<span data-ttu-id="cff24-152">Windows Search 中的編制索引進程</span><span class="sxs-lookup"><span data-stu-id="cff24-152">Indexing Process in Windows Search</span></span>](-search-indexing-process-overview.md)
</dt> <dt>

[<span data-ttu-id="cff24-153">在 Windows Search 中查詢進程</span><span class="sxs-lookup"><span data-stu-id="cff24-153">Querying Process in Windows Search</span></span>](querying-process--windows-search-.md)
</dt> <dt>

[<span data-ttu-id="cff24-154">URL 格式設定需求</span><span class="sxs-lookup"><span data-stu-id="cff24-154">URL Formatting Requirements</span></span>](url-formatting-requirements.md)
</dt> </dl>

 

 
