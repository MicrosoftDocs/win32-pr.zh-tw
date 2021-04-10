---
title: '通知 (舊版 Windows 環境功能的變更索引) '
description: 使用 Microsoft Windows 桌面搜尋 (WDS) 2.6，指定資料存放區的通訊協定處理常式可以在其存放區中的資料變更時，告訴 WDS 索引子。
ms.assetid: 700b1707-dd11-4a30-8f00-5c4aae1173ff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6021cfe5cd7061a3d3255e56d08e665a6caedf03
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104187269"
---
# <a name="notifying-the-index-of-changes-legacy-windows-environment-features"></a><span data-ttu-id="ccb43-103">通知 (舊版 Windows 環境功能的變更索引) </span><span class="sxs-lookup"><span data-stu-id="ccb43-103">Notifying the Index of Changes (Legacy Windows Environment Features)</span></span>

> [!NOTE]
> <span data-ttu-id="ccb43-104">Windows Desktop Search 2.x 是一種淘汰的技術，最初是以 Windows XP 和 Windows Server 2003 的增益集形式提供。</span><span class="sxs-lookup"><span data-stu-id="ccb43-104">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="ccb43-105">在之後的版本中，請改用 [Windows Search](../search/-search-3x-wds-overview.md) 。</span><span class="sxs-lookup"><span data-stu-id="ccb43-105">On later releases, use [Windows Search](../search/-search-3x-wds-overview.md) instead.</span></span>

<span data-ttu-id="ccb43-106">使用 Microsoft Windows 桌面搜尋 (WDS) 2.6，指定資料存放區的通訊協定處理常式可以在其存放區中的資料變更時，告訴 WDS 索引子。</span><span class="sxs-lookup"><span data-stu-id="ccb43-106">With Microsoft Windows Desktop Search (WDS) 2.6, protocol handlers for a given data store can tell the WDS Indexer when data in their store has changed.</span></span> <span data-ttu-id="ccb43-107">這可確保索引子不會在累加式索引上編目整個存放區，以改善效能。</span><span class="sxs-lookup"><span data-stu-id="ccb43-107">This improves performance by ensuring the Indexer doesn't crawl the entire store on incremental indexes.</span></span> <span data-ttu-id="ccb43-108">使用通知 Api 時，通訊協定處理常式可以通知索引子已移動或刪除專案，而且可以將範圍新增至需要編制索引之 Url 的 WDS 索引子編目佇列。</span><span class="sxs-lookup"><span data-stu-id="ccb43-108">Using notification APIs, protocol handlers can notify the Indexer that an item has been moved or deleted, and they can add scopes to the WDS Indexer's crawl queue of URLs requiring indexing.</span></span> <span data-ttu-id="ccb43-109">通知對電子郵件之類的應用程式很有説明，因為通訊協定處理常式會監視存放區，並通知索引子該專案已變更且需要編制索引。</span><span class="sxs-lookup"><span data-stu-id="ccb43-109">Notification is helpful for applications such as email, where the protocol handler monitors the store and notifies the Indexer that items have changed and require indexing.</span></span>

## <a name="isearchitemschangedsink"></a><span data-ttu-id="ccb43-110">ISearchItemsChangedSink</span><span class="sxs-lookup"><span data-stu-id="ccb43-110">ISearchItemsChangedSink</span></span>

<span data-ttu-id="ccb43-111">通訊協定處理常式會透過 [**ISearchItemsChangedSink**](/windows/desktop/api/searchapi/nn-searchapi-isearchitemschangedsink) 介面通知索引子的變更。</span><span class="sxs-lookup"><span data-stu-id="ccb43-111">Protocol handlers notify the Indexer of changes through the [**ISearchItemsChangedSink**](/windows/desktop/api/searchapi/nn-searchapi-isearchitemschangedsink) interface.</span></span> <span data-ttu-id="ccb43-112">您應該在搜尋 \_ 專案變更結構和搜尋類型的變更列舉型別中收集資料變更的相關資訊 \_ ，然後 \_ \_ \_ 透過 **ISearchItemsChangedSink** 介面的 **OnItemsChanged** 方法，傳達給索引子。</span><span class="sxs-lookup"><span data-stu-id="ccb43-112">Information about data changes should be collected in SEARCH\_ITEM\_CHANGE structs and SEARCH\_KIND\_OF\_CHANGE enumeration types and then communicated to the Indexer through the **OnItemsChanged** method of the **ISearchItemsChangedSink** interface.</span></span>

<span data-ttu-id="ccb43-113">若要存取此介面，自訂通訊協定處理常式必須先具現化 [**ISearchManager**](/windows/desktop/api/searchapi/nn-searchapi-isearchmanager) 物件，以取得 [**ISearchCatalogManager**](/windows/desktop/api/searchapi/nn-searchapi-isearchcatalogmanager) 物件的存取權。</span><span class="sxs-lookup"><span data-stu-id="ccb43-113">To access this interface, a custom protocol handlers must first instantiate an [**ISearchManager**](/windows/desktop/api/searchapi/nn-searchapi-isearchmanager) object to gain access to the [**ISearchCatalogManager**](/windows/desktop/api/searchapi/nn-searchapi-isearchcatalogmanager) object.</span></span> <span data-ttu-id="ccb43-114">從該處，您可以具現化 [**ISearchItemsChangedSink**](/windows/desktop/api/searchapi/nn-searchapi-isearchitemschangedsink) 物件，並通知索引子資料變更。</span><span class="sxs-lookup"><span data-stu-id="ccb43-114">From there, one can instantiate an [**ISearchItemsChangedSink**](/windows/desktop/api/searchapi/nn-searchapi-isearchitemschangedsink) object and notify the Indexer of the data changes.</span></span>

<span data-ttu-id="ccb43-115">OnItemsChanged 方法可讓您收集資料變更並與客戶資料存放區進行通訊，以起始索引。</span><span class="sxs-lookup"><span data-stu-id="ccb43-115">The OnItemsChanged method lets you collect and communicate data changes to your customer data store to initiate indexing.</span></span>



| <span data-ttu-id="ccb43-116">方向</span><span class="sxs-lookup"><span data-stu-id="ccb43-116">Direction</span></span> | <span data-ttu-id="ccb43-117">變數</span><span class="sxs-lookup"><span data-stu-id="ccb43-117">Variable</span></span>              | <span data-ttu-id="ccb43-118">描述</span><span class="sxs-lookup"><span data-stu-id="ccb43-118">Description</span></span>                                                              |
|-----------|-----------------------|--------------------------------------------------------------------------|
| <span data-ttu-id="ccb43-119">位於</span><span class="sxs-lookup"><span data-stu-id="ccb43-119">In</span></span>        | <span data-ttu-id="ccb43-120">dwNumberofChanges</span><span class="sxs-lookup"><span data-stu-id="ccb43-120">dwNumberofChanges</span></span>     | <span data-ttu-id="ccb43-121">通知中的變更總數。</span><span class="sxs-lookup"><span data-stu-id="ccb43-121">Total number of changes in the notification.</span></span>                             |
| <span data-ttu-id="ccb43-122">位於</span><span class="sxs-lookup"><span data-stu-id="ccb43-122">In</span></span>        | <span data-ttu-id="ccb43-123">DataChangeEntries\[\]</span><span class="sxs-lookup"><span data-stu-id="ccb43-123">DataChangeEntries\[\]</span></span> | <span data-ttu-id="ccb43-124">搜尋專案的陣列中的所有變更通知都會 \_ \_ 變更結構。</span><span class="sxs-lookup"><span data-stu-id="ccb43-124">All change notifications in an array of SEARCH\_ITEM\_CHANGE structures.</span></span> |
| <span data-ttu-id="ccb43-125">外</span><span class="sxs-lookup"><span data-stu-id="ccb43-125">Out</span></span>       | <span data-ttu-id="ccb43-126">dwBatchId</span><span class="sxs-lookup"><span data-stu-id="ccb43-126">dwBatchId</span></span>             | <span data-ttu-id="ccb43-127">將傳回錯誤的批次識別碼。</span><span class="sxs-lookup"><span data-stu-id="ccb43-127">The batch ID that will be passed back with errors.</span></span>                       |
| <span data-ttu-id="ccb43-128">外</span><span class="sxs-lookup"><span data-stu-id="ccb43-128">Out</span></span>       | <span data-ttu-id="ccb43-129">hrCompletionCodes\[\]</span><span class="sxs-lookup"><span data-stu-id="ccb43-129">hrCompletionCodes\[\]</span></span> | <span data-ttu-id="ccb43-130">指出是否接受每個 URL 來編制索引。</span><span class="sxs-lookup"><span data-stu-id="ccb43-130">Indicates whether each URL was accepted for indexing.</span></span>                    |



 

<span data-ttu-id="ccb43-131">搜尋 \_ 專案 \_ 變更結構會識別發生的變更種類，以及專案目前的 url 和先前的 url （如果適用）。</span><span class="sxs-lookup"><span data-stu-id="ccb43-131">The SEARCH\_ITEM\_CHANGE structure identifies the kind of change that occurred as well as the item's current URL and previous URL, if applicable.</span></span> <span data-ttu-id="ccb43-132">結構的定義如下：</span><span class="sxs-lookup"><span data-stu-id="ccb43-132">The structure is defined as follows:</span></span>



| <span data-ttu-id="ccb43-133">屬性名稱</span><span class="sxs-lookup"><span data-stu-id="ccb43-133">Property Name</span></span> | <span data-ttu-id="ccb43-134">屬性類型</span><span class="sxs-lookup"><span data-stu-id="ccb43-134">Property Type</span></span>                  | <span data-ttu-id="ccb43-135">Description</span><span class="sxs-lookup"><span data-stu-id="ccb43-135">Description</span></span>                                                                |
|---------------|--------------------------------|----------------------------------------------------------------------------|
| <span data-ttu-id="ccb43-136">變更</span><span class="sxs-lookup"><span data-stu-id="ccb43-136">Change</span></span>        | <span data-ttu-id="ccb43-137">搜尋 \_ \_ 變更種類 \_</span><span class="sxs-lookup"><span data-stu-id="ccb43-137">SEARCH\_KIND\_OF\_CHANGE</span></span>       | <span data-ttu-id="ccb43-138">要通知的變更類型。</span><span class="sxs-lookup"><span data-stu-id="ccb43-138">The type of change that is being notified.</span></span>                                 |
| <span data-ttu-id="ccb43-139">URL</span><span class="sxs-lookup"><span data-stu-id="ccb43-139">URL</span></span>           | <span data-ttu-id="ccb43-140">LPWSTR</span><span class="sxs-lookup"><span data-stu-id="ccb43-140">LPWSTR</span></span>                         | <span data-ttu-id="ccb43-141">已變更之物件的 URL。</span><span class="sxs-lookup"><span data-stu-id="ccb43-141">The URL for the object that has changed.</span></span>                                   |
| <span data-ttu-id="ccb43-142">OldURL</span><span class="sxs-lookup"><span data-stu-id="ccb43-142">OldURL</span></span>        | <span data-ttu-id="ccb43-143">LPWSTR</span><span class="sxs-lookup"><span data-stu-id="ccb43-143">LPWSTR</span></span>                         | <span data-ttu-id="ccb43-144">如果通知是移動，則會提供舊的 URL，而且必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="ccb43-144">If the notification is a move, the old URL is provided and must be unique.</span></span> |
| <span data-ttu-id="ccb43-145">優先順序</span><span class="sxs-lookup"><span data-stu-id="ccb43-145">Priority</span></span>      | <span data-ttu-id="ccb43-146">搜尋 \_ 通知 \_ 優先順序</span><span class="sxs-lookup"><span data-stu-id="ccb43-146">SEARCH\_NOTIFICATION\_PRIORITY</span></span> | <span data-ttu-id="ccb43-147">變更的優先順序。</span><span class="sxs-lookup"><span data-stu-id="ccb43-147">The priority of the change.</span></span>                                                |



 

<span data-ttu-id="ccb43-148">\_變更列舉的搜尋種類 \_ 定義如下 \_ ：</span><span class="sxs-lookup"><span data-stu-id="ccb43-148">The SEARCH\_KIND\_OF\_CHANGE enumeration is defined as follows:</span></span>



| <span data-ttu-id="ccb43-149">列舉值</span><span class="sxs-lookup"><span data-stu-id="ccb43-149">Enum Value</span></span>                           | <span data-ttu-id="ccb43-150">值</span><span class="sxs-lookup"><span data-stu-id="ccb43-150">Value</span></span>   | <span data-ttu-id="ccb43-151">描述</span><span class="sxs-lookup"><span data-stu-id="ccb43-151">Description</span></span>                                                                                     |
|--------------------------------------|---------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ccb43-152">搜尋 \_ 變更 \_ 新增</span><span class="sxs-lookup"><span data-stu-id="ccb43-152">SEARCH\_CHANGE\_ADD</span></span>                  | <span data-ttu-id="ccb43-153">0</span><span class="sxs-lookup"><span data-stu-id="ccb43-153">0</span></span>       | <span data-ttu-id="ccb43-154">通知是針對額外的 URL。</span><span class="sxs-lookup"><span data-stu-id="ccb43-154">The notification is for an additional URL.</span></span>                                                      |
| <span data-ttu-id="ccb43-155">搜尋 \_ 變更 \_ 刪除</span><span class="sxs-lookup"><span data-stu-id="ccb43-155">SEARCH\_CHANGE\_DELETE</span></span>               | <span data-ttu-id="ccb43-156">1</span><span class="sxs-lookup"><span data-stu-id="ccb43-156">1</span></span>       | <span data-ttu-id="ccb43-157">通知是用來刪除 URL。</span><span class="sxs-lookup"><span data-stu-id="ccb43-157">The notification is for the deletion of a URL.</span></span>                                                  |
| <span data-ttu-id="ccb43-158">搜尋 \_ 變更 \_ 修改</span><span class="sxs-lookup"><span data-stu-id="ccb43-158">SEARCH\_CHANGE\_MODIFY</span></span>               | <span data-ttu-id="ccb43-159">2</span><span class="sxs-lookup"><span data-stu-id="ccb43-159">2</span></span>       | <span data-ttu-id="ccb43-160">通知是 URL 已經修改過了。</span><span class="sxs-lookup"><span data-stu-id="ccb43-160">The notification is that a URL has been modified.</span></span>                                               |
| <span data-ttu-id="ccb43-161">搜尋 \_ 變更 \_ 移動 \_ 重新命名</span><span class="sxs-lookup"><span data-stu-id="ccb43-161">SEARCH\_CHANGE\_MOVE\_RENAME</span></span>         | <span data-ttu-id="ccb43-162">3</span><span class="sxs-lookup"><span data-stu-id="ccb43-162">3</span></span>       | <span data-ttu-id="ccb43-163">通知是用來將物件的移動和重新命名為新的 URL。</span><span class="sxs-lookup"><span data-stu-id="ccb43-163">The notification is for the move and rename of an object to a new URL.</span></span>                          |
| <span data-ttu-id="ccb43-164">搜尋 \_ 變更 \_ 語義 \_ 目錄</span><span class="sxs-lookup"><span data-stu-id="ccb43-164">SEARCH\_CHANGE\_SEMANTICS\_DIRECTORY</span></span> | <span data-ttu-id="ccb43-165">0x10000</span><span class="sxs-lookup"><span data-stu-id="ccb43-165">0x10000</span></span> | <span data-ttu-id="ccb43-166">通知適用于容器 URL。</span><span class="sxs-lookup"><span data-stu-id="ccb43-166">The notification is for a container URL.</span></span>                                                        |
| <span data-ttu-id="ccb43-167">搜尋 \_ 變更 \_ 語義 \_ 淺層</span><span class="sxs-lookup"><span data-stu-id="ccb43-167">SEARCH\_CHANGE\_SEMANTICS\_SHALLOW</span></span>   | <span data-ttu-id="ccb43-168">0x20000</span><span class="sxs-lookup"><span data-stu-id="ccb43-168">0x20000</span></span> | <span data-ttu-id="ccb43-169">這項通知適用于應只將其容器屬性編制索引的容器 URL。</span><span class="sxs-lookup"><span data-stu-id="ccb43-169">The notification is for a container URL that should only have its container properties indexed.</span></span> |
| <span data-ttu-id="ccb43-170">搜尋 \_ 變更 \_ 語義 \_ 安全性</span><span class="sxs-lookup"><span data-stu-id="ccb43-170">SEARCH\_CHANGE\_SEMANTICS\_SECURITY</span></span>  | <span data-ttu-id="ccb43-171">0x40000</span><span class="sxs-lookup"><span data-stu-id="ccb43-171">0x40000</span></span> | <span data-ttu-id="ccb43-172">通知是針對已變更其安全性屬性的 URL 或容器 URL。</span><span class="sxs-lookup"><span data-stu-id="ccb43-172">The notification is for a URL or container URL that has had its security properties changed.</span></span>    |



 

<span data-ttu-id="ccb43-173">搜尋 \_ 通知 \_ 優先順序列舉定義如下：</span><span class="sxs-lookup"><span data-stu-id="ccb43-173">The SEARCH\_NOTIFICATION\_PRIORITY enumeration is defined as follows:</span></span>



| <span data-ttu-id="ccb43-174">列舉值</span><span class="sxs-lookup"><span data-stu-id="ccb43-174">Enum Value</span></span>               | <span data-ttu-id="ccb43-175">值</span><span class="sxs-lookup"><span data-stu-id="ccb43-175">Value</span></span> | <span data-ttu-id="ccb43-176">描述</span><span class="sxs-lookup"><span data-stu-id="ccb43-176">Description</span></span>                                                                                                                                                                    |
|--------------------------|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ccb43-177">搜尋 \_ 正常 \_ 優先順序</span><span class="sxs-lookup"><span data-stu-id="ccb43-177">SEARCH\_NORMAL\_PRIORITY</span></span> | <span data-ttu-id="ccb43-178">0</span><span class="sxs-lookup"><span data-stu-id="ccb43-178">0</span></span>     | <span data-ttu-id="ccb43-179">索引 URL 時，應該只使用一般的優先權。</span><span class="sxs-lookup"><span data-stu-id="ccb43-179">Only a normal priority should be used when indexing the URL.</span></span> <span data-ttu-id="ccb43-180">這些通知會在使用者的檔案和存放區的一般背景累加式編制索引之前進行處理。</span><span class="sxs-lookup"><span data-stu-id="ccb43-180">These notifications are processed before the normal background incremental indexing of a user's files and stores.</span></span> |



 

 

 
